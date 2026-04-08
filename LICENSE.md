<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بوابة الشيخ الطيب المعرفية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --primary: #1a237e; --secondary: #2e7d32; --whatsapp: #25D366; --telegram: #0088cc; --bg: #f8f9fa; }
        body { font-family: 'Segoe UI', Tahoma, sans-serif; background: var(--bg); margin: 0; color: #333; scroll-behavior: smooth; }
        
        /* شريط التنقل */
        nav { background: var(--primary); padding: 12px 0; position: sticky; top: 0; z-index: 2000; }
        .nav-links { display: flex; justify-content: center; gap: 15px; list-style: none; padding: 0; margin: 0; flex-wrap: wrap; }
        .nav-links a { color: white; text-decoration: none; font-weight: 500; font-size: 0.85rem; }

        header { background: linear-gradient(135deg, var(--primary), #3949ab); color: white; padding: 40px 20px; text-align: center; }
        .container { max-width: 1100px; margin: 20px auto; padding: 0 15px; }
        .section-box { background: #fff; border-radius: 20px; padding: 30px; margin-bottom: 30px; box-shadow: 0 5px 15px rgba(0,0,0,0.05); }

        /* الزر العائم والقائمة المنبثقة */
        .fab-wrapper { position: fixed; bottom: 30px; left: 30px; z-index: 9999; display: flex; flex-direction: column; align-items: center; gap: 15px; }
        .fab-main { width: 60px; height: 60px; background: var(--primary); color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 24px; box-shadow: 0 4px 15px rgba(0,0,0,0.3); cursor: pointer; transition: 0.3s; }
        .fab-main:hover { transform: scale(1.1); }
        
        .fab-options { display: none; flex-direction: column; gap: 10px; margin-bottom: 10px; }
        .fab-option { width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; color: white; text-decoration: none; font-size: 20px; box-shadow: 0 4px 10px rgba(0,0,0,0.2); transition: 0.3s; transform: scale(0); animation: popIn 0.3s forwards; }
        
        @keyframes popIn { to { transform: scale(1); } }
        .bg-wa { background: var(--whatsapp); }
        .bg-tg { background: var(--telegram); }

        /* الأقسام والمحتوى */
        .contact-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; }
        .contact-card { padding: 20px; border-radius: 15px; text-align: center; color: white; text-decoration: none; }
        .wa-sdn { background: var(--whatsapp); }
        .wa-qtr { background: #128C7E; }

        footer { background: #111; color: #999; text-align: center; padding: 30px; }
    </style>
</head>
<body>

<div class="fab-wrapper">
    <div class="fab-options" id="fabOptions">
        <a href="https://wa.me/249999876200" class="fab-option bg-wa" title="واتساب السودان"><i class="fab fa-whatsapp"></i></a>
        <a href="https://wa.me/97471375305" class="fab-option bg-wa" style="background:#128C7E" title="واتساب قطر"><i class="fab fa-whatsapp"></i></a>
        <a href="https://t.me/+97471375305" class="fab-option bg-tg" title="تلجرام قطر"><i class="fab fa-telegram-plane"></i></a>
    </div>
    <div class="fab-main" onclick="toggleFab()"><i class="fas fa-comment-dots"></i></div>
</div>

<nav>
    <ul class="nav-links">
        <li><a href="#articlesSection">المقالات</a></li>
        <li><a href="#librarySection">المكتبة</a></li>
        <li><a href="#directContact">اتصل بي</a></li>
    </ul>
</nav>

<header>
    <h1>بوابة الشيخ الطيب المعرفية</h1>
    <p>تواصل سريع وبحث شامل في تاريخ الريف الشمالي</p>
</header>

<div class="container">
    <section id="articlesSection" class="section-box">
        <h2><i class="fas fa-book"></i> الموسوعة التاريخية</h2>
        <p>منطقة الشيخ الطيب.. إرث العلم والزراعة في قلب السودان.</p>
    </section>

    <section id="librarySection" class="section-box">
        <h2><i class="fas fa-university"></i> المكتبة الإلكترونية</h2>
        <p>كتب ودراسات عن تاريخ القبائل والزراعة المروية.</p>
    </section>

    <section id="directContact" class="section-box">
        <h2><i class="fas fa-phone-alt"></i> تواصل مباشر</h2>
        <div class="contact-grid">
            <a href="https://wa.me/249999876200" class="contact-card wa-sdn">
                <i class="fab fa-whatsapp"></i>
                <p>واتساب (السودان)</p>
            </a>
            <a href="https://wa.me/97471375305" class="contact-card wa-qtr">
                <i class="fab fa-whatsapp"></i>
                <p>واتساب (قطر)</p>
            </a>
        </div>
    </section>
</div>

<footer>
    <p>بوابة الشيخ الطيب &copy; 2026 | تطوير م. أبو الحسن</p>
</footer>

<script>
    // وظيفة إظهار وإخفاء أزرار التواصل العائمة
    function toggleFab() {
        const options = document.getElementById('fabOptions');
        if (options.style.display === 'flex') {
            options.style.display = 'none';
        } else {
            options.style.display = 'flex';
        }
    }

    // رسالة تنبيه عند الإرسال من النماذج
    document.querySelectorAll('form').forEach(form => {
        form.onsubmit = (e) => {
            e.preventDefault();
            alert("تم استلام طلبك، سيتم الرد عليك عبر وسيلة التواصل المفضلة لديك.");
            form.reset();
        };
    });
</script>

</body>
</html>
