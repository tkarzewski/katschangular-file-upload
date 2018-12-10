# Angular File Upload

Simple Angular FileUploader with support to upload multiple files in one request

## What is this
For a project I needed an Angular Uploader Lib, which is easy to use, offers some config and supports multiple
Files uploaded in one Request. Because I didn't find any fullfilling these requirements I cloned
[ng2-file-upload](https://github.com/valor-software/ng2-file-upload), merged this
[PullRequest](https://github.com/valor-software/ng2-file-upload/pull/993), made some Enhancements and created 
some Components to use it quickly.

For future Releases I am thinking of offer Components like a Dropzone, Queue, Progressbar and Buttons similar 
to the Example-Application. Feel free to contribute :-)

So credits go to [Valor Software](https://valor-software.com) and [Koen van der Linden](https://github.com/koenvanderlinden)

## How to use it
Use it like the [ng2-file-upload](https://github.com/valor-software/ng2-file-upload) and enjoy the new option
`uploadFilesInSingleRequest` in the `FileUploaderOptions` (credits to [Koen Van der Linden](https://github.com/koenvanderlinden))
to upload multiple files in just one request. Be aware that this cannot be combined with `disableMultipart` is 
`true`.

Following instructions are from [ng2-file-upload](https://github.com/valor-software/ng2-file-upload)

### Quick start

1. A recommended way to install ***angular-file-upload*** is through [npm](https://www.npmjs.com/search?q=angular-file-upload)
package manager using the following command:

  `npm i -S angular-file-upload`

  Alternatively, you can [download it in a ZIP file](https://github.com/tkarzewski/angular-file-upload/archive/master.zip).

2. Currently `angular-file-upload` contains two directives: `afo-file-select` and `afo-file-drop`. `afo-file-select`
is used for 'file-input' field of form and `afo-file-drop` is used for area that will be used for dropping of 
file or files.

3. More information regarding using of ***ng2-file-upload*** is located in
  [demo](http://www.tobias-karzewski.de/angular-file-upload/) and [demo sources](https://github.com/tkarzewski/angular-file-upload/src).
  
### Using ***angular-file-upload*** in a project

1. Install as shown in the above section.

2. Import `AngularFileUploadModule` into the module that declares the component using ***angular-file-upload***:
   <br>```import { AngularFileUploadModule } from 'angular-file-upload';```

3. Add it to `[imports]` under `@NgModule`:
   <br>```imports: [ ... AngularFileUploadModule, ... ]```

4. Import `FileUploader` into the component:
   <br>```import {  FileUploader } from 'angular-file-upload';```

5. Initialize it:
   <br>```public uploader:FileUploader = new FileUploader({url: 'https://my-upload.url.com/api''});```
