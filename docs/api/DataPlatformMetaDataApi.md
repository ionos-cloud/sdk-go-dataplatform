# \DataPlatformMetaDataApi

All URIs are relative to *https://api.ionos.com/dataplatform*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**VersionsGet**](DataPlatformMetaDataApi.md#VersionsGet) | **Get** /versions | Managed Data Stack API version|



## VersionsGet

```go
var result []string = VersionsGet(ctx)
                      .Execute()
```

Managed Data Stack API version



### Example

```go
package main

import (
    "context"
    "fmt"
    "os"

    ionoscloud "github.com/ionos-cloud/sdk-go-dataplatform"
)

func main() {

    configuration := ionoscloud.NewConfiguration("USERNAME", "PASSWORD", "TOKEN", "HOST_URL")
    apiClient := ionoscloud.NewAPIClient(configuration)
    resource, resp, err := apiClient.DataPlatformMetaDataApi.VersionsGet(context.Background()).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DataPlatformMetaDataApi.VersionsGet``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", resp)
    }
    // response from `VersionsGet`: []string
    fmt.Fprintf(os.Stdout, "Response from `DataPlatformMetaDataApi.VersionsGet`: %v\n", resource)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to an apiVersionsGetRequest struct via the builder pattern


### Return type

**[]string**

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


