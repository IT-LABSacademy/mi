<template>
  <!-- section -->
  <section class="sectionn" id="bg">
    <!-- container -->
    <div class="container">
      <!-- left -->
      <div class="leeft">
        <!-- texts -->
        <div class="item-text">
          <h1>Стильный электросамокат с мощным аккумулятором</h1>
        </div>
        <div class="p-text">
          <p>
            Улучшенная производительность для дальних путешествий. Работает так
            же просто, как и выглядит.
          </p>
        </div>
        <!-- button || white && black -->
        <label class="switch" onclick="change()">
          <input type="checkbox" />
          <span class="slider round"></span>
        </label>
        <!-- <div class="btnn">
                        <TheButton color="white">White</TheButton>
                        <TheButton color="black">Black</TheButton>
                    </div> -->
      </div>
    </div>
  </section>
</template>


<script >
import TheButton from "../TheButton.vue";

export default {
  components: {
    TheButton,
  },

};
</script>


<script setup>

function change() {
  document.getElementById("bg").style.backgroundImage = "url(black-scooter.png)";
}

</script>


<style lang="scss" scoped>
@import "./styles/hero.scss";
</style>



<style scoped>
/* The switch - the box around the slider */
.switch {
  position: relative;
  display: inline-block;
  width: 130px;
  height: 54px;
}

/* Hide default HTML checkbox */
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

/* The slider */
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #595959;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 46px;
  width: 46px;
  left: 4px;
  bottom: 4px;
  background-color: #ff4c0d;
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked+.slider {
  background-color: #f0f0f0;
}

input:focus+.slider {
  box-shadow: 0 0 1px #2196F3;
}

input:checked+.slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(76px);
}

/* Rounded sliders */
.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
</style>