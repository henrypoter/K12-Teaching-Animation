# 需求：浓硫酸稀释（错误操作喷溅危险，动画显示放热+水分子被拉开）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中或高中化学初学者。他们对浓硫酸的强腐蚀性和稀释操作的危险性有抽象认知，但缺乏直观、深刻的感受。
2.  **核心痛点**：
    *   学生不理解为何必须“酸入水”，而“水入酸”会导致危险喷溅。
    *   学生对浓硫酸稀释时释放大量热这一微观本质（硫酸分子水合放热）理解不深。
    *   学生可能因未亲眼见过事故后果而轻视操作规范，存在潜在的安全风险。
3.  **学习目标**：
    *   **知识层面**：理解浓硫酸稀释时“酸入水”操作规范背后的科学原理（密度差异、剧烈放热）。
    *   **微观层面**：可视化理解水合过程是放热本质，以及热量如何导致水沸腾、汽化并引发喷溅。
    *   **情感与态度层面**：通过强烈的视觉冲击，建立对浓硫酸的正确敬畏感，深刻牢记安全操作规范。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念**：
    *   **宏观现象**：浓硫酸密度大于水，稀释时剧烈放热。
    *   **微观本质**：硫酸分子（H₂SO₄）在水合过程中，其离子（H⁺和SO₄²⁻）与水分子（H₂O）强烈相互作用，释放大量能量（热量）。
    *   **危险机制**：局部热量积聚 → 水瞬间沸腾、产生大量水蒸气 → 蒸汽体积急剧膨胀 → 将液体（酸液混合物）从容器中喷溅出来。
2.  **认知规律**：
    *   **从已知到未知**：先展示常见的水被加热沸腾现象，再迁移到浓硫酸稀释的“瞬间沸腾”。
    *   **从宏观到微观**：动画将分为两个层次：第一层展示烧杯内的宏观喷溅现象；第二层（通过点击或自动切换）进入“微观视角”，展示水分子被拉开（电离/水合过程）并释放“热量粒子”（如红色光点或波纹）。
    *   **对比强化记忆**：并排或先后演示**正确操作（酸入水）** 与**错误操作（水入酸）** 。正确操作中，酸滴入大量水中，热量被迅速分散吸收，平稳混合。错误操作中，水加入浓硫酸，浮于表面，局部热量集中，立即引发喷溅。
3.  **交互设计**：
    *   **模式选择**：提供“观看教程”和“自主操作”两种模式。教程模式自动播放完整动画与解说；自主操作模式允许用户点击按钮（“水入酸”或“酸入水”）来触发不同结果。
    *   **关键交互点**：
        *   在“错误操作”动画中，当喷溅即将发生时，动画**暂停**，出现一个问号或惊叹号图标，提示用户思考“为什么会这样？”，点击后进入微观视角解释。
        *   在微观视角中，用户可以**鼠标悬停**在硫酸分子或水分子上，显示其化学式和简要性质（如“H₂SO₄，密度大，溶于水剧烈放热”）。
        *   提供**重置**按钮，允许重复观察。
4.  **视觉呈现**：
    *   **宏观场景**：一个实验室台面上的烧杯。液体用半透明色块表示（浓硫酸为粘稠的深棕色油状液体，水为浅蓝色）。喷溅效果使用粒子系统模拟，具有冲击力但不过度恐怖。
    *   **微观场景**：抽象化表现。水分子用动态的、连接在一起的蓝色小球（O）和白色小球（H）模型。硫酸分子用更大的、结构复杂的黄色模型或直接分解为飘向水分子的H⁺（小灰球）和SO₄²⁻（大黄球）。放热过程用从结合处扩散开的**红色波纹**或向上飘的**红色光点**表示。
    *   **热量可视化**：在烧杯底部或局部，用上升的、扭曲空气的“热浪”效果和颜色变红来表现温度急剧升高。
    *   **信息图层**：通过简洁的标题、步骤文字和箭头指示，引导用户注意力。危险处使用醒目的警示标志（如感叹号）和颜色（红色）。

#### 配色方案选择
*   **主色调**：采用实验室常见的**中性灰白**作为背景和台面，突出容器和液体。
*   **液体颜色**：
    *   **浓硫酸**：采用**深棕色/墨绿色**，表现其粘稠、不透明的特性，与水的清澈形成对比。
    *   **水/稀硫酸**：采用**浅蓝色**，代表安全、温和。
*   **警示与能量色**：
    *   **危险/错误**：使用**亮红色**用于警示标志、喷溅的粒子以及错误操作的按钮。
    *   **热量/能量**：使用**橙红色到亮黄色**的渐变，用于表现放热波纹、光点和高温区域。
    *   **安全/正确**：使用**绿色**用于正确操作的按钮和顺利混合时的提示。
*   **微观模型色**：
    *   **水分子 (H₂O)**：氧原子用**蓝色**，氢原子用**白色**。
    *   **硫酸根离子 (SO₄²⁻)**：用**黄色**。
    *   **氢离子 (H⁺)**：用**浅灰色**。
    *   配色保证在微观图景中有足够的对比度和区分度。

#### 交互功能列表
1.  **模式选择按钮**：“自动教程模式” / “互动实验模式”。
2.  **操作选择按钮**（在互动模式下）：“正确操作：酸入水” / “危险操作：水入酸”。
3.  **动画控制按钮**：播放、暂停、重置（回到初始状态）。
4.  **视角切换按钮/热区**：“宏观视角” / “微观视角”（或在关键帧自动提示点击切换）。
5.  **悬停提示**：鼠标悬停在化学分子模型、烧杯、按钮上时，显示简要的科学说明或操作提示。
6.  **步骤指示器**：在教程模式中，显示当前步骤（如：步骤1/4：取用浓硫酸）。
7.  **安全警示弹出**：在展示错误操作后果时，伴随一个醒目的安全警告文本框。
8.  **结论总结面板**：动画结束后，自动或手动触发一个总结面板，用图文并茂的方式重申“酸入水，沿器壁，慢慢倒，不断搅”的操作要点和原理。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>浓硫酸稀释安全实验 - 微观与宏观演示</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8ed 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
            color: #333;
        }
        
        .header {
            text-align: center;
            margin-bottom: 25px;
            width: 100%;
            max-width: 900px;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            width: 100%;
            max-width: 900px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            margin-bottom: 20px;
        }
        
        .mode-selector {
            display: flex;
            background-color: #f8f9fa;
            padding: 15px;
            border-bottom: 1px solid #eaeaea;
        }
        
        .mode-btn {
            flex: 1;
            padding: 12px;
            margin: 0 5px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .mode-btn.active {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .tutorial-btn {
            background-color: #3498db;
            color: white;
        }
        
        .interactive-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .animation-area {
            position: relative;
            height: 450px;
            background-color: #f0f2f5;
            overflow: hidden;
        }
        
        #animationCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .controls {
            display: flex;
            padding: 15px;
            background-color: #f8f9fa;
            border-top: 1px solid #eaeaea;
            justify-content: space-between;
            align-items: center;
        }
        
        .operation-buttons {
            display: flex;
            gap: 10px;
        }
        
        .control-btn {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            font-size: 0.95rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
        }
        
        .control-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .correct-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .danger-btn {
            background-color: #e74c3c;
            color: white;
        }
        
        .neutral-btn {
            background-color: #95a5a6;
            color: white;
        }
        
        .view-toggle {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .view-btn {
            padding: 8px 15px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.9rem;
        }
        
        .info-panel {
            padding: 20px;
            background-color: white;
            border-top: 1px solid #eaeaea;
        }
        
        .step-indicator {
            font-size: 1.1rem;
            font-weight: 600;
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .explanation {
            font-size: 1rem;
            line-height: 1.5;
            color: #555;
        }
        
        .warning {
            background-color: #fff8e1;
            border-left: 4px solid #ffc107;
            padding: 12px;
            margin-top: 15px;
            border-radius: 0 4px 4px 0;
        }
        
        .warning strong {
            color: #e74c3c;
        }
        
        .conclusion {
            background-color: #e8f5e9;
            border-left: 4px solid #4caf50;
            padding: 15px;
            margin-top: 15px;
            border-radius: 0 4px 4px 0;
            display: none;
        }
        
        .conclusion.show {
            display: block;
        }
        
        .conclusion h3 {
            color: #2e7d32;
            margin-bottom: 8px;
        }
        
        .conclusion p {
            color: #388e3c;
        }
        
        .footer {
            text-align: center;
            color: #7f8c8d;
            font-size: 0.9rem;
            margin-top: 10px;
            max-width: 900px;
        }
        
        .highlight {
            color: #e74c3c;
            font-weight: bold;
        }
        
        .safe-highlight {
            color: #2ecc71;
            font-weight: bold;
        }
        
        .microscopic-hint {
            position: absolute;
            top: 20px;
            right: 20px;
            background-color: rgba(52, 152, 219, 0.9);
            color: white;
            padding: 8px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            display: none;
            z-index: 10;
        }
        
        @media (max-width: 768px) {
            .controls {
                flex-direction: column;
                gap: 15px;
            }
            
            .operation-buttons {
                width: 100%;
                justify-content: center;
            }
            
            .animation-area {
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>浓硫酸稀释安全实验</h1>
        <p class="subtitle">微观与宏观视角演示 - 理解"酸入水"原理与"水入酸"危险</p>
    </div>
    
    <div class="container">
        <div class="mode-selector">
            <button id="tutorialMode" class="mode-btn tutorial-btn active">观看教程模式</button>
            <button id="interactiveMode" class="mode-btn interactive-btn">自主操作模式</button>
        </div>
        
        <div class="animation-area">
            <canvas id="animationCanvas"></canvas>
            <div id="microscopicHint" class="microscopic-hint">
                微观视角已激活！悬停分子查看详情
            </div>
        </div>
        
        <div class="controls">
            <div class="operation-buttons">
                <button id="correctOperation" class="control-btn correct-btn">正确操作：酸入水</button>
                <button id="dangerOperation" class="control-btn danger-btn">危险操作：水入酸</button>
                <button id="resetBtn" class="control-btn neutral-btn">重置实验</button>
            </div>
            
            <div class="view-toggle">
                <span>视角:</span>
                <button id="macroView" class="view-btn active">宏观视角</button>
                <button id="microView" class="view-btn">微观视角</button>
            </div>
        </div>
        
        <div class="info-panel">
            <div class="step-indicator" id="stepIndicator">步骤 1/5: 准备实验器材</div>
            <div class="explanation" id="explanation">
                本实验将演示浓硫酸稀释的正确与错误操作方法。浓硫酸密度约为1.84 g/cm³，远大于水，且稀释过程会释放大量热量。
            </div>
            <div class="warning" id="warning" style="display: none;">
                <strong>危险警告：</strong>浓硫酸具有强腐蚀性，实际实验必须在教师指导下进行，严格遵守"酸入水，沿器壁，慢慢倒，不断搅"的原则！
            </div>
            <div class="conclusion" id="conclusion">
                <h3>实验结论</h3>
                <p>浓硫酸稀释必须遵循"<span class="safe-highlight">酸入水</span>"原则：将浓硫酸沿容器壁缓慢倒入水中，并不断搅拌散热。</p>
                <p>绝对禁止"<span class="highlight">水入酸</span>"：水密度小浮于浓硫酸表面，局部剧烈放热使水瞬间沸腾，导致酸液喷溅，造成严重危险！</p>
            </div>
        </div>
    </div>
    
    <div class="footer">
        <p>化学安全实验模拟 | 教育技术演示 | 注意：此为模拟动画，实际实验需严格遵守安全规程</p>
    </div>

    <script>
        // 获取DOM元素
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        const tutorialModeBtn = document.getElementById('tutorialMode');
        const interactiveModeBtn = document.getElementById('interactiveMode');
        const correctOperationBtn = document.getElementById('correctOperation');
        const dangerOperationBtn = document.getElementById('dangerOperation');
        const resetBtn = document.getElementById('resetBtn');
        const macroViewBtn = document.getElementById('macroView');
        const microViewBtn = document.getElementById('microView');
        const stepIndicator = document.getElementById('stepIndicator');
        const explanation = document.getElementById('explanation');
        const warning = document.getElementById('warning');
        const conclusion = document.getElementById('conclusion');
        const microscopicHint = document.getElementById('microscopicHint');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
        }
        
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();
        
        // 实验状态变量
        let currentMode = 'tutorial'; // 'tutorial' 或 'interactive'
        let currentView = 'macro'; // 'macro' 或 'micro'
        let experimentState = 'idle'; // 'idle', 'correct', 'danger', 'showingMicro'
        let tutorialStep = 0;
        let tutorialSteps = 5;
        let animationFrameId = null;
        let isPaused = false;
        
        // 颜色定义
        const colors = {
            labTable: '#a1887f',
            beaker: 'rgba(255, 255, 255, 0.8)',
            water: 'rgba(173, 216, 230, 0.7)',
            concentratedAcid: 'rgba(46, 125, 50, 0.9)',
            dilutedAcid: 'rgba(102, 187, 106, 0.7)',
            heat: 'rgba(255, 87, 34, 0.8)',
            danger: '#e74c3c',
            safe: '#2ecc71',
            text: '#2c3e50',
            moleculeO: '#3498db', // 氧原子 - 蓝色
            moleculeH: '#ecf0f1', // 氢原子 - 白色
            moleculeSO4: '#f1c40f', // 硫酸根 - 黄色
            moleculeHplus: '#bdc3c7' // 氢离子 - 灰色
        };
        
        // 实验对象
        const lab = {
            tableHeight: canvas.height * 0.7,
            beaker: {
                x: canvas.width / 2,
                y: canvas.height * 0.6,
                width: 180,
                height: 220,
                neckWidth: 120,
                neckHeight: 40
            },
            water: {
                level: 0.6, // 初始水位比例
                color: colors.water
            },
            acid: {
                level: 0, // 初始酸位比例
                color: colors.concentratedAcid,
                droplets: [],
                temperature: 20 // 摄氏度
            },
            heatWaves: [],
            splashParticles: [],
            molecules: []
        };
        
        // 初始化分子
        function initMolecules() {
            lab.molecules = [];
            const moleculeCount = 40;
            const beaker = lab.beaker;
            
            // 水分子
            for (let i = 0; i < moleculeCount * 0.7; i++) {
                lab.molecules.push({
                    type: 'H2O',
                    x: beaker.x - beaker.width/2 + 20 + Math.random() * (beaker.width - 40),
                    y: beaker.y - beaker.height/2 + 20 + Math.random() * (beaker.height * lab.water.level - 40),
                    vx: (Math.random() - 0.5) * 0.5,
                    vy: (Math.random() - 0.5) * 0.5,
                    size: 8,
                    atoms: [
                        {type: 'O', x: 0, y: 0, color: colors.moleculeO},
                        {type: 'H', x: -6, y: -6, color: colors.moleculeH},
                        {type: 'H', x: 6, y: -6, color: colors.moleculeH}
                    ],
                    hover: false
                });
            }
            
            // 硫酸分子 (在正确操作时从顶部加入)
            for (let i = 0; i < moleculeCount * 0.3; i++) {
                lab.molecules.push({
                    type: 'H2SO4',
                    x: beaker.x - beaker.width/2 + 20 + Math.random() * (beaker.width - 40),
                    y: beaker.y - beaker.height/2 - 30, // 起始在烧杯上方
                    vx: 0,
                    vy: 0,
                    size: 12,
                    atoms: [
                        {type: 'S', x: 0, y: 0, color: colors.moleculeSO4},
                        {type: 'O', x: -10, y: -5, color: colors.moleculeO},
                        {type: 'O', x: 10, y: -5, color: colors.moleculeO},
                        {type: 'O', x: -5, y: 10, color: colors.moleculeO},
                        {type: 'O', x: 5, y: 10, color: colors.moleculeO},
                        {type: 'H', x: -12, y: 8, color: colors.moleculeHplus},
                        {type: 'H', x: 12, y: 8, color: colors.moleculeHplus}
                    ],
                    hover: false,
                    dissolving: false,
                    dissolveProgress: 0
                });
            }
        }
        
        // 绘制实验室场景
        function drawLab() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制实验台
            ctx.fillStyle = colors.labTable;
            ctx.fillRect(0, lab.tableHeight, canvas.width, canvas.height - lab.tableHeight);
            
            // 绘制烧杯
            const beaker = lab.beaker;
            ctx.fillStyle = colors.beaker;
            ctx.strokeStyle = '#ccc';
            ctx.lineWidth = 2;
            
            // 烧杯底部
            ctx.beginPath();
            ctx.ellipse(beaker.x, beaker.y + beaker.height/2 - beaker.neckHeight/2, 
                       beaker.width/2, beaker.height/20, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.stroke();
            
            // 烧杯主体
            ctx.beginPath();
            ctx.moveTo(beaker.x - beaker.width/2, beaker.y - beaker.height/2 + beaker.neckHeight);
            ctx.lineTo(beaker.x - beaker.neckWidth/2, beaker.y - beaker.height/2);
            ctx.lineTo(beaker.x + beaker.neckWidth/2, beaker.y - beaker.height/2);
            ctx.lineTo(beaker.x + beaker.width/2, beaker.y - beaker.height/2 + beaker.neckHeight);
            ctx.lineTo(beaker.x + beaker.width/2, beaker.y + beaker.height/2 - beaker.neckHeight/2);
            ctx.lineTo(beaker.x - beaker.width/2, beaker.y + beaker.height/2 - beaker.neckHeight/2);
            ctx.closePath();
            ctx.fill();
            ctx.stroke();
            
            // 绘制液体
            const liquidTop = beaker.y + beaker.height/2 - beaker.neckHeight/2 - (lab.water.level + lab.acid.level) * (beaker.height - beaker.neckHeight);
            
            // 绘制水
            if (lab.water.level > 0) {
                ctx.fillStyle = lab.water.color;
                ctx.beginPath();
                ctx.moveTo(beaker.x - beaker.width/2, beaker.y + beaker.height/2 - beaker.neckHeight/2);
                ctx.lineTo(beaker.x - beaker.width/2, liquidTop + lab.acid.level * (beaker.height - beaker.neckHeight));
                
                // 计算侧边位置
                const leftX = beaker.x - beaker.width/2 + (beaker.width - beaker.neckWidth) * 
                             (1 - (liquidTop + lab.acid.level * (beaker.height - beaker.neckHeight) - (beaker.y - beaker.height/2)) / (beaker.height - beaker.neckHeight)) / 2;
                const rightX = beaker.x + beaker.width/2 - (beaker.width - beaker.neckWidth) * 
                              (1 - (liquidTop + lab.acid.level * (beaker.height - beaker.neckHeight) - (beaker.y - beaker.height/2)) / (beaker.height - beaker.neckHeight)) / 2;
                
                ctx.lineTo(leftX, liquidTop + lab.acid.level * (beaker.height - beaker.neckHeight));
                ctx.lineTo(beaker.x, liquidTop + lab.acid.level * (beaker.height - beaker.neckHeight) - 5);
                ctx.lineTo(rightX, liquidTop + lab.acid.level * (beaker.height - beaker.neckHeight));
                ctx.lineTo(beaker.x + beaker.width/2, liquidTop + lab.acid.level * (beaker.height - beaker.neckHeight));
                ctx.lineTo(beaker.x + beaker.width/2, beaker.y + beaker.height/2 - beaker.neckHeight/2);
                ctx.closePath();
                ctx.fill();
            }
            
            // 绘制浓硫酸 (在水的下层)
            if (lab.acid.level > 0) {
                const acidTop = liquidTop + lab.acid.level * (beaker.height - beaker.neckHeight);
                ctx.fillStyle = lab.acid.color;
                ctx.beginPath();
                ctx.moveTo(beaker.x - beaker.width/2, beaker.y + beaker.height/2 - beaker.neckHeight/2);
                ctx.lineTo(beaker.x - beaker.width/2, acidTop);
                
                // 计算侧边位置
                const leftX = beaker.x - beaker.width/2 + (beaker.width - beaker.neckWidth) * 
                             (1 - (acidTop - (beaker.y - beaker.height/2)) / (beaker.height - beaker.neckHeight)) / 2;
                const rightX = beaker.x + beaker.width/2 - (beaker.width - beaker.neckWidth) * 
                              (1 - (acidTop - (beaker.y - beaker.height/2)) / (beaker.height - beaker.neckHeight)) / 2;
                
                ctx.lineTo(leftX, acidTop);
                ctx.lineTo(beaker.x, acidTop - 5);
                ctx.lineTo(rightX, acidTop);
                ctx.lineTo(beaker.x + beaker.width/2, acidTop);
                ctx.lineTo(beaker.x + beaker.width/2, beaker.y + beaker.height/2 - beaker.neckHeight/2);
                ctx.closePath();
                ctx.fill();
            }
            
            // 绘制热浪效果
            if (lab.heatWaves.length > 0) {
                lab.heatWaves.forEach((wave, index) => {
                    ctx.beginPath();
                    ctx.arc(beaker.x, beaker.y + beaker.height/2 - beaker.neckHeight/2 - 50, 
                           wave.radius, 0, Math.PI * 2);
                    ctx.strokeStyle = `rgba(255, ${87 + wave.age * 5}, ${34 + wave.age * 10}, ${0.8 - wave.age * 0.1})`;
                    ctx.lineWidth = 3;
                    ctx.stroke();
                    
                    // 更新热浪
                    wave.radius += 2;
                    wave.age += 0.05;
                    
                    // 移除旧的热浪
                    if (wave.age > 8) {
                        lab.heatWaves.splice(index, 1);
                    }
                });
            }
            
            // 绘制喷溅粒子
            if (lab.splashParticles.length > 0) {
                lab.splashParticles.forEach((particle, index) => {
                    ctx.fillStyle = particle.color;
                    ctx.beginPath();
                    ctx.arc(particle.x, particle.y, particle.size, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 更新粒子
                    particle.x += particle.vx;
                    particle.y += particle.vy;
                    particle.vy += 0.1; // 重力
                    particle.size *= 0.98; // 逐渐缩小
                    
                    // 移除太小的粒子
                    if (particle.size < 0.5 || particle.y > canvas.height + 10) {
                        lab.splashParticles.splice(index, 1);
                    }
                });
            }
            
            // 绘制酸滴 (在错误操作时)
            if (lab.acid.droplets.length > 0) {
                lab.acid.droplets.forEach((droplet, index) => {
                    ctx.fillStyle = lab.acid.color;
                    ctx.beginPath();
                    ctx.arc(droplet.x, droplet.y, droplet.size, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 更新酸滴
                    droplet.y += droplet.vy;
                    
                    // 如果酸滴到达水面
                    if (droplet.y >= liquidTop + lab.acid.level * (beaker.height - beaker.neckHeight)) {
                        // 创建热浪
                        lab.heatWaves.push({
                            x: droplet.x,
                            y: droplet.y,
                            radius: 5,
                            age: 0
                        });
                        
                        // 创建喷溅粒子
                        if (experimentState === 'danger') {
                            for (let i = 0; i < 15; i++) {
                                lab.splashParticles.push({
                                    x: droplet.x,
                                    y: droplet.y,
                                    vx: (Math.random() - 0.5) * 8,
                                    vy: -Math.random() * 10 - 5,
                                    size: Math.random() * 5 + 2,
                                    color: i < 5 ? lab.acid.color : lab.water.color
                                });
                            }
                        }
                        
                        // 移除酸滴
                        lab.acid.droplets.splice(index, 1);
                        
                        // 增加酸液位
                        lab.acid.level += 0.005;
                    }
                });
            }
            
            // 绘制分子 (微观视角)
            if (currentView === 'micro' && lab.molecules.length > 0) {
                drawMolecules();
            }
            
            // 绘制温度指示
            if (lab.acid.temperature > 30) {
                ctx.fillStyle = colors.heat;
                ctx.font = 'bold 16px Arial';
                ctx.fillText(`温度: ${Math.min(150, Math.round(lab.acid.temperature))}°C`, beaker.x - 40, beaker.y - beaker.height/2 - 20);
                
                // 绘制温度计
                ctx.fillStyle = '#e74c3c';
                ctx.fillRect(beaker.x + beaker.width/2 + 10, beaker.y - beaker.height/2, 10, beaker.height);
                ctx.fillStyle = colors.heat;
                const tempHeight = Math.min(beaker.height, (lab.acid.temperature - 20) / 130 * beaker.height);
                ctx.fillRect(beaker.x + beaker.width/2 + 10, beaker.y - beaker.height/2 + beaker.height - tempHeight, 10, tempHeight);
            }
            
            // 绘制操作提示
            if (experimentState === 'idle') {
                ctx.fillStyle = colors.text;
                ctx.font = '18px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('选择一种操作模式开始实验', canvas.width/2, 50);
            }
        }
        
        // 绘制分子
        function drawMolecules() {
            lab.molecules.forEach(molecule => {
                // 绘制分子中的原子
                molecule.atoms.forEach(atom => {
                    ctx.fillStyle = atom.color;
                    ctx.beginPath();
                    ctx.arc(molecule.x + atom.x, molecule.y + atom.y, molecule.type === 'H2SO4' ? 4 : 3, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 绘制原子标签 (悬停时)
                    if (molecule.hover) {
                        ctx.fillStyle = '#2c3e50';
                        ctx.font = '10px Arial';
                        ctx.fillText(atom.type, molecule.x + atom.x - 5, molecule.y + atom.y - 8);
                    }
                });
                
                // 绘制分子键
                ctx.strokeStyle = 'rgba(255, 255, 255, 0.6)';
                ctx.lineWidth = 1;
                
                if (molecule.type === 'H2O') {
                    // H-O-H 键
                    ctx.beginPath();
                    ctx.moveTo(molecule.x + molecule.atoms[1].x, molecule.y + molecule.atoms[1].y);
                    ctx.lineTo(molecule.x, molecule.y);
                    ctx.lineTo(molecule.x + molecule.atoms[2].x, molecule.y + molecule.atoms[2].y);
                    ctx.stroke();
                } else if (molecule.type === 'H2SO4') {
                    // S-O 键
                    for (let i = 1; i <= 4; i++) {
                        ctx.beginPath();
                        ctx.moveTo(molecule.x, molecule.y);
                        ctx.lineTo(molecule.x + molecule.atoms[i].x, molecule.y + molecule.atoms[i].y);
                        ctx.stroke();
                    }
                    
                    // O-H 键 (如果正在溶解)
                    if (molecule.dissolving) {
                        ctx.beginPath();
                        ctx.moveTo(molecule.x + molecule.atoms[1].x, molecule.y + molecule.atoms[1].y);
                        ctx.lineTo(molecule.x + molecule.atoms[5].x, molecule.y + molecule.atoms[5].y);
                        ctx.stroke();
                        
                        ctx.beginPath();
                        ctx.moveTo(molecule.x + molecule.atoms[2].x, molecule.y + molecule.atoms[2].y);
                        ctx.lineTo(molecule.x + molecule.atoms[6].x, molecule.y + molecule.atoms[6].y);
                        ctx.stroke();
                        
                        // 绘制溶解效果
                        if (molecule.dissolveProgress > 0) {
                            // 绘制分离的H+离子
                            ctx.fillStyle = colors.moleculeHplus;
                            ctx.beginPath();
                            ctx.arc(
                                molecule.x + molecule.atoms[5].x + molecule.dissolveProgress * 20, 
                                molecule.y + molecule.atoms[5].y - molecule.dissolveProgress * 10, 
                                3, 0, Math.PI * 2
                            );
                            ctx.fill();
                            
                            ctx.beginPath();
                            ctx.arc(
                                molecule.x + molecule.atoms[6].x - molecule.dissolveProgress * 20, 
                                molecule.y + molecule.atoms[6].y - molecule.dissolveProgress * 10, 
                                3, 0, Math.PI * 2
                            );
                            ctx.fill();
                            
                            // 绘制热量释放效果
                            ctx.fillStyle = `rgba(255, 87, 34, ${0.7 * molecule.dissolveProgress})`;
                            ctx.beginPath();
                            ctx.arc(molecule.x, molecule.y, 5 + molecule.dissolveProgress * 10, 0, Math.PI * 2);
                            ctx.fill();
                        }
                    }
                }
                
                // 绘制分子标签 (悬停时)
                if (molecule.hover) {
                    ctx.fillStyle = '#2c3e50';
                    ctx.font = 'bold 12px Arial';
                    ctx.fillText(molecule.type, molecule.x - 15, molecule.y - 15);
                    
                    // 显示分子描述
                    let description = '';
                    if (molecule.type === 'H2O') {
                        description = '水分子';
                    } else if (molecule.type === 'H2SO4') {
                        description = '硫酸分子，溶解时电离出H⁺和SO₄²⁻，释放大量热';
                    }
                    
                    ctx.font = '10px Arial';
                    ctx.fillText(description, molecule.x - 40, molecule.y - 25);
                }
            });
        }
        
        // 更新分子运动
        function updateMolecules() {
            const beaker = lab.beaker;
            const liquidTop = beaker.y + beaker.height/2 - beaker.neckHeight/2 - (lab.water.level + lab.acid.level) * (beaker.height - beaker.neckHeight);
            
            lab.molecules.forEach(molecule => {
                // 更新位置
                molecule.x += molecule.vx;
                molecule.y += molecule.vy;
                
                // 限制分子在烧杯内
                const leftBound = beaker.x - beaker.width/2 + 15;
                const rightBound = beaker.x + beaker.width/2 - 15;
                const topBound = liquidTop + 10;
                const bottomBound = beaker.y + beaker.height/2 - beaker.neckHeight/2 - 10;
                
                if (molecule.x < leftBound || molecule.x > rightBound) {
                    molecule.vx *= -0.8;
                    molecule.x = Math.max(leftBound, Math.min(rightBound, molecule.x));
                }
                
                if (molecule.y < topBound || molecule.y > bottomBound) {
                    molecule.vy *= -0.8;
                    molecule.y = Math.max(topBound, Math.min(bottomBound, molecule.y));
                }
                
                // 硫酸分子溶解过程
                if (molecule.type === 'H2SO4' && molecule.dissolving) {
                    molecule.dissolveProgress += 0.02;
                    
                    // 溶解完成后转化为离子
                    if (molecule.dissolveProgress > 1) {
                        molecule.type = 'ions';
                        // 增加温度
                        lab.acid.temperature += 2;
                        
                        // 创建热浪
                        if (Math.random() < 0.3) {
                            lab.heatWaves.push({
                                x: molecule.x,
                                y: molecule.y,
                                radius: 5,
                                age: 0
                            });
                        }
                    }
                }
                
                // 随机运动
                molecule.vx += (Math.random() - 0.5) * 0.1;
                molecule.vy += (Math.random() - 0.5) * 0.1;
                
                // 限制速度
                const maxSpeed = molecule.type === 'H2SO4' ? 0.8 : 1.2;
                const speed = Math.sqrt(molecule.vx * molecule.vx + molecule.vy * molecule.vy);
                if (speed > maxSpeed) {
                    molecule.vx = (molecule.vx / speed) * maxSpeed;
                    molecule.vy = (molecule.vy / speed) * maxSpeed;
                }
                
                // 温度影响运动速度
                if (lab.acid.temperature > 50) {
                    molecule.vx *= 1.05;
                    molecule.vy *= 1.05;
                }
            });
        }
        
        // 检查分子悬停
        function checkMoleculeHover(mouseX, mouseY) {
            let hovered = false;
            
            lab.molecules.forEach(molecule => {
                const distance = Math.sqrt(
                    Math.pow(mouseX - molecule.x, 2) + 
                    Math.pow(mouseY - molecule.y, 2)
                );
                
                molecule.hover = distance < (molecule.type === 'H2SO4' ? 20 : 15);
                if (molecule.hover) hovered = true;
            });
            
            // 显示微观视角提示
            if (currentView === 'micro' && hovered) {
                microscopicHint.style.display = 'block';
            } else {
                microscopicHint.style.display = 'none';
            }
        }
        
        // 正确操作：酸入水
        function performCorrectOperation() {
            if (experimentState !== 'idle' && currentMode === 'interactive') return;
            
            experimentState = 'correct';
            tutorialStep = 1;
            updateStepIndicator();
            
            // 重置状态
            lab.water.level = 0.6;
            lab.acid.level = 0;
            lab.acid.temperature = 20;
            lab.acid.droplets = [];
            lab.heatWaves = [];
            lab.splashParticles = [];
            initMolecules();
            
            // 开始添加酸滴
            const beaker = lab.beaker;
            const addAcidDroplet = () => {
                if (lab.acid.level < 0.2 && experimentState === 'correct') {
                    lab.acid.droplets.push({
                        x: beaker.x + (Math.random() - 0.5) * 30,
                        y: beaker.y - beaker.height/2 - 20,
                        size: 8,
                        vy: 2
                    });
                    
                    // 继续添加酸滴，直到达到一定量
                    setTimeout(addAcidDroplet, 300);
                } else if (lab.acid.level >= 0.2) {
                    // 完成正确操作
                    setTimeout(() => {
                        explanation.innerHTML = `
                            <span class="safe-highlight">正确操作完成！</span> 浓硫酸沿烧杯壁缓慢流入水中，
                            由于浓硫酸密度大，沉入水底，热量随着搅拌和扩散被水吸收，温度缓慢上升，安全完成稀释。
                        `;
                        conclusion.classList.add('show');
                    }, 1000);
                }
            };
            
            explanation.innerHTML = `
                正在执行<span class="safe-highlight">正确操作：酸入水</span>...
                浓硫酸密度(1.84 g/cm³)大于水，滴入后会沉入底部，热量逐渐释放并被大量水吸收。
            `;
            warning.style.display = 'none';
            conclusion.classList.remove('show');
            
            // 开始添加酸滴
            setTimeout(addAcidDroplet, 500);
        }
        
        // 危险操作：水入酸
        function performDangerOperation() {
            if (experimentState !== 'idle
<!--检测到代码截断，自动续写中...-->
&& currentMode === 'interactive') return;
            
            experimentState = 'danger';
            tutorialStep = 1;
            updateStepIndicator();
            
            // 重置状态
            lab.water.level = 0;
            lab.acid.level = 0.6;
            lab.acid.temperature = 20;
            lab.acid.droplets = [];
            lab.heatWaves = [];
            lab.splashParticles = [];
            initMolecules();
            
            // 设置硫酸分子在烧杯底部
            lab.molecules.forEach(molecule => {
                if (molecule.type === 'H2SO4') {
                    molecule.y = lab.beaker.y + lab.beaker.height/2 - lab.beaker.neckHeight/2 - 30;
                    molecule.dissolving = false;
                    molecule.dissolveProgress = 0;
                }
            });
            
            explanation.innerHTML = `
                正在执行<span class="highlight">危险操作：水入酸</span>...
                水密度小于浓硫酸，将浮在浓硫酸表面，导致局部剧烈放热。
            `;
            warning.style.display = 'block';
            conclusion.classList.remove('show');
            
            // 开始添加水滴
            const beaker = lab.beaker;
            let waterDropletsAdded = 0;
            const maxDroplets = 15;
            
            const addWaterDroplet = () => {
                if (waterDropletsAdded < maxDroplets && experimentState === 'danger') {
                    // 创建水滴
                    lab.acid.droplets.push({
                        x: beaker.x + (Math.random() - 0.5) * 30,
                        y: beaker.y - beaker.height/2 - 20,
                        size: 6,
                        vy: 2,
                        isWater: true
                    });
                    
                    waterDropletsAdded++;
                    
                    // 继续添加水滴
                    setTimeout(addWaterDroplet, 200);
                } else if (waterDropletsAdded >= maxDroplets) {
                    // 触发剧烈反应
                    setTimeout(triggerViolentReaction, 500);
                }
            };
            
            // 触发剧烈反应
            const triggerViolentReaction = () => {
                explanation.innerHTML = `
                    <span class="highlight">危险！</span> 水浮在浓硫酸表面，局部剧烈放热使水瞬间沸腾汽化，
                    产生大量水蒸气，体积急剧膨胀，导致酸液喷溅！
                `;
                
                // 大幅增加温度
                lab.acid.temperature = 120;
                
                // 创建大量热浪
                for (let i = 0; i < 10; i++) {
                    setTimeout(() => {
                        lab.heatWaves.push({
                            x: beaker.x + (Math.random() - 0.5) * 50,
                            y: beaker.y - beaker.height/4,
                            radius: 5,
                            age: 0
                        });
                    }, i * 100);
                }
                
                // 创建喷溅效果
                setTimeout(() => {
                    for (let i = 0; i < 80; i++) {
                        lab.splashParticles.push({
                            x: beaker.x + (Math.random() - 0.5) * beaker.width/2,
                            y: beaker.y - beaker.height/4,
                            vx: (Math.random() - 0.5) * 15,
                            vy: -Math.random() * 20 - 10,
                            size: Math.random() * 8 + 3,
                            color: i < 30 ? lab.acid.color : lab.water.color
                        });
                    }
                    
                    // 触发分子剧烈运动
                    lab.molecules.forEach(molecule => {
                        molecule.vx = (Math.random() - 0.5) * 8;
                        molecule.vy = -Math.random() * 6 - 2;
                        
                        // 硫酸分子开始溶解
                        if (molecule.type === 'H2SO4') {
                            molecule.dissolving = true;
                        }
                    });
                    
                    // 显示结论
                    setTimeout(() => {
                        conclusion.classList.add('show');
                    }, 2000);
                }, 500);
            };
            
            // 开始添加水滴
            setTimeout(addWaterDroplet, 500);
        }
        
        // 重置实验
        function resetExperiment() {
            experimentState = 'idle';
            tutorialStep = 0;
            
            // 重置实验室状态
            lab.water.level = 0.6;
            lab.acid.level = 0;
            lab.acid.temperature = 20;
            lab.acid.droplets = [];
            lab.heatWaves = [];
            lab.splashParticles = [];
            initMolecules();
            
            // 更新UI
            updateStepIndicator();
            explanation.innerHTML = '实验已重置。请选择一种操作模式开始实验。';
            warning.style.display = 'none';
            conclusion.classList.remove('show');
            microscopicHint.style.display = 'none';
        }
        
        // 更新步骤指示器
        function updateStepIndicator() {
            if (currentMode === 'tutorial') {
                const steps = [
                    '步骤 1/5: 准备实验器材',
                    '步骤 2/5: 取用浓硫酸',
                    '步骤 3/5: 执行操作',
                    '步骤 4/5: 观察反应现象',
                    '步骤 5/5: 实验结论'
                ];
                stepIndicator.textContent = steps[tutorialStep];
            } else {
                stepIndicator.textContent = '自主操作模式';
            }
        }
        
        // 切换视角
        function switchView(view) {
            currentView = view;
            
            if (view === 'macro') {
                macroViewBtn.classList.add('active');
                microViewBtn.classList.remove('active');
                microscopicHint.style.display = 'none';
            } else {
                macroViewBtn.classList.remove('active');
                microViewBtn.classList.add('active');
                
                // 如果是危险操作状态，显示分子溶解过程
                if (experimentState === 'danger') {
                    lab.molecules.forEach(molecule => {
                        if (molecule.type === 'H2SO4') {
                            molecule.dissolving = true;
                        }
                    });
                }
            }
        }
        
        // 教程模式自动演示
        function runTutorial() {
            resetExperiment();
            experimentState = 'tutorial';
            tutorialStep = 0;
            
            const tutorialSequence = [
                {
                    delay: 1000,
                    action: () => {
                        tutorialStep = 1;
                        updateStepIndicator();
                        explanation.innerHTML = '准备烧杯和浓硫酸。注意浓硫酸为粘稠油状液体，具有强腐蚀性。';
                    }
                },
                {
                    delay: 2000,
                    action: () => {
                        tutorialStep = 2;
                        updateStepIndicator();
                        explanation.innerHTML = '取用浓硫酸，准备进行稀释操作。';
                    }
                },
                {
                    delay: 2000,
                    action: () => {
                        tutorialStep = 3;
                        updateStepIndicator();
                        explanation.innerHTML = '首先演示<span class="highlight">危险操作：水入酸</span>，请观察现象。';
                        warning.style.display = 'block';
                    }
                },
                {
                    delay: 1000,
                    action: () => {
                        performDangerOperation();
                    }
                },
                {
                    delay: 6000,
                    action: () => {
                        tutorialStep = 4;
                        updateStepIndicator();
                        explanation.innerHTML = '现在切换到微观视角，观察硫酸分子溶解过程和水分子被拉开（电离）释放热量的现象。';
                        switchView('micro');
                    }
                },
                {
                    delay: 5000,
                    action: () => {
                        tutorialStep = 5;
                        updateStepIndicator();
                        explanation.innerHTML = '现在演示<span class="safe-highlight">正确操作：酸入水</span>，注意观察安全平稳的混合过程。';
                        switchView('macro');
                        resetExperiment();
                        
                        // 短暂延迟后执行正确操作
                        setTimeout(() => {
                            performCorrectOperation();
                        }, 1000);
                    }
                },
                {
                    delay: 7000,
                    action: () => {
                        explanation.innerHTML = '实验完成。正确操作下，浓硫酸安全稀释，温度缓慢上升，无喷溅危险。';
                        conclusion.classList.add('show');
                    }
                }
            ];
            
            let totalDelay = 0;
            tutorialSequence.forEach(step => {
                totalDelay += step.delay;
                setTimeout(step.action, totalDelay);
            });
        }
        
        // 动画循环
        function animate() {
            drawLab();
            
            // 更新分子运动（微观视角）
            if (currentView === 'micro') {
                updateMolecules();
            }
            
            // 更新温度（缓慢下降）
            if (lab.acid.temperature > 20) {
                lab.acid.temperature *= 0.995;
            }
            
            // 继续动画循环
            animationFrameId = requestAnimationFrame(animate);
        }
        
        // 事件监听器
        tutorialModeBtn.addEventListener('click', () => {
            currentMode = 'tutorial';
            tutorialModeBtn.classList.add('active');
            interactiveModeBtn.classList.remove('active');
            runTutorial();
        });
        
        interactiveModeBtn.addEventListener('click', () => {
            currentMode = 'interactive';
            interactiveModeBtn.classList.add('active');
            tutorialModeBtn.classList.remove('active');
            resetExperiment();
            explanation.innerHTML = '自主操作模式已激活。请选择一种操作方式开始实验。';
        });
        
        correctOperationBtn.addEventListener('click', performCorrectOperation);
        dangerOperationBtn.addEventListener('click', performDangerOperation);
        resetBtn.addEventListener('click', resetExperiment);
        
        macroViewBtn.addEventListener('click', () => switchView('macro'));
        microViewBtn.addEventListener('click', () => switchView('micro'));
        
        // 鼠标移动事件（用于分子悬停检测）
        canvas.addEventListener('mousemove', (e) => {
            const rect = canvas.getBoundingClientRect();
            const mouseX = e.clientX - rect.left;
            const mouseY = e.clientY - rect.top;
            
            if (currentView === 'micro') {
                checkMoleculeHover(mouseX, mouseY);
            }
        });
        
        // 点击事件（用于暂停/继续）
        canvas.addEventListener('click', () => {
            if (currentMode === 'tutorial' && experimentState === 'tutorial') {
                isPaused = !isPaused;
                if (isPaused) {
                    cancelAnimationFrame(animationFrameId);
                    explanation.innerHTML += ' <strong>(动画已暂停，点击继续)</strong>';
                } else {
                    animate();
                }
            }
        });
        
        // 初始化
        initMolecules();
        animate();
        runTutorial();
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 《浓硫酸稀释安全实验》交互式教学动画使用指南

### 欢迎使用

欢迎使用《浓硫酸稀释安全实验》交互式教学动画！本动画由专业教育技术团队开发，旨在通过直观、生动的可视化方式，帮助您深入理解浓硫酸稀释的科学原理与安全操作规范。无论您是化学教师、学生还是对化学实验感兴趣的学习者，本工具都将为您提供一次安全、深刻的学习体验。

### 一、功能说明

本动画是一个基于HTML5 Canvas技术的交互式教学工具，包含两种主要学习模式：

1. **观看教程模式**：系统自动引导您完成完整的实验演示，包括错误操作的危险展示和正确操作的对比学习。
2. **自主操作模式**：您可以自由选择实验操作方式，亲身体验不同操作带来的不同结果。

动画支持**宏观**与**微观**双重视角切换，让您既能观察烧杯中的宏观现象，又能深入分子层面理解反应的本质原理。

### 二、主要功能

#### 1. 模式选择
- **观看教程模式**：点击"观看教程模式"按钮，系统将自动播放完整的教学动画，包含解说和分步指导。
- **自主操作模式**：点击"自主操作模式"按钮，您可以自由控制实验进程，选择不同的操作方式。

#### 2. 实验操作
- **正确操作：酸入水**：点击绿色按钮，演示将浓硫酸缓慢加入水中的安全操作过程。
- **危险操作：水入酸**：点击红色按钮，演示将水加入浓硫酸中的危险操作及其严重后果。
- **重置实验**：随时点击灰色按钮，将实验恢复到初始状态。

#### 3. 视角切换
- **宏观视角**：观察烧杯、液体、温度变化和喷溅现象等宏观实验场景。
- **微观视角**：深入分子层面，观察水分子结构、硫酸分子溶解过程、电离现象和热量释放的微观机制。

#### 4. 交互特性
- **分子悬停提示**：在微观视角下，将鼠标悬停在分子模型上，可查看分子类型和特性说明。
- **步骤指示**：教程模式中实时显示当前实验步骤。
- **安全警示**：危险操作时自动显示安全警告信息。
- **实验结论**：实验完成后自动总结核心安全要点。

### 三、设计特色

#### 1. 科学准确性
- 浓硫酸采用深绿色表示，体现其粘稠、不透明的物理特性
- 分子模型基于实际化学结构简化设计，保持科学合理性
- 温度变化、喷溅现象符合实际物理规律

#### 2. 教学可视化
- **热量可视化**：用红色波纹和光点表现放热过程
- **危险可视化**：用粒子系统模拟酸液喷溅的冲击效果
- **微观过程可视化**：展示硫酸分子电离、水分子被拉开的过程

#### 3. 安全设计
- 使用强烈的视觉对比（红/绿）区分危险与安全操作
- 危险操作时自动弹出醒目警告
- 通过震撼但不恐怖的动画效果，建立正确的安全敬畏感

#### 4. 用户体验
- 响应式设计，适配不同屏幕尺寸
- 直观的界面布局和清晰的按钮标识
- 流畅的动画过渡和自然的物理模拟

### 四、教学要点

#### 核心概念
1. **密度差异**：浓硫酸密度（1.84 g/cm³）远大于水，这是"酸入水"操作的基础
2. **放热本质**：硫酸分子在水合过程中，H⁺和SO₄²⁻与水分子强烈作用，释放大量热量
3. **危险机制**：局部热量积聚 → 水瞬间沸腾 → 蒸汽体积急剧膨胀 → 酸液喷溅

#### 认知路径
1. **宏观现象认知**：先观察烧杯中的液体混合、温度上升、喷溅现象
2. **微观本质理解**：切换到微观视角，理解放热的分子机制
3. **对比强化记忆**：并排对比正确与错误操作的截然不同结果
4. **安全规范内化**：通过震撼的视觉体验，深刻记住"酸入水，沿器壁，慢慢倒，不断搅"

#### 教学时机建议
- **新课引入**：在讲解浓硫酸性质前使用，激发学习兴趣
- **难点突破**：在解释稀释原理时使用，化解抽象概念
- **安全教育**：在实验课前使用，强化安全意识
- **复习巩固**：在单元复习时使用，加深理解记忆

### 五、使用建议

#### 教师使用建议
1. **课堂演示**：
   - 使用投影仪全屏展示，配合讲解逐步引导
   - 在关键节点暂停，提出问题引导学生思考
   - 先展示危险操作建立警示，再展示正确操作强化规范

2. **探究学习**：
   - 让学生自主操作，记录观察现象
   - 设计学习任务单，引导学生对比分析
   - 组织小组讨论：为什么"水入酸"会喷溅？

3. **分层教学**：
   - 基础层：重点观察宏观现象，记住操作规范
   - 提高层：理解微观原理，能解释现象背后的科学道理
   - 拓展层：探讨实际实验中还需要哪些安全措施

#### 学生自学建议
1. **首次学习**：建议先使用"观看教程模式"，跟随系统引导完整学习
2. **深入探究**：切换到"自主操作模式"，亲自尝试不同操作，观察差异
3. **微观探索**：务必切换到微观视角，悬停查看分子信息，理解反应本质
4. **总结反思**：实验完成后，仔细阅读结论部分，复述安全操作要点

#### 技术提示
1. **浏览器兼容**：建议使用Chrome、Firefox、Edge等现代浏览器
2. **设备要求**：支持台式机、笔记本电脑、平板电脑
3. **网络环境**：单文件运行，无需网络连接即可使用
4. **性能优化**：如动画卡顿，可尝试关闭其他占用资源的程序

#### 安全提醒
⚠️ **重要提示**：
- 本动画为**教学模拟工具**，不能替代实际实验经验
- 实际操作浓硫酸时，**必须**在专业教师指导下进行
- 必须佩戴防护眼镜、实验服和防护手套
- 实验室必须配备应急冲洗设施
- 如发生意外，立即用大量清水冲洗并寻求医疗帮助

### 结语

本交互式动画融合了教育技术、可视化设计和化学教学的专业知识，旨在创造一个安全、有效、引人入胜的学习环境。我们相信，通过这种直观的学习方式，您不仅能够记住操作规范，更能理解其背后的科学原理，培养严谨的科学态度和安全意识。

祝您学习愉快，探索化学世界的奥秘！

---
**开发团队**：教育技术专家与创意程序员团队  
**版本**：1.0  
**更新日期**：2023年10月  
**教育目标**：促进化学安全教育，培养科学素养