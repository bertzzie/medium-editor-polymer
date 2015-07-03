# Medium Editor for Polymer

A project that integrates the [medium-eEditor](https://github.com/yabwe/medium-editor) to polymer. I also included the editor's [insert-plugin](https://github.com/orthes/medium-editor-insert-plugin) so user can insert pictures and videos. 

**Note**: For now, this project is very limited. This is my first polymer component, so there's still much to learn. Please submit pull-rquest or email me if there's something that needs to be improved.

## Todo List

There's still several things needed to be done to improve the projects:

* add a test (haven't figured out how to do. [some clue](https://gist.github.com/addyosmani/b318ca7618eed38c05e1))
* integrate a build system (e.g. [vulcanize](https://github.com/Polymer/vulcanize))

## How to Use

First step is to include the editor in your HTML file:

    <script src="/path/to/webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="path/to/medium-editor-polymer.html">

`webcomponents` is a library provided by Polymer to add web component support to browsers that don't support it yet. After importing both of those, you can directly use the component in your HTML:

    <medium-editor-polymer upload-url="/image/upload/path" upload-method="PUT">
    </medium-editor-polymer>

The editor currently has three attributes you can use:

     Attribute      |  Type  | Value
--------------------|--------|--------------------------------------------------------------------------
`upload-url`        | String | URL of your server that can receive image upload. Default: ""
`upload-method`     | String | HTTP Method for `upload-url`. Default: `PUT`
`upload-data-type`  | Object | Data type your server recieve. Default: `/(\.|\/)(gif|jpe?g|png)$/i`
`upload-field-name` | String | The parameter name you'd like to use for uploaded image. Default: "image"

## Events

The editor support several events related to the content:

       Attribute      | Value
----------------------|------------------------------------------------------------------------------
`image-upload-failed` | Event triggered when image upload process failed due to server or other issue

## License

Unless explicitly mentioned, the license for this project is Polymer's BSD (see `LICENSE.txt`). 
