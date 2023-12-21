# \DataPlatformNodePoolApi

All URIs are relative to *https://api.ionos.com/dataplatform*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**ClustersNodepoolsDelete**](DataPlatformNodePoolApi.md#ClustersNodepoolsDelete) | **Delete** /clusters/{clusterId}/nodepools/{nodepoolId} | Remove a DataPlatformNodePool from a DataPlatformCluster|
|[**ClustersNodepoolsFindById**](DataPlatformNodePoolApi.md#ClustersNodepoolsFindById) | **Get** /clusters/{clusterId}/nodepools/{nodepoolId} | Retrieve a DataPlatformNodePool|
|[**ClustersNodepoolsGet**](DataPlatformNodePoolApi.md#ClustersNodepoolsGet) | **Get** /clusters/{clusterId}/nodepools | List the DataPlatformNodePools of a DataPlatformCluster|
|[**ClustersNodepoolsPatch**](DataPlatformNodePoolApi.md#ClustersNodepoolsPatch) | **Patch** /clusters/{clusterId}/nodepools/{nodepoolId} | Partially Modify a DataPlatformNodePool|
|[**ClustersNodepoolsPost**](DataPlatformNodePoolApi.md#ClustersNodepoolsPost) | **Post** /clusters/{clusterId}/nodepools | Create a DataPlatformNodePool for a distinct DataPlatformCluster|



## ClustersNodepoolsDelete

```go
var result NodePoolResponseData = ClustersNodepoolsDelete(ctx, clusterId, nodepoolId)
                      .Execute()
```

Remove a DataPlatformNodePool from a DataPlatformCluster



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
    clusterId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The unique ID of the cluster. Must conform to the UUID format. 
    nodepoolId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The unique ID of the node pool. Must conform to the UUID format. 

    configuration := ionoscloud.NewConfiguration("USERNAME", "PASSWORD", "TOKEN", "HOST_URL")
    apiClient := ionoscloud.NewAPIClient(configuration)
    resp, err := apiClient.DataPlatformNodePoolApi.ClustersNodepoolsDelete(context.Background(), clusterId, nodepoolId).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DataPlatformNodePoolApi.ClustersNodepoolsDelete``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", resp)
    }
    // response from `ClustersNodepoolsDelete`: NodePoolResponseData
    fmt.Fprintf(os.Stdout, "Response from `DataPlatformNodePoolApi.ClustersNodepoolsDelete`: %v\n", resource)
}
```

### Path Parameters


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
|**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.|
|**clusterId** | **string** | The unique ID of the cluster. Must conform to the UUID format.  | |
|**nodepoolId** | **string** | The unique ID of the node pool. Must conform to the UUID format.  | |

### Other Parameters

Other parameters are passed through a pointer to an apiClustersNodepoolsDeleteRequest struct via the builder pattern


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|

### Return type

[**NodePoolResponseData**](../models/NodePoolResponseData.md)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### URLs Configuration per Operation
Each operation can use different server URL defined using `OperationServers` map in the `Configuration`.
An operation is uniquely identified by `"DataPlatformNodePoolApiService.ClustersNodepoolsDelete"` string.
Similar rules for overriding default operation server index and variables apply by using `sw.ContextOperationServerIndices` and `sw.ContextOperationServerVariables` context maps.

```golang
ctx := context.WithValue(context.Background(), {packageName}.ContextOperationServerIndices, map[string]int{
    "DataPlatformNodePoolApiService.ClustersNodepoolsDelete": 2,
})
ctx = context.WithValue(context.Background(), {packageName}.ContextOperationServerVariables, map[string]map[string]string{
    "DataPlatformNodePoolApiService.ClustersNodepoolsDelete": {
    "port": "8443",
},
})
```


## ClustersNodepoolsFindById

```go
var result NodePoolResponseData = ClustersNodepoolsFindById(ctx, clusterId, nodepoolId)
                      .Execute()
```

Retrieve a DataPlatformNodePool



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
    clusterId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The unique ID of the cluster. Must conform to the UUID format. 
    nodepoolId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The unique ID of the node pool. Must conform to the UUID format. 

    configuration := ionoscloud.NewConfiguration("USERNAME", "PASSWORD", "TOKEN", "HOST_URL")
    apiClient := ionoscloud.NewAPIClient(configuration)
    resource, resp, err := apiClient.DataPlatformNodePoolApi.ClustersNodepoolsFindById(context.Background(), clusterId, nodepoolId).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DataPlatformNodePoolApi.ClustersNodepoolsFindById``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", resp)
    }
    // response from `ClustersNodepoolsFindById`: NodePoolResponseData
    fmt.Fprintf(os.Stdout, "Response from `DataPlatformNodePoolApi.ClustersNodepoolsFindById`: %v\n", resource)
}
```

### Path Parameters


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
|**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.|
|**clusterId** | **string** | The unique ID of the cluster. Must conform to the UUID format.  | |
|**nodepoolId** | **string** | The unique ID of the node pool. Must conform to the UUID format.  | |

### Other Parameters

Other parameters are passed through a pointer to an apiClustersNodepoolsFindByIdRequest struct via the builder pattern


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|

### Return type

[**NodePoolResponseData**](../models/NodePoolResponseData.md)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### URLs Configuration per Operation
Each operation can use different server URL defined using `OperationServers` map in the `Configuration`.
An operation is uniquely identified by `"DataPlatformNodePoolApiService.ClustersNodepoolsFindById"` string.
Similar rules for overriding default operation server index and variables apply by using `sw.ContextOperationServerIndices` and `sw.ContextOperationServerVariables` context maps.

```golang
ctx := context.WithValue(context.Background(), {packageName}.ContextOperationServerIndices, map[string]int{
    "DataPlatformNodePoolApiService.ClustersNodepoolsFindById": 2,
})
ctx = context.WithValue(context.Background(), {packageName}.ContextOperationServerVariables, map[string]map[string]string{
    "DataPlatformNodePoolApiService.ClustersNodepoolsFindById": {
    "port": "8443",
},
})
```


## ClustersNodepoolsGet

```go
var result NodePoolListResponseData = ClustersNodepoolsGet(ctx, clusterId)
                      .Execute()
```

List the DataPlatformNodePools of a DataPlatformCluster



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
    clusterId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The unique ID of the cluster. Must conform to the UUID format. 

    configuration := ionoscloud.NewConfiguration("USERNAME", "PASSWORD", "TOKEN", "HOST_URL")
    apiClient := ionoscloud.NewAPIClient(configuration)
    resource, resp, err := apiClient.DataPlatformNodePoolApi.ClustersNodepoolsGet(context.Background(), clusterId).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DataPlatformNodePoolApi.ClustersNodepoolsGet``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", resp)
    }
    // response from `ClustersNodepoolsGet`: NodePoolListResponseData
    fmt.Fprintf(os.Stdout, "Response from `DataPlatformNodePoolApi.ClustersNodepoolsGet`: %v\n", resource)
}
```

### Path Parameters


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
|**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.|
|**clusterId** | **string** | The unique ID of the cluster. Must conform to the UUID format.  | |

### Other Parameters

Other parameters are passed through a pointer to an apiClustersNodepoolsGetRequest struct via the builder pattern


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|

### Return type

[**NodePoolListResponseData**](../models/NodePoolListResponseData.md)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


### URLs Configuration per Operation
Each operation can use different server URL defined using `OperationServers` map in the `Configuration`.
An operation is uniquely identified by `"DataPlatformNodePoolApiService.ClustersNodepoolsGet"` string.
Similar rules for overriding default operation server index and variables apply by using `sw.ContextOperationServerIndices` and `sw.ContextOperationServerVariables` context maps.

```golang
ctx := context.WithValue(context.Background(), {packageName}.ContextOperationServerIndices, map[string]int{
    "DataPlatformNodePoolApiService.ClustersNodepoolsGet": 2,
})
ctx = context.WithValue(context.Background(), {packageName}.ContextOperationServerVariables, map[string]map[string]string{
    "DataPlatformNodePoolApiService.ClustersNodepoolsGet": {
    "port": "8443",
},
})
```


## ClustersNodepoolsPatch

```go
var result NodePoolResponseData = ClustersNodepoolsPatch(ctx, clusterId, nodepoolId)
                      .PatchNodePoolRequest(patchNodePoolRequest)
                      .Execute()
```

Partially Modify a DataPlatformNodePool



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
    clusterId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The unique ID of the cluster. Must conform to the UUID format. 
    nodepoolId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The unique ID of the node pool. Must conform to the UUID format. 
    patchNodePoolRequest := *openapiclient.NewPatchNodePoolRequest(*openapiclient.NewPatchNodePoolProperties()) // PatchNodePoolRequest | Request payload with the properties that shall be applied to an existing DataPlatformNodePool. 

    configuration := ionoscloud.NewConfiguration("USERNAME", "PASSWORD", "TOKEN", "HOST_URL")
    apiClient := ionoscloud.NewAPIClient(configuration)
    resource, resp, err := apiClient.DataPlatformNodePoolApi.ClustersNodepoolsPatch(context.Background(), clusterId, nodepoolId).PatchNodePoolRequest(patchNodePoolRequest).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DataPlatformNodePoolApi.ClustersNodepoolsPatch``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", resp)
    }
    // response from `ClustersNodepoolsPatch`: NodePoolResponseData
    fmt.Fprintf(os.Stdout, "Response from `DataPlatformNodePoolApi.ClustersNodepoolsPatch`: %v\n", resource)
}
```

### Path Parameters


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
|**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.|
|**clusterId** | **string** | The unique ID of the cluster. Must conform to the UUID format.  | |
|**nodepoolId** | **string** | The unique ID of the node pool. Must conform to the UUID format.  | |

### Other Parameters

Other parameters are passed through a pointer to an apiClustersNodepoolsPatchRequest struct via the builder pattern


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **patchNodePoolRequest** | [**PatchNodePoolRequest**](../models/PatchNodePoolRequest.md) | Request payload with the properties that shall be applied to an existing DataPlatformNodePool.  | |

### Return type

[**NodePoolResponseData**](../models/NodePoolResponseData.md)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### URLs Configuration per Operation
Each operation can use different server URL defined using `OperationServers` map in the `Configuration`.
An operation is uniquely identified by `"DataPlatformNodePoolApiService.ClustersNodepoolsPatch"` string.
Similar rules for overriding default operation server index and variables apply by using `sw.ContextOperationServerIndices` and `sw.ContextOperationServerVariables` context maps.

```golang
ctx := context.WithValue(context.Background(), {packageName}.ContextOperationServerIndices, map[string]int{
    "DataPlatformNodePoolApiService.ClustersNodepoolsPatch": 2,
})
ctx = context.WithValue(context.Background(), {packageName}.ContextOperationServerVariables, map[string]map[string]string{
    "DataPlatformNodePoolApiService.ClustersNodepoolsPatch": {
    "port": "8443",
},
})
```


## ClustersNodepoolsPost

```go
var result NodePoolResponseData = ClustersNodepoolsPost(ctx, clusterId)
                      .CreateNodePoolRequest(createNodePoolRequest)
                      .Execute()
```

Create a DataPlatformNodePool for a distinct DataPlatformCluster



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
    clusterId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The unique ID of the cluster. Must conform to the UUID format. 
    createNodePoolRequest := *openapiclient.NewCreateNodePoolRequest(*openapiclient.NewCreateNodePoolProperties("my-node-pool", int32(2))) // CreateNodePoolRequest | Request payload with the properties that defines a DataPlatformNodePool. 

    configuration := ionoscloud.NewConfiguration("USERNAME", "PASSWORD", "TOKEN", "HOST_URL")
    apiClient := ionoscloud.NewAPIClient(configuration)
    resource, resp, err := apiClient.DataPlatformNodePoolApi.ClustersNodepoolsPost(context.Background(), clusterId).CreateNodePoolRequest(createNodePoolRequest).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DataPlatformNodePoolApi.ClustersNodepoolsPost``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", resp)
    }
    // response from `ClustersNodepoolsPost`: NodePoolResponseData
    fmt.Fprintf(os.Stdout, "Response from `DataPlatformNodePoolApi.ClustersNodepoolsPost`: %v\n", resource)
}
```

### Path Parameters


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
|**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.|
|**clusterId** | **string** | The unique ID of the cluster. Must conform to the UUID format.  | |

### Other Parameters

Other parameters are passed through a pointer to an apiClustersNodepoolsPostRequest struct via the builder pattern


|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createNodePoolRequest** | [**CreateNodePoolRequest**](../models/CreateNodePoolRequest.md) | Request payload with the properties that defines a DataPlatformNodePool.  | |

### Return type

[**NodePoolResponseData**](../models/NodePoolResponseData.md)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


### URLs Configuration per Operation
Each operation can use different server URL defined using `OperationServers` map in the `Configuration`.
An operation is uniquely identified by `"DataPlatformNodePoolApiService.ClustersNodepoolsPost"` string.
Similar rules for overriding default operation server index and variables apply by using `sw.ContextOperationServerIndices` and `sw.ContextOperationServerVariables` context maps.

```golang
ctx := context.WithValue(context.Background(), {packageName}.ContextOperationServerIndices, map[string]int{
    "DataPlatformNodePoolApiService.ClustersNodepoolsPost": 2,
})
ctx = context.WithValue(context.Background(), {packageName}.ContextOperationServerVariables, map[string]map[string]string{
    "DataPlatformNodePoolApiService.ClustersNodepoolsPost": {
    "port": "8443",
},
})
```

