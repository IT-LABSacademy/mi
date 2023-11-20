<template>
    <section class="economiya">
        <div class="container">
            <h1>Мощная батарея и экономичный расход <br> заряда позволяют преодолевать <br> расстояния до 45 км</h1>
            <div class="wrapper">
                <div v-for="(item, index) in cardArray" :key="item" @click="activeCard(index)" class="text-card">
                    <h2 v-if="!item.orangeLine" class="white-title">{{ item.title }}</h2>
                    <h2 v-else class="orange">{{ item.title }}</h2>

                    <p v-if="!item.whiteText" class="gray-text">{{ item.text }}</p>
                    <p v-else class="white-text">{{ item.text }}</p>
                </div>
            </div>
            <div class="images">
                <img class="img-1" src="../../assets/images/economiya-img-1.svg" alt="#">
                <img class="img-2" src="../../assets/images/economiya-img-2.svg" alt="#">
            </div>
            <div class="media-images">
                <img class="media-img-1" src="../../assets/images/media-economiya.svg" alt="#">
                <img class="media-img-2" src="../../assets/images/media.svg" alt="#">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            cardArray: [
                {
                    title: 'Три режима скорости',
                    text: 'Три режима езды позволяют почуствовать себя комфортно в любой ситуации. Режим «S» увеличитвает скорость, если опаздываете на работу.Во время прогулки по парку активируйте режим «D».Включите режим «Пешеход», когда двигаетесь по оживлённой улице.',
                    orangeLine: true,
                    whiteText: true,
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

            if (index === 0) {
                this.cardArray[0].orangeLine = true
                this.cardArray[1].orangeLine = false
                this.cardArray[2].orangeLine = false

                this.cardArray[0].whiteText = true
                this.cardArray[1].whiteText = false
                this.cardArray[2].whiteText = false
            }

            if (index === 1) {
                this.cardArray[1].whiteText = true
                this.cardArray[1].orangeLine = true

                this.cardArray[2].whiteText = false
                this.cardArray[2].orangeLine = false
            }

            if (index === 2) {
                this.cardArray[1].orangeLine = true
                this.cardArray[1].whiteText = true
            }
        },

    }
}
</script>

<style lang="scss" scoped>
@import '../home/styles/theEconomiya.scss';
</style>