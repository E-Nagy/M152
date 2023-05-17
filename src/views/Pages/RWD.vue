<template>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <ul class="people">
    <li v-for="index in 10" :key="index" class="person">
      <img
        class="person__image"
        src="https://source.unsplash.com/300x300/?portrait"
      />
      <div class="person__inner">
        <div class="person__title">Andi Moser</div>
        <div class="person__text">Web Entwickler</div>
        <button class="person__button">Kontaktieren</button>
      </div>
    </li>
  </ul>
</template>
<style lang="scss">
.people {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 10px;
  list-style-type: none;
  .person {
    &__image {
      border-radius: 50%;
      width: 100%;
    }
    &__inner {
      text-align: center;
    }
    &__title {
      font-size: 2rem;
      font-weight: bold;
    }
    &__button {
      background-color: rgb(85, 145, 87);
      border-radius: 5px;
      color: white;
      padding: 10px;
      border: none;
      margin: 30px 0 0;
    }
    margin-bottom: 40px;
  }
  @media only screen and (max-width: 768px) {
    display: grid;
    grid-template-columns: 1fr 1fr;
    .person{
        display: grid;
        grid-template-columns: 1fr 1fr;
        &__image{
            width: 50%;
        }
        &__inner{
            width: 50%;
        }
        &__title {
            font-size: 1rem;
            font-weight: bold;
        }
        &__button {
            border-radius: 5px;
            color: white;
            padding: 3px;
            border: none;
            margin: 1px 0 0;
        }
    }
  }
   @media only screen and (max-width: 426px) {
    display: grid;
    grid-template-columns: 1fr;
    list-style-type: none;

    .person{
        display: grid;
        grid-template-columns: 1fr;
        &__image {
            border-radius: 50%;
            width: 100%;
        }
        &__inner {
            text-align: center;
            width: 100%;
        }
        &__title {
            font-size: 1rem;
            font-weight: bold;
        }
        &__button {
            border-radius: 5px;
            color: white;
            padding: 3px;
            border: none;
            margin: 1px 0 0;
        }
    }
  }
}
</style>