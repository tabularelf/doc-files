### `.GetBufferContents([forceCompress])`<br>
This returns the buffer contents that the surface has been saved onto (if any), with a small header format to determine if:<br>
- It's compressed
- The width
- The height

If `[forceCompress]` is set to `true` (default is `false`), it will give you a compressed version of the current contents, if it's not compressed.


### `.GetTexture()`<br>
Gets the texture of the surface.

### `.GetPixel(x, y)`<br>
Gets colour data from a pixel from the buffer cache. 

### `.GetPixelArray(x, y)`<br>
Gets colour data from a pixel from the buffer cache, in the form of an array.

### `.GetSurfaceID()`

Returns: `Surface ID` or `-1`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Returns the Canvas surface ID, if there's any data.

### `.GetTexture()`

Returns: `Surface texture ID`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Frees the Canvas surface, flushing it from VRAM.

### `.GetWidth()`

Returns: `Real`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Returns the width of the Canvas.

### `.GetHeight()`

Returns: `Real`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Returns the height of the Canvas.

### `.GetStatus()`

Returns: `CanvasStatus Enum value`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Returns the status of the Canvas, which can be compared against one of the many enum values from `CanvasStatus`.

|Name|Purpose|
|---|---|
|`NO_DATA`|Canvas contains no data.|
|`IN_USE`|Canvas is currently being written to.|
|`HAS_DATA`|Canvas has data.|
|`HAS_DATA_CACHED`|Canvas has data but is cached in memory.|

### `.GetFormat()`

Returns: `Surface Format`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Returns the format that the Canvas is using, as the argument passed when creating a Canvas instance.

### `.GetDepthEnabled()`

Returns: `Boolean`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Returns whether depth is enabled or not.