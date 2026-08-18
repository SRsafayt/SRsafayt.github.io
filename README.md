
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cyber Security Architecture & Roadmap</title>
    <style>
        :root {
            --bg-color: #060b11;
            --card-bg: rgba(13, 25, 38, 0.7);
            --blue-team: #00d2ff;
            --red-team: #ff3366;
            --text-color: #e2e8f0;
            --border-glow-blue: rgba(0, 210, 255, 0.4);
            --border-glow-red: rgba(255, 51, 102, 0.4);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            background-image: 
                radial-gradient(circle at 50% 0%, rgba(0, 210, 255, 0.15), transparent 50%),
                radial-gradient(circle at 50% 100%, rgba(255, 51, 102, 0.15), transparent 50%);
            min-height: 100vh;
            padding: 40px 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 50px;
        }

        .header h1 {
            font-size: 2.8rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            background: linear-gradient(90deg, var(--blue-team), #ffffff, var(--red-team));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 20px rgba(0, 210, 255, 0.3);
        }

        .header p {
            color: #94a3b8;
            margin-top: 10px;
            font-size: 1.1rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        @media (max-width: 850px) {
            .container {
                grid-template-columns: 1fr;
            }
        }

        .team-sector {
            background: var(--card-bg);
            border-radius: 16px;
            padding: 30px;
            backdrop-filter: blur(10px);
            position: relative;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .blue-sector {
            border: 1px solid var(--border-glow-blue);
            box-shadow: 0 0 25px rgba(0, 210, 255, 0.1);
        }

        .blue-sector:hover {
            box-shadow: 0 0 35px rgba(0, 210, 255, 0.25);
            transform: translateY(-5px);
        }

        .red-sector {
            border: 1px solid var(--border-glow-red);
            box-shadow: 0 0 25px rgba(255, 51, 102, 0.1);
        }

        .red-sector:hover {
            box-shadow: 0 0 35px rgba(255, 51, 102, 0.25);
            transform: translateY(-5px);
        }

        .sector-title {
            text-align: center;
            font-size: 1.8rem;
            margin-bottom: 25px;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
        }

        .blue-sector .sector-title {
            color: var(--blue-team);
            border-bottom: 2px solid var(--blue-team);
            padding-bottom: 10px;
        }

        .red-sector .sector-title {
            color: var(--red-team);
            border-bottom: 2px solid var(--red-team);
            padding-bottom: 10px;
        }

        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
        }

        .card {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 10px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: all 0.3s ease;
        }

        .card:hover {
            background: rgba(255, 255, 255, 0.08);
            cursor: pointer;
        }

        .card h3 {
            font-size: 1.2rem;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .blue-sector .card h3 { color: #80e5ff; }
        .red-sector .card h3 { color: #ff80a0; }

        .card ul {
            list-style: none;
        }

        .card ul li {
            font-size: 0.95rem;
            color: #cbd5e1;
            margin-bottom: 8px;
            position: relative;
            padding-left: 18px;
        }

        .card ul li::before {
            content: "▹";
            position: absolute;
            left: 0;
        }

        .blue-sector .card ul li::before { color: var(--blue-team); }
        .red-sector .card ul li::before { color: var(--red-team); }

        .footer {
            text-align: center;
            margin-top: 60px;
            color: #64748b;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <div class="header">
        <h1>Cyber Security Architecture</h1>
        <p>Defensive vs Offensive Security Roadmap & Framework</p>
    </div>

    <div class="container">
        <!-- Blue Team Section -->
        <div class="team-sector blue-sector">
            <div class="sector-title">
                🛡️ Defensive Security (Blue Team)
            </div>
            
            <div class="category-grid">
                <div class="card">
                    <h3>🌐 Network Security</h3>
                    <ul>
                        <li>Firewalls</li>
                        <li>VPNs & Encryption</li>
                        <li>Intrusion Detection (IDS)</li>
                    </ul>
                </div>

                <div class="card">
                    <h3>🚨 Incident Response</h3>
                    <ul>
                        <li>Threat Hunting</li>
                        <li>Malware Analysis</li>
                        <li>Forensic Investigation</li>
                    </ul>
                </div>

                <div class="card">
                    <h3>📊 SIEM & Analytics</h3>
                    <ul>
                        <li>Splunk</li>
                        <li>ELK Stack</li>
                        <li>ArcSight Analysis</li>
                    </ul>
                </div>

                <div class="card">
                    <h3>🔐 Identity & Governance</h3>
                    <ul>
                        <li>Identity & Management</li>
                        <li>Cryptography</li>
                        <li>Security Design Patterns</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Red Team Section -->
        <div class="team-sector red-sector">
            <div class="sector-title">
                🎯 Offensive Security (Red Team)
            </div>

            <div class="category-grid">
                <div class="card">
                    <h3>⚔️ Red Teaming</h3>
                    <ul>
                        <li>Penetration Testing</li>
                        <li>Social Engineering</li>
                        <li>Exploit Development</li>
                    </ul>
                </div>

                <div class="card">
                    <h3>🛠️ Penetration Tools</h3>
                    <ul>
                        <li>Kali Linux</li>
                        <li>Metasploit Framework</li>
                        <li>Nmap Network Scanner</li>
                        <li>Burp Suite</li>
                    </ul>
                </div>

                <div class="card">
                    <h3>🔍 Vulnerability Mgmt</h3>
                    <ul>
                        <li>Nessus Vulnerability Scanner</li>
                        <li>OpenVAS</li>
                        <li>Qualys Guard</li>
                    </ul>
                </div>

                <div class="card">
                    <h3>📋 Governance & Risk (GRC)</h3>
                    <ul>
                        <li>Risk Management</li>
                        <li>Compliance (GDPR, ISO)</li>
                        <li>Policy & Audit</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <div class="footer">
        <p>Created for Cyber Security Learning & Portfolio | Hosted on GitHub Pages</p>
    </div>

    <script>
        // Interactive Click Effect on Cards
        document.querySelectorAll('.card').forEach(card => {
            card.addEventListener('click', () => {
                const title = card.querySelector('h3').innerText;
                console.log(`Clicked on: ${title}`);
            });
        });
    </script>
</body>
</html>
