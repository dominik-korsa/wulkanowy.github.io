<template>
  <div class="contact home-section">
    <h2 class="contact__title">Kontakt</h2>
    <div class="contact__direct">
      <a class="contact__direct-link" href="mailto:wulkanowyinc@gmail.com" title="Email">
        <span class="mdi mdi-email"></span>
        <span class="text">wulkanowyinc@gmail.com</span>
      </a>
      <a class="contact__direct-link" href="https://discord.gg/vccAQBr" title="Discord">
        <span class="mdi mdi-discord"></span>
        <span class="text">wulkanowy</span>
      </a>
    </div>
    <form class="contact__form" action="https://formspree.io/xqkzgzqp" method="POST">
      <label for="contact__form-email" class="contact__form-label">Twój adres email:</label>
      <input
        type="email"
        id="contact__form-email"
        class="contact__form-email"
        name="_replyto"
        required
        placeholder="twój-email@example.com"
      >
      <label for="contact__form-message" class="contact__form-label">Wiadomość:</label>
      <textarea
        name="message"
        id="contact__form-message"
        class="contact__form-message"
        required
        placeholder="Twoja wiadomość"
      ></textarea>
      <input type="submit" class="contact__form-submit" value="Wyślij">
    </form>
  </div>
</template>

<script>
  export default {
    name: 'home-contact-form-section',
  };
</script>

<style lang="scss">
  .contact {
    height: 100vh;
    box-sizing: border-box;
    padding: 0 32px 32px;
    overflow: hidden;
    display: grid;
    grid-template-columns: 1fr auto auto 1fr;
    grid-template-rows: auto 1fr auto 1fr;
    background:
      linear-gradient(
      rgba(0, 0, 0, 0.6),
      rgba(0, 0, 0, 0.6)
      ),
      url("../assets/wallpaper.jpg");
    background-size: cover;
    background-position: center;
    background-attachment: fixed;

    @media screen and (max-width: 875px) {
      grid-template-columns: 1fr;
      grid-template-rows: auto auto 1fr auto 1fr;
      padding: 0 16px 16px;
    }

    @media screen and (max-width: 450px) {
      padding: 0 8px 16px;
    }

    &__title {
      font-size: 32px;
      text-align: center;
      color: #fff;
      font-family: 'Roboto', sans-serif;
      font-weight: 400;
      grid-column: 1/5;
      grid-row: 1;

      @media screen and (max-width: 875px) {
        grid-column: 1;
      }
    }

    &__direct {
      grid-column: 2;
      grid-row: 3;
      padding: 8px 32px;
      align-self: center;

      @media screen and (max-width: 875px) {
        grid-column: 1;
        grid-row: 2;
        justify-self: center;
      }
    }

    &__direct-link {
      display: flex;
      background-color: #fff;
      min-width: fit-content;
      padding: 4px;
      padding-left: 12px;
      padding-right: 16px;
      height: 48px;
      margin: 16px 0;
      border-radius: 3px;
      text-decoration: none;
      color: #000;
      box-shadow:
        0px 5px 5px -3px rgba(0, 0, 0, 0.2),
        0px 8px 10px 1px rgba(0, 0, 0, 0.14),
        0px 3px 14px 2px rgba(0, 0, 0, 0.12);
      transition: box-shadow 150ms;
      font-family: 'Roboto', sans-serif;
      flex-direction: row;
      align-items: center;

      @media screen and (max-width: 450px) {
        padding: 4px;
        padding-left: 8px;
        padding-right: 10px;
        height: 32px;
      }

      &:focus {
        outline: none;
      }

      &:focus, &:hover {
        box-shadow: 0 11px 15px -7px rgba(0, 0, 0, 0.2),
        0 24px 38px 3px rgba(0, 0, 0, 0.14),
        0 9px 46px 8px rgba(0, 0, 0, 0.12);
      }

      .text {
        font-size: 20px;
        flex-grow: 1;
        text-align: center;

        @media screen and (max-width: 450px) {
          font-size: 16px;
        }
      }

      .mdi {
        font-size: 32px;
        margin-right: 10px;

        @media screen and (max-width: 450px) {
          font-size: 28px;
          margin-right: 8px;
        }
      }
    }

    &__form {
      display: flex;
      padding: 8px 32px;
      grid-row: 3;
      grid-column: 3;
      flex-direction: column;
      justify-content: center;
      align-items: stretch;
      min-width: 30vw;

      @media screen and (max-width: 875px) {
        grid-column: 1;
        grid-row: 4;
      }
    }

    .contact__form-label {
      color: #fff;
      text-align: center;
      margin: 8px 16px;
      font-size: 20px;
      font-family: 'Roboto', sans-serif;
    }

    &__form-email, &__form-message {
      background: none;
      border: none;
      color: #fff;
      font-size: 20px;
      border: 1px solid #fff;
      border-radius: 5px;
      padding: 4px 8px;
      transition: background-color 300ms;

      &::placeholder {
        color: #fffa;
        font-weight: 300;
        font-family: 'Roboto Mono', monospace;
      }

      &:focus, &:hover {
        padding: 3px 7px;
        border: 2px solid #fff;
      }

      &:hover {
        background-color: #fff2;
      }

      &:focus {
        outline: none;
        background-color: #fff5;
      }
    }

    &__form-email {
      font-family: 'Roboto Mono', monospace;
    }

    &__form-message {
      font-family: 'Roboto', sans-serif;
      flex-grow: 1;
      resize: vertical;
      min-height: 120px;
    }

    &__form-submit {
      background: #fff;
      border: none;
      font-size: 20px;
      border-radius: 4px;
      padding: 8px 8px;
      transition: background-color 300ms;
      font-family: 'Roboto', sans-serif;
      margin-top: 16px;
      cursor: pointer;
      min-height: 48px;

      &:focus {
        outline: none;
      }

      &:focus, &:hover {
        box-shadow: 0 11px 15px -7px rgba(0, 0, 0, 0.2),
          0 24px 38px 3px rgba(0, 0, 0, 0.14),
          0 9px 46px 8px rgba(0, 0, 0, 0.12);
      }
    }
  }
</style>
