# com.ayriaplatform.apg.Api.PaymentApi

All URIs are relative to *https://api.ayria.club/apg/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetPaymentByReferenceCode**](PaymentApi.md#getpaymentbyreferencecode) | **GET** /get/{referenceCode} | Find payment with referenceCode
[**PaymentCancel**](PaymentApi.md#paymentcancel) | **POST** /cancel | Cancel a  payment
[**PaymentCreate**](PaymentApi.md#paymentcreate) | **POST** /create | Add a new payment



## GetPaymentByReferenceCode

> AyriaPaymentV1DTO GetPaymentByReferenceCode (string referenceCode)

Find payment with referenceCode

Returns a single payment

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using com.ayriaplatform.apg.Api;
using com.ayriaplatform.apg.Client;
using com.ayriaplatform.apg.Model;

namespace Example
{
    public class GetPaymentByReferenceCodeExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "https://api.ayria.club/apg/v1";
            // Configure API key authorization: APG-API-KEY
            Configuration.Default.AddApiKey("APG-API-KEY", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("APG-API-KEY", "Bearer");

            var apiInstance = new PaymentApi(Configuration.Default);
            var referenceCode = referenceCode_example;  // string | ReferenceCode of payment to return

            try
            {
                // Find payment with referenceCode
                AyriaPaymentV1DTO result = apiInstance.GetPaymentByReferenceCode(referenceCode);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PaymentApi.GetPaymentByReferenceCode: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **referenceCode** | **string**| ReferenceCode of payment to return | 

### Return type

[**AyriaPaymentV1DTO**](AyriaPaymentV1DTO.md)

### Authorization

[APG-API-KEY](../README.md#APG-API-KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |
| **400** | Invalid Reference code supplied |  -  |
| **404** | Payment not found |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PaymentCancel

> AyriaPaymentV1DTO PaymentCancel (AyriaPaymentV1CancelCommand ayriaPaymentV1CancelCommand = null)

Cancel a  payment

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using com.ayriaplatform.apg.Api;
using com.ayriaplatform.apg.Client;
using com.ayriaplatform.apg.Model;

namespace Example
{
    public class PaymentCancelExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "https://api.ayria.club/apg/v1";
            // Configure API key authorization: APG-API-KEY
            Configuration.Default.AddApiKey("APG-API-KEY", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("APG-API-KEY", "Bearer");

            var apiInstance = new PaymentApi(Configuration.Default);
            var ayriaPaymentV1CancelCommand = new AyriaPaymentV1CancelCommand(); // AyriaPaymentV1CancelCommand |  (optional) 

            try
            {
                // Cancel a  payment
                AyriaPaymentV1DTO result = apiInstance.PaymentCancel(ayriaPaymentV1CancelCommand);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PaymentApi.PaymentCancel: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ayriaPaymentV1CancelCommand** | [**AyriaPaymentV1CancelCommand**](AyriaPaymentV1CancelCommand.md)|  | [optional] 

### Return type

[**AyriaPaymentV1DTO**](AyriaPaymentV1DTO.md)

### Authorization

[APG-API-KEY](../README.md#APG-API-KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |
| **400** | Bad request - payment is either canceled already or paid |  -  |
| **404** | Not found |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PaymentCreate

> AyriaPaymentV1DTO PaymentCreate (AyriaPaymentV1Command ayriaPaymentV1Command = null)

Add a new payment

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using com.ayriaplatform.apg.Api;
using com.ayriaplatform.apg.Client;
using com.ayriaplatform.apg.Model;

namespace Example
{
    public class PaymentCreateExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "https://api.ayria.club/apg/v1";
            // Configure API key authorization: APG-API-KEY
            Configuration.Default.AddApiKey("APG-API-KEY", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("APG-API-KEY", "Bearer");

            var apiInstance = new PaymentApi(Configuration.Default);
            var ayriaPaymentV1Command = new AyriaPaymentV1Command(); // AyriaPaymentV1Command |  (optional) 

            try
            {
                // Add a new payment
                AyriaPaymentV1DTO result = apiInstance.PaymentCreate(ayriaPaymentV1Command);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PaymentApi.PaymentCreate: " + e.Message );
                Debug.Print("Status Code: "+ e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ayriaPaymentV1Command** | [**AyriaPaymentV1Command**](AyriaPaymentV1Command.md)|  | [optional] 

### Return type

[**AyriaPaymentV1DTO**](AyriaPaymentV1DTO.md)

### Authorization

[APG-API-KEY](../README.md#APG-API-KEY)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | successful operation |  -  |
| **400** | Bad request |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

