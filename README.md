<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FDI and Economic Growth in Algeria</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            width: 100%;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 60px 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }

        .container::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(102, 126, 234, 0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .content {
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 3.5em;
            font-weight: 800;
            text-align: center;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInDown 1s ease-out;
            line-height: 1.2;
        }

        .subtitle {
            font-size: 1.5em;
            text-align: center;
            color: #555;
            margin-bottom: 30px;
            font-weight: 300;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .badges {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 40px;
            animation: fadeIn 1s ease-out 0.4s both;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            padding: 8px 16px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 20px;
            font-size: 0.9em;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
        }

        .badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(102, 126, 234, 0.5);
        }

        .tagline {
            text-align: center;
            font-size: 1.1em;
            color: #666;
            font-style: italic;
            margin-bottom: 40px;
            animation: fadeIn 1s ease-out 0.6s both;
        }

        .quick-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            animation: fadeInUp 1s ease-out 0.8s both;
        }

        .quick-link {
            padding: 12px 30px;
            background: white;
            border: 2px solid #667eea;
            color: #667eea;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .quick-link:hover {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .divider {
            height: 2px;
            background: linear-gradient(90deg, transparent, #667eea, transparent);
            margin: 50px 0;
            animation: fadeIn 1s ease-out 1s both;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 40px;
            animation: fadeIn 1s ease-out 1.2s both;
        }

        .stat-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            color: white;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .stat-card:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: 800;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 0.9em;
            opacity: 0.9;
        }

        /* README Content Styles */
        .readme-content {
            margin-top: 60px;
            padding-top: 40px;
            border-top: 3px solid #667eea;
        }

        .readme-content h2 {
            color: #667eea;
            font-size: 2em;
            margin-top: 40px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .readme-content h3 {
            color: #764ba2;
            font-size: 1.5em;
            margin-top: 30px;
            margin-bottom: 15px;
        }

        .readme-content p {
            line-height: 1.8;
            color: #333;
            margin-bottom: 15px;
        }

        .readme-content table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .readme-content th {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px;
            text-align: left;
            font-weight: 600;
        }

        .readme-content td {
            padding: 12px 15px;
            border-bottom: 1px solid #f0f0f0;
        }

        .readme-content tr:last-child td {
            border-bottom: none;
        }

        .readme-content code {
            background: #f5f5f5;
            padding: 2px 6px;
            border-radius: 4px;
            font-family: 'Courier New', monospace;
            color: #667eea;
        }

        .readme-content blockquote {
            border-left: 4px solid #667eea;
            padding-left: 20px;
            margin: 20px 0;
            color: #555;
            font-style: italic;
        }

        .readme-content ul, .readme-content ol {
            margin-left: 30px;
            margin-bottom: 15px;
        }

        .readme-content li {
            margin-bottom: 8px;
            line-height: 1.6;
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2.5em;
            }
            .subtitle {
                font-size: 1.2em;
            }
            .container {
                padding: 40px 25px;
            }
            .stat-number {
                font-size: 2em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="content">
            <!-- Interactive Title Section -->
            <h1>🌍 Foreign Direct Investment and Economic Growth in Algeria</h1>
            
            <div class="subtitle">
                📊 An ARDL Bounds Testing Approach (1990–2023)
            </div>

            <div class="badges">
                <span class="badge">🐍 Python 3.8+</span>
                <span class="badge">📓 Jupyter Notebook</span>
                <span class="badge">📜 MIT License</span>
                <span class="badge">✅ Complete</span>
            </div>

            <div class="tagline">
                An econometric investigation of FDI-growth dynamics in Algeria's hydrocarbon-dependent economy
            </div>

            <div class="quick-links">
                <a href="#results" class="quick-link">
                    <span>📊</span> View Results
                </a>
                <a href="#quickstart" class="quick-link">
                    <span>🚀</span> Quick Start
                </a>
                <a href="#methodology" class="quick-link">
                    <span>📖</span> Documentation
                </a>
                <a href="#author" class="quick-link">
                    <span>👤</span> Author
                </a>
            </div>

            <div class="divider"></div>

            <div class="stats">
                <div class="stat-card">
                    <div class="stat-number">34</div>
                    <div class="stat-label">Years of Data</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">7</div>
                    <div class="stat-label">Variables Analyzed</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">ARDL</div>
                    <div class="stat-label">Methodology</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">1990-2023</div>
                    <div class="stat-label">Study Period</div>
                </div>
            </div>

            <!-- README Content -->
            <div class="readme-content">
                <h2>📑 Table of Contents</h2>
                <ul>
                    <li><a href="#project-overview">📌 Project Overview</a></li>
                    <li><a href="#research-objectives">🎯 Research Objectives</a></li>
                    <li><a href="#methodological-framework">🧠 Methodological Framework</a></li>
                    <li><a href="#data-description">📊 Data Description</a></li>
                    <li><a href="#econometric-procedure">🧪 Econometric Procedure</a></li>
                    <li><a href="#key-findings">📈 Key Findings</a></li>
                    <li><a href="#quick-start">🚀 Quick Start</a></li>
                    <li><a href="#technologies-used">🛠️ Technologies Used</a></li>
                    <li><a href="#references">📚 References</a></li>
                    <li><a href="#author">👤 Author</a></li>
                    <li><a href="#license">📜 License</a></li>
                </ul>

                <div class="divider"></div>

                <h2 id="project-overview">📌 Project Overview</h2>
                
                <table>
                    <tr>
                        <td width="50%">
                            <h3>🎓 Academic Context</h3>
                            <p>Master's thesis project investigating the empirical relationship between FDI and economic growth in Algeria using advanced time series econometrics.</p>
                        </td>
                        <td width="50%">
                            <h3>🔬 Methodological Approach</h3>
                            <p>ARDL Bounds Testing framework enabling robust analysis of both short-run dynamics and long-run equilibrium relationships.</p>
                        </td>
                    </tr>
                </table>

                <p>This repository contains the <strong>complete empirical implementation</strong> of an econometric study examining the relationship between <strong>Foreign Direct Investment (FDI)</strong> and <strong>economic growth</strong> in Algeria using the <strong>Autoregressive Distributed Lag (ARDL) Bounds Testing</strong> framework.</p>

                <p>The analysis investigates both <strong>short-run dynamics</strong> and <strong>long-run equilibrium relationships</strong> between FDI and GDP while accounting for key macroeconomic variables such as oil prices, trade openness, inflation, and gross capital formation.</p>

                <blockquote>
                    💡 <strong>Context:</strong> The project is conducted in the context of Algeria's structural dependence on hydrocarbons and recurring exposure to external shocks, including the <strong>COVID-19 pandemic</strong>, which is explicitly modeled using a dummy variable.
                </blockquote>

                <div class="divider"></div>

                <h2 id="research-objectives">🎯 Research Objectives</h2>

                <p>The study seeks to answer the following questions:</p>

                <table>
                    <thead>
                        <tr>
                            <th width="5%">#</th>
                            <th>Research Question</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1️⃣</td>
                            <td>Does FDI exert a <strong>long-run cointegrated effect</strong> on Algeria's economic growth?</td>
                        </tr>
                        <tr>
                            <td>2️⃣</td>
                            <td>Are there <strong>short-run dynamic effects</strong> of FDI on GDP?</td>
                        </tr>
                        <tr>
                            <td>3️⃣</td>
                            <td>How do <strong>oil prices</strong>, <strong>trade openness</strong>, and <strong>macroeconomic stability</strong> influence growth?</td>
                        </tr>
                        <tr>
                            <td>4️⃣</td>
                            <td>Has the relationship between FDI and GDP remained <strong>stable over time</strong>?</td>
                        </tr>
                    </tbody>
                </table>

                <div class="divider"></div>

                <h2 id="methodological-framework">🧠 Methodological Framework</h2>

                <h3>Why ARDL?</h3>

                <table>
                    <thead>
                        <tr>
                            <th>✨ Advantage</th>
                            <th>📝 Description</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>🔄 <strong>Mixed Integration</strong></td>
                            <td>Accommodates variables integrated of order <strong>I(0)</strong> and <strong>I(1)</strong></td>
                        </tr>
                        <tr>
                            <td>📊 <strong>Small Sample Performance</strong></td>
                            <td>Performs well with <strong>limited observations</strong></td>
                        </tr>
                        <tr>
                            <td>⚡ <strong>Simultaneous Estimation</strong></td>
                            <td>Captures both short-run dynamics and long-run relationships</td>
                        </tr>
                        <tr>
                            <td>🎯 <strong>Spurious Regression Avoidance</strong></td>
                            <td>Robust specification when properly implemented</td>
                        </tr>
                    </tbody>
                </table>

                <blockquote>
                    ⚠️ <strong>Important:</strong> No variable integrated of order I(2) is included, ensuring full compliance with ARDL assumptions.
                </blockquote>

                <div class="divider"></div>

                <h2 id="data-description">📊 Data Description</h2>

                <h3>📅 Dataset Overview</h3>

                <table>
                    <thead>
                        <tr>
                            <th>Attribute</th>
                            <th>Details</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>🌍 <strong>Country</strong></td>
                            <td>Algeria</td>
                        </tr>
                        <tr>
                            <td>📆 <strong>Period</strong></td>
                            <td>1990–2023 (34 years)</td>
                        </tr>
                        <tr>
                            <td>📈 <strong>Frequency</strong></td>
                            <td>Annual</td>
                        </tr>
                        <tr>
                            <td>🗂️ <strong>Observations</strong></td>
                            <td>34</td>
                        </tr>
                    </tbody>
                </table>

                <h3>🔢 Variables Used</h3>

                <table>
                    <thead>
                        <tr>
                            <th>Variable</th>
                            <th>Description</th>
                            <th>Source</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><code>log(Real GDP)</code></td>
                            <td>🏭 Measure of economic growth</td>
                            <td>World Bank WDI</td>
                        </tr>
                        <tr>
                            <td><code>FDI (% of GDP)</code></td>
                            <td>💰 Foreign direct investment inflows</td>
                            <td>World Bank WDI</td>
                        </tr>
                        <tr>
                            <td><code>Inflation</code></td>
                            <td>📊 CPI inflation rate</td>
                            <td>World Bank WDI</td>
                        </tr>
                        <tr>
                            <td><code>GCF (% of GDP)</code></td>
                            <td>🏗️ Gross capital formation</td>
                            <td>World Bank WDI</td>
                        </tr>
                        <tr>
                            <td><code>Trade Openness</code></td>
                            <td>🌐 (Exports + Imports) / GDP</td>
                            <td>World Bank WDI</td>
                        </tr>
                        <tr>
                            <td><code>log(Oil Price)</code></td>
                            <td>🛢️ International crude oil price</td>
                            <td>FRED (POILBREUSD)</td>
                        </tr>
                        <tr>
                            <td><code>D2020</code></td>
                            <td>🦠 COVID-19 dummy variable</td>
                            <td>Constructed</td>
                        </tr>
                    </tbody>
                </table>

                <p><strong>📚 Data Sources:</strong> <a href="https://databank.worldbank.org/">World Bank WDI</a> • <a href="https://www.macrotrends.net/">Macrotrends</a> • <a href="https://fred.stlouisfed.org/">FRED</a></p>

                <div class="divider"></div>

                <h2 id="key-findings">📈 Key Findings</h2>

                <h3>🎯 Summary of Results</h3>

                <table>
                    <tr>
                        <td width="50%" valign="top">
                            <h3>🔹 Long-Run Relationship</h3>
                            <p style="color: #cf222e; font-weight: bold;">❌ No Evidence of Cointegration</p>
                            <p><strong>Key Finding:</strong></p>
                            <ul>
                                <li>FDI does <strong>not</strong> drive sustained long-run growth in Algeria (1990–2023)</li>
                                <li>F-statistic below critical bounds</li>
                                <li>No long-run equilibrium relationship detected</li>
                            </ul>
                            <p><strong>Interpretation:</strong> Algeria's FDI has failed to create lasting productive capacity or technological spillovers necessary for sustained economic expansion.</p>
                        </td>
                        <td width="50%" valign="top">
                            <h3>🔹 Short-Run Dynamics</h3>
                            <p style="color: #bf8700; font-weight: bold;">⚠️ Weak and Unstable Effects</p>
                            <p><strong>Key Findings:</strong></p>
                            <ul>
                                <li>❌ FDI effects: <strong>weak, unstable</strong>, marginally significant</li>
                                <li>✅ <strong>Oil prices</strong>: strong positive effect (delayed)</li>
                                <li>⚠️ <strong>Trade openness</strong>: negative lagged effects</li>
                                <li>🦠 <strong>COVID-19</strong>: significant GDP contraction</li>
                            </ul>
                            <p><strong>Interpretation:</strong> Short-term FDI contributions are negligible compared to oil price movements.</p>
                        </td>
                    </tr>
                </table>

                <h3>🏛️ Structural Insights</h3>

                <table>
                    <thead>
                        <tr>
                            <th>🎯 Characteristic</th>
                            <th>📊 Finding</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>🛢️ <strong>Hydrocarbon Dependence</strong></td>
                            <td>Economy remains highly dependent on oil revenues</td>
                        </tr>
                        <tr>
                            <td>💥 <strong>External Vulnerability</strong></td>
                            <td>Significant exposure to external shocks</td>
                        </tr>
                        <tr>
                            <td>🔄 <strong>FDI Absorption Capacity</strong></td>
                            <td>Limited ability to transform FDI into durable growth</td>
                        </tr>
                        <tr>
                            <td>🏗️ <strong>Structural Reforms</strong></td>
                            <td>Need for economic diversification and institutional improvements</td>
                        </tr>
                    </tbody>
                </table>

                <blockquote>
                    💡 <strong>Policy Implication:</strong> Algeria must address structural barriers and improve the business environment to better leverage FDI for sustainable growth.
                </blockquote>

                <div class="divider"></div>

                <h2 id="quick-start">🚀 Quick Start</h2>

                <h3>Prerequisites</h3>
                <ul>
                    <li>Python 3.8 or higher</li>
                    <li>Git</li>
                </ul>

                <div class="divider"></div>

                <h2 id="technologies-used">🛠️ Technologies Used</h2>

                <h3>Core Stack</h3>
                <p>
                    <span class="badge">Python</span>
                    <span class="badge">Jupyter</span>
                    <span class="badge">NumPy</span>
                    <span class="badge">Pandas</span>
                </p>

                <h3>Econometric & Statistical</h3>
                <table>
                    <thead>
                        <tr>
                            <th>Package</th>
                            <th>Purpose</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><code>statsmodels</code></td>
                            <td>📊 Econometric modeling (ARDL, ADF, diagnostics)</td>
                        </tr>
                        <tr>
                            <td><code>arch</code></td>
                            <td>📈 ARCH/GARCH models</td>
                        </tr>
                        <tr>
                            <td><code>scipy</code></td>
                            <td>🔬 Statistical tests</td>
                        </tr>
                    </tbody>
                </table>

                <h3>Visualization</h3>
                <table>
                    <thead>
                        <tr>
                            <th>Package</th>
                            <th>Purpose</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><code>matplotlib</code></td>
                            <td>📊 Static plots and charts</td>
                        </tr>
                        <tr>
                            <td><code>seaborn</code></td>
                            <td>🎨 Statistical data visualization</td>
                        </tr>
                        <tr>
                            <td><code>plotly</code></td>
                            <td>📈 Interactive visualizations</td>
                        </tr>
                    </tbody>
                </table>

                <div class="divider"></div>

                <h2 id="references">📚 References</h2>

                <ol>
                    <li><strong>Pesaran, M. H., Shin, Y., & Smith, R. J.</strong> (2001). <em>Bounds testing approaches to the analysis of level relationships</em>. Journal of Applied Econometrics, 16(3), 289-326.</li>
                    <li><strong>Dickey, D. A., & Fuller, W. A.</strong> (1979). <em>Distribution of the estimators for autoregressive time series with a unit root</em>. Journal of the American Statistical Association, 74(366a), 427-431.</li>
                    <li><strong>Gujarati, D. N., & Porter, D. C.</strong> (2009). <em>Basic Econometrics</em> (5th ed.). McGraw-Hill Education.</li>
                    <li><strong>Louail, B., Benanaya, D., & Bakdi, A.</strong> (2017). Foreign Direct Investment and Economic Growth in Algeria. <em>International Journal of Economics and Finance</em>, 9(4).</li>
                    <li><strong>World Bank</strong> – World Development Indicators (WDI)</li>
                </ol>

                <div class="divider"></div>

                <h2 id="author">👤 Author</h2>

                <div style="text-align: center;">
                    <h3><strong>Amrani Bouabdellah</strong></h3>
                    <p>Master's Student – Statistics & Data Science<br>
                    📍 ENSSEA (École Nationale Supérieure de Statistique et d'Économie Appliquée)<br>
                    📍 Algiers, Algeria</p>
                    <p>
                        <a href="mailto:abdouugk@gmail.com" class="badge">📧 Email</a>
                        <a href="https://github.com/amrani-213" class="badge">💻 GitHub</a>
                    </p>
                </div>

                <div class="divider"></div>

                <h2 id="license">📜 License</h2>

                <p style="text-align: center;">
                    This project is licensed under the <strong>MIT License</strong><br>
                    See the LICENSE file for details
                </p>

                <div class="divider"></div>

                <h2>🙏 Acknowledgments</h2>

                <p style="text-align: center;">
                    Special thanks to:<br><br>
                    🌍 <strong>World Bank</strong> for open data availability<br>
                    💻 <strong>Open-source community</strong> for econometric tools<br>
                    📚 <strong>Research community</strong> for methodological foundations
                </p>

                <div class="divider"></div>

                <div style="text-align: center; margin-top: 60px;">
                    <h3>⭐ <strong>Star this repository if you find it useful!</strong></h3>
                    <p><a href="#" class="quick-link">⬆ Back to Top</a></p>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
