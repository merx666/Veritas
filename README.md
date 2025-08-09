# Veritas dApp - Decentralized Freelance Marketplace

![Veritas Logo]([https://via.placeholder.com/200x80/3B82F6/FFFFFF?text=VERITAS](https://veritas-works.cloud/app-icon-512.svg))

## Overview

Veritas is a decentralized freelance marketplace that leverages World ID for identity verification and provides secure, transparent transactions through smart contracts. Built on World Chain, it ensures trust between freelancers and clients while maintaining privacy and security.

## 🌟 Key Features

- **World ID Verification**: Secure identity verification using Worldcoin's World ID
- **Smart Contract Escrow**: Automated payment escrow using blockchain technology
- **USDC Payments**: Stable cryptocurrency payments through MiniKit
- **Reputation System**: Transparent rating and review system
- **Multi-language Support**: Available in English and Spanish
- **Responsive Design**: Optimized for desktop and mobile devices
- **Real-time Updates**: Live job status and payment tracking

## 🏗️ Architecture

### Frontend
- **React 18** with TypeScript
- **Tailwind CSS** for styling
- **Zustand** for state management
- **React Router** for navigation
- **i18next** for internationalization
- **Vite** for build tooling

### Backend
- **Node.js** with Express
- **TypeScript** for type safety
- **JSON-based mock database** (development)
- **Joi** for validation
- **CORS** and security middleware

### Smart Contracts
- **Solidity** smart contracts
- **Hardhat** development environment
- **World Chain** deployment
- **Escrow contract** for secure payments

### Testing
- **Jest** for unit and integration tests
- **React Testing Library** for component testing
- **Cypress** for end-to-end testing
- **Comprehensive test coverage**

## 🚀 Quick Start

### Prerequisites

- Node.js 18+
- npm or yarn
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-org/veritas-dapp.git
   cd veritas-dapp
   ```

2. **Install dependencies**
   ```bash
   # Install frontend dependencies
   cd frontend
   npm install
   
   # Install backend dependencies
   cd ../backend
   npm install
   
   # Install contract dependencies
   cd ../contracts
   npm install
   ```

3. **Environment Setup**
   ```bash
   # Frontend environment
   cd frontend
   cp .env.example .env
   # Edit .env with your configuration
   
   # Backend environment
   cd ../backend
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Start Development Servers**
   ```bash
   # Terminal 1: Start backend
   cd backend
   npm run dev
   
   # Terminal 2: Start frontend
   cd frontend
   npm run dev
   
   # Terminal 3: Start local blockchain (optional)
   cd contracts
   npx hardhat node
   ```

5. **Access the Application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:4000
   - Local blockchain: http://localhost:8545

## 📱 Usage

### For Clients

1. **Verify Identity**: Use World ID to verify your identity
2. **Browse Services**: Search and filter available services
3. **Place Orders**: Select a service and make secure USDC payments
4. **Track Progress**: Monitor job status in real-time
5. **Leave Reviews**: Rate and review completed work

### For Freelancers

1. **Create Profile**: Set up your professional profile
2. **List Services**: Create service offerings with pricing
3. **Manage Jobs**: Accept and complete client orders
4. **Receive Payments**: Get paid automatically upon job completion
5. **Build Reputation**: Earn ratings and build your reputation

## 🧪 Testing

### Run All Tests
```bash
# Frontend tests
cd frontend
npm test
npm run test:coverage
npm run e2e

# Backend tests
cd backend
npm test

# Contract tests
cd contracts
npm test
```

### Test Coverage
- Unit tests for all components and utilities
- Integration tests for user flows
- End-to-end tests for critical paths
- Smart contract tests for security

## 🚀 Deployment

### Frontend Deployment

1. **Build the application**
   ```bash
   cd frontend
   npm run build
   ```

2. **Deploy using the script**
   ```bash
   ./scripts/deploy.sh --deploy
   ```

3. **Manual deployment options**
   - Vercel: `vercel --prod`
   - Netlify: `netlify deploy --prod --dir=dist`
   - AWS S3: `aws s3 sync dist/ s3://bucket-name`

### Backend Deployment

1. **Prepare for production**
   ```bash
   cd backend
   npm run build
   ```

2. **Deploy to your preferred platform**
   - Heroku, Railway, DigitalOcean, AWS, etc.

### Smart Contract Deployment

1. **Deploy to World Chain**
   ```bash
   cd contracts
   npx hardhat deploy --network worldchain
   ```

See [DEPLOYMENT.md](frontend/DEPLOYMENT.md) for detailed deployment instructions.

## 🔧 Configuration

### Environment Variables

#### Frontend
```bash
VITE_API_URL=http://localhost:4000/api/v1
VITE_WORLD_ID_APP_ID=your_world_id_app_id
VITE_WORLD_ID_ACTION_ID=your_action_id
VITE_MINIKIT_API_KEY=your_minikit_key
```

#### Backend
```bash
PORT=4000
NODE_ENV=development
WORLD_ID_APP_ID=your_world_id_app_id
WORLD_ID_ACTION_ID=your_action_id
```

#### Smart Contracts
```bash
PRIVATE_KEY=your_private_key
WORLD_CHAIN_RPC_URL=https://worldchain-mainnet.g.alchemy.com/v2/your-key
```

## 📚 API Documentation

### Authentication
All protected endpoints require World ID verification.

### Endpoints

#### Users
- `GET /api/v1/users/:worldId` - Get user profile
- `POST /api/v1/users` - Create user profile
- `PUT /api/v1/users/:worldId` - Update user profile

#### Services
- `GET /api/v1/services` - List services
- `GET /api/v1/services/:id` - Get service details
- `POST /api/v1/services` - Create service
- `GET /api/v1/services/search` - Search services

#### Jobs
- `GET /api/v1/jobs/user/:worldId` - Get user jobs
- `POST /api/v1/jobs` - Create job
- `PUT /api/v1/jobs/:id/status` - Update job status

#### Reviews
- `GET /api/v1/reviews/user/:worldId` - Get user reviews
- `POST /api/v1/reviews` - Submit review

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Workflow

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Ensure all tests pass
6. Submit a pull request

### Code Standards

- TypeScript for type safety
- ESLint for code quality
- Prettier for code formatting
- Conventional commits for commit messages

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

### Documentation
- [Frontend README](frontend/README.md)
- [Backend README](backend/README.md)
- [Smart Contracts README](contracts/README.md)
- [Testing Guide](frontend/TESTING.md)
- [Deployment Guide](frontend/DEPLOYMENT.md)

### Community
- [Discord](https://discord.gg/veritas-dapp)
- [Telegram](https://t.me/veritas_dapp)
- [Twitter](https://twitter.com/veritas_dapp)

### Issues
If you encounter any issues, please [create an issue](https://github.com/your-org/veritas-dapp/issues) on GitHub.

## 🙏 Acknowledgments

- [Worldcoin](https://worldcoin.org) for World ID integration
- [World Chain](https://worldchain.org) for blockchain infrastructure
- [MiniKit](https://docs.worldcoin.org/minikit) for payment integration
- The open-source community for amazing tools and libraries

## 🗺️ Roadmap

### Phase 1 (Current)
- ✅ Core marketplace functionality
- ✅ World ID integration
- ✅ Smart contract escrow
- ✅ Multi-language support

### Phase 2 (Next)
- [ ] Advanced search and filtering
- [ ] Dispute resolution system
- [ ] Mobile app development
- [ ] Integration with more payment methods

### Phase 3 (Future)
- [ ] DAO governance
- [ ] NFT certificates for completed work
- [ ] AI-powered matching
- [ ] Cross-chain compatibility

---

**Built with ❤️ by the Veritas Team**
