# Smallest App

The smallest app is a demo app that is really the simplest thing you can deploy to Cloud Foundry. 

It consists of just this file. This is only here to provide instructions and because the cf cli requires at least one file to upload.

## Usage

Run `cf push -m 64m -b staticfile_buildpack --random-route smallest-app`. Then to test `curl https://<assigned-route>/README.md`.

## Details

When run, the cf cli will upload the application which consists of just the README.md file. It will use the static file buildpack to install Nginx & run Nginx which serves up the README.md file.

You could make the app slightly more useful by supplying an `index.html` file instead, but that's not done here to show that you can get by with even less & is left as an exercise for the reader.
