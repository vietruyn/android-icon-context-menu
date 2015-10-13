# Context Menu with Icons #

In Android, context menus (1) can't have icons (2) cannot be flexibly created and destroyed. With this embeddable library, you get a context menu that solves both problems.

Sample (from [Hi-Q MP3 Recorder](https://market.android.com/details?id=yuku.mp3recorder.full)):

![http://lh5.ggpht.com/_ODdyLCCXPpQ/TSbQ--iLdFI/AAAAAAAAwcc/6zm8eak2qIE/s640/device.png](http://lh5.ggpht.com/_ODdyLCCXPpQ/TSbQ--iLdFI/AAAAAAAAwcc/6zm8eak2qIE/s640/device.png)

Consistency to Android platform is maintained by not using custom layouts, instead it uses internal layouts only.

## How to use ##

You can easily add this project as a [library project](http://developer.android.com/guide/developing/eclipse-adt.html#libraryProject) in Eclipse.

  1. Create a menu in XML as what you would do when you create a normal (options) menu. Specify the drawables as usual. You can also create the menu on-the-fly by using MenuBuilder which implements Menu.
  1. Create the Context Menu with Icons by calling `IconContextMenu cm = new IconContextMenu(context, R.menu.contextmenu)`
  1. Create, and then set the context menu handler by calling `setOnIconContextItemSelectedListener(IconContextItemSelectedListener)`.
  1. (Optional) set additional info to differentiate sources, e.g. the position of the item on the list that was clicked. `cm.setInfo(position)`
  1. Open the context menu by calling `show()`.

See also other projects for Android:
  * [Android Color Picker](http://code.google.com/p/android-color-picker/)
