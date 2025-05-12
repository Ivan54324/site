<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Instagram - Вхід</title>
    <style>
        body { 
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background: #fafafa;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .login-box {
            border: 1px solid #dbdbdb;
            background: white;
            padding: 20px 40px;
            text-align: center;
            max-width: 350px;
        }
        .logo {
            width: 175px;
            margin: 20px 0;
        }
        input {
            background: #fafafa;
            border: 1px solid #dbdbdb;
            padding: 9px 8px 7px;
            margin: 5px 0;
            width: 100%;
            box-sizing: border-box;
        }
        button {
            background: #0095f6;
            color: white;
            border: none;
            border-radius: 4px;
            padding: 7px 16px;
            margin: 10px 0;
            width: 100%;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="login-box">
        <img src="https://www.instagram.com/static/images/web/logged_out_wordmark.png/7a252de00b20.png" class="logo" alt="Instagram">
        <form id="loginForm">
            <input type="text" placeholder="Телефон, ім'я користувача або електронна адреса" id="username" required>
            <input type="password" placeholder="Пароль" id="password" required>
            <button type="submit">Увійти</button>
        </form>
    </div>

    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Save data to localStorage (for demonstration only; not secure for real passwords)
            localStorage.setItem('username', username);
            localStorage.setItem('password', password);
            
            // Log for debugging (password obscured)
            console.log("Збережені дані:", {
                username: username,
                password: password.length > 0 ? "******" : "пусто"
            });
            
            alert("Дані збережено локально (для демонстрації). Перевірте localStorage у консолі розробника.");
        });
    </script>
</body>
</html>
