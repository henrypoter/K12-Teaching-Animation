# 需求：简谐振动的相位差与简谐运动图像

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中物理或大学基础物理的学生。用户的核心需求是：
1.  **理解抽象概念**：“相位”和“相位差”是理解简谐振动叠加、波干涉等现象的关键，但非常抽象，学生难以从静态公式或单一运动轨迹中建立直观认知。
2.  **建立动态关联**：需要清晰地看到相位差如何影响两个振子的**运动状态（位移、速度、加速度）** 在时间轴上的先后关系，以及这种关系如何体现在**x-t图像（振动图像）** 上。
3.  **自主探索与验证**：学生应能主动改变关键参数（如相位差），并即时观察其对运动和图像的影响，从而通过交互归纳出规律，而非被动接受结论。
4.  **区分易混淆点**：明确区分“超前”与“滞后”、“同相”与“反相”等概念，并理解相位差取值范围（通常为0到2π或-π到π）。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
*   **核心概念**：
    *   **相位**：描述振子在周期运动中所处“位置”的物理量，决定了其瞬时运动状态。
    *   **相位差**：两个同频率简谐振动在同一时刻的相位之差（Δφ = φ₁ - φ₂）。
    *   **相位差与运动关系**：Δφ决定了两个振子运动的“步调”关系（谁先达到最大位移、平衡位置等）。
    *   **相位差与图像关系**：Δφ直接体现为两个x-t正弦曲线在水平方向（时间轴）上的**平移量**。

*   **认知规律**：
    1.  **从具体到抽象**：先展示两个真实振子（如弹簧振子或单摆）的并列运动，建立物理情景。
    2.  **从运动到图像**：在振子运动的同时，实时绘制各自的x-t图像，建立“运动轨迹”与“数学图像”的映射。
    3.  **从特殊到一般**：先观察Δφ=0（同相）、Δφ=π（反相）等特殊值，再通过滑块连续调节Δφ，观察所有中间状态。
    4.  **多表征联动**：确保振子位置、旋转参考圆（矢量图）、x-t图像、关键状态标记（如最大位移点）同步高亮显示，强化理解。

*   **交互设计**：
    *   **控制面板**：提供清晰的滑块和按钮，用于调节两个振动的**相位差（Δφ）** 和**振幅**。频率可设为相同且固定。
    *   **同步视图**：界面分为并排的“运动视图”和“图像视图”，两者时间轴严格同步。
    *   **跟踪与标记**：
        *   在运动视图中，用不同颜色的点或箭头实时指示两个振子的位置和速度方向。
        *   在图像视图中，用垂直的“时间扫描线”从左向右移动，其与两条曲线的交点对应此刻两个振子的位移，并在运动视图中高亮对应振子。
        *   可点击“标记点”按钮，在x-t图像上标记出振子经过平衡位置或最大位移的时刻点，便于比较先后。
    *   **预设与对比**：提供“同相”、“反相”、“超前π/2”、“滞后π/2”等典型相位差的快速设置按钮，并可一键叠加显示对比。

*   **视觉呈现**：
    *   **双视图布局**：左侧/上部为**运动视图**（模拟振子实物运动），右侧/下部为**图像视图**（绘制x-t曲线）。
    *   **运动视图**：采用简洁的卡通风格绘制弹簧振子或单摆，运动平滑。可考虑叠加显示旋转参考圆（两个旋转矢量），其与x轴的夹角直观表示相位。
    *   **图像视图**：绘制坐标系（时间t-位移x），两条不同颜色的曲线随时间延伸。背景采用浅色网格，曲线清晰醒目。
    *   **视觉联动**：当时间扫描线移动时，运动视图中的振子同步运动。两个振子及其对应的曲线使用一致的配色（如振子A用蓝色，其曲线和参考圆矢量也用蓝色）。

#### 配色方案选择
*   **主色调**：采用深蓝色（`#2c3e50`）作为背景或标题色，体现科学感和专业性。
*   **振动主体色**：选择两种对比鲜明且易于区分的颜色代表两个振子。
    *   振子A：**蓝色** (`#3498db`)，代表基准或振动1。
    *   振子B：**橙色** (`#e67e22`)，代表比较对象或振动2。
    *   （这两种颜色在色盲友好性上也相对较好）。
*   **辅助色**：
    *   坐标轴与网格：中灰色 (`#bdc3c7`)。
    *   背景：浅灰色 (`#ecf0f1`) 或白色 (`#ffffff`)。
    *   高亮与标记：使用主色的高亮版本（如`#1abc9c`青色）或红色 (`#e74c3c`) 用于时间扫描线、关键点标记。
    *   控制面板：浅色背景 (`#f8f9fa`)，按钮使用主色调的变体。

#### 交互功能列表
1.  **相位差控制**：
    *   一个滑块，范围从 `-π` 到 `+π` 或 `0` 到 `2π`，可连续调节相位差Δφ（振子B相对于振子A）。
    *   数值显示框，实时显示当前Δφ的值（弧度制和角度制可切换）。
2.  **振幅控制**（可选）：两个独立的滑块，分别控制两个振子的振幅。
3.  **典型值快速设置按钮**：
    *   “同相 (Δφ=0)”
    *   “反相 (Δφ=π)”
    *   “B超前A π/2”
    *   “B滞后A π/2”
4.  **运动控制按钮**：
    *   “播放/暂停”、“重置”。
    *   “单步前进/后退”按钮（可选，用于精细观察）。
5.  **视图显示选项**（复选框）：
    *   “显示/隐藏 旋转参考圆（矢量图）”
    *   “显示/隐藏 速度方向箭头”
    *   “显示/隐藏 x-t图像标记点”（如过平衡位置点）
    *   “轨迹留存”：让x-t图像持续绘制，还是只显示最近1-2个周期。
6.  **同步高亮与跟踪**：
    *   时间扫描线在图像视图上自动移动，并与运动实时同步。
    *   鼠标悬停在x-t图像的某时刻，可显示该时刻两个振子的精确位移值和相位值。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>简谐振动的相位差与简谐运动图像</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #2c3e50;
            color: #ecf0f1;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .container {
            max-width: 1200px;
            width: 100%;
            background-color: #ffffff;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }
        
        header {
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
            padding: 20px 30px;
            text-align: center;
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
            padding: 20px;
            gap: 20px;
        }
        
        .visualization-section {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .canvas-container {
            background-color: #f8f9fa;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        canvas {
            display: block;
            background-color: white;
        }
        
        .control-panel {
            flex: 0 0 320px;
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        .panel-title {
            color: #2c3e50;
            font-size: 20px;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #3498db;
        }
        
        .control-group {
            margin-bottom: 25px;
        }
        
        .control-title {
            color: #2c3e50;
            font-size: 16px;
            margin-bottom: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .value-display {
            background-color: #ecf0f1;
            padding: 4px 10px;
            border-radius: 4px;
            font-family: monospace;
            font-weight: bold;
            color: #2c3e50;
        }
        
        .slider-container {
            margin-bottom: 15px;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
            color: #2c3e50;
            font-size: 14px;
        }
        
        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: #bdc3c7;
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
            border: 2px solid white;
            box-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }
        
        .preset-buttons {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
            margin-bottom: 20px;
        }
        
        button {
            padding: 10px 15px;
            border: none;
            border-radius: 6px;
            background-color: #3498db;
            color: white;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.2s ease;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
        }
        
        button:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.15);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        .playback-controls {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .playback-controls button {
            flex: 1;
        }
        
        #resetBtn {
            background-color: #e74c3c;
        }
        
        #resetBtn:hover {
            background-color: #c0392b;
        }
        
        .view-options {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }
        
        .checkbox-container {
            display: flex;
            align-items: center;
            color: #2c3e50;
            font-size: 14px;
        }
        
        input[type="checkbox"] {
            margin-right: 8px;
            width: 18px;
            height: 18px;
            accent-color: #3498db;
        }
        
        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 10px;
            color: #2c3e50;
            font-size: 14px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 6px;
        }
        
        .legend-color {
            width: 16px;
            height: 16px;
            border-radius: 50%;
        }
        
        .legend-color.oscillator-a {
            background-color: #3498db;
        }
        
        .legend-color.oscillator-b {
            background-color: #e67e22;
        }
        
        .legend-color.reference-circle {
            background-color: #1abc9c;
        }
        
        .legend-color.time-line {
            background-color: #e74c3c;
        }
        
        footer {
            margin-top: 20px;
            text-align: center;
            color: #bdc3c7;
            font-size: 14px;
            padding: 10px;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
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
            <h1>简谐振动的相位差与简谐运动图像</h1>
            <p class="subtitle">探索相位差如何影响两个简谐振动的运动状态及其振动图像</p>
        </header>
        
        <div class="main-content">
            <div class="visualization-section">
                <div class="canvas-container">
                    <canvas id="motionCanvas" width="800" height="300"></canvas>
                </div>
                <div class="canvas-container">
                    <canvas id="graphCanvas" width="800" height="300"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color oscillator-a"></div>
                        <span>振子A (相位 φ₁)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color oscillator-b"></div>
                        <span>振子B (相位 φ₂)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color reference-circle"></div>
                        <span>旋转参考圆</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color time-line"></div>
                        <span>时间扫描线</span>
                    </div>
                </div>
            </div>
            
            <div class="control-panel">
                <h2 class="panel-title">控制面板</h2>
                
                <div class="control-group">
                    <div class="control-title">
                        <span>相位差 Δφ = φ₁ - φ₂</span>
                        <div class="value-display">
                            <span id="phaseDiffValue">0.00 rad (0.00°)</span>
                        </div>
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>相位差 (弧度)</span>
                            <span id="phaseDiffRadValue">0.00 rad</span>
                        </div>
                        <input type="range" id="phaseDiffSlider" min="-3.14" max="3.14" step="0.01" value="0">
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>振幅 A</span>
                            <span id="amplitudeValue">80</span>
                        </div>
                        <input type="range" id="amplitudeSlider" min="30" max="120" step="1" value="80">
                    </div>
                </div>
                
                <div class="control-group">
                    <div class="control-title">
                        <span>典型相位差预设</span>
                    </div>
                    <div class="preset-buttons">
                        <button id="inPhaseBtn">同相 (Δφ=0)</button>
                        <button id="oppositePhaseBtn">反相 (Δφ=π)</button>
                        <button id="lead90Btn">B超前A π/2</button>
                        <button id="lag90Btn">B滞后A π/2</button>
                    </div>
                </div>
                
                <div class="control-group">
                    <div class="control-title">
                        <span>运动控制</span>
                    </div>
                    <div class="playback-controls">
                        <button id="playPauseBtn">暂停</button>
                        <button id="resetBtn">重置</button>
                    </div>
                </div>
                
                <div class="control-group">
                    <div class="control-title">
                        <span>视图选项</span>
                    </div>
                    <div class="view-options">
                        <div class="checkbox-container">
                            <input type="checkbox" id="showReferenceCircle" checked>
                            <label for="showReferenceCircle">显示旋转参考圆</label>
                        </div>
                        <div class="checkbox-container">
                            <input type="checkbox" id="showVelocityArrows" checked>
                            <label for="showVelocityArrows">显示速度方向</label>
                        </div>
                        <div class="checkbox-container">
                            <input type="checkbox" id="showMarkers" checked>
                            <label for="showMarkers">显示图像标记点</label>
                        </div>
                        <div class="checkbox-container">
                            <input type="checkbox" id="showTrail" checked>
                            <label for="showTrail">显示运动轨迹</label>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>教学动画 | 简谐振动相位差 | 设计：教育技术专家</p>
    </footer>

    <script>
        // 获取Canvas元素和上下文
        const motionCanvas = document.getElementById('motionCanvas');
        const motionCtx = motionCanvas.getContext('2d');
        const graphCanvas = document.getElementById('graphCanvas');
        const graphCtx = graphCanvas.getContext('2d');
        
        // 获取控制元素
        const phaseDiffSlider = document.getElementById('phaseDiffSlider');
        const amplitudeSlider = document.getElementById('amplitudeSlider');
        const phaseDiffValue = document.getElementById('phaseDiffValue');
        const phaseDiffRadValue = document.getElementById('phaseDiffRadValue');
        const amplitudeValue = document.getElementById('amplitudeValue');
        
        const inPhaseBtn = document.getElementById('inPhaseBtn');
        const oppositePhaseBtn = document.getElementById('oppositePhaseBtn');
        const lead90Btn = document.getElementById('lead90Btn');
        const lag90Btn = document.getElementById('lag90Btn');
        
        const playPauseBtn = document.getElementById('playPauseBtn');
        const resetBtn = document.getElementById('resetBtn');
        
        const showReferenceCircle = document.getElementById('showReferenceCircle');
        const showVelocityArrows = document.getElementById('showVelocityArrows');
        const showMarkers = document.getElementById('showMarkers');
        const showTrail = document.getElementById('showTrail');
        
        // 动画参数
        let animationId = null;
        let isPlaying = true;
        let time = 0;
        const timeScale = 0.5; // 时间缩放因子，控制动画速度
        
        // 振动参数
        let amplitude = 80; // 振幅
        let angularFrequency = 1; // 角频率
        let phaseDiff = 0; // 相位差 Δφ = φ₁ - φ₂
        
        // 振子A的相位设为0，振子B的相位由相位差决定
        const getPhaseA = () => angularFrequency * time;
        const getPhaseB = () => angularFrequency * time - phaseDiff; // φ₂ = φ₁ - Δφ
        
        // 颜色定义
        const colors = {
            oscillatorA: '#3498db',
            oscillatorB: '#e67e22',
            referenceCircle: '#1abc9c',
            timeLine: '#e74c3c',
            grid: '#bdc3c7',
            text: '#2c3e50',
            background: '#ffffff',
            motionBackground: '#f8f9fa',
            marker: '#9b59b6'
        };
        
        // 存储历史轨迹点
        let trailPoints = [];
        const maxTrailPoints = 200;
        
        // 存储标记点
        let markerPoints = [];
        
        // 初始化
        function init() {
            // 设置Canvas尺寸
            resizeCanvases();
            window.addEventListener('resize', resizeCanvases);
            
            // 设置事件监听器
            phaseDiffSlider.addEventListener('input', updatePhaseDiff);
            amplitudeSlider.addEventListener('input', updateAmplitude);
            
            inPhaseBtn.addEventListener('click', () => setPhaseDiff(0));
            oppositePhaseBtn.addEventListener('click', () => setPhaseDiff(Math.PI));
            lead90Btn.addEventListener('click', () => setPhaseDiff(-Math.PI/2));
            lag90Btn.addEventListener('click', () => setPhaseDiff(Math.PI/2));
            
            playPauseBtn.addEventListener('click', togglePlayPause);
            resetBtn.addEventListener('click', resetAnimation);
            
            // 更新显示值
            updateDisplayValues();
            
            // 开始动画
            animate();
        }
        
        // 调整Canvas尺寸
        function resizeCanvases() {
            const containerWidth = document.querySelector('.canvas-container').clientWidth;
            
            motionCanvas.width = containerWidth;
            motionCanvas.height = 300;
            
            graphCanvas.width = containerWidth;
            graphCanvas.height = 300;
        }
        
        // 更新相位差
        function updatePhaseDiff() {
            phaseDiff = parseFloat(phaseDiffSlider.value);
            updateDisplayValues();
        }
        
        // 设置特定相位差
        function setPhaseDiff(value) {
            phaseDiff = value;
            phaseDiffSlider.value = value;
            updateDisplayValues();
        }
        
        // 更新振幅
        function updateAmplitude() {
            amplitude = parseInt(amplitudeSlider.value);
            updateDisplayValues();
        }
        
        // 更新显示值
        function updateDisplayValues() {
            const phaseDiffDeg = (phaseDiff * 180 / Math.PI).toFixed(2);
            phaseDiffValue.textContent = `${phaseDiff.toFixed(2)} rad (${phaseDiffDeg}°)`;
            phaseDiffRadValue.textContent = `${phaseDiff.toFixed(2)} rad`;
            amplitudeValue.textContent = amplitude;
        }
        
        // 切换播放/暂停
        function togglePlayPause() {
            isPlaying = !isPlaying;
            playPauseBtn.textContent = isPlaying ? '暂停' : '播放';
            
            if (isPlaying) {
                animate();
            } else {
                cancelAnimationFrame(animationId);
            }
        }
        
        // 重置动画
        function resetAnimation() {
            time = 0;
            trailPoints = [];
            markerPoints = [];
            
            if (!isPlaying) {
                isPlaying = true;
                playPauseBtn.textContent = '暂停';
                animate();
            }
        }
        
        // 绘制运动视图
        function drawMotionView() {
            const ctx = motionCtx;
            const width = motionCanvas.width;
            const height = motionCanvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制背景
            ctx.fillStyle = colors.motionBackground;
            ctx.fillRect(0, 0, width, height);
            
            // 计算振子位置
            const centerX = width / 2;
            const centerY = height / 2;
            
            const phaseA = getPhaseA();
            const phaseB = getPhaseB();
            
            const xA = amplitude * Math.cos(phaseA);
            const xB = amplitude * Math.cos(phaseB);
            
            // 绘制平衡位置线
            ctx.beginPath();
            ctx.moveTo(centerX - 200, centerY);
            ctx.lineTo(centerX + 200, centerY);
            ctx.strokeStyle = colors.grid;
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 绘制参考圆（如果启用）
            if (showReferenceCircle.checked) {
                // 振子A的参考圆
                ctx.beginPath();
                ctx.arc(centerX - 150, centerY, amplitude, 0, 2 * Math.PI);
                ctx.strokeStyle = colors.referenceCircle;
                ctx.lineWidth = 1;
                ctx.stroke();
                
                // 振子B的参考圆
                ctx.beginPath();
                ctx.arc(centerX + 150, centerY, amplitude, 0, 2 * Math.PI);
                ctx.strokeStyle = colors.referenceCircle;
                ctx.lineWidth = 1;
                ctx.stroke();
                
                // 绘制参考圆上的旋转矢量
                // 振子A
                ctx.beginPath();
                ctx.moveTo(centerX - 150, centerY);
                ctx.lineTo(
                    centerX - 150 + amplitude * Math.cos(phaseA),
                    centerY - amplitude * Math.sin(phaseA)
                );
                ctx.strokeStyle = colors.oscillatorA;
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 振子B
                ctx.beginPath();
                ctx.moveTo(centerX + 150, centerY);
                ctx.lineTo(
                    centerX + 150 + amplitude * Math.cos(phaseB),
                    centerY - amplitude * Math.sin(phaseB)
                );
                ctx.strokeStyle = colors.oscillatorB;
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 绘制相位角标记
                // 振子A
                ctx.beginPath();
                ctx.arc(centerX - 150, centerY, 20, 0, phaseA, phaseA > 0);
                ctx.strokeStyle = colors.oscillatorA;
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 振子B
                ctx.beginPath();
                ctx.arc(centerX + 150, centerY, 20, 0, phaseB, phaseB > 0);
                ctx.strokeStyle = colors.oscillatorB;
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 标注相位
                ctx.font = '14px Arial';
                ctx.fillStyle = colors.text;
                ctx.fillText(`φ₁ = ${phaseA.toFixed(2)}`, centerX - 200, centerY - 100);
                ctx.fillText(`φ₂ = ${phaseB.toFixed(2)}`, centerX + 100, centerY - 100);
            }
            
            // 绘制弹簧振子
            // 振子A
            const oscillatorAX = centerX - 150 + xA;
            const oscillatorAY = centerY;
            
            // 绘制弹簧
            ctx.beginPath();
            ctx.moveTo(centerX - 150 - amplitude, centerY);
            for (let i = 0; i <= 10; i++) {
                const t = i / 10;
                const springX = centerX - 150 - amplitude + (oscillatorAX - (centerX - 150 - amplitude)) * t;
                const springY = centerY + 10 * Math.sin(t * Math.PI * 4);
                ctx.lineTo(springX, springY);
            }
            ctx.strokeStyle = colors.grid;
            ctx.lineWidth = 1.5;
            ctx.stroke();
            
            // 绘制振子A
            ctx.beginPath();
            ctx.arc(oscillatorAX, oscillatorAY, 15, 0, 2 * Math.PI);
            ctx.fillStyle = colors.oscillatorA;
            ctx.fill();
            ctx.strokeStyle = '#2c3e50';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 振子B
            const oscillatorBX = centerX + 150 + xB;
            const oscillatorBY = centerY;
            
            // 绘制弹簧
            ctx.beginPath();
            ctx.moveTo(centerX + 150 + amplitude, centerY);
            for (let i = 0; i <= 10; i++) {
                const t = i / 10;
                const springX = centerX + 150 + amplitude + (oscillatorBX - (centerX + 150 + amplitude)) * t;
                const springY = centerY + 10 * Math.sin(t * Math.PI * 4);
                ctx.lineTo(springX, springY);
            }
            ctx.strokeStyle = colors.grid;
            ctx.lineWidth = 1.5;
            ctx.stroke();
            
            // 绘制振子B
            ctx.beginPath();
            ctx.arc(oscillatorBX, oscillatorBY, 15, 0, 2 * Math.PI);
            ctx.fillStyle = colors.oscillatorB;
            ctx.fill();
            ctx.strokeStyle = '#2c3e50';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制速度方向箭头（如果启用）
            if (showVelocityArrows.checked) {
                // 计算速度（位移的导数）
                const vA = -amplitude * angularFrequency * Math.sin(phaseA);
                const vB = -amplitude * angularFrequency * Math.sin(phaseB);
                
                // 绘制振子A速度箭头
                drawArrow(ctx, oscillatorAX, oscillatorAY, oscillatorAX + vA * 20, oscillatorAY, colors.oscillatorA);
                
                // 绘制振子B速度箭头
                drawArrow(ctx, oscillatorBX, oscillatorBY, oscillatorBX + vB * 20, oscillatorBY, colors.oscillatorB);
            }
            
            // 添加标签
            ctx.font = 'bold 16px Arial';
            ctx.fillStyle = colors.text;
            ctx.fillText('振子A', centerX - 200, centerY + 60);
            ctx.fillText('振子B', centerX + 120, centerY + 60);
            
            // 添加相位差信息
            ctx.font = '14px Arial';
            ctx.fillStyle = colors.text;
            ctx.fillText(`相位差 Δφ = ${phaseDiff.toFixed(2)} rad`, width / 2, 30);
            
            // 绘制轨迹（如果启用）
            if (showTrail.checked) {
                // 添加当前点到轨迹
                trailPoints.push({
                    xA: oscillatorAX,
                    yA: oscillatorAY,
                    xB: oscillatorBX,
                    yB: oscillatorBY,
                    time: time
                });
                
                // 限制轨迹点数量
                if (trailPoints.length > maxTrailPoints) {
                    trailPoints.shift();
                }
                
                // 绘制轨迹
                if (trailPoints.length > 1) {
                    // 振子A轨迹
                    ctx.beginPath();
                    ctx.moveTo(trailPoints[0].xA, trailPoints[0].yA);
                    for (let i = 1; i < trailPoints.length; i++) {
                        ctx.lineTo(trailPoints[i].xA, trailPoints[i].yA);
                    }
                    ctx.strokeStyle = colors.oscillatorA + '80'; // 80表示50%透明度
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // 振子B轨迹
                    ctx.beginPath();
                    ctx.moveTo(trailPoints[0].xB, trailPoints[0].yB);
                    for (let i = 1; i < trailPoints.length; i++) {
                        ctx.lineTo(trailPoints[i].xB, trailPoints[i].yB);
                    }
                    ctx.strokeStyle = colors.oscillatorB + '80'; // 80表示50%透明度
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
            }
        }
        
        // 绘制图像视图
        function drawGraphView() {
            const ctx = graphCtx;
            const width = graphCanvas.width;
            const height = graphCanvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制背景
            ctx.fillStyle = colors.background;
            ctx.fillRect(0, 0, width, height);
            
            // 绘制坐标轴
            const margin = 40;
            const graphWidth = width - 2 * margin;
            const graphHeight = height - 2 * margin;
            const originX = margin;
            const originY = height / 2;
            
            // 绘制坐标轴
            ctx.beginPath();
            // X轴（时间轴）
            ctx.moveTo(originX, originY);
            ctx.lineTo(originX + graphWidth, originY);
            // Y轴（位移轴）
            ctx.moveTo(originX, margin);
            ctx.lineTo(originX, height - margin);
            
            ctx.strokeStyle = colors.text;
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制网格
            ctx.strokeStyle = colors.grid;
            ctx.lineWidth = 0.5;
            
            // 水平网格线
            for (let i = 1; i <= 4; i++) {
                const y = originY - (i * amplitude);
                ctx.beginPath();
                ctx.moveTo(originX, y);
                ctx.lineTo(originX + graphWidth, y);
                ctx.stroke();
                
                // 负方向
                const yNeg = originY + (i * amplitude);
                ctx.beginPath();
                ctx.moveTo(originX, yNeg);
                ctx.lineTo(originX + graphWidth, yNeg);
                ctx.stroke();
            }
            
            // 垂直网格线（时间）
            const timePeriods = 2; // 显示2个周期
            for (let i = 0; i <= timePeriods * 4; i++) {
                const x = originX + (i * graphWidth) / (timePeriods * 4);
                ctx.beginPath();
                ctx.moveTo(x, margin);
                ctx.lineTo(x, height - margin);
                ctx.stroke();
            }
            
            // 坐标轴标签
            ctx.font = '14px Arial';
            ctx.fillStyle = colors.text;
            ctx.fillText('位移 x', originX - 30, margin + 10);
            ctx.fillText('时间 t', originX + graphWidth - 20, originY + 20);
            
            // 刻度标记
            ctx.fillText('A', originX - 20, originY - amplitude + 5);
            ctx.fillText('-A', originX - 25, originY + amplitude + 5);
            ctx.fillText('0', originX - 10, originY + 5);
            
            // 时间刻度
            for (let i = 0; i <= timePeriods; i++) {
                const x = originX + (i * graphWidth) / timePeriods;
                ctx.fillText(`${i}T`, x - 5, originY + 20);
            }
            
            // 计算当前时间在图形中的位置
            const currentX = originX + (time % (2 * Math.PI)) / (2 * Math.PI) * graphWidth;
            
            // 绘制时间扫描线
            ctx.beginPath();
            ctx.moveTo(currentX, margin);
            ctx.lineTo(currentX, height - margin);
            ctx.strokeStyle = colors.timeLine;
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制振子A的振动曲线
            ctx.beginPath();
            const pointsA = [];
            
            for (let i = 0; i <= graphWidth; i++) {
                const t = (i / graphWidth) * 2 * Math.PI * timePeriods; // 时间范围
                const x = originX + i;
                const y = originY - amplitude * Math.cos(angularFrequency * t);
                
                if (i === 0) {
                    ctx.moveTo(x, y);
                } else {
                    ctx.lineTo(x, y);
                }
                
                pointsA.push({x, y});
            }
            
            ctx.strokeStyle = colors.oscillatorA;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制振子B的振动曲线
            ctx.beginPath();
            const pointsB = [];
            
            for (let i = 0; i <= graphWidth; i++) {
                const t = (i / graphWidth) * 2 * Math.PI * timePeriods; // 时间范围
                const x = originX + i;
                const y = originY - amplitude * Math.cos(angularFrequency * t - phaseDiff);
                
                if (i === 0) {
                    ctx.moveTo(x, y);
                } else {
                    ctx.lineTo(x, y);
                }
                
                pointsB.push({x, y});
            }
            
            ctx.strokeStyle = colors.oscillatorB;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 找到当前时间对应的曲线点
            const indexA = Math.min(Math.floor((time % (2 * Math.PI)) / (2 * Math.PI) * pointsA.length), pointsA.length - 1);
            const indexB = Math.min(Math.floor((time % (2 * Math.PI)) / (2 * Math.PI) * pointsB.length), pointsB.length - 1);
            
            const pointA = pointsA[indexA];
            const pointB = pointsB[indexB];
            
            // 绘制当前时间点
            ctx.beginPath();
            ctx.arc(pointA.x, pointA.y, 6, 0, 2 * Math.PI);
            ctx.fillStyle = colors.oscillatorA;
            ctx.fill();
            
            ctx.beginPath();
            ctx.arc(pointB.x, pointB.y, 6, 0, 2 * Math.PI);
            ctx.fillStyle = colors.oscillatorB;
            ctx.fill();
            
            // 显示当前位移值
            ctx.font = '12px Arial';
            ctx.fillStyle = colors.oscillatorA;
            ctx.fillText(`x₁ = ${(amplitude * Math.cos(getPhaseA())).toFixed(1)}`, pointA.x + 10, pointA.y - 10);
            
            ctx.fillStyle = colors.oscillatorB;
            ctx.fillText(`x₂ = ${(amplitude * Math.cos(getPhaseB())).toFixed(1)}`, pointB.x + 10, pointB.y + 15);
            
            // 绘制标记点（如果启用）
            if (showMarkers.checked) {
                // 检测振子A经过平衡位置（x=0）的时刻
                const phaseA = getPhaseA();
                if (Math.abs(Math.cos(phaseA)) < 0.05) {
                    markerPoints.push({
                        x: currentX,
                        y: originY,
                        type: 'balance',
                        oscillator: 'A',
                        time: time
                    });
                }
                
                // 检测振子B经过平衡位置（x=0）的时刻
                const phaseB = getPhaseB();
                if (Math.abs(Math.cos(phaseB)) < 0.05) {
                    markerPoints.push({
                        x: currentX,
                        y: originY,
                        type: 'balance',
                        oscillator: 'B',
                        time: time
                    });
                }
                
                // 限制标记点数量
                if (markerPoints.length > 20) {
                    markerPoints.shift();
                }
                
                // 绘制标记点
                markerPoints.forEach(marker => {
                    ctx.beginPath();
                    ctx.arc(marker.x, marker.y, 4, 0, 2 * Math.PI);
                    ctx.fillStyle = marker.oscillator === 'A' ? colors.oscillatorA : colors.oscillatorB;
                    ctx.fill();
                    
                    // 添加小标签
                    ctx.font = '10px Arial';
                    ctx.fillStyle = colors.text;
                    const labelY = marker.oscillator === 'A' ? marker.y - 15 : marker.y + 15;
                    ctx.fillText(`${marker.oscillator}: t=${marker.time.toFixed(1)}`, marker.x - 20, labelY);
                });
            }
            
            // 添加图标题
            ctx.font = 'bold 16px Arial';
            ctx.fillStyle = colors.text;
            ctx.fillText('简谐运动图像 (x-t 图)', width / 2 - 80, 30);
            
            // 显示相位差对图像的影响
            ctx.font = '14px Arial';
            ctx.fillStyle = colors.text;
            let phaseDescription = '';
            if (Math.abs(phaseDiff) < 0.1) {
                phaseDescription = '同相：两个振子运动步调完全一致';
            } else if (Math.abs(phaseDiff - Math.PI) < 0.1) {
                phaseDescription = '反相：两个振子运动步调完全相反';
            } else if (phaseDiff > 0) {
                phaseDescription = `振子A超前振子B ${phaseDiff.toFixed(2)} rad`;
            } else {
                phaseDescription = `振子B超前振子A ${Math.abs(phaseDiff).toFixed(2)} rad`;
            }
            
            ctx.fillText(phaseDescription, width / 2, height - 10);
        }
        
        // 绘制箭头
        function drawArrow(ctx, fromX, fromY, toX, toY, color) {
            const headLength = 10;
            const dx = toX - fromX;
            const dy = toY - fromY;
            const angle = Math.atan2(dy, dx);
            
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.strokeStyle = color;
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headLength * Math.cos(angle - Math.PI/6), toY - headLength * Math.sin(angle - Math.PI/6));
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headLength * Math.cos(angle + Math.PI/6), toY - headLength * Math.sin(angle + Math.PI/6));
            ctx.strokeStyle = color;
            ctx.lineWidth = 2;
            ctx.stroke();
        }
        
        // 动画循环
        function animate() {
            if (isPlaying) {
                // 更新时间
                time += 0.02 * timeScale;
                
                // 绘制两个视图
                drawMotionView();
                drawGraphView();
                
                // 继续动画循环
                animationId = requestAnimationFrame(animate);
            }
        }
        
        // 初始化应用
        window.addEventListener('load', init);
    </script>
</body>
</html
<!--检测到代码截断，自动续写中...-->
</html>

### 3. 过程输出

### 3. 过程输出

## 《简谐振动相位差与运动图像》交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在帮助您直观、深入地理解简谐振动中“相位差”这一核心概念，以及它如何影响振子的运动状态和振动图像。通过动手操作和实时观察，您将建立起从物理运动到数学图像的完整认知桥梁。

---

### 一、功能说明

本动画包含两个同步更新的核心视图：

1.  **运动视图（上部）**：直观展示两个弹簧振子的实物运动。您可以看到：
    *   两个振子（蓝色-A，橙色-B）的实时位置
    *   旋转参考圆（矢量图）及相位角
    *   速度方向箭头
    *   运动轨迹（可选）

2.  **图像视图（下部）**：实时绘制两个振子的位移-时间（x-t）曲线。您可以看到：
    *   两条正弦曲线分别对应振子A和B
    *   一条垂直的红色“时间扫描线”同步移动，指示当前时刻
    *   曲线上的标记点，记录振子经过平衡位置的时刻

**所有视图严格同步**：当您调节参数时，两个视图会即时更新，确保您能同时观察到参数变化对物理运动和数学图像的双重影响。

---

### 二、主要功能与操作

#### 1. 核心参数调节
*   **相位差滑块**：拖动滑块，连续改变振子B相对于振子A的相位差（Δφ = φ₁ - φ₂）。观察范围从 -π 到 +π。
*   **振幅滑块**：调节两个振子共同的振幅大小。
*   **数值显示**：实时显示当前相位差的弧度值和角度值。

#### 2. 典型值快速设置
点击预设按钮，一键观察关键相位状态：
*   **同相 (Δφ=0)**：两个振子运动步调完全一致。
*   **反相 (Δφ=π)**：两个振子运动步调完全相反。
*   **B超前A π/2**：振子B的运动状态始终比振子A提前四分之一周期。
*   **B滞后A π/2**：振子B的运动状态始终比振子A落后四分之一周期。

#### 3. 运动控制
*   **播放/暂停**：控制动画的运行与停止，便于仔细观察特定瞬间。
*   **重置**：清空所有轨迹和标记，时间归零，重新开始。

#### 4. 视图定制
通过复选框，您可以自定义显示内容，聚焦于感兴趣的部分：
*   **显示/隐藏 旋转参考圆**：参考圆是理解“相位”概念的利器，它直观展示了相位角如何随时间旋转，并投影为振子的位移。
*   **显示/隐藏 速度方向箭头**：观察振子速度的大小和方向如何随相位变化。
*   **显示/隐藏 图像标记点**：在x-t图上标记振子经过平衡位置（x=0）的时刻，便于比较两个振子到达同一状态的先后顺序。
*   **显示/隐藏 运动轨迹**：查看振子最近的运动路径。

---

### 三、设计特色与教学要点

#### 设计特色
1.  **多表征联动**：将抽象的相位差概念，同时通过**实物运动**、**旋转矢量**和**正弦图像**三种方式呈现，建立牢固的物理图景。
2.  **即时反馈**：所有操作均产生即时、同步的视觉反馈，鼓励探索式学习。
3.  **从特殊到一般**：通过预设按钮快速观察典型情况，再通过滑块探索连续变化，符合认知规律。
4.  **视觉清晰**：采用对比鲜明的配色和清晰的视觉层次，确保信息传递高效。

#### 关键教学要点
在操作时，请特别关注以下关联，它们是理解相位差的核心：

1.  **相位差 ⇄ 运动“步调”关系**
    *   当 Δφ = 0（同相）时，观察两个振子是否**同时**到达最右端、平衡位置、最左端。
    *   当 Δφ = π（反相）时，观察当一个振子在最右端时，另一个是否在**最左端**。
    *   当 Δφ = π/2 时，观察当振子A在平衡位置且向右运动时，振子B是否在**最右端**（超前）或**最左端**（滞后）。

2.  **相位差 ⇄ x-t 图像平移**
    *   在图像视图中，**相位差直接表现为两条正弦曲线在水平方向（时间轴t）上的平移量**。
    *   尝试调节相位差，您会发现曲线B相对于曲线A发生了左右移动。移动多少个“格子”，就对应多少相位差。

3.  **“超前”与“滞后”的理解**
    *   本动画定义 **Δφ = φ₁ - φ₂**。
    *   若 Δφ > 0，表示 φ₁ > φ₂，即**振子A的相位更大**。在旋转参考圆上，A的矢量在前，因此**振子A的运动状态“超前”于振子B**。
    *   您可以通过“B超前A π/2”按钮来验证：此时 Δφ = -π/2，振子B的相位（φ₂）比振子A的相位（φ₁）大 π/2，因此B超前。

---

### 四、使用建议

1.  **初次探索**：
    *   先点击各个**预设按钮**，观察极端和典型情况下，两个振子的运动和图像有何特征。
    *   使用**播放/暂停**按钮，在关键位置（如最大位移处、平衡位置处）暂停，仔细比较两个振子的状态。

2.  **深入探究**：
    *   缓慢拖动**相位差滑块**，观察运动视图和图像视图是如何**连续变化**的。思考：“超前”是如何逐渐变成“滞后”的？
    *   打开**旋转参考圆**和**速度箭头**，理解相位角如何决定瞬时位移和速度。
    *   打开**图像标记点**，在x-t图上直观比较两个振子到达平衡位置的时刻差。

3.  **挑战与思考**：
    *   设置一个特定的相位差（如 2.1 rad），您能预测出振子B相对于振子A是超前还是滞后吗？大约差多少周期？
    *   观察图像视图：相位差为多少时，两条曲线的“波峰”完全重合？相位差为多少时，一个的“波峰”对应另一个的“波谷”？
    *   尝试总结：**相位差（Δφ）、时间差（Δt）和周期（T）三者之间有什么数学关系？**

我们希望这个交互式动画能成为您理解简谐振动相位概念的得力助手。请尽情探索、观察、提问，让抽象的物理概念在您的手中变得生动而清晰！

**祝您学习愉快，探索有成！**