<template>
  <div class="container">
    <div class="column photo-area">
      <img src="/photo.png" alt="Vadym Riazantsev">
    </div>

    <div class="column info-area">

      <div class="content">
        <h5>Ruby developer</h5>

        <h2>Vadym Riazantsev</h2>

        <p>
          Creator of <a href="https://github.com/vrtsev/Telegrammer">Telegrammer bot manager application</a>, mentor, in love with Ruby lang, Vue.js enthusiast. Write clean, scalable code.
          Explore new technologies, experiment with code-libraries, architecture and performance
        </p>

        <div class="social-area">
          <h3>Follow Me</h3>

          <ul class="list">
            <li><a href="https://github.com/vrtsev/"><i class="fa fa-github"></i></a></li>
            <li><a href="https://www.linkedin.com/in/vrtsev/"><i class="fa fa-linkedin"></i></a></li>
            <li><a href="mailto:v.rtsev@gmail.com"><i class="fa fa-envelope"></i></a></li>
          </ul>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  layout: 'landing',
}
</script>

<style>
.container {
  background-color: #1f1f1f;
  color: #acb0b5;
  height: 100%;
  display: flex;
  flex-direction: row;
}

.column {
  width: 100%;
}

.column.photo-area {
  flex: 0;
}

.column.info-area {
  flex: 1;
  overflow-y: auto;
}

.column.photo-area img {
  display: block;
  height: 100%;
}

.column.info-area .content {
  margin-left: 10%;
  margin-right: 10%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.social-area .list {
  list-style: none;
  padding: 0;
}

.social-area .list li {
  margin-right: 17px;
  display: inline-block;
}

.social-area .list li a {
  color: #9e9e9e;
  font-size: 30px;
  transition: all 300ms linear 0s;
}

.social-area .list li a:hover {
  color: #ffffff;
  text-decoration: underline;
}

/* TYPOGRAPHY */
.info-area .content h5 {
  color: #787878;
  font-size: 0.9em;
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  letter-spacing: 2.1px;
  margin-bottom: 20px;
}

.info-area .content h2 {
  margin-top: 0px;
  font-size: 2.5em;
  font-weight: bold;
  font-family: "Heebo", sans-serif;
  line-height: 54px;
  text-transform: uppercase;
  margin-bottom: 20px;
}

.info-area .content p {
  color: #787878;
  font-family: "Roboto", sans-serif;
  max-width: 680px;
  font-size: 1em;
  line-height: 26px;
}

.info-area .content p a {
  color: #d1d1d1;
}

.social-area h3 {
  font-size: 1.8em;
  font-family: "Heebo", sans-serif;
  font-weight: bold;
}
/* END OF TYPOGRAPHY */

@media screen and (max-aspect-ratio: 10/8) {
  .container {
    flex-direction: column;
  }

  .column.photo-area img {
    width: 100%;
  }

  .column.info-area {
    flex: 1;
    height: initial;
    overflow-y: initial;
  }
}

@media screen and (max-height: 400px) {
  .column.info-area .content {
    justify-content: initial;
  }
}
</style>

