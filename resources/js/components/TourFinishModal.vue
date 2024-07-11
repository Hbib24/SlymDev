<template>
    <div
        id="tour-finish-modal"
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
                    <div class="flex justify-center py-8">
                        <Animation v-if="earned == 500" />
                        <span
                            class="material-symbols-rounded fill text-featured animate__animated animate__tada"
                            style="font-size: 6.3rem"
                            >check_circle</span
                        >
                    </div>
                    <div class="text-2xl font-bold">
                        Congratulations You've Completed
                    </div>
                    <div class="mt-2 mb-6">
                        <span
                            id="earned"
                            class="text-3xl hidden font-bold text-featured absolute inline-flex opacity-75 text-featured"
                        >
                            DM Tour Guide
                        </span>
                        <span class="text-3xl font-bold text-featured">
                            DM Tour Guide
                        </span>
                    </div>
                    <div
                        class="flex justify-between items-center my-6 w-1/2 font-bold mx-auto"
                    >
                        <span class="text-gray-500">Total XP earned</span>
                        <div class="text-md text-featured flex items-center">
                            <span class="material-symbols-rounded text-base"
                                >check</span
                            >
                            <div>600 <span class="text-xs">XP</span></div>
                            <img :src="diamond" alt="diamond" class="w-12" />
                        </div>
                    </div>
                    <button
                        @click="instance.hide()"
                        class="h-16 w-full rounded-xl bg-featured font-bold text-white"
                    >
                        Done
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
    props: { showTourFinish: Boolean, instance: Modal },
    // watch: {
    //     showTourFinish() {
    //         if (this.showTourFinish) {
    //             const ele = document.getElementById("earned");
    //             ele.classList.add("hidden");
    //             ele.classList.remove("animate-ping");
    //             this.earned = 0;
    //             const int = setInterval(() => {
    //                 if (this.earned == 500) {
    //                     clearInterval(int);
    //                     ele.classList.remove("hidden");
    //                     ele.classList.add("animate-ping");
    //                 } else {
    //                     this.earned++;
    //                 }
    //             }, 5);
    //         }
    //     },
    // },
    data() {
        return { diamond };
    },
};
</script>
