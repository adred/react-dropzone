# selfmade-react-dropzone

Simple React hook to create a HTML5-compliant drag'n'drop zone for files with support for auto-upload and appending files through multiple drag and drop. This is based on https://github.com/react-dropzone/react-dropzone/

## Installation

Install it from npm and include it in your React build process (using [Webpack](http://webpack.github.io/), [Browserify](http://browserify.org/), etc).

```bash
npm install --save selfmade-react-dropzone
```

or:

```bash
yarn add selfmade-react-dropzone
```

## Usage

Please refer to https://react-dropzone.js.org for most of the functionality it offers.

For appending files, it's enabled by default. If you want to disable it just pass `appendFiles` prop and set to false

```javascript
const {
  acceptedFiles,
  draggedFiles,
  getRootProps,
  getInputProps
} = useDropzone({
  appendFiles: false
});
```

For auto-uploading files, you need to pass `uploadConfig` prop. To monitor the progress, you can access the files with status through `uploadedFiles` state. Note that this is work in progress...

```javascript
const {
  acceptedFiles,
  uploadedFiles,
  draggedFiles,
  getRootProps,
  getInputProps
} = useDropzone({
  uploadConfig: {
    url: "https://httpbin.org/post", // required
    metadata: {}, // optional
    headers: {}, // optional
    withCredentials: true // optional
  }
});
```

## License

MIT
