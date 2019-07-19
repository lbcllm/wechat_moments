<template>
    <div class="discover">
        <header title="发现">
            <div class="content">
                <cell :src="cellData.src" :title="cellData.title" :ref="cellData.path"/>
            </div>
        </header>
    </div>
</template>
<script>
import header from '../components/header';
import cell from '../components/cell';
export default {
    name: 'discover',
    data() {
        return {
            cellData: {
                src: 'pyq.jpg',
                title: '朋友圈',
                path: '/moments'
            }
        };
    },
    components: {
        header,
        cell
    }
}
</script>

<style lang="scss" scoped>
.discover {
    width: 100%;
    height: calc(100% - 55px);
    position: relative;
    box-sizing: border-box;
    .content {
        width: 100%;
        height: calc(100% - 50px);
        margin-top: 50px;
    }
}
</style>


