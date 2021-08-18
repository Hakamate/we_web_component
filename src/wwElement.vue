<template>
    <div class="my-element w-full grid grid-cols-2">
        <div v-for="i in 10" :key="i" class="flex items-center p-4 bg-white border-2 border-gray-200 rounded-lg shadow-sm dark:bg-gray-800">
            <img alt="mountain" class="w-45 rounded-md border-2 border-gray-300" src="https://picsum.photos/seed/picsum/200" />
            <div id="body" class="flex flex-col ml-5">
                <h4 id="name" class="text-xl font-semibold mb-2">{{ wwLang.getText(content.title) }}</h4>
                <p id="job" class="text-gray-800 mt-2">Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
                <div class="flex mt-5">
                    <img alt="avatar" class="w-6 rounded-full border-2 border-gray-300" src="https://picsum.photos/seed/picsum/200" />
                    <p class="ml-3">John Doe</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import './index.css'
export default {
    name: "__COMPONENT_NAME__",
    wwDefaultContent: {
        textColor: "#F23636",
        title: { en: "My title" },
    },
    props: {
        content: { type: "Object", required: true },
    },
    data() {
        return {
            wwLang: wwLib.wwLang,
        };
    },
    computed: {
        textStyle() {
            return {
                color: this.content.textColor,
            };
        },
    },
};
</script>

<style lang="scss" scoped>

</style>
