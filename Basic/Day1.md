#Ansible written in Python there is dependency where you need Python to be installed in Linux disto
#For Windows it is Powershell supported
#Facts : Ansible gathers the system information used for multiple usecases
1. Where we have ansible.builtin.package ansible should know which one to connect based on distribution, it checks facts and understands the distribution

Ansible is a tool built in top of Python where in backend it has python programming, for example:
    1. Idempotency - How it is checked in Bash or Python we need condtional statement to write and manage the code now with Ansible we have this feature is builtin, and Idempotency is where first time it runs the commands and if next time same thing is run and if it sees the config is similer it just says config is available i am not going to do any changes and output shows as "OK" , if not available will be created.