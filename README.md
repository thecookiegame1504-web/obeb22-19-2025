<!doctype html>
<html lang="ru">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Алхимия Диалога — регистрация</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --gold:#d6b24a;
      --bg:#071018;
      --muted:#9b8f6a;
      --ornament:#4a3b18;
    }
    html,body{height:100%;}
    body{
      margin:0; padding:0; font-family:'Montserrat',sans-serif;
      background: radial-gradient(ellipse at center, rgba(12,18,22,0.95) 0%, rgba(3,6,8,1) 60%), var(--bg);
      color:#efe6d5;
      display:flex; align-items:center; justify-content:center;
      padding:20px;
      box-sizing:border-box;
    }
    .card{
      width:100%; max-width:960px;
      border-radius:14px; overflow:hidden;
      box-shadow:0 20px 60px rgba(0,0,0,0.7);
      display:grid; grid-template-columns:1fr 420px; min-height:640px;
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.25));
      position:relative;
    }
    .poster{
      position:relative; padding:44px; display:flex; flex-direction:column; align-items:center; justify-content:center;
      background: radial-gradient(circle at center, rgba(214,178,74,0.06) 0%, transparent 70%), repeating-radial-gradient(circle at center, transparent 0, rgba(214,178,74,0.03) 2px, transparent 4px);
    }
    .poster::before{
      content:""; position:absolute; inset:0; background:
      radial-gradient(circle at 20% 30%, rgba(214,178,74,0.05) 0%, transparent 50%),
      radial-gradient(circle at 80% 70%, rgba(214,178,74,0.04) 0%, transparent 50%);
      pointer-events:none;
    }
    .poster .title{
      color:var(--gold); font-family:'Playfair Display',serif; font-weight:900; font-size:48px; text-align:center; letter-spacing:2px; text-transform:uppercase; text-shadow:0 2px 8px rgba(0,0,0,0.7);
    }
    .poster .subtitle{color:var(--muted); font-style:italic; margin-top:8px; font-family:'Playfair Display',serif;}
    .ornaments{
      position:absolute; inset:0; pointer-events:none; overflow:hidden;
    }
    .ornaments::before, .ornaments::after{
      content:""; position:absolute; width:120px; height:120px; border:2px solid var(--ornament); border-radius:50%; opacity:0.2;
      animation:spin 60s linear infinite;
    }
    .ornaments::before{top:-40px; left:-40px;}
    .ornaments::after{bottom:-40px; right:-40px;}
    @keyframes spin{from{transform:rotate(0deg);} to{transform:rotate(360deg);}}

    .form-wrap{
      padding:40px 36px; background:linear-gradient(180deg, rgba(5,7,10,0.6), rgba(3,4,6,0.9)); display:flex; flex-direction:column; gap:18px;
    }
    .badge{color:var(--gold); font-family:'Playfair Display',serif; font-size:20px;}
    .when{font-family:'Playfair Display',serif; color:var(--gold); font-size:28px; margin-top:6px;}
    .muted{color:var(--muted); font-size:14px;}

    form{display:flex; flex-direction:column; gap:14px; margin-top:12px;}
    label{font-size:13px; color:#e6dcc4;}
    input[type=text],input[type=email],input[type=tel],textarea{
      width:100%; background:rgba(255,255,255,0.03); border:1px solid rgba(255,255,255,0.1);
      padding:12px 14px; border-radius:8px; color:#fff; font-size:15px;
      box-sizing:border-box; transition:box-shadow .18s,border-color .18s;
    }
    input:focus,textarea:focus{border-color:rgba(214,178,74,0.8); box-shadow:0 0 8px rgba(214,178,74,0.25);}
    textarea{min-height:120px; resize:vertical;}

    .row{display:flex; flex-wrap:wrap; gap:10px;}
    .row .col{flex:1 1 45%; min-width:0;}

    .submit{
      margin-top:6px; background:linear-gradient(180deg, rgba(214,178,74,0.95), rgba(170,130,40,0.95)); color:#081018; border:none;
      padding:12px 16px; border-radius:10px; cursor:pointer; font-weight:700; font-size:16px;
      box-shadow:0 10px 30px rgba(214,178,74,0.14), inset 0 -2px 0 rgba(0,0,0,0.08);
    }
    .submit:hover{filter:brightness(1.1);}

    .note{font-size:13px; color:var(--muted); margin-top:6px;}
    .success{display:none; padding:12px; border-radius:10px; background:rgba(20,40,20,0.4); color:#dff1da; border:1px solid rgba(200,220,190,0.06);}
    footer.small{margin-top:auto; color:var(--muted); font-size:12px;}

    @media (max-width:900px){
      .card{grid-template-columns:1fr;}
      .poster{min-height:320px; padding:30px;}
      .form-wrap{padding:28px;}
    }
  </style>
</head>
<body>
  <div class="card" role="main">
    <div class="poster">
      <div class="ornaments"></div>
      <div style="z-index:2; text-align:center;">
        <div class="title">Алхимия Диалога</div>
        <div class="subtitle">Синтез вашего Я-Золота</div>
      </div>
    </div>
    <div class="form-wrap">
      <div>
        <div class="badge">Регистрация на мероприятие</div>
        <div class="when">17 ноября — 14:00</div>
        <div class="muted">Ауд. 804 • Практическая мастерская по переводу конфликтов в понимание</div>
      </div>
      <form id="regForm" autocomplete="on">
        <div class="row">
          <div class="col">
            <label for="fname">Имя и фамилия</label>
            <input id="fname" name="fullname" type="text" placeholder="Иван Иванов" required />
          </div>
          <div class="col">
            <label for="phone">Телефон</label>
            <input id="phone" name="phone" type="tel" placeholder="+7 (___) ___‑__‑__" />
          </div>
        </div>
        <label for="email">E‑mail</label>
        <input id="email" name="email" type="email" placeholder="name@example.com" required />
        <label for="role">Кого вы представляете (опционально)</label>
        <input id="role" name="role" type="text" placeholder="Компания / Группа / Индивидуально" />
        <label for="note">Короткая заметка / ожидания</label>
        <textarea id="note" name="note" placeholder="Что бы вы хотели получить от встречи?"></textarea>
        <button type="submit" class="submit">Зарегистрироваться — 17 ноя, 14:00</button>
        <div id="success" class="success" role="status" aria-live="polite">Спасибо! Ваша заявка принята. Мы отправим подтверждение на ваш e‑mail.</div>
        <div class="note">Все поля, отмеченные звёздочкой, обязательны. Место ограничено.</div>
      </form>
      <footer class="small">Организаторы: Фаянцева С.А., Королева В.А., Кальянова А.Ю., Санникова З.В., Цыкина Д.А. </footer>
    </div>
  </div>
  <script>
    document.getElementById('regForm').addEventListener('submit', function(e){
      e.preventDefault();
      var btn = this.querySelector('.submit');
      btn.disabled = true; btn.textContent = 'Отправка...';
      setTimeout(function(){
        document.getElementById('success').style.display = 'block';
        btn.textContent = 'Зарегистрировано';
        btn.style.opacity = 0.9;
      }, 900);
    });
  </script>
</body>
</html>
