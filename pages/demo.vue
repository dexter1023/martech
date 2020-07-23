<template>
  <div class="page-wrapper">
    <section>
      <div class="content__layer">
        <div class="container p-t-75 p-b-75">
          <div class="row nowrap">
            <div class="momentum-logo">
              <img
                src="@/assets/img/logos/momentum-m-logo.svg"
                alt="Momentum"
              />
            </div>
            <div class="col-6">
              <div class="header">
                <div class="header__logo mobile-text-center">
                  <img
                    src="@/assets/img/logos/momentum-white-logo.svg"
                    alt="Momentum Logo"
                  />
                </div>
                <div class="header__text-main font-bold">
                  <h2>Asset Creation Made Easy For The Enterprise</h2>
                </div>
                <div class="header__text">
                  Enabling anyone to build on brand emails and landing pages in
                  minutes.
                </div>
              </div>
            </div>
            <div class="col-sm">
              <Card title="Request a Demo">
                <div>
                  <form>
                    <div class="row">
                      <div class="col-6">
                        <Input v-model="form.firstName" label="first name" />
                      </div>
                      <div class="col-6">
                        <Input v-model="form.lastName" label="last name" />
                      </div>
                      <div class="col-6">
                        <Input
                          v-model="form.email"
                          label="email"
                          type="email"
                        />
                      </div>
                      <div class="col-6">
                        <Input v-model="form.telephone" label="telephone" />
                      </div>
                      <div class="col-6">
                        <Input v-model="form.position" label="position" />
                      </div>
                      <div class="col-6">
                        <Input v-model="form.company" label="company" />
                      </div>
                      <div class="col">
                        <div class="form__submit">
                          <CustomButton full-width>
                            Submit
                          </CustomButton>
                        </div>
                      </div>
                    </div>
                  </form>
                </div>
              </Card>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section>
      <div class="arrow-section">
        <img src="@/assets/img/shapes/arrow.svg" alt="Arrow" class="arrow" />
        <div class="container p-t-60">
          <div class="row">
            <div class="col">
              <ListItem
                v-for="el in listItems"
                :key="el.text"
                :text="el.text"
                :logo="el.logo"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Card from '@/components/Common/Card'
import Input from '@/components/Common/Form/Input.vue'
import ListItem from '@/components/Common/ListItem'
import CustomButton from '@/components/Common/Button'
export default {
  components: {
    Card,
    Input,
    ListItem,
    CustomButton,
  },
  data() {
    return {
      form: {
        firstName: '',
        lastName: '',
        email: '',
        telephone: '',
        position: '',
        company: '',
      },
      listItems: [
        {
          text: 'Easly integrate momentum into workflow',
          logo: 'circle.svg',
        },
        {
          text: 'Quickly build brand emails',
          logo: 'star.svg',
        },
        {
          text: 'Review and approve teams emails and pages',
          logo: 'arrow.svg',
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
.content__layer {
  background-color: rgba(0, 0, 0, 0.1);
}
.momentum-logo {
  position: absolute;
  right: 0;
  opacity: 0.3;
  z-index: -100;
  top: -100px;
  img {
    width: 1000px;
  }
}
.header {
  color: $white;
  @media screen and (max-width: $phone) {
    padding-bottom: 30px;
  }
}
.header__logo {
  img {
    max-width: 242px;
  }
}
.header__text-main {
  font-size: $font-big;
  margin: 20px 0;
}
.header__text {
  font-size: $font-medium;
}
.content__layer {
  background-color: rgba(0, 0, 0, 0.1);
}
.arrow {
  position: absolute;
  left: -180px;
  width: 473px;
  height: 473px;
  transform: matrix(0.71, 0.71, -0.71, 0.71, 0, 0);
  filter: $filter-white;
  opacity: 0.3;
}
.arrow-section {
  min-height: 473px;
}
.form__submit {
  width: calc(50% + 30px);
  margin-left: calc(50% - 15px);
  margin-top: 65px;
  @media screen and (max-width: $phone) {
    width: 100%;
    margin-top: 65px;
    margin-left: 0;
    button {
      width: 100%;
    }
  }
}
</style>
