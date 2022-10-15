<img src="https://i.imgur.com/49wEe0fl.png" width="100"/>

# Pin.swift
Swift library for positioning SwiftUI or UIKit views inside legacy UIKit apps


## SwiftUI
```swift
struct StatsText: SwiftUI.View {
        var body: some SwiftUI.View {
            HStack {
                Text("Stats")
                    .font(.system(size: 40, weight: .heavy, design: .default))
              Spacer()
            }
        }
    }
    
    // in viewDidLoad()
    addSwiftUI(StatsText(), top: 25, left: 18, w: 250, h: 44, clear: true)
```

## UIKit
```swift
let label: UILabel = {
        let l = UILabel()
        l.text = "Stats"
        l.font = UIFont.systemFont(ofSize: 40, weight: UIFont.Weight.heavy)
        return l
    }()
   
   
   
   viewDidLoad(){
         super.viewDidLoad();
         view.addSubview(label) // Do not forget to add label as a subview to UIViewController, otherwise the app will crash! 
         label.pin(a: .top, b: .left, ac: 25, bc: 18, w: view.frame.width, h: 44, to: nil)
   }
```


## Examples

### .pin
```swift
view.pin(a: .top, b: .center, ac: 200, bc: 0, w: 200, h: 30, to: nil)
```

### .bottomPin
```swift
map.bottomPin(top: 250, safe: false)
```

### .pinTo
```swift
view.pinTo(another, position: .bottom, h: 40, margin: 10)
```

