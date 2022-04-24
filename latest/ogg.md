# Ogg Reference

### `audioExtOggAddStream(filePath, [preload], [alias])`

Returns: struct or `undefined`.

|Name|Datatype|Purpose|
|---|---|---|
|filePath|string|Path to load file.|
|[preload]|boolean|Defaults to false. Adds an entry but doesn't actually load in the file.|
|[alias]|string|Defaults to the name of the file (excluding the extension).|

Adds the ogg file as a sound source from a filename. Since ogg files are streamed, they need to remain on disk.

### `audioExtOggScan(filePath, [preload])`

Returns: N/A (`undefined`).

|Name|Datatype|Purpose|
|---|---|---|
|filePath|buffer|Path to scan for ogg files.|
|[preload]|boolean|Defaults to false. Adds an entry but doesn't actually load in the file.|

Scans all of the files within the chosen filePath and loads in any ogg files.

### `audioExtWavOggNames()`

Returns: array.

|Name|Datatype|Purpose|
|---|---|---|
|N/A|||

Gets the name of all of the ogg files from the database.

### `audioExtOggRemove(audioName)`

Returns: N/A (`undefined`).

|Name|Datatype|Purpose|
|---|---|---|
|audioName|string|Name of audio file.|

Removes the string specified by the audioName from the ogg database.
