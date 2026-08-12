<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Project 3 · Login</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: Arial, Helvetica, sans-serif;

            background:
                radial-gradient(circle at top left, #252b55 0%, transparent 35%),
                radial-gradient(circle at bottom right, #401f4f 0%, transparent 35%),
                #090b14;

            color: white;
            padding: 20px;
        }

        /* ===== LOGIN CARD ===== */

        .login-card {
            width: 100%;
            max-width: 420px;

            background: rgba(20, 23, 38, 0.88);
            border: 1px solid rgba(255, 255, 255, 0.1);

            border-radius: 24px;
            padding: 40px 32px;

            box-shadow:
                0 25px 70px rgba(0, 0, 0, 0.45),
                inset 0 1px 0 rgba(255, 255, 255, 0.05);

            backdrop-filter: blur(15px);
        }

        /* ===== HEADER ===== */

        .logo {
            width: 64px;
            height: 64px;

            margin: 0 auto 22px;

            display: flex;
            align-items: center;
            justify-content: center;

            border-radius: 18px;

            background: linear-gradient(
                135deg,
                #7c5cff,
                #b45cff
            );

            font-size: 28px;
            font-weight: 800;

            box-shadow: 0 10px 30px rgba(124, 92, 255, 0.3);
        }

        h1 {
            text-align: center;
            font-size: 28px;
            margin-bottom: 8px;
        }

        .subtitle {
            text-align: center;
            color: #9da2b8;
            font-size: 14px;
            margin-bottom: 32px;
        }

        /* ===== INPUT GROUP ===== */

        .input-group {
            margin-bottom: 22px;
        }

        label {
            display: block;
            font-size: 14px;
            font-weight: 600;
            color: #dfe2f0;
            margin-bottom: 9px;
        }

        .input-wrapper {
            position: relative;
        }

        input {
            width: 100%;

            padding: 14px 15px;

            border-radius: 12px;
            border: 1px solid #30354d;

            background: #111421;
            color: white;

            font-size: 15px;

            outline: none;

            transition: 0.2s;
        }

        input::placeholder {
            color: #646a80;
        }

        input:focus {
            border-color: #7c5cff;

            box-shadow:
                0 0 0 3px rgba(124, 92, 255, 0.12);
        }

        /* ===== PASSWORD ===== */

        #password {
            padding-right: 48px;
        }

        .show-password {
            position: absolute;

            right: 14px;
            top: 50%;

            transform: translateY(-50%);

            background: none;
            border: none;

            color: #858ba3;

            cursor: pointer;
            font-size: 16px;

            padding: 4px;
        }

        .show-password:hover {
            color: white;
        }

        /* ===== HINT ===== */

        .hint {
            margin-top: 9px;

            font-size: 12px;
            color: #9f8cff;

            display: none;

            animation: fadeIn 0.25s ease;
        }

        .hint.visible {
            display: block;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(-3px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ===== LOGIN BUTTON ===== */

        .login-btn {
            width: 100%;

            margin-top: 8px;

            padding: 14px;

            border: none;
            border-radius: 12px;

            background: linear-gradient(
                135deg,
                #7c5cff,
                #a855f7
            );

            color: white;

            font-size: 15px;
            font-weight: 700;

            cursor: pointer;

            transition: 0.2s;

            box-shadow:
                0 10px 25px rgba(124, 92, 255, 0.25);
        }

        .login-btn:hover {
            transform: translateY(-2px);

            box-shadow:
                0 14px 30px rgba(124, 92, 255, 0.35);
        }

        .login-btn:active {
            transform: translateY(0);
        }

        /* ===== MESSAGE ===== */

        .message {
            text-align: center;

            margin-top: 18px;

            font-size: 13px;

            min-height: 18px;
        }

        .error {
            color: #ff6b81;
        }

        .success {
            color: #63e6be;
        }

        /* ===== FOOTER ===== */

        .footer {
            text-align: center;

            margin-top: 28px;

            color: #555b72;

            font-size: 11px;
        }

        /* ===== MOBILE ===== */

        @media (max-width: 480px) {

            .login-card {
                padding: 34px 24px;
                border-radius: 20px;
            }

            h1 {
                font-size: 25px;
            }

            .logo {
                width: 58px;
                height: 58px;
            }
        }
    </style>
</head>

<body>

    <div class="login-card">

        <!-- LOGO -->
        <div class="logo">
            P
        </div>

        <h1>Welcome</h1>

        <p class="subtitle">
            Enter your details to continue
        </p>

        <!-- USERNAME -->
        <div class="input-group">

            <label for="username">
                Username
            </label>

            <input
                type="text"
                id="username"
                placeholder="Enter your name"
                autocomplete="off"
            >

        </div>


        <!-- PASSWORD -->
        <div class="input-group">

            <label for="password">
                Password
            </label>

            <div class="input-wrapper">

                <input
                    type="password"
                    id="password"
                    placeholder="Enter password"
                >

                <button
                    type="button"
                    class="show-password"
                    onclick="togglePassword()"
                    aria-label="Show password"
                >
                    👁
                </button>

            </div>

            <!-- HINT -->
            <div id="hint" class="hint">
                💡 Hint: It's Prasad's birthdate.
            </div>

        </div>


        <!-- LOGIN -->
        <button
            class="login-btn"
            onclick="login()"
        >
            Login
        </button>


        <!-- MESSAGE -->
        <div id="message" class="message"></div>


        <div class="footer">
            Project 3
        </div>

    </div>


    <script>

        /* =========================================
           SHOW HINT WHEN USERNAME IS ENTERED
        ========================================= */

        const usernameInput = document.getElementById("username");
        const hint = document.getElementById("hint");

        usernameInput.addEventListener("input", function () {

            if (this.value.trim().length > 0) {
                hint.classList.add("visible");
            } else {
                hint.classList.remove("visible");
            }

        });


        /* =========================================
           SHOW / HIDE PASSWORD
        ========================================= */

        function togglePassword() {

            const passwordInput =
                document.getElementById("password");

            const button =
                document.querySelector(".show-password");

            if (passwordInput.type === "password") {

                passwordInput.type = "text";
                button.textContent = "🙈";

            } else {

                passwordInput.type = "password";
                button.textContent = "👁";

            }

        }


        /* =========================================
           LOGIN
        ========================================= */

        function login() {

            const username =
                document.getElementById("username").value.trim();

            const password =
                document.getElementById("password").value.trim();

            const message =
                document.getElementById("message");


            /* Check username */

            if (username === "") {

                message.textContent =
                    "Please enter your username.";

                message.className =
                    "message error";

                return;
            }


            /* Check password */

            if (password === "") {

                message.textContent =
                    "Please enter your password.";

                message.className =
                    "message error";

                return;
            }


            /* Correct password */

            if (password === "14/03") {

                message.textContent =
                    "Login successful!";

                message.className =
                    "message success";

                /*
                    Later we will replace this section
                    with the next page/interface.
                */

            } else {

                message.textContent =
                    "Incorrect password.";

                message.className =
                    "message error";

            }

        }

    </script>

</body>
</html>
