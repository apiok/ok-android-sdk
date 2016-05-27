Join our chat on the app: Telegram Messenger, https://telegram.me/joinchat/AAK8BAdKmiij41ce8IT33w 

ok-android-sdk
-------
Android SDK and sample for native apps integrated with OK.RU


Application Requirements
-------
An application registered within OK platform should have:

1. Target platform checked (like ANDROID or IOS)
2. EXTERNAL platform checked
3. Client OAUTH checkbox checked
4. A VALUABLE_ACCESS permission being checked or requested
5. (recommended) LONG_ACCESS_TOKEN permission requested from [api-support](mailto:api-support@ok.ru) in order to be able to use tokens with long ttl
6. A redirect url configured in application settings including okauth://ok12345 where 12345 is your application id on OK platform


Quick Start
-------
A quick-start with login and viral widgets is available in [example](https://github.com/odnoklassniki/ok-android-sdk/tree/master/odnoklassniki-android-sdk-example)

Note that you should also register a schema okauth://ok23346346 within your [manifest](https://github.com/odnoklassniki/ok-android-sdk/blob/master/odnoklassniki-android-sdk-example/src/main/AndroidManifest.xml#L39) where 23346346 is application id in order to native sso login to work properly.

FAQ
-------
+ Method sdk.getInstallSource does not return correct value.
  - Probably you have not bundled your application with *com.google.android.gms:play-services-ads* library that is required to get advertising id that is used to track application installation.
