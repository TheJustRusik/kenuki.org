<template>
    <div>
        <v-card>
            <v-img
                height="300px"
                :src=image
                cover
            ></v-img>

            <v-card-title>
                {{ title }}
            </v-card-title>

            <v-card-subtitle>
                {{ subtitle }}
            </v-card-subtitle>

            <v-card-actions>
                <v-btn
                color="orange-lighten-2"
                text="Explore"
                ></v-btn>

                <v-spacer></v-spacer>

                <v-btn
                :icon="showDescription ? 'mdi-chevron-up' : 'mdi-chevron-down'"
                @click="showDescription = !showDescription"
                ></v-btn>
            </v-card-actions>

            <v-expand-transition>
                <div v-show="showDescription">
                <v-divider></v-divider>

                <v-card-text>
                    {{ text }}
                </v-card-text>
                </div>
            </v-expand-transition>
        </v-card>
    </div>
</template>

<script setup>
    import { ref } from 'vue';

    let showDescription = ref(false)

    defineProps({
        title: String,
        subtitle: String,
        text: String,
        image: String
    })
</script>