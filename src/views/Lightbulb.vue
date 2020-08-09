<template>
    <div>
        <h2>
            这里是个请求的示例
        </h2>
        <MusicList :list="musicList"></MusicList>
    </div>
</template>
<script>
    import MusicList from "../components/MusicList";
    import axios from "axios";

    export default {
        data: () => (
            {
                musicList: [],
            }
        ),
        components: {
            MusicList
        },
        created() {
            axios.get('https://api.apiopen.top/musicRankings').then((data) => {
                if (data.data.result) {
                    this.musicList = data.data.result
                }
            })
        }
    }
</script>
