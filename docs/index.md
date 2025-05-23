
<img src="./assets/baner_new.png" alt="delab photo" style="width: 90vw; height: auto; object-fit: cover; display: block; margin: 0; padding: 0; margin-top:-50px;">

<!-- LOGO pod banerem -->
<div class="logo-container">
    <img src="./assets/logo_FA.png" alt="Additional Logo">
</div>

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

<div class="banner-background">
  <h1 class="center-title1">
    <span class="lang-pl"><b>Weź udział w konferencji<br> i stań się częścią rewolucji AI <br>w nauce i edukacji!</b></span>
    <span class="lang-en hidden"><b>Join the conference<br> and be part of the AI revolution <br>in science and education!</b></span>
  </h1>
</div>


<!-- Przycisk rejestracji-->
<div class="info-button-container">
    <!-- Przycisk rejestracji (zablokowany) -->
    <a href="https://forms.office.com/e/V50Si3feZv" class="info-button disabled">
        <span class="lang-pl">Zarejestruj się teraz</span>
        <span class="lang-en hidden">Register now</span>
    </a>
    <!-- Przycisk Call for Papers -->
    <button class="info-button" id="callForAbstractsButton">
        <span class="lang-pl">Call for presentations</span>
        <span class="lang-en hidden">Call for presentations</span>
    </button>
    <p style="color: #808080; font-size: 0.9em; font-style: italic;">
    * Click ‘Register Now’ to sign up as a passive participant (attending the conference without giving a presentation)
    </p>
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
            font-family: Open Sans;
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
            <span class="lang-pl">Do rozpoczęcia konferencji zostało:</span>
            <span class="lang-en hidden">Countdown to the start of the conference:</span>
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
            const eventDate = new Date("May 29, 2025 23:59:59").getTime();
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
        This event is organized by <b>DELab UW</b>, an interdisciplinary center at the University of Warsaw, <br>connecting academia, business, and public administration to drive innovation and digital transformation.<br></span>
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
    <div class="lang-pl" style="text-align: left; margin-top: 15px;">
    <br>
        <b>Dyskusje będą się toczyć w dwóch równoległych ścieżkach:</b><br>
        <br>
        <b>Ścieżka dla społeczności UW</b> – rozpocznie się 29 maja o godz. 11:30 panelem, podczas którego przedstawione zostaną postulaty studenckie opracowane dzień wcześniej. Debaty w tej części konferencji skupią się na przyszłości uczelni, strategiach rozwoju edukacji wyższej oraz praktycznych wyzwaniach związanych z wdrażaniem technologii AI na Uniwersytecie Warszawskim.<br>
        <br>
        <b>Ścieżka naukowa (międzynarodowa)</b> – skierowana do badaczy i dydaktyków z całego świata. Podczas dwóch dni konferencji prezentowane będą najnowsze wyniki badań i projektów dotyczących wykorzystania generatywnej AI w edukacji i nauce. Wśród zaproszonych gości znajdzie się m.in. prof. Peter Kahn z University of Manchester oraz wielu innych cenionych specjalistów.<br>
        <br>
Serdecznie zapraszamy wszystkich członków społeczności akademickiej Uniwersytetu Warszawskiego do aktywnego udziału w konferencji. Wspólnie zastanówmy się, czym powinna być dziś uniwersytecka edukacja – otwarta na wyzwania technologiczne, odpowiedzialna społecznie i zakorzeniona w wartościach akademickich. 
</div>
    <div class="lang-en hidden" style="text-align: left; margin-top: 15px;">
  <br>
  <b>Discussions will take place along two parallel tracks:</b><br><br>

  <b>University of Warsaw Community Track</b> – this track will begin on May 29 at 11:30 AM with a panel presenting student proposals developed the previous day. The debates in this part of the conference will focus on the future of the university, strategies for the development of higher education, and practical challenges related to implementing AI technologies at the University of Warsaw.<br><br>

  <b>Scientific Track (International)</b> – dedicated to researchers and educators from around the world. Over the course of two days, the latest research findings and projects on the use of generative AI in education and science will be presented. Among the invited speakers is Prof. Peter Kahn from the University of Manchester, along with many other distinguished experts.<br><br>

  We warmly invite all members of the University of Warsaw academic community to actively participate in the conference. Let us reflect together on what university education should be today – open to technological challenges, socially responsible, and rooted in academic values.
</div>
</div>

<br>



<!-- Agenda -->

<h1 id="harmonogram" style="margin-top: 50px; font-weight: bold; font-size: 30px; margin-left: 10px;">
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
          <div class="agenda-day" data-day="pre-day">
                <span class="day-title">
                    <span class="lang-pl">Pre Day</span>
                    <span class="lang-en hidden">Pre Day</span>
                </span><br>
                <span class="day-subtitle">
                    <span class="lang-pl">środa 28.05</span>
                    <span class="lang-en hidden">Wednesday 28.05</span>
                </span>
            </div>
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
                    <li>Przedstawiciela Ministerstwa Nauki i Szkolnictwa Wyższego</li>
                    <li>Dyrektor DELab UW</li>
                    </ul>
                    </span>
                    <span class="lang-en hidden">Address by:
                    <ul>
                    <li>His Magnificence the Rector</li>
                    <li>The representative of the Ministry <br>of Science and Higher Education</li>
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
                    <button onclick="openModal('panelModal2')" style="all: unset; cursor: pointer;display: inline-flex;align-items: center;justify-content: center;border-radius: 6px;padding: 6px 12px;font-size: 16px;color: #404040;background-color: #f0f0f0;transition: background-color 0.3s, box-shadow 0.3s;margin-top: 1px; margin-right: 20px; margin-bottom: -10px;" onmouseover="this.style.backgroundColor='#bacde6'; this.style.boxShadow='0 2px 6px rgba(0,0,0,0.1)'"onmouseout="this.style.backgroundColor='#f0f0f0'; this.style.boxShadow='none'" onmouseout="this.style.backgroundColor='#f7f7f7'; this.style.boxShadow='none'">
                    <span class="lang-pl">
                    <b><i>GenAI in Higher Education – some things we need to talk about</i> - prof. Neil Selwyn</b>
                    </span>
                    <span class="lang-en hidden">
                    <b><i>GenAI in Higher Education – some things we need to talk about</i> - prof. Neil Selwyn</b>
                    </span>
                    </button>
                    <p style="color: #808080; font-size: 0.7em; font-style: italic; margin-top: 1px;">* Click for more information</p>
                    <!-- MODAL -->
                <div id="panelModal2" class="modal" style="display:none; position:fixed; z-index:1000; left:0; top:0; width:100%; height:100%; background-color:rgba(0,0,0,0.6);">
                <div class="modal-content" style="background:#fff; margin:10% auto; padding:20px; max-width:600px; border-radius:8px; position:relative;">
                <span class="close-modal" onclick="closeModal('panelModal2')" style="position:absolute; top:10px; right:20px; font-size:24px; cursor:pointer;">&times;</span>
                  <h3>
                  <span class="lang-en hidden"><b><i>GenAI in Higher Education – some things we need to talk about</i></b></span>
                  </h3>
                  <p>
                  <span class="lang-en hidden">With the hype around genAI now beginning to settle down, Neil Selwyn points to some longer-term questions that need to be discussed as genAI capabilities are now being baked into various aspects of higher education practice. What forms of genAI are now taking hold in universities, and with what consequences? How do genAI logics and values fit with established educational and scholarly expectations, and how are tensions being resolved? Is there a moral case for universities resisting and rejecting genAI completely … or is it possible to think otherwise about alternate forms of genAI that higher education might want and genuinely benefit from?
                  </span>
                  </p>
                </div>
                </div>
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
                        <span class="lang-pl">Debate</span>
                        <span class="lang-en hidden">Debate</span>
                    </div>
                    <div class="event-time">11:30-13:00</div>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                            <span class="lang-pl">Główna aula 0.410</span>
                            <span class="lang-en hidden">Main hall 0.410</span>
                        </span>
                </div>
                <div class="event-right">
                    <p>
                    <button onclick="openModal('panelModal3')" style="all: unset; cursor: pointer;display: inline-flex;align-items: center;justify-content: center;border-radius: 6px;padding: 6px 12px;font-size: 16px;color: #404040;background-color: #f0f0f0;transition: background-color 0.3s, box-shadow 0.3s;margin-top: 1px; margin-right: 0px; margin-bottom: -10px;" onmouseover="this.style.backgroundColor='#bacde6'; this.style.boxShadow='0 2px 6px rgba(0,0,0,0.1)'"onmouseout="this.style.backgroundColor='#f0f0f0'; this.style.boxShadow='none'" onmouseout="this.style.backgroundColor='#f7f7f7'; this.style.boxShadow='none'">
                    <span class="lang-pl">
                    <b><i>The Fix or the Break: GenAI in Higher Education</i></b>
                    </span>
                    <span class="lang-en hidden">
                    <b><i>The Fix or the Break: GenAI in Higher Education</i></b>
                    </span>
                    </button>
                    <p style="color: #808080; font-size: 0.7em; font-style: italic; margin-top: 1px;">* Click for more information</p>
                    <!-- MODAL -->
                <div id="panelModal3" class="modal" style="display:none; position:fixed; z-index:1000; left:0; top:0; width:100%; height:100%; background-color:rgba(0,0,0,0.6);">
                <div class="modal-content" style="background:#fff; margin:10% auto; padding:20px; max-width:600px; border-radius:8px; position:relative;">
                <span class="close-modal" onclick="closeModal('panelModal3')" style="position:absolute; top:10px; right:20px; font-size:24px; cursor:pointer;">&times;</span>
                    <h3>
                    <span class="lang-en hidden"><b>Debate: <i>The Fix or the Break: GenAI in Higher Education</i></b></span>
                    </h3>
                  <span class="lang-en hidden"><b>Moderated by:</b> Prof. Renata Włoch (University of Warsaw)</span>
                  <p>
                  <b>Panelists:</b>
                  <ul>
                  <li>Prof. Neil Selwyn (Monash University)</li>
                  <li>Prof. Peter Kahn (University of Manchester)</li>
                  <li>Prof. Zygmunt Lalak (Vice-Rector for Research, University of Warsaw)</li>
                  </ul>
                  <br>
                  <b>Description:</b><br>This high-level debate brings together leading voices to reflect on the promises and risks of generative artificial intelligence in higher education. As universities worldwide begin to explore the use of GenAI tools in teaching, learning and research, the question arises:<i>Will AI fix what is broken in the university – or will it break what still works?</i>
                  <br>
                  The panel will juxtapose two contrasting yet complementary perspectives.<br> Prof. <b>Neil Selwyn</b>, one of the world’s most recognized critical scholars of educational technology, will challenge assumptions about the optimistic rhetoric surrounding GenAI, emphasizing the social, pedagogical and political consequences of unreflective adoption. On the other hand, Prof. <b>Peter Kahn</b> will offer a vision of constructive integration, where GenAI functions as a learning assistant and mentor, enhancing individual agency, flexibility and pedagogical responsiveness.
                  <br>Joining the conversation,<b> Vice-Rector Zygmunt Lalak </b>will bring the institutional and leadership perspective of the University of Warsaw, reflecting on the challenges of aligning innovation with academic identity, educational values, and regulatory frameworks.
                  <br>
                  The debate will address key strategic questions:<br>
                  <ul>
                  <li>What kind of university do we want in the age of GenAI?</li>
                  <li>How can institutions balance experimentation with responsibility?</li>
                  <li>What does it take to become a learning organisation in a time of rapid technological change?</li>
                  <li>What role should academic communities play in defining boundaries, values and purposes for AI in education?</li>
                  <br>
                  As part of the GenAI in Higher Education conference – the first of its kind in Poland – this panel sets out to create a critical and open space for dialogue, where no single narrative dominates, and where the future of the university is not only imagined, but actively negotiated.
                  </p>
                </div>
                </div>
                    <br>
                    </p>
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
                    <div class="event-title">
                        <span class="lang-pl"></span>
                        <span class="lang-en hidden"></span>
                    </div>
                    <div class="event-time">14:00 - 15:30</div>
                </div>
                <div class="event-right" style="display: flex; flex-wrap: wrap; gap: 20px;">
                <div class="track-title">
                  <!-- POLSKI -->
                  <span class="lang-pl"><b>Ścieżka dla społeczności UW</b></span>
                  <!-- ANGIELSKI -->
                  <span class="lang-en hidden"><b>UW community track</b></span>
                  </div>
                  <div class="event-topics" style="flex: 1 1 50%; min-width: 100px;">
                    <p>
                    <button onclick="openModal('panelModal')" style="all: unset; cursor: pointer;display: inline-flex;align-items: center;justify-content: center;border-radius: 6px;padding: 6px 12px;font-size: 16px;color: #404040;background-color: #f0f0f0;transition: background-color 0.3s, box-shadow 0.3s;margin-top: 1px; margin-right: 20px; margin-bottom: -10px;" onmouseover="this.style.backgroundColor='#bacde6'; this.style.boxShadow='0 2px 6px rgba(0,0,0,0.1)'"onmouseout="this.style.backgroundColor='#f0f0f0'; this.style.boxShadow='none'" onmouseout="this.style.backgroundColor='#f7f7f7'; this.style.boxShadow='none'">
                    <span class="lang-pl">
                    <b>Debata: <i>Jakiej uczelni chcemy w obliczu rozwoju AI?</i></b>
                    </span>
                    <span class="lang-en hidden">
                    <b>Debate: <i>Jakiej uczelni chcemy w obliczu rozwoju AI?</i></b>
                    </span>
                    </button>
                    <p style="color: #808080; font-size: 0.7em; font-style: italic; margin-top: 1px; margin-bottom: 10px;">* Click for more information</p>
                    <br>
                     <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
                    <span>
                    <span class="lang-pl">Główna aula 0.410</span>
                    <span class="lang-en hidden">Main hall 0.410</span>
                    </span>
                    <br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#8B0000"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm1 15h-2v-6h2v6zm0-8h-2V7h2v2z"/></svg>
                    <span class="lang-pl">Panel będzie prowadzony w języku <b>polskim</b>. <br>Nie przewidujemy tłumaczenia symultanicznego.</span>
                    <span class="lang-en hidden">Please note: the discussion<br> will be conducted in <b>Polish</b>. <br>No simultaneous translation<br> will be provided.</span>
                    <br><br>
                    </p>
                    </div>
                  </div>
                  <!-- MODAL -->
                <div id="panelModal" class="modal" style="display:none; position:fixed; z-index:1000; left:0; top:0; width:100%; height:100%; background-color:rgba(0,0,0,0.6);">
                <div class="modal-content" style="background:#fff; margin:10% auto; padding:20px; max-width:600px; border-radius:8px; position:relative;">
                <span class="close-modal" onclick="closeModal('panelModal')" style="position:absolute; top:10px; right:20px; font-size:24px; cursor:pointer;">&times;</span>
              <h3>
                <span class="lang-en hidden"><b>Debata: <i>Jakiej uczelni chcemy w obliczu rozwoju AI?</i></b></span>
              </h3>
            <p>
              <span class="lang-en hidden">
              <span class="lang-en hidden"><b>Uczestnicy:</b></span>
              <ul>
              <b>Prowadzi:</b> Dr hab. Katarzyna Śledziewska, prof. UW </li>
              <li>prof. dr hab. Ewa Krogulec </li>
              <li>prof. Anna Giza-Poleszczuk </li>
              <li>prof. Janusz Uriasz - Przewodniczący PKA</li>
              </ul>
              <h3>
              <span class="lang-en hidden"><b>Cel:</b></span>
              </h3> Otwarcie strategicznej debaty o przyszłości uczelni – nie tylko w kontekście technologii, ale przede wszystkim w kontekście misji uczelni, wartości, tożsamości oraz roli społecznej i gospodarczej.
              <br><br>
              <h3>
              <span class="lang-en hidden"><b>Opis:</b></span>
              </h3> W dobie dynamicznego rozwoju sztucznej inteligencji, pytanie „jakiej uczelni chcemy?” staje się jednym z najważniejszych wyzwań dla systemu szkolnictwa wyższego. Czy uczelnie powinny jedynie adaptować się do zmian technologicznych, czy aktywnie je współkształtować? Na czym powinna się opierać ich misja w świecie, w którym wiedza staje się natychmiast dostępna, a kompetencje zmieniają się szybciej niż programy kształcenia?
              <br>
              <br>
              Debata otworzy refleksję nad tym:<br>
              <ul>
              <li>Jak zmieni się misja edukacyjna uczelni w ciągu 10 lat? </li>
              <li>Jaką funkcję społeczną i kulturową mają dziś pełnić uczelnie?</li>
              <li>Na jakich wartościach powinna być oparta ich tożsamość w erze generatywnej AI?</li>
              <li>Czego powinniśmy bronić, a co powinniśmy odważnie zmieniać?</li>
              <li>Czy uczelnie powinny pozostać strażnikami akademickiej autonomii, czy stać się liderami cyfrowych przemian?</li>
              </ul>
              </span>
            </p>
          </div>
        </div>
                <div class="event-right" style="display: flex; flex-wrap: wrap; gap: 20px; margin-top: 5px;">
                <div class="event-heading">
                <span class="lang-pl">
                <b>Ścieżka naukowa (międzynarodowa)</b></span>
                <span class="lang-en hidden">
                <b>Scientific track (international)</b></span>
                </div>
                <span class="lang-pl"><b>Warsztaty i dyskusje</b></span>
                    <span class="lang-en hidden"><b>Workshops & Discussions</b></span>
                <div class="event-topics" style="flex: 1 1 50%; min-width: 300px;">
                    <p>
                    <span class="lang-pl"><b>Warsztaty: Nauka i Badania</b></span>
                    <span class="lang-en hidden"><b>Workshop: Science and Research</b></span>
                    <br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                            <span class="lang-pl">Sala: 1.132</span>
                            <span class="lang-en hidden">Room: 1.132</span>
                        </span>
                        <br>
                        <span class="lang-pl">Temat: Automatyzacja procesów badawczych</span>
                        <span class="lang-en hidden">Topic: Automation of research processes</span>
                        <br>
                    <br>
                    <span class="lang-pl"><b>Warsztaty: Dydaktyka</b></span>
                    <span class="lang-en hidden"><b>Workshop: Teaching</b></span>
                    <br><svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                        <span class="lang-pl">Sala: 1.138</span>
                        <span class="lang-en hidden">Room: 1.138</span>
                        </span>
                        <br>
                        <span class="lang-pl">Temat: Włączanie nowych narzędzi cyfrowych w procesy dydaktyczne</span>
                        <span class="lang-en hidden">Topic: Incorporating new digital tools into teaching processes</span>
                    <br>
                    <br>
                    <span class="lang-pl"><b>Dyskusja: Otoczenie uczelni</b></span>
                    <span class="lang-en hidden"><b>Discussion: University ecosystem</b></span>
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
                    </div>
                    <div class="event-time">16:00 - 17:00</div>
                </div>
                <div class="event-right" style="display: flex; flex-wrap: wrap; gap: 20px;">
                <div class="track-title">
                  <!-- POLSKI -->
                  <span class="lang-pl"><b>Ścieżka dla społeczności UW</b></span>
                  <!-- ANGIELSKI -->
                  <span class="lang-en hidden"><b>UW community track</b></span>
                  </div>
                    <div class="event-topics" style="flex: 1 1 50%; min-width: 300px;">
                    <p>
                    <button onclick="openModal('panelModal1')" style="all: unset; cursor: pointer;display: inline-flex;align-items: center;justify-content: center;border-radius: 6px;padding: 6px 12px;font-size: 16px;color: #404040;background-color: #f0f0f0;transition: background-color 0.3s, box-shadow 0.3s;margin-top: 1px; margin-right: 20px; margin-bottom: -10px;" onmouseover="this.style.backgroundColor='#bacde6'; this.style.boxShadow='0 2px 6px rgba(0,0,0,0.1)'"onmouseout="this.style.backgroundColor='#f0f0f0'; this.style.boxShadow='none'" onmouseout="this.style.backgroundColor='#f7f7f7'; this.style.boxShadow='none'">
                    <span class="lang-pl">
                    <b>Debata: <i>Jakiej strategii potrzebują uczelnie w dobie AI? Od wizji do działania</i></b>
                    </span>
                    <span class="lang-en hidden">
                    <b>Debate: <i>Jakiej strategii potrzebują uczelnie w dobie AI? Od wizji do działania</i></b>
                    </span>
                    </button>
                    <p style="color: #808080; font-size: 0.7em; font-style: italic; margin-top: 1px; margin-bottom: 10px;">* Click for more information</p>
                    <br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
                        <span>
                            <span class="lang-pl">Główna aula 0.410</span>
                            <span class="lang-en hidden">Main hall 0.410</span>
                        </span>
                        <br>
                        <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#8B0000"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm1 15h-2v-6h2v6zm0-8h-2V7h2v2z"/></svg>
                        <span class="lang-en hidden">Please note: the discussion<br> will be conducted in <b>Polish</b>. <br>No simultaneous translation<br> will be provided.</span>
                        <br>
                    </p>
                    </div>
                </div>
                <!-- MODAL -->
                <div id="panelModal1" class="modal" style="display:none; position:fixed; z-index:1000; left:0; top:0; width:100%; height:100%; background-color:rgba(0,0,0,0.6);">
                <div class="modal-content" style="background:#fff; margin:10% auto; padding:20px; max-width:600px; border-radius:8px; position:relative;">
                <span class="close-modal" onclick="closeModal('panelModal1')" style="position:absolute; top:10px; right:20px; font-size:24px; cursor:pointer;">&times;</span>
              <h3>
                <span class="lang-en hidden"><b>Debata: <i>Jakiej strategii potrzebują uczelnie w dobie AI? Od wizji do działania</i></b></span>
              </h3>
            <p>
            <span class="lang-en hidden"><b>Uczestnicy:</b></span>
              <span class="lang-en hidden">
              <ul>
              <b>Prowadzi:</b> dr hab. Magdalena Słok-Wódkowska, prof. UW, Kierowniczka Pracowni Regulacyjnej DELab, Pełnomocniczka ds. równości WPiA </li>
              <li>prof. Ewa Krogulec, Prorektor ds. rozwoju UW </li>
              <li>Robert Grey - kanclerz UW </li>
              <li>dr Zuzanna Hazubska - Pełnomocniczka Ministra ds. spójności polityki naukowej państwa, MNiSW</li>
              <li>Dr Elżbieta Jaskulska, KJD Wydziału Archeologii, URK</li>
              </ul>
              <h3>
              <span class="lang-en hidden"><b>Cel:</b></span>
              </h3> Przedyskutowanie konkretnych kierunków i narzędzi strategicznych, które pozwolą uczelniom – w szczególności Uniwersytetowi Warszawskiemu – skutecznie odpowiedzieć na wyzwania i możliwości związane z AI.
              <br><br>
              <h3>
              <span class="lang-en hidden"><b>Opis:</b></span>
              </h3> Jak przełożyć wizję nowoczesnej uczelni na konkretne działania? Ta debata skupi się na realnych możliwościach wdrażania strategii rozwoju w kontekście barier instytucjonalnych, konieczności współpracy międzysektorowej i wyzwań organizacyjnych.
              <br>
              <br>
              Dyskusja obejmie m.in.:<br>
              <ul>
              <li>Jak pogodzić tempo zmian technologicznych z tempem zmian instytucjonalnych? </li>
              <li>Co jest realnie możliwe do wdrożenia na Uniwersytecie Warszawskim i innych uczelniach w najbliższych latach?</li>
              <li>Czy i na jakich warunkach warto wchodzić we współpracę z big techami?</li>
              <li>Jak tworzyć strategie, które uwzględniają różnorodność wydziałów, potrzeb i poziomów cyfryzacji?</li>
              </ul>
              </span>
            </p>
          </div>
        </div>
                <div class="event-right" style="display: flex; flex-wrap: wrap; gap: 20px; margin-top: 5px;">
                <div class="event-heading">
                <span class="lang-pl">
                <b>Ścieżka naukowa (międzynarodowa)</b></span>
                <span class="lang-en hidden">
                <b>Scientific track (international)</b></span>
                </div>
                <span class="lang-pl"></span>
                    <span class="lang-en hidden"></span>
                <div class="event-topics" style="flex: 1 1 50%; min-width: 300px;">
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
                        <span class="lang-pl">Temat: Automatyzacja procesów badawczych</span>
                        <span class="lang-en hidden">Topic: Automation of research processes</span>
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
                        <span class="lang-pl">Temat: Włączanie nowych narzędzi cyfrowych w procesy dydaktyczne</span>
                        <span class="lang-en hidden">Topic: Incorporating new digital tools into teaching processes</span>
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
                    <br>
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
                    <span class="lang-pl"><b>Teoria AI</b></span>
                    <span class="lang-en hidden"><b>AI Theory</b></span>
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
                    <span class="lang-en hidden">Sponsor and practitioner presentations</span>
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
                    <div class="event-time">11:00-12:30</div>
                </div>
                <div class="event-right">
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Sala: 1.132</span>
                    <span class="lang-en hidden">Room: 1.132</span>
                    </span>
                    <br>
                    <span class="lang-pl"><b>Wykorzystanie AI w nauce</b></span>
                    <span class="lang-en hidden"><b>Using AI in science</b></span>
                    <br><br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Sala: 1.138</span>
                    <span class="lang-en hidden">Room: 1.138</span>
                    </span>
                    <br>
                    <span class="lang-pl"><b>Nowe technologie w dydaktyce</b></span>
                    <span class="lang-en hidden"><b>New technologies in teaching</b></span>
                    <br><br>
                    <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                    <span>
                    <span class="lang-pl">Sala: 1.128</span>
                    <span class="lang-en hidden">Room: 1.128</span>
                    </span>
                    <br>
                    <span class="lang-pl"><b>Praktyki i Wymiana Wiedzy</b></span>
                    <span class="lang-en hidden"><b>Practices and Knowledge Exchange</b></span>
                </div>
            </div>
            <div class="event">
                <div class="event-left">
                    <div class="event-title">
                    <span class="lang-pl">Zamknięcie Konferencji</span>
                    <span class="lang-en hidden">Closing of the Conference</span>
                    </div>
                    <div class="event-time">12:30 - 13:30</div>
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
    <div class="agenda-schedule active" id="pre-day">
    <h3> </h3>
            <div class="event">
                <div class="event-left">
                    <div class="event-title">
                        <span class="lang-pl">Spotkanie ze studentami</span>
                        <span class="lang-en hidden">“Student hearing”</span>
                    </div>
                    <div class="event-time"></div>
                        <svg xmlns="http://www.w3.org/2000/svg" height="16" viewBox="0 0 24 24" width="16" fill="#bbb" style="vertical-align: middle; margin-right: 5px;"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"></path></svg>
                        <span>
                            <span class="lang-pl">ul. Karowa 18 - Wydział Socjologii UW</span>
                            <span class="lang-en hidden">ul. Karowa 18 - Faculty of Sociology</span>
                            </span>
                </div>
                <div class="event-right">
                    <span class="lang-pl">Wydarzenie rozpocznie się 28 maja od wyjątkowego „wysłuchania studenckiego”, prowadzonego przez prof. Annę Gizę-Poleszczuk. Będzie to przestrzeń, w której studenci podzielą się swoimi doświadczeniami, wątpliwościami i propozycjami dotyczącymi roli AI w edukacji. Wnioski ze spotkania zostaną przedstawione władzom uczelni i staną się punktem wyjścia do dalszych debat.
                    </span>
                    <span class="lang-en hidden">The event will begin on May 28 with a unique “student hearing”, led by Professor Anna Giza-Poleszczuk. This will be a space where students can share their experiences, concerns, and proposals regarding the role of AI in education. The conclusions from the meeting will be presented to the university authorities and will serve as a starting point for further debates.
                    </span>
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

<div style="background-color: #f9f9f9; padding: 20px; border-radius: 10px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); margin: 20px 0; font-family: Open Sans; font-size: 1em; color: #333; line-height: 1.6;">
    <ul style="list-style-type: disc; margin: 0; padding: 0 20px;">
        <li>
        <span class="lang-pl"><b>Stoiska partnerów:</b></span>
        <span class="lang-en hidden"><b>Partner stands:</b></span> 
        <span class="lang-pl">Dostępne przez cały czas trwania konferencji w atrium w miejscu konferencji</span>
        <span class="lang-en hidden">Available throughout the conference in the atrium at the conference venue</span>
        </li>
        <li>
        <span class="lang-pl"><b>Rejestracja:</b></span>
        <span class="lang-en hidden"><b>Registration:</b></span> 
        <span class="lang-pl">Przy wejściu do głównej sali</span>
        <span class="lang-en hidden">At the entrance to the main hall</span>
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
<script>
  function openModal(id) {
    document.getElementById(id).style.display = 'block';
  }
  function closeModal(id) {
    document.getElementById(id).style.display = 'none';
  }
  window.onclick = function(event) {
    const modals = document.querySelectorAll('.modal');
    modals.forEach(modal => {
      if (event.target === modal) {
        modal.style.display = "none";
      }
    });
  };
</script>

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
            scheduleButton.style.backgroundColor = '#bacde6';
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

            // Tworzenie przycisku Prelegentów
            const speakersButton = document.createElement('button');
            speakersButton.id = 'speakersButton';
            speakersButton.className = 'speakers-button';
            speakersButton.textContent = 'Speakers';

            // Stylizacja przycisku Prelegentów
            speakersButton.style.marginRight = '10px';
            speakersButton.style.backgroundColor = '#bacde6';
            speakersButton.style.color = '#333';
            speakersButton.style.border = 'none';
            speakersButton.style.padding = '8px 16px';
            speakersButton.style.borderRadius = '4px';
            speakersButton.style.cursor = 'pointer';
            speakersButton.style.fontSize = '14px';

            // Dodanie funkcji przewijania do przycisku Prelegentów
            speakersButton.addEventListener('click', (event) => {
                event.stopPropagation(); // Zapobiega propagacji zdarzeń
                const target = document.getElementById('speakers');
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
            locationButton.style.backgroundColor = '#bacde6';
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
            headerInner.appendChild(speakersButton); // Dodaj przycisk Speakers
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
                speakersButton.textContent = isEnglish ? 'Speakers':'Prelegenci';
                locationButton.textContent = isEnglish ? 'Location':'Lokalizacja';
            });
        }
    });
</script>

<br><br>

<!-- Speakers -->
<h1 id="speakers" style="margin-top: 50px; font-weight: bold; font-size: 30px; margin-left: 10px;">
    <span class="lang-pl"><b>Prelerenci</b></span>
    <span class="lang-en hidden"><b>Speakers</b></span>
</h1>

<div class="about-section2">
    <div class="topics-container">
        <div class="topic">
  



<!-- Styl sekcji -->
<style>
  .speakers-section {
    padding: 40px 20px;
    background-color: #fff;
  }

  .speakers-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    margin-top: 10px;
    margin-left: 20px;
    margin-right: 20px;
  }

  .speaker-card {
    flex: 0 0 290px;
    text-align: center;
    cursor: pointer;
}



  .speaker-photo {
    width: 290px;
    height: auto;
    object-fit: cover;
    border-radius: 8px;
    border: 2px solid #ccc;
    transition: transform 0.3s;
  }

  .speaker-photo:hover {
    transform: scale(1.05);
  }

  .speaker-name {
    margin-top: 10px;
    font-weight: bold;
    color: #034A76;
  }

  .speaker-role {
    font-size: 14px;
    color: #555;
  }

  /* Modal */
  .modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0; top: 0;
    width: 100%; height: 100%;
    overflow: auto;
    background-color: rgba(0,0,0,0.6);
  }

  .modal-content {
    background-color: #fff;
    margin: 10% auto;
    padding: 20px;
    width: 90%;
    max-width: 600px;
    border-radius: 6px;
    position: relative;
  }

  .close-modal {
    color: #aaa;
    position: absolute;
    top: 10px; right: 20px;
    font-size: 24px;
    cursor: pointer;
  }
</style>




<!-- Sekcja: Prelegenci -->

<div class="speakers-section">
  <div class="speakers-grid">
    <!-- Prelegent 1 -->
    <div class="speaker-card" onclick="openModal('modal1')">
      <img src="./assets/ns.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Prof. Neil Selwyn</div>
    <div class="speaker-role">Keynote Speaker, Monasch University, Australia</div>
    </div>
    <!-- Prelegent 11 -->
    <div class="speaker-card" onclick="openModal('modal44')">
      <img src="./assets/pk.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Prof. Peter Kahn</div>
    <div class="speaker-role">University of Manchester</div>
    </div>
    <!-- Prelegent 2 -->
    <div class="speaker-card" onclick="openModal('modal2')">
      <img src="./assets/re.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Ross English</div>
    <div class="speaker-role">University of Southampton, UK</div>
    </div>
    <!-- Prelegent 3 -->
    <div class="speaker-card" onclick="openModal('modal3')">
      <img src="./assets/jm.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Assoc. Prof. Joanna Mytnik</div>
    <div class="speaker-role">Gdansk University of Technology, Poland</div>
    </div>
    <!-- Prelegent 4 -->
    <div class="speaker-card" onclick="openModal('modal4')">
      <img src="./assets/jb.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Jacqueline Bellon</div>
    <div class="speaker-role">University of Tübingen</div>
    </div>
    <!-- Prelegent 5 -->
    <div class="speaker-card" onclick="openModal('modal5')">
      <img src="./assets/ma.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Michael Agyemang Adarkwah</div>
    <div class="speaker-role">Friedrich Schiller University Jena</div>
    </div>
    <!-- Prelegent 6 -->
    <div class="speaker-card" onclick="openModal('modal6')">
      <img src="./assets/td.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Assoc. Prof. Tymoteusz Doligalski</div>
    <div class="speaker-role">SGH Warsaw School of Economics</div>
    </div>
        <!-- Prelegent 7 -->
    <div class="speaker-card" onclick="openModal('modal7')">
      <img src="./assets/lh.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr László Horváth</div>
    <div class="speaker-role">ELTE Eötvös Loránd University</div>
    </div>
    <!-- Prelegent 8 -->
    <div class="speaker-card" onclick="openModal('modal8')">
      <img src="./assets/mz.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Prof. Marek Zieliński</div>
    <div class="speaker-role">Collegium Da Vinci</div>
    </div>
    <!-- Prelegent 9 -->
    <div class="speaker-card" onclick="openModal('modal9')">
      <img src="./assets/kp.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Krzysztof Patkowski</div>
    <div class="speaker-role">Collegium Da Vinci</div>
    </div>
    <!-- Prelegent 10 -->
    <div class="speaker-card" onclick="openModal('modal10')">
      <img src="./assets/tk.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Tomasz Kopczewski</div>
    <div class="speaker-role">Faculty of Economic Sciences University of Warsaw</div>
    </div>
    <!-- Prelegent 11 -->
    <div class="speaker-card" onclick="openModal('modal11')">
      <img src="./assets/jp.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Prof. Joanna Paliszkiewicz</div>
    <div class="speaker-role">Warsaw University of Life Sciences</div>
    </div>
    <!-- Prelegent 12 -->
    <div class="speaker-card" onclick="openModal('modal12')">
      <img src="./assets/em.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Ewa Malinowska</div>
    <div class="speaker-role">Psychology Department, Warsaw University</div>
    </div>
    <!-- Prelegent 13 -->
    <div class="speaker-card" onclick="openModal('modal13')">
      <img src="./assets/al.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Albert Łukasik</div>
    <div class="speaker-role">Nicolaus Copernicus University</div>
    </div>
    <!-- Prelegent 14 -->
    <div class="speaker-card" onclick="openModal('modal14')">
      <img src="./assets/jc.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Jon Cardoso-Silva</div>
    <div class="speaker-role">LSE</div>
    </div>
    <!-- Prelegent 15 -->
    <div class="speaker-card" onclick="openModal('modal15')">
      <img src="./assets/10.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Ewelina Gdaniec</div>
    <div class="speaker-role">WSG University in Bydgoszcz</div>
    </div>
    <!-- Prelegent 16 -->
    <div class="speaker-card" onclick="openModal('modal16')">
      <img src="./assets/11.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Anna Miotk</div>
    <div class="speaker-role">University of Warsaw, Faculty of Journalism, Information, and Book Studies</div>
    </div>
    <!-- Prelegent 17 -->
    <div class="speaker-card" onclick="openModal('modal17')">
      <img src="./assets/12.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Jan Majewski</div>
    <div class="speaker-role">University of Warsaw</div>
    </div>
    <!-- Prelegent 18 -->
    <div class="speaker-card" onclick="openModal('modal18')">
      <img src="./assets/13.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Przemysław Tomczyk</div>
    <div class="speaker-role">Kozminski University</div>
    </div>
    <!-- Prelegent 19 -->
    <div class="speaker-card" onclick="openModal('modal19')">
      <img src="./assets/14.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Assoc. Prof. Igor Lyubashenko</div>
    <div class="speaker-role">SWPS University</div>
    </div>
    <!-- Prelegent 20 -->
    <div class="speaker-card" onclick="openModal('modal20')">
      <img src="./assets/15.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Krzysztof Karsznia</div>
    <div class="speaker-role">Warsaw University of Technology</div>
    </div>
    <!-- Prelegent 21 -->
    <div class="speaker-card" onclick="openModal('modal21')">
      <img src="./assets/16.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Krzysztof Książek</div>
    <div class="speaker-role">Warsaw University of Technology</div>
    </div>
    <!-- Prelegent 22 -->
    <div class="speaker-card" onclick="openModal('modal22')">
      <img src="./assets/17.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Sonja Niemann</div>
    <div class="speaker-role">Bavarian Research Institute for Digital Transformation (bidt)</div>
    </div>
    <!-- Prelegent 23 -->
    <div class="speaker-card" onclick="openModal('modal23')">
      <img src="./assets/18.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Antonia Becker</div>
    <div class="speaker-role">Bavarian Research Institute for Digital Transformation (bidt)</div>
    </div>
    <!-- Prelegent 24 -->
    <div class="speaker-card" onclick="openModal('modal24')">
      <img src="./assets/md.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Mary Dawood</div>
    <div class="speaker-role">University of Birmingham</div>
    </div>
    <!-- Prelegent 25 -->
    <div class="speaker-card" onclick="openModal('modal25')">
      <img src="./assets/kd.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Katarzyna Drożdżal</div>
    <div class="speaker-role">Instytut Psychologii PAN</div>
    </div>
    <!-- Prelegent 26 -->
    <div class="speaker-card" onclick="openModal('modal26')">
      <img src="./assets/jma.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Jacek Mańko</div>
    <div class="speaker-role">Kozminski University</div>
    </div>
    <!-- Prelegent 27 -->
    <div class="speaker-card" onclick="openModal('modal27')">
      <img src="./assets/kr.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Karolina Rożek</div>
    <div class="speaker-role">AGH University of Cracow</div>
    </div>
    <!-- Prelegent 28 -->
    <div class="speaker-card" onclick="openModal('modal28')">
      <img src="./assets/ak.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Agata Komendant-Brodowska</div>
    <div class="speaker-role">Faculty of Sociology, University of Warsaw</div>
    </div>
    <!-- Prelegent 29 -->
    <div class="speaker-card" onclick="openModal('modal29')">
      <img src="./assets/ae.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Ani Encheva</div>
    <div class="speaker-role">Utrecht University</div>
    </div>
    <!-- Prelegent 30 -->
    <div class="speaker-card" onclick="openModal('modal30')">
      <img src="./assets/pko.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Prof. Przemysław Kordos</div>
    <div class="speaker-role">University of Warsaw, Faculty of "Artes Liberales"</div>
    </div>
    <!-- Prelegent 31 -->
    <div class="speaker-card" onclick="openModal('modal31')">
      <img src="./assets/kso.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Krzysztof Skonieczny</div>
    <div class="speaker-role">University of Warsaw, Faculty of "Artes Liberales"</div>
    </div>
    <!-- Prelegent 32 -->
    <div class="speaker-card" onclick="openModal('modal32')">
      <img src="./assets/po.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Pauldy Otermans</div>
    <div class="speaker-role">Otermans Institute</div>
    </div>
    <!-- Prelegent 33 -->
    <div class="speaker-card" onclick="openModal('modal33')">
      <img src="./assets/da.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dev Aditya</div>
    <div class="speaker-role">Otermans Institute and Brunel University of London</div>
    </div>
    <!-- Prelegent 34 -->
    <div class="speaker-card" onclick="openModal('modal34')">
      <img src="./assets/jmo.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Jakub Możaryn</div>
    <div class="speaker-role">Warsaw University of Technology, Institute of Automatic Control and Robotics</div>
    </div>
    <!-- Prelegent 35 -->
    <div class="speaker-card" onclick="openModal('modal35')">
      <img src="./assets/ts.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr TING-YU SYLWIA LEE</div>
    <div class="speaker-role">SWPS University, Department of Asian Studies</div>
    </div>
    <!-- Prelegent 36 -->
    <div class="speaker-card" onclick="openModal('modal36')">
      <img src="./assets/jni.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Jedrzej Niklas</div>
    <div class="speaker-role">Institute of Continuing Education, University of Cambridge</div>
    </div>
    <!-- Prelegent 37 -->
    <div class="speaker-card" onclick="openModal('modal37')">
      <img src="./assets/dw.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Dominika Wiśniewska</div>
    <div class="speaker-role">Google for Education</div>
    </div>
    <!-- Prelegent 38 -->
    <div class="speaker-card" onclick="openModal('modal38')">
      <img src="./assets/jgr.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Prof. Jakub Growiec</div>
    <div class="speaker-role">SGH Warsaw School of Economics</div>
    </div>
    <!-- Prelegent 39 -->
    <div class="speaker-card" onclick="openModal('modal39')">
      <img src="./assets/th.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Tim Hallas</div>
    <div class="speaker-role">Anglia Ruskin University</div>
    </div>
    <!-- Prelegent 40 -->
    <div class="speaker-card" onclick="openModal('modal40')">
      <img src="./assets/jbw.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Justyna Berniak-Woźny</div>
    <div class="speaker-role">SWPS University</div>
    </div>
    <!-- Prelegent 41 -->
    <div class="speaker-card" onclick="openModal('modal41')">
      <img src="./assets/kma.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Karolina Małek</div>
    <div class="speaker-role">Warsaw University, Faculty of Psychology</div>
    </div>
    <!-- Prelegent 42 -->
    <div class="speaker-card" onclick="openModal('modal42')">
      <img src="./assets/gmo.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Assoc. Prof. Gaëlle Molinari</div>
    <div class="speaker-role">University of Geneva</div>
    </div>
    <!-- Prelegent 43 -->
    <div class="speaker-card" onclick="openModal('modal43')">
      <img src="./assets/mm.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Prof. Marek Mieńkowski</div>
    <div class="speaker-role">Pedagogium Wyższa Szkoła Nauk Społecznych</div>
    </div>
    <!-- Prelegent 45 -->
    <div class="speaker-card" onclick="openModal('modal45')">
      <img src="./assets/ww.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Wojciech Woźniak</div>
    <div class="speaker-role">Warsaw University of Life Sciences</div>
    </div>
    <!-- Prelegent 46 -->
    <div class="speaker-card" onclick="openModal('modal46')">
      <img src="./assets/srud.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Prof. Seweryn Rudnicki</div>
    <div class="speaker-role">AGH University</div>
    </div>
    <!-- Prelegent 47 -->
    <div class="speaker-card" onclick="openModal('modal47')">
      <img src="./assets/maghy.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Magdalena Hyczko</div>
    <div class="speaker-role">Google Cloud</div>
    </div>
    <!-- Prelegent 48 -->
    <div class="speaker-card" onclick="openModal('modal48')">
      <img src="./assets/abd.png" alt="Speaker Photo" class="speaker-photo">
      <div class="speaker-name">Dr Anna Baczko-Dombi</div>
    <div class="speaker-role">Faculty of Sociology, University of Warsaw</div>
    </div>
    <!-- Można dodać więcej prelegentów kopiując blok powyżej i zmieniając modal -->
  </div>
</div>


<!-- Modal - bio prelegenta -->
<div id="modal1" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal1')">&times;</span>
    <h3><b>prof. Neil Selwyn, Monasch University, Australia</b></h3>
    <p>
      Professor Neil Selwyn is a Distinguished Professor in the Faculty of Education at Monash University, Australia, and a leading international researcher in the field of digital education. His work critically explores the social, political and pedagogical implications of technology use in education. Over a 30-year academic career, he has authored or co-authored 18 books and over 300 scholarly publications, with his research translated into numerous languages. He is among the most cited Australian educational researchers, with an H-index of 97 and over 41,000 citations. Selwyn has led over 30 funded research projects, supported by institutions such as the ARC, UNESCO, Gates Foundation and Microsoft. He has advised global bodies including UNESCO, the OECD and the Council of Europe on the digitalisation of education. As former editor of *Learning, Media and Technology*, he has shaped critical debates in educational technology. He currently investigates the role of AI, datafication and digital automation in schools and universities. A sought-after keynote speaker, he regularly presents at conferences and advises policymakers across Europe, Asia and the Americas. He is a Fellow of the Academy of the Social Sciences in Australia and holds honorary appointments at Oxford and Lund University.
    <br> 
    <br><b>Title of presentation:</b> <br>
    <i>GenAI in Higher Education – some things we need to talk about</i>
    </p>
  </div>
</div>
<div id="modal2" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal2')">&times;</span>
    <h3><b>Dr. Ross English, University of Southampton, UK</b></h3>
    <p>
      Ross English is a Senior Teaching Fellow in Academic Practice in the Centre for Higher Education Practice at the University of Southampton, UK. He works with the Doctoral College, delivering training to postgraduate researchers. His research focuses of the experience of postgraduate researchers in UK Higher Education.
    <br> 
    <br><b>Title of presentation:</b> <br>
    <i>“It’s ‘easier than asking [my] supervisor for support’: UK based Doctoral candidates’ use of Generative AI and implications for supervisory support</i>
    </p>
  </div>
</div>
<div id="modal3" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal3')">&times;</span>
    <h3><b>Assoc. Prof. Joanna Mytnik, PhD, Director of the Center for Modern Education at Gdańsk University of Technology</b></h3>
    <p>
    Biologist, researcher, and academic lecturer (since 1999) and leader of the Center for Modern Education at Gdańsk University of Technology (since 2020). She is passionate about designing learning ecosystems based on the latest neuroscience research and with mindfulness towards human needs. She is fascinated by the search for innovative solutions in education.
    Since 2010, she has been conducting training for teachers at all educational levels (including over 300 hours of AI-related training), supporting the creation of innovative learning ecosystems and promoting the appreciation of teachers. She is a vocal opponent of traditional grading systems and oppressive educational structures.
    Her key areas of expertise include: educational transformation, neuroscience, gamification, AI in education, new technologies, assessment without grades, and active lecturing methods.
    For over 25 years, she has taught children, youth, and adults using original, non-standard teaching methods and tools.
    She is the creator of the EDUxAI strategy at Gdańsk University of Technology and the author of dozens of lectures, training sessions, and webinars on AI in education.
    More information: www.joannamytnik.com.pl
    <br> 
    <br><b>Title of presentation:</b> <br>
    <i>EDUxAI: A Comprehensive Strategy for Implementing Open GenAI Policy in Higher Education. Gdansk Tech case.</i>
    </p>
  </div>
</div>
<div id="modal4" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal4')">&times;</span>
    <h3><b>Jacqueline Bellon, Research Assistant, University of Tübingen</b></h3>
    <p>
    Jacqueline Bellon's background is in philosophy, specifically philosophy of technology, epistemology, theories of culture, the history and philosophy of the cognitive sciences, and the history of ideas. She is currently a research assistant at the University of Tübingen, Germany. Her research interests include human-technology relations, computer vision, and generative AI. She works in a three year project on "Epistemic and Ethical Aspects of Generative AI in Higher Education" in which she is developing empirically evaluated teaching material for university staff to use in classes. The material includes exercises on AI literacy, technical knowledge, competent and critical use of AI tools, proposals for an AI policy, for succesful assignment completion, and it overall aims at ensuring that we will continue to teach skills such as structured argumentation and standards of academic writing even in times in which a significant number of stundents complete written assignments with the help of Large Language Model applications.
    <br> 
    <br><b>Title of presentation:</b> <br>
    <i>Epistemical and ethical aspects of AI tools in higher education: teaching material and empirical results from a three-year project</i>
    </p>
  </div>
</div>
<div id="modal5" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal5')">&times;</span>
    <h3><b>Dr Michael Agyemang Adarkwah, Friedrich Schiller University Jena</b></h3>
    <p>
    Dr Michael Agyemang Adarkwah is a Research Associate at Friedrich Schiller University Jena, Germany. He was a Postdoctoral Researcher at Beijing Normal University, China. He is an Editor of the book series Assessment of Educational Technology(AET) at Routledge. He is a Senior Editor for Frontiers of Digital Education. He is also an Associate Editor for SN Social Sciences, the Journal of Applied Learning and Teaching (JALT), and the Journal of University Teaching and Learning Practice (JUTLP).
    <br> 
    <br><b>Title of presentation:</b> <br>
    <i>GenAI as a “Silent Partner” and “Silent Killer” in Adult Higher Education: A Pathway for Safe and Responsible Adoption</i>
    </p>
  </div>
</div>
<div id="modal6" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal6')">&times;</span>
    <h3><b>Assoc. Prof. Tymoteusz Doligalski, SGH Warsaw School of Economics</b></h3>
    <p>
    Tymoteusz Doligalski, Research and Teaching Fellow in the e-Business Unit at SGH Warsaw School of Economics. He researches the functioning of online companies, especially platforms, from the perspective of business models and AI. Deputy director of the AI Lab at SGH. He publishes research notes on the blog: https://www.doligalski.net/
    <br> 
    <br><b>Title of presentation:</b> <br>
    <i>GenAI as a Research Partner</i>
    </p>
  </div>
</div>
<div id="modal7" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal7')">&times;</span>
    <h3><b>Dr László Horváth, ELTE Eötvös Loránd University</b></h3>
    <p>
    László Horváth, is an economist-andragogue, currently working as an Assistant Professor at the Institute of Education, ELTE Eötvös Loránd University. He obtained his PhD (2019) in higher education management, focusing on higher education institutions as learning organisations. His research interests concentrate on how educational institutions and teaching professionals adapt and learn in response to the challenges of digital transformation (e.g. artificial intelligence). He worked in various national (e.g. post-doctoral research grant focusing on digital transformation in education) and international research, development, and consultancy projects (e.g. supporting the OECD in their study of labour market outcomes of Hungarian doctoral education or exploring quality assurance of digital teaching and learning in Hungarian higher education). He teaches in teacher education and continuous professional development, pedagogy BA, educational sciences MA, and human resources counselling MA programmes courses focusing on organizational/school development, development of entrepreneurial competencies, educational technology and policy.<br> 
    <br><b>Title of presentation:</b> <br>
    <i>Pedagogically-aware AI use of higher education teachers - developing a competence measurement scale</i>
    </p>
  </div>
</div>
<div id="modal8" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal8')">&times;</span>
    <h3><b>Prof. Marek Zieliński, Collegium Da Vinci</b></h3>
    <p>
    Rector of Collegium Da Vinci in Poznań, scientist, educator and practitioner with many years of experience in combining the world of science with business. In his scientific work, he focuses on business relations, which he studied from the perspective of trust, knowledge sharing and adaptation. His current research concerns the use of new technologies in education, especially tools based on artificial intelligence and their impact on learning and teaching processes.
    Author of numerous scientific publications on trust and knowledge exchange in B2B relations and the role of AI in shaping the modern education model. Co-author of the reports "Polish education in the shadow of AI" and "In search of competences for the future: forecasts for education and the labor market". Initiator of the futurological project "PoznAI future: On the mind and science", devoted to the vision of education of the future.
    In his activities, he promotes the ideas of a practical approach to learning and developing competences that respond to the dynamically changing needs of the labor market.
    As the rector of Collegium Da Vinci, a university focused on practical education in the creative business sector, Dr. Hab. Marek Zieliński actively supports the digitalization of universities, the use of new technologies in education and interdisciplinary initiatives of cooperation with business.
    <br><br><b>Title of presentation:</b> <br>
    <i>AI-Based Tools in Education: Attitudes and Dilemmas in the Light of Research</i>
    </p>
  </div>
</div>
<div id="modal9" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal9')">&times;</span>
    <h3><b>Dr Krzysztof Patkowski, Collegium Da Vinci</b></h3>
    <p>
    Dr Krzysztof Patkowski is Dean of the Faculty of Applied Sciences at Collegium Da Vinci. He is an education manager, academic lecturer, and researcher with extensive experience in developing practice-oriented study programs in close collaboration with employers, addressing the evolving demands of the global job market. His academic focus includes the impact of artificial intelligence on higher education and the development of future skills. He is the co-author of several influential publications in this field, including Polish Education in the Shadow of AI, Fears and Threats Related to AI in Education: One Phenomenon, Different Perspectives, and AI-Based Tools in Education: Attitudes and Dilemmas in the Light of Research.<br>
    <br><b>Title of presentation:</b> <br>
    <i>AI-Based Tools in Education: Attitudes and Dilemmas in the Light of Research</i>
    </p>
  </div>
</div>
<div id="modal10" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal10')">&times;</span>
    <h3><b>Dr Tomasz Kopczewski, Faculty of Economic Sciences University of Warsaw</b></h3>
    <p>
    Tomasz Kopczewski is an associate professor at the Faculty of Economic Sciences, University of Warsaw. His research and teaching focus on microeconomics, with a unique approach that channels insights from teaching into research. As an "economic knowledge engineer", he designs innovative teaching tools to foster a two-way knowledge flow. He developed the "Know Yourself" methodology, which combines experimental economics, data science, Monte Carlo simulations, philosophy, and ethics, bridging orthodox and heterodox theories. His recent work explores non-ergodic processes, ethical dilemmas in economics, and the role of collective knowledge in economic decisions.<br>
    <br><b>Title of presentation:</b> <br>
    <i>Algorithmic Troll or Collective Wisdom? Rethinking Economic Narratives Through Generative AI</i>
    </p>
  </div>
</div>
<div id="modal11" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal11')">&times;</span>
    <h3><b>Prof. Joanna Paliszkiewicz, Warsaw University of Life Sciences</b></h3>
    <p>
    Joanna Paliszkiewicz is a Full Professor at the Warsaw University of Life Sciences (WULS—SGGW), where she serves as the Director of the Management Institute. She is also a professor at the University of Economics in Ho Chi Minh City, Vietnam, and an adjunct professor at the University of Vaasa, Finland. She obtained her full professorship title from the International School for Social and Business Studies in Slovenia. A recognized expert in knowledge and trust management, she has published over 250 papers and is the author/co-author/editor of 23 books. She has received multiple research fellowships in the United States, Ireland, Slovakia, Taiwan, the UK, and Hungary. She is an active speaker at international conferences and serves as Deputy Editor-in-Chief of Management and Production Engineering Review and Associate Editor for Journal of Computer Information Systems, Expert Systems with Applications, Issues in Information Systems, Przegląd Organizacji, and Intelligent Systems with Applications. As President of the International Association for Computer Information Systems (IACIS) in the U.S., she organizes international conferences. She has successfully supervised Ph.D. students worldwide and has served as an external reviewer for doctoral programs in Poland, India, and Finland. She was awarded the Computer Educator of the Year (2013) by IACIS in the U.S. and is an expert for the Polish Accreditation Commission and a member of the Polish Academy of Science.
    Internet page: https://paliszkiewicz.pl<br>
    <br><b>Title of presentation:</b> <br>
    <i>Artificial Intelligence In Education and Research – Transforming Teaching, Learning, and Research Practices</i>
    </p>
  </div>
</div>
<div id="modal12" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal12')">&times;</span>
    <h3><b>Dr Ewa Malinowska, Psychology Department, Warsaw University</b></h3>
    <p>
    I have been leading at the Academia different formats of classes for over 20 years. Currently I am one of the members of a team at the Faculty of Psychology focusing on the improvement of teaching processes among lectures. Lately, one of the main areas of interest of our team is the widely understood usage/incorporation of AI in the processes of both teaching and learning.<br>
    <br><b>Title of presentation:</b> <br>
    <i>Attitudes towards the usage of AI in the group of psychology students</i>
    </p>
  </div>
</div>
<div id="modal13" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal13')">&times;</span>
    <h3><b>Albert Łukasik, Nicolaus Copernicus University</b></h3>
    <p>
    Master's degree in cognitive science currently at the PhD school of social sciences in Torun, where I'm focusing my research activity on the relationship between humans and artificial agents using psychological and neural approach. I completed a research internship in Lisbon studying human-computer interactions with the Pepper robot, currently focusing on the similiar issue in collaboration with a German research team in Bochum. I carried research on human-chatbot interactions and currently I'm researching perception of artificial intelligence among Polish students. In my career, I was involved in designing augmented reality applications for educational purposes, and currently I'm co-leading MindEasy - a company applying neurotechnology to education in combination with generative artificial intelligence in the form of a virtual tutor. In the free time, I conduct workshops introducing to artificial intelligence and virtual reality in social research.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>Brain-Powered AI Learning - Personalizing Education Through Neural Insights</i>
    </p>
  </div>
</div>
<div id="modal14" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal14')">&times;</span>
    <h3><b>Dr Jon Cardoso-Silva, LSE</b></h3>
    <p>
    Dr. Jonathan Cardoso-Silva is an Assistant Professor (Education) in the Data Science Institute at the London School of Economics (LSE), where he co-leads GENIAL (Generative AI as a Catalyst for Learning), a research initiative exploring the transformative potential of generative AI in higher education. At the LSE Data Science Institute, Jonathan integrates empirical learning approaches with AI-enhanced methodologies in undergraduate education in the data science courses he leads, DS105 and DS205. His recent work examines how ChatGPT influences student programming practices, illuminating both the opportunities and challenges these technologies present for contemporary education, and what it means for education in general. Through his innovative teaching practices and research, Jonathan actively shapes discussions around meaningful, effective, and ethically sound AI integration in academia.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>Bridging the Learning Divide: Mitigating Generative AI’s Impact on Student Engagement and Critical Thinking</i>
    </p>
  </div>
</div>
<div id="modal15" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal15')">&times;</span>
    <h3><b>Dr Ewelina Gdaniec, WSG University in Bydgoszcz</b></h3>
    <p>
    Dr Ewelina Gdaniec is a digital humanities researcher, with a background in contemporary history and historical methodology. She has coordinated interdisciplinary projects focusing on historical game development, integrating AR solutions into higher education and developing e-courses for diverse student populations. Her forthcoming monograph, History 2.0, delves into novel digital methods of historical research, emphasizing collaboration between humanities and technology. In her research, she explores i.e. how AI-driven methodologies can transform historical inquiry, educational game design and e-learning platforms. In addition to her scholarly pursuits, dr Gdaniec actively mentors emerging female researchers and promotes inclusive STEM engagement.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>Cyfrowa rekonfiguracja przeszłości: generatywna AI jako narzędzie weryfikacji i rekonstrukcji źródeł historycznych</i>
    </p>
  </div>
</div>
<div id="modal16" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal16')">&times;</span>
    <h3><b>Dr Anna Miotk, University of Warsaw, Faculty of Journalism, Information, and Book Studies</b></h3>
    <p>
    Since 2014, she has been the director of communications at Polskie Badania Internetu. At the same time, she works as an academic teacher at the Faculty of Journalism, Information and Bibliology at the University of Warsaw. Her professional experience also includes leading the development of a media monitoring system and PR consultancy. She holds a PhD in Political Science, having previously completed a Master's degree in Sociology at the University of Gdansk. Business trainer and author. Winner of the Lew PR 2023 award from the Polish Public Relations Association for lifetime achievement.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>Decoding the Digital Divide: AI Literacy Across Demographics and Its Implications for Education</i>
    </p>
  </div>
</div>
<div id="modal17" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal17')">&times;</span>
    <h3><b>Dr Jan Majewski, University of Warsaw</b></h3>
    <p>
    Jan Majewski - assistant professor at the Department of Digital Sociology, University of Warsaw. He specializes in social simulation and social network analysis with strong focus on applied problems of sustainable cooperation, reputation management and computational law. His interest in generative models is broad, but he deems latest developments in AI agent architecture as especially important.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>Explainability as humanity’s stronghold? The case of (plausible) scientific advisers.</i>
    </p>
  </div>
</div>
<div id="modal18" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal18')">&times;</span>
    <h3><b>Dr Przemysław Tomczyk, Kozminski University</b></h3>
    <p>
    Przemysław Tomczyk, PhD in economics in the field of management sciences. He defended his PhD thesis at the Warsaw School of Economics in 2015. Assistant professor at the Department of Marketing at Kozminski University.
    He specializes in the role of artificial intelligence in scientific writing and science automation. Author of several dozen scientific publications and the YouTube channel "dr Przemek Tomczyk AI".
    https://www.youtube.com/@drprzemek
    Teaches how to write scientifically more ethical, faster and better using artificial intelligence.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>From Automation to Partnership: The Evolving Role of AI in Academic Writing</i>
    </p>
  </div>
</div>
<div id="modal19" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal19')">&times;</span>
    <h3><b>Assoc. Prof. Igor Lyubashenko, SWPS University</b></h3>
    <p>
    Igor Lyubashenko is an associate professor at SWPS University and an expert in the use of AI in research,  He has over 10 years of experience as an expert in social research and qualitative research methodology. His research focuses on factors determining the effectiveness of public policies, solutions, and interventions. He has led two projects funded by the National Science Centre and participated in several other scientific and applied projects. He teaches courses on public management, public solution design, systems thinking, and methodological courses.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>From Digital Conversations to Research Insights: AI-Assisted Exploration of Social Dynamics</i>
    </p>
  </div>
</div>
<div id="modal20" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal20')">&times;</span>
    <h3><b>Dr Krzysztof Karsznia, Warsaw University of Technology</b></h3>
    <p>
    Academic teacher (Assistant Professor at Warsaw University of Technology) – surveyor with many years of practical and scientific experience who has worked in Poland and abroad (e.g., Swiss Federal Institute of Technology ETH Zurich). He participated in numerous foreign internships, conferences, postgraduate studies, and workshops. Constantly improving his qualifications both in the research and didactic spheres. A passionate about modern teaching methods, as well as aspects of university internationalization.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>Future Directions in Geodesy and Cartography Education: Student Perspectives on Technology and AI-Driven Skills</i>
    </p>
  </div>
</div>
<div id="modal21" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal21')">&times;</span>
    <h3><b>Krzysztof Książek, Warsaw University of Technology</b></h3>
    <p>
    In 2021, he obtained his M.Sc. degree after completing full-time second-cycle studies in Geodesy and Cartography with a specialisation in Engineering Geodesy at the Faculty of Geodesy and Cartography, Warsaw University of Technology. He completed his master's studies with honours. His MSc thesis was recognised in the Association of Polish Surveyors' competition for the ‘Best thesis defended at the Faculty of Geodesy and Cartography in 2020/2021’, where he was awarded 2nd place in the MSc thesis category. He is currently employed at the Department of Engineering Geodesy and Measurement Systems, Faculty of Geodesy and Cartography, Warsaw University of Technology. He is a member of the Association of Polish Surveyors, the Scientific and Technical Section of Engineering Geodesy and the Scientific Society of Revitalization. He holds certificates: ECDL 2D CAD, CIVIL 3D, EPP GIS.
    Scientific interests: displacement and deformation monitoring of buildings, technical condition analyses of historical buildings with modelling and AI
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>Future Directions in Geodesy and Cartography Education: Student Perspectives on Technology and AI-Driven Skills</i>
    </p>
  </div>
</div>
<div id="modal22" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal22')">&times;</span>
    <h3><b>Sonja Niemann, Bavarian Research Institute for Digital Transformation (bidt)</b></h3>
    <p>
    Academic Backround:<br>
    BSc Psychology
    MSc Computing in the Humanities<br>
    Current affiliation:
    Researcher at bidt since May 2024 and PhD candidate at Cognitive Systems Chair, University of Bamberg
    Current research project: Human-AI co-creation of code with different prior knowledge: Effects on performance and trust (pAIrProg)
    Results for example: A survey about code generator use by computer science students. Why do they use them and for what tasks? The goal of the project is to incorporate genAI into Computer science education, specifically programming without sacrificing basic knowledge about programming concepts.
    Other projects and Interests: Intelligent Tutoring System for recursive programming; Trust in AI; effects from role models on women in STEM; XAI 
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>GenAI in Universities : Between Academic Freedom and Regulatory Chaos</i>
    </p>
  </div>
</div>
<div id="modal23" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal23')">&times;</span>
    <h3><b>Antonia Becker, Bavarian Research Institute for Digital Transformation (bidt)</b></h3>
    <p>
    Antonia Becker is a research assistant in the Research Department at the Bavarian Research Institute for Digital Transformation. She studied law at the LMU Munich and Uppsala University. She is currently doing her legal clerkship at the Higher Regional Court of Munich. During her studies, she specialized in intellectual property, competition law and antitrust law, where she focused on copyright law and AI. Since December 2024, she has been researching at bidt in the interdisciplinary project “Legal uncertainty through generative AI? Reform considerations for the promotion of system trust at universities” as part of the research focus ‘Humans and Generative Artificial Intelligence: Trust in Co-Creation’.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>GenAI in Universities : Between Academic Freedom and Regulatory Chaos</i>
    </p>
  </div>
</div>
<div id="modal24" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal24')">&times;</span>
    <h3><b>Dr Mary Dawood, University of Birmingham</b></h3>
    <p>
    Dr Mary Dawood is a Lecturer in Economics at the University of Birmingham. She has undertaken a variety of administrative roles at the School level, amongst which is Generative AI co-lead. In recognition of her distinction in higher education practice, she has been awarded the status of Senior Fellow in the Higher Education Academy (SFHEA). Dr Dawood has presented her research on the application of gamification techniques in economics pedagogy, the creation of inclusive and engaging teaching and learning environments, and case studies on integrating generative AI into business education at esteemed national and international conferences. Her publications in leading education journals disseminate these innovative practices to a global audience. Dr Dawood’s work is driven by a commitment to educational excellence, a passion for diversity and inclusivity, and a dedication to advancing knowledge through impactful scholarly endeavours aimed at empowering students and transforming learning.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>GenAI Literacy: Empowering Students for the Future</i>
    </p>
  </div>
</div>
<div id="modal25" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal25')">&times;</span>
    <h3><b>Katarzyna Drożdżal, Instytut Psychologii PAN</b></h3>
    <p>
    Psychologist, researcher, and designer. She holds a master's degree in psychology from the University of Silesia (2007). She is currently a PhD candidate at the Personality Psychology Lab of the Institute of Psychology, Polish Academy of Sciences, under the supervision of Professor Małgorzata Fajkowska.
    Her research interests include cyberpsychology, personality, narrative, and social psychology. She focuses mainly on the self-regulation processes of digital product users.
    Professionally, she specializes in user experience research and service design. She has coordinated numerous projects related to the development of digital products. She is the co-founder of the research agency Selkie and a co-organizer of the international World Usability Day Silesia conference, where she also engages in public outreach. She collaborates with various organizations, including the Polish-American Freedom Foundation, as part of the Sektor 3.0 Fund initiative.
    She also teaches within the User Experience Design and E-marketing postgraduate programs at SWPS University.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>Generative AI in Social Research: The Relevance of Scientific Integrity and Reliability in the Face of Technological Hype</i>
    </p>
  </div>
</div>
<div id="modal26" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal26')">&times;</span>
    <h3><b>Jacek Mańko, Kozminski University</b></h3>
    <p>
    Jacek Mańko is a research and teaching associate at the Kozminski University, Department of Management in Digital and Networked Societies. His research interests center on science and technology studies, with a focus on artificial intelligence and digital media. Additionally, he critically engages in public discourse on these issues and actively contributes to the popularization of science.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>Generative AI in Social Research: The Relevance of Scientific Integrity and Reliability in the Face of Technological Hype</i>
    </p>
  </div>
</div>
<div id="modal27" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal27')">&times;</span>
    <h3><b>Karolina Rożek, AGH University of Cracow</b></h3>
    <p>
    A master’s student in sociology at AGH University of Science and Technology, coordinating a research project on how students use GPT models in their academic work. The project examines how individuals from various disciplines use GPT models and for which academic tasks they apply them. She is also intrigued by the role of AI in various contexts, not only in automating repetitive tasks and expanding knowledge but also in its applications in scientific and research work.
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>GPT and the Future of Learning: A Study on AI Usage in Academic Tasks</i>
    </p>
  </div>
</div>
<div id="modal28" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal28')">&times;</span>
    <h3><b>Dr Agata Komendant-Brodowska, Faculty of Sociology, University of Warsaw</b></h3>
    <p>
    Educational change-maker, project leader, educator, researcher, sociologist and formally - Assistant Professor at the University of Warsaw, Faculty of Sociology.
    <br>What makes me busy now:<br>
    -> socialpolarisation.eu -> I'm leading a European educational project ActIPLEx whose aim is to create online courses (MOOCs and university courses), educational games and game-based workshops about social polarisation and dialogue. It is also a continuation of ACTISS-EDU.EU, a project devoted to creating online courses about computational social sciences;
    <br>-> teaching: introductory workshops on data analysis in social sciences, introduction to modelling and simulations, and recently also project management;
    <br>-> I'm also coordinating the science festival (Festiwal Nauki) at the Faculty of Sociology UW
    <br>
    <br><b>Title of presentation:</b> <br>
    <i>How Creating MOOCs Helped us Become Better Teachers: the Case for Integrating New Technologies in Everyday Educational Practices</i>
    </p>
  </div>
</div>
<div id="modal29" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal29')">&times;</span>
    <h3><b>Ani Encheva, Utrecht University</b></h3>
    <p>
    Ani Encheva is a Research Master’s student in Media, Art, and Performance Studies at Utrecht University, where she also completed her BA in Media and Culture. She is currently a student assistant at the Data School, an editor for the Graduate Journal of the Humanities Junctions, and a participant in the Leadership Honours Programme. In early 2025, Ani completed a research internship under the supervision of Dr. Karin van Es and Dr. Dennis Nguyen, contributing to a project on ChatGPT data donations, which invited students to share their ChatGPT data for academic research. In parallel, she conducted an independent study, interviewing Humanities students at Utrecht University to examine their perspectives on the role of Generative AI in higher education. This experience solidified her research interest in the critical study of education and technology, which she is eager to develop further in her Master’s thesis in September 2025.
    <br><b>Title of presentation:</b> <br>
    <i>How Do We Draw the Line? Students' Perspectives on Plagiarism and Academic Integrity in the Age of Generative AI</i>
    </p>
  </div>
</div>
<div id="modal30" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal30')">&times;</span>
    <h3><b>Prof. Przemysław Kordos, University of Warsaw, Faculty of "Artes Liberales"</b></h3>
    <p>
    Dr. hab. prof. ucz. Przemysław Kordos graduated from the University of Warsaw, earning two master's degrees: one in Sociology and another in Ethnology, both theses focusing on contemporary Greece. In 2020, he obtained his habilitation based on the book “Beyond Greekness: Studies in Contemporary Greek Prose”. He teaches courses on contemporary literature and culture of Greece and Cyprus, cultural studies methodology and speculative literature. Since 2022 he also teaches and co-teaches courses for academic teachers and students on AI in Higher Education. He has translated into Polish books by Nikos Dimou, Petros Markaris, and Antonis Georgiou.
    <br><b>Title of presentation:</b> <br>
    <i>How Not to Keep Up with gAI: Workshop Insights on Navigating the Generative AI Revolution in Higher Education</i>
    </p>
  </div>
</div>
<div id="modal31" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal31')">&times;</span>
    <h3><b>Dr Krzysztof Skonieczny, University of Warsaw, Faculty of "Artes Liberales"</b></h3>
    <p>
    Krzysztof Skonieczny is Assistant Professor at the Faculty of “Artes Liberales”, Uni­versity of Warsaw, where he is a member of the Techno-Humanities Lab and teaches a number of courses in animal studies and contemporary “continental” philosophy. He is the author of Immanence and the Animal. A Conceptual Inquiry (Routledge 2020) and co-editor (with Szymon Wróbel) of Living and Thinking in the Post-Digital World. Theories, Experiences, Expectations (Universitas 2021), and Regimes of Capital in the Post-Digital Age (Routledge 2023). His next book, Deleuze and Slowness. Against Accelerationist Thinking is forthcoming (Bloomsbury 2025). He is currently Principal Investigator in the projects EDUCATHUM: „Education at the Frontiers of the Human: The Challenge of New Technologies” (NCN OPUS LAP, 2023-2026) and AIAI: “AI: Authorship and Interpretation” (NCN OPUS LAP 2025-2027).
    <br><b>Title of presentation:</b> <br>
    <i>How Not to Keep Up with gAI: Workshop Insights on Navigating the Generative AI Revolution in Higher Education</i>
    </p>
  </div>
</div>
<div id="modal32" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal32')">&times;</span>
    <h3><b>Dr Pauldy Otermans, Otermans Institute</b></h3>
    <p>
    Dr. Pauldy Otermans is a female tech leader in the UK. She is a neuroscientist and psychologist by academic background and a female leader of AI technology. She was awarded as the inspirational womxn in the Tech Industry by Hustle Awards, was named one of the ‘22 most influential women in the UK of 2022’ by Start-Up Magazine UK, and has also been awarded by the UK Prime Minister in the UK in 2021, and globally for her work. Pauldy helped build the first digital human teachers powered by AI in 2021 called OIAI. Her language models are now also used to power Teddy AI which is a conversational AI study buddy for all children aged 3-7 years where parents can control their child's learning journey by prompting Teddy AI and get reports back. Its users dubbed Teddy as the potential "ChatGPT for children". She is the winner of the Women in Tech Excellence award 2023. She is also active in the research community of AI in Education and is Topic Editor for Frontiers in AI: The Role of Conversational AI in Higher Education.
    <br><b>Title of presentation:</b> <br>
    <i>My version is what I want and what I need: How personalisation of learning content is changing EdTech and HE forever</i>
    </p>
  </div>
</div>
<div id="modal33" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal33')">&times;</span>
    <h3><b>Dev Aditya, Otermans Institute and Brunel University of London</b></h3>
    <p>
    Dr. Pauldy Otermans is a female tech leader in the UK. She is a neuroscientist and psychologist by academic background and a female leader of AI technology. She was awarded as the inspirational womxn in the Tech Industry by Hustle Awards, was named one of the ‘22 most influential women in the UK of 2022’ by Start-Up Magazine UK, and has also been awarded by the UK Prime Minister in the UK in 2021, and globally for her work. Pauldy helped build the first digital human teachers powered by AI in 2021 called OIAI. Her language models are now also used to power Teddy AI which is a conversational AI study buddy for all children aged 3-7 years where parents can control their child's learning journey by prompting Teddy AI and get reports back. Its users dubbed Teddy as the potential "ChatGPT for children". She is the winner of the Women in Tech Excellence award 2023. She is also active in the research community of AI in Education and is Topic Editor for Frontiers in AI: The Role of Conversational AI in Higher Education.
    <br><b>Title of presentation:</b> <br>
    <i>Dev Aditya is an expert in AI from London, UK. He led the team that built the first Digital Human AI teacher (OIAI) with the mission to upskill 750 million learners globally by 2030. Currently, his AI teachers teach in 8 countries from teaching for universities and corporates to direct marginalised learners. Dev Aditya has also developed a specialist teaching and learning LLM OIMISA-7B. Dev Aditya was awarded by the UK Prime Minister for his work and has been a Young Global Innovator and Under 30 Social Entrepreneur (Mint). For research work in AI, he was recognised by Innovate UK and secured national level funding from them. He has conducted AI and HCI research with The Alan Turing Institute and Brunel University of London, regularly publishes in this space, and his work is currently operating in 15 countries.</i>
    </p>
  </div>
</div>
<div id="modal34" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal34')">&times;</span>
    <h3><b>Dr Jakub Możaryn, Warsaw University of Technology, Institute of Automatic Control and Robotics</b></h3>
    <p>
    Jakub Filip Możaryn is an assistant professor at the Warsaw University of Technology, specializing in automation, robotics, and artificial intelligence. His research focuses on designing adaptive and autonomous systems using AI and machine learning, particularly in control systems and process modelling. Jakub has extensive experience integrating modern digital solutions into higher education, emphasizing interactive and student-centred learning methods. He contributes to curriculum modernization, particularly in automation and digital learning tools. Currently, he leads the project at Warsaw University of Technology, "MyPW: Intelligent System for Improving the Warsaw University of Technology Campus."
    <br><b>Title of presentation:</b> <br>
    <i>MyPW: Intelligent System for Improving the Warsaw University of Technology Campus</i>
    </p>
  </div>
</div>
<div id="modal34" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal34')">&times;</span>
    <h3><b>Dr Jakub Możaryn, Warsaw University of Technology, Institute of Automatic Control and Robotics</b></h3>
    <p>
    Jakub Filip Możaryn is an assistant professor at the Warsaw University of Technology, specializing in automation, robotics, and artificial intelligence. His research focuses on designing adaptive and autonomous systems using AI and machine learning, particularly in control systems and process modelling. Jakub has extensive experience integrating modern digital solutions into higher education, emphasizing interactive and student-centred learning methods. He contributes to curriculum modernization, particularly in automation and digital learning tools. Currently, he leads the project at Warsaw University of Technology, "MyPW: Intelligent System for Improving the Warsaw University of Technology Campus."
    <br><b>Title of presentation:</b> <br>
    <i>MyPW: Intelligent System for Improving the Warsaw University of Technology Campus</i>
    </p>
  </div>
</div>
<div id="modal35" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal35')">&times;</span>
    <h3><b>Dr TING-YU SYLWIA LEE, SWPS University, Department of Asian Studies</b></h3>
    <p>
    I have been teaching Chinese in Poland as a native speaker more than 15 year. I have been teaching Chinese language courses in SWPS  University since 2008. Through my contacts in the Chinese academic community in mainland and Taiwan, I assisted  numerous Polish students to obtain scholarships in Taiwan and mainland China. I am determined to introduce Polish  university students to various aspects of Chinese tradition and culture. I am currently working on a series of research articles related to the Chinese Internet language, communication and social media. I have published two scientific papers  in Taiwan and Poland. My research interests include:(1) intercultural communication and managment in Chinese societies;(2) development of  the Internet lexicon in China ; (3) social capital and internet communication in China; (4)internet words and phrases  adapted from mainland China in Taiwan; (5) online Chinese teaching and learning in the unversity with the application of AI  and  ChatGPT.
    <br>1.Journal Article: Online Chinese Teaching During the Pandemic—A Case Study of SWPS University in  Poland"疫情下的線上華語教學—以波蘭人文(SWPS)大學為例”, "pp. 171-178, Chinese World, Issue 131, June  2023.
    <br>2.Scentific Report for Institute of New Europe (Think Tank ) ：The Rise of Chinese Internet Language :  Internet Lexicon and Social Media, 2022. http:// ine.org.pl/en/the-rise-of-chinese-internet-language internet-lexicon-and-social-media/
    <br>3.Journal Article:“Language Change in Progress: Chinese Internet Lexicon and the Symbolic Meaning in the Harmonious  Society”, p.132-145, Nowa Polityka Wschodnia nr 4 (27), 2020.
    <br>4.Journal Article:Dynamic Cultural Impact and Computer Assisted Language Learning (CALL) for Second Language  Acquisition (SLA)”, p. 107-111, China : Language –Culture – Business, Warsaw 2013.
    <br>5.Article in the book : “The influence of Neo-Confucianism on moral education : a comparative case study between  Mainland China and Taiwan”, China past and present”, Warsaw University Press, pp.158-169, Warsaw 2010.
    <br><b>Title of presentation:</b> <br>
    <i>Online Education Platform : A Case Study of Application of  Google classroom integrated with E-learning Platform for  teaching Chinese Phonetics </i>
    </p>
  </div>
</div>
<div id="modal36" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal36')">&times;</span>
    <h3><b>Dr Jedrzej Niklas, Institute of Continuing Education, University of Cambridge</b></h3>
    <p>
    Dr Jedrzej Niklas is a Senior Teaching Associate at the University of Cambridge, where he specialises in AI governance and the role of technology in the public sector. His research draws on socio-legal studies and critical data studies to explore how AI and data infrastructures transform public institutions, state authority, and the governance of natural resources. He has worked across sectors including public administration, environmental management, and civil society.
    <br>Before entering academia, Jedrzej was a legal and policy analyst in the non-governmental sector, actively involved in EU-level debates on GDPR, digital rights, and AI regulation. He previously held research positions at the London School of Economics, Cardiff University’s Data Justice Lab, and the Polish Academy of Sciences. He continues to advise on grant-making strategies related to data justice and the political dimensions of AI governance.
    <br><b>Title of presentation:</b> <br>
    <i>Teaching AI Governance & Ethics in Higher Education: Complexity, Policy, and Critical Perspectives</i>
    </p>
  </div>
</div>
<div id="modal37" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal37')">&times;</span>
    <h3><b>Dr Dominika Wiśniewska, Google for Education</b></h3>
    <p>
    Dominika Wiśniewska is a seasoned professional with over 15 years of experience dedicated to the advancement of digital literacy and inclusion. Her career encompasses the strategic management of communication initiatives for non-profit organisations, the development of technological education communities, and the formulation of educational strategy at the Central Technology Hub (CDT), with a specific focus on promoting STEAM education.
    <br>Currently, as Customer Success Manager at Google for Education Poland, she spearheads the development of educational strategies pertaining to artificial intelligence skills and competencies, while fostering collaborative relationships with schools and universities. Possessing a PhD in Social Sciences, she conducts research on the role of media in political contexts and holds a lectureship at SWPS University in Warsaw.
    <br><b>Title of presentation:</b> <br>
    <i>The Algorithmic Colleague: A Critical Dialogue on AI's Role in Academic Work</i>
    </p>
  </div>
</div>
<div id="modal38" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal38')">&times;</span>
    <h3><b>Prof. Jakub Growiec, SGH Warsaw School of Economics</b></h3>
    <p>
    Professor of Economics, SGH Warsaw School of Economics, Poland. His core research interests include long-run economic growth, technological change and the economics of transformative AI. He has published 35 scientific articles in respectable international journals and a monograph Accelerating Economic Growth: Lessons From 200 000 Years of Technological Progress and Human Development (Springer, 2022). He believes that transformative AI is a source of existential risk for humanity.
    <br><b>Title of presentation:</b> <br>
    <i>The Economics of p(doom): Scenarios of Existential Risk and Economic Growth in the Age of Transformative AI</i>
    </p>
  </div>
</div>
<div id="modal39" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal39')">&times;</span>
    <h3><b>Dr Tim Hallas, Anglia Ruskin University</b></h3>
    <p>
    Tim Hallas completed his undergraduate studies in music at ARU, Cambridge and has gone onto post-graduate study with the University of Hertfordshire and the University of Cambridge. He is now completing his PhD back where he started at ARU with Dr Phil Kirkman and Dr Fiona Aubrey-Smith. Tim is an expert in the use of technology as a pedagogical teaching tool and has written many articles on the subject and spoken at many conferences. 
    <br>He currently works as the Head of Digital Pedagogy at Hills Road Sixth Form College, Cambridge, UK. His current research interests are focused on technology mediated pedagogy and organisational development and the potential of AI as a tool for teaching.
    <br><b>Title of presentation:</b> <br>
    <i>The Impact of AI on Education and Its Disruptive Potential on Existing Power Dynamics</i>
    </p>
  </div>
</div>
<div id="modal40" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal40')">&times;</span>
    <h3><b>Dr Justyna Berniak-Woźny, SWPS University</b></h3>
    <p>
    Dr. Justyna Berniak-Woźny holds a PhD in Social Sciences from Leeds Metropolitan University (now Leeds Beckett University) and an MBA from Oxford Brookes University. She is a researcher and lecturer at SWPS University. Her expertise lies in ESG, corporate social responsibility (CSR), and sustainable development from a process and project management perspective. She is the author of numerous national and international scientific publications, as well as educational and training materials in these fields. Dr. Berniak-Woźny is a certified business trainer, an accredited tutor, and an experienced Project Manager (PMP, Agile PM Practitioner) with extensive experience in managing projects that support green and digital transformation. Her research and teaching also focus on future competences, including AI literacy, fostering the development of skills necessary to navigate the evolving landscape of sustainable business and technology-driven innovation.
    <br><b>Title of presentation:</b> <br>
    <i>University Students' Employability and Workability Skills for the Workplace in the Digital Era: Insights from AI Usage in Higher Education</i>
    </p>
  </div>
</div>
<div id="modal41" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal41')">&times;</span>
    <h3><b>Dr Karolina Małek, Warsaw University, Faculty of Psychology</b></h3>
    <p>
    I am an Assistant Professor at the Faculty of Psychology, University of Warsaw, where I am engaged in both teaching and research. I am a Member of the Didactic Council and the Teaching Development Team at the Faculty of Psychology, driving to enhance the quality of education through innovative didactic strategies. Additionally, I coordinate Psychological Education for students specializing in teacher training at Warsaw University, preparing them for their future roles in education.My research focuses on qualitative studies of schools, teachers, and learning processes, including those within higher education. I am particularly interested in how educational environments shape both teaching practices and student experiences. By integrating psychological perspectives with pedagogical approaches, I aim to contribute to the development of more effective and evidence-based teaching methodologies.
    <br><b>Title of presentation:</b> <br>
    <i>Use, attitudes and perceptions of AI among Psychology students of UW</i>
    </p>
  </div>
</div>
<div id="modal42" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal42')">&times;</span>
    <h3><b>Assoc. Prof. Gaëlle Molinari, University of Geneva</b></h3>
    <p>
    Gaëlle Molinari is an Associate Professor in Educational Technologies at the University of Geneva, where she leads the TEPEE group (Technologies for Positive lEarning Experiences) within the TECFA Lab. TEPEE investigates how digital learning environments can be designed to enhance well-being and encourage beneficial types of motivation and emotions. She and her team are currently exploring artificial intelligence systems and their impact on the transformation of academic skills.
    <br><b>Title of presentation:</b> <br>
    <i>Students’ Perceptions of GenAI’s Impact on Their Psychological Needs for Autonomy and Competence: A METUX-Based Approach</i>
    </p>
  </div>
</div>
<div id="modal43" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal43')">&times;</span>
    <h3><b>Prof. Marek Mieńkowski, Pedagogium Wyższa Szkoła Nauk Społecznych</b></h3>
    <p>
    Prof. Dr. Marta Mackiewicz is an assistant professor at the Institute of World Economy at the Warsaw School of Economics. She deals with issues related to business innovation, regional competitiveness, clusters and sustainable development. She has participated in over 100 research and evaluation projects, including the project ‘Investigating the Impact of the Innovation Union’ (2015-2018) as part of the Horizon 2020 programme and ‘Cluster Action For Ecosystem Innovation Network’ as part of the Horizon Europe programme. In 2017-2019, she participated in the international project ‘Assessing and Improving Research Performance at South East Asian Universities’. She is the head of the postgraduate studies ‘ESG Business Models. Sustainability Reporting’. She is the author of publications and expert opinions for government institutions, the European Commission and the European Investment Bank.
    Prof. WSNS dr Marek Mieńkowski is the rector of Pedagogium WSNS in Warsaw. He deals with issues related to the ethical area of AI, quantum AI, decision theory and ESG. He has participated in many research and innovation projects. He is the author of many courses of study and an assessor evaluating applications for EU funding.
    <br><b>Title of presentation:</b> <br>
    <i>Polish science needs a Polish LLM</i>
    </p>
  </div>
</div>
<div id="modal44" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal44')">&times;</span>
    <h3><b>Prof. Peter Kahn, University of Manchester</b></h3>
    <p>
    <br><b>Title of presentation:</b> <br>
    <i>Teacher agency and Generative AI: reconceptualising Higher Education pedagogy</i>
    </p>
  </div>
</div>
<div id="modal45" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal45')">&times;</span>
    <h3><b>Dr Wojciech Woźniak, Warsaw University of Life Sciences</b></h3>
    <p>
    Political scientist, archivist, civil servant
    He graduated from the Institute of Social Sciences at Opole University in 1999 and the Institute of Administration in 2000. In 2004, he earned a PhD from the Institute of History at Opole University.
    From December 1999 to March 2009, he worked as an archivist at the State Archive in Opole, where he served as the head of the department responsible for records created after 1945. In April 2009, he became the National Digital Archives (NDA) deputy director. Since October 2012, he has held the position of director of the NDA.
    In addition to his archival work, he has been a lecturer at the University of Warsaw since October 2009, teaching electronic records management.
    Between 2016 and 2018, he served as the Director General of State Archives. From 2019 to 2021, he worked at the General Counsel to the Republic of Poland. Since February 2021, he has been the director of the Main Library at the Warsaw University of Life Sciences.
    <br><b>Title of presentation:</b> <br>
    <i>Navigating the digital evolution of WULS in the age of artificial intelligence: achievements, challenges and perspectives</i>
    </p>
  </div>
</div>
<div id="modal46" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal45')">&times;</span>
    <h3><b>Prof. Seweryn Rudnicki, AGH University</b></h3>
    <p>
    Seweryn Rudnicki – PhD, associate professor at AGH University, sociologist. His research interests include the practical application of social science knowledge, the use of AI technologies in social research, creativity and innovation studies. He is the co-founder of the agency Hearts & Heads, which supports businesses in implementing user-centered design approaches and creativity techniques. He also collaborates with Delft University of Technology (Netherlands), co-develops the Science of Ideas project, and is involved in the SoTechLab and Gender Equality Team at AGH.
    <br><b>Title of presentation:</b> <br>
    <i>AI and Reconfiguration of Social Research Practices</i>
    </p>
  </div>
</div>
<div id="modal47" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal47')">&times;</span>
    <h3><b>Magdalena Hyczko, Google Cloud</b></h3>
    <p>
    Programmer and analyst with over a decade of experience in Enterprise IT and network systems for major Polish IT providers like Cisco, IBM, and Microsoft. At Google Cloud for 3+ years, she provides tech support specializing in digital transformation and AI. Since 2024, she's a Konstancin-Jeziorna city councilor and Deputy Chairwoman. Holds a Computer Science degree from AGH and postgraduate Gender Studies from Jagiellonian University.
    <br><b>Title of presentation:</b> <br>
    <i>The Algorithmic Colleague: A Critical Dialogue on AI's Role in Academic Work</i>
    </p>
  </div>
</div>
<div id="modal48" class="modal">
  <div class="modal-content">
    <span class="close-modal" onclick="closeModal('modal48')">&times;</span>
    <h3><b>Dr Anna Baczko-Dombi, Faculty of Sociology, University of Warsaw</b></h3>
    <p>
    Anna Baczko-Dombi is a researcher and lecturer at the Faculty of Sociology, University of Warsaw, where she has been teaching since 2008. Her academic work is deeply intertwined with her teaching practice, particularly in active, experience-based formats such as workshops and research seminars. She co-created the “Digital Sociology” MA program and led it for four years. Her research focuses on educational decision-making and barriers in STEM learning, including studies on the social perception of mathematics. She has been actively involved as a co-creator in EU-fund educational projects (actiss-edu.eu, socialpolarisation.eu), developing courses based on social simulations to explore social phenomena. Drawing on her experience with MOOCs, she emphasizes clarity, accessibility, and learner autonomy. Passionate about bridging theory and practice, she encourages students to challenge disciplinary stereotypes and engage with complex topics in a hands-on way.
    <br><b>Title of presentation:</b> <br>
    <i>How Creating MOOCs Helped us Become Better Teachers: the Case for Integrating New Technologies in Everyday Educational Practices</i>
    </p>
  </div>
</div>



<!-- Skrypt modala -->
<script>
  function openModal(id) {
    document.getElementById(id).style.display = 'block';
  }

  function closeModal(id) {
    document.getElementById(id).style.display = 'none';
  }

  window.onclick = function(event) {
    const modals = document.querySelectorAll('.modal');
    modals.forEach(modal => {
      if (event.target === modal) {
        modal.style.display = "none";
      }
    });
  };
</script>
        </div>
    </div>
</div>     

<br><br>


<!-- Call -->
<h1 id="call" style="margin-top: 50px; font-weight: bold; font-size: 30px; margin-left: 10px;">
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

<!-- Sekcja call -->
<div class="topics-container">
        <div class="topic">
            <div class="topic-content-class">
                <p>
                <span class="lang-en hidden">DELab UW, on behalf of the Rector of the University of Warsaw, prof. Alojzy Nowak, invites academics together with students, administrators, practitioners and business leaders to join the interdisciplinary conference GenAI in Higher Education: New Perspectives<br>for Research and Teaching. This unique event will provide a platform for collaboration, fostering connections between researchers <br>and professionals to co-create knowledge, exchange experiences, and develop innovative ideas in this dynamic field.</span>
                </p>
                <span class="lang-pl">DELab UW, w imieniu Rektora Uniwersytetu Warszawskiego, prof. Alojzego Nowaka, zaprasza naukowców, studentów, pracowników administracyjnych, praktyków oraz liderów biznesu do udziału w interdyscyplinarnej konferencji GenAI in Higher Education: Nowe perspektywy dla badań i nauczania. To wyjątkowe wydarzenie stworzy platformę do współpracy, budowania relacji między badaczami a profesjonalistami, wspólnego tworzenia wiedzy, wymiany doświadczeń oraz rozwijania innowacyjnych pomysłów w tej dynamicznie rozwijającej się dziedzinie.
                </span>
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


<h1 id="location" style="margin-top: 50px; font-weight: bold; font-size: 30px; margin-left: 10px;">
    <span class="lang-pl"><b>Szczegóły lokalizacji</b></span>
    <span class="lang-en hidden"><b>Location details</b></span></h1>

<div class="about-section1">
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