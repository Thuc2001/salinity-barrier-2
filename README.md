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

    background:#071018;
    color:white;
    min-height:100vh;

}

/* =======================================
HEADER
======================================= */

.topbar{

    width:100%;
    height:85px;

    background:#009999;

    display:flex;
    justify-content:space-between;
    align-items:center;

    padding:0 40px;

    box-shadow:0 3px 15px rgba(0,0,0,0.4);

}

.logo{

    font-size:42px;
    font-weight:bold;
    letter-spacing:2px;

}

.title{

    font-size:28px;
    font-weight:600;

}

.status{

    display:flex;
    align-items:center;
    gap:12px;

    font-size:18px;

}

.light{

    width:16px;
    height:16px;

    border-radius:50%;

    background:#00ff66;

    box-shadow:0 0 12px #00ff66;

}

/* =======================================
MAIN
======================================= */

.main{

    padding:40px;

}

.section-title{

    font-size:50px;

    color:#00e5ff;

    margin-bottom:45px;

}

/* =======================================
GRID
======================================= */

.station-grid{

    display:grid;

    grid-template-columns:repeat(3,1fr);

    gap:25px;

}

/* =======================================
CARD
======================================= */

.station-card{

    background:#1b222c;

    border:2px solid #00c3ff;

    border-radius:18px;

    overflow:hidden;

    transition:0.3s;

    box-shadow:0 0 20px rgba(0,255,255,0.08);

}

.station-card:hover{

    transform:translateY(-10px);

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

    padding:30px;

}

.parameter{

    display:flex;

    justify-content:space-between;

    padding:16px 0;

    border-bottom:1px solid #2b3645;

    font-size:19px;

}

.parameter-name{

    color:#cbd5e1;

}

.parameter-value{

    color:#00ff99;

    font-weight:bold;

}

/* =======================================
BUTTON
======================================= */

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

/* =======================================
FOOTER
======================================= */

footer{

    margin-top:50px;

    text-align:center;

    color:#94a3b8;

    padding:20px;

    border-top:1px solid #1e293b;

    font-size:16px;

}

/* =======================================
RESPONSIVE
======================================= */

@media(max-width:1200px){

    .station-grid{

        grid-template-columns:1fr;

    }

}

</style>

</head>

<body>

<!-- =======================================
HEADER
======================================= -->

<div class="topbar">

    <div class="logo">

        SIEMENS

    </div>

    <div class="title">

        Saltwater Barrier Dam SCADA System

    </div>

    <div class="status">

        <div class="light"></div>

        System Online

    </div>

</div>

<!-- =======================================
MAIN
======================================= -->

<div class="main">

    <div class="section-title">

        Remote Monitoring Stations

    </div>

    <div class="station-grid">

        <!-- =======================================
        STATION 1
        ======================================= -->

        <div class="station-card">

            <div class="card-header">

                STATION 1

            </div>

            <div class="card-body">

                <div class="parameter">

                    <div class="parameter-name">

                        Communication

                    </div>

                    <div class="parameter-value">

                        ONLINE

                    </div>

                </div>

                <div class="parameter">

                    <div class="parameter-name">

                        Controller

                    </div>

                    <div class="parameter-value">

                        IOT2050

                    </div>

                </div>

                <div class="parameter">

                    <div class="parameter-name">

                        SCADA

                    </div>

                    <div class="parameter-value">

                        NODE-RED

                    </div>

                </div>

                <button class="access-btn"

                onclick="window.open(
                'https://chlorophylloid-specifically-angeles.ngrok-free.dev/ui/#!/0?socketid=W1xVV4OzZvok39hCAAAD'
                )">

                    ACCESS STATION 1

                </button>

            </div>

        </div>

        <!-- =======================================
        STATION 2
        ======================================= -->

        <div class="station-card">

            <div class="card-header">

                STATION 2

            </div>

            <div class="card-body">

                <div class="parameter">

                    <div class="parameter-name">

                        Communication

                    </div>

                    <div class="parameter-value">

                        ONLINE

                    </div>

                </div>

                <div class="parameter">

                    <div class="parameter-name">

                        Controller

                    </div>

                    <div class="parameter-value">

                        IOT2050

                    </div>

                </div>

                <div class="parameter">

                    <div class="parameter-name">

                        SCADA

                    </div>

                    <div class="parameter-value">

                        NODE-RED

                    </div>

                </div>

                <button class="access-btn"

                onclick="window.open(
                '[https://freckles-remote-covenant.ngrok-free.dev/#flow/2531f58050f4a1a6](https://freckles-remote-covenant.ngrok-free.dev/ui/#!/0?socketid=KMn-QVZANMehV3m4AAAN#flow%2F2531f58050f4a1a6)'
                )">

                    ACCESS STATION 2

                </button>

            </div>

        </div>

        <!-- =======================================
        STATION 3
        ======================================= -->

        <div class="station-card">

            <div class="card-header">

                STATION 3

            </div>

            <div class="card-body">

                <div class="parameter">

                    <div class="parameter-name">

                        Communication

                    </div>

                    <div class="parameter-value">

                        OFFLINE

                    </div>

                </div>

                <div class="parameter">

                    <div class="parameter-name">

                        Controller

                    </div>

                    <div class="parameter-value">

                        NOT CONNECTED

                    </div>

                </div>

                <div class="parameter">

                    <div class="parameter-name">

                        SCADA

                    </div>

                    <div class="parameter-value">

                        NO DATA

                    </div>

                </div>

                <button class="access-btn">

                    NO STATION LINK

                </button>

            </div>

        </div>

    </div>

</div>

<!-- =======================================
FOOTER
======================================= -->

<footer>

    SCADA Monitoring Platform |
    IoT2050 + Node-RED + Modbus TCP

</footer>

</body>

</html>
