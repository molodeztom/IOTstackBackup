# IOTstack Backup and Restore

This is a fork from IOTstackBackup from Paraphraser. He did the main work and I am thankful for his work. 
I have added a way to safe backups on dropbox and to keep a certain number of backups on the raspberry.
I use a Raspi4 with an USB SSD so I have plenty of local space. 
I am not an expert with linux nor bash programming. Some lines and ideas are from other sources like dropbox Uploader. 

If you want to use encryption you have to set up gpg first. You can write the passphrase into a file so it will not ask.
If you do not want encryption simply delete the line with gpg -c --passphrase-file /home/pi/user/pass --pinentry-mode loopback $RUNTAG.FullBackup.tar

The structure of backup folders is:

IOTSTACK-backups
              - archive (used temporarily as source for upload)
              - arvive_old n backups configurable in script
              - influxdb influxdb backup merged (tar) into "backup".tar

