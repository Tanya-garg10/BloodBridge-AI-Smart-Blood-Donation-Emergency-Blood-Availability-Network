# BloodBridge AI

<div align="center">
  <h3>🩸 Smart Blood Donation & Emergency Blood Availability Network</h3>
  <p>An intelligent blood donation management system that connects donors, hospitals, and blood banks through AI-powered matching and real-time coordination.</p>
</div>

![BloodBridge AI](https://img.shields.io/badge/BloodBridge-AI-red)
![Node.js](https://img.shields.io/badge/Node.js-18%2B-green)
![React](https://img.shields.io/badge/React-19-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5%2B-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 🌟 Features

### 🏥 For Hospitals
- **Smart Blood Matching**: AI-powered donor matching based on blood type, location, and urgency
- **Inventory Management**: Real-time blood inventory tracking with shortage predictions
- **Emergency Requests**: Instant blood shortage alerts and donor notifications
- **Monthly Reports**: Automated PDF reports for blood donation statistics
- **Shortage Prediction**: AI-driven forecasting for blood demand

### 👤 For Donors
- **Donor Portal**: Profile management with donation history
- **Availability Status**: Easy availability toggle for emergency situations
- **Real-time Notifications**: Instant alerts for urgent blood needs in your area
- **Smart Matching**: Location-based matching with hospitals

### 🏛️ For Administrators
- **Admin Dashboard**: Complete overview of the blood donation network
- **User Management**: Manage donors, hospitals, and system users
- **Analytics**: Comprehensive statistics and reports
- **Targeted Outreach**: Campaign system for specific blood group shortages

## 🚀 Tech Stack

- **Backend**: Node.js with Express
- **Frontend**: React 19 with Vite
- **Styling**: Tailwind CSS 4
- **Language**: TypeScript
- **Build Tools**: esbuild, tsx
- **PDF Generation**: jsPDF
- **Animations**: Motion + Canvas Confetti
- **Icons**: Lucide React

## 📦 Installation & Setup

### Prerequisites
- Node.js 18 or higher
- npm or yarn
- OpenAI API key

### Step 1: Clone the Repository
```bash
git clone https://github.com/Tanya-garg10/BloodBridge-AI-Smart-Blood-Donation-Emergency-Blood-Availability-Network.git
cd BloodBridge-AI-Smart-Blood-Donation-Emergency-Blood-Availability-Network
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Set Up Environment Variables
```bash
cp .env.example .env.local
```

Edit `.env.local` and add your OpenAI API key:
```env
OPENAI_API_KEY="your_openai_api_key_here"
APP_URL="http://localhost:3000"
```

### Step 4: Run the Development Server
```bash
npm run dev
```

The application will be available at `http://localhost:3000`

## 🔧 Available Scripts

- `npm run dev` - Start development server with hot reload
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm run preview` - Preview production build locally
- `npm run lint` - Run TypeScript type checking
- `npm run clean` - Clean build artifacts

## 🌐 Deployment

### Render (Recommended)

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

1. **Push your code to GitHub** (already done)
2. **Create a Render account** at [render.com](https://render.com)
3. **Create a new Web Service**:
   - Connect your GitHub repository: `Tanya-garg10/BloodBridge-AI-Smart-Blood-Donation-Emergency-Blood-Availability-Network`
   - Render will automatically detect the `render.yaml` configuration
4. **Configure Environment Variables**:
   - `OPENAI_API_KEY`: Your OpenAI API key
   - (Other variables are auto-configured by render.yaml)
5. **Deploy** - Render will automatically handle the build and deployment

### Manual Deployment

```bash
# Build the project
npm install --legacy-peer-deps
npm run build

# Set environment variables
export OPENAI_API_KEY="your_key_here"
export NODE_ENV="production"
export PORT="3000"

# Start the server
npm start
```

## 📡 API Endpoints

### Health & System
- `GET /api/health` - Health check and system status

### Donors
- `GET /api/donors` - List donors with filtering options
- `PATCH /api/donors/:id` - Update donor information

### Hospitals
- `GET /api/hospitals` - List registered hospitals

### Blood Inventory
- `GET /api/inventory` - View blood inventory status
- `PATCH /api/inventory/:id` - Update inventory levels

### Emergency Requests
- `GET /api/requests` - List emergency blood requests
- `POST /api/requests` - Create new emergency request
- `POST /api/requests/:id/respond` - Accept/decline requests

### Outreach & Notifications
- `POST /api/outreach` - Create donor outreach campaigns
- `GET /api/notifications` - Get user notifications
- `PATCH /api/notifications/:id/read` - Mark notification as read

### Demo
- `POST /api/demo/reset` - Reset demo data to initial state

## 📁 Project Structure

```
bloodbridge/
├── src/
│   ├── components/
│   │   ├── admin/          # Admin dashboard components
│   │   ├── common/         # Shared components (Header, Footer, etc.)
│   │   ├── donor/          # Donor-specific components
│   │   ├── hospital/       # Hospital dashboard components
│   │   └── landing/        # Landing page components
│   ├── context/            # React context providers
│   ├── data/               # Seed data and mock data
│   ├── services/           # Business logic (blood matching, PDF generation)
│   ├── App.tsx             # Main React application
│   ├── main.tsx            # Application entry point
│   ├── index.css           # Global styles
│   └── types.ts            # TypeScript type definitions
├── server.ts               # Express server and API routes
├── index.html              # Main HTML entry point
├── render.yaml             # Render deployment configuration
├── package.json            # Dependencies and scripts
├── tsconfig.json           # TypeScript configuration
├── vite.config.ts          # Vite configuration
└── README.md               # This file
```

## 🧬 Blood Matching Algorithm

The system uses a sophisticated deterministic matching algorithm that considers:

1. **Blood Compatibility** (40 points): Strict medical compatibility rules
2. **Proximity** (25 points): Distance-based scoring (closer = higher score)
3. **Availability** (15 points): Current donor availability status
4. **Eligibility** (10 points): Medical eligibility and donation history
5. **Response History** (10 points): Past donation reliability

The algorithm ensures the best possible match for emergency situations while prioritizing patient safety.

## 🐛 Troubleshooting

### Build Issues
If you encounter build errors related to peer dependencies:
```bash
npm install --legacy-peer-deps
```

### Port Already in Use
If port 3000 is already in use, you can change the port:
```bash
export PORT=3001
npm run dev
```

### Environment Variables Not Loading
Ensure your `.env.local` file is in the root directory and contains valid values.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Authors

- **Tanya Garg** - Initial work

## 🙏 Acknowledgments

- OpenAI for AI capabilities
- React and Vite communities
- Tailwind CSS for styling
- All blood donors who save lives every day

## 📞 Support

For support, please open an issue in the GitHub repository or contact the maintainers.

---

<div align="center">
  <p>Made with ❤️ to save lives through smart blood donation management</p>
  <p>BloodBridge AI - Connecting Donors, Hospitals, and Hope</p>
</div>
