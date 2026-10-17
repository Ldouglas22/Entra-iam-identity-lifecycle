#entra-healthcare-iam-portfolio
├── 01-lifecycle-management/ (Dynamic group rules, workflow JSONs)
├── 02-rbac-least-privilege/ (App role manifests, PIM configuration guide)
├── 03-access-monitoring/ (KQL query scripts for Log Analytics)
└── README.md
02-rbac-least-privilege
{
  "appName": "Enterprise EMR Portal (Simulation)",
  "complianceContext": "HIPAA Least Privilege Enforcement",
  "appRoles": [
    {
      "displayName": "Clinical Reader",
      "value": "Clinical.Read",
      "targetScope": "Patient Vitals & Medical Notes"
    },
    {
      "displayName": "Billing Administrator",
      "value": "Billing.Manage",
      "targetScope": "Revenue Ledger & Claims Processing"
    },
    {
      "displayName": "Emergency Override",
      "value": "System.BreakGlass",
      "targetScope": "Full System Emergency Access (Time-Bound)"
    }
  ]
}
