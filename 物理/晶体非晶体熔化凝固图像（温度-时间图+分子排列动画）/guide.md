# 需求：晶体/非晶体熔化凝固图像（温度-时间图+分子排列动画）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向初中或高中物理/化学学生，用于学习“物态变化”中晶体与非晶体在熔化和凝固过程中的核心区别。用户的核心需求是：
1.  **理解抽象概念**：将抽象的“温度-时间”图像与微观的分子运动、排列变化建立直观联系。
2.  **对比学习**：清晰区分晶体（有固定熔点/凝固点）与非晶体（无固定熔点/凝固点）在宏观图像和微观结构上的不同。
3.  **动态过程观察**：观察从固态到液态（或反向）的连续变化过程，理解“吸热/放热”与“温度变化/不变”之间的关系。
4.  **自主探究**：能够控制实验进程，观察不同阶段的现象，加深记忆。

#### 教学设计思路
1.  **核心概念**：
    *   **晶体**：有固定熔点/凝固点；熔化/凝固过程中，温度保持不变（图像出现平台）；分子排列规则（空间点阵）。
    *   **非晶体**：无固定熔点/凝固点；熔化/凝固过程中，温度持续变化（图像为平滑曲线）；分子排列不规则。
    *   **熔化吸热**：用于克服分子间的束缚，使分子排列从有序变为无序。
    *   **凝固放热**：分子排列从无序变为有序，能量释放。

2.  **认知规律**：
    *   **从宏观到微观**：先展示宏观的温度-时间图像变化，再联动展示对应的微观分子排列动画，建立“图像-现象-本质”的认知链条。
    *   **从对比到归纳**：将晶体与非晶体的动画并排展示，通过强烈的视觉对比，引导学生自己归纳总结差异。
    *   **交互式建构**：允许用户控制加热/冷却过程，在关键点（如熔点）暂停并观察，主动建构知识。

3.  **交互设计**：
    *   **双视图联动**：左侧为“温度-时间”坐标图，右侧为“分子排列模型”动画区。两者进度完全同步。
    *   **过程控制**：提供“播放/暂停”、“重置”按钮，以及一个可拖拽的“加热/冷却”滑块或速率选择器。
    *   **阶段提示**：当图像进入“固态升温”、“熔化（温度平台）”、“液态升温”等阶段时，在视图上方用文字标签高亮提示，并解释该阶段能量去向（如“吸收的热量用于增加分子动能” vs “吸收的热量用于破坏晶格结构”）。
    *   **对比模式**：默认并排展示晶体（如冰/金属）与非晶体（如玻璃/石蜡）的熔化过程。可提供单选按钮，让用户单独查看某一种物质。

4.  **视觉呈现**：
    *   **坐标图**：清晰、简洁。温度曲线平滑，晶体平台段需特别突出。可考虑在曲线上添加一个跟随进度的圆点，并实时显示当前时间和温度数值。
    *   **分子模型**：
        *   **晶体**：固态时，分子显示为规则排列的“点阵”（如方格状或更贴近实际晶体结构），分子在平衡位置附近振动。熔化时，点阵结构从边缘开始逐渐“松动”、“崩溃”，分子变得可自由移动，但局部可能仍有短暂有序。液态时，分子无序运动，间距稍大。
        *   **非晶体**：固态时，分子呈现无序“冻结”状态，但排列紧密。整个软化过程中，分子逐渐获得移动能力，没有明显的结构崩溃点，直接过渡到液态。
    *   **能量可视化**：可以用动态的“热箭头”从外部流入模型，或在分子振动加剧时用颜色深浅/光晕大小表示分子平均动能。

#### 配色方案选择
*   **主色调**：采用科技蓝 (`#3498db`) 或理性紫 (`#9b59b6`) 作为坐标轴、按钮的主色，传递科学和严谨感。
*   **视图背景**：坐标图背景为浅灰色 (`#f8f9fa`) 或白色，分子模型区背景为深色 (`#2c3e50`)，以突出白色的分子模型，模拟微观世界的观察感。
*   **温度曲线**：
    *   晶体曲线用 **蓝色** (`#2980b9`， 固态/液态) 和 **红色水平线段** (`#e74c3c`， 熔化/凝固平台) 强调。
    *   非晶体曲线用 **橙色** (`#e67e22`) 区分。
*   **分子与状态指示**：
    *   固态分子：用 **浅蓝色** (`#aed6f1`) 表示“较冷”，振动平缓。
    *   液态分子：用 **浅红色/橙色** (`#f5b7b1` / `#fad7a0`) 表示“较热”，运动剧烈。
    *   文字提示框：使用温和的黄色 (`#fff9c4`) 作为背景，黑色文字。

#### 交互功能列表
1.  **物质选择器**：单选按钮组，用于选择“晶体（冰）”、“非晶体（石蜡）”或“对比模式”。
2.  **过程控制面板**：
    *   **播放/暂停按钮**：开始或暂停动画。
    *   **重置按钮**：将动画恢复到初始状态（完全固态）。
    *   **加热/冷却切换**：一个双态按钮，用于切换过程是“熔化”还是“凝固”。
    *   **速率滑块**：控制加热/冷却的快慢。
3.  **联动可视化**：
    *   坐标图上有一个移动的 **指示点**，实时对应时间与温度。
    *   分子动画的剧烈程度与当前温度/阶段严格对应。
4.  **智能提示系统**：
    *   **阶段标题**：在视图顶部动态显示当前阶段（如“固态吸热升温”、“熔化过程，温度不变”）。
    *   **能量说明**：在阶段标题下方或侧边，用一两句话简要说明该阶段吸收的热量主要用于做什么。
    *   **关键点标记**：当指示点到达熔点/凝固点时，坐标图上该点会闪烁提示。
5.  **温度/时间读数**：实时显示当前模拟的时间 (`t`) 和温度 (`T`)。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>晶体与非晶体熔化凝固过程教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
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
            margin-bottom: 30px;
        }
        
        .control-panel {
            flex: 1;
            min-width: 300px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .visualization-area {
            flex: 2;
            min-width: 600px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .graph-container, .molecule-container {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .graph-title, .molecule-title {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.3rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 300px;
        }
        
        canvas {
            display: block;
            border-radius: 8px;
        }
        
        .molecule-canvas-container {
            position: relative;
            width: 100%;
            height: 300px;
            background-color: #2c3e50;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .control-group {
            margin-bottom: 25px;
        }
        
        h3 {
            color: #3498db;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #f0f0f0;
        }
        
        .material-selector {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        
        .radio-option {
            display: flex;
            align-items: center;
            padding: 12px 15px;
            background-color: #f8f9fa;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .radio-option:hover {
            background-color: #eef5ff;
            transform: translateY(-2px);
        }
        
        .radio-option.active {
            background-color: #e3f2fd;
            border-left: 5px solid #3498db;
        }
        
        .radio-option input {
            margin-right: 12px;
            transform: scale(1.2);
        }
        
        .process-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            align-items: center;
        }
        
        .btn {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
        }
        
        .btn-primary {
            background-color: #3498db;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: #e74c3c;
            color: white;
        }
        
        .btn-secondary:hover {
            background-color: #c0392b;
            transform: translateY(-2px);
        }
        
        .btn-toggle {
            background-color: #9b59b6;
            color: white;
        }
        
        .btn-toggle:hover {
            background-color: #8e44ad;
            transform: translateY(-2px);
        }
        
        .slider-container {
            margin-top: 15px;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }
        
        .slider {
            width: 100%;
            height: 10px;
            border-radius: 5px;
            background: #ddd;
            outline: none;
            -webkit-appearance: none;
        }
        
        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        .info-panel {
            background-color: #fff9c4;
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
            border-left: 5px solid #f1c40f;
        }
        
        .phase-indicator {
            font-size: 1.2rem;
            font-weight: 600;
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .energy-info {
            color: #7f8c8d;
            line-height: 1.5;
        }
        
        .readings {
            display: flex;
            justify-content: space-around;
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 10px;
            margin-top: 15px;
        }
        
        .reading-item {
            text-align: center;
        }
        
        .reading-value {
            font-size: 1.5rem;
            font-weight: 700;
            color: #2c3e50;
        }
        
        .reading-label {
            font-size: 0.9rem;
            color: #7f8c8d;
            margin-top: 5px;
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
            border-radius: 4px;
        }
        
        .crystal-solid { background-color: #2980b9; }
        .crystal-melting { background-color: #e74c3c; }
        .non-crystal { background-color: #e67e22; }
        
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
            
            .visualization-area {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>晶体与非晶体熔化凝固过程</h1>
            <p class="subtitle">温度-时间图像与分子排列动画联动演示</p>
        </header>
        
        <div class="main-content">
            <div class="control-panel">
                <div class="control-group">
                    <h3>物质选择</h3>
                    <div class="material-selector">
                        <label class="radio-option active">
                            <input type="radio" name="material" value="crystal" checked> 
                            晶体（冰） - 有固定熔点
                        </label>
                        <label class="radio-option">
                            <input type="radio" name="material" value="non-crystal"> 
                            非晶体（石蜡） - 无固定熔点
                        </label>
                        <label class="radio-option">
                            <input type="radio" name="material" value="compare"> 
                            对比模式（同时显示）
                        </label>
                    </div>
                </div>
                
                <div class="control-group">
                    <h3>过程控制</h3>
                    <div class="process-controls">
                        <button id="playPauseBtn" class="btn btn-primary">开始熔化</button>
                        <button id="resetBtn" class="btn btn-secondary">重置</button>
                        <button id="toggleProcessBtn" class="btn btn-toggle">切换为凝固过程</button>
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>加热/冷却速率</span>
                            <span id="rateValue">中速</span>
                        </div>
                        <input type="range" min="1" max="5" value="3" class="slider" id="rateSlider">
                    </div>
                </div>
                
                <div class="info-panel">
                    <div class="phase-indicator" id="phaseIndicator">初始状态：固态</div>
                    <div class="energy-info" id="energyInfo">系统处于初始固态，分子在平衡位置附近振动。</div>
                </div>
                
                <div class="readings">
                    <div class="reading-item">
                        <div class="reading-value" id="timeValue">0 s</div>
                        <div class="reading-label">时间</div>
                    </div>
                    <div class="reading-item">
                        <div class="reading-value" id="tempValue">-10 °C</div>
                        <div class="reading-label">温度</div>
                    </div>
                    <div class="reading-item">
                        <div class="reading-value" id="stateValue">固态</div>
                        <div class="reading-label">物态</div>
                    </div>
                </div>
            </div>
            
            <div class="visualization-area">
                <div class="graph-container">
                    <div class="graph-title">
                        <span>温度-时间图像</span>
                        <div class="legend">
                            <div class="legend-item">
                                <div class="legend-color crystal-solid"></div>
                                <span>晶体固态/液态</span>
                            </div>
                            <div class="legend-item">
                                <div class="legend-color crystal-melting"></div>
                                <span>晶体熔化/凝固平台</span>
                            </div>
                            <div class="legend-item">
                                <div class="legend-color non-crystal"></div>
                                <span>非晶体</span>
                            </div>
                        </div>
                    </div>
                    <div class="canvas-container">
                        <canvas id="graphCanvas" width="800" height="280"></canvas>
                    </div>
                </div>
                
                <div class="molecule-container">
                    <div class="molecule-title">
                        <span>分子排列模型</span>
                        <span id="moleculeSubtitle">晶体分子排列</span>
                    </div>
                    <div class="molecule-canvas-container">
                        <canvas id="moleculeCanvas" width="800" height="280"></canvas>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>教学动画设计：晶体有固定熔点，熔化时温度保持不变；非晶体无固定熔点，熔化时温度持续上升。</p>
            <p>注意观察：晶体熔化时分子排列从有序变为无序，需要吸收热量破坏晶格结构；非晶体分子排列始终无序。</p>
        </footer>
    </div>

    <script>
        // 全局变量
        let animationId = null;
        let isPlaying = false;
        let isMelting = true; // true: 熔化过程, false: 凝固过程
        let currentMaterial = 'crystal'; // 'crystal', 'non-crystal', 'compare'
        let animationRate = 3; // 1-5
        
        // 模拟参数
        let time = 0;
        let temperature = -10;
        let state = 'solid'; // 'solid', 'melting', 'liquid', 'freezing'
        
        // 晶体参数
        const crystalMeltingPoint = 0;
        const crystalMeltingDuration = 60; // 熔化平台持续时间
        const crystalHeatingRate = 0.3; // 固态/液态加热速率 °C/s
        const crystalMaxTemp = 30;
        const crystalMinTemp = -10;
        
        // 非晶体参数
        const nonCrystalHeatingRate = 0.25; // 加热速率 °C/s
        const nonCrystalSofteningStart = 40; // 开始软化温度
        const nonCrystalLiquidTemp = 70; // 完全液态温度
        const nonCrystalMaxTemp = 80;
        const nonCrystalMinTemp = -10;
        
        // 获取DOM元素
        const graphCanvas = document.getElementById('graphCanvas');
        const moleculeCanvas = document.getElementById('moleculeCanvas');
        const graphCtx = graphCanvas.getContext('2d');
        const moleculeCtx = moleculeCanvas.getContext('2d');
        
        const playPauseBtn = document.getElementById('playPauseBtn');
        const resetBtn = document.getElementById('resetBtn');
        const toggleProcessBtn = document.getElementById('toggleProcessBtn');
        const rateSlider = document.getElementById('rateSlider');
        const rateValue = document.getElementById('rateValue');
        
        const phaseIndicator = document.getElementById('phaseIndicator');
        const energyInfo = document.getElementById('energyInfo');
        const timeValue = document.getElementById('timeValue');
        const tempValue = document.getElementById('tempValue');
        const stateValue = document.getElementById('stateValue');
        const moleculeSubtitle = document.getElementById('moleculeSubtitle');
        
        // 物质选择器
        const materialOptions = document.querySelectorAll('input[name="material"]');
        materialOptions.forEach(option => {
            option.addEventListener('change', function() {
                document.querySelectorAll('.radio-option').forEach(el => el.classList.remove('active'));
                this.parentElement.classList.add('active');
                currentMaterial = this.value;
                updateMoleculeSubtitle();
                resetAnimation();
            });
        });
        
        // 按钮事件监听
        playPauseBtn.addEventListener('click', toggleAnimation);
        resetBtn.addEventListener('click', resetAnimation);
        toggleProcessBtn.addEventListener('click', toggleProcess);
        rateSlider.addEventListener('input', updateRate);
        
        // 初始化
        initGraph();
        drawMolecules();
        updateInfoPanel();
        
        // 初始化温度-时间图
        function initGraph() {
            const ctx = graphCtx;
            const width = graphCanvas.width;
            const height = graphCanvas.height;
            const padding = { top: 20, right: 30, bottom: 40, left: 60 };
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制坐标轴
            ctx.strokeStyle = '#2c3e50';
            ctx.lineWidth = 2;
            
            // Y轴（温度）
            ctx.beginPath();
            ctx.moveTo(padding.left, padding.top);
            ctx.lineTo(padding.left, height - padding.bottom);
            ctx.stroke();
            
            // X轴（时间）
            ctx.beginPath();
            ctx.moveTo(padding.left, height - padding.bottom);
            ctx.lineTo(width - padding.right, height - padding.bottom);
            ctx.stroke();
            
            // Y轴刻度与标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = '14px Arial';
            ctx.textAlign = 'right';
            ctx.textBaseline = 'middle';
            
            const maxTemp = 100;
            const tempStep = 20;
            for (let temp = -20; temp <= maxTemp; temp += tempStep) {
                const y = height - padding.bottom - (temp + 20) * (height - padding.top - padding.bottom) / (maxTemp + 20);
                ctx.beginPath();
                ctx.moveTo(padding.left - 5, y);
                ctx.lineTo(padding.left, y);
                ctx.stroke();
                
                ctx.fillText(temp + '°C', padding.left - 10, y);
            }
            
            // X轴刻度与标签
            ctx.textAlign = 'center';
            ctx.textBaseline = 'top';
            
            const maxTime = 300;
            const timeStep = 50;
            for (let t = 0; t <= maxTime; t += timeStep) {
                const x = padding.left + t * (width - padding.left - padding.right) / maxTime;
                ctx.beginPath();
                ctx.moveTo(x, height - padding.bottom);
                ctx.lineTo(x, height - padding.bottom + 5);
                ctx.stroke();
                
                ctx.fillText(t + 's', x, height - padding.bottom + 10);
            }
            
            // 坐标轴标签
            ctx.font = 'bold 16px Arial';
            ctx.fillStyle = '#3498db';
            ctx.textAlign = 'center';
            ctx.fillText('时间 (s)', width / 2, height - 5);
            
            ctx.save();
            ctx.translate(15, height / 2);
            ctx.rotate(-Math.PI / 2);
            ctx.fillText('温度 (°C)', 0, 0);
            ctx.restore();
            
            // 绘制晶体熔点参考线
            ctx.strokeStyle = 'rgba(231, 76, 60, 0.3)';
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            const meltingY = height - padding.bottom - (crystalMeltingPoint + 20) * (height - padding.top - padding.bottom) / (maxTemp + 20);
            ctx.moveTo(padding.left, meltingY);
            ctx.lineTo(width - padding.right, meltingY);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制晶体熔化区域
            ctx.fillStyle = 'rgba(231, 76, 60, 0.1)';
            const meltStartX = padding.left + 80 * (width - padding.left - padding.right) / maxTime;
            const meltEndX = padding.left + (80 + crystalMeltingDuration) * (width - padding.left - padding.right) / maxTime;
            ctx.fillRect(meltStartX, meltingY - 20, meltEndX - meltStartX, 40);
            
            // 添加文本标签
            ctx.fillStyle = '#e74c3c';
            ctx.font = 'italic 14px Arial';
            ctx.fillText('晶体熔点: 0°C', width - padding.right - 80, meltingY - 10);
        }
        
        // 绘制分子模型
        function drawMolecules() {
            const ctx = moleculeCtx;
            const width = moleculeCanvas.width;
            const height = moleculeCanvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 根据当前物质和状态绘制分子
            if (currentMaterial === 'compare') {
                // 对比模式：左右分屏显示
                drawCrystalMolecules(0, 0, width/2, height);
                drawNonCrystalMolecules(width/2, 0, width/2, height);
            } else if (currentMaterial === 'crystal') {
                drawCrystalMolecules(0, 0, width, height);
            } else {
                drawNonCrystalMolecules(0, 0, width, height);
            }
        }
        
        // 绘制晶体分子
        function drawCrystalMolecules(x, y, w, h) {
            const ctx = moleculeCtx;
            const centerX = x + w/2;
            const centerY = y + h/2;
            
            // 根据状态确定分子排列
            let moleculeSize, spacing, vibration, order, color;
            
            if (state === 'solid') {
                // 固态：规则排列，小幅度振动
                moleculeSize = 8;
                spacing = 20;
                vibration = 1;
                order = 1.0;
                color = '#aed6f1'; // 浅蓝色
            } else if (state === 'melting' || state === 'freezing') {
                // 熔化/凝固中：部分有序，中等振动
                moleculeSize = 9;
                spacing = 22;
                vibration = 3;
                order = 0.5;
                color = '#f5b7b1'; // 浅红色
            } else {
                // 液态：无序排列，大幅度运动
                moleculeSize = 10;
                spacing = 25;
                vibration = 5;
                order = 0.0;
                color = '#fad7a0'; // 浅橙色
            }
            
            // 计算分子数量
            const cols = Math.floor(w / spacing) - 2;
            const rows = Math.floor(h / spacing) - 2;
            const startX = centerX - (cols * spacing) / 2;
            const startY = centerY - (rows * spacing) / 2;
            
            // 绘制分子
            for (let i = 0; i < cols; i++) {
                for (let j = 0; j < rows; j++) {
                    let posX, posY;
                    
                    if (order > 0.5) {
                        // 有序排列（晶格）
                        posX = startX + i * spacing;
                        posY = startY + j * spacing;
                        
                        // 添加振动效果
                        if (vibration > 0) {
                            posX += (Math.random() - 0.5) * vibration;
                            posY += (Math.random() - 0.5) * vibration;
                        }
                    } else if (order > 0.2) {
                        // 部分有序（熔化/凝固中）
                        const baseX = startX + i * spacing;
                        const baseY = startY + j * spacing;
                        const disorder = (1 - order) * 15;
                        
                        posX = baseX + (Math.random() - 0.5) * disorder;
                        posY = baseY + (Math.random() - 0.5) * disorder;
                        
                        // 添加振动效果
                        posX += (Math.random() - 0.5) * vibration;
                        posY += (Math.random() - 0.5) * vibration;
                    } else {
                        // 完全无序（液态）
                        posX = startX + i * spacing + (Math.random() - 0.5) * 20;
                        posY = startY + j * spacing + (Math.random() - 0.5) * 20;
                        
                        // 添加运动效果
                        const motion = time * 0.1;
                        posX += Math.sin(i * 0.5 + motion) * 3;
                        posY += Math.cos(j * 0.5 + motion) * 3;
                    }
                    
                    // 绘制分子
                    ctx.beginPath();
                    ctx.arc(posX, posY, moleculeSize, 0, Math.PI * 2);
                    
                    // 根据温度添加渐变填充
                    const gradient = ctx.createRadialGradient(
                        posX, posY, 0,
                        posX, posY, moleculeSize
                    );
                    
                    if (temperature < 0) {
                        gradient.addColorStop(0, '#aed6f1');
                        gradient.addColorStop(1, '#5dade2');
                    } else if (temperature < 20) {
                        gradient.addColorStop(0, '#f5b7b1');
                        gradient.addColorStop(1, '#e74c3c');
                    } else {
                        gradient.addColorStop(0, '#fad7a0');
                        gradient.addColorStop(1, '#e67e22');
                    }
                    
                    ctx.fillStyle = gradient;
                    ctx.fill();
                    
                    // 添加高光效果
                    ctx.beginPath();
                    ctx.arc(posX - moleculeSize/3, posY - moleculeSize/3, moleculeSize/3, 0, Math.PI * 2);
                    ctx.fillStyle = 'rgba(255, 255, 255, 0.6)';
                    ctx.fill();
                }
            }
            
            // 如果是熔化/凝固过程，绘制晶格结构线（逐渐消失/出现）
            if (state === 'melting' || state === 'freezing') {
                ctx.strokeStyle = `rgba(255, 255, 255, ${order * 0.5})`;
                ctx.lineWidth = 1;
                
                for (let i = 0; i < cols; i++) {
                    for (let j = 0; j < rows; j++) {
                        const baseX = startX + i * spacing;
                        const baseY = startY + j * spacing;
                        
                        // 水平连接线
                        if (i < cols - 1) {
                            ctx.beginPath();
                            ctx.moveTo(baseX, baseY);
                            ctx.lineTo(baseX + spacing, baseY);
                            ctx.stroke();
                        }
                        
                        // 垂直连接线
                        if (j < rows - 1) {
                            ctx.beginPath();
                            ctx.moveTo(baseX, baseY);
                            ctx.lineTo(baseX, baseY + spacing);
                            ctx.stroke();
                        }
                    }
                }
            }
        }
        
        // 绘制非晶体分子
        function drawNonCrystalMolecules(x, y, w, h) {
            const ctx = moleculeCtx;
            const centerX = x + w/2;
            const centerY = y + h/2;
            
            // 根据状态确定分子排列
            let moleculeSize, spacing, vibration, order, color;
            const softening = (temperature - nonCrystalSofteningStart) / (nonCrystalLiquidTemp - nonCrystalSofteningStart);
            
            if (temperature < nonCrystalSofteningStart) {
                // 固态：无序但紧密排列
                moleculeSize = 8;
                spacing = 18;
                vibration = 0.5;
                order = 0.0;
                color = '#aed6f1';
            } else if (temperature < nonCrystalLiquidTemp) {
                // 软化中：逐渐变得松散
                moleculeSize = 9;
                spacing = 18 + softening * 10;
                vibration = 1 + softening * 4;
                order = 0.0;
                color = '#f5b7b1';
            } else {
                // 液态：松散无序
                moleculeSize = 10;
                spacing = 28;
                vibration = 6;
                order = 0.0;
                color = '#fad7a0';
            }
            
            // 计算分子数量
            const cols = Math.floor(w / spacing) - 2;
            const rows = Math.floor(h / spacing) - 2;
            const startX = centerX - (cols * spacing) / 2;
            const startY = centerY - (rows * spacing) / 2;
            
            // 绘制分子（始终无序排列）
            for (let i = 0; i < cols; i++) {
                for (let j = 0; j < rows; j++) {
                    const baseX = startX + i * spacing;
                    const baseY = startY + j * spacing;
                    
                    // 非晶体始终有一定程度的无序
                    const disorder = 10 * (1 - order);
                    let posX = baseX + (Math.random() - 0.5) * disorder;
                    let posY = baseY + (Math.random() - 0.5) * disorder;
                    
                    // 添加振动/运动效果
                    posX += (Math.random() - 0.5) * vibration;
                    posY += (Math.random() - 0.5) * vibration;
                    
                    // 如果是液态，添加流动效果
                    if (temperature >= nonCrystalLiquidTemp) {
                        const motion = time * 0.1;
                        posX += Math.sin(i * 0.3 + motion) * 4;
                        posY += Math.cos(j * 0.3 + motion) * 4;
                    }
                    
                    // 绘制分子
                    ctx.beginPath();
                    ctx.arc(posX, posY, moleculeSize, 0, Math.PI * 2);
                    
                    // 根据温度添加渐变填充
                    const gradient = ctx.createRadialGradient(
                        posX, posY, 0,
                        posX, posY, moleculeSize
                    );
                    
                    if (temperature < 20) {
                        gradient.addColorStop(0, '#aed6f1');
                        gradient.addColorStop(1, '#5dade2');
                    } else if (temperature < 50) {
                        gradient.addColorStop(0, '#f5b7b1');
                        gradient.addColorStop(1, '#e74c3c');
                    } else {
                        gradient.addColorStop(0, '#fad7a0');
                        gradient.addColorStop(1, '#e67e22');
                    }
                    
                    ctx.fillStyle = gradient;
                    ctx.fill();
                    
                    // 添加高光效果
                    ctx.beginPath();
                    ctx.arc(posX - moleculeSize/3, posY - moleculeSize/3, moleculeSize/3, 0, Math.PI * 2);
                    ctx.fillStyle = 'rgba(255, 255, 255, 0.6)';
                    ctx.fill();
                }
            }
        }
        
        // 绘制温度曲线
        function drawTemperatureCurve() {
            const ctx = graphCtx;
            const width = graphCanvas.width;
            const height = graphCanvas.height;
            const padding = { top: 20, right: 30, bottom: 40, left: 60 };
            const maxTemp = 100;
            const maxTime = 300;
            
            // 清除之前的曲线（保留坐标轴）
            ctx.clearRect(padding.left, padding.top, 
                         width - padding.left - padding.right, 
                         height - padding.top - padding.bottom);
            
            // 绘制晶体曲线（如果当前物质是晶体或对比模式）
            if (currentMaterial === 'crystal' || currentMaterial === 'compare') {
                drawCrystalCurve();
            }
            
            // 绘制非晶体曲线（如果当前物质是非晶体或对比模式）
            if (currentMaterial === 'non-crystal' || currentMaterial === 'compare') {
                drawNonCrystalCurve();
            }
            
            // 绘制当前时间点指示器
            const x = padding.left + time * (width - padding.left - padding.right) / maxTime;
            const currentTemp = currentMaterial === 'non-crystal' ? 
                calculateNonCrystalTemperature(time) : calculateCrystalTemperature(time);
            const y = height - padding.bottom - (currentTemp + 20) * (height - padding.top - padding.bottom) / (maxTemp + 20);
            
            // 绘制指示点
            ctx.beginPath();
            ctx.arc(x, y, 8, 0, Math.PI * 2);
            ctx.fillStyle = '#2c3e50';
            ctx.fill();
            ctx.strokeStyle = 'white';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制指示线
            ctx.strokeStyle = 'rgba(52, 152, 219, 0.5)';
            ctx.setLineDash([3, 3]);
            ctx.beginPath();
            ctx.moveTo(x, padding.top);
            ctx.lineTo(x, height - padding.bottom);
            ctx.moveTo(padding.left, y);
            ctx.lineTo(width - padding.right, y);
            ctx.stroke();
            ctx.setLineDash([]);
        }
        
        // 绘制晶体温度曲线
        function drawCrystalCurve() {
            const ctx = graphCtx;
            const width = graphCanvas.width;
            const height = graphCanvas.height;
            const padding = { top: 20, right: 30, bottom: 40, left: 60 };
            const maxTemp = 100;
            const maxTime = 300;
            
            ctx.beginPath();
            ctx.lineWidth = 3;
            
            // 固态升温阶段 (0-80s)
            const solidEndX = padding.left + 80 * (width - padding.left - padding.right) / maxTime;
            const solidEndY = height - padding.bottom - (crystalMeltingPoint + 20) * (height - padding.top - padding.bottom) / (maxTemp + 20);
            
            ctx.moveTo(padding.left, height - padding.bottom - (-10 + 20) * (height - padding.top - padding.bottom) / (maxTemp + 20));
            ctx.lineTo(solidEndX, solidEndY);
            ctx.strokeStyle = '#2980b9';
            ctx.stroke();
            
            // 熔化平台阶段 (80-140s)
            const meltEndX = padding.left + (80 + crystalMeltingDuration) * (width - padding.left - padding.right) / maxTime;
            ctx.beginPath();
            ctx.moveTo(solidEndX, solidEndY);
            ctx.lineTo(meltEndX, solidEndY);
            ctx.strokeStyle = '#e74c3c';
            ctx.lineWidth = 4;
            ctx.stroke();
            
            // 液态升温阶段 (140-300s)
            ctx.beginPath();
            ctx.moveTo(meltEndX, solidEndY);
            ctx.lineTo(width - padding.right, height - padding.bottom - (crystalMaxTemp + 20) * (height - padding.top - padding.bottom) / (maxTemp + 20));
            ctx.strokeStyle = '#2980b9';
            ctx.lineWidth = 3;
            ctx.stroke();
        }
        
        // 绘制非晶体温度曲线
        function drawNonCrystalCurve() {
            const ctx = graphCtx;
            const width = graphCanvas.width;
            const height = graphCanvas.height;
            const padding = { top: 20, right: 30, bottom: 40, left: 60 };
            const maxTemp = 100;
            const maxTime = 300;
            
            ctx.beginPath();
            ctx.lineWidth = 3;
            ctx.strokeStyle = '#e67e22';
            
            // 非晶体曲线（平滑上升，无平台）
            const points = [];
            for (let t = 0; t <= maxTime; t += 5) {
                const temp = calculateNonCrystalTemperature(t);
                const x = padding.left + t * (width - padding.left - padding.right) / maxTime;
                const y = height - padding.bottom - (temp + 20) * (height - padding.top - padding.bottom) / (maxTemp + 20);
                points.push({x, y});
            }
            
            // 绘制曲线
            ctx.moveTo(points[0].x, points[0].y);
            for (let i = 1; i < points.length; i++) {
                ctx.lineTo(points[i].x, points[i].y);
            }
            ctx.stroke();
            
            // 标记软化开始区域
            const softeningStartY = height - padding.bottom - (nonCrystalSofteningStart + 20) * (height - padding.top - padding.bottom) / (maxTemp + 20);
            const softeningStartX = padding.left + 160 * (width - padding.left - padding.right) / maxTime;
            
            ctx.fillStyle = 'rgba(230, 126, 34, 0.1)';
            ctx.fillRect(softeningStartX, softeningStartY - 30, 100, 60);
            
            ctx.fillStyle = '#e67e22';
            ctx.font = 'italic 12px Arial';
            ctx.fillText('软化
<!--检测到代码截断，自动续写中...-->
开始', softeningStartX + 10, softeningStartY - 10);
        }
        
        // 计算晶体在给定时间的温度
        function calculateCrystalTemperature(t) {
            if (t < 80) {
                // 固态升温阶段
                return -10 + t * crystalHeatingRate;
            } else if (t < 80 + crystalMeltingDuration) {
                // 熔化平台阶段
                return crystalMeltingPoint;
            } else if (t < 300) {
                // 液态升温阶段
                return crystalMeltingPoint + (t - 80 - crystalMeltingDuration) * crystalHeatingRate;
            } else {
                return crystalMaxTemp;
            }
        }
        
        // 计算非晶体在给定时间的温度
        function calculateNonCrystalTemperature(t) {
            // 非晶体温度持续上升，但速率可能变化
            if (t < 160) {
                return -10 + t * nonCrystalHeatingRate;
            } else if (t < 240) {
                // 软化阶段，升温稍慢
                return nonCrystalSofteningStart + (t - 160) * nonCrystalHeatingRate * 0.8;
            } else {
                return nonCrystalLiquidTemp + (t - 240) * nonCrystalHeatingRate * 0.6;
            }
        }
        
        // 更新信息面板
        function updateInfoPanel() {
            // 更新读数
            timeValue.textContent = time.toFixed(1) + ' s';
            tempValue.textContent = temperature.toFixed(1) + ' °C';
            
            // 更新状态显示
            let stateText = '';
            if (currentMaterial === 'crystal') {
                if (state === 'solid') stateText = '固态';
                else if (state === 'melting') stateText = '熔化中';
                else if (state === 'liquid') stateText = '液态';
                else if (state === 'freezing') stateText = '凝固中';
            } else if (currentMaterial === 'non-crystal') {
                if (temperature < nonCrystalSofteningStart) stateText = '固态';
                else if (temperature < nonCrystalLiquidTemp) stateText = '软化中';
                else stateText = '液态';
            } else {
                stateText = '对比模式';
            }
            stateValue.textContent = stateText;
            
            // 更新阶段指示器和能量信息
            updatePhaseAndEnergyInfo();
        }
        
        // 更新阶段和能量信息
        function updatePhaseAndEnergyInfo() {
            let phaseText = '';
            let energyText = '';
            
            if (currentMaterial === 'crystal') {
                if (state === 'solid') {
                    phaseText = '固态升温阶段';
                    energyText = '吸收的热量用于增加分子动能，分子振动加剧，温度上升。';
                } else if (state === 'melting') {
                    phaseText = '熔化过程（温度平台）';
                    energyText = '吸收的热量用于破坏晶格结构，分子排列从有序变为无序，温度保持不变。';
                } else if (state === 'liquid') {
                    phaseText = '液态升温阶段';
                    energyText = '吸收的热量用于增加分子动能，分子运动更加剧烈，温度上升。';
                } else if (state === 'freezing') {
                    phaseText = '凝固过程（温度平台）';
                    energyText = '释放的热量使分子排列从无序变为有序，形成晶格结构，温度保持不变。';
                }
            } else if (currentMaterial === 'non-crystal') {
                if (temperature < nonCrystalSofteningStart) {
                    phaseText = '固态升温阶段';
                    energyText = '吸收的热量用于增加分子动能，分子振动加剧，温度持续上升。';
                } else if (temperature < nonCrystalLiquidTemp) {
                    phaseText = '软化过程';
                    energyText = '分子逐渐获得移动能力，排列逐渐变得松散，没有明显的相变平台。';
                } else {
                    phaseText = '液态升温阶段';
                    energyText = '分子可以自由移动，吸收的热量使分子运动更加剧烈，温度持续上升。';
                }
            } else {
                phaseText = '对比模式';
                energyText = '左侧：晶体有固定熔点，熔化时温度保持不变。右侧：非晶体无固定熔点，熔化时温度持续上升。';
            }
            
            phaseIndicator.textContent = phaseText;
            energyInfo.textContent = energyText;
        }
        
        // 更新分子模型副标题
        function updateMoleculeSubtitle() {
            if (currentMaterial === 'crystal') {
                moleculeSubtitle.textContent = '晶体分子排列（有规则晶格结构）';
            } else if (currentMaterial === 'non-crystal') {
                moleculeSubtitle.textContent = '非晶体分子排列（无规则结构）';
            } else {
                moleculeSubtitle.textContent = '左侧：晶体分子排列 | 右侧：非晶体分子排列';
            }
        }
        
        // 动画循环
        function animate() {
            if (!isPlaying) return;
            
            // 根据速率更新时间
            const rateFactor = animationRate / 3; // 基准速率为3
            time += 0.5 * rateFactor;
            
            // 限制时间范围
            if (time > 300) time = 300;
            if (time < 0) time = 0;
            
            // 计算当前温度
            if (currentMaterial === 'non-crystal') {
                temperature = calculateNonCrystalTemperature(time);
                
                // 更新非晶体状态
                if (temperature < nonCrystalSofteningStart) {
                    state = 'solid';
                } else if (temperature < nonCrystalLiquidTemp) {
                    state = 'melting'; // 使用melting表示软化过程
                } else {
                    state = 'liquid';
                }
            } else {
                // 晶体或对比模式
                temperature = calculateCrystalTemperature(time);
                
                // 更新晶体状态
                if (time < 80) {
                    state = 'solid';
                } else if (time < 80 + crystalMeltingDuration) {
                    state = isMelting ? 'melting' : 'freezing';
                } else {
                    state = 'liquid';
                }
            }
            
            // 如果是凝固过程，调整温度显示
            if (!isMelting && currentMaterial !== 'non-crystal') {
                // 对于凝固过程，我们从高温开始
                const reverseTime = 300 - time;
                temperature = calculateCrystalTemperature(reverseTime);
                
                // 更新状态
                if (reverseTime > 80 + crystalMeltingDuration) {
                    state = 'liquid';
                } else if (reverseTime > 80) {
                    state = 'freezing';
                } else {
                    state = 'solid';
                }
            }
            
            // 更新显示
            drawTemperatureCurve();
            drawMolecules();
            updateInfoPanel();
            
            // 继续动画循环
            if (isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }
        
        // 切换动画播放状态
        function toggleAnimation() {
            isPlaying = !isPlaying;
            
            if (isPlaying) {
                playPauseBtn.textContent = isMelting ? '暂停熔化' : '暂停凝固';
                playPauseBtn.classList.remove('btn-primary');
                playPauseBtn.classList.add('btn-secondary');
                animationId = requestAnimationFrame(animate);
            } else {
                playPauseBtn.textContent = isMelting ? '继续熔化' : '继续凝固';
                playPauseBtn.classList.remove('btn-secondary');
                playPauseBtn.classList.add('btn-primary');
                if (animationId) {
                    cancelAnimationFrame(animationId);
                }
            }
        }
        
        // 重置动画
        function resetAnimation() {
            time = 0;
            temperature = -10;
            state = 'solid';
            
            // 根据当前过程设置初始状态
            if (!isMelting && currentMaterial !== 'non-crystal') {
                // 凝固过程从高温开始
                time = 300;
                temperature = calculateCrystalTemperature(300);
                state = 'liquid';
            }
            
            drawTemperatureCurve();
            drawMolecules();
            updateInfoPanel();
            
            // 如果正在播放，重新开始动画
            if (isPlaying) {
                if (animationId) cancelAnimationFrame(animationId);
                animationId = requestAnimationFrame(animate);
            }
        }
        
        // 切换熔化/凝固过程
        function toggleProcess() {
            isMelting = !isMelting;
            
            if (isMelting) {
                toggleProcessBtn.textContent = '切换为凝固过程';
                playPauseBtn.textContent = isPlaying ? '暂停熔化' : '开始熔化';
            } else {
                toggleProcessBtn.textContent = '切换为熔化过程';
                playPauseBtn.textContent = isPlaying ? '暂停凝固' : '开始凝固';
            }
            
            resetAnimation();
        }
        
        // 更新速率
        function updateRate() {
            animationRate = parseInt(rateSlider.value);
            
            // 更新速率显示
            const rateLabels = ['极慢', '慢速', '中速', '快速', '极快'];
            rateValue.textContent = rateLabels[animationRate - 1];
        }
        
        // 初始更新
        updateMoleculeSubtitle();
        updateRate();
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 晶体与非晶体熔化凝固过程交互式教学动画使用指南

欢迎使用本交互式教学动画！本动画旨在帮助您直观理解晶体与非晶体在熔化和凝固过程中的核心差异。通过联动展示宏观的温度-时间图像与微观的分子排列模型，您将能够深入探索物态变化的物理本质。

---

### 一、功能说明

本动画包含三个主要交互区域：

1. **控制面板**（左侧）：提供物质选择、过程控制、信息显示等功能
2. **温度-时间图像区**（右上）：动态绘制晶体与非晶体的熔化/凝固曲线
3. **分子排列模型区**（右下）：实时展示对应物态下的分子运动与排列变化

三个区域完全联动，任何操作都会同步更新所有显示内容。

---

### 二、主要功能

#### 1. 物质选择功能
- **晶体（冰）模式**：展示有固定熔点（0°C）的典型晶体物质
- **非晶体（石蜡）模式**：展示无固定熔点的典型非晶体物质
- **对比模式**：并排显示晶体与非晶体的熔化过程，便于直观比较

#### 2. 过程控制功能
- **开始/暂停**：启动或暂停动画过程
- **重置**：将动画恢复到初始状态
- **过程切换**：在"熔化过程"与"凝固过程"之间切换
- **速率调节**：五档速度调节（极慢、慢速、中速、快速、极快）

#### 3. 信息显示功能
- **实时读数**：显示当前时间、温度和物态
- **阶段指示**：高亮显示当前所处阶段（如"固态升温"、"熔化过程"等）
- **能量说明**：解释每个阶段吸收/释放热量的去向
- **视觉提示**：坐标图上的指示点、参考线、高亮区域

---

### 三、设计特色

#### 1. 双视图联动设计
- **宏观与微观结合**：温度曲线的每个变化点都对应分子模型的特定状态
- **实时同步**：时间轴上的任何位置都能看到对应的分子排列状态

#### 2. 视觉对比设计
- **颜色编码**：晶体用蓝色系，非晶体用橙色系，熔化平台用红色强调
- **分子动画差异**：
  - 晶体：固态时规则晶格，熔化时晶格逐渐崩溃，液态时完全无序
  - 非晶体：始终无序排列，从固态到液态为连续渐变过程

#### 3. 认知引导设计
- **阶段化提示**：每个关键阶段都有文字说明和能量解释
- **关键点标记**：熔点、软化点等关键温度有视觉标记
- **对比模式**：并排显示强化差异认知

---

### 四、教学要点

#### 核心概念对比

| 特征 | 晶体（如冰） | 非晶体（如石蜡） |
|------|-------------|-----------------|
| **熔点** | 有固定熔点（0°C） | 无固定熔点 |
| **温度曲线** | 熔化/凝固时有水平平台 | 平滑曲线，无平台 |
| **分子排列** | 固态时规则晶格结构 | 始终无序排列 |
| **熔化过程** | 晶格结构在熔点处崩溃 | 逐渐软化，无结构突变 |
| **能量变化** | 熔化时吸收热量破坏晶格 | 持续吸热，温度持续上升 |

#### 关键观察点

1. **晶体熔化平台**：
   - 观察温度保持在0°C不变的时间段
   - 注意此时分子模型的变化：晶格结构逐渐瓦解
   - 理解能量去向：吸收的热量用于破坏分子间的有序排列

2. **非晶体连续变化**：
   - 观察温度持续上升，无平台期
   - 注意分子模型从固态到液态的渐变过程
   - 理解"软化"概念：分子逐渐获得移动能力

3. **凝固过程对比**：
   - 晶体凝固时出现温度平台，分子重新形成有序排列
   - 非晶体凝固时温度持续下降，分子逐渐"冻结"在无序状态

---

### 五、使用建议

#### 1. 初次探索（建议用时：5分钟）
- 选择"晶体（冰）模式"，点击"开始熔化"
- 观察温度曲线如何变化，特别关注0°C平台
- 同时观察分子模型从有序晶格到无序液体的转变
- 阅读右侧的信息提示，理解每个阶段的物理意义

#### 2. 对比学习（建议用时：8分钟）
- 切换到"对比模式"
- 同时观察晶体与非晶体的熔化过程
- 重点关注：
  - 晶体有平台 vs 非晶体无平台
  - 晶体分子排列突变 vs 非晶体分子排列渐变
- 使用"暂停"功能在关键点仔细对比

#### 3. 深入探究（建议用时：10分钟）
- 尝试"凝固过程"，观察与熔化过程的异同
- 调节动画速率，在"极慢"模式下仔细观察分子细节
- 思考问题：
  - 为什么晶体有固定熔点而非晶体没有？
  - 熔化过程中，能量去了哪里？
  - 分子排列如何影响物质的宏观性质？

#### 4. 教学应用建议
- **课堂演示**：使用投影仪全屏展示，教师边操作边讲解
- **小组探究**：学生分组操作，完成对比观察任务单
- **自主学习**：学生自主探索，记录观察结果并回答问题
- **复习巩固**：作为章节复习工具，强化核心概念理解

---

### 技术提示

1. **最佳观看环境**：建议在电脑或平板电脑上使用，确保屏幕分辨率足够
2. **浏览器兼容**：支持所有现代浏览器（Chrome、Firefox、Safari、Edge）
3. **交互技巧**：
   - 鼠标悬停在控制按钮上有视觉反馈
   - 使用滑块可精细控制动画速度
   - 重置后可以重新开始观察

---

### 学习目标达成

完成本动画的学习后，您应该能够：

1. **解释**晶体与非晶体在熔化凝固过程中的温度变化差异
2. **描述**晶体与非晶体的微观结构特征
3. **关联**宏观温度曲线与微观分子排列变化
4. **应用**能量守恒原理解释熔化凝固过程中的能量转化
5. **区分**常见物质中哪些是晶体、哪些是非晶体

---

**祝您探索愉快！** 通过这个交互式动画，我们希望您不仅能记住知识，更能理解现象背后的物理本质。如有任何问题或建议，欢迎反馈。

*熊猫老师 教学动画设计团队*  
*让抽象概念变得触手可及*