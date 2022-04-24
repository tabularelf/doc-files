# Collage Methods

### `.startBatch()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Tells Collage to batch images instead of building right away.

### `.finishBatch()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Tells Collage that it's done batching images and to start building.

### `.clearBatch()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Tells Collage to clear the list of images.

### `.addFile(filepath, [identifier], [subimages], [removeback], [smooth], [xorigin], [yorigin], [is3D])`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`filepath`|string|The path to the image.|
|`identifier`|string|The name of the image. By default, uses the filename without the extension.|
|`subimage`|real|Number of subimages. (Default `1`)|
|`removeback`|boolean|Whether to removeback or not. (Default `false`)|
|`smooth`|boolean|Whether to smooth the image or not. (Default `false`)|
|`xorigin`|real|xoffset of image. (Default `0`)|
|`yorigin`|real|yoffset of image.  (Default `0`)|
|`is3D`|boolean|Whether image should have its own texture page, regardless of size. (Default `false`)|

Loads a image and adds it to the texture page. (Note: If `.startBatch()` was called, then images are added to a list until `.finishBatch()` is called.)

### `.addSprite(spriteID, [identifier], [isCopy], [is3D])`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`spriteID`|sprite_index|The path to the image.|
|`identifier`|string|The name of the image. By default, uses the filename without the extension.|
|`isCopy`|boolean|Whether this image is a copy of another. Hints to collage to auto delete the sprite at the end. (Default `false`)|
|`is3D`|boolean|Whether to removeback or not. (Default `false`)|

Marks a sprite as an image and adds it to the texture page. (Note: If `.startBatch()` was called, then images are added to a list until `.finishBatch()` is called.)

### `.addFileStrip(filepath, [identifier], [removeback], [smooth], [xorigin], [yorigin], [is3D])`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`filepath`|string|The path to the image.|
|`identifier`|string|The name of the image. By default, uses the filename without the extension.|
|`removeback`|boolean|Whether to removeback or not. (Default `false`)|
|`smooth`|boolean|Whether to smooth the image or not. (Default `false`)|
|`xorigin`|real|xoffset of image. (Default `0`)|
|`yorigin`|real|yoffset of image.  (Default `0`)|
|`is3D`|boolean|Whether image should have its own texture page, regardless of size. (Default `false`)|

Loads a image strip and adds it to the texture page. (Note: If `.startBatch()` was called, then images are added to a list until `.finishBatch()` is called.)

### `.addSurface(surfaceID, [identifier], [x], [y], [width], [height], [removeback], [smooth], [xorigin], [yorigin], [is3D])`

Converts a surface into an image and  adds it to the texture page. (Note: If `.startBatch()` was called, then images are added to a list until `.finishBatch()` is called.)

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`surfaceID`|surfaceID|The ID of the surface.|
|`identifier`|string|The name of the image. By default, uses the filename without the extension.|
|`x`|real|The x position to copy from. (Default `0`)|
|`y`|real|The y position to copy from.  (Default `0`)|
|`width`|real|The width of the area to be copied (from the x position). (Default `surface_width`)|
|`height`|real|The height of the area to be copied (from the y position). (Default `surface_height`)|
|`removeback`|boolean|Whether to removeback or not. (Default `false`)|
|`smooth`|boolean|Whether to smooth the image or not. (Default `false`)|
|`xorigin`|real|xoffset of image. (Default `0`)|
|`yorigin`|real|yoffset of image.  (Default `0`)|
|`is3D`|boolean|Whether image should have its own texture page, regardless of size. (Default `false`)|

### `.freePages()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Frees the texture pages (and images).

### `.getPage()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Frees the texture pages (and images).

### `.getPageCount()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Frees the texture pages (and images).

### `.flushPages()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Flushes all texture pages to cached memory.

### `.flushPage()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Flushes a texture page to cached memory.

### `.prefetchPages()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Loads all texture pages from cached memory.

### `.prefetchPage(index)`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`index`|real|Texture page to load from cache.|

Loads a texture page from cached memory.