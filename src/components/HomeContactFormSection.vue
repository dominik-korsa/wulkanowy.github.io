<template>
  <div class="contact-form home-section">
    <h2 class="contact-form__title">Kontakt</h2>
    <div class="contact-form__direct">
      <a class="contact-form__direct-link" href="mailto:wulkanowyinc@gmail.com">
        <span class="mdi mdi-email"></span>
        <span class="text">wulkanowyinc@gmail.com</span>
      </a>
      <a class="contact-form__direct-link" href="https://discord.gg/vccAQBr">
        <span class="mdi mdi-discord"></span>
        <span class="text">wulkanowy</span>
      </a>
    </div>
    <form>
    </form>
  </div>
</template>

<script>
  export default {
    name: 'home-contact-form-section',
  };
</script>

<style lang="scss">
  .contact-form {
    height: 100vh;
    box-sizing: border-box;
    padding: 0 32px 32px;
    overflow: hidden;
    display: grid;
    grid-template-columns: 1fr auto 1fr;
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
      grid-column: 1/4;
      grid-row: 1;

      @media screen and (max-width: 875px) {
        grid-column: 1;
      }
    }

    &__direct {
      grid-column: 2;
      grid-row: 3;
      padding: 8px;

      @media screen and (max-width: 875px) {
        grid-column: 1;
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
      }

      .mdi {
        font-size: 32px;
        margin-right: 10px;
      }
    }
  }
</style>
