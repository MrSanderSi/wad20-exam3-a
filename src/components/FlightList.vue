<template>
    <table>
        <tr>
            <td>From</td>
            <td>To</td>
            <td id="departure-label">Departure</td>
            <td>Arrival</td>
            <td>Price</td>
        </tr>
        <tr>
            <td colspan="3" style="text-align: right;">
                <span>Total: <span id="total"></span> EUR</span>
            </td>
        </tr>
    </table>
</template>

<script>

    export default {
        name: 'FlightList',
        props: {
            flights: Array
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    table {
        width: 50%;
        margin: 0 auto;
    }
</style>