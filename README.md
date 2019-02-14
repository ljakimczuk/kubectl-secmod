# kubectl-secmod
The vim-based Kubectl plugin for editing secrets.

The plugin is based on the Daniel Gray's [menu.sh](https://gist.github.com/DanielFGray/ab9801481f92e19b6e87321ede56c91e).  

The plugin gets the given Secret's data, base64 decodes the selected one for a user to modify it and upon completion patch the Secret with the new value.

![](.doc/secmod.gif)

## Installation

To install the SecMod plugin, execute the following command:

```bash
sudo curl -L https://github.com/ljakimczuk/kubectl-secmod/raw/master/bin/kubectl-secmod -o /usr/local/bin/kubectl-secmod
sudo chmod a+x /usr/local/bin/kubectl-secmod
```

## Usage

In order to edit the secret pass its name and optionally a namespace to the plugin. Use `-h` option for help and examples:

```bash
Edit Kubernetes Secrets.

Examples:
  # Edit Secret in the current namespace.
  kubectl secmod secret123

  # Edit Secret in the given namespace.
  kubectl secmod -n namespace123 secret123

Usage:
  kubectl secmod
[-n <NAMESPACE> | -h]
```
