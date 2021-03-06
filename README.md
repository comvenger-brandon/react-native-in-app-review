# react-native-in-app-review
The Google Play In-App Review API lets you prompt users to submit Play Store ratings and reviews without the inconvenience of leaving your app or game.

Generally, the in-app review can be triggered at any time throughout the user journey of your app. During the flow, the user has the ability to rate your app using the 1 to 5 star system and to add an optional comment. Once submitted, the review is sent to the Play Store and eventually displayed.

# Android Only

# Google Play In-App Review API
[![N|Solid](https://developer.android.com/images/google/play/in-app-review/iar-flow.jpg)](https://developer.android.com/guide/playcore/in-app-review)

# Getting Started
```sh
$ npm install react-native-in-app-review
```
# Usage 
```sh
import InAppReview from 'react-native-in-app-review';
```

```javascript
 InAppReview.RequestInAppReview();
```

# When to request an in-app review

 Follow these guidelines to help you decide when to request in-app reviews from users:

* Trigger the in-app review flow after a user has experienced enough of your app or game to provide useful feedback.
* Do not prompt the user excessively for a review. This approach helps minimize user frustration and limit API usage (see the section on quotas).
* Your app should not ask the user any questions before or while presenting the rating button or card, including questions about their opinion (such as “Do you like the app?”) or predictive questions (such as “Would you rate this app 5 stars”).

# Quotas
To provide a great user experience, Google Play enforces a quota on how often a user can be shown the review dialog. Because of this, calling a launchReviewFlow method might not always display a dialog. For example, you should not have a call-to-action option (such as a button) to trigger a review as a user might have already hit their quota and the flow won’t be shown, presenting a broken experience to the user.

# Device requirements
In-app reviews only work on the following devices:

* Android devices (phones and tablets) running Android 5.0 (API level 21) or higher that have the Google Play Store installed.
* Chrome OS devices that have the Google Play Store installed.

# Please Note, Test using the Google Play Store
* In-app reviews require your app to be published in Play Store. However, you can test your integration without publishing your app to production using either internal test tracks or internal app sharing.
