<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>kawasaki</title>

    <style>

        /* ------------------------------
           BODY
        ------------------------------ */
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #eeeeee;
        }

        /* Main container */
        .container {
            width: 90%;
            margin: 20px auto;

            /* Rounded corners */
            border-radius: 15px;

            /* Shadow */
            box-shadow: 0 0 15px #555;

            /* Border image */
            border: 10px solid transparent;
            border-image: url("images/border.png") 30 round;

            overflow: hidden;
        }


        /* ------------------------------
           HEADER
        ------------------------------ */
        header {
            height: 160px;

            /* Multiple backgrounds */
            background-image:
                url("images/flower.png"),
                linear-gradient(to bottom, #2670c5, #4c91d9);

            background-position:
                left 20px,
                center;

            background-repeat:
                no-repeat,
                no-repeat;

            background-size:
                100px 100px,
                cover;

            position: relative;
        }

        header h1 {
            color: white;
            text-align: center;
            padding-top: 50px;
            margin: 0;

            text-shadow: 3px 3px 5px #222;
        }


        /* ------------------------------
           NAVIGATION
        ------------------------------ */
        nav {
            display: flex;
            justify-content: space-around;

            background: linear-gradient(
                to right,
                #ff0000,
                #ff9999,
                #cccccc
            );
        }

        nav a {
            width: 25%;
            padding: 12px;
            text-align: center;
            text-decoration: none;
            color: black;
            font-weight: bold;

            transition: 0.3s;
        }

        /* Hover pseudo-class */
        nav a:hover {
            background-color: #ff0000;
            color: white;
            box-shadow: inset 0 0 10px #333;
        }


        /* ------------------------------
           ITEMS SECTION
        ------------------------------ */
        .items-section {
            background:
                linear-gradient(
                    rgba(255, 180, 200, 0.9),
                    rgba(255, 200, 210, 0.9)
                );

            padding: 15px;
            text-align: center;
        }

        .items {
            width: 300px;
            margin: auto;

            /* Rounded corners */
            border-radius: 15px;

            overflow: hidden;

            /* Shadow */
            box-shadow: 0 5px 15px #555;
        }

        .items h3 {
            margin: 0;
            padding: 8px;

            background: linear-gradient(
                to right,
                #802d00,
                #cc8500
            );

            color: white;
        }

        /* Table */
        table {
            width: 100%;
            border-collapse: collapse;
        }

        td {
            padding: 8px;
            font-weight: bold;
        }

        /* Odd rows */
        tr:nth-child(odd) {
            background-color: #ffdd00;
        }

        /* Even rows */
        tr:nth-child(even) {
            background-color: #999400;
            color: white;
        }

        /* Mouse over rows */
        tr:hover {
            background-color: #ffff00;
            color: black;
        }

        /* Image opacity */
        .itemImg img {
            width: 40px;
            height: 40px;
            opacity: 0.3;

            transition: 0.5s;

            /* Rounded corners */
            border-radius: 10px;
        }

        /*
           Adjacent sibling selector:
           When itemName is hovered,
           the next itemImg becomes visible.
        */
        .itemName:hover + .itemImg img {
            opacity: 1;
            transform: scale(1.2);
        }


        /* ------------------------------
           LOGIN AREA
        ------------------------------ */
        .login-area {
            min-height: 400px;

            /* Multiple backgrounds */
            background-image:
                linear-gradient(
                    rgba(0, 0, 0, 0.55),
                    rgba(0, 0, 0, 0.55)
                ),
                url("images/background.jpg");

            background-size:
                cover,
                cover;

            background-position:
                center,
                center;

            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;

            padding: 30px;
        }


        /* ------------------------------
           LOGIN / SIGNUP BOX
        ------------------------------ */
        .box {
            width: 230px;
            padding: 20px;

            background-color: white;

            /* Rounded corners */
            border-radius: 15px;

            /* Shadow */
            box-shadow: 0 5px 20px #222;
        }

        .box h2 {
            text-align: center;
            margin-top: 0;
            color: #222;

            text-shadow: 1px 1px 2px #aaa;
        }

        .box label {
            font-size: 13px;
            font-weight: bold;
        }


        /* ------------------------------
           INPUT ELEMENTS
        ------------------------------ */
        input {
            width: 100%;
            box-sizing: border-box;

            padding: 10px;
            margin: 5px 0 12px;

            border: 2px solid #ccc;
            border-radius: 5px;

            background-color: #eeeeee;

            outline: none;
        }

        /* :focus pseudo-class */
        input:focus {
            border: 3px solid red;
            background-color: #ffffcc;
        }

        /* :required pseudo-class */
        input:required {
            border-left: 4px solid blue;
        }

        /* Valid email */
        input[type="email"]:valid {
            color: blue;
            border-color: green;
        }

        /* Invalid email */
        input[type="email"]:invalid {
            color: red;
        }


        /* ------------------------------
           BUTTON
        ------------------------------ */
        button {
            width: 100%;
            padding: 10px;

            border: none;
            border-radius: 5px;

            background: linear-gradient(
                to bottom,
                #1685ff,
                #0066cc
            );

            color: white;
            cursor: pointer;

            box-shadow: 0 3px 5px #777;

            transition: 0.3s;
        }

        button:hover {
            background: linear-gradient(
                to bottom,
                #0055aa,
                #003366
            );

            transform: scale(1.03);
        }


        /* ------------------------------
           FOOTER
        ------------------------------ */
        footer {
            background: linear-gradient(
                to right,
                #ffe0b2,
                #fff0d0
            );

            padding: 20px;

            font-style: italic;
            font-weight: bold;

            text-shadow: 1px 1px 2px #aaa;
        }


        /* ------------------------------
           RESPONSIVE DESIGN
        ------------------------------ */
        @media screen and (max-width: 700px) {

            .container {
                width: 95%;
            }

            .login-area {
                flex-direction: column;
            }

            nav {
                flex-direction: column;
            }

            nav a {
                width: auto;
            }
        }

    </style>
</head>

<body>

    <div class="container">

        <!-- HEADER -->
        <header>
            <h1>kawasaki</h1>
        </header>


        <!-- NAVIGATION -->
        <nav>
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Menu</a>
            <a href="#">Offers</a>
        </nav>

<!-- VEHICLE SECTION -->
<section class="items-section">

    <div class="items">

        <h3>Vehicle Names</h3>

        <table>

            <tr>
                <td class="itemName">Kawasaki Z900</td>
                <td class="itemImg">
                    <img src="c:\Users\jasfe\Downloads\images.webp" alt="Vehicle 1">
                </td>
            </tr>

            <tr>
                <td class="itemName">kawasaki zx10r</td>
                <td class="itemImg">
                    <img src="c:\Users\jasfe\Downloads\kawasaki-ninja-zx10r-1-min-scaled-1-1024x800.jpg" alt="Vehicle 2">
                </td>
            </tr>

            <tr>
                <td class="itemName">kawasaki ninja h2r</td>
                <td class="itemImg">
                    <img src="c:\Users\jasfe\Downloads\71c7-154VDL.jpg" alt="Vehicle 3">
                </td>
            </tr>

            <tr>
                <td class="itemName">kawasaki ninja 300</td>
                <td class="itemImg">
                    <img src="c:\Users\jasfe\Downloads\Kawasaki-Ninja-300-2-Copy-1-907x680.jpg" alt="Vehicle 4">
                </td>
            </tr>
        </table>

    </div>

</section>

        <!-- SIGN IN / SIGN UP -->
        <section class="login-area">

            <!-- SIGN IN -->
            <div class="box">

                <h2>Sign In</h2>

                <form>

                    <label>Username</label>

                    <input
                        type="text"
                        placeholder="Enter Username / Email / Phone Number"
                        required
                    >

                    <label>Password</label>

                    <input
                        type="password"
                        placeholder="Enter Password"
                        required
                    >

                    <button type="submit">
                        Sign In
                    </button>

                </form>

            </div>


            <!-- SIGN UP -->
            <div class="box">

                <h2>Sign Up</h2>

                <form>

                    <label>Name</label>

                    <input
                        type="text"
                        placeholder="Enter Name"
                        required
                    >

                    <label>Email</label>

                    <input
                        type="email"
                        placeholder="Enter Email"
                        required
                    >

                    <label>Password</label>

                    <input
                        type="password"
                        placeholder="Enter Password"
                        required
                    >

                    <button type="submit">
                        Sign Up
                    </button>

                </form>

            </div>

        </section>


        <!-- FOOTER -->
        <footer>

            Your Address<br>

            Kawasaki - Coimbatore — CKS Towers, 1/433 Avinashi Road, Chinniyampalayam, Coimbatore – 641048. Phone: 83000 97273.
        </footer>

    </div>

</body>
</html><img width="1917" height="1077" alt="image" src="https://github.com/user-attachments/assets/86081005-b1c4-4817-bd42-1d06480e46bf" />
