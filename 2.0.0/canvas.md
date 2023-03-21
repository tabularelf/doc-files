# Canvas

### `Canvas(width, height, [forceInit], [surfaceFormat])`

Returns: An instance of `Canvas`.

|Name|Datatype|Purpose|
|---|---|---|
|`width`|`Real`|Width of the Canvas.|
|`height`|`Real`|Height of the Canvas.|
|`forceInit`|`Bool`|Whether to forcefully init the Canvas or not. Defaults to `false`.|
|`surfaceFormat`|`SurfaceFormatType`|The surface format to use for the Canvas instance. Defaults to `surface_rgba8unorm`. See [`surface_create`](https://manual.yoyogames.com/GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create.htm) for more.|

Constructor, creates a new instance of `Canvas` to be used for storing the contents of the surface.

### `.Start([targetID])`

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`TargetID`|`Real`|Sets the Canvas target, used for shaders primarily. Default is `-1`, which is for no target.|

Starts writing to the Canvas.

### `.Finish()`

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Finishes writing to the Canvas. If caching writing is enabled, it will also write the Canvas data to the Canvas instance's cache.

### `.Free()`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Frees the Canvas contents, allowing for discarding safely.

### `.Flush()`

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Frees the Canvas surface, flushing it from VRAM.

### `.Resize(width, height, [keepData])`

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Sets the width and height of the Canvas. If `[keepData]` is set to `true`, it will also maintain the current data.
Note: This will also free the surface/buffer context as they're now both invalid data.
Additional note: `[keepData]` currently does not work properly on HTML5, so it has been forcedfully switched off.

### `.CopySurface(surfaceID, x, y, [forceResize], [updateCache])`<br>

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Copies one surface to the Canvas surface, as per `surface_copy()`. <br>
If `[forceResize]` is set to `true` (default is `false`), it will also resize the surface/buffer prior to copying the surface as per `x + width`, `y + height`. <br>
If `[updateCache]` is set to `true` (default is the state of `.WriteToCache()`), it will update the cache.

### `.CopySurfacePart(surfaceID, x, y, xs, ys, ws, hs, [forceResize], [updateCache])`<br>

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Same as above, except also takes in a few additional arguments for copying parts of a surface.

### `.CopyCanvas(canvas, x, y, [forceResize], [updateCache])`<br>

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Same as `.CopySurface()`, but copies a Canvas surface instead.

### `.CopyCanvasPart(canvas, x, y, xs, ys, ws, hs, [forceResize], [updateCache])`<br>

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Same as `.CopySurfacePart()`, but copies a Canvas surface instead.

### `.CheckSurface()`<br>

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

?> This method is deprecated and is currently being phased out slowly.<br>

Checks up on the surface. This isn't normally needed to be called in about every function, as this is automatically invoked.

### `.UpdateCache()`<br>

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Updates the cache when called.

### `.IsAvailable()`<br>

Returns: `Boolean`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Determines if the Canvas has some kind of data, and isn't in use.

### `.Clear()`<br>

Returns: `self`.

|Name|Datatype|Purpose|
|---|---|---|
|`N/A`|||

Clears data. 