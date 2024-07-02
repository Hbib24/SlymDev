<template>
    <!-------------------------------

        INSTEAD OF A FULL PAGE DEDICATED TO A MENU I OPTED FOR A DRAWER MENU FOR MOBILE
        AS I THINK ITS MORE COMMON IN MODERN APPS AND DELIVERS A BETTER UX

    --------------------------------->

    <div id="sidebar-nav" class="fixed top-0 left-0 z-40 h-screen p-4 bg-white w-3/4 overflow-y-auto transition-transform -translate-x-full" >
        <Sidebar />
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

                        PAGE CONTENT SHOULD BE RENDERED THROUGH A ROUTER OUTLET SO THAT PAGE CHANGES WITH ROUTING

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
