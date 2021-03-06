---
layout: "v2_fluid/docs_base"
version: "2.1.1"
versionHref: "/docs/v2/native"
path: ""
category: native
id: "paypal"
title: "PayPal"
header_sub_title: "Class in module "
doc: "PayPal"
docType: "class"
---







<h1 class="api-title">
  
  PayPal
  

  

  

</h1>

<a class="improve-v2-docs" href="http://github.com/driftyco/ionic-native/edit/master/src/plugins/pay-pal.ts#L0">
  Improve this doc
</a>



<!-- decorators -->


<pre><code>$ ionic plugin add com.paypal.cordova.mobilesdk</code></pre>
<p>Repo:
  <a href="https://github.com/paypal/PayPal-Cordova-Plugin">
    https://github.com/paypal/PayPal-Cordova-Plugin
  </a>
</p>

<!-- description -->

<p>PayPal plugin for Cordova/Ionic Applications</p>



<!-- @usage tag -->

<h2>Usage</h2>

<pre><code>import {PayPal} from &#39;ionic-native&#39;;

PayPal.init({
     &quot;PayPalEnvironmentProduction&quot;: &quot;YOUR_PRODUCTION_CLIENT_ID&quot;,
       &quot;PayPalEnvironmentSandbox&quot;: &quot;YOUR_SANDBOX_CLIENT_ID&quot;
       })
  .then(onSuccess)
  .catch(onError);
</code></pre>




<!-- @property tags -->


<h2>Static Members</h2>

<div id="init"></div>
<h3><code>init(environment:,&nbsp;configuration:)</code>
  
</h3>


You must preconnect to PayPal to prepare the device for processing payments.
This improves the user experience, by making the presentation of the
UI faster. The preconnect is valid for a limited time, so
the recommended time to preconnect is on page load.



<table class="table param-table" style="margin:0;">
  <thead>
  <tr>
    <th>Param</th>
    <th>Type</th>
    <th>Details</th>
  </tr>
  </thead>
  <tbody>
  
  <tr>
    <td>
      environment:
      
      
    </td>
    <td>
      
<code>String</code>
    </td>
    <td>
      <p>available options are &quot;PayPalEnvironmentNoNetwork&quot;, &quot;PayPalEnvironmentProduction&quot; and &quot;PayPalEnvironmentSandbox&quot;</p>

      
    </td>
  </tr>
  
  <tr>
    <td>
      configuration:
      
      
    </td>
    <td>
      
<code>PayPalConfiguration</code>
    </td>
    <td>
      <p>For Future Payments merchantName, merchantPrivacyPolicyURL and merchantUserAgreementURL must be set be set</p>

      
    </td>
  </tr>
  
  </tbody>
</table>







<div id="version"></div>
<h3><code>version()</code>
  
</h3>


Retreive the version of PayPal iOS SDK Library.










<div id="renderSinglePaymentUI"></div>
<h3><code>renderSinglePaymentUI(payment:)</code>
  
</h3>


Start PayPal UI to collect payment from the user.
See https://developer.paypal.com/webapps/developer/docs/integration/mobile/ios-integration-guide/
for more documentation of the params.



<table class="table param-table" style="margin:0;">
  <thead>
  <tr>
    <th>Param</th>
    <th>Type</th>
    <th>Details</th>
  </tr>
  </thead>
  <tbody>
  
  <tr>
    <td>
      payment:
      
      
    </td>
    <td>
      
<code>PayPalPayment</code>
    </td>
    <td>
      <p>PayPalPayment object</p>

      
    </td>
  </tr>
  
  </tbody>
</table>







<div id="clientMetadataID"></div>
<h3><code>clientMetadataID()</code>
  
</h3>


Once a user has consented to future payments, when the user subsequently initiates a PayPal payment
from their device to be completed by your server, PayPal uses a Correlation ID to verify that the
payment is originating from a valid, user-consented device+application.
This helps reduce fraud and decrease declines.
This method MUST be called prior to initiating a pre-consented payment (a "future payment") from a mobile device.
Pass the result to your server, to include in the payment request sent to PayPal.
Do not otherwise cache or store this value.










<div id="renderFuturePaymentUI"></div>
<h3><code>renderFuturePaymentUI()</code>
  
</h3>


Please Read Docs on Future Payments at https://github.com/paypal/PayPal-iOS-SDK#future-payments










<div id="renderProfileSharingUI"></div>
<h3><code>renderProfileSharingUI(scopes:)</code>
  
</h3>


Please Read Docs on Profile Sharing at https://github.com/paypal/PayPal-iOS-SDK#profile-sharing



<table class="table param-table" style="margin:0;">
  <thead>
  <tr>
    <th>Param</th>
    <th>Type</th>
    <th>Details</th>
  </tr>
  </thead>
  <tbody>
  
  <tr>
    <td>
      scopes:
      
      
    </td>
    <td>
      
<code>Array&lt;string&gt;</code>
    </td>
    <td>
      <p>scopes Set of requested scope-values. Accepted scopes are: openid, profile, address, email, phone, futurepayments and paypalattributes
See <a href="https://developer.paypal.com/docs/integration/direct/identity/attributes/">https://developer.paypal.com/docs/integration/direct/identity/attributes/</a> for more details</p>

      
    </td>
  </tr>
  
  </tbody>
</table>








<!-- methods on the class -->



<!-- other classes -->

<!-- end other classes -->

<!-- interfaces -->

<h2><a class="anchor" name="interfaces" href="#interfaces"></a>Interfaces</h2>


<h3><a class="anchor" name="PayPalEnvironment" href="#PayPalEnvironment"></a>PayPalEnvironment</h3>


<table class="table param-table" style="margin:0;">
  <thead>
  <tr>
    <th>Param</th>
    <th>Type</th>
    <th>Details</th>
  </tr>
  </thead>
  <tbody>
  
  <tr>
    <td>
      PayPalEnvironmentProduction
      
    </td>
    <td>
      string
    </td>
    <td>
      
    </td>
  </tr>
  
  <tr>
    <td>
      PayPalEnvironmentSandbox
      
    </td>
    <td>
      string
    </td>
    <td>
      
    </td>
  </tr>
  
  </tbody>
</table>




<h3><a class="anchor" name="PayPalPayment" href="#PayPalPayment"></a>PayPalPayment</h3>


<table class="table param-table" style="margin:0;">
  <thead>
  <tr>
    <th>Param</th>
    <th>Type</th>
    <th>Details</th>
  </tr>
  </thead>
  <tbody>
  
  <tr>
    <td>
      amount
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>The amount of the payment.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      currencyCode
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>The ISO 4217 currency for the payment.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      shortDescription
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>A short description of the payment.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      intent
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>&quot;Sale&quot; for an immediate payment.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      bnCode
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Optional Build Notation code (&quot;BN code&quot;), obtained from partnerprogram@paypal.com,
for your tracking purposes.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      invoiceNumber
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Optional invoice number, for your tracking purposes. (up to 256 characters)</p>

    </td>
  </tr>
  
  <tr>
    <td>
      custom
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Optional text, for your tracking purposes. (up to 256 characters)</p>

    </td>
  </tr>
  
  <tr>
    <td>
      softDescriptor
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Optional text which will appear on the customer&#39;s credit card statement. (up to 22 characters)</p>

    </td>
  </tr>
  
  <tr>
    <td>
      items
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Optional array of PayPalItem objects.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      shippingAddress
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Optional customer shipping address, if your app wishes to provide this to the SDK.</p>

    </td>
  </tr>
  
  </tbody>
</table>




<h3><a class="anchor" name="PayPAlItem" href="#PayPAlItem"></a>PayPAlItem</h3>




<h3><a class="anchor" name="PayPalPaymentDetails" href="#PayPalPaymentDetails"></a>PayPalPaymentDetails</h3>


<table class="table param-table" style="margin:0;">
  <thead>
  <tr>
    <th>Param</th>
    <th>Type</th>
    <th>Details</th>
  </tr>
  </thead>
  <tbody>
  
  <tr>
    <td>
      subtotal
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Sub-total (amount) of items being paid for. 10 characters max with support for 2 decimal places.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      shipping
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Amount charged for shipping. 10 characters max with support for 2 decimal places.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      tax
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Amount charged for tax. 10 characters max with support for 2 decimal places.</p>

    </td>
  </tr>
  
  </tbody>
</table>




<h3><a class="anchor" name="PayPalConfigurationOptions" href="#PayPalConfigurationOptions"></a>PayPalConfigurationOptions</h3>


<table class="table param-table" style="margin:0;">
  <thead>
  <tr>
    <th>Param</th>
    <th>Type</th>
    <th>Details</th>
  </tr>
  </thead>
  <tbody>
  
  <tr>
    <td>
      defaultUserEmail
      <div><em>(optional)</em></div>
    </td>
    <td>
      string
    </td>
    <td>
      <p>Will be overridden by email used in most recent PayPal login.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      defaultUserPhoneCountryCode
      <div><em>(optional)</em></div>
    </td>
    <td>
      string
    </td>
    <td>
      <p>Will be overridden by phone country code used in most recent PayPal login</p>

    </td>
  </tr>
  
  <tr>
    <td>
      defaultUserPhoneNumber
      <div><em>(optional)</em></div>
    </td>
    <td>
      string
    </td>
    <td>
      <p>Will be overridden by phone number used in most recent PayPal login.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      merchantName
      <div><em>(optional)</em></div>
    </td>
    <td>
      string
    </td>
    <td>
      <p>Your company name, as it should be displayed to the user when requesting consent via a PayPalFuturePaymentViewController.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      merchantPrivacyPolicyUrl
      <div><em>(optional)</em></div>
    </td>
    <td>
      string
    </td>
    <td>
      <p>URL of your company&#39;s privacy policy, which will be offered to the user when requesting consent via a PayPalFuturePaymentViewController.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      merchantUserAgreementUrl
      <div><em>(optional)</em></div>
    </td>
    <td>
      string
    </td>
    <td>
      <p>URL of your company&#39;s user agreement, which will be offered to the user when requesting consent via a PayPalFuturePaymentViewController.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      acceptCreditCards
      <div><em>(optional)</em></div>
    </td>
    <td>
      boolean
    </td>
    <td>
      <p>If set to NO, the SDK will only support paying with PayPal, not with credit cards.
This applies only to single payments (via PayPalPaymentViewController).
Future payments (via PayPalFuturePaymentViewController) always use PayPal.
Defaults to true</p>

    </td>
  </tr>
  
  <tr>
    <td>
      payPalShippingAddressOption
      <div><em>(optional)</em></div>
    </td>
    <td>
      number
    </td>
    <td>
      <p>For single payments, options for the shipping address.</p>
<ul>
<li>0 - PayPalShippingAddressOptionNone: no shipping address applies.</li>
<li>1 - PayPalShippingAddressOptionProvided: shipping address will be provided by your app,
in the shippingAddress property of PayPalPayment.</li>
<li>2 - PayPalShippingAddressOptionPayPal: user will choose from shipping addresses on file
for their PayPal account.</li>
<li>3 - PayPalShippingAddressOptionBoth: user will choose from the shipping address provided by your app,
in the shippingAddress property of PayPalPayment, plus the shipping addresses on file for the user&#39;s PayPal account.
Defaults to 0 (PayPalShippingAddressOptionNone).</li>
</ul>

    </td>
  </tr>
  
  <tr>
    <td>
      rememberUser
      <div><em>(optional)</em></div>
    </td>
    <td>
      boolean
    </td>
    <td>
      <p>If set to YES, then if the user pays via their PayPal account,
the SDK will remember the user&#39;s PayPal username or phone number;
if the user pays via their credit card, then the SDK will remember
the PayPal Vault token representing the user&#39;s credit card.</p>
<p>If set to NO, then any previously-remembered username, phone number, or
credit card token will be erased, and subsequent payment information will
not be remembered.</p>
<p>Defaults to YES.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      languageOrLocale
      <div><em>(optional)</em></div>
    </td>
    <td>
      string
    </td>
    <td>
      <p>If not set, or if set to nil, defaults to the device&#39;s current language setting.</p>
<p>Can be specified as a language code (&quot;en&quot;, &quot;fr&quot;, &quot;zh-Hans&quot;, etc.) or as a locale (&quot;en_AU&quot;, &quot;fr_FR&quot;, &quot;zh-Hant_HK&quot;, etc.).
If the library does not contain localized strings for a specified locale, then will fall back to the language. E.g., &quot;es_CO&quot; -&gt; &quot;es&quot;.
If the library does not contain localized strings for a specified language, then will fall back to American English.</p>
<p>If you specify only a language code, and that code matches the device&#39;s currently preferred language,
then the library will attempt to use the device&#39;s current region as well.
E.g., specifying &quot;en&quot; on a device set to &quot;English&quot; and &quot;United Kingdom&quot; will result in &quot;en_GB&quot;.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      disableBlurWhenBackgrounding
      <div><em>(optional)</em></div>
    </td>
    <td>
      boolean
    </td>
    <td>
      <p>Normally, the SDK blurs the screen when the app is backgrounded,
to obscure credit card or PayPal account details in the iOS-saved screenshot.
If your app already does its own blurring upon backgrounding, you might choose to disable this.
Defaults to NO.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      presentingInPopover
      <div><em>(optional)</em></div>
    </td>
    <td>
      boolean
    </td>
    <td>
      <p>If you will present the SDK&#39;s view controller within a popover, then set this property to YES.
Defaults to NO. (iOS only)</p>

    </td>
  </tr>
  
  <tr>
    <td>
      forceDefaultsInSandbox
      <div><em>(optional)</em></div>
    </td>
    <td>
      boolean
    </td>
    <td>
      <p>Sandbox credentials can be difficult to type on a mobile device. Setting this flag to YES will
cause the sandboxUserPassword and sandboxUserPin to always be pre-populated into login fields.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      sandboxUserPassword
      <div><em>(optional)</em></div>
    </td>
    <td>
      string
    </td>
    <td>
      <p>Password to use for sandbox if &#39;forceDefaultsInSandbox&#39; is set.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      sandboxUserPin
      <div><em>(optional)</em></div>
    </td>
    <td>
      string
    </td>
    <td>
      <p>PIN to use for sandbox if &#39;forceDefaultsInSandbox&#39; is set.</p>

    </td>
  </tr>
  
  </tbody>
</table>




<h3><a class="anchor" name="PayPalShippingAddress" href="#PayPalShippingAddress"></a>PayPalShippingAddress</h3>


<table class="table param-table" style="margin:0;">
  <thead>
  <tr>
    <th>Param</th>
    <th>Type</th>
    <th>Details</th>
  </tr>
  </thead>
  <tbody>
  
  <tr>
    <td>
      recipientName
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Name of the recipient at this address. 50 characters max.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      line1
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Line 1 of the address (e.g., Number, street, etc). 100 characters max.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      line2
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>Line 2 of the address (e.g., Suite, apt #, etc). 100 characters max. Optional.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      city
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>City name. 50 characters max.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      state
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>2-letter code for US states, and the equivalent for other countries. 100 characters max. Required in certain countries.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      postalCode
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>ZIP code or equivalent is usually required for countries that have them. 20 characters max. Required in certain countries.</p>

    </td>
  </tr>
  
  <tr>
    <td>
      countryCode
      
    </td>
    <td>
      string
    </td>
    <td>
      <p>2-letter country code. 2 characters max.</p>

    </td>
  </tr>
  
  </tbody>
</table>





<!-- end interfaces -->

<!-- related link --><!-- end content block -->


<!-- end body block -->

