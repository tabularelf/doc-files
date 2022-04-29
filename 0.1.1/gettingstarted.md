## Installing
<p>audioExt

## Updating to a new version

## Loading in your audio files
<p>audioExt includes a variety of ways of loading in your wav and ogg files. You can:

- Scan a directory for each type.
- Add them manually.

Additionally, wav files include adding in a whole buffer. Allowing you to utilize `buffer_load_async`.

We'll start by

```gml
// Scans and adds all wavs to the database.
audioExtWavScan("sounds\\", true, false);

// Scans and adds all oggs to the database.
audioExtOggScan("music\\");

```