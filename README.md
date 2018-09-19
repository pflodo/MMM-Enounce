# MMM-Enounce
Notification API Module for MagicMirror<sup>2</sup>

## Example

![](https://forum.magicmirror.builders/uploads/files/1473753516823-syslog-icon-4.jpg)

## Dependencies
  * An installation of [MagicMirror<sup>2</sup>](https://github.com/MichMich/MagicMirror)

## Installation
 Clone this repo:
    ````
    cd ~/MagicMirror/modules
    git clone https://github.com/pflodo/MMM-Enounce.git
    ```` 
 Configure your `~/MagicMirror/config/config.js`:

## Update

````
cd ~/MagicMirror/modules/MMM-Enounce
git pull
````

## Config Options

````
modules: [
	{
		module: 'MMM-Enounce',
		position: 'top_center', // This can be any of the regions.
		config: {
   title: "Alerts:"
			max: 5,
		},
	},
]
````
| **Option** | **Default** | **Description** |
| --- | --- | --- |
| `max` | `5` | How many messages should be displayed on the screen. |
| `format` | `false` | Displays relative date format, for absolute date format provide a string like `'DD:MM HH:mm'` [All Options](http://momentjs.com/docs/#/displaying/format/) |
| `types` | `{INFO: "dimmed", WARNING: "normal", ERROR: "bright"}` | Object with message types and their css class. |
| `shortenMessage` | `false` | After how many characters the message should be cut. Default: show all. |
| `alert` | `true` | Display notification? |

## How to Use
Make an http get request like:
  http://MIRROR_IP:MIRROR_PORT/enounce?type=INFO&message=YOUR_MESSAGE&silent=true : no notification

