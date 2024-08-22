# kns

`kns` is a command line tool to interactively select and set Kubernetes namespaces.

```bash
~$ kns
Current namespace: default
Pick your namespace:

=> default
kube-system
my-namespace
another-namespace
exit
```

## Install
Clone the repo:

```bash
$ git clone https://github.com/roubles/kns
$ cd kns
$ pip install .
```

Copy Code

## Usage

```bash
usage: kns [-h] [--list] [substring]


interactively pick a k8s namespace


positional arguments:
substring substring to filter namespaces (must match from the beginning)


optional arguments:
-h, --help show this help message and exit
--list list namespaces instead of launching interactive menu
```

### Example

#### Selecting namespaces

To run `kns` and select a namespace interactively:

```bash
$ kns
```

To run `kns` and set the namespace directly if there is an exact match:

```
$ kns my-namespace
```

If there are multiple matches, it will show a menu to select from.

#### Listing namespaces

To list namespaces:

```bash
$ kns --list
```

To list namespaces with a filter:

```bash
$ kns --list ku
```

This will list namespaces that start with "ku".

### Features
- Interactively select a Kubernetes namespace from the terminal.
- Displays the current namespace.
- Sets the selected namespace as the current context.
- Lists namespaces with the `--list` argument.
- Filters namespaces based on a substring that must match from the beginning.

### Requirements
- Python 2.7 or later
- `kubectl` installed and configured
- `pick` library (installed automatically with `pip install kns`)

### License
This project is licensed under the Creative Commons Attribution-Noncommercial-Share Alike license.