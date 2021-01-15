# flutterPDFViewer

# advance_pdf_viewer

A flutter plugin for handling PDF files. Works on both Android & iOS. Originally forked from(https://github.com/lohanidamodar/pdf_viewer), which was originally forked from (https://github.com/CrossPT/flutter_plugin_pdf_viewer).



## Installation

Add  *advance_pdf_viewer*  as a dependency in [your pubspec.yaml file](https://flutter.io/platform-plugins/).
```
advance_pdf_viewer:
    git:
        url: https://github.com/adiltirur/flutterPDFViewer.git
```

---

## Android
No permissions required. Uses application cache directory.

## iOS
No permissions required.

## How-to:

#### Load PDF
```
// Load from assets
PDFDocument doc = await PDFDocument.fromAsset('assets/test.pdf');
 
// Load from URL
PDFDocument doc = await PDFDocument.fromURL('http://www.africau.edu/images/default/sample.pdf');

// Load from file
File file  = File('...');
PDFDocument doc = await PDFDocument.fromFile(file);
```

#### Load pages
```
// Load specific page
PDFPage pageOne = await doc.get(page: _number);
```

#### Pre-built viewer
Use the pre-built PDF Viewer
```
@override
  Widget build(BuildContext context) {
    Scaffold(
        appBar: AppBar(
          title: Text('Example'),
        ),
        body: Center(
        child: _isLoading
            ? Center(child: CircularProgressIndicator())
            : PDFViewer(document: document, isIOS:true)),
    );
  }
```

---

## New Platform Awareness Addition

* use isIos flag


---

#### Third-party packages used

| Name | Description  |
|-|-|
| [path_provider](https://pub.dartlang.org/packages/path_provider)               | A Flutter plugin for finding commonly used locations on the filesystem. Supports iOS and Android.            |
| [flutter_cache_manager](https://pub.dartlang.org/packages/flutter_cache_manager)       | A CacheManager to download and cache files in the cache directory of the app. Various settings on how long to keep a file can be changed. |
| [numberpicker](https://pub.dartlang.org/packages/numberpicker)                | NumberPicker is a custom widget designed for choosing an integer or decimal number by scrolling spinners. |
| [flutter_advanced_networkimage](https://pub.dartlang.org/packages/flutter_advanced_networkimage) | An advanced image provider provides caching and retrying for flutter app. Now with zoomable widget and transition to image widget. |
