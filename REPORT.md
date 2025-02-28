bari@ubuntu24:~$ export GITHUB_USERNAME=YaQQrQ
bari@ubuntu24:~$ export GIST_TOKEN=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
bari@ubuntu24:~$ alias edit=vim
bari@ubuntu24:~$ mkdir -p ${GITHUB_USERNAME}/workspace
bari@ubuntu24:~$ cd ${GITHUB_USERNAME}/workspace
bari@ubuntu24:~/YaQQrQ/workspace$ pwd
/home/bari/YaQQrQ/workspace
bari@ubuntu24:~/YaQQrQ/workspace$ cd ..
bari@ubuntu24:~/YaQQrQ$ pwd
/home/bari/YaQQrQ
bari@ubuntu24:~/YaQQrQ$ mkdir -p workspace/tasks/
bari@ubuntu24:~/YaQQrQ$ mkdir -p workspace/projects/
bari@ubuntu24:~/YaQQrQ$ mkdir -p workspace/reports/
bari@ubuntu24:~/YaQQrQ$ cd workspace
bari@ubuntu24:~/YaQQrQ/workspace$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2025-02-26 18:37:50--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Resolving nodejs.org (nodejs.org)... 104.20.22.46, 104.20.23.46, 2606:4700:10::6814:162e, ...
Connecting to nodejs.org (nodejs.org)|104.20.22.46|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9356460 (8.9M) [application/x-xz]
Saving to: ‘node-v6.11.5-linux-x64.tar.xz’

node-v6.11.5-linux- 100%[===================>]   8.92M  9.27MB/s    in 1.0s    

2025-02-26 18:37:51 (9.27 MB/s) - ‘node-v6.11.5-linux-x64.tar.xz’ saved [9356460/9356460]

bari@ubuntu24:~/YaQQrQ/workspace$ tar -xf node-v6.11.5-linux-x64.tar.xz
bari@ubuntu24:~/YaQQrQ/workspace$ rm -rf node-v6.11.5-linux-x64.tar.xz
bari@ubuntu24:~/YaQQrQ/workspace$ mv node-v6.11.5-linux-x64 node
bari@ubuntu24:~/YaQQrQ/workspace$ ls node/bin
node  npm
bari@ubuntu24:~/YaQQrQ/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin
bari@ubuntu24:~/YaQQrQ/workspace$ export PATH=${PATH}:`pwd`/node/bin
bari@ubuntu24:~/YaQQrQ/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin:/home/bari/YaQQrQ/workspace/node/bin
bari@ubuntu24:~/YaQQrQ/workspace$ mkdir scripts
bari@ubuntu24:~/YaQQrQ/workspace$ cat > scripts/activate<<EOF
> export PATH=\${PATH}:`pwd`/node/bin
> EOF
bari@ubuntu24:~/YaQQrQ/workspace$ source scripts/activate
bari@ubuntu24:~/YaQQrQ/workspace$ gem install gist
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /var/lib/gems/3.3.0 directory.
	/usr/lib/ruby/vendor_ruby/rubygems/installer.rb:713:in `verify_gem_home'
	/usr/lib/ruby/vendor_ruby/rubygems/installer.rb:903:in `pre_install_checks'
	/usr/lib/ruby/vendor_ruby/rubygems/installer.rb:303:in `install'
	/usr/lib/ruby/vendor_ruby/rubygems/resolver/specification.rb:105:in `install'
	/usr/lib/ruby/vendor_ruby/rubygems/request_set.rb:195:in `block in install'
	/usr/lib/ruby/vendor_ruby/rubygems/request_set.rb:183:in `each'
	/usr/lib/ruby/vendor_ruby/rubygems/request_set.rb:183:in `install'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:215:in `install_gem'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:231:in `block in install_gems'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:224:in `each'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:224:in `install_gems'
	/usr/lib/ruby/vendor_ruby/rubygems/commands/install_command.rb:170:in `execute'
	/usr/lib/ruby/vendor_ruby/rubygems/command.rb:328:in `invoke_with_build_args'
	/usr/lib/ruby/vendor_ruby/rubygems/command_manager.rb:253:in `invoke_command'
	/usr/lib/ruby/vendor_ruby/rubygems/command_manager.rb:193:in `process_args'
	/usr/lib/ruby/vendor_ruby/rubygems/command_manager.rb:151:in `run'
	/usr/lib/ruby/vendor_ruby/rubygems/gem_runner.rb:52:in `run'
	/usr/bin/gem:12:in `<main>'
bari@ubuntu24:~/YaQQrQ/workspace$ sudo apt install gist
[sudo] password for bari: 
Installing:                     
  gist

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 127
  Download size: 30.0 kB
  Space needed: 180 kB / 22.4 GB available

Get:1 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 gist all 6.0.0-3 [30.0 kB]
Fetched 30.0 kB in 1s (39.8 kB/s)
Selecting previously unselected package gist.
(Reading database ... 159174 files and directories currently installed.)
Preparing to unpack .../archives/gist_6.0.0-3_all.deb ...
Unpacking gist (6.0.0-3) ...
Setting up gist (6.0.0-3) ...
Processing triggers for man-db (2.12.1-3) ...
bari@ubuntu24:~/YaQQrQ/workspace$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
bari@ubuntu24:~/YaQQrQ/workspace$ 
bari@ubuntu24:~/YaQQrQ/workspace$ export LAB_NUMBER=01
bari@ubuntu24:~/YaQQrQ/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Cloning into 'tasks/lab01'...
remote: Enumerating objects: 74, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 74 (delta 0), reused 1 (delta 0), pack-reused 71 (from 1)
Receiving objects: 100% (74/74), 945.07 KiB | 3.06 MiB/s, done.
bari@ubuntu24:~/YaQQrQ/workspace$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
bari@ubuntu24:~/YaQQrQ/workspace$ cd reports/lab${LAB_NUMBER}
bari@ubuntu24:~/YaQQrQ/workspace/reports/lab01$ edit REPORT.md
[1]+  Stopped                 vim REPORT.md
bari@ubuntu24:~/YaQQrQ/workspace/reports/lab01$ gist REPORT.md
Command 'gist' not found, but can be installed with:
sudo apt install yorick
bari@ubuntu24:~/YaQQrQ/workspace/reports/lab01$ sudo apt install yorick
Installing:                     
  yorick

Installing dependencies:
  rlwrap  yorick-data  yorick-z

Suggested packages:
  yorick-full  yorick-mpy-openmpi  | yorick-mpy-mpich2  emacsen

Summary:
  Upgrading: 0, Installing: 4, Removing: 0, Not Upgrading: 127
  Download size: 1,457 kB
  Space needed: 4,588 kB / 22.4 GB available

Continue? [Y/n] Y
Get:1 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 rlwrap amd64 0.46.1-1build2 [107 kB]
Get:2 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 yorick-data all 2.2.04+dfsg1-13 [505 kB]
Get:3 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 yorick amd64 2.2.04+dfsg1-13 [809 kB]
Get:4 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 yorick-z amd64 1.2.0+cvs20080115-5.1build2 [36.7 kB]
Fetched 1,457 kB in 0s (4,301 kB/s)
Selecting previously unselected package rlwrap.
(Reading database ... 161427 files and directories currently installed.)
Preparing to unpack .../rlwrap_0.46.1-1build2_amd64.deb ...
Unpacking rlwrap (0.46.1-1build2) ...
Selecting previously unselected package yorick-data.
Preparing to unpack .../yorick-data_2.2.04+dfsg1-13_all.deb ...
Unpacking yorick-data (2.2.04+dfsg1-13) ...
Selecting previously unselected package yorick.
Preparing to unpack .../yorick_2.2.04+dfsg1-13_amd64.deb ...
Unpacking yorick (2.2.04+dfsg1-13) ...
Selecting previously unselected package yorick-z.
Preparing to unpack .../yorick-z_1.2.0+cvs20080115-5.1build2_amd64.deb ...
Unpacking yorick-z (1.2.0+cvs20080115-5.1build2) ...
Setting up yorick-data (2.2.04+dfsg1-13) ...
Setting up rlwrap (0.46.1-1build2) ...
update-alternatives: using /usr/bin/rlwrap to provide /usr/bin/readline-editor (readline-editor) in auto mode
/usr/share/rlwrap/filters/ftp_filter.py:57: SyntaxWarning: invalid escape sequence '\s'
  results = [re.split('\s+', l)[dir_filename_column[where]] for l in lines]
/usr/share/rlwrap/filters/ftp_filter.py:100: SyntaxWarning: invalid escape sequence '\s'
  nwords = len(re.split('\s+', line))
/usr/share/rlwrap/filters/ftp_filter.py:108: SyntaxWarning: invalid escape sequence '\s'
  command = re.search('\s*(\S+)', line).group(1)
/usr/share/rlwrap/filters/rlwrapfilter.py:4: SyntaxWarning: invalid escape sequence '\s'
  """
/usr/share/rlwrap/filters/rlwrapfilter.py:211: SyntaxWarning: invalid escape sequence '\S'
  m = re.match("(\S+) (.*?)\r?\n", sys.stdin.readline())
Setting up yorick (2.2.04+dfsg1-13) ...
Setting up yorick-z (1.2.0+cvs20080115-5.1build2) ...
Processing triggers for man-db (2.12.1-3) ...
Processing triggers for install-info (7.1-3build2) ...
bari@ubuntu24:~/YaQQrQ/workspace/reports/lab01$ gist REPORT.md
gist: (WARNING) fread failed (command) on CGM file REPORT.md
gist: (WARNING) BEGIN METAFILE element missing
gist: (WARNING) REPORT.md is not a binary CGM, cannot open
