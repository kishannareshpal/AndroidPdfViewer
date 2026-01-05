> [!NOTE]
>
> This is a fork of https://github.com/zacharee/AndroidPdfViewer which itself is a fork of the unmaintained
> https://github.com/barteksc/AndroidPdfViewerV2.

[![Release](https://jitpack.io/v/zacharee/AndroidPdfViewer.svg)](https://jitpack.io/#zacharee/AndroidPdfViewer)

Add to `build.gradle`:

```groovy
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```

Add the dependency:

```groovy
implementation 'com.github.kishannareshpal:AndroidPdfViewer:Tag'
```

Consider also depending directly on [PdfiumAndroidKt](https://github.com/johngray1965/PdfiumAndroidKt) in order to stay
up-to-date on the actual PDF rendering logic

```groovy
implementation 'io.legere:pdfiumandroid:Version'
```

---


### Changes in this package (`com.github.kishannareshpal:AndroidPdfViewer`):

- [x] Used by [kishannareshpal/expo-pdf](https://github.com/kishannareshpal/expo-pdf)
- [x] Added support for content insets via a new `PdfView().contentPadding(left: Int = 0, top: Int = 0, right: Int = 0, bottom: Int = 0).load()` option in the PDFView builder.
  - This is useful to apply a padding around the entire document, while still allowing pan and zoom in 
  those areas - for example - you could use this to apply safe area insets while maintaining the
  PDF viewer fullscreen.


### Original documentation for reference

- Please read the original documentation for additional API references and examples [here](./docs/ORIGINAL_DOCUMENTATION.md).