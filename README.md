<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Christmas Surprise</title>
    <style>
        
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: radial-gradient(circle, #b30000, #4d0000); /* خلفية حمراء متدرجة */
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        
        .container {
            background-color: #fff9f5;
            width: 90%;
            max-width: 350px;
            padding: 30px 20px;
            border-radius: 40px; /* حواف منحنية زي الصورة */
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            text-align: center;
            position: relative;
        }

        
        .year-badge {
            background-color: #b32d2e;
            color: white;
            padding: 5px 20px;
            border-radius: 20px;
            display: inline-block;
            font-weight: bold;
            margin-bottom: 20px;
        }

        
        .emoji-header {
            font-size: 50px;
            margin-bottom: 10px;
        }

        h2 {
            color: #b32d2e;
            font-family: 'Georgia', serif;
            font-size: 28px;
            margin-bottom: 20px;
        }

        
        input[type="password"] {
            width: 80%;
            padding: 12px;
            border: 2px solid #ffccd2;
            border-radius: 25px;
            text-align: center;
            margin-bottom: 15px;
            outline: none;
        }

        
        .unlock-btn {
            background: linear-gradient(to bottom, #b32d2e, #801a1b);
            color: white;
            border: none;
            padding: 12px 40px;
            border-radius: 25px;
            font-size: 18px;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            transition: 0.3s;
        }

        .unlock-btn:hover {
            transform: scale(1.05);
        }

        
        #message-screen {
            display: none;
            color: #4d0000;
        }

        .main-title {
            color: #b32d2e;
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .love-letter {
            line-height: 1.8;
            font-size: 16px;
        }

        
        .lights {
            position: absolute;
            top: -15px;
            width: 100%;
            display: flex;
            justify-content: space-around;
        }
        .light {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        .red { background: red; box-shadow: 0 0 10px red; }
        .green { background: green; box-shadow: 0 0 10px green; }
        .yellow { background: yellow; box-shadow: 0 0 10px yellow; }

    </style>
</head>
<body>

    <div class="container">
        <div class="lights">
            <div class="light green"></div>
            <div class="light yellow"></div>
            <div class="light red"></div>
            <div class="light green"></div>
        </div>

        <div id="login-screen">
            <div class="year-badge">2026</div>
            <div class="emoji-header">🎄</div>
            <h2>Christmas</h2>
            <p style="color: #888; font-style: italic;">enter password</p>
            <input type="password" id="passInput" placeholder="Password">
            <br>
            <button class="unlock-btn" onclick="unlock()">🔓 unlock</button>
            <div style="margin-top: 20px; font-size: 24px;">
                ☃️ 💝 🎅 🎁 🎄
            </div>
        </div>

        <div id="message-screen">
            <div style="font-size: 40px;">💌</div>
            <div class="main-title">يا نور عيني</div>
            <div class="love-letter">
                أحلى حد هدخل معاه السنة الجديدة ربنا يخليكي ليا <br>
                يارب تكون سنة حلوة وهتبقى حلوة أصلاً <br>
                لأننا مع بعض وأنا داخل السنة وأنا معايا <br>
                أغلى وأكتر حد بحبه <br>
                أنت سبب فرحي أنتي سبب ضحكتي أنتي <br>
                سبب كل حاجة حلوة <br>
                <b>بحبك</b>
            </div>
            <p style="color: #b32d2e; margin-top: 20px; cursor: pointer;">تعالي نشوف كام ميموري كده مع بعض</p>
        </div>
    </div>

    <script>
        function unlock() {
            const pass = document.getElementById('passInput').value;
            
            if(pass === "13102022") {
                document.getElementById('login-screen').style.display = 'none';
                document.getElementById('message-screen').style.display = 'block';
            } else {
                alert("incorrect password please try again");
            }
        }
    

    </script>
</body>
</html>
