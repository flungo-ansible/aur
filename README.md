# AUR Ansible role

Ansible role for AUR. Installs pacaur onto a machine to be used with the [cdown/ansible-aur](https://github.com/cdown/ansible-aur) module.

If `pacaur` is already installed it will update via the `aur` module otherwise it will manually install with `git` and `makepkg`.

## Testing

Testing can be performed using the Dockerfile included. To perform the test, build the image with `docker build .`. If the build is successful then the role works on an archlinux machine that does not already have pacman installed and the image built will have `pacaur` installed.

## Usage

This role should be included as part of your own playbook but it can be run independently using the test playbook. You will be required to have the [cdown/ansible-aur](https://github.com/cdown/ansible-aur) module installed on your system or as part of your playbook.

To run the ansible role locally, you can execute the testing playbook by running `ansible-playbook --ask-sudo-pass test/main.yml`.
