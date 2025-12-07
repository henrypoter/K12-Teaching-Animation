# 需求：重力加速度测量（真实实验误差大，动画可做到0阻力）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画的目标用户主要是**高中物理学生**和**大学物理初学者**。他们的核心需求是：
1.  **理解核心原理**：直观理解自由落体运动中重力加速度 `g` 的测量原理（`h = 1/2 * g * t^2`），以及理想无阻力环境与真实实验的差异。
2.  **掌握实验方法**：学习如何使用光电门、打点计时器等工具测量下落时间 `t` 和高度 `h`，并计算 `g`。
3.  **探究误差来源**：明确认识到空气阻力、测量精度（如计时误差、高度测量误差）是导致真实实验 `g` 值测量不准或偏小的主要原因。
4.  **获得理想参照**：在动画创造的“理想零阻力”环境中，观察“完美”数据，与真实实验数据形成对比，加深对理论公式和误差来源的理解。
5.  **互动与探究**：能够通过调整参数（如高度、物体质量/形状、是否开启空气阻力）来观察不同条件下的运动与测量结果，进行探究式学习。

#### 教学设计思路
*   **核心概念**：重力加速度 `g`、自由落体运动公式、实验测量法（光电门/打点计时器）、系统误差与偶然误差、空气阻力的影响。
*   **认知规律**：
    *   **从理想模型到现实复杂化**：首先展示无阻力、完美的自由落体动画和精确测量，建立理想认知模型。然后引入“空气阻力”这一因素，观察数据如何偏离理想值，符合“先建立理想模型，再考虑实际情况”的认知顺序。
    *   **对比学习**：并排或可切换地展示“理想实验”与“模拟真实实验”，让差异可视化，强化理解。
    *   **控制变量探究**：允许用户独立改变一个变量（如高度、物体形状），观察其对运动时间 `t` 和计算结果 `g` 的影响，培养科学探究思维。
*   **交互设计**：
    *   **场景化界面**：设计一个虚拟的实验室场景，包含测量尺、光电门、释放装置、数据展示面板等元素。
    *   **分步引导与自由探索结合**：可设置“引导模式”分步讲解实验，并提供一个“自由实验模式”，让用户自主操作。
    *   **即时反馈**：物体下落时，实时显示时间、瞬时速度；落地后，立即在数据面板显示测量出的 `g` 值，并与理论值（如9.8 m/s²）对比，用颜色（绿色/红色）高亮显示误差大小。
    *   **参数控制面板**：提供清晰的滑块或输入框，用于调整下落高度、物体属性（质量、形状：球体、纸片等）、空气阻力开关及强度。
*   **视觉呈现**：
    *   **主体突出**：下落物体（如小球）要清晰，运动轨迹平滑。测量工具（光电门的光束、打点计时器的纸带）要有明确的视觉提示。
    *   **数据可视化**：除了数字，可以用动态图表辅助理解，例如：
        *   实时绘制 `h-t` 图或 `v-t` 图。
        *   用不同长度的箭头表示重力与空气阻力的大小和方向。
    *   **运动细节**：在开启空气阻力时，可以示意性地绘制物体后的“流线”或粒子效果，暗示阻力的存在；物体若轻（如纸片），可呈现飘落效果，与小球形成鲜明对比。

#### 配色方案选择
*   **主色调**：采用**科技蓝**与**实验室白**。背景和主面板以浅灰色或白色为主，营造干净、专业的实验室氛围。关键交互元素和重点数据使用蓝色系，传达理性与科学感。
*   **辅助色与强调色**：
    *   **绿色**：用于表示正确的操作、理想状态的数据、与理论值吻合的结果。
    *   **红色/橙色**：用于表示警告、错误操作、显著的测量误差、空气阻力开启状态。
    *   **黄色**：用于高亮当前选中的物体、激活的光电门光束等，起到提示作用。
    *   **黑色/深灰色**：用于文字、测量尺刻度、坐标系，确保清晰可读。
*   **整体风格**：扁平化设计结合轻微拟物化（如按钮、面板的轻微阴影），在保证现代感的同时，让交互元素有明确的“可操作性”。

#### 交互功能列表
1.  **实验控制**：
    *   “释放物体”按钮：开始单次下落实验。
    *   “重置”按钮：将物体放回起始位置，清空当前数据。
2.  **环境与参数设置**：
    *   “空气阻力”开关：开启/关闭空气阻力模拟。
    *   “阻力系数”滑块：当开启阻力时，可调整阻力大小。
    *   “下落高度”滑块/输入框：调整释放点的高度（例如1m至10m）。
    *   “物体选择器”：提供2-3种不同物体（如：金属球、塑料球、纸片），其质量、形状（影响阻力）不同。
3.  **测量工具选择**：
    *   “测量工具”切换：可在“光电门”和“打点计时器”两种模拟测量方式间切换，动画呈现相应的测量原理。
4.  **数据显示面板**：
    *   实时显示：下落时间 `t`、瞬时速度 `v`、已下落高度 `h`。
    *   实验结果显示：本次实验测量的 `g` 值 (`g_meas = 2h / t^2`)。
    *   理论/对比显示：当地理论 `g` 值（如9.80 m/s²），并计算并高亮显示本次测量的**百分比误差**。
    *   数据历史：记录最近几次实验的 `g` 测量值，方便对比。
5.  **可视化辅助**：
    *   “显示/隐藏”坐标图：可切换显示实时的 `h-t` 图或 `v-t` 图。
    *   “显示受力分析”开关：开启后，在物体上显示重力（向下）和空气阻力（向上，如果存在）的矢量箭头。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>重力加速度测量实验 - 理想vs真实</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        header {
            text-align: center;
            padding: 20px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            border-left: 6px solid #3498db;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 8px;
            font-size: 2.2rem;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }

        .experiment-area {
            flex: 3;
            min-width: 300px;
            background: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-direction: column;
        }

        .canvas-container {
            flex: 1;
            position: relative;
            background: #f8f9fa;
            border-radius: 8px;
            overflow: hidden;
            border: 2px solid #e9ecef;
            margin-bottom: 15px;
        }

        #experimentCanvas {
            display: block;
            background: white;
        }

        .canvas-overlay {
            position: absolute;
            top: 10px;
            left: 10px;
            background: rgba(255, 255, 255, 0.9);
            padding: 8px 12px;
            border-radius: 6px;
            font-size: 0.9rem;
            border-left: 4px solid #3498db;
        }

        .control-panel {
            flex: 2;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .panel {
            background: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .panel h2 {
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #ecf0f1;
            font-size: 1.4rem;
        }

        .control-group {
            margin-bottom: 15px;
        }

        .control-group label {
            display: block;
            margin-bottom: 6px;
            color: #34495e;
            font-weight: 500;
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .slider-container input[type="range"] {
            flex: 1;
            height: 6px;
            border-radius: 3px;
            background: #ecf0f1;
            outline: none;
            -webkit-appearance: none;
        }

        .slider-container input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }

        .slider-value {
            min-width: 40px;
            text-align: right;
            font-weight: 600;
            color: #2c3e50;
        }

        .button-group {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        button {
            padding: 10px 16px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            font-size: 0.95rem;
        }

        .btn-primary {
            background: #3498db;
            color: white;
            flex: 2;
        }

        .btn-primary:hover {
            background: #2980b9;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(52, 152, 219, 0.3);
        }

        .btn-secondary {
            background: #ecf0f1;
            color: #34495e;
            flex: 1;
        }

        .btn-secondary:hover {
            background: #d5dbdb;
            transform: translateY(-2px);
        }

        .btn-success {
            background: #27ae60;
            color: white;
        }

        .btn-success:hover {
            background: #219653;
        }

        .btn-warning {
            background: #f39c12;
            color: white;
        }

        .btn-warning:hover {
            background: #e67e22;
        }

        .toggle-switch {
            display: flex;
            align-items: center;
            gap: 10px;
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
            background-color: #ccc;
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
            background-color: #27ae60;
        }

        input:checked + .slider:before {
            transform: translateX(26px);
        }

        .object-selector {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        .object-option {
            flex: 1;
            padding: 10px;
            text-align: center;
            border: 2px solid #ecf0f1;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .object-option:hover {
            border-color: #3498db;
            background: #f8f9fa;
        }

        .object-option.selected {
            border-color: #3498db;
            background: #e3f2fd;
            font-weight: 600;
        }

        .data-display {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 10px;
        }

        .data-item {
            background: #f8f9fa;
            padding: 12px;
            border-radius: 8px;
            text-align: center;
            border-left: 4px solid #3498db;
        }

        .data-label {
            font-size: 0.85rem;
            color: #7f8c8d;
            margin-bottom: 5px;
        }

        .data-value {
            font-size: 1.4rem;
            font-weight: 700;
            color: #2c3e50;
        }

        .data-unit {
            font-size: 0.9rem;
            color: #7f8c8d;
            margin-left: 2px;
        }

        .error-display {
            margin-top: 15px;
            padding: 12px;
            border-radius: 8px;
            text-align: center;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .error-low {
            background: #d5f4e6;
            color: #27ae60;
            border-left: 4px solid #27ae60;
        }

        .error-high {
            background: #fde8e8;
            color: #e74c3c;
            border-left: 4px solid #e74c3c;
        }

        .history-panel {
            margin-top: 20px;
        }

        .history-list {
            max-height: 150px;
            overflow-y: auto;
            margin-top: 10px;
        }

        .history-item {
            display: flex;
            justify-content: space-between;
            padding: 8px 12px;
            border-bottom: 1px solid #ecf0f1;
            font-size: 0.9rem;
        }

        .history-item:nth-child(odd) {
            background: #f8f9fa;
        }

        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
            font-size: 0.85rem;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .legend-color {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }

        .legend-ideal {
            background: #27ae60;
        }

        .legend-real {
            background: #e74c3c;
        }

        footer {
            text-align: center;
            padding: 15px;
            color: #7f8c8d;
            font-size: 0.9rem;
            margin-top: 20px;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .data-display {
                grid-template-columns: repeat(2, 1fr);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>重力加速度测量实验</h1>
            <p class="subtitle">对比理想无阻力环境与真实有阻力环境的测量差异</p>
        </header>

        <div class="main-content">
            <div class="experiment-area">
                <div class="canvas-container">
                    <canvas id="experimentCanvas" width="800" height="500"></canvas>
                    <div class="canvas-overlay">
                        实验高度: <span id="currentHeightDisplay">2.00 m</span> | 
                        当前模式: <span id="currentModeDisplay">理想无阻力</span>
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color legend-ideal"></div>
                        <span>理想轨迹 (无阻力)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color legend-real"></div>
                        <span>真实轨迹 (有阻力)</span>
                    </div>
                </div>
            </div>

            <div class="control-panel">
                <div class="panel">
                    <h2>实验控制</h2>
                    
                    <div class="control-group">
                        <label>下落高度: <span id="heightValue">2.00</span> m</label>
                        <div class="slider-container">
                            <input type="range" id="heightSlider" min="1" max="10" step="0.1" value="2">
                            <span class="slider-value">10.0 m</span>
                        </div>
                    </div>

                    <div class="control-group">
                        <label>实验物体</label>
                        <div class="object-selector">
                            <div class="object-option selected" data-object="metal">
                                <div>金属球</div>
                                <small>质量大，阻力小</small>
                            </div>
                            <div class="object-option" data-object="plastic">
                                <div>塑料球</div>
                                <small>质量中，阻力中</small>
                            </div>
                            <div class="object-option" data-object="paper">
                                <div>纸片</div>
                                <small>质量小，阻力大</small>
                            </div>
                        </div>
                    </div>

                    <div class="control-group">
                        <div class="toggle-switch">
                            <span>空气阻力模拟:</span>
                            <label class="switch">
                                <input type="checkbox" id="resistanceToggle">
                                <span class="slider"></span>
                            </label>
                            <span id="resistanceStatus">关闭</span>
                        </div>
                    </div>

                    <div class="control-group" id="resistanceControl" style="display: none;">
                        <label>阻力系数: <span id="resistanceValue">0.5</span></label>
                        <div class="slider-container">
                            <input type="range" id="resistanceSlider" min="0.1" max="2" step="0.1" value="0.5">
                            <span class="slider-value">2.0</span>
                        </div>
                    </div>

                    <div class="button-group">
                        <button id="startBtn" class="btn-primary">开始实验</button>
                        <button id="resetBtn" class="btn-secondary">重置</button>
                    </div>

                    <div class="button-group">
                        <button id="idealModeBtn" class="btn-success">理想模式</button>
                        <button id="realModeBtn" class="btn-warning">真实模式</button>
                    </div>
                </div>

                <div class="panel">
                    <h2>测量数据</h2>
                    
                    <div class="data-display">
                        <div class="data-item">
                            <div class="data-label">下落高度</div>
                            <div class="data-value" id="heightData">2.00<span class="data-unit">m</span></div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">下落时间</div>
                            <div class="data-value" id="timeData">0.00<span class="data-unit">s</span></div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">未速度</div>
                            <div class="data-value" id="velocityData">0.00<span class="data-unit">m/s</span></div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">测量g值</div>
                            <div class="data-value" id="gMeasuredData">0.00<span class="data-unit">m/s²</span></div>
                        </div>
                    </div>

                    <div class="data-item" style="margin-top: 15px;">
                        <div class="data-label">理论g值 (参考)</div>
                        <div class="data-value" id="gTheoreticalData">9.80<span class="data-unit">m/s²</span></div>
                    </div>

                    <div id="errorDisplay" class="error-display" style="display: none;">
                        误差: <span id="errorValue">0.00</span>%
                    </div>
                </div>

                <div class="panel history-panel">
                    <h2>实验记录</h2>
                    <div class="history-list" id="historyList">
                        <!-- 历史记录将通过JS动态添加 -->
                    </div>
                </div>
            </div>
        </div>

        <footer>
            <p>教学动画说明：本实验模拟了重力加速度的测量。在"理想模式"下，物体在真空中自由落体，测量结果精确；在"真实模式"下，空气阻力会导致测量值偏小。</p>
            <p>计算公式: g = 2h / t² | 误差 = |(测量值 - 9.80)/9.80| × 100%</p>
        </footer>
    </div>

    <script>
        // 全局变量
        const canvas = document.getElementById('experimentCanvas');
        const ctx = canvas.getContext('2d');
        
        // 实验状态
        let experimentState = {
            isRunning: false,
            isResistanceOn: false,
            height: 2.0, // 米
            resistanceCoefficient: 0.5,
            selectedObject: 'metal',
            mode: 'ideal', // 'ideal' 或 'real'
            startTime: 0,
            currentTime: 0,
            position: 0,
            velocity: 0,
            measuredG: 0,
            history: []
        };

        // 物体属性
        const objects = {
            metal: { mass: 1.0, radius: 15, color: '#3498db', dragCoefficient: 0.1 },
            plastic: { mass: 0.3, radius: 15, color: '#9b59b6', dragCoefficient: 0.3 },
            paper: { mass: 0.05, radius: 12, color: '#e74c3c', dragCoefficient: 1.2 }
        };

        // 物理常量
        const gTheoretical = 9.80; // m/s²
        const airDensity = 1.2; // kg/m³
        const scale = 50; // 像素/米

        // DOM元素
        const heightSlider = document.getElementById('heightSlider');
        const heightValue = document.getElementById('heightValue');
        const resistanceToggle = document.getElementById('resistanceToggle');
        const resistanceStatus = document.getElementById('resistanceStatus');
        const resistanceControl = document.getElementById('resistanceControl');
        const resistanceSlider = document.getElementById('resistanceSlider');
        const resistanceValue = document.getElementById('resistanceValue');
        const startBtn = document.getElementById('startBtn');
        const resetBtn = document.getElementById('resetBtn');
        const idealModeBtn = document.getElementById('idealModeBtn');
        const realModeBtn = document.getElementById('realModeBtn');
        const objectOptions = document.querySelectorAll('.object-option');
        
        // 数据显示元素
        const heightData = document.getElementById('heightData');
        const timeData = document.getElementById('timeData');
        const velocityData = document.getElementById('velocityData');
        const gMeasuredData = document.getElementById('gMeasuredData');
        const gTheoreticalData = document.getElementById('gTheoreticalData');
        const errorDisplay = document.getElementById('errorDisplay');
        const errorValue = document.getElementById('errorValue');
        const historyList = document.getElementById('historyList');
        const currentHeightDisplay = document.getElementById('currentHeightDisplay');
        const currentModeDisplay = document.getElementById('currentModeDisplay');

        // 初始化
        function init() {
            updateSliders();
            setupEventListeners();
            drawExperiment();
            updateDisplay();
        }

        // 更新滑块显示
        function updateSliders() {
            heightValue.textContent = experimentState.height.toFixed(2);
            resistanceValue.textContent = experimentState.resistanceCoefficient.toFixed(1);
            
            // 更新滑块最大值显示
            document.querySelector('#heightSlider + .slider-value').textContent = 
                heightSlider.max + ' m';
            document.querySelector('#resistanceSlider + .slider-value').textContent = 
                resistanceSlider.max;
            
            currentHeightDisplay.textContent = experimentState.height.toFixed(2) + ' m';
            currentModeDisplay.textContent = experimentState.mode === 'ideal' ? '理想无阻力' : '真实有阻力';
        }

        // 设置事件监听器
        function setupEventListeners() {
            // 高度滑块
            heightSlider.addEventListener('input', function() {
                experimentState.height = parseFloat(this.value);
                updateSliders();
                if (!experimentState.isRunning) {
                    drawExperiment();
                }
            });

            // 阻力开关
            resistanceToggle.addEventListener('change', function() {
                experimentState.isResistanceOn = this.checked;
                resistanceStatus.textContent = this.checked ? '开启' : '关闭';
                resistanceControl.style.display = this.checked ? 'block' : 'none';
                
                if (experimentState.isResistanceOn) {
                    experimentState.mode = 'real';
                    updateModeButtons();
                }
            });

            // 阻力系数滑块
            resistanceSlider.addEventListener('input', function() {
                experimentState.resistanceCoefficient = parseFloat(this.value);
                updateSliders();
            });

            // 物体选择
            objectOptions.forEach(option => {
                option.addEventListener('click', function() {
                    objectOptions.forEach(opt => opt.classList.remove('selected'));
                    this.classList.add('selected');
                    experimentState.selectedObject = this.dataset.object;
                    if (!experimentState.isRunning) {
                        drawExperiment();
                    }
                });
            });

            // 开始实验按钮
            startBtn.addEventListener('click', startExperiment);

            // 重置按钮
            resetBtn.addEventListener('click', resetExperiment);

            // 模式按钮
            idealModeBtn.addEventListener('click', () => setMode('ideal'));
            realModeBtn.addEventListener('click', () => setMode('real'));
        }

        // 设置实验模式
        function setMode(mode) {
            experimentState.mode = mode;
            if (mode === 'ideal') {
                experimentState.isResistanceOn = false;
                resistanceToggle.checked = false;
                resistanceStatus.textContent = '关闭';
                resistanceControl.style.display = 'none';
            } else {
                experimentState.isResistanceOn = true;
                resistanceToggle.checked = true;
                resistanceStatus.textContent = '开启';
                resistanceControl.style.display = 'block';
            }
            updateModeButtons();
            updateSliders();
            if (!experimentState.isRunning) {
                drawExperiment();
            }
        }

        // 更新模式按钮状态
        function updateModeButtons() {
            if (experimentState.mode === 'ideal') {
                idealModeBtn.classList.add('btn-success');
                idealModeBtn.classList.remove('btn-secondary');
                realModeBtn.classList.add('btn-secondary');
                realModeBtn.classList.remove('btn-warning');
            } else {
                realModeBtn.classList.add('btn-warning');
                realModeBtn.classList.remove('btn-secondary');
                idealModeBtn.classList.add('btn-secondary');
                idealModeBtn.classList.remove('btn-success');
            }
        }

        // 开始实验
        function startExperiment() {
            if (experimentState.isRunning) return;
            
            experimentState.isRunning = true;
            experimentState.startTime = Date.now();
            experimentState.position = 0;
            experimentState.velocity = 0;
            experimentState.measuredG = 0;
            
            startBtn.disabled = true;
            startBtn.textContent = '实验中...';
            
            // 开始动画循环
            requestAnimationFrame(animateExperiment);
        }

        // 重置实验
        function resetExperiment() {
            experimentState.isRunning = false;
            experimentState.position = 0;
            experimentState.velocity = 0;
            experimentState.measuredG = 0;
            
            startBtn.disabled = false;
            startBtn.textContent = '开始实验';
            
            updateDisplay();
            drawExperiment();
        }

        // 动画循环
        function animateExperiment() {
            if (!experimentState.isRunning) return;
            
            const currentTime = Date.now();
            const elapsedTime = (currentTime - experimentState.startTime) / 1000; // 转换为秒
            
            // 计算物理
            calculatePhysics(elapsedTime);
            
            // 更新显示
            updateDisplay();
            
            // 绘制
            drawExperiment();
            
            // 检查是否到达底部
            if (experimentState.position >= experimentState.height) {
                finishExperiment();
            } else {
                requestAnimationFrame(animateExperiment);
            }
        }

        // 计算物理
        function calculatePhysics(elapsedTime) {
            experimentState.currentTime = elapsedTime;
            experimentState.position = calculatePosition(elapsedTime);
            experimentState.velocity = calculateVelocity(elapsedTime);
            
            // 计算测量到的g值
            if (elapsedTime > 0) {
                experimentState.measuredG = (2 * experimentState.position) / (elapsedTime * elapsedTime);
            }
        }

        // 计算位置
        function calculatePosition(t) {
            const obj = objects[experimentState.selectedObject];
            const h = experimentState.height;
            
            if (experimentState.isResistanceOn && experimentState.mode === 'real') {
                // 有阻力情况 - 简化模型
                const k = experimentState.resistanceCoefficient * obj.dragCoefficient / obj.mass;
                const terminalVelocity = Math.sqrt(gTheoretical / k);
                
                if (k > 0) {
                    return (gTheoretical / k) * Math.log(Math.cosh(Math.sqrt(k * gTheoretical) * t));
                }
            }
            
            // 无阻力情况
            return 0.5 * gTheoretical * t * t;
        }

        // 计算速度
        function calculateVelocity(t) {
            const obj = objects[experimentState.selectedObject];
            
            if (experimentState.isResistanceOn && experimentState.mode === 'real') {
                // 有阻力情况
                const k = experimentState.resistanceCoefficient * obj.dragCoefficient / obj.mass;
                const terminalVelocity = Math.sqrt(gTheoretical / k);
                
                if (k > 0) {
                    return terminalVelocity * Math.tanh(Math.sqrt(k * gTheoretical) * t);
                }
            }
            
            // 无阻力情况
            return gTheoretical * t;
        }

        // 完成实验
        function finishExperiment() {
            experimentState.isRunning = false;
            experimentState.position = experimentState.height;
            
            // 计算最终g值
            const finalTime = experimentState.currentTime;
            experimentState.measuredG = (2 * experimentState.height) / (finalTime * finalTime);
            
            // 添加到历史记录
            addToHistory();
            
            startBtn.disabled = false;
            startBtn.textContent = '开始实验';
            
            updateDisplay();
            drawExperiment();
        }

        // 添加到历史记录
        function addToHistory() {
            const error = Math.abs((experimentState.measuredG - gTheoretical) / gTheoretical) * 100;
            const historyItem = {
                mode: experimentState.mode,
                object: experimentState.selectedObject,
                height: experimentState.height,
                time: experimentState.currentTime,
                g: experimentState.measuredG,
                error: error,
                timestamp: new Date().toLocaleTimeString()
            };
            
            experimentState.history.unshift(historyItem);
            if (experimentState.history.length > 5) {
                experimentState.history.pop();
            }
            
            updateHistoryDisplay();
        }

        // 更新历史记录显示
        function updateHistoryDisplay() {
            historyList.innerHTML = '';
            
            experimentState.history.forEach(item => {
                const div = document.createElement('div');
                div.className = 'history-item';
                
                const modeText = item.mode === 'ideal' ? '理想' : '真实';
                const objectText = item.object === 'metal' ? '金属球' : 
                                 item.object === 'plastic' ? '塑料球' : '纸片';
                
                div.innerHTML = `
                    <div>
                        <strong>${modeText}</strong> | ${objectText}
                    </div>
                    <div>
                        g=${item.g.toFixed(2)} (${item.error.toFixed(1)}%)
                    </div>
                `;
                
                historyList.appendChild(div);
            });
        }

        // 更新数据显示
        function updateDisplay() {
            // 更新数据
            heightData.innerHTML = experimentState.height.toFixed(2) + '<span class="data-unit">m</span>';
            timeData.innerHTML = experimentState.currentTime.toFixed(2) + '<span class="data-unit">s</span>';
            velocityData.innerHTML = experimentState.velocity.toFixed(2) + '<span class="data-unit">m/s</span>';
            gMeasuredData.innerHTML = experimentState.measuredG.toFixed(2) + '<span class="data-unit">m/s²</span>';
            gTheoreticalData.innerHTML = gTheoretical.toFixed(2) + '<span class="data-unit">m/s²</span>';
            
            // 更新误差显示
            if (experimentState.currentTime > 0) {
                const error = Math.abs((experimentState.measuredG - gTheoretical) / gTheoretical) * 100;
                errorValue.textContent = error.toFixed(2);
                
                errorDisplay.style.display = 'block';
                if (error < 5) {
                    errorDisplay.className = 'error-display error-low';
                } else {
                    errorDisplay.className = 'error-display error-high';
                }
            } else {
                errorDisplay.style.display = 'none';
            }
        }

        // 绘制实验场景
        function drawExperiment() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 绘制测量尺
            drawRuler();
            
            // 绘制理想轨迹
            if (experimentState.mode === 'real' || !experimentState.isRunning) {
                drawIdealTrajectory();
            }
            
            // 绘制真实轨迹
            if (experimentState.isRunning && experimentState.mode === 'real') {
                drawRealTrajectory();
            }
            
            // 绘制物体
            drawObject();
            
            // 绘制光电门
            drawPhotogates();
            
            // 绘制受力分析
            if (experimentState.isRunning) {
                drawForceAnalysis();
            }
        }

        // 绘制背景
        function drawBackground() {
            // 实验室背景
            ctx.fillStyle = '#f8f9fa';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 地面
            ctx.fillStyle = '#95a5a6';
            ctx.fillRect(0, canvas.height - 20, canvas.width, 20);
            
            // 网格线
            ctx.strokeStyle = '#ecf0f1';
            ctx.lineWidth = 0.5;
            
            for (let x = 0; x < canvas.width; x += 50) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, canvas.height - 20);
                ctx.stroke();
            }
            
            for (let y = 0; y < canvas.height - 20; y += 50) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(canvas.width, y);
                ctx.stroke();
            }
        }

        // 绘制测量尺
        function drawRuler() {
            const maxHeight = 10; // 米
            const rulerX = 50;
            
            // 尺子主体
            ctx.fillStyle = '#34495e';
            ctx.fillRect(rulerX - 5, 0, 10, canvas.height - 20);
            
            // 刻度
            ctx.fillStyle = '#ecf0f1';
            ctx.font = '12px Arial';
            ctx.textAlign = 'right';
            
            for (let h = 0; h <= maxHeight; h += 1) {
                const y = canvas.height - 20 - h * scale;
                
                // 主刻度
                ctx.beginPath();
                ctx.moveTo(rulerX - 10, y);
                ctx.lineTo(rulerX + 10, y);
                ctx.strokeStyle = '#ecf0f1';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 刻度标签
                ctx.fillText(h + 'm', rulerX - 15, y + 4);
                
                // 小刻度
                for (let i = 1; i < 10; i++) {
                    const smallY = y - i * scale / 10;
                    if (smallY > 0) {
                        ctx.beginPath();
                        ctx.moveTo(rulerX - 5, smallY);
                        ctx.lineTo(rulerX + 5, smallY);
                        ctx.strokeStyle = '#bdc3c7';
                        ctx.lineWidth = 1;
                        ctx.stroke();
                    }
                }
            }
            
            // 当前高度标记
            const currentY = canvas.height - 20 - experimentState.height * scale;
            ctx.beginPath();
            ctx.moveTo(rulerX + 15, currentY);
            ctx.lineTo(canvas.width - 50, currentY);
            ctx.strokeStyle = '#3498db';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 高度标签
            ctx.fillStyle = '#3498db';
            ctx.font = '14px Arial';
            ctx.textAlign = 'left';
            ctx.fillText(`释放点: ${experimentState.height.toFixed(2)}m`, rulerX + 20, currentY - 5);
        }

        // 绘制理想轨迹
        function drawIdealTrajectory() {
            const steps = 50;
            const obj = objects[experimentState.selectedObject];
            const startX = 150;
            
            ctx.beginPath();
            ctx.strokeStyle = '#27ae60';
            ctx.lineWidth = 2;
            ctx.setLineDash([5, 3]);
            
            for (let i = 0; i <= steps; i++) {
                const t = i * Math.sqrt(2 * experimentState.height / gTheoretical) / steps;
                const y = 0.5 * gTheoretical * t * t;
                const x = startX;
                const canvasY = canvas.height - 20 - y * scale;
                
                if (i === 0) {
                    ctx.moveTo(x, canvasY);
                } else {
                    ctx.lineTo(x, canvasY);
                }
            }
            
            ctx.stroke();
            ctx.setLineDash([]);
        }

        // 绘制真实轨迹
        function drawRealTrajectory() {
            if (!experimentState.isRunning) return;
            
            const steps = Math.min(100, Math.floor(experimentState.currentTime * 100));
            const obj = objects[experimentState.selectedObject];
            const startX = 150;
            
            ctx.beginPath();
            ctx.strokeStyle = '#e74c3c';
            ctx.lineWidth = 2;
            
            for (let i = 0; i <= steps; i++) {
                const t = i * experimentState.currentTime / steps;
                const y = calculatePosition(t);
                const x = startX;
                const canvasY = canvas.height - 20 - y * scale;
                
                if (i === 0) {
                    ctx.moveTo(x, canvasY);
                } else {
                    ctx.lineTo(x, canvasY);
                }
            }
            
            ctx.stroke();
            
            // 绘制阻力效果
            if (experimentState.isResistanceOn) {
                const currentX = startX;
                const currentY = canvas.height - 20 - experimentState.position * scale;
                
                // 阻力粒子效果
                for (let i = 0; i < 5; i++) {
                    const angle = Math.random() * Math.PI * 2;
                    const radius = Math.random() * 5 + 2;
                    const offsetX = Math.cos(angle) * radius;
                    const offsetY = Math.sin(angle) * radius;
                    
                    ctx.beginPath();
                    ctx.arc(currentX + offsetX, currentY + offsetY, 1, 0, Math.PI * 2);
                    ctx.fillStyle = 'rgba(231, 76, 60, 0.3)';
                    ctx.fill();
                }
            }
        }

        // 绘制物体
        function drawObject() {
            const obj = objects[experimentState.selectedObject];
            const x = 150;
            const y = experimentState.isRunning ? 
                canvas.height - 20 - experimentState.position * scale : 
                canvas.height - 20 - experimentState.height * scale;
            
            // 绘制球体
            ctx.beginPath();
            ctx.arc(x, y, obj.radius, 0, Math.PI *
<!--检测到代码截断，自动续写中...-->
2);
            ctx.fillStyle = obj.color;
            ctx.fill();
            
            // 球体高光
            ctx.beginPath();
            ctx.arc(x - obj.radius/3, y - obj.radius/3, obj.radius/4, 0, Math.PI * 2);
            ctx.fillStyle = 'rgba(255, 255, 255, 0.6)';
            ctx.fill();
            
            // 物体标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(
                experimentState.selectedObject === 'metal' ? '金属球' :
                experimentState.selectedObject === 'plastic' ? '塑料球' : '纸片',
                x, y + obj.radius + 15
            );
            
            // 如果正在运行，显示速度
            if (experimentState.isRunning) {
                ctx.fillStyle = '#3498db';
                ctx.font = 'bold 14px Arial';
                ctx.fillText(`v = ${experimentState.velocity.toFixed(2)} m/s`, x, y - obj.radius - 10);
            }
        }

        // 绘制光电门
        function drawPhotogates() {
            const startX = 140;
            const endX = 160;
            
            // 顶部光电门（释放点）
            const topY = canvas.height - 20 - experimentState.height * scale;
            drawPhotogate(startX, topY, endX, topY, '释放传感器');
            
            // 底部光电门（落地检测）
            const bottomY = canvas.height - 20;
            drawPhotogate(startX, bottomY, endX, bottomY, '落地传感器');
            
            // 如果正在运行，绘制光束
            if (experimentState.isRunning) {
                const currentY = canvas.height - 20 - experimentState.position * scale;
                
                // 光束效果
                if (currentY > topY && currentY < bottomY) {
                    ctx.beginPath();
                    ctx.moveTo(startX, currentY);
                    ctx.lineTo(endX, currentY);
                    ctx.strokeStyle = 'rgba(52, 152, 219, 0.3)';
                    ctx.lineWidth = 20;
                    ctx.stroke();
                }
            }
        }

        // 绘制单个光电门
        function drawPhotogate(x1, y, x2, y, label) {
            // 光电门支架
            ctx.beginPath();
            ctx.moveTo(x1, y);
            ctx.lineTo(x1, y - 30);
            ctx.moveTo(x2, y);
            ctx.lineTo(x2, y - 30);
            ctx.strokeStyle = '#7f8c8d';
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 光电门横梁
            ctx.beginPath();
            ctx.moveTo(x1, y - 30);
            ctx.lineTo(x2, y - 30);
            ctx.strokeStyle = '#34495e';
            ctx.lineWidth = 4;
            ctx.stroke();
            
            // 光电门标签
            ctx.fillStyle = '#7f8c8d';
            ctx.font = '11px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(label, (x1 + x2) / 2, y - 35);
        }

        // 绘制受力分析
        function drawForceAnalysis() {
            const obj = objects[experimentState.selectedObject];
            const x = 150;
            const y = canvas.height - 20 - experimentState.position * scale;
            
            // 重力箭头
            drawArrow(x, y, x, y + 60, '#2c3e50', '重力');
            
            // 如果有阻力，绘制阻力箭头
            if (experimentState.isResistanceOn && experimentState.mode === 'real') {
                const resistanceForce = experimentState.resistanceCoefficient * obj.dragCoefficient * 
                                      experimentState.velocity * experimentState.velocity;
                const arrowLength = Math.min(60, 20 + resistanceForce * 10);
                
                drawArrow(x, y, x, y - arrowLength, '#e74c3c', '空气阻力');
            }
        }

        // 绘制箭头
        function drawArrow(fromX, fromY, toX, toY, color, label) {
            const headlen = 10;
            const angle = Math.atan2(toY - fromY, toX - fromX);
            
            // 绘制箭头线
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.strokeStyle = color;
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(
                toX - headlen * Math.cos(angle - Math.PI / 6),
                toY - headlen * Math.sin(angle - Math.PI / 6)
            );
            ctx.lineTo(
                toX - headlen * Math.cos(angle + Math.PI / 6),
                toY - headlen * Math.sin(angle + Math.PI / 6)
            );
            ctx.closePath();
            ctx.fillStyle = color;
            ctx.fill();
            
            // 绘制标签
            ctx.fillStyle = color;
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            
            const midX = (fromX + toX) / 2;
            const midY = (fromY + toY) / 2;
            
            // 根据箭头方向调整标签位置
            if (Math.abs(toX - fromX) < Math.abs(toY - fromY)) {
                // 垂直箭头
                ctx.fillText(label, midX + 30, midY);
            } else {
                // 水平箭头
                ctx.fillText(label, midX, midY - 15);
            }
        }

        // 初始化
        init();
        updateModeButtons();
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 交互式教学动画使用指南

欢迎使用“重力加速度测量实验”交互式教学动画！本动画旨在通过直观、互动的方式，帮助您深入理解重力加速度的测量原理，并探究真实实验与理想模型之间的差异。

---

### 一、 功能说明

本动画模拟了一个虚拟的物理实验室，您可以在此进行自由落体实验，测量重力加速度 `g`。动画的核心价值在于**对比**：您可以轻松地在“理想无阻力环境”和“模拟真实有阻力环境”之间切换，直观地观察空气阻力如何影响物体的下落运动、测量时间以及最终计算出的 `g` 值。

### 二、 主要功能

1.  **实验控制区**
    *   **开始/重置实验**：点击“开始实验”按钮释放物体，动画将模拟其下落过程。实验结束后或过程中，可点击“重置”按钮将一切恢复初始状态。
    *   **模式切换**：
        *   **理想模式**：模拟物体在真空中自由落体，无任何空气阻力，运动遵循 `h = 1/2 * g * t²` 的完美规律。
        *   **真实模式**：开启空气阻力模拟，物体下落会受到与速度相关的阻力，运动轨迹和测量结果将偏离理想值。
    *   **参数调节**：
        *   **下落高度**：通过滑块调节释放点的高度（1米至10米），观察不同高度对下落时间和测量精度的影响。
        *   **实验物体**：选择金属球、塑料球或纸片。不同物体的质量和形状（影响阻力系数）将导致显著不同的下落表现。
        *   **空气阻力**：开关控制是否启用阻力模拟。开启后，可进一步通过“阻力系数”滑块调节阻力大小。

2.  **可视化实验区**
    *   **实时动画**：画布上实时显示物体的下落过程、测量尺和光电门。
    *   **轨迹对比**：
        *   **绿色虚线**：显示当前高度下，物体在理想模式（无阻力）中应遵循的轨迹。
        *   **红色实线**：在真实模式（有阻力）下，物体实际下落的轨迹会实时绘制，与绿色轨迹形成鲜明对比。
    *   **受力分析**：实验过程中，物体上会显示代表**重力（向下）**和**空气阻力（向上）**的箭头，直观展示力的平衡与变化。

3.  **数据与记录区**
    *   **实时数据**：动态显示下落高度、已用时间、瞬时速度和根据当前数据计算出的 **`g` 测量值**。
    *   **误差分析**：将测量出的 `g` 值与理论值（9.80 m/s²）对比，并计算百分比误差。误差大小会通过颜色提示（绿色表示误差小，红色表示误差大）。
    *   **实验历史**：自动记录最近5次实验的关键数据（模式、物体、测量g值、误差），方便进行横向对比和规律总结。

### 三、 设计特色

*   **双轨对比可视化**：并排展示理想与现实轨迹，是理解“模型”与“实际”差异最有力的视觉工具。
*   **探究式学习环境**：您不是被动观看，而是主动的“实验者”。通过控制变量（高度、物体、阻力），自主发现物理规律。
*   **即时反馈与引导**：所有操作都有即时的视觉和数据反馈。画布上的提示信息和数据面板的颜色编码，能有效引导您的注意力。
*   **符合认知规律的界面**：界面布局清晰，左侧为“实验现象”，右侧为“控制与数据”，符合“观察-操作-分析”的科学探究流程。
*   **专业而友好的视觉设计**：采用科技蓝与实验室白的配色，营造严谨而清新的学习氛围，关键元素突出，交互反馈明确。

### 四、 教学要点

本动画可用于演示和探究以下核心物理概念：

1.  **自由落体运动公式**：`h = 1/2 * g * t²`。在理想模式下，您可以验证此公式的准确性。
2.  **重力加速度 `g` 的测量方法**：理解如何通过测量高度 `h` 和时间 `t` 来间接求得 `g`（`g = 2h / t²`）。
3.  **空气阻力的影响**：
    *   阻力导致物体下落**变慢**，测得的时间 `t` **变长**，从而使计算出的 `g` 测量值**偏小**。
    *   阻力影响与物体**形状**和**速度**有关。纸片比金属球受影响大得多。
4.  **误差分析**：区分**系统误差**（如空气阻力导致的固有偏差）和**偶然误差**。理解为何真实实验难以测得完美的9.80 m/s²。
5.  **控制变量法**：学习如何设计实验，例如：保持高度和物体不变，只改变“有无阻力”，来单一地研究阻力的影响。

### 五、 使用建议

**对于学生：**
1.  **初次探索**：先使用“理想模式”，选择金属球，从2米高度释放。观察完美的匀加速运动，记录数据，验证公式。
2.  **引入阻力**：切换到“真实模式”，使用相同设置再次实验。对比两次的轨迹、下落时间和 `g` 值，直观感受阻力的效果。
3.  **深入探究**：
    *   **探究阻力与物体的关系**：在真实模式下，固定高度，依次释放金属球、塑料球和纸片。观察谁的轨迹偏离理想线最多？谁的 `g` 值误差最大？
    *   **探究阻力与高度的关系**：选择纸片，分别在1米和5米高度释放。思考：为什么高度增加后，测量误差可能会变化？
    *   **挑战任务**：尝试通过调节“阻力系数”，让塑料球在真实模式下测得的 `g` 值接近9.80。这模拟了什么现实情况？（答：在阻力很小的环境中实验，或对阻力进行修正）

**对于教师：**
1.  **课堂演示**：可作为引入新课或讲解误差时的动态演示工具，比静态图片或公式更具说服力。
2.  **设计探究任务**：为学生布置上述“深入探究”中的任务，让他们在动画中完成实验报告，培养科学探究能力。
3.  **概念辨析**：利用“受力分析”箭头，讲解下落过程中重力与阻力的关系，以及“加速度减小”与“速度增加”并不矛盾的概念。

希望这个交互式动画能成为您探索物理世界的有力助手！请尽情实验、观察、思考，享受科学发现的乐趣。