# GROK_SISSY — Archival Database

🌐 **Live Site**: [https://anacondy.github.io/grok-cis/](https://anacondy.github.io/grok-cis/)

![Deploy Status](https://github.com/anacondy/grok-cis/actions/workflows/deploy.yml/badge.svg)

An archival database app for scanning and analyzing images using AI vision models. Features a cyberpunk-inspired UI optimized for high refresh rate displays (90Hz+). Supports multiple AI providers with automatic fallback.

---

## AI Providers

The app supports three providers. Set `VITE_AI_PROVIDER` to choose one — or leave it unset and the app auto-detects based on which key is present (Mistral → Gemini → xAI priority).

| Provider | Model | Env Var |
|---|---|---|
| **Mistral** (recommended) | `pixtral-large-latest` | `VITE_MISTRAL_API_KEY` |
| **Gemini** | `gemini-2.0-flash` | `VITE_GEMINI_API_KEY` |
| **xAI / Grok** | `grok-4.3` | `VITE_XAI_API_KEY` |

---

## Running Locally — Step by Step

### 1. Clone the repository

```bash
git clone https://github.com/anacondy/grok-cis.git
cd grok-cis
```

### 2. Install dependencies

```bash
npm install
```

### 3. Get an API key

Pick one (or more) of these providers:

**Mistral (recommended — free tier available)**
1. Go to [console.mistral.ai](https://console.mistral.ai/)
2. Sign up and verify your email
3. Go to **API Keys** → **Create new key**
4. Copy the key

**Gemini**
1. Go to [aistudio.google.com](https://aistudio.google.com/app/apikey)
2. Sign in with a Google account
3. Click **Create API key**
4. Copy the key

**xAI / Grok**
1. Go to [console.x.ai](https://console.x.ai/)
2. Sign up and add credits
3. Go to **API Keys** → create a key
4. Copy the key

### 4. Create your `.env` file

In the project root, create a file called `.env`:

```env
# Choose your provider: mistral | gemini | xai
VITE_AI_PROVIDER=mistral

# Add the key for your chosen provider:
VITE_MISTRAL_API_KEY=your_mistral_key_here
# VITE_GEMINI_API_KEY=your_gemini_key_here
# VITE_XAI_API_KEY=your_xai_key_here
```

You only need the key for the provider you're using. The `VITE_AI_MODEL` variable is optional — the app uses the latest recommended model for each provider automatically.

### 5. Start the dev server

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## Deploying to GitHub Pages

### 1. Fork this repository

Click **Fork** at the top right of this page.

### 2. Enable GitHub Pages

Go to your fork → **Settings** → **Pages** → set Source to **GitHub Actions**.

### 3. Add your API key as a secret

Go to **Settings** → **Secrets and variables** → **Actions** → **New repository secret**:

| Secret name | Value |
|---|---|
| `VITE_AI_PROVIDER` | `mistral` (or `gemini` or `xai`) |
| `VITE_MISTRAL_API_KEY` | your Mistral key |

Add whichever key matches your chosen provider.

### 4. Trigger a deploy

Push any change to `main`, or go to **Actions** → **Deploy to GitHub Pages** → **Run workflow**.

Your site will be live at `https://your-username.github.io/grok-cis/` in ~2 minutes.

---

## Features

- **Multi-provider AI**: Mistral, Gemini, and xAI/Grok vision models
- **Auto-detection**: Picks the right provider based on which API key is present
- **Cyberpunk UI**: Dark interface with particle effects and monospace terminal aesthetic
- **High refresh rate optimized**: Delta-time physics engine for smooth 90Hz+ displays
- **PWA ready**: Installable on mobile and desktop
- **Automated CI/CD**: GitHub Actions deploys on every push to `main`

---

## Tech Stack

- **React 18** + **Vite 5**
- **Tailwind CSS 3**
- **Lucide React** icons
- **GitHub Pages** + **GitHub Actions**

---

## Security Notes

- Never commit `.env` to the repository (it's in `.gitignore` already)
- Use GitHub Secrets for production — keys are injected only at build time
- No API keys are exposed client-side after build

---

## License

[MIT](LICENSE)
