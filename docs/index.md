
<img src="./assets/baner_new.png" alt="delab photo" style="width: 90vw; height: auto; object-fit: cover; display: block; margin: 0; padding: 0; margin-top:-50px;">


<!-- Sekcja lokalizacji -->
<div class="location-container">
        <span class="location-icon">
            <!-- Ikona lokalizacji (np. Font Awesome lub inna) -->
            <svg xmlns="http://www.w3.org/2000/svg" height="45" viewBox="0 0 24 24" width="45" fill="#888888"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
        </span>
        <span class="lang-pl">Uniwersytet Warszawski, ul. Dobra 55</span>
        <span class="lang-en hidden">University of Warsaw, Warsaw, ul. Dobra 55</span>
</div>

<br>

<!-- Nagłówek -->
<h1 class="center-title">
    <span class="lang-pl"><b>Weź udział w konferencji<br> i stań się częścią rewolucji AI <br>w nauce i edukacji!</b></span>
    <span class="lang-en hidden"><b>Join the conference<br> and be part of the AI revolution <br>in science and education!</b></span>
</h1>


<!-- Przycisk rejestracji-->
<div class="info-button-container">
    <!-- Przycisk rejestracji (zablokowany) -->
    <a href="#" class="info-button disabled" onclick="return false;">
        <span class="lang-pl">Zarejestruj się teraz</span>
        <span class="lang-en hidden">Register now</span>
    </a>
    <!-- Przycisk Call for Papers -->
    <button class="info-button" id="callForAbstractsButton">
        <span class="lang-pl">Call for presentations</span>
        <span class="lang-en hidden">Call for presentations</span>
    </button>
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
            font-family: Barlow;
            border-radius: 5px;
            max-width: 600px;
            margin: 20px auto;
        }
        .countdown-title {
            font-size: 1.7em;
            margin-bottom: 10px;
            margin-top: 20px;
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
            color: #034A76; /* Akcent - czerwony */
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
    background-color: #034A76; /* Ciemnoniebieski kolor przycisku */
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
    
<!-- About -->
<div class="about-title">
    <span class="lang-pl"><b>O konferencji GenAI w edukacji wyższej</b></span>
    <span class="lang-en hidden"><b>About the GenAI Conference in Higher Education</b></span>
</div>
    <p class="about-text">
        <span class="lang-pl">Konferencja GenAI łączy naukowców, dydaktyków, praktyków i liderów biznesu, aby wspólnie analizować wpływ technologii AI na transformację edukacji i badań naukowych.<br><br>
        Wydarzenie jest organizowane przez <b>DELab UW</b>, interdyscyplinarne centrum Uniwersytetu Warszawskiego, które<br> łączy środowisko akademickie, biznes i administrację publiczną, aby wspierać innowacje i transformację cyfrową.
        </span>
        <span class="lang-en hidden">The GenAI Conference brings together academic researchers, educators, practitioners, and business leaders to explore how AI technologies are reshaping teaching and research.<br><br>
        This event is organized by <b>DELab UW</b>, an interdisciplinary center at the University of Warsaw, <br>connecting academia, business, and public administration to drive innovation and digital transformation.</span>
    </p>

<!-- Sekcja obszarów tematycznych -->
<div class="topics-container">
        <!-- Obszar tematyczny 1 -->
        <div class="topic">
            <div class="icon-container">
                <i class="fas fa-globe" style="color: #034A76; font-size: 24px;"></i>
            </div>
            <div class="topic-content">
                <h3>
                <span class="lang-pl">Innowacyjne nauczanie</span>
                <span class="lang-en hidden">Innovative teaching</span>
                </h3>
                <p>
                <span class="lang-pl">Jak generatywna AI zmienia sposób nauczania i uczenia się.</span>
                <span class="lang-en hidden">How generative AI <br>is changing the way we teach and learn.</span>
                </p>
            </div>
        </div>
        
<!-- Obszar tematyczny 2 -->
<div class="topic">
            <div class="icon-container">
                <i class="fas fa-microscope" style="color: #034A76; font-size: 24px;"></i>
            </div>
            <div class="topic-content">
                <h3>
                <span class="lang-pl">Nowatorskie badania naukowe</span>
                <span class="lang-en hidden">Pioneering research</span>
                </h3>
                <p>
                <span class="lang-pl">Przełomowe zastosowania AI w nauce i badaniach.</span>
                <span class="lang-en hidden">Groundbreaking applications of AI <br>in science and research.</span>
                </p>
            </div>
</div>

<!-- Obszar tematyczny 3 -->
<div class="topic">
            <div class="icon-container">
                <i class="fas fa-university" style="color: #034A76; font-size: 24px;"></i>
            </div>
            <div class="topic-content">
                <h3>
                <span class="lang-pl">Dobre praktyki</span>
                <span class="lang-en hidden">Best practices</span>
                </h3>
                <p>
                <span class="lang-pl">Inspirujące przykłady wdrożeń technologii na uczelniach.</span>
                <span class="lang-en hidden">Inspiring examples <br>of technology implementations <br>at universities.</span>
                </p>
            </div>
        </div>

<!-- Obszar tematyczny 4 -->
<div class="topic">
            <div class="icon-container">
                <i class="fas fa-handshake" style="color: #034A76; font-size: 24px;"></i>
            </div>
            <div class="topic-content">
                <h3>
                <span class="lang-pl">Portal wiedzy</span>
                <span class="lang-en hidden">Knowledge portal</span>
                </h3>
                <p>
                <span class="lang-pl">Tworzenie platformy wymiany doświadczeń między badaczami, firmami i dydaktykami.</span>
                <span class="lang-en hidden">Creating a platform <br>for the exchange <br>of experiences between researchers, companies and educators.</span>
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
                    <div class="event-title">
                        <span class="lang-pl">Otwarcie konferencji</span>
                        <span class="lang-en hidden">Opening of the conference</span>
                    </div>
                    <div class="event-time">9:00-10:00</div>
                        <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                            <span class="lang-pl">Główna aula 0.410</span>
                            <span class="lang-en hidden">Main hall 0.410</span>
                            </span>
                </div>
                <div class="event-right">
                    <span class="lang-pl">Przemówienia:
                    <ul>
                    <li>JM rektora</li>
                    <li>Przedstawiciela Ministerstwa Edukacji i Nauki</li>
                    <li>Dyrektor DELab UW</li>
                    </ul>
                    </span>
                    <span class="lang-en hidden">Address by:
                    <ul>
                    <li>His Magnificence the Rector</li>
                    <li>The representative of the Ministry <br>of Education and Science</li>
                    <li>The Director of DELab UW</li>
                    </ul>
                    </span>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-title">Keynote Speech</div>
                    <div class="event-time">10:00-11:00</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                            <span class="lang-pl">Główna aula 0.410</span>
                            <span class="lang-en hidden">Main hall 0.410</span>
                        </span>
                </div>
                <div class="event-right">
                    <p>
                    <span class="lang-pl">Temat: Wpływ nowych technologii na edukację i naukę (TBC) - prof. Neil Selwyn</span>
                    <span class="lang-en hidden">Topic: The impact of new technologies on education and science (TBC) - prof. Neil Selwyn</span>
                    </p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-time"><br>11:00-11:30</div>
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
                    <div class="event-title">
                        <span class="lang-pl">Sesje równoległe</span>
                        <span class="lang-en hidden">Parallel sessions</span>
                    </div>
                    <div class="event-time">11:30 - 13:00</div>
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
                    <span class="lang-en hidden"><b>Teaching</b></span>
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
                    <div class="event-time"><br>13:00 - 14:00</div>
                    <div class="event-title"> </div>
                </div>
                <div class="event-right">
                    <p>Lunch</p>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-title">Workshops & Discussions
                    </div>
                    <div class="event-time">14:00 - 15:30</div>
                </div>
                <div class="event-right">
                    <span class="lang-pl"><br><b>Warsztaty</b></span>
                    <span class="lang-en hidden"><br><b>Workshops</b></span>
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
                    <span class="lang-pl">Temat: TBC</span>
                    <span class="lang-en hidden">Topic: TBC</span>
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
                    <div class="event-title">
                        <span class="lang-pl">Panel Dyskusyjny</span>
                        <span class="lang-en hidden">Discussion Panel</span>
                    </div>
                    <div class="event-time">16:00 - 17:30</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Główna aula 0.410</span>
                    <span class="lang-en hidden">Main hall 0.410</span>
                    </span>
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
                    <div class="event-time"><br>19:00-22:00</div>
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
                    <div class="event-title">
                    <span class="lang-pl">Sesje równoległe</span>
                    <span class="lang-en hidden">Parallel sessions</span>
                    </div>
                    <div class="event-time">9:00-10:30</div>
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
                    <span class="lang-en hidden"><b>Teaching</b></span>
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
                    <div class="event-title">
                    <span class="lang-pl">Warsztaty</span>
                    <span class="lang-en hidden">Workshops</span>
                    </div>
                    <div class="event-time">11:30-12:30</div>
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
                    <div class="event-title">
                    <span class="lang-pl">Panel Dyskusyjny</span>
                    <span class="lang-en hidden">Discussion Panel</span>
                    </div>
                    <div class="event-time">13:30 - 15:00</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Główna aula 0.410</span>
                    <span class="lang-en hidden">Main hall 0.410</span>
                    </span><br>
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
                    <div class="event-title">
                    <span class="lang-pl">Zamknięcie Konferencji</span>
                    <span class="lang-en hidden">Closing of the Conference</span>
                    </div>
                    <div class="event-time">15:00 - 15:30</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Główna aula 0.410</span>
                    <span class="lang-en hidden">Main hall 0.410</span>
                    </span><br>
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
        <span class="lang-en hidden"><b>Partner stands:</b></span> 
        <span class="lang-pl">Dostępne przez cały czas trwania konferencji w atrium w miejscu konferencji</span>
        <span class="lang-en hidden">Available throughout the conference in the atrium at the conference venue</span>
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
            scheduleButton.addEventListener('click', (event) => {
                event.stopPropagation(); // Zapobiega propagacji zdarzeń
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
            switchButton.style.backgroundColor = '#034A76';
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
            polishTexts.forEach(text => text.classList.add('hidden'));
            englishTexts.forEach(text => text.classList.remove('hidden'));


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


<!-- Call -->
<h1 id="call" style="margin-top: 50px; color: #034A76">
    <span class="lang-pl"><b>Call for presentations</b></span>
    <span class="lang-en hidden"><b>Call for presentations</b></span></h1>

<div class="about-section">
    
<!-- Nagłówek sekcji -->
<p class="about-text-call">
        <span class="lang-pl">GenAI in Higher Education: New Perspectives for Research and Teaching
        <br>May 29–30, 2025 | University of Warsaw, Poland</span>
        <span class="lang-en hidden">GenAI in Higher Education: New Perspectives for Research and Teaching
        <br>May 29–30, 2025 | University of Warsaw, Poland</span>
</p>

<!-- Sekcja obszarów tematycznych -->
<div class="topics-container">
        <div class="topic">
            <div class="topic-content-class">
                <p>
                <span class="lang-pl">DELab UW, w imieniu Rektora Uniwersytetu Warszawskiego, prof. Alojzego Nowaka, zaprasza naukowców, studentów, pracowników administracyjnych, praktyków oraz liderów biznesu do udziału w interdyscyplinarnej konferencji GenAI in Higher Education: Nowe perspektywy dla badań i nauczania. To wyjątkowe wydarzenie stworzy platformę do współpracy, budowania relacji między badaczami a profesjonalistami, wspólnego tworzenia wiedzy, wymiany doświadczeń oraz rozwijania innowacyjnych pomysłów w tej dynamicznie rozwijającej się dziedzinie.
                </span>
                <span class="lang-en hidden">DELab UW, on behalf of the Rector of the University of Warsaw, prof. Alojzy Nowak, invites academics together with students, administrators, practitioners and business leaders to join the interdisciplinary conference GenAI in Higher Education: New Perspectives<br>for Research and Teaching. This unique event will provide a platform for collaboration, fostering connections between researchers <br>and professionals to co-create knowledge, exchange experiences, and develop innovative ideas in this dynamic field.</span>
                </p>
                <h3 style="margin-top: 40px; margin-bottom:20px; font-weight: bold; color: #034A76;">
                    <span class="lang-pl">Dlaczego warto wziąć udział?</span>
                    <span class="lang-en hidden">Why Attend?</span>
                </h3>
                <p>
                <span class="lang-pl">To wyjątkowe spotkanie naukowców, ekspertów i praktyków zapewnia unikalną przestrzeń do dzielenia się spostrzeżeniami oraz nawiązywania kontaktów w dynamicznie rozwijającej się dziedzinie generatywnej sztucznej inteligencji w środowisku akademickim. Uczestnicy będą mieli okazję:</span> 
                <span class="lang-en hidden">This extraordinary gathering of scholars, experts, and practitioners offers a unique space for sharing insights and networking in the rapidly evolving domain of generative AI in academia. Attendees will have the opportunity to:</span> 
                <div class="lang-pl">
                <ul>
                    <li>Wziąć udział w inspirujących wykładach, w tym w wykładzie otwierającym, który wygłosi <b>profesor Neil Selwyn</b> światowy autorytet w dziedzinie odpowiedzialnego wykorzystania technologii cyfrowych w edukacji.</li>
                    <li>Uczestniczyć w prezentacjach z udziałem liderów technologicznych, sesjach akademickich oraz warsztatach praktycznych, skupionych na zastosowaniach generatywnej AI w edukacji i badaniach.</li>
                    <li>Nawiązywać kontakty i rozwijać nowe współprace w dynamicznie rozwijającej się dziedzinie badań i nauczania, dotyczących wyzwań związanych z wykorzystaniem generatywnej AI w szkolnictwie wyższym.</li>
                </ul>
                </div>
                <div class="lang-en hidden">
                <ul>
                    <li>Engage in thought-provoking keynote speeches, including an opening lecture by <b>Professor Neil Selwyn</b>, a global authority<br> on the responsible use of digital technologies in education.</li>
                    <li>Participate in presentations with technology leaders, academic sessions, and hands-on workshops focused on practical applications of generative AI in education and research.</li>
                    <li>Network and develop new collaborations within the rapidly developing academic field of research and teaching concerning challenges of genAI use in higher education.</li>
                </ul>
                </div>
                <h3 style="margin-top: 40px; margin-bottom:20px; font-weight: bold; color: #034A76;">
                    <span class="lang-pl">Kluczowe obszary tematyczne</span>
                    <span class="lang-en hidden">Key Focus Areas</span>
                </h3>
                <p>
                <span class="lang-pl">Zapraszamy do zgłaszania prezentacji dotyczących pięciu kluczowych obszarów:</span>
                <span class="lang-en hidden">We invite presentations concerning five core areas:</span>
                <div class="lang-pl">
                <ol>
                    <li>Potencjał innowacyjnych badań naukowych wspieranych przez technologie generatywnej AI.</li>
                    <li>Możliwości rozwoju nowoczesnej pedagogiki w szkolnictwie wyższym z wykorzystaniem generatywnej sztucznej inteligencji.</li>
                    <li>Zrównoważone i odpowiedzialne wdrażanie generatywnej AI w środowisku akademickim.</li>
                    <li>Prezentacja narzędzi generatywnej AI dla badań i nauczania.</li>
                    <li>Dzielenie się dobrymi praktykami dotyczącymi skutecznej integracji generatywnej AI w środowisku akademickim.</li>
                </ol>
                </div>
                <div class="lang-en hidden">
                <ol>
                    <li>The potential of innovative scientific research supported by generative AI technologies.</li>
                    <li>Opportunities for developing modern pedagogy in higher education using generative AI.</li>
                    <li>Sustainable and responsible generative AI implementation in academia.</li>
                    <li>Presentation of generative AI tools for research and teaching.</li>
                    <li>Sharing best practices for the effective integration of generative AI in academia.</li>
                </ol>
                </div>
                <br>
                <p>
                <span class="lang-pl"><b>Szczególnie zachęcamy do zgłaszania prezentacji, które odnoszą się do, ale nie ograniczają się do następujących tematów:</b></span>
                <span class="lang-en hidden"><b>We particularly encourage presentations that address, but are not limited to, the following themes:</b></span>
                </p>
                <div class="lang-pl">
                <ul>
                    <li>Nowe podejścia edukacyjne w erze cyfrowej: Innowacje w pedagogice wspierane przez narzędzia cyfrowe i sztuczną inteligencję.</li>
                    <li>Nowe wzorce współpracy w erze cyfrowej: Rola generatywnej AI w przekształcaniu praktyk współpracy.</li>
                    <li>Automatyzacja procesów badawczych: Wykorzystanie AI dla zwiększenia efektywności i innowacyjności metodologii badawczych.</li>
                    <li>Krytyczne podejścia do wdrażania generatywnej AI w szkolnictwie wyższym: Perspektywy etyczne i środowiskowe oraz dyskusja.</li>
                    <li>Integracja nowych narzędzi cyfrowych w procesach nauczania: Praktyczne zastosowania nowoczesnych technologii w środowisku akademickim.</li>
                    <li>Przyszłość szkolnictwa wyższego: Eksploracja transformacji w środowisku akademickim napędzanych postępem cyfrowym.</li>
                    <li>AI w badaniach: Zastosowania generatywnej AI w badaniach akademickich i ich implikacje.</li>
                    <li>Nowe technologie w dydaktyce: Wpływ i możliwości wynikające z wprowadzania nowoczesnych technologii w nauczaniu.</li>
                    <li>W kierunku nowego ekosystemu badań i edukacji w środowisku akademickim: Wizja zintegrowanych ekosystemów edukacyjnych i badawczych w erze AI.</li>
                    <li>EdTech w szkolnictwie wyższym: szanse i wyzwania: Analiza zmieniającego się krajobrazu technologii edukacyjnych.</li>
                </ul>
                </div>
                <div class="lang-en hidden">
                <ul>
                    <li>New Educational Approaches in the Digital Era: Innovations in pedagogy enabled by digital tools and AI.</li>
                    <li>New Patterns of Collaboration in the Digital Era: Generative AI’s role in reshaping collaborative practices.</li>
                    <li>Automation of Research Processes: Leveraging AI for efficiency and innovation in research methodologies.</li>
                    <li>Critical Approaches to the Implementation of Generative AI in Higher Education: Ethical and Environmental perspectives <br>and discussion.</li>
                    <li>Integration of New Digital Tools in Teaching Processes: Practical applications of cutting-edge technology in academia.</li>
                    <li>The Future of Higher Education: Exploring transformations in academia driven by digital advancements.</li>
                    <li>AI in Research: Generative AI applications in academic research and its implications.</li>
                    <li>New Technologies in Teaching: Impact and opportunities of emerging technologies in teaching.</li>
                    <li>Towards a New Research and Education Ecosystem in Academia: Envisioning integrated ecosystems for education and research <br>in the AI era.</li>
                    <li>EdTechs in Higher Education: Opportunities and Challenges: Examining the evolving landscape of educational technologies.</li>
                </ul>
                </div>
                <h3 style="margin-top: 40px; margin-bottom:20px; font-weight: bold; color: #034A76;">
                    <span class="lang-pl">Wytyczne dotyczące zgłoszeń</span>
                    <span class="lang-en hidden">Submission Guidelines</span>
                </h3>
                <p>
                <span class="lang-pl">Proces selekcji prezentacji będzie oparty na przesłanych streszczeniach.</span>
                <span class="lang-en hidden">The selection process for presentations will be based on submitted abstracts.</span>
                </p>
                <div class="lang-pl">
                <ul>
                    <li><b>Długość</b>: Streszczenia powinny zawierać od 150 do 300 słów.</li>
                    <li><b>Zawartość</b>: Należy uwzględnić tytuł, cel badań, główny problem badawczy, pytania/hypotezy badawcze, metodologię, próbę (dane) i/lub wyniki.</li>
                    <li><b>Język</b>: Angielski.</li>
                    <li><b>Platforma</b>: Prześlij swoje streszczenie za pomocą <a href="https://forms.office.com/e/V50Si3feZv" target="_blank">formularza rejestracyjnego</a>.</li>
                </ul>
                </div>
                <div class="lang-en hidden">
                <ul>
                    <li><b>Length</b>: Abstracts should be between 150 and 300 words.</li>
                    <li><b>Content</b>: Include the title, aim of the research, main research problem, research questions/hypotheses, methodology, sample (data), and/or results.</li>
                    <li><b>Language</b>: English.</li>
                    <li><b>Platform</b>: Submit your abstract via <a href="https://forms.office.com/e/V50Si3feZv" target="_blank">registration form</a>.</li>
                </ul>
                </div>
                <h3 style="margin-top: 40px; margin-bottom:20px; font-weight: bold; color: #034A76;">
                    <span class="lang-pl">Ważne daty</span>
                    <span class="lang-en hidden">Important Dates</span>
                </h3>
                <div class="lang-pl">
                <ul>
                    <li><b>Otwarcie zgłoszeń</b>: 17 stycznia 2025</li>
                    <li><b>Termin nadsyłania zgłoszeń</b>: 23 lutego 2025</li>
                    <li><b>Powiadomienie o akceptacji</b>: 3 marca 2025</li>
                </ul>
                </div>
                <div class="lang-en hidden">
                <ul>
                    <li><b>Opening of Submissions</b>: January 17, 2025.</li>
                    <li><b>Submission Deadline</b>: February 23, 2025</li>
                    <li><b>Notification of Acceptance</b>: March 3, 2025</li>
                </ul>
                </div>
                <h3 style="margin-top: 40px; margin-bottom:20px; font-weight: bold; color: #034A76;">
                    <span class="lang-pl">Opłata konferencyjna</span>
                    <span class="lang-en hidden">Conference Fee</span>
                </h3>
                <span class="lang-pl"><b>360 EUR</b> (obejmuje dostęp do wszystkich sesji, warsztatów i materiałów, obiady i przerwy kawowe).</span>
                <span class="lang-en hidden"><b>360 EUR</b> (includes access to all sessions, workshops, and materials, lunches and coffee breaks).</span>
                <h3 style="margin-top: 40px; margin-bottom:20px; font-weight: bold; color: ##034A76;">
                    <span class="lang-pl">Dołącz do nas!</span>
                    <span class="lang-en hidden">Join Us!</span>
                </h3>
                <span class="lang-pl">Ta konferencja wykracza poza granice tradycyjnego wydarzenia akademickiego, stając się dynamicznym forum intelektualnej współpracy, krytycznego dialogu i wizjonerskiej inspiracji. Wspólnie dążymy do zdefiniowania przyszłości szkolnictwa wyższego i badań naukowych w transformacyjnej erze generatywnej sztucznej inteligencji.</span><br>
                <span class="lang-en hidden">This conference transcends the boundaries of a conventional academic event, serving as a dynamic forum for intellectual collaboration, critical dialogue, and visionary inspiration. Together, we aim to redefine the future of higher education and research in the transformative era of generative AI.</span><br>
                <span class="lang-pl">W przypadku pytań lub chęci uzyskania dodatkowych informacji prosimy o kontakt pod adresem: <b>genai.conf@delab.uw.edu.pl</b></span><br>
                <span class="lang-en hidden">For inquiries or additional information, please contact us at: <b>genai.conf@delab.uw.edu.pl</b> </span><br>
                <span class="lang-pl">Czekamy na Państwa propozycje i mamy nadzieję, że powitamy Państwa w Warszawie!</span><br>
                <span class="lang-en hidden">We look forward to your contributions and to welcoming you to Warsaw!</span><br>
            </div>
        </div>
    </div>    
</div>


<br><br>

<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">

<div class="about-section">

<h1 id="location" style="margin-bottom:10px;">
    <span class="lang-pl"><b>Szczegóły lokalizacji</b></span>
    <span class="lang-en hidden"><b>Location details</b></span></h1>

<div class="about-section">
<!-- Nagłówek sekcji -->
<div class="topic-content-class">
    <div class="topic">
    <p>
        <span class="lang-pl">Konferencja odbędzie się na Uniwersytecie Warszawskim, przy ul. Dobrej 55 w Warszawie. Nowoczesny budynek zapewnia doskonałe warunki i jest dogodnie zlokalizowany w pobliżu centrum miasta, co sprawia, że jest łatwo dostępny komunikacją miejską.
        <br><br>
        Zachęcamy do sprawdzenia pobliskich hoteli na czas pobytu. Polecamy nocleg w <a href="https://maps.app.goo.gl/8Dp4BtXQNdQULk8S9" target="_blank">Motel One Warsaw-Chopin</a>, który znajduje się w pobliżu miejsca konferencji.</span>
        <span class="lang-en hidden">The conference will take place at the University of Warsaw, located at ul. Dobra 55, Warsaw. This modern venue offers excellent facilities and is conveniently situated near the city center, making it easily accessible by public transportation.
        <br><br>We recommend checking nearby hotels for your stay. Our suggested accommodation is <a href="https://maps.app.goo.gl/8Dp4BtXQNdQULk8S9" target="_blank">Motel One Warsaw-Chopin</a>, which <br>is located within close proximity to the conference venue.</span>
    </p>
    </div>
</div>

<br>

<div class="map-container">
    <!-- Mapka -->
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2443.0606552367494!2d21.023453166131585!3d52.24228192515387!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x471ecde67488c39f%3A0xf68db960a58fd4eb!2sDobra%2055%2C%2000-312%20Warszawa!5e0!3m2!1sen!2spl!4v1737108036372!5m2!1sen!2spl" width="800" height="600" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
</div>


<script>
document.addEventListener('DOMContentLoaded', () => {
    // Funkcja przewijania do sekcji
    const callForAbstractsButton = document.getElementById('callForAbstractsButton');
    callForAbstractsButton.addEventListener('click', () => {
        const target = document.getElementById('call'); // Identyfikator sekcji Call for abstracts
        if (target) {
            target.scrollIntoView({ behavior: 'smooth' }); // Płynne przewijanie do sekcji
        }
    });
});
</script>