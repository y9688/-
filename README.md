<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>شبكة هيبر نت H.Net</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to bottom, #e0f7fa, #ffffff);
            text-align: center;
            padding: 20px;
        }
        h1 {
            color: #00796b;
        }
        input[type="text"] {
            padding: 10px;
            width: 250px;
            margin: 10px;
            border: 2px solid #00796b;
            border-radius: 5px;
            font-size: 16px;
        }
        button {
            padding: 10px 30px;
            font-size: 18px;
            background-color: #00796b;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .card-info {
            display: none;
            margin-top: 20px;
            padding: 15px;
            background-color: #c8e6c9;
            border: 2px solid #388e3c;
            border-radius: 10px;
            color: #2e7d32;
            font-weight: bold;
        }
        .footer {
            margin-top: 40px;
            font-size: 14px;
            color: #555;
        }
        .flag {
            width: 80px;
            vertical-align: middle;
            margin-top: 15px;
        }
        .leader-img {
            width: 200px;
            margin-top: 20px;
            border-radius: 10px;
            border: 2px solid #00796b;
        }
        a {
            text-decoration: none;
            color: #00695c;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <h1>مرحباً بك في شبكة هيبر نت (H.Net)</h1>
    <p>أدخل رمز الكرت للاتصال بالإنترنت</p>
    <input type="text" id="codeInput" placeholder="ادخل الرمز هنا">
    <br>
    <button onclick="login()">دخول</button>

    <div class="card-info" id="cardInfo">
        <p>تم تسجيل الدخول بنجاح!</p>
        <p>رقم الكرت: 199809421r2</p>
        <p>السرعة: 5 ميجا</p>
        <p>الرصيد: 2.5 جيجا</p>
        <p>التاريخ: <span id="today"></span></p>
        <p>الوقت الآن: <span id="timeNow"></span></p>
    </div>

    <img src="https://upload.wikimedia.org/wikipedia/commons/0/00/Flag_of_Palestine.svg" class="flag" alt="علم فلسطين">
    
    <br>
    <img src="https://i.ibb.co/zP5n6qv/yemen-nature.jpg" class="leader-img" alt="صورة طبيعة يمنية">

    <div class="footer">
        <p>المهندس: أبو صمود التميمي</p>
        <p>رقم التواصل: 734982602</p>
        <p><a href="https://t.me/sijaqkharsiub" target="_blank">تابعنا على التليجرام</a></p>
    </div>

    <script>
        function login() {
            var code = document.getElementById('codeInput').value;
            if (code === "199809421r2") {
                document.getElementById('cardInfo').style.display = 'block';
            } else {
                alert("رمز غير صحيح. يرجى المحاولة مرة أخرى.");
            }
        }

        function updateDateTime() {
            var now = new Date();
            var date = now.toLocaleDateString('ar-EG');
            var time = now.toLocaleTimeString('ar-EG');
            document.getElementById("today").textContent = date;
            document.getElementById("timeNow").textContent = time;
        }

        setInterval(updateDateTime, 1000);
    </script>

</body>
</html>
