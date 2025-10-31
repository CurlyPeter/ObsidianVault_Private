![](ximg_58e25fec436c6.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.gFewdPVMAu.png)

The bash shell is the standard terminal environment included with most Linux distributions, included with macOS, and <a href="https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/" rel="noopener" class="external-link" target="_blank"><u>available for installation on Windows 10</u></a>. It remembers the commands you type and stores them in a history file. You probably know a few basics of the bash history, but it’s a lot more powerful than you might realize.


## **Keyboard Shortcuts**
**RELATED:** <a href="https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/" rel="noopener" class="external-link" target="_blank"><b><i><u>The Best Keyboard Shortcuts for Bash (aka the Linux and macOS Terminal)</u></i></b></a>
To scroll through your bash history, you can use a few of <a href="https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/" rel="noopener" class="external-link" target="_blank"><u>bash’s many useful keyboard shortcuts</u></a>. Press these shortcuts and commands you’ve previously used will appear at the prompt.
- **Up Arrow** or **Ctrl+P**: Go to the previous command in your history. Press the key multiple times to walk backwards through the commands you’ve used.
- **Down Arrow** or **Ctrl+N**: Go to the next command in your history. Press the key multiple times to walk forwards through the commands you’ve used.
- **Alt+R**: Revert any changes to a command you’ve pulled from your history if you’ve edited it on the current line.
Bash also has a special “recall” mode you can use to search for commands you’ve previously run, rather than scrolling through them one by one.
- **Ctrl+R**: Recall the last command matching the characters you provide. Press this shortcut and start typing to search your bash history for a command.
- **Ctrl+O**: Run the command you found with Ctrl+R.
- **Ctrl+G**: Leave the history searching mode without running a command.

![](ximg_58c09a8605fed.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.jpPFZK6W2R.png)

## **View Your Bash History**
You can print your entire bash history to the screen by running a single command:
history
You’ll see a list of all the commands in your bash history, along with a number to the left of each. The command with a “1” next to it is the oldest command in your bash history, while the command with the highest number is the most recent.

![](ximg_58e24cc02d84e.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.DTXkJst6Y3.png)

**RELATED:** <a href="https://www.howtogeek.com/110150/become-a-linux-terminal-power-user-with-these-8-tricks/" rel="noopener" class="external-link" target="_blank"><b><i><u>Become a Linux Terminal Power User With These 8 Tricks</u></i></b></a>
You can do anything you like with the output. For example, you could <a href="https://www.howtogeek.com/110150/become-a-linux-terminal-power-user-with-these-8-tricks/" rel="noopener" class="external-link" target="_blank"><u>pipe it</u></a> to the grepcommand to search your command history.
history | grep your_search

![](ximg_58e24d2ab7a2b.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.Tg54w5m53w.png)

You could also pipe it to the tail command to view only a small number of the recent commands you’ve run. For example, the following command would show the last 5 entries in your history.
history | tail -5

![](ximg_58e25953e3709.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.f3LguITaqm.png)

## **Run Commands From Your History**
Bash can quickly “expand” previous commands, or expand them and modifying them. This feature is known as “history expansion” and uses an exclamation mark, known as a “bang”. Just type them at the prompt and press Enter to run them like you’d run any other command.
To run a specific command from your history by its number, use the following command:
!#
For example, let’s say you wanted to run the 12th command from your bash history. That’s the command with a “12” to the left of it when you run the history command. You’d type the following command.
!12

![](ximg_58e25152b1206.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.E9SyMOuDIK.png)

To re-run the last command you ran, type the following. This has the same effect as pressing the Up arrow once to view the previous command and then pressing Enter.
!!
You can also refer to a command a certain number of lines back. For example, !-2 would run the second to last command you ran. !! means the same thing as !-1 .

![](ximg_58e25145afc88.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.1XEgJM9oIx.png)

This expansion works anywhere on the line. You can add anything you like before or after !! or any of the other expressions in this section. For example, you can type the following command to rerun the last command you ran through sudo, giving it root privileges. This is particularly useful if you forget to add  sudo before running a command.
sudo !!
Or, for example, you could rerun the previous command and pipe its output to grep to search for some text.
!! | grep text

![](ximg_58e3b008adc1a.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.SHjT653gJV.png)

To search for a command in your history and run it, type the following. This will run the last command that matches the text you specify:
!text
So, if you recently ran a command that began with ping, you can run the following command to search for it. This will search backwards through your history, locate the most recent command that begins with “pi“, and immediately run it:
!pi

![](ximg_58e25133e2ceb.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.obCeNuBDXH.png)

You can append a :p to any of the above expansions and bash will print the command to the terminal without running it. This is useful if you want to confirm you’re selecting the correct command before you run it.
!12:p
!!:p
!text:p

![](ximg_58e25c74dcc84.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.DBQTQ-bqM2.png)

## **Reuse Arguments From Your History**
Bash also allows you to run a new command, but use arguments from previous commands in your history. This can help you quickly reuse long or complicated arguments without having to retype them.
command !$
For example, let’s say you ran the command touch /home/chris/some_long_file_name_you_dont_want_to_type_again . You now want to run the command nano /home/chris/some_long_file_name_you_dont_want_to_type_again. Rather than typing the whole thing from scratch, you could run:
nano !$
The !$ would make bash automatically fill in the last argument from your previous command.

![](ximg_58e252512621b.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.bsziF5Lbci.png)

This only fills in the last argument. So, if you run ping google.com -c 4 and then run ping !$ , this would just expand to “ping 4“.
To fix this situation, you can use the following trick to expand the first argument on the line, rather than the last:
command !^
So, if you ran ping google.com -c 4 and then ran ping !^ , bash would expand this to “ping google.com".

![](ximg_58e25501535c9.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.P7XjiovvPc.png)

To fill in all the arguments used in the previous command instead of just a single argument, you’d use the following:
command !*
So, if you ran ping !* instead, bash would automatically fill in all the arguments you used in the previous command.

![](img_58e255cc79926.png)

You can use the same trick you use to run commands from your history to get arguments from them. Just use the following form.
command !abc:#
For example, we ran the command sudo hostname ubuntu earlier. If we run the following command, bash will search backwards through the history to find the last command beginning with the letters we type and fill in the argument we specify. So, if we run echo !su:2 , bash will search back to find the last command beginning with “su” and fill in its second argument, which is “ubuntu“.
Other tricks work as you might expect. For example, replacing the number with an asterisk, known as the wildcard, causes bash to fill in all arguments from the command:
command !abc:*

![](img_58e2578705d77.png)

## **Rerun the Previous Command and Modify It**
Bash also allows you to rerun the previous command and specify something that should be changed. This can be useful for correcting a typo in a command. For example, the following command will rerun the previous command, replacing the text “abc” in it with the text “xyz“.
^abc^xyz
For example, if you accidentally ran ping gogle.com, you could then run ^gog^goog and bash would run the command ping google.com instead.

![](ximg_58e25db2a1eb3.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.1UUg5MkAUN.png)

## **Where Your History Is Stored, and How to Clear It**
The bash shell stores the history of commands you’ve run in your user account’s history file at~/.bash_history by default. For example, if your username is bob, you’ll find this file at /home/bob/.bash_history.
Because your history is stored in a file, it persists between sessions. You can run some commands, sign out, come back the next day, and those commands will still be in your history file ready to view and use. Each user account has its own history file with a separate command history.
To clear your bash history, you can run the following command. This erases the contents of your user account’s .bash_history file:
history -c

![](ximg_58e26077acf8e.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.me1RUB5EFs.png)

Bash only remembers a limited number of commands by default, preventing the history file from growing too large. The number of history entries bash remembers is controlled by the HISTSIZEvariable. The default is usually 500 or 1000 entries. You can run the following command to view the size of the bash history on your system.
echo $HISTSIZE
To set your history to zero, run the following command.
HISTSIZE=0
For the current session, bash won’t store any history entries unless your run a command like HISTSIZE=1000 to set it back to a certain number of entries.

![](ximg_58e260434460e.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.e94bphs_E8.png)

## **How to Ignore Spaces and Duplicates**
Bash allows you to ignore history entries that begin with a space if you set the HISTCONTROLvariable to ignorespace.
HISTCONTROL=ignorespace
Type a space before a command before running it in the bash shell and the command will run normally, but won’t appear in your history if you have this variable enabled. This allows you to keep your history a bit cleaner, choosing to run commands without them appearing in your history.

![](img_58e262f13abe7.png)

Bash also allows you to ignore duplicate commands that can clutter your history. To do so, set HISTCONTROL to ignoredups.
HISTCONTROL=ignoredups

![](img_58e2623406800.png)

To use both the ignorespace and ignoredups feature, set the HISTCONTROL variable to ignoreboth.
HISTCONTROL=ignoreboth
Note that bash variables you set will only persist for the current session. You’ll need to add these to your user account’s .bashrc file to have these values automatically set in every bash session you start, if you prefer that.

![](img_58e2627bd6d06.png)

The bash shell is a complex tool with many more options than these. Consult the <a href="https://www.gnu.org/software/bash/manual/html_node/Bash-History-Builtins.html" rel="noopener" class="external-link" target="_blank"><u>Bash History Builtins</u></a> and <a href="https://www.gnu.org/software/bash/manual/html_node/History-Interaction.html" rel="noopener" class="external-link" target="_blank"><u>History Expansion</u></a> sections in the official bash manual more detailed information and other advanced tricks you can use.
## **READ NEXT**
		› [How to Hide or Disable Meet Now in Windows 10](https://www.howtogeek.com/704215/how-to-hide-or-disable-meet-now-in-windows-10/)
		- › [How to Search Open Tabs on Google Chrome](https://www.howtogeek.com/704212/how-to-search-open-tabs-on-google-chrome/)
		- › [How to Send Someone Money with Google Pay](https://www.howtogeek.com/703524/how-to-send-someone-money-with-google-pay/)
		- › [How to Create a Checklist in Microsoft Excel](https://www.howtogeek.com/698565/how-to-create-a-checklist-in-microsoft-excel/)
		- › [How to Quickly Turn Off App Notifications on Mac](https://www.howtogeek.com/701233/how-to-quickly-turn-off-app-notifications-on-mac/)