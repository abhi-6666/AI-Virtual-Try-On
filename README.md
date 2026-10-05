# AI Virtual Try-On Chrome Extension

A Chrome Extension based AI shopping assistant that detects product images on shopping websites and sends a selected product together with a reusable digital profile to an AI virtual try-on backend powered by IDM-VTON.

## Assignment coverage

- Manifest V3 Chrome extension
- Reusable digital body/profile photo stored locally in Chrome storage
- Product detection from the current shopping webpage
- Product title, image, URL, retailer, price, MRP/discount, category and metadata extraction when available
- Generic DOM + structured-data detection rather than a single hard-coded website
- Product selection and Try On action
- AI try-on request through FastAPI + IDM-VTON
- Upper-body, lower-body and dress category mapping for the current model
- Loading/progress state and readable failure messages
- Try-on history and wardrobe stored locally
- Privacy controls for profile deletion and result/history cleanup
- Backend result storage and local result deletion endpoint
- Architecture, installation and demonstration documentation

## Project structure

```text
AI-Virtual-Try-On-main/
├── extension/
│   ├── manifest.json
│   ├── content.js
│   ├── popup.html
│   ├── popup.css
│   └── popup.js
├── backend/
│   ├── main.py
│   ├── image_input_prep.py
│   ├── requirements.txt
│   └── test / diagnostic utilities
├── docs/
│   ├── ARCHITECTURE.md
│   ├── SETUP.md
│   └── DEMO_CHECKLIST.md
└── harness_*.js
```

## Important

The project uses the IDM-VTON hosted Hugging Face Space. A Hugging Face account/token and a working hosted inference quota are required for live generation. The extension does not contain the Hugging Face token; authentication is performed by the backend.

For academic submission, retain the original project's attribution/license requirements and identify any reused open-source components according to their license.
