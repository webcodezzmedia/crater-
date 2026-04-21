
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{background:#000;color:#fff;font-family:var(--font-sans,'Inter',sans-serif)}
.wrap{background:#000;min-height:100vh;padding:0 0 60px}

@keyframes fadeUp{from{opacity:0;transform:translateY(40px)}to{opacity:1;transform:translateY(0)}}
@keyframes pulse{0%,100%{box-shadow:0 0 0 0 rgba(139,92,246,0.4)}50%{box-shadow:0 0 0 18px rgba(139,92,246,0)}}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-10px)}}
@keyframes spin{from{transform:rotate(0deg)}to{transform:rotate(360deg)}}
@keyframes lineGrow{from{width:0}to{width:100%}}
@keyframes countUp{from{opacity:0}to{opacity:1}}
@keyframes borderGlow{0%,100%{border-color:rgba(139,92,246,0.3)}50%{border-color:rgba(139,92,246,0.9)}}

.hero{text-align:center;padding:70px 20px 50px;animation:fadeUp .8s ease both}
.badge{display:inline-flex;align-items:center;gap:6px;background:rgba(139,92,246,0.15);border:1px solid rgba(139,92,246,0.4);border-radius:20px;padding:6px 14px;font-size:12px;color:#a78bfa;margin-bottom:24px;letter-spacing:.5px}
.badge-dot{width:6px;height:6px;border-radius:50%;background:#a78bfa;animation:pulse 2s infinite}
.hero h1{font-size:clamp(28px,5vw,54px);font-weight:500;line-height:1.15;color:#fff;margin-bottom:16px}
.hero h1 span{background:linear-gradient(135deg,#a78bfa,#60a5fa);-webkit-background-clip:text;-webkit-text-fill-color:transparent}
.hero p{color:#888;font-size:16px;max-width:520px;margin:0 auto 32px;line-height:1.7}
.hero-btns{display:flex;gap:12px;justify-content:center;flex-wrap:wrap}
.btn-primary{background:linear-gradient(135deg,#7c3aed,#3b82f6);border:none;color:#fff;padding:12px 28px;border-radius:8px;font-size:14px;cursor:pointer;transition:opacity .2s,transform .2s}
.btn-primary:hover{opacity:.85;transform:scale(1.03)}
.btn-outline{background:transparent;border:1px solid rgba(255,255,255,.2);color:#ccc;padding:12px 28px;border-radius:8px;font-size:14px;cursor:pointer;transition:border-color .2s,color .2s}
.btn-outline:hover{border-color:rgba(139,92,246,.7);color:#a78bfa}

.divider{height:1px;background:linear-gradient(90deg,transparent,rgba(139,92,246,.4),transparent);margin:0 40px}

.stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:1px;background:rgba(255,255,255,.06);border-top:1px solid rgba(255,255,255,.06);border-bottom:1px solid rgba(255,255,255,.06);margin:0}
.stat{background:#000;padding:28px 20px;text-align:center;animation:fadeUp .8s ease both}
.stat:nth-child(2){animation-delay:.1s}
.stat:nth-child(3){animation-delay:.2s}
.stat:nth-child(4){animation-delay:.3s}
.stat-num{font-size:28px;font-weight:500;color:#a78bfa;margin-bottom:4px}
.stat-label{font-size:12px;color:#666;letter-spacing:.5px}

.section{padding:60px 24px;max-width:900px;margin:0 auto}
.sec-tag{font-size:11px;letter-spacing:2px;color:#7c3aed;text-transform:uppercase;margin-bottom:10px}
.sec-title{font-size:clamp(20px,3vw,32px);font-weight:500;color:#fff;margin-bottom:12px}
.sec-sub{font-size:15px;color:#666;max-width:480px;line-height:1.7;margin-bottom:36px}

.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px}
.card{background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.08);border-radius:12px;padding:24px;transition:border-color .3s,transform .3s;animation:fadeUp .8s ease both}
.card:hover{border-color:rgba(139,92,246,.5);transform:translateY(-4px)}
.card-icon{width:40px;height:40px;border-radius:10px;display:flex;align-items:center;justify-content:center;margin-bottom:16px;font-size:18px}
.card-icon.purple{background:rgba(139,92,246,.15)}
.card-icon.blue{background:rgba(59,130,246,.15)}
.card-icon.teal{background:rgba(20,184,166,.15)}
.card-icon.pink{background:rgba(236,72,153,.15)}
.card h3{font-size:15px;font-weight:500;color:#e5e5e5;margin-bottom:8px}
.card p{font-size:13px;color:#666;line-height:1.6}

.feedback-wrap{display:grid;grid-template-columns:1fr 1fr;gap:24px}
@media(max-width:580px){.feedback-wrap{grid-template-columns:1fr}}
.feedback-left{display:flex;flex-direction:column;gap:16px}
.review-card{background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.07);border-radius:12px;padding:20px;animation:fadeUp .8s ease both;animation-fill-mode:both}
.review-card:nth-child(2){animation-delay:.15s}
.review-card:nth-child(3){animation-delay:.3s}
.stars{display:flex;gap:3px;margin-bottom:10px}
.star{color:#f59e0b;font-size:14px}
.review-text{font-size:13px;color:#aaa;line-height:1.6;margin-bottom:12px}
.reviewer{display:flex;align-items:center;gap:10px}
.avatar{width:30px;height:30px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:500}
.av1{background:rgba(139,92,246,.25);color:#a78bfa}
.av2{background:rgba(59,130,246,.25);color:#60a5fa}
.av3{background:rgba(20,184,166,.25);color:#2dd4bf}
.reviewer-name{font-size:13px;color:#ccc;font-weight:500}
.reviewer-role{font-size:11px;color:#555}

.form-card{background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.08);border-radius:14px;padding:28px;animation:borderGlow 3s ease infinite;animation-delay:.5s}
.form-card h3{font-size:17px;font-weight:500;color:#fff;margin-bottom:6px}
.form-card p{font-size:13px;color:#666;margin-bottom:22px}
.field{margin-bottom:14px}
.field label{display:block;font-size:12px;color:#777;margin-bottom:6px;letter-spacing:.3px}
.field input,.field textarea,.field select{width:100%;background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.1);border-radius:8px;padding:10px 12px;color:#e5e5e5;font-size:13px;outline:none;font-family:inherit;transition:border-color .2s}
.field input:focus,.field textarea:focus,.field select:focus{border-color:rgba(139,92,246,.6)}
.field textarea{resize:vertical;min-height:80px}
.field select option{background:#111;color:#e5e5e5}
.rating-row{display:flex;gap:6px}
.rating-btn{background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.1);color:#888;padding:8px 14px;border-radius:6px;font-size:13px;cursor:pointer;transition:all .2s}
.rating-btn.active,.rating-btn:hover{background:rgba(139,92,246,.2);border-color:#7c3aed;color:#a78bfa}
#submitFeedback{width:100%;background:linear-gradient(135deg,#7c3aed,#3b82f6);border:none;color:#fff;padding:12px;border-radius:8px;font-size:14px;cursor:pointer;margin-top:6px;transition:opacity .2s;font-family:inherit}
#submitFeedback:hover{opacity:.85}
.success-msg{display:none;text-align:center;padding:20px;color:#2dd4bf;font-size:14px;animation:fadeUp .4s ease}

.contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:24px}
@media(max-width:580px){.contact-grid{grid-template-columns:1fr}}
.contact-info{display:flex;flex-direction:column;gap:20px}
.contact-item{display:flex;gap:14px;align-items:flex-start;animation:fadeUp .8s ease both}
.contact-item:nth-child(2){animation-delay:.12s}
.contact-item:nth-child(3){animation-delay:.24s}
.contact-item:nth-child(4){animation-delay:.36s}
.contact-icon{width:38px;height:38px;border-radius:10px;background:rgba(139,92,246,.12);border:1px solid rgba(139,92,246,.25);display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:16px;animation:float 3s ease infinite}
.contact-item:nth-child(2) .contact-icon{animation-delay:.5s}
.contact-item:nth-child(3) .contact-icon{animation-delay:1s}
.contact-icon svg{width:16px;height:16px;stroke:#a78bfa;fill:none;stroke-width:2;stroke-linecap:round;stroke-linejoin:round}
.contact-detail h4{font-size:13px;font-weight:500;color:#ccc;margin-bottom:3px}
.contact-detail p{font-size:12px;color:#555}
.contact-detail a{font-size:12px;color:#7c3aed;text-decoration:none}
.contact-detail a:hover{color:#a78bfa}

.reach-card{background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.08);border-radius:14px;padding:28px}
.reach-card h3{font-size:17px;font-weight:500;color:#fff;margin-bottom:6px}
.reach-card p{font-size:13px;color:#666;margin-bottom:20px}
.social-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:20px}
.social-btn{display:flex;align-items:center;gap:10px;background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.08);border-radius:8px;padding:10px 14px;cursor:pointer;transition:all .2s;text-decoration:none}
.social-btn:hover{border-color:rgba(139,92,246,.5);background:rgba(139,92,246,.08)}
.social-icon{width:26px;height:26px;border-radius:6px;display:flex;align-items:center;justify-content:center;font-size:13px}
.si-tw{background:rgba(29,161,242,.2)}
.si-yt{background:rgba(255,0,0,.15)}
.si-ig{background:rgba(225,48,108,.15)}
.si-li{background:rgba(10,102,194,.2)}
.social-btn span{font-size:13px;color:#bbb}
.newsletter{background:rgba(139,92,246,.08);border:1px solid rgba(139,92,246,.2);border-radius:10px;padding:16px}
.newsletter p{font-size:13px;color:#999;margin-bottom:12px}
.nl-row{display:flex;gap:8px}
.nl-row input{flex:1;background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.12);border-radius:7px;padding:9px 12px;color:#e5e5e5;font-size:13px;outline:none;font-family:inherit}
.nl-row input:focus{border-color:rgba(139,92,246,.6)}
.nl-btn{background:#7c3aed;border:none;color:#fff;padding:9px 16px;border-radius:7px;font-size:13px;cursor:pointer;white-space:nowrap;font-family:inherit;transition:opacity .2s}
.nl-btn:hover{opacity:.85}

.ticker{border-top:1px solid rgba(255,255,255,.06);border-bottom:1px solid rgba(255,255,255,.06);padding:14px 0;overflow:hidden;white-space:nowrap}
.ticker-inner{display:inline-flex;gap:60px;animation:tickerMove 20s linear infinite}
@keyframes tickerMove{from{transform:translateX(0)}to{transform:translateX(-50%)}}
.ticker-item{font-size:13px;color:#444;display:inline-flex;align-items:center;gap:8px}
.ticker-item b{color:#7c3aed}

.footer{text-align:center;padding:40px 20px 0;border-top:1px solid rgba(255,255,255,.06)}
.footer p{font-size:12px;color:#444}
.footer p span{color:#7c3aed}
</style>

<div class="wrap">

<div class="hero">
  <div class="badge"><span class="badge-dot"></span>Creator Platform</div>
  <h1>Build. Connect.<br><span>Grow Together</span></h1>
  <p>A unified space for creators to share work, collect meaningful feedback, and reach customers worldwide.</p>
  <div class="hero-btns">
    <button class="btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Get Started</button>
    <button class="btn-outline" onclick="document.getElementById('feedback-sec').scrollIntoView({behavior:'smooth'})">Leave Feedback</button>
  </div>
</div>

<div class="stats">
  <div class="stat"><div class="stat-num" id="s1">0</div><div class="stat-label">Active Creators</div></div>
  <div class="stat"><div class="stat-num" id="s2">0</div><div class="stat-label">Feedback Collected</div></div>
  <div class="stat"><div class="stat-num" id="s3">0</div><div class="stat-label">Customer Reach</div></div>
  <div class="stat"><div class="stat-num" id="s4">0</div><div class="stat-label">Countries</div></div>
</div>

<div class="section">
  <div class="sec-tag">What We Offer</div>
  <div class="sec-title">Everything a creator needs</div>
  <div class="sec-sub">From building your audience to understanding what they love — all in one place.</div>
  <div class="cards">
    <div class="card" style="animation-delay:.0s">
      <div class="card-icon purple">✦</div>
      <h3>Creator Studio</h3>
      <p>Publish content, build portfolios, and showcase your work with beautiful animated profiles.</p>
    </div>
    <div class="card" style="animation-delay:.1s">
      <div class="card-icon blue">◎</div>
      <h3>Smart Feedback</h3>
      <p>Collect structured feedback with star ratings, categories, and sentiment analysis.</p>
    </div>
    <div class="card" style="animation-delay:.2s">
      <div class="card-icon teal">⬡</div>
      <h3>Customer Reach</h3>
      <p>Expand your audience with targeted campaigns, social integrations and newsletters.</p>
    </div>
    <div class="card" style="animation-delay:.3s">
      <div class="card-icon pink">◈</div>
      <h3>Live Analytics</h3>
      <p>Real-time dashboards showing engagement, conversion rates and growth trends.</p>
    </div>
  </div>
</div>

<div class="divider"></div>

<div class="section" id="feedback-sec">
  <div class="sec-tag">Community Voice</div>
  <div class="sec-title">Feedback that matters</div>
  <div class="sec-sub">See what creators and customers are saying, then share your own thoughts.</div>
  <div class="feedback-wrap">
    <div class="feedback-left">
      <div class="review-card">
        <div class="stars"><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span></div>
        <p class="review-text">The platform completely transformed how I connect with my audience. The feedback tools are incredibly intuitive.</p>
        <div class="reviewer"><div class="avatar av1">SA</div><div><div class="reviewer-name">Sofia Alvarez</div><div class="reviewer-role">Digital Artist · 12k followers</div></div></div>
      </div>
      <div class="review-card">
        <div class="stars"><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span></div>
        <p class="review-text">Customer reach doubled within 3 months. The analytics give me exactly the insights I need to grow.</p>
        <div class="reviewer"><div class="avatar av2">MK</div><div><div class="reviewer-name">Marcus Kim</div><div class="reviewer-role">Content Creator · Podcaster</div></div></div>
      </div>
      <div class="review-card">
        <div class="stars"><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span></div>
        <p class="review-text">Finally a platform that treats creators as professionals. The tools here are world-class.</p>
        <div class="reviewer"><div class="avatar av3">PN</div><div><div class="reviewer-name">Priya Nair</div><div class="reviewer-role">UX Designer · Educator</div></div></div>
      </div>
    </div>
    <div class="form-card">
      <h3>Share your feedback</h3>
      <p>Your opinion shapes the platform</p>
      <div id="feedbackForm">
        <div class="field">
          <label>Your name</label>
          <input type="text" id="fname" placeholder="e.g. Alex Johnson">
        </div>
        <div class="field">
          <label>Category</label>
          <select id="fcat">
            <option value="">Select a category</option>
            <option>Creator Tools</option>
            <option>Feedback System</option>
            <option>Customer Reach</option>
            <option>Analytics</option>
            <option>General</option>
          </select>
        </div>
        <div class="field">
          <label>Rating</label>
          <div class="rating-row" id="ratingRow">
            <button class="rating-btn" onclick="setRating(1)">1</button>
            <button class="rating-btn" onclick="setRating(2)">2</button>
            <button class="rating-btn" onclick="setRating(3)">3</button>
            <button class="rating-btn" onclick="setRating(4)">4</button>
            <button class="rating-btn" onclick="setRating(5)">5</button>
          </div>
        </div>
        <div class="field">
          <label>Your message</label>
          <textarea id="fmsg" placeholder="Tell us what you think..."></textarea>
        </div>
        <button id="submitFeedback" onclick="submitFeedback()">Submit Feedback →</button>
      </div>
      <div class="success-msg" id="successMsg">
        ✓ Thank you! Your feedback has been received.
      </div>
    </div>
  </div>
</div>

<div class="divider"></div>

<div class="section" id="contact">
  <div class="sec-tag">Get In Touch</div>
  <div class="sec-title">Customer reach starts here</div>
  <div class="sec-sub">Connect with us through any channel — we're ready to help you grow.</div>
  <div class="contact-grid">
    <div class="contact-info">
      <div class="contact-item">
        <div class="contact-icon">
          <svg viewBox="0 0 24 24"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        </div>
        <div class="contact-detail">
          <h4>Email us</h4>
          <a href="#">hello@creatorplatform.io</a>
          <p>Response within 24 hours</p>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon">
          <svg viewBox="0 0 24 24"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 13a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.6 2h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
        </div>
        <div class="contact-detail">
          <h4>Call us</h4>
          <a href="#">+1 (800) 123-4567</a>
          <p>Mon–Fri, 9 AM – 6 PM EST</p>
        </div>
      </div>
      <div class="contact-item">
        <div class="contact-icon">
          <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        </div>
        <div class="contact-detail">
          <h4>Live chat</h4>
          <a href="#">Start a conversation</a>
          <p>Available 24/7 for creators</p>
        </div>
      </div>
    </div>

    <div class="reach-card">
      <h3>Follow &amp; connect</h3>
      <p>Stay updated across all platforms</p>
      <div class="social-grid">
        <a class="social-btn" href="#"><div class="social-icon si-tw">𝕏</div><span>Twitter/X</span></a>
        <a class="social-btn" href="#"><div class="social-icon si-yt">▶</div><span>YouTube</span></a>
        <a class="social-btn" href="#"><div class="social-icon si-ig">◉</div><span>Instagram</span></a>
        <a class="social-btn" href="#"><div class="social-icon si-li">in</div><span>LinkedIn</span></a>
      </div>
      <div class="newsletter">
        <p>Get creator tips & platform updates in your inbox.</p>
        <div class="nl-row">
          <input type="email" id="nlEmail" placeholder="your@email.com">
          <button class="nl-btn" onclick="subscribeNL()">Subscribe</button>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="ticker">
  <div class="ticker-inner" id="ticker">
    <span class="ticker-item">✦ <b>12,400+</b> active creators</span>
    <span class="ticker-item">◎ <b>98%</b> satisfaction rate</span>
    <span class="ticker-item">⬡ <b>45</b> countries reached</span>
    <span class="ticker-item">◈ <b>500K+</b> feedbacks collected</span>
    <span class="ticker-item">✦ <b>2.3M</b> customers connected</span>
    <span class="ticker-item">◎ <b>Free</b> to get started</span>
    <span class="ticker-item">✦ <b>12,400+</b> active creators</span>
    <span class="ticker-item">◎ <b>98%</b> satisfaction rate</span>
    <span class="ticker-item">⬡ <b>45</b> countries reached</span>
    <span class="ticker-item">◈ <b>500K+</b> feedbacks collected</span>
    <span class="ticker-item">✦ <b>2.3M</b> customers connected</span>
    <span class="ticker-item">◎ <b>Free</b> to get started</span>
  </div>
</div>

<div class="footer">
  <p>© 2026 <span>Creator Platform</span> · Built for creators, by creators</p>
</div>

</div>

<script>
let selectedRating = 0;

function setRating(n) {
  selectedRating = n;
  document.querySelectorAll('.rating-btn').forEach((b,i) => {
    b.classList.toggle('active', i < n);
  });
}

function submitFeedback() {
  const name = document.getElementById('fname').value.trim();
  const msg = document.getElementById('fmsg').value.trim();
  if (!name || !msg || !selectedRating) {
    const btn = document.getElementById('submitFeedback');
    btn.style.background = 'linear-gradient(135deg,#991b1b,#7f1d1d)';
    btn.textContent = 'Please fill all fields';
    setTimeout(() => {
      btn.style.background = 'linear-gradient(135deg,#7c3aed,#3b82f6)';
      btn.textContent = 'Submit Feedback →';
    }, 2000);
    return;
  }
  document.getElementById('feedbackForm').style.display = 'none';
  const s = document.getElementById('successMsg');
  s.style.display = 'block';
  setTimeout(() => {
    s.style.display = 'none';
    document.getElementById('feedbackForm').style.display = 'block';
    document.getElementById('fname').value = '';
    document.getElementById('fcat').value = '';
    document.getElementById('fmsg').value = '';
    selectedRating = 0;
    document.querySelectorAll('.rating-btn').forEach(b => b.classList.remove('active'));
  }, 3000);
}

function subscribeNL() {
  const el = document.getElementById('nlEmail');
  if (!el.value.includes('@')) {
    el.style.borderColor = 'rgba(220,38,38,.6)';
    setTimeout(() => el.style.borderColor = '', 1500);
    return;
  }
  const btn = document.querySelector('.nl-btn');
  btn.textContent = '✓ Subscribed!';
  btn.style.background = '#0f6e56';
  el.value = '';
  setTimeout(() => {
    btn.textContent = 'Subscribe';
    btn.style.background = '#7c3aed';
  }, 3000);
}

function animateCount(id, end, suffix) {
  let start = 0;
  const dur = 2000;
  const step = 16;
  const inc = end / (dur / step);
  const el = document.getElementById(id);
  const t = setInterval(() => {
    start += inc;
    if (start >= end) { start = end; clearInterval(t); }
    el.textContent = Math.round(start).toLocaleString() + suffix;
  }, step);
}

setTimeout(() => {
  animateCount('s1', 12400, '+');
  animateCount('s2', 500, 'K+');
  animateCount('s3', 2.3, 'M');
  animateCount('s4', 45, '');
}, 400);
</script>
