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
                    <div class="text-3xl font-bold">
                        Congratulations You've Earned
                    </div>
                    <div class="text-4xl font-bold text-featured my-6">
                        500 <span class="text-3xl">XP</span>
                    </div>

                    <button
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
export default {};
</script>
