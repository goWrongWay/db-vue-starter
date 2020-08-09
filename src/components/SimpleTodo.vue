<template>
    <div>
        <div style="display: flex;margin-bottom: 20px">
            <Input
                    type="text"
                    placeholder="What must be done?"
                    v-model="text"
            />
            <Button @click="addTodo" style="margin-left: 20px;"> Add Todo </Button>
        </div>
        <List  border size="small">
            <ListItem v-for="(todo, index) in todos"
                      :key="index" >{{ todo.text }}
            <Button @click="removeTodo(todo)">x</Button>
            </ListItem>
        </List>

    </div>
</template>

<script>
    import store from '../store';

    export default {
        data() {
            return {
                text: ''
            }
        },
        computed: { todos: () => store.state.todos },
        methods: {
            addTodo() {
                store.commit('addTodo', this.text)
                this.text = ''
            },
            removeTodo(id) {
                store.commit('removeTodo', id)
            }
        }
    }
</script>