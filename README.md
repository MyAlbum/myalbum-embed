# myalbum-embed
Our [Wordpress plugin](https://myalbum.com/wordpress) offers you a full embed of your album without any MyAlbum branding (when used in combination with our [business account](https://myalbum.com/business)). If you don't use Wordpress you can still use this functionality by integrating the following code into your site:


```html
<div id="holder"></div>

<script>
// ENTER THE LANGUAGE OF PREFERENCE ("nl", "en", "de", "fr" or "es")
var langCode = "nl";

// ENTER THE ALBUM KEY HERE
var albumKey = "cc0cRaWhajJ2";

// ENTER DOM ELEMENT ID
var domId = "holder";


// NO NEED TO EDIT BELOW THIS LINE
var s = document.createElement("script");
s.src = "https://myalbum.com/res/package/js/api-album.js?hl="+langCode;
s.async = true;
document.body.appendChild(s);
// This function will perform once the MyAlbum API has been loaded
function initMyAlbum()
{
  var album = new myalbum.album.Create(domId);
  album.load(albumKey);
}
</script>
```
