<template>
  <div class="card">
    <div class="card-image"></div>
    <div class="card-content">
      <h2 class="heading">
        Shift the overall look and feel by adding these wonderful touches to
        furniture in your home
      </h2>
      <p class="paragraph">
        Ever been in a room and felt like something was missing? Perhaps it felt
        slightly bare and uninviting. I’ve got some simple tips to help you make
        any room feel complete.
      </p>
      <div class="user-details">
        <img
          src="../assets/images/avatar-michelle.jpg"
          alt="Woman's avatar photo"
          class="user-avatar"
        />
        <div class="user-text">
          <h3>Michelle Appleton</h3>
          <p>28 Jun 2020</p>
        </div>
        <a href="#" class="share-btn">
          <svg xmlns="http://www.w3.org/2000/svg" width="15" height="13">
            <path
              fill="#6E8098"
              d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"
            />
          </svg>
        </a>

        <div class="share">
          <p class="share-text">SHARE</p>
          <img src="../assets/images/icon-facebook.svg" alt="facebook" />
          <img src="../assets/images/icon-twitter.svg" alt="twitter" />
          <img src="../assets/images/icon-pinterest.svg" alt="pinterest" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
h2,
h3 {
  color: var(--color-Very-Dark-Grayish-Blue);
}

.heading {
  font-size: 1.3rem;
  font-weight: 700;
}
.paragraph {
  color: var(--color-Desaturated-Dark-Blue);
}

p {
  color: var(--color-Grayish-Blue);
}

.card {
  width: 62em;
  height: auto;
  display: flex;
  position: absolute;
  top: 50%;
  left: 50%;
  background-color: #fff;
  transform: translate(-50%, -50%);
  border-radius: 6px;
  overflow: hidden;
  text-align: left;
  box-shadow: 0 14px 15px rgba(190, 190, 190, 0.7);
}

.card-content {
  padding: 40px;
}

.paragraph {
  font-size: 14px;
  margin: 30px 0;
}

.card-image {
  width: 100%;
  background-image: url("../assets/images/drawers.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}

.user-details {
  display: flex;
  align-items: center;
  margin-top: 20px;
}

.user-avatar {
  width: 60px;
  border-radius: 50%;
  margin-right: 15px;
}

.user-details a {
  background-color: var(--color-Light-Grayish-Blue);
  padding: 10px 12px;
  border-radius: 50%;
  margin-left: auto;
  cursor: pointer;
}

.share-text {
  letter-spacing: 2px;
}

.share {
  background-color: hsl(217, 19%, 35%);
  border-radius: 8px;
  padding: 10px 25px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: absolute;
  right: 1%;
  bottom: 32%;
  opacity: 0;
  visibility: hidden;
  box-shadow: 26px 19px 50px -16px hsla(217, 19%, 35%, 0.616);
  transition: all 0.5s ease-in-out;
  z-index: 1;
}
.share::after {
  content: "";
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-top: 10px solid hsl(217, 19%, 35%);
  position: absolute;
  right: 20%;
  transform: translate(-50%);
  bottom: -9px;
  z-index: 1;
}
.share p {
  letter-spacing: 5px;
  font-size: 12px;
  color: hsl(212, 23%, 69%);
}
.share img {
  width: 18px;
  cursor: pointer;
  margin: 0 6px;
}

.active {
  opacity: 1;
  visibility: visible;
}

/* Responsive */
@media (max-width: 768px) {
  .card {
    width: 80%;
    height: auto;
    display: grid;
    align-content: space-between;
    padding-bottom: 15px;
  }

  .card-image {
    width: 100%;
    height: 100%;
    margin-bottom: 30em;
  }

  .card-content h2 {
    font-size: 1.2em;
  }

  .user-avatar {
    position: absolute;
    bottom: 0.9rem;
    left: 2rem;
  }

  .user-text {
    position: absolute;
    bottom: 1.6rem;
    left: 6.5rem;
  }

  .share {
    width: 100%;
    right: 0;
    bottom: 0;
    justify-content: center;
    padding: 25px;
  }
  .share p {
    justify-self: end;
  }
  .share img {
    align-self: center;
  }
  .share::after {
    display: none;
  }
  .share-btn {
    z-index: 3;
    position: absolute;
    bottom: 1.4rem;
    right: 2rem;
  }
}
</style>
