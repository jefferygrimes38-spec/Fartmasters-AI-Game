* {
  box-sizing: border-box;
}

:root {
  --bg: #0a0a0d;
  --bg-deep: #111216;
  --panel: rgba(17, 19, 23, 0.9);
  --panel-strong: rgba(27, 31, 37, 0.95);
  --line: rgba(255, 255, 255, 0.08);
  --orange: #ff8d2a;
  --orange-strong: #ff5b00;
  --gold: #ffd166;
  --red: #ff3a3a;
  --red-deep: #9d1b1b;
  --white: #f5f5f4;
  --muted: #c8c3bc;
  --green: #6ae38a;
  --shadow: rgba(0, 0, 0, 0.45);
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  min-height: 100vh;
  font-family: 'Rajdhani', sans-serif;
  background:
    radial-gradient(circle at top, rgba(255, 103, 0, 0.24), transparent 28%),
    linear-gradient(180deg, #050507 0%, #0d1014 35%, #100d0d 100%);
  color: var(--white);
}

button,
input {
  font: inherit;
}

button {
  cursor: pointer;
}

#root {
  min-height: 100vh;
}

.app-shell {
  max-width: 1440px;
  margin: 0 auto;
  padding: 24px;
}

.panel {
  background: linear-gradient(180deg, rgba(27, 31, 37, 0.9), rgba(13, 17, 20, 0.92));
  border: 1px solid var(--line);
  border-radius: 22px;
  box-shadow: 0 28px 60px var(--shadow);
  backdrop-filter: blur(12px);
}

.topbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 18px;
  padding: 18px 22px;
}

.brand-block {
  display: flex;
  align-items: center;
  gap: 16px;
}

.brand-mark {
  width: 54px;
  height: 54px;
  display: grid;
  place-items: center;
  background: linear-gradient(135deg, var(--orange), var(--red));
  border-radius: 16px;
  color: var(--white);
  font-weight: 900;
  font-size: 1.5rem;
  box-shadow: inset 0 0 18px rgba(255, 255, 255, 0.18), 0 12px 25px rgba(255, 110, 0, 0.38);
}

h1, h2, h3, h4 {
  margin: 0;
  font-family: 'Orbitron', sans-serif;
  letter-spacing: 0.04em;
}

h1 {
  font-size: clamp(1.3rem, 2vw, 2rem);
}

h2 {
  font-size: clamp(2.1rem, 4vw, 4.2rem);
  line-height: 1.05;
}

h3 {
  font-size: clamp(1.3rem, 2.5vw, 2rem);
}

.eyebrow {
  margin: 0 0 4px 0;
  font-size: 0.72rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--muted);
}

.eyebrow.accent {
  color: var(--gold);
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 22px;
  color: var(--muted);
}

.nav-links a {
  color: var(--muted);
  text-decoration: none;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  font-size: 0.74rem;
}

.header-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

.stat-pill,
.signal,
.badge {
  border-radius: 999px;
  padding: 8px 12px;
  font-size: 0.75rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.stat-pill {
  background: rgba(255, 148, 0, 0.14);
  border: 1px solid rgba(255, 148, 0, 0.35);
  color: var(--gold);
}

.signal {
  background: rgba(106, 227, 138, 0.12);
  border: 1px solid rgba(106, 227, 138, 0.32);
  color: var(--green);
}

.primary-button,
.secondary-button,
.ghost-button,
.submit-button,
.small-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border: 0;
  border-radius: 14px;
  transition: 180ms ease;
  font-weight: 700;
}

.primary-button,
.submit-button {
  background: linear-gradient(135deg, var(--orange), var(--red));
  color: var(--white);
  box-shadow: 0 18px 24px rgba(255, 86, 0, 0.2);
}

.primary-button {
  padding: 14px 22px;
  text-decoration: none;
}

.secondary-button,
.ghost-button,
.small-button {
  background: rgba(255, 255, 255, 0.03);
  color: var(--white);
  border: 1px solid var(--line);
}

.secondary-button,
.ghost-button {
  padding: 12px 18px;
}

.submit-button {
  width: 100%;
  padding: 16px 18px;
  margin-top: 18px;
  font-size: 1rem;
}

.small-button {
  padding: 9px 14px;
}

.page-grid {
  margin-top: 24px;
  display: grid;
  gap: 24px;
}

.hero {
  display: grid;
  grid-template-columns: 1.5fr 0.9fr;
  gap: 20px;
  padding: 18px 18px 22px;
}

.hero-copy {
  padding: 12px 12px 0;
}

.hero-copy p:not(.eyebrow) {
  color: var(--muted);
  line-height: 1.65;
  max-width: 680px;
  font-size: 1.1rem;
}

.hero-actions {
  display: flex;
  align-items: center;
  gap: 14px;
  margin-top: 18px;
}

.kpis {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 14px;
  margin-top: 26px;
}

.kpis > div,
.wallet-card,
.owner-card,
.average-box {
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid var(--line);
  border-radius: 16px;
  padding: 14px 16px;
}

.kpis > div {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.kpis span,
.wallet-card span,
.owner-card span {
  color: var(--muted);
  font-size: 0.72rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
}

.kpis strong,
.wallet-card strong,
.owner-card strong,
.average-box strong {
  font-size: 1.7rem;
  letter-spacing: 0.02em;
}

.podium {
  background: linear-gradient(180deg, rgba(20, 23, 27, 0.96), rgba(11, 14, 17, 0.96));
  border-radius: 20px;
  padding: 16px 14px 18px;
}

.panel-inner {
  border: 1px solid var(--line);
  background: rgba(255, 255, 255, 0.02);
}

.podium-head {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: var(--gold);
  letter-spacing: 0.12em;
  text-transform: uppercase;
  font-size: 0.7rem;
  padding: 0 8px 14px;
}

.podium-row {
  display: grid;
  grid-template-columns: auto 1fr auto;
  gap: 12px;
  align-items: center;
  padding: 12px 10px;
  border-radius: 14px;
  border: 1px solid var(--line);
  background: rgba(255, 255, 255, 0.02);
  margin-top: 10px;
}

.rank-badge {
  width: 38px;
  height: 38px;
  border-radius: 12px;
  display: grid;
  place-items: center;
  font-weight: 900;
  background: linear-gradient(135deg, var(--orange), var(--red));
  color: var(--white);
}

.podium-row strong,
.leader-meta strong {
  display: block;
  font-size: 1.05rem;
}

.podium-row small,
.leader-meta small {
  color: var(--muted);
  font-size: 0.76rem;
}

.podium-score {
  font-family: 'Orbitron', sans-serif;
  color: var(--gold);
  font-size: 1.5rem;
  font-weight: 800;
}

.content-grid {
  display: grid;
  grid-template-columns: 1.5fr 0.7fr;
  gap: 24px;
}

.submit-panel,
.right-rail,
.leaderboard-panel,
.competition-panel,
.store-panel,
.owner-panel {
  padding: 20px;
}

.panel-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
  margin-bottom: 18px;
}

.field-row {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 14px;
  margin-bottom: 18px;
}

label {
  display: flex;
  flex-direction: column;
  gap: 8px;
  color: var(--muted);
  font-size: 0.83rem;
  text-transform: uppercase;
  letter-spacing: 0.12em;
}

input {
  width: 100%;
  border: 1px solid var(--line);
  border-radius: 12px;
  background: rgba(255, 255, 255, 0.02);
  color: var(--white);
  padding: 12px 14px;
  outline: none;
}

.record-wrap {
  margin-top: 14px;
  border: 1px solid var(--line);
  border-radius: 18px;
  background: rgba(255, 255, 255, 0.02);
  padding: 18px;
}

.recording-visual {
  display: grid;
  place-items: center;
  min-height: 118px;
}

.pulse {
  width: 110px;
  height: 110px;
  border-radius: 50%;
  border: 2px solid rgba(255, 148, 0, 0.8);
  background: radial-gradient(circle, rgba(255, 164, 0, 0.3), rgba(255, 78, 0, 0.05));
  box-shadow: 0 0 0 12px rgba(255, 146, 0, 0.08), 0 0 34px rgba(255, 103, 0, 0.22);
}

.pulse.live {
  animation: heartbeat 0.8s infinite alternate;
}

@keyframes heartbeat {
  from {
    transform: scale(0.96);
    box-shadow: 0 0 0 10px rgba(255, 146, 0, 0.08), 0 0 20px rgba(255, 103, 0, 0.22);
  }
  to {
    transform: scale(1.1);
    box-shadow: 0 0 0 18px rgba(255, 146, 0, 0.04), 0 0 38px rgba(255, 103, 0, 0.32);
  }
}

.record-buttons {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-top: 10px;
}

.audio-panel {
  margin-top: 18px;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

audio {
  width: 100%;
}

.clip-meta {
  display: flex;
  justify-content: space-between;
  color: var(--muted);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  font-size: 0.7rem;
}

.purchase-list {
  display: grid;
  gap: 12px;
}

.purchase-card {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  text-align: left;
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid var(--line);
  border-radius: 16px;
  padding: 16px;
  color: var(--white);
}

.purchase-card strong,
.purchase-card small {
  display: block;
}

.purchase-card strong {
  font-size: 1.1rem;
}

.purchase-card small {
  margin-top: 6px;
  color: var(--muted);
}

.badge {
  display: inline-block;
  background: rgba(255, 166, 0, 0.08);
  border: 1px solid rgba(255, 166, 0, 0.24);
  color: var(--gold);
  margin-bottom: 8px;
}

.badge.dark {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid var(--line);
  color: var(--muted);
}

.wallet-card {
  margin-top: 18px;
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.wallet-card.mini {
  margin-top: 0;
}

.judges-panel {
  margin-top: 18px;
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 12px;
}

.judge-card {
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid var(--line);
  border-radius: 14px;
  padding: 12px 10px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}

.average-box {
  grid-column: span 2;
}

.commentary-box {
  grid-column: 1 / -1;
  border-radius: 16px;
  border: 1px solid var(--line);
  background: rgba(255, 255, 255, 0.02);
  padding: 14px 16px;
  margin-top: 4px;
}

.commentary-box p {
  margin: 10px 0 0 0;
  color: var(--muted);
  line-height: 1.5;
}

.leaderboard-table {
  display: grid;
  gap: 14px;
}

.leader-row {
  display: grid;
  grid-template-columns: 70px minmax(160px, 1fr) 100px 1.2fr auto;
  gap: 14px;
  align-items: center;
  padding: 14px 16px;
  border: 1px solid var(--line);
  border-radius: 18px;
  background: rgba(255, 255, 255, 0.02);
}

.leader-rank {
  width: 56px;
  height: 56px;
  border-radius: 16px;
  display: grid;
  place-items: center;
  background: linear-gradient(135deg, rgba(255, 141, 42, 0.18), rgba(255, 58, 58, 0.18));
  border: 1px solid rgba(255, 141, 42, 0.3);
  font-weight: 900;
  color: var(--gold);
}

.leader-score {
  font-family: 'Orbitron', sans-serif;
  color: var(--gold);
  font-size: 1.3rem;
  font-weight: 700;
}

.leader-commentary {
  color: var(--muted);
  font-size: 0.9rem;
  line-height: 1.4;
}

.mini-audio {
  width: 140px;
}

.competition-list,
.store-grid,
.owner-stats {
  display: grid;
  gap: 16px;
}

.competition-list {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.competition-card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 12px;
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid var(--line);
  border-radius: 18px;
  padding: 16px;
}

.competition-card h4 {
  font-size: 1.1rem;
  margin-top: 10px;
}

.competition-stats {
  display: flex;
  justify-content: space-between;
  gap: 14px;
  color: var(--muted);
  font-size: 0.9rem;
}

.store-grid {
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.store-card {
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid var(--line);
  border-radius: 18px;
  padding: 16px;
}

.store-card.active {
  border-color: rgba(255, 140, 0, 0.75);
  box-shadow: inset 0 0 0 1px rgba(255, 140, 0, 0.34);
}

.store-card h4 {
  font-size: 1.1rem;
  margin-top: 14px;
}

.store-card p {
  margin: 10px 0 12px;
  color: var(--muted);
  min-height: 48px;
}

.store-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  color: var(--muted);
}

.store-avatar {
  width: 72px;
  height: 72px;
  border-radius: 18px;
  background: linear-gradient(135deg, var(--orange), var(--red));
  box-shadow: 0 20px 30px rgba(255, 96, 0, 0.18);
}

.store-avatar.red {
  background: linear-gradient(135deg, #ff5e5b, #db2a2a);
}

.store-avatar.gold {
  background: linear-gradient(135deg, #ffd166, #ff9f1c);
}

.store-avatar.chrome {
  background: linear-gradient(135deg, #d7dbe0, #7e8994);
}

.owner-input-block {
  display: flex;
  gap: 12px;
  margin-bottom: 18px;
}

.owner-input-block input {
  flex: 1;
}

.owner-stats {
  grid-template-columns: repeat(4, minmax(0, 1fr));
}

.owner-card {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.toast {
  position: fixed;
  right: 18px;
  bottom: 18px;
  padding: 12px 18px;
  border-radius: 999px;
  background: rgba(15, 17, 20, 0.92);
  border: 1px solid rgba(255, 255, 255, 0.12);
  color: var(--white);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.38);
}

@media (max-width: 980px) {
  .topbar,
  .nav-links,
  .header-actions,
  .hero,
  .content-grid,
  .competition-list,
  .store-grid,
  .owner-stats {
    grid-template-columns: 1fr;
    display: grid;
  }

  .topbar {
    align-items: flex-start;
  }

  .nav-links,
  .header-actions {
    display: flex;
    flex-wrap: wrap;
  }

  .kpis,
  .judges-panel,
  .field-row {
    grid-template-columns: 1fr;
  }

  .leader-row {
    grid-template-columns: 56px 1fr;
  }

  .leader-score,
  .leader-commentary,
  .mini-audio {
    grid-column: 2;
  }
}

@media (max-width: 640px) {
  .app-shell {
    padding: 16px;
  }

  .hero,
  .submit-panel,
  .right-rail,
  .leaderboard-panel,
  .competition-panel,
  .store-panel,
  .owner-panel {
    padding: 16px;
  }

  .hero-actions,
  .record-buttons,
  .owner-input-block {
    flex-direction: column;
    align-items: stretch;
  }

  .primary-button,
  .secondary-button,
  .ghost-button,
  .submit-button {
    width: 100%;
  }
}

































































































