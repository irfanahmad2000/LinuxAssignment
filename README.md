(1)Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.
-------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ pwd
/home
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ cd 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd /home/
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ mkdir ~/MyFiles
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ cd ~/MyFiles
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ ls
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ pwd
/home/irfan/MyFiles
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ 

(2)Copy a file named "document.txt" from your home directory to the "MyFiles" directory. Move the file to a subdirectory named "Documents" within "MyFiles."
-------------------------------------------------------------------------------------------------------------------------------------------------------

irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ pwd
/home/irfan/MyFiles
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ cd 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd /home/
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ cp ~/document.txt ~/MyFiles/
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ mv ~/MyFiles/document.txt ~/MyFiles/Documents/
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ pwd
/home
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ ls
irfan
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ ls
irfan
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ cd 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd /home/
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ cd /irfan/
bash: cd: /irfan/: No such file or directory
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ cd irfan/
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd MyFiles/
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ cd Documents/
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ pwd
/home/irfan/MyFiles/Documents
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ls
document.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ 



(3)Create an empty file named "notes.txt" in the "MyFiles" directory. Afterward, delete the file.
----------------------------------------------------------------------------------------------

irfan@irfan-HP-Laptop-15s-fq4xxx:~$ pwd
/home/irfan
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd /home/
irfan@irfan-HP-Laptop-15s-fq4xxx:/home$ cd irfan/
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd MyFiles/
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ cd 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ touch notes.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ rm notes.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ pwd
/home/irfan
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ ^C
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 


(4)Create a hard link named "hardlink.txt" for the file "document.txt" within the "Documents" subdirectory. Also, create a symbolic link named "symlink.txt" in the same location.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ cd ~/MyFiles/Documents/
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ln document.txt hardlink.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ln -s document.txt symlink.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ pwd
/home/irfan/MyFiles/Documents
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ls
document.txt  hardlink.txt  symlink.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ 


(5)In the "MyFiles" directory, use a single command to list all files that start with the letter "a" and have a ".txt" extension.
-----------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ cd ~/MyFiles/Documents/
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ln document.txt hardlink.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ln -s document.txt symlink.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ pwd
/home/irfan/MyFiles/Documents
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ls
document.txt  hardlink.txt  symlink.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ls a*.txt
ls: cannot access 'a*.txt': No such file or directory
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ cd 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ touch abc.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ touch aab.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ touch all.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ ls a*.txt
aab.txt  abc.txt  all.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 

(6)Rename all files in the "Documents" subdirectory of "MyFiles" with a ".bak" extension. Ensure the original file names are preserved.
-----------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd ~/MyFiles/Documents/
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ls
document.txt  hardlink.txt  symlink.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ cd ..
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ ls
Documents
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ pwd
/home/irfan/MyFiles
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ ls
Documents
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ cd Documents/
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ls
document.txt  hardlink.txt  symlink.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ touch a.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ touch aa.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ for file in *; do
>   mv "$file" "${file}.bak"
> done
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ls
aa.txt.bak  a.txt.bak  document.txt.bak  hardlink.txt.bak  symlink.txt.bak
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ^C
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ 


(7)Use a wildcard character to copy all files from the "Documents" subdirectory of "MyFiles" to another directory named "Backup."
----------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ cp -r * ../Backup/
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ ls
aa.txt.bak  a.txt.bak  document.txt.bak  hardlink.txt.bak  symlink.txt.bak
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ cd Backup
bash: cd: Backup: No such file or directory
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Documents$ cd ..
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ pwd
/home/irfan/MyFiles
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ cd Backup/
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Backup$ ls
aa.txt.bak  a.txt.bak  document.txt.bak  hardlink.txt.bak  symlink.txt.bak
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Backup$ 


(8)Execute the ls command to list files in the current directory. Save the output to a file named "file_list.txt." Then, use a pipe to filter the output through grep to display only files with a ".txt" extension.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles/Backup$ cd ..
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ ls > file_list.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ cat file_list.txt | grep '\.txt$'
file_list.txt







(9)Create a new text file named "my_notes.txt" using the touch command. Open the file in the Vim editor, add some text, and save the changes.
------------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ touch my_notes.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ ls

irfan@irfan-HP-Laptop-15s-fq4xxx:~$ vim my_notes.txt

Command 'vim' not found, but can be installed with:

sudo apt install vim         # version 2:8.1.2269-1ubuntu5.20, or
sudo apt install vim-tiny    # version 2:8.1.2269-1ubuntu5.20
sudo apt install vim-athena  # version 2:8.1.2269-1ubuntu5.20
sudo apt install vim-gtk3    # version 2:8.1.2269-1ubuntu5.20
sudo apt install vim-nox     # version 2:8.1.2269-1ubuntu5.20
sudo apt install neovim      # version 0.4.3-3

irfan@irfan-HP-Laptop-15s-fq4xxx:~$ ^C
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ vim my_notes.txt

Command 'vim' not found, but can be installed with:

sudo apt install vim         # version 2:8.1.2269-1ubuntu5.20, or
sudo apt install vim-tiny    # version 2:8.1.2269-1ubuntu5.20
sudo apt install vim-athena  # version 2:8.1.2269-1ubuntu5.20
sudo apt install vim-gtk3    # version 2:8.1.2269-1ubuntu5.20
sudo apt install vim-nox     # version 2:8.1.2269-1ubuntu5.20
sudo apt install neovim      # version 0.4.3-3

irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo apt install vim 
[sudo] password for irfan: 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  vim-runtime
Suggested packages:
  ctags vim-doc vim-scripts
The following NEW packages will be installed:
  vim vim-runtime
0 upgraded, 2 newly installed, 0 to remove and 25 not upgraded.
Need to get 7,121 kB of archives.
After this operation, 34.6 MB of additional disk space will be used.
Do you want to continue? [Y/n] Y
Get:1 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 vim-runtime all 2:8.1.2269-1ubuntu5.21 [5,878 kB]
Get:2 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 vim amd64 2:8.1.2269-1ubuntu5.21 [1,243 kB]
Fetched 7,121 kB in 3s (2,293 kB/s)
Selecting previously unselected package vim-runtime.
(Reading database ... 209082 files and directories currently installed.)
Preparing to unpack .../vim-runtime_2%3a8.1.2269-1ubuntu5.21_all.deb ...
Adding 'diversion of /usr/share/vim/vim81/doc/help.txt to /usr/share/vim/vim81/d
oc/help.txt.vim-tiny by vim-runtime'
Adding 'diversion of /usr/share/vim/vim81/doc/tags to /usr/share/vim/vim81/doc/t
ags.vim-tiny by vim-runtime'
Unpacking vim-runtime (2:8.1.2269-1ubuntu5.21) ...
Selecting previously unselected package vim.
Preparing to unpack .../vim_2%3a8.1.2269-1ubuntu5.21_amd64.deb ...
Unpacking vim (2:8.1.2269-1ubuntu5.21) ...
Setting up vim-runtime (2:8.1.2269-1ubuntu5.21) ...
Setting up vim (2:8.1.2269-1ubuntu5.21) ...
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vim (vim) in a
uto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vimdiff (vimdi
ff) in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/rvim (rvim) in
 auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/rview (rview) 
in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vi (vi) in aut
o mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/view (view) in
 auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/ex (ex) in aut
o mode
Processing triggers for man-db (2.9.1-1) ...
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ ls
 my_notes.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ vim my_notes.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 

(10)Run the date command and store the output in a variable named "current_date." Display the value of the variable and append it to the "my_notes.txt" file.
--------------------------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ pwd
/home/irfan
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cd /home/irfan/MyFiles
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ current_date=$(date)
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ echo "Current Date: $current_date"
Current Date: Wednesday 31 January 2024 11:35:54 PM IST
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ echo "Current Date: $current_date" >> my_notes.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ 

(11)Edit the Bash startup script (e.g., .bashrc) to set an environment variable named "CUSTOM_PATH" to a specific directory path. Ensure the variable is available in new shell sessions.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ echo 'export CUSTOM_PATH=/home/irfan/my_specific_directory' >> ~/.bashrc
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ source ~/.bashrc
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ echo $CUSTOM_PATH
/home/irfan/my_specific_directory
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ 

(12)Use the echo command to add a new line of text to the "my_notes.txt" file without overwriting existing content. Verify that the new text is appended.
----------------------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ pwd
/home/irfan/MyFiles
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ ls
Backup  Documents  file_list.txt  my_notes.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ echo 'This is a new line of text.' >> ~/MyFiles/my_notes.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ cat ~/MyFiles/my_notes.txt
Current Date: Wednesday 31 January 2024 11:35:54 PM IST
This is a new line of text.
irfan@irfan-HP-Laptop-15s-fq4xxx:~/MyFiles$ 

(13)List all files in the "/etc" directory, filter the output to include only those containing the word "conf," and save the result to a file named "conf_files.txt."
----------------------------------------------------------------------------------------------------------------------------------------------------------------

irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo find /etc -type f -name "*conf*" > conf_files.txt
[sudo] password for irfan: 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ find /etc -type f -name "*conf*" > conf_files.txt
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/cups/ssl’: Permission denied
find: ‘/etc/polkit-1/localauthority’: Permission denied
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo find /etc -type f -name "*conf*" > conf_files.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ cat conf_files.txt
/etc/libaudit.conf
/etc/debconf.conf
/etc/manpath.config
/etc/python3/debian_config
/etc/ubuntu-advantage/uaclient.conf
/etc/dpkg/dpkg.cfg.d/pkg-config-hook-config
/etc/initramfs-tools/initramfs.conf
/etc/initramfs-tools/update-initramfs.conf
/etc/usb_modeswitch.conf
/etc/host.conf
/etc/depmod.d/ubuntu.conf
/etc/udev/udev.conf
/etc/X11/Xsession.d/70im-config_launch
/etc/X11/Xwrapper.config
/etc/sysctl.d/10-ipv6-privacy.conf
/etc/sysctl.d/10-zeropage.conf
/etc/sysctl.d/10-kernel-hardening.conf
/etc/sysctl.d/10-console-messages.conf
/etc/sysctl.d/30-postgresql-shm.conf
/etc/sysctl.d/10-network-security.conf
/etc/sysctl.d/10-magic-sysrq.conf
/etc/sysctl.d/10-link-restrictions.conf
/etc/sysctl.d/10-ptrace.conf
/etc/speech-dispatcher/clients/emacs.conf
/etc/speech-dispatcher/modules/pico-generic.conf
/etc/speech-dispatcher/modules/kali.conf
/etc/speech-dispatcher/modules/dtk-generic.conf
/etc/speech-dispatcher/modules/swift-generic.conf
/etc/speech-dispatcher/modules/llia_phon-generic.conf
/etc/speech-dispatcher/modules/cicero.conf
/etc/speech-dispatcher/modules/espeak-ng.conf
/etc/speech-dispatcher/modules/espeak.conf
/etc/speech-dispatcher/modules/ibmtts.conf
/etc/speech-dispatcher/modules/ivona.conf
/etc/speech-dispatcher/modules/espeak-ng-mbrola-generic.conf
/etc/speech-dispatcher/modules/espeak-generic.conf
/etc/speech-dispatcher/modules/mary-generic.conf
/etc/speech-dispatcher/modules/baratinoo.conf
/etc/speech-dispatcher/modules/epos-generic.conf
/etc/speech-dispatcher/modules/espeak-mbrola-generic.conf
/etc/speech-dispatcher/modules/flite.conf
/etc/speech-dispatcher/modules/festival.conf
/etc/speech-dispatcher/speechd.conf
/etc/gdm3/greeter.dconf-defaults
/etc/gdm3/config-error-dialog.sh
/etc/gdm3/custom.conf
/etc/rygel.conf
/etc/mke2fs.conf
/etc/logrotate.conf
/etc/pcmcia/config.opts
/etc/environment.d/90atk-adaptor.conf
/etc/environment.d/90qt-a11y.conf
/etc/fwupd/remotes.d/vendor-directory.conf
/etc/fwupd/remotes.d/dell-esrt.conf
/etc/fwupd/remotes.d/vendor.conf
/etc/fwupd/remotes.d/lvfs.conf
/etc/fwupd/remotes.d/lvfs-testing.conf
/etc/fwupd/uefi_capsule.conf
/etc/fwupd/redfish.conf
/etc/fwupd/daemon.conf
/etc/fwupd/thunderbolt.conf
/etc/selinux/semanage.conf
/etc/ufw/ufw.conf
/etc/ufw/sysctl.conf
/etc/kernel-img.conf
/etc/modprobe.d/iwlwifi.conf
/etc/modprobe.d/blacklist-framebuffer.conf
/etc/modprobe.d/blacklist-rare-network.conf
/etc/modprobe.d/blacklist-ath_pci.conf
/etc/modprobe.d/blacklist.conf
/etc/modprobe.d/blacklist-modem.conf
/etc/modprobe.d/alsa-base.conf
/etc/modprobe.d/amd64-microcode-blacklist.conf
/etc/modprobe.d/blacklist-firewire.conf
/etc/modprobe.d/intel-microcode-blacklist.conf
/etc/apparmor/parser.conf
/etc/xattr.conf
/etc/avahi/avahi-daemon.conf
/etc/gai.conf
/etc/UPower/UPower.conf
/etc/adduser.conf
/etc/postgresql-common/createcluster.conf
/etc/pnm2ppa.conf
/etc/pam.conf
/etc/ca-certificates.conf
/etc/fonts/conf.d/65-khmer.conf
/etc/fonts/conf.avail/67-smc-keraleeyam.conf
/etc/fonts/conf.avail/11-lcdfilter-default.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-sans.conf
/etc/fonts/conf.avail/30-cjk-aliases.conf
/etc/fonts/conf.avail/20-unhint-small-vera.conf
/etc/fonts/conf.avail/69-language-selector-zh-cn.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-serif.conf
/etc/fonts/conf.avail/67-smc-suruma.conf
/etc/fonts/conf.avail/67-smc-anjalioldlipi.conf
/etc/fonts/conf.avail/65-0-fonts-guru-extra.conf
/etc/fonts/conf.avail/10-sub-pixel-vrgb.conf
/etc/fonts/conf.avail/67-smc-karumbi.conf
/etc/fonts/conf.avail/58-dejavu-lgc-sans.conf
/etc/fonts/conf.avail/66-lohit-gujarati.conf
/etc/fonts/conf.avail/66-lohit-gurmukhi.conf
/etc/fonts/conf.avail/66-lohit-tamil.conf
/etc/fonts/conf.avail/58-dejavu-lgc-serif.conf
/etc/fonts/conf.avail/10-scale-bitmap-fonts.conf
/etc/fonts/conf.avail/50-user.conf
/etc/fonts/conf.avail/45-latin.conf
/etc/fonts/conf.avail/65-fonts-persian.conf
/etc/fonts/conf.avail/10-sub-pixel-bgr.conf
/etc/fonts/conf.avail/69-language-selector-ja.conf
/etc/fonts/conf.avail/59-lohit-devanagari.conf
/etc/fonts/conf.avail/69-language-selector-zh-mo.conf
/etc/fonts/conf.avail/70-force-bitmaps.conf
/etc/fonts/conf.avail/65-0-fonts-beng-extra.conf
/etc/fonts/conf.avail/57-dejavu-sans-mono.conf
/etc/fonts/conf.avail/10-sub-pixel-rgb.conf
/etc/fonts/conf.avail/67-smc-uroob.conf
/etc/fonts/conf.avail/66-lohit-assamese.conf
/etc/fonts/conf.avail/66-lohit-odia.conf
/etc/fonts/conf.avail/69-language-selector-zh-sg.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-lgc-serif.conf
/etc/fonts/conf.avail/51-local.conf
/etc/fonts/conf.avail/60-generic.conf
/etc/fonts/conf.avail/65-0-fonts-deva-extra.conf
/etc/fonts/conf.avail/10-autohint.conf
/etc/fonts/conf.avail/11-lcdfilter-legacy.conf
/etc/fonts/conf.avail/10-sub-pixel-vbgr.conf
/etc/fonts/conf.avail/45-generic.conf
/etc/fonts/conf.avail/10-hinting-full.conf
/etc/fonts/conf.avail/64-language-selector-prefer.conf
/etc/fonts/conf.avail/30-metric-aliases.conf
/etc/fonts/conf.avail/80-delicious.conf
/etc/fonts/conf.avail/69-language-selector-zh-hk.conf
/etc/fonts/conf.avail/10-antialias.conf
/etc/fonts/conf.avail/69-unifont.conf
/etc/fonts/conf.avail/65-0-smc-meera.conf
/etc/fonts/conf.avail/10-no-sub-pixel.conf
/etc/fonts/conf.avail/65-khmer.conf
/etc/fonts/conf.avail/10-hinting-medium.conf
/etc/fonts/conf.avail/66-lohit-telugu.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-lgc-sans.conf
/etc/fonts/conf.avail/10-hinting-none.conf
/etc/fonts/conf.avail/65-0-fonts-orya-extra.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-sans-mono.conf
/etc/fonts/conf.avail/65-0-fonts-telu-extra.conf
/etc/fonts/conf.avail/69-language-selector-zh-tw.conf
/etc/fonts/conf.avail/70-yes-bitmaps.conf
/etc/fonts/conf.avail/58-dejavu-lgc-sans-mono.conf
/etc/fonts/conf.avail/67-fonts-smc-manjari.conf
/etc/fonts/conf.avail/25-unhint-nonlatin.conf
/etc/fonts/conf.avail/57-dejavu-serif.conf
/etc/fonts/conf.avail/70-no-bitmaps.conf
/etc/fonts/conf.avail/67-lohit-malayalam.conf
/etc/fonts/conf.avail/53-monospace-lcd-filter.conf
/etc/fonts/conf.avail/65-droid-sans-fallback.conf
/etc/fonts/conf.avail/90-synthetic.conf
/etc/fonts/conf.avail/66-lohit-kannada.conf
/etc/fonts/conf.avail/99-language-selector-zh.conf
/etc/fonts/conf.avail/40-nonlatin.conf
/etc/fonts/conf.avail/66-lohit-bengali.conf
/etc/fonts/conf.avail/66-lohit-tamil-classical.conf
/etc/fonts/conf.avail/65-0-fonts-pagul.conf
/etc/fonts/conf.avail/56-language-selector-ar.conf
/etc/fonts/conf.avail/30-droid-noto-mono.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-lgc-sans-mono.conf
/etc/fonts/conf.avail/65-0-fonts-gujr-extra.conf
/etc/fonts/conf.avail/65-0-smc-rachana.conf
/etc/fonts/conf.avail/67-smc-raghumalayalamsans.conf
/etc/fonts/conf.avail/65-0-fonts-gubbi.conf
/etc/fonts/conf.avail/11-lcdfilter-light.conf
/etc/fonts/conf.avail/10-unhinted.conf
/etc/fonts/conf.avail/57-dejavu-sans.conf
/etc/fonts/conf.avail/67-smc-dyuthi.conf
/etc/fonts/conf.avail/60-latin.conf
/etc/fonts/conf.avail/67-smc-chilanka.conf
/etc/fonts/conf.avail/49-sansserif.conf
/etc/fonts/conf.avail/10-hinting-slight.conf
/etc/fonts/conf.avail/65-nonlatin.conf
/etc/fonts/conf.avail/66-lohit-devanagari.conf
/etc/fonts/fonts.conf
/etc/openvpn/update-resolv-conf
/etc/profile.d/im-config_wayland.sh
/etc/cups/subscriptions.conf
/etc/cups/cupsd.conf
/etc/cups/cups-files.conf
/etc/cups/subscriptions.conf.O
/etc/cups/cups-browsed.conf
/etc/cups/snmp.conf
/etc/apport/crashdb.conf
/etc/modules-load.d/cups-filters.conf
/etc/sysstat/sysstat.ioconf
/etc/deluser.conf
/etc/brltty.conf
/etc/NetworkManager/NetworkManager.conf
/etc/NetworkManager/conf.d/default-wifi-powersave-on.conf
/etc/polkit-1/localauthority.conf.d/51-ubuntu-admin.conf
/etc/polkit-1/localauthority.conf.d/50-localauthority.conf
/etc/xdg/user-dirs.conf
/etc/ghostscript/cidfmap.d/90gs-cjk-resource-cns1.conf
/etc/ghostscript/cidfmap.d/90gs-cjk-resource-japan2.conf
/etc/ghostscript/cidfmap.d/90gs-cjk-resource-japan1.conf
/etc/ghostscript/cidfmap.d/90gs-cjk-resource-gb1.conf
/etc/ghostscript/cidfmap.d/90gs-cjk-resource-korea1.conf
/etc/gtk-3.0/im-multipress.conf
/etc/alsa/conf.d/99-pulseaudio-default.conf.example
/etc/libao.conf
/etc/e2scrub.conf
/etc/udisks2/udisks2.conf
/etc/kerneloops.conf
/etc/fuse.conf
/etc/gtk-2.0/im-multipress.conf
/etc/apparmor.d/usr.lib.snapd.snap-confine.real
/etc/apparmor.d/local/usr.lib.snapd.snap-confine.real
/etc/apparmor.d/abstractions/dconf
/etc/hdparm.conf
/etc/hp/hplip.conf
/etc/mtools.conf
/etc/postgresql/16/main/pg_hba.conf
/etc/postgresql/16/main/start.conf
/etc/postgresql/16/main/postgresql.conf
/etc/postgresql/16/main/pg_ident.conf
/etc/postgresql/16/main/pg_ctl.conf
/etc/postgresql/12/main/pg_hba.conf
/etc/postgresql/12/main/start.conf
/etc/postgresql/12/main/postgresql.conf
/etc/postgresql/12/main/pg_ident.conf
/etc/postgresql/12/main/pg_ctl.conf
/etc/systemd/system.conf
/etc/systemd/journald.conf
/etc/systemd/networkd.conf
/etc/systemd/pstore.conf
/etc/systemd/logind.conf
/etc/systemd/user.conf
/etc/systemd/resolved.conf
/etc/systemd/timesyncd.conf
/etc/systemd/sleep.conf
/etc/init/whoopsie.conf
/etc/ld.so.conf.d/libc.conf
/etc/ld.so.conf.d/x86_64-linux-gnu.conf
/etc/rsyslog.d/20-ufw.conf
/etc/rsyslog.d/50-default.conf
/etc/pulse/client.conf
/etc/pulse/daemon.conf
/etc/libreoffice/psprint.conf
/etc/security/pam_env.conf
/etc/security/namespace.conf
/etc/security/access.conf
/etc/security/limits.conf
/etc/security/capability.conf
/etc/security/faillock.conf
/etc/security/time.conf
/etc/security/group.conf
/etc/security/sepermit.conf
/etc/security/pwquality.conf
/etc/sane.d/dc240.conf
/etc/sane.d/u12.conf
/etc/sane.d/stv680.conf
/etc/sane.d/microtek2.conf
/etc/sane.d/xerox_mfp.conf
/etc/sane.d/hpsj5s.conf
/etc/sane.d/teco1.conf
/etc/sane.d/epson.conf
/etc/sane.d/net.conf
/etc/sane.d/kodak.conf
/etc/sane.d/umax_pp.conf
/etc/sane.d/lexmark.conf
/etc/sane.d/coolscan.conf
/etc/sane.d/escl.conf
/etc/sane.d/hp.conf
/etc/sane.d/plustek.conf
/etc/sane.d/ricoh.conf
/etc/sane.d/artec.conf
/etc/sane.d/pixma.conf
/etc/sane.d/sp15c.conf
/etc/sane.d/canon_pp.conf
/etc/sane.d/bh.conf
/etc/sane.d/avision.conf
/etc/sane.d/rts8891.conf
/etc/sane.d/kvs1025.conf
/etc/sane.d/hp4200.conf
/etc/sane.d/p5.conf
/etc/sane.d/abaton.conf
/etc/sane.d/tamarack.conf
/etc/sane.d/test.conf
/etc/sane.d/epson2.conf
/etc/sane.d/cardscan.conf
/etc/sane.d/pieusb.conf
/etc/sane.d/microtek.conf
/etc/sane.d/epsonds.conf
/etc/sane.d/dc210.conf
/etc/sane.d/apple.conf
/etc/sane.d/hs2p.conf
/etc/sane.d/saned.conf
/etc/sane.d/dc25.conf
/etc/sane.d/sharp.conf
/etc/sane.d/canon_dr.conf
/etc/sane.d/fujitsu.conf
/etc/sane.d/agfafocus.conf
/etc/sane.d/teco3.conf
/etc/sane.d/genesys.conf
/etc/sane.d/teco2.conf
/etc/sane.d/sceptre.conf
/etc/sane.d/epjitsu.conf
/etc/sane.d/matsushita.conf
/etc/sane.d/coolscan2.conf
/etc/sane.d/sm3840.conf
/etc/sane.d/canon.conf
/etc/sane.d/ibm.conf
/etc/sane.d/mustek_usb.conf
/etc/sane.d/dll.conf
/etc/sane.d/snapscan.conf
/etc/sane.d/mustek.conf
/etc/sane.d/leo.conf
/etc/sane.d/umax1220u.conf
/etc/sane.d/nec.conf
/etc/sane.d/mustek_pp.conf
/etc/sane.d/dmc.conf
/etc/sane.d/umax.conf
/etc/sane.d/qcam.conf
/etc/sane.d/dell1600n_net.conf
/etc/sane.d/kodakaio.conf
/etc/sane.d/artec_eplus48u.conf
/etc/sane.d/gt68xx.conf
/etc/sane.d/hp5400.conf
/etc/sane.d/s9036.conf
/etc/sane.d/hp3900.conf
/etc/sane.d/canon630u.conf
/etc/sane.d/gphoto2.conf
/etc/sane.d/coolscan3.conf
/etc/sane.d/ma1509.conf
/etc/sane.d/pie.conf
/etc/sane.d/st400.conf
/etc/sane.d/magicolor.conf
/etc/sane.d/plustek_pp.conf
/etc/cracklib/cracklib.conf
/etc/appstream.conf
/etc/bluetooth/network.conf
/etc/bluetooth/input.conf
/etc/bluetooth/main.conf
/etc/sysctl.conf
/etc/fprintd.conf
/etc/ldap/ldap.conf
/etc/apache2/ports.conf
/etc/apache2/apache2.conf
/etc/apache2/conf-available/pgadmin4.conf
/etc/apache2/conf-available/charset.conf
/etc/apache2/conf-available/serve-cgi-bin.conf
/etc/apache2/conf-available/security.conf
/etc/apache2/conf-available/localized-error-pages.conf
/etc/apache2/conf-available/other-vhosts-access-log.conf
/etc/apache2/mods-available/wsgi.conf
/etc/apache2/mods-available/mpm_worker.conf
/etc/apache2/mods-available/dav_fs.conf
/etc/apache2/mods-available/reqtimeout.conf
/etc/apache2/mods-available/mpm_event.conf
/etc/apache2/mods-available/ldap.conf
/etc/apache2/mods-available/negotiation.conf
/etc/apache2/mods-available/proxy_ftp.conf
/etc/apache2/mods-available/autoindex.conf
/etc/apache2/mods-available/cache_disk.conf
/etc/apache2/mods-available/mime.conf
/etc/apache2/mods-available/proxy_balancer.conf
/etc/apache2/mods-available/alias.conf
/etc/apache2/mods-available/ssl.conf
/etc/apache2/mods-available/http2.conf
/etc/apache2/mods-available/status.conf
/etc/apache2/mods-available/deflate.conf
/etc/apache2/mods-available/setenvif.conf
/etc/apache2/mods-available/proxy.conf
/etc/apache2/mods-available/cgid.conf
/etc/apache2/mods-available/dir.conf
/etc/apache2/mods-available/mpm_prefork.conf
/etc/apache2/mods-available/actions.conf
/etc/apache2/mods-available/proxy_html.conf
/etc/apache2/mods-available/mime_magic.conf
/etc/apache2/mods-available/info.conf
/etc/apache2/mods-available/userdir.conf
/etc/apache2/sites-available/default-ssl.conf
/etc/apache2/sites-available/000-default.conf
/etc/sensors3.conf
/etc/ltrace.conf
/etc/nsswitch.conf
/etc/PackageKit/PackageKit.conf
/etc/PackageKit/Vendor.conf
/etc/dhcp/dhclient.conf
/etc/dbus-1/system.d/com.hp.hplip.conf
/etc/dbus-1/system.d/com.ubuntu.SoftwareProperties.conf
/etc/dbus-1/system.d/com.redhat.NewPrinterNotification.conf
/etc/dbus-1/system.d/org.freedesktop.GeoClue2.Agent.conf
/etc/dbus-1/system.d/gdm.conf
/etc/dbus-1/system.d/net.hadess.SwitcherooControl.conf
/etc/dbus-1/system.d/wpa_supplicant.conf
/etc/dbus-1/system.d/org.freedesktop.ModemManager1.conf
/etc/dbus-1/system.d/org.opensuse.CupsPkHelper.Mechanism.conf
/etc/dbus-1/system.d/com.ubuntu.LanguageSelector.conf
/etc/dbus-1/system.d/org.freedesktop.Accounts.conf
/etc/dbus-1/system.d/org.freedesktop.thermald.conf
/etc/dbus-1/system.d/bluetooth.conf
/etc/dbus-1/system.d/com.ubuntu.WhoopsiePreferences.conf
/etc/dbus-1/system.d/org.debian.apt.conf
/etc/dbus-1/system.d/org.freedesktop.GeoClue2.conf
/etc/dbus-1/system.d/org.freedesktop.PackageKit.conf
/etc/dbus-1/system.d/dnsmasq.conf
/etc/dbus-1/system.d/kerneloops.conf
/etc/dbus-1/system.d/net.hadess.SensorProxy.conf
/etc/dbus-1/system.d/avahi-dbus.conf
/etc/dbus-1/system.d/pulseaudio-system.conf
/etc/dbus-1/system.d/com.redhat.PrinterDriversInstaller.conf
/etc/dbus-1/system.d/com.ubuntu.USBCreator.conf
/etc/apt/apt.conf.d/70debconf
/etc/apt/apt.conf.d/20snapd.conf
/etc/apt/apt.conf.d/20apt-esm-hook.conf
/etc/apg.conf
/etc/geoclue/geoclue.conf
/etc/ca-certificates.conf.dpkg-old
/etc/ld.so.conf
/etc/default/im-config
/etc/popularity-contest.conf
/etc/ucf.conf
/etc/ssh/ssh_config
/etc/rsyslog.conf
/etc/snmp/snmp.conf



(14)Open the "my_notes.txt" file in Vim. Use Vim's search and replace functionality to replace all occurrences of the word "important" with "critical." Save the changes.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------

E325: ATTENTION
Found a swap file by the name ".my_notes.txt.swp"
          owned by: irfan   dated: Sat Feb 03 20:43:05 2024
         file name: ~irfan/my_notes.txt
          modified: YES
         user name: irfan   host name: irfan-HP-Laptop-15s-fq4xxx
        process ID: 3775
While opening file "my_notes.txt"
             dated: Sat Feb 03 20:49:05 2024
      NEWER than swap file!

(1) Another program may be editing the same file.  If this is the case,
    be careful not to end up with two different instances of the same
    file when making changes.  Quit, or continue with caution.
(2) An edit session for this file crashed.
    If this is the case, use ":recover" or "vim -r my_notes.txt"
    to recover the changes (see ":help recovery").
    If you did this already, delete the swap file ".my_notes.txt.swp"
    to avoid this message.

Swap file ".my_notes.txt.swp" already exists!
[O]pen Read-Only, (E)dit anyway, (R)ecover, (D)elete it, (Q)uit, (A)bort: 

New file added:%s/important/critical/g
~                                                                               
"my_notes.txt" 2L, 40C written  
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ vim my_notes.txt
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 

                                                                          
(15)Create a new user account named "john_doe." Set the user's home directory to "/home/john_doe" and assign the user to the "users" group.
--------------------------------------------------------------------------------------------------------------------------------------                   
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo useradd -m -d /home/john_doe -g users john_doe
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo useradd -m -d /home/john_doe -g users john_doe
useradd: user 'john_doe' already exists
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 


(16)Add the user "john_doe" to the sudoers file, allowing them superuser privileges. Confirm that "john_doe" can execute commands with sudo.
---------------------------------------------------------------------------------------------------------------------------------------

# Host alias specification

# User alias specification

# Cmnd alias specification

# User privilege specification
root    ALL=(ALL:ALL) ALL

# Members of the admin group may gain root privileges
%admin ALL=(ALL) ALL

# Allow members of group sudo to execute any command
%sudo   ALL=(ALL:ALL) ALL

# See sudoers(5) for more information on "#include" directives:

#includedir /etc/sudoers.d

                   [ line 31/31 (100%), col 1/1 (100%), char 755/755 (100%) ]
^G Get Help     ^O Write Out    ^W Where Is     ^K Cut Text     ^J Justify      ^C Cur Pos
^X Exit         ^R Read File    ^\ Replace      ^U Paste Text   ^T To Spell     ^_ Go To Line


(17)Modify the user account "john_doe" to change the default shell to "/bin/bash" and set the account's expiration date to one month from today.
-------------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chsh -s /bin/bash john_doe
[sudo] password for irfan: 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chage -E $(date -d '+1 month' +"%Y-%m-%d") john_doe
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chsh -s /bin/bash john_doe
[sudo] password for irfan: 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chage -E $(date -d '+1 month' +"%Y-%m-%d") john_doe
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ grep john_doe /etc/passwd
john_doe:x:1001:100::/home/john_doe:/bin/bash
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chage -l john_doe
Last password change					: Feb 03, 2024
Password expires					: never
Password inactive					: never
Account expires						: Mar 03, 2024
Minimum number of days between password change		: 0
Maximum number of days between password change		: 99999
Number of days of warning before password expires	: 7
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 

(18)Create a new group named "development_team." Add "john_doe" to this group and verify the group's existence.
----------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo addgroup development_team
Adding group `development_team' (GID 1001) ...
Done.
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo usermod -aG development_team john_doe
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ grep development_team /etc/group
development_team:x:1001:john_doe
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 


(19)Remove "john_doe" from the "users" group and add them to the "development_team" group. Confirm the changes.
----------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo deluser john_doe users
/usr/sbin/deluser: You may not remove the user from their primary group.
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo adduser john_doe development_team
The user `john_doe' is already a member of `development_team'.
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ groups john_doe
john_doe : users development_team
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 

(20)Delete the user account "john_doe" and ensure that their home directory is also removed.
---------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo userdel -r john_doe
userdel: john_doe mail spool (/var/mail/john_doe) not found
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 

(21)Delete the group "development_team" and ensure that all users previously belonging to the group are appropriately handled.
-------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo deluser john_doe development_team
/usr/sbin/deluser: The user `john_doe' does not exist.
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo deluser jane_smith development_team
/usr/sbin/deluser: The user `jane_smith' does not exist.
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo delgroup development_team
Removing group `development_team' ...
Done.
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ grep development_team /etc/group

(22)Implement a password policy that requires users to change their passwords every 90 days. Apply this policy to all existing and new user accounts.
-----------------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo nano /etc/login.defs
[sudo] password for irfan: 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chage --maxdays 90 --allusers
chage: unrecognized option '--allusers'
Usage: chage [options] LOGIN

Options:
  -d, --lastday LAST_DAY        set date of last password change to LAST_DAY
  -E, --expiredate EXPIRE_DATE  set account expiration date to EXPIRE_DATE
  -h, --help                    display this help message and exit
  -i, --iso8601                 use YYYY-MM-DD when printing dates
  -I, --inactive INACTIVE       set password inactive after expiration
                                to INACTIVE
  -l, --list                    show account aging information
  -m, --mindays MIN_DAYS        set minimum number of days before password
                                change to MIN_DAYS
  -M, --maxdays MAX_DAYS        set maximum number of days before password
                                change to MAX_DAYS
  -R, --root CHROOT_DIR         directory to chroot into
  -W, --warndays WARN_DAYS      set expiration warning days to WARN_DAYS

irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chage --maxdays 90 --allusers
chage: unrecognized option '--allusers'
Usage: chage [options] LOGIN

Options:
  -d, --lastday LAST_DAY        set date of last password change to LAST_DAY
  -E, --expiredate EXPIRE_DATE  set account expiration date to EXPIRE_DATE
  -h, --help                    display this help message and exit
  -i, --iso8601                 use YYYY-MM-DD when printing dates
  -I, --inactive INACTIVE       set password inactive after expiration
                                to INACTIVE
  -l, --list                    show account aging information
  -m, --mindays MIN_DAYS        set minimum number of days before password
                                change to MIN_DAYS
  -M, --maxdays MAX_DAYS        set maximum number of days before password
                                change to MAX_DAYS
  -R, --root CHROOT_DIR         directory to chroot into
  -W, --warndays WARN_DAYS      set expiration warning days to WARN_DAYS


(23)Manually lock the user account "john_doe." Attempt to log in as "john_doe" to confirm that the account is locked. Then, unlock the account.
------------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo passwd -S john_doe
john_doe L 02/03/2024 0 90 7 -1
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo passwd john_doe
New password: 
Retype new password: 
passwd: password updated successfully
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ su - john_doe
Password: 
su: warning: cannot change directory to /home/john_doe: No such file or directory
$ 


(24)Use the id command to display detailed information about the "john_doe" user, including user ID, group ID, and supplementary groups.
-----------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ id john_doe
uid=1001(john_doe) gid=1001(john_doe) groups=1001(john_doe)
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 


(25)Configure the password aging for the user "john_doe" to enforce a maximum password age of 60 days. Confirm that the changes take effect.
----------------------------------------------------------------------------------------------------------------------------------------
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chage -M 60 john_doe
[sudo] password for irfan: 
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chage -M 60 john_doe
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ sudo chage -l john_doe
Last password change					: Feb 04, 2024
Password expires					: Apr 04, 2024
Password inactive					: never
Account expires						: never
Minimum number of days between password change		: 0
Maximum number of days between password change		: 60
Number of days of warning before password expires	: 7
irfan@irfan-HP-Laptop-15s-fq4xxx:~$ 



































































