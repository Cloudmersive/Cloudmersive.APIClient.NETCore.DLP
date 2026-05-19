# Cloudmersive.APIClient.NETCore.DLP - the C# library for the dlpapi

Easily and directly scan and detect sensitive data (PII) in input text.

This C# SDK is for the [Cloudmersive DLP API](https://www.cloudmersive.com/dlp-data-loss-prevention-api):

- API version: v1
- SDK version: 1.1.2
- Build package: io.swagger.codegen.languages.CSharpClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET Core >=1.0
- .NET Framework >=4.6
- Mono/Xamarin >=vNext
- UWP >=10.0

<a name="dependencies"></a>
## Dependencies
- FubarCoder.RestSharp.Portable.Core >=4.0.7
- FubarCoder.RestSharp.Portable.HttpClient >=4.0.7
- Newtonsoft.Json >=10.0.3

<a name="installation"></a>
## Installation
Generate the DLL using your preferred tool

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;
```
<a name="getting-started"></a>
## Getting Started

```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DLP.Api;
using Cloudmersive.APIClient.NETCore.DLP.Client;
using Cloudmersive.APIClient.NETCore.DLP.Model;

namespace Example
{
    public class Example
    {
        public void main()
        {

            // Configure API key authorization: Apikey
            Configuration.Default.ApiKey.Add("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("Apikey", "Bearer");

            var apiInstance = new DetectApi();
            var body = new DlpAudioDetectionRequest(); // DlpAudioDetectionRequest | Input request (optional) 

            try
            {
                // Detect User Data in Audio File
                DlpAudioDetectionResponse result = apiInstance.DetectAudio(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DetectApi.DetectAudio: " + e.Message );
            }

        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DetectApi* | [**DetectAudio**](docs/DetectApi.md#detectaudio) | **POST** /dlp/detect/audio | Detect User Data in Audio File
*DetectApi* | [**DetectAudioAdvanced**](docs/DetectApi.md#detectaudioadvanced) | **POST** /dlp/detect/audio/advanced | Detect User Data in Audio File (Advanced)
*DetectApi* | [**DetectDocument**](docs/DetectApi.md#detectdocument) | **POST** /dlp/detect/document | Detect User Data in Document Image
*DetectApi* | [**DetectDocumentAdvanced**](docs/DetectApi.md#detectdocumentadvanced) | **POST** /dlp/detect/document/advanced | Detect User Data in Document Image (Advanced)
*DetectApi* | [**DetectText**](docs/DetectApi.md#detecttext) | **POST** /dlp/detect/text | Detect User Data in Input Text
*DetectApi* | [**DetectTextAdvanced**](docs/DetectApi.md#detecttextadvanced) | **POST** /dlp/detect/text/advanced | Detect User Data in Input Text (Advanced)
*RedactApi* | [**RedactAudio**](docs/RedactApi.md#redactaudio) | **POST** /dlp/redact/audio | Redact User Data in Audio File
*RedactApi* | [**RedactAudioAdvanced**](docs/RedactApi.md#redactaudioadvanced) | **POST** /dlp/redact/audio/advanced | Redact User Data in Audio File (Advanced)
*RedactApi* | [**RedactDocument**](docs/RedactApi.md#redactdocument) | **POST** /dlp/redact/document | Redact User Data in Document
*RedactApi* | [**RedactDocumentAdvanced**](docs/RedactApi.md#redactdocumentadvanced) | **POST** /dlp/redact/document/advanced | Redact User Data in Document (Advanced)
*RedactApi* | [**RedactText**](docs/RedactApi.md#redacttext) | **POST** /dlp/redact/text | Redact User Data in Input Text
*RedactApi* | [**RedactTextAdvanced**](docs/RedactApi.md#redacttextadvanced) | **POST** /dlp/redact/text/advanced | Redact User Data in Input Text (Advanced)
*TasksBatchJobApi* | [**DetectAudioAdvancedBatchJob**](docs/TasksBatchJobApi.md#detectaudioadvancedbatchjob) | **POST** /dlp/batch-job/detect/audio/advanced | Detect User Data in Audio File (Advanced) as a Batch Job
*TasksBatchJobApi* | [**DetectAudioBatchJob**](docs/TasksBatchJobApi.md#detectaudiobatchjob) | **POST** /dlp/batch-job/detect/audio | Detect User Data in Audio File as a Batch Job
*TasksBatchJobApi* | [**GetAsyncJobStatus**](docs/TasksBatchJobApi.md#getasyncjobstatus) | **GET** /dlp/batch-job/status | Get the status and result of a DLP Batch Job
*TasksBatchJobApi* | [**RedactAudioAdvancedBatchJob**](docs/TasksBatchJobApi.md#redactaudioadvancedbatchjob) | **POST** /dlp/batch-job/redact/audio/advanced | Redact User Data in Audio File (Advanced) as a Batch Job
*TasksBatchJobApi* | [**RedactAudioBatchJob**](docs/TasksBatchJobApi.md#redactaudiobatchjob) | **POST** /dlp/batch-job/redact/audio | Redact User Data in Audio File as a Batch Job


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.AudioTimestamp](docs/AudioTimestamp.md)
 - [Model.CustomPiiField](docs/CustomPiiField.md)
 - [Model.DlpAdvancedAudioDetectionRequest](docs/DlpAdvancedAudioDetectionRequest.md)
 - [Model.DlpAdvancedAudioDetectionResponse](docs/DlpAdvancedAudioDetectionResponse.md)
 - [Model.DlpAdvancedAudioRedactionRequest](docs/DlpAdvancedAudioRedactionRequest.md)
 - [Model.DlpAdvancedAudioRedactionResponse](docs/DlpAdvancedAudioRedactionResponse.md)
 - [Model.DlpAdvancedDetectionRequest](docs/DlpAdvancedDetectionRequest.md)
 - [Model.DlpAdvancedDetectionResponse](docs/DlpAdvancedDetectionResponse.md)
 - [Model.DlpAdvancedDocumentDetectionRequest](docs/DlpAdvancedDocumentDetectionRequest.md)
 - [Model.DlpAdvancedDocumentRedactionRequest](docs/DlpAdvancedDocumentRedactionRequest.md)
 - [Model.DlpAdvancedDocumentRedactionResponse](docs/DlpAdvancedDocumentRedactionResponse.md)
 - [Model.DlpAdvancedRedactionRequest](docs/DlpAdvancedRedactionRequest.md)
 - [Model.DlpAdvancedRedactionResponse](docs/DlpAdvancedRedactionResponse.md)
 - [Model.DlpAudioDetectionRequest](docs/DlpAudioDetectionRequest.md)
 - [Model.DlpAudioDetectionResponse](docs/DlpAudioDetectionResponse.md)
 - [Model.DlpAudioRedactionRequest](docs/DlpAudioRedactionRequest.md)
 - [Model.DlpAudioRedactionResponse](docs/DlpAudioRedactionResponse.md)
 - [Model.DlpBatchJobResult](docs/DlpBatchJobResult.md)
 - [Model.DlpBatchJobStatusResult](docs/DlpBatchJobStatusResult.md)
 - [Model.DlpDetectionRequest](docs/DlpDetectionRequest.md)
 - [Model.DlpDetectionResponse](docs/DlpDetectionResponse.md)
 - [Model.DlpDocumentDetectionRequest](docs/DlpDocumentDetectionRequest.md)
 - [Model.DlpDocumentRedactionRequest](docs/DlpDocumentRedactionRequest.md)
 - [Model.DlpDocumentRedactionResponse](docs/DlpDocumentRedactionResponse.md)
 - [Model.DlpRedactionRequest](docs/DlpRedactionRequest.md)
 - [Model.DlpRedactionResponse](docs/DlpRedactionResponse.md)
 - [Model.RedactedAudioSegment](docs/RedactedAudioSegment.md)
 - [Model.RedactedPageInfo](docs/RedactedPageInfo.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="Apikey"></a>
### Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header

