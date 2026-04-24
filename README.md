# 🛒 Grocify

Grocify is a modern, smart grocery planning and list management application built with React Native and Expo. It helps you plan smarter and shop calmer by organizing your next grocery run with categories, quantities, priorities, and actionable insights.

---

## ✨ Features

- **Smart Grocery Planner:** Build your list with specific quantities, categories, and urgency levels.
- **Priority Management:** Easily identify high-priority items so you never forget the essentials.
- **Real-time Insights:** View statistics on your shopping habits, pending items, and total quantities.
- **Categorization:** Organize items by categories to make aisle navigation a breeze.
- **Secure Authentication:** Seamless and secure user login flow using Clerk.
- **Beautiful UI/UX:** A clean, modern interface styled with Tailwind CSS (NativeWind) and smooth animations.

---

## 🛠 Tech Stack

- **Framework:** React Native / [Expo](https://expo.dev/)
- **Navigation:** Expo Router
- **Styling:** Tailwind CSS ([NativeWind](https://www.nativewind.dev/))
- **State Management:** [Zustand](https://github.com/pmndrs/zustand)
- **Authentication:** [Clerk Expo](https://clerk.com/docs/quickstarts/expo)
- **Database:** [Neon Serverless](https://neon.tech/) & [Drizzle ORM](https://orm.drizzle.team/)
- **Icons:** Expo Vector Icons

---

## 🚀 Installation & Setup

### Prerequisites

Ensure you have the following installed on your machine:
- [Node.js](https://nodejs.org/) (LTS recommended)
- [Git](https://git-scm.com/)
- Expo Go app on your physical device (or an iOS/Android simulator)

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd grocify
```

### 2. Install dependencies

Using npm:

```bash
npm install
```

### 3. Environment Setup

Create a `.env` file in the root directory and add the following required environment variables:

```env
# Clerk Authentication Key
EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key

# Neon Database URL
DATABASE_URL=your_neon_database_url
```

*Note: You will need to set up a Clerk project and a Neon database to get these keys.*

### 4. Database Setup

To push your database schema to Neon via Drizzle ORM, run:

```bash
npm run db:push
```

To seed the initial grocery data, run:

```bash
npm run seed:grocery
```

---

## 📱 Running the App

Start the Expo development server:

```bash
npm start
```

Once the server is running, you can:
- **Run on Android:** Press `a` in the terminal or use `npm run android`
- **Run on iOS:** Press `i` in the terminal or use `npm run ios` (requires macOS with Xcode)
- **Run on Web:** Press `w` in the terminal or use `npm run web`
- **Run on Physical Device:** Scan the QR code using the Expo Go app (Android) or the native Camera app (iOS).

---

## 📂 Folder Structure

```
grocify/
├── app/                  # Expo Router file-based routing
│   ├── (tabs)/           # Main tab screens (Planner, Insights, etc.)
│   └── _layout.tsx       # Root layout and context providers
├── assets/               # Images, fonts, and other static assets
├── components/           # Reusable React components (UI, Forms, Lists)
├── store/                # Zustand state management files
├── api/                  # API routes and backend integration
├── scripts/              # Database seeding and utility scripts
├── tailwind.config.js    # Tailwind CSS configuration
├── package.json          # Project dependencies and scripts
└── README.md             # Project documentation
```

---

## 🛠 Common Commands

- `npm start` - Starts the Expo bundler
- `npm run android` - Starts the app on Android
- `npm run ios` - Starts the app on iOS
- `npm run lint` - Runs Expo linting to check for code issues
- `npm run db:push` - Pushes database schema changes
- `npm run reset-project` - Resets the Expo project cache

---

## 📸 Screenshots

*(Add screenshots of your application here)*

| Planner Screen | Insights Screen | List View |
|:--------------:|:---------------:|:---------:|
| ![Planner](placeholder-planner.png) | ![Insights](placeholder-insights.png) | ![List](placeholder-list.png) |

---

## 🐛 Troubleshooting

**1. Metro Bundler not starting or caching issues:**
Clear the cache by running:
```bash
npm start -- --clear
```

**2. Clerk Authentication not working:**
Ensure that your `EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY` in the `.env` file is correct and matches your Clerk dashboard.

**3. Database connection errors:**
Verify that your `DATABASE_URL` in the `.env` file is correctly formatted and your IP address is whitelisted in the Neon Database settings.

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).
