# How-To
## Send files directly from context menu on Windows
### Registering to open files with ShareGlimmer
The [File Handling API](https://learn.microsoft.com/en-us/microsoft-edge/progressive-web-apps-chromium/how-to/handle-files) is implemented

This is still experimental and must be enabled via a flag **before** the PWA is installed to Windows.
1. [Enabled feature in Edge](https://learn.microsoft.com/en-us/microsoft-edge/progressive-web-apps-chromium/how-to/handle-files#enable-the-file-handling-api)
2. Install ShareGlimmer by visiting https://ShareGlimmer.net/ with the Edge browser and install it as described [here](faq.md#help--i-cant-install-the-pwa-).
3. You are done! You can now send most files one at a time via ShareGlimmer:
   
   _context menu > Open with > ShareGlimmer_

[//]: # (Todo: add screenshots)

### Sending multiple files to ShareGlimmer
Outstandingly, it is also possible to send multiple files to ShareGlimmer via the context menu by adding ShareGlimmer to the `Send to` menu:
1. [Register ShareGlimmer as file handler](#registering-to-open-files-with-ShareGlimmer) 
2. Hit Windows Key+R, type: `shell:programs` and hit Enter.
3. Copy the ShareGlimmer shortcut from the directory
4. Hit Windows Key+R, type: `shell:sendto` and hit Enter.
5. Paste the copied shortcut into the directory
6. You are done! You can now send multiple files (but no directories) directly via ShareGlimmer:
   
   _context menu > Send to > ShareGlimmer_

[//]: # (Todo: add screenshots)

## Send directly from share menu on iOS
I created an iOS shortcut to send images, files, folder, URLs or text directly from the share-menu 
https://routinehub.co/shortcut/13990/

[//]: # (Todo: add doku with screenshots)


## Send directly from share menu on Android
The [Web Share Target API](https://developer.mozilla.org/en-US/docs/Web/Manifest/share_target) is implemented.

When the PWA is installed, it will register itself to the share-menu of the device automatically.


## Send directly via command-line interface
Send files or text with ShareGlimmer via command-line interface.

This opens ShareGlimmer in the default browser where you can choose the receiver.

### Usage
```bash
$ ShareGlimmer -h
Current domain: https://ShareGlimmer.net/

Usage:
Open ShareGlimmer:          ShareGlimmer
Send files:             ShareGlimmer file/directory
Send text:              ShareGlimmer -t "text"
Specify domain:         ShareGlimmer -d "https://ShareGlimmer.net/"
Show this help text:    ShareGlimmer (-h|--help)
```

On Windows Command Prompt you need to use bash: `bash ShareGlimmer -h`


### Setup
Download the bash file: [ShareGlimmer-cli/ShareGlimmer](/ShareGlimmer-cli/ShareGlimmer).

#### Linux
1. Put file in a preferred folder e.g. `/usr/local/bin`
2. Make sure the bash file is executable. Otherwise, use `chmod +x ShareGlimmer`
3. Add absolute path of the folder to PATH variable to make `ShareGlimmer` available globally by executing
   `export PATH=$PATH:/opt/ShareGlimmer-cli`

#### Mac
1. add bash file to `/usr/local/bin`

#### Windows
1. Put file in a preferred folder e.g. `C:\Users\Public\ShareGlimmer-cli`
2. Search for and open `Edit environment variables for your account`
3. Click `Environment Variables...`
4. Under *System Variables* select `Path` and click *Edit...*
5. Click *New*, insert the preferred folder (`C:\Users\Public\ShareGlimmer-cli`), click *OK* until all windows are closed
6. Reopen Command prompt window

[< Back](/README.md)
