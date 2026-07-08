[README.html](https://github.com/user-attachments/files/29821126/README.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Milo — ACQ AI Employee Demo | README</title>
<style>
  :root {
    --sambucus: #131628;
    --indigo: #6f00ff;
    --lavender: #a08bec;
    --white: #ffffff;
    --silver: #d1d1d1;
    --silver-bg: #f4f3f7;
    --border: #e4e2ec;
  }
  * { box-sizing: border-box; }
  body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    color: var(--sambucus);
    background: var(--white);
    line-height: 1.6;
  }
  .wrap {
    max-width: 760px;
    margin: 0 auto;
    padding: 56px 24px 80px;
  }
  header {
    display: flex;
    align-items: center;
    gap: 14px;
    margin-bottom: 8px;
  }
  .mark {
    width: 34px;
    height: 34px;
    flex-shrink: 0;
  }
  h1 {
    font-size: 28px;
    font-weight: 800;
    margin: 0;
    letter-spacing: -0.01em;
  }
  h1 span { color: var(--indigo); }
  .tagline {
    color: #5b5b6b;
    font-size: 15px;
    margin: 6px 0 30px;
  }
  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 34px;
  }
  .badge {
    font-size: 11.5px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.04em;
    padding: 5px 10px;
    border-radius: 6px;
    background: var(--silver-bg);
    color: var(--sambucus);
    border: 1px solid var(--border);
  }
  .badge.accent {
    background: var(--sambucus);
    color: var(--white);
    border-color: var(--sambucus);
  }
  h2 {
    font-size: 18px;
    font-weight: 700;
    margin: 40px 0 12px;
    padding-bottom: 8px;
    border-bottom: 1px solid var(--border);
  }
  p { font-size: 14.5px; color: #2b2b38; }
  ul, ol { font-size: 14.5px; color: #2b2b38; padding-left: 20px; }
  li { margin-bottom: 6px; }
  code {
    background: var(--silver-bg);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 1px 6px;
    font-size: 13px;
    font-family: "SF Mono", Menlo, Consolas, monospace;
  }
  pre {
    background: var(--sambucus);
    color: var(--white);
    padding: 16px 18px;
    border-radius: 8px;
    overflow-x: auto;
    font-size: 13px;
    font-family: "SF Mono", Menlo, Consolas, monospace;
  }
  pre code {
    background: none;
    border: none;
    padding: 0;
    color: inherit;
  }
  .note {
    background: var(--silver-bg);
    border-left: 3px solid var(--lavender);
    padding: 12px 16px;
    border-radius: 0 8px 8px 0;
    font-size: 13.5px;
    color: #45455a;
    margin: 16px 0;
  }
  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 13.5px;
    margin: 12px 0;
  }
  th, td {
    text-align: left;
    padding: 8px 10px;
    border-bottom: 1px solid var(--border);
  }
  th {
    font-weight: 700;
    color: var(--sambucus);
    font-size: 11.5px;
    text-transform: uppercase;
    letter-spacing: 0.03em;
    color: #6b6b7d;
  }
  a { color: var(--indigo); text-decoration: none; }
  a:hover { text-decoration: underline; }
  footer {
    margin-top: 56px;
    padding-top: 20px;
    border-top: 1px solid var(--border);
    font-size: 12.5px;
    color: #8a8a9a;
    text-align: center;
  }
</style>
</head>
<body>
<div class="wrap">

  <header>
    <svg class="mark" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M50 6 L92 82 L8 82 Z" stroke="#6f00ff" stroke-width="7" stroke-linejoin="round"/>
    </svg>
    <h1>Milo <span>— ACQ AI Employee Demo</span></h1>
  </header>
  <p class="tagline">A single-file interactive demo of an AI onboarding teammate — built on Claude for the ACQ AI-First Hackathon.</p>

  <div class="badges">
    <span class="badge accent">Runs on Claude</span>
    <span class="badge">Single-file HTML</span>
    <span class="badge">No build step</span>
    <span class="badge">Demo / Prototype</span>
  </div>

  <h2>What is this?</h2>
  <p>
    Milo is a concept demo for an AI employee that onboards a new hire on day one. It's presented as a
    chat interface: a new sales associate ("Jordan Lee") can ask Milo about benefits, their 30/60/90 plan,
    tool access, expense policy, and PTO — and Milo answers as if it had already read every onboarding
    document overnight.
  </p>
  <p>
    The whole thing is one self-contained <code>.html</code> file with inline CSS and JavaScript — open it
    in a browser and it just works, no server or dependencies required.
  </p>

  <div class="note">
    This is a scripted demo build. Milo's answers are pre-written responses tied to five sample questions
    (not a live model call), meant to illustrate the intended product experience rather than a working
    integration.
  </div>

  <h2>Try it live</h2>
  <ol>
    <li>Open <code>milo-ai-employee-demo.html</code> directly in any modern browser, or</li>
    <li>Enable GitHub Pages on this repo and visit the hosted URL.</li>
  </ol>
  <p>Click one of the suggested question chips, or type your own message — any input not in the scripted set will fall back to a default response.</p>

  <h2>What it demonstrates</h2>
  <table>
    <tr><th>Feature</th><th>Details</th></tr>
    <tr><td>Sidebar profile</td><td>New hire identity, role, and a 90-day plan progress tracker</td></tr>
    <tr><td>Tool connections</td><td>Shows which of 9 onboarding tools (Slack, Gmail, Calendar, Asana, HubSpot, etc.) are already connected</td></tr>
    <tr><td>Chat interface</td><td>Conversational Q&A styled as a real AI teammate, with sourced answers</td></tr>
    <tr><td>Suggested prompts</td><td>Quick-tap chips for common first-day questions</td></tr>
  </table>

  <h2>Sample questions</h2>
  <ul>
    <li>What's my health insurance deductible?</li>
    <li>What should I focus on this week?</li>
    <li>How do I get access to my tools?</li>
    <li>Can you summarize the expense policy?</li>
    <li>Who handles PTO questions?</li>
  </ul>

  <h2>Tech stack</h2>
  <ul>
    <li>Plain HTML, CSS, and vanilla JavaScript — no frameworks, no build tools</li>
    <li>Google Fonts (Poppins) loaded via CDN</li>
    <li>Styled with ACQ's brand colors and type system</li>
  </ul>

  <h2>Repo structure</h2>
  <pre><code>.
├── milo-ai-employee-demo.html   # the entire demo (open this file)
└── README.html                  # this file
</code></pre>

  <h2>Notes / next steps</h2>
  <ul>
    <li>Wire up the input to a real Claude API call instead of the scripted response map</li>
    <li>Connect actual tools (Slack, HubSpot, Google Calendar, etc.) via MCP for live data</li>
    <li>Replace sample onboarding documents with real HR content per new hire</li>
  </ul>

  <footer>
    Built for the ACQ AI-First Hackathon · Powered by Claude
  </footer>

</div>
</body>
</html>
