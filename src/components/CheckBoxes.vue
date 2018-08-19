<template>
    <div>
        <input type="checkbox" checked v-on:click="toggleConsist('digits')">
        <span>Digits</span>
        <input type="checkbox" checked v-on:click="toggleConsist('upr')">
        <span>Upper Case</span>
        <input type="checkbox" checked v-on:click="toggleConsist('symbols')">
        <span>Symbols</span>
        <input type="checkbox" checked v-on:click="toggleConsist('lower')">
        <span>Lower</span>
    </div>
</template>

<script>
    export default {
        props: ['status'],
        methods: {
            toggleConsist(check) {
                switch (check) {
                    case 'digits': 
                        this.status.digitsInclude = !this.status.digitsInclude;
                        break;
                    case 'upr': 
                        this.status.uprInclude = !this.status.uprInclude;
                        break;
                    case 'symbols': 
                        this.status.symbolsInclude = !this.status.symbolsInclude;
                        break;
                    case 'lower': 
                        this.status.lwrInclude = !this.status.lwrInclude;
                        break;
                    }
            }
        }
    }
</script>