<template>
  <section class="main-section orders">
    <div class="filtr-add-row">
        <div class="filter-blcok">
          <div class="filter-block__filter">
            
            <select name="" v-model="search">
              <option>Все заказы</option>
              <option>Новый</option>
              <option>Нуждаетя в подтверждении</option>
              <option>Изменен</option>
              <option>Выполняется</option>
              <option>Готов к отгрузке</option>
            </select>
          </div>
        </div>
        <div class="add-block">
          <a href="#" class="add-block__link">+ Добавить новый заказ</a>
        </div>
      </div>    

      <div class="main-section__content">
        <div class="main-section__item main-section__item_order" v-for="item in filterOrderStatus" :key="item.number">
          <div class="ms-item__col ms-item__col_order-number">
            <div class="ms-item__title ms-item__title_big">
              Заказ № {{ item.number}}
            </div>
            <div class="ms-item__text">
              13:04, 01.03.2019
            </div>
          </div>
          <div class="ms-item__col ms-item__col_quantity">
            <div class="ms-item__title">
              Товар в заказе:
            </div>
            <div class="ms-item__text">
              5 шт
            </div>
          </div>

          <div class="ms-item__col ms-item__col_name">
            <div class="ms-item__title">
              Клиент:
            </div>
            <div class="ms-item__text">
              Иванов В.В., ООО “Ласунка”
            </div>
          </div>

          <div class="ms-item__col ms-item__col_estimate">
            <div class="ms-item__title">
              Выполнить до:
            </div>
            <div class="ms-item__text">
              30.08.2019
            </div>
          </div>

          <div class="ms-item__col ms-item__col_status">
            <div class="ms-item__title">
              Статус:
            </div>
            <div class="ms-item__text">
              {{ item.status}}
            </div>
          </div>
        </div>      
        
      </div>

      <div class="pagination">
        <a href="#" class="pagination__link">1</a>
        <a href="#" class="pagination__link">2</a>
        <a href="#" class="pagination__link">3</a>
        <a href="#" class="pagination__link">4</a>
        <a href="#" class="pagination__link">5</a>
      </div>
  </section>
</template>
<script>
export default {
  name: 'order',

  data(){
    return {
      search: 'Все заказы',
      array: [
        {
          number: 12,
          date: '13:04, 01.03.2019',
          quantity: 5,
          client: 'Трахтенберг В.В., ООО “Ласунка”',
          estimate: '30.12.2019',
          status: 'Новый'
        },
        {
          number: 13,
          date: '13:04, 01.03.2019',
          quantity: 5,
          client: 'Трахтенберг В.В., ООО “Ласунка”',
          estimate: '30.01.2020',
          status: 'Нуждаетя в подтверждении'
        }
      ]
    }
  },
  computed: {
    filterOrderStatus(){
      const filtered = this.array.filter(item => {
        if(this.search==='Все заказы') return true;
        else return item.status.indexOf(this.search) > -1;
      })
      return filtered
    }
  }
}
</script>