<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Haki Sochi - مطعم سوشي</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }
        nav {
            background-color: #2c3e50; /* أزرق داكن */
            color: white;
            padding: 10px 20px;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            text-align: center;
        }
        nav ul li {
            display: inline;
            margin: 0 15px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: #f39c12; /* برتقالي للـ hover */
        }
        .hero {
            background-image: url('https://images.unsplash.com/photo-1579584425555-c3ce17fd4351?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding-top: 60px; /* لتجنب الشريط الثابت */
            animation: slideIn 3s ease-out;
        }
        @keyframes slideIn {
            from { transform: translateY(-100px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        .hero h1 {
            font-size: 4em;
            margin: 0;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        .hero p {
            font-size: 1.5em;
            margin: 20px 0;
        }
        .hero button {
            background-color: #e74c3c;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2em;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .hero button:hover {
            background-color: #c0392b;
        }
        .section {
            padding: 80px 20px;
            max-width: 1200px;
            margin: 0 auto;
            background-color: white;
            margin-bottom: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            animation: fadeInUp 1s ease-out;
        }
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .menu {
            text-align: center;
        }
        .menu h2 {
            font-size: 2.5em;
            margin-bottom: 30px;
            color: #2c3e50;
        }
        .menu-items {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
        .menu-item {
            width: 250px;
            margin: 15px;
            background: #8B4513; /* تغيير إلى بني داكن */
            color: white; /* للتباين مع الخلفية البنية */
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .menu-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
        }
        .menu-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
        }
        .gallery {
            background-color: #34495e;
            color: white;
            text-align: center;
        }
        .gallery h2 {
            font-size: 2.5em;
            margin-bottom: 30px;
        }
        .gallery img {
            width: 30%;
            margin: 10px;
            border-radius: 10px;
            transition: transform 0.5s;
        }
        .gallery img:hover {
            transform: scale(1.1) rotate(5deg);
        }
        .contact {
            background-color: white; /* تغيير إلى أبيض */
            color: black; /* تغيير النص إلى أسود للتباين */
            text-align: center;
            border: 2px solid #8B4513; /* حدود بنية للتمييز */
        }
        .contact h2 {
            font-size: 2.5em;
            margin-bottom: 30px;
            color: #8B4513; /* عنوان بني */
        }
        footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 20px;
        }
        @media (max-width: 768px) {
            .menu-items {
                flex-direction: column;
                align-items: center;
            }
            .menu-item {
                width: 100%;
            }
            .gallery img {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <nav>
        <ul>
            <li><a href="#hero">الرئيسية</a></li>
            <li><a href="#menu">القائمة</a></li>
            <li><a href="#gallery">الصور</a></li>
            <li><a href="#contact">الاتصال</a></li>
        </ul>
    </nav>

    <section class="hero" id="hero">
        <div>
            <h1>مرحباً بك في Haki Sochi</h1>
            <p>استمتع بأشهى أطباق السوشي الطازجة!</p>  <!-- النص المحدث هنا -->
            <button onclick="scrollToMenu()">اطلب الآن</button>
        </div>
    </section>

    <section class="section menu" id="menu">
        <h2>قائمة الطعام</h2>
        <div class="menu-items">
            <div class="menu-item">
                <img src="https://images.unsplash.com/photo-1553621042-f6e147245754?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=60" alt="سوشي سلمون">
                <h3>سوشي السلمون</h3>
                <p>طازج وشهي - 50 درهم مغربي</p>
            </div>
            <div class="menu-item">
                <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ca4b?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=60" alt="سوشي تونة">
                <h3>سوشي التونة</h3>
                <p>نكهة قوية - 60 درهم مغربي</p>
            </div>
            <div class="menu-item">
                <img src="https://images.unsplash.com/photo-1579584425555-c3ce17fd4351?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=60" alt="سوشي نباتي">
                <h3>سوشي نباتي</h3>
                <p>للنباتيين - 40 درهم مغربي</p>
            </div>
            <div class="menu-item">
                <img src="https://images.unsplash.com/photo-1513104890138-7c749659a591?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=60" alt="بيتزا">
                <h3>بيتزا مارغريتا</h3>
                <p>جبنة وطماطم - 45 درهم مغربي</p>
            </div>
            <div class="menu-item">
                <img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=60" alt="بيرجر">
                <h3>بيرجر كلاسيكي</h3>
                <p>لحم وخضار - 55 درهم مغربي</p>
            </div>
        </div>
    </section>

    <section class="section gallery" id="gallery">
        <h2>صور من مطعمنا</h2>
        <img src="https://images.unsplash.com/photo-1553621042-f6e147245754?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=60" alt="صورة سوشي">
        <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ca4b?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=60" alt="صورة سوشي">
        <img src="https://images.unsplash.com/photo-1579584425555-c3ce17fd4351?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=60" alt="صورة سوشي">
    </section>

    <section class="section contact" id="contact">
        <h2>اتصل بنا</h2>
        <p>العنوان: شارع محمد الخامس، الدار البيضاء</p>
        <p>الهاتف: 012-3456789</p>
        <p>البريد الإلكتروني: info@hakisushi.com</p>
        <p><a href="https://wa.me/212612345678" target="_blank" style="color: #8B4513; text-decoration: underline;">تواصل عبر WhatsApp: +212 6 12 34 56 78</a></p>
    </section>

    <footer>
        <p>&copy; 2023 Haki Sochi. جميع الحقوق محفوظة.</p>
    </footer>

    <script>
        function scrollToMenu() {
            document.getElementById('menu').scrollIntoView({ behavior: 'smooth' });
        }
        // رسوم متحركة محسنة
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        });
        document.querySelectorAll('.section').forEach(section => {
            observer.observe(section);
            section.style.opacity = '0';
            section.style.transform = 'translateY(50px)';
            section.style.transition = 'opacity 1s, transform 1s';
        });
    </script>
</body>
</html>
