# Cloudshield SDK & Integration Guide

Official integration guide and SDK for validating Cloudshield software licenses.

## Quick Start

### 1. Verify License Key (Node.js / JavaScript)

```javascript
const response = await fetch('https://cloudshield-licensing-backend.onrender.com/api/verify-license), {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ licenseKey: 'YOUR_LICENSE_KEY' })
});

const data = await response.json();
if (data.valid) {
  console.log('License active until:', data.expiresAt);
} else {
  console.error('Invalid license');
}
