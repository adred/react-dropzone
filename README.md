# selfmade-react-dropzone

Simple React hook to create a HTML5-compliant drag'n'drop zone for files with support for auto-upload. This is based on [react-dropzone](https://github.com/react-dropzone/react-dropzone/)

## Demo

[Demo](https://codesandbox.io/s/selfmade-react-dropzone-demo-4zx3z?file=/src/App.js)

## Installation

```bash
npm install --save selfmade-react-dropzone
```

or:

```bash
yarn add selfmade-react-dropzone
```

## Usage

Please refer to [react-dropzone](https://react-dropzone.js.org) for most of the functionality it offers.

For auto-uploading files, you need to pass `uploadConfig` prop. To monitor the progress, you can access the files with status through `uploadedFiles` state.

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
    withCredentials: true, // optional
    responseType: "json" // optional
  }
});
```

## License

MIT
