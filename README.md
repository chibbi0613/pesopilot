[README.md](https://github.com/user-attachments/files/25872692/README.md)
# ₱ PesoPilot — Philippine Peso Budget Tracker

> A full-featured Progressive Web App (PWA) for managing your personal finances in Philippine Peso (₱). Track income, expenses, loans, bills, credit cards, and your overall net worth — all stored locally on your device, no account required.

**Live App:** [chibbi0613.github.io/pesopilot](https://chibbi0613.github.io/pesopilot)

---

## 📱 Features Overview

### 🏠 Dashboard
- Monthly income vs. expense summary
- Net balance with savings rate percentage
- Spending breakdown donut chart by category
- Debt-to-Income (DTI) ratio ring chart with health rating
- Recent transaction activity feed

### 📋 Transactions (Entries)
- Add multiple income and expense entries per day
- **Granular expense categories** grouped by type:
  - Food & Dining (Groceries, Dining Out, Delivery, Coffee/Snacks)
  - Transport (Commute, Ride-hailing, Fuel, Toll, Vehicle Maintenance)
  - Utilities (Electricity, Water, Internet, Mobile, LPG, Cable/Streaming)
  - Housing (Rent, Condo Dues, Repairs, Appliances)
  - Health (Doctor, Pharmacy, Dental, Lab Tests)
  - Education (Tuition, Supplies, Online Courses)
  - Personal (Hygiene, Clothing, Salon/Spa)
  - Shopping (Online, Mall)
  - Lifestyle (Entertainment, Travel, Gaming)
  - Finance (Savings, Insurance)
  - Support (Family Remittance, Gifts, Charity)
  - Pets, Miscellaneous
- **Merchant/Biller field** with quick-tap suggestions per category
  - e.g. selecting Water Utility shows: Manila Water, Maynilad, MCWD, etc.
- **Linked payments** — loan, bill, and credit card payments are linked directly to their records and auto-update balances
- Filter by All / Income / Expense
- Grouped by date with tap-to-view detail and delete

### 🎯 Budget Tracker
- Set monthly spending limits per expense category
- Visual progress bars (green → yellow → red as you approach/exceed budget)
- Shows amount spent vs. budget per category

### 🏦 Loans
- Add loans with name, type, loan amount, total payable, and terms
- **Auto-calculates** interest rate from Loan Amount vs. Total Payable
- **Auto-calculates** monthly payment from Total Payable ÷ Terms
- Current balance tracking with paid-off percentage progress bar
- Estimated months remaining
- **Payment history** pulled directly from linked transactions
- Edit and delete individual loans

**Supported loan types:** Personal Loan, Car Loan, Home Loan / Mortgage, SSS Salary Loan, Pag-IBIG Loan, GSIS Loan, Business Loan, Student Loan, Gadget Loan

### 🧾 Monthly Bills (12-Month Tracker)
- Add recurring monthly bills with a biller name and category
- **Variable monthly amounts** — set a default, then enter the actual amount each month when marking paid
- 12-month calendar grid showing paid/unpaid status per month
- Tap any month to log the actual amount paid, date, and notes
- Year-to-date total paid per bill
- Edit and delete bills

**Bill categories:** Electricity, Water, Mobile/Phone, Internet, Rent/Association Dues, LPG/Gas, Cable/Streaming, Subscriptions, Tuition/School, Insurance

### 💳 Credit Cards
- **Bank presets** with real Philippine bank rates pre-loaded:

  | Bank | Monthly Rate | Min Payment |
  |------|-------------|-------------|
  | BDO | 3.54% | 2% |
  | BPI | 3.50% | 2% |
  | Metrobank | 3.63% | 2% |
  | PNB | 2.00% | 2% |
  | Security Bank | 3.54% | 2% |
  | RCBC | 3.50% | 2% |
  | EastWest Bank | 3.54% | 3% |
  | Citibank | 3.50% | 2% |
  | HSBC | 3.50% | 2% |
  | UnionBank | 3.50% | 2% |
  | Maya Card | 3.50% | 2% |
  | GCash CC | 3.50% | 2% |

- Credit utilization bar with color warnings (green < 50%, yellow < 80%, red > 80%)
- **Payoff forecasts** showing exact monthly payment needed to pay off in:
  - 6 months
  - 12 months
  - 24 months
  - Minimum payment only (with total interest cost warning)
- **Payment history** from linked transactions
- Edit and delete cards

### 📊 Reports & Insights
- 6-month income vs. expenses bar chart
- Auto-generated financial insights:
  - Savings rate analysis
  - Top spending category alert
  - Credit card utilization warnings
  - Total loan balance summary
- Full expense breakdown with percentage of income

### 💰 Net Worth Summary
- Total Assets minus Total Liabilities
- Add assets by type: Cash/Savings, Investments/Stocks/UITF, Real Estate, Vehicle, Business Value, Receivables
- Liabilities auto-populated from loan balances and credit card balances
- Edit and delete assets

---

## 🔗 Linked Payments (Key Feature)

When adding an expense transaction and selecting a **Loan Payment**, **Bill Payment**, or **Credit Card Payment**, the app shows your actual saved records as chip options. Selecting one:

1. **Pre-fills the amount** with the scheduled payment / minimum due / default bill amount
2. **Saves the transaction** in your Entries log with a `linked` badge
3. **Automatically updates** the linked record:
   - Loan balance is reduced
   - Card balance is reduced
   - Bill month is marked as paid

This means you only enter payments once — they appear in your transaction history AND update your loan/bill/card records simultaneously.

---

## 🚀 Deployment Guide

### Option 1: GitHub Pages (Recommended — Free, No Limits)

1. Create a free account at [github.com](https://github.com)
2. Click **New** → Repository name: `pesopilot` → Set to **Public** → Check **Add a README** → Create
3. Click **Add file** → **Upload files** → drag `index.html`, `manifest.json`, `sw.js`
4. Click **Commit changes**
5. Go to **Settings** → **Pages** → Branch: `main` / `/ (root)` → **Save**
6. Wait 1–2 minutes → your app is live at `https://yourusername.github.io/pesopilot`

**Installing on Android:**
1. Open Chrome on your Android phone
2. Visit your GitHub Pages URL
3. Tap the ⋮ menu → **Add to Home screen** → **Add**
4. PesoPilot icon appears on your home screen and works offline ✓

### Option 2: Vercel (Free)
1. Go to [vercel.com](https://vercel.com) → Sign up free
2. Drag and drop your project folder onto the dashboard
3. Get an instant URL like `https://pesopilot.vercel.app`

### Option 3: Cloudflare Pages (Free, Fast)
1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Connect GitHub repo or upload files directly
3. Deploy — runs on Cloudflare's global edge network

### Option 4: Tiiny.host (Quickest, No Account Needed)
1. Go to [tiiny.host](https://tiiny.host)
2. Drag your folder → get an instant URL in 30 seconds

---

## 💾 Data Storage

All data is stored **locally on your device** using the browser's localStorage. No data is sent to any server. No account is required.

| Data | Storage Key |
|------|------------|
| Transactions | `tx2` |
| Loans | `loans2` |
| Bills | `bills2` |
| Credit Cards | `cards2` |
| Budgets | `budgets2` |
| Assets | `assets2` |
| Settings | `settings2` |

**Backup your data regularly** via Settings → Export Data (JSON). This downloads a full JSON backup of all your records.

---

## 📂 File Structure

```
pesopilot/
├── index.html      ← Main app (all-in-one, self-contained)
├── manifest.json   ← PWA manifest (makes it installable on Android)
├── sw.js           ← Service worker (enables offline use)
└── README.md       ← This file
```

---

## 🛠 Updating the App

To push updates to your live GitHub Pages site:

1. Go to `github.com/yourusername/pesopilot`
2. Click `index.html`
3. Click the ✏️ pencil (Edit) icon
4. Replace the content with the new version
5. Click **Commit changes**
6. Wait ~1 minute for the live site to update

---

## 📌 Income Categories

| Category | Description |
|----------|-------------|
| 💼 Salary / Wages | Regular employment income |
| 💻 Freelance / Contract | Project-based or gig work |
| 🎁 Bonus / 13th Month | Performance bonuses, 13th month pay |
| 🏪 Business Income | Business revenue |
| 🏠 Rental Income | Property rental |
| 🏦 Interest / Dividends | Bank interest, stock dividends |
| 📈 Investment Returns | Capital gains, fund returns |
| 📨 Remittance / Padala | Money sent from abroad |
| 🎓 Allowance / Stipend | School or family allowance |
| 👴 Pension / SSS / GSIS | Government pension |

---

## 📌 Expense Categories (Grouped)

| Group | Categories |
|-------|-----------|
| Food & Dining | Groceries, Dining Out, Food Delivery, Coffee/Snacks |
| Transport | Commute/MRT/Jeep, Ride-hailing, Fuel, Toll/Parking, Vehicle Maintenance |
| Utilities | Electricity, Water, Internet, Mobile, LPG/Gas, Cable/Streaming |
| Housing | Rent, Condo/HOA Dues, Home Repair, Appliances/Furniture |
| Health | Doctor/Hospital, Medicine, Dental, Check-up/Lab Tests |
| Education | Tuition, School Supplies, Online Courses |
| Personal | Personal Care/Hygiene, Clothing/Shoes, Haircut/Salon/Spa |
| Shopping | Online Shopping, Mall Shopping |
| Lifestyle | Entertainment/Events, Travel/Vacation, Gaming |
| Finance | Savings/Investment, Insurance Premium |
| Support | Family Support/Padala, Gifts/Celebrations, Charity/Donations |
| Other | Pets, Miscellaneous |

---

## 📊 DTI Ratio Guide

| DTI Range | Status | Meaning |
|-----------|--------|---------|
| Below 20% | ✅ Excellent | Very healthy debt level |
| 20% – 36% | 🟦 Good | Manageable debt |
| 36% – 43% | ⚠️ Caution | Getting risky — reduce debt |
| Above 43% | 🔴 High Risk | Difficult to get new credit; prioritize debt payoff |

*DTI = Monthly Debt Obligations ÷ Monthly Gross Income × 100*

---

## 🔧 Technical Details

- **Type:** Progressive Web App (PWA) — installable, works offline
- **Framework:** Vanilla HTML/CSS/JavaScript (no build tools required)
- **Charts:** Chart.js 4.4.0 (loaded from CDN)
- **Fonts:** Syne + DM Sans (Google Fonts)
- **Storage:** Browser localStorage (client-side only)
- **Currency:** Philippine Peso (₱ / PHP)
- **Offline:** Full offline support via Service Worker caching

---

## 🔒 Privacy

- ✅ No account required
- ✅ No data sent to any server
- ✅ All data stays on your device
- ✅ No ads, no tracking
- ✅ Export your data anytime as JSON

---

*PesoPilot v3.0 — Built for Filipino personal finance management*
