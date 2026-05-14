<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Local Travel App</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    background:#f4f7fb;
}

/* HEADER */

header{
    background:#0d6efd;
    color:white;
    padding:20px;
    text-align:center;
}

.hero{
    height:300px;
    background:url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e') center/cover;
    display:flex;
    justify-content:center;
    align-items:center;
    color:white;
    font-size:40px;
    font-weight:bold;
}

/* REGISTRATION */

.register-section{
    width:90%;
    max-width:500px;
    margin:40px auto;
    background:white;
    padding:30px;
    border-radius:12px;
    box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

.register-section h2{
    text-align:center;
    margin-bottom:20px;
    color:#0d6efd;
}

.register-section form{
    display:flex;
    flex-direction:column;
    gap:15px;
}

.register-section input,
.register-section select{
    padding:12px;
    border:1px solid #ccc;
    border-radius:8px;
}

.register-section button{
    padding:12px;
    background:#198754;
    color:white;
    border:none;
    border-radius:8px;
    cursor:pointer;
}

/* APP INFO */

.about-app{
    padding:50px 20px;
    text-align:center;
}

.features{
    display:flex;
    justify-content:center;
    flex-wrap:wrap;
    gap:20px;
    margin-top:30px;
}

.feature-box{
    background:white;
    width:300px;
    padding:25px;
    border-radius:12px;
    box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

/* RENT VEHICLE */

.vehicle-rent{
    padding:50px 20px;
    background:#f8f9fa;
    text-align:center;
}

.vehicle-card{
    width:320px;
    margin:auto;
    background:white;
    border-radius:15px;
    overflow:hidden;
    box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

.vehicle-card img{
    width:100%;
    height:220px;
    object-fit:cover;
}

.vehicle-card button{
    margin:20px;
    padding:12px 20px;
    border:none;
    background:#198754;
    color:white;
    border-radius:8px;
    cursor:pointer;
}

/* FARE CALCULATOR */

.fare-calculator{
    width:90%;
    max-width:500px;
    margin:50px auto;
    padding:30px;
    background:white;
    border-radius:12px;
    box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

.fare-calculator h2{
    text-align:center;
    margin-bottom:20px;
}

.fare-calculator input{
    width:100%;
    padding:12px;
    margin-bottom:15px;
    border:1px solid #ccc;
    border-radius:8px;
}

.fare-calculator button{
    width:100%;
    padding:12px;
    background:#0d6efd;
    color:white;
    border:none;
    border-radius:8px;
}

.result{
    margin-top:20px;
    line-height:2;
}

/* WALLET */

.wallet-section{
    padding:50px 20px;
    text-align:center;
    background:#f8f9fa;
}

.wallet-card{
    width:90%;
    max-width:400px;
    margin:auto;
    background:white;
    padding:25px;
    border-radius:15px;
    box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

.wallet-card input{
    width:100%;
    padding:12px;
    margin-top:10px;
    border:1px solid #ccc;
    border-radius:8px;
}

.wallet-card button{
    width:100%;
    padding:12px;
    margin-top:15px;
    background:#198754;
    color:white;
    border:none;
    border-radius:8px;
}

/* FOOTER */

footer{
    background:#111;
    color:white;
    text-align:center;
    padding:15px;
    margin-top:40px;
}

</style>
</head>

<body>

<header>
    <h1>Local Driver & Passenger App</h1>
    <p>Connect Local Drivers With Local Passengers</p>
</header>

<div class="hero">
    Book Local Rides Easily
</div>

<!-- REGISTRATION -->

<section class="register-section">

    <h2>Create Account</h2>

    <form id="registerForm">

        <input type="text" placeholder="Full Name" required>

        <input type="tel" placeholder="Mobile Number" required>

        <input type="password" placeholder="Password" required>

        <select required>

            <option value="">Select Account Type</option>

            <option>Service Provider</option>

            <option>Client</option>

        </select>

        <button type="submit">
            Register Now
        </button>

    </form>

</section>

<!-- ABOUT APP -->

<section class="about-app">

    <h2>About App</h2>

    <p>
        This app helps local drivers connect with local passengers
        for rides, tours, airport pickup, and vehicle rentals.
    </p>

    <div class="features">

        <div class="feature-box">
            <h3>For Drivers</h3>
            <p>Earn money from local ride bookings.</p>
        </div>

        <div class="feature-box">
            <h3>For Passengers</h3>
            <p>Find trusted nearby drivers quickly.</p>
        </div>

    </div>

</section>

<!-- VEHICLE RENT -->

<section class="vehicle-rent">

    <h2>Vehicle Rental</h2>

    <div class="vehicle-card">

        <img src="https://images.unsplash.com/photo-1549399542-7e3f8b79c341">

        <h3>Innova Crysta</h3>

        <p>Approx Running Cost ₹13/KM</p>

        <button>
            Rent Vehicle
        </button>

    </div>

</section>

<!-- FARE CALCULATOR -->

<section class="fare-calculator">

    <h2>Ride Fare Calculator</h2>

    <input type="number" id="distance" placeholder="Distance (KM)">

    <button onclick="calculateFare()">
        Calculate Fare
    </button>

    <div class="result">

        <p>
            Vehicle Cost: ₹
            <span id="vehicleCost">0</span>
        </p>

        <p>
            Driver Profit: ₹
            <span id="driverProfit">0</span>
        </p>

        <p>
            App Commission: ₹
            <span id="commission">0</span>
        </p>

        <p>
            Total Fare: ₹
            <span id="totalFare">0</span>
        </p>

    </div>

</section>

<!-- WALLET -->

<section class="wallet-section">

    <h2>Wallet Payment</h2>

    <div class="wallet-card">

        <h3>Wallet Balance</h3>

        <h1>
            ₹ <span id="walletBalance">5000</span>
        </h1>

        <input type="number" id="addMoney" placeholder="Add Money">

        <button onclick="addWalletMoney()">
            Add Money
        </button>

        <button onclick="payRideFare()">
            Pay Ride Fare
        </button>

    </div>

</section>

<footer>
    © 2026 Local Travel App
</footer>

<script>

/* REGISTRATION */

document.getElementById("registerForm")
.addEventListener("submit", function(e){

    e.preventDefault();

    alert("Registration Successful!");

});

/* FARE CALCULATOR */

let currentFare = 0;

function calculateFare(){

    let distance =
    parseFloat(document.getElementById("distance").value);

    let vehicleCost =
    distance * 13;

    let driverProfit =
    distance * 3;

    let commission =
    (vehicleCost + driverProfit) * 0.10;

    let totalFare =
    vehicleCost + driverProfit + commission;

    currentFare = totalFare;

    document.getElementById("vehicleCost").innerText =
    vehicleCost.toFixed(2);

    document.getElementById("driverProfit").innerText =
    driverProfit.toFixed(2);

    document.getElementById("commission").innerText =
    commission.toFixed(2);

    document.getElementById("totalFare").innerText =
    totalFare.toFixed(2);

}

/* WALLET SYSTEM */

let walletBalance = 5000;

function addWalletMoney(){

    let amount =
    parseFloat(document.getElementById("addMoney").value);

    if(amount > 0){

        walletBalance += amount;

        document.getElementById("walletBalance").innerText =
        walletBalance.toFixed(2);

        alert("Money Added Successfully!");

    }

}

function payRideFare(){

    if(currentFare <= 0){

        alert("Please Calculate Fare First!");

        return;

    }

    if(walletBalance >= currentFare){

        walletBalance -= currentFare;

        document.getElementById("walletBalance").innerText =
        walletBalance.toFixed(2);

        alert("Ride Payment Successful!");

    }else{

        alert("Insufficient Wallet Balance!");

    }

}

</script>

</body>
</html># -My-life-ride-