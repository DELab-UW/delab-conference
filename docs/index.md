
<img src="./assets/baner_en.png" alt="delab photo" style="width: 100vw; height: auto; object-fit: cover; display: block; margin: 0; padding: 0;">


<!-- Sekcja lokalizacji -->
<div class="location-container">
        <span class="location-icon">
            <!-- Ikona lokalizacji (np. Font Awesome lub inna) -->
            <svg xmlns="http://www.w3.org/2000/svg" height="45" viewBox="0 0 24 24" width="45" fill="#888888"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
        </span>
        <span class="lang-pl">Uniwersytet Warszawski, Wydział Neofilologii Warszawa, ul. Dobra 55</span>
        <span class="lang-en hidden">University of Warsaw, Faculty of Neophilology, Warsaw, ul. Dobra 55</span>
</div>

<br>

<!-- Nagłówek -->
<h1>
    <span class="lang-pl"><b>Weź udział w konferencji i stań się częścią rewolucji w nauce i edukacji!</b></span>
    <span class="lang-en hidden"><b>Join the conference and be part of the revolution in science and education!</b></span>
</h1>

<!-- Przycisk rejestracji-->
<div class="info-button-container">
    <!-- Przycisk rejestracji -->
    <a href="#register" class="info-button">
        <span class="lang-pl">Zarejestruj się teraz</span>
        <span class="lang-en hidden">Register now</span>
    </a>
    <!-- Przycisk Call for Papers -->
    <a href="#call" class="info-button">
        <span class="lang-pl">Call for papers</span>
        <span class="lang-en hidden">Call for papers</span>
    </a>
</div>


<!-- Timer -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Countdown Timer</title>
    <style>
        /* Stylizacja sekcji odliczania */
        .countdown-container {
            text-align: center;
            background-color: #fff;
            color: grey;
            padding: 20px 20px;
            font-family: Poppins;
            border-radius: 5px;
            max-width: 600px;
            margin: 20px auto;
        }
        .countdown-title {
            font-size: 1.5em;
            margin-bottom: 10px;
        }
        .countdown-timer {
            display: flex;
            justify-content: center;
            gap: 30px;
            font-size: 1.2em;
            font-weight: bold;
        }
        .countdown-timer div {
            text-align: center;
        }
        .countdown-timer span {
            display: block;
            font-size: 2em;
            color: #2c84c9; /* Akcent - czerwony */
        }
        .countdown-labels {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-left: 45px;
            margin-top: 10px;
            font-size: 1em;
            text-transform: uppercase;
            color: #BFBFBF;
        }
    </style>
</head>
<body>
    <div class="countdown-container">
        <div class="countdown-title">
            <span class="lang-pl">Konferencja rozpocznie się już za:</span>
            <span class="lang-en hidden">The conference starts in:</span>
        </div>
        <!-- Timer liczb -->
        <div class="countdown-timer">
            <div>
                <span id="days">0</span>
            </div>
            <div>
                <span id="hours">0</span>
            </div>
            <div>
                <span id="minutes">0</span>
            </div>
            <div>
                <span id="seconds">0</span>
            </div>
        </div>
        <!-- Etykiety dla wartości -->
        <div class="countdown-labels">
            <div>
                <span class="lang-pl">Dni</span>
                <span class="lang-en hidden">Days</span>
            </div>
            <div>
                <span class="lang-pl">Godziny</span>
                <span class="lang-en hidden">Hours</span>
            </div>
            <div>
                <span class="lang-pl">Minuty</span>
                <span class="lang-en hidden">Minutes</span>
            </div>
            <div>
                <span class="lang-pl">Sekundy</span>
                <span class="lang-en hidden">Seconds</span>
            </div>
        </div>
    </div>

<script>
        // Funkcja odliczania
        function countdown() {
            const eventDate = new Date("May 29, 2025 00:00:00").getTime();
            const now = new Date().getTime();
            const timeLeft = eventDate - now;
            const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
            document.getElementById("days").textContent = days;
            document.getElementById("hours").textContent = hours;
            document.getElementById("minutes").textContent = minutes;
            document.getElementById("seconds").textContent = seconds;
            // Jeśli czas minął
            if (timeLeft < 0) {
                clearInterval(timer);
                document.querySelector(".countdown-title").textContent = "Konferencja już się rozpoczęła!";
                document.querySelector(".countdown-timer").style.display = "none";
                document.querySelector(".countdown-labels").style.display = "none";
            }
        }
        // Uruchomienie odliczania
        const timer = setInterval(countdown, 1000);
        countdown();
    </script>
</body>
</html>



<style>
/* Stylowanie kontenera dla przycisku */
.info-button-container {
    text-align: center; /* Wyśrodkowanie przycisku */
    margin-top: 30px; /* Dodanie większej przestrzeni nad przyciskiem */
}

/* Stylowanie przycisku */
.info-button {
    background-color: #155B83; /* Ciemnoniebieski kolor przycisku */
    color: #FFFFFF; /* Biały tekst */
    text-decoration: none; /* Usunięcie podkreślenia */
    padding: 15px 30px; /* Większe wewnętrzne odstępy */
    border-radius: 50px; /* Mocno zaokrąglone rogi */
    font-size: 1.3em; /* Większy rozmiar tekstu */
    font-weight: bold; /* Pogrubienie tekstu */
    display: inline-block; /* Blokowy styl dla stylizacji */
    transition: all 0.3s ease; /* Płynna animacja na hover */
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Lekki cień */
}

/* Efekt hover na przycisku */
.info-button:hover {
    background-color: #0D3E5C; /* Jeszcze ciemniejszy niebieski przy najechaniu */
    box-shadow: 0 6px 8px rgba(0, 0, 0, 0.2); /* Większy cień przy hover */
    transform: translateY(-2px); /* Subtelne uniesienie przycisku */
    color: #FFFFFF; /* Utrzymanie białego tekstu */
}
</style>

<br>


<!-- Opis -->
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">

<div class="about-section">
    
<!-- Nagłówek sekcji -->
<div class="about-title">
    <span class="lang-pl">O konferencji GenAI w edukacji wyższej</span>
    <span class="lang-en hidden">About the GenAI Conference in Higher Education</span>
</div>
    <p class="about-text">
        <span class="lang-pl">Poznaj możliwości generatywnej sztucznej inteligencji w edukacji i nauce! Konferencja GenAI to miejsce, gdzie liderzy, badacze i praktycy spotykają się, aby omówić przyszłość technologii AI w kształtowaniu dydaktyki i badań naukowych.</span>
        <span class="lang-en hidden">Explore the possibilities of generative AI in education and science! The GenAI conference is a place where leaders, researchers and practitioners meet to discuss the future of AI technologies in shaping teaching and research.</span>
    </p>

<!-- Sekcja obszarów tematycznych -->
<div class="topics-container">
        <!-- Obszar tematyczny 1 -->
        <div class="topic">
            <div class="icon-container">
                <i class="fas fa-globe" style="color: #2c84c9; font-size: 24px;"></i>
            </div>
            <div class="topic-content">
                <h3>
                <span class="lang-pl">Nowoczesna dydaktyka</span>
                <span class="lang-en hidden">Modern didactics</span>
                </h3>
                <p>
                <span class="lang-pl">Jak generatywna AI zmienia sposób nauczania i uczenia się.</span>
                <span class="lang-en hidden">How generative AI is changing the way we teach and learn.</span>
                </p>
            </div>
        </div>
        
<!-- Obszar tematyczny 2 -->
<div class="topic">
            <div class="icon-container">
                <i class="fas fa-microscope" style="color: #2c84c9; font-size: 24px;"></i>
            </div>
            <div class="topic-content">
                <h3>
                <span class="lang-pl">Innowacyjne badania naukowe</span>
                <span class="lang-en hidden">Innovative research</span>
                </h3>
                <p>
                <span class="lang-pl">Przełomowe zastosowania AI w nauce i badaniach.</span>
                <span class="lang-en hidden">Groundbreaking applications of AI in science and research.</span>
                </p>
            </div>
</div>

<!-- Obszar tematyczny 3 -->
<div class="topic">
            <div class="icon-container">
                <i class="fas fa-university" style="color: #2c84c9; font-size: 24px;"></i>
            </div>
            <div class="topic-content">
                <h3>
                <span class="lang-pl">Dobre praktyki w edukacji</span>
                <span class="lang-en hidden">Best practices in education</span>
                </h3>
                <p>
                <span class="lang-pl">Inspirujące przykłady wdrożeń technologii na uczelniach.</span>
                <span class="lang-en hidden">Inspiring examples of technology implementations at universities.</span>
                </p>
            </div>
        </div>

<!-- Obszar tematyczny 4 -->
<div class="topic">
            <div class="icon-container">
                <i class="fas fa-handshake" style="color: #2c84c9; font-size: 24px;"></i>
            </div>
            <div class="topic-content">
                <h3>
                <span class="lang-pl">Budowanie portalu wiedzy</span>
                <span class="lang-en hidden">Building a knowledge portal</span>
                </h3>
                <p>
                <span class="lang-pl">Tworzenie platformy wymiany doświadczeń między badaczami, firmami i dydaktykami.</span>
                <span class="lang-en hidden">Creating a platform for the exchange of experiences between researchers, companies and educators.</span>
                </p>
            </div>
        </div>
    </div>
</div>

<br>



<!-- Agenda -->

<h1 id="harmonogram" style="margin-top: 50px;">
    <span class="lang-pl"><b>Harmonogram wydarzenia</b></span>
    <span class="lang-en hidden"><b>Event Schedule</b></span></h1>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <div class="agenda-container">
        <!-- Bloki z dniami -->
        <div class="agenda-days">
            <div class="agenda-day active" data-day="day1">
                <span class="day-title">
                    <span class="lang-pl">Dzień 1</span>
                    <span class="lang-en hidden">Day 1</span>
                </span><br>
                <span class="day-subtitle">
                    <span class="lang-pl">czwartek 29.05</span>
                    <span class="lang-en hidden">Thursday 29.05</span>
                </span>
            </div>
            <div class="agenda-day" data-day="day2">
                <span class="day-title">
                    <span class="lang-pl">Dzień 2</span>
                    <span class="lang-en hidden">Day 2</span>
                </span><br>
                <span class="day-subtitle">
                    <span class="lang-pl">piątek 30.05</span>
                    <span class="lang-en hidden">Friday 30.05</span>
                </span>
            </div>
        </div>
        <!-- Harmonogram wyświetlany dynamicznie -->
        <div class="agenda-schedule active" id="day1">
            <h3> </h3>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">9:00-10:00</div>
                        <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                            <span class="lang-pl">Główna aula 0.410</span>
                            <span class="lang-en hidden">Main hall 0.410</span>
                            </span>
                    <div class="event-title">
                        <span class="lang-pl">Otwarcie konferencji</span>
                        <span class="lang-en hidden">Opening of the conference</span>
                    </div> 
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl">Uroczyste przemówienie JM rektora</span>
                    <span class="lang-en hidden">Ceremonial Address by His Magnificence the Rector</span>
                    <br>
                    <span class="lang-pl">Wystąpienia ministrów</span>
                    <span class="lang-en hidden">Ministers' speeches</span>
                    <br>
                    <span class="lang-pl">Wystąpienie Dyrektor DELab UW</span>
                    <span class="lang-en hidden">Speech by the Director of DELab UW</span>
                    </p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">10:00-11:00</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                            <span class="lang-pl">Główna aula 0.410</span>
                            <span class="lang-en hidden">Main hall 0.410</span>
                        </span>
                    <div class="event-title">Keynote Speech</div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl">prof. Neil Selwyn (Monash University, Australia)</span>
                    <span class="lang-en hidden">prof. Neil Selwyn (Monash University, Australia)</span>
                    <br>
                    <span class="lang-pl">Temat: Wpływ nowych technologii na edukację i naukę (TBC)</span>
                    <span class="lang-en hidden">Topic: The impact of new technologies on education and science (TBC)</span>
                    </p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">11:00-11:30</div>
                    <div class="event-title"></div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl">Przerwa kawowa</span>
                    <span class="lang-en hidden">Coffee break</span>
                    </p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">11:30 - 13:00</div>
                    <div class="event-title">
                        <span class="lang-pl">Sesje równoległe</span>
                        <span class="lang-en hidden">Parallel sessions</span>
                    </div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl"><b>Nauka i Badania</b></span>
                    <span class="lang-en hidden"><b>Science and Research</b></span>
                    <br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                            <span class="lang-pl">Sala: 1.132</span>
                            <span class="lang-en hidden">Room: 1.132</span>
                        </span>
                        <br>
                        <span class="lang-pl">Temat: Nowe paradygmaty badawcze w erze cyfrowej</span>
                        <span class="lang-en hidden">Topic: New research paradigms in the digital era</span>
                        <br>
                    <br>
                    <span class="lang-pl"><b>Dydaktyka</b></span>
                    <span class="lang-en hidden"><b>Didactics</b></span>
                    <br><svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                        <span class="lang-pl">Sala: 1.138</span>
                        <span class="lang-en hidden">Room: 1.138</span>
                        </span>
                        <br>
                        <span class="lang-pl">Temat: Nowe podejścia edukacyjne w erze cyfrowej</span>
                        <span class="lang-en hidden">Topic: New educational approaches in the digital era</span>
                    <br>
                    <br>
                    <span class="lang-pl"><b>Otoczenie uczelni</b></span>
                    <span class="lang-en hidden"><b>University ecosystem</b></span>
                    <br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                        <span class="lang-pl">Sala: 1.128</span>
                        <span class="lang-en hidden">Room: 1.128</span>
                        </span>
                        <br>
                        <span class="lang-pl">Temat: Nowe wzorce współpracy w erze cyfrowej</span>
                        <span class="lang-en hidden">Topic: New patterns of collaboration in digital era </span>
                        <br>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">13:00 - 14:00</div>
                    <div class="event-title"> </div>
                </div>
                <div class="event-right">
                    <p>Lunch</p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">14:00 - 15:30</div>
                    <div class="event-title">
                    </div>
                </div>
                <div class="event-right">
                    <span class="lang-pl"><b>Warsztaty</b></span>
                    <span class="lang-en hidden"><b>Workshops</b></span>
                    <br>
                    <br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                        <span class="lang-pl">Sala: 1.132</span>
                        <span class="lang-en hidden">Room: 1.132</span>
                    </span>
                    <br>
                    <span class="lang-pl">Temat: Automatyzacja procesów badawczych</span>
                    <span class="lang-en hidden">Topic: Automation of research processes</span>
                    <br><br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                        <span class="lang-pl">Sala: 1.138</span>
                        <span class="lang-en hidden">Room: 1.138</span>
                    </span><br>
                    <span class="lang-pl">Temat: Włączanie nowych narzędzi cyfrowych w procesy dydaktyczne</span>
                    <span class="lang-en hidden">Topic: Incorporating new digital tools into teaching processes</span>
                    <br>
                    <br>
                    <br>
                    <span class="lang-pl"><b>Dyskusje</b></span>
                    <span class="lang-en hidden"><b>Discussions</b></span>
                    <br>
                    <br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span class="lang-pl">Sala: 1.128</span>
                    <span class="lang-en hidden">Room: 1.128</span>
                    <br>
                    <span class="lang-pl">Temat: EdTechs w szkolnictwie wyższym. Możliwości i wyzwania</span>
                    <span class="lang-en hidden">Topic: EdTechs in higher education. Opportunities and challenges</span>
                    <br>
                    <br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span class="lang-pl">Główna aula 0.410</span>
                    <span class="lang-en hidden">Main hall 0.410</span>
                    <br>
                    <span class="lang-pl">Temat: </span>
                    <span class="lang-en hidden">Topic: </span>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">15:30 - 16:00</div>
                    <div class="event-title"> </div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl">Przerwa kawowa</span>
                    <span class="lang-en hidden">Coffee break</span>
                    </p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">16:00 - 17:30</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Główna aula 0.410</span>
                    <span class="lang-en hidden">Main hall 0.410</span>
                    </span>
                    <div class="event-title">
                        <span class="lang-pl">Panel Dyskusyjny</span>
                        <span class="lang-en hidden">Discussion Panel</span>
                    </div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl">Temat: W kierunku nowego ekosystemu badań i edukacji w środowisku akademickim</span>
                    <span class="lang-en hidden">Topic: Towards new research and education ecosystem in academia</span>
                    </p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">19:00-22:00</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Sale Muzeum Uniwersytetu Warszawskiego</span>
                    <span class="lang-en hidden">Halls of the University of Warsaw Museum</span>
                    </span>
                    <div class="event-title"> </div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl"><b>Kolacja bankietowa</b></span>
                    <span class="lang-en hidden"><b>Banquet Dinner</b></span>
                    </p>
                </div>
            </div>
        </div>
        <div class="agenda-schedule" id="day2">
            <h3> </h3>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">9:00-10:30</div>
                    <div class="event-title">
                    <span class="lang-pl">Sesje równoległe</span>
                    <span class="lang-en hidden">Parallel sessions</span>
                    </div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl"><b>Nauka i Badania</b></span>
                    <span class="lang-en hidden"><b>Science and Research</b></span>
                    <br><svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Sala: 1.132</span>
                    <span class="lang-en hidden">Room: 1.132</span>
                    </span>
                    <br>
                    <span class="lang-pl">Temat: Przyszłość publikacji naukowych</span>
                    <span class="lang-en hidden">Topic: The Future of Scientific Publishing</span>
                    <br><br>
                    <span class="lang-pl"><b>Dydaktyka</b></span>
                    <span class="lang-en hidden"><b>Didactics</b></span>
                    <br><svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Sala: 1.138</span>
                    <span class="lang-en hidden">Room: 1.138</span>
                    </span>
                    <br>
                    <span class="lang-pl">Temat: Innowacyjne metody nauczania</span>
                    <span class="lang-en hidden">Topic: Innovative teaching methods</span>
                    </p><br>
                    <span class="lang-pl"><b>Praktyki i Wymiana Wiedzy</b></span>
                    <span class="lang-en hidden"><b>Practices and Knowledge Exchange</b></span>
                    <br><svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Sala: 1.128</span>
                    <span class="lang-en hidden">Room: 1.128</span>
                    </span>
                    <br>
                    <span class="lang-pl">Prezentacje sponsorów i praktyków</span>
                    <span class="lang-en hidden">Presentations by Sponsors and Practitioners</span>
                    </p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">10:30 - 11:00</div>
                    <div class="event-title"> </div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl">Przerwa kawowa</span>
                    <span class="lang-en hidden">Coffee break</span>
                    </p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">11:30-12:30</div>
                    <div class="event-title">
                    <span class="lang-pl">Warsztaty</span>
                    <span class="lang-en hidden">Workshops</span>
                    </div>
                </div>
                <div class="event-right">
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Sala: 1.132</span>
                    <span class="lang-en hidden">Room: 1.132</span>
                    </span>
                    <br>
                    <span class="lang-pl">Wykorzystanie AI w nauce</span>
                    <span class="lang-en hidden">Using AI in science</span>
                    <br><br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Sala: 1.138</span>
                    <span class="lang-en hidden">Room: 1.138</span>
                    </span>
                    <br>
                    <span class="lang-pl">Nowe technologie w dydaktyce</span>
                    <span class="lang-en hidden">New technologies in teaching</span>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">12:30-13:30 </div>
                    <div class="event-title"> </div>
                </div>
                <div class="event-right">
                    <p>Lunch</p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">13:30 - 15:00</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Główna aula 0.410</span>
                    <span class="lang-en hidden">Main hall 0.410</span>
                    </span><br>
                    <div class="event-title">
                    <span class="lang-pl">Panel Dyskusyjny</span>
                    <span class="lang-en hidden">Discussion Panel</span>
                    </div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl">Temat: Przyszłość edukacji wyższej</span>
                    <span class="lang-en hidden">Topic: The Future of Higher Education</span>
                    </p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time">15:00 - 15:30</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Główna aula 0.410</span>
                    <span class="lang-en hidden">Main hall 0.410</span>
                    </span><br>
                    <div class="event-title">
                    <span class="lang-pl">Zamknięcie Konferencji</span>
                    <span class="lang-en hidden">Closing of the Conference</span>
                    </div>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl">Podsumowanie i wnioski</span>
                    <span class="lang-en hidden">Summary and Conclusions</span>
                    </p>
                </div>
            </div>
        </div>
    </div>
    <script>
        // Pobierz wszystkie bloki z dniami
        const days = document.querySelectorAll('.agenda-day');
        const schedules = document.querySelectorAll('.agenda-schedule');
        // Funkcja zmieniająca aktywny dzień
        function setActiveDay(dayId) {
            // Usuń klasę 'active' ze wszystkich dni
            days.forEach(day => day.classList.remove('active'));
            // Usuń klasę 'active' ze wszystkich harmonogramów
            schedules.forEach(schedule => schedule.classList.remove('active'));
            // Dodaj klasę 'active' do wybranego dnia i harmonogramu
            document.querySelector(`[data-day="${dayId}"]`).classList.add('active');
            document.getElementById(dayId).classList.add('active');
        }
        // Domyślnie ustaw aktywny "Dzień 1"
        setActiveDay('day1');
        // Dodaj zdarzenie kliknięcia dla każdego dnia
        days.forEach(day => {
            day.addEventListener('click', () => {
                const dayId = day.getAttribute('data-day');
                setActiveDay(dayId);
            });
        });
    </script>
</body>
</html>

<div style="background-color: #f9f9f9; padding: 20px; border-radius: 10px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); margin: 20px 0; font-family: Poppins, sans-serif; font-size: 1em; color: #333; line-height: 1.6;">
    <ul style="list-style-type: disc; margin: 0; padding: 0 20px;">
        <li>
        <span class="lang-pl"><b>Stoiska partnerów:</b></span>
        <span class="lang-en hidden"><b>Partner stands</b></span> 
        <span class="lang-pl">Dostępne przez cały czas trwania konferencji na dziedzińcu australijskim</span>
        <span class="lang-en hidden">Available throughout the conference in the Australian Atrium</span>
        </li>
        <li>
        <span class="lang-pl"><b>Materiały konferencyjne:</b></span>
        <span class="lang-en hidden"><b>Conference materials:</b></span> 
        <span class="lang-pl">Dostępne w formie cyfrowej i drukowanej</span>
        <span class="lang-en hidden">Available in digital and printed formats</span>
        </li>
        <li>
        <span class="lang-pl"><b>Live Streaming na kanale: </b></span>
        <span class="lang-en hidden"><b>Live Streaming on channel: </b></span><a href="https://www.youtube.com/@delab-uw" target="_blank" style="color: #2c84c9; text-decoration: none;">https://www.youtube.com/@delab-uw</a></li>
    </ul>
</div>


<!-- Nawigacja -->
<script>
    document.addEventListener('DOMContentLoaded', () => {
        const headerInner = document.querySelector('.md-header__inner.md-grid');
        if (headerInner) {
            // Tworzenie przycisku Harmonogramu
            const scheduleButton = document.createElement('button');
            scheduleButton.id = 'scheduleButton';
            scheduleButton.className = 'schedule-button';
            scheduleButton.textContent = 'Schedule';

            // Stylizacja przycisku Harmonogramu
            scheduleButton.style.marginRight = '10px';
            scheduleButton.style.backgroundColor = '#f0f0f0';
            scheduleButton.style.color = '#333';
            scheduleButton.style.border = 'none';
            scheduleButton.style.padding = '8px 16px';
            scheduleButton.style.borderRadius = '4px';
            scheduleButton.style.cursor = 'pointer';
            scheduleButton.style.fontSize = '14px';

            // Dodanie funkcji przewijania do przycisku Harmonogramu
            scheduleButton.addEventListener('click', () => {
                const target = document.getElementById('harmonogram');
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });

            // Tworzenie przycisku Lokalizacji
            const locationButton = document.createElement('button');
            locationButton.id = 'locationButton';
            locationButton.className = 'location-button';
            locationButton.textContent = 'Location';

            // Stylizacja przycisku Lokalizacji
            locationButton.style.marginRight = '10px';
            locationButton.style.backgroundColor = '#f0f0f0';
            locationButton.style.color = '#333';
            locationButton.style.border = 'none';
            locationButton.style.padding = '8px 16px';
            locationButton.style.borderRadius = '4px';
            locationButton.style.cursor = 'pointer';
            locationButton.style.fontSize = '14px';

            // Dodanie funkcji przewijania do przycisku Lokalizacji
            locationButton.addEventListener('click', () => {
                const target = document.getElementById('call');
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });

            // Tworzenie przycisku do zmiany języka
            const switchButton = document.createElement('button');
            switchButton.id = 'languageSwitch';
            switchButton.className = 'language-switch';

            // Utwórz ikonę SVG do zmiany języka
            const svgIcon = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
            svgIcon.setAttribute('xmlns', 'http://www.w3.org/2000/svg');
            svgIcon.setAttribute('viewBox', '0 0 24 24');
            svgIcon.setAttribute('height', '20'); // Rozmiar ikony
            svgIcon.setAttribute('width', '20');
            svgIcon.setAttribute('fill', 'white'); // Ustawienie koloru ikony na biały

            const path1 = document.createElementNS('http://www.w3.org/2000/svg', 'path');
            path1.setAttribute(
                'd',
                'M12.87 15.07l-2.54-2.51.03-.03A17.5 17.5 0 0 0 14.07 6H17V4h-7V2H8v2H1v2h11.17C11.5 7.92 10.44 9.75 9 11.35 8.07 10.32 7.3 9.19 6.69 8h-2c.73 1.63 1.73 3.17 2.98 4.56l-5.09 5.02L4 19l5-5 3.11 3.11zM18.5 10h-2L12 22h2l1.12-3h4.75L21 22h2zm-2.62 7 1.62-4.33L19.12 17z'
            );

            svgIcon.appendChild(path1);
            switchButton.appendChild(svgIcon);

            // Stylizacja przycisku zmiany języka
            switchButton.style.marginLeft = 'auto';
            switchButton.style.backgroundColor = '#2c84c9';
            switchButton.style.color = 'white';
            switchButton.style.border = 'none';
            switchButton.style.padding = '8px';
            switchButton.style.borderRadius = '4px';
            switchButton.style.cursor = 'pointer';
            switchButton.style.display = 'flex';
            switchButton.style.alignItems = 'center'; // Wyśrodkowanie ikony

            // Dodanie przycisków do headera
            headerInner.appendChild(scheduleButton); // Dodaj przycisk Harmonogram
            headerInner.appendChild(locationButton); // Dodaj przycisk Lokalizacja
            headerInner.appendChild(switchButton); // Dodaj przycisk zmiany języka

            // Logika przełączania języka
            const polishTexts = document.querySelectorAll('.lang-pl');
            const englishTexts = document.querySelectorAll('.lang-en');
            let isEnglish = true; // Flaga języka

            // Ustaw początkowy stan języka
            polishTexts.forEach(text => text.classList.toggle('hidden', isEnglish));
            englishTexts.forEach(text => text.classList.toggle('hidden', !isEnglish));


            switchButton.addEventListener('click', () => {
                isEnglish = !isEnglish; // Przełącz flagę języka
                polishTexts.forEach(text => text.classList.toggle('hidden', isEnglish));
                englishTexts.forEach(text => text.classList.toggle('hidden', !isEnglish));
                scheduleButton.textContent = isEnglish ? 'Schedule':'Harmonogram'; // Zmień tekst przycisku Harmonogramu
                locationButton.textContent = isEnglish ? 'Location':'Lokalizacja';
            });
        }
    });
</script>


<br><br>

<h1 id="call" style="margin-top: 50px;">
    <span class="lang-pl"><b>Call for papers</b></span>
    <span class="lang-en hidden"><b>Call for papers</b></span></h1>



<br><br>

<h1 id="location" style="margin-top: 50px; margin-bottom:50px;">
    <span class="lang-pl"><b>Szczegóły lokalizacji</b></span>
    <span class="lang-en hidden"><b>Location details</b></span></h1>

<div class="map-container">
    <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d4663.501770262157!2d21.0202136!3d52.2417561!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x471ecc5c1509e0dd%3A0x82c92afcf5ab31!2sFaculty%20of%20Modern%20Languages%20%E2%80%8B%E2%80%8Bat%20the%20University%20of%20Warsaw!5e1!3m2!1sen!2spl!4v1736941097058!5m2!1sen!2spl" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
</div>
