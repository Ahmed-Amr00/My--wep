<!doctype html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Ahmed Amr - إسكنات وشحن جواهر مجانًا</title>
  <style>
    :root{--bg:#0f1724;--card:#0b1220;--accent:#ffce00;--muted:#9aa4b2}
    *{box-sizing:border-box;font-family: 'Segoe UI', Tahoma, Arial, sans-serif}
    body{margin:0;min-height:100vh;background:linear-gradient(180deg,#071024 0%, #081428 60%);color:#e6eef8;display:flex;align-items:center;justify-content:center;padding:24px}
    .container{width:100%;max-width:960px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border-radius:14px;padding:22px;box-shadow:0 8px 30px rgba(2,6,23,0.7);border:1px solid rgba(255,255,255,0.03)}
    header{display:flex;align-items:center;gap:14px;flex-wrap:wrap}
    .logo{background:linear-gradient(90deg,var(--accent),#ff8a00);color:#071024;font-weight:700;padding:10px 14px;border-radius:10px;font-size:18px}
    h1{margin:0;font-size:20px}
    p.lead{margin:6px 0 18px;color:var(--muted)}
    .grid{display:grid;grid-template-columns:1fr 380px;gap:18px}
    @media(max-width:880px){.grid{grid-template-columns:1fr} .right{order:-1}}
    .card{background:var(--card);padding:16px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)}
    .skins{display:flex;gap:10px;flex-wrap:wrap}
    .skin{width:88px;height:120px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border-radius:10px;padding:8px;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;cursor:pointer;transition:transform .3s}
    .skin:hover{transform:translateY(-6px) scale(1.05)}
    .skin .icon{width:56px;height:56px;border-radius:8px;background:linear-gradient(135deg,#ffd86b,#ff8a00);display:flex;align-items:center;justify-content:center;color:#071024;font-weight:700}
    label{display:block;margin-bottom:6px;font-size:14px;color:var(--muted)}
    input,select{width:100%;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit}
    .btn{display:inline-block;padding:10px 14px;border-radius:10px;background:linear-gradient(90deg,var(--accent),#ff8a00);color:#071024;font-weight:700;border:none;cursor:pointer;margin-top:10px;transition:transform .2s}
    .btn:hover{transform:scale(1.05)}
    .muted{color:var(--muted);font-size:13px}
    .success{display:none;margin-top:12px;padding:12px;border-radius:10px;background:linear-gradient(90deg, rgba(0,255,100,0.08), rgba(0,255,100,0.04));border:1px solid rgba(0,255,100,0.12);color:#c8ffd0;opacity:0;transition:opacity .6s ease}
    .success.show{display:block;opacity:1}
    .smallnote{font-size:12px;color:var(--muted);margin-top:10px}
    .footer{margin-top:12px;color:var(--muted);font-size:13px;text-align:center}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="logo">Ahmed Amr</div>
      <div>
        <h1>إسكنات وشحن جواهر مجانًا</h1>
        <p class="lead">هذه نسخة تجريبية - لعرض واجهة موقع شحن (غير حقيقي ولا يقبل دفعات).</p>
      </div>
    </header>

    <div class="grid" style="margin-top:16px">
      <div class="card left">
        <h3 style="margin:0 0 10px">أشهر الإسكنات</h3>
        <div class="skins">
          <div class="skin">
            <div class="icon">M1</div>
            <div class="muted" style="margin-top:8px">سكين درب</div>
          </div>
          <div class="skin">
            <div class="icon">M2</div>
            <div class="muted" style="margin-top:8px">سكين نار</div>
          </div>
          <div class="skin">
            <div class="icon">M3</div>
            <div class="muted" style="margin-top:8px">سكين رويال</div>
          </div>
          <div class="skin">
            <div class="icon">M4</div>
            <div class="muted" style="margin-top:8px">سكين الشبح</div>
          </div>
        </div>
        <div style="margin-top:16px" class="smallnote">ملاحظة: هذه العناصر تجريبية للعرض فقط.</div>
      </div>

      <div class="card right">
        <h3 style="margin:0 0 10px">شحن مجانية</h3>
        <form id="chargeForm">
          <label>اكتب ID الحساب</label>
          <input type="text" id="userId" placeholder="مثال: 123456789" required>

          <label style="margin-top:10px">اكتب مستوى الحساب (Level)</label>
          <input type="number" id="level" placeholder="مثال: 45" min="1" required>

          <label style="margin-top:10px">كمية الجواهر المطلوبة</label>
          <select id="amount">
            <option value="50">50 جوهرة</option>
            <option value="100">100 جوهرة</option>
            <option value="250">250 جوهرة</option>
            <option value="500">500 جوهرة</option>
          </select>

          <button class="btn" id="submitBtn">شحن الآن (تجريبي)</button>

          <div class="success" id="successBox">
            تم التحويل بنجاح ✅<br>
            <span class="muted" id="successInfo"></span>
          </div>

          <div class="smallnote">هذا الموقع لعرض واجهة فقط — لا يتم إرسال أو استلام أي أموال أو أكواد.</div>
        </form>
      </div>
    </div>

    <div class="footer">© Ahmed Amr — مثال تجريبي للتعليم فقط</div>
  </div>

  <script>
    const form = document.getElementById('chargeForm');
    const successBox = document.getElementById('successBox');
    const successInfo = document.getElementById('successInfo');
    const submitBtn = document.getElementById('submitBtn');

    form.addEventListener('submit', function(e){
      e.preventDefault();
      const id = document.getElementById('userId').value.trim();
      const lvl = document.getElementById('level').value.trim();
      const amount = document.getElementById('amount').value;

      if(!id || !lvl){
        alert('مطلوب: اكتب ID والمستوى.');
        return;
      }

      submitBtn.disabled = true;
      submitBtn.textContent = 'جاري الشحن...';

      setTimeout(()=>{
        submitBtn.disabled = false;
        submitBtn.textContent = 'شحن الآن (تجريبي)';

        successInfo.textContent = `تم شحن ${amount} جوهرة للحساب (ID: ${id}) - مستوى: ${lvl}`;
        successBox.classList.add('show');
      }, 1100);
    });
  </script>
</body>
</html>
