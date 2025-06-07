# Custom Alert Usage

### Loading The Plugin
```
h5gg.require(7.8);

// Load the faketouch plugin
var myAlert = h5gg.loadPlugin("MyAlert", "serenityplugin.dylib");
if (!myAlert) alert("⚠️ serenityplugin.dylib load failed!");
```

### ChatGPT Example:

```
// Example 1: No argument
myAlert.alert0();

// Example 2: One argument
myAlert.alert1("Hello from JavaScript!");

// Example 3: Two arguments (title + message)
myAlert.alert2("Custom Title", "This is a custom message from JS");

// Example 4: Simple choice dialog
myAlert.choice(["Option 1", "Option 2", "Option 3"], function(result) {
    if (result !== null) {
        console.log("Selected:", result);
    } else {
        console.log("Cancelled");
    }
});

// Example 5: Flexible choice dialog
myAlert.flexChoice({
    title: "Pick a Color",
    message: "Choose your favorite color below:",
    items: [
        { title: "Red", description: "The color of fire", js: "console.log('Red selected')" },
        { title: "Green", description: "The color of nature", js: "console.log('Green selected')" },
        { title: "Blue", description: "The color of the sky", js: "console.log('Blue selected')" }
    ],
    cancelTitle: "Maybe Later"
}, function(result) {
    if (result !== null) {
        console.log("You selected:", result.title);
    } else {
        console.log("Dialog was cancelled.");
    }
});

// Example 6: Flexible alert with JS code
myAlert.flexAlert({
    title: "Welcome",
    message: "This is a dynamic alert",
    buttonTitle: "Got it",
    js: "console.log('Alert dismissed')"
});
```

To use JS please use the flexAlert.
