# Ansible Role: Kitty Terminal Emulator
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit)

This role installs and customizes the Kitty terminal emulator on Debian-based Linux systems. It:
 - Ensures that Kitty is installed
 - Ensures that Kitty is configured for the specified kitty_user

See: [https://sw.kovidgoyal.net/kitty/](https://sw.kovidgoyal.net/kitty/)  
See: [https://github.com/kovidgoyal/kitty](https://github.com/kovidgoyal/kitty)

## Role Variables
See `defaults/main.yml` for a comprehensive list of role variables.  
Some of the most pertinent variables are:
- `kitty_user`  
- `kitty_font`

## Dependencies
I recommend using a Python3 virtual environment (venv).  
`python3 -m venv venv`  
`source ./venv/bin/activate`  
`python3 -m pip install -r requirements.txt`

## Testing
Testing is performed using Molecule.  
See the [molecule](./molecule/) directory for more information.

## Linting
Linting is done automatically via [https://pre-commit.com/](https://pre-commit.com/).  
After setting up a virtual environment and installing `requirements.txt`, run  
`pre-commit run --all-files`  
See: https://github.com/ansible/ansible-lint  
See: https://github.com/pre-commit/pre-commit

## Example Playbook
    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
        - librick.kitty

*Inside `vars/main.yml`*:

    kitty_user: johndoe
    kitty_font: FiraCode Nerd Font Mono

## License

MIT Licensed

## Author Information

This role was created in 2023 by [Eric McDonald](https://juniperspring.xyz/).
