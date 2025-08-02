# Strategic Compass™ Web Application - Complete Specification

## Project Overview

**Application Name:** Strategic Compass™ by PromptReports.ai  
**Purpose:** Interactive 4D vendor positioning and strategic analysis platform  
**Target Users:** C-level executives, strategic planners, procurement teams  
**Technology Stack:** React + TypeScript, Tailwind CSS, Recharts, Framer Motion  

---

## Application Architecture

### Page Structure
```
/strategic-compass (Landing Page)
├── /dashboard (Main Analysis Interface)
├── /compare (Vendor Comparison Tool)
├── /methodology (Framework Explanation)
├── /request-analysis (Client Onboarding)
├── /sample-report (Report Preview)
└── /admin (Data Management - Demo)
```

### Component Hierarchy
```
App
├── Layout
│   ├── Header (Navigation)
│   ├── Footer
│   └── Sidebar (when applicable)
├── Pages
│   ├── LandingPage
│   ├── Dashboard
│   ├── ComparisonPage
│   ├── MethodologyPage
│   ├── RequestAnalysisPage
│   ├── SampleReportPage
│   └── AdminPage
└── Components
    ├── StrategicCompass (Main Visualization)
    ├── VendorCard
    ├── MetricChart
    ├── FilterPanel
    ├── ComparisonTable
    └── FormComponents
```

---

## Sample Data Structure

### Vendor Data Model
```json
{
  "id": "vendor_001",
  "name": "TechFlow Solutions",
  "logo": "/logos/techflow.png",
  "description": "Enterprise workflow automation platform",
  "founded": 2008,
  "employees": 2500,
  "headquarters": "San Francisco, CA",
  "website": "techflow.com",
  "industry": "Enterprise Software",
  "companySize": "Growth",
  "strategicMetrics": {
    "innovationIndex": 0.89,
    "marketImpact": 0.92,
    "executionReliability": 0.87,
    "futureReadiness": 0.91
  },
  "strategicPosition": "market_pioneers",
  "strategicMomentum": 0.12,
  "marketMetrics": {
    "marketShare": 18.5,
    "revenueGrowth": 28.3,
    "customerCount": 1250,
    "revenue": 450000000
  },
  "competitiveProfile": {
    "advantages": [
      "Industry-leading AI integration capabilities",
      "Strongest partner ecosystem with 200+ integrations",
      "Highest customer satisfaction scores (4.7/5)",
      "Fastest time-to-value implementation"
    ],
    "vulnerabilities": [
      "Premium pricing limits SMB market penetration",
      "Complex feature set requires extensive training"
    ],
    "opportunities": [
      "Expanding international presence in APAC",
      "Growing demand for AI-powered automation",
      "Potential for vertical market specialization"
    ],
    "threats": [
      "Increasing competition from cloud-native vendors",
      "Economic downturn affecting enterprise spending"
    ]
  },
  "threeYearOutlook": "Strong growth trajectory with market leadership consolidation",
  "buyerGuidance": {
    "bestFor": "Large enterprises requiring comprehensive automation",
    "considerations": "Ensure adequate training budget and change management",
    "implementation": "12-18 months for full deployment"
  }
}
```

### Complete Vendor Dataset (20 Companies)

#### Market Pioneers
1. **TechFlow Solutions** - Innovation: 0.89, Market: 0.92, Execution: 0.87, Future: 0.91
2. **DataVantage Corp** - Innovation: 0.85, Market: 0.88, Execution: 0.91, Future: 0.83

#### Innovation Leaders  
3. **NextGen Systems** - Innovation: 0.92, Market: 0.65, Execution: 0.74, Future: 0.89
4. **FutureStack** - Innovation: 0.87, Market: 0.58, Execution: 0.69, Future: 0.91

#### Execution Champions
5. **CloudMaster Systems** - Innovation: 0.58, Market: 0.84, Execution: 0.93, Future: 0.67
6. **ReliableCore** - Innovation: 0.52, Market: 0.79, Execution: 0.95, Future: 0.61

#### Market Builders
7. **ScaleWorx** - Innovation: 0.74, Market: 0.71, Execution: 0.78, Future: 0.76
8. **DigitalEdge** - Innovation: 0.69, Market: 0.73, Execution: 0.81, Future: 0.72

#### Emerging Disruptors
9. **InnovatePro** - Innovation: 0.81, Market: 0.45, Execution: 0.63, Future: 0.85
10. **DisruptTech** - Innovation: 0.76, Market: 0.38, Execution: 0.58, Future: 0.88

#### Niche Specialists
11. **SpecialtyOps** - Innovation: 0.48, Market: 0.42, Execution: 0.76, Future: 0.51
12. **FocusedSolutions** - Innovation: 0.45, Market: 0.39, Execution: 0.72, Future: 0.48

#### Additional Vendors
13. **SmartOps Pro** - Innovation: 0.67, Market: 0.61, Execution: 0.79, Future: 0.64
14. **VelocityTech** - Innovation: 0.73, Market: 0.56, Execution: 0.68, Future: 0.78
15. **PowerScale** - Innovation: 0.55, Market: 0.67, Execution: 0.84, Future: 0.59
16. **FlexiCore** - Innovation: 0.61, Market: 0.49, Execution: 0.77, Future: 0.66
17. **UltraSync** - Innovation: 0.79, Market: 0.53, Execution: 0.71, Future: 0.82
18. **ProActive Systems** - Innovation: 0.58, Market: 0.72, Execution: 0.86, Future: 0.63
19. **CoreLogic Enterprise** - Innovation: 0.64, Market: 0.68, Execution: 0.75, Future: 0.69
20. **AdaptiveFlow** - Innovation: 0.71, Market: 0.44, Execution: 0.65, Future: 0.74

---

## User Interface Specifications

### Design System

#### Color Palette
```css
Primary Colors:
- Brand Blue: #1E40AF (rgb(30, 64, 175))
- Brand Purple: #7C3AED (rgb(124, 58, 237))
- Accent Gold: #F59E0B (rgb(245, 158, 11))

Strategic Position Colors:
- Market Pioneers: #3B82F6 (Blue)
- Innovation Leaders: #10B981 (Green)
- Execution Champions: #F97316 (Orange)
- Market Builders: #8B5CF6 (Purple)
- Emerging Disruptors: #EF4444 (Red)
- Niche Specialists: #6B7280 (Gray)

Neutral Colors:
- Background: #0F172A (Dark Navy)
- Surface: #1E293B (Slate)
- Text Primary: #F8FAFC (White)
- Text Secondary: #CBD5E1 (Light Gray)
```

#### Typography
```css
Headings: 'Inter', sans-serif
- H1: 48px, font-weight: 700
- H2: 36px, font-weight: 600
- H3: 24px, font-weight: 600
- H4: 20px, font-weight: 500

Body: 'Inter', sans-serif
- Large: 18px, font-weight: 400
- Regular: 16px, font-weight: 400
- Small: 14px, font-weight: 400
```

#### Spacing System
```css
Scale: 4px base unit
- xs: 4px
- sm: 8px
- md: 16px
- lg: 24px
- xl: 32px
- 2xl: 48px
- 3xl: 64px
```

### Layout Specifications

#### Header Navigation
```
Logo (PromptReports.ai) | Strategic Compass™ | Dashboard | Compare | Methodology | Request Analysis
```

#### Footer
```
© 2024 PromptReports.ai | Privacy Policy | Terms of Service | Contact
```

---

## Page-by-Page Specifications

### 1. Landing Page (/strategic-compass)

#### Hero Section
- **Heading:** "Strategic Compass™ Analysis"
- **Subheading:** "Revolutionary 4D Vendor Positioning Framework"
- **Description:** "Move beyond traditional quadrants. Our proprietary Strategic Compass provides multi-dimensional vendor analysis with predictive intelligence and strategic momentum tracking."
- **Primary CTA:** "Explore Live Demo" → /dashboard
- **Secondary CTA:** "Request Analysis" → /request-analysis
- **Background:** Animated compass with subtle rotation

#### Benefits Section
Three columns with icons and descriptions:
1. **Multi-Dimensional Analysis** - "4D positioning across Innovation, Market Impact, Execution, and Future Readiness"
2. **Strategic Momentum** - "Track vendor trajectory and competitive dynamics over time"
3. **Executive Intelligence** - "C-level insights with actionable strategic recommendations"

#### Interactive Preview
- Mini Strategic Compass (400px x 400px)
- 8-10 sample vendors plotted
- Hover effects showing vendor names
- "Explore Full Analysis" button

#### Statistics
- "50+ Vendors Analyzed"
- "95% Decision Accuracy" 
- "30+ Industries Covered"
- "$2.5B+ in Strategic Decisions Supported"

#### Client Testimonials
Rotating cards with fictional testimonials:
- "Strategic Compass transformed our vendor selection process" - Jane Smith, CTO, GlobalTech
- "The 4D analysis revealed competitive insights we never saw before" - Mike Johnson, VP Strategy, InnovateCorp

### 2. Dashboard (/dashboard)

#### Layout Structure
```
Header Navigation
├── Filter Panel (Left Sidebar - 300px)
├── Main Compass (Center - 600px x 600px)
├── Vendor Details Panel (Right Sidebar - 350px)
└── Market Insights (Bottom Panel - Full Width)
```

#### Strategic Compass Visualization
- **Canvas Size:** 600px x 600px
- **Axes:** Four labeled axes from center to edge
  - Top: Innovation Index (0.0 to 1.0)
  - Right: Market Impact (0.0 to 1.0)
  - Bottom: Execution Reliability (0.0 to 1.0)
  - Left: Future Readiness (0.0 to 1.0)
- **Vendor Nodes:**
  - Circular nodes (20px diameter)
  - Company logo in center
  - Color-coded by strategic position
  - Size varies by market impact (15px to 30px)
  - Hover effect: Increase size by 20%, show tooltip
  - Click: Open vendor details panel

#### Zone Overlays
Six strategic position zones with transparent overlays:
- **Market Pioneers:** Top-right quadrant (blue, 20% opacity)
- **Innovation Leaders:** Top-left quadrant (green, 20% opacity)
- **Execution Champions:** Bottom-right quadrant (orange, 20% opacity)
- **Market Builders:** Center area (purple, 20% opacity)
- **Emerging Disruptors:** Left-center (red, 20% opacity)
- **Niche Specialists:** Bottom-left (gray, 20% opacity)

#### Filter Panel Controls
- **Industry Filter:** Dropdown with options
- **Company Size:** Checkboxes (Startup, Growth, Enterprise)
- **Strategic Position:** Toggle buttons for each position
- **Metric Sliders:** 
  - Innovation Index (0.0 - 1.0)
  - Market Impact (0.0 - 1.0)
  - Revenue Range ($1M - $10B)
- **Search:** Text input for vendor name
- **Reset Filters:** Clear all filters button

#### Vendor Details Panel
Appears when vendor is clicked:
- Company logo and name
- Strategic position badge
- Description
- 4D metric scores with progress bars
- Key statistics (revenue, growth, employees)
- Competitive advantages (top 3)
- Strategic vulnerabilities (top 2)
- 3-year outlook indicator
- "Add to Comparison" button
- "View Full Profile" link

#### Market Insights Panel
Bottom section with key metrics:
- **Market Overview:** Total vendors, market size, growth rate
- **Strategic Momentum Leaders:** Top 5 vendors with highest momentum
- **Market Trends:** Key industry trends affecting positioning
- **Risk Alerts:** Vendors with declining positions

### 3. Comparison Page (/compare)

#### Vendor Selection
- Search and add vendors (up to 4)
- Selected vendor cards with remove option
- "Start Comparison" button

#### Comparison Interface
Side-by-side cards for each selected vendor:
- Company information
- Strategic position
- 4D metrics radar chart
- Key statistics table
- SWOT analysis
- Strategic recommendations

#### Detailed Analysis
- Head-to-head metric comparison
- Historical trend charts
- Competitive advantages matrix
- Risk assessment comparison

#### Export Options
- Generate PDF comparison report
- Export data to CSV
- Email comparison
- Save comparison

### 4. Methodology Page (/methodology)

#### Framework Overview
- Strategic Compass explanation
- 4D positioning benefits
- Algorithm overview

#### Dimension Explanations
Detailed breakdown of each dimension:

**Innovation Index (25% weight)**
- R&D investment ratio (30%)
- Patent velocity (25%)
- Technology leadership (20%)
- Product innovation frequency (15%)
- Research partnerships (10%)

**Market Impact (25% weight)**
- Market share (35%)
- Customer growth (25%)
- Revenue influence (20%)
- Industry recognition (20%)

**Execution Reliability (25% weight)**
- Customer satisfaction (30%)
- Delivery performance (25%)
- Operational efficiency (20%)
- Financial stability (25%)

**Future Readiness (25% weight)**
- Strategic vision (30%)
- Technology investment (25%)
- Adaptability (20%)
- Talent acquisition (25%)

#### Data Sources
- Primary data collection methods
- Third-party data providers
- Validation processes
- Update frequency

#### Accuracy & Validation
- Algorithm accuracy metrics
- Peer review process
- Continuous improvement
- Industry benchmarks

### 5. Request Analysis Page (/request-analysis)

#### Multi-Step Form

**Step 1: Company Information**
```
Company Name* (text input)
Industry* (dropdown: Enterprise Software, Cloud Services, Cybersecurity, Data Analytics, etc.)
Company Size* (radio: Startup <100, Growth 100-1000, Enterprise >1000)
Contact Name* (text input)
Email* (email input with validation)
Phone (phone input)
```

**Step 2: Analysis Requirements**
```
Market/Category to Analyze* (text input with suggestions)
Specific Vendors to Include (multi-select with search)
Analysis Depth* (radio: Basic $5K, Standard $15K, Comprehensive $35K)
Timeline* (dropdown: 2 weeks, 4 weeks, 8 weeks, Custom)
Geographic Focus (checkboxes: North America, Europe, APAC, Global)
```

**Step 3: Use Case & Requirements**
```
Primary Use Case* (checkboxes):
- Vendor Selection
- Market Entry Strategy  
- Competitive Intelligence
- Investment Planning
- Strategic Planning

Key Questions to Address (textarea)
Stakeholders Involved (checkboxes: IT, Procurement, Finance, Executive)
Decision Timeline (dropdown)
Budget Range (dropdown)
```

**Step 4: Custom Requirements**
```
Custom Metrics Needed (textarea)
Industry-Specific Considerations (textarea)
Compliance Requirements (checkboxes)
Integration Requirements (textarea)
Special Analysis Requests (textarea)
File Upload (for requirements documents)
```

**Step 5: Review & Submit**
```
Request Summary (auto-generated)
Estimated Timeline (calculated)
Investment Required (calculated)
Terms & Conditions (checkbox)
Subscribe to Updates (checkbox)
```

#### Form Features
- Real-time validation
- Progress indicator (5 steps)
- Save draft functionality
- Auto-save every 30 seconds
- Conditional logic (show/hide fields based on selections)
- File upload for documents
- Calendar integration for consultation scheduling

### 6. Sample Report Page (/sample-report)

#### Report Preview
Interactive preview of Strategic Compass report:
- Executive summary
- Strategic Compass visualization
- Vendor analysis
- Market insights
- Strategic recommendations

#### Download Options
- Full PDF Report (25 pages)
- Executive Summary (5 pages)
- Data Export (Excel)
- PowerPoint Template

#### Customization Preview
- White-label options
- Custom branding
- Format preferences
- Delivery methods

### 7. Admin Page (/admin)

#### Vendor Management
- Add/edit vendor profiles
- Update metrics and scores
- Upload vendor logos
- Bulk data import/export

#### Visualization Controls
- Real-time compass updates
- Metric adjustment sliders
- Position recalculation
- Data refresh

#### Report Management
- Generate custom reports
- Template management
- Automated scheduling
- Client report history

---

## Technical Requirements

### State Management
```typescript
// Global State Structure
interface AppState {
  vendors: Vendor[];
  filters: FilterState;
  selectedVendors: string[];
  comparisonVendors: Vendor[];
  user: UserState;
  ui: UIState;
}

interface FilterState {
  industry: string[];
  companySize: string[];
  strategicPosition: string[];
  metrics: {
    innovationMin: number;
    innovationMax: number;
    marketImpactMin: number;
    marketImpactMax: number;
  };
  search: string;
}
```

### API Endpoints (Mock/Demo)
```typescript
// Vendor Data
GET /api/vendors - Get all vendors
GET /api/vendors/:id - Get specific vendor
POST /api/vendors - Create vendor (admin)
PUT /api/vendors/:id - Update vendor (admin)

// Analysis Requests
POST /api/analysis-requests - Submit analysis request
GET /api/analysis-requests/:id - Get request status

// Reports
GET /api/reports/sample - Get sample report
POST /api/reports/generate - Generate custom report
```

### Performance Requirements
- Initial page load: <3 seconds
- Compass visualization: <1 second render
- Filter updates: <500ms
- Smooth 60fps animations
- Mobile responsive (<768px breakpoint)

### Accessibility
- WCAG 2.1 AA compliance
- Keyboard navigation support
- Screen reader compatibility
- High contrast mode support
- Focus indicators on all interactive elements

---

## Content Requirements

### Copy Guidelines
- **Tone:** Professional, authoritative, yet accessible
- **Voice:** Strategic, data-driven, executive-focused
- **Style:** Clear, concise, jargon-free where possible
- **Length:** Headlines 5-8 words, descriptions 20-30 words

### SEO Requirements
- **Title Tags:** Include "Strategic Compass", "Vendor Analysis", "PromptReports.ai"
- **Meta Descriptions:** Focus on benefits and differentiation
- **Headers:** H1 for page titles, H2 for major sections, H3 for subsections
- **Alt Text:** Descriptive alt text for all images and charts

### Legal Requirements
- Copyright notice: "© 2024 PromptReports.ai. All rights reserved."
- Trademark notice: "Strategic Compass™ is a trademark of PromptReports.ai"
- Privacy policy link in footer
- Terms of service link in footer

---

## Testing Requirements

### Functional Testing
- All form validations work correctly
- Compass visualization responds to filters
- Vendor selection and comparison functions
- Export functionality works
- Mobile responsive design

### Performance Testing
- Page load times under 3 seconds
- Smooth animations at 60fps
- Efficient re-renders
- Memory usage optimization

### Accessibility Testing
- Screen reader compatibility
- Keyboard navigation
- Color contrast ratios
- Focus management

### Browser Compatibility
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS Safari, Chrome Mobile)

---

## Deployment Specifications

### Build Configuration
```json
{
  "name": "strategic-compass-app",
  "version": "1.0.0",
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint",
    "type-check": "tsc --noEmit"
  },
  "dependencies": {
    "react": "^18.0.0",
    "typescript": "^5.0.0",
    "tailwindcss": "^3.0.0",
    "framer-motion": "^10.0.0",
    "recharts": "^2.0.0",
    "react-hook-form": "^7.0.0",
    "zustand": "^4.0.0"
  }
}
```

### Environment Variables
```
NEXT_PUBLIC_APP_URL=https://promptreports.ai
NEXT_PUBLIC_API_BASE_URL=/api
NEXT_PUBLIC_ANALYTICS_ID=your-analytics-id
```

### File Structure
```
src/
├── components/
│   ├── ui/
│   ├── charts/
│   ├── forms/
│   └── layout/
├── pages/
├── hooks/
├── utils/
├── types/
├── data/
└── styles/
```

This specification provides everything needed for lovable.dev to build a complete, production-ready Strategic Compass application.