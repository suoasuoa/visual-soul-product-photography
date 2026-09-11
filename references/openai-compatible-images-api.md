# OpenAI-Compatible Images API

Read this reference only when the selected provider exposes an OpenAI-compatible Images API.

## Secure setup

Keep credentials in the user's secure environment. Common variables are:

```bash
export OPENAI_API_KEY="..."
export OPENAI_BASE_URL="https://your-provider.example/v1"
```

Do not commit `.env` files, API keys, internal gateway URLs, request logs containing authorization headers, or unlicensed reference images.

## Image references

Some compatible providers accept images through an edit endpoint and require each input to be a base64 data URL:

```json
{
  "image_url": "data:image/png;base64,<encoded-bytes>"
}
```

Use the correct MIME type. Product references normally control geometry and materials; one or two visual references control mood and camera behavior. Check provider documentation for model names, endpoint paths, accepted request fields, output format, and size support.

## Output handling

Save every candidate with a versioned name. Decode image data only after a successful response, inspect actual output dimensions, then review against the candidate score card. A provider can return a different aspect ratio from the one requested.

## Provider-neutral rule

This skill defines creative and review logic, not a vendor lock-in. The user chooses the image provider. Never silently replace a user-selected provider with another provider.
