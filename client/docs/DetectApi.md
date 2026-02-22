# Cloudmersive.APIClient.NETCore.DLP.Api.DetectApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DetectDocument**](DetectApi.md#detectdocument) | **POST** /dlp/detect/document | Detect User Data in Document Image
[**DetectDocumentAdvanced**](DetectApi.md#detectdocumentadvanced) | **POST** /dlp/detect/document/advanced | Detect User Data in Document Image (Advanced)
[**DetectText**](DetectApi.md#detecttext) | **POST** /dlp/detect/text | Detect User Data in Input Text
[**DetectTextAdvanced**](DetectApi.md#detecttextadvanced) | **POST** /dlp/detect/text/advanced | Detect User Data in Input Text (Advanced)


<a name="detectdocument"></a>
# **DetectDocument**
> DlpDetectionResponse DetectDocument (DlpDocumentDetectionRequest body = null)

Detect User Data in Document Image

Detects configurable types of user data in a document image (PDF, DOCX, PNG, JPG) using Advanced AI.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class DetectDocumentExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new DetectApi();
            var body = new DlpDocumentDetectionRequest(); // DlpDocumentDetectionRequest | Input request (optional) 

            try
            {
                // Detect User Data in Document Image
                DlpDetectionResponse result = apiInstance.DetectDocument(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DetectApi.DetectDocument: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpDocumentDetectionRequest**](DlpDocumentDetectionRequest.md)| Input request | [optional] 

### Return type

[**DlpDetectionResponse**](DlpDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="detectdocumentadvanced"></a>
# **DetectDocumentAdvanced**
> DlpAdvancedDetectionResponse DetectDocumentAdvanced (DlpAdvancedDocumentDetectionRequest body = null)

Detect User Data in Document Image (Advanced)

Detects 29 configurable types of user data including health-related PHI in a document image (PDF, DOCX, PNG, JPG) using Advanced AI.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class DetectDocumentAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new DetectApi();
            var body = new DlpAdvancedDocumentDetectionRequest(); // DlpAdvancedDocumentDetectionRequest | Input request (optional) 

            try
            {
                // Detect User Data in Document Image (Advanced)
                DlpAdvancedDetectionResponse result = apiInstance.DetectDocumentAdvanced(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DetectApi.DetectDocumentAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpAdvancedDocumentDetectionRequest**](DlpAdvancedDocumentDetectionRequest.md)| Input request | [optional] 

### Return type

[**DlpAdvancedDetectionResponse**](DlpAdvancedDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="detecttext"></a>
# **DetectText**
> DlpDetectionResponse DetectText (DlpDetectionRequest body = null)

Detect User Data in Input Text

Detects configurable types of user data in an input text string using Advanced AI.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class DetectTextExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new DetectApi();
            var body = new DlpDetectionRequest(); // DlpDetectionRequest | Input request (optional) 

            try
            {
                // Detect User Data in Input Text
                DlpDetectionResponse result = apiInstance.DetectText(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DetectApi.DetectText: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpDetectionRequest**](DlpDetectionRequest.md)| Input request | [optional] 

### Return type

[**DlpDetectionResponse**](DlpDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="detecttextadvanced"></a>
# **DetectTextAdvanced**
> DlpAdvancedDetectionResponse DetectTextAdvanced (DlpAdvancedDetectionRequest body = null)

Detect User Data in Input Text (Advanced)

Detects 29 configurable types of user data including health-related PHI in an input text string using Advanced AI.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class DetectTextAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new DetectApi();
            var body = new DlpAdvancedDetectionRequest(); // DlpAdvancedDetectionRequest | Input request (optional) 

            try
            {
                // Detect User Data in Input Text (Advanced)
                DlpAdvancedDetectionResponse result = apiInstance.DetectTextAdvanced(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DetectApi.DetectTextAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpAdvancedDetectionRequest**](DlpAdvancedDetectionRequest.md)| Input request | [optional] 

### Return type

[**DlpAdvancedDetectionResponse**](DlpAdvancedDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

