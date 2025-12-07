# 需求：欧姆定律（I-U图象实时生成，电阻丝温度变化）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向初中或高中物理初学者，旨在帮助学生直观、动态地理解欧姆定律的核心内涵及其在真实电路中的复杂表现。用户的核心需求在于：
1.  **从抽象到具体**：将公式 `I = U/R` 转化为可视化的电流、电压、电阻关系。
2.  **理解动态过程**：观察当电压连续变化时，电流如何随之实时变化，并生成对应的 `I-U` 图象。
3.  **突破理想模型**：探究“电阻丝温度变化”这一关键因素，理解电阻并非恒定不变，从而建立对欧姆定律适用条件的深刻认识。
4.  **主动探究学习**：通过交互操作，自主改变参数（如电压、初始电阻、材料属性），观察不同条件下的现象差异，构建因果关系。

#### 教学设计思路
1.  **核心概念**：
    *   **欧姆定律**：导体中的电流与导体两端的电压成正比，与导体的电阻成反比。
    *   **I-U 图象**：以电压(U)为横轴、电流(I)为纵轴的图线，其斜率（或切线斜率）的倒数反映电阻大小。
    *   **电阻的温度效应**：金属导体的电阻随温度升高而增大。当电流通过电阻丝做功（产生焦耳热）时，其温度升高，电阻值发生变化，导致 `I-U` 图象偏离过原点的直线。

2.  **认知规律**：
    *   **分层递进**：先展示“理想电阻”（电阻恒定）下的线性关系，建立基准认知；再引入“真实电阻丝”（电阻随温度变化），展示非线性关系，形成认知冲突与深化。
    *   **多表征关联**：同步呈现**电路实物模拟图**、**实时数据仪表**、**动态生成的I-U图象**，以及**电阻丝的热效应视觉反馈**，将公式、数据、图像、物理现象紧密连接，促进意义建构。
    *   **对比学习**：提供“理想模式”与“温度效应模式”的切换，允许学生并排或叠加对比两种 `I-U` 图象，突出温度影响的关键性。

3.  **交互设计**：
    *   **控制面板**：清晰、集中的区域提供滑块、按钮等控件。
    *   **实时反馈**：任何操作都立即在电路图、仪表盘和坐标图中得到视觉和数值反馈。
    *   **探索引导**：通过预设问题或挑战（如：“你能让图象弯曲吗？”），引导用户进行有目的的交互。
    *   **节奏可控**：电压变化可“连续扫描”也可“步进调整”，允许用户仔细观察每个状态。

4.  **视觉呈现**：
    *   **主次分明**：电路与坐标图为核心区域，控制面板为辅助区域。
    *   **动态可视化**：
        *   电路中使用流动的光点或箭头表示电流大小与方向。
        *   电阻丝用颜色（如从暗红到亮红/橙）或形变（轻微膨胀）表示温度变化。
        *   `I-U` 图象的绘制过程平滑、连续，像一支笔在实时绘图。
    *   **数据可视化**：电压表、电流表指针摆动，并显示精确数值。

#### 配色方案选择
*   **主色调**：采用深蓝色或深灰色作为背景，营造专注、科技感的实验环境，并能突出前景的亮色元素。
*   **电路元素**：
    *   导线：亮银色或浅灰色。
    *   电阻丝：**动态颜色**，常态为金属灰，随温度升高渐变为暗红、亮红、橙色。这是视觉关键点。
    *   电源、电表：使用简洁的白色或浅色线框图标。
*   **数据与图形**：
    *   `I-U` 图象：
        *   理想电阻线：**亮蓝色实线**，清晰稳定。
        *   温度影响线：**橙色或红色曲线**，与电阻丝颜色呼应，暗示热源。
    *   坐标轴：白色细线。
    *   仪表读数：高对比度的白色或绿色数字/指针。
*   **交互控件**：使用温和的青色或紫色作为滑块、按钮的激活色，与核心图形的蓝色/橙色形成区分又保持和谐。
*   **提示与标签**：使用柔和的黄色或白色，确保可读性。

#### 交互功能列表
1.  **模式选择开关**：在“理想电阻（恒定）”和“真实电阻丝（温度影响）”两种模式间切换。
2.  **电压控制**：
    *   滑块：手动平滑调节电源电压（例如 0V 至 10V）。
    *   扫描按钮：启动自动电压扫描（从0V增至最大值再返回），自动生成完整 `I-U` 图象。
    *   步进按钮：以固定步长（如0.5V）增加/减小电压。
3.  **电路参数调节**（在“真实电阻丝”模式下更关键）：
    *   `初始电阻 R0` 滑块：调节电阻丝在常温（未通电）下的阻值。
    *   `材料热敏感性` 滑块：模拟不同材料（如钨丝 vs 铜丝）的电阻温度系数，控制电阻随温度变化的剧烈程度。
    *   `散热效率` 滑块：模拟散热条件，影响电阻丝达到热平衡的速度和最终温度。
4.  **图形控制**：
    *   “清空图象”按钮：清除当前坐标图上的轨迹，重新开始记录。
    *   “叠加显示”复选框：在“温度效应模式”下，是否同时显示作为对比的“理想线性图象”。
    *   图例：清晰标明每条曲线对应的模式。
5.  **实时数据显示**：
    *   电压 `U`、电流 `I`、当前电阻 `R`、电阻丝温度 `T`（或相对热等级）的数值实时显示。
    *   在 `I-U` 图象上，随鼠标移动或绘图点移动，显示对应点的 `(U, I)` 坐标值。
6.  **视觉反馈联动**：
    *   调节电压时，电路中的“电流流动”动画速度同步变化。
    *   电阻丝颜色/亮度随其计算出的“温度”实时变化。
    *   电压表、电流表指针实时偏转。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>欧姆定律探究：I-U图象与电阻丝温度效应</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: #e2e8f0;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .header {
            text-align: center;
            margin-bottom: 25px;
            width: 100%;
            max-width: 1200px;
        }
        
        h1 {
            color: #60a5fa;
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .subtitle {
            color: #94a3b8;
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            width: 100%;
            max-width: 1200px;
            justify-content: center;
        }
        
        .simulation-area {
            flex: 1;
            min-width: 500px;
            background: rgba(30, 41, 59, 0.7);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(100, 116, 139, 0.2);
        }
        
        .graph-area {
            flex: 1;
            min-width: 500px;
            background: rgba(30, 41, 59, 0.7);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(100, 116, 139, 0.2);
        }
        
        .panel-title {
            color: #38bdf8;
            font-size: 1.5rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid rgba(56, 189, 248, 0.3);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .panel-title svg {
            width: 24px;
            height: 24px;
        }
        
        .circuit-container {
            position: relative;
            width: 100%;
            height: 300px;
            background: rgba(15, 23, 42, 0.5);
            border-radius: 10px;
            margin-bottom: 25px;
            overflow: hidden;
            border: 1px solid rgba(100, 116, 139, 0.3);
        }
        
        #circuitCanvas {
            width: 100%;
            height: 100%;
        }
        
        .controls {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .control-group {
            background: rgba(15, 23, 42, 0.5);
            padding: 18px;
            border-radius: 10px;
            border: 1px solid rgba(100, 116, 139, 0.2);
        }
        
        .control-title {
            color: #a78bfa;
            font-size: 1.1rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .control-row {
            margin-bottom: 15px;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .slider-label {
            min-width: 120px;
            color: #cbd5e1;
            font-size: 0.95rem;
        }
        
        .slider-value {
            min-width: 50px;
            color: #60a5fa;
            font-weight: bold;
            text-align: right;
        }
        
        input[type="range"] {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            background: linear-gradient(to right, #1e40af, #3b82f6, #60a5fa);
            border-radius: 4px;
            outline: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #38bdf8;
            cursor: pointer;
            box-shadow: 0 0 10px rgba(56, 189, 248, 0.7);
            border: 2px solid #ffffff;
        }
        
        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 10px;
        }
        
        button {
            padding: 10px 18px;
            border: none;
            border-radius: 8px;
            background: linear-gradient(to right, #4f46e5, #7c3aed);
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            flex: 1;
            min-width: 120px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
            background: linear-gradient(to right, #6366f1, #8b5cf6);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        button.secondary {
            background: linear-gradient(to right, #0ea5e9, #06b6d4);
        }
        
        .mode-toggle {
            display: flex;
            background: rgba(15, 23, 42, 0.7);
            border-radius: 10px;
            padding: 5px;
            margin-bottom: 20px;
            border: 1px solid rgba(100, 116, 139, 0.3);
        }
        
        .mode-btn {
            flex: 1;
            padding: 12px;
            text-align: center;
            cursor: pointer;
            border-radius: 8px;
            transition: all 0.3s ease;
            font-weight: 600;
        }
        
        .mode-btn.active {
            background: linear-gradient(to right, #4f46e5, #7c3aed);
            color: white;
            box-shadow: 0 4px 8px rgba(79, 70, 229, 0.3);
        }
        
        .graph-container {
            width: 100%;
            height: 400px;
            background: rgba(15, 23, 42, 0.5);
            border-radius: 10px;
            margin-bottom: 25px;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(100, 116, 139, 0.3);
        }
        
        #graphCanvas {
            width: 100%;
            height: 100%;
        }
        
        .data-panel {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .data-box {
            background: rgba(15, 23, 42, 0.7);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            border: 1px solid rgba(100, 116, 139, 0.2);
        }
        
        .data-label {
            color: #94a3b8;
            font-size: 0.9rem;
            margin-bottom: 8px;
        }
        
        .data-value {
            color: #60a5fa;
            font-size: 1.8rem;
            font-weight: bold;
            font-family: 'Courier New', monospace;
        }
        
        .data-unit {
            color: #cbd5e1;
            font-size: 1rem;
            margin-left: 5px;
        }
        
        .legend {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-top: 15px;
            flex-wrap: wrap;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 8px;
            border-radius: 2px;
        }
        
        .legend-text {
            color: #cbd5e1;
            font-size: 0.9rem;
        }
        
        .instructions {
            background: rgba(30, 41, 59, 0.7);
            border-radius: 10px;
            padding: 20px;
            margin-top: 25px;
            max-width: 1200px;
            width: 100%;
            border-left: 4px solid #10b981;
        }
        
        .instructions h3 {
            color: #10b981;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .instructions ul {
            padding-left: 20px;
            color: #cbd5e1;
            line-height: 1.6;
        }
        
        .instructions li {
            margin-bottom: 8px;
        }
        
        @media (max-width: 1100px) {
            .container {
                flex-direction: column;
            }
            
            .simulation-area, .graph-area {
                min-width: 100%;
            }
        }
        
        @media (max-width: 600px) {
            .controls {
                grid-template-columns: 1fr;
            }
            
            .data-panel {
                grid-template-columns: repeat(2, 1fr);
            }
            
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>欧姆定律探究实验</h1>
        <p class="subtitle">I-U图象实时生成与电阻丝温度效应观察 | 通过交互理解理想模型与真实电路的差异</p>
    </div>
    
    <div class="container">
        <div class="simulation-area">
            <div class="panel-title">
                <svg viewBox="0 0 24 24" fill="currentColor">
                    <path d="M13 9h-2V7h2m0 10h-2v-6h2m-1-9A10 10 0 002 12a10 10 0 0010 10 10 10 0 0010-10A10 10 0 0012 2z"/>
                </svg>
                <span>电路仿真与参数控制</span>
            </div>
            
            <div class="mode-toggle">
                <div class="mode-btn active" id="modeIdeal">理想电阻模式</div>
                <div class="mode-btn" id="modeReal">温度效应模式</div>
            </div>
            
            <div class="circuit-container">
                <canvas id="circuitCanvas"></canvas>
            </div>
            
            <div class="controls">
                <div class="control-group">
                    <div class="control-title">
                        <svg viewBox="0 0 24 24" fill="currentColor" width="20" height="20">
                            <path d="M13 19V7H15V19H13M9 19V7H11V19H9Z"/>
                        </svg>
                        <span>电压控制</span>
                    </div>
                    
                    <div class="control-row">
                        <div class="slider-container">
                            <span class="slider-label">电源电压 (U)</span>
                            <input type="range" id="voltageSlider" min="0" max="10" step="0.1" value="0">
                            <span class="slider-value" id="voltageValue">0.0 V</span>
                        </div>
                    </div>
                    
                    <div class="button-group">
                        <button id="scanBtn" class="secondary">自动扫描电压</button>
                        <button id="stepUpBtn">+0.5V</button>
                        <button id="stepDownBtn">-0.5V</button>
                    </div>
                </div>
                
                <div class="control-group" id="tempControlGroup">
                    <div class="control-title">
                        <svg viewBox="0 0 24 24" fill="currentColor" width="20" height="20">
                            <path d="M15 13V5A3 3 0 009 5V13A5 5 0 105 13V7A1 1 0 013 7V13A7 7 0 0017 13V9A1 1 0 0119 9V13H21V15H17A5 5 0 0111 15V5A1 1 0 0113 5V13A3 3 0 0015 13Z"/>
                        </svg>
                        <span>电阻丝参数</span>
                    </div>
                    
                    <div class="control-row">
                        <div class="slider-container">
                            <span class="slider-label">初始电阻 (R₀)</span>
                            <input type="range" id="resistanceSlider" min="1" max="10" step="0.1" value="5">
                            <span class="slider-value" id="resistanceValue">5.0 Ω</span>
                        </div>
                    </div>
                    
                    <div class="control-row">
                        <div class="slider-container">
                            <span class="slider-label">热敏感性</span>
                            <input type="range" id="sensitivitySlider" min="0.1" max="2" step="0.1" value="1">
                            <span class="slider-value" id="sensitivityValue">1.0</span>
                        </div>
                    </div>
                    
                    <div class="control-row">
                        <div class="slider-container">
                            <span class="slider-label">散热效率</span>
                            <input type="range" id="coolingSlider" min="0.5" max="3" step="0.1" value="1.5">
                            <span class="slider-value" id="coolingValue">1.5</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="graph-area">
            <div class="panel-title">
                <svg viewBox="0 0 24 24" fill="currentColor">
                    <path d="M5,19H19V17H5V19M19,5V9H5V5H19M19,11V15H5V11H19M3,21H21V3H3V21Z"/>
                </svg>
                <span>I-U图象与实时数据</span>
            </div>
            
            <div class="graph-container">
                <canvas id="graphCanvas"></canvas>
            </div>
            
            <div class="data-panel">
                <div class="data-box">
                    <div class="data-label">电压 (U)</div>
                    <div class="data-value" id="displayVoltage">0.00<span class="data-unit">V</span></div>
                </div>
                <div class="data-box">
                    <div class="data-label">电流 (I)</div>
                    <div class="data-value" id="displayCurrent">0.00<span class="data-unit">A</span></div>
                </div>
                <div class="data-box">
                    <div class="data-label">电阻 (R)</div>
                    <div class="data-value" id="displayResistance">5.00<span class="data-unit">Ω</span></div>
                </div>
                <div class="data-box">
                    <div class="data-label">温度等级</div>
                    <div class="data-value" id="displayTemperature">1.00<span class="data-unit"></span></div>
                </div>
            </div>
            
            <div class="button-group" style="margin-top: 20px;">
                <button id="clearGraphBtn">清空图象</button>
                <button id="toggleIdealBtn">显示理想曲线</button>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #60a5fa;"></div>
                    <div class="legend-text">理想电阻 (I-U线性关系)</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #f97316;"></div>
                    <div class="legend-text">温度效应 (I-U曲线)</div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="instructions">
        <h3>
            <svg viewBox="0 0 24 24" fill="currentColor" width="24" height="24">
                <path d="M13.5,4A1.5,1.5 0 0,0 12,5.5A1.5,1.5 0 0,0 13.5,7A1.5,1.5 0 0,0 15,5.5A1.5,1.5 0 0,0 13.5,4M13.14,8.77C11.95,8.87 8.7,11.46 8.7,11.46C8.5,11.61 8.56,11.6 8.72,11.88C8.88,12.15 8.86,12.17 9.05,12.04C9.25,11.91 9.58,11.7 10.13,11.36C12.25,10 10.47,13.14 9.56,18.43C9.2,21.05 11.56,19.7 12.17,19.3C12.77,18.91 14.38,17.8 14.54,17.69C14.76,17.54 14.6,17.42 14.43,17.17C14.31,17 14.19,17.12 14.19,17.12C13.54,17.55 12.35,18.45 12.19,17.88C12,17.31 13.22,13.4 13.89,10.71C14,10.07 14.3,8.67 13.14,8.77Z"/>
            </svg>
            实验指导
        </h3>
        <ul>
            <li><strong>理想电阻模式</strong>：电阻值恒定，I-U图象为过原点的直线，符合欧姆定律 I = U/R。</li>
            <li><strong>温度效应模式</strong>：电阻丝发热导致电阻增大，I-U图象为曲线，电流增长随电压升高而变慢。</li>
            <li>使用"自动扫描电压"观察完整I-U图象的生成过程，对比两种模式的差异。</li>
            <li>调节"热敏感性"和"散热效率"参数，观察它们对I-U曲线形状的影响。</li>
            <li>点击"显示理想曲线"可在温度效应模式下叠加显示理想直线作为对比。</li>
        </ul>
    </div>

    <script>
        // 全局变量
        let mode = 'ideal'; // 'ideal' 或 'real'
        let voltage = 0; // 电压 (V)
        let resistance = 5; // 初始电阻 (Ω)
        let currentResistance = 5; // 当前电阻 (Ω)，考虑温度效应
        let temperature = 1.0; // 温度等级 (1.0为常温)
        let sensitivity = 1.0; // 热敏感性系数
        let cooling = 1.5; // 散热效率系数
        
        let isScanning = false;
        let scanDirection = 1; // 1: 增加, -1: 减少
        let scanSpeed = 0.02; // 扫描速度 (V/帧)
        
        let showIdealCurve = true;
        
        // 存储数据点用于绘图
        let dataPoints = {
            ideal: [],
            real: []
        };
        
        // 获取Canvas元素和上下文
        const circuitCanvas = document.getElementById('circuitCanvas');
        const circuitCtx = circuitCanvas.getContext('2d');
        
        const graphCanvas = document.getElementById('graphCanvas');
        const graphCtx = graphCanvas.getContext('2d');
        
        // 初始化Canvas尺寸
        function initCanvas() {
            const circuitContainer = document.querySelector('.circuit-container');
            circuitCanvas.width = circuitContainer.clientWidth;
            circuitCanvas.height = circuitContainer.clientHeight;
            
            const graphContainer = document.querySelector('.graph-container');
            graphCanvas.width = graphContainer.clientWidth;
            graphCanvas.height = graphContainer.clientHeight;
        }
        
        // 初始化事件监听
        function initEventListeners() {
            // 模式切换
            document.getElementById('modeIdeal').addEventListener('click', () => {
                setMode('ideal');
            });
            
            document.getElementById('modeReal').addEventListener('click', () => {
                setMode('real');
            });
            
            // 电压控制
            const voltageSlider = document.getElementById('voltageSlider');
            voltageSlider.addEventListener('input', () => {
                voltage = parseFloat(voltageSlider.value);
                document.getElementById('voltageValue').textContent = voltage.toFixed(1) + ' V';
                updateCircuit();
            });
            
            // 参数控制
            document.getElementById('resistanceSlider').addEventListener('input', function() {
                resistance = parseFloat(this.value);
                currentResistance = resistance;
                document.getElementById('resistanceValue').textContent = resistance.toFixed(1) + ' Ω';
                updateCircuit();
            });
            
            document.getElementById('sensitivitySlider').addEventListener('input', function() {
                sensitivity = parseFloat(this.value);
                document.getElementById('sensitivityValue').textContent = sensitivity.toFixed(1);
                updateCircuit();
            });
            
            document.getElementById('coolingSlider').addEventListener('input', function() {
                cooling = parseFloat(this.value);
                document.getElementById('coolingValue').textContent = cooling.toFixed(1);
                updateCircuit();
            });
            
            // 按钮控制
            document.getElementById('scanBtn').addEventListener('click', toggleScan);
            document.getElementById('stepUpBtn').addEventListener('click', () => stepVoltage(0.5));
            document.getElementById('stepDownBtn').addEventListener('click', () => stepVoltage(-0.5));
            document.getElementById('clearGraphBtn').addEventListener('click', clearGraph);
            document.getElementById('toggleIdealBtn').addEventListener('click', toggleIdealCurve);
            
            // 窗口大小变化时调整Canvas
            window.addEventListener('resize', initCanvas);
        }
        
        // 设置模式
        function setMode(newMode) {
            mode = newMode;
            
            // 更新UI
            document.getElementById('modeIdeal').classList.toggle('active', mode === 'ideal');
            document.getElementById('modeReal').classList.toggle('active', mode === 'real');
            
            // 温度效应模式下的控制组
            const tempControlGroup = document.getElementById('tempControlGroup');
            tempControlGroup.style.opacity = mode === 'real' ? '1' : '0.6';
            tempControlGroup.style.pointerEvents = mode === 'real' ? 'auto' : 'none';
            
            // 重置温度
            temperature = 1.0;
            currentResistance = resistance;
            
            updateCircuit();
        }
        
        // 步进电压
        function stepVoltage(step) {
            const voltageSlider = document.getElementById('voltageSlider');
            let newVoltage = voltage + step;
            
            // 限制范围
            newVoltage = Math.max(0, Math.min(10, newVoltage));
            
            voltage = newVoltage;
            voltageSlider.value = voltage;
            document.getElementById('voltageValue').textContent = voltage.toFixed(1) + ' V';
            
            updateCircuit();
        }
        
        // 切换自动扫描
        function toggleScan() {
            isScanning = !isScanning;
            const scanBtn = document.getElementById('scanBtn');
            scanBtn.textContent = isScanning ? '停止扫描' : '自动扫描电压';
            scanBtn.classList.toggle('secondary', !isScanning);
            
            if (isScanning) {
                scanDirection = 1;
            }
        }
        
        // 清空图象
        function clearGraph() {
            dataPoints.ideal = [];
            dataPoints.real = [];
            drawGraph();
        }
        
        // 切换理想曲线显示
        function toggleIdealCurve() {
            showIdealCurve = !showIdealCurve;
            const toggleBtn = document.getElementById('toggleIdealBtn');
            toggleBtn.textContent = showIdealCurve ? '隐藏理想曲线' : '显示理想曲线';
            drawGraph();
        }
        
        // 更新电路状态
        function updateCircuit() {
            // 计算电流
            let current;
            
            if (mode === 'ideal') {
                // 理想模式：电阻恒定
                currentResistance = resistance;
                current = voltage / currentResistance;
                
                // 存储数据点
                if (voltage > 0 || dataPoints.ideal.length === 0) {
                    addDataPoint('ideal', voltage, current);
                }
            } else {
                // 温度效应模式：电阻随温度变化
                // 计算温度变化 (简化模型)
                const power = voltage * voltage / currentResistance; // 功率 P = U²/R
                const heating = power * sensitivity * 0.01; // 加热效应
                const coolingEffect = (temperature - 1.0) * cooling * 0.01; // 冷却效应
                
                temperature += heating - coolingEffect;
                temperature = Math.max(1.0, Math.min(3.0, temperature)); // 限制温度范围
                
                // 电阻随温度变化 (线性近似)
                currentResistance = resistance * (1 + 0.2 * (temperature - 1.0));
                current = voltage / currentResistance;
                
                // 存储数据点
                if (voltage > 0 || dataPoints.real.length === 0) {
                    addDataPoint('real', voltage, current);
                }
            }
            
            // 更新数据显示
            document.getElementById('displayVoltage').innerHTML = voltage.toFixed(2) + '<span class="data-unit">V</span>';
            document.getElementById('displayCurrent').innerHTML = current.toFixed(2) + '<span class="data-unit">A</span>';
            document.getElementById('displayResistance').innerHTML = currentResistance.toFixed(2) + '<span class="data-unit">Ω</span>';
            document.getElementById('displayTemperature').innerHTML = temperature.toFixed(2);
            
            // 重绘
            drawCircuit();
            drawGraph();
        }
        
        // 添加数据点
        function addDataPoint(type, voltage, current) {
            const points = dataPoints[type];
            points.push({ voltage, current });
            
            // 限制数据点数量，避免性能问题
            if (points.length > 200) {
                points.shift();
            }
        }
        
        // 绘制电路
        function drawCircuit() {
            const width = circuitCanvas.width;
            const height = circuitCanvas.height;
            
            // 清空画布
            circuitCtx.clearRect(0, 0, width, height);
            
            // 计算电路元件位置
            const centerX = width / 2;
            const centerY = height / 2;
            const circuitWidth = Math.min(width, height) * 0.7;
            const circuitHeight = circuitWidth * 0.4;
            
            const leftX = centerX - circuitWidth / 2;
            const rightX = centerX + circuitWidth / 2;
            const topY = centerY - circuitHeight / 2;
            const bottomY = centerY + circuitHeight / 2;
            
            // 绘制导线
            circuitCtx.strokeStyle = '#cbd5e1';
            circuitCtx.lineWidth = 3;
            circuitCtx.lineCap = 'round';
            
            // 左上到左下
            circuitCtx.beginPath();
            circuitCtx.moveTo(leftX, topY);
            circuitCtx.lineTo(leftX, bottomY);
            circuitCtx.stroke();
            
            // 左下到右下
            circuitCtx.beginPath();
            circuitCtx.moveTo(leftX, bottomY);
            circuitCtx.lineTo(rightX, bottomY);
            circuitCtx.stroke();
            
            // 右下到右上
            circuitCtx.beginPath();
            circuitCtx.moveTo(rightX, bottomY);
            circuitCtx.lineTo(rightX, topY);
            circuitCtx.stroke();
            
            // 右上到左上
            circuitCtx.beginPath();
            circuitCtx.moveTo(rightX, topY);
            circuitCtx.lineTo(leftX, topY);
            circuitCtx.stroke();
            
            // 绘制电源
            const batteryWidth = 30;
            const batteryHeight = 50;
            const batteryX = leftX + 40;
            const batteryY = centerY - batteryHeight / 2;
            
            // 电池外壳
            circuitCtx.fillStyle = '#475569';
            circuitCtx.fillRect(batteryX, batteryY, batteryWidth, batteryHeight);
            
            // 电池正负极
            circuitCtx.fillStyle = '#ef4444'; // 红色负极
            circuitCtx.fillRect(batteryX + 5, batteryY + 10, batteryWidth - 10, 10);
            
            circuitCtx.fillStyle = '#3b82f6'; // 蓝色正极
            circuitCtx.fillRect(batteryX + 5, batteryY + batteryHeight - 20, batteryWidth - 10, 10);
            
            // 电池标签
            circuitCtx.fillStyle = '#ffffff';
            circuitCtx.font = '12px Arial';
            circuitCtx.textAlign = 'center';
            circuitCtx.fillText('电源', batteryX + batteryWidth / 2, batteryY + batteryHeight / 2 + 4);
            
            // 绘制电阻丝
            const resistorWidth = 80;
            const resistorHeight = 40;
            const resistorX = rightX - 100;
            const resistorY = centerY - resistorHeight / 2;
            
            // 根据温度计算电阻丝颜色
            let resistorColor;
            if (temperature < 1.5) {
                // 冷色到暖色
                const t = (temperature - 1.0) / 0.5;
                const r = Math.floor(150 + 50 * t);
                const g = Math.floor(150 - 50 * t);
                const b = Math.floor(150 - 100 * t);
                resistorColor = `rgb(${r}, ${g}, ${b})`;
            } else {
                // 暖色到热色
                const t = Math.min(1, (temperature - 1.5) / 1.5);
                const r = Math.floor(200 + 55 * t);
                const g = Math.floor(100 - 80 * t);
                const b = Math.floor(50 - 50 * t);
                resistorColor = `rgb(${r}, ${g}, ${b})`;
            }
            
            // 电阻丝主体
            circuitCtx.fillStyle = resistorColor;
            circuitCtx.fillRect(resistorX, resistorY, resistorWidth, resistorHeight);
            
            // 电阻丝线圈图案
            circuitCtx.strokeStyle = '#1e293b';
            circuitCtx.lineWidth = 2;
            const coilCount = 6;
            const coilSpacing = resistorWidth / (coilCount + 1);
            
            circuitCtx.beginPath();
            for (let i = 1; i <= coilCount; i++) {
                const x = resistorX + i * coilSpacing;
                circuitCtx.moveTo(x, resistorY);
                circuitCtx.lineTo(x, resistorY + resistorHeight);
            }
            circuitCtx.stroke();
            
            // 电阻丝标签
            circuitCtx.fillStyle = '#ffffff';
            circuitCtx.font = '12px Arial';
            circuitCtx.textAlign = 'center';
            circuitCtx.fillText('电阻丝', resistorX + resistorWidth / 2, resistorY + resistorHeight / 2 + 4);
            
            // 绘制电流流动效果
            if (voltage > 0) {
                // 计算电流流动位置
                const flowSpeed = 2 + current * 5; // 流速与电流大小相关
                const flowOffset = (Date.now() / 50) % (circuitWidth * 2 + circuitHeight * 2);
                
                circuitCtx.strokeStyle = '#60a5fa';
                circuitCtx.lineWidth = 4;
                circuitCtx.lineCap = 'round';
                
                // 根据偏移量确定流动点的位置
                let flowX, flowY;
                
                if (flowOffset < circuitWidth) {
                    // 上边导线
                    flowX = leftX + flowOffset;
                    flowY = topY;
                } else if (flowOffset < circuitWidth + circuitHeight) {
                    // 右边导线
                    flowX = rightX;
                    flowY = topY + (flowOffset - circuitWidth);
                } else if (flowOffset < circuitWidth * 2 + circuitHeight) {
                    // 下边导线
                    flowX = rightX - (flowOffset - circuitWidth - circuitHeight);
                    flowY = bottomY;
                } else {
                    // 左边导线
                    flowX = leftX;
                    flowY = bottomY - (flowOffset - circuitWidth * 2 - circuitHeight);
                }
                
                // 绘制流动点
                circuitCtx.beginPath();
                circuitCtx.arc(flowX, flowY, 5, 0, Math.PI * 2);
                circuitCtx.fillStyle = '#60a5fa';
                circuitCtx.fill();
                
                // 绘制流动轨迹
                const trailLength = 20;
                circuitCtx.beginPath();
                for (let i = 0; i < trailLength; i++) {
                    const trailOffset = flowOffset - i * 2;
                    let trailX, trailY;
                    
                    if (trailOffset < 0) trailOffset += circuitWidth * 2 + circuitHeight * 2;
                    
                    if (trailOffset < circuitWidth) {
                        trailX = leftX + trailOffset;
                        trailY = topY;
                    } else if (trailOffset < circuitWidth + circuitHeight) {
                        trailX = rightX;
                        trailY = topY + (trailOffset - circuitWidth);
                    } else if (trailOffset < circuitWidth * 2 + circuitHeight) {
                        trailX = rightX - (trailOffset - circuitWidth - circuitHeight);
                        trailY = bottomY;
                    } else {
                        trailX = leftX;
                        trailY = bottomY - (trailOffset - circuitWidth * 2 - circuitHeight);
                    }
                    
                    if (i === 0) {
                        circuitCtx.moveTo(trailX, trailY);
                    } else {
                        circuitCtx.lineTo(trailX, trailY);
                    }
                }
                circuitCtx.stroke();
            }
            
            // 绘制电表
            const meterX
<!--检测到代码截断，自动续写中...-->
= centerX;
            const meterY = topY - 40;
            const meterRadius = 20;
            
            // 电压表
            circuitCtx.fillStyle = '#1e293b';
            circuitCtx.beginPath();
            circuitCtx.arc(meterX - 50, meterY, meterRadius, 0, Math.PI * 2);
            circuitCtx.fill();
            
            circuitCtx.fillStyle = '#ffffff';
            circuitCtx.font = '10px Arial';
            circuitCtx.textAlign = 'center';
            circuitCtx.fillText('V', meterX - 50, meterY + 4);
            
            // 电流表
            circuitCtx.fillStyle = '#1e293b';
            circuitCtx.beginPath();
            circuitCtx.arc(meterX + 50, meterY, meterRadius, 0, Math.PI * 2);
            circuitCtx.fill();
            
            circuitCtx.fillStyle = '#ffffff';
            circuitCtx.font = '10px Arial';
            circuitCtx.textAlign = 'center';
            circuitCtx.fillText('A', meterX + 50, meterY + 4);
            
            // 绘制表针
            const voltageAngle = Math.PI * 0.2 + (voltage / 10) * Math.PI * 0.6;
            const currentAngle = Math.PI * 0.2 + (voltage / (10 * resistance)) * Math.PI * 0.6;
            
            // 电压表指针
            circuitCtx.strokeStyle = '#10b981';
            circuitCtx.lineWidth = 2;
            circuitCtx.beginPath();
            circuitCtx.moveTo(meterX - 50, meterY);
            circuitCtx.lineTo(
                meterX - 50 + Math.cos(voltageAngle) * (meterRadius - 3),
                meterY + Math.sin(voltageAngle) * (meterRadius - 3)
            );
            circuitCtx.stroke();
            
            // 电流表指针
            circuitCtx.strokeStyle = '#f59e0b';
            circuitCtx.lineWidth = 2;
            circuitCtx.beginPath();
            circuitCtx.moveTo(meterX + 50, meterY);
            circuitCtx.lineTo(
                meterX + 50 + Math.cos(currentAngle) * (meterRadius - 3),
                meterY + Math.sin(currentAngle) * (meterRadius - 3)
            );
            circuitCtx.stroke();
            
            // 绘制模式标签
            circuitCtx.fillStyle = mode === 'ideal' ? '#60a5fa' : '#f97316';
            circuitCtx.font = 'bold 16px Arial';
            circuitCtx.textAlign = 'center';
            circuitCtx.fillText(
                mode === 'ideal' ? '理想电阻模式' : '温度效应模式',
                centerX,
                bottomY + 30
            );
        }
        
        // 绘制I-U图象
        function drawGraph() {
            const width = graphCanvas.width;
            const height = graphCanvas.height;
            
            // 清空画布
            graphCtx.clearRect(0, 0, width, height);
            
            // 设置坐标系参数
            const margin = 60;
            const graphWidth = width - 2 * margin;
            const graphHeight = height - 2 * margin;
            
            const maxVoltage = 10;
            const maxCurrent = 2; // 最大电流 2A
            
            // 绘制坐标轴
            graphCtx.strokeStyle = '#64748b';
            graphCtx.lineWidth = 2;
            
            // X轴 (电压)
            graphCtx.beginPath();
            graphCtx.moveTo(margin, height - margin);
            graphCtx.lineTo(width - margin, height - margin);
            graphCtx.stroke();
            
            // Y轴 (电流)
            graphCtx.beginPath();
            graphCtx.moveTo(margin, margin);
            graphCtx.lineTo(margin, height - margin);
            graphCtx.stroke();
            
            // 坐标轴箭头
            // X轴箭头
            graphCtx.beginPath();
            graphCtx.moveTo(width - margin, height - margin);
            graphCtx.lineTo(width - margin - 10, height - margin - 5);
            graphCtx.lineTo(width - margin - 10, height - margin + 5);
            graphCtx.closePath();
            graphCtx.fillStyle = '#64748b';
            graphCtx.fill();
            
            // Y轴箭头
            graphCtx.beginPath();
            graphCtx.moveTo(margin, margin);
            graphCtx.lineTo(margin - 5, margin + 10);
            graphCtx.lineTo(margin + 5, margin + 10);
            graphCtx.closePath();
            graphCtx.fillStyle = '#64748b';
            graphCtx.fill();
            
            // 坐标轴标签
            graphCtx.fillStyle = '#cbd5e1';
            graphCtx.font = 'bold 16px Arial';
            graphCtx.textAlign = 'center';
            graphCtx.fillText('电压 U (V)', width / 2, height - margin / 3);
            
            graphCtx.save();
            graphCtx.translate(margin / 3, height / 2);
            graphCtx.rotate(-Math.PI / 2);
            graphCtx.fillText('电流 I (A)', 0, 0);
            graphCtx.restore();
            
            // 绘制网格和刻度
            graphCtx.strokeStyle = 'rgba(100, 116, 139, 0.3)';
            graphCtx.lineWidth = 1;
            graphCtx.fillStyle = '#94a3b8';
            graphCtx.font = '12px Arial';
            graphCtx.textAlign = 'center';
            
            // X轴刻度
            for (let i = 0; i <= maxVoltage; i += 2) {
                const x = margin + (i / maxVoltage) * graphWidth;
                
                graphCtx.beginPath();
                graphCtx.moveTo(x, height - margin - 5);
                graphCtx.lineTo(x, height - margin + 5);
                graphCtx.stroke();
                
                graphCtx.fillText(i.toString(), x, height - margin + 20);
            }
            
            // Y轴刻度
            for (let i = 0; i <= maxCurrent; i += 0.5) {
                const y = height - margin - (i / maxCurrent) * graphHeight;
                
                graphCtx.beginPath();
                graphCtx.moveTo(margin - 5, y);
                graphCtx.lineTo(margin + 5, y);
                graphCtx.stroke();
                
                graphCtx.textAlign = 'right';
                graphCtx.fillText(i.toFixed(1), margin - 10, y + 4);
                graphCtx.textAlign = 'center';
            }
            
            // 绘制原点标记
            graphCtx.fillStyle = '#ffffff';
            graphCtx.beginPath();
            graphCtx.arc(margin, height - margin, 4, 0, Math.PI * 2);
            graphCtx.fill();
            graphCtx.fillText('O', margin - 15, height - margin + 15);
            
            // 绘制理想电阻曲线 (如果显示)
            if (showIdealCurve && dataPoints.ideal.length > 0) {
                drawCurve('ideal', '#60a5fa');
            }
            
            // 绘制温度效应曲线
            if (dataPoints.real.length > 0) {
                drawCurve('real', '#f97316');
            }
            
            // 绘制当前数据点
            if (voltage > 0) {
                const current = voltage / currentResistance;
                const pointX = margin + (voltage / maxVoltage) * graphWidth;
                const pointY = height - margin - (current / maxCurrent) * graphHeight;
                
                // 绘制点
                graphCtx.fillStyle = mode === 'ideal' ? '#60a5fa' : '#f97316';
                graphCtx.beginPath();
                graphCtx.arc(pointX, pointY, 8, 0, Math.PI * 2);
                graphCtx.fill();
                
                // 绘制十字线
                graphCtx.strokeStyle = 'rgba(255, 255, 255, 0.5)';
                graphCtx.lineWidth = 1;
                graphCtx.setLineDash([5, 5]);
                
                graphCtx.beginPath();
                graphCtx.moveTo(pointX, margin);
                graphCtx.lineTo(pointX, height - margin);
                graphCtx.moveTo(margin, pointY);
                graphCtx.lineTo(width - margin, pointY);
                graphCtx.stroke();
                
                graphCtx.setLineDash([]);
                
                // 显示坐标值
                graphCtx.fillStyle = '#ffffff';
                graphCtx.font = '14px Arial';
                graphCtx.textAlign = 'left';
                graphCtx.fillText(
                    `(${voltage.toFixed(2)}V, ${current.toFixed(2)}A)`,
                    pointX + 10,
                    pointY - 10
                );
            }
            
            // 绘制图例
            const legendX = width - margin;
            const legendY = margin + 30;
            
            if (showIdealCurve) {
                graphCtx.fillStyle = '#60a5fa';
                graphCtx.fillRect(legendX - 100, legendY, 15, 3);
                graphCtx.fillStyle = '#cbd5e1';
                graphCtx.font = '12px Arial';
                graphCtx.textAlign = 'left';
                graphCtx.fillText('理想电阻', legendX - 80, legendY + 8);
            }
            
            graphCtx.fillStyle = '#f97316';
            graphCtx.fillRect(legendX - 100, legendY + 20, 15, 3);
            graphCtx.fillStyle = '#cbd5e1';
            graphCtx.font = '12px Arial';
            graphCtx.textAlign = 'left';
            graphCtx.fillText('温度效应', legendX - 80, legendY + 28);
        }
        
        // 绘制曲线
        function drawCurve(type, color) {
            const width = graphCanvas.width;
            const height = graphCanvas.height;
            const margin = 60;
            const graphWidth = width - 2 * margin;
            const graphHeight = height - 2 * margin;
            
            const maxVoltage = 10;
            const maxCurrent = 2;
            
            const points = dataPoints[type];
            
            if (points.length < 2) return;
            
            graphCtx.strokeStyle = color;
            graphCtx.lineWidth = 3;
            graphCtx.lineJoin = 'round';
            graphCtx.lineCap = 'round';
            
            graphCtx.beginPath();
            
            // 移动到第一个点
            const firstPoint = points[0];
            const firstX = margin + (firstPoint.voltage / maxVoltage) * graphWidth;
            const firstY = height - margin - (firstPoint.current / maxCurrent) * graphHeight;
            graphCtx.moveTo(firstX, firstY);
            
            // 绘制曲线
            for (let i = 1; i < points.length; i++) {
                const point = points[i];
                const x = margin + (point.voltage / maxVoltage) * graphWidth;
                const y = height - margin - (point.current / maxCurrent) * graphHeight;
                
                graphCtx.lineTo(x, y);
            }
            
            graphCtx.stroke();
            
            // 绘制数据点
            if (points.length > 1) {
                const lastPoint = points[points.length - 1];
                const lastX = margin + (lastPoint.voltage / maxVoltage) * graphWidth;
                const lastY = height - margin - (lastPoint.current / maxCurrent) * graphHeight;
                
                graphCtx.fillStyle = color;
                graphCtx.beginPath();
                graphCtx.arc(lastX, lastY, 5, 0, Math.PI * 2);
                graphCtx.fill();
            }
        }
        
        // 动画循环
        function animate() {
            // 自动扫描逻辑
            if (isScanning) {
                let newVoltage = voltage + scanDirection * scanSpeed;
                
                // 到达边界时改变方向
                if (newVoltage >= 10) {
                    newVoltage = 10;
                    scanDirection = -1;
                } else if (newVoltage <= 0) {
                    newVoltage = 0;
                    scanDirection = 1;
                }
                
                voltage = newVoltage;
                
                // 更新UI
                document.getElementById('voltageSlider').value = voltage;
                document.getElementById('voltageValue').textContent = voltage.toFixed(1) + ' V';
                
                updateCircuit();
            }
            
            requestAnimationFrame(animate);
        }
        
        // 初始化
        function init() {
            initCanvas();
            initEventListeners();
            updateCircuit();
            animate();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 欧姆定律交互式教学动画使用指南

欢迎使用“欧姆定律探究：I-U图象实时生成与电阻丝温度效应”交互式教学动画！本工具旨在通过直观的视觉呈现和丰富的交互体验，帮助您深入理解欧姆定律的核心原理及其在真实电路中的表现。

---

### 一、功能说明

本动画模拟了一个完整的电路实验环境，包含以下核心组件：

1. **电路仿真区**：可视化展示包含电源、电阻丝、导线和电表的完整电路
2. **I-U图象区**：实时绘制电流-电压关系曲线，直观展示欧姆定律的数学表达
3. **参数控制面板**：提供多种可调节参数，支持个性化探究实验
4. **实时数据显示**：精确显示电压、电流、电阻和温度等级的数值变化

### 二、主要功能

#### 1. 双模式切换
- **理想电阻模式**：模拟电阻值恒定的理想情况，I-U图象为过原点的直线
- **温度效应模式**：模拟真实电阻丝发热导致电阻变化的情况，I-U图象为曲线

#### 2. 电压控制方式
- **手动滑块调节**：精细控制电压从0V到10V的变化
- **步进调节**：以0.5V为步长精确增减电压
- **自动扫描**：自动完成电压从0V到10V再返回的完整扫描过程

#### 3. 电阻丝参数调节（温度效应模式下）
- **初始电阻**：调节电阻丝在常温下的阻值（1-10Ω）
- **热敏感性**：模拟不同材料的电阻温度系数（如钨丝的高敏感性）
- **散热效率**：模拟不同散热条件对温度平衡的影响

#### 4. 图形控制功能
- **清空图象**：重置I-U坐标图，开始新的数据记录
- **显示/隐藏理想曲线**：在温度效应模式下叠加显示理想直线作为对比
- **实时坐标显示**：鼠标悬停时显示曲线上任意点的(U, I)坐标值

### 三、设计特色

#### 1. 多表征同步呈现
- **物理现象可视化**：电阻丝颜色随温度实时变化（金属灰→暗红→亮红→橙色）
- **电流流动动画**：光点沿电路流动，速度与电流大小成正比
- **电表指针偏转**：电压表和电流表指针实时反映测量值
- **数据图形联动**：电路状态、数值显示和I-U图象完全同步更新

#### 2. 认知分层设计
- **从简单到复杂**：先建立理想模型的认知，再引入温度效应的复杂性
- **从观察到解释**：先看到现象（曲线弯曲），再探究原因（电阻变化）
- **从具体到抽象**：将具体电路现象与抽象的I-U图象建立联系

#### 3. 探究式学习支持
- **参数自由调节**：允许改变多个变量，观察其对系统的综合影响
- **对比实验设计**：支持理想与真实情况的并排对比
- **即时反馈机制**：任何操作都能立即看到可视化结果

### 四、教学要点

#### 核心概念理解
1. **欧姆定律的本质**：在理想条件下，导体中的电流与电压成正比（I ∝ U）
2. **I-U图象的意义**：
   - 直线的斜率反映电阻大小（斜率越大，电阻越小）
   - 过原点表示电压为零时电流为零
3. **电阻的温度效应**：
   - 金属导体的电阻随温度升高而增大
   - 电流通过电阻做功产生焦耳热（Q = I²Rt）
   - 热平衡：产热速率 = 散热速率时达到稳定温度

#### 关键观察点
1. **理想模式**：
   - 电阻值始终保持不变
   - I-U图象为完美的直线
   - 符合公式 I = U/R

2. **温度效应模式**：
   - 电阻值随电压升高而增大
   - I-U图象向上弯曲（斜率逐渐减小）
   - 电流增长速率随电压升高而变慢
   - 电阻丝颜色变化反映温度变化

#### 探究性问题引导
1. **基础观察**：
   - 在理想模式下，改变电压时电流如何变化？
   - I-U图象的斜率代表什么物理量？

2. **对比分析**：
   - 两种模式下的I-U图象有何不同？
   - 为什么温度效应模式下的图象会弯曲？

3. **深入探究**：
   - 调节“热敏感性”参数会如何影响曲线形状？
   - “散热效率”如何影响电阻丝的最终温度？
   - 初始电阻的大小对曲线有何影响？

### 五、使用建议

#### 课堂教学应用
1. **演示教学**：
   - 教师操作，全班观察
   - 分步骤展示：理想情况→引入温度效应→参数影响
   - 关键节点暂停讲解，强调物理原理

2. **小组探究**：
   - 每组分配不同的探究任务
   - 例如：“探究不同初始电阻对曲线的影响”
   - 小组汇报发现，全班讨论

3. **个人练习**：
   - 学生自主操作，完成实验报告
   - 记录不同参数下的实验数据
   - 分析数据，得出结论

#### 学习路径建议
1. **第一阶段：熟悉工具**（约5分钟）
   - 尝试所有控制滑块和按钮
   - 观察电路和图形的响应
   - 了解各个显示区域的功能

2. **第二阶段：基础探究**（约10分钟）
   - 在理想模式下，手动调节电压，观察线性关系
   - 使用自动扫描，观察完整I-U直线的生成
   - 切换到温度效应模式，对比观察曲线变化

3. **第三阶段：深入探究**（约15分钟）
   - 调节初始电阻，观察对曲线的影响
   - 改变热敏感性，理解材料特性的影响
   - 调整散热效率，探究热平衡过程
   - 使用“显示理想曲线”功能进行对比分析

4. **第四阶段：总结应用**（约10分钟）
   - 解释观察到的所有现象
   - 联系实际应用（如白炽灯、电热器）
   - 讨论欧姆定律的适用范围和局限性

#### 技术提示
1. **最佳观看**：在全屏模式下使用，确保所有元素清晰可见
2. **操作节奏**：手动调节时建议缓慢移动滑块，便于观察细节变化
3. **数据记录**：可截图保存不同参数下的I-U图象用于对比分析
4. **问题解决**：如遇显示异常，刷新页面即可重置所有参数

---

### 教育价值声明

本交互式动画不仅展示了欧姆定律的基本原理，更重要的是：
- **培养科学探究能力**：通过自主调节参数、观察现象、分析数据
- **建立物理直觉**：将抽象公式转化为直观的视觉体验
- **理解科学模型的层次性**：认识理想模型与真实世界的差异
- **激发学习兴趣**：游戏化的交互设计让物理学习变得生动有趣

我们希望这个工具能够成为您探索电学世界的得力助手，让欧姆定律的学习从记忆公式转变为理解本质，从被动接受转变为主动发现！

**祝您探索愉快，学有所获！** 🚀