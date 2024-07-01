<template>
    <div class="p-4 h-dvh">
        <div class="flex justify-between mb-4">
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
        <div class="flex gap-3">
            <div class="w-96 bg-white rounded-xl p-4">
                <!-- Sidebar content -->
            </div>
            <div class="flex-1 rounded-xl w-full bg-white/50">
                <!-- Main content -->
            </div>
        </div>
    </div>
</template>

<script>
export default {};
</script>

<style>
.back-btn {
    background-color: rgb(223, 229, 241);
    span {
        font-size: 16px;
        text-align: center;
    }
}
</style>
