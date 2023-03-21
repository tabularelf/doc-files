### `CanvasIsCanvas(canvas)`

Returns: `Boolean`

|Name|Datatype|Purpose|
|---|---|---|
|`Canvas`|`Any`|Canvas that you want to check is a Canvas instance.|

Checks whether if it's a valid Canvas instance or not.

### `CanvasGetAppSurf(newAppSurf)`

Returns: An instance of `Canvas`.

|Name|Datatype|Purpose|
|---|---|---|
|`newAppSurf`|`Boolean`|Whether to return the global Canvas `application_surface`, or to create a new Canvas instance with a copy of the `application_surface` contents.|

Returns `true` if it's a Canvas instance, `false` if it's not.