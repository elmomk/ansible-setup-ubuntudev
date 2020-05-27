# Setup Ubuntu development environment

This is my first ansible playbook to configure a development workstation based on Ubuntu 20.04. It is not very elegant but it is functional.

## Prerequisites

The only prerequisites are : 

* Ubuntu 20.04 installed
* ansible installed: ansible version 2.9.6 is part of the standard repo of Ubuntu 20.04. Installation is straightforward. Run the following commands in a terminal : `sudo apt update && sudo apt install -y ansible && sudo apt install -y git`

> The commands are also available in a gist available here : [setup-ansible.sh](https://gist.github.com/pondichys/b4b7c1e17d22ae2d6f2d1c91611707f8)

## Running the playbook

Clone this repository.

Adapt the user variable if needed (or pass it through `-e` argument).

Run the playbook with `-K` option to supply the `sudo` password.

```bash
ansible-playbook playbook-setup-ubuntudev -K
```

## Packages installed

The following packages are installed by this playbook:

* git (just to be sure ;) )
* [Visual Studio Code](https://code.visualstudio.com/)
* [azure-cli](https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest)
> Remark: at this time (2020-05-20) there is no packages available of azure-cli for Ubuntu 20.04. We use the package from 18.04 as a workaround ...
* [virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/)
* [python3-venv](https://docs.python.org/3/library/venv.html) for Azure Functions project creation in VSCode
* [powerline go](https://github.com/justjanne/powerline-go)
