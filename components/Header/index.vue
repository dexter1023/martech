<template>
  <header>
    <div class="header">
      <div class="header__back">
        <img src="@/assets/img/icons/back-icon.svg" />
        <span class="tk-museo-sans-rounded font-bold">back to articles</span>
      </div>
      <div class="header__logo">
        <img
          src="@/assets/img/logos/love-martech-logo.svg"
          alt="Logo Love Martech"
        />
      </div>
    </div>
  </header>
</template>
<style lang="scss" scoped>
header {
  background-color: $dark-slate;
}
.header {
  display: flex;
  padding: 28px 48px;
}
.header__logo {
  width: 50%;
  text-align: center;
  img {
    max-height: 39px;
  }
  @media screen and (max-width: $phone) {
    width: 100%;
  }
}
.header__back {
  color: $light-gray;
  display: flex;
  align-content: flex-end;
  width: 25%;
  img {
    max-width: 11px;
    margin-right: 10px;
  }
  span {
    font-size: 18px;
    letter-spacing: -0.18px;
  }
  @media screen and (max-width: $phone) {
    display: none;
  }
}
</style>
