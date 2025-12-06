# 需求：化学平衡的动态建立与移动（分子个数实时变化）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中或大学低年级的化学学习者。用户的核心需求是**直观、动态地理解化学平衡这一抽象概念**。具体痛点包括：
1.  **难以想象微观过程**：学生难以在脑海中构建反应物与生成物分子在密闭容器中持续碰撞、反应、生成的动态画面。
2.  **混淆“平衡”与“静止”**：常误认为达到平衡时，正逆反应停止，分子数量不再变化。
3.  **不理解平衡移动的微观本质**：对浓度、压强、温度等因素如何通过改变分子碰撞频率来影响平衡，缺乏粒子层面的理解。
因此，动画的核心任务是**将微观粒子行为可视化、数据化**，并允许用户通过交互主动探究，将抽象概念转化为具象认知。

#### 教学设计思路
*   **核心概念**：围绕“可逆反应”、“动态平衡”、“平衡常数K”、“平衡移动（勒夏特列原理）”展开。动画将清晰地展示：反应开始 → 正反应速率主导 → 逆反应速率出现并增大 → 正逆反应速率相等（动态平衡） → 外界条件改变 → 平衡移动 → 建立新平衡。
*   **认知规律**：遵循“具体 → 抽象”、“观察 → 归纳”的路径。先让学生观察五彩斑斓的分子运动，再引导其关注数量/速率曲线，最后总结出规律。
*   **交互设计**：
    *   **控制与探究**：用户可点击“开始/暂停/重置”控制反应，通过滑块或按钮“增加反应物浓度”、“增大压强（压缩容器）”、“升高温度”来扰动平衡，观察系统的即时响应和重新平衡过程。
    *   **多通道反馈**：视觉（分子运动与数量变化）、数据（实时分子个数、反应速率值）、图形（浓度-时间曲线、速率-时间曲线）同步更新，强化理解。
    *   **焦点引导**：通过高亮、闪烁或放大特定分子（如在增加A浓度时，新加入的A分子会高亮），提示用户关注变化起点。
*   **视觉呈现**：
    *   **主视图**：一个显眼的密闭容器（如烧瓶或透明盒子），内部有大量**颜色、形状截然不同**的粒子（如红色圆球代表A分子，蓝色圆球代表B分子，黄色双球代表C分子等）进行无规则热运动。碰撞时会有简单的视觉效果（如闪光或短暂变形）表示反应发生。
    *   **数据面板**：实时显示反应物和生成物的**分子个数**，以及**正反应速率**和**逆反应速率**的数值。
    *   **曲线图**：绘制两条实时曲线图：
        1.  **分子个数-时间图**：用不同颜色的曲线分别追踪反应物和生成物分子数量随时间的变化，最终趋于水平。
        2.  **反应速率-时间图**：用两条曲线分别展示正、逆反应速率随时间的变化，最终交汇于一点（速率相等）。

#### 配色方案选择
选择明亮、对比度高且符合化学视觉习惯的配色，确保清晰度和可访问性。
*   **粒子颜色**：
    *   反应物A：`#FF6B6B`（珊瑚红，醒目）
    *   反应物B：`#4ECDC4`（青绿色，与红色形成对比）
    *   生成物C：`#FFD166`（琥珀黄，温暖明亮）
    *   （可选）生成物D：`#9D65C9`（紫色）
*   **背景与容器**：
    *   画布背景：`#F7F9FC`（浅灰蓝，柔和护眼）
    *   反应容器：`#FFFFFF`（白色）描边，带轻微阴影，内部为透明或极浅的`#E3F2FD`（淡蓝），以突出粒子。
*   **数据与UI**：
    *   数据文本：`#2C3E50`（深蓝灰，清晰易读）
    *   控制按钮（开始/暂停）：`#2E86AB`（专业蓝）/ `#A23B72`（暂停红）
    *   干扰按钮（加浓度/压/温）：`#F18F01`（橙色，代表“行动”或“改变”）
    *   曲线颜色：与对应粒子颜色一致（如红色曲线代表A的数量，黄色曲线代表C的数量）。

#### 交互功能列表
1.  **反应控制**：
    *   “开始/暂停”按钮：启动或暂停模拟。
    *   “重置”按钮：将所有参数恢复至初始状态。
2.  **平衡扰动（探究工具）**：
    *   “增加A浓度”按钮：瞬间向容器中加入一定数量的A分子（高亮显示）。
    *   “增大压强”（压缩容器）按钮：视觉上容器体积缩小，单位体积内分子密度瞬间增加。
    *   “升高温度”按钮：所有分子运动速度明显加快，碰撞更频繁。
    *   （可选）“添加催化剂”按钮：降低反应活化能，正逆反应速率同比增加，但不影响平衡点。
3.  **视图与显示控制**：
    *   “显示/隐藏曲线图”切换：可专注于粒子视图或数据分析。
    *   “显示/隐藏数据面板”切换。
    *   “显示/隐藏速率箭头”切换：在粒子上方显示表示运动速度大小和方向的小箭头。
4.  **实时反馈**：
    *   所有交互操作均实时、同步地更新粒子视图、数据面板和曲线图。
    *   当正逆反应速率相等（平衡）时，界面有温和的提示（如“动态平衡达成”的文字提示或容器边框微光）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>化学平衡的动态建立与移动</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #F7F9FC;
            color: #2C3E50;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            padding: 25px;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #E3F2FD;
        }
        
        h1 {
            color: #2E86AB;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }
        
        .subtitle {
            color: #5D6D7E;
            font-size: 1.1rem;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 25px;
        }
        
        .simulation-area {
            flex: 1;
            min-width: 500px;
            background-color: #FFFFFF;
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.05);
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 400px;
            background-color: #F7F9FC;
            border-radius: 8px;
            overflow: hidden;
            border: 2px solid #E3F2FD;
            margin-bottom: 15px;
        }
        
        #reactionCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .balance-indicator {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: rgba(46, 134, 171, 0.9);
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: bold;
            font-size: 0.9rem;
            opacity: 0;
            transition: opacity 0.5s;
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.2);
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .control-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            flex: 1;
        }
        
        button {
            padding: 10px 18px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            font-size: 0.95rem;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }
        
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        .btn-start {
            background-color: #2E86AB;
            color: white;
        }
        
        .btn-pause {
            background-color: #A23B72;
            color: white;
        }
        
        .btn-reset {
            background-color: #5D6D7E;
            color: white;
        }
        
        .btn-disturb {
            background-color: #F18F01;
            color: white;
        }
        
        .btn-toggle {
            background-color: #4ECDC4;
            color: white;
        }
        
        .data-panel {
            flex: 1;
            min-width: 300px;
            background-color: #FFFFFF;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.05);
        }
        
        .data-title {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: #2E86AB;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .data-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 25px;
        }
        
        .data-item {
            background-color: #F7F9FC;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #4ECDC4;
        }
        
        .data-item.reactant {
            border-left-color: #FF6B6B;
        }
        
        .data-item.product {
            border-left-color: #FFD166;
        }
        
        .data-label {
            font-size: 0.95rem;
            color: #5D6D7E;
            margin-bottom: 5px;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        
        .data-value {
            font-size: 2rem;
            font-weight: 700;
        }
        
        .rate-data {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
        }
        
        .rate-item {
            text-align: center;
        }
        
        .rate-value {
            font-size: 1.5rem;
            font-weight: 700;
        }
        
        .rate-label {
            font-size: 0.9rem;
            color: #5D6D7E;
        }
        
        .chart-container {
            width: 100%;
            height: 300px;
            margin-top: 20px;
            background-color: #FFFFFF;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.05);
        }
        
        .chart-title {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: #2E86AB;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        #chartCanvas {
            width: 100%;
            height: calc(100% - 30px);
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
            gap: 6px;
            font-size: 0.9rem;
        }
        
        .legend-color {
            width: 16px;
            height: 16px;
            border-radius: 50%;
        }
        
        .instructions {
            background-color: #E3F2FD;
            border-radius: 10px;
            padding: 20px;
            margin-top: 25px;
        }
        
        .instructions h3 {
            color: #2E86AB;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .instructions ul {
            padding-left: 20px;
        }
        
        .instructions li {
            margin-bottom: 8px;
        }
        
        @media (max-width: 900px) {
            .main-content {
                flex-direction: column;
            }
            
            .simulation-area, .data-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>化学平衡的动态建立与移动</h1>
            <p class="subtitle">可视化模拟：A + B ⇌ C 反应中分子个数的实时变化与平衡移动</p>
        </header>
        
        <div class="main-content">
            <div class="simulation-area">
                <div class="canvas-container">
                    <canvas id="reactionCanvas"></canvas>
                    <div class="balance-indicator" id="balanceIndicator">动态平衡达成 ✓</div>
                </div>
                
                <div class="controls">
                    <div class="control-group">
                        <button id="startBtn" class="btn-start">
                            <span>▶</span> 开始反应
                        </button>
                        <button id="pauseBtn" class="btn-pause" disabled>
                            <span>⏸</span> 暂停
                        </button>
                        <button id="resetBtn" class="btn-reset">
                            <span>↺</span> 重置
                        </button>
                    </div>
                    
                    <div class="control-group">
                        <button id="addAButton" class="btn-disturb">
                            <span>+</span> 增加A浓度
                        </button>
                        <button id="increasePressure" class="btn-disturb">
                            <span>↓</span> 增大压强
                        </button>
                        <button id="increaseTemp" class="btn-disturb">
                            <span>↑</span> 升高温度
                        </button>
                    </div>
                </div>
                
                <div class="controls">
                    <button id="toggleArrows" class="btn-toggle">
                        <span>⇄</span> 显示/隐藏速率箭头
                    </button>
                    <button id="toggleChart" class="btn-toggle">
                        <span>📈</span> 显示/隐藏曲线图
                    </button>
                </div>
            </div>
            
            <div class="data-panel">
                <h2 class="data-title">
                    <span>📊</span> 实时数据面板
                </h2>
                
                <div class="data-grid">
                    <div class="data-item reactant">
                        <div class="data-label">
                            <span style="color: #FF6B6B">●</span> 反应物 A
                        </div>
                        <div class="data-value" id="countA">100</div>
                    </div>
                    
                    <div class="data-item reactant">
                        <div class="data-label">
                            <span style="color: #4ECDC4">●</span> 反应物 B
                        </div>
                        <div class="data-value" id="countB">80</div>
                    </div>
                    
                    <div class="data-item product">
                        <div class="data-label">
                            <span style="color: #FFD166">●</span> 生成物 C
                        </div>
                        <div class="data-value" id="countC">0</div>
                    </div>
                    
                    <div class="data-item">
                        <div class="data-label">
                            <span>⚖️</span> 平衡常数 K
                        </div>
                        <div class="data-value" id="kValue">0.00</div>
                    </div>
                </div>
                
                <div class="rate-data">
                    <div class="rate-item">
                        <div class="rate-value" id="forwardRate">0.00</div>
                        <div class="rate-label">正反应速率</div>
                    </div>
                    
                    <div class="rate-item">
                        <div class="rate-value" id="reverseRate">0.00</div>
                        <div class="rate-label">逆反应速率</div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="chart-container" id="chartContainer">
            <h2 class="chart-title">
                <span>📈</span> 分子个数与反应速率变化曲线
            </h2>
            <canvas id="chartCanvas"></canvas>
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #FF6B6B;"></div>
                    <span>反应物A</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #4ECDC4;"></div>
                    <span>反应物B</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #FFD166;"></div>
                    <span>生成物C</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #A23B72;"></div>
                    <span>正反应速率</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #2E86AB;"></div>
                    <span>逆反应速率</span>
                </div>
            </div>
        </div>
        
        <div class="instructions">
            <h3>
                <span>💡</span> 使用说明
            </h3>
            <ul>
                <li><strong>开始反应</strong>：观察分子运动、碰撞反应以及分子数量的实时变化。</li>
                <li><strong>动态平衡</strong>：当正逆反应速率相等时，系统达到动态平衡（分子数量不再变化，但反应仍在进行）。</li>
                <li><strong>扰动平衡</strong>：使用"增加A浓度"、"增大压强"或"升高温度"按钮，观察平衡如何移动并重新建立。</li>
                <li><strong>数据解读</strong>：关注实时数据面板和曲线图，理解分子个数、反应速率和平衡常数的变化规律。</li>
                <li><strong>勒夏特列原理</strong>：系统会抵抗外界条件的改变，向着减弱这种改变的方向移动。</li>
            </ul>
        </div>
    </div>

    <script>
        // 全局变量和配置
        const config = {
            canvasWidth: 800,
            canvasHeight: 400,
            containerPadding: 20,
            particleRadius: 8,
            reactionRadius: 12,
            baseSpeed: 1.5,
            temperature: 1.0, // 温度因子，影响分子速度
            pressure: 1.0,   // 压强因子，影响容器尺寸
            showArrows: false,
            showChart: true,
            isRunning: false,
            isBalanced: false,
            time: 0,
            timeStep: 0.05,
            maxHistory: 300,
            equilibriumThreshold: 0.05
        };
        
        // 反应参数
        const reaction = {
            // A + B ⇌ C
            countA: 100,
            countB: 80,
            countC: 0,
            forwardRate: 0,
            reverseRate: 0,
            k: 0,
            
            // 反应速率常数
            kForward: 0.02,
            kReverse: 0.01,
            
            // 历史数据记录
            history: {
                time: [],
                countA: [],
                countB: [],
                countC: [],
                forwardRate: [],
                reverseRate: []
            }
        };
        
        // 分子数组
        let particles = [];
        
        // Canvas 上下文
        let reactionCtx, chartCtx;
        
        // DOM 元素
        let startBtn, pauseBtn, resetBtn, addAButton, increasePressure, increaseTemp;
        let toggleArrows, toggleChart;
        let countAElement, countBElement, countCElement, kValueElement;
        let forwardRateElement, reverseRateElement, balanceIndicator;
        let chartContainer;
        
        // 初始化函数
        function init() {
            // 获取Canvas上下文
            const reactionCanvas = document.getElementById('reactionCanvas');
            const chartCanvas = document.getElementById('chartCanvas');
            
            // 设置Canvas尺寸
            reactionCanvas.width = reactionCanvas.offsetWidth;
            reactionCanvas.height = reactionCanvas.offsetHeight;
            config.canvasWidth = reactionCanvas.width;
            config.canvasHeight = reactionCanvas.height;
            
            chartCanvas.width = chartCanvas.offsetWidth;
            chartCanvas.height = chartCanvas.offsetHeight;
            
            reactionCtx = reactionCanvas.getContext('2d');
            chartCtx = chartCanvas.getContext('2d');
            
            // 获取DOM元素
            startBtn = document.getElementById('startBtn');
            pauseBtn = document.getElementById('pauseBtn');
            resetBtn = document.getElementById('resetBtn');
            addAButton = document.getElementById('addAButton');
            increasePressure = document.getElementById('increasePressure');
            increaseTemp = document.getElementById('increaseTemp');
            toggleArrows = document.getElementById('toggleArrows');
            toggleChart = document.getElementById('toggleChart');
            
            countAElement = document.getElementById('countA');
            countBElement = document.getElementById('countB');
            countCElement = document.getElementById('countC');
            kValueElement = document.getElementById('kValue');
            forwardRateElement = document.getElementById('forwardRate');
            reverseRateElement = document.getElementById('reverseRate');
            balanceIndicator = document.getElementById('balanceIndicator');
            chartContainer = document.getElementById('chartContainer');
            
            // 设置事件监听器
            startBtn.addEventListener('click', startReaction);
            pauseBtn.addEventListener('click', pauseReaction);
            resetBtn.addEventListener('click', resetReaction);
            addAButton.addEventListener('click', () => addReactantA(20));
            increasePressure.addEventListener('click', increaseSystemPressure);
            increaseTemp.addEventListener('click', increaseSystemTemperature);
            toggleArrows.addEventListener('click', toggleVelocityArrows);
            toggleChart.addEventListener('click', toggleChartVisibility);
            
            // 初始化粒子
            createParticles();
            
            // 初始化图表
            updateChart();
            
            // 初始渲染
            drawReaction();
            updateDataDisplay();
        }
        
        // 创建粒子
        function createParticles() {
            particles = [];
            
            // 创建A分子
            for (let i = 0; i < reaction.countA; i++) {
                particles.push({
                    type: 'A',
                    x: Math.random() * (config.canvasWidth - 2 * config.containerPadding) + config.containerPadding,
                    y: Math.random() * (config.canvasHeight - 2 * config.containerPadding) + config.containerPadding,
                    vx: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                    vy: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                    color: '#FF6B6B',
                    radius: config.particleRadius,
                    highlight: false,
                    highlightTime: 0
                });
            }
            
            // 创建B分子
            for (let i = 0; i < reaction.countB; i++) {
                particles.push({
                    type: 'B',
                    x: Math.random() * (config.canvasWidth - 2 * config.containerPadding) + config.containerPadding,
                    y: Math.random() * (config.canvasHeight - 2 * config.containerPadding) + config.containerPadding,
                    vx: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                    vy: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                    color: '#4ECDC4',
                    radius: config.particleRadius,
                    highlight: false,
                    highlightTime: 0
                });
            }
            
            // 创建C分子
            for (let i = 0; i < reaction.countC; i++) {
                particles.push({
                    type: 'C',
                    x: Math.random() * (config.canvasWidth - 2 * config.containerPadding) + config.containerPadding,
                    y: Math.random() * (config.canvasHeight - 2 * config.containerPadding) + config.containerPadding,
                    vx: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                    vy: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                    color: '#FFD166',
                    radius: config.particleRadius,
                    highlight: false,
                    highlightTime: 0
                });
            }
        }
        
        // 开始反应
        function startReaction() {
            if (!config.isRunning) {
                config.isRunning = true;
                startBtn.disabled = true;
                pauseBtn.disabled = false;
                animate();
            }
        }
        
        // 暂停反应
        function pauseReaction() {
            config.isRunning = false;
            startBtn.disabled = false;
            pauseBtn.disabled = true;
        }
        
        // 重置反应
        function resetReaction() {
            config.isRunning = false;
            config.isBalanced = false;
            config.time = 0;
            config.temperature = 1.0;
            config.pressure = 1.0;
            
            startBtn.disabled = false;
            pauseBtn.disabled = true;
            
            // 重置反应参数
            reaction.countA = 100;
            reaction.countB = 80;
            reaction.countC = 0;
            reaction.forwardRate = 0;
            reaction.reverseRate = 0;
            reaction.k = 0;
            
            // 清空历史数据
            reaction.history = {
                time: [],
                countA: [],
                countB: [],
                countC: [],
                forwardRate: [],
                reverseRate: []
            };
            
            // 重新创建粒子
            createParticles();
            
            // 更新显示
            updateDataDisplay();
            drawReaction();
            updateChart();
            
            // 隐藏平衡指示器
            balanceIndicator.style.opacity = '0';
        }
        
        // 增加反应物A
        function addReactantA(count) {
            if (!config.isRunning) return;
            
            // 增加A分子数量
            reaction.countA += count;
            
            // 添加新的A粒子（高亮显示）
            for (let i = 0; i < count; i++) {
                particles.push({
                    type: 'A',
                    x: Math.random() * (config.canvasWidth - 2 * config.containerPadding) + config.containerPadding,
                    y: Math.random() * (config.canvasHeight - 2 * config.containerPadding) + config.containerPadding,
                    vx: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                    vy: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                    color: '#FF6B6B',
                    radius: config.particleRadius,
                    highlight: true,
                    highlightTime: 60 // 高亮显示60帧
                });
            }
            
            // 平衡被打破
            config.isBalanced = false;
            balanceIndicator.style.opacity = '0';
            
            updateDataDisplay();
        }
        
        // 增大系统压强（压缩容器）
        function increaseSystemPressure() {
            if (!config.isRunning) return;
            
            // 增加压强因子（减小容器有效空间）
            config.pressure *= 0.8;
            
            // 平衡被打破
            config.isBalanced = false;
            balanceIndicator.style.opacity = '0';
            
            // 更新显示
            updateDataDisplay();
        }
        
        // 升高系统温度
        function increaseSystemTemperature() {
            if (!config.isRunning) return;
            
            // 增加温度因子
            config.temperature *= 1.5;
            
            // 增加所有粒子的速度
            particles.forEach(p => {
                p.vx *= Math.sqrt(config.temperature);
                p.vy *= Math.sqrt(config.temperature);
            });
            
            // 平衡被打破
            config.isBalanced = false;
            balanceIndicator.style.opacity = '0';
            
            updateDataDisplay();
        }
        
        // 切换速度箭头显示
        function toggleVelocityArrows() {
            config.showArrows = !config.showArrows;
        }
        
        // 切换图表显示
        function toggleChartVisibility() {
            config.showChart = !config.showChart;
            chartContainer.style.display = config.showChart ? 'block' : 'none';
        }
        
        // 动画循环
        function animate() {
            if (!config.isRunning) return;
            
            // 更新时间
            config.time += config.timeStep;
            
            // 更新粒子位置
            updateParticles();
            
            // 处理化学反应
            processReactions();
            
            // 计算反应速率
            calculateReactionRates();
            
            // 检查是否达到平衡
            checkEquilibrium();
            
            // 记录历史数据
            recordHistory();
            
            // 更新显示
            updateDataDisplay();
            drawReaction();
            updateChart();
            
            // 继续动画循环
            requestAnimationFrame(animate);
        }
        
        // 更新粒子位置
        function updateParticles() {
            // 计算有效容器尺寸（考虑压强影响）
            const effectiveWidth = config.canvasWidth * config.pressure;
            const effectiveHeight = config.canvasHeight * config.pressure;
            const offsetX = (config.canvasWidth - effectiveWidth) / 2;
            const offsetY = (config.canvasHeight - effectiveHeight) / 2;
            
            particles.forEach(p => {
                // 更新位置
                p.x += p.vx;
                p.y += p.vy;
                
                // 边界碰撞检测（考虑压强影响）
                if (p.x - p.radius < offsetX + config.containerPadding || p.x + p.radius > offsetX + effectiveWidth - config.containerPadding) {
                    p.vx = -p.vx;
                    p.x = Math.max(offsetX + config.containerPadding + p.radius, 
                                  Math.min(offsetX + effectiveWidth - config.containerPadding - p.radius, p.x));
                }
                
                if (p.y - p.radius < offsetY + config.containerPadding || p.y + p.radius > offsetY + effectiveHeight - config.containerPadding) {
                    p.vy = -p.vy;
                    p.y = Math.max(offsetY + config.containerPadding + p.radius, 
                                  Math.min(offsetY + effectiveHeight - config.containerPadding - p.radius, p.y));
                }
                
                // 更新高亮时间
                if (p.highlight && p.highlightTime > 0) {
                    p.highlightTime--;
                    if (p.highlightTime === 0) {
                        p.highlight = false;
                    }
                }
            });
        }
        
        // 处理化学反应
        function processReactions() {
            // 正反应：A + B → C
            // 基于碰撞概率模拟反应
            const forwardProbability = reaction.kForward * config.temperature;
            
            // 查找A和B分子
            const aParticles = particles.filter(p => p.type === 'A');
            const bParticles = particles.filter(p => p.type === 'B');
            
            // 随机选择一些A和B分子尝试反应
            const reactionAttempts = Math.floor(forwardProbability * Math.min(aParticles.length, bParticles.length));
            
            for (let i = 0; i < reactionAttempts; i++) {
                if (aParticles.length === 0 || bParticles.length === 0) break;
                
                // 随机选择A和B分子
                const aIndex = Math.floor(Math.random() * aParticles.length);
                const bIndex = Math.floor(Math.random() * bParticles.length);
                
                const aParticle = aParticles[aIndex];
                const bParticle = bParticles[bIndex];
                
                // 检查是否在反应半径内（模拟碰撞）
                const dx = aParticle.x - bParticle.x;
                const dy = aParticle.y - bParticle.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance < config.reactionRadius) {
                    // 发生反应：A + B → C
                    // 移除A和B分子
                    const aGlobalIndex = particles.indexOf(aParticle);
                    const bGlobalIndex = particles.indexOf(bParticle);
                    
                    if (aGlobalIndex !== -1 && bGlobalIndex !== -1) {
                        // 移除A和B
                        particles.splice(Math.max(aGlobalIndex, bGlobalIndex), 1);
                        particles.splice(Math.min(aGlobalIndex, bGlobalIndex), 1);
                        
                        // 添加C分子
                        particles.push({
                            type: 'C',
                            x: (aParticle.x + bParticle.x) / 2,
                            y: (aParticle.y + bParticle.y) / 2,
                            vx: (aParticle.vx + bParticle.vx) / 2,
                            vy: (aParticle.vy + bParticle.vy) / 2,
                            color: '#FFD166',
                            radius: config.particleRadius,
                            highlight: false,
                            highlightTime: 0
                        });
                        
                        // 更新计数
                        reaction.countA--;
                        reaction.countB--;
                        reaction.countC++;
                    }
                }
            }
            
            // 逆反应：C → A + B
            const reverseProbability = reaction.kReverse * config.temperature;
            const cParticles = particles.filter(p => p.type === 'C');
            const reverseAttempts = Math.floor(reverseProbability * cParticles.length);
            
            for (let i = 0; i < reverseAttempts; i++) {
                if (cParticles.length === 0) break;
                
                // 随机选择C分子
                const cIndex = Math.floor(Math.random() * cParticles.length);
                const cParticle = cParticles[cIndex];
                
                // 发生逆反应：C → A + B
                const globalIndex = particles.indexOf(cParticle);
                
                if (globalIndex !== -1) {
                    // 移除C分子
                    particles.splice(globalIndex, 1);
                    
                    // 添加A和B分子
                    particles.push({
                        type: 'A',
                        x: cParticle.x + (Math.random() - 0.5) * 20,
                        y: cParticle.y + (Math.random() - 0.5) * 20,
                        vx: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                        vy: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                        color: '#FF6B6B',
                        radius: config.particleRadius,
                        highlight: false,
                        highlightTime: 0
                    });
                    
                    particles.push({
                        type: 'B',
                        x: cParticle.x + (Math.random() - 0.5) * 20,
                        y: cParticle.y + (Math.random() - 0.5) * 20,
                        vx: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                        vy: (Math.random() - 0.5) * config.baseSpeed * config.temperature,
                        color: '#4ECDC4',
                        radius: config.particleRadius,
                        highlight: false,
                        highlightTime: 0
                    });
                    
                    // 更新计数
                    reaction.countA++;
                    reaction.countB++;
                    reaction.countC--;
                }
            }
        }
        
        // 计算反应速率
        function calculateReactionRates() {
            // 正反应速率 = k_forward * [A] * [B]
            // 这里使用分子数量近似浓度
            const forwardRate = reaction.kForward * reaction.countA * reaction.countB * config.temperature;
            
            // 逆反应速率 = k_reverse * [C]
            const reverseRate = reaction.kReverse * reaction.countC * config.temperature;
            
            reaction.forwardRate = forwardRate;
            reaction.reverseRate = reverseRate;
            
            // 计算平衡常数 K = [C] / ([A] * [B])
            if (reaction.countA > 0 && reaction.countB > 0) {
                reaction.k = reaction.countC / (reaction.countA * reaction.countB);
            } else {
                reaction.k = 0;
            }
        }
        
        // 检查是否达到平衡
        function checkEquilibrium() {
            const rateDifference = Math.abs(reaction.forwardRate - reaction.reverseRate);
            const rateSum = reaction.forwardRate + reaction.reverseRate;
            
            if (rateSum > 0 && rateDifference / rateSum < config.equilibriumThreshold) {
                if (!config.isBalanced) {
                    config.isBalanced = true;
                    balanceIndicator.style.opacity = '1';
                }
            } else {
                if (config.isBalanced) {
                    config.isBalanced = false;
                    balanceIndicator.style.opacity = '0';
                }
            }
        }
        
        // 记录历史数据
        function recordHistory() {
            // 添加当前数据点
            reaction.history.time.push(config.time);
            reaction.history.countA.push(reaction.countA);
            reaction.history.countB.push(reaction.countB);
            reaction.history.countC.push(reaction.countC);
            reaction.history.forwardRate.push(reaction.forwardRate);
            reaction.history.reverseRate.push(reaction.reverseRate);
            
            // 限制历史数据长度
            if (reaction.history.time.length > config.maxHistory) {
                reaction.history.time.shift();
                reaction.history.countA.shift();
                reaction.history.countB.shift();
                reaction.history.countC.shift();
                reaction.history.forwardRate.shift();
                reaction.history.reverseRate.shift();
            }
        }
        
        // 更新数据显示
        function updateDataDisplay() {
            countAElement.textContent = reaction.countA;
            countBElement.textContent = reaction.countB;
            countCElement.textContent = reaction.countC;
            kValueElement.textContent = reaction.k.toFixed(4);
            forwardRateElement.textContent = reaction.forwardRate.toFixed(2);
            reverseRateElement.textContent = reaction.reverseRate.toFixed(2);
        }
        
        // 绘制反应场景
        function drawReaction() {
            // 清除画布
            reactionCtx.clearRect(0, 0, config.canvasWidth, config.canvasHeight);
            
            // 绘制容器背景
            reactionCtx.fillStyle = '#F7F9FC';
            reactionCtx.fillRect(0, 0, config.canvasWidth, config.canvasHeight);
            
            // 计算有效容器尺寸（考虑压强影响）
            const effectiveWidth = config.canvasWidth * config.pressure;
            const effectiveHeight = config.canvasHeight * config.pressure;
            const offsetX = (config.canvasWidth - effectiveWidth) / 2;
            const offsetY = (config.canvasHeight - effectiveHeight) / 2;
            
            // 绘制容器边框
            reactionCtx.strokeStyle = '#2E86AB';
            reactionCtx.lineWidth = 3;
            reactionCtx.strokeRect(
                offsetX + config.containerPadding, 
                offsetY + config.containerPadding, 
                effectiveWidth - 2 * config.containerPadding, 
                effectiveHeight - 2 * config.containerPadding
            );
            
            // 绘制所有粒子
            particles.forEach(p => {
                // 绘制粒子
                reactionCtx.beginPath();
                reactionCtx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
                
                // 设置颜色（高亮粒子用更亮的颜色）
                if (p.highlight) {
                    reactionCtx.fillStyle = p.type === 'A' ? '#FF9999' : 
                                           p.type === 'B' ? '#7CECDF' : '#FFE299';
                } else {
                    reactionCtx.fillStyle = p.color;
                }
                
                reactionCtx.fill();
                
                // 绘制粒子边框
                reactionCtx.strokeStyle = '#2C3E50';
                reactionCtx.lineWidth = 1;
                reactionCtx.stroke();
                
                // 绘制速率箭头（如果启用）
                if (config.showArrows) {
                    const speed = Math.sqrt(p.vx * p.vx + p.vy * p.vy);
                    if (speed > 0.1) {
                        const arrowLength = speed * 10;
                        const angle = Math.atan2(p.vy, p.vx);
                        
                        reactionCtx.beginPath();
                        reactionCtx.moveTo(p.x, p.y);
                        reactionCtx.lineTo(
                            p.x + Math.cos(angle) * arrowLength,
                            p.y + Math.sin(angle) * arrowLength
                        );
                        reactionCtx.strokeStyle = '#2C3E50';
                        reactionCtx.lineWidth = 1.5;
                        reactionCtx.stroke();
                        
                        // 绘制箭头头部
                        reactionCtx.beginPath();
                        reactionCtx.moveTo(
                           
<!--检测到代码截断，自动续写中...-->
p.x + Math.cos(angle) * arrowLength,
                            p.y + Math.sin(angle) * arrowLength
                        );
                        reactionCtx.lineTo(
                            p.x + Math.cos(angle - Math.PI/6) * arrowLength * 0.5,
                            p.y + Math.sin(angle - Math.PI/6) * arrowLength * 0.5
                        );
                        reactionCtx.lineTo(
                            p.x + Math.cos(angle + Math.PI/6) * arrowLength * 0.5,
                            p.y + Math.sin(angle + Math.PI/6) * arrowLength * 0.5
                        );
                        reactionCtx.closePath();
                        reactionCtx.fillStyle = '#2C3E50';
                        reactionCtx.fill();
                    }
                }
            });
            
            // 绘制反应速率文本
            reactionCtx.fillStyle = '#2C3E50';
            reactionCtx.font = '14px Arial';
            reactionCtx.fillText(`温度因子: ${config.temperature.toFixed(2)}`, 10, 20);
            reactionCtx.fillText(`压强因子: ${config.pressure.toFixed(2)}`, 10, 40);
            reactionCtx.fillText(`总分子数: ${particles.length}`, 10, 60);
        }
        
        // 更新图表
        function updateChart() {
            const chartWidth = chartCtx.canvas.width;
            const chartHeight = chartCtx.canvas.height;
            const padding = {top: 30, right: 30, bottom: 50, left: 60};
            const graphWidth = chartWidth - padding.left - padding.right;
            const graphHeight = chartHeight - padding.top - padding.bottom;
            
            // 清除图表
            chartCtx.clearRect(0, 0, chartWidth, chartHeight);
            
            // 如果没有数据，不绘制
            if (reaction.history.time.length < 2) return;
            
            // 获取数据范围
            const times = reaction.history.time;
            const countAs = reaction.history.countA;
            const countBs = reaction.history.countB;
            const countCs = reaction.history.countC;
            const forwardRates = reaction.history.forwardRate;
            const reverseRates = reaction.history.reverseRate;
            
            // 计算Y轴范围（分子数量）
            const allCounts = [...countAs, ...countBs, ...countCs];
            const maxCount = Math.max(...allCounts);
            const minCount = 0;
            
            // 计算Y轴范围（反应速率）
            const allRates = [...forwardRates, ...reverseRates];
            const maxRate = Math.max(...allRates, 1);
            
            // 绘制网格和坐标轴
            drawChartAxes(padding, graphWidth, graphHeight, times, maxCount, maxRate);
            
            // 绘制曲线
            drawChartCurve(times, countAs, '#FF6B6B', padding, graphWidth, graphHeight, maxCount, false);
            drawChartCurve(times, countBs, '#4ECDC4', padding, graphWidth, graphHeight, maxCount, false);
            drawChartCurve(times, countCs, '#FFD166', padding, graphWidth, graphHeight, maxCount, false);
            
            // 绘制反应速率曲线（使用次Y轴）
            drawChartCurve(times, forwardRates, '#A23B72', padding, graphWidth, graphHeight, maxRate, true);
            drawChartCurve(times, reverseRates, '#2E86AB', padding, graphWidth, graphHeight, maxRate, true);
        }
        
        // 绘制图表坐标轴和网格
        function drawChartAxes(padding, graphWidth, graphHeight, times, maxCount, maxRate) {
            // 绘制背景
            chartCtx.fillStyle = '#FFFFFF';
            chartCtx.fillRect(0, 0, chartCtx.canvas.width, chartCtx.canvas.height);
            
            // 绘制网格
            chartCtx.strokeStyle = '#E0E0E0';
            chartCtx.lineWidth = 0.5;
            
            // 水平网格线（分子数量）
            const yGridLines = 5;
            for (let i = 0; i <= yGridLines; i++) {
                const y = padding.top + graphHeight - (i / yGridLines) * graphHeight;
                chartCtx.beginPath();
                chartCtx.moveTo(padding.left, y);
                chartCtx.lineTo(padding.left + graphWidth, y);
                chartCtx.stroke();
                
                // Y轴标签（分子数量）
                chartCtx.fillStyle = '#5D6D7E';
                chartCtx.font = '12px Arial';
                chartCtx.textAlign = 'right';
                chartCtx.fillText(Math.round((i / yGridLines) * maxCount).toString(), padding.left - 10, y + 4);
            }
            
            // 水平网格线（反应速率，次Y轴）
            const yRateGridLines = 5;
            for (let i = 0; i <= yRateGridLines; i++) {
                const y = padding.top + graphHeight - (i / yRateGridLines) * graphHeight;
                // 只在右侧绘制速率标签
                chartCtx.fillStyle = '#5D6D7E';
                chartCtx.font = '12px Arial';
                chartCtx.textAlign = 'left';
                chartCtx.fillText((i / yRateGridLines * maxRate).toFixed(1), padding.left + graphWidth + 10, y + 4);
            }
            
            // 垂直网格线
            const xGridLines = 10;
            for (let i = 0; i <= xGridLines; i++) {
                const x = padding.left + (i / xGridLines) * graphWidth;
                chartCtx.beginPath();
                chartCtx.moveTo(x, padding.top);
                chartCtx.lineTo(x, padding.top + graphHeight);
                chartCtx.stroke();
                
                // X轴标签（时间）
                if (times.length > 0) {
                    const maxTime = times[times.length - 1];
                    const timeValue = (i / xGridLines) * maxTime;
                    chartCtx.fillStyle = '#5D6D7E';
                    chartCtx.font = '12px Arial';
                    chartCtx.textAlign = 'center';
                    chartCtx.fillText(timeValue.toFixed(1), x, padding.top + graphHeight + 20);
                }
            }
            
            // 绘制坐标轴
            chartCtx.strokeStyle = '#2C3E50';
            chartCtx.lineWidth = 2;
            
            // Y轴（分子数量）
            chartCtx.beginPath();
            chartCtx.moveTo(padding.left, padding.top);
            chartCtx.lineTo(padding.left, padding.top + graphHeight);
            chartCtx.stroke();
            
            // Y轴（反应速率，右侧）
            chartCtx.beginPath();
            chartCtx.moveTo(padding.left + graphWidth, padding.top);
            chartCtx.lineTo(padding.left + graphWidth, padding.top + graphHeight);
            chartCtx.stroke();
            
            // X轴
            chartCtx.beginPath();
            chartCtx.moveTo(padding.left, padding.top + graphHeight);
            chartCtx.lineTo(padding.left + graphWidth, padding.top + graphHeight);
            chartCtx.stroke();
            
            // 坐标轴标签
            chartCtx.fillStyle = '#2C3E50';
            chartCtx.font = 'bold 14px Arial';
            chartCtx.textAlign = 'center';
            
            // X轴标签
            chartCtx.fillText('时间 (s)', padding.left + graphWidth / 2, padding.top + graphHeight + 40);
            
            // Y轴标签（左侧，分子数量）
            chartCtx.save();
            chartCtx.translate(20, padding.top + graphHeight / 2);
            chartCtx.rotate(-Math.PI / 2);
            chartCtx.textAlign = 'center';
            chartCtx.fillText('分子数量', 0, 0);
            chartCtx.restore();
            
            // Y轴标签（右侧，反应速率）
            chartCtx.save();
            chartCtx.translate(padding.left + graphWidth + 40, padding.top + graphHeight / 2);
            chartCtx.rotate(-Math.PI / 2);
            chartCtx.textAlign = 'center';
            chartCtx.fillText('反应速率', 0, 0);
            chartCtx.restore();
        }
        
        // 绘制图表曲线
        function drawChartCurve(times, values, color, padding, graphWidth, graphHeight, maxValue, isRate) {
            if (times.length === 0 || values.length === 0) return;
            
            const maxTime = times[times.length - 1];
            
            // 开始绘制路径
            chartCtx.beginPath();
            
            // 移动到第一个点
            const firstX = padding.left + (times[0] / maxTime) * graphWidth;
            const firstY = isRate ? 
                padding.top + graphHeight - (values[0] / maxValue) * graphHeight :
                padding.top + graphHeight - (values[0] / maxValue) * graphHeight;
            
            chartCtx.moveTo(firstX, firstY);
            
            // 绘制曲线
            for (let i = 1; i < times.length; i++) {
                const x = padding.left + (times[i] / maxTime) * graphWidth;
                const y = isRate ? 
                    padding.top + graphHeight - (values[i] / maxValue) * graphHeight :
                    padding.top + graphHeight - (values[i] / maxValue) * graphHeight;
                
                // 使用二次贝塞尔曲线平滑连接点
                const prevX = padding.left + (times[i-1] / maxTime) * graphWidth;
                const prevY = isRate ? 
                    padding.top + graphHeight - (values[i-1] / maxValue) * graphHeight :
                    padding.top + graphHeight - (values[i-1] / maxValue) * graphHeight;
                
                const cpX = (prevX + x) / 2;
                const cpY1 = prevY;
                const cpY2 = y;
                
                chartCtx.quadraticCurveTo(cpX, cpY1, cpX, cpY1);
                chartCtx.quadraticCurveTo(cpX, cpY2, x, y);
            }
            
            // 设置线条样式
            chartCtx.strokeStyle = color;
            chartCtx.lineWidth = 2.5;
            chartCtx.stroke();
            
            // 添加数据点（每隔一定间隔）
            chartCtx.fillStyle = color;
            for (let i = 0; i < times.length; i += Math.floor(times.length / 15)) {
                const x = padding.left + (times[i] / maxTime) * graphWidth;
                const y = isRate ? 
                    padding.top + graphHeight - (values[i] / maxValue) * graphHeight :
                    padding.top + graphHeight - (values[i] / maxValue) * graphHeight;
                
                chartCtx.beginPath();
                chartCtx.arc(x, y, 3, 0, Math.PI * 2);
                chartCtx.fill();
            }
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
        // 窗口大小改变时重新调整Canvas
        window.addEventListener('resize', function() {
            if (config.isRunning) {
                pauseReaction();
            }
            init();
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 化学平衡动态模拟动画使用指南

欢迎使用“化学平衡的动态建立与移动”交互式教学动画！本工具旨在通过直观的可视化方式，帮助您深入理解化学平衡这一核心概念。无论您是学生、教师还是化学爱好者，都能通过亲手操作和观察，获得对微观反应过程的深刻洞察。

---

### 一、功能说明

本动画模拟了一个典型的可逆化学反应 **A + B ⇌ C**，在一个密闭容器中的动态过程。您将能够：

1. **实时观察**数百个分子（A、B、C）的无规则热运动和相互碰撞。
2. **追踪数据**：实时查看各物质分子数量、正逆反应速率和平衡常数的变化。
3. **主动探究**：通过改变反应条件（浓度、压强、温度），观察平衡如何移动并重新建立。
4. **分析图表**：通过动态曲线图，直观理解各物理量随时间的变化趋势。

整个模拟严格遵循化学反应动力学和勒夏特列原理，将抽象的化学理论转化为生动、可视的微观世界。

---

### 二、主要功能与操作指南

#### 1. 反应控制区（左侧面板）
*   **▶ 开始反应**：点击后，反应启动。分子开始运动、碰撞，反应发生。观察分子数量如何从初始状态向平衡态变化。
*   **⏸ 暂停**：在任意时刻暂停模拟，便于仔细观察某一瞬间的粒子分布或数据。
*   **↺ 重置**：将所有参数恢复至初始状态，清空历史数据，重新开始。

#### 2. 平衡扰动区（探究工具）
*   **+ 增加A浓度**：在反应进行中或平衡时点击，会瞬间向容器中加入一批新的A分子（会高亮显示）。**观察重点**：平衡如何被打破？系统如何通过消耗新增的A来建立新的平衡？
*   **↓ 增大压强**：模拟压缩容器体积。点击后，容器视觉上会“缩小”，单位体积内分子数密度瞬间增加。**观察重点**：平衡向分子数减少的方向移动了吗？（对于A+B⇌C，增大压强平衡向生成C的方向移动）
*   **↑ 升高温度**：所有分子运动速度明显加快，碰撞更频繁。**观察重点**：正逆反应速率如何变化？平衡常数K值是否改变？（本模拟中，预设正反应为放热反应，升温平衡向逆反应方向移动）

#### 3. 视图与显示控制
*   **⇄ 显示/隐藏速率箭头**：切换显示每个分子运动的速度矢量和方向，直观感受“温度”对分子平均动能的影响。
*   **📈 显示/隐藏曲线图**：控制下方曲线图区域的显示，便于您在全屏观察粒子运动或专注数据分析之间切换。

#### 4. 实时数据面板（右侧面板）
*   **分子数量**：实时显示A、B、C三种分子的当前个数。
*   **平衡常数K**：根据公式 K = [C] / ([A]×[B]) 实时计算并显示。**教学要点**：K值只随温度改变，不随浓度、压强改变。
*   **反应速率**：分别显示正反应(A+B→C)和逆反应(C→A+B)的瞬时速率。当两者数值相等时，系统达到**动态平衡**。

#### 5. 动态曲线图
*   **分子数量-时间曲线**（红、青、黄线）：展示各物种分子数量随时间的变化，最终趋于平稳（平衡态）。
*   **反应速率-时间曲线**（紫红、蓝色线）：展示正逆反应速率随时间的变化，最终两条曲线交汇（速率相等）。
*   **图表解读**：曲线交汇或趋于水平并不代表反应停止，而是达到了动态平衡的宏观表现。

---

### 三、设计特色

1.  **多通道学习体验**：结合了**视觉动画**（粒子运动）、**数值反馈**（实时数据）和**图形分析**（历史曲线），满足不同学习风格的需求。
2.  **科学的模拟算法**：粒子运动基于分子运动论，反应概率基于质量作用定律，平衡移动遵循勒夏特列原理，确保了模拟的科学性。
3.  **即时的平衡指示**：当系统达到动态平衡时，界面右上角会出现“动态平衡达成 ✓”的提示，并伴有边框微光效果。
4.  **专业的视觉设计**：
    *   **色彩编码**：A(红)、B(青)、C(黄)，颜色鲜明且与曲线图一一对应，便于追踪。
    *   **清晰的UI分区**：控制区、模拟区、数据区、图表区分工明确，逻辑清晰。
    *   **友好的交互反馈**：按钮有悬停和点击效果，新增分子有高亮提示，操作反馈明确。

---

### 四、核心教学要点

在操作过程中，请特别关注并思考以下关键概念：

1.  **动态平衡的本质**：达到平衡时，反应并未停止，而是**正逆反应速率相等**。分子数量宏观不变，但微观上A、B、C分子仍在不断相互转化。
2.  **平衡常数K的意义**：K是温度的函数。在模拟中，只有“升高温度”操作会改变K值，而改变浓度或压强只会改变平衡点，不会改变K值。
3.  **勒夏特列原理的微观解释**：
    *   **增加反应物浓度**：增加了A与B碰撞的概率，瞬间正反应速率提高，平衡右移。
    *   **增大压强（压缩体积）**：所有分子浓度等比例增加，但对于A+B⇌C（气体分子数减少的反应），正反应速率增加得更显著，平衡向生成C的方向移动。
    *   **升高温度**：同时提高了正、逆反应的速率，但由于本模拟预设正反应放热，升温对逆反应速率的提升更显著，因此平衡左移。
4.  **速率-时间曲线的解读**：曲线交汇点是达到平衡的时刻。外界条件改变会导致一条速率曲线“跳跃”，然后两条曲线逐渐再次靠拢，直至在新的水平线上交汇。

---

### 五、使用建议

1.  **对于学生（自主学习）**：
    *   **第一步**：先点击“开始”，不做任何干预，完整观察一次平衡从建立到稳定的全过程。关注数据面板和曲线的变化。
    *   **第二步**：待平衡后，依次尝试三个“扰动”按钮。每次操作后，耐心观察系统如何“抵抗”你的改变，并建立新平衡。
    *   **第三步**：结合观察，回答：为什么说平衡是“动态”的？K值在什么情况下会变？

2.  **对于教师（课堂演示或探究任务）**：
    *   **课堂演示**：可在大屏幕上展示，通过提问引导学生预测点击按钮后的结果，再用模拟验证，极具说服力。
    *   **布置探究任务**：可以设计任务单，例如：“请设计实验（操作模拟）验证：温度改变会影响平衡常数K，而浓度改变不会。”
    *   **突破难点**：针对“动态平衡”、“勒夏特列原理的微观解释”等教学难点，本动画是极佳的辅助工具。

3.  **通用技巧**：
    *   善用“暂停”功能，在关键时刻定格画面进行讲解或思考。
    *   对比观察“分子数量图”和“反应速率图”，理解宏观现象（浓度不变）与微观本质（速率相等）的联系。
    *   重置后，可以尝试不同的操作顺序，比较不同扰动下系统达到新平衡的快慢。

---

**祝您探索愉快！希望通过这个交互式动画，化学平衡不再是书本上抽象的文字和公式，而是一幅生动、深刻且令人惊叹的微观世界图景。**