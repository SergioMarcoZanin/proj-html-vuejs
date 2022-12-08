<template>
    <div class="background">
        <div class="container-fluid pt-5">
            <div class="text-center py-5">
                <h4 class="h4sp">People are praising Maxcoach</h4>
                <!-- title -->
                <div class="d-flex justify-content-center pb-3">
                    <h1>what make they&nbsp;<span class="thinner">love us?</span></h1>
                </div>
            </div>
            <div v-if="n === 0" class="pt-5 mt-5 row justify-content-around ">
                <div v-for="(person, index) in people.first" :key="index" class="text-center card-member">

                    <div class="profile-pic"> <img :src="person.img" alt=""> </div>
                    <h4>{{ person.info2 }}</h4>

                    <p class="info">
                        {{ person.info }}
                    </p>
                    <p class="fw-bold">
                        {{ person.name }}
                    </p>
                    <span> {{ person.profession }} </span>
                </div>
            </div>
            <div v-else-if="n === 1" class="pt-5 mt-5 row justify-content-around ">
                <div v-for="(person, index) in people.second" :key="index" class="text-center card-member">

                    <div class="profile-pic"> <img :src="person.img" alt=""> </div>
                    <h4>{{ person.info2 }}</h4>
                    <p class="info">
                        {{ person.info }}
                    </p>
                    <p class="fw-bold">
                        {{ person.name }}
                    </p>
                    <span> {{ person.profession }} </span>
                </div>
            </div>
            <div v-else-if="n === 2" class="pt-5 mt-5 row justify-content-around ">
                <div v-for="(person, index) in people.third" :key="index" class="text-center card-member">

                    <div class="profile-pic"> <img :src="person.img" alt=""> </div>
                    <h4>{{ person.info2 }}</h4>
                    <p class="info">
                        {{ person.info }}
                    </p>
                    <p class="fw-bold">
                        {{ person.name }}
                    </p>
                    <span> {{ person.profession }} </span>
                </div>
            </div>
            <div v-else-if="n === 3" class="pt-5 mt-5 row justify-content-around ">
                <div v-for="(person, index) in people.four" :key="index" class="text-center card-member">

                    <div class="profile-pic"> <img :src="person.img" alt=""> </div>
                    <h4>{{ person.info2 }}</h4>
                    <p class="info">
                        {{ person.info }}
                    </p>
                    <p class="fw-bold">
                        {{ person.name }}
                    </p>
                    <span> {{ person.profession }} </span>
                </div>
            </div>
            <div class="d-flex justify-content-center pt-4">
                <div @click="changeN(index)" v-for="(element, index) in dots" :key="index" class="m-3"
                    :class="condition(index) ? 'color-dots fs-5' : 'text-dark'">
                    <i :class="`fa-solid ${element.dot}`"></i>
                </div>
            </div>
            <div class="d-flex justify-content-around pt-5 pb-5">
                <div @click="prevTree()" class="btn btncol">
                    <i class="fa-solid fa-arrow-left"></i>
                </div>
                <div @click="nextTree()" class="btn btncol">
                    <i class="fa-solid fa-arrow-right"></i>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data: function () {
        return {
            dots: [
                {
                    dot: 'fa-circle'
                },
                {
                    dot: 'fa-circle'
                },
                {
                    dot: 'fa-circle'
                },
                {
                    dot: 'fa-circle'
                },
            ],
            people: {
                first: [
                    {
                        img: 'img/testimonial-avata-02.jpg',
                        info2: 'High level of efficiency and scientific teaching methods',
                        info: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
                        name: 'MINO HOLLACE',
                        profession: '/ Freelancer'
                    },
                ],
                second: [
                    {
                        img: 'img/testimonial-avata-01.jpg',
                        info2: 'Professional team of specialists and passionate mentors at reach',
                        info: 'I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.',
                        name: 'MADLEY PONDOR',
                        profession: '/ IT Specialst'
                    },
                ],
                third: [
                    {
                        img: 'img/testimonial-avata-04.jpg',
                        info2: 'The MaxCoach team works really hard to ensure high quality',
                        info: 'I am happy with their arrangement of lessons and subjects. They reflect a scientific  investigation into effective methods to be adopted for learners of all levels.',
                        name: 'LUVIC DUBBLE',
                        profession: '/ Private Tutor'
                    },
                ],
                four: [
                    {
                        img: 'img/testimonial-avata-03.jpg',
                        info2: 'It\'s a choice of quality for people with special needs',
                        info: 'I\'m a very strict person so I require everything to be organized and neat. Then, I\'ll be able to make things right and shine. MaxCoach guys just got me.',
                        name: 'FLORENCE THEMES',
                        profession: '/ Private Tutor'
                    },
                ],
            },
            n: 0
        }
    },
    methods: {
        nextTree() {
            this.n++;
            if (this.n > 3) {
                this.n = 0
            }
        },
        prevTree() {
            this.n--;
            if (this.n < 0) {
                this.n = 3
            }
        },
        condition(index) {
            if (index === this.n) {
                return true
            }
        },
        changeN(i) {
            this.n = i;
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/mixins' as *;
@use '../assets/partials/variables' as *;

.color-special {
    color: $col4;
}

.color-dots {
    color: $col1-1;
}

.background {
    background-color: $col11;
}

.h4sp {
    color: $col4;
    padding-bottom: 30px;
}

h1 {
    color: $col1-2;
    font-size: 3rem;
    font-weight: bold;
}

.thinner {
    font-size: 3rem;
    color: $col4;
    font-weight: 200;
}

.card-member {
    width: 30%;
    background-color: $col1;
    position: relative;
    padding: 65px 30px;
    border-radius: 6px;
    box-shadow: 10px 5px 5px 5px $col5;
}

.profile-pic {
    width: 150px;
    position: absolute;
    bottom: 80%;
    left: 32%;
    margin-bottom: 20px;
}

.profile-pic img {
    width: 100%;
    border-radius: 50%;
}

.info {
    color: $col5;
}

.card-member span {
    color: $col1-1;
    font-weight: 500;
}

.btncol {
    background-color: $col1-1;
    color: white;

    &:hover {
        background-color: $col4;
        color: white;
    }
}
</style>