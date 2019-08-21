# rhino3dm.d.ts

interim rhino3dmjs typescript declaration file

McNeel is [currently developing](https://discourse.mcneel.com/t/rhino3dm-js-typescript-declaration-file/) a typescript declaration file generator. It's still missing a handful of things.

Am keeping a rolling collection of manual fixes here.

## diff

* `File3dm` does not declare any output types for its methods ( like `objects()` and `layers()` ) | should be `File3dmObjectTable` and `File3dmLayerTable` respectively
* `File3dmLayerTable.count()` output as `void` return type | should be `number`
* `GeometryBase.getBoundingBox()` is generated with an argument for `accurate` but the javascript call fails if the argument is provided.
