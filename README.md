# react-whiteboard

<div>
  <h2>
    React virtual whiteboard with PDF and Images upload functionality
    <br />
  </h2>
</div>

<br />





Check App demo here:

<img width="947" alt="image" src="https://github.com/AmanShukla-rko/whiteboard/assets/81101653/e036be54-3fbb-4fa9-b8b5-71e91b4969de">
<img width="948" alt="image" src="https://github.com/AmanShukla-rko/whiteboard/assets/81101653/78573098-14f6-4315-adaf-0ffe2b68bf35">
<img width="951" alt="image" src="https://github.com/AmanShukla-rko/whiteboard/assets/81101653/9e7c7241-d26b-4edd-8584-d71255f6a43f">
<img width="944" alt="image" src="https://github.com/AmanShukla-rko/whiteboard/assets/81101653/af7f742b-cfc8-486a-b2da-31c8792a370a">

png save image
<img width="817" alt="image" src="https://github.com/AmanShukla-rko/whiteboard/assets/81101653/c2963fd4-a65c-46ab-854c-d25620c3b57b">



<br/>



## Usage

```javascript
const App = () => {
  return (
    <div>
      <Whiteboard />
    </div>
  );
};
```

You can change default props

```javascript
import { Whiteboard } from 'react-whiteboard-pdf';

const App = () => {
  return (
    <Whiteboard
      // default parameters
      drawingSettings={{
        brushWidth: 5, // :number (optional) (default: 5) - brush size for drawing
        background: false, // :boolean (optional) (default: false) - polkadot as background picture
        currentMode: modes.PENCIL, //
        currentColor: '#000000',
        brushWidth: 5,
        fill: false, // if true, square, rectangle, and triangle will be filled with current color
      }}
      // default controls
      controls={{
        PENCIL: true,
        LINE: true,
        RECTANGLE: true,
        ELLIPSE: true,
        TRIANGLE: true,
        TEXT: true,
        SELECT: true,
        ERASER: true,
        CLEAR: true,
        FILL: true,
        BRUSH: true,
        COLOR_PICKER: true,
        DEFAULT_COLORS: true,
        FILES: true,
        SAVE_AS_IMAGE: true,
        GO_TO_START: true,
        SAVE_AND_LOAD: true,
        ZOOM: true,
        TABS: true,
      }}
      settings={{
        zoom: 1,
        minZoom: 0.05,
        maxZoom: 9.99,
        contentJSON: null, // JSON to render in canvas
      }}
      fileInfo={{
        file: { name: 'Whiteboard' },
        totalPages: 1,
        currentPageNumber: 1,
        currentPage: '',
      }}
      onObjectAdded={(addedObject) => {}}
      onObjectRemoved={(removedObject) => {}}
      onObjectAdded={(data, event, canvas) => {}}
      onObjectRemoved={(data, event, canvas) => {}}
      onZoom={(data, event, canvas) => {}}
      onImageUploaded={(data, event, canvas) => {}}
      onPDFUploaded={(data, event, canvas) => {}}
      onPDFUpdated={(data, event, canvas) => {}}
      onPageChange={(data, event, canvas) => {}}
      onOptionsChange={(data, event, canvas) => {}}
      onSaveCanvasAsImage={(data, event, canvas) => {}}
      onConfigChange={(data, event, canvas) => {}}
      onSaveCanvasState={(data, event, canvas) => {}}
      onDocumentChanged={(data, event, canvas) => {}}
    />
  );
};
```

