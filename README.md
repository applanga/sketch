# Applanga Sketch Plugin

[![Applanga](https://www.applanga.com/assets/images/applanga_blue.png)](https://applanga.com)

A sketch plugin for translating sketch files with Applanga.  

## Installation

Applanga requires [Sketch](https://www.sketch.com/) v54+ to run.

- To localize a Sketch file [download](https://github.com/applanga/sketch/releases/download/v1.0.0/applanga.sketchplugin.zip) the latest release of the plugin
- Un-zip & Double-click on applanga.sketchplugin, this should create a **Applanga** sub-menu under **Plugins** in Sketch


## Configuration

- Create new project in Applanga Dashboard
- Go to `App Settings` of the project
- Add `0.0.0.0/0` in the List of IP's authorized for API upload
- Add `sketchId` as a Metadata field
- Save changes
- Go to the API section in the Applanga Project Settings and click on “Show API Token” and copy the Token
- Make sure the source language of the Sketch file (e.g. English) does exist on the Applanga dashboard
- Open Sketch and in the Menu Bar, go to Plugins > Applanga > Configure API Token and input the Applanga API Token


## Plugin Commands

1. Upload strings
    * All _(upload strings of the whole sketch file)_
    * Current Page _(upload strings of the current page from the sketch file)_
2. Upload Screenshots
    * All _(upload all artboards)_
    * Current Page _(upload artboards of the current page)_
3. Download From Applanga
    * Target _(download strings translated as target values)_
    * Draft[1] _(download strings translated strings as draft values)_
4. Update Api Token _(copy the API Token from your App settings)_

[1]: if the draft value doesn't exist, the target value will be taken

#### Exclude from Upload

If you want to skip text elements from uploading to Applanga, prefix them with three underscores (___).


## Usage

**How to upload Sketch content for translation?** 

After you installed the Applanga Sketch Plugin and set up the Applanga Sketch integration as described in the Configuration section, open the Sketch file you want to translate. 

Start by uploading the translatable text content. In the Menu Bar under Plugins > Applanga choose Upload Strings. You can either upload all pages or only the currently selected one. 

After you made you chose the upload option form the Plugin menu, a pop-up will appear to ask you to select a source language (the current language of the file). The upload might take a moment. There will be a pop-up to confirm when the upload is done.  

The Applanga Sketch plugin can also upload the pages in the sketch file itself as a visual reference for the translation process to Applanga. For this feature, use the Upload Screenshots option from the plugin menu. 


**How to generate translated Sketch files?**

Once translations are available for your Sketch content on Applanga, you can use the plugin to generate a translated versions of your file. 

From the plugin menu, choose Download from Applanga. You will need to decide to either use the Draft version of the string or the Target version. 

In the pop-up that appears after that, select the language you want to download. When saving the file, using the .sketch ending in the file name is mandatory. 


