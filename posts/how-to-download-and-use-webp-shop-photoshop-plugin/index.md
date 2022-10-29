---

title: How to download and use Google's WebpShop Photoshop plugin
description: A quick and detailed guide to using the Webp shop plugin in Photoshop

---

![How to use and run WebpShop in Photoshop](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/How-to-run-and-use-WebpShop-plugin-in-PhotoShop.webp)

Webp is an image format developed by Google which supports maximum compression under Google's initiative to 'make the web faster.

WebP is an image file format developed by Google and intended as a replacement for JPEG, PNG, and GIF file formats which supports both lossy and lossless compression as well as animation and transparency.

Google defines webp as:

> A modern  **image format**  that provides superior  **lossless and lossy**  compression for images on the web. Using WebP, webmasters and web developers can create smaller, richer images that make the web faster.

Google announced the WebP format on September 30 2010 and released the first stable version of its supporting library in April 2018.

Along with supporting image compression just like png, webp also supports transparency which is not possible with jpeg files.

## How to create webp images?
One of the simplest and easiest ways of converting png or jpeg files to webp is using an online file converter like CloudConvert. With CloudConvert's free version you can convert 25 files per day, which is not convenient for big website owners. While other converters show lots of ads which is frustrating.

Google released the Webp converter library which is a command line tool and is also not convenient for people without coding experience or beginners and Windows Defender keeps blocking it. 

Most people edit their images with Photoshop. It would be so great if there would be a plugin that could open webp images in Photoshop and convert normal images to webp.
Google understood this need and created a photoshop plugin to **read and write webp files**, WebpShop.

Note: The latest version of photoshop supports webp format. However, some features such as **preview at encoding and animations are missing**, stated by Google in the Readme of WebpShop's [repository](https://github.com/webmproject/WebPShop).

### How to install the Webp Shop plugin in Photoshop (on windows)

 1. Download the .8bi file from this link https://github.com/webmproject/WebPShop/releases/download/v0.4.3/WebPShop_0_4_3_Win_x64.8bi.
 2. Move the downloaded file to `C:\Program Files\Common Files\Adobe\Plug-Ins\CC`.
		![Screenshot of the location where the plugin should be kept](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/webpshop-plugin-location-screenshot.webp)
 3.  Restart photoshop. For a quick verification if the plugin is working on not, open Photoshop and click on Help > About Plug-ins > WebpShop.
![Click on the Help, located at the top.](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/click-on-help-located-at-the-top-in-photoshop.webp)
Like this: [screen recording of validating if the WebpShop plugin is working or not.](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/video-of-verifying-if-the-plugin-is-working-in-photoshop.webm).

If you can see this, the Webp Shop plugin is working and you are good to go.

If you are not able to find WebpShop in About Plug-ins, try updating your Photoshop application to the latest version.

If it is still undetected, try putting the plugin file in each of these folders (For Windows). 
```
C:\Program Files\Common Files\Adobe\Plug-Ins\CC
C:\Program Files\Common Files\Adobe\Plug-Ins\CC\File Formats
C:\Program Files\Adobe\Adobe Photoshop 2022\Plug-ins
```
Google recommends removing other plugins if there is a plugin conflict and restarting the computer. It also recommends checking [https://github.com/webmproject/WebPShop/issues](https://github.com/webmproject/WebPShop/issues) to see if it is already mentioned or to open a new bug report if not. 


## How to run and use the Webp Shop plugin in Photoshop

1. **Create an image in Photoshop** - I am editing the cover image of this article in Photoshop and I will show you how to export this Photoshop project in webp format.
![Screenshot of the "How to use and run WebpShop in Photoshop" cover in Photoshop](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/screenshot-of-the-image-in-photoshop.webp)
As you can see in the image this Photoshop project contains various image formats like png and jpeg along with text elements and clip masks. We will now convert this to webp with the help of Google's WebpShop plugin.

2. Click on the **File** option and then select **Save As**.
![Click on "Save As"](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/click-on-file-then-save-as-to-access-webp-shop-plugin.webp)

3. Select **WebpShop** as **Save as type** in the dialogue box.
![Select WebpShop option](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/click-on-webpshop-option-in-save-as-type.webp)

4.  You may see the **warning** button but you can ignore it. Click on the **Save** button.

	![Click on the save button](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/click-on-save-button.webp)

5. The WebpShop window will open.
	![WebpShop Window](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/Webpshop-window.webp)
	You can click on the **Preview** checkbox to see the image preview along with the file size which gets updated upon changing the WebpShops' settings.
	
6.  You can play with WebpShops' settings and see live changes in the preview image.
	![WebpShops' settings](https://mayankvikash.in/posts/how-to-download-and-use-webp-shop-photoshop-plugin/webpshop-settings.webp)
	The default value is 75. For the best quality, you can keep it 90-98. For best compression 20-60 is best.
7. Click on OK to finalize your selection and export your image.

There are also a few offline windows applications which you can find on the web to convert the images offline. But Google's official Photoshop plugin seems more trustworthy than those free applications and also has a great UI compared to those.

Thanks for reading. Tag [@MayankVikash1](https://twitter.com/mayankvikash1) on Twitter to share your feedback.

### References
[WebpShop Github repository](https://github.com/webmproject/WebPShop)

[WebpShop Docs](https://developers.google.com/speed/webp/docs/webpshop)

[Webp Wikipedia](https://en.wikipedia.org/wiki/WebP)

Written by Mayank Vikash.

Published on 28th October 2022.

Last updated Oct 29, 2022.
