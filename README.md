# BriskStack Platform SDK (TypeScript)

Official TypeScript SDK for the BriskStack Platform. Access all BriskStack services through a single unified SDK.

[![npm version](https://badge.fury.io/js/%40briskstack%2Fsdk.svg)](https://www.npmjs.com/package/@briskstack/platform-sdk)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Installation

```bash
npm install @briskstack/platform-sdk
```

Or with yarn:

```bash
yarn add @briskstack/platform-sdk
```

Or with pnpm:

```bash
pnpm add @briskstack/platform-sdk
```

## Quick Start

```typescript
import { Configuration, HelloWorldMessagesApi, AiGatewayChatApi } from '@briskstack/platform-sdk';

// Configure once for all services
const config = new Configuration({
  basePath: 'https://api.briskstack.com',
  accessToken: 'your-jwt-token',
});

// Use different services
const helloWorldApi = new HelloWorldMessagesApi(config);
const message = await helloWorldApi.helloWorldV1MessagesPost({
  helloWorldCreateMessageRequest: { content: 'Hello!' },
});

const aiGatewayApi = new AiGatewayChatApi(config);
const completion = await aiGatewayApi.aiGatewayV1ChatCompletionsPost({
  aiGatewayChatCompletionRequest: {
    model: 'gpt-4',
    messages: [{ role: 'user', content: 'Hello AI' }],
  },
});
```

## Features

- 🚀 **Unified SDK** - Access all BriskStack services through a single package
- 📦 **Tree-shakeable** - Only bundle the APIs you use
- 🔐 **Multiple Auth Methods** - Support for JWT tokens and API keys
- 🌐 **Environment URLs** - Predefined configs for dev, staging, and production
- 📝 **Full TypeScript Support** - Complete type definitions for all APIs
- 🔄 **Auto-generated** - Always up-to-date with the latest API changes

## Authentication

### Bearer Token (JWT)

For user authentication via Supabase:

```typescript
const config = new Configuration({
  basePath: 'https://api.briskstack.com',
  accessToken: 'your-jwt-token',
});
```

### API Key

For BYOK (Bring Your Own Key) scenarios:

```typescript
const config = new Configuration({
  basePath: 'https://api.briskstack.com',
  apiKey: 'your-api-key',
});
```

## Environment URLs

The SDK supports multiple environments:

```typescript
// Development
const config = new Configuration({
  basePath: 'https://api-dev.briskstack.com',
  accessToken: 'your-token',
});

// Staging
const config = new Configuration({
  basePath: 'https://api-staging.briskstack.com',
  accessToken: 'your-token',
});

// Production
const config = new Configuration({
  basePath: 'https://api.briskstack.com',
  accessToken: 'your-token',
});
```

## Available Services

This SDK includes all BriskStack platform services:

- **Hello World** - Example service
- **AI Gateway** - AI model integrations
- _(More services added automatically)_

See the [API documentation](https://docs.briskstack.com) for complete service details.

## Usage Examples

### Hello World Service

```typescript
import { Configuration, HelloWorldMessagesApi } from '@briskstack/platform-sdk';

const config = new Configuration({
  basePath: 'https://api.briskstack.com',
  accessToken: 'your-jwt-token',
});

const api = new HelloWorldMessagesApi(config);

// Create a message
const message = await api.helloWorldV1MessagesPost({
  helloWorldCreateMessageRequest: { content: 'Hello, World!' },
});

console.log(message.data);
```

### AI Gateway Service

```typescript
import { Configuration, AiGatewayChatApi } from '@briskstack/platform-sdk';

const config = new Configuration({
  basePath: 'https://api.briskstack.com',
  apiKey: 'your-api-key', // Use API key for BYOK
});

const api = new AiGatewayChatApi(config);

// Create a chat completion
const completion = await api.aiGatewayV1ChatCompletionsPost({
  aiGatewayChatCompletionRequest: {
    model: 'gpt-4',
    messages: [
      { role: 'system', content: 'You are a helpful assistant.' },
      { role: 'user', content: 'Tell me a joke about programming.' },
    ],
  },
});

console.log(completion.data.choices[0].message.content);
```

## Error Handling

```typescript
try {
  const message = await api.helloWorldV1MessagesPost({
    helloWorldCreateMessageRequest: { content: 'Hello!' },
  });
} catch (error) {
  if (error.response) {
    // Server responded with error status
    console.error('Error:', error.response.status, error.response.data);
  } else if (error.request) {
    // Request was made but no response received
    console.error('No response:', error.request);
  } else {
    // Something else went wrong
    console.error('Error:', error.message);
  }
}
```

## TypeScript Support

This SDK is written in TypeScript and provides full type definitions:

```typescript
import type {
  HelloWorldMessage,
  HelloWorldCreateMessageRequest,
  AiGatewayChatCompletionRequest,
  AiGatewayChatCompletionResponse,
} from '@briskstack/platform-sdk';

const request: HelloWorldCreateMessageRequest = {
  content: 'Hello!',
  metadata: { key: 'value' },
};

const message: HelloWorldMessage = await api.helloWorldV1MessagesPost({
  helloWorldCreateMessageRequest: request,
});
```

## Framework Integration

### Next.js

```typescript
// app/api/hello/route.ts
import { Configuration, HelloWorldMessagesApi } from '@briskstack/platform-sdk';
import { NextResponse } from 'next/server';

export async function POST(request: Request) {
  const config = new Configuration({
    basePath: process.env.BRISKSTACK_API_URL,
    accessToken: request.headers.get('authorization')?.replace('Bearer ', ''),
  });

  const api = new HelloWorldMessagesApi(config);
  const message = await api.helloWorldV1MessagesPost({
    helloWorldCreateMessageRequest: await request.json(),
  });

  return NextResponse.json(message.data);
}
```

### Express

```typescript
import express from 'express';
import { Configuration, HelloWorldMessagesApi } from '@briskstack/platform-sdk';

const app = express();
app.use(express.json());

app.post('/api/hello', async (req, res) => {
  const config = new Configuration({
    basePath: process.env.BRISKSTACK_API_URL,
    accessToken: req.headers.authorization?.replace('Bearer ', ''),
  });

  const api = new HelloWorldMessagesApi(config);
  const message = await api.helloWorldV1MessagesPost({
    helloWorldCreateMessageRequest: req.body,
  });

  res.json(message.data);
});
```

## Browser Support

This SDK uses the [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) and is compatible with:

- Chrome/Edge 42+
- Firefox 39+
- Safari 10.1+
- Node.js 18+

For older browsers, use a fetch polyfill like [whatwg-fetch](https://www.npmjs.com/package/whatwg-fetch).

## Contributing

This SDK is automatically generated from OpenAPI specifications. For SDK issues, please open an issue in this repository.

## Documentation

- [API Documentation](https://docs.briskstack.com)

## License

MIT

## Support

- GitHub Issues: [briskstack/platform-sdk-typescript/issues](https://github.com/briskstack/platform-sdk-typescript/issues)
- Email: support@briskstack.com
- Documentation: [docs.briskstack.com](https://docs.briskstack.com)
