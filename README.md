<!DOCTYPE html>
<html>
<head>
    <title>Food Corner Restaurant</title>

    <style>

        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
        }

        body{
            font-family:Arial;
            background:#f5f5f5;
        }

        header{
            background:#8b4513;
            color:white;
            text-align:center;
            padding:20px;
        }

        nav{
            background:#333;
            padding:15px;
            text-align:center;
            position:sticky;
            top:0;
        }

        nav a{
            color:white;
            text-decoration:none;
            margin:15px;
            font-size:18px;
        }

        nav a:hover{
            color:orange;
        }

        /* Hero Section */

        .hero{
            height:400px;

            background-image:
            linear-gradient(rgba(0,0,0,0.5),
            rgba(0,0,0,0.5)),
            url("https://images.unsplash.com/photo-1504674900247-0877df9cc836");

            background-size:cover;
            background-position:center;

            display:flex;
            justify-content:center;
            align-items:center;

            text-align:center;
            color:white;
        }

        .hero-text h1{
            font-size:50px;
            margin-bottom:10px;
        }

        .hero-text p{
            font-size:20px;
            margin-bottom:20px;
        }

        .hero button{
            padding:12px 25px;
            border:none;
            background:orange;
            color:white;
            font-size:18px;
            border-radius:5px;
            cursor:pointer;
        }

        .hero button:hover{
            background:darkorange;
        }

        section{
            padding:30px;
        }

        .box{
            background:white;
            padding:20px;
            margin-top:25px;
            border-radius:10px;
            box-shadow:0px 0px 8px lightgray;
        }

        .menu-container{
            display:flex;
            flex-wrap:wrap;
            gap:20px;
            justify-content:center;
        }

        .card{
            width:220px;
            background:#fafafa;
            border-radius:10px;
            overflow:hidden;
            box-shadow:0px 0px 5px gray;
            text-align:center;
            padding-bottom:15px;
        }

        .card img{
            width:100%;
            height:160px;
        }

        .card h3{
            margin-top:10px;
        }

        .card p{
            margin:8px;
        }

        input, select{
            width:100%;
            padding:10px;
            margin-top:10px;
            margin-bottom:15px;
            border:1px solid gray;
            border-radius:5px;
        }

        button{
            background:#8b4513;
            color:white;
            border:none;
            padding:10px 20px;
            border-radius:5px;
            cursor:pointer;
        }

        button:hover{
            background:#a0522d;
        }

        .message{
            margin-top:15px;
            color:green;
            font-weight:bold;
        }

        footer{
            background:#333;
            color:white;
            text-align:center;
            padding:15px;
            margin-top:20px;
        }

    </style>
</head>

<body>

    <!-- Header -->

    <header id="home">
        <h1>🍴 Food Corner Restaurant</h1>
        <p>Fresh & Delicious Food Everyday 😋</p>
    </header>

    <!-- Navbar -->

    <nav>
        <a href="#home">Home</a>
        <a href="#menu">Menu</a>
        <a href="#order">Order Dish</a>
        <a href="#table">Book Table</a>
        <a href="#contact">Contact</a>
    </nav>

    <!-- Hero Section -->

    <section class="hero">

        <div class="hero-text">
            <h1>Enjoy Delicious Food 🍕</h1>
            <p>Fresh Taste • Fast Service • Best Quality</p>

            <button>Order Now</button>
        </div>

    </section>

    <!-- About -->

    <section>

        <div class="box">

            <h2>About Us</h2>
            <br>

            <p>
                Welcome to Food Corner Restaurant.
                We provide tasty food, fast service
                and comfortable dining experience.
            </p>

        </div>

    </section>

    <!-- Menu -->

    <section id="menu">

        <div class="box">

            <h2>Our Menu</h2>
            <br>

            <div class="menu-container">

                <!-- Pizza -->

                <div class="card">
                    <img src="https://images.unsplash.com/photo-1513104890138-7c749659a591">

                    <h3>🍕 Pizza</h3>

                    <p>Cheesy Pizza</p>

                    <p>₹150</p>
                </div>

                <!-- Burger -->

                <div class="card">
                    <img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd">

                    <h3>🍔 Burger</h3>

                    <p>Veg Burger</p>

                    <p>₹100</p>
                </div>

                <!-- Pasta -->

                <div class="card">
                    <img src="https://images.unsplash.com/photo-1621996346565-e3dbc646d9a9">

                    <h3>🍝 Pasta</h3>

                    <p>Italian Pasta</p>

                    <p>₹120</p>
                </div>

                <!-- Salad -->

                <div class="card">
                    <img src="https://images.unsplash.com/photo-1546793665-c74683f339c1">

                    <h3>🥗 Salad</h3>

                    <p>Fresh Salad</p>

                    <p>₹80</p>
                </div>

            </div>

        </div>

    </section>

    <!-- Order Dish -->

    <section id="order">

        <div class="box">

            <h2>Order Your Dish</h2>
            <br>

            <form onsubmit="dishOrder()">

                <label>Your Name</label>

                <input type="text" placeholder="Enter your name" required>

                <label>Select Dish</label>

                <select required>
                    <option>Pizza</option>
                    <option>Burger</option>
                    <option>Pasta</option>
                    <option>Salad</option>
                </select>

                <label>Quantity</label>

                <input type="number" placeholder="Enter quantity" required>

                <button type="submit">Order Now</button>

            </form>

            <p class="message" id="dishMessage"></p>

        </div>

    </section>

    <!-- Table Booking -->

    <section id="table">

        <div class="box">

            <h2>Book a Table</h2>

            <br>

            <form onsubmit="tableBook()">

                <label>Your Name</label>

                <input type="text" placeholder="Enter your name" required>

                <label>Mobile Number</label>

                <input type="tel" placeholder="Enter mobile number" required>

                <label>Number of People</label>

                <input type="number" placeholder="How many people" required>

                <label>Date & Time</label>

                <input type="datetime-local" required>

                <button type="submit">Book Table</button>

            </form>

            <p class="message" id="tableMessage"></p>

        </div>

    </section>

    <!-- Contact -->

    <section id="contact">

        <div class="box">

            <h2>Contact Us</h2>

            <br>

            <p>📍 Location: Lucknow</p>

            <p>📞 Phone: 9876543210</p>

            <p>📧 Email: foodcorner@gmail.com</p>

        </div>

    </section>

    <!-- Footer -->

    <footer>
        <p>© 2026 Food Corner Restaurant | All Rights Reserved</p>
    </footer>

    <!-- JavaScript -->

    <script>

        function dishOrder(){

            event.preventDefault();

            document.getElementById("dishMessage").innerHTML =
            "✅ Your Dish is Booked Successfully!";
        }

        function tableBook(){

            event.preventDefault();

            document.getElementById("tableMessage").innerHTML =
            "✅ Your Table is Booked Successfully!";
        }

    </script>

</body>
</html>
