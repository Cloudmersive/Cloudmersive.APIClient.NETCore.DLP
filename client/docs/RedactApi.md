# Cloudmersive.APIClient.NETCore.DLP.Api.RedactApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**RedactAudio**](RedactApi.md#redactaudio) | **POST** /dlp/redact/audio | Redact User Data in Audio File
[**RedactAudioAdvanced**](RedactApi.md#redactaudioadvanced) | **POST** /dlp/redact/audio/advanced | Redact User Data in Audio File (Advanced)
[**RedactDocument**](RedactApi.md#redactdocument) | **POST** /dlp/redact/document | Redact User Data in Document
[**RedactDocumentAdvanced**](RedactApi.md#redactdocumentadvanced) | **POST** /dlp/redact/document/advanced | Redact User Data in Document (Advanced)
[**RedactText**](RedactApi.md#redacttext) | **POST** /dlp/redact/text | Redact User Data in Input Text
[**RedactTextAdvanced**](RedactApi.md#redacttextadvanced) | **POST** /dlp/redact/text/advanced | Redact User Data in Input Text (Advanced)


<a name="redactaudio"></a>
# **RedactAudio**
> DlpAudioRedactionResponse RedactAudio (DlpAudioRedactionRequest body = null)

Redact User Data in Audio File

Transcribes an audio file (WAV, MP3, M4A, FLAC, OGG, WMA), detects 23 configurable types of user data in the transcript, and redacts audio segments containing PII. Returns the redacted audio, redacted transcript, detection results, and redacted segment timestamps.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class RedactAudioExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new RedactApi();
            var body = new DlpAudioRedactionRequest(); // DlpAudioRedactionRequest | Input request (optional) 

            try
            {
                // Redact User Data in Audio File
                DlpAudioRedactionResponse result = apiInstance.RedactAudio(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RedactApi.RedactAudio: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpAudioRedactionRequest**](DlpAudioRedactionRequest.md)| Input request | [optional] 

### Return type

[**DlpAudioRedactionResponse**](DlpAudioRedactionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="redactaudioadvanced"></a>
# **RedactAudioAdvanced**
> DlpAdvancedAudioRedactionResponse RedactAudioAdvanced (DlpAdvancedAudioRedactionRequest body = null)

Redact User Data in Audio File (Advanced)

Transcribes an audio file (WAV, MP3, M4A, FLAC, OGG, WMA), detects 34 configurable types of user data including health-related PHI in the transcript, and redacts audio segments containing PII. Returns the redacted audio, redacted transcript, detection results, redacted segment timestamps, and optional rationale.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class RedactAudioAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new RedactApi();
            var body = new DlpAdvancedAudioRedactionRequest(); // DlpAdvancedAudioRedactionRequest | Input request (optional) 

            try
            {
                // Redact User Data in Audio File (Advanced)
                DlpAdvancedAudioRedactionResponse result = apiInstance.RedactAudioAdvanced(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RedactApi.RedactAudioAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpAdvancedAudioRedactionRequest**](DlpAdvancedAudioRedactionRequest.md)| Input request | [optional] 

### Return type

[**DlpAdvancedAudioRedactionResponse**](DlpAdvancedAudioRedactionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="redactdocument"></a>
# **RedactDocument**
> DlpDocumentRedactionResponse RedactDocument (DlpDocumentRedactionRequest body = null)

Redact User Data in Document

Detects and redacts configurable types of user data in a document (PDF, DOC, DOCX, XLS, XLSX, PPT, PPTX, HTML, EML, MSG, PNG, JPG, WEBP) using Advanced AI. Rasterizes document pages, detects PII regions using a grid-overlay approach, blurs those regions, and returns a rasterized PDF.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class RedactDocumentExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new RedactApi();
            var body = new DlpDocumentRedactionRequest(); // DlpDocumentRedactionRequest | Input request (optional) 

            try
            {
                // Redact User Data in Document
                DlpDocumentRedactionResponse result = apiInstance.RedactDocument(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RedactApi.RedactDocument: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpDocumentRedactionRequest**](DlpDocumentRedactionRequest.md)| Input request | [optional] 

### Return type

[**DlpDocumentRedactionResponse**](DlpDocumentRedactionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="redactdocumentadvanced"></a>
# **RedactDocumentAdvanced**
> DlpAdvancedDocumentRedactionResponse RedactDocumentAdvanced (DlpAdvancedDocumentRedactionRequest body = null)

Redact User Data in Document (Advanced)

Detects and redacts 35 configurable types of user data including health-related PHI in a document (PDF, DOC, DOCX, XLS, XLSX, PPT, PPTX, HTML, EML, MSG, PNG, JPG, WEBP) using Advanced AI. Rasterizes document pages, detects PII regions using a row-overlay approach, redacts those regions, and returns a rasterized PDF.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class RedactDocumentAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new RedactApi();
            var body = new DlpAdvancedDocumentRedactionRequest(); // DlpAdvancedDocumentRedactionRequest | Input request (optional) 

            try
            {
                // Redact User Data in Document (Advanced)
                DlpAdvancedDocumentRedactionResponse result = apiInstance.RedactDocumentAdvanced(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RedactApi.RedactDocumentAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpAdvancedDocumentRedactionRequest**](DlpAdvancedDocumentRedactionRequest.md)| Input request | [optional] 

### Return type

[**DlpAdvancedDocumentRedactionResponse**](DlpAdvancedDocumentRedactionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="redacttext"></a>
# **RedactText**
> DlpRedactionResponse RedactText (DlpRedactionRequest body = null)

Redact User Data in Input Text

Detects and redacts configurable types of user data in an input text string using Advanced AI. First detects PII, then redacts disallowed types by either deleting them or replacing them with asterisks.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class RedactTextExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new RedactApi();
            var body = new DlpRedactionRequest(); // DlpRedactionRequest | Input request (optional) 

            try
            {
                // Redact User Data in Input Text
                DlpRedactionResponse result = apiInstance.RedactText(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RedactApi.RedactText: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpRedactionRequest**](DlpRedactionRequest.md)| Input request | [optional] 

### Return type

[**DlpRedactionResponse**](DlpRedactionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="redacttextadvanced"></a>
# **RedactTextAdvanced**
> DlpAdvancedRedactionResponse RedactTextAdvanced (DlpAdvancedRedactionRequest body = null)

Redact User Data in Input Text (Advanced)

Detects and redacts 34 configurable types of user data including health-related PHI in an input text string using Advanced AI. First detects PII, then redacts disallowed types by either deleting them or replacing them with asterisks.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class RedactTextAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new RedactApi();
            var body = new DlpAdvancedRedactionRequest(); // DlpAdvancedRedactionRequest | Input request (optional) 

            try
            {
                // Redact User Data in Input Text (Advanced)
                DlpAdvancedRedactionResponse result = apiInstance.RedactTextAdvanced(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling RedactApi.RedactTextAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpAdvancedRedactionRequest**](DlpAdvancedRedactionRequest.md)| Input request | [optional] 

### Return type

[**DlpAdvancedRedactionResponse**](DlpAdvancedRedactionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

