# sshpass-script

Written a script to ssh to any machine without a Password, without worrying about changes to public ssh keys

**Script Steps**

1. Check if any argument is given to the script, if not then exit
2. Find any public SSH key for the given IP in known_hosts and delete them
3. Add the latest public SSH key of the given IP to /.ssh/known_hosts
4. Try to ssh


**How to run**

1. Clone the repo 

2. Install sshpass using your package manager, brew for MacOS users, use yum package manager for CentOS/RHEL
   ```
   brew install sshpass
   ```

4. Make the klogin file as an executable
   ```
   chmod +x klogin
   ```

6. Add the path of this directory to your PATH, example: "/Users/garvit.bhateja/sshpass-script"
   ```
   sudo vi /etc/paths
   ```

8. SSH using follwoing command
   ```
   klogin 10.10.10.10
   ```
