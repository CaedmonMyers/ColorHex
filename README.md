# ColorHex
![Static Badge](https://img.shields.io/badge/Platforms-iOS%2013%2B%20%7C%20macOS%2010.15%2B%20%7C%20watchOS%206%2B%20%7C%20tvOS%2013%2B%20%7C%20visionOS-h)

ColorHex is a simple package for Swift apps. It allows you to easily work with hex codes in your app.

## Installation
To install with [Swift Package Manager](https://swift.org/package-manager/), add the following as a dependency to your `Package.swift`:

```swift
dependencies: [
    .package(url: "https://github.com/CaedmonMyers/ColorHex.git", from: "1.0.1")
]
```

Alternatively, you can install the package by downloading the ColorHex.swift and adding it to your project.
## Usage
**Show a color view from a hex string:**
```swift
import ColorHex

struct ContentView: View {
    var body: some View {
        Color(hex: "FFFFFF")
    }
}
```


**Use .toHex() with a color picker:**
```swift
ColorPicker("Color Picker", selection: $color)
.onChange(of: color) { oldValue, newValue in
let uiColor = UIColor(newValue)
let hexString = uiColor1.toHex()

spaces[selectedSpaceIndex].startHex = hexString
}
```

## Functions
- `Color(hex: "FFFFFF")`: View
- `.toHex()`: String?

You will need to properly handle the optional value for the .toHex() function in the event the conversion fails.
