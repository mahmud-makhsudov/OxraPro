<template>
  <div class="card-page">
    <ul class="breadcrumb">
      <li class="breadcrumb__item"><a href="#">Мои компании</a></li>
      <li class="breadcrumb__item"><span>Карточка компании</span></li>
    </ul>
    <h5 class="title">Карточка компании</h5>
    <div class="tabs">
      <b-tabs>
        <b-tab title="Детальная информация" active>
          <div class="tabs__content">
        <div class="list">
          <div class="line">
            <div class="line__label">Название компании</div>
            <div class="line__value">Какое-то название компании</div>
          </div>
          <div class="line">
            <div class="line__label">Телефон</div>
            <div class="line__value">+ 7 911 000 00 00</div>
          </div>
          <div class="line">
            <div class="line__label">E-mail</div>
            <div class="line__value"><a href="#">ivanov@mail.ru</a></div>
          </div>
          <div class="line">
            <div class="line__label">Сайт</div>
            <div class="line__value"><a href="#">site.com</a></div>
          </div>
          <div class="line">
            <div class="line__label">Сфера деятельности</div>
            <div class="line__value">
              <div class="line__value-items">
                <div class="line__value-item">ИНН	7712345678 <br> КПП	779101001 <br> БИК	044521234</div>
                <div class="line__value-item">Р/С	40702810123450101230 <br> К/С	30101234500000000225 <br> ОКПО	12345678</div>
                <div class="line__value-item">ОКАТО	87654321000 <br> ОКВЭД (основной)	18.15 <br> ОГРН	1047712345678</div>
              </div>
            </div>
          </div>
          <div class="line">
            <div class="line__label">Номер Договора </div>
            <div class="line__value">3434341232</div>
          </div>
          <div class="line">
            <div class="line__label">Скан-копия договора</div>
            <div class="line__value"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></div>
          </div>
          <div class="line">
            <div class="line__label">Список необходимых обучений</div>
            <div class="line__value">Список необходимых обучений</div>
          </div>
          <div class="line">
            <div class="line__label">Используемое Эдо</div>
            <div class="line__value">Система Электронного документооборота</div>
          </div>
          <div class="line">
            <div class="line__label">Количество сотрудников в компании</div>
            <div class="line__value">Более 500 человек</div>
          </div>
        </div>
      </div>
        </b-tab>
        <b-tab title="Список сотрудников">
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Molestias deleniti eos autem adipisci illum, repellat, ullam magni minus ipsum quae consequatur enim perspiciatis quidem consectetur fugit veritatis, debitis labore sapiente.
          </p>
        </b-tab>
        <b-tab title="Сделки">          
          <div class="deal">
            <div class="deal__top">
              <div class="deal__top-item">
                <label for="example-datepicker">Дата создания с</label>
                <input type="date" id="example-datepicker">
                <div class="date-picker__links">
                  <a href="#">Неделя</a>
                  <a href="#">Месяц</a>
                  <a href="#">Квартал</a>
                  <a href="#">Год</a>
                </div>
              </div>
              <div class="deal__top-item">
                <label for="example-datepicker-2">по</label>
                <input type="date" id="example-datepicker-2">
              </div>
              <div class="deal__top-item">
                <label>Стадии обучения</label>
                <b-form-select v-model="selected" :options="options" size="sm"></b-form-select>
              </div>
              <div class="deal__top-item">
                <label for="num">Номер договора</label>
                <input type="number" id="num" placeholder="Введите номер договора">
              </div>
            </div>
            <table class="deal__table">
              <tr>
                <td class="id">ID</td>
                <td class="date-of-creation">дата создания</td>
                <td class="learning-stage">Стадия обучения</td>
                <td class="company">Компания</td>
                <td class="summ">Сумма, Руб.</td>
                <td class="contract-no">№ договора</td>
                <td class="scanner">Скан счета, договора, акты</td>
              </tr>
              <tr>
                <td class="id">34334</td>
                <td class="date-of-creation"><a href="#">20.06.2021</a></td>
                <td class="learning-stage">Пройдено</td>
                <td class="company">Название компании </td>
                <td class="summ"><a href="#">23 000 руб.</a></td>
                <td class="contract-no">3434341232</td>
                <td class="scanner"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></td>
              </tr>
              <tr>
                <td class="id">34334</td>
                <td class="date-of-creation"><a href="#">20.06.2021</a></td>
                <td class="learning-stage">Пройдено</td>
                <td class="company">Название компании </td>
                <td class="summ"><a href="#">23 000 руб.</a></td>
                <td class="contract-no">3434341232</td>
                <td class="scanner"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></td>
              </tr>
              <tr>
                <td class="id">34334</td>
                <td class="date-of-creation"><a href="#">20.06.2021</a></td>
                <td class="learning-stage">Пройдено</td>
                <td class="company">Название компании </td>
                <td class="summ"><a href="#">23 000 руб.</a></td>
                <td class="contract-no">3434341232</td>
                <td class="scanner"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></td>
              </tr>
              <tr>
                <td class="id">34334</td>
                <td class="date-of-creation"><a href="#">20.06.2021</a></td>
                <td class="learning-stage">Пройдено</td>
                <td class="company">Название компании </td>
                <td class="summ"><a href="#">23 000 руб.</a></td>
                <td class="contract-no">3434341232</td>
                <td class="scanner"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></td>
              </tr>
              <tr>
                <td class="id">34334</td>
                <td class="date-of-creation"><a href="#">20.06.2021</a></td>
                <td class="learning-stage">Пройдено</td>
                <td class="company">Название компании </td>
                <td class="summ"><a href="#">23 000 руб.</a></td>
                <td class="contract-no">3434341232</td>
                <td class="scanner"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></td>
              </tr>
              <tr>
                <td class="id">34334</td>
                <td class="date-of-creation"><a href="#">20.06.2021</a></td>
                <td class="learning-stage">Пройдено</td>
                <td class="company">Название компании </td>
                <td class="summ"><a href="#">23 000 руб.</a></td>
                <td class="contract-no">3434341232</td>
                <td class="scanner"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></td>
              </tr>
              <tr>
                <td class="id">34334</td>
                <td class="date-of-creation"><a href="#">20.06.2021</a></td>
                <td class="learning-stage">Пройдено</td>
                <td class="company">Название компании </td>
                <td class="summ"><a href="#">23 000 руб.</a></td>
                <td class="contract-no">3434341232</td>
                <td class="scanner"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></td>
              </tr>
              <tr>
                <td class="id">34334</td>
                <td class="date-of-creation"><a href="#">20.06.2021</a></td>
                <td class="learning-stage">Пройдено</td>
                <td class="company">Название компании </td>
                <td class="summ"><a href="#">23 000 руб.</a></td>
                <td class="contract-no">3434341232</td>
                <td class="scanner"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></td>
              </tr>
              <tr>
                <td class="id">34334</td>
                <td class="date-of-creation"><a href="#">20.06.2021</a></td>
                <td class="learning-stage">Пройдено</td>
                <td class="company">Название компании </td>
                <td class="summ"><a href="#">23 000 руб.</a></td>
                <td class="contract-no">3434341232</td>
                <td class="scanner"><button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button></td>
              </tr>
            </table>
            <div class="deal__bottom">
              <div class="pagination">
                <b-pagination v-model="currentPage" :total-rows="rows"></b-pagination>
              </div>
              <div class="companies-top__filter">
                <div class="companies-top__filter-text">Показать по</div>
                <div class="select">
                  <b-form-select v-model="selectBottom" :options="selectBottomOptions" size="sm"></b-form-select>
                </div>
              </div>
            </div>
          </div>
        </b-tab>
        <b-tab title="Статистика">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium voluptatem tempore ex facilis aperiam placeat, sint minus iusto ipsa ut vel magnam, fugiat laudantium architecto? Ratione perferendis a enim incidunt!
          </p>
        </b-tab>
        <b-tab title="Информация о сделке">
          <button class="btn-exit">Назад</button>
          <div class="tabs__content">
            <b-tabs pills card vertical>
              <b-tab title="Информация по сделке" active>
                  <div class="tab__title">Информация о сделке</div>
                  <div class="list tab__content-list">
                    <div class="line">
                      <div class="line__label">ID</div>
                      <div class="line__value">13462321</div>
                    </div>
                    <div class="line">
                      <div class="line__label">ДАТА СОЗДАНИЯ</div>
                      <div class="line__value">20.06.2021</div>
                    </div>
                    <div class="line">
                      <div class="line__label">Стадия обучения</div>
                      <div class="line__value">Пройдено</div>
                    </div>
                    <div class="line">
                      <div class="line__label">Название компании</div>
                      <div class="line__value">Какое-то название компании</div>
                    </div>
                    <div class="line">
                      <div class="line__label">Сумма, Руб.</div>
                      <div class="line__value"><a href="#">23 000 руб.</a></div>
                    </div>
                    <div class="line">
                      <div class="line__label">Номер договора </div>
                      <div class="line__value">3434341232</div>
                    </div>
                    <div class="line">
                      <div class="line__label">Список программ</div>
                      <div class="line__value">
                        <ul>
                          <li>Обучения по пожарной безопасности, 7 мест, 2590 руб.</li>
                          <li>Обучения по средствам индивидуальной защиты, 5 мест, 2360 руб.</li>
                        </ul>
                      </div>  
                    </div>
                    <div class="line">
                      <div class="line__label">Скан счета, договора</div>
                      <div class="line__value">
                        <button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button>
                      </div>
                    </div>
                    <div class="line">
                      <div class="line__label">АКТЫ</div>
                      <div class="line__value">
                        <button @click="$bvModal.show('modal-scoped')" class="line__value-btn">Посмотреть файлы (3 шт)</button>
                      </div>
                    </div>
                </div>
              </b-tab>
              <b-tab title="Счета сделки"><b-card-text>Tab contents 2</b-card-text></b-tab>
              <b-tab title="Журнал слушателей"><b-card-text>Tab contents 3</b-card-text></b-tab>
              <b-tab title="Статистика"><b-card-text>Tab contents 3</b-card-text></b-tab>
              <b-tab title="Матрица обучений"><b-card-text>Tab contents 3</b-card-text></b-tab>
            </b-tabs>
          </div>
        </b-tab>
      </b-tabs>

    </div>

  <b-modal id="modal-scoped" size="lg">
    <template #modal-header="{ close }">
      <div class="modal__header">
        <h5 class="modal__title">Просмотр файлов</h5>
        <button class="modal__btn" @click="close()">
          <img src="@/assets/icons/x.svg" alt="x">
        </button>
      </div>
    </template>

    <template #default>
      <div class="modal__content">
        <img src="@/assets/sreen-1.png" alt="text">
        <img src="@/assets/sreen-2.png" alt="text">
        <div class="modal__content-filename">скан2.pdf</div>
      </div>
    </template>

    <template #modal-footer>
      <div class="modal-footer__inner">
        <div class="modal-footer__nav">
          <button class="modal-footer__nav-btn">
            <img src="../../assets/prev.svg" alt="<">
          </button>
          <div class="modal-footer__nav-text">
            Файл 5<span> / 5</span>
          </div>
          <button class="modal-footer__nav-btn">
            <img src="../../assets/next.svg" alt=">">
          </button>
        </div>
        <button class="modal-footer__btn">Скачать</button>
      </div>
    </template>
  </b-modal>


  </div>
</template>

<script>
  export default {
    data() {
      return {
        show: false,
        selected: 'a',
        selectBottom: 'a',
        rows: 50,
        currentPage: 1,
        options: [
          { value: 'a', text: 'Выберите стадию обучения' },
          { value: 'b', text: 'Выберите стадию обучения' },
          { value: 'c', text: 'Выберите стадию обучения' },
          { value: 'd', text: 'Выберите стадию обучения' }
        ],
        selectBottomOptions: [
          { value: 'a', text: 10 },
          { value: 'b', text: 20 },
          { value: 'c', text: 30 },
          { value: 'd', text: 40 }
        ]
      }
    }
  }
</script>

<style src="./Card.scss" lang="scss">