<!-- eslint-disable vuejs-accessibility/click-events-have-key-events -->
<!-- eslint-disable quotes -->
<!-- eslint-disable vuejs-accessibility/form-control-has-label -->
<!-- eslint-disable vuejs-accessibility/label-has-for -->
<!-- eslint-disable max-len -->
<template>
  <main class="main">
    <nav class="nav">
      <div class="nav__logo">
        <img src="./assets/icons/Bold/l.png" class="nav__logo--1" alt="logo" />
        <img src="./assets/icons/Bold/heart.png" class="nav__logo--2" alt="logo" />
        <img src="./assets/icons/Bold/yalbaze.png" class="nav__logo--3" alt="logo" />
      </div>
      <div>
        <img src="./assets/icons/priority-btn.png" class="nav__link" alt="">
      </div>
    </nav>
    <img
      src="./assets/icons/ellipse/Ellipse-39.png"
      class="header__ellipse-39 header__ellipse"
      alt="ellipse-39"
    />

    <section class="header">
      <div class="header__section">
        <img src="./assets/icons/stars/Star-2.png" class="header__star-2" alt="star-2" />
        <img
          src="./assets/icons/ellipse/Ellipse-37.png"
          class="header__ellipse-37"
          alt="ellipse-37"
        />
        <h1>Turn your best customers into <span>Loyal fans</span></h1>
        <img src="./assets/icons/stars/Star-3.png" class="header__star-3" alt="star-3" />
        <p>
          Loyalbaze, empowers businesses to offer digital, mobile-first loyalty programs to their
          customers. With our AI Powered platform, you can easily create and manage custom loyalty
          and rewards programs, track customer engagement, and gain valuable insights to improve
          your business. Sign up now to get early access.
          <img
            src="./assets/icons/ellipse/Ellipse-38.png"
            class="header__ellipse-38"
            alt="ellipse-38"
          />
        </p>
        <img src="./assets/icons/Bold/Vector-3.png" class="header__vector-3" alt="vector-3" />
        <form class="header-form">
          <div class="header-form__group">
            <input class="header-form__input" type="text" placeholder="Tell us your name" />
          </div>

          <div class="header-form__group">
            <input class="header-form__input" type="text" placeholder="Enter your email address" />
          </div>
          <popup-view v-if="showModal">
            <div class="popup-icon">
              <img
                src="./assets/icons/green-ellipse.png"
                class="popup-icon__ellipse"
                alt="ellipse"
              />
              <img src="./assets/icons/verified.png" class="popup-icon__verified" alt="verified" />
            </div>

            <div class="popup-text">
              <h4>Congratulations</h4>
              <p>
                Great move! You're one step closer to getting your hands on the product. Please
                check your mail for more information.
              </p>
            </div>
          </popup-view>

          <div class="header-form__group">
            <button class="btn" @click.prevent="showModal = !showModal">Get early access</button>
          </div>
        </form>

        <div class="header__icons">
          <div class="header-img">
            <div>
              <img src="./assets/icons/goum.png" alt="" />
            </div>
          </div>
        </div>
        <img src="./assets/icons/stars/Star-1.png" class="header__star-1" alt="star-1" />
      </div>
      <img src="./assets/icons/stars/Star-4.png" class="header__star-4" alt="star-4" />
    </section>

    <!-- section 2 What we do -->
    <section class="priority" id="priority-access">
      <div class="row">
        <div class="col-1">
          <img
            src="./assets/icons/ellipse/Ellipse-39.png"
            class="col-1__ellipse-39"
            alt="ellipse-39"
          />
          <img src="./assets/icons/stars/Star-3.png" class="col-1__star-3" alt="star-3" />
          <!-- <h2>Priority Access</h2> -->
          <img
            src="./assets/icons/Priority-Access.png"
            class="col-1__priority-access"
            alt="star-3"
          />

          <img src="./assets/icons/Line/line-6.png" class="col-1__line-6" alt="line-6" />
          <p>
            Get ready to revolutionize the way you interact with your customers and drive sales with
            Loyalbaze. Skip the waitlist and get exclusive priority access to LoyalBaze. Limited
            slots available. Please tell us a bit about your business and needs and of our
            consultants will be in touch Immediately!
          </p>
          <img src="./assets/icons/stars/Star-5.png" class="col-1__star-5" alt="star-5" />
        </div>

        <div class="col-2">
          <form class="form">
            <h3>Book a consultation with us</h3>
            <div class="form__group">
              <input type="text" class="form__input" placeholder="Enter your full name" />
            </div>

            <div class="form__group">
              <input type="text" class="form__input" placeholder="Enter your work email" />
            </div>

            <div class="form__group">
              <input type="text" class="form__input" placeholder="Mobile number" />
            </div>

            <div class="form__group">
              <input type="text" class="form__input" placeholder="Company Name" />
            </div>

            <div class="form__group">
              <input type="text" class="form__input" placeholder="select country" />
            </div>

            <div class="form__group">
              <textarea placeholder="Drop a message..." class="form__input"></textarea>
            </div>

            <div class="form__group">
              <button class="btn btn--request" @click.prevent="">Send request</button>
            </div>
          </form>
          <img src="./assets/icons/stars/Star-4.png" class="col-2__star-4" alt="star-4" />
        </div>
      </div>
    </section>
    <div class="overlay" v-if="showModal" @click="showModal = !showModal"></div>

    <footer class="footer">
      <div class="footer__stroke">
        <img src="./assets/icons/Line-14.png" alt="" />
      </div>

      <div class="footer__row">
        <div class="footer__col footer__col--1">
          <img src="./assets/icons/Bold/Vector-2.png" alt="address" />
          <div>
            <p>2nd Floor, The Garnet Building, KM14</p>
            <p>Lekki Epe Expressway, Lagos, Nigeria</p>
          </div>
        </div>

        <div class="footer__col footer__col--3">
          <p>Loyalbaze is almost here.</p>
        </div>

        <div class="footer__col footer__col--3">
          <img src="./assets/icons/Bold/Vector.png" alt="telephone" />
          <p>+234 903 618 9485</p>
        </div>
      </div>
    </footer>
  </main>
</template>

<script>
import PopupView from '@/components/PopupView.vue';

export default {
  name: 'App',
  components: { PopupView },

  data() {
    return {
      showModal: false,
    };
  },
};
</script>
