<style>

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    -webkit-tap-highlight-color: transparent;
}

html {
    width: 100%;
}

body {
    width: 100%;
    min-height: 100vh;
    min-height: 100dvh;

    display: flex;
    justify-content: center;
    align-items: center;

    /* MORE SPACE AROUND THE CARD */
    padding: 22px 16px;

    font-family: "Segoe UI", Arial, sans-serif;

    color: #4b3543;

    background:
        radial-gradient(circle at 5% 5%, #ffdbe9 0%, transparent 30%),
        radial-gradient(circle at 95% 10%, #e6dcff 0%, transparent 30%),
        radial-gradient(circle at 50% 100%, #ffeadc 0%, transparent 35%),
        #fff9fc;

    overflow-x: hidden;
}


/* =====================================================
   BACKGROUND HEARTS
===================================================== */

.background-heart {
    position: fixed;
    color: rgba(226, 117, 157, 0.10);
    pointer-events: none;
    user-select: none;
    z-index: 0;
    animation: floatHeart 7s ease-in-out infinite;
}

.heart1 {
    top: 8%;
    left: 5%;
    font-size: 25px;
}

.heart2 {
    bottom: 12%;
    left: 4%;
    font-size: 19px;
    animation-delay: 2s;
}

.heart3 {
    top: 12%;
    right: 5%;
    font-size: 21px;
    animation-delay: 1s;
}

.heart4 {
    bottom: 8%;
    right: 5%;
    font-size: 27px;
    animation-delay: 3s;
}

@keyframes floatHeart {

    0%, 100% {
        transform: translateY(0) rotate(0deg);
    }

    50% {
        transform: translateY(-8px) rotate(5deg);
    }
}


/* =====================================================
   CARD
===================================================== */

.card {

    /* INTENTIONALLY SMALLER */
    width: min(92%, 390px);

    max-height: calc(100dvh - 44px);

    overflow-y: auto;
    overflow-x: hidden;

    /* SMALLER INTERNAL SPACING */
    padding: 27px 23px;

    background: rgba(255, 255, 255, 0.80);

    border: 1px solid rgba(255,255,255,0.9);

    border-radius: 25px;

    box-shadow:
        0 18px 48px rgba(170,110,140,0.14),
        0 5px 16px rgba(170,110,140,0.06);

    backdrop-filter: blur(16px);
    -webkit-backdrop-filter: blur(16px);

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
        transform: translateY(12px);
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

    width: 55px;
    height: 55px;

    margin: 0 auto 14px;

    display: flex;
    justify-content: center;
    align-items: center;

    border-radius: 50%;

    background:
        linear-gradient(
            135deg,
            #f5aac5,
            #c8b5f4
        );

    color: white;

    font-size: 22px;

    box-shadow:
        0 8px 18px rgba(210,130,165,0.20);
}

h1 {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    /* SMALLER */
    font-size: 25px;

    font-weight: 500;

    color: #543b49;

    margin-bottom: 6px;
}

.subtitle {

    text-align: center;

    color: #9b7d8c;

    /* SMALLER */
    font-size: 12px;

    line-height: 1.45;

    margin-bottom: 21px;
}


/* =====================================================
   INPUTS
===================================================== */

.input-group {
    margin-bottom: 14px;
}

label {

    display: block;

    margin-bottom: 6px;

    font-size: 11px;

    font-weight: 600;

    color: #6c4c5c;
}

input {

    width: 100%;

    /* SMALLER */
    min-height: 44px;

    padding: 10px 13px;

    border-radius: 12px;

    border: 1px solid #efd9e3;

    background: rgba(255,255,255,0.8);

    color: #4b3543;

    /* SMALLER */
    font-size: 14px;

    outline: none;
}

input::placeholder {
    color: #c0a8b4;
}

input:focus {

    border-color: #e3a1bc;

    background: white;

    box-shadow:
        0 0 0 3px rgba(231,157,188,0.11);
}


/* =====================================================
   PASSWORD
===================================================== */

.password-wrapper {
    position: relative;
}

.password-wrapper input {
    padding-right: 45px;
}

.show-password {

    position: absolute;

    right: 4px;
    top: 50%;

    transform: translateY(-50%);

    width: 36px;
    height: 36px;

    display: flex;
    align-items: center;
    justify-content: center;

    border: none;

    background: transparent;

    color: #b38d9e;

    font-size: 15px;
}

.hint {

    display: none;

    margin-top: 6px;

    font-size: 10px;

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

    /* SMALLER */
    min-height: 44px;

    padding: 10px 15px;

    border: none;

    border-radius: 12px;

    background:
        linear-gradient(
            135deg,
            #e995b6,
            #b9a0e8
        );

    color: white;

    /* SMALLER */
    font-size: 13px;

    font-weight: 600;

    cursor: pointer;

    box-shadow:
        0 7px 17px rgba(204,132,166,0.20);
}

.login-btn {
    margin-top: 3px;
}


/* =====================================================
   MESSAGE
===================================================== */

.message {

    min-height: 16px;

    margin-top: 10px;

    text-align: center;

    font-size: 11px;
}

.error {
    color: #d66b83;
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

    /* SMALLER */
    font-size: 42px;

    margin-bottom: 7px;

    animation: heartbeat 1.5s infinite;
}

@keyframes heartbeat {

    0%,100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.07);
    }
}

.date-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    /* SMALLER */
    font-size: 25px;

    font-weight: 500;

    color: #543b49;

    margin-bottom: 8px;
}

.date-question {

    text-align: center;

    /* SMALLER */
    font-size: 14px;

    line-height: 1.45;

    color: #704f60;

    margin-bottom: 19px;
}


/* =====================================================
   YES / NO
===================================================== */

.date-buttons {

    width: 100%;

    height: 53px;

    position: relative;

    display: flex;

    align-items: center;

    justify-content: center;

    gap: 10px;

    overflow: hidden;
}

.yes-btn,
.no-btn {

    min-height: 42px;

    padding: 9px 19px;

    border-radius: 50px;

    /* SMALLER */
    font-size: 13px;

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
        0 6px 15px rgba(210,120,160,0.20);
}

.no-btn {

    position: absolute;

    left: calc(50% + 5px);

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

    font-size: 38px;

    margin-bottom: 7px;
}

.reason-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 23px;

    color: #543b49;

    margin-bottom: 7px;
}

.reason-text {

    text-align: center;

    color: #9b7d8c;

    font-size: 11px;

    line-height: 1.5;

    margin-bottom: 14px;
}

.reason-box {

    width: 100%;

    min-height: 100px;

    padding: 11px;

    resize: vertical;

    border-radius: 12px;

    border: 1px solid #efd9e3;

    background: rgba(255,255,255,0.85);

    color: #4b3543;

    font-family: inherit;

    font-size: 14px;

    outline: none;
}

.proceed-btn {
    margin-top: 10px;
}


/* =====================================================
   WARNING
===================================================== */

.warning-icon {

    text-align: center;

    font-size: 43px;

    margin-bottom: 8px;
}

.warning-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 25px;

    color: #543b49;

    margin-bottom: 11px;
}

.warning-message {

    text-align: center;

    font-size: 13px;

    line-height: 1.55;

    color: #704f60;
}


/* =====================================================
   DETAILS
===================================================== */

.details-icon {

    text-align: center;

    font-size: 43px;

    margin-bottom: 6px;
}

.details-title {

    text-align: center;

    font-family: Georgia, "Times New Roman", serif;

    font-size: 25px;

    color: #543b49;

    margin-bottom: 14px;
}

.details-card {

    background: rgba(255,255,255,0.78);

    border: 1px solid #f0dce5;

    border-radius: 14px;

    padding: 4px 13px;
}

.detail-row {

    display: flex;

    align-items: center;

    gap: 9px;

    padding: 10px 0;

    border-bottom: 1px solid #f3e5eb;
}

.detail-row:last-child {
    border-bottom: none;
}

.detail-emoji {

    width: 23px;

    flex-shrink: 0;

    text-align: center;

    font-size: 17px;
}

.detail-content {
    min-width: 0;
    flex: 1;
}

.detail-label {

    font-size: 8px;

    text-transform: uppercase;

    letter-spacing: 0.8px;

    color: #b08b9d;

    margin-bottom: 2px;
}

.detail-value {

    font-size: 12px;

    line-height: 1.3;

    font-weight: 600;

    color: #5e4351;

    word-break: break-word;
}


/* =====================================================
   FOOTER
===================================================== */

.footer {

    margin-top: 16px;

    text-align: center;

    color: #c19eae;

    font-size: 8px;

    letter-spacing: 0.3px;
}


/* =====================================================
   EXTRA SMALL PHONES
===================================================== */

@media (max-width: 360px) {

    body {
        padding: 18px 12px;
    }

    .card {

        width: 94%;

        padding: 24px 19px;

        border-radius: 22px;
    }

    h1 {
        font-size: 23px;
    }

    .date-title {
        font-size: 23px;
    }

    .date-question {
        font-size: 13px;
    }

}


/* =====================================================
   SHORT PHONES
===================================================== */

@media (max-height: 650px) {

    body {
        align-items: flex-start;

        padding-top: 10px;
        padding-bottom: 10px;
    }

    .card {
        max-height: calc(100dvh - 20px);
    }

}

</style>
