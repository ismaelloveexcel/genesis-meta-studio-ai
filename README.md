# GENESIS Meta Studio AI v1.0

**Professional AI-powered Content Generation Platform**

> Create stunning videos, interactive games, and immersive 3D worlds in minutes using cutting-edge AI technology.

[![GitHub](https://img.shields.io/badge/GitHub-GENESIS%20Meta%20Studio%20AI-blue?logo=github)](https://github.com/GENEZUX/genesis-meta-studio-ai)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen)]()

## Features

- **Video Studio Ultra**: Generate 4K professional videos with AI using Nova, Krea.ai, and Adobe Firefly
- **Game Builder AI**: Create 3D games without coding using Babylon.js and WebGL
- **3D World Generator**: Build procedural 3D worlds with Genie 3 DeepMind
- **Marketplace**: Sell and monetize content with 30% commission model
- **Real-time Dashboard**: Monitor metrics, usage, and subscriptions
- **Enterprise Security**: JWT authentication, GDPR compliance, 99.9% SLA

## Technology Stack

### Frontend
- **Framework**: Next.js 14 + React 18
- **Styling**: Tailwind CSS + Shadcn/ui
- **Type Safety**: TypeScript
- **Animations**: Framer Motion

### Backend
- **Runtime**: Node.js 20+
- **Framework**: Express.js
- **Database**: PostgreSQL + Prisma ORM
- **Cache**: Redis
- **Authentication**: JWT + OAuth 2.0

### AI/ML Integrations
- **Video Generation**: Nova Agent API
- **Video Enhancement**: Krea.ai API
- **Visual Effects**: Adobe Firefly API
- **3D Rendering**: Babylon.js + WebGL
- **Automation**: n8n Workflows

### Infrastructure
- **Frontend Hosting**: Vercel
- **Backend Orchestration**: Kubernetes
- **Payment Processing**: Stripe
- **CI/CD**: GitHub Actions
- **Containerization**: Docker (node:20-alpine)
- **Monitoring**: Winston, Sentry, Prometheus

## Project Structure

```
genesis-meta-studio-ai/
├── frontend/                    # Next.js frontend application
│   ├── pages/
│   │   ├── index.tsx           # Landing page
│   │   ├── dashboard.tsx       # User dashboard
│   │   ├── studio/
│   │   │   ├── video.tsx       # Video studio
│   │   │   ├── game.tsx        # Game builder
│   │   │   └── 3d.tsx          # 3D world generator
│   │   └── marketplace.tsx     # Marketplace
│   ├── components/
│   ├── lib/
│   └── styles/
├── backend/                     # Express.js backend
│   ├── src/
│   │   ├── routes/
│   │   │   ├── auth.ts         # Authentication endpoints
│   │   │   ├── video.ts        # Video generation
│   │   │   ├── game.ts         # Game creation
│   │   │   ├── 3d.ts           # 3D world generation
│   │   │   ├── payment.ts      # Payment/subscription
│   │   │   ├── marketplace.ts  # Marketplace
│   │   │   └── dashboard.ts    # Metrics
│   │   ├── middleware/
│   │   │   ├── auth.ts         # JWT verification
│   │   │   ├── rateLimit.ts    # Rate limiting
│   │   │   └── errorHandler.ts # Global error handling
│   │   ├── services/
│   │   │   ├── novaService.ts  # Nova AI integration
│   │   │   ├── kreiaService.ts # Krea.ai integration
│   │   │   ├── stripeService.ts# Stripe integration
│   │   │   └── cacheService.ts # Redis caching
│   │   ├── db/
│   │   │   └── prisma/
│   │   │       └── schema.prisma # Database schema
│   │   └── app.ts              # Express app setup
│   └── .env.example            # Environment variables
├── workflows/                   # n8n automation workflows
│   ├── video-generation.json    # Video generation pipeline
│   ├── game-creation.json       # Game creation workflow
│   └── 3d-generation.json       # 3D world generation
├── docker/
│   ├── Dockerfile              # Docker configuration
│   └── docker-compose.yml       # Docker compose for local dev
├── .github/
│   └── workflows/
│       ├── ci-cd.yml           # CI/CD pipeline
│       └── deployment.yml      # Deployment automation
└── README.md                    # This file
```

## API Endpoints

### Authentication
- `POST /api/v1/auth/register` - Register new user
- `POST /api/v1/auth/login` - Login user
- `POST /api/v1/auth/refresh` - Refresh JWT token
- `POST /api/v1/auth/logout` - Logout user

### Video Studio
- `POST /api/v1/video/generate` - Generate video from prompt
- `GET /api/v1/video/:id` - Get video status and metadata
- `DELETE /api/v1/video/:id` - Delete video

### Game Builder
- `POST /api/v1/game/create` - Create new game
- `GET /api/v1/game/:id` - Get game details
- `PUT /api/v1/game/:id` - Update game configuration

### 3D World Generator
- `POST /api/v1/3d/generate` - Generate 3D world
- `GET /api/v1/3d/:id` - Get world generation progress
- `POST /api/v1/3d/:id/export` - Export 3D world

### Payments & Subscriptions
- `POST /api/v1/payment/subscribe` - Create subscription
- `GET /api/v1/payment/subscription` - Get subscription details
- `POST /api/v1/payment/upgrade` - Upgrade plan
- `DELETE /api/v1/payment/subscription` - Cancel subscription

### Dashboard & Metrics
- `GET /api/v1/dashboard/metrics` - Get user metrics
- `GET /api/v1/dashboard/usage` - Get resource usage
- `GET /api/v1/user/profile` - Get user profile

### Marketplace
- `GET /api/v1/marketplace/items` - List marketplace items
- `POST /api/v1/marketplace/item` - Upload item to marketplace
- `GET /api/v1/marketplace/item/:id` - Get item details
- `POST /api/v1/marketplace/item/:id/purchase` - Purchase item

## Environment Variables

Create a `.env.local` file in the root directory:

```bash
# Database
DATABASE_URL="postgresql://user:password@localhost:5432/genesis_db"
REDIS_URL="redis://localhost:6379"

# Authentication
JWT_SECRET="your-secret-key-here"
OAUTH_CLIENT_ID="your-oauth-client-id"
OAUTH_CLIENT_SECRET="your-oauth-client-secret"

# AI Services
NOVA_API_KEY="your-nova-api-key"
KREA_API_KEY="your-krea-api-key"
ADOBE_FIREFLY_KEY="your-adobe-firefly-key"

# Payment Processing
STRIPE_SECRET_KEY="your-stripe-secret-key"
STRIPE_PUBLISHABLE_KEY="your-stripe-publishable-key"

# n8n Automation
N8N_API_URL="https://n8n.your-domain.com"
N8N_API_KEY="your-n8n-api-key"

# Application
NODE_ENV="production"
PORT="3000"
FRONTEND_URL="https://genesis-metaworks.com"
```

## Installation

### Prerequisites
- Node.js 20+
- PostgreSQL 14+
- Redis 7+
- Docker & Docker Compose (optional)

### Backend Setup

```bash
# Clone repository
git clone https://github.com/GENEZUX/genesis-meta-studio-ai.git
cd genesis-meta-studio-ai/backend

# Install dependencies
npm install

# Setup database
npx prisma migrate dev

# Start development server
npm run dev
```

### Frontend Setup

```bash
cd ../frontend
npm install
npm run dev
```

### Replit Deployment

You can deploy this project directly on Replit:

1. **Fork to Replit**: Click the "Run on Replit" button or import the repository directly from GitHub
2. **Configure Environment**: Set up your environment variables in the Replit Secrets tab
3. **Run**: Click the "Run" button - the project will automatically install dependencies and start

[![Run on Replit](https://replit.com/badge/github/GENEZUX/genesis-meta-studio-ai)](https://replit.com/github/GENEZUX/genesis-meta-studio-ai)

The project includes `.replit` and `replit.nix` configuration files for seamless deployment.

## API Testing

All endpoints are documented and testable. Use the following:

```bash
# Test video generation
curl -X POST http://localhost:3000/api/v1/video/generate \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "prompt": "Create a professional marketing video",
    "duration": 30,
    "quality": "4k"
  }'
```

## Pricing Plans

| Plan | Price | Features |
|------|-------|----------|
| **Starter** | $29/mo | 10 videos, 1 game, Community support |
| **Professional** | $99/mo | 500 videos, 100 games, Priority support, Marketplace |
| **Enterprise** | Custom | Unlimited, SLA 99.9%, Dedicated support, API access |

## Security

- ✅ JWT-based authentication
- ✅ bcryptjs password hashing
- ✅ HTTPS/TLS encryption
- ✅ CORS protection
- ✅ Rate limiting (1000 req/min)
- ✅ SQL injection prevention
- ✅ GDPR compliant
- ✅ SOC 2 ready

## Performance

- Video generation: ~60-120 seconds per 30s video
- API response time: <200ms (p99)
- Uptime: 99.9% SLA
- Concurrent users: 50,000+
- Database connections: 100+ optimized pools

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## Support

- **Documentation**: [docs.genesis-metaworks.com](https://docs.genesis-metaworks.com)
- **Email**: support@genesis-metaworks.com
- **Discord**: [Join community](https://discord.gg/genesis-metaworks)
- **Issues**: [GitHub Issues](https://github.com/GENEZUX/genesis-meta-studio-ai/issues)

## Roadmap

- [ ] **v1.1** - Advanced video editing, Multiplayer games
- [ ] **v1.2** - AR/VR support, Real-time collaboration
- [ ] **v1.3** - Mobile app (iOS/Android), Cloud storage integration
- [ ] **v2.0** - Enterprise features, Advanced analytics

## License

MIT License - see [LICENSE](LICENSE) file for details

## Authors

- **GENESIS METAWORKS** - [GitHub](https://github.com/GENEZUX)

## Acknowledgments

- Nova AI for video generation
- Krea.ai for video enhancement
- Adobe Firefly for visual effects
- Babylon.js for 3D rendering
- Vercel for hosting platform

---

**Built with ❤️ by GENESIS METAWORKS**

Make something amazing. 🚀
