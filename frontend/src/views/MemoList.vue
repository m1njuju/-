<template>
    <div>
        <table>
            <tr>
                <td>번호</td>
                <td>제목</td>
            </tr>
            <tr v-for="(memo,i) in memo" :key="i">
                <td>{{memo.id}}</td>
                <td @click="$router.push(`/list/${memo.id}`)">{{memo.title}}</td>
            </tr>
        </table>
    </div>
</template>
<script>
export default {
    data () {
        return ({
            memo: []
        })
    },
    created() {
        // 서버로 접근해서 데이터를 가져올 함수
        // axios 비동기로 값을 가져옴: get
        this.$http.get('/api/memo') // /api는 서버의 있는 주소를 가져오겠다는 것
        .then((response)=>{
            //서버에서 어떤 값이 들어왔는지 알기 위해서는 log로 확인
            //console.log(response.data);
            this.memo = response.data;
        })
    }
}
</script>