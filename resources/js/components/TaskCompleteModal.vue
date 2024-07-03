<template>
    <div
        id="task-complete-modal"
        tabindex="-1"
        aria-hidden="true"
        class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full"
    >
        <div class="relative p-4 w-full max-w-2xl max-h-full">
            <div
                class="relative bg-white/80 rounded-3xl shadow dark:bg-gray-700 animate__animated animate__faster animate__fadeIn animate__zoomIn"
            >
                <div
                    class="flex-col w-full text-center items-center justify-center p-8"
                >
                    <div class="flex justify-center">
                        <Animation v-if="earned == 500" />
                        <img
                            :src="diamond"
                            alt="diamond"
                            class="w-60 animate__animated animate__tada"
                        />
                    </div>
                    <div class="text-2xl font-bold">
                        Congratulations You've Earned
                    </div>
                    <div class="my-6">
                        <span
                            id="earned"
                            class="text-3xl hidden font-bold text-featured absolute inline-flex opacity-75 text-featured"
                        >
                            {{ earned }} <span class="text-3xl">XP</span>
                        </span>
                        <span class="text-3xl font-bold text-featured">
                            {{ earned }} <span class="text-3xl">XP</span>
                        </span>
                    </div>
                    <button
                        @click="instance.hide()"
                        class="h-16 w-full rounded-xl bg-featured font-bold text-white"
                    >
                        Yeahhhhhhhhhhhhhh !
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import diamond from "../../assets/Diamond.svg";
import Animation from "./Animation.vue";
import { Modal } from "flowbite";
export default {
    components: { Animation },
    props: { showTaskComplete: Boolean, instance: Modal },
    watch: {
        showTaskComplete() {
            if (this.showTaskComplete) {
                const ele = document.getElementById("earned");
                ele.classList.add("hidden");
                ele.classList.remove("animate-ping");
                this.earned = 0;
                const int = setInterval(() => {
                    if (this.earned == 500) {
                        clearInterval(int);
                        ele.classList.remove("hidden");
                        ele.classList.add("animate-ping");
                    } else {
                        this.earned++;
                    }
                }, 7);
            }
        },
    },
    data() {
        return { diamond, earned: 0 };
    },
};
</script>
