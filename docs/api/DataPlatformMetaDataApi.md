# \DataPlatformMetaDataApi

All URIs are relative to *https://api.ionos.com/dataplatform*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**VersionsGet**](DataPlatformMetaDataApi.md#VersionsGet) | **Get** /versions | Managed Stackable Data Platform API Versions|



## VersionsGet

```go
var result VersionsGet200Response = VersionsGet(ctx)
                      .Execute()
```

Managed Stackable Data Platform API Versions



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
    // response from `VersionsGet`: VersionsGet200Response
    fmt.Fprintf(os.Stdout, "Response from `DataPlatformMetaDataApi.VersionsGet`: %v\n", resource)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to an apiVersionsGetRequest struct via the builder pattern


### Return type

[**VersionsGet200Response**](../models/VersionsGet200Response.md)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### URLs Configuration per Operation
Each operation can use different server URL defined using `OperationServers` map in the `Configuration`.
An operation is uniquely identified by `"DataPlatformMetaDataApiService.VersionsGet"` string.
Similar rules for overriding default operation server index and variables apply by using `sw.ContextOperationServerIndices` and `sw.ContextOperationServerVariables` context maps.

```golang
ctx := context.WithValue(context.Background(), {packageName}.ContextOperationServerIndices, map[string]int{
    "DataPlatformMetaDataApiService.VersionsGet": 2,
})
ctx = context.WithValue(context.Background(), {packageName}.ContextOperationServerVariables, map[string]map[string]string{
    "DataPlatformMetaDataApiService.VersionsGet": {
    "port": "8443",
},
})
```

