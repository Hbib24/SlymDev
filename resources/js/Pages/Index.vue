<template>
    <div class="py-4 px-2 h-dvh">
        <div class="flex justify-between py-3">
            <div>
                <button class="rounded-lg back-btn w-10 h-10">
                    <span class="material-symbols-rounded ml-1">
                        arrow_back_ios
                    </span>
                </button>
                <span class="mx-3 font-semibold">Messages</span>
            </div>
            <button class="rounded-full">
                <img
                    class="inline-block h-12 w-12 rounded-full ring-2 ring-white"
                    src="https://randomuser.me/api/portraits/women/51.jpg"
                    alt="user"
                />
            </button>
        </div>
        <div class="flex gap-3" style="height: 92%;">
            <div class="w-96 bg-white rounded-xl p-4 hidden lg:block">
                 <Sidebar />
            </div>
            <div class="flex-1 rounded-xl w-full bg-white/50">
                <!-- Main content -->
                 <Content />
            </div>
        </div>
    </div>
</template>

<script>
import Sidebar from "./Sidebar.vue";
import Content from "./Content.vue";
export default {
    components: { Sidebar, Content },
};
</script>

<style>

</style>
