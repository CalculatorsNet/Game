# How to use ruffle on github pages

1. Download ruffle from [ruffle(https://github.com/ruffle-rs/ruffle/releases/download/nightly-2025-02-24/ruffle-nightly-2025_02_24-web-selfhosted.zip)]

2. Extract the file

3. Upload entire ruffle folder to github repo containing swf file

4. Copy the following code into an index.html file:
```
<!DOCTYPE html>
      <html lang="en-us">
      <head>
        <meta charset="utf-8">
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
        <title>Stick Cricket</title>
        <style>
          body {
          margin: 0px;
          padding: 0px;
          overflow: hidden;
        }
        </style>
        <meta name="description" content="Stick Cricket">
        <meta property="og:image" content="stickcricket.png" />
      </head>
      
      <body>
        <div class="webgl-content">
          <div id="gameContainer" style="width: 100vw; height: 100vh">
            <script src="patch/ruffle.js"></script>
            <script>
              window.RufflePlayer = window.RufflePlayer || {};
              window.RufflePlayer.config = {
                  warnOnUnsupportedContent: false,
                  autoplay: "on",
                  unmuteOverlay: "hidden",
                  maxExecutionDuration: 30,
                  base: null,
                  forceScale: false,
                  quality: 'high'
              };
            </script>
            <div id="gamefilearea" class="prestitial-running" style="height:100%;">
      
            <object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" codebase="http://fpdownload.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=8,0,0,0" width="900" height="600" id="gamefile" align="middle">
            <param name="allowScriptAccess" value="always" />
            <param name="movie" value="stick-cricket.swf" />
            <param name="quality" value="high" />
            <param name="wmode" value="window" />
            <param name="allowfullscreen" value="false" />
            <param name="allowfullscreeninteractive" value="false" />
            <param name="fullScreenAspectRatio" value="" />
            <param name="quality" value="high" />
            <param name="play" value="true" />
            <param name="loop" value="true" />
            <param name="menu" value="" />
            <param name="flashvars" value="gameID=13824" />
            <param name="hasPriority" value="true" />
      
            <embed src="stick-cricket.swf" width="100%" height="100%" id="gamefileEmbed" name="gamefile" align="middle" wmode="window" allowfullscreen="false" allowfullscreeninteractive="false" fullScreenAspectRatio="" quality="high" play="true" loop="true" menu="" allowScriptAccess="always" flashvars="gameID=13824" hasPriority="true" type="application/x-shockwave-flash" pluginspage="http://www.adobe.com/go/getflashplayer"></embed>
            </object>
      
          </div>
        </div>
          <script src="js/analytics_ubg_v1_4.js"></script>
          <script src="js/ubg235_client_v1_2.js"></script>
      
      </body>
      </html>
```

5. Modify the `stick-cricket.swf` to whatever the name of the flash file that you have

6. Modify `patch/ruffle.js` to whatever the location of your `ruffle.js` file is

7. Modify the title and the image to whatever your game is

8. Use github pages to host
