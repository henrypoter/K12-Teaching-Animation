# 需求：水在通电时分解成氢气和氧气（电解水微观动画，体积比2:1清晰可见）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中或高中化学初学者，他们需要直观理解电解水这一抽象的电化学过程。
2.  **核心需求**：用户需要清晰地看到：
    *   **宏观现象**：水通电后，两个电极上产生气泡。
    *   **微观本质**：水分子（H₂O）在电流作用下分解为氢原子和氧原子，并重新组合成氢气（H₂）和氧气（O₂）分子。
    *   **定量关系**：最直观地理解并记住“生成的氢气与氧气的体积比为2:1”这一关键结论。
3.  **潜在难点**：微观过程不可见，学生容易混淆哪个电极产生哪种气体，以及体积比与分子构成的关系。

#### 教学设计思路
1.  **核心概念**：
    *   电解水是化学变化，水分子被破坏，生成了新的氢分子和氧分子。
    *   化学反应方程式：2H₂O → 通电 → 2H₂↑ + O₂↑。
    *   体积比2:1的直接微观解释：每分解2个水分子，生成2个氢分子和1个氧分子。
2.  **认知规律（动画流程设计）**：
    *   **从静到动，从宏观到微观**：先展示完整的实验装置静态图，点击“通电”后，宏观上开始产生气泡。随后通过“放大镜”或“视角切换”功能，将焦点引导至微观层面的分子变化。
    *   **分解与组合的清晰呈现**：
        *   水分子（H₂O）移动到电极（阴极/阳极）附近。
        *   在阴极（接电源负极），水分子中的氢原子（H）获得电子，两个H结合成一个H₂分子（气泡）。
        *   在阳极（接电源正极），水分子中的氧原子（O）失去电子，两个O结合成一个O₂分子（气泡）。
    *   **突出体积比**：在宏观视图中，用两个不同粗细的连通试管收集气体，并通过动画高亮和数字标签（如“体积：2份”和“体积：1份”）强化2:1的比例。在微观层面，通过计数“每生成1个O₂气泡的同时，在另一侧生成2个H₂气泡”来建立关联。
3.  **交互设计**：
    *   **控制面板**：提供明确的“开始/暂停/重置”按钮，允许用户控制动画节奏。
    *   **视角切换**：提供“宏观视图”和“微观视图”的切换按钮，或通过点击装置特定部分（如电极）进行缩放，帮助用户在宏观现象和微观解释之间建立联系。
    *   **提示与标签**：鼠标悬停在分子、电极、气泡上时，显示其名称（如“水分子 H₂O”、“阴极”、“氢气气泡”）。关键步骤配有简短的文字说明。
    *   **步骤引导**：可设计一个“分步演示”模式，将整个过程分解为几个关键步骤，由用户点击逐步推进，适合教师讲解。
4.  **视觉呈现**：
    *   **分子模型**：采用球棍模型。氢原子（H）用较小的浅灰色或白色小球表示，氧原子（O）用较大的红色小球表示。化学键用短棍连接。
    *   **电极与电路**：阴极和阳极用明显的颜色区分（如阴极蓝色，阳极红色），并连接至清晰的电池（+，- 极标识）和导线。
    *   **气泡与收集**：气泡从电极表面产生、上浮。用两个并排的刻度试管收集气体，氢气侧的液面下降速度明显是氧气侧的两倍，视觉对比强烈。
    *   **动画重点**：分子拆解、原子移动、新分子组合的动画需要平滑、清晰，速度适中。可以使用高亮、发光效果来强调正在发生反应的分子和原子。

#### 配色方案选择
*   **主色调**：采用清爽、科学的蓝色调，背景使用浅蓝灰或白色，营造干净、专注的实验环境。
*   **关键元素配色**：
    *   **水（H₂O）**：透明浅蓝色背景（表示水溶液），水分子中的**氧原子（O）用红色**（标准化学配色），**氢原子（H）用浅灰色或白色**。
    *   **电极**：**阴极（负极）用蓝色**，**阳极（正极）用红色**，与电源符号颜色一致，便于记忆。
    *   **气体**：**氢气（H₂）气泡用浅黄色或淡金色**上浮，**氧气（O₂）气泡用浅蓝色**上浮，与分子颜色有一定关联但区分明显。
    *   **收集试管**：透明玻璃材质，背景有刻度。氢气试管上方可标“H₂”，氧气试管标“O₂”。
    *   **电路与电池**：导线为深灰色，电池正极为红色，负极为蓝色。
*   **交互与高亮色**：使用**亮黄色或绿色**的光圈、箭头来高亮当前正在讲解或反应的部分。

#### 交互功能列表
1.  **主控按钮**：开始 / 暂停 / 重置（回到初始状态）。
2.  **视图切换按钮**：宏观实验视图 / 微观分子视图。
3.  **信息提示**：鼠标悬停在任何主要元素（分子、原子、电极、气泡、试管）上时，显示其名称和简要信息。
4.  **分步演示模式**（可选）：将动画分解为4-5步（如：1. 装置介绍 2. 通电 3. 观察气泡 4. 微观分解 5. 体积比较），用户点击“下一步”逐步学习。
5.  **比例强调开关**：一个“显示/隐藏体积比”的按钮，点击后会在两个收集试管上动态显示“2V”和“1V”的标签，并可能用动画柱状图对比。
6.  **速度调节滑块**：允许用户调整分子运动和气泡产生的速度。
7.  **化学方程式显示**：在画面一角动态高亮显示反应方程式，与动画步骤同步。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>电解水微观动画 - 氢气与氧气体积比2:1</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
            color: #333;
        }
        
        .header {
            text-align: center;
            margin-bottom: 20px;
            width: 100%;
            max-width: 1000px;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }
        
        .subtitle {
            color: #3498db;
            font-size: 1.2rem;
            margin-bottom: 15px;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            max-width: 1000px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            padding: 20px;
        }
        
        .animation-area {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #f0f8ff;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 20px;
            border: 2px solid #d1e3f0;
        }
        
        #animationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-bottom: 20px;
            width: 100%;
        }
        
        .btn {
            padding: 12px 24px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(50, 150, 250, 0.2);
        }
        
        .btn:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
            box-shadow: 0 6px 8px rgba(50, 150, 250, 0.3);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        .btn.active {
            background-color: #2ecc71;
            box-shadow: 0 4px 6px rgba(46, 204, 113, 0.3);
        }
        
        .btn.active:hover {
            background-color: #27ae60;
        }
        
        .btn.reset {
            background-color: #e74c3c;
            box-shadow: 0 4px 6px rgba(231, 76, 60, 0.2);
        }
        
        .btn.reset:hover {
            background-color: #c0392b;
        }
        
        .view-toggle {
            display: flex;
            background-color: #ecf0f1;
            border-radius: 8px;
            overflow: hidden;
            margin: 0 10px;
        }
        
        .view-btn {
            padding: 12px 20px;
            background-color: transparent;
            color: #7f8c8d;
            border: none;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .view-btn.active {
            background-color: #3498db;
            color: white;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            background-color: #ecf0f1;
            padding: 0 15px;
            border-radius: 8px;
            margin: 0 10px;
        }
        
        .slider-container label {
            margin-right: 10px;
            font-weight: 600;
            color: #2c3e50;
            white-space: nowrap;
        }
        
        .speed-slider {
            width: 150px;
        }
        
        .info-panel {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            width: 100%;
            background-color: #f8fafc;
            border-radius: 10px;
            padding: 20px;
            margin-top: 10px;
            border: 1px solid #e1e8ed;
        }
        
        .info-box {
            flex: 1;
            min-width: 200px;
            margin: 10px;
            padding: 15px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.05);
        }
        
        .info-title {
            color: #3498db;
            font-weight: 700;
            margin-bottom: 10px;
            font-size: 1.1rem;
            border-bottom: 2px solid #3498db;
            padding-bottom: 5px;
        }
        
        .equation {
            font-size: 1.4rem;
            text-align: center;
            color: #2c3e50;
            font-weight: 700;
            margin: 10px 0;
            padding: 10px;
            background-color: #f1f8ff;
            border-radius: 8px;
        }
        
        .highlight {
            color: #e74c3c;
            font-weight: 800;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 15px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            margin-right: 15px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            margin-right: 8px;
        }
        
        .tooltip {
            position: absolute;
            background-color: rgba(44, 62, 80, 0.9);
            color: white;
            padding: 8px 12px;
            border-radius: 6px;
            font-size: 0.9rem;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 100;
            max-width: 200px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        @media (max-width: 768px) {
            .controls {
                flex-direction: column;
                align-items: center;
            }
            
            .btn, .view-toggle, .slider-container {
                width: 100%;
                max-width: 300px;
                margin: 5px 0;
            }
            
            .animation-area {
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>电解水微观过程动画</h1>
        <div class="subtitle">直观展示水分子分解为氢气和氧气，体积比2:1</div>
    </div>
    
    <div class="container">
        <div class="animation-area">
            <canvas id="animationCanvas" width="960" height="500"></canvas>
            <div class="tooltip" id="tooltip"></div>
        </div>
        
        <div class="controls">
            <button class="btn" id="startBtn">开始电解</button>
            <button class="btn" id="pauseBtn">暂停</button>
            <button class="btn reset" id="resetBtn">重置</button>
            
            <div class="view-toggle">
                <button class="view-btn active" id="macroBtn">宏观视图</button>
                <button class="view-btn" id="microBtn">微观视图</button>
            </div>
            
            <div class="slider-container">
                <label for="speedSlider">动画速度:</label>
                <input type="range" min="1" max="10" value="5" class="speed-slider" id="speedSlider">
            </div>
            
            <button class="btn" id="ratioBtn">显示体积比</button>
        </div>
        
        <div class="equation">
            2H<sub>2</sub>O <span style="color:#7f8c8d">→ 通电 →</span> 2H<sub>2</sub>↑ + O<sub>2</sub>↑
        </div>
        
        <div class="info-panel">
            <div class="info-box">
                <div class="info-title">实验原理</div>
                <p>水在直流电作用下分解为氢气和氧气。</p>
                <p>阴极（负极）：产生<strong>氢气</strong>，体积较大</p>
                <p>阳极（正极）：产生<strong>氧气</strong>，体积较小</p>
                <p>氢气与氧气的<strong class="highlight">体积比为2:1</strong></p>
            </div>
            
            <div class="info-box">
                <div class="info-title">微观解释</div>
                <p>1. 水分子(H₂O)在电流作用下分解</p>
                <p>2. 氢原子在阴极结合成氢分子(H₂)</p>
                <p>3. 氧原子在阳极结合成氧分子(O₂)</p>
                <p>4. 每生成1个O₂分子，同时生成2个H₂分子</p>
            </div>
            
            <div class="info-box">
                <div class="info-title">图例说明</div>
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff6b6b;"></div>
                        <span>氧原子 (O)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #d1d1d1;"></div>
                        <span>氢原子 (H)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #3498db;"></div>
                        <span>阴极 (-)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span>阳极 (+)</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        const tooltip = document.getElementById('tooltip');
        
        // 动画状态
        let animationId = null;
        let isAnimating = false;
        let isMacroView = true;
        let showVolumeRatio = false;
        let animationSpeed = 5;
        
        // 实验装置参数
        const waterLevel = 350;
        const cathodeX = 300;
        const anodeX = 660;
        const electrodeWidth = 10;
        const electrodeHeight = 120;
        
        // 气体收集管参数
        const leftTubeX = 150;
        const rightTubeX = 810;
        const tubeWidth = 60;
        const tubeHeight = 180;
        const tubeY = 100;
        
        // 气体体积
        let hydrogenVolume = 0;
        let oxygenVolume = 0;
        const maxVolume = 120;
        
        // 分子参数
        const molecules = [];
        const bubbles = [];
        
        // 初始化水分子
        function initMolecules() {
            molecules.length = 0;
            
            // 创建水分子
            for (let i = 0; i < 40; i++) {
                const x = Math.random() * (canvas.width - 200) + 100;
                const y = Math.random() * (waterLevel - 100) + 100;
                
                molecules.push({
                    x: x,
                    y: y,
                    vx: (Math.random() - 0.5) * 0.5,
                    vy: (Math.random() - 0.5) * 0.5,
                    type: 'h2o',
                    atoms: [
                        {type: 'o', x: 0, y: 0, angle: 0},
                        {type: 'h', x: -15, y: 10, angle: 0},
                        {type: 'h', x: 15, y: 10, angle: 0}
                    ],
                    radius: 20,
                    color: '#3498db',
                    opacity: 0.7,
                    state: 'free', // free, movingToCathode, movingToAnode, decomposing
                    targetX: 0,
                    targetY: 0,
                    progress: 0
                });
            }
        }
        
        // 绘制实验装置
        function drawApparatus() {
            // 绘制水槽
            ctx.fillStyle = 'rgba(173, 216, 230, 0.3)';
            ctx.fillRect(100, waterLevel, canvas.width - 200, canvas.height - waterLevel);
            ctx.strokeStyle = '#5dade2';
            ctx.lineWidth = 2;
            ctx.strokeRect(100, waterLevel, canvas.width - 200, canvas.height - waterLevel);
            
            // 绘制水位线
            ctx.strokeStyle = '#3498db';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            ctx.moveTo(100, waterLevel);
            ctx.lineTo(canvas.width - 100, waterLevel);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制阴极（蓝色）
            ctx.fillStyle = '#3498db';
            ctx.fillRect(cathodeX - electrodeWidth/2, waterLevel - electrodeHeight, electrodeWidth, electrodeHeight);
            
            // 绘制阳极（红色）
            ctx.fillStyle = '#e74c3c';
            ctx.fillRect(anodeX - electrodeWidth/2, waterLevel - electrodeHeight, electrodeWidth, electrodeHeight);
            
            // 绘制电极标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('阴极 (-)', cathodeX, waterLevel - electrodeHeight - 20);
            ctx.fillText('阳极 (+)', anodeX, waterLevel - electrodeHeight - 20);
            
            // 绘制电源
            ctx.fillStyle = '#2c3e50';
            ctx.fillRect(canvas.width/2 - 40, 50, 80, 40);
            ctx.fillStyle = '#e74c3c';
            ctx.font = 'bold 20px Arial';
            ctx.fillText('+', canvas.width/2 - 20, 78);
            ctx.fillStyle = '#3498db';
            ctx.fillText('-', canvas.width/2 + 15, 78);
            
            // 绘制导线
            ctx.strokeStyle = '#7f8c8d';
            ctx.lineWidth = 3;
            ctx.beginPath();
            // 正极导线到阳极
            ctx.moveTo(canvas.width/2 - 20, 90);
            ctx.lineTo(anodeX, 90);
            ctx.lineTo(anodeX, waterLevel - electrodeHeight);
            // 负极导线到阴极
            ctx.moveTo(canvas.width/2 + 20, 90);
            ctx.lineTo(cathodeX, 90);
            ctx.lineTo(cathodeX, waterLevel - electrodeHeight);
            ctx.stroke();
            
            // 绘制气体收集管
            drawGasTubes();
        }
        
        // 绘制气体收集管
        function drawGasTubes() {
            // 左侧收集管（氢气）
            ctx.strokeStyle = '#95a5a6';
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.rect(leftTubeX, tubeY, tubeWidth, tubeHeight);
            ctx.stroke();
            
            // 右侧收集管（氧气）
            ctx.beginPath();
            ctx.rect(rightTubeX, tubeY, tubeWidth, tubeHeight);
            ctx.stroke();
            
            // 绘制收集管中的水
            ctx.fillStyle = 'rgba(173, 216, 230, 0.5)';
            const hydrogenWaterLevel = tubeY + tubeHeight - (hydrogenVolume / maxVolume) * tubeHeight;
            const oxygenWaterLevel = tubeY + tubeHeight - (oxygenVolume / maxVolume) * tubeHeight;
            
            ctx.fillRect(leftTubeX, hydrogenWaterLevel, tubeWidth, tubeHeight - hydrogenWaterLevel + tubeY);
            ctx.fillRect(rightTubeX, oxygenWaterLevel, tubeWidth, tubeHeight - oxygenWaterLevel + tubeY);
            
            // 绘制气体
            ctx.fillStyle = 'rgba(255, 235, 59, 0.7)'; // 氢气颜色
            ctx.fillRect(leftTubeX, tubeY, tubeWidth, hydrogenWaterLevel - tubeY);
            
            ctx.fillStyle = 'rgba(100, 181, 246, 0.7)'; // 氧气颜色
            ctx.fillRect(rightTubeX, tubeY, tubeWidth, oxygenWaterLevel - tubeY);
            
            // 绘制标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('H₂', leftTubeX + tubeWidth/2, tubeY - 10);
            ctx.fillText('O₂', rightTubeX + tubeWidth/2, tubeY - 10);
            
            // 显示体积比
            if (showVolumeRatio) {
                ctx.fillStyle = '#e74c3c';
                ctx.font = 'bold 18px Arial';
                ctx.fillText(`体积: ${(hydrogenVolume/20).toFixed(1)}`, leftTubeX + tubeWidth/2, tubeY + tubeHeight + 25);
                ctx.fillText(`体积: ${(oxygenVolume/20).toFixed(1)}`, rightTubeX + tubeWidth/2, tubeY + tubeHeight + 25);
                
                // 绘制比例箭头
                ctx.strokeStyle = '#e74c3c';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(leftTubeX + tubeWidth/2, tubeY + tubeHeight + 15);
                ctx.lineTo(rightTubeX + tubeWidth/2, tubeY + tubeHeight + 15);
                ctx.stroke();
                
                // 绘制比例标签
                ctx.fillStyle = '#e74c3c';
                ctx.font = 'bold 20px Arial';
                ctx.fillText('2 : 1', canvas.width/2, tubeY + tubeHeight + 25);
            }
        }
        
        // 绘制分子
        function drawMolecules() {
            molecules.forEach(molecule => {
                // 计算分子位置
                const centerX = molecule.x;
                const centerY = molecule.y;
                
                // 绘制分子
                ctx.save();
                ctx.translate(centerX, centerY);
                
                // 绘制化学键
                ctx.strokeStyle = molecule.type === 'h2o' ? '#3498db' : 
                                 molecule.type === 'h2' ? '#ffeb3b' : '#64b5f6';
                ctx.lineWidth = 2;
                
                if (molecule.type === 'h2o') {
                    // H-O键
                    ctx.beginPath();
                    ctx.moveTo(0, 0);
                    ctx.lineTo(-15, 10);
                    ctx.stroke();
                    
                    ctx.beginPath();
                    ctx.moveTo(0, 0);
                    ctx.lineTo(15, 10);
                    ctx.stroke();
                    
                    // 绘制原子
                    // 氧原子
                    ctx.fillStyle = '#ff6b6b';
                    ctx.beginPath();
                    ctx.arc(0, 0, 8, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 氢原子
                    ctx.fillStyle = '#d1d1d1';
                    ctx.beginPath();
                    ctx.arc(-15, 10, 5, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.beginPath();
                    ctx.arc(15, 10, 5, 0, Math.PI * 2);
                    ctx.fill();
                    
                } else if (molecule.type === 'h2') {
                    // H-H键
                    ctx.beginPath();
                    ctx.moveTo(-8, 0);
                    ctx.lineTo(8, 0);
                    ctx.stroke();
                    
                    // 氢原子
                    ctx.fillStyle = '#d1d1d1';
                    ctx.beginPath();
                    ctx.arc(-8, 0, 5, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.beginPath();
                    ctx.arc(8, 0, 5, 0, Math.PI * 2);
                    ctx.fill();
                    
                } else if (molecule.type === 'o2') {
                    // O=O双键
                    ctx.beginPath();
                    ctx.moveTo(-10, -3);
                    ctx.lineTo(10, -3);
                    ctx.stroke();
                    
                    ctx.beginPath();
                    ctx.moveTo(-10, 3);
                    ctx.lineTo(10, 3);
                    ctx.stroke();
                    
                    // 氧原子
                    ctx.fillStyle = '#ff6b6b';
                    ctx.beginPath();
                    ctx.arc(-10, 0, 8, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.beginPath();
                    ctx.arc(10, 0, 8, 0, Math.PI * 2);
                    ctx.fill();
                }
                
                ctx.restore();
                
                // 绘制分子运动轨迹（仅微观视图）
                if (!isMacroView && molecule.state === 'movingToCathode') {
                    ctx.strokeStyle = 'rgba(52, 152, 219, 0.3)';
                    ctx.lineWidth = 1;
                    ctx.setLineDash([5, 5]);
                    ctx.beginPath();
                    ctx.moveTo(molecule.x, molecule.y);
                    ctx.lineTo(cathodeX, waterLevel - electrodeHeight/2);
                    ctx.stroke();
                    ctx.setLineDash([]);
                }
                
                if (!isMacroView && molecule.state === 'movingToAnode') {
                    ctx.strokeStyle = 'rgba(231, 76, 60, 0.3)';
                    ctx.lineWidth = 1;
                    ctx.setLineDash([5, 5]);
                    ctx.beginPath();
                    ctx.moveTo(molecule.x, molecule.y);
                    ctx.lineTo(anodeX, waterLevel - electrodeHeight/2);
                    ctx.stroke();
                    ctx.setLineDash([]);
                }
            });
        }
        
        // 绘制气泡
        function drawBubbles() {
            bubbles.forEach(bubble => {
                // 气泡颜色
                ctx.fillStyle = bubble.type === 'h2' ? 
                    'rgba(255, 235, 59, 0.8)' : 'rgba(100, 181, 246, 0.8)';
                
                // 绘制气泡
                ctx.beginPath();
                ctx.arc(bubble.x, bubble.y, bubble.radius, 0, Math.PI * 2);
                ctx.fill();
                
                // 气泡高光
                ctx.fillStyle = 'rgba(255, 255, 255, 0.6)';
                ctx.beginPath();
                ctx.arc(bubble.x - bubble.radius/3, bubble.y - bubble.radius/3, bubble.radius/3, 0, Math.PI * 2);
                ctx.fill();
            });
        }
        
        // 更新分子状态
        function updateMolecules() {
            if (!isAnimating) return;
            
            // 随机选择水分子移动到电极
            if (Math.random() < 0.02 * (animationSpeed/5)) {
                const freeMolecules = molecules.filter(m => m.type === 'h2o' && m.state === 'free');
                if (freeMolecules.length > 0) {
                    const molecule = freeMolecules[Math.floor(Math.random() * freeMolecules.length)];
                    
                    // 随机选择阴极或阳极
                    if (Math.random() < 0.67) { // 2/3的概率去阴极（因为需要2个H₂O产生2个H₂）
                        molecule.state = 'movingToCathode';
                        molecule.targetX = cathodeX;
                        molecule.targetY = waterLevel - electrodeHeight/2;
                    } else {
                        molecule.state = 'movingToAnode';
                        molecule.targetX = anodeX;
                        molecule.targetY = waterLevel - electrodeHeight/2;
                    }
                }
            }
            
            // 更新分子位置和状态
            molecules.forEach(molecule => {
                // 自由运动的分子
                if (molecule.state === 'free') {
                    molecule.x += molecule.vx;
                    molecule.y += molecule.vy;
                    
                    // 边界反弹
                    if (molecule.x < 120 || molecule.x > canvas.width - 120) {
                        molecule.vx *= -1;
                    }
                    if (molecule.y < 120 || molecule.y > waterLevel - 20) {
                        molecule.vy *= -1;
                    }
                }
                // 向电极移动的分子
                else if (molecule.state === 'movingToCathode' || molecule.state === 'movingToAnode') {
                    const dx = molecule.targetX - molecule.x;
                    const dy = molecule.targetY - molecule.y;
                    const distance = Math.sqrt(dx*dx + dy*dy);
                    
                    if (distance < 5) {
                        // 到达电极，开始分解
                        molecule.state = 'decomposing';
                        molecule.progress = 0;
                    } else {
                        // 向电极移动
                        const speed = 2 * (animationSpeed/5);
                        molecule.x += (dx / distance) * speed;
                        molecule.y += (dy / distance) * speed;
                    }
                }
                // 分解中的分子
                else if (molecule.state === 'decomposing') {
                    molecule.progress += 0.02 * (animationSpeed/5);
                    
                    if (molecule.progress >= 1) {
                        // 分解完成
                        if (molecule.targetX === cathodeX) {
                            // 在阴极分解为氢气
                            molecule.type = 'h2';
                            molecule.state = 'bubble';
                            molecule.progress = 0;
                            
                            // 创建气泡
                            bubbles.push({
                                x: cathodeX,
                                y: waterLevel - electrodeHeight/2,
                                vx: (Math.random() - 0.5) * 0.5,
                                vy: -2 - Math.random(),
                                radius: 8,
                                type: 'h2',
                                life: 1
                            });
                            
                            // 增加氢气体积
                            hydrogenVolume = Math.min(maxVolume, hydrogenVolume + 2);
                            
                        } else {
                            // 在阳极分解为氧气
                            molecule.type = 'o2';
                            molecule.state = 'bubble';
                            molecule.progress = 0;
                            
                            // 创建气泡
                            bubbles.push({
                                x: anodeX,
                                y: waterLevel - electrodeHeight/2,
                                vx: (Math.random() - 0.5) * 0.5,
                                vy: -2 - Math.random(),
                                radius: 10,
                                type: 'o2',
                                life: 1
                            });
                            
                            // 增加氧气体积
                            oxygenVolume = Math.min(maxVolume, oxygenVolume + 1);
                        }
                    }
                }
                // 气泡状态的分子
                else if (molecule.state === 'bubble') {
                    molecule.progress += 0.01 * (animationSpeed/5);
                    molecule.y -= 2 * (animationSpeed/5);
                    
                    if (molecule.progress >= 1) {
                        // 气泡到达水面，重新变为水分子
                        molecule.type = 'h2o';
                        molecule.state = 'free';
                        molecule.x = Math.random() * (canvas.width - 200) + 100;
                        molecule.y = Math.random() * (waterLevel - 100) + 100;
                        molecule.progress = 0;
                    }
                }
            });
        }
        
        // 更新气泡
        function updateBubbles() {
            for (let i = bubbles.length - 1; i >= 0; i--) {
                const bubble = bubbles[i];
                
                bubble.y += bubble.vy;
                bubble.x += bubble.vx;
                bubble.life -= 0.01;
                
                // 气泡到达水面
                if (bubble.y < 50 || bubble.life <= 0) {
                    bubbles.splice(i, 1);
                }
            }
        }
        
        // 绘制微观视图
        function drawMicroView() {
            // 绘制放大区域
            ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
            ctx.fillRect(50, 50, canvas.width - 100, canvas.height - 100);
            ctx.strokeStyle = '#3498db';
            ctx.lineWidth = 3;
            ctx.strokeRect(50, 50, canvas.width - 100, canvas.height - 100);
            
            // 绘制标题
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('微观视图 - 水分子分解过程', canvas.width/2, 30);
            
            // 绘制电极区域
            ctx.fillStyle = '#3498db';
            ctx.fillRect(200, 150, 80, 200);
            ctx.fillStyle = '#e74c3c';
            ctx.fillRect(canvas.width - 280, 150, 80, 200);
            
            // 电极标签
            ctx.fillStyle = 'white';
            ctx.font = 'bold 16px Arial';
            ctx.fillText('阴极', 240, 140);
            ctx.fillText('阳极', canvas.width - 240, 140);
            
            // 绘制分子
            drawMolecules();
            
            // 绘制说明文本
            ctx.fillStyle = '#2c3e50';
            ctx.font = '16px Arial';
            ctx.textAlign = 'left';
            ctx.fillText('• 水分子(H₂O)在电极附近分解', 100, 400);
            ctx.fillText('• 氢原子在阴极结合成H₂分子', 100, 430);
            ctx.fillText('• 氧原子在阳极结合成O₂分子', 100, 460);
            ctx.fillText(`• 已分解: ${Math.floor(hydrogenVolume/2)}个H₂O分子`, canvas.width - 300, 400);
            
            // 绘制反应方程式
            ctx.fillStyle = '#e74c3c';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('2H₂O → 2H₂ + O₂', canvas.width/2, 450);
        }
        
        // 绘制宏观视图
        function drawMacroView() {
            // 绘制实验装置
            drawApparatus();
            
            // 绘制分子（半透明）
            if (isAnimating) {
                ctx.globalAlpha = 0.3;
                drawMolecules();
                ctx.globalAlpha = 1.0;
            }
            
            // 绘制气泡
            drawBubbles();
            
            // 绘制标题
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('宏观视图 - 电解水实验', canvas.width/2, 30);
            
            // 绘制状态指示
            ctx.fillStyle = isAnimating ? '#2ecc71' : '#e74c3c';
            ctx.font = 'bold 16px Arial';
            ctx.fillText(isAnimating ? '电解进行中...' : '已停止', canvas.width/2, 60);
        }
        
        // 主绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            ctx.fillStyle = '#f0f8ff';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 根据视图模式绘制
            if (isMacroView) {
                drawMacroView();
            } else {
                drawMicroView();
            }
            
            // 更新状态
            updateMolecules();
            updateBubbles();
            
            // 继续动画循环
            animationId = requestAnimationFrame(draw);
        }
        
        // 鼠标移动事件处理
        canvas.addEventListener('mousemove', (e) => {
            const rect = canvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            let tooltipText = '';
            
            // 检查鼠标是否在元素上
            if (isMacroView) {
                // 检查阴极
                if (x > cathodeX - 20 && x < cathodeX + 20 && 
                    y > waterLevel - electrodeHeight && y < waterLevel) {
                    tooltipText = '阴极（负极）：产生氢气';
                }
                // 检查阳极
                else if (x > anodeX - 20 && x < anodeX + 20 && 
                         y > waterLevel - electrodeHeight && y < waterLevel) {
                    tooltipText = '阳极（正极）：产生氧气';
                }
                // 检查氢气收集管
                else if (x > leftTubeX && x < leftTubeX + tubeWidth && 
                         y > tubeY && y < tubeY + tubeHeight) {
                    tooltipText = `氢气收集管：体积 ${(hydrogenVolume/20).toFixed(1)}`;
                }
                // 检查氧气收集管
                else if (x > rightTubeX && x < rightTubeX + tubeWidth && 
                         y > tubeY && y < tubeY + tubeHeight) {
                    tooltipText = `氧气收集管：体积 ${(oxygenVolume/20).toFixed(1)}`;
                }
                // 检查气泡
                else {
                    for (const bubble of bubbles) {
                        const dx = x - bubble.x;
                        const dy = y - bubble.y;
                        const distance = Math.sqrt(dx*dx + dy*dy);
                        
                        if (distance < bubble.radius) {
                            tooltipText = bubble.type === 'h2' ? '氢气气泡 (H₂)' : '氧气气泡 (O₂)';
                            break;
                        }
                    }
                }
            } else {
                // 微观视图中的提示
                for (const molecule of molecules) {
                    const dx = x - molecule.x;
                    const dy = y - molecule.y;
                    const distance = Math.sqrt(dx*dx + dy*dy);
                    
                    if (distance < molecule.radius) {
                        if (molecule.type === 'h2o') {
                            tooltipText = '水分子 (H₂O)';
                        } else if (molecule.type === 'h2') {
                            tooltipText = '氢分子 (H₂)';
                        } else if (molecule.type === 'o2') {
                            tooltipText = '氧分子 (O₂)';
                        }
                        break;
                    }
                }
            }
            
            // 显示或隐藏工具提示
            if (tooltipText) {
                tooltip.textContent = tooltipText;
                tooltip.style.left = (e.clientX + 10) + 'px';
                tooltip.style.top = (e.clientY + 10) + 'px';
                tooltip.style.opacity = '1';
            } else {
                tooltip.style.opacity = '0';
            }
        });
        
        // 初始化
<!--检测到代码截断，自动续写中...-->
// 初始化
        initMolecules();
        
        // 按钮事件监听
        document.getElementById('startBtn').addEventListener('click', () => {
            if (!isAnimating) {
                isAnimating = true;
                document.getElementById('startBtn').classList.add('active');
                document.getElementById('pauseBtn').classList.remove('active');
            }
        });
        
        document.getElementById('pauseBtn').addEventListener('click', () => {
            isAnimating = false;
            document.getElementById('startBtn').classList.remove('active');
            document.getElementById('pauseBtn').classList.add('active');
        });
        
        document.getElementById('resetBtn').addEventListener('click', () => {
            isAnimating = false;
            hydrogenVolume = 0;
            oxygenVolume = 0;
            bubbles.length = 0;
            initMolecules();
            document.getElementById('startBtn').classList.remove('active');
            document.getElementById('pauseBtn').classList.remove('active');
        });
        
        document.getElementById('macroBtn').addEventListener('click', () => {
            isMacroView = true;
            document.getElementById('macroBtn').classList.add('active');
            document.getElementById('microBtn').classList.remove('active');
        });
        
        document.getElementById('microBtn').addEventListener('click', () => {
            isMacroView = false;
            document.getElementById('macroBtn').classList.remove('active');
            document.getElementById('microBtn').classList.add('active');
        });
        
        document.getElementById('ratioBtn').addEventListener('click', () => {
            showVolumeRatio = !showVolumeRatio;
            document.getElementById('ratioBtn').classList.toggle('active', showVolumeRatio);
            document.getElementById('ratioBtn').textContent = showVolumeRatio ? '隐藏体积比' : '显示体积比';
        });
        
        document.getElementById('speedSlider').addEventListener('input', (e) => {
            animationSpeed = parseInt(e.target.value);
        });
        
        // 开始动画
        draw();
        
        // 添加键盘快捷键
        document.addEventListener('keydown', (e) => {
            switch(e.key) {
                case ' ':
                case 'Spacebar':
                    // 空格键切换开始/暂停
                    e.preventDefault();
                    isAnimating = !isAnimating;
                    document.getElementById('startBtn').classList.toggle('active', isAnimating);
                    document.getElementById('pauseBtn').classList.toggle('active', !isAnimating);
                    break;
                case 'r':
                case 'R':
                    // R键重置
                    e.preventDefault();
                    document.getElementById('resetBtn').click();
                    break;
                case 'm':
                case 'M':
                    // M键切换视图
                    e.preventDefault();
                    document.getElementById(isMacroView ? 'microBtn' : 'macroBtn').click();
                    break;
            }
        });
        
        // 添加触摸设备支持
        let touchStartX = 0;
        let touchStartY = 0;
        
        canvas.addEventListener('touchstart', (e) => {
            e.preventDefault();
            const touch = e.touches[0];
            touchStartX = touch.clientX;
            touchStartY = touch.clientY;
        });
        
        canvas.addEventListener('touchend', (e) => {
            e.preventDefault();
            const touch = e.changedTouches[0];
            const deltaX = touch.clientX - touchStartX;
            const deltaY = touch.clientY - touchStartY;
            
            // 如果滑动距离很小，则视为点击
            if (Math.abs(deltaX) < 10 && Math.abs(deltaY) < 10) {
                // 在触摸位置显示工具提示
                const rect = canvas.getBoundingClientRect();
                const x = touch.clientX - rect.left;
                const y = touch.clientY - rect.top;
                
                let tooltipText = '';
                
                // 检查触摸位置（与鼠标移动事件类似）
                if (isMacroView) {
                    if (x > cathodeX - 20 && x < cathodeX + 20 && 
                        y > waterLevel - electrodeHeight && y < waterLevel) {
                        tooltipText = '阴极（负极）：产生氢气';
                    } else if (x > anodeX - 20 && x < anodeX + 20 && 
                               y > waterLevel - electrodeHeight && y < waterLevel) {
                        tooltipText = '阳极（正极）：产生氧气';
                    }
                }
                
                if (tooltipText) {
                    tooltip.textContent = tooltipText;
                    tooltip.style.left = (touch.clientX + 10) + 'px';
                    tooltip.style.top = (touch.clientY + 10) + 'px';
                    tooltip.style.opacity = '1';
                    
                    // 2秒后隐藏工具提示
                    setTimeout(() => {
                        tooltip.style.opacity = '0';
                    }, 2000);
                }
            }
        });
        
        // 阻止触摸滚动
        canvas.addEventListener('touchmove', (e) => {
            e.preventDefault();
        }, { passive: false });
        
        // 窗口大小调整处理
        window.addEventListener('resize', () => {
            // 获取新的画布尺寸
            const container = document.querySelector('.animation-area');
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            
            // 重新初始化分子位置
            initMolecules();
        });
        
        // 初始调整画布大小
        const container = document.querySelector('.animation-area');
        canvas.width = container.clientWidth;
        canvas.height = container.clientHeight;
        
        // 添加使用说明
        console.log('电解水动画使用说明：');
        console.log('1. 点击"开始电解"按钮开始动画');
        console.log('2. 点击"宏观视图"/"微观视图"切换不同视角');
        console.log('3. 鼠标悬停在元素上查看详细信息');
        console.log('4. 使用滑块调整动画速度');
        console.log('5. 快捷键：空格键(开始/暂停)，R键(重置)，M键(切换视图)');
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

### 功能说明

欢迎使用“电解水微观过程动画”！本交互式教学工具旨在通过直观的视觉呈现和交互体验，帮助您深入理解电解水的化学原理。动画采用HTML5 Canvas技术开发，实现了从宏观实验现象到微观分子变化的完整展示，特别突出了氢气与氧气体积比为2:1这一关键知识点。

### 主要功能

#### 1. 双重视角切换
- **宏观视图**：展示完整的电解水实验装置，包括电极、电源、导线和气体收集管
- **微观视图**：聚焦于分子层面的变化，展示水分子分解为氢原子和氧原子的过程

#### 2. 动画控制
- **开始/暂停**：控制电解过程的进行与停止
- **重置**：恢复实验初始状态
- **速度调节**：通过滑块调整动画速度（1-10档）

#### 3. 交互特性
- **鼠标悬停提示**：悬停在实验装置、分子或气泡上，显示详细信息
- **体积比显示**：一键显示/隐藏氢气与氧气的体积比例（2:1）
- **触摸屏支持**：适配移动设备，支持触摸操作

#### 4. 信息面板
- 实验原理说明
- 微观过程解释
- 化学方程式展示
- 图例说明

### 设计特色

#### 视觉设计
- **科学配色方案**：
  - 氧原子：红色（标准化学配色）
  - 氢原子：浅灰色
  - 阴极：蓝色（对应负极）
  - 阳极：红色（对应正极）
  - 氢气：浅黄色气泡
  - 氧气：浅蓝色气泡

- **清晰的层次结构**：
  - 宏观与微观视图分离
  - 分子模型采用球棍模型
  - 气体收集管直观显示体积变化

#### 教学逻辑
- **从现象到本质**：先展示宏观气泡产生，再揭示微观分子变化
- **定量可视化**：通过气体收集管的液面变化直观展示2:1体积比
- **过程分解**：将电解过程分解为多个可观察的步骤

### 教学要点

#### 核心概念
1. **电解水是化学变化**
   - 水分子（H₂O）被破坏
   - 生成新的氢分子（H₂）和氧分子（O₂）

2. **电极反应**
   - 阴极（负极）：2H₂O + 2e⁻ → H₂↑ + 2OH⁻
   - 阳极（正极）：2H₂O → O₂↑ + 4H⁺ + 4e⁻

3. **体积比关系**
   - 化学方程式：2H₂O → 2H₂↑ + O₂↑
   - 每分解2个水分子，生成2个氢分子和1个氧分子
   - 同温同压下，气体体积比等于分子数比

#### 观察重点
1. **宏观层面**：
   - 两个电极上气泡产生的速率差异
   - 气体收集管中液面下降的速度比
   - 气泡颜色的区别（教学辅助设计）

2. **微观层面**：
   - 水分子向电极移动的轨迹
   - 分子在电极表面的分解过程
   - 原子重新组合为新分子的动画

### 使用建议

#### 课堂教学场景
1. **导入环节**（2-3分钟）
   - 展示宏观视图，提问：“通电后你观察到了什么现象？”
   - 引导学生注意两个电极上气泡产生的差异

2. **探究环节**（5-8分钟）
   - 切换到微观视图，讲解分子分解过程
   - 使用“暂停”功能，分步讲解关键步骤
   - 引导学生发现“每生成1个氧气泡，同时生成2个氢气泡”

3. **总结环节**（3-5分钟）
   - 点击“显示体积比”按钮，强化2:1的概念
   - 回归化学方程式，建立宏观现象与微观本质的联系
   - 使用重置功能，让学生预测并验证现象

#### 自主学习建议
1. **探索式学习**：
   - 先自行操作动画，记录观察结果
   - 尝试解释观察到的现象
   - 使用提示功能验证理解

2. **分层学习路径**：
   - **基础层**：观察宏观现象，记住体积比
   - **提高层**：理解微观过程，掌握电极反应
   - **拓展层**：思考实际应用（如氢能源制备）

#### 技术提示
1. **快捷键**：
   - 空格键：开始/暂停动画
   - R键：重置实验
   - M键：切换宏观/微观视图

2. **设备适配**：
   - 支持电脑、平板和手机访问
   - 触摸屏设备支持点击查看详细信息
   - 建议使用Chrome、Firefox等现代浏览器

3. **性能优化**：
   - 动画速度可调，适应不同硬件性能
   - 复杂场景下可适当降低速度以获得流畅体验

#### 教学延伸
1. **问题引导**：
   - “为什么氢气的体积是氧气的两倍？”
   - “如果改变电压，会有什么影响？”
   - “这个实验在实际生活中有哪些应用？”

2. **实验联系**：
   - 将动画与实际实验视频对比
   - 讨论动画模拟与实际操作的异同
   - 设计验证体积比的实验方案

3. **跨学科连接**：
   - 物理：电流、电压与电解效率
   - 数学：比例关系与气体定律
   - 工程：电解槽设计与优化

---

**温馨提示**：本动画工具旨在辅助理解，建议与实际实验、教材讲解和教师指导相结合使用。动画中的颜色和比例经过教学化处理，以便更清晰地展示科学原理。

祝您教学愉快，探索成功！ 🎓✨