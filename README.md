# Blender Bezier2JSON Exporter
First of all note that this script is hardly inspired on @qerrant's [BezierBlenderToUE](https://github.com/qerrant/BezierBlenderToUE) script.
We adapted it to export `json` instead of `csv`.

# Why this?
This plug-in commes from the necesity of avoiding handcrafting bezier curves mostly when they are related to some other geometry. Why can't we just export them
as we do with our `gltf` models? Remember that `gltf` doesn't support bezier data like points + handles info.

There's where this plug-in makes sense. Imagine you need a spline that travels through a castle model, to animate the camera position for example. Crafting
that by hand might be a pain in the ass 😬. Imagine that then for some reason you update your castle model, remove some rooms here and there and scale some
stuff, you have go back and update all the points by hand again to keep it consistent with the model. There's no reason to do that if you can just update it
on Blender working on the same context 🙏🏼.

# Installation
To use this plug-in just install it like any other custom Blender plug-in, it will add a new export type under `File > Export > Bezier2JSON (.json)`.
If you don't know how to install a custom plug-in [check this](https://youtu.be/cyt0O7saU4Q?t=33).

# How to use it (ThreeJS)
Once you have your `bezier.json` there's a piece of code that you'll need to parse it to ThreeJS interfaces, you can get it in [this example's code](https://github.com/basementstudio/basement-laboratory/blob/main/src/experiments/49.bezier-import.js)
you can also see a demo of how it works on the [example's live url](https://lab.basement.studio/experiments/49.bezier-import.js).
