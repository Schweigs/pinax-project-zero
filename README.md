# pinax-project-zero

[![Join the chat at https://gitter.im/pinax/pinax-project-zero](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/pinax/pinax-project-zero?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

This project lays the foundation for all other Pinax starter projects. It
provides the project directory layout and bootstrap-based theme.


Usage:

```
django-admin.py startproject --template=https://github.com/pinax/pinax-project-zero/zipball/master <project_name>
```

Getting Started:

```
pip install virtualenv
virtualenv mysiteenv
source mysiteenv/bin/activate
pip install Django==1.8.3
django-admin.py startproject --template=https://github.com/pinax/pinax-project-zero/zipball/master mysite
cd mysite
chmod +x manage.py
pip install -r requirements.txt
./manage.py migrate
./manage.py loaddata sites
./manage.py runserver
```

#### Modifying static assets

We rely on the Node Package Manager (`npm`), which comes with `node`. If on the
Mac, you can just `brew install node`. Otherwise, you can find [documentation](https://docs.npmjs.com/getting-started/installing-node)
on how to install it for your operating system or desired setup.

If you don't already have `webpack` setup globally on your system run:

```
npm install webpack -g
```

Now run:

```
npm install  # this will install all the dependencies in package.json
webpack      # this will build everything according to the configuration we've provided in webpack.config.js
```

#### Setting up a watcher

You can run `webpack -w` in a terminal to watch the file system and rebuild just
what is needed when you save changes. This will work for any `less` or `js`
changes.
