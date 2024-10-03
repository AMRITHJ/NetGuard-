<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="shortcut icon" type="image/x-icon" href="PIC/logo.png" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      href="https://cdn.jsdelivr.net/npm/remixicon@4.3.0/fonts/remixicon.css"
      rel="stylesheet"
    />
    
    <title>NeTGuard | Real-Time Malicious Website Detection</title>

    <style>
      @import url('https://fonts.googleapis.com/css2?family=Mulish:ital,wght@0,200..1000;1,200..1000&display=swap');

:root {
  --primary-color: #0011ff;
  --text-dark: #0f172a;
  --text-light: #475569;
  --extra-light: #f2f2f2;
  --white: #ffffff;
  --max-width: 1200px;
  --gradient: linear-gradient(to bottom, #0011ff, #ffffff);
  --hover-color: #fff; /* Text color on hover */
  --hover-background: #0011ff; /* Background color on hover */
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.section__container {
  max-width: var(--max-width);
  margin: auto;
  padding: 5rem 1rem;
}

.section__subheader {
  margin-bottom: 0.5rem;
  font-size: 1rem;
  font-weight: 600;
  color: var(--text-light);
  letter-spacing: 1px;
}

.section__header {
  font-size: 2.5rem;
  font-weight: 800;
  color: var(--text-dark);
}

.btn {
  padding: 0.75rem 1.5rem;
  outline: none;
  border: none;
  font-size: 1rem;
  color: var(--white);
  background-color: #0015ff;
  white-space: nowrap;
  border-radius: 4px;
  transition: 0.3s;
  cursor: pointer;
}

.btn:hover {
  background-color: #3c4286;
}

img {
  display: flex;
  width: 100%;
}

a {
  text-decoration: none;
  transition: 0.3s;
}

ul {
  list-style: none;
}

html,
body {
  scroll-behavior: smooth;
}

body {
  font-family: "Mulish", sans-serif;
}

header {
  position: relative;
}

header::before {
  position: absolute;
  content: "";
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.1));
  z-index: -1;
}

nav {
  position: fixed;
  isolation: isolate;
  width: 100%;
  z-index: 9;
}

.nav__header {
  padding: 1rem;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: var(--primary-color);
}

.nav__logo a {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--white);
  margin-left: -40px;
}

.nav__menu__btn {
  font-size: 1.5rem;
  color: var(--white);
  cursor: pointer;
}

.nav__links {
  position:absolute;
  top: 100;
  left: 0;
  width: 100%;
  padding: 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 2rem;
  background-color: var(--primary-color);
  transition: 0.5s;
  z-index: -1;
  transform: translateY(-100%);
}

.nav__links.open {
  transform: translateY(0);
}

.nav__links a {
  font-weight: 700;
  color: var(--white);
}

.nav__links .btn {
  padding: 0;
  background-color: transparent;
}

.nav__btns {
  display: none;
}

.header__container {
  display: grid;
  gap: 2rem 0;
  position: relative;
  isolation: isolate;
  overflow: hidden;
}

.header__container::before {
  position: absolute;
  content: "";
  top: 0;
  right: 0;
  width: 100%;
  height: 50%;
  background: var(--gradient);
  border-radius: 1rem 1rem 0.5rem 0.5rem;
  z-index: -1;
}

.header__content h1 {
  position: relative;
  isolation: isolate;
  margin-bottom: 2rem;
  font-size: 2.75rem;
  font-weight: 800;
  color: var(--text-dark);
  line-height: 3.25rem;
}

.header__content h1::before {
  position: absolute;
  content: "";
  left: 0;
  bottom: -1rem;
  height: 4px;
  width: 2rem;
  background-color: var(--primary-color);
}

.header__content p {
  margin-bottom: 2rem;
  font-weight: 500;
  color: var(--text-dark);
  line-height: 1.75rem;
}

.header__links {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.header__links img {
  max-width: 125px;
  border-radius: 5px;
  box-shadow: 5px 5px 20px #0000001a;
}

.steps__container :is(.section__subheader, .section__header) {
  text-align: center;
}

.steps__grid {
  margin-top: 4rem;
  display: grid;
  gap: 2rem;
}

.steps__card {
  text-align: center;
}

.steps__card span {
  display: inline-block;
  margin-bottom: 2rem;
  padding: 10px 17px;
  font-size: 1.75rem;
  color: var(--primary-color);
  border-radius: 5px;
  background-color: var(--extra-light);
  border: 4px solid var(--white);
  box-shadow: 5px 5px 20px #0000001a;
}

.steps__card:hover span {
  padding: 14px 21px;
  background: var(--gradient);
  color: var(--white);
  border: none;

  transform: translateY(-5px); /* Move up on hover */
  box-shadow: 5px 10px 25px #0011ff; /* Increase shadow on hover */
  color: var(--hover-color); /* Change text color on hover */
  background-color: var(--hover-background); /* Change background color on hover */
}




.steps__card h4 {
  margin-bottom: 1rem;
  font-size: 1.25rem;
  font-weight: 800;
  color: var(--text-dark);
}

.steps__card p {
  color: var(--text-light);
  line-height: 1.75rem;
}

.service__container {
  display: grid;
  gap: 2rem;
  overflow: hidden;
}

.service__card span {
  display: inline-block;
  margin-bottom: 2rem;
  padding: 10px 17px;
  font-size: 1.75rem;
  color: var(--primary-color);
  border-radius: 5px;
  background-color: var(--extra-light);
  border: 4px solid var(--white);
  box-shadow: 5px 5px 20px rgb(0, 0, 0);
}

.service__card:hover span {
  padding: 14px 21px;
  background: var(--gradient);
  color: var(--white);
  border: none;

  transform: translateY(-5px); /* Move up on hover */
  box-shadow: 5px 10px 25px #0011ff; /* Increase shadow on hover */
  color: var(--hover-color); /* Change text color on hover */
  background-color: var(--hover-background); /* Change background color on hover */
}


.service__card {
  margin-top: 2rem;
  display: grid;
  gap: 2rem;
}

.service__card li {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.service__card li span {
  padding: 12px 15px;
  font-size: 1.5rem;
  color: var(--primary-color);
  background-color: var(--extra-light);
  border: 4px solid var(--white);
  border-radius: 5px;
  box-shadow: 5px 5px 20px #0000001a;
}

.service__card h4 {
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
  font-weight: 700;
  color: var(--text-dark);
}

.service__card p {
  color: var(--text-light);
  line-height: 1.75rem;
}

.experience__container :is(.section__subheader, .section__header) {
  text-align: center;
  max-width: 600px;
  margin-inline: auto;
}

.experience__content {
  max-width: 1024px;
  margin-inline: auto;
  margin-top: 4rem;
  position: relative;
  isolation: isolate;
}

.experience__content img {
  max-width: 300px;
  margin-inline: auto;
  opacity: 0.5;
}

.experience__card {
  position: absolute;
  max-width: 200px;
}

.experience__card span {
  display: inline-block;
  margin-bottom: 0.5rem;
  padding: 10px 13px;
  font-size: 1.5rem;
  color: var(--primary-color);
  background-color: var(--extra-light);
  border: 4px solid var(--white);
  border-radius: 5px;
  box-shadow: 5px 5px 20px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s, color 0.3s, background-color 0.3s; /* Add transition for color and background */
}

.experience__card span:hover {
  transform: translateY(-5px); /* Move up on hover */
  box-shadow: 5px 10px 25px #0011ff; /* Increase shadow on hover */
  color: var(--hover-color); /* Change text color on hover */
  background-color: var(--hover-background); /* Change background color on hover */
}


.experience__card h4 {
  font-size: 1rem;
  font-weight: 700;
  color: var(--text-dark);
}

.experience__card:nth-child(1) {
  top: 1rem;
  left: 1rem;
}

.experience__card:nth-child(2) {
  top: 50%;
  left: -2rem;
  transform: translateY(-40%);
}

.experience__card:nth-child(3) {
  bottom: -1rem;
  left: 1rem;
}

.experience__card:nth-child(4) {
  top: 1rem;
  right: 1rem;
  text-align: right;
}

.experience__card:nth-child(5) {
  top: 50%;
  right: -3rem;
  transform: translateY(-50%);
  text-align: right;
}

.experience__card:nth-child(6) {
  bottom: -1rem;
  right: 1rem;
  text-align: right;
}

.bot{
  margin-top: -100px;
}

.download__container {
  overflow: hidden;
}

.download__grid {
  display: grid;
  padding: 5rem 1rem;
  background: var(--gradient);
  border-radius: 1rem;
}

.download__image {
  display: none;
}

.download__content .section__header {
  margin-bottom: 1rem;
  color: var(--white);
}

.download__content p {
  margin-bottom: 2rem;
  color: var(--extra-light);
  line-height: 1.75rem;
}

.download__links {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.download__links img {
  max-width: 125px;
  border-radius: 5px;
  box-shadow: 5px 5px 20px rgba(0, 0, 0, 0.1);
}

.footer__container {
  display: grid;
  gap: 4rem 2rem;
  border-bottom: 1px solid var(--text-light);
}

.footer__col h4 {
  margin-bottom: 2rem;
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--text-dark);
}

.footer__links {
  display: grid;
  gap: 1rem;
}

.footer__links a {
  font-weight: 600;
  color: var(--text-light);
}

.footer__links a:hover {
  color: var(--primary-color);
}

.footer__bar {
  padding-block: 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-direction: column;
  gap: 1rem;
  flex-wrap: wrap;
}

.footer__bar h4 {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--text-dark);
}

.footer__bar p {
  font-weight: 500;
  color: var(--text-light);
  text-align: center;
}

.footer__socials {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.footer__socials a {
  display: inline-block;
  padding: 8px 10px;
  font-size: 1rem;
  color: var(--text-dark);
  border-radius: 100%;
  box-shadow: 5px 5px 20px rgba(0, 0, 0, 0.1);
}

.footer__socials a:hover {
  color: var(--white);
  background: var(--gradient);
}

@media (width > 540px) {
  .steps__grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .footer__container {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (width > 768px) {
  header::before {
    height: calc(100% - 4rem);
  }

  nav {
    position: static;
    padding-block: 2rem;
    padding-inline: 1rem;
    max-width: var(--max-width);
    margin-inline: auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 2rem;
  }

  .nav__header {
    flex: 1;
    padding: 0;
    background-color: transparent;
  }

  .nav__logo a {
    font-weight: 800;
    color: var(--text-dark);
  }

  .nav__menu__btn {
    display: none;
  }

  .nav__links {
    position: static;
    padding: 0;
    width: fit-content;
    flex-direction: row;
    background-color: transparent;
    transform: none;
  }

  .nav__links a {
    padding-block: 5px;
    color: var(--text-dark);
    border-bottom: 2px solid transparent;
  }

  .nav__links a:hover {
    border-color: var(--primary-color);
  }

  .nav__links__btn {
    display: none;
  }

  .nav__btns {
    display: flex;
    flex: 1;
    align-items: center;
    justify-content: flex-end;
  }

  .nav__btns .btn__primary {
    color: var(--text-dark);
    background-color: transparent;
  }

  .header__container {
    grid-template-columns: repeat(5, 1fr);
    align-items: center;
  }

  .header__container::before {
    right: 5rem;
    width: calc(50% - 4rem);
    height: 100%;
  }

  .header__image {
    grid-column: 3/6;
  }

  .header__content {
    grid-area: 1/1/2/3;
  }

  .steps__grid {
    grid-template-columns: repeat(3, 1fr);
  }

  .service__container {
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
  }

  .experience__content img {
    opacity: 5;
  }

  .experience__card:nth-child(1) {
    left: 5rem;
  }

  .experience__card:nth-child(3) {
    left: 5rem;
  }

  .experience__card:nth-child(4) {
    right: 5rem;
  }

  .experience__card:nth-child(6) {
    right: 5rem;
  }

  .download__grid {
    margin-block: 4rem;
    padding-inline: 2rem;
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
  }

  .download__image {
    display: flex;
    position: relative;
    isolation: isolate;
  }

  .download__image img {
    position: absolute;
    max-width: 300px;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    filter: drop-shadow(0 0 20px rgba(0, 0, 0, 0.2));
  }

  .footer__container {
    grid-template-columns: repeat(4, 1fr);
  }

  .footer__bar {
    flex-direction: row;
  }

  .footer__bar :is(h4, .footer__socials) {
    flex: 1;
  }

  .footer__socials {
    justify-content: flex-end;
  }
}



* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #ffffff;
}


header {
  background-color: rgb(243, 243, 245);
  padding: 1rem 0;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.nav__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

.nav__logo a {
  color: rgb(0, 0, 0);
  text-decoration: none;
  font-size: 1.5rem;
  font-weight: bold;
}

.nav__menu__btn {
  display: none;
  font-size: 2rem;
  color: rgb(3, 0, 0);
}

.nav__links {
  list-style: none;
  display: flex;
  align-items: center;
}

.nav__links li {
  margin-left: 2rem;
}

.nav__links a {
  color: rgb(0, 0, 0);
  text-decoration: none;
  font-size: 1rem;
}

.nav__links__btn .btn {
  background-color: white;
  color: rgb(40, 5, 238);
  border: none;
  padding: 0.5rem 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.nav__links__btn .btn:hover {
  background-color: #f0f0f0;
}

.nav__btns {
  display: none;
}

.btn__primary {
  background-color: white;
  color: rgb(8, 52, 248);
  padding: 0.5rem 1rem;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn__secondary {
  background-color: transparent;
  color: white;
  padding: 0.5rem 1rem;
  border: 1px solid white;
  cursor: pointer;
  transition: background-color 0.3s ease, color 0.3s ease;
}

.btn__primary:hover {
  background-color: #f0f0f0;
}

.btn__secondary:hover {
  background-color: white;
  color: rgb(4, 60, 245);
}


.search {
  background-color: white;
  text-align: center;
  padding: 5rem 0;
}

.search-content h1 {
  font-size: 2.5rem;
  margin-bottom: 2rem;
}

.search-content form {
  display: flex;
  justify-content: center;
  margin-bottom: 2rem;
}

.search-content input[type="text"] {
  padding: 0.5rem;
  font-size: 1rem;
  border: 1px solid #ddd;
  border-radius: 5px 0 0 5px;
}

.search-content button {
  padding: 0.5rem 1rem;
  font-size: 1rem;
  border: none;
  background-color: rgb(0, 47, 255);
  color: white;
  cursor: pointer;
  border-radius: 0 5px 5px 0;
  transition: background-color 0.3s ease;
}

.search-content button:hover {
  background-color: rgb(25, 0, 255);
}

.info-cards {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.card {
  background-color: rgb(4, 0, 255);
  color: white;
  padding: 1rem;
  border-radius: 5px;
  width: 150px;
  text-align: center;
}


@media (max-width: 768px) {
  .nav__menu__btn {
      display: block;
  }
  
  .nav__links {
      display: none;
      flex-direction: column;
      background-color: orange;
      position: absolute;
      top: 60px;
      right: 0;
      width: 100%;
      text-align: right;
      padding-right: 1rem;
  }

  .nav__links li {
      margin: 1rem 0;
  }

  .nav__links__btn {
      display: none;
  }

  .nav__btns {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding-top: 1rem;
  }

  .nav__btns .btn {
      margin-top: 1rem;
      width: 80%;
  }
}

    </style>
  </head>
  <body>
    <header>
      <nav>
        <div class="nav__header">
          <div class="nav__logo">
            <a href="#">NeTGuard</a>
          </div>
          <div class="nav__menu__btn" id="menu-btn">
            <i class="ri-menu-2-line"></i>
          </div>
        </div>
        <ul class="nav__links" id="nav-links">
          <li><a href="#home">Home</a></li>
          <li><a href="#rules">Rules</a></li>
          <li><a href="#service">service</a></li>
          <li><a href="#exp">Experience</a></li>
          <li><a href="#search">Prediction</a></li>
          <li><a href="#download">Download</a></li>
        </ul>
      </nav>
      <div class="section__container header__container" id="home">
        <div class="header__image">
          <img src="PIC/1bot.png" alt="header" />
        </div>
        <div class="header__content">
          <h1>Looking for a safe URL browsing?</h1>
          <p>
            Discover unparalleled security with NetGuard's real-time detection
            of malicious websites. Ensure every click is safe, protecting you
            from online dangers instantly.
          </p>
          <div class="header__links">
            <a href="#">
              <img src="PIC/AS.jpeg" alt="app store" />
            </a>
            <a href="#">
              <img src="PIC/GP.jpeg" alt="play" />
            </a>
          </div>
        </div>
      </div>
    </header>

    <section class="section__container steps__container" id="rules">
      <p class="section__subheader">HOW IT WORKS</p>
      <h2 class="section__header">Following 4 working steps</h2>
      <div class="steps__grid">
        <div class="steps__card">
          <span><i class="ri-puzzle-line"></i></span>
          <h4>Use our Website / Extension</h4>
          <p>Select your desired platform for URL browsing.</p>
        </div>
        <div class="steps__card">
          <span><i class="ri-search-eye-line"></i></span>
          <h4>Input your link</h4>
          <p>Please enter your desired link into the search bar for analyzing it.</p>
        </div>
        <div class="steps__card">
          <span><i class="ri-file-warning-line"></i></span>
          <h4>Pop-up</h4>
          <p>A Pop-up will be shown on your screen to continue or a warning Pop-up for alerting the user about the malicious website.</p>
        </div>
        <div class="steps__card">
          <span><i class="ri-bookmark-3-fill"></i></span>
          <h4>Happy Browsing</h4>
          <p>Once the URL has been returned as valid, it will redirect the user to their desired website.</p>
        </div>
      </div>
    </section>

    <section class="section__container service__container" id="service">
      <div class="service__image">
        <img src="PIC/3bot.png" alt="service" />
      </div>
      <div class="service__content">
        <p class="section__subheader">ELITE ASSISTANCE</p>
        <h2 class="section__header">
          Experience unparalleled protection with NetGuard's advanced detection capabilities.
        </h2>
        <ul >
          <li class="service__card">
            <span><i class="ri-price-tag-3-fill"></i></span>
            <div>
              <h4>Seamless Integration Across Devices</h4>
              <p>NetGuard’s browser extension provides seamless, cross-device protection with easy management and alerts.</p>
            </div>
          </li>
          <li class="service__card">
            <span><i class="ri-wallet-fill"></i></span>
            <div>
              <h4>Real-Time Malicious Website Detection</h4>
              <p>We offer real-time protection by analyzing websites for threats, ensuring every click is safe from phishing, malware, and other online dangers.</p>
            </div>
          </li>
          <li class="service__card">
            <span><i class="ri-customer-service-fill"></i></span>
            <div>
              <h4>Support 24/7</h4>
              <p>Our dedicated team is available 24/7 to assist you with any questions or concerns, ensuring a smooth browsing experience.</p>
            </div>
          </li>
        </ul>
      </div>
    </section>

    <section class="section__container experience__container" id="exp">
      <p class="section__subheader">USER EXPERIENCE</p>
      <h2 class="section__header">We are ensuring the best user experience</h2>
      <div class="experience__content">
        <div class="experience__card">
          <span><i class="ri-price-tag-3-fill"></i></span>
          <h4>Seamless Integration</h4>
        </div>
        <div class="experience__card">
          <span><i class="ri-money-rupee-circle-fill"></i></span>
          <h4>Real-Time Alerts</h4>
        </div>
        <div class="experience__card">
          <span><i class="ri-bank-card-fill"></i></span>
          <h4>User-Friendly Interface</h4>
        </div>
        <div class="experience__card">
          <span><i class="ri-award-fill"></i></span>
          <h4>Customizable Settings</h4>
        </div>
        <div class="experience__card">
          <span><i class="ri-customer-service-2-fill"></i></span>
          <h4> Comprehensive Support</h4>
        </div>
        <div class="experience__card">
          <span><i class="ri-car-fill"></i></span>
          <h4>Minimal Impact</h4>
        </div>
        <img src="PIC/2bot.png" alt="experience"  width="500" height="300"/>
      </div>
    </section>

    <section class="search" id="search">
      <div class="search-content">
        <h1>Phishing Website Detector</h1>
        <form id="detector-form">
          <input type="text" id="url-input" placeholder="Enter URL" />
          <button type="button" id="predict-button">Predict</button>
        </form>
        <div class="info-cards">
          <div class="card">
            <p>If you suspect deceit, hit delete</p>
          </div>
          <div class="card">
            <p>Think before you click</p>
          </div>
          <div class="card">
            <p>Don't take the bait</p>
          </div>
        </div>
      </div>
    </section>

    <section class="section__container download__container" id="download">
      <div class="download__grid">
        <div class="download__content">
          <h2 class="section__header">Download the free NeTGuard extension</h2>
          <p>Download the NeTGuard extension to manage your web search, find access to 24/7 support, all from your mobile device.</p>
          <div class="download__links">
            <a href="#">
              <img src="PIC/AS.jpeg" alt="app store" />
            </a>
            <a href="#">
              <img src="PIC/GP.jpeg" alt="play" />
            </a>
          </div>
        </div>
        <div class="download__image">
          <img src="PIC/ext.png" alt="download" />
        </div>
      </div>
    </section>
    <script>
      const menuBtn = document.getElementById("menu-btn");
const navLinks = document.getElementById("nav-links");
const menuBtnIcon = menuBtn.querySelector("i");

menuBtn.addEventListener("click", (e) => {
  navLinks.classList.toggle("open");

  const isOpen = navLinks.classList.contains("open");
  menuBtnIcon.setAttribute("class", isOpen ? "ri-close-line" : "ri-menu-2-line");
});

navLinks.addEventListener("click", (e) => {
  navLinks.classList.remove("open");
  menuBtnIcon.setAttribute("class", "ri-menu-2-line");
});

const scrollRevealOption = {
  distance: "50px",
  origin: "bottom",
  duration: 1000,
};

ScrollReveal().reveal(".header__image img", {
  ...scrollRevealOption,
  origin: "right",
});
ScrollReveal().reveal(".header__content h1", {
  ...scrollRevealOption,
  delay: 500,
});
ScrollReveal().reveal(".header__content p", {
  ...scrollRevealOption,
  delay: 1000,
});
ScrollReveal().reveal(".header__links", {
  ...scrollRevealOption,
  delay: 1500,
});

ScrollReveal().reveal(".steps__card", {
  ...scrollRevealOption,
  interval: 500,
});

ScrollReveal().reveal(".service__image img", {
  ...scrollRevealOption,
  origin: "left",
});
ScrollReveal().reveal(".service__content .section__subheader", {
  ...scrollRevealOption,
  delay: 500,
});
ScrollReveal().reveal(".service__content .section__header", {
  ...scrollRevealOption,
  delay: 1000,
});
ScrollReveal().reveal(".service__list li", {
  ...scrollRevealOption,
  delay: 1500,
  interval: 500,
});

ScrollReveal().reveal(".experience__card", {
  duration: 1000,
  interval: 500,
});

ScrollReveal().reveal(".download__image img", {
  ...scrollRevealOption,
  origin: "right",
});
ScrollReveal().reveal(".download__content .section__header", {
  ...scrollRevealOption,
  delay: 500,
});
ScrollReveal().reveal(".download__content p", {
  ...scrollRevealOption,
  delay: 1000,
});
ScrollReveal().reveal(".download__links", {
  ...scrollRevealOption,
  delay: 1500,
});

    </script>

  </body>
</html>
