<template>
    <div class="flex justify-between items-center h-20">
        <div class="flex items-center">
            <button
                class="hidden lg:block rounded-lg back-btn bg-gray-300/50 hover:bg-gray-300 w-10 h-10"
            >
                <span class="material-symbols-rounded ml-1">
                    arrow_back_ios
                </span>
            </button>
            <button
                data-drawer-target="sidebar-nav"
                data-drawer-show="sidebar-nav"
                aria-controls="sidebar-nav"
                class="block lg:hidden rounded-lg back-btn bg-gray-300/50 hover:bg-gray-300 w-10 h-10"
            >
                <span class="material-symbols-rounded"> menu </span>
            </button>
            <span class="mx-3 font-semibold hidden md:block">Messages</span>
        </div>
        <button class="rounded-full">
            <img
                class="inline-block h-12 w-12 rounded-full ring-2 ring-white"
                src="https://randomuser.me/api/portraits/women/51.jpg"
                alt="user"
            />
        </button>
    </div>
</template>

<script>
export default {};
</script>
