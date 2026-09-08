# Security notes

## Gemini API key
This application can call Gemini directly from the browser. A browser-side API key must be treated as exposed to the user/browser environment.

- Do not use a highly privileged production key.
- Restrict the key in Google AI Studio / Google Cloud as appropriate.
- Do not enter personal or confidential school information into external AI services unless your organization permits it.
- For institutional deployment, prefer a server-side proxy that keeps the API credential off the client.

## Local data
Student records are intended to remain in the browser's local storage unless the teacher explicitly exports, backs up, or sends content to an external AI service.

## Teacher responsibility
AI output is assistance only. The teacher must review and make the final decision before using any generated wording in official records.
