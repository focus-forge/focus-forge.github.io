# FocusFor⚒️e

**FocusFor⚒️e** is a comprehensive iOS productivity app designed to help users stay focused, build better habits, and maximize their time through intelligent app blocking, routine management, and fitness integration.

![iOS](https://img.shields.io/badge/iOS-18.5%2B-blue)
![Swift](https://img.shields.io/badge/Swift-5.9-orange)
![SwiftUI](https://img.shields.io/badge/SwiftUI-Framework-green)
![Xcode](https://img.shields.io/badge/Xcode-16.0-blue)

---

## ✨ Features

### 🔥 Core Productivity Tools

- **Sticky Timer**: Advanced Pomodoro-style timer with pause/resume functionality
- **App Blocking**: Two-tier blocking system
  - **Loose Block** (Free): Limited bypasses with customizable attempts
  - **Strict Block** (Pro): Unbreakable blocking with zero bypasses
- **Daily Routines**: Schedule and manage recurring habits with time-based triggers
- **Task Management**: Complete task system with categories, priorities, and completion tracking
- **Progress Analytics**: Detailed statistics and insights on your productivity

### 💪 Fitness Integration

- **Workout Scheduling**: Plan workouts throughout your day
- **Exercise Library**: Pre-built workout plans with detailed instructions
- **Custom Workouts**: Create your own exercise routines
- **Fitness Tracking**: Integration with HealthKit for comprehensive tracking
- **Today's Workouts**: Clear view of upcoming and completed sessions

### 🏆 Gamification

- **Challenges System**: Productivity challenges with streak tracking
- **Achievement Unlocking**: Earn rewards for consistent focus
- **Progress Visualization**: Beautiful charts and graphs

### 💎 Pro Features

- Strict Block (unbreakable app blocking)
- Unlimited routines
- Advanced analytics
- Custom themes (coming soon)
- Web dashboard access (coming soon)

---

## 🛠️ Technology Stack

- **Language**: Swift 5.9
- **Framework**: SwiftUI
- **Minimum iOS Version**: 18.5+
- **Architecture**: MVVM with ObservableObject managers
- **Key Frameworks**:
  - `FamilyControls` - Screen Time API for app blocking
  - `HealthKit` - Fitness tracking integration
  - `StoreKit` - In-app purchases
  - `Combine` - Reactive programming

### Third-Party Services

- **[Superwall](https://superwall.com)** - Paywall and subscription management
- **[Supabase](https://supabase.com)** - Backend and authentication (configured)

---

## 📱 Screenshots

*(Add screenshots here)*

---

## 🚀 Getting Started

### Prerequisites

- macOS 14.0+ (Sonoma or later)
- Xcode 16.0+
- iOS 18.5+ device or simulator
- Apple Developer account (for Screen Time API)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/FocusForge.git
   cd FocusForge
   ```

2. **Open in Xcode**
   ```bash
   open FocusForge.xcodeproj
   ```

3. **Configure Signing**
   - Select the FocusForge target
   - Go to "Signing & Capabilities"
   - Select your development team
   - Repeat for FocusForgeShield and FocusForgeShieldAction targets

4. **Add API Keys** (Optional)

   Create a `Config.swift` file (not tracked by git):
   ```swift
   struct Config {
       static let superwallAPIKey = "YOUR_SUPERWALL_KEY"
       static let supabaseURL = "YOUR_SUPABASE_URL"
       static let supabaseAnonKey = "YOUR_SUPABASE_KEY"
   }
   ```

5. **Build and Run**
   - Select a device or simulator
   - Press `Cmd + R` to build and run

---

## 📂 Project Structure

```
FocusForge/
├── FocusForge/                  # Main app target
│   ├── FocusFlowApp.swift      # App entry point
│   ├── ContentView.swift       # Main view with all tabs
│   ├── OnboardingFlow.swift    # Onboarding screens
│   ├── Managers/
│   │   ├── SuperwallManager    # Paywall handling
│   │   ├── SupabaseManager     # Backend integration
│   │   ├── FitnessManager      # Workout tracking
│   │   └── BlockManager        # App blocking logic
│   ├── Views/
│   │   ├── FitnessTabView      # Fitness UI
│   │   ├── InterventionView    # Blocking interventions
│   │   └── ...
│   └── Models/
│       ├── FitnessModels       # Workout data structures
│       └── OnboardingModels    # Onboarding data
├── FocusForgeShield/           # Screen Time shield extension
├── FocusForgeShieldAction/     # Shield action handler
└── Documentation/
    ├── GITHUB_SETUP.md
    ├── FREE_TIER_WITHOUT_ACCOUNTS.md
    ├── ACCOUNTS_VS_NO_ACCOUNTS.md
    └── ...
```

---

## 🎨 App Blocking System

### Loose Block (Free Tier)
- Configurable bypass attempts (default: 3)
- Customizable time per attempt (default: 5 minutes)
- Intervention screens with motivational messages
- Perfect for building discipline

### Strict Block (Pro)
- Zero bypasses - truly unbreakable
- Uses iOS Screen Time API
- Custom app selection via FamilyActivityPicker
- Ideal for deep focus sessions

---

## 📊 Key Features Breakdown

### Sticky Timer
- Multiple preset durations (25, 45, 60, 90 minutes)
- Custom time selection
- Pause/Resume with preserved state
- Automatic app blocking integration
- Visual countdown display

### Routines Management
- Create unlimited routines (2 for free, unlimited for Pro)
- Set specific times and days
- Automatic triggering based on schedule
- Edit and delete with confirmation
- Beautiful card-based UI

### Task System
- Five categories: Work, Personal, Health, Learning, Other
- Four priority levels: Low, Medium, High, Urgent
- Complete/Uncomplete tasks with one tap
- Context menus for quick actions
- Completion statistics and tracking

### Fitness Integration
- Schedule workouts for specific times
- Pre-built exercise library
- Custom workout creator
- Exercise instructions with animations
- Workout completion tracking
- Today's view with upcoming/completed sections

---

## 🔐 Permissions Required

FocusForge requires the following permissions:

1. **Screen Time** - For app blocking functionality
2. **Notifications** - For routine and timer alerts (optional)
3. **HealthKit** - For fitness tracking (optional)

All permissions are requested during onboarding with clear explanations.

---

## 💰 Monetization

### Free Tier
- Loose Block with limited bypasses
- 2 routines
- Basic task management
- Basic analytics
- Core fitness features

### Pro Tier
**Annual:** $29.99/year (3-day free trial)
**Weekly:** $5.99/week (3-day free trial)

**Features:**
- Strict Block (unbreakable)
- Unlimited routines
- Advanced analytics
- Priority support
- Future features (web dashboard, AI insights)

Subscription handled via Superwall.

---

## 🐛 Known Issues

- [ ] Superwall events may not fire correctly on first launch
- [ ] HealthKit integration requires additional testing
- [ ] Some SwiftUI deprecation warnings (iOS 17 compatibility)

See [Issues](https://github.com/YOUR_USERNAME/FocusForge/issues) for full list.

---

## 🚧 Roadmap

- [ ] iPad optimization
- [ ] Web dashboard
- [ ] AI-powered insights
- [ ] Social features (accountability partners)
- [ ] Apple Watch companion app
- [ ] Siri Shortcuts integration
- [ ] Widget support
- [ ] Cross-device sync

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Built with **SwiftUI** and modern iOS frameworks
- Paywall powered by **Superwall**
- Backend by **Supabase**
- Icons from **SF Symbols**
- Developed with assistance from **Claude Code**

---

## 📧 Contact

For questions, suggestions, or issues:
- Open an issue on GitHub
- Email: caazamar@gmail.com

---

## ⭐ Show Your Support

If you find FocusForge helpful, please consider:
- Starring this repository
- Sharing with friends
- Contributing to the codebase
- Reporting bugs and suggesting features

---

**Made with ❤️ for productivity enthusiasts**

🤖 *Initial codebase generated with [Claude Code](https://claude.com/claude-code)*
