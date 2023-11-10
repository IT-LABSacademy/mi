<template>
    <section class="economiya">
        <div class="container">
            <h1>Мощная батарея и экономичный расход <br> заряда позволяют преодолевать <br> расстояния до 45 км</h1>
            <div class="wrapper">
                <div  @click="activeLine_3" v-for="item in isLine" class="text-card">
                    <h2 v-if="!orangeLine_3"  class="white-title">{{ item.title }}</h2>
                    <h2 v-else="!orangeLine_3" class="orange">{{ item.title }}</h2>

                    <p v-if="!whiteText" @click="activeText" class="gray-text">{{ item.text }}</p>
                    <p v-else="!whiteText" @click="activeText" class="white-text">{{ item.text }}</p>
                </div>

                <div v-for="item in isLine" @click="activeLine" class="text-card">
                    <h2 v-if="!orangeLine" class="white-title">{{ item.title_2 }}</h2>
                    <h2 v-else="!orangeLine" class="orange">{{ item.title_2 }}</h2>

                    <p v-if="!whiteText_2" @click="activeText_2" class="gray-text">{{ item.text_2 }}</p>
                    <p v-else="!whiteText_2" @click="activeText_2" class="white-text">{{ item.text_2 }}</p>
                </div>

                <div v-for="item in isLine" @click="activeLine_2" class="text-card">
                    <h2  v-if="!orangeLine_2" class="white-title">{{ item.title_3 }}</h2>
                    <h2 v-else="!orangeLine_2" class="orange">{{ item.title_3 }}</h2>
                    <p v-if="!whiteText_3" @click="activeText_3" class="gray-text">{{ item.text_3 }}</p>
                    <p v-else="!whiteText_3" @click="activeText_3" class="white-text">{{ item.text_3 }}</p>
                </div>

            </div>
            <div class="images">
                <img class="img-1" src="../assets/images/economiya-img-1.svg" alt="#">
                <img class="img-2" src="../assets/images/economiya-img-2.svg" alt="#">
                <img class="media-img-1" src="../assets/images/media-economiya.svg" alt="#">
                <img class="media-img-2" src="../assets/images/media.svg" alt="#">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            orangeLine: false,
            orangeLine_2: false,
            orangeLine_3: false,
            whiteText: false,
            whiteText_2: false,
            whiteText_3: false,
            isLine: [{
                title: 'Три режима скорости',
                title_2: 'Система восстановления энергии',
                title_3: 'Мощная батарея',

                text: 'Три режима езды позволяют почуствовать себя комфортно в любой ситуации. Режим «S» увеличитвает скорость, если опаздываете на работу.Во время прогулки по парку активируйте режим «D».Включите режим «Пешеход», когда двигаетесь по оживлённой улице.',
                text_2: 'Во время торможения и движения по инерции система преобразовывает кинетическую энергию в электрическую, позволяя увеличить общий запас хода самоката.',
                text_3: 'Самокат оснащен аккумулятором емкостью 12 800 мАч. Это позволяет преодолевать расстояния до 45 км без подзарядки.',
            }]
        }
    },
    methods: {
        activeLine() {
            if (this.orangeLine = true || this.whiteText === true) {}
        },

        activeLine_2() {
            if (this.orangeLine_2 = true) {}
        },

        activeLine_3() {
            if (this.orangeLine_3 = true) {}
        },

        activeText() {
            if (this.whiteText = true) {}
        },

        activeText_2() {
            if (this.whiteText_2 = true) {}
        },

        activeText_3() {
            if (this.whiteText_3 = true) {}
        },
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/components/theEconomiya.scss';
</style>