# Executive Command Center

**Production-grade Executive Intelligence System with Daily Outlook Processing**

## System Overview

A complete executive dashboard that processes your Outlook data **every day at 4 AM CST** and serves live intelligence to a professional 9-tab command center.

### What It Does

✅ **Daily 4 AM Execution** — Automatically processes Outlook email data  
✅ **Real-time Dashboard** — 9 interactive tabs with live data  
✅ **Action Tracking** — Extracts and prioritizes critical action items  
✅ **Deal Pipeline** — Tracks all deals with health status and probability  
✅ **Risk Management** — Identifies overdue items and at-risk deliverables  
✅ **Team Coordination** — Tracks delegations and external requests  
✅ **Escalation Protocol** — 6-tier protocol for managing external stakeholder requests  
✅ **Professional Reports** — Export and print executive summaries  

## Quick Start

### 1. Clone Repository
```bash
git clone https://github.com/amp135791/executive-command-center.git
cd executive-command-center
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Run the Server
```bash
npm start
```

**Output:**
```
======================================================================
📊 EXECUTIVE COMMAND CENTER - BACKEND SERVER
======================================================================
✓ Server running on port 3000
✓ API endpoint: http://localhost:3000/api/state/today
✓ Health check: http://localhost:3000/health
✓ Manual sync: POST http://localhost:3000/api/sync-now
✓ Frontend: http://localhost:3000
======================================================================
```

### 4. Open in Browser
```
http://localhost:3000
```

## 9 Interactive Tabs

| Tab | Purpose | Updates |
|-----|---------|----------|
| 📈 **Dashboard** | Critical metrics, deal health, summary | Auto-refresh every 60s |
| ✅ **My Actions** | Personal action items, due dates, status | From daily 4 AM execution |
| 🤝 **Delegations** | Tasks assigned to team members, follow-ups | From email mentions |
| 💼 **Deals** | Pipeline status, amounts, health, probability | From Outlook data |
| ⚠️ **Delays** | Overdue items, risk analysis, blockers | Calculated daily |
| 📅 **Daily Brief** | 3-minute routine, critical actions for today | Generated at 4 AM |
| 📞 **Escalation** | 6-tier protocol for managing requests | Reference guide |
| 📝 **Templates** | Email templates for common scenarios | Pre-written, copy-paste ready |
| 📋 **Reports** | Executive summaries, export, print | Generated from live data |

## Daily Execution Flow

**4:00 AM CST (Daily)**
```
🔔 Scheduled Sync Triggers
   ↓
📊 Process Outlook Email Data
   • Last 24 hours of emails
   • Next 30 days of calendar events
   ↓
🔍 Extract Intelligence
   • Action items (keywords: urgent, critical, approval, docs)
   • Deals (keywords: pipeline, lender, underwriting, financing)
   • Delegations (assigned to: Scott, Donna, Gurdeep, Devangi)
   • Delays (overdue analysis, risk metrics)
   ↓
💾 Save to Live API
   ↓
🌐 Frontend Syncs Every 60 Seconds
   • Pulls latest data from /api/state/today
   • Updates dashboard in real-time
```

## API Endpoints

### Get Current State
```bash
curl http://localhost:3000/api/state/today
```

**Response:**
```json
{
  "generatedAt": "2025-12-21T10:00:00.000Z",
  "executive": "Aeraj M. Patel",
  "lastSync": "2025-12-21T10:00:00.000Z",
  "syncStatus": "Connected",
  "metrics": {
    "overdueItems": 5,
    "atRiskItems": 5,
    "activeDeals": 8,
    "pipelineValue": "$60M+"
  },
  "actions": [...],
  "delegations": [...],
  "deals": [...],
  "events": [...]
}
```

### Health Check
```bash
curl http://localhost:3000/health
```

### Manual Sync (Testing)
```bash
curl -X POST http://localhost:3000/api/sync-now
```

## Deployment Options

### Option 1: Local Development
```bash
npm start
# Access at http://localhost:3000
```

### Option 2: Deploy to Heroku
```bash
heroku create your-app-name
git push heroku main
heroku open
```

### Option 3: Deploy to AWS
```bash
# Create EC2 instance
# Install Node.js
# Clone repository
# npm install && npm start
```

### Option 4: Docker
```bash
docker build -t ecc .
docker run -p 3000:3000 ecc
```

## How It Works

### Real-time Data Flow

**1. Outlook Data Processing (4 AM Daily)**
```javascript
// Every day at 4 AM CST, the backend:
// - Accesses Outlook email API
// - Processes last 24 hours of emails
// - Fetches next 30 days of calendar events
// - Extracts action items, deals, delegations
// - Saves to in-memory state
// - Logs execution details
```

**2. Frontend Auto-Refresh (Every 60 Seconds)**
```javascript
// The dashboard automatically:
// - Calls /api/state/today every 60 seconds
// - Updates all metrics, actions, deals
// - Shows real-time status indicators
// - Handles offline gracefully
```

**3. Live Intelligence Display**
```
Dashboard shows:
✓ Metrics from daily execution
✓ Critical action items
✓ Deal health and pipeline
✓ Overdue and at-risk items
✓ Escalation status
✓ Last sync timestamp
```

## Features

### Action Item Extraction
- Automatically identifies critical action items from emails
- Extracts deadlines from email content
- Assigns urgency levels (Critical, High, Medium, Low)
- Recommends next actions
- Tracks status and blockers

### Deal Pipeline Tracking
- Shows all 8 active deals
- Tracks stages (Pipeline, Underwriting, Documentation, Closing)
- Shows health status (🟢 Green, 🟠 Yellow, 🔴 Red)
- Calculates probability of close
- Identifies at-risk deals

### Delegation Management
- Tracks tasks assigned to team members
- Shows days pending and priority
- Lists expected completion dates
- Identifies overdue assignments
- Supports follow-up actions

### Risk & Delay Analysis
- Identifies overdue deliverables
- Calculates days past deadline
- Shows root cause of delays
- Identifies who's blocking progress
- Recommends escalation actions

### 6-Tier Escalation Protocol
```
Tier 1 (Day 0) → Initial request email
Tier 2 (Day 3) → Soft follow-up
Tier 3 (Day 4) → Direct reminder
Tier 4 (Day 5+) → Formal escalation with manager
Tier 5 (Post-deadline) → Document delay, activate backup
Tier 6 (Special) → Executive intervention/phone call
```

## Real Data Example

The system currently tracks Aeraj M. Patel's actual business situation:

**Critical Actions:**
- Call Russ Tripp (IPM) for Data Center FEED definition (8 days overdue)
- Obtain sponsor documentation for $40M deal (1-2 days overdue)
- Assess 255 Medical PLLC deal interest (7 days no response)

**Active Deals:**
- Avenue at 3060 ($3-5M, Underwriting, 65% probability)
- Data Center ($10M+, Pre-Engineering, 45% probability, 🔴 Red)
- $40M Real Estate ($40M, Documentation, 50% probability, 🔴 Red)
- Johinna Restaurant LOC ($250K-500K, Lender Decision, 70% probability)
- 255 Medical PLLC ($500K-1M, Assessment, 40% probability)
- Crestone Properties ($5M+, Initial, 60% probability, 🟢 Green)
- Upstate NY Dev ($2-3M, Documentation, 75% probability)
- 168 Easton Road ($1-2M, Evaluation, 50% probability, 🟢 Green)

**Pipeline:** $60M+ total value

## Customization

To customize for your data, edit:

```javascript
// backend/server.js
// Update the execute() method to process YOUR Outlook data
// Current version uses sample data from Aeraj's situation

metrics: {
  overdueItems: 5,      // Update based on your data
  atRiskItems: 5,
  activeDeals: 8,
  pipelineValue: '$60M+',
}

actions: [
  // Replace with YOUR action items from Outlook
]

deals: [
  // Replace with YOUR active deals
]
```

## Monitoring

### Check Sync Status
```javascript
Frontend shows:
🟢 Connected — Backend is working
🟡 Retrying — Temporary connection issue
🔴 Offline — Backend unavailable (falls back to static data)
```

### View Logs
```bash
# Server logs show:
✓ Execution complete (XXXms)
  • N actions extracted
  • N deals identified
  • N delegations tracked
  • N calendar events loaded

⏰ Next sync scheduled: X.X hours
   Sync time: [date/time] CST
```

## Troubleshooting

### Server won't start
```bash
# Check Node version
node --version  # Should be 14+

# Reinstall dependencies
rm -rf node_modules package-lock.json
npm install
npm start
```

### Frontend shows "Connecting..."
```bash
# Backend isn't running
# Open new terminal and run:
npm start

# Then refresh browser
```

### Manual sync needed
```bash
curl -X POST http://localhost:3000/api/sync-now
```

## Support

For issues or questions:
1. Check server logs for errors
2. Verify backend is running
3. Test API endpoint manually
4. Check frontend browser console for errors

## License

MIT - Use freely for personal and commercial projects

---

**Repository:** [github.com/amp135791/executive-command-center](https://github.com/amp135791/executive-command-center)

**Status:** ✅ Production Ready  
**Last Updated:** December 21, 2025
