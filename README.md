# Android PDF Viewer

> [!NOTE]
>
> This is a fork of [zacharee/AndroidPdfViewer](https://github.com/zacharee/AndroidPdfViewer) which 
> itself is a fork of the unmaintained [barteksc/AndroidPdfViewerV2](https://github.com/barteksc/AndroidPdfViewerV2).
>
> Credit goes to the original authors and the many contributors across the various forks that have kept 
> this excellent PDF viewer alive. intend to keep this fork reasonably up to date with upstream changes. 
> Pull requests are welcome.

[![Release](https://jitpack.io/v/kishannareshpal/AndroidPdfViewer.svg)](https://jitpack.io/#kishannareshpal/AndroidPdfViewer)


### Installation

Add JitPack to your `build.gradle`:

```groovy
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```

Add the dependency

```groovy
implementation 'com.github.zacharee:AndroidPdfViewer:2026.01.05'
```

(Optiona, but recommended) For more direct control and to stay up to date with the underlying PDF rendering engine, you may also want to depend directly on
[PdfiumAndroidKt](https://github.com/johngray1965/PdfiumAndroidKt):

```groovy
implementation 'io.legere:pdfiumandroid:Version'
```


### Changes in this fork (`com.github.kishannareshpal:AndroidPdfViewer`):

- Used by [@kishannareshpal/expo-pdf](https://github.com/kishannareshpal/expo-pdf)
- Added support for content insets via a new option on the PDFView builder:
  ```kotlin
  PdfView()
    .contentPadding(
        left = 0,
        top = 0,
        right = 0,
        bottom = 0
    )
    .load()
  ```
  This allows padding to be applied around the entire document while still supporting pan and zoom in those areas.
  A common use case is applying safe-area insets while keeping the PDF viewer fullscreen.

### Original documentation for reference

- For the original repo API references and usage examples, please refer to [this page](./docs/ORIGINAL_DOCUMENTATION.md).

### Contributing

#### Releasing a new version

This package is distributed via the [JitPack repository](https://jitpack.io/#kishannareshpal/AndroidPdfViewer).

1. Update the `README` installation instruction to point to the new Tag
2. Create a new GH release tagging main with the version name format: `YYYY.MM.DD.n` (where `n` indicates the release count of the day starting at 1)
3. JitPack will automatically build the necessary assets, which you can see at: https://jitpack.io/#kishannareshpal/AndroidPdfViewer
4. That's it - once JitPack finishes building, you'll be able to install it on your apps.