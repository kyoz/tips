# CUSTOM 000WEBHOST ERROR PAGES

#### There are some step you have to do to custom your 000webhost error pages

#### Step 1

Navigate to your File Manger inside you control panel

#### Step 2

Create a New file called `.htaccess` inside your `public_html` folder.

#### Step 3

Insert The Following code into the .htaccess file:

```
ErrorDocument 400 <URL of Error Page>
ErrorDocument 401 <URL of Error Page>
ErrorDocument 403 <URL of Error Page>
ErrorDocument 404 <URL of Error Page>
ErrorDocument 500 <URL of Error Page>
ErrorDocument 502 <URL of Error Page>
```

#### Step 4

Change all of the `<URL of Error Page>` to the page that you want people to be sent to when an error is called back on your website.

Create all the files that you have the URL's for and test it out !

####Example

```
ErrorDocument 400 /404.html
ErrorDocument 401 /401.html
```

**NOTE**: [404.html](#) and [401.html](#) must be in your `public_html` so it can work properly.