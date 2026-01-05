> [!NOTE]
>
> This is a fork of https://github.com/zacharee/AndroidPdfViewer which itself is a fork of the unmaintained
> https://github.com/barteksc/AndroidPdfViewerV2.

[![Release](https://jitpack.io/v/zacharee/AndroidPdfViewer.svg)](https://jitpack.io/#zacharee/AndroidPdfViewer)

Add to _build.gradle_:

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
implementation 'com.github.zacharee:AndroidPdfViewer:Tag'
```

Consider also depending directly on [PdfiumAndroidKt](https://github.com/johngray1965/PdfiumAndroidKt) in order to stay
up-to-date on the actual PDF rendering logic

```groovy
implementation 'io.legere:pdfiumandroid:Version'
```

---


### Original documentation

- Please read the original documentation for API references and examples [here](./docs/ORIGINAL_DOCUMENTATION.md).