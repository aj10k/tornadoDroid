# tornadoDroid

- Never open an app store again.
- Never change settings manually again.
- Never be without key files again.
- No root required.
- No phone install requied.

![](HERE_IT_COMES.png)

## Without Device Interaction
- update/install all apps(f-droid, apkpure, local apk files)
- apply all needed settings
- push/pull files to/from device

## Usage:
- if not already: turn on adb in dev setting on phone
- `sh tornado` to use these tools sequentially, and provide options with dmenu
	- (or run each separately. The "-n" option can be used for new installs)
		- what this does
			- apps: without -n local apks are not installed
			- settings: some addational settings pushed with -n
			- files: which files to push

## Modify the Script
- apps:
	- edit the .csv for your apps
- settings:
	- edit script for your settings
		- (full list of settings)
			- `adb shell settings list system`
			- `adb shell settings list global`
			- `adb shell settings list secure`
- files:
	- edit the 'push' location (emulated/0/)
	- edit pull locations (DCIM ...)

## Dependencies
	adb
	fdroidcl
	apkeep
	dmenu

## Extra
	- check out this guide to adb: [https://github.com/wuseman/adb-shell](https://github.com/wuseman/adb-shell)
	- similar idea on pc: [https://larbs.xyz/](https://larbs.xyz/)
	- ["if your XAPK file contains a .obb file (you should see a folder named Android), then run also the following: adb push Android\obb\com.application.name /storage/emulated/0/Android/obb/ (replace com.application.name with the name of the apk you are installing)."](https://android.stackexchange.com/a/234797)
