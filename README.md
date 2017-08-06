# Popx - Case Study
Pay as you go, modular showrooms for small retail vendors. Similar to WeWork for retail.

The goal of this project was to identify a problem in the retail space, speak to customers, and find a solution to bring physical retail back to life. The end result was finding cheap real-estate in packed urban areas, segmented each store into blocks, and selling individual blocks at a premium.

Custodmer feedback, research, and other case study documents can be found here: [Case Study Documents](https://github.com/cgil/popx/tree/master/case_study_documents)


![PopX Demo](https://github.com/cgil/popx/blob/master/popx/static/img/popx-landingpage.png?raw=true)


## Landing Page

### Bootstrap
```
# Set up your environment
$ cd popx
$ virtualenv env
$ source env/bin/activate

$ pip install fabric  # If this is not already installed globally.
# Bootstrap dependencies
$ fab bootstrap
```

### Testing
```
# After bootstrapping
$ fab test
```

### Running locally
```
# Run a local server
fab serve
```

### Usage
* Add a new page route to `popx/__init__.py`
* Set a template for the route, the default is `home.html`
* Edit development.yaml and production.yaml with appropriate variables to include your new page

You may include mailchimp and google analytics options by manually updating the template.
You can also show/hide sections of a template by using the 'show' booleans.

Place all images in the `static/img/` folder.

### Migrations on production (Heroku)
```
# Migrate to head.
heroku db upgrade head

# Upgrade +X revisions.
heroku db upgrade +1

# Downgrade -X revisions.
heroku db downgrade -1
```

### Deploying to Heroku
```
# Deploys on push.
$ git heroku push master
```

### Future Work
More templates to come, and more dynamic pages will be added in the future.


