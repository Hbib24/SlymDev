<template>
    <!-------------------------------

        INSTEAD OF A FULL PAGE DEDICATED TO A MENU I OPTED FOR A DRAWER MENU FOR MOBILE
        AS I THINK ITS MORE COMMON IN MODERN APPS AND DELIVERS A BETTER UX

    --------------------------------->

    <div
        id="sidebar-nav"
        class="fixed top-0 left-0 z-40 h-screen bg-white sm:w-3/4 md:w-1/2 overflow-y-auto transition-transform -translate-x-full"
    >
        <div class="flex justify-between items-center p-4">
            <div class="flex items-center">
                <button
                    class="rounded-lg back-btn bg-gray-300/50 hover:bg-gray-300 w-10 h-10"
                >
                    <span class="material-symbols-rounded ml-1">
                        arrow_back_ios
                    </span>
                </button>

                <span class="mx-3 font-semibold">Messages</span>
            </div>
        </div>

        <div class="h-px w-full bg-gray-300"></div>

        <div class="p-4"><Sidebar /></div>
    </div>

    <div class="px-3 h-dvh">
        <Header />
        <div class="main flex gap-3">
            <div
                class="overflow-auto w-96 bg-white rounded-xl p-4 hidden lg:block"
            >
                <Sidebar />
            </div>
            <div
                class="overflow-y-auto overflow-x-hidden flex-1 rounded-xl w-full md:bg-white/50 md:p-6"
            >
                <!-------------------------------

                        PAGE CONTENT SHOULD BE RENDERED THROUGH A ROUTER OUTLET SO THAT CONTENT CHANGES WITH ROUTING

                --------------------------------->
                <Content />
            </div>
        </div>
    </div>
</template>

<script>
import Sidebar from "../components/Sidebar.vue";
import Header from "../components/Header.vue";
import Content from "../Pages/Content.vue";
export default {
    components: { Sidebar, Content, Header },
};
</script>

<style>
.main {
    height: calc(100dvh - 95px);
}
</style>
