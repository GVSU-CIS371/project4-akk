<template>
  <v-card height="100%">
    <v-img
      :src="product.data.image"
      :alt="product.data.name"
      height="200"
    ></v-img>
    <v-card-title>
      {{ product.data.name }}
    </v-card-title>
    <v-card-subtitle>
      {{ product.data.category }}
    </v-card-subtitle>
    <v-card-text>
      <p>Price: ${{ product.data.price }}</p>
      <p>Rating: {{ product.data.rating }}</p>
      <p>{{ product.data.description }}</p>
    </v-card-text>
    <v-card-actions>
      <v-btn color="primary">Add to Cart</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script lang="ts" setup>
import { defineProps } from "vue";
import { ProductDoc } from "../types/product";

defineProps<{
  product: ProductDoc;
}>();
</script>

