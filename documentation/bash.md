## Bash scripts

### Set of commands/instructions from the `user` to `OS`

---

- Create `.sh` file
- First line !/bash/bin
- !/bin/bash - Install shebang

- Communicate with OS that this is going to be a bash script

- `sudo apt-get update -y` - Run updates

- `sudo apt-get upgrade -y`- Run upgrades

- `sudo apt-get install nginx -y` - install nginx

- `sudo systemctl start nginx` - Start nginx

- `sudo systemctl enable nginx` - Enable nginx

Upon script creation, `chmod +x provision.sh` then `sudo ./provision.sh` to enable script in terminal

---

## Running scripts alongside `vagrant up`

- Follow the above steps to create script

- Add `config.vm.provision "shell", path: "provisioning.sh"` to Vagrantfile

  - configure the vm, provisioner type shell script, the provisioner is located at PATH

- `vagrant provision`

  - Runs any configured provisioners against the running Vagrant managed machine.

- `vagrant reload`

- Run localhost(the IP you set)

---

## Automating set up process for dev env

- `#!/bin/bash`

- `sudo apt-get update -y`

- `sudo apt-get upgrade -y`

- `sudo apt-get install nginx -y`

- `sudo systemctl start nginx`

- `sudo systemctl enable nginx`

The above is the same process as previous script.

- `cd app/app` - Changes into the appropriate directory

- `sudo apt-get install nodejs -y` - Installs nodejs

- `sudo apt-get install python-software-properties -y` - Installs python-software-properties

- `curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -` -
  Makes a curl request to https://deb.nodesource.com and downloads the specific nodejs version (in this case 12)

- `sudo apt-get install -y nodejs` -
  Installs the nodejs version requested with the above curl request

- `sudo apt-get update -y` - Updates

- `npm install` - Installs the dependencies

- `npm start &` - Runs npm in the background
