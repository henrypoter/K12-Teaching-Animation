# 需求：自由落体与空气阻力影响（伽利略斜面实验的理想化）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画的目标用户主要为高中或大学低年级的物理学习者。他们的核心需求是：
1.  **理解核心矛盾**：直观感受“理想自由落体（无阻力）”与“现实自由落体（有阻力）”之间的差异，这是从经典力学向更复杂模型过渡的关键。
2.  **建立物理图像**：将抽象的物理公式（如 `v=gt`， `F=kv` 或 `F=kv²`）转化为具体的、可视的运动过程。
3.  **探究变量关系**：通过交互，自主探索不同因素（如物体质量、形状、空气密度、释放高度）对下落过程的影响。
4.  **连接历史与理想化方法**：理解伽利略如何通过“理想斜面实验”外推并抽象出自由落体定律，以及现代分析中“理想模型”的重要性。

#### 教学设计思路
1.  **核心概念**：
    *   **理想自由落体**：仅在重力作用下，加速度恒为 `g`，与质量无关。
    *   **空气阻力**：阻力大小与速度（一次或二次方）相关，方向与运动方向相反。
    *   **收尾速度**：当阻力与重力平衡时，物体匀速下落。
    *   **理想化方法**：通过忽略次要因素（如空气阻力、摩擦）来建立核心物理规律，再逐步加入复杂因素逼近现实。

2.  **认知规律**：
    *   **对比先行**：首先并排展示“理想真空”与“有空气”两种情境下，相同物体的下落过程，形成强烈视觉与数据对比，引发认知冲突。
    *   **控制变量**：设计交互面板，允许用户每次只改变一个参数（如质量、横截面积），观察其对运动轨迹和速度曲线的影响，引导归纳规律。
    *   **从定性到定量**：动画初期强调“谁快谁慢”、“是否同时落地”的定性观察，随后通过实时图表（位移-时间，速度-时间）引入定量分析。
    *   **历史情境融入**：以伽利略的“思想实验”为引子，将斜面实验作为理解“如何外推至90度（自由落体）”的桥梁。

3.  **交互设计**：
    *   **场景切换**：提供“伽利略斜面理想化”、“自由落体对比实验”、“参数探究实验室”三个主场景，逻辑递进。
    *   **模拟控制**：提供“播放/暂停/重置”按钮，允许用户控制模拟节奏。
    *   **参数调节器**：使用滑块或下拉菜单调节物体属性（质量、形状/横截面积）、环境属性（空气密度、重力加速度）和释放高度。
    *   **可视化叠加**：可勾选是否显示“受力示意图”（重力、阻力箭头）、“速度矢量箭头”、“实时曲线图”和“数据面板（瞬时速度、加速度、位移）”。
    *   **对象选择**：允许同时释放多个不同属性的物体，进行对比。

4.  **视觉呈现**：
    *   **主体明确**：下落物体采用简洁的几何图形（球体、立方体、羽毛图标等），确保视觉焦点清晰。
    *   **动态可视化**：
        *   用颜色和长度实时变化的箭头代表力与速度。
        *   用平滑的曲线图在旁侧同步绘制运动状态。
        *   理想模型下的物体可采用半透明或发光轮廓，与现实模型区分。
    *   **层次清晰**：将交互控制面板、数据图表与主动画区域明确分区，避免信息过载。

#### 配色方案选择
*   **主色调**：采用深蓝色或深空灰色作为画布背景，模拟科学实验的深邃感和专注感，并能突出前景元素。
*   **强调色**：
    *   **理想模型**：使用**蓝色**（代表理性、理想）。例如，理想下落物体的轨迹、速度曲线用蓝色表示。
    *   **现实模型/空气阻力**：使用**橙色**或**红色**（代表现实、能量耗散、阻力）。有阻力物体的轨迹、阻力箭头用橙色表示。
    *   **重力**：使用**黄色**或**恒定绿色**箭头表示，与阻力形成对比。
    *   **速度**：使用**青色**箭头表示，其长度和颜色明度可与速度大小关联。
    *   **界面与数据**：控制面板使用浅灰色卡片，文字用高对比度的白色或浅灰色。图表曲线颜色与对应物体颜色一致。
*   **原则**：保证足够的对比度，确保色盲友好，且颜色具有一致的物理含义指向。

#### 交互功能列表
1.  **场景选择器**：按钮切换“斜面理想化”、“自由落体对比”、“参数实验室”场景。
2.  **实验控制台**：
    *   播放 / 暂停 / 重置 按钮。
    *   “释放物体”按钮（可多次点击添加不同物体）。
    *   “清空画面”按钮。
3.  **物体参数面板**（在“参数实验室”中突出）：
    *   质量 `m` 调节滑块（范围：1kg - 100kg）。
    *   形状/横截面积选择器（图标：小球、大球、平板、羽毛）。
    *   阻力系数 `k` 或阻力模型选择（`F∝v` / `F∝v²`）下拉菜单。
4.  **环境参数面板**：
    *   空气密度调节滑块（范围：0（真空） - 1.5倍标准大气密度）。
    *   重力加速度 `g` 调节滑块（范围：1 - 20 m/s²）。
    *   释放高度调节滑块。
5.  **可视化开关**：
    *   ✔ 显示/隐藏 受力分析（重力、阻力箭头）。
    *   ✔ 显示/隐藏 速度箭头。
    *   ✔ 显示/隐藏 运动轨迹。
    *   ✔ 显示/隐藏 实时曲线图（s-t, v-t 可选）。
    *   ✔ 显示/隐藏 数据面板（实时数值显示）。
6.  **图表与数据**：
    *   并排的位移-时间与速度-时间坐标系。
    *   每个物体对应一条曲线，颜色与物体一致。
    *   数据面板动态显示选中物体的瞬时速度、位移、加速度和所受合力。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>自由落体与空气阻力影响 - 伽利略斜面实验的理想化</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0a0a2a 0%, #1a1a40 100%);
            color: #e0e0ff;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1600px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background: rgba(20, 20, 60, 0.7);
            border-radius: 15px;
            border: 1px solid #3a3a8a;
        }

        h1 {
            color: #4fc3f7;
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }

        .subtitle {
            color: #b39ddb;
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 20px;
        }

        .simulation-area {
            flex: 3;
            min-width: 300px;
            background: rgba(10, 10, 40, 0.8);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid #3a3a8a;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .control-panel {
            flex: 2;
            min-width: 300px;
            background: rgba(20, 20, 60, 0.8);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid #3a3a8a;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .panel-title {
            color: #4fc3f7;
            font-size: 1.5rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #3a3a8a;
        }

        .scene-selector {
            display: flex;
            gap: 10px;
            margin-bottom: 25px;
            flex-wrap: wrap;
        }

        .scene-btn {
            flex: 1;
            min-width: 120px;
            padding: 12px 15px;
            background: #2a2a6a;
            color: #b39ddb;
            border: 2px solid #3a3a8a;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            text-align: center;
        }

        .scene-btn:hover {
            background: #3a3a8a;
            color: #e0e0ff;
        }

        .scene-btn.active {
            background: #1565c0;
            color: white;
            border-color: #4fc3f7;
            box-shadow: 0 0 15px rgba(79, 195, 247, 0.5);
        }

        .control-section {
            margin-bottom: 25px;
            padding: 15px;
            background: rgba(30, 30, 70, 0.5);
            border-radius: 10px;
        }

        .section-title {
            color: #81c784;
            font-size: 1.2rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title i {
            font-size: 1.4rem;
        }

        .button-group {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 15px;
        }

        .btn {
            padding: 10px 20px;
            background: #2a2a6a;
            color: #e0e0ff;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            flex: 1;
            min-width: 100px;
        }

        .btn:hover {
            background: #3a3a8a;
            transform: translateY(-2px);
        }

        .btn.primary {
            background: #1565c0;
            color: white;
        }

        .btn.primary:hover {
            background: #1976d2;
            box-shadow: 0 4px 15px rgba(21, 101, 192, 0.4);
        }

        .btn.warning {
            background: #f57c00;
            color: white;
        }

        .btn.warning:hover {
            background: #ff9800;
        }

        .slider-container {
            margin: 15px 0;
        }

        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .slider-label span {
            color: #e0e0ff;
            font-size: 0.95rem;
        }

        .slider-value {
            color: #4fc3f7;
            font-weight: bold;
        }

        .slider {
            width: 100%;
            height: 8px;
            -webkit-appearance: none;
            background: #2a2a6a;
            border-radius: 4px;
            outline: none;
        }

        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #4fc3f7;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: 0 0 10px rgba(79, 195, 247, 0.8);
        }

        .checkbox-group {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 12px;
            margin-top: 10px;
        }

        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
            padding: 8px;
            border-radius: 6px;
            transition: background 0.3s;
        }

        .checkbox-item:hover {
            background: rgba(79, 195, 247, 0.1);
        }

        .checkbox-item input[type="checkbox"] {
            width: 18px;
            height: 18px;
            cursor: pointer;
            accent-color: #4fc3f7;
        }

        .checkbox-item label {
            cursor: pointer;
            color: #e0e0ff;
            font-size: 0.95rem;
        }

        .object-selector {
            display: flex;
            gap: 15px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .object-option {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            cursor: pointer;
            padding: 10px;
            border-radius: 8px;
            border: 2px solid transparent;
            transition: all 0.3s;
            background: rgba(40, 40, 80, 0.5);
        }

        .object-option:hover {
            background: rgba(79, 195, 247, 0.1);
            border-color: #4fc3f7;
        }

        .object-option.selected {
            background: rgba(79, 195, 247, 0.2);
            border-color: #4fc3f7;
            box-shadow: 0 0 15px rgba(79, 195, 247, 0.3);
        }

        .object-icon {
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
        }

        .object-name {
            font-size: 0.9rem;
            color: #b39ddb;
        }

        .canvas-container {
            position: relative;
            width: 100%;
            height: 600px;
            background: rgba(5, 5, 25, 0.9);
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid #3a3a8a;
        }

        #simulationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .data-panel {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(10, 10, 40, 0.85);
            border-radius: 10px;
            padding: 15px;
            border: 1px solid #3a3a8a;
            min-width: 250px;
            backdrop-filter: blur(5px);
        }

        .data-title {
            color: #81c784;
            font-size: 1.1rem;
            margin-bottom: 10px;
            text-align: center;
        }

        .data-item {
            display: flex;
            justify-content: space-between;
            margin: 8px 0;
            padding-bottom: 5px;
            border-bottom: 1px dashed #3a3a8a;
        }

        .data-label {
            color: #b39ddb;
        }

        .data-value {
            color: #4fc3f7;
            font-weight: bold;
            font-family: 'Courier New', monospace;
        }

        .chart-container {
            margin-top: 20px;
            background: rgba(10, 10, 40, 0.8);
            border-radius: 10px;
            padding: 15px;
            border: 1px solid #3a3a8a;
        }

        .chart-title {
            color: #ffb74d;
            font-size: 1.2rem;
            margin-bottom: 15px;
            text-align: center;
        }

        #chartCanvas {
            width: 100%;
            height: 250px;
            display: block;
        }

        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 10px;
            flex-wrap: wrap;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }

        .legend-text {
            color: #e0e0ff;
            font-size: 0.9rem;
        }

        .info-panel {
            background: rgba(20, 20, 60, 0.8);
            border-radius: 15px;
            padding: 20px;
            margin-top: 20px;
            border: 1px solid #3a3a8a;
        }

        .info-title {
            color: #ffb74d;
            font-size: 1.3rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .info-content {
            color: #e0e0ff;
            font-size: 1rem;
            line-height: 1.7;
        }

        .info-content p {
            margin-bottom: 15px;
        }

        .highlight {
            color: #4fc3f7;
            font-weight: bold;
        }

        .resistance-highlight {
            color: #ff8a65;
            font-weight: bold;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            padding: 20px;
            color: #b39ddb;
            font-size: 0.9rem;
            border-top: 1px solid #3a3a8a;
        }

        @media (max-width: 1200px) {
            .main-content {
                flex-direction: column;
            }
            
            .canvas-container {
                height: 500px;
            }
        }

        @media (max-width: 768px) {
            .canvas-container {
                height: 400px;
            }
            
            .data-panel {
                position: relative;
                top: 0;
                right: 0;
                margin-top: 20px;
                width: 100%;
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
            <h1>自由落体与空气阻力影响</h1>
            <p class="subtitle">伽利略斜面实验的理想化 · 交互式物理教学动画</p>
        </header>

        <div class="main-content">
            <div class="simulation-area">
                <h2 class="panel-title">模拟实验区</h2>
                
                <div class="scene-selector">
                    <button class="scene-btn active" data-scene="incline">斜面理想化</button>
                    <button class="scene-btn" data-scene="comparison">自由落体对比</button>
                    <button class="scene-btn" data-scene="lab">参数实验室</button>
                </div>
                
                <div class="canvas-container">
                    <canvas id="simulationCanvas"></canvas>
                    
                    <div class="data-panel">
                        <div class="data-title">实时数据</div>
                        <div class="data-item">
                            <span class="data-label">时间 (t):</span>
                            <span id="timeValue" class="data-value">0.00 s</span>
                        </div>
                        <div class="data-item">
                            <span class="data-label">理想速度:</span>
                            <span id="idealSpeed" class="data-value">0.00 m/s</span>
                        </div>
                        <div class="data-item">
                            <span class="data-label">实际速度:</span>
                            <span id="realSpeed" class="data-value">0.00 m/s</span>
                        </div>
                        <div class="data-item">
                            <span class="data-label">位移:</span>
                            <span id="displacement" class="data-value">0.00 m</span>
                        </div>
                        <div class="data-item">
                            <span class="data-label">空气阻力:</span>
                            <span id="airResistance" class="data-value">0.00 N</span>
                        </div>
                        <div class="data-item">
                            <span class="data-label">收尾速度:</span>
                            <span id="terminalVelocity" class="data-value">-- m/s</span>
                        </div>
                    </div>
                </div>
                
                <div class="chart-container">
                    <div class="chart-title">速度-时间关系图</div>
                    <canvas id="chartCanvas"></canvas>
                    <div class="legend">
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #4fc3f7;"></div>
                            <span class="legend-text">理想自由落体 (无阻力)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #ff8a65;"></div>
                            <span class="legend-text">实际落体 (有空气阻力)</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="control-panel">
                <h2 class="panel-title">实验控制台</h2>
                
                <div class="control-section">
                    <div class="section-title">
                        <span>🏃 实验控制</span>
                    </div>
                    <div class="button-group">
                        <button id="playBtn" class="btn primary">▶ 播放</button>
                        <button id="pauseBtn" class="btn">⏸ 暂停</button>
                        <button id="resetBtn" class="btn warning">🔄 重置</button>
                    </div>
                    <div class="button-group">
                        <button id="addObjectBtn" class="btn">➕ 添加物体</button>
                        <button id="clearBtn" class="btn">🗑️ 清空画面</button>
                    </div>
                </div>
                
                <div class="control-section">
                    <div class="section-title">
                        <span>⚙️ 物体参数</span>
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>质量 (m):</span>
                            <span id="massValue" class="slider-value">10 kg</span>
                        </div>
                        <input type="range" min="1" max="100" value="10" class="slider" id="massSlider">
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>横截面积:</span>
                            <span id="areaValue" class="slider-value">0.1 m²</span>
                        </div>
                        <input type="range" min="1" max="100" value="10" class="slider" id="areaSlider">
                    </div>
                    
                    <div style="margin: 15px 0;">
                        <div class="slider-label">
                            <span>物体形状:</span>
                        </div>
                        <div class="object-selector">
                            <div class="object-option selected" data-shape="sphere">
                                <div class="object-icon">●</div>
                                <span class="object-name">球体</span>
                            </div>
                            <div class="object-option" data-shape="cube">
                                <div class="object-icon">■</div>
                                <span class="object-name">立方体</span>
                            </div>
                            <div class="object-option" data-shape="plate">
                                <div class="object-icon">▭</div>
                                <span class="object-name">平板</span>
                            </div>
                            <div class="object-option" data-shape="feather">
                                <div class="object-icon">𓆰</div>
                                <span class="object-name">羽毛</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>阻力模型:</span>
                            <span id="resistanceModelValue" class="slider-value">F ∝ v²</span>
                        </div>
                        <input type="range" min="0" max="1" value="1" class="slider" id="resistanceModelSlider">
                    </div>
                </div>
                
                <div class="control-section">
                    <div class="section-title">
                        <span>🌍 环境参数</span>
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>空气密度 (ρ):</span>
                            <span id="densityValue" class="slider-value">1.0 (标准)</span>
                        </div>
                        <input type="range" min="0" max="150" value="100" class="slider" id="densitySlider">
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>重力加速度 (g):</span>
                            <span id="gravityValue" class="slider-value">9.8 m/s²</span>
                        </div>
                        <input type="range" min="10" max="200" value="98" class="slider" id="gravitySlider">
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>释放高度:</span>
                            <span id="heightValue" class="slider-value">100 m</span>
                        </div>
                        <input type="range" min="10" max="500" value="100" class="slider" id="heightSlider">
                    </div>
                </div>
                
                <div class="control-section">
                    <div class="section-title">
                        <span>👁️ 可视化选项</span>
                    </div>
                    
                    <div class="checkbox-group">
                        <div class="checkbox-item">
                            <input type="checkbox" id="showForces" checked>
                            <label for="showForces">显示受力分析</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showVelocity" checked>
                            <label for="showVelocity">显示速度箭头</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showTrajectory">
                            <label for="showTrajectory">显示运动轨迹</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showGrid" checked>
                            <label for="showGrid">显示参考网格</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showTerminal" checked>
                            <label for="showTerminal">标记收尾速度</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showData" checked>
                            <label for="showData">显示数据面板</label>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="info-panel">
            <div class="info-title">
                <span>📚 物理原理说明</span>
            </div>
            <div class="info-content">
                <p><span class="highlight">理想自由落体</span>：物体仅在重力作用下下落，加速度恒为 <span class="highlight">g = 9.8 m/s²</span>，与质量无关。速度随时间线性增加：<span class="highlight">v = g·t</span>。</p>
                <p><span class="resistance-highlight">空气阻力影响</span>：阻力大小与速度相关（<span class="resistance-highlight">F ∝ v</span> 或 <span class="resistance-highlight">F ∝ v²</span>），方向与运动方向相反。随着速度增加，阻力增大，净加速度减小。</p>
                <p><span class="highlight">收尾速度</span>：当阻力增长到与重力平衡时，物体以恒定速度下落，此时加速度为零。收尾速度取决于物体质量、形状和空气密度。</p>
                <p><span class="highlight">伽利略的理想化方法</span>：通过斜面实验减小重力加速度分量，使测量更精确，再外推至90°（自由落体）。这种方法通过忽略次要因素（如空气阻力）来揭示核心物理规律。</p>
            </div>
        </div>
        
        <footer>
            <p>交互式物理教学动画 | 自由落体与空气阻力影响 | 设计：教育技术专家</p>
            <p>提示：通过调节参数观察不同条件下物体的运动差异，理解理想模型与现实情况的区别</p>
        </footer>
    </div>

    <script>
        // 全局变量和常量
        const canvas = document.getElementById('simulationCanvas');
        const chartCanvas = document.getElementById('chartCanvas');
        const ctx = canvas.getContext('2d');
        const chartCtx = chartCanvas.getContext('2d');
        
        // 模拟状态
        let simulationTime = 0;
        let isPlaying = false;
        let lastTimestamp = 0;
        let currentScene = 'incline';
        let objects = [];
        let chartData = { ideal: [], real: [], time: [] };
        let maxChartTime = 10;
        
        // 物理参数
        let params = {
            mass: 10,           // kg
            area: 0.1,          // m²
            shape: 'sphere',    // 形状
            density: 1.0,       // 空气密度 (标准=1.0)
            gravity: 9.8,       // m/s²
            height: 100,        // m
            resistanceModel: 1, // 0: F ∝ v, 1: F ∝ v²
            dragCoefficient: 0.47 // 阻力系数 (球体)
        };
        
        // 可视化选项
        let visualOptions = {
            showForces: true,
            showVelocity: true,
            showTrajectory: false,
            showGrid: true,
            showTerminal: true,
            showData: true
        };
        
        // 颜色定义
        const colors = {
            ideal: '#4fc3f7',      // 蓝色 - 理想模型
            real: '#ff8a65',       // 橙色 - 实际模型
            gravity: '#81c784',    // 绿色 - 重力
            resistance: '#ff5252', // 红色 - 阻力
            velocity: '#29b6f6',   // 青色 - 速度
            grid: '#3a3a8a',       // 网格颜色
            text: '#e0e0ff',       // 文本颜色
            background: '#0a0a2a'  // 背景色
        };
        
        // 物体类
        class FallingObject {
            constructor(x, y, isIdeal = false) {
                this.x = x;
                this.y = y;
                this.isIdeal = isIdeal;
                this.vx = 0;
                this.vy = 0;
                this.ax = 0;
                this.ay = isIdeal ? params.gravity : params.gravity;
                this.mass = params.mass;
                this.area = params.area;
                this.shape = params.shape;
                this.color = isIdeal ? colors.ideal : colors.real;
                this.trajectory = [];
                this.terminalVelocity = 0;
                this.calculateTerminalVelocity();
                
                // 根据形状调整阻力系数
                this.dragCoefficient = this.getDragCoefficient();
                
                // 唯一ID
                this.id = Date.now() + Math.random();
            }
            
            getDragCoefficient() {
                switch(params.shape) {
                    case 'sphere': return 0.47;
                    case 'cube': return 1.05;
                    case 'plate': return 1.28;
                    case 'feather': return 1.5;
                    default: return 0.47;
                }
            }
            
            calculateTerminalVelocity() {
                if (this.isIdeal) {
                    this.terminalVelocity = Infinity;
                    return;
                }
                
                const g = params.gravity;
                const m = this.mass;
                const A = this.area;
                const ρ = params.density * 1.225; // 标准空气密度 1.225 kg/m³
                const Cd = this.dragCoefficient;
                
                if (params.resistanceModel === 0) {
                    // F ∝ v 模型 (线性阻力)
                    // 假设 k = 0.5 * ρ * Cd * A
                    const k = 0.5 * ρ * Cd * A;
                    this.terminalVelocity = (m * g) / k;
                } else {
                    // F ∝ v² 模型 (二次阻力)
                    // v_terminal = sqrt(2mg / ρACd)
                    this.terminalVelocity = Math.sqrt((2 * m * g) / (ρ * A * Cd));
                }
            }
            
            update(dt) {
                // 保存轨迹点
                if (visualOptions.showTrajectory) {
                    this.trajectory.push({x: this.x, y: this.y});
                    if (this.trajectory.length > 100) {
                        this.trajectory.shift();
                    }
                }
                
                // 理想物体：只受重力
                if (this.isIdeal) {
                    this.vy += params.gravity * dt;
                    this.y += this.vy * dt;
                    return;
                }
                
                // 实际物体：重力 + 空气阻力
                const g = params.gravity;
                const m = this.mass;
                const A = this.area;
                const ρ = params.density * 1.225;
                const Cd = this.dragCoefficient;
                
                // 计算当前速度大小
                const v = Math.sqrt(this.vx*this.vx + this.vy*this.vy);
                
                // 计算阻力
                let dragForce = 0;
                if (params.resistanceModel === 0) {
                    // 线性阻力模型: F_drag = k * v
                    const k = 0.5 * ρ * Cd * A;
                    dragForce = k * v;
                } else {
                    // 二次阻力模型: F_drag = 0.5 * ρ * Cd * A * v²
                    dragForce = 0.5 * ρ * Cd * A * v * v;
                }
                
                // 计算阻力加速度 (方向与速度相反)
                const dragAcceleration = dragForce / m;
                
                // 计算阻力方向分量
                let dragAx = 0, dragAy = 0;
                if (v > 0) {
                    dragAx = -dragAcceleration * (this.vx / v);
                    dragAy = -dragAcceleration * (this.vy / v);
                }
                
                // 总加速度 = 重力加速度 + 阻力加速度
                this.ax = dragAx;
                this.ay = g + dragAy;
                
                // 更新速度
                this.vx += this.ax * dt;
                this.vy += this.ay * dt;
                
                // 更新位置
                this.x += this.vx * dt;
                this.y += this.vy * dt;
                
                // 重新计算收尾速度 (参数可能已改变)
                this.calculateTerminalVelocity();
            }
            
            draw(ctx) {
                // 绘制轨迹
                if (visualOptions.showTrajectory && this.trajectory.length > 1) {
                    ctx.beginPath();
                    ctx.strokeStyle = this.color + '80'; // 半透明
                    ctx.lineWidth = 2;
                    
                    for (let i = 0; i < this.trajectory.length; i++) {
                        const point = this.trajectory[i];
                        if (i === 0) {
                            ctx.moveTo(point.x, point.y);
                        } else {
                            ctx.lineTo(point.x, point.y);
                        }
                    }
                    
                    ctx.stroke();
                }
                
                // 绘制物体
                ctx.save();
                ctx.translate(this.x, this.y);
                
                // 根据形状绘制不同图形
                const size = 20 + this.mass / 5;
                
                ctx.fillStyle = this.color;
                ctx.strokeStyle = '#ffffff';
                ctx.lineWidth = 2;
                
                switch(this.shape) {
                    case 'sphere':
                        ctx.beginPath();
                        ctx.arc(0, 0, size/2, 0, Math.PI * 2);
                        ctx.fill();
                        ctx.stroke();
                        
                        // 添加高光效果
                        ctx.beginPath();
                        ctx.arc(-size/4, -size/4, size/6, 0, Math.PI * 2);
                        ctx.fillStyle = '#ffffff40';
                        ctx.fill();
                        break;
                        
                    case 'cube':
                        ctx.fillRect(-size/2, -size/2, size, size);
                        ctx.strokeRect(-size/2, -size/2, size, size);
                        break;
                        
                    case 'plate':
                        ctx.fillRect(-size, -size/3, size*2, size/1.5);
                        ctx.strokeRect(-size, -size/3, size*2, size/1.5);
                        break;
                        
                    case 'feather':
                        // 绘制羽毛简化图形
                        ctx.beginPath();
                        ctx.moveTo(0, -size);
                        ctx.bezierCurveTo(size/2, -size/2, size/2, size/2, 0, size);
                        ctx.bezierCurveTo(-size/2, size/2, -size/2, -size/2, 0, -size);
                        ctx.fill();
                        ctx.stroke();
                        break;
                }
                
                // 绘制速度箭头
                if (visualOptions.showVelocity && (this.vx !== 0 || this.vy !== 0)) {
                    const speed = Math.sqrt(this.vx*this.vx + this.vy*this.vy);
                    const arrowLength = Math.min(speed * 5, 100);
                    
                    if (arrowLength > 5) {
                        ctx.save();
                        ctx.rotate(Math.atan2(this.vy, this.vx));
                        
                        ctx.beginPath();
                        ctx.moveTo(0, 0);
                        ctx.lineTo(arrowLength, 0);
                        ctx.lineTo(arrowLength - 10, -5);
                        ctx.moveTo(arrowLength, 0);
                        ctx.lineTo(arrowLength - 10, 5);
                        
                        ctx.strokeStyle = colors.velocity;
                        ctx.lineWidth = 3;
                        ctx.stroke();
                        
                        ctx.restore();
                    }
                }
                
                // 绘制受力分析
                if (visualOptions.showForces && !this.isIdeal) {
                    // 重力箭头 (向下)
                    ctx.beginPath();
                    ctx.moveTo(0, 0);
                    ctx.lineTo(0, 50);
                    ctx.lineTo(-5, 45);
                    ctx.moveTo(0, 50);
                    ctx.lineTo(5, 45);
                    
                    ctx.strokeStyle = colors.gravity;
                    ctx.lineWidth = 3;
                    ctx.stroke();
                    
                    ctx.fillStyle = colors.gravity;
                    ctx.font = '12px Arial';
                    ctx.fillText('G', 10, 25);
                    
                    // 阻力箭头 (向上，与速度方向相反)
                    const speed = Math.sqrt(this.vx*this.vx + this.vy*this.vy);
                    if (speed > 0.1) {
                        const dragLength = Math.min(speed * 3, 40);
                        
                        ctx.beginPath();
                        ctx.moveTo(0, 0);
                        ctx.lineTo(-this.vx/speed * dragLength, -this.vy/speed * dragLength);
                        ctx.lineTo(-this.vx/speed * dragLength + 5, -this.vy/speed * dragLength + 5);
                        ctx.moveTo(-this.vx/speed * dragLength, -this.vy/speed * dragLength);
                        ctx.lineTo(-this.vx/speed * dragLength - 5, -this.vy/speed * dragLength + 5);
                        
                        ctx.strokeStyle = colors.resistance;
                        ctx.lineWidth = 3;
                        ctx.stroke();
                        
                        ctx.fillStyle = colors.resistance;
                        ctx.fillText('Fₐ', -this.vx/speed * dragLength/2 - 15, -this.vy/speed * dragLength/2);
                    }
                }
                
                ctx.restore();
                
                // 标记收尾速度
                if (visualOptions.showTerminal && !this.isIdeal && this.terminalVelocity > 0) {
                    const currentSpeed = Math.sqrt(this.vx*this.vx + this.vy*this.vy);
                    const terminalRatio = currentSpeed / this.terminalVelocity;
                    
                    if (terminalRatio > 0.9) {
                        ctx.save();
                        ctx.translate(this.x, this.y);
                        
                        ctx.beginPath();
                        ctx.arc(0, 0, 25, 0, Math.PI * 2);
                        ctx.strokeStyle = '#ffeb3b';
                        ctx.lineWidth = 2;
                        ctx.setLineDash([5, 5]);
                        ctx.stroke();
                        ctx.setLineDash([]);
                        
                        ctx.fillStyle = '#ffeb3b';
                        ctx.font = 'bold 12px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('≈收尾速度', 0, -35);
                        
                        ctx.restore();
                   

### 3. 过程输出

### 3. 使用指南

## 《自由落体与空气阻力影响》交互式教学动画使用指南

欢迎使用这款精心设计的物理教学动画！本工具旨在通过直观的交互体验，帮助您深入理解自由落体运动的本质以及空气阻力的影响。无论您是教师、学生还是物理爱好者，都能从中获得有价值的科学洞察。

---

### 一、功能说明

本动画模拟了三种核心教学场景：

1. **斜面理想化场景**：再现伽利略的经典思想实验，展示如何通过斜面实验外推至自由落体，理解理想化方法
2. **自由落体对比场景**：并排展示理想（无阻力）与实际（有阻力）下落过程，形成直观对比
3. **参数实验室场景**：提供完整的参数调节功能，让您自主探究各因素对运动的影响

### 二、主要功能

#### 🎮 实验控制区
- **播放/暂停/重置**：控制模拟的开始、暂停和重新开始
- **添加物体**：在场景中添加新的下落物体进行对比实验
- **清空画面**：移除所有物体，重新开始实验

#### ⚙️ 参数调节区
- **物体参数**：
  - 质量（1-100 kg）：调节物体质量
  - 横截面积：调节物体迎风面积
  - 物体形状：选择球体、立方体、平板或羽毛（不同形状对应不同阻力系数）
  - 阻力模型：在线性阻力（F∝v）和二次阻力（F∝v²）模型间切换

- **环境参数**：
  - 空气密度（0-1.5倍标准）：从真空到高密度空气环境
  - 重力加速度（1-20 m/s²）：模拟不同星球的重力环境
  - 释放高度（10-500 m）：调节下落起始高度

#### 👁️ 可视化选项
- **受力分析**：显示重力（绿色箭头）和空气阻力（红色箭头）
- **速度箭头**：显示物体的瞬时速度（青色箭头）
- **运动轨迹**：记录并显示物体的运动路径
- **参考网格**：提供空间尺度参考
- **收尾速度标记**：当物体接近收尾速度时显示标记
- **数据面板**：实时显示关键物理量数值

### 三、设计特色

#### 🎨 视觉设计
- **科学配色方案**：
  - 蓝色（#4fc3f7）：代表理想模型、理性思维
  - 橙色（#ff8a65）：代表实际模型、空气阻力影响
  - 绿色（#81c784）：重力
  - 红色（#ff5252）：空气阻力
  - 深空背景：营造科学实验的专注氛围

- **动态可视化**：
  - 力与速度箭头随物理量实时变化
  - 速度-时间曲线同步更新
  - 物体形状与参数关联

#### 📊 数据呈现
- **实时数据面板**：显示时间、速度、位移、阻力、收尾速度等关键数据
- **速度-时间图表**：同时绘制理想与实际物体的速度变化曲线
- **物理原理说明**：提供简洁明了的理论解释

### 四、教学要点

#### 核心概念探究
1. **理想自由落体定律**
   - 观察无阻力情况下，所有物体同时落地的现象
   - 验证速度与时间的线性关系：v = g·t
   - 理解加速度恒为g，与质量无关

2. **空气阻力影响**
   - 观察阻力如何随速度增加而增大
   - 发现阻力导致加速度逐渐减小
   - 理解收尾速度的形成机制

3. **收尾速度概念**
   - 探究收尾速度与质量、形状、空气密度的关系
   - 验证收尾速度公式：vₜ = √(2mg/ρAC₄)
   - 理解平衡状态下的匀速运动

4. **伽利略的理想化方法**
   - 通过斜面实验理解如何减小测量难度
   - 学习"忽略次要因素，抓住主要矛盾"的科学思维
   - 体会从理想模型到现实模型的渐进过程

#### 实验设计建议
- **对比实验**：同时释放不同质量的球体，观察在空气中和真空中的差异
- **控制变量法**：固定其他参数，只改变一个变量（如质量或面积）
- **极限情况**：将空气密度调为0（真空），验证伽利略的结论
- **形状影响**：比较球体、平板和羽毛的下落过程

### 五、使用建议

#### 对于教师
1. **课堂演示**：
   - 使用"自由落体对比"场景引入课题
   - 通过参数调节展示不同条件下的运动差异
   - 利用图表分析速度变化规律

2. **探究式学习**：
   - 提出问题："为什么羽毛和铁球在空气中下落速度不同？"
   - 引导学生设计实验验证假设
   - 组织小组讨论分析数据

3. **概念巩固**：
   - 在讲解收尾速度时，使用"参数实验室"进行动态演示
   - 通过改变重力加速度，讨论不同星球上的下落现象

#### 对于学生
1. **自主学习**：
   - 按照"观察-提问-实验-总结"的步骤进行探索
   - 记录不同参数组合下的实验结果
   - 尝试解释观察到的现象

2. **概念理解**：
   - 先观察理想情况，再逐步加入复杂因素
   - 关注受力分析，理解加速度变化的根本原因
   - 将图表数据与运动现象联系起来

3. **拓展思考**：
   - 思考：如果阻力与速度的三次方成正比，运动会怎样变化？
   - 探究：如何设计一个实验来测量空气阻力系数？
   - 应用：跳伞运动员如何利用收尾速度原理？

#### 最佳实践流程
1. **第一步：观察现象**
   - 在"自由落体对比"场景中，播放默认设置下的模拟
   - 观察理想物体与实际物体的运动差异

2. **第二步：提出问题**
   - 为什么实际物体的速度增长会变慢？
   - 哪些因素会影响收尾速度的大小？

3. **第三步：实验探究**
   - 切换到"参数实验室"
   - 依次调节质量、面积、形状、空气密度
   - 记录每次变化对运动的影响

4. **第四步：数据分析**
   - 关注速度-时间曲线的变化
   - 比较不同条件下收尾速度的数值
   - 寻找各参数与收尾速度的定量关系

5. **第五步：总结规律**
   - 归纳空气阻力的影响因素
   - 理解收尾速度的形成条件
   - 掌握理想化方法的科学价值

---

### 技术支持与反馈

本动画基于HTML5 Canvas技术开发，支持现代主流浏览器。如果您在使用过程中遇到任何问题，或对功能改进有建议，请记录以下信息：
- 浏览器类型和版本
- 操作步骤描述
- 期望与实际表现的差异

**教育目标**：通过这款交互式工具，我们希望能够：
1. 将抽象的物理公式转化为直观的视觉体验
2. 培养科学探究的思维方法
3. 激发对物理学的兴趣和好奇心
4. 理解理想模型在科学发展中的重要作用

祝您探索愉快，在自由落体的世界中发现物理的奥秘！🚀

---
*设计理念：让复杂的物理概念变得可见、可操作、可理解*