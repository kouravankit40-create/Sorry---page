# Sorry---page<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="A heartfelt apology webpage for Kavya with shayari and confetti!">
    <title>I'm Sorry Kavya ❤️</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
        }
        .container {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            max-width: 500px;
            width: 90%;
            animation: fadeIn 1.8s ease-in-out;
        }
        h1 {
            color: #ff4d6d;
            font-size: 36px;
            margin-bottom: 15px;
        }
        p {
            font-size: 18px;
            color: #555;
            margin: 20px 0;
            line-height: 1.6;
        }
        .shayari {
            font-style: italic;
            color: #ff4d6d;
            margin-top: 15px;
            font-size: 17px;
            opacity: 0;
            animation: fadeInShayari 3s ease-in-out 1s forwards;
        }
        button {
            background: #ff4d6d;
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 16px;
            border-radius: 25px;
            cursor: pointer;
            transition: 0.3s;
            margin-top: 20px;
        }
        button:hover {
            background: #e63950;
            transform: scale(1.05);
        }
        .heart {
            font-size: 40px;
            animation: heartbeat 1.5s infinite;
            margin-bottom: 15px;
        }
        @keyframes fadeIn {
            from {opacity: 0; transform: translateY(20px);}
            to {opacity: 1; transform: translateY(0);}
        }
        @keyframes fadeInShayari {
            from {opacity: 0; transform: translateY(10px);}
            to {opacity: 1; transform: translateY(0);}
        }
        @keyframes heartbeat {
            0%, 40%, 100% { transform: scale(1); }
            25%, 60% { transform: scale(1.2); }
        }
        @media (max-width: 500px) {
            h1 { font-size: 28px; }
            p, .shayari { font-size: 16px; }
            button { padding: 10px 20px; font-size: 15px; }
            .heart { font-size: 30px; }
            .container { padding: 30px 20px; }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="heart" aria-label="Heart emoji">❤️</div>
    <h1>I'm Truly Sorry, Kavya</h1>
    <p>
       me maafi chahunga 🥹 ln.  
        i am really sorry sorry 🎀.
    </p>
    <div class="shayari">
        "Galti meri thi, par khamoshi tumhari bhi thi,  
        Maafi maang raha hoon dil se, kyunki zarurat tumhari hi thi."
    </div>
    <button onclick="forgive()" aria-label="Forgive button">Click if you forgive me 💕</button>
</div>

<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
<script>
    // Check if already forgiven (persistent)
    if(localStorage.getItem('forgiven')) {
        forgive();
    }

    function forgive() {
        const btn = document.querySelector('button');
        btn.innerText = "Thank You ❤️";
        btn.disabled = true;
        btn.style.background = "#8ecae6";
        localStorage.setItem('forgiven', 'true');

        // Confetti effect
        confetti({
            particleCount: 120,
            spread: 70,
            origin: { y: 0.6 }
        });
    }
</script>

</body>
</html>
