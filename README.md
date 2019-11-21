# Fork Info
* Previously known as "com.phonegap.plugins.video" or "VideoPlayer" by Simon MacDomand (https://github.com/macdonst/VideoPlayer)
* It's possible the original was intended to assist with video playing on iOS too but as far as I remember from usage/experience this was only to get video playback working on Android PhoneGap (Cordova) apps. Kind of wish the author put the word "android" in the name/namespace to make that clear. But I thank him for building this regardless!
* Forked/updated to work with Cordova apps as of 2019112x. Basically was just needing a package.json added.
* I incremented the plugin version to 1.0.1 just make this one distinct from the original but no functionality difference (hopefully).

# Original Info 

## VideoPlayer plugin for Phonegap #

The video player allows you to display videos from your PhoneGap application.

This command fires an Intent to have your devices video player show the video.

### Adding the Plugin to your project ##

Using this plugin requires [Android PhoneGap](https://github.com/apache/incubator-cordova-android).

1. To install the plugin, move www/video to your project's www folder and include a reference to it in your html file after phonegap.js.

    &lt;script type="text/javascript" charset="utf-8" src="phonegap.js"&gt;&lt;/script&gt;<br/>
    &lt;script type="text/javascript" charset="utf-8" src="video.js"&gt;&lt;/script&gt;
    
2. Create a directory within your project called "src/com/phonegap/plugins/video" and move VideoPlayer.java into it.

3. In your res/xml/plugins.xml file add the following line:

    &lt;plugin name="VideoPlayer" value="com.phonegap.plugins.video.VideoPlayer"/&gt;

### Using the plugin ##

The plugin creates the object `window.plugins.videoPlayer`.  To use, call the play() method:

<pre>
  /**
	* Display an intent to play the video.
    *
    * @param url           The url to play
    */
  play(url)
</pre>

Sample use:

    window.plugins.videoPlayer.play("http://path.to.my/video.mp4");
    window.plugins.videoPlayer.play("file:///path/to/my/video.mp4");
    window.plugins.videoPlayer.play("file:///android_asset/www/path/to/my/video.mp4");
    window.plugins.videoPlayer.play("https://www.youtube.com/watch?v=en_sVVjWFKk");

Note: When playing video from the assets folder, the video is first copied to internal storage with MODE_WORLD_READABLE.

### All Other Info
See original repo: https://github.com/macdonst/VideoPlayer
 
