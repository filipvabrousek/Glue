# Glue.swift
Swift library which positions SwiftUI Views in UIKit


### SwiftUI
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
    
    addSwiftUI(StatsText(), top: 25, left: 18, w: 250, h: 44, clear: true)
```

### UIKit
```swift
let label: UILabel = {
        let l = UILabel()
        l.text = "Stats"
        l.font = UIFont.systemFont(ofSize: 40, weight: UIFont.Weight.heavy)
        return l
    }()
   
   label.pin(a: .top, b: .left, ac: 25, bc: 18, w: view.frame.width, h: 44, to: nil)
```


