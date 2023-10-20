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
cd /home/alex/PycharmProjects/odoo-16-2/odoo-16.0
cd /home/alex/odoo-16.0
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

```
install addons 
```
```
install git
sudo apt install git
git config --global user.name "Oleksandr M"
git config --global user.email alexitmcaf@gmail.com
```
```
create ssh key
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
/home/alex/odoo-16.0/odoo/odoo-bin
-c /home/alex/odoo-16.0/conf/odoo.conf
/home/alex/odoo-16.0/odoo
comment in odoo.conf; logfile = /home/alex/odoo-16.0/logs/odoo.log

odoo-helper-fetch -r https://github.com/OCA/web.git

create dir probe in repositories dir and run
odoo-helper scaffold myaddon .
add to custom_addons
odoo-helper link .
install myaddon
odoo-helper-addons install myaddon
add for install from custom addons
odoo-helper link .


for update we can add to run configuration in Parametrs box: 
-u myaddon

# create module
odoo-helper-fetch -r git@github.com:aexitmcaf/odoo-s.git
odoo-helper scaffold kw_library repositories/aexitmcaf/odoo-s

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

# Error
[Errno 98] Address already in use odoo
```
ps -fA | grep python
sudo kill -process id
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
