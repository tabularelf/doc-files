# Wav Reference

!> Wav files must be unsigned 8bit or signed 16bit.

### `audioExtWavAddFile(filePath, [is3D], [preload], [compressedInMemory], [alias])`

Returns: struct or `undefined`.

|Name|Datatype|Purpose|
|---|---|---|
|filePath|string|Path to load file.|
|[is3D]|boolean|Defaults to false. Determines if the audio file is intended for 3D Audio. Otherwise uses whatever the wav format determines. (Mono/Stereo)|
|[preload]|boolean|Defaults to false. Adds an entry but doesn't actually load in the file.|
|[compressedInMemory]|boolean|Defaults to false. Compresses data in memory automatically. Note: If `[preload]` is set to false, it will load in the file, but quickly compresses down in memory, then unloading it.|
|[alias]|string|Defaults to the name of the file (excluding the extension).|

Adds the wav file as a sound source from a filename. As this audio is loaded and handled in memory, you do not need to keep the file around afterwards.
  
### `audioExtWavAddBuffer(buffer, alias, [is3D], [preload], [compressedInMemory], [filePath])`

Returns: struct or `undefined`.

|Name|Datatype|Purpose|
|---|---|---|
|buffer|buffer|Path to load file.|
|alias|string|Name of audio.|
|[is3D]|boolean|Defaults to false. Determines if the audio file is intended for 3D Audio. Otherwise uses whatever the wav format determines. (Mono/Stereo)|
|[preload]|boolean|Defaults to false. Adds an entry but doesn't actually load in the file.|
|[compressedInMemory]|boolean|Defaults to false. Compresses data in memory automatically. Note: If `[preload]` is set to false, it will load in the file, but quickly compresses down in memory, then unloading it.|
|[filePath]|string|Defaults to `""`. The path for the function to call upon, if it ever unloads.|

Adds the wav file as a sound source from a buffer. The buffer itself is copied. 

### `audioExtWavScan(filePath, [preload], [compressedInMemory])`

Returns: N/A (`undefined`).

|Name|Datatype|Purpose|
|---|---|---|
|filePath|buffer|Path to scan for wav files.|
|[preload]|boolean|Defaults to false. Adds an entry but doesn't actually load in the file.|
|[compressedInMemory]|boolean|Defaults to false. Compresses data in memory automatically. Note: If `[preload]` is set to false, it will load in the file, but quickly compresses down in memory, then unloading it.|

Scans all of the files within the chosen filePath and loads in any wav files.

### `audioExtWavGetNames()`

Returns: array.

|Name|Datatype|Purpose|
|---|---|---|
|N/A|||

Gets the name of all of the wav files from the database.

### `audioExtWavRemove(audioName)`

Returns: N/A (`undefined`).

|Name|Datatype|Purpose|
|---|---|---|
|audioName|string|Name of audio file.|

Removes the string specified by the audioName from the wav database.
