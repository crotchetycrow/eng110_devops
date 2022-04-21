## Env variables

- `printenv ENV_NAME` - Check `env variable`
  - `env` - Same result
- `export ENV_NAME=VALUE` - Creating an env variable
  - To permanently export the environment variable, you will need to `nano .profile` and `export ENV_NAME=VALUE` at the bottom of the file. Then `exit` the VM and `vagrant ssh` back in
