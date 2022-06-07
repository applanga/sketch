# Applanga Sketch Plugin

[<img src="https://www.applanga.com/assets/images/applanga_blue.png" style="max-width: 344px;">](https://applanga.com)


A Sketch plugin for translating Sketch files with Applanga.  

## Table of Contents

  1. [Installation in Sketch app](#installation-in-sketch-app)
  2. [Configuration of the Applanga Project and Plugin](#configuration-of-the-applanga-project-and-plugin)
  3. [Usage](#usage)
     1. [Connection Settings](#connection-settings)
	 2. [Uploading content for translation](#uploading-content-for-translation)
	 3. [Translate your Sketch file](#translate-your-sketch-file)
	 4. [Uploading translated screenshots](#uploading-translated-screenshots)
	 5. [Uploading translated screenshots for multiple languages](#uploading-translated-screenshots-for-multiple-languages-at-once)
	 5. [Inspect & Edit Ids](#inspect-and-edit-ids)
	 6. [Check and Align file](#check-and-align-file)


## Installation in Sketch app

Applanga requires [Sketch](https://www.sketch.com/) v54+ to run.

1. To localize a Sketch file [download](https://github.com/applanga/sketch/releases/latest/download/applanga.sketchplugin.zip) the latest release of the plugin
2. Unzip & Double-click on applanga.sketchplugin, this should create a **Applanga** sub-menu under **Plugins** in Sketch


## Configuration of the Applanga Project and Plugin

**For a new project**

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch3a.png" style="max-width: 344px;">
<br />

1. Create a new project in Applanga Dashboard.
2. Follow the prompts and select the Sketch integration option.
3. Copy the Applanga API Token by clicking on the clipboard icon. You will need it to start using the plugin.  
4. Click on "Go to Project" to confirm the configuration (and whitelisted IPs)

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch3b.png" style="max-width: 344px;">
<br />


**For an already existing project**

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch3.png" style="max-width: 344px;">
<br />

1. Go to `Project Settings` of the project.
2. Add `::/0` and `0.0.0.0/0` or the authorised IP addresses in the List of IP's authorised for API upload.
3.  *(Optional)* Copy the Applanga API Token by clicking on "Show API key" and then the clipboard icon. You will need it to start using the plugin.
4. Save changes.

<br />

**In the Applanga Plugin**

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch02.png" style="max-width: 344px;">
<br />

1. If the design file is not yet connected to an Applanga project, the plugin will open on the [*Connection Settings*](#connection-settings) page
1. Enter the Applanga Project API Token
1. Confirm the Applanga Project Name is correct
1. Click *Save Settings*

<br />

[Back to Top](#table-of-contents)

<br />


## Usage

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch01.png" style="max-width: 344px;">
<p>&nbsp;</p>

### Connection Settings


<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch02.png" style="max-width: 344px;">

1. *Applanga Project API Token*: please copy the API Token from your Applanga Project Settings page
2. *Applanga Project Name* corresponds to the entered API token (not editable)
3. *Save Options*: saves the Connection Settings on your local machine. The selected options are saved separately for each Sketch file and will be loaded next time you open the file on your machine and start the plugin.


<br />

[Back to Top](#table-of-contents)

<br />

### Uploading content for translation


<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch03.png" style="max-width: 344px;">

**Upload Options**

* *Project Name*: this is set to the Applanga project which the plugin is currently linked via the API token (not editable)
* *Select Language*: the source language is preselected by default, but you can select any language for upload
* *Upload Scope*
	+ *All Content*: All content from the design file is included in the scope of the upload
	+ *Only Current Page*: Only content from the current page is included in the scope of the upload
	+ *Only Selected Content*: Only the content from the selection is included in the scope of the upload
* *Include Text* and *Include Screenshots*: select what should be included in the upload to your Applanga project (by default both options are selected for source language, and only the Screenshots option is selected for target language uploads)
* *Advanced Upload Options:*
	+ *Upload new/missing text*: with this option enabled, any text present in the file and not yet on Applanga is uploaded (by default enabled)
	+ *Merge new duplicated text into a single Applanga string*: when this option is enabled during upload, for every text that is not on  Applanga yet, all duplicates found in the file for that text are 'merged' into a single new Applanga string Id. If this option is disabled, one string Id is created for each of the duplicate texts (by default enabled)
	+ *Set status*: this option sets a status for all new content uploaded to an Applanga project. To update the status of an already existing string on Applanga, use the *Change status* option
	+ *Merge Sketch text with existing Applanga strings*: when this option is enabled during upload, if a entry with the exact same text already exists, the corresponding string Id is applied to the Sketch file instead of generating a new one. If multiple such matching entries exist, one is chosen randomly (by default enabled)
	+ *Update existing Applanga strings with changes made in Sketch file*: when this option is selected, the corresponding entries on Applanga will be overwritten with the content from the Sketch file (by default enabled)
	+ *Change status*: this option changes the status of an already existing string on Applanga. 
	+ *Exclude untranslatable content*: this option will exclude specific types of untranslatable content from upload to the Applanga project. Options for exclusion from upload include only numbers, times and dates, special characters,Lorem ipsum placeholder text, symbols, or single characters.
	+ *Include Screenshots without Linked Text*: if selected, screenshots that couldn't be linked to any text are uploaded to the Applanga project (by default disabled)
	+ *Include Hidden Content*: determines if the hidden (close/open eye icon) content is included in translation scope (by default disabled).
Please note, that there may be invisible elements that will be included in scope, because they are invisible for other reasons than the “visible” property status.
	+ *Include Locked Content*: determines if the locked (padlock icon) content is included in translation scope (by default disabled)
<p>&nbsp;</p>

**Important notes!**  

* If you want to exclude pages or other elements from the upload, add 3 underscores in front of the element or page name (___).
* The upload for large files, particularly when screenshot upload is included, may take several minutes.

The **Upload** button is only active if there is an upload language selected and either the Text or Screenshots option is selected. The Activity log will display the progress indication and error messages.

<br />

[Back to Top](#table-of-contents)

<br />

**Renaming String IDs**  
When new IDs are being created on Applanga as part of the upload, there is the option to manually edit any of those new IDs. The dialog will not display if only screenshots are being uploaded or there are no new strings to upload.

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch04.png" style="max-width: 344px;">

* Click on the source text, to expand it and display the full text
* Click on the suggested string ID name to edit it
* Click *Confirm* to approve the edits. You can also *unconfirm* to restore the original ID name. If the *Confirm* button becomes red, the string ID name is invalid. Most often its a value conflict (the same ID name, but different source text) with an ID that already exists in Applanga or is a duplicate to a newly created ID name. Hover over the button to see a more detailed error message.
* *Only Approved* or *All* (default) determines if all of the texts are to be uploaded to Applanga or only confirmed ones(green checkbox). If any edits are made to the string IDs, only those approved will be included in the upload. 

The **Upload** button starts the upload immediately. During the upload process, an activity log will inform you about the progress and any errors.

<br />

[Back to Top](#table-of-contents)

<br />

### Translate your Sketch file

Once translations for your content are available on Applanga, you can use the plugin to download the translations and populate them in your file. 

You may prevent any part of your file from being translated by locking or hiding the elements out of scope and/or by limiting the download to specific pages (see *Scope* below)

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch08.png" style="max-width: 344px;">

**Download Options**

* *Project Name* is set to the connected Applanga project via the API token (not editable)
* *Select Language*: selects the target language to be downloaded. Please note that the *Download* button will not be active until a target language is picked (none is selected by default)
* *Mode* determines if target translation values or draft translation values are downloaded and populate (by default Target plus Draft will be populated)
* *Scope* determines if the whole file is processed or only the currently open page (by default all content is in scope)
* *Overwrite Hidden Content* determines if the hidden (close/open eye icon) content is included in scope (by default excluded)
* *Overwrite Locked Content* determines if the locked (padlock icon) content is included in scope (by default excluded)
* *Merge Sketch text with existing Applanga strings* allows the linking of text in Sketch missing Applanga Ids to an existing Applanga string Id in the connected Applanga project. Please note, the text matching to the source text in Applanga project may not work or may give false positives if the file is (partially) translated.

**Important notes!** 

* Please be aware that translation download for very large files may take several minutes.
* Note that any content that has 3 underscore characters (___) at the beginning of the element or page name is excluded from the scope.
* The translation download will overwrite the source text in your file. It is recommended to create a copy of the file for the translation process. You can also revert back to your starting point by selecting your source language and downloading it again.
* It may take up to 10 minutes before changes made to translations on the Applanga dashboard are available for download.


The **Download** button starts the download immediately. The button is only active if there is a download language selected. During the download process, an activity log will inform you about the progress and any errors. 

<br />

[Back to Top](#table-of-contents)

<br />

### Uploading translated screenshots

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch05.png" style="max-width: 344px;">


If you want to upload screenshots of your translated Sketch file back to Applanga, for example, if you want somebody to review the translation in-context, please follow these steps:  

1. Go to *Download* and select a language, run the download process.
2. After the download is finished, go to *Upload* and select the language again but make sure that you only select *Screenshots* in the *upload* options


<br />

[Back to Top](#table-of-contents)

<br />

### Uploading Translated Screenshots for multiple languages at once

The *Batch Screenshot Upload* option can be used to start an automated process that will, step by step, download translations for a language, take screenshots of the translated Sketch design, and upload the translated screenshots back to Applanga for all languages selected one after the other automatically.

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch06.png" style="max-width: 344px;">

In order to upload translated screenshots for multiple languages at once, in the plugin UI, choose the *Batch Screenshot Upload* option. In the subsection of the *Batch* option, you can select which languages to include (all or everything but source), which set of strings (*Draft or Target*), and which layers (all or only the currently selected one) will be in scope for the batch process.


<br />

[Back to Top](#table-of-contents)

<br />

### Inspect & Edit Ids

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch_inspectIds.png" style="max-width: 344px;">

Inspect & Edit Ids allows users to view the Applanga string Ids connected to specific text in the respective design file. Users can also create new strings Ids by removing the current Id and setting a new one via the plugin.


1. Select the element of the design file to display string Ids in the plugin
1. Click on the *String Id* text field to edit the string Id, then select the checkmark to approve for upload (if an Id already exists for a given text on Applanga, users can search and apply that specific Id)
1. Once Ids are updated, click *Upload*

**Important Notes!**

* Due to a 10-minute CDN delay, recently uploaded or changed string Ids may not display in the plugin and return a message of “No Id set yet.” Please allow 10 minutes for the cache to update and try again.
* Screenshots are not automatically uploaded with strings when using the *Inspect & Edit Ids* option. Users can manually assign strings on the Applanga dashboard using the screens tag. See the [tags]({{site.baseurl}}docs/translation-management-dashboard/applanga-tags) page for more info.


<br />

[Back to Top](#table-of-contents)

<br />

### Check & Align File

<img src="https://www.applanga.com/assets/images/docu/integration-documentation/sketch07.png" style="max-width: 344px;">

**Check/Fix File Options**

* *Link Sketch text with existing Applanga IDs*: this option tries to match the text in the file with existing Applanga IDs. It's similar to Merge Sketch text with existing Applanga strings in download options, but is not limited to selections.
* *Remove all linking to Applanga IDs*: this option allows users to unlink Applanga string IDs from a previously uploaded  Sketch file. When users upload a previously Applanga-integrated file to a new project, the existing Applanaga IDs can cause issues with the upload to the new project. This option prevents issues with both uploading and downloading content from Applanga. 
* *Migrate IDs to new plugin version*: Applanga plugin update from version 1.* to 2.* changed how string IDs are stored; this option will migrate this string Id storage method if you have previously uploaded the same Sketch project with the Version 1.* plugin. This migration will **not** happen automatically during the upload or download process. 

<br />

[Back to Top](#table-of-contents)
