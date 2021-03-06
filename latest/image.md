# Image

?> If `COLLAGE_IMAGES_MAKE_PUBLIC` is set to false, functions that take in a string as an identifier may not work for all functions.

### `CollageGetImageInfo(identifier)`

Returns: struct or `undefined`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string|Name of image.|

Gets the image information (if any exists) or returns `undefined`.
?> If `COLLAGE_IMAGES_MAKE_PUBLIC` is set to false, this function will not work!

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
|`identifier`|string/image|Name of image.|
|`subImage`|real|Subimage of image.|

Loads in an image from cache memory.

### `CollageGetImageUVs(identifier, image_index)`

Returns: instance of `__CollageImageUVsClass`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string/image|Name of image|
|`image_index`|real|subimage of image|

Returns the UV struct of an image.

### `CollageCompatibilityGetImageUVs(identifier, image_index)`

Returns: `array`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string/image|Name of image|
|`image_index`|real|subimage of image|

Returns an array of UV data that is setup similarily to how GMSprite `sprite_get_uvs()` works.

### `CollageGetImageTexture(identifier, subImage)`

Returns: `texturePointer`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string/image|Name of image.|
|`subImage`|real|Subimage of image.|

Gets the texture pointer of an image.

### `CollageGetImageTexturePage(identifier, subImage)`

Returns: `__CollageTexturePageClass`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string/image|Name of image.|
|`subImage`|real|Subimage of image.|

Gets the `__CollageTexturePageClass` of an image.

### `CollageGetImageSurface(identifier, subImage)`

Returns: `surfaceID`.

|Name|Datatype|Purpose|
|---|---|---|
|`identifier`|string/image|Name of image.|
|`subImage`|real|Subimage of image.|

Gets the surfaceID of an images texture page.