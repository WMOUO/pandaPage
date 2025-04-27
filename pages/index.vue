<script setup>
    const list = ref([
        {
            id:'1',
            title: '標題一',
            route: 'list/test1',
            description: '第一格',
            img: '圖片一'
        },
        {
            id:'2',
            title: '標題二',
            route: 'list/test2',
            description: '第二格',
            img: '圖片二'
        },
        {
            id:'3',
            title: '標題三',
            route: 'list/test1',
            description: '第三格',
            img: '圖片三'
        }
    ])
</script>
<template>
    <div>
        <!-- 網頁首頁 -->
        <div class="h-screen w-screen flex items-center justify-center">
            <div>
                <p class="text-9xl font-bold bg-clip-text bg-gradient-to-r from-violet-600 to-sky-700 text-transparent p-6">
                    Welcome To
                </p>
                <p class="flex justify-center p-6 text-8xl font-bold bg-clip-text bg-gradient-to-r from-violet-600 to-sky-700 text-transparent">
                    Panda Page
                </p>
            </div>
        </div>
        <div class="flex flex-row flex-wrap items-centers">
            <div class="grid grid-cols-10 grid-rows-2 gap-3">
                <div v-for="item in list" :key="item.id" class="grid grid-cols-10 grid-rows-3">
                    <!-- 圖片 -->
                    <div class="cols-tart-1 rows-start-1 col-span-3 row-span-3">
                        {{ item.img }}
                    </div>
                    <!-- 標題 -->
                    <div class="col-start-4 row-start-1 row-span-1">
                        {{  item.title }}
                    </div>
                    <!-- 描述 -->
                    <div class="col-start-2 row-start-4 row-span-2 ">
                        {{  item.description }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>