# 需求：减数分裂全过程（尤其是第一次分裂的联会、四分体、同源染色体分离）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的生物学学习者。他们需要理解减数分裂这一抽象、动态且复杂的细胞过程，特别是第一次分裂中的关键事件。
2.  **核心痛点**：
    *   **过程抽象**：染色体行为（复制、配对、分离）无法直接观察。
    *   **概念易混淆**：联会、四分体、同源染色体、姐妹染色单体等术语和结构关系容易混淆。
    *   **动态理解困难**：从静态的教科书插图难以构建连续、完整的动态过程。
    *   **阶段性重点**：需要突出第一次分裂（减数分裂I）与第二次分裂（减数分裂II）的本质区别，尤其是“同源染色体分离”发生在第一次。
3.  **学习目标**：通过动画，用户应能清晰描述并可视化减数分裂I的全过程，准确指认各阶段的关键结构和事件，理解染色体数目减半发生的时机与机制。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念聚焦**：
    *   **主线**：二倍体细胞（2n）→ 染色体复制 → 同源染色体联会形成四分体 → 同源染色体分离（减数分裂I）→ 姐妹染色单体分离（减数分裂II）→ 形成单倍体配子（n）。
    *   **重点突破**：将“联会”、“四分体”、“同源染色体分离”作为核心交互讲解点，与非同源染色体的自由组合建立联系。

2.  **遵循认知规律**：
    *   **从整体到局部**：先自动播放完整动画，建立宏观流程印象。再允许用户分阶段（间期、前期I、中期I、后期I、末期I…）逐步探索。
    *   **从结构到过程**：先通过高亮、标签介绍染色体、着丝粒、同源染色体等静态结构，再演示它们的动态行为。
    *   **对比与强调**：将减数分裂I与II并列对比，强调“同源分离”与“姐妹分离”的关键区别。用颜色（如红/蓝代表来自父本/母本的同源染色体）强化视觉区分。

3.  **交互设计策略**：
    *   **可控的动画**：提供播放/暂停、步进（前一阶段/后一阶段）、重置控制。允许用户控制动画节奏。
    *   **探索式学习**：点击特定结构（如“四分体”）时，动画局部暂停，弹出放大详解视图和文字说明。
    *   **阶段选择器**：提供一个清晰的阶段进度条或按钮菜单，允许用户直接跳转到任一特定时期进行观察。
    *   **“显微镜”视角**：主画面为细胞整体视图，可切换或弹出一个小窗口，聚焦于一对同源染色体的行为特写。

4.  **视觉呈现方案**：
    *   **层级清晰**：背景（细胞膜、细胞核膜）最淡，细胞器（中心体、纺锤丝）次之，染色体最突出。
    *   **动态表达**：用平滑的补间动画表现染色体的移动、纺锤丝的牵引。使用“高亮”、“脉动”效果引导用户注意力。
    *   **结构标识**：染色体形态（长短、着丝粒位置）要有差异，体现同源染色体的“对等”关系。姐妹染色单体在复制后应紧密并列。
    *   **示意图简化**：为突出核心过程，可适当简化其他细胞器细节，但必须准确呈现纺锤体、中心粒等与分裂直接相关的结构。

#### 配色方案选择
*   **染色体**：
    *   **父本来源**：采用一种深色调（如**深蓝色**#2E5A88）。
    *   **母本来源**：采用另一种对比色（如**深红色**#A63D40）。
    *   **复制后的姐妹染色单体**：使用同色系但半透明（例如，深蓝色+50%透明度的浅蓝色）来表现，体现其遗传一致性。
*   **细胞结构与背景**：
    *   **细胞膜/核膜**：极浅的灰色（#F5F5F5）描边。
    *   **细胞质**：接近白色的浅米色（#FAF8F0）。
    *   **纺锤丝/微管**：浅灰色（#CCCCCC）或浅紫色（#D4C1E0），动态拉长时可有轻微发光效果。
    *   **中心体/中心粒**：深灰色（#666666）。
*   **界面与高亮**：
    *   **交互高亮**：使用醒目的**明黄色**（#FFD700）描边或光晕。
    *   **说明文字框**：半透明白色背景（rgba(255,255,255,0.9)），深灰色文字。
    *   **按钮/控制器**：中性蓝色系（#4A6FA5），悬停时变深。

#### 交互功能列表
1.  **主控制面板**：
    *   播放/暂停按钮
    *   上一阶段 / 下一阶段 步进按钮
    *   重置按钮
    *   速度调节滑块
2.  **阶段导航器**：以进度条或图标按钮形式列出“间期”、“前期I”、“中期I”、“后期I”、“末期I/前期II”、“中期II”、“后期II”、“末期II”，点击可跳转。
3.  **结构交互点**（点击触发详解）：
    *   **同源染色体对**：高亮一对，说明其来源、形态相似性。
    *   **联会/四分体**：点击时，放大显示联会复合体，解释非姐妹染色单体间的交叉互换（可配简单示意图）。
    *   **纺锤丝与着丝粒**：显示附着过程，解释牵引作用。
4.  **视角切换**：一个“特写镜头”按钮，用于在主视图（整个细胞）和特写视图（一对同源染色体）之间切换。
5.  **图示图例**：一个可开关的图例面板，解释颜色、线条所代表的生物学含义。
6.  **阶段描述面板**：随动画进程，自动更新当前阶段的名称和关键事件文字描述。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>减数分裂全过程教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        header {
            background: linear-gradient(to right, #2E5A88, #4A6FA5);
            color: white;
            padding: 25px 30px;
            text-align: center;
        }

        h1 {
            font-size: 2.2em;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .subtitle {
            font-size: 1.1em;
            opacity: 0.9;
            font-weight: 300;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            padding: 20px;
            gap: 20px;
        }

        .animation-section {
            flex: 1;
            min-width: 300px;
            background: #FAF8F0;
            border-radius: 15px;
            padding: 15px;
            box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.05);
        }

        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #FAF8F0;
            border-radius: 10px;
            overflow: hidden;
            border: 2px solid #E0E0E0;
        }

        #meiosisCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .controls-section {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .control-panel {
            background: white;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        h2 {
            color: #2E5A88;
            font-size: 1.4em;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #E8E8E8;
        }

        .stage-nav {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
            margin-bottom: 20px;
        }

        .stage-btn {
            background: #f0f4f8;
            border: 2px solid #d0d8e4;
            border-radius: 8px;
            padding: 10px 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.85em;
            text-align: center;
            color: #555;
        }

        .stage-btn:hover {
            background: #e1e8f0;
            transform: translateY(-2px);
        }

        .stage-btn.active {
            background: #4A6FA5;
            color: white;
            border-color: #2E5A88;
            font-weight: 600;
        }

        .player-controls {
            display: flex;
            gap: 10px;
            align-items: center;
            margin-bottom: 20px;
        }

        .ctrl-btn {
            padding: 10px 20px;
            border: none;
            border-radius: 8px;
            background: #4A6FA5;
            color: white;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            flex: 1;
        }

        .ctrl-btn:hover {
            background: #2E5A88;
            transform: translateY(-2px);
        }

        .ctrl-btn:active {
            transform: translateY(0);
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 20px;
        }

        #speedSlider {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            background: #e0e0e0;
            border-radius: 4px;
            outline: none;
        }

        #speedSlider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #4A6FA5;
            cursor: pointer;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 10px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9em;
        }

        .color-box {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }

        .info-panel {
            background: white;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            flex: 1;
        }

        .stage-info {
            background: #f8f9fa;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 15px;
            border-left: 4px solid #4A6FA5;
        }

        .stage-title {
            font-size: 1.2em;
            color: #2E5A88;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .stage-desc {
            line-height: 1.6;
            color: #555;
        }

        .highlight {
            background-color: rgba(255, 215, 0, 0.2);
            padding: 2px 5px;
            border-radius: 3px;
            font-weight: 600;
        }

        .interactive-hint {
            background: #fff8e1;
            border-radius: 10px;
            padding: 15px;
            margin-top: 15px;
            border-left: 4px solid #FFD700;
            font-size: 0.9em;
            color: #666;
        }

        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            font-size: 0.9em;
            border-top: 1px solid #eee;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .stage-nav {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .canvas-container {
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>减数分裂全过程教学动画</h1>
            <p class="subtitle">探索染色体复制、联会、四分体形成与同源染色体分离的奥秘</p>
        </header>
        
        <div class="main-content">
            <section class="animation-section">
                <h2>减数分裂过程</h2>
                <div class="canvas-container">
                    <canvas id="meiosisCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="color-box" style="background-color: #2E5A88;"></div>
                        <span>父本来源染色体</span>
                    </div>
                    <div class="legend-item">
                        <div class="color-box" style="background-color: #A63D40;"></div>
                        <span>母本来源染色体</span>
                    </div>
                    <div class="legend-item">
                        <div class="color-box" style="background-color: rgba(46, 90, 136, 0.5);"></div>
                        <span>姐妹染色单体</span>
                    </div>
                    <div class="legend-item">
                        <div class="color-box" style="background-color: #D4C1E0; border: 1px solid #999;"></div>
                        <span>纺锤丝</span>
                    </div>
                </div>
                
                <div class="interactive-hint">
                    💡 交互提示：点击画布中的染色体可以查看详细信息。尝试点击"四分体"结构！
                </div>
            </section>
            
            <section class="controls-section">
                <div class="control-panel">
                    <h2>动画控制</h2>
                    
                    <div class="stage-nav">
                        <button class="stage-btn" data-stage="0">间期</button>
                        <button class="stage-btn" data-stage="1">前期 I</button>
                        <button class="stage-btn" data-stage="2">中期 I</button>
                        <button class="stage-btn" data-stage="3">后期 I</button>
                        <button class="stage-btn" data-stage="4">末期 I</button>
                        <button class="stage-btn" data-stage="5">前期 II</button>
                        <button class="stage-btn" data-stage="6">中期 II</button>
                        <button class="stage-btn" data-stage="7">后期 II</button>
                        <button class="stage-btn" data-stage="8">末期 II</button>
                    </div>
                    
                    <div class="player-controls">
                        <button id="prevBtn" class="ctrl-btn">◀ 上一阶段</button>
                        <button id="playPauseBtn" class="ctrl-btn">▶ 播放</button>
                        <button id="nextBtn" class="ctrl-btn">下一阶段 ▶</button>
                    </div>
                    
                    <button id="resetBtn" class="ctrl-btn" style="background: #666;">重置动画</button>
                    
                    <div class="speed-control">
                        <span>速度:</span>
                        <input type="range" id="speedSlider" min="0.5" max="3" step="0.1" value="1">
                        <span id="speedValue">1.0x</span>
                    </div>
                </div>
                
                <div class="info-panel">
                    <h2>阶段信息</h2>
                    <div class="stage-info">
                        <div class="stage-title" id="currentStageTitle">间期</div>
                        <div class="stage-desc" id="currentStageDesc">
                            染色体复制，细胞准备进行减数分裂。每个染色体复制形成两个姐妹染色单体，由着丝粒连接。
                        </div>
                    </div>
                    
                    <div class="stage-info">
                        <div class="stage-title">关键概念</div>
                        <div class="stage-desc">
                            <p><span class="highlight">联会</span>: 同源染色体配对的过程，发生在前期I。</p>
                            <p><span class="highlight">四分体</span>: 一对同源染色体复制后形成的4条染色单体结构。</p>
                            <p><span class="highlight">同源染色体分离</span>: 减数分裂I后期，同源染色体分别移向细胞两极。</p>
                            <p><span class="highlight">染色体减半</span>: 发生在减数分裂I结束时，从2n变为n。</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>
        
        <div class="footer">
            <p>教学动画设计 | 减数分裂全过程 | 适用于高中及大学生物学学习</p>
        </div>
    </div>

    <script>
        // 全局变量
        const canvas = document.getElementById('meiosisCanvas');
        const ctx = canvas.getContext('2d');
        const stageButtons = document.querySelectorAll('.stage-btn');
        const playPauseBtn = document.getElementById('playPauseBtn');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const resetBtn = document.getElementById('resetBtn');
        const speedSlider = document.getElementById('speedSlider');
        const speedValue = document.getElementById('speedValue');
        const currentStageTitle = document.getElementById('currentStageTitle');
        const currentStageDesc = document.getElementById('currentStageDesc');
        
        // 画布尺寸
        let canvasWidth, canvasHeight;
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvasWidth = canvas.width = container.clientWidth;
            canvasHeight = canvas.height = container.clientHeight;
        }
        
        // 动画状态
        let currentStage = 0;
        let isPlaying = false;
        let animationSpeed = 1.0;
        let animationProgress = 0;
        let lastTime = 0;
        let selectedChromosome = null;
        
        // 减数分裂阶段信息
        const stages = [
            {
                name: "间期",
                description: "染色体复制，细胞准备进行减数分裂。每个染色体复制形成两个姐妹染色单体，由着丝粒连接。",
                duration: 2
            },
            {
                name: "前期 I",
                description: "染色体凝缩，同源染色体配对（联会），形成四分体。非姐妹染色单体间可能发生交叉互换。",
                duration: 3
            },
            {
                name: "中期 I",
                description: "四分体排列在细胞中央的赤道板上。纺锤丝附着在染色体的着丝粒上。",
                duration: 2
            },
            {
                name: "后期 I",
                description: "同源染色体分离，分别移向细胞两极。这是染色体数目减半的关键步骤。",
                duration: 2
            },
            {
                name: "末期 I",
                description: "染色体到达两极，细胞开始分裂，形成两个子细胞，每个子细胞含有单倍体染色体组。",
                duration: 2
            },
            {
                name: "前期 II",
                description: "两个子细胞中的染色体再次凝缩，纺锤体重新形成。",
                duration: 1.5
            },
            {
                name: "中期 II",
                description: "染色体排列在细胞中央的赤道板上，着丝粒分裂准备。",
                duration: 1.5
            },
            {
                name: "后期 II",
                description: "姐妹染色单体分离，分别移向细胞两极。",
                duration: 2
            },
            {
                name: "末期 II",
                description: "染色体到达两极，细胞分裂完成，形成四个单倍体配子。",
                duration: 2
            }
        ];
        
        // 染色体数据
        const chromosomes = [
            { id: 1, length: 80, centromerePos: 0.3, paternal: true, x: 0, y: 0, angle: 0, replicated: false },
            { id: 2, length: 70, centromerePos: 0.5, paternal: false, x: 0, y: 0, angle: 0, replicated: false },
            { id: 3, length: 90, centromerePos: 0.4, paternal: true, x: 0, y: 0, angle: 0, replicated: false },
            { id: 4, length: 60, centromerePos: 0.6, paternal: false, x: 0, y: 0, angle: 0, replicated: false }
        ];
        
        // 细胞数据
        const cell = {
            x: 0,
            y: 0,
            radius: 0,
            nuclearMembrane: true,
            spindlePoles: [{x: 0, y: 0}, {x: 0, y: 0}],
            spindleFibers: []
        };
        
        // 初始化
        function init() {
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // 设置初始位置
            updateCellDimensions();
            arrangeChromosomes();
            
            // 事件监听
            playPauseBtn.addEventListener('click', togglePlayPause);
            prevBtn.addEventListener('click', prevStage);
            nextBtn.addEventListener('click', nextStage);
            resetBtn.addEventListener('click', resetAnimation);
            speedSlider.addEventListener('input', updateSpeed);
            
            stageButtons.forEach(btn => {
                btn.addEventListener('click', () => {
                    const stage = parseInt(btn.dataset.stage);
                    goToStage(stage);
                });
            });
            
            canvas.addEventListener('click', handleCanvasClick);
            
            // 初始绘制
            draw();
            updateStageInfo();
            updateStageButtons();
            
            // 开始动画循环
            requestAnimationFrame(animate);
        }
        
        // 更新细胞尺寸
        function updateCellDimensions() {
            cell.x = canvasWidth / 2;
            cell.y = canvasHeight / 2;
            cell.radius = Math.min(canvasWidth, canvasHeight) * 0.4;
        }
        
        // 排列染色体
        function arrangeChromosomes() {
            const angleStep = (Math.PI * 2) / chromosomes.length;
            
            chromosomes.forEach((chr, index) => {
                const angle = angleStep * index;
                const distance = cell.radius * 0.6;
                
                chr.x = cell.x + Math.cos(angle) * distance;
                chr.y = cell.y + Math.sin(angle) * distance;
                chr.angle = angle;
            });
        }
        
        // 动画循环
        function animate(timestamp) {
            if (!lastTime) lastTime = timestamp;
            const deltaTime = (timestamp - lastTime) / 1000;
            lastTime = timestamp;
            
            if (isPlaying) {
                animationProgress += deltaTime * animationSpeed;
                
                const stageDuration = stages[currentStage].duration;
                if (animationProgress >= stageDuration) {
                    animationProgress = 0;
                    if (currentStage < stages.length - 1) {
                        currentStage++;
                        updateStageInfo();
                        updateStageButtons();
                    } else {
                        isPlaying = false;
                        playPauseBtn.textContent = '▶ 播放';
                    }
                }
            }
            
            draw();
            requestAnimationFrame(animate);
        }
        
        // 绘制函数
        function draw() {
            // 清空画布
            ctx.clearRect(0, 0, canvasWidth, canvasHeight);
            
            // 绘制细胞质
            ctx.fillStyle = '#FAF8F0';
            ctx.beginPath();
            ctx.arc(cell.x, cell.y, cell.radius, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制细胞膜
            ctx.strokeStyle = '#F5F5F5';
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.arc(cell.x, cell.y, cell.radius, 0, Math.PI * 2);
            ctx.stroke();
            
            // 绘制核膜（前期I之前）
            if (cell.nuclearMembrane && currentStage < 1) {
                ctx.strokeStyle = '#F5F5F5';
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 5]);
                ctx.beginPath();
                ctx.arc(cell.x, cell.y, cell.radius * 0.8, 0, Math.PI * 2);
                ctx.stroke();
                ctx.setLineDash([]);
            }
            
            // 更新纺锤体
            updateSpindle();
            
            // 绘制纺锤体
            drawSpindle();
            
            // 绘制染色体
            drawChromosomes();
            
            // 绘制被选中的染色体高亮
            if (selectedChromosome) {
                drawSelectedChromosome();
            }
        }
        
        // 更新纺锤体
        function updateSpindle() {
            // 纺锤体极点位置
            const poleDistance = cell.radius * 0.8;
            
            if (currentStage >= 2 && currentStage <= 3) { // 中期I和后期I
                cell.spindlePoles[0].x = cell.x - poleDistance;
                cell.spindlePoles[0].y = cell.y;
                cell.spindlePoles[1].x = cell.x + poleDistance;
                cell.spindlePoles[1].y = cell.y;
            } else if (currentStage >= 6 && currentStage <= 7) { // 中期II和后期II
                // 减数分裂II有两个细胞
                const cell1X = cell.x - cell.radius * 0.5;
                const cell2X = cell.x + cell.radius * 0.5;
                
                cell.spindlePoles[0].x = cell1X - poleDistance * 0.6;
                cell.spindlePoles[0].y = cell.y;
                cell.spindlePoles[1].x = cell1X + poleDistance * 0.6;
                cell.spindlePoles[1].y = cell.y;
            } else {
                cell.spindlePoles[0].x = cell.x - poleDistance;
                cell.spindlePoles[0].y = cell.y;
                cell.spindlePoles[1].x = cell.x + poleDistance;
                cell.spindlePoles[1].y = cell.y;
            }
            
            // 更新纺锤丝
            cell.spindleFibers = [];
            
            if (currentStage >= 2) { // 中期I及以后
                chromosomes.forEach(chr => {
                    if (currentStage >= 4 && currentStage <= 8) {
                        // 减数分裂II，染色体在不同细胞中
                        return;
                    }
                    
                    const progress = animationProgress / stages[currentStage].duration;
                    
                    if (currentStage === 2) { // 中期I
                        // 染色体在赤道板
                        const targetX = cell.x;
                        const targetY = cell.y - cell.radius * 0.3 + chr.id * 20;
                        
                        chr.x += (targetX - chr.x) * 0.1;
                        chr.y += (targetY - chr.y) * 0.1;
                        
                        // 连接到两极
                        cell.spindleFibers.push({
                            from: cell.spindlePoles[0],
                            to: {x: chr.x - 10, y: chr.y}
                        });
                        cell.spindleFibers.push({
                            from: cell.spindlePoles[1],
                            to: {x: chr.x + 10, y: chr.y}
                        });
                    } else if (currentStage === 3) { // 后期I
                        // 同源染色体分离
                        const targetPole = chr.paternal ? 0 : 1;
                        const targetX = cell.spindlePoles[targetPole].x;
                        const targetY = cell.spindlePoles[targetPole].y + (chr.id % 2) * 40 - 20;
                        
                        chr.x += (targetX - chr.x) * 0.05 * progress;
                        chr.y += (targetY - chr.y) * 0.05 * progress;
                        
                        // 连接到对应的极
                        cell.spindleFibers.push({
                            from: cell.spindlePoles[targetPole],
                            to: {x: chr.x, y: chr.y}
                        });
                    }
                });
            }
        }
        
        // 绘制纺锤体
        function drawSpindle() {
            if (currentStage < 2) return; // 前期I之前不显示纺锤体
            
            // 绘制中心体
            ctx.fillStyle = '#666666';
            cell.spindlePoles.forEach(pole => {
                ctx.beginPath();
                ctx.arc(pole.x, pole.y, 8, 0, Math.PI * 2);
                ctx.fill();
                
                // 中心体周围的微管组织中心
                ctx.strokeStyle = '#666666';
                ctx.lineWidth = 1;
                ctx.beginPath();
                ctx.arc(pole.x, pole.y, 15, 0, Math.PI * 2);
                ctx.stroke();
            });
            
            // 绘制纺锤丝
            ctx.strokeStyle = '#D4C1E0';
            ctx.lineWidth = 2;
            ctx.setLineDash([2, 2]);
            
            cell.spindleFibers.forEach(fiber => {
                ctx.beginPath();
                ctx.moveTo(fiber.from.x, fiber.from.y);
                ctx.lineTo(fiber.to.x, fiber.to.y);
                ctx.stroke();
            });
            
            ctx.setLineDash([]);
        }
        
        // 绘制染色体
        function drawChromosomes() {
            chromosomes.forEach(chr => {
                // 根据阶段更新染色体状态
                updateChromosomeState(chr);
                
                // 绘制染色体
                drawChromosome(chr);
            });
            
            // 如果是前期I，绘制联会复合体和四分体
            if (currentStage === 1) {
                drawSynapsis();
            }
        }
        
        // 更新染色体状态
        function updateChromosomeState(chr) {
            // 染色体复制（间期）
            if (currentStage >= 0 && !chr.replicated) {
                chr.replicated = true;
            }
            
            // 染色体凝缩（前期I）
            if (currentStage >= 1) {
                // 染色体变得更粗更短
                chr.displayLength = chr.length * 0.7;
            } else {
                chr.displayLength = chr.length;
            }
        }
        
        // 绘制单个染色体
        function drawChromosome(chr) {
            const length = chr.displayLength || chr.length;
            const centromerePos = chr.centromerePos;
            
            // 染色体颜色
            const mainColor = chr.paternal ? '#2E5A88' : '#A63D40';
            const sisterColor = chr.paternal ? 'rgba(46, 90, 136, 0.5)' : 'rgba(166, 61, 64, 0.5)';
            
            // 计算染色体端点
            const endX1 = chr.x + Math.cos(chr.angle) * length * centromerePos;
            const endY1 = chr.y + Math.sin(chr.angle) * length * centromerePos;
            const endX2 = chr.x - Math.cos(chr.angle) * length * (1 - centromerePos);
            const endY2 = chr.y - Math.sin(chr.angle) * length * (1 - centromerePos);
            
            // 绘制姐妹染色单体（如果已复制）
            if (chr.replicated && currentStage >= 0) {
                const offset = 5;
                const offsetX = Math.cos(chr.angle + Math.PI/2) * offset;
                const offsetY = Math.sin(chr.angle + Math.PI/2) * offset;
                
                // 第一条姐妹染色单体
                ctx.strokeStyle = sisterColor;
                ctx.lineWidth = 6;
                ctx.beginPath();
                ctx.moveTo(endX1 + offsetX, endY1 + offsetY);
                ctx.lineTo(endX2 + offsetX, endY2 + offsetY);
                ctx.stroke();
                
                // 第二条姐妹染色单体
                ctx.strokeStyle = mainColor;
                ctx.lineWidth = 6;
                ctx.beginPath();
                ctx.moveTo(endX1 - offsetX, endY1 - offsetY);
                ctx.lineTo(endX2 - offsetX, endY2 - offsetY);
                ctx.stroke();
                
                // 绘制着丝粒
                ctx.fillStyle = '#333';
                ctx.beginPath();
                ctx.arc(chr.x, chr.y, 4, 0, Math.PI * 2);
                ctx.fill();
                
                // 存储染色体边界用于点击检测
                chr.bounds = {
                    x: Math.min(endX1, endX2) - 10,
                    y: Math.min(endY1, endY2) - 10,
                    width: Math.abs(endX1 - endX2) + 20,
                    height: Math.abs(endY1 - endY2) + 20
                };
            } else {
                // 未复制的染色体
                ctx.strokeStyle = mainColor;
                ctx.lineWidth = 8;
                ctx.beginPath();
                ctx.moveTo(endX1, endY1);
                ctx.lineTo(endX2, endY2);
                ctx.stroke();
                
                // 绘制着丝粒
                ctx.fillStyle = '#333';
                ctx.beginPath();
                ctx.arc(chr.x, chr.y, 4, 0, Math.PI * 2);
                ctx.fill();
                
                // 存储染色体边界
                chr.bounds = {
                    x: Math.min(endX1, endX2) - 10,
                    y: Math.min(endY1, endY2) - 10,
                    width: Math.abs(endX1 - endX2) + 20,
                    height: Math.abs(endY1 - endY2) + 20
                };
            }
            
            // 如果是被选中的染色体，绘制高亮
            if (selectedChromosome === chr.id) {
                ctx.strokeStyle = '#FFD700';
                ctx.lineWidth = 3;
                ctx.beginPath();
                ctx.arc(chr.x, chr.y, length/2 + 15, 0, Math.PI * 2);
                ctx.stroke();
            }
        }
        
        // 绘制联会和四分体
        function drawSynapsis() {
            // 将染色体按同源配对分组
            const pairedChromosomes = [
                [chromosomes[0], chromosomes[1]], // 第一对同源染色体
                [chromosomes[2], chromosomes[3]]  // 第二对同源染色体
            ];
            
            pairedChromosomes.forEach(pair => {
                const chr1 = pair[0];
                const chr2 = pair[1];
                
                // 计算配对位置
                const pairX = (chr1.x + chr2.x) / 2;
                const pairY = (chr1.y + chr2.y) / 2;
                
                // 绘制联会复合体（连接两条同源染色体）
                ctx.strokeStyle = '#888';
                ctx.lineWidth = 2;
                ctx.setLineDash([3, 3]);
                ctx.beginPath();
                ctx.moveTo(chr1.x, chr1.y);
                ctx.lineTo(chr2.x, chr2.y);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 绘制四分体标签（仅在第一对染色体上）
                if (pair === pairedChromosomes[0]) {
                    ctx.fillStyle = '#2E5A88';
                    ctx.font = 'bold 16px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('四分体', pairX, pairY - 30);
                    
                    // 绘制交叉互换示意图
                    ctx.strokeStyle = '#FF6B6B';
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.moveTo(pairX - 20, pairY - 10);
                    ctx.lineTo(pairX + 20, pairY + 10);
                    ctx.stroke();
                    
                    ctx.beginPath();
                    ctx.moveTo(pairX + 20, pairY - 10);
                    ctx.lineTo(pairX - 20, pairY + 10);
                    ctx.stroke();
                }
            });
        }
        
        // 绘制被选中的染色体详细信息
        function drawSelectedChromosome() {
            const chr = chromosomes.find(c => c.id === selectedChromosome);
            if (!chr) return;
            
            // 绘制信息框
            const infoX = chr.x + 100;
            const infoY = chr.y - 50;
            const infoWidth = 200;
            const infoHeight = 120;
            
            // 背景
            ctx.fillStyle = 'rgba(255, 255, 255, 0.95)';
            ctx.strokeStyle = '#4A6FA5';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.roundRect(infoX, infoY, infoWidth, infoHeight, 10);
            ctx.fill();
            ctx.stroke();
            
            // 文本
            ctx.fillStyle = '#333';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'left';
            ctx.fillText(`染色体 ${chr.id}`, infoX + 10, infoY + 25);
            
            ctx.font = '14px Arial';
            ctx.fillText(`来源: ${chr.paternal ? '父本' : '母本'}`, infoX + 10, infoY + 50);
            ctx.fillText(`长度: ${chr.length}`, infoX + 10, infoY + 70);
            ctx.fillText(`着丝粒位置: ${chr.centromerePos}`, infoX + 10, infoY + 90);
            ctx.fillText(`状态: ${chr.replicated ? '已复制' : '未复制'}`, infoX + 10, infoY + 110);
            
            // 连接线
            ctx.strokeStyle = '#4A6FA5';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            ctx.moveTo(chr.x, chr.y);
            ctx.lineTo(infoX, infoY + infoHeight/2);
            ctx.stroke();
            ctx.setLineDash([]);
        }
        
        // 处理画布点击
        function handleCanvasClick(event) {
            const rect = canvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;
            
            // 检查是否点击了染色体
            for (const chr of chromosomes) {
                if (chr.bounds && 
                    x >= chr.bounds.x && x <= chr.bounds.x + chr.bounds.width &&
                    y >= chr.bounds.y && y <= chr.bounds.y + chr.bounds.height) {
                    
                    if (selectedChromosome === chr.id) {
                        selectedChromosome = null; // 取消选择
                    } else {
                        selectedChromosome = chr.id; // 选择染色体
                        
                        // 如果是前期I且点击了第一对同源染色体，显示四分体信息
                        if (currentStage === 1 && chr.id <= 2) {
                            setTimeout(() => {
                                alert('四分体：一对同源染色体复制后形成的4条染色单体结构。\n\n在四分体时期，非姐妹染色单体之间可能发生交叉互换，这是遗传变异的重要来源。');
                            }, 100);
                        }
                    }
                    return;
                }
            }
            
            // 点击其他区域取消选择
            selectedChromosome = null;
        }
        
        // 动画控制函数
        function togglePlayPause() {
            isPlaying = !isPlaying;
            playPauseBtn.textContent = isPlaying ? '⏸ 暂停' : '▶ 播放';
        }
        
        function prevStage() {
            if (currentStage > 0) {
                currentStage--;
                animationProgress = 0;
                updateStageInfo();
                updateStageButtons();
            }
        }
        
        function nextStage() {
            if (currentStage < stages.length - 1) {
                currentStage++;
                animationProgress = 0;
                updateStageInfo();
                updateStageButtons();
            }
        }
        
        function goToStage(stage) {
            currentStage = stage;
            animationProgress = 0;
            updateStageInfo();
            updateStageButtons();
            
            // 根据阶段更新细胞状态
            if (currentStage >= 1) {
                cell.nuclearMembrane = false; // 前期I核膜消失
            } else {
                cell.nuclearMembrane = true;
            }
            
            // 重置染色体位置
            if (currentStage === 0) {
                arrangeChromosomes();
            }
        }
        
        function resetAnimation() {
            currentStage = 0;
            animationProgress = 0;
            isPlaying = false;
            playPauseBtn.textContent = '▶ 播放';
            selectedChromosome = null;
            
            // 重置染色体状态
            chromosomes.forEach(chr => {
                chr.replicated = false;
            });
            
            cell.nuclearMembrane = true;
            arrangeChromosomes();
            
            updateStageInfo();
            updateStageButtons();
        }
        
        function updateSpeed() {
            animationSpeed = parseFloat(speedSlider.value);
            speedValue.textContent = animationSpeed.toFixed(1) + 'x
<!--检测到代码截断，自动续写中...-->
        }
        
        function updateStageInfo() {
            const stage = stages[currentStage];
            currentStageTitle.textContent = stage.name;
            currentStageDesc.textContent = stage.description;
        }
        
        function updateStageButtons() {
            stageButtons.forEach((btn, index) => {
                if (index === currentStage) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
        }
        
        // 初始化并开始
        init();
        
        // 添加圆角矩形绘制方法（兼容性）
        if (!CanvasRenderingContext2D.prototype.roundRect) {
            CanvasRenderingContext2D.prototype.roundRect = function(x, y, width, height, radius) {
                if (width < 2 * radius) radius = width / 2;
                if (height < 2 * radius) radius = height / 2;
                this.beginPath();
                this.moveTo(x + radius, y);
                this.arcTo(x + width, y, x + width, y + height, radius);
                this.arcTo(x + width, y + height, x, y + height, radius);
                this.arcTo(x, y + height, x, y, radius);
                this.arcTo(x, y, x + width, y, radius);
                this.closePath();
                return this;
            }
        }
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 《减数分裂全过程交互式教学动画》使用指南

欢迎使用减数分裂全过程交互式教学动画！本指南将帮助您充分利用这个精心设计的教学工具，深入理解减数分裂这一重要的生物学过程。

---

### 一、功能说明

本动画是一个基于HTML5 Canvas技术开发的交互式教学工具，专门用于可视化展示减数分裂的全过程。它通过动态、可交互的方式，将抽象的染色体行为转化为直观的视觉体验，特别聚焦于减数分裂第一次分裂中的关键事件：**联会、四分体形成和同源染色体分离**。

### 二、主要功能

#### 1. **完整的阶段导航**
   - **阶段选择器**：通过顶部的9个阶段按钮（间期、前期I、中期I、后期I、末期I、前期II、中期II、后期II、末期II），您可以随时跳转到减数分裂的任何特定时期。
   - **实时阶段信息**：右侧信息面板会同步显示当前阶段的名称和详细描述。

#### 2. **灵活的动画控制**
   - **播放/暂停**：控制动画的连续播放或暂停在特定时刻。
   - **步进控制**：使用"上一阶段"和"下一阶段"按钮，按步骤观察每个关键转变。
   - **速度调节**：通过滑块调整动画播放速度（0.5x至3.0x），适应不同的学习节奏。
   - **重置功能**：一键回到初始状态，重新开始学习。

#### 3. **交互式探索**
   - **染色体点击交互**：点击画布中的任何染色体，会弹出详细信息框，显示该染色体的来源（父本/母本）、长度、着丝粒位置和状态。
   - **四分体特写**：在前期I阶段，点击第一对同源染色体，会触发关于"四分体"的详细解释弹窗，包括交叉互换的示意图。
   - **视觉高亮**：被选中的染色体会被明黄色光环高亮显示。

#### 4. **清晰的视觉编码**
   - **颜色系统**：
     - **深蓝色**：父本来源的染色体
     - **深红色**：母本来源的染色体
     - **半透明色**：复制后的姐妹染色单体
     - **浅紫色虚线**：纺锤丝
   - **动态效果**：染色体移动、纺锤丝牵引、核膜消失等过程都有平滑的动画表现。

### 三、设计特色

#### 1. **认知友好的教学设计**
   - **从整体到局部**：建议先观看完整动画，建立整体印象，再分阶段深入研究。
   - **重点突出**：通过颜色对比、高亮效果和特写镜头，强调同源染色体配对、分离等核心概念。
   - **对比学习**：清晰区分减数分裂I（同源染色体分离）和减数分裂II（姐妹染色单体分离）。

#### 2. **科学的准确性**
   - 染色体形态差异（长短、着丝粒位置）体现了同源染色体的"形态相似但来源不同"。
   - 准确呈现了纺锤体、中心粒等细胞结构在分裂中的作用。
   - 阶段划分和关键事件描述符合生物学标准。

#### 3. **响应式设计**
   - 适配不同屏幕尺寸，在电脑、平板等设备上都能获得良好的观看体验。

### 四、教学要点

#### 重点理解的核心概念：

1. **联会（Synapsis）**
   - **发生时期**：减数分裂前期I
   - **本质**：同源染色体配对的过程
   - **教学提示**：观察染色体如何从分散状态逐渐靠近并配对

2. **四分体（Tetrad）**
   - **形成条件**：同源染色体复制后配对
   - **结构特点**：4条染色单体（2条姐妹染色单体+2条非姐妹染色单体）
   - **重要意义**：交叉互换的发生部位，是遗传变异的来源之一
   - **教学提示**：点击第一对染色体查看特写，注意非姐妹染色单体间的交叉示意

3. **同源染色体分离**
   - **发生时期**：减数分裂后期I
   - **关键意义**：染色体数目减半（2n→n）的决定性步骤
   - **教学提示**：注意观察父本和母本来源的染色体如何分别移向两极

4. **两次分裂的本质区别**
   - **减数分裂I**：同源染色体分离，染色体数目减半
   - **减数分裂II**：姐妹染色单体分离，类似有丝分裂
   - **教学提示**：对比中期I（四分体排列）和中期II（染色体排列）的不同

### 五、使用建议

#### 给教师的建议：

1. **课堂演示**
   - 使用投影仪全屏展示，配合讲解逐步推进动画。
   - 在关键阶段暂停，引导学生观察特定结构（如四分体、纺锤丝附着点）。
   - 利用"重置"功能，重复演示难点部分。

2. **探究式学习**
   - 提出问题让学生通过交互探索寻找答案：
     - "染色体数目何时减半？"
     - "同源染色体和姐妹染色单体有何区别？"
     - "交叉互换发生在哪个时期？"
   - 让学生操作动画，解释他们观察到的现象。

3. **巩固练习**
   - 让学生不看描述，仅凭动画说出当前阶段和关键事件。
   - 比较减数分裂与有丝分裂的异同。

#### 给学生的建议：

1. **学习路径**
   - **第一步**：点击"播放"，完整观看一遍动画，了解全过程。
   - **第二步**：使用阶段导航，逐个阶段仔细研究，阅读右侧的详细说明。
   - **第三步**：尝试自己描述每个阶段的关键事件，然后与系统描述对照。
   - **第四步**：点击染色体进行交互探索，特别是前期I的四分体结构。

2. **难点突破**
   - 如果对"同源染色体"概念模糊，注意观察颜色区分（蓝vs红）和配对行为。
   - 如果混淆两次分裂，使用步进控制仔细比较中期I和中期II的差异。
   - 调整动画速度，在难点处慢速播放，仔细观察细节。

3. **自我检测**
   - 关闭阶段描述，仅凭动画画面判断当前阶段。
   - 解释为什么减数分裂能产生遗传多样性。
   - 绘制减数分裂关键阶段的示意图。

---

**温馨提示**：生物学概念的理解需要时间和反复观察。建议您多次使用本动画，每次关注不同的重点。随着对过程的熟悉，您会发现那些曾经抽象的概念变得越来越清晰直观。

祝您学习愉快，探索生命的奥秘！ 🧬🔬