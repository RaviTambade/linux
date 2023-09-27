<h2>File Permissions</h2>

<p>On a Linux system, each file and directory is assigned access rights for the
owner of the file, the members of a group of related users, and everybody else.
Rights can be assigned to read a file, to write a file, and to execute a file
(i.e., run the file as a program).</p>

### What do Linux file permissions actually do?
I've talked about how to view file permissions, who they apply to, and how to read what permissions are enabled or disabled. But what do these permissions actually do in practice?

- <b>Read (r)</b>
Read permission is used to access the file's contents. You can use a tool like cat or less on the file to display the file contents. You could also use a text editor like Vi or view on the file to display the contents of the file. Read permission is required to make copies of a file, because you need to access the file's contents to make a duplicate of it.

- <b>Write (w)</b>
Write permission allows you to modify or change the contents of a file. Write permission also allows you to use the redirect or append operators in the shell (> or >>) to change the contents of a file. Without write permission, changes to the file's contents are not permitted.

- <b>Execute (x)</b>
Execute permission allows you to execute the contents of a file. Typically, executables would be things like commands or compiled binary applications. However, execute permission also allows someone to run Bash shell scripts, Python programs, and a variety of interpreted languages.



<p>To see the permission settings for a file, we can use the <code
class="user">ls</code> command.  As an example, we will look at the <code
class="user">bash</code> program which is located in the <code>/bin</code>
directory:</p>

```
[me@linuxbox me]$ ls -l /bin/bash
-rwxr-xr-x 1 root root 1113504 Sept  27  2023 /bin/bash
```
<p>Here we can see:</p>

<ul>
  <li>The file "/bin/bash" is owned by user
  "root"</li>

  <li>The superuser has the right to read, write,
  and execute this file</li>

  <li>The file is owned by the group "root"</li>

  <li>Members of the group "root" can also read and
  execute this file</li>

  <li>Everybody else can read and execute this
  file</li>
</ul>

<p>In the diagram below, we see how the first portion of the listing is
interpreted. It consists of a character indicating the file type, followed by
three sets of three characters that convey the reading, writing and execution
permission for the owner, group, and everybody else.<br><br>

<img src="/images/permissions/file_permissions.png" width="660" height="386"
alt="permissions diagram"><br><br></p>

<h2>chmod</h2>

<p>The <code class="user">chmod</code> command is used to change the
permissions of a file or directory.  To use it, we specify the desired
permission settings and the file or files that we wish to modify. There are two
ways to specify the permissions. In this lesson we will focus on one of these,
called the <i>octal notation</i> method.</p>

<p>It is easy to think of the permission settings as a series of bits (which is
how the computer thinks about them). Here's how it works:</p>

<pre>rwx rwx rwx = 111 111 111
rw- rw- rw- = 110 110 110
rwx --- --- = 111 000 000

and so on...

rwx = 111 in binary = 7
rw- = 110 in binary = 6
r-x = 101 in binary = 5
r-- = 100 in binary = 4</pre>

<p>Now, if we represent each of the three sets of permissions (owner, group,
and other) as a single digit, we have a pretty convenient way of expressing the
possible permissions settings. For example, if we wanted to set
<code>some_file</code> to have read and write permission for the owner, but
wanted to keep the file private from others, we would:</p>

```
[me@linuxbox me]$ chmod 600 some_file
```

<p>Here is a table of numbers that covers all the common settings. The ones
beginning with "7" are used with programs (since they enable execution) and the
rest are for other kinds of files.<br> <br> </p>

<table>
  <tr>
    <td><strong>Value</strong></td>
    <td><strong>Meaning</strong></td>
  </tr>
  <tr>
    <td>
    <strong>777</strong>
    </td>
    <td>
    <strong>(rwxrwxrwx)</strong> No restrictions on
    permissions. Anybody may do anything.
    Generally not a desirable setting.
    </td>
  </tr>
  <tr>
    <td>
    <strong>755</strong>
    </td>
    <td>
    <strong>(rwxr-xr-x)</strong> The file's owner may
    read, write, and execute the file. All others
    may read and execute the file. This setting
    is common for programs that are used by all
    users.
    </td>
  </tr>
  <tr>
    <td>
    <strong>700</strong>
    </td>
    <td>
    <strong>(rwx------)</strong> The file's owner may
    read, write, and execute the file. Nobody
    else has any rights. This setting is useful
    for programs that only the owner may use and
    must be kept private from others.
    </td>
  </tr>
  <tr>
    <td>
    <strong>666</strong>
    </td>
    <td>
    <strong>(rw-rw-rw-)</strong> All users may read
    and write the file.
    </td>
  </tr>
  <tr>
    <td>
    <strong>644</strong>
    </td>
    <td>
    <strong>(rw-r--r--)</strong> The owner may read
    and write a file, while all others may only
    read the file. A common setting for data
    files that everybody may read, but only the
    owner may change.
    </td>
  </tr>
  <tr>
    <td>
    <strong>600</strong>
    </td>
    <td>
    <strong>(rw-------)</strong> The owner may read
    and write a file. All others have no rights.
    A common setting for data files that the
    owner wants to keep private.
    </td>
  </tr>
</table>


### How do you modify Linux file permissions?
You can modify file and directory permissions with the chmod command, which stands for "change mode." To change file permissions in numeric mode, you enter chmod and the octal value you desire, such as 744, alongside the file name. To change file permissions in symbolic mode, you enter a user class and the permissions you want to grant them next to the file name. For example:

```
$ chmod ug+rwx example.txt
$ chmod o+r example2.txt
```
<p>This grants read, write, and execute for the user and group, and only read for others. In symbolic mode, chmod u represents permissions for the user owner, chmod g represents other users in the file's group, chmod o represents other users not in the file's group. For all users, use chmod a.</p>

<p>Maybe you want to change the user owner itself. You can do that with the chown command. Similarly, the chgrp command can be used to change the group ownership of a file.</p>

<h2>Directory Permissions</h2>
<p>The <b>chmod</b> command can also be used to control the
access permissions for directories. Again, we can use the octal notation to set
permissions, but the meaning of the r, w, and x attributes is different:</p>

<ul>
  <li><b>r</b> - Allows the contents of the directory to be listed
  if the x attribute is also set.</li>
  <li><b>w</b> - Allows files within the directory to be created,
  deleted, or renamed if the x attribute is also set.</li>
  <li><b>x</b> - Allows a directory to be entered (i.e. cd dir).</li>
</ul>
<p>Here are some useful
settings for directories:<br>
<br>
</p>
<table>
  <tr>
    <th><strong>Value</strong></th>
    <th><strong>Meaning</strong></th>
  </tr>
  <tr>
    <td>
    <strong>777</strong>
    </td>
    <td>
    <strong>(rwxrwxrwx)</strong> No restrictions on
    permissions. Anybody may list files, create
    new files in the directory and delete files
    in the directory. Generally not a good
    setting.
    </td>
  </tr>
  <tr>
    <td>
    <strong>755</strong>
    </td>
    <td>
    <strong>(rwxr-xr-x)</strong> The directory owner
    has full access. All others may list the
    directory, but cannot create files nor delete
    them. This setting is common for directories
    that you wish to share with other users.
    </td>
  </tr>
  <tr>
    <td>
    <strong>700</strong>
    </td>
    <td>
    <strong>(rwx------)</strong> The directory owner
    has full access. Nobody else has any rights.
    This setting is useful for directories that
    only the owner may use and must be kept
    private from others.
    </td>
  </tr>
</table>

<h2>Becoming the Superuser for a Short While</h2>

<p>It is often necessary to become the superuser to
perform important system administration tasks, but
as we know, we
should not stay logged in as the superuser.
In most distributions, there is a program that can give you
temporary access to the superuser's privileges.
This program is called <code class="user">su</code>
(short for substitute user) and can be used in those
cases when you need to be the superuser for a small
number of tasks. To become the superuser, simply
type the <code class="user">su</code> command. You will
be prompted for the superuser's password:</p>

```
[me@linuxbox me]$ su
Password:
[root@linuxbox me]#
```

<p>After executing the <b>su</b> command, we have a new
shell session as the superuser. To exit the superuser session, type <b>exit</b> and we will return to your previous session.</p>

<p>In most modern distributions, an alternate method is used.  Rather than
using <b>su</b>, these systems employ the <b>sudo</b> command instead.  With <b>sudo</b>,
one or more users are granted superuser privileges on an as needed basis.  To
execute a command as the superuser, the desired command is simply preceded
with the sudo command.  After the command is entered,
the user is prompted for the their own password rather than the superuser's:</p>

```
[me@linuxbox me]$ sudo some_command
Password for me:
[me@linuxbox me]$
```

<p>In fact, modern distributions don't even set the root account password thus
making it impossible to log in as the root user. A root shell is still possible
with <code class="user">sudo</code> by using the "-i" option: </p>

```
[me@linuxbox me]$sudo -i
Password for me:
root@linuxbox:~#
```

<h2>Changing File Ownership</h2>

<p>We can change the owner of a file by using the <code
class="user">chown</code> command. Here's an example: Suppose we wanted to
change the owner of <code>some_file</code> from "me" to "you". We could:</p>

```
[me@linuxbox me]$ sudo chown you some_file
```


<p>Notice that in order to change the owner of a file, we must have superuser
privileges. To do this, our example employed the <b>sudo</b>
command to execute  <b>chown</b>.</p>

<p> <b>chown</b> works the same way on directories as it does
on files.</p>

<h2>Changing Group Ownership</h2>

<p>The group ownership of a file or directory may be changed with <code
class="user">chgrp</code>. This command is used like this:</p>

```
[me@linuxbox me]$ chgrp new_group some_file
```


<p>In the example above, we changed the group ownership of
<code>some_file</code> from its previous group to "new_group". We must be the
owner of the file or directory to perform a <b>chgrp</b>.</p>
