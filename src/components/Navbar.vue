<template>

    <header>
        <div class="navigation-bar" id="navigation">
            <div class="navbar">
                <a href="/html/index.html" class="BigLogo"><img src="..\..\public\Images\Logo.jpg" ></a> <!-- Saite uz sākumlapu un logo -->
            
                <a class="pressed1" href="../html/Library.html"><i style="font-size:16px" class="fa">&#xf02d;</i> Bibliotēka</a> <!-- Saite uz lapu "Bibliotēka" -->
                <a class="pressed1" href="../html/Bookmarks.html"><i style="font-size:16px;" class="fa">&#xf02e;</i> Grāmatzīmes</a> <!-- Saite uz lapu "Grāmatzīmes" -->
                <a class="pressed1"><i style="font: size 16px" class="fa">&#xf040;</i> Rakstīšana</a> <!-- Saite uz lapu "Rakstīšana" -->
                
                <a href="javascript:void(0);" class="icon" onclick="myFunction()">
                    <i class="fa fa-bars"></i>
                </a>

                <div id="myLinks">
                    <a href="#news">News</a>
                    <a href="#contact">Contact</a>
                    <a href="#about">About</a>
                </div>
            </div>  
            <div class="account"> <!-- Bloks konta pārvaldīšanai -->
                <a class="pressed2" href="#SigIn"><i style="font-size:16px" class="fa">&#xf2bd;</i> Reģistrācija</a> <!-- Saite uz reģistrācijas lapu -->
                <a class="pressed2" href="#LogIn"> <i style="font-size:16px" class="fa">&#xf2be;</i> Pieslēgties</a> <!-- Saite uz pierakstīšanās lapu -->
                <div class="search"> <!-- Meklēšanas josla -->
                    <input type="text" class="input" placeholder="Meklēt grāmatu..."> <!-- Ievades lauks meklēšanai -->
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
        display: flex; /* Flexbox izkārtojums */
        align-items: center; /* Elementu vertikāla izlīdzināšana */
        background-color: #c58667; /* Fona krāsa navigācijas joslas augšā */
        height: 55px; 
        box-shadow: rgba(63, 31, 4, 0.8) 0px 0px 15px; /* Ēna navigācijas joslas apakšā */
        overflow: hidden;
        position: relative;
    }
    #myLinks {
    display: none; /* Скрываем элемент */
    flex-direction: column; /* Выравниваем элементы вертикально */
    background-color: #c58667; /* Цвет фона */
    position: absolute; /* Позиционируем относительно родителя */
    top: 55px; /* Устанавливаем ниже навигации */
    right: 0;
    width: 100%; /* Меню будет занимать всю ширину */
    z-index: 1000; /* Приоритет слоя */
}

/* Показываем блок, если добавлен класс active */
    #myLinks.active {
        display: flex;
    }

    .navigation-bar > div {
        margin: 2px; /* Atstarpe ap elementiem */
        padding: 2px; /* Iekšējās atstarpes */
    }

    .navbar{
        display: flex; /* Flexbox izkārtojums */
        align-items: center; /* Elementu vertikāla izlīdzināšana */
        flex-grow: 1; /* Izplešas, lai aizpildītu vietu */
    }

    /* Konta pārvaldīšanas bloks */
    .account{
        display: flex; /* Flexbox izkārtojums konta sadaļai */
        margin-left: auto; /* Novietojam konta bloku pa labi */
        text-align: center; /* Centrējam tekstu */
    }

    /* Navigācijas joslas saites */
    .pressed1{
        color: rgba(26, 16, 8, 0.8); /*Teksta krāsa */
        text-align: center; /* Centrējam tekstu */
        text-decoration: none; /* Noņemam noklusēto teksta apakšsvītrojumu */
        font-size: 17px; /* Fonta izmērs navigācijas tekstam */
        cursor: pointer; /* Mainam peles formu uz rādītāju */
        font-family: Tahoma, Helvetica, sans-serif; /* Fonta tips */
        margin: 10px; /* Atstarpe ap elementiem */
    }

    .pressed2{
        color: rgba(26, 16, 8, 0.8); /*Teksta krāsa */
        text-align: center; /* Centrējam tekstu */
        text-decoration: none; /* Noņemam noklusēto teksta apakšsvītrojumu */
        font-size: 17px; /* Fonta izmērs navigācijas tekstam */
        font-family: Tahoma, Helvetica, sans-serif; /* Fonta tips */
        margin: 10px; /* Atstarpe ap elementiem */

    }
    
    .pressed2:hover .fa{
        color: rgba(255, 187, 142, 0.8); /*Teksts, kad pele tiek pārvilkta */

    }
    .pressed2:hover {
        color: rgba(255, 187, 142, 0.8); /*Teksts, kad pele tiek pārvilkta */
    }
    .pressed1:hover .fa{
        color: rgba(255, 187, 142, 0.8); /*Teksts, kad pele tiek pārvilkta */

    }
    .pressed1:hover{
        color: rgba(255, 187, 142, 0.8); /*Teksts, kad pele tiek pārvilkta */
    }
    
    /* Meklēšanas josla */
    .search {
        display: flex;  /* Flexbox izkārtojums konta sadaļai */
        align-items: center;  /* Elementu vertikāla izlīdzināšana */
    }

    .search:hover {
        transform: none; /*noņemam transformāciju, kad pele tiek pārvilkta */
    }

    /* Ievades lauks meklēšanai */
    .search .input {
        background-color: #ffffff; /*Krasa fona */
        border: 0; /* Noņemam apmales */
        border-radius: 20px; /* Noapaļo apmalas*/
        border-color: rgba(26, 16, 8, 0.8); /* Mainam apmales krāsu */
        font-size: 15px; /* Fonta izmērs */
        padding: 10px; /* Iekšējās atstarpes */
        height: 10px; 
        width: 0; /* Sakam ar nulles platumu */
        overflow: hidden; /* Paslēpjam pārplūdes elementus */
        opacity: 0; /* Paslēpjam elementu */
    }

    /* Poga meklēšanai */
    .search .btn {
        background-color: #c58667; 
        border: 2px solid rgba(26, 16, 8, 0.8); /*apmales vērtības */
        border-radius: 20px;
        padding: 7px; /* Iekšējās atstarpes */
        cursor: pointer; /* Peles formāts */
        outline: none; /* Noņemam noklusēto apmales stāvokli */
        margin-right: 10px; /* Atstarpe no labās puses */
        width: 33px; 
        height: 33px;
    }

    /* Meklēšanas joslas aktīvā stāvoklis */
    .search.active .input {
        width: 150px; 
        height: 5px;
        opacity: 1; /* Parādam elementu */
        margin: 5px;
    }

    .input{
        color: rgba(26, 16, 8, 0.8);
        font-family: Tahoma, Helvetica, sans-serif; /* Fonta tips */
    }
    
    .input:focus {
        outline: none; /* Noņemam noklusēto apmales stāvokli */
    }
    .btn:hover {
        border-color: rgba(255, 187, 142, 0.8); /* Mainam apmales krāsu, kad pele tiek pārvilkta */
    }
    .btn:hover .fa {
        color: rgba(255, 187, 142, 0.8); /* Mainam ikonas krāsu, kad pele tiek pārvilkta */
    }
    .fa{
        color: rgba(26, 16, 8, 0.8); 

    }
    
    @media screen and (max-width: 1200px) {
        .navigation-bar {
            
            height: auto; /* Augstumu uz automātisku */
        }
        .pressed1 {
            display: none; /* Paslēpjam saites */
        }
        .pressed2 {
            display: none; /* Paslēpjam saites */
        }
        .BigLogo {
            display: none; /* Paslēpjam logo */
        }
    }
    @media screen and (min-width: 1200px) {
        .icon {
            display: none; /* Paslēpjam meklēšanas joslu */
        }
        
    }
</style>

<script>

// Meklēšanas joslas funkcionalitāte
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

document.addEventListener("DOMContentLoaded", () => {
    window.myFunction = function() {
        const x = document.getElementById("myLinks");
        if (x.style.display === "block") {
            x.style.display = "none";
        } else {
            x.style.display = "block";
        }
    };
});

</script>