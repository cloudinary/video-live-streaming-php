Video Live Streaming (Beta) PHP SDK
==================

Use the Video Live Streaming API to create and manage your RTMP live streams. This includes managing outputs as well as manually starting and stopping streams. See the [live streaming guide](https://cloudinary.com/documentation/video_live_streaming) for information on how to use the Live Streaming API to stream video to your users.

  **Note**: The Live Streaming API is currently in development and is available as a Public Beta, which means we value your feedback, so please feel free to [share any thoughts with us](https://support.cloudinary.com/hc/en-us/requests/new).

  The API supports Basic Authentication using your Cloudinary API Key and API Secret (which can be found on the Dashboard page of your [Cloudinary Console](https://console.cloudinary.com/pm)).


For more information, please visit [https://support.cloudinary.com](https://support.cloudinary.com).

## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "require": {
    "cloudinary/video-live-streaming": "*"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/video-live-streaming/vendor/autoload.php');
```


## Configuration

The API uses **Basic Authentication** over HTTPS.

You can find your product environment configuration credentials in the API Keys page of the Cloudinary Console [Dashboard](https://console.cloudinary.com/pm/developer-dashboard).

You can either pass configuration with each `$apiInstance` initialization:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure Cloudinary URL: basicAuth
$config = Cloudinary\Video\LiveStreaming\Configuration::getDefaultConfiguration()
              ->setCloudinaryUrl('cloudinary://key:secret@cloud_name');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi(null, $config);
```

Or set the environment variable globally.

For example, to set a temporary environment variable:

* On Mac or Linux:

    ```
    export CLOUDINARY_URL=cloudinary://key:secret@cloud_name
    ```

* On Windows:

    ```
    set CLOUDINARY_URL=cloudinary://key:secret@cloud_name
    ```

And then you can simply initialize `$apiInstance` as follows:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();


try {
    $result = $apiInstance->getLiveStreams();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->getLiveStreams: ', $e->getMessage(), PHP_EOL;
}
```

## API Endpoints

All URIs are relative to https://api.cloudinary.com/v2/CLOUD_NAME/video, except if the operation defines another base path.

| Class | Method | HTTP request | Description |
| ------------ | ------------- | ------------- | ------------- |
| *LiveStreamApi* | [**activateLiveStream**](docs/Api/LiveStreamApi.md#activatelivestream) | **POST** /live_streams/{liveStreamId}/activate | Manually activate a live stream |
| *LiveStreamApi* | [**createLiveStream**](docs/Api/LiveStreamApi.md#createlivestream) | **POST** /live_streams | Create a new live stream |
| *LiveStreamApi* | [**createLiveStreamOutput**](docs/Api/LiveStreamApi.md#createlivestreamoutput) | **POST** /live_streams/{liveStreamId}/outputs | Create a new live stream output |
| *LiveStreamApi* | [**deleteLiveStream**](docs/Api/LiveStreamApi.md#deletelivestream) | **DELETE** /live_streams/{liveStreamId} | Delete a live stream |
| *LiveStreamApi* | [**deleteLiveStreamOutput**](docs/Api/LiveStreamApi.md#deletelivestreamoutput) | **DELETE** /live_streams/{liveStreamId}/outputs/{liveStreamOutputId} | Delete a live stream output |
| *LiveStreamApi* | [**getLiveStream**](docs/Api/LiveStreamApi.md#getlivestream) | **GET** /live_streams/{liveStreamId} | Get a single live stream |
| *LiveStreamApi* | [**getLiveStreamOutput**](docs/Api/LiveStreamApi.md#getlivestreamoutput) | **GET** /live_streams/{liveStreamId}/outputs/{liveStreamOutputId} | Get a single live stream output |
| *LiveStreamApi* | [**getLiveStreamOutputs**](docs/Api/LiveStreamApi.md#getlivestreamoutputs) | **GET** /live_streams/{liveStreamId}/outputs | Get a list of live stream outputs |
| *LiveStreamApi* | [**getLiveStreams**](docs/Api/LiveStreamApi.md#getlivestreams) | **GET** /live_streams | Get a list of live streams |
| *LiveStreamApi* | [**idleLiveStream**](docs/Api/LiveStreamApi.md#idlelivestream) | **POST** /live_streams/{liveStreamId}/idle | Manually idle a live stream |
| *LiveStreamApi* | [**updateLiveStream**](docs/Api/LiveStreamApi.md#updatelivestream) | **PATCH** /live_streams/{liveStreamId} | Update a live stream |
| *LiveStreamApi* | [**updateLiveStreamOutput**](docs/Api/LiveStreamApi.md#updatelivestreamoutput) | **PATCH** /live_streams/{liveStreamId}/outputs/{liveStreamOutputId} | Update a live stream output |

## Models

- [ErrorWrappedResponse](docs/Model/ErrorWrappedResponse.md)
- [LiveStreamCreatePayload](docs/Model/LiveStreamCreatePayload.md)
- [LiveStreamInputCreatePayload](docs/Model/LiveStreamInputCreatePayload.md)
- [LiveStreamInputResponse](docs/Model/LiveStreamInputResponse.md)
- [LiveStreamOutputCreatePayload](docs/Model/LiveStreamOutputCreatePayload.md)
- [LiveStreamOutputResponse](docs/Model/LiveStreamOutputResponse.md)
- [LiveStreamOutputUpdatePayload](docs/Model/LiveStreamOutputUpdatePayload.md)
- [LiveStreamOutputWrappedResponse](docs/Model/LiveStreamOutputWrappedResponse.md)
- [LiveStreamOutputsWrappedResponse](docs/Model/LiveStreamOutputsWrappedResponse.md)
- [LiveStreamResponse](docs/Model/LiveStreamResponse.md)
- [LiveStreamUpdatePayload](docs/Model/LiveStreamUpdatePayload.md)
- [LiveStreamWrappedResponse](docs/Model/LiveStreamWrappedResponse.md)
- [LiveStreamsWrappedResponse](docs/Model/LiveStreamsWrappedResponse.md)
- [MessageWrappedResponse](docs/Model/MessageWrappedResponse.md)
- [MessageWrappedResponseData](docs/Model/MessageWrappedResponseData.md)

## Authorization

### basicAuth

- **Type**: HTTP basic authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

support@cloudinary.com

## About this package

This Video Live Streaming (Beta) PHP package is automatically generated.

- Package version: `0.1.0`
- API version: `0.1.9`
- Build package: `org.openapitools.codegen.languages.PhpNextgenClientCodegen`
