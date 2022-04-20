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

- `vagrant reload`

- Run localhost
