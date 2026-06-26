# ZIP API

## Publisher: Gineesoft

## Overview

ZIP API by Gineesoft enables Power Automate users to work with ZIP files directly in their flows — no coding required. With 4 simple operations, you can create ZIP archives, extract ZIP files, and work with password protected ZIPs using AES-256 encryption.

## Prerequisites

To use this connector, you need a free ZIP API subscription key:

1. Go to [https://gineesoft.com](https://gineesoft.com)
2. Sign up for a free account
3. Navigate to your dashboard
4. Copy your API subscription key
5. Use this key when setting up the connector in Power Automate

## Supported Operations

| Operation | Description |
|---|---|
| **ZipFunction** | Create a ZIP archive from one or more files |
| **UnzipFunction** | Extract all files from a ZIP archive |
| **ZipWithPassword** | Create a password protected ZIP archive (AES-256) |
| **UnzipWithPassword** | Extract files from a password protected ZIP archive |

## Getting Started

### Step 1: Get Your Free Subscription Key
1. Visit [https://gineesoft.com](https://gineesoft.com)
2. Click **Sign Up** and create a free account
3. Go to your **Dashboard**
4. Copy your **API Subscription Key**

### Step 2: Add the Connector in Power Automate
1. Open your Power Automate flow
2. Click **+ New step**
3. Search for **ZIP API**
4. Select any of the 4 operations
5. When prompted, enter your subscription key
6. Click **Create connection**

### Step 3: Use the Operations

#### Create a ZIP file
```json
{
  "zipFileName": "myarchive",
  "files": [
    {
      "name": "document.txt",
      "content": "Hello World",
      "isBase64": false
    }
  ]
}
```

#### Extract a ZIP file
```json
{
  "zipContent": "<base64 encoded ZIP content>",
  "fileName": "myarchive.zip"
}
```

#### Create a password protected ZIP
```json
{
  "zipFileName": "secure-archive",
  "password": "MySecurePassword123",
  "files": [
    {
      "name": "confidential.txt",
      "content": "Confidential content here",
      "isBase64": false
    }
  ]
}
```

#### Extract a password protected ZIP
```json
{
  "zipContent": "<base64 encoded ZIP content>",
  "fileName": "secure-archive.zip",
  "password": "MySecurePassword123"
}
```

## Pricing

| Tier | Calls/Month | Cost |
|---|---|---|
| **Free** | 100 | Free |
| **Paid** | 10,000 | Contact info@gineesoft.com |

## Known Issues and Limitations

- Free tier is limited to 100 API calls per month
- Maximum file size: 50MB per ZIP archive
- Password protected ZIPs use AES-256 encryption
- File content must be provided as plain text or base64 encoded string
- Rate limit: 10 calls per minute (Free), 60 calls per minute (Paid)

## Frequently Asked Questions

**Q: What file types are supported?**  
A: All file types are supported. Provide content as plain text or base64 encoded string.

**Q: How do I convert a file to base64 in Power Automate?**  
A: Use the `base64()` expression. Example: `@{base64(body('Get_file_content'))}`

**Q: What encryption is used for password protected ZIPs?**  
A: AES-256 encryption is used for maximum security.

**Q: Can I use this connector without a premium Power Automate license?**  
A: Once certified as a Standard connector by Microsoft, no premium license is required.

## Support

- **Website:** [https://gineesoft.com](https://gineesoft.com)
- **Email:** [info@gineesoft.com](mailto:info@gineesoft.com)
- **Documentation:** [https://gineesoft.com/docs/zipapi](https://gineesoft.com/docs/zipapi)

## About Gineesoft

Gineesoft is a software company focused on building productivity tools and API services for Microsoft Power Platform users. Our mission is to simplify complex file operations for business users without requiring any coding knowledge.
