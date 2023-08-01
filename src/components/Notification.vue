<template>
  <main class="main-container">
    <!-- Header Container -->
    <header class="header-container">
      <div class="header__notification">
        <h1 class="header__main-title">Notifications</h1>
        <div class="header__notification-number">{{ notificationNumber }}</div>
      </div>

      <button type="button" class="btn" @click="markAll">
        Mark all as read
      </button>
    </header>

    <!-- Notification 1 -->
    <section
      class="notification notification__new"
      :class="mark == true ? 'marked' : ''"
    >
      <div class="notification__img">
        <img
          src="../assets/images/avatar-mark-webber.webp"
          alt="Men Profile Picture"
        />
      </div>

      <div class="notification__info">
        <div class="notification__text">
          <p class="notification__paragraph">
            <strong class="notification__name">Mark Webber</strong> reacted to
            your recent post
            <a href="#" class="notification__link"
              >My first tournament today!</a
            >
            <span class="circle"></span>
          </p>
        </div>

        <span class="notification__time">1m ago</span>
      </div>
    </section>

    <!-- Notification 2 -->
    <section
      class="notification notification__new"
      :class="mark == true ? 'marked' : ''"
    >
      <div class="notification__img">
        <img
          src="../assets/images/avatar-angela-gray.webp"
          alt="Woman Profile Picture"
        />
      </div>

      <div class="notification__info">
        <div class="notification__text">
          <p class="notification__paragraph">
            <strong class="notification__name"> Angela Gray</strong> followed
            you
            <span class="circle"></span>
          </p>
        </div>

        <span class="notification__time">5m ago</span>
      </div>
    </section>

    <!-- Notification 3 -->
    <section
      class="notification notification__new"
      :class="mark == true ? 'marked' : ''"
    >
      <div class="notification__img">
        <img
          src="../assets/images/avatar-jacob-thompson.webp"
          alt="Man Profile Picture"
        />
      </div>

      <div class="notification__info">
        <div class="notification__text">
          <p class="notification__paragraph">
            <strong class="notification__name">Jacob Thompson</strong> has
            joined your group
            <a href="#" class="notification__link-2">Chess Club</a>
            <span class="circle"></span>
          </p>
        </div>

        <span class="notification__time">1 day ago</span>
      </div>
    </section>

    <!-- Notification 4 -->
    <section class="notification">
      <div class="flex">
        <div class="notification__img">
          <img
            src="../assets/images/avatar-rizky-hasanuddin.webp"
            alt="Man Profile Picture"
          />
        </div>

        <div class="notification__info">
          <div class="notification__text">
            <p class="notification__paragraph">
              <strong class="notification__name">Rizky Hasanuddin</strong> sent
              you a private message
            </p>
          </div>

          <span class="notification__time">5 days ago</span>
        </div>
      </div>

      <div class="private-msg">
        <p>
          Hello, thanks for setting up the Chess Club. I've been a member for a
          few weeks now and I'm already having lots of fun and improving my
          game.
        </p>
      </div>
    </section>

    <!-- Notification 5 -->
    <section class="notification">
      <div class="notification__img">
        <img
          src="../assets/images/avatar-kimberly-smith.webp"
          alt="Woman Profile Picture"
        />
      </div>

      <div class="notification__info">
        <div class="notification__text">
          <p class="notification__paragraph">
            <strong class="notification__name">Kimberly Smith</strong> commented
            on your picture
          </p>
        </div>

        <span class="notification__time">1 week ago</span>
      </div>

      <div class="commented-img">
        <img src="../assets/images/image-chess.webp" alt="Chess Image" />
      </div>
    </section>

    <!-- Notification 6 -->
    <section class="notification">
      <div class="notification__img">
        <img
          src="../assets/images/avatar-nathan-peterson.webp"
          alt="Man Profile Picture"
        />
      </div>

      <div class="notification__info">
        <div class="notification__text">
          <p class="notification__paragraph">
            <strong class="notification__name">Nathan Peterson</strong> reacted
            to your recent post
            <a href="#" class="notification__link"
              >5 end-game strategies to increase your win rate</a
            >
          </p>
        </div>

        <span class="notification__time">2 weeks ago</span>
      </div>
    </section>

    <!-- Notification 7 -->
    <section class="notification">
      <div class="notification__img">
        <img
          src="../assets/images/avatar-anna-kim.webp"
          alt="Woman Profile Picture"
        />
      </div>

      <div class="notification__info">
        <div class="notification__text">
          <p class="notification__paragraph">
            <strong class="notification__name">Anna Kim</strong> left the group
            <a href="#" class="notification__link-2">Chess Club</a>
          </p>
        </div>

        <span class="notification__time">2 weeks ago</span>
      </div>
    </section>
  </main>

  <footer class="attribution">
    <p>
      Challenge by
      <a href="https://www.frontendmentor.io?ref=challenge" target="_blank"
        >Frontend Mentor</a
      >
    </p>

    <p>
      Code <span>&hearts;</span> by
      <a href="https://github.com/SouleymaneSy7" target="_blank"
        >Souleymane Sy</a
      >
    </p>
  </footer>
</template>

<script setup>
import { ref } from "vue";

const mark = ref(false);
const notificationNumber = ref(3);

const markAll = () => {
  mark.value = true;
  notificationNumber.value = 0;
};
</script>
