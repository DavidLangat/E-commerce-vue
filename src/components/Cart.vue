<template>
  <div class="cart">
    <h5 class="cart__heading">Your shopping cart</h5>
    <div v-if="cart.line_items.length">
      <CartItem
        v-for="lineItem in cart.line_items"
        :key="lineItem.id"
        :item="lineItem"
        @update-quantity="handleUpdateQuantity"
        @remove-from-cart="$emit('remove-from-cart', $event)"
        class="cart__inner"
      />
      <div class="cart__total">
        <p class="cart__total-title">Subtotal:</p>
        <p class="cart__total-price">{{ cart.subtotal.formatted_with_symbol }}</p>
      </div>
    </div>
    <div class="cart__footer">
      <button
        v-if="cart.line_items.length"
        @click="emptyCart"
        class="cart__btn-empty"
      >
        Empty cart
      </button>
      <p class="cart__none" v-else>You have no items in your shopping cart, start adding some!</p>
    </div>
  </div>
</template>

<script>
import CartItem from './CartItem'

export default {
  name: 'MyCartOne',
  components: {
    CartItem
  },
  props: ['cart'],
  data () {
    return {
      showCart: false
    }
  },
  methods: {
    /**
     * Updates line_items in cart
     * https://commercejs.com/docs/sdk/cart/#update-cart
     *
     * @param {string} lineItemId ID of the cart line item being updated
     * @param {number} quantity New line item quantity to update
     */
    handleUpdateQuantity (lineItemId, quantity) {
      this.$commerce.cart.update(lineItemId, { quantity }).then((resp) => {
      }).catch((error) => {
        console.log('There was an error updating the cart items', error)
      })
    },
    /**
     * Empty the entire cart
     * https://commercejs.com/docs/sdk/cart#empty-cart
     */
    emptyCart () {
      this.$emit('empty-cart')
    }
  }
}
</script>

<style lang="scss">
.cart {
    @apply bg-white border-2 border-blue;
    width: 350px;
    position: absolute;
    top: 10px;
    right: 10px;

    &__heading {
        @apply py-3 px-4 font-bold border-b-2 border-blue text-blue;
    }

    &__inner {
        @apply p-5;
    }

    &__total {
        @apply flex px-5 py-4 border-t-2 border-blue;
        justify-content: space-between;
    }

    &__total-title {
        @apply text-blue font-bold;
    }

    &__btn-empty {
        @apply bg-white border border-blue pl-5 mx-5 mb-5 py-2 px-3 text-xs uppercase text-blue font-bold;
    }

    &__none {
        @apply p-5 text-blue text-center;
    }
}

</style>
