# 需求：自由落体与空气阻力影响（伽利略斜面实验的理想化）

### 1. 专业思考

**用户需求**：
用户的核心教学目标是帮助学生理解“自由落体”这一理想物理模型，并探究“空气阻力”如何影响真实世界中的下落运动。通过对比理想模型与实际情况，深化学生对伽利略斜面实验思想（即通过减小阻力来逼近理想状态）的理解。

**教学设计思路**：
- **核心概念**：自由落体是只受重力作用的匀加速直线运动；空气阻力会改变运动的性质，使其最终达到匀速（收尾速度）。
- **认知规律**：
    1.  **具象引入**：展示两个物体（如羽毛和铁球）在真实环境（有空气）中下落的不同现象，引发认知冲突。
    2.  **理想模型**：切换到真空环境，展示两者同时落地，建立自由落体的理想概念。
    3.  **参数探究**：通过调节阻力系数和质量，观察其对运动轨迹和收尾速度的影响，理解阻力作用的规律。
    4.  **抽象总结**：通过实时绘制并对比速度-时间图，将直观运动抽象为物理图像，揭示背后的数学规律（v-t图斜率、渐近线）。
- **交互设计**：
    - **场景切换**：通过按钮在“有空气”和“真空”两种环境中切换。
    - **参数调节**：使用滑块实时调节下落物体的“质量”和“空气阻力系数”。
    - **控制与重置**：提供“开始/暂停”和“重置”按钮控制动画。
    - **视觉反馈**：物体下落速度实时变化，并同步绘制速度-时间曲线图。
- **视觉呈现**：
    - 主场景为简洁的“实验竖井”，顶部释放物体，底部有刻度尺。
    - 左侧为控制面板，右侧为实时v-t图绘制区。
    - 物体用不同颜色和大小区分，下落时有轻微的位置变化模拟抖动，增强真实感。

**配色方案选择**：
选择 **“科技蓝”** 配色方案。深蓝色背景（`#0a1931`）模拟深邃的科学探索空间，与浅蓝色（`#00adb5`）、青色（`#a6e3e9`）和亮黄色（`#ffd369`）形成对比。这种配色冷静、理性，符合物理实验的科技感，同时能有效突出关键的运动物体（黄色）和数据曲线（青色），保护学生视力，营造专注的学习氛围。

**交互功能**：
1.  **环境切换**：在“有空气”和“真空”模式间切换。
2.  **物体选择**：选择“铁球”（质量大）或“羽毛”（质量小）进行下落。
3.  **参数调节**：通过滑块独立调节“质量”和“空气阻力系数”。
4.  **动画控制**：“开始/暂停”动画，“重置”回到初始状态。
5.  **实时绘图**：同步绘制并显示速度-时间关系图，包含理想自由落体曲线作为对比。
6.  **数据显示**：实时显示物体的瞬时速度、下落时间和是否达到收尾速度。

### 2. HTML_CODE
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>自由落体与空气阻力 | 交互教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        body {
            background-color: #0a1931;
            color: #a6e3e9;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }
        header {
            text-align: center;
            margin-bottom: 25px;
            width: 100%;
            max-width: 1000px;
        }
        h1 {
            color: #ffd369;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }
        .subtitle {
            color: #00adb5;
            font-size: 1.1rem;
        }
        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 25px;
            width: 100%;
            max-width: 1000px;
        }
        .control-panel {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 15px;
            padding: 25px;
            width: 320px;
            display: flex;
            flex-direction: column;
            gap: 25px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        .panel-section {
            border-bottom: 1px solid rgba(0, 173, 181, 0.3);
            padding-bottom: 20px;
        }
        .panel-section:last-of-type {
            border-bottom: none;
        }
        h2 {
            color: #00adb5;
            font-size: 1.4rem;
            margin-bottom: 15px;
        }
        .button-group {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }
        button {
            padding: 10px 18px;
            border: none;
            border-radius: 8px;
            background-color: #00adb5;
            color: #0a1931;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
        }
        button:hover {
            background-color: #ffd369;
            transform: translateY(-2px);
        }
        button.active {
            background-color: #ffd369;
            box-shadow: 0 0 15px rgba(255, 211, 105, 0.7);
        }
        .slider-container {
            margin-bottom: 20px;
        }
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }
        .slider-label span:last-child {
            color: #ffd369;
            font-weight: bold;
        }
        input[type="range"] {
            width: 100%;
            height: 8px;
            -webkit-appearance: none;
            background: rgba(0, 173, 181, 0.3);
            border-radius: 4px;
            outline: none;
        }
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #ffd369;
            cursor: pointer;
            box-shadow: 0 0 10px rgba(255, 211, 105, 0.8);
        }
        .data-display {
            background: rgba(166, 227, 233, 0.1);
            border-radius: 10px;
            padding: 15px;
            font-size: 0.95rem;
            line-height: 1.8;
        }
        .data-value {
            color: #ffd369;
            font-weight: bold;
        }
        .simulation-area {
            flex: 1;
            min-width: 600px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        #simulationCanvas {
            background-color: rgba(10, 25, 47, 0.9);
            border-radius: 15px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
            border: 2px solid #00adb5;
            width: 100%;
            height: 400px;
        }
        #graphCanvas {
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border: 2px solid #00adb5;
            width: 100%;
            height: 250px;
        }
        footer {
            margin-top: 30px;
            text-align: center;
            color: #00adb5;
            font-size: 0.9rem;
            padding: 20px;
            width: 100%;
            max-width: 1000px;
            border-top: 1px solid rgba(0, 173, 181, 0.2);
        }
        @media (max-width: 950px) {
            .container {
                flex-direction: column;
                align-items: center;
            }
            .control-panel, .simulation-area {
                width: 100%;
                min-width: unset;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>自由落体与空气阻力影响</h1>
        <p class="subtitle">探究伽利略斜面实验的理想化思想：从现实阻力到理想真空</p>
    </header>

    <div class="container">
        <div class="control-panel">
            <div class="panel-section">
                <h2>🏛️ 实验环境</h2>
                <div class="button-group">
                    <button id="btnAir" class="active">🌪️ 有空气</button>
                    <button id="btnVacuum">🪐 真空</button>
                </div>
                <p style="font-size:0.9rem; color:#a6e3e9;">切换环境，观察阻力对下落的影响。</p>
            </div>

            <div class="panel-section">
                <h2>🎯 物体与参数</h2>
                <div class="button-group">
                    <button id="btnBall">⚫ 铁球</button>
                    <button id="btnFeather">🪶 羽毛</button>
                </div>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>质量 (kg):</span>
                        <span id="massValue">5.0</span>
                    </div>
                    <input type="range" id="massSlider" min="0.1" max="20" step="0.1" value="5.0">
                </div>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>阻力系数 (kg/m):</span>
                        <span id="dragValue">0.05</span>
                    </div>
                    <input type="range" id="dragSlider" min="0" max="0.2" step="0.001" value="0.05">
                </div>
                <p style="font-size:0.9rem; color:#a6e3e9;">调节参数，探索质量与阻力如何决定运动。</p>
            </div>

            <div class="panel-section">
                <h2>⏯️ 动画控制</h2>
                <div class="button-group">
                    <button id="btnStartPause">开始下落</button>
                    <button id="btnReset">重置实验</button>
                </div>
            </div>

            <div class="panel-section">
                <h2>📊 实时数据</h2>
                <div class="data-display">
                    <p>下落时间: <span id="timeValue" class="data-value">0.00</span> 秒</p>
                    <p>瞬时速度: <span id="velocityValue" class="data-value">0.00</span> m/s</p>
                    <p>下落高度: <span id="heightValue" class="data-value">0.00</span> 米</p>
                    <p>状态: <span id="statusValue" class="data-value">等待释放</span></p>
                </div>
            </div>
        </div>

        <div class="simulation-area">
            <canvas id="simulationCanvas" width="600" height="400"></canvas>
            <canvas id="graphCanvas" width="600" height="250"></canvas>
        </div>
    </div>

    <footer>
        <p>交互式教学动画 | 设计原理：自由落体运动 v = gt， 有阻力运动 a = g - (k/m)v² | 致敬伽利略的科学思想</p>
    </footer>

    <script>
        // 获取Canvas和上下文
        const simCanvas = document.getElementById('simulationCanvas');
        const simCtx = simCanvas.getContext('2d');
        const graphCanvas = document.getElementById('graphCanvas');
        const graphCtx = graphCanvas.getContext('2d');

        // 获取控制元素
        const btnAir = document.getElementById('btnAir');
        const btnVacuum = document.getElementById('btnVacuum');
        const btnBall = document.getElementById('btnBall');
        const btnFeather = document.getElementById('btnFeather');
        const btnStartPause = document.getElementById('btnStartPause');
        const btnReset = document.getElementById('btnReset');
        const massSlider = document.getElementById('massSlider');
        const dragSlider = document.getElementById('dragSlider');
        const massValue = document.getElementById('massValue');
        const dragValue = document.getElementById('dragValue');
        const timeValue = document.getElementById('timeValue');
        const velocityValue = document.getElementById('velocityValue');
        const heightValue = document.getElementById('heightValue');
        const statusValue = document.getElementById('statusValue');

        // 物理参数与状态变量
        let physics = {
            environment: 'air', // 'air' 或 'vacuum'
            mass: 5.0, // 质量 (kg)
            dragCoefficient: 0.05, // 阻力系数 (kg/m)
            gravity: 9.81, // 重力加速度 (m/s²)
            time: 0,
            velocity: 0,
            height: 0,
            isRunning: false,
            isFinished: false,
            objectType: 'ball', // 'ball' 或 'feather'
            terminalVelocity: 0,
            maxTime: 8, // 模拟最大时间
            maxHeight: 380 // 模拟高度 (像素)
        };

        // 历史数据记录，用于绘图
        let history = {
            times: [],
            velocities: [],
            idealVelocities: [] // 理想自由落体速度
        };

        // 初始化与重置
        function resetExperiment() {
            physics.time = 0;
            physics.velocity = 0;
            physics.height = 0;
            physics.isFinished = false;
            history.times = [];
            history.velocities = [];
            history.idealVelocities = [];
            btnStartPause.textContent = '开始下落';
            physics.isRunning = false;
            statusValue.textContent = '等待释放';
            updateDataDisplay();
            drawSimulation();
            drawGraph();
        }

        // 更新数据显示
        function updateDataDisplay() {
            timeValue.textContent = physics.time.toFixed(2);
            velocityValue.textContent = physics.velocity.toFixed(2);
            heightValue.textContent = ((physics.height / physics.maxHeight) * 380).toFixed(2); // 转换为米
            massValue.textContent = physics.mass.toFixed(1);
            dragValue.textContent = physics.dragCoefficient.toFixed(3);

            // 计算并显示收尾速度
            if (physics.environment === 'air' && physics.dragCoefficient > 0) {
                physics.terminalVelocity = Math.sqrt((physics.mass * physics.gravity) / physics.dragCoefficient);
                if (physics.isRunning && !physics.isFinished) {
                    const ratio = physics.velocity / physics.terminalVelocity;
                    if (ratio > 0.95) {
                        statusValue.textContent = `接近收尾速度: ${physics.terminalVelocity.toFixed(2)} m/s`;
                    } else {
                        statusValue.textContent = '加速下落中';
                    }
                }
            } else {
                physics.terminalVelocity = Infinity;
                statusValue.textContent = physics.isRunning ? '匀加速下落中' : '等待释放';
            }
        }

        // 物理计算（欧拉积分法）
        function updatePhysics(deltaTime) {
            if (physics.isFinished) return;

            physics.time += deltaTime;
            let acceleration = physics.gravity; // 默认重力加速度

            // 计算空气阻力（与速度平方成正比）
            if (physics.environment === 'air' && physics.dragCoefficient > 0) {
                const dragForce = physics.dragCoefficient * physics.velocity * physics.velocity;
                acceleration -= dragForce / physics.mass;
            }

            // 更新速度与高度
            physics.velocity += acceleration * deltaTime;
            if (physics.velocity < 0) physics.velocity = 0;
            physics.height += physics.velocity * deltaTime;

            // 记录历史数据
            history.times.push(physics.time);
            history.velocities.push(physics.velocity);
            history.idealVelocities.push(physics.gravity * physics.time); // 理想自由落体速度

            // 检查是否落地
            if (physics.height >= physics.maxHeight) {
                physics.isFinished = true;
                physics.height = physics.maxHeight;
                statusValue.textContent = '已落地';
                btnStartPause.textContent = '开始下落';
                physics.isRunning = false;
            }

            updateDataDisplay();
        }

        // 绘制主模拟场景
        function drawSimulation() {
            simCtx.clearRect(0, 0, simCanvas.width, simCanvas.height);

            // 绘制背景与竖井
            simCtx.fillStyle = '#0a1931';
            simCtx.fillRect(0, 0, simCanvas.width, simCanvas.height);

            // 绘制竖井墙壁
            simCtx.strokeStyle = '#00adb5';
            simCtx.lineWidth = 3;
            simCtx.beginPath();
            simCtx.moveTo(150, 10);
            simCtx.lineTo(150, simCanvas.height - 10);
            simCtx.moveTo(450, 10);
            simCtx.lineTo(450, simCanvas.height - 10);
            simCtx.stroke();

            // 绘制高度刻度尺
            simCtx.strokeStyle = '#a6e3e9';
            simCtx.lineWidth = 1;
            simCtx.font = '12px Arial';
            simCtx.fillStyle = '#a6e3e9';
            for (let h = 0; h <= 380; h += 38) {
                const y = 10 + h;
                simCtx.beginPath();
                simCtx.moveTo(140, y);
                simCtx.lineTo(150, y);
                simCtx.moveTo(450, y);
                simCtx.lineTo(460, y);
                simCtx.stroke();
                const meter = (380 - h).toFixed(0);
                simCtx.fillText(`${meter}m`, 110, y + 4);
                simCtx.fillText(`${meter}m`, 465, y + 4);
            }

            // 绘制底部地面
            simCtx.fillStyle = '#555';
            simCtx.fillRect(150, simCanvas.height - 10, 300, 10);
            simCtx.fillStyle = '#777';
            simCtx.fillRect(150, simCanvas.height - 10, 300, 5);

            // 绘制下落物体
            const x = simCanvas.width / 2;
            const y = 10 + physics.height; // 顶部起点为 y=10

            if (physics.objectType === 'ball') {
                // 绘制铁球
                const radius = 20 + physics.mass / 5;
                const gradient = simCtx.createRadialGradient(x, y, 5, x, y, radius);
                gradient.addColorStop(0, '#ffd369');
                gradient.addColorStop(1, '#cc9900');
                simCtx.beginPath();
                simCtx.arc(x, y, radius, 0, Math.PI * 2);
                simCtx.fillStyle = gradient;
                simCtx.fill();
                simCtx.strokeStyle = '#996600';
                simCtx.lineWidth = 2;
                simCtx.stroke();
                // 高光
                simCtx.beginPath();
                simCtx.arc(x - radius/3, y - radius/3, radius/4, 0, Math.PI * 2);
                simCtx.fillStyle = 'rgba(255, 255, 255, 0.6)';
                simCtx.fill();
            } else {
                // 绘制羽毛
                simCtx.save();
                simCtx.translate(x, y);
                // 轻微晃动模拟空气影响
                if (physics.environment === 'air' && physics.velocity > 0) {
                    simCtx.rotate(Math.sin(physics.time * 5) * 0.05);
                }
                simCtx.fillStyle = '#f0f0f0';
                simCtx.beginPath();
                // 羽毛主干
                simCtx.moveTo(0, -25);
                simCtx.lineTo(0, 15);
                // 羽毛绒
                for (let i = -20; i <= 15; i += 5) {
                    const len = 10 + Math.sin(i) * 5;
                    simCtx.moveTo(0, i);
                    simCtx.lineTo(-len, i - 3);
                    simCtx.moveTo(0, i);
                    simCtx.lineTo(len, i - 3);
                }
                simCtx.strokeStyle = '#ccc';
                simCtx.lineWidth = 1.5;
                simCtx.stroke();
                simCtx.restore();
            }

            // 绘制环境标签
            simCtx.font = 'bold 16px Arial';
            simCtx.fillStyle = physics.environment === 'air' ? '#00adb5' : '#ffd369';
            const envText = physics.environment === 'air' ? '🌪️ 有空气环境' : '🪐 真空环境';
            simCtx.fillText(envText, simCanvas.width - 200, 30);

            // 绘制收尾速度参考线（如果有）
            if (physics.environment === 'air' && physics.terminalVelocity < 100 && physics.velocity > 0) {
                const terminalY = 10 + (physics.terminalVelocity / physics.gravity) * physics.maxHeight;
                if (terminalY < simCanvas.height - 10) {
                    simCtx.strokeStyle = 'rgba(255, 100, 100, 0.7)';
                    simCtx.setLineDash([5, 5]);
                    simCtx.lineWidth = 1;
                    simCtx.beginPath();
                    simCtx.moveTo(150, terminalY);
                    simCtx.lineTo(450, terminalY);
                    simCtx.stroke();
                    simCtx.setLineDash([]);
                    simCtx.fillStyle = 'rgba(255, 100, 100, 0.9)';
                    simCtx.fillText(`收尾速度线`, 460, terminalY - 5);
                }
            }
        }

        // 绘制速度-时间图
        function drawGraph() {
            graphCtx.clearRect(0, 0, graphCanvas.width, graphCanvas.height);

            // 绘制网格背景
            graphCtx.strokeStyle = 'rgba(0, 173, 181, 0.2)';
            graphCtx.lineWidth = 1;
            const gridSize = 50;
            for (let x = 0; x <= graphCanvas.width; x += gridSize) {
                graphCtx.beginPath();
                graphCtx.moveTo(x, 0);
                graphCtx.lineTo(x, graphCanvas.height);
                graphCtx.stroke();
            }
            for (let y = 0; y <= graphCanvas.height; y += gridSize) {
                graphCtx.beginPath();
                graphCtx.moveTo(0, y);
                graphCtx.lineTo(graphCanvas.width, y);
                graphCtx.stroke();
            }

            // 绘制坐标轴
            graphCtx.strokeStyle = '#00adb5';
            graphCtx.lineWidth = 2;
            graphCtx.beginPath();
            graphCtx.moveTo(50, graphCanvas.height - 30);
            graphCtx.lineTo(graphCanvas.width - 20, graphCanvas.height - 30);
            graphCtx.moveTo(50, 20);
            graphCtx.lineTo(50, graphCanvas.height - 30);
            graphCtx.stroke();

            // 坐标轴标签
            graphCtx.fillStyle = '#a6e3e9';
            graphCtx.font = '14px Arial';
            graphCtx.fillText('时间 t (s)', graphCanvas.width - 80, graphCanvas.height - 10);
            graphCtx.save();
            graphCtx.translate(20, graphCanvas.height / 2);
            graphCtx.rotate(-Math.PI / 2);
            graphCtx.fillText('速度 v (m/s)', 0, 0);
            graphCtx.restore();

            // 刻度
            graphCtx.font = '12px Arial';
            for (let t = 0; t <= physics.maxTime; t += 1) {
                const x = 50 + (t / physics.maxTime) * (graphCanvas.width - 70);
                graphCtx.beginPath();
                graphCtx.moveTo(x, graphCanvas.height - 35);
                graphCtx.lineTo(x, graphCanvas.height - 25);
                graphCtx.stroke();
                graphCtx.fillText(t.toString(), x - 5, graphCanvas.height - 15);
            }
            const maxV = 80;
            for (let v = 0; v <= maxV; v += 20) {
                const y = graphCanvas.height - 30 - (v / maxV) * (graphCanvas.height - 50);
                graphCtx.beginPath();
                graphCtx.moveTo(45, y);
                graphCtx.lineTo(55, y);
                graphCtx.stroke();
                graphCtx.fillText(v.toString(), 25, y + 4);
            }

            // 如果没有数据，返回
            if (history.times.length === 0) return;

            // 绘制理想自由落体曲线 (v = gt)
            graphCtx.strokeStyle = 'rgba(255, 211, 105, 0.6)';
            graphCtx.lineWidth = 2;
            graphCtx.setLineDash([5, 5]);
            graphCtx.beginPath();
            for (let i = 0; i < history.times.length; i++) {
                const x = 50 + (history.times[i] / physics.maxTime) * (graphCanvas.width - 70);
                const y = graphCanvas.height - 30 - (history.idealVelocities[i] / maxV) * (graphCanvas.height - 50);
                if (i === 0) graphCtx.moveTo(x, y);
                else graphCtx.lineTo(x, y);
            }
            graphCtx.stroke();
            graphCtx.setLineDash([]);

            // 绘制实际速度曲线
            graphCtx.strokeStyle = '#00adb5';
            graphCtx.lineWidth = 3;
            graphCtx.beginPath();
            for (let i = 0; i < history.times.length; i++) {
                const x = 50 + (history.times[i] / physics.maxTime) * (graphCanvas.width - 70);
                const y = graphCanvas.height - 30 - (history.velocities[i] / maxV) * (graphCanvas.height - 50);
                if (i === 0) graphCtx.moveTo(x, y);
                else graphCtx.lineTo(x, y);
            }
            graphCtx.stroke();

            // 图例
            graphCtx.fillStyle = '#ffd369';
            graphCtx.fillRect(graphCanvas.width - 180, 25, 15, 15);
            graphCtx.fillStyle = '#a6e3e9';
            graphCtx.font = '14px Arial';
            graphCtx.fillText('理想自由落体 (v=gt)', graphCanvas.width - 160, 37);

            graphCtx.fillStyle = '#00adb5';
            graphCtx.fillRect(graphCanvas.width - 180, 50, 15, 15);
            graphCtx.fillStyle = '#a6e3e9';
            graphCtx.fillText('实际运动曲线', graphCanvas.width - 160, 62);
        }

        // 动画循环
        let lastTime = 0;
        function animate(currentTime) {
            const deltaTime = (currentTime - lastTime) / 1000; // 转换为秒
            if (deltaTime > 0.1) deltaTime = 0.1; // 限制最大时间步长，防止跳帧

            if (physics.isRunning && !physics.isFinished) {
                updatePhysics(deltaTime);
                drawSimulation();
                drawGraph();
            }

            lastTime = currentTime;
            requestAnimationFrame(animate);
        }

        // 事件监听与初始化
        btnAir.addEventListener('click', () => {
            physics.environment = 'air';
            btnAir.classList.add('active');
            btnVacuum.classList.remove('active');
            resetExperiment();
        });
        btnVacuum.addEventListener('click', () => {
            physics.environment = 'vacuum';
            btnVacuum.classList.add('active');
            btnAir.classList.remove('active');
            resetExperiment();
        });
        btnBall.addEventListener('click', () => {
            physics.objectType = 'ball';
            btnBall.classList.add('active');
            btnFeather.classList.remove('active');
            massSlider.value = 5.0;
            physics.mass = 5.0;
            resetExperiment();
        });
        btnFeather.addEventListener('click', () => {
            physics.objectType = 'feather';
            btnFeather.classList.add('active');
            btnBall.classList.remove('active');
            massSlider.value = 0.1;
            physics.mass = 0.1;
            resetExperiment();
        });
        btnStartPause.addEventListener('click', () => {
            if (physics.isFinished) return;
            physics.isRunning = !physics.isRunning;
            btnStartPause.textContent = physics.isRunning ? '暂停下落' : '继续下落';
            if (physics.isRunning && physics.time === 0) {
                statusValue.textContent = '开始下落';
            }
        });
        btnReset.addEventListener('click', resetExperiment);
        massSlider.addEventListener('input', () => {
            physics.mass = parseFloat(massSlider.value);
            resetExperiment();
        });
        dragSlider.addEventListener('input', () => {
            physics.dragCoefficient = parseFloat(dragSlider.value);
            resetExperiment();
        });

        // 初始化
        resetExperiment();
        requestAnimationFrame(animate);
    </script>
</body>
</html>
```

### 3. 过程输出

## 🎯 《自由落体与空气阻力影响》交互式教学动画使用指南

**📚 功能说明**
本动画旨在通过高度可视化和可交互的方式，帮助学生深入理解**自由落体**这一理想物理模型，以及**空气阻力**如何影响真实世界中的下落运动。它直观地演示了伽利略斜面实验的核心思想——通过减小阻力来逼近理想状态，从而揭示自然规律。

**🎮 主要功能**
1.  **环境切换**：点击“🌪️ 有空气”或“🪐 真空”按钮，可在两种物理环境间即时切换，直观对比阻力存在与否的惊人差异。
2.  **物体选择**：预设“⚫ 铁球”（质量大）和“🪶 羽毛”（质量小）两种典型物体，一键切换，重现经典对比实验。
3.  **参数调节**：
    - **质量滑块**：动态调整下落物体的质量（0.1kg 至 20kg）。
    - **阻力系数滑块**：精细调节空气阻力的大小（0 至 0.2 kg/m）。
    - **实时生效**：任何参数改变都会重置实验，让您即刻观察其影响。
4.  **动画控制**：使用“开始下落/暂停”和“重置实验”按钮，完全掌控实验进程，便于分步讲解和重复观察。
5.  **双重可视化**：
    - **主模拟区**：物体在“实验竖井”中下落，带有高度刻度。有空气时，物体会轻微晃动，并标注“收尾速度线”。
    - **实时图表区**：同步绘制**速度-时间（v-t）图**，用实线（实际运动）和虚线（理想自由落体v=gt）进行对比，清晰展示加速度的变化和收尾速度的渐近过程。
6.  **数据监控**：实时显示下落时间、瞬时速度、下落高度和当前运动状态。

**🎨 设计特色**
- **科技感配色**：采用深空蓝（`#0a1931`）为主背景，搭配青色（`#00adb5`）和亮黄色（`#ffd369`），营造专注、理性的科学探索氛围，关键信息突出。
- **拟真与抽象结合**：主场景模拟实验竖井，物体绘制精细（铁球有光泽，羽毛有细节）；图表区则完成从现象到物理规律的抽象升华。
- **智能反馈**：物体状态（如“接近收尾速度”）会实时更新，v-t图中的图例清晰说明曲线含义。
- **响应式布局**：适配不同屏幕尺寸，在电脑和平板上都能获得良好体验。

**💡 教学要点**
本动画能有效辅助讲解以下核心知识点：
- **理想模型与实际情况**：真空环境下所有物体加速度相同（g），完美诠释自由落体定义；有空气时，运动变得复杂。
- **收尾速度**：展示当重力与阻力平衡时，物体匀速下落的临界状态。引导学生推导公式 `v_t = sqrt(mg/k)`，并通过调节参数验证。
- **质量与阻力的影响**：通过单独调节质量和阻力系数，让学生自主发现：质量越大、阻力越小，越接近自由落体；轻小物体受阻力影响极大。
- **图像分析能力**：通过对比实际v-t曲线与理想斜线，直观理解“加速度减小直至为零”的过程，培养从图像中提取物理信息的能力。

**📱 使用建议**
1.  **引入环节**：先展示“有空气”下羽毛和铁球的下落，提问“为什么不同？”，引发认知冲突。再切换到“真空”，展示同时落地的震撼效果，引出“自由落体”概念。
2.  **探究环节**：
    - **固定阻力，变质量**：选择“有空气”，固定一个阻力系数，分别用铁球和羽毛（或调节质量滑块），观察谁先达到收尾速度，谁的下落时间长。
    - **固定质量，变阻力**：选择铁球，逐渐增大阻力系数，观察其v-t曲线如何从直线逐渐弯曲，理解阻力对加速度的削弱作用。
3.  **总结环节**：结合图表，引导学生总结空气阻力下物体运动的三个阶段：加速度逐渐减小的加速运动、收尾速度附近的准匀速运动。并与理想的匀加速直线运动进行对比。
4.  **课后延伸**：鼓励学生尝试用极端参数（如质量极大或阻力为0），预测并验证运动情况，深化对公式 `a = g - (k/m)v²` 的理解。

希望这款动画能成为您物理课堂上的得力助手，让抽象的概念生动起来，激发学生的探究热情！