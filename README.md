<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- No visible crystal-date heading -->
<title></title>

<style>
* {
    box-sizing: border-box;
}

html, body {
    margin: 0;
    padding: 0;
    min-height: 100%;
}

body {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    font-family: Georgia, serif;
    background:
        radial-gradient(circle at top, #fff8fa, transparent 40%),
        linear-gradient(135deg, #ffeaf1, #fff5f8);
    color: #642b3d;
}

.card {
    width: 100%;
    max-width: 600px;
    background: rgba(255,255,255,.94);
    border-radius: 28px;
    padding: 35px 25px;
    text-align: center;
    box-shadow: 0 15px 45px rgba(120,40,70,.15);
}

.hidden {
    display: none !important;
}

.fade {
    animation: fade .8s ease;
}

.heart {
    font-size: 55px;
    color: #d95778;
    animation: heartbeat 1.5s infinite;
}

h1 {
    color: #9e3c59;
    margin-bottom: 15px;
}

h2 {
    color: #9e3c59;
}

.question {
    font-size: 23px;
    margin: 25px 0;
}

.buttons {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 15px;
    min-height: 80px;
}

button {
    border: none;
    border-radius: 30px;
    padding: 13px 30px;
    font-family: Georgia, serif;
    font-size: 16px;
    cursor: pointer;
    transition: .3s;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}

button:focus {
    outline: none;
}

#yesBtn {
    background: #d95778;
    color: white;
    box-shadow: 0 5px 15px rgba(217,87,120,.25);
}

#yesBtn:hover {
    transform: scale(1.08);
}

#noBtn {
    background: #eeeeee;
    color: #555;
    border: 1px solid #ddd;
}

.subtitle {
    line-height: 1.7;
}

.date-box {
    margin-top: 25px;
}

input[type="date"] {
    width: 100%;
    max-width: 300px;
    padding: 13px;
    border: 2px solid #efb5c5;
    border-radius: 12px;
    font-size: 16px;
    color: #642b3d;
    background: white;
    font-family: Georgia, serif;
}

input[type="date"]:focus {
    outline: none;
    border-color: #d95778;
    box-shadow: 0 0 0 3px rgba(217,87,120,.12);
}

.places {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-top: 15px;
}

.place {
    padding: 18px 10px;
    border-radius: 16px;
    background: #fff4f7;
    border: 2px solid #f2c4d0;
    cursor: pointer;
    transition: .3s;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
}

.place:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 15px rgba(120,40,70,.08);
}

.place.selected {
    background: #d95778;
    color: white;
    border-color: #d95778;
    transform: translateY(-2px);
}

.confirm {
    margin-top: 25px;
    background: #9e3c59;
    color: white;
}

.confirm:hover {
    transform: scale(1.05);
    background: #87324d;
}

.letter {
    margin-top: 25px;
    padding: 25px;
    background: #fff7fa;
    border-left: 4px solid #d95778;
    border-radius: 12px;
    text-align: left;
    line-height: 1.8;
}

.signature {
    text-align: right;
    font-style: italic;
    margin-top: 20px;
}

.date-summary {
    margin-top: 20px;
    padding: 15px;
    background: #fff0f4;
    border-radius: 15px;
    line-height: 1.7;
}

@keyframes fade {
    from {
        opacity: 0;
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes heartbeat {
    0%, 100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.12);
    }
}

.floating-heart {
    position: fixed;
    bottom: -30px;
    color: #d95778;
    pointer-events: none;
    animation: floatUp 5s linear forwards;
    z-index: 9999;
}

@keyframes floatUp {
    from {
        transform: translateY(0);
        opacity: 1;
    }

    to {
        transform: translateY(-110vh);
        opacity: 0;
    }
}

@media (max-width: 500px) {
    body {
        padding: 12px;
    }

    .card {
        padding: 28px 18px;
        border-radius: 22px;
    }

    .question {
        font-size: 20px;
    }

    .buttons {
        gap: 10px;
    }

    button {
        padding: 12px 22px;
        font-size: 15px;
    }

    .places {
        grid-template-columns: 1fr;
    }

    .letter {
        padding: 20px;
    }
}

@media (max-width: 360px) {
    .buttons {
        flex-direction: column;
    }

    #yesBtn,
    #noBtn {
        width: 160px;
    }
}
</style>
</head>

<body>

<div class="card">

<!-- YOUR EXISTING STEP 1, STEP 2, STEP 3 CODE GOES HERE -->

</div>

<!-- YOUR EXISTING SCRIPT GOES HERE -->

</body>
</html>
</script>
