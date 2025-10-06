# ShwaasSaathi - Breathing Exercise iOS App

<div align="center">
  <img src="https://img.shields.io/badge/iOS-26.0+-blue.svg" alt="iOS Version">
  <img src="https://img.shields.io/badge/Swift-5.0-orange.svg" alt="Swift Version">
  <img src="https://img.shields.io/badge/Xcode-17.0+-blue.svg" alt="Xcode Version">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
</div>

## 📱 Overview

**ShwaasSaathi** (Sanskrit: श्वास साथी - "Breathing Companion") is a comprehensive iOS breathing exercise app designed to help users improve their respiratory health through guided breathing techniques. The app features three scientifically-backed breathing exercises with visual instructions, progress tracking, and multi-language support.

## ✨ Features

### 🫁 Breathing Exercises
- **Diaphragmatic Breathing**: Strengthens diaphragm and improves breathing efficiency
- **Pursed-lip Breathing**: Controls shortness of breath and releases trapped air  
- **Segmental Breathing**: Targets specific lung segments for better ventilation

### 🎯 Core Functionality
- **Interactive Visual Instructions**: Step-by-step animated guides for each exercise
- **Audio Guidance**: Voice instructions with multi-language support
- **Progress Tracking**: Session history, streaks, and performance analytics
- **Achievement System**: Unlock badges for milestones and consistency
- **CloudKit Integration**: Seamless data sync across devices
- **Haptic Feedback**: Enhanced user experience with tactile responses

### 🌍 Accessibility & Localization
- **Multi-language Support**: English, Hindi, Gujarati, Marathi
- **Dark Mode**: Adaptive UI for different lighting conditions
- **Accessibility Features**: VoiceOver support, large text, high contrast
- **Responsive Design**: Optimized for all iPhone screen sizes

## 🏗️ Architecture

### 📁 Project Structure

```
ShwaasSaathi/
├── 📱 App/
│   ├── ShwaasSaathiApp.swift          # App entry point
│   └── ContentView.swift              # Legacy main view
├── 🎨 Views/
│   ├── MainTabView.swift              # Tab navigation
│   ├── HomeView.swift                 # Dashboard & quick actions
│   ├── ExercisesView.swift            # Exercise selection
│   ├── ExerciseDetailView.swift       # Exercise information
│   ├── BreathingSessionView.swift     # Active session interface
│   ├── VisualInstructionsView.swift   # Animated exercise guides
│   ├── ProgressView.swift             # Analytics & history
│   ├── BadgesView.swift               # Achievement system
│   └── SettingsView.swift             # App configuration
├── 🧠 ViewModels/
│   ├── BreathingSessionViewModel.swift # Session state management
│   └── ProgressViewModel.swift        # Progress data handling
├── 📊 Models/
│   ├── BreathingExercise.swift        # Exercise definitions
│   ├── Badge.swift                    # Achievement system
│   └── CoreDataModels.swift           # Core Data entities
├── 🔧 Services/
│   ├── DataManager.swift              # Core Data operations
│   ├── PersistenceController.swift    # CloudKit integration
│   ├── AudioManager.swift             # Voice guidance
│   ├── HapticManager.swift            # Tactile feedback
│   └── NotificationManager.swift      # Local notifications
├── 🎨 Utils/
│   ├── UIComponents.swift             # Reusable UI elements
│   ├── ColorScheme.swift              # Design system
│   └── AnimationHelpers.swift         # Animation utilities
├── 🌍 Localization/
│   ├── LocalizationManager.swift      # Language management
│   ├── en.lproj/                      # English strings
│   ├── hi.lproj/                      # Hindi strings
│   ├── gu.lproj/                      # Gujarati strings
│   └── mr.lproj/                      # Marathi strings
└── 📦 Resources/
    ├── Assets.xcassets/               # App icons & images
    ├── ShwaasSaathi.xcdatamodeld/     # Core Data model
    └── Info.plist                     # App configuration
```

### 🏛️ Design Patterns

- **MVVM Architecture**: Clean separation of concerns with ViewModels
- **Singleton Pattern**: Shared managers (DataManager, AudioManager, etc.)
- **Observer Pattern**: Combine framework for reactive programming
- **Repository Pattern**: DataManager abstracts Core Data operations
- **Factory Pattern**: Exercise and badge creation

## 🛠️ Technical Stack

### 📱 iOS Frameworks
- **SwiftUI**: Modern declarative UI framework
- **Core Data**: Local data persistence
- **CloudKit**: Cloud synchronization
- **AVFoundation**: Audio playback and speech synthesis
- **UserNotifications**: Local notification scheduling
- **Combine**: Reactive programming

### 🎨 Design System
- **Human Interface Guidelines**: Apple's design principles
- **Glass Morphism**: Modern translucent UI elements
- **Adaptive Colors**: Dynamic color system supporting light/dark modes
- **Typography Scale**: Consistent font sizing hierarchy
- **Spacing System**: Standardized layout measurements

### 📊 Data Management
- **Core Data Stack**: Local persistence with CloudKit sync
- **Entity Relationships**: Normalized data structure
- **Migration Support**: Schema versioning for updates
- **Background Processing**: Efficient data operations

## 🚀 Getting Started

### Prerequisites
- Xcode 17.0 or later
- iOS 26.0+ deployment target
- Apple Developer Account (for CloudKit)
- macOS Sequoia or later

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ShwaasSaathi.git
   cd ShwaasSaathi
   ```

2. **Open in Xcode**
   ```bash
   open ShwaasSaathi.xcodeproj
   ```

3. **Configure CloudKit**
   - Enable CloudKit capability in project settings
   - Configure container identifier: `iCloud.com.arpitpatel.ShwaasSaathi`
   - Set up CloudKit schema in CloudKit Console

4. **Build and Run**
   - Select target device/simulator
   - Press `Cmd + R` to build and run

### Configuration

#### CloudKit Setup
1. Open CloudKit Console
2. Create new container or use existing
3. Configure record types:
   - `BreathingSession`
   - `UserProgress`
4. Enable CloudKit in Xcode capabilities

#### Localization
- Add new language in Xcode project settings
- Create corresponding `.lproj` folder
- Translate `Localizable.strings` file

## 📱 App Flow

### 🏠 Home Screen
- **Greeting**: Time-based personalized welcome
- **Quick Stats**: Streak, sessions, level display
- **Today's Goal**: Progress toward daily target
- **Quick Start**: Popular exercise shortcuts
- **Recent Activity**: Session history preview

### 🫁 Exercise Selection
- **Categories**: Organized by purpose (relaxation, energy, focus, recovery)
- **Exercise Cards**: Visual preview with difficulty and duration
- **Filtering**: Search and category-based filtering

### 🎯 Breathing Session
- **Visual Guide**: Animated breathing instructions
- **Audio Cues**: Spoken guidance in selected language
- **Progress Tracking**: Real-time session progress
- **Phase Indicators**: Current breathing phase display
- **Controls**: Play, pause, stop functionality

### 📊 Progress Analytics
- **Statistics**: Comprehensive session analytics
- **Charts**: Visual progress representation
- **Streaks**: Consistency tracking
- **History**: Detailed session logs

### 🏆 Achievement System
- **Badge Categories**: Various achievement types
- **Progress Indicators**: Visual progress toward next badge
- **Unlock Animations**: Celebratory badge reveals

## 🎨 Design System

### Color Palette
```swift
// Primary Colors
static let primaryBlue = Color(red: 0.0, green: 0.478, blue: 1.0)
static let breathingMint = Color(red: 0.0, green: 0.780, blue: 0.745)
static let breathingPurple = Color(red: 0.749, green: 0.352, blue: 1.0)
static let breathingOrange = Color(red: 1.0, green: 0.584, blue: 0.0)

// Semantic Colors
static let backgroundPrimary = Color(UIColor.systemBackground)
static let textPrimary = Color(UIColor.label)
static let statusSuccess = Color(UIColor.systemGreen)
```

### Typography
```swift
// Display Fonts
static let displayLarge = Font.system(size: 57, weight: .regular)
static let headlineSmall = Font.system(size: 24, weight: .regular)

// Body Fonts
static let bodyLarge = Font.system(size: 16, weight: .regular)
static let labelMedium = Font.system(size: 12, weight: .medium)
```

### Spacing System
```swift
struct Spacing {
    static let xs: CGFloat = 4
    static let sm: CGFloat = 8
    static let md: CGFloat = 16
    static let lg: CGFloat = 24
    static let xl: CGFloat = 32
}
```

## 🔧 Core Components

### BreathingSessionViewModel
Manages active breathing session state:
- Timer management for session and breathing phases
- Progress calculation and phase transitions
- Audio instruction coordination
- Session data persistence

### DataManager
Handles all Core Data operations:
- Session CRUD operations
- User progress calculations
- Badge unlock logic
- CloudKit synchronization

### AudioManager
Provides voice guidance:
- Text-to-speech synthesis
- Multi-language support
- Audio session management
- Background audio capability

### LocalizationManager
Manages app localization:
- Dynamic language switching
- String resource management
- Locale-specific formatting

## 🌍 Localization

### Supported Languages
- **English** (en): Primary language
- **Hindi** (hi): हिंदी support
- **Gujarati** (gu): ગુજરાતી support  
- **Marathi** (mr): मराठी support

### Adding New Languages
1. Add language in Xcode project settings
2. Create new `.lproj` folder
3. Copy and translate `Localizable.strings`
4. Update `LocalizationManager.swift` with language code mapping

## 📊 Data Model

### Core Data Entities

#### BreathingSession
```swift
@NSManaged public var sessionID: UUID?
@NSManaged public var exerciseType: String?
@NSManaged public var duration: Double
@NSManaged public var repetitions: Int32
@NSManaged public var date: Date?
```

#### UserProgress
```swift
@NSManaged public var userID: UUID?
@NSManaged public var totalSessions: Int32
@NSManaged public var currentStreak: Int32
@NSManaged public var longestStreak: Int32
@NSManaged public var level: Int32
@NSManaged public var lastSessionDate: Date?
@NSManaged public var unlockedBadges: [String]?
```

## 🏆 Achievement System

### Badge Types
- **First Breath**: Complete first session
- **3-Day Warrior**: 3-day streak
- **Weekly Champion**: 7-day streak
- **Monthly Master**: 30-day streak
- **Lung Hero**: 50 total sessions
- **Breathing Master**: Try all exercise types
- **Consistency King**: 21-day streak
- **Exercise Explorer**: Complete all exercises

### Unlock Logic
Badges are automatically unlocked based on user progress:
- Session count milestones
- Streak achievements
- Exercise variety completion
- Consistency rewards

## 🔒 Privacy & Security

### Data Protection
- **Local Storage**: Core Data with encryption
- **CloudKit Sync**: End-to-end encrypted
- **No Third-party Analytics**: Privacy-first approach
- **Minimal Permissions**: Only necessary system access

### User Control
- **Data Export**: Complete data portability
- **Data Deletion**: Full data removal option
- **Sync Control**: Optional CloudKit synchronization

## 🧪 Testing

### Unit Tests
- ViewModel logic testing
- Data manager operations
- Localization functionality
- Badge unlock algorithms

### UI Tests
- Navigation flow testing
- Session interaction testing
- Accessibility compliance
- Multi-language support

### Performance Testing
- Core Data performance
- Animation smoothness
- Memory usage optimization
- Battery impact assessment

## 📈 Performance Optimization

### Memory Management
- Weak references in closures
- Proper timer invalidation
- Efficient Core Data fetching
- Image asset optimization

### Battery Efficiency
- Background processing limits
- Efficient animation techniques
- Optimized CloudKit sync
- Smart notification scheduling

## 🚀 Deployment

### App Store Requirements
- iOS 26.0+ deployment target
- Privacy policy compliance
- Accessibility guidelines adherence
- App Store Review Guidelines compliance

### Build Configuration
```swift
// Release configuration
SWIFT_OPTIMIZATION_LEVEL = -O
ENABLE_BITCODE = YES
VALIDATE_PRODUCT = YES
```

## 🤝 Contributing

### Development Guidelines
1. Follow Swift style guide
2. Maintain MVVM architecture
3. Add unit tests for new features
4. Update localization strings
5. Document public APIs

### Pull Request Process
1. Fork the repository
2. Create feature branch
3. Implement changes with tests
4. Update documentation
5. Submit pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Arpit Patel** - *Initial work* - [@arpitpatel](https://github.com/arpit15006)

## 🙏 Acknowledgments

- Apple Human Interface Guidelines
- iOS Accessibility Guidelines
- SwiftUI Documentation
- Core Data Programming Guide
- CloudKit Documentation

## 📞 Support

For support, email arpit6814@gmail.com or create an issue in this repository.

---

<div align="center">
  <p>Made with ❤️ for better breathing and wellness</p>
  <p>© 2024 ShwaasSaathi. All rights reserved.</p>
</div>
