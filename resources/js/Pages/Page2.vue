<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";
import { useForm } from "@inertiajs/inertia-vue3";
import Card1 from "./../Components/Card1.vue";
import Card2 from "./../Components/Card2.vue";

const form = useForm({
    loading: false,
    selection: 1,
});

function reserve() {
    form.loading = true;
    setTimeout(() => (form.loading = false), 2000);
}
</script>
<template>
    <AppLayout title="Page 2">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Vuetify: Page 2
            </h2>
        </template>

        <v-app class="">
            <v-container>
                <v-row align="start" class="mb-2">
                    <v-col v-for="n in 12" :key="n" cols="12" md="4">
                        <Card2 />
                    </v-col>
                </v-row>
                <v-row>
                    <Card1 />
                </v-row>
            </v-container>
        </v-app>
    </AppLayout>
</template>
<style lang="scss" scoped></style>
