<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I'm Sorry</title>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            color: #333;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            max-width: 600px;
            background-color: #fff;
            padding: 30px;
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
            border-radius: 12px;
            text-align: center;
        }
        h1 {
            color: #ff6f61;
            margin-bottom: 20px;
        }
        p {
            line-height: 1.8;
            margin: 15px 0;
            font-size: 1.1em;
        }
        .signature {
            margin-top: 30px;
            font-style: italic;
            color: #555;
        }
        .heart {
            font-size: 2em;
            color: #ff6f61;
            margin: 20px 0;
        }
        .emoji {
            font-size: 1.5em;
            margin: 10px;
        }
        .actions {
            margin-top: 20px;
        }
        .actions button {
            padding: 10px 20px;
            margin: 5px;
            font-size: 1em;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.3s ease, font-size 0.3s ease;
        }
        .actions .yes {
            background-color: #ff6f61;
            color: white;
        }
        .actions .no {
            background-color: #ddd;
            color: #333;
        }
        .actions .yes:hover {
            transform: scale(1.1);
        }
        .actions .no:hover {
            transform: scale(0.9);
        }
        footer {
            margin-top: 20px;
            font-size: 0.9em;
            color: #777;
        }
    </style>
    <script>
        function handleResponse(response) {
            if (response === 'yes') {
                window.location.href = 'forgiveness.html';
            } else if (response === 'no') {
                const noButton = document.querySelector('.actions .no');
                let currentFontSize = parseFloat(window.getComputedStyle(noButton).fontSize);
                const interval = setInterval(() => {
                    if (currentFontSize > 5) {
                        currentFontSize -= 0.5;
                        noButton.style.fontSize = currentFontSize + 'px';
                    } else {
                        clearInterval(interval);
                        noButton.style.display = 'none';
                    }
                }, 100);
            }
        }
    </script>
</head>
<body>
    <div class="container">
        <h1>I'm Sorry Gudu ❤️</h1>
        
        <p>I want to begin by saying how deeply sorry I am for always doing the same mistake. Hurting you is the last thing I would ever want to do.</p>
        <p>You mean so much to me bche 💕 You are my everything. I realize I could have handled things differently by acting maturely instead of ego. I am committed to being better for you and for us.</p>
        <p> i will never repeat such things pka se...! i hope you can forgive me. I love you more than anything. 🥺❤️</p>
        <div class="heart">❤️</div>
        <div class="actions">
            <button class="yes" onclick="handleResponse('yes')">Forgive Me</button>
            <button class="no" onclick="handleResponse('no')">No</button>
        </div>
        <div class="signature">
            Forever yours,<br>
            Your Raghu
        </div>
    </div>
    <footer>
        &copy; 2025 Built with Love
    </footer>
</body>
</html>
