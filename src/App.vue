<template>
    <div id="app">
        <FlightList :flights="flights"/>
    </div>
</template>

<script>
    import FlightList from './components/FlightList.vue'

    export default {
        name: 'App',
        components: {
            FlightList
        },
        data: function () {
            return {
                flights: [
                    {
                        from: "Tartu",
                        to: "Tallinn",
                        price: 50,
                        departure: "2021-01-30 15:15:00",
                        arrival: "2021-01-30 16:15:00",
                    },
                    {
                        from: "Helsinki",
                        to: "Tartu",
                        price: 125,
                        departure: "2021-01-29 09:30:00",
                        arrival: "2021-01-29 10:15:00",
                    },
                    {
                        from: "Tallinn",
                        to: "Sydney",
                        price: 950,
                        departure: "2021-01-31 12:00:00",
                        arrival: "2021-02-01 03:15:00",
                    },
                ]
            }
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
