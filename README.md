# AI Voice Assistant Dashboard

## Overview
This project provides a simple web‑based dashboard for initiating and managing AI‑assisted voice calls. It acts as the front‑end for a voice assistant platform, allowing users to dial phone numbers, choose the purpose of the call, schedule calls, customize call scripts and manage reusable call templates. The dashboard is built with plain HTML, Tailwind CSS and JavaScript and is intended to be integrated with backend services (e.g. Twilio or Azure Communication Services and an AI service like OpenAI) to handle call routing and AI responses.

## Features & Tech Stack
- **Outbound call panel:** input a phone number, choose a call purpose (customer support, information inquiry, appointment reminder, follow‑up call or a custom script), and schedule the call immediately or at a future time.
- **Custom call scripts:** provide a custom message or script that the AI voice assistant will speak during the call.
- **Call templates management:** create, edit and delete reusable templates to standardize common call types.
- **Call status feedback:** after initiating a call, view a status indicator with a loading animation and messages describing the call’s current state.
 **Transcripts display:** show the live transcript of the conversation between the AI assistant and the callee (requires backend support).
- **Lightweight and self‑contained:** single HTML file styled with Tailwind CSS; easy to deploy on static hosting or integrate into an existing project.


| Technology | Description |
| --- | --- |
| HTML | Provides markup for the dashboard UI |
| Tailwind CSS | Provides styling and responsive layout |
| JavaScript | Handles user interactions and integrates with backend services |
Project Structure
The repository consists of two main files:
- `Azure-RefactorAllInOne.html` – a single‑page application containing the dashboard’s markup, inline styles and JavaScript logic.
- `README.md` – this file, describing the purpose and usage of the dashboard.

## Getting Started
Because this repository contains only the client‑side dashboard, you’ll need to supply server‑side APIs to send and receive voice calls. A typical setup includes:
1. **Telephony provider** – use a platform like [Twilio](https://www.twilio.com/) or Azure Communication Services to place outbound calls and receive webhooks for call status updates and transcripts.
2. **AI speech service** – integrate with an AI service (e.g. [OpenAI](https://openai.com/), Azure Cognitive Services) to generate responses to user speech.
3. **Backend API** – build endpoints that the dashboard’s JavaScript can call to start calls, send call scripts and templates, and receive real‑time updates. Update the `fetch` URLs inside `Azure‑RefactorAllInOne.html` accordingly.

To test locally:
1. Clone this repository:
   ```bash
   git clone https://github.com/g4mm4p4nd4/ai‑voice‑dashboard.git
   cd ai‑voice‑dashboard
   ```
2. Open `Azure‑RefactorAllInOne.html` in a modern web browser. The UI will load but initiating calls requires your backend service endpoints to be configured.

## Customization
- Modify the call purposes and options in the `<select id="call-purpose">` element to fit your use case.
- Tailwind CSS classes can be adjusted or removed if you prefer another styling method.
- Update the JavaScript functions at the bottom of `Azure‑RefactorAllInOne.html` to integrate with your backend endpoints.

## Contributing
Pull requests and suggestions are welcome! If you enhance the dashboard or integrate new features (e.g. multi‑language support, inbound calls, authentication), feel free to submit a PR. Ensure that your code is well commented and tested.

## License
At thAt the time of writing there is no explicit license file in this repository. If you intend to use or redistribute this project, consider adding an appropriate open-source license or contact the repository owner for guidance.
## Business & Entrepreneurial Value

- **Subscription and licensing potential:** The AI-powered voice call dashboard can be monetized through subscriptions or licensing to organizations that need automated outbound calling and text-to-speech features.
- **Scalability and integration:** Designed as a client‑side interface, this project can scale with serverless backends and integrate with telephony providers and AI services, unlocking opportunities for upsells and custom deployments.
- **Efficiency and insights:** Automating voice calls reduces operational overhead and captures rich data for analytics, enabling businesses to make data‑driven decisions and create differentiated products.

## Consumer Value

- **User-friendly experience:** End users benefit from an intuitive dashboard that simplifies initiating, monitoring and customizing voice calls without needing to write code.
- **Time savings and convenience:** Automated dialing, scripted responses and real‑time updates streamline communication workflows and save users time compared to manual outreach.
- **Trust and transparency:** With an open‑source design and clear separation between client and server functionality, users have greater control over their data and can adapt the dashboard to meet privacy requirements.
