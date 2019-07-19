<template>
   <header class="header">
       <div class="header-button is-left" v-show="isLeft">
           <i class="fa fa-chevron-left"></i>
           <button @click="$router.push('/moments')">返回</button>
       </div>
   </header>
</template>
