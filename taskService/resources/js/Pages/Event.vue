<template>
    <Head title="Welcome" />

    <div class="w-1/2 relative flex flex-wrap mx-auto py-4">
        <h1 class="w-full text-center text-2xl font-bold px-4">Thông tin sự kiện</h1>
        <table class="w-full">
            <tr class="w-full py-2">
                <td class="w-1/2 pr-2">
                    <label class="text-xl font-bold">Tên sự kiện</label>
                    <div class="font-bold text-red-500">{{event.name}}</div>
                </td>
                <td class="w-1/2 pl-2">
                    <label class="text-xl font-bold">Mô tả sự kiện</label>
                    <div class="font-bold text-red-500">{{event.description}}</div>
                </td>
            </tr>
            <tr class="w-full py-2">
                <td class="w-1/2 pr-2">
                    <label class="text-xl font-bold">Thời gian bắt đầu sự kiện</label>
                    <div class="font-bold text-red-500">{{event.start_time}}</div>
                </td>
                <td class="w-1/2 pl-2">
                    <label class="text-xl font-bold">Thời gian kết thúc sự kiện</label>
                    <div class="font-bold text-red-500">{{event.end_time}}</div>
                </td>
            </tr>
            <tr class="w-full py-2">
                <td class="w-1/2 pr-2">
                    <label class="text-xl font-bold">Created_at</label>
                    <div class="font-bold text-red-500">{{event.created_at}}</div>
                </td>
                <td class="w-1/2 pl-2">
                    <label class="text-xl font-bold">Updated_at</label>
                    <div class="font-bold text-red-500">{{event.updated_at}}</div>
                </td>
            </tr>
        </table>
        <div class='w-full'>
            <award :awards="event.award"></award>
        </div>
        <div class="flex justify-end w-full">
            <JetButton class="bg-blue-700">Next</JetButton>
        </div>
    </div>
</template>
<script>
    import JetButton from '@/Jetstream/Button.vue'
    import JetInput from '@/Jetstream/Input.vue'
    import JetLabel from '@/Jetstream/Label.vue'
    import axios from 'axios'
    import Award from '@/Pages/Award.vue'
    export default ({
        components: {
            JetButton,
            JetInput,
            JetLabel,
            Award,
        },
        data() {
            return {
            }
        },
        methods: {
        },
        props:  {
            event: Object,
            }
    })
</script>