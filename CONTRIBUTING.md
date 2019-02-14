# Contributing

By participating to this project, you agree to abide our [code of conduct](/CODE_OF_CONDUCT.md).

## Setup your machine

Prerequisites:

* [Python](https://www.python.org)
* [Ansible](https://ansible.com/)
* [Docker](https://docker.com)

Clone `ansible-role-consul` from source into your favorite path:
```sh
$ git clone git@github.com:fabiorphp/ansible-role-consul.git
$ cd ansible-role-consul
```

Install Python dependencies (Please use the Python Virtualenv):
```sh
$ pip install -r requirements.txt
```

## Running tests
After the installation of python dependencies run the command below:
```sh
$ molecule test
```

## Create a commit

Commit messages should be well formatted.

After a colon, you should give the message a title, starting with uppercase and ending without a dot.
Keep the width of the text at 72 chars.
The title must be followed with a newline, then a more detailed description.

Please reference any GitHub issues on the last line of the commit message (e.g. `See #123`, `Closes #123`, `Fixes #123`).

An example:

```
Add example for --release-notes flag

I added an example to the docs of the `--release-notes` flag to make
the usage more clear.  The example is an realistic use case and might
help others to generate their own changelog.

See #284
```

## Submit a pull request

Push your branch to your `ansible-role-consul` fork and open a pull request against the master branch.
