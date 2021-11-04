<script>
    import { metatags } from '@roxi/routify'
    
    metatags.title = 'Fluffy - Handelspartner'
    metatags.description = 'Description coming soon...'

    // Set the date we're counting down to
var countDownDate = new Date("Jan 5, 2022 15:37:25").getTime();

// Update the count down every 1 second
var x = setInterval(function() {

  // Get todays date and time
  var now = new Date().getTime();

  // Find the distance between now an the count down date
  var distance = countDownDate - now;

  // Time calculations for days, hours, minutes and seconds
  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

  // Display the result in an element with id="demo"
  document.getElementById("time").innerHTML = days + "d " + hours + "h "
  + minutes + "m " + seconds + "s ";

  // If the count down is finished, write some text
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("time").innerHTML = "EXPIRED";
  }
}, 1000); 
</script>

<style>

.bgimg {
  position: relative;
  bottom: 18rem;
  color: white;
  font-family: "Courier New", Courier, monospace;
  font-size: 25px;
}


.middle {
  position: absolute;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}

hr {
  margin: auto;
  width: 40%;
} 

.photo {
  height: auto;
  width: 100%;
  background-position: center;
  background-size: cover;
  position: relative;
}
</style>

<img src="public/img/baustelle.jpg" alt="Baustelle" class="photo"/>
<div class="bgimg">
    <div class="middle">
      <h1>COMING SOON</h1>
      <hr>
      <p id="time"></p>
    </div>
  </div> 