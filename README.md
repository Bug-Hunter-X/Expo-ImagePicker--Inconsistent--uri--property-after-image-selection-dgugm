# Expo ImagePicker: Inconsistent `uri` Property

This repository demonstrates a bug in the Expo ImagePicker library where the `uri` property of a selected image is sometimes undefined or null. This inconsistency leads to unexpected application behavior and errors.

## Problem Description

The `ImagePicker.launchImageLibraryAsync()` function in Expo, while generally functioning correctly, exhibits intermittent behavior where the `uri` property of the selected image is returned as undefined or null. This issue is not consistent, happening sporadically and without a clear pattern.

## Reproduction

Clone this repository and run the `bug.js` file. Select an image. Observe that sometimes the image URI is properly displayed, other times it isn't.

## Solution

The `bugSolution.js` file demonstrates a solution that addresses the issue by implementing error handling and checks for the `uri` property before using it.  This method ensures that the application does not crash and handles the unpredictable nature of the `uri` property.