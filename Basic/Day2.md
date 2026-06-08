Basic adhoc commands:
adhoc commands uses modules to run the commands in backend.
#For example: 
ansible <servers mentioned in ini> -m shell -a "uptime | grep "test" 
Modules: ping, command, shell, file, copy,script
sudo dnf install ansible-core

Variable Preference Order:

1.Task level
2.var_files under play Level
3.promt under play level # Kind of user input
4.play level vars
5.invenory vars # 1. host level 2. group level


