index.html



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
  <title>WriteForMoney · Apply & Earn</title>
  <!-- Font Awesome 6 (free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    /* ---------- RESET & GLOBAL ---------- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
    }

    body {
      background: #f8f9fc;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    /* ---------- BRAND COLORS (writing / editorial palette) ---------- */
    :root {
      --primary: #2c3e50;        /* deep navy – professional */
      --primary-light: #34495e;
      --accent: #e67e22;         /* warm orange – call to action */
      --accent-dark: #d35400;
      --accent-soft: #fef5e7;
      --text-dark: #1e1e2f;
      --text-gray: #6b7280;
      --text-light: #9ca3af;
      --white: #ffffff;
      --border: #e5e7eb;
      --success: #059669;
      --success-bg: #ecfdf5;
      --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.04), 0 1px 2px rgba(0, 0, 0, 0.02);
      --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.05), 0 2px 4px rgba(0, 0, 0, 0.03);
      --shadow-lg: 0 10px 40px rgba(0, 0, 0, 0.08);
      --radius-card: 16px;
      --radius-button: 12px;
      --radius-pill: 999px;
    }

    /* ---------- HEADER ---------- */
    .header {
      background: var(--white);
      padding: 0.9rem 1.5rem;
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      gap: 1rem 2rem;
      box-shadow: var(--shadow-sm);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 50;
    }

    .logo-area {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .logo-icon {
      background: linear-gradient(135deg, var(--accent), var(--accent-dark));
      width: 40px;
      height: 40px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.3rem;
      color: white;
    }

    .logo-text {
      font-size: 1.35rem;
      font-weight: 800;
      color: var(--primary);
      letter-spacing: -0.5px;
    }

    .logo-text span {
      color: var(--accent);
    }

    .nav-links {
      display: flex;
      gap: 1.8rem;
      margin-left: auto;
      align-items: center;
    }

    .nav-links a {
      color: var(--text-gray);
      text-decoration: none;
      font-weight: 500;
      font-size: 0.92rem;
      transition: color 0.2s;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .nav-links a:hover {
      color: var(--accent);
    }

    .nav-links a i {
      font-size: 0.95rem;
    }

    .user-badge {
      background: var(--accent-soft);
      color: var(--accent-dark);
      border-radius: var(--radius-pill);
      padding: 6px 14px;
      font-size: 0.8rem;
      font-weight: 700;
    }

    /* ---------- MAIN CONTAINER ---------- */
    .main-container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 2rem 1.5rem 3rem;
      width: 100%;
      flex: 1;
    }

    /* hero / title section */
    .career-hero {
      text-align: center;
      margin-bottom: 2.2rem;
    }

    .career-hero h1 {
      font-size: 2.3rem;
      font-weight: 800;
      color: var(--primary);
      letter-spacing: -0.03em;
      line-height: 1.2;
    }

    .career-hero h1 i {
      color: var(--accent);
      margin-right: 10px;
    }

    .career-hero .subhead {
      color: var(--text-gray);
      font-size: 1.05rem;
      margin-top: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 12px;
      flex-wrap: wrap;
    }

    .fee-badge {
      background: var(--accent-soft);
      border: 1px solid #fde68a;
      padding: 6px 18px;
      border-radius: var(--radius-pill);
      color: var(--accent-dark);
      font-weight: 600;
      font-size: 0.9rem;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .fee-badge i {
      color: var(--accent);
    }

    /* stats strip */
    .stats-strip {
      display: flex;
      justify-content: center;
      gap: 2.5rem;
      flex-wrap: wrap;
      margin: 1.8rem 0 2.4rem;
      padding: 1.2rem 1.5rem;
      background: white;
      border-radius: var(--radius-card);
      box-shadow: var(--shadow-sm);
      border: 1px solid var(--border);
    }

    .stat-item {
      text-align: center;
    }

    .stat-item .stat-value {
      font-size: 1.5rem;
      font-weight: 800;
      color: var(--primary);
      letter-spacing: -0.02em;
    }

    .stat-item .stat-label {
      font-size: 0.82rem;
      color: var(--text-gray);
      font-weight: 500;
      margin-top: 2px;
    }

    /* ---------- JOB GRID ---------- */
    .section-label {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 1.2rem;
      flex-wrap: wrap;
      gap: 10px;
    }

    .section-label h2 {
      font-size: 1.25rem;
      font-weight: 700;
      color: var(--primary);
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .section-label h2 i {
      color: var(--accent);
      font-size: 1.1rem;
    }

    .section-label .count-pill {
      background: var(--accent-soft);
      color: var(--accent-dark);
      font-size: 0.78rem;
      font-weight: 700;
      padding: 4px 12px;
      border-radius: var(--radius-pill);
    }

    .jobs-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(310px, 1fr));
      gap: 1.5rem;
    }

    /* job card */
    .job-card {
      background: var(--white);
      border-radius: var(--radius-card);
      padding: 1.5rem 1.5rem 1.4rem;
      box-shadow: var(--shadow-sm);
      transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s;
      display: flex;
      flex-direction: column;
      border: 1px solid var(--border);
      position: relative;
    }

    .job-card:hover {
      transform: translateY(-4px);
      box-shadow: var(--shadow-md);
      border-color: #fcd9b0;
    }

    .job-header {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      margin-bottom: 1rem;
      gap: 10px;
    }

    .job-icon {
      background: var(--accent-soft);
      width: 48px;
      height: 48px;
      border-radius: 14px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--accent);
      font-size: 1.4rem;
      flex-shrink: 0;
    }

    .fee-tag {
      background: var(--accent-soft);
      border-radius: var(--radius-pill);
      padding: 6px 12px;
      font-size: 0.75rem;
      font-weight: 700;
      color: var(--accent-dark);
      letter-spacing: 0.2px;
      border: 1px solid #fde68a;
      white-space: nowrap;
      display: flex;
      align-items: center;
      gap: 5px;
    }

    .fee-tag i {
      font-size: 0.7rem;
    }

    .job-title {
      font-size: 1.18rem;
      font-weight: 700;
      color: var(--text-dark);
      margin-bottom: 6px;
      line-height: 1.35;
    }

    .job-meta-row {
      display: flex;
      align-items: center;
      gap: 1rem;
      flex-wrap: wrap;
      margin-bottom: 0.9rem;
      font-size: 0.82rem;
      color: var(--text-gray);
    }

    .job-meta-row span {
      display: flex;
      align-items: center;
      gap: 5px;
    }

    .job-meta-row i {
      color: var(--accent);
      font-size: 0.8rem;
    }

    .job-desc {
      color: #4b5563;
      font-size: 0.92rem;
      line-height: 1.55;
      margin-bottom: 1.2rem;
      flex: 1;
    }

    .job-footer {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 1rem;
      gap: 10px;
    }

    .pay-rate {
      font-size: 0.88rem;
      font-weight: 700;
      color: var(--success);
      display: flex;
      align-items: center;
      gap: 5px;
    }

    .pay-rate i {
      font-size: 0.8rem;
    }

    .job-type-tag {
      background: #f3f4f6;
      padding: 4px 10px;
      border-radius: var(--radius-pill);
      font-size: 0.75rem;
      font-weight: 600;
      color: var(--text-gray);
    }

    .apply-btn {
      background: var(--accent);
      border: none;
      color: #ffffff;
      font-weight: 700;
      padding: 0.85rem 1.2rem;
      border-radius: var(--radius-button);
      font-size: 0.95rem;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      cursor: pointer;
      transition: background 0.2s ease, transform 0.1s ease, box-shadow 0.2s;
      width: 100%;
      letter-spacing: 0.2px;
      box-shadow: 0 2px 8px rgba(230, 126, 34, 0.25);
    }

    .apply-btn i {
      font-size: 0.9rem;
    }

    .apply-btn:hover {
      background: var(--accent-dark);
      box-shadow: 0 4px 14px rgba(230, 126, 34, 0.35);
    }

    .apply-btn:active {
      transform: scale(0.98);
    }

    .apply-btn.paid {
      background: var(--success);
      box-shadow: 0 2px 8px rgba(5, 150, 105, 0.25);
      pointer-events: none;
      opacity: 0.95;
    }

    .apply-btn.paid i {
      color: white;
    }

    .card-ribbon {
      position: absolute;
      top: 1rem;
      right: 1rem;
      background: var(--success-bg);
      color: var(--success);
      font-size: 0.68rem;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      padding: 3px 9px;
      border-radius: var(--radius-pill);
      border: 1px solid #a7f3d0;
      display: none;
    }

    .job-card.applied .card-ribbon {
      display: block;
    }

    /* ---------- PAYMENT MODAL ---------- */
    .modal-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(15, 23, 42, 0.55);
      backdrop-filter: blur(5px);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 1000;
      padding: 1.5rem;
      opacity: 0;
      visibility: hidden;
      transition: opacity 0.25s ease, visibility 0.25s;
    }

    .modal-overlay.active {
      opacity: 1;
      visibility: visible;
    }

    .modal-card {
      background: white;
      max-width: 460px;
      width: 100%;
      border-radius: 24px;
      padding: 1.8rem 1.8rem 1.6rem;
      box-shadow: var(--shadow-lg);
      transform: translateY(14px);
      transition: transform 0.3s ease;
      max-height: 92vh;
      overflow-y: auto;
    }

    .modal-overlay.active .modal-card {
      transform: translateY(0);
    }

    .modal-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 0.4rem;
      gap: 10px;
    }

    .modal-header h3 {
      font-size: 1.35rem;
      font-weight: 800;
      color: var(--primary);
      display: flex;
      align-items: center;
      gap: 10px;
      letter-spacing: -0.02em;
    }

    .modal-header h3 i {
      color: var(--accent);
      font-size: 1.1rem;
    }

    .close-modal {
      background: #f3f4f6;
      border: none;
      font-size: 1.2rem;
      cursor: pointer;
      color: var(--text-gray);
      transition: all 0.15s;
      line-height: 1;
      width: 34px;
      height: 34px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }

    .close-modal:hover {
      background: #fee2e2;
      color: #dc2626;
    }

    .modal-job-title {
      color: var(--text-gray);
      font-size: 0.9rem;
      margin-bottom: 1.1rem;
      line-height: 1.4;
    }

    .modal-job-title strong {
      color: var(--text-dark);
    }

    .payment-detail {
      background: #f9fafb;
      border-radius: 14px;
      padding: 0.9rem 1.1rem;
      margin: 0.8rem 0 1.1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border: 1px dashed #d1d5db;
    }

    .payment-detail span:first-child {
      color: var(--text-gray);
      font-size: 0.9rem;
      font-weight: 500;
    }

    .payment-detail .amount {
      font-weight: 800;
      font-size: 1.35rem;
      color: var(--primary);
      letter-spacing: -0.02em;
    }

    .payment-detail .amount small {
      font-size: 0.8rem;
      font-weight: 600;
      color: var(--text-gray);
      margin-left: 4px;
    }

    .modal-input-group {
      margin-bottom: 0.9rem;
    }

    .modal-input-group label {
      font-weight: 600;
      font-size: 0.82rem;
      display: block;
      margin-bottom: 6px;
      color: var(--text-dark);
    }

    .modal-input-group input {
      width: 100%;
      padding: 0.8rem 1rem;
      border: 1.5px solid var(--border);
      border-radius: 12px;
      font-size: 0.95rem;
      transition: 0.2s;
      background: #fafafa;
      color: var(--text-dark);
    }

    .modal-input-group input:focus {
      border-color: var(--accent);
      outline: none;
      background: white;
      box-shadow: 0 0 0 3px rgba(230, 126, 34, 0.1);
    }

    .pay-btn {
      background: var(--accent);
      border: none;
      width: 100%;
      padding: 0.95rem;
      font-weight: 700;
      font-size: 1rem;
      border-radius: var(--radius-button);
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      cursor: pointer;
      margin-top: 0.4rem;
      transition: background 0.2s;
      color: white;
      box-shadow: 0 2px 8px rgba(230, 126, 34, 0.25);
    }

    .pay-btn:hover {
      background: var(--accent-dark);
    }

    .pay-btn i {
      font-size: 0.9rem;
    }

    .secure-note {
      text-align: center;
      font-size: 0.76rem;
      color: var(--text-light);
      margin-top: 0.9rem;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
    }

    /* toast message */
    .toast-msg {
      position: fixed;
      bottom: 24px;
      left: 50%;
      transform: translateX(-50%) translateY(80px);
      background: var(--primary);
      color: white;
      font-weight: 500;
      padding: 12px 24px;
      border-radius: var(--radius-pill);
      font-size: 0.9rem;
      box-shadow: var(--shadow-lg);
      opacity: 0;
      transition: transform 0.35s ease, opacity 0.3s;
      z-index: 1200;
      white-space: nowrap;
      pointer-events: none;
      display: flex;
      align-items: center;
      gap: 8px;
      max-width: 92vw;
      overflow: hidden;
      text-overflow: ellipsis;
    }

    .toast-msg.show {
      opacity: 1;
      transform: translateX(-50%) translateY(0);
    }

    .toast-msg i {
      color: var(--accent);
      flex-shrink: 0;
    }

    /* ---------- FOOTER ---------- */
    .footer {
      background: white;
      border-top: 1px solid var(--border);
      padding: 2rem 1.5rem 1.5rem;
      margin-top: 1.5rem;
      text-align: center;
      color: var(--text-gray);
      font-size: 0.88rem;
    }

    .footer .footer-links {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 1.8rem;
      margin-bottom: 1.1rem;
    }

    .footer a {
      color: var(--text-gray);
      text-decoration: none;
      transition: 0.15s;
    }

    .footer a:hover {
      color: var(--accent);
    }

    /* ---------- RESPONSIVE ---------- */
    @media (max-width: 720px) {
      .header {
        padding: 0.8rem 1rem;
        gap: 0.7rem;
      }

      .logo-text {
        font-size: 1.15rem;
      }

      .logo-icon {
        width: 34px;
        height: 34px;
        font-size: 1.1rem;
        border-radius: 10px;
      }

      .nav-links {
        gap: 1.2rem;
        margin-left: 0;
        width: 100%;
        justify-content: space-between;
      }

      .nav-links a {
        font-size: 0.82rem;
      }

      .main-container {
        padding: 1.5rem 1rem 2rem;
      }

      .career-hero h1 {
        font-size: 1.75rem;
      }

      .career-hero .subhead {
        font-size: 0.95rem;
        flex-direction: column;
        gap: 8px;
      }

      .stats-strip {
        gap: 1.5rem;
        padding: 1rem;
      }

      .stat-item .stat-value {
        font-size: 1.25rem;
      }

      .jobs-grid {
        gap: 1.1rem;
      }

      .job-card {
        padding: 1.2rem;
      }

      .modal-card {
        padding: 1.5rem;
      }
    }

    @media (max-width: 400px) {
      .nav-links {
        flex-wrap: wrap;
        justify-content: center;
        gap: 0.9rem;
      }

      .job-title {
        font-size: 1.08rem;
      }

      .fee-tag {
        font-size: 0.68rem;
        padding: 4px 9px;
      }

      .job-meta-row {
        gap: 0.6rem;
        font-size: 0.78rem;
      }

      .section-label h2 {
        font-size: 1.1rem;
      }
    }

    /* success pulse animation */
    @keyframes pulseSuccess {
      0% { box-shadow: 0 0 0 0 rgba(5, 150, 105, 0.4); }
      70% { box-shadow: 0 0 0 12px rgba(5, 150, 105, 0); }
      100% { box-shadow: 0 0 0 0 rgba(5, 150, 105, 0); }
    }

    .apply-btn.paid {
      animation: pulseSuccess 0.6s ease;
    }
  </style>
</head>
<body>
  <!-- HEADER -->
  <header class="header">
    <div class="logo-area">
      <div class="logo-icon"><i class="fas fa-feather-alt"></i></div>
      <div class="logo-text">Write<span>ForMoney</span></div>
    </div>
    <div class="nav-links">
      <a href="#"><i class="fas fa-search"></i> Browse Jobs</a>
      <a href="#"><i class="fas fa-star"></i> Top Writers</a>
      <a href="#"><i class="fas fa-user"></i> Dashboard</a>
      <span class="user-badge"><i class="fas fa-wallet" style="margin-right:4px;"></i> $0.00</span>
    </div>
  </header>

  <!-- MAIN CONTENT -->
  <main class="main-container">
    <!-- Hero -->
    <div class="career-hero">
      <h1><i class="fas fa-pen-fancy"></i> Get paid to write</h1>
      <div class="subhead">
        <span class="fee-badge"><i class="fas fa-lock"></i> Application fee: $7.99 (one-time)</span>
        <span>Pay & apply — start earning today</span>
      </div>
    </div>

    <!-- Stats strip -->
    <div class="stats-strip">
      <div class="stat-item">
        <div class="stat-value">1,240+</div>
        <div class="stat-label">Active jobs</div>
      </div>
      <div class="stat-item">
        <div class="stat-value">$0.08</div>
        <div class="stat-label">Per word avg.</div>
      </div>
      <div class="stat-item">
        <div class="stat-value">48h</div>
        <div class="stat-label">Avg. payout</div>
      </div>
      <div class="stat-item">
        <div class="stat-value">100%</div>
        <div class="stat-label">Remote</div>
      </div>
    </div>

    <!-- Section label -->
    <div class="section-label">
      <h2><i class="fas fa-briefcase"></i> Open writing positions</h2>
      <span class="count-pill" id="jobCountPill">6 jobs</span>
    </div>

    <!-- Job grid -->
    <div class="jobs-grid" id="jobsGrid">
      <!-- Job cards injected by JavaScript -->
    </div>
  </main>

  <!-- PAYMENT MODAL -->
  <div class="modal-overlay" id="paymentModal">
    <div class="modal-card">
      <div class="modal-header">
        <h3><i class="fas fa-credit-card"></i> Pay application fee</h3>
        <button class="close-modal" id="closeModalBtn" aria-label="Close">&times;</button>
      </div>
      <p class="modal-job-title">
        You are applying for <strong id="jobTitleModal">this position</strong>
      </p>
      <div class="payment-detail">
        <span>Application fee</span>
        <span class="amount">$7.99 <small>USD</small></span>
      </div>
      <div class="modal-input-group">
        <label for="cardNumberInput">Card number</label>
        <input type="text" id="cardNumberInput" placeholder="4242 4242 4242 4242" maxlength="19" autocomplete="cc-number">
      </div>
      <div class="modal-input-group">
        <label for="cardNameInput">Full name on card</label>
        <input type="text" id="cardNameInput" placeholder="John Doe" autocomplete="cc-name">
      </div>
      <button class="pay-btn" id="confirmPaymentBtn">
        <i class="fas fa-lock"></i> Pay $7.99 & apply
      </button>
      <div class="secure-note">
        <i class="fas fa-shield-alt"></i> Secure payment · demo only
      </div>
    </div>
  </div>

  <!-- TOAST -->
  <div class="toast-msg" id="toastMsg">
    <i class="fas fa-check-circle"></i>
    <span id="toastText">Application submitted!</span>
  </div>

  <!-- FOOTER -->
  <footer class="footer">
    <div class="footer-links">
      <a href="#">About</a>
      <a href="#">How it works</a>
      <a href="#">Writer guidelines</a>
      <a href="#">Terms</a>
      <a href="#">Privacy</a>
    </div>
    <p>© 2025 WriteForMoney — demo UI. No real payments processed.</p>
  </footer>

  <script>
    (function() {
      'use strict';

      // ---------- JOB DATA ----------
      const jobs = [
        {
          id: 'w1',
          title: 'Blog Post Writer (Tech & SaaS)',
          location: 'Remote',
          type: 'Freelance',
          rate: '$0.08/word',
          fee: 7.99,
          icon: 'fa-laptop-code',
          description: 'Write 1,500-word SEO blog posts about software tools and productivity. 3–5 articles per week. Long-term collaboration.'
        },
        {
          id: 'w2',
          title: 'Product Description Copywriter',
          location: 'Remote',
          type: 'Part-time',
          rate: '$0.06/word',
          fee: 7.99,
          icon: 'fa-tags',
          description: 'Craft compelling product descriptions for e-commerce catalogues. Short-form copy that converts. Weekly batches of 40+ SKUs.'
        },
        {
          id: 'w3',
          title: 'Ghostwriter — Business eBooks',
          location: 'Remote',
          type: 'Contract',
          rate: '$1,200/project',
          fee: 7.99,
          icon: 'fa-book-open',
          description: 'Ghostwrite 20,000-word business eBooks for founders and consultants. Interview-based writing. 1–2 projects per month.'
        },
        {
          id: 'w4',
          title: 'Technical Writer (API Docs)',
          location: 'Remote',
          type: 'Full-time',
          rate: '$4,500/month',
          fee: 7.99,
          icon: 'fa-code',
          description: 'Write and maintain developer documentation for REST APIs and SDKs. Experience with Markdown, OpenAPI, and Git required.'
        },
        {
          id: 'w5',
          title: 'SEO Content Editor',
          location: 'Remote',
          type: 'Part-time',
          rate: '$25/hour',
          fee: 7.99,
          icon: 'fa-search',
          description: 'Edit and optimise articles for search intent, readability, and keyword density. Review 15–20 pieces per week.'
        },
        {
          id: 'w6',
          title: 'Social Media Copywriter',
          location: 'Remote',
          type: 'Freelance',
          rate: '$0.10/word',
          fee: 7.99,
          icon: 'fa-hashtag',
          description: 'Write punchy captions and thread copy for Twitter, LinkedIn, and Instagram. 10–15 posts per week for a fintech client.'
        }
      ];

      // ---------- STATE ----------
      const paidJobs = new Set();
      let currentJobId = null;

      // ---------- DOM ELEMENTS ----------
      const jobsGrid = document.getElementById('jobsGrid');
      const jobCountPill = document.getElementById('jobCountPill');
      const modalOverlay = document.getElementById('paymentModal');
      const closeModalBtn = document.getElementById('closeModalBtn');
      const confirmPaymentBtn = document.getElementById('confirmPaymentBtn');
      const jobTitleModal = document.getElementById('jobTitleModal');
      const cardNumberInput = document.getElementById('cardNumberInput');
      const cardNameInput = document.getElementById('cardNameInput');
      const toastMsg = document.getElementById('toastMsg');
      const toastText = document.getElementById('toastText');
      const toastIcon = toastMsg.querySelector('i');

      // ---------- TOAST ----------
      let toastTimer = null;
      function showToast(message, isError = false) {
        toastText.textContent = message;
        toastIcon.className = isError
          ? 'fas fa-exclamation-circle'
          : 'fas fa-check-circle';
        toastIcon.style.color = isError ? '#fca5a5' : '#fcd34d';
        toastMsg.classList.add('show');
        clearTimeout(toastTimer);
        toastTimer = setTimeout(() => {
          toastMsg.classList.remove('show');
        }, 3000);
      }

      // ---------- RENDER ----------
      function renderJobs() {
        jobsGrid.innerHTML = '';

        jobs.forEach(job => {
          const isPaid = paidJobs.has(job.id);
          const card = document.createElement('div');
          card.className = 'job-card' + (isPaid ? ' applied' : '');
          card.dataset.jobId = job.id;

          card.innerHTML = `
            <span class="card-ribbon">Applied</span>
            <div class="job-header">
              <div class="job-icon"><i class="fas ${job.icon}"></i></div>
              <div class="fee-tag"><i class="fas fa-tag"></i> $${job.fee.toFixed(2)} fee</div>
            </div>
            <h3 class="job-title">${job.title}</h3>
            <div class="job-meta-row">
              <span><i class="fas fa-map-marker-alt"></i> ${job.location}</span>
              <span><i class="fas fa-clock"></i> Flexible</span>
            </div>
            <p class="job-desc">${job.description}</p>
            <div class="job-footer">
              <span class="pay-rate"><i class="fas fa-coins"></i> ${job.rate}</span>
              <span class="job-type-tag">${job.type}</span>
            </div>
            <button class="apply-btn ${isPaid ? 'paid' : ''}" data-job-id="${job.id}" ${isPaid ? 'disabled' : ''}>
              ${isPaid
                ? '<i class="fas fa-check-circle"></i> Applied &amp; paid'
                : '<i class="fas fa-paper-plane"></i> Pay $' + job.fee.toFixed(2) + ' &amp; apply'}
            </button>
          `;

          jobsGrid.appendChild(card);
        });

        // update count pill
        const remaining = jobs.length - paidJobs.size;
        jobCountPill.textContent = remaining + (remaining === 1 ? ' job' : ' jobs');

        // attach event listeners
        jobsGrid.querySelectorAll('.apply-btn').forEach(btn => {
          btn.addEventListener('click', function() {
            const jobId = this.dataset.jobId;
            if (!jobId || paidJobs.has(jobId)) return;
            openPaymentModal(jobId);
          });
        });
      }

      // ---------- MODAL CONTROLS ----------
      function openPaymentModal(jobId) {
        const job = jobs.find(j => j.id === jobId);
        if (!job) return;
        currentJobId = jobId;
        jobTitleModal.textContent = job.title;
        cardNumberInput.value = '';
        cardNameInput.value = '';
        modalOverlay.classList.add('active');
        setTimeout(() => cardNumberInput.focus(), 220);
      }

      function closeModal() {
        modalOverlay.classList.remove('active');
        currentJobId = null;
      }

      // ---------- PAYMENT ----------
      function handlePayment() {
        if (!currentJobId) {
          closeModal();
          return;
        }

        const cardNum = cardNumberInput.value.trim();
        const cardName = cardNameInput.value.trim();

        // basic validation
        if (!cardNum || cardNum.replace(/\s/g, '').length < 8) {
          showToast('Please enter a valid card number (demo)', true);
          cardNumberInput.focus();
          return;
        }
        if (!cardName) {
          showToast('Please enter the name on the card', true);
          cardNameInput.focus();
          return;
        }

        const jobId = currentJobId;
        const job = jobs.find(j => j.id === jobId);
        paidJobs.add(jobId);

        closeModal();
        renderJobs();

        showToast('Payment successful! You applied for ' + job.title);

        // small highlight delay to show the animation
        setTimeout(() => {
          const paidCard = jobsGrid.querySelector(`[data-job-id="${jobId}"]`);
          if (paidCard) {
            paidCard.scrollIntoView({ behavior: 'smooth', block: 'center' });
          }
        }, 100);
      }

      // ---------- EVENT LISTENERS ----------
      closeModalBtn.addEventListener('click', closeModal);

      modalOverlay.addEventListener('click', function(e) {
        if (e.target === modalOverlay) closeModal();
      });

      confirmPaymentBtn.addEventListener('click', handlePayment);

      // Enter key triggers payment from inputs
      [cardNumberInput, cardNameInput].forEach(input => {
        input.addEventListener('keydown', function(e) {
          if (e.key === 'Enter') {
            e.preventDefault();
            handlePayment();
          }
        });
      });

      // Escape key closes modal
      document.addEventListener('keydown', function(e) {
        if (e.key === 'Escape' && modalOverlay.classList.contains('active')) {
          closeModal();
        }
      });

      // Card number auto-format (adds spaces every 4 digits)
      cardNumberInput.addEventListener('input', function() {
        let v = this.value.replace(/\s/g, '').replace(/\D/g, '');
        v = v.substring(0, 16);
        this.value = v.replace(/(\d{4})(?=\d)/g, '$1 ');
      });

      // ---------- INIT ----------
      renderJobs();
    })();
  </script>
</body>
</html>
