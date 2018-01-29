# REMOVE 000WEBHOST BANNER

#### To remove 000webhost banner. Just add this script to your [index.html](#) file. ( Must be before your other scripts :laughing: )

```js
<!-- Remove 000webhost banner -->
  <script type="text/javascript">
    window.onload = function() {
      var a_tag = document.querySelector('a[title="Hosted on free web hosting 000webhost.com. Host your own website for FREE."]');
      var banner = a_tag.parentNode;
      banner.remove();
    }
  </script>
<!-- End remove 000webhost banner -->

```