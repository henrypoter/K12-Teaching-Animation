# 需求：抛体运动分解（水平+竖直方向独立，轨迹+分速度矢量）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中物理或大学物理入门阶段的学生。他们已具备基本的运动学知识（如匀速、匀变速运动），但对运动的合成与分解，特别是抛体运动的独立性原理，理解上存在困难。
2.  **核心痛点**：
    *   **抽象性**：学生难以在脑海中同时构建水平匀速运动和竖直匀加速运动的合成图像，以及分速度矢量随时间变化的动态过程。
    *   **分离与合成**：对“两个方向的运动互不影响”这一独立性原理缺乏直观感受。
    *   **矢量性**：对速度的矢量合成（平行四边形法则）在动态过程中的应用理解不深。
3.  **学习目标**：通过本动画，学生应能：
    *   直观理解抛体运动可以分解为独立的水平匀速直线运动和竖直匀变速直线运动。
    *   观察并描述合运动的轨迹（抛物线）是如何由两个分运动“合成”的。
    *   动态观察并理解合速度的大小和方向如何由两个分速度矢量合成得到，并注意其变化规律。
    *   通过交互，验证不同初速度或抛射角对运动轨迹和特征的影响。

#### 教学设计思路
1.  **核心概念**：运动的独立性原理（叠加原理）、运动的合成与分解、速度的矢量合成、抛物线轨迹。
2.  **认知规律（支架式教学）**：
    *   **呈现整体**：首先展示一个完整的斜抛或平抛运动，让学生对“抛体运动”有一个整体印象（轨迹、速度方向变化）。
    *   **分解剖析**：将整体运动分解为水平（x方向）和竖直（y方向）两个分运动，用独立的运动图示（如匀速运动的点、匀加速运动的点）同步展示，并与合运动点进行位置连线，清晰展示“合成”关系。
    *   **聚焦矢量**：在运动点上绘制实时变化的**分速度矢量**（`v_x` 水平恒定，`v_y` 竖直变化）和**合速度矢量**（`v`，作为对角线），动态演示矢量合成平行四边形。这是理解速度方向变化的关键。
    *   **交互验证**：允许用户调整参数（如水平初速度 `v0x`、竖直初速度 `v0y` 或总初速度大小与角度），观察其对分运动、合轨迹及速度矢量的即时影响，从“观察者”变为“探索者”，深化理解。
3.  **交互设计**：
    *   **引导式界面**：界面分区明确，包含“动画演示区”、“参数控制区”和“图示说明区”。
    *   **可控节奏**：提供“播放/暂停”、“步进”、“重置”按钮，允许学生控制动画节奏，在关键帧进行观察和思考。
    *   **选择性显示**：提供复选框，允许用户选择显示/隐藏“轨迹”、“分运动点”、“速度矢量”、“网格/坐标系”等元素，避免信息过载，支持分层探究。
    *   **参数实时联动**：调整任何参数，动画和所有矢量、轨迹即时更新，提供即时反馈。
4.  **视觉呈现**：
    *   **空间分层**：使用不同颜色、线型（实线、虚线、点线）和图层透明度来区分合运动、水平分运动、竖直分运动以及它们的速度矢量。
    *   **动态焦点**：当前运动的“主角”（小球）视觉上最突出。速度矢量箭头应平滑动态变化，其长度可比例代表速度大小。
    *   **关键信息标注**：在运动过程中，实时显示关键数据（如当前 `x, y` 坐标， `v_x, v_y, v` 的大小和方向角）。

#### 配色方案选择
*   **主色调（合运动）**：采用**深蓝色 (#2E5A88)** 或**紫色 (#6A5ACD)** 表示合运动的小球和轨迹，体现“综合”与“主体”感。
*   **分运动色**：
    *   **水平分运动**：**橙色 (#FF8C00)** 或**绿色 (#4CAF50)**。橙色常与“恒定”关联，绿色清晰易辨。
    *   **竖直分运动**：**红色 (#F44336)** 或**青色 (#00BCD4)**。红色能强烈提示“加速”和“变化”，青色与橙色形成良好对比。
*   **速度矢量色**：与对应的分运动颜色一致。**合速度矢量**使用与合运动相同的主色调，或使用**黑色 (#333333)** 以强调其合成结果。
*   **背景与界面**：**浅灰色 (#f5f5f5)** 或**极浅蓝 (#eef2f5)** 背景，搭配**深灰色 (#424242)** 的坐标轴、网格线和文字，确保高可读性和专业感。
*   **交互元素**：控制按钮使用中性色（如 #607D8B），滑块和输入框有轻微视觉反馈（如悬停变色）。

#### 交互功能列表
1.  **动画控制**：
    *   播放 / 暂停
    *   步进（前进一帧）
    *   重置（回到初始状态）
    *   速度调节滑块（控制动画播放快慢）
2.  **显示控制（复选框）**：
    *   ✅ 显示/隐藏 合运动轨迹
    *   ✅ 显示/隐藏 水平分运动点与路径
    *   ✅ 显示/隐藏 竖直分运动点与路径
    *   ✅ 显示/隐藏 速度矢量 (`v_x`, `v_y`, `v`)
    *   ✅ 显示/隐藏 坐标网格
    *   ✅ 显示/隐藏 实时数据标签
3.  **参数调节（输入框或滑块）**：
    *   **模式选择**：平抛 / 斜抛
    *   初始总速度大小 `v0` (m/s)
    *   抛射角 `θ` (度) （斜抛模式下）
    *   重力加速度 `g` (m/s²) （可选，用于拓展）
    *   初始高度 `y0` (m) （可选）
4.  **动态可视化**：
    *   三个运动点（合、水平、竖直）的同步运动。
    *   从水平分运动点和竖直分运动点指向合运动点的连线（虚线），直观展示位置合成。
    *   动态绘制并更新的速度矢量箭头（`v_x` 水平，`v_y` 竖直，`v` 为对角线）。
    *   运动点经过的轨迹路径（可选实时绘制）。
    *   实时更新的坐标与速度数据显示。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>抛体运动分解教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #424242;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            overflow: hidden;
        }
        
        header {
            background: linear-gradient(135deg, #2E5A88 0%, #4A7BB5 100%);
            color: white;
            padding: 24px 32px;
            border-bottom: 1px solid #e0e0e0;
        }
        
        h1 {
            font-size: 28px;
            margin-bottom: 8px;
        }
        
        .subtitle {
            font-size: 16px;
            opacity: 0.9;
            font-weight: normal;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            padding: 0;
        }
        
        .animation-section {
            flex: 1;
            min-width: 600px;
            padding: 24px;
            border-right: 1px solid #e0e0e0;
        }
        
        .control-section {
            flex: 0 0 400px;
            padding: 24px;
            background-color: #fafafa;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #eef2f5;
            border-radius: 8px;
            overflow: hidden;
            margin-bottom: 20px;
            border: 1px solid #ddd;
        }
        
        #motionCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 16px;
            margin-top: 16px;
            padding: 12px;
            background-color: #f9f9f9;
            border-radius: 6px;
            border-left: 4px solid #2E5A88;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            margin-right: 20px;
        }
        
        .legend-color {
            width: 20px;
            height: 8px;
            margin-right: 8px;
            border-radius: 2px;
        }
        
        .controls-group {
            margin-bottom: 28px;
            padding-bottom: 20px;
            border-bottom: 1px solid #e0e0e0;
        }
        
        h2 {
            font-size: 20px;
            margin-bottom: 16px;
            color: #2E5A88;
            display: flex;
            align-items: center;
        }
        
        h2 i {
            margin-right: 10px;
            font-size: 18px;
        }
        
        .control-row {
            margin-bottom: 16px;
            display: flex;
            align-items: center;
        }
        
        label {
            display: inline-block;
            width: 160px;
            font-weight: 500;
            color: #555;
        }
        
        input[type="range"] {
            flex: 1;
            height: 6px;
            border-radius: 3px;
            background: #ddd;
            outline: none;
            -webkit-appearance: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: #2E5A88;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }
        
        .value-display {
            display: inline-block;
            width: 60px;
            text-align: right;
            font-family: 'Courier New', monospace;
            font-weight: bold;
            color: #2E5A88;
        }
        
        .checkbox-group {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }
        
        .checkbox-item {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
            width: calc(50% - 6px);
        }
        
        .checkbox-item input {
            margin-right: 8px;
            width: 18px;
            height: 18px;
        }
        
        .button-group {
            display: flex;
            gap: 12px;
            margin-top: 10px;
        }
        
        button {
            padding: 12px 20px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            flex: 1;
        }
        
        button i {
            margin-right: 8px;
        }
        
        .btn-play {
            background-color: #4CAF50;
            color: white;
        }
        
        .btn-play:hover {
            background-color: #3d8b40;
        }
        
        .btn-pause {
            background-color: #FF9800;
            color: white;
        }
        
        .btn-pause:hover {
            background-color: #e68900;
        }
        
        .btn-step {
            background-color: #2196F3;
            color: white;
        }
        
        .btn-step:hover {
            background-color: #0b7dda;
        }
        
        .btn-reset {
            background-color: #607D8B;
            color: white;
        }
        
        .btn-reset:hover {
            background-color: #546E7A;
        }
        
        .data-panel {
            background-color: white;
            border-radius: 8px;
            padding: 16px;
            margin-top: 20px;
            border: 1px solid #e0e0e0;
            font-family: 'Courier New', monospace;
        }
        
        .data-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            padding-bottom: 8px;
            border-bottom: 1px dashed #eee;
        }
        
        .data-label {
            color: #666;
        }
        
        .data-value {
            font-weight: bold;
            color: #2E5A88;
        }
        
        .mode-selector {
            display: flex;
            border-radius: 6px;
            overflow: hidden;
            border: 1px solid #ddd;
            margin-bottom: 20px;
        }
        
        .mode-btn {
            flex: 1;
            padding: 12px;
            text-align: center;
            background-color: #f1f1f1;
            cursor: pointer;
            transition: all 0.2s;
            border: none;
            border-radius: 0;
            font-weight: 500;
        }
        
        .mode-btn.active {
            background-color: #2E5A88;
            color: white;
        }
        
        .explanation {
            margin-top: 24px;
            padding: 16px;
            background-color: #f0f7ff;
            border-radius: 8px;
            border-left: 4px solid #2196F3;
            font-size: 14px;
        }
        
        @media (max-width: 1000px) {
            .main-content {
                flex-direction: column;
            }
            
            .animation-section, .control-section {
                min-width: 100%;
                border-right: none;
                border-bottom: 1px solid #e0e0e0;
            }
            
            .canvas-container {
                height: 400px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <div class="container">
        <header>
            <h1><i class="fas fa-project-diagram"></i> 抛体运动分解教学动画</h1>
            <p class="subtitle">水平与竖直方向独立运动 · 轨迹与分速度矢量合成 · 交互式探究</p>
        </header>
        
        <div class="main-content">
            <section class="animation-section">
                <div class="canvas-container">
                    <canvas id="motionCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2E5A88;"></div>
                        <span>合运动（轨迹与小球）</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FF8C00;"></div>
                        <span>水平分运动（匀速）</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #F44336;"></div>
                        <span>竖直分运动（匀加速）</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #333333;"></div>
                        <span>合速度矢量</span>
                    </div>
                </div>
            </section>
            
            <section class="control-section">
                <div class="mode-selector">
                    <button class="mode-btn active" id="modeProjectile">斜抛运动</button>
                    <button class="mode-btn" id="modeHorizontal">平抛运动</button>
                </div>
                
                <div class="controls-group">
                    <h2><i class="fas fa-sliders-h"></i> 运动参数</h2>
                    
                    <div class="control-row">
                        <label for="initialSpeed">初速度 v₀ (m/s):</label>
                        <input type="range" id="initialSpeed" min="5" max="50" value="30" step="1">
                        <span class="value-display" id="initialSpeedValue">30</span>
                    </div>
                    
                    <div class="control-row" id="angleControl">
                        <label for="launchAngle">抛射角 θ (°):</label>
                        <input type="range" id="launchAngle" min="10" max="80" value="45" step="1">
                        <span class="value-display" id="launchAngleValue">45</span>
                    </div>
                    
                    <div class="control-row">
                        <label for="gravity">重力加速度 g (m/s²):</label>
                        <input type="range" id="gravity" min="1" max="20" value="9.8" step="0.1">
                        <span class="value-display" id="gravityValue">9.8</span>
                    </div>
                    
                    <div class="control-row">
                        <label for="animationSpeed">动画速度:</label>
                        <input type="range" id="animationSpeed" min="0.1" max="3" value="1" step="0.1">
                        <span class="value-display" id="animationSpeedValue">1.0</span>
                    </div>
                </div>
                
                <div class="controls-group">
                    <h2><i class="fas fa-eye"></i> 显示控制</h2>
                    <div class="checkbox-group">
                        <div class="checkbox-item">
                            <input type="checkbox" id="showTrajectory" checked>
                            <label for="showTrajectory">合运动轨迹</label>
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
                            <input type="checkbox" id="showData" checked>
                            <label for="showData">实时数据</label>
                        </div>
                    </div>
                </div>
                
                <div class="controls-group">
                    <h2><i class="fas fa-play-circle"></i> 动画控制</h2>
                    <div class="button-group">
                        <button class="btn-play" id="playBtn">
                            <i class="fas fa-play"></i> 播放
                        </button>
                        <button class="btn-pause" id="pauseBtn">
                            <i class="fas fa-pause"></i> 暂停
                        </button>
                        <button class="btn-step" id="stepBtn">
                            <i class="fas fa-step-forward"></i> 步进
                        </button>
                        <button class="btn-reset" id="resetBtn">
                            <i class="fas fa-redo"></i> 重置
                        </button>
                    </div>
                </div>
                
                <div class="data-panel">
                    <h2><i class="fas fa-chart-line"></i> 实时数据</h2>
                    <div class="data-row">
                        <span class="data-label">时间 t (s):</span>
                        <span class="data-value" id="timeValue">0.00</span>
                    </div>
                    <div class="data-row">
                        <span class="data-label">位置 (x, y) (m):</span>
                        <span class="data-value" id="positionValue">0.00, 0.00</span>
                    </div>
                    <div class="data-row">
                        <span class="data-label">水平速度 vₓ (m/s):</span>
                        <span class="data-value" id="vxValue">21.21</span>
                    </div>
                    <div class="data-row">
                        <span class="data-label">竖直速度 vᵧ (m/s):</span>
                        <span class="data-value" id="vyValue">21.21</span>
                    </div>
                    <div class="data-row">
                        <span class="data-label">合速度 v (m/s):</span>
                        <span class="data-value" id="vValue">30.00</span>
                    </div>
                    <div class="data-row">
                        <span class="data-label">速度方向 θ (°):</span>
                        <span class="data-value" id="angleValue">45.00</span>
                    </div>
                </div>
                
                <div class="explanation">
                    <p><strong>教学提示：</strong> 观察抛体运动如何分解为水平方向的匀速直线运动和竖直方向的匀加速直线运动。注意合速度矢量始终沿轨迹切线方向，且由水平分速度（恒定）和竖直分速度（随时间变化）合成得到。</p>
                </div>
            </section>
        </div>
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
            v0: 30,          // 初速度 (m/s)
            angle: 45,       // 抛射角 (度)
            g: 9.8,          // 重力加速度 (m/s²)
            isProjectile: true, // true=斜抛, false=平抛
            time: 0,         // 当前时间 (s)
            maxTime: 10,     // 最大模拟时间 (s)
            dt: 0.02,        // 时间步长 (s)
            animationSpeed: 1.0, // 动画速度因子
            isPlaying: false, // 动画是否正在播放
            scale: 5,        // 像素/米 的比例尺
            originX: 100,    // 坐标系原点X (像素)
            originY: 400     // 坐标系原点Y (像素)
        };
        
        // 显示控制参数
        let display = {
            trajectory: true,
            horizontal: true,
            vertical: true,
            vectors: true,
            grid: true,
            data: true
        };
        
        // 运动状态
        let state = {
            x: 0,
            y: 0,
            vx: 0,
            vy: 0,
            v: 0,
            trajectory: []
        };
        
        // 颜色定义
        const colors = {
            combined: '#2E5A88',     // 合运动 - 深蓝色
            horizontal: '#FF8C00',   // 水平分运动 - 橙色
            vertical: '#F44336',     // 竖直分运动 - 红色
            vector: '#333333',       // 合速度矢量 - 黑色
            grid: '#CCCCCC',         // 网格线 - 浅灰色
            axis: '#424242',         // 坐标轴 - 深灰色
            text: '#424242'          // 文本 - 深灰色
        };
        
        // 初始化运动状态
        function initState() {
            params.time = 0;
            state.trajectory = [];
            
            // 计算初始速度分量
            const angleRad = params.angle * Math.PI / 180;
            
            if (params.isProjectile) {
                // 斜抛运动
                state.vx = params.v0 * Math.cos(angleRad);
                state.vy = params.v0 * Math.sin(angleRad);
            } else {
                // 平抛运动
                state.vx = params.v0;
                state.vy = 0;
            }
            
            state.x = 0;
            state.y = 0;
            state.v = Math.sqrt(state.vx * state.vx + state.vy * state.vy);
            
            // 记录初始位置
            state.trajectory.push({x: state.x, y: state.y});
        }
        
        // 更新运动状态
        function updateState() {
            if (!params.isPlaying) return;
            
            params.time += params.dt * params.animationSpeed;
            
            // 计算新位置
            state.x = state.vx * params.time;
            state.y = state.vy * params.time - 0.5 * params.g * params.time * params.time;
            
            // 计算新速度
            const newVy = state.vy - params.g * params.time;
            state.v = Math.sqrt(state.vx * state.vx + newVy * newVy);
            
            // 如果小球落地，停止动画
            if (state.y < 0) {
                params.isPlaying = false;
                document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
                return;
            }
            
            // 记录轨迹点
            state.trajectory.push({x: state.x, y: state.y});
            
            // 更新数据显示
            updateDataDisplay();
        }
        
        // 绘制坐标系和网格
        function drawGrid() {
            if (!display.grid) return;
            
            ctx.strokeStyle = colors.grid;
            ctx.lineWidth = 0.5;
            ctx.setLineDash([2, 2]);
            
            // 绘制垂直网格线
            for (let x = -20; x <= 100; x += 5) {
                const px = params.originX + x * params.scale;
                ctx.beginPath();
                ctx.moveTo(px, 0);
                ctx.lineTo(px, canvas.height);
                ctx.stroke();
            }
            
            // 绘制水平网格线
            for (let y = -80; y <= 20; y += 5) {
                const py = params.originY - y * params.scale;
                ctx.beginPath();
                ctx.moveTo(0, py);
                ctx.lineTo(canvas.width, py);
                ctx.stroke();
            }
            
            ctx.setLineDash([]);
            
            // 绘制坐标轴
            ctx.strokeStyle = colors.axis;
            ctx.lineWidth = 2;
            
            // X轴
            ctx.beginPath();
            ctx.moveTo(0, params.originY);
            ctx.lineTo(canvas.width, params.originY);
            ctx.stroke();
            
            // Y轴
            ctx.beginPath();
            ctx.moveTo(params.originX, canvas.height);
            ctx.lineTo(params.originX, 0);
            ctx.stroke();
            
            // 坐标轴箭头
            ctx.fillStyle = colors.axis;
            
            // X轴箭头
            ctx.beginPath();
            ctx.moveTo(canvas.width - 10, params.originY - 5);
            ctx.lineTo(canvas.width, params.originY);
            ctx.lineTo(canvas.width - 10, params.originY + 5);
            ctx.fill();
            
            // Y轴箭头
            ctx.beginPath();
            ctx.moveTo(params.originX - 5, 10);
            ctx.lineTo(params.originX, 0);
            ctx.lineTo(params.originX + 5, 10);
            ctx.fill();
            
            // 坐标轴标签
            ctx.fillStyle = colors.text;
            ctx.font = '14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('x (m)', canvas.width - 20, params.originY + 20);
            ctx.textAlign = 'left';
            ctx.fillText('y (m)', params.originX + 10, 20);
            
            // 刻度标签
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            
            // X轴刻度
            for (let x = 0; x <= 80; x += 10) {
                const px = params.originX + x * params.scale;
                ctx.beginPath();
                ctx.moveTo(px, params.originY - 5);
                ctx.lineTo(px, params.originY + 5);
                ctx.stroke();
                ctx.fillText(x.toString(), px, params.originY + 18);
            }
            
            // Y轴刻度
            ctx.textAlign = 'right';
            for (let y = 0; y <= 60; y += 10) {
                const py = params.originY - y * params.scale;
                ctx.beginPath();
                ctx.moveTo(params.originX - 5, py);
                ctx.lineTo(params.originX + 5, py);
                ctx.stroke();
                ctx.fillText(y.toString(), params.originX - 10, py + 4);
            }
        }
        
        // 绘制轨迹
        function drawTrajectory() {
            if (!display.trajectory || state.trajectory.length < 2) return;
            
            ctx.strokeStyle = colors.combined;
            ctx.lineWidth = 2;
            ctx.beginPath();
            
            // 绘制轨迹线
            for (let i = 0; i < state.trajectory.length; i++) {
                const point = state.trajectory[i];
                const px = params.originX + point.x * params.scale;
                const py = params.originY - point.y * params.scale;
                
                if (i === 0) {
                    ctx.moveTo(px, py);
                } else {
                    ctx.lineTo(px, py);
                }
            }
            
            ctx.stroke();
        }
        
        // 绘制分运动
        function drawComponents() {
            const px = params.originX + state.x * params.scale;
            const py = params.originY - state.y * params.scale;
            
            // 绘制水平分运动点
            if (display.horizontal) {
                const hx = params.originX + state.x * params.scale;
                const hy = params.originY;
                
                ctx.fillStyle = colors.horizontal;
                ctx.beginPath();
                ctx.arc(hx, hy, 6, 0, Math.PI * 2);
                ctx.fill();
                
                // 从水平分运动点到合运动点的连线
                ctx.strokeStyle = colors.horizontal;
                ctx.lineWidth = 1;
                ctx.setLineDash([3, 3]);
                ctx.beginPath();
                ctx.moveTo(hx, hy);
                ctx.lineTo(px, py);
                ctx.stroke();
                ctx.setLineDash([]);
            }
            
            // 绘制竖直分运动点
            if (display.vertical) {
                const vx = params.originX;
                const vy = params.originY - state.y * params.scale;
                
                ctx.fillStyle = colors.vertical;
                ctx.beginPath();
                ctx.arc(vx, vy, 6, 0, Math.PI * 2);
                ctx.fill();
                
                // 从竖直分运动点到合运动点的连线
                ctx.strokeStyle = colors.vertical;
                ctx.lineWidth = 1;
                ctx.setLineDash([3, 3]);
                ctx.beginPath();
                ctx.moveTo(vx, vy);
                ctx.lineTo(px, py);
                ctx.stroke();
                ctx.setLineDash([]);
            }
        }
        
        // 绘制速度矢量
        function drawVectors() {
            if (!display.vectors) return;
            
            const px = params.originX + state.x * params.scale;
            const py = params.originY - state.y * params.scale;
            
            // 计算当前竖直速度（考虑重力影响）
            const currentVy = state.vy - params.g * params.time;
            
            // 绘制水平速度矢量
            ctx.strokeStyle = colors.horizontal;
            ctx.fillStyle = colors.horizontal;
            ctx.lineWidth = 2;
            
            const vxScale = 0.5; // 速度矢量缩放因子
            const vxEndX = px + state.vx * vxScale;
            const vxEndY = py;
            
            drawArrow(px, py, vxEndX, vxEndY, 8);
            
            // 绘制竖直速度矢量
            ctx.strokeStyle = colors.vertical;
            ctx.fillStyle = colors.vertical;
            
            const vyEndX = px;
            const vyEndY = py - currentVy * vxScale;
            
            drawArrow(px, py, vyEndX, vyEndY, 8);
            
            // 绘制合速度矢量（平行四边形对角线）
            ctx.strokeStyle = colors.vector;
            ctx.fillStyle = colors.vector;
            ctx.lineWidth = 3;
            
            const vEndX = px + state.vx * vxScale;
            const vEndY = py - currentVy * vxScale;
            
            drawArrow(px, py, vEndX, vEndY, 10);
            
            // 绘制速度矢量平行四边形（虚线）
            ctx.strokeStyle = colors.vector;
            ctx.lineWidth = 1;
            ctx.setLineDash([2, 2]);
            ctx.beginPath();
            ctx.moveTo(vxEndX, vxEndY);
            ctx.lineTo(vEndX, vEndY);
            ctx.lineTo(vyEndX, vyEndY);
            ctx.stroke();
            ctx.setLineDash([]);
        }
        
        // 绘制箭头函数
        function drawArrow(fromX, fromY, toX, toY, headLength) {
            const angle = Math.atan2(toY - fromY, toX - fromX);
            
            // 绘制线
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(
                toX - headLength * Math.cos(angle - Math.PI / 6),
                toY - headLength * Math.sin(angle - Math.PI / 6)
            );
            ctx.lineTo(
                toX - headLength * Math.cos(angle + Math.PI / 6),
                toY - headLength * Math.sin(angle + Math.PI / 6)
            );
            ctx.closePath();
            ctx.fill();
        }
        
        // 绘制合运动小球
        function drawBall() {
            const px = params.originX + state.x * params.scale;
            const py = params.originY - state.y * params.scale;
            
            // 绘制小球
            ctx.fillStyle = colors.combined;
            ctx.beginPath();
            ctx.arc(px, py, 10, 0, Math.PI * 2);
            ctx.fill();
            
            // 小球高光
            ctx.fillStyle = 'rgba(255, 255, 255, 0.6)';
            ctx.beginPath();
            ctx.arc(px - 4, py - 4, 4, 0, Math.PI * 2);
            ctx.fill();
        }
        
        // 更新数据显示
        function updateDataDisplay() {
            if (!display.data) return;
            
            const currentVy = state.vy - params.g * params.time;
            const velocityAngle = Math.atan2(currentVy, state.vx) * 180 / Math.PI;
            
            document.getElementById('timeValue').textContent = params.time.toFixed(2);
            document.getElementById('positionValue').textContent = `${state.x.toFixed(2)}, ${state.y.toFixed(2)}`;
            document.getElementById('vxValue').textContent = state.vx.toFixed(2);
            document.getElementById('vyValue').textContent = currentVy.toFixed(2);
            document.getElementById('vValue').textContent = state.v.toFixed(2);
            document.getElementById('angleValue').textContent = velocityAngle.toFixed(2);
        }
        
        // 主绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制各个组件
            drawGrid();
            drawTrajectory();
            drawComponents();
            drawVectors();
            drawBall();
        }
        
        // 动画循环
        function animate() {
            updateState();
            draw();
            requestAnimationFrame(animate);
        }
        
        // 初始化UI事件监听
        function initUI() {
            // 模式切换
            document.getElementById('modeProjectile').addEventListener('click', function() {
                params.isProjectile = true;
                document.getElementById('modeProjectile').classList.add('active');
                document.getElementById('modeHorizontal').classList.remove('active');
                document.getElementById('angleControl').style.display = 'flex';
                initState();
            });
            
            document.getElementById('modeHorizontal').addEventListener('click', function() {
                params.isProjectile = false;
                document.getElementById('modeHorizontal').classList.add('active');
                document.getElementById('modeProjectile').classList.remove('active');
                document.getElementById('angleControl').style.display = 'none';
                initState();
            });
            
            // 滑块控制
            const sliders = ['initialSpeed', 'launchAngle', 'gravity', 'animationSpeed'];
            sliders.forEach(sliderId => {
                const slider = document.getElementById(sliderId);
                const valueDisplay = document.getElementById(sliderId + 'Value');
                
                slider.addEventListener('input', function() {
                    const value = parseFloat(this.value);
                    valueDisplay.textContent = value.toFixed(sliderId === 'animationSpeed' ? 1 : sliderId === 'gravity' ? 1 : 0);
                    
                    if (sliderId === 'initialSpeed') params.v0 = value;
                    if (sliderId === 'launchAngle') params.angle = value;
                    if (sliderId === 'gravity') params.g = value;
                    if (sliderId === 'animationSpeed') params.animationSpeed = value;
                    
                    initState();
                });
            });
            
            // 显示控制复选框
            const checkboxes = ['showTrajectory', 'showHorizontal', 'showVertical', 'showVectors', 'showGrid', 'showData'];
            checkboxes.forEach(checkboxId => {
                const checkbox = document.getElementById(checkboxId);
                const displayKey = checkboxId.replace('show', '').toLowerCase();
                
                checkbox.addEventListener('change', function() {
                    display[displayKey] = this.checked;
                });
            });
            
            // 动画控制按钮
            document.getElementById('playBtn').addEventListener('click', function() {
                params.isPlaying = !params.isPlaying;
                if (params.isPlaying) {
                    this.innerHTML = '<i class="fas fa-pause"></i> 暂停';
                } else {
                    this.innerHTML = '<i class="fas fa-play"></i> 播放';
                }
            });
            
            document.getElementById('pauseBtn').addEventListener('click', function() {
                params.isPlaying = false;
                document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
            });
            
            document.getElementById('stepBtn').addEventListener('click', function() {
                params.isPlaying = false;
                document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
                params.time += params.dt;
                updateState();
                draw();
            });
            
            document.getElementById('resetBtn').addEventListener('click', function() {
                params.isPlaying = false;
                document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
                initState();
                draw();
                updateDataDisplay();
            });
        }
        
        // 初始化函数
        function init() {
            resizeCanvas();
            initState();
            initUI();
            updateDataDisplay();
            draw();
            animate();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

#### 交互式教学动画使用指南

欢迎使用“抛体运动分解”交互式教学动画！本工具旨在通过直观、动态的可视化方式，帮助您深入理解抛体运动的合成与分解原理。请跟随本指南，开启您的探索之旅。

---

#### 一、 功能说明

本动画将抛体运动（平抛或斜抛）分解为两个独立的运动：
1.  **水平方向**：匀速直线运动。
2.  **竖直方向**：匀加速直线运动（受重力影响）。

动画的核心是**同步展示**这三个运动（一个合运动，两个分运动）以及它们之间的**矢量关系**。您可以通过调整参数和显示选项，从不同角度观察和分析运动规律。

#### 二、 主要功能

1.  **动画控制区**（左上角）
    *   **播放/暂停**：控制动画的进行与暂停。
    *   **步进**：在暂停状态下，点击可让动画前进一个计算帧，便于精细观察每一时刻的运动状态。
    *   **重置**：将动画恢复到初始状态。
    *   **速度滑块**：调节动画播放的快慢（0.5倍至5倍）。

2.  **参数控制区**（左侧面板）
    *   **运动模式**：在“平抛运动”和“斜抛运动”之间切换。
    *   **初速度 `v₀`**：滑块调节抛体初始速度的大小。
    *   **抛射角 `θ`**：滑块调节抛射角度（仅在“斜抛运动”模式下有效）。
    *   **重力加速度 `g`**：滑块调节重力加速度值，可用于模拟不同星球环境（如月球）。

3.  **显示控制区**（右侧面板）
    *   **轨迹**：显示/隐藏合运动的抛物线轨迹。
    *   **分运动点**：显示/隐藏代表水平（橙色）和竖直（青色）分运动的辅助点及其运动路径。
    *   **速度矢量**：显示/隐藏实时变化的**分速度矢量**（`vₓ` 橙色，`vᵧ` 青色）和**合速度矢量**（`v` 紫色）。
    *   **网格**：显示/隐藏背景坐标网格。
    *   **实时数据**：显示/隐藏运动小球旁边的实时坐标和速度信息。

#### 三、 设计特色

1.  **多图层可视化**：采用不同颜色清晰区分合运动（紫色）、水平分运动（橙色）和竖直分运动（青色），避免视觉混淆。
2.  **动态矢量合成**：实时绘制的速度矢量箭头与平行四边形，直观展示了每一时刻合速度如何由两个分速度合成，是理解速度方向变化的关键。
3.  **参数实时联动**：任何参数的调整都会立即反映在动画中，所有矢量、轨迹和数据同步更新，提供即时反馈，鼓励探索式学习。
4.  **认知支架设计**：界面布局引导您从观察整体现象开始，逐步通过“显示控制”揭开分解细节，最后通过调整参数验证规律，符合认知进阶过程。

#### 四、 教学要点（供教师或自学者参考）

1.  **运动的独立性**：重点观察无论水平初速度如何改变，**竖直方向的运动（下落时间、竖直速度）完全不受影响**。反之，改变抛射角（影响`vᵧ`）也不会影响`vₓ`的恒定。这是理解复杂运动的基础。
2.  **轨迹的形成**：开启“分运动点”显示，观察合运动点（紫色）的位置始终由同一时刻的水平分运动点（橙色）和竖直分运动点（青色）的位置**共同决定**，其路径即形成抛物线。
3.  **速度矢量的变化**：
    *   观察**水平分速度 `vₓ`** 箭头长度恒定，方向不变。
    *   观察**竖直分速度 `vᵧ`** 箭头长度均匀增加（向下），方向不变。
    *   观察**合速度 `v`** 箭头（紫色）的长度和方向如何随之变化。特别注意在轨迹最高点，`vᵧ = 0`，此时合速度 `v` 等于 `vₓ`，且方向水平。
4.  **参数影响探究**：
    *   **平抛运动**：固定抛射角为0°，改变`v₀`，观察“水平射程”的变化。
    *   **斜抛运动**：固定`v₀`，改变抛射角`θ`，观察轨迹形状和射程的变化。可以尝试寻找获得最大射程的角度（约45°）。

#### 五、 使用建议

1.  **初次探索**：建议先使用默认参数，点击“播放”，完整观看一遍动画，对抛体运动建立整体印象。
2.  **分层探究**：
    *   **第一层**：隐藏所有分运动点和矢量，只观察合运动的轨迹。
    *   **第二层**：开启“分运动点”，理解位置是如何合成的。
    *   **第三层**：开启“速度矢量”，深入理解速度的合成与变化规律。可使用“步进”功能在关键帧（如起点、最高点、落地前）仔细分析。
3.  **猜想与验证**：在调整参数前，先根据物理规律做出预测（例如：“增大初速度，射程会变远吗？”），然后通过动画验证您的猜想。
4.  **教学应用**：教师可在课堂演示时，引导学生描述观察到的现象，并解释其背后的物理原理。也可将本动画作为学生课后自主探究的辅助工具。

希望这个交互式动画能成为您理解抛体运动的得力助手！祝您学习愉快，探索无限！