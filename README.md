<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>SIEMENS SCADA - Saltwater Barrier Dam</title>

    <style>

        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
            font-family:"Segoe UI", Arial, sans-serif;
        }

        body{
            background:#050b12;
            color:white;
            min-height:100vh;
        }

        /* =========================================
           TOP HEADER
        ========================================= */

        .topbar{

            width:100%;
            height:85px;

            background:#009999;

            display:flex;
            align-items:center;
            justify-content:space-between;

            padding:0 40px;

            box-shadow:0 3px 15px rgba(0,0,0,0.5);

        }

        .logo{

            font-size:42px;
            font-weight:bold;
            letter-spacing:2px;

        }

        .title{

            font-size:30px;
            font-weight:600;

        }

        .system-status{

            display:flex;
            align-items:center;
            gap:12px;

            font-size:20px;

        }

        .status-light{

            width:16px;
            height:16px;

            border-radius:50%;

            background:#00ff66;

            box-shadow:0 0 10px #00ff66;

        }

        /* =========================================
           MAIN
        ========================================= */

        .main{

            padding:35px;

        }

        .section-title{

            font-size:52px;
            color:#00e5ff;

            margin-bottom:45px;

            text-shadow:0 0 20px rgba(0,255,255,0.3);

        }

        /* =========================================
           GRID
        ========================================= */

        .station-grid{

            display:grid;

            grid-template-columns:repeat(3,1fr);

            gap:25px;

        }

        /* =========================================
           CARD
        ========================================= */

        .station-card{

            background:#1b222c;

            border:2px solid #00c3ff;

            border-radius:18px;

            overflow:hidden;

            transition:0.3s;

            box-shadow:0 0 20px rgba(0,255,255,0.08);

        }

        .station-card:hover{

            transform:translateY(-8px);

            box-shadow:0 0 30px rgba(0,255,255,0.2);

        }

        .card-header{

            background:#009999;

            padding:24px;

            text-align:center;

            font-size:34px;
            font-weight:bold;

        }

        .card-body{

            padding:28px;

        }

        /* =========================================
           PARAMETERS
        ========================================= */

        .parameter{

            display:flex;

            justify-content:space-between;

            align-items:center;

            padding:15px 0;

            border-bottom:1px solid #2b3645;

            font-size:20px;

        }

        .parameter-name{

            color:#dbeafe;

        }

        .parameter-value{

            color:#00ff99;

            font-weight:bold;

        }

        /* =========================================
           BUTTON
        ========================================= */

        .access-btn{

            width:100%;

            margin-top:30px;

            padding:18px;

            border:none;

            border-radius:12px;

            background:#00b894;

            color:white;

            font-size:22px;
            font-weight:bold;

            cursor:pointer;

            transition:0.3s;

        }

        .access-btn:hover{

            background:#00d8aa;

            transform:scale(1.02);

        }

        /* =========================================
           FOOTER
        ========================================= */

        footer{

            margin-top:50px;

            text-align:center;

            color:#94a3b8;

            padding:20px;

            border-top:1px solid #1e293b;

            font-size:16px;

        }

        /* =========================================
           RESPONSIVE
        ========================================= */

        @media(max-width:1200px){

            .station-grid{

                grid-template-columns:1fr;

            }

        }

    </style>

</head>

<body>

    <!-- =========================================
         HEADER
    ========================================= -->

    <div class="topbar">

        <div class="logo">

            SIEMENS

        </div>

        <div class="title">

            Saltwater Barrier Dam SCADA System

        </div>

        <div class="system-status">

            <div class="status-light"></div>

            System Online

        </div>

    </div>

    <!-- =========================================
         MAIN
    ========================================= -->

    <div class="main">

        <div class="section-title">

            Remote Monitoring Stations

        </div>

        <div class="station-grid">

            <!-- =========================================
                 STATION 1
            ========================================= -->

            <div class="station-card">

                <div class="card-header">

                    STATION 1

                </div>

                <div class="card-body">

                    <div class="parameter">

                        <div class="parameter-name">

                            Upstream Water Level

                        </div>

                        <div class="parameter-value"
                             id="waterUp1">

                             0.0 m

                        </div>

                    </div>

                    <div class="parameter">

                        <div class="parameter-name">

                            Water Level Inside

                        </div>

                        <div class="parameter-value"
                             id="waterInside1">

                             0.0 m

                        </div>

                    </div>

                    <div class="parameter">

                        <div class="parameter-name">

                            River Salinity

                        </div>

                        <div class="parameter-value"
                             id="salinity1">

                             0.0 ppt

                        </div>

                    </div>

                    <div class="parameter">

                        <div class="parameter-name">

                            Communication

                        </div>

                        <div class="parameter-value"
                             id="status1">

                             ONLINE

                        </div>

                    </div>

                    <!-- BUTTON -->

                    <button class="access-btn"

                    onclick="window.open(
                    'https://YOUR-NGROK-STATION1.ngrok-free.app'
                    )">

                        ACCESS STATION 1

                    </button>

                </div>

            </div>

            <!-- =========================================
                 STATION 2
            ========================================= -->

            <div class="station-card">

                <div class="card-header">

                    STATION 2

                </div>

                <div class="card-body">

                    <div class="parameter">

                        <div class="parameter-name">

                            Upstream Water Level

                        </div>

                        <div class="parameter-value"
                             id="waterUp2">

                             0.0 m

                        </div>

                    </div>

                    <div class="parameter">

                        <div class="parameter-name">

                            Water Level Inside

                        </div>

                        <div class="parameter-value"
                             id="waterInside2">

                             0.0 m

                        </div>

                    </div>

                    <div class="parameter">

                        <div class="parameter-name">

                            River Salinity

                        </div>

                        <div class="parameter-value"
                             id="salinity2">

                             0.0 ppt

                        </div>

                    </div>

                    <div class="parameter">

                        <div class="parameter-name">

                            Communication

                        </div>

                        <div class="parameter-value"
                             id="status2">

                             ONLINE

                        </div>

                    </div>

                    <!-- BUTTON -->

                    <button class="access-btn"

                    onclick="window.open(
                    'https://YOUR-NGROK-STATION2.ngrok-free.app'
                    )">

                        ACCESS STATION 2

                    </button>

                </div>

            </div>

            <!-- =========================================
                 STATION 3
            ========================================= -->

            <div class="station-card">

                <div class="card-header">

                    STATION 3

                </div>

                <div class="card-body">

                    <div class="parameter">

                        <div class="parameter-name">

                            Upstream Water Level

                        </div>

                        <div class="parameter-value"
                             id="waterUp3">

                             0.0 m

                        </div>

                    </div>

                    <div class="parameter">

                        <div class="parameter-name">

                            Water Level Inside

                        </div>

                        <div class="parameter-value"
                             id="waterInside3">

                             0.0 m

                        </div>

                    </div>

                    <div class="parameter">

                        <div class="parameter-name">

                            River Salinity

                        </div>

                        <div class="parameter-value"
                             id="salinity3">

                             0.0 ppt

                        </div>

                    </div>

                    <div class="parameter">

                        <div class="parameter-name">

                            Communication

                        </div>

                        <div class="parameter-value"
                             id="status3">

                             ONLINE

                        </div>

                    </div>

                    <!-- BUTTON -->

                    <button class="access-btn"

                    onclick="window.open(
                    'https://YOUR-NGROK-STATION3.ngrok-free.app'
                    )">

                        ACCESS STATION 3

                    </button>

                </div>

            </div>

        </div>

    </div>

    <!-- =========================================
         FOOTER
    ========================================= -->

    <footer>

        SCADA Monitoring Platform |
        IoT2050 + Node-RED + Modbus TCP

    </footer>

    <!-- =========================================
         JAVASCRIPT REALTIME
    ========================================= -->

    <script>

        /*
        ============================================
        STATION 1
        ============================================
        */

        async function loadStation1(){

            try{

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

                document.getElementById("status1").innerHTML =
                    "ONLINE";

            }
            catch(error){

                document.getElementById("status1").innerHTML =
                    "OFFLINE";

            }

        }

        /*
        ============================================
        STATION 2
        ============================================
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

                document.getElementById("status2").innerHTML =
                    "ONLINE";

            }
            catch(error){

                document.getElementById("status2").innerHTML =
                    "OFFLINE";

            }

        }

        /*
        ============================================
        STATION 3
        ============================================
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

                document.getElementById("status3").innerHTML =
                    "ONLINE";

            }
            catch(error){

                document.getElementById("status3").innerHTML =
                    "OFFLINE";

            }

        }

        /*
        ============================================
        UPDATE ALL STATIONS
        ============================================
        */

        function updateAllStations(){

            loadStation1();

            loadStation2();

            loadStation3();

        }

        /*
        UPDATE EVERY 2 SECONDS
        */

        setInterval(updateAllStations,2000);

        updateAllStations();

    </script>

</body>

</html>
