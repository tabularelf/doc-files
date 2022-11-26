# Getting Started

## Installing
1. Download Collage's .yymp from [releases!](https://github.com/tabularelf/Collage/releases)
2. With your GameMaker Project, drag the .yymp (or at the top goto Tools -> Import Local Package)
3. Press "Add All" and press "Import".

## Updating to a new version
?> If you've made changes to [`__CollageConfig`](configuration.md), consider backing it up (preferably with source control) before updating!

1. Delete `Collage`'s folder (with all scripts inside.)
2. Follow the steps through [Installing](#installing), but with the latest version.
3. Reimport your [`__CollageConfig`](configuration.md) (if changes were made)

## Using Collage
<p>Collage includes a variety of ways to adding images onto its texture pages.

Here are some of the examples in which you can add images to Collage. (These were mostly taken/referenced from the project from the Github repo.)

<!-- tabs:start -->

#### **.AddSprite**

```gml
texPage = new Collage();
texPage.AddSprite(spr_soldier);
```

?> Unless otherwise specified by `isCopy`, Collage will auto assign all sprites to be copies (including ones added via the IDE, though those ones will be duplicated.)

#### **.AddSurface**

```gml
texPage = new Collage();
var surf = surface_create(512, 512);
surface_set_target(surf);
draw_rectangle_color(0,0, 512, 512, c_red, c_blue, c_green, c_yellow, false);
surface_reset_target();

texPage.AddSurface(surf, "colours");
surface_free(surf);
```

?> This will add the underlying surface as a sprite. The surface itself still needs to be freed.

#### **.AddFile**

```gml
texPage = new Collage();
texPage.AddFile("soldier.png");
```

#### **.AddFileStrip**

```gml
texPage = new Collage();
texPage.AddFileStrip("soldier_strip.png");
```

#### **.AddSpriteSheet**

```gml
texPage = new Collage();
var _batSprite = sprite_add("bats.png", 1, false, false, 0, 0);
var _array = [
	CollageDefineSpriteSheet("_fly_down", 32, 0, 128, 32),
	CollageDefineSpriteSheet("_fly_right", 32, 32, 128, 32),
	CollageDefineSpriteSheet("_fly_up", 32, 64, 128, 32),
	CollageDefineSpriteSheet("_fly_left", 32, 96, 128, 32),
	CollageDefineSpriteSheet("_dead_down", 0, 0, 32, 32),
	CollageDefineSpriteSheet("_dead_right", 0, 32, 32, 32),
	CollageDefineSpriteSheet("_dead_up", 0, 64, 32, 32),
	CollageDefineSpriteSheet("_dead_left", 0, 96, 32, 32),
];
texPage.AddSpriteSheet(_batSprite, _array, "bat", 32, 32);
sprite_delete(_batSprite);
```

?> The spritesheet that's used won't be freed, as copies of it are used instead.

<!-- tabs:end -->

?> Each `.Add*` method has some additional parameters, which most are entirely optional. You can see more by reading their specific documentation under [Collage](collage.md).


Once you've added your images, you can get their info via [`CollageGetImageInfo()`](image.md#collagegetimageinfoidentifier) or [`.GetImageInfo()`](collage.md#getimageinfoidentifier). Which you can then use to render the image.
```gml
// Getting image info
image = texPage.GetImageInfo("test");

// Rendering
draw_image(image, 0, x, y);
```