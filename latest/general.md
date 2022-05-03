# General

### `Collage([width], [height], [crop], [separation], [identifier])`

Returns: struct, an instance of `Collage`.

|Name|Datatype|Purpose|
|---|---|---|
|`width`|real|Width of the texture page.|
|`height`|real|Height of the texture page.|
|`crop`|boolean|Whether to crop every image.|
|`separation`|real|How many pixels should images be spaced apart.|
|`identifier`|strimg|Name of the texture page.|

Constructor, creates a new instance of `Collage` to be used for building texture pages. If `identifier` was passed, Collage will assign itself to a global database and can be used with `CollageGet()` to retrieve said Collage instance.

### `CollageIsPowerTwo(number)`

Returns: `boolean`.

|Name|Datatype|Purpose|
|---|---|---|
|`number`|real|Number to check if power of two.|

Determines whether the number passed is a valid power of two.

### `CollageConvertPowerTwo(number)`

Returns: `real`.

|Name|Datatype|Purpose|
|---|---|---|
|`number`|real|Number to convert to power of two|

Converts a number to the nearest power of two.

### `CollageSterlizeGPUState()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Sterlizes the GPU states, matrices and shader, preparing for adding onto a texture page as is.

### `CollageRestoreGPUState()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Restores the GPU states, matrices and shader from `CollageSterlizeGPUState()`.