<template>
  <!-- header -->
  <div>
    <div class="flex bg-white">
      <div class="flex-none bg-blue">
        <div class="text-gray-700 text-3xl font-bold text-center py-6 px-16">
          会社名
        </div>
      </div>
      <div class="flex-grow">
        <div class="flex">

          <div 
            v-for="(item,i) in upperHeaderLinks"
            :key="'uh-'+i"
            class="text-gray-700 font-bold p-2 text-center m-2 hover:text-red-700 cursor-pointer"
          >
            {{item.text}}
          </div>

          <input type="text" class="bg-blue-400">
        </div>
        <div class="flex justify-between bg-gray-400">
          <div class="flex bg-gray-700">
            <div class="triangle-left bg-white cursor-pointer">
            </div>
            <div 
              v-for="(item,i) in lowerLeftHeaderLinks"
              :key="'lh-'+i"
              class="text-white font-bold px-4 py-2 text-center hover:bg-red-700 cursor-pointer"
            >
              {{item.text}}
            </div>
            <div class="triangle-right cursor-pointer bg-gray-400">
            </div>
          </div>


          <div class="flex bg-gray-700">
            <div class="triangle-left  bg-gray-400 cursor-pointer">
            </div>
            <div 
              v-for="(item,i) in lowerRightHeaderLinks"
              :key="'lh-'+i"
              class=" text-white font-bold px-4 py-2 text-center hover:bg-red-700 cursor-pointer"
            >
              {{item.text}}
            </div>
          </div>
        </div>
        
      </div>
    </div>

    <!-- contents -->
    <Nuxt />
  </div>
</template>
<script>
export default {
  data(){
    return {
      upperHeaderLinks:[
        {
          text:"ゲーム",
        },
        {
          text:"マガジン＆ブックス",
        },
        {
          text:"ミュージック",
        },
        {
          text:"グッズ",
        }
      ],
      lowerLeftHeaderLinks:[
        {
          text:"ストア",
        },
        {
          text:"メンバーズ",
        },
        {
          text:"動画",
        }
      ],
      lowerRightHeaderLinks:[
        {
          text:"会社情報",
        },
        {
          text:"採用情報",
        }
      ]
    }
  }
}
</script>

<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}



</style>
<style scoped>

.triangle-left{
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 0 0 50px 50px;
  border-color: transparent transparent rgba(74, 85, 104,1) transparent;

}

.triangle-right{
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 50px 50px 0 0;
  border-color: rgba(74, 85, 104,1) transparent transparent transparent;
}
</style>