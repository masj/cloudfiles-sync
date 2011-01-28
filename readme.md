# Cloudfiles-sync

This is a script that allows the syncronisation of Rackspace Cloudfiles (Or any SWIFT object store) with a local directory. Currently it allows the user to pipe a list of files into in that are to be uploaded to cloud files.

Some of the features are:

* Lightweight - Currently the only non standard python library required is python-cloudfiles. The aim is NOT to require anything else, and hence ensuring maximum portability
* Support for Cloudfiles UK and US along with any SWIFT object store
* Comparision of files to ensure Bandwidth is not wasted by compare the remote & local
** MD5
** Modified Time
* Removal of files that do not exist in the source from the destination
* Quiet by default - Allows the script to run as a cron without any noise
* Verbose mode - Useful for logging or debuging
* Progress - a simple progress report

See the projects github wiki page for more info
https://github.com/welbymcroberts/cloudfiles-sync/wiki

# Example usage
`cd /backups && find -type f | python cfsync.py`
