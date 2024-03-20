<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Netflix</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="icon" href="netflix.png">
    <style>
        body
        {
            margin: 0;
            padding: 0;
            background-color: #000;
            color: #fff;

        }
        .header
        {
            width: 100%;
            height: 100vh;
            background-image: url(images/header-image.png);
            background-size: cover;
            background-position: center;
            position: relative;
            opacity: 20px;
            backdrop-filter: blur(20px);
            padding: 10px 20px;
            background-image: linear-gradient(rgba(0 0 0 0.7) rgba(0 0 0 0.7) url(images/header-image.png)) ;
           
        }
        nav
        {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 20px;
        }
        .logo
        {
            width: 150px;
            padding: 10px;
            cursor: pointer;
        }
        nav button
        {
            border: 0;
            background-color: red;
            color: white;
            outline: 0;
            padding: 10px;
            border-radius: 4px;
            cursor: pointer;
            margin-left: 10px;
        }
        .lang.btn
        {
            display: inline-flex;
            align-items: center;
            background: transparent;
            border: 1px solid #fff;
            padding: 7px 10px;
        }
        .header-content
        {
            
             position: absolute;
             top: 50%;
             left: 50%;
             transform: translate(-50%, -50%);
             text-align: center;
             margin-top: 100px;


        }
        .header-content h1
        {
            font-weight: 600;
            font-size: 60px;
            font-family: Arial, Helvetica, sans-serif;
            

        }
        .header-content h3
        {
            font-weight: 600;
            margin-bottom: 10px;
        }
        .email-signup
        {
            display: flex;
            align-items: center;
            border-radius: 4px;
            background-color: #fff;
            overflow: hidden;
            margin-top: 30px;
        }
        .email-signup input{
            flex: 1;
            border: 0;
            outline: 0;
            margin-left: 20px;
            border-color: #fff;
            color: black;
            opacity: blur(10px);
            padding-right: 10px;
        }
        .email-signup button
        {
            border: 0;
            outline: 0;
            background-color: red;
            cursor: pointer;
            padding: 20px;
            color: white ;  
            font-size: 20px;
        }
        .email-signup button span
        {
            font-size: 20px;
        }
        .features h3
        {
            font-family: Arial, Helvetica, sans-serif;
            font-size: 30px;
            padding: 20px;
            margin-left: 20px;

        }
        .features-h1
        {
            display: flex;
            justify-content: space-between;
            align-items: column;
            border-color: #fff;
            background: linear-gradient(black, rgb(7, 7, 70));  
            border-radius: 10px;
            border-width: 5px; 
            text-align: center;
            padding: 10px; 
            margin-right:10px ;
            height: 300px;
            font-family: Arial, Helvetica, sans-serif;
            font-size: 40px;
    
        }
        .faq
        {
            margin: 100px auto;
            width: 600px;
            font-family: Arial, Helvetica, sans-serif;

        }
        .faq li
        {
            list-style-type: none;
            width: 100%;
            margin-bottom: 10px;
            padding: 10px;
            border-radius: 5px;
            background-color: rgb(58, 53, 53);
        }
        .faq li label
        {  
            padding: 10px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            font-size: 20px;
            font-weight: 500;
            
        }
        .faq-h1
        {
            padding: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-top: 40px;
        }
        .faq li label span
        {
            transform: rotate(90deg);
            font-size: 22px;
        }
        .faq input [type="radio"]
        {
            display: none;
        }
        .faq-cont
        {
            padding: 0 10px;
            line-height: 26px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s;
        }
        .faq   + input [type="radio"]:checked+.faq-cont
        {max-height: 400px;}
        
        label::before
        {
            content: '+';
            margin-right: 10px;
            font-size: 24px;
            font-weight: 600;
        }
        footer h3
        {
            display: flex;
            margin: 60px;
            padding: 5px;
            font-family: Arial, Helvetica, sans-serif;
            justify-content: space-evenly;
        }
        footer email-signup
        {
            flex: 1;
            border: 0;
            outline: 0;
            margin-left: 20px;
            border-color: #fff;
            color: white;
            opacity: blur(10px);
            padding-right: 10px;
        } 
        footer .btn 
        {
            border: 0;
            outline: 0;
            background-color: red;
            cursor: pointer;
            padding: 20px;
            color: white ;  
            font-size: 20px;

        }
        .email
        {
            
            
            margin-left: 20px;
            border-color: #fff;
            color: white;
            opacity: blur(10px);
            
            display: flex;
            align-items: center;
            border-radius: 4px;
            background-color: #fff;
            overflow: hidden;
            margin-top: 30px;

        }
        
        .footer-mail
        {
            flex: 1;
            border: 0;
            outline: 0;
            margin-left: 20px;
            border-color: #fff;
            color: black;
            opacity: blur(10px);
            padding-right: 10px;
            padding: 10px;
            align-items: center;
            margin-left: 40px;
        }
        .ul
        {
            list-style-type: none;
            padding:10px ;
            row-gap: 70px;
            margin-left: 20px;
            align-items: center;
            justify-content: center;

        }
       





    </style>
</head>
<body>
    
    <div class="header">
        <nav>
            <img src="images/logo.png" class="logo">
            <div>
                <button class="lang-btn">English <img src="images/down-icon.png" ></button>
                <button class="signup-btn">Sign Up</button>
            </div>
        </nav>
        <div class="header-content">
            <h1 class="h1">Unlimited movies, TV shows and more</h1>
            <h3>Starts at ₹149. Cancel anytime.</h3>
            <p>Ready to watch? Enter your email to create or restart your membership.</p>
            <form class="email-signup">
                <input type="email" placeholder="E-mail" required>
                <button type="submit">Get Started <span>&#x3e;</span></button>
            </form>
        </div>
    </div>
    <div>
        <div class="features">
            <h3>More reasons to join</h3>
            <ul class="features-h1">
                <h1 class="features-h1">Stories tailored to your taste</h1>
                <h1 class="features-h1">Cancel or switch plans anytime</h1>
                <h1 class="features-h1">A place just for kids</h1>
                <h1 class="features-h1">For your phone, tablet, laptop and TV</h1>
           </ul>

        </div>
    </div>
    <h1 class="faq-h1">Frequently Asked Question</h1>
    <ul class="faq">
        <li>
            <label for="first">What is Netflix? <span>&#x3e;</span></label>
            <input type="radio" id="first" checked >
            <div class="faq-cont"><p>Netflix is a streaming service that offers a wide variety of award-winning TV shows, movies, anime, documentaries and more – on thousands of internet-connected devices.

                You can watch as much as you want, whenever you want, without a single ad – all for one low monthly price. There's always something new to discover, and new TV shows and movies are added every week!</p></div>
        </li>
        <li>
            <label for="second">How much does Netflix costs? <span>&#x3e;</span></label>
            <input type="radio" id="second" >
            <div class="faq-cont"><p>Watch Netflix on your smartphone, tablet, Smart TV, laptop, or streaming device, all for one fixed monthly fee. Plans range from ₹649 to ₹149 a month. No extra costs, no contracts.</p></div>
        
        </li>
        <li>
            <label for="third">Where I can watch? <span>&#x3e;</span></label>
            <input type="radio" id="third" >
            <div class="faq-cont"><p>Watch anywhere, anytime. Sign in with your Netflix account to watch instantly on the web at netflix.com from your personal computer or on any internet-connected device that offers the Netflix app, including smart TVs, smartphones, tablets, streaming media players and game consoles.

                You can also download your favourite shows with the iOS, Android, or Windows 10 app. Use downloads to watch while you're on the go and without an internet connection. Take Netflix with you anywhere.</p></div>
        </li>
        <li>
            <label for="forth">How do I cancel? <span>&#x3e;</span></label>
            <input type="radio" id="forth" >
            <div class="faq-cont"><p>Netflix is flexible. There are no annoying contracts and no commitments. You can easily cancel your account online in two clicks. There are no cancellation fees – start or stop your account anytime.</p></div>

        </li>
        <li>
            <label for="fifth">Is Netflix good for kids? <span>&#x3e;</span></label>
            <input type="radio" id="fifth" >
            <div class="faq-cont"><p>The Netflix Kids experience is included in your membership to give parents control while kids enjoy family-friendly TV shows and films in their own space.

                Kids profiles come with PIN-protected parental controls that let you restrict the maturity rating of content kids can watch and block specific titles you don’t want kids to see.</p></div>
        </li>
    </ul>
    <footer>
        <h3>Ready to watch? Enter your email to create or restart your membership.</h3>
        <div> 
            
            <form class="email">
                <input type="email" class="footer-mail" id="email" placeholder="Email Address">
                <button class="sign-up btn"> Get Started</button>
            </form>
        </div>
        <nav>
            <ul class="ul">
                <li>FAQ</li>
                <li>Investor Relations</li>
                <li>Privacy</li>
                <li>Speed Test</li>
            </ul>
            
            
            
        </nav>
    </footer>
</body>
</html>
