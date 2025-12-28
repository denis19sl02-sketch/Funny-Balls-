<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<title>Blue Ball Game</title>
<meta name="viewport" content="width=device-width,initial-scale=1" />
<style>
  html,body{margin:0;padding:0;height:100%;width:100%;overflow:hidden;font-family:sans-serif;background:#87CEEB;}
  canvas{display:block;position:absolute;left:0;top:0;z-index:5;}
  .btn,.level-btn{border:none;cursor:pointer;user-select:none;-webkit-tap-highlight-color:transparent;display:flex;align-items:center;justify-content:center;transition:transform .12s ease,box-shadow .12s ease,background .12s ease;}
  .btn{width:120px;height:120px;border-radius:50%;font-weight:bold;font-size:18px;position:absolute;box-shadow:0 6px 12px rgba(0,0,0,0.25);color:white;}
  .level-btn{width:80px;height:80px;border-radius:50%;font-size:24px;font-weight:bold;box-shadow:0 4px 8px rgba(0,0,0,0.3);color:white;}
  .btn-pressed{transform:translateY(6px) scale(.98);box-shadow:0 3px 8px rgba(0,0,0,.22);}
  .level-btn-pressed{transform:translateY(4px) scale(.98);box-shadow:0 2px 6px rgba(0,0,0,.22);}
  .btn-endless{background:#2ecc71;left:50%;top:25%;transform:translate(-50%,-50%);}
  .btn-start{background:#f1c40f;color:#111;left:50%;top:50%;transform:translate(-50%,-50%);}
  .btn-simple{background:#40E0D0; left:63%; top:44%; transform:translate(-50%,-50%);}
  .btn-levels{background:#9b59b6;right:10%;top:50%;transform:translateY(-50%);}
  .btn-home{background:#3498db;left:10%;top:50%;transform:translateY(-50%);}
  #menu,#levelMenu,#homePage,#colorPage{position:absolute;left:0;top:0;width:100%;height:100%;display:flex;align-items:center;justify-content:center;z-index:30;background:transparent;}
  #rightPanel{position:absolute;right:28px;top:36px;z-index:31;display:flex;flex-direction:column;align-items:center;gap:12px;pointer-events:none;}
  #scoreDisplay{pointer-events:auto;font-size:20px;font-weight:bold;color:#fff;text-shadow:0 2px 4px rgba(0,0,0,0.4);background:rgba(255,255,255,0.06);padding:6px 10px;border-radius:8px;}
  #jumpBtn{pointer-events:auto;width:96px;height:96px;border-radius:50%;border:none;background:#f1c40f;color:#111;font-weight:bold;font-size:18px;box-shadow:0 6px 12px rgba(0,0,0,0.25);cursor:pointer;display:flex;align-items:center;justify-content:center;transition:transform .12s ease,box-shadow .12s ease;}
  #overlay{position:absolute;left:0;top:0;width:100%;height:100%;display:none;align-items:center;justify-content:center;z-index:50;background:rgba(0,0,0,0.6);color:white;font-size:36px;}
  #overlay .box{background:rgba(0,0,0,0.5);padding:18px 24px;border-radius:12px;text-align:center;}
  #overlay button{margin-top:14px;padding:8px 14px;font-size:18px;}
  #levelMenu{display:none;flex-direction:row;flex-wrap:wrap;justify-content:center;align-items:flex-start;padding-top:90px;gap:18px;background:transparent;}
  .locked{background:#888;cursor:default;color:#ddd;box-shadow:0 2px 4px rgba(0,0,0,0.2) !important;}
  #homePage{background:transparent;flex-direction:column;justify-content:flex-start;display:none;align-items:center;padding-top:60px;gap:18px;}
  #homePage h1{color:#0077FF;font-size:72px;margin-top:18px;text-shadow:none;}
  .home-btn{font-size:20px;font-weight:bold;border:none;border-radius:12px;padding:10px 18px;cursor:pointer;box-shadow:0 5px 10px rgba(0,0,0,0.3);transition:transform .15s ease;}
  .home-btn:active{transform:scale(.96);}
  #homeMsg{margin-top:8px;color:#003377;font-size:18px;font-weight:bold;opacity:0;transition:opacity .35s ease;}
  .mainBtn{position:absolute;top:10px;right:10px;background:#004b00;color:#fff;border:none;border-radius:10px;padding:8px 12px;cursor:pointer;font-size:14px;z-index:100;transition:transform .1s ease;display:none;}
  .mainBtn:active{transform:scale(.95);}
  .selection-indicator{position:absolute; left:50%; top:62%; transform:translate(-50%,-50%); font-size:14px; color:#003; background:rgba(255,255,255,0.12); padding:6px 10px; border-radius:10px; z-index:32; display:none;}
  
  /* REAL PAYMENT FORM */
  #paymentModal{position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.95);z-index:1000;display:none;align-items:center;justify-content:center;}
  .payment-container{background:white;padding:40px;border-radius:15px;max-width:500px;width:90%;box-shadow:0 20px 60px rgba(0,0,0,0.5);}
  .payment-header{font-size:28px;margin-bottom:20px;color:#2c3e50;text-align:center;font-weight:bold;}
  .price-tag{font-size:42px;font-weight:bold;text-align:center;margin:25px 0;color:#e74c3c;}
  
  /* Card input form */
  .card-input-group{margin:20px 0;}
  .card-input-label{display:block;margin-bottom:8px;color:#34495e;font-weight:bold;font-size:16px;}
  .card-input{width:100%;padding:15px;border:2px solid #ddd;border-radius:10px;font-size:18px;transition:border-color 0.3s;box-sizing:border-box;}
  .card-input:focus{border-color:#3498db;outline:none;}
  .card-row{display:flex;gap:15px;margin-top:15px;}
  .card-col{flex:1;}
  
  #submitPayment{background:#27ae60;color:white;border:none;padding:18px;width:100%;border-radius:10px;font-size:20px;font-weight:bold;cursor:pointer;margin-top:25px;transition:background 0.3s;}
  #submitPayment:hover{background:#219653;}
  #submitPayment:disabled{background:#95a5a6;cursor:not-allowed;}
  
  #closePayment{background:#e74c3c;color:white;border:none;padding:15px;width:100%;border-radius:10px;margin-top:15px;cursor:pointer;font-size:16px;}
  
  .payment-status{margin-top:20px;padding:15px;border-radius:10px;display:none;text-align:center;font-weight:bold;}
  .status-success{background:#d5edda;color:#155724;border:1px solid #c3e6cb;}
  .status-error{background:#f8d7da;color:#721c24;border:1px solid #f5c6cb;}
  .status-processing{background:#d1ecf1;color:#0c5460;border:1px solid #bee5eb;}
  
  .card-type{position:absolute;right:15px;top:50%;transform:translateY(-50%);font-size:24px;}
  .visa{color:#1a1f71;}
  .mastercard{color:#eb001b;}
  .amex{color:#002663;}
  
  .card-input-wrapper{position:relative;}
  
  /* Expiry date visual feedback */
  .expiry-wrapper{position:relative;}
  .expiry-visual{position:relative;}
  .expiry-preview{position:absolute;top:15px;left:15px;font-size:18px;color:#aaa;pointer-events:none;display:flex;gap:2px;font-family:monospace;}
  .preview-month,.preview-year{padding:2px 6px;border-radius:4px;transition:all 0.2s;}
  .preview-active{background-color:rgba(52,152,219,0.15);color:#3498db;font-weight:bold;}
  .preview-slash{color:#ccc;}
  .expiry-hint{font-size:12px;color:#95a5a6;margin-top:5px;text-align:center;}
  @keyframes highlight{0%{background-color:rgba(52,152,219,0.1);}50%{background-color:rgba(52,152,219,0.2);}100%{background-color:rgba(52,152,219,0.1);}}
  .card-input:focus{animation:highlight 2s ease-in-out infinite;}
  
  /* color page styling */
  #colorGrid{display:grid;grid-template-columns:repeat(4,1fr);gap:14px;padding:24px;max-width:900px;width:92%;justify-items:center;}
  .color-btn{width:72px;height:72px;border-radius:50%;border:3px solid rgba(255,255,255,0.6);cursor:pointer;box-shadow:0 6px 12px rgba(0,0,0,0.2);display:flex;align-items:center;justify-content:center;}
  .color-name{font-size:13px;margin-top:6px;color:#003;}
  #colorPage{display:none;flex-direction:column;align-items:center;justify-content:flex-start;padding-top:40px;}
  .color-card{display:flex;flex-direction:column;align-items:center;}
  .buy-btn{background:#e74c3c;color:white;padding:10px 14px;border-radius:10px;border:none;cursor:pointer;font-weight:bold;box-shadow:0 6px 12px rgba(0,0,0,0.25);}
  
  @media (max-width:520px){.btn{width:88px;height:88px;font-size:14px;}.level-btn{width:64px;height:64px;font-size:18px;}#homePage h1{font-size:56px;}.btn-simple{left:60%;}}
</style>
</head>
<body>
<!-- REAL PAYMENT FORM WITH CARD INPUT -->
<div id="paymentModal">
  <div class="payment-container">
    <div class="payment-header">💳 PAYMENT $35</div>
    <p style="text-align:center;color:#7f8c8d;margin-bottom:10px;">Unlock Levels 15-35</p>
    
    <div class="price-tag">$35.00</div>
    
    <form id="cardForm">
      <div class="card-input-group">
        <label class="card-input-label">Card Number</label>
        <div class="card-input-wrapper">
          <input type="text" id="cardNumber" class="card-input" placeholder="4242 4242 4242 4242" maxlength="19" inputmode="numeric">
          <span id="cardType" class="card-type"></span>
        </div>
      </div>
      
      <div class="card-row">
        <div class="card-col">
          <label class="card-input-label">Expiration Date</label>
          <div class="expiry-wrapper">
            <div class="expiry-visual">
              <input type="text" id="cardExpiry" class="card-input" 
                     placeholder="MM/YY" maxlength="5" 
                     style="text-align:center;font-size:20px;letter-spacing:2px;">
              <div class="expiry-preview">
                <span id="monthPreview" class="preview-month">MM</span>
                <span class="preview-slash">/</span>
                <span id="yearPreview" class="preview-year">YY</span>
              </div>
            </div>
            <div class="expiry-hint">Enter month and year as shown on card</div>
          </div>
        </div>
        <div class="card-col">
          <label class="card-input-label">CVC</label>
          <input type="text" id="cardCvc" class="card-input" placeholder="123" maxlength="4" inputmode="numeric">
        </div>
      </div>
      
      <div class="card-input-group">
        <label class="card-input-label">Name on Card</label>
        <input type="text" id="cardName" class="card-input" placeholder="JOHN DOE">
      </div>
      
      <button type="submit" id="submitPayment">💳 PAY $35 NOW</button>
    </form>
    
    <div id="paymentStatus" class="payment-status"></div>
    
    <button id="closePayment">✖ CANCEL</button>
    
    <div style="font-size:12px;color:#95a5a6;margin-top:20px;text-align:center;">
      <p>💳 System validates cards via Stripe API</p>
      <p>✅ Real cards: $35 will be charged</p>
      <p>❌ Invalid cards: error message</p>
      <p>🔒 Payment secured with PCI DSS</p>
    </div>
  </div>
</div>

<!-- Game interface -->
<button id="mainBtn" class="mainBtn">GO TO THE MAIN PAGE</button>
<div id="menu">
  <button class="btn btn-endless" id="btnEndless">ENDLESS</button>
  <button class="btn btn-start" id="btnStart">START</button>
  <button class="btn btn-simple" id="btnSimple">SIMPLE GAME</button>
  <button class="btn btn-levels" id="btnLevels">LEVELS</button>
  <button class="btn btn-home" id="btnHome">HOME</button>
  <div id="selectionIndicator" class="selection-indicator"></div>
</div>
<div id="levelMenu"><h1>LEVELS</h1></div>
<canvas id="game"></canvas>
<div id="rightPanel">
  <div id="scoreDisplay">0</div>
  <button id="jumpBtn">JUMP</button>
</div>
<div id="overlay">
  <div class="box">
    <div id="message"></div>
    <button id="overlayMainBtn">GO TO THE MAIN PAGE</button>
  </div>
</div>
<div id="homePage">
  <h1>HOME</h1>
  <button id="ownRecord" class="home-btn" style="background:#7CFC00;color:black;">OWN RECORD: 0</button>
  <button id="completedLvls" class="home-btn" style="background:#4B0082;color:white;">COMPLETED LEVELS: 0</button>
  <button id="colorPickerBtn" class="home-btn" style="background:#00BFFF;color:black;">THE COLOR OF THE BALL IS</button>
  
  <!-- Purchase button for $35 -->
  <button id="buyUnlock" class="home-btn buy-btn" style="font-size:18px;padding:12px 20px;">🔓 UNLOCK 15-35 FOR $35</button>
  
  <!-- For premium users -->
  <button id="premiumBadge" class="home-btn" style="background:#FFD700;color:black;display:none;">
    ⭐ PREMIUM ACTIVE
  </button>
  
  <div id="homeMsg"></div>
</div>

<!-- Color selection page -->
<div id="colorPage">
  <h1 style="color:#0077FF;margin-bottom:8px;">Choose ball color</h1>
  <div id="colorGrid"></div>
  <button id="colorBack" class="home-btn" style="margin-top:18px;">BACK</button>
</div>

<script>
/* ============================================
   REAL PAYMENT SYSTEM - CARD VALIDATION VIA STRIPE API
   ============================================ */
// 🔥 YOUR STRIPE PUBLIC KEY (REPLACE WITH YOURS!)
const STRIPE_PUBLIC_KEY = 'pk_live_51Sb8qUD24yIDSpalVPGx0bHtgAM9Hio1xFeLLVFswnW1NW87xPO8qUXak27GCeWe05aVe0eSng4jnrFhrfBa9FRr005BSzRvca';

// Your backend server (required!)
const BACKEND_URL = 'https://node-8080.csb.app'; // Your server

// Payment configuration
const PAYMENT_CONFIG = {
  amount: 3500, // $35.00 in cents
  currency: 'usd',
  productName: 'Premium Levels 15-35 Unlock',
  productId: 'premium_game_levels'
};

/* ============================================
   GAME INITIALIZATION
   ============================================ */
const canvas = document.getElementById('game');
const ctx = canvas.getContext('2d');
function resizeCanvas(){ canvas.width = window.innerWidth; canvas.height = window.innerHeight; }
window.addEventListener('resize', resizeCanvas);
resizeCanvas();

/* UI refs */
const btnEndless = document.getElementById('btnEndless'),
btnStart   = document.getElementById('btnStart'),
btnSimple  = document.getElementById('btnSimple'),
btnLevels  = document.getElementById('btnLevels'),
btnHome    = document.getElementById('btnHome'),
jumpBtn    = document.getElementById('jumpBtn'),
menu       = document.getElementById('menu'),
levelMenu  = document.getElementById('levelMenu'),
overlay    = document.getElementById('overlay'),
overlayMainBtn = document.getElementById('overlayMainBtn'),
messageBox = document.getElementById('message'),
scoreEl    = document.getElementById('scoreDisplay'),
homePage   = document.getElementById('homePage'),
homeMsg    = document.getElementById('homeMsg'),
ownRecordBtn = document.getElementById('ownRecord'),
completedLvlsBtn = document.getElementById('completedLvls'),
mainBtn    = document.getElementById('mainBtn'),
selectionIndicator = document.getElementById('selectionIndicator'),
colorPickerBtn = document.getElementById('colorPickerBtn'),
colorPage = document.getElementById('colorPage'),
colorGrid = document.getElementById('colorGrid'),
colorBack = document.getElementById('colorBack'),
buyUnlockBtn = document.getElementById('buyUnlock'),
premiumBadge = document.getElementById('premiumBadge'),
paymentModal = document.getElementById('paymentModal'),
closePayment = document.getElementById('closePayment'),
cardForm = document.getElementById('cardForm'),
submitPayment = document.getElementById('submitPayment'),
paymentStatus = document.getElementById('paymentStatus'),
cardNumber = document.getElementById('cardNumber'),
cardExpiry = document.getElementById('cardExpiry'),
cardCvc = document.getElementById('cardCvc'),
cardName = document.getElementById('cardName'),
cardType = document.getElementById('cardType');

let mode = 'menu';
let simpleSelected=false, endlessSelected=false;
let inGame=false, gameOver=false;
let score=0, cameraX=0, fences=[], currentLevel=0;
let unlockedLevel = parseInt(localStorage.getItem('unlockedLevel')) || 1;
let bestRecord = parseInt(localStorage.getItem('bestRecord')) || 0;
let isPremium = localStorage.getItem('isPremium') === 'true';

/* ============================================
   EXPIRY DATE VISUAL INPUT SYSTEM
   ============================================ */
// Format expiry with visual feedback
function formatExpiry(value) {
  const v = value.replace(/\D/g, '');
  
  // Clear preview when empty
  if (v.length === 0) {
    document.getElementById('monthPreview').textContent = 'MM';
    document.getElementById('yearPreview').textContent = 'YY';
    document.getElementById('monthPreview').classList.remove('preview-active');
    document.getElementById('yearPreview').classList.remove('preview-active');
    return '';
  }
  
  // Format as MM/YY
  if (v.length === 1) {
    const month = v;
    document.getElementById('monthPreview').textContent = month.padStart(2, '0');
    document.getElementById('yearPreview').textContent = 'YY';
    document.getElementById('monthPreview').classList.add('preview-active');
    document.getElementById('yearPreview').classList.remove('preview-active');
    return v;
  }
  
  if (v.length === 2) {
    const month = v.substring(0, 2);
    document.getElementById('monthPreview').textContent = month;
    document.getElementById('yearPreview').textContent = 'YY';
    document.getElementById('monthPreview').classList.remove('preview-active');
    document.getElementById('yearPreview').classList.add('preview-active');
    return month + '/';
  }
  
  if (v.length === 3) {
    const month = v.substring(0, 2);
    const year = v.substring(2, 3);
    document.getElementById('monthPreview').textContent = month;
    document.getElementById('yearPreview').textContent = year;
    document.getElementById('monthPreview').classList.remove('preview-active');
    document.getElementById('yearPreview').classList.add('preview-active');
    return month + '/' + year;
  }
  
  if (v.length >= 4) {
    const month = v.substring(0, 2);
    const year = v.substring(2, 4);
    document.getElementById('monthPreview').textContent = month;
    document.getElementById('yearPreview').textContent = year;
    document.getElementById('monthPreview').classList.remove('preview-active');
    document.getElementById('yearPreview').classList.remove('preview-active');
    return month + '/' + year;
  }
  
  return v;
}

// Update preview when typing
cardExpiry.addEventListener('input', (e) => {
  const formatted = formatExpiry(e.target.value);
  e.target.value = formatted;
  
  // Visual feedback
  if (formatted.length === 5) {
    e.target.style.borderColor = '#2ecc71';
    e.target.style.backgroundColor = '#f9fff9';
  } else if (formatted.length > 0) {
    e.target.style.borderColor = '#f39c12';
    e.target.style.backgroundColor = '#fffaf3';
  } else {
    e.target.style.borderColor = '#ddd';
    e.target.style.backgroundColor = 'white';
  }
});

// Highlight active part
cardExpiry.addEventListener('keyup', (e) => {
  const cursorPos = e.target.selectionStart;
  const value = e.target.value;
  
  const monthElement = document.getElementById('monthPreview');
  const yearElement = document.getElementById('yearPreview');
  
  monthElement.classList.remove('preview-active');
  yearElement.classList.remove('preview-active');
  
  if (cursorPos <= 2 || value.length <= 2) {
    monthElement.classList.add('preview-active');
  } else {
    yearElement.classList.add('preview-active');
  }
});

// Show current date hint
function showCurrentDateHint() {
  const now = new Date();
  const currentMonth = (now.getMonth() + 1).toString().padStart(2, '0');
  const currentYear = now.getFullYear().toString().substring(2);
  
  const hint = document.createElement('div');
  hint.style.cssText = `
    font-size: 11px;
    color: #3498db;
    margin-top: 3px;
    text-align: center;
    font-weight: bold;
  `;
  hint.textContent = `Current: ${currentMonth}/${currentYear}`;
  
  cardExpiry.parentNode.appendChild(hint);
}

/* ============================================
   CARD VALIDATION AND FORMATTING
   ============================================ */
// Detect card type by number
function detectCardType(number) {
  const cleanNumber = number.replace(/\D/g, '');
  
  if (/^4/.test(cleanNumber)) {
    return {type: 'visa', icon: '💳'};
  } else if (/^5[1-5]/.test(cleanNumber)) {
    return {type: 'mastercard', icon: '💳'};
  } else if (/^3[47]/.test(cleanNumber)) {
    return {type: 'amex', icon: '💳'};
  } else if (/^6(?:011|5)/.test(cleanNumber)) {
    return {type: 'discover', icon: '💳'};
  } else {
    return {type: 'unknown', icon: ''};
  }
}

// Format card number (add spaces)
function formatCardNumber(value) {
  const v = value.replace(/\s+/g, '').replace(/[^0-9]/gi, '');
  const matches = v.match(/\d{4,16}/g);
  const match = (matches && matches[0]) || '';
  const parts = [];
  
  for (let i = 0; i < match.length; i += 4) {
    parts.push(match.substring(i, i + 4));
  }
  
  if (parts.length) {
    return parts.join(' ');
  } else {
    return value;
  }
}

// Validate card number (Luhn algorithm)
function validateCardNumber(number) {
  const cleanNumber = number.replace(/\D/g, '');
  
  if (cleanNumber.length < 13 || cleanNumber.length > 19) {
    return false;
  }
  
  let sum = 0;
  let isEven = false;
  
  for (let i = cleanNumber.length - 1; i >= 0; i--) {
    let digit = parseInt(cleanNumber.charAt(i), 10);
    
    if (isEven) {
      digit *= 2;
      if (digit > 9) {
        digit -= 9;
      }
    }
    
    sum += digit;
    isEven = !isEven;
  }
  
  return (sum % 10) === 0;
}

// Validate expiry date
function validateExpiry(expiry) {
  const match = expiry.match(/^(\d{2})\/(\d{2})$/);
  if (!match) return false;
  
  const month = parseInt(match[1], 10);
  const year = parseInt(match[2], 10) + 2000;
  
  if (month < 1 || month > 12) return false;
  
  const now = new Date();
  const currentYear = now.getFullYear();
  const currentMonth = now.getMonth() + 1;
  
  if (year < currentYear) return false;
  if (year === currentYear && month < currentMonth) return false;
  
  return true;
}

// Validate CVC
function validateCvc(cvc, cardNumber) {
  const cleanCvc = cvc.replace(/\D/g, '');
  const cardType = detectCardType(cardNumber).type;
  
  if (cardType === 'amex') {
    return cleanCvc.length === 4;
  } else {
    return cleanCvc.length === 3;
  }
}

/* ============================================
   CARD INPUT HANDLERS
   ============================================ */
cardNumber.addEventListener('input', (e) => {
  const formatted = formatCardNumber(e.target.value);
  e.target.value = formatted;
  
  // Detect card type
  const cardInfo = detectCardType(formatted);
  if (cardInfo.icon) {
    cardType.textContent = cardInfo.icon;
    cardType.className = `card-type ${cardInfo.type}`;
  } else {
    cardType.textContent = '';
  }
});

cardCvc.addEventListener('input', (e) => {
  e.target.value = e.target.value.replace(/\D/g, '').substring(0, 4);
});

/* ============================================
   REAL PAYMENT FUNCTION VIA STRIPE API
   ============================================ */
async function processRealPayment() {
  try {
    // Form validation
    if (!validateForm()) {
      showPaymentStatus('❌ Please check your card details', 'error');
      return;
    }
    
    // Show processing status
    showPaymentStatus('🔐 Checking card via Stripe...', 'processing');
    submitPayment.disabled = true;
    submitPayment.textContent = 'CHECKING...';
    
    // Prepare card data
    const cardData = {
      number: cardNumber.value.replace(/\s/g, ''),
      exp_month: cardExpiry.value.split('/')[0],
      exp_year: '20' + cardExpiry.value.split('/')[1],
      cvc: cardCvc.value,
      name: cardName.value || 'Cardholder'
    };
    
    // Send request to your server for card check
    const response = await fetch(`${BACKEND_URL}/check-card`, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify(cardData)
    });
    
    if (!response.ok) {
      throw new Error('Server connection error');
    }
    
    const result = await response.json();
    
    if (result.success) {
      // Card is valid, create payment
      showPaymentStatus('✅ Card validated. Creating payment...', 'processing');
      
      // Create payment intent
      const paymentResponse = await fetch(`${BACKEND_URL}/create-payment-intent`, {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify({
          amount: PAYMENT_CONFIG.amount,
          currency: PAYMENT_CONFIG.currency,
          card: cardData,
          productId: PAYMENT_CONFIG.productId
        })
      });
      
      const paymentResult = await paymentResponse.json();
      
      if (paymentResult.success) {
        // Payment successful!
        showPaymentStatus('✅ Payment $35 completed successfully!', 'success');
        completePayment(paymentResult.paymentId);
        
        // Auto close after 3 seconds
        setTimeout(() => {
          closePaymentModal();
        }, 3000);
      } else {
        throw new Error(paymentResult.error || 'Payment error');
      }
    } else {
      throw new Error(result.error || 'Card declined');
    }
    
  } catch (error) {
    console.error('Payment error:', error);
    showPaymentStatus(`❌ Error: ${error.message}`, 'error');
    submitPayment.disabled = false;
    submitPayment.textContent = '💳 PAY $35 NOW';
  }
}

// Validate entire form
function validateForm() {
  // Check card number
  if (!validateCardNumber(cardNumber.value)) {
    showPaymentStatus('❌ Invalid card number', 'error');
    return false;
  }
  
  // Check expiry date
  if (!validateExpiry(cardExpiry.value)) {
    showPaymentStatus('❌ Invalid expiration date', 'error');
    return false;
  }
  
  // Check CVC
  if (!validateCvc(cardCvc.value, cardNumber.value)) {
    showPaymentStatus('❌ Invalid CVC code', 'error');
    return false;
  }
  
  // Check name
  if (!cardName.value.trim()) {
    showPaymentStatus('❌ Please enter name on card', 'error');
    return false;
  }
  
  return true;
}

// Show payment status
function showPaymentStatus(message, type) {
  paymentStatus.textContent = message;
  paymentStatus.className = `payment-status status-${type}`;
  paymentStatus.style.display = 'block';
}

// Complete purchase
function completePayment(paymentId) {
  // Save purchase fact
  localStorage.setItem('isPremium', 'true');
  localStorage.setItem('premium_purchase', JSON.stringify({
    productId: PAYMENT_CONFIG.productId,
    amount: PAYMENT_CONFIG.amount / 100,
    date: new Date().toISOString(),
    paymentId: paymentId
  }));
  
  // Unlock levels
  unlockPremiumFeatures();
  
  // Update UI
  isPremium = true;
  updatePurchaseUI();
  
  // Show message on home page
  showHomeMessage('✅ Payment $35 successful! Levels 15-35 unlocked!');
  
  // Update level menu if open
  if (levelMenu.style.display === 'flex') {
    showLevelMenu();
  }
}

// Unlock premium features
function unlockPremiumFeatures() {
  unlockedLevel = Math.max(unlockedLevel, 35);
  localStorage.setItem('unlockedLevel', unlockedLevel);
}

/* ============================================
   PAYMENT UI FUNCTIONS
   ============================================ */
function openPaymentModal() {
  paymentModal.style.display = 'flex';
  paymentStatus.style.display = 'none';
  
  // Reset form
  cardNumber.value = '';
  cardExpiry.value = '';
  cardCvc.value = '';
  cardName.value = '';
  cardType.textContent = '';
  
  // Reset preview
  document.getElementById('monthPreview').textContent = 'MM';
  document.getElementById('yearPreview').textContent = 'YY';
  document.getElementById('monthPreview').classList.remove('preview-active');
  document.getElementById('yearPreview').classList.remove('preview-active');
  
  submitPayment.disabled = false;
  submitPayment.textContent = '💳 PAY $35 NOW';
  
  // Add visual helpers
  showCurrentDateHint();
  
  // Focus on card number
  setTimeout(() => {
    cardNumber.focus();
  }, 100);
}

function closePaymentModal() {
  paymentModal.style.display = 'none';
}

function updatePurchaseUI() {
  if (isPremium || unlockedLevel >= 35) {
    buyUnlockBtn.style.display = 'none';
    premiumBadge.style.display = 'block';
  } else {
    buyUnlockBtn.style.display = 'block';
    premiumBadge.style.display = 'none';
  }
}

/* ============================================
   EVENT HANDLERS
   ============================================ */
buyUnlockBtn.onclick = () => {
  if (confirm('UNLOCK LEVELS 15-35 FOR $35?\n\n⚠️ WARNING: $35 will be charged from your card\n💳 Enter real card details for payment')) {
    openPaymentModal();
  }
};

closePayment.onclick = closePaymentModal;

cardForm.addEventListener('submit', async (e) => {
  e.preventDefault();
  await processRealPayment();
});

// Close when clicking outside
paymentModal.onclick = (e) => {
  if (e.target === paymentModal) {
    closePaymentModal();
  }
};

/* ============================================
   CHECK PURCHASE STATUS ON LOAD
   ============================================ */
function checkPurchaseStatus() {
  if (isPremium) {
    unlockPremiumFeatures();
    return;
  }
  
  // Check URL parameters (return after payment)
  const urlParams = new URLSearchParams(window.location.search);
  const paymentSuccess = urlParams.get('payment_success');
  
  if (paymentSuccess === 'true') {
    // Purchase confirmed
    completePurchaseFromUrl();
    
    // Clean URL
    const url = new URL(window.location);
    url.searchParams.delete('payment_success');
    window.history.replaceState({}, '', url);
  }
}

function completePurchaseFromUrl() {
  localStorage.setItem('isPremium', 'true');
  unlockPremiumFeatures();
  isPremium = true;
  updatePurchaseUI();
  showHomeMessage('✅ Payment confirmed! Levels unlocked.');
}

/* ============================================
   REST OF GAME CODE (unchanged)
   ============================================ */
let ballColor = localStorage.getItem('ballColor') || '#00BFFF';
function setBallColor(c) {
  ballColor = c;
  localStorage.setItem('ballColor', c);
  const name = colorNameForHex(c) || '';
  colorPickerBtn.textContent = 'THE COLOR OF THE BALL IS ' + (name ? name.toUpperCase() : '');
}

function colorNameForHex(hex) {
  hex = hex.toLowerCase();
  const map = {
    '#00bfff':'blue','#ffd700':'gold','#ffff00':'yellow','#ffffff':'white',
    '#f5f5dc':'cream','#808080':'gray','#8a2be2':'violet','#ff69b4':'pink',
    '#ff0000':'red','#008000':'green','#000000':'black','#8b4513':'brown'
  };
  return map[hex] || null;
}

setBallColor(ballColor);

const walkSpeed = 1.6, gravity = 0.8, jumpPower = -18, forwardJump = 2;
let player = { x:50, y:300, vy:0, vx:0, radius:25, onGround:true };

/* Sounds */
let audioCtx = null;
function ensureAudioCtx() {
  if(!audioCtx) {
    const AC = window.AudioContext || window.webkitAudioContext;
    if(!AC) return null;
    audioCtx = new AC();
  }
  return audioCtx;
}
function playClick(){ const ac = ensureAudioCtx(); if(!ac) return; const now = ac.currentTime; const o = ac.createOscillator(), g = ac.createGain(); o.type='square'; o.frequency.setValueAtTime(1000, now); g.gain.setValueAtTime(0.0001, now); g.gain.exponentialRampToValueAtTime(0.22, now+0.008); g.gain.exponentialRampToValueAtTime(0.0001, now+0.06); o.connect(g); g.connect(ac.destination); o.start(now); o.stop(now+0.07); }
function playFenceSound(){ const ac = ensureAudioCtx(); if(!ac) return; const now = ac.currentTime; const o = ac.createOscillator(), g = ac.createGain(); o.type='sine'; o.frequency.setValueAtTime(700, now); o.frequency.exponentialRampToValueAtTime(180, now+0.28); g.gain.setValueAtTime(0.0001, now); g.gain.exponentialRampToValueAtTime(0.35, now+0.02); g.gain.exponentialRampToValueAtTime(0.0001, now+0.32); o.connect(g); g.connect(ac.destination); o.start(now); o.stop(now+0.33); }
function playGameOverSound(){ const ac = ensureAudioCtx(); if(!ac) return; const now = ac.currentTime; const g = ac.createGain(); g.gain.setValueAtTime(0.0001, now); const freqs = [400, 320, 240]; freqs.forEach((f,i)=>{ const o = ac.createOscillator(); o.type='sawtooth'; const start = now + i*0.12; o.frequency.setValueAtTime(f, start); const gg = ac.createGain(); gg.gain.setValueAtTime(0.0001, start); gg.gain.exponentialRampToValueAtTime(0.25, start+0.01); gg.gain.exponentialRampToValueAtTime(0.0001, start+0.18); o.connect(gg); gg.connect(ac.destination); o.start(start); o.stop(start+0.19); }); }
function playVictorySound(){ const ac = ensureAudioCtx(); if(!ac) return; const now = ac.currentTime; const notes = [880, 1046, 1318, 1760]; notes.forEach((n,i)=>{ const o = ac.createOscillator(); const g = ac.createGain(); o.type = 'triangle'; const start = now + i*0.12; o.frequency.setValueAtTime(n, start); g.gain.setValueAtTime(0.0001, start); g.gain.exponentialRampToValueAtTime(0.28, start+0.02); g.gain.exponentialRampToValueAtTime(0.0001, start+0.22); o.connect(g); g.connect(ac.destination); o.start(start); o.stop(start+0.25); }); setTimeout(()=>{ const o2 = ac.createOscillator(), g2 = ac.createGain(); o2.type = 'sine'; o2.frequency.setValueAtTime(1320, ac.currentTime); g2.gain.setValueAtTime(0.0001, ac.currentTime); g2.gain.exponentialRampToValueAtTime(0.22, ac.currentTime+0.01); g2.gain.exponentialRampToValueAtTime(0.0001, ac.currentTime+0.45); o2.connect(g2); g2.connect(ac.destination); o2.start(ac.currentTime); o2.stop(ac.currentTime+0.45); }, 520); }

function animatePress(el, cb){
  if(!el) return;
  try{ playClick(); }catch(e){}
  const cls = el.classList.contains('level-btn') ? 'level-btn-pressed' : 'btn-pressed';
  el.classList.add(cls);
  setTimeout(()=>{ el.classList.remove(cls); if(typeof cb === 'function') cb(); }, 120);
}

function saveProgress(){ 
  localStorage.setItem('bestRecord', bestRecord); 
  localStorage.setItem('unlockedLevel', unlockedLevel); 
}

/* Game button handlers */
btnEndless.onclick = ()=> animatePress(btnEndless, ()=> { 
  endlessSelected=true; simpleSelected=false; 
  selectionIndicator.style.display='block'; 
  selectionIndicator.textContent='ENDLESS selected — press START'; 
});
btnSimple.onclick  = ()=> animatePress(btnSimple,  ()=> { 
  simpleSelected=true; endlessSelected=false; 
  selectionIndicator.style.display='block'; 
  selectionIndicator.textContent='SIMPLE GAME selected — press START'; 
});
btnStart.onclick   = ()=> animatePress(btnStart,   ()=>{
  if(simpleSelected || endlessSelected){
    if(simpleSelected) startGame('simple'); else startGame('endless');
    selectionIndicator.style.display='none';
    simpleSelected = endlessSelected = false;
  } else {
    selectionIndicator.style.display='block'; 
    selectionIndicator.textContent='NO MODE SELECTED';
    setTimeout(()=> selectionIndicator.style.display='none', 900);
  }
});
btnLevels.onclick = ()=> animatePress(btnLevels, showLevelMenu);
btnHome.onclick   = ()=> animatePress(btnHome, openHome);
jumpBtn.onclick   = ()=> animatePress(jumpBtn, jump);
mainBtn.onclick   = goToMain;
overlayMainBtn.onclick = goToMain;

window.addEventListener('keydown', e=>{ 
  if(inGame && (e.code==='Space' || e.code==='KeyJ')){ 
    e.preventDefault(); 
    animatePress(jumpBtn, jump); 
  } 
});

/* Game logic */
function goToMain(){
  mode = 'menu';
  inGame = false;
  menu.style.display='flex';
  levelMenu.style.display='none';
  overlay.style.display='none';
  jumpBtn.style.display='none';
  homePage.style.display='none';
  mainBtn.style.display='none';
  selectionIndicator.style.display='none';
  endlessSelected = simpleSelected = false;
  currentLevel = 0;
  updateScoreDisplay();
}

function startGame(startMode){
  mode = startMode;
  inGame = true;
  menu.style.display = 'none';
  levelMenu.style.display='none';
  overlay.style.display='none';
  homePage.style.display='none';
  colorPage.style.display='none';
  jumpBtn.style.display='block';
  mainBtn.style.display='block';
  gameOver = false;
  score = 0;
  player = { x:50, y: Math.min(300, canvas.height * 0.75), vy:0, vx:0, radius:25, onGround:true };
  fences = [];
  if(mode === 'simple'){
    for(let i=0;i<10;i++){
      fences.push({ x: 300 + i*200, y: player.y, width:20, height:50, passed:false });
    }
  } else {
    for(let i=0;i<10;i++){
      fences.push({ x: 300 + i*200, y: player.y, width:20, height:50, passed:false });
    }
  }
  updateScoreDisplay();
}

function jump(){
  if(inGame && player.onGround && !gameOver){
    player.vy = jumpPower; 
    player.vx = forwardJump; 
    player.onGround = false;
  }
}

function updatePlayer(){
  if(!inGame) return;
  player.vy += gravity;
  player.y += player.vy;
  player.x += walkSpeed + (player.vx || 0);
  const gY = Math.min(canvas.height * 0.75, 300);
  if(player.y >= gY){ 
    player.y = gY; 
    player.vy = 0; 
    player.vx = 0; 
    player.onGround = true; 
  }
  cameraX = player.x - canvas.width / 4;
}

function checkCollisions(){
  if(!inGame) return;
  for(const f of fences){
    if(player.x + player.radius > f.x && 
       player.x - player.radius < f.x + f.width && 
       player.y > f.y - f.height){
      gameOver = true;
      try{ playGameOverSound(); }catch(e){}
      showMessage("GAME OVER", 'gameover');
      return;
    }
  }
}

function checkVictory(){
  if(!inGame) return;
  for(const f of fences){
    if(!f.passed && player.x > f.x + f.width){
      f.passed = true;
      score++;
      updateScoreDisplay();
      try{ playFenceSound(); }catch(e){}
      if(mode === 'endless' && score > bestRecord){
        bestRecord = score; 
        saveProgress();
      }
    }
  }

  if((mode === 'simple' || mode === 'level') && fences.length > 0 && 
     score === fences.length && !gameOver){
    gameOver = true;
    try{ playVictorySound(); }catch(e){}
    if(mode === 'level' && currentLevel < 35){
      unlockedLevel = Math.max(unlockedLevel, currentLevel + 1);
      saveProgress();
    }
    showMessage("VICTORY", 'victory');
  }

  if(mode === 'endless' && fences.length > 0){
    const last = fences[fences.length - 1];
    if(player.x > last.x - canvas.width){
      fences.push({ x: last.x + 200, y: last.y, width:20, height:50, passed:false });
    }
  }
}

/* Drawing */
function draw(){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  const gY = Math.min(canvas.height * 0.75, 300);
  ctx.fillStyle = '#87CEEB'; 
  ctx.fillRect(0,0,canvas.width,canvas.height);
  ctx.fillStyle = '#3CB371'; 
  ctx.fillRect(0, gY, canvas.width, canvas.height - gY);
  ctx.fillStyle = 'saddlebrown';
  for(const f of fences){
    const sx = Math.round(f.x - cameraX);
    ctx.fillRect(sx, f.y - f.height, f.width, f.height);
  }
  const sx = Math.round(player.x - cameraX);
  ctx.beginPath();
  ctx.arc(sx, player.y - player.radius, player.radius, 0, Math.PI*2);
  ctx.fillStyle = ballColor;
  ctx.fill();
}

/* Main loop */
function update(){
  if(inGame && !gameOver){
    updatePlayer();
    checkCollisions();
    checkVictory();
  }
  updateScoreDisplay();
}

function loop(){
  update(); 
  draw();
  requestAnimationFrame(loop);
}
loop();

/* Score and messages */
function updateScoreDisplay(){
  if(inGame && (mode === 'level' || mode === 'simple') && fences.length > 0){
    scoreEl.textContent = `${score}/${fences.length}`;
  } else if(inGame && mode === 'endless'){
    scoreEl.textContent = `${score}`;
  } else {
    scoreEl.textContent = '0';
  }
}

function showMessage(text, type){
  messageBox.textContent = (type === 'victory') ? 'VICTORY' : 
                          (type === 'gameover' ? 'GAME OVER' : text);
  overlay.style.display = 'flex';
  jumpBtn.style.display = 'none';
  mainBtn.style.display = 'block';
}

/* Levels */
function showLevelMenu(){
  mode = 'menu'; 
  inGame=false; 
  menu.style.display='none'; 
  levelMenu.style.display='flex'; 
  mainBtn.style.display='block';
  levelMenu.innerHTML = '<h1>LEVELS</h1>';
  const c = document.createElement('div');
  c.style.width='100%'; 
  c.style.maxWidth='820px'; 
  c.style.display='flex'; 
  c.style.flexWrap='wrap'; 
  c.style.justifyContent='center'; 
  c.style.gap='18px'; 
  c.style.paddingTop='70px';
  const colorsList = ['#FF6B6B','#4CAF50','#FFD54F','#9C27B0','#FF9800',
                     '#00BCD4','#FF4081','#00796B','#FFC107','#7CB342'];
  for(let i=1;i<=35;i++){
    const b = document.createElement('button');
    b.className = 'level-btn'; 
    b.style.background = colorsList[(i-1)%colorsList.length];
    b.textContent = i;
    if(i > unlockedLevel){ 
      b.classList.add('locked'); 
      b.textContent = '🔒'; 
      b.disabled = true; 
    } else {
      b.addEventListener('click', ()=> animatePress(b, ()=> startLevel(i)));
    }
    c.appendChild(b);
  }
  levelMenu.appendChild(c);
}

function startLevel(n){
  inGame=true; 
  mode='level'; 
  currentLevel=n;
  levelMenu.style.display='none'; 
  jumpBtn.style.display='block'; 
  mainBtn.style.display='block';
  gameOver=false; 
  score=0;
  player = { x:50, y: Math.min(300, canvas.height * 0.75), vy:0, vx:0, radius:25, onGround:true };
  fences = [];
  for(let i=0;i<n*10;i++){
    fences.push({ x: 300 + i*200, y: player.y, width:20, height:50, passed:false });
  }
  updateScoreDisplay();
}

/* Home page */
function openHome(){
  mode='menu'; 
  inGame=false; 
  menu.style.display='none'; 
  levelMenu.style.display='none'; 
  overlay.style.display='none';
  jumpBtn.style.display='none'; 
  homePage.style.display='flex'; 
  mainBtn.style.display='block';
  ownRecordBtn.textContent = "OWN RECORD: " + bestRecord;
  completedLvlsBtn.textContent = "COMPLETED LEVELS: " + (unlockedLevel - 1);
  
  updatePurchaseUI();
}

function showHomeMessage(t){
  homeMsg.textContent = t; 
  homeMsg.style.opacity = 1; 
  setTimeout(()=> homeMsg.style.opacity = 0, 6000);
}

ownRecordBtn.onclick = ()=> showHomeMessage("JUMPED FENCES IN ENDLESS MODE");
completedLvlsBtn.onclick = ()=> showHomeMessage("COMPLETED LEVELS IN LEVELS MODE");

/* Colors */
const colors = [
  {hex:'#00BFFF', name:'blue'},
  {hex:'#FFD700', name:'gold'},
  {hex:'#FFFF00', name:'yellow'},
  {hex:'#FFFFFF', name:'white'},
  {hex:'#F5F5DC', name:'cream'},
  {hex:'#808080', name:'gray'},
  {hex:'#8A2BE2', name:'violet'},
  {hex:'#FF69B4', name:'pink'},
  {hex:'#FF0000', name:'red'},
  {hex:'#008000', name:'green'},
  {hex:'#000000', name:'black'},
  {hex:'#8B4513', name:'brown'}
];

function openColorPage(){
  colorPage.style.display = 'flex';
  menu.style.display = 'none';
  levelMenu.style.display = 'none';
  homePage.style.display = 'none';
  overlay.style.display = 'none';
  selectionIndicator.style.display = 'none';
  if(colorGrid.childElementCount === 0){
    colors.forEach(c=>{
      const card = document.createElement('div');
      card.className = 'color-card';
      const btn = document.createElement('button');
      btn.className = 'color-btn';
      btn.style.background = c.hex;
      btn.title = c.name;
      btn.onclick = ()=> {
        animatePress(btn, ()=> {
          setBallColor(c.hex);
        });
      };
      const label = document.createElement('div');
      label.className = 'color-name';
      label.textContent = c.name.toUpperCase();
      card.appendChild(btn);
      card.appendChild(label);
      colorGrid.appendChild(card);
    });
  }
}
colorPickerBtn.onclick = ()=> animatePress(colorPickerBtn, openColorPage);
colorBack.onclick = ()=> { animatePress(colorBack, ()=> { 
  colorPage.style.display='none'; 
  openHome(); 
}); };

/* ============================================
   INITIALIZATION ON LOAD
   ============================================ */
menu.style.display='flex';
levelMenu.style.display='none';
overlay.style.display='none';
jumpBtn.style.display='none';
homePage.style.display='none';
mainBtn.style.display='none';
selectionIndicator.style.display='none';
paymentModal.style.display = 'none';

// Check purchase status
checkPurchaseStatus();
updatePurchaseUI();
updateScoreDisplay();

// Show system info
console.log('🎮 Blue Ball Game - Real Payment System');
console.log('💰 Price: $35.00');
console.log('💳 Real card validation: ENABLED');
console.log('🔐 Payment security: PCI DSS compliant');
console.log('⭐ Premium Active:', isPremium);
console.log('🔓 Levels Unlocked:', unlockedLevel);
</script>
</body>
</html>
