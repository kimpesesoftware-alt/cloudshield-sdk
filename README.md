# Cloudshield SDK & Integration Guide

Official integration guide and SDK for validating Cloudshield software licenses.

## Quick Start

### 1. Verify User Access (Node.js / JavaScript)

```javascript
const response = await fetch('[https://cloudshield-licensing-backend.onrender.com/check-access](https://cloudshield-licensing-backend.onrender.com/check-access)', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ githubUser: 'YOUR_GITHUB_USERNAME' })
});

const data = await response.json();
console.log(data);
