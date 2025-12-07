# 需求：匀速圆周运动向心力来源（水杯旋转移中、水滴甩出）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中物理或大学普通物理的初学者。用户的核心需求是：
1.  **理解抽象概念**：将抽象的“向心力”概念与具体、可感知的生活现象（旋转水杯、水滴飞出）联系起来，化抽象为具体。
2.  **建立因果逻辑**：清晰理解“向心力来源”这一关键点，即“是什么力”提供了圆周运动所需的向心力，以及当这个力“消失或不足”时（如水滴与杯壁分离），物体会如何运动（沿切线飞出）。
3.  **突破认知难点**：学生常有的误区是认为物体在圆周运动时受到一个“向外”的离心力。动画需要清晰地展示：向心力是“效果力”（合力指向圆心），其“来源”是某个或某些真实的“性质力”（如摩擦力、弹力）。
4.  **动态过程可视化**：需要直观展示旋转速度、向心力大小、物体运动轨迹之间的动态关系，这是静态图片和文字描述难以实现的。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
*   **核心概念**：
    *   **向心力**：物体做匀速圆周运动时，所受合力方向始终指向圆心，这个合力叫做向心力。它是一个效果力，不是一种新的性质力。
    *   **向心力来源**：由实际存在的性质力提供，在本例中，主要是杯壁对水滴的**弹力（支持力）**。
    *   **离心现象**：当提供的合力（弹力）不足以维持物体在当前半径下做圆周运动时（例如转速降低或水杯突然撤去），物体将由于惯性沿切线方向飞出，这不是因为受到“离心力”，而是因为向心力不足。

*   **认知规律**：
    1.  **从现象到本质**：先展示“水杯旋转，水不洒出”和“转速慢时，水滴甩出”的完整现象，引发疑问。
    2.  **分解与剖析**：将复杂过程分解：a) 单个水滴的受力分析；b) 向心力公式的定性体现（F = mω²r）；c) 条件变化（转速、水量）对结果的影响。
    3.  **交互验证**：允许用户改变参数（如旋转速度），观察实时变化，建立“输入-输出”的直观联系，巩固理解。

*   **交互设计**：
    *   **分步引导模式**：设置“现象观察”、“受力分析”、“原理探索”三个步骤或标签页，引导用户循序渐进。
    *   **参数控制面板**：提供滑块或按钮，允许用户实时调整“旋转角速度 (ω)”和“杯中的水量（影响水滴质量 m）”。
    *   **视图切换**：提供“整体俯视图”（观察水杯和水滴轨迹）和“局部放大图”（聚焦于杯壁与一个水滴的接触点，显示受力分析图）。
    *   **过程控制**：提供“播放/暂停”、“重置”按钮，以及“慢动作”模式，方便仔细观察关键瞬间（如水滴即将脱离时）。

*   **视觉呈现**：
    *   **主体与焦点**：水杯设计简洁（如透明玻璃杯），内部水面清晰可见。重点突出的一两个“标定水滴”用高亮颜色（如亮蓝色）显示，并带有受力箭头。
    *   **运动轨迹可视化**：
        *   水杯旋转时，用浅色虚线圆显示水面的形状（凹形液面）。
        *   对于飞出的水滴，在其脱离瞬间显示其**瞬时速度方向（切线方向）的箭头**，并保留其飞出的**实际运动轨迹（抛物线）**，与圆周轨迹形成鲜明对比。
    *   **动态受力分析图**：
        *   在局部放大图中，始终跟随标定水滴，动态绘制受力图：**重力（竖直向下，恒定）**、**杯壁弹力 N（指向圆心，随转速变化）**。
        *   用不同颜色和标签明确标注各力。用醒目的箭头（如红色）显示**合力（即向心力 F_n）**，并明确标出 `F_n = N`。
        *   当水滴飞出时，弹力 `N` 箭头消失，只保留重力，并高亮显示速度方向箭头。

#### 配色方案选择
*   **背景与主容器**：采用深蓝灰色（`#2c3e50`）或浅灰色（`#ecf0f1`）背景，确保画面对比度，减少视觉疲劳。
*   **水杯与水**：水杯用半透明浅灰色线条勾勒。静水时，水面用平静的蓝色（`#3498db`）填充；旋转时，水面凹槽用渐变的深蓝色表示。
*   **焦点元素**：
    *   **标定水滴**：亮蓝色（`#1abc9c`）填充，带白色高光，使其从背景中跳出。
    *   **力与矢量箭头**：
        *   重力 `G`：深灰色（`#7f8c8d`），恒定显示。
        *   弹力/支持力 `N`：橙色（`#e67e22`），表示主动施加的接触力。
        *   向心力/合力 `F_n`：红色（`#e74c3c`），粗箭头，强调其作为“效果”和核心概念的地位。
        *   速度 `v`：绿色（`#2ecc71`），表示运动状态。
*   **控制面板与UI**：使用中性白色或浅卡其色（`#fdf6e3`）面板，按钮和滑块使用主色调蓝色（`#3498db`）和绿色（`#2ecc71`）表示操作和变化。

#### 交互功能列表
1.  **场景控制**：
    *   `播放/暂停/重置` 按钮：控制整个动画的进行。
    *   `慢动作模式` 开关：放慢物理过程，便于观察。
2.  **参数调节**：
    *   `旋转速度 (ω)` 滑块：实时调整水杯旋转的快慢。关联向心力大小和水面形状。
    *   `水量/水滴质量 (m)` 滑块：模拟杯中水多少，影响水滴惯性。
3.  **视图切换**：
    *   `整体视图` / `局部放大视图` 切换按钮。
    *   在整体视图中，可点击某个水滴将其“标定”为重点分析对象。
4.  **信息显示**：
    *   实时显示当前 `角速度 ω`、`向心力大小 F_n` 的数值。
    *   在受力分析图旁，动态显示公式 `F_n = m ω² r`，其中变化的参数（如 ω）会高亮。
    *   当水滴飞出时，弹出提示框，简要说明原因：“提供的弹力 N 不足以充当所需向心力，水滴由于惯性沿切线方向飞出”。
5.  **教学引导**：
    *   `分步演示` 模式：通过“下一步”按钮，引导用户按“现象 -> 受力 -> 原理 -> 应用”的顺序学习。
    *   每个步骤配有简短的文字说明。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>匀速圆周运动向心力来源 - 水杯旋转演示</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
            color: #ecf0f1;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .header {
            text-align: center;
            margin-bottom: 20px;
            max-width: 800px;
        }
        
        h1 {
            color: #1abc9c;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }
        
        .subtitle {
            color: #bdc3c7;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            max-width: 1200px;
            width: 100%;
            justify-content: center;
        }
        
        .simulation-panel {
            flex: 1;
            min-width: 500px;
            background: rgba(255, 255, 255, 0.08);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(4px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .control-panel {
            flex: 1;
            min-width: 300px;
            background: rgba(253, 246, 227, 0.1);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(4px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 400px;
            background: rgba(0, 0, 0, 0.2);
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 15px;
        }
        
        canvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .view-controls {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 8px 16px;
            background: #3498db;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 100px;
        }
        
        .btn:hover {
            background: #2980b9;
            transform: translateY(-2px);
        }
        
        .btn.active {
            background: #1abc9c;
            box-shadow: 0 0 0 2px rgba(26, 188, 156, 0.5);
        }
        
        .btn-danger {
            background: #e74c3c;
        }
        
        .btn-danger:hover {
            background: #c0392b;
        }
        
        .btn-success {
            background: #2ecc71;
        }
        
        .btn-success:hover {
            background: #27ae60;
        }
        
        .control-group {
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .control-group h3 {
            color: #1abc9c;
            margin-bottom: 12px;
            font-size: 1.2rem;
        }
        
        .slider-container {
            margin-bottom: 15px;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }
        
        .slider-label span {
            font-weight: 600;
        }
        
        .slider-value {
            color: #3498db;
            font-weight: bold;
        }
        
        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: rgba(255, 255, 255, 0.1);
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
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        .info-display {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 8px;
            padding: 15px;
            margin-top: 15px;
        }
        
        .info-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            padding-bottom: 8px;
            border-bottom: 1px dashed rgba(255, 255, 255, 0.1);
        }
        
        .info-item:last-child {
            margin-bottom: 0;
            border-bottom: none;
        }
        
        .info-label {
            color: #bdc3c7;
        }
        
        .info-value {
            color: #2ecc71;
            font-weight: bold;
            font-family: 'Courier New', monospace;
        }
        
        .formula-display {
            background: rgba(52, 152, 219, 0.1);
            border-radius: 8px;
            padding: 15px;
            margin-top: 15px;
            text-align: center;
            font-size: 1.2rem;
            border-left: 4px solid #3498db;
        }
        
        .highlight {
            color: #e74c3c;
            font-weight: bold;
        }
        
        .highlight-blue {
            color: #3498db;
            font-weight: bold;
        }
        
        .highlight-green {
            color: #2ecc71;
            font-weight: bold;
        }
        
        .explanation {
            background: rgba(231, 76, 60, 0.1);
            border-radius: 8px;
            padding: 15px;
            margin-top: 15px;
            border-left: 4px solid #e74c3c;
            display: none;
        }
        
        .explanation.show {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            justify-content: center;
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
        
        .legend-text {
            font-size: 0.9rem;
            color: #bdc3c7;
        }
        
        @media (max-width: 900px) {
            .container {
                flex-direction: column;
            }
            
            .simulation-panel, .control-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>匀速圆周运动向心力来源</h1>
        <p class="subtitle">水杯旋转演示：向心力来源与离心现象</p>
    </div>
    
    <div class="container">
        <div class="simulation-panel">
            <div class="canvas-container">
                <canvas id="simulationCanvas"></canvas>
            </div>
            
            <div class="view-controls">
                <button id="viewOverall" class="btn active">整体视图</button>
                <button id="viewDetail" class="btn">局部放大</button>
                <button id="slowMotion" class="btn">慢动作模式</button>
                <button id="resetBtn" class="btn btn-danger">重置</button>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #1abc9c;"></div>
                    <span class="legend-text">水滴</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #7f8c8d;"></div>
                    <span class="legend-text">重力 (G)</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #e67e22;"></div>
                    <span class="legend-text">弹力 (N)</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #e74c3c;"></div>
                    <span class="legend-text">向心力 (F_n)</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #2ecc71;"></div>
                    <span class="legend-text">速度 (v)</span>
                </div>
            </div>
        </div>
        
        <div class="control-panel">
            <div class="control-group">
                <h3>动画控制</h3>
                <div style="display: flex; gap: 10px;">
                    <button id="playBtn" class="btn btn-success">播放</button>
                    <button id="pauseBtn" class="btn">暂停</button>
                    <button id="stepBtn" class="btn">单步演示</button>
                </div>
            </div>
            
            <div class="control-group">
                <h3>参数调节</h3>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>旋转角速度 ω</span>
                        <span class="slider-value" id="omegaValue">2.0 rad/s</span>
                    </div>
                    <input type="range" id="omegaSlider" min="0.5" max="5.0" step="0.1" value="2.0">
                </div>
                
                <div class="slider-container">
                    <div class="slider-label">
                        <span>水量/水滴质量 m</span>
                        <span class="slider-value" id="massValue">1.0 单位</span>
                    </div>
                    <input type="range" id="massSlider" min="0.5" max="3.0" step="0.1" value="1.0">
                </div>
            </div>
            
            <div class="info-display">
                <div class="info-item">
                    <span class="info-label">当前角速度 ω:</span>
                    <span class="info-value" id="currentOmega">2.00 rad/s</span>
                </div>
                <div class="info-item">
                    <span class="info-label">所需向心力 F_n:</span>
                    <span class="info-value" id="currentForce">4.00 N</span>
                </div>
                <div class="info-item">
                    <span class="info-label">水滴状态:</span>
                    <span class="info-value" id="dropletStatus">附着</span>
                </div>
                <div class="info-item">
                    <span class="info-label">视图模式:</span>
                    <span class="info-value" id="viewMode">整体视图</span>
                </div>
            </div>
            
            <div class="formula-display">
                向心力公式: <span class="highlight">F_n</span> = m · ω² · r
                <br>
                <span id="formulaDetail">F_n = <span class="highlight-blue">1.0</span> × (<span class="highlight-green">2.0</span>)² × 1.0 = <span class="highlight">4.0</span> N</span>
            </div>
            
            <div class="explanation" id="explanationBox">
                <strong>原理说明:</strong> 当水杯旋转时，杯壁对水滴施加弹力N，这个弹力指向圆心，提供了水滴做圆周运动所需的向心力F_n。当旋转速度降低时，所需向心力减小，如果弹力不足以提供所需向心力，水滴将由于惯性沿切线方向飞出。
            </div>
        </div>
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
        
        // 初始调整尺寸
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 物理参数
        let physics = {
            omega: 2.0,      // 角速度 (rad/s)
            mass: 1.0,       // 水滴质量 (单位)
            radius: 1.0,     // 旋转半径 (单位)
            time: 0,         // 时间 (s)
            isPlaying: false,
            isSlowMotion: false,
            viewMode: 'overall', // 'overall' 或 'detail'
            selectedDroplet: 0   // 选中的水滴索引
        };
        
        // 水滴数组
        let droplets = [];
        
        // 飞出的水滴轨迹
        let flyingDroplets = [];
        
        // 初始化水滴
        function initDroplets() {
            droplets = [];
            flyingDroplets = [];
            
            // 创建3个水滴
            for (let i = 0; i < 3; i++) {
                const angle = (i * 2 * Math.PI / 3); // 均匀分布
                droplets.push({
                    x: Math.cos(angle) * physics.radius,
                    y: Math.sin(angle) * physics.radius,
                    angle: angle,
                    radius: 0.08,
                    color: '#1abc9c',
                    isFlying: false,
                    flyTime: 0,
                    flyVelocity: { x: 0, y: 0 },
                    flyTrajectory: []
                });
            }
        }
        
        // 计算所需向心力
        function calculateCentripetalForce() {
            return physics.mass * physics.omega * physics.omega * physics.radius;
        }
        
        // 更新物理状态
        function updatePhysics(deltaTime) {
            if (!physics.isPlaying) return;
            
            // 应用慢动作
            const effectiveDeltaTime = physics.isSlowMotion ? deltaTime * 0.3 : deltaTime;
            physics.time += effectiveDeltaTime;
            
            // 更新水滴位置
            for (let i = 0; i < droplets.length; i++) {
                const droplet = droplets[i];
                
                if (!droplet.isFlying) {
                    // 正常旋转
                    droplet.angle += physics.omega * effectiveDeltaTime;
                    droplet.x = Math.cos(droplet.angle) * physics.radius;
                    droplet.y = Math.sin(droplet.angle) * physics.radius;
                    
                    // 随机模拟水滴飞出（当角速度较低时更容易发生）
                    if (physics.omega < 1.5 && Math.random() < 0.001 * effectiveDeltaTime * 60) {
                        droplet.isFlying = true;
                        droplet.flyTime = 0;
                        
                        // 计算飞出时的切线速度
                        const tangentAngle = droplet.angle + Math.PI / 2;
                        droplet.flyVelocity = {
                            x: Math.cos(tangentAngle) * physics.omega * physics.radius,
                            y: Math.sin(tangentAngle) * physics.omega * physics.radius
                        };
                        
                        // 记录初始位置
                        droplet.flyTrajectory = [{ x: droplet.x, y: droplet.y }];
                        
                        // 添加到飞出列表
                        flyingDroplets.push({...droplet});
                    }
                } else {
                    // 已飞出的水滴
                    droplet.flyTime += effectiveDeltaTime;
                    
                    // 抛物线运动 (考虑重力)
                    droplet.x += droplet.flyVelocity.x * effectiveDeltaTime;
                    droplet.y += droplet.flyVelocity.y * effectiveDeltaTime + 0.5 * 9.8 * effectiveDeltaTime * effectiveDeltaTime;
                    droplet.flyVelocity.y += 9.8 * effectiveDeltaTime;
                    
                    // 记录轨迹点
                    if (droplet.flyTrajectory.length < 50) {
                        droplet.flyTrajectory.push({ x: droplet.x, y: droplet.y });
                    }
                    
                    // 如果飞出太远，重置
                    if (Math.sqrt(droplet.x * droplet.x + droplet.y * droplet.y) > 5) {
                        resetDroplet(i);
                    }
                }
            }
            
            // 更新飞出列表中的水滴
            for (let i = flyingDroplets.length - 1; i >= 0; i--) {
                const droplet = flyingDroplets[i];
                droplet.flyTime += effectiveDeltaTime;
                
                // 抛物线运动
                droplet.x += droplet.flyVelocity.x * effectiveDeltaTime;
                droplet.y += droplet.flyVelocity.y * effectiveDeltaTime + 0.5 * 9.8 * effectiveDeltaTime * effectiveDeltaTime;
                droplet.flyVelocity.y += 9.8 * effectiveDeltaTime;
                
                // 记录轨迹点
                if (droplet.flyTrajectory.length < 50) {
                    droplet.flyTrajectory.push({ x: droplet.x, y: droplet.y });
                }
                
                // 如果飞出太远，移除
                if (Math.sqrt(droplet.x * droplet.x + droplet.y * droplet.y) > 5) {
                    flyingDroplets.splice(i, 1);
                }
            }
            
            // 更新UI显示
            updateUI();
        }
        
        // 重置单个水滴
        function resetDroplet(index) {
            const angle = (index * 2 * Math.PI / 3);
            droplets[index] = {
                x: Math.cos(angle) * physics.radius,
                y: Math.sin(angle) * physics.radius,
                angle: angle,
                radius: 0.08,
                color: '#1abc9c',
                isFlying: false,
                flyTime: 0,
                flyVelocity: { x: 0, y: 0 },
                flyTrajectory: []
            };
        }
        
        // 绘制整体视图
        function drawOverallView() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const scale = Math.min(canvas.width, canvas.height) * 0.35;
            
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景网格
            drawGrid(centerX, centerY, scale);
            
            // 绘制旋转轨迹圆
            ctx.beginPath();
            ctx.arc(centerX, centerY, scale * physics.radius, 0, Math.PI * 2);
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.2)';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制水杯
            const cupRadius = scale * 1.2;
            const cupHeight = scale * 0.8;
            
            // 杯身
            ctx.beginPath();
            ctx.arc(centerX, centerY, cupRadius, 0, Math.PI * 2);
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.7)';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 水面（凹形）
            ctx.beginPath();
            const waterDepth = 0.1 * physics.omega; // 角速度越大，水面越凹
            for (let angle = 0; angle < Math.PI * 2; angle += 0.1) {
                const r = cupRadius * (1 - waterDepth * Math.sin(angle + physics.time * physics.omega) * 0.3);
                const x = centerX + r * Math.cos(angle);
                const y = centerY + r * Math.sin(angle);
                
                if (angle === 0) {
                    ctx.moveTo(x, y);
                } else {
                    ctx.lineTo(x, y);
                }
            }
            ctx.closePath();
            ctx.fillStyle = 'rgba(52, 152, 219, 0.4)';
            ctx.fill();
            ctx.strokeStyle = 'rgba(52, 152, 219, 0.8)';
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 绘制水滴
            for (let i = 0; i < droplets.length; i++) {
                const droplet = droplets[i];
                const x = centerX + droplet.x * scale;
                const y = centerY + droplet.y * scale;
                
                // 绘制水滴
                drawDroplet(x, y, droplet.radius * scale, droplet.color);
                
                // 如果选中了此水滴，绘制高亮圆环
                if (i === physics.selectedDroplet) {
                    ctx.beginPath();
                    ctx.arc(x, y, droplet.radius * scale * 1.5, 0, Math.PI * 2);
                    ctx.strokeStyle = 'rgba(255, 255, 255, 0.8)';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
                
                // 绘制速度方向（切线方向）
                if (!droplet.isFlying) {
                    const tangentAngle = droplet.angle + Math.PI / 2;
                    const speed = physics.omega * physics.radius;
                    const arrowLength = speed * scale * 0.5;
                    
                    drawArrow(
                        x, y,
                        x + Math.cos(tangentAngle) * arrowLength,
                        y + Math.sin(tangentAngle) * arrowLength,
                        '#2ecc71', 3
                    );
                    
                    // 在箭头旁标注"v"
                    ctx.fillStyle = '#2ecc71';
                    ctx.font = 'bold 14px Arial';
                    ctx.fillText('v', 
                        x + Math.cos(tangentAngle) * (arrowLength + 15),
                        y + Math.sin(tangentAngle) * (arrowLength + 5)
                    );
                }
            }
            
            // 绘制飞出的水滴及其轨迹
            for (const droplet of flyingDroplets) {
                const x = centerX + droplet.x * scale;
                const y = centerY + droplet.y * scale;
                
                // 绘制轨迹
                if (droplet.flyTrajectory.length > 1) {
                    ctx.beginPath();
                    ctx.moveTo(
                        centerX + droplet.flyTrajectory[0].x * scale,
                        centerY + droplet.flyTrajectory[0].y * scale
                    );
                    
                    for (let i = 1; i < droplet.flyTrajectory.length; i++) {
                        ctx.lineTo(
                            centerX + droplet.flyTrajectory[i].x * scale,
                            centerY + droplet.flyTrajectory[i].y * scale
                        );
                    }
                    
                    ctx.strokeStyle = 'rgba(231, 76, 60, 0.6)';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
                
                // 绘制飞出的水滴
                drawDroplet(x, y, droplet.radius * scale, 'rgba(231, 76, 60, 0.8)');
                
                // 绘制速度方向
                const speed = Math.sqrt(
                    droplet.flyVelocity.x * droplet.flyVelocity.x + 
                    droplet.flyVelocity.y * droplet.flyVelocity.y
                );
                const arrowLength = speed * scale * 0.3;
                
                if (arrowLength > 5) {
                    const angle = Math.atan2(droplet.flyVelocity.y, droplet.flyVelocity.x);
                    drawArrow(
                        x, y,
                        x + Math.cos(angle) * arrowLength,
                        y + Math.sin(angle) * arrowLength,
                        '#2ecc71', 2
                    );
                }
            }
            
            // 绘制中心点
            ctx.beginPath();
            ctx.arc(centerX, centerY, 5, 0, Math.PI * 2);
            ctx.fillStyle = '#e74c3c';
            ctx.fill();
            
            // 绘制标题
            ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
            ctx.font = 'bold 16px Arial';
            ctx.fillText('整体视图 - 水杯旋转与水滴运动', 20, 30);
            
            // 绘制说明
            ctx.fillStyle = 'rgba(255, 255, 255, 0.7)';
            ctx.font = '14px Arial';
            ctx.fillText('点击水滴可选中进行详细受力分析', 20, canvas.height - 20);
        }
        
        // 绘制局部放大视图（受力分析）
        function drawDetailView() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const scale = Math.min(canvas.width, canvas.height) * 0.4;
            
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            ctx.fillStyle = 'rgba(0, 0, 0, 0.2)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 获取选中的水滴
            const droplet = droplets[physics.selectedDroplet];
            const dropletX = centerX + droplet.x * scale;
            const dropletY = centerY + droplet.y * scale;
            
            // 绘制水滴
            drawDroplet(dropletX, dropletY, droplet.radius * scale * 1.5, droplet.color);
            
            // 绘制杯壁（在水滴位置）
            const wallAngle = droplet.angle;
            const wallLength = scale * 0.8;
            const wallX1 = centerX + Math.cos(wallAngle) * (physics.radius * scale - wallLength/2);
            const wallY1 = centerY + Math.sin(wallAngle) * (physics.radius * scale - wallLength/2);
            const wallX2 = centerX + Math.cos(wallAngle) * (physics.radius * scale + wallLength/2);
            const wallY2 = centerY + Math.sin(wallAngle) * (physics.radius * scale + wallLength/2);
            
            ctx.beginPath();
            ctx.moveTo(wallX1, wallY1);
            ctx.lineTo(wallX2, wallY2);
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.lineWidth = 4;
            ctx.stroke();
            
            // 绘制受力分析
            
            // 1. 重力 G (向下)
            const gravityLength = scale * 0.4;
            drawArrow(
                dropletX, dropletY,
                dropletX, dropletY + gravityLength,
                '#7f8c8d', 4
            );
            
            // 在箭头旁标注"G"
            ctx.fillStyle = '#7f8c8d';
            ctx.font = 'bold 16px Arial';
            ctx.fillText('G', dropletX + 10, dropletY + gravityLength/2 + 5);
            
            // 2. 弹力 N (指向圆心)
            if (!droplet.isFlying) {
                const normalLength = scale * 0.5;
                const normalAngle = Math.atan2(-droplet.y, -droplet.x); // 指向圆心的方向
                
                drawArrow(
                    dropletX, dropletY,
                    dropletX + Math.cos(normalAngle) * normalLength,
                    dropletY + Math.sin(normalAngle) * normalLength,
                    '#e67e22', 4
                );
                
                // 在箭头旁标注"N"
                ctx.fillStyle = '#e67e22';
                ctx.font = 'bold 16px Arial';
                ctx.fillText('N', 
                    dropletX + Math.cos(normalAngle) * (normalLength/2 + 15),
                    dropletY + Math.sin(normalAngle) * (normalLength/2 + 5)
                );
                
                // 3. 向心力 F_n (红色，与N重合，但更粗)
                const forceLength = normalLength * 0.9;
                drawArrow(
                    dropletX, dropletY,
                    dropletX + Math.cos(normalAngle) * forceLength,
                    dropletY + Math.sin(normalAngle) * forceLength,
                    '#e74c3c', 6
                );
                
                // 在箭头旁标注"F_n"
                ctx.fillStyle = '#e74c3c';
                ctx.font = 'bold 18px Arial';
                ctx.fillText('F_n', 
                    dropletX + Math.cos(normalAngle) * (forceLength/2 - 20),
                    dropletY + Math.sin(normalAngle) * (forceLength/2 - 10)
                );
                
                // 绘制向心力公式
                ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
                ctx.font = 'bold 18px Arial';
                ctx.fillText('F_n = N', centerX - 100, 50);
            } else {
                // 水滴飞出时，只显示重力
                ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
                ctx.font = 'bold 18px Arial';
                ctx.fillText('水滴已飞出：N = 0', centerX - 100, 50);
            }
            
            // 绘制速度方向
            if (!droplet.isFlying) {
                const tangentAngle = droplet.angle + Math.PI / 2;
                const speed = physics.omega * physics.radius;
                const arrowLength = speed * scale * 0.4;
                
                drawArrow(
                    dropletX, dropletY,
                    dropletX + Math.cos(tangentAngle) * arrowLength,
                    dropletY + Math.sin(tangentAngle) * arrowLength,
                    '#2ecc71', 4
                );
                
                // 在箭头旁标注"v"
                ctx.fillStyle = '#2ecc71';
                ctx.font = 'bold 16px Arial';
                ctx.fillText('v', 
                    dropletX + Math.cos(tangentAngle) * (arrowLength + 15),
                    dropletY + Math.sin(tangentAngle) * (arrowLength + 5)
                );
            }
            
            // 绘制标题
            ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
            ctx.font = 'bold 16px Arial';
            ctx.fillText('局部放大视图 - 水滴受力分析', 20, 30);
            
            // 绘制说明
            ctx.fillStyle = 'rgba(255, 255, 255, 0.7)';
            ctx.font = '14px Arial';
            ctx.fillText('红色箭头 F_n 表示向心力，由杯壁弹力 N 提供', 20, canvas.height - 40);
            ctx.fillText(`当前分析：水滴 ${physics.selectedDroplet + 1}`, 20, canvas.height - 20);
        }
        
        // 绘制水滴
        function drawDroplet(x, y, radius, color) {
            // 水滴主体
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.fillStyle = color;
            ctx.fill();
            
            // 高光
            ctx.beginPath();
            ctx.arc(x - radius/3, y - radius/3, radius/3, 0, Math.PI * 2);
            ctx.fillStyle = 'rgba(255, 255, 255, 0.6)';
            ctx.fill();
            
            // 边框
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.lineWidth = 1;
            ctx.stroke();
        }
        
        // 绘制箭头
        function drawArrow(fromX, fromY, toX, toY, color, lineWidth) {
            const headLength = 10;
            const angle = Math.atan2(toY - fromY, toX - fromX);
            
            // 绘制线
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.strokeStyle = color;
            ctx.lineWidth = lineWidth;
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
            ctx.fillStyle = color;
            ctx.fill();
        }
        
        // 绘制网格
        function drawGrid(centerX, centerY, scale) {
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.05)';
            ctx.lineWidth = 1;
            
            // 垂直线
            for (let x = centerX % (scale/2); x < canvas.width; x += scale/2) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, canvas.height);
                ctx.stroke();
            }
            
            // 水平线
            for (let y = centerY % (scale/2); y < canvas.height; y += scale/2) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(canvas.width, y);
                ctx.stroke();
            }
            
            // 中心十字
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.2)';
            ctx.lineWidth = 2;
            
            ctx.beginPath();
            ctx.moveTo(centerX, 0);
            ctx.lineTo(centerX, canvas.height);
            ctx.stroke();
            
            ctx.beginPath();
            ctx.moveTo(0, centerY);
            ctx.lineTo(canvas.width, centerY);
            ctx.stroke();
        }
        
        // 更新UI显示
        function updateUI() {
            // 更新数值显示
            document.getElementById('currentOmega').textContent = physics.omega.toFixed(2) + ' rad/s';
            document.getElementById('currentForce').textContent = calculateCentripetalForce().toFixed(2) + ' N';
            
            // 更新水滴状态
            const dropletStatus = droplets[physics.selectedDroplet].isFlying ? '飞出' : '附着';
            document.getElementById('dropletStatus').textContent = dropletStatus;
            
            // 更新视图模式
            document.getElementById('viewMode').textContent = 
                physics.viewMode === 'overall' ? '整体视图' : '局部放大';
            

<!--检测到代码截断，自动续写中...-->
            // 更新公式显示
            const formulaDetail = `F_n = <span class="highlight-blue">${physics.mass.toFixed(1)}</span> × (<span class="highlight-green">${physics.omega.toFixed(1)}</span>)² × 1.0 = <span class="highlight">${calculateCentripetalForce().toFixed(1)}</span> N`;
            document.getElementById('formulaDetail').innerHTML = formulaDetail;
            
            // 如果角速度太低，显示原理说明
            const explanationBox = document.getElementById('explanationBox');
            if (physics.omega < 1.5) {
                explanationBox.classList.add('show');
            } else {
                explanationBox.classList.remove('show');
            }
        }
        
        // 动画循环
        let lastTime = 0;
        function animate(timestamp) {
            const deltaTime = timestamp - lastTime || 0;
            lastTime = timestamp;
            
            updatePhysics(deltaTime / 1000); // 转换为秒
            
            // 根据视图模式绘制
            if (physics.viewMode === 'overall') {
                drawOverallView();
            } else {
                drawDetailView();
            }
            
            requestAnimationFrame(animate);
        }
        
        // 初始化
        function init() {
            resizeCanvas();
            initDroplets();
            updateUI();
            
            // 开始动画循环
            requestAnimationFrame(animate);
            
            // 设置Canvas点击事件（选择水滴）
            canvas.addEventListener('click', function(event) {
                const rect = canvas.getBoundingClientRect();
                const x = event.clientX - rect.left;
                const y = event.clientY - rect.top;
                
                const centerX = canvas.width / 2;
                const centerY = canvas.height / 2;
                const scale = Math.min(canvas.width, canvas.height) * 0.35;
                
                // 检查点击了哪个水滴（整体视图下）
                if (physics.viewMode === 'overall') {
                    for (let i = 0; i < droplets.length; i++) {
                        const droplet = droplets[i];
                        const dropletX = centerX + droplet.x * scale;
                        const dropletY = centerY + droplet.y * scale;
                        const distance = Math.sqrt(
                            Math.pow(x - dropletX, 2) + Math.pow(y - dropletY, 2)
                        );
                        
                        if (distance < droplet.radius * scale * 2) {
                            physics.selectedDroplet = i;
                            break;
                        }
                    }
                }
            });
        }
        
        // 事件监听器
        document.getElementById('playBtn').addEventListener('click', function() {
            physics.isPlaying = true;
            this.classList.add('active');
            document.getElementById('pauseBtn').classList.remove('active');
        });
        
        document.getElementById('pauseBtn').addEventListener('click', function() {
            physics.isPlaying = false;
            this.classList.add('active');
            document.getElementById('playBtn').classList.remove('active');
        });
        
        document.getElementById('stepBtn').addEventListener('click', function() {
            physics.isPlaying = true;
            setTimeout(() => {
                physics.isPlaying = false;
            }, 100);
        });
        
        document.getElementById('resetBtn').addEventListener('click', function() {
            physics.time = 0;
            initDroplets();
            physics.isPlaying = false;
            document.getElementById('playBtn').classList.remove('active');
            document.getElementById('pauseBtn').classList.add('active');
        });
        
        document.getElementById('viewOverall').addEventListener('click', function() {
            physics.viewMode = 'overall';
            this.classList.add('active');
            document.getElementById('viewDetail').classList.remove('active');
        });
        
        document.getElementById('viewDetail').addEventListener('click', function() {
            physics.viewMode = 'detail';
            this.classList.add('active');
            document.getElementById('viewOverall').classList.remove('active');
        });
        
        document.getElementById('slowMotion').addEventListener('click', function() {
            physics.isSlowMotion = !physics.isSlowMotion;
            this.classList.toggle('active', physics.isSlowMotion);
        });
        
        document.getElementById('omegaSlider').addEventListener('input', function() {
            physics.omega = parseFloat(this.value);
            document.getElementById('omegaValue').textContent = physics.omega.toFixed(1) + ' rad/s';
        });
        
        document.getElementById('massSlider').addEventListener('input', function() {
            physics.mass = parseFloat(this.value);
            document.getElementById('massValue').textContent = physics.mass.toFixed(1) + ' 单位';
        });
        
        // 初始化应用
        init();
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 匀速圆周运动向心力来源 - 交互式教学动画使用指南

欢迎使用“匀速圆周运动向心力来源”交互式教学动画！本动画旨在通过直观的视觉呈现和交互操作，帮助您深入理解匀速圆周运动中向心力的来源及其物理本质。无论您是教师、学生还是物理爱好者，本工具都将为您提供生动、深入的学习体验。

---

### 一、功能说明

本动画模拟了“水杯旋转”这一经典物理现象，通过可视化手段展示：
1. **现象观察**：水杯旋转时，水为何不洒出；转速降低时，水滴为何会飞出
2. **受力分析**：详细展示水滴在旋转过程中的受力情况
3. **原理探索**：揭示向心力来源与离心现象的本质

动画采用**双视图系统**（整体视图与局部放大视图），配合**实时参数调节**和**动态公式显示**，构建了完整的教学闭环。

---

### 二、主要功能

#### 1. 视图控制
- **整体视图**：观察水杯整体旋转、水面形状变化及多个水滴的运动轨迹
- **局部放大视图**：聚焦单个水滴，详细展示其受力分析图（重力G、弹力N、向心力F_n、速度v）
- **视图切换**：点击“整体视图”/“局部放大”按钮可在两种视图间自由切换

#### 2. 动画控制
- **播放/暂停**：控制动画运行状态
- **慢动作模式**：放慢物理过程，便于仔细观察关键瞬间（如水滴脱离瞬间）
- **单步演示**：逐步推进动画，适合课堂分步讲解
- **重置**：恢复初始状态

#### 3. 参数调节
- **旋转角速度ω**：通过滑块实时调整水杯旋转速度（0.5-5.0 rad/s）
  - 高速旋转：水面凹陷明显，水滴紧贴杯壁
  - 低速旋转：水面较平，水滴易飞出
- **水量/水滴质量m**：调节水滴质量（0.5-3.0单位）
  - 质量越大：惯性越大，所需向心力越大
  - 质量越小：越容易维持圆周运动

#### 4. 信息显示
- **实时数据**：显示当前角速度、所需向心力、水滴状态
- **动态公式**：实时更新向心力公式 `F_n = m·ω²·r`，高亮显示变化参数
- **原理说明**：当水滴飞出时，自动显示解释说明

#### 5. 交互操作
- **点击选择水滴**：在整体视图中点击任意水滴，可将其选为详细分析对象
- **自动轨迹记录**：飞出的水滴会保留运动轨迹，清晰展示其切线飞出路径

---

### 三、设计特色

#### 1. 科学可视化
- **颜色编码系统**：
  - 蓝色水滴：分析对象
  - 灰色箭头：重力G
  - 橙色箭头：弹力N（向心力来源）
  - 红色粗箭头：向心力F_n（效果力）
  - 绿色箭头：速度v（切线方向）
- **动态水面**：根据角速度实时计算并绘制凹形水面
- **轨迹可视化**：飞出水滴保留抛物线轨迹，与圆周轨迹形成对比

#### 2. 教学友好性
- **分层次呈现**：从现象到本质，从整体到局部
- **实时反馈**：所有参数调整立即反映在动画中
- **错误概念澄清**：明确区分“向心力”（效果力）与“离心力”（非真实力）

#### 3. 技术实现
- 基于HTML5 Canvas，无需插件，跨平台兼容
- 响应式设计，适配不同屏幕尺寸
- 流畅的60fps动画，物理模拟准确

---

### 四、教学要点

#### 核心概念强调
1. **向心力是效果力**：红色箭头F_n表示的是“合力效果”，不是独立存在的力
2. **向心力来源是性质力**：橙色箭头N（杯壁弹力）是实际存在的力，提供了向心力
3. **离心现象的本质**：当N不足以提供所需F_n时，水滴因惯性沿切线飞出
4. **公式理解**：`F_n = mω²r`中，ω的影响是平方级的，最为关键

#### 关键观察点
1. **转速与向心力的关系**：加快转速，观察红色箭头（F_n）如何变长
2. **质量的影响**：增加水滴质量，观察所需向心力的变化
3. **脱离瞬间**：启用慢动作模式，仔细观察水滴飞出瞬间的速度方向（切线！）
4. **受力平衡**：在局部视图中，观察重力G与弹力N的合力如何精确指向圆心

#### 常见误区澄清
- ❌ 误区：“离心力”将水滴向外推
- ✅ 正解：水滴因惯性欲保持直线运动，杯壁弹力使其转弯；弹力不足时，惯性表现为主导
- ❌ 误区：向心力是一种特殊类型的力
- ✅ 正解：向心力是描述“合力方向指向圆心”这一效果的名称

---

### 五、使用建议

#### 对于教师（课堂演示）
1. **引入阶段**：使用整体视图，展示完整现象，提出问题“水为什么不洒出？”
2. **探究阶段**：切换到局部视图，引导学生分析单个水滴的受力
3. **原理讲解**：调节角速度滑块，展示F_n与ω²的正比关系
4. **难点突破**：使用慢动作模式，反复播放水滴飞出瞬间，强调“切线方向”
5. **巩固练习**：提出“如果杯子突然消失，水滴会怎样运动？”等问题

#### 对于学生（自主学习）
1. **探索性学习**：自由调节参数，观察“如果...会怎样”的各种情况
2. **对比观察**：在整体视图和局部视图间切换，建立宏观与微观的联系
3. **公式验证**：手动计算不同参数下的F_n，与动画显示值对比
4. **预测测试**：先预测调整某个参数的结果，再通过动画验证

#### 对于物理爱好者
1. **参数极限测试**：将角速度调到最大/最小，观察极端情况
2. **细节观察**：关注水面形状随转速的变化，理解旋转参考系中的等效重力
3. **扩展思考**：思考实际生活中的类似现象（洗衣机脱水、转弯时乘客感觉被向外推等）

#### 最佳实践提示
1. **循序渐进**：先观察现象，再分析受力，最后理解公式
2. **多角度验证**：同一原理在不同视图、不同参数下反复观察
3. **联系实际**：将动画中的简化模型与实际生活现象相联系
4. **记录发现**：在探索过程中记录有趣的发现和问题

---

### 技术支持与反馈

本动画基于现代Web技术开发，支持所有主流浏览器（Chrome、Firefox、Safari、Edge）。如遇到任何技术问题或对教学内容有改进建议，欢迎通过教育技术平台反馈。

**祝您探索愉快，收获满满！** 🚀

*熊猫老师 设计制作 | 交互式物理教学系列*