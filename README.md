# OpenSkinJS *for Framework7*
![](https://raw.githubusercontent.com/Shugabuga/OpenSkinJS/master/OpenSkin.png)

*OpenSkin: The Flexible and Open Skin Format*

## Introduction

OpenSkin is a proposed file format based off of the JSON syntax that will ([try to](https://xkcd.com/927/)) make a standardized format for application theming. It is based off of the skin format of web-based GameBoy Advance emulator [iGBA (now Eclipse)](https://eclipseemu.me), but expanded to be used for non-emulators and to enrich the capabilities of their theming system, as it was quite limited in its standard state.

## The Library

OpenSkinJS is a library designed for developers to easily take advantage of OpenSkin-formatted skins with little effort, especially for [Framework7](http://framework7.io)-based web applications. It will take the skin file (as an object, JSON string, or a remote file (given it doesn't violate cross-site restrictions)) and allow for it to be loaded into the DOM, as well as the ability to work with the skin's metadata (like name and description).

## Setup

To set up OpenSkin in your project, add the following towards the end of the page (to make sure any dependencies are loaded and to reduce page load time):

```html
<!-- OpenSkin -->
<script>var openskin = "appName"</script>
<script src="openskin.min.js"></script>
<!-- /OpenSkin -->
```

Make sure to replace `appName` with your web app's name. This is used for skin developers to fine-tune their skins for your site (if needed).

## Skin Designers

If you are a skin designer, use `example.json` to assist in making new skins. Please refer to the specific application for properties that might be used for said application, on top of the defaults.

## Usage

### Fetching the Skin

`OpenSkin.getJSON(url, loadAfter)`: Loads a skin from a given `url` (most browsers require that files have to be loaded from the same domain for security purposes)

`OpenSkin.getStr(json, loadAfter)`: Takes a string of JSON (passed as `json`) and loads it

`OpenSkin.getObj(object, loadAfter)`: Takes an already-parsed object and loads it

### Applying the Skin

`OpenSkin.load()`: Applies the skin.

The `loadAfter` boolean in the fetch methods, when set to true, will apply the skin after the skin is loaded.

### Skin API

The `OpenSkin.skin()` function will return an object that allows for the access of the currently loaded skin, including its name, properties, and styles.

## Reporting Bugs

### Vulnerabilities (i.e. XSS)

Please contact [HeyItsShuga](https://twitter.com/HeyItsShuga) immediately.

### Everything Else

Please use the Issues tab to report any bugs that don't compromise security.
