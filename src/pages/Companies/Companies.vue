<template>
  <div class="companies">
    <div class="companies-top">
      <h5 class="companies-top__title">Мои компании</h5>
      <div class="companies-top__filter">
        <div class="companies-top__filter-text">Показать по</div>
        <div class="select">
        <b-form-select v-model="selected" :options="options" size="sm"></b-form-select>
        </div>
      </div>
    </div>

    <div class="companies__table">
      <table class="companies__table-top">
        <tr class="companies__table-titles">
          <td class="cell cell-1"><span>Название компании </span> <button><img src="../../assets/icons/change.svg" alt="><"></button></td>
          <td class="cell cell-2">номер договора</td>
          <td class="cell cell-3">ИНН</td>
          <td class="cell cell-4">Телефон</td>
          <td class="cell cell-5">email</td>
        </tr>
        <tr class="companies__table-inputs">
          <td class="cell cell-1"><input type="text" placeholder="Введите название компании"></td>
          <td class="cell cell-2"><input type="number" placeholder="Введите номер "></td>
          <td class="cell cell-3"><input type="number" placeholder="Введите ИНН "></td>
          <td class="cell cell-4"><input type="tel" placeholder="Введите телефон "></td>
          <td class="cell cell-5"><input type="email" placeholder="Введите email "></td>
        </tr>
      </table>
      <table class="companies__table-content">
        <tr>
          <td class="cell cell-1"><a href="#">Название компании 1</a></td>
          <td class="cell cell-2">4353535353</td>
          <td class="cell cell-3">435222222</td>
          <td class="cell cell-4">+ 7 911 000 00 00</td>
          <td class="cell cell-5"><a href="#">ivanov@mail.ru</a></td>
        </tr>
        <tr>
          <td class="cell cell-1"><a href="#">Название компании 1</a></td>
          <td class="cell cell-2">4353535353</td>
          <td class="cell cell-3">435222222</td>
          <td class="cell cell-4">+ 7 911 000 00 00</td>
          <td class="cell cell-5"><a href="#">ivanov@mail.ru</a></td>
        </tr>
        <tr>
          <td class="cell cell-1"><a href="#">Название компании 1</a></td>
          <td class="cell cell-2">4353535353</td>
          <td class="cell cell-3">435222222</td>
          <td class="cell cell-4">+ 7 911 000 00 00</td>
          <td class="cell cell-5"><a href="#">ivanov@mail.ru</a></td>
        </tr>
        <tr>
          <td class="cell cell-1"><a href="#">Название компании 1</a></td>
          <td class="cell cell-2">4353535353</td>
          <td class="cell cell-3">435222222</td>
          <td class="cell cell-4">+ 7 911 000 00 00</td>
          <td class="cell cell-5"><a href="#">ivanov@mail.ru</a></td>
        </tr>
        <tr>
          <td class="cell cell-1"><a href="#">Название компании 1</a></td>
          <td class="cell cell-2">4353535353</td>
          <td class="cell cell-3">435222222</td>
          <td class="cell cell-4">+ 7 911 000 00 00</td>
          <td class="cell cell-5"><a href="#">ivanov@mail.ru</a></td>
        </tr>
        <tr>
          <td class="cell cell-1"><a href="#">Название компании 1</a></td>
          <td class="cell cell-2">4353535353</td>
          <td class="cell cell-3">435222222</td>
          <td class="cell cell-4">+ 7 911 000 00 00</td>
          <td class="cell cell-5"><a href="#">ivanov@mail.ru</a></td>
        </tr>
        <tr>
          <td class="cell cell-1"><a href="#">Название компании 1</a></td>
          <td class="cell cell-2">4353535353</td>
          <td class="cell cell-3">435222222</td>
          <td class="cell cell-4">+ 7 911 000 00 00</td>
          <td class="cell cell-5"><a href="#">ivanov@mail.ru</a></td>
        </tr>
        <tr>
          <td class="cell cell-1"><a href="#">Название компании 1</a></td>
          <td class="cell cell-2">4353535353</td>
          <td class="cell cell-3">435222222</td>
          <td class="cell cell-4">+ 7 911 000 00 00</td>
          <td class="cell cell-5"><a href="#">ivanov@mail.ru</a></td>
        </tr>
      </table>
    </div>
    <div class="pagination">
    <b-pagination v-model="currentPage" :total-rows="rows"></b-pagination>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        rows: 50,
        currentPage: 1,
        selected: 'a',
        options: [
          { value: 'a', text: 10 },
          { value: 'b', text: 20 },
          { value: 'c', text: 30 },
          { value: 'd', text: 40 }
        ]
      }
    }
  }
</script>

<style src="./Companies.scss" lang="scss">