<template>
  <footer>
    <div class="content__layer p-t-60 p-b-75">
      <div class="container">
        <div class="row flex-space-between p-b-75 column-reverse">
          <img
            v-lazy
            src="@/assets/img/logos/love-martech-logo.svg"
            alt="Logo martech"
            class="martech-logo"
          />

          <img
            v-lazy
            src="@/assets/img/logos/clevertouch-icon.svg"
            alt="Clevertouch"
            class="filter-white clevertouch-icon"
          />
        </div>
        <div class="row mobile-text-center">
          <div class="col-3">
            <p class="font-bold">start a conversation</p>
            <p>
              <a href="phone:+44 (0)1962 677 000">+44 (0)1962 677 000</a>
            </p>
            <p>
              hello@clever-touch.com
            </p>
            <p><CustomButton>Start live chat</CustomButton></p>
          </div>
          <div class="col-3">
            <p class="font-bold">find us</p>
            <p>
              Clevertouch HQ The Old Forge, The Dean, Alresford, Hampshire, SO24
              9BH Get directions
            </p>
            <p><a href="#">Get directions</a></p>
          </div>
          <div class="col-3">
            <p class="font-bold">never miss a thing</p>
            <inputButton placeholder="Email" text="Sign up" />
            <p>Sign me up to receive marketing tips and content</p>
            <div class="social-icons filter-white">
              <a href="#">
                <img src="@/assets/img/icons/twitter-icon.svg" alt="Twitter" />
              </a>
              <a href="#">
                <img
                  src="@/assets/img/icons/linkedin-icon.svg"
                  alt="LinkedIn"
                />
              </a>
            </div>
          </div>
          <div class="col-3 font-little align-right mobile-text-center">
            <div class="placeholders-images">
              <img
                v-lazy
                src="@/assets/img/placeholders/best-company.png"
                alt="Best company 3 stars"
              /><img
                v-lazy
                src="@/assets/img/placeholders/times-100-best-small-companies.png"
                alt="Times 100 best small companies"
              />
            </div>
            <div class="font-gray">
              <p>© 2020 Clevertouch Marketing.</p>
              <p>
                <a href="#">Terms & Conditions</a><a href="#">Privacy Policy</a>
              </p>
              <p>Designed by <a href="#">Bigger Picture</a></p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<script>
import CustomButton from '@/components/Common/Button'
import InputButton from '@/components/Common/Form/InputButton'
export default {
  components: {
    CustomButton,
    InputButton,
  },
}
</script>
<style lang="scss" scoped>
footer {
  color: $white;
}
.clevertouch-icon {
  max-width: 75px;
  max-height: 84px;
  @media screen and(max-width: $phone) {
    margin-bottom: 36px;
  }
}
.martech-logo {
  max-width: 100%;
  max-height: 39px;
  min-height: 20px;
}
.social-icons {
  img {
    max-width: 30px;
  }
}
.col-3 {
  font-size: $font-small;
  @media screen and (max-width: $phone) {
    margin-bottom: 30px;
  }
}
.col-3 .font-bold {
  font-size: $font-normal;
}
.placeholders-images {
  width: 100%;
  img {
    height: 84px;
    margin-left: 24px;
  }
}
</style>
