# 📱 Namma-Shaale Inventory

![Namma-Shaale Banner](inventory_banner.png)

A modern, highly efficient Android application designed for schools in Karnataka to seamlessly register, track, audit, and manage physical assets (such as sports gear, laboratory tools, computers, and classroom equipment). 

Built using modern Android architecture, Jetpack Compose, and Room Database, Namma-Shaale Inventory provides a simple, structured, and user-friendly interface tailored for teachers.

---

## 📌 Problem Statement & Solution

### ❗ The Challenge
Government and public schools receive various resources (such as tablets, sports kits, and science lab apparatus) through funding. However, there is **no automated system to track their usage, condition, or location**. Items frequently get damaged, misplaced, or lost without accountability, leading to poor resource utilisation.

### 🎯 The Solution
**Namma-Shaale Inventory** acts as a **Digital Asset Auditor**. It empowers school administrators and teachers to:
- **Register Assets** immediately upon delivery.
- **Conduct Periodic Audits** (Monthly Health Checks) with just a few taps.
- **Log Issues & Report Damages** transparently.
- **Request Maintenance/Repairs** to preserve school infrastructure.
- **Access Visual Reports** on the overall inventory health.

---

## 🚀 Key Features

| Feature | Description | Screen |
| :--- | :--- | :--- |
| **📦 Asset Register** | Add details of assets including name, serial number, category, and purchase date. | `AssetRegistrationScreen` |
| **🔍 Condition Tracking** | Dynamically update item status: `WORKING`, `NEEDS_REPAIR`, `BROKEN`, or `LOST`. | `HealthCheckScreen` |
| **📝 Issue Logs** | Record damage details, reasons, and date of occurrences for non-functional assets. | `IssueLogScreen` |
| **🛠️ Maintenance requests** | Send and monitor items that need technical repair. Mark them resolved once working. | `RepairRequestScreen` |
| **📊 Dashboard** | An intuitive high-level dashboard displaying total assets, condition distribution, and quick action shortcuts. | `DashboardScreen` |
| **📈 Summary Reports** | Circular charts representing inventory health statistics. Supports exporting summaries. | `SummaryReportScreen` |

---

## 🛠️ Technology Stack & Architecture

- **UI Framework:** [Jetpack Compose](https://developer.android.com/compose) (100% Declarative Kotlin UI)
- **Design Language:** [Material Design 3 (M3)](https://m3.material.io/)
- **Database:** [Room SQLite Database](https://developer.android.com/training/data-storage/room) (Local persistence with reactive `Flow` integration)
- **State Management:** [ViewModel & LiveData](https://developer.android.com/topic/libraries/architecture/viewmodel)
- **Navigation:** [Jetpack Compose Navigation](https://developer.android.com/jetpack/compose/navigation)
- **Language:** Kotlin
- **Build System:** Gradle Kotlin DSL (`.kts`)

---

## 📂 Project Structure

```text
app/src/main/java/com/example/nammashaleinventery/
├── data/
│   ├── local/
│   │   ├── dao/
│   │   │   └── AssetDao.kt          # Room DAO for DB transactions
│   │   ├── database/
│   │   │   └── AppDatabase.kt       # App SQLite Room DB configuration & Converters
│   │   └── entities/
│   │       ├── Asset.kt             # Database entity model representing school assets
│   │       └── IssueLog.kt          # Database entity model representing logged issue reports
│   └── repository/
│       └── AssetRepository.kt       # Single source of truth for assets & issue log data
├── ui/
│   ├── assetlist/
│   │   └── AssetListScreen.kt       # Searchable and categorised inventory listing screen
│   ├── dashboard/
│   │   └── DashboardScreen.kt       # Main entry point with analytics and action cards
│   ├── healthcheck/
│   │   └── HealthCheckScreen.kt     # Perform asset condition audits quickly
│   ├── issuelog/
│   │   └── IssueLogScreen.kt        # Display list of registered issue history
│   ├── navigation/
│   │   └── Screen.kt                # Type-safe routing definitions
│   ├── registration/
│   │   └── AssetRegistrationScreen.kt # Screen to register new school assets
│   ├── repairs/
│   │   └── RepairRequestScreen.kt   # View items under maintenance and resolve status
│   ├── summary/
│   │   └── SummaryReportScreen.kt   # Visualise audit percentage and share reports
│   └── theme/
│       ├── Color.kt                 # Custom color scheme (School Navy, Success Green, etc.)
│       ├── Theme.kt                 # Material Theme Builder
│       └── Type.kt                  # Typography rules
├── viewmodel/
│   └── AssetViewModel.kt            # Business logic and UI state holder
└── MainActivity.kt                  # App entry point host containing Compose NavHost
```

---

## ⚙️ Installation & Usage

### Prerequisites
- [Android Studio Jellyfish / Koala](https://developer.android.com/studio) or newer
- JDK 17 or JDK 21 configured (Java 11 compatible source compilation)
- Android SDK 24+ (minSdk 24, targetSdk 36)

### Running Locally
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/Sreddy08840/Namma-Shaale-Inventory.git
   ```
2. Open the project in Android Studio.
3. Allow Gradle to sync and download required dependencies.
4. Run the application on your Android device or an Emulator:
   - Command line option:
     ```bash
     ./gradlew assembleDebug
     ```
   - Find the compiled debug APK at `app/build/outputs/apk/debug/app-debug.apk`.

---

## 👨‍💻 Authors & Contributors

- **VEERESHA** - Creator & Core Developer

## 🤝 Contributors

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/Sreddy08840">
        <img src="https://github.com/Sreddy08840.png" width="100px;" alt="Sreddy08840"/><br/>
        <sub><b>Sreddy08840</b></sub>
      </a><br/>
      <sub>🌱 Creator & Lead Developer</sub><br/>
      <sub>· Voice AI · </sub>
    </td>
  </tr>
</table>

---


## 📄 License
This project is for educational and public school infrastructure audit assistance purposes.
