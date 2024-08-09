<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>個人記帳網站</title>
    <style>
        :root {
            --primary-color: #B8C1C1;
            --background-color: #F0F0F0;
            --font-color: #333333;
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

        .login-form, .main-content {
            display: none;
        }

        .login-form.active, .main-content.active {
            display: block;
        }

        .form-group {
            margin-bottom: 15px;
        }

        label {
            display: block;
            margin-bottom: 5px;
        }

        input[type="text"], input[type="password"], input[type="number"], textarea {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
        }

        button {
            background-color: var(--primary-color);
            border: none;
            color: #fff;
            padding: 10px 15px;
            cursor: pointer;
            border-radius: 4px;
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
    </style>
</head>
<body>
    <header>
        <h1>個人記帳網站</h1>
    </header>

    <div class="container">
        <!-- 登入畫面 -->
        <div class="login-form active">
            <h2>用戶登入</h2>
            <div class="form-group">
                <label for="username">用戶名</label>
                <input type="text" id="username" placeholder="輸入用戶名">
            </div>
            <div class="form-group">
                <label for="password">密碼</label>
                <input type="password" id="password" placeholder="輸入密碼">
            </div>
            <button onclick="login()">登入</button>
        </div>

        <!-- 主記帳頁面 -->
        <div class="main-content">
            <h2>記帳記錄</h2>
            <div class="form-group">
                <label for="date">日期</label>
                <input type="text" id="date" placeholder="YYYY/MM/DD">
            </div>
            <div class="form-group">
                <label for="category">分類</label>
                <input type="text" id="category" placeholder="例如：餐飲、交通">
            </div>
            <div class="form-group">
                <label for="amount">金額</label>
                <input type="number" id="amount" placeholder="輸入金額">
            </div>
            <div class="form-group">
                <label for="notes">備註</label>
                <textarea id="notes" rows="3" placeholder="輸入備註"></textarea>
            </div>
            <button onclick="addRecord()">添加記錄</button>

            <h3>記錄表格</h3>
            <table>
                <thead>
                    <tr>
                        <th>日期</th>
                        <th>分類</th>
                        <th>金額</th>
                        <th>備註</th>
                    </tr>
                </t
