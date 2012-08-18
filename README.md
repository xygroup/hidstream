# HIDSTREAM 
__Streaming HID Events in Node.js__


----------

### Example:

`
var hid = require('hidstream');
var dev = new hid.device('0001:001:00');

dev.on("data", function(dat) {

	console.log(dat); // easily consumed data format!
});
`

### Sample HID Data Packet:

__The user has pressed Ctrl + Alt + Del__
`
{
	modKeys : [
		, 'ctrl'
		, 'alt'
	]
	, keyCodes : [
		76
	]
	, keyChars : [] // not yet implemented
	, errorStatus : false
}
`