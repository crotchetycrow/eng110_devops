## Setting up git repository

- From terminal, cd to directory on your local machine where you want the repo to be
- git clone {URL}
- nano README.md
  - Edit and save
- git add .
- git commit -m "Message here"
- git push

## Setting up VM with vagrant and virtualbox

- From terminal, cd to directory where the project is located
- vagrant init "ubuntu/xenial64"
  - Initialises VM so that it can be used with ubuntu
- vagrant up
  - Creates guest machines according to your Vagrantfile config
- vagrant status
  - Check the status of the VM
- vagrant ssh
  - Establish SSH session into VM to give shell access
- sudo apt-get update
  - Connect VM to internet
- vagrant halt
  - To stop VM
