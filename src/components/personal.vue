<template>
  <div id="personal">
    <div class="intro">
      <div class="name">Hi, I am Ekadharma <br /></div>

      <VueWriter
        :array="[
          'Front End Junior',
          'Web Developer',
        ]"
        :eraseSpeed="40"
        :typeSpeed="50"
        :delay="3000"
      />
    </div>
    <div class="card border-0">
      <div class="card-body">
        <div class="profil">
          <div class="desc">
            I have a student background at ITB STIKOM BALI. In January 2020 I attended a field work training at Kominfo Badung. 
            I believe that my qualifications and skills can make a significant contribution to the company. 
            I'm a person who can do well as part of a team and on my own. I am also a hard worker, and eager to learn.
          </div>
          <div class="foto">
            <img src="@/assets/img/eka.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "personal-vue",
  data() {
    return {};
  },
  created() {},
};
</script>

<style lang="scss">
#personal {
  transition: all 0.4s;
  padding: 0 20px;
}

.card {
  transition: all 0.4s;
  background: var(--color-1);
  color: var(--text-color-1);
  border-radius: 20px;
  position: relative;
}

.card::before {
  position: absolute;
  content: "";
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: url("../assets/img/pattern.webp");
  background-size: 50%;
  opacity: 0.1;
}

.name {
  font-size: 1.5em;
  margin-bottom: -10px;
}

.intro {
  font-size: 1.2em;
  margin-bottom: 10px;
}

.profil {
  position: relative;
  display: flex;
}

.desc {
  width: 60%;
  font-size: 0.8em;
}

.foto {
  position: relative;
  // overflow-x: hidden;
  width: 40%;
}

.foto img {
  position: absolute;
  bottom: -15px;
  right: -10px;
  width: 100%;
}

@media only screen and (max-width: 600px) {
  .foto img {
    width: 120%;
  }
}
</style>