## Installing
1. Download Collage's .yymp from [releases!](https://github.com/tabularelf/Collage/releases)
2. With your GameMaker Project, drag the .yymp (or at the top goto Tools -> Import Local Package)
3. Press "Add All" and press "Import".

## Updating to a new version
?> If you've made changes to `__CollageConfig`, consider backing it up (preferably with source control) before updating!

1. Delete `Collage`'s folder (with all scripts inside.)
2. Follow the steps through [Installing](#installing), but with the latest version.
3. Reimport your `__CollageConfig` (if changes were made)

## Loading in your audio files
<p>audioExt includes a variety of ways of loading in your wav and ogg files. You can:

- Scan a directory for each type.
- Add them manually.

Additionally, wav files include adding in a whole buffer. Allowing you to utilize `buffer_load_async`.

We'll start 

```gml
// Scans and adds all wavs to the database.
audioExtWavScan("sounds\\", true, false);

// Scans and adds all oggs to the database.
audioExtOggScan("music\\");

```