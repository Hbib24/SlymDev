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
                        <Animation v-if="showAnim" />
                        <span
                            class="material-symbols-rounded fill text-featured animate__animated animate__tada"
                            style="font-size: 6.3rem"
                            >check_circle</span
                        >
                    </div>
                    <div
                        class="text-2xl font-bold animate__animated animate__fadeInDown"
                    >
                        Congratulations You've Completed
                    </div>
                    <div
                        class="mt-2 mb-6 animate__animated animate__fadeInDown"
                        style="animation-delay: 500ms"
                    >
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
                        class="flex justify-between items-center my-6 w-1/2 font-bold mx-auto animate__animated animate__fadeInDown"
                        style="animation-delay: 1000ms"
                    >
                        <span class="text-gray-500">Total XP earned</span>
                        <div
                            class="text-md text-featured flex items-center animate__animated animate__tada"
                            style="animation-delay: 1500ms"
                        >
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
    watch: {
        showTourFinish() {
            this.showAnim = false;
            if (this.showTourFinish) {
                setTimeout(() => {
                    this.showAnim = true;
                }, 1500);
            }
        },
    },
    data() {
        return { diamond, showAnim: false };
    },
};
</script>
