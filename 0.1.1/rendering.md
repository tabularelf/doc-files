# Rendering

### `draw_image(sprite_index/image, image_index, x, y)`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`sprite_index/image`|real or struct|sprite or image you wish to render.|
|`image_index`|real|subimage you wish to draw from sprite or image.|
|`x`|real|x position of where you want to draw sprite or image.|
|`y`|real|y position of where you want to draw sprite or image.|

A compatibility function, designed to allow drawing either GM sprites or Collage images. Draws the GM sprite or Collage image.

### `draw_image_ext(sprite_index/image, image_index, x, y, xscale, yscale, rot, col, alpha)`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`sprite_index/image`|real or struct|sprite or image you wish to render.|
|`image_index`|real|subimage you wish to draw from sprite or image.|
|`x`|real|x position of where you want to draw sprite or image.|
|`y`|real|y position of where you want to draw sprite or image.|
|`xscale`|real|xscale you'd like to draw sprite or image.|
|`yscale`|real|yscale you'd like to draw sprite or image.|
|`rot`|real|Angle to draw sprite or image.|
|`col`|real|Colour to draw sprite or image.|
|`alpha`|real|Alpha to draw sprite or image.|

A compatibility function, designed to allow drawing either GM sprites or Collage images. Draws the GM sprite or Collage image.

### `CollageDrawImage(image, image_index, x, y)`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`image`|struct|image you wish to render.|
|`image_index`|real|subimage you wish to draw from sprite or image.|
|`x`|real|x position of where you want to draw image.|
|`y`|real|y position of where you want to draw image.|

Draws Collage image.

### `CollageDrawImageExt(image, image_index, x, y, xscale, yscale, rot, col, alpha)`

Returns: `N/A`.

|Name|Datatype|Purpose|
|---|---|---|
|`image`|struct|image you wish to render.|
|`image_index`|real|subimage you wish to draw from image.|
|`x`|real|x position of where you want to draw image.|
|`y`|real|y position of where you want to draw image.|
|`xscale`|real|xscale you'd like to draw image.|
|`yscale`|real|yscale you'd like to draw image.|
|`rot`|real|Angle to draw image.|
|`col`|real|Colour to draw image.|
|`alpha`|real|Alpha to draw image.|

Draws Collage image.