
# Com.AyriaPlatform.APG.Model.AyriaPaymentV1DTO

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ReferralCode** | **long** | Payee referral code | [optional] 
**Amount** | **long** | Total price in Riyal currency | [optional] 
**PayerMobile** | **string** | Payer mobile number | [optional] 
**TrackingNumber** | **long** | Tracking number | [optional] 
**ReferenceCode** | **string** | Reference code | [optional] 
**PayeeName** | **string** | Payee name | [optional] 
**PayerName** | **string** | Payer name | [optional] 
**Description** | **string** | Description for payment | [optional] 
**ExtraData** | **string** | Extra data related to payment | [optional] 
**PaymentNumber** | **string** | Payment number (external) | [optional] 
**Paid** | **bool** | Payment paid status | [optional] 
**Canceled** | **bool** | Payment cancel status | [optional] 
**CreatedDate** | **string** | Create date of payment | [optional] 
**PaymentUrl** | **string** | Payment URL | [optional] 
**CancelDescription** | **string** | Cancel description | [optional] 
**IssuerMustVerifyPayment** | **bool** | If is &#39;true&#39; issuer must verify payment | [optional] 
**PaymentStatus** | **string** | Is usually DEFAULT, but can be WAITING_FOR_VERIFY or VERIFIED if issuerMustVerifyPayment is true | [optional] 
**CallbackUrl** | **string** | Callback url, if is null then default callback url will be used instead | [optional] 
**Kalas** | [**List&lt;AyriaPaymentV1KalaDTO&gt;**](AyriaPaymentV1KalaDTO.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to README]](../README.md)

