# Devrant Api Map

This project has the goal of creating a FULL map of the devRant API.
Unlike other api mapping projects this one tries aims to be complete, including
features exclusive to the mobile app.

# Documentation format
The documentation is in the Swagger v2.0 format.

# Contributing
Contributing is very much appeciated!
If you have mapped more routes, added explainations, fixed typos or have
anything else to contribute, don't hesitate to make a PR.
Contributors will be mentioned below.

# Data sources
Currently the main data source is a MITMProxy request capture of the mobile
app, which can be found in the file _req-capture_.

To view it, run `mitmproxy --rfile req-capture`.
The tool used to disable certificate pinning is [objection](https://github.com/sensepost/objection).
To make your own request captures:
1. Download the devRant APK
2. patch it with: `objection patchapk -s devRant.apk -d`
3. install it on your device with `adb install devRant.objection.apk`
4. Install and run mitmproxy with `mitmproxy --save-stream-file FILENAME`
5. Set your PC to be the proxy server on your phone
6. go to mitm.it on your phone to install your local mitmproxy root cert.
7. Start the app
8. open the objection console with `objection explore`
9. disable ssl-pinning with `android sslpinning disable`
10. Use the app.

# Contributors
## xzvf

# License
This project is licensed under GPL v3, in order to make sure that this documentation
becomes as good as possible, because improvements need to be shared.

See the LICENSE file for the full license.
