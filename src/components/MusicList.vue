<template>
    <Collapse simple v-if="list.length">
        <Panel  v-for="item in list" :key="item.name" :name="item.name">
            {{item.name}}
            <List slot="content">
                <ListItem v-for="innerItem in item.content" :key="innerItem.song_id">
                    <ListItemMeta :avatar="innerItem.pic_small" :title="innerItem.title"
                                  :description="innerItem.author"/>
                </ListItem>
            </List>
        </Panel>
    </Collapse>
</template>


<script>
    export default {
        name: 'MusicList',
        props: {
            list: Array
        },

    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
