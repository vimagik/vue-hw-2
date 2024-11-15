<script setup>
const props = defineProps(['product-data'])
</script>

<template>
    <div>
        <v-card class="mx-3 my-2 d-flex flex-column" width="350" height="100%">
            <v-img class="mt-2" :src="props.productData.image" max-height="200"></v-img>
            <v-card-text>
                <p class="text-h6">{{ props.productData.title }}</p>
                <p class="font-weight-black">{{ props.productData.price }} тубриков</p>
                <div class="d-flex flex-row ga-2 mt-2">
                    <v-chip prepend-icon="mdi-bookmark-check" color="primary">
                        {{ props.productData.category }}
                    </v-chip>
                    <v-rating readonly :length="5" :size="32" :model-value="props.productData.rating.rate"
                        active-color="primary" half-increments />
                </div>
                <p class="mt-3">{{ props.productData.description }}</p>
            </v-card-text>
            <v-card-actions class="align-end">
                <v-btn color="primary">Купить</v-btn>
            </v-card-actions>
        </v-card>
    </div>
</template>