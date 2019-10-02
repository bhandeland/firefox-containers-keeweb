# firefox-containers-keeweb
Integrating Keeweb with Firefox and Multi-account containers.  This set of instructions will allow you to register a URL in keeweb and have it open in a new Firefox Browser tab with an autocreated container.  This is useful for logging into a website multiple times, '''AWS Consoles''' etc.

## Requirements ##
- Linux Desktop (Mine is Ubuntu 18.04 with Gnome)
- Keeweb: https://keeweb.info/
- Firefox
- Firefox Containers 
     - Addon: https://addons.mozilla.org/en-GB/firefox/addon/multi-account-containers/
     - Source: https://github.com/mozilla/multi-account-containers#readme
- Firefox Open URL in Container: 
     - Addon: https://addons.mozilla.org/en-US/firefox/addon/open-url-in-container/
     - Source: https://github.com/honsiorovskyi/open-url-in-container
     
## Installation ##
1.) Copy '''firefox-container.desktop''' to ~/.local/share/applications or to /usr/share/applications
    
    $ cp firefox-container.desktop ~/.local/share/applications
    
2.) Register the MIME handler 
    
    $ xdg-mime default firefox-container.desktop x-scheme-handler/firefox
    
3.) Copy firefox-c to somewhere in your path.  I use my home directory/bin:
    
    $ cp firefox-c ~/bin
    $ chmod +x ~/bin/firefox-c
4.) Setup the '''Website''' address in keeweb to use the firefox handler:
    
    firefox://https://www.google.com
    
Thats it.  Whenever you click the firefox:// link in keepass (or anywhere on your desktop for that matter), it will automatically launch in a new container tab (create it if necessary).

## Thanks ##
Thanks to '''Denys Honsiorovskyi''' for creating the Open URL in Container extension. Denys did all the heavy lifting of the URL handling.

Thanks to Mozilla for creating the Multi-container tabs.

And of course, thanks to the keeweb guys for making a great product.
     

