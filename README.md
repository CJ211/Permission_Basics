# Permission_Basics
Android_Assignment_9.1


a) What is the difference between Internal Storage & External Storage?

When building an app that uses the internal storage, the Android OS creates a unique folder, which will only be accessible from the app, so no other app, or even the user, can see what's in the folder.

The external storage is more like a public storage, so for now, it's the sdcard, but could become any other type of storage (remote hard drive, or anything else).

The internal storage should only be used for application data, (preferences files and settings, sound or image media for the app to work). If you intent to download many mp3s, i'd reccomend saving them to external storage, as the external storage is often bigger. Besides, storing data on the internal storage may prevent the user to install other applications.


b) For how long the data resides in the cache?

Your app's internal storage directory is specified by your app's package
name in a special location of the Android file system. Technically, another app can
read your internal files if you set the file mode to be readable. However, the other
app would also need to know your app package name and file names. Other apps
cannot browse your internal directories and do not have read or write access
unless you explicitly set the files to be readable or writable. So as long as you
use MODE_PRIVATE for your files on the internal storage, they are never
accessible to other apps

c) What are the critical Permissions and Normal Permissions? What are the
examples of each?

Normal permissions do not directly risk the user's privacy. If your app lists a normal permission in its manifest, the system grants the permission automatically.
 For example, permission to set the time zone is a normal permission

Dangerous permissions can give the app access to the user's confidential data. If your app lists a normal permission in its manifest, the system grants the permission automatically. If you list a dangerous permission, the user has to explicitly give approval to your app.
 For example, the ability to read the user's contacts is a dangerous permission. If an app declares that it needs a dangerous permission, the user has to explicitly grant the permission to the app.
