* Home
	- [Features](README.md#features)
	- [Supported Platforms](README.md#supported-platforms)
	- [License](README.md#license)

- [Getting started](gettingstarted.md)

  - [Installing](gettingstarted.md#installing)
  - [Updating to a new version](gettingstarted.md#updating-to-a-new-version)
  - [Loading in your audio files](gettingstarted.md#loading-in-your-audio-files)
  
---

**API Reference**

- [Configuration](configuration.md)
- [General](general.md)
  - [Collage(width, height, [crop], [separation], [identifier])](general.md#collagewidth-height-crop-separation-identifier)
  - [CollageIsPowerTwo(number)](general.md#CollageIsPowerTwoNumber)
  - [CollageConvertPowerTwo(number)](general.md#CollageConvertPowerTwonumber)
  - [CollageSterlizeGPUState()](general.md#CollageSterlizeGPUState)
  - [CollageRestoreGPUState()](general.md#CollageRestoreGPUState)
- [Collage Methods](collage-methods.md)
  - [.StartBatch()](collage-methods#startbatch)
  - [.FinishBatch()](collage-methods#finishbatch)
  - [.ClearBatch()](collage-methods#clearbatch)
  - [.AddFile(filepath, [identifier], [subimages], [removeback], [smooth], [xorigin], [yorigin], [is3D])](collage-methods#addfilefilepath-identifier-subimages-removeback-smooth-xorigin-yorigin-is3d)
  - [.AddSprite(spriteID, [identifier], [isCopy], [is3D])](collage-methods#addspritespriteid-identifier-iscopy-is3d)
  - [.AddFileStrip(filepath, [identifier], [removeback], [smooth], [xorigin], [yorigin], [is3D])](collage-methods#addfilestripfilepath-identifier-removeback-smooth-xorigin-yorigin-is3d)
  - [.AddSurface(surfaceID, [identifier], [x], [y], [width], [height], [removeback], [smooth], [xorigin], [yorigin], [is3D])](collage-methods#addsurfacesurfaceid-identifier-x-y-width-height-removeback-smooth-xorigin-yorigin-is3d)
  - [.FreePages()](collage-methods#freepages)
  - [.GetPage()](collage-methods#getpage)
  - [.GetPageCount()](collage-methods#getpagecount)
  - [.FlushPages()](collage-methods#flushpages)
  - [.FlushPage(index)](collage-methods#flushpageindex)
  - [.PrefetchPages()](collage-methods#prefetchpages)
  - [.PrefetchPage(index)()](collage-methods#prefetchpageindex)
  - [.GetImageInfo(identifier)](collage-methods#getimageinfoidentifier)
  - [.Exists(identifier)](collage-methods#existsidentifier)
  - [.GetStatus()](collage-methods#getstatus)
  - [.ImagesToArray()](collage-methods#imagestoarray)
  - [.ImagesNamesToArray()](collage-methods#imagesnamestoarray)
  - [.Destroy()](collage-methods#destroy)
- [Image](image.md)
  - [CollageGetImageInfo(identifier)](image.md#collagegetimageinfoidentifier)
  - [CollageImageIsLoaded(identifier, subImage)](image.md#collageimageisloadedidentifier-subimage)
  - [CollageImageLoad(identifier, subImage)](image.md#collageimageloadidentifier-subimage)
  - [CollageGetImageUVs(identifier, subImage)](image.md#collagegetimageuvsidentifier-subimage)
  - [CollageGetImageTexture(identifier, subImage)](image.md#collagegetimagetextureidentifier-subimage)
  - [CollageGetImagePage(identifier, subImage)](image.md#collagegetimagepageidentifier-subimage)
- [Rendering](rendering.md)
  - [draw_image(sprite_index/image, image_index, x, y)](rendering.md#draw_imagesprite_indeximage-image_index-x-y)
  - [draw_image_ext(sprite_index/image, image_index, x, y, xscale, yscale, rot, col, alpha)](rendering.md#draw_image_extsprite_indeximage-image_index-x-y-xscale-yscale-rot-col-alpha)
  - [CollageDrawImage(image, image_index, x, y)](rendering.md#collagedrawimageimage-image_index-x-y)
  - [CollageDrawImageExt(image, image_index, x, y, xscale, yscale, rot, col, alpha)](rendering.md#collagedrawimageextimage-image_index-x-y-xscale-yscale-rot-col-alpha)