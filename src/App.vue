<template>
    <div>
        <button @click="isOpen = !isOpen">Is open?</button>
        <p>Returned value: {{ returnedValue }}</p>

        <Dialog v-if="isOpen">
            <Button :returnValue="true" @buttonClick="returnedValue = $event"
                >Yes</Button
            >
            <Button :returnValue="false" @buttonClick="returnedValue = $event"
                >No</Button
            >
        </Dialog>
    </div>
</template>

<script>
import DialogVue from "./components/Dialog.vue";
import ButtonVue from "./components/Button.vue";
import { ref } from "vue";

export default {
    name: "App",
    components: {
        Dialog: DialogVue,
        Button: ButtonVue,
    },
    setup() {
        const isOpen = ref(false);
        const returnedValue = ref(null);

        return { isOpen, returnedValue };
    },
};
</script>
