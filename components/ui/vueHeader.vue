<template>
  <header>
    <div class="Header">
      <div class="main_container">
        <div>
          <nuxt-link to="/">
            <img src="@/assets/images/Header/logo.png" />
          </nuxt-link>
        </div>
        <nav>
          <div class="nav">
            <div class="language">
              <p class="mb-0 mr-2">Русский</p>
              <svg
                width="10"
                height="5"
                viewBox="0 0 10 5"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path d="M10 0H0L5 5L10 0Z" fill="white" />
              </svg>
            </div>
            <div class="profile">
              <img src="@/assets/images/Header/profile.png" />
              <p class="mb-0 ml-2">Профиль</p>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.Header {
  width: 100%;
  height: auto;

  padding: 15px 0;
  background: #2e7094;
}
.main_container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.nav,
.language,
.profile {
  display: flex;
  align-items: center;
}
.language {
  margin-right: 40px;
  p {
    cursor: pointer;
  }
}
.profile {
  img {
    cursor: pointer;
  }
}
p {
  font-family: "Roboto-Regular";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 19px;
  text-align: center;
  color: #ffffff;
}
</style>