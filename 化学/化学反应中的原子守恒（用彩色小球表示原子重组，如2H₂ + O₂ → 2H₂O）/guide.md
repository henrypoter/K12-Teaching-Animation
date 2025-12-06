# 需求：化学反应中的原子守恒（用彩色小球表示原子重组，如2H₂ + O₂ → 2H₂O）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中或高中化学初学者，他们需要直观地理解化学反应中“原子守恒”这一核心定律。
2.  **核心需求**：用户需要摆脱抽象的化学方程式和文字描述，通过视觉化、动态化的方式，亲眼看到反应前后原子的种类和数目没有变化，只是进行了重新组合。
3.  **潜在难点**：学生可能混淆“分子被拆开”和“原子被创造或毁灭”的概念。动画需要清晰地展示分子分解为原子，原子再重新组合成新分子的两步过程。
4.  **使用场景**：适用于教师课堂演示、学生自主预习或复习，需要动画清晰、逻辑自洽、交互直观，便于理解和记忆。

#### 教学设计思路
1.  **核心概念**：聚焦于“质量守恒定律”的微观本质——原子守恒。强调化学反应是原子重新排列组合的过程，反应前后原子的种类、数目、质量均不变。
2.  **认知规律**：
    *   **从具体到抽象**：用彩色小球（具体）代表原子，用小球组合（具体）代表分子，最后关联到抽象的化学方程式。
    *   **分步演示**：将反应过程分解为清晰的三个阶段：“反应前”→“键的断裂与原子自由移动”→“键的形成与反应后”。这对应了化学反应的“碰撞-断键-成键”机理。
    *   **对比强化**：在动画前后，明确展示并对比原子的种类和数量，强化“守恒”的印象。
3.  **交互设计**：
    *   **引导式自动播放**：提供一个完整的、带解说的标准动画流程，让用户先建立整体认知。
    *   **关键步骤控制**：提供“暂停”、“下一步”、“重置”按钮，让用户能在关键节点（如断键前、成键前）停下来观察和思考。
    *   **探索式交互**：允许用户拖拽分子或原子，模拟“碰撞”以触发反应，增加参与感和趣味性。
4.  **视觉呈现**：
    *   **符号系统**：采用国际通用的球棍模型简化版。不同颜色的球代表不同原子（如：白色=H，红色=O），棍代表化学键。
    *   **动态效果**：
        *   断键时，化学键（棍）平滑断裂或消失，小球分离。
        *   原子移动时，有平滑的轨迹动画。
        *   成键时，新的化学键从小球间生长出来。
    *   **信息分层**：
        *   **主视觉区**：动态的原子和分子模型。
        *   **信息面板**：实时显示原子计数（如：H: 4, O: 2）和当前阶段的文字说明。
        *   **方程式区**：高亮与动画同步的化学方程式部分。

#### 配色方案选择
*   **原子颜色**：
    *   氢原子（H）：**浅蓝色**（或传统的白色）。避免使用过于强烈的颜色，因为氢原子小且数量多。
    *   氧原子（O）：**红色**。这是化学中表示氧的常用色，醒目且易于区分。
    *   (为扩展性预留) 碳：灰色，氮：蓝色，等。
*   **化学键**：使用**深灰色**或**黑色**的细线，清晰但不抢眼。
*   **背景**：使用**浅灰色**或**米白色**的柔和背景，确保彩色原子突出，减少视觉疲劳。
*   **UI与文字**：按钮使用简洁的蓝色系，文字使用深灰色，强调信息使用橙色或绿色。
*   **状态高亮**：被选中的分子或原子可添加**浅黄色光晕**；发生变化的区域（如断裂的键、新形成的键）可伴有短暂的**闪光效果**。

#### 交互功能列表
1.  **动画控制面板**：
    *   “播放/暂停”按钮：控制引导动画的播放。
    *   “下一步”按钮：步进式观看反应的关键阶段。
    *   “重置”按钮：将动画恢复到初始状态。
2.  **原子/分子计数器**：实时显示画面中每种原子的数量，反应前后对比，数字会随动画变化。
3.  **阶段指示器**：用文字标签（如：“反应物：2H₂ + O₂”、“键断裂”、“原子重组”、“生成物：2H₂O”）明确指示当前动画阶段。
4.  **方程式高亮同步**：化学方程式 `2H₂ + O₂ → 2H₂O` 显示在屏幕上，动画进行到哪部分，方程式对应的部分（如 `2H₂`）被高亮。
5.  **探索模式开关**：
    *   开启后，自动动画停止。
    *   用户可以用鼠标拖拽氢分子（H₂）去碰撞氧分子（O₂），当碰撞达到一定力度和角度时，触发断键和重组动画。
    *   此模式旁配有简短的文字提示：“拖拽一个H₂分子去撞击O₂分子试试看！”。
6.  **提示与解说**：一个可开关的文本框，提供每一步的简短文字解说，辅助理解。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>化学反应中的原子守恒 | 2H₂ + O₂ → 2H₂O</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #4a90e2;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 25px;
        }
        
        .main-content {
            flex: 3;
            min-width: 300px;
        }
        
        .side-panel {
            flex: 1;
            min-width: 250px;
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .animation-container {
            background-color: white;
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            margin-bottom: 20px;
            position: relative;
            overflow: hidden;
        }
        
        #canvas {
            display: block;
            margin: 0 auto;
            background-color: #f8f9fa;
            border-radius: 8px;
            cursor: pointer;
        }
        
        .controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 12px 24px;
            border: none;
            border-radius: 6px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .btn-primary {
            background-color: #4a90e2;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #3a7bc8;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: #f1f2f6;
            color: #2c3e50;
        }
        
        .btn-secondary:hover {
            background-color: #e4e6eb;
            transform: translateY(-2px);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        .btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none !important;
        }
        
        .equation-container {
            text-align: center;
            font-size: 2.2rem;
            font-weight: bold;
            margin: 25px 0;
            padding: 15px;
            background-color: #f0f7ff;
            border-radius: 8px;
            border-left: 5px solid #4a90e2;
        }
        
        .equation-part {
            padding: 5px 10px;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        
        .highlight {
            background-color: #ffeaa7;
            box-shadow: 0 0 10px rgba(255, 204, 0, 0.5);
        }
        
        .info-panel {
            margin-bottom: 25px;
        }
        
        .panel-title {
            font-size: 1.3rem;
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #ecf0f1;
        }
        
        .atom-counter {
            display: flex;
            justify-content: space-around;
            margin-bottom: 20px;
        }
        
        .atom-item {
            text-align: center;
        }
        
        .atom-circle {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin: 0 auto 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: white;
            font-size: 1.2rem;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        .hydrogen {
            background-color: #74b9ff;
        }
        
        .oxygen {
            background-color: #e17055;
        }
        
        .atom-count {
            font-size: 1.8rem;
            font-weight: bold;
            margin-top: 5px;
        }
        
        .stage-indicator {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            border-left: 4px solid #4a90e2;
        }
        
        .stage-title {
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 8px;
            font-size: 1.1rem;
        }
        
        .stage-desc {
            color: #636e72;
            font-size: 0.95rem;
        }
        
        .instructions {
            background-color: #fff9e6;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #fdcb6e;
            margin-top: 20px;
        }
        
        .instructions h3 {
            color: #e17055;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }
        
        .instructions ul {
            padding-left: 20px;
            color: #636e72;
        }
        
        .instructions li {
            margin-bottom: 8px;
        }
        
        .legend {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-top: 15px;
            flex-wrap: wrap;
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
        
        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #dfe6e9;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .controls {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
                justify-content: center;
            }
            
            .equation-container {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>化学反应中的原子守恒</h1>
        <p class="subtitle">微观视角下的质量守恒定律：2H₂ + O₂ → 2H₂O</p>
    </header>
    
    <div class="container">
        <div class="main-content">
            <div class="animation-container">
                <canvas id="canvas" width="800" height="500"></canvas>
                
                <div class="controls">
                    <button id="playBtn" class="btn btn-primary">
                        <span id="playIcon">▶</span> <span id="playText">播放动画</span>
                    </button>
                    <button id="stepBtn" class="btn btn-secondary">下一步</button>
                    <button id="resetBtn" class="btn btn-secondary">重置</button>
                    <button id="exploreBtn" class="btn btn-secondary">探索模式</button>
                </div>
            </div>
            
            <div class="equation-container">
                <span id="reactants" class="equation-part">2H₂ + O₂</span>
                <span> → </span>
                <span id="products" class="equation-part">2H₂O</span>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color hydrogen"></div>
                    <span>氢原子 (H)</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color oxygen"></div>
                    <span>氧原子 (O)</span>
                </div>
                <div class="legend-item">
                    <div style="width: 30px; height: 3px; background-color: #2d3439; margin-right: 8px;"></div>
                    <span>化学键</span>
                </div>
            </div>
        </div>
        
        <div class="side-panel">
            <div class="info-panel">
                <h2 class="panel-title">原子计数器</h2>
                <div class="atom-counter">
                    <div class="atom-item">
                        <div class="atom-circle hydrogen">H</div>
                        <div>氢原子</div>
                        <div class="atom-count" id="hCount">4</div>
                    </div>
                    <div class="atom-item">
                        <div class="atom-circle oxygen">O</div>
                        <div>氧原子</div>
                        <div class="atom-count" id="oCount">2</div>
                    </div>
                </div>
                
                <div class="stage-indicator">
                    <div class="stage-title" id="stageTitle">反应物阶段</div>
                    <div class="stage-desc" id="stageDesc">2个氢分子和1个氧分子准备反应</div>
                </div>
            </div>
            
            <div class="instructions">
                <h3>如何使用本动画</h3>
                <ul>
                    <li>点击<strong>播放动画</strong>观看完整的反应过程</li>
                    <li>使用<strong>下一步</strong>按钮分步观察反应的每个阶段</li>
                    <li>点击<strong>探索模式</strong>后，可以拖拽分子进行碰撞实验</li>
                    <li>注意观察反应前后原子的数量和种类是否变化</li>
                </ul>
            </div>
        </div>
    </div>
    
    <footer>
        <p>教学动画设计：化学反应中的原子守恒 | 基于质量守恒定律的微观解释</p>
        <p>提示：化学反应是原子重新排列组合的过程，反应前后原子的种类、数目和质量保持不变</p>
    </footer>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('canvas');
        const ctx = canvas.getContext('2d');
        
        // 获取UI元素
        const playBtn = document.getElementById('playBtn');
        const playIcon = document.getElementById('playIcon');
        const playText = document.getElementById('playText');
        const stepBtn = document.getElementById('stepBtn');
        const resetBtn = document.getElementById('resetBtn');
        const exploreBtn = document.getElementById('exploreBtn');
        const reactantsEq = document.getElementById('reactants');
        const productsEq = document.getElementById('products');
        const hCountElem = document.getElementById('hCount');
        const oCountElem = document.getElementById('oCount');
        const stageTitle = document.getElementById('stageTitle');
        const stageDesc = document.getElementById('stageDesc');
        
        // 动画状态
        let animationState = 'initial'; // initial, breaking, moving, forming, final
        let isPlaying = false;
        let isExplorationMode = false;
        let animationFrameId = null;
        let animationProgress = 0;
        const animationSpeed = 0.02;
        
        // 原子和分子定义
        const atomTypes = {
            H: { color: '#74b9ff', radius: 15, label: 'H' },
            O: { color: '#e17055', radius: 20, label: 'O' }
        };
        
        // 初始分子配置
        let molecules = [
            // 两个H₂分子
            {
                type: 'H2',
                atoms: [
                    { type: 'H', x: 200, y: 250, targetX: 200, targetY: 250, vx: 0, vy: 0 },
                    { type: 'H', x: 240, y: 250, targetX: 240, targetY: 250, vx: 0, vy: 0 }
                ],
                bonds: [[0, 1]],
                centerX: 220,
                centerY: 250,
                isDragging: false,
                dragOffsetX: 0,
                dragOffsetY: 0
            },
            {
                type: 'H2',
                atoms: [
                    { type: 'H', x: 300, y: 250, targetX: 300, targetY: 250, vx: 0, vy: 0 },
                    { type: 'H', x: 340, y: 250, targetX: 340, targetY: 250, vx: 0, vy: 0 }
                ],
                bonds: [[0, 1]],
                centerX: 320,
                centerY: 250,
                isDragging: false,
                dragOffsetX: 0,
                dragOffsetY: 0
            },
            // 一个O₂分子
            {
                type: 'O2',
                atoms: [
                    { type: 'O', x: 500, y: 250, targetX: 500, targetY: 250, vx: 0, vy: 0 },
                    { type: 'O', x: 550, y: 250, targetX: 550, targetY: 250, vx: 0, vy: 0 }
                ],
                bonds: [[0, 1]],
                centerX: 525,
                centerY: 250,
                isDragging: false,
                dragOffsetX: 0,
                dragOffsetY: 0
            }
        ];
        
        // 自由原子（反应中断键后产生）
        let freeAtoms = [];
        
        // 最终水分子
        let waterMolecules = [];
        
        // 初始化水分子目标位置
        function initWaterMolecules() {
            waterMolecules = [
                {
                    type: 'H2O',
                    atoms: [
                        { type: 'O', x: 350, y: 150, targetX: 350, y: 150, vx: 0, vy: 0 },
                        { type: 'H', x: 310, y: 190, targetX: 310, y: 190, vx: 0, vy: 0 },
                        { type: 'H', x: 390, y: 190, targetX: 390, y: 190, vx: 0, vy: 0 }
                    ],
                    bonds: [[0, 1], [0, 2]],
                    centerX: 350,
                    centerY: 170
                },
                {
                    type: 'H2O',
                    atoms: [
                        { type: 'O', x: 350, y: 350, targetX: 350, y: 350, vx: 0, vy: 0 },
                        { type: 'H', x: 310, y: 310, targetX: 310, y: 310, vx: 0, vy: 0 },
                        { type: 'H', x: 390, y: 310, targetX: 390, y: 310, vx: 0, vy: 0 }
                    ],
                    bonds: [[0, 1], [0, 2]],
                    centerX: 350,
                    centerY: 330
                }
            ];
        }
        
        // 初始化
        initWaterMolecules();
        
        // 更新原子计数器
        function updateAtomCounter() {
            let hCount = 0;
            let oCount = 0;
            
            // 统计分子中的原子
            molecules.forEach(molecule => {
                molecule.atoms.forEach(atom => {
                    if (atom.type === 'H') hCount++;
                    if (atom.type === 'O') oCount++;
                });
            });
            
            // 统计自由原子
            freeAtoms.forEach(atom => {
                if (atom.type === 'H') hCount++;
                if (atom.type === 'O') oCount++;
            });
            
            // 统计水分子中的原子
            waterMolecules.forEach(molecule => {
                molecule.atoms.forEach(atom => {
                    if (atom.type === 'H') hCount++;
                    if (atom.type === 'O') oCount++;
                });
            });
            
            hCountElem.textContent = hCount;
            oCountElem.textContent = oCount;
        }
        
        // 更新阶段指示器
        function updateStageIndicator() {
            switch(animationState) {
                case 'initial':
                    stageTitle.textContent = '反应物阶段';
                    stageDesc.textContent = '2个氢分子(H₂)和1个氧分子(O₂)准备反应';
                    reactantsEq.classList.add('highlight');
                    productsEq.classList.remove('highlight');
                    break;
                case 'breaking':
                    stageTitle.textContent = '化学键断裂';
                    stageDesc.textContent = '分子碰撞导致H-H键和O-O键断裂，生成自由原子';
                    reactantsEq.classList.add('highlight');
                    productsEq.classList.remove('highlight');
                    break;
                case 'moving':
                    stageTitle.textContent = '原子重新排列';
                    stageDesc.textContent = '氢原子和氧原子自由移动，准备形成新键';
                    reactantsEq.classList.remove('highlight');
                    productsEq.classList.remove('highlight');
                    break;
                case 'forming':
                    stageTitle.textContent = '新键形成';
                    stageDesc.textContent = '氢原子和氧原子结合形成水分子(H₂O)';
                    reactantsEq.classList.remove('highlight');
                    productsEq.classList.add('highlight');
                    break;
                case 'final':
                    stageTitle.textContent = '生成物阶段';
                    stageDesc.textContent = '形成2个水分子(H₂O)，反应前后原子种类和数量不变';
                    reactantsEq.classList.remove('highlight');
                    productsEq.classList.add('highlight');
                    break;
            }
        }
        
        // 绘制原子
        function drawAtom(x, y, type) {
            const atom = atomTypes[type];
            
            // 绘制原子球体
            ctx.beginPath();
            ctx.arc(x, y, atom.radius, 0, Math.PI * 2);
            ctx.fillStyle = atom.color;
            ctx.fill();
            
            // 绘制边框
            ctx.lineWidth = 2;
            ctx.strokeStyle = '#2d3439';
            ctx.stroke();
            
            // 绘制原子标签
            ctx.fillStyle = 'white';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText(atom.label, x, y);
        }
        
        // 绘制化学键
        function drawBond(x1, y1, x2, y2, isBreaking = false) {
            ctx.beginPath();
            ctx.moveTo(x1, y1);
            
            // 如果键正在断裂，绘制虚线
            if (isBreaking && animationState === 'breaking') {
                const dx = x2 - x1;
                const dy = y2 - y1;
                const distance = Math.sqrt(dx * dx + dy * dy);
                const dashLength = 10;
                const dashGap = 5;
                const steps = Math.floor(distance / (dashLength + dashGap));
                
                for (let i = 0; i <= steps; i++) {
                    const startRatio = i / steps;
                    const endRatio = Math.min((i + 0.7) / steps, 1);
                    
                    const startX = x1 + dx * startRatio;
                    const startY = y1 + dy * startRatio;
                    const endX = x1 + dx * endRatio;
                    const endY = y1 + dy * endRatio;
                    
                    ctx.moveTo(startX, startY);
                    ctx.lineTo(endX, endY);
                }
            } else {
                ctx.lineTo(x2, y2);
            }
            
            ctx.lineWidth = 4;
            ctx.strokeStyle = '#2d3439';
            ctx.stroke();
        }
        
        // 绘制分子
        function drawMolecule(molecule) {
            // 绘制化学键
            molecule.bonds.forEach(bond => {
                const atom1 = molecule.atoms[bond[0]];
                const atom2 = molecule.atoms[bond[1]];
                const isBreaking = animationState === 'breaking' && animationProgress > 0.3;
                drawBond(atom1.x, atom1.y, atom2.x, atom2.y, isBreaking);
            });
            
            // 绘制原子
            molecule.atoms.forEach(atom => {
                drawAtom(atom.x, atom.y, atom.type);
            });
            
            // 如果分子正在被拖拽，绘制高亮效果
            if (molecule.isDragging) {
                ctx.beginPath();
                ctx.arc(molecule.centerX, molecule.centerY, 50, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(255, 234, 167, 0.3)';
                ctx.fill();
            }
        }
        
        // 绘制自由原子
        function drawFreeAtoms() {
            freeAtoms.forEach(atom => {
                drawAtom(atom.x, atom.y, atom.type);
            });
        }
        
        // 绘制所有内容
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景网格（辅助参考）
            ctx.strokeStyle = 'rgba(0, 0, 0, 0.05)';
            ctx.lineWidth = 1;
            
            // 垂直网格线
            for (let x = 50; x < canvas.width; x += 50) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, canvas.height);
                ctx.stroke();
            }
            
            // 水平网格线
            for (let y = 50; y < canvas.height; y += 50) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(canvas.width, y);
                ctx.stroke();
            }
            
            // 根据动画状态绘制不同内容
            if (animationState === 'initial' || animationState === 'breaking') {
                // 绘制初始分子
                molecules.forEach(molecule => {
                    drawMolecule(molecule);
                });
            } else if (animationState === 'moving') {
                // 绘制自由原子
                drawFreeAtoms();
            } else if (animationState === 'forming' || animationState === 'final') {
                // 绘制水分子
                waterMolecules.forEach(molecule => {
                    drawMolecule(molecule);
                });
            }
            
            // 绘制反应箭头
            drawReactionArrow();
        }
        
        // 绘制反应箭头
        function drawReactionArrow() {
            const arrowY = canvas.height - 50;
            
            // 绘制箭头线
            ctx.beginPath();
            ctx.moveTo(100, arrowY);
            ctx.lineTo(700, arrowY);
            ctx.lineWidth = 3;
            ctx.strokeStyle = '#4a90e2';
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(700, arrowY);
            ctx.lineTo(680, arrowY - 10);
            ctx.lineTo(680, arrowY + 10);
            ctx.closePath();
            ctx.fillStyle = '#4a90e2';
            ctx.fill();
            
            // 添加文字标签
            ctx.fillStyle = '#4a90e2';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('化学反应过程', 400, arrowY - 20);
        }
        
        // 动画更新逻辑
        function updateAnimation() {
            if (!isPlaying) return;
            
            animationProgress += animationSpeed;
            
            if (animationProgress >= 1) {
                animationProgress = 1;
                
                // 进入下一阶段
                if (animationState === 'initial') {
                    animationState = 'breaking';
                    animationProgress = 0;
                } else if (animationState === 'breaking') {
                    // 键断裂后，生成自由原子
                    freeAtoms = [];
                    molecules.forEach(molecule => {
                        molecule.atoms.forEach(atom => {
                            freeAtoms.push({
                                type: atom.type,
                                x: atom.x,
                                y: atom.y,
                                targetX: atom.x + (Math.random() - 0.5) * 100,
                                targetY: atom.y + (Math.random() - 0.5) * 100,
                                vx: 0,
                                vy: 0
                            });
                        });
                    });
                    molecules = [];
                    animationState = 'moving';
                    animationProgress = 0;
                } else if (animationState === 'moving') {
                    animationState = 'forming';
                    animationProgress = 0;
                } else if (animationState === 'forming') {
                    animationState = 'final';
                    animationProgress = 0;
                    isPlaying = false;
                    playIcon.textContent = '↻';
                    playText.textContent = '重新播放';
                }
            }
            
            // 根据当前状态和进度更新位置
            if (animationState === 'breaking') {
                // 分子振动效果
                molecules.forEach(molecule => {
                    molecule.atoms.forEach(atom => {
                        atom.x = atom.targetX + Math.sin(animationProgress * 10) * 5;
                        atom.y = atom.targetY + Math.cos(animationProgress * 8) * 5;
                    });
                });
            } else if (animationState === 'moving') {
                // 自由原子移动
                freeAtoms.forEach(atom => {
                    // 简单缓动动画
                    atom.x += (atom.targetX - atom.x) * 0.05;
                    atom.y += (atom.targetY - atom.y) * 0.05;
                });
            } else if (animationState === 'forming') {
                // 水分子形成动画
                waterMolecules.forEach((molecule, index) => {
                    molecule.atoms.forEach((atom, atomIndex) => {
                        // 从自由原子位置移动到水分子位置
                        const startX = 400 + (index === 0 ? -50 : 50);
                        const startY = 250 + (index === 0 ? -100 : 100);
                        
                        atom.x = startX + (atom.targetX - startX) * animationProgress;
                        atom.y = startY + (atom.targetY - startY) * animationProgress;
                    });
                });
            }
            
            // 更新UI
            updateAtomCounter();
            updateStageIndicator();
            
            // 重绘
            draw();
            
            // 继续动画循环
            if (isPlaying) {
                animationFrameId = requestAnimationFrame(updateAnimation);
            }
        }
        
        // 开始/暂停动画
        function togglePlay() {
            if (isExplorationMode) {
                alert('请先退出探索模式以观看自动动画');
                return;
            }
            
            isPlaying = !isPlaying;
            
            if (isPlaying) {
                playIcon.textContent = '⏸';
                playText.textContent = '暂停动画';
                
                // 如果动画已经结束，重新开始
                if (animationState === 'final') {
                    resetAnimation();
                    animationState = 'initial';
                }
                
                animationFrameId = requestAnimationFrame(updateAnimation);
            } else {
                playIcon.textContent = '▶';
                playText.textContent = '继续播放';
                if (animationFrameId) {
                    cancelAnimationFrame(animationFrameId);
                }
            }
        }
        
        // 下一步
        function nextStep() {
            if (isExplorationMode) {
                alert('请先退出探索模式以使用步进功能');
                return;
            }
            
            if (isPlaying) {
                isPlaying = false;
                playIcon.textContent = '▶';
                playText.textContent = '继续播放';
                if (animationFrameId) {
                    cancelAnimationFrame(animationFrameId);
                }
            }
            
            // 根据当前状态进入下一阶段
            if (animationState === 'initial') {
                animationState = 'breaking';
                animationProgress = 0;
            } else if (animationState === 'breaking') {
                // 键断裂后，生成自由原子
                freeAtoms = [];
                molecules.forEach(molecule => {
                    molecule.atoms.forEach(atom => {
                        freeAtoms.push({
                            type: atom.type,
                            x: atom.x,
                            y: atom.y,
                            targetX: atom.x + (Math.random() - 0.5) * 100,
                            targetY: atom.y + (Math.random() - 0.5) * 100,
                            vx: 0,
                            vy: 0
                        });
                    });
                });
                molecules = [];
                animationState = 'moving';
                animationProgress = 0;
            } else if (animationState === 'moving') {
                animationState = 'forming';
                animationProgress = 0;
            } else if (animationState === 'forming') {
                animationState = 'final';
                animationProgress = 1;
            } else if (animationState === 'final') {
                resetAnimation();
                animationState = 'initial';
            }
            
            // 更新UI并重绘
            updateAtomCounter();
            updateStageIndicator();
            draw();
        }
        
        // 重置动画
        function resetAnimation() {
            if (isPlaying) {
                isPlaying = false;
                playIcon.textContent = '▶';
                playText.textContent = '播放动画';
                if (animationFrameId) {
                    cancelAnimationFrame(animationFrameId);
                }
            }
            
            // 重置状态
            animationState = 'initial';
            animationProgress = 0;
            isExplorationMode = false;
            exploreBtn.textContent = '探索模式';
            exploreBtn.classList.remove('btn-primary');
            exploreBtn.classList.add('btn-secondary');
            
            // 重置分子
            molecules = [
                {
                    type: 'H2',
                    atoms: [
                        { type: 'H', x: 200, y: 250, targetX: 200, targetY: 250, vx: 0, vy: 0 },
                        { type: 'H', x: 240, y: 250, targetX: 240, targetY: 250, vx: 0, vy: 0 }
                    ],
                    bonds: [[0, 1]],
                    centerX: 220,
                    centerY: 250,
                    isDragging: false,
                    dragOffsetX: 0,
                    dragOffsetY: 0
                },
                {
                    type: 'H2',
                    atoms: [
                        { type: 'H', x: 300, y: 250, targetX: 300, targetY: 250, vx: 0, vy: 0 },
                        { type: 'H', x: 340, y: 250, targetX: 340, targetY: 250, vx: 0, vy: 0 }
                    ],
                    bonds: [[0, 1]],
                    centerX: 320,
                    centerY: 250,
                    isDragging: false,
                    dragOffsetX: 0,
                    dragOffsetY: 0
                },
                {
                    type: 'O2',
                    atoms: [
                        { type: 'O', x: 500, y: 250, targetX: 500, targetY: 250, vx: 0, vy: 0 },
                        { type: 'O', x: 550, y: 250, targetX: 550, targetY: 250, vx: 0, vy: 0 }
                    ],
                    bonds: [[0, 1]],
                    centerX: 525,
                    centerY: 250,
                    isDragging: false,
                    dragOffsetX: 0,
                    dragOffsetY: 0
                }
            ];
            
            // 清空自由原子和水分子
            freeAtoms = [];
            initWaterMolecules();
            
            // 更新UI并重绘
            updateAtomCounter();
            updateStageIndicator();
            draw();
        }
        
        // 切换探索模式
        function toggleExplorationMode() {
            if (isPlaying) {
                isPlaying = false;
                playIcon.textContent = '▶';
                playText.textContent = '播放动画';
                if (animationFrameId) {
                    cancelAnimationFrame(animationFrameId);
                }
            }
            
            isExplorationMode = !isExplorationMode;
            
            if (isExplorationMode) {
                exploreBtn.textContent = '退出探索';
                exploreBtn.classList.remove('btn-secondary');
                exploreBtn.classList.add('btn-primary');
                stageTitle.textContent = '探索模式';
                stageDesc.textContent = '拖拽分子进行碰撞实验，观察反应如何发生';
            } else {
                exploreBtn.textContent = '探索模式';
                exploreBtn.classList.remove('btn-primary');
                exploreBtn.classList.add('btn-secondary');
                updateStageIndicator();
                
                // 重置拖拽状态
                molecules.forEach(molecule => {
                    molecule.isDragging = false;
                });
            }
            
            draw();
        }
        
        // 检查分子碰撞
        function checkMoleculeCollision() {
            if (!isExplorationMode || molecules.length < 3) return;
            
            // 检查两个H₂分子和O₂分子是否足够接近
            const h2Molecules = molecules.filter(m => m.type === 'H2');
            const o2Molecule = molecules.find(m => m.type === 'O2');
            
            if (h2Molecules.length < 2 || !o2Molecule) return;
            
            // 检查两个H₂分子是否都与O₂分子碰撞
            let collisionCount = 0;
            h2Molecules.forEach(h2 => {
                const dx = h2.centerX - o2Molecule.centerX;
                const dy = h2.centerY - o2Molecule.centerY;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance < 80) {
                    collisionCount++;
                }
            });
            
            // 如果两个H₂分子都与O₂分子碰撞，触发反应
            if (collisionCount >= 2) {
                // 进入反应动画
                isExplorationMode = false;
                exploreBtn.textContent = '探索模式';
                exploreBtn.classList.remove('btn-primary');
                exploreBtn.classList.add('btn-secondary');
                
                // 开始自动动画
                animationState = 'breaking';
                animationProgress = 0;
                isPlaying = true;
                playIcon.textContent = '⏸';
                playText.textContent = '暂停动画';
                animationFrameId = requestAnimationFrame(updateAnimation);
            }
        }
        
        // 鼠标事件处理
        let isDragging = false;
        let draggedMolecule = null;
        
        canvas.addEventListener('mousedown', function(e) {
            if (!isExplorationMode) return;
            
            const rect = canvas.getBoundingClientRect();
            const mouseX = e.clientX - rect.left;
            const mouseY = e.clientY - rect.top;
            
            // 检查是否点击了分子
            for (let i = 0; i < molecules.length; i++) {
                const molecule = molecules[i];
                const dx = mouseX - molecule.centerX;
                const dy = mouseY - molecule.centerY;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance < 40) {
                    isDragging = true;
                    draggedMolecule = molecule;
                    molecule.isDragging = true;
                    molecule.dragOffsetX = mouseX - molecule.centerX;
                    molecule.dragOffsetY = mouseY - molecule.centerY;
                    break;
                }
            }
            
            draw();
        });
        
        canvas.addEventListener('mousemove', function(e) {

<!--检测到代码截断，自动续写中...-->
if (!isExplorationMode || !isDragging || !draggedMolecule) return;
            
            const rect = canvas.getBoundingClientRect();
            const mouseX = e.clientX - rect.left;
            const mouseY = e.clientY - rect.top;
            
            // 更新被拖拽分子的位置
            draggedMolecule.centerX = mouseX - draggedMolecule.dragOffsetX;
            draggedMolecule.centerY = mouseY - draggedMolecule.dragOffsetY;
            
            // 更新分子中原子的位置
            const atomOffsetX = draggedMolecule.type === 'H2' ? 20 : 25;
            draggedMolecule.atoms[0].x = draggedMolecule.centerX - atomOffsetX;
            draggedMolecule.atoms[0].y = draggedMolecule.centerY;
            draggedMolecule.atoms[0].targetX = draggedMolecule.centerX - atomOffsetX;
            draggedMolecule.atoms[0].targetY = draggedMolecule.centerY;
            
            draggedMolecule.atoms[1].x = draggedMolecule.centerX + atomOffsetX;
            draggedMolecule.atoms[1].y = draggedMolecule.centerY;
            draggedMolecule.atoms[1].targetX = draggedMolecule.centerX + atomOffsetX;
            draggedMolecule.atoms[1].targetY = draggedMolecule.centerY;
            
            // 检查碰撞
            checkMoleculeCollision();
            
            draw();
        });
        
        canvas.addEventListener('mouseup', function() {
            if (!isExplorationMode) return;
            
            if (isDragging && draggedMolecule) {
                draggedMolecule.isDragging = false;
            }
            
            isDragging = false;
            draggedMolecule = null;
            
            draw();
        });
        
        canvas.addEventListener('mouseleave', function() {
            if (!isExplorationMode) return;
            
            if (isDragging && draggedMolecule) {
                draggedMolecule.isDragging = false;
            }
            
            isDragging = false;
            draggedMolecule = null;
            
            draw();
        });
        
        // 触摸事件支持（移动设备）
        canvas.addEventListener('touchstart', function(e) {
            if (!isExplorationMode) return;
            
            e.preventDefault();
            const rect = canvas.getBoundingClientRect();
            const touch = e.touches[0];
            const mouseX = touch.clientX - rect.left;
            const mouseY = touch.clientY - rect.top;
            
            // 检查是否点击了分子
            for (let i = 0; i < molecules.length; i++) {
                const molecule = molecules[i];
                const dx = mouseX - molecule.centerX;
                const dy = mouseY - molecule.centerY;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance < 40) {
                    isDragging = true;
                    draggedMolecule = molecule;
                    molecule.isDragging = true;
                    molecule.dragOffsetX = mouseX - molecule.centerX;
                    molecule.dragOffsetY = mouseY - molecule.centerY;
                    break;
                }
            }
            
            draw();
        });
        
        canvas.addEventListener('touchmove', function(e) {
            if (!isExplorationMode || !isDragging || !draggedMolecule) return;
            
            e.preventDefault();
            const rect = canvas.getBoundingClientRect();
            const touch = e.touches[0];
            const mouseX = touch.clientX - rect.left;
            const mouseY = touch.clientY - rect.top;
            
            // 更新被拖拽分子的位置
            draggedMolecule.centerX = mouseX - draggedMolecule.dragOffsetX;
            draggedMolecule.centerY = mouseY - draggedMolecule.dragOffsetY;
            
            // 更新分子中原子的位置
            const atomOffsetX = draggedMolecule.type === 'H2' ? 20 : 25;
            draggedMolecule.atoms[0].x = draggedMolecule.centerX - atomOffsetX;
            draggedMolecule.atoms[0].y = draggedMolecule.centerY;
            draggedMolecule.atoms[0].targetX = draggedMolecule.centerX - atomOffsetX;
            draggedMolecule.atoms[0].targetY = draggedMolecule.centerY;
            
            draggedMolecule.atoms[1].x = draggedMolecule.centerX + atomOffsetX;
            draggedMolecule.atoms[1].y = draggedMolecule.centerY;
            draggedMolecule.atoms[1].targetX = draggedMolecule.centerX + atomOffsetX;
            draggedMolecule.atoms[1].targetY = draggedMolecule.centerY;
            
            // 检查碰撞
            checkMoleculeCollision();
            
            draw();
        });
        
        canvas.addEventListener('touchend', function() {
            if (!isExplorationMode) return;
            
            if (isDragging && draggedMolecule) {
                draggedMolecule.isDragging = false;
            }
            
            isDragging = false;
            draggedMolecule = null;
            
            draw();
        });
        
        // 按钮事件监听
        playBtn.addEventListener('click', togglePlay);
        stepBtn.addEventListener('click', nextStep);
        resetBtn.addEventListener('click', resetAnimation);
        exploreBtn.addEventListener('click', toggleExplorationMode);
        
        // 初始绘制
        updateAtomCounter();
        updateStageIndicator();
        draw();
        
        // 窗口大小调整处理
        window.addEventListener('resize', function() {
            // 保持Canvas尺寸不变，或根据需要调整
            draw();
        });
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## 交互式教学动画《化学反应中的原子守恒》使用指南

欢迎使用本交互式教学动画！本动画旨在通过直观、动态的可视化方式，帮助您深入理解化学反应中“原子守恒”这一核心概念。无论您是教师用于课堂演示，还是学生用于自主学习，本工具都将为您提供生动、深刻的学习体验。

---

### 一、 功能说明

本动画以氢气与氧气反应生成水（2H₂ + O₂ → 2H₂O）为例，通过彩色小球（原子）和连接棒（化学键）的模型，动态展示了化学反应过程中分子分解、原子重组、新分子形成的全过程。核心目标是让您亲眼见证：**反应前后，原子的种类和数量没有发生任何变化，只是进行了重新排列组合**。

### 二、 主要功能

1.  **自动动画演示**：
    *   **播放/暂停**：点击“播放动画”按钮，观看从反应物到生成物的完整、连贯的动画过程，伴有阶段提示和方程式高亮。
    *   **重新播放**：动画结束后，按钮变为“重新播放”，可一键从头开始。

2.  **分步学习控制**：
    *   **下一步**：如果您希望仔细研究反应的每一个关键阶段，可以使用“下一步”按钮。动画将分为“反应物→键断裂→原子移动→键形成→生成物”五个步骤，让您在每个环节停下来观察和思考。

3.  **探索与实验模式**：
    *   **探索模式**：点击此按钮进入互动实验模式。在此模式下，您可以**用鼠标拖拽画面中的氢分子（H₂）去碰撞氧分子（O₂）**。
    *   **触发反应**：当两个H₂分子都与O₂分子足够接近时，系统会自动触发完整的化学反应动画，模拟真实的分子碰撞反应过程。

4.  **实时信息反馈**：
    *   **原子计数器**：右侧面板实时显示画面中氢原子和氧原子的总数。无论动画进行到哪一步，您都可以直观地看到原子总数始终保持不变。
    *   **阶段指示器**：清晰标明当前动画所处的阶段，并配有简短的文字说明，解释该阶段发生的微观过程。
    *   **方程式高亮**：上方的化学方程式 `2H₂ + O₂ → 2H₂O` 会随着动画进展同步高亮，将微观现象与宏观符号（化学方程式）紧密联系起来。

5.  **一键重置**：
    *   点击“重置”按钮，随时将动画恢复到初始状态，方便进行多次观看或演示。

### 三、 设计特色

1.  **符合认知规律的视觉设计**：
    *   **色彩编码**：采用化学中常用的配色方案（浅蓝色代表氢原子H，红色代表氧原子O），易于识别和记忆。
    *   **球棍模型简化**：使用国际通用的球棍模型简化形式，直观表现原子和化学键。
    *   **平滑动画**：化学键的断裂、原子的移动、新键的形成均采用平滑过渡动画，符合物理直觉。

2.  **多层次的信息呈现**：
    *   将动态模型（主画面）、定量数据（原子计数）、定性描述（阶段说明）和化学符号（方程式）有机结合，满足不同学习风格的需求。

3.  **引导与探索相结合**：
    *   既提供了结构清晰的“引导式”自动演示，帮助建立正确概念；又提供了开放的“探索式”互动，激发好奇心和探究欲。

### 四、 教学要点

在使用本动画进行教学或学习时，建议重点关注以下核心概念：

1.  **原子是化学反应中的最小微粒**：动画清晰地展示了分子（如H₂， O₂）在反应中被“拆开”成独立的原子，而这些原子本身并未被破坏。
2.  **原子守恒是质量守恒的微观本质**：请时刻关注右侧的“原子计数器”。无论反应如何剧烈进行，氢原子和氧原子的总数从始至终都保持不变。这就是化学反应前后总质量不变的微观原因。
3.  **化学反应是旧键断裂、新键形成的过程**：注意观察“键断裂”阶段化学键的消失，以及“新键形成”阶段新化学键（H-O键）的产生。理解能量变化与化学键断裂和形成的关系。
4.  **化学方程式是对微观过程的宏观表征**：引导学习者将动画中的每一步（2个H₂分子 + 1个O₂分子 → 2个H₂O分子）与上方的化学方程式 `2H₂ + O₂ → 2H₂O` 对应起来，理解方程式的系数和符号所代表的微观意义。

### 五、 使用建议

*   **对于教师**：
    *   **课堂演示**：可在大屏幕上播放完整动画，作为引入“质量守恒定律”或“化学反应本质”的精彩开场。
    *   **分步讲解**：使用“下一步”功能，在每一个关键阶段暂停，向学生提问（例如：“现在化学键发生了什么变化？”“原子的数量变了吗？”），进行深入的课堂互动。
    *   **小组探究**：让学生以小组形式进入“探索模式”，尝试拖拽分子并讨论“如何才能成功引发反应”，从而理解反应发生的条件（如有效碰撞）。
*   **对于学生**：
    *   **预习**：先观看一遍完整动画，对反应过程有一个整体印象。
    *   **深入学习**：使用“下一步”功能，逐步观看，并结合右侧的说明文字，理解每一个步骤。
    *   **自我检测**：在观看过程中或观看后，尝试回答：反应前后各有几种原子？每种原子各有几个？水分子是如何构成的？
    *   **趣味探索**：一定要试试“探索模式”，亲自“动手”让分子碰撞，体验化学反应的触发过程。

---

我们希望这个交互式动画能成为您探索化学微观世界的得力助手。通过直观的视觉体验和有趣的互动操作，让“原子守恒”这个抽象的概念变得生动具体，深入人心。祝您学习愉快，探索无限！