<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>個人記帳網站</title>
    <style>
        :root {
            --primary-color: #B8C1C1; /* 默認莫蘭迪色系 */
            --background-color: #F0F0F0; /* 背景色 */
            --font-color: #333333; /* 字體顏色 */
        }

        body {
            background-color: var(--background-color);
            color: var(--font-color);
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: var(--primary-color);
            padding: 20px;
            text-align: center;
        }

        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .toggle-style {
            margin: 20px 0;
            text-align: center;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }

        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: center;
        }

        th {
            background-color: var(--primary-color);
        }

        .cute-style {
            --primary-color: #FFD5E5;
            --background-color: #FFF0F5;
            --font-color: #FF69B4;
        }

        .minimalist-style {
            --primary-color: #B8C1C1;
            --background-color: #F0F0F0;
            --font-color: #333333;
        }
    </style>
</head>
<body>
    <header>
        <h1>個人記帳網站</h1>
    </header>

    <div class="container">
        <div class="toggle-style">
            <label>切換風格：</label>
            <button onclick="setStyle('minimalist')">簡約風</button>
            <button onclick="setStyle('cute')">可愛風</button>
        </div>

        <h2>記帳記錄</h2>
        <table>
            <thead>
                <tr>
                    <th>日期</th>
                    <th>分類</th>
                    <th>支出</th>
                    <th>收入</th>
                    <th>備註</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>2024/08/09</td>
                    <td>餐飲</td>
                    <td>300</td>
                    <td>-</td>
                    <td>午餐</td>
                </tr>
                <!-- 更多記錄可以在這裡添加 -->
            </tbody>
        </table>
    </div>

    <script>
        function setStyle(style) {
            if (style === 'cute') {
                document.body.classList.remove('minimalist-style');
                document.body.classList.add('cute-style');
            } else {
                document.body.classList.remove('cute-style');
                document.body.classList.add('minimalist-style');
            }
        }

        // 預設樣式
        setStyle('minimalist');
    </script>
</body>
</html>
