# 需求：简谐运动的波形图与圆周运动投影关系

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中物理或大学基础物理的学生。用户的核心需求是直观、动态地理解“简谐运动是匀速圆周运动在直径上的投影”这一抽象且关键的概念。他们可能面临的认知难点包括：
1.  **空间想象困难**：难以在脑海中同时构建旋转的圆周运动和水平/垂直的投影运动。
2.  **相位与初相位的抽象性**：不理解相位角 `(ωt + φ)` 在圆周运动和波形图中的物理意义与对应关系。
3.  **波形图生成的动态过程**：不理解波形图（位移-时间图像）是如何随着时间“绘制”出来的，以及图像上每个点与圆周运动状态的对应关系。
因此，动画的核心价值在于将这三个过程**同步、可视化、可交互地**呈现出来，将抽象数学关系转化为直观的视觉体验。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念**：
    1.  **对应关系**：匀速圆周运动的质点，其某一坐标轴（如x轴）上的投影运动是简谐运动。
    2.  **参数映射**：
        *   圆周半径 `R` <-> 简谐运动振幅 `A`。
        *   圆周角速度 `ω` <-> 简谐运动角频率 `ω`。
        *   圆周运动的相位角 `(ωt + φ)` <-> 简谐运动的相位 `(ωt + φ)`。
        *   圆周运动的初始相位 `φ` <-> 简谐运动的初相 `φ`。
    3.  **波形图生成**：投影质点的位移随时间变化，在右侧的坐标系中连续描点，形成正弦/余弦曲线（波形图）。

*   **认知规律与交互设计**：
    1.  **分层呈现，由静到动**：
        *   **初始状态**：展示静止的圆周、投影点、初始相位角φ、振幅A。用户可先观察静态关系。
        *   **单步运动**：提供“单步”按钮，让圆周运动一个微小角度，同步更新投影点位置，并在波形图区域绘制一个对应的点。此模式帮助用户理解“点对点”的对应关系。
        *   **连续运动**：提供“播放/暂停”按钮，让动画连续运行，直观展示波形被“绘制”出来的全过程。
    2.  **聚焦与关联**：
        *   **高亮与连线**：当前圆周上的质点、其在直径上的投影点、以及波形图上正在绘制的点，三者之间用醒目的颜色连线或高亮显示，强化视觉关联。
        *   **关键参数可视化**：实时显示当前相位角 `(ωt + φ)` 的数值和图示（圆周上的角度），并在波形图对应的点上显示时间 `t` 和位移 `x`。
    3.  **探索与验证**：
        *   **交互控制**：允许用户拖动调整参数，如**振幅A（半径R）**、**角频率ω**、**初相位φ**，并实时观察圆周运动、投影运动及波形图的变化。这是理解参数物理意义的关键。
        *   **投影轴选择**：提供切换投影轴（x轴或y轴）的选项，展示分别生成余弦曲线和正弦曲线，深化对“初相位影响图像起点”的理解。

*   **视觉呈现**：
    1.  **三区域同屏布局**：
        *   **左侧区域（圆周运动与投影）**：一个大的圆形轨迹，一个做圆周运动的质点，一条清晰的投影线（如垂直或水平虚线）连接至中央的直径（或坐标轴）。
        *   **中央区域（简谐运动演示）**：展示质点在直径（或坐标轴）上做往复直线运动（简谐运动），此区域与左侧投影区域紧密衔接。
        *   **右侧区域（波形图绘制）**：一个独立的位移-时间坐标系，随着动画进行，从左向右动态绘制出 `x-t` 曲线。有一条垂直的“时间线”从左向右扫描，代表当前时刻。
    2.  **运动同步**：三个区域的动画必须严格同步，时间轴统一。圆周运动转过的角度、投影点的位置、波形图描点的位置，三者时刻对应。

#### 配色方案选择
*   **主色调与清晰度**：采用深色背景（如 `#1e1e2e` 或 `#0f172a`），以突出彩色的运动元素和轨迹，减少视觉干扰，营造科技感与专注氛围。
*   **核心元素色**：
    *   **圆周与轨迹**：使用中等亮度的灰色（如 `#94a3b8`），清晰但不抢眼。
    *   **运动质点**：使用高饱和度的**青色**（如 `#06b6d4`），作为视觉焦点。
    *   **投影线与投影点**：使用**亮黄色**（如 `#fbbf24`），表示从圆周运动“衍生”出的关键过程。
    *   **简谐运动路径（直径/坐标轴）**：使用白色或浅灰色（`#e2e8f0`）。
    *   **波形图曲线**：使用与投影点同色的**亮黄色**，强调其直接来源于投影运动。
    *   **辅助线与标记**（如相位角、半径、坐标轴）：使用低饱和度的蓝色或绿色（如 `#67e8f9` 或 `#86efac`），提供信息但不杂乱。
    *   **控制面板/文字**：使用浅灰色（`#cbd5e1`）确保可读性。

#### 交互功能列表
1.  **动画控制**：
    *   播放 / 暂停 / 重置 按钮。
    *   单步前进 按钮（前进一个小的相位角，如 π/12）。
    *   速度调节滑块（控制角速度ω或动画播放速度）。
2.  **参数实时调整**（通过滑块或输入框）：
    *   振幅 A / 圆周半径 R。
    *   角频率 ω。
    *   初相位 φ（用角度或弧度表示）。
3.  **视图与投影控制**：
    *   切换投影轴（X轴投影 / Y轴投影）。
    *   显示/隐藏关键辅助线（如投影线、相位角标注、时间线）。
    *   显示/隐藏波形图上的实时坐标 `(t, x)`。
4.  **教学提示**：
    *   一个可展开/折叠的说明区域，分点解释当前演示的核心原理。
    *   在关键元素（如质点、投影点、波形点）悬停时，显示简短的工具提示说明。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>简谐运动与圆周运动投影关系演示</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background-color: #0f172a;
            color: #cbd5e1;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid #334155;
        }

        h1 {
            color: #06b6d4;
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #94a3b8;
            font-size: 1.2rem;
        }

        .main-content {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .animation-area {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .canvas-container {
            background-color: #1e293b;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            flex: 1;
            min-width: 300px;
            max-width: 900px;
        }

        canvas {
            display: block;
            width: 100%;
            height: 500px;
            border-radius: 8px;
        }

        .controls-panel {
            background-color: #1e293b;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            width: 100%;
            max-width: 400px;
        }

        .panel-section {
            margin-bottom: 25px;
        }

        h2 {
            color: #67e8f9;
            font-size: 1.5rem;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #334155;
        }

        h3 {
            color: #86efac;
            font-size: 1.2rem;
            margin-bottom: 12px;
        }

        .control-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #e2e8f0;
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        input[type="range"] {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            background: #334155;
            border-radius: 4px;
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #06b6d4;
            cursor: pointer;
        }

        .value-display {
            min-width: 60px;
            text-align: center;
            background: #334155;
            padding: 5px 10px;
            border-radius: 6px;
            font-family: monospace;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 15px;
        }

        button {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            background-color: #3b82f6;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            flex: 1;
            min-width: 120px;
        }

        button:hover {
            background-color: #2563eb;
            transform: translateY(-2px);
        }

        button:active {
            transform: translateY(0);
        }

        button.reset {
            background-color: #ef4444;
        }

        button.reset:hover {
            background-color: #dc2626;
        }

        button.step {
            background-color: #f59e0b;
        }

        button.step:hover {
            background-color: #d97706;
        }

        .toggle-group {
            display: flex;
            gap: 15px;
            margin-top: 10px;
        }

        .toggle-btn {
            padding: 10px 15px;
            background-color: #475569;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.2s ease;
            text-align: center;
            flex: 1;
        }

        .toggle-btn.active {
            background-color: #06b6d4;
            color: white;
        }

        .toggle-btn:hover {
            background-color: #64748b;
        }

        .info-panel {
            background-color: #1e293b;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }

        .info-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease;
        }

        .info-content.expanded {
            max-height: 500px;
        }

        .info-toggle {
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            padding-bottom: 15px;
        }

        .info-toggle h2 {
            margin-bottom: 0;
            border-bottom: none;
        }

        .toggle-icon {
            font-size: 1.5rem;
            transition: transform 0.3s ease;
        }

        .info-list {
            list-style-type: none;
            padding-top: 15px;
        }

        .info-list li {
            margin-bottom: 15px;
            padding-left: 20px;
            position: relative;
        }

        .info-list li:before {
            content: "•";
            color: #06b6d4;
            font-size: 1.5rem;
            position: absolute;
            left: 0;
            top: -5px;
        }

        .status-display {
            background-color: #334155;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
            font-family: monospace;
            font-size: 1.1rem;
        }

        .status-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .status-item:last-child {
            margin-bottom: 0;
        }

        .status-label {
            color: #94a3b8;
        }

        .status-value {
            color: #fbbf24;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #334155;
            color: #94a3b8;
            font-size: 0.9rem;
        }

        @media (max-width: 1100px) {
            .animation-area {
                flex-direction: column;
                align-items: center;
            }
            
            .canvas-container, .controls-panel {
                max-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>简谐运动与圆周运动投影关系</h1>
            <p class="subtitle">动态演示简谐运动是匀速圆周运动在直径上的投影</p>
        </header>
        
        <div class="main-content">
            <div class="animation-area">
                <div class="canvas-container">
                    <canvas id="animationCanvas"></canvas>
                </div>
                
                <div class="controls-panel">
                    <div class="panel-section">
                        <h2>动画控制</h2>
                        <div class="button-group">
                            <button id="playPauseBtn">播放</button>
                            <button id="stepBtn" class="step">单步前进</button>
                            <button id="resetBtn" class="reset">重置</button>
                        </div>
                        
                        <div class="control-group">
                            <label for="speedSlider">动画速度: <span id="speedValue">1.0x</span></label>
                            <div class="slider-container">
                                <input type="range" id="speedSlider" min="0.1" max="3" step="0.1" value="1">
                                <div class="value-display" id="speedDisplay">1.0x</div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="panel-section">
                        <h2>参数调整</h2>
                        
                        <div class="control-group">
                            <label for="amplitudeSlider">振幅 A = 半径 R: <span id="amplitudeValue">150</span> px</label>
                            <div class="slider-container">
                                <input type="range" id="amplitudeSlider" min="50" max="250" step="10" value="150">
                                <div class="value-display" id="amplitudeDisplay">150</div>
                            </div>
                        </div>
                        
                        <div class="control-group">
                            <label for="frequencySlider">角频率 ω: <span id="frequencyValue">1.0</span> rad/s</label>
                            <div class="slider-container">
                                <input type="range" id="frequencySlider" min="0.2" max="3" step="0.1" value="1">
                                <div class="value-display" id="frequencyDisplay">1.0</div>
                            </div>
                        </div>
                        
                        <div class="control-group">
                            <label for="phaseSlider">初相位 φ: <span id="phaseValue">0.0</span> rad</label>
                            <div class="slider-container">
                                <input type="range" id="phaseSlider" min="0" max="6.28" step="0.1" value="0">
                                <div class="value-display" id="phaseDisplay">0.0</div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="panel-section">
                        <h2>视图选项</h2>
                        
                        <div class="control-group">
                            <h3>投影轴选择</h3>
                            <div class="toggle-group">
                                <div id="projectXBtn" class="toggle-btn active">X轴投影 (余弦)</div>
                                <div id="projectYBtn" class="toggle-btn">Y轴投影 (正弦)</div>
                            </div>
                        </div>
                        
                        <div class="control-group">
                            <h3>显示选项</h3>
                            <div class="toggle-group">
                                <div id="toggleLinesBtn" class="toggle-btn active">显示辅助线</div>
                                <div id="toggleCoordsBtn" class="toggle-btn active">显示坐标</div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="status-display">
                        <div class="status-item">
                            <span class="status-label">相位角 (ωt+φ):</span>
                            <span class="status-value" id="phaseAngleValue">0.00 rad</span>
                        </div>
                        <div class="status-item">
                            <span class="status-label">时间 t:</span>
                            <span class="status-value" id="timeValue">0.00 s</span>
                        </div>
                        <div class="status-item">
                            <span class="status-label">位移 x:</span>
                            <span class="status-value" id="displacementValue">150.00 px</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="info-panel">
                <div class="info-toggle" id="infoToggle">
                    <h2>原理说明</h2>
                    <div class="toggle-icon" id="toggleIcon">▼</div>
                </div>
                <div class="info-content" id="infoContent">
                    <ul class="info-list">
                        <li><strong>核心关系</strong>: 匀速圆周运动在直径上的投影是简谐运动。圆周上的质点（青色）在x轴或y轴上的投影点（黄色）做简谐振动。</li>
                        <li><strong>参数对应</strong>: 圆周半径R对应简谐运动振幅A；圆周角速度ω对应简谐运动角频率ω；圆周相位角(ωt+φ)对应简谐运动相位。</li>
                        <li><strong>波形图生成</strong>: 右侧波形图记录了投影点的位移随时间的变化，形成正弦/余弦曲线。波形图上的每个点都对应左侧圆周运动的一个特定相位。</li>
                        <li><strong>相位角</strong>: 表示圆周运动质点的位置角度，决定了简谐运动质点的位移。初相位φ决定了t=0时质点的起始位置。</li>
                        <li><strong>交互操作</strong>: 调整参数观察变化；使用"单步前进"仔细查看对应关系；切换投影轴观察正弦/余弦波形差异。</li>
                    </ul>
                </div>
            </div>
        </div>
        
        <footer>
            <p>教学动画演示 | 简谐运动与圆周运动投影关系 | 设计原理：匀速圆周运动在直径上的投影是简谐运动</p>
        </footer>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = 500;
        }
        
        // 初始调整尺寸
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 动画状态
        let animationId = null;
        let isPlaying = false;
        let time = 0;
        let lastTime = 0;
        
        // 物理参数
        let amplitude = 150;    // 振幅/半径 (px)
        let frequency = 1.0;    // 角频率 (rad/s)
        let phase = 0;          // 初相位 (rad)
        let speedFactor = 1.0;  // 动画速度因子
        
        // 视图选项
        let projectToX = true;  // true: 投影到X轴 (余弦), false: 投影到Y轴 (正弦)
        let showLines = true;   // 显示辅助线
        let showCoords = true;  // 显示坐标
        
        // 颜色定义
        const colors = {
            background: '#0f172a',
            canvasBg: '#1e293b',
            circle: '#94a3b8',
            circlePoint: '#06b6d4',
            projectionLine: '#fbbf24',
            projectionPoint: '#fbbf24',
            harmonicPath: '#e2e8f0',
            waveCurve: '#fbbf24',
            angleArc: '#67e8f9',
            angleLine: '#67e8f9',
            text: '#cbd5e1',
            axis: '#475569',
            grid: '#334155'
        };
        
        // 获取DOM元素
        const playPauseBtn = document.getElementById('playPauseBtn');
        const stepBtn = document.getElementById('stepBtn');
        const resetBtn = document.getElementById('resetBtn');
        const speedSlider = document.getElementById('speedSlider');
        const speedValue = document.getElementById('speedValue');
        const speedDisplay = document.getElementById('speedDisplay');
        const amplitudeSlider = document.getElementById('amplitudeSlider');
        const amplitudeValue = document.getElementById('amplitudeValue');
        const amplitudeDisplay = document.getElementById('amplitudeDisplay');
        const frequencySlider = document.getElementById('frequencySlider');
        const frequencyValue = document.getElementById('frequencyValue');
        const frequencyDisplay = document.getElementById('frequencyDisplay');
        const phaseSlider = document.getElementById('phaseSlider');
        const phaseValue = document.getElementById('phaseValue');
        const phaseDisplay = document.getElementById('phaseDisplay');
        const projectXBtn = document.getElementById('projectXBtn');
        const projectYBtn = document.getElementById('projectYBtn');
        const toggleLinesBtn = document.getElementById('toggleLinesBtn');
        const toggleCoordsBtn = document.getElementById('toggleCoordsBtn');
        const phaseAngleValue = document.getElementById('phaseAngleValue');
        const timeValue = document.getElementById('timeValue');
        const displacementValue = document.getElementById('displacementValue');
        const infoToggle = document.getElementById('infoToggle');
        const infoContent = document.getElementById('infoContent');
        const toggleIcon = document.getElementById('toggleIcon');
        
        // 波形数据存储
        let wavePoints = [];
        const maxWavePoints = 500;
        
        // 初始化事件监听
        function initEventListeners() {
            // 动画控制
            playPauseBtn.addEventListener('click', togglePlayPause);
            stepBtn.addEventListener('click', stepAnimation);
            resetBtn.addEventListener('click', resetAnimation);
            
            // 参数滑块
            speedSlider.addEventListener('input', function() {
                speedFactor = parseFloat(this.value);
                speedValue.textContent = speedFactor.toFixed(1) + 'x';
                speedDisplay.textContent = speedFactor.toFixed(1) + 'x';
            });
            
            amplitudeSlider.addEventListener('input', function() {
                amplitude = parseInt(this.value);
                amplitudeValue.textContent = amplitude;
                amplitudeDisplay.textContent = amplitude;
                // 重置波形数据
                wavePoints = [];
            });
            
            frequencySlider.addEventListener('input', function() {
                frequency = parseFloat(this.value);
                frequencyValue.textContent = frequency.toFixed(1);
                frequencyDisplay.textContent = frequency.toFixed(1);
            });
            
            phaseSlider.addEventListener('input', function() {
                phase = parseFloat(this.value);
                phaseValue.textContent = phase.toFixed(1);
                phaseDisplay.textContent = phase.toFixed(1);
                // 重置波形数据
                wavePoints = [];
            });
            
            // 视图选项
            projectXBtn.addEventListener('click', function() {
                projectToX = true;
                projectXBtn.classList.add('active');
                projectYBtn.classList.remove('active');
                // 重置波形数据
                wavePoints = [];
            });
            
            projectYBtn.addEventListener('click', function() {
                projectToX = false;
                projectYBtn.classList.add('active');
                projectXBtn.classList.remove('active');
                // 重置波形数据
                wavePoints = [];
            });
            
            toggleLinesBtn.addEventListener('click', function() {
                showLines = !showLines;
                toggleLinesBtn.classList.toggle('active', showLines);
            });
            
            toggleCoordsBtn.addEventListener('click', function() {
                showCoords = !showCoords;
                toggleCoordsBtn.classList.toggle('active', showCoords);
            });
            
            // 信息面板切换
            infoToggle.addEventListener('click', function() {
                infoContent.classList.toggle('expanded');
                toggleIcon.textContent = infoContent.classList.contains('expanded') ? '▲' : '▼';
            });
        }
        
        // 动画控制函数
        function togglePlayPause() {
            if (isPlaying) {
                pauseAnimation();
            } else {
                playAnimation();
            }
        }
        
        function playAnimation() {
            if (!isPlaying) {
                isPlaying = true;
                playPauseBtn.textContent = '暂停';
                lastTime = performance.now();
                animationId = requestAnimationFrame(animate);
            }
        }
        
        function pauseAnimation() {
            if (isPlaying) {
                isPlaying = false;
                playPauseBtn.textContent = '播放';
                if (animationId) {
                    cancelAnimationFrame(animationId);
                    animationId = null;
                }
            }
        }
        
        function stepAnimation() {
            // 前进一个时间步长 (对应π/12弧度)
            const stepAngle = Math.PI / 12;
            time += stepAngle / frequency;
            updateWavePoints();
            draw();
        }
        
        function resetAnimation() {
            time = 0;
            wavePoints = [];
            draw();
            
            // 如果正在播放，继续播放
            if (isPlaying) {
                lastTime = performance.now();
            }
        }
        
        // 动画循环
        function animate(currentTime) {
            if (!lastTime) lastTime = currentTime;
            
            // 计算时间增量 (考虑速度因子)
            const deltaTime = (currentTime - lastTime) / 1000; // 转换为秒
            time += deltaTime * speedFactor;
            lastTime = currentTime;
            
            // 更新波形数据
            updateWavePoints();
            
            // 绘制场景
            draw();
            
            // 更新状态显示
            updateStatusDisplay();
            
            // 继续动画循环
            if (isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }
        
        // 更新波形数据点
        function updateWavePoints() {
            // 计算当前相位角
            const phaseAngle = frequency * time + phase;
            
            // 计算投影位移
            let displacement;
            if (projectToX) {
                displacement = amplitude * Math.cos(phaseAngle); // X轴投影 (余弦)
            } else {
                displacement = amplitude * Math.sin(phaseAngle); // Y轴投影 (正弦)
            }
            
            // 添加新的波形点
            wavePoints.push({
                time: time,
                displacement: displacement,
                phaseAngle: phaseAngle
            });
            
            // 限制波形点的数量
            if (wavePoints.length > maxWavePoints) {
                wavePoints.shift();
            }
        }
        
        // 绘制整个场景
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 计算布局参数
            const centerX = canvas.width * 0.3;
            const centerY = canvas.height / 2;
            const circleRadius = amplitude;
            const waveStartX = canvas.width * 0.6;
            const waveWidth = canvas.width * 0.35;
            const waveHeight = circleRadius * 2;
            
            // 绘制网格背景
            drawGrid(centerX, centerY, waveStartX, waveWidth, waveHeight);
            
            // 绘制左侧圆周运动区域
            drawCircleMotion(centerX, centerY, circleRadius);
            
            // 绘制中央简谐运动区域
            drawHarmonicMotion(centerX, centerY, circleRadius);
            
            // 绘制右侧波形图区域
            drawWaveGraph(waveStartX, centerY, waveWidth, waveHeight);
            
            // 绘制连接线（连接三个区域的关键点）
            drawConnections(centerX, centerY, circleRadius, waveStartX, waveHeight);
        }
        
        // 绘制网格背景
        function drawGrid(centerX, centerY, waveStartX, waveWidth, waveHeight) {
            ctx.strokeStyle = colors.grid;
            ctx.lineWidth = 0.5;
            ctx.setLineDash([2, 2]);
            
            // 左侧区域网格
            const gridSize = 40;
            for (let x = centerX - 300; x <= centerX + 300; x += gridSize) {
                if (x >= 0 && x <= waveStartX - 50) {
                    ctx.beginPath();
                    ctx.moveTo(x, 0);
                    ctx.lineTo(x, canvas.height);
                    ctx.stroke();
                }
            }
            
            for (let y = centerY - 300; y <= centerY + 300; y += gridSize) {
                if (y >= 0 && y <= canvas.height) {
                    ctx.beginPath();
                    ctx.moveTo(0, y);
                    ctx.lineTo(waveStartX - 50, y);
                    ctx.stroke();
                }
            }
            
            // 波形图区域网格
            for (let x = waveStartX; x <= waveStartX + waveWidth; x += gridSize) {
                ctx.beginPath();
                ctx.moveTo(x, centerY - waveHeight/2);
                ctx.lineTo(x, centerY + waveHeight/2);
                ctx.stroke();
            }
            
            for (let y = centerY - waveHeight/2; y <= centerY + waveHeight/2; y += gridSize) {
                ctx.beginPath();
                ctx.moveTo(waveStartX, y);
                ctx.lineTo(waveStartX + waveWidth, y);
                ctx.stroke();
            }
            
            ctx.setLineDash([]);
        }
        
        // 绘制圆周运动
        function drawCircleMotion(centerX, centerY, radius) {
            // 绘制圆周轨迹
            ctx.strokeStyle = colors.circle;
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.arc(centerX, centerY, radius, 0, Math.PI * 2);
            ctx.stroke();
            
            // 计算当前相位角
            const phaseAngle = frequency * time + phase;
            
            // 计算圆周上的质点位置
            const circlePointX = centerX + radius * Math.cos(phaseAngle);
            const circlePointY = centerY - radius * Math.sin(phaseAngle); // 注意：Canvas Y轴向下为正
            
            // 绘制坐标轴
            ctx.strokeStyle = colors.axis;
            ctx.lineWidth = 1;
            
            // X轴
            ctx.beginPath();
            ctx.moveTo(centerX - radius - 20, centerY);
            ctx.lineTo(centerX + radius + 20, centerY);
            ctx.stroke();
            
            // Y轴
            ctx.beginPath();
            ctx.moveTo(centerX, centerY - radius - 20);
            ctx.lineTo(centerX, centerY + radius + 20);
            ctx.stroke();
            
            // 绘制相位角
            if (showLines) {
                ctx.strokeStyle = colors.angleArc;
                ctx.lineWidth = 1.5;
                ctx.beginPath();
                ctx.arc(centerX, centerY, radius * 0.3, 0, phaseAngle, phaseAngle < 0);
                ctx.stroke();
                
                // 角度线
                ctx.beginPath();
                ctx.moveTo(centerX, centerY);
                ctx.lineTo(
                    centerX + radius * 0.3 * Math.cos(phaseAngle),
                    centerY - radius * 0.3 * Math.sin(phaseAngle)
                );
                ctx.stroke();
                
                // 角度标签
                ctx.fillStyle = colors.angleArc;
                ctx.font = '14px Arial';
                const angleLabelX = centerX + radius * 0.35 * Math.cos(phaseAngle/2);
                const angleLabelY = centerY - radius * 0.35 * Math.sin(phaseAngle/2) - 5;
                ctx.fillText(`φ = ${phaseAngle.toFixed(2)} rad`, angleLabelX, angleLabelY);
            }
            
            // 绘制圆周上的质点
            ctx.fillStyle = colors.circlePoint;
            ctx.beginPath();
            ctx.arc(circlePointX, circlePointY, 8, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制半径线
            if (showLines) {
                ctx.strokeStyle = colors.angleLine;
                ctx.lineWidth = 1.5;
                ctx.beginPath();
                ctx.moveTo(centerX, centerY);
                ctx.lineTo(circlePointX, circlePointY);
                ctx.stroke();
                
                // 半径标签
                ctx.fillStyle = colors.angleLine;
                ctx.font = '14px Arial';
                const radiusLabelX = (centerX + circlePointX) / 2;
                const radiusLabelY = (centerY + circlePointY) / 2;
                ctx.fillText(`R = A = ${amplitude}`, radiusLabelX + 5, radiusLabelY - 5);
            }
            
            // 绘制坐标标签
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 16px Arial';
            ctx.fillText('圆周运动', centerX - 40, centerY - radius - 30);
            ctx.fillText(`ω = ${frequency.toFixed(1)} rad/s`, centerX - 40, centerY - radius - 10);
        }
        
        // 绘制简谐运动
        function drawHarmonicMotion(centerX, centerY, radius) {
            // 计算当前相位角
            const phaseAngle = frequency * time + phase;
            
            // 计算投影点位置
            let projectionX, projectionY;
            if (projectToX) {
                // X轴投影
                projectionX = centerX + radius * Math.cos(phaseAngle);
                projectionY = centerY;
            } else {
                // Y轴投影
                projectionX = centerX;
                projectionY = centerY - radius * Math.sin(phaseAngle);
            }
            
            // 绘制投影轴
            ctx.strokeStyle = colors.harmonicPath;
            ctx.lineWidth = 2;
            
            if (projectToX) {
                // X轴投影 - 绘制水平线
                ctx.beginPath();
                ctx.moveTo(centerX - radius, centerY);
                ctx.lineTo(centerX + radius, centerY);
                ctx.stroke();
                
                // 绘制投影线
                if (showLines) {
                    ctx.strokeStyle = colors.projectionLine;
                    ctx.lineWidth = 1;
                    ctx.setLineDash([5, 3]);
                    ctx.beginPath();
                    const circlePointX = centerX + radius * Math.cos(phaseAngle);
                    const circlePointY = centerY - radius * Math.sin(phaseAngle);
                    ctx.moveTo(circlePointX, circlePointY);
                    ctx.lineTo(projectionX, projectionY);
                    ctx.stroke();
                    ctx.setLineDash([]);
                }
            } else {
                // Y轴投影 - 绘制垂直线
                ctx.beginPath();
                ctx.moveTo(centerX, centerY - radius);
                ctx.lineTo(centerX, centerY + radius);
                ctx.stroke();
                
                // 绘制投影线
                if (showLines) {
                    ctx.strokeStyle = colors.projectionLine;
                    ctx.lineWidth = 1;
                    ctx.setLineDash([5, 3]);
                    ctx.beginPath();
                    const circlePointX = centerX + radius * Math.cos(phaseAngle);
                    const circlePointY = centerY - radius * Math.sin(phaseAngle);
                    ctx.moveTo(circlePointX, circlePointY);
                    ctx.lineTo(projectionX, projectionY);
                    ctx.stroke();
                    ctx.setLineDash([]);
                }
            }
            
            // 绘制投影点（简谐运动质点）
            ctx.fillStyle = colors.projectionPoint;
            ctx.beginPath();
            ctx.arc(projectionX, projectionY, 6, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制简谐运动标签
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 16px Arial';
            const labelY = projectToX ? centerY + 40 : centerX + 40;
            const labelX = projectToX ? centerX - 40 : centerX + 20;
            const labelText = projectToX ? 'X轴投影 (余弦)' : 'Y轴投影 (正弦)';
            ctx.fillText('简谐运动', labelX, labelY);
            ctx.fillText(labelText, labelX, labelY + 20);
        }
        
        // 绘制波形图
        function drawWaveGraph(startX, centerY, width, height) {
            // 绘制坐标轴
            ctx.strokeStyle = colors.axis;
            ctx.lineWidth = 2;
            
            // 时间轴 (X轴)
            ctx.beginPath();
            ctx.moveTo(startX, centerY);
            ctx.lineTo(startX + width, centerY);
            ctx.stroke();
            
            // 位移轴 (Y轴)
            ctx.beginPath();
            ctx.moveTo(startX, centerY - height/2);
            ctx.lineTo(startX, centerY + height/2);
            ctx.stroke();
            
            // 坐标轴标签
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 16px Arial';
            ctx.fillText('波形图 x(t)', startX + width/2 - 40, centerY - height/2 - 10);
            ctx.font = '14px Arial';
            ctx.fillText('位移 x', startX - 30, centerY - height/2 + 10);
            ctx.fillText('时间 t', startX + width - 20, centerY + 20);
            
            // 绘制刻度
            ctx.strokeStyle = colors.axis;
            ctx.lineWidth = 1;
            
            // Y轴刻度 (位移)
            for (let i = -2; i <= 2; i++) {
                if (i === 0) continue;
                const y = centerY - (i/2) * (height/2);
                ctx.beginPath();
                ctx.moveTo(startX - 5, y);
                ctx.lineTo(startX, y);
                ctx.stroke();
                
                ctx.fillText(`${i * amplitude/2}`, startX - 30, y + 4);
            }
            
            // 绘制波形曲线
            if (wavePoints.length > 1) {
                ctx.strokeStyle = colors.waveCurve;
                ctx.lineWidth = 2;
                ctx.beginPath();
                
                // 找到时间范围
                const maxTime = wavePoints[wavePoints.length - 1].time;
                const minTime = Math.max(0, maxTime - 10); // 显示最近10秒
                
                for (let i = 0; i < wavePoints.length; i++) {
                    const point = wavePoints[i];
                    
                    // 只绘制在时间范围内的点
                    if (point.time >= minTime) {
                        const x = startX + ((point.time - minTime) / (maxTime - minTime)) * width;
                        const y = centerY - (point.displacement / amplitude) * (height/2);
                        
                        if (i === 0) {
                            ctx.moveTo(x, y);
                        } else {
                            ctx.lineTo(x, y);
                        }
                    }
                }
                
                ctx.stroke();
            }
            
            // 绘制当前时间点
            if (wavePoints.length > 0) {
                const currentPoint = wavePoints[wavePoints.length - 1];
                const maxTime = wavePoints[wavePoints.length - 1].time;
                const minTime = Math.max(0, maxTime - 10);
                
                const currentX = startX + ((currentPoint.time - minTime) / (maxTime - minTime)) * width;
                const currentY = centerY - (currentPoint.displacement / amplitude) * (height/2);
                
                // 绘制时间线
                ctx.strokeStyle = colors.projectionLine;
                ctx.lineWidth = 1;
                ctx.setLineDash([3, 3]);
                ctx.beginPath();
                ctx.moveTo(currentX, centerY - height/2);
                ctx.lineTo(currentX, centerY + height/2);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 绘制当前波形点
                ctx.fillStyle = colors.projectionPoint;
                ctx.beginPath();
                ctx.arc(currentX, currentY, 6, 0, Math.PI * 2);
                ctx.fill();
                
                // 显示当前坐标
                if (showCoords) {
                    ctx.fillStyle = colors.projectionLine;
                    ctx.font = '14px Arial';
                    ctx.fillText(`t=${currentPoint.time.toFixed(2)}`, currentX + 5, centerY - height/2 + 15);
                    ctx.fillText(`x=${currentPoint.displacement.toFixed(1)}`, currentX + 5, currentY - 10);
                }
            }
            
            // 绘制波形图标签
            const waveType = projectToX ? 'x = A·cos(ωt+φ)' : 'x = A·sin(ωt+φ)';
            ctx.fillStyle = colors.text;
            ctx.font = '14px Arial';
            ctx.fillText(waveType, startX + 10, centerY - height/2 + 25);
        }
        
        // 绘制连接线
        function drawConnections(centerX, centerY, radius, waveStartX, waveHeight) {
            if (!showLines || wavePoints.length === 0) return;
            
            const current
<!--检测到代码截断，自动续写中...-->
const currentPoint = wavePoints[wavePoints.length - 1];
            const phaseAngle = currentPoint.phaseAngle;
            
            // 计算圆周上的点
            const circlePointX = centerX + radius * Math.cos(phaseAngle);
            const circlePointY = centerY - radius * Math.sin(phaseAngle);
            
            // 计算投影点
            let projectionX, projectionY;
            if (projectToX) {
                projectionX = centerX + radius * Math.cos(phaseAngle);
                projectionY = centerY;
            } else {
                projectionX = centerX;
                projectionY = centerY - radius * Math.sin(phaseAngle);
            }
            
            // 计算波形图上的点
            const maxTime = wavePoints[wavePoints.length - 1].time;
            const minTime = Math.max(0, maxTime - 10);
            const waveX = waveStartX + ((currentPoint.time - minTime) / (maxTime - minTime)) * (canvas.width * 0.35);
            const waveY = centerY - (currentPoint.displacement / amplitude) * (waveHeight/2);
            
            // 绘制从圆周点到投影点的连接线
            ctx.strokeStyle = colors.projectionLine;
            ctx.lineWidth = 1.5;
            ctx.setLineDash([5, 3]);
            ctx.beginPath();
            ctx.moveTo(circlePointX, circlePointY);
            ctx.lineTo(projectionX, projectionY);
            ctx.stroke();
            
            // 绘制从投影点到波形图的连接线
            ctx.beginPath();
            ctx.moveTo(projectionX, projectionY);
            ctx.lineTo(waveX, waveY);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制连接点
            ctx.fillStyle = colors.projectionLine;
            ctx.beginPath();
            ctx.arc(projectionX, projectionY, 4, 0, Math.PI * 2);
            ctx.fill();
        }
        
        // 更新状态显示
        function updateStatusDisplay() {
            if (wavePoints.length > 0) {
                const currentPoint = wavePoints[wavePoints.length - 1];
                const phaseAngle = currentPoint.phaseAngle;
                
                phaseAngleValue.textContent = phaseAngle.toFixed(2) + ' rad';
                timeValue.textContent = currentPoint.time.toFixed(2) + ' s';
                displacementValue.textContent = currentPoint.displacement.toFixed(2) + ' px';
            }
        }
        
        // 初始化
        function init() {
            initEventListeners();
            updateWavePoints();
            draw();
            updateStatusDisplay();
            
            // 初始绘制
            requestAnimationFrame(() => {
                draw();
            });
        }
        
        // 启动初始化
        init();
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

# 交互式教学动画使用指南
## 简谐运动与圆周运动投影关系

---

### 功能说明

本交互式动画旨在直观展示**简谐运动是匀速圆周运动在直径上的投影**这一核心物理原理。通过同步可视化圆周运动、投影简谐运动和波形图生成三个过程，将抽象的数学关系转化为生动的视觉体验，帮助您深入理解简谐运动的本质及其与圆周运动的内在联系。

### 主要功能

#### 1. 动画控制区
- **播放/暂停**：控制动画的连续运行与暂停
- **单步前进**：每次前进π/12弧度（15°），适合精细观察对应关系
- **重置**：将动画恢复到初始状态（时间t=0）
- **速度调节**：控制动画播放速度（0.1x至3.0x）

#### 2. 参数调整区
- **振幅A（半径R）**：50-250像素，控制圆周半径和简谐运动振幅
- **角频率ω**：0.2-3.0 rad/s，控制运动快慢
- **初相位φ**：0-2π rad，控制运动的起始位置

#### 3. 视图选项区
- **投影轴选择**：
  - X轴投影：生成余弦波形 `x = A·cos(ωt+φ)`
  - Y轴投影：生成正弦波形 `x = A·sin(ωt+φ)`
- **显示选项**：
  - 显示/隐藏辅助线（投影线、相位角标注等）
  - 显示/隐藏实时坐标值

#### 4. 状态显示区
实时显示：
- 当前相位角 (ωt+φ)
- 时间 t
- 位移 x

#### 5. 原理说明区
可展开/折叠的详细原理说明，包含核心概念解释。

### 设计特色

#### 视觉设计
- **三区域同步布局**：左侧圆周运动 → 中央简谐运动 → 右侧波形图，严格同步
- **色彩编码系统**：
  - 青色 (#06b6d4)：圆周运动质点
  - 亮黄色 (#fbbf24)：投影点、投影线、波形曲线
  - 蓝绿色 (#67e8f9)：相位角标注
  - 深色背景：减少视觉干扰，突出运动元素
- **动态连线**：实时连接圆周点、投影点、波形点，强化对应关系

#### 交互设计
- **实时响应**：所有参数调整立即反映在动画中
- **渐进式学习**：支持从静态观察 → 单步前进 → 连续播放的学习路径
- **探索式学习**：通过调整参数自主探索规律

### 教学要点

#### 核心概念对应关系
| 圆周运动 | 简谐运动 | 物理意义 |
|---------|---------|---------|
| 半径 R | 振幅 A | 最大位移 |
| 角速度 ω | 角频率 ω | 运动快慢 |
| 相位角 (ωt+φ) | 相位 (ωt+φ) | 运动状态 |
| 初始相位 φ | 初相 φ | 起始位置 |

#### 关键观察点
1. **相位角的双重角色**：
   - 在圆周上：决定质点的位置角度
   - 在波形图上：决定曲线的"阶段"

2. **波形图生成机制**：
   - 波形图是位移-时间关系的记录
   - 每个波形点对应一个特定的相位角
   - 波形图随时间从左向右"绘制"

3. **初相位的影响**：
   - 改变φ值，观察圆周起始位置的变化
   - 注意波形图起点的相应变化
   - 对比X/Y投影的不同效果

### 使用建议

#### 适合的学习路径
1. **初次接触**（建议用时：5分钟）
   - 点击"播放"，观察整体动画效果
   - 展开"原理说明"，阅读核心概念
   - 注意观察三个区域的同步关系

2. **深入理解**（建议用时：10分钟）
   - 点击"暂停"，使用"单步前进"按钮
   - 仔细观察每一步中：
     * 圆周点的位置变化
     * 投影点的对应移动
     * 波形图上新点的添加
   - 开启"显示辅助线"，观察连接关系

3. **自主探索**（建议用时：15分钟）
   - 调整振幅A：观察圆周大小和波形幅度的变化
   - 调整角频率ω：观察运动快慢和波形疏密的变化
   - 调整初相位φ：观察起始位置和波形平移的变化
   - 切换投影轴：对比正弦和余弦波形的差异

4. **巩固验证**（建议用时：10分钟）
   - 根据公式预测：设置特定参数，预测波形形状
   - 通过动画验证预测
   - 尝试解释观察到的现象

#### 教学应用建议
- **课堂演示**：教师可逐步展示，引导学生发现规律
- **自主学习**：学生可自主探索，构建理解
- **小组讨论**：设置探究问题，小组合作寻找答案
- **课后复习**：作为抽象概念的直观辅助

#### 技术提示
- 推荐使用Chrome、Edge等现代浏览器
- 确保屏幕分辨率足够，以同时显示三个区域
- 调整浏览器缩放至100%以获得最佳效果
- 动画性能可能受设备性能影响，可适当降低速度

---

### 探索问题（供思考与讨论）

1. **参数影响**：当角频率ω增大时，为什么波形图变得更"密集"？
2. **相位关系**：初相位φ从0变化到π时，波形图发生了什么变化？为什么？
3. **投影差异**：X轴投影和Y轴投影产生的波形有什么本质区别？
4. **极限情况**：当振幅A趋近于0时，三个区域分别会发生什么？
5. **实际应用**：这个原理在哪些实际物理系统中有应用？（如弹簧振子、单摆等）

---

**祝您探索愉快！通过这个交互式动画，您将不仅看到物理规律，更能理解其背后的数学之美和自然之妙。**