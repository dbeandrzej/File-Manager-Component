# File Manager Provider
<p>Provider plugin is a bridge between the component plugin and a storage (third-party services or applications such as Amazon S3, Dropbox, Apex application and etc.). It consists of metadata, core, javascript interface.</p>
<div style="text-align:center">
<img src="https://apexfilesdir.s3.eu-west-1.amazonaws.com/apexutil/FileManagerPluginSchema.png" alt="Provider" width="300px">
</div>
<p>
Metadata is initial information which describes a storage (credential, url, host, port, additional parameters) and user settings. Core is PL/SQL code which processes metadata and generates attributes and parameters such as access token, headers, paths and etc., for specific third-party service. JavaScript interface calls web services of the storage by using attributes and parameters from the core and returns result to the component.</p> 