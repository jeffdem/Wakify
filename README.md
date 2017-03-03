# Wakify
A spotify alarm clock Raspberry based

### Requirements
    - spotify premium account
    - working raspberry with raspbian

### On raspberry (based on raspbian):
    --------------
    Installation 
    --------------
    - wget -q -O - https://apt.mopidy.com/mopidy.gpg | sudo apt-key add -
    - #sudo wget -q -O /etc/apt/sources.list.d/mopidy.list https://apt.mopidy.com/jessie.list
    - edit apt source.list : deb http://apt.mopidy.com/ stable main contrib non-free deb-src http://apt.mopidy.com/ stable main contrib non-free
    - sudo apt-get update
    - sudo apt-get upgrade
    - sudo apt-get install mopidy
    - sudo apt-get install mopidy-spotify
    - add in /etc/mopidy/mopidy.conf :
        - [spotify]
        - enabled = true
        - username = yourlogin
        - password = yoursecretpass
    - Obsolete : install iris (webclient)
        - apt-get install python-pip
        - pip install Mopidy-Iris
    - sudo service mopidy restart
    - sudo update-rc.d mopidy enable
    
    -----------
    Tests 
    -----------
    - MPC :
        - sudo apt-get install mpc
        - mpc add spotify:user:jeffdem:playlist:4hGM0zgnXmACBaOjTyjOAl
        - mpc random
        - mpc play
        - mpc volume 50
        - mpc clear
    - IRIS :
        - http://127.0.0.1:6680/iris
