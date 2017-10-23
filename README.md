# Trapezoidal Image Warp


[![WTFPL badge](http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-4.png)](http://www.wtfpl.net/)

android sample java code to show how to do 4 point image distortion using Matrix setPolytoPoly.

## Features
Uses Android's Matrix SetPolyToPoly to perform the perspective  image transform mapping (warp /deform / distort ) .

Could be used to shape an image to fit in any 4 point (4 sided) quadrilateral polygon, including:
Trapezoidal, Rhombus, Parallelogram, Rectangle, Square, Kite, etc.

Screenshots:

[https://developer.android.com/reference/android/graphics/Matrix.html#setPolyToPoly(float[],%20int,%20float[],%20int,%20int)](https://developer.android.com/reference/android/graphics/Matrix.html#setPolyToPoly(float[],%20int,%20float[],%20int,%20int))

Could probably be used to map any 2D graphics onto the siade /facet of a 3D polygon as well.

## Limitations /drawbacks/ Issues:

SetPolyToPoly has issues when the shape is concave or complex (see screenshots)

For a alternative /workaround for these shortcomings, one possible is to use the Android Canvas' drawBitmapMesh:

[https://developer.android.com/reference/android/graphics/Canvas.html#drawBitmapMesh%28android.graphics.Bitmap,%20int,%20int,%20float%5B%5D,%20int,%20int%5B%5D,%20int,%20android.graphics.Paint%29](https://developer.android.com/reference/android/graphics/Canvas.html#drawBitmapMesh%28android.graphics.Bitmap,%20int,%20int,%20float%5B%5D,%20int,%20int%5B%5D,%20int,%20android.graphics.Paint%29)

However to use drawBitmapMesh effectively you must be able to programmatically manipulate meshes.

The APIDemo BitmapMesh.java file is on Github here:

[https://github.com/appium/android-apidemos/blob/master/src/io/appium/android/apis/graphics/BitmapMesh.java](https://github.com/appium/android-apidemos/blob/master/src/io/appium/android/apis/graphics/BitmapMesh.java)

There aren't many Android examples /samples of using an onTouch event to warp an image using drawBitmapMesh so I may upload a zip with a working Eclipse workspace project to show how it works.. 

## License
WTFPL. See [LICENSE.md](https://cdn.rawgit.com/Evpok/latex-autocomplete/master/LICENSE.md)
