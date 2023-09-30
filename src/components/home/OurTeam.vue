<template>
  <section class="team">
    <div class="container_team">
      <h1 class="heading" id="team">Meet Our Team</h1>
      <p class="caption">Para anggota kelompok 16 yang keren merupakan dalang di balik bagusnya web ini.</p>
      <div class="row">
        <div class="card">
          <div class="image">
            <img :src="zulfa" alt="zulfa" />
          </div>
          <div class="info">
            <h3>Zulfa Hafizh Kusuma</h3>
            <span>5027221038</span>
            <div class="icons">
              <a href="" class="fa-facebook" target=""><font-awesome-icon icon="fa-brands fa-facebook" size="sm" /></a>
              <a href="https://instagram.com/hafizhkusuma" class="fa-instagram" target="_blank"><font-awesome-icon icon="fa-brands fa-instagram" size="sm" /></a>
              <a href="https://www.linkedin.com/in/hafizh-k-b5ba41248/" class="fa-linkedin" target="_blank"><font-awesome-icon icon="fa-brands fa-linkedin" size="sm" /></a>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="card">
          <div class="image">
            <img :src="ilhan" alt="Ilhan" />
          </div>
          <div class="info">
            <h3>Ilhan Ahmad Syafa</h3>
            <span>5027221040</span>
            <div class="icons">
              <a href="" class="fa-facebook" target=""><font-awesome-icon icon="fa-brands fa-facebook" size="sm" /></a>
              <a href="https://instagram.com/ilhanahmads" class="fa-instagram" target="_blank"><font-awesome-icon icon="fa-brands fa-instagram" size="sm" /></a>
              <a href="https://www.linkedin.com/in/ilhan-ahmad-syafa-754810248/" class="fa-linkedin" target="_blank"><font-awesome-icon icon="fa-brands fa-linkedin" size="sm" /></a>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="card">
          <div class="image">
            <img :src="dito" alt="dito" />
          </div>
          <div class="info">
            <h3>M. Harvian Dito Syahputra</h3>
            <span>5027221039</span>
            <div class="icons">
              <a href="" class="fa-facebook" target=""><font-awesome-icon icon="fa-brands fa-facebook" size="sm" /></a>
              <a href="https://www.instagram.com/harviandt/" class="fa-instagram" target="_blank"><font-awesome-icon icon="fa-brands fa-instagram" size="sm" /></a>
              <a href="https://www.linkedin.com/in/muhammad-harvian-dito-syahputra-888993245/" class="fa-linkedin" target="_blank"><font-awesome-icon icon="fa-brands fa-linkedin" size="sm" /></a>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="card">
          <div class="image">
            <img :src="aras" alt="aras" />
          </div>
          <div class="info">
            <h3>Aras Rizky Ananta</h3>
            <span>5027221053</span>
            <div class="icons">
              <a href="" class="fa-facebook" target=""><font-awesome-icon icon="fa-brands fa-facebook" size="sm" /></a>
              <a href="" class="fa-instagram" target=""><font-awesome-icon icon="fa-brands fa-instagram" size="sm" /></a>
              <a href="https://www.linkedin.com/in/aras-rizky-ananta-0151261a4/" class="fa-linkedin" target="_blank"><font-awesome-icon icon="fa-brands fa-linkedin" size="sm" /></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import zulfa from "@/assets/images/zulfa.jpg";
import ilhan from "@/assets/images/Ilhan.jpg";
import dito from "@/assets/images/dito.jpg";
import aras from "@/assets/images/aras.png";

export default {
  name: "OurMission",
  props: {},

  data() {
    return {
      zulfa: zulfa,
      ilhan: ilhan,
      dito: dito,
      aras: aras,
    };
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@800&family=Poppins&display=swap");

.team {
  text-align: center;
  background-color: var(--biru);
}

.team .heading {
  color: var(--kuning);
  font-size: 64px;
  font-weight: 800;
  font-family: "Montserrat";
  margin-top: 7rem;
  padding-top: 100px;
}

.caption {
  color: var(--putih);
  font-size: 24px;
  font-family: "Poppins", sans-serif;
}

.team .row {
  display: inline-block;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.team .row .card {
  height: 27rem;
  width: 20rem;
  background-color: #fff;
  text-align: center;
  margin: 5rem 2rem;
  position: relative;
  overflow: hidden;
  transition: 0.5s;
  border-radius: 8%;
}

.team .row .card:hover {
  transform: scale(0.9);
  cursor: pointer;
}

.team .row .card .image {
  margin: 1rem 0;
  padding-top: 2rem;
}

.team .row .card .image img {
  height: 12rem;
  width: 12rem;
  border-radius: 50%;
  border: 0.5rem solid var(--biru);
  box-shadow: 0 0 0.5rem rgba(0, 0, 0, 0.3);
  object-fit: cover;
}

.team .row .card .info h3 {
  font-size: 18px;
  color: var(--biru);
  font-family: "Poppins", sans-serif;
  font-weight: bold;
}

.team .row .card .info span {
  font-size: 16px;
  color: var(--biru);
  font-family: "Poppins", sans-serif;
}

.team .row .card .info .icons a {
  margin-top: 4rem;
  padding-top: 0 1rem;
  font-size: 2rem;
  color: #333;
  align-items: center;
  justify-content: center;
  padding: 1rem;
}

.team .row .card .info .icons .fa-facebook,
.team .row .card .info .icons .fa-instagram,
.team .row .card .info .icons .fa-linkedin {
  margin: 0.001rem;
  transition: 0.5s;
}

.team .row .card .info .icons .fa-facebook:hover {
  color: #4267b2;
  text-decoration: none;
  transform: scale(0.9);
  cursor: pointer;
}

.team .row .card .info .icons .fa-instagram:hover {
  color: #c13584;
  text-decoration: none;
  transform: scale(0.9);
  cursor: pointer;
}

.team .row .card .info .icons .fa-linkedin:hover {
  color: #2867b2;
  text-decoration: none;
  transform: scale(0.9);
  cursor: pointer;
}

@media(max-width: 480px) {
  .team .heading {
    font-size: 30px;
    margin-top: 3rem;
    padding-top: 80px;
  }

  .caption {
    font-size: 16px;
    margin-bottom: 2rem;
    margin-right: 1rem;
    margin-right: 1rem;
  }
}

/* .team .row .card::before,
.team .row .card::after {
  content: "";
  position: absolute;
  border-radius: 50%;
  height: 13.5rem;
  width: 13.5rem;
  z-index: -1;
}

.team .row .card::before {
  background: linear-gradient(#00bfff, var(--biru));
  top: -6rem;
  right: -8rem;
}

.team .row .card::after {
  background: var(--kuning);
  bottom: -8rem;
  left: -6rem;
} */
</style>
