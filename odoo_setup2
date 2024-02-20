sudo apt-get update
sudo apt-get upgrade
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt install python3.11 -y
sudo apt-get install git
mkdir odoo_projects
cd odoo_projects/
git clone -b 17.0 --single-branch --depth=1 https://github.com/odoo/odoo.git
mv odoo odoo17
git clone -b 16.0 --single-branch --depth=1 https://github.com/odoo/odoo.git odoo16





/odoo_projects
sudo apt-get install openssh-server
sudo apt-get install -y python3-pip -y

sudo apt-get install python3-dev libxml2-dev libxslt1-dev zlib1g-dev libsasl2-dev libldap2-dev build-essential libssl-dev libffi-dev libmysqlclient-dev libjpeg-dev libpq-dev libjpeg8-dev liblcms2-dev libblas-dev libatlas-base-dev

sudo apt-get install -y npm
sudo pip install virtualenv
sudo apt-get install -y python3.11-venv
python3.11 -m ensurepip
python3.11 -m venv odoo17env

python3.11 -m venv odoo16env
sudo apt-get install -y npm
sudo ln -s /usr/bin/nodejs /usr/bin/node
sudo npm install -g less less-plugin-clean-css
npm audit fix --force
sudo apt-get install -y node-less

sudo apt-get install postgresql
sudo su postgres
psql -d postgres
create role sunrise with superuser login password 'a';
\q

source odoo17env/bin/activate
cd odoo_projects/odoo17
pip install whell
pip install --upgrade pip
pip install -r requirements.txt

you will get (ERROR: Could not build wheels for psycopg2, python-ldap, which is required to install pyproject.toml-based projects)
for that open odoo_projects/odoo17 requirements.txt and remove directly (
31 psycopg2==2.9.2 ; sys_platform != 'win32' and python_version <= '3.10'
32 psycopg2==2.9.5 ; python_version > '3.10' or sys_platform == 'win32'
38 python-ldap==3.4.0 ; sys_platform != 'win32'  # min version = 3.2.0 (Focal with security backports)
)

ang again run 
pip install -r requirements.txt

pip install psycopg2-binary

python odoo-bin

cecc-epe5-frt5 odoo17 master pass
