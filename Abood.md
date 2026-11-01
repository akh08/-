<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة رعاية - الخدمات البيطرية الشاملة</title>
    <style>
        :root {
            --primary-color: #0d9488;
            --primary-dark: #0f766e;
            --secondary-color: #f0fdfa;
            --accent-color: #f59e0b;
            --text-color: #1f2937;
            --bg-color: #f8fafc;
            --white: #ffffff;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        /* الهيدر وشريط التنقل */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary-color);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 600;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        .btn {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 0.6rem 1.5rem;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;
        }

        .btn:hover {
            background-color: var(--primary-dark);
        }

        /* قسم البطل (Hero Section) */
        .hero {
            background: linear-gradient(135sdeg, #ccfbf1 0%, #f0fdfa 100%);
            padding: 4rem 2rem;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.5rem;
            color: var(--primary-dark);
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.1rem;
            color: #4b5563;
            max-width: 600px;
            margin: 0 auto 2rem;
        }

        /* الأقسام الرئيسية */
        .container {
            max-width: 1200px;
            margin: 3rem auto;
            padding: 0 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 2.5rem;
            color: var(--text-color);
        }

        /* شبكة الخدمات */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
            text-align: center;
            transition: transform 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .service-card h3 {
            margin-bottom: 0.5rem;
            color: var(--primary-dark);
        }

        /* نموذج حجز موعد تفاعلي */
        .booking-section {
            background: var(--white);
            padding: 3rem;
            border-radius: 16px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            margin-top: 4rem;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        .form-group label {
            font-weight: 600;
            font-size: 0.9rem;
        }

        .form-group input, .form-group select, .form-group textarea {
            padding: 0.8rem;
            border: 1px solid #d1d5db;
            border-radius: 8px;
            font-size: 1rem;
            outline: none;
        }

        .form-group input:focus, .form-group select:focus {
            border-color: var(--primary-color);
        }

        .form-group.full-width {
            grid-column: 1 / -1;
        }

        /* التذييل */
        footer {
            background-color: #111827;
            color: var(--white);
            text-align: center;
            padding: 2rem;
            margin-top: 4rem;
        }

        /* رسالة النجاح */
        .success-msg {
            display: none;
            background-color: #d1fae5;
            color: #065f46;
            padding: 1rem;
            border-radius: 8px;
            text-align: center;
            font-weight: bold;
            margin-top: 1rem;
        }
    </style>
</head>
<body>

    <!-- الهيدر -->
    <header>
        <div class="navbar">
            <div class="logo">
                <span>🐾</span> منصة رعاية البيطرية
            </div>
            <ul class="nav-links">
                <li><a href="#services">الخدمات</a></li>
                <li><a href="#booking">حجز موعد</a></li>
                <li><a href="#emergency">الطوارئ</a></li>
            </ul>
            <button class="btn" onclick="scrollToBooking()">احجز الآن</button>
        </div>
    </header>

    <!-- قسم الترحيب -->
    <section class="hero">
        <h1>رعاية بيطرية متكاملة لصحة أحيائك الأليفة</h1>
        <p>نخبة من الأطباء البيطريين المتخصصين لتقديم أفضل رعاية، فحص دوري، واستشارات فورية على مدار الساعة.</p>
        <button class="btn" onclick="scrollToBooking()">ابدأ حجز موعدك</button>
    </section>

    <!-- الخدمات -->
    <div class="container" id="services">
        <h2 class="section-title">خدماتنا الطبية</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🩺</div>
                <h3>الكشف السريري</h3>
                <p>فحص شامل ودقيق باستخدام أحدث الأجهزة الطبية لتشخيص الحالة بدقة.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">💉</div>
                <h3>التطعيمات والوقاية</h3>
                <p>برامج تحصين متكاملة لحماية حيوانك الأليف من الأمراض المعدية الشائعة.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🏠</div>
                <h3>الزيارات المنزلية</h3>
                <p>خدمة الكشف المبكر والمعالجة الفورية في راحة منزلك لتقليل التوتر.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🚨</div>
                <h3>طوارئ 24/7</h3>
                <p>فريق طوارئ جاهز للتدخل السريع في الحالات الحرجة والحوادث.</p>
            </div>
        </div>
    </div>

    <!-- قسم الحجز -->
    <div class="container" id="booking">
        <div class="booking-section">
            <h2 class="section-title" style="margin-bottom: 1.5rem;">حجز موعد طبي جديد</h2>
            <form id="bookingForm" onsubmit="handleBooking(event)">
                <div class="form-grid">
                    <div class="form-group">
                        <label>اسم المالك</label>
                        <input type="text" id="ownerName" placeholder="أدخل اسمك الكريم" required>
                    </div>
                    <div class="form-group">
                        <label>رقم الهاتف</label>
                        <input type="tel" id="phone" placeholder="05xxxxxxxx" required>
                    </div>
                    <div class="form-group">
                        <label>نوع الحيوان الأليف</label>
                        <select id="petType">
                            <option value="cat">قطة</option>
                            <option value="dog">كلب</option>
                            <option value="bird">طيور</option>
                            <option value="livestock">مواشي / حيوانات أخرى</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>الخدمة المطلوبة</label>
                        <select id="serviceType">
                            <option value="checkup">كشف وعلاج عام</option>
                            <option value="vaccine">تطعيم وقائي</option>
                            <option value="home">زيارة منزلية</option>
                            <option value="emergency">حالة طارئة</option>
                        </select>
                    </div>
                    <div class="form-group full-width">
                        <label>تفاصيل الحالة أو الأعراض</label>
                        <textarea id="notes" rows="3" placeholder="اكتب وصفاً مختصراً لحالة الحيوان..."></textarea>
                    </div>
                </div>
                <button type="submit" class="btn" style="width: 100%; padding: 1rem; font-size: 1.1rem;">تأكيد الحجز</button>
            </form>
            <div id="successMessage" class="success-msg">
                تم استلام طلب حجزك بنجاح! سيقوم فريق العيادة بالتواصل معك قريباً لتأكيد الموعد.
            </div>
        </div>
    </div>

    <!-- التذييل -->
    <footer>
        <p>جميع الحقوق محفوظة © 2026 - منصة رعاية للخدمات البيطرية</p>
    </footer>

    <script>
        function scrollToBooking() {
            document.getElementById('booking').scrollIntoView({ behavior: 'smooth' });
        }

        function handleBooking(event) {
            event.preventDefault();
            const successDiv = document.getElementById('successMessage');
            successDiv.style.display = 'block';
            document.getElementById('bookingForm').reset();
            
            setTimeout(() => {
                successDiv.style.display = 'none';
            }, 5000);
        }
    </script>
</body>
</html>
