build-lists: true

# [fit] Debugging
## [fit] Tips and Techniques

---

## [fit]Salmo Junior

iOS developer since 2011, CocoaHeads Belo Horizonte chapter leader, traveller and cheese addict.

![right](../assets/Eu2.png)

<br><br><br><br><br><br><br><br><br>

Senior iOS Developer at CI&T
junior.salmo@gmail.com
@salmojr

---

# Agenda

- Advanced Breakpoints
- LLDB Debugger
- View Debugging

---

# [fit] Advanced Breakpoints

---

# Advanced Breakpoints

Xcode breakpoints offer a number of different features and making use of them we can bring our debug experience to another level.

- Add actions and conditions
- Inject code instructions at runtime
- Automate repetitive steps among tests
- Configure breakpoints for your user
- Share breakpoints with your team
- Improve Exception Breakpoint usage

---

# Adding actions and conditions


---

# Injecting code instructions at runtime


---

# Improve Exception Breakpoint usage


---

# Breakpoint Shortcuts 😁

Add/Remove breakpoint  =  command +  \\

Edit breakpoint  =  command + option + click

Breakpoints Navigator  =  command + 7

---

# Advanced Breakpoints
# [fit] Demo

---

# [fit] LLDB Debugger

---

# LLDB Debugger

- Type Lookup
- Watchpoints
- Stopping on Specific Errors
- Import Frameworks

---

# Xcode Debugging Area

![inline](https://developer.apple.com/library/content/documentation/DeveloperTools/Conceptual/debugging_with_xcode/Art/dwx-dt-debugarea-1_2x.png)

---

# Type Lookup


---

# Watchpoints


---

# Stopping on Specific Errors


---

# Import Frameworks


---

# LLDB Debugger
# [fit] Demo

---

# [fit] View Debugging

---

# View Debugging

- Xcode View Debugging
- iOS Simulator Debug
- UIDebuggingInformationOverlay

---

# Xcode View Debugging

Available since Xcode 6 this features helps to analize view layers and easily identify and fix issues in an app's user interface.

<br>

![inline left](https://cms-assets.tutsplus.com/uploads/users/473/posts/22530/image/capViewHierarchy.png)

![right](https://koenig-media.raywenderlich.com/uploads/2015/03/Screenshot-3.gif)

---

# iOS Simulator Debug

Simulator has some great features on Debug menu option to help find issues on app's user interface.

![inline](https://i.stack.imgur.com/HGl8i.png)

---

# UIDebuggingInformationOverlay

`UIDebuggingInformationOverlay` is a private `UIWindow` subclass created by Apple, presumably to help developers and designers debug Apple’s own iOS apps.

```Swift
let overlay = NSClassFromString("UIDebuggingInformationOverlay")
as? UIWindow.Type
_ = overlay?.perform(NSSelectorFromString("prepareDebuggingOverlay"))
```

<br><br><br><br><br><br><br><br>

![inline](http://images.clipartpanda.com/hypertension-clipart-9iREg9pie.png) Don't send it to production

![right 30%](http://ryanipete.com/blog/assets/images/uidebugginginformationoverlay_0.png)

---

# View Debugging
# [fit] Demo

---

<br><br><br><br><br><br><br><br>

# [fit] Questions?

---

# References

[https://developer.apple.com/support/debugging](https://developer.apple.com/support/debugging)

[http://ryanipete.com/blog/ios/swift/objective-c/uidebugginginformationoverlay/](http://ryanipete.com/blog/ios/swift/objective-c/uidebugginginformationoverlay/)

---

# [fit] Thanks 

# for being here

<br><br><br><br><br><br><br><br><br>

junior.salmo@gmail.com
@salmojr