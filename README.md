# 🤖 WhatsApp Financial Tracker Bot

A privacy-focused WhatsApp bot that uses OCR technology to extract financial data from receipts and transaction images, automatically categorizes them, and provides real-time balance tracking.

## 🌟 Overview

This WhatsApp Finance Bot leverages OCR (Optical Character Recognition) to automatically process receipt images and transaction screenshots, provides seamless financial tracking through WhatsApp.

### 🎯 Main Purpose

- **Automated Receipt Processing**: Scan and extract financial data from images
- **Multi-language Support**: Process receipts in Indonesian and English
- **Privacy-First Design**: All processing happens in-memory with optional exports
- **Comprehensive Reporting**: Generate detailed Excel reports with financial insights

## ✨ Key Features

### 🧾 OCR Processing
- **Multi-Strategy OCR**: High-quality, fast, and receipt-optimized processing modes
- **Indonesian Receipt Support**: Specialized parsing for ShopeePay, DANA, Indomaret, Alfamart, and more
- **Bank Transaction Processing**: Extract data from mobile banking screenshots

### 💰 Financial Management
- **Category Classification**: Automatic income/expense categorization
- **Transaction History**: Comprehensive history with date filtering
- **Date Filters**: Today, week, month, custom day ranges

### 🤖 Bot Experience
- **User Onboarding**: Guided setup for new users with balance initialization
- **Smart Conversation Flow**: Context-aware responses and session management
- **Command System**: Full command suite (`/balance`, `/history`, `/export`, etc.)
- **Category Selection**: 14 predefined categories for accurate classification

### 📊 Reporting & Export
- **Excel Reports**: Professional multi-sheet reports with formatting
- **Google Sheets Integration**: Optional real-time logging to Google Sheets
- **Privacy-Safe Exports**: Masked user IDs in all external reports

### 🔒 Privacy & Security
- **In-Memory Storage**: Primary storage for real-time performance
- **User ID Masking**: Automatic privacy protection (format: `1234****5678`)
- **Session Management**: Automatic cleanup and timeout handling
- **No Persistent Image Storage**: Images processed in memory only

## 🛠️ Technologies Used

- **TypeScript** - Type-safe JavaScript with OOP features
- **Node.js** - Runtime environment
- **WhatsApp Web.js** - WhatsApp Web API integration
- **Tesseract.js** - OCR engine for text extraction
- **ExcelJS** - Excel workbook generation
- **Google Sheets API** - Optional cloud-based data logging

## 🚀 Installation

### Prerequisites
- **Node.js** 18.0.0 or higher
- **WhatsApp account** for bot connection
- **Google Service Account** (optional, for Google Sheets)

### Setup Steps

1. **Clone and Install**
```bash
git clone https://github.com/friskaam/finance-tracker-bot.git
cd finance-tracker-bot
npm install
```

2. **Environment Configuration**
Create `.env` file:
```env
# Bot Configuration
SESSION_TIMEOUT=3600000
MAX_IMAGE_SIZE=10485760
USE_EXCEL=true
USE_GOOGLE_SHEETS=false

# OCR Configuration
OCR_LANGUAGES=eng+ind
OCR_MIN_CONFIDENCE=60

# Google Sheets (Optional)
GOOGLE_SPREADSHEET_ID=your_spreadsheet_id
GOOGLE_SERVICE_ACCOUNT_KEY_FILE=./service-account-key.json
```

3. **Start the Bot**
```bash
# Development
npm run dev

# Production
npm run build
npm start
```

4. **Connect WhatsApp**
- Scan QR code with WhatsApp
- Send `/start` to begin

## 📊 Usage

### Basic Commands
```bash
/start      # Start or setup balance
/balance    # Check current balance
/history    # View transactions
/history 7  # Last 7 days
/export     # Generate Excel report
/help       # Show all commands
/end        # Save and exit
```

### Workflow
1. **Setup**: Send `/start` and enter initial balance
2. **Process**: Send receipt image → Select payment method → Choose category
3. **Track**: Use `/balance` and `/history` to monitor finances
4. **Export**: Use `/export` for detailed reports

## 🧪 Testing

### Basic Tests
```bash
# Type checking
npx tsc --noEmit

# Development testing
npm run dev
# Send "hi" or "/start" to test connection
# Send receipt image to test OCR
```

### Supported Receipt Types
- Indonesian E-wallets: ShopeePay, DANA, GoPay, OVO
- Retail Stores: Indomaret, Alfamart, Carrefour
- Bank Transfers: Mobile banking screenshots

## 📁 Project Structure

```
whatsapp-finance-bot/
├── bot/                    # Main bot controller
├── services/               # Business logic services
├── utils/                  # Utility classes
├── types/                  # TypeScript definitions
├── exports/                # Generated reports
└── index.ts               # Entry point
```

## 🤝 Contributing

1. Fork the repository
2. Create feature branch: `git checkout -b feature/name`
3. Commit changes: `git commit -m 'Add feature'`
4. Push to branch: `git push origin feature/name`
5. Open Pull Request

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

---

*Built with ❤️ for privacy-conscious financial tracking*

**Made by Friska Mahardini**
