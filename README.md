<html lang="en">
<head>>

<meta charset="UTF-8">

<meta
    name="viewport"
    content="width=device-width, initial-scale=1.0"
>

<title>A Little Something ♡</title>


<style>

/* =====================================================
   RESET
===================================================== */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
}

html {
    width: 100%;
    min-height: 100%;
}

body {

    width: 100%;

    min-height: 100vh;
    min-height: 100dvh;

    display: flex;

    justify-content: center;
    align-items: center;

    padding:
        max(18px, env(safe-area-inset-top))
        max(18px, env(safe-area-inset-right))
        max(18px, env(safe-area-inset-bottom))
        max(18px, env(safe-area-inset-left));

    font-family:
        "Segoe UI",
        Arial,
        sans-serif;

    color: #4b3543;

    background:

        radial-gradient(
            circle at 10% 10%,
            #ffd6e7 0%,
            transparent 35%
        ),

        radial-gradient(
            circle at 90% 15%,
            #e4d8ff 0%,
            transparent 35%
        ),

        radial-gradient(
            circle at 50% 100%,
            #ffe9d6 0%,
            transparent 40%
        ),

        #fff8fb;

    overflow-x: hidden;
}


/* =====================================================
   FLOATING HEARTS
===================================================== */

.background-heart {

    position: fixed;

    color: rgba(
        226,
        117,
        157,
        0.13
    );

    pointer-events: none;

    user-select: none;

    z-index: 0;

    animation:
        floatHeart
        7s
        ease-in-out
        infinite;
}

.heart1 {

    top: 8%;
    left: 6%;

    font-size: 34px;
}

.heart2 {

    bottom: 14%;
    left: 5%;

    font-size: 25px;

    animation-delay: 2s;
}

.heart3 {

    top: 13%;
    right: 6%;

    font-size: 28px;

    animation-delay: 1s;
}

.heart4 {

    bottom: 9%;
    right: 7%;

    font-size: 38px;

    animation-delay: 3s;
}


@keyframes floatHeart {

    0%,
    100% {

        transform:
            translateY(0)
            rotate(0deg);
    }

    50% {

        transform:
            translateY(-12px)
            rotate(7deg);
    }
}


/* =====================================================
   MAIN CARD
===================================================== */

.card {

    width: min(
        100%,
        460px
    );

    max-height:
        calc(100dvh - 36px);

    overflow-y: auto;
    overflow-x: hidden;

    padding:
        38px 32px;

    background:
        rgba(
            255,
            255,
            255,
            0.80
        );

    border:
        1px solid
        rgba(
            255,
            255,
            255,
            0.90
        );

    border-radius: 30px;

    box-shadow:

        0 25px 70px
        rgba(
            170,
            110,
            140,
            0.18
        ),

        0 8px 25px
        rgba(
            170,
            110,
            140,
            0.08
        );

    backdrop-filter:
        blur(20px);

    -webkit-backdrop-filter:
        blur(20px);

    position: relative;

    z-index: 2;

    animation:
        cardAppear
        0.6s
        ease;

    scrollbar-width: none;
}


.card::-webkit-scrollbar {
    display: none;
}


@keyframes cardAppear {

    from {

        opacity: 0;

        transform:
            translateY(18px)
            scale(0.98);
    }

    to {

        opacity: 1;

        transform:
            translateY(0)
            scale(1);
    }
}


/* =====================================================
   LOGIN LOGO
===================================================== */

.logo {

    width: 70px;
    height: 70px;

    margin:
        0 auto 20px;

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

    font-size: 28px;

    box-shadow:

        0 12px 28px
        rgba(
            210,
            130,
            165,
            0.28
        );
}


/* =====================================================
   LOGIN TITLE
===================================================== */

h1 {

    text-align: center;

    font-family:
        Georgia,
        "Times New Roman",
        serif;

    font-size:
        clamp(
            27px,
            7vw,
            31px
        );

    font-weight: 500;

    color: #543b49;

    margin-bottom: 8px;
}


.subtitle {

    text-align: center;

    color: #9b7d8c;

    font-size: 14px;

    line-height: 1.5;

    margin-bottom: 29px;
}


/* =====================================================
   INPUTS
===================================================== */

.input-group {

    margin-bottom: 20px;
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

    min-height: 52px;

    padding:
        14px 16px;

    border-radius: 14px;

    border:
        1px solid
        #efd9e3;

    background:
        rgba(
            255,
            255,
            255,
            0.80
        );

    color: #4b3543;

    font-size: 16px;

    outline: none;

    transition:
        0.2s;
}


input::placeholder {
    color: #c0a8b4;
}


input:focus {

    border-color:
        #e3a1bc;

    background: white;

    box-shadow:

        0 0 0 4px
        rgba(
            231,
            157,
            188,
            0.13
        );
}


/* =====================================================
   PASSWORD
===================================================== */

.password-wrapper {

    position: relative;
}


.password-wrapper input {

    padding-right: 55px;
}


.show-password {

    position: absolute;

    right: 8px;
    top: 50%;

    transform:
        translateY(-50%);

    width: 42px;
    height: 42px;

    display: flex;

    align-items: center;
    justify-content: center;

    background: transparent;

    border: none;

    color: #b38d9e;

    cursor: pointer;

    font-size: 17px;
}


/* =====================================================
   PASSWORD HINT
===================================================== */

.hint {

    display: none;

    margin-top: 9px;

    font-size: 12px;

    color: #b06d8e;

    line-height: 1.4;
}


.hint.show {
    display: block;
}


/* =====================================================
   GENERAL BUTTONS
===================================================== */

button {

    font-family: inherit;

    touch-action:
        manipulation;
}


.login-btn,
.proceed-btn {

    width: 100%;

    min-height: 52px;

    padding:
        14px 18px;

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

    letter-spacing: 0.2px;

    cursor: pointer;

    box-shadow:

        0 10px 25px
        rgba(
            204,
            132,
            166,
            0.25
        );

    transition:
        transform 0.2s ease;
}


.login-btn {
    margin-top: 5px;
}


.login-btn:active,
.proceed-btn:active {

    transform:
        scale(0.98);
}


/* =====================================================
   LOGIN MESSAGE
===================================================== */

.message {

    min-height: 20px;

    margin-top: 14px;

    text-align: center;

    font-size: 13px;

    line-height: 1.4;
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

.date-page {
    display: none;
}


.date-page.active {
    display: block;
}


.date-icon {

    text-align: center;

    font-size:
        clamp(
            45px,
            13vw,
            58px
        );

    margin-bottom: 12px;

    animation:
        heartbeat
        1.5s
        infinite;
}


@keyframes heartbeat {

    0%,
    100% {

        transform:
            scale(1);
    }

    50% {

        transform:
            scale(1.10);
    }
}


.date-title {

    text-align: center;

    font-family:
        Georgia,
        "Times New Roman",
        serif;

    font-size:
        clamp(
            27px,
            7vw,
            31px
        );

    font-weight: 500;

    color: #543b49;

    margin-bottom: 12px;
}


.date-question {

    text-align: center;

    font-size:
        clamp(
            16px,
            4.5vw,
            18px
        );

    line-height: 1.55;

    color: #704f60;

    margin-bottom: 26px;
}


/* =====================================================
   YES / NO AREA
===================================================== */

.date-buttons {

    position: relative;

    width: 100%;

    height: 65px;

    display: flex;

    justify-content: center;

    align-items: center;

    gap: 14px;

    overflow: hidden;
}


.yes-btn,
.no-btn {

    min-height: 50px;

    padding:
        13px 24px;

    border-radius: 50px;

    font-size: 15px;

    white-space: nowrap;
}


.yes-btn {

    background:

        linear-gradient(
            135deg,
            #e995b6,
            #d77fa5
        );

    color: white;

    border: none;

    box-shadow:

        0 8px 20px
        rgba(
            210,
            120,
            160,
            0.25
        );
}


.yes-btn:active {

    transform:
        scale(0.96);
}


.no-btn {

    background: white;

    border:
        1px solid
        #e5ccd7;

    color: #8b6878;

    position: absolute;

    left:
        calc(50% + 8px);

    transform:
        translateX(0);

    transition:

        left 0.18s ease,
        top 0.18s ease,
        transform 0.18s ease;
}


/* =====================================================
   REASON PAGE
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

    margin-bottom: 13px;
}


.reason-title {

    text-align: center;

    font-family:
        Georgia,
        "Times New Roman",
        serif;

    font-size:
        clamp(
            25px,
            7vw,
            29px
        );

    color: #543b49;

    margin-bottom: 10px;
}


.reason-text {

    text-align: center;

    color: #9b7d8c;

    font-size: 14px;

    line-height: 1.55;

    margin-bottom: 20px;
}


.reason-box {

    width: 100%;

    min-height: 125px;

    resize: vertical;

    padding: 14px;

    border-radius: 15px;

    border:
        1px solid
        #efd9e3;

    background:
        rgba(
            255,
            255,
            255,
            0.85
        );

    color: #4b3543;

    font-family: inherit;

    font-size: 16px;

    outline: none;
}


.reason-box:focus {

    border-color:
        #e3a1bc;

    box-shadow:

        0 0 0 4px
        rgba(
            231,
            157,
            188,
            0.13
        );
}


.proceed-btn {
    margin-top: 14px;
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

    font-size: 52px;

    margin-bottom: 13px;
}


.warning-title {

    text-align: center;

    font-family:
        Georgia,
        "Times New Roman",
        serif;

    font-size:
        clamp(
            27px,
            7vw,
            31px
        );

    color: #543b49;

    margin-bottom: 15px;
}


.warning-message {

    text-align: center;

    font-size: 16px;

    line-height: 1.65;

    color: #704f60;
}


/* =====================================================
   DETAILS PAGE
===================================================== */

.details-page {
    display: none;
}


.details-page.active {
    display: block;
}


.details-icon {

    text-align: center;

    font-size: 52px;

    margin-bottom: 10px;
}


.details-title {

    text-align: center;

    font-family:
        Georgia,
        "Times New Roman",
        serif;

    font-size:
        clamp(
            27px,
            7vw,
            31px
        );

    color: #543b49;

    margin-bottom: 20px;
}


.details-card {

    background:
        rgba(
            255,
            255,
            255,
            0.78
        );

    border:
        1px solid
        #f0dce5;

    border-radius: 18px;

    padding:
        8px 17px;
}


.detail-row {

    display: flex;

    align-items: center;

    gap: 12px;

    padding: 14px 0;

    border-bottom:
        1px solid
        #f3e5eb;
}


.detail-row:last-child {
    border-bottom: none;
}


.detail-emoji {

    font-size: 20px;

    width: 27px;

    flex-shrink: 0;

    text-align: center;
}


.detail-content {

    min-width: 0;

    flex: 1;
}


.detail-label {

    font-size: 10px;

    text-transform: uppercase;

    letter-spacing: 1px;

    color: #b08b9d;

    margin-bottom: 3px;
}


.detail-value {

    font-size: 14px;

    line-height: 1.4;

    font-weight: 600;

    color: #5e4351;

    word-break: break-word;
}


/* =====================================================
   FOOTER
===================================================== */

.footer {

    margin-top: 24px;

    text-align: center;

    color: #c19eae;

    font-size: 10px;

    letter-spacing: 0.5px;
}


/* =====================================================
   SMALL PHONES
===================================================== */

@media (max-width: 380px) {

    body {
        padding: 12px;
    }

    .card {

        padding:
            28px 20px;

        border-radius: 24px;

        max-height:
            calc(100dvh - 24px);
    }

    .logo {

        width: 60px;
        height: 60px;

        margin-bottom: 16px;
    }

    .subtitle {
        margin-bottom: 24px;
    }

    .input-group {
        margin-bottom: 17px;
    }

    .date-buttons {
        gap: 8px;
    }

    .yes-btn,
    .no-btn {

        padding-left: 19px;
        padding-right: 19px;

        font-size: 14px;
    }
}


/* =====================================================
   SHORT SCREENS
===================================================== */

@media (max-height: 650px) {

    body {

        align-items:
            flex-start;

        padding-top: 12px;
        padding-bottom: 12px;
    }

    .card {

        max-height:
            calc(100dvh - 24px);
    }

    .logo {

        width: 56px;
        height: 56px;

        margin-bottom: 12px;
    }

    .subtitle {
        margin-bottom: 20px;
    }
}


/* =====================================================
   DESKTOP HOVER
===================================================== */

@media (hover: hover) {

    .login-btn:hover,
    .proceed-btn:hover {

        transform:
            translateY(-2px);
    }

    .yes-btn:hover {

        transform:
            translateY(-2px)
            scale(1.02);
    }

}

</style>
</head>


<body>


<!-- =====================================================
     BACKGROUND
===================================================== -->

<div class="background-heart heart1">♡</div>

<div class="background-heart heart2">♡</div>

<div class="background-heart heart3">♡</div>

<div class="background-heart heart4">♡</div>


<!-- =====================================================
     MAIN CARD
===================================================== -->

<div class="card">


<!-- =====================================================
     LOGIN PAGE
===================================================== -->

<div id="loginPage">


    <div class="logo">
        ✦
    </div>


    <h1>
        Welcome
    </h1>


    <p class="subtitle">
        There's a little something waiting for you ✨
    </p>


    <!-- USERNAME -->

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


    <!-- PASSWORD -->

    <div class="input-group">

        <label for="password">
            Password
        </label>


        <div class="password-wrapper">

            <input
                type="password"
                id="password"
                placeholder="Enter your password"
                autocomplete="off"
            >


            <button
                type="button"
                class="show-password"
                onclick="togglePassword()"
            >
                ♡
            </button>

        </div>


        <div
            id="hint"
            class="hint"
        >
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
     DATE PAGE
===================================================== -->

<div
    id="datePage"
    class="date-page"
>


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
     REASON PAGE
===================================================== -->

<div
    id="reasonPage"
    class="reason-page"
>


    <div class="reason-icon">
        🥺
    </div>


    <div class="reason-title">
        Okay... tell me why?
    </div>


    <div class="reason-text">

        If you're saying no,
        at least give me a reason.

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
     WARNING PAGE
===================================================== -->

<div
    id="warningPage"
    class="warning-page"
>


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
     DETAILS PAGE
===================================================== -->

<div
    id="detailsPage"
    class="details-page"
>


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


        <!-- COMPANY -->

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
   PASSWORD VISIBILITY
===================================================== */

function togglePassword() {

    const password =
        document.getElementById(
            "password"
        );

    const button =
        document.querySelector(
            ".show-password"
        );


    if (
        password.type ===
        "password"
    ) {

        password.type =
            "text";

        button.textContent =
            "♥";

    } else {

        password.type =
            "password";

        button.textContent =
            "♡";
    }

}


/* =====================================================
   USERNAME HINT
===================================================== */

const usernameInput =
    document.getElementById(
        "username"
    );

const hint =
    document.getElementById(
        "hint"
    );


usernameInput.addEventListener(
    "input",
    function() {

        if (
            usernameInput.value
                .trim() !== ""
        ) {

            hint.classList.add(
                "show"
            );

        } else {

            hint.classList.remove(
                "show"
            );

        }

    }
);


/* =====================================================
   LOGIN
===================================================== */

function login() {

    const username =
        document
            .getElementById(
                "username"
            )
            .value
            .trim();


    const password =
        document
            .getElementById(
                "password"
            )
            .value
            .trim();


    const message =
        document.getElementById(
            "loginMessage"
        );


    /* USERNAME CHECK */

    if (
        username === ""
    ) {

        message.textContent =
            "Please enter your name.";

        message.className =
            "message error";

        return;
    }


    /* PASSWORD CHECK */

    if (
        password === ""
    ) {

        message.textContent =
            "Please enter your password.";

        message.className =
            "message error";

        return;
    }


    /* CORRECT PASSWORD */

    if (
        password === "14/03"
    ) {

        document
            .getElementById(
                "loginPage"
            )
            .style.display =
            "none";


        document
            .getElementById(
                "datePage"
            )
            .classList.add(
                "active"
            );


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
    document.getElementById(
        "noButton"
    );


function sayNo() {


    /*
       After 4 attempts,
       allow the No button
       to actually work.
    */

    if (
        noAttempts >= 4
    ) {

        document
            .getElementById(
                "datePage"
            )
            .classList.remove(
                "active"
            );


        document
            .getElementById(
                "reasonPage"
            )
            .classList.add(
                "active"
            );


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
        document.querySelector(
            ".date-buttons"
        );


    const areaWidth =
        area.clientWidth;


    const areaHeight =
        area.clientHeight;


    const buttonWidth =
        noButton.offsetWidth;


    const buttonHeight =
        noButton.offsetHeight;


    const maxX =
        Math.max(
            0,
            areaWidth -
            buttonWidth
        );


    const maxY =
        Math.max(
            0,
            areaHeight -
            buttonHeight
        );


    const randomX =
        Math.random() *
        maxX;


    const randomY =
        Math.random() *
        maxY;


    noButton.style.left =
        randomX + "px";


    noButton.style.top =
        randomY + "px";

}


/* =====================================================
   YES BUTTON
===================================================== */

function sayYes() {


    document
        .getElementById(
            "datePage"
        )
        .classList.remove(
            "active"
        );


    document
        .getElementById(
            "detailsPage"
        )
        .classList.add(
            "active"
        );

}


/* =====================================================
   SUBMIT REASON
===================================================== */

function submitReason() {


    const reason =
        document
            .getElementById(
                "reasonBox"
            )
            .value
            .trim();


    if (
        reason === ""
    ) {

        alert(
            "You have to give me a reason first 😭"
        );

        return;
    }


    document
        .getElementById(
            "reasonPage"
        )
        .classList.remove(
            "active"
        );


    document
        .getElementById(
            "warningPage"
        )
        .classList.add(
            "active"
        );


    /*
       Show warning for
       3.5 seconds, then
       reveal the date details.
    */

    setTimeout(
        function() {


            document
                .getElementById(
                    "warningPage"
                )
                .classList.remove(
                    "active"
                );


            document
                .getElementById(
                    "detailsPage"
                )
                .classList.add(
                    "active"
                );


        },
        3500
    );

}


</script>

</body>
</html>
