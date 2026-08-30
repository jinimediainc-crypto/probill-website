<div align="center">

# 📊 Google Play Store ASO & Release Master Manual
### *Optimization Strategy, Keystore Signatures & Release Runbook for `com.jinimedia.probill_invoice_estimate`*

</div>

---

## 🎯 App Store Funnel Conversion Architecture

```mermaid
graph TD
    A["🔍 Organic Search / AdMob Campaign\n('Invoice Maker', 'Estimate Builder', 'POS Thermal')"] --> B["🖼️ Store Impression\n(App Icon V1 + Feature Graphic Banner)"]
    B --> C["📄 Product Details Page View\n(Short Description + 5 Marketing Mockup Screenshots)"]
    C --> D["📲 High-Intent Installation\n(Under 30MB fast download, zero login barrier)"]
    D --> E["⚡ Instant 30-Second First Invoice\n(100% Offline SQLite, Pre-filled Trade SOP)"]
    E --> F["⭐️ 5-Star Store Review & Pro Upgrade\n(In-App Review Prompt + WhatsApp Sharing)"]
```

---

## 📋 Google Play Store Listing Copy Specifications

```mermaid
pie title Listing Copy Character Utilization
    "App Title Used (29)" : 29
    "App Title Remaining (1)" : 1
    "Short Description Used (77)" : 77
    "Short Description Remaining (3)" : 3
```

| Console Input Field | Production Metadata | Character Count / Limit | Compliance Status |
| :--- | :--- | :---: | :---: |
| **App Title** | `ProBill: Estimates & Invoices` | **29 / 30** | ✅ 100% Compliant |
| **Short Description** | `Fast offline invoice maker, estimates, POS thermal receipts & tax calculator.` | **77 / 80** | ✅ 100% Compliant |
| **Package Name** | `com.jinimedia.probill_invoice_estimate` | Reverse Domain | ✅ Certified |
| **Category** | Business / Productivity / Finance | Store Standard | ✅ Verified |
| **Developer Email** | `jinimedia.inc@gmail.com` | Official Support | ✅ Active |
| **Privacy Policy URL** | `https://jinimediainc-crypto.github.io/probill-website/privacy-policy.html` | HTTPS Static | ✅ Live |
| **Terms of Use URL** | `https://jinimediainc-crypto.github.io/probill-website/terms-of-use.html` | HTTPS Static | ✅ Live |
| **Data Safety URL** | `https://jinimediainc-crypto.github.io/probill-website/data-safety.html` | HTTPS Static | ✅ Live |
| **app-ads.txt URL** | `https://jinimediainc-crypto.github.io/probill-website/app-ads.txt` | Direct Seller | ✅ Certified |

---

## 🔑 Production Keystore & Certificate Verification

```mermaid
flowchart LR
    A["🔐 upload-keystore.jks\n(RSA 2048-bit / 10,000 Days)"] --> B["⚙️ key.properties\n(Alias: probill_upload_key)"]
    B --> C["📦 Gradle bundleRelease\n(build.gradle.kts)"]
    C --> D["🛡️ validateSigningRelease\n(Verified Certificate)"]
    D --> E["✅ app-release.aab\n(Ready for Google Play Console)"]
```

### 🔐 Keystore Parameter Reference:
- **Keystore File**: `android/app/upload-keystore.jks`
- **Key Alias**: `probill_upload_key`
- **Store & Key Password**: `probill2026pass`
- **Certificate Identity**: `CN=Jini Media Inc, OU=Mobile, O=Jini Media Inc, L=Surat, ST=Gujarat, C=IN`
- **Protection**: Secured via `.gitignore` (`key.properties`, `*.jks`, `*.keystore`)

---

## 📈 Monetization & Watermark Policy

```mermaid
stateDiagram-v2
    [*] --> FreeTier: App Launch
    
    state FreeTier {
        [*] --> StandardQuota: 10 Invoices / Month
        StandardQuota --> QuotaReached: 10th Invoice Created
        QuotaReached --> RewardedAdPrompt: User clicks "Create Invoice"
        RewardedAdPrompt --> BonusUnlocked: Watches AdMob Rewarded Video
        BonusUnlocked --> StandardQuota: +1 Bonus Invoice Granted
    }

    state ProTier {
        [*] --> UnlimitedMode: Auto-Renewing Sub / Lifetime
        UnlimitedMode --> ZeroAds: Complete Ad Suppression
        UnlimitedMode --> CustomBrand: Watermark Removed
        UnlimitedMode --> AutoBYOC: Scheduled Nightly Cloud Backup
    }

    FreeTier --> ProTier: Subscribes to Pro ($9.99/mo or $79.99/yr)
```

---

## 🚀 5-Step Google Play Console Upload Runbook

```mermaid
graph TD
    Step1["1️⃣ Open Google Play Console\n(Select 'ProBill: Estimates & Invoices')"] --> Step2["2️⃣ Navigate to Production / Closed Testing\n(Create New Release)"]
    Step2 --> Step3["3️⃣ Upload 'app-release.aab'\n(build/app/outputs/bundle/release/app-release.aab)"]
    Step3 --> Step4["4️⃣ Paste Store Listing Copy & Upload Graphics\n(App Icon, Feature Graphic, 5 Mockups)"]
    Step4 --> Step5["5️⃣ Submit for Review & Roll Out!\n(Internal testers get instant access)"]
```

---

<div align="center">
  <sub>Documented for <strong>Jini Media Inc.</strong> • ProBill Release Engineering</sub>
</div>
