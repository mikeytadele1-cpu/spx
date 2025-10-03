# SpendX Card - Crypto Card & Wallet Platform

## Overview
SpendX Card is a crypto card and wallet platform enabling users to spend cryptocurrency anywhere. It features a professional dark theme with gold accents, real-time crypto market data, and a comprehensive deposit system supporting multiple cryptocurrencies and networks. The project's vision is to provide a seamless and secure way for users to integrate cryptocurrency into their daily spending habits, leveraging a sophisticated yet user-friendly interface.

## User Preferences
Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript, using Vite for development and optimized builds.
- **Routing**: Wouter for lightweight client-side routing.
- **State Management**: React Context API for authentication, and TanStack Query for server state and data fetching.
- **Styling**: Tailwind CSS with a custom design system, utilizing Radix UI primitives and shadcn/ui components.
- **UI/UX Decisions**:
    - **Theme**: Professional dark theme with FTX-inspired accents (dark navy/charcoal primary, teal, gold, and orange accents).
    - **Color Scheme**: Primary Teal: #00BCD4, Secondary Cyan: #33D6E0, News Orange: #FF9900, Gold: #F4C430, Primary Dark: #0B0E11, Secondary Dark: #1E2126.
    - **Button Styling**: Custom CSS classes for professional, animated FTX-themed buttons (`.btn-ftx-primary`, `.btn-ftx-secondary`, `.btn-ftx-outline`).
    - **Typography**: Modern font stack with proper hierarchy.
    - **Responsive Design**: Mobile-first approach with Tailwind breakpoints.
    - **Animations**: Subtle CSS animations for enhanced user experience (e.g., slideIn, fadeIn, scaleIn, floating effects, hover effects, glow animations).
    - **Key Features**: Embedded sign-up/sign-in experience within the referral section, professional password feedback system, comprehensive FAQ, real-time FOMO countdown timers, and integrated video content on the Dashboard.

### Backend Architecture
- **Framework**: Express.js with TypeScript on Node.js (ES modules).
- **Database**: PostgreSQL with Drizzle ORM, hosted on Neon serverless PostgreSQL.
- **Authentication**: Firebase Authentication (Google OAuth, Apple Sign-in), with a streamlined direct account creation process.
- **Session Management**: In-memory storage with an extensible interface.

### Technical Implementations & Features
- **Authentication System**: Firebase-powered, supporting Google and Apple sign-in. Features direct account creation, robust password requirements with interactive feedback, and secure password reset. Each user receives a unique, persistent 12-word seed phrase.
- **Crypto Data Integration**: Utilizes Coinbase Pro API for institutional-grade swap rates primarily, with CoinGecko API as a robust fallback for real-time market data, trending coins, and market statistics. Includes a real-time data source indicator.
- **Deposit System**: Supports multiple cryptocurrencies and networks (Bitcoin, Ethereum, Solana, BNB, USDT, USDC). Features static addresses for demo purposes, QR code generation, and copy-to-clipboard functionality.
- **Card Ordering & Payment**: Offers digital and physical card options with a streamlined manual crypto payment system (Bitcoin-focused). Includes network recommendation for card activation, final confirmation checklists, and urgent pricing alerts.
- **Referral System**: Completely rebuilt with unique, database-integrated referral codes for each user. Rewards are only paid after admin verification of card payment and card activation, ensuring genuine referrals. Each referral earns $30 for virtual cards and $45 for physical cards.
- **Withdrawal System**: Comprehensive withdrawal system supporting USDT and USDC with multiple networks (TRC20, ERC20, BSC) plus traditional cryptocurrencies (BTC, ETH, BNB, SOL). Features admin approval workflow with detailed currency/network tracking, customizable minimum withdrawal amounts per currency, and complete transaction history.
- **Admin Panel**: Full-featured admin dashboard for managing card orders, withdrawal requests, and user verification. Includes transaction hash verification, order status management, and referral reward processing upon card activation.
- **Swap System**: Comprehensive swap functionality with accurate real-world pricing calculations and enhanced success notifications.
- **Security Features**: Implementation of multi-layered security notices, secure seed phrase management, and strong password validation.
- **Test Account System**: Comprehensive test environment with 11 special accounts (ethiocapitalx@gmail.com + Test001-010@gmail.com) featuring custom balances, activated cards, and referral earnings for demonstration and testing purposes.

### Recent Changes (August 2025)
- **TEST USER SYSTEM (August 19, 2025)**: Created 10 test accounts with activated cards and custom balances ranging from $420 to $3000. All test users have referral earnings and activated virtual cards to demonstrate full platform functionality. Special balance handling for ethiocapitalx@gmail.com ($1742) and Test001-010@gmail.com accounts.
- **CRITICAL SECURITY FIXES (August 19, 2025)**: Fixed major security vulnerability where any user could view any order without authentication. Implemented mandatory authentication for all order status checks, added user ownership verification for orders, and secured all order-related endpoints with proper firebaseUid validation.
- **Enhanced Real-time Balance System**: Fixed balance display issues for all special accounts (ethiocapitalx@gmail.com + Test001-010@gmail.com), implemented real-time balance updates every 5 seconds, added manual refresh functionality with loading indicators, and fixed TanStack Query compatibility issues (cacheTime → gcTime). Resolved API response mapping issue where calculated referral data was overriding correct database values.
- **Protected Order System**: All order pages now require authentication, order status checking validates user ownership, URL-based order access requires verification tokens, and proper error handling for unauthorized access attempts.
- **Enhanced Withdrawal System**: Added USDT and USDC support with TRC20, ERC20, and BSC networks. Updated database schema to include currency field, implemented network-specific minimum withdrawal amounts, and enhanced admin interface for better withdrawal management.
- **Comprehensive Referral System Implementation**: Built complete referral system where rewards are only paid after card activation. Users receive unique referral codes after registration, referral records track pending/paid status, and admin verification automatically processes referral rewards ($30 for virtual cards, $45 for physical cards).
- **Streamlined Admin Verification Process**: Completely restructured the admin workflow so that payment verification automatically activates cards and processes referral rewards in a single action. Removed separate card activation step for improved efficiency.
- **Withdrawal System Consolidation**: Removed standalone withdrawal page and integrated all withdrawal functionality into the dashboard. Set uniform $100 minimum withdrawal amount for all cryptocurrencies. Withdrawal is now accessible only through the dashboard for better user experience.
- **Referral System Security & Balance Updates**: Implemented card activation verification before showing referral codes/links. No demo referral codes are provided - users must activate their SpendX Card first to unlock their paid referral system. Auto-fill functionality for referral codes in signup page works via URL parameters. Proper balance tracking for paid referrals with correct "Paid Balance" and "Total Paid" statistics display.
- **Database Schema Updates**: Added referral tracking fields (cardType, orderId, paidAt) to referrals table, updated related interfaces and API endpoints to support referral reward processing with proper activation verification.

## External Dependencies

### Third-Party APIs
- **CoinGecko API**: Real-time cryptocurrency market data, prices, and statistics.
- **Coinbase Pro API**: Institutional-grade swap rates and price data.
- **Firebase**: Authentication services, user management, and password reset.

### UI Libraries
- **Radix UI**: Accessible component primitives for building UI.
- **shadcn/ui**: Pre-built, customizable UI components.
- **Tailwind CSS**: Utility-first CSS framework for styling.
- **Lucide React**: Icon library.

### Development Tools
- **Vite**: Frontend build tool and development server.
- **TypeScript**: For type safety and enhanced developer experience.
- **ESLint**: Code linting.
- **PostCSS**: CSS processing.
- **Drizzle ORM**: For database interactions with PostgreSQL.
- **Neon**: Serverless PostgreSQL database hosting.