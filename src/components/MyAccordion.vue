<template>
  <div class="main">
    <div class="accordion">
      <transition-group name="flip-list">
        <div v-for="item in items" :key="item">
          <ul @click="item.open = !item.open">{{item.title}}</ul>
          <li v-if="item.open">{{item.text}}</li>
        </div>
      </transition-group>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyAccordion',
  data() {
    return {
      items: {
        obj1: {
          title: 'text title 1',
          text: 'Lorem ipsum dolor sit amet.',
          open: false
        },
        obj2: {
          title: 'text title 2',
          text: 'Lorem ipsum dolor sit amet, consectetur.',
          open: false
        },
        obj3: {
          title: 'text title 3',
          text: 'Lorem ipsum dolor sit.',
          open: false
        },
      }
    }
  }
};
</script>

<style lang="scss">
body {
  background-color: #94d1d1;
  margin: 20px;
  padding: 0;

  .main {
    height: 100vh;
    position: relative;


    .accordion {
      max-width: 500px;
      width: 100%;
      margin: 0 auto;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      -webkit-transform: translate(-50%, -50%);

      ul {
        padding: 15px 25px;
        border: 1px solid #0da928;
        text-align: center;
        background-color: #ffffff;
        border-radius: 5px;
        font-size: 14px;
        font-weight: bold;
        cursor: pointer;
      }

      li {
        border-radius: 5px;
        border: 1px solid #c50202;
        padding: 15px;
        font-size: 13px;
        margin: 5px 0;
        background-color: #eaeaea;
        list-style: none;
      }
    }

    .flip-list-move {
      transition: transform 0.8s ease;
    }
  }
}

</style>
