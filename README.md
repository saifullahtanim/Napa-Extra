# Napa Extra — Developer Portfolio

A modern, responsive developer portfolio with a cyberpunk-inspired interface, interactive network background, project showcase cards, terminal-style CLI, animated browser tab identity, and a working contact form powered by Web3Forms.

## ✨ Features

- Responsive layout for desktop, tablet, and mobile
- Cyberpunk/glassmorphism visual design
- Animated browser tab title and neon favicon
- Interactive particle network background
  - Mouse movement interaction
  - Click-based particle burst effect
- Scroll reveal animations
- Skill progress bars
- Interactive terminal section
- 3D project card tilt effect
- Project cards with preview images
- Contact form connected to Web3Forms
- Form validation and success/error states
- Accessible labels, buttons, and navigation
- Reduced-motion support for users who prefer less animation

## 📁 Project Structure

```text
.
├── napa_extra_portfolio.html
├── README.md
└── assets/
    ├── portfolio-projects.png
    └── portfolio-showcase.png
```

## 🚀 Run Locally

The portfolio is a standalone HTML project. You can open the file directly in a browser:

```text
napa_extra_portfolio.html
```

For the best local testing experience, run it through a local server.

### Option 1: VS Code Live Server

1. Install the **Live Server** extension in VS Code.
2. Open `napa_extra_portfolio.html`.
3. Right-click the file.
4. Select **Open with Live Server**.

### Option 2: Using Node.js

Open PowerShell inside the project folder:

```powershell
cd "C:\Users\Saifulla Tanim\Downloads"
npx serve .
```

Then open the localhost URL shown in the terminal.

## 📩 Contact Form Setup

The contact form uses [Web3Forms](https://web3forms.com), so no custom backend or Gmail password is required.

### Current configuration

The form is configured to send messages to:

```text
nimpataaaa@gmail.com
```

### To create or replace an Access Key

1. Visit [web3forms.com](https://web3forms.com).
2. Sign in with the email address that should receive messages.
3. Create a new form.
4. Use your local website URL during development, or use your Vercel URL after deployment.
5. Copy the generated Access Key.
6. Open `napa_extra_portfolio.html`.
7. Find the hidden `access_key` field inside `#secure-form`.
8. Replace its value with your new key:

```html
<input type="hidden" name="access_key" value="YOUR_ACCESS_KEY">
```

Never put a Gmail password, SMTP password, OTP, or private server credential inside this HTML file.

## 🌐 Deploy to Vercel

### Using the Vercel dashboard

1. Create a GitHub repository.
2. Upload:
   - `napa_extra_portfolio.html`
   - `README.md`
   - the `assets` folder
3. Go to [vercel.com](https://vercel.com).
4. Select **Add New Project**.
5. Import your GitHub repository.
6. Keep the default framework setting if Vercel asks for one.
7. Click **Deploy**.

### Important Vercel setting

Vercel looks for an `index.html` file by default. Rename:

```text
napa_extra_portfolio.html
```

to:

```text
index.html
```

Then update the Web3Forms website URL to your deployed Vercel URL, for example:

```text
https://your-portfolio.vercel.app
```

## 🛠️ Customization

### Change the portfolio name

Search for:

```text
NAPA EXTRA
```

and replace it with your preferred name or brand.

### Change the email address

Search for:

```text
nimpataaaa@gmail.com
```

Update the Web3Forms account or form configuration if you want messages to go to a different email address.

### Change project content

Inside the `#projects` section, update:

- Project title
- Description
- Technology tags
- Status badge
- Image source
- Image alt text

### Change colors

The main theme colors are configured near the top of the file inside `tailwind.config`.

Current accent colors:

```text
Neon green: #00ff41
Cyan:       #08f7fe
Purple:     #b026ff
Red:        #ff003c
Background: #07090d
```

## 📬 How the Contact Form Works

```text
Visitor fills out the form
        ↓
Browser sends the form data to Web3Forms
        ↓
Web3Forms delivers the message
        ↓
nimpataaaa@gmail.com receives the email
```

The form does not open the visitor's email application. It sends the form data through the Web3Forms API.

## 🔐 Security Notes

- Do not add Gmail passwords to the project.
- Do not add SMTP credentials to frontend JavaScript.
- Do not publish private backend secrets in HTML.
- Keep the honeypot field enabled to reduce basic bot spam.
- If spam becomes a problem, enable additional spam protection in Web3Forms.
- Replace the Access Key if it is exposed or abused.

## 🧪 Testing Checklist

Before deployment, verify:

- Navigation links scroll to the correct sections.
- Project images load correctly.
- Mobile navigation opens and closes.
- Terminal commands respond.
- Mouse interaction works on the network background.
- Click burst effect appears on the background.
- Contact form validates empty fields.
- A test message arrives at the configured inbox.
- The deployed Vercel URL is added to Web3Forms.

## 📄 License

This project is a personal portfolio template. Customize the text, branding, colors, images, and project information for your own use.

