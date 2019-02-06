### dpigs utility : ...(provided by debian-goodies package) -  Show which installed packages occupy the most space
  install debian goodies :
`
$ sudo apt install debian-goodies
`

[dpigs](http://manpages.ubuntu.com/manpages/cosmic/man1/dpigs.1.html) ==> click on this !!

dpigs is the command :

`
$ dpigs
`

read man pages for more info

`
man dpigs
`

### apt: remove, purge 
**_remove_** :  Removing a package removes all packaged data, but leaves usually
           small (modified) user configuration files behind, in case the
           remove was an accident. Just issuing an installation request for
           the accidentally removed package will restore its function as
           before in that case. 
           
           $ sudo apt remove <package-name> 
           
         
...package-name as in listed by **_dpigs_**
           
**_purge_** :     On the other hand you can get rid of these
           leftovers by calling purge even on already removed packages. Note
           that this does not affect any data or configuration stored in your
           home directory. 
           
           $ sudo apt purge <package-name*>
...to remove leftover config files of **_package-name_**

### apt-get: clean, autoclean, autoremove, purge

**_autoremove_** :  autoremove is used to remove packages that were automatically
           installed to satisfy dependencies for other packages and are now no
           longer needed as dependencies changed or the package(s) needing
           them were removed in the meantime.
           
           $ sudo apt-get autoremove
           
**_clean_**      :  clean clears out the local repository of retrieved package files.
           It removes everything but the lock file from
           `/var/cache/apt/archives/ and /var/cache/apt/archives/partial/` .
          
           $ sudo apt-get clean
 
**_autoclean_**  :  Like clean, autoclean clears out the local repository of retrieved
           package files. The difference is that it only removes package files
           that can no longer be downloaded, and are largely useless. This
           allows a cache to be maintained over a long period without it
           growing out of control.
           
           $ sudo apt-get autoclean
  
**_purge_**   :   purge is identical to remove except that packages are removed and
           purged (any configuration files are deleted too).
           
           $ sudo apt-get purge
