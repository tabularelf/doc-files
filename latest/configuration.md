# Collage Configuration

|Name|Default Value|Purpose|
|---|---|---|
|`__COLLAGE_ENSURE_POWER_TWO`|`true`|Whether Collage should respect Power of Two sizes. (Will readjust the texture page if it's not power of two)|
|`__COLLAGE_CLAMP_TEXTURE_SIZE`|`true`|Whether Collage should clamp to the max texture page size.|
|`__COLLAGE_MIN_TEXTURE_SIZE`|`256`|The absolute minimum size that Collage will allow a texture page to be. Surfaces can work as low as 1. (I wouldn't recommend setting it to anything lower than 256.)|
|`__COLLAGE_MAX_TEXTURE_SIZE`|`8192`|The absolute maximum size that Collage will allow a texture page to be. On Windows, the absolute max is 16384. Other platforms/devices may vary.|
|`__COLLAGE_DEFAULT_TEXTURE_SIZE`|`2048`|The default texture page size.|
|`__COLLAGE_SCALE_TO_TEXTURES_ON_PAGE`|`true`|Whether Collage should scale images that are bigger than the texture page itself.|
|`__COLLAGE_RENDER_DEBUG_LINES`|`false`|Whether Collage should bake coloured boxes around all of the images or not. This is mostly used to determine that images are correctly fitting on the texture page, and otherwise serve no real purpose.|
|`__COLLAGE_DEFAULT_CROP`|`true`|Whether Collage should autocrop any texture pages that weren't given a crop true/false value.|
|`__COLLAGE_DEFAULT_SEPARATION`|`0`|Separation value that Collage will respect across the board if no sep value was passed.|