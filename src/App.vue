<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <button @click="selectedComponent = 'app-quote'">Quote</button>
                <button @click="selectedComponent = 'app-author'">Author</button>
                <button @click="selectedComponent = 'app-new'">New</button>
                <hr>
                <p>{{ selectedComponent }}</p>
                <keep-alive>
                    <component :is="selectedComponent">Default Content</component>
                </keep-alive>
               <!-- <app-quote>
                   <h2 slot="title">{{ title }}</h2>
                   <p>{{ myQuote }}</p>
               </app-quote> -->
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';
    import Author from './components/Author.vue';
    import New from './components/New.vue';

    export default {
        data: function() {
            return {
                title: 'The Quote',
                myQuote: 'A Wonderful Quote!',
                selectedComponent: 'app-quote'
            }
        },
        components: {
            'app-quote': Quote,
            'app-author': Author,
            'app-new': New
        }
    }
</script>

<style>
</style>
