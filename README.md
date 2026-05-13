# Siemens SCADA Embedded Dashboard Website

```html
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

html{
    scroll-behavior:smooth;
}

body{

    background:
    linear-gradient(
        rgba(5,15,25,0.88),
        rgba(5,15,25,0.92)
    ),

    url("https://images.unsplash.com/photo-1518770660439-4636190af475?q=80&w=2070&auto=format&fit=crop");

    background-size:cover;
    background-position:center;
    background-attachment:fixed;

    color:white;
    min-height:100vh;

}

/* =======================================
HEADER
======================================= */

.topbar{

    width:100%;
    height:85px;

    background:rgba(0,153,153,0.92);

    backdrop-filter:blur(6px);

    display:flex;
    justify-content:space-between;
    align-items:center;

    padding:0 40px;

    box-shadow:0 3px 15px rgba(0,0,0,0.4);

    position:sticky;
    top:0;
    z-index:999;

}

.logo{

    font-size:42px;
    font-weight:bold;
    letter-spacing:2px;

    color:white;

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

    font-size:52px;

    color:#00e5ff;

    margin-bottom:45px;

    text-align:center;

    text-shadow:0 0 20px rgba(0,255,255,0.5);

}

/* =======================================
GRID
======================================= */

.station-grid{

    display:grid;

    grid-template-columns:repeat(2,1fr);

    gap:35px;

}

/* =======================================
CARD
======================================= */

.station-card{

    background:rgba(27,34,44,0.82);

    backdrop-filter:blur(10px);

    border:2px solid #00c3ff;

    border-radius:18px;

    overflow:hidden;

    transition:0.3s;

    box-shadow:0 0 25px rgba(0,255,255,0.15);

}

.station-card:hover{

    transform:translateY(-10px);

    box-shadow:0 0 35px rgba(0,255,255,0.3);

}

.card-header{

    background:#009999;

    padding:24px;

    text-align:center;

    font-size:34px;
    font-weight:bold;

    letter-spacing:1px;

}

.card-body{

    padding:30px;

}

.parameter{

    display:flex;

    justify-content:space-between;

    padding:16px 0;

    border-bottom:1px solid rgba(255,255,255,0.1);

    font-size:19px;

}

.parameter-name{

    color:#dbeafe;

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

    box-shadow:0 0 18px rgba(0,255,180,0.4);

}

/* =======================================
DASHBOARD VIEW
======================================= */

.dashboard-container{

    margin-top:50px;

    background:rgba(15,23,42,0.88);

    border:2px solid #00c3ff;

    border-radius:20px;

    overflow:hidden;

    box-shadow:0 0 30px rgba(0,255,255,0.18);

}

.dashboard-header{

    background:#009999;

    padding:20px;

    font-size:28px;
    font-weight:bold;

    text-align:center;

}

iframe{

    width:100%;

    height:900px;

    border:none;

    background:white;

}

/* =======================================
FOOTER
======================================= */

footer{

    margin-top:50px;

    text-align:center;

    color:#cbd5e1;

    padding:20px;

    border-top:1px solid rgba(255,255,255,0.1);

    font-size:16px;

    background:rgba(0,0,0,0.25);

}

/* =======================================
RESPONSIVE
======================================= */

@media(max-width:1000px){

    .station-grid{

        grid-template-columns:1fr;

    }

    iframe{

        height:650px;

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
                onclick="loadStation1()">

                    OPEN STATION 1 DASHBOARD

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
                onclick="loadStation2()">

                    OPEN STATION 2 DASHBOARD

                </button>

            </div>

        </div>

    </div>

    <!-- =======================================
    EMBEDDED DASHBOARD
    ======================================= -->

    <div class="dashboard-container" id="dashboardSection">

        <div class="dashboard-header" id="dashboardTitle">

            Select Station Dashboard

        </div>

        <iframe id="dashboardFrame"
        src="https://chlorophylloid-specifically-angeles.ngrok-free.dev/ui/">
        </iframe>

    </div>

</div>

<!-- =======================================
FOOTER
======================================= -->

<footer>

    SCADA Monitoring Platform |
    IoT2050 + Node-RED + Modbus TCP

</footer>

<!-- =======================================
JAVASCRIPT
======================================= -->

<script>

function loadStation1(){

    document.getElementById("dashboardTitle").innerHTML =
    "STATION 1 LIVE DASHBOARD";

    document.getElementById("dashboardFrame").src =
    "https://chlorophylloid-specifically-angeles.ngrok-free.dev/ui/";

    document.getElementById("dashboardSection")
    .scrollIntoView({behavior:"smooth"});

}

function loadStation2(){

    document.getElementById("dashboardTitle").innerHTML =
    "STATION 2 LIVE DASHBOARD";

    document.getElementById("dashboardFrame").src =
    "https://freckles-remote-covenant.ngrok-free.dev/ui/";

    document.getElementById("dashboardSection")
    .scrollIntoView({behavior:"smooth"});

}

</script>

</body>

</html>
```

Sau khi nhấn:

* `OPEN STATION 1 DASHBOARD`
* `OPEN STATION 2 DASHBOARD`

Dashboard sẽ nhúng trực tiếp xuống phía dưới website bằng `iframe`, không mở tab mới nữa.
