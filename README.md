# jupyterhub-DO

## Installation of Jupyterhub on Digital Ocean Ubuntu 16.04

1. Setup user with sudo privileges

2. Update/Upgrade packages:

    - `$ sudo apt-get update`
    - `$ sudo apt-get dist-upgrade`
    
3. Install required packages:

    - `$ sudo apt-get install git fail2ban python3-pip python3-dev nginx build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev`

4. Install npm tools:

    - `$ sudo apt-get install npm nodejs-legacy`
    - `$ sudo npm install -g configurable-http-proxy`

5. Install virtualenv tools:

    - `$ sudo pip3 install virtualenv virtualenvwrapper`
    
6. Setup bash aliases:

    - Append following lines to `~/.bashrc`
      * `$ export WORKON_HOME=~/.virtualenvs`
      * `$ export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3`
      * `$ source /usr/local/bin/virtualenvwrapper.sh`
     
   - Run `source ~/.bashrc`

7. Use pyenv to download desired version of Python:

    - Clone pyenv
        * `$ git clone https://github.com/yyuu/pyenv.git ~/.pyenv`
    - Install desired version of Python (3.6.1 in this example)
        * `$ sudo ~/.pyenv/bin/pyenv install 3.6.1`
        
8. Create virtual environment using virtualenvwrapper:

    - Using Python 3.6.1 installation with venv name __jhub__
        * `$ mkvirtualenv -p ~/.pyenv/versions/3.6.1/bin/python jhub`
        
8. Prepare virtualenv __jhub__:

    - Enable virtualenv
        * `$ workon jhub`
    - Install jupyterhub
        * `(jhub)$ pip install jupyterhub`
    - Install/Updgrade Jupyter notebook
        * `(jhub)$ pip install --upgrade notebook`
        
9. Test initial setup:
    - Launch jupyterhub
        * `(jhub)$ jupyterhub`
    - Login using sudo user credentials
