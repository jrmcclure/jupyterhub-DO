# jupyterhub-DO

## Installation of Jupyterhub on Digital Ocean Ubuntu 16.04

1. Setup user with sudo privileges

2. Update/Upgrade packages:

    - `sudo apt-get update`
    - `sudo apt-get dist-upgrade`
    
3. Install required packages:

    - `sudo apt-get install git fail2ban python3-pip python3-dev nginx build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev`
    
4. Install virtualenv tools:

    - `sudo pip3 install virtualenv virtualenvwrapper`
    
5. Setup bash aliases:

    - Append following lines to `~/.bashrc`
      * `export WORKON_HOME=~/.virtualenvs`
      * `export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3`
      * `source /usr/local/bin/virtualenvwrapper.sh`
     
   - Run `source ~/.bashrc`
