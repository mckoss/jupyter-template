# Jupyter Notebook Template

This repl solves a number of problems in running Jupyter notebooks "as is"
from replit.com.

- Serving to the (default) SSL port.
- Allowing access from a remote client (normally just serves to the local machine).
- Setting a password to allow access without using a randomly generated token.
- Putting all notebooks in their own directory.

# Getting started

Start by forking [this template](https://replit.com/@mckoss/jupyter-template)
on replit.com.

When you first run this repl, you should be prompted for a password
in the Console window.  This will only happen the first time you run it.

Once started, visit the web address for your repl in a browser:

```
https://YOUR-REPL-NAME.YOUR-USERNAME.repl.co
```

# Changing your password

If you want to change your user password enter the following into the Shell
window:

```
$ jupyter notebook password
```

and you will be prompted for a new password (you may have to Stop and re-Run the
repl for the change to take effect).

# Behind the Scenes

Configuration and password files are stored outside the repl directory itself (they
are in `$HOME/.jupyter`).  So they have to be generated when this repl server is
created (or forked).

This server is started from a small bash script, `run-server` which takes care
of creating an initial password and defaulting to a notebooks directory.
