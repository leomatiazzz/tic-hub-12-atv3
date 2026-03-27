<script lang="ts">
import { Shipment } from '@/enum/shipment.enum'
import { Product } from '@/model/product.model'
import { formatCurrency } from '@/utils/formatCurrency'
import { defineComponent } from 'vue'
import Card from 'primevue/card'
import Button from 'primevue/button'

export default defineComponent({
  components: {
    Card,
    Button,
  },
  emits: ['add-to-cart'],
  props: {
    product: {
      type: Product,
    },
  },
  data() {
    return {
      title: this.product?.title ?? '',
      price: formatCurrency(this.product?.discountedPrice ?? 0),
      hasDiscount: (this.product?.discountPercentage ?? 0) > 0,
      discountPercentage: (this.product?.discountPercentage ?? 0) + '% OFF',
      originalPrice: formatCurrency(this.product?.price ?? 0),
      hasFreeShipping: this.product?.shipment === Shipment.FREE,
    }
  },
})
</script>

<template>
  <Card
    unstyled
    class="product shadow-md transition-all duration-300 hover:-translate-y-0.5 hover:shadow-xl"
  >
    <template #content>
      <article class="product-content">
        <Button
          icon="pi pi-shopping-cart"
          rounded
          severity="info"
          class="add-to-cart"
          @click="$emit('add-to-cart')"
        />

        <div class="header">
          <figure class="image-container">
            <img :src="product?.image" :alt="title" class="image" />
          </figure>
        </div>

        <div class="content">
          <h1 class="title">{{ title }}</h1>

          <!-- sempre renderizado para garantir altura uniforme entre cards -->
          <p class="original-price" :style="{ visibility: hasDiscount ? 'visible' : 'hidden' }">
            {{ originalPrice }}
          </p>

          <h2 class="price">
            <span class="discount" v-if="hasDiscount">{{ discountPercentage }}</span>
            {{ price }}
          </h2>

          <p class="free-shipment" v-if="hasFreeShipping">Frete Grátis</p>
        </div>
      </article>
    </template>
  </Card>
</template>

<style scoped>
.product {
  background-color: #2d3748;
  border-radius: 12px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.product {
  transition:
    transform 0.25s ease,
    box-shadow 0.25s ease;
}

.product:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.4);
}

.product-content {
  position: relative;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.header {
  position: relative;
  flex-shrink: 0;
}

.image-container {
  align-items: center;
  background-color: #ffffff;
  display: flex;
  justify-content: center;
  height: 220px;
  overflow: hidden;
}

.image {
  max-height: 210px;
  max-width: 200px;
  object-fit: contain;
}

.content {
  flex: 1;
  display: flex;
  flex-direction: column;
  padding: 16px;
}

.title {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
  height: 2.8rem;
  font-size: 1rem;
  font-weight: 700;
  color: #e2e8f0;
  margin: 0 0 8px 0;
  line-height: 1.4;
}

.original-price {
  text-align: left;
  font-size: 0.875rem;
  color: #a0aec0;
  text-decoration: line-through;
  margin: 0 0 4px 0;
}

.price {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 1.4rem;
  font-weight: 700;
  color: #fff;
  margin: 0;
}

.discount {
  background-color: var(--color-green-200);
  border-radius: 4px;
  color: var(--color-green-800);
  font-size: 0.75rem;
  font-weight: 700;
  padding: 4px 8px;
  flex-shrink: 0;
}

.free-shipment {
  margin-top: auto;
  padding-top: 8px;
  text-align: left;
  color: var(--color-green-600);
  font-size: 0.85rem;
  font-weight: 700;
}

:deep(.add-to-cart.p-button) {
  position: absolute;
  top: 10px;
  right: 10px;
  width: 42px;
  height: 42px;
  padding: 0;
  z-index: 10;
}

:deep(.add-to-cart .p-button-icon) {
  font-size: 0.95rem;
}
</style>
