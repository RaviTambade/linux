#  Regular Linux Commands used  
The commands listed below are some of the most useful and most frequently used Linux commands. 

1. ls - The most frequently used command in Linux to list directories
1. pwd - Print working directory command in Linux
1. cd - Linux command to navigate through directories
1. mkdir - Command used to create directories in Linux
1. mv - Move or rename files in Linux
1. cp - Similar usage as mv but for copying files in Linux
1. rm - Delete files or directories
1. touch - Create blank/empty files
1. ln - Create symbolic links (shortcuts) to other files
1. cat - Display file contents on the terminal
1. clear - Clear the terminal display
1. echo - Print any text that follows the command
1. less - Linux command to display paged outputs in the terminal
1. man - Access manual pages for all Linux commands
1. uname - Linux command to get basic information about the OS
1. whoami - Get the active username
1. tar - Command to extract and compress files in Linux
1. grep - Search for a string within an output
1. head - Return the specified number of lines from the top
1. tail - Return the specified number of lines from the bottom
1. diff - Find the difference between two files
1. cmp - Allows you to check if two files are identical
1. comm - Combines the functionality of diff and cmp
1. sort - Linux command to sort the content of a file while outputting
1. export - Export environment variables in Linux
1. zip - Zip files in Linux
1. unzip - Unzip files in Linux
1. ssh - Secure Shell command in Linux
1. service - Linux command to start and stop services
1. ps - Display active processes
1. kill and killall - Kill active processes by process ID or name
1. df - Display disk filesystem information
1. mount - Mount file systems in Linux
1. chmod - Command to change file permissions
1. chown - Command for granting ownership of files or folders
1. ifconfig - Display network interfaces and IP addresses
1. traceroute - Trace all the network hops to reach the destination
1. wget - Direct download files from the internet
1. ufw - Firewall command
1. iptables - Base firewall for all other firewall utilities to interface with
1. apt, pacman, yum, rpm - Package managers depending on the distro
1. sudo - Command to escalate privileges in Linux
1. cal - View a command-line calendar
1. alias - Create custom shortcuts for your regularly used commands
1. dd - Majorly used for creating bootable USB sticks
1. whereis - Locate the binary, source, and manual pages for a command
1. whatis - Find what a command is used for
1. top - View active processes live with their system usage
1. useradd and usermod - Add new user or change existing users data
1. passwd - Create or update passwords for existing users



<p>Now let’s dive a little deeper into each of these commands and understand them in more detail.</p>
<h2 id="the-ls-command-in-linux"><a href="#the-ls-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The ls command in Linux</a><a class="hash-anchor" href="#the-ls-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The ls command is used to list files and directories in the current working directory. This is going to be one of the most frequently used Linux commands you must know of.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/ls-command-default.png" alt="Ls Command Default"></p>
<p>As you can see in the above image, using the command by itself without any arguments will give us an output with all the files and directories in the directory. The command offers a lot of flexibility in terms of displaying the data in the output.</p>

<h2 id="the-pwd-command-in-linux"><a href="#the-pwd-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The pwd command in Linux</a><a class="hash-anchor" href="#the-pwd-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The pwd command allows you to print the current working directory on your terminal. It’s a very basic command and solves its purpose very well.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/pwd-default-output.png" alt="Pwd Default Output"></p>
<p>Now, your terminal prompt should usually have the complete directory anyway. But in case it doesn’t, this can be a quick command to see the directory that you’re in. Another application of this command is when creating scripts where this command can allow us to find the directory where the script has been saved.</p>
<h2 id="the-cd-command-in-linux"><a href="#the-cd-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The cd command in Linux</a><a class="hash-anchor" href="#the-cd-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>While working within the terminal, moving around within directories is pretty much a necessity. The cd command is one of the important Linux commands you must know and it will help you to navigate through directories. Just type <strong>cd</strong> followed by directory as shown below.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># cd &lt;directory path&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/cd-command-default.png" alt="Cd Command Default"></p>
<p>As you can see in the above command, I simply typed <strong>cd /etc/</strong> to get into the /etc directory. We used the <strong>pwd command</strong> to print the current working directory.</p>
<h2 id="the-mkdir-command-in-linux"><a href="#the-mkdir-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The mkdir command in Linux</a><a class="hash-anchor" href="#the-mkdir-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The mkdir command allows you to create directories from within the terminal. The default syntax is <strong>mkdir</strong> followed by the directory name.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># mkdir &lt;folder name&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/mkdir-default.png" alt="Mkdir Default"></p>
<p>As you can see in the above screenshot, we created the JournalDev directory with just this simple command.</p>

<h2 id="the-cp-and-mv-commands"><a href="#the-cp-and-mv-commands" onclick="navigator.clipboard.writeText(this.href);">The cp and mv commands</a><a class="hash-anchor" href="#the-cp-and-mv-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The cp and mv commands are equivalent to the copy-paste and cut-paste in Windows. But since Linux doesn’t really have a command for renaming files, we also make use of the mv command to rename files and folders.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># cp &lt;source&gt; &lt;destination&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/Cp-command-default.png" alt="Cp Command Default"></p>
<p>In the above command, we created a copy of the file named Sample. Let’s see how what happens if we use the mv command in the same manner. For this demonstration, I’ll delete the Sample-Copy file.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># mv &lt;source&gt; &lt;destination</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/mv-command-default.png" alt="Mv Command Linux commands you should know"></p>
<p>In the above case, since we were moving the file within the same directory, it acted as rename. The file name is now changed.</p>

<h2 id="the-rm-command-in-linux"><a href="#the-rm-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The rm command in Linux</a><a class="hash-anchor" href="#the-rm-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>In the previous section, we deleted the Sample-Copy file. The rm command is used to delete files and folders and is one of the important Linux commands you must know.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># rm &lt;file name&gt;</span>
root@ubuntu:~<span class="token comment"># rm -r &lt;folder/directory name&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/rm-default.png" alt="Rm Default"></p>
<p>To delete a directory, you have to add the <strong>-r</strong> argument to it. Without the -r argument, rm command won’t delete directories.</p>
<h2 id="the-touch-command-in-linux"><a href="#the-touch-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The touch command in Linux</a><a class="hash-anchor" href="#the-touch-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>To create a new file, the touch command will be used. The <strong>touch</strong> keyword followed by the file name will create a file in the current directory.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># touch &lt;file name&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/touch-command-default.png" alt="Touch Command  - Linux commands you should know"></p>
<h2 id="the-ln-command-in-linux"><a href="#the-ln-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The ln command in Linux</a><a class="hash-anchor" href="#the-ln-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>To create a link to another file, we use the ln command. This is one of the important Linux commands that you should know if you’re planning to work as a Linux administrator.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># ln -s &lt;source path&gt; &lt;link name&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/symbolic-link-default.png" alt="Symbolic Link Default"></p>
<p>The basic syntax involves using the <strong>-s</strong> parameter so we can create a symbolic link or soft link.</p>
<h2 id="the-cat-echo-and-less-commands"><a href="#the-cat-echo-and-less-commands" onclick="navigator.clipboard.writeText(this.href);">The cat, echo, and less commands</a><a class="hash-anchor" href="#the-cat-echo-and-less-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>When you want to output the contents of a file, or print anything to the terminal output, we make use of the cat or echo commands. Let’s see their basic usage. I’ve added some text to our New-File that we created earlier.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># cat &lt;file name&gt;</span>
root@ubuntu:~<span class="token comment"># echo &lt;Text to print on terminal&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/cat-and-echo-commands.png" alt="Cat And Echo Commands"></p>
<p>As you can see in the above example, the <strong>cat command</strong> when used on our “New-File”, prints the contents of the file. At the same time, when we use <strong>echo command</strong>, it simply prints whatever follows after the command.</p>
<p>The <strong>less command</strong> is used when the output printed by any command is larger than the screen space and needs scrolling. The less command allows use to break down the output and scroll through it with the use of the enter or space keys.</p>
<p>The simple way to do this is with the use of the pipe operator (<strong>|</strong>).</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># cat /boot/grub/grub.cfg  | less</span>
</code></pre>

<h2 id="the-man-command-in-linux"><a href="#the-man-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The man command in Linux</a><a class="hash-anchor" href="#the-man-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The man command is a very useful Linux command you must know. When working with Linux, the packages that we download can have a lot of functionality. Knowing it all is impossible.</p>
<p>The man pages offer a really efficient way to know the functionality of pretty much all the packages that you can download using the package managers in your Linux distro.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># man &lt;command&gt;</span>
</code></pre>
<h2 id="the-uname-and-whoami-commands"><a href="#the-uname-and-whoami-commands" onclick="navigator.clipboard.writeText(this.href);">The uname and whoami commands</a><a class="hash-anchor" href="#the-uname-and-whoami-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The uname and whoami commands allow you to know some basic information which comes really handy when you work on multiple systems. In general, if you’re working with a single computer, you won’t really need it as often as someone who is a network administrator.</p>
<p>Let’s see the output of both the commands and the way we can use these.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># uname -a</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/uname-and-whoami-commands.png" alt="Uname And Whoami Commands Linux commands you should know"></p>
<p>The parameter <strong>-a</strong> which I’ve supplied to uname, stands for “all”. This prints out the complete information. If the parameter is not added, all you will get as the output is “Linux”.</p>
<h2 id="the-tar-zip-and-unzip-commands"><a href="#the-tar-zip-and-unzip-commands" onclick="navigator.clipboard.writeText(this.href);">The tar, zip, and unzip commands</a><a class="hash-anchor" href="#the-tar-zip-and-unzip-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The tar command in Linux is used to create and extract archived files in Linux. We can extract multiple different archive files using the tar command.</p>
<p>To create an archive, we use the -c parameter and to extract an archive, we use the -x parameter. Let’s see it working.</p>
<pre class="language-bash"><code><span class="token comment">#Compress</span>
root@ubuntu:~<span class="token comment"># tar -cvf &lt;archive name&gt; &lt;files seperated by space&gt;</span>
<span class="token comment">#Extract</span>
root@ubuntu:~<span class="token comment"># tar -xvf &lt;archive name&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/tar-basic-usage.png" alt="Tar Basic Usage Linux commands you should know"></p>
<p>In the first line, we created an archive named <strong>Compress.tar</strong> with the New-File and New-File-Link. In the next command, we have extracted those files from the archive.</p>
<p>Now coming to the zip and unzip commands. Both these commands are very straight forward. You can use them without any parameters and they’ll work as intended. Let’s see an example below.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># zip &lt;archive name&gt; &lt;file names separated by space&gt;</span>
root@ubuntu:~<span class="token comment"># unzip &lt;archive name&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/zip-unzip-commands.png" alt="Zip Unzip Commands"></p>
<p>Since we already have those files in the same directory, the unzip command prompts us before overwriting those files.</p>

<h2 id="the-grep-command-in-linux"><a href="#the-grep-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The grep command in Linux</a><a class="hash-anchor" href="#the-grep-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>If you wish to search for a specific string within an output, the grep command comes into the picture. We can pipe (<strong>|</strong>) the output to the grep command and extract the required string.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># &lt;Any command with output&gt; | grep &quot;&lt;string to find&gt;&quot;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/grep-command-example.png" alt="Grep Command Example"></p>

<h2 id="the-head-and-tail-commands"><a href="#the-head-and-tail-commands" onclick="navigator.clipboard.writeText(this.href);">The head and tail commands</a><a class="hash-anchor" href="#the-head-and-tail-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>When outputting large files, the head and the tail commands come in handy. I’ve created a file named “Words” with a lot of words arranged alphabetically in it. The head command will output the first 10 lines from the file, while the tail command will output the last 10. This also includes any blank lines and not just lines with text.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># head &lt;file name&gt;</span>
root@ubuntu:~<span class="token comment"># tail &lt;file name&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/head-command.png" alt="Head Command"></p>
<p>As you can see, the head command showed 10 lines from the top of the file.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/tail-command.png" alt="Tail Command Linux commands you should know"></p>
<p>The tail command outputted the bottom 10 lines from the file.</p>

<h2 id="the-diff-comm-and-cmp-commands"><a href="#the-diff-comm-and-cmp-commands" onclick="navigator.clipboard.writeText(this.href);">The diff, comm, and cmp commands</a><a class="hash-anchor" href="#the-diff-comm-and-cmp-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>Linux offers multiple commands to compare files. The diff, comm, and cmp commands compare differences and are some of the most useful Linux commands you must know. Let’s see the default outputs for all the three commands.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># diff &lt;file 1&gt; &lt;file 2&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/diff-command.png" alt="Diff Command Linux commands you should know"></p>
<p>As you can see above, I’ve added a small piece of text saying “This line is edited” to the New-File-Edited file.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># cmp &lt;file 1&gt; &lt;file 2&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/cmp-command.png" alt="Cmp Command"></p>
<p>The cmp command only tells use the line number which is different. Not the actual text. Let’s see what the comm command does.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># comm &lt;file 1&gt; &lt;file2&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/comm-command.png" alt="Comm Command"></p>
<p>The text that’s aligned to the left is the text that’s only present in file 1. The center-aligned text is present only in file 2. And the right-aligned text is present in both the files.</p>
<p>By the looks of it, comm command makes the most sense when we’re trying to compare larger files and would like to see everything arranged together.</p>
<h2 id="the-sort-command-in-linux"><a href="#the-sort-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The sort command in Linux</a><a class="hash-anchor" href="#the-sort-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The sort command will provide a sorted output of the contents of a file. Let’s use the sort command without any parameters and see the output.</p>
<p>The basic syntax of the sort command is:</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># sort &lt;filename&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/sort-command.png" alt="Sort Command Linux commands you should know"></p>
<h2 id="the-export-command-in-linux"><a href="#the-export-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The export command in Linux</a><a class="hash-anchor" href="#the-export-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The export command is specially used when exporting environment variables in runtime. For example, if I wanted to update the bash prompt, I’ll update the PS1 environment variable. The bash prompt will be updated with immediate effect.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># export &lt;variable name&gt;=&lt;value&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/export-environment-variables.png" alt="Export Environment Variables"></p>
<p>If for some reason, your bash prompt doesn’t update, just type in <strong>bash</strong> and you should see the updated terminal prompt.</p>

<h2 id="the-ssh-command-in-linux"><a href="#the-ssh-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The ssh command in Linux</a><a class="hash-anchor" href="#the-ssh-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The ssh command allows us to connect to an external machine on the network with the use of the ssh protocol. The basic syntax of the ssh command is:</p>
<pre class="language-bash"><code>root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">ssh</span> username@hostname
</code></pre>

<h2 id="the-service-command-in-linux"><a href="#the-service-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The service command in Linux</a><a class="hash-anchor" href="#the-service-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The service command in Linux is used for starting and stopping different services within the operating system. The basic syntax of the command is as below.</p>
<pre class="language-bash"><code>root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">service</span> <span class="token function">ssh</span> status
root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">service</span> <span class="token function">ssh</span> stop
root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">service</span> <span class="token function">ssh</span> start 
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/service-command.png" alt="Service Command"></p>
<p>As you can see in the image, the ssh server is running on our system.</p>
<h2 id="the-ps-kill-and-killall-commands"><a href="#the-ps-kill-and-killall-commands" onclick="navigator.clipboard.writeText(this.href);">The ps, kill, and killall commands</a><a class="hash-anchor" href="#the-ps-kill-and-killall-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>While we’re on the topic of processes, let’s see how we can find active processes and kill them. To find the running processes, we can simply type <strong>ps</strong> in the terminal prompt and get the list of running processes.</p>
<pre class="language-bash"><code>root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">ps</span> 
root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">kill</span> <span class="token operator">&lt;</span>process ID<span class="token operator">&gt;</span>
root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">killall</span> <span class="token operator">&lt;</span>process name<span class="token operator">&gt;</span>
</code></pre>
<p>For demonstration purposes, I’m creating a shell script with an infinite loop and will run it in the background.</p>
<p>With the use of the <strong>&amp;</strong> symbol, I can pass a process into the background. As you can see, a new bash process with PID 14490 is created.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/ps-command.png" alt="Ps Command Linux commands you should know"></p>
<p>Now, to kill a process with the <strong>kill</strong> command, you can type <strong>kill</strong> followed b the PID of the process.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/kill-command.png" alt="Kill Command linux commands you should know"></p>
<p>But if you do not know the process ID and just want to kill the process with the name, you can make use of the killall command.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/killall-command.png" alt="Killall Command linux commands you should know"></p>
<p>You will notice that PID 14490 stayed active. That is because both the times, I killed the sleep process.</p>

<h2 id="the-df-and-mount-commands"><a href="#the-df-and-mount-commands" onclick="navigator.clipboard.writeText(this.href);">The df and mount commands</a><a class="hash-anchor" href="#the-df-and-mount-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>When working with Linux, the df and mount commands are very efficient utilities to mount filesystems and get details of the file system.</p>
<p>When I say mount, it means that we’ll connect the device to a folder so we can access the files from our filesystem. The default syntax to mount a filesystem is below:</p>
<pre class="language-bash"><code>root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">mount</span> /dev/cdrom /mnt
root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">df</span> <span class="token parameter variable">-h</span>
</code></pre>
<p>In the above case, <strong>/dev/cdrom</strong> is the device that needs to be mounted. Usually, a mountable device is found inside the /dev folder. <strong>/mnt</strong> is the destination folder to mount the device to. You can change it to any folder you want but I’ve used /mnt as it’s pretty much a system default folder for mounting devices.</p>
<p>To see the mounted devices and get more information about them, we make use of the df command. Just typing <strong>df</strong> will give us the data in bytes which is not readable. So we’ll use the <strong>-h</strong> parameter to make the data human-readable.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/df-command.png" alt="Df Command linux commands you should know"></p>

<h2 id="the-chmod-and-chown-commands"><a href="#the-chmod-and-chown-commands" onclick="navigator.clipboard.writeText(this.href);">The chmod and chown commands</a><a class="hash-anchor" href="#the-chmod-and-chown-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The chmod and chown commands give us the functionality to change the file permissions and file ownership are the most important Linux commands you should know.</p>
<p>The main difference between the functions of the two commands is that the chmod command allows changing file permissions, while chown allows us to change the file owners.</p>
<p>The default syntax for both the commands is <strong>chmod &lt;parameter&gt; filename</strong> and <strong>chown <a href="user:group">user:group</a> filename</strong></p>
<pre class="language-bash"><code>root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">chmod</span> +x loop.sh
root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">chmod</span> root:root loop.sh
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/chmod-command.png" alt="Chmod Command linux commands you should know"></p>
<p>In the above example, we’re adding executable permissions to the <a href="http://loop.sh">loop.sh</a> file with the <strong>chmod command</strong>. Apart from that, with the <strong>chown command</strong>, we’ve made it accessible only by root user and users within the root group.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/chown-command.png" alt="Chown Command linux commands you should know"></p>
<p>As you will notice, the <strong>root root</strong> part is now changed to <strong>www-data</strong> which is the new user who has full file ownership.</p>

<h2 id="the-ifconfig-and-traceroute-commands"><a href="#the-ifconfig-and-traceroute-commands" onclick="navigator.clipboard.writeText(this.href);">The ifconfig and traceroute commands</a><a class="hash-anchor" href="#the-ifconfig-and-traceroute-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>Moving on to the networking section in Linux, we come across the ifconfig and traceroute commands which will be frequently used if you manage a network.</p>
<p>The ifconfig command will give you the list of all the network interfaces along with the IP addresses, MAC addresses and other information about the interface.</p>
<pre class="language-bash"><code>root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">ifconfig</span>
</code></pre>
<p>There are multiple parameters that can be used but we’ll work with the basic command here.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/ifconfig-command.png" alt="Ifconfig Command linux commands you should know"></p>
<p>When working with traceroute, you can simply specify the IP address, the hostname or the domain name of the endpoint.</p>
<pre class="language-bash"><code>root@ubuntu:~ --<span class="token operator">&gt;&gt;</span> <span class="token function">traceroute</span> <span class="token operator">&lt;</span>destination address<span class="token operator">&gt;</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/traceroute-command.png" alt="Traceroute Command linux commands to know"></p>
<p>Now obviously, localhost is just one hop (which is the network interface itself). You can try this same command with any other domain name or IP address to see all the routers that your data packets pass through to reach the destination.</p>

<h2 id="the-wget-command-in-linux"><a href="#the-wget-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The wget command in Linux</a><a class="hash-anchor" href="#the-wget-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>If you want to download a file from within the terminal, the wget command is one of the handiest command-line utilities available. This will be one of the important Linux commands you should know when working with source files.</p>
<p>When you specify the link for download, it has to directly be a link to the file. If the file cannot be accessed by the wget command, it will simply download the webpage in HTML format instead of the actual file that you wanted.</p>
<p>Let’s try an example. The basic syntax of the wget command is :</p>
<pre class="language-markup"><code>root@ubuntu:~ --&gt;&gt; wget <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>link</span> <span class="token attr-name">to</span> <span class="token attr-name">file</span><span class="token punctuation">&gt;</span></span>
OR
root@ubuntu:~ --&gt;&gt; wget -c <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>link</span> <span class="token attr-name">to</span> <span class="token attr-name">file</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<p>The <strong>-c</strong> argument allows us to resume an interrupted download.</p>
<h2 id="the-ufw-and-iptables-commands"><a href="#the-ufw-and-iptables-commands" onclick="navigator.clipboard.writeText(this.href);">The ufw and iptables commands</a><a class="hash-anchor" href="#the-ufw-and-iptables-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>UFW and IPTables are firewall interfaces for the Linux Kernel’s netfilter firewall. IPTables directly passes firewall rules to netfilter while UFW configures the rules in IPTables which then sends those rules to netfilter.</p>
<p>Why do we need UFW when we have IPTables? Because IPTables is pretty difficult for a newbie. UFW makes things extremely easy. See the below example where we are trying to allow the port 80 for our webserver.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># iptables -A INPUT -p tcp -m tcp --dport 80 -j ACCEPT</span>
root@ubuntu:~<span class="token comment"># ufw allow 80</span>
</code></pre>
<p>I’m sure you now know why UFW was created! Look at how easy the syntax becomes. Both these firewalls are very comprehensive and can allow you to create any kind of configuration required for your network. Learn at least the basics of UFW or IPTables firewall as these are the Linux commands you must know.</p>
<p>Learn more <a href="/community/tutorials/opening-a-port-on-linux">opening ports on Linux(Link to article)</a></p>
<h2 id="package-managers-in-linux"><a href="#package-managers-in-linux" onclick="navigator.clipboard.writeText(this.href);">Package Managers in Linux</a><a class="hash-anchor" href="#package-managers-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>Different distros of Linux make use of different package managers. Since we’re working on a Ubuntu server, we have the <strong>apt package manager</strong>. But for someone working on a Fedora, Red Hat, Arch, or Centos machine, the package manager will be different.</p>
<ul>
<li><strong>Debian and Debian-based distros</strong> - apt install &lt;package name&gt;</li>
<li><strong>Arch and Arch-based distros</strong> - pacman -S &lt;package name&gt;</li>
<li><strong>Red Hat and Red Hat-based distros</strong> - yum install &lt;package name&gt;</li>
<li><strong>Fedora and CentOS</strong> - yum install &lt;package&gt;</li>
</ul>
<p>Getting yourself well versed with the package manager of your distribution will make things much easier for you in the long run. So even if you have a GUI based package management tool installed, try an make use of the CLI based tool before you move on to the GUI utility. Add these to your list of Linux commands you must know.</p>
<h2 id="the-sudo-command-in-linux"><a href="#the-sudo-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The sudo command in Linux</a><a class="hash-anchor" href="#the-sudo-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p><em>“With great power, comes great responsibility”</em></p>
<p>This is the quote that’s displayed when a sudo enabled user(sudoer) first makes use of the sudo command to escalate privileges. This command is equivalent to having logged in as root (based on what permissions you have as a sudoer).</p>
<pre class="language-bash"><code>non-root-user@ubuntu:~<span class="token comment"># sudo &lt;command you want to run&gt;</span>
Password: 
</code></pre>
<p>Just add the word <strong>sudo</strong> before any command that you need to run with escalated privileges and that’s it. It’s very simple to use, but can also be an added security risk if a malicious user gains access to a sudoer.</p>

<h2 id="the-cal-command-in-linux"><a href="#the-cal-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The cal command in Linux</a><a class="hash-anchor" href="#the-cal-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>Ever wanted to view the calendar in the terminal? Me neither! But there apparently are people who wanted it to happen and well here it is.</p>
<p>The <strong>cal</strong> command displays a well-presented calendar on the terminal. Just enter the word cal on your terminal prompt.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># cal</span>
root@ubuntu:~<span class="token comment"># cal May 2019</span>
</code></pre>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/cal-command-output.png" alt="Cal Command Output"></p>
<p>Even though I don’t need it, it’s a really cool addition! I’m sure there are people who are terminal fans and this is a really amazing option for them.</p>
<h2 id="the-alias-command"><a href="#the-alias-command" onclick="navigator.clipboard.writeText(this.href);">The alias command</a><a class="hash-anchor" href="#the-alias-command" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>Do you have some commands that you run very frequently while using the terminal? It could be <strong>rm -r</strong> or <strong>ls -l</strong>, or it could be something longer like <strong>tar -xvzf</strong>. This is one of the productivity-boosting Linux commands you must know.</p>
<p>If you know a command that you run very often, it’s time to create an alias. What’s an alias? In simple terms, it’s another name for a command that you’ve defined.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># alias lsl=&quot;ls -l&quot;</span>
OR
root@ubuntu:~<span class="token comment"># alias rmd=&quot;rm -r&quot;</span>
</code></pre>
<p>Now every time you enter <strong>lsl</strong> or <strong>rmd</strong> in the terminal, you’ll receive the output that you’d have received if you had used the full commands.</p>
<p>The examples here are for really small commands that you can still type by hand every time. But in some situations where a command has too many arguments that you need to type, it’s best to create a shorthand version of the same.</p>

<h2 id="the-dd-command-in-linux"><a href="#the-dd-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The dd command in Linux</a><a class="hash-anchor" href="#the-dd-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>This command was created to convert and copy files from multiple file system formats. In the current day, the command is simply used to create bootable USB for Linux but there still are some things important you can do with the command.</p>
<p>For example, if I wanted to back up the entire hard drive as is to another drive, I’ll make use of the dd command.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># dd if = /dev/sdb of = /dev/sda</span>
</code></pre>
<p>The <strong>if</strong> and <strong>of</strong> arguments stand for <strong>input file</strong> and <strong>output file</strong>.</p>
<h2 id="the-whereis-and-whatis-commands"><a href="#the-whereis-and-whatis-commands" onclick="navigator.clipboard.writeText(this.href);">The whereis and whatis commands</a><a class="hash-anchor" href="#the-whereis-and-whatis-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The names of the commands make it very clear as to their functionality. But let’s demonstrate their functionality to make things more clear.</p>
<p>The <strong>whereis</strong> command will output the exact location of any command that you type in after the <strong>whereis</strong> command.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># whereis sudo</span>
sudo: /usr/bin/sudo /usr/lib/sudo /usr/share/man/man8/sudo.8.gz
</code></pre>
<p>The <strong>whatis</strong> command gives us an explanation of what a command actually is. Similar to the whereis command, you’ll receive the information for any command that you type after the <strong>whatis</strong> command.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># whatis sudo</span>
<span class="token function">sudo</span> <span class="token punctuation">(</span><span class="token number">8</span><span class="token punctuation">)</span> - execute a <span class="token builtin class-name">command</span> as another user
</code></pre>
<h2 id="the-top-command-in-linux"><a href="#the-top-command-in-linux" onclick="navigator.clipboard.writeText(this.href);">The top command in Linux</a><a class="hash-anchor" href="#the-top-command-in-linux" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>A few sections earlier, we talked about the ps command. You observed that the ps command will output the active processes and end itself.</p>
<p>The top command is like a CLI version of the task manager in Windows. You get a live view of the processes and all the information accompanying those processes like memory usage, CPU usage, etc.</p>
<p>To get the top command, all you need to do is type the word <strong>top</strong> in your terminal.</p>
<p><img src="https://journaldev.nyc3.digitaloceanspaces.com/2020/01/top-command-output.png" alt="Top Command Output Linux commands you shoud know"></p>
<h2 id="the-useradd-and-usermod-commands"><a href="#the-useradd-and-usermod-commands" onclick="navigator.clipboard.writeText(this.href);">The useradd and usermod commands</a><a class="hash-anchor" href="#the-useradd-and-usermod-commands" aria-hidden="true" onclick="navigator.clipboard.writeText(this.href);"></a></h2>
<p>The <strong>useradd</strong> or <strong>adduser</strong> commands are the exact same commands where adduser is just a symbolic link to the useradd command. This command allows us to create a new user in Linux.</p>
<pre class="language-bash"><code>root@ubuntu:~<span class="token comment"># useradd JournalDev -d /home/JD</span>
</code></pre>
<p>The above command will create a new user named JournalDev with the home directory as <strong>/home/JD</strong>.</p>
<p>The <strong>usermod</strong> command, on the other hand, is used to modify existing users. You can modify any value of the user including the groups, the permissions, etc.</p>
<p>For example, if you want to add more groups to the user, you can type in:</p>
<pre class="language-markup"><code>root@ubuntu:~# usermod JournalDev -a -G sudo, audio, mysql
</code></pre>
