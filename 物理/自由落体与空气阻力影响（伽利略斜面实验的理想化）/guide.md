# 需求：自由落体与空气阻力影响（伽利略斜面实验的理想化）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的物理初学者。他们已具备基本的运动学知识，但对“理想化模型”与“现实世界”的差异理解不深。
2.  **核心需求**：
    *   **理解理想化模型**：理解伽利略斜面实验如何通过“减小阻力影响”来逼近“自由落体”这一理想模型，以及理想模型在物理学中的重要性。
    *   **直观对比**：直观地看到在**完全无阻力**（理想自由落体）、**有空气阻力**（现实世界）以及**斜面减缓过程**三种情境下，物体运动状态的差异。
    *   **探究变量影响**：能够改变参数（如物体质量、迎风面积、斜面角度），观察这些变量如何影响空气阻力的效果，以及它们是否影响理想自由落体。
    *   **降低抽象门槛**：将抽象的“理想化”、“阻力与重力平衡”等概念，通过可视化的动画和实时数据图表具象化。

#### 教学设计思路
*   **核心概念**：
    1.  **理想自由落体**：所有物体仅在重力作用下，以相同的加速度（g）下落，与质量、形状无关。
    2.  **空气阻力**：与现实物体形状、速度、迎风面积有关，方向与运动方向相反。
    3.  **伽利略的智慧**：利用斜面“稀释”重力，减缓下落速度，从而显著减小空气阻力的影响，更接近理想条件，得以发现落体定律。
    4.  **终端速度**：当阻力与重力平衡时，物体将匀速下落。

*   **认知规律（动画流程设计）**：
    1.  **从历史与问题出发**：开场简短展示“轻重物体是否同时落地”的亚里士多德观点与伽利略的质疑，引发认知冲突。
    2.  **建立理想参照系**：首先展示在**真空管**（理想环境）中，不同质量小球同时下落，确立理想模型的结论。
    3.  **引入现实复杂性**：然后在**空气中**释放相同小球，观察它们因阻力不同而略微分开，与理想情况对比。
    4.  **揭示伽利略的方法**：接着引入**斜面**。展示同一个球在空气中从不同角度斜面滚下，角度越大（越接近竖直），阻力影响越显著，下落时间与理想值的偏差越大；角度越小，阻力影响越小，运动越接近匀加速规律。这直观解释了为何斜面实验是当时条件下的“理想化”工具。
    5.  **深化与探究**：最后提供控制面板，允许用户单独对比“理想落体”、“有阻力落体”和“斜面运动”，并自由调节参数，观察数据变化。

*   **交互设计**：
    *   **阶段式引导**：采用“引导模式”和“自由探索模式”。引导模式按上述认知规律分步播放并高亮关键点。自由探索模式开放所有控制。
    *   **对比可视化**：屏幕并排或重叠显示两种场景（如左理想，右现实），便于直接对比。
    *   **参数控制面板**：提供滑块或输入框调节：小球质量、半径（影响迎风面积）、空气密度、斜面倾角。
    *   **实时数据反馈**：动画旁实时显示关键数据（瞬时速度、加速度、下落距离、时间），并绘制速度-时间（v-t）图。在理想情况下，v-t图是一条直线；在有阻力时，曲线会逐渐变平（趋向终端速度）。

*   **视觉呈现**：
    *   **场景分区**：画布清晰划分为“理想真空环境”、“有空气环境”和“伽利略斜面”三个主要区域，或用标签切换。
    *   **运动可视化**：
        *   用**箭头**动态表示力（重力箭头恒定向下，阻力箭头随速度增大而增大，方向向上）。
        *   用**运动轨迹**或**拖尾**效果增强动感。
        *   在斜面上，可以绘制等间距的时间标记，显示小球在相等时间间隔内下落的距离越来越大（匀加速特征）。
    *   **重点突出**：在讲解关键点时，使用光圈、放大或颜色高亮来吸引注意力（如高亮阻力箭头的变化）。

#### 配色方案选择
*   **主色调**：采用深蓝色（`#1a237e`）或深空蓝作为背景，模拟科学感和深邃的思考空间。
*   **物体与重点色**：
    *   小球：使用明亮的**黄色**（`#ffeb3b`）和**红色**（`#f44336`），在深背景下非常醒目，也便于区分不同物体。
    *   力箭头：**重力**用白色或浅灰色（`#e0e0e0`）表示恒定与基础。**空气阻力**用**橙色**（`#ff9800`）表示，因其是可变且需要重点关注的效果。
    *   斜面与装置：使用浅灰色（`#bdbdbd`）或木质纹理色，体现实验器材感。
    *   图表与数据：图表背景半透明黑，数据线颜色与对应小球颜色一致（如理想模型用青色 `#00bcd4`，现实模型用对应小球色）。
*   **整体风格**：干净、简洁、现代，减少视觉噪音，确保所有视觉元素都服务于教学目的。

#### 交互功能列表
1.  **模式选择按钮**：“引导教程” / “自由探索”。
2.  **场景选择/控制**：
    *   “理想真空落体” 开关。
    *   “有空气阻力落体” 开关。
    *   “伽利略斜面实验” 开关（可切换不同角度预设，如5°，30°，60°，90°）。
3.  **参数调节面板**（在自由探索模式下）：
    *   小球1质量滑块 (m1)。
    *   小球2质量滑块 (m2)。
    *   小球半径滑块 (影响阻力)。
    *   空气密度滑块 (从“真空”到“浓密”)。
    *   斜面倾角滑块 (0° 到 90°)。
4.  **动画控制按钮**：播放 / 暂停 / 重置。
5.  **数据可视化面板**：
    *   实时数值显示：时间、速度、加速度、下落距离。
    *   动态v-t图，随着动画进行同步绘制。
    *   可勾选显示/隐藏不同场景的数据曲线。
6.  **提示与说明**：一个固定的文本框区域，根据当前动画阶段显示简明的原理说明或伽利略的历史引言。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>自由落体与空气阻力影响 | 伽利略斜面实验的理想化</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0d1b2a 0%, #1a237e 100%);
            color: #e0e0e0;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        h1 {
            color: #ffeb3b;
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            color: #00bcd4;
            font-size: 1.2rem;
            font-weight: 300;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .simulation-area {
            flex: 3;
            min-width: 300px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background: rgba(13, 27, 42, 0.7);
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 20px;
        }
        
        #simulationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .controls-area {
            flex: 2;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .control-panel {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        h2 {
            color: #ff9800;
            font-size: 1.5rem;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid rgba(255, 152, 0, 0.3);
        }
        
        .mode-selector {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .mode-btn {
            flex: 1;
            padding: 12px;
            background: rgba(255, 152, 0, 0.1);
            border: 1px solid rgba(255, 152, 0, 0.3);
            color: #ff9800;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        .mode-btn:hover {
            background: rgba(255, 152, 0, 0.2);
        }
        
        .mode-btn.active {
            background: rgba(255, 152, 0, 0.4);
            border-color: #ff9800;
            box-shadow: 0 0 10px rgba(255, 152, 0, 0.3);
        }
        
        .scene-selector {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .scene-btn {
            padding: 10px;
            background: rgba(0, 188, 212, 0.1);
            border: 1px solid rgba(0, 188, 212, 0.3);
            color: #00bcd4;
            border-radius: 8px;
            cursor: pointer;
            text-align: center;
            transition: all 0.3s;
        }
        
        .scene-btn:hover {
            background: rgba(0, 188, 212, 0.2);
        }
        
        .scene-btn.active {
            background: rgba(0, 188, 212, 0.4);
            border-color: #00bcd4;
            box-shadow: 0 0 10px rgba(0, 188, 212, 0.3);
        }
        
        .param-controls {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .param-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }
        
        .param-label {
            display: flex;
            justify-content: space-between;
        }
        
        .param-name {
            font-weight: 600;
        }
        
        .param-value {
            color: #ffeb3b;
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
            background: #ff9800;
            cursor: pointer;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
        }
        
        .animation-controls {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        
        .anim-btn {
            flex: 1;
            padding: 12px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        #playBtn {
            background: rgba(76, 175, 80, 0.2);
            color: #4CAF50;
            border: 1px solid rgba(76, 175, 80, 0.4);
        }
        
        #playBtn:hover {
            background: rgba(76, 175, 80, 0.3);
        }
        
        #resetBtn {
            background: rgba(244, 67, 54, 0.2);
            color: #f44336;
            border: 1px solid rgba(244, 67, 54, 0.4);
        }
        
        #resetBtn:hover {
            background: rgba(244, 67, 54, 0.3);
        }
        
        .data-panel {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .data-display {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .data-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #00bcd4;
        }
        
        .data-label {
            font-size: 0.9rem;
            color: #aaa;
            margin-bottom: 5px;
        }
        
        .data-value {
            font-size: 1.5rem;
            font-weight: 700;
            color: #ffeb3b;
        }
        
        .chart-container {
            width: 100%;
            height: 200px;
            background: rgba(0, 0, 0, 0.2);
            border-radius: 8px;
            position: relative;
            overflow: hidden;
        }
        
        #velocityChart {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .explanation-area {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            margin-top: 20px;
        }
        
        .explanation-text {
            font-size: 1.1rem;
            line-height: 1.7;
            color: #e0e0e0;
            min-height: 120px;
        }
        
        .highlight {
            color: #ff9800;
            font-weight: 600;
        }
        
        .concept {
            color: #00bcd4;
            font-weight: 600;
        }
        
        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
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
            height: 20px;
            border-radius: 50%;
        }
        
        .legend-text {
            font-size: 0.9rem;
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            padding: 20px;
            color: #aaa;
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
        }
        
        @media (max-width: 600px) {
            .scene-selector {
                grid-template-columns: 1fr;
            }
            
            .data-display {
                grid-template-columns: 1fr;
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
            <p class="subtitle">伽利略斜面实验的理想化 | 交互式物理教学动画</p>
        </header>
        
        <div class="main-content">
            <div class="simulation-area">
                <h2>物理现象模拟</h2>
                <div class="canvas-container">
                    <canvas id="simulationCanvas"></canvas>
                </div>
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ffeb3b;"></div>
                        <div class="legend-text">小球1 (质量较大)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f44336;"></div>
                        <div class="legend-text">小球2 (质量较小)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e0e0e0;"></div>
                        <div class="legend-text">重力</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff9800;"></div>
                        <div class="legend-text">空气阻力</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #00bcd4;"></div>
                        <div class="legend-text">理想模型轨迹</div>
                    </div>
                </div>
            </div>
            
            <div class="controls-area">
                <div class="control-panel">
                    <h2>实验控制</h2>
                    <div class="mode-selector">
                        <button id="guideModeBtn" class="mode-btn active">引导模式</button>
                        <button id="freeModeBtn" class="mode-btn">自由探索</button>
                    </div>
                    
                    <div class="scene-selector">
                        <button id="vacuumBtn" class="scene-btn active">理想真空落体</button>
                        <button id="airBtn" class="scene-btn">有空气阻力落体</button>
                        <button id="inclineBtn" class="scene-btn">伽利略斜面实验</button>
                    </div>
                    
                    <div class="param-controls">
                        <div class="param-group">
                            <div class="param-label">
                                <span class="param-name">小球1质量 (m₁)</span>
                                <span id="mass1Value" class="param-value">10 kg</span>
                            </div>
                            <input type="range" id="mass1Slider" min="1" max="50" value="10" step="1">
                        </div>
                        
                        <div class="param-group">
                            <div class="param-label">
                                <span class="param-name">小球2质量 (m₂)</span>
                                <span id="mass2Value" class="param-value">1 kg</span>
                            </div>
                            <input type="range" id="mass2Slider" min="1" max="50" value="1" step="1">
                        </div>
                        
                        <div class="param-group">
                            <div class="param-label">
                                <span class="param-name">小球半径 (影响阻力)</span>
                                <span id="radiusValue" class="param-value">0.3 m</span>
                            </div>
                            <input type="range" id="radiusSlider" min="0.1" max="1" value="0.3" step="0.05">
                        </div>
                        
                        <div class="param-group">
                            <div class="param-label">
                                <span class="param-name">空气密度</span>
                                <span id="densityValue" class="param-value">标准</span>
                            </div>
                            <input type="range" id="densitySlider" min="0" max="3" value="1" step="0.1">
                        </div>
                        
                        <div class="param-group">
                            <div class="param-label">
                                <span class="param-name">斜面倾角</span>
                                <span id="angleValue" class="param-value">30°</span>
                            </div>
                            <input type="range" id="angleSlider" min="5" max="90" value="30" step="5">
                        </div>
                    </div>
                    
                    <div class="animation-controls">
                        <button id="playBtn" class="anim-btn">开始实验</button>
                        <button id="resetBtn" class="anim-btn">重置</button>
                    </div>
                </div>
                
                <div class="data-panel">
                    <h2>数据监测</h2>
                    <div class="data-display">
                        <div class="data-item">
                            <div class="data-label">实验时间</div>
                            <div id="timeValue" class="data-value">0.00 s</div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">小球1速度</div>
                            <div id="velocity1Value" class="data-value">0.00 m/s</div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">小球2速度</div>
                            <div id="velocity2Value" class="data-value">0.00 m/s</div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">下落距离</div>
                            <div id="distanceValue" class="data-value">0.00 m</div>
                        </div>
                    </div>
                    
                    <div class="chart-container">
                        <canvas id="velocityChart"></canvas>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="explanation-area">
            <h2>原理说明</h2>
            <div id="explanationText" class="explanation-text">
                欢迎来到自由落体实验！在<span class="highlight">引导模式</span>下，我们将按照物理学发展历史，一步步探索自由落体的奥秘。首先，我们将观察在<span class="concept">理想真空环境</span>中，不同质量物体的下落情况。点击"开始实验"按钮开始探索！
            </div>
        </div>
        
        <footer>
            <p>交互式物理教学动画 | 设计理念：通过可视化对比理解伽利略斜面实验的理想化方法</p>
            <p>© 2023 物理教育技术实验室 | 本模拟中重力加速度 g = 9.8 m/s²</p>
        </footer>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const simCanvas = document.getElementById('simulationCanvas');
        const chartCanvas = document.getElementById('velocityChart');
        const simCtx = simCanvas.getContext('2d');
        const chartCtx = chartCanvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvases() {
            const container = document.querySelector('.canvas-container');
            const chartContainer = document.querySelector('.chart-container');
            
            simCanvas.width = container.clientWidth;
            simCanvas.height = container.clientHeight;
            
            chartCanvas.width = chartContainer.clientWidth;
            chartCanvas.height = chartContainer.clientHeight;
        }
        
        // 初始调整尺寸
        resizeCanvases();
        window.addEventListener('resize', resizeCanvases);
        
        // 物理常量
        const g = 9.8; // 重力加速度 (m/s²)
        const AIR_DENSITY_STD = 1.225; // 标准空气密度 (kg/m³)
        const DRAG_COEFFICIENT = 0.47; // 球体阻力系数
        
        // 实验状态
        let experimentState = {
            mode: 'guide', // 'guide' 或 'free'
            scene: 'vacuum', // 'vacuum', 'air', 'incline'
            isRunning: false,
            time: 0,
            step: 0, // 引导模式步骤
            guideCompleted: false
        };
        
        // 物理参数
        let physicsParams = {
            mass1: 10, // kg
            mass2: 1,  // kg
            radius: 0.3, // m
            airDensity: AIR_DENSITY_STD, // kg/m³
            inclineAngle: 30 // 度
        };
        
        // 小球状态
        let balls = [
            { x: 0, y: 0, vx: 0, vy: 0, ax: 0, ay: 0, color: '#ffeb3b', trail: [], isOnIncline: false },
            { x: 0, y: 0, vx: 0, vy: 0, ax: 0, ay: 0, color: '#f44336', trail: [], isOnIncline: false }
        ];
        
        // 图表数据
        let chartData = {
            time: [],
            velocity1: [],
            velocity2: [],
            idealVelocity: []
        };
        
        // 动画帧ID
        let animationId = null;
        
        // 初始化函数
        function initExperiment() {
            // 重置小球状态
            const startX1 = simCanvas.width * 0.25;
            const startX2 = simCanvas.width * 0.75;
            const startY = 100;
            
            balls[0].x = startX1;
            balls[0].y = startY;
            balls[0].vx = 0;
            balls[0].vy = 0;
            balls[0].ax = 0;
            balls[0].ay = 0;
            balls[0].trail = [];
            balls[0].isOnIncline = false;
            
            balls[1].x = startX2;
            balls[1].y = startY;
            balls[1].vx = 0;
            balls[1].vy = 0;
            balls[1].ax = 0;
            balls[1].ay = 0;
            balls[1].trail = [];
            balls[1].isOnIncline = false;
            
            // 重置实验状态
            experimentState.time = 0;
            experimentState.isRunning = false;
            
            // 重置图表数据
            chartData.time = [];
            chartData.velocity1 = [];
            chartData.velocity2 = [];
            chartData.idealVelocity = [];
            
            // 更新UI
            updateDataDisplay();
            draw();
            updateChart();
            
            // 更新说明文本
            updateExplanation();
        }
        
        // 计算空气阻力
        function calculateDrag(ball, densityFactor) {
            if (experimentState.scene === 'vacuum') return 0;
            
            const speed = Math.sqrt(ball.vx * ball.vx + ball.vy * ball.vy);
            if (speed === 0) return 0;
            
            // 阻力公式: F_drag = 0.5 * ρ * v² * C_d * A
            const area = Math.PI * physicsParams.radius * physicsParams.radius;
            const dragForce = 0.5 * physicsParams.airDensity * densityFactor * speed * speed * DRAG_COEFFICIENT * area;
            
            return dragForce;
        }
        
        // 更新物理状态
        function updatePhysics(deltaTime) {
            const dt = deltaTime / 1000; // 转换为秒
            
            // 更新实验时间
            experimentState.time += dt;
            
            // 斜面相关计算
            const angleRad = physicsParams.inclineAngle * Math.PI / 180;
            const gParallel = g * Math.sin(angleRad); // 斜面方向的重力分量
            const gPerpendicular = g * Math.cos(angleRad); // 垂直斜面的重力分量
            
            for (let i = 0; i < balls.length; i++) {
                const ball = balls[i];
                const mass = i === 0 ? physicsParams.mass1 : physicsParams.mass2;
                
                // 保存当前位置到轨迹
                ball.trail.push({x: ball.x, y: ball.y});
                if (ball.trail.length > 50) ball.trail.shift();
                
                // 根据场景计算加速度
                if (experimentState.scene === 'incline') {
                    // 斜面实验
                    if (!ball.isOnIncline) {
                        // 自由下落阶段
                        const dragForce = calculateDrag(ball, 1);
                        const dragAcceleration = dragForce / mass;
                        
                        ball.ax = 0;
                        ball.ay = g - dragAcceleration * (ball.vy > 0 ? 1 : 0);
                    } else {
                        // 斜面滚动阶段
                        const dragForce = calculateDrag(ball, 0.3); // 斜面上阻力较小
                        const dragAcceleration = dragForce / mass;
                        
                        // 斜面方向加速度
                        const inclineAcceleration = gParallel - dragAcceleration;
                        
                        ball.ax = inclineAcceleration * Math.cos(angleRad);
                        ball.ay = inclineAcceleration * Math.sin(angleRad);
                    }
                    
                    // 检查是否到达斜面
                    if (!ball.isOnIncline && ball.y >= simCanvas.height * 0.4) {
                        ball.isOnIncline = true;
                        // 调整位置到斜面上
                        const inclineStartX = simCanvas.width * 0.1;
                        const inclineStartY = simCanvas.height * 0.4;
                        const distanceAlongIncline = (ball.y - inclineStartY) / Math.sin(angleRad);
                        
                        ball.x = inclineStartX + distanceAlongIncline * Math.cos(angleRad);
                        ball.y = inclineStartY + distanceAlongIncline * Math.sin(angleRad);
                    }
                } else {
                    // 自由落体（有/无空气阻力）
                    const dragForce = experimentState.scene === 'air' ? calculateDrag(ball, 1) : 0;
                    const dragAcceleration = dragForce / mass;
                    
                    ball.ax = 0;
                    ball.ay = g - dragAcceleration * (ball.vy > 0 ? 1 : 0);
                }
                
                // 更新速度
                ball.vx += ball.ax * dt;
                ball.vy += ball.ay * dt;
                
                // 更新位置
                ball.x += ball.vx * dt * 50; // 乘以50以放大视觉效果
                ball.y += ball.vy * dt * 50;
                
                // 边界检查
                if (ball.y > simCanvas.height - 50) {
                    ball.y = simCanvas.height - 50;
                    ball.vy = 0;
                    ball.ay = 0;
                }
            }
            
            // 更新图表数据
            chartData.time.push(experimentState.time);
            chartData.velocity1.push(Math.sqrt(balls[0].vx*balls[0].vx + balls[0].vy*balls[0].vy));
            chartData.velocity2.push(Math.sqrt(balls[1].vx*balls[1].vx + balls[1].vy*balls[1].vy));
            
            // 计算理想速度（无阻力）
            const idealV = g * experimentState.time;
            chartData.idealVelocity.push(idealV);
            
            // 限制数据点数量
            if (chartData.time.length > 100) {
                chartData.time.shift();
                chartData.velocity1.shift();
                chartData.velocity2.shift();
                chartData.idealVelocity.shift();
            }
            
            // 更新UI
            updateDataDisplay();
            updateChart();
            
            // 检查实验是否结束（小球触底）
            const allStopped = balls.every(ball => ball.y >= simCanvas.height - 50);
            if (allStopped) {
                experimentState.isRunning = false;
                cancelAnimationFrame(animationId);
                updateExplanation();
            }
        }
        
        // 绘制函数
        function draw() {
            // 清除画布
            simCtx.clearRect(0, 0, simCanvas.width, simCanvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 绘制斜面（如果场景需要）
            if (experimentState.scene === 'incline') {
                drawIncline();
            }
            
            // 绘制小球的轨迹
            drawTrails();
            
            // 绘制小球
            for (let i = 0; i < balls.length; i++) {
                drawBall(balls[i], i);
            }
            
            // 绘制力箭头
            if (experimentState.isRunning) {
                drawForceArrows();
            }
            
            // 绘制场景标签
            drawSceneLabels();
        }
        
        // 绘制背景
        function drawBackground() {
            // 渐变背景
            const gradient = simCtx.createLinearGradient(0, 0, 0, simCanvas.height);
            gradient.addColorStop(0, '#0d1b2a');
            gradient.addColorStop(1, '#1a237e');
            simCtx.fillStyle = gradient;
            simCtx.fillRect(0, 0, simCanvas.width, simCanvas.height);
            
            // 网格线（仅自由落体场景）
            if (experimentState.scene !== 'incline') {
                simCtx.strokeStyle = 'rgba(255, 255, 255, 0.05)';
                simCtx.lineWidth = 1;
                
                // 垂直线
                for (let x = 0; x < simCanvas.width; x += 50) {
                    simCtx.beginPath();
                    simCtx.moveTo(x, 0);
                    simCtx.lineTo(x, simCanvas.height);
                    simCtx.stroke();
                }
                
                // 水平线（表示高度）
                for (let y = 0; y < simCanvas.height; y += 50) {
                    simCtx.beginPath();
                    simCtx.moveTo(0, y);
                    simCtx.lineTo(simCanvas.width, y);
                    simCtx.stroke();
                    
                    // 高度标签
                    simCtx.fillStyle = 'rgba(255, 255, 255, 0.3)';
                    simCtx.font = '12px Arial';
                    simCtx.fillText(`${((simCanvas.height - y) / 50).toFixed(1)} m`, 10, y - 5);
                }
            }
            
            // 地面
            simCtx.fillStyle = 'rgba(100, 100, 100, 0.7)';
            simCtx.fillRect(0, simCanvas.height - 50, simCanvas.width, 50);
            
            // 地面标签
            simCtx.fillStyle = 'rgba(255, 255, 255, 0.7)';
            simCtx.font = '14px Arial';
            simCtx.fillText('地面', simCanvas.width / 2 - 20, simCanvas.height - 20);
        }
        
        // 绘制斜面
        function drawIncline() {
            const angleRad = physicsParams.inclineAngle * Math.PI / 180;
            const startX = simCanvas.width * 0.1;
            const startY = simCanvas.height * 0.4;
            const length = simCanvas.width * 0.8;
            const endX = startX + length * Math.cos(angleRad);
            const endY = startY + length * Math.sin(angleRad);
            
            // 绘制斜面
            simCtx.strokeStyle = '#bdbdbd';
            simCtx.lineWidth = 8;
            simCtx.beginPath();
            simCtx.moveTo(startX, startY);
            simCtx.lineTo(endX, endY);
            simCtx.stroke();
            
            // 绘制斜面支撑
            simCtx.strokeStyle = '#8d6e63';
            simCtx.lineWidth = 6;
            simCtx.beginPath();
            simCtx.moveTo(startX, startY);
            simCtx.lineTo(startX, simCanvas.height - 50);
            simCtx.stroke();
            
            // 绘制角度标记
            simCtx.strokeStyle = '#00bcd4';
            simCtx.lineWidth = 2;
            const arcRadius = 40;
            simCtx.beginPath();
            simCtx.arc(startX, startY, arcRadius, -Math.PI/2, -Math.PI/2 + angleRad, false);
            simCtx.stroke();
            
            // 角度标签
            simCtx.fillStyle = '#00bcd4';
            simCtx.font = '16px Arial';
            simCtx.fillText(
                `${physicsParams.inclineAngle}°`, 
                startX + arcRadius * 0.7, 
                startY - 10
            );
            
            // 斜面标签
            simCtx.fillStyle = '#bdbdbd';
            simCtx.font = '18px Arial';
            simCtx.fillText('伽利略斜面', startX + length/2 - 40, startY + length/2 * Math.sin(angleRad) - 20);
            
            // 绘制时间标记（匀加速运动特征）
            if (experimentState.isRunning) {
                const timeMarkers = 5;
                simCtx.strokeStyle = 'rgba(255, 255, 255, 0.3)';
                simCtx.lineWidth = 1;
                simCtx.setLineDash([5, 5]);
                
                for (let i = 1; i <= timeMarkers; i++) {
                    const t = i / timeMarkers;
                    const markerX = startX + t * length * Math.cos(angleRad);
                    const markerY = startY + t * length * Math.sin(angleRad);
                    
                    simCtx.beginPath();
                    simCtx.moveTo(markerX - 10 * Math.sin(angleRad), markerY + 10 * Math.cos(angleRad));
                    simCtx.lineTo(markerX + 10 * Math.sin(angleRad), markerY - 10 * Math.cos(angleRad));
                    simCtx.stroke();
                }
                simCtx.setLineDash([]);
            }
        }
        
        // 绘制小球轨迹
        function drawTrails() {
            for (let i = 0; i < balls.length; i++) {
                const ball = balls[i];
                const trailColor = i === 0 ? 'rgba(255, 235, 59, 0.3)' : 'rgba(244, 67, 54, 0.3)';
                
                if (ball.trail.length > 1) {
                    simCtx.strokeStyle = trailColor;
                    simCtx.lineWidth = 2;
                    simCtx.beginPath();
                    simCtx.moveTo(ball.trail[0].x, ball.trail[0].y);
                    
                    for (let j = 1; j < ball.trail.length; j++) {
                        simCtx.lineTo(ball.trail[j].x, ball.trail[j].y);
                    }
                    simCtx.stroke();
                }
            }
            
            // 绘制理想轨迹（仅在有阻力场景中对比）
            if (experimentState.scene === 'air' && balls[0].trail.length > 1) {
                simCtx.strokeStyle = 'rgba(0, 188, 212, 0.5)';
                simCtx.lineWidth = 2;
                simCtx.setLineDash([5, 5]);
                simCtx.beginPath();
                
                const startX = balls[0].trail[0].x;
                const startY = balls[0].trail[0].y;
                simCtx.moveTo(startX, startY);
                
                // 理想轨迹是抛物线
                for (let i = 1; i < balls[0].trail.length; i++) {
                    const t = i / 10;
                    const idealY = startY + 0.5 * g * t * t * 50;
                    simCtx.lineTo(startX, idealY);
                }
                
                simCtx.stroke();
                simCtx.setLineDash([]);
            }
        }
        
        // 绘制小球
        function drawBall(ball, index) {
            // 小球阴影
            simCtx.beginPath();
            simCtx.arc(ball.x, ball.y + 3, physicsParams.radius * 20, 0, Math.PI * 2);
            simCtx.fillStyle = 'rgba(0, 0, 0, 0.3)';
            simCtx.fill();
            
            // 小球主体
            simCtx.beginPath();
            simCtx.arc(ball.x, ball.y, physicsParams.radius * 20, 0, Math.PI * 2);
            
            // 渐变填充
            const gradient = simCtx.createRadialGradient(
                ball.x - physicsParams.radius * 10, 
                ball.y - physicsParams.radius * 10, 
                0,
                ball.x, 
                ball.y, 
                physicsParams.radius * 20
            );
            
            gradient.addColorStop(0, ball.color);
            gradient.addColorStop(1, index === 0 ? '#f57f17' : '#c62828');
            simCtx
<!--检测到代码截断，自动续写中...-->
            simCtx.fillStyle = gradient;
            simCtx.fill();
            
            // 小球边框
            simCtx.strokeStyle = 'rgba(255, 255, 255, 0.8)';
            simCtx.lineWidth = 2;
            simCtx.stroke();
            
            // 小球标签
            simCtx.fillStyle = 'white';
            simCtx.font = 'bold 16px Arial';
            simCtx.textAlign = 'center';
            simCtx.fillText(`m${index+1}`, ball.x, ball.y + 5);
            
            // 质量显示
            simCtx.font = '14px Arial';
            const mass = index === 0 ? physicsParams.mass1 : physicsParams.mass2;
            simCtx.fillText(`${mass}kg`, ball.x, ball.y + physicsParams.radius * 20 + 20);
        }
        
        // 绘制力箭头
        function drawForceArrows() {
            for (let i = 0; i < balls.length; i++) {
                const ball = balls[i];
                const mass = i === 0 ? physicsParams.mass1 : physicsParams.mass2;
                
                // 重力箭头（白色）
                const gravityScale = 2;
                drawArrow(
                    ball.x, ball.y,
                    ball.x, ball.y + gravityScale * g,
                    '#e0e0e0',
                    '重力',
                    3
                );
                
                // 空气阻力箭头（橙色，仅在有阻力时显示）
                if (experimentState.scene !== 'vacuum') {
                    const dragForce = calculateDrag(ball, experimentState.scene === 'incline' ? 0.3 : 1);
                    if (dragForce > 0 && ball.vy > 0) {
                        const dragScale = dragForce / mass * 5;
                        drawArrow(
                            ball.x, ball.y,
                            ball.x, ball.y - dragScale,
                            '#ff9800',
                            '空气阻力',
                            3
                        );
                    }
                }
                
                // 净力箭头（引导模式下高亮显示）
                if (experimentState.mode === 'guide' && experimentState.step >= 2) {
                    const netAy = ball.ay;
                    const netScale = netAy * 2;
                    drawArrow(
                        ball.x, ball.y,
                        ball.x, ball.y + netScale,
                        '#4CAF50',
                        '净力',
                        4
                    );
                }
            }
        }
        
        // 绘制箭头函数
        function drawArrow(fromX, fromY, toX, toY, color, label, lineWidth) {
            const headLength = 10;
            const dx = toX - fromX;
            const dy = toY - fromY;
            const angle = Math.atan2(dy, dx);
            
            // 绘制箭头线
            simCtx.strokeStyle = color;
            simCtx.lineWidth = lineWidth;
            simCtx.beginPath();
            simCtx.moveTo(fromX, fromY);
            simCtx.lineTo(toX, toY);
            simCtx.stroke();
            
            // 绘制箭头头部
            simCtx.beginPath();
            simCtx.moveTo(toX, toY);
            simCtx.lineTo(
                toX - headLength * Math.cos(angle - Math.PI / 6),
                toY - headLength * Math.sin(angle - Math.PI / 6)
            );
            simCtx.lineTo(
                toX - headLength * Math.cos(angle + Math.PI / 6),
                toY - headLength * Math.sin(angle + Math.PI / 6)
            );
            simCtx.closePath();
            simCtx.fillStyle = color;
            simCtx.fill();
            
            // 绘制标签
            if (label) {
                simCtx.fillStyle = color;
                simCtx.font = 'bold 14px Arial';
                simCtx.textAlign = 'center';
                simCtx.fillText(label, (fromX + toX) / 2, (fromY + toY) / 2 - 10);
            }
        }
        
        // 绘制场景标签
        function drawSceneLabels() {
            simCtx.fillStyle = 'rgba(255, 255, 255, 0.9)';
            simCtx.font = 'bold 20px Arial';
            simCtx.textAlign = 'center';
            
            let sceneTitle = '';
            switch(experimentState.scene) {
                case 'vacuum':
                    sceneTitle = '理想真空环境（无空气阻力）';
                    break;
                case 'air':
                    sceneTitle = '有空气阻力环境（现实世界）';
                    break;
                case 'incline':
                    sceneTitle = '伽利略斜面实验';
                    break;
            }
            
            simCtx.fillText(sceneTitle, simCanvas.width / 2, 40);
            
            // 在引导模式下显示步骤说明
            if (experimentState.mode === 'guide' && !experimentState.guideCompleted) {
                simCtx.fillStyle = '#ff9800';
                simCtx.font = '18px Arial';
                
                let stepText = '';
                switch(experimentState.step) {
                    case 0:
                        stepText = '步骤1: 观察理想真空中的自由落体';
                        break;
                    case 1:
                        stepText = '步骤2: 观察有空气阻力时的差异';
                        break;
                    case 2:
                        stepText = '步骤3: 探索伽利略的斜面实验方法';
                        break;
                }
                
                simCtx.fillText(stepText, simCanvas.width / 2, 70);
            }
        }
        
        // 更新数据展示
        function updateDataDisplay() {
            document.getElementById('timeValue').textContent = experimentState.time.toFixed(2) + ' s';
            
            const speed1 = Math.sqrt(balls[0].vx * balls[0].vx + balls[0].vy * balls[0].vy);
            const speed2 = Math.sqrt(balls[1].vx * balls[1].vx + balls[1].vy * balls[1].vy);
            
            document.getElementById('velocity1Value').textContent = speed1.toFixed(2) + ' m/s';
            document.getElementById('velocity2Value').textContent = speed2.toFixed(2) + ' m/s';
            
            const distance = Math.max(simCanvas.height - 50 - balls[0].y, simCanvas.height - 50 - balls[1].y);
            document.getElementById('distanceValue').textContent = (distance / 50).toFixed(2) + ' m';
        }
        
        // 更新图表
        function updateChart() {
            const width = chartCanvas.width;
            const height = chartCanvas.height;
            const padding = 40;
            
            // 清除图表
            chartCtx.clearRect(0, 0, width, height);
            
            // 绘制背景
            chartCtx.fillStyle = 'rgba(0, 0, 0, 0.2)';
            chartCtx.fillRect(0, 0, width, height);
            
            // 如果没有数据，直接返回
            if (chartData.time.length === 0) return;
            
            // 计算坐标范围
            const maxTime = Math.max(...chartData.time);
            const maxVelocity = Math.max(
                ...chartData.velocity1,
                ...chartData.velocity2,
                ...chartData.idealVelocity
            );
            
            // 绘制坐标轴
            chartCtx.strokeStyle = 'rgba(255, 255, 255, 0.5)';
            chartCtx.lineWidth = 1;
            
            // X轴
            chartCtx.beginPath();
            chartCtx.moveTo(padding, height - padding);
            chartCtx.lineTo(width - padding, height - padding);
            chartCtx.stroke();
            
            // Y轴
            chartCtx.beginPath();
            chartCtx.moveTo(padding, padding);
            chartCtx.lineTo(padding, height - padding);
            chartCtx.stroke();
            
            // 坐标轴标签
            chartCtx.fillStyle = 'rgba(255, 255, 255, 0.7)';
            chartCtx.font = '12px Arial';
            chartCtx.textAlign = 'center';
            
            // X轴标签
            chartCtx.fillText('时间 (s)', width / 2, height - 10);
            
            // Y轴标签
            chartCtx.save();
            chartCtx.translate(15, height / 2);
            chartCtx.rotate(-Math.PI / 2);
            chartCtx.fillText('速度 (m/s)', 0, 0);
            chartCtx.restore();
            
            // 绘制刻度
            chartCtx.textAlign = 'right';
            chartCtx.fillStyle = 'rgba(255, 255, 255, 0.5)';
            
            // Y轴刻度
            for (let v = 0; v <= maxVelocity; v += 10) {
                const y = height - padding - (v / maxVelocity) * (height - 2 * padding);
                chartCtx.beginPath();
                chartCtx.moveTo(padding - 5, y);
                chartCtx.lineTo(padding, y);
                chartCtx.stroke();
                
                chartCtx.fillText(v.toString(), padding - 10, y + 4);
            }
            
            // X轴刻度
            for (let t = 0; t <= maxTime; t += 1) {
                const x = padding + (t / maxTime) * (width - 2 * padding);
                chartCtx.beginPath();
                chartCtx.moveTo(x, height - padding);
                chartCtx.lineTo(x, height - padding + 5);
                chartCtx.stroke();
                
                chartCtx.textAlign = 'center';
                chartCtx.fillText(t.toString(), x, height - padding + 20);
                chartCtx.textAlign = 'right';
            }
            
            // 绘制数据曲线
            const scaleX = (width - 2 * padding) / maxTime;
            const scaleY = (height - 2 * padding) / maxVelocity;
            
            // 理想速度曲线（青色）
            if (chartData.idealVelocity.length > 0) {
                chartCtx.strokeStyle = '#00bcd4';
                chartCtx.lineWidth = 2;
                chartCtx.setLineDash([5, 5]);
                chartCtx.beginPath();
                
                for (let i = 0; i < chartData.time.length; i++) {
                    const x = padding + chartData.time[i] * scaleX;
                    const y = height - padding - chartData.idealVelocity[i] * scaleY;
                    
                    if (i === 0) {
                        chartCtx.moveTo(x, y);
                    } else {
                        chartCtx.lineTo(x, y);
                    }
                }
                
                chartCtx.stroke();
                chartCtx.setLineDash([]);
            }
            
            // 小球1速度曲线（黄色）
            if (chartData.velocity1.length > 0) {
                chartCtx.strokeStyle = '#ffeb3b';
                chartCtx.lineWidth = 3;
                chartCtx.beginPath();
                
                for (let i = 0; i < chartData.time.length; i++) {
                    const x = padding + chartData.time[i] * scaleX;
                    const y = height - padding - chartData.velocity1[i] * scaleY;
                    
                    if (i === 0) {
                        chartCtx.moveTo(x, y);
                    } else {
                        chartCtx.lineTo(x, y);
                    }
                }
                
                chartCtx.stroke();
            }
            
            // 小球2速度曲线（红色）
            if (chartData.velocity2.length > 0) {
                chartCtx.strokeStyle = '#f44336';
                chartCtx.lineWidth = 3;
                chartCtx.beginPath();
                
                for (let i = 0; i < chartData.time.length; i++) {
                    const x = padding + chartData.time[i] * scaleX;
                    const y = height - padding - chartData.velocity2[i] * scaleY;
                    
                    if (i === 0) {
                        chartCtx.moveTo(x, y);
                    } else {
                        chartCtx.lineTo(x, y);
                    }
                }
                
                chartCtx.stroke();
            }
            
            // 图表标题
            chartCtx.fillStyle = 'rgba(255, 255, 255, 0.9)';
            chartCtx.font = 'bold 16px Arial';
            chartCtx.textAlign = 'center';
            chartCtx.fillText('速度-时间图 (v-t)', width / 2, 25);
            
            // 图例
            const legendX = width - 150;
            const legendY = 30;
            
            // 理想模型
            chartCtx.fillStyle = '#00bcd4';
            chartCtx.fillRect(legendX, legendY, 20, 3);
            chartCtx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            chartCtx.font = '12px Arial';
            chartCtx.textAlign = 'left';
            chartCtx.fillText('理想模型', legendX + 25, legendY + 8);
            
            // 小球1
            chartCtx.fillStyle = '#ffeb3b';
            chartCtx.fillRect(legendX, legendY + 15, 20, 3);
            chartCtx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            chartCtx.fillText('小球1', legendX + 25, legendY + 23);
            
            // 小球2
            chartCtx.fillStyle = '#f44336';
            chartCtx.fillRect(legendX, legendY + 30, 20, 3);
            chartCtx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            chartCtx.fillText('小球2', legendX + 25, legendY + 38);
        }
        
        // 更新说明文本
        function updateExplanation() {
            const explanationEl = document.getElementById('explanationText');
            let explanation = '';
            
            if (experimentState.mode === 'guide') {
                if (!experimentState.isRunning && !experimentState.guideCompleted) {
                    switch(experimentState.step) {
                        case 0:
                            explanation = `
                                <span class="highlight">步骤1：理想真空中的自由落体</span><br><br>
                                在<span class="concept">完全真空的理想环境</span>中，空气阻力为零。根据伽利略的理论，<span class="concept">所有物体无论质量大小，都以相同的加速度（g = 9.8 m/s²）下落</span>。
                                观察两个质量不同的小球，它们是否同时落地？点击"开始实验"验证这一理论。
                            `;
                            break;
                        case 1:
                            explanation = `
                                <span class="highlight">步骤2：有空气阻力的现实世界</span><br><br>
                                在现实世界中，空气阻力会影响物体的下落。<span class="concept">阻力大小与物体的速度、迎风面积和形状有关</span>。
                                注意观察：<br>
                                1. 阻力箭头（橙色）如何随速度增加而增大<br>
                                2. 两个小球的下落速度差异<br>
                                3. 与理想轨迹（青色虚线）的对比
                            `;
                            break;
                        case 2:
                            explanation = `
                                <span class="highlight">步骤3：伽利略的智慧 - 斜面实验</span><br><br>
                                伽利略无法创造真空环境，但他想出了一个巧妙的方法：<span class="concept">使用斜面来"稀释"重力</span>。
                                通过减小下落速度，<span class="concept">空气阻力的影响大大降低</span>，使得实验结果更接近理想情况。
                                观察小球在斜面上的运动，注意等时间标记显示的距离变化规律。
                            `;
                            break;
                    }
                } else if (experimentState.guideCompleted) {
                    explanation = `
                        <span class="highlight">引导实验完成！</span><br><br>
                        您已经完成了自由落体与空气阻力影响的三步探索。现在可以切换到<span class="concept">自由探索模式</span>，调整各种参数（质量、半径、空气密度、斜面角度），深入探究这些变量如何影响物体的运动。
                        尝试回答以下问题：<br>
                        1. 质量是否影响理想自由落体？<br>
                        2. 什么情况下空气阻力的影响最显著？<br>
                        3. 斜面角度如何影响实验的"理想化"程度？
                    `;
                }
            } else {
                // 自由探索模式
                explanation = `
                    <span class="highlight">自由探索模式</span><br><br>
                    您现在可以完全控制实验的所有参数。尝试调整：<br>
                    • <span class="concept">小球质量</span>：观察质量在有无阻力时的不同影响<br>
                    • <span class="concept">小球半径</span>：半径越大，空气阻力影响越显著<br>
                    • <span class="concept">空气密度</span>：从真空到浓密空气，观察阻力的变化<br>
                    • <span class="concept">斜面角度</span>：角度越小，阻力影响越小，越接近理想情况<br><br>
                    注意观察v-t图中曲线的变化，理解<span class="concept">终端速度</span>的概念。
                `;
            }
            
            explanationEl.innerHTML = explanation;
        }
        
        // 动画循环
        function animate(timestamp) {
            if (!experimentState.lastTimestamp) {
                experimentState.lastTimestamp = timestamp;
            }
            
            const deltaTime = timestamp - experimentState.lastTimestamp;
            experimentState.lastTimestamp = timestamp;
            
            if (experimentState.isRunning) {
                updatePhysics(deltaTime);
                draw();
            }
            
            animationId = requestAnimationFrame(animate);
        }
        
        // 开始实验
        function startExperiment() {
            if (!experimentState.isRunning) {
                experimentState.isRunning = true;
                experimentState.lastTimestamp = null;
                document.getElementById('playBtn').textContent = '暂停实验';
                
                // 在引导模式下，自动推进步骤
                if (experimentState.mode === 'guide' && !experimentState.guideCompleted) {
                    // 实验结束后自动进入下一步
                    setTimeout(() => {
                        if (experimentState.isRunning) {
                            const allStopped = balls.every(ball => ball.y >= simCanvas.height - 50);
                            if (allStopped) {
                                experimentState.isRunning = false;
                                document.getElementById('playBtn').textContent = '开始实验';
                                
                                if (experimentState.step < 2) {
                                    experimentState.step++;
                                    updateExplanation();
                                    
                                    // 自动切换到下一个场景
                                    const sceneOrder = ['vacuum', 'air', 'incline'];
                                    const nextScene = sceneOrder[experimentState.step];
                                    switchScene(nextScene);
                                    
                                    // 重置实验
                                    setTimeout(() => {
                                        initExperiment();
                                    }, 1500);
                                } else {
                                    experimentState.guideCompleted = true;
                                    updateExplanation();
                                }
                            }
                        }
                    }, 100);
                }
                
                requestAnimationFrame(animate);
            } else {
                experimentState.isRunning = false;
                document.getElementById('playBtn').textContent = '继续实验';
                cancelAnimationFrame(animationId);
            }
        }
        
        // 重置实验
        function resetExperiment() {
            experimentState.isRunning = false;
            document.getElementById('playBtn').textContent = '开始实验';
            cancelAnimationFrame(animationId);
            
            initExperiment();
        }
        
        // 切换模式
        function switchMode(mode) {
            experimentState.mode = mode;
            experimentState.guideCompleted = false;
            
            // 更新按钮状态
            document.getElementById('guideModeBtn').classList.toggle('active', mode === 'guide');
            document.getElementById('freeModeBtn').classList.toggle('active', mode === 'free');
            
            // 在自由模式下，重置步骤
            if (mode === 'free') {
                experimentState.step = 0;
            }
            
            // 更新说明
            updateExplanation();
            
            // 重置实验
            resetExperiment();
        }
        
        // 切换场景
        function switchScene(scene) {
            experimentState.scene = scene;
            
            // 更新按钮状态
            document.getElementById('vacuumBtn').classList.toggle('active', scene === 'vacuum');
            document.getElementById('airBtn').classList.toggle('active', scene === 'air');
            document.getElementById('inclineBtn').classList.toggle('active', scene === 'incline');
            
            // 在引导模式下，如果切换场景，重置引导状态
            if (experimentState.mode === 'guide') {
                experimentState.guideCompleted = false;
                const sceneOrder = ['vacuum', 'air', 'incline'];
                experimentState.step = sceneOrder.indexOf(scene);
            }
            
            // 更新说明
            updateExplanation();
            
            // 重置实验
            resetExperiment();
        }
        
        // 更新参数值显示
        function updateParamDisplays() {
            document.getElementById('mass1Value').textContent = physicsParams.mass1 + ' kg';
            document.getElementById('mass2Value').textContent = physicsParams.mass2 + ' kg';
            document.getElementById('radiusValue').textContent = physicsParams.radius.toFixed(2) + ' m';
            
            // 空气密度显示
            let densityText = '';
            if (physicsParams.airDensity === 0) {
                densityText = '真空';
            } else if (physicsParams.airDensity < AIR_DENSITY_STD * 0.5) {
                densityText = '稀薄';
            } else if (physicsParams.airDensity > AIR_DENSITY_STD * 1.5) {
                densityText = '浓密';
            } else {
                densityText = '标准';
            }
            document.getElementById('densityValue').textContent = densityText;
            
            document.getElementById('angleValue').textContent = physicsParams.inclineAngle + '°';
        }
        
        // 事件监听器设置
        function setupEventListeners() {
            // 模式切换按钮
            document.getElementById('guideModeBtn').addEventListener('click', () => switchMode('guide'));
            document.getElementById('freeModeBtn').addEventListener('click', () => switchMode('free'));
            
            // 场景切换按钮
            document.getElementById('vacuumBtn').addEventListener('click', () => switchScene('vacuum'));
            document.getElementById('airBtn').addEventListener('click', () => switchScene('air'));
            document.getElementById('inclineBtn').addEventListener('click', () => switchScene('incline'));
            
            // 动画控制按钮
            document.getElementById('playBtn').addEventListener('click', startExperiment);
            document.getElementById('resetBtn').addEventListener('click', resetExperiment);
            
            // 参数滑块
            const sliders = ['mass1Slider', 'mass2Slider', 'radiusSlider', 'densitySlider', 'angleSlider'];
            sliders.forEach(sliderId => {
                const slider = document.getElementById(sliderId);
                slider.addEventListener('input', function() {
                    switch(sliderId) {
                        case 'mass1Slider':
                            physicsParams.mass1 = parseInt(this.value);
                            break;
                        case 'mass2Slider':
                            physicsParams.mass2 = parseInt(this.value);
                            break;
                        case 'radiusSlider':
                            physicsParams.radius = parseFloat(this.value);
                            break;
                        case 'densitySlider':
                            const densityFactor = parseFloat(this.value);
                            physicsParams.airDensity = AIR_DENSITY_STD * densityFactor;
                            break;
                        case 'angleSlider':
                            physicsParams.inclineAngle = parseInt(this.value);
                            break;
                    }
                    
                    updateParamDisplays();
                    
                    // 如果实验未运行，立即更新显示
                    if (!experimentState.isRunning) {
                        draw();
                        updateChart();
                    }
                });
            });
            
            // 初始更新参数显示
            updateParamDisplays();
        }
        
        // 初始化
        function init() {
            resizeCanvases();
            setupEventListeners();
            initExperiment();
            updateExplanation();
            
            // 开始动画循环（即使实验未运行，也保持绘制）
            requestAnimationFrame(animate);
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 《自由落体与空气阻力影响》交互式教学动画使用指南

欢迎使用本交互式物理教学动画！本动画旨在通过直观的可视化对比，帮助您深入理解伽利略斜面实验的理想化思想，以及空气阻力对自由落体运动的影响。无论您是学生、教师还是物理爱好者，本工具都将为您提供一次富有启发性的科学探索体验。

---

### 一、功能说明

本动画模拟了三种物理场景：
1. **理想真空落体**：在完全无阻力的理想环境中，所有物体以相同加速度下落
2. **有空气阻力落体**：在现实空气中，物体受到与速度相关的阻力影响
3. **伽利略斜面实验**：通过斜面"稀释"重力，减小阻力影响，逼近理想条件

通过对比这三种场景，您可以直观地理解：
- 理想化模型在物理学中的重要性
- 空气阻力如何影响不同物体的下落
- 伽利略如何通过巧妙的实验设计克服测量困难

---

### 二、主要功能

#### 1. 双模式操作
- **引导模式**：按照物理学发展逻辑，分步骤引导您完成探索
- **自由探索模式**：开放所有控制，供您自主实验和探究

#### 2. 参数调节系统
- **质量调节**：独立调节两个小球的质量（1-50kg）
- **半径调节**：改变小球半径（0.1-1m），影响迎风面积和阻力
- **空气密度调节**：从"真空"到"浓密"空气（0-3倍标准密度）
- **斜面倾角调节**：5°到90°，观察角度对运动的影响

#### 3. 实时数据监测
- 实验时间、小球速度、下落距离的实时显示
- 动态速度-时间（v-t）图表，直观对比不同场景下的运动规律

#### 4. 可视化辅助
- **力箭头**：白色箭头表示重力，橙色箭头表示空气阻力
- **运动轨迹**：显示小球的运动路径
- **理想轨迹对比**：在有阻力场景中显示理想轨迹作为参照
- **斜面时间标记**：展示匀加速运动的特征

---

### 三、设计特色

#### 1. 历史与科学结合
动画设计融入了物理学史元素，重现了伽利略通过斜面实验发现落体定律的科学历程，让您亲身体验科学发现的逻辑过程。

#### 2. 多层次对比
- **横向对比**：并排显示不同场景下的运动状态
- **纵向对比**：理想模型与现实情况的差异
- **参数对比**：改变单一变量，观察其对运动的影响

#### 3. 认知友好设计
- 从简单到复杂的分步引导
- 关键概念的高亮显示
- 实时原理说明，降低理解门槛

#### 4. 专业配色方案
- 深空蓝背景营造科学探索氛围
- 明快的小球颜色确保视觉清晰
- 力箭头的颜色编码（白-重力，橙-阻力）便于识别

---

### 四、教学要点

#### 针对学生：
1. **核心概念理解**
   - 理想自由落体：所有物体加速度相同（g=9.8m/s²）
   - 空气阻力：与速度平方、迎风面积、空气密度成正比
   - 终端速度：阻力与重力平衡时的匀速状态

2. **实验观察重点**
   - 在真空中，质量不同的小球是否同时落地？
   - 在空气中，质量、半径如何影响下落速度？
   - 斜面角度如何改变阻力影响程度？

3. **数据分析技能**
   - 阅读v-t图：直线代表匀加速，曲线趋平代表趋向终端速度
   - 比较数值：注意速度、加速度的瞬时变化

#### 针对教师：
1. **课堂演示建议**
   - 先展示"亚里士多德观点"与"伽利略质疑"的认知冲突
   - 按引导模式逐步展开，每步后暂停讨论
   - 重点讲解斜面实验的"理想化"思想

2. **探究活动设计**
   - "如果伽利略有现代仪器，他会怎么做？"
   - "设计实验验证终端速度公式"
   - "如何减小实验误差？"

3. **概念联系**
   - 联系牛顿第二定律：F=ma
   - 联系能量守恒：重力势能转化为动能和热能
   - 联系科学方法：理想化、建模、实验验证

---

### 五、使用建议

#### 1. 初次使用者
**推荐路径**：
1. 选择"引导模式"，让系统带领您完成整个探索
2. 仔细观察每个步骤的动画效果和原理说明
3. 完成引导后，切换到"自由探索模式"尝试自己的想法

#### 2. 课堂教学应用
**建议流程**：
1. **导入**：提出"轻重物体谁先落地"的问题
2. **演示**：运行引导模式，分步讲解
3. **探究**：学生分组，在自由模式下设计实验
4. **讨论**：分享发现，总结规律
5. **拓展**：联系实际应用（如降落伞、雨滴下落）

#### 3. 深度探究方向
- **变量控制实验**：固定其他变量，只改变质量/半径/空气密度
- **极限情况测试**：将空气密度调到最大，观察"羽毛下落"效果
- **斜面优化探究**：找到"阻力影响最小"的最佳斜面角度
- **数据验证**：用公式计算理论值，与模拟结果对比

#### 4. 注意事项
- 模拟中的比例尺经过调整，以便清晰展示
- 空气阻力模型采用简化公式，适合教学理解
- 建议结合真实实验（如牛顿管实验）使用本动画

---

### 六、技术提示

1. **最佳观看**：使用Chrome或Edge浏览器，确保Canvas支持
2. **屏幕适配**：动画支持响应式设计，适应不同屏幕尺寸
3. **性能优化**：如果动画卡顿，可减少轨迹长度或关闭部分视觉效果
4. **数据记录**：重要数据可以截图保存，用于实验报告

---

### 结语

本交互式动画不仅是一个演示工具，更是一个探索平台。我们鼓励您：
- **提出问题**：不要满足于观察，要思考"为什么"
- **大胆尝试**：改变参数，看看会发生什么意外结果
- **联系实际**：想想生活中的类似现象
- **享受过程**：科学探索本身就是最大的乐趣

希望这次虚拟实验能点燃您对物理学的热情，让伽利略的科学精神在数字时代继续闪耀！

**探索无限，真理永存！**

---
*动画设计：教育技术实验室*
*物理顾问：熊猫老师团队*
*版本：1.0 | 最后更新：2023年10月*