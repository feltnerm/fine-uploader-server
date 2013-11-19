# Fine Uploader 101

## Intro

Hello! ...

### Server

Download server as zip and extract

`
`
Download and install node

`http://nodejs.org/download/
`
Make sure server works!

`node install
node server.js
`
### Prepare the Client
1. Download FU built source files as .zip and extract
1. Copy all FU built source files into assets/1. Open up assets/templates/default.html Replace lines 13 and 14 with:

`    <!-- much jquery -->
    <script src="//code.jquery.com/jquery-1.10.2.min.js"></script>

    <!-- wow so uplood -->
    <link href="../fineuploader-4.0.3.css" rel="stylesheet">
    <script src="../jquery.fineuploader-4.0.3.js"></script>
`
GOTO:

`http://localhost:8000/assets/templates/default.html
`
Clean slate.

# Modifiying FU

## Uploadin' Stuff

1. Make an instance of Fine Uploader on your page

`    <div id="i-am-the-fine-uploader"></div>

    <script type="text/javascript">
    $(document).ready(function () {
        $('#i-am-the-fine-uploader').fineUploader({
            request: {
                endpoint: '/uploads'
            }
        });
    });
    </script>
`
Make some uploads happen.

### Deletin' Stuff

`deleteFile: {
    enabled: true,
    endpoint: '/uploads'
},
`
Boom. Gone. NSA can't find your files now!

### Previews

Editing the template.

`template: 'qq-simple-thumbnails-template',
`
### Drag 'n' Drop

Remove:

` <div class="qq-upload-drop-area-selector qq-upload-drop-area" qq-hide-dropzone>
    <span>Drop files here to upload</span>
</div>
`
Lol, no more dropzone.

### Edit Filename

Already enabled.

#### Autoupload

`autoupload: false
`
#### Upload Button

`<div id="extra-button"><input type="button" value="Upload Now!"></div>

<script type="text/javascript">
    $('#extra-button').click(function() {
        $('#i-am-the-fine-uploader').fineUploader('uploadStoredFiles');
    });
</script>
`
### Make it 'pop'

Edit css.


----


w00t!

> Written with [StackEdit](https://stackedit.io/).
