<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tłumaczenie strony</title>
    <style>
        .language-switch {
            position: absolute;
            top: 100px;
            right: 20px;
            background-color: #2c84c9;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 14px;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <button class="language-switch" id="languageSwitch">Switch to English</button>
    <div id="content">
        <h1>
            <span class="lang-pl">Witaj na stronie konferencji!</span>
            <span class="lang-en hidden">Welcome to the conference page!</span>
        </h1>
        <p>
            <span class="lang-pl">Ta konferencja dotyczy nowoczesnych technologii w edukacji.</span>
            <span class="lang-en hidden">This conference is about modern technologies in education.</span>
        </p>
        <p>
            <span class="lang-pl">Data: 29–30 maja 2025</span>
            <span class="lang-en hidden">Date: May 29–30, 2025</span>
        </p>
    </div>
    <script>
        // Funkcja do przełączania języka
        const switchButton = document.getElementById('languageSwitch');
        const polishTexts = document.querySelectorAll('.lang-pl');
        const englishTexts = document.querySelectorAll('.lang-en');
        switchButton.addEventListener('click', () => {
            // Przełącz język
            polishTexts.forEach(text => text.classList.toggle('hidden'));
            englishTexts.forEach(text => text.classList.toggle('hidden'));
            // Zmień tekst przycisku
            if (switchButton.textContent === 'Switch to English') {
                switchButton.textContent = 'Przełącz na polski';
            } else {
                switchButton.textContent = 'Switch to English';
            }
        });
    </script>
</body>
</html>
