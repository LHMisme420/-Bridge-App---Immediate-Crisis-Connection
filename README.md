# -Bridge-App---Immediate-Crisis-Connection
Bridge App
bridge-app/
│
├── 📄 README.md                          # Main project documentation
├── 📄 LICENSE                            # MIT License - open source
├── 📄 package.json                       # Dependencies and scripts
├── 📄 .gitignore                         # Standard React/Firebase ignores
│
├── 📁 public/                            # PWA public assets
│   ├── index.html
│   ├── manifest.json                     # PWA configuration
│   └── service-worker.js                 # Offline functionality
│
├── 📁 src/                               # Main application source
│   ├── index.js
│   ├── App.js                            # Main app component
│   ├── App.css                           # Global styles
│   │
│   ├── 📁 components/                    # React components
│   │   ├── EmergencyLanding.js           # 3-button landing page
│   │   ├── CrisisFlow.js                 # Crisis intervention flow
│   │   ├── ComfortFlow.js                # Emotional support flow
│   │   ├── ConnectionFlow.js             # Community connection flow
│   │   ├── ResourceMap.js                # Interactive resource map
│   │   ├── VolunteerPortal.js            # Volunteer management
│   │   └── AdminDashboard.js             # Real-time metrics
│   │
│   ├── 📁 services/                      # Backend services
│   │   ├── firebase.js                   # Firebase configuration
│   │   ├── crisisRouter.js               # Route to appropriate help
│   │   ├── geolocation.js                # Location services
│   │   ├── twilioService.js              # SMS/voice integration
│   │   └── analytics.js                  # Impact tracking
│   │
│   ├── 📁 data/                          # Resource databases
│   │   ├── crisisResources.json          # National crisis lines
│   │   ├── chicagoResources.json         # Chicago-specific resources
│   │   ├── baltimoreResources.json       # Baltimore-specific resources
│   │   └── templateResources.json        # Template for new cities
│   │
│   ├── 📁 hooks/                         # Custom React hooks
│   │   ├── useLocation.js                # Geolocation hook
│   │   ├── useCrisisDetection.js         # Urgency assessment
│   │   └── useLocalStorage.js            # Offline data persistence
│   │
│   └── 📁 utils/                         # Utility functions
│       ├── emergencyValidator.js         # Input validation
│       ├── privacyUtils.js               # Data anonymization
│       └── formatPhone.js                # Phone number formatting
│
├── 📁 docs/                              # Documentation
│   ├── DEPLOYMENT.md                     # Deployment instructions
│   ├── API_INTEGRATION.md                # Partner API documentation
│   ├── VOLUNTEER_GUIDE.md                # Volunteer training
│   ├── RESOURCE_ADDING.md                # How to add new resources
│   └── CRISIS_PROTOCOLS.md               # Safety procedures
│
├── 📁 scripts/                           # Build and deployment scripts
│   ├── deploy-prod.js                    # Production deployment
│   ├── emergency-build.js                # 72-hour build script
│   ├── data-import.js                    # Resource data importer
│   └── partner-integration.js            # Crisis line integration
│
├── 📁 integration/                       # Partner integration templates
│   ├── 988-lifeline/                     # Suicide prevention integration
│   ├── crisis-text-line/                 # Text line integration
│   ├── domestic-violence-hotline/        # DV hotline integration
│   └── local-resources/                  # Local partner templates
│
├── 📁 field-tools/                       # Resource mapping tools
│   ├── resource-survey/                  # Field data collection
│   ├── neighborhood-mapper/              # Geographic mapping
│   └── volunteer-recruiter/              # Mass recruitment tools
│
└── 📁 physical-infrastructure/           # Physical sanctuary tools
    ├── space-acquisition/                # Location securing scripts
    ├── mobile-unit-setup/                # Mobile deployment
    └── safety-protocols/                 # Physical safety procedures
    # 🌉 Bridge App - Immediate Crisis Connection

> **Connecting people to healing resources in under 60 seconds**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Deployment: 72 Hours](https://img.shields.io/badge/Deployment-72_Hours-urgent)](DEPLOYMENT.md)

## 🚨 The Problem

People in crisis face overwhelming barriers to getting help:
- Complex navigation through healthcare systems
- Long wait times when seconds matter  
- Technological barriers for vulnerable populations
- Isolation when connection is most needed

## 🎯 Our Solution

A **3-click bridge** that connects people to appropriate help in under 60 seconds:
- **No signups** - Immediate access
- **Anonymous** - Privacy protected
- **Location-aware** - Finds nearest resources
- **Multi-channel** - Phone, text, chat, in-person

## 🌟 Live Demos

- **Production**: https://bridge.empathyatlas.org
- **Staging**: https://staging.bridge.empathyatlas.org  
- **Local Development**: `npm start`

## 🚀 Quick Start

```bash
# Clone and run in 5 minutes
git clone https://github.com/empathy-atlas/bridge-app.git
cd bridge-app
npm install
npm start
User → 3-Option Landing → Needs Assessment → Resource Matching → Warm Handoff → Follow-up
npm run deploy:emergency --city=YourCity

## **📄 package.json**

```json
{
  "name": "bridge-app",
  "version": "1.0.0",
  "description": "Immediate crisis connection platform - 3 clicks to help",
  "homepage": "https://bridge.empathyatlas.org",
  "repository": {
    "type": "git",
    "url": "https://github.com/empathy-atlas/bridge-app.git"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "deploy:prod": "npm run build && vercel --prod",
    "deploy:staging": "npm run build && vercel",
    "deploy:emergency": "node scripts/emergency-build.js",
    "data:import": "node scripts/data-import.js",
    "partner:integrate": "node scripts/partner-integration.js",
    "field:survey": "node field-tools/resource-survey/launch.js",
    "volunteer:train": "node field-tools/volunteer-recruiter/train.js"
  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-scripts": "5.0.1",
    "firebase": "^10.0.0",
    "twilio": "^4.0.0",
    "@googlemaps/react-wrapper": "^1.0.0",
    "socket.io-client": "^4.7.0",
    "workbox-background-sync": "^6.0.0",
    "workbox-broadcast-update": "^6.0.0",
    "workbox-cacheable-response": "^6.0.0",
    "workbox-core": "^6.0.0",
    "workbox-expiration": "^6.0.0",
    "workbox-precaching": "^6.0.0",
    "workbox-range-requests": "^6.0.0",
    "workbox-routing": "^6.0.0",
    "workbox-strategies": "^6.0.0"
  },
  "devDependencies": {
    "vercel": "^28.0.0"
  },
  "browserslist": {
    "production": [
      ">0.2%",
      "not dead",
      "not op_mini all"
    ],
    "development": [
      "last 1 chrome version",
      "last 1 firefox version",
      "last 1 safari version"
    ]
  }
}# 🚀 Emergency Deployment Guide

## 72-Hour Deployment Protocol

### Phase 1: Foundation (Hours 0-24)
```bash
# 1. Clone and setup
git clone https://github.com/empathy-atlas/bridge-app.git
cd bridge-app
npm install

# 2. Configure environment
cp .env.example .env.local
# Edit with your Firebase and API keys

# 3. Deploy to staging
npm run deploy:staging
# 1. Add local resources
npm run data:import --city=YourCity

# 2. Integrate local partners  
npm run partner:integrate --city=YourCity

# 3. Train initial volunteers
npm run volunteer:train --city=YourCity --count=50
# 1. Go live
npm run deploy:prod

# 2. Monitor impact
# Check real-time dashboard at /admin

# 3. Scale based on demand
npm run fREACT_APP_FIREBASE_API_KEY=your_key
REACT_APP_FIREBASE_AUTH_DOMAIN=your_domain
REACT_APP_FIREBASE_PROJECT_ID=your_project
REACT_APP_TWILIO_ACCOUNT_SID=your_sid
REACT_APP_TWILIO_AUTH_TOKEN=your_token
REACT_APP_GOOGLE_MAPS_API_KEY=your_maps_keyield:survey --neighborhoods=all
npm run deploy:emergency --city=Chicago --neighborhoods=Englewood,WestGarfieldPark
import React from 'react';
import './EmergencyLanding.css';

const EmergencyLanding = ({ onFlowSelect }) => {
  return (
    <div className="emergency-landing">
      <div className="urgency-indicator">
        <div className="pulse-dot"></div>
        <span>Help available 24/7</span>
      </div>

      <div className="help-options">
        <button 
          className="help-option crisis" 
          onClick={() => onFlowSelect('crisis')}
        >
          <div className="icon">🚨</div>
          <h2>I'm in crisis or danger</h2>
          <p>Immediate safety and crisis support</p>
          <div className="response-time">
            <span>Response: &lt; 60 seconds</span>
          </div>
        </button>

        <button 
          className="help-option comfort" 
          onClick={() => onFlowSelect('comfort')}
        >
          <div className="icon">💔</div>
          <h2>I need someone to talk to</h2>
          <p>Compassionate listening and emotional support</p>
          <div className="response-time">
            <span>Response: &lt; 2 minutes</span>
          </div>
        </button>

        <button 
          className="help-option connection" 
          onClick={() => onFlowSelect('connection')}
        >
          <div className="icon">🌉</div>
          <h2>I feel alone and need community</h2>
          <p>Local connections and ongoing support</p>
          <div className="response-time">
            <span>Response: &lt; 24 hours</span>
          </div>
        </button>
      </div>

      <div className="safety-features">
        <h3>You're Safe Here</h3>
        <div className="features-grid">
          <div className="feature">
            <span>🔒</span>
            <span>Anonymous</span>
          </div>
          <div className="feature">
            <span>📞</span>
            <span>24/7 Available</span>
          </div>
          <div className="feature">
            <span>💝</span>
            <span>Compassionate</span>
          </div>
          <div className="feature">
            <span>🌍</span>
            <span>Local Help</span>
          </div>
        </div>
      </div>
    </div>
  );
};

export default EmergencyLanding;import { db } from './firebase';
import { collection, query, where, getDocs } from 'firebase/firestore';

class CrisisRouter {
  // Route user to appropriate help based on needs and location
  async routeToHelp(needType, userNeeds, location) {
    try {
      let resources;
      
      switch (needType) {
        case 'crisis':
          resources = await this.getCrisisResources(userNeeds, location);
          break;
        case 'comfort':
          resources = await this.getComfortResources(userNeeds, location);
          break;
        case 'connection':
          resources = await this.getConnectionResources(userNeeds, location);
          break;
        default:
          resources = await this.getFallbackResources(location);
      }

      return this.formatResponse(resources, userNeeds);
    } catch (error) {
      console.error('Routing error:', error);
      return this.getEmergencyFallback();
    }
  }

  async getCrisisResources(userNeeds, location) {
    const resources = [];
    
    // National crisis lines (always available)
    resources.push({
      type: 'national_crisis_line',
      name: '988 Suicide & Crisis Lifeline',
      contact: '988',
      availability: '24/7',
      languages: ['English', 'Spanish'],
      description: 'Immediate crisis support for suicide, mental health, substance use'
    });

    resources.push({
      type: 'crisis_text',
      name: 'Crisis Text Line',
      contact: 'Text HOME to 741741',
      availability: '24/7',
      description: 'Free crisis counseling via text message'
    });

    // Add location-specific crisis resources
    if (location) {
      const localResources = await this.getLocalCrisisResources(location);
      resources.push(...localResources);
    }

    // Add need-specific resources
    if (userNeeds.includes('violence') || userNeeds.includes('abuse')) {
      resources.push({
        type: 'domestic_violence',
        name: 'National Domestic Violence Hotline',
        contact: '1-800-799-7233',
        availability: '24/7',
        description: 'Support for domestic violence situations'
      });
    }

    return resources;
  }

  async getLocalCrisisResources(location) {
    const resourcesRef = collection(db, 'local_resources');
    const q = query(
      resourcesRef,
      where('type', '==', 'crisis'),
      where('city', '==', location.city),
      where('available', '==', true)
    );

    const snapshot = await getDocs(q);
    return snapshot.docs.map(doc => ({
      id: doc.id,
      ...doc.data()
    }));
  }

  formatResponse(resources, userNeeds) {
    return {
      immediate_actions: resources.slice(0, 3), // Top 3 most relevant
      additional_support: resources.slice(3),
      safety_check: this.generateSafetyPlan(userNeeds),
      follow_up: this.scheduleFollowUp()
    };
  }

  generateSafetyPlan(userNeeds) {
    const plan = [];
    
    if (userNeeds.includes('suicide') || userNeeds.includes('self-harm')) {
      plan.push('Remove access to means of self-harm');
      plan.push('Stay with a trusted person if possible');
      plan.push('Call 988 or go to nearest emergency room if in immediate danger');
    }

    if (userNeeds.includes('violence')) {
      plan.push('Identify safe places to go');
      plan.push('Keep phone charged and accessible');
      plan.push('Develop code word with trusted contacts');
    }

    return plan;
  }

  scheduleFollowUp() {
    return {
      check_in: new Date(Date.now() + 24 * 60 * 60 * 1000), // 24 hours
      method: 'anonymous_sms',
      message: 'How are you doing today? Reply with 1-10 (10=great)'
    };
  }

  getEmergencyFallback() {
    return {
      immediate_actions: [{
        type: 'emergency',
        name: 'Emergency Services',
        contact: '911',
        description: 'Call for immediate life-threatening emergencies'
      }],
      safety_check: ['Call 911 if in immediate danger'],
      follow_up: { check_in: null }
    };
  }
}

export default{
  "national_resources": [
    {
      "id": "988",
      "name": "988 Suicide & Crisis Lifeline",
      "contact": "988",
      "alternate_contacts": ["1-800-273-8255"],
      "languages": ["English", "Spanish", "150+ via interpreter"],
      "availability": "24/7/365",
      "services": ["Suicide prevention", "Mental health crisis", "Substance use support"],
      "access_methods": ["Phone", "Chat", "Text"],
      "response_time": "< 30 seconds",
      "privacy": "Anonymous",
      "cost": "Free"
    },
    {
      "id": "crisis-text",
      "name": "Crisis Text Line", 
      "contact": "Text HOME to 741741",
      "languages": ["English"],
      "availability": "24/7",
      "services": ["Crisis counseling via text", "Anxiety", "Depression", "Relationships"],
      "access_methods": ["Text only"],
      "response_time": "< 2 minutes",
      "privacy": "Anonymous",
      "cost": "Free"
    }
  ],
  "specialized_resources": [
    {
      "id": "domestic-violence",
      "name": "National Domestic Violence Hotline",
      "contact": "1-800-799-7233",
      "alternate_contacts": ["Text START to 88788"],
      "languages": ["English", "Spanish", "200+ via interpreter"],
      "availability": "24/7",
      "services": ["Domestic violence support", "Safety planning", "Shelter referrals"],
      "access_methods": ["Phone", "Chat", "Text"],
      "privacy": "Confidential",
      "cost": "Free"
    },
    {
      "id": "trevor-project",
      "name": "The Trevor Project",
      "contact": "1-866-488-7386",
      "alternate_contacts": ["Text START to 678678"],
      "languages": ["English"],
      "availability": "24/7",
      "services": ["LGBTQ+ crisis support", "Suicide prevention", "Coming out support"],
      "access_methods": ["Phone", "Chat", "Text"],
      "privacy": "Anonymous",
      "cost": "Free"
    }
  ]
} new CrisisRouter();
name: Emergency Deployment
on:
  workflow_dispatch:
    inputs:
      city:
        description: 'City to deploy to'
        required: true
        type: string
      neighborhoods:
        description: 'Specific neighborhoods'
        required: false
        type: string
      urgency:
        description: 'Deployment urgency'
        required: false
        type: choice
        options:
        - high
        - maximum

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    
    - name: Setup Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '18'
        cache: 'npm'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Import city data
      run: npm run data:import --city=${{ github.event.inputs.city }}
      
    - name: Build app
      run: npm run build
      
    - name: Deploy to production
      run: npm run deploy:prod
      env:
        VERCEL_TOKEN: ${{ secrets.VERCEL_TOKEN }}
        
    - name: Notify deployment
      run: |
        echo "🚀 Emergency deployment complete for ${{ github.event.inputs.city }}"
        echo "Neighborhoods: ${{ github.event.inputs.neighborhoods }}"
# 🤝 Contributing to Bridge App

## We Need Your Help

This is a humanitarian project - every contribution saves lives.

## How to Help

### 🚨 Immediate Needs (This Week)

**Developers:**
- React components for crisis flows
- Firebase security rules
- Offline PWA functionality
- Twilio SMS integration

**Crisis Professionals:**
- Safety protocol development
- Resource verification
- Volunteer training materials
- Crisis response scripts

**Community Organizers:**
- Local resource mapping
- Volunteer recruitment
- Community outreach
- Partnership development

**Designers:**
- High-stress UX optimization
- Accessibility improvements
- Multilingual interfaces
- Brand assets

### 📝 Contribution Process

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### 🏗️ Development Setup

```bash
# 1. Fork and clone
git clone https://github.com/YOUR_USERNAME/bridge-app.git
cd bridge-app

# 2. Install dependencies
npm install

# 3. Set up environment
cp .env.example .env.local
# Add your development API keys

# 4. Start development server
npm start

## **🚀 DEPLOYMENT COMMANDS**

```bash
# CREATE THE REPOSITORY
mkdir bridge-app
cd bridge-app
git init

# ADD ALL FILES
# (Copy all the file structures above)

# INITIAL COMMIT
git add .
git commit -m "🌉 Initial commit: Bridge App for immediate crisis connection"

# CREATE GITHUB REPO AND PUSH
gh repo create empathy-atlas/bridge-app --public --description "Immediate crisis connection platform - 3 clicks to help"
git push -u origin main

# DEPLOY IMMEDIATELY
npm run deploy:emergency --city=Chicago --neighborhoods=Englewood,WestGarfieldPark
