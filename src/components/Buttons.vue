<template>
    <div class="hello">
        <div class="card" style="width: 18rem;">
            <!--            <img src=".././assets/logo.png" class="card-img-top" alt="Vue logo">-->
            <div class="card-body">
                <h5 class="text-center">
                    <label>
                        <input type="number" v-model="message" @keyup.enter="saveMessage">
                    </label>
                </h5>
                <!--                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>-->
                <button
                        type="button"
                        class="btn btn-primary"
                        @click="myadd1"
                >ADD +1
                </button>
                <button
                        type="button"
                        class="btn btn-success"
                        @click="setOff1"
                >Set off 1
                </button>
                <button
                        type="button"
                        class="btn btn-secondary"
                        @click="myadd100"
                >ADD 100
                </button>

                <button
                        type="button"
                        class="btn btn-danger"
                        @click="setOff100"
                >Set off 100
                </button>
                <button
                        type="button"
                        class="btn btn-warning"
                        @click="reset"
                >RESET
                </button>
                <!--                <button type="button" class="btn btn-info">Info</button>-->
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        methods: {
            saveMessage: function () {
                console.log('saveMessage', this.message);
                this.$emit('input-msg', this.message);
                this.message = '';
            },
            myadd1: function () {

                console.log('myadd1', 1);
                this.$emit('add', 1)
            },
            myadd100: function () {
                console.log('myadd100', 100);
                this.$emit('add', 100)
            },
            reset: function () {
                console.log('reset');
                this.$emit('reset')
            },
            setOff1: function () {

                console.log('setOff', 1);
                this.$emit('set-off', 1)
            },
            setOff100: function () {

                console.log('setOff', 100);
                this.$emit('set-off', 100)
            }
        },
        data: function () {
            return {
                message: '',
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
    /*h3 {*/
    /*  margin: 40px 0 0;*/
    /*}*/
    /*ul {*/
    /*  list-style-type: none;*/
    /*  padding: 0;*/
    /*}*/
    /*li {*/
    /*  display: inline-block;*/
    /*  margin: 0 10px;*/
    /*}*/
    /*a {*/
    /*  color: #42b983;*/
    /*}*/
</style>

