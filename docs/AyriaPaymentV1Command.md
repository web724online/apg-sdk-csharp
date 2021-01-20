
# Com.AyriaPlatform.APG.Model.AyriaPaymentV1Command

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ReferralCode** | **long** | Payee referral code | 
**Amount** | **long** | Total price in Riyal currency | 
**PayerMobile** | **string** | Payer mobile number | 
**PayerName** | **string** | Payer name | [optional] 
**Description** | **string** | Description for payment | [optional] 
**PaymentNumber** | **string** | Payment number (external) | [optional] 
**ExtraData** | **string** | Extra data related to payment | [optional] 
**IssuerMustVerifyPayment** | **bool** | Set it to &#39;true&#39; if you want to verify payment | [optional] 
**CallbackUrl** | **string** | Useful for when you want to have dynamic callback url | [optional] 
**Kalas** | [**List&lt;AyriaPaymentV1KalaDTO&gt;**](AyriaPaymentV1KalaDTO.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to README]](../README.md)

