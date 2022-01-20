<template>

    <!-- component -->
    <form action="memo/update" method="post">
        <input type="hidden" name="_token" v-bind:value="csrf">
    
    <div v-for="memo in memos" :key="memo.id">
        <div class="bg-indigo-200 min-h-screen md:px-20 pt-6">
            <div class=" bg-white rounded-md px-6 py-10 max-w-2xl mx-auto">
                <h1 class="text-center text-2xl font-bold text-gray-500 mb-10">memo</h1>
                <div class="space-y-4">
                    
                    <div>
                        <label for="title" class="text-lx">Title:
                        </label>
                        <input
                            type="text"
                            id="title"
                            :value="memo.title"
                            class="ml-2 outline-none py-1 px-2 text-md border-2 rounded-md"></div>
                        <div>
                            <label for="content" class="block mb-2 text-lg">content :</label>
                            <textarea
                                :value="memo.content"
                                id="content"
                                cols="30"
                                rows="10"
                                placeholder="whrite here.."
                                class="w-full p-4 text-gray-600 bg-indigo-50 outline-none rounded-md"></textarea>
                        </div>
                        <button
                            class=" px-6 py-2 mx-auto block rounded-md text-lg font-semibold text-indigo-100 bg-indigo-600  ">submit</button>
                    </div>
                </div>
            </div>
        </div>

</form>
</template>

<script>
    export default {
        components: {
        }, 
        props: ['memos', 
                'csrf',
                ]
   }


</script>
