<script setup>
import AppLayout from "@/Layouts/AppLayout.vue";

const items = [
    {
        text: "Dashboard",
        disabled: false,
        href: "dashboard",
    },
    {
        text: "Page 1",
        disabled: false,
        href: "page1",
    },
];
const desserts = [
    {
        name: "Frozen Yogurt",
        calories: 159,
    },
    {
        name: "Ice cream sandwich",
        calories: 237,
    },
    {
        name: "Eclair",
        calories: 262,
    },
    {
        name: "Cupcake",
        calories: 305,
    },
    {
        name: "Gingerbread",
        calories: 356,
    },
    {
        name: "Jelly bean",
        calories: 375,
    },
    {
        name: "Lollipop",
        calories: 392,
    },
    {
        name: "Honeycomb",
        calories: 408,
    },
    {
        name: "Donut",
        calories: 452,
    },
    {
        name: "KitKat",
        calories: 518,
    },
];
</script>
<template>
    <AppLayout title="Page 1">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Vuetify: Page 1
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    <v-card>
                        <v-table>
                            <thead>
                                <tr>
                                    <th class="text-left">Name</th>
                                    <th class="text-left">Calories</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr v-for="item in desserts" :key="item.name">
                                    <td>{{ item.name }}</td>
                                    <td>{{ item.calories }}</td>
                                </tr>
                            </tbody>
                        </v-table>
                    </v-card>
                </div>
            </div>
        </div>
    </AppLayout>
</template>
