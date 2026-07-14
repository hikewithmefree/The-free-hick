<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Protocol</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Courier New', monospace;
            background: #000;
            color: #ccc;
            line-height: 1.7;
            -webkit-font-smoothing: antialiased;
            letter-spacing: 0.5px;
        }

        .hero {
            width: 100%;
            height: 60vh;
            background: #000;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            border-bottom: 1px solid #333;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: radial-gradient(circle at center, rgba(30,30,30,0.8) 0%, rgba(0,0,0,0.95) 100%);
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        .hero-content .number {
            font-size: 4rem;
            font-weight: 300;
            color: #fff;
            letter-spacing: 8px;
            opacity: 0.8;
        }

        .hero-content .label {
            font-size: 0.8rem;
            letter-spacing: 4px;
            color: #888;
            text-transform: uppercase;
            margin-top: 10px;
        }

        .divider-line {
            width: 40px;
            height: 1px;
            background: #555;
            margin: 40px auto;
        }

        .container {
            max-width: 540px;
            margin: 0 auto;
            padding: 25px;
        }

        .card {
            border: 1px solid #222;
            background: #0a0a0a;
            padding: 30px 25px;
            margin-bottom: 25px;
            border-radius: 2px;
        }

        .card h3 {
            color: #fff;
            font-size: 0.85rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            margin-bottom: 25px;
            text-align: center;
            font-weight: 400;
        }

        .spec-row {
            display: flex;
            justify-content: space-between;
            padding: 10px 0;
            border-bottom: 1px solid #111;
            font-size: 0.85rem;
        }

        .spec-row .spec-label {
            color: #666;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .spec-row .spec-value {
            color: #fff;
            letter-spacing: 1px;
        }

        .conversion-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }

        .conversion-table th {
            color: #666;
            font-size: 0.7rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            padding: 12px 8px;
            border-bottom: 1px solid #1a1a1a;
            font-weight: 400;
        }

        .conversion-table td {
            color: #aaa;
            text-align: center;
            padding: 14px 8px;
            border-bottom: 1px solid #0d0d0d;
            font-size: 0.9rem;
        }

        .conversion-table .highlight {
            color: #fff;
            font-weight: bold;
        }

        .video-btn {
            display: block;
            width: 100%;
            background: #0a0a0a;
            border: 1px solid #1a1a1a;
            padding: 16px 18px;
            margin-bottom: 8px;
            color: #aaa;
            text-decoration: none;
            font-size: 0.8rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            transition: all 0.2s ease;
            border-radius: 2px;
        }

        .video-btn:hover {
            border-color: #555;
            color: #fff;
            background: #111;
        }

        .video-btn .arrow {
            float: right;
            color: #555;
        }

        footer {
            text-align: center;
            padding: 60px 20px 40px;
            border-top: 1px solid #111;
            margin-top: 30px;
        }

        footer .main {
            font-size: 0.9rem;
            color: #888;
            letter-spacing: 2px;
            margin-bottom: 8px;
        }

        footer .sub {
            font-size: 0.7rem;
            color: #444;
            letter-spacing: 3px;
            text-transform: uppercase;
        }

        .disclaimer {
            text-align: center;
            color: #333;
            font-size: 0.65rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            padding: 20px;
        }
    </style>
</head>
<body>

    <div class="hero">
        <div class="hero-content">
            <div class="number">20</div>
            <div class="label">Research Protocol</div>
        </div>
    </div>

    <div class="container">

        <div class="card">
            <h3>Specifications</h3>
            <div class="spec-row">
                <span class="spec-label">Compound</span>
                <span class="spec-value">Retatrutide</span>
            </div>
            <div class="spec-row">
                <span class="spec-label">Mass</span>
                <span class="spec-value">20 mg</span>
            </div>
            <div class="spec-row">
                <span class="spec-label">Diluent</span>
                <span class="spec-value">1.0 mL BAC</span>
            </div>
            <div class="spec-row">
                <span class="spec-label">Concentration</span>
                <span class="spec-value">20 mg/mL</span>
            </div>
        </div>

        <div class="card">
            <h3>Dose Conversion — U-100</h3>
            <table class="conversion-table">
                <thead>
                    <tr>
                        <th>Units</th>
                        <th>Dose</th>
                    </tr>
                </thead>
                <tbody>
                    <tr><td>5 UI</td><td class="highlight">1 mg</td></tr>
                    <tr><td>10 UI</td><td class="highlight">2 mg</td></tr>
                    <tr><td>15 UI</td><td class="highlight">3 mg</td></tr>
                    <tr><td>20 UI</td><td class="highlight">4 mg</td></tr>
                    <tr><td>25 UI</td><td class="highlight">5 mg</td></tr>
                </tbody>
            </table>
        </div>

        <div class="divider-line"></div>

        <div class="card" style="padding: 20px 0; background: none; border: none;">
            <a href="https://youtu.be/ukCySPXN0WU" target="_blank" class="video-btn">
                Reconstitution <span class="arrow">→</span>
            </a>
            <a href="https://youtu.be/HGX8-Mnpf7M" target="_blank" class="video-btn">
                Injection Method <span class="arrow">→</span>
            </a>
            <a href="https://youtu.be/JFVGx9rkSzw" target="_blank" class="video-btn">
                Dosing Protocol <span class="arrow">→</span>
            </a>
            <a href="https://youtu.be/OrMf75kq3I8" target="_blank" class="video-btn">
                Storage <span class="arrow">→</span>
            </a>
            <a href="https://youtube.com/shorts/-M_4EA2grAQ" target="_blank" class="video-btn">
                Pen Setup <span class="arrow">→</span>
            </a>
            <a href="https://youtube.com/shorts/IoRSPJqc56c" target="_blank" class="video-btn">
                Drawing <span class="arrow">→</span>
            </a>
            <a href="https://youtube.com/shorts/DT4d7I4hVmo" target="_blank" class="video-btn">
                Technique <span class="arrow">→</span>
            </a>
        </div>

        <p class="disclaimer">For research purposes only</p>

    </div>

    <footer>
        <p class="main">Thank you for this journey to achieving greatness.</p>
        <p class="sub">Keep learning. Keep building. Keep rising.</p>
    </footer>

</body>
</html>
