# AgriFuture 🌱

A blockchain-based platform for sustainable agriculture, built for the Hedera Hackathon.

## Overview

AgriFuture is a decentralized application (dApp) designed to revolutionize the agricultural supply chain by empowering farmers with blockchain technology. Built for the Hedera Hackathon, AgriFuture leverages Hedera’s blockchain to provide transparency, immutability, and security for tracking and tokenizing agricultural produce. The platform also plans to integrate Chainlink for real-time market data, ensuring fair pricing for farmers. AgriFuture promotes sustainable farming practices, reduces waste, and fosters a global marketplace for eco-friendly produce.

Key highlights:
- **Transparency**: Uses Hedera’s Consensus Service to record produce data immutably.
- **Tokenization**: Enables farmers to tokenize crops as digital assets on Hedera’s Token Service.
- **Sustainability**: Encourages eco-friendly farming with features like sustainability scoring and carbon offset tracking.
- **Accessibility**: Supports multiple languages (English/Spanish) for global reach.

**Live Demo**: [https://NyamumboC.github.io/AgriFuture/](https://NyamumboC.github.io/AgriFuture/)  
**Demo Video**: [Watch the Demo](https://youtu.be/your-video-id)  
**Repository**: [https://github.com/NyamumboC/AgriFuture](https://github.com/NyamumboC/AgriFuture)

---

## Vision

AgriFuture envisions a transparent, sustainable agricultural ecosystem using Hedera and Chainlink. We empower farmers to track, tokenize, and trade produce on Hedera, while Chainlink provides real-time market data for fair pricing. Our goal is to create a global, eco-friendly marketplace that connects farmers, buyers, and communities, driving a greener future for agriculture worldwide.

---

## Features

AgriFuture offers a range of features to support farmers in managing and trading their produce:

- **Landing Page**:
  - A clean, welcoming interface with a "Get Started" button to guide users into the platform.
  - Includes a language toggle (English/Spanish) for accessibility.
- **Auth Modal**:
  - A login form for farmers to access the platform.
  - Built with `react-hook-form` for efficient form handling and validation.
  - Features smooth animations using `framer-motion` for a better user experience.
- **Dashboard**:
  - Displays produce tracking data with visualizations powered by `chart.js`.
  - Shows metrics like quantity, status, and trends over time, helping farmers make informed decisions.
- **Tokenize Crop**:
  - Allows farmers to tokenize their produce on the Hedera network.
  - Captures details such as:
    - Product name (e.g., "Wheat")
    - Quantity (e.g., "100 kg")
    - Location (e.g., "Farm A")
    - Date (e.g., "04/02/2025")
    - Sustainability score (e.g., "80/100")
    - Insurance status (e.g., "Insured")
  - Integrates with Hedera’s Token Service to create digital assets.
- **Navigation Menu**:
  - Provides access to additional features (some planned for future implementation):
    - **Marketplace**: For buying and selling tokenized crops.
    - **P2P Trading**: For direct peer-to-peer trading.
    - **Logistics**: For tracking shipments.
    - **Insurance**: For managing crop insurance.
    - **AI Insights**: For data-driven farming recommendations.
    - **Soil Analysis**: For soil health insights.
    - **Token Staking**: For staking tokenized assets.
    - **Community Chat**: For farmer collaboration.
    - **Carbon Offset**: For tracking sustainability efforts.
    - **Analytics**: For advanced data insights.
    - **Settings**: For user preferences.
- **Notifications**:
  - Uses `react-toastify` to display success/error messages (e.g., "Token created with ID: 0.0.123456").
- **Responsive Design**:
  - Styled with `tailwindcss` for a modern, mobile-friendly UI.
- **Animations**:
  - Smooth transitions and effects (e.g., modal open/close) using `framer-motion`.

---

## Demo

A live demo of AgriFuture is available at [https://NyamumboC.github.io/AgriFuture/](https://NyamumboC.github.io/AgriFuture/). You can also watch a short demo video showcasing the platform’s features and Hedera integration:


## Build Process

AgriFuture was developed as a React-based web application with a focus on blockchain integration and user experience. Below is a detailed breakdown of the build process.


### Frontend Development
- **Landing Page**:
  - Designed a simple landing page with a "Get Started" button and language toggle.
  - Used Tailwind CSS for a clean, responsive layout.
- **Auth Modal**:
  - Built a modal for user login with `react-hook-form` to handle form inputs (username, password).
  - Added animations with `framer-motion` for smooth transitions.
- **Dashboard**:
  - Created a dashboard to display produce data using `chart.js` for bar charts and line graphs.
  - Styled with Tailwind CSS for a modern look.
- **Tokenize Crop**:
  - Developed a form to tokenize crops, capturing details like product name, quantity, and sustainability score.
  - Integrated with Hedera to create tokens on the blockchain.
- **Navigation Menu**:
  - Added a sidebar with links to various features (e.g., Marketplace, P2P Trading).
  - Used Tailwind CSS for styling and `framer-motion` for hover effects.

### Hedera Integration
- **Setup**:
  - Installed the Hedera SDK (`@hashgraph/sdk`) to interact with the Hedera testnet.
  - Configured a Hedera client in `App.js` using testnet credentials.
- **Consensus Service**:
  - Implemented a `handleCreateTopic` function to create topics for recording produce data.
  - Used `TopicCreateTransaction` to create a topic on the testnet, logging the topic ID to the console.
- **Token Service**:
  - Implemented a `handleTokenizeCrop` function to tokenize crops.
  - Used `TokenCreateTransaction` to create a token for each crop, logging the token ID to the console.
- **Security**:
  - Stored Hedera credentials in a `.env` file to prevent hardcoding sensitive information.

### Chainlink Integration
- **Planned Integration**:
  - Planned to use Chainlink Price Feeds to fetch real-time market data for crops (e.g., price of wheat).
  - Due to time constraints, mocked the functionality with a `fetchMarketPrice` function in `App.js`.
- **Future Implementation**:
  - Will integrate Chainlink’s decentralized oracles to provide accurate market data for fair pricing in the marketplace.


### Challenges Faced
- **Hedera Setup**:
  - Initially struggled to set up a Hedera testnet account and obtain sufficient testnet HBAR. Resolved by using the Hedera portal’s faucet.
- **Deployment Issues**:
  - Encountered errors due to long filenames in `node_modules` when deploying to GitHub Pages. Fixed by updating `.gitignore` to exclude `node_modules` and focusing on the built files.
- **Time Constraints**:
  - Due to the hackathon deadline, mocked some functionality (e.g., Chainlink integration) but ensured core Hedera features were fully implemented.


## Technical Details

### Hedera Integration
AgriFuture uses Hedera’s blockchain to ensure transparency and security:
- **Consensus Service**:
  - Creates topics to record produce data immutably on the Hedera testnet.
  - Example: The `handleCreateTopic` function in `App.js` uses `TopicCreateTransaction` to create a topic, logging the topic ID (e.g., `0.0.123456`) to the console.

- **Token Service**:
  - Tokenizes crops as digital assets, enabling secure tracking and trading.
  - Example: The `handleTokenizeCrop` function uses `TokenCreateTransaction` to create a token for a crop (e.g., "Wheat"), logging the token ID to the console.
- **Benefits**:
  - Hedera’s low fees and high throughput make it ideal for agricultural use cases.
  - Immutability ensures trust between farmers and buyers.

### Chainlink Integration
- **Planned Feature**:
  - AgriFuture plans to integrate Chainlink Price Feeds to fetch real-time market data (e.g., the price of wheat).
  - This will ensure fair pricing in the marketplace and P2P trading features.
- **Current State**:
  - Mocked the functionality with a `fetchMarketPrice` function due to time constraints.
  - Example: `fetchMarketPrice("wheat")` returns a mocked price of `$300 per ton`.
- **Future Implementation**:
  - Will use Chainlink’s decentralized oracles to fetch accurate, tamper-proof market data.
- 
### Other Integrations
- **Chart.js**:
  - Used in the dashboard to visualize produce data (e.g., bar charts for quantity over time).
- **React Hook Form**:
  - Handles form inputs in the auth modal and tokenize crop form, ensuring efficient validation.
- **Framer Motion**:
  - Adds smooth animations (e.g., modal transitions, button hover effects).
- **React Toastify**:
  - Displays notifications (e.g., "Token created successfully").
- **Tailwind CSS**:
  - Provides responsive, modern styling across the app.
