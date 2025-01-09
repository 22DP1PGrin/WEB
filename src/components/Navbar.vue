<template>

    <header>
        <div class="navigation-bar" id="navigation">
            <div class="navbar">
                <img src="..\..\public\Images\Logo.jpg" > <!-- Attēls ar grāmatas rakstīšanu -->
                <p>&nbsp&nbsp</p>
                <a class="active" href="../html/index.html"><i style="font-size:17px" class="fa">&#xf015;</i> Home</a> <!-- Saite uz kontaktu lapu -->
                <div class="dropdown"> <!-- Izveidojam nolaižamo sarakstu -->
                    <p class="active"><i style="font: size 14px" class="fa">&#xf013;</i> Service</p> <!-- Aktīvā saite, kas parāda nolaižamā saraksta nosaukumu -->
                    <div class="dropdown-content"> <!-- Nolaižamā satura konteiners -->
                        <a href="../html/abou_us.html">About us</a> <!-- Saite uz bibliotēkas piekļuvi -->
                        <a href="../html/Functionality.html">Functionality</a> <!-- Saite uz funkcionalitāti -->
                        <a href="../html/Rules.html">Rules</a> <!-- Saite uz saites noteikumi -->
                    </div>
                </div>
                
                <a class="active" href="../html/Contact.html"><i style="font-size:14px" class="fa">&#xf0e0;</i> Contact</a> <!-- Saite uz lapu "Par mums" -->
            </div>  
            <div class="account"> <!-- Bloks konta pārvaldīšanai -->
                <a class="active2" href="#SigIn"><i style="font-size:14px" class="fa">&#xf2bd;</i> Sign in</a> <!-- Saite uz reģistrācijas lapu -->
                <a class="active2" href="#LogIn"> <i style="font-size:14px" class="fa">&#xf2be;</i> Log in &nbsp &nbsp </a> <!-- Saite uz pierakstīšanās lapu -->
                <div class="search">
                    <input type="text" class="input" placeholder="Search...">
                    <button class="btn">
                        <i class="fa fa-search" aria-hidden="true"></i>
                    </button>
                </div>
            </div>    
        </div>
    </header>

</template>

<style scoped>

    /* Navigācijas josla */
    .navigation-bar{
        display: flex; /* Flexbox izkārtojums navigācijai */
        justify-content: space-between; /* Atstarpes starp navigācijas elementiem */
        align-items: center; /* Elementu vertikāla izlīdzināšana */
        background-color: #c58667; /* Fona krāsa ar gradientu */
        height: 55px; /* Augstums */
    }

    .navigation-bar > div {
        margin: 2px; /* Malas ap katru navigācijas elementu */
        padding: 2px; /* Atstarpe iekšpusē */
    }

    .navbar{
        display: flex; /* Flexbox izkārtojums */
        align-items: center; /* Elementu vertikāla izlīdzināšana */
        flex-grow: 1; /* Izplešas, lai aizpildītu vietu */
        transition: transform 0.3s ease; /* Pārejas efekts uz transformācijām */

    }

    .account{
        display: flex; /* Flexbox izkārtojums konta sadaļai */
        margin-left: auto; /* Novietojam konta bloku pa labi */
        text-align: center; /* Center text */
    }

    .dropdown-content {
        display: none; /* Paslēpt nolaižamo saturu pēc noklusējuma */
        position: absolute; /* Absolūta pozīcija, lai nolaižamais saturs tiktu parādīts virs citiem elementiem */
        background-color: #c58667; /* Fona krāsa nolaižamajam saturam */
        min-width: 120px; /* Minimālais platums nolaižamajam saturam */
    }

    .dropdown-content a {
        color: rgba(26, 16, 8, 0.8); /* Saite teksta krāsa */
        padding: 10px 10px; /* Iekšējās atstarpes ap saiti */
        text-decoration: none; /* Noņemam noklusēto apakšsvītrojumu */
        display: block; /* Iestatām saites kā bloku, lai aizpildītu visu platumu */
    }
    .dropdown-content a:hover {
        background-color: #f5b89a; /* Fona krāsa, kad pele ir virs saites */
    }

    .dropdown:hover .dropdown-content {
        display: block; /* Parādām nolaižamo saturu, kad pele ir virs nolaižamā saraksta */
    }

    .active{
        color: rgba(26, 16, 8, 0.8); /*Teksta krāsa */
        text-align: center; /* Centrējam tekstu */
        text-decoration: none; /* Noņemam noklusēto teksta apakšsvītrojumu */
        margin-left: 17px; /* Atstarpes starp saitēm */
        font-size: 17px; /* Fonta izmērs navigācijas tekstam */
        cursor: pointer;
    }

    .activeother{
        .context-menu {cursor: context-menu;}
    }

    .active2{
        color: rgba(26, 16, 8, 0.8); /* Text color */
        text-align: center; /* Center text */
        text-decoration: none; /* Remove default text underline */
        margin-left: 17px; /* Space between links */
        display: inline-block; /* Inline block to properly display spacing */
        font-size: 17px; /* Font size for navigation text */
        margin-top: 7px;
    }

    .active:hover {
        color: rgba(241, 189, 141, 0.8); /* Teksta krāsa, kad pele tiek pārvilkta */
        transform: scale(1.2); /* Saites mērogošana uz augšu, kad pele ir virs tām */
    }

    .active2:hover {
        color: rgba(241, 189, 141, 0.8); /* Teksta krāsa, kad pele tiek pārvilkta */
        transform: scale(1.2); /* Saites mērogošana uz augšu, kad pele ir virs tām */
    }
    
    @media (max-width: 500px) {
        .fa {
        display: none !important; /* Inore citus noteikumus */
        }
    }



/* Existing styles */
.search {
    position: relative;
    display: flex; /* Use flexbox to align items */
    align-items: center; /* Center items vertically */
}

.search .input {
    background-color: #FFFFFF;
    border: 0;
    font-size: 15px;
    padding: 10px;
    height: 10px; /* Adjusted height for better visibility */
    width: 0; /* Start with width 0 */
    overflow: hidden; /* Hide overflow */
    opacity: 0;
}

.search .btn {
    background-color: #ffffff; /* Set background color */
    border: none; /* Remove border */
    padding: 10px; /* Add padding */
    font-size: 10px; /* Set font size */
    cursor: pointer; /* Change cursor to pointer */
    transition: transform 0.3s ease; /* Add transition for smooth transform */
    outline: none; /* Remove outline */
}

.search.active .input {
    width: 150px; /* Expanded width */
    height: 5px;
    opacity: 1; 
}
</style>
<script>

document.addEventListener('DOMContentLoaded', () => {
    const search = document.querySelector('.search');
    const btn = document.querySelector('.btn');
    const input = document.querySelector('.input');

    if (btn) {
        btn.addEventListener('click', () => {
            search.classList.toggle('active');
            input.focus();
        });
    }
});
</script>