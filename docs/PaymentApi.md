# Com.AyriaPlatform.APG.Api.PaymentApi

All URIs are relative to *https://api.ayria.club/apg/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetPaymentByReferenceCode**](PaymentApi.md#getpaymentbyreferencecode) | **GET** /get/{referenceCode} | Find payment with referenceCode
[**GetPayments**](PaymentApi.md#getpayments) | **GET** /list | List of payments between given dates
[**PaymentCancel**](PaymentApi.md#paymentcancel) | **POST** /cancel | Cancel a  payment
[**PaymentCreate**](PaymentApi.md#paymentcreate) | **POST** /create | Add a new payment
[**VerifyPaymentByReferenceCode**](PaymentApi.md#verifypaymentbyreferencecode) | **POST** /verify/{referenceCode} | Verify payment with referenceCode



## GetPaymentByReferenceCode

> AyriaPaymentV1DTO GetPaymentByReferenceCode (string APG_WALLET_ID, string referenceCode)

Find payment with referenceCode

Returns a single payment

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Com.AyriaPlatform.APG.Api;
using Com.AyriaPlatform.APG.Client;
using Com.AyriaPlatform.APG.Model;

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
            var APG_WALLET_ID = APG_WALLET_ID_example;  // string | 
            var referenceCode = referenceCode_example;  // string | ReferenceCode of payment to return

            try
            {
                // Find payment with referenceCode
                AyriaPaymentV1DTO result = apiInstance.GetPaymentByReferenceCode(APG_WALLET_ID, referenceCode);
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
 **APG_WALLET_ID** | **string**|  | 
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


## GetPayments

> List&lt;AyriaPaymentV1DTO&gt; GetPayments (string APG_WALLET_ID, string page = null, string size = null, string sort = null, string createdDateGreaterThan = null, string createdDateToLessThanOrEqual = null)

List of payments between given dates

Returns a payment list

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Com.AyriaPlatform.APG.Api;
using Com.AyriaPlatform.APG.Client;
using Com.AyriaPlatform.APG.Model;

namespace Example
{
    public class GetPaymentsExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "https://api.ayria.club/apg/v1";
            // Configure API key authorization: APG-API-KEY
            Configuration.Default.AddApiKey("APG-API-KEY", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("APG-API-KEY", "Bearer");

            var apiInstance = new PaymentApi(Configuration.Default);
            var APG_WALLET_ID = APG_WALLET_ID_example;  // string | 
            var page = page_example;  // string | Page number (optional) 
            var size = size_example;  // string | Page size (optional) 
            var sort = sort_example;  // string | Sort column and direction (optional) 
            var createdDateGreaterThan = createdDateGreaterThan_example;  // string | Created date greater than (optional) 
            var createdDateToLessThanOrEqual = createdDateToLessThanOrEqual_example;  // string | Created date less than or equal (optional) 

            try
            {
                // List of payments between given dates
                List<AyriaPaymentV1DTO> result = apiInstance.GetPayments(APG_WALLET_ID, page, size, sort, createdDateGreaterThan, createdDateToLessThanOrEqual);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PaymentApi.GetPayments: " + e.Message );
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
 **APG_WALLET_ID** | **string**|  | 
 **page** | **string**| Page number | [optional] 
 **size** | **string**| Page size | [optional] 
 **sort** | **string**| Sort column and direction | [optional] 
 **createdDateGreaterThan** | **string**| Created date greater than | [optional] 
 **createdDateToLessThanOrEqual** | **string**| Created date less than or equal | [optional] 

### Return type

[**List&lt;AyriaPaymentV1DTO&gt;**](AyriaPaymentV1DTO.md)

### Authorization

[APG-API-KEY](../README.md#APG-API-KEY)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |

[[Back to top]](#)
[[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PaymentCancel

> AyriaPaymentV1DTO PaymentCancel (string APG_WALLET_ID, AyriaPaymentV1CancelCommand ayriaPaymentV1CancelCommand = null)

Cancel a  payment

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Com.AyriaPlatform.APG.Api;
using Com.AyriaPlatform.APG.Client;
using Com.AyriaPlatform.APG.Model;

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
            var APG_WALLET_ID = APG_WALLET_ID_example;  // string | 
            var ayriaPaymentV1CancelCommand = new AyriaPaymentV1CancelCommand(); // AyriaPaymentV1CancelCommand |  (optional) 

            try
            {
                // Cancel a  payment
                AyriaPaymentV1DTO result = apiInstance.PaymentCancel(APG_WALLET_ID, ayriaPaymentV1CancelCommand);
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
 **APG_WALLET_ID** | **string**|  | 
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

> AyriaPaymentV1DTO PaymentCreate (string APG_WALLET_ID, AyriaPaymentV1Command ayriaPaymentV1Command = null)

Add a new payment

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Com.AyriaPlatform.APG.Api;
using Com.AyriaPlatform.APG.Client;
using Com.AyriaPlatform.APG.Model;

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
            var APG_WALLET_ID = APG_WALLET_ID_example;  // string | 
            var ayriaPaymentV1Command = new AyriaPaymentV1Command(); // AyriaPaymentV1Command |  (optional) 

            try
            {
                // Add a new payment
                AyriaPaymentV1DTO result = apiInstance.PaymentCreate(APG_WALLET_ID, ayriaPaymentV1Command);
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
 **APG_WALLET_ID** | **string**|  | 
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


## VerifyPaymentByReferenceCode

> AyriaPaymentV1DTO VerifyPaymentByReferenceCode (string APG_WALLET_ID, string referenceCode)

Verify payment with referenceCode

Returns a single payment

### Example

```csharp
using System.Collections.Generic;
using System.Diagnostics;
using Com.AyriaPlatform.APG.Api;
using Com.AyriaPlatform.APG.Client;
using Com.AyriaPlatform.APG.Model;

namespace Example
{
    public class VerifyPaymentByReferenceCodeExample
    {
        public static void Main()
        {
            Configuration.Default.BasePath = "https://api.ayria.club/apg/v1";
            // Configure API key authorization: APG-API-KEY
            Configuration.Default.AddApiKey("APG-API-KEY", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("APG-API-KEY", "Bearer");

            var apiInstance = new PaymentApi(Configuration.Default);
            var APG_WALLET_ID = APG_WALLET_ID_example;  // string | 
            var referenceCode = referenceCode_example;  // string | ReferenceCode of payment to verify

            try
            {
                // Verify payment with referenceCode
                AyriaPaymentV1DTO result = apiInstance.VerifyPaymentByReferenceCode(APG_WALLET_ID, referenceCode);
                Debug.WriteLine(result);
            }
            catch (ApiException e)
            {
                Debug.Print("Exception when calling PaymentApi.VerifyPaymentByReferenceCode: " + e.Message );
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
 **APG_WALLET_ID** | **string**|  | 
 **referenceCode** | **string**| ReferenceCode of payment to verify | 

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

