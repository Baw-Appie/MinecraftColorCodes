# MinecraftColorCodes
Minecraft has it's own Color Code system, in which they use § characters.  
This JS library I made will translate all color codes into HTML, so you can insert it in your website.  
This project is a project forked [here](https://github.com/FoxInFlame/MinecraftColorCodes).  

## Installation

## Use CDN

Just put the simple code in the ```head``` tag.
Like so:
```
<head>
<script src="https://cdn.jsdelivr.net/gh/Baw-Appie/MinecraftColorCodes/MinecraftColorCodes.js"></script>
</head>
```
You can also link the JS file at the bottom of the webpage, right before the ```body``` tag.

Now you can use it!

## Manually Install
Download this project [here](https://gitlab.com/Baw-Appie/MinecraftColorCodes/-/archive/master/MinecraftColorCodes-master.zip) as a zip file, and open the zip file.  
Place MinecraftColorCodes.js in the directory you want.  
In the webpage you have the string want to translate, link the JS file in your ``` head ``` tag.  
Like so:
```
<head>
<script src="MinecraftColorCodes.js"></script>
</head>
```
You can also link the JS file at the bottom of the webpage, right before the ```body``` tag.

Now you can use it!

## Usage
Example:
```
<script>
var yourMOTD = "§d§lnerd.nu§8: §6§oCreative Rev 28";
var newMOTD = yourMOTD.replaceColorCodes();
console.log(newMOTD);
<script>
```
Simple enough. Get your string, attach the function at the end (Don't forget the brackets, they are essential) and voila! You can then do whatever you like with it!


## Extras
You might want to get your server's MOTD, but you don't know how to access the server from your website?
Use this code! (jQuery needed)
```
$(document).ready(function(){
  $.getJSON('https://mcapi.us/server/status?ip=c.nerd.nu', function(obj){
    if(obj.online === true){
      motdHTML = obj.motd.replaceColorCodes();
      console.log(motdHTML);
    } else {
      console.log("Server is offline...");
    }
  });
})
```
https://mcapi.us provides JSON responses from the server provided in the URL. By using this, you can parse the JSON, and get your desired information! Visit http://mcapi.us for more information on the JSON format.


## Bugs / ToDo

If you find one, please submit an [issue ticket](https://gitlab.com/Baw-Appie/MinecraftColorCodes/issues) or a [merge request](https://gitlab.com/Baw-Appie/MinecraftColorCodes/merge_requests).

## Updates

v3.7 - Fixed Bug, put everything in a huge ```String.prototype``` function, so now you can't input your output element ID/Class. I mean come on, what if you just wanted to output to the console? I also changed a few tweaks here and there.

v3.8 - &f tag can be processed in black.

## Legal
You can modify this file in any way, but if you want, create a pull request so I can have a look. Also, try not sell this file/work for a price. I mean come on, if you really want money, go get a proper job. Thirdly and lastly, you can not give away this file/work without giving credit to me, and possibly giving the URL to this Github page. Due to the informality of this piece of text, you could ignore this if you want to.
