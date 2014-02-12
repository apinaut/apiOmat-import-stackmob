<a href="https://github.com/apinaut/apiOmat-import-stackmob">apiOmat-import-stackmob</a>
============

Import your data from StackMob into the apiOmat backend.

This script will import your data and schemas from StackMob into the backend of <a href="http://www.apiomat.com">apiOmat</a>.
See below for an example and a step-by-step guide.

After the script is finished you can start programming against the apiOmat backend. For tutorials see <a href="http://www.apiomat.com/docs/">our documentation</a>.

# Install

1. Go to <a href="https://apiomat.org/?locale=en&fromDashboard=false">SignUp</a> to create a new account on apiOmat.
 If you already have an account <a href="https://apiomat.org/?locale=en&free=true&fromDashboard=false#login">login</a> and create a new app.
2. Deploy your app to our cloud by pressing the deploy icon.
3. Copy your 'ApiKey' from the App-Setup in our dashboard. Take also note of the selected system in the left panel (TEST, STAGING or LIVE).
4. Install <a href="http://www.pip-installer.org/en/latest/installing.html">pip</a> on your system.
5. Type 'pip install import-stackmob-to-apiOmat' on the command line to install the python script into your system.
6. ######## export your data from stackmob ###########
7. After ##############, save the data on your harddisk.

# Usage

```js
import-stackmob-to-apiOmat <###parameterlist###>
```
Explanation of parameters:
* --ifile <path_to_zipfile> Insert here filesystem path to the downloaded zip-file
* --appName <appName> The name of your app in apiOmat system
* --apiKey <apiKey> The apiKey from the apiOmat system copied in step 3 above
* --userMail <userName> Your apiOmat username which you use to login in our dashboard
* --password <password> Your password which you use to login in our dashboard
* --system <usedSystem> The system (LIVE , STAGING or TEST) where you are going to import your data. (If you have selected the basic plan you can only import into LIVE system)
* --defaultPwd <default_pw_for_users> Default password for imported users
* --smKey Your public key for the stackmob app (can be found in your Stackmob dashboard https://dashboard.stackmob.com/)
* --smEnv [0,1] 0 = Import your development data from stackmob, 1 means import your production data from stackmob
	
#Example
```js
import-stackmob-to-apiOmat  --ifile=9339.zip --smKey 12345 --smEnv 0 --appName=ParseImport --apiKey=2234224 --userMail=login@apiomat.org --password=12345 --system=LIVE --defaultPwd=12345

```

# Known issues

* same issues? new issues?


# Contributing

This is open source. Feel free to modify and enhance this script
