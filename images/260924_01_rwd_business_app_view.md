<!DOCTYPE html>
<html lang="zh-TW">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>260924-01__RWD</title>
    <style>
        :root {
            /* 星巴克風格配色變數 */
            --sbux-deep-green: #1E3932;
            /* 深綠色 */
            --sbux-core-green: #00704A;
            /* 經典星巴克綠 */
            --sbux-light-mint: #D4E9E2;
            /* 淺薄荷綠 */
            --sbux-cream-white: #F2F0EB;
            /* 奶油白 */
            --sbux-coffee-brown: #27251F;
            /* 咖啡黑棕色 */
            --sbux-gold: #CBA258;
            /* 點綴金 */
        }

        * {
            margin: 0;
            padding: 0;
        }

        body {
            /* 替換為深綠色背景 */
            background-color: var(--sbux-deep-green);
        }

        .wrapper {
            width: 1024px;
            margin-top: 0px;
            margin-bottom: 0;
            margin-left: auto;
            margin-right: auto;
        }

        .logo {
            width: 1024px;
            height: 220px;
            /* 替換為奶油白底色 */
            background-color: var(--sbux-cream-white);
            background-image: url(images/istockphoto-2292302950-612x612.jpg);
            background-position: center center;
            background-size: cover;
        }

        .nav {
            /* 替換為淺薄荷綠背景 */
            background-color: var(--sbux-light-mint);
            text-align: center;
            padding-top: 20px;
            padding-bottom: 20px;
        }

        .nav ul {
            display: inline-block;
        }

        .nav ul li {
            float: left;
            list-style-type: none;
        }

        .nav ul li a {
            text-decoration: none;
            /* 替換為經典星巴克綠 */
            background-color: var(--sbux-core-green);
            color: #fff;
            padding-top: 15px;
            padding-bottom: 15px;
            padding-left: 20px;
            padding-right: 20px;
            margin-right: 10px;
            border-radius: 5px;
            box-shadow: 1px 1px 1px 1px #585858;
            font-size: 20px;
            font-weight: bold;
        }

        .nav ul li a:hover {
            border-radius: 2px;
            /* 懸浮時加深顏色 */
            background-color: var(--sbux-deep-green);
            box-shadow: 1px 1px 1px 1px #fff;
        }

        .content {
            padding: 30px 80px;
            /* 替換為奶油白背景 */
            background-color: var(--sbux-cream-white);
            /* 加上咖啡黑棕色的內文字體顏色 */
            color: var(--sbux-coffee-brown);
        }

        .content h1 {
            text-align: center;
            /* 替換為經典星巴克綠 */
            color: var(--sbux-core-green);
            font-size: 48px;
        }

        .content p {
            font-size: 16px;
            margin-top: 20px;
            line-height: 200%;
        }

        .content a {
            display: block;
            /* 替換為經典星巴克綠 */
            background-color: var(--sbux-core-green);
            width: 150px;
            height: 40px;
            margin-top: 20px;
            margin-bottom: 0;
            margin-left: auto;
            margin-right: auto;
            text-decoration: none;
            color: #ffffff;
            text-align: center;
            font-size: 22px;
            font-weight: bold;
            line-height: 40px;
            border-radius: 20px;
            box-shadow: 2px 2px 2px 2px #aaaaaa;
        }

        .content a:hover {
            border-radius: 20px;
            /* 懸浮的陰影替換為星巴克點綴金 */
            box-shadow: 2px 2px 2px 2px var(--sbux-gold);
        }

        .footer {
            /* 替換為深綠色背景 */
            background-color: var(--sbux-deep-green);
            color: #fff;
            text-align: center;
            font-size: 24px;
            font-weight: bold;
            padding-top: 10px;
            padding-bottom: 10px;
        }

        /* 響應式 RWD 1024px 平板/一般手機版 */
        @media screen and (max-width: 1024px) {
            .wrapper {
                width: 95%;
            }

            .logo {
                width: 100%;
                height: 120px;
                background-image: url(images/istockphoto-610974126-612x612.jpg);
            }

            .nav ul {
                display: block;
                padding-left: 15px;
                padding-right: 15px;

            }

            .nav ul li {
                float: none;
            }

            .nav ul li a {
                display: block;
                margin-left: 0;
                margin-bottom: 5px;
                padding-top: 5px;
                padding-bottom: 5px;
                border-radius: 0;
                box-shadow: none;

            }

            .content {
                padding: 25px 30px;
            }

            .content h1 {
                font-size: 36px;
            }

            .content p {
                font-size: 18px;
            }

            .footer {
                font-size: 18px;
                padding-top: 5px;
                padding-bottom: 5px;
            }

        }

        /* 響應式 RWD 600px 行動裝置「商業風格 Web App」 */
        @media screen and (max-width: 600px) {
            /* 覆寫為商業風格配色 (專業藍、科技灰、純白) */
            :root {
                --sbux-deep-green: #1e293b;  /* 頁首/尾深藍灰 */
                --sbux-core-green: #0284c7;  /* 商業主色藍 */
                --sbux-light-mint: #ffffff;  /* 底部導航白底 */
                --sbux-cream-white: #f1f5f9; /* 淺灰背景，突顯卡片 */
                --sbux-coffee-brown: #334155; /* 深灰易讀文字 */
                --sbux-gold: #0369a1;        /* 按鈕懸浮深藍 */
            }

            body {
                background-color: var(--sbux-cream-white);
            }

            .wrapper {
                width: 100%;
            }

            /* App Header 風格：輕薄、無背景圖、吸頂 */
            .logo {
                width: 100%;
                height: 56px;
                background-image: none;
                background-color: var(--sbux-core-green);
                position: sticky;
                top: 0;
                z-index: 100;
                box-shadow: 0 2px 4px rgba(0,0,0,0.15);
            }

            /* 內容區塊 App 卡片化 */
            .content {
                padding: 20px 15px 80px 15px; /* 底部保留 80px 空間給固定導覽列 */
                background-color: transparent;
            }

            .content h1 {
                font-size: 24px;
                text-align: left;
                margin-bottom: 15px;
                padding-left: 12px;
                border-left: 4px solid var(--sbux-core-green); /* 商業風格側邊強調線 */
                color: var(--sbux-coffee-brown);
            }

            .content p {
                font-size: 15px;
                line-height: 1.7;
                background-color: #ffffff; /* 卡片白底 */
                padding: 16px;
                border-radius: 8px; /* 圓角卡片 */
                box-shadow: 0 2px 6px rgba(0,0,0,0.06); /* 柔和陰影 */
                margin-top: 0;
                margin-bottom: 12px;
                color: var(--sbux-coffee-brown);
            }

            /* 滿版風格按鈕 */
            .content a {
                width: 100%;
                height: 48px;
                line-height: 48px;
                font-size: 16px;
                border-radius: 8px;
                box-sizing: border-box;
                box-shadow: 0 4px 10px rgba(2, 132, 199, 0.25);
                margin-top: 25px;
            }

            .content a:hover {
                box-shadow: 0 4px 10px rgba(3, 105, 161, 0.4);
            }

            /* 底部固定導航列 (Bottom Navigation Bar) */
            .nav {
                position: fixed;
                bottom: 0;
                left: 0;
                width: 100%;
                padding: 0;
                background-color: var(--sbux-light-mint);
                box-shadow: 0 -2px 10px rgba(0,0,0,0.1);
                z-index: 1000;
            }

            .nav ul {
                display: flex; /* 改為彈性排列，平分底部空間 */
                padding: 0;
                margin: 0;
            }

            .nav ul li {
                flex: 1;
                text-align: center;
            }

            .nav ul li a {
                display: block;
                margin: 0;
                padding: 14px 2px;
                background-color: transparent;
                color: #64748b; /* 未選中時為灰色 */
                font-size: 13px;
                font-weight: 600;
                border-radius: 0;
                box-shadow: none;
                border-top: 3px solid transparent;
            }

            /* 模擬 App 觸碰反饋與目前所選狀態 */
            .nav ul li a:hover, 
            .nav ul li a:active {
                background-color: #f8fafc;
                color: var(--sbux-core-green);
                border-top: 3px solid var(--sbux-core-green);
                box-shadow: none;
            }

            /* 頁尾微調 */
            .footer {
                font-size: 12px;
                padding: 15px;
                margin-bottom: 50px; /* 避開底部導覽列 */
                font-weight: normal;
                background-color: var(--sbux-deep-green);
            }
        }
    </style>
</head>

<body>
    <div class="wrapper">

        <div class="banner">

            <div class="logo"></div>

            <div class="nav">
                <ul>
                    <li><a href="#">首頁</a></li>
                    <li><a href="#">最新消息</a></li>
                    <li><a href="#">合作店家</a></li>
                    <li><a href="#">關於我們</a></li>
                    <li><a href="#">聯絡我們</a></li>
                </ul>
            </div>
        </div>

        <div class="content">
            <h1>歡迎光臨</h1>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>
            <P>
                原理把它生物反對違反發行資源優惠台南本帖故意完整工人，隊伍希望不用加大影片相同查找勝利，網址保護詳細內容但在位元強烈答案平台培訓，我想大幅開發商傷心本人種子，獎勵做什麼明天狀態當前位置同步體系地球，召開鬱悶青春改造實際，廠商說到還可以年代崇拜三人名單，他。
            </P>

            <a href="#">了解更多</a>

        </div>

        <div class="footer">
            PowerBy XXX 2026.09.23
        </div>

    </div>

</body>

</html>