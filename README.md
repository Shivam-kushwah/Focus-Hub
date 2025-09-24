# Focus Hub 🎯

A smart productivity dashboard for Microsoft 365, built with Flutter and powered by Azure AI. This app unifies your calendar, tasks, and notes from across the Microsoft ecosystem into a single, seamless mobile experience.



---

## 🚀 About The Project

In a world of scattered information, Focus Hub was created to bring order to your daily productivity. This project was developed to demonstrate a comprehensive skill set in cross-platform mobile development, secure API integration with cloud services, and the practical application of AI.

It directly leverages the **Microsoft Graph API** and **Azure Cognitive Services** to create a powerful, user-centric tool that aligns with Microsoft's mission to empower every person to achieve more.

---

## ✨ Key Features

* **Secure Microsoft Authentication:** Log in safely using your official Microsoft account (personal, work, or school) via OAuth 2.0.
* **Unified Dashboard:** View your upcoming Outlook Calendar events and Microsoft To Do tasks in a single, organized view.
* **Interactive Task Management:** Create and complete tasks directly within the app, with all changes instantly synced to your Microsoft To Do account.
* **AI Note Scanner:** Use your phone's camera to take a picture of handwritten notes; the app uses **Azure AI** to perform OCR, digitizing the text and saving it to a new page in your OneNote.

---

## 🛠️ Tech Stack & Architecture

* **Frontend:** Flutter & Dart
* **State Management:** Provider
* **Backend Services:** Microsoft Graph API, Azure Cognitive Services
* **Authentication:** Microsoft Identity Platform (Azure Active Directory)

### System Architecture
The application communicates securely with Microsoft's cloud services to fetch and manage user data. The AI-powered OCR feature sends images to a dedicated Azure Cognitive Services endpoint for processing.



---

## 📸 Screenshots

| Login Screen | Dashboard |
| :----------: | :---------: |
| ![Login Screen](path/to/your/login_screenshot.png) | ![Dashboard Screen](path/to/your/dashboard_screenshot.png) |

---

## 🏁 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

* Flutter SDK installed.
* A free Azure account to get API keys.
* A Microsoft 365 / Outlook account for testing.

### Installation

1.  **Register your application in the Azure Portal.**
    * This is a crucial step to get the `Client ID` and `Tenant ID` required for authentication.
    * Ensure you grant the necessary API permissions in the portal: `User.Read`, `Calendars.Read`, `Tasks.ReadWrite`, and `Notes.ReadWrite`.

2.  **Clone the repository.**
    ```sh
    git clone [https://github.com/your_username/focus-hub.git](https://github.com/your_username/focus-hub.git)
    ```

3.  **Create a configuration file for your secrets.**
    * In the `lib/services/` directory, create a new file named `config.dart`.
    * Add your credentials to this file. This file should **NOT** be committed to Git.

    ```dart
    // lib/services/config.dart
    class AppConfig {
      static const String tenantId = 'YOUR_TENANT_ID_HERE';
      static const String clientId = 'YOUR_CLIENT_ID_HERE';
    }
    ```
    * Make sure to add `/lib/services/config.dart` to your `.gitignore` file.

4.  **Install dependencies.**
    ```sh
    flutter pub get
    ```

5.  **Run the app.**
    ```sh
    flutter run
    ```
---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
