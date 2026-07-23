# AZERTY CRM

AZERTY CRM with fake Genesys Cloud Composable Desktop
A comprehensive, dependency-free fake CRM front-end built with plain HTML, CSS and JavaScript.

## Run it

Open `index.html` directly in a modern browser, or serve the directory locally:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080`.

## Included CRM features

- Responsive CRM dashboard
- Revenue chart and pipeline health visualisation
- Contacts with filtering, sorting, bulk selection and deletion
- Company account cards
- Drag-and-drop sales pipeline
- Tasks with filters and completion states
- Activity timeline
- Reports, integrations and settings screens
- Quick-create menu and reusable modals
- Local CSV dashboard export
- Toast notifications
- Keyboard shortcut: Ctrl/Cmd + K focuses global search

## Genesys Cloud Composable Desktop demo

The **Genesys Desktop** workspace adds a realistic simulation of a CRM-hosted agent experience:

- Omnichannel interaction inbox for voice, chat and email
- Agent presence and queue metrics
- Active conversation controls: mute, hold, keypad, transfer and disconnect
- CRM screen pop matched to the current interaction
- Live transcript and customer context
- Simulated **Agent Copilot** component
- Simulated **Scripts / Scripter** component
- Simulated **ACW** component with wrap-up code and CRM follow-up task creation
- CRM click-to-call from the Contacts table
- SDK sandbox for `GET_STATUS`, `REGISTRATION_REQUEST`, `SET_LOCALE` and `SET_INTERACTION`
- Simulated broker event log and default / embedded component scopes

### Moving from simulation to the real SDK

The visual components are intentionally simulated so the project runs without credentials. A real Genesys Cloud Composable Desktop implementation requires:

1. A valid Genesys Cloud environment and user permissions.
2. Hosting the CRM integration over HTTPS for cross-origin messaging.
3. A component ID and a component name approved during Composable Desktop onboarding.
4. A hidden broker iframe and visible component iframes.
5. Broker registration, status handling and interaction propagation through `window.postMessage`.
6. A valid Genesys Cloud interaction ID to provide component context.

The official examples demonstrate Copilot in the default scope and Scripts plus ACW in embedded scopes.

All CRM and interaction data in this project is fake and stored in memory, so refreshing the page resets the demo.
