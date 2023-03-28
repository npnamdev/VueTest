<template>
  <div id="wp-content">
    <h3>Sản Phẩm</h3>
    <div id="main-product">
      <li v-for="product in $store.state.products" :key="product.id">
        <a href="#">
          <div class="image">100x100</div>
          <h5>{{ product.name }}</h5>
          <span>{{ product.price }}$</span>
          <button @click="$store.commit('addToCart', product)">
            Add to cart
          </button>
        </a>
      </li>
    </div>
    <br />
    <div>{{ $store.state.cartProducts }}</div>
  </div>
</template>

