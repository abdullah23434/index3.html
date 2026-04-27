<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <style>
        body { background: #1a1a1a; color: white; font-family: sans-serif; text-align: center; }
        .card { border: 2px solid #00ff00; padding: 20px; margin: 10px; border-radius: 15px; background: #262626; }
        .stat { color: #00ff00; font-weight: bold; }
        h1 { color: #00ff00; text-shadow: 0 0 10px #00ff00; }
    </style>
</head>
<body>
    <h1>رادار الطائرات العالمي ✈️</h1>
    <div id="plane-info" class="card">
        <h2 id="planeName">اختر طائرة للمواصفات</h2>
        <p>السرعة: <span id="speed" class="stat">-</span></p>
        <p>الحمولة (صواريخ/ركاب): <span id="payload" class="stat">-</span></p>
        <p>العدد في العالم: <span id="total" class="stat">-</span></p>
        <button onclick="showNext()">الطائرة التالية ➡️</button>
    </div>

    <script>
        const planes = [
            { name: "F-15SA (النسخة السعودية)", speed: "3,017 كم/س", payload: "12 صاروخ جو-جو", total: "84 حبة في الرياض/الظهران" },
            { name: "بوينج 787 (دريملاينر)", speed: "903 كم/س", payload: "242 - 330 راكب", total: "1,100+ حول العالم" }
        ];
        let index = 0;
        function showNext() {
            let p = planes[index];
            document.getElementById('planeName').innerText = p.name;
            document.getElementById('speed').innerText = p.speed;
            document.getElementById('payload').innerText = p.payload;
            document.getElementById('total').innerText = p.total;
            index = (index + 1) % planes.length;
        }
    </script>
</body>
</html>
