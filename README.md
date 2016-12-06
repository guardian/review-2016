A collection of header graphics and a page enhancer used on 2016 review pages
============================================================================== 


The header graphicfiles are located in 
------------------------------------------
review-2016/src/js/text/review-ukfilm.html

review-2016/src/js/text/review-usfilm.html

review-2016/src/js/text/review-music.html

review-2016/src/js/text/review-tv.html



Here are working examples 
---------------------------------

https://www.theguardian.com/film/2016/nov/29/the-50-best-uk-films-of-2016-full-list

https://www.theguardian.com/film/2016/nov/29/50-best-us-film-of-2016-the-full-list

https://www.theguardian.com/music/2016/nov/30/the-best-albums-of-2016




Page Enhancer
---------------------------------
Using the ES6 template instructions below will generate a boot.js to embed in a composer page. Edit the css (review-2016/src/css/main.css) to update styles in the composer page. 




Guardian interactive ES6 template
=================================

An interactive template & test harness, set up with commonly used components and example code

Usage
=====

Setup
-----
`npm install`

Development
-----------
`npm start`

Production / deployment
-----------------------

1. Update `cfg/s3.json`
2. `grunt deploy`

NOTE: Ensure you have AWS credentials setup by either adding them to your `~/.bashrc` or
creating a `~/.aws/credentials` file with the following content:

```
[default]
aws_access_key_id = <YOUR_ACCESS_KEY_ID>
aws_secret_access_key = <YOUR_SECRET_ACCESS_KEY>
```


Using third party js
--------------------
1. Install package using JSPM e.g.

	`jspm install reqwest` or

	`jspm install github:guardian/iframe-messenger`

2. Import package. e.g.

	`import reqwest from 'reqwest'` or

	`import reqwest from 'guardian/iframe-messenger'`

Text/JSON in javascript
-----------------------
```
import someHTML from './text/template.html!text'
import someJSON from './data/data.json!json'
```

Test Harness
============

`index.html` - Stripped down test harness. Includes frontend fonts and curl for loading boot.js.
`immersive.html` - Immersive-style interactive page pulled from theguardian.com
