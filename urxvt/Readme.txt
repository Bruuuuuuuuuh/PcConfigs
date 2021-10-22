if you are having problems with unicode characters in urxvt, make sure your localization settings are correct.
Use the locale command to get your data. Usually what's missing is the definition of "LC_ALL=" and "LANG=", so just edit the /etc/environment file and add the lines 

LC_ALL=en_US.UTF-8
LANG=en_US.UTF-8 

More information here: https://qastack.com.br/ubuntu/162391/how-do-i-fix-my-locale-issue
If this doesn't work, see more solutions here: https://github.com/powerline/powerline/issues/347

If you can't use "ç", edit (if this file doesn't exist, create him) ~/.xinitrc and add:
export LANG=pt_BR.UTF-8

Make sure the locale configs are the same in /etc/environment and ~/.xinitrc.
