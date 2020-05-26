# Applanga Sketch Plugin

[![Applanga](https://www.applanga.com/assets/images/applanga_blue.png)](https://applanga.com)

A sketch plugin for translating sketch files with Applanga.  

## Installation

Applanga requires [Sketch](https://www.sketch.com/) v54+ to run.

- To localize a Sketch file [download](https://github.com/applanga/sketch/releases/download/v1.0.1/applanga.sketchplugin.zip) the latest release of the plugin
- Un-zip & Double-click on applanga.sketchplugin, this should create a **Applanga** sub-menu under **Plugins** in Sketch


## Configuration

- Create new project in Applanga Dashboard
- Go to `App Settings` of the project
- Add `::/0` in the List of IP's authorized for API upload
- Add `sketchId` as a Metadata field
- Save changes

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