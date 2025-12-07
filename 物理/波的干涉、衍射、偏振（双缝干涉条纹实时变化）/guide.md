# 需求：波的干涉、衍射、偏振（双缝干涉条纹实时变化）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的物理学习者。他们已具备波动的基本知识（如波长、频率、振幅），但对波的干涉、衍射和偏振等抽象概念的理解存在困难。
2.  **核心痛点**：
    *   **抽象性**：干涉条纹的形成、衍射现象的变化、偏振光的特性难以通过静态图片或公式直观理解。
    *   **动态过程**：双缝干涉条纹随参数（如波长、缝距）的实时变化是关键教学难点，需要动态可视化。
    *   **概念关联**：学生容易将干涉、衍射、偏振视为孤立现象，需要在一个统一的框架下展示它们的联系与区别。
    *   **探究需求**：学习者希望通过自主调节参数，观察现象变化，从而构建自己的物理图景，而非被动接受结论。
3.  **学习目标**：通过本动画，用户应能：
    *   直观理解双缝干涉条纹的形成原理和分布规律。
    *   掌握干涉条纹间距与波长、缝距、屏距的定性关系。
    *   初步了解单缝衍射对双缝干涉图样的调制作用。
    *   理解偏振片对光波振动方向的筛选作用，以及偏振对干涉条纹的影响。

#### 教学设计思路
1.  **核心概念与结构**：
    *   **主线**：以“双缝干涉”为核心实验装置，逐步引入和关联“衍射”与“偏振”。
    *   **分解**：
        *   **干涉**：展示两列相干波（水波或光波）从双缝发出，在空间叠加，形成稳定的加强区（亮纹）和减弱区（暗纹）。重点展示光程差与明暗条纹位置的对应关系。
        *   **衍射**：将每个缝视为一个次波源，展示光通过单缝时的衍射现象。进而展示“双缝干涉”实际受“单缝衍射”调制的综合图样（即干涉条纹的包络线受衍射影响）。
        *   **偏振**：在光路中加入可旋转的偏振片，展示自然光变为偏振光的过程，以及当两束光偏振方向垂直时，干涉条纹消失的现象，强调相干条件中“振动方向相同”的重要性。
2.  **认知规律**：
    *   **从具体到抽象**：先使用更直观的水波类比演示干涉和衍射的波动叠加原理，再过渡到光波。
    *   **从理想到实际**：先展示理想的、无限窄缝的干涉条纹（等间距明暗条纹），再引入单缝衍射的调制效应（条纹亮度不均匀），更符合物理实际。
    *   **从观察到控制**：用户先观察自动演示，然后通过交互控件主动改变参数，建立“因-果”联系，深化理解。
3.  **交互设计**：
    *   **模块化标签页**：设计“干涉”、“干涉+衍射”、“偏振”三个主标签，内容由浅入深，结构清晰。
    *   **实时同步可视化**：界面分为“控制面板”、“波动传播区”和“接收屏/光强分布图”三个主要区域。任何参数调整，三个区域的变化实时、同步发生。
    *   **渐进式提示与标注**：关键位置（如波峰、波谷、光程差、振动方向）有动态或静态标注。首次进入时有简明的操作指引。
4.  **视觉呈现**：
    *   **波动传播区**：采用简洁的线条图或粒子点阵代表波阵面。用对比色（如蓝/红）分别表示从两个缝发出的子波，叠加区域用颜色混合或亮度变化表示加强或减弱。
    *   **接收屏**：干涉条纹的显示要清晰、锐利。随着参数变化，条纹应平滑地移动或变密/变疏。
    *   **光强分布曲线**：在屏幕旁同步绘制理论光强分布曲线（I-x 或 I-θ 曲线），将直观的条纹与抽象的数学表达直接关联，是教学的关键桥梁。
    *   **动画节奏**：波传播速度适中，便于跟踪；参数变化时，动画过渡平滑，避免跳跃。

#### 配色方案选择
*   **主色调**：深空蓝 (#0F1A2F) 或深灰 (#2C3E50) 作为画布背景，模拟暗室环境，突出光波和条纹。
*   **波动与光路**：
    *   相干子波1：亮青色 (#00FFFF)，代表高能/波峰。
    *   相干子波2：洋红色 (#FF00FF)，代表高能/波峰。
    *   波谷/背景：使用主色调的浅色渐变，对比度低。
    *   **叠加效果**：加强区（同相）显示为亮白色或亮黄色；减弱区（反相）显示为暗灰色或接近背景色。
*   **干涉条纹**：在接收屏上，亮纹为亮黄色 (#FFFF00) 或白色，暗纹为背景色。
*   **控制面板与UI元素**：使用浅卡其色 (#F5F5DC) 或浅灰色 (#ECF0F1) 背景，搭配深蓝色 (#2980B9) 的滑块和按钮，确保可读性和操作感。
*   **标注与曲线**：使用醒目的白色或亮绿色 (#00FF00) 进行标注。光强分布曲线用橙色 (#FFA500) 绘制，与屏上条纹纵向对齐。
*   **整体原则**：高对比度以突出核心元素，颜色有明确的语义（如两种子波、叠加结果），且整体色调舒适，不易引起视觉疲劳。

#### 交互功能列表
1.  **核心参数控制（滑块）**：
    *   光源波长 (λ)：可调范围（例如代表可见光的400nm-700nm）。
    *   双缝间距 (d)：可调范围（例如0.05mm - 0.5mm）。
    *   缝屏距离 (L)：可调范围（例如1m - 3m）。
    *   （在“干涉+衍射”模块）单缝宽度 (a)：可调范围。
2.  **实验装置控制**：
    *   **光源切换**：按钮在“水波类比”和“单色光”之间切换。
    *   **偏振片控制**（在“偏振”模块）：
        *   偏振片1（置于缝前）开关与旋转角度控制。
        *   偏振片2（置于缝前）开关与旋转角度控制。
        *   检偏器（置于屏前）开关与旋转角度控制。
3.  **视图与显示控制**：
    *   **动画播放/暂停**：控制波传播动画。
    *   **显示/隐藏**：复选框控制“波阵面”、“光强分布曲线”、“标注文字”等的显示。
    *   **重置**：按钮将所有参数恢复至默认值。
4.  **信息反馈**：
    *   实时显示当前参数值（λ， d， L， a等）。
    *   在波动传播区，鼠标悬停于某点时，显示该点相对于两个缝的光程差 (Δr) 和相位差。
    *   在接收屏上，鼠标悬停时，显示该位置的相对光强值。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>波的干涉、衍射与偏振 - 双缝干涉实验模拟</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #0F1A2F;
            color: #ECF0F1;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #2980B9;
        }
        
        h1 {
            color: #00FFFF;
            font-size: 2.4rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            color: #FFA500;
            font-size: 1.2rem;
            font-weight: normal;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 25px;
        }
        
        .simulation-area {
            flex: 1;
            min-width: 800px;
            background-color: #1A2536;
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
        }
        
        .canvas-container {
            position: relative;
            flex: 1;
            border: 1px solid #2C3E50;
            border-radius: 5px;
            overflow: hidden;
            background-color: #0F1A2F;
        }
        
        #mainCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .control-panel {
            flex: 0 0 350px;
            background-color: #1A2536;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
        }
        
        .tabs {
            display: flex;
            margin-bottom: 20px;
            border-bottom: 1px solid #2C3E50;
        }
        
        .tab {
            padding: 10px 20px;
            background-color: transparent;
            color: #ECF0F1;
            border: none;
            border-bottom: 3px solid transparent;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s;
        }
        
        .tab.active {
            color: #00FFFF;
            border-bottom-color: #00FFFF;
            background-color: rgba(0, 255, 255, 0.1);
        }
        
        .tab:hover:not(.active) {
            background-color: rgba(255, 255, 255, 0.05);
        }
        
        .tab-content {
            flex: 1;
            display: none;
        }
        
        .tab-content.active {
            display: flex;
            flex-direction: column;
        }
        
        .control-group {
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px dashed #2C3E50;
        }
        
        .control-group:last-child {
            border-bottom: none;
        }
        
        .control-title {
            color: #FFA500;
            margin-bottom: 12px;
            font-size: 1.1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .control-item {
            margin-bottom: 15px;
        }
        
        .control-label {
            display: block;
            margin-bottom: 6px;
            color: #ECF0F1;
            font-size: 0.95rem;
        }
        
        .value-display {
            color: #00FFFF;
            font-weight: bold;
            background-color: rgba(0, 0, 0, 0.2);
            padding: 2px 8px;
            border-radius: 3px;
            min-width: 60px;
            text-align: center;
            display: inline-block;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        input[type="range"] {
            flex: 1;
            height: 6px;
            -webkit-appearance: none;
            background: linear-gradient(to right, #2980B9, #00FFFF);
            border-radius: 3px;
            outline: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: #FFA500;
            cursor: pointer;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
        }
        
        .button-group {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        
        button {
            padding: 10px 15px;
            background-color: #2980B9;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 0.95rem;
            transition: background-color 0.3s;
            flex: 1;
        }
        
        button:hover {
            background-color: #3498DB;
        }
        
        button:active {
            transform: translateY(1px);
        }
        
        .toggle-switch {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        
        .switch-label {
            color: #ECF0F1;
            font-size: 0.95rem;
        }
        
        .switch {
            position: relative;
            display: inline-block;
            width: 50px;
            height: 24px;
        }
        
        .switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }
        
        .slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #2C3E50;
            transition: .4s;
            border-radius: 24px;
        }
        
        .slider:before {
            position: absolute;
            content: "";
            height: 16px;
            width: 16px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: .4s;
            border-radius: 50%;
        }
        
        input:checked + .slider {
            background-color: #00FFFF;
        }
        
        input:checked + .slider:before {
            transform: translateX(26px);
        }
        
        .info-panel {
            background-color: #1A2536;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            margin-top: 20px;
        }
        
        .info-title {
            color: #FFA500;
            margin-bottom: 15px;
            font-size: 1.2rem;
        }
        
        .info-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
        }
        
        .info-item {
            background-color: rgba(255, 255, 255, 0.05);
            padding: 12px;
            border-radius: 5px;
            border-left: 3px solid #2980B9;
        }
        
        .info-item h4 {
            color: #00FFFF;
            margin-bottom: 5px;
            font-size: 1rem;
        }
        
        .info-item p {
            color: #BDC3C7;
            font-size: 0.9rem;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #2C3E50;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 3px;
        }
        
        .legend-text {
            font-size: 0.85rem;
            color: #BDC3C7;
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #2C3E50;
            color: #7F8C8D;
            font-size: 0.9rem;
        }
        
        @media (max-width: 1200px) {
            .main-content {
                flex-direction: column;
            }
            
            .simulation-area {
                min-width: 100%;
            }
            
            .control-panel {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>波的干涉、衍射与偏振</h1>
            <p class="subtitle">双缝干涉实验实时模拟与探究</p>
        </header>
        
        <div class="main-content">
            <div class="simulation-area">
                <div class="canvas-container">
                    <canvas id="mainCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #00FFFF;"></div>
                        <div class="legend-text">左侧缝发出的波</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FF00FF;"></div>
                        <div class="legend-text">右侧缝发出的波</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FFFF00;"></div>
                        <div class="legend-text">干涉加强区（亮纹）</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FFA500;"></div>
                        <div class="legend-text">光强分布曲线</div>
                    </div>
                </div>
            </div>
            
            <div class="control-panel">
                <div class="tabs">
                    <button class="tab active" data-tab="interference">干涉</button>
                    <button class="tab" data-tab="diffraction">干涉+衍射</button>
                    <button class="tab" data-tab="polarization">偏振</button>
                </div>
                
                <div id="interference" class="tab-content active">
                    <div class="control-group">
                        <div class="control-title">
                            <span>实验参数</span>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                波长 λ: <span class="value-display" id="wavelengthValue">550</span> nm
                            </div>
                            <div class="slider-container">
                                <input type="range" id="wavelengthSlider" min="400" max="700" step="10" value="550">
                            </div>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                双缝间距 d: <span class="value-display" id="slitDistanceValue">0.2</span> mm
                            </div>
                            <div class="slider-container">
                                <input type="range" id="slitDistanceSlider" min="0.05" max="0.5" step="0.01" value="0.2">
                            </div>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                缝屏距离 L: <span class="value-display" id="screenDistanceValue">1.5</span> m
                            </div>
                            <div class="slider-container">
                                <input type="range" id="screenDistanceSlider" min="1" max="3" step="0.1" value="1.5">
                            </div>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-title">
                            <span>显示控制</span>
                        </div>
                        
                        <div class="toggle-switch">
                            <span class="switch-label">显示波阵面</span>
                            <label class="switch">
                                <input type="checkbox" id="showWavefronts" checked>
                                <span class="slider"></span>
                            </label>
                        </div>
                        
                        <div class="toggle-switch">
                            <span class="switch-label">显示光强曲线</span>
                            <label class="switch">
                                <input type="checkbox" id="showIntensityCurve" checked>
                                <span class="slider"></span>
                            </label>
                        </div>
                        
                        <div class="toggle-switch">
                            <span class="switch-label">显示标注</span>
                            <label class="switch">
                                <input type="checkbox" id="showLabels" checked>
                                <span class="slider"></span>
                            </label>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="button-group">
                            <button id="playPauseBtn">暂停动画</button>
                            <button id="resetBtn">重置参数</button>
                        </div>
                    </div>
                </div>
                
                <div id="diffraction" class="tab-content">
                    <div class="control-group">
                        <div class="control-title">
                            <span>干涉+衍射参数</span>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                单缝宽度 a: <span class="value-display" id="slitWidthValue">0.04</span> mm
                            </div>
                            <div class="slider-container">
                                <input type="range" id="slitWidthSlider" min="0.01" max="0.1" step="0.005" value="0.04">
                            </div>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                波长 λ: <span class="value-display" id="wavelengthValue2">550</span> nm
                            </div>
                            <div class="slider-container">
                                <input type="range" id="wavelengthSlider2" min="400" max="700" step="10" value="550">
                            </div>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                双缝间距 d: <span class="value-display" id="slitDistanceValue2">0.2</span> mm
                            </div>
                            <div class="slider-container">
                                <input type="range" id="slitDistanceSlider2" min="0.05" max="0.5" step="0.01" value="0.2">
                            </div>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-title">
                            <span>显示控制</span>
                        </div>
                        
                        <div class="toggle-switch">
                            <span class="switch-label">显示衍射包络</span>
                            <label class="switch">
                                <input type="checkbox" id="showDiffractionEnvelope" checked>
                                <span class="slider"></span>
                            </label>
                        </div>
                        
                        <div class="toggle-switch">
                            <span class="switch-label">显示光强曲线</span>
                            <label class="switch">
                                <input type="checkbox" id="showIntensityCurve2" checked>
                                <span class="slider"></span>
                            </label>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="button-group">
                            <button id="playPauseBtn2">暂停动画</button>
                            <button id="resetBtn2">重置参数</button>
                        </div>
                    </div>
                </div>
                
                <div id="polarization" class="tab-content">
                    <div class="control-group">
                        <div class="control-title">
                            <span>偏振片设置</span>
                        </div>
                        
                        <div class="toggle-switch">
                            <span class="switch-label">偏振片1 (左缝前)</span>
                            <label class="switch">
                                <input type="checkbox" id="polarizer1Toggle" checked>
                                <span class="slider"></span>
                            </label>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                偏振片1角度: <span class="value-display" id="polarizer1AngleValue">0</span>°
                            </div>
                            <div class="slider-container">
                                <input type="range" id="polarizer1AngleSlider" min="0" max="180" step="1" value="0">
                            </div>
                        </div>
                        
                        <div class="toggle-switch">
                            <span class="switch-label">偏振片2 (右缝前)</span>
                            <label class="switch">
                                <input type="checkbox" id="polarizer2Toggle" checked>
                                <span class="slider"></span>
                            </label>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                偏振片2角度: <span class="value-display" id="polarizer2AngleValue">0</span>°
                            </div>
                            <div class="slider-container">
                                <input type="range" id="polarizer2AngleSlider" min="0" max="180" step="1" value="0">
                            </div>
                        </div>
                        
                        <div class="toggle-switch">
                            <span class="switch-label">检偏器 (屏前)</span>
                            <label class="switch">
                                <input type="checkbox" id="analyzerToggle">
                                <span class="slider"></span>
                            </label>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                检偏器角度: <span class="value-display" id="analyzerAngleValue">0</span>°
                            </div>
                            <div class="slider-container">
                                <input type="range" id="analyzerAngleSlider" min="0" max="180" step="1" value="0">
                            </div>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-title">
                            <span>干涉参数</span>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                波长 λ: <span class="value-display" id="wavelengthValue3">550</span> nm
                            </div>
                            <div class="slider-container">
                                <input type="range" id="wavelengthSlider3" min="400" max="700" step="10" value="550">
                            </div>
                        </div>
                        
                        <div class="control-item">
                            <div class="control-label">
                                双缝间距 d: <span class="value-display" id="slitDistanceValue3">0.2</span> mm
                            </div>
                            <div class="slider-container">
                                <input type="range" id="slitDistanceSlider3" min="0.05" max="0.5" step="0.01" value="0.2">
                            </div>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="button-group">
                            <button id="playPauseBtn3">暂停动画</button>
                            <button id="resetBtn3">重置参数</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="info-panel">
            <h3 class="info-title">物理原理说明</h3>
            <div class="info-content">
                <div class="info-item">
                    <h4>双缝干涉</h4>
                    <p>光通过两个狭缝后形成相干光源，在屏幕上叠加形成明暗相间的条纹。亮纹位置满足光程差 Δ = d·sinθ = mλ (m=0,±1,±2...)。条纹间距 Δx = λL/d。</p>
                </div>
                <div class="info-item">
                    <h4>单缝衍射调制</h4>
                    <p>实际双缝实验中，每个缝都有一定宽度a，会产生单缝衍射。双缝干涉图样受到单缝衍射光强分布的调制，表现为干涉条纹的包络线由衍射图样决定。</p>
                </div>
                <div class="info-item">
                    <h4>偏振对干涉的影响</h4>
                    <p>光的相干条件包括频率相同、相位差恒定、振动方向相同。当两束光的偏振方向垂直时，即使其他条件满足，也不会产生干涉条纹。</p>
                </div>
            </div>
        </div>
        
        <footer>
            <p>波的干涉、衍射与偏振教学动画 | 设计：教育技术专家 | 使用HTML5 Canvas实现</p>
            <p>提示：鼠标悬停在屏幕上可查看该点的光程差和光强信息</p>
        </footer>
    </div>

    <script>
        // 全局变量和配置
        const canvas = document.getElementById('mainCanvas');
        const ctx = canvas.getContext('2d');
        
        // 调整Canvas大小以适应容器
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        
        // 初始调整大小
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 模拟状态
        let simulationState = {
            // 通用参数
            isPlaying: true,
            time: 0,
            animationSpeed: 0.05,
            
            // 干涉参数
            wavelength: 550, // nm
            slitDistance: 0.2, // mm
            screenDistance: 1.5, // m
            
            // 衍射参数
            slitWidth: 0.04, // mm
            showDiffractionEnvelope: true,
            
            // 偏振参数
            polarizer1: { enabled: true, angle: 0 }, // 角度(度)
            polarizer2: { enabled: true, angle: 0 },
            analyzer: { enabled: false, angle: 0 },
            
            // 显示控制
            showWavefronts: true,
            showIntensityCurve: true,
            showLabels: true,
            
            // 当前活动标签
            activeTab: 'interference',
            
            // 鼠标交互
            mouseX: -1,
            mouseY: -1
        };
        
        // 物理常量
        const MM_TO_M = 0.001;
        const NM_TO_M = 1e-9;
        
        // 初始化UI控件与状态同步
        function initializeControls() {
            // 标签切换
            document.querySelectorAll('.tab').forEach(tab => {
                tab.addEventListener('click', function() {
                    const tabId = this.getAttribute('data-tab');
                    switchTab(tabId);
                });
            });
            
            // 干涉标签控件
            document.getElementById('wavelengthSlider').addEventListener('input', function() {
                simulationState.wavelength = parseFloat(this.value);
                document.getElementById('wavelengthValue').textContent = this.value;
            });
            
            document.getElementById('slitDistanceSlider').addEventListener('input', function() {
                simulationState.slitDistance = parseFloat(this.value);
                document.getElementById('slitDistanceValue').textContent = this.value;
            });
            
            document.getElementById('screenDistanceSlider').addEventListener('input', function() {
                simulationState.screenDistance = parseFloat(this.value);
                document.getElementById('screenDistanceValue').textContent = this.value;
            });
            
            document.getElementById('showWavefronts').addEventListener('change', function() {
                simulationState.showWavefronts = this.checked;
            });
            
            document.getElementById('showIntensityCurve').addEventListener('change', function() {
                simulationState.showIntensityCurve = this.checked;
            });
            
            document.getElementById('showLabels').addEventListener('change', function() {
                simulationState.showLabels = this.checked;
            });
            
            document.getElementById('playPauseBtn').addEventListener('click', function() {
                simulationState.isPlaying = !simulationState.isPlaying;
                this.textContent = simulationState.isPlaying ? '暂停动画' : '播放动画';
            });
            
            document.getElementById('resetBtn').addEventListener('click', function() {
                resetToDefaults('interference');
            });
            
            // 衍射标签控件
            document.getElementById('slitWidthSlider').addEventListener('input', function() {
                simulationState.slitWidth = parseFloat(this.value);
                document.getElementById('slitWidthValue').textContent = this.value;
            });
            
            document.getElementById('wavelengthSlider2').addEventListener('input', function() {
                simulationState.wavelength = parseFloat(this.value);
                document.getElementById('wavelengthValue2').textContent = this.value;
            });
            
            document.getElementById('slitDistanceSlider2').addEventListener('input', function() {
                simulationState.slitDistance = parseFloat(this.value);
                document.getElementById('slitDistanceValue2').textContent = this.value;
            });
            
            document.getElementById('showDiffractionEnvelope').addEventListener('change', function() {
                simulationState.showDiffractionEnvelope = this.checked;
            });
            
            document.getElementById('showIntensityCurve2').addEventListener('change', function() {
                simulationState.showIntensityCurve = this.checked;
            });
            
            document.getElementById('playPauseBtn2').addEventListener('click', function() {
                simulationState.isPlaying = !simulationState.isPlaying;
                this.textContent = simulationState.isPlaying ? '暂停动画' : '播放动画';
            });
            
            document.getElementById('resetBtn2').addEventListener('click', function() {
                resetToDefaults('diffraction');
            });
            
            // 偏振标签控件
            document.getElementById('polarizer1Toggle').addEventListener('change', function() {
                simulationState.polarizer1.enabled = this.checked;
            });
            
            document.getElementById('polarizer1AngleSlider').addEventListener('input', function() {
                simulationState.polarizer1.angle = parseFloat(this.value);
                document.getElementById('polarizer1AngleValue').textContent = this.value;
            });
            
            document.getElementById('polarizer2Toggle').addEventListener('change', function() {
                simulationState.polarizer2.enabled = this.checked;
            });
            
            document.getElementById('polarizer2AngleSlider').addEventListener('input', function() {
                simulationState.polarizer2.angle = parseFloat(this.value);
                document.getElementById('polarizer2AngleValue').textContent = this.value;
            });
            
            document.getElementById('analyzerToggle').addEventListener('change', function() {
                simulationState.analyzer.enabled = this.checked;
            });
            
            document.getElementById('analyzerAngleSlider').addEventListener('input', function() {
                simulationState.analyzer.angle = parseFloat(this.value);
                document.getElementById('analyzerAngleValue').textContent = this.value;
            });
            
            document.getElementById('wavelengthSlider3').addEventListener('input', function() {
                simulationState.wavelength = parseFloat(this.value);
                document.getElementById('wavelengthValue3').textContent = this.value;
            });
            
            document.getElementById('slitDistanceSlider3').addEventListener('input', function() {
                simulationState.slitDistance = parseFloat(this.value);
                document.getElementById('slitDistanceValue3').textContent = this.value;
            });
            
            document.getElementById('playPauseBtn3').addEventListener('click', function() {
                simulationState.isPlaying = !simulationState.isPlaying;
                this.textContent = simulationState.isPlaying ? '暂停动画' : '播放动画';
            });
            
            document.getElementById('resetBtn3').addEventListener('click', function() {
                resetToDefaults('polarization');
            });
            
            // 鼠标移动交互
            canvas.addEventListener('mousemove', function(event) {
                const rect = canvas.getBoundingClientRect();
                simulationState.mouseX = event.clientX - rect.left;
                simulationState.mouseY = event.clientY - rect.top;
            });
            
            canvas.addEventListener('mouseleave', function() {
                simulationState.mouseX = -1;
                simulationState.mouseY = -1;
            });
        }
        
        // 切换标签
        function switchTab(tabId) {
            // 更新UI
            document.querySelectorAll('.tab').forEach(tab => {
                tab.classList.remove('active');
            });
            document.querySelector(`.tab[data-tab="${tabId}"]`).classList.add('active');
            
            document.querySelectorAll('.tab-content').forEach(content => {
                content.classList.remove('active');
            });
            document.getElementById(tabId).classList.add('active');
            
            // 更新状态
            simulationState.activeTab = tabId;
        }
        
        // 重置参数到默认值
        function resetToDefaults(tab) {
            if (tab === 'interference') {
                simulationState.wavelength = 550;
                simulationState.slitDistance = 0.2;
                simulationState.screenDistance = 1.5;
                
                document.getElementById('wavelengthSlider').value = 550;
                document.getElementById('slitDistanceSlider').value = 0.2;
                document.getElementById('screenDistanceSlider').value = 1.5;
                
                document.getElementById('wavelengthValue').textContent = '550';
                document.getElementById('slitDistanceValue').textContent = '0.2';
                document.getElementById('screenDistanceValue').textContent = '1.5';
            } 
            else if (tab === 'diffraction') {
                simulationState.wavelength = 550;
                simulationState.slitDistance = 0.2;
                simulationState.slitWidth = 0.04;
                
                document.getElementById('wavelengthSlider2').value = 550;
                document.getElementById('slitDistanceSlider2').value = 0.2;
                document.getElementById('slitWidthSlider').value = 0.04;
                
                document.getElementById('wavelengthValue2').textContent = '550';
                document.getElementById('slitDistanceValue2').textContent = '0.2';
                document.getElementById('slitWidthValue').textContent = '0.04';
            }
            else if (tab === 'polarization') {
                simulationState.wavelength = 550;
                simulationState.slitDistance = 0.2;
                simulationState.polarizer1 = { enabled: true, angle: 0 };
                simulationState.polarizer2 = { enabled: true, angle: 0 };
                simulationState.analyzer = { enabled: false, angle: 0 };
                
                document.getElementById('wavelengthSlider3').value = 550;
                document.getElementById('slitDistanceSlider3').value = 0.2;
                document.getElementById('polarizer1Toggle').checked = true;
                document.getElementById('polarizer1AngleSlider').value = 0;
                document.getElementById('polarizer2Toggle').checked = true;
                document.getElementById('polarizer2AngleSlider').value = 0;
                document.getElementById('analyzerToggle').checked = false;
                document.getElementById('analyzerAngleSlider').value = 0;
                
                document.getElementById('wavelengthValue3').textContent = '550';
                document.getElementById('slitDistanceValue3').textContent = '0.2';
                document.getElementById('polarizer1AngleValue').textContent = '0';
                document.getElementById('polarizer2AngleValue').textContent = '0';
                document.getElementById('analyzerAngleValue').textContent = '0';
            }
        }
        
        // 计算干涉光强
        function calculateInterferenceIntensity(x, y, params) {
            const { wavelength, slitDistance, screenDistance, time, includeDiffraction = false, slitWidth = 0 } = params;
            
            // 转换为米
            const lambda = wavelength * NM_TO_M;
            const d = slitDistance * MM_TO_M;
            const L = screenDistance;
            const a = slitWidth * MM_TO_M;
            
            // 屏幕上的位置（以中心为原点）
            const screenX = (x / canvas.width - 0.5) * 0.3 * L; // 缩放因子
            
            // 计算从两个缝到屏幕上点的距离
            const r1 = Math.sqrt(L*L + (screenX - d/2)*(screenX - d/2));
            const r2 = Math.sqrt(L*L + (screenX + d/2)*(screenX + d/2));
            
            // 光程差和相位差
            const pathDifference = r2 - r1;
            const phaseDifference = 2 * Math.PI * pathDifference / lambda;
            
            // 时间相关的相位
            const timePhase = 2 * Math.PI * time;
            
            // 干涉项
            const interferenceTerm = Math.cos(phaseDifference + timePhase);
            
            // 单缝衍射因子（如果包含衍射）
            let diffractionFactor = 1;
            if (includeDiffraction && a > 0) {
                const beta = Math.PI * a * Math.sin(Math.atan(screenX / L)) / lambda;
                if (Math.abs(beta) > 1e-10) {
                    diffractionFactor = Math.pow(Math.sin(beta) / beta, 2);
                }
            }
            
            // 总光强（归一化）
            return diffractionFactor * (1 + interferenceTerm) / 2;
        }
        
        // 计算偏振影响下的干涉光强
        function calculatePolarizedInterferenceIntensity(x, y, params) {
            const { wavelength, slitDistance, screenDistance, time, polarizer1, polarizer2, analyzer } = params;
            
            // 转换为米
            const lambda = wavelength * NM_TO_M;
            const d = slitDistance * MM_TO_M;
            const L = screenDistance;
            
            // 屏幕上的位置（以中心为原点）
            const screenX = (x / canvas.width - 0.5) * 0.3 * L;
            
            // 计算从两个缝到屏幕上点的距离
            const r1 = Math.sqrt(L*L + (screenX - d/2)*(screenX - d/2));
            const r2 = Math.sqrt(L*L + (screenX + d/2)*(screenX + d/2));
            
            // 光程差和相位差
            const pathDifference = r2 - r1;
            const phaseDifference = 2 * Math.PI * pathDifference / lambda;
            
            // 时间相关的相位
            const timePhase = 2 * Math.PI * time;
            
            // 偏振角度转换为弧度
            const theta1 = polarizer1.enabled ? polarizer1.angle * Math.PI / 180 : 0;
            const theta2 = polarizer2.enabled ? polarizer2.angle * Math.PI / 180 : 0;
            const thetaA = analyzer.enabled ? analyzer.angle * Math.PI / 180 : 0;
            
            // 计算电场分量
            const E1x = Math.cos(theta1) * Math.cos(phaseDifference/2 + timePhase);
            const E1y = Math.sin(theta1) * Math.cos(phaseDifference/2 + timePhase);
            
            const E2x = Math.cos(theta2) * Math.cos(-phaseDifference/2 + timePhase);
            const E2y = Math.sin(theta2) * Math.cos(-phaseDifference/2 + timePhase);
            
            // 通过检偏器后的分量
            const Ex = (E1x + E2x) * Math.cos(thetaA) + (E1y + E2y) * Math.sin(thetaA);
            
            // 光强与电场振幅平方成正比
            return Ex * Ex / 4; // 归一化
        }
        
        // 绘制实验装置
        function drawApparatus
<!--检测到代码截断，自动续写中...-->
() {
            const width = canvas.width;
            const height = canvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制暗室背景
            ctx.fillStyle = '#0F1A2F';
            ctx.fillRect(0, 0, width, height);
            
            // 定义布局参数
            const leftMargin = width * 0.05;
            const rightMargin = width * 0.05;
            const topMargin = height * 0.1;
            const bottomMargin = height * 0.15;
            
            const sourceX = leftMargin + width * 0.1;
            const slitsX = leftMargin + width * 0.3;
            const screenX = width - rightMargin - width * 0.1;
            
            const centerY = height / 2;
            const slitSpacing = simulationState.slitDistance * 100; // 放大显示
            
            // 绘制光源
            ctx.fillStyle = '#FFFF00';
            ctx.beginPath();
            ctx.arc(sourceX, centerY, 10, 0, Math.PI * 2);
            ctx.fill();
            
            if (simulationState.showLabels) {
                ctx.fillStyle = '#FFFFFF';
                ctx.font = '14px Arial';
                ctx.fillText('单色光源', sourceX - 30, centerY - 15);
            }
            
            // 绘制光路（从光源到双缝）
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.3)';
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            ctx.moveTo(sourceX + 10, centerY);
            ctx.lineTo(slitsX - 20, centerY);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制双缝板
            ctx.fillStyle = '#7F8C8D';
            ctx.fillRect(slitsX - 10, topMargin, 20, height - topMargin - bottomMargin);
            
            // 绘制双缝
            ctx.fillStyle = '#0F1A2F';
            const slitHeight = 40;
            ctx.fillRect(slitsX - 2, centerY - slitHeight/2, 4, slitHeight);
            
            // 绘制两个缝
            const leftSlitY = centerY - slitSpacing/2;
            const rightSlitY = centerY + slitSpacing/2;
            
            ctx.fillStyle = '#00FFFF';
            ctx.beginPath();
            ctx.arc(slitsX, leftSlitY, 4, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.fillStyle = '#FF00FF';
            ctx.beginPath();
            ctx.arc(slitsX, rightSlitY, 4, 0, Math.PI * 2);
            ctx.fill();
            
            if (simulationState.showLabels) {
                ctx.fillStyle = '#FFFFFF';
                ctx.font = '14px Arial';
                ctx.fillText('双缝板', slitsX - 25, topMargin + 20);
                ctx.fillText(`d = ${simulationState.slitDistance} mm`, slitsX + 15, centerY);
            }
            
            // 绘制偏振片（如果激活）
            if (simulationState.activeTab === 'polarization') {
                drawPolarizers(slitsX, leftSlitY, rightSlitY);
            }
            
            // 绘制接收屏
            ctx.fillStyle = '#34495E';
            ctx.fillRect(screenX - 5, topMargin, 10, height - topMargin - bottomMargin);
            
            if (simulationState.showLabels) {
                ctx.fillStyle = '#FFFFFF';
                ctx.font = '14px Arial';
                ctx.fillText('接收屏', screenX - 25, topMargin + 20);
                ctx.fillText(`L = ${simulationState.screenDistance} m`, (slitsX + screenX)/2, topMargin - 10);
            }
            
            // 绘制光路（从双缝到屏幕）
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.2)';
            ctx.setLineDash([3, 3]);
            ctx.beginPath();
            ctx.moveTo(slitsX + 10, leftSlitY);
            ctx.lineTo(screenX - 5, topMargin + 50);
            ctx.moveTo(slitsX + 10, rightSlitY);
            ctx.lineTo(screenX - 5, topMargin + 50);
            ctx.stroke();
            ctx.setLineDash([]);
            
            return {
                sourceX, slitsX, screenX,
                leftSlitY, rightSlitY,
                topMargin, bottomMargin,
                centerY
            };
        }
        
        // 绘制偏振片
        function drawPolarizers(slitsX, leftSlitY, rightSlitY) {
            const polarizerSize = 15;
            
            // 左缝前的偏振片
            if (simulationState.polarizer1.enabled) {
                const angle1 = simulationState.polarizer1.angle * Math.PI / 180;
                ctx.save();
                ctx.translate(slitsX - 30, leftSlitY);
                ctx.rotate(angle1);
                
                ctx.fillStyle = 'rgba(52, 152, 219, 0.7)';
                ctx.fillRect(-polarizerSize/2, -polarizerSize/2, polarizerSize, polarizerSize);
                
                ctx.strokeStyle = '#FFFFFF';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(0, -polarizerSize/2);
                ctx.lineTo(0, polarizerSize/2);
                ctx.stroke();
                
                ctx.restore();
                
                if (simulationState.showLabels) {
                    ctx.fillStyle = '#3498DB';
                    ctx.font = '12px Arial';
                    ctx.fillText(`P1: ${simulationState.polarizer1.angle}°`, slitsX - 50, leftSlitY - 20);
                }
            }
            
            // 右缝前的偏振片
            if (simulationState.polarizer2.enabled) {
                const angle2 = simulationState.polarizer2.angle * Math.PI / 180;
                ctx.save();
                ctx.translate(slitsX - 30, rightSlitY);
                ctx.rotate(angle2);
                
                ctx.fillStyle = 'rgba(231, 76, 60, 0.7)';
                ctx.fillRect(-polarizerSize/2, -polarizerSize/2, polarizerSize, polarizerSize);
                
                ctx.strokeStyle = '#FFFFFF';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(0, -polarizerSize/2);
                ctx.lineTo(0, polarizerSize/2);
                ctx.stroke();
                
                ctx.restore();
                
                if (simulationState.showLabels) {
                    ctx.fillStyle = '#E74C3C';
                    ctx.font = '12px Arial';
                    ctx.fillText(`P2: ${simulationState.polarizer2.angle}°`, slitsX - 50, rightSlitY + 25);
                }
            }
            
            // 检偏器（屏前）
            if (simulationState.analyzer.enabled) {
                const analyzerX = canvas.width * 0.7;
                const analyzerY = canvas.height / 2;
                const angleA = simulationState.analyzer.angle * Math.PI / 180;
                
                ctx.save();
                ctx.translate(analyzerX, analyzerY);
                ctx.rotate(angleA);
                
                ctx.fillStyle = 'rgba(46, 204, 113, 0.7)';
                ctx.fillRect(-polarizerSize*1.5, -polarizerSize*1.5, polarizerSize*3, polarizerSize*3);
                
                ctx.strokeStyle = '#FFFFFF';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(0, -polarizerSize*1.5);
                ctx.lineTo(0, polarizerSize*1.5);
                ctx.stroke();
                
                ctx.restore();
                
                if (simulationState.showLabels) {
                    ctx.fillStyle = '#2ECC71';
                    ctx.font = '12px Arial';
                    ctx.fillText(`A: ${simulationState.analyzer.angle}°`, analyzerX - 25, analyzerY - 30);
                }
            }
        }
        
        // 绘制波阵面
        function drawWavefronts(slitsX, leftSlitY, rightSlitY) {
            if (!simulationState.showWavefronts) return;
            
            const time = simulationState.time;
            const wavelength = simulationState.wavelength;
            const waveSpeed = 0.5; // 动画速度因子
            
            // 计算当前波前半径
            const baseRadius = (time % 1) * 100 * waveSpeed;
            
            // 绘制左缝发出的波（青色）
            for (let i = 0; i < 5; i++) {
                const radius = baseRadius + i * 25;
                if (radius > 0) {
                    ctx.strokeStyle = `rgba(0, 255, 255, ${0.7 - i * 0.15})`;
                    ctx.lineWidth = 1.5;
                    ctx.beginPath();
                    ctx.arc(slitsX, leftSlitY, radius, 0, Math.PI * 2);
                    ctx.stroke();
                }
            }
            
            // 绘制右缝发出的波（洋红色）
            for (let i = 0; i < 5; i++) {
                const radius = baseRadius + i * 25;
                if (radius > 0) {
                    ctx.strokeStyle = `rgba(255, 0, 255, ${0.7 - i * 0.15})`;
                    ctx.lineWidth = 1.5;
                    ctx.beginPath();
                    ctx.arc(slitsX, rightSlitY, radius, 0, Math.PI * 2);
                    ctx.stroke();
                }
            }
            
            // 绘制叠加区域
            const overlapRadius = baseRadius + 50;
            if (overlapRadius > 30) {
                // 计算两圆交点区域
                const d = Math.abs(rightSlitY - leftSlitY);
                if (overlapRadius > d/2) {
                    ctx.save();
                    
                    // 创建叠加效果
                    const gradient = ctx.createRadialGradient(
                        slitsX, leftSlitY, overlapRadius - 20,
                        slitsX, leftSlitY, overlapRadius + 20
                    );
                    gradient.addColorStop(0, 'rgba(255, 255, 0, 0.3)');
                    gradient.addColorStop(1, 'rgba(255, 255, 0, 0)');
                    
                    ctx.fillStyle = gradient;
                    ctx.beginPath();
                    ctx.arc(slitsX, leftSlitY, overlapRadius + 20, 0, Math.PI * 2);
                    ctx.arc(slitsX, rightSlitY, overlapRadius + 20, 0, Math.PI * 2);
                    ctx.fill('evenodd');
                    
                    ctx.restore();
                }
            }
        }
        
        // 绘制干涉条纹
        function drawInterferencePattern(apparatus) {
            const { screenX, topMargin, bottomMargin } = apparatus;
            const screenWidth = 10;
            const screenHeight = canvas.height - topMargin - bottomMargin;
            const screenTop = topMargin;
            
            // 绘制屏幕上的干涉条纹
            const imageData = ctx.createImageData(screenWidth, screenHeight);
            const data = imageData.data;
            
            for (let y = 0; y < screenHeight; y++) {
                // 计算屏幕上的y位置（相对于中心）
                const screenY = screenTop + y;
                const normalizedY = (y / screenHeight - 0.5) * 2;
                
                let intensity;
                
                if (simulationState.activeTab === 'polarization') {
                    // 偏振干涉
                    intensity = calculatePolarizedInterferenceIntensity(
                        screenX, screenY,
                        {
                            wavelength: simulationState.wavelength,
                            slitDistance: simulationState.slitDistance,
                            screenDistance: simulationState.screenDistance,
                            time: simulationState.time,
                            polarizer1: simulationState.polarizer1,
                            polarizer2: simulationState.polarizer2,
                            analyzer: simulationState.analyzer
                        }
                    );
                } else {
                    // 普通干涉或干涉+衍射
                    const includeDiffraction = simulationState.activeTab === 'diffraction';
                    intensity = calculateInterferenceIntensity(
                        screenX, screenY,
                        {
                            wavelength: simulationState.wavelength,
                            slitDistance: simulationState.slitDistance,
                            screenDistance: simulationState.screenDistance,
                            time: simulationState.time,
                            includeDiffraction: includeDiffraction,
                            slitWidth: includeDiffraction ? simulationState.slitWidth : 0
                        }
                    );
                }
                
                // 将强度转换为颜色
                const brightness = Math.pow(intensity, 0.7); // Gamma校正
                const colorValue = Math.floor(brightness * 255);
                
                for (let x = 0; x < screenWidth; x++) {
                    const index = (y * screenWidth + x) * 4;
                    data[index] = colorValue;     // R
                    data[index + 1] = colorValue; // G
                    data[index + 2] = 0;          // B
                    data[index + 3] = 255;        // A
                }
            }
            
            // 将图像数据绘制到屏幕上
            ctx.putImageData(imageData, screenX - screenWidth/2, screenTop);
            
            // 绘制衍射包络线（如果激活）
            if (simulationState.activeTab === 'diffraction' && simulationState.showDiffractionEnvelope) {
                drawDiffractionEnvelope(screenX, screenTop, screenHeight);
            }
            
            // 绘制光强分布曲线（如果激活）
            if (simulationState.showIntensityCurve) {
                drawIntensityCurve(screenX, screenTop, screenHeight);
            }
            
            // 鼠标交互：显示当前位置信息
            if (simulationState.mouseX >= screenX - screenWidth/2 && 
                simulationState.mouseX <= screenX + screenWidth/2 &&
                simulationState.mouseY >= screenTop && 
                simulationState.mouseY <= screenTop + screenHeight) {
                
                const mouseY = simulationState.mouseY;
                const relativeY = (mouseY - screenTop) / screenHeight;
                
                // 计算光程差
                const lambda = simulationState.wavelength * NM_TO_M;
                const d = simulationState.slitDistance * MM_TO_M;
                const L = simulationState.screenDistance;
                const screenY = (relativeY - 0.5) * 0.3 * L;
                
                const r1 = Math.sqrt(L*L + (screenY - d/2)*(screenY - d/2));
                const r2 = Math.sqrt(L*L + (screenY + d/2)*(screenY + d/2));
                const pathDifference = (r2 - r1) * 1e6; // 转换为微米
                
                // 计算光强
                let intensity;
                if (simulationState.activeTab === 'polarization') {
                    intensity = calculatePolarizedInterferenceIntensity(
                        screenX, mouseY,
                        {
                            wavelength: simulationState.wavelength,
                            slitDistance: simulationState.slitDistance,
                            screenDistance: simulationState.screenDistance,
                            time: simulationState.time,
                            polarizer1: simulationState.polarizer1,
                            polarizer2: simulationState.polarizer2,
                            analyzer: simulationState.analyzer
                        }
                    );
                } else {
                    const includeDiffraction = simulationState.activeTab === 'diffraction';
                    intensity = calculateInterferenceIntensity(
                        screenX, mouseY,
                        {
                            wavelength: simulationState.wavelength,
                            slitDistance: simulationState.slitDistance,
                            screenDistance: simulationState.screenDistance,
                            time: simulationState.time,
                            includeDiffraction: includeDiffraction,
                            slitWidth: includeDiffraction ? simulationState.slitWidth : 0
                        }
                    );
                }
                
                // 绘制信息框
                ctx.fillStyle = 'rgba(0, 0, 0, 0.8)';
                ctx.fillRect(simulationState.mouseX + 10, simulationState.mouseY - 60, 180, 55);
                
                ctx.fillStyle = '#FFFFFF';
                ctx.font = '12px Arial';
                ctx.fillText(`光程差 Δr: ${pathDifference.toFixed(2)} μm`, simulationState.mouseX + 15, simulationState.mouseY - 40);
                ctx.fillText(`相对光强 I: ${intensity.toFixed(3)}`, simulationState.mouseX + 15, simulationState.mouseY - 20);
                
                const order = pathDifference * 1e-6 / lambda; // 干涉级次
                ctx.fillText(`干涉级次 m: ${order.toFixed(2)}`, simulationState.mouseX + 15, simulationState.mouseY);
            }
        }
        
        // 绘制衍射包络线
        function drawDiffractionEnvelope(screenX, screenTop, screenHeight) {
            const lambda = simulationState.wavelength * NM_TO_M;
            const a = simulationState.slitWidth * MM_TO_M;
            const L = simulationState.screenDistance;
            
            ctx.strokeStyle = 'rgba(0, 255, 255, 0.6)';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 3]);
            ctx.beginPath();
            
            for (let y = 0; y <= screenHeight; y += 2) {
                const relativeY = (y / screenHeight - 0.5) * 2;
                const screenY = relativeY * 0.15 * L;
                const theta = Math.atan(screenY / L);
                
                const beta = Math.PI * a * Math.sin(theta) / lambda;
                let intensity;
                
                if (Math.abs(beta) < 1e-10) {
                    intensity = 1;
                } else {
                    intensity = Math.pow(Math.sin(beta) / beta, 2);
                }
                
                const x = screenX + 20 + intensity * 100;
                const plotY = screenTop + y;
                
                if (y === 0) {
                    ctx.moveTo(x, plotY);
                } else {
                    ctx.lineTo(x, plotY);
                }
            }
            
            ctx.stroke();
            ctx.setLineDash([]);
            
            if (simulationState.showLabels) {
                ctx.fillStyle = '#00FFFF';
                ctx.font = '12px Arial';
                ctx.fillText('单缝衍射包络', screenX + 130, screenTop + 20);
            }
        }
        
        // 绘制光强分布曲线
        function drawIntensityCurve(screenX, screenTop, screenHeight) {
            const curveWidth = 150;
            const curveX = screenX + 40;
            
            ctx.strokeStyle = '#FFA500';
            ctx.lineWidth = 2;
            ctx.beginPath();
            
            for (let y = 0; y <= screenHeight; y += 2) {
                const screenY = screenTop + y;
                
                let intensity;
                if (simulationState.activeTab === 'polarization') {
                    intensity = calculatePolarizedInterferenceIntensity(
                        screenX, screenY,
                        {
                            wavelength: simulationState.wavelength,
                            slitDistance: simulationState.slitDistance,
                            screenDistance: simulationState.screenDistance,
                            time: simulationState.time,
                            polarizer1: simulationState.polarizer1,
                            polarizer2: simulationState.polarizer2,
                            analyzer: simulationState.analyzer
                        }
                    );
                } else {
                    const includeDiffraction = simulationState.activeTab === 'diffraction';
                    intensity = calculateInterferenceIntensity(
                        screenX, screenY,
                        {
                            wavelength: simulationState.wavelength,
                            slitDistance: simulationState.slitDistance,
                            screenDistance: simulationState.screenDistance,
                            time: simulationState.time,
                            includeDiffraction: includeDiffraction,
                            slitWidth: includeDiffraction ? simulationState.slitWidth : 0
                        }
                    );
                }
                
                const x = curveX + intensity * curveWidth;
                const plotY = screenTop + y;
                
                if (y === 0) {
                    ctx.moveTo(x, plotY);
                } else {
                    ctx.lineTo(x, plotY);
                }
            }
            
            ctx.stroke();
            
            // 绘制坐标轴
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.5)';
            ctx.lineWidth = 1;
            ctx.beginPath();
            ctx.moveTo(curveX, screenTop);
            ctx.lineTo(curveX, screenTop + screenHeight);
            ctx.moveTo(curveX, screenTop + screenHeight/2);
            ctx.lineTo(curveX + curveWidth, screenTop + screenHeight/2);
            ctx.stroke();
            
            if (simulationState.showLabels) {
                ctx.fillStyle = '#FFA500';
                ctx.font = '12px Arial';
                ctx.fillText('光强分布 I(x)', curveX + 10, screenTop + 20);
                ctx.fillText('0', curveX - 10, screenTop + screenHeight/2 + 4);
                ctx.fillText('1', curveX + curveWidth + 5, screenTop + screenHeight/2 + 4);
            }
        }
        
        // 绘制物理公式和说明
        function drawFormulasAndInfo() {
            if (!simulationState.showLabels) return;
            
            const width = canvas.width;
            const height = canvas.height;
            
            ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
            ctx.font = '14px Arial';
            
            // 根据当前标签显示不同的公式
            if (simulationState.activeTab === 'interference') {
                ctx.fillText('双缝干涉公式:', width * 0.05, height * 0.05);
                ctx.fillText('亮纹条件: Δ = d·sinθ = mλ', width * 0.05, height * 0.05 + 20);
                ctx.fillText('条纹间距: Δx = λL/d', width * 0.05, height * 0.05 + 40);
                
                // 显示当前参数计算出的条纹间距
                const lambda = simulationState.wavelength * 1e-9; // m
                const d = simulationState.slitDistance * 1e-3; // m
                const L = simulationState.screenDistance; // m
                const deltaX = (lambda * L / d) * 1000; // mm
                
                ctx.fillText(`当前条纹间距: Δx = ${deltaX.toFixed(2)} mm`, width * 0.05, height * 0.05 + 65);
            }
            else if (simulationState.activeTab === 'diffraction') {
                ctx.fillText('干涉+衍射公式:', width * 0.05, height * 0.05);
                ctx.fillText('I = I₀·(sinβ/β)²·cos²(δ/2)', width * 0.05, height * 0.05 + 20);
                ctx.fillText('其中 β = πa·sinθ/λ, δ = 2πd·sinθ/λ', width * 0.05, height * 0.05 + 40);
                
                // 显示缺级条件
                const ratio = simulationState.slitDistance / simulationState.slitWidth;
                ctx.fillText(`缝宽比 d/a = ${ratio.toFixed(2)}`, width * 0.05, height * 0.05 + 65);
                if (Math.abs(ratio - Math.round(ratio)) < 0.1) {
                    ctx.fillStyle = '#FF5555';
                    ctx.fillText(`第${Math.round(ratio)}级干涉条纹缺级!`, width * 0.05, height * 0.05 + 85);
                }
            }
            else if (simulationState.activeTab === 'polarization') {
                ctx.fillText('偏振干涉:', width * 0.05, height * 0.05);
                
                // 计算偏振夹角
                const angleDiff = Math.abs(simulationState.polarizer1.angle - simulationState.polarizer2.angle);
                const cosDiff = Math.cos(angleDiff * Math.PI / 180);
                
                ctx.fillText(`偏振片夹角: ${angleDiff.toFixed(1)}°`, width * 0.05, height * 0.05 + 20);
                ctx.fillText(`干涉可见度: V = |cos(${angleDiff.toFixed(1)}°)| = ${Math.abs(cosDiff).toFixed(3)}`, width * 0.05, height * 0.05 + 40);
                
                if (angleDiff > 85 && angleDiff < 95) {
                    ctx.fillStyle = '#FF5555';
                    ctx.fillText('偏振方向垂直 → 干涉条纹消失!', width * 0.05, height * 0.05 + 65);
                }
            }
        }
        
        // 主渲染函数
        function render() {
            // 绘制实验装置
            const apparatus = drawApparatus();
            
            // 绘制波阵面
            drawWavefronts(apparatus.slitsX, apparatus.leftSlitY, apparatus.rightSlitY);
            
            // 绘制干涉条纹
            drawInterferencePattern(apparatus);
            
            // 绘制公式和说明
            drawFormulasAndInfo();
        }
        
        // 动画循环
        function animate() {
            if (simulationState.isPlaying) {
                simulationState.time += simulationState.animationSpeed;
                if (simulationState.time > 1000) simulationState.time = 0;
            }
            
            render();
            requestAnimationFrame(animate);
        }
        
        // 初始化
        function init() {
            initializeControls();
            animate();
            
            // 初始调整大小
            resizeCanvas();
        }
        
        // 启动应用
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## 波的干涉、衍射与偏振交互式教学动画使用指南

欢迎使用这款专业的物理教学动画！本工具旨在通过直观、交互的方式，帮助您深入理解波的干涉、衍射和偏振现象。无论您是学生、教师还是物理爱好者，都能通过亲手操作，亲眼观察这些抽象物理概念的动态过程。

---

### 一、 功能说明

本动画模拟了经典的双缝干涉实验，并在此基础上扩展了衍射和偏振模块。它通过**实时计算**和**可视化渲染**，将物理公式转化为生动的图像，让您能够：

1.  **观察**：直观看到光波（或水波）从双缝发出、传播、叠加的全过程。
2.  **探究**：通过调节实验参数，实时观察干涉条纹的变化规律。
3.  **关联**：理解干涉、衍射、偏振三个核心概念之间的联系与区别。

---

### 二、 主要功能

#### 1. 三大探究模块
*   **干涉模块**：展示理想双缝干涉。您可以调节**波长 (λ)**、**双缝间距 (d)** 和**缝屏距离 (L)**，观察明暗相间条纹的实时变化。
*   **干涉+衍射模块**：引入现实因素。增加**单缝宽度 (a)** 参数，展示单缝衍射如何调制双缝干涉图样，理解“缺级”现象。
*   **偏振模块**：探究光的矢量性。可控制两个缝前的**偏振片**角度以及屏前的**检偏器**，观察偏振方向对干涉条纹可见度的影响。

#### 2. 核心交互控件
*   **滑块**：所有物理参数（λ, d, L, a，偏振角）均可通过滑块平滑调节，数值实时显示。
*   **开关**：可随时开启/关闭波阵面、光强曲线、衍射包络线等可视化元素。
*   **播放控制**：可暂停/播放波动动画，便于仔细观察某一瞬间的叠加状态。
*   **标签页**：清晰划分三个知识模块，学习路径由浅入深。

#### 3. 多重可视化反馈
*   **主画布**：左侧显示波源、双缝、波阵面传播；右侧屏幕显示干涉条纹。
*   **光强分布曲线**：在屏幕旁同步绘制理论光强随位置变化的曲线，建立图像与数学表达的直接联系。
*   **实时信息提示**：鼠标悬停在接收屏上任意位置，会弹出该点的**光程差**、**相对光强**和**干涉级次**。
*   **原理公式提示**：画布左上方会根据当前模块动态显示核心物理公式和计算结果（如条纹间距、缺级条件、干涉可见度）。

---

### 三、 设计特色

1.  **符合认知规律**：从“理想干涉”到“实际干涉+衍射”，再到“偏振干涉”，设计符合从简单到复杂、从理想模型到实际应用的认知逻辑。
2.  **实时同步响应**：任何参数的调整，都会立刻在波阵面、干涉条纹和光强曲线上同步、平滑地体现出来，强化“因-果”联系。
3.  **专业视觉编码**：
    *   **色彩**：使用对比鲜明的青色(`#00FFFF`)和洋红色(`#FF00FF`)分别表示来自两个缝的子波，黄色(`#FFFF00`)表示干涉加强区。
    *   **布局**：暗色背景模拟实验室环境，突出光路与条纹。控制面板与显示区域分离，界面整洁。
4.  **教学导向明确**：每个模块都配有“物理原理说明”，动画中关键位置有文字标注，引导用户关注核心概念。

---

### 四、 教学要点（建议探究的问题）

#### 在“干涉”模块中，您可以探究：
*   当**波长 (λ)** 增大时，条纹是变密还是变疏？为什么？
*   当**双缝间距 (d)** 减小时，条纹间距如何变化？这与公式 `Δx = λL/d` 是否一致？
*   中央亮纹（零级明纹）的位置是否随参数改变而移动？

#### 在“干涉+衍射”模块中，您可以探究：
*   保持 `d` 不变，逐渐增大**单缝宽度 (a)**，干涉图样会发生什么变化？（衍射效应增强，包络变窄）
*   当 `d/a` 为整数时，观察是否出现了“缺级”现象？是哪几级干涉条纹消失了？
*   思考：为什么实际实验室中看到的双缝干涉条纹，中间最亮，往两边逐渐变暗？

#### 在“偏振”模块中，您可以探究：
*   保持两个偏振片角度相同（例如都是0°），干涉条纹是否清晰？缓慢旋转其中一个偏振片，条纹会发生什么变化？
*   当两个偏振片角度相差 **90°** 时，干涉条纹为何会消失？这说明了光的什么性质？
*   打开“检偏器”并旋转它，它对已经形成的干涉图样有什么影响？（马吕斯定律的体现）

---

### 五、 使用建议

1.  **初次使用者**：建议按“干涉” → “干涉+衍射” → “偏振”的顺序依次体验。每个模块先点击“重置参数”，然后逐个拖动滑块，观察单一变量变化带来的影响。
2.  **课堂教学**：
    *   **教师演示**：可用于引入概念，通过提问（如“如果波长变长，条纹会怎样？”）让学生预测，然后通过动画验证，激发思考。
    *   **学生探究**：可布置具体的探究任务单，让学生记录不同参数下的条纹间距、缺级条件等，并尝试总结规律。
3.  **自主学习**：
    *   善用**暂停**功能，仔细观察波峰与波峰叠加（加强）、波峰与波谷叠加（减弱）的瞬间。
    *   充分利用**鼠标悬停提示**，将屏幕上具体的“亮纹”位置与显示的“光程差等于整数倍波长”的数值联系起来，深化理解。
    *   尝试用动画验证您从教科书上学到的公式和结论。
4.  **技术提示**：
    *   本动画使用HTML5 Canvas技术，请在Chrome、Firefox、Edge等现代浏览器中打开以获得最佳体验。
    *   如果动画运行不流畅，可以尝试关闭“显示波阵面”以降低渲染负担。

---

**祝您探索愉快，在光与波的奇妙世界中收获知识与灵感！**

> 设计理念：将抽象的物理原理转化为可触摸、可交互的视觉体验，让学习像探索一样有趣。