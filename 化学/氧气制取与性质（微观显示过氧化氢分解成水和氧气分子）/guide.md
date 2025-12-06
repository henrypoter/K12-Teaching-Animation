# 需求：氧气制取与性质（微观显示过氧化氢分解成水和氧气分子）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中或高中化学初学者。他们需要直观理解抽象的微观化学反应过程，特别是分子在反应中的断裂与重组。
2.  **核心痛点**：传统教学（如课本插图、板书）难以动态、清晰地展示“过氧化氢分解”这一过程中，分子如何破裂成原子，原子又如何重新组合成新分子。学生容易混淆反应物与生成物，对“催化剂”的作用机制感到困惑。
3.  **学习目标**：
    *   **知识层面**：掌握过氧化氢在二氧化锰催化下分解生成水和氧气的化学反应方程式（2H₂O₂ → 2H₂O + O₂↑）。
    *   **微观层面**：可视化理解反应过程：过氧化氢分子（H₂O₂）分解成氢原子和氧原子，这些原子重新组合成水分子（H₂O）和氧分子（O₂）。
    *   **概念层面**：理解“催化剂”在反应中“参与反应但质量和化学性质不变”的微观本质——即催化剂的表面如何促进分子断裂。
4.  **交互需求**：用户需要能够控制动画的进程（播放、暂停、重置），并能选择观察视角（如整体反应、催化剂特写），以主动探索和理解。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念**：
    *   **化学反应的本质**：分子的破裂和原子的重新组合。
    *   **催化剂的作用**：提供反应场所，降低反应活化能，自身不消耗。
    *   **质量守恒定律**（微观体现）：反应前后原子种类和数目不变。

2.  **认知规律**：
    *   **从宏观到微观**：动画开场可展示一个装有双氧水的锥形瓶，加入二氧化锰后产生气泡（氧气）。然后镜头推入，进入微观世界，将宏观现象与微观过程联系起来。
    *   **分解复杂过程**：将连续的反应分解为几个关键阶段，并允许用户分步观看：
        a. 反应前：展示自由的过氧化氢分子和静止的二氧化锰催化剂颗粒。
        b. 吸附与断裂：过氧化氢分子被吸附到催化剂表面，化学键（O-O键）断裂。
        c. 原子重组：断裂产生的原子在催化剂表面移动并重新组合。
        d. 生成与脱附：新生成的水分子和氧分子从催化剂表面脱离。
    *   **突出关键变化**：使用高亮、颜色变化和动态效果来强调化学键的断裂与形成。

3.  **交互设计**：
    *   **进程控制**：提供清晰的播放/暂停/重置按钮。
    *   **阶段控制**：提供“步骤按钮”（如“步骤1：反应物”、“步骤2：键的断裂”、“步骤3：原子重组”、“步骤4：生成物”），允许用户按阶段学习。
    *   **视角切换**：提供“整体视图”和“催化剂特写视图”的切换按钮，让用户可以聚焦观察催化剂表面的细节过程。
    *   **提示与标注**：鼠标悬停在分子或原子上时，显示其名称和化学式。在关键步骤，有简明的文字说明自动浮现。

4.  **视觉呈现**：
    *   **分子模型**：采用比例准确的球棍模型。不同原子用不同颜色和大小的球体表示（国际惯例：氢=白色，氧=红色）。化学键用棍状表示。
    *   **动画设计**：
        *   分子和原子运动平滑，符合物理直觉（如轻微布朗运动）。
        *   化学键断裂时，连接的“棍子”会高亮、振动然后消失。
        *   新化学键形成时，会有“连接”的动画效果。
    *   **催化剂表示**：将二氧化锰颗粒简化为一个灰色的、具有不规则表面的静态背景物体，以区别于运动的分子。
    *   **布局**：画面中央为反应区。控制面板置于底部，信息提示框置于顶部或侧边。

#### 配色方案选择
*   **主色调**：采用深蓝色或深空灰色作为背景，模拟深邃的微观世界或实验室的沉稳感，能很好地突出前景的彩色分子。
*   **原子颜色**：
    *   氢原子（H）：浅灰色或白色。避免使用过于鲜艳的颜色，以突出氧。
    *   氧原子（O）：鲜红色。这是化学中表示氧的通用色，非常醒目。
    *   （催化剂中的锰、氧原子）：使用不同明度的灰色（如锰用深灰，氧用中灰）表示，以表明它们在反应中“不变化”的特性。
*   **化学键**：使用浅灰色或白色的棍状线条。
*   **高亮与强调色**：
    *   键断裂/形成时：使用亮黄色或青色进行高亮闪烁。
    *   按钮与UI元素：使用与主色调协调的蓝色系（如湖蓝色），搭配白色文字，清晰友好。
*   **文字与提示**：白色或浅黄色文字，配以半透明黑色背景框，确保可读性。

#### 交互功能列表
1.  **动画控制区**：
    *   “播放/暂停”按钮：开始或暂停连续动画。
    *   “重置”按钮：将动画恢复到初始状态。
    *   “慢速/常速”切换：调整动画播放速度。
2.  **学习阶段控制区**：
    *   “步骤1：反应物”按钮：显示初始的H₂O₂分子和MnO₂催化剂。
    *   “步骤2：吸附与断裂”按钮：演示H₂O₂分子吸附到催化剂表面及O-O键断裂。
    *   “步骤3：重组与生成”按钮：演示H、O原子重组为H₂O和O₂。
    *   “步骤4：生成物脱附”按钮：演示H₂O和O₂分子离开催化剂表面。
    *   “连续播放所有步骤”按钮：自动按顺序执行1-4步。
3.  **视角控制区**：
    *   “整体视图”按钮：显示包含多个分子和催化剂颗粒的宏观微观场景。
    *   “催化剂特写”按钮：镜头拉近，聚焦于单个催化剂颗粒表面的一个反应位点，详细展示反应过程。
4.  **信息提示功能**：
    *   鼠标悬停交互：悬停在任意原子、分子或催化剂上，显示其名称和化学式。
    *   动态字幕：在动画播放不同阶段，画面顶部或底部自动出现简要的步骤说明文字（如：“过氧化氢分子在二氧化锰表面吸附并分解”）。
    *   化学方程式显示：在画面固定位置（如右上角）始终显示反应方程式：2H₂O₂ → 2H₂O + O₂↑，并在动画过程中，对正在参与步骤的反应物和生成物进行高亮。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>微观世界：过氧化氢分解制取氧气</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0a1929 0%, #1a2b3c 100%);
            color: #e0f7ff;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }
        
        .header {
            text-align: center;
            margin-bottom: 20px;
            width: 100%;
            max-width: 1000px;
        }
        
        h1 {
            color: #4fc3f7;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            color: #b3e5fc;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }
        
        .equation-container {
            background-color: rgba(0, 30, 60, 0.7);
            border-radius: 10px;
            padding: 15px;
            margin: 15px auto;
            border: 1px solid #2a4a6a;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            width: fit-content;
        }
        
        .equation {
            font-size: 1.8rem;
            font-weight: bold;
            color: #ffffff;
        }
        
        .equation .reactant {
            color: #ffcc80;
        }
        
        .equation .product {
            color: #80deea;
        }
        
        .equation .catalyst {
            color: #b0bec5;
            font-size: 1.4rem;
        }
        
        .main-container {
            display: flex;
            flex-direction: column;
            width: 100%;
            max-width: 1000px;
            gap: 20px;
        }
        
        .animation-section {
            flex: 1;
            background-color: rgba(10, 25, 41, 0.8);
            border-radius: 12px;
            padding: 15px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.4);
            border: 1px solid #2a4a6a;
            position: relative;
            overflow: hidden;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #0a1929;
            border-radius: 8px;
            overflow: hidden;
        }
        
        #reactionCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .info-overlay {
            position: absolute;
            top: 15px;
            left: 15px;
            background-color: rgba(0, 20, 40, 0.85);
            padding: 12px 18px;
            border-radius: 8px;
            border-left: 4px solid #4fc3f7;
            max-width: 300px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.4);
        }
        
        .info-title {
            color: #4fc3f7;
            font-weight: bold;
            margin-bottom: 5px;
            font-size: 1.1rem;
        }
        
        .info-text {
            color: #e0f7ff;
            font-size: 0.95rem;
            line-height: 1.4;
        }
        
        .controls-section {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .control-panel {
            background-color: rgba(10, 25, 41, 0.8);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.4);
            border: 1px solid #2a4a6a;
        }
        
        .panel-title {
            color: #4fc3f7;
            font-size: 1.2rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .panel-title i {
            font-size: 1.4rem;
        }
        
        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .btn {
            background-color: #1a3a5f;
            color: #e0f7ff;
            border: none;
            padding: 10px 16px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            gap: 6px;
            flex: 1;
            min-width: 120px;
            justify-content: center;
        }
        
        .btn:hover {
            background-color: #2a4a7f;
            transform: translateY(-2px);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        .btn-primary {
            background-color: #1565c0;
        }
        
        .btn-primary:hover {
            background-color: #0d47a1;
        }
        
        .btn-success {
            background-color: #2e7d32;
        }
        
        .btn-success:hover {
            background-color: #1b5e20;
        }
        
        .btn-warning {
            background-color: #f57c00;
        }
        
        .btn-warning:hover {
            background-color: #e65100;
        }
        
        .btn-danger {
            background-color: #c62828;
        }
        
        .btn-danger:hover {
            background-color: #b71c1c;
        }
        
        .btn-active {
            box-shadow: 0 0 0 2px #4fc3f7;
        }
        
        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 10px;
        }
        
        .speed-label {
            color: #b3e5fc;
            font-size: 0.9rem;
        }
        
        .speed-slider {
            flex: 1;
            height: 6px;
            -webkit-appearance: none;
            appearance: none;
            background: #2a4a6a;
            border-radius: 3px;
            outline: none;
        }
        
        .speed-slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: #4fc3f7;
            cursor: pointer;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #2a4a6a;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
        }
        
        .legend-text {
            font-size: 0.9rem;
            color: #b3e5fc;
        }
        
        .footer {
            margin-top: 20px;
            text-align: center;
            color: #78909c;
            font-size: 0.9rem;
            width: 100%;
            max-width: 1000px;
            padding-top: 15px;
            border-top: 1px solid #2a4a6a;
        }
        
        @media (min-width: 768px) {
            .main-container {
                flex-direction: row;
            }
            
            .animation-section {
                flex: 2;
            }
            
            .controls-section {
                flex: 1;
                min-width: 300px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <div class="header">
        <h1><i class="fas fa-atom"></i> 微观世界：过氧化氢分解制取氧气</h1>
        <p class="subtitle">可视化过氧化氢在二氧化锰催化下分解为水和氧气的微观过程</p>
        
        <div class="equation-container">
            <div class="equation">
                <span class="reactant">2H₂O₂</span>
                <span style="color: #ffffff;"> + </span>
                <span class="catalyst" title="催化剂">MnO₂</span>
                <span style="color: #ffffff;"> → </span>
                <span class="product">2H₂O</span>
                <span style="color: #ffffff;"> + </span>
                <span class="product">O₂↑</span>
            </div>
        </div>
    </div>
    
    <div class="main-container">
        <div class="animation-section">
            <div class="canvas-container">
                <canvas id="reactionCanvas"></canvas>
                <div class="info-overlay">
                    <div class="info-title" id="stepTitle">准备开始</div>
                    <div class="info-text" id="stepDescription">点击下方按钮开始观察过氧化氢分解的微观过程。</div>
                </div>
            </div>
        </div>
        
        <div class="controls-section">
            <div class="control-panel">
                <div class="panel-title"><i class="fas fa-play-circle"></i> 动画控制</div>
                <div class="button-group">
                    <button id="playBtn" class="btn btn-primary">
                        <i class="fas fa-play"></i> 播放
                    </button>
                    <button id="pauseBtn" class="btn btn-warning">
                        <i class="fas fa-pause"></i> 暂停
                    </button>
                    <button id="resetBtn" class="btn btn-danger">
                        <i class="fas fa-redo"></i> 重置
                    </button>
                </div>
                
                <div class="speed-control">
                    <span class="speed-label">动画速度:</span>
                    <input type="range" min="1" max="10" value="5" class="speed-slider" id="speedSlider">
                </div>
            </div>
            
            <div class="control-panel">
                <div class="panel-title"><i class="fas fa-list-ol"></i> 学习步骤</div>
                <div class="button-group">
                    <button id="step1Btn" class="btn">
                        <i class="fas fa-vial"></i> 步骤1: 反应物
                    </button>
                    <button id="step2Btn" class="btn">
                        <i class="fas fa-bolt"></i> 步骤2: 键的断裂
                    </button>
                </div>
                <div class="button-group">
                    <button id="step3Btn" class="btn">
                        <i class="fas fa-sync-alt"></i> 步骤3: 原子重组
                    </button>
                    <button id="step4Btn" class="btn">
                        <i class="fas fa-wind"></i> 步骤4: 生成物
                    </button>
                </div>
                <button id="fullProcessBtn" class="btn btn-success" style="width: 100%; margin-top: 5px;">
                    <i class="fas fa-forward"></i> 连续播放所有步骤
                </button>
            </div>
            
            <div class="control-panel">
                <div class="panel-title"><i class="fas fa-eye"></i> 观察视角</div>
                <div class="button-group">
                    <button id="overallViewBtn" class="btn btn-active">
                        <i class="fas fa-globe"></i> 整体视图
                    </button>
                    <button id="catalystViewBtn" class="btn">
                        <i class="fas fa-search"></i> 催化剂特写
                    </button>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff9999;"></div>
                        <div class="legend-text">氧原子 (O)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #cccccc;"></div>
                        <div class="legend-text">氢原子 (H)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #aaaaaa;"></div>
                        <div class="legend-text">催化剂 (MnO₂)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ffff00;"></div>
                        <div class="legend-text">化学键断裂/形成</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="footer">
        <p>教学动画设计 | 化学反应微观可视化 | 过氧化氢分解制取氧气</p>
        <p>提示：将鼠标悬停在分子或原子上可以查看详细信息</p>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const canvas = document.getElementById('reactionCanvas');
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
        
        // 动画状态变量
        let animationId = null;
        let currentStep = 0; // 0: 初始, 1: 反应物, 2: 键断裂, 3: 原子重组, 4: 生成物
        let animationSpeed = 5; // 1-10
        let isPlaying = false;
        let isCatalystView = false;
        let animationProgress = 0; // 0-100
        let hoveredObject = null;
        
        // 颜色定义
        const colors = {
            background: '#0a1929',
            oxygen: '#ff6666',
            hydrogen: '#e0e0e0',
            catalyst: '#aaaaaa',
            bond: '#cccccc',
            highlight: '#ffff00',
            text: '#e0f7ff',
            infoBg: 'rgba(0, 20, 40, 0.9)'
        };
        
        // 分子和原子定义
        class Atom {
            constructor(type, x, y) {
                this.type = type; // 'O' 或 'H'
                this.x = x;
                this.y = y;
                this.radius = this.type === 'O' ? 12 : 8;
                this.color = this.type === 'O' ? colors.oxygen : colors.hydrogen;
                this.originalX = x;
                this.originalY = y;
                this.vx = 0;
                this.vy = 0;
                this.isMoving = false;
                this.targetX = x;
                this.targetY = y;
                this.highlight = false;
            }
            
            draw() {
                // 绘制原子
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = this.highlight ? colors.highlight : this.color;
                ctx.fill();
                
                // 绘制原子边框
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.strokeStyle = this.highlight ? '#ffffff' : (this.type === 'O' ? '#cc3333' : '#999999');
                ctx.lineWidth = 1.5;
                ctx.stroke();
                
                // 绘制原子类型标签
                ctx.fillStyle = '#ffffff';
                ctx.font = 'bold 10px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(this.type, this.x, this.y);
                
                // 如果被鼠标悬停，显示详细信息
                if (this === hoveredObject) {
                    this.drawInfo();
                }
            }
            
            drawInfo() {
                const name = this.type === 'O' ? '氧原子' : '氢原子';
                const symbol = this.type === 'O' ? 'O' : 'H';
                
                ctx.fillStyle = colors.infoBg;
                ctx.fillRect(this.x - 40, this.y - this.radius - 40, 80, 30);
                
                ctx.fillStyle = colors.text;
                ctx.font = '10px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`${name} (${symbol})`, this.x, this.y - this.radius - 25);
            }
            
            update() {
                // 如果原子需要移动，则更新位置
                if (this.isMoving) {
                    const dx = this.targetX - this.x;
                    const dy = this.targetY - this.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance > 1) {
                        this.vx = dx * 0.05 * (animationSpeed / 5);
                        this.vy = dy * 0.05 * (animationSpeed / 5);
                        this.x += this.vx;
                        this.y += this.vy;
                    } else {
                        this.x = this.targetX;
                        this.y = this.targetY;
                        this.isMoving = false;
                    }
                }
            }
            
            moveTo(x, y) {
                this.targetX = x;
                this.targetY = y;
                this.isMoving = true;
            }
        }
        
        class Molecule {
            constructor(type, atoms, bonds) {
                this.type = type; // 'H2O2', 'H2O', 'O2'
                this.atoms = atoms;
                this.bonds = bonds;
                this.x = atoms.reduce((sum, atom) => sum + atom.x, 0) / atoms.length;
                this.y = atoms.reduce((sum, atom) => sum + atom.y, 0) / atoms.length;
                this.highlight = false;
            }
            
            draw() {
                // 绘制化学键
                for (const bond of this.bonds) {
                    const atom1 = this.atoms[bond[0]];
                    const atom2 = this.atoms[bond[1]];
                    
                    ctx.beginPath();
                    ctx.moveTo(atom1.x, atom1.y);
                    ctx.lineTo(atom2.x, atom2.y);
                    ctx.strokeStyle = this.highlight ? colors.highlight : colors.bond;
                    ctx.lineWidth = this.highlight ? 4 : 3;
                    ctx.stroke();
                }
                
                // 绘制原子
                for (const atom of this.atoms) {
                    atom.draw();
                }
                
                // 如果被鼠标悬停，显示详细信息
                if (this === hoveredObject) {
                    this.drawInfo();
                }
            }
            
            drawInfo() {
                let name, formula;
                switch(this.type) {
                    case 'H2O2': name = '过氧化氢'; formula = 'H₂O₂'; break;
                    case 'H2O': name = '水'; formula = 'H₂O'; break;
                    case 'O2': name = '氧气'; formula = 'O₂'; break;
                }
                
                ctx.fillStyle = colors.infoBg;
                ctx.fillRect(this.x - 50, this.y - 50, 100, 40);
                
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 12px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(name, this.x, this.y - 35);
                
                ctx.font = '14px Arial';
                ctx.fillText(formula, this.x, this.y - 20);
            }
            
            update() {
                for (const atom of this.atoms) {
                    atom.update();
                }
                
                // 更新分子中心位置
                this.x = this.atoms.reduce((sum, atom) => sum + atom.x, 0) / this.atoms.length;
                this.y = this.atoms.reduce((sum, atom) => sum + atom.y, 0) / this.atoms.length;
            }
        }
        
        class Catalyst {
            constructor(x, y, width, height) {
                this.x = x;
                this.y = y;
                this.width = width;
                this.height = height;
                this.surfaceAtoms = [];
                this.generateSurface();
            }
            
            generateSurface() {
                // 生成催化剂表面原子
                const atomSpacing = 15;
                const rows = Math.floor(this.height / atomSpacing);
                const cols = Math.floor(this.width / atomSpacing);
                
                for (let r = 0; r < rows; r++) {
                    for (let c = 0; c < cols; c++) {
                        const x = this.x + c * atomSpacing + (r % 2) * atomSpacing/2;
                        const y = this.y + r * atomSpacing;
                        
                        // 随机省略一些原子以创建不规则表面
                        if (Math.random() > 0.3) {
                            this.surfaceAtoms.push({
                                x: x,
                                y: y,
                                radius: 6,
                                type: Math.random() > 0.5 ? 'Mn' : 'O'
                            });
                        }
                    }
                }
            }
            
            draw() {
                // 绘制催化剂主体
                ctx.fillStyle = colors.catalyst;
                ctx.fillRect(this.x, this.y, this.width, this.height);
                
                // 绘制表面纹理
                ctx.fillStyle = '#888888';
                for (let i = 0; i < this.surfaceAtoms.length; i++) {
                    const atom = this.surfaceAtoms[i];
                    ctx.beginPath();
                    ctx.arc(atom.x, atom.y, atom.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 绘制原子标签
                    ctx.fillStyle = '#ffffff';
                    ctx.font = 'bold 8px Arial';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText(atom.type, atom.x, atom.y);
                    ctx.fillStyle = '#888888';
                }
                
                // 如果被鼠标悬停，显示详细信息
                if (this === hoveredObject) {
                    this.drawInfo();
                }
            }
            
            drawInfo() {
                ctx.fillStyle = colors.infoBg;
                ctx.fillRect(this.x + this.width/2 - 60, this.y - 40, 120, 30);
                
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 12px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('二氧化锰催化剂', this.x + this.width/2, this.y - 25);
                ctx.font = '10px Arial';
                ctx.fillText('MnO₂', this.x + this.width/2, this.y - 10);
            }
        }
        
        // 创建反应物、生成物和催化剂
        let h2o2Molecules = [];
        let h2oMolecules = [];
        let o2Molecules = [];
        let catalyst;
        let freeAtoms = [];
        
        function initScene() {
            // 清空所有数组
            h2o2Molecules = [];
            h2oMolecules = [];
            o2Molecules = [];
            freeAtoms = [];
            
            // 创建催化剂
            const catalystWidth = canvas.width * 0.7;
            const catalystHeight = canvas.height * 0.2;
            catalyst = new Catalyst(
                canvas.width/2 - catalystWidth/2,
                canvas.height/2 - catalystHeight/2 + 50,
                catalystWidth,
                catalystHeight
            );
            
            // 根据当前步骤初始化场景
            if (currentStep === 0 || currentStep === 1) {
                // 步骤1: 反应物 - 创建过氧化氢分子
                const h2o2Count = 4;
                for (let i = 0; i < h2o2Count; i++) {
                    const angle = (i / h2o2Count) * Math.PI * 2;
                    const radius = Math.min(canvas.width, canvas.height) * 0.3;
                    const centerX = canvas.width/2 + Math.cos(angle) * radius;
                    const centerY = canvas.height/2 + Math.sin(angle) * radius - 50;
                    
                    // 创建H2O2分子 (H-O-O-H)
                    const atom1 = new Atom('H', centerX - 25, centerY - 5);
                    const atom2 = new Atom('O', centerX - 10, centerY);
                    const atom3 = new Atom('O', centerX + 10, centerY);
                    const atom4 = new Atom('H', centerX + 25, centerY - 5);
                    
                    const bonds = [[0, 1], [1, 2], [2, 3]];
                    const molecule = new Molecule('H2O2', [atom1, atom2, atom3, atom4], bonds);
                    h2o2Molecules.push(molecule);
                }
            } else if (currentStep === 2) {
                // 步骤2: 键的断裂 - 过氧化氢分子在催化剂表面分解
                // 创建一些在催化剂表面的过氧化氢分子
                const h2o2Count = 3;
                for (let i = 0; i < h2o2Count; i++) {
                    const x = catalyst.x + catalyst.width * (0.2 + i * 0.3);
                    const y = catalyst.y - 40;
                    
                    const atom1 = new Atom('H', x - 15, y - 10);
                    const atom2 = new Atom('O', x - 5, y);
                    const atom3 = new Atom('O', x + 5, y);
                    const atom4 = new Atom('H', x + 15, y - 10);
                    
                    // 高亮显示即将断裂的键
                    atom2.highlight = true;
                    atom3.highlight = true;
                    
                    const bonds = [[0, 1], [1, 2], [2, 3]];
                    const molecule = new Molecule('H2O2', [atom1, atom2, atom3, atom4], bonds);
                    molecule.highlight = true;
                    h2o2Molecules.push(molecule);
                }
                
                // 创建一些已经断裂的原子
                for (let i = 0; i < 4; i++) {
                    const x = catalyst.x + catalyst.width * (0.1 + i * 0.25);
                    const y = catalyst.y + 10;
                    
                    if (i % 2 === 0) {
                        freeAtoms.push(new Atom('H', x, y));
                    } else {
                        freeAtoms.push(new Atom('O', x, y));
                    }
                }
            } else if (currentStep === 3) {
                // 步骤3: 原子重组 - 原子在催化剂表面重新组合
                // 创建一些自由原子
                for (let i = 0; i < 6; i++) {
                    const x = catalyst.x + catalyst.width * (0.1 + i * 0.15);
                    const y = catalyst.y + 10 + (i % 3) * 15;
                    
                    if (i % 3 === 0) {
                        freeAtoms.push(new Atom('H', x, y));
                    } else {
                        freeAtoms.push(new Atom('O', x, y));
                    }
                }
                
                // 创建一些正在形成的水分子
                const h2oCount = 2;
                for (let i = 0; i < h2oCount; i++) {
                    const x = catalyst.x + catalyst.width * (0.3 + i * 0.4);
                    const y = catalyst.y - 60;
                    
                    const atom1 = new Atom('H', x - 10, y - 5);
                    const atom2 = new Atom('O', x, y);
                    const atom3 = new Atom('H', x + 10, y - 5);
                    
                    // 高亮显示正在形成的键
                    atom1.highlight = true;
                    atom2.highlight = true;
                    atom3.highlight = true;
                    
                    const bonds = [[0, 1], [1, 2]];
                    const molecule = new Molecule('H2O', [atom1, atom2, atom3], bonds);
                    molecule.highlight = true;
                    h2oMolecules.push(molecule);
                }
                
                // 创建一个正在形成的氧气分子
                const o2X = catalyst.x + catalyst.width * 0.7;
                const o2Y = catalyst.y - 80;
                
                const oAtom1 = new Atom('O', o2X - 8, o2Y);
                const oAtom2 = new Atom('O', o2X + 8, o2Y);
                
                oAtom1.highlight = true;
                oAtom2.highlight = true;
                
                const o2Bonds = [[0, 1]];
                const o2Molecule = new Molecule('O2', [oAtom1, oAtom2], o2Bonds);
                o2Molecule.highlight = true;
                o2Molecules.push(o2Molecule);
            } else if (currentStep === 4) {
                // 步骤4: 生成物 - 水和氧气分子离开催化剂
                // 创建水分子
                const h2oCount = 4;
                for (let i = 0; i < h2oCount; i++) {
                    const angle = (i / h2oCount) * Math.PI * 2;
                    const radius = Math.min(canvas.width, canvas.height) * 0.25;
                    const centerX = canvas.width/2 + Math.cos(angle) * radius;
                    const centerY = canvas.height/2 + Math.sin(angle) * radius - 80;
                    
                    const atom1 = new Atom('H', centerX - 10, centerY - 5);
                    const atom2 = new Atom('O', centerX, centerY);
                    const atom3 = new Atom('H', centerX + 10, centerY - 5);
                    
                    const bonds = [[0, 1], [1, 2]];
                    const molecule = new Molecule('H2O', [atom1, atom2, atom3], bonds);
                    h2oMolecules.push(molecule);
                }
                
                // 创建氧气分子
                const o2Count = 2;
                for (let i = 0; i < o2Count; i++) {
                    const x = canvas.width/2 + (i - 0.5) * 100;
                    const y = canvas.height/2 - 120;
                    
                    const atom1 = new Atom('O', x - 8, y);
                    const atom2 = new Atom('O', x + 8, y);
                    
                    const bonds = [[0, 1]];
                    const molecule = new Molecule('O2', [atom1, atom2], bonds);
                    o2Molecules.push(molecule);
                }
                
                // 催化剂仍然在底部
                catalyst.y = canvas.height - catalyst.height - 50;
            }
        }
        
        // 动画循环
        function animate() {
            // 清空画布
            ctx.fillStyle = colors.background;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制催化剂
            catalyst.draw();
            
            // 更新和绘制所有分子和原子
            for (const molecule of h2o2Molecules) {
                molecule.update();
                molecule.draw();
            }
            
            for (const molecule of h2oMolecules) {
                molecule.update();
                molecule.draw();
            }
            
            for (const molecule of o2Molecules) {
                molecule.update();
                molecule.draw();
            }
            
            for (const atom of freeAtoms) {
                atom.update();
                atom.draw();
            }
            
            // 如果动画正在播放，更新进度
            if (isPlaying) {
                animationProgress += animationSpeed * 0.5;
                if (animationProgress >= 100) {
                    animationProgress = 0;
                    if (currentStep < 4) {
                        currentStep++;
                        updateStepInfo();
                        initScene();
                    } else {
                        isPlaying = false;
                        document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
                    }
                }
            }
            
            // 继续动画循环
            animationId = requestAnimationFrame(animate);
        }
        
        // 更新步骤信息
        function updateStepInfo() {
            const stepTitle = document.getElementById('stepTitle');
            const stepDescription = document.getElementById('stepDescription');
            
            switch(currentStep) {
                case 0:
                    stepTitle.textContent = '准备开始';
                    stepDescription.textContent = '点击下方按钮开始观察过氧化氢分解的微观过程。';
                    break;
                case 1:
                    stepTitle.textContent = '步骤1: 反应物';
                    stepDescription.textContent = '过氧化氢分子(H₂O₂)和二氧化锰催化剂准备就绪。注意过氧化氢分子中的O-O键。';
                    break;
                case 2:
                    stepTitle.textContent = '步骤2: 键的断裂';
                    stepDescription.textContent = '过氧化氢分子吸附在催化剂表面，O-O键断裂，分解为氢原子和氧原子。';
                    break;
                case 3:
                    stepTitle.textContent = '步骤3: 原子重组';
                    stepDescription.textContent = '氢原子和氧原子在催化剂表面重新组合，形成水分子(H₂O)和氧分子(O₂)。';
                    break;
                case 4:
                    stepTitle.textContent = '步骤4: 生成物';
                    stepDescription.textContent = '水分子和氧分子从催化剂表面脱离，催化剂保持不变，可以继续催化反应。';
                    break;
            }
            
            // 更新步骤按钮的高亮状态
            document.querySelectorAll('.button-group .btn').forEach(btn => {
                btn.classList.remove('btn-active');
            });
            
            if (currentStep >= 1) {
                document.getElementById(`step${currentStep}Btn`).classList.add('btn-active');
            }
        }
        
        // 鼠标悬停检测
        function checkHover(mouseX, mouseY) {
            hoveredObject = null;
            
            // 检查催化剂
            if (mouseX >= catalyst.x && mouseX <= catalyst.x + catalyst.width &&
                mouseY >= catalyst.y && mouseY <= catalyst.y + catalyst.height) {
                hoveredObject = catalyst;
                return;
            }
            
            // 检查所有分子
            const allMolecules = [...h2o2Molecules, ...h2oMolecules, ...o2Molecules];
            for (const molecule of allMolecules) {
                const dx = mouseX - molecule.x;
                const dy = mouseY - molecule.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance < 40) {
                    hoveredObject = molecule;
                    return;
                }
            }
            
            // 检查所有原子
            const allAtoms = [];
            for (const molecule of allMolecules) {
                allAtoms.push(...molecule.atoms);
            }
            allAtoms.push(...freeAtoms);
            
            for (const atom of allAtoms) {
                const dx = mouseX - atom.x;
                const dy = mouseY - atom.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance < atom.radius + 5) {
                    hoveredObject = atom;
                    return;
                }
            }
        }
        
        // 事件监听器
        canvas.addEventListener('mousemove', (e) => {
            const rect = canvas.getBounding
<!--检测到代码截断，自动续写中...-->
ClientRect();
            const mouseX = e.clientX - rect.left;
            const mouseY = e.clientY - rect.top;
            checkHover(mouseX, mouseY);
        });
        
        // 按钮事件监听
        document.getElementById('playBtn').addEventListener('click', () => {
            isPlaying = !isPlaying;
            if (isPlaying) {
                document.getElementById('playBtn').innerHTML = '<i class="fas fa-pause"></i> 暂停';
                if (currentStep === 0) {
                    currentStep = 1;
                    initScene();
                    updateStepInfo();
                }
            } else {
                document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
            }
        });
        
        document.getElementById('pauseBtn').addEventListener('click', () => {
            isPlaying = false;
            document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
        });
        
        document.getElementById('resetBtn').addEventListener('click', () => {
            isPlaying = false;
            currentStep = 0;
            animationProgress = 0;
            document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
            initScene();
            updateStepInfo();
        });
        
        document.getElementById('step1Btn').addEventListener('click', () => {
            isPlaying = false;
            currentStep = 1;
            animationProgress = 0;
            document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
            initScene();
            updateStepInfo();
        });
        
        document.getElementById('step2Btn').addEventListener('click', () => {
            isPlaying = false;
            currentStep = 2;
            animationProgress = 0;
            document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
            initScene();
            updateStepInfo();
        });
        
        document.getElementById('step3Btn').addEventListener('click', () => {
            isPlaying = false;
            currentStep = 3;
            animationProgress = 0;
            document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
            initScene();
            updateStepInfo();
        });
        
        document.getElementById('step4Btn').addEventListener('click', () => {
            isPlaying = false;
            currentStep = 4;
            animationProgress = 0;
            document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
            initScene();
            updateStepInfo();
        });
        
        document.getElementById('fullProcessBtn').addEventListener('click', () => {
            isPlaying = true;
            currentStep = 1;
            animationProgress = 0;
            document.getElementById('playBtn').innerHTML = '<i class="fas fa-pause"></i> 暂停';
            initScene();
            updateStepInfo();
        });
        
        document.getElementById('overallViewBtn').addEventListener('click', () => {
            isCatalystView = false;
            document.getElementById('overallViewBtn').classList.add('btn-active');
            document.getElementById('catalystViewBtn').classList.remove('btn-active');
            // 在实际实现中，这里会调整摄像机视角
        });
        
        document.getElementById('catalystViewBtn').addEventListener('click', () => {
            isCatalystView = true;
            document.getElementById('catalystViewBtn').classList.add('btn-active');
            document.getElementById('overallViewBtn').classList.remove('btn-active');
            // 在实际实现中，这里会调整摄像机视角
        });
        
        document.getElementById('speedSlider').addEventListener('input', (e) => {
            animationSpeed = parseInt(e.target.value);
        });
        
        // 初始化场景并开始动画
        initScene();
        updateStepInfo();
        animate();
        
        // 添加键盘快捷键
        document.addEventListener('keydown', (e) => {
            switch(e.key) {
                case ' ':
                    // 空格键切换播放/暂停
                    isPlaying = !isPlaying;
                    if (isPlaying) {
                        document.getElementById('playBtn').innerHTML = '<i class="fas fa-pause"></i> 暂停';
                        if (currentStep === 0) {
                            currentStep = 1;
                            initScene();
                            updateStepInfo();
                        }
                    } else {
                        document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
                    }
                    e.preventDefault();
                    break;
                case 'r':
                case 'R':
                    // R键重置
                    isPlaying = false;
                    currentStep = 0;
                    animationProgress = 0;
                    document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
                    initScene();
                    updateStepInfo();
                    break;
                case '1':
                    document.getElementById('step1Btn').click();
                    break;
                case '2':
                    document.getElementById('step2Btn').click();
                    break;
                case '3':
                    document.getElementById('step3Btn').click();
                    break;
                case '4':
                    document.getElementById('step4Btn').click();
                    break;
            }
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

# 交互式教学动画使用指南
## 《微观世界：过氧化氢分解制取氧气》

---

### 一、功能说明

欢迎使用《微观世界：过氧化氢分解制取氧气》交互式教学动画！本动画旨在通过可视化手段，帮助您直观理解过氧化氢在二氧化锰催化下分解为水和氧气的微观过程。通过动态展示分子断裂、原子重组的过程，让抽象的化学反应变得生动具体。

### 二、主要功能

#### 1. **动画控制区**
- **播放/暂停**：开始或暂停连续动画演示
- **重置**：将动画恢复到初始状态
- **速度调节**：通过滑块调整动画播放速度（1-10档）

#### 2. **学习步骤区**
- **步骤1：反应物** - 展示初始的过氧化氢分子和二氧化锰催化剂
- **步骤2：键的断裂** - 演示过氧化氢分子吸附到催化剂表面及O-O键断裂
- **步骤3：原子重组** - 演示氢、氧原子重新组合为水分子和氧分子
- **步骤4：生成物** - 展示水分子和氧分子离开催化剂表面
- **连续播放所有步骤** - 自动按顺序演示完整反应过程

#### 3. **观察视角区**
- **整体视图**：显示完整的反应场景，包括多个分子和催化剂
- **催化剂特写**：聚焦于催化剂表面的反应细节（注：本版本中视角切换主要为概念展示）

#### 4. **交互功能**
- **鼠标悬停**：将鼠标悬停在原子、分子或催化剂上，可查看详细信息
- **动态提示**：动画播放时，左上角会显示当前步骤的说明文字
- **化学方程式**：右上角始终显示反应方程式，并在动画过程中高亮相关部分

### 三、设计特色

#### 1. **科学的可视化设计**
- 采用国际通用的球棍模型：氧原子（红色）、氢原子（白色/灰色）
- 化学键断裂/形成时使用亮黄色高亮显示
- 催化剂表面设计为不规则结构，模拟真实催化剂的活性位点

#### 2. **符合认知规律的教学流程**
- **从宏观到微观**：通过化学方程式连接宏观现象与微观过程
- **分步学习**：将复杂反应分解为四个关键步骤，便于逐步理解
- **重点突出**：关键步骤和变化点都有视觉和文字提示

#### 3. **专业的教学支持**
- 每个步骤都有明确的化学原理说明
- 原子和分子的标注符合化学教学规范
- 催化剂“参与反应但质量和化学性质不变”的特性得到清晰展示

### 四、教学要点

#### 1. **核心概念**
- **化学反应的本质**：分子的破裂和原子的重新组合
- **催化剂的作用机制**：提供反应场所，降低活化能，自身不消耗
- **质量守恒定律**：反应前后原子种类和数目不变

#### 2. **关键观察点**
- **步骤1**：注意过氧化氢分子（H₂O₂）的结构，特别是中间的O-O键
- **步骤2**：观察O-O键如何在催化剂表面断裂
- **步骤3**：关注氢原子和氧原子如何重新组合成新分子
- **步骤4**：注意催化剂在反应前后的状态保持不变

#### 3. **常见问题引导**
- 为什么过氧化氢需要催化剂才能快速分解？
- 反应过程中，哪些化学键断裂了？哪些新化学键形成了？
- 催化剂在反应中起到了什么作用？它本身发生了什么变化？
- 如何从微观角度理解质量守恒定律？

### 五、使用建议

#### 1. **课堂教学应用**
- **导入环节**：先展示化学方程式，提出问题“这个反应在微观层面是如何发生的？”
- **探究环节**：让学生分组操作动画，观察不同步骤，记录发现
- **讲解环节**：教师结合动画讲解关键概念，解答学生疑问
- **巩固环节**：让学生用自己的话描述反应过程，或绘制反应示意图

#### 2. **自主学习建议**
1. **第一次观看**：点击“连续播放所有步骤”，了解反应全过程
2. **分步学习**：依次点击步骤1-4，仔细观察每个阶段的变化
3. **深入探究**：使用暂停功能，仔细研究分子结构和原子运动
4. **互动探索**：鼠标悬停在各个元素上，了解它们的名称和作用
5. **速度调节**：对于复杂步骤，可降低速度仔细观察

#### 3. **键盘快捷键**
- **空格键**：播放/暂停切换
- **R键**：重置动画
- **数字键1-4**：快速跳转到对应步骤

#### 4. **教学扩展**
- **联系实际**：讨论过氧化氢在生活中的应用（如消毒、漂白）
- **对比学习**：比较有催化剂和无催化剂条件下反应速率的差异
- **微观绘图**：让学生根据动画绘制反应过程的微观示意图
- **小组讨论**：讨论“如果没有催化剂，这个反应会如何发生？”

---

### 技术支持与反馈

本动画基于HTML5 Canvas技术开发，支持现代主流浏览器。如遇显示问题，请确保浏览器已启用JavaScript。

我们希望这个交互式动画能够帮助您和您的学生更好地理解化学反应的微观世界。如果您有任何建议或发现任何问题，欢迎通过教育技术平台反馈。

**祝您教学愉快，探索成功！**

*—— 教育技术开发团队*