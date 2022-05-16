
AWS CLI installation in centos/ amazon:

yum install python3

curl -O https://bootstrap.pypa.io/get-pip.py

python3 get-pip.py --user

ls -a ~

export PATH=~/.local/bin:$PATH

source ~/.bash_profile

pip3 --version

pip3 install awscli --upgrade --user

yum install pip -y

pip install boto
