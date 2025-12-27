# Health & Activity Tracker

這是一個基於 SwiftUI 開發的全方位健康活動追蹤 iOS App。使用者可以記錄日常運動、飲水與睡眠數據，設定個人目標，並透過圖表分析每週進度。此外，App 結合了即時天氣資訊與貼心的使用提示 (TipKit)，提供良好的使用者體驗。

## 📱 介面展示 (App Preview)

<p align="center">
  <img src="health_app_screen.gif" alt="Login & Home" width="300" />
</p>

## ✨ 主要功能 (Features)

### 1. 使用者管理系統 (User Management)
* **註冊與登入**：支援帳號註冊、登入驗證及「保持登入」功能 (UserDefaults)。
* **個人檔案設定**：可更換大頭貼、編輯聯絡電話、設定性別與生日。
* **密碼管理**：支援修改密碼功能，具備舊密碼驗證與新密碼確認機制。
* **地區設定**：可選擇國家與城市，這將連動天氣資訊的顯示。

### 2. 活動追蹤 (Activity Tracking)
* **多樣化記錄**：支援三種活動類型：
    * 🏋️ **運動 (Exercise)**：記錄消耗卡路里、開始與結束時間。
    * 💧 **飲水 (Hydration)**：記錄飲水量 (ml)。
    * 😴 **睡眠 (Sleep)**：自動計算睡眠時長 (hrs)。
* **CRUD 操作**：使用者可以新增、查看、編輯與刪除活動記錄。
* **搜尋與篩選**：支援關鍵字搜尋及自訂日期範圍篩選。

### 3. 目標設定 (Goal Setting)
* **設定目標**：針對不同活動類型設定數值目標（如：每日喝水 2000ml）。
* **進度可視化**：透過進度條顯示完成度，包含已完成數值與剩餘數值。
* **達成獎勵**：當目標進度達到 100% 時，會顯示 Lottie 動畫 ("Check Mark") 給予回饋。

### 4. 數據分析 (Data Analysis)
* **每週圖表**：使用 **Swift Charts** 繪製每週趨勢圖（折線圖），可切換查看運動、飲水或睡眠數據。
* **統計摘要**：自動計算一週的總量與平均值（如：平均每日睡眠時數）。

### 5. 即時天氣 (Live Weather)
* **OpenWeatherMap 整合**：根據使用者設定的城市，即時抓取溫度、體感溫度、濕度、風速等資訊。
* **懸浮天氣小工具**：主畫面包含一個可拖曳的懸浮天氣圖示，點擊可查看詳細天氣卡片。

### 6. 使用者體驗優化 (UX Enhancements)
* **TipKit 提示**：首次使用時，提供功能引導提示（如：如何新增記錄、如何切換圖表）。
* **Lottie 動畫**：整合 Lottie-ios 套件，豐富視覺互動。

## 🛠 技術架構 (Tech Stack)

* **語言**：Swift 5.0+
* **框架**：SwiftUI
* **資料持久化**：**SwiftData** (iOS 17+)
* **圖表繪製**：Swift Charts
* **網路請求**：URLSession (串接 OpenWeatherMap API)
* **第三方套件**：
    * [Lottie-ios](https://github.com/airbnb/lottie-ios) (透過 Swift Package Manager 管理)
* **其他框架**：TipKit, Combine

## 📱 系統需求 (Requirements)

* **iOS 版本**：iOS 18.0 (根據專案設定)
* **Xcode 版本**：Xcode 16.0 或以上

## 🚀 安裝與執行 (Installation)

1.  **複製專案**：
    下載並解壓縮專案檔案。
2.  **開啟專案**：
    使用 Xcode 開啟 `01157025_final.xcodeproj`。
3.  **套件下載**：
    Xcode 會自動透過 SPM 下載 `Lottie` 套件，請等待下載完成。
4.  **設定簽署**：
    前往專案設定的 `Signing & Capabilities`，選擇您的開發者帳號 (Team)。
5.  **編譯並執行**：
    選擇模擬器 (如 iPhone 16) 或實體裝置，按下 `Cmd + R` 執行。

## 📂 專案結構 (Project Structure)

* `Model/`: `User.swift`, `ActivityRecord.swift`, `Goal.swift`, `WeatherModel.swift`
* `View/`: `LoginView.swift`, `MaintabView.swift`, `ActivityListView.swift`, `AnalysisView.swift`, `GoalView.swift`, `UserView.swift`
* `Utils/`: `Tip.swift`

## 👤 作者 (Author)

* **Student ID**: 01157025
* **Created Date**: 2024/11/28
* **Medium Blog**: [點擊閱讀開發心得](https://medium.com/%E6%B5%B7%E5%A4%A7-ios-app-%E7%A8%8B%E5%BC%8F%E8%A8%AD%E8%A8%88/ios%E6%87%89%E7%94%A8%E7%A8%8B%E5%BC%8F%E9%96%8B%E7%99%BC%E5%85%A5%E9%96%80-04-swiftui-ios-app-%E5%85%A5%E9%96%80%E8%AA%B2%E7%A8%8B%E6%9C%9F%E6%9C%AB%E5%B0%88%E9%A1%8C%E4%B8%80-crud-%E7%B4%80%E9%8C%84-app-4b5af097cefa) ✍️
