# Getting the Android SDK

## On OSX

* You can use [brew][1] (`brew install android`)  or get the SDK from the [android developer hub][2]
* Once you have installed the SDK run the SDK Manager (`android sdk`)
  * You will want to have a version of the API with version greater or equal to 17
  * Check out [the docs][3] for the SDK Manager for more information on the subject
* Then you will need to export `$ANDROID_HOME`
  * If you used brew:
	
		`export ANDROID_HOME=/usr/local/Cellar/android-sdk/r21.1`
  
  * Or else export the folder you unzipped your SDK to
* The next step is creating your virtual device

	`android create avd -n <name> -t <id> -b x86`

* Now you can go ahead and run your avd

	`emulator @<name>`

### Notes:
* Intel provides HAX (Hardware Accelerated Execution), this lets the Android VM be hardware accelerated making it faster
* 10.6 and 10.7 users follow these [instructions][4]
* 10.8 should check out the hotfix found [here][5]

## On Linux 

This should be pretty similar to OSX.

### Notes:

* For Ubuntu, you can `apt-get install android-tools-adb` but you will still need the SDK Manager. So getting it all from the [android developper hub][2] should be simpler (and insure your version is up to date).


[1]: http://mxcl.github.io/homebrew/ "brew"
[2]: https://developer.android.com/sdk/index.html "android dev hub"
[3]: https://developer.android.com/tools/help/sdk-manager.html "SDK Manager"
[4]: http://software.intel.com/en-us/articles/installation-instructions-for-intel-hardware-accelerated-execution-manager-macosx "HAX"
[5]: http://software.intel.com/en-us/articles/intel-hardware-accelerated-execution-manager/ "HAX 10.8"
