# Cloudmersive.APIClient.NETCore.DLP.Api.TasksBatchJobApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DetectAudioAdvancedBatchJob**](TasksBatchJobApi.md#detectaudioadvancedbatchjob) | **POST** /dlp/batch-job/detect/audio/advanced | Detect User Data in Audio File (Advanced) as a Batch Job
[**DetectAudioBatchJob**](TasksBatchJobApi.md#detectaudiobatchjob) | **POST** /dlp/batch-job/detect/audio | Detect User Data in Audio File as a Batch Job
[**GetAsyncJobStatus**](TasksBatchJobApi.md#getasyncjobstatus) | **GET** /dlp/batch-job/status | Get the status and result of a DLP Batch Job
[**RedactAudioAdvancedBatchJob**](TasksBatchJobApi.md#redactaudioadvancedbatchjob) | **POST** /dlp/batch-job/redact/audio/advanced | Redact User Data in Audio File (Advanced) as a Batch Job
[**RedactAudioBatchJob**](TasksBatchJobApi.md#redactaudiobatchjob) | **POST** /dlp/batch-job/redact/audio | Redact User Data in Audio File as a Batch Job


<a name="detectaudioadvancedbatchjob"></a>
# **DetectAudioAdvancedBatchJob**
> DlpBatchJobResult DetectAudioAdvancedBatchJob (DlpAdvancedAudioDetectionRequest body = null)

Detect User Data in Audio File (Advanced) as a Batch Job

Creates an async batch job for detecting user data in an audio file using Advanced detection.  Use the GetAsyncJobStatus API to check on the status of the job and retrieve the result when complete.  Transcribes an audio file (WAV, MP3, M4A, FLAC, OGG, WMA) and detects 29 configurable types of user data including health-related PHI in the transcript using Advanced AI. Returns the full transcript, token timestamps, detection results, and optional rationale.  Requires Managed Instance or Private Cloud deployment.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class DetectAudioAdvancedBatchJobExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new TasksBatchJobApi();
            var body = new DlpAdvancedAudioDetectionRequest(); // DlpAdvancedAudioDetectionRequest | Input request (optional) 

            try
            {
                // Detect User Data in Audio File (Advanced) as a Batch Job
                DlpBatchJobResult result = apiInstance.DetectAudioAdvancedBatchJob(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TasksBatchJobApi.DetectAudioAdvancedBatchJob: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpAdvancedAudioDetectionRequest**](DlpAdvancedAudioDetectionRequest.md)| Input request | [optional] 

### Return type

[**DlpBatchJobResult**](DlpBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="detectaudiobatchjob"></a>
# **DetectAudioBatchJob**
> DlpBatchJobResult DetectAudioBatchJob (DlpAudioDetectionRequest body = null)

Detect User Data in Audio File as a Batch Job

Creates an async batch job for detecting user data in an audio file.  Use the GetAsyncJobStatus API to check on the status of the job and retrieve the result when complete.  Transcribes an audio file (WAV, MP3, M4A, FLAC, OGG, WMA) and detects 23 configurable types of user data in the transcript using Advanced AI. Returns the full transcript, token timestamps, and detection results.  Requires Managed Instance or Private Cloud deployment.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class DetectAudioBatchJobExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new TasksBatchJobApi();
            var body = new DlpAudioDetectionRequest(); // DlpAudioDetectionRequest | Input request (optional) 

            try
            {
                // Detect User Data in Audio File as a Batch Job
                DlpBatchJobResult result = apiInstance.DetectAudioBatchJob(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TasksBatchJobApi.DetectAudioBatchJob: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DlpAudioDetectionRequest**](DlpAudioDetectionRequest.md)| Input request | [optional] 

### Return type

[**DlpBatchJobResult**](DlpBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getasyncjobstatus"></a>
# **GetAsyncJobStatus**
> DlpBatchJobStatusResult GetAsyncJobStatus (string asyncJobID = null)

Get the status and result of a DLP Batch Job

Returns the result of the Async Job - possible states can be STARTED or COMPLETED.  When COMPLETED, the corresponding result field (detection or redaction result) is populated on the response.  This API is only available for Cloudmersive Managed Instance and Private Cloud deployments.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class GetAsyncJobStatusExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new TasksBatchJobApi();
            var asyncJobID = asyncJobID_example;  // string | Job ID for the batch job to get the status of (optional) 

            try
            {
                // Get the status and result of a DLP Batch Job
                DlpBatchJobStatusResult result = apiInstance.GetAsyncJobStatus(asyncJobID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TasksBatchJobApi.GetAsyncJobStatus: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asyncJobID** | **string**| Job ID for the batch job to get the status of | [optional] 

### Return type

[**DlpBatchJobStatusResult**](DlpBatchJobStatusResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="redactaudioadvancedbatchjob"></a>
# **RedactAudioAdvancedBatchJob**
> DlpBatchJobResult RedactAudioAdvancedBatchJob (DlpAdvancedAudioRedactionRequest body = null)

Redact User Data in Audio File (Advanced) as a Batch Job

Creates an async batch job for redacting user data in an audio file using Advanced detection.  Use the GetAsyncJobStatus API to check on the status of the job and retrieve the redacted audio and transcript when complete.  Transcribes an audio file (WAV, MP3, M4A, FLAC, OGG, WMA), detects 34 configurable types of user data including health-related PHI in the transcript, and redacts audio segments containing PII. Returns the redacted audio, redacted transcript, detection results, redacted segment timestamps, and optional rationale.  Requires Managed Instance or Private Cloud deployment.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class RedactAudioAdvancedBatchJobExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new TasksBatchJobApi();
            var body = new DlpAdvancedAudioRedactionRequest(); // DlpAdvancedAudioRedactionRequest | Input request (optional) 

            try
            {
                // Redact User Data in Audio File (Advanced) as a Batch Job
                DlpBatchJobResult result = apiInstance.RedactAudioAdvancedBatchJob(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TasksBatchJobApi.RedactAudioAdvancedBatchJob: " + e.Message );
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

[**DlpBatchJobResult**](DlpBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="redactaudiobatchjob"></a>
# **RedactAudioBatchJob**
> DlpBatchJobResult RedactAudioBatchJob (DlpAudioRedactionRequest body = null)

Redact User Data in Audio File as a Batch Job

Creates an async batch job for redacting user data in an audio file.  Use the GetAsyncJobStatus API to check on the status of the job and retrieve the redacted audio and transcript when complete.  Transcribes an audio file (WAV, MP3, M4A, FLAC, OGG, WMA), detects 23 configurable types of user data in the transcript, and redacts audio segments containing PII. Returns the redacted audio, redacted transcript, detection results, and redacted segment timestamps.  Requires Managed Instance or Private Cloud deployment.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class RedactAudioBatchJobExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new TasksBatchJobApi();
            var body = new DlpAudioRedactionRequest(); // DlpAudioRedactionRequest | Input request (optional) 

            try
            {
                // Redact User Data in Audio File as a Batch Job
                DlpBatchJobResult result = apiInstance.RedactAudioBatchJob(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling TasksBatchJobApi.RedactAudioBatchJob: " + e.Message );
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

[**DlpBatchJobResult**](DlpBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

