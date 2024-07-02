<template>
    <div class="flex justify-between items-center h-20">
        <div class="flex items-center">
            <button
                type="button"
                data-drawer-target="sidebar-nav"
                data-drawer-show="sidebar-nav"
                aria-controls="sidebar-nav"
                class="md:hidden rounded-lg hover:bg-gray-300 bg-gray-300/50 w-10 h-10"
            >
                <span class="material-symbols-rounded text-xl"> menu </span>
            </button>
            <button
                type="button"
                class="hidden md:block rounded-lg hover:bg-gray-300 bg-gray-300/50 w-10 h-10"
            >
                <span class="material-symbols-rounded text-xl">
                    arrow_back
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
</template>
