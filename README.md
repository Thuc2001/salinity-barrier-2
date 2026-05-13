<script>

/*
==================================================
STATION 1
==================================================
*/

async function loadStation1(){

    try{

        // API Node-RED station 1
        const response = await fetch(
            "https://YOUR-NGROK-STATION1.ngrok-free.app/api/status"
        );

        const data = await response.json();

        document.getElementById("waterUp1").innerHTML =
            data.waterUp + " m";

        document.getElementById("waterInside1").innerHTML =
            data.waterInside + " m";

        document.getElementById("salinity1").innerHTML =
            data.salinity + " ppt";

    }catch(error){

        console.log("Station 1 offline");

    }

}

/*
==================================================
STATION 2
==================================================
*/

async function loadStation2(){

    try{

        const response = await fetch(
            "https://YOUR-NGROK-STATION2.ngrok-free.app/api/status"
        );

        const data = await response.json();

        document.getElementById("waterUp2").innerHTML =
            data.waterUp + " m";

        document.getElementById("waterInside2").innerHTML =
            data.waterInside + " m";

        document.getElementById("salinity2").innerHTML =
            data.salinity + " ppt";

    }catch(error){

        console.log("Station 2 offline");

    }

}

/*
==================================================
STATION 3
==================================================
*/

async function loadStation3(){

    try{

        const response = await fetch(
            "https://YOUR-NGROK-STATION3.ngrok-free.app/api/status"
        );

        const data = await response.json();

        document.getElementById("waterUp3").innerHTML =
            data.waterUp + " m";

        document.getElementById("waterInside3").innerHTML =
            data.waterInside + " m";

        document.getElementById("salinity3").innerHTML =
            data.salinity + " ppt";

    }catch(error){

        console.log("Station 3 offline");

    }

}

/*
==================================================
AUTO UPDATE
==================================================
*/

function updateAllStations(){

    loadStation1();
    loadStation2();
    loadStation3();

}

/* update mỗi 2 giây */

setInterval(updateAllStations,2000);

updateAllStations();

</script>
