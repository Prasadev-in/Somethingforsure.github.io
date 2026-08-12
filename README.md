<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>A Little Something ♡</title>

<style>

/* =====================================================
   GENERAL
===================================================== */

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


/* =====================================================
   FLOATING HEARTS
===================================================== */

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


/* =====================================================
   MAIN CARD
===================================================== */

.card {

    width: 100%;
    max-width: 460px;

    padding: 42px 34px;

    background: rgba(255, 255, 255, 0.78);

    border: 1px solid rgba(255, 255, 255, 0.85);

    border-radius: 30px;

    box-shadow:
        0 25px 70px rgba(170, 110, 140, 0.18),
        0 8px 25px rgba(170, 110, 140, 0.08);

    backdrop-filter: blur(20px);

    position: relative;

    z-index: 2;

    animation: cardAppear 0.6s ease;
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


/* =====================================================
   LOGIN PAGE
===================================================== */

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
}

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
}


/* =====================================================
   INPUTS
===================================================== */

.input-group {
    margin-bottom: 21px;
}

label {

    display: block;

    margin-bottom: 8px;

    font-size: 13px;

    font-weight: 600;

    color: #6c4c5c;
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

    transition: 0.25s;
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


/* =====================================================
   PASSWORD
===================================================== */

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
}

.hint {

    display: none;

    margin-top: 9px;

    font-size: 12px;

    color: #b06d8e;
}

.hint.show {
    display: block;
}


/* =====================================================
   BUTTON
===================================================== */

.login-btn,
.proceed-btn,
.yes-btn,
.no-btn {

    border: none;

    cursor: pointer;

    font-weight: 600;

    transition: 0.25s;
}

.login-btn {

    width: 100%;

    padding: 15px;

    margin-top: 7px;

    border-radius: 15px;

    background:
        linear-gradient(
            135deg,
            #e995b6,
            #b9a0e8
        );

    color: white;

    font-size: 15px;

    box-shadow:
        0 10px 25px rgba(204, 132, 166, 0.25);
}

.login-btn:hover {
    transform: translateY(-2px);
}


/* =====================================================
   MESSAGE
===================================================== */

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


/* =====================================================
   DATE INVITATION PAGE
===================================================== */

.date-page {
    display: none;
}

.date-page.active {
    display: block;
}

.date-icon {

    font-size: 55px;

    text-align: center;

    margin-bottom: 15px;

    animation: heartbeat 1.5s infinite;
}

@keyframes heartbeat {

    0%, 100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.12);
    }

}

.date-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 30px;

    font-weight: 500;

    color: #543b49;

    margin-bottom: 12px;
}

.date-question {

    text-align: center;

    font-size: 18px;

    color: #704f60;

    line-height: 1.5;

    margin-bottom: 30px;
}


/* =====================================================
   YES / NO BUTTONS
===================================================== */

.date-buttons {

    position: relative;

    display: flex;

    justify-content: center;

    align-items: center;

    gap: 18px;

    min-height: 70px;
}

.yes-btn {

    padding: 14px 30px;

    border-radius: 50px;

    background:
        linear-gradient(135deg, #e995b6, #d77fa5);

    color: white;

    font-size: 15px;

    box-shadow:
        0 8px 20px rgba(210, 120, 160, 0.25);
}

.yes-btn:hover {
    transform: translateY(-3px) scale(1.03);
}

.no-btn {

    padding: 14px 30px;

    border-radius: 50px;

    background: #fff;

    border: 1px solid #e5ccd7;

    color: #8b6878;

    font-size: 15px;

    position: relative;
}

.no-btn:hover {
    background: #fff5f8;
}


/* =====================================================
   NO REASON BOX
===================================================== */

.reason-page {
    display: none;
}

.reason-page.active {
    display: block;
}

.reason-icon {

    text-align: center;

    font-size: 48px;

    margin-bottom: 15px;
}

.reason-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 27px;

    color: #543b49;

    margin-bottom: 10px;
}

.reason-text {

    text-align: center;

    color: #9b7d8c;

    font-size: 14px;

    line-height: 1.5;

    margin-bottom: 22px;
}

.reason-box {

    width: 100%;

    min-height: 120px;

    resize: none;

    padding: 14px;

    border-radius: 15px;

    border: 1px solid #efd9e3;

    background: rgba(255,255,255,0.8);

    color: #4b3543;

    font-family: inherit;

    font-size: 14px;

    outline: none;
}

.reason-box:focus {

    border-color: #e3a1bc;

    box-shadow:
        0 0 0 4px rgba(231,157,188,0.13);
}

.proceed-btn {

    width: 100%;

    margin-top: 15px;

    padding: 14px;

    border-radius: 14px;

    background:
        linear-gradient(135deg, #e995b6, #b9a0e8);

    color: white;

    font-size: 15px;
}


/* =====================================================
   WARNING PAGE
===================================================== */

.warning-page {
    display: none;
}

.warning-page.active {
    display: block;
}

.warning-icon {

    text-align: center;

    font-size: 55px;

    margin-bottom: 15px;
}

.warning-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 30px;

    color: #543b49;

    margin-bottom: 15px;
}

.warning-message {

    text-align: center;

    font-size: 17px;

    line-height: 1.6;

    color: #704f60;
}


/* =====================================================
   DATE DETAILS
===================================================== */

.details-page {
    display: none;
}

.details-page.active {
    display: block;
}

.details-icon {

    text-align: center;

    font-size: 55px;

    margin-bottom: 12px;
}

.details-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 30px;

    color: #543b49;

    margin-bottom: 22px;
}

.details-card {

    background: rgba(255,255,255,0.75);

    border: 1px solid #f0dce5;

    border-radius: 18px;

    padding: 20px;
}

.detail-row {

    display: flex;

    align-items: flex-start;

    gap: 15px;

    padding: 13px 0;

    border-bottom: 1px solid #f3e5eb;
}

.detail-row:last-child {
    border-bottom: none;
}

.detail-emoji {

    font-size: 21px;

    width: 30px;
}

.detail-content {
    flex: 1;
}

.detail-label {

    font-size: 11px;

    text-transform: uppercase;

    letter-spacing: 1px;

    color: #b08b9d;

    margin-bottom: 3px;
}

.detail-value {

    font-size: 15px;

    font-weight: 600;

    color: #5e4351;
}


/* =====================================================
   FOOTER
===================================================== */

.footer {

    margin-top: 27px;

    text-align: center;

    color: #c19eae;

    font-size: 11px;

    letter-spacing: 0.5px;
}


/* =====================================================
   MOBILE
===================================================== */

@media (max-width: 480px) {

    .card {
        padding: 36px 24px;
    }

    h1,
    .date-title {
        font-size: 28px;
    }

    .date-question {
        font-size: 17px;
    }

}

</style>
</head>


<body>


<!-- =====================================================
     BACKGROUND DECORATION
===================================================== -->

<div class="background-heart heart1">♡</div>
<div class="background-heart heart2">♡</div>
<div class="background-heart heart3">♡</div>
<div class="background-heart heart4">♡</div>


<!-- =====================================================
     MAIN CARD
===================================================== -->

<div class="card">


    <!-- =================================================
         LOGIN PAGE
    ================================================== -->

    <div id="loginPage">

        <div class="logo">
            ✦
        </div>

        <h1>Welcome</h1>

        <p class="subtitle">
            There's a little something waiting for you ✨
        </p>


        <!-- USERNAME -->

        <div class="input-group">

            <label>
                Your name
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

            <label>
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


    <!-- =================================================
         DATE INVITATION
    ================================================== -->

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


    <!-- =================================================
         REASON PAGE
    ================================================== -->

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


    <!-- =================================================
         WARNING PAGE
    ================================================== -->

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

            Please proceed with the date.
            ♡
        </div>

    </div>


    <!-- =================================================
         DATE DETAILS
    ================================================== -->

    <div id="detailsPage" class="details-page">

        <div class="details-icon">
            🌹
        </div>

        <div class="details-title">
            It's a Date ♡
        </div>


        <div class="details-card">


            <!-- VENUE -->

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


            <!-- DATE -->

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


            <!-- TIME -->

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


            <!-- DRESS CODE -->

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


            <!-- COMPANION -->

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


    <!-- FOOTER -->

    <div class="footer">
        made with a little extra thought ♡
    </div>


</div>


<script>


/* =====================================================
   SHOW PASSWORD
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
   SHOW LOGIN HINT
===================================================== */

const username =
    document.getElementById("username");

const hint =
    document.getElementById("hint");


username.addEventListener("input", function() {

    if (username.value.trim() !== "") {

        hint.classList.add("show");

    } else {

        hint.classList.remove("show");

    }

});


/* =====================================================
   LOGIN
===================================================== */

function login() {

    const usernameValue =
        document.getElementById("username")
        .value
        .trim();

    const passwordValue =
        document.getElementById("password")
        .value
        .trim();

    const message =
        document.getElementById("loginMessage");


    if (usernameValue === "") {

        message.textContent =
            "Please enter your name.";

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


    if (passwordValue.toLowerCase() === "14 march") {

        /* Hide login */

        document.getElementById("loginPage")
            .style.display = "none";


        /* Show date question */

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

    /*
       After 4 attempts the button finally
       allows the user to continue.
    */

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

    const container =
        document.querySelector(".date-buttons");

    const containerWidth =
        container.offsetWidth;

    const buttonWidth =
        noButton.offsetWidth;


    const maxMove =
        Math.max(20, containerWidth - buttonWidth);


    const randomX =
        Math.random() * maxMove - maxMove / 2;


    const randomY =
        Math.random() * 100 - 50;


    noButton.style.transform =
        `translate(${randomX}px, ${randomY}px)`;

}


/* =====================================================
   YES BUTTON
===================================================== */

function sayYes() {

    document.getElementById("datePage")
        .classList.remove("active");

    document.getElementById("detailsPage")
        .classList.add("active");

}


/* =====================================================
   SUBMIT REASON
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


    /* Show warning */

    document.getElementById("reasonPage")
        .classList.remove("active");

    document.getElementById("warningPage")
        .classList.add("active");


    /*
       After 3 seconds show the date details.
    */

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
