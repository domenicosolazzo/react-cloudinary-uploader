# react-cloudinary-uploader
React File Uploader for Cloudinary.
This React component wraps the Cloudinary Widget.It wraps all the properties of both the widget and the returned results in the state of the React component. 

# Installation
==============
You need to [include the Cloudinary script](http://goo.gl/VnTE0q) at the bottom of your page, but before loading your React app.

* npm install
* node server.js

# Configuration
===============
The component accepts few properties as input. cloudName and uploadPreset are required properties for this component.
* **cloudName**: the cloud name that you can find in your configuration in Cloudinary.
* **uploadPreset**: The upload_preset that you can find in your settins (Upload) in Cloudinary. 
* **showPoweredBy** [true | false]: It shows the poweredBy logo in the widget. 
* **allowedFormats**: An array of allowed format. (e.g. ['jpeg', 'png'])
* **maxFileSize**: If specified, perform client side validation that prevents uploading files bigger than the given bytes size (e.g. 130000)
* **maxImageWidth**: If specified, client-side scale-down resizing takes place before uploading if the width of the selected file is bigger than the specified value. (e.g. 2000)
* **maxImageHeight**: If specified, client-side scale-down resizing takes place before uploading if the height of the selected file is bigger than the specified value. (e.g. 2000)
* **sources** ["local", "web", "web"]: List of file sources
* **defaultSource**: The default selected source tab when the widget is opened.
* **multiple**: Whether selecting and uploading multiple images is allowed.
* **maxFiles**: The maximum number of files allowed in multiple upload mode.
* **cropping** ["server" | null]: Whether to enable interactive cropping of images before uploading.
* **croppingAspectRatio**: If specified, enforce the given aspect ratio on selected region when performing interactive cropping. (e.g. 0.5)
* **publicId**: Custom public ID to assign to a single uploaded image.
* **folder**: Folder name for all uploaded images. Acts as the prefix of assigned public IDs.
* **tags**: One or more tags to assign to the uploaded images.
* **resourceType** ["auto", "image", "raw"]: The resource type of the uploaded files.
* **contextAlt**: Additional context metadata to attach to the uploaded images.
* **contextCaption**: Additional context metadata to attach to the uploaded images.
* **buttonClass**: Allows overriding the default CSS class name of the upload button added to your site.
* **buttonCaption**: Allows overriding the default caption of the upload button added to your site.

# State
=======
The React component keeps track of the information returned from the upload.
* **bytes**: Bytes of the image
* **created_at**: Last modification date of the image
* **etag**: Etag of the image
* **format**: Format of the image
* **height**: Height of the image
* **width**: Width of the image,
* **path**: Image path,
* **public_id**: Image public id,
* **resource_type**: Resource type,
* **secure_url**: Secure URL for the image,
* **signature**: Signature for the image,
* **tags**: List of tags connected to the image
* **thumbnail_url**: Thumbnail url
* **type**: Image type
* **url**: Image URL
* **version**: Version of the image
* **isError**: True if there was an error during upload, false otherwise
* **errorMessage**: The error message in case there was an error
* **uuid**: Unique identifier for the widget

## WIP
* Clean up some state properties
* Allow multiple upload 
* Allow basic transformations
