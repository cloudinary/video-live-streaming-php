# Cloudinary\Video\LiveStreaming\LiveStreamApi

All URIs are relative to https://api.cloudinary.com/v2/CLOUD_NAME/video, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**activateLiveStream()**](LiveStreamApi.md#activateLiveStream) | **POST** /live_streams/{liveStreamId}/activate | Manually activate a live stream |
| [**createLiveStream()**](LiveStreamApi.md#createLiveStream) | **POST** /live_streams | Create a new live stream |
| [**createLiveStreamOutput()**](LiveStreamApi.md#createLiveStreamOutput) | **POST** /live_streams/{liveStreamId}/outputs | Create a new live stream output |
| [**deleteLiveStream()**](LiveStreamApi.md#deleteLiveStream) | **DELETE** /live_streams/{liveStreamId} | Delete a live stream |
| [**deleteLiveStreamOutput()**](LiveStreamApi.md#deleteLiveStreamOutput) | **DELETE** /live_streams/{liveStreamId}/outputs/{liveStreamOutputId} | Delete a live stream output |
| [**getLiveStream()**](LiveStreamApi.md#getLiveStream) | **GET** /live_streams/{liveStreamId} | Get a single live stream |
| [**getLiveStreamOutput()**](LiveStreamApi.md#getLiveStreamOutput) | **GET** /live_streams/{liveStreamId}/outputs/{liveStreamOutputId} | Get a single live stream output |
| [**getLiveStreamOutputs()**](LiveStreamApi.md#getLiveStreamOutputs) | **GET** /live_streams/{liveStreamId}/outputs | Get a list of live stream outputs |
| [**getLiveStreams()**](LiveStreamApi.md#getLiveStreams) | **GET** /live_streams | Get a list of live streams |
| [**idleLiveStream()**](LiveStreamApi.md#idleLiveStream) | **POST** /live_streams/{liveStreamId}/idle | Manually idle a live stream |
| [**updateLiveStream()**](LiveStreamApi.md#updateLiveStream) | **PATCH** /live_streams/{liveStreamId} | Update a live stream |
| [**updateLiveStreamOutput()**](LiveStreamApi.md#updateLiveStreamOutput) | **PATCH** /live_streams/{liveStreamId}/outputs/{liveStreamOutputId} | Update a live stream output |


## `activateLiveStream()`

```php
activateLiveStream($liveStreamId): \Cloudinary\Video\LiveStreaming\Model\MessageWrappedResponse
```

Manually activate a live stream

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id

try {
    $result = $apiInstance->activateLiveStream($liveStreamId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->activateLiveStream: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\MessageWrappedResponse**](../Model/MessageWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createLiveStream()`

```php
createLiveStream($liveStreamCreatePayload): \Cloudinary\Video\LiveStreaming\Model\LiveStreamWrappedResponse
```

Create a new live stream

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamCreatePayload = new \Cloudinary\Video\LiveStreaming\Model\LiveStreamCreatePayload(); // \Cloudinary\Video\LiveStreaming\Model\LiveStreamCreatePayload

try {
    $result = $apiInstance->createLiveStream($liveStreamCreatePayload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->createLiveStream: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamCreatePayload** | [**\Cloudinary\Video\LiveStreaming\Model\LiveStreamCreatePayload**](../Model/LiveStreamCreatePayload.md)|  | [optional] |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\LiveStreamWrappedResponse**](../Model/LiveStreamWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createLiveStreamOutput()`

```php
createLiveStreamOutput($liveStreamId, $liveStreamOutputCreatePayload): \Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputWrappedResponse
```

Create a new live stream output

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id
$liveStreamOutputCreatePayload = {"name":"new youtube","type":"simulcast","uri":"rtmp://a.rtmp.youtube.com/live2","stream_key":"43q7qmah2e1p83jhfpbs","vendor":"youtube"}; // \Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputCreatePayload

try {
    $result = $apiInstance->createLiveStreamOutput($liveStreamId, $liveStreamOutputCreatePayload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->createLiveStreamOutput: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |
| **liveStreamOutputCreatePayload** | [**\Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputCreatePayload**](../Model/LiveStreamOutputCreatePayload.md)|  | [optional] |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputWrappedResponse**](../Model/LiveStreamOutputWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteLiveStream()`

```php
deleteLiveStream($liveStreamId): \Cloudinary\Video\LiveStreaming\Model\MessageWrappedResponse
```

Delete a live stream

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id

try {
    $result = $apiInstance->deleteLiveStream($liveStreamId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->deleteLiveStream: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\MessageWrappedResponse**](../Model/MessageWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteLiveStreamOutput()`

```php
deleteLiveStreamOutput($liveStreamId, $liveStreamOutputId): \Cloudinary\Video\LiveStreaming\Model\MessageWrappedResponse
```

Delete a live stream output

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id
$liveStreamOutputId = "&#39;liveStreamOutputId_example&#39;"; // string | live stream output id

try {
    $result = $apiInstance->deleteLiveStreamOutput($liveStreamId, $liveStreamOutputId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->deleteLiveStreamOutput: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |
| **liveStreamOutputId** | **string**| live stream output id | |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\MessageWrappedResponse**](../Model/MessageWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLiveStream()`

```php
getLiveStream($liveStreamId): \Cloudinary\Video\LiveStreaming\Model\LiveStreamWrappedResponse
```

Get a single live stream

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id

try {
    $result = $apiInstance->getLiveStream($liveStreamId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->getLiveStream: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\LiveStreamWrappedResponse**](../Model/LiveStreamWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLiveStreamOutput()`

```php
getLiveStreamOutput($liveStreamId, $liveStreamOutputId): \Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputWrappedResponse
```

Get a single live stream output

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id
$liveStreamOutputId = "&#39;liveStreamOutputId_example&#39;"; // string | live stream output id

try {
    $result = $apiInstance->getLiveStreamOutput($liveStreamId, $liveStreamOutputId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->getLiveStreamOutput: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |
| **liveStreamOutputId** | **string**| live stream output id | |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputWrappedResponse**](../Model/LiveStreamOutputWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLiveStreamOutputs()`

```php
getLiveStreamOutputs($liveStreamId): \Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputsWrappedResponse
```

Get a list of live stream outputs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id

try {
    $result = $apiInstance->getLiveStreamOutputs($liveStreamId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->getLiveStreamOutputs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputsWrappedResponse**](../Model/LiveStreamOutputsWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLiveStreams()`

```php
getLiveStreams(): \Cloudinary\Video\LiveStreaming\Model\LiveStreamsWrappedResponse
```

Get a list of live streams

### Example

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

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\LiveStreamsWrappedResponse**](../Model/LiveStreamsWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `idleLiveStream()`

```php
idleLiveStream($liveStreamId): \Cloudinary\Video\LiveStreaming\Model\MessageWrappedResponse
```

Manually idle a live stream

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id

try {
    $result = $apiInstance->idleLiveStream($liveStreamId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->idleLiveStream: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\MessageWrappedResponse**](../Model/MessageWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateLiveStream()`

```php
updateLiveStream($liveStreamId, $liveStreamUpdatePayload): \Cloudinary\Video\LiveStreaming\Model\LiveStreamWrappedResponse
```

Update a live stream

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id
$liveStreamUpdatePayload = new \Cloudinary\Video\LiveStreaming\Model\LiveStreamUpdatePayload(); // \Cloudinary\Video\LiveStreaming\Model\LiveStreamUpdatePayload

try {
    $result = $apiInstance->updateLiveStream($liveStreamId, $liveStreamUpdatePayload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->updateLiveStream: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |
| **liveStreamUpdatePayload** | [**\Cloudinary\Video\LiveStreaming\Model\LiveStreamUpdatePayload**](../Model/LiveStreamUpdatePayload.md)|  | [optional] |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\LiveStreamWrappedResponse**](../Model/LiveStreamWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateLiveStreamOutput()`

```php
updateLiveStreamOutput($liveStreamId, $liveStreamOutputId, $liveStreamOutputUpdatePayload): \Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputWrappedResponse
```

Update a live stream output

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Cloudinary\Video\LiveStreaming\Api\LiveStreamApi();

$liveStreamId = "&#39;liveStreamId_example&#39;"; // string | live stream id
$liveStreamOutputId = "&#39;liveStreamOutputId_example&#39;"; // string | live stream output id
$liveStreamOutputUpdatePayload = {"name":"new youtube","type":"simulcast","uri":"rtmp://a.rtmp.youtube.com/live2","stream_key":"43q7qmah2e1p83jhfpbs","vendor":"youtube"}; // \Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputUpdatePayload

try {
    $result = $apiInstance->updateLiveStreamOutput($liveStreamId, $liveStreamOutputId, $liveStreamOutputUpdatePayload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LiveStreamApi->updateLiveStreamOutput: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **liveStreamId** | **string**| live stream id | |
| **liveStreamOutputId** | **string**| live stream output id | |
| **liveStreamOutputUpdatePayload** | [**\Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputUpdatePayload**](../Model/LiveStreamOutputUpdatePayload.md)|  | [optional] |

### Return type

[**\Cloudinary\Video\LiveStreaming\Model\LiveStreamOutputWrappedResponse**](../Model/LiveStreamOutputWrappedResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#)
[[Back to API list]](../../README.md#api-endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
