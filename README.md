<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>A Little Something ✨</title>

<style>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;

    display: flex;
    justify-content: center;
    align-items: center;

    padding: 20px;

    font-family: "Segoe UI", Arial, sans-serif;

    color: #4b3543;

    background:
        radial-gradient(circle at 15% 15%, #ffd6e7 0%, transparent 35%),
        radial-gradient(circle at 85% 20%, #e4d8ff 0%, transparent 35%),
        radial-gradient(circle at 50% 100%, #ffe9d6 0%, transparent 40%),
        #fff8fb;

    overflow: hidden;
}


/* =========================================
   FLOATING BACKGROUND HEARTS
========================================= */

.background-heart {
    position: fixed;

    color: rgba(226, 117, 157, 0.15);

    font-size: 35px;

    pointer-events: none;

    animation: floatHeart 7s ease-in-out infinite;
}

.heart1 {
    top: 12%;
    left: 10%;
}

.heart2 {
    top: 70%;
    left: 8%;

    font-size: 25px;

    animation-delay: 2s;
}

.heart3 {
    top: 18%;
    right: 10%;

    font-size: 28px;

    animation-delay: 1s;
}

.heart4 {
    bottom: 10%;
    right: 12%;

    font-size: 40px;

    animation-delay: 3s;
}

@keyframes floatHeart {

    0%, 100% {
        transform: translateY(0) rotate(0deg);
    }

    50% {
        transform: translateY(-15px) rotate(8deg);
    }

}


/* =========================================
   MAIN CARD
========================================= */

.login-card {

    width: 100%;
    max-width: 410px;

    padding: 42px 34px;

    background: rgba(255, 255, 255, 0.72);

    border: 1px solid rgba(255, 255, 255, 0.8);

    border-radius: 30px;

    box-shadow:
        0 25px 70px rgba(170, 110, 140, 0.18),
        0 8px 25px rgba(170, 110, 140, 0.08);

    backdrop-filter: blur(20px);

    position: relative;

    z-index: 2;

    animation: cardAppear 0.7s ease;
}

@keyframes cardAppear {

    from {
        opacity: 0;
        transform: translateY(20px) scale(0.97);
    }

    to {
        opacity: 1;
        transform: translateY(0) scale(1);
    }

}


/* =========================================
   TOP ICON
========================================= */

.logo {

    width: 72px;
    height: 72px;

    margin: 0 auto 20px;

    display: flex;
    justify-content: center;
    align-items: center;

    border-radius: 50%;

    background:
        linear-gradient(
            135deg,
            #f7a8c4,
            #c9b4f7
        );

    color: white;

    font-size: 29px;

    box-shadow:
        0 12px 28px rgba(210, 130, 165, 0.28);

    position: relative;
}

.logo::after {

    content: "♡";

    position: absolute;

    font-size: 13px;

    right: -2px;
    top: 1px;

    color: #e78eae;
}


/* =========================================
   TITLE
========================================= */

h1 {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 31px;

    font-weight: 500;

    color: #543b49;

    margin-bottom: 8px;
}

.subtitle {

    text-align: center;

    color: #9b7d8c;

    font-size: 14px;

    margin-bottom: 32px;

    letter-spacing: 0.2px;
}


/* =========================================
   INPUTS
========================================= */

.input-group {

    margin-bottom: 21px;
}

label {

    display: block;

    margin-bottom: 8px;

    font-size: 13px;

    font-weight: 600;

    color: #6c4c5c;

    letter-spacing: 0.2px;
}

input {

    width: 100%;

    padding: 15px 16px;

    border-radius: 14px;

    border: 1px solid #efd9e3;

    background: rgba(255, 255, 255, 0.75);

    color: #4b3543;

    font-size: 15px;

    outline: none;

    transition: all 0.25s ease;
}

input::placeholder {

    color: #c0a8b4;
}

input:focus {

    border-color: #e3a1bc;

    background: white;

    box-shadow:
        0 0 0 4px rgba(231, 157, 188, 0.13);
}


/* =========================================
   PASSWORD
========================================= */

.password-wrapper {

    position: relative;
}

.password-wrapper input {

    padding-right: 50px;
}

.show-password {

    position: absolute;

    right: 13px;
    top: 50%;

    transform: translateY(-50%);

    background: none;

    border: none;

    color: #b38d9e;

    cursor: pointer;

    font-size: 17px;

    padding: 5px;
}

.show-password:hover {

    color: #d27d9f;
}


/* =========================================
   HINT
========================================= */

.hint {

    display: none;

    margin-top: 9px;

    font-size: 12px;

    color: #b06d8e;

    animation: hintAppear 0.3s ease;
}

.hint.show {

    display: block;
}

@keyframes hintAppear {

    from {
        opacity: 0;
        transform: translateY(-4px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }

}


/* =========================================
   BUTTON
========================================= */

.login-btn {

    width: 100%;

    padding: 15px;

    margin-top: 7px;

    border: none;

    border-radius: 15px;

    background:
        linear-gradient(
            135deg,
            #e995b6,
            #b9a0e8
        );

    color: white;

    font-size: 15px;

    font-weight: 600;

    letter-spacing: 0.3px;

    cursor: pointer;

    box-shadow:
        0 10px 25px rgba(204, 132, 166, 0.25);

    transition: all 0.25s ease;
}

.login-btn:hover {

    transform: translateY(-2px);

    box-shadow:
        0 14px 30px rgba(204, 132, 166, 0.32);
}

.login-btn:active {

    transform: translateY(0);
}


/* =========================================
   MESSAGE
========================================= */

.message {

    min-height: 20px;

    margin-top: 16px;

    text-align: center;

    font-size: 13px;
}

.error {

    color: #d66b83;
}

.success {

    color: #69a98c;
}


/* =========================================
   FOOTER
========================================= */

.footer {

    margin-top: 27px;

    text-align: center;

    color: #c19eae;

    font-size: 11px;

    letter-spacing: 0.5px;
}


/* =========================================
   MOBILE
========================================= */

@media (max-width: 480px) {

    .login-card {

        padding: 36px 24px;

        border-radius: 26px;
    }

    h1 {

        font-size: 28px;
    }

    .logo {

        width: 66px;
        height: 66px;
    }

}

</style>
</head>


<body>


<!-- Floating decorative hearts -->

<div class="background-heart heart1">♡</div>
<div class="background-heart heart2">♡</div>
<div class="background-heart heart3">♡</div>
<div class="background-heart heart4">♡</div>


<!-- =========================================
     LOGIN CARD
========================================= -->

<div class="login-card">


    <!-- Logo -->

    <div class="logo">
        ✦
    </div>


    <!-- Title -->

    <h1>Welcome</h1>

    <p class="subtitle">
        There's a little something waiting for you ✨
    </p>


    <!-- =====================================
         USERNAME
    ====================================== -->

    <div class="input-group">

        <label for="username">
            Your name
        </label>

        <input
            type="text"
            id="username"
            placeholder="Enter your name"
            autocomplete="off"
        >

    </div>


    <!-- =====================================
         PASSWORD
    ====================================== -->

    <div class="input-group">

        <label for="password">
            Password
        </label>

        <div class="password-wrapper">

            <input
                type="password"
                id="password"
                placeholder="Enter your password"
            >

            <button
                type="button"
                class="show-password"
                onclick="togglePassword()"
                aria-label="Show password"
            >
                ♡
            </button>

        </div>


        <!-- Hint appears after username -->

        <div id="hint" class="hint">

            ✨ Hint: It's Prasad's birthdate.

        </div>

    </div>


    <!-- =====================================
         LOGIN BUTTON
    ====================================== -->

    <button
        class="login-btn"
        onclick="login()"
    >

        Continue ✨

    </button>


    <!-- Message -->

    <div
        id="message"
        class="message"
    ></div>


    <!-- Footer -->

    <div class="footer">

        made with a little extra thought ♡

    </div>


</div>


<script>


/* =========================================
   SHOW HINT
========================================= */

const usernameInput =
    document.getElementById("username");

const hint =
    document.getElementById("hint");


usernameInput.addEventListener("input", function() {

    if (usernameInput.value.trim() !== "") {

        hint.classList.add("show");

    } else {

        hint.classList.remove("show");

    }

});


/* =========================================
   SHOW / HIDE PASSWORD
========================================= */

function togglePassword() {

    const password =
        document.getElementById("password");

    const button =
        document.querySelector(".show-password");


    if (password.type === "password") {

        password.type = "text";

        button.textContent = "♥";

    } else {

        password.type = "password";

        button.textContent = "♡";

    }

}


/* =========================================
   LOGIN
========================================= */

function login() {

    const username =
        document.getElementById("username")
        .value
        .trim();

    const password =
        document.getElementById("password")
        .value
        .trim();

    const message =
        document.getElementById("message");


    /* Username check */

    if (username === "") {

        message.textContent =
            "Please enter your name.";

        message.className =
            "message error";

        return;
    }


    /* Password check */

    if (password === "") {

        message.textContent =
            "Please enter your password.";

        message.className =
            "message error";

        return;
    }


    /* Correct password */

    if (password.toLowerCase() === "14 march") {

        message.textContent =
            "Login successful ✨";

        message.className =
            "message success";


        /*
           THE NEXT PART OF PROJECT 3
           WILL GO HERE.
        */

    } else {

        message.textContent =
            "That's not quite right ♡";

        message.className =
            "message error";

    }

}

</script>


</body>
</html>
