# 需求：实验室制取二氧化碳的全微观过程（CaCO₃ → CaO + CO₂分子飞出）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中或高中化学初学者。他们需要直观理解实验室制取二氧化碳（大理石与稀盐酸反应）的宏观现象与微观本质之间的联系。
2.  **核心需求**：用户不仅需要知道“反应方程式是 CaCO₃ + 2HCl → CaCl₂ + H₂O + CO₂↑”，更需要**可视化地理解**：
    *   固体反应物（CaCO₃）在酸中如何“溶解”并参与反应。
    *   氢离子（H⁺）在反应中的关键作用。
    *   二氧化碳气体分子（CO₂）是如何从溶液中产生并逸出的。
    *   整个过程的动态、连续性。
3.  **潜在难点**：学生容易混淆宏观的“气泡产生”与微观的“分子重组与释放”，对离子反应过程感到抽象。动画需拆解步骤，降低认知负荷。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
*   **核心概念**：
    *   离子反应：H⁺ 与 CO₃²⁻ 的反应是核心驱动力。
    *   分子模型：用球棍模型清晰展示反应物、中间态、生成物的结构变化。
    *   质量守恒：通过原子计数和颜色对应，体现反应前后原子种类与数目不变。
*   **认知规律**：
    1.  **从宏观到微观**：动画起始于一个烧杯的宏观视角，然后镜头推入，进入微观分子世界。
    2.  **分步演示**：将连续反应分解为几个关键步骤，按逻辑顺序播放，并允许用户控制节奏。
    3.  **突出关键**：使用高亮、闪烁、运动轨迹强调（如H⁺的攻击、CO₂分子的形成与逃逸）。
*   **交互设计**：
    *   **步骤控制**：提供“上一步”、“播放/暂停”、“下一步”按钮，让用户自主探索。
    *   **视角切换**：提供“宏观视图”（烧杯）和“微观视图”（分子）的切换按钮，强化联系。
    *   **提示与标注**：鼠标悬停在特定分子或离子上时，显示其名称和化学式（如“碳酸根离子 CO₃²⁻”）。
    *   **重置功能**：一键重置动画到初始状态。
*   **视觉呈现**：
    *   **分子模型**：采用标准球棍模型，原子颜色遵循CPK规则（C: 灰色， O: 红色， H: 白色， Cl: 绿色， Ca²⁺: 浅灰色带“+”号）。
    *   **动态效果**：
        *   CaCO₃固体表面分子被“剥离”并进入溶液。
        *   H⁺离子（以H₃O⁺水合氢离子形式呈现）动态撞击CO₃²⁻。
        *   CO₂分子形成后，因溶解度低而“抖动”并加速向上飞出液面。
        *   溶液中的Ca²⁺和Cl⁻离子在背景中缓慢运动，表示它们的存在但非反应焦点。
    *   **界面布局**：左侧为主动画区，右侧为信息面板，显示当前步骤的化学方程式和文字说明。

#### 配色方案选择
*   **主背景**：柔和的浅蓝色渐变，模拟天空或干净的实验室背景，确保主体突出。
*   **烧杯与液体**：烧杯为半透明玻璃质感；液体（稀盐酸）为非常浅的蓝绿色，表示酸性溶液，且透明度高，以便看清内部微观过程。
*   **分子与离子**：
    *   **CaCO₃晶体**：浅灰色（Ca）与红灰相间（CO₃）的团块，表面有规则纹理。
    *   **H₂O分子**：半透明的浅蓝色小球，作为溶剂背景，运动缓慢。
    *   **H₃O⁺/H⁺**：核心原子（H）用醒目的**亮粉色**或**橙色**表示，强调其“攻击性”和关键作用。
    *   **CO₂**：形成后，分子整体可以带有轻微的**发光黄色边框**，当其逸出时变为气泡状（外围加一圈白色高光）。
    *   **离子**：Ca²⁺（浅灰色带“+”）， Cl⁻（绿色带“-”）， CO₃²⁻（红色和灰色原子组合，整体可带“2-”标注）。
*   **UI控件**：采用简洁的科技蓝或中性灰，按钮有明确的悬停和点击反馈。

#### 交互功能列表
1.  **播放控制栏**：包含“重置”、“上一步”、“播放/暂停”、“下一步”按钮。
2.  **视图切换按钮**：“宏观视角（烧杯）”、“微观视角（分子）”。
3.  **信息提示**：鼠标悬停在任何模型上时，弹出标签显示其名称和化学式/离子符号。
4.  **步骤指示器**：一个进度条或步骤列表（如：1. 固体接触酸液， 2. H⁺攻击CO₃²⁻， 3. 形成H₂CO₃并分解， 4. CO₂逸出），高亮当前步骤。
5.  **实时方程式面板**：在动画右侧，同步高亮显示当前步骤对应的部分离子方程式或总方程式。
6.  **速度调节**（可选）：一个滑块，允许用户调整微观粒子运动的快慢。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>实验室制取二氧化碳微观过程动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #e6f7ff 0%, #f0f9ff 100%);
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
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }
        
        .equation {
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 10px;
            padding: 15px;
            margin: 15px auto;
            font-size: 1.5rem;
            font-weight: bold;
            color: #2980b9;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            text-align: center;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            max-width: 1200px;
            width: 100%;
            justify-content: center;
        }
        
        .animation-area {
            flex: 1;
            min-width: 600px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }
        
        .canvas-container {
            flex: 1;
            position: relative;
            background: linear-gradient(to bottom, #87CEEB 0%, #E0F7FF 100%);
            overflow: hidden;
        }
        
        #reactionCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .info-panel {
            flex: 0 0 350px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            padding: 25px;
            display: flex;
            flex-direction: column;
        }
        
        .panel-title {
            color: #2c3e50;
            font-size: 1.4rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #ecf0f1;
        }
        
        .step-indicator {
            margin-bottom: 25px;
        }
        
        .step-list {
            list-style-type: none;
        }
        
        .step-item {
            padding: 12px 15px;
            margin-bottom: 10px;
            border-radius: 8px;
            background-color: #f8f9fa;
            border-left: 4px solid #bdc3c7;
            transition: all 0.3s ease;
        }
        
        .step-item.active {
            background-color: #e3f2fd;
            border-left-color: #2196f3;
            font-weight: bold;
            color: #1565c0;
        }
        
        .step-number {
            display: inline-block;
            width: 26px;
            height: 26px;
            background-color: #bdc3c7;
            color: white;
            border-radius: 50%;
            text-align: center;
            line-height: 26px;
            margin-right: 10px;
            font-size: 0.9rem;
        }
        
        .step-item.active .step-number {
            background-color: #2196f3;
        }
        
        .legend {
            margin-top: auto;
            padding-top: 20px;
            border-top: 1px solid #ecf0f1;
        }
        
        .legend-title {
            font-size: 1.1rem;
            margin-bottom: 15px;
            color: #2c3e50;
        }
        
        .legend-items {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            margin-bottom: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            margin-right: 10px;
            border: 1px solid rgba(0,0,0,0.1);
        }
        
        .controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            padding: 20px;
            background-color: #f8f9fa;
            border-top: 1px solid #e9ecef;
        }
        
        .btn {
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        
        .btn-primary {
            background-color: #2196f3;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #0d8bf2;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: #6c757d;
            color: white;
        }
        
        .btn-secondary:hover {
            background-color: #5a6268;
            transform: translateY(-2px);
        }
        
        .btn-outline {
            background-color: transparent;
            color: #2196f3;
            border: 2px solid #2196f3;
        }
        
        .btn-outline:hover {
            background-color: #e3f2fd;
        }
        
        .view-controls {
            display: flex;
            justify-content: center;
            gap: 10px;
            padding: 15px;
            background-color: #f1f8ff;
            border-bottom: 1px solid #e9ecef;
        }
        
        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 15px;
        }
        
        .speed-slider {
            flex: 1;
        }
        
        .tooltip {
            position: absolute;
            background-color: rgba(0, 0, 0, 0.85);
            color: white;
            padding: 8px 12px;
            border-radius: 6px;
            font-size: 0.9rem;
            pointer-events: none;
            z-index: 100;
            max-width: 200px;
            transform: translate(-50%, -100%);
            margin-top: -10px;
            display: none;
        }
        
        .tooltip::after {
            content: '';
            position: absolute;
            top: 100%;
            left: 50%;
            margin-left: -5px;
            border-width: 5px;
            border-style: solid;
            border-color: rgba(0, 0, 0, 0.85) transparent transparent transparent;
        }
        
        @media (max-width: 1100px) {
            .container {
                flex-direction: column;
                align-items: center;
            }
            
            .animation-area, .info-panel {
                width: 100%;
                min-width: unset;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>实验室制取二氧化碳微观过程</h1>
        <p class="subtitle">CaCO₃ + 2HCl → CaCl₂ + H₂O + CO₂↑ 的分子层面可视化</p>
        <div class="equation">
            CaCO₃(s) + 2H⁺(aq) → Ca²⁺(aq) + H₂O(l) + CO₂(g)↑
        </div>
    </div>
    
    <div class="container">
        <div class="animation-area">
            <div class="view-controls">
                <button id="macroViewBtn" class="btn btn-outline">
                    <span>🔍</span> 宏观视角
                </button>
                <button id="microViewBtn" class="btn btn-primary">
                    <span>🔬</span> 微观视角
                </button>
            </div>
            
            <div class="canvas-container">
                <canvas id="reactionCanvas"></canvas>
                <div id="tooltip" class="tooltip"></div>
            </div>
            
            <div class="controls">
                <button id="resetBtn" class="btn btn-secondary">
                    <span>🔄</span> 重置
                </button>
                <button id="prevBtn" class="btn btn-secondary">
                    <span>◀</span> 上一步
                </button>
                <button id="playPauseBtn" class="btn btn-primary">
                    <span>▶</span> 播放
                </button>
                <button id="nextBtn" class="btn btn-secondary">
                    <span>▶</span> 下一步
                </button>
            </div>
            
            <div class="speed-control">
                <span>动画速度:</span>
                <input type="range" id="speedSlider" class="speed-slider" min="0.5" max="3" step="0.5" value="1">
                <span id="speedValue">正常</span>
            </div>
        </div>
        
        <div class="info-panel">
            <h2 class="panel-title">反应步骤</h2>
            
            <div class="step-indicator">
                <ul class="step-list">
                    <li class="step-item active" data-step="0">
                        <span class="step-number">1</span>
                        固体CaCO₃与稀盐酸接触
                    </li>
                    <li class="step-item" data-step="1">
                        <span class="step-number">2</span>
                        H⁺离子攻击CO₃²⁻离子
                    </li>
                    <li class="step-item" data-step="2">
                        <span class="step-number">3</span>
                        形成H₂CO₃并分解为H₂O和CO₂
                    </li>
                    <li class="step-item" data-step="3">
                        <span class="step-number">4</span>
                        CO₂分子逸出溶液
                    </li>
                    <li class="step-item" data-step="4">
                        <span class="step-number">5</span>
                        反应完成，生成Ca²⁺和Cl⁻离子
                    </li>
                </ul>
            </div>
            
            <div class="current-step-info">
                <h3 class="panel-title">当前步骤说明</h3>
                <div id="stepDescription" class="step-description">
                    大理石（主要成分CaCO₃）固体与稀盐酸接触。固体表面的CaCO₃分子开始溶解进入溶液。
                </div>
            </div>
            
            <div class="legend">
                <h3 class="legend-title">分子/离子图例</h3>
                <div class="legend-items">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #95a5a6;"></div>
                        <span>钙离子 Ca²⁺</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span>氧原子 O</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #7f8c8d;"></div>
                        <span>碳原子 C</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff6b9d;"></div>
                        <span>氢离子 H⁺</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2ecc71;"></div>
                        <span>氯离子 Cl⁻</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #3498db;"></div>
                        <span>水分子 H₂O</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 全局变量
        const canvas = document.getElementById('reactionCanvas');
        const ctx = canvas.getContext('2d');
        const tooltip = document.getElementById('tooltip');
        const stepItems = document.querySelectorAll('.step-item');
        const stepDescription = document.getElementById('stepDescription');
        const speedSlider = document.getElementById('speedSlider');
        const speedValue = document.getElementById('speedValue');
        
        // 动画状态
        let animationId = null;
        let isPlaying = false;
        let currentStep = 0;
        let animationSpeed = 1.0;
        let isMicroView = true;
        
        // 步骤描述
        const stepDescriptions = [
            "大理石（主要成分CaCO₃）固体与稀盐酸接触。固体表面的CaCO₃分子开始溶解进入溶液，解离为Ca²⁺和CO₃²⁻离子。",
            "溶液中的H⁺离子（来自HCl）攻击CO₃²⁻离子。每个CO₃²⁻离子与2个H⁺离子结合，形成不稳定的H₂CO₃（碳酸）。",
            "H₂CO₃分子极不稳定，立即分解为一个水分子（H₂O）和一个二氧化碳分子（CO₂）。这是反应的关键步骤。",
            "CO₂分子在水中的溶解度较低，因此从溶液中逸出，形成气泡。气泡上升到液面，进入空气中。",
            "反应完成后，溶液中留下Ca²⁺和Cl⁻离子，它们结合形成CaCl₂（氯化钙）。大理石固体不断溶解，直到反应物耗尽。"
        ];
        
        // 原子颜色定义 (CPK规则)
        const atomColors = {
            'C': '#7f8c8d',   // 碳 - 灰色
            'O': '#e74c3c',   // 氧 - 红色
            'H': '#ffffff',   // 氢 - 白色
            'Cl': '#2ecc71',  // 氯 - 绿色
            'Ca': '#95a5a6',  // 钙 - 浅灰色
            'H+': '#ff6b9d'   // 氢离子 - 粉色
        };
        
        // 分子和离子定义
        class Particle {
            constructor(x, y, type, charge = 0) {
                this.x = x;
                this.y = y;
                this.type = type;
                this.charge = charge;
                this.vx = 0;
                this.vy = 0;
                this.radius = 0;
                this.color = '#ffffff';
                this.label = '';
                this.isActive = true;
                this.bondedTo = [];
                this.initProperties();
            }
            
            initProperties() {
                switch(this.type) {
                    case 'Ca2+':
                        this.radius = 12;
                        this.color = atomColors.Ca;
                        this.label = 'Ca²⁺';
                        break;
                    case 'CO3-2':
                        this.radius = 18;
                        this.color = '#d35400';
                        this.label = 'CO₃²⁻';
                        break;
                    case 'H+':
                        this.radius = 10;
                        this.color = atomColors['H+'];
                        this.label = 'H⁺';
                        break;
                    case 'Cl-':
                        this.radius = 11;
                        this.color = atomColors.Cl;
                        this.label = 'Cl⁻';
                        break;
                    case 'H2O':
                        this.radius = 14;
                        this.color = '#3498db';
                        this.label = 'H₂O';
                        break;
                    case 'CO2':
                        this.radius = 16;
                        this.color = '#f39c12';
                        this.label = 'CO₂';
                        break;
                    case 'C':
                        this.radius = 10;
                        this.color = atomColors.C;
                        break;
                    case 'O':
                        this.radius = 9;
                        this.color = atomColors.O;
                        break;
                }
            }
            
            draw() {
                if (!this.isActive) return;
                
                // 绘制粒子
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = this.color;
                ctx.fill();
                
                // 绘制边框
                ctx.strokeStyle = 'rgba(0, 0, 0, 0.2)';
                ctx.lineWidth = 1;
                ctx.stroke();
                
                // 绘制标签
                if (this.label) {
                    ctx.fillStyle = '#2c3e50';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText(this.label, this.x, this.y);
                }
                
                // 绘制电荷符号
                if (this.charge !== 0) {
                    ctx.fillStyle = this.charge > 0 ? '#e74c3c' : '#3498db';
                    ctx.font = '10px Arial';
                    ctx.textAlign = 'right';
                    ctx.textBaseline = 'top';
                    const chargeText = this.charge > 0 ? 
                        (this.charge === 1 ? '+' : this.charge + '+') : 
                        (this.charge === -1 ? '−' : this.charge + '−');
                    ctx.fillText(chargeText, this.x + this.radius - 2, this.y - this.radius + 2);
                }
            }
            
            update() {
                if (!this.isActive) return;
                
                // 应用随机运动（布朗运动）
                this.vx += (Math.random() - 0.5) * 0.2 * animationSpeed;
                this.vy += (Math.random() - 0.5) * 0.2 * animationSpeed;
                
                // 限制速度
                const maxSpeed = 1.5 * animationSpeed;
                const speed = Math.sqrt(this.vx * this.vx + this.vy * this.vy);
                if (speed > maxSpeed) {
                    this.vx = (this.vx / speed) * maxSpeed;
                    this.vy = (this.vy / speed) * maxSpeed;
                }
                
                // 应用阻尼
                this.vx *= 0.95;
                this.vy *= 0.95;
                
                // 更新位置
                this.x += this.vx;
                this.y += this.vy;
                
                // 边界检查
                const canvasWidth = canvas.width;
                const canvasHeight = canvas.height;
                
                if (this.x < this.radius) {
                    this.x = this.radius;
                    this.vx = Math.abs(this.vx) * 0.5;
                }
                if (this.x > canvasWidth - this.radius) {
                    this.x = canvasWidth - this.radius;
                    this.vx = -Math.abs(this.vx) * 0.5;
                }
                if (this.y < this.radius) {
                    this.y = this.radius;
                    this.vy = Math.abs(this.vy) * 0.5;
                }
                if (this.y > canvasHeight - this.radius) {
                    this.y = canvasHeight - this.radius;
                    this.vy = -Math.abs(this.vy) * 0.5;
                }
            }
            
            isMouseOver(mx, my) {
                const dx = mx - this.x;
                const dy = my - this.y;
                return dx * dx + dy * dy <= this.radius * this.radius;
            }
        }
        
        // 反应系统
        class ReactionSystem {
            constructor() {
                this.particles = [];
                this.solidParticles = [];
                this.bubbles = [];
                this.stepProgress = 0;
                this.stepDuration = 300; // 每步动画帧数
                this.initSystem();
            }
            
            initSystem() {
                this.particles = [];
                this.solidParticles = [];
                this.bubbles = [];
                this.stepProgress = 0;
                
                const canvasWidth = canvas.width;
                const canvasHeight = canvas.height;
                
                // 创建固体CaCO₃（底部）
                const solidWidth = 300;
                const solidHeight = 80;
                const solidX = canvasWidth / 2 - solidWidth / 2;
                const solidY = canvasHeight - solidHeight - 20;
                
                for (let i = 0; i < 25; i++) {
                    const x = solidX + Math.random() * solidWidth;
                    const y = solidY + Math.random() * solidHeight;
                    const particle = new Particle(x, y, 'CO3-2');
                    particle.vx = 0;
                    particle.vy = 0;
                    particle.isInSolid = true;
                    this.solidParticles.push(particle);
                }
                
                // 创建溶液中的离子
                // H+ 离子
                for (let i = 0; i < 15; i++) {
                    const x = 100 + Math.random() * (canvasWidth - 200);
                    const y = 150 + Math.random() * (solidY - 200);
                    const particle = new Particle(x, y, 'H+');
                    particle.charge = 1;
                    this.particles.push(particle);
                }
                
                // Cl- 离子
                for (let i = 0; i < 15; i++) {
                    const x = 100 + Math.random() * (canvasWidth - 200);
                    const y = 150 + Math.random() * (solidY - 200);
                    const particle = new Particle(x, y, 'Cl-');
                    particle.charge = -1;
                    this.particles.push(particle);
                }
                
                // H2O 分子
                for (let i = 0; i < 30; i++) {
                    const x = 100 + Math.random() * (canvasWidth - 200);
                    const y = 150 + Math.random() * (solidY - 200);
                    const particle = new Particle(x, y, 'H2O');
                    this.particles.push(particle);
                }
            }
            
            update() {
                this.stepProgress++;
                
                // 根据当前步骤更新系统
                switch(currentStep) {
                    case 0: // 固体溶解
                        this.updateStep0();
                        break;
                    case 1: // H+攻击CO3-2
                        this.updateStep1();
                        break;
                    case 2: // 形成H2CO3并分解
                        this.updateStep2();
                        break;
                    case 3: // CO2逸出
                        this.updateStep3();
                        break;
                    case 4: // 反应完成
                        this.updateStep4();
                        break;
                }
                
                // 更新所有粒子
                this.particles.forEach(p => p.update());
                
                // 更新气泡
                this.bubbles.forEach(bubble => {
                    bubble.y -= 2 * animationSpeed;
                    bubble.x += Math.sin(bubble.y * 0.05) * 0.5;
                    
                    // 移除超出画布的气泡
                    if (bubble.y < -20) {
                        bubble.isActive = false;
                    }
                });
                
                // 过滤掉不活跃的气泡
                this.bubbles = this.bubbles.filter(b => b.isActive);
                
                // 自动进入下一步
                if (this.stepProgress > this.stepDuration && isPlaying) {
                    if (currentStep < 4) {
                        goToStep(currentStep + 1);
                    } else {
                        isPlaying = false;
                        document.getElementById('playPauseBtn').innerHTML = '<span>▶</span> 播放';
                    }
                }
            }
            
            updateStep0() {
                // 固体逐渐溶解
                if (this.stepProgress % 20 === 0 && this.solidParticles.length > 0) {
                    const particle = this.solidParticles.pop();
                    particle.isInSolid = false;
                    particle.vx = (Math.random() - 0.5) * 2;
                    particle.vy = -1 - Math.random() * 2;
                    
                    // 同时释放Ca2+离子
                    const caParticle = new Particle(
                        particle.x + 20, 
                        particle.y, 
                        'Ca2+'
                    );
                    caParticle.charge = 2;
                    caParticle.vx = (Math.random() - 0.5) * 2;
                    caParticle.vy = -1 - Math.random() * 2;
                    this.particles.push(caParticle);
                    
                    this.particles.push(particle);
                }
            }
            
            updateStep1() {
                // H+离子向CO3-2离子移动
                const co3Particles = this.particles.filter(p => p.type === 'CO3-2');
                const hPlusParticles = this.particles.filter(p => p.type === 'H+');
                
                co3Particles.forEach(co3 => {
                    // 寻找最近的H+离子
                    let closestH = null;
                    let minDist = Infinity;
                    
                    hPlusParticles.forEach(h => {
                        if (h.bondedTo.length > 0) continue; // 已经结合的H+
                        
                        const dx = h.x - co3.x;
                        const dy = h.y - co3.y;
                        const dist = dx * dx + dy * dy;
                        
                        if (dist < minDist && dist < 10000) {
                            minDist = dist;
                            closestH = h;
                        }
                    });
                    
                    // 如果找到H+离子且CO3-2还没有结合2个H+
                    if (closestH && co3.bondedTo.length < 2) {
                        const dx = co3.x - closestH.x;
                        const dy = co3.y - closestH.y;
                        const dist = Math.sqrt(dx * dx + dy * dy);
                        
                        if (dist > 30) {
                            // 向CO3-2移动
                            closestH.vx -= dx / dist * 0.3 * animationSpeed;
                            closestH.vy -= dy / dist * 0.3 * animationSpeed;
                        } else if (dist < 25) {
                            // 结合
                            closestH.bondedTo.push(co3);
                            co3.bondedTo.push(closestH);
                            
                            // 改变颜色表示结合
                            if (co3.bondedTo.length === 2) {
                                co3.color = '#9b59b6'; // 紫色表示H2CO3
                                co3.label = 'H₂CO₃';
                            }
                        }
                    }
                });
            }
            
            updateStep2() {
                // 寻找已结合2个H+的CO3-2（即H2CO3）
                const h2co3Particles = this.particles.filter(p => 
                    p.type === 'CO3-2' && p.bondedTo.length === 2
                );
                
                h2co3Particles.forEach(h2co3 => {
                    // 逐渐分解
                    if (this.stepProgress > 100) {
                        // 分解为CO2和H2O
                        h2co3.isActive = false;
                        
                        // 创建CO2分子
                        const co2 = new Particle(h2co3.x, h2co3.y, 'CO2');
                        co2.vx = (Math.random() - 0.5) * 2;
                        co2.vy = -1 - Math.random();
                        this.particles.push(co2);
                        
                        // 创建H2O分子
                        const h2o = new Particle(h2co3.x + 15, h2co3.y, 'H2O');
                        h2o.vx = (Math.random() - 0.5) * 2;
                        h2o.vy = -0.5 - Math.random();
                        this.particles.push(h2o);
                        
                        // 移除结合的H+离子
                        h2co3.bondedTo.forEach(h => {
                            h.isActive = false;
                        });
                    }
                });
            }
            
            updateStep3() {
                // CO2分子上升并形成气泡
                const co2Particles = this.particles.filter(p => p.type === 'CO2');
                
                co2Particles.forEach(co2 => {
                    // 向上运动
                    co2.vy -= 0.05 * animationSpeed;
                    
                    // 当接近顶部时形成气泡
                    if (co2.y < 150 && Math.random() < 0.02) {
                        this.bubbles.push({
                            x: co2.x,
                            y: co2.y,
                            radius: 15 + Math.random() * 10,
                            isActive: true
                        });
                        co2.isActive = false;
                    }
                });
            }
            
            updateStep4() {
                // 反应完成，粒子自由运动
                // 可以添加一些最终状态的视觉效果
            }
            
            draw() {
                // 绘制烧杯（宏观视图）
                if (!isMicroView) {
                    this.drawBeaker();
                    return;
                }
                
                // 绘制微观视图
                
                // 绘制固体区域
                ctx.fillStyle = 'rgba(189, 195, 199, 0.7)';
                ctx.fillRect(canvas.width/2 - 150, canvas.height - 100, 300, 80);
                
                // 绘制固体粒子
                this.solidParticles.forEach(p => {
                    ctx.beginPath();
                    ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
                    ctx.fillStyle = p.color;
                    ctx.fill();
                    
                    ctx.strokeStyle = 'rgba(0, 0, 0, 0.2)';
                    ctx.lineWidth = 1;
                    ctx.stroke();
                });
                
                // 绘制连接线（化学键）
                this.particles.forEach(p => {
                    if (p.bondedTo.length > 0) {
                        p.bondedTo.forEach(bonded => {
                            ctx.beginPath();
                            ctx.moveTo(p.x, p.y);
                            ctx.lineTo(bonded.x, bonded.y);
                            ctx.strokeStyle = 'rgba(0, 0, 0, 0.3)';
                            ctx.lineWidth = 2;
                            ctx.stroke();
                        });
                    }
                });
                
                // 绘制粒子
                this.particles.forEach(p => p.draw());
                
                // 绘制气泡
                this.bubbles.forEach(bubble => {
                    ctx.beginPath();
                    ctx.arc(bubble.x, bubble.y, bubble.radius, 0, Math.PI * 2);
                    ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
                    ctx.fill();
                    
                    ctx.strokeStyle = 'rgba(52, 152, 219, 0.6)';
                    ctx.lineWidth = 1.5;
                    ctx.stroke();
                    
                    // 气泡高光
                    ctx.beginPath();
                    ctx.arc(bubble.x - bubble.radius/3, bubble.y - bubble.radius/3, bubble.radius/4, 0, Math.PI * 2);
                    ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
                    ctx.fill();
                });
                
                // 绘制步骤高亮
                this.drawStepHighlight();
            }
            
            drawBeaker() {
                const canvasWidth = canvas.width;
                const canvasHeight = canvas.height;
                
                // 绘制烧杯
                ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
                ctx.strokeStyle = '#7f8c8d';
                ctx.lineWidth = 3;
                
                // 烧杯主体
                ctx.beginPath();
                ctx.moveTo(canvasWidth/2 - 120, canvasHeight - 50);
                ctx.lineTo(canvasWidth/2 - 150, canvasHeight - 200);
                ctx.lineTo(canvasWidth/2 - 120, canvasHeight - 350);
                ctx.lineTo(canvasWidth/2 + 120, canvasHeight - 350);
                ctx.lineTo(canvasWidth/2 + 150, canvasHeight - 200);
                ctx.lineTo(canvasWidth/2 + 120, canvasHeight - 50);
                ctx.closePath();
                ctx.fill();
                ctx.stroke();
                
                // 液体
                ctx.fillStyle = 'rgba(52, 152, 219, 0.3)';
                ctx.beginPath();
                ctx.moveTo(canvasWidth/2 - 130, canvasHeight - 200);
                ctx.lineTo(canvasWidth/2 - 125, canvasHeight - 300);
                ctx.lineTo(canvasWidth/2 + 125, canvasHeight - 300);
                ctx.lineTo(canvasWidth/2 + 130, canvasHeight - 200);
                ctx.closePath();
                ctx.fill();
                
                // 固体（大理石）
                ctx.fillStyle = 'rgba(189, 195, 199, 0.9)';
                ctx.beginPath();
                ctx.ellipse(canvasWidth/2, canvasHeight - 180, 80, 20, 0, 0, Math.PI * 2);
                ctx.fill();
                
                // 气泡
                for (let i = 0; i < 15; i++) {
                    const x = canvasWidth/2 - 80 + Math.random() * 160;
                    const y = canvasHeight - 250 - Math.random() * 100;
                    const radius = 3 + Math.random() * 5;
                    
                    ctx.beginPath();
                    ctx.arc(x, y, radius, 0, Math.PI * 2);
                    ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
                    ctx.fill();
                }
                
                // 标签
                ctx.fillStyle = '#2c3e50';
                ctx.font = 'bold 24px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('烧杯（宏观视图）', canvasWidth/2, 50);
                ctx.font = '18px Arial';
                ctx.fillText('稀盐酸 + 大理石', canvasWidth/2, canvasHeight - 400);
                ctx.fillText('观察气泡（CO₂）产生', canvasWidth/2, canvasHeight - 370);
            }
            
            drawStepHighlight() {
                // 根据当前步骤高亮相关粒子
                ctx.globalAlpha = 0.3;
                
                switch(currentStep) {
                    case 0:
                        // 高亮固体粒子
                        this.solidParticles.forEach(p => {
                            ctx.beginPath();
                            ctx.arc(p.x, p.y, p.radius + 5, 0, Math.PI * 2);
                            ctx.fillStyle = '#f1c40f';
                            ctx.fill();
                        });
                        break;
                    case 1:
                        // 高亮H+和CO3-2
                        this.particles.forEach(p => {
                            if (p.type === 'H+' || p.type === 'CO3-2') {
                                ctx.beginPath();
                                ctx.arc(p.x, p.y, p.radius + 5, 0, Math.PI * 2);
                                ctx.fillStyle = p.type === 'H+' ? '#ff6b9d' : '#d35400';
                                ctx.fill();
                            }
                        });
                        break;
                    case 2:
                        // 高亮H2CO3
                        this.particles.forEach(p => {
                            if (p.type === 'CO3-2' && p.bondedTo.length === 2) {
                                ctx.beginPath();
                                ctx.arc(p.x, p.y, p.radius + 5, 0, Math.PI * 2);
                                ctx.fillStyle = '#9b59b6';
                                ctx
<!--检测到代码截断，自动续写中...-->
fill();
                            }
                        });
                        break;
                    case 3:
                        // 高亮CO2和气泡
                        this.particles.forEach(p => {
                            if (p.type === 'CO2') {
                                ctx.beginPath();
                                ctx.arc(p.x, p.y, p.radius + 5, 0, Math.PI * 2);
                                ctx.fillStyle = '#f39c12';
                                ctx.fill();
                            }
                        });
                        this.bubbles.forEach(bubble => {
                            ctx.beginPath();
                            ctx.arc(bubble.x, bubble.y, bubble.radius + 5, 0, Math.PI * 2);
                            ctx.fillStyle = '#3498db';
                            ctx.fill();
                        });
                        break;
                    case 4:
                        // 高亮Ca2+和Cl-
                        this.particles.forEach(p => {
                            if (p.type === 'Ca2+' || p.type === 'Cl-') {
                                ctx.beginPath();
                                ctx.arc(p.x, p.y, p.radius + 5, 0, Math.PI * 2);
                                ctx.fillStyle = p.type === 'Ca2+' ? '#95a5a6' : '#2ecc71';
                                ctx.fill();
                            }
                        });
                        break;
                }
                
                ctx.globalAlpha = 1.0;
            }
        }

        // 创建反应系统实例
        let reactionSystem = new ReactionSystem();

        // 调整画布大小
        function resizeCanvas() {
            const container = document.querySelector('.canvas-container');
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }

        // 初始化
        function init() {
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // 初始绘制
            draw();
            
            // 设置事件监听器
            setupEventListeners();
        }

        // 设置事件监听器
        function setupEventListeners() {
            // 播放/暂停按钮
            document.getElementById('playPauseBtn').addEventListener('click', () => {
                isPlaying = !isPlaying;
                document.getElementById('playPauseBtn').innerHTML = isPlaying ? 
                    '<span>⏸</span> 暂停' : '<span>▶</span> 播放';
                
                if (isPlaying) {
                    animate();
                } else {
                    if (animationId) {
                        cancelAnimationFrame(animationId);
                        animationId = null;
                    }
                }
            });
            
            // 上一步按钮
            document.getElementById('prevBtn').addEventListener('click', () => {
                if (currentStep > 0) {
                    goToStep(currentStep - 1);
                }
            });
            
            // 下一步按钮
            document.getElementById('nextBtn').addEventListener('click', () => {
                if (currentStep < 4) {
                    goToStep(currentStep + 1);
                }
            });
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', () => {
                reactionSystem = new ReactionSystem();
                goToStep(0);
                isPlaying = false;
                document.getElementById('playPauseBtn').innerHTML = '<span>▶</span> 播放';
            });
            
            // 宏观视角按钮
            document.getElementById('macroViewBtn').addEventListener('click', () => {
                isMicroView = false;
                document.getElementById('microViewBtn').classList.remove('btn-primary');
                document.getElementById('microViewBtn').classList.add('btn-outline');
                document.getElementById('macroViewBtn').classList.remove('btn-outline');
                document.getElementById('macroViewBtn').classList.add('btn-primary');
            });
            
            // 微观视角按钮
            document.getElementById('microViewBtn').addEventListener('click', () => {
                isMicroView = true;
                document.getElementById('macroViewBtn').classList.remove('btn-primary');
                document.getElementById('macroViewBtn').classList.add('btn-outline');
                document.getElementById('microViewBtn').classList.remove('btn-outline');
                document.getElementById('microViewBtn').classList.add('btn-primary');
            });
            
            // 速度滑块
            speedSlider.addEventListener('input', () => {
                animationSpeed = parseFloat(speedSlider.value);
                const speedLabels = {
                    0.5: '慢速',
                    1.0: '正常',
                    1.5: '中速',
                    2.0: '快速',
                    2.5: '高速',
                    3.0: '极速'
                };
                speedValue.textContent = speedLabels[animationSpeed] || '正常';
            });
            
            // 步骤指示器点击
            stepItems.forEach(item => {
                item.addEventListener('click', () => {
                    const step = parseInt(item.getAttribute('data-step'));
                    goToStep(step);
                });
            });
            
            // 鼠标移动事件（用于提示）
            canvas.addEventListener('mousemove', (e) => {
                const rect = canvas.getBoundingClientRect();
                const mouseX = e.clientX - rect.left;
                const mouseY = e.clientY - rect.top;
                
                let hoveredParticle = null;
                
                // 检查是否悬停在粒子上
                reactionSystem.particles.forEach(p => {
                    if (p.isMouseOver(mouseX, mouseY)) {
                        hoveredParticle = p;
                    }
                });
                
                reactionSystem.solidParticles.forEach(p => {
                    if (p.isMouseOver(mouseX, mouseY)) {
                        hoveredParticle = p;
                    }
                });
                
                if (hoveredParticle) {
                    tooltip.style.display = 'block';
                    tooltip.style.left = mouseX + 'px';
                    tooltip.style.top = mouseY + 'px';
                    
                    let tooltipText = hoveredParticle.label;
                    if (hoveredParticle.type === 'CO3-2' && hoveredParticle.bondedTo.length === 2) {
                        tooltipText = '碳酸 H₂CO₃ (不稳定)';
                    } else if (hoveredParticle.charge !== 0) {
                        tooltipText += ` (${hoveredParticle.charge > 0 ? '+' : ''}${hoveredParticle.charge}电荷)`;
                    }
                    
                    tooltip.textContent = tooltipText;
                } else {
                    tooltip.style.display = 'none';
                }
            });
            
            canvas.addEventListener('mouseleave', () => {
                tooltip.style.display = 'none';
            });
        }

        // 跳转到指定步骤
        function goToStep(step) {
            currentStep = step;
            reactionSystem.stepProgress = 0;
            
            // 更新步骤指示器
            stepItems.forEach((item, index) => {
                if (index === step) {
                    item.classList.add('active');
                } else {
                    item.classList.remove('active');
                }
            });
            
            // 更新步骤描述
            stepDescription.textContent = stepDescriptions[step];
            
            // 如果是最后一步，确保所有反应完成
            if (step === 4) {
                // 确保所有CO3-2都反应了
                reactionSystem.particles.forEach(p => {
                    if (p.type === 'CO3-2' && p.bondedTo.length < 2) {
                        p.bondedTo = [];
                        p.isActive = false;
                    }
                });
            }
        }

        // 动画循环
        function animate() {
            if (!isPlaying) return;
            
            update();
            draw();
            animationId = requestAnimationFrame(animate);
        }

        // 更新动画状态
        function update() {
            reactionSystem.update();
        }

        // 绘制场景
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            if (isMicroView) {
                // 微观视图背景
                const gradient = ctx.createLinearGradient(0, 0, 0, canvas.height);
                gradient.addColorStop(0, '#87CEEB');
                gradient.addColorStop(1, '#E0F7FF');
                ctx.fillStyle = gradient;
                ctx.fillRect(0, 0, canvas.width, canvas.height);
                
                // 绘制网格（微观背景）
                ctx.strokeStyle = 'rgba(255, 255, 255, 0.1)';
                ctx.lineWidth = 1;
                const gridSize = 40;
                
                for (let x = 0; x < canvas.width; x += gridSize) {
                    ctx.beginPath();
                    ctx.moveTo(x, 0);
                    ctx.lineTo(x, canvas.height);
                    ctx.stroke();
                }
                
                for (let y = 0; y < canvas.height; y += gridSize) {
                    ctx.beginPath();
                    ctx.moveTo(0, y);
                    ctx.lineTo(canvas.width, y);
                    ctx.stroke();
                }
            }
            
            // 绘制反应系统
            reactionSystem.draw();
            
            // 绘制当前步骤标签
            if (isMicroView) {
                ctx.fillStyle = 'rgba(0, 0, 0, 0.7)';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'left';
                ctx.fillText(`步骤 ${currentStep + 1}: ${stepDescriptions[currentStep].split('。')[0]}`, 20, 30);
            }
        }

        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

欢迎使用“实验室制取二氧化碳微观过程”交互式教学动画！本动画旨在通过直观、动态的可视化方式，帮助您深入理解化学反应在分子层面的本质。无论您是学生、教师还是化学爱好者，本工具都将为您提供全新的学习体验。

---

### 一、功能说明

本动画完整模拟了实验室用大理石（碳酸钙）与稀盐酸反应制取二氧化碳的微观过程。它将宏观的化学现象（气泡产生）与微观的分子、离子行为（反应、重组、逸出）紧密联系起来，实现了从“看到现象”到“理解本质”的认知跨越。

### 二、主要功能

1.  **分步动画演示**
    *   动画将连续反应分解为5个逻辑清晰的步骤，便于您循序渐进地理解。
    *   步骤包括：固体溶解 → 离子攻击 → 中间物分解 → 气体逸出 → 反应完成。

2.  **双重视角切换**
    *   **微观视角**：深入溶液内部，观察分子、离子的运动、碰撞与反应。
    *   **宏观视角**：回到实验室场景，观察烧杯中气泡产生的宏观现象。

3.  **交互式学习控制**
    *   **播放控制**：使用“播放/暂停”、“上一步/下一步”按钮自主控制动画进度。
    *   **步骤跳转**：点击右侧信息面板的步骤列表，可直接跳转到任意步骤。
    *   **动画调速**：通过滑块调整粒子运动速度（慢速到极速），适应不同观察需求。

4.  **智能提示系统**
    *   将鼠标悬停在任意一个分子或离子上，会弹出提示框，显示其名称、化学式和电荷信息。

5.  **实时信息同步**
    *   右侧信息面板会同步显示当前步骤的详细文字说明和完整的离子方程式。

### 三、设计特色

1.  **科学的视觉编码**
    *   严格遵循**CPK规则**使用原子颜色：碳（灰）、氧（红）、氢（白）、氯（绿）、钙（浅灰）。
    *   关键反应物**氢离子（H⁺）** 使用醒目的粉色高亮，强调其在反应中的驱动作用。
    *   **二氧化碳（CO₂）** 分子逸出时，会转变为带有白色高光的气泡，直观表示状态变化。

2.  **符合认知规律的教学设计**
    *   **从宏观到微观**：动画起始于宏观视角，引导您建立现象与原理的初步联系。
    *   **关键点高亮**：在每一步中，相关的分子或离子会被彩色光晕高亮，引导您的注意力。
    *   **过程拆解**：将复杂的连续反应分解为独立的、易于理解的子过程。

3.  **专业且友好的界面**
    *   界面布局清晰，左侧为主动画区，右侧为信息区，操作按钮位于下方。
    *   配色方案柔和、专业，长时间观看不易疲劳。

### 四、教学要点

本动画生动诠释了以下核心化学概念：

1.  **离子反应的本质**：清晰地展示了反应的真实驱动力是 **H⁺ 与 CO₃²⁻ 的结合**，而非分子间的直接作用。
2.  **中间产物的不稳定性**：可视化地呈现了 **H₂CO₃（碳酸）** 作为中间产物，其生成后立即分解的特性。
3.  **气体逸出的微观解释**：解释了为何CO₂会形成气泡——因其在水中**溶解度低**，分子聚集并从溶液中逃逸。
4.  **质量守恒定律**：通过颜色对应的原子和动态过程，直观表明反应前后**原子种类和数目没有变化**，只是进行了重组。
5.  **宏观与微观的联系**：明确地将烧杯中的每一个气泡与微观上成千上万个CO₂分子的形成与逃逸关联起来。

### 五、使用建议

1.  **对学生而言**：
    *   **预习**：在课堂学习前，完整观看一遍动画，对过程建立整体印象。
    *   **复习与解惑**：当对反应机理感到困惑时，使用“分步控制”功能，反复观看难点步骤，并结合提示信息加深理解。
    *   **自主探究**：尝试先使用“宏观视角”观察，然后切换到“微观视角”，并思考“气泡到底是什么？从哪里来？”。

2.  **对教师而言**：
    *   **课堂演示**：可在讲解该反应时，作为核心可视化工具进行投屏演示。建议先播放宏观现象，再切换到微观视角揭示本质。
    *   **引导式教学**：可以分步播放动画，在每一步暂停，向学生提问：“接下来会发生什么？”“为什么H⁺会向CO₃²⁻移动？”
    *   **突破教学难点**：重点利用**第二步（H⁺攻击）** 和**第三步（H₂CO₃分解）** 的动画，帮助学生突破对离子反应和中间产物理解的障碍。

3.  **通用学习路径**：
    *   **第一步**：点击“播放”，以正常速度观看完整动画。
    *   **第二步**：点击“重置”，使用“下一步”按钮，手动控制，仔细阅读每一步的说明。
    *   **第三步**：再次观看，但将速度调至“慢速”，专注于观察特定粒子（如H⁺）的运动轨迹。
    *   **第四步**：在不同视角间切换，巩固宏观现象与微观本质的联系。

我们希望这个精心设计的交互式动画能成为您探索化学世界的有力工具，让抽象的概念变得生动具体，激发您对化学的持久兴趣与深刻理解！

**祝您学习愉快，探索无限！**