* {
  box-sizing: border-box;
}

:root {
  --bg: #0d0f12;
  --panel: #141a1d;
  --panel-alt: #1a2329;
  --sidebar: #182326;
  --soft: #cfe4d6;
  --text: #ecf4ef;
  --muted: #97a7a0;
  --primary: #62d59d;
  --primary-deep: #3ca876;
  --secondary: #2a3740;
  --border: rgba(255, 255, 255, 0.08);
  --shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
}

html, body, #root {
  margin: 0;
  min-height: 100%;
  min-width: 100%;
  font-family: 'Inter', sans-serif;
  background: linear-gradient(135deg, #0f1518 0%, #0d0f12 100%);
  color: var(--text);
}

body {
  min-height: 100vh;
}

button, textarea, select {
  font: inherit;
}

button {
  cursor: pointer;
}

.app-shell {
  display: grid;
  grid-template-columns: 280px 1fr;
  min-height: 100vh;
}

.sidebar {
  background: rgba(24, 35, 38, 0.94);
  border-right: 1px solid var(--border);
  padding: 24px 18px;
}

.brand-block {
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 6px 8px 22px;
}

.brand-mark {
  width: 54px;
  height: 54px;
  border-radius: 18px;
  background: #5f7d64;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #0a0c0d;
  box-shadow: inset 0 0 0 2px rgba(0,0,0,0.18);
}

.brand-mark svg {
  width: 42px;
  height: 42px;
}

.brand-block h1 {
  margin: 0;
  font-size: 1.5rem;
  letter-spacing: -0.06em;
}

.brand-block p {
  margin: 4px 0 0;
  color: var(--muted);
  font-size: 0.76rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
}

.nav-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-top: 16px;
}

.nav-item {
  background: transparent;
  color: var(--text);
  border: 1px solid transparent;
  border-radius: 12px;
  padding: 12px 14px;
  text-align: left;
  transition: 0.2s ease;
  font-weight: 600;
}

.nav-item:hover,
.nav-item.active {
  background: rgba(98, 213, 157, 0.12);
  border-color: rgba(98, 213, 157, 0.35);
  color: var(--primary);
}

.main-panel {
  padding: 28px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.topbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 6px 0 0;
}

.eyebrow {
  margin: 0 0 6px;
  color: var(--muted);
  text-transform: uppercase;
  letter-spacing: 0.12em;
  font-size: 0.7rem;
}

.topbar h2 {
  margin: 0;
  font-size: clamp(1.8rem, 2vw, 2.4rem);
  letter-spacing: -0.08em;
}

.status-pill {
  background: rgba(98, 213, 157, 0.12);
  color: var(--primary);
  padding: 8px 14px;
  border-radius: 999px;
  border: 1px solid rgba(98, 213, 157, 0.24);
  font-weight: 700;
}

.content-card {
  background: rgba(20, 26, 29, 0.96);
  border: 1px solid var(--border);
  border-radius: 24px;
  box-shadow: var(--shadow);
  min-height: 620px;
  overflow: hidden;
}

.panel {
  padding: 18px;
  height: 100%;
}

.chat-panel {
  display: flex;
  flex-direction: column;
  gap: 16px;
  height: 100%;
}

.chat-window {
  flex: 1;
  overflow: auto;
  display: flex;
  flex-direction: column;
  gap: 12px;
  padding: 6px 10px 0;
}

.message {
  max-width: 75%;
  border-radius: 18px;
  padding: 14px 16px;
  border: 1px solid var(--border);
}

.message.user {
  margin-left: auto;
  background: rgba(98, 213, 157, 0.14);
  border-color: rgba(98, 213, 157, 0.28);
}

.message.assistant {
  background: rgba(255,255,255,0.02);
}

.role {
  display: block;
  font-size: 0.7rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--muted);
  margin-bottom: 6px;
}

.message p {
  margin: 0;
  line-height: 1.6;
  color: var(--text);
}

.composer {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

textarea,
select {
  width: 100%;
  border-radius: 16px;
  border: 1px solid rgba(255,255,255,0.08);
  background: rgba(19, 24, 28, 0.9);
  color: var(--text);
  padding: 14px 16px;
  resize: vertical;
}

textarea {
  min-height: 110px;
}

.composer-actions,
.code-toolbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
}

.primary,
.secondary {
  border: none;
  border-radius: 12px;
  padding: 11px 18px;
  font-weight: 700;
  transition: transform 0.2s ease;
}

.primary {
  background: linear-gradient(135deg, var(--primary) 0%, var(--primary-deep) 100%);
  color: #07110d;
}

.secondary {
  background: var(--secondary);
  color: var(--text);
}

.primary:hover,
.secondary:hover {
  transform: translateY(-1px);
}

.preview-box {
  height: 240px;
  border-radius: 18px;
  overflow: hidden;
  border: 1px solid var(--border);
  background: linear-gradient(135deg, rgba(92, 113, 119, 0.4), rgba(28, 33, 36, 0.9));
  margin-bottom: 18px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.preview-art {
  width: 72%;
  height: 72%;
  background: radial-gradient(circle at center, rgba(255,255,255,0.8), rgba(98,213,157,0.25) 30%, rgba(13,14,17,0.6) 70%);
  border-radius: 24px;
  border: 1px solid rgba(255,255,255,0.14);
  box-shadow: inset 0 0 40px rgba(98, 213, 157, 0.18);
}

.video-scene {
  width: 85%;
  height: 72%;
  border-radius: 24px;
  background: linear-gradient(180deg, #183442, #0e151b 60%, #06080a);
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid rgba(255,255,255,0.08);
}

.video-scene span {
  font-size: 1.4rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #bfeee2;
}

.prompt-box {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.code-panel {
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.code-toolbar {
  display: flex;
  justify-content: space-between;
  align-items: end;
}

.code-toolbar label {
  display: flex;
  flex-direction: column;
  gap: 10px;
  color: var(--muted);
  font-size: 0.8rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  min-width: 180px;
}

.code-block {
  margin: 0;
  background: rgba(7, 12, 15, 0.9);
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 20px;
  color: #d8f5e5;
  line-height: 1.7;
  overflow: auto;
}

.billboard-panel {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 18px;
  height: 100%;
}

.billboard-box {
  min-height: 260px;
  border-radius: 22px;
  background: linear-gradient(135deg, #d7ebdf 0%, #b5d9c1 100%);
  color: #08120e;
  padding: 24px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.billboard-box .label {
  display: inline-block;
  margin-bottom: 18px;
  text-transform: uppercase;
  letter-spacing: 0.14em;
  font-size: 0.72rem;
  font-weight: 700;
}

.billboard-box p {
  margin: 0;
  font-size: clamp(1.2rem, 2vw, 1.9rem);
  line-height: 1.5;
  font-weight: 700;
}

.status-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 14px;
  background: rgba(12, 19, 20, 0.94);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 14px 18px;
  color: var(--muted);
}

@media (max-width: 900px) {
  .app-shell {
    grid-template-columns: 1fr;
  }

  .sidebar {
    border-right: none;
    border-bottom: 1px solid var(--border);
  }

  .nav-list {
    flex-direction: row;
    flex-wrap: wrap;
  }

  .main-panel {
    padding: 18px;
  }
}
