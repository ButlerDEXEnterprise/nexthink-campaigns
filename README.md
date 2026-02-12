# Nexthink Campaigns Library

A collection of ready-to-deploy Campaigns for Nexthink Infinity — gather feedback, communicate with users, and drive self-service IT actions.

> **Part of [Butler DEX Enterprise](https://github.com/ButlerDEXEnterprise)** — At Your Enterprise's Service.

---

## 📋 Available Campaigns

| Campaign | Category | Description | Tier |
|---|---|---|---|
| [DEX Satisfaction Survey](#dex-satisfaction-survey) | Feedback | Measures overall digital experience satisfaction with a quick pulse check | 🟢 Free |
| [Reboot Nudge](#reboot-nudge) | Compliance | Friendly reminder for users who haven't rebooted in X days with a one-click reboot option | 🟢 Free |
| [Software Request](#software-request) | Self-Service | Lets users request software through a structured campaign instead of a ticket | 🟢 Free |
| [VDI Experience Pulse](#vdi-experience-pulse) | Feedback | Targeted survey for VDI/virtual desktop users to capture pain points | 🔵 Premium |
| [Change Readiness Check](#change-readiness-check) | Communication | Pre-migration or pre-upgrade campaign to assess user readiness and communicate timelines | 🔵 Premium |

<!-- Add rows as you publish more campaigns -->

---

## 🟢 Free Campaigns

### DEX Satisfaction Survey

**What it does:** A short, non-intrusive survey that asks users to rate their overall digital experience on a 1-5 scale with an optional comment field.

**Why it matters:** You can't improve what you don't measure. This gives you a baseline DEX score to track over time and identify problem areas before they become ticket storms.

**Use case:** Run monthly or quarterly to track trends. Pair with NQL queries to correlate satisfaction with device health metrics.

<details>
<summary>📥 Setup Instructions</summary>

1. Import the campaign definition into your Nexthink instance
2. Customize the question text and branding for your organization
3. Configure targeting (all users, specific departments, etc.)
4. Set the schedule and frequency
5. Test on a pilot group before broad deployment

</details>

---

### Reboot Nudge

**What it does:** Sends a friendly, branded notification to users whose devices haven't rebooted in X days. Includes a one-click "Reboot Now" or "Remind Me Later" option.

**Why it matters:** Forced reboots create frustration and lost work. A well-designed campaign gives users agency while still driving compliance. Most users will reboot voluntarily when asked nicely.

**Estimated impact:** Reduces forced reboot incidents and associated helpdesk calls. Pairs well with the [Reboot Reminder Workflow](https://github.com/ButlerDEXEnterprise/nexthink-workflows).

<details>
<summary>📥 Setup Instructions</summary>

1. Import the campaign definition
2. Set the uptime threshold that triggers the campaign (default: 7 days)
3. Customize the messaging and branding
4. Configure the reboot action and snooze options
5. Deploy to target scope

</details>

---

### Software Request

**What it does:** Provides users with a structured form to request software. Captures the application name, business justification, and urgency — then routes it to the appropriate team.

**Why it matters:** Software requests via email or generic tickets lack structure and slow down fulfillment. A campaign-based approach standardizes the intake, captures the data you need, and gives users a better experience.

**Use case:** Replace ad-hoc software request processes with a consistent, trackable workflow.

<details>
<summary>📥 Setup Instructions</summary>

1. Import the campaign definition
2. Customize the form fields for your approval process
3. Configure the routing (ServiceNow, Jira, email, etc.)
4. Test the end-to-end flow with a pilot group
5. Deploy organization-wide

</details>

---

## 🔵 Premium Campaigns

### VDI Experience Pulse

**What it does:** A targeted survey designed specifically for VDI and virtual desktop users. Captures latency perception, app performance, audio/video quality, and overall satisfaction with the virtual workspace.

**Why it matters:** VDI users have unique pain points that generic surveys miss. This campaign captures the specific metrics that matter for virtual environments — helping you prioritize infrastructure investments where they'll have the most impact.

**Estimated impact:** Identifies VDI performance issues that correlate with productivity loss and support ticket volume.

> **This is a premium solution.** The campaign design and approach are documented here, but the production implementation is available through a consulting engagement. [Contact us](https://github.com/ButlerDEXEnterprise) to discuss your environment.

---

### Change Readiness Check

**What it does:** A pre-migration or pre-upgrade campaign that assesses user readiness, communicates timelines, and collects scheduling preferences. Captures whether users have saved their work, closed critical apps, and are ready for the change.

**Why it matters:** Migrations and upgrades fail when users aren't prepared. This campaign reduces failed deployments, after-hours support calls, and user frustration by ensuring everyone is informed and ready.

**Estimated savings:** Reduces failed deployment attempts and associated rollback costs.

> **This is a premium solution.** [Contact us](https://github.com/ButlerDEXEnterprise) to discuss your environment.

---

## 📁 Repository Structure

```
nexthink-campaigns/
├── README.md
├── LICENSE
├── free/
│   ├── dex-satisfaction-survey/
│   │   ├── README.md
│   │   └── campaign-definition.json
│   ├── reboot-nudge/
│   │   ├── README.md
│   │   └── campaign-definition.json
│   └── software-request/
│       ├── README.md
│       └── campaign-definition.json
└── premium/
    ├── vdi-experience-pulse/
    │   └── README.md
    └── change-readiness-check/
        └── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Nexthink Infinity with Campaigns enabled
- Appropriate permissions to create and manage Campaigns
- API access for programmatic triggering (optional — see [NexthinkAPI PowerShell module](https://github.com/NexthinkGuru/NexthinkAPI))

### Import a Campaign
Each free campaign folder contains everything you need:
1. Review the README in the specific folder
2. Import the campaign definition into your Nexthink instance
3. Customize messaging, branding, and targeting for your environment
4. Test on a small user group first
5. Scale to your full environment

---

## ⚠️ Disclaimer

These campaigns are provided as-is. Always test in a non-production environment first. The author is not responsible for any unintended effects. This is not affiliated with or supported by Nexthink S.A.

---

## 📄 License

MIT License — free to use, modify, and contribute.
