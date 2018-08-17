# VMware-fusion
This is a solution to solve VMware fusion cannot find a valid peer process to connect

## Method 1
* Open System Preferences by searching in Spotlight or clicking the gear icon in the dock.
* On the top row there is an icon for Security and Privacy - Click that icon
* Near the bottom of the screen that appears following statement

if you did not get the allow button to appear under the Security & Privacy General tab
try this:
```
sudo spctl --master-disable
```
## Method 2
if method 1 is still not working, try this.

* restart Mac, hold ### Command + R at the startup chime until you see the Apple logo. This will boot into the Recovery OS.
* See the top of screen, you will find the Top Menu, select Utilities -> Terminal
* In Terminal, check the status Kernel Extension User Consent via
```
spctl kext-consent status
```
The output should be "ENABLED"
* To disable, type:
```
spctl kext-consent disable
```
* Close Terminal and Restart.
