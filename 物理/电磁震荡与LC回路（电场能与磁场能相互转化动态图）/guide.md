# 需求：电磁震荡与LC回路（电场能与磁场能相互转化动态图）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中或大学低年级的物理学习者。用户的核心需求是：
1.  **直观理解抽象过程**：电磁振荡和能量转化是肉眼不可见的物理过程，用户需要一个动态、可视化的模型来建立直观感受。
2.  **掌握关键变量关系**：理解电荷 `q`、电流 `i`、电场能、磁场能如何随时间周期性变化，以及它们之间的相位关系。
3.  **探究参数影响**：用户希望了解电感 `L` 和电容 `C` 的数值如何影响振荡频率（周期），并能通过交互验证公式 `T = 2π√LC`。
4.  **建立统一图景**：将抽象的电路图、具体的物理过程（电荷移动、场的变化）和抽象的数学图像（正弦曲线）三者关联起来。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
*   **核心概念**：
    *   **能量守恒与转化**：在无阻尼理想LC回路中，总能量（电场能 + 磁场能）保持不变，能量在电容（电场）和电感（磁场）之间周期性转移。
    *   **相位关系**：电荷 `q`（或电压 `U`）与电流 `i` 存在90度的相位差。当 `q` 最大（电场能最大）时，`i` 为0（磁场能为0）；反之亦然。
    *   **决定因素**：振荡周期 `T` 由回路本身的电感 `L` 和电容 `C` 决定。

*   **认知规律**：
    1.  **从具体到抽象**：先展示电荷在极板间往复运动的“宏观”动画，再引出电场和磁场的“场”的视角，最后用波形图进行数学抽象。
    2.  **多表征联动**：将电路动画、场能变化动画和波形图同步呈现，强化概念之间的联系。
    3.  **主动探索**：允许用户调整 `L` 和 `C` 参数，观察振荡快慢的变化，从现象归纳规律。

*   **交互设计**：
    *   **主控面板**：提供“播放/暂停”、“重置”按钮，控制动画运行。
    *   **参数调节**：提供滑块或输入框，允许用户实时调节电感 `L` 和电容 `C` 的值，动画即时响应。
    *   **视图切换**：允许用户选择显示/隐藏电场线、磁场线、能量条、波形图等图层，避免初学时信息过载。
    *   **关键点高亮**：当鼠标悬停或动画运行到特定相位（如 `q` 最大）时，高亮对应的电路部分、能量条和波形图上的点。

*   **视觉呈现**：
    *   **布局**：采用三栏式布局。左侧为**LC回路动态模拟区**（核心动画），中部为**能量转化可视化区**（动态柱状图或饼图），右侧为**变量随时间变化曲线区**（`q-t`, `i-t`, `能量-t` 曲线）。
    *   **动画元素**：
        *   **电容**：用平行板电容器表示，极板上的“+”和“-”号数量动态变化，直观表示电荷量 `q`。用疏密变化的电场线连接两极板。
        *   **电感**：用线圈表示，用环绕线圈的圆圈（⊗ 和 ⊙）表示磁场方向与强弱，其疏密和方向随电流 `i` 变化。
        *   **电荷流**：用流动的光点或箭头表示电流方向与大小。
        *   **能量可视化**：用两个并排的、高度动态变化的彩色柱状图分别表示电场能和磁场能，其总和保持恒定。也可用比例动态变化的双色圆饼图表示。

#### 配色方案选择
选择清晰、科学且符合物理直觉的配色：
*   **电路与元件**：电容极板、电感线圈使用深灰色或黑色，保持中性。
*   **电场相关**：**紫色系**。正电荷用“洋红/粉红”，负电荷用“深蓝”，电场线、电场能柱状图使用“蓝紫色”。（紫色常与电压、电场关联）
*   **磁场相关**：**绿色系**。磁场线、磁场能柱状图使用“蓝绿色”或“翠绿色”。（绿色常与电感、磁场关联）
*   **电流与运动**：电流流动的光点或箭头使用醒目的**亮黄色或橙色**，表示能量的流动和活跃性。
*   **曲线图**：`q-t` 曲线用**蓝色**，`i-t` 曲线用**红色**，总能量线用**灰色虚线**，电场能曲线用紫色，磁场能曲线用绿色。便于区分和对比。
*   **背景**：使用浅灰色或极浅的渐变背景，确保所有元素清晰可辨。

#### 交互功能列表
1.  **动画控制**：
    *   播放 / 暂停 / 重置按钮。
    *   动画速度调节滑块。
2.  **电路参数调节**：
    *   电感 `L` 调节滑块（例如：0.1H - 5.0H）。
    *   电容 `C` 调节滑块（例如：10μF - 500μF）。
    *   调节后，周期 `T` 的计算值实时显示。
3.  **可视化图层控制**（复选框）：
    *   [显示/隐藏] 电场线与电荷。
    *   [显示/隐藏] 磁场线。
    *   [显示/隐藏] 流动电荷（电流）。
    *   [显示/隐藏] 能量柱状图/饼图。
    *   [显示/隐藏] 右侧波形图。
4.  **阶段提示与高亮**：
    *   动画循环时，在关键相位（如“电场能最大”、“电流最大”）自动弹出文字提示。
    *   鼠标悬停在电路元件、能量条或曲线上时，显示当前瞬时数值（如 `q=...`, `i=...`, `能量=...`）。
5.  **初始状态设置**（可选高级功能）：
    *   预设初始电荷量 `q0` 的滑块，模拟从不同能量状态开始的振荡。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>电磁振荡与LC回路 - 电场能与磁场能相互转化</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%);
            color: #333;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        header {
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            border-left: 5px solid #8a2be2;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .panel {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            flex: 1;
            min-width: 300px;
        }
        
        .panel-title {
            font-size: 1.4rem;
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid #eee;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .panel-title i {
            font-style: normal;
            background: #8a2be2;
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
        
        #simulationPanel {
            flex: 2;
            min-width: 500px;
        }
        
        #controlPanel {
            flex: 1;
            min-width: 300px;
        }
        
        #graphPanel {
            flex: 2;
            min-width: 500px;
        }
        
        #energyPanel {
            flex: 1;
            min-width: 300px;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 400px;
            background: #f8f9fa;
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid #e0e0e0;
        }
        
        canvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .control-group {
            margin-bottom: 20px;
        }
        
        .control-title {
            font-weight: 600;
            margin-bottom: 10px;
            color: #444;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 10px;
        }
        
        .slider-label {
            min-width: 80px;
            font-weight: 500;
        }
        
        .slider-value {
            min-width: 60px;
            text-align: right;
            font-weight: 600;
            color: #8a2be2;
        }
        
        input[type="range"] {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            background: #e0e0e0;
            border-radius: 4px;
            outline: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #8a2be2;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        .button-group {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }
        
        button {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
            font-size: 1rem;
        }
        
        #playBtn {
            background: #2ecc71;
            color: white;
        }
        
        #playBtn:hover {
            background: #27ae60;
        }
        
        #resetBtn {
            background: #e74c3c;
            color: white;
        }
        
        #resetBtn:hover {
            background: #c0392b;
        }
        
        #speedSlider {
            margin-top: 5px;
        }
        
        .checkbox-group {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-top: 10px;
        }
        
        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .checkbox-item input {
            width: 18px;
            height: 18px;
            cursor: pointer;
        }
        
        .checkbox-item label {
            cursor: pointer;
            user-select: none;
        }
        
        .phase-indicator {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 10px;
            margin-top: 15px;
            border-left: 4px solid #3498db;
        }
        
        .phase-title {
            font-weight: 600;
            color: #3498db;
            margin-bottom: 5px;
        }
        
        .phase-desc {
            font-size: 0.95rem;
            color: #555;
        }
        
        .value-display {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-top: 15px;
        }
        
        .value-item {
            background: #f8f9fa;
            padding: 12px;
            border-radius: 8px;
            text-align: center;
        }
        
        .value-label {
            font-size: 0.9rem;
            color: #777;
            margin-bottom: 5px;
        }
        
        .value-number {
            font-size: 1.3rem;
            font-weight: 700;
            font-family: 'Courier New', monospace;
        }
        
        #qValue {
            color: #2980b9;
        }
        
        #iValue {
            color: #e74c3c;
        }
        
        #energyValue {
            color: #2ecc71;
        }
        
        #periodValue {
            color: #9b59b6;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #eee;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
        }
        
        .legend-color {
            width: 15px;
            height: 15px;
            border-radius: 3px;
        }
        
        .legend-electric {
            background: #8a2be2;
        }
        
        .legend-magnetic {
            background: #2ecc71;
        }
        
        .legend-current {
            background: #ffa500;
        }
        
        .legend-charge-plus {
            background: #ff6b8b;
        }
        
        .legend-charge-minus {
            background: #3498db;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: #7f8c8d;
            font-size: 0.9rem;
            margin-top: 20px;
        }
        
        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
            
            .panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>电磁振荡与LC回路</h1>
            <p class="subtitle">电场能与磁场能相互转化动态模拟 | 理想无阻尼振荡 | 周期公式 T = 2π√LC</p>
        </header>
        
        <div class="main-content">
            <div class="panel" id="simulationPanel">
                <div class="panel-title"><i>1</i> LC回路动态模拟</div>
                <div class="canvas-container">
                    <canvas id="simulationCanvas"></canvas>
                </div>
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color legend-electric"></div>
                        <span>电场/电场能</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color legend-magnetic"></div>
                        <span>磁场/磁场能</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color legend-current"></div>
                        <span>电流方向</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color legend-charge-plus"></div>
                        <span>正电荷</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color legend-charge-minus"></div>
                        <span>负电荷</span>
                    </div>
                </div>
            </div>
            
            <div class="panel" id="controlPanel">
                <div class="panel-title"><i>2</i> 控制面板</div>
                
                <div class="control-group">
                    <div class="control-title">
                        <span>动画控制</span>
                    </div>
                    <div class="button-group">
                        <button id="playBtn">暂停</button>
                        <button id="resetBtn">重置</button>
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">动画速度</div>
                        <input type="range" id="speedSlider" min="0.1" max="3" step="0.1" value="1">
                        <div class="slider-value" id="speedValue">1.0x</div>
                    </div>
                </div>
                
                <div class="control-group">
                    <div class="control-title">
                        <span>电路参数调节</span>
                        <span id="periodDisplay">T = 0.00s</span>
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">电感 L</div>
                        <input type="range" id="lSlider" min="0.1" max="5" step="0.1" value="1">
                        <div class="slider-value" id="lValue">1.0 H</div>
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">电容 C</div>
                        <input type="range" id="cSlider" min="10" max="500" step="10" value="100">
                        <div class="slider-value" id="cValue">100 μF</div>
                    </div>
                </div>
                
                <div class="control-group">
                    <div class="control-title">
                        <span>可视化选项</span>
                    </div>
                    <div class="checkbox-group">
                        <div class="checkbox-item">
                            <input type="checkbox" id="showFieldLines" checked>
                            <label for="showFieldLines">电场线/磁场线</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showCurrent" checked>
                            <label for="showCurrent">电流方向</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showCharges" checked>
                            <label for="showCharges">电荷显示</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showEnergyFlow" checked>
                            <label for="showEnergyFlow">能量流动</label>
                        </div>
                    </div>
                </div>
                
                <div class="phase-indicator">
                    <div class="phase-title" id="phaseTitle">电场能最大阶段</div>
                    <div class="phase-desc" id="phaseDesc">电容器充满电，电流为零，能量全部储存在电场中。</div>
                </div>
            </div>
            
            <div class="panel" id="graphPanel">
                <div class="panel-title"><i>3</i> 变量随时间变化曲线</div>
                <div class="canvas-container">
                    <canvas id="graphCanvas"></canvas>
                </div>
            </div>
            
            <div class="panel" id="energyPanel">
                <div class="panel-title"><i>4</i> 能量转化与实时数据</div>
                
                <div class="canvas-container">
                    <canvas id="energyCanvas"></canvas>
                </div>
                
                <div class="value-display">
                    <div class="value-item">
                        <div class="value-label">电荷量 q</div>
                        <div class="value-number" id="qValue">+1.00 C</div>
                    </div>
                    <div class="value-item">
                        <div class="value-label">电流 i</div>
                        <div class="value-number" id="iValue">0.00 A</div>
                    </div>
                    <div class="value-item">
                        <div class="value-label">总能量</div>
                        <div class="value-number" id="energyValue">5.00 J</div>
                    </div>
                    <div class="value-item">
                        <div class="value-label">振荡周期</div>
                        <div class="value-number" id="periodValue">0.063 s</div>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>电磁振荡教学动画 | 理想LC回路 | 能量守恒：电场能 + 磁场能 = 常量</p>
            <p>交互提示：调节电感和电容可以改变振荡频率，观察各物理量的相位关系</p>
        </footer>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const simCanvas = document.getElementById('simulationCanvas');
        const graphCanvas = document.getElementById('graphCanvas');
        const energyCanvas = document.getElementById('energyCanvas');
        
        const simCtx = simCanvas.getContext('2d');
        const graphCtx = graphCanvas.getContext('2d');
        const energyCtx = energyCanvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvases() {
            const containers = document.querySelectorAll('.canvas-container');
            
            containers.forEach(container => {
                const canvas = container.querySelector('canvas');
                const rect = container.getBoundingClientRect();
                
                canvas.width = rect.width;
                canvas.height = rect.height;
            });
        }
        
        // 初始调整尺寸
        resizeCanvases();
        window.addEventListener('resize', resizeCanvases);
        
        // 物理参数
        let L = 1.0; // 电感 (H)
        let C = 100e-6; // 电容 (F) - 100μF
        let q0 = 1.0; // 初始电荷 (C)
        let i0 = 0.0; // 初始电流 (A)
        
        // 计算振荡参数
        const omega = () => 1 / Math.sqrt(L * C); // 角频率
        const period = () => 2 * Math.PI * Math.sqrt(L * C); // 周期
        
        // 动画状态
        let time = 0;
        let isPlaying = true;
        let speed = 1.0;
        let animationId = null;
        
        // 获取DOM元素
        const playBtn = document.getElementById('playBtn');
        const resetBtn = document.getElementById('resetBtn');
        const speedSlider = document.getElementById('speedSlider');
        const speedValue = document.getElementById('speedValue');
        const lSlider = document.getElementById('lSlider');
        const lValue = document.getElementById('lValue');
        const cSlider = document.getElementById('cSlider');
        const cValue = document.getElementById('cValue');
        const periodDisplay = document.getElementById('periodDisplay');
        const periodValue = document.getElementById('periodValue');
        
        const showFieldLines = document.getElementById('showFieldLines');
        const showCurrent = document.getElementById('showCurrent');
        const showCharges = document.getElementById('showCharges');
        const showEnergyFlow = document.getElementById('showEnergyFlow');
        
        const phaseTitle = document.getElementById('phaseTitle');
        const phaseDesc = document.getElementById('phaseDesc');
        
        const qValue = document.getElementById('qValue');
        const iValue = document.getElementById('iValue');
        const energyValue = document.getElementById('energyValue');
        
        // 初始化UI
        function updateUI() {
            lValue.textContent = `${L.toFixed(1)} H`;
            cValue.textContent = `${(C * 1e6).toFixed(0)} μF`;
            speedValue.textContent = `${speed.toFixed(1)}x`;
            
            const T = period();
            periodDisplay.textContent = `T = ${T.toFixed(3)}s`;
            periodValue.textContent = `${T.toFixed(3)} s`;
        }
        
        // 计算当前时刻的物理量
        function calculatePhysics(t) {
            const w = omega();
            const q = q0 * Math.cos(w * t); // 电荷量
            const i = -q0 * w * Math.sin(w * t); // 电流 (i = dq/dt)
            
            // 能量计算
            const Ue = 0.5 * q * q / C; // 电场能
            const Ub = 0.5 * L * i * i; // 磁场能
            const totalEnergy = Ue + Ub; // 总能量
            
            return { q, i, Ue, Ub, totalEnergy, w };
        }
        
        // 绘制LC回路模拟
        function drawSimulation() {
            const width = simCanvas.width;
            const height = simCanvas.height;
            
            // 清空画布
            simCtx.clearRect(0, 0, width, height);
            
            // 计算当前物理量
            const physics = calculatePhysics(time);
            const { q, i, Ue, Ub } = physics;
            
            // 确定相位
            const phase = (physics.w * time) % (2 * Math.PI);
            updatePhaseIndicator(phase);
            
            // 绘制背景
            simCtx.fillStyle = '#f8f9fa';
            simCtx.fillRect(0, 0, width, height);
            
            // 电路布局参数
            const centerX = width / 2;
            const centerY = height / 2;
            const capacitorWidth = 80;
            const capacitorHeight = 120;
            const coilRadius = 40;
            const coilTurns = 6;
            const wireLength = 150;
            
            // 绘制导线
            simCtx.beginPath();
            simCtx.moveTo(centerX - wireLength, centerY);
            simCtx.lineTo(centerX - capacitorWidth/2, centerY);
            simCtx.moveTo(centerX + capacitorWidth/2, centerY);
            
            // 绘制电感线圈
            for (let j = 0; j < coilTurns; j++) {
                const angle = j * (Math.PI / (coilTurns-1));
                const x = centerX + capacitorWidth/2 + 20 + j * 15;
                const y = centerY + coilRadius * Math.sin(angle);
                if (j === 0) {
                    simCtx.lineTo(x, y);
                } else {
                    simCtx.lineTo(x, y);
                }
            }
            
            simCtx.lineTo(centerX + wireLength, centerY);
            simCtx.strokeStyle = '#333';
            simCtx.lineWidth = 3;
            simCtx.stroke();
            
            // 绘制电容
            const capacitorLeft = centerX - capacitorWidth/2;
            const capacitorRight = centerX + capacitorWidth/2;
            const capacitorTop = centerY - capacitorHeight/2;
            const capacitorBottom = centerY + capacitorHeight/2;
            
            // 电容极板
            simCtx.fillStyle = '#444';
            simCtx.fillRect(capacitorLeft - 5, capacitorTop, 10, capacitorHeight);
            simCtx.fillRect(capacitorRight - 5, capacitorTop, 10, capacitorHeight);
            
            // 电荷显示
            if (showCharges.checked) {
                const maxChargeDots = 20;
                const chargeDots = Math.min(maxChargeDots, Math.abs(q) * 10);
                
                // 正电荷
                if (q > 0) {
                    simCtx.fillStyle = '#ff6b8b'; // 粉色表示正电荷
                    for (let j = 0; j < chargeDots; j++) {
                        const x = capacitorLeft - 10;
                        const y = capacitorTop + (j + 0.5) * (capacitorHeight / chargeDots);
                        simCtx.beginPath();
                        simCtx.arc(x, y, 4, 0, Math.PI * 2);
                        simCtx.fill();
                        simCtx.fillText('+', x - 3, y + 3);
                    }
                    
                    simCtx.fillStyle = '#3498db'; // 蓝色表示负电荷
                    for (let j = 0; j < chargeDots; j++) {
                        const x = capacitorRight + 10;
                        const y = capacitorTop + (j + 0.5) * (capacitorHeight / chargeDots);
                        simCtx.beginPath();
                        simCtx.arc(x, y, 4, 0, Math.PI * 2);
                        simCtx.fill();
                        simCtx.fillText('-', x - 3, y + 3);
                    }
                } else {
                    simCtx.fillStyle = '#3498db'; // 蓝色表示负电荷
                    for (let j = 0; j < chargeDots; j++) {
                        const x = capacitorLeft - 10;
                        const y = capacitorTop + (j + 0.5) * (capacitorHeight / chargeDots);
                        simCtx.beginPath();
                        simCtx.arc(x, y, 4, 0, Math.PI * 2);
                        simCtx.fill();
                        simCtx.fillText('-', x - 3, y + 3);
                    }
                    
                    simCtx.fillStyle = '#ff6b8b'; // 粉色表示正电荷
                    for (let j = 0; j < chargeDots; j++) {
                        const x = capacitorRight + 10;
                        const y = capacitorTop + (j + 0.5) * (capacitorHeight / chargeDots);
                        simCtx.beginPath();
                        simCtx.arc(x, y, 4, 0, Math.PI * 2);
                        simCtx.fill();
                        simCtx.fillText('+', x - 3, y + 3);
                    }
                }
            }
            
            // 电场线
            if (showFieldLines.checked) {
                const fieldLineCount = 12;
                const fieldStrength = Math.abs(q) / q0;
                
                simCtx.strokeStyle = 'rgba(138, 43, 226, 0.6)'; // 紫色电场线
                simCtx.lineWidth = 1 + fieldStrength * 2;
                
                for (let j = 0; j < fieldLineCount; j++) {
                    const y = capacitorTop + (j + 0.5) * (capacitorHeight / fieldLineCount);
                    
                    simCtx.beginPath();
                    simCtx.moveTo(capacitorLeft, y);
                    simCtx.bezierCurveTo(
                        centerX - capacitorWidth/4, y,
                        centerX + capacitorWidth/4, y,
                        capacitorRight, y
                    );
                    simCtx.stroke();
                    
                    // 电场方向箭头
                    if (q > 0) {
                        drawArrow(simCtx, centerX, y, 8, Math.PI, '#8a2be2');
                    } else {
                        drawArrow(simCtx, centerX, y, 8, 0, '#8a2be2');
                    }
                }
            }
            
            // 电流方向
            if (showCurrent.checked) {
                const currentStrength = Math.abs(i) / (q0 * physics.w);
                const arrowCount = 8;
                const arrowSpacing = (2 * wireLength - capacitorWidth - 40) / arrowCount;
                
                simCtx.fillStyle = 'rgba(255, 165, 0, 0.8)'; // 橙色电流
                
                for (let j = 0; j < arrowCount; j++) {
                    const x = centerX - wireLength + 30 + j * arrowSpacing;
                    
                    // 跳过电容区域
                    if (x > capacitorLeft - 20 && x < capacitorRight + 20) continue;
                    
                    if (i > 0) {
                        drawArrow(simCtx, x, centerY, 10 + currentStrength * 10, Math.PI/2, '#ffa500');
                    } else {
                        drawArrow(simCtx, x, centerY, 10 + currentStrength * 10, -Math.PI/2, '#ffa500');
                    }
                }
            }
            
            // 磁场线（电感周围）
            if (showFieldLines.checked) {
                const magneticStrength = Math.abs(i) / (q0 * physics.w);
                const magneticLines = 8;
                
                simCtx.strokeStyle = 'rgba(46, 204, 113, 0.6)'; // 绿色磁场线
                simCtx.lineWidth = 1 + magneticStrength * 2;
                
                const coilCenterX = centerX + capacitorWidth/2 + 20 + (coilTurns-1) * 15 / 2;
                
                for (let j = 0; j < magneticLines; j++) {
                    const angle = j * (2 * Math.PI / magneticLines);
                    const radius = coilRadius + 15;
                    
                    simCtx.beginPath();
                    simCtx.arc(coilCenterX, centerY, radius, angle, angle + Math.PI * 1.8);
                    simCtx.stroke();
                    
                    // 磁场方向
                    const arrowAngle = angle + Math.PI * 0.9;
                    const arrowX = coilCenterX + radius * Math.cos(arrowAngle);
                    const arrowY = centerY + radius * Math.sin(arrowAngle);
                    
                    if (i > 0) {
                        drawArrow(simCtx, arrowX, arrowY, 6, arrowAngle + Math.PI/2, '#2ecc71');
                    } else {
                        drawArrow(simCtx, arrowX, arrowY, 6, arrowAngle - Math.PI/2, '#2ecc71');
                    }
                }
            }
            
            // 能量流动指示
            if (showEnergyFlow.checked) {
                const energyFlowRadius = 15;
                const flowX = centerX;
                const flowY = centerY + capacitorHeight/2 + 30;
                
                simCtx.beginPath();
                simCtx.arc(flowX, flowY, energyFlowRadius, 0, Math.PI * 2);
                simCtx.strokeStyle = '#9b59b6';
                simCtx.lineWidth = 2;
                simCtx.stroke();
                
                // 流动方向
                if (Math.abs(Ub) > Math.abs(Ue)) {
                    // 磁场能 > 电场能，能量流向电容
                    drawArrow(simCtx, flowX, flowY, 12, Math.PI, '#9b59b6');
                    simCtx.fillText('能量流向电容', flowX - 40, flowY - 25);
                } else {
                    // 电场能 > 磁场能，能量流向电感
                    drawArrow(simCtx, flowX, flowY, 12, 0, '#9b59b6');
                    simCtx.fillText('能量流向电感', flowX - 40, flowY - 25);
                }
            }
            
            // 标签
            simCtx.fillStyle = '#333';
            simCtx.font = 'bold 16px Arial';
            simCtx.fillText('C', centerX, capacitorTop - 10);
            simCtx.fillText('L', centerX + capacitorWidth/2 + 50, centerY - coilRadius - 10);
            
            // 更新数据显示
            qValue.textContent = `${physics.q.toFixed(2)} C`;
            iValue.textContent = `${physics.i.toFixed(2)} A`;
            energyValue.textContent = `${physics.totalEnergy.toFixed(2)} J`;
        }
        
        // 绘制曲线图
        function drawGraph() {
            const width = graphCanvas.width;
            const height = graphCanvas.height;
            
            // 清空画布
            graphCtx.clearRect(0, 0, width, height);
            
            // 绘制背景
            graphCtx.fillStyle = '#f8f9fa';
            graphCtx.fillRect(0, 0, width, height);
            
            // 绘制坐标轴
            graphCtx.strokeStyle = '#aaa';
            graphCtx.lineWidth = 1;
            
            // X轴
            graphCtx.beginPath();
            graphCtx.moveTo(50, height - 50);
            graphCtx.lineTo(width - 20, height - 50);
            graphCtx.stroke();
            
            // Y轴
            graphCtx.beginPath();
            graphCtx.moveTo(50, 20);
            graphCtx.lineTo(50, height - 50);
            graphCtx.stroke();
            
            // 坐标轴标签
            graphCtx.fillStyle = '#666';
            graphCtx.font = '14px Arial';
            graphCtx.fillText('时间 t (s)', width - 80, height - 20);
            graphCtx.save();
            graphCtx.translate(15, height / 2);
            graphCtx.rotate(-Math.PI / 2);
            graphCtx.fillText('物理量', 0, 0);
            graphCtx.restore();
            
            // 绘制网格
            graphCtx.strokeStyle = '#eee';
            graphCtx.lineWidth = 0.5;
            
            // 水平网格
            for (let i = 0; i <= 10; i++) {
                const y = 20 + (height - 70) * i / 10;
                graphCtx.beginPath();
                graphCtx.moveTo(50, y);
                graphCtx.lineTo(width - 20, y);
                graphCtx.stroke();
            }
            
            // 垂直网格
            const timeRange = 2 * period();
            for (let i = 0; i <= 10; i++) {
                const x = 50 + (width - 70) * i / 10;
                graphCtx.beginPath();
                graphCtx.moveTo(x, 20);
                graphCtx.lineTo(x, height - 50);
                graphCtx.stroke();
                
                // 时间刻度
                const t = (i / 10) * timeRange;
                graphCtx.fillStyle = '#666';
                graphCtx.fillText(t.toFixed(2), x - 10, height - 30);
            }
            
            // 绘制曲线
            const timeRangeSeconds = 2 * period();
            const points = 200;
            const dx = (width - 70) / points;
            
            // 电荷曲线 (蓝色)
            graphCtx.beginPath();
            for (let i = 0; i <= points; i++) {
                const t = (i / points) * timeRangeSeconds;
                const physics = calculatePhysics(t);
                const x = 50 + (i / points) * (width - 70);
                const y = height/2 - (physics.q / q0) * (height - 70) / 3;
                
                if (i === 0) {
                    graphCtx.moveTo(x, y);
                } else {
                    graphCtx.lineTo(x, y);
                }
            }
            graphCtx.strokeStyle = '#2980b9';
            graphCtx.lineWidth = 2;
            graphCtx.stroke();
            
            // 电流曲线 (红色)
            graphCtx.beginPath();
            for (let i = 0; i <= points; i++) {
                const t = (i / points) * timeRangeSeconds;
                const physics = calculatePhysics(t);
                const x = 50 + (i / points) * (width - 70);
                const y = height/2 - (physics.i / (q0 * omega())) * (height - 70) / 3;
                
                if (i === 0) {
                    graphCtx.moveTo(x, y);
                } else {
                    graphCtx.lineTo(x, y);
                }
            }
            graphCtx.strokeStyle = '#e74c3c';
            graphCtx.lineWidth = 2;
            graphCtx.stroke();
            
            // 能量曲线
            graphCtx.beginPath();
            for (let i = 0; i <= points; i++) {
                const t = (i / points) * timeRangeSeconds;
                const physics = calculatePhysics(t);
                const x = 50 + (i / points) * (width - 70);
                const y = height - 50 - (physics.Ue / (0.5 * q0 * q0 / C)) * (height - 70) / 2;
                
                if (i === 0) {
                    graphCtx.moveTo(x, y);
                } else {
                    graphCtx.lineTo(x, y);
                }
            }
            graphCtx.strokeStyle = '#8a2be2';
            graphCtx.lineWidth = 2;
            graphCtx.stroke();
            
            graphCtx.beginPath();
            for (let i = 0; i <= points; i++) {
                const t = (i / points) * timeRangeSeconds;
                const physics = calculatePhysics(t);
                const x = 50 + (i / points) * (width - 70);
                const y = height - 50 - (physics.Ub / (0.5 * q0 * q0 / C)) * (height - 70) / 2;
                
                if (i === 0) {
                    graphCtx.moveTo(x, y);
                } else {
                    graphCtx.lineTo(x, y);
                }
            }
            graphCtx.strokeStyle = '#2ecc71';
            graphCtx.lineWidth = 2;
            graphCtx.stroke();
            
            // 当前时间指示线
            const currentX = 50 + (time % timeRangeSeconds) / timeRangeSeconds * (width - 70);
            graphCtx.beginPath();
            graphCtx.moveTo(currentX, 20);
            graphCtx.lineTo(currentX, height - 50);
            graphCtx.strokeStyle = '#e67e22';
            graphCtx.lineWidth = 2;
            graphCtx.stroke();
            
            // 图例
            const legendY = 30;
            const legendItems
<!--检测到代码截断，自动续写中...-->
= [
                {color: '#2980b9', label: '电荷 q(t)'},
                {color: '#e74c3c', label: '电流 i(t)'},
                {color: '#8a2be2', label: '电场能 Ue(t)'},
                {color: '#2ecc71', label: '磁场能 Ub(t)'}
            ];
            
            legendItems.forEach((item, index) => {
                const y = legendY + index * 25;
                
                graphCtx.fillStyle = item.color;
                graphCtx.fillRect(width - 150, y, 15, 15);
                
                graphCtx.fillStyle = '#333';
                graphCtx.font = '12px Arial';
                graphCtx.fillText(item.label, width - 130, y + 12);
            });
        }
        
        // 绘制能量图
        function drawEnergy() {
            const width = energyCanvas.width;
            const height = energyCanvas.height;
            
            // 清空画布
            energyCtx.clearRect(0, 0, width, height);
            
            // 计算当前物理量
            const physics = calculatePhysics(time);
            const { Ue, Ub, totalEnergy } = physics;
            
            // 绘制能量柱状图
            const barWidth = 60;
            const maxBarHeight = height - 100;
            
            // 电场能柱
            const electricHeight = (Ue / totalEnergy) * maxBarHeight;
            energyCtx.fillStyle = '#8a2be2';
            energyCtx.fillRect(width/2 - barWidth - 20, height - 50 - electricHeight, barWidth, electricHeight);
            
            // 磁场能柱
            const magneticHeight = (Ub / totalEnergy) * maxBarHeight;
            energyCtx.fillStyle = '#2ecc71';
            energyCtx.fillRect(width/2 + 20, height - 50 - magneticHeight, barWidth, magneticHeight);
            
            // 柱状图标签
            energyCtx.fillStyle = '#333';
            energyCtx.font = 'bold 16px Arial';
            energyCtx.fillText('电场能', width/2 - barWidth - 20, height - 20);
            energyCtx.fillText('磁场能', width/2 + 20, height - 20);
            
            // 数值标签
            energyCtx.font = '14px Arial';
            energyCtx.fillStyle = '#8a2be2';
            energyCtx.fillText(`${Ue.toFixed(2)} J`, width/2 - barWidth - 15, height - 60 - electricHeight);
            
            energyCtx.fillStyle = '#2ecc71';
            energyCtx.fillText(`${Ub.toFixed(2)} J`, width/2 + 25, height - 60 - magneticHeight);
            
            // 总能量线
            energyCtx.strokeStyle = '#7f8c8d';
            energyCtx.lineWidth = 2;
            energyCtx.setLineDash([5, 5]);
            energyCtx.beginPath();
            energyCtx.moveTo(30, height - 50 - maxBarHeight);
            energyCtx.lineTo(width - 30, height - 50 - maxBarHeight);
            energyCtx.stroke();
            energyCtx.setLineDash([]);
            
            // 总能量标签
            energyCtx.fillStyle = '#7f8c8d';
            energyCtx.font = 'bold 14px Arial';
            energyCtx.fillText(`总能量: ${totalEnergy.toFixed(2)} J`, width/2 - 50, height - 70 - maxBarHeight);
            
            // 绘制能量转化饼图
            const pieRadius = 60;
            const pieX = width/2;
            const pieY = 80;
            
            // 电场能部分
            const electricAngle = (Ue / totalEnergy) * 2 * Math.PI;
            energyCtx.beginPath();
            energyCtx.moveTo(pieX, pieY);
            energyCtx.arc(pieX, pieY, pieRadius, 0, electricAngle);
            energyCtx.closePath();
            energyCtx.fillStyle = '#8a2be2';
            energyCtx.fill();
            
            // 磁场能部分
            energyCtx.beginPath();
            energyCtx.moveTo(pieX, pieY);
            energyCtx.arc(pieX, pieY, pieRadius, electricAngle, 2 * Math.PI);
            energyCtx.closePath();
            energyCtx.fillStyle = '#2ecc71';
            energyCtx.fill();
            
            // 饼图边框
            energyCtx.beginPath();
            energyCtx.arc(pieX, pieY, pieRadius, 0, 2 * Math.PI);
            energyCtx.strokeStyle = '#333';
            energyCtx.lineWidth = 2;
            energyCtx.stroke();
            
            // 饼图标签
            energyCtx.fillStyle = '#333';
            energyCtx.font = 'bold 14px Arial';
            energyCtx.fillText('能量分布', pieX - 35, pieY + pieRadius + 30);
            
            // 百分比
            const electricPercent = Math.round((Ue / totalEnergy) * 100);
            const magneticPercent = Math.round((Ub / totalEnergy) * 100);
            
            energyCtx.font = '12px Arial';
            energyCtx.fillStyle = '#8a2be2';
            energyCtx.fillText(`${electricPercent}%`, pieX - 40, pieY - 10);
            
            energyCtx.fillStyle = '#2ecc71';
            energyCtx.fillText(`${magneticPercent}%`, pieX + 20, pieY + 20);
        }
        
        // 绘制箭头函数
        function drawArrow(ctx, x, y, size, angle, color) {
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(angle);
            ctx.fillStyle = color;
            
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(-size, -size/2);
            ctx.lineTo(-size, size/2);
            ctx.closePath();
            ctx.fill();
            
            ctx.restore();
        }
        
        // 更新相位指示器
        function updatePhaseIndicator(phase) {
            const normalizedPhase = (phase + 2 * Math.PI) % (2 * Math.PI);
            
            if (normalizedPhase < Math.PI/4 || normalizedPhase > 7*Math.PI/4) {
                phaseTitle.textContent = '电场能最大阶段';
                phaseDesc.textContent = '电容器充满电，电流为零，能量全部储存在电场中。';
            } else if (normalizedPhase >= Math.PI/4 && normalizedPhase < 3*Math.PI/4) {
                phaseTitle.textContent = '能量转化阶段 (电场→磁场)';
                phaseDesc.textContent = '电容器放电，电流增大，电场能转化为磁场能。';
            } else if (normalizedPhase >= 3*Math.PI/4 && normalizedPhase < 5*Math.PI/4) {
                phaseTitle.textContent = '磁场能最大阶段';
                phaseDesc.textContent = '电容器电量为零，电流最大，能量全部储存在磁场中。';
            } else {
                phaseTitle.textContent = '能量转化阶段 (磁场→电场)';
                phaseDesc.textContent = '电容器反向充电，电流减小，磁场能转化为电场能。';
            }
        }
        
        // 动画循环
        function animate() {
            if (isPlaying) {
                time += 0.016 * speed; // 每帧增加的时间，乘以速度因子
            }
            
            drawSimulation();
            drawGraph();
            drawEnergy();
            
            animationId = requestAnimationFrame(animate);
        }
        
        // 事件监听器
        playBtn.addEventListener('click', () => {
            isPlaying = !isPlaying;
            playBtn.textContent = isPlaying ? '暂停' : '播放';
        });
        
        resetBtn.addEventListener('click', () => {
            time = 0;
            if (!isPlaying) {
                isPlaying = true;
                playBtn.textContent = '暂停';
            }
        });
        
        speedSlider.addEventListener('input', () => {
            speed = parseFloat(speedSlider.value);
            updateUI();
        });
        
        lSlider.addEventListener('input', () => {
            L = parseFloat(lSlider.value);
            updateUI();
        });
        
        cSlider.addEventListener('input', () => {
            C = parseFloat(cSlider.value) * 1e-6; // 转换为法拉
            updateUI();
        });
        
        // 初始化UI
        updateUI();
        
        // 开始动画
        animate();
        
        // 初始绘制
        drawSimulation();
        drawGraph();
        drawEnergy();
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 《电磁振荡与LC回路》交互式教学动画使用指南

欢迎使用这款精心设计的交互式教学动画！本工具旨在通过动态可视化方式，帮助您深入理解电磁振荡的核心原理和LC回路中电场能与磁场能的相互转化过程。无论您是学生、教师还是物理爱好者，都能通过直观的交互体验，掌握这一抽象的物理概念。

---

### 一、功能说明

本动画模拟了一个**理想的无阻尼LC振荡回路**，通过四个联动面板全方位展示电磁振荡过程：

1.  **LC回路动态模拟区**：直观展示电荷运动、电场线、磁场线和电流方向
2.  **控制面板**：调节参数、控制动画、选择可视化选项
3.  **变量曲线图区**：同步显示电荷、电流和能量随时间变化的波形
4.  **能量转化面板**：实时显示能量分布和转化比例的柱状图与饼图

所有面板实时联动，确保您观察到的每个变化都能在其他视图中找到对应的数学和物理表征。

---

### 二、主要功能

#### 1. 动画控制功能
- **播放/暂停**：控制动画运行与停止，便于仔细观察关键瞬间
- **重置**：将动画恢复到初始状态（电容器充满电，电流为零）
- **速度调节**：通过滑块调整动画播放速度（0.1x - 3.0x），适合不同学习节奏

#### 2. 参数调节功能
- **电感L调节**：0.1H - 5.0H，观察电感对振荡周期的影响
- **电容C调节**：10μF - 500μF，观察电容对振荡周期的影响
- **实时周期计算**：根据公式 `T = 2π√LC` 实时显示当前参数下的振荡周期

#### 3. 可视化选项
- **电场线/磁场线**：显示/隐藏电场和磁场的可视化线条
- **电流方向**：显示/指示电流流动方向的橙色箭头
- **电荷显示**：显示/隐藏电容器极板上的正负电荷符号
- **能量流动**：显示/隐藏能量在电容和电感之间流动的指示

#### 4. 实时数据显示
- 电荷量 `q`、电流 `i`、总能量的瞬时数值
- 当前振荡周期的计算值
- 相位状态提示（电场能最大、磁场能最大等四个关键阶段）

---

### 三、设计特色

#### 1. 多表征联动设计
- **物理过程**（电荷运动、场线变化）
- **电路模型**（电容、电感、导线）
- **数学表征**（正弦波形、相位关系）
- **能量视角**（柱状图、饼图比例）

四个视角同步更新，帮助您建立完整的物理图景。

#### 2. 直观的视觉编码
- **紫色系**（电场相关）：电场线、电场能、正电荷
- **绿色系**（磁场相关）：磁场线、磁场能
- **橙色**（电流）：流动方向和强度
- **蓝色/红色曲线**：电荷与电流的相位差可视化

#### 3. 认知友好的交互
- 从具体（电荷运动）到抽象（数学曲线）的渐进展示
- 关键相位自动提示，强化概念理解
- 可调节的信息密度，避免认知过载

---

### 四、教学要点

#### 核心概念强化
1. **能量守恒**：观察总能量（电场能+磁场能）始终保持不变，理解能量在两种形式间的周期性转化
2. **相位关系**：注意电荷 `q` 与电流 `i` 存在90°相位差
   - 当 `q` 最大时（电场能最大），`i` = 0（磁场能为零）
   - 当 `i` 最大时（磁场能最大），`q` = 0（电场能为零）
3. **决定因素**：通过调节L和C，验证振荡周期公式 `T = 2π√LC`

#### 观察重点
- **电场能最大时**：电容器极板电荷最多，电场线最密集，电流为零
- **磁场能最大时**：电感周围磁场线最密集，电容器电量为零，电流最大
- **能量转化过程**：注意能量流动方向与电流方向的关系

---

### 五、使用建议

#### 对于学生
1. **初次接触**：先使用默认参数，打开所有可视化选项，完整观看几个振荡周期
2. **分步学习**：
   - 第一步：只关注电荷运动和电流方向
   - 第二步：加入电场线和磁场线观察
   - 第三步：观察能量柱状图和波形图的关系
3. **探究学习**：
   - 固定C，改变L：观察周期如何变化
   - 固定L，改变C：观察周期如何变化
   - 验证 `T ∝ √L` 和 `T ∝ √C` 的关系

#### 对于教师
1. **课堂演示**：
   - 使用投影展示，逐步揭示不同可视化层
   - 在关键相位暂停，引导学生观察和讨论
   - 通过参数调节，让学生预测周期变化
2. **探究任务设计**：
   - 任务1：找出电场能最大的两个时刻，测量时间间隔，验证与计算周期是否一致
   - 任务2：调节L和C使周期加倍，记录多组数据，归纳规律
   - 任务3：解释为什么电流最大时电容器电量为零

#### 最佳实践流程
1. **观察现象**：播放完整动画，建立直观感受
2. **分析关系**：暂停在关键相位，分析各物理量关系
3. **探究规律**：调节参数，观察周期变化规律
4. **数学验证**：对比波形图与理论公式预测
5. **总结提升**：关闭部分可视化，尝试在心中构建完整物理图像

---

### 温馨提示

- 本动画基于**理想无阻尼模型**，实际LC回路存在电阻，振荡会逐渐衰减
- 动画中的“电荷”是宏观模型，实际是电子的定向移动
- 电场线和磁场线是人为引入的直观表示工具，帮助理解场的分布

希望这款交互式动画能成为您学习电磁振荡的得力助手！通过动手调节、仔细观察，您将不仅记住公式，更能真正理解电场能与磁场能相互转化的美妙舞蹈。

**探索的乐趣在于发现，理解的深度源于互动。祝您学习愉快！**

---
*动画设计：教育技术专家团队 | 物理原理：经典电磁学 | 交互设计：基于认知科学的最佳实践*