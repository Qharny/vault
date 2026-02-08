# AgriVault Ghana - Complete Project Documentation

## Table of Contents

### Part A: Project Proposal
1. [Problems We Are Solving](#1-problems-we-are-solving)
2. [Aim of the Project](#2-aim-of-the-project)
3. [Background Study](#3-background-study)
4. [Problem Statement](#4-problem-statement)
5. [Aim and Objectives of the Project](#5-aim-and-objectives-of-the-project)
6. [Methodology](#6-methodology)
7. [Expected Outcomes](#7-expected-outcomes)
8. [Tools and Facilities to be Used](#8-tools-and-facilities-to-be-used)
9. [Scope of Work](#9-scope-of-work)

### Part B: Technical Documentation
10. [Project Overview](#project-overview)
11. [Technology Stack](#technology-stack)
12. [Architecture](#architecture)
13. [Features & Modules](#features--modules)
14. [Database Schema](#database-schema)
15. [API & Edge Functions](#api--edge-functions)
16. [Authentication & Authorization](#authentication--authorization)
17. [Component Structure](#component-structure)
18. [Setup & Configuration](#setup--configuration)
19. [Admin Panel](#admin-panel)
20. [E-Commerce Features](#e-commerce-features)

---

# PART A: PROJECT PROPOSAL

---

## 1. Problems We Are Solving

### 1.1 Post-Harvest Losses
Ghanaian farmers lose an estimated **20-40% of their harvest annually** due to:
- Inadequate storage facilities and poor handling practices
- Lack of real-time information about optimal storage conditions
- Inability to predict spoilage risks based on weather and crop type
- This translates to billions of Ghanaian Cedis in losses each year, affecting food security and farmer livelihoods

### 1.2 Limited Access to Agricultural Information
- Farmers lack access to **timely weather forecasts** specific to their agricultural zones
- Limited knowledge about **pest and disease outbreaks** in nearby areas leads to widespread crop damage
- Inadequate information about **soil health and nutrient management** results in suboptimal yields
- Difficulty accessing **expert agricultural advice** due to limited extension officer coverage (ratio of 1:3000)

### 1.3 Poor Financial Management
- **Inconsistent record-keeping** of farm income and expenses
- Difficulty **tracking profitability** across different crops and seasons
- Lack of **financial planning tools** tailored for agricultural operations
- Limited understanding of true cost of production

### 1.4 Market Access Challenges
- Farmers struggle to **connect directly with buyers**, relying on middlemen
- **Price information asymmetry** leads to unfair pricing and exploitation
- Limited **visibility of available produce** in local markets
- No centralized platform for agricultural trade

### 1.5 Pest and Disease Management
- **Delayed identification** of crop diseases leads to widespread damage
- Lack of **community-based pest surveillance systems** for early warning
- Limited access to **treatment recommendations** available in Ghana
- No mechanism for reporting and tracking outbreaks

### 1.6 Climate Vulnerability
- **Unpredictable rainfall patterns** affecting planting and harvesting schedules
- Lack of tools for **climate-smart agricultural planning**
- No integration of weather data with farm management decisions

---

## 2. Aim of the Project

The primary aim of AgriVault Ghana is to **develop a comprehensive digital farm management platform** that empowers Ghanaian smallholder farmers to:

1. **Minimize post-harvest losses** through intelligent spoilage risk prediction and storage optimization
2. **Make data-driven decisions** using real-time environmental and agricultural data
3. **Improve farm productivity and profitability** through better resource management
4. **Connect with markets and buyers** through an integrated marketplace platform
5. **Access AI-powered agricultural advice** tailored to Ghana's unique farming conditions
6. **Build resilience** against climate variability and pest/disease outbreaks
7. **Achieve financial sustainability** through better record-keeping and analysis

---

## 3. Background Study

### 3.1 Agricultural Context in Ghana

Agriculture is the **backbone of Ghana's economy**, playing a critical role in:
- **Employment**: Approximately 44% of the workforce is engaged in agriculture
- **GDP Contribution**: About 20% of national GDP
- **Food Security**: Primary source of food for the population
- **Export Revenue**: Major export crops include cocoa, cashew, and palm oil

The sector is dominated by **smallholder farmers** who:
- Cultivate an average of 2 hectares per household
- Rely primarily on rain-fed agriculture
- Use traditional farming methods passed through generations
- Have limited access to modern agricultural technologies

### 3.2 Key Crops in Ghana

| Category | Crops |
|----------|-------|
| **Cash Crops** | Cocoa (world's 2nd largest producer), palm oil, cashew nuts, shea nuts |
| **Food Crops** | Maize, cassava, yam, plantain, rice, millet, sorghum |
| **Vegetables** | Tomatoes, onions, peppers, okra, garden eggs |
| **Fruits** | Pineapple, mango, pawpaw, oranges, bananas |

### 3.3 Agricultural Zones in Ghana

Ghana has distinct agricultural zones with varying conditions:

| Zone | Characteristics | Main Crops |
|------|-----------------|------------|
| **Coastal Savanna** | Low rainfall, sandy soils | Cassava, maize, vegetables |
| **Forest Zone** | High rainfall, fertile soils | Cocoa, oil palm, plantain |
| **Transitional Zone** | Moderate rainfall | Maize, cassava, yam |
| **Guinea Savanna** | Single rainy season | Maize, sorghum, groundnuts |
| **Sudan Savanna** | Low rainfall, dry conditions | Millet, sorghum, shea |

### 3.4 Technological Landscape

The digital transformation in Ghana presents opportunities:
- **Mobile phone penetration** exceeds 130%
- **Internet penetration** is approximately 53% and growing
- **Smartphone adoption** is increasing among rural populations
- Government initiatives like the **Ghana Digital Agricultural Accelerator** promote technology adoption

### 3.5 Existing Challenges and Gaps

1. **Infrastructure Gaps**: Poor road networks, inadequate storage and processing facilities
2. **Extension Services**: Limited reach with only 1 extension officer per 3,000 farmers
3. **Financial Exclusion**: Limited access to formal banking, credit, and insurance
4. **Climate Variability**: Increasingly unpredictable weather patterns
5. **Technology Adoption**: Low adoption of digital tools due to usability and access issues

### 3.6 Review of Existing Solutions

| Solution | Strengths | Limitations |
|----------|-----------|-------------|
| **Government Extension Services** | Free, localized knowledge | Limited coverage, infrequent visits |
| **NGO Programs** | Targeted interventions | Project-based, not sustainable |
| **Generic Farm Apps** | Modern technology | Not tailored to Ghana, language barriers |
| **Traditional Methods** | Trusted, familiar | Not data-driven, no climate adaptation |

---

## 4. Problem Statement

Despite being the cornerstone of Ghana's economy, the agricultural sector faces significant challenges that limit farmer productivity and income. **Post-harvest losses**, estimated at 20-40% of total production, represent a critical issue that undermines food security and farmer livelihoods.

Current interventions are **fragmented and inadequate**, with farmers relying on:
- Traditional knowledge passed through generations without scientific validation
- Sporadic government extension services with limited reach
- Informal market networks with limited price transparency and fairness
- No integrated system for weather monitoring, pest surveillance, or financial management

**There is a pressing need for an integrated digital solution** that:
1. Consolidates farm management, risk prediction, market access, and expert advice into a single, accessible platform
2. Is tailored to the unique needs of Ghanaian farmers (local crops, zones, languages)
3. Uses modern AI technology to provide intelligent recommendations
4. Creates a community-based approach to pest and disease surveillance
5. Empowers farmers with data-driven decision-making tools

Without such a solution, Ghanaian farmers will continue to suffer from preventable losses, limited market access, and inability to adapt to changing climate conditions.

---

## 5. Aim and Objectives of the Project

### 5.1 Main Aim

To design, develop, and deploy a **comprehensive web-based farm management system** that reduces post-harvest losses, improves agricultural productivity, and enhances market access for Ghanaian smallholder farmers.

### 5.2 Specific Objectives

#### Objective 1: Harvest Risk Assessment & Management
- Develop algorithms to predict spoilage risk based on crop type, storage conditions, and environmental factors
- Provide real-time alerts and actionable recommendations to minimize losses
- Track harvest quality and storage conditions over time

#### Objective 2: Weather Integration & Climate Adaptation
- Integrate weather data specific to Ghana's agricultural zones
- Provide actionable weather forecasts for farm planning
- Alert farmers to adverse weather conditions

#### Objective 3: Crop Health Monitoring & AI-Powered Disease Detection
- Implement AI-powered crop disease detection using image analysis
- Provide treatment recommendations available in Ghana
- Maintain a database of common crop diseases and their solutions

#### Objective 4: Financial Management & Record Keeping
- Enable comprehensive income and expense tracking
- Generate financial reports and profit/loss analysis
- Provide insights for better financial decision-making

#### Objective 5: Pest & Disease Surveillance Network
- Create a community-based pest and disease reporting system
- Visualize pest outbreaks on interactive maps for early warning
- Enable farmers to learn from nearby reports

#### Objective 6: Marketplace Integration
- Connect farmers directly with buyers
- Enable product listing and order management
- Reduce reliance on middlemen and improve pricing

#### Objective 7: AI Advisory System (AgriChat)
- Provide AI-powered farming advice tailored to Ghanaian conditions
- Support queries about planting, harvesting, storage, and pest control
- Deliver context-aware recommendations based on location and crops

#### Objective 8: Task & Farm Calendar Management
- Enable task scheduling and tracking
- Integrate with traditional farming calendars
- Provide seasonal reminders and planning tools

---

## 6. Methodology

### 6.1 Development Approach

The project follows an **Agile Development Methodology** with iterative development cycles, allowing for continuous feedback and improvement.

### 6.2 Development Phases

#### Phase 1: Research and Requirements Gathering
**Duration**: 2 weeks
- Stakeholder interviews with Ghanaian farmers and agricultural officers
- Analysis of existing agricultural apps and their limitations
- Documentation of functional and non-functional requirements
- User persona development and user journey mapping

#### Phase 2: System Design and Architecture
**Duration**: 2 weeks
- User interface design following mobile-first principles
- Database schema design for scalability and performance
- API architecture for third-party integrations
- Security architecture and data protection planning

#### Phase 3: Frontend Development
**Duration**: 4 weeks
- Implementation of React.js components with TypeScript
- Integration of UI component library (shadcn/ui)
- Responsive design for mobile and desktop
- Implementation of data visualization components

#### Phase 4: Backend Development
**Duration**: 4 weeks
- Database setup with PostgreSQL (Supabase)
- Authentication and authorization implementation
- API development for all modules
- Edge function development for AI integrations

#### Phase 5: AI Integration
**Duration**: 2 weeks
- Integration of Google Gemini AI for crop analysis
- Development of AI advisory chatbot
- Training and optimization for Ghanaian context

#### Phase 6: Testing and Quality Assurance
**Duration**: 2 weeks
- Unit testing of individual components
- Integration testing of system modules
- User acceptance testing with target farmers
- Performance and security testing

#### Phase 7: Deployment and Launch
**Duration**: 1 week
- Cloud deployment configuration
- Domain setup and SSL certificates
- Monitoring and logging setup
- User training materials and documentation

#### Phase 8: Post-Launch and Iteration
**Duration**: Ongoing
- Continuous feedback collection
- Bug fixes and improvements
- Feature enhancements based on user needs
- Performance optimization

### 6.3 Data Collection Methods

| Method | Purpose | Frequency |
|--------|---------|-----------|
| **Automated Weather APIs** | Real-time weather data | Continuous |
| **User Input (Forms)** | Harvest logs, soil tests, financial records | As needed |
| **AI Image Analysis** | Crop disease detection | On-demand |
| **Community Reporting** | Pest and disease reports | As reported |
| **System Analytics** | Usage patterns and performance | Continuous |

### 6.4 System Development Life Cycle (SDLC)

```
┌─────────────────────────────────────────────────────────────┐
│                    AGILE SDLC                               │
├─────────────────────────────────────────────────────────────┤
│  Sprint 1-2: Core Infrastructure                            │
│    ├── Authentication System                                │
│    ├── Database Setup                                       │
│    └── Basic UI Framework                                   │
├─────────────────────────────────────────────────────────────┤
│  Sprint 3-4: Farm Management Modules                        │
│    ├── Dashboard                                            │
│    ├── Crop Management                                      │
│    └── Harvest Tracking                                     │
├─────────────────────────────────────────────────────────────┤
│  Sprint 5-6: Advanced Features                              │
│    ├── AI Crop Analysis                                     │
│    ├── Weather Integration                                  │
│    └── Pest Surveillance Map                                │
├─────────────────────────────────────────────────────────────┤
│  Sprint 7-8: Financial & Marketplace                        │
│    ├── Financial Management                                 │
│    ├── Marketplace                                          │
│    └── Order Management                                     │
├─────────────────────────────────────────────────────────────┤
│  Sprint 9-10: Admin & Polish                                │
│    ├── Admin Panel                                          │
│    ├── Analytics & Reports                                  │
│    └── Testing & Optimization                               │
└─────────────────────────────────────────────────────────────┘
```

---

## 7. Expected Outcomes

### 7.1 Quantitative Outcomes

| Metric | Current Baseline | Target Improvement |
|--------|-----------------|-------------------|
| Post-harvest losses | 20-40% | Reduce by 30-50% |
| Farmer adoption | N/A | 1,000+ users in first year |
| Farmer income | Baseline | Increase by 15-25% |
| Pest outbreak response time | Days/weeks | Reduce by 60% |
| Financial record accuracy | <30% farmers | 90%+ compliance |
| Direct market sales | <20% | Increase to 50%+ |

### 7.2 Qualitative Outcomes

1. **Improved Decision Making**: Farmers will have access to data-driven insights for planting, harvesting, and storage decisions

2. **Enhanced Market Access**: Direct connections between farmers and buyers will reduce middleman exploitation

3. **Knowledge Sharing**: Community-based pest reporting will enable collective learning and early warning

4. **Financial Literacy**: Better understanding of farm economics and profitability

5. **Climate Resilience**: Proactive adaptation to weather changes through forecasting

6. **Empowerment**: Farmers will feel more confident and in control of their farming operations

### 7.3 Deliverables

| Deliverable | Description |
|-------------|-------------|
| **Web Application** | Fully functional, responsive web app accessible on mobile devices |
| **User Documentation** | Guides, tutorials, and help resources |
| **API Documentation** | Technical documentation for integrations |
| **Training Materials** | Video tutorials and quick-start guides |
| **Project Report** | Comprehensive evaluation and metrics |
| **Source Code** | Well-documented, maintainable codebase |

### 7.4 Success Indicators

- User registration and retention rates
- Frequency of feature usage (harvest logging, AI queries, etc.)
- Reduction in reported post-harvest losses
- Farmer satisfaction scores
- Market transaction volumes
- Pest report accuracy and response rates

---

## 8. Tools and Facilities to be Used

### 8.1 Frontend Technologies

| Tool/Technology | Version | Purpose |
|-----------------|---------|---------|
| **React** | 18.3.1 | User interface framework |
| **TypeScript** | Latest | Type-safe JavaScript development |
| **Tailwind CSS** | 3.x | Utility-first CSS styling |
| **shadcn/ui** | Latest | Pre-built accessible UI components |
| **Vite** | 5.x | Build tool and development server |
| **React Router** | 6.x | Client-side routing |
| **TanStack Query** | 5.x | Server state management |
| **Recharts** | 2.x | Data visualization and charts |
| **React Hook Form** | 7.x | Form handling and validation |
| **Zod** | 3.x | Schema validation |
| **date-fns** | 3.x | Date manipulation |
| **Lucide React** | Latest | Icon library |

### 8.2 Backend Technologies

| Tool/Technology | Purpose |
|-----------------|---------|
| **Supabase** | Backend-as-a-Service platform |
| **PostgreSQL** | Relational database |
| **Supabase Auth** | User authentication and authorization |
| **Supabase Storage** | File and image storage |
| **Edge Functions (Deno)** | Serverless functions |
| **Row Level Security (RLS)** | Database access control |

### 8.3 AI and External Services

| Service | Purpose |
|---------|---------|
| **Google Gemini AI** | Crop image analysis and advisory chatbot |
| **OpenWeatherMap API** | Weather data integration |
| **Mapbox GL** | Interactive mapping for pest surveillance |
| **Google Maps API** | Location services |

### 8.4 Development Tools

| Tool | Purpose |
|------|---------|
| **Git/GitHub** | Version control |
| **VS Code** | Code editor |
| **Lovable Platform** | AI-powered development and hosting |
| **ESLint** | Code quality and linting |
| **Prettier** | Code formatting |
| **Chrome DevTools** | Debugging and testing |

### 8.5 Deployment Infrastructure

| Service | Purpose |
|---------|---------|
| **Lovable Cloud** | Application hosting |
| **Supabase Cloud** | Database and backend hosting |
| **Cloudflare** | CDN and DDoS protection |
| **Let's Encrypt** | SSL/TLS certificates |

### 8.6 Hardware Requirements

**Development:**
- Computer with 8GB+ RAM
- Stable internet connection
- Modern web browser

**End Users:**
- Smartphone or computer with internet access
- Minimum 2G connection (3G+ recommended)
- Modern web browser (Chrome, Firefox, Safari, Edge)

---

## 9. Scope of Work

### 9.1 In Scope - Core Features

#### 9.1.1 User Management
- [x] User registration and authentication
- [x] Profile management with farm details
- [x] Role-based access control (Admin, Farmer, User)
- [x] Password reset and account recovery

#### 9.1.2 Dashboard
- [x] Overview of farm metrics and activities
- [x] Weather widget with location-based forecasts
- [x] Risk alerts and notifications
- [x] Quick access to all features
- [x] Summary charts and statistics

#### 9.1.3 Harvest Management
- [x] Log harvest details (crop, quantity, quality, location)
- [x] Spoilage risk calculation and alerts
- [x] Historical harvest data analysis
- [x] Storage location tracking
- [x] Export harvest reports

#### 9.1.4 Crop Management
- [x] Crop registration and tracking
- [x] Growth stage monitoring
- [x] Expected harvest date predictions
- [x] Field assignment
- [x] Local variety support

#### 9.1.5 Weather Monitoring
- [x] Real-time weather data for Ghana
- [x] 7-day forecasts
- [x] Weather alerts for agricultural planning
- [x] Historical weather trends

#### 9.1.6 Soil Analysis
- [x] Record soil test results
- [x] Track pH, nutrients, and moisture
- [x] Get soil improvement recommendations
- [x] Link to specific fields

#### 9.1.7 Task Management
- [x] Create and assign farm tasks
- [x] Set priorities and due dates
- [x] Track task completion
- [x] Calendar integration

#### 9.1.8 Financial Management
- [x] Income tracking from sales
- [x] Expense recording by category
- [x] Profit/loss analysis
- [x] Financial reports generation

#### 9.1.9 AI Crop Analysis
- [x] Upload crop images for disease detection
- [x] AI-powered health assessment
- [x] Treatment recommendations
- [x] Historical analysis records

#### 9.1.10 AI Advisory (AgriChat)
- [x] Conversational AI for farming advice
- [x] Ghana-specific recommendations
- [x] Storage tips and best practices
- [x] Pest and disease guidance

#### 9.1.11 Pest & Disease Surveillance
- [x] Report pest/disease sightings
- [x] Interactive map visualization
- [x] Severity tracking
- [x] Community-based early warning

#### 9.1.12 Marketplace
- [x] Product listing for farmers
- [x] Browse and search products
- [x] Shopping cart functionality
- [x] Order management

#### 9.1.13 Farm Calendar
- [x] Event scheduling
- [x] Traditional farming calendar
- [x] Crop-specific reminders
- [x] Seasonal planning

#### 9.1.14 Admin Panel
- [x] User management
- [x] Product moderation
- [x] Order oversight
- [x] Analytics dashboard

### 9.2 Out of Scope (Future Phases)

The following features are planned for future development phases:

| Feature | Phase | Priority |
|---------|-------|----------|
| Native mobile apps (iOS/Android) | Phase 2 | High |
| Offline functionality with sync | Phase 2 | High |
| SMS notifications for feature phones | Phase 2 | Medium |
| Mobile money integration (MTN, Vodafone) | Phase 2 | High |
| Government database integration | Phase 3 | Medium |
| Drone-based field monitoring | Phase 3 | Low |
| Blockchain traceability | Phase 3 | Low |
| Multi-language support (local dialects) | Phase 2 | Medium |
| IoT sensor integration | Phase 3 | Medium |
| Machine learning price prediction | Phase 3 | Medium |

### 9.3 Target Users

| User Type | Description | Priority |
|-----------|-------------|----------|
| **Primary** | Smallholder farmers in Ghana (2-10 hectares) | Highest |
| **Secondary** | Agricultural extension officers | High |
| **Tertiary** | Agricultural cooperatives and buyers | Medium |

### 9.4 Geographic Focus

**Initial Deployment**: All regions of Ghana

**Priority Zones**:
1. Ashanti Region - Major cocoa and food crop production
2. Brong-Ahafo Region - Major food crop production
3. Eastern Region - Cocoa and diversified farming
4. Northern Region - Grain and legume production

### 9.5 Constraints and Limitations

| Constraint | Impact | Mitigation |
|------------|--------|------------|
| Internet connectivity required | Rural access issues | Lightweight design, future offline mode |
| Smartphone/computer needed | Excludes feature phone users | Future SMS integration |
| English interface (initially) | Language barrier | Planned local language support |
| Third-party API dependency | Service availability | Error handling, fallback options |

### 9.6 Assumptions

1. Target users have access to smartphones or computers
2. Internet connectivity is available (even if intermittent)
3. Users have basic digital literacy
4. Weather and AI API services remain available
5. Supabase/Lovable Cloud services are reliable

### 9.7 Risks and Mitigation

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Low user adoption | Medium | High | User-centered design, training materials |
| API service disruption | Low | Medium | Caching, fallback mechanisms |
| Data security breach | Low | High | RLS, encryption, security audits |
| Scalability issues | Medium | Medium | Cloud architecture, performance monitoring |
| Inaccurate AI predictions | Medium | Medium | User feedback loop, continuous improvement |

---

# PART B: TECHNICAL DOCUMENTATION

---

## Project Overview

**AgriVault Ghana** is a comprehensive farm management and e-commerce platform designed specifically for Ghanaian farmers. The system combines traditional farm management tools with modern AI-powered features and marketplace functionality to help farmers optimize their operations and connect directly with buyers and suppliers.

### Target Users
- **Farmers**: Primary users managing crops, tasks, and selling produce
- **Buyers**: Purchase agricultural products directly from farmers
- **Input Suppliers**: Sell seeds, fertilizers, and farming equipment
- **Administrators**: Platform management and oversight

### Geographic Focus
- Tailored for Ghana's agricultural zones
- Support for local crops (cocoa, maize, cassava, yam, plantain, rice)
- Weather data specific to Ghana's climate zones
- Local language support (English and Ghanaian languages)

---

## Technology Stack

### Frontend
- **Framework**: React 18.3.1 with TypeScript
- **Build Tool**: Vite
- **Styling**: Tailwind CSS with custom design system
- **UI Components**: shadcn/ui (Radix UI primitives)
- **State Management**: React Context API + TanStack Query
- **Routing**: React Router DOM v6
- **Charts**: Recharts
- **Maps**: Google Maps API (@react-google-maps/api)
- **Forms**: React Hook Form + Zod validation
- **Date Handling**: date-fns

### Backend (Lovable Cloud/Supabase)
- **Database**: PostgreSQL (Supabase)
- **Authentication**: Supabase Auth
- **Storage**: Supabase Storage
- **Edge Functions**: Deno-based serverless functions
- **Real-time**: Supabase Realtime subscriptions

### AI Integration
- **AI Provider**: Google Gemini AI
- **Use Cases**: 
  - Crop disease detection
  - Agricultural advisory chatbot
  - Crop image analysis

### APIs & Services
- **Weather Data**: Custom weather API integration
- **Maps**: Google Maps JavaScript API
- **AI**: Google Generative AI (@google/generative-ai)

---

## Architecture

### High-Level Architecture

```
┌─────────────────────────────────────────────────┐
│            React Frontend (Vite)                │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐     │
│  │  Pages   │  │Components│  │ Contexts │     │
│  └──────────┘  └──────────┘  └──────────┘     │
└─────────────────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────┐
│         Lovable Cloud (Supabase)                │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐     │
│  │PostgreSQL│  │   Auth   │  │ Storage  │     │
│  └──────────┘  └──────────┘  └──────────┘     │
│  ┌──────────────────────────────────────┐     │
│  │      Edge Functions (Deno)           │     │
│  │  - analyze-crop-image                │     │
│  │  - chat-ai                           │     │
│  │  - gemini-chat                       │     │
│  └──────────────────────────────────────┘     │
└─────────────────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────┐
│           External Services                     │
│  - Google Gemini AI                             │
│  - Google Maps API                              │
│  - Weather Data API                             │
└─────────────────────────────────────────────────┘
```

### Folder Structure

```
agrivault/
├── public/               # Static assets
├── src/
│   ├── api/             # API client modules
│   ├── components/      # React components
│   │   ├── ui/         # shadcn/ui components
│   │   ├── dashboard/  # Dashboard-specific components
│   │   └── financial/  # Financial management components
│   ├── contexts/        # React Context providers
│   ├── hooks/          # Custom React hooks
│   ├── integrations/   # Third-party integrations
│   │   └── supabase/   # Supabase client & types
│   ├── lib/            # Utility libraries
│   ├── pages/          # Route pages
│   ├── types/          # TypeScript type definitions
│   ├── utils/          # Helper functions
│   ├── index.css       # Global styles & design tokens
│   └── main.tsx        # Application entry point
├── supabase/
│   ├── functions/      # Edge functions
│   └── config.toml     # Supabase configuration
└── ...config files
```

---

## Features & Modules

### 1. Dashboard
**Location**: `src/pages/Dashboard.tsx`

**Features**:
- Summary cards showing key metrics
- Crop distribution pie chart
- Harvest trends line chart
- Soil health radar chart
- Task status overview
- Recent harvests list
- Quick action buttons

**Components**:
- `DashboardSummaryCards.tsx`
- `CropDistributionChart.tsx`
- `HarvestTrendsChart.tsx`
- `SoilHealthChart.tsx`
- `TaskStatusChart.tsx`
- `RecentHarvestsList.tsx`

### 2. Crop Management
**Location**: `src/pages/Crops.tsx`

**Features**:
- Add/edit/delete crops
- Track crop growth stages
- Monitor crop health
- Support for major Ghanaian crops
- Local variety management
- Crop images and details

**Supported Crops**:
- Cocoa
- Maize
- Cassava
- Yam
- Plantain
- Rice
- Other local varieties

### 3. Weather Monitoring
**Location**: `src/pages/Weather.tsx`

**Features**:
- Real-time weather data for farm locations
- 7-day weather forecast
- Agricultural weather metrics
- Ghana-specific climate zone data
- Weather alerts and warnings
- Temperature, humidity, rainfall tracking

**Component**: `WeatherWidget.tsx`

### 4. Soil Analysis
**Location**: `src/pages/SoilAnalysis.tsx`

**Features**:
- Record soil test results
- Track soil pH, nutrients, and composition
- Region-specific recommendations
- Soil improvement guidance for Ghana's zones
- Historical soil data tracking
- Visual soil health indicators

### 5. Task Management
**Location**: `src/pages/Tasks.tsx`

**Features**:
- Create and assign farm tasks
- Set priorities and due dates
- Track task completion status
- Seasonal task templates
- Task categories (planting, fertilizing, harvesting, etc.)
- Task reminders and notifications

### 6. Harvest Tracking
**Location**: `src/pages/Harvests.tsx`

**Features**:
- Record harvest yields
- Track harvest quality
- Storage condition monitoring
- Analyze harvest data
- Market price integration
- Export harvest reports

**Components**:
- `HarvestTable.tsx`
- `HarvestRiskCard.tsx`
- `NewHarvestForm.tsx`

**Types**: `src/types/harvest.ts`
**Utils**: `src/utils/riskCalculator.ts`

### 7. AI Advisor
**Location**: `src/pages/AIAdvisor.tsx`

**Features**:
- AI-powered agricultural recommendations
- Planting time optimization
- Issue identification and prevention
- Local language support
- Context-aware advice for Ghana
- Chat-based interface

**Component**: `AgriChat.tsx`

### 8. Crop Disease Analysis
**Location**: `src/pages/AnalyseCropImage.tsx`

**Features**:
- Upload crop images
- AI-powered disease detection
- Treatment recommendations
- Local variety recognition
- Severity assessment
- Prevention guidelines

**Edge Function**: `supabase/functions/analyze-crop-image/index.ts`

### 9. Pest & Disease Surveillance Map
**Location**: `src/pages/PestDiseaseMap.tsx`

**Features**:
- Interactive Google Map with Ghana focus
- Report pest/disease outbreaks
- View nearby reports
- Heatmap visualization
- Filter by pest/disease type and severity
- Real-time data from database
- Crowd-sourced reporting

**Database Integration**:
- Stores reports in `pest_reports` table
- Real-time updates
- Geolocation data

### 10. Financial Management
**Location**: `src/pages/FinancialManagement.tsx`

**Features**:
- Income tracking
- Expense tracking
- Profit/loss overview
- Financial reports and analytics
- Category-based tracking
- Export financial data

**Components**:
- `IncomeTracker.tsx`
- `ExpenseTracker.tsx`
- `ProfitLossOverview.tsx`
- `FinancialReports.tsx`

### 11. Calendar & Events
**Location**: `src/pages/Calendar.tsx`

**Features**:
- Agricultural calendar
- Traditional farming events
- Task scheduling
- Seasonal reminders
- Event categories
- Custom event creation

### 12. Analytics & Reports
**Location**: `src/pages/Analytics.tsx`, `src/pages/Reports.tsx`

**Features**:
- Farm performance analytics
- Crop yield analysis
- Financial reports
- Custom date ranges
- Export functionality
- Visual data representation

### 13. User Profile & Settings
**Locations**: 
- `src/pages/Profile.tsx`
- `src/pages/Settings.tsx`

**Features**:
- User profile management
- Language preferences
- Notification settings
- Account security
- Farm information
- Contact details

### 14. Help & Support
**Location**: `src/pages/HelpAndSupport.tsx`

**Features**:
- Comprehensive FAQ
- User guides and tutorials
- Contact support
- Local language support
- Video tutorials
- Community forum links

### 15. Admin Panel (NEW)
**Location**: `src/pages/AdminPanel.tsx`

**Features**: See [Admin Panel](#admin-panel) section below

---

## Database Schema

### Core Tables

#### 1. `users` (Supabase Auth)
Extended with custom profile data:
```sql
- id (uuid, PK)
- email (text)
- phone (text)
- role (enum: farmer, buyer, supplier, admin)
- full_name (text)
- farm_location (text)
- language_preference (text)
- created_at (timestamp)
- updated_at (timestamp)
```

#### 2. `crops`
```sql
- id (uuid, PK)
- user_id (uuid, FK -> users)
- crop_name (text)
- crop_type (text)
- variety (text)
- planting_date (date)
- expected_harvest_date (date)
- field_size (numeric)
- growth_stage (text)
- health_status (text)
- notes (text)
- image_url (text)
- created_at (timestamp)
- updated_at (timestamp)
```

#### 3. `harvests`
```sql
- id (uuid, PK)
- user_id (uuid, FK -> users)
- crop_id (uuid, FK -> crops)
- harvest_date (date)
- quantity (numeric)
- unit (text)
- quality_grade (text)
- storage_location (text)
- storage_conditions (text)
- market_price (numeric)
- notes (text)
- created_at (timestamp)
```

#### 4. `tasks`
```sql
- id (uuid, PK)
- user_id (uuid, FK -> users)
- crop_id (uuid, FK -> crops, nullable)
- title (text)
- description (text)
- task_type (enum: planting, fertilizing, harvesting, weeding, other)
- priority (enum: low, medium, high)
- status (enum: pending, in_progress, completed)
- due_date (date)
- completed_at (timestamp, nullable)
- assigned_to (text)
- created_at (timestamp)
```

#### 5. `soil_tests`
```sql
- id (uuid, PK)
- user_id (uuid, FK -> users)
- test_date (date)
- field_location (text)
- ph_level (numeric)
- nitrogen (numeric)
- phosphorus (numeric)
- potassium (numeric)
- organic_matter (numeric)
- recommendations (text)
- lab_name (text)
- created_at (timestamp)
```

#### 6. `weather_data`
```sql
- id (uuid, PK)
- location (text)
- date (date)
- temperature_high (numeric)
- temperature_low (numeric)
- humidity (numeric)
- rainfall (numeric)
- wind_speed (numeric)
- conditions (text)
- forecast (jsonb)
- created_at (timestamp)
```

#### 7. `pest_reports` (NEW)
```sql
- id (uuid, PK)
- user_id (uuid, FK -> users)
- latitude (numeric)
- longitude (numeric)
- pest_type (text)
- disease_type (text)
- crop_affected (text)
- severity (enum: low, medium, high, critical)
- description (text)
- image_url (text)
- status (enum: active, resolved, false_alarm)
- reported_at (timestamp)
- resolved_at (timestamp, nullable)
- created_at (timestamp)
```

### E-Commerce Tables (NEW)

#### 8. `market_products`
```sql
- id (uuid, PK)
- seller_id (uuid, FK -> users)
- product_type (enum: produce, seeds, fertilizer, equipment)
- product_name (text)
- description (text)
- category (text)
- subcategory (text)
- price (numeric)
- unit (text)
- quantity_available (numeric)
- images (text[])
- location (text)
- status (enum: pending, approved, rejected, sold)
- featured (boolean)
- approved_by (uuid, FK -> users, nullable)
- approved_at (timestamp, nullable)
- created_at (timestamp)
- updated_at (timestamp)
```

#### 9. `orders`
```sql
- id (uuid, PK)
- buyer_id (uuid, FK -> users)
- seller_id (uuid, FK -> users)
- product_id (uuid, FK -> market_products)
- quantity (numeric)
- total_price (numeric)
- platform_commission (numeric)
- status (enum: pending, confirmed, in_transit, delivered, cancelled, refunded)
- payment_status (enum: pending, paid, refunded)
- delivery_address (text)
- delivery_method (text)
- tracking_number (text, nullable)
- notes (text)
- ordered_at (timestamp)
- confirmed_at (timestamp, nullable)
- delivered_at (timestamp, nullable)
- created_at (timestamp)
```

#### 10. `transactions`
```sql
- id (uuid, PK)
- order_id (uuid, FK -> orders)
- buyer_id (uuid, FK -> users)
- seller_id (uuid, FK -> users)
- amount (numeric)
- commission (numeric)
- payment_method (text)
- transaction_reference (text)
- status (enum: pending, completed, failed, refunded)
- processed_at (timestamp)
- created_at (timestamp)
```

#### 11. `disputes`
```sql
- id (uuid, PK)
- order_id (uuid, FK -> orders)
- complainant_id (uuid, FK -> users)
- respondent_id (uuid, FK -> users)
- complaint_type (enum: quality, delivery, payment, other)
- description (text)
- status (enum: open, investigating, resolved, closed)
- resolution (text, nullable)
- resolved_by (uuid, FK -> users, nullable)
- resolved_at (timestamp, nullable)
- created_at (timestamp)
- updated_at (timestamp)
```

#### 12. `reviews`
```sql
- id (uuid, PK)
- order_id (uuid, FK -> orders)
- reviewer_id (uuid, FK -> users)
- reviewee_id (uuid, FK -> users)
- product_id (uuid, FK -> market_products)
- rating (integer, 1-5)
- comment (text)
- created_at (timestamp)
```

#### 13. `activity_logs`
```sql
- id (uuid, PK)
- admin_id (uuid, FK -> users)
- action_type (text)
- target_type (text)
- target_id (uuid)
- description (text)
- metadata (jsonb)
- created_at (timestamp)
```

---

## API & Edge Functions

### Edge Functions (Deno/TypeScript)

#### 1. `analyze-crop-image`
**Location**: `supabase/functions/analyze-crop-image/index.ts`

**Purpose**: Analyze crop images for disease detection using Google Gemini AI

**Endpoint**: `POST /functions/v1/analyze-crop-image`

**Request**:
```json
{
  "image": "base64_encoded_image",
  "cropType": "maize"
}
```

**Response**:
```json
{
  "disease": "Fall Armyworm",
  "severity": "medium",
  "confidence": 0.85,
  "treatment": "Apply Bt-based pesticide...",
  "prevention": "Regular monitoring..."
}
```

#### 2. `chat-ai`
**Location**: `supabase/functions/chat-ai/index.ts`

**Purpose**: AI agricultural advisory chatbot

**Endpoint**: `POST /functions/v1/chat-ai`

**Request**:
```json
{
  "message": "When should I plant maize in Ghana?",
  "context": {
    "location": "Kumasi",
    "crops": ["maize", "cassava"]
  }
}
```

**Response**:
```json
{
  "response": "For Kumasi, the best time to plant maize is...",
  "confidence": 0.92
}
```

#### 3. `gemini-chat`
**Location**: `supabase/functions/gemini-chat/index.ts`

**Purpose**: General Gemini AI integration for various AI features

**Endpoint**: `POST /functions/v1/gemini-chat`

### Client-Side API

#### Crop Analysis API
**Location**: `src/api/cropAnalysis.js`

**Functions**:
- `analyzeCropImage(imageFile, cropType)`: Analyze crop image
- `getCropRecommendations(cropType, location)`: Get crop recommendations

---

## Authentication & Authorization

### Authentication Methods
1. **Email/Password**: Primary method using Supabase Auth
2. **Phone/OTP**: SMS-based authentication
3. **Google Sign-In**: OAuth integration (planned)

### User Roles
- **Farmer**: Default role, full access to farm management features
- **Buyer**: Access to marketplace, limited farm features
- **Supplier**: Access to marketplace as seller, limited farm features
- **Admin**: Full access to admin panel and all features

### Row Level Security (RLS)
All database tables use RLS policies to ensure:
- Users can only access their own data
- Admins have elevated permissions
- Public data (market listings, pest reports) is accessible to all authenticated users

### Auth Context
**Location**: `src/contexts/AuthContext.tsx`

**Provides**:
- `user`: Current user object
- `session`: Current session
- `signIn()`: Login function
- `signUp()`: Registration function
- `signOut()`: Logout function
- `isAdmin`: Boolean flag for admin access

---

## Component Structure

### Layout Components
- `Layout.tsx`: Main app layout with sidebar
- `AppSidebar.tsx`: Collapsible sidebar navigation
- `AppSidebarExtended.tsx`: Extended sidebar with additional links

### UI Components (`src/components/ui/`)
Based on shadcn/ui (Radix UI primitives):
- Forms: `input`, `textarea`, `select`, `checkbox`, `radio-group`, `switch`
- Display: `card`, `table`, `badge`, `avatar`, `separator`
- Overlays: `dialog`, `sheet`, `drawer`, `popover`, `tooltip`, `alert-dialog`
- Navigation: `tabs`, `accordion`, `breadcrumb`, `pagination`, `navigation-menu`
- Feedback: `toast`, `alert`, `progress`, `skeleton`
- Charts: `chart` (recharts wrapper)

### Feature Components

#### Dashboard Components
- `DashboardSummaryCards.tsx`: Metric cards
- `CropDistributionChart.tsx`: Pie chart
- `HarvestTrendsChart.tsx`: Line chart
- `SoilHealthChart.tsx`: Radar chart
- `TaskStatusChart.tsx`: Status overview
- `RecentHarvestsList.tsx`: Recent harvests

#### Financial Components
- `ExpenseTracker.tsx`
- `IncomeTracker.tsx`
- `ProfitLossOverview.tsx`
- `FinancialReports.tsx`

#### Shared Components
- `WeatherWidget.tsx`: Weather display
- `AgriChat.tsx`: AI chat interface
- `HarvestTable.tsx`: Harvest data table
- `HarvestRiskCard.tsx`: Risk assessment display
- `NewHarvestForm.tsx`: Form for recording harvests

---

## Setup & Configuration

### Prerequisites
- Node.js 18+ and npm
- Lovable Cloud account (for backend)
- Google Maps API key
- Google Gemini API key

### Environment Variables
Create `.env` file:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_GOOGLE_MAPS_API_KEY=AIzaSyAqNJcq9hhvuJ6Aeewup5sbk9WnoMYYU08
```

### Installation
```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

### Supabase Setup
1. Enable Lovable Cloud in project settings
2. Create database tables using schema above
3. Set up RLS policies
4. Configure authentication providers
5. Upload edge functions
6. Add API keys to secrets

### Google Maps Setup
1. Enable Maps JavaScript API
2. Enable Places API
3. Set up API key restrictions
4. Add key to environment variables

---

## Admin Panel

**Location**: `src/pages/AdminPanel.tsx`

### Features

#### 1. User & Vendor Management
- View all users with filters
- Approve/suspend vendor accounts
- Assign user roles
- Verify farmer documents
- Grant trust badges
- View user activity logs

#### 2. Product & Listing Management
- Approve/reject crop and input listings
- Flag inappropriate content
- Set product visibility
- Feature products on homepage
- Manage categories and subcategories
- Bulk actions on listings

#### 3. Order Management
- View all platform orders
- Filter by status and date range
- Force-cancel or refund orders
- Assign delivery logistics
- Track order fulfillment
- Generate order reports

#### 4. Payment & Commission Control
- Revenue dashboard
- Set commission rates by category
- Track payment statuses
- Process refunds
- Export financial reports (Excel, CSV, PDF)
- Payment gateway integration monitoring

#### 5. Dispute Resolution Center
- View all disputes
- Ticket-based resolution system
- Access chat logs
- Ban malicious users
- Automated dispute escalation
- Resolution tracking

#### 6. Analytics & Insights
- Daily/weekly/monthly reports
- Top-selling products and vendors
- Regional activity heatmap
- User growth and retention metrics
- Revenue analytics
- Conversion tracking

#### 7. Content & Language Control
- Manage translations
- Edit platform announcements
- Update FAQs
- Push notifications
- Banner management
- Content moderation

#### 8. Promotions & Marketing
- Feature vendors or products
- Approve sponsored placements
- Create discount campaigns
- Seasonal promotions
- Email marketing integration
- Promotional analytics

### Admin UI Structure
```
Admin Dashboard
├── Overview Cards (Sales, Users, Orders, Active Listings)
├── Quick Actions (Approve Listings, Resolve Disputes)
├── Navigation Tabs
│   ├── Users & Vendors
│   ├── Products & Listings
│   ├── Orders & Transactions
│   ├── Disputes
│   ├── Analytics
│   ├── Content Management
│   └── Settings
└── Activity Feed
```

### Admin Permissions
- `admin.read`: View admin dashboard
- `admin.users.manage`: Manage users
- `admin.products.moderate`: Moderate listings
- `admin.orders.manage`: Manage orders
- `admin.disputes.resolve`: Resolve disputes
- `admin.analytics.view`: View analytics
- `admin.content.edit`: Edit content
- `admin.super`: Full access (super admin)

---

## E-Commerce Features

### Marketplace Structure
- **Produce**: Fresh crops from farmers
- **Seeds**: Local and improved varieties
- **Fertilizers**: Organic and synthetic
- **Equipment**: Tools and machinery
- **Services**: Consulting, land preparation

### Buyer Features
- Browse products by category
- Search and filter listings
- View vendor profiles and ratings
- Add to cart and checkout
- Track orders
- Leave reviews
- Dispute resolution

### Seller Features
- Create product listings
- Manage inventory
- Track sales and revenue
- Process orders
- Communicate with buyers
- Analytics dashboard
- Promotional tools

### Transaction Flow
1. Buyer browses and adds to cart
2. Checkout and payment
3. Seller receives order notification
4. Seller confirms and prepares order
5. Delivery/pickup arranged
6. Buyer receives and confirms
7. Payment released to seller (minus commission)
8. Both parties can review

### Payment Integration
- Mobile Money (MTN, Vodafone, AirtelTigo)
- Bank transfer
- Cash on delivery
- Escrow system for trust
- Automated commission calculation
- Refund processing

### Commission Structure
Configurable by admin:
- Produce: 5-10%
- Seeds: 8-12%
- Fertilizers: 8-12%
- Equipment: 10-15%
- Services: 15-20%

---

## Design System

### Color Tokens (HSL format)
Defined in `src/index.css`:

**Light Mode**:
```css
--background: 0 0% 100%
--foreground: 20 14.3% 4.1%
--primary: 24 9.8% 10%
--secondary: 60 4.8% 95.9%
--accent: 60 4.8% 95.9%
--muted: 60 4.8% 95.9%
```

**Dark Mode**:
```css
--background: 20 14.3% 4.1%
--foreground: 60 9.1% 97.8%
--primary: 60 9.1% 97.8%
--secondary: 12 6.5% 15.1%
--accent: 12 6.5% 15.1%
--muted: 12 6.5% 15.1%
```

### Typography
- Font Family: System font stack
- Headings: Bold, scaled sizing
- Body: Regular weight
- Code: Monospace

### Spacing
Tailwind default spacing scale (0.25rem base)

### Components
All UI components use semantic tokens from the design system

---

## Development Guidelines

### Code Style
- TypeScript strict mode
- ESLint configuration
- Functional components with hooks
- Descriptive variable names
- Comments for complex logic

### Component Guidelines
- Small, focused components
- Props interface for TypeScript
- Default exports for pages
- Named exports for utilities
- Responsive design by default

### State Management
- Local state with `useState`
- Global state with Context API
- Server state with TanStack Query
- Form state with React Hook Form

### Performance
- Code splitting with React.lazy
- Image optimization
- Lazy loading for charts and maps
- Memoization where appropriate
- Virtual scrolling for large lists

### Testing
- Component testing (to be implemented)
- Integration testing (to be implemented)
- E2E testing (to be implemented)

### Deployment
- Automatic deployment via Lovable
- Edge functions auto-deploy
- Environment variables in Lovable secrets
- Custom domain support

---

## Future Enhancements

### Planned Features
1. Mobile app (React Native)
2. Offline mode with sync
3. SMS notifications
4. WhatsApp integration
5. Blockchain for supply chain
6. IoT sensor integration
7. Drone imagery analysis
8. Cooperative management
9. Loan and insurance integration
10. Multi-farm management

### Technical Improvements
1. PWA support
2. Performance optimization
3. Advanced caching strategies
4. Real-time collaboration
5. GraphQL API
6. Microservices architecture
7. Advanced AI models
8. Predictive analytics
9. Machine learning for yield prediction
10. Automated testing suite

---

## Support & Resources

### Documentation
- README.md: Quick start guide
- This file: Complete documentation
- Inline code comments
- API documentation (to be created)

### Community
- GitHub Issues: Bug reports and feature requests
- Discord/Slack: Community support
- Email: support@agrivault.com

### Contributing
1. Fork the repository
2. Create feature branch
3. Make changes with tests
4. Submit pull request
5. Code review process

### License
MIT License - See LICENSE file

---

## Changelog

### Version 1.0.0 (Current)
- Initial release
- Core farm management features
- AI advisor and crop analysis
- Pest surveillance map with database
- Admin panel
- E-commerce marketplace foundation

---

**Last Updated**: 2025-10-14

**Maintained By**: AgriVault Development Team

**Contact**: support@agrivault.com
