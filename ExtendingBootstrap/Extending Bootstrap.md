# Extending Bootstrap

Install bootstrap with npm

	npm install bootstrap@3

[Free bootstrap themes @ bootswatch](http://bootswatch.com/paper/)

[w3schools theme tutorial](http://www.w3schools.com/bootstrap/bootstrap_theme_me.asp)
[Cool w3schools Band theme tutorial](http://www.w3schools.com/bootstrap/bootstrap_theme_band.asp)
[Bootstrap live customizer](http://bootstrap-live-customizer.com/)
3 years old text[How To Make A Bootstrap 3 Theme The Proper Way](http://antjanus.com/blog/uncategorized/make-bootstrap-3-theme-proper-way/)
## 4. LESS

Recess is a LESS compiler

	npm install -g recess

Create \ExtendingBootstrap\less\styles.less

    @font-family: Arial;
    @text-color: red;
    body {
    font-family: @font-family;
    color: @text-color;
    }

Compile less to css

	recess styles.less --compile > styles.css

OR

    recess styles.less --compress > styles.min.css

Read how to setup [File watcher](https://www.jetbrains.com/help/webstorm/2016.2/new-watcher-dialog.html)

## Compiling CSS and JavaScript

From book:

    C:\webStormWS\ExtendingBootstrap>recess less/main.less --compile > css/main.css
    > produce empty main.css


Bootstrap uses Grunt for its build system, with convenient methods for working with the framework. It's how we compile our code, run tests, and more
[Compiling CSS and JavaScript](http://getbootstrap.com/getting-started/#grunt)
Follow instructio as is.
change index.html to point new bootstrap

<link href=".\bootstrap-3.3.7\dist\css\bootstrap.css" rel="stylesheet">

To run Grunt
    C:\webStormWS\ExtendingBootstrap\bootstrap-3.3.7>grunt dist

- Save index.html as index-2.html

    add C:\webStormWS\ExtendingBootstrap\bootstrap-3.3.7\less\canon-variables.less
    with @brand-color: #bada55;

- 

    add C:\webStormWS\ExtendingBootstrap\bootstrap-3.3.7\less\canon-theme.less
    with .container .jumbotron {
         border-radius: 0;
         }.
         .label {
         border-radius: 0;
         }

add canon-theme.less canon-variables.less to bootstrap-3.3.7\less\bootstrap.less
cause page rendering Error
    //@import "canon-theme.less";
    @import "canon-variables.less";


## TODOs

- install bootstrap and recess locally

