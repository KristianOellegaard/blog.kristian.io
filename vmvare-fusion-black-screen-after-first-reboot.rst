VMVare fusion black screen after first reboot
#############################################
:date: 2011-05-07 22:19
:category: Apple, Mac, System administration

Today i wanted to test some stuff, so i fired up 3 vms with the newest
ubuntu server, i used VMVware fusions easy install feature and it didnt
take many minutes before everything worked, however, then i did sudo
reboot and got black screen, no reaction at all. However, after randomly
doing a couple of things, i tried to turn it off - and it actually
printed the different services going down. So i found out that it
default didnt activate any tty's, so you just have to switch to any one
of them, e.g. ALT + F1 (if you are on a macbook pro too, remember the FN
button in the combination, to actually use the F2 key)
