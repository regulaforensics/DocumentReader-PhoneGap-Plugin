# [Deprecated]
As Adobe has discontinued PhoneGap Build and ended investment in PhoneGap and Apache Cordova, this repository is deprecated now and won’t be updated anymore.

#  Regula Document Reader (PhoneGap version)
Regula Document Reader SDK allows you to read various kinds of identification documents, passports, driving licenses, ID cards, etc. All processing is performed completely  _**offline**_  on your device. No any data leaving your device.

You can use native camera to scan the documents or image from gallery for extract all data from it.

We have provided a simple application that demonstrates the  _**API**_  calls you can use to interact with the Document Reader Library.

# Content
* [How to build the demo application](#how-to-build-the-demo-application)
* [How to add the SDK to the project](#how-to-add-the-sdk-to-the-project)
* [Troubleshooting license issues](#troubleshooting-license-issues)
* [Documentation](#documentation)
* [Additional information](#additional-information)

## How to build the demo application
1. Visit [licensing.regulaforensics.com](https://licensing.regulaforensics.com) to get a trial license (`regula.license` file). The license creation wizard will guide you through the necessary steps.
2. Download or clone current repository using the command `git clone https://github.com/regulaforensics/DocumentReader-PhoneGap-Plugin.git`.
3. Run the following commands in Terminal:
```bash
$ cd DocumentReader
$ npm install
$ cordova prepare
```

4. Copy the `regula.license` file to the `DocumentReader/www` folder.
5. Change the application ID to the one you have specified during the registration at [licensing.regulaforensics.com](https://licensing.regulaforensics.com).
6. Android:
  * Run `cordova run android` inside `DocumentReader` folder - this is just one way to run the app. You can also run it directly from within Android Studio.

**Note**: if the following error is encountered: `Program type already present: android.support ...`, remove this line: `cordova.system.library.1=com.android.support:support-...` from the `project.properties` file.

6. iOS:
  * Run `cordova run ios` inside `DocumentReader` folder - this is just one way to run the app. You can also run it directly from within Xcode.

## How to add the SDK to the project
Document Reader libraries are available on [npm](https://www.npmjs.com/~regula).
First of all, install **API** library, simply running the following command:
```bash
$ phonegap plugin add @regulaforensics/cordova-plugin-document-reader-api --variable CAMERA_USAGE_DESCRIPTION="To take photo" --variable READ_EXTERNAL_STORAGE="To choose photo"
```

And then add one of the [Core](https://docs.regulaforensics.com/cordova/core) libraries depend on the functionality that you wish and the license capabilities, e.g.:

```bash
$ phonegap plugin add @regulaforensics/cordova-plugin-document-reader-core-fullrfid
```

## Troubleshooting license issues
If you have issues with license verification when running the application, please verify that next is true:
1. The OS, which you use, is specified in the license (e.g., Android and/or iOS).
2. The application (Bundle) ID, which you use, is specified in the license.
3. The license is valid (not expired).
4. The date and time on the device, where you run the application, are valid.
5. You use the latest release version of the Document Reader SDK.
6. You placed the license into the project.

## Documentation
The documentation on the SDK can be found [here](https://docs.regulaforensics.com/cordova).

## Additional information
If you have any technical questions, feel free to [contact](mailto:cordova.support@regulaforensics.com) us or create issue [here](https://github.com/regulaforensics/DocumentReader-PhoneGap-Plugin/issues).

To use our SDK in your own app you need to [purchase](https://pipedrivewebforms.com/form/394a3706041290a04fbd0d18e7d7810f1841159) a commercial license.
