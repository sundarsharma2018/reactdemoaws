install putty by 
//https://www.puttygen.com/download-putty#PuTTY_for_linux

then convert pem to ppk
https://www.codegrepper.com/code-examples/shell/how+to+convert+pem+to+ppk+in+ubuntu

then insert public ip in session and choose auth insert .ppk file and save
cmd ll open then insert username like ec2-user
-> sudo su
-> ls
-> mkdir workspace
-> cd workspace
-> install git, npm, nodejs, pm2 globally, serve globally


//error
Try installing the active LTS version instead of latest with nvm install 16 (instead of nvm install node) as per the examples.

This is was tested on the docker image amazonlinux:2 and correlates to what AWS CDK supports (ref)

//install git
https://www.codegrepper.com/code-examples/shell/installing+git+on+ec2


//install pm2 
npm install pm2 -g

More info
https://www.youtube.com/watch?v=I_FmJGtOePk&list=PL_ouohgNX4xbSFWk61_qq4jzZuYbhiGah&index=13


//redeploy website on aws ec2
https://docs.aws.amazon.com/codedeploy/latest/userguide/tutorials-windows-update-and-redeploy-application.html


//Again deploy

commit from vishul code and update npm run build thhen got to putty call git pull


///import 
https://www.youtube.com/watch?v=h-h2Po7Xwbc&t=3s



//pm2 command
pm2 serve build 80 --spa


pm2 start npm -- start
pm2 stop  npm -- stop
pm2 list
pm2 startup



//How to Clear Cache and Swap Space in Ubuntu/Linux

https://www.youtube.com/watch?v=E9M5OYX4z7c
For Clearing pagecache, dentries, and inodes.

echo 3 {use gaterthan symbol}/proc/sys/vm/drop_caches
//For Clearing Swap Space 

swapoff -a && swapon -a



//deploy code step
//vishul studio
npm run build
git status
git add .
git commit -m ""
git push -u origin branchname
//putty
session ->hostname(43.204.84.32 or public ip) 
Saved session
SSH->Auth->private key file for authentication (.ppk file) ->open
ec2-user
sudo su
cd workspace
cd reactdemoaws
nvm i 16
git status
git pull


//How to migrate EC2 instance from one region to another region
https://www.youtube.com/watch?v=xK6oZc3TqJ4

steps
1. stop instance
2. create AMI
3. copy AMI to another region
4. Lunch instance

