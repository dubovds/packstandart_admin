<template>
  <div class="header">
    <div class="header__search-block">
      <input type="text" class="header__input" placeholder="Search..">
    </div>
    <div class="header__info-block">
      <div class="header__ring">
        <div class="header__ring-icon">
          <div class="header__ring-alert" :class="{ show: isYouHaveMessage  }"></div>
        </div>
      </div>
      <div class="header__username">
        admin name
      </div>
    </div>
  </div>  
</template>

<script>
export default {
  name: 'Header',

  data() {
    return {
      isYouHaveMessage: true
    }
  }
}
</script>