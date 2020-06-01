<b>I learnt Vue.js during last weekend. Develop an sample app from scratching in two days. This is not for production, just to practise and help me to learn Vue.js.<b>
<hr/>

# note-app
  
<b>Simple Note App</b> (<u>click to show/hide detail</u>) is a online Note taking app built with Vue.js + jQuery + firebase.
Data is synchronized with Google firebase powered restful database in real time.
<u>Click this sentence to hide description for more space</u>.

This app is to practise frontend tech such as JS, html and restful.
It implements features such as add/delete/update a note, change color, resize/reposition/z-index, realtime data syncing and ect.<br/>

1. On load the page, existing data will be retrieved from firebase DB and note will be displayed on screen in grid layout.
Inline-block mode is used as it works well on different device and screen size mode, hence note size and position is note saved in online db.
The status on header of a note will change to "Updated" after it is loaded from firebase db.<br/>
1. Open another (or more) browser and load the same url, observe notes rendering in both browsers.
Syncing mode can be switched-off by setting data.config.use_firebase = false.<br/>
1. Click "+" button to add a note. New added note will be uploaded to firebase db too, rendering in other browsers shall be updated too.
When syncing to db is done, the note status will changed to "Saved"<br/>
1. Click "X" on a note will delete it. Note deleting is synced with firebase db.<br/>
1. Click one of three color button on the up-right of a note will change its color. Color is synced with firebase db.<br/>
1. Type inside a note to edit its content. Note status changes to "Typing..." while editing. Content will be synced to firebase every 1 sec.
As content of a note grows, its height grows automatically to to fit text.
A confirm message will be displayed if users attempt to close/reload browser when any note is still syncing with online DB.
Since size is not shared, note rendered in other browser will appear a scrollbar.<br/>
1. A note can be resized by dragging the bottom-right corner of a note.
However, note resizing in inline-block mode would have a negative impression of the overall layout, thus a better layout design for multi-devices is needed.<br/>
1. A note can be moved by dragging its header. If two notes overlaps, click one will bring it to the front.
This is done by jQuery draggable() function. More browser compatability testing is needed to ensure using jquery with Vue.js is safe.<br>
1. Resizing and reposition is not synced with online DB, because it will cause layout issues.
Hence a better note layout design is needed, such a layout should fit most devices and different screen size.
Problem like how to display notes layout made from a large screen into mobile screen.<br/>
1. Reload the browser, all changes, except size/position, should be saved and reloaded.<br/>
1. This html app has been tested on Mac chrome, firefox, safari. Windows Edge, IE. Samsung Note 10.
Version ignored, more browser compatability testing is needed for productoin usage.<br/>
