<template>
    <section class="economiya">
        <div class="container">
            <h1>Мощная батарея и экономичный расход <br> заряда позволяют преодолевать <br> расстояния до 45 км</h1>
            <div  class="wrapper">
            <div v-for="(item, index) in cardArray" :key="item"   @click="activeCard(index)" class="text-card">
                    <h2 v-if="!item.orangeLine"  class="white-title">{{ item.title }}</h2>
                    <h2 v-else="item.orangeLine" class="orange">{{ item.title }}</h2>

                    <p v-if="!item.whiteText" @click="activeCard" class="gray-text">{{ item.text }}</p>
                    <p v-else="item.whiteText" @click="activeCard" class="white-text">{{ item.text }}</p>
                </div>
            </div>
            <div class="images">
                <img class="img-1" src="../assets/images/economiya-img-1.svg" alt="#">
                <img class="img-2" src="../assets/images/economiya-img-2.svg" alt="#">
            </div>
            <div class="media-images">
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
            whiteText: false,
            cardArray: [
                {
                    title: 'Три режима скорости',
                    text: 'Три режима езды позволяют почуствовать себя комфортно в любой ситуации. Режим «S» увеличитвает скорость, если опаздываете на работу.Во время прогулки по парку активируйте режим «D».Включите режим «Пешеход», когда двигаетесь по оживлённой улице.',
                    orangeLine: false,
                    whiteText: false,
                },
                {
                    title: 'Система восстановления энергии',
                    text: 'Во время торможения и движения по инерции система преобразовывает кинетическую энергию в электрическую, позволяя увеличить общий запас хода самоката.',
                    orangeLine: false,
                    whiteText: false,
                },
                {
                    title: 'Мощная батарея',
                    text: 'Самокат оснащен аккумулятором емкостью 12 800 мАч. Это позволяет преодолевать расстояния до 45 км без подзарядки.',
                    orangeLine: false,
                    whiteText: false,
                },
               
            ]
        }
    },
    methods: {
        activeCard(index) {
            this.cardArray[index].orangeLine = !this.cardArray[index].orangeLine
            this.cardArray[index].whiteText = !this.cardArray[index].whiteText
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/components/theEconomiya.scss';
</style>