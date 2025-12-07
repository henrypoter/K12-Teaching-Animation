# 需求：抛体运动的分运动合成

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中或大学低年级的物理学习者。用户的核心需求是**直观理解抛体运动可以分解为水平匀速直线运动和竖直方向匀加速（自由落体）运动**。他们可能存在的认知难点包括：
1.  **抽象性**：难以在脑海中同时构建合运动与两个分运动的动态图像。
2.  **独立性**：不理解两个分运动在时间和空间上如何相互独立、互不影响。
3.  **矢量合成**：对位移、速度的矢量合成（平行四边形法则）在动态过程中的应用感到困惑。
因此，动画的核心任务是**将抽象的矢量分解与合成过程可视化、动态化、可交互化**，降低认知负荷，促进概念建构。

#### 教学设计思路
*   **核心概念**：明确传达“抛体运动 = 水平匀速运动 + 竖直匀加速运动”。强调分运动的**独立性**（同时性、互不干扰）和**矢量性**（位移、速度的合成遵循平行四边形法则）。
*   **认知规律**：
    1.  **从整体到局部**：先展示完整的抛体轨迹（抛物线），再引导用户观察其如何由两个简单的直线运动合成。
    2.  **从静态到动态**：允许用户暂停、单步播放动画，在关键帧观察矢量的几何关系。
    3.  **从观察到操控**：提供交互控件，让用户改变初速度、抛射角等参数，即时观察对分运动和合运动的影响，建立因果联系。
*   **交互设计**：
    *   **分层/聚焦控制**：允许用户选择单独显示“合运动”、“水平分运动”、“竖直分运动”或它们的任意组合，避免信息过载。
    *   **轨迹跟踪**：为小球和它的两个“分身影子”（水平投影和竖直投影）留下运动轨迹，清晰对比。
    *   **矢量可视化**：实时绘制并标注合速度、水平分速度、竖直分速度矢量（最好用不同颜色），并动态展示其合成关系。
    *   **参数探索**：提供滑块，允许实时调整初速度大小、抛射角度、重力加速度，并立即重置动画观察效果。
*   **视觉呈现**：
    *   **主场景**：一个简洁的物理空间，包含地面、高度和距离刻度尺。
    *   **焦点突出**：运动的小球（合运动）作为视觉焦点。两个“分身点”（代表纯水平运动和纯竖直运动的虚拟点）用不同颜色和较轻的视觉权重呈现。
    *   **引导与标注**：使用虚线、连线、动态生长的箭头来建立小球与两个分身点之间的位置关联。关键物理量（如位移、速度）随动画进行动态标注。
    *   **信息面板**：固定区域实时显示时间、水平位移、竖直位移、合速度大小等数据。

#### 配色方案选择
选择清晰、对比度高、符合教育场景且有助于区分概念的配色：
*   **主色调/合运动**：`#3498db`（科技蓝）。用于抛体小球、合运动轨迹、合速度矢量。代表核心观察对象。
*   **水平分运动**：`#2ecc71`（活力绿）。用于水平分身点、水平运动轨迹、水平速度矢量。绿色常与“恒定”、“匀速”关联。
*   **竖直分运动**：`#e74c3c`（警示红）。用于竖直分身点、竖直运动轨迹、竖直速度矢量。红色常与“加速”、“变化”关联，且能吸引对重力作用的注意。
*   **辅助元素**：`#95a5a6`（浅灰色）用于背景、坐标轴、刻度、地面。`#2c3e50`（深灰色）用于文字和重要标注。
*   **背景**：纯白色或极浅的灰色 (`#f8f9fa`)，确保清晰度。

#### 交互功能列表
1.  **动画控制**：播放/暂停、重置、单步前进/后退按钮。
2.  **显示/隐藏切换**：多选框，用于独立控制以下元素的显示：
    *   合运动（小球及抛物线轨迹）
    *   水平分运动（水平点及水平直线轨迹）
    *   竖直分运动（竖直点及竖直直线轨迹）
    *   速度矢量箭头（合速度、水平分速度、竖直分速度）
    *   位移辅助线（连接小球与两个分身的虚线）
3.  **参数调节面板**：
    *   滑块：初速度大小 (`v0`)
    *   滑块：抛射角度 (`θ`，范围0°-90°)
    *   滑块：重力加速度 (`g`，可调以演示不同星球环境)
    *   “应用参数并重置”按钮
4.  **实时数据面板**：显示当前时间 `t`、水平位移 `x`、竖直位移 `y`、水平速度 `vx`、竖直速度 `vy`、合速度大小 `v`。
5.  **轨迹留存**：可选是否清除上一次运动的轨迹。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>抛体运动的分运动合成 | 交互式教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #f8f9fa;
            color: #2c3e50;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        header {
            text-align: center;
            padding-bottom: 15px;
            border-bottom: 2px solid #3498db;
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
            gap: 25px;
        }

        .simulation-area {
            flex: 1;
            min-width: 700px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            display: flex;
            flex-direction: column;
        }

        .canvas-container {
            position: relative;
            flex: 1;
            border: 1px solid #ecf0f1;
            border-radius: 8px;
            overflow: hidden;
            background-color: white;
        }

        #motionCanvas {
            display: block;
            width: 100%;
            height: 100%;
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
            font-size: 0.95rem;
        }

        .color-box {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }

        .control-panel {
            flex: 0 0 350px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 25px;
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .panel-section {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        h2 {
            color: #3498db;
            font-size: 1.4rem;
            padding-bottom: 8px;
            border-bottom: 1px solid #ecf0f1;
        }

        h3 {
            color: #2c3e50;
            font-size: 1.1rem;
            margin-bottom: 5px;
        }

        .control-group {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .checkbox-group {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }

        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .checkbox-item input[type="checkbox"] {
            width: 18px;
            height: 18px;
            cursor: pointer;
        }

        .checkbox-item label {
            cursor: pointer;
            user-select: none;
        }

        .slider-container {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .slider-label {
            display: flex;
            justify-content: space-between;
        }

        .slider-label span:last-child {
            font-weight: bold;
            color: #3498db;
        }

        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: #ecf0f1;
            outline: none;
            -webkit-appearance: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        .button-group {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        button {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            background-color: #3498db;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            flex: 1;
            min-width: 120px;
        }

        button:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(52, 152, 219, 0.3);
        }

        button:active {
            transform: translateY(0);
        }

        button#resetBtn {
            background-color: #95a5a6;
        }

        button#resetBtn:hover {
            background-color: #7f8c8d;
        }

        .data-panel {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 20px;
            border-left: 4px solid #3498db;
        }

        .data-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }

        .data-item {
            display: flex;
            flex-direction: column;
        }

        .data-label {
            font-size: 0.9rem;
            color: #7f8c8d;
            margin-bottom: 4px;
        }

        .data-value {
            font-size: 1.4rem;
            font-weight: bold;
            color: #2c3e50;
            font-family: 'Courier New', monospace;
        }

        .unit {
            font-size: 0.9rem;
            color: #95a5a6;
            margin-left: 4px;
        }

        footer {
            text-align: center;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid #ecf0f1;
            color: #7f8c8d;
            font-size: 0.9rem;
        }

        @media (max-width: 1100px) {
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
            <h1>抛体运动的分运动合成</h1>
            <p class="subtitle">探索水平匀速直线运动与竖直匀加速运动的独立性与矢量合成</p>
        </header>

        <div class="main-content">
            <div class="simulation-area">
                <div class="canvas-container">
                    <canvas id="motionCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="color-box" style="background-color: #3498db;"></div>
                        <span>合运动（抛体）</span>
                    </div>
                    <div class="legend-item">
                        <div class="color-box" style="background-color: #2ecc71;"></div>
                        <span>水平分运动（匀速）</span>
                    </div>
                    <div class="legend-item">
                        <div class="color-box" style="background-color: #e74c3c;"></div>
                        <span>竖直分运动（匀加速）</span>
                    </div>
                    <div class="legend-item">
                        <div class="color-box" style="background-color: #f39c12;"></div>
                        <span>速度矢量</span>
                    </div>
                </div>
            </div>

            <div class="control-panel">
                <div class="panel-section">
                    <h2>动画控制</h2>
                    <div class="button-group">
                        <button id="playPauseBtn">播放</button>
                        <button id="stepBtn">单步前进</button>
                        <button id="resetBtn">重置</button>
                    </div>
                    
                    <div class="control-group">
                        <label>
                            <input type="checkbox" id="clearTrails" checked>
                            每次重置时清除轨迹
                        </label>
                    </div>
                </div>

                <div class="panel-section">
                    <h2>显示控制</h2>
                    <div class="checkbox-group">
                        <div class="checkbox-item">
                            <input type="checkbox" id="showResultant" checked>
                            <label for="showResultant">合运动</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showHorizontal" checked>
                            <label for="showHorizontal">水平分运动</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showVertical" checked>
                            <label for="showVertical">竖直分运动</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showVectors" checked>
                            <label for="showVectors">速度矢量</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showGrid" checked>
                            <label for="showGrid">坐标网格</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showTrails" checked>
                            <label for="showTrails">运动轨迹</label>
                        </div>
                    </div>
                </div>

                <div class="panel-section">
                    <h2>参数设置</h2>
                    <div class="control-group">
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>初速度 v₀</span>
                                <span id="v0Value">20 m/s</span>
                            </div>
                            <input type="range" id="v0Slider" min="5" max="40" step="1" value="20">
                        </div>
                        
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>抛射角 θ</span>
                                <span id="angleValue">45°</span>
                            </div>
                            <input type="range" id="angleSlider" min="0" max="90" step="1" value="45">
                        </div>
                        
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>重力加速度 g</span>
                                <span id="gValue">9.8 m/s²</span>
                            </div>
                            <input type="range" id="gSlider" min="1" max="20" step="0.1" value="9.8">
                        </div>
                        
                        <button id="applyParamsBtn">应用参数并重置</button>
                    </div>
                </div>

                <div class="panel-section">
                    <h2>实时数据</h2>
                    <div class="data-panel">
                        <div class="data-grid">
                            <div class="data-item">
                                <div class="data-label">时间 t</div>
                                <div class="data-value"><span id="timeValue">0.00</span><span class="unit">s</span></div>
                            </div>
                            <div class="data-item">
                                <div class="data-label">水平位移 x</div>
                                <div class="data-value"><span id="xValue">0.00</span><span class="unit">m</span></div>
                            </div>
                            <div class="data-item">
                                <div class="data-label">竖直位移 y</div>
                                <div class="data-value"><span id="yValue">0.00</span><span class="unit">m</span></div>
                            </div>
                            <div class="data-item">
                                <div class="data-label">合位移 s</div>
                                <div class="data-value"><span id="sValue">0.00</span><span class="unit">m</span></div>
                            </div>
                            <div class="data-item">
                                <div class="data-label">水平速度 vₓ</div>
                                <div class="data-value"><span id="vxValue">14.14</span><span class="unit">m/s</span></div>
                            </div>
                            <div class="data-item">
                                <div class="data-label">竖直速度 vᵧ</div>
                                <div class="data-value"><span id="vyValue">14.14</span><span class="unit">m/s</span></div>
                            </div>
                            <div class="data-item">
                                <div class="data-label">合速度 v</div>
                                <div class="data-value"><span id="vValue">20.00</span><span class="unit">m/s</span></div>
                            </div>
                            <div class="data-item">
                                <div class="data-label">最大高度</div>
                                <div class="data-value"><span id="maxHeight">10.20</span><span class="unit">m</span></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <footer>
            <p>教学动画设计：抛体运动的分运动合成 | 使用HTML5 Canvas实现 | 适用于物理教学</p>
        </footer>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('motionCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        
        // 初始调整尺寸
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 物理参数
        let params = {
            v0: 20,        // 初速度 (m/s)
            angle: 45,     // 抛射角 (度)
            g: 9.8,        // 重力加速度 (m/s²)
            time: 0,       // 当前时间 (s)
            dt: 0.05,      // 时间步长 (s)
            isPlaying: false,
            maxTime: 0
        };
        
        // 计算最大飞行时间
        function calculateMaxTime() {
            const v0y = params.v0 * Math.sin(params.angle * Math.PI / 180);
            return 2 * v0y / params.g;
        }
        
        // 状态变量
        let animationId = null;
        let trails = [];
        
        // 颜色定义
        const colors = {
            resultant: '#3498db',
            horizontal: '#2ecc71',
            vertical: '#e74c3c',
            vector: '#f39c12',
            grid: 'rgba(149, 165, 166, 0.2)',
            text: '#2c3e50',
            ground: '#95a5a6'
        };
        
        // 显示控制
        const display = {
            resultant: true,
            horizontal: true,
            vertical: true,
            vectors: true,
            grid: true,
            trails: true,
            clearOnReset: true
        };
        
        // 获取DOM元素
        const playPauseBtn = document.getElementById('playPauseBtn');
        const stepBtn = document.getElementById('stepBtn');
        const resetBtn = document.getElementById('resetBtn');
        const applyParamsBtn = document.getElementById('applyParamsBtn');
        
        // 显示控制复选框
        const showResultant = document.getElementById('showResultant');
        const showHorizontal = document.getElementById('showHorizontal');
        const showVertical = document.getElementById('showVertical');
        const showVectors = document.getElementById('showVectors');
        const showGrid = document.getElementById('showGrid');
        const showTrails = document.getElementById('showTrails');
        const clearTrails = document.getElementById('clearTrails');
        
        // 参数滑块
        const v0Slider = document.getElementById('v0Slider');
        const angleSlider = document.getElementById('angleSlider');
        const gSlider = document.getElementById('gSlider');
        
        // 参数显示
        const v0Value = document.getElementById('v0Value');
        const angleValue = document.getElementById('angleValue');
        const gValue = document.getElementById('gValue');
        
        // 数据面板
        const timeValue = document.getElementById('timeValue');
        const xValue = document.getElementById('xValue');
        const yValue = document.getElementById('yValue');
        const sValue = document.getElementById('sValue');
        const vxValue = document.getElementById('vxValue');
        const vyValue = document.getElementById('vyValue');
        const vValue = document.getElementById('vValue');
        const maxHeight = document.getElementById('maxHeight');
        
        // 初始化显示控制
        showResultant.checked = display.resultant;
        showHorizontal.checked = display.horizontal;
        showVertical.checked = display.vertical;
        showVectors.checked = display.vectors;
        showGrid.checked = display.grid;
        showTrails.checked = display.trails;
        clearTrails.checked = display.clearOnReset;
        
        // 更新参数显示
        function updateParamDisplays() {
            v0Value.textContent = `${params.v0} m/s`;
            angleValue.textContent = `${params.angle}°`;
            gValue.textContent = `${params.g} m/s²`;
            
            // 计算并显示最大高度
            const v0y = params.v0 * Math.sin(params.angle * Math.PI / 180);
            const hMax = (v0y * v0y) / (2 * params.g);
            maxHeight.textContent = hMax.toFixed(2);
        }
        
        // 计算当前位置和速度
        function calculateMotion(t) {
            const angleRad = params.angle * Math.PI / 180;
            const v0x = params.v0 * Math.cos(angleRad);
            const v0y = params.v0 * Math.sin(angleRad);
            
            const x = v0x * t;
            const y = v0y * t - 0.5 * params.g * t * t;
            
            const vx = v0x;
            const vy = v0y - params.g * t;
            const v = Math.sqrt(vx * vx + vy * vy);
            
            return { x, y, vx, vy, v };
        }
        
        // 坐标转换：物理坐标到Canvas坐标
        function toCanvasCoords(x, y) {
            const scale = 15; // 像素/米
            const groundY = canvas.height * 0.8;
            
            const canvasX = canvas.width * 0.1 + x * scale;
            const canvasY = groundY - y * scale;
            
            return { x: canvasX, y: canvasY };
        }
        
        // 绘制坐标网格
        function drawGrid() {
            if (!display.grid) return;
            
            ctx.strokeStyle = colors.grid;
            ctx.lineWidth = 1;
            
            const groundY = canvas.height * 0.8;
            const scale = 15;
            
            // 水平网格线
            for (let y = 0; y <= groundY; y += scale) {
                const physicalY = (groundY - y) / scale;
                if (physicalY >= 0) {
                    ctx.beginPath();
                    ctx.moveTo(canvas.width * 0.1, y);
                    ctx.lineTo(canvas.width * 0.9, y);
                    ctx.stroke();
                    
                    // 标注
                    ctx.fillStyle = colors.text;
                    ctx.font = '12px Arial';
                    ctx.fillText(physicalY.toFixed(1), canvas.width * 0.05, y + 4);
                }
            }
            
            // 垂直网格线
            for (let x = canvas.width * 0.1; x <= canvas.width * 0.9; x += scale) {
                const physicalX = (x - canvas.width * 0.1) / scale;
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, groundY);
                ctx.stroke();
                
                // 标注
                ctx.fillStyle = colors.text;
                ctx.font = '12px Arial';
                ctx.fillText(physicalX.toFixed(1), x - 10, groundY + 15);
            }
            
            // 坐标轴
            ctx.strokeStyle = colors.text;
            ctx.lineWidth = 2;
            
            // X轴（地面）
            ctx.beginPath();
            ctx.moveTo(canvas.width * 0.1, groundY);
            ctx.lineTo(canvas.width * 0.9, groundY);
            ctx.stroke();
            
            // Y轴
            ctx.beginPath();
            ctx.moveTo(canvas.width * 0.1, 0);
            ctx.lineTo(canvas.width * 0.1, groundY);
            ctx.stroke();
            
            // 坐标轴标签
            ctx.fillStyle = colors.text;
            ctx.font = '14px Arial';
            ctx.fillText('x (m)', canvas.width * 0.9 - 30, groundY + 25);
            ctx.fillText('y (m)', canvas.width * 0.05, 20);
        }
        
        // 绘制运动轨迹
        function drawTrails() {
            if (!display.trails || trails.length < 2) return;
            
            // 绘制合运动轨迹
            if (display.resultant) {
                ctx.strokeStyle = colors.resultant + '80';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(trails[0].resultant.x, trails[0].resultant.y);
                for (let i = 1; i < trails.length; i++) {
                    ctx.lineTo(trails[i].resultant.x, trails[i].resultant.y);
                }
                ctx.stroke();
            }
            
            // 绘制水平分运动轨迹
            if (display.horizontal) {
                ctx.strokeStyle = colors.horizontal + '60';
                ctx.lineWidth = 1.5;
                ctx.setLineDash([5, 5]);
                ctx.beginPath();
                ctx.moveTo(trails[0].horizontal.x, trails[0].horizontal.y);
                for (let i = 1; i < trails.length; i++) {
                    ctx.lineTo(trails[i].horizontal.x, trails[i].horizontal.y);
                }
                ctx.stroke();
                ctx.setLineDash([]);
            }
            
            // 绘制竖直分运动轨迹
            if (display.vertical) {
                ctx.strokeStyle = colors.vertical + '60';
                ctx.lineWidth = 1.5;
                ctx.setLineDash([5, 5]);
                ctx.beginPath();
                ctx.moveTo(trails[0].vertical.x, trails[0].vertical.y);
                for (let i = 1; i < trails.length; i++) {
                    ctx.lineTo(trails[i].vertical.x, trails[i].vertical.y);
                }
                ctx.stroke();
                ctx.setLineDash([]);
            }
        }
        
        // 绘制速度矢量
        function drawVelocityVectors(resultantPos, vx, vy) {
            if (!display.vectors) return;
            
            const scale = 0.5; // 矢量缩放因子
            const groundY = canvas.height * 0.8;
            
            // 水平速度矢量
            if (display.horizontal) {
                ctx.strokeStyle = colors.horizontal;
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(resultantPos.x, resultantPos.y);
                ctx.lineTo(resultantPos.x + vx * scale, resultantPos.y);
                ctx.stroke();
                
                // 箭头
                drawArrowhead(resultantPos.x + vx * scale, resultantPos.y, Math.atan2(0, vx), colors.horizontal);
            }
            
            // 竖直速度矢量
            if (display.vertical) {
                ctx.strokeStyle = colors.vertical;
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(resultantPos.x, resultantPos.y);
                ctx.lineTo(resultantPos.x, resultantPos.y - vy * scale);
                ctx.stroke();
                
                // 箭头
                drawArrowhead(resultantPos.x, resultantPos.y - vy * scale, Math.atan2(-vy, 0), colors.vertical);
            }
            
            // 合速度矢量
            if (display.resultant) {
                const v = Math.sqrt(vx * vx + vy * vy);
                const angle = Math.atan2(-vy, vx);
                
                ctx.strokeStyle = colors.vector;
                ctx.lineWidth = 3;
                ctx.beginPath();
                ctx.moveTo(resultantPos.x, resultantPos.y);
                ctx.lineTo(resultantPos.x + vx * scale, resultantPos.y - vy * scale);
                ctx.stroke();
                
                // 箭头
                drawArrowhead(resultantPos.x + vx * scale, resultantPos.y - vy * scale, angle, colors.vector);
                
                // 绘制平行四边形
                ctx.strokeStyle = colors.vector + '40';
                ctx.lineWidth = 1;
                ctx.setLineDash([3, 3]);
                ctx.beginPath();
                ctx.moveTo(resultantPos.x + vx * scale, resultantPos.y);
                ctx.lineTo(resultantPos.x + vx * scale, resultantPos.y - vy * scale);
                ctx.moveTo(resultantPos.x, resultantPos.y - vy * scale);
                ctx.lineTo(resultantPos.x + vx * scale, resultantPos.y - vy * scale);
                ctx.stroke();
                ctx.setLineDash([]);
            }
        }
        
        // 绘制箭头
        function drawArrowhead(x, y, angle, color) {
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(angle);
            ctx.fillStyle = color;
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(-8, -4);
            ctx.lineTo(-8, 4);
            ctx.closePath();
            ctx.fill();
            ctx.restore();
        }
        
        // 绘制连接线
        function drawConnectionLines(resultantPos, horizontalPos, verticalPos) {
            ctx.strokeStyle = 'rgba(149, 165, 166, 0.5)';
            ctx.lineWidth = 1;
            ctx.setLineDash([3, 3]);
            
            // 连接到水平分运动点
            if (display.horizontal) {
                ctx.beginPath();
                ctx.moveTo(resultantPos.x, resultantPos.y);
                ctx.lineTo(horizontalPos.x, horizontalPos.y);
                ctx.stroke();
            }
            
            // 连接到竖直分运动点
            if (display.vertical) {
                ctx.beginPath();
                ctx.moveTo(resultantPos.x, resultantPos.y);
                ctx.lineTo(verticalPos.x, verticalPos.y);
                ctx.stroke();
            }
            
            ctx.setLineDash([]);
        }
        
        // 绘制所有物体
        function drawScene() {
            // 清空Canvas
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制网格
            drawGrid();
            
            // 绘制轨迹
            drawTrails();
            
            // 计算当前位置
            const motion = calculateMotion(params.time);
            const resultantPos = toCanvasCoords(motion.x, motion.y);
            const horizontalPos = toCanvasCoords(motion.x, 0);
            const verticalPos = toCanvasCoords(0, motion.y);
            
            // 绘制连接线
            drawConnectionLines(resultantPos, horizontalPos, verticalPos);
            
            // 绘制分运动点
            if (display.horizontal) {
                ctx.fillStyle = colors.horizontal;
                ctx.beginPath();
                ctx.arc(horizontalPos.x, horizontalPos.y, 6, 0, Math.PI * 2);
                ctx.fill();
                ctx.strokeStyle = 'white';
                ctx.lineWidth = 2;
                ctx.stroke();
            }
            
            if (display.vertical) {
                ctx.fillStyle = colors.vertical;
                ctx.beginPath();
                ctx.arc(verticalPos.x, verticalPos.y, 6, 0, Math.PI * 2);
                ctx.fill();
                ctx.strokeStyle = 'white';
                ctx.lineWidth = 2;
                ctx.stroke();
            }
            
            // 绘制合运动点
            if (display.resultant) {
                ctx.fillStyle = colors.resultant;
                ctx.beginPath();
                ctx.arc(resultantPos.x, resultantPos.y, 10, 0, Math.PI * 2);
                ctx.fill();
                ctx.strokeStyle = 'white';
                ctx.lineWidth = 3;
                ctx.stroke();
            }
            
            // 绘制速度矢量
            drawVelocityVectors(resultantPos, motion.vx, motion.vy);
            
            // 更新数据面板
            updateDataPanel(motion);
        }
        
        // 更新数据面板
        function updateDataPanel(motion) {
            timeValue.textContent = params.time.toFixed(2);
            xValue.textContent = motion.x.toFixed(2);
            yValue.textContent = motion.y.toFixed(2);
            sValue.textContent = Math.sqrt(motion.x * motion.x + motion.y * motion.y).toFixed(2);
            vxValue.textContent = motion.vx.toFixed(2);
            vyValue.textContent = motion.vy.toFixed(2);
            vValue.textContent = motion.v.toFixed(2);
        }
        
        // 动画循环
        function animate() {
            if (!params.isPlaying) return;
            
            // 更新时间
            params.time += params.dt;
            
            // 检查是否落地
            if (params.time > params.maxTime || calculateMotion(params.time).y < 0) {
                params.isPlaying = false;
                playPauseBtn.textContent = '播放';
                params.time = Math.min(params.time, params.maxTime);
            }
            
            // 记录轨迹点
            const motion = calculateMotion(params.time);
            const resultantPos = toCanvasCoords(motion.x, motion.y);
            const horizontalPos = toCanvasCoords(motion.x, 0);
            const verticalPos = toCanvasCoords(0, motion.y);
            
            trails.push({
                resultant: resultantPos,
                horizontal: horizontalPos,
                vertical: verticalPos
            });
            
            // 绘制场景
            drawScene();
            
            // 继续动画
            if (params.isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }
        
        // 重置动画
        function resetAnimation() {
            params.time = 0;
            params.maxTime = calculateMaxTime();
            
            if (display.clearOnReset) {
                trails = [];
            }
            
            // 记录初始位置
            const motion = calculateMotion(0);
            const resultantPos = toCanvasCoords(motion.x, motion.y);
            const horizontalPos = toCanvasCoords(motion.x, 0);
            const verticalPos = toCanvasCoords(0, motion.y);
            
            trails = [{
                resultant: resultantPos,
                horizontal: horizontalPos,
                vertical: verticalPos
            }];
            
            drawScene();
            updateParamDisplays();
        }
        
        // 单步前进
        function stepForward() {
            if (params.time < params.maxTime) {
                params.time += params.dt;
                
                const motion = calculateMotion(params.time);
                const resultantPos = toCanvasCoords(motion.x, motion.y);
                const horizontalPos = toCanvasCoords(motion.x, 0);
                const verticalPos = toCanvasCoords(0, motion.y);
                
                trails.push({
                    resultant: resultantPos,
                    horizontal: horizontalPos,
                    vertical: verticalPos
                });
                
                drawScene();
            }
        }
        
        // 事件监听器
        playPauseBtn.addEventListener('click', () => {
            params.isPlaying = !params.isPlaying;
            playPauseBtn.textContent = params.isPlaying ? '暂停' : '播放';
            
            if (params.isPlaying) {
                // 如果已经落地，重置
                if (params.time >= params.maxTime || calculateMotion(params.time).y < 0) {
                    resetAnimation();
                }
                animationId = requestAnimationFrame(animate);
            } else if (animationId) {
                cancelAnimationFrame(animationId);
            }
        });
        
        stepBtn.addEventListener('click', stepForward);
        
        resetBtn.addEventListener('click', resetAnimation);
        
        applyParamsBtn.addEventListener('click', () => {
            params.v0 = parseFloat(v0Slider.value);
            params.angle = parseFloat(angleSlider.value);
            params.g = parseFloat(gSlider.value);
            updateParamDisplays();
            resetAnimation();
        });
        
        // 显示控制事件
        showResultant.addEventListener('change', (e) => {
            display.resultant = e.target.checked;
            drawScene();
        });
        
        showHorizontal.addEventListener('change', (e) => {
            display.horizontal = e.target.checked;
            drawScene();
        });
        
        showVertical.addEventListener('change', (e) => {
            display.vertical = e.target.checked;
            drawScene();
        });
        
        showVectors.addEventListener('change', (e) => {
            display.vectors = e.target.checked;
            drawScene();
        });
        
        showGrid.addEventListener('change', (e) => {
            display.grid = e.target.checked;
            drawScene();
        });
        
        showTrails.addEventListener('change', (e) => {
            display.trails = e.target.checked;
            drawScene();
        });
        
        clearTrails.addEventListener('change', (e) => {
            display.clearOnReset = e.target.checked;
        });
        
        // 滑块事件
        v0Slider.addEventListener('input', (e) => {
            v0Value.textContent = `${e.target.value} m/s`;
        });
        
        angleSlider.addEventListener('input', (e) => {
            angleValue.textContent = `${e.target.value}°`;
        });
        
        gSlider.addEventListener('input', (e) => {
            gValue.textContent = `${e.target.value} m/s²`;
        });
        
        // 初始化
        updateParamDisplays();
        resetAnimation();
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 抛体运动分运动合成交互式教学动画使用指南

欢迎使用“抛体运动的分运动合成”交互式教学动画！本工具旨在通过可视化、可交互的方式，帮助您深入理解抛体运动的本质——即抛体运动可以分解为水平方向的匀速直线运动和竖直方向的匀加速（自由落体）运动。让我们一起来探索这个精彩的物理世界吧！

---

### 一、功能说明

本动画提供了一个完整的抛体运动模拟环境，包含：

1. **主模拟区**：可视化展示抛体运动的完整过程
2. **控制面板**：提供动画控制、显示设置和参数调节功能
3. **实时数据面板**：显示运动过程中的关键物理量
4. **图例说明**：清晰标识不同颜色代表的运动类型

### 二、主要功能

#### 1. 动画控制区
- **播放/暂停**：开始或暂停动画模拟
- **单步前进**：逐帧观察运动细节，适合精细分析
- **重置**：回到初始状态，重新开始模拟
- **轨迹清除**：可选择是否在重置时保留之前的运动轨迹

#### 2. 显示控制区
您可以自由组合显示以下元素：
- ✅ **合运动**：蓝色小球及其抛物线轨迹
- ✅ **水平分运动**：绿色点及其水平直线轨迹（匀速）
- ✅ **竖直分运动**：红色点及其竖直直线轨迹（匀加速）
- ✅ **速度矢量**：橙色箭头显示速度的合成与分解
- ✅ **坐标网格**：辅助观察位置关系的参考网格
- ✅ **运动轨迹**：显示各运动的完整路径

#### 3. 参数设置区
通过滑块实时调节物理参数：
- **初速度 v₀**：5-40 m/s（控制抛体的初始动能）
- **抛射角 θ**：0°-90°（改变运动轨迹的形状）
- **重力加速度 g**：1-20 m/s²（模拟不同星球环境）
- **应用参数**：确认修改并重置动画

#### 4. 实时数据区
动态显示以下物理量：
- 时间 t、水平位移 x、竖直位移 y、合位移 s
- 水平速度 vₓ、竖直速度 vᵧ、合速度 v
- 理论最大高度

### 三、设计特色

#### 1. 分层可视化设计
- **颜色编码系统**：蓝=合运动，绿=水平运动，红=竖直运动，橙=速度矢量
- **轨迹对比**：同时显示三种运动的轨迹，直观对比差异
- **矢量动态合成**：实时展示速度矢量的平行四边形法则

#### 2. 认知友好的交互
- **渐进式显示**：可从简单到复杂逐步显示各元素
- **单步模式**：适合教师讲解和学生自主探索
- **即时反馈**：所有参数调整立即反映在动画中

#### 3. 教学导向的功能
- **物理量实时计算**：理论与实践相结合
- **参数影响可视化**：直观展示各参数对运动的影响
- **错误状态预防**：自动检测落地条件，防止不合理显示

### 四、教学要点

#### 核心概念强化
1. **运动的独立性原理**
   - 观察水平运动不受竖直运动影响
   - 验证竖直运动不受水平运动影响
   - 理解“同时性”概念

2. **矢量合成与分解**
   - 观察位移的合成（小球位置由两个分运动共同决定）
   - 分析速度的合成（合速度始终沿轨迹切线方向）
   - 理解加速度的独立性（只有竖直方向有加速度）

3. **参数影响分析**
   - **初速度 v₀**：影响射程和最大高度
   - **抛射角 θ**：
     - θ=0°：水平抛射
     - θ=45°：最大射程（无空气阻力时）
     - θ=90°：竖直上抛
   - **重力加速度 g**：影响运动时间和轨迹曲率

#### 推荐探究活动
1. **基础观察**：先只显示合运动，观察抛物线轨迹；再逐步加入分运动
2. **对比实验**：固定v₀，改变θ，观察轨迹变化；固定θ，改变v₀，观察影响
3. **矢量分析**：在最高点、落地点等关键位置暂停，分析速度矢量的特点
4. **极限情况**：设置θ=0°或90°，验证特殊情况下的运动规律
5. **星球探索**：改变g值，模拟月球（g≈1.6）或木星（g≈24.8）上的抛体运动

### 五、使用建议

#### 课堂教学场景
1. **引入阶段**：只显示合运动，提出问题“这个曲线运动能否分解？”
2. **探究阶段**：逐步显示分运动，引导学生发现分解规律
3. **验证阶段**：使用单步模式，在关键位置分析物理量关系
4. **拓展阶段**：让学生自主调节参数，总结规律

#### 自主学习场景
1. **循序渐进**：按照“合运动→分运动→速度矢量”的顺序逐步探索
2. **记录对比**：调整参数时，记录数据变化，总结规律
3. **提出问题**：例如“为什么45°时射程最大？”“竖直速度何时为零？”
4. **联系实际**：思考生活中的抛体运动实例（投篮、掷铅球等）

#### 技术提示
1. **响应式设计**：工具适应不同屏幕尺寸，但在较大屏幕上体验更佳
2. **性能优化**：如果轨迹显示卡顿，可关闭“运动轨迹”选项
3. **数据解读**：关注数据面板的变化，将可视化与量化分析结合
4. **教学节奏**：单步模式适合精细讲解，连续播放适合整体观察

---

### 教学理念说明

本工具基于建构主义学习理论设计，强调：
- **主动探索**：学生通过交互操作建构知识
- **多重表征**：同一概念通过图形、数据、动画多种方式呈现
- **即时反馈**：操作结果立即可视化，强化学习效果
- **认知支架**：从具体到抽象，从简单到复杂的渐进式学习路径

我们希望这个工具能够成为您理解抛体运动的得力助手，让抽象的物理概念变得生动具体。祝您探索愉快，收获满满！

**提示**：本工具完全在浏览器中运行，无需安装任何插件。建议使用Chrome、Firefox或Edge等现代浏览器以获得最佳体验。