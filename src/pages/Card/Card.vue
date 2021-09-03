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
        <b-tab title="Список сотрудников"><p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Molestias deleniti eos autem adipisci illum, repellat, ullam magni minus ipsum quae consequatur enim perspiciatis quidem consectetur fugit veritatis, debitis labore sapiente.</p></b-tab>
        <b-tab title="Сделки"><p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium voluptatem tempore ex facilis aperiam placeat, sint minus iusto ipsa ut vel magnam, fugiat laudantium architecto? Ratione perferendis a enim incidunt!</p></b-tab>
        <b-tab title="Статистика"><p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium voluptatem tempore ex facilis aperiam placeat, sint minus iusto ipsa ut vel magnam, fugiat laudantium architecto? Ratione perferendis a enim incidunt!</p></b-tab>
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
        variants: ['primary', 'secondary', 'success', 'warning', 'danger', 'info', 'light', 'dark'],
        headerBgVariant: 'dark',
        headerTextVariant: 'light',
        bodyBgVariant: 'light',
        bodyTextVariant: 'dark',
        footerBgVariant: 'warning',
        footerTextVariant: 'dark'
      }
    }
  }
</script>

<style src="./Card.scss" lang="scss">