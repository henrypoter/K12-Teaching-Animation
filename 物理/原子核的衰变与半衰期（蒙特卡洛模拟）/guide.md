# 需求：原子核的衰变与半衰期（蒙特卡洛模拟）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中或大学低年级的物理、化学或核科学入门学生。用户的核心需求是：
1.  **理解抽象概念**：将“衰变概率”、“半衰期”这类难以直观感受的微观随机过程可视化、动态化。
2.  **建立统计观念**：理解单个原子的衰变是随机的，而大量原子的衰变遵循确定的统计规律（指数衰减）。
3.  **掌握核心定义**：清晰理解“半衰期”的定义——统计意义上，原子数目减半所需的时间。
4.  **体验科学方法**：通过蒙特卡洛模拟（一种基于随机数的计算方法）来再现和探索物理规律，了解计算模拟在现代科学中的作用。
5.  **降低认知门槛**：通过友好的交互和直观的视觉反馈，让学习者主动探索，而非被动接受公式。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念**：
    *   **原子核衰变**：不稳定的原子核随机地发射粒子转变为另一种原子核。
    *   **衰变概率（λ）**：每个原子在单位时间内发生衰变的可能性，是固有属性。
    *   **半衰期（T½）**：大量放射性原子核的数目衰减到初始值一半所需的时间。T½ = ln(2) / λ。
    *   **蒙特卡洛模拟**：利用计算机生成随机数，模拟每个原子在每一时间步长内是否衰变，从而从微观随机行为涌现出宏观统计规律。

*   **认知规律**：
    *   **从具体到抽象**：先展示单个原子的“闪烁”衰变，再观察整体数量的衰减曲线。
    *   **从随机到规律**：强调单个原子的不可预测性和整体行为的可预测性之间的对比。
    *   **从观察到控制**：允许用户调整参数（如原子总数、半衰期），观察结果如何变化，建立因果关系。
    *   **从模拟到理论**：将模拟得到的衰减曲线与理论指数衰减曲线进行对比验证。

*   **交互设计**：
    *   **分层控制**：设计清晰的控制面板，分为“模拟参数设置”、“模拟控制”、“视图切换”。
    *   **即时反馈**：任何参数调整或操作都立即在动画和图表中反映出来。
    *   **探索式学习**：提供“单步执行”功能，让用户仔细体会每一步的随机过程；提供“重置/随机种子”功能，比较不同随机序列下的相同统计结果。
    *   **焦点引导**：通过高亮、注释、动画过渡来引导用户的注意力到关键变化上。

*   **视觉呈现**：
    *   **双视图模式**：
        1.  **微观视图（原子视图）**：用圆点（如发光小球）代表未衰变原子，衰变后变为另一种颜色/灰度的静止圆点或消失，并伴有短暂的视觉特效（如缩小、变色、粒子飞溅）。
        2.  **宏观视图（图表视图）**：实时绘制“未衰变原子数 vs. 时间”的曲线图。同时绘制一条光滑的理论预测曲线进行对比。
    *   **信息可视化**：在图表上动态标记“当前时间”和“当前原子数”，当数量减半时，高亮显示并标注“半衰期 T½”。
    *   **隐喻运用**：可以将原子群比喻为“一群萤火虫”，每隔一段时间随机有萤火虫熄灭，帮助形象化记忆。

#### 配色方案选择
选择清晰、科学且对色盲友好的配色方案，同时区分状态和数据类型。
*   **主背景**：深空蓝或深灰色（`#0d1b2a` 或 `#2b2d42`），营造专注的“实验室”或“宇宙”氛围，并让发光元素更突出。
*   **原子颜色**：
    *   **未衰变原子**：明亮的暖色（如 `#4cc9f0` 青蓝色，或 `#f72585` 玫红色），带有微弱的发光效果，代表活跃状态。
    *   **已衰变原子**：中性暗色（如 `#6c757d` 灰色），或淡绿色（`#90be6d`），表示稳定/结束状态。
*   **图表元素**：
    *   **模拟数据曲线**：亮黄色（`#ffd166`）或青色（`#06d6a0`），清晰醒目。
    *   **理论预测曲线**：白色（`#ffffff`）或浅灰色（`#adb5bd`），带虚线线型，与模拟曲线形成对比。
    *   **坐标轴与网格**：中灰色（`#495057`），半透明。
    *   **半衰期标记线**：红色（`#ef476f`），加粗并闪烁提示。
*   **控制面板**：半透明黑色背景（`rgba(0,0,0,0.7)`），白色文字，按钮使用主色系的变体。

#### 交互功能列表
1.  **模拟参数设置区**：
    *   **初始原子数量**：滑动条（例如，范围 100 - 1000）。
    *   **半衰期 (T½)**：滑动条或输入框（例如，范围 5 - 50 秒或时间步长）。
    *   **时间步长 (Δt)**：滑动条（控制模拟速度与精度）。
2.  **模拟控制区**：
    *   **开始/暂停** 按钮：控制模拟运行。
    *   **单步执行** 按钮：每点击一次，前进一个时间步长。
    *   **重置** 按钮：清除当前模拟，恢复初始设置。
    *   **重置（新随机种子）** 按钮：用新的随机序列重新开始。
3.  **视图控制区**：
    *   **视图切换**：单选按钮或标签页，在“原子视图”、“图表视图”、“并排视图”间切换。
    *   **图表显示切换**：复选框，控制是否显示“理论曲线”。
4.  **动态信息显示区**：
    *   **当前时间**：显示已模拟的时间。
    *   **剩余原子数**：实时计数。
    *   **已衰变原子数**：实时计数。
    *   **当前衰变比例**：显示百分比。
5.  **动画与提示**：
    *   原子衰变时的视觉特效。
    *   当剩余原子数首次低于初始值一半时，在图表上高亮标注第一个“半衰期”点。
    *   鼠标悬停在图表数据点上时，显示精确的（时间，数量）坐标。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>原子核衰变与半衰期 - 蒙特卡洛模拟</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0d1b2a 0%, #1b263b 100%);
            color: #e0e1dd;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .container {
            max-width: 1200px;
            width: 100%;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        header {
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        h1 {
            color: #4cc9f0;
            font-size: 2.2rem;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(76, 201, 240, 0.3);
        }

        .subtitle {
            color: #90be6d;
            font-size: 1.1rem;
            opacity: 0.9;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }

        .simulation-area {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .view-container {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            padding: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .view-title {
            color: #ffd166;
            margin-bottom: 10px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .view-title::before {
            content: "●";
            color: #ffd166;
            font-size: 0.8rem;
        }

        #atomCanvas {
            background: rgba(13, 27, 42, 0.8);
            border-radius: 10px;
            width: 100%;
            height: 400px;
            display: block;
        }

        #chartCanvas {
            background: rgba(13, 27, 42, 0.8);
            border-radius: 10px;
            width: 100%;
            height: 400px;
            display: block;
        }

        .controls-panel {
            flex: 0 0 320px;
            background: rgba(0, 0, 0, 0.5);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .panel-section {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 15px;
        }

        .section-title {
            color: #4cc9f0;
            margin-bottom: 15px;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .section-title::before {
            content: "▶";
            font-size: 0.8rem;
        }

        .control-group {
            margin-bottom: 15px;
        }

        .control-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
            font-size: 0.95rem;
        }

        .value-display {
            color: #ffd166;
            font-weight: bold;
        }

        input[type="range"] {
            width: 100%;
            height: 6px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 3px;
            outline: none;
            -webkit-appearance: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: #4cc9f0;
            cursor: pointer;
            box-shadow: 0 0 5px rgba(76, 201, 240, 0.8);
        }

        .button-group {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-top: 10px;
        }

        button {
            padding: 12px 15px;
            border: none;
            border-radius: 8px;
            background: linear-gradient(135deg, #4cc9f0 0%, #3a86ff 100%);
            color: white;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(76, 201, 240, 0.4);
        }

        button:active {
            transform: translateY(0);
        }

        button.secondary {
            background: linear-gradient(135deg, #90be6d 0%, #43aa8b 100%);
        }

        button.secondary:hover {
            box-shadow: 0 5px 15px rgba(144, 190, 109, 0.4);
        }

        button.warning {
            background: linear-gradient(135deg, #f72585 0%, #b5179e 100%);
        }

        button.warning:hover {
            box-shadow: 0 5px 15px rgba(247, 37, 133, 0.4);
        }

        .stats-display {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }

        .stat-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            padding: 12px;
            text-align: center;
        }

        .stat-value {
            font-size: 1.8rem;
            font-weight: bold;
            color: #ffd166;
            margin: 5px 0;
        }

        .stat-label {
            font-size: 0.9rem;
            color: #adb5bd;
        }

        .view-toggle {
            display: flex;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            padding: 5px;
            margin-top: 10px;
        }

        .view-toggle button {
            flex: 1;
            padding: 8px;
            background: transparent;
            border-radius: 6px;
            font-size: 0.9rem;
        }

        .view-toggle button.active {
            background: rgba(76, 201, 240, 0.2);
            color: #4cc9f0;
        }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 10px;
        }

        input[type="checkbox"] {
            width: 18px;
            height: 18px;
            accent-color: #4cc9f0;
        }

        .legend {
            display: flex;
            gap: 15px;
            margin-top: 10px;
            flex-wrap: wrap;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 0.9rem;
        }

        .legend-color {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }

        .info-panel {
            background: rgba(239, 71, 111, 0.1);
            border-left: 4px solid #ef476f;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
            font-size: 0.95rem;
            line-height: 1.5;
        }

        .info-panel strong {
            color: #ef476f;
        }

        footer {
            text-align: center;
            padding: 20px;
            color: #6c757d;
            font-size: 0.9rem;
            margin-top: 20px;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .controls-panel {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>原子核衰变与半衰期</h1>
            <p class="subtitle">蒙特卡洛模拟 - 探索微观随机性与宏观统计规律</p>
        </header>

        <div class="main-content">
            <div class="simulation-area">
                <div class="view-container">
                    <div class="view-title">微观视图：原子衰变过程</div>
                    <canvas id="atomCanvas"></canvas>
                    <div class="legend">
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #4cc9f0;"></div>
                            <span>未衰变原子</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #90be6d;"></div>
                            <span>已衰变原子</span>
                        </div>
                    </div>
                </div>

                <div class="view-container">
                    <div class="view-title">宏观视图：衰变统计曲线</div>
                    <canvas id="chartCanvas"></canvas>
                    <div class="legend">
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #ffd166;"></div>
                            <span>模拟数据曲线</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #ffffff;"></div>
                            <span>理论预测曲线</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #ef476f;"></div>
                            <span>半衰期标记</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="controls-panel">
                <div class="panel-section">
                    <div class="section-title">模拟参数设置</div>
                    
                    <div class="control-group">
                        <div class="control-label">
                            <span>初始原子数量</span>
                            <span class="value-display" id="atomCountValue">500</span>
                        </div>
                        <input type="range" id="atomCount" min="100" max="1000" step="50" value="500">
                    </div>

                    <div class="control-group">
                        <div class="control-label">
                            <span>半衰期 (T½)</span>
                            <span class="value-display" id="halfLifeValue">20</span>
                        </div>
                        <input type="range" id="halfLife" min="5" max="50" step="1" value="20">
                    </div>

                    <div class="control-group">
                        <div class="control-label">
                            <span>时间步长 (Δt)</span>
                            <span class="value-display" id="timeStepValue">0.5</span>
                        </div>
                        <input type="range" id="timeStep" min="0.1" max="2" step="0.1" value="0.5">
                    </div>
                </div>

                <div class="panel-section">
                    <div class="section-title">模拟控制</div>
                    <div class="button-group">
                        <button id="startBtn">
                            <span>▶</span> 开始
                        </button>
                        <button id="stepBtn" class="secondary">
                            <span>⏯</span> 单步执行
                        </button>
                        <button id="resetBtn" class="secondary">
                            <span>↻</span> 重置
                        </button>
                        <button id="randomBtn" class="warning">
                            <span>🎲</span> 新随机种子
                        </button>
                    </div>
                </div>

                <div class="panel-section">
                    <div class="section-title">视图控制</div>
                    <div class="view-toggle">
                        <button id="viewAtom" class="active">原子视图</button>
                        <button id="viewChart">图表视图</button>
                        <button id="viewBoth">并排视图</button>
                    </div>
                    <div class="checkbox-group">
                        <input type="checkbox" id="showTheory" checked>
                        <label for="showTheory">显示理论预测曲线</label>
                    </div>
                </div>

                <div class="panel-section">
                    <div class="section-title">实时数据</div>
                    <div class="stats-display">
                        <div class="stat-item">
                            <div class="stat-value" id="currentTime">0.0</div>
                            <div class="stat-label">当前时间</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="remainingAtoms">500</div>
                            <div class="stat-label">剩余原子数</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="decayedAtoms">0</div>
                            <div class="stat-label">已衰变原子数</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="decayPercent">0%</div>
                            <div class="stat-label">衰变比例</div>
                        </div>
                    </div>
                </div>

                <div class="info-panel">
                    <strong>教学提示：</strong> 观察单个原子的随机衰变如何产生整体的指数衰减规律。调整半衰期参数，观察曲线变化。注意第一个半衰期标记（红色线）出现时，剩余原子数正好减半。
                </div>
            </div>
        </div>

        <footer>
            <p>蒙特卡洛模拟 | 原子核衰变与半衰期 | 教育技术演示</p>
        </footer>
    </div>

    <script>
        // 全局变量
        let simulation = {
            atoms: [],
            decayedAtoms: [],
            time: 0,
            isRunning: false,
            animationId: null,
            halfLife: 20,
            timeStep: 0.5,
            atomCount: 500,
            decayConstant: 0,
            dataPoints: [],
            randomSeed: Math.random(),
            firstHalfLifeMarked: false
        };

        // DOM 元素
        const atomCanvas = document.getElementById('atomCanvas');
        const chartCanvas = document.getElementById('chartCanvas');
        const atomCtx = atomCanvas.getContext('2d');
        const chartCtx = chartCanvas.getContext('2d');

        // 控制元素
        const atomCountSlider = document.getElementById('atomCount');
        const halfLifeSlider = document.getElementById('halfLife');
        const timeStepSlider = document.getElementById('timeStep');
        const startBtn = document.getElementById('startBtn');
        const stepBtn = document.getElementById('stepBtn');
        const resetBtn = document.getElementById('resetBtn');
        const randomBtn = document.getElementById('randomBtn');
        const showTheoryCheckbox = document.getElementById('showTheory');
        const viewAtomBtn = document.getElementById('viewAtom');
        const viewChartBtn = document.getElementById('viewChart');
        const viewBothBtn = document.getElementById('viewBoth');

        // 数据显示元素
        const atomCountValue = document.getElementById('atomCountValue');
        const halfLifeValue = document.getElementById('halfLifeValue');
        const timeStepValue = document.getElementById('timeStepValue');
        const currentTimeDisplay = document.getElementById('currentTime');
        const remainingAtomsDisplay = document.getElementById('remainingAtoms');
        const decayedAtomsDisplay = document.getElementById('decayedAtoms');
        const decayPercentDisplay = document.getElementById('decayPercent');

        // 初始化 Canvas 尺寸
        function initCanvasSize() {
            const container = atomCanvas.parentElement;
            const width = container.clientWidth - 30;
            
            atomCanvas.width = width;
            atomCanvas.height = 400;
            
            chartCanvas.width = width;
            chartCanvas.height = 400;
        }

        // 初始化原子
        function initAtoms() {
            simulation.atoms = [];
            simulation.decayedAtoms = [];
            simulation.dataPoints = [];
            simulation.time = 0;
            simulation.firstHalfLifeMarked = false;
            
            // 计算衰变常数 λ = ln(2) / T½
            simulation.decayConstant = Math.log(2) / simulation.halfLife;
            
            const width = atomCanvas.width;
            const height = atomCanvas.height;
            const padding = 20;
            
            // 创建未衰变原子
            for (let i = 0; i < simulation.atomCount; i++) {
                simulation.atoms.push({
                    x: padding + Math.random() * (width - 2 * padding),
                    y: padding + Math.random() * (height - 2 * padding),
                    radius: 4,
                    color: '#4cc9f0',
                    decayTime: null,
                    isDecayed: false,
                    id: i
                });
            }
            
            // 添加初始数据点
            simulation.dataPoints.push({
                time: 0,
                count: simulation.atomCount,
                theoretical: simulation.atomCount
            });
            
            updateDisplays();
        }

        // 执行一个时间步长的模拟
        function simulateStep() {
            if (simulation.atoms.length === 0) return;
            
            simulation.time += simulation.timeStep;
            
            // 计算每个原子在这一步长内的衰变概率
            const decayProbability = 1 - Math.exp(-simulation.decayConstant * simulation.timeStep);
            
            // 标记要衰变的原子
            const atomsToDecay = [];
            for (let i = 0; i < simulation.atoms.length; i++) {
                if (!simulation.atoms[i].isDecayed && Math.random() < decayProbability) {
                    atomsToDecay.push(i);
                }
            }
            
            // 处理衰变原子
            atomsToDecay.sort((a, b) => b - a); // 从后往前删除
            for (const index of atomsToDecay) {
                const atom = simulation.atoms[index];
                atom.isDecayed = true;
                atom.decayTime = simulation.time;
                atom.color = '#90be6d';
                
                // 移动到已衰变数组
                simulation.decayedAtoms.push(atom);
                simulation.atoms.splice(index, 1);
            }
            
            // 记录数据点
            const currentCount = simulation.atoms.length;
            const theoreticalCount = simulation.atomCount * Math.exp(-simulation.decayConstant * simulation.time);
            
            simulation.dataPoints.push({
                time: simulation.time,
                count: currentCount,
                theoretical: theoreticalCount
            });
            
            // 检查是否达到半衰期
            if (!simulation.firstHalfLifeMarked && currentCount <= simulation.atomCount / 2) {
                simulation.firstHalfLifeMarked = true;
                // 可以添加视觉反馈
            }
            
            updateDisplays();
        }

        // 更新数据显示
        function updateDisplays() {
            currentTimeDisplay.textContent = simulation.time.toFixed(1);
            remainingAtomsDisplay.textContent = simulation.atoms.length;
            decayedAtomsDisplay.textContent = simulation.decayedAtoms.length;
            
            const decayPercent = (simulation.decayedAtoms.length / simulation.atomCount * 100).toFixed(1);
            decayPercentDisplay.textContent = `${decayPercent}%`;
        }

        // 绘制原子视图
        function drawAtomView() {
            const ctx = atomCtx;
            const width = atomCanvas.width;
            const height = atomCanvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制背景
            ctx.fillStyle = '#0d1b2a';
            ctx.fillRect(0, 0, width, height);
            
            // 绘制网格
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.05)';
            ctx.lineWidth = 1;
            const gridSize = 40;
            
            for (let x = 0; x < width; x += gridSize) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, height);
                ctx.stroke();
            }
            
            for (let y = 0; y < height; y += gridSize) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(width, y);
                ctx.stroke();
            }
            
            // 绘制已衰变原子
            for (const atom of simulation.decayedAtoms) {
                ctx.beginPath();
                ctx.arc(atom.x, atom.y, atom.radius, 0, Math.PI * 2);
                ctx.fillStyle = atom.color;
                ctx.fill();
                
                // 添加微弱的发光效果
                ctx.beginPath();
                ctx.arc(atom.x, atom.y, atom.radius + 2, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(144, 190, 109, 0.2)';
                ctx.fill();
            }
            
            // 绘制未衰变原子（带发光效果）
            for (const atom of simulation.atoms) {
                // 发光效果
                const gradient = ctx.createRadialGradient(
                    atom.x, atom.y, 0,
                    atom.x, atom.y, atom.radius + 3
                );
                gradient.addColorStop(0, 'rgba(76, 201, 240, 0.8)');
                gradient.addColorStop(1, 'rgba(76, 201, 240, 0)');
                
                ctx.beginPath();
                ctx.arc(atom.x, atom.y, atom.radius + 3, 0, Math.PI * 2);
                ctx.fillStyle = gradient;
                ctx.fill();
                
                // 原子核心
                ctx.beginPath();
                ctx.arc(atom.x, atom.y, atom.radius, 0, Math.PI * 2);
                ctx.fillStyle = atom.color;
                ctx.fill();
            }
            
            // 绘制标题
            ctx.fillStyle = '#ffd166';
            ctx.font = '14px Arial';
            ctx.fillText(`未衰变原子: ${simulation.atoms.length}`, 10, 20);
            ctx.fillText(`时间: ${simulation.time.toFixed(1)}`, 10, 40);
        }

        // 绘制图表视图
        function drawChartView() {
            const ctx = chartCtx;
            const width = chartCanvas.width;
            const height = chartCanvas.height;
            const padding = { top: 40, right: 20, bottom: 40, left: 60 };
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制背景
            ctx.fillStyle = '#0d1b2a';
            ctx.fillRect(0, 0, width, height);
            
            // 计算坐标轴范围
            const maxTime = Math.max(simulation.time, simulation.halfLife * 3);
            const maxCount = simulation.atomCount;
            
            // 坐标转换函数
            const toX = (time) => padding.left + (time / maxTime) * (width - padding.left - padding.right);
            const toY = (count) => padding.top + (1 - count / maxCount) * (height - padding.top - padding.bottom);
            
            // 绘制网格
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.1)';
            ctx.lineWidth = 1;
            ctx.font = '12px Arial';
            ctx.fillStyle = '#adb5bd';
            
            // 水平网格线（数量）
            for (let i = 0; i <= 10; i++) {
                const count = (maxCount * i / 10);
                const y = toY(count);
                
                ctx.beginPath();
                ctx.moveTo(padding.left, y);
                ctx.lineTo(width - padding.right, y);
                ctx.stroke();
                
                ctx.fillText(Math.round(count).toString(), 5, y + 4);
            }
            
            // 垂直网格线（时间）
            for (let i = 0; i <= 10; i++) {
                const time = (maxTime * i / 10);
                const x = toX(time);
                
                ctx.beginPath();
                ctx.moveTo(x, padding.top);
                ctx.lineTo(x, height - padding.bottom);
                ctx.stroke();
                
                ctx.fillText(time.toFixed(1), x - 10, height - padding.bottom + 20);
            }
            
            // 绘制坐标轴
            ctx.strokeStyle = '#ffffff';
            ctx.lineWidth = 2;
            
            // Y轴
            ctx.beginPath();
            ctx.moveTo(padding.left, padding.top);
            ctx.lineTo(padding.left, height - padding.bottom);
            ctx.stroke();
            
            // X轴
            ctx.beginPath();
            ctx.moveTo(padding.left, height - padding.bottom);
            ctx.lineTo(width - padding.right, height - padding.bottom);
            ctx.stroke();
            
            // 轴标签
            ctx.fillStyle = '#ffffff';
            ctx.font = '14px Arial';
            ctx.fillText('原子数量', 10, padding.top - 10);
            ctx.fillText('时间', width - padding.right, height - padding.bottom + 30);
            
            // 绘制理论曲线（如果启用）
            if (showTheoryCheckbox.checked) {
                ctx.beginPath();
                ctx.strokeStyle = '#ffffff';
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 5]);
                
                for (let t = 0; t <= maxTime; t += maxTime / 100) {
                    const count = simulation.atomCount * Math.exp(-simulation.decayConstant * t);
                    const x = toX(t);
                    const y = toY(count);
                    
                    if (t === 0) {
                        ctx.moveTo(x, y);
                    } else {
                        ctx.lineTo(x, y);
                    }
                }
                ctx.stroke();
                ctx.setLineDash([]);
            }
            
            // 绘制模拟数据曲线
            if (simulation.dataPoints.length > 0) {
                ctx.beginPath();
                ctx.strokeStyle = '#ffd166';
                ctx.lineWidth = 3;
                ctx.lineJoin = 'round';
                
                for (let i = 0; i < simulation.dataPoints.length; i++) {
                    const point = simulation.dataPoints[i];
                    const x = toX(point.time);
                    const y = toY(point.count);
                    
                    if (i === 0) {
                        ctx.moveTo(x, y);
                    } else {
                        ctx.lineTo(x, y);
                    }
                }
                ctx.stroke();
                
                // 绘制数据点
                for (const point of simulation.dataPoints) {
                    const x = toX(point.time);
                    const y = toY(point.count);
                    
                    ctx.beginPath();
                    ctx.arc(x, y, 3, 0, Math.PI * 2);
                    ctx.fillStyle = '#ffd166';
                    ctx.fill();
                }
            }
            
            // 绘制半衰期标记
            if (simulation.firstHalfLifeMarked) {
                const halfLifeX = toX(simulation.halfLife);
                
                // 垂直线
                ctx.beginPath();
                ctx.strokeStyle = '#ef476f';
                ctx.lineWidth = 2;
                ctx.setLineDash([3, 3]);
                ctx.moveTo(halfLifeX, padding.top);
                ctx.lineTo(halfLifeX, height - padding.bottom);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 标签
                ctx.fillStyle = '#ef476f';
                ctx.font = 'bold 14px Arial';
                ctx.fillText(`T½ = ${simulation.halfLife}`, halfLifeX + 5, padding.top + 20);
                
                // 水平线标记一半数量
                const halfY = toY(simulation.atomCount / 2);
                ctx.beginPath();
                ctx.moveTo(padding.left, halfY);
                ctx.lineTo(halfLifeX, halfY);
                ctx.strokeStyle = '#ef476f';
                ctx.lineWidth = 1;
                ctx.setLineDash([2, 2]);
                ctx.stroke();
                ctx.setLineDash([]);
            }
            
            // 绘制当前时间标记
            if (simulation.time > 0) {
                const currentX = toX(simulation.time);
                const currentY = toY(simulation.atoms.length);
                
                // 垂直线
                ctx.beginPath();
                ctx.strokeStyle = '#4cc9f0';
                ctx.lineWidth = 1;
                ctx.setLineDash([2, 2]);
                ctx.moveTo(currentX, padding.top);
                ctx.lineTo(currentX, height - padding.bottom);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 数据点
                ctx.beginPath();
                ctx.arc(currentX, currentY, 6, 0, Math.PI * 2);
                ctx.fillStyle = '#4cc9f0';
                ctx.fill();
                
                // 标签
                ctx.fillStyle = '#4cc9f0';
                ctx.font = '12px Arial';
                ctx.fillText(`当前: ${simulation.atoms.length}`, currentX + 10, currentY - 10);
            }
        }

        // 动画循环
        function animate() {
            if (simulation.isRunning) {
                simulateStep();
            }
            
            // 根据当前视图模式绘制
            const atomView = document.querySelector('.view-container:nth-child(1)');
            const chartView = document.querySelector('.view-container:nth-child(2)');
            
            if (viewAtomBtn.classList.contains('active')) {
                atomView.style.display = 'block';
                chartView.style.display = 'none';
                drawAtomView();
            } else if (viewChartBtn.classList.contains('active')) {
                atomView.style.display = 'none';
                chartView.style.display = 'block';
                drawChartView();
            } else {
                atomView.style.display = 'block';
                chartView.style.display = 'block';
                drawAtomView();
                drawChartView();
            }
            
            simulation.animationId = requestAnimationFrame(animate);
        }

        // 事件监听器
        atomCountSlider.addEventListener('input', function() {
            simulation.atomCount = parseInt(this.value);
            atomCountValue.textContent = simulation.atomCount;
            if (!simulation.isRunning) {
                initAtoms();
            }
        });

        halfLifeSlider.addEventListener('input', function() {
            simulation.halfLife = parseInt(this.value);
            halfLifeValue.textContent = simulation.halfLife;
            simulation.decayConstant = Math.log(2) / simulation.halfLife;
        });

        timeStepSlider.addEventListener('input', function() {
            simulation.timeStep = parseFloat(this.value);
            timeStepValue.textContent = simulation.timeStep.toFixed(1);
        });

        startBtn.addEventListener('click', function() {
            simulation.isRunning = !simulation.isRunning;
            if (simulation.isRunning) {
                startBtn.innerHTML = '<span>⏸</span> 暂停';
                startBtn.style.background = 'linear-gradient(135deg, #f72585 0%, #b5179e 100%)';
            } else {
                startBtn.innerHTML = '<span>▶</span> 继续';
                startBtn.style.background = 'linear-gradient(135deg, #4cc9f0 0%, #3a86ff 100%)';
            }
        });

        stepBtn.addEventListener('click', function() {
            if (!simulation.isRunning) {
                simulateStep();
            }
        });

        resetBtn.addEventListener('click', function() {
            simulation.isRunning = false;
            startBtn.innerHTML = '<span>▶</span> 开始';
            startBtn.style.background = 'linear-gradient(135deg, #4cc9f0 0%, #3a86ff 100%)';
            initAtoms();
        });

        randomBtn.addEventListener('click', function() {
            simulation.randomSeed = Math.random();
            simulation.isRunning = false;
            startBtn.innerHTML = '<span>▶</span> 开始';
            startBtn.style.background = 'linear-gradient(135deg, #4cc9f0 0%, #3a86ff 100%)';
            initAtoms();
            
            // 添加视觉反馈
            randomBtn.style.transform = 'scale(0.95)';
            setTimeout(() => {
                randomBtn.style.transform = '';
            }, 200);
        });

        // 视图切换
        viewAtomBtn.addEventListener('click', function() {
            viewAtomBtn.classList.add('active');
            viewChartBtn.classList.remove('active');
            viewBothBtn.classList.remove('active');
        });

        viewChartBtn.addEventListener('click', function() {
            viewAtomBtn.classList.remove('active');
            viewChartBtn.classList.add('active');
            viewBothBtn.classList.remove('active');
        });

        viewBothBtn.addEventListener('click', function() {
            viewAtomBtn.classList.remove('active');
            viewChartBtn.classList.remove('active');
            viewBothBtn.classList.add('active');
        });

        // 窗口大小调整
        window.addEventListener('resize', function() {
            initCanvasSize();
            if (!simulation.isRunning) {
                drawAtomView();
                drawChartView();
            }
        });

        // 初始化
        function init() {
            initCanvasSize();
            initAtoms();
            animate();
            
            // 设置初始值显示
            atomCountValue.textContent = simulation.atomCount;
            halfLifeValue.textContent = simulation.halfLife;
            timeStepValue.textContent = simulation.timeStep.toFixed(1);
        }

        // 启动应用
        init();
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 原子核衰变与半衰期 - 蒙特卡洛模拟使用指南

欢迎使用这款交互式教学动画！本工具旨在通过直观的蒙特卡洛模拟，帮助您深入理解原子核衰变的微观随机性与宏观统计规律。无论您是学生、教师还是科学爱好者，都能通过亲手操作，亲眼见证物理规律的涌现。

---

### 🎯 核心目标
- **可视化抽象概念**：将“衰变概率”、“半衰期”等难以捉摸的微观过程，转化为清晰可见的动态图像。
- **连接随机与确定**：体验单个原子的**随机衰变**如何汇聚成整体**确定的指数衰减规律**。
- **掌握科学方法**：学习如何运用**蒙特卡洛模拟**（一种基于随机数的计算方法）来研究和验证物理理论。

---

### 🕹️ 主要功能与操作说明

#### 1. **模拟参数设置区**
   这是您控制“虚拟实验”的起点。
   - **初始原子数量 (100-1000)**：滑动条调整模拟的原子总数。数量越多，统计规律越平滑，但计算负荷也越大。
   - **半衰期 T½ (5-50 时间单位)**：设定原子核衰变的快慢。**半衰期越短，衰变越快**，曲线下降越陡峭。
   - **时间步长 Δt (0.1-2)**：控制模拟的“帧速率”。步长越小，模拟越精细、越慢；步长越大，模拟越快、但可能跳过细节。

#### 2. **模拟控制区**
   控制模拟的“播放”、“暂停”与“重置”。
   - **开始/暂停 (▶/⏸)**：启动或暂停连续模拟。观察动态过程时使用。
   - **单步执行 (⏯)**：每点击一次，模拟前进一个时间步长。**强烈推荐**在初次学习时使用，以便仔细观察每一步的随机衰变过程。
   - **重置 (↻)**：清空当前模拟，用**相同的随机种子**重新开始。用于重复实验。
   - **新随机种子 (🎲)**：用**全新的随机序列**重新开始。用于对比**相同参数、不同随机性**下的结果，验证统计规律的一致性。

#### 3. **视图控制区**
   切换您观察模拟的“镜头”。
   - **原子视图**：聚焦于**微观世界**。每个发光青蓝色（`#4cc9f0`）圆点代表一个未衰变原子，变为绿色（`#90be6d`）表示已衰变。观察它们的随机“闪烁”熄灭。
   - **图表视图**：聚焦于**宏观数据**。绘制剩余原子数随时间变化的曲线。
   - **并排视图**：同时观察微观与宏观，**这是理解两者联系的最佳模式**。
   - **显示理论预测曲线**：勾选后，图表上会叠加一条白色的虚线，表示理论预测的指数衰减曲线。将**模拟结果（黄色实线）与理论（白色虚线）对比**，是验证模拟准确性的关键。

#### 4. **实时数据面板**
   为您提供精确的量化反馈。
   - **当前时间**：模拟已进行的时间。
   - **剩余/已衰变原子数**：最核心的数据。
   - **衰变比例**：直观显示已衰变原子的百分比。

---

### ✨ 设计特色与教学要点

1.  **双重视角，建立联系**
    - **微观视图**让您感受**不确定性**——无法预测下一个衰变的是哪个原子。
    - **图表视图**让您看到**确定性**——整体曲线光滑地遵循指数衰减。
    - **教学要点**：引导学习者思考“个体的随机性如何导致整体的规律性？”这一核心问题。

2.  **动态标记，突出重点**
    - 当剩余原子数首次降至初始值一半时，图表会动态生成一条**红色标记线（T½）**，并标注数值。
    - **教学要点**：这正是**半衰期定义**的直观体现。可以暂停在此刻，强调“一半”的概念。

3.  **参数探索，发现规律**
    - 鼓励您大胆调整**半衰期**参数。
    - **操作建议**：先设 T½=20，运行模拟；再改为 T½=5 重新运行。观察图表曲线陡峭度的显著变化。
    - **教学要点**：半衰期是放射性核素的“身份证”，决定了其衰变速率。

4.  **理论对照，深化理解**
    - 开启“理论曲线”后，您会发现模拟的黄色数据点紧密围绕在白色理论曲线周围。
    - **教学要点**：这说明蒙特卡洛模拟作为一种**数值方法**，可以很好地逼近**解析理论（N(t)=N₀e^(-λt)）**。差异源于统计涨落，原子数越多，吻合度越好。

---

### 🧪 推荐学习路径（使用建议）

**第一步：初次接触**
1.  保持默认参数（原子数500，T½=20）。
2.  切换到**并排视图**，打开**理论曲线**显示。
3.  点击 **“单步执行”** 5-10次，仔细观察：左侧有哪些原子衰变了？右侧图表上的点如何移动？

**第二步：观察连续过程**
1.  点击 **“开始”**，让模拟连续运行。
2.  专注观看图表，等待**第一条红色半衰期标记线**出现。
3.  暂停，检查此时“剩余原子数”是否接近250（500的一半）。理解半衰期的定义。

**第三步：探索与验证**
1.  点击 **“新随机种子”** 重置，然后再次 **“开始”**。
2.  **问自己**：这次的衰变序列和上次一样吗？最终的曲线形状一样吗？半衰期出现的时间点一样吗？
3.  **答案**：序列不同（随机性），曲线形状高度相似（统计规律），半衰期时间点几乎相同（确定性）。

**第四步：参数实验**
1.  将**半衰期调整为5**，其他不变，重新开始模拟。
2.  观察曲线如何以快得多的速度下降，并在更短的时间出现半衰期标记。
3.  尝试增加**原子数量到1000**，观察曲线相比500时是否更平滑、与理论曲线贴合得更好。

**第五步：高阶思考**
- 尝试设置一个**极短的时间步长（如0.1）** 和一个**极长的时间步长（如2）** 分别运行。思考时间步长对模拟精度和效率的影响。
- 在模拟运行时，**动态拖动“半衰期”滑动条**，观察曲线如何实时响应变化。这直观展示了参数λ对衰变过程的直接影响。

---

### 💡 给教师的课堂整合建议

- **演示环节**：全屏运行动画，使用“单步执行”逐步引导学生观察，在关键节点（如达到半衰期）暂停提问。
- **探究任务**：为学生设置挑战，例如：“请通过调整参数，模拟出一种在30秒内衰变掉75%的核素。”
- **概念巩固**：在模拟后，要求学生用自己的话解释：为什么单个原子的衰变是随机的，但我们却能预测一堆原子的衰变行为？

希望本工具能成为您探索微观世界奥秘的得力助手。科学的美，在于从混沌中发现秩序。祝您探索愉快！