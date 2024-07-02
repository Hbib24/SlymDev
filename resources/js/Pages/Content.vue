<template>
    <div class="flex flex-col items-center gap-6 max-w-xl mx-auto">
        <div class="w-full h-20 animate__animated animate__fadeIn">
            <div class="flex justify-between items-center">
                <div class="flex gap-x-3">
                    <span
                        class="material-symbols-rounded fill text-2xl text-featured"
                    >
                        auto_awesome
                    </span>
                    <div class="text-featured font-bold text-2xl">
                        Get Started
                    </div>
                </div>
                <div>
                    <div id="total-xp" class="text-featured font-bold">
                        You earned {{ earnings.toLocaleString("fr") }}
                    </div>
                    <div
                        id="xp-to-earn"
                        class="text-xs text-gray-500 font-semibold invisible"
                    >
                        Total XP to earn: 12 000
                    </div>
                </div>
            </div>
            <div
                id="progress-bar"
                class="w-full rounded-full bg-white flex items-center mt-4 p-1 shadow-sm"
            >
                <div
                    class="bg-blue-400 h-2 rounded-full bg-featured ease-out duration-300"
                    :style="{ width: completionPercent + '%' }"
                ></div>
            </div>
        </div>

        <!-------------------------------

            IN A REAL APP THIS CARD WOULD BE A COMPONENT WITH DYNAMIC CONTENT PROJECTION
            BUT SINCE THIS IS A TEST I FOCUSED ON DESIGN RATHER THAN OPTIMIZATION  

        --------------------------------->
        <div
            class="w-full bg-white p-5 shadow-sm rounded-xl flex flex-col items-center animate__animated animate__fadeIn hover:scale-105 ease-out duration-300 cursor-pointer"
        >
            <img :src="img" />

            <div class="mt-6 flex justify-between items-center w-full">
                <div class="flex gap-2">
                    <span class="material-symbols-rounded fill text-featured"
                        >check_circle</span
                    >
                    <div>
                        <div class="line-through text-gray-700 font-bold">
                            Create more inbox
                        </div>

                        <div class="text-gray-500 mt-2 text-xs">
                            Create more inbox, welcome your new contact by a
                            message
                        </div>
                    </div>
                </div>
                <div class="text-featured font-bold flex items-center">
                    <span class="material-symbols-rounded">check </span>
                    <span> 500 <small>XP</small></span>
                </div>
            </div>
        </div>

        <div
            class="w-full bg-white p-5 shadow-sm rounded-xl flex flex-col items-center animate__animated animate__fadeIn hover:scale-105 ease-out duration-300 cursor-pointer"
        >
            <img class="w-full" :src="img3" />

            <div class="mt-6 flex justify-between items-center w-full">
                <div class="flex gap-2">
                    <span class="material-symbols-rounded text-featured"
                        >radio_button_unchecked</span
                    >
                    <div>
                        <div class="font-bold">Manage your messaging rules</div>

                        <div class="text-gray-500 mt-2 text-xs">
                            Create more inbox, welcome your new contact by a
                            message
                        </div>
                    </div>
                </div>
                <div class="text-featured font-bold flex items-center">
                    <span class="">+ </span>
                    <span> 100 <small>XP</small></span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import img from "../../assets/inboxGuide.png";
import img2 from "../../assets/inboxGuide.png";
import img3 from "../../assets/video.png";
import check from "../../assets/check.png";
export default {
    data() {
        return {
            img,
            img2,
            img3,
            check,
            completionPercent: 0,
            earnings: 0,
        };
    },
    mounted() {
        const int = setInterval(() => {
            if (this.completionPercent == 50) {
                clearInterval(int);
                [
                    document.getElementById("progress-bar"),
                    document.getElementById("total-xp"),
                ].forEach((ele) => {
                    ele.classList.add("animate__animated");
                    ele.classList.add("animate__pulse");
                });

                const ele = document.getElementById("xp-to-earn");
                ele.classList.remove("invisible");
                ele.classList.add("animate__animated");
                ele.classList.add("animate__fadeInDown");
            } else {
                this.completionPercent += 1;
                this.earnings += 550;
            }
        }, 20);
    },
};
</script>
