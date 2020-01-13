Hello Dev!!!!!!!!!!!!!!!!!!!!
## Creating an Instance
1.	Ubuntu Server 18.04 LTS (HVM), SSD Volume Type
2.	T2 micro
3.	Enable auto-assign IP
4.	Skip storage
5.	Added tag
6.	Source my IP

## Steps
1.	Decide where we want to SSH into
cd ~/.ssh
ssh -i ~/.ssh/keyname.pem ubuntu@IP (ip is your public IP)
Note: don’t need ~/.ssh/ however makes it absolute (can be used everywhere)
exit
ssh -i keyname.pem ubuntu@IP

2.	Manually deploying code to a server online using the provisions
atom . to deployment code
Make sure the provisions are executable in app by using command ll in the folder and db admin, owner and groups should be executable
If not chmod +x provision.sh or can do it inside linux
If we want to run in linux from windows – dos2unix -h
Back to app to provision - dox2unix provision.sh
Using SCP command to securely copy files from local machine to AWS
•	To use scp with a key pair use the following command: scp -i path/to/key file/to/copy user@ec2-xx-xx-xxx-xxx.compute-1.amazonaws.com:path/to/file.
•	To use it without a key pair, just omit the flag -i and type in the password of the user when prompted.
Can use it in recursive mode when you want to transfer several files at once
•	To copy a directory (in this case environment) to Ubuntu
•	scp -i ~/.ssh/keyname -r ../environment/ ubuntu@IP:/home/ubuntu/


scp -i ~/.ssh/keyname ../environment/app/provision.sh ubuntu@IP6:/home/ubuntu/file.sh
the file should then be in your ubuntu shell

To run provision file:
./filename.sh

To give executable instructions:
chmod +x provision.sh

To set a path e.g. if you had to download dos2unix (check it using command dos2unix -h)
Path > edit system environment variables > environmental envariables
Copy dos2unix and put it inside windows/system32

## To terminate:
Exit ubuntu...
Actions > Instance State > Stop > wait to stop then Terminate
To run it had to add
sudo npm install ejs mongoose express into app / installed twice using
sudo apt install npm, npm install then npm start
To add features such as images on the reverse proxy in port 80 sudo vi into default in /etc/nginx/sites-enabled and make the changes.
Use cat default to check that the change is made.
