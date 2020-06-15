# kaggle-to-github(for LINUX USERS)
A Bash command line which pull your Kaggle kernel and push it to Github repo.
### Step 1
Spawn an EC2 instance on AWS if you are not an Linux user
### Step 2
run these commands:
yum install python3
yum install python-pip or yum install python3-pip

### Step 3
Get API token from Kaggle--> My Account -->Create new API token
Put token file in /root/.kaggle/kaggle.json
chmod 600 kaggle.json

### Step 4 
Run the script


# kaggle-to-github(for Windows USERS)
A Bash command line which pull your Kaggle kernel and push it to Github repo.
### Pre-requisites
Python should be Installed, preferably ANACONDA
### Step 2
run these commands:
pip3 install kaggle
### Step 3
Get API token from Kaggle--> My Account -->Create new API token
Put token file in C:\Users\<Windows-username>\.kaggle\kaggle.json - you can check the exact location, sans drive, with echo %HOMEPATH%)

### Step 4 
git clone https://github.com/$GITHUB_USERNAME/$REPO.git
or if you don't want to clone, do 'git init' to initialize git rpeository
kaggle datasets download $DATASET -p ./$REPO/kaggle/input/$KERNEL/ --force  --unzip

kaggle kernels pull (YOUR-KAGGLE-NAME)/(KAGGLE-REPO)
git stage --all
git commit -m "Added a new kernel"
git push

