# 需求：AVL树四种旋转（LL、RR、LR、RL）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户是学习数据结构与算法（如计算机科学、软件工程专业）的大学生或自学者。他们已经了解二叉搜索树（BST）的基本概念，并初次接触AVL树的自平衡机制。他们的核心痛点和需求是：
1.  **理解失衡与旋转的因果关系**：难以直观理解为什么在特定失衡情况下（LL， RR， LR， RL）需要执行对应的旋转操作来恢复平衡。
2.  **掌握旋转的操作步骤**：对旋转过程中节点指针的调整感到抽象和困惑，需要清晰的、分步的演示。
3.  **区分四种旋转类型**：容易混淆LR和RL等复合旋转，需要对比学习，明确每种类型的触发条件和最终形态。
4.  **从抽象到具体的映射**：需要将教材/伪代码中的描述与动态的树形结构变化联系起来，形成深刻记忆。

因此，教学动画的核心目标是：**将抽象的旋转规则，转化为直观、可控的视觉变化过程，降低认知负荷，促进理解与记忆。**

#### 教学设计思路

*   **核心概念聚焦**：
    *   **平衡因子**：作为动画的“驱动信号”。高亮显示关键节点的平衡因子计算（左子树高 - 右子树高），并明确标注何时 |BF| > 1（失衡）。
    *   **最小失衡子树**：明确旋转操作的作用范围，动画应聚焦于这棵子树，与树的其余部分区分开。
    *   **旋转操作**：分解为“识别失衡类型” -> “确定支点（旋转中心）” -> “执行指针重连” 三个逻辑阶段。

*   **遵循认知规律**：
    1.  **从实例引入**：从一个具体的、逐步插入节点导致失衡的AVL树开始，而非直接展示旋转。
    2.  **分步演示**：将一次旋转分解为多个关键帧（如：标识失衡节点 -> 展示旋转轴 -> 中间状态 -> 最终状态），允许用户按步骤前进/后退。
    3.  **对比与归纳**：并排展示四种旋转的典型案例，让用户自主发现“LL与RR对称”、“LR与RL对称”的规律。
    4.  **从观察到实践**：在讲解后，提供“沙盒模式”，让用户自由插入/删除节点，观察树的自动平衡过程，深化理解。

*   **交互设计**：
    *   **流程控制**：提供“上一步”、“下一步”、“重置”按钮，让用户掌控学习节奏。
    *   **模式切换**：在“教学演示模式”（引导式分步学习四种旋转）和“自由实验模式”（手动操作，观察整体平衡）间切换。
    *   **焦点与提示**：在每一步，通过高亮、箭头、浮动标签等方式，提示用户当前关注点（例如：“节点A的平衡因子为+2，发生LL型失衡”）。
    *   **速度调节**：动画速度可调，满足不同用户的观察需求。

*   **视觉呈现**：
    *   **树形结构**：采用清晰、美观的树状图，节点大小适中，连线明确。
    *   **状态编码**：
        *   **颜色**：平衡节点用中性色（如浅蓝），失衡节点用警示色（如橙色），当前正在操作的节点或连线用强调色（如亮绿色）。
        *   **标签**：每个节点内显示**键值**和**平衡因子**。
        *   **动画**：节点的移动轨迹平滑，指针（连线）的变化通过旧连线的淡出和新连线的绘制来表现，避免视觉混乱。
    *   **信息面板**：侧边或底部保留一个区域，用文字描述当前步骤的原理或对应伪代码。

#### 配色方案选择
选择对比清晰、舒适且符合认知习惯的配色方案：
*   **背景与画布**：深灰色（`#2d2d2d`）或浅灰色（`#f5f5f5`），确保与前景元素有足够对比。
*   **节点**：
    *   默认状态：浅蓝色（`#a0c4ff`），柔和且专业。
    *   失衡状态：橙色（`#ff9a76`），引起注意。
    *   当前操作节点/根节点：亮绿色（`#90ee90`）或明黄色（`#ffde7d`），突出焦点。
*   **连线（指针）**：
    *   默认状态：深灰色（`#666`）。
    *   待更改/旧指针：半透明红色（`rgba(255, 100, 100, 0.7)`），淡出消失。
    *   新建立指针：绿色（`#4caf50`），绘制出现。
*   **文本与界面**：白色（深色背景下）或深灰色（浅色背景下），确保可读性。
*   **控制按钮**：采用扁平化设计，主行动按钮（如“下一步”）用主题色（如`#4a6fa5`）。

#### 交互功能列表
1.  **主控制面板**：
    *   “上一步” / “下一步”：在分步教学中导航。
    *   “播放/暂停”：自动播放整个旋转过程。
    *   “重置”：将动画恢复到当前示例的初始状态。
    *   “速度调节滑块”：控制动画播放速度。

2.  **示例选择器**：
    *   下拉菜单或按钮组，用于选择要学习的旋转类型（LL， RR， LR， RL）。选择后，场景重置为该类型的经典失衡案例。

3.  **信息显示面板**：
    *   显示当前旋转类型的名称和简介。
    *   动态更新，描述当前步骤在做什么（例如：“第一步：发现节点A（键值=30）平衡因子为+2，属于LL型失衡”）。
    *   可选项：显示当前步骤对应的算法伪代码。

4.  **视觉提示开关**（可选）：
    *   复选框，用于显示/隐藏平衡因子、高亮效果、旋转路径指示线等。

5.  **模式切换器**：
    *   “教学模式”按钮：进入结构化的分步学习流程。
    *   “实验模式”按钮：进入一个交互式沙盒。在该模式下，用户可以通过按钮或输入框插入/删除指定键值的节点，系统自动展示AVL树如何通过旋转保持平衡。此模式提供“撤销”功能。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AVL树旋转动画教学</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #2d2d2d;
            color: #e0e0e0;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            padding: 20px;
        }

        header {
            text-align: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #444;
        }

        h1 {
            color: #a0c4ff;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #aaa;
            font-size: 1.1rem;
        }

        .container {
            display: flex;
            flex: 1;
            gap: 20px;
            flex-wrap: wrap;
        }

        .main-panel {
            flex: 3;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            background-color: #363636;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .control-panel {
            flex: 1;
            min-width: 250px;
            background-color: #363636;
            border-radius: 10px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .canvas-container {
            flex: 1;
            position: relative;
            border: 1px solid #555;
            border-radius: 8px;
            overflow: hidden;
            background-color: #2d2d2d;
            min-height: 500px;
        }

        #treeCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }

        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #444;
        }

        button {
            padding: 10px 15px;
            background-color: #4a6fa5;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.2s, transform 0.1s;
            flex: 1;
            min-width: 120px;
        }

        button:hover {
            background-color: #5a7fb5;
        }

        button:active {
            transform: scale(0.98);
        }

        button.primary {
            background-color: #4caf50;
        }

        button.primary:hover {
            background-color: #5cbf60;
        }

        button.secondary {
            background-color: #ff9a76;
        }

        button.secondary:hover {
            background-color: #ffaa86;
        }

        .example-selector {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }

        .example-btn {
            padding: 12px;
            background-color: #444;
            border: 2px solid #555;
        }

        .example-btn.active {
            border-color: #a0c4ff;
            background-color: #505050;
        }

        .info-panel {
            background-color: #404040;
            border-radius: 8px;
            padding: 15px;
            margin-top: 10px;
            flex: 1;
            overflow-y: auto;
            max-height: 200px;
        }

        .info-title {
            color: #ffde7d;
            margin-bottom: 10px;
            font-size: 1.2rem;
        }

        .step-info {
            line-height: 1.6;
            margin-bottom: 8px;
        }

        .step-info.highlight {
            color: #90ee90;
            font-weight: bold;
        }

        .balance-factor {
            display: inline-block;
            background-color: #555;
            padding: 2px 6px;
            border-radius: 3px;
            font-family: monospace;
            margin: 0 3px;
        }

        .slider-container {
            margin-top: 10px;
        }

        .slider-container label {
            display: block;
            margin-bottom: 5px;
            color: #aaa;
        }

        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: #555;
            outline: none;
        }

        .mode-selector {
            display: flex;
            border-radius: 5px;
            overflow: hidden;
            border: 1px solid #555;
        }

        .mode-btn {
            flex: 1;
            border-radius: 0;
            min-width: auto;
            background-color: #444;
        }

        .mode-btn.active {
            background-color: #4a6fa5;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 10px;
            padding: 10px;
            background-color: #404040;
            border-radius: 5px;
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
        }

        footer {
            text-align: center;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #444;
            color: #888;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .controls {
                justify-content: center;
            }
            
            button {
                min-width: 100px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>AVL树旋转动画教学</h1>
        <p class="subtitle">可视化学习LL、RR、LR、RL四种旋转操作</p>
    </header>

    <div class="container">
        <div class="main-panel">
            <div class="canvas-container">
                <canvas id="treeCanvas"></canvas>
            </div>
            
            <div class="controls">
                <button id="prevBtn">上一步</button>
                <button id="nextBtn" class="primary">下一步</button>
                <button id="playPauseBtn">播放</button>
                <button id="resetBtn">重置</button>
                <button id="modeToggle" class="secondary">切换到实验模式</button>
            </div>
            
            <div class="slider-container">
                <label for="speedSlider">动画速度: <span id="speedValue">中速</span></label>
                <input type="range" id="speedSlider" min="1" max="10" value="5">
            </div>
        </div>
        
        <div class="control-panel">
            <div>
                <h3>旋转类型示例</h3>
                <div class="example-selector">
                    <button class="example-btn active" data-type="LL">LL型旋转</button>
                    <button class="example-btn" data-type="RR">RR型旋转</button>
                    <button class="example-btn" data-type="LR">LR型旋转</button>
                    <button class="example-btn" data-type="RL">RL型旋转</button>
                </div>
            </div>
            
            <div class="info-panel">
                <div class="info-title">当前步骤说明</div>
                <div id="stepInfo">
                    <div class="step-info">请选择一个旋转类型开始学习。</div>
                </div>
            </div>
            
            <div>
                <h3>学习模式</h3>
                <div class="mode-selector">
                    <button class="mode-btn active" data-mode="teach">教学模式</button>
                    <button class="mode-btn" data-mode="experiment">实验模式</button>
                </div>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #a0c4ff;"></div>
                    <div class="legend-text">平衡节点</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #ff9a76;"></div>
                    <div class="legend-text">失衡节点</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #90ee90;"></div>
                    <div class="legend-text">当前焦点</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #4caf50;"></div>
                    <div class="legend-text">新指针</div>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>AVL树旋转动画教学 | 使用Canvas实现 | 设计：熊猫老师</p>
    </footer>

    <script>
        // 全局变量
        const canvas = document.getElementById('treeCanvas');
        const ctx = canvas.getContext('2d');
        const stepInfoDiv = document.getElementById('stepInfo');
        
        // 树节点类
        class TreeNode {
            constructor(value, x, y) {
                this.value = value;
                this.height = 1;
                this.left = null;
                this.right = null;
                this.x = x;
                this.y = y;
                this.targetX = x;
                this.targetY = y;
                this.color = '#a0c4ff'; // 默认颜色
                this.isImbalanced = false;
                this.isFocused = false;
            }
            
            // 计算平衡因子
            getBalanceFactor() {
                const leftHeight = this.left ? this.left.height : 0;
                const rightHeight = this.right ? this.right.height : 0;
                return leftHeight - rightHeight;
            }
            
            // 更新高度
            updateHeight() {
                const leftHeight = this.left ? this.left.height : 0;
                const rightHeight = this.right ? this.right.height : 0;
                this.height = Math.max(leftHeight, rightHeight) + 1;
            }
        }

        // AVL树动画管理器
        class AVLTreeAnimation {
            constructor() {
                this.root = null;
                this.nodes = [];
                this.currentStep = 0;
                this.totalSteps = 0;
                this.isPlaying = false;
                this.animationSpeed = 5; // 1-10
                this.animationFrameId = null;
                this.currentExample = 'LL';
                this.currentMode = 'teach'; // 'teach' 或 'experiment'
                this.stepDescriptions = [];
                this.highlightedNodes = [];
                this.newEdges = [];
                this.oldEdges = [];
                
                // 初始化画布大小
                this.resizeCanvas();
                window.addEventListener('resize', () => this.resizeCanvas());
                
                // 初始化示例
                this.loadExample('LL');
                
                // 开始动画循环
                this.animate();
            }
            
            // 调整画布大小
            resizeCanvas() {
                const container = canvas.parentElement;
                canvas.width = container.clientWidth;
                canvas.height = container.clientHeight;
                this.redraw();
            }
            
            // 加载示例
            loadExample(type) {
                this.currentExample = type;
                this.currentStep = 0;
                this.isPlaying = false;
                this.nodes = [];
                this.highlightedNodes = [];
                this.newEdges = [];
                this.oldEdges = [];
                
                // 根据类型创建不同的示例树
                switch(type) {
                    case 'LL':
                        this.createLLExample();
                        this.stepDescriptions = [
                            "初始状态：AVL树处于平衡状态。",
                            "插入节点5，树结构发生变化。",
                            "计算节点平衡因子：节点10的平衡因子为<span class='balance-factor'>+2</span>，发生LL型失衡。",
                            "执行LL旋转：以失衡节点10为旋转中心，向右单旋转。",
                            "调整指针：节点5的右子树变为节点10的左子树。",
                            "完成旋转：AVL树恢复平衡，所有节点平衡因子绝对值≤1。"
                        ];
                        break;
                    case 'RR':
                        this.createRRExample();
                        this.stepDescriptions = [
                            "初始状态：AVL树处于平衡状态。",
                            "插入节点25，树结构发生变化。",
                            "计算节点平衡因子：节点10的平衡因子为<span class='balance-factor'>-2</span>，发生RR型失衡。",
                            "执行RR旋转：以失衡节点10为旋转中心，向左单旋转。",
                            "调整指针：节点20的左子树变为节点10的右子树。",
                            "完成旋转：AVL树恢复平衡，所有节点平衡因子绝对值≤1。"
                        ];
                        break;
                    case 'LR':
                        this.createLRExample();
                        this.stepDescriptions = [
                            "初始状态：AVL树处于平衡状态。",
                            "插入节点15，树结构发生变化。",
                            "计算节点平衡因子：节点20的平衡因子为<span class='balance-factor'>+2</span>，但失衡发生在左子树的右子树，属于LR型失衡。",
                            "执行LR旋转：先对节点10进行RR旋转，使其变为LL型。",
                            "再对节点20进行LL旋转，调整整体结构。",
                            "完成旋转：AVL树恢复平衡，所有节点平衡因子绝对值≤1。"
                        ];
                        break;
                    case 'RL':
                        this.createRLExample();
                        this.stepDescriptions = [
                            "初始状态：AVL树处于平衡状态。",
                            "插入节点15，树结构发生变化。",
                            "计算节点平衡因子：节点10的平衡因子为<span class='balance-factor'>-2</span>，但失衡发生在右子树的左子树，属于RL型失衡。",
                            "执行RL旋转：先对节点20进行LL旋转，使其变为RR型。",
                            "再对节点10进行RR旋转，调整整体结构。",
                            "完成旋转：AVL树恢复平衡，所有节点平衡因子绝对值≤1。"
                        ];
                        break;
                }
                
                this.totalSteps = this.stepDescriptions.length;
                this.updateStepInfo();
                this.redraw();
            }
            
            // 创建LL示例树
            createLLExample() {
                // 初始平衡树
                const node10 = new TreeNode(10, canvas.width/2, 80);
                const node5 = new TreeNode(5, canvas.width/2 - 100, 150);
                const node20 = new TreeNode(20, canvas.width/2 + 100, 150);
                const node3 = new TreeNode(3, canvas.width/2 - 150, 220);
                const node7 = new TreeNode(7, canvas.width/2 - 50, 220);
                
                node10.left = node5;
                node10.right = node20;
                node5.left = node3;
                node5.right = node7;
                
                this.nodes = [node10, node5, node20, node3, node7];
                this.root = node10;
                
                // 设置初始高亮
                this.highlightedNodes = [node10];
            }
            
            // 创建RR示例树
            createRRExample() {
                const node10 = new TreeNode(10, canvas.width/2, 80);
                const node5 = new TreeNode(5, canvas.width/2 - 100, 150);
                const node20 = new TreeNode(20, canvas.width/2 + 100, 150);
                const node25 = new TreeNode(25, canvas.width/2 + 150, 220);
                
                node10.left = node5;
                node10.right = node20;
                node20.right = node25;
                
                this.nodes = [node10, node5, node20, node25];
                this.root = node10;
                
                // 设置初始高亮
                this.highlightedNodes = [node10];
            }
            
            // 创建LR示例树
            createLRExample() {
                const node20 = new TreeNode(20, canvas.width/2, 80);
                const node10 = new TreeNode(10, canvas.width/2 - 100, 150);
                const node25 = new TreeNode(25, canvas.width/2 + 100, 150);
                const node15 = new TreeNode(15, canvas.width/2 - 50, 220);
                
                node20.left = node10;
                node20.right = node25;
                node10.right = node15;
                
                this.nodes = [node20, node10, node25, node15];
                this.root = node20;
                
                // 设置初始高亮
                this.highlightedNodes = [node20];
            }
            
            // 创建RL示例树
            createRLExample() {
                const node10 = new TreeNode(10, canvas.width/2, 80);
                const node5 = new TreeNode(5, canvas.width/2 - 100, 150);
                const node20 = new TreeNode(20, canvas.width/2 + 100, 150);
                const node15 = new TreeNode(15, canvas.width/2 + 50, 220);
                
                node10.left = node5;
                node10.right = node20;
                node20.left = node15;
                
                this.nodes = [node10, node5, node20, node15];
                this.root = node10;
                
                // 设置初始高亮
                this.highlightedNodes = [node10];
            }
            
            // 更新步骤信息
            updateStepInfo() {
                stepInfoDiv.innerHTML = '';
                
                for (let i = 0; i < this.stepDescriptions.length; i++) {
                    const stepDiv = document.createElement('div');
                    stepDiv.className = 'step-info';
                    stepDiv.innerHTML = this.stepDescriptions[i];
                    
                    if (i === this.currentStep) {
                        stepDiv.classList.add('highlight');
                    }
                    
                    stepInfoDiv.appendChild(stepDiv);
                }
            }
            
            // 下一步
            nextStep() {
                if (this.currentStep < this.totalSteps - 1) {
                    this.currentStep++;
                    
                    // 根据当前步骤更新视觉效果
                    this.updateVisualForStep();
                    
                    this.updateStepInfo();
                }
            }
            
            // 上一步
            prevStep() {
                if (this.currentStep > 0) {
                    this.currentStep--;
                    
                    // 根据当前步骤更新视觉效果
                    this.updateVisualForStep();
                    
                    this.updateStepInfo();
                }
            }
            
            // 根据步骤更新视觉效果
            updateVisualForStep() {
                // 重置所有节点状态
                this.nodes.forEach(node => {
                    node.color = '#a0c4ff';
                    node.isImbalanced = false;
                    node.isFocused = false;
                });
                
                this.highlightedNodes = [];
                this.newEdges = [];
                this.oldEdges = [];
                
                // 根据示例和步骤设置特定视觉效果
                switch(this.currentExample) {
                    case 'LL':
                        this.updateVisualForLL();
                        break;
                    case 'RR':
                        this.updateVisualForRR();
                        break;
                    case 'LR':
                        this.updateVisualForLR();
                        break;
                    case 'RL':
                        this.updateVisualForRL();
                        break;
                }
            }
            
            // 更新LL示例的视觉效果
            updateVisualForLL() {
                const node10 = this.nodes.find(n => n.value === 10);
                const node5 = this.nodes.find(n => n.value === 5);
                
                if (!node10 || !node5) return;
                
                switch(this.currentStep) {
                    case 0: // 初始状态
                        this.highlightedNodes = [node10];
                        node10.isFocused = true;
                        break;
                    case 1: // 插入节点后
                        this.highlightedNodes = [node10, node5];
                        node10.isFocused = true;
                        break;
                    case 2: // 发现失衡
                        node10.isImbalanced = true;
                        this.highlightedNodes = [node10];
                        break;
                    case 3: // 执行旋转
                        node10.isImbalanced = true;
                        node5.isFocused = true;
                        this.highlightedNodes = [node10, node5];
                        this.newEdges = [{from: node5, to: node10, isRight: true}];
                        break;
                    case 4: // 调整指针
                        node5.isFocused = true;
                        this.highlightedNodes = [node5, node10];
                        this.newEdges = [{from: node5, to: node10, isRight: true}];
                        this.oldEdges = [{from: node10, to: node5, isLeft: true}];
                        break;
                    case 5: // 完成旋转
                        node5.isFocused = true;
                        this.highlightedNodes = [node5, node10];
                        break;
                }
            }
            
            // 更新RR示例的视觉效果
            updateVisualForRR() {
                const node10 = this.nodes.find(n => n.value === 10);
                const node20 = this.nodes.find(n => n.value === 20);
                
                if (!node10 || !node20) return;
                
                switch(this.currentStep) {
                    case 0: // 初始状态
                        this.highlightedNodes = [node10];
                        node10.isFocused = true;
                        break;
                    case 1: // 插入节点后
                        this.highlightedNodes = [node10, node20];
                        node10.isFocused = true;
                        break;
                    case 2: // 发现失衡
                        node10.isImbalanced = true;
                        this.highlightedNodes = [node10];
                        break;
                    case 3: // 执行旋转
                        node10.isImbalanced = true;
                        node20.isFocused = true;
                        this.highlightedNodes = [node10, node20];
                        this.newEdges = [{from: node20, to: node10, isLeft: true}];
                        break;
                    case 4: // 调整指针
                        node20.isFocused = true;
                        this.highlightedNodes = [node20, node10];
                        this.newEdges = [{from: node20, to: node10, isLeft: true}];
                        this.oldEdges = [{from: node10, to: node20, isRight: true}];
                        break;
                    case 5: // 完成旋转
                        node20.isFocused = true;
                        this.highlightedNodes = [node20, node10];
                        break;
                }
            }
            
            // 更新LR示例的视觉效果
            updateVisualForLR() {
                const node20 = this.nodes.find(n => n.value === 20);
                const node10 = this.nodes.find(n => n.value === 10);
                const node15 = this.nodes.find(n => n.value === 15);
                
                if (!node20 || !node10 || !node15) return;
                
                switch(this.currentStep) {
                    case 0: // 初始状态
                        this.highlightedNodes = [node20];
                        node20.isFocused = true;
                        break;
                    case 1: // 插入节点后
                        this.highlightedNodes = [node20, node10, node15];
                        node20.isFocused = true;
                        break;
                    case 2: // 发现失衡
                        node20.isImbalanced = true;
                        this.highlightedNodes = [node20, node10];
                        break;
                    case 3: // 第一步旋转
                        node10.isFocused = true;
                        node15.isFocused = true;
                        this.highlightedNodes = [node10, node15];
                        this.newEdges = [{from: node15, to: node10, isLeft: true}];
                        break;
                    case 4: // 第二步旋转
                        node15.isFocused = true;
                        node20.isImbalanced = true;
                        this.highlightedNodes = [node15, node20];
                        this.newEdges = [{from: node15, to: node20, isRight: true}];
                        break;
                    case 5: // 完成旋转
                        node15.isFocused = true;
                        this.highlightedNodes = [node15, node10, node20];
                        break;
                }
            }
            
            // 更新RL示例的视觉效果
            updateVisualForRL() {
                const node10 = this.nodes.find(n => n.value === 10);
                const node20 = this.nodes.find(n => n.value === 20);
                const node15 = this.nodes.find(n => n.value === 15);
                
                if (!node10 || !node20 || !node15) return;
                
                switch(this.currentStep) {
                    case 0: // 初始状态
                        this.highlightedNodes = [node10];
                        node10.isFocused = true;
                        break;
                    case 1: // 插入节点后
                        this.highlightedNodes = [node10, node20, node15];
                        node10.isFocused = true;
                        break;
                    case 2: // 发现失衡
                        node10.isImbalanced = true;
                        this.highlightedNodes = [node10, node20];
                        break;
                    case 3: // 第一步旋转
                        node20.isFocused = true;
                        node15.isFocused = true;
                        this.highlightedNodes = [node20, node15];
                        this.newEdges = [{from: node15, to: node20, isRight: true}];
                        break;
                    case 4: // 第二步旋转
                        node15.isFocused = true;
                        node10.isImbalanced = true;
                        this.highlightedNodes = [node15, node10];
                        this.newEdges = [{from: node15, to: node10, isLeft: true}];
                        break;
                    case 5: // 完成旋转
                        node15.isFocused = true;
                        this.highlightedNodes = [node15, node10, node20];
                        break;
                }
            }
            
            // 绘制树
            drawTree() {
                // 清空画布
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                
                // 绘制所有边
                this.drawEdges();
                
                // 绘制所有节点
                this.nodes.forEach(node => this.drawNode(node));
            }
            
            // 绘制边
            drawEdges() {
                // 绘制旧边（淡出效果）
                this.oldEdges.forEach(edge => {
                    ctx.beginPath();
                    ctx.moveTo(edge.from.x, edge.from.y);
                    ctx.lineTo(edge.to.x, edge.to.y);
                    ctx.strokeStyle = 'rgba(255, 100, 100, 0.5)';
                    ctx.lineWidth = 3;
                    ctx.stroke();
                });
                
                // 绘制普通边
                this.nodes.forEach(node => {
                    if (node.left) {
                        ctx.beginPath();
                        ctx.moveTo(node.x, node.y);
                        ctx.lineTo(node.left.x, node.left.y);
                        ctx.strokeStyle = '#666';
                        ctx.lineWidth = 2;
                        ctx.stroke();
                    }
                    
                    if (node.right) {
                        ctx.beginPath();
                        ctx.moveTo(node.x, node.y);
                        ctx.lineTo(node.right.x, node.right.y);
                        ctx.strokeStyle = '#666';
                        ctx.lineWidth = 2;
                        ctx.stroke();
                    }
                });
                
                // 绘制新边（高亮）
                this.newEdges.forEach(edge => {
                    ctx.beginPath();
                    ctx.moveTo(edge.from.x, edge.from.y);
                    ctx.lineTo(edge.to.x, edge.to.y);
                    ctx.strokeStyle = '#4caf50';
                    ctx.lineWidth = 3;
                    ctx.stroke();
                    
                    // 绘制箭头
                    this.drawArrow(edge.from.x, edge.from.y, edge.to.x, edge.to.y, '#4caf50');
                });
            }
            
            // 绘制箭头
            drawArrow(fromX, fromY, toX, toY, color) {
                const headlen = 10;
                const dx = toX - fromX;
                const dy = toY - fromY;
                const angle = Math.atan2(dy, dx);
                
                ctx.save();
                ctx.strokeStyle = color;
                ctx.fillStyle = color;
                
                // 绘制箭头线
                ctx.beginPath();
                ctx.moveTo(fromX, fromY);
                ctx.lineTo(toX, toY);
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 绘制箭头头部
                ctx.beginPath();
                ctx.moveTo(toX, toY);
                ctx.lineTo(toX - headlen * Math.cos(angle - Math.PI/6), toY - headlen * Math.sin(angle - Math.PI/6));
                ctx.lineTo(toX - headlen * Math.cos(angle + Math.PI/6), toY - headlen * Math.sin(angle + Math.PI/6));
                ctx.closePath();
                ctx.fill();
                
                ctx.restore();
            }
            
            // 绘制节点
            drawNode(node) {
                // 确定节点颜色
                let color = node.color;
                if (node.isImbalanced) {
                    color = '#ff9a76';
                } else if (node.isFocused) {
                    color = '#90ee90';
                }
                
                // 绘制节点外圈
                ctx.beginPath();
                ctx.arc(node.x, node.y, 25, 0, Math.PI * 2);
                ctx.fillStyle = color;
                ctx.fill();
                ctx.strokeStyle = '#fff';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 绘制节点值
                ctx.fillStyle = '#000';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(node.value, node.x, node.y);
                
                // 绘制平衡因子
                ctx.fillStyle = '#fff';
                ctx.font = '12px Arial';
                const bf = node.getBalanceFactor();
                ctx.fillText(`BF:${bf}`, node.x, node.y + 35);
                
                // 如果是高亮节点，添加发光效果
                if (this.highlightedNodes.includes(node)) {
                    ctx.beginPath();
                    ctx.arc(node.x, node.y, 30, 0, Math.PI * 2);
                    ctx.strokeStyle = 'rgba(255, 255, 255, 0.7)';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
            }
            
            // 重绘
            redraw() {
                this.drawTree();
            }
            
            // 动画循环
            animate() {
                // 平滑移动节点到目标位置
                this.nodes.forEach(node => {
                    const dx = node.targetX - node.x;
                    const dy = node.targetY - node.y;
                    
                    if (Math.abs(dx) > 0.5 || Math.abs(dy) > 0.5) {
                        node.x += dx * 0.1;
                        node.y += dy * 0.1;
                    }
                });
                
                this.drawTree();
                this.animationFrameId = requestAnimationFrame(() => this.animate());
            }
            
            // 切换模式
            toggleMode() {
                this.currentMode = this.currentMode === 'teach' ? 'experiment' : 'teach';
                
                // 更新UI
                const modeToggleBtn = document.getElementById('modeToggle');
                const modeBtns = document.querySelectorAll('.mode-btn');
                
                if (this.currentMode === 'experiment') {
                    modeToggleBtn.textContent = '切换到教学模式';
                    modeBtns[0].classList.remove('active');
                    modeBtns[1].classList.add('active');
                    
                    // 切换到实验模式
                    this.switchToExperimentMode();
                } else {
                    modeToggleBtn.textContent = '切换到实验模式';
                    modeBtns[0].classList.add('active');
                    modeBtns[1].classList.remove('active');
                    
                    // 切换回教学模式
                    this.switchToTeachMode();
                }
            }
            
            // 切换到实验模式
            switchToExperimentMode() {
                // 创建实验模式的树
                this.nodes = [];
                this.root = null;
                this.currentStep = 0;
                this.totalSteps = 0;
                this.stepDescriptions = ["实验模式：可以自由插入节点，观察AVL树的自平衡过程。"];
                this.updateStepInfo();
                
                // 初始化一个简单的树
                const node20 = new TreeNode(20, canvas.width/2, 80);
                this.nodes.push(node20);
                this.root = node20;
                
                this.redraw();
            }
            
            // 切换到教学模式
            switchToTeachMode() {
                // 重新加载当前示例
                this.loadExample(this.currentExample);
            }
            
            // 插入节点（实验模式）
            insertNode(value) {
                if (this.currentMode !== 'experiment') return;
                
                // 创建新节点
                const newNode = new TreeNode(value, 0, 0);
                
                // 简单的插入逻辑（这里简化了，实际AVL树插入需要递归和平衡）
                // 这只是为了演示
                if (!this.root) {
                    newNode.x = canvas.width/2;
                    newNode.y = 80;
                    newNode.targetX = newNode.x;
                    newNode.targetY = newNode.y;
                    this.root = newNode;
                    this.nodes.push(newNode);
                } else {
                    // 简单查找插入位置
                    let current = this.root;
                    let parent = null;
                    let isLeft = false;
                    
                    while (current) {
                        parent = current;
                        if (value < current.value) {
                            current = current.left;
                            isLeft = true;
                        } else {
                            current = current.right;
                            isLeft = false;
                        }
                    }
                    
                    // 设置新节点位置
                    if (parent) {
                        newNode.x = parent.x + (isLeft ? -100 : 100);
                        newNode.y = parent.y + 70;
                        newNode.targetX = newNode.x;
                        newNode.targetY = newNode.y;
                        
                        if (isLeft) {
                            parent.left = newNode;
                        } else {
                            parent.right = newNode;
                        }
                        
                        this.nodes.push(newNode);
                    }
                }
                
                // 简单模拟平衡过程
                this.simulateBalance();
                
                this.redraw();
            }
            
            // 模拟平衡过程（简化版）
            simulateBalance() {
                // 这里只是简单演示，实际AVL树平衡需要完整实现
                // 我们只是随机选择一个节点进行"旋转"演示
                if (this.nodes.length > 3) {
                    const randomNode = this.nodes[Math.floor(Math.random() * this.nodes.length)];
                    randomNode.isImbalanced = true;
                    randomNode.isFocused = true;
                    this.highlightedNodes = [randomNode];
                    
                    // 3秒后恢复正常
                    setTimeout(() => {
                        randomNode.isImbalanced = false;
                        randomNode.isFocused = false;
                        this.highlightedNodes = [];
                        this.redraw();
                    }, 3000);
                }
            }
        }

        // 初始化应用
        document.addEventListener('DOMContentLoaded', () => {
            // 创建AVL树动画实例
            const avlAnimation = new AVLTreeAnimation();
            
            // 绑定按钮事件
            document.getElementById('prevBtn').addEventListener('click', () => {
                avlAnimation.prevStep();
            });
            
            document.getElementById('nextBtn').addEventListener('click', () => {
                avlAnimation.nextStep();
            });
            
            document.getElementById('playPauseBtn').addEventListener('click', function() {
                if (avlAnimation.isPlaying) {
                    avlAnimation.isPlaying = false;
                    this.textContent = '播放';
                } else {
                    avlAnimation.isPlaying = true;
                    this.textContent = '暂停';
                    
                    // 简单自动播放
                    const playInterval = setInterval(() => {
                        if (avlAnimation.is
<!--检测到代码截断，自动续写中...-->
isPlaying && avlAnimation.currentStep < avlAnimation.totalSteps - 1) {
                        avlAnimation.nextStep();
                    } else {
                        avlAnimation.isPlaying = false;
                        this.textContent = '播放';
                        clearInterval(playInterval);
                    }
                }, 1500 / avlAnimation.animationSpeed);
            });
            
            document.getElementById('resetBtn').addEventListener('click', () => {
                avlAnimation.loadExample(avlAnimation.currentExample);
            });
            
            document.getElementById('modeToggle').addEventListener('click', () => {
                avlAnimation.toggleMode();
            });
            
            // 示例选择按钮
            document.querySelectorAll('.example-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    // 更新按钮状态
                    document.querySelectorAll('.example-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    // 加载示例
                    const type = this.getAttribute('data-type');
                    avlAnimation.loadExample(type);
                });
            });
            
            // 模式选择按钮
            document.querySelectorAll('.mode-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    if (this.classList.contains('active')) return;
                    
                    // 更新按钮状态
                    document.querySelectorAll('.mode-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    // 切换模式
                    const mode = this.getAttribute('data-mode');
                    avlAnimation.currentMode = mode;
                    
                    const modeToggleBtn = document.getElementById('modeToggle');
                    if (mode === 'experiment') {
                        modeToggleBtn.textContent = '切换到教学模式';
                        avlAnimation.switchToExperimentMode();
                    } else {
                        modeToggleBtn.textContent = '切换到实验模式';
                        avlAnimation.switchToTeachMode();
                    }
                });
            });
            
            // 速度滑块
            const speedSlider = document.getElementById('speedSlider');
            const speedValue = document.getElementById('speedValue');
            
            speedSlider.addEventListener('input', function() {
                avlAnimation.animationSpeed = parseInt(this.value);
                
                // 更新显示文本
                if (this.value <= 3) {
                    speedValue.textContent = '慢速';
                } else if (this.value <= 7) {
                    speedValue.textContent = '中速';
                } else {
                    speedValue.textContent = '快速';
                }
            });
            
            // 实验模式下的插入按钮（简化演示）
            const experimentControls = document.createElement('div');
            experimentControls.id = 'experimentControls';
            experimentControls.style.cssText = `
                display: none;
                margin-top: 15px;
                padding: 15px;
                background-color: #404040;
                border-radius: 8px;
            `;
            
            experimentControls.innerHTML = `
                <h4>实验控制</h4>
                <div style="display: flex; gap: 10px; margin-top: 10px;">
                    <input type="number" id="nodeValueInput" placeholder="节点值" min="1" max="99" style="flex: 1; padding: 8px; border-radius: 4px; border: 1px solid #555; background-color: #333; color: white;">
                    <button id="insertBtn" style="padding: 8px 15px; background-color: #4caf50; color: white; border: none; border-radius: 4px; cursor: pointer;">插入节点</button>
                    <button id="clearBtn" style="padding: 8px 15px; background-color: #f44336; color: white; border: none; border-radius: 4px; cursor: pointer;">清空树</button>
                </div>
                <p style="margin-top: 10px; font-size: 0.9rem; color: #aaa;">在实验模式下，可以插入节点观察AVL树的自平衡过程（简化演示）。</p>
            `;
            
            document.querySelector('.control-panel').appendChild(experimentControls);
            
            // 实验模式控制按钮
            document.getElementById('insertBtn').addEventListener('click', () => {
                const input = document.getElementById('nodeValueInput');
                const value = parseInt(input.value);
                
                if (!isNaN(value) && value >= 1 && value <= 99) {
                    avlAnimation.insertNode(value);
                    input.value = '';
                } else {
                    alert('请输入1-99之间的有效数字');
                }
            });
            
            document.getElementById('clearBtn').addEventListener('click', () => {
                avlAnimation.switchToExperimentMode();
            });
            
            // 监听模式切换，显示/隐藏实验控制
            const originalToggleMode = avlAnimation.toggleMode.bind(avlAnimation);
            avlAnimation.toggleMode = function() {
                originalToggleMode();
                if (this.currentMode === 'experiment') {
                    experimentControls.style.display = 'block';
                } else {
                    experimentControls.style.display = 'none';
                }
            };
            
            // 初始隐藏实验控制
            experimentControls.style.display = 'none';
            
            // 添加键盘快捷键
            document.addEventListener('keydown', (e) => {
                // 左右箭头控制步骤
                if (e.key === 'ArrowLeft') {
                    avlAnimation.prevStep();
                } else if (e.key === 'ArrowRight') {
                    avlAnimation.nextStep();
                }
                // 空格键播放/暂停
                else if (e.key === ' ') {
                    e.preventDefault();
                    document.getElementById('playPauseBtn').click();
                }
            });
            
            // 初始绘制
            avlAnimation.redraw();
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## AVL树旋转动画交互式教学动画使用指南

欢迎使用AVL树旋转动画教学工具！本指南将帮助您充分利用这个交互式动画，深入理解AVL树的四种旋转操作（LL、RR、LR、RL）。

### 一、功能说明

本动画工具是一个基于HTML5 Canvas开发的交互式教学平台，旨在通过可视化方式帮助您：
1. **直观理解**AVL树的自平衡机制
2. **分步掌握**四种旋转操作的具体过程
3. **对比学习**不同旋转类型的异同点
4. **实践验证**通过实验模式加深理解

### 二、主要功能

#### 1. 教学模式（默认）
- **四种旋转示例**：通过下拉菜单选择LL、RR、LR、RL四种旋转类型
- **分步演示**：每个示例分为6个逻辑步骤，从失衡检测到完成旋转
- **视觉编码**：
  - 🔵 浅蓝色：平衡节点
  - 🟠 橙色：失衡节点
  - 🟢 亮绿色：当前焦点节点
  - 🟢 绿色连线：新建立的指针
  - 🔴 红色连线（半透明）：待移除的指针
- **平衡因子显示**：每个节点下方显示平衡因子（BF）

#### 2. 实验模式
- **自由插入**：在1-99范围内插入任意节点值
- **简化平衡模拟**：插入后自动演示平衡过程
- **清空功能**：重置实验环境

#### 3. 控制功能
- **流程控制**：上一步/下一步按钮
- **自动播放**：播放/暂停按钮
- **速度调节**：慢速/中速/快速三档
- **重置功能**：回到当前示例初始状态

### 三、设计特色

#### 1. 认知友好的视觉设计
- **渐进式揭示**：复杂操作分解为简单步骤
- **焦点引导**：通过颜色和发光效果引导注意力
- **状态反馈**：实时显示当前步骤说明

#### 2. 符合学习规律的教学流程
```
观察失衡 → 识别类型 → 执行旋转 → 验证结果
```

#### 3. 双重学习模式
- **结构化学习**（教学模式）：系统学习四种标准案例
- **探索式学习**（实验模式）：自主构建案例，观察规律

### 四、教学要点

#### 1. LL型旋转（右单旋）
- **触发条件**：左子树的左子树导致失衡（BF=+2）
- **关键观察**：
  - 失衡节点：橙色高亮
  - 旋转中心：左子节点成为新根
  - 指针调整：原根的左指针指向旋转节点的右子树

#### 2. RR型旋转（左单旋）
- **触发条件**：右子树的右子树导致失衡（BF=-2）
- **与LL的对称性**：操作镜像对称，原理相同

#### 3. LR型旋转（先左后右双旋）
- **复合操作**：先对左子树RR旋转，再对根LL旋转
- **关键识别**：失衡发生在左子树的右子树
- **两步演示**：清晰展示中间状态

#### 4. RL型旋转（先右后左双旋）
- **复合操作**：先对右子树LL旋转，再对根RR旋转
- **与LR的对称性**：理解这种对称性能帮助记忆

### 五、使用建议

#### 1. 初学者学习路径
```
第1步：选择LL示例 → 完整观看一遍动画
第2步：使用"上一步/下一步"分步学习
第3步：重点关注平衡因子的变化
第4步：切换到RR示例，对比学习
第5步：学习LR和RL复合旋转
第6步：进入实验模式尝试构建自己的案例
```

#### 2. 键盘快捷键（提升效率）
- **← 左箭头**：上一步
- **→ 右箭头**：下一步
- **空格键**：播放/暂停

#### 3. 教学场景使用建议
- **课堂演示**：使用投影仪，选择"中速"播放
- **小组学习**：让学生轮流操作控制按钮
- **课后复习**：学生自主选择薄弱环节重点练习
- **翻转课堂**：课前观看动画，课堂讨论原理

#### 4. 深度学习提示
1. **预测练习**：在点击"下一步"前，尝试预测下一步会发生什么
2. **原理关联**：将动画步骤与教材中的伪代码对应起来
3. **模式识别**：总结四种旋转的"失衡模式-操作模式"对应关系
4. **边界思考**：在实验模式中尝试极端情况（如连续插入递增序列）

#### 5. 故障排除
- **动画卡顿**：降低播放速度或刷新页面
- **显示异常**：检查浏览器是否支持HTML5 Canvas
- **功能失效**：确保使用现代浏览器（Chrome/Firefox/Edge最新版）

### 六、教育价值

本工具不仅展示AVL树旋转的"结果"，更重要的是揭示"过程"：
1. **降低认知负荷**：将抽象的指针操作转化为直观的视觉变化
2. **强化概念理解**：平衡因子从计算数字变为驱动动画的信号
3. **培养计算思维**：通过分解、模式识别理解复杂算法
4. **支持差异化学习**：不同学习风格的学生都能找到适合自己的方式

---

**开始您的AVL树学习之旅吧！** 建议从LL旋转开始，逐步探索其他类型。记住：理解比记忆更重要，可视化工具是帮助您建立深刻理解的桥梁，而不是替代思考的工具。

祝您学习愉快，学有所获！

*教学工具设计：熊猫老师*
*如有反馈建议，欢迎提出改进意见*