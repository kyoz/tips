# USE SINGLE PAGE APPLICATION IN GITLAB/GITHUB PAGES

#### There are two things you must do to make your [Gitlab/Github Pages]() work properly

#### 1. Create the [404.html](#) file with those below contents:

- Note that if you are setting up a Project Pages site and not using a [custom domain](#) (i.e. your site's address is [username.gitlab.io/repo-name](#)), then you need to set [`segmentCount`](#) to [`1`](#) in the [404.html](#) file in order to keep [/repo-name](#) in the path after the redirect.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Single Page Apps for GitLab/GitHub Pages</title>
    <script type="text/javascript">
      var segmentCount = 0;
      var l = window.location;
      l.replace(
        l.protocol + '//' + l.hostname + (l.port ? ':' + l.port : '') +
        l.pathname.split('/').slice(0, 1 + segmentCount).join('/') + '/?p=/' +
        l.pathname.slice(1).split('/').slice(segmentCount).join('/').replace(/&/g, '~and~') +
        (l.search ? '&q=' + l.search.slice(1).replace(/&/g, '~and~') : '') +
        l.hash
      );
    </script>
  </head>
  <body>
  </body>
</html>
```
  
#### 2. Copy those below script to your [index.html](#) file

- Note that the redirect script must be placed *before* your single page app script in your [index.html](#) file
&nbsp;

```javascript
<!-- Start Single Page Apps for Gitlab/GitHub Pages -->
  <script type="text/javascript">
    (function(l) {
      if (l.search) {
        var q = {};
          l.search.slice(1).split('&').forEach(function(v) {
            var a = v.split('=');
            q[a[0]] = a.slice(1).join('=').replace(/~and~/g, '&');
          });
          if (q.p !== undefined) {
            window.history.replaceState(null, null,
              l.pathname.slice(0, -1) + (q.p || '') +
              (q.q ? ('?' + q.q) : '') +
              l.hash
          );
        }
      }
    }(window.location))
  </script>
<!-- End Single Page Apps for GitLab/GitHub Pages -->
```
  

