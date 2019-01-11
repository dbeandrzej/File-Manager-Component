# File Manager Component  (Oracle APEX Plugin)
This is a simple file input that gives you file browser capabilities like never before - eg. put your files on Amazon S3 cloud. Advantages: 
* does not need database to upload files; 
* does not need Oracle Wallet; 
* high performance, dependend only on yours connection speed.

To use it you need 2 elements - This File Manager Component and second plugin - "File Manager Provider". The Provider acts as plugin for specific 3rd party file server support. At the moment we have only Amazon S3 Cloud. But we will add more in time! Stay tuned!
### Available providers
* [File Manager Provider AWS3](#).

## What is File Manager?
File Manager is the family of plugins for file management for APEX application. It gives ability to upload / download / delete files from 3rd party providers (eg. Amazon S3 /others in progress/). 
The set consists two parts: 
1. [Component plugin](#what-is-component) - APEX page item (file browse input);
2. [Provider plugin](#what-is-provider) - connection between the component and a storage.
<p align="center">
<img src="http://apexfilesdir.s3.eu-west-1.amazonaws.com/apexutil/FMschema1.png" alt="File Manager" width="400px">
</p>

## What is component?
Component plugin is APEX page item. It provides simple user interface which enables the user to locate and upload a file from a local file system.
<p align="center">
<img src="https://apexfilesdir.s3.eu-west-1.amazonaws.com/apexutil/FileManager.PNG?v=1" alt="Component" width="400px">
</p>

<p align="center">
<img src="http://apexfilesdir.s3.eu-west-1.amazonaws.com/apexutil/FMschema2.png" alt="Component" width="400px">
</p>

## What is provider?
Provider plugin is a bridge between the component plugin and a storage (third-party services or applications such as Amazon S3, Dropbox, Apex application etc.). It consists of metadata, core and javascript interface.
<p align="center">
<img src="https://apexfilesdir.s3.eu-west-1.amazonaws.com/apexutil/FileManagerPluginSchema.png" alt="Provider" width="300px">
</p>
Metadata is initial information which describes a storage (credential, url, host, port, additional parameters) and user settings. Core is PL/SQL code which processes metadata and generates attributes and parameters such as access token, headers, paths etc., for specific third-party service. JavaScript interface calls web services of the storage by using attributes and parameters from the core and returns result to the component.

