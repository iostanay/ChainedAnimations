# SwiftUI ChainedAnimation Demo

A delightful SwiftUI animation showcase featuring interactive sun and sports ball animations using PhaseAnimator.

## 🌟 Features

- Interactive sun animation with dynamic scaling and rotation
- Synchronized baseball and soccer ball rotation system
- Phase-based animation using SwiftUI's PhaseAnimator
- Simple trigger mechanism for animation control
- Smooth transitions and fluid movements


## 🔧 Requirements

- iOS 17.0+
- Xcode 15.0+
- Swift 5.9+

## 🚀 Installation

1. Clone the repository:
```bash
git clone https://github.com/iostanay/ChainedAnimations.git
```

2. Open the project in Xcode:
```bash
cd ChainedAnimations
open ChainedAnimations.xcodeproj
```

3. Build and run the project using Cmd + R

## 💻 Usage

The animation can be triggered with a simple button tap. Here's how it works:

```swift
Button {
    trigger.toggle()
} label: {
    Text("Animate")
        .fontWeight(.heavy)
        .foregroundStyle(.white)
        .padding()
        .background(.green)
        .cornerRadius(5.0)
}
```

## 🔍 Implementation Details

The project demonstrates several SwiftUI animation techniques:

1. **Sun Animation:**
   - Uses PhaseAnimator for rotation and scaling
   - Implements smooth transition effects
   - Combines multiple transformations

2. **Sports Ball Animation:**
   - Synchronized rotation of soccer ball and baseball
   - Custom phase-based animation timing
   - Coordinated movement patterns

## 🎯 Key Components

- `PhaseAnimator`: Used for creating smooth, phase-based animations
- `symbolRenderingMode`: Ensures proper rendering of SF Symbols
- State management using `@State` property wrapper
- Custom animation timing and curves

## 📖 Documentation

The main animation components are implemented in `ContentView.swift`:

```swift
PhaseAnimator([360, 0], trigger: trigger) { phase in
    ZStack {
        Image(systemName: "soccerball")
            .resizable()
            .frame(width: 120, height: 120)
            .rotationEffect(.degrees(Double(phase - 360)))
        // ... more code
    }
}
```







