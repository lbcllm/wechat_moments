<template>
    <div class="mine">
        <header title="我"></header>
        <div class="container">
            <div class="cell-wrapper">
                <div class="cell-title" v-if="user">
                    <img :src="user.avatar" alt="">
                    <span>{{user.name}}</span>
                </div>
            </div>
            <div class="btn_wrapper">
                <button @click="logout">退出登录</button>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'me',
    computed: {
        
    },
    methods: {
      logout() {
          localStorage.removeItem('wxpyqtoken');
          this.$router.push('/login');
      }
    },
    components: {

    }
}
</script>

<style lang="scss" scoped>
.mine {
    width: 100%;
    height: 100%;
    overflow: hidden;
    .container {
        width: 100%;
        height: 100%;
        margin-top: 50px;
        .cell-wrapper {
            background-color: #fff;
            box-sizing: border-box;
            color: inherit;
            min-height: 88px;
            display: flex;
            font-style: 16px;
            line-height: 1;
            overflow: hidden;
            padding: 0 8px;
            width: 100%;
            line-height: 80px;
            border-top: 1px solid #d9d9d9;
            border-bottom: 1px solid #d9d9d9;
            .cell-title {
                flex: 1;
                img {
                    width: 4rem;
                    height: 4rem;
                    vertical-align: middle;
                    margin-right: 0.6rem;
                }
                span {
                    display: inline-block;
                    vertical-align: middle;
                }
            }
        }
    }
}
.btn_wrapper {
    box-sizing: border-box;
    padding: 20px;
}
</style>


