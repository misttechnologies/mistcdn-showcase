# MistCDN showcase

MistCDN enables low-cost, scalable delivery of your contents. Signup form here.  https://console.mistcdn.com

This repository shows examples of MistCDN Applications. We welcome your pull requests.

## VOD Simple


### Step1: Include the MistCDN Javascript file in your page.

You need to include MistCDN main script in your page
in order to deliver contents via MistCDN.
Place the row below in the &lt;head&gt; tag of your page.

```html
<script src="//dist.mistcdn.com/mistcdn.min.js"></script>
```

### Step2: Include the Video.js Javascript, CSS and plugin files

In order to play videos with Video.js, some javascript and CSS files have to be loaded.
Two are for the Video.js main component, and the other is for Video.js plugins.
Add few lines below in the &lt;head&gt; tag of your page.

```html
<link href="//vjs.zencdn.net/4.12/video-js.css" rel="stylesheet">
<script src="//vjs.zencdn.net/4.12/video.js"></script>
<script src="//dist.mistcdn.com/videojs-contrib/videojs.misthls.min.js"></script>
```


### Step3: Add an HTML5 &lt;video&gt; tag to your page.

Place the &lt;video&gt; tag below at the appropriate location on your &lt;body&gt; tag.
A video player will be embedded there when viewed by end-user.

```html
<video  id="example_video_1" class="video-js vjs-default-skin"
        width="1280" height="720" controls
        data-setup='{}'>
    <source src="https://example.net/path/to/playlist.m3u8"
            type="application/x-mpegURL">
</video>
```

#### Option

If data-setup attribute of &lt;video&gt; tag is omitted, the auto setup process will not be
executed. In such a case you have to initialize the player on your own.

```javascript
<script type="text/javascript">
    videojs('example_video_1');
</script>
```

#### Tips about Video.js setup

Default options object for video.js auto setup is shown below.

```javascript
{
    "techOrder": ["hls", "html5", "flash"],
    "flash": {
        "swf": "//vjs.zencdn.net/4.12/video-js.swf"
    },
    "width": 300, // width of video player
    "height": 150 // height of video player
}
```

!!!Notice!!!: Auto setup options which are passed to data-setup attribute of
&lt;video&gt; tag have to be strict JSON format; all the keys and strings must be
embraced by double quotations.


## Video	Live

Coming soon

## Images (jpg, png, gif...)	

Coming soon. MistCDN supports Lazy Loading

## Downloader

Coming soon. 
