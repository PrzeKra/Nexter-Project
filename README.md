# Nexter-Project

Master CSS Grid Layouts Udemy Course


The content is a bit old so if you have a newer version of SASS it recommends you uninstall yours and reinstall the old things.

If you don't want to do that but want to work with the latest versions available:

1) Download the starter files as is and delete package.json

2) npm init [enter and change names until done].

Now you have a fresh package.json file.

3) npm install node-sass --save-dev

4) npm install auto-prefixer live-server npm-run-all postcss-cli concat



Now you have all packages that Jonas uses and live-server won't give issues since you explicitly installed it



After they've installed you can manually add these scripts that he uses into package.json



"scripts": { "watch:sass": "node-sass sass/main.scss css/style.css -w", "devserver": "live-server --browser=firefox",
"start": "npm-run-all --parallel devserver watch:sass",
"compile:sass": "node-sass sass/main.scss css/style.comp.css", "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.comp.css -o css/style.prefix.css",
"compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
"build:css": "npm-run-all compile:sass prefix:css compress:css" }
