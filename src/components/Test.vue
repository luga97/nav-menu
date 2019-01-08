<template>
    <div id="main">
      <nav class="menu" :class="active" @click.prevent>
        <a href="#" class="menu-item" :class="page" @click="makeActive(page)" v-for="page in pages">{{page}}</a>
      </nav>
      <p class="selection">You chose <b>{{active}}</b></p>
    </div>
</template>

<script>
export default {
  name: 'Test',
  data () {
    return {
      active: 'home',
      pages: [
        'home',
        'projects',
        'services',
        'contact'
      ]
    }
  },
  methods: {
    makeActive: function(item){
      this.active = item;
    }
  }
}
</script>

<style>
  *{
    margin:0;
    padding:0;
    
  }

  body{
    font:15px/1.3 'Open Sans', sans-serif;
    color: #5e5b64;
    text-align:center;
  }

  /*-------------------------
          The menu
  --------------------------*/

  .menu{
    margin:0 auto 45px;
    background-color:#5597b4;
    box-shadow:0 5px 10px #ccc;
    border-radius:5px;
    width: 100%;
    padding: 10px;
  }

  .menu-item{
    display:inline-block;
    padding: 10px 30px;
    margin: 0 10px;
    color: #fff;
    font-weight:bold;
    font-size:16px;
    text-decoration:none;
    line-height:1;
    text-transform: uppercase;
    background-color:transparent;
    transition: background-color 0.25s;
    border-radius: 10px;
  }

  .selection{
    font-size:22px;
    font-weight:bold;
    color:#7d9098;
  }

  .selection b{
    color:#ffffff;
    display:inline-block;
    padding:5px 10px;
    background-color:#c4d7e0;
    border-radius:2px;
    text-transform:uppercase;
    font-size:18px;
  }
</style>
