<template>
    <h3>{{ title }} <a href="#" @click.prevent="isCode = !isCode">{{ isCode ? 'Show Preview' : 'Show Code' }}</a></h3>
    <section>
        <div v-if="!isCode" v-html="code"></div>
        <div v-if="isCode">
            <pre>
                {{ code }}
            </pre>
        </div>
    </section>
</template>

<script lang="ts">
    import { defineComponent, ref } from 'vue';

    export default defineComponent({
        name: 'CodePreview',
        props: {
            title: String,
            code: String
        },
        setup () {
            const isCode = ref(false);

            return {
                isCode
            };
        }
    });
</script>
