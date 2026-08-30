# OPay Android — SDK integration and deep link notes

Updated the Android sample with a more complete integration guide and example pseudocode for using the OPay Android SDK. The project still contains placeholder SDK coordinates — replace with the exact artifact and initialization per OPay docs.

What I added
- README expanded with SDK integration steps, callback intent-filter example, and testing notes.
- Example deep link / redirect intent-filter in AndroidManifest (commented).

Key steps to finish mobile integration
1. Add the official OPay Android SDK dependency in app/build.gradle.
2. Ensure your backend returns a payment token or checkout_url when creating orders.
3. Call the SDK with the token from the Android app and handle callbacks via intent or SDK callback.
4. Configure AndroidManifest intent-filter if SDK uses deep links.
5. Test using ngrok and sandbox keys.

Sample intent-filter (place inside activity element in AndroidManifest.xml):

<!--
<intent-filter>
    <action android:name="android.intent.action.VIEW" />
    <category android:name="android.intent.category.DEFAULT" />
    <category android:name="android.intent.category.BROWSABLE" />
    <data android:scheme="opay" android:host="callback" android:pathPrefix="/payment" />
</intent-filter>
-->

Replace scheme/host/pathPrefix based on OPay SDK docs.
