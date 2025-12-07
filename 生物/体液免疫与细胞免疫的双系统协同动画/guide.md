# 需求：体液免疫与细胞免疫的双系统协同动画

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的生物学/医学专业学生，他们已具备基础的免疫学知识，需要深入理解体液免疫与细胞免疫这两个核心分支的区别、流程及协同机制。
2.  **核心需求**：
    *   **概念可视化**：将抽象的免疫细胞（B细胞、T细胞、抗原呈递细胞等）、分子（抗体、细胞因子）和作用过程（活化、增殖、效应）转化为直观、动态的视觉元素。
    *   **流程清晰化**：清晰地展示体液免疫（抗体介导）和细胞免疫（T细胞直接攻击）两条路径各自的启动、发展和效应阶段。
    *   **协同机制突出**：重点演示两个系统如何并非孤立工作，而是通过辅助T细胞（Th细胞）等关键节点进行信息交流和协同作战，共同清除病原体（特别是胞内寄生菌、病毒感染细胞等）。
    *   **对比与整合**：提供清晰的对比，帮助用户区分两种免疫方式的特点，并最终整合到完整的免疫应答图景中。
3.  **学习痛点**：传统教材中的静态图表难以表现动态过程；学生对“协同”的理解停留在文字描述，缺乏直观感受；记忆点多，容易混淆。

#### 教学设计思路
*   **核心概念**：
    *   **体液免疫**：B细胞识别抗原→活化、增殖分化为浆细胞和记忆B细胞→浆细胞产生特异性抗体→抗体中和、调理病原体。
    *   **细胞免疫**：抗原呈递细胞（APC）处理并呈递抗原→激活细胞毒性T细胞（Tc）和辅助T细胞（Th）→Tc识别并杀伤被感染的靶细胞。
    *   **协同核心**：辅助T细胞（Th）是桥梁。它被APC激活后，一方面分泌细胞因子（如白细胞介素）辅助B细胞活化（体液免疫），另一方面辅助Tc细胞的完全活化（细胞免疫）。
*   **认知规律**：
    1.  **分层递进**：动画将分阶段展开。先分别介绍体液免疫和细胞免疫的基本流程，确保用户对各自路径有清晰认识。
    2.  **对比强化**：在分述时，采用并排或切换视图，突出两者在作用对象（胞外病原体 vs. 受感染细胞）、效应分子（抗体 vs. 效应T细胞）、记忆细胞等方面的差异。
    3.  **整合与协同**：在单独路径演示后，引入一个复杂的感染场景（如病毒入侵），动态展示两条路径如何被同时启动，并通过Th细胞交汇、协作，最终共同清除威胁。
    4.  **交互探索**：允许用户控制播放节奏，点击关键细胞或分子查看详细说明，甚至选择不同的病原体类型来观察免疫系统的侧重反应。
*   **交互设计**：
    *   **叙事模式**：提供“自动播放”的引导式教学动画，配有语音或文字解说。
    *   **探索模式**：允许用户自由点击场景中的免疫细胞、分子，弹出信息卡（名称、功能）。
    *   **控制面板**：播放/暂停/进度条、重置按钮。可能包含“仅显示体液免疫”、“仅显示细胞免疫”、“显示协同”的视图切换开关。
    *   **挑战/测试环节**：可设置简单的拖拽题（如将细胞拖到正确的作用位置）或选择题，即时反馈，巩固学习效果。
*   **视觉呈现**：
    *   **风格**：采用简洁、扁平的卡通化设计，避免过于复杂的细节干扰认知。关键结构（如抗原与受体的结合）可适当夸张。
    *   **动态**：运动平滑，路径清晰。用“脉冲光”或“连接线”表示激活信号，用“气泡”表示分子分泌，用“爆炸”或“溶解”表示细胞被杀伤。
    *   **布局**：主画布居中。初期可分左右两栏对比演示，协同阶段合并为统一场景。侧边栏或浮动框用于显示说明文字和图例。

#### 配色方案选择
*   **主色调**：采用柔和、专业的蓝绿色系，营造科学、清晰的氛围。
*   **区分配色**：
    *   **病原体**：使用醒目的**红色**或**橙色**（代表危险、外来），如红色病毒颗粒、橙色细菌。
    *   **体液免疫线**：使用**蓝色系**。B细胞、抗体用不同明度的蓝色。
    *   **细胞免疫线**：使用**绿色系**。T细胞（Tc, Th）、APC用不同明度的绿色。
    *   **关键连接元素**：**辅助T细胞（Th）** 使用**紫色**，象征其连接和调节功能。其分泌的**细胞因子**可用**亮黄色**光点或箭头表示，突出其信号作用。
    *   **背景与组织**：使用非常浅的灰色或米白色，突出前景元素。
    *   **记忆细胞**：可在原色基础上添加**金色边框**或光晕，以示特殊。

#### 交互功能列表
1.  **主流程控制**：播放、暂停、重置、进度拖动。
2.  **视图切换**：按钮或选项卡，用于在“体液免疫”、“细胞免疫”、“双系统协同”三个主要场景间切换。
3.  **信息提示**：
    *   鼠标悬停在任何细胞、分子上时，高亮显示并显示其名称。
    *   点击关键元素（如活化的Th细胞、抗体），弹出详细信息卡片（功能、重要性）。
4.  **步骤控制**：在自动播放模式下，可以点击“上一步”、“下一步”进行分步学习。
5.  **图例开关**：一个可开关的图例面板，解释不同颜色和形状代表的元素。
6.  **（进阶）情景选择**：选择不同的感染类型（如“细菌感染”、“病毒感染”），观察免疫应答的侧重点变化。
7.  **（进阶）知识测验**：在动画结束后，提供3-5道互动选择题或匹配题，检验学习成果。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>体液免疫与细胞免疫的双系统协同动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
            color: #333;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .header {
            text-align: center;
            margin-bottom: 20px;
            width: 100%;
            max-width: 1200px;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }
        
        .subtitle {
            color: #5a6c7d;
            font-size: 1.1rem;
            margin-bottom: 25px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.5;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            width: 100%;
            max-width: 1200px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            margin-bottom: 25px;
        }
        
        .animation-area {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #f8fafc;
            border-bottom: 1px solid #e2e8f0;
            overflow: hidden;
        }
        
        #immuneCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .controls {
            padding: 20px;
            background-color: #f8fafc;
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            align-items: center;
            justify-content: center;
            border-bottom: 1px solid #e2e8f0;
        }
        
        .view-controls {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            justify-content: center;
        }
        
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .btn-primary {
            background-color: #4f8cff;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #3a7cff;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(79, 140, 255, 0.3);
        }
        
        .btn-secondary {
            background-color: #e9ecef;
            color: #495057;
        }
        
        .btn-secondary:hover {
            background-color: #dee2e6;
            transform: translateY(-2px);
        }
        
        .btn-active {
            box-shadow: inset 0 0 0 2px currentColor;
        }
        
        .view-btn {
            padding: 8px 16px;
        }
        
        #humoralBtn {
            color: #2d7dd2;
            background-color: #e3f2fd;
        }
        
        #cellularBtn {
            color: #2ecc71;
            background-color: #e8f8ef;
        }
        
        #combinedBtn {
            color: #9b59b6;
            background-color: #f3e5f5;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
            flex: 1;
            max-width: 400px;
            min-width: 250px;
        }
        
        #speedSlider {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            appearance: none;
            background: #d1d9e6;
            border-radius: 4px;
            outline: none;
        }
        
        #speedSlider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #4f8cff;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        .info-panel {
            padding: 25px;
            background-color: white;
        }
        
        .info-title {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.4rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .info-content {
            line-height: 1.6;
            color: #4a5568;
            font-size: 1.05rem;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding: 15px;
            background-color: #f8fafc;
            border-radius: 10px;
            justify-content: center;
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
            border-radius: 50%;
        }
        
        .tooltip {
            position: absolute;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 8px;
            padding: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15);
            max-width: 300px;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 100;
            border-left: 4px solid #4f8cff;
        }
        
        .tooltip-title {
            font-weight: bold;
            margin-bottom: 5px;
            color: #2c3e50;
        }
        
        .tooltip-desc {
            font-size: 0.9rem;
            color: #5a6c7d;
            line-height: 1.4;
        }
        
        .footer {
            text-align: center;
            color: #718096;
            font-size: 0.9rem;
            margin-top: 10px;
            width: 100%;
            max-width: 1200px;
        }
        
        @media (max-width: 768px) {
            .container {
                border-radius: 10px;
            }
            
            .animation-area {
                height: 400px;
            }
            
            .controls {
                flex-direction: column;
                align-items: stretch;
            }
            
            .slider-container {
                max-width: 100%;
            }
            
            h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>体液免疫与细胞免疫的双系统协同</h1>
        <p class="subtitle">本动画展示了免疫系统中体液免疫（抗体介导）和细胞免疫（T细胞介导）的独立作用机制以及它们如何协同工作，共同抵御病原体入侵。</p>
    </div>
    
    <div class="container">
        <div class="animation-area">
            <canvas id="immuneCanvas"></canvas>
            <div class="tooltip" id="tooltip"></div>
        </div>
        
        <div class="controls">
            <div class="view-controls">
                <button id="humoralBtn" class="view-btn btn-active">
                    <span>体液免疫</span>
                </button>
                <button id="cellularBtn" class="view-btn">
                    <span>细胞免疫</span>
                </button>
                <button id="combinedBtn" class="view-btn">
                    <span>双系统协同</span>
                </button>
            </div>
            
            <div class="slider-container">
                <span>速度:</span>
                <input type="range" id="speedSlider" min="0.5" max="3" step="0.1" value="1">
                <span id="speedValue">1.0x</span>
            </div>
            
            <button id="playPauseBtn" class="btn-primary">
                <span id="playIcon">▶</span>
                <span id="playText">播放</span>
            </button>
            
            <button id="resetBtn" class="btn-secondary">
                <span>重置</span>
            </button>
        </div>
        
        <div class="info-panel">
            <div class="info-title">
                <span id="currentViewTitle">体液免疫</span>
            </div>
            <div class="info-content" id="currentViewDescription">
                体液免疫主要针对细胞外的病原体，如细菌和病毒。B细胞识别抗原后，在辅助T细胞的帮助下活化、增殖并分化为浆细胞和记忆B细胞。浆细胞产生大量特异性抗体，抗体与病原体结合，通过中和、调理作用等方式清除病原体。
            </div>
        </div>
        
        <div class="legend">
            <div class="legend-item">
                <div class="legend-color" style="background-color: #e74c3c;"></div>
                <span>病原体 (病毒/细菌)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #3498db;"></div>
                <span>B细胞 / 抗体</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #2ecc71;"></div>
                <span>T细胞 (Tc/Th)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #9b59b6;"></div>
                <span>辅助T细胞 (Th)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #f1c40f;"></div>
                <span>细胞因子 (信号分子)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #e67e22;"></div>
                <span>抗原呈递细胞 (APC)</span>
            </div>
        </div>
    </div>
    
    <div class="footer">
        <p>教学动画 | 免疫系统 | 体液免疫与细胞免疫协同作用</p>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const canvas = document.getElementById('immuneCanvas');
        const ctx = canvas.getContext('2d');
        const tooltip = document.getElementById('tooltip');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
        }
        
        // 初始调整尺寸
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 动画状态
        let animationId = null;
        let isPlaying = false;
        let animationSpeed = 1.0;
        let currentView = 'humoral'; // 'humoral', 'cellular', 'combined'
        let time = 0;
        
        // 视图描述信息
        const viewInfo = {
            humoral: {
                title: '体液免疫',
                description: '体液免疫主要针对细胞外的病原体，如细菌和病毒。B细胞识别抗原后，在辅助T细胞的帮助下活化、增殖并分化为浆细胞和记忆B细胞。浆细胞产生大量特异性抗体，抗体与病原体结合，通过中和、调理作用等方式清除病原体。'
            },
            cellular: {
                title: '细胞免疫',
                description: '细胞免疫主要针对细胞内病原体（如病毒感染的细胞）和癌细胞。抗原呈递细胞(APC)处理并呈递抗原，激活细胞毒性T细胞(Tc)和辅助T细胞(Th)。活化的Tc细胞识别并杀伤被感染的靶细胞，而Th细胞分泌细胞因子调节免疫应答。'
            },
            combined: {
                title: '双系统协同',
                description: '在实际免疫应答中，体液免疫和细胞免疫协同工作。辅助T细胞(Th)是关键的协调者：它被APC激活后，一方面分泌细胞因子帮助B细胞活化（体液免疫），另一方面帮助Tc细胞完全活化（细胞免疫）。这种协同确保了对各种病原体的全面清除。'
            }
        };
        
        // 动画元素定义
        const elements = {
            pathogens: [],
            bCells: [],
            antibodies: [],
            tCells: [],
            helperTCells: [],
            apcs: [],
            cytokines: [],
            infectedCells: [],
            memoryCells: []
        };
        
        // 颜色定义
        const colors = {
            pathogen: '#e74c3c',
            bCell: '#3498db',
            antibody: '#2980b9',
            tCell: '#2ecc71',
            helperTCell: '#9b59b6',
            apc: '#e67e22',
            cytokine: '#f1c40f',
            infectedCell: '#e74c3c',
            memoryCell: '#f39c12',
            background: '#f8fafc',
            tissue: '#e8f4f8',
            bloodVessel: '#a5d8ff'
        };
        
        // 初始化动画元素
        function initElements() {
            // 清空所有元素
            for (let key in elements) {
                elements[key] = [];
            }
            
            // 根据当前视图初始化元素
            if (currentView === 'humoral' || currentView === 'combined') {
                // 添加病原体（细菌/病毒）
                for (let i = 0; i < 8; i++) {
                    elements.pathogens.push({
                        x: 100 + Math.random() * (canvas.width - 200),
                        y: 100 + Math.random() * (canvas.height - 200),
                        radius: 8 + Math.random() * 6,
                        type: Math.random() > 0.5 ? 'bacteria' : 'virus',
                        speed: 0.5 + Math.random() * 0.5,
                        angle: Math.random() * Math.PI * 2,
                        neutralized: false,
                        neutralizedTime: 0
                    });
                }
                
                // 添加B细胞
                for (let i = 0; i < 4; i++) {
                    elements.bCells.push({
                        x: 150 + i * 80,
                        y: canvas.height - 150,
                        radius: 15,
                        state: 'inactive', // inactive, activated, dividing, plasma
                        activationProgress: 0,
                        targetPathogen: null,
                        divisionProgress: 0,
                        antibodiesProduced: 0
                    });
                }
                
                // 添加辅助T细胞（紫色）
                elements.helperTCells.push({
                    x: canvas.width / 2,
                    y: canvas.height / 2 + 50,
                    radius: 16,
                    state: 'inactive', // inactive, activated, signaling
                    activationProgress: 0,
                    signalTarget: null
                });
            }
            
            if (currentView === 'cellular' || currentView === 'combined') {
                // 添加被感染的细胞
                for (let i = 0; i < 5; i++) {
                    elements.infectedCells.push({
                        x: canvas.width - 150 - i * 70,
                        y: 150 + Math.random() * 50,
                        radius: 20,
                        infectionProgress: 0.3 + Math.random() * 0.7,
                        beingAttacked: false,
                        destructionProgress: 0
                    });
                }
                
                // 添加细胞毒性T细胞
                for (let i = 0; i < 3; i++) {
                    elements.tCells.push({
                        x: 150 + i * 100,
                        y: canvas.height - 100,
                        radius: 14,
                        state: 'inactive', // inactive, activated, attacking
                        activationProgress: 0,
                        targetCell: null,
                        attackProgress: 0
                    });
                }
                
                // 添加抗原呈递细胞
                elements.apcs.push({
                    x: canvas.width / 2 - 100,
                    y: canvas.height / 2 - 50,
                    radius: 18,
                    state: 'inactive', // inactive, presenting, migrating
                    antigen: null,
                    migrationProgress: 0,
                    target: null
                });
                
                // 在协同视图中，共享辅助T细胞
                if (currentView === 'cellular') {
                    elements.helperTCells.push({
                        x: canvas.width / 2,
                        y: canvas.height / 2 + 50,
                        radius: 16,
                        state: 'inactive',
                        activationProgress: 0,
                        signalTarget: null
                    });
                }
            }
        }
        
        // 绘制圆形元素
        function drawCircle(x, y, radius, color, label = '') {
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.fillStyle = color;
            ctx.fill();
            
            if (label) {
                ctx.fillStyle = 'white';
                ctx.font = 'bold 12px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(label, x, y);
            }
        }
        
        // 绘制抗体（Y形）
        function drawAntibody(x, y, size, color, angle = 0) {
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(angle);
            
            ctx.beginPath();
            ctx.moveTo(0, -size);
            ctx.lineTo(0, size);
            
            ctx.moveTo(-size/2, -size/2);
            ctx.lineTo(size/2, -size/2);
            
            ctx.moveTo(-size/2, size/2);
            ctx.lineTo(size/2, size/2);
            
            ctx.strokeStyle = color;
            ctx.lineWidth = 2;
            ctx.stroke();
            
            ctx.restore();
        }
        
        // 绘制细胞因子（小点）
        function drawCytokine(x, y, size, color) {
            ctx.beginPath();
            ctx.arc(x, y, size, 0, Math.PI * 2);
            ctx.fillStyle = color;
            ctx.fill();
            
            // 添加发光效果
            ctx.beginPath();
            ctx.arc(x, y, size * 1.5, 0, Math.PI * 2);
            const gradient = ctx.createRadialGradient(x, y, size, x, y, size * 1.5);
            gradient.addColorStop(0, color + '80');
            gradient.addColorStop(1, color + '00');
            ctx.fillStyle = gradient;
            ctx.fill();
        }
        
        // 绘制连接线（表示相互作用）
        function drawConnection(x1, y1, x2, y2, color, width = 2, dashed = false) {
            ctx.beginPath();
            ctx.moveTo(x1, y1);
            ctx.lineTo(x2, y2);
            ctx.strokeStyle = color;
            ctx.lineWidth = width;
            
            if (dashed) {
                ctx.setLineDash([5, 5]);
            } else {
                ctx.setLineDash([]);
            }
            
            ctx.stroke();
            ctx.setLineDash([]);
        }
        
        // 绘制组织背景
        function drawBackground() {
            // 绘制背景颜色
            ctx.fillStyle = colors.background;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制组织纹理（简单表示）
            ctx.fillStyle = colors.tissue + '20';
            for (let i = 0; i < 20; i++) {
                const x = Math.random() * canvas.width;
                const y = Math.random() * canvas.height;
                const radius = 30 + Math.random() * 50;
                
                ctx.beginPath();
                ctx.arc(x, y, radius, 0, Math.PI * 2);
                ctx.fill();
            }
            
            // 绘制血管（简单表示）
            ctx.strokeStyle = colors.bloodVessel + '40';
            ctx.lineWidth = 15;
            ctx.beginPath();
            ctx.moveTo(0, canvas.height / 3);
            ctx.bezierCurveTo(canvas.width / 4, canvas.height / 4, canvas.width * 3/4, canvas.height / 2, canvas.width, canvas.height / 3);
            ctx.stroke();
            
            ctx.beginPath();
            ctx.moveTo(0, canvas.height * 2/3);
            ctx.bezierCurveTo(canvas.width / 3, canvas.height * 3/4, canvas.width * 2/3, canvas.height * 3/4, canvas.width, canvas.height * 2/3);
            ctx.stroke();
        }
        
        // 更新动画逻辑
        function updateAnimation() {
            time += 0.02 * animationSpeed;
            
            // 更新病原体
            elements.pathogens.forEach(pathogen => {
                if (!pathogen.neutralized) {
                    // 移动病原体
                    pathogen.x += Math.cos(pathogen.angle) * pathogen.speed * animationSpeed;
                    pathogen.y += Math.sin(pathogen.angle) * pathogen.speed * animationSpeed;
                    
                    // 边界反弹
                    if (pathogen.x < pathogen.radius || pathogen.x > canvas.width - pathogen.radius) {
                        pathogen.angle = Math.PI - pathogen.angle;
                    }
                    if (pathogen.y < pathogen.radius || pathogen.y > canvas.height - pathogen.radius) {
                        pathogen.angle = -pathogen.angle;
                    }
                    
                    // 随机改变方向
                    if (Math.random() < 0.02) {
                        pathogen.angle += (Math.random() - 0.5) * 0.5;
                    }
                } else {
                    pathogen.neutralizedTime += 0.02 * animationSpeed;
                }
            });
            
            // 更新B细胞和抗体（体液免疫）
            if (currentView === 'humoral' || currentView === 'combined') {
                elements.bCells.forEach((bCell, index) => {
                    if (bCell.state === 'inactive') {
                        // 寻找病原体
                        if (time > 1 + index * 0.5) {
                            const pathogen = elements.pathogens.find(p => !p.neutralized);
                            if (pathogen) {
                                bCell.targetPathogen = pathogen;
                                bCell.state = 'activating';
                            }
                        }
                    } else if (bCell.state === 'activating') {
                        bCell.activationProgress += 0.01 * animationSpeed;
                        
                        // 需要辅助T细胞激活
                        const helperT = elements.helperTCells[0];
                        if (helperT && helperT.state === 'activated' && bCell.activationProgress > 0.5) {
                            // 辅助T细胞帮助激活B细胞
                            if (helperT.signalTarget === null) {
                                helperT.signalTarget = bCell;
                                helperT.state = 'signaling';
                            }
                            
                            if (bCell.activationProgress >= 1) {
                                bCell.state = 'dividing';
                                bCell.activationProgress = 0;
                            }
                        }
                    } else if (bCell.state === 'dividing') {
                        bCell.divisionProgress += 0.015 * animationSpeed;
                        
                        if (bCell.divisionProgress >= 1) {
                            bCell.state = 'plasma';
                            bCell.divisionProgress = 0;
                            
                            // 创建记忆B细胞
                            elements.memoryCells.push({
                                x: bCell.x + 40,
                                y: bCell.y,
                                radius: 12,
                                type: 'bMemory'
                            });
                        }
                    } else if (bCell.state === 'plasma') {
                        // 产生抗体
                        if (time % 0.5 < 0.1) {
                            elements.antibodies.push({
                                x: bCell.x,
                                y: bCell.y,
                                size: 6,
                                angle: Math.random() * Math.PI * 2,
                                speed: 2 + Math.random(),
                                target: bCell.targetPathogen,
                                attached: false
                            });
                            bCell.antibodiesProduced++;
                        }
                    }
                });
                
                // 更新抗体
                elements.antibodies.forEach((antibody, index) => {
                    if (!antibody.attached && antibody.target) {
                        // 向目标病原体移动
                        const dx = antibody.target.x - antibody.x;
                        const dy = antibody.target.y - antibody.y;
                        const distance = Math.sqrt(dx * dx + dy * dy);
                        
                        if (distance < 5) {
                            // 附着到病原体
                            antibody.attached = true;
                            if (antibody.target && !antibody.target.neutralized) {
                                antibody.target.neutralized = true;
                            }
                        } else {
                            // 移动抗体
                            antibody.x += (dx / distance) * antibody.speed * animationSpeed;
                            antibody.y += (dy / distance) * antibody.speed * animationSpeed;
                            antibody.angle = Math.atan2(dy, dx);
                        }
                    }
                });
                
                // 更新辅助T细胞
                elements.helperTCells.forEach(helperT => {
                    if (helperT.state === 'inactive' && time > 0.5) {
                        // 被APC激活（在协同视图中）
                        if (currentView === 'combined') {
                            const apc = elements.apcs[0];
                            if (apc && apc.state === 'presenting') {
                                helperT.state = 'activating';
                                apc.target = helperT;
                            }
                        } else {
                            // 在体液免疫视图中自动激活
                            helperT.state = 'activating';
                        }
                    } else if (helperT.state === 'activating') {
                        helperT.activationProgress += 0.01 * animationSpeed;
                        if (helperT.activationProgress >= 1) {
                            helperT.state = 'activated';
                            helperT.activationProgress = 0;
                        }
                    } else if (helperT.state === 'signaling') {
                        // 向B细胞发送信号
                        if (helperT.signalTarget) {
                            // 创建细胞因子信号
                            if (time % 0.3 < 0.1) {
                                elements.cytokines.push({
                                    x: helperT.x,
                                    y: helperT.y,
                                    size: 3,
                                    target: helperT.signalTarget,
                                    progress: 0,
                                    speed: 1.5
                                });
                            }
                        }
                    }
                });
            }
            
            // 更新细胞免疫元素
            if (currentView === 'cellular' || currentView === 'combined') {
                // 更新抗原呈递细胞
                elements.apcs.forEach(apc => {
                    if (apc.state === 'inactive' && time > 0.3) {
                        // 寻找被感染的细胞
                        const infectedCell = elements.infectedCells.find(cell => cell.infectionProgress > 0.5);
                        if (infectedCell) {
                            apc.state = 'migrating';
                            apc.target = infectedCell;
                        }
                    } else if (apc.state === 'migrating' && apc.target) {
                        // 向被感染细胞移动
                        const dx = apc.target.x - apc.x;
                        const dy = apc.target.y - apc.y;
                        const distance = Math.sqrt(dx * dx + dy * dy);
                        
                        if (distance < 10) {
                            // 到达目标，开始呈递抗原
                            apc.state = 'presenting';
                            apc.antigen = apc.target;
                            apc.migrationProgress = 0;
                        } else {
                            // 移动APC
                            apc.x += (dx / distance) * 1.5 * animationSpeed;
                            apc.y += (dy / distance) * 1.5 * animationSpeed;
                            apc.migrationProgress += 0.01 * animationSpeed;
                        }
                    } else if (apc.state === 'presenting') {
                        // 呈递抗原，激活T细胞
                        if (currentView === 'combined') {
                            // 在协同视图中，激活辅助T细胞
                            const helperT = elements.helperTCells[0];
                            if (helperT && helperT.state === 'inactive') {
                                helperT.state = 'activating';
                            }
                        }
                        
                        // 激活细胞毒性T细胞
                        const inactiveTCell = elements.tCells.find(t => t.state === 'inactive');
                        if (inactiveTCell && time % 1 < 0.1) {
                            inactiveTCell.state = 'activating';
                            inactiveTCell.target = apc;
                        }
                    }
                });
                
                // 更新细胞毒性T细胞
                elements.tCells.forEach(tCell => {
                    if (tCell.state === 'activating') {
                        tCell.activationProgress += 0.01 * animationSpeed;
                        
                        // 需要辅助T细胞激活（在协同视图中）
                        if (currentView === 'combined') {
                            const helperT = elements.helperTCells[0];
                            if (helperT && helperT.state === 'activated' && tCell.activationProgress > 0.5) {
                                if (helperT.signalTarget === null) {
                                    helperT.signalTarget = tCell;
                                    helperT.state = 'signaling';
                                }
                            }
                        }
                        
                        if (tCell.activationProgress >= 1) {
                            tCell.state = 'attacking';
                            tCell.activationProgress = 0;
                            
                            // 寻找被感染细胞作为目标
                            const infectedCell = elements.infectedCells.find(cell => !cell.beingAttacked && cell.infectionProgress > 0.3);
                            if (infectedCell) {
                                tCell.targetCell = infectedCell;
                                infectedCell.beingAttacked = true;
                            }
                        }
                    } else if (tCell.state === 'attacking' && tCell.targetCell) {
                        // 向目标细胞移动
                        const dx = tCell.targetCell.x - tCell.x;
                        const dy = tCell.targetCell.y - tCell.y;
                        const distance = Math.sqrt(dx * dx + dy * dy);
                        
                        if (distance < 15) {
                            // 攻击目标细胞
                            tCell.attackProgress += 0.02 * animationSpeed;
                            tCell.targetCell.destructionProgress += 0.015 * animationSpeed;
                            
                            if (tCell.targetCell.destructionProgress >= 1) {
                                // 目标细胞被摧毁
                                tCell.state = 'inactive';
                                tCell.targetCell = null;
                                tCell.attackProgress = 0;
                            }
                        } else {
                            // 移动T细胞
                            tCell.x += (dx / distance) * 2 * animationSpeed;
                            tCell.y += (dy / distance) * 2 * animationSpeed;
                        }
                    }
                });
                
                // 更新被感染细胞
                elements.infectedCells.forEach(cell => {
                    if (cell.infectionProgress < 1 && !cell.beingAttacked) {
                        cell.infectionProgress += 0.002 * animationSpeed;
                    }
                });
            }
            
            // 更新细胞因子
            elements.cytokines.forEach((cytokine, index) => {
                cytokine.progress += 0.03 * animationSpeed * cytokine.speed;
                
                if (cytokine.progress >= 1) {
                    // 到达目标，移除细胞因子
                    elements.cytokines.splice(index, 1);
                }
            });
            
            // 清理中和时间过长的病原体
            elements.pathogens = elements.pathogens.filter(p => !p.neutralized || p.neutralizedTime < 3);
            
            // 清理到达目标的抗体
            elements.antibodies = elements.antibodies.filter(a => !a.attached || Math.random() > 0.01);
        }
        
        // 绘制动画
        function drawAnimation() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 绘制被感染的细胞（细胞免疫）
            if (currentView === 'cellular' || currentView === 'combined') {
                elements.infectedCells.forEach(cell => {
                    const color = cell.beingAttacked ? 
                        `rgba(231, 76, 60, ${0.7 - cell.destructionProgress * 0.5})` : 
                        `rgba(231, 76, 60, ${0.3 + cell.infectionProgress * 0.5})`;
                    
                    drawCircle(cell.x, cell.y, cell.radius, color, cell.beingAttacked ? '💀' : '🦠');
                    
                    // 绘制感染进度条
                    if (cell.infectionProgress > 0 && cell.infectionProgress < 1) {
                        ctx.beginPath();
                        ctx.arc(cell.x, cell.y, cell.radius + 5, 0, Math.PI * 2 * cell.infectionProgress);
                        ctx.strokeStyle = colors.infectedCell;
                        ctx.lineWidth = 3;
                        ctx.stroke();
                    }
                    
                    // 绘制破坏进度
                    if (cell.destructionProgress > 0) {
                        ctx.beginPath();
                        ctx.arc(cell.x, cell.y, cell.radius * (1 - cell.destructionProgress * 0.5), 0, Math.PI * 2);
                        ctx.strokeStyle = '#2ecc71';
                        ctx.lineWidth = 2;
                        ctx.setLineDash([3, 3]);
                        ctx.stroke();
                        ctx.setLineDash([]);
                    }
                });
            }
            
            // 绘制病原体（体液免疫）
            if (currentView === 'humoral' || currentView === 'combined') {
                elements.pathogens.forEach(pathogen => {
                    const color = pathogen.neutralized ? 
                        `rgba(231, 76, 60, ${0.3 - pathogen.neutralizedTime * 0.1})` : 
                        colors.pathogen;
                    
                    drawCircle(pathogen.x, pathogen.y, pathogen.radius, color, pathogen.type === 'bacteria' ? '🦠' : '🦠');
                    
                    // 如果被中和，绘制抗体附着
                    if (pathogen.neutralized) {
                        for (let i = 0; i < 3; i++) {
                            const angle = pathogen.neutralizedTime + i * Math.PI/3;
                            drawAntibody(
                                pathogen.x + Math.cos(angle) * pathogen.radius * 1.2,
                                pathogen.y + Math.sin(angle) * pathogen.radius * 1.2,
                                4, colors.antibody, angle
                            );
                        }
                    }
                });
            }
            
            // 绘制B细胞和抗体（体液免疫）
            if (currentView === 'humoral' || currentView === 'combined') {
                // 绘制抗体
                elements.antibodies.forEach(antibody => {
                    if (!antibody.attached) {
                        drawAntibody(antibody.x, antibody.y, antibody.size, colors.antibody, antibody.angle);
                    }
                });
                
                // 绘制B细胞
                elements.bCells.forEach(bCell => {
                    let color = colors.bCell;
                    let label = 'B';
                    
                    if (bCell.state === 'activating') {
                        color = `rgba(52, 152, 219, ${0.5 + bCell.activationProgress * 0.5})`;
                        label = 'B*';
                        
                        // 绘制激活脉冲
                        ctx.beginPath();
                        ctx.arc(bCell.x, bCell.y, bCell.radius * (1 + bCell.activationProgress * 2), 0, Math.PI * 2);
                        ctx.strokeStyle = `rgba(52, 152, 219, ${0.3
<!--检测到代码截断，自动续写中...-->
- bCell.activationProgress * 0.2})`;
                        ctx.lineWidth = 2;
                        ctx.stroke();
                    } else if (bCell.state === 'dividing') {
                        color = `rgba(41, 128, 185, ${0.7 + Math.sin(time*10)*0.3})`;
                        label = 'B÷';
                        
                        // 绘制分裂效果
                        const splitOffset = bCell.divisionProgress * 20;
                        drawCircle(bCell.x - splitOffset/2, bCell.y, bCell.radius, color, 'B');
                        drawCircle(bCell.x + splitOffset/2, bCell.y, bCell.radius, color, 'B');
                        
                        // 连接线表示分裂过程
                        drawConnection(bCell.x - splitOffset/2, bCell.y, bCell.x + splitOffset/2, bCell.y, color, 2, true);
                        return; // 跳过下面的标准绘制
                    } else if (bCell.state === 'plasma') {
                        color = colors.antibody;
                        label = 'P';
                        
                        // 绘制抗体产生效果
                        if (time % 0.5 < 0.25) {
                            ctx.beginPath();
                            ctx.arc(bCell.x, bCell.y, bCell.radius * 1.5, 0, Math.PI * 2);
                            ctx.strokeStyle = `rgba(41, 128, 185, 0.3)`;
                            ctx.lineWidth = 1;
                            ctx.stroke();
                        }
                    }
                    
                    drawCircle(bCell.x, bCell.y, bCell.radius, color, label);
                    
                    // 如果B细胞有目标病原体，绘制连接线
                    if (bCell.targetPathogen && !bCell.targetPathogen.neutralized) {
                        drawConnection(bCell.x, bCell.y, bCell.targetPathogen.x, bCell.targetPathogen.y, colors.bCell, 1, true);
                    }
                });
                
                // 绘制记忆B细胞
                elements.memoryCells.forEach(cell => {
                    drawCircle(cell.x, cell.y, cell.radius, colors.memoryCell, 'M');
                    
                    // 添加金色边框表示记忆细胞
                    ctx.beginPath();
                    ctx.arc(cell.x, cell.y, cell.radius + 2, 0, Math.PI * 2);
                    ctx.strokeStyle = '#f39c12';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                });
            }
            
            // 绘制细胞免疫元素
            if (currentView === 'cellular' || currentView === 'combined') {
                // 绘制抗原呈递细胞
                elements.apcs.forEach(apc => {
                    let color = colors.apc;
                    let label = 'APC';
                    
                    if (apc.state === 'migrating') {
                        color = `rgba(230, 126, 34, ${0.6 + Math.sin(time*5)*0.2})`;
                        
                        // 绘制迁移轨迹
                        if (apc.target) {
                            drawConnection(apc.x, apc.y, apc.target.x, apc.target.y, colors.apc, 1, true);
                        }
                    } else if (apc.state === 'presenting') {
                        color = `rgba(230, 126, 34, ${0.8 + Math.sin(time*8)*0.2})`;
                        label = 'APC*';
                        
                        // 绘制抗原呈递效果
                        ctx.beginPath();
                        ctx.arc(apc.x, apc.y, apc.radius * 1.3, 0, Math.PI * 2);
                        ctx.strokeStyle = `rgba(230, 126, 34, 0.4)`;
                        ctx.lineWidth = 2;
                        ctx.stroke();
                    }
                    
                    drawCircle(apc.x, apc.y, apc.radius, color, label);
                    
                    // 如果APC有抗原，绘制小抗原点
                    if (apc.antigen) {
                        drawCircle(apc.x + 10, apc.y - 10, 5, colors.pathogen, '');
                    }
                });
                
                // 绘制细胞毒性T细胞
                elements.tCells.forEach(tCell => {
                    let color = colors.tCell;
                    let label = 'Tc';
                    
                    if (tCell.state === 'activating') {
                        color = `rgba(46, 204, 113, ${0.5 + tCell.activationProgress * 0.5})`;
                        label = 'Tc*';
                        
                        // 绘制激活效果
                        ctx.beginPath();
                        ctx.arc(tCell.x, tCell.y, tCell.radius * (1 + tCell.activationProgress * 2), 0, Math.PI * 2);
                        ctx.strokeStyle = `rgba(46, 204, 113, ${0.3 - tCell.activationProgress * 0.2})`;
                        ctx.lineWidth = 2;
                        ctx.stroke();
                        
                        // 如果正在被辅助T细胞激活，绘制连接线
                        if (currentView === 'combined') {
                            const helperT = elements.helperTCells[0];
                            if (helperT && helperT.signalTarget === tCell) {
                                drawConnection(helperT.x, helperT.y, tCell.x, tCell.y, colors.helperTCell, 1, true);
                            }
                        }
                    } else if (tCell.state === 'attacking') {
                        color = '#27ae60';
                        label = 'Tc⚔';
                        
                        // 绘制攻击效果
                        if (tCell.targetCell) {
                            drawConnection(tCell.x, tCell.y, tCell.targetCell.x, tCell.targetCell.y, '#27ae60', 2);
                            
                            // 攻击动画
                            if (tCell.attackProgress > 0) {
                                const pulseSize = tCell.radius * (1 + Math.sin(time*20)*0.3);
                                ctx.beginPath();
                                ctx.arc(tCell.x, tCell.y, pulseSize, 0, Math.PI * 2);
                                ctx.strokeStyle = `rgba(39, 174, 96, ${0.5})`;
                                ctx.lineWidth = 2;
                                ctx.stroke();
                            }
                        }
                    }
                    
                    drawCircle(tCell.x, tCell.y, tCell.radius, color, label);
                });
            }
            
            // 绘制辅助T细胞（共享元素）
            elements.helperTCells.forEach(helperT => {
                let color = colors.helperTCell;
                let label = 'Th';
                
                if (helperT.state === 'activating') {
                    color = `rgba(155, 89, 182, ${0.5 + helperT.activationProgress * 0.5})`;
                    label = 'Th*';
                    
                    // 绘制激活效果
                    ctx.beginPath();
                    ctx.arc(helperT.x, helperT.y, helperT.radius * (1 + helperT.activationProgress * 2), 0, Math.PI * 2);
                    ctx.strokeStyle = `rgba(155, 89, 182, ${0.3 - helperT.activationProgress * 0.2})`;
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // 在协同视图中，如果被APC激活，绘制连接线
                    if (currentView === 'combined') {
                        const apc = elements.apcs[0];
                        if (apc && apc.target === helperT) {
                            drawConnection(apc.x, apc.y, helperT.x, helperT.y, colors.apc, 1, true);
                        }
                    }
                } else if (helperT.state === 'activated') {
                    color = '#8e44ad';
                    label = 'Th*';
                    
                    // 激活状态脉冲
                    ctx.beginPath();
                    ctx.arc(helperT.x, helperT.y, helperT.radius * (1.2 + Math.sin(time*6)*0.3), 0, Math.PI * 2);
                    ctx.strokeStyle = `rgba(142, 68, 173, 0.3)`;
                    ctx.lineWidth = 2;
                    ctx.stroke();
                } else if (helperT.state === 'signaling' && helperT.signalTarget) {
                    color = '#8e44ad';
                    label = 'Th→';
                    
                    // 绘制信号传递
                    drawConnection(helperT.x, helperT.y, helperT.signalTarget.x, helperT.signalTarget.y, colors.helperTCell, 2, false);
                }
                
                drawCircle(helperT.x, helperT.y, helperT.radius, color, label);
            });
            
            // 绘制细胞因子
            elements.cytokines.forEach(cytokine => {
                if (cytokine.target) {
                    // 计算当前位置
                    const x = cytokine.x + (cytokine.target.x - cytokine.x) * cytokine.progress;
                    const y = cytokine.y + (cytokine.target.y - cytokine.y) * cytokine.progress;
                    
                    drawCytokine(x, y, cytokine.size, colors.cytokine);
                    
                    // 绘制轨迹
                    ctx.beginPath();
                    ctx.moveTo(cytokine.x, cytokine.y);
                    ctx.lineTo(x, y);
                    ctx.strokeStyle = colors.cytokine + '60';
                    ctx.lineWidth = 1;
                    ctx.setLineDash([2, 2]);
                    ctx.stroke();
                    ctx.setLineDash([]);
                }
            });
            
            // 绘制视图标题
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'left';
            ctx.textBaseline = 'top';
            
            let viewTitle = '';
            if (currentView === 'humoral') viewTitle = '体液免疫 (抗体介导)';
            else if (currentView === 'cellular') viewTitle = '细胞免疫 (T细胞介导)';
            else viewTitle = '双系统协同作用';
            
            ctx.fillText(viewTitle, 20, 20);
            
            // 绘制当前阶段指示器
            ctx.font = '14px Arial';
            ctx.fillStyle = '#7f8c8d';
            
            let stageText = '';
            if (currentView === 'humoral') {
                if (time < 2) stageText = '阶段1: B细胞识别抗原';
                else if (time < 4) stageText = '阶段2: 辅助T细胞激活B细胞';
                else if (time < 6) stageText = '阶段3: B细胞增殖分化为浆细胞';
                else stageText = '阶段4: 浆细胞产生抗体中和病原体';
            } else if (currentView === 'cellular') {
                if (time < 2) stageText = '阶段1: APC呈递抗原';
                else if (time < 4) stageText = '阶段2: T细胞激活';
                else if (time < 6) stageText = '阶段3: 细胞毒性T细胞攻击受感染细胞';
                else stageText = '阶段4: 清除受感染细胞';
            } else {
                if (time < 2) stageText = '阶段1: 病原体入侵，APC呈递抗原';
                else if (time < 4) stageText = '阶段2: 辅助T细胞激活';
                else if (time < 6) stageText = '阶段3: 辅助T细胞协调B细胞和Tc细胞';
                else stageText = '阶段4: 抗体中和病原体，Tc细胞清除受感染细胞';
            }
            
            ctx.fillText(stageText, 20, 50);
        }
        
        // 动画循环
        function animate() {
            updateAnimation();
            drawAnimation();
            
            if (isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }
        
        // 切换视图
        function switchView(view) {
            currentView = view;
            time = 0;
            
            // 更新按钮状态
            document.getElementById('humoralBtn').classList.toggle('btn-active', view === 'humoral');
            document.getElementById('cellularBtn').classList.toggle('btn-active', view === 'cellular');
            document.getElementById('combinedBtn').classList.toggle('btn-active', view === 'combined');
            
            // 更新信息面板
            document.getElementById('currentViewTitle').textContent = viewInfo[view].title;
            document.getElementById('currentViewDescription').textContent = viewInfo[view].description;
            
            // 重新初始化元素
            initElements();
            
            // 如果动画正在播放，继续播放
            if (isPlaying) {
                if (animationId) cancelAnimationFrame(animationId);
                animationId = requestAnimationFrame(animate);
            } else {
                // 否则只绘制一帧
                drawAnimation();
            }
        }
        
        // 播放/暂停动画
        function togglePlayPause() {
            isPlaying = !isPlaying;
            
            const playIcon = document.getElementById('playIcon');
            const playText = document.getElementById('playText');
            
            if (isPlaying) {
                playIcon.textContent = '⏸';
                playText.textContent = '暂停';
                
                if (animationId) cancelAnimationFrame(animationId);
                animationId = requestAnimationFrame(animate);
            } else {
                playIcon.textContent = '▶';
                playText.textContent = '播放';
                
                if (animationId) {
                    cancelAnimationFrame(animationId);
                    animationId = null;
                }
            }
        }
        
        // 重置动画
        function resetAnimation() {
            time = 0;
            initElements();
            
            if (!isPlaying) {
                drawAnimation();
            }
        }
        
        // 鼠标悬停检测
        function handleMouseMove(event) {
            const rect = canvas.getBoundingClientRect();
            const mouseX = event.clientX - rect.left;
            const mouseY = event.clientY - rect.top;
            
            let tooltipContent = '';
            let foundElement = false;
            
            // 检查病原体
            elements.pathogens.forEach(pathogen => {
                const dx = mouseX - pathogen.x;
                const dy = mouseY - pathogen.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance < pathogen.radius) {
                    tooltipContent = `<div class="tooltip-title">${pathogen.type === 'bacteria' ? '细菌' : '病毒'}</div>
                                     <div class="tooltip-desc">外来病原体，触发免疫应答${pathogen.neutralized ? ' (已被抗体中和)' : ''}</div>`;
                    foundElement = true;
                }
            });
            
            // 检查B细胞
            if (!foundElement) {
                elements.bCells.forEach(bCell => {
                    const dx = mouseX - bCell.x;
                    const dy = mouseY - bCell.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < bCell.radius) {
                        let stateDesc = '';
                        if (bCell.state === 'inactive') stateDesc = '静止状态';
                        else if (bCell.state === 'activating') stateDesc = '激活中';
                        else if (bCell.state === 'dividing') stateDesc = '增殖中';
                        else stateDesc = '浆细胞(产生抗体)';
                        
                        tooltipContent = `<div class="tooltip-title">B细胞</div>
                                         <div class="tooltip-desc">体液免疫的核心细胞，识别抗原并产生抗体。当前状态: ${stateDesc}</div>`;
                        foundElement = true;
                    }
                });
            }
            
            // 检查T细胞
            if (!foundElement) {
                elements.tCells.forEach(tCell => {
                    const dx = mouseX - tCell.x;
                    const dy = mouseY - tCell.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < tCell.radius) {
                        let stateDesc = '';
                        if (tCell.state === 'inactive') stateDesc = '静止状态';
                        else if (tCell.state === 'activating') stateDesc = '激活中';
                        else stateDesc = '攻击受感染细胞';
                        
                        tooltipContent = `<div class="tooltip-title">细胞毒性T细胞 (Tc)</div>
                                         <div class="tooltip-desc">细胞免疫的效应细胞，识别并杀伤受感染的细胞。当前状态: ${stateDesc}</div>`;
                        foundElement = true;
                    }
                });
            }
            
            // 检查辅助T细胞
            if (!foundElement) {
                elements.helperTCells.forEach(helperT => {
                    const dx = mouseX - helperT.x;
                    const dy = mouseY - helperT.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < helperT.radius) {
                        let stateDesc = '';
                        if (helperT.state === 'inactive') stateDesc = '静止状态';
                        else if (helperT.state === 'activating') stateDesc = '激活中';
                        else if (helperT.state === 'activated') stateDesc = '已激活';
                        else stateDesc = '发送信号中';
                        
                        tooltipContent = `<div class="tooltip-title">辅助T细胞 (Th)</div>
                                         <div class="tooltip-desc">免疫系统的协调者，激活B细胞和Tc细胞，是体液免疫和细胞免疫的桥梁。当前状态: ${stateDesc}</div>`;
                        foundElement = true;
                    }
                });
            }
            
            // 检查APC
            if (!foundElement && elements.apcs.length > 0) {
                elements.apcs.forEach(apc => {
                    const dx = mouseX - apc.x;
                    const dy = mouseY - apc.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < apc.radius) {
                        let stateDesc = '';
                        if (apc.state === 'inactive') stateDesc = '静止状态';
                        else if (apc.state === 'migrating') stateDesc = '迁移中';
                        else stateDesc = '呈递抗原中';
                        
                        tooltipContent = `<div class="tooltip-title">抗原呈递细胞 (APC)</div>
                                         <div class="tooltip-desc">捕获、处理并呈递抗原给T细胞，启动细胞免疫应答。当前状态: ${stateDesc}</div>`;
                        foundElement = true;
                    }
                });
            }
            
            // 显示或隐藏工具提示
            if (foundElement) {
                tooltip.innerHTML = tooltipContent;
                tooltip.style.left = (event.clientX + 15) + 'px';
                tooltip.style.top = (event.clientY + 15) + 'px';
                tooltip.style.opacity = '1';
            } else {
                tooltip.style.opacity = '0';
            }
        }
        
        // 初始化
        function init() {
            // 初始化元素
            initElements();
            
            // 绘制初始帧
            drawAnimation();
            
            // 设置事件监听器
            document.getElementById('humoralBtn').addEventListener('click', () => switchView('humoral'));
            document.getElementById('cellularBtn').addEventListener('click', () => switchView('cellular'));
            document.getElementById('combinedBtn').addEventListener('click', () => switchView('combined'));
            
            document.getElementById('playPauseBtn').addEventListener('click', togglePlayPause);
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            
            document.getElementById('speedSlider').addEventListener('input', function() {
                animationSpeed = parseFloat(this.value);
                document.getElementById('speedValue').textContent = animationSpeed.toFixed(1) + 'x';
            });
            
            canvas.addEventListener('mousemove', handleMouseMove);
            
            // 初始显示体液免疫视图
            switchView('humoral');
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 交互式教学动画使用指南

欢迎使用“体液免疫与细胞免疫的双系统协同”交互式教学动画！本指南将帮助您充分利用这一精心设计的教学工具，深入理解免疫系统两大核心防御机制的运作原理。

---

#### 一、 功能说明

本动画是一个基于HTML5 Canvas开发的交互式教学工具，旨在通过动态可视化方式，生动展示：
1.  **体液免疫**：以B细胞和抗体为核心的防御路径，主要清除细胞外病原体。
2.  **细胞免疫**：以T细胞为核心的防御路径，主要清除被感染的自身细胞和癌细胞。
3.  **双系统协同**：展示在真实感染场景下，体液免疫与细胞免疫如何通过辅助T细胞（Th）进行精密协作，形成高效、完整的免疫应答。

动画将抽象的免疫学概念（如抗原呈递、细胞活化、信号传递等）转化为直观的图形和动态过程，降低学习门槛，提升理解深度。

---

#### 二、 主要功能

1.  **三视图切换**：
    *   **体液免疫视图**：聚焦展示B细胞识别抗原、在辅助T细胞帮助下活化、增殖分化为浆细胞并产生抗体的全过程。
    *   **细胞免疫视图**：聚焦展示抗原呈递细胞（APC）激活T细胞、细胞毒性T细胞（Tc）识别并杀伤受感染靶细胞的全过程。
    *   **双系统协同视图**：整合展示两条路径，重点突出辅助T细胞（Th）作为“免疫指挥官”的核心协调作用。

2.  **动画控制**：
    *   **播放/暂停**：控制动画的进行与暂停，便于分步观察。
    *   **速度调节**：通过滑块自由调整动画播放速度（0.5倍至3.0倍），适应不同学习节奏。
    *   **重置**：一键将动画恢复到初始状态，方便重复观看。

3.  **交互探索**：
    *   **鼠标悬停提示**：将鼠标移动到画布中的任何免疫细胞或分子（如B细胞、T细胞、抗体、病原体）上，会弹出详细的信息提示框，说明其名称和功能。
    *   **动态图例**：页面底部提供完整的颜色图例，帮助您快速识别动画中不同颜色的元素所代表的含义。

4.  **实时信息面板**：
    *   切换视图时，动画下方的信息面板会同步更新，提供当前视图的**文字概述**和**核心知识点**，实现图文并茂的学习体验。
    *   画布左上角会显示当前动画所处的**关键阶段**，帮助您把握学习进程。

---

#### 三、 设计特色

1.  **科学的视觉编码**：
    *   **颜色体系**：采用一套严谨的配色方案（蓝色系代表体液免疫，绿色系代表细胞免疫，紫色代表辅助T细胞，红色代表病原体），使复杂的免疫网络一目了然。
    *   **动态效果**：使用脉冲、连接线、轨迹、形态变化等动画效果，清晰表达“识别”、“激活”、“信号传递”、“攻击”、“中和”等关键生物学过程。

2.  **符合认知规律的教学设计**：
    *   **从分到总**：先独立学习两个子系统，再理解其协同，符合“分析-综合”的认知逻辑。
    *   **突出关键**：将辅助T细胞（Th）设计为醒目的紫色，并强化其在协同视图中的中心地位，紧扣教学重点。
    *   **即时反馈**：交互提示和阶段标识提供即时学习反馈，增强学习沉浸感。

3.  **响应式与可访问性**：
    *   界面适配不同屏幕尺寸，在电脑、平板等设备上均可获得良好体验。
    *   控制面板布局清晰，按钮功能明确，易于操作。

---

#### 四、 教学要点

在观看动画时，请特别关注以下核心生物学过程和概念：

1.  **体液免疫路径**：
    *   **特异性识别**：B细胞通过膜表面受体识别特定抗原。
    *   **T细胞依赖的激活**：B细胞的完全活化需要辅助T细胞（Th）提供的第二信号（细胞因子）。
    *   **效应与记忆**：活化的B细胞分化为**浆细胞**（效应细胞，产生抗体）和**记忆B细胞**（提供长期免疫）。

2.  **细胞免疫路径**：
    *   **抗原加工与呈递**：APC吞噬病原体，处理抗原并将其呈递给T细胞。
    *   **双信号激活**：T细胞的激活需要APC提供的抗原信号（第一信号）和共刺激信号（第二信号）。
    *   **靶向杀伤**：活化的细胞毒性T细胞（Tc）通过释放穿孔素、颗粒酶等物质，特异性杀伤被感染的靶细胞。

3.  **协同机制（教学核心）**：
    *   **辅助T细胞（Th）是枢纽**：同一个被APC激活的Th细胞，可以同时向B细胞和Tc细胞提供活化信号。
    *   **针对不同威胁的协作**：动画在“协同视图”中展示了抗体如何中和细胞外病毒，而Tc细胞如何清除已被病毒感染的细胞，体现了“内外兼防”的策略。
    *   **免疫应答的整体性**：两个系统并非独立工作，而是在Th细胞的协调下，根据病原体类型和感染阶段，动态调整资源，实现最有效的防御。

---

#### 五、 使用建议

1.  **初次学习者**：
    *   建议按照 **“体液免疫” → “细胞免疫” → “双系统协同”** 的顺序依次观看。
    *   每个视图先使用**正常速度（1.0x）自动播放**一遍，了解全过程。
    *   随后使用**暂停**和**慢速播放**，结合**鼠标悬停**功能，仔细研究每一步的细节和细胞间的相互作用。

2.  **复习与深化者**：
    *   直接进入“**双系统协同**”视图，尝试在脑海中预判不同细胞的行为。
    *   使用**重置**功能，多次观看协同过程，重点关注**辅助T细胞（紫色）** 的活动轨迹及其与其他细胞的连接。
    *   思考并回答：如果辅助T细胞功能缺失，会对免疫应答产生何种影响？

3.  **教学演示者**：
    *   可以分屏操作，一边播放动画，一边进行讲解。
    *   利用视图切换功能，对比讲解两种免疫方式的特点（如作用对象、效应分子、记忆细胞类型等）。
    *   在播放协同动画时，随时暂停，提问引导学生预测下一步会发生什么，增加课堂互动性。

我们希望这个交互式动画能成为您探索免疫学奥秘的得力助手。请尽情交互、探索，并享受发现的乐趣！如果您有任何反馈或教学心得，欢迎与我们分享。祝您学习愉快！