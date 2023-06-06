<template>

    <!-- SOCIALS -->
    <div class="socials">
        <h3>Connect with us:</h3>
        <div class="social-icons">
            <img id="icon" src="@/assets/google-icon.png" height="30" width="30" >
            <img id="icon" src="@/assets/facebook-icon.png" height="30" width="30" >
            <img id="icon" src="@/assets//twitter-icon.png" height="30" width="30" >
            <img id="icon" src="@/assets/instagram-icon.png" height="30" width="30" >
        </div>
    </div>
        <!-- SOCIALS -->

        <!-- FOOTER -->
    <div class="wrap-wrap">
        <div class='footer-wrapper'>

            <!-- FIRST COLUMN -->
            <div class="col first">
                <h2>SHOE STORE</h2>
                <h3>Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
                    Aperiam odio ratione perferendis rerum doloremque blanditiis exercitationem! 
                    Optio molestiae eaque beatae? 
                    Eaque adipisci illo expedita ipsam.</h3>
            </div>
            <!-- FIRST COLUMN -->

            <!-- SECOND COLUMN -->
            <div class="col second">
                <h2>Company</h2>
                <p>Home</p>
                <p>About</p>
                <p>Service</p>
                <p>Shop</p>
            </div>
            <!-- SECOND COLUMN -->
            
            <!-- THIRD COLUMN -->
            <div class="col third">
                <h2>Products</h2>
                <p>Running Shoes</p>
                <p>Gym Shoes</p>
                <p>CROCCS</p>
            </div>
            <!-- THIRD COLUMN -->

            <!-- FOURTH COLUMN -->
            <div class="col fourth">
                <h2>Support</h2>
                <p>Product Help</p>
                <p>Service & Warranty</p>
                <p>(+225) 25 52 25 52</p>
            </div>
            <!-- FOURTH COLUMN -->


        </div>
        
        <div id="footer-separation"></div>

    <h3 class="copyrite">@SHOE STORE Copyright 2023. All rights reserved</h3>
</div>    
    <!-- FOOTER -->
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;900&display=swap');

#footer-separation {
    background-color: white;
    position: absolute;
    left: 10%;
    border: 1px solid gray;
    width: 75%;

}

.copyrite {
    padding: 2%;
    position: absolute;
    left: 40%;
}

.wrap-wrap {
    width: 100%;
    background-color: white;
}

.socials {
    background-color: #1F6AAD;
    color: white;
    font-family: 'Roboto';
    display: flex;
    justify-content: space-around;
    font-size: 22px;
    width: 100%;
}

.social-icons {
    padding-top: 1.5%;
    padding-left: 5px;
    filter: invert();
}

#icon {
    padding-left: 100px;
}

.footer-wrapper {
    font-family: 'Roboto';
    color: black;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

.col {
    display: flex;
    flex-direction: column;
}

.first {
    width: 25%;
}

.col > p {
    font-size: 1    8px;
}

</style>