# 💇‍♀️ Hair Style Database App – React Native + Expo Cheat Sheet

## 🛠️ 1. Project Initialization
```bash
npm install -g expo-cli
expo init hairstyle-app
cd hairstyle-app
expo start
```

## 📦 2. Folder Structure Setup
```bash
mkdir -p assets components screens services utils contexts hooks types
```
Suggested structure:
```
/assets        → Images, icons
/components    → Reusable UI (Card, VideoPlayer)
/screens       → Home, Profile, Upload, Detail
/services      → API calls (axios)
/utils         → Constants, helpers
/contexts      → Auth, theme context
/hooks         → Custom hooks
/types         → TypeScript types
```

## 🧠 3. Install Core Dependencies
```bash
npm install @react-navigation/native @react-navigation/native-stack @react-navigation/bottom-tabs
npm install react-native-paper react-native-gesture-handler react-native-reanimated react-native-safe-area-context react-native-screens
npm install react-hook-form yup axios react-native-vector-icons zustand
npm install expo-image-picker expo-camera expo-av
```

## 👥 4. User Authentication
- Backend: Implement Node.js + Express auth routes (register/login)
- Use JWT & bcrypt
```bash
npm install jsonwebtoken bcryptjs
```
Frontend:
- Store token in SecureStore or AsyncStorage
```bash
expo install expo-secure-store
```

## 🎥 5. Upload Component
- Use expo-image-picker or camera:
```bash
expo install expo-image-picker expo-camera expo-av
```
- Allow user to select or record video
- Upload to Firebase or S3

## 🖼 6. Hair Style Gallery (Grid View)
- Use FlatList to show:
  - Thumbnail
  - Name + short desc
  - Tag badges
  - Vote count

## 🔍 7. Filters & Search
- Add TextInput for search
- Filter by:
  - Length (short, med, long)
  - Texture (curly, straight...)
  - Occasion (casual, party)
- Backend: Add query params to filter API

## 📄 8. Hairstyle Detail Screen
- Display full video/image
- List related videos
- Voting button
- Comment section
- Step-by-step guide (text/tutorial)

## 📊 9. Voting System
- Button to upvote videos
- POST vote to backend with userId & videoId
- Prevent duplicate votes
- Use vote counts to generate trending list

## 💬 10. Community Features
- Comment form and list
- Profile screen:
  - User uploads
  - Follow button
- Follow model in DB (followers/following)

## 🚀 11. Trending & Recommendations
- Backend cron job:
  - Calculate top videos (last 24h)
- Home screen shows:
  - Trending styles
  - Personalized recommendations (by tags)

## 🔗 12. Sharing & Social
- Use expo-sharing:
```bash
expo install expo-sharing
```
- Add native share option for each style/video

## 💰 13. Monetization
- Add AdMob:
```bash
expo install expo-ads-admob
```
- Promote stylists with premium tags or sorting
- Booking link/button for stylist profile

## 🧪 14. Testing & QA
```bash
npm install --save-dev jest @testing-library/react-native
```

## 🧱 15. Deployment
- Mobile builds:
```bash
npx expo install eas-cli
npx eas build:configure
npx eas build -p android
npx eas build -p ios
```
- Backend deployment: Render / Railway / Vercel
- DB: PlanetScale (MySQL) or Supabase
- Media: Cloudinary / S3 / Firebase Storage