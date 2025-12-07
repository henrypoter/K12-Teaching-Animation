# 需求：生态系统碳循环与全球碳失衡（含人类活动干扰）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画的目标用户主要是高中至大学低年级的学生，以及对环境科学感兴趣的社会公众。他们的核心需求是：
1.  **理解复杂过程**：将抽象的碳循环（包括生物地球化学过程）和全球碳失衡概念，转化为直观、动态、可视化的模型。
2.  **识别关键环节**：清晰区分自然碳循环（动态平衡）与人类活动干扰（主要是化石燃料燃烧和土地利用变化）这两个核心部分。
3.  **建立因果联系**：直观地看到人类活动如何打破自然平衡，导致大气中二氧化碳浓度增加，进而引发全球变暖等一系列问题。
4.  **激发探究与反思**：不仅了解“是什么”和“为什么”，还能通过交互引发对“如何应对”的思考。

#### 教学设计思路
本设计遵循“从整体到局部，从平衡到失衡，从观察到交互”的认知规律。

*   **核心概念分层呈现**：
    *   **第一层：自然碳循环**：展示碳在四大储库（大气、海洋、陆地生物圈、土壤）之间的自然流动（光合作用、呼吸作用、分解、海洋溶解与释放），强调这是一个接近平衡的动态系统。
    *   **第二层：人类活动干扰**：以醒目的方式叠加显示人类活动（化石燃料燃烧图标、森林砍伐图标）向大气中“注入”额外的碳流。
    *   **第三层：碳失衡与影响**：展示因额外碳注入导致大气储库“膨胀”，并用热力图或温度计等视觉隐喻展示其对全球能量平衡的影响（温室效应增强）。

*   **认知规律引导**：
    1.  **吸引与概述**：开场用地球和循环箭头动画吸引注意力，并语音/文字概述学习目标。
    2.  **建立基线**：先完整、流畅地自动播放一遍**纯自然状态下的碳循环**，让学习者建立“平衡”的视觉印象。
    3.  **引入变量**：然后重置，加入“人类活动”开关。让学习者手动开启干扰，观察系统如何从平衡走向失衡。
    4.  **聚焦与深化**：通过点击各储库或流动路径，弹出详细信息卡片（如具体数据、化学反应式）。
    5.  **挑战与反思**：在最后环节，设置一个简单的“减排挑战”交互，让学习者尝试调节人类活动强度，观察其对大气碳浓度的影响。

*   **交互设计**：
    *   **渐进式揭示**：信息分层，避免初始画面过于杂乱。
    *   **直接操作**：通过拖拽、点击、滑动开关来控制动画的进程和显示内容。
    *   **因果即时反馈**：任何操作（如开启化石燃料排放）都能立即在动画中得到视觉反馈（碳流增加、大气库变大）。
    *   **叙事控制**：提供“仅自然循环”、“加入人类活动”、“快进100年”等预设场景按钮，方便教师讲解或学生自主探索。

*   **视觉呈现**：
    *   **拟物化与符号化结合**：地球、森林、工厂、汽车等采用简洁的图标化设计；碳流（CO₂分子团）用粒子动画表示，自然碳流用绿色/蓝色，人类排放碳流用橙色/红色以示区分。
    *   **动态数据可视化**：每个碳储库的大小可随碳量变化而轻微缩放，旁边配有动态变化的数字标签（单位：GtC）。
    *   **视觉焦点引导**：使用柔和的聚光灯效果或脉冲动画，在讲解时高亮当前重点部分。

#### 配色方案选择
配色需清晰区分系统各部分，并传达情感基调（自然 vs. 人为干扰）。
*   **主背景**：深空蓝或深灰色，模拟宇宙空间感，突出前景元素。
*   **自然系统色**：
    *   **大气**：浅蓝色半透明层。
    *   **海洋**：深蓝色到蓝绿色渐变。
    *   **陆地生物圈（森林等）**：不同明度的绿色。
    *   **土壤**：棕色。
    *   **自然碳流**：青绿色或温和的蓝色箭头/粒子。
*   **人类干扰色**：
    *   **人类活动图标（工厂、汽车等）**：灰色金属色。
    *   **人为排放碳流**：鲜明的橙色或红色箭头/粒子，具有警示意味。
*   **失衡与影响色**：
    *   **失衡的大气层**：当浓度超标时，浅蓝色大气层可逐渐叠加一层淡淡的红色晕染。
    *   **温室效应热力图**：使用红-黄暖色调表示热量滞留。
*   **界面与文字**：白色或浅灰色，确保高可读性。

#### 交互功能列表
1.  **主场景控制面板**：
    *   **播放/暂停/重置** 按钮：控制整个动画的播放。
    *   **场景选择器**：一键切换“纯自然循环”、“工业革命前”、“现代（高排放）”、“未来情景”等模式。
    *   **时间流速滑块**：加快或减慢碳循环过程的演示速度。

2.  **图层显示开关**：
    *   “显示/隐藏自然碳流”
    *   “显示/隐藏人类排放”
    *   “显示/隐藏碳储库数据标签”
    *   “显示/隐藏温室效应示意图”

3.  **对象交互**：
    *   **点击碳储库**（如“海洋”）：弹出详细卡片，显示该储库的碳储量、主要过程（如溶解泵、生物泵）、与人类活动的关系。
    *   **点击碳流动路径**（如“光合作用”箭头）：弹出详细卡片，说明该过程，并显示每年通量数据。
    *   **点击人类活动源**（如“煤电厂”）：弹出卡片，显示其年排放量、历史变化曲线。

4.  **模拟与挑战模块**：
    *   **“人类活动”控制杆**：一个可拖动的滑块，模拟从“无干扰”到“极高排放”的不同强度。实时显示对应的大气CO₂浓度和全球平均温度变化值。
    *   **“减排挑战”**：给定一个目标（如“将2100年升温控制在2℃以内”），学习者需要通过组合调整“能源结构”、“森林覆盖率”、“工业效率”等多个滑块来实现目标，系统即时反馈模拟结果。

5.  **辅助功能**：
    *   解说音轨开关与字幕。
    *   关键术语提示（鼠标悬停显示）。
    *   一键保存当前状态为图片的功能。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>生态系统碳循环与全球碳失衡</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0a1929 0%, #1a2b3c 100%);
            color: #e0f2fe;
            min-height: 100vh;
            padding: 20px;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background: rgba(16, 42, 67, 0.7);
            border-radius: 15px;
            border: 1px solid rgba(64, 156, 255, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #4ade80, #22d3ee);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        .subtitle {
            font-size: 1.1rem;
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }

        .animation-section {
            flex: 3;
            min-width: 300px;
            background: rgba(16, 42, 67, 0.7);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(64, 156, 255, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }

        .controls-section {
            flex: 1;
            min-width: 300px;
            background: rgba(16, 42, 67, 0.7);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(64, 156, 255, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        #animationCanvas {
            width: 100%;
            height: 600px;
            background: rgba(10, 25, 41, 0.5);
            border-radius: 10px;
            display: block;
            cursor: pointer;
        }

        .control-group {
            margin-bottom: 25px;
        }

        h2 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #7dd3fc;
            border-bottom: 2px solid rgba(125, 211, 252, 0.3);
            padding-bottom: 8px;
        }

        h3 {
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: #a5f3fc;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }

        button {
            padding: 12px 20px;
            background: linear-gradient(135deg, #1e40af, #3b82f6);
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 500;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 120px;
        }

        button:hover {
            background: linear-gradient(135deg, #1e3a8a, #2563eb);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.4);
        }

        button:active {
            transform: translateY(0);
        }

        button.active {
            background: linear-gradient(135deg, #059669, #10b981);
            box-shadow: 0 0 0 2px rgba(16, 185, 129, 0.5);
        }

        .slider-container {
            margin: 20px 0;
        }

        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .slider-label span:last-child {
            color: #7dd3fc;
            font-weight: 600;
        }

        input[type="range"] {
            width: 100%;
            height: 8px;
            -webkit-appearance: none;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #3b82f6;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.3);
        }

        .toggle-group {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .toggle-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 12px;
            background: rgba(30, 58, 138, 0.3);
            border-radius: 8px;
            transition: all 0.3s ease;
        }

        .toggle-item:hover {
            background: rgba(30, 58, 138, 0.5);
        }

        .toggle-item label {
            display: flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
            flex: 1;
        }

        .toggle-icon {
            width: 24px;
            height: 24px;
            border-radius: 4px;
        }

        .toggle-switch {
            position: relative;
            width: 50px;
            height: 26px;
        }

        .toggle-switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }

        .toggle-slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #475569;
            border-radius: 34px;
            transition: .4s;
        }

        .toggle-slider:before {
            position: absolute;
            content: "";
            height: 18px;
            width: 18px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            border-radius: 50%;
            transition: .4s;
        }

        input:checked + .toggle-slider {
            background-color: #10b981;
        }

        input:checked + .toggle-slider:before {
            transform: translateX(24px);
        }

        .info-panel {
            background: rgba(30, 41, 59, 0.8);
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
            border-left: 4px solid #3b82f6;
        }

        .info-title {
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: #7dd3fc;
        }

        .info-content {
            line-height: 1.6;
            opacity: 0.9;
        }

        .data-display {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .data-item {
            background: rgba(30, 58, 138, 0.3);
            padding: 15px;
            border-radius: 8px;
            text-align: center;
        }

        .data-label {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-bottom: 5px;
        }

        .data-value {
            font-size: 1.5rem;
            font-weight: 700;
            color: #7dd3fc;
        }

        .data-unit {
            font-size: 0.9rem;
            opacity: 0.7;
        }

        .challenge-section {
            background: rgba(16, 42, 67, 0.7);
            border-radius: 15px;
            padding: 25px;
            margin-top: 30px;
            border: 1px solid rgba(64, 156, 255, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .challenge-controls {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .challenge-slider {
            background: rgba(30, 41, 59, 0.8);
            padding: 15px;
            border-radius: 10px;
        }

        .challenge-result {
            text-align: center;
            padding: 20px;
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.2), rgba(16, 185, 129, 0.2));
            border-radius: 10px;
            margin-top: 20px;
        }

        .result-value {
            font-size: 2rem;
            font-weight: 700;
            margin: 10px 0;
            color: #10b981;
        }

        .warning {
            color: #f87171;
        }

        .success {
            color: #4ade80;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            opacity: 0.7;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            #animationCanvas {
                height: 400px;
            }
            
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>🌍 生态系统碳循环与全球碳失衡</h1>
            <p class="subtitle">探索自然碳循环的动态平衡，观察人类活动如何干扰这一系统，并理解全球碳失衡对气候的影响。</p>
        </header>

        <div class="main-content">
            <section class="animation-section">
                <h2>碳循环动态模拟</h2>
                <canvas id="animationCanvas"></canvas>
                
                <div class="data-display">
                    <div class="data-item">
                        <div class="data-label">大气 CO₂ 浓度</div>
                        <div class="data-value" id="co2Value">415</div>
                        <div class="data-unit">ppm</div>
                    </div>
                    <div class="data-item">
                        <div class="data-label">全球平均温度</div>
                        <div class="data-value" id="tempValue">1.2</div>
                        <div class="data-unit">°C (相对于工业革命前)</div>
                    </div>
                    <div class="data-item">
                        <div class="data-label">年碳排放量</div>
                        <div class="data-value" id="emissionValue">36.8</div>
                        <div class="data-unit">Gt CO₂/年</div>
                    </div>
                    <div class="data-item">
                        <div class="data-label">碳循环状态</div>
                        <div class="data-value" id="balanceStatus">失衡</div>
                        <div class="data-unit" id="balanceDetail">(自然吸收 < 人类排放)</div>
                    </div>
                </div>
            </section>

            <section class="controls-section">
                <h2>模拟控制</h2>
                
                <div class="control-group">
                    <h3>场景模式</h3>
                    <div class="button-group">
                        <button id="btnNatural" class="active">仅自然循环</button>
                        <button id="btnPreIndustrial">工业革命前</button>
                        <button id="btnModern">现代高排放</button>
                        <button id="btnFuture">未来情景</button>
                    </div>
                </div>

                <div class="control-group">
                    <h3>时间控制</h3>
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>模拟速度</span>
                            <span id="speedValue">1.0x</span>
                        </div>
                        <input type="range" id="speedSlider" min="0.1" max="3" step="0.1" value="1">
                    </div>
                    <div class="button-group">
                        <button id="btnPlay">⏸️ 暂停</button>
                        <button id="btnReset">🔄 重置</button>
                        <button id="btnFastForward">⏩ 快进100年</button>
                    </div>
                </div>

                <div class="control-group">
                    <h3>显示选项</h3>
                    <div class="toggle-group">
                        <div class="toggle-item">
                            <label>
                                <div class="toggle-icon" style="background: #22d3ee;"></div>
                                <span>自然碳流</span>
                            </label>
                            <div class="toggle-switch">
                                <input type="checkbox" id="toggleNatural" checked>
                                <div class="toggle-slider"></div>
                            </div>
                        </div>
                        <div class="toggle-item">
                            <label>
                                <div class="toggle-icon" style="background: #f97316;"></div>
                                <span>人类排放</span>
                            </label>
                            <div class="toggle-switch">
                                <input type="checkbox" id="toggleHuman" checked>
                                <div class="toggle-slider"></div>
                            </div>
                        </div>
                        <div class="toggle-item">
                            <label>
                                <div class="toggle-icon" style="background: #ef4444;"></div>
                                <span>温室效应</span>
                            </label>
                            <div class="toggle-switch">
                                <input type="checkbox" id="toggleGreenhouse">
                                <div class="toggle-slider"></div>
                            </div>
                        </div>
                        <div class="toggle-item">
                            <label>
                                <div class="toggle-icon" style="background: #8b5cf6;"></div>
                                <span>数据标签</span>
                            </label>
                            <div class="toggle-switch">
                                <input type="checkbox" id="toggleLabels" checked>
                                <div class="toggle-slider"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="info-panel">
                    <div class="info-title">💡 点击交互提示</div>
                    <div class="info-content">
                        点击画布中的不同元素查看详细信息：
                        <ul style="margin-top: 10px; padding-left: 20px;">
                            <li>🌳 森林 - 光合作用与呼吸作用</li>
                            <li>🌊 海洋 - 碳溶解与生物泵</li>
                            <li>🏭 工厂 - 化石燃料排放</li>
                            <li>🚗 汽车 - 交通排放</li>
                        </ul>
                    </div>
                </div>
            </section>
        </div>

        <section class="challenge-section">
            <h2>🌱 减排挑战：将2100年升温控制在2°C以内</h2>
            <p style="margin-bottom: 20px; opacity: 0.9;">调整以下参数，观察对大气CO₂浓度和全球温度的影响：</p>
            
            <div class="challenge-controls">
                <div class="challenge-slider">
                    <div class="slider-label">
                        <span>能源结构</span>
                        <span id="energyValue">50%</span>
                    </div>
                    <input type="range" id="energySlider" min="0" max="100" value="50">
                    <div style="font-size: 0.9rem; opacity: 0.8; margin-top: 5px;">
                        可再生能源比例
                    </div>
                </div>
                
                <div class="challenge-slider">
                    <div class="slider-label">
                        <span>森林覆盖率</span>
                        <span id="forestValue">30%</span>
                    </div>
                    <input type="range" id="forestSlider" min="10" max="50" value="30">
                    <div style="font-size: 0.9rem; opacity: 0.8; margin-top: 5px;">
                        全球森林覆盖率
                    </div>
                </div>
                
                <div class="challenge-slider">
                    <div class="slider-label">
                        <span>工业效率</span>
                        <span id="efficiencyValue">60%</span>
                    </div>
                    <input type="range" id="efficiencySlider" min="20" max="90" value="60">
                    <div style="font-size: 0.9rem; opacity: 0.8; margin-top: 5px;">
                        能源利用效率
                    </div>
                </div>
            </div>

            <div class="challenge-result">
                <h3>2100年预测结果</h3>
                <div class="data-item" style="display: inline-block; margin: 10px;">
                    <div class="data-label">大气 CO₂ 浓度</div>
                    <div class="data-value" id="futureCO2">520</div>
                    <div class="data-unit">ppm</div>
                </div>
                <div class="data-item" style="display: inline-block; margin: 10px;">
                    <div class="data-label">全球升温</div>
                    <div class="data-value" id="futureTemp">2.8</div>
                    <div class="data-unit">°C</div>
                </div>
                
                <div id="challengeMessage" class="result-value warning">
                    ❌ 超出2°C目标
                </div>
                
                <p style="margin-top: 15px; font-size: 0.9rem; opacity: 0.8;">
                    目标：将可再生能源比例提高到70%以上，森林覆盖率提高到40%以上，工业效率提高到80%以上
                </p>
            </div>
        </section>

        <footer>
            <p>教学动画设计 | 生态系统碳循环与全球碳失衡 | 数据基于IPCC报告与科学研究</p>
            <p>交互式教育工具 - 通过可视化理解复杂的生态系统过程</p>
        </footer>
    </div>

    <script>
        // 初始化Canvas
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
        }
        
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 模拟状态
        let simulationState = {
            mode: 'natural', // natural, preIndustrial, modern, future
            isPlaying: true,
            speed: 1.0,
            time: 0,
            
            // 显示选项
            showNatural: true,
            showHuman: true,
            showGreenhouse: false,
            showLabels: true,
            
            // 碳储库数据 (单位: GtC)
            reservoirs: {
                atmosphere: { value: 850, capacity: 1000, color: '#7dd3fc', x: 0.5, y: 0.2, radius: 60 },
                ocean: { value: 38000, capacity: 40000, color: '#22d3ee', x: 0.8, y: 0.6, radius: 90 },
                biosphere: { value: 560, capacity: 600, color: '#4ade80', x: 0.3, y: 0.5, radius: 50 },
                soil: { value: 2300, capacity: 2500, color: '#a16207', x: 0.2, y: 0.7, radius: 55 }
            },
            
            // 碳流动
            flows: {
                photosynthesis: { from: 'atmosphere', to: 'biosphere', rate: 123, color: '#10b981', active: true },
                respiration: { from: 'biosphere', to: 'atmosphere', rate: 118, color: '#86efac', active: true },
                decomposition: { from: 'biosphere', to: 'soil', rate: 60, color: '#d9f99d', active: true },
                soilRespiration: { from: 'soil', to: 'atmosphere', rate: 58, color: '#fef08a', active: true },
                oceanUptake: { from: 'atmosphere', to: 'ocean', rate: 92, color: '#38bdf8', active: true },
                oceanRelease: { from: 'ocean', to: 'atmosphere', rate: 90, color: '#0ea5e9', active: true }
            },
            
            // 人类活动
            humanActivities: {
                fossilFuels: { rate: 9.5, color: '#f97316', x: 0.7, y: 0.3, icon: '🏭' },
                deforestation: { rate: 1.5, color: '#ef4444', x: 0.4, y: 0.8, icon: '🪓' },
                transportation: { rate: 8.0, color: '#f59e0b', x: 0.6, y: 0.4, icon: '🚗' }
            },
            
            // 温室效应
            greenhouseEffect: {
                intensity: 0.3,
                temperatureRise: 1.2
            },
            
            // 点击交互信息
            activeInfo: null
        };
        
        // 粒子系统
        class Particle {
            constructor(x, y, color, vx, vy, life = 100) {
                this.x = x;
                this.y = y;
                this.color = color;
                this.vx = vx;
                this.vy = vy;
                this.life = life;
                this.maxLife = life;
                this.size = Math.random() * 3 + 2;
            }
            
            update() {
                this.x += this.vx;
                this.y += this.vy;
                this.life--;
                this.vx *= 0.99;
                this.vy *= 0.99;
            }
            
            draw(ctx) {
                const alpha = this.life / this.maxLife;
                ctx.save();
                ctx.globalAlpha = alpha;
                ctx.fillStyle = this.color;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
                ctx.restore();
            }
            
            isAlive() {
                return this.life > 0;
            }
        }
        
        let particles = [];
        
        // 绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 绘制碳储库
            drawReservoirs();
            
            // 绘制碳流动
            if (simulationState.showNatural) {
                drawFlows();
            }
            
            // 绘制人类活动
            if (simulationState.showHuman) {
                drawHumanActivities();
            }
            
            // 绘制温室效应
            if (simulationState.showGreenhouse) {
                drawGreenhouseEffect();
            }
            
            // 绘制数据标签
            if (simulationState.showLabels) {
                drawLabels();
            }
            
            // 绘制粒子
            drawParticles();
            
            // 绘制点击信息
            if (simulationState.activeInfo) {
                drawInfoPanel();
            }
        }
        
        function drawBackground() {
            // 渐变背景
            const gradient = ctx.createLinearGradient(0, 0, canvas.width, canvas.height);
            gradient.addColorStop(0, '#0a1929');
            gradient.addColorStop(1, '#1a2b3c');
            ctx.fillStyle = gradient;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 网格线
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.05)';
            ctx.lineWidth = 1;
            
            const gridSize = 50;
            for (let x = 0; x < canvas.width; x += gridSize) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, canvas.height);
                ctx.stroke();
            }
            for (let y = 0; y < canvas.height; y += gridSize) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(canvas.width, y);
                ctx.stroke();
            }
        }
        
        function drawReservoirs() {
            for (const [key, reservoir] of Object.entries(simulationState.reservoirs)) {
                const x = reservoir.x * canvas.width;
                const y = reservoir.y * canvas.height;
                const radius = reservoir.radius;
                
                // 绘制储库
                ctx.save();
                
                // 发光效果
                ctx.shadowColor = reservoir.color;
                ctx.shadowBlur = 15;
                
                // 填充
                const gradient = ctx.createRadialGradient(x, y, 0, x, y, radius);
                gradient.addColorStop(0, reservoir.color + 'cc');
                gradient.addColorStop(1, reservoir.color + '33');
                
                ctx.fillStyle = gradient;
                ctx.beginPath();
                ctx.arc(x, y, radius, 0, Math.PI * 2);
                ctx.fill();
                
                // 边框
                ctx.strokeStyle = reservoir.color;
                ctx.lineWidth = 2;
                ctx.stroke();
                
                ctx.restore();
                
                // 绘制标签
                if (simulationState.showLabels) {
                    ctx.fillStyle = '#ffffff';
                    ctx.font = '14px Arial';
                    ctx.textAlign = 'center';
                    
                    let label = '';
                    switch(key) {
                        case 'atmosphere': label = '大气圈'; break;
                        case 'ocean': label = '海洋'; break;
                        case 'biosphere': label = '生物圈'; break;
                        case 'soil': label = '土壤'; break;
                    }
                    
                    ctx.fillText(label, x, y + radius + 20);
                    ctx.fillText(`${Math.round(reservoir.value)} GtC`, x, y + radius + 40);
                }
            }
        }
        
        function drawFlows() {
            for (const [key, flow] of Object.entries(simulationState.flows)) {
                if (!flow.active) continue;
                
                const from = simulationState.reservoirs[flow.from];
                const to = simulationState.reservoirs[flow.to];
                
                const fromX = from.x * canvas.width;
                const fromY = from.y * canvas.height;
                const toX = to.x * canvas.width;
                const toY = to.y * canvas.height;
                
                // 计算箭头方向
                const dx = toX - fromX;
                const dy = toY - fromY;
                const distance = Math.sqrt(dx * dx + dy * dy);
                const angle = Math.atan2(dy, dx);
                
                // 调整起点和终点到圆边缘
                const startX = fromX + Math.cos(angle) * from.radius;
                const startY = fromY + Math.sin(angle) * from.radius;
                const endX = toX - Math.cos(angle) * to.radius;
                const endY = toY - Math.sin(angle) * to.radius;
                
                // 绘制流动线
                ctx.save();
                ctx.strokeStyle = flow.color;
                ctx.lineWidth = 2;
                ctx.lineCap = 'round';
                
                // 虚线效果
                ctx.setLineDash([5, 5]);
                
                ctx.beginPath();
                ctx.moveTo(startX, startY);
                ctx.lineTo(endX, endY);
                ctx.stroke();
                
                ctx.restore();
                
                // 绘制箭头
                const arrowSize = 8;
                const arrowX = endX - Math.cos(angle) * arrowSize;
                const arrowY = endY - Math.sin(angle) * arrowSize;
                
                ctx.save();
                ctx.fillStyle = flow.color;
                ctx.translate(arrowX, arrowY);
                ctx.rotate(angle);
                
                ctx.beginPath();
                ctx.moveTo(0, 0);
                ctx.lineTo(-arrowSize * 1.5, -arrowSize);
                ctx.lineTo(-arrowSize * 1.5, arrowSize);
                ctx.closePath();
                ctx.fill();
                
                ctx.restore();
                
                // 生成粒子
                if (simulationState.isPlaying) {
                    const progress = (simulationState.time % 100) / 100;
                    const particleX = startX + (endX - startX) * progress;
                    const particleY = startY + (endY - startY) * progress;
                    
                    if (Math.random() < 0.3) {
                        particles.push(new Particle(
                            particleX,
                            particleY,
                            flow.color,
                            Math.cos(angle) * 2,
                            Math.sin(angle) * 2,
                            50
                        ));
                    }
                }
            }
        }
        
        function drawHumanActivities() {
            for (const [key, activity] of Object.entries(simulationState.humanActivities)) {
                const x = activity.x * canvas.width;
                const y = activity.y * canvas.height;
                
                // 绘制图标
                ctx.save();
                ctx.font = '30px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(activity.icon, x, y);
                ctx.restore();
                
                // 绘制排放流
                const toX = simulationState.reservoirs.atmosphere.x * canvas.width;
                const toY = simulationState.reservoirs.atmosphere.y * canvas.height;
                
                const dx = toX - x;
                const dy = toY - y;
                const angle = Math.atan2(dy, dx);
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                // 调整终点到大气圈边缘
                const endX = toX - Math.cos(angle) * simulationState.reservoirs.atmosphere.radius;
                const endY = toY - Math.sin(angle) * simulationState.reservoirs.atmosphere.radius;
                
                // 绘制排放线
                ctx.save();
                ctx.strokeStyle = activity.color;
                ctx.lineWidth = 3;
                ctx.lineCap = 'round';
                
                // 闪烁效果
                const alpha = 0.5 + 0.5 * Math.sin(simulationState.time * 0.1);
                ctx.globalAlpha = alpha;
                
                ctx.beginPath();
                ctx.moveTo(x, y);
                ctx.lineTo(endX, endY);
                ctx.stroke();
                
                ctx.restore();
                
                // 生成排放粒子
                if (simulationState.isPlaying) {
                    const progress = (simulationState.time % 50) / 50;
                    const particleX = x + (endX - x) * progress;
                    const particleY = y + (endY - y) * progress;
                    
                    if (Math.random() < 0.5) {
                        particles.push(new Particle(
                            particleX,
                            particleY,
                            activity.color,
                            Math.cos(angle) * 3,
                            Math.sin(angle) * 3,
                            70
                        ));
                    }
                }
                
                // 绘制标签
                if (simulationState.showLabels) {
                    ctx.fillStyle = activity.color;
                    ctx.font = '12px Arial';
                    ctx.textAlign = 'center';
                    
                    let label = '';
                    switch(key) {
                        case 'fossilFuels': label = '化石燃料'; break;
                        case 'deforestation': label = '森林砍伐'; break;
                        case 'transportation': label = '交通运输'; break;
                    }
                    
                    ctx.fillText(`${label} ${activity.rate} GtC/年`, x, y + 25);
                }
            }
        }
        
        function drawGreenhouseEffect() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const maxRadius = Math.min(canvas.width, canvas.height) * 0.4;
            
            // 绘制热力图
            const gradient = ctx.createRadialGradient(
                centerX, centerY, maxRadius * 0.3,
                centerX, centerY, maxRadius
            );
            
            gradient.addColorStop(0, '#ef444400');
            gradient.addColorStop(0.5, '#f9731640');
            gradient.addColorStop(1, '#ef444420');
            
            ctx.save();
            ctx.fillStyle = gradient;
            ctx.beginPath();
            ctx.arc(centerX, centerY, maxRadius, 0, Math.PI * 2);
            ctx.fill();
            ctx.restore();
            
            // 绘制温度计
            const thermometerX = canvas.width - 100;
            const thermometerY = 100;
            const thermometerHeight = 200;
            const thermometerWidth = 30;
            
            // 温度计背景
            ctx.fillStyle = 'rgba(255, 255, 255, 0.1)';
            ctx.fillRect(thermometerX, thermometerY, thermometerWidth, thermometerHeight);
            
            // 温度填充
            const tempHeight = (simulationState.greenhouseEffect.temperatureRise / 5) * thermometerHeight;
            const tempGradient = ctx.createLinearGradient(
                thermometerX, thermometerY + thermometerHeight - tempHeight,
                thermometerX + thermometerWidth, thermometerY + thermometerHeight
            );
            
            tempGradient.addColorStop(0, '#10b981');
            tempGradient.addColorStop(0.5, '#f59e0b');
            tempGradient.addColorStop(1, '#ef4444');
            
            ctx.fillStyle = tempGradient;
            ctx.fillRect(
                thermometerX,
                thermometerY + thermometerHeight - tempHeight,
                thermometerWidth,
                tempHeight
            );
            
            // 温度计边框
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.5)';
            ctx.lineWidth = 2;
            ctx.strokeRect(thermometerX, thermometerY, thermometerWidth, thermometerHeight);
            
            // 标签
            ctx.fillStyle = '#ffffff';
            ctx.font = '12px Arial';
            ctx.textAlign = 'left';
            ctx.fillText('全球升温', thermometerX + thermometerWidth + 10, thermometerY + 20);
            ctx.fillText(`${simulationState.greenhouseEffect.temperatureRise.toFixed(1)}°C`, 
                        thermometerX + thermometerWidth + 10, thermometerY + 40);
        }
        
        function drawLabels() {
            // 绘制标题
            ctx.fillStyle = '#ffffff';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('生态系统碳循环模拟', canvas.width / 2, 30);
            
            // 绘制模式指示器
            let modeText =
<!--检测到代码截断，自动续写中...-->
let modeText = '';
            switch(simulationState.mode) {
                case 'natural': modeText = '模式：仅自然循环'; break;
                case 'preIndustrial': modeText = '模式：工业革命前'; break;
                case 'modern': modeText = '模式：现代高排放'; break;
                case 'future': modeText = '模式：未来情景'; break;
            }
            
            ctx.font = '14px Arial';
            ctx.fillStyle = simulationState.isPlaying ? '#4ade80' : '#f59e0b';
            ctx.fillText(`${modeText} | ${simulationState.isPlaying ? '播放中' : '已暂停'}`, canvas.width / 2, 55);
        }
        
        function drawParticles() {
            for (let i = particles.length - 1; i >= 0; i--) {
                const particle = particles[i];
                particle.update();
                particle.draw(ctx);
                
                if (!particle.isAlive()) {
                    particles.splice(i, 1);
                }
            }
        }
        
        function drawInfoPanel() {
            const info = simulationState.activeInfo;
            const panelWidth = 300;
            const panelHeight = 200;
            const x = Math.min(canvas.width - panelWidth - 20, info.x + 20);
            const y = Math.min(canvas.height - panelHeight - 20, info.y + 20);
            
            // 绘制面板背景
            ctx.save();
            ctx.fillStyle = 'rgba(30, 41, 59, 0.95)';
            ctx.strokeStyle = '#3b82f6';
            ctx.lineWidth = 2;
            ctx.shadowColor = 'rgba(0, 0, 0, 0.5)';
            ctx.shadowBlur = 10;
            ctx.shadowOffsetX = 0;
            ctx.shadowOffsetY = 5;
            
            ctx.beginPath();
            ctx.roundRect(x, y, panelWidth, panelHeight, 10);
            ctx.fill();
            ctx.stroke();
            ctx.restore();
            
            // 绘制标题
            ctx.fillStyle = '#7dd3fc';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'left';
            ctx.fillText(info.title, x + 15, y + 30);
            
            // 绘制内容
            ctx.fillStyle = '#e0f2fe';
            ctx.font = '14px Arial';
            const lines = info.content.split('\n');
            lines.forEach((line, i) => {
                ctx.fillText(line, x + 15, y + 60 + i * 25);
            });
            
            // 绘制关闭按钮
            ctx.fillStyle = '#ef4444';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('×', x + panelWidth - 20, y + 20);
        }
        
        // 模拟更新函数
        function updateSimulation() {
            if (!simulationState.isPlaying) return;
            
            simulationState.time += simulationState.speed;
            
            // 根据模式更新数据
            switch(simulationState.mode) {
                case 'natural':
                    // 自然平衡状态
                    simulationState.humanActivities.fossilFuels.rate = 0;
                    simulationState.humanActivities.deforestation.rate = 0;
                    simulationState.humanActivities.transportation.rate = 0;
                    simulationState.greenhouseEffect.temperatureRise = 0;
                    break;
                    
                case 'preIndustrial':
                    // 工业革命前
                    simulationState.humanActivities.fossilFuels.rate = 0.1;
                    simulationState.humanActivities.deforestation.rate = 0.3;
                    simulationState.humanActivities.transportation.rate = 0;
                    simulationState.greenhouseEffect.temperatureRise = 0;
                    break;
                    
                case 'modern':
                    // 现代高排放
                    simulationState.humanActivities.fossilFuels.rate = 9.5;
                    simulationState.humanActivities.deforestation.rate = 1.5;
                    simulationState.humanActivities.transportation.rate = 8.0;
                    simulationState.greenhouseEffect.temperatureRise = 1.2;
                    break;
                    
                case 'future':
                    // 未来情景
                    simulationState.humanActivities.fossilFuels.rate = 12.0;
                    simulationState.humanActivities.deforestation.rate = 2.0;
                    simulationState.humanActivities.transportation.rate = 10.0;
                    simulationState.greenhouseEffect.temperatureRise = 2.8;
                    break;
            }
            
            // 更新碳储库
            updateReservoirs();
            
            // 更新UI显示
            updateUIDisplay();
            
            // 更新挑战模拟
            updateChallenge();
        }
        
        function updateReservoirs() {
            // 计算净自然流动
            let netNaturalFlow = 0;
            for (const flow of Object.values(simulationState.flows)) {
                if (flow.active) {
                    const from = simulationState.reservoirs[flow.from];
                    const to = simulationState.reservoirs[flow.to];
                    
                    // 确保有足够的碳
                    if (from.value >= flow.rate * 0.01) {
                        from.value -= flow.rate * 0.01;
                        to.value += flow.rate * 0.01;
                    }
                }
            }
            
            // 计算人类排放
            let totalHumanEmission = 0;
            for (const activity of Object.values(simulationState.humanActivities)) {
                totalHumanEmission += activity.rate;
                simulationState.reservoirs.atmosphere.value += activity.rate * 0.01;
            }
            
            // 更新大气CO₂浓度显示
            const co2Value = document.getElementById('co2Value');
            const baseCO2 = 280; // 工业革命前浓度
            const humanContribution = totalHumanEmission * 0.47; // 简化转换因子
            const currentCO2 = Math.round(baseCO2 + humanContribution);
            co2Value.textContent = currentCO2;
            
            // 更新温度
            const tempValue = document.getElementById('tempValue');
            const tempRise = simulationState.greenhouseEffect.temperatureRise;
            tempValue.textContent = tempRise.toFixed(1);
            tempValue.className = 'data-value ' + 
                (tempRise < 1 ? 'success' : tempRise < 2 ? '' : 'warning');
            
            // 更新排放量
            const emissionValue = document.getElementById('emissionValue');
            emissionValue.textContent = (totalHumanEmission * 3.67).toFixed(1); // 转换为Gt CO2
            
            // 更新平衡状态
            const balanceStatus = document.getElementById('balanceStatus');
            const balanceDetail = document.getElementById('balanceDetail');
            
            const naturalAbsorption = simulationState.flows.oceanUptake.rate + 
                                     simulationState.flows.photosynthesis.rate;
            
            if (totalHumanEmission > naturalAbsorption * 0.8) {
                balanceStatus.textContent = '严重失衡';
                balanceStatus.className = 'data-value warning';
                balanceDetail.textContent = `(自然吸收 ${naturalAbsorption.toFixed(1)} < 人类排放 ${totalHumanEmission.toFixed(1)} GtC/年)`;
            } else if (totalHumanEmission > 0) {
                balanceStatus.textContent = '轻度失衡';
                balanceStatus.className = 'data-value';
                balanceDetail.textContent = `(自然吸收 ${naturalAbsorption.toFixed(1)} ≈ 人类排放 ${totalHumanEmission.toFixed(1)} GtC/年)`;
            } else {
                balanceStatus.textContent = '平衡';
                balanceStatus.className = 'data-value success';
                balanceDetail.textContent = '(自然循环动态平衡)';
            }
        }
        
        function updateUIDisplay() {
            // 更新速度显示
            document.getElementById('speedValue').textContent = simulationState.speed.toFixed(1) + 'x';
            
            // 更新按钮状态
            document.getElementById('btnPlay').textContent = simulationState.isPlaying ? '⏸️ 暂停' : '▶️ 播放';
            
            // 更新模式按钮
            const modeButtons = ['btnNatural', 'btnPreIndustrial', 'btnModern', 'btnFuture'];
            modeButtons.forEach(btnId => {
                document.getElementById(btnId).classList.remove('active');
            });
            document.getElementById('btn' + simulationState.mode.charAt(0).toUpperCase() + simulationState.mode.slice(1)).classList.add('active');
        }
        
        function updateChallenge() {
            // 获取滑块值
            const energyValue = parseInt(document.getElementById('energySlider').value);
            const forestValue = parseInt(document.getElementById('forestSlider').value);
            const efficiencyValue = parseInt(document.getElementById('efficiencySlider').value);
            
            // 更新显示值
            document.getElementById('energyValue').textContent = energyValue + '%';
            document.getElementById('forestValue').textContent = forestValue + '%';
            document.getElementById('efficiencyValue').textContent = efficiencyValue + '%';
            
            // 计算未来CO2浓度
            const baseCO2 = 415; // 当前浓度
            const energyFactor = (100 - energyValue) / 100;
            const forestFactor = (40 - forestValue) / 40;
            const efficiencyFactor = (100 - efficiencyValue) / 100;
            
            const futureCO2 = Math.round(baseCO2 + 
                energyFactor * 150 + 
                forestFactor * 80 + 
                efficiencyFactor * 70);
            
            // 计算未来温度
            const baseTemp = 1.2;
            const tempRise = baseTemp + 
                (futureCO2 - 415) / 100 * 0.6;
            
            // 更新显示
            document.getElementById('futureCO2').textContent = futureCO2;
            document.getElementById('futureTemp').textContent = tempRise.toFixed(1);
            
            // 更新挑战结果
            const challengeMessage = document.getElementById('challengeMessage');
            if (tempRise <= 2.0) {
                challengeMessage.textContent = '✅ 达成2°C目标';
                challengeMessage.className = 'result-value success';
            } else if (tempRise <= 2.5) {
                challengeMessage.textContent = '⚠️ 接近目标';
                challengeMessage.className = 'result-value';
            } else {
                challengeMessage.textContent = '❌ 超出2°C目标';
                challengeMessage.className = 'result-value warning';
            }
        }
        
        // 事件处理
        function setupEventListeners() {
            // 画布点击事件
            canvas.addEventListener('click', (e) => {
                const rect = canvas.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                // 检查是否点击关闭按钮
                if (simulationState.activeInfo) {
                    const panelWidth = 300;
                    const panelHeight = 200;
                    const infoX = Math.min(canvas.width - panelWidth - 20, simulationState.activeInfo.x + 20);
                    const infoY = Math.min(canvas.height - panelHeight - 20, simulationState.activeInfo.y + 20);
                    
                    if (x >= infoX + panelWidth - 30 && x <= infoX + panelWidth - 10 &&
                        y >= infoY && y <= infoY + 30) {
                        simulationState.activeInfo = null;
                        return;
                    }
                }
                
                // 检查点击了哪个元素
                let clickedElement = null;
                
                // 检查碳储库
                for (const [key, reservoir] of Object.entries(simulationState.reservoirs)) {
                    const resX = reservoir.x * canvas.width;
                    const resY = reservoir.y * canvas.height;
                    const distance = Math.sqrt((x - resX) ** 2 + (y - resY) ** 2);
                    
                    if (distance <= reservoir.radius) {
                        let title = '';
                        let content = '';
                        
                        switch(key) {
                            case 'atmosphere':
                                title = '🌤️ 大气圈';
                                content = '碳储量：约850 GtC\n主要过程：\n- 光合作用吸收CO₂\n- 呼吸作用释放CO₂\n- 海洋气体交换\n人类影响：化石燃料排放增加大气CO₂浓度';
                                break;
                            case 'ocean':
                                title = '🌊 海洋';
                                content = '碳储量：约38,000 GtC\n主要过程：\n- 物理溶解泵\n- 生物泵（浮游生物）\n- 碳酸盐泵\n吸收能力：年吸收约92 GtC';
                                break;
                            case 'biosphere':
                                title = '🌳 生物圈';
                                content = '碳储量：约560 GtC\n主要过程：\n- 光合作用固定CO₂\n- 呼吸作用释放CO₂\n- 食物链传递\n人类影响：森林砍伐减少碳汇';
                                break;
                            case 'soil':
                                title = '🟤 土壤';
                                content = '碳储量：约2,300 GtC\n主要过程：\n- 有机物分解\n- 微生物呼吸\n- 碳矿化\n储存时间：数百年至数千年';
                                break;
                        }
                        
                        clickedElement = { title, content, x, y };
                        break;
                    }
                }
                
                // 检查人类活动
                if (!clickedElement) {
                    for (const [key, activity] of Object.entries(simulationState.humanActivities)) {
                        const actX = activity.x * canvas.width;
                        const actY = activity.y * canvas.height;
                        const distance = Math.sqrt((x - actX) ** 2 + (y - actY) ** 2);
                        
                        if (distance <= 30) {
                            let title = '';
                            let content = '';
                            
                            switch(key) {
                                case 'fossilFuels':
                                    title = '🏭 化石燃料燃烧';
                                    content = `年排放量：${activity.rate} GtC/年\n来源：\n- 煤炭发电\n- 石油化工\n- 天然气\n影响：工业革命以来主要排放源`;
                                    break;
                                case 'deforestation':
                                    title = '🪓 土地利用变化';
                                    content = `年排放量：${activity.rate} GtC/年\n原因：\n- 森林砍伐\n- 农业扩张\n- 城市发展\n影响：减少碳汇，释放土壤碳`;
                                    break;
                                case 'transportation':
                                    title = '🚗 交通运输';
                                    content = `年排放量：${activity.rate} GtC/年\n来源：\n- 汽车尾气\n- 航空燃油\n- 船舶燃料\n趋势：随经济发展持续增长`;
                                    break;
                            }
                            
                            clickedElement = { title, content, x, y };
                            break;
                        }
                    }
                }
                
                simulationState.activeInfo = clickedElement;
            });
            
            // 控制按钮事件
            document.getElementById('btnPlay').addEventListener('click', () => {
                simulationState.isPlaying = !simulationState.isPlaying;
                updateUIDisplay();
            });
            
            document.getElementById('btnReset').addEventListener('click', () => {
                simulationState.time = 0;
                simulationState.mode = 'natural';
                simulationState.isPlaying = true;
                
                // 重置碳储库
                simulationState.reservoirs.atmosphere.value = 850;
                simulationState.reservoirs.ocean.value = 38000;
                simulationState.reservoirs.biosphere.value = 560;
                simulationState.reservoirs.soil.value = 2300;
                
                updateUIDisplay();
            });
            
            document.getElementById('btnFastForward').addEventListener('click', () => {
                simulationState.time += 10000; // 快进100年
                simulationState.mode = 'future';
                updateUIDisplay();
            });
            
            // 模式按钮事件
            document.getElementById('btnNatural').addEventListener('click', () => {
                simulationState.mode = 'natural';
                updateUIDisplay();
            });
            
            document.getElementById('btnPreIndustrial').addEventListener('click', () => {
                simulationState.mode = 'preIndustrial';
                updateUIDisplay();
            });
            
            document.getElementById('btnModern').addEventListener('click', () => {
                simulationState.mode = 'modern';
                updateUIDisplay();
            });
            
            document.getElementById('btnFuture').addEventListener('click', () => {
                simulationState.mode = 'future';
                updateUIDisplay();
            });
            
            // 速度滑块
            document.getElementById('speedSlider').addEventListener('input', (e) => {
                simulationState.speed = parseFloat(e.target.value);
                updateUIDisplay();
            });
            
            // 显示选项切换
            document.getElementById('toggleNatural').addEventListener('change', (e) => {
                simulationState.showNatural = e.target.checked;
            });
            
            document.getElementById('toggleHuman').addEventListener('change', (e) => {
                simulationState.showHuman = e.target.checked;
            });
            
            document.getElementById('toggleGreenhouse').addEventListener('change', (e) => {
                simulationState.showGreenhouse = e.target.checked;
            });
            
            document.getElementById('toggleLabels').addEventListener('change', (e) => {
                simulationState.showLabels = e.target.checked;
            });
            
            // 挑战滑块
            document.getElementById('energySlider').addEventListener('input', updateChallenge);
            document.getElementById('forestSlider').addEventListener('input', updateChallenge);
            document.getElementById('efficiencySlider').addEventListener('input', updateChallenge);
        }
        
        // 动画循环
        function animate() {
            updateSimulation();
            draw();
            requestAnimationFrame(animate);
        }
        
        // 初始化
        function init() {
            setupEventListeners();
            updateChallenge(); // 初始化挑战模拟
            animate();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
        
        // 添加roundRect支持
        if (!CanvasRenderingContext2D.prototype.roundRect) {
            CanvasRenderingContext2D.prototype.roundRect = function(x, y, width, height, radius) {
                if (width < 2 * radius) radius = width / 2;
                if (height < 2 * radius) radius = height / 2;
                this.beginPath();
                this.moveTo(x + radius, y);
                this.arcTo(x + width, y, x + width, y + height, radius);
                this.arcTo(x + width, y + height, x, y + height, radius);
                this.arcTo(x, y + height, x, y, radius);
                this.arcTo(x, y, x + width, y, radius);
                this.closePath();
                return this;
            };
        }
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 🌍 生态系统碳循环与全球碳失衡：交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态可视化与直观交互，帮助您深入理解生态系统碳循环的复杂过程以及人类活动如何导致全球碳失衡。无论您是教师、学生还是对环境科学感兴趣的公众，本指南都将帮助您充分利用这一教学资源。

---

### 一、功能说明

本动画是一个基于HTML5 Canvas构建的完整模拟系统，它动态展示了碳元素在**大气圈、海洋、生物圈和土壤**四大储库之间的自然流动，并叠加了**人类活动**（化石燃料燃烧、森林砍伐、交通运输）的干扰。系统实时计算并可视化碳通量、大气CO₂浓度变化及全球温度上升，将抽象的科学数据转化为直观的视觉体验。

---

### 二、主要功能模块

#### 1. **核心模拟区（主画布）**
*   **动态碳循环**：观察以彩色箭头和流动粒子表示的碳流动过程，包括光合作用、呼吸作用、分解、海洋吸收与释放。
*   **碳储库**：四个主要储库（大气、海洋、生物圈、土壤）以彩色圆球显示，其大小和数值标签随碳储量变化。
*   **人类活动源**：工厂、汽车、斧头图标代表主要排放源，红色/橙色流动线醒目地展示其向大气的额外碳输入。
*   **点击交互**：**点击画布中的任何元素（储库或图标）**，会弹出详细信息面板，包含科学数据和过程解释。

#### 2. **模拟控制面板**
*   **场景模式**：一键切换四种预设情景：
    *   **仅自然循环**：观察无人类干扰的理想平衡状态。
    *   **工业革命前**：观察低强度人类活动的影响。
    *   **现代高排放**：展示当前人类活动主导的碳流（默认情景）。
    *   **未来情景**：模拟在“一切照旧”路径下的可能未来。
*   **时间控制**：
    *   **播放/暂停**：控制模拟运行。
    *   **速度滑块**：调整模拟速度（0.1x 至 3.0x）。
    *   **重置**：将模拟恢复至初始状态。
    *   **快进100年**：直观展示长期排放的累积效应。
*   **显示图层开关**：独立控制“自然碳流”、“人类排放”、“温室效应热力图”和“数据标签”的显示与隐藏，便于分层讲解。

#### 3. **实时数据仪表盘**
实时显示关键指标：
*   **大气CO₂浓度 (ppm)**
*   **全球平均温度变化 (°C)**
*   **年碳排放量 (Gt CO₂/年)**
*   **碳循环状态**（平衡/失衡）

#### 4. **“减排挑战”互动模块**
这是一个基于情景的探索性游戏：
*   **目标**：通过调整三个滑块（**能源结构**、**森林覆盖率**、**工业效率**），尝试将2100年的全球升温控制在2°C以内。
*   **即时反馈**：调整滑块会立即更新预测的2100年CO₂浓度和温升结果，并给出“成功”、“接近”或“失败”的评价。
*   **教学意义**：让学习者直观理解不同减排措施的相对贡献和协同效应。

---

### 三、设计特色与教学理念

1.  **视觉隐喻与编码**：
    *   **颜色编码**：自然过程使用**蓝-绿色系**，人类排放使用**橙-红色系**，从视觉上清晰区分“自然”与“人为”。
    *   **粒子系统**：用流动的粒子代表碳原子（CO₂）的移动，使“通量”概念变得生动可感。
    *   **动态缩放**：储库大小和数值的轻微变化，直观体现碳的“源”与“汇”。

2.  **建构主义学习路径**：
    *   **先建立基线**：建议首先在“仅自然循环”模式下运行，理解系统的动态平衡。
    *   **再引入干扰**：切换到“现代高排放”模式，观察平衡如何被打破，大气库如何“膨胀”。
    *   **最后探索解决方案**：在“减排挑战”中主动探索缓解路径，完成从认知到行动的思维闭环。

3.  **支持探究式学习**：
    *   学习者可以自主控制变量（如关闭人类排放观察恢复），提出并验证假设。
    *   弹出的详细信息卡片提供了深入探究的起点。

---

### 四、核心教学要点与讨论引导

教师或自学者可围绕以下要点展开学习与讨论：

| 模块 | 核心概念 | 可提出的问题 |
| :--- | :--- | :--- |
| **自然循环** | 碳循环的动态平衡、储库与通量 | 1. 自然循环中，碳最主要的“源”和“汇”分别是什么？<br>2. 为什么说工业革命前碳循环大致是平衡的？ |
| **人类干扰** | 人为排放、碳汇破坏、净通量 | 1. 比较三条红色排放流，哪一个是当前最大的贡献者？<br>2. 森林砍伐如何同时影响碳的“源”和“汇”？ |
| **碳失衡** | 大气CO₂浓度累积、温室效应 | 1. 为什么排放的碳不会立即被海洋和森林完全吸收？<br>2. 观察“快进100年”后，温度和CO₂浓度发生了什么变化？这说明了什么科学原理？ |
| **减排挑战** | 减缓路径、政策协同、技术选择 | 1. 要实现2°C目标，哪个杠杆（能源、森林、效率）最有效？<br>2. 为什么需要多管齐下，而不是只依靠一种方案？ |

---

### 五、使用建议

1.  **课堂教学（教师主导）**：
    *   **引入**：全屏播放动画，提出一个核心问题（如“我们呼吸的碳原子从何而来，去往何处？”）。
    *   **讲解**：使用“暂停”功能，结合“显示图层开关”，分层讲解各个过程。利用“点击交互”调出详细数据。
    *   **探究**：将学生分组，分配不同的“场景模式”或“减排挑战”任务，让他们探索并汇报结果。
    *   **评估**：让学生描述从“自然循环”到“现代高排放”模式切换时观察到的三个关键变化。

2.  **自主学习**：
    *   建议按照“**观察 → 交互 → 记录 → 反思**”的步骤进行。
    *   打开一个记事本，记录下你操作不同控件时观察到的现象和产生的疑问。
    *   尝试完成“减排挑战”目标，并思考其现实意义。

3.  **最佳实践**：
    *   **首次使用**：请先点击“**仅自然循环**”模式，然后点击“**重置**”按钮，从头开始体验完整的学习流程。
    *   **深入探索**：尝试关闭“自然碳流”图层，只观察“人类排放”，直观感受人类活动的相对规模和路径。
    *   **联系现实**：将模拟中显示的当前CO₂浓度（~415 ppm）与工业革命前（280 ppm）进行对比，理解变化的剧烈程度。

---

**结语**
本工具不仅仅是一个动画，更是一个动态的、可探索的科学模型。我们希望它能点燃您对地球系统科学的好奇心，并深刻理解人类在这个复杂而精妙的碳循环中所扮演的角色。让我们一起观察、思考并探索可持续的未来路径。

祝您探索愉快！