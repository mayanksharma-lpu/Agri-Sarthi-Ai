# AgriSarthi AI - Smart Farming Assistant 🌾

A comprehensive agricultural AI web application built with React, TypeScript, and Tailwind CSS. AgriSarthi AI helps farmers make data-driven decisions using artificial intelligence and machine learning algorithms.

## 🚀 Features

### 1. **AI Crop Disease Detection**
- Upload crop images for instant disease identification
- AI-powered analysis using image processing (simulates MobileNetV2)
- Get disease name, confidence score, symptoms, solutions, and prevention tips
- Supports multiple crops: Tomato, Potato, Wheat, Rice, Corn
- Voice assistant to listen to results

### 2. **Continuous Crop Monitoring**
- Track crop health over time
- Compare current vs. previous disease detection results
- Health score trending with charts
- Improvement/decline analysis
- Automated recommendations based on trends

### 3. **Crop Recommendation System**
- AI-based crop suggestions (simulates Random Forest algorithm)
- Input soil nutrients (N, P, K), pH, temperature, humidity, rainfall
- Get best crop recommendations with confidence scores
- Alternative crop suggestions
- Supports 10+ crops including rice, wheat, cotton, maize, etc.

### 4. **Soil Intelligence**
- Comprehensive soil fertility analysis
- Calculate overall soil health score and grade
- Nutrient-level breakdown (NPK, pH, organic matter, moisture)
- Personalized soil improvement recommendations
- Natural fertilizer suggestions (organic options)
- Detailed application guidelines

### 5. **Smart Irrigation System**
- Calculate optimal irrigation needs based on:
  - Soil moisture levels
  - Crop type and growth stage
  - Weather conditions (temperature, humidity, rainfall)
  - Soil type
- Get irrigation urgency (Low/Medium/High)
- Recommended water amount in mm
- Crop-specific irrigation schedules
- Best timing recommendations

### 6. **Crop Risk Prediction**
- AI-powered risk assessment (simulates Logistic Regression)
- Analyze multiple risk factors:
  - Soil health
  - Weather risk
  - Pest incidence
  - Irrigation quality
  - Crop age
- Get Low/Medium/High risk classification
- Detailed risk factor breakdown
- Actionable recommendations

### 7. **Weather Alerts & Forecast**
- Real-time weather monitoring
- 7-day weather forecast
- Intelligent weather alerts:
  - Temperature warnings (heat/frost)
  - Rainfall predictions
  - High humidity alerts
  - Wind warnings
- Crop-specific weather advice
- Weather-based farming tips

### 8. **Yield & Profit Estimation**
- AI-based yield prediction (simulates Linear Regression)
- Calculate expected yield in quintals
- Revenue and profit estimation
- Cost analysis
- Market price integration
- Financial summary and recommendations

### 9. **Market Price Intelligence**
- Live market prices for 10+ crops
- 6-month price trend analysis
- Price change indicators (up/down/stable)
- Market demand status
- MSP (Minimum Support Price) information
- Future price predictions (3-month forecast)
- Smart selling recommendations
- Nearby market/mandi information

### 10. **Government Schemes Eligibility**
- Check eligibility for 10+ government agricultural schemes
- Includes:
  - PM-KISAN (income support)
  - Pradhan Mantri Fasal Bima Yojana (crop insurance)
  - Kisan Credit Card
  - Soil Health Card Scheme
  - Micro-irrigation subsidies
  - Organic farming support
  - Pension schemes
  - And more...
- Personalized eligibility checking
- Detailed benefits, documents, and application process
- Reason for eligibility/ineligibility

### 11. **Farmer Community**
- Create and share posts
- Upload images
- Like posts
- Comment on posts
- Real-time community feed
- All data stored locally

### 12. **Voice Assistant**
- Text-to-speech for all major outputs
- Listen button on key information
- Uses Web Speech API (offline capable)
- Supports multiple languages

## 🛠️ Technology Stack

- **Frontend:** React 18, TypeScript
- **Styling:** Tailwind CSS v4
- **Routing:** React Router v7 (Data Mode)
- **Charts:** Recharts
- **UI Components:** Radix UI (Shadcn)
- **Icons:** Lucide React
- **Voice:** Web Speech API
- **Storage:** LocalStorage (offline data persistence)
- **Build Tool:** Vite

## 📦 Installation & Setup

### Prerequisites
- Node.js 18+ and npm/pnpm

### Steps

1. **Clone or download the project**

2. **Install dependencies**
   ```bash
   npm install
   # or
   pnpm install
   ```

3. **Run the development server**
   ```bash
   npm run dev
   # or
   pnpm dev
   ```

4. **Open in browser**
   ```
   http://localhost:5173
   ```

## 🎯 How to Use

### For Crop Disease Detection:
1. Navigate to "Crop Disease" from sidebar
2. Select crop type (Tomato, Potato, Wheat, Rice, Corn)
3. Upload a clear image of affected crop/leaves
4. Click "Analyze Disease"
5. Get AI-powered disease detection with solutions
6. Click "Listen" button to hear the results

### For Crop Recommendation:
1. Go to "Recommendations" page
2. Enter soil nutrients (N, P, K)
3. Set soil pH level
4. Input weather conditions (temperature, humidity, rainfall)
5. Click "Get Recommendation"
6. Receive best crop suggestions with alternatives

### For Soil Analysis:
1. Visit "Soil Intelligence" page
2. Enter soil test results (N, P, K, pH, organic matter, moisture)
3. Click "Analyze Soil Health"
4. View fertility score and grade
5. Get improvement recommendations and natural fertilizer suggestions

### For Irrigation Planning:
1. Open "Irrigation" page
2. Select crop type and growth stage
3. Enter soil moisture level
4. Input current weather conditions
5. Click "Calculate Irrigation"
6. Get water amount and timing recommendations

### For Government Schemes:
1. Navigate to "Govt. Schemes"
2. Enter your land size
3. Set land ownership status
4. Input age
5. Select farming practices
6. Click "Check Eligibility"
7. View all eligible and ineligible schemes with reasons

### For Community:
1. Go to "Community" page
2. Write post title and content
3. Optionally upload an image
4. Click "Post" to share
5. Like and comment on others' posts

## 🧠 AI Models (Simulation)

All AI models use deterministic algorithms that simulate real machine learning models:

1. **Crop Disease Detection:** Image color analysis simulating MobileNetV2 + PlantVillage dataset
2. **Crop Recommendation:** Decision tree logic simulating Random Forest
3. **Risk Prediction:** Multi-factor scoring simulating Logistic Regression
4. **Yield Estimation:** Formula-based calculation simulating Linear Regression

## 💾 Data Storage

- All data stored in browser's LocalStorage
- Works 100% offline after first load
- No backend or database required
- Data persists between sessions
- Can be cleared from browser settings

## 📱 Responsive Design

- Fully responsive across desktop, tablet, and mobile
- Mobile-friendly sidebar navigation
- Touch-optimized UI components
- Adaptive layouts for all screen sizes

## 🎨 UI/UX Features

- Modern gradient designs
- Smooth animations and transitions
- Color-coded alerts and badges
- Interactive charts and graphs
- Progress bars for visual feedback
- Card-based layout for better organization
- Intuitive navigation
- Professional dashboard design

## 🔊 Voice Features

- Uses browser's Web Speech API
- Works offline (after first load)
- Multiple voice options (based on browser/OS)
- Supports English and regional languages
- Click "Listen" button on any result

## 📊 Charts & Visualizations

- Line charts for health trends
- Price trend graphs
- Progress bars for scores
- Color-coded badges for statuses
- Interactive tooltips

## 🌐 Offline Capability

The app works offline by:
- Storing all logic client-side
- Using LocalStorage for data persistence
- No external API dependencies for core features
- Service Worker compatible (can be added)

## 🔐 Privacy & Security

- No data sent to external servers
- All processing happens in browser
- No user accounts or authentication required
- Data stored only on user's device
- No tracking or analytics

## 🚀 Performance

- Fast load times with Vite
- Lazy loading components
- Optimized images
- Minimal bundle size
- Efficient re-renders with React

## 🤝 Contributing

This is a demonstration project. For production use:
- Replace simulated AI with real ML models
- Add backend API integration
- Implement user authentication
- Add real-time data sources
- Deploy to cloud platform

## 📄 License

This project is open source and available for educational purposes.

## 🙏 Credits

- UI Components: Shadcn UI
- Icons: Lucide React
- Charts: Recharts
- Styling: Tailwind CSS

## 📞 Support

For issues or questions, please refer to the inline documentation and tooltips within the application.

---

**Built with ❤️ for farmers using AI technology**

🌾 AgriSarthi AI - Empowering Agriculture with Intelligence
