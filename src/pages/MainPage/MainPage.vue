<template>
    <div class="main-page">
      <h5 class="title">Главная страница</h5>
      <div class="main-page__items">
        <div class="main-page__item">
          <div class="main-page__item-title">
            Количество выставленных и оплаченных счетов
          </div>
          <div class="main-page__bottom">
            <div class="main-page__bottom-item">
              <div class="main-page__bottom-item-number">324</div>
              <div class="main-page__bottom-item-text">Выставленные</div>
            </div>
            <div class="main-page__bottom-item">
              <div class="main-page__bottom-item-number">302</div>
              <div class="main-page__bottom-item-text">Оплаченные</div>
            </div>
          </div>
        </div>
        <div class="main-page__item">
          <div class="main-page__item-title red">
            Количество запланированных и проведеннных обучений
          </div>
          <div class="main-page__bottom">
            <div class="main-page__bottom-item">
              <div class="main-page__bottom-item-number">37</div>
              <div class="main-page__bottom-item-text">
                Запланированные
              </div>
            </div>
            <div class="main-page__bottom-item">
              <div class="main-page__bottom-item-number">31</div>
              <div class="main-page__bottom-item-text">Проведеннные</div>
            </div>
          </div>
        </div>
        <div class="main-page__item">
          <div class="main-page__item-title">Просроченные обучения</div>
          <div class="main-page__bottom">
            <div class="main-page__bottom-item">
              <div class="main-page__bottom-item-number">4</div>
              <div class="main-page__bottom-item-text">Просроченных</div>
            </div>
          </div>
        </div>
      </div>

      <h5 class="title">
        Даты очных занятий и экзаменов в РТН
      </h5>
      <div class="dates">
        <button class="dates__btn"><img src="@/assets/left.png" alt="<"></button>
        <div class="dates__items">
          <b-calendar></b-calendar>
          <b-calendar></b-calendar>
          <b-calendar></b-calendar>
        </div>
        <button class="dates__btn"><img src="@/assets/right.png" alt="<"></button>
      </div>
    </div>
</template>

<style src="./MainPage.scss" lang="scss" />
