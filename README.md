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

        /* ================= HEADER ================= */

        .topbar{
            width:100%;
            height:80px;
            background:#009999;
            display:flex;
            align-items:center;
            justify-content:space-between;
            padding:0 40px;
            box-shadow:0 3px 15px rgba(0,0,0,0.5);
        }

        .logo{
            font-size:40px;
            font-weight:bold;
            letter-spacing:2px;
        }

        .title{
            font-size:28px;
            font-weight:600;
        }

        .system-status{
            display:flex;
            align-items:center;
            gap:10px;
            font-size:18px;
        }

        .status-light{
            width:16px;
            height:16px;
            border-radius:50%;
            background:#00ff66;
            box-shadow:0 0 10px #00ff66;
        }

        /* ================= MAIN ================= */

        .main{
            padding:35px;
        }

        .section-title{
            font-size:42px;
            color:#00e5ff;
            margin-bottom:40px;
        }

        /* ================= GRID ================= */

        .station-grid{
            display:grid;

            /* 3 station cùng 1 hàng */
            grid-template-columns:repeat(3,1fr);

            gap:25px;
        }

        /* ================= CARD ================= */

        .station-card{
            background:#1b222c;
            border:2px solid #00bcd4;
            border-radius:18px;
            overflow:hidden;
            transition:0.3s;
            box-shadow:0 0 20px rgba(0,255,255,0.08);
        }

        .station-card:hover{
            transform:translateY(-8px);
            box-shadow:0 0 25px rgba(0,255,255,0.2);
        }

        .card-header{
            background:#009999;
            padding:22px;
            text-align:center;
            font-size:30px;
            font-weight:bold;
        }

        .card-body{
            padding:25px;
        }

        /* ================= PARAMETER ================= */

        .parameter{
            display:flex;
            justify-content:space-between;
            align-items:center;
            padding:14px 0;
            border-bottom:1px solid #2b3645;
            font-size:18px;
        }

        .parameter-name{
            color:#dbeafe;
        }

        .parameter-value{
            color:#00ff99;
            font-weight:bold;
        }

        /* ================= BUTTON ================= */

        .access-btn{
            width:100%;
            margin-top:30px;
            padding:18px;
            border:none;
            border-radius:10px;
            background:#00b894;
            color:white;
            font-size:20px;
            font-weight:bold;
            cursor:pointer;
            transition:0.3s;
        }

        .access-btn:hover{
            background:#00d6aa;
            transform:scale(1.02);
        }

        /* ================= FOOTER ================= */

        footer{
            margin-top:50px;
            text-align:center;
            color:#94a3b8;
            padding:20px;
            border-top:1px solid #1e293b;
        }

        /* ================= RESPONSIVE ================= */

        @media(max-width:1200px){

            .station-grid{
                grid-template-columns:1fr;
            }

        }

    </style>

</head>

<body>

    <!-- ================= HEADER ================= -->

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

    <!-- ================= MAIN ================= -->

    <div class="main">

        <div class="section-title">
            Remote Monitoring Stations
        </div>

        <div class="station-grid">

            <!-- ================================================= -->
            <!-- STATION 1 -->
            <!-- ================================================= -->

            <div class="station-card">

                <div class="card-header">
                    STATION 1
                </div>

                <div class="card-body">

                    <!-- dữ liệu realtime từ node-red -->
                    <div class="parameter">
                        <div class="parameter-name">
                            Upstream Water Level
                        </div>

                        <div class="parameter-value" id="waterUp1">
                            0.0 m
                        </div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">
                            Water Level Inside
                        </div>

                        <div class="parameter-value" id="waterInside1">
                            0.0 m
                        </div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">
                            River Salinity
                        </div>

                        <div class="parameter-value" id="salinity1">
                            0.0 ppt
                        </div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">
                            Communication
                        </div>

                        <div class="parameter-value">
                            ONLINE
                        </div>
                    </div>

                    <!-- BUTTON TRUY CẬP NODE RED -->

                    <button class="access-btn"
                    onclick="window.open('https://YOUR-NGROK-STATION1.ngrok-free.app')">

                        ACCESS STATION 1

                    </button>

                </div>

            </div>

            <!-- ================================================= -->
            <!-- STATION 2 -->
            <!-- ================================================= -->

            <div class="station-card">

                <div class="card-header">
                    STATION 2
                </div>

                <div class="card-body">

                    <div class="parameter">
                        <div class="parameter-name">
                            Upstream Water Level
                        </div>

                        <div class="parameter-value" id="waterUp2">
                            0.0 m
                        </div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">
                            Water Level Inside
                        </div>

                        <div class="parameter-value" id="waterInside2">
                            0.0 m
                        </div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">
                            River Salinity
                        </div>

                        <div class="parameter-value" id="salinity2">
                            0.0 ppt
                        </div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">
                            Communication
                        </div>

                        <div class="parameter-value">
                            ONLINE
                        </div>
                    </div>

                    <button class="access-btn"
                    onclick="window.open('https://YOUR-NGROK-STATION2.ngrok-free.app')">

                        ACCESS STATION 2

                    </button>

                </div>

            </div>

            <!-- ================================================= -->
            <!-- STATION 3 -->
            <!-- ================================================= -->

            <div class="station-card">

                <div class="card-header">
                    STATION 3
                </div>

                <div class="card-body">

                    <div class="parameter">
                        <div class="parameter-name">
                            Upstream Water Level
                        </div>

                        <div class="parameter-value" id="waterUp3">
                            0.0 m
                        </div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">
                            Water Level Inside
                        </div>

                        <div class="parameter-value" id="waterInside3">
                            0.0 m
                        </div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">
                            River Salinity
                        </div>

                        <div class="parameter-value" id="salinity3">
                            0.0 ppt
                        </div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">
                            Communication
                        </div>

                        <div class="parameter-value">
                            ONLINE
                        </div>
                    </div>

                    <button class="access-btn"
                    onclick="window.open('https://YOUR-NGROK-STATION3.ngrok-free.app')">

                        ACCESS STATION 3

                    </button>

                </div>

            </div>

        </div>

    </div>

    <!-- ================= FOOTER ================= -->

    <footer>

        SCADA Monitoring Platform | IoT2050 + Node-RED + Modbus TCP

    </footer>

    <!-- ================= JAVASCRIPT ================= -->

    <script>

        /*
        ===================================================
        DEMO REALTIME DATA
        ===================================================

        Sau này Node-RED sẽ gửi dữ liệu thật qua MQTT
        hoặc HTTP API.

        */

        function randomData(){

            // STATION 1
            document.getElementById("waterUp1").innerHTML =
                (Math.random()*3).toFixed(2) + " m";

            document.getElementById("waterInside1").innerHTML =
                (Math.random()*2).toFixed(2) + " m";

            document.getElementById("salinity1").innerHTML =
                (Math.random()*5).toFixed(2) + " ppt";

            // STATION 2
            document.getElementById("waterUp2").innerHTML =
                (Math.random()*3).toFixed(2) + " m";

            document.getElementById("waterInside2").innerHTML =
                (Math.random()*2).toFixed(2) + " m";

            document.getElementById("salinity2").innerHTML =
                (Math.random()*5).toFixed(2) + " ppt";

            // STATION 3
            document.getElementById("waterUp3").innerHTML =
                (Math.random()*3).toFixed(2) + " m";

            document.getElementById("waterInside3").innerHTML =
                (Math.random()*2).toFixed(2) + " m";

            document.getElementById("salinity3").innerHTML =
                (Math.random()*5).toFixed(2) + " ppt";
        }

        // update mỗi 2 giây
        setInterval(randomData,2000);

    </script>

</body>

</html>
