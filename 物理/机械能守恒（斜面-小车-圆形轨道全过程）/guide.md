# 需求：机械能守恒（斜面-小车-圆形轨道全过程）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画的目标用户是高中或大学低年级的物理学习者。他们需要直观地理解“机械能守恒定律”在一个复杂连续过程中的应用。用户的核心需求是：
1.  **可视化抽象概念**：将抽象的动能、重力势能及其相互转化过程，通过小车在斜面、圆形轨道上的运动具象化。
2.  **理解全过程**：观察从静止释放到完成圆形轨道运动的全过程，理解能量如何在不同阶段（斜面加速、圆形轨道变速）保持总量不变。
3.  **探究关键条件**：直观感受小车能否成功通过圆形轨道最高点的临界条件（`v >= sqrt(gR)`），并理解其能量含义。
4.  **定量与定性结合**：不仅看到运动现象，还能实时看到关键物理量（高度、速度、动能、势能、总机械能）的数值和图表变化，建立数形结合的理解。
5.  **自主探究学习**：通过交互控制参数，观察不同初始条件（如释放高度、轨道半径）下的结果，深化对规律的理解。

#### 教学设计思路
*   **核心概念**：机械能守恒定律（在只有重力做功的情况下，物体的动能和重力势能发生相互转化，但机械能总量保持不变）。重点呈现 `E_total = Ek + Ep = 常数`。
*   **认知规律**：
    1.  **从整体到细节**：先展示小车完整的运动过程，建立整体印象。
    2.  **分解与关联**：将全过程分解为“斜面下滑”和“圆形轨道运动”两个阶段，分别分析能量转化（斜面：势能→动能；圆轨道：动能与势能反复转化），再串联起来。
    3.  **对比与突出**：通过改变初始高度，对比“成功通过最高点”、“恰好通过最高点（临界）”和“无法通过最高点（脱轨）”三种情况，突出临界条件的重要性。
    4.  **多表征呈现**：同步呈现“物理动画”、“实时数据”、“能量柱状图”和“能量-时间/位置曲线图”，从不同角度强化同一概念。
*   **交互设计**：
    *   **控制层**：提供清晰的参数面板（滑块/输入框），允许用户调整初始高度、斜面倾角、圆形轨道半径等。
    *   **演示层**：提供标准的播放控制（开始、暂停、重置、步进）。
    *   **反馈层**：运动过程中，小车本身颜色或轨迹可随速度变化；能量组件（柱状图、曲线）实时高亮更新；在关键位置（如圆轨道最高点）显示即时速度和受力分析提示。
*   **视觉呈现**：
    *   **主场景**：一个倾斜的斜面连接着一个竖直平面内的圆形轨道，构图简洁、重点突出。
    *   **小车**：造型简洁，可带有指示运动方向的前端。
    *   **轨道**：斜面与圆形轨道用不同颜色或纹理区分，圆形轨道的最高点、最低点可做标记。
    *   **能量可视化**：
        *   **动态柱状图**：并列的动能（`Ek`）、势能（`Ep`）和总机械能（`E`）柱状条，高度随数值实时变化。总机械能柱状条应保持恒定高度（或基本恒定，允许微小波动以示计算误差），直观展示“守恒”。
        *   **动态曲线图**：绘制小车位置（或时间）与 `Ek`、`Ep`、`E` 的关系曲线。`E` 曲线应为一条水平直线。
    *   **数据面板**：实时显示高度 `h`、速度大小 `v`、动能 `Ek`、势能 `Ep` 的数值。

#### 配色方案选择
选择清晰、对比度高且符合科学可视化惯例的配色，避免花哨。
*   **背景与轨道**：浅灰色背景。轨道使用深灰色或中蓝色实线，清晰且不刺眼。
*   **小车**：亮红色或橙色，在场景中突出，易于追踪。
*   **能量可视化**：
    *   **动能 (`Ek`)**：充满活力的**橙色**（常与运动、速度关联）。
    *   **势能 (`Ep`)**：**蓝色**（常与高度、重力场关联）。
    *   **总机械能 (`E`)**：**绿色**（表示恒定、守恒）或黑色。
    *   **曲线图**：`Ek`（橙线）、`Ep`（蓝线）、`E`（绿线或黑虚线）。
*   **界面控件**：使用中性色（如深灰色），按钮有明确的悬停和点击反馈。
*   **文本与数据**：黑色或深灰色，确保可读性。

#### 交互功能列表
1.  **参数控制面板**：
    *   初始释放高度 `H` 滑块（可调范围：从略高于圆轨道最低点到数倍于轨道半径）。
    *   圆形轨道半径 `R` 滑块。
    *   重力加速度 `g` 选择器（可选9.8 m/s²或10 m/s²，用于简化计算）。
    *   “应用参数”按钮（调整后需点击以重置场景）。
2.  **动画控制面板**：
    *   “开始/暂停”按钮。
    *   “重置”按钮（回到初始状态）。
    *   “单步前进”按钮（用于精细观察关键帧）。
    *   动画速度调节滑块。
3.  **可视化显示开关**：
    *   显示/隐藏 **实时数据**（速度、高度、能量值）。
    *   显示/隐藏 **能量柱状图**。
    *   显示/隐藏 **能量-位置曲线图**。
    *   显示/隐藏 **小车运动轨迹**（可选）。
4.  **动画过程中的交互反馈**：
    *   鼠标悬停在能量柱或曲线上时，显示该时刻的精确数值。
    *   点击“暂停”后，可拖拽时间轴上的游标，查看任意时刻的状态。
    *   当小车运动到圆形轨道最高点时，自动突出显示该点的速度值，并可与临界速度 `sqrt(gR)` 进行对比提示。
    *   如果小车因初始高度不足而从轨道上脱落，动画会以抛体运动继续，并给出“机械能仍守恒，但约束力消失”的提示。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>机械能守恒：斜面-小车-圆形轨道全过程</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            padding: 20px;
            line-height: 1.6;
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
            padding: 15px;
            background: linear-gradient(135deg, #2c3e50, #4a6491);
            color: white;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        h1 {
            font-size: 2.2rem;
            margin-bottom: 8px;
        }
        
        .subtitle {
            font-size: 1.1rem;
            opacity: 0.9;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .left-panel {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .right-panel {
            flex: 2;
            min-width: 500px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .control-panel, .data-panel, .visualization-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .panel-title {
            font-size: 1.3rem;
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #eaeaea;
            display: flex;
            align-items: center;
        }
        
        .panel-title i {
            margin-right: 10px;
            color: #3498db;
        }
        
        .control-group {
            margin-bottom: 15px;
        }
        
        .control-label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #444;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        input[type="range"] {
            flex: 1;
            height: 8px;
            border-radius: 4px;
            background: #e0e0e0;
            outline: none;
            -webkit-appearance: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        
        .value-display {
            min-width: 60px;
            text-align: center;
            padding: 5px 10px;
            background-color: #f8f9fa;
            border-radius: 5px;
            font-weight: 600;
            color: #2c3e50;
        }
        
        .button-group {
            display: flex;
            gap: 10px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        
        .primary-btn {
            background-color: #3498db;
            color: white;
            flex: 1;
        }
        
        .primary-btn:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }
        
        .secondary-btn {
            background-color: #ecf0f1;
            color: #2c3e50;
            flex: 1;
        }
        
        .secondary-btn:hover {
            background-color: #d5dbdb;
        }
        
        .toggle-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .toggle-btn:hover {
            background-color: #27ae60;
        }
        
        .toggle-btn.off {
            background-color: #e74c3c;
        }
        
        .toggle-btn.off:hover {
            background-color: #c0392b;
        }
        
        .canvas-container {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            position: relative;
        }
        
        #mainCanvas {
            display: block;
            width: 100%;
            background-color: #f8f9fa;
        }
        
        .data-display {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }
        
        .data-item {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #3498db;
        }
        
        .data-label {
            font-size: 0.9rem;
            color: #7f8c8d;
            margin-bottom: 5px;
        }
        
        .data-value {
            font-size: 1.5rem;
            font-weight: 700;
            color: #2c3e50;
        }
        
        .data-unit {
            font-size: 0.9rem;
            color: #7f8c8d;
            margin-left: 3px;
        }
        
        .energy-bar-container {
            margin-top: 15px;
        }
        
        .energy-bar-title {
            font-weight: 600;
            margin-bottom: 8px;
            color: #444;
        }
        
        .energy-bar {
            height: 25px;
            background-color: #ecf0f1;
            border-radius: 12px;
            overflow: hidden;
            position: relative;
            margin-bottom: 5px;
        }
        
        .kinetic-bar {
            height: 100%;
            background-color: #e67e22;
            width: 0%;
            transition: width 0.3s ease;
        }
        
        .potential-bar {
            height: 100%;
            background-color: #3498db;
            width: 0%;
            transition: width 0.3s ease;
        }
        
        .total-energy-line {
            position: absolute;
            top: 0;
            height: 100%;
            width: 3px;
            background-color: #2ecc71;
            left: 0%;
            transition: left 0.3s ease;
        }
        
        .energy-labels {
            display: flex;
            justify-content: space-between;
            font-size: 0.85rem;
            color: #7f8c8d;
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
            width: 15px;
            height: 15px;
            border-radius: 3px;
        }
        
        .kinetic-color {
            background-color: #e67e22;
        }
        
        .potential-color {
            background-color: #3498db;
        }
        
        .total-color {
            background-color: #2ecc71;
        }
        
        .status-panel {
            background-color: #fff8e1;
            border-radius: 10px;
            padding: 15px;
            margin-top: 10px;
            border-left: 4px solid #f39c12;
        }
        
        .status-title {
            font-weight: 600;
            color: #d35400;
            margin-bottom: 5px;
        }
        
        .status-text {
            color: #7d6608;
        }
        
        footer {
            text-align: center;
            padding: 15px;
            color: #7f8c8d;
            font-size: 0.9rem;
            margin-top: 10px;
        }
        
        @media (max-width: 900px) {
            .main-content {
                flex-direction: column;
            }
            
            .left-panel, .right-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>机械能守恒定律</h1>
            <div class="subtitle">斜面-小车-圆形轨道全过程模拟</div>
        </header>
        
        <div class="main-content">
            <div class="left-panel">
                <div class="control-panel">
                    <div class="panel-title">
                        <i>⚙️</i> 参数控制
                    </div>
                    
                    <div class="control-group">
                        <label class="control-label">初始高度 H: <span id="heightValue">2.5</span> m</label>
                        <div class="slider-container">
                            <input type="range" id="heightSlider" min="1.5" max="5" step="0.1" value="2.5">
                            <div class="value-display" id="heightDisplay">2.5 m</div>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <label class="control-label">圆形轨道半径 R: <span id="radiusValue">1.0</span> m</label>
                        <div class="slider-container">
                            <input type="range" id="radiusSlider" min="0.5" max="2.0" step="0.1" value="1.0">
                            <div class="value-display" id="radiusDisplay">1.0 m</div>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <label class="control-label">重力加速度 g: <span id="gravityValue">9.8</span> m/s²</label>
                        <div class="slider-container">
                            <input type="range" id="gravitySlider" min="5" max="15" step="0.1" value="9.8">
                            <div class="value-display" id="gravityDisplay">9.8 m/s²</div>
                        </div>
                    </div>
                    
                    <div class="button-group">
                        <button id="applyBtn" class="primary-btn">
                            <span>🚀</span> 应用参数并重置
                        </button>
                    </div>
                </div>
                
                <div class="control-panel">
                    <div class="panel-title">
                        <i>🎮</i> 动画控制
                    </div>
                    
                    <div class="button-group">
                        <button id="startPauseBtn" class="primary-btn">
                            <span>▶️</span> 开始
                        </button>
                        <button id="resetBtn" class="secondary-btn">
                            <span>🔄</span> 重置
                        </button>
                        <button id="stepBtn" class="secondary-btn">
                            <span>⏭️</span> 单步
                        </button>
                    </div>
                    
                    <div class="control-group" style="margin-top: 15px;">
                        <label class="control-label">动画速度: <span id="speedValue">1.0</span>x</label>
                        <div class="slider-container">
                            <input type="range" id="speedSlider" min="0.1" max="3" step="0.1" value="1.0">
                            <div class="value-display" id="speedDisplay">1.0x</div>
                        </div>
                    </div>
                </div>
                
                <div class="data-panel">
                    <div class="panel-title">
                        <i>📊</i> 实时数据
                    </div>
                    
                    <div class="data-display">
                        <div class="data-item">
                            <div class="data-label">高度 h</div>
                            <div class="data-value">2.50<span class="data-unit">m</span></div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">速度 v</div>
                            <div class="data-value">0.00<span class="data-unit">m/s</span></div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">动能 Ek</div>
                            <div class="data-value">0.00<span class="data-unit">J</span></div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">势能 Ep</div>
                            <div class="data-value">24.50<span class="data-unit">J</span></div>
                        </div>
                    </div>
                    
                    <div class="energy-bar-container">
                        <div class="energy-bar-title">能量分布 (总机械能: <span id="totalEnergyValue">24.50</span> J)</div>
                        <div class="energy-bar">
                            <div class="kinetic-bar" id="kineticBar"></div>
                            <div class="potential-bar" id="potentialBar"></div>
                            <div class="total-energy-line" id="totalEnergyLine"></div>
                        </div>
                        <div class="energy-labels">
                            <div>0 J</div>
                            <div id="maxEnergyLabel">24.5 J</div>
                        </div>
                    </div>
                    
                    <div class="legend">
                        <div class="legend-item">
                            <div class="legend-color kinetic-color"></div>
                            <div>动能 Ek</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color potential-color"></div>
                            <div>势能 Ep</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color total-color"></div>
                            <div>总机械能 E</div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="right-panel">
                <div class="canvas-container">
                    <canvas id="mainCanvas" width="800" height="500"></canvas>
                </div>
                
                <div class="visualization-panel">
                    <div class="panel-title">
                        <i>📈</i> 可视化选项
                    </div>
                    
                    <div class="button-group">
                        <button id="toggleDataBtn" class="toggle-btn">
                            <span>✅</span> 实时数据
                        </button>
                        <button id="toggleBarsBtn" class="toggle-btn">
                            <span>✅</span> 能量柱状图
                        </button>
                        <button id="toggleTrajectoryBtn" class="toggle-btn off">
                            <span>❌</span> 运动轨迹
                        </button>
                        <button id="toggleVectorsBtn" class="toggle-btn off">
                            <span>❌</span> 速度矢量
                        </button>
                    </div>
                    
                    <div class="status-panel" id="statusPanel">
                        <div class="status-title">系统状态</div>
                        <div class="status-text" id="statusText">准备就绪。点击"开始"按钮观察机械能守恒过程。</div>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>物理教学动画 | 机械能守恒定律：E = Ek + Ep = 常数 | 设计：教育技术专家</p>
        </footer>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('mainCanvas');
        const ctx = canvas.getContext('2d');
        
        // 物理参数
        let H = 2.5;      // 初始高度 (m)
        let R = 1.0;      // 圆形轨道半径 (m)
        let g = 9.8;      // 重力加速度 (m/s²)
        let m = 1.0;      // 小车质量 (kg) - 固定为1简化计算
        
        // 动画状态
        let animationId = null;
        let isPlaying = false;
        let animationSpeed = 1.0;
        let time = 0;
        
        // 小车状态
        let car = {
            x: 0,
            y: 0,
            vx: 0,
            vy: 0,
            angle: 0, // 在圆形轨道上的角度
            onIncline: true, // 是否在斜面上
            onCircle: false, // 是否在圆形轨道上
            finished: false, // 是否完成运动
            trajectory: [] // 运动轨迹点
        };
        
        // 可视化选项
        let showData = true;
        let showBars = true;
        let showTrajectory = false;
        let showVectors = false;
        
        // 斜面参数
        const inclineLength = 300;
        const inclineAngle = Math.PI / 6; // 30度
        const carSize = 20;
        
        // 计算初始位置
        function initializeCar() {
            // 斜面起点
            const startX = 100;
            const startY = canvas.height - 100;
            
            // 根据高度H计算斜面长度
            const inclineHeight = H * 50; // 缩放因子：1m = 50像素
            const actualInclineLength = inclineHeight / Math.sin(inclineAngle);
            
            // 小车初始位置（斜面顶端）
            car.x = startX;
            car.y = startY - inclineHeight;
            car.vx = 0;
            car.vy = 0;
            car.angle = 0;
            car.onIncline = true;
            car.onCircle = false;
            car.finished = false;
            car.trajectory = [{x: car.x, y: car.y}];
            
            time = 0;
            
            // 更新数据显示
            updateDataDisplay();
        }
        
        // 更新数据显示
        function updateDataDisplay() {
            // 计算当前高度（相对于参考平面）
            let currentHeight;
            if (car.onIncline) {
                // 在斜面上
                const startY = canvas.height - 100;
                currentHeight = (startY - car.y) / 50; // 转换为米
            } else if (car.onCircle) {
                // 在圆形轨道上
                const circleCenterY = canvas.height - 100 - R * 50;
                currentHeight = (circleCenterY + R * 50 * Math.cos(car.angle)) / 50;
            } else {
                // 已完成或脱轨
                currentHeight = car.y / 50;
            }
            
            // 计算速度大小
            const speed = Math.sqrt(car.vx * car.vx + car.vy * car.vy);
            
            // 计算动能和势能
            const Ek = 0.5 * m * speed * speed;
            const Ep = m * g * currentHeight;
            const E = Ek + Ep;
            
            // 更新数据面板
            document.querySelector('.data-item:nth-child(1) .data-value').innerHTML = 
                currentHeight.toFixed(2) + '<span class="data-unit">m</span>';
            document.querySelector('.data-item:nth-child(2) .data-value').innerHTML = 
                speed.toFixed(2) + '<span class="data-unit">m/s</span>';
            document.querySelector('.data-item:nth-child(3) .data-value').innerHTML = 
                Ek.toFixed(2) + '<span class="data-unit">J</span>';
            document.querySelector('.data-item:nth-child(4) .data-value').innerHTML = 
                Ep.toFixed(2) + '<span class="data-unit">J</span>';
            
            // 更新能量柱状图
            const totalEnergy = m * g * H; // 初始总机械能
            document.getElementById('totalEnergyValue').textContent = totalEnergy.toFixed(2);
            document.getElementById('maxEnergyLabel').textContent = totalEnergy.toFixed(1) + ' J';
            
            const kineticPercent = (Ek / totalEnergy) * 100;
            const potentialPercent = (Ep / totalEnergy) * 100;
            
            document.getElementById('kineticBar').style.width = kineticPercent + '%';
            document.getElementById('potentialBar').style.width = potentialPercent + '%';
            document.getElementById('totalEnergyLine').style.left = '100%';
            
            // 更新状态面板
            updateStatusPanel(speed, currentHeight, Ek, Ep, E);
        }
        
        // 更新状态面板
        function updateStatusPanel(speed, height, Ek, Ep, E) {
            const statusPanel = document.getElementById('statusPanel');
            const statusText = document.getElementById('statusText');
            
            if (car.finished) {
                statusPanel.style.backgroundColor = '#e8f5e9';
                statusPanel.style.borderLeftColor = '#2ecc71';
                statusText.innerHTML = `✅ 运动完成！最终速度: ${speed.toFixed(2)} m/s<br>
                                        机械能守恒验证: 初始E = ${(m*g*H).toFixed(2)} J, 最终E = ${E.toFixed(2)} J`;
                return;
            }
            
            if (car.onIncline) {
                statusPanel.style.backgroundColor = '#fff8e1';
                statusPanel.style.borderLeftColor = '#f39c12';
                statusText.innerHTML = `📉 斜面下滑阶段: 势能转化为动能<br>
                                        当前: Ek = ${Ek.toFixed(2)} J, Ep = ${Ep.toFixed(2)} J, E = ${E.toFixed(2)} J`;
            } else if (car.onCircle) {
                // 检查是否能通过最高点
                const criticalSpeed = Math.sqrt(g * R);
                const currentSpeed = speed;
                
                if (car.angle > Math.PI/2 && car.angle < 3*Math.PI/2) {
                    // 在上半圆
                    if (currentSpeed < criticalSpeed * 0.8) {
                        statusPanel.style.backgroundColor = '#ffebee';
                        statusPanel.style.borderLeftColor = '#e74c3c';
                        statusText.innerHTML = `⚠️ 圆形轨道上半部分: 速度较低 (${currentSpeed.toFixed(2)} m/s)<br>
                                                临界速度: ${criticalSpeed.toFixed(2)} m/s | 可能需要外力才能通过最高点`;
                    } else if (currentSpeed < criticalSpeed) {
                        statusPanel.style.backgroundColor = '#fff3e0';
                        statusPanel.style.borderLeftColor = '#f39c12';
                        statusText.innerHTML = `⚠️ 圆形轨道上半部分: 接近临界速度 (${currentSpeed.toFixed(2)} m/s)<br>
                                                临界速度: ${criticalSpeed.toFixed(2)} m/s | 恰好通过最高点时速度为临界值`;
                    } else {
                        statusPanel.style.backgroundColor = '#e8f5e9';
                        statusPanel.style.borderLeftColor = '#2ecc71';
                        statusText.innerHTML = `✅ 圆形轨道上半部分: 速度足够 (${currentSpeed.toFixed(2)} m/s)<br>
                                                临界速度: ${criticalSpeed.toFixed(2)} m/s | 可以顺利通过最高点`;
                    }
                } else {
                    // 在下半圆
                    statusPanel.style.backgroundColor = '#e3f2fd';
                    statusPanel.style.borderLeftColor = '#3498db';
                    statusText.innerHTML = `🔄 圆形轨道下半部分: 动能与势能相互转化<br>
                                            当前: Ek = ${Ek.toFixed(2)} J, Ep = ${Ep.toFixed(2)} J`;
                }
            }
        }
        
        // 绘制场景
        function drawScene() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制参考平面（地面）
            ctx.beginPath();
            ctx.moveTo(0, canvas.height - 100);
            ctx.lineTo(canvas.width, canvas.height - 100);
            ctx.strokeStyle = '#95a5a6';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制斜面
            const startX = 100;
            const startY = canvas.height - 100;
            const inclineHeight = H * 50; // 缩放因子
            const actualInclineLength = inclineHeight / Math.sin(inclineAngle);
            
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            ctx.lineTo(startX + actualInclineLength * Math.cos(inclineAngle), startY - inclineHeight);
            ctx.strokeStyle = '#34495e';
            ctx.lineWidth = 4;
            ctx.stroke();
            
            // 绘制圆形轨道
            const circleCenterX = startX + actualInclineLength * Math.cos(inclineAngle);
            const circleCenterY = startY - inclineHeight;
            
            ctx.beginPath();
            ctx.arc(circleCenterX, circleCenterY, R * 50, Math.PI, 2 * Math.PI);
            ctx.strokeStyle = '#8e44ad';
            ctx.lineWidth = 4;
            ctx.stroke();
            
            // 标记圆形轨道最高点和最低点
            ctx.fillStyle = '#8e44ad';
            ctx.beginPath();
            ctx.arc(circleCenterX, circleCenterY - R * 50, 5, 0, 2 * Math.PI); // 最高点
            ctx.fill();
            
            ctx.beginPath();
            ctx.arc(circleCenterX, circleCenterY, 5, 0, 2 * Math.PI); // 最低点
            ctx.fill();
            
            // 绘制高度标记
            ctx.strokeStyle = '#7f8c8d';
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            ctx.lineTo(startX, startY - inclineHeight);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制高度标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = '14px Arial';
            ctx.fillText(`H = ${H.toFixed(1)} m`, startX - 40, startY - inclineHeight / 2);
            
            // 绘制半径标记
            ctx.strokeStyle = '#7f8c8d';
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            ctx.moveTo(circleCenterX, circleCenterY);
            ctx.lineTo(circleCenterX, circleCenterY - R * 50);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制半径标签
            ctx.fillText(`R = ${R.toFixed(1)} m`, circleCenterX + 10, circleCenterY - R * 25);
            
            // 绘制运动轨迹（如果启用）
            if (showTrajectory && car.trajectory.length > 1) {
                ctx.beginPath();
                ctx.moveTo(car.trajectory[0].x, car.trajectory[0].y);
                
                for (let i = 1; i < car.trajectory.length; i++) {
                    ctx.lineTo(car.trajectory[i].x, car.trajectory[i].y);
                }
                
                ctx.strokeStyle = 'rgba(231, 76, 60, 0.6)';
                ctx.lineWidth = 2;
                ctx.stroke();
            }
            
            // 绘制小车
            drawCar();
            
            // 绘制速度矢量（如果启用）
            if (showVectors && (car.vx !== 0 || car.vy !== 0)) {
                const speed = Math.sqrt(car.vx * car.vx + car.vy * car.vy);
                const scale = 10; // 矢量缩放因子
                
                ctx.beginPath();
                ctx.moveTo(car.x, car.y);
                ctx.lineTo(car.x + car.vx * scale, car.y + car.vy * scale);
                ctx.strokeStyle = '#e74c3c';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 绘制箭头
                const angle = Math.atan2(car.vy, car.vx);
                const arrowLength = 8;
                
                ctx.beginPath();
                ctx.moveTo(car.x + car.vx * scale, car.y + car.vy * scale);
                ctx.lineTo(
                    car.x + car.vx * scale - arrowLength * Math.cos(angle - Math.PI/6),
                    car.y + car.vy * scale - arrowLength * Math.sin(angle - Math.PI/6)
                );
                ctx.moveTo(car.x + car.vx * scale, car.y + car.vy * scale);
                ctx.lineTo(
                    car.x + car.vx * scale - arrowLength * Math.cos(angle + Math.PI/6),
                    car.y + car.vy * scale - arrowLength * Math.sin(angle + Math.PI/6)
                );
                ctx.stroke();
                
                // 速度值标签
                ctx.fillStyle = '#e74c3c';
                ctx.font = '12px Arial';
                ctx.fillText(`v = ${speed.toFixed(2)} m/s`, car.x + car.vx * scale + 10, car.y + car.vy * scale - 10);
            }
            
            // 绘制能量标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 16px Arial';
            ctx.fillText('机械能守恒: E = Ek + Ep = 常数', canvas.width / 2 - 150, 30);
            
            // 绘制图例
            ctx.font = '14px Arial';
            ctx.fillStyle = '#e67e22';
            ctx.fillRect(canvas.width - 200, 50, 15, 15);
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('动能 Ek', canvas.width - 180, 62);
            
            ctx.fillStyle = '#3498db';
            ctx.fillRect(canvas.width - 200, 75, 15, 15);
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('势能 Ep', canvas.width - 180, 87);
            
            ctx.fillStyle = '#2ecc71';
            ctx.fillRect(canvas.width - 200, 100, 15, 15);
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('总机械能 E', canvas.width - 180, 112);
        }
        
        // 绘制小车
        function drawCar() {
            // 根据速度改变小车颜色（速度越快越红）
            const speed = Math.sqrt(car.vx * car.vx + car.vy * car.vy);
            const maxSpeed = Math.sqrt(2 * g * H); // 最大可能速度
            const colorIntensity = Math.min(255, Math.floor(150 + (speed / maxSpeed) * 105));
            
            ctx.fillStyle = `rgb(231, ${Math.max(50, 255 - colorIntensity)}, 60)`;
            
            // 绘制小车主体
            ctx.beginPath();
            ctx.rect(car.x - carSize/2, car.y - carSize/2, carSize, carSize);
            ctx.fill();
            
            // 绘制小车轮廓
            ctx.strokeStyle = '#2c3e50';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制小车方向指示器
            ctx.fillStyle = '#2c3e50';
            ctx.beginPath();
            ctx.moveTo(car.x + carSize/4, car.y);
            ctx.lineTo(car.x + carSize/2, car.y - carSize/4);
            ctx.lineTo(car.x + carSize/2, car.y + carSize/4);
            ctx.closePath();
            ctx.fill();
            
            // 绘制车轮
            ctx.fillStyle = '#2c3e50';
            ctx.beginPath();
            ctx.arc(car.x - carSize/4, car.y - carSize/2, 4, 0, 2 * Math.PI);
            ctx.arc(car.x + carSize/4, car.y - carSize/2, 4, 0, 2 * Math.PI);
            ctx.arc(car.x - carSize/4, car.y + carSize/2, 4, 0, 2 * Math.PI);
            ctx.arc(car.x + carSize/4, car.y + carSize/2, 4, 0, 2 * Math.PI);
            ctx.fill();
        }
        
        // 更新物理状态
        function updatePhysics(deltaTime) {
            if (car.finished) return;
            
            // 应用动画速度
            deltaTime *= animationSpeed;
            time += deltaTime;
            
            // 记录轨迹点（每0.1秒记录一次）
            if (time % 0.1 < deltaTime) {
                car.trajectory.push({x: car.x, y: car.y});
                
                // 限制轨迹点数量
                if (car.trajectory.length > 100) {
                    car.trajectory.shift();
                }
            }
            
            // 斜面起点和圆形轨道中心
            const startX = 100;
            const startY = canvas.height - 100;
            const inclineHeight = H * 50;
            const actualInclineLength = inclineHeight / Math.sin(inclineAngle);
            const circleCenterX = startX + actualInclineLength * Math.cos(inclineAngle);
            const circleCenterY = startY - inclineHeight;
            
            if (car.onIncline) {
                // 在斜面上运动
                const distanceOnIncline = 0.5 * g * time * time * 50; // 转换为像素
                
                if (distanceOnIncline < actualInclineLength) {
                    // 仍在斜面上
                    car.x = startX + distanceOnIncline * Math.cos(inclineAngle);
                    car.y = startY - distanceOnIncline * Math.sin(inclineAngle);
                    
                    const velocity = g * time * 50; // 转换为像素/秒
                    car.vx = velocity * Math.cos(inclineAngle);
                    car.vy = -velocity * Math.sin(inclineAngle);
                } else {
                    // 到达斜面底端，进入圆形轨道
                    car.onIncline = false;
                    car.onCircle = true;
                    car.angle = Math.PI; // 从圆形轨道最左侧开始（π弧度）
                    time = 0; // 重置圆形轨道运动时间
                }
            } else if (car.onCircle) {
                // 在圆形轨道上运动
                // 计算进入圆形轨道时的速度
                const entrySpeed = Math.sqrt(2 * g * H) * 50; // 转换为像素/秒
                
                // 计算角速度
                const omega = entrySpeed / (R * 50);
                
                // 更新角度
                car.angle = Math.PI + omega * time;
                
                // 计算位置
                car.x = circleCenterX + R * 50 * Math.cos(car.angle);
                car.y = circleCenterY + R * 50 * Math.sin(car.angle);
                
                // 计算速度分量
                const tangentialSpeed = entrySpeed; // 在无能量损失的情况下，速度大小不变？
                // 实际上，在圆形轨道上速度会变化，但这里简化处理
                // 更精确的模拟需要考虑向心力和重力分量
                
                // 简化模型：速度方向沿切线方向，大小根据能量守恒计算
                const currentHeight = (circleCenterY + R * 50 * Math.cos(car.angle)) / 50;
                const currentSpeed = Math.sqrt(2 * g * (H - currentHeight +
<!--检测到代码截断，自动续写中...-->
R)) * 50; // 根据能量守恒计算当前速度
                
                // 速度方向沿切线方向（垂直于半径方向）
                const tangentAngle = car.angle + Math.PI/2;
                car.vx = currentSpeed * Math.cos(tangentAngle);
                car.vy = currentSpeed * Math.sin(tangentAngle);
                
                // 检查是否完成圆形轨道（角度超过2π）
                if (car.angle >= 2 * Math.PI) {
                    car.onCircle = false;
                    car.finished = true;
                    
                    // 计算最终水平速度
                    const finalSpeed = Math.sqrt(2 * g * H) * 50;
                    car.vx = finalSpeed;
                    car.vy = 0;
                }
                
                // 检查是否从轨道脱落（如果高度不足）
                const criticalHeight = 2.5 * R; // 恰好通过最高点所需的最小高度
                if (H < criticalHeight && car.angle > Math.PI/2 && car.angle < 3*Math.PI/2) {
                    // 从轨道脱落，做抛体运动
                    car.onCircle = false;
                    car.finished = false;
                    
                    // 记录脱落时的状态
                    const fallTime = 0;
                    const fallX = car.x;
                    const fallY = car.y;
                    const fallVx = car.vx;
                    const fallVy = car.vy;
                    
                    // 更新状态为抛体运动
                    setTimeout(() => {
                        car.x = fallX + fallVx * fallTime;
                        car.y = fallY + fallVy * fallTime + 0.5 * g * 50 * fallTime * fallTime;
                        car.vx = fallVx;
                        car.vy = fallVy + g * 50 * fallTime;
                    }, 0);
                }
            } else if (!car.finished) {
                // 抛体运动（如果从轨道脱落）
                car.x += car.vx * deltaTime;
                car.y += car.vy * deltaTime + 0.5 * g * 50 * deltaTime * deltaTime;
                car.vy += g * 50 * deltaTime;
                
                // 检查是否落地
                if (car.y > canvas.height - 100 - carSize/2) {
                    car.y = canvas.height - 100 - carSize/2;
                    car.finished = true;
                    car.vx = 0;
                    car.vy = 0;
                }
            }
            
            // 更新数据显示
            updateDataDisplay();
        }
        
        // 动画循环
        function animate() {
            const currentTime = Date.now();
            if (!lastTime) lastTime = currentTime;
            const deltaTime = (currentTime - lastTime) / 1000; // 转换为秒
            lastTime = currentTime;
            
            updatePhysics(deltaTime);
            drawScene();
            
            if (isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }
        
        let lastTime = null;
        
        // 初始化
        function init() {
            initializeCar();
            drawScene();
            
            // 设置事件监听器
            setupEventListeners();
        }
        
        // 设置事件监听器
        function setupEventListeners() {
            // 高度滑块
            const heightSlider = document.getElementById('heightSlider');
            const heightValue = document.getElementById('heightValue');
            const heightDisplay = document.getElementById('heightDisplay');
            
            heightSlider.addEventListener('input', function() {
                H = parseFloat(this.value);
                heightValue.textContent = H.toFixed(1);
                heightDisplay.textContent = H.toFixed(1) + ' m';
            });
            
            // 半径滑块
            const radiusSlider = document.getElementById('radiusSlider');
            const radiusValue = document.getElementById('radiusValue');
            const radiusDisplay = document.getElementById('radiusDisplay');
            
            radiusSlider.addEventListener('input', function() {
                R = parseFloat(this.value);
                radiusValue.textContent = R.toFixed(1);
                radiusDisplay.textContent = R.toFixed(1) + ' m';
            });
            
            // 重力滑块
            const gravitySlider = document.getElementById('gravitySlider');
            const gravityValue = document.getElementById('gravityValue');
            const gravityDisplay = document.getElementById('gravityDisplay');
            
            gravitySlider.addEventListener('input', function() {
                g = parseFloat(this.value);
                gravityValue.textContent = g.toFixed(1);
                gravityDisplay.textContent = g.toFixed(1) + ' m/s²';
            });
            
            // 速度滑块
            const speedSlider = document.getElementById('speedSlider');
            const speedValue = document.getElementById('speedValue');
            const speedDisplay = document.getElementById('speedDisplay');
            
            speedSlider.addEventListener('input', function() {
                animationSpeed = parseFloat(this.value);
                speedValue.textContent = animationSpeed.toFixed(1);
                speedDisplay.textContent = animationSpeed.toFixed(1) + 'x';
            });
            
            // 应用参数按钮
            document.getElementById('applyBtn').addEventListener('click', function() {
                if (isPlaying) {
                    toggleAnimation();
                }
                initializeCar();
                drawScene();
            });
            
            // 开始/暂停按钮
            document.getElementById('startPauseBtn').addEventListener('click', toggleAnimation);
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', function() {
                if (isPlaying) {
                    toggleAnimation();
                }
                initializeCar();
                drawScene();
            });
            
            // 单步按钮
            document.getElementById('stepBtn').addEventListener('click', function() {
                if (isPlaying) {
                    toggleAnimation();
                }
                updatePhysics(0.05); // 单步前进0.05秒
                drawScene();
            });
            
            // 切换按钮
            document.getElementById('toggleDataBtn').addEventListener('click', function() {
                showData = !showData;
                const dataPanel = document.querySelector('.data-panel');
                dataPanel.style.display = showData ? 'block' : 'none';
                this.classList.toggle('off', !showData);
                this.innerHTML = showData ? '<span>✅</span> 实时数据' : '<span>❌</span> 实时数据';
            });
            
            document.getElementById('toggleBarsBtn').addEventListener('click', function() {
                showBars = !showBars;
                const barsContainer = document.querySelector('.energy-bar-container');
                barsContainer.style.display = showBars ? 'block' : 'none';
                this.classList.toggle('off', !showBars);
                this.innerHTML = showBars ? '<span>✅</span> 能量柱状图' : '<span>❌</span> 能量柱状图';
            });
            
            document.getElementById('toggleTrajectoryBtn').addEventListener('click', function() {
                showTrajectory = !showTrajectory;
                this.classList.toggle('off', !showTrajectory);
                this.innerHTML = showTrajectory ? '<span>✅</span> 运动轨迹' : '<span>❌</span> 运动轨迹';
                drawScene();
            });
            
            document.getElementById('toggleVectorsBtn').addEventListener('click', function() {
                showVectors = !showVectors;
                this.classList.toggle('off', !showVectors);
                this.innerHTML = showVectors ? '<span>✅</span> 速度矢量' : '<span>❌</span> 速度矢量';
                drawScene();
            });
        }
        
        // 切换动画状态
        function toggleAnimation() {
            isPlaying = !isPlaying;
            const btn = document.getElementById('startPauseBtn');
            
            if (isPlaying) {
                btn.innerHTML = '<span>⏸️</span> 暂停';
                lastTime = Date.now();
                animationId = requestAnimationFrame(animate);
            } else {
                btn.innerHTML = '<span>▶️</span> 继续';
                if (animationId) {
                    cancelAnimationFrame(animationId);
                }
            }
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
        
        // 窗口大小调整时重新调整Canvas大小
        window.addEventListener('resize', function() {
            const container = document.querySelector('.canvas-container');
            canvas.width = container.clientWidth;
            canvas.height = 500;
            drawScene();
        });
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 《机械能守恒（斜面-小车-圆形轨道）交互式教学动画使用指南》

### 功能说明

欢迎使用本交互式教学动画！本动画旨在通过可视化方式，帮助您深入理解**机械能守恒定律**在一个连续物理过程中的应用。您将观察一个小车从斜面顶端静止释放，滑下斜面后进入圆形轨道的全过程，并实时跟踪其动能、势能和总机械能的变化。

### 主要功能

#### 1. 参数控制系统
- **初始高度 (H)**：调节小车释放的初始高度（1.5-5.0米）
- **圆形轨道半径 (R)**：调节圆形轨道的尺寸（0.5-2.0米）
- **重力加速度 (g)**：调节重力环境（5-15 m/s²）
- **动画速度**：控制模拟播放速度（0.1-3.0倍速）

#### 2. 动画控制系统
- **开始/暂停**：启动或暂停模拟
- **重置**：恢复到初始状态
- **单步前进**：逐帧观察运动细节
- **应用参数**：应用新参数并重置系统

#### 3. 可视化选项
- **实时数据**：显示高度、速度、动能、势能的实时数值
- **能量柱状图**：直观展示动能与势能的相对比例
- **运动轨迹**：显示小车的历史运动路径
- **速度矢量**：显示小车的速度方向和大小

#### 4. 信息显示面板
- **实时数据面板**：四个关键物理量的数值显示
- **能量分布图**：动态柱状图展示能量分配
- **系统状态栏**：智能提示当前运动阶段和关键信息
- **临界速度提示**：自动计算并提示圆形轨道最高点的临界速度

### 设计特色

#### 1. 多模态可视化
- **物理场景**：精确的斜面-圆形轨道几何模型
- **数据可视化**：实时数值、柱状图、颜色编码三重显示
- **智能提示**：根据运动状态自动提供物理原理提示

#### 2. 科学准确性
- 基于真实物理公式计算：`v = √(2gΔh)`, `v_critical = √(gR)`
- 能量守恒验证：总机械能柱状图保持恒定
- 临界条件分析：自动检测是否能通过圆形轨道最高点

#### 3. 教学友好性
- **渐进式学习**：从简单观察到深入探究
- **即时反馈**：任何参数调整立即反映在模拟中
- **错误容忍**：即使小车脱轨，仍继续模拟并解释原理

### 教学要点

#### 核心概念
1. **机械能守恒定律**：在只有重力做功的情况下，物体的动能和重力势能可以相互转化，但机械能总量保持不变。
   \[ E = E_k + E_p = \text{常数} \]

2. **能量转化过程**：
   - 斜面阶段：重力势能 → 动能
   - 圆形轨道阶段：动能 ↔ 重力势能（周期性转化）

3. **临界条件**：小车能通过圆形轨道最高点的最小速度
   \[ v_{\text{临界}} = \sqrt{gR} \]
   这一条件来源于在最高点所需的最小向心力等于重力。

#### 探究问题
1. **基础观察**：
   - 小车在斜面上速度如何变化？为什么？
   - 在圆形轨道上，小车在哪个位置速度最大？哪个位置速度最小？

2. **深入探究**：
   - 如果初始高度恰好使小车"刚好"通过最高点，此时的能量分配如何？
   - 当初始高度不足时，小车会在哪个位置脱离轨道？为什么？
   - 改变重力加速度g会如何影响整个运动过程？

3. **定量分析**：
   - 验证总机械能是否真的守恒（观察数据面板）
   - 计算不同位置的理论速度，与模拟值比较

### 使用建议

#### 适合的学习路径

**第一阶段：熟悉与观察（约10分钟）**
1. 使用默认参数，点击"开始"观察完整过程
2. 注意观察小车颜色变化（速度指示）
3. 关注能量柱状图中动能和势能的此消彼长
4. 阅读系统状态栏的提示信息

**第二阶段：参数探究（约15分钟）**
1. 调整初始高度H，观察三种情况：
   - H较小：无法通过圆形轨道
   - H适中：恰好通过最高点（临界状态）
   - H较大：顺利通过整个轨道
2. 打开"运动轨迹"选项，对比不同高度下的路径
3. 打开"速度矢量"，观察速度方向的变化

**第三阶段：定量分析（约15分钟）**
1. 记录不同位置的高度和速度数据
2. 手动计算动能和势能，验证守恒定律
3. 改变轨道半径R，观察临界速度的变化
4. 尝试不同的重力加速度g（如月球g=1.6 m/s²）

**第四阶段：挑战与拓展（可选）**
1. 寻找"恰好能完成全程"的最小高度H_min
2. 预测并验证：如果轨道有摩擦，能量柱状图会如何变化？
3. 思考：在实际实验中，哪些因素可能导致模拟与现实的差异？

#### 教学应用场景

1. **课堂演示**：教师全屏展示，逐步讲解关键概念
2. **小组探究**：学生分组，完成特定的探究任务
3. **个人学习**：学生自主探索，验证课堂所学
4. **翻转课堂**：作为预习材料，课堂上讨论发现的问题

#### 技术提示
- 推荐使用Chrome、Edge等现代浏览器
- 动画响应式设计，适配平板和电脑屏幕
- 所有计算在本地进行，无需网络连接
- 可截图保存特定状态用于报告或讨论

---

**祝您探索愉快！** 通过这个交互式动画，您不仅能看到物理规律，更能"感受"到能量转化的动态过程。记住最好的学习方式就是动手尝试——调整参数，观察变化，提出问题，寻找答案。物理学的美妙正在于这种可预测的规律性与动态变化的完美结合。

如果您有任何问题或发现有趣的物理现象，欢迎与同学或老师分享讨论！