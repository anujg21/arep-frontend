# AgentGuardian — Landing Page

Marketing and early access site for [AgentGuardian](https://agentguardian.tech).

## Preview locally

```bash
open index.html
```

## Wire up the form

1. Sign up at [formspree.io](https://formspree.io) → New Form
2. Copy your form ID (e.g. `xpwzabcd`)
3. In `index.html` find and replace:
   ```js
   const FORMSPREE_ID = 'YOUR_FORM_ID';
   ```

## Wire up demo booking

1. Create an event at [calendly.com](https://calendly.com)
2. In `index.html` find the `demo-link` anchor and update `href` to your Calendly URL
