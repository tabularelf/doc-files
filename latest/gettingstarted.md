## Installing
1. Download Collage's .yymp from [releases!](https://github.com/tabularelf/Collage/releases)
2. With your GameMaker Project, drag the .yymp (or at the top goto Tools -> Import Local Package)
3. Press "Add All" and press "Import".

## Updating to a new version
?> If you've made changes to `__CollageConfig`, consider backing it up (preferably with source control) before updating!

1. Delete `Collage`'s folder (with all scripts inside.)
2. Follow the steps through [Installing](#installing), but with the latest version.
3. Reimport your `__CollageConfig` (if changes were made)

## Using Collage
<p>Collage includes a variety of ways to adding images onto texture pages.

We'll start by

```gml
// Collage takes in: width, height, separation
texPage = new Collage();

```