<template lang="">
    <div>
        <h2>Fullname - {{firstName}} {{lastName}}</h2>
        <h2>Computed fullname - {{fullName}}</h2>
        <button @click="changeFullName()">Change fullname</button>

        <br/>

        <h2>Total - {{items.reduce((total, curr) => (total = total + curr.price), 0)}}</h2>
        <button @click="items.push({id:4,title:'Keyboard', price: 50})">Add item</button>
        <h2>Computed total - {{total}}</h2>
        <h2>method total - {{getTotal()}}</h2>
        <input type="text" v-model="country">
    </div>
    <div>
        <template v-for="item in items" :key="item.id">
            <h2 v-if="item.price > 100">{{item.title}} {{item.price}}</h2>
        </template>

        <br/>

        <h2 v-for="item in expensiveItems" :key="item.id">{{item.title}} {{item.price}}</h2>
    </div>
</template>
<script>
export default {
    data() {
            return {
                firstName: "Filip",
                lastName: "Zemla",
                items: [
                {
                    id: 1,
                    title: 'TV',
                    price: 100,
                },
                {
                    id: 2,
                    title: 'Phone',
                    price: 200,
                },
                {
                    id: 3,
                    title: 'Laptop',
                    price: 300,
                },
                ],
                country: ''
            }
    },
    methods: {
        // method sa vykonava pri akejkolvek zmene, napr pri pisani do inputu
        getTotal() {
            console.log("getTotal Method");
            return this.items.reduce((total, curr) => (total = total + curr.price), 0)
        },

        changeFullName() {
            this.fullName = 'Clark Kent';
        }
    },
    computed: {
        fullName: {
            get() {
                return `${this.firstName} ${this.lastName}`
            },
            set(value) {
                const names = value.split(' ');
                this.firstName = names[0];
                this.lastName = names[1];
            }
        },
        // computed sa vykonava iba ked je potrebne refreshnut component
        total() {
            console.log("getTotal computed");
            return this.items.reduce((total, curr) => (total = total + curr.price), 0)
        },

        expensiveItems() {
            return this.items.filter( item => item.price > 100);
        }
    }
}
</script>
<style lang="">
    
</style>