<template>
    <div class="">
        <div class="flex justify-between items-center h-16">
            <span class="font-semibold">DM Setting</span>
            <button class="rounded-lg border w-10 h-10 hover:bg-gray-100">
                <span class="material-symbols-rounded mt-1"> close </span>
            </button>
        </div>

        <ul class="list-none menu-list my-4">
            <li
                class="menu-item selected my-1 flex items-center gap-3 p-3 rounded-lg cursor-pointer"
            >
                <span class="material-symbols-rounded fill text-featured"
                    >auto_awesome</span
                >
                <span class="text-featured">DM Tour Guide</span>
            </li>
        </ul>

        <span class="text-gray-400 text-xs">MANAGE INBOX</span>

        <ul class="list-none menu-list my-4">
            <li
                class="menu-item my-1 flex items-center gap-3 p-3 rounded-lg cursor-pointer"
            >
                <img :src="img4" />
                <span>Inbox</span>
            </li>
            <li
                class="menu-item my-1 flex items-center gap-3 p-3 rounded-lg cursor-pointer"
            >
                <img :src="img5" />
                <span>Discussion Rules </span>
            </li>
            <li
                class="menu-item my-1 flex items-center gap-3 p-3 rounded-lg cursor-pointer"
            >
                <img :src="img6" />
                <span>Adress Book</span>
            </li>
            <li
                class="menu-item my-1 flex items-center gap-3 p-3 rounded-lg cursor-pointer"
            >
                <img :src="img3" />
                <span>Zapier</span>
            </li>
        </ul>

        <span class="text-gray-400 text-xs">ADVANCED MESSAGES</span>

        <ul class="list-none menu-list my-4">
            <li
                class="menu-item my-1 flex justify-between items-center gap-3 p-3 rounded-lg cursor-pointer text-gray-400"
            >
                <div class="flex gap-3 items-center">
                    <img :src="img1" />
                    <span>Boost DM®</span>
                </div>
                <div class="text-xs">Coming soon</div>
            </li>
            <li
                class="menu-item my-1 flex justify-between items-center gap-3 p-3 rounded-lg cursor-pointer text-gray-400"
            >
                <div class="flex gap-3 items-center">
                    <img :src="img2" />
                    <span>Blurred DM®</span>
                </div>
                <div class="text-xs">Coming soon</div>
            </li>
        </ul>
    </div>
</template>

<script>
import img1 from "../../assets/boostDM.png";
import img2 from "../../assets/BlurredDM.png";
import img3 from "../../assets/Zapier.png";
import img4 from "../../assets/inbox.png";
import img5 from "../../assets/rules.png";
import img6 from "../../assets/adressBook.png";
export default {
    data() {
        return {
            img1,
            img2,
            img3,
            img4,
            img5,
            img6,
        };
    },
};
</script>

<style>
.menu-item {
    font-weight: 700;
    img {
        width: 24px;
    }
}

.menu-item:hover {
    background-color: #1752650d;
}

.menu-item.selected {
    background-color: #1752650d;
}
</style>
