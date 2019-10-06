<template>
  <div id="wrapper-sidebar">
    <div class="sidebar-back"></div>   
    <div class="sidebar__header">
      <div class="sidebar__logo"></div>  
    </div>
    <div class="sidebar__content">
      <ul class="sidebar__list">
        <li class="sidebar__item">
          <router-link class="sidebar__link sidebar__link_order" :to="'/'">
            Заказы
          </router-link>
        </li>
        <li class="sidebar__item">
          <router-link class="sidebar__link sidebar__link_cards" :to="'/cards'">Техкарты</router-link>
        </li>
        <li class="sidebar__item">
          <router-link class="sidebar__link sidebar__link_users" :to="'/users'">Пользователи</router-link>
        </li>
        <li class="sidebar__item">
          <router-link class="sidebar__link sidebar__link_entities" :to="'/entities'">Юридические лица</router-link>
        </li>
        <li class="sidebar__item">
          <router-link class="sidebar__link sidebar__link_abc" :to="'/abc'">Группа компаний</router-link>
        </li>
        <li class="sidebar__item">
          <router-link class="sidebar__link sidebar__link_news" :to="'/news'">Новости</router-link>
        </li>
        <li class="sidebar__item">
          <router-link class="sidebar__link sidebar__link_text" :to="'/'">Текст главной</router-link>
        </li>
      </ul>
      
    </div>
    
  </div>  
</template>

<script>
export default {
  name: 'Navigation'
}
</script>