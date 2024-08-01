<template>
    <table class="table-auto">
        <tr>
            
            <td class="text-2xl" v-if="!props.download">
                <h2>
                    Profiel
                </h2>
            </td>
            <td v-if="props.download" colspan="2">
                <h2>
                    &lt;Profiel /&gt;
                </h2>
            </td>
        </tr>
        <tr v-if="!props.download">
            <td class="font-bold">Naam</td>
            <td class="pl-3">Thor Demeestere</td>
        </tr>
    </table>
</template>

<script setup lang="ts">

    const props = defineProps<{
        download: boolean;
    }>();
    
</script>

<style scoped>
    td + td:before {
        content: ":";
        padding-right: 1rem;
    }
</style>
