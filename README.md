# React Native Dimensions API Orientation Change Bug

This repository demonstrates a common but often overlooked bug in React Native: the `Dimensions` API's failure to automatically update when the device orientation changes.  The provided code shows the problem, and a solution is offered to address this issue.

## Problem

The initial implementation fetches screen dimensions using `Dimensions.get('window')` upon component mount.  However, if the device orientation changes (from portrait to landscape or vice versa), the dimensions remain unchanged, leading to layout issues and incorrect display.

## Solution

The solution uses the `Dimensions` API's `addEventListener` method to listen for orientation changes and update the state accordingly.  This ensures the dimensions are always up-to-date, regardless of the orientation.