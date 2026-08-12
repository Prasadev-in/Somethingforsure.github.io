<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Project 3 - Login</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;

    font-family: Arial, sans-serif;

    background:
        radial-gradient(circle at top left, #292f5c, transparent 35%),
        radial-gradient(circle at bottom right, #492052, transparent 35%),
        #090b14;

    color: white;
}

.login-card {
    width: 100%;
    max-width: 420px;

    padding: 40px 32px;

    background: rgba(20, 23, 38, 0.95);

    border: 1px solid rgba(255,255,255,0.1);

    border-radius: 24px;

    box-shadow: 0 25px 70px rgba(0,0,0,0.5);
}

.logo {
    width: 64px;
    height: 64px;

    margin: 0 auto 20px;

    display: flex;
    justify-content: center;
    align-items: center;

    border-radius: 18px;

    background: linear-gradient(135deg, #7c5cff, #b45cff);

    font-size: 28px;
    font-weight: bold;
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
    margin-bottom: 30px;
}

.input-group {
    margin-bottom: 22px;
}

label {
    display: block;
    margin-bottom: 9px;

    font-size: 14px;
    font-weight: bold;

    color: #dfe2f0;
}

input {
    width: 100%;

    padding: 14px;

    border-radius: 12px;

    border: 1px solid #30354d;

    background: #111421;

    color: white;

    font-size: 15px;

    outline: none;
}

input::placeholder {
    color: #646a80;
}

input:focus {
    border-color: #7c5cff;

    box-shadow: 0 0 0 3px rgba(124,92,255,0.12);
}

/* Password wrapper */

.password-wrapper {
    position: relative;
}

.password-wrapper input {
    padding-right: 50px;
}

/* Show password button */

.show-password {
    position: absolute;

    right: 12px;
    top: 50%;

    transform: translateY(-50%);

    background: none;
    border: none;

    color: #858ba3;

    cursor: pointer;

    font-size: 16px;
}

/* Hint */

.hint {
    display: none;

    margin-top: 9px;

    font-size: 12px;

    color: #a998ff;
}

.hint.show {
    display: block;
}

/* Login button */

.login-btn {
    width: 100%;

    padding: 14px;

    margin-top: 5px;

    border: none;
    border-radius: 12px;

    background: linear-gradient(135deg, #7c5cff, #a855f7);

    color: white;

    font-size: 15px;
    font-weight: bold;

    cursor: pointer;

    transition: 0.2s;
}

.login-btn:hover {
    transform: translateY(-2px);
}

.login-btn:active {
    transform: translateY(0);
}

/* Message */

.message {
    min-height: 20px;

    margin-top: 16px;

    text-align: center;

    font-size: 13px;
}

.error {
    color: #ff6b81;
}

.success {
    color: #63e6be;
}

.footer {
    margin-top: 28px;

    text-align: center;

    color: #555b72;

    font-size: 11px;
}

@media (max-width: 480px) {

    .login-card {
        padding: 32px 24px;
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

        <div class="password-wrapper">

            <input
                type="password"
                id="password"
                placeholder="DD/MM"
            >

            <button
                type="button"
                class="show-password"
                onclick="togglePassword()"
            >
                👁
            </button>

        </div>


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


    <div id="message" class="message"></div>


    <div class="footer">
        Project 3
    </div>

</div>


<script>

/* Show the hint when username is entered */

const username = document.getElementById("username");
const hint = document.getElementById("hint");

username.addEventListener("input", function() {

    if (username.value.trim() !== "") {
        hint.classList.add("show");
    } else {
        hint.classList.remove("show");
    }

});


/* Show / hide password */

function togglePassword() {

    const password = document.getElementById("password");
    const button = document.querySelector(".show-password");

    if (password.type === "password") {

        password.type = "text";
        button.textContent = "🙈";

    } else {

        password.type = "password";
        button.textContent = "👁";

    }

}


/* Login */

function login() {

    const usernameValue =
        document.getElementById("username").value.trim();

    const passwordValue =
        document.getElementById("password").value.trim();

    const message =
        document.getElementById("message");


    if (usernameValue === "") {

        message.textContent =
            "Please enter your username.";

        message.className =
            "message error";

        return;

    }


    if (passwordValue === "") {

        message.textContent =
            "Please enter your password.";

        message.className =
            "message error";

        return;

    }


    if (passwordValue === "14/03") {

        message.textContent =
            "Login successful!";

        message.className =
            "message success";

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
