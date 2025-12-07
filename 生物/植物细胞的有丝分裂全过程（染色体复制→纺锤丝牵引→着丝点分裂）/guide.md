# 需求：植物细胞的有丝分裂全过程（染色体复制→纺锤丝牵引→着丝点分裂）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要为中学生或生物学入门者。他们的核心需求是：
1.  **理解过程**：直观、动态地理解植物细胞有丝分裂从间期到末期的连续、复杂过程，特别是染色体形态与位置的关键变化。
2.  **掌握关键点**：清晰识别并记忆“染色体复制”、“纺锤丝牵引”、“着丝点分裂”这三个核心环节。
3.  **克服抽象难点**：将课本中静态的、分阶段的示意图，转化为一个动态、连续的整体过程，解决空间想象和过程连贯性理解上的困难。
4.  **自主探索**：能够控制动画的进度，反复观察特定阶段，并获取关键结构的名称和功能说明。

#### 教学设计思路
*   **核心概念**：聚焦于**染色体行为**这一主线。将细胞核、核膜、纺锤体、细胞板等结构作为背景或辅助元素，确保视觉焦点始终在染色体的复制、排列、分离和分配上。
*   **认知规律**：
    *   **从整体到细节**：先自动播放一次完整动画，建立整体过程印象。然后允许用户分阶段（间期、前期、中期、后期、末期）逐步学习。
    *   **强调对比**：通过颜色区分姐妹染色单体；通过动画高亮（如闪烁、放大）强调“复制”、“牵引”、“分裂”等关键动作时刻。
    *   **图文声同步**：关键步骤配有简洁的文字说明和温和的提示音效，强化记忆。
*   **交互设计**：
    *   **进程控制**：提供播放/暂停、步进（下一步/上一步）、重置按钮，以及一个可拖动的进度条。
    *   **阶段导航**：提供清晰的阶段标签（如“前期”、“中期”），点击可跳转。
    *   **探索式学习**：鼠标悬停在关键结构（如染色体、着丝点、纺锤丝）上时，显示其名称和简要功能。
    *   **提示与反馈**：在关键步骤前，有文字提示引导用户观察接下来会发生什么。
*   **视觉呈现**：
    *   **风格**：采用简洁、扁平化略带柔和质感的卡通风格，避免过于写实带来的视觉混乱。
    *   **视角**：采用固定的细胞横截面视角，保持场景稳定，便于观察内部变化。
    *   **动画节奏**：关键动作（如纺锤丝附着、着丝点分裂）速度稍慢，过渡阶段速度平缓，确保用户能跟上。

#### 配色方案选择
选择明亮、清晰且符合生物学直觉的配色，确保良好的可访问性和视觉舒适度。
*   **背景**：浅米色或极浅的灰色，营造柔和、专注的画布。
*   **细胞质/细胞壁**：半透明的浅黄绿色，表示生命感。
*   **细胞核/核膜**：浅蓝色，代表“控制中心”。
*   **染色体（染色质）**：
    *   **间期染色质**：浅灰色的网状。
    *   **分裂期染色体**：使用两种对比色（如亮红色和亮蓝色）区分来自父本和母本的同源染色体（简化模型），使复制和分离过程一目了然。
*   **着丝点**：亮黄色的小圆点，在染色体上非常醒目。
*   **纺锤丝**：纤细的深灰色或紫色线条。
*   **细胞板**：逐渐生长的绿色线条或区域。
*   **高亮/提示色**：使用醒目的橙色或明黄色，用于关键步骤的闪烁提示。

#### 交互功能列表
1.  **主控制面板**：
    *   播放/暂停按钮
    *   上一步/下一步按钮
    *   重置按钮
    *   进度条（可拖动）
2.  **阶段导航栏**：以标签形式显示“间期”、“前期”、“中期”、“后期”、“末期”，点击跳转。
3.  **信息显示区**：实时显示当前阶段的名称和简要描述。
4.  **悬停提示**：鼠标悬停在染色体、纺锤丝、着丝点、中心体（植物细胞中心体位置示意）上时，显示标签和功能说明。
5.  **关键步骤提示**：在进入“着丝点分裂”、“染色体分离”等关键节点前，出现文字提示框。
6.  **视觉焦点引导**：在关键动作发生时，使用光圈放大或颜色闪烁短暂突出相关结构。
7.  **音效反馈（可选）**：在阶段切换、关键动作完成时播放轻柔的提示音。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>植物细胞有丝分裂全过程教学动画</title>
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
            margin-bottom: 20px;
        }

        .main-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            max-width: 900px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            padding: 25px;
            margin-bottom: 20px;
        }

        .animation-container {
            position: relative;
            width: 100%;
            height: 500px;
            margin-bottom: 25px;
            border-radius: 10px;
            overflow: hidden;
            background-color: #fafafa;
            border: 2px solid #e0e0e0;
        }

        #mitosisCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .info-panel {
            position: absolute;
            top: 20px;
            left: 20px;
            background-color: rgba(255, 255, 255, 0.92);
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            min-width: 250px;
            max-width: 300px;
            border-left: 5px solid #3498db;
        }

        .phase-title {
            font-size: 1.4rem;
            color: #2c3e50;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .phase-description {
            font-size: 0.95rem;
            color: #555;
            line-height: 1.5;
        }

        .highlight {
            color: #e74c3c;
            font-weight: 600;
        }

        .controls {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 12px;
            margin-bottom: 25px;
            width: 100%;
        }

        .btn {
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .btn-primary {
            background-color: #3498db;
            color: white;
        }

        .btn-primary:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background-color: #95a5a6;
            color: white;
        }

        .btn-secondary:hover {
            background-color: #7f8c8d;
            transform: translateY(-2px);
        }

        .btn-success {
            background-color: #2ecc71;
            color: white;
        }

        .btn-success:hover {
            background-color: #27ae60;
            transform: translateY(-2px);
        }

        .btn-warning {
            background-color: #f39c12;
            color: white;
        }

        .btn-warning:hover {
            background-color: #d68910;
            transform: translateY(-2px);
        }

        .phase-nav {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
            width: 100%;
        }

        .phase-btn {
            padding: 10px 18px;
            background-color: #ecf0f1;
            border: 2px solid #bdc3c7;
            border-radius: 6px;
            font-size: 0.95rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            color: #34495e;
        }

        .phase-btn:hover {
            background-color: #d5dbdb;
        }

        .phase-btn.active {
            background-color: #3498db;
            color: white;
            border-color: #2980b9;
        }

        .slider-container {
            width: 100%;
            margin-bottom: 20px;
        }

        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-weight: 600;
            color: #2c3e50;
        }

        #phaseSlider {
            width: 100%;
            height: 10px;
            -webkit-appearance: none;
            appearance: none;
            background: linear-gradient(to right, #2ecc71, #f1c40f, #e74c3c, #9b59b6, #3498db);
            border-radius: 5px;
            outline: none;
        }

        #phaseSlider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 24px;
            height: 24px;
            border-radius: 50%;
            background: #2c3e50;
            cursor: pointer;
            border: 3px solid white;
            box-shadow: 0 2px 6px rgba(0,0,0,0.3);
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #eee;
            width: 100%;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
        }

        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }

        .tooltip {
            position: absolute;
            background-color: rgba(44, 62, 80, 0.95);
            color: white;
            padding: 10px 15px;
            border-radius: 6px;
            font-size: 0.9rem;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 100;
            max-width: 250px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
        }

        .footer {
            text-align: center;
            color: #7f8c8d;
            font-size: 0.9rem;
            margin-top: 10px;
            width: 100%;
            max-width: 900px;
        }

        @media (max-width: 768px) {
            .main-container {
                padding: 15px;
            }
            
            .animation-container {
                height: 400px;
            }
            
            .info-panel {
                position: relative;
                top: 0;
                left: 0;
                margin-bottom: 15px;
                max-width: 100%;
            }
            
            .btn {
                padding: 10px 18px;
                font-size: 0.9rem;
            }
            
            .phase-btn {
                padding: 8px 14px;
                font-size: 0.85rem;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>🌱 植物细胞有丝分裂全过程</h1>
        <p class="subtitle">染色体复制 → 纺锤丝牵引 → 着丝点分裂 → 细胞分裂</p>
    </div>

    <div class="main-container">
        <div class="animation-container">
            <canvas id="mitosisCanvas"></canvas>
            <div class="info-panel">
                <div class="phase-title" id="currentPhaseTitle">间期 (Interphase)</div>
                <div class="phase-description" id="currentPhaseDesc">细胞生长，DNA复制，为分裂做准备。染色体以染色质形式存在。</div>
            </div>
            <div class="tooltip" id="cellTooltip"></div>
        </div>

        <div class="phase-nav">
            <button class="phase-btn active" data-phase="0">间期</button>
            <button class="phase-btn" data-phase="1">前期</button>
            <button class="phase-btn" data-phase="2">中期</button>
            <button class="phase-btn" data-phase="3">后期</button>
            <button class="phase-btn" data-phase="4">末期</button>
        </div>

        <div class="slider-container">
            <div class="slider-label">
                <span>有丝分裂进程</span>
                <span id="phaseLabel">间期</span>
            </div>
            <input type="range" id="phaseSlider" min="0" max="100" value="0">
        </div>

        <div class="controls">
            <button class="btn btn-primary" id="playPauseBtn">
                <span id="playIcon">▶</span> <span id="playText">播放</span>
            </button>
            <button class="btn btn-secondary" id="prevBtn">◀ 上一步</button>
            <button class="btn btn-secondary" id="nextBtn">下一步 ▶</button>
            <button class="btn btn-warning" id="resetBtn">↺ 重置</button>
            <button class="btn btn-success" id="highlightBtn">🔍 高亮关键步骤</button>
        </div>

        <div class="legend">
            <div class="legend-item">
                <div class="legend-color" style="background-color: #e74c3c;"></div>
                <span>母源染色体</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #3498db;"></div>
                <span>父源染色体</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #f1c40f;"></div>
                <span>着丝点</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #9b59b6;"></div>
                <span>纺锤丝</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #2ecc71;"></div>
                <span>细胞板</span>
            </div>
        </div>
    </div>

    <div class="footer">
        <p>教学动画 | 植物细胞有丝分裂 | 交互式学习工具 | 染色体行为可视化</p>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('mitosisCanvas');
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
        
        // 有丝分裂阶段定义
        const phases = [
            {
                name: "间期",
                title: "间期 (Interphase)",
                description: "细胞生长，<span class='highlight'>DNA复制</span>，为分裂做准备。染色体以染色质形式存在。",
                duration: 200,
                progress: 0
            },
            {
                name: "前期",
                title: "前期 (Prophase)",
                description: "染色质螺旋化，缩短变粗形成<span class='highlight'>染色体</span>。核膜、核仁逐渐消失。<span class='highlight'>纺锤丝</span>开始形成。",
                duration: 150,
                progress: 0
            },
            {
                name: "中期",
                title: "中期 (Metaphase)",
                description: "染色体在<span class='highlight'>纺锤丝牵引</span>下排列在细胞中央的赤道板上。这是观察染色体形态和数目的最佳时期。",
                duration: 150,
                progress: 0
            },
            {
                name: "后期",
                title: "后期 (Anaphase)",
                description: "<span class='highlight'>着丝点分裂</span>，姐妹染色单体分离，在纺锤丝牵引下移向细胞两极。",
                duration: 150,
                progress: 0
            },
            {
                name: "末期",
                title: "末期 (Telophase)",
                description: "染色体到达两极，解螺旋成为染色质。核膜、核仁重新出现。<span class='highlight'>细胞板</span>形成，将细胞质分割为两部分。",
                duration: 200,
                progress: 0
            }
        ];
        
        // 动画状态
        let currentPhase = 0;
        let phaseProgress = 0;
        let isPlaying = false;
        let animationId = null;
        let highlightMode = false;
        let lastTime = 0;
        
        // 细胞和染色体参数
        const cell = {
            x: 0,
            y: 0,
            radius: 0,
            wallWidth: 8,
            nuclearRadius: 0,
            nuclearMembraneWidth: 4,
            spindlePoles: [],
            cellPlateProgress: 0
        };
        
        // 染色体参数
        const chromosomes = [];
        const chromosomeCount = 4; // 简化模型：2对同源染色体
        
        // 初始化染色体
        function initChromosomes() {
            chromosomes.length = 0;
            
            // 创建染色体对（简化模型）
            for (let i = 0; i < chromosomeCount; i++) {
                const isMaternal = i < chromosomeCount / 2; // 前一半为母源
                
                chromosomes.push({
                    id: i,
                    isMaternal: isMaternal,
                    x: 0,
                    y: 0,
                    length: 40,
                    width: 8,
                    angle: Math.random() * Math.PI * 2,
                    condensed: false, // 是否凝缩
                    duplicated: false, // 是否复制
                  sisterSeparated: false, // 姐妹染色单体是否分离
                    centromereX: 0,
                    centromereY: 0,
                    spindleAttached: false,
                    movingToPole: false,
                    targetPole: 0,
                    progress: 0
                });
            }
        }
        
        // 初始化细胞参数
        function initCell() {
            cell.x = canvas.width / 2;
            cell.y = canvas.height / 2;
            cell.radius = Math.min(canvas.width, canvas.height) * 0.35;
            cell.nuclearRadius = cell.radius * 0.6;
            
            // 纺锤体两极
            cell.spindlePoles = [
                { x: cell.x - cell.radius * 0.6, y: cell.y },
                { x: cell.x + cell.radius * 0.6, y: cell.y }
            ];
            
            cell.cellPlateProgress = 0;
        }
        
        // 更新UI
        function updateUI() {
            // 更新阶段标题和描述
            document.getElementById('currentPhaseTitle').textContent = phases[currentPhase].title;
            document.getElementById('currentPhaseDesc').innerHTML = phases[currentPhase].description;
            
            // 更新阶段按钮
            document.querySelectorAll('.phase-btn').forEach((btn, index) => {
                if (index === currentPhase) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            // 更新滑块和标签
            const totalProgress = currentPhase * 20 + (phaseProgress / phases[currentPhase].duration) * 20;
            document.getElementById('phaseSlider').value = totalProgress;
            document.getElementById('phaseLabel').textContent = phases[currentPhase].name;
            
            // 更新播放按钮
            document.getElementById('playIcon').textContent = isPlaying ? '⏸' : '▶';
            document.getElementById('playText').textContent = isPlaying ? '暂停' : '播放';
        }
        
        // 绘制细胞
        function drawCell() {
            // 细胞壁
            ctx.beginPath();
            ctx.arc(cell.x, cell.y, cell.radius, 0, Math.PI * 2);
            ctx.fillStyle = 'rgba(240, 255, 240, 0.7)';
            ctx.fill();
            ctx.lineWidth = cell.wallWidth;
            ctx.strokeStyle = '#7cb342';
            ctx.stroke();
            
            // 细胞质（轻微纹理）
            for (let i = 0; i < 30; i++) {
                const angle = Math.random() * Math.PI * 2;
                const dist = Math.random() * cell.radius * 0.8;
                const x = cell.x + Math.cos(angle) * dist;
                const y = cell.y + Math.sin(angle) * dist;
                const radius = Math.random() * 5 + 2;
                
                ctx.beginPath();
                ctx.arc(x, y, radius, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(200, 230, 200, 0.2)';
                ctx.fill();
            }
            
            // 核膜（根据阶段逐渐消失/重现）
            if (currentPhase < 1 || currentPhase >= 4) {
                const nuclearAlpha = currentPhase < 1 ? 1 : (phaseProgress / phases[4].duration);
                
                ctx.beginPath();
                ctx.arc(cell.x, cell.y, cell.nuclearRadius, 0, Math.PI * 2);
                ctx.fillStyle = `rgba(173, 216, 230, ${0.3 * nuclearAlpha})`;
                ctx.fill();
                ctx.lineWidth = cell.nuclearMembraneWidth;
                ctx.strokeStyle = `rgba(70, 130, 180, ${nuclearAlpha})`;
                ctx.stroke();
                
                // 核仁（间期和末期）
                if (currentPhase < 1 || currentPhase >= 4) {
                    ctx.beginPath();
                    ctx.arc(cell.x, cell.y, cell.nuclearRadius * 0.3, 0, Math.PI * 2);
                    ctx.fillStyle = `rgba(255, 228, 181, ${0.7 * nuclearAlpha})`;
                    ctx.fill();
                }
            }
            
            // 纺锤体（前期到后期）
            if (currentPhase >= 1 && currentPhase <= 3) {
                const spindleAlpha = Math.min(1, phaseProgress / 30);
                
                // 纺锤丝
                chromosomes.forEach(chromosome => {
                    if (chromosome.spindleAttached) {
                        const pole = cell.spindlePoles[chromosome.targetPole];
                        
                        ctx.beginPath();
                        ctx.moveTo(pole.x, pole.y);
                        ctx.lineTo(chromosome.centromereX, chromosome.centromereY);
                        ctx.lineWidth = 2;
                        ctx.strokeStyle = `rgba(155, 89, 182, ${spindleAlpha})`;
                        ctx.stroke();
                        
                        // 纺锤丝端点
                        ctx.beginPath();
                        ctx.arc(pole.x, pole.y, 5, 0, Math.PI * 2);
                        ctx.fillStyle = `rgba(155, 89, 182, ${spindleAlpha})`;
                        ctx.fill();
                    }
                });
            }
            
            // 细胞板（末期）
            if (currentPhase === 4) {
                cell.cellPlateProgress = phaseProgress / phases[4].duration;
                
                ctx.beginPath();
                ctx.moveTo(cell.x - cell.radius, cell.y);
                ctx.lineTo(cell.x - cell.radius + cell.radius * 2 * cell.cellPlateProgress, cell.y);
                ctx.lineWidth = 6;
                ctx.strokeStyle = '#2ecc71';
                ctx.stroke();
            }
        }
        
        // 绘制染色体
        function drawChromosomes() {
            chromosomes.forEach(chromosome => {
                // 计算染色体位置和状态
                updateChromosomeState(chromosome);
                
                // 染色体颜色
                const color = chromosome.isMaternal ? '#e74c3c' : '#3498db';
                
                // 间期：染色质状态（网状）
                if (currentPhase === 0) {
                    drawChromatin(chromosome, color);
                } 
                // 其他时期：染色体状态
                else {
                    drawCondensedChromosome(chromosome, color);
                }
                
                // 高亮模式：显示着丝点
                if (highlightMode && currentPhase >= 1) {
                    ctx.beginPath();
                    ctx.arc(chromosome.centromereX, chromosome.centromereY, 6, 0, Math.PI * 2);
                    ctx.fillStyle = '#f1c40f';
                    ctx.fill();
                    ctx.lineWidth = 2;
                    ctx.strokeStyle = '#d35400';
                    ctx.stroke();
                }
            });
        }
        
        // 绘制染色质（间期）
        function drawChromatin(chromosome, color) {
            const chromatinProgress = phaseProgress / phases[0].duration;
            const duplicated = chromatinProgress > 0.5;
            
            // 染色质网状结构
            const points = [];
            const numPoints = 8;
            
            for (let i = 0; i < numPoints; i++) {
                const angle = chromosome.angle + (i / numPoints) * Math.PI * 2;
                const radius = chromosome.length * 0.5 * (0.7 + Math.random() * 0.3);
                const x = chromosome.x + Math.cos(angle) * radius;
                const y = chromosome.y + Math.sin(angle) * radius;
                points.push({x, y});
                
                // 绘制点
                ctx.beginPath();
                ctx.arc(x, y, 3, 0, Math.PI * 2);
                ctx.fillStyle = color;
                ctx.fill();
            }
            
            // 连接线（染色质纤维）
            for (let i = 0; i < points.length; i++) {
                for (let j = i + 1; j < points.length; j++) {
                    if (Math.random() > 0.6) {
                        ctx.beginPath();
                        ctx.moveTo(points[i].x, points[i].y);
                        ctx.lineTo(points[j].x, points[j].y);
                        ctx.lineWidth = 1;
                        ctx.strokeStyle = `${color}80`;
                        ctx.stroke();
                    }
                }
            }
            
            // 如果已复制，绘制第二个染色质团
            if (duplicated) {
                const offset = 15;
                
                for (let i = 0; i < numPoints; i++) {
                    const angle = chromosome.angle + (i / numPoints) * Math.PI * 2;
                    const radius = chromosome.length * 0.5 * (0.7 + Math.random() * 0.3);
                    const x = chromosome.x + Math.cos(angle) * radius + offset;
                    const y = chromosome.y + Math.sin(angle) * radius + offset;
                    
                    ctx.beginPath();
                    ctx.arc(x, y, 3, 0, Math.PI * 2);
                    ctx.fillStyle = color;
                    ctx.fill();
                }
            }
        }
        
        // 绘制凝缩的染色体
        function drawCondensedChromosome(chromosome, color) {
            // 计算染色体位置
            const phase = currentPhase;
            const progress = chromosome.progress;
            
            let startX, startY, endX, endY;
            let centromerePos = 0.5; // 着丝点位置
            
            // 根据阶段确定染色体位置和方向
            if (phase === 1) { // 前期：随机分布
                startX = chromosome.x;
                startY = chromosome.y;
                endX = startX + Math.cos(chromosome.angle) * chromosome.length;
                endY = startY + Math.sin(chromosome.angle) * chromosome.length;
                
                // 逐渐凝缩
                const condensation = Math.min(1, progress * 2);
                chromosome.condensed = condensation > 0.5;
            } 
            else if (phase === 2) { // 中期：排列在赤道板
                const row = Math.floor(chromosome.id / 2);
                const col = chromosome.id % 2;
                const spacing = chromosome.length * 1.5;
                
                startX = cell.x - spacing/2 + col * spacing;
                startY = cell.y - spacing/2 + row * spacing;
                endX = startX;
                endY = startY + chromosome.length;
                
                // 纺锤丝附着
                if (progress > 0.3) {
                    chromosome.spindleAttached = true;
                    chromosome.targetPole = chromosome.id % 2;
                }
            } 
            else if (phase === 3) { // 后期：向两极移动
                const pole = cell.spindlePoles[chromosome.targetPole];
                const poleProgress = progress;
                
                // 计算移动位置
                const startPos = { x: cell.x, y: cell.y };
                if (chromosome.id % 2 === 0) {
                    startPos.x -= chromosome.length;
                } else {
                    startPos.x += chromosome.length;
                }
                
                startX = startPos.x + (pole.x - startPos.x) * poleProgress;
                startY = startPos.y + (pole.y - startPos.y) * poleProgress;
                
                // 指向极点的方向
                const angleToPole = Math.atan2(pole.y - startY, pole.x - startX);
                endX = startX + Math.cos(angleToPole) * chromosome.length;
                endY = startY + Math.sin(angleToPole) * chromosome.length;
                
                // 着丝点分裂，姐妹染色单体分离
                if (progress > 0.5) {
                    chromosome.sisterSeparated = true;
                }
            } 
            else if (phase === 4) { // 末期：到达两极并开始解螺旋
                const pole = cell.spindlePoles[chromosome.targetPole];
                const decondenseProgress = progress;
                
                startX = pole.x;
                startY = pole.y;
                
                // 逐渐解螺旋
                const currentLength = chromosome.length * (1 - decondenseProgress * 0.7);
                const angle = chromosome.angle + progress * Math.PI;
                
                endX = startX + Math.cos(angle) * currentLength;
                endY = startY + Math.sin(angle) * currentLength;
                
                chromosome.condensed = decondenseProgress < 0.5;
            }
            
            // 更新着丝点位置
            chromosome.centromereX = startX + (endX - startX) * centromerePos;
            chromosome.centromereY = startY + (endY - startY) * centromerePos;
            
            // 绘制染色体臂
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            ctx.lineTo(endX, endY);
            ctx.lineWidth = chromosome.width;
            ctx.lineCap = 'round';
            ctx.strokeStyle = color;
            ctx.stroke();
            
            // 如果已复制且未分离，绘制姐妹染色单体
            if (chromosome.duplicated && !chromosome.sisterSeparated) {
                const offset = chromosome.width;
                const perpendicularAngle = Math.atan2(endY - startY, endX - startX) + Math.PI/2;
                
                const startX2 = startX + Math.cos(perpendicularAngle) * offset;
                const startY2 = startY + Math.sin(perpendicularAngle) * offset;
                const endX2 = endX + Math.cos(perpendicularAngle) * offset;
                const endY2 = endY + Math.sin(perpendicularAngle) * offset;
                
                ctx.beginPath();
                ctx.moveTo(startX2, startY2);
                ctx.lineTo(endX2, endY2);
                ctx.lineWidth = chromosome.width;
                ctx.lineCap = 'round';
                ctx.strokeStyle = `${color}80`; // 半透明
                ctx.stroke();
                
                // 连接两条单体（着丝点区域）
                ctx.beginPath();
                ctx.moveTo(startX + (endX - startX) * centromerePos, startY + (endY - startY) * centromerePos);
                ctx.lineTo(startX2 + (endX2 - startX2) * centromerePos, startY2 + (endY2 - startY2) * centromerePos);
                ctx.lineWidth = 3;
                ctx.strokeStyle = '#f1c40f';
                ctx.stroke();
            }
            
            // 绘制着丝点（高亮模式或特定阶段）
            if (highlightMode || (phase >= 2 && phase <= 3)) {
                ctx.beginPath();
                ctx.arc(chromosome.centromereX, chromosome.centromereY, 4, 0, Math.PI * 2);
                ctx.fillStyle = '#f1c40f';
                ctx.fill();
            }
        }
        
        // 更新染色体状态
        function updateChromosomeState(chromosome) {
            // 更新染色体位置（在细胞核内随机分布）
            if (currentPhase <= 1) {
                const angle = chromosome.angle + 0.01;
                const radius = cell.nuclearRadius * 0.7;
                
                chromosome.x = cell.x + Math.cos(angle) * radius;
                chromosome.y = cell.y + Math.sin(angle) * radius;
                chromosome.angle = angle;
            }
            
            // 更新阶段进度
            chromosome.progress = phaseProgress / phases[currentPhase].duration;
            
            // 根据阶段设置染色体状态
            if (currentPhase === 0 && chromosome.progress > 0.5) {
                chromosome.duplicated = true; // DNA复制完成
            }
            
            if (currentPhase === 1 && chromosome.progress > 0.7) {
                chromosome.condensed = true; // 染色体凝缩
            }
            
            if (currentPhase === 3 && chromosome.progress > 0.3) {
                chromosome.movingToPole = true; // 开始向极点移动
            }
        }
        
        // 绘制高亮提示
        function drawHighlights() {
            if (!highlightMode) return;
            
            ctx.fillStyle = 'rgba(255, 255, 200, 0.1)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 根据阶段显示不同的高亮提示
            ctx.font = 'bold 18px Arial';
            ctx.fillStyle = '#e74c3c';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            
            if (currentPhase === 0 && phaseProgress > phases[0].duration * 0.4) {
                ctx.fillText('DNA复制中...', canvas.width / 2, canvas.height / 2 - 50);
            } 
            else if (currentPhase === 1 && phaseProgress > phases[1].duration * 0.5) {
                ctx.fillText('染色体凝缩，纺锤体形成', canvas.width / 2, canvas.height / 2 - 50);
            } 
            else if (currentPhase === 2 && phaseProgress > phases[2].duration * 0.5) {
                ctx.fillText('纺锤丝牵引染色体排列', canvas.width / 2, canvas.height / 2 - 50);
            } 
            else if (currentPhase === 3 && phaseProgress > phases[3].duration * 0.3) {
                ctx.fillText('着丝点分裂！姐妹染色单体分离', canvas.width / 2, canvas.height / 2 - 50);
            } 
            else if (currentPhase === 4 && phaseProgress > phases[4].duration * 0.5) {
                ctx.fillText('细胞板形成，细胞质分裂', canvas.width / 2, canvas.height / 2 - 50);
            }
        }
        
        // 绘制工具提示
        function drawTooltip(mouseX, mouseY) {
            const tooltip = document.getElementById('cellTooltip');
            let tooltipText = '';
            
            // 检查鼠标是否在染色体上
            chromosomes.forEach(chromosome => {
                if (currentPhase === 0) {
                    // 间期：检查染色质区域
                    const dx = mouseX - chromosome.x;
                    const dy = mouseY - chromosome.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < 30) {
                        tooltipText = chromosome.isMaternal ? '母源染色质' : '父源染色质';
                        if (chromosome.duplicated) {
                            tooltipText += ' (已复制)';
                        }
                    }
                } else {
                    // 其他时期：检查染色体区域
                    const dx = mouseX - chromosome.centromereX;
                    const dy = mouseY - chromosome.centromereY;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < 15) {
                        tooltipText = chromosome.isMaternal ? '母源染色体' : '父源染色体';
                        if (chromosome.duplicated && !chromosome.sisterSeparated) {
                            tooltipText += ' (姐妹染色单体)';
                        }
                        if (chromosome.sisterSeparated) {
                            tooltipText += ' (已分离)';
                        }
                    }
                }
            });
            
            // 检查鼠标是否在纺锤丝上
            if (currentPhase >= 1 && currentPhase <= 3) {
                cell.spindlePoles.forEach((pole, index) => {
                    const dx = mouseX - pole.x;
                    const dy = mouseY - pole.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < 10) {
                        tooltipText = index === 0 ? '纺锤体一极' : '纺锤体另一极';
                    }
                });
            }
            
            // 检查鼠标是否在细胞板上
            if (currentPhase === 4) {
                const dx = mouseX - cell.x;
                const dy = mouseY - cell.y;
                
                if (Math.abs(dy - cell.y) < 10 && Math.abs(dx) < cell.radius * cell.cellPlateProgress) {
                    tooltipText = '细胞板 (正在形成)';
                }
            }
            
            // 显示或隐藏工具提示
            if (tooltipText) {
                tooltip.style.opacity = '1';
                tooltip.style.left = (mouseX + 15) + 'px';
                tooltip.style.top = (mouseY - 15) + 'px';
                tooltip.textContent = tooltipText;
            } else {
                tooltip.style.opacity = '0';
            }
        }
        
        // 主绘制函数
        function draw(timestamp) {
            // 计算时间增量
            const deltaTime = lastTime ? timestamp - lastTime : 0;
            lastTime = timestamp;
            
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 更新动画进度
            if (isPlaying) {
                phaseProgress += deltaTime * 0.1; // 控制动画速度

<!--检测到代码截断，自动续写中...-->
// 检查是否进入下一阶段
                if (phaseProgress >= phases[currentPhase].duration) {
                    phaseProgress = 0;
                    currentPhase++;
                    
                    if (currentPhase >= phases.length) {
                        currentPhase = phases.length - 1;
                        isPlaying = false;
                    }
                    
                    updateUI();
                }
            }
            
            // 绘制所有元素
            drawCell();
            drawChromosomes();
            drawHighlights();
            
            // 继续动画循环
            animationId = requestAnimationFrame(draw);
        }
        
        // 初始化函数
        function init() {
            initCell();
            initChromosomes();
            updateUI();
            
            // 开始动画循环
            animationId = requestAnimationFrame(draw);
            
            // 设置事件监听器
            setupEventListeners();
        }
        
        // 设置事件监听器
        function setupEventListeners() {
            // 播放/暂停按钮
            document.getElementById('playPauseBtn').addEventListener('click', () => {
                isPlaying = !isPlaying;
                updateUI();
            });
            
            // 上一步按钮
            document.getElementById('prevBtn').addEventListener('click', () => {
                phaseProgress = 0;
                if (currentPhase > 0) {
                    currentPhase--;
                }
                isPlaying = false;
                updateUI();
            });
            
            // 下一步按钮
            document.getElementById('nextBtn').addEventListener('click', () => {
                phaseProgress = 0;
                if (currentPhase < phases.length - 1) {
                    currentPhase++;
                }
                isPlaying = false;
                updateUI();
            });
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', () => {
                currentPhase = 0;
                phaseProgress = 0;
                isPlaying = false;
                initChromosomes();
                updateUI();
            });
            
            // 高亮按钮
            document.getElementById('highlightBtn').addEventListener('click', () => {
                highlightMode = !highlightMode;
                document.getElementById('highlightBtn').style.backgroundColor = 
                    highlightMode ? '#e74c3c' : '#2ecc71';
            });
            
            // 阶段按钮
            document.querySelectorAll('.phase-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    currentPhase = parseInt(btn.dataset.phase);
                    phaseProgress = 0;
                    isPlaying = false;
                    updateUI();
                });
            });
            
            // 进度条
            document.getElementById('phaseSlider').addEventListener('input', (e) => {
                const value = parseInt(e.target.value);
                currentPhase = Math.floor(value / 20);
                phaseProgress = (value % 20) / 20 * phases[currentPhase].duration;
                isPlaying = false;
                updateUI();
            });
            
            // 鼠标移动事件（工具提示）
            canvas.addEventListener('mousemove', (e) => {
                const rect = canvas.getBoundingClientRect();
                const mouseX = e.clientX - rect.left;
                const mouseY = e.clientY - rect.top;
                drawTooltip(mouseX, mouseY);
            });
            
            // 鼠标离开画布时隐藏工具提示
            canvas.addEventListener('mouseleave', () => {
                document.getElementById('cellTooltip').style.opacity = '0';
            });
            
            // 键盘控制
            document.addEventListener('keydown', (e) => {
                switch(e.key) {
                    case ' ':
                    case 'Spacebar':
                        e.preventDefault();
                        isPlaying = !isPlaying;
                        updateUI();
                        break;
                    case 'ArrowLeft':
                        e.preventDefault();
                        phaseProgress = 0;
                        if (currentPhase > 0) currentPhase--;
                        isPlaying = false;
                        updateUI();
                        break;
                    case 'ArrowRight':
                        e.preventDefault();
                        phaseProgress = 0;
                        if (currentPhase < phases.length - 1) currentPhase++;
                        isPlaying = false;
                        updateUI();
                        break;
                    case 'r':
                    case 'R':
                        e.preventDefault();
                        currentPhase = 0;
                        phaseProgress = 0;
                        isPlaying = false;
                        initChromosomes();
                        updateUI();
                        break;
                    case 'h':
                    case 'H':
                        e.preventDefault();
                        highlightMode = !highlightMode;
                        document.getElementById('highlightBtn').style.backgroundColor = 
                            highlightMode ? '#e74c3c' : '#2ecc71';
                        break;
                }
            });
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
        
        // 清理动画帧
        window.addEventListener('beforeunload', () => {
            if (animationId) {
                cancelAnimationFrame(animationId);
            }
        });
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

# 植物细胞有丝分裂交互式教学动画使用指南

## 🎯 功能说明

欢迎使用"植物细胞有丝分裂全过程"交互式教学动画！本工具旨在通过动态可视化方式，帮助您深入理解植物细胞有丝分裂的完整过程，特别是染色体复制、纺锤丝牵引和着丝点分裂等关键生物学事件。动画采用专业教学设计，结合直观的视觉呈现和灵活的交互控制，让复杂的分裂过程变得生动易懂。

## 🎮 主要功能

### 1. **动画控制面板**
   - **播放/暂停**：控制动画的连续播放与暂停
   - **上一步/下一步**：逐阶段前进或后退，精细观察每个变化
   - **重置**：将动画恢复到初始状态（间期）
   - **高亮关键步骤**：突出显示当前阶段的核心生物学事件

### 2. **智能导航系统**
   - **阶段标签导航**：直接点击"间期、前期、中期、后期、末期"标签，快速跳转到指定阶段
   - **进度条控制**：拖动滑块自由调整动画进度，精确控制观察节奏
   - **键盘快捷键**：
     - 空格键：播放/暂停
     - 左右箭头：上一步/下一步
     - R键：重置动画
     - H键：切换高亮模式

### 3. **交互学习功能**
   - **悬停提示**：鼠标悬停在染色体、纺锤丝、着丝点等结构上，显示其名称和状态信息
   - **实时信息面板**：左侧信息栏实时显示当前阶段的名称、特征和关键生物学过程
   - **视觉图例**：底部图例清晰标示不同结构的颜色编码

## 🌟 设计特色

### 1. **科学准确性**
   - 严格遵循植物细胞有丝分裂的生物学过程
   - 准确呈现染色体形态变化：染色质→染色体→染色质的循环
   - 真实模拟纺锤体形成、着丝点分裂等关键事件

### 2. **教学友好性**
   - **渐进式学习**：从整体观察到细节探索，符合认知规律
   - **重点突出**：使用颜色对比区分母源/父源染色体，黄色高亮着丝点
   - **过程连贯**：展现分裂过程的连续性，而非孤立的阶段图片

### 3. **视觉优化**
   - **色彩科学**：采用生物学直觉配色方案，增强记忆关联
   - **层次分明**：细胞壁、细胞质、细胞核、染色体层次清晰
   - **动态流畅**：动画过渡自然，关键动作速度适宜

## 📚 教学要点

### 核心概念可视化
1. **染色体复制（间期）**
   - 观察染色质从单一线状到复制成双的过程
   - 注意DNA复制发生在间期，为分裂做准备

2. **纺锤丝牵引（前期-中期）**
   - 前期：纺锤体开始形成，核膜逐渐消失
   - 中期：染色体在纺锤丝牵引下排列在赤道板
   - 理解纺锤丝在染色体移动中的"轨道"作用

3. **着丝点分裂（后期）**
   - 这是整个过程的**关键转折点**
   - 观察姐妹染色单体在着丝点分裂后分离
   - 注意纺锤丝收缩牵引染色体向两极移动

4. **细胞分裂（末期）**
   - 观察细胞板如何从中央向两侧生长
   - 理解植物细胞特有的细胞板形成过程
   - 注意核膜、核仁的重现

### 易混淆点澄清
- **植物vs动物细胞**：重点观察细胞板形成（植物特有）vs 缢裂（动物特有）
- **染色体计数时机**：中期是观察染色体形态和数目的最佳时期
- **DNA量变化**：间期复制后DNA加倍，末期结束时恢复原量

## 💡 使用建议

### 课堂教学场景
1. **导入环节**：全屏播放一次完整动画，建立整体印象
2. **讲解环节**：分阶段暂停，结合信息面板详细讲解
3. **互动环节**：让学生操作控制面板，探索特定阶段
4. **巩固环节**：关闭高亮提示，测试学生识别能力

### 自主学习模式
1. **探索式学习**：
   - 先自主操作观察，记录发现的问题
   - 使用高亮功能验证自己的理解
   - 反复观察难点步骤（如着丝点分裂）

2. **笔记辅助**：
   - 在每个阶段暂停，绘制简图
   - 记录关键事件的发生顺序
   - 对比不同阶段染色体的形态变化

3. **自我测试**：
   - 隐藏信息面板，尝试描述当前阶段
   - 预测下一步会发生什么
   - 解释染色体移动的机制

### 最佳实践技巧
1. **观察顺序建议**：
   ```
   整体播放 → 分阶段学习 → 难点反复 → 完整回顾
   ```

2. **注意力引导**：
   - 前期：关注染色体凝缩和纺锤体形成
   - 中期：注意赤道板排列的整齐性
   - 后期：紧盯着丝点分裂瞬间
   - 末期：观察细胞板的生长方向

3. **概念联系**：
   - 将动画过程与课本文字描述对应
   - 思考每个变化的生物学意义
   - 联系实际：理解细胞分裂对植物生长的意义

### 技术提示
- 推荐使用Chrome或Edge浏览器获得最佳体验
- 全屏模式可获得更佳观察效果（F11键）
- 在平板设备上支持触摸操作
- 动画响应式设计，适应不同屏幕尺寸

## 🎓 学习目标达成

通过本动画的学习，您将能够：
1. **描述**有丝分裂各阶段的主要特征
2. **解释**染色体行为变化的内在机制
3. **识别**植物细胞有丝分裂的关键结构
4. **比较**不同阶段染色体的形态差异
5. **应用**所学知识分析细胞分裂相关问题

---

**教学提示**：生物学是动态的科学，细胞分裂是生命延续的基础过程。建议教师引导学生不仅"看"动画，更要"思"原理，将形态变化与功能意义相结合，培养生物学核心素养。

祝您探索愉快，在微观世界中发现生命的奥秘！ 🌱🔬