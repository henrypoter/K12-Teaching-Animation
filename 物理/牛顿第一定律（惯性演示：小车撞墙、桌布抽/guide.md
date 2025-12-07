# 需求：牛顿第一定律（惯性演示：小车撞墙、桌布抽离）

# 专业思考

## 用户需求
用户需要制作一个关于牛顿第一定律（惯性定律）的教学动画，重点演示两个经典实验：
1. **小车撞墙实验**：展示运动中的物体具有保持原有运动状态的特性
2. **桌布抽离实验**：展示静止的物体具有保持静止状态的特性

核心教学目标是帮助学生理解"一切物体在没有受到外力作用时，总保持静止状态或匀速直线运动状态"这一物理定律。

## 教学设计思路

### 核心概念
- 惯性：物体保持原有运动状态的性质
- 外力作用：改变物体运动状态的原因
- 质量与惯性的关系：质量越大，惯性越大

### 认知规律
1. **从具象到抽象**：通过两个直观的生活化实验，让学生先观察现象，再理解背后的物理原理
2. **从现象到本质**：先展示实验现象，再揭示惯性原理，最后总结牛顿第一定律
3. **从简单到复杂**：先演示单一实验，再对比两个实验，最后引入质量对惯性的影响

### 交互设计
1. **场景切换**：通过按钮在两个实验场景间切换
2. **参数调节**：
   - 质量滑块：调节小车或杯子的质量
   - 速度滑块：调节小车初始速度
   - 抽离速度滑块：调节桌布抽离速度
3. **实验控制**：
   - 开始/暂停/重置按钮
   - 慢动作模式
   - 显示受力分析选项

### 视觉呈现
- 使用简洁的几何图形表示物理对象
- 添加运动轨迹和受力分析可视化
- 使用箭头表示速度和力的方向
- 添加关键物理量的实时显示

### 配色方案选择
选择**科技蓝**配色方案：
- 主色调：深蓝色(#1a237e) - 营造科学严谨的氛围
- 辅助色：浅蓝色(#bbdefb) - 用于背景和次要元素
- 强调色：橙色(#ff9800) - 用于重要元素和交互反馈
- 文字色：白色/浅灰色 - 确保可读性

蓝色系能营造冷静、理性的科学氛围，橙色作为强调色能有效吸引注意力到关键交互元素。

### 交互功能
1. 场景切换：小车撞墙实验 / 桌布抽离实验
2. 质量调节：0.5kg - 5kg
3. 速度调节：1m/s - 10m/s
4. 抽离速度调节：慢 - 快
5. 实验控制：开始/暂停/重置
6. 显示选项：轨迹显示、受力分析、慢动作模式
7. 实时数据显示：速度、质量、惯性大小

# HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>牛顿第一定律：惯性演示</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #0a192f;
            color: #e6f1ff;
            padding: 20px;
            min-height: 100vh;
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
            background: linear-gradient(135deg, #1a237e 0%, #0d47a1 100%);
            border-radius: 15px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
            margin-bottom: 10px;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: #ff9800;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: #bbdefb;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
        }
        
        .law-text {
            background-color: rgba(13, 71, 161, 0.3);
            padding: 15px;
            border-radius: 10px;
            margin-top: 15px;
            font-style: italic;
            border-left: 4px solid #ff9800;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .simulation-area {
            flex: 1;
            min-width: 300px;
            background-color: #112240;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
        }
        
        .canvas-container {
            background-color: #0a192f;
            border-radius: 10px;
            overflow: hidden;
            flex-grow: 1;
            position: relative;
            border: 2px solid #1a237e;
        }
        
        #simulationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .controls-area {
            flex: 1;
            min-width: 300px;
            background-color: #112240;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .control-section {
            background-color: rgba(26, 35, 126, 0.3);
            padding: 15px;
            border-radius: 10px;
            border-left: 4px solid #ff9800;
        }
        
        h2 {
            color: #64ffda;
            margin-bottom: 15px;
            font-size: 1.5rem;
        }
        
        h3 {
            color: #bbdefb;
            margin-bottom: 10px;
            font-size: 1.2rem;
        }
        
        .scene-selector {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .scene-btn {
            flex: 1;
            padding: 12px;
            background-color: #1a237e;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .scene-btn:hover {
            background-color: #283593;
            transform: translateY(-2px);
        }
        
        .scene-btn.active {
            background-color: #ff9800;
            color: #0a192f;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(255, 152, 0, 0.3);
        }
        
        .slider-container {
            margin-bottom: 15px;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }
        
        .slider-value {
            color: #ff9800;
            font-weight: bold;
        }
        
        input[type="range"] {
            width: 100%;
            height: 8px;
            -webkit-appearance: none;
            background: linear-gradient(to right, #1a237e, #64ffda);
            border-radius: 4px;
            outline: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            background-color: #ff9800;
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
        }
        
        .button-group {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        
        .control-btn {
            flex: 1;
            padding: 12px;
            background-color: #1a237e;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .control-btn:hover {
            background-color: #283593;
            transform: translateY(-2px);
        }
        
        .control-btn.primary {
            background-color: #ff9800;
            color: #0a192f;
            font-weight: bold;
        }
        
        .control-btn.primary:hover {
            background-color: #ffb74d;
        }
        
        .checkbox-group {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 10px;
        }
        
        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        input[type="checkbox"] {
            width: 18px;
            height: 18px;
            accent-color: #ff9800;
        }
        
        .data-display {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 10px;
        }
        
        .data-item {
            background-color: rgba(26, 35, 126, 0.5);
            padding: 12px;
            border-radius: 8px;
            text-align: center;
        }
        
        .data-value {
            font-size: 1.5rem;
            font-weight: bold;
            color: #64ffda;
            margin-top: 5px;
        }
        
        .data-label {
            font-size: 0.9rem;
            color: #bbdefb;
        }
        
        .explanation {
            background-color: #112240;
            border-radius: 15px;
            padding: 20px;
            margin-top: 20px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
        }
        
        .explanation-content {
            line-height: 1.6;
            margin-bottom: 15px;
        }
        
        .key-point {
            background-color: rgba(255, 152, 0, 0.1);
            padding: 12px;
            border-radius: 8px;
            border-left: 4px solid #ff9800;
            margin-top: 15px;
        }
        
        footer {
            text-align: center;
            margin-top: 20px;
            padding: 15px;
            color: #8892b0;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>牛顿第一定律：惯性演示</h1>
            <div class="subtitle">
                通过交互式动画演示惯性定律：一切物体在没有受到外力作用时，总保持静止状态或匀速直线运动状态
            </div>
            <div class="law-text">
                "任何物体都要保持匀速直线运动或静止状态，直到外力迫使它改变运动状态为止。" —— 牛顿第一定律
            </div>
        </header>
        
        <div class="main-content">
            <div class="simulation-area">
                <h2>实验模拟</h2>
                <div class="canvas-container">
                    <canvas id="simulationCanvas"></canvas>
                </div>
            </div>
            
            <div class="controls-area">
                <div class="control-section">
                    <h3>实验场景</h3>
                    <div class="scene-selector">
                        <button class="scene-btn active" id="scene1Btn">小车撞墙实验</button>
                        <button class="scene-btn" id="scene2Btn">桌布抽离实验</button>
                    </div>
                    <p id="sceneDescription">
                        小车以一定速度向右运动，撞到墙壁后停止，但车上的物体会由于惯性继续向前运动。
                    </p>
                </div>
                
                <div class="control-section">
                    <h3>实验参数</h3>
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>质量</span>
                            <span class="slider-value" id="massValue">2.0 kg</span>
                        </div>
                        <input type="range" id="massSlider" min="0.5" max="5" step="0.5" value="2">
                    </div>
                    
                    <div class="slider-container" id="speedContainer">
                        <div class="slider-label">
                            <span>初始速度</span>
                            <span class="slider-value" id="speedValue">5.0 m/s</span>
                        </div>
                        <input type="range" id="speedSlider" min="1" max="10" step="0.5" value="5">
                    </div>
                    
                    <div class="slider-container" id="pullSpeedContainer" style="display: none;">
                        <div class="slider-label">
                            <span>抽离速度</span>
                            <span class="slider-value" id="pullSpeedValue">中等</span>
                        </div>
                        <input type="range" id="pullSpeedSlider" min="1" max="3" step="1" value="2">
                    </div>
                </div>
                
                <div class="control-section">
                    <h3>实验控制</h3>
                    <div class="button-group">
                        <button class="control-btn primary" id="startBtn">开始实验</button>
                        <button class="control-btn" id="pauseBtn">暂停</button>
                        <button class="control-btn" id="resetBtn">重置</button>
                    </div>
                    
                    <div class="checkbox-group">
                        <div class="checkbox-item">
                            <input type="checkbox" id="showTrajectory" checked>
                            <label for="showTrajectory">显示运动轨迹</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showForces">
                            <label for="showForces">显示受力分析</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="slowMotion">
                            <label for="slowMotion">慢动作模式</label>
                        </div>
                    </div>
                </div>
                
                <div class="control-section">
                    <h3>实时数据</h3>
                    <div class="data-display">
                        <div class="data-item">
                            <div class="data-label">质量</div>
                            <div class="data-value" id="currentMass">2.0 kg</div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">速度</div>
                            <div class="data-value" id="currentSpeed">0.0 m/s</div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">惯性大小</div>
                            <div class="data-value" id="inertiaValue">中</div>
                        </div>
                        <div class="data-item">
                            <div class="data-label">状态</div>
                            <div class="data-value" id="stateValue">静止</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="explanation">
            <h2>惯性原理说明</h2>
            <div class="explanation-content" id="dynamicExplanation">
                惯性是物体保持原有运动状态的性质。当小车撞到墙壁时，小车停止，但车上的物体由于惯性会继续向前运动。质量越大，惯性越大，物体保持原有运动状态的能力越强。
            </div>
            <div class="key-point">
                <strong>教学要点：</strong> 惯性是物体的固有属性，只与物体的质量有关，质量越大，惯性越大。牛顿第一定律也称为惯性定律。
            </div>
        </div>
        
        <footer>
            交互式物理教学动画 | 牛顿第一定律演示 | 设计：教育技术专家
        </footer>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('simulationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        
        // 初始调整Canvas大小
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 实验状态
        let currentScene = 1; // 1: 小车撞墙, 2: 桌布抽离
        let isRunning = false;
        let isPaused = false;
        let animationId = null;
        let time = 0;
        
        // 实验参数
        let mass = 2.0; // kg
        let speed = 5.0; // m/s
        let pullSpeed = 2; // 1:慢, 2:中, 3:快
        
        // 小车撞墙实验状态
        let carX = 0;
        let carY = 0;
        let objectX = 0;
        let objectY = 0;
        let wallX = 0;
        let hasCollided = false;
        let objectFlying = false;
        let objectVx = 0;
        let objectVy = 0;
        const gravity = 0.2;
        
        // 桌布抽离实验状态
        let tableclothX = 0;
        let tableclothWidth = 0;
        let cupX = 0;
        let cupY = 0;
        let cupTilt = 0;
        let isTableclothPulled = false;
        let tableclothSpeed = 0;
        
        // 轨迹点数组
        let trajectoryPoints = [];
        
        // 初始化实验
        function initExperiment() {
            time = 0;
            trajectoryPoints = [];
            
            const canvasWidth = canvas.width;
            const canvasHeight = canvas.height;
            
            if (currentScene === 1) {
                // 小车撞墙实验初始化
                carX = canvasWidth * 0.1;
                carY = canvasHeight * 0.6;
                objectX = carX + 40;
                objectY = carY - 30;
                wallX = canvasWidth * 0.7;
                hasCollided = false;
                objectFlying = false;
                objectVx = 0;
                objectVy = 0;
            } else {
                // 桌布抽离实验初始化
                tableclothWidth = canvasWidth * 0.6;
                tableclothX = canvasWidth * 0.2;
                cupX = canvasWidth * 0.5;
                cupY = canvasHeight * 0.65;
                cupTilt = 0;
                isTableclothPulled = false;
                tableclothSpeed = 0;
            }
            
            updateDataDisplay();
        }
        
        // 更新数据显示
        function updateDataDisplay() {
            document.getElementById('currentMass').textContent = mass.toFixed(1) + ' kg';
            document.getElementById('currentSpeed').textContent = speed.toFixed(1) + ' m/s';
            
            // 根据质量确定惯性大小
            let inertiaLevel = '小';
            if (mass >= 3.5) inertiaLevel = '大';
            else if (mass >= 2.0) inertiaLevel = '中';
            
            document.getElementById('inertiaValue').textContent = inertiaLevel;
            
            // 更新状态显示
            let state = '静止';
            if (currentScene === 1) {
                if (isRunning && !hasCollided) state = '运动中';
                else if (hasCollided && objectFlying) state = '物体飞出';
                else if (hasCollided) state = '已碰撞';
            } else {
                if (isRunning && !isTableclothPulled) state = '准备抽离';
                else if (isTableclothPulled) state = '抽离中';
            }
            
            document.getElementById('stateValue').textContent = state;
        }
        
        // 绘制小车撞墙实验
        function drawCarExperiment() {
            const canvasWidth = canvas.width;
            const canvasHeight = canvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, canvasWidth, canvasHeight);
            
            // 绘制背景
            drawBackground();
            
            // 绘制地面
            ctx.fillStyle = '#37474f';
            ctx.fillRect(0, canvasHeight * 0.7, canvasWidth, canvasHeight * 0.3);
            
            // 绘制墙壁
            ctx.fillStyle = '#546e7a';
            ctx.fillRect(wallX - 10, canvasHeight * 0.3, 20, canvasHeight * 0.4);
            ctx.fillStyle = '#78909c';
            ctx.fillRect(wallX - 5, canvasHeight * 0.35, 10, canvasHeight * 0.3);
            
            // 绘制墙壁标签
            ctx.fillStyle = '#e6f1ff';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('墙壁', wallX, canvasHeight * 0.28);
            
            // 绘制小车
            ctx.fillStyle = '#2196f3';
            ctx.fillRect(carX - 30, carY - 20, 60, 30);
            ctx.fillStyle = '#1976d2';
            ctx.fillRect(carX - 25, carY - 15, 50, 20);
            
            // 绘制车轮
            ctx.fillStyle = '#212121';
            ctx.beginPath();
            ctx.arc(carX - 15, carY + 5, 8, 0, Math.PI * 2);
            ctx.fill();
            ctx.beginPath();
            ctx.arc(carX + 15, carY + 5, 8, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制小车上的物体
            ctx.fillStyle = mass >= 3.5 ? '#f44336' : (mass >= 2.0 ? '#ff9800' : '#4caf50');
            ctx.beginPath();
            ctx.arc(objectX, objectY, 20, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制物体上的质量标签
            ctx.fillStyle = '#ffffff';
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(mass.toFixed(1) + 'kg', objectX, objectY + 5);
            
            // 绘制小车标签
            ctx.fillStyle = '#e6f1ff';
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('小车', carX, carY + 40);
            
            // 如果显示轨迹，绘制轨迹点
            if (document.getElementById('showTrajectory').checked && trajectoryPoints.length > 0) {
                ctx.strokeStyle = 'rgba(255, 152, 0, 0.6)';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(trajectoryPoints[0].x, trajectoryPoints[0].y);
                
                for (let i = 1; i < trajectoryPoints.length; i++) {
                    ctx.lineTo(trajectoryPoints[i].x, trajectoryPoints[i].y);
                }
                ctx.stroke();
                
                // 绘制轨迹点
                for (let point of trajectoryPoints) {
                    ctx.fillStyle = 'rgba(255, 152, 0, 0.8)';
                    ctx.beginPath();
                    ctx.arc(point.x, point.y, 3, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 如果显示受力分析，绘制力箭头
            if (document.getElementById('showForces').checked) {
                // 绘制惯性力箭头（从物体中心向左）
                if (hasCollided && objectFlying) {
                    drawArrow(objectX, objectY, objectX - 60, objectY, '#ff9800', '惯性');
                }
                
                // 绘制重力箭头
                if (objectFlying) {
                    drawArrow(objectX, objectY, objectX, objectY + 40, '#f44336', '重力');
                }
                
                // 绘制运动方向箭头
                if (!hasCollided && isRunning) {
                    drawArrow(carX + 40, carY - 30, carX + 100, carY - 30, '#4caf50', '运动方向');
                }
            }
            
            // 绘制实验标题
            ctx.fillStyle = '#64ffda';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'left';
            ctx.fillText('小车撞墙实验', 20, 30);
            
            // 绘制状态说明
            ctx.fillStyle = '#bbdefb';
            ctx.font = '16px Arial';
            ctx.textAlign = 'left';
            
            let statusText = '状态: ';
            if (!isRunning) statusText += '准备开始';
            else if (!hasCollided) statusText += '小车向墙壁运动';
            else if (objectFlying) statusText += '物体由于惯性继续运动';
            else statusText += '实验结束';
            
            ctx.fillText(statusText, 20, 60);
        }
        
        // 绘制桌布抽离实验
        function drawTableclothExperiment() {
            const canvasWidth = canvas.width;
            const canvasHeight = canvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, canvasWidth, canvasHeight);
            
            // 绘制背景
            drawBackground();
            
            // 绘制桌子
            ctx.fillStyle = '#8d6e63';
            ctx.fillRect(canvasWidth * 0.1, canvasHeight * 0.7, canvasWidth * 0.8, 20);
            ctx.fillStyle = '#a1887f';
            ctx.fillRect(canvasWidth * 0.15, canvasHeight * 0.72, canvasWidth * 0.7, 10);
            
            // 绘制桌布
            ctx.fillStyle = isTableclothPulled ? '#e0e0e0' : '#b39ddb';
            ctx.fillRect(tableclothX, canvasHeight * 0.65, tableclothWidth, canvasHeight * 0.08);
            
            // 绘制桌布图案
            ctx.fillStyle = isTableclothPulled ? '#b0bec5' : '#9575cd';
            for (let i = 0; i < 5; i++) {
                const patternX = tableclothX + (i * tableclothWidth / 5) + tableclothWidth / 10;
                ctx.beginPath();
                ctx.arc(patternX, canvasHeight * 0.69, 5, 0, Math.PI * 2);
                ctx.fill();
            }
            
            // 绘制杯子
            ctx.fillStyle = '#ff9800';
            
            // 应用倾斜效果
            ctx.save();
            ctx.translate(cupX, cupY);
            ctx.rotate(cupTilt * Math.PI / 180);
            
            // 绘制杯身
            ctx.fillRect(-15, -40, 30, 40);
            
            // 绘制杯口
            ctx.fillStyle = '#ffb74d';
            ctx.fillRect(-18, -42, 36, 5);
            
            // 绘制杯内液体
            ctx.fillStyle = '#4caf50';
            ctx.fillRect(-12, -20, 24, 20);
            
            ctx.restore();
            
            // 绘制杯子标签
            ctx.fillStyle = '#ffffff';
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(mass.toFixed(1) + 'kg', cupX, cupY + 30);
            
            // 绘制实验标题
            ctx.fillStyle = '#64ffda';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'left';
            ctx.fillText('桌布抽离实验', 20, 30);
            
            // 绘制状态说明
            ctx.fillStyle = '#bbdefb';
            ctx.font = '16px Arial';
            ctx.textAlign = 'left';
            
            let statusText = '状态: ';
            if (!isRunning) statusText += '准备开始';
            else if (!isTableclothPulled) statusText += '准备抽离桌布';
            else if (cupTilt < 30) statusText += '桌布被快速抽离';
            else statusText += '杯子由于惯性保持静止';
            
            ctx.fillText(statusText, 20, 60);
            
            // 如果显示受力分析，绘制力箭头
            if (document.getElementById('showForces').checked) {
                // 绘制摩擦力箭头
                if (isTableclothPulled) {
                    drawArrow(cupX, cupY - 20, cupX - 50, cupY - 20, '#f44336', '摩擦力');
                }
                
                // 绘制惯性力箭头
                drawArrow(cupX, cupY - 40, cupX, cupY - 80, '#ff9800', '惯性');
                
                // 绘制重力箭头
                drawArrow(cupX, cupY, cupX, cupY + 40, '#2196f3', '重力');
            }
        }
        
        // 绘制背景
        function drawBackground() {
            const canvasWidth = canvas.width;
            const canvasHeight = canvas.height;
            
            // 绘制渐变背景
            const gradient = ctx.createLinearGradient(0, 0, 0, canvasHeight);
            gradient.addColorStop(0, '#0a192f');
            gradient.addColorStop(1, '#112240');
            ctx.fillStyle = gradient;
            ctx.fillRect(0, 0, canvasWidth, canvasHeight);
        }
        
        // 绘制箭头
        function drawArrow(fromX, fromY, toX, toY, color, label) {
            const headlen = 15;
            const angle = Math.atan2(toY - fromY, toX - fromX);
            
            // 绘制箭头线
            ctx.strokeStyle = color;
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.fillStyle = color;
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headlen * Math.cos(angle - Math.PI/6), toY - headlen * Math.sin(angle - Math.PI/6));
            ctx.lineTo(toX - headlen * Math.cos(angle + Math.PI/6), toY - headlen * Math.sin(angle + Math.PI/6));
            ctx.closePath();
            ctx.fill();
            
            // 绘制标签
            ctx.fillStyle = color;
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(label, (fromX + toX) / 2, (fromY + toY) / 2 - 10);
        }
        
        // 更新小车撞墙实验
        function updateCarExperiment() {
            const canvasWidth = canvas.width;
            const timeFactor = document.getElementById('slowMotion').checked ? 0.5 : 1;
            
            if (!hasCollided) {
                // 小车向前移动
                carX += speed * timeFactor;
                objectX = carX + 40;
                
                // 记录轨迹点
                if (time % 5 === 0) {
                    trajectoryPoints.push({x: objectX, y: objectY});
                    
                    // 限制轨迹点数量
                    if (trajectoryPoints.length > 50) {
                        trajectoryPoints.shift();
                    }
                }
                
                // 检测碰撞
                if (carX + 30 >= wallX - 10) {
                    hasCollided = true;
                    objectFlying = true;
                    objectVx = speed * 0.8; // 物体以稍慢的速度继续前进
                    objectVy = -speed * 0.3; // 向上抛射
                }
            } else if (objectFlying) {
                // 物体飞行运动
                objectX += objectVx * timeFactor;
                objectY += objectVy * timeFactor;
                objectVy += gravity * timeFactor;
                
                // 记录轨迹点
                if (time % 2 === 0) {
                    trajectoryPoints.push({x: objectX, y: objectY});
                    
                    // 限制轨迹点数量
                    if (trajectoryPoints.length > 50) {
                        trajectoryPoints.shift();
                    }
                }
                
                // 检测物体落地
                if (objectY > canvas.height * 0.7 - 20) {
                    objectFlying = false;
                    objectY = canvas.height * 0.7 - 20;
                }
            }
            
            time++;
        }
        
        // 更新桌布抽离实验
        function updateTableclothExperiment() {
            const timeFactor = document.getElementById('slowMotion').checked ? 0.5 : 1;
            
            if (isTableclothPulled) {
                // 桌布被抽离
                tableclothX += tableclothSpeed * timeFactor;
                
                // 杯子倾斜效果
                if (cupTilt < 45) {
                    cupTilt += (mass < 2.0 ? 2 : (mass < 3.5 ? 1 : 0.5)) * timeFactor;
                }
                
                // 如果桌布完全抽离，停止实验
                if (tableclothX > canvas.width) {
                    isRunning = false;
                }
            }
            
            time++;
        }
        
        // 动画循环
        function animate() {
            if (isRunning && !isPaused) {
                if (currentScene === 1) {
                    updateCarExperiment();
                    drawCarExperiment();
                } else {
                    updateTableclothExperiment();
                    drawTableclothExperiment();
                }
                
                updateDataDisplay();
            }
            
            animationId = requestAnimationFrame(animate);
        }
        
        // 开始动画循环
        animate();
        
        // 初始化实验
        initExperiment();
        
        // DOM元素引用
        const scene1Btn = document.getElementById('scene1Btn');
        const scene2Btn = document.getElementById('scene2Btn');
        const sceneDescription = document.getElementById('sceneDescription');
        const massSlider = document.getElementById('massSlider');
        const massValue = document.getElementById('massValue');
        const speedSlider = document.getElementById('speedSlider');
        const speedValue = document.getElementById('speedValue');
        const pullSpeedSlider = document.getElementById('pullSpeedSlider');
        const pullSpeedValue = document.getElementById('pullSpeedValue');
        const startBtn = document.getElementById('startBtn');
        const pauseBtn = document.getElementById('pauseBtn');
        const resetBtn = document.getElementById('resetBtn');
        const speedContainer = document.getElementById('speedContainer');
        const pullSpeedContainer = document.getElementById('pullSpeedContainer');
        
        // 场景切换
        scene1Btn.addEventListener('click', function() {
            currentScene = 1;
            scene1Btn.classList.add('active');
            scene2Btn.classList.remove('active');
            sceneDescription.textContent = '小车以一定速度向右运动，撞到墙壁后停止，但车上的物体会由于惯性继续向前运动。';
            speedContainer.style.display = 'block';
            pullSpeedContainer.style.display = 'none';
            initExperiment();
            updateExplanation();
        });
        
        scene2Btn.addEventListener('click', function() {
            currentScene = 2;
            scene2Btn.classList.add('active');
            scene1Btn.classList.remove('active');
            sceneDescription.textContent = '快速抽离桌布，由于惯性，杯子会保持静止状态，留在原处。';
            speedContainer.style.display = 'none';
            pullSpeedContainer.style.display = 'block';
           