# odoo_setup
```
wget -O /tmp/odoo-helper-install.bash https://gitlab.com/katyukha/odoo-helper-scripts/raw/master/install-system.bash;
sudo bash /tmp/odoo-helper-install.bash;
odoo-helper install pre-requirements
odoo-helper install postgres
odoo-helper install sys-deps 16.0
odoo-install --odoo-version 16.0 --dev --archive --db-user odoo16 --create-db-user --http-port 15069
sudo apt install mc
```
copi path from
Odoo installation path: 
adn put in terminal
example
```
cd /home/alex/PycharmProjects/odoo-16-2/odoo-16.0
cd /home/alex/odoo-16.0
```
and run mc and you will see file in mc
```
mc
```
```
odoo-helper server --help
```
```
odoo-helper start
```
```
odoo-helper db --help
odoo-helper db create --help
odoo-helper db create --demo --tdb --install crm
```
```
http://localhost:15069
email  admin
password  admin
```


qyxq vjhe glsh xzmc

install addons 


install git
```
sudo apt install git
```
```
git config --global user.name "Oleksandr M"
git config --global user.email alexitmcaf@gmail.com
```

create ssh key
```
ssh-keygen -t rsa -b 4098
enter enter enter
```
```
copy ssh key
cat ~/.ssh/id_rsa.pub
```

in custom addons
```
git clone -b 15 --single-branch --depth=1 git@github.com:GarazdCreation/odoo-school.git
```
after you can link in reposutory folder 
```
odoo-helper link .
```
add path to config 
/odoo-16.0/custom_addons/odoo-school

/odoo-16.0/custom_addons/odoo-school
```
git status

git checkout -b 15.0-TASK-1.4
```
change something
```
nano school_lesson_6_1/__manifest__.py
```
```
git status
git diff
```
```
git commit -am '[REF] school_lesson_6_1: change module summary'
```
```
git push --set-upstream origin
git push --set-upstream origin 15.0-TASK-1.4
```

config pyCharm
add configuration
```
/home/alex/odoo-16.0/odoo/odoo-bin
```
```
-c /home/alex/odoo-16.0/conf/odoo.conf
```
```
/home/alex/odoo-16.0/odoo
```
comment in odoo.conf; logfile = /home/alex/odoo-16.0/logs/odoo.log
```
odoo-helper-fetch -r https://github.com/OCA/web.git
```

create dir probe in repositories dir and run
```
odoo-helper scaffold myaddon .
```
add to custom_addons
```
odoo-helper link .
```
install myaddon
```
odoo-helper-addons install myaddon
add for install from custom addons
odoo-helper link .
```


for update we can add to run configuration in Parametrs box: 
```
-u myaddon
```

# create module
```
odoo-helper-fetch -r git@github.com:aexitmcaf/odoo-s.git
odoo-helper scaffold kw_library repositories/aexitmcaf/odoo-s
```

ad models security views

instal module
```
odoo-helper-addons install kw_library
```

check code linter
```
odoo-helper flake8 repositories/aexitmcaf/odoo-s/
```
```
odoo-helper pylint repositories/aexitmcaf/odoo-s/
```
```
odoo-helper lint pylint .
```

# Error
[Errno 98] Address already in use odoo
```
ps -fA | grep python
kill -9 000000
sudo kill -process id
sudo pkill python
```

# install PgAdmin
```
curl  -fsSL https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/pgadmin.gpg
```
then install curl if need

then
```
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list'
```

then
 check the contents of the repository file created using the following command
 ```
$ cat /etc/apt/sources.list.d/pgadmin4.list
```

then
```
1- sudo apt-get install wget ca-certificates
2- sudo apt-get update
3- sudo apt-get upgrade
4- sudo apt-get install pgadmin4
deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/bullseye pgadmin4 main
```
#check pull request
```
git pull origin pull/5/head
```

#check remote branches 
```
git clone git@github.com...............................
git branch -r
git fetch origin <remote branche name>
git checkout <remote branche name>

git clone git@github.com...............................
git branch -a
git checkout -b testing origin/testing

git pull
git branch
```
version tag
```
git tag v1.0.0
git push origin v1.0.0
git checkout v1.0.0
```
kill proucess
```
sudo pkill python
```
#test module with tag (library), add conf after -i in odoo-bin 
```
school_lesson_6_4
--test-tags
library
--test-enable
--log-level=test
--stop-after-init
```
#test without for example (access) tag
```
school_lesson_6_4
--test-tags=-access
--log-level=test
--stop-after-init
```
#test module school_lesson_6_4, add / and name module
```
school_lesson_6_4
--test-tags=-access/school_lesson_6_4
--log-level=test
--stop-after-init
```
#run test for TestForm class in school_lesson_6_4, add : and class name
```
school_lesson_6_4
--test-tags=/school_lesson_6_4:TestForm
--log-level=test
--stop-after-init
```
#run test for method test_02_library_admin_access_rights from TestAccessRights class in school_lesson_6_4, add : and class name . and method name
```
school_lesson_6_4
--test-tags=/school_lesson_6_4:TestAccessRights.test_02_library_admin_access_rights
--log-level=test
--stop-after-init
```

#ssh
```
cd ~/.ssh
cat id_rsa.pub
```

```
git clone git@github.com: some  repo url
git fetch origin main
git checkout main
git merge develop
git tag v1.0.0
git push origin v1.0.0


git tag -d v1.0.0
git push -d origin v1.0.0

```

#Two separate repo with ssh
```
mkdir -p ~/.ssh

ssh-keygen -t rsa -b 4096 -C "mc@gmail.com" -f ~/.ssh/id_rsa_mc

ssh-keygen -t rsa -b 4096 -C "mcr@gmail.com" -f ~/.ssh/id_rsa_mcr
```
#Start the SSH agent and add the generated keys:
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa_mc
ssh-add ~/.ssh/id_rsa_mcr
```
#Copy the new public keys to your clipboard:

```
cat ~/.ssh/id_rsa_mc.pub
cat ~/.ssh/id_rsa_mcr.pub
```
#Edit the SSH config file to specify which key to use for each host:

```
nano ~/.ssh/config
```
#Add the following configurations:
```
Host github.com-mc
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_mc

Host github.com-mcr
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_mcr
```
```
git clone git@github.com-mc:mc/res.git

git clone git@github.com-mcr:mcr/res.git
```
if it is error 
ERROR: Permission to mcafmorps/resource_management.git denied to MORPSmcaf.
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists
```
sudo nano ~/.ssh/config
```
git remote -v
```
#check
```
ssh -T git@github.com-something
ssh -T git@github.com-something2
```
#run
```
git remote set-url origin git@github.com-something:.....................git
```
