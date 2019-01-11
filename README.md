# File Manager Component  (Apex Plugin)

## What is File Manager?
File Manager is the family of plugins for file management for APEX application. It gives ability to upload / download / delete files from 3rd party providers (eg. Amazon S3 /others in progress/). 
The set consists two parts: 
1. [Component plugin](#what-is-component) - APEX page item (file browse input);
2. [Provider plugin](#what-is-provider) - connection between the component and a storage.
<p align="center">
<img src="http://apexfilesdir.s3.eu-west-1.amazonaws.com/apexutil/FMschema1.png" alt="File Manager" width="400px">
</p>

## What is component?
<p align="center">
<img src="http://apexfilesdir.s3.eu-west-1.amazonaws.com/apexutil/FMschema2.png" alt="Component" width="400px">
</p>

## What is provider?
Provider plugin is a bridge between the component plugin and a storage (third-party services or applications such as Amazon S3, Dropbox, Apex application and etc.). It consists of metadata, core, javascript interface.
<p align="center">
<img src="https://apexfilesdir.s3.eu-west-1.amazonaws.com/apexutil/FileManagerPluginSchema.png" alt="Provider" width="300px">
</p>
Metadata is initial information which describes a storage (credential, url, host, port, additional parameters) and user settings. Core is PL/SQL code which processes metadata and generates attributes and parameters such as access token, headers, paths and etc., for specific third-party service. JavaScript interface calls web services of the storage by using attributes and parameters from the core and returns result to the component.

### Available providers
* [File Manager Provider AWS3](#).

