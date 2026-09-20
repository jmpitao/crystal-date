<style> * { box-sizing: border-box; } html, body { margin: 0; padding: 0; min-height: 100%; } body { min-height: 100vh; display: flex; justify-content: center; align-items: center; padding: 20px; font-family: Georgia, serif; background: radial-gradient( circle at top, #fff8fa, transparent 40% ), linear-gradient( 135deg, #ffeaf1, #fff5f8 ); color: #642b3d; } /* ================================ MAIN CARD ================================ */ .card { width: 100%; max-width: 600px; background: rgba(255,255,255,.94); border-radius: 28px; padding: 35px 25px; text-align: center; box-shadow: 0 15px 45px rgba(120,40,70,.15); } /* ================================ GENERAL ================================ */ .hidden { display: none !important; } .fade { animation: fade .8s ease; } .heart { font-size: 55px; color: #d95778; animation: heartbeat 1.5s infinite; } h1 { color: #9e3c59; margin-bottom: 15px; } h2 { color: #9e3c59; } /* ================================ STEP 1 ================================ */ .question { font-size: 23px; margin: 25px 0; } .buttons { display: flex; justify-content: center; align-items: center; gap: 15px; min-height: 80px; } /* ================================ BUTTONS ================================ */ button { border: none; border-radius: 30px; padding: 13px 30px; font-family: Georgia, serif; font-size: 16px; cursor: pointer; transition: .3s; user-select: none; -webkit-tap-highlight-color: transparent; } button:focus { outline: none; } /* YES BUTTON */ #yesBtn { background: #d95778; color: white; box-shadow: 0 5px 15px rgba(217,87,120,.25); } #yesBtn:hover { transform: scale(1.08); } /* NO BUTTON */ #noBtn { background: #eeeeee; color: #555; border: 1px solid #ddd; } /* ================================ STEP 2 ================================ */ .subtitle { line-height: 1.7; } /* ================================ DATE ================================ */ .date-box { margin-top: 25px; } input[type="date"] { width: 100%; max-width: 300px; padding: 13px; border: 2px solid #efb5c5; border-radius: 12px; font-size: 16px; color: #642b3d; background: white; font-family: Georgia, serif; } input[type="date"]:focus { outline: none; border-color: #d95778; box-shadow: 0 0 0 3px rgba(217,87,120,.12); } /* ================================ LOCATIONS ================================ */ .places { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 15px; } .place { padding: 18px 10px; border-radius: 16px; background: #fff4f7; border: 2px solid #f2c4d0; cursor: pointer; transition: .3s; user-select: none; -webkit-tap-highlight-color: transparent; } .place:hover { transform: translateY(-3px); box-shadow: 0 6px 15px rgba(120,40,70,.08); } .place.selected { background: #d95778; color: white; border-color: #d95778; transform: translateY(-2px); } /* ================================ CONFIRM BUTTON ================================ */ .confirm { margin-top: 25px; background: #9e3c59; color: white; } .confirm:hover { transform: scale(1.05); background: #87324d; } /* ================================ STEP 3 — LETTER ================================ */ .letter { margin-top: 25px; padding: 25px; background: #fff7fa; border-left: 4px solid #d95778; border-radius: 12px; text-align: left; line-height: 1.8; } .signature { text-align: right; font-style: italic; margin-top: 20px; } /* ================================ DATE SUMMARY ================================ */ .date-summary { margin-top: 20px; padding: 15px; background: #fff0f4; border-radius: 15px; line-height: 1.7; } /* ================================ ANIMATIONS ================================ */ @keyframes fade { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } } @keyframes heartbeat { 0%, 100% { transform: scale(1); } 50% { transform: scale(1.12); } } /* ================================ FLOATING HEARTS ================================ */ .floating-heart { position: fixed; bottom: -30px; color: #d95778; pointer-events: none; animation: floatUp 5s linear forwards; z-index: 9999; } @keyframes floatUp { from { transform: translateY(0); opacity: 1; } to { transform: translateY(-110vh); opacity: 0; } } /* ================================ MOBILE ================================ */ @media (max-width: 500px) { body { padding: 12px; } .card { padding: 28px 18px; border-radius: 22px; } .question { font-size: 20px; } .buttons { gap: 10px; } button { padding: 12px 22px; font-size: 15px; } .places { grid-template-columns: 1fr; } .letter { padding: 20px; } } /* ================================ SMALL PHONES ================================ */ @media (max-width: 360px) { .buttons { flex-direction: column; } #yesBtn, #noBtn { width: 160px; } } </style>
<!-- ============================
     STEP 1
============================= -->

<section id="step1">

    <div class="heart">
        ♡
    </div>

    <h1>
        Crystal...
    </h1>

    <div class="question">
        Will you go on a date with me? 🥺
    </div>

    <div class="buttons">

        <button id="yesBtn">
            Yes ♡
        </button>

        <button id="noBtn">
            No
        </button>

    </div>

</section>


<!-- ============================
     STEP 2
============================= -->

<section
    id="step2"
    class="hidden"
>

    <div class="heart">
        ♡
    </div>

    <h1>
        Yay! 🥹
    </h1>

    <p class="subtitle">

        Then you get to choose everything.

        <br>

        Pick a date and a place for us. 🤍

    </p>


    <div class="date-box">

        <h2>
            When? 📅
        </h2>

        <input
            type="date"
            id="datePicker"
        >

    </div>


    <div class="date-box">

        <h2>
            Where? 📍
        </h2>

        <div class="places">

            <div
                class="place"
                onclick="choosePlace(this, 'Festival Mall')"
            >
                🎡
                <br>
                Festival Mall
            </div>


            <div
                class="place"
                onclick="choosePlace(this, 'SM City Sucat')"
            >
                🛍️
                <br>
                SM City Sucat
            </div>


            <div
                class="place"
                onclick="choosePlace(this, 'SM BF')"
            >
                ☕
                <br>
                SM BF
            </div>


            <div
                class="place"
                onclick="choosePlace(this, 'SM Mall of Asia')"
            >
                🌊
                <br>
                SM MOA
            </div>

        </div>

    </div>


    <button
        class="confirm"
        onclick="confirmDate()"
    >
        Confirm ♡
    </button>

</section>


<!-- ============================
     STEP 3
============================= -->

<section
    id="step3"
    class="hidden"
>

    <div class="heart">
        ♡
    </div>

    <h1>
        For You, Crystal
    </h1>


    <div
        id="dateSummary"
        class="date-summary"
    >
    </div>


    <div class="letter">

        <p>
            Hi Crystal,
        </p>

        <p>
            I don't really know how to say this
            without making it awkward, so I decided
            to make this little thing for you instead.
        </p>

        <p>
            Thank you for saying yes.
        </p>

        <p>
            I just wanted to spend some time with you.
            Nothing too complicated — just us,
            some food, random conversations,
            stupid laughs, and hopefully a really
            nice memory together.
        </p>

        <p>
            I hope this little date becomes something
            we can both look back on and smile about.
        </p>

        <p>
            So I'll see you on our date, Crystal. 🤍
        </p>

        <div class="signature">
            — Shin ♡
        </div>

    </div>

</section>
<script> /* ================================ VARIABLES ================================ */ let selectedPlace = ""; let noCount = 0; /* ================================ YES BUTTON ================================ */ document .getElementById("yesBtn") .onclick = function() { document .getElementById("step1") .classList .add("hidden"); document .getElementById("step2") .classList .remove("hidden"); document .getElementById("step2") .classList .add("fade"); window.scrollTo({ top: 0, behavior: "smooth" }); }; /* ================================ NO BUTTON ================================ */ const noBtn = document.getElementById("noBtn"); const noMessages = [ "Are you sure? 🥺", "Really? 😭", "Think again...", "Please? 👉👈", "One more chance? 🥹", "I'll ask again ♡" ]; noBtn.onclick = function() { noCount++; noBtn.innerText = noMessages[ Math.min( noCount - 1, noMessages.length - 1 ) ]; const x = Math.floor( Math.random() * 140 ) - 70; const y = Math.floor( Math.random() * 60 ) - 30; noBtn.style.transform = `translate(${x}px, ${y}px)`; if (noCount >= 6) { setTimeout(function() { noCount = 0; noBtn.innerText = "No"; noBtn.style.transform = "translate(0, 0)"; }, 1000); } }; /* ================================ CHOOSE PLACE ================================ */ function choosePlace( element, place ) { document .querySelectorAll(".place") .forEach(function(item) { item.classList .remove("selected"); }); element .classList .add("selected"); selectedPlace = place; } /* ================================ CONFIRM DATE ================================ */ function confirmDate() { const date = document .getElementById("datePicker") .value; if (!date) { alert( "Crystal, pick a date first ♡" ); return; } if (!selectedPlace) { alert( "Choose where we're going too 🥺" ); return; } const formattedDate = new Date( date + "T00:00:00" ) .toLocaleDateString( "en-US", { weekday: "long", month: "long", day: "numeric", year: "numeric" } ); document .getElementById("dateSummary") .innerHTML = ` Our Date ♡
📅 ${formattedDate}
📍 ${selectedPlace} `; document .getElementById("step2") .classList .add("hidden"); document .getElementById("step3") .classList .remove("hidden"); document .getElementById("step3") .classList .add("fade"); window.scrollTo({ top: 0, behavior: "smooth" }); createHearts(); } /* ================================ FLOATING HEARTS ================================ */ function createHearts() { for ( let i = 0; i < 25; i++ ) { const heart = document.createElement("div"); heart.className = "floating-heart"; heart.innerText = Math.random() > 0.5 ? "♡" : "♥"; heart.style.left = Math.random() * 100 + "vw"; heart.style.fontSize = ( 15 + Math.random() * 20 ) + "px"; heart.style.animationDuration = ( 3 + Math.random() * 3 ) + "s"; document .body .appendChild(heart); setTimeout( function() { heart.remove(); }, 6000 ); } } </script>ument .getElementById("step3") .classList .remove("hidden"); document .getElementById("step3") .classList .add("fade"); window.scrollTo({ top: 0, behavior: "smooth" }); createHearts(); } /* ================================ FLOATING HEARTS ================================ */ function createHearts() { for ( let i = 0; i < 25; i++ ) { const heart = document.createElement("div"); heart.className = "floating-heart"; heart.innerText = Math.random() > 0.5 ? "♡" : "♥"; heart.style.left = Math.random() * 100 + "vw"; heart.style.fontSize = ( 15 + Math.random() * 20 ) + "px"; heart.style.animationDuration = ( 3 + Math.random() * 3 ) + "s"; document .body .appendChild(heart); setTimeout( function() { heart.remove(); }, 6000 ); } } </script>
