<template>
    <table>
        <tr>
            <td>From</td>
            <td>To</td>
            <td id="departure-label">Departure</td>
            <td>Arrival</td>
            <td>Price</td>
        </tr>
        <tr v-for="flight in flights" :key="flight.arrival">
          <td>{{flight.from}}</td>
          <td>{{flight.to}}</td>
          <td><span>{{filteredDate(flight.departure)}}</span></td>
          <td><span>{{filteredDate(flight.arrival)}}</span></td>
          <td>{{flight.price}}</td>
        </tr>
        <tr>
            <td colspan="3" style="text-align: right;">
                <span>Total: <span id="total">{{total(flights)}}</span> EUR</span>
            </td>
        </tr>
    </table>
</template>

<script>
    import moment from 'moment'
    export default {
        name: 'FlightList',
        props: {
            flights: Array
        },
        methods: {
          total: function (flights) {
            var total = [];
            flights.forEach(element => { total.push(element.price)});
            return total.reduce(function(total, sum){ return total + sum}, 0);
          },
          filteredDate: function(date){

            return moment(date).format('MMM DD, YYYY hh:mm A');
          }

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
