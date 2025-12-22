# Grok Sissy - Archival Database

🌐 **Live Site**: [https://anacondy.github.io/grok-cis/](https://anacondy.github.io/grok-cis/)

![Deploy Status](https://github.com/anacondy/grok-cis/actions/workflows/deploy.yml/badge.svg)

A high-performance, archival database application for scanning and analyzing movie posters and images using Grok Vision AI. Features a cyberpunk-inspired UI optimized for high refresh rate displays (90Hz+).

## ✨ Features

- 🤖 **AI-Powered Analysis**: Uses Grok Vision AI for intelligent image recognition
- 🎨 **Cyberpunk UI**: Modern, immersive interface with particle effects
- ⚡ **High Refresh Rate Optimized**: Delta-time physics engine for smooth 90Hz+ displays
- 📱 **Progressive Web App**: Installable on mobile and desktop devices
- 🌐 **GitHub Pages Ready**: Automated CI/CD deployment pipeline

## 🖥️ Minimum Requirements

- **Browser**: Modern browser with ES2020+ support (Chrome 90+, Firefox 88+, Safari 14.1+, Edge 90+)
- **Display**: 90Hz+ refresh rate recommended for optimal experience
- **Internet**: Active connection for API calls
- **API Key**: Valid X.AI API key for Grok Vision

## 🚀 Installation

### For Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/anacondy/grok-cis.git
   cd grok-cis
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure API Key**
   
   Create a `.env` file in the root directory:
   ```env
   VITE_XAI_API_KEY=your_xai_api_key_here
   ```

4. **Start development server**
   ```bash
   npm run dev
   ```

5. **Open in browser**
   
   Navigate to `http://localhost:5173`

### For Production Build

```bash
npm run build
npm run preview
```

## ⚙️ Configuration

### API Key Setup

#### Local Development

Create a `.env` file in the project root:

```env
VITE_XAI_API_KEY=xai-xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

#### GitHub Pages Deployment

1. Go to your repository **Settings** → **Secrets and variables** → **Actions**
2. Click **New repository secret**
3. Add secret:
   - **Name**: `VITE_XAI_API_KEY`
   - **Value**: Your X.AI API key
4. Save the secret

The deployment workflow will automatically use this secret during builds.

### Getting an X.AI API Key

1. Visit [x.ai](https://x.ai/) and create an account
2. Navigate to API settings
3. Generate a new API key
4. Copy and use in your configuration

## 📸 Screenshots

### Desktop View (16:9)
*Screenshot placeholder - Desktop interface showing the archival database with scanning capabilities*

### Mobile View (20:9)
*Screenshot placeholder - Mobile-optimized view with PWA installation prompt*

## 🛠️ Technology Stack

- **Frontend Framework**: React 18.3+
- **Build Tool**: Vite 5.4+
- **Styling**: Tailwind CSS 3.4+
- **Icons**: Lucide React
- **AI Model**: Grok Vision 2 (via X.AI API)
- **Deployment**: GitHub Pages + Actions

## 📱 PWA Installation

### On Desktop

1. Open the site in Chrome/Edge
2. Click the install icon (⊕) in the address bar
3. Click "Install"

### On Mobile

1. Open the site in Safari/Chrome
2. Tap the share button
3. Select "Add to Home Screen"

## 🔄 CI/CD Pipeline

This repository uses GitHub Actions for automated deployment:

- **Deploy Workflow**: Triggers on push to `main` branch or manual dispatch
- **Maintenance Workflow**: Runs automatically every 48 hours to check dependencies and security

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.

## 🔒 Security

- Never commit API keys to the repository
- Use GitHub Secrets for production deployments
- API keys are only accessible during build time
- No client-side exposure of sensitive credentials

## 📞 Support

For issues, questions, or suggestions, please open an issue on GitHub.
