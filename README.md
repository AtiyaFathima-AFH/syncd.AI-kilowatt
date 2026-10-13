# syncd. AI
### Smarter Products. Seamless Sync.

**An AI-Assisted Product Information Management (PIM) Platform**

**Developed for the Kilowott Hackathon | PIM System Integration Challenge**

---

## Project Overview

**syncd. AI** is an AI-assisted Product Information Management platform designed to simplify e-commerce catalog operations through centralized product management, intelligent data auditing, inventory monitoring, and WooCommerce synchronization workflows.

The platform combines traditional product management capabilities with AI-powered recommendations to help businesses maintain accurate, consistent, and organized product information.

By integrating Google Gemini AI with a modern web application, syncd. AI demonstrates how intelligent automation can improve product data quality and support better e-commerce decisions.

## Problem Statement

Managing product information across e-commerce platforms can be challenging, particularly when businesses handle large product catalogs.

Common challenges include:

- Incomplete or inconsistent product descriptions
- Incorrect pricing and inventory information
- Duplicate product identifiers (SKUs)
- Difficulty identifying low-stock products
- Repetitive manual catalog maintenance
- Errors during product synchronization

These challenges can reduce operational efficiency and affect the overall quality of online product listings.

## Proposed Solution

syncd. AI addresses these challenges through a centralized platform that enables users to manage, validate, analyze, and prepare product information for synchronization.

The solution combines:

- Centralized product catalog management
- Automated product quality validation
- AI-assisted catalog analysis
- Inventory monitoring
- WooCommerce synchronization workflows
- Synchronization history and error reporting

## Key Features

### 1. Product Management

Manage product information through a centralized dashboard.

- Add new products
- View and search existing products
- Edit product information
- Delete products
- Maintain product descriptions, prices, categories, and SKUs

### 2. Category Management

Organize products into categories to improve catalog structure and navigation.

### 3. Inventory Management

Monitor stock quantities and identify products requiring attention.

### 4. Product Quality Audit

A rule-based validation engine automatically detects common catalog issues, including:

- Missing product descriptions
- Invalid product prices
- Missing or duplicate SKUs
- Invalid stock quantities
- Low-stock products
- Missing product categories

Detected issues are categorized by priority to help users identify important improvements.

### 5. AI-Powered Catalog Assistant

Integrated with **Google Gemini AI**, the intelligent assistant analyzes product information and provides actionable recommendations.

Example queries:

- Audit my product catalog and identify issues.
- Which products need restocking?
- How can I improve my product descriptions?
- Recommend my top three catalog improvements.

A local rule-based fallback provides basic catalog analysis when the Gemini service is temporarily unavailable.

### 6. WooCommerce Synchronization

The Sync Center supports two operating modes.

**Demo Mode**
- Simulates product synchronization without modifying an external store
- Generates product-level synchronization results
- Records simulated synchronization activity

**Live WooCommerce Mode**
- Uses the WooCommerce REST API
- Supports product creation and updates using SKUs
- Reports synchronization failures

*Live synchronization requires valid WooCommerce API credentials and has not yet been verified against a real store.*

### 7. Synchronization History

View synchronization activity, including:

- Synchronization mode
- Date and time
- Products processed
- Successful and failed operations
- Individual product results

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js, Vite, JavaScript |
| Backend | Node.js, Express.js |
| AI Integration | Google Gemini API |
| E-commerce Integration | WooCommerce REST API |
| API Communication | REST, JSON |
| Styling | CSS |
| Development Tools | Visual Studio Code, Git, GitHub |

## System Architecture

The application follows a frontend–backend architecture.

**React Frontend**
- Product and inventory management
- AI Agent interface
- Product auditing
- Sync Center
- Synchronization history

↓

**Node.js / Express Backend**
- API request handling
- Product validation
- Gemini AI integration
- WooCommerce API integration

↓

**External Services**
- Google Gemini API
- WooCommerce REST API (when configured)

Product data is currently maintained locally in the browser, while synchronization history is recorded for demonstration purposes.

## Application Workflow

1. The user opens the syncd. AI dashboard.
2. Products are added or managed through the product catalog.
3. Product details are validated using the Product Quality Audit.
4. The AI Agent analyzes catalog data and provides recommendations.
5. The user reviews and improves product information.
6. Products can be processed through Demo Sync or the configured Live WooCommerce workflow.
7. Synchronization results are displayed in Sync History.

## Installation and Setup

### Prerequisites

- Node.js and npm
- Git
- A Google Gemini API key for AI functionality
- A WooCommerce store and REST API credentials for Live Sync (optional)

### 1. Clone the Repository

```bash
git clone https://github.com/AtiyaFathima-AFH/syncd.AI-kilowatt.git
cd syncd.AI-kilowatt
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file inside the `server` directory.

```env
PORT=5000
GEMINI_API_KEY=your_gemini_api_key
GEMINI_MODEL=gemini-3.8-flash
```

For optional live WooCommerce integration, add:

```env
WOO_STORE_URL=https://your-store.com
WOO_CONSUMER_KEY=your_consumer_key
WOO_CONSUMER_SECRET=your_consumer_secret
```

**Security:** Never commit real API keys, consumer secrets, or `.env` files to GitHub.

### 4. Start the Backend

```bash
node server/index.js
```

Backend URL:

`http://localhost:5000`

### 5. Start the Frontend

Open another terminal:

```bash
npm run dev
```

Frontend URL:

`http://localhost:5173`

### 6. Open the Application

Navigate to the frontend URL and begin managing products.

## Hackathon Results

During development, the following functionality was implemented:

- Interactive product management dashboard
- Product quality validation engine
- AI-assisted catalog recommendations
- Inventory monitoring
- Demo synchronization workflow
- Synchronization history
- Backend API integration

### Demonstrated Synchronization Result

| Metric | Result |
|---|---|
| Products processed | 4 |
| Simulated synchronizations | 4 |
| Reported failures | 0 |
| Sync history entry | Successfully recorded |

**Note:** These results represent a successful Demo Mode simulation, not actual product synchronization with a live WooCommerce store.

## Challenges and Solutions

### Gemini API Availability

**Challenge:** Temporary service overload caused some AI requests to fail.

**Solution:** Implemented a local catalog-analysis fallback to provide useful results when Gemini is unavailable.

### Frontend–Backend Integration

**Challenge:** API routing and server configuration issues initially prevented synchronization requests from completing.

**Solution:** Configured the API connection, implemented the synchronization endpoints, and verified successful Demo Mode responses.

### Reliable Product Validation

**Challenge:** Incomplete or inconsistent product information can lead to synchronization errors.

**Solution:** Added validation rules for product identifiers, pricing, stock quantities, and other catalog information.

## Current Limitations

- Live WooCommerce synchronization requires real-store integration testing.
- Product data is stored locally rather than in a production database.
- Synchronization history is intended for prototype use.
- Gemini AI responses depend on external API availability.
- The application is a hackathon prototype and is not yet production-ready.

## Future Enhancements

- Persistent database integration
- Advanced product attribute mapping
- Bulk import and export
- Scheduled synchronization
- Multi-store integration
- Advanced AI-based product enrichment
- Analytics and reporting
- User authentication and role-based access

## Potential Impact

syncd. AI aims to help e-commerce businesses:

- Reduce repetitive manual catalog work
- Improve product information quality
- Detect inventory-related risks earlier
- Maintain more consistent product listings
- Support informed catalog management decisions
- Simplify synchronization workflows

## Project Information

**Project:** syncd. AI

**Tagline:** Smarter Products. Seamless Sync.

**Hackathon:** Kilowott Hackathon

**Challenge:** PIM System Integration

**Category:** AI-Assisted E-commerce / Product Information Management

---

**syncd. AI — Making product management smarter, simpler, and more connected.**
