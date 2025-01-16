<template>

    <header>
        <div class="navigation-bar" id="navigation">
            <div class="navbar">
                <a href="/html/index.html"><img src="..\..\public\Images\Logo.jpg" ></a> <!-- Attēls ar grāmatas rakstīšanu -->
                <p>&nbsp&nbsp</p>
                <a class="pressed1" href="../html/index.html"><i style="font-size:16px" class="fa">&#xf02d;</i> Bibliotēka</a> <!-- Saite uz kontaktu lapu -->
                <a class="pressed1" href="../html/Contact.html"><i style="font-size:16px;" class="fa">&#xf02e;</i> Manas grāmatas</a> <!-- Saite uz lapu "Par mums" -->
                <a class="pressed1"><i style="font: size 16px" class="fa">&#xf040;</i> Rakstīšana</a> <!-- Aktīvā saite, kas parāda nolaižamā saraksta nosaukumu -->
    
            </div>  
            <div class="account"> <!-- Bloks konta pārvaldīšanai -->
                <a class="pressed2" href="#SigIn"><i style="font-size:16px" class="fa">&#xf2bd;</i> Reģistrācija</a> <!-- Saite uz reģistrācijas lapu -->
                <a class="pressed2" href="#LogIn"> <i style="font-size:16px" class="fa">&#xf2be;</i> Pieslēgties</a> <!-- Saite uz pierakstīšanās lapu -->
                <div class="search">
                    <input type="text" class="input" placeholder="Meklēt...">
                    <button class="btn">
                        <i style="font-size:14px" class="fa">&#xf002;</i>
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
        box-shadow: rgba(26, 16, 8, 0.8) 0px 0px 15px; /* Ēna navigācijas joslas apakšā */
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

    .pressed1{
        color: rgba(26, 16, 8, 0.8); /*Teksta krāsa */
        text-align: center; /* Centrējam tekstu */
        text-decoration: none; /* Noņemam noklusēto teksta apakšsvītrojumu */
        font-size: 17px; /* Fonta izmērs navigācijas tekstam */
        cursor: pointer;
        font-family: Tahoma, Helvetica, sans-serif;
        margin: 10px;
    }

    .activeother{
        .context-menu {cursor: context-menu;}
    }

    .pressed2{
        color: rgba(26, 16, 8, 0.8); /* Text color */
        text-align: center; /* Center text */
        text-decoration: none; /* Remove default text underline */
        display: inline-block; /* Inline block to properly display spacing */
        font-size: 17px; /* Font size for navigation text */
        font-family: Tahoma, Helvetica, sans-serif;
        position: relative;
        margin: 10px;

    }
    
    .pressed2:hover .fa{
        color: rgba(247, 186, 146, 0.8); /* Text color when hovered */

    }
    .pressed2:hover {
        color: rgba(247, 186, 146, 0.8); /* Text color when hovered */
    }
    .pressed1:hover .fa{
        color: rgba(247, 186, 146, 0.8); /* Text color when hovered */

    }
    .pressed1:hover{
        color: rgba(247, 186, 146, 0.8); /* Text color when hovered */
    }
    
/* Presentational Styles */

    
    @media (max-width: 500px) {
        .fa {
        display: none !important; /* Inore citus noteikumus */
        }
    }

    /* search bar */
    .search {
        position: relative;
        display: flex; /* Use flexbox to align items */
        align-items: center; /* Center items vertically */
    }

    .search:hover {
        transform: none;
    }

    .search .input {
        background-color: #ffffff;
        border: 0;
        border-radius: 20px;
        border-color: rgba(26, 16, 8, 0.8);
        font-size: 15px;
        padding: 10px;
        height: 10px; /* Adjusted height for better visibility */
        width: 0; /* Start with width 0 */
        overflow: hidden; /* Hide overflow */
        opacity: 0;
    }

    .search .btn {
        background-color: #c58667; /* Set background color */
        border: 2px solid rgba(26, 16, 8, 0.8); /* Remove border */
        border-radius: 20px;
        padding: 7px; /* Add padding */
        cursor: pointer; /* Change cursor to pointer */
        transition: transform 0.3s ease; /* Add transition for smooth transform */
        outline: none; /* Remove outline */
        margin-right: 10px; /* Add margin to the right */
        width: 33px; /* Set width */
        height: 33px;
    }

    .search.active .input {
        width: 150px; /* Expanded width */
        height: 5px;
        opacity: 1; 
        margin: 5px;
    }

    .input{
        color: rgba(26, 16, 8, 0.8);
        font-family: Tahoma, Helvetica, sans-serif;
    }
    
    .input:focus {
        outline: none; /* Убирает стандартную рамку браузера */
    }
    .btn:hover {
        border-color: rgba(247, 186, 146, 0.8); /* Change border color on hover */
    }
    .btn:hover .fa {
        color: rgba(247, 186, 146, 0.8);
    }
    .fa{
        color: rgba(26, 16, 8, 0.8);

    }
 
</style>
<script>
document.addEventListener('DOMContentLoaded', () => {
    const search = document.querySelector('.search');
    const btn = document.querySelector('.btn');
    const input = document.querySelector('.input');

    if (btn) {
        btn.addEventListener('click', () => {
            if (input.value.trim() === '') {
                search.classList.toggle('active');
            } else {
                input.focus();
            }
        });
    }
});
</script>