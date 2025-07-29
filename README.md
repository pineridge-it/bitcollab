# BitCollab - Decentralized Collaboration Platform

BitCollab is a revolutionary decentralized collaboration platform that leverages Bitcoin-based reputation tokens to create a trustless environment for project collaboration, task management, and contributor recognition.

## 🚀 Features

### Core Functionality
- **Decentralized Project Management**: Create and manage projects without centralized control
- **Bitcoin-Based Reputation System**: Earn and spend reputation tokens backed by Bitcoin
- **Task Assignment & Tracking**: Comprehensive task management with milestone tracking
- **Contributor Recognition**: Transparent reputation scoring based on contributions
- **Secure Wallet Integration**: Connect Bitcoin wallets for reputation token transactions

### Advanced Features
- **Smart Contract Integration**: Automated reputation distribution through smart contracts
- **Peer-to-Peer Collaboration**: Direct collaboration without intermediaries
- **Reputation Marketplace**: Trade reputation tokens with other contributors
- **Project Analytics**: Detailed insights into project progress and contributor performance
- **Multi-signature Support**: Enhanced security for high-value projects

## 🛠 Technology Stack

- **Frontend**: Next.js 14, React 18, TypeScript
- **Styling**: Tailwind CSS, Shadcn/ui components
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: NextAuth.js with multiple providers
- **Bitcoin Integration**: Custom Bitcoin wallet integration
- **State Management**: React Context API
- **API**: Next.js API routes with RESTful endpoints

## 📋 Prerequisites

Before running BitCollab, ensure you have the following installed:

- **Node.js** (v18.0.0 or higher)
- **npm** or **yarn** package manager
- **PostgreSQL** (v13.0 or higher)
- **Git** for version control
- **Bitcoin Core** (optional, for advanced features)

## 🔧 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/pineridge-it/bitcollab.git
cd bitcollab
```

### 2. Install Dependencies
```bash
cd app
npm install
# or
yarn install
```

### 3. Environment Configuration
Create a `.env.local` file in the app directory with the following variables:

```env
# Database Configuration
DATABASE_URL="postgresql://username:password@localhost:5432/bitcollab"

# NextAuth Configuration
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="your-nextauth-secret-key"

# OAuth Providers (optional)
GITHUB_CLIENT_ID="your-github-client-id"
GITHUB_CLIENT_SECRET="your-github-client-secret"
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"

# Bitcoin Configuration
BITCOIN_NETWORK="testnet" # or "mainnet" for production
BITCOIN_RPC_URL="http://localhost:18332"
BITCOIN_RPC_USER="your-rpc-username"
BITCOIN_RPC_PASSWORD="your-rpc-password"

# Application Settings
APP_URL="http://localhost:3000"
REPUTATION_TOKEN_SYMBOL="BTCR"
```

### 4. Database Setup
```bash
cd app
# Generate Prisma client
npx prisma generate

# Run database migrations
npx prisma migrate dev

# Seed the database (optional)
npx prisma db seed
```

## 🚀 Running the Application

### Development Mode
```bash
cd app
npm run dev
# or
yarn dev
```

The application will be available at `http://localhost:3000`

### Production Build
```bash
cd app
# Build the application
npm run build

# Start production server
npm run start
```

### Database Management
```bash
cd app
# View database in Prisma Studio
npx prisma studio

# Reset database
npx prisma migrate reset

# Deploy migrations to production
npx prisma migrate deploy
```

## 📁 Project Structure

```
bitcollab/
├── app/                    # Next.js 14 app directory
│   ├── api/               # API routes
│   ├── components/        # React components
│   ├── lib/              # Utility libraries
│   ├── prisma/           # Database schema and migrations
│   ├── scripts/          # Database seeding scripts
│   └── pages/            # Application pages
├── README.md             # Project documentation
└── .gitignore           # Git ignore rules
```

## 🔐 Security Features

- **Multi-signature Wallet Support**: Enhanced security for reputation token transactions
- **Encrypted Data Storage**: Sensitive data encrypted at rest
- **Rate Limiting**: API endpoints protected against abuse
- **Input Validation**: Comprehensive validation on all user inputs
- **CSRF Protection**: Cross-site request forgery protection enabled

## 🤝 Contributing

We welcome contributions to BitCollab! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Write comprehensive tests for new features
- Ensure code passes ESLint and Prettier checks
- Update documentation for new features

## 📊 API Documentation

### Authentication Endpoints
- `POST /api/auth/signin` - User sign in
- `POST /api/auth/signout` - User sign out
- `GET /api/auth/session` - Get current session

### Project Management
- `GET /api/projects` - List all projects
- `POST /api/projects` - Create new project
- `GET /api/projects/[id]` - Get project details
- `PUT /api/projects/[id]` - Update project
- `DELETE /api/projects/[id]` - Delete project

### Reputation System
- `GET /api/reputation/balance` - Get user reputation balance
- `POST /api/reputation/transfer` - Transfer reputation tokens
- `GET /api/reputation/history` - Get transaction history

## 🧪 Testing

```bash
cd app
# Run unit tests
npm run test

# Run integration tests
npm run test:integration

# Run end-to-end tests
npm run test:e2e

# Generate test coverage report
npm run test:coverage
```

## 🚀 Deployment

### Vercel Deployment (Recommended)
1. Connect your GitHub repository to Vercel
2. Set the root directory to `app`
3. Configure environment variables in Vercel dashboard
4. Deploy automatically on push to main branch

### Docker Deployment
```bash
# Build Docker image
docker build -t bitcollab ./app

# Run container
docker run -p 3000:3000 bitcollab
```

### Manual Deployment
1. Navigate to app directory: `cd app`
2. Build the application: `npm run build`
3. Set up PostgreSQL database
4. Configure environment variables
5. Start the application: `npm run start`

## 🔧 Configuration

### Bitcoin Network Configuration
- **Testnet**: Use for development and testing
- **Mainnet**: Use for production with real Bitcoin

### Database Configuration
- Supports PostgreSQL, MySQL, and SQLite
- Configure connection string in `DATABASE_URL`

## 📈 Roadmap

- [ ] Mobile application (React Native)
- [ ] Advanced analytics dashboard
- [ ] Integration with more Bitcoin wallets
- [ ] Multi-chain support (Ethereum, Litecoin)
- [ ] AI-powered project recommendations
- [ ] Advanced reputation algorithms

## 🐛 Known Issues

- Bitcoin testnet transactions may take longer to confirm
- Large file uploads may timeout on slower connections
- Some wallet integrations require manual configuration

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Bitcoin Core** team for the foundational Bitcoin protocol
- **Next.js** team for the excellent React framework
- **Prisma** team for the powerful database toolkit
- **Tailwind CSS** for the utility-first CSS framework
- **Shadcn/ui** for the beautiful component library

## 📞 Support

For support and questions:
- Create an issue on GitHub
- Join our Discord community
- Email: support@bitcollab.dev

## 🌟 Star History

If you find BitCollab useful, please consider giving it a star on GitHub!

---

**Built with ❤️ by the BitCollab team**
