<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>SIEMENS - Saltwater Barrier Dam SCADA</title>

    <style>

        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
            font-family: "Segoe UI", Arial, sans-serif;
        }

        body{
            background:#0b0f14;
            color:white;
            min-height:100vh;
        }

        /* TOP HEADER */

        .topbar{
            width:100%;
            height:70px;
            background:#009999;
            display:flex;
            align-items:center;
            justify-content:space-between;
            padding:0 30px;
            box-shadow:0 3px 10px rgba(0,0,0,0.4);
        }

        .logo{
            font-size:28px;
            font-weight:bold;
            letter-spacing:2px;
        }

        .system-name{
            font-size:20px;
            font-weight:500;
        }

        .status-box{
            display:flex;
            align-items:center;
            gap:10px;
            font-size:16px;
        }

        .status-light{
            width:14px;
            height:14px;
            border-radius:50%;
            background:#00ff66;
            box-shadow:0 0 10px #00ff66;
        }

        /* MAIN */

        .main{
            padding:40px;
        }

        .section-title{
            font-size:30px;
            margin-bottom:30px;
            color:#00d9d9;
        }

        /* STATION GRID */

        .station-grid{
            display:grid;
            grid-template-columns:repeat(auto-fit,minmax(320px,1fr));
            gap:30px;
        }

        /* CARD */

        .station-card{
            background:#1a1f26;
            border:2px solid #009999;
            border-radius:16px;
            overflow:hidden;
            transition:0.3s;
            box-shadow:0 0 15px rgba(0,255,255,0.08);
        }

        .station-card:hover{
            transform:translateY(-8px);
            box-shadow:0 0 25px rgba(0,255,255,0.2);
        }

        .card-header{
            background:#009999;
            padding:18px;
            font-size:24px;
            font-weight:bold;
            text-align:center;
        }

        .card-body{
            padding:30px;
        }

        .parameter{
            display:flex;
            justify-content:space-between;
            margin-bottom:18px;
            padding-bottom:10px;
            border-bottom:1px solid #2d3748;
            font-size:17px;
        }

        .parameter-name{
            color:#cbd5e1;
        }

        .parameter-value{
            color:#00ff99;
            font-weight:bold;
        }

        /* BUTTON */

        .access-btn{
            width:100%;
            margin-top:25px;
            padding:16px;
            border:none;
            border-radius:10px;
            background:#00b894;
            color:white;
            font-size:18px;
            font-weight:bold;
            cursor:pointer;
            transition:0.3s;
        }

        .access-btn:hover{
            background:#00d1a7;
            transform:scale(1.02);
        }

        /* FOOTER */

        footer{
            text-align:center;
            padding:20px;
            color:#94a3b8;
            border-top:1px solid #1e293b;
            margin-top:50px;
        }

        /* RESPONSIVE */

        @media(max-width:768px){

            .topbar{
                flex-direction:column;
                height:auto;
                gap:10px;
                padding:15px;
            }

            .main{
                padding:20px;
            }

            .section-title{
                text-align:center;
            }

        }

    </style>

</head>

<body>

    <!-- TOP BAR -->

    <div class="topbar">

        <div class="logo">
            SIEMENS
        </div>

        <div class="system-name">
            Saltwater Barrier Dam SCADA System
        </div>

        <div class="status-box">
            <div class="status-light"></div>
            System Online
        </div>

    </div>

    <!-- MAIN CONTENT -->

    <div class="main">

        <div class="section-title">
            Remote Monitoring Stations
        </div>

        <div class="station-grid">

            <!-- STATION 1 -->

            <div class="station-card">

                <div class="card-header">
                    STATION 1
                </div>

                <div class="card-body">

                    <div class="parameter">
                        <div class="parameter-name">Gate Status</div>
                        <div class="parameter-value">NORMAL</div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">Water Level</div>
                        <div class="parameter-value">2.35 m</div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">Salinity</div>
                        <div class="parameter-value">0.8 ppt</div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">Communication</div>
                        <div class="parameter-value">ONLINE</div>
                    </div>

                    <!-- CHANGE YOUR NGROK LINK -->

                    <button class="access-btn"
                    onclick="window.open('https://your-ngrok-link-1.ngrok-free.app')">

                        ACCESS STATION

                    </button>

                </div>

            </div>

            <!-- STATION 2 -->

            <div class="station-card">

                <div class="card-header">
                    STATION 2
                </div>

                <div class="card-body">

                    <div class="parameter">
                        <div class="parameter-name">Gate Status</div>
                        <div class="parameter-value">NORMAL</div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">Water Level</div>
                        <div class="parameter-value">1.92 m</div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">Salinity</div>
                        <div class="parameter-value">1.1 ppt</div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">Communication</div>
                        <div class="parameter-value">ONLINE</div>
                    </div>

                    <!-- CHANGE YOUR NGROK LINK -->

                    <button class="access-btn"
                    onclick="window.open('https://your-ngrok-link-2.ngrok-free.app')">

                        ACCESS STATION

                    </button>

                </div>

            </div>

            <!-- STATION 3 -->

            <div class="station-card">

                <div class="card-header">
                    STATION 3
                </div>

                <div class="card-body">

                    <div class="parameter">
                        <div class="parameter-name">Gate Status</div>
                        <div class="parameter-value">NORMAL</div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">Water Level</div>
                        <div class="parameter-value">2.10 m</div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">Salinity</div>
                        <div class="parameter-value">0.6 ppt</div>
                    </div>

                    <div class="parameter">
                        <div class="parameter-name">Communication</div>
                        <div class="parameter-value">ONLINE</div>
                    </div>

                    <!-- CHANGE YOUR NGROK LINK -->

                    <button class="access-btn"
                    onclick="window.open('https://your-ngrok-link-3.ngrok-free.app')">

                        ACCESS STATION

                    </button>

                </div>

            </div>

        </div>

    </div>

    <!-- FOOTER -->

    <footer>

        SCADA Monitoring Platform | IoT2050 + Node-RED Integration

    </footer>

</body>

</html>
