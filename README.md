<a href="https://github.com/apiOmat/apiOmat-import-parse">apiOmat-import-parse</a>
============

Import your data from Parse into apiOmat backend.

This script will import your data and schemas from Parse into the backend of <a href="http://www.apiomat.com">apiOmat</a>.
See below for an example and a step-by-step guide.

After the script is finished you can start programming against the apiOmat backend. For tutorials see <a href="http://www.apiomat.com/docs/">our documentation</a>. A comparsion of the android client code between parse and apiomat can be found <a href="http://www.apiomat.com/docs/android-parse-comparison/">here</a>.

# Install

1. Go to <a href="https://apiomat.org/?locale=en&fromDashboard=false">SignUp</a> to create a new account on apiOmat.
 If you already have an account <a href="https://apiomat.org/?locale=en&free=true&fromDashboard=false#login">login</a> and create a new app.
2. Deploy your app to our cloud by pressing the deploy icon.
3. Copy your 'ApiKey' from the App-Setup in our dashboard. Take also note of the selected system in the left panel (TEST, STAGING or LIVE).
4. Install <a href="http://www.pip-installer.org/en/latest/installing.html">pip</a> on your system.
5. Type 'pip install import-parse-to-apiOmat' on the command line to install the python script into your system.
6. Go to your Parse dashboard and export your data as zip. For details see <a href="http://blog.parse.com/2012/03/09/one-click-export/">this link</a>.
7. After you received the mail with your data, save them on your harddisk.

# Usage

```js
import-parse-to-apiOmat --ifile=<path_to_zipfile> --appName=<appName> --apiKey=<apiKey> --userMail=<userMail> --password=<password> --system=<usedSystem> --defaultPwd=<default_pw_for_users>
```
Explanation of parameters:
* --ifile <path_to_zipfile> Insert here filesystem path to the downloaded zip-file
* --appName <appName> The name of your app in apiOmat system
* --apiKey <apiKey> The apiKey from the apiOmat system copied in step 3 above
* --userMail <userName> Your apiOmat username which you use to login in our dashboard
* --password <password> Your password which you use to login in our dashboard
* --system <usedSystem> The system (LIVE , STAGING or TEST) where you are going to import your data. (If you have selected the basic plan you can only import into LIVE system)
* --defaultPwd <default_pw_for_users> Default password for imported users
	
#Example
```js
import-parse-to-apiOmat  --ifile=9339.zip --appName=ParseImport --apiKey=2234224 --userMail=login@apiomat.org --password=12345 --system=LIVE --defaultPwd=12345
```

# Known issues

* Can't import binary files, this Parse data format will be converted to a String and saves only the URL to the data
* No support for arrays with mixed types
* Can't import passwords from existing users. The password for existing users would be resetted to given password, cause we won't decrypt passwords from Parse users
* actual no support for ACL (coming to apiOmat soon)


# Contributing

This is open source. Feel free to modify and enhance this script