# EcoFinds - Sustainable Marketplace Platform

A modern, full-stack marketplace platform built for the Odoo Hackathon, connecting eco-conscious buyers and sellers in a sustainable e-commerce environment.

## 🌱 Project Overview

EcoFinds is a comprehensive marketplace solution that enables users to buy and sell eco-friendly products. The platform features a modern React frontend with TypeScript, a robust Express.js backend, and seamless deployment via Netlify.

## 🚀 Features

### Core Marketplace Features
- **User Authentication & Registration**: Secure login and signup with role-based access
- **Product Listings**: Create, browse, and manage sustainable product listings
- **Shopping Cart**: Add items to cart with real-time updates
- **Purchase Management**: Track orders and purchase history
- **Seller Dashboard**: Comprehensive tools for sellers to manage their listings
- **Admin Panel**: Administrative controls for platform management

### Technical Features
- **Modern Stack**: React 18, TypeScript, Express.js, Tailwind CSS
- **Responsive Design**: Mobile-first approach with Radix UI components
- **Real-time Updates**: Optimistic UI updates with React Query
- **Serverless Architecture**: Deployed on Netlify with serverless functions
- **Type Safety**: Full TypeScript implementation across frontend and backend
- **Modern Dev Tools**: Vite for fast development, Vitest for testing

## 🛠️ Tech Stack

### Frontend
- **React 18.3** with TypeScript
- **Vite** for build tooling and development
- **Tailwind CSS** for styling
- **Radix UI** for accessible components
- **React Router** for navigation
- **React Query** for data fetching and caching
- **Framer Motion** for animations
- **Lucide React** for icons

### Backend
- **Express.js 5.0** with TypeScript
- **Serverless Functions** on Netlify
- **CORS** enabled for cross-origin requests
- **Zod** for schema validation
- **Node.js** runtime

### Development Tools
- **TypeScript** for type safety
- **Prettier** for code formatting
- **Vitest** for testing
- **ESBuild** for fast bundling

## 📁 Project Structure

```
├── client/                 # React frontend application
│   ├── components/         # Reusable UI components
│   ├── pages/             # Application pages
│   ├── hooks/             # Custom React hooks
│   ├── lib/               # Utility functions and API clients
│   └── context/           # React context providers
├── server/                # Express.js backend
│   ├── routes/            # API route definitions
│   └── index.ts           # Server entry point
├── netlify/functions/     # Serverless functions for Netlify
├── shared/               # Shared types and utilities
└── public/               # Static assets
```

## 🚦 Getting Started

### Prerequisites
- **Node.js** (v18 or higher)
- **pnpm** package manager
- **Git** for version control

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd odoo-hackathon
   ```

2. **Install dependencies**
   ```bash
   pnpm install
   ```

3. **Environment Setup**
   
   Create a `.env.local` file for local development:
   ```bash
   # .env.local (for local secrets)
   VITE_PUBLIC_BUILDER_KEY=your_builder_key_here
   DATABASE_URL=your_database_url
   JWT_SECRET=your_jwt_secret
   ```

4. **Start development server**
   ```bash
   # Start both frontend and backend
   pnpm dev
   
   # Frontend only (http://localhost:5173)
   pnpm dev:client
   
   # Backend only (http://localhost:3001)
   pnpm dev:server
   ```

### Available Scripts

```bash
# Development
pnpm dev              # Start development server
pnpm dev:client       # Start frontend only
pnpm dev:server       # Start backend only

# Building
pnpm build           # Build for production
pnpm build:client  # Build frontend only
pnpm build:server  # Build backend only

# Testing
pnpm test            # Run tests
pnpm typecheck      # Type checking
pnpm format.fix     # Format code with Prettier

# Production
pnpm start          # Start production server
```

## 🌐 Deployment

### Netlify Deployment

The project is configured for seamless deployment on Netlify:

1. **Connect repository** to Netlify
2. **Build settings** are automatically configured via `netlify.toml`
3. **Environment variables** can be set in Netlify dashboard

### Environment Variables

#### Required Variables
- `VITE_PUBLIC_BUILDER_KEY`: Builder.io API key for content management
- `PING_MESSAGE`: Health check message

#### Optional Variables
- `DATABASE_URL`: Database connection string
- `JWT_SECRET`: Secret for JWT token generation
- `PORT`: Server port (default: 3001)

## 🎯 Core Pages & Features

### Authentication
- **Login Page** (`/login`): User authentication
- **Register Page** (`/register`): New user registration

### Marketplace
- **Home Page** (`/`): Landing page with featured products
- **Marketplace** (`/marketplace`): Browse all products
- **Listing Detail** (`/listing/:id`): Individual product view
- **Sell Page** (`/sell`): Create new product listings

### User Dashboard
- **Dashboard** (`/dashboard`): User overview and stats
- **My Listings** (`/my-listings`): Manage seller listings
- **Cart** (`/cart`): Shopping cart management
- **Purchases** (`/purchases`): Order history and tracking

### Administration
- **Admin Panel** (`/admin`): Platform administration tools

## 🔧 Development Guidelines

### Code Style
- **TypeScript**: All code should be strongly typed
- **Prettier**: Code is automatically formatted on save
- **ESLint**: Follows recommended TypeScript rules

### Component Structure
```typescript
// Example component structure
interface ComponentProps {
  // Type definitions
}

export const ComponentName: React.FC<ComponentProps> = ({ props }) => {
  // Component logic
  return (
    // JSX markup
  );
};
```

### API Structure
```typescript
// Example API route
export const apiRoute = express.Router();

apiRoute.get('/endpoint', async (req, res) => {
  try {
    // Business logic
    res.json({ success: true, data });
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
});
```

## 🧪 Testing

### Running Tests
```bash
# Run all tests
pnpm test

# Run tests in watch mode
pnpm test:watch

# Run tests with coverage
pnpm test:coverage
```

### Test Structure
- **Unit tests** in `*.spec.ts` files
- **Component tests** using React Testing Library
- **API tests** for backend endpoints

## 📱 Responsive Design

The application is built with a mobile-first approach:
- **Mobile**: 320px and up
- **Tablet**: 768px and up  
- **Desktop**: 1024px and up
- **Large screens**: 1280px and up

## 🤝 Contributing

1. **Fork the repository**
2. **Create feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit changes**: `git commit -m 'Add amazing feature'`
4. **Push to branch**: `git push origin feature/amazing-feature`
5. **Open Pull Request**

### Commit Message Format
```
type(scope): description

Examples:
feat(marketplace): add product filtering
fix(auth): resolve login validation bug
docs(readme): update installation instructions
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Odoo Hackathon** for the opportunity
- **Open source community** for the amazing tools and libraries
- **Contributors** who helped make this project possible

## 📞 Support

For support and questions:
- **Issues**: [GitHub Issues](https://github.com/your-repo/issues)
- **Email**: support@ecofinds.com
- **Discord**: [Join our community](https://discord.gg/ecofinds)

---

**Built with ❤️ for the Odoo Hackathon**