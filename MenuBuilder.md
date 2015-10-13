# Introduction #

`MenuInflater` asks for a [Menu](http://developer.android.com/reference/android/view/Menu.html) instance. However, Menu is an interface and not an implementation. I took `MenuBuilder` from the Android Open Source Project to be used in this project.

# Details #

You can create a new menu by calling `new MenuBuilder(context)`.

Example:

```
Menu m = new MenuBuilder(context);
getMenuInflater().inflate(R.menu.contextmenu, m);
IconContextMenu cm = new IconContextMenu(context, m);
```

There is also a shortcut:

```
IconContextMenu cm = new IconContextMenu(context, R.menu.contextmenu);
```