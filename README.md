<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>A Little Something ♡</title>

<style>

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    -webkit-tap-highlight-color: transparent;
}

html,
body {
    width: 100%;
    min-height: 100%;
}

body {
    min-height: 100vh;
    min-height: 100dvh;

    display: flex;
    align-items: center;
    justify-content: center;

    padding: 16px;

    font-family: "Segoe UI", Arial, sans-serif;

    color: #4b3543;

    background:
        radial-gradient(circle at 5% 5%, #ffdbe9 0%, transparent 32%),
        radial-gradient(circle at 95% 10%, #e6dcff 0%, transparent 32%),
        radial-gradient(circle at 50% 100%, #ffeadc 0%, transparent 38%),
        #fff9fc;

    overflow-x: hidden;
}


/* =====================================================
   BACKGROUND HEARTS
===================================================== */

.background-heart {
    position: fixed;

    color: rgba(226, 117, 157, 0.11);

    pointer-events: none;

    user-select: none;

    z-index: 0;

    animation: floatHeart 7s ease-in-out infinite;
}

.heart1 {
    top: 8%;
    left: 5%;
    font-size: 30px;
}

.heart2 {
    bottom: 12%;
    left: 4%;
    font-size: 22px;
    animation-delay: 2s;
}

.heart3 {
    top: 12%;
    right: 5%;
    font-size: 25px;
    animation-delay: 1s;
}

.heart4 {
    bottom: 8%;
    right: 5%;
    font-size: 32px;
    animation-delay: 3s;
}

@keyframes floatHeart {

    0%, 100% {
        transform: translateY(0) rotate(0deg);
    }

    50% {
        transform: translateY(-10px) rotate(6deg);
    }
}


/* =====================================================
   MAIN CARD
===================================================== */

.card {

    width: min(100%, 430px);

    max-height: calc(100dvh - 32px);

    overflow-y: auto;
    overflow-x: hidden;

    padding: 34px 28px;

    background: rgba(255, 255, 255, 0.82);

    border: 1px solid rgba(255, 255, 255, 0.9);

    border-radius: 28px;

    box-shadow:
        0 20px 55px rgba(170, 110, 140, 0.16),
        0 5px 20px rgba(170, 110, 140, 0.07);

    backdrop-filter: blur(18px);
    -webkit-backdrop-filter: blur(18px);

    position: relative;

    z-index: 2;

    scrollbar-width: none;

    animation: appear 0.55s ease;
}

.card::-webkit-scrollbar {
    display: none;
}

@keyframes appear {

    from {
        opacity: 0;
        transform: translateY(15px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}


/* =====================================================
   LOGIN
===================================================== */

.logo {

    width: 62px;
    height: 62px;

    margin: 0 auto 17px;

    display: flex;
    align-items: center;
    justify-content: center;

    border-radius: 50%;

    background:
        linear-gradient(
            135deg,
            #f5aac5,
            #c8b5f4
        );

    color: white;

    font-size: 25px;

    box-shadow:
        0 9px 22px rgba(210, 130, 165, 0.22);
}

h1 {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 28px;

    font-weight: 500;

    color: #543b49;

    margin-bottom: 7px;
}

.subtitle {

    text-align: center;

    color: #9b7d8c;

    font-size: 13px;

    line-height: 1.5;

    margin-bottom: 25px;
}


/* =====================================================
   INPUTS
===================================================== */

.input-group {
    margin-bottom: 17px;
}

label {

    display: block;

    margin-bottom: 7px;

    font-size: 12px;

    font-weight: 600;

    color: #6c4c5c;
}

input {

    width: 100%;

    min-height: 48px;

    padding: 12px 14px;

    border-radius: 13px;

    border: 1px solid #efd9e3;

    background: rgba(255, 255, 255, 0.8);

    color: #4b3543;

    font-size: 15px;

    outline: none;
}

input::placeholder {
    color: #c0a8b4;
}

input:focus {

    border-color: #e3a1bc;

    background: white;

    box-shadow:
        0 0 0 3px rgba(231, 157, 188, 0.12);
}


/* =====================================================
   PASSWORD
===================================================== */

.password-wrapper {
    position: relative;
}

.password-wrapper input {
    padding-right: 48px;
}

.show-password {

    position: absolute;

    right: 5px;
    top: 50%;

    transform: translateY(-50%);

    width: 40px;
    height: 40px;

    display: flex;
    justify-content: center;
    align-items: center;

    border: none;

    background: transparent;

    color: #b38d9e;

    font-size: 16px;

    cursor: pointer;
}

.hint {

    display: none;

    margin-top: 7px;

    font-size: 11px;

    color: #b06d8e;
}

.hint.show {
    display: block;
}


/* =====================================================
   BUTTONS
===================================================== */

button {
    font-family: inherit;
    touch-action: manipulation;
}

.login-btn,
.proceed-btn {

    width: 100%;

    min-height: 48px;

    padding: 12px 16px;

    border: none;

    border-radius: 13px;

    background:
        linear-gradient(
            135deg,
            #e995b6,
            #b9a0e8
        );

    color: white;

    font-size: 14px;

    font-weight: 600;

    cursor: pointer;

    box-shadow:
        0 8px 20px rgba(204, 132, 166, 0.22);
}

.login-btn {
    margin-top: 5px;
}

.login-btn:active,
.proceed-btn:active {
    transform: scale(0.98);
}


/* =====================================================
   MESSAGE
===================================================== */

.message {

    min-height: 18px;

    margin-top: 12px;

    text-align: center;

    font-size: 12px;
}

.error {
    color: #d66b83;
}

.success {
    color: #69a98c;
}


/* =====================================================
   DATE PAGE
===================================================== */

.date-page,
.reason-page,
.warning-page,
.details-page {
    display: none;
}

.date-page.active,
.reason-page.active,
.warning-page.active,
.details-page.active {
    display: block;
}

.date-icon {

    text-align: center;

    font-size: 48px;

    margin-bottom: 10px;

    animation: heartbeat 1.5s infinite;
}

@keyframes heartbeat {

    0%, 100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.08);
    }
}

.date-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 28px;

    font-weight: 500;

    color: #543b49;

    margin-bottom: 10px;
}

.date-question {

    text-align: center;

    font-size: 16px;

    line-height: 1.5;

    color: #704f60;

    margin-bottom: 23px;
}


/* =====================================================
   YES / NO
===================================================== */

.date-buttons {

    width: 100%;

    height: 60px;

    position: relative;

    display: flex;

    align-items: center;

    justify-content: center;

    gap: 12px;

    overflow: hidden;
}

.yes-btn,
.no-btn {

    min-height: 46px;

    padding: 11px 22px;

    border-radius: 50px;

    font-size: 14px;

    white-space: nowrap;
}

.yes-btn {

    border: none;

    background:
        linear-gradient(
            135deg,
            #e995b6,
            #d77fa5
        );

    color: white;

    box-shadow:
        0 7px 18px rgba(210, 120, 160, 0.22);
}

.no-btn {

    position: absolute;

    left: calc(50% + 6px);

    background: white;

    border: 1px solid #e5ccd7;

    color: #8b6878;

    transition:
        left 0.18s ease,
        top 0.18s ease;
}


/* =====================================================
   REASON
===================================================== */

.reason-icon {

    text-align: center;

    font-size: 43px;

    margin-bottom: 10px;
}

.reason-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 26px;

    color: #543b49;

    margin-bottom: 8px;
}

.reason-text {

    text-align: center;

    color: #9b7d8c;

    font-size: 13px;

    line-height: 1.5;

    margin-bottom: 18px;
}

.reason-box {

    width: 100%;

    min-height: 115px;

    padding: 13px;

    resize: vertical;

    border-radius: 13px;

    border: 1px solid #efd9e3;

    background: rgba(255,255,255,0.85);

    color: #4b3543;

    font-family: inherit;

    font-size: 15px;

    outline: none;
}

.reason-box:focus {

    border-color: #e3a1bc;

    box-shadow:
        0 0 0 3px rgba(231,157,188,0.12);
}

.proceed-btn {
    margin-top: 12px;
}


/* =====================================================
   WARNING
===================================================== */

.warning-icon {

    text-align: center;

    font-size: 48px;

    margin-bottom: 10px;
}

.warning-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 28px;

    color: #543b49;

    margin-bottom: 13px;
}

.warning-message {

    text-align: center;

    font-size: 15px;

    line-height: 1.6;

    color: #704f60;
}


/* =====================================================
   DATE DETAILS
===================================================== */

.details-icon {

    text-align: center;

    font-size: 48px;

    margin-bottom: 8px;
}

.details-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 28px;

    color: #543b49;

    margin-bottom: 17px;
}

.details-card {

    background: rgba(255,255,255,0.78);

    border: 1px solid #f0dce5;

    border-radius: 16px;

    padding: 5px 15px;
}

.detail-row {

    display: flex;

    align-items: center;

    gap: 11px;

    padding: 12px 0;

    border-bottom: 1px solid #f3e5eb;
}

.detail-row:last-child {
    border-bottom: none;
}

.detail-emoji {

    width: 26px;

    flex-shrink: 0;

    text-align: center;

    font-size: 19px;
}

.detail-content {
    min-width: 0;
    flex: 1;
}

.detail-label {

    font-size: 9px;

    text-transform: uppercase;

    letter-spacing: 0.9px;

    color: #b08b9d;

    margin-bottom: 2px;
}

.detail-value {

    font-size: 13px;

    line-height: 1.35;

    font-weight: 600;

    color: #5e4351;

    word-break: break-word;
}


/* =====================================================
   FOOTER
===================================================== */

.footer {

    margin-top: 20px;

    text-align: center;

    color: #c19eae;

    font-size: 9px;

    letter-spacing: 0.4px;
}


/* =====================================================
   PHONE OPTIMIZATION
===================================================== */

@media (max-width: 480px) {

    body {
        padding: 12px;
    }

    .card {

        width: 100%;

        padding: 30px 22px;

        border-radius: 24px;

        max-height: calc(100dvh - 24px);
    }

    .background-heart {
        opacity: 0.65;
    }
}


/* =====================================================
   VERY SMALL PHONES
===================================================== */

@media (max-width: 360px) {

    body {
        padding: 9px;
    }

    .card {

        padding: 26px 18px;

        border-radius: 22px;
    }

    .logo {

        width: 56px;
        height: 56px;

        font-size: 22px;

        margin-bottom: 14px;
    }

    h1 {
        font-size: 25px;
    }

    .subtitle {
        font-size: 12px;
        margin-bottom: 21px;
    }

    .date-title {
        font-size: 25px;
    }

    .date-question {
        font-size: 15px;
    }

    .yes-btn,
    .no-btn {

        padding-left: 18px;
        padding-right: 18px;

        font-size: 13px;
    }
}


/* =====================================================
   SHORT PHONE SCREENS
===================================================== */

@media (max-height: 650px) {

    body {
        align-items: flex-start;
        padding-top: 8px;
        padding-bottom: 8px;
    }

    .card {
        max-height: calc(100dvh - 16px);
    }

    .logo {
        width: 52px;
        height: 52px;
        margin-bottom: 11px;
    }

    .subtitle {
        margin-bottom: 18px;
    }
}


/* =====================================================
   DESKTOP
===================================================== */

@media (min-width: 481px) {

    .login-btn:hover,
    .proceed-btn:hover {

        transform: translateY(-2px);
    }

    .yes-btn:hover {

        transform: translateY(-2px) scale(1.02);
    }
}

</style>
</head>


<body>


<div class="background-heart heart1">♡</div>
<div class="background-heart heart2">♡</div>
<div class="background-heart heart3">♡</div>
<div class="background-heart heart4">♡</div>


<div class="card">


<!-- =====================================================
     LOGIN
===================================================== -->

<div id="loginPage">

    <div class="logo">
        ✦
    </div>

    <h1>Welcome</h1>

    <p class="subtitle">
        There's a little something waiting for you ✨
    </p>


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
            >
                ♡
            </button>

        </div>

        <div id="hint" class="hint">
            ✨ Hint: It's Prasad's birthdate.
        </div>

    </div>


    <button
        class="login-btn"
        onclick="login()"
    >
        Continue ✨
    </button>


    <div
        id="loginMessage"
        class="message"
    ></div>

</div>


<!-- =====================================================
     DATE QUESTION
===================================================== -->

<div id="datePage" class="date-page">

    <div class="date-icon">
        💌
    </div>

    <div class="date-title">
        A Little Question...
    </div>

    <div class="date-question">
        Would you like to go on a date with me? ♡
    </div>


    <div class="date-buttons">

        <button
            class="yes-btn"
            onclick="sayYes()"
        >
            Yes 💕
        </button>

        <button
            id="noButton"
            class="no-btn"
            onclick="sayNo()"
        >
            No 🙃
        </button>

    </div>

</div>


<!-- =====================================================
     REASON
===================================================== -->

<div id="reasonPage" class="reason-page">

    <div class="reason-icon">
        🥺
    </div>

    <div class="reason-title">
        Okay... tell me why?
    </div>

    <div class="reason-text">
        If you're saying no, at least give me a reason.
        <br>
        I promise I'll read it properly. ♡
    </div>


    <textarea
        id="reasonBox"
        class="reason-box"
        placeholder="Write your reason here..."
    ></textarea>


    <button
        class="proceed-btn"
        onclick="submitReason()"
    >
        Proceed
    </button>

</div>


<!-- =====================================================
     WARNING
===================================================== -->

<div id="warningPage" class="warning-page">

    <div class="warning-icon">
        ⚠️
    </div>

    <div class="warning-title">
        Wait a minute...
    </div>

    <div class="warning-message">

        Your response has been received.

        <br><br>

        But unfortunately...

        <br>

        <strong>
            "No" is currently under maintenance. 😂
        </strong>

        <br><br>

        Please proceed with the date. ♡

    </div>

</div>


<!-- =====================================================
     DATE DETAILS
===================================================== -->

<div id="detailsPage" class="details-page">

    <div class="details-icon">
        🌹
    </div>

    <div class="details-title">
        It's a Date ♡
    </div>


    <div class="details-card">


        <div class="detail-row">

            <div class="detail-emoji">
                📍
            </div>

            <div class="detail-content">

                <div class="detail-label">
                    Venue
                </div>

                <div class="detail-value">
                    Your Venue Here
                </div>

            </div>

        </div>


        <div class="detail-row">

            <div class="detail-emoji">
                📅
            </div>

            <div class="detail-content">

                <div class="detail-label">
                    Date
                </div>

                <div class="detail-value">
                    Your Date Here
                </div>

            </div>

        </div>


        <div class="detail-row">

            <div class="detail-emoji">
                🕐
            </div>

            <div class="detail-content">

                <div class="detail-label">
                    Time
                </div>

                <div class="detail-value">
                    Your Time Here
                </div>

            </div>

        </div>


        <div class="detail-row">

            <div class="detail-emoji">
                👗
            </div>

            <div class="detail-content">

                <div class="detail-label">
                    Dress Code
                </div>

                <div class="detail-value">
                    Something You Feel Pretty In ♡
                </div>

            </div>

        </div>


        <div class="detail-row">

            <div class="detail-emoji">
                🫶
            </div>

            <div class="detail-content">

                <div class="detail-label">
                    Company
                </div>

                <div class="detail-value">
                    Me, obviously.
                </div>

            </div>

        </div>


    </div>

</div>


<div class="footer">
    made with a little extra thought ♡
</div>


</div>


<script>

/* =====================================================
   PASSWORD
===================================================== */

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


/* =====================================================
   HINT
===================================================== */

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


/* =====================================================
   LOGIN
===================================================== */

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
        document.getElementById("loginMessage");


    if (username === "") {

        message.textContent =
            "Please enter your name.";

        message.className =
            "message error";

        return;
    }


    if (password === "") {

        message.textContent =
            "Please enter your password.";

        message.className =
            "message error";

        return;
    }


    if (password.toLowerCase() === "14 march") {

        document.getElementById("loginPage")
            .style.display = "none";

        document.getElementById("datePage")
            .classList.add("active");

    } else {

        message.textContent =
            "That's not quite right ♡";

        message.className =
            "message error";

    }

}


/* =====================================================
   NO BUTTON
===================================================== */

let noAttempts = 0;

const noButton =
    document.getElementById("noButton");


function sayNo() {

    if (noAttempts >= 4) {

        document.getElementById("datePage")
            .classList.remove("active");

        document.getElementById("reasonPage")
            .classList.add("active");

        return;
    }


    noAttempts++;

    moveNoButton();

}


/* =====================================================
   MOVE NO BUTTON
===================================================== */

function moveNoButton() {

    const area =
        document.querySelector(".date-buttons");

    const areaWidth =
        area.clientWidth;

    const areaHeight =
        area.clientHeight;

    const buttonWidth =
        noButton.offsetWidth;

    const buttonHeight =
        noButton.offsetHeight;


    const maxX =
        Math.max(0, areaWidth - buttonWidth);

    const maxY =
        Math.max(0, areaHeight - buttonHeight);


    const randomX =
        Math.random() * maxX;

    const randomY =
        Math.random() * maxY;


    noButton.style.left =
        randomX + "px";

    noButton.style.top =
        randomY + "px";

}


/* =====================================================
   YES
===================================================== */

function sayYes() {

    document.getElementById("datePage")
        .classList.remove("active");

    document.getElementById("detailsPage")
        .classList.add("active");

}


/* =====================================================
   REASON
===================================================== */

function submitReason() {

    const reason =
        document.getElementById("reasonBox")
        .value
        .trim();


    if (reason === "") {

        alert(
            "You have to give me a reason first 😭"
        );

        return;
    }


    document.getElementById("reasonPage")
        .classList.remove("active");

    document.getElementById("warningPage")
        .classList.add("active");


    setTimeout(function() {

        document.getElementById("warningPage")
            .classList.remove("active");

        document.getElementById("detailsPage")
            .classList.add("active");

    }, 3500);

}

</script>

</body>
</html>
