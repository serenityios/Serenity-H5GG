# 🖱️ Auto Click Usage

How to use the Autoclick Feature in our H5GG Plugin

### 🔌 Loading the Plugin

```
h5gg.require(7.8);

// Load serenity plugin
var autoclick = h5gg.loadPlugin("AutoClick", "serenityplugin.dylib");
if (!autoclick) alert("⚠️ serenityplugin.dylib load failed!");
```
### 👀 Showing the Autoclick Circle
A Draggable Circle will show letting you drag it where you want it to autoclick
```
// Show the Circle to drag for autoclicking
autoclick.show();
```

### ▶️ Starting the Autoclicker
To Start the Autoclicker, this is the JS Function
```
// Start the Autoclick with 1 Click per MS
autoclick.start(0.01);
```

### ⏹️ Stopping the Autoclicker
Need a break?
```
autoclick.stop();
```

### 🫣 Hiding the Autoclicker
Need to remove & stop the Autoclicker from your screen for a moment? Use this JS Function

```
autoclick.hide();
```

Thats it!
