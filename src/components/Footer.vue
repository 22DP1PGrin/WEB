<template>
    <!-- Kājene ar saitēm uz dažādām lapām -->
<footer id="footer">
    <div class="footer-container">
        <div class="footer-section">
            <ul class="footer-links">
                <li><a href="#FAQ">FAQ</a></li> <!-- Saite uz atbalsta dienestu -->
                <li><a href="#UserAgreement">User Agreement</a></li> <!-- Saite uz lietotāja līgumu -->
            </ul>
        </div>
        <div class="footer-section">
            <ul class="footer-links">
                <li><a href="#Copyright">Copyright</a></li> <!-- Saite uz autortiesībām -->
                <li><a href="#PrivacyPolicy">Privacy Policy</a></li> <!-- Saite uz privātumu -->
            </ul>
        </div>
    </div>
</footer>

</template>

<style scoped> 
    /* Footer */
footer {
    text-align: center; /* Teksta centrēšana */
    background-image: linear-gradient(#f5b89a,#c58667,#704733); /* Fona attēla gradienta iestatījums */
    justify-content: space-around; /* Telpas starp sadaļām */
    padding: 25px; /* Atstarpe ap konteineru */
    max-width: 100%; /* Veido maksimalo garums */
}

.footer-container {
    display: flex; /* Flexbox izkārtojums */
    justify-content: center; /* Centrējam kolonnas */
}

.footer-section {
    margin: 0 30px; /* Atstarpe starp sadaļām */
}

.footer-links {
    list-style: none; /* Noņemam saraksta marķierus */
}

.footer-links li {
    margin: 5px 0; /* Atstarpe starp saraksta elementiem */
}

.footer-links a {
    color: rgba(20, 13, 7, 0.8); /* Saites teksta krāsa */
    text-decoration: none; /* Noņemam apakšsvītrojumu */
    transition: transform 0.3s ease; /* Gluda pāreja transformācijai */
    display: inline-block; /* Nodrošinām, ka mērogošana darbojas pareizi */
}

.footer-links a:hover {
    color: rgba(241, 189, 141, 0.8); /* Teksta krāsa saitēm, kad pele tiek pārvilkta */
    transform: scale(1.2); /* Saites mērogošana uz augšu, kad pele ir virs tām */
}

</style>