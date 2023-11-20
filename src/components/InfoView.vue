<!-- <template>
    <section class="information">
        <div class="container">
            <h1>Заботится о вашей безопасности</h1>
            <div class="list-wrapper">
                <div class="card" v-for="(card, index) in infoArray" :key="card" @click="activeTab(index)"
                    :class="{ active: card.active }">
                    <h2>{{ card.title }}</h2>
                    <hr>
                    <p>{{ card.text }}</p>
                </div>
            </div>
            <div class="images" :class="{active: index === tabIndex}" v-for="(image, index) in infoArray" :key="image">
                <img class="scooter1" :src="image.image1" alt="">
                <img class="scooter2" :src="image.image2" alt="">
            </div>

        </div>
    </section>
</template> -->

<script>
import image1 from '../assets/images/Rectangle 23.png'
import image2 from '../assets/images/Rectangle 24.png'
import image3 from '../assets/images/brakes.png'
// import image1 from '../assets/images/Rectangle 23.png'

export default {
    data() {
        return {
            tabIndex: 0,
            infoArray: [
                {
                    title: 'Яркие ходовые огни 1',
                    text: 'Продуманный угол рассеивания света позволяет сохранять хорошую видимость, не ослепляя других участников движения.',
                    active: true,
                    image1: image1,
                    image2: image2,
                },
                {
                    title: 'Яркие ходовые огни 2',
                    text: 'Продуманный угол рассеивания света позволяет сохранять хорошую видимость, не ослепляя других участников движения.',
                    active: false,
                    image1: image3,
                    image2: image2,
                },
                {
                    title: 'Яркие ходовые огни 3',
                    text: 'Продуманный угол рассеивания света позволяет сохранять хорошую видимость, не ослепляя других участников движения.',
                    active: false,
                    image1: image1,
                    image2: image2,
                },
                {
                    title: 'Яркие ходовые огни 4',
                    text: 'Продуманный угол рассеивания света позволяет сохранять хорошую видимость, не ослепляя других участников движения.',
                    active: false,
                    image1: image1,
                    image2: image2,
                },
            ]
        }
    },
    methods: {
        activeTab(index) {
            this.tabIndex = index
            this.infoArray[index].active = !this.infoArray[index].active
            console.log(index)

            if (index === 1) {
                this.infoArray[1].active = true
                this.infoArray[2].active = false
                this.infoArray[3].active = false
            }
            
            if (index === 2) {
                this.infoArray[1].active = true
                this.infoArray[2].active = true
                this.infoArray[3].active = false
            }
            
            if (index === 3) {
                this.infoArray[1].active = true
                this.infoArray[2].active = true
            }

            if (index === 0) {
                this.infoArray.forEach(item => item.active = false)
            }
        }
    }
}

</script>

<!-- <style lang="scss" scoped>
@import '../assets/components/theInfo.scss';
</style> -->