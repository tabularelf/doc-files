# Image

### `CollageGetImageInfo(identifier)`

Returns: struct or `undefined`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string|Name of image.|

Gets the image information (if any exists) or returns `undefined`.

### `CollageImageIsLoaded(identifier, subImage)`

Returns: `boolean`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string|Name of image.|
|`subImage`|real|Subimage of image.|

Checks whether the image is loaded or not.

### `CollageImageLoad(identifier, subImage)`

Returns: `struct`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string|Name of image.|
|`subImage`|real|Subimage of image.|

Loads in an image from cache memory.

### `CollageGetImageUVs(identifier, subImage)`

Returns: `struct`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string|Name of image.|
|`subImage`|real|Subimage of image.|

Gets the UV coordinates of an image.

### `CollageGetImageTexture(identifier, subImage)`

Returns: `texturePointer`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string|Name of image.|
|`subImage`|real|Subimage of image.|

Gets the texture pointer of an image.

### `CollageGetImagePage(identifier, subImage)`

Returns: `surfaceID`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string|Name of image.|
|`subImage`|real|Subimage of image.|

Gets the surface id of an image.