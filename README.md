# aws-ciccd-ebs





#JDBC
JDBC_CONNECTION_STRING typically refers to the connection 
string used to establish a connection to a relational database using Java Database Connectivity (JDBC)


###Create RDS

Allow port 3306 in RDS SG from Beanstalk SG 

Init DB 
Ssh to BS instance
INstall MYSQL client
Deploy db_backup.sql file

Update health check 


yum install mariadb


 mysql -h preproddb.cwvkmjbyihka.us-east-1.rds.amazonaws.com -u admin -p

 ls src/main/resources/db_backup.sql

mysql -h preproddb.cwvkmjbyihka.us-east-1.rds.amazonaws.com -u admin -p'Passws' Accounts < src/main/resources/db_backup.sql



 (/c/Users/Guest Login/.ssh/id_rsa): /c/Users/Guest Login/.ssh/preprod-coderepo_rsa

 cat preprod-coderepo_rsa.pub

Create config file –if codecommit is done use this login
Host git-codecommit.*.amazonaws.com
    User APKAWK46G4URVCGN27HW
    IdentityFile ~/.ssh/preprod-coderepo_rsa



Host git-preprod-coderepo.*.amazonaws.com
        User APKAWK46G4URVCGN27HW
        IdentityFile ~/.ssh/preprod-coderepo_rsa

 ssh git-codecommit.us-east-1.amazonaws.com
 git clone ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/profilerepo




FINALLY:

cat .git/config
[core]
        repositoryformatversion = 0
        filemode = false
        bare = false
        logallrefupdates = true
        symlinks = false
        ignorecase = true
[remote "origin"]
        url = ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/profilerepo
        fetch = +refs/heads/*:refs/remotes/origin/*





# Remove the 'profilerepo/' directory recursively
rm -rf profilerepo/

# Remove all files in 'profilerepo/'
rm -f profilerepo/*

# Display the content of the 'config' file
cat config

# Navigate to the home directory
cd

# Navigate to the '/tmp/' directory
cd /tmp/

# Clone the CodeCommit repository 'profilerepo' using SSH
git clone ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/profilerepo

# Navigate to the home directory
cd

# Clone the GitHub repository 'vprofile-project.git' using HTTPS
git clone https://github.com/devopshydclub/vprofile-project.git

# List the contents of the current directory
ls

# List the contents of the current directory again
ls

# Navigate to the 'vprofile-project/' directory
cd vprofile-project/

# List the contents of the 'vprofile-project/' directory
ls

# Incorrect command - 'git checout master', corrected to 'git checkout master'
git checkout master

# Corrected command - 'git checout master' to 'git checkout master'
git checkout master

# List the contents of the current directory
ls

# List the contents of the current directory again
ls

# Navigate to the home directory
cd

# Incorrect command - 'vprofile-project > /tmp/', corrected to 'cp -r vprofile-project /tmp/'
cp -r vprofile-project /tmp/

# List the contents of the current directory
ls

# Navigate to the 'vprofile-project/' directory
cd vprofile-project/

# List the contents of the 'vprofile-project/' directory
ls

# Navigate to the '/tmp/' directory
cd /tmp/

# List the contents of the '/tmp/' directory
ls

# Navigate to the home directory
cd

# Navigate to the 'vprofile-project/' directory
cd vprofile-project/

# List the contents of the 'vprofile-project/' directory
ls

# List all remote branches, extract branch names, and store them in a file
git branch -a | grep -v HEAD | cut -d '/' -f3 | grep -v master > /tmp/branches

# Display the content of the '/tmp/branches' file
cat /tmp/branches

# Incorrect loop syntax - 'for i in 'cat /tmp/branches'', corrected to 'for i in $(cat /tmp/branches)'
for i in $(cat /tmp/branches); do echo $i; done

# Display the content of the '/tmp/branches' file
cat /tmp/branches

# Corrected loop syntax - 'for i in $(cat /tmp/branches); do echo $i; done'
for i in $(cat /tmp/branches); do echo $i; done

# Checkout each branch listed in '/tmp/branches'
for i in $(cat /tmp/branches); do git checkout $i; done

# Fetch tags from the remote repository
git fetch --tags

# Remove the existing remote 'origin' and add a new 'origin' pointing to the CodeCommit repository using SSH
git remote rm origin
git remote add origin ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/profilerepo

# Display the content of the '.git/config' file
cat .git/config

# Display the command history
History

git push origin --all




Build
##
##Docker will create run and die



Codebuild-preprod-build-service-role

####Builspec yaml file

Replace pwd with rds pwd 
##Build test
##create Pipeline


Get project
#https://github.com/devopshydclub/vprofile-project.git
