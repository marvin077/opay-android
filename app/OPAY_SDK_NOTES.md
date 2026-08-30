## OPay Android SDK Integration

This file includes a short example of how your Android app should call the backend and hand a returned token to the OPay SDK.

Pseudocode (replace with actual SDK calls):

// After creating the order on your backend and receiving a payment token:
// val token = responseJson.getString("payment_token")
// Initialize SDK (example)
// val opay = OPaySdk.getInstance(context, OPAY_SANDBOX_KEY)
// opay.startCheckout(token, object: OPayCallback {
//   override fun onSuccess(result: PaymentResult) { /* inform backend or update UI */ }
//   override fun onFailure(error: OPayError) { /* handle error */ }
// })
