<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <script src="https://unpkg.com/htmx.org@1.5.0"
    integrity="sha384-oGA+prIp5Vchu6we2YkI51UtVzN9Jpx2Z7PnR1I78PnZlN8LkrCT4lqqqmDkyrvI"
    crossorigin="anonymous"></script>
    <link href="{% static 'css/style.css' %}" rel="stylesheet">
    <meta property="og:image" content="">
    <link rel="icon" type="image/x-icon" href="{% static 'images/logo.png' %}">
    <link href='https://unpkg.com/boxicons@2.0.7/css/boxicons.min.css' rel='stylesheet'>
    <link href="https://fonts.googleapis.com/css2?family=Almarai:wght@300;400;700;800&family=Cairo:wght@200;400;600;700&family=El+Messiri:wght@500;700&family=Tajawal:wght@300;400;500;700&display=swap" rel="stylesheet">
    <title>DOVER</title>
      <meta property="og:title" content="">
      <meta property="og:description" content="">
      <meta property="og:url" content="">
  </head>
  <style>
    /* GOOGLE FONTS */
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;900&display=swap");
/* VARIABLES CSS */
:root {
  --header-height: 3.5rem;
  /* Colors */
  --hue: 14;
  --first-color: #5D688D;
  --first-color-alt: hsl(var(--hue), 91%, 50%);
  --title-color: hsl(var(--hue), 4%, 100%);
  --text-color: hsl(var(--hue), 4%, 85%);
  --text-color-light: hsl(var(--hue), 4%, 55%);
  /*Red gradient*/
  --body-color: linear-gradient(90deg, #D39397, #5D688D);
  --container-color: linear-gradient(136deg, #D39397, #5D688D);
  --sub: #ffffff;
  /* Font and typography */
  --body-font: "Poppins", sans-serif;
  --biggest-font-size: 2rem;
  --h1-font-size: 1.5rem;
  --h2-font-size: 1.25rem;
  --h3-font-size: 1rem;
  --normal-font-size: 0.938rem;
  --small-font-size: 0.813rem;
  --smaller-font-size: 0.75rem;
  /* Font weight */
  --font-medium: 500;
  --font-semi-bold: 600;
  --font-black: 900;
  /* Margenes Bottom */
  --mb-0-25: 0.25rem;
  --mb-0-5: 0.5rem;
  --mb-0-75: 0.75rem;
  --mb-1: 1rem;
  --mb-1-5: 1.5rem;
  --mb-2: 2rem;
  --mb-2-5: 2.5rem;
  /* z index */
  --z-tooltip: 10;
  --z-fixed: 100;
}
/* Responsive typography */
@media screen and (min-width: 992px) {
  :root {
    --biggest-font-size: 4rem;
    --h1-font-size: 2.25rem;
    --h2-font-size: 1.5rem;
    --h3-font-size: 1.25rem;
    --normal-font-size: 1rem;
    --small-font-size: 0.875rem;
    --smaller-font-size: 0.813rem;
  }
}
/* BASE */
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
html {
  scroll-behavior: smooth;
}
body {
  margin: var(--header-height) 0 0 0;
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
  background: var(--body-color);
  color: var(--text-color);
  transition: 0.3s;
}
h1,
h2,
h3,
h4 {
  color: var(--title-color);
  font-weight: var(--font-semi-bold);
}
ul {
  list-style: none;
}
a {
  text-decoration: none;
}
img {
  max-width: 100%;
  height: auto;
}
button,
input {
  border: none;
  outline: none;
}
button {
  cursor: pointer;
  font-family: var(--body-font);
  font-size: var(--normal-font-size);
}


/* LAYOUT */
.container {
  max-width: 968px;
  margin-left: var(--mb-1-5);
  margin-right: var(--mb-1-5);
}
@media screen and (max-width: 400px) {
    .container {
            padding-bottom: 100px;
  margin-top: -50px;
    }
}
@media screen and (min-width: 992px) {

.grid {
  display: grid;
  height: auto;
    height: 95vh;
  align-items: center;

}
}



/* HOME */

.home__group {
  display: grid;
  position: relative;
  padding-top: 100px;
  padding-bottom: 50px
}

.home__indicator {
  width: 8px;
  height: 8px;
  background-color: var(--title-color);
  border-radius: 50%;
  position: absolute;
  top: 70px;
  right: 10px;
}
.home__indicator::after {
  content: "";
  position: absolute;
  width: 1px;
  height: 48px;
  background-color: var(--title-color);
  top: -50px;
  right: 45%;
}
.home__details-img {
  position: absolute;
  right: 5px;
}
.home__details-title,
.home__details-subtitle {
  display: block;
  font-size: var(--small-font-size);
  text-align: right;
}
.home__subtitle {
  font-size: var(--h3-font-size);
  color: var(--sub);
  text-transform: uppercase;
  margin-bottom: 30px;
}
.pumpkin__subtitle {
  font-size: var(--h3-font-size);
  color: #ffffff;
  text-transform: uppercase;
  margin-bottom: 10px;
}
.home__title {
  font-size: var(--biggest-font-size);
  font-weight: var(--font-black);
  line-height: 109%;
  margin-bottom: var(--mb-1);
}
.home__description {
  margin-bottom: var(--mb-1);
}
.home__buttons {
  display: flex;
  justify-content: space-between;
  margin-top: 50px;
}

/* BUTTONS */


.book__now {
  display: inline-block;
  transition: 0.3s;
  width: 150px;
}
.book__now:hover {
  transform: scale(1.2);
}


.button--link {
  color: var(--title-color);
}
.button--flex {
  display: inline-flex;
  align-items: center;
  column-gap: 5px;
}


/* SCROLL BAR */
::-webkit-scrollbar {
  width: 0.6rem;
  background: #413e3e;
}
::-webkit-scrollbar-thumb {
  background: #272525;
  border-radius: 0.5rem;
}
/* For small devices */

@media screen and (min-width: 767px) {
  body {
    margin: 0;
  }
  .home__content {
    padding: 50px 50px;
    grid-template-columns: repeat(2, 1fr);
    gap: 40px;
  }


  
}
/* For large devices */
@media screen and (min-width: 992px) {
  .container {
        margin-left: auto;
        margin-right: auto;
        align-items: center;
  }


  .home__group {
    padding-top: 0;
  }
  .home__img {
    height: 400px;
    transform: translateY(-3rem);
  }
  .home__indicator {
    top: initial;
    right: initial;
    bottom: 15%;
    left: 45%;
  }
  .home__indicator::after {
    top: 0;
    height: 75px;
  }
  .home__details-img {
    bottom: 0;
    right: 58%;
  }
  .home__title {
    margin-bottom: var(--mb-1-5);
  }
  .home__description {
    margin-bottom: var(--mb-2-5);
    padding-right: 2rem;
  }

}




  </style>
  <body>

  <main class="main">

    <!-- HOME -->
    
    <section class="home container" id="home">

          <div class='navbar'>
          <img src="https://dover.elettihad.ly/wp-content/uploads/2024/05/Group-12sdfsdfsdf3.png" style="width: 150px; margin: 10px 5px;">
      </div>
          <!-- HOME SLIDER 1 -->
          <section class="swiper-slide">
            <div class="home__content grid">
              <div class="home__group">
                <img style="width: 400px; margin: auto;" src="https://dover.elettihad.ly/wp-content/uploads/2024/05/Grosdfsfup-147-scaled.webp" alt="" class="home__img">
                <div class="home__indicator"></div>
                <div class="home__details-img">
                  <h4 class="home__details-title">Write Email</h4>
                  <span class="home__details-subtitle">Hello@Dover.ly</span>
                </div>
              </div>
              <div class="home__data">
                <h3 class="pumpkin__subtitle">Just Brilliant, with</h3>
                <h1 class="home__title">Dover <br> You'll Not Over!! </h1>
                <p class="home__description">Hi I’m Reiza, people call me “The Labu” currently I’m trying to learn something new, building my own bike with parts only made from Malaysia. </p>
                <div class="home__buttons">
                  <a href="https://www.instagram.com/direct/t/17847519126191982" target="_blank" class="book__now">
                    <img src="https://dover.elettihad.ly/wp-content/uploads/2024/05/ezgif.com-svg-to-png-converter-2-1.png" alt="" />
                  </a>
                  <a href="https://www.instagram.com/dover.ly/" target="_blank" class="button--link button--flex"><i class='bx bxl-instagram-alt' style="font-size: 20px"></i>Follow Us 
                  </a>
                </div>
              </div>
            </div>
          </section>
        </div>
        <div class="swiper-pagination"></div>
      </div>
    </section>
      
  </body>
</html>
