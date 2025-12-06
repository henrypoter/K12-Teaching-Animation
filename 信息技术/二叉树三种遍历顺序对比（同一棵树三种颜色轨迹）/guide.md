# 需求：二叉树三种遍历顺序对比（同一棵树三种颜色轨迹）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为学习数据结构与算法的初学者（如计算机专业大学生、编程自学者）。他们已了解二叉树的基本结构，但难以直观理解三种遍历（先序、中序、后序）的递归过程与差异。
2.  **核心痛点**：
    *   **抽象性**：遍历的递归逻辑抽象，仅凭静态图示或代码难以形成动态过程思维。
    *   **对比性**：难以在同一棵树上清晰、同步地对比三种遍历顺序的路径差异。
    *   **过程性**：需要可视化“访问节点”的时机（何时输出值），而不仅仅是最终序列。
3.  **学习目标**：通过动画，用户应能：
    *   清晰识别并描述先序、中序、后序遍历每一步的访问顺序和移动路径。
    *   直观对比三种遍历在访问节点时机上的核心区别。
    *   将动态的遍历路径与最终的节点序列输出建立牢固联系。

#### 教学设计思路
1.  **核心概念**：聚焦于 **“访问节点的时机”** 。将遍历过程解构为：**“沿着特定路径移动”** 和 **“在特定位置访问（点亮/记录）当前节点”** 两个动作。
2.  **认知规律**：
    *   **从具体到抽象**：使用一棵具体、结构清晰的二叉树（例如包含7个节点，结构完整）。
    *   **分解与同步**：将复杂的递归分解为单步可视化过程。让三种遍历**同步开始**，通过并行动画突出差异。
    *   **多通道编码**：结合**颜色**（区分遍历类型）、**运动轨迹**（显示访问路径）、**高亮**（显示当前访问节点）和**文本输出**（实时显示遍历结果），强化记忆。
3.  **交互设计**：
    *   **控制核心**：提供“播放/暂停”、“下一步/上一步”、“重置”控件。允许用户自主控制节奏，支持反复观察难点。
    *   **焦点引导**：在单步执行时，通过轻微放大或脉动效果强调当前被访问的节点。
    *   **层次揭示**：初始时只显示树结构。动画开始后，再动态绘制出三种颜色的遍历轨迹，避免初始信息过载。
4.  **视觉呈现**：
    *   **结构清晰**：树形布局美观、对称，节点间距适中，连线清晰。
    *   **轨迹设计**：三种遍历路径以三种不同颜色的**光滑曲线**（或带有方向箭头的线条）表示，从根节点开始，依次经过每个节点。轨迹在节点处应有一个明显的“停留点”（代表访问动作）。
    *   **状态反馈**：节点被某次遍历访问时，其边框和填充色变为对应轨迹的高亮色，并可能显示一个序号。访问后恢复为中性色，但留下一个小的颜色标记（如一个色点）以示“已访问”。

#### 配色方案选择
选择对比鲜明、易于区分且符合认知习惯的颜色来区分三种遍历，同时确保整体界面清爽、专注。

*   **遍历轨迹与高亮色**：
    *   **先序遍历（Pre-order）**：**红色** (#FF5252)。红色具有“开始”、“优先”的心理暗示，契合先序“根-左-右”中首先访问根节点的特性。
    *   **中序遍历（In-order）**：**蓝色** (#448AFF)。蓝色沉稳、居中，契合中序“左-根-右”的中间访问特性。
    *   **后序遍历（Post-order）**：**绿色** (#4CAF50)。绿色常代表“完成”、“最后”，契合后序“左-右-根”的最后访问根节点的特性。
*   **界面基础色**：
    *   **画布背景**：浅灰色 (#f8f9fa) 或白色。
    *   **二叉树节点**：未访问时为浅灰色边框 (#ddd) 和白色填充。节点文字为深灰色 (#333)。
    *   **节点连接线**：深灰色 (#666)。
    *   **控制面板**：中性浅色背景。

#### 交互功能列表
1.  **动画控制区**：
    *   **播放/暂停按钮**：开始或暂停连续的自动动画演示。
    *   **下一步按钮**：手动单步执行下一步（三种遍历同时前进一步）。
    *   **上一步按钮**：手动回退到上一步。
    *   **重置按钮**：将动画恢复至初始状态。
    *   **速度调节滑块**：控制自动播放的速度。
2.  **可视化主体区**：
    *   **静态二叉树**：清晰显示节点（可标有字母或数字）和连线。
    *   **动态颜色轨迹**：
        *   三条彩色线条（红、蓝、绿）分别从根节点开始生长，描绘遍历路径。
        *   线条在节点处绘制一个“圆点”或“停留标记”表示访问。
    *   **节点状态反馈**：
        *   当被遍历访问时，节点高亮为对应颜色。
        *   高亮后，节点旁或内部留下一个该颜色的小标记，表示已被该顺序访问。
3.  **信息输出区**：
    *   **三个遍历结果序列显示框**：分别以红、蓝、绿为标题色，实时显示当前已访问的节点序列，清晰展示三种遍历的输出差异。
    *   **当前步骤说明**：简短的文字说明当前步骤（例如：“先序：访问节点A”、“中序：移动到左子树B”）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>二叉树三种遍历顺序对比动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eaeaea;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.1em;
        }

        .legend {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .legend-item {
            display: flex;
            align-items: center;
            font-weight: 500;
        }

        .color-box {
            width: 20px;
            height: 20px;
            margin-right: 8px;
            border-radius: 3px;
        }

        .preorder-color {
            background-color: #FF5252;
        }

        .inorder-color {
            background-color: #448AFF;
        }

        .postorder-color {
            background-color: #4CAF50;
        }

        .container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        @media (min-width: 992px) {
            .container {
                flex-direction: row;
            }
            
            .visualization-section {
                flex: 2;
            }
            
            .control-section {
                flex: 1;
            }
        }

        .visualization-section {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .tree-container {
            position: relative;
            height: 500px;
            margin: 20px 0;
            overflow: hidden;
            border-radius: 8px;
            background-color: #fefefe;
            border: 1px solid #eee;
        }

        #treeCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }

        .control-section {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .control-panel {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .control-title {
            font-size: 1.2em;
            color: #2c3e50;
            margin-bottom: 5px;
            padding-bottom: 8px;
            border-bottom: 1px dashed #eee;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 10px;
        }

        button {
            padding: 10px 16px;
            border: none;
            border-radius: 6px;
            background-color: #3498db;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            flex: 1;
            min-width: 120px;
        }

        button:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        button:active {
            transform: translateY(0);
        }

        button:disabled {
            background-color: #bdc3c7;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        #playPauseBtn {
            background-color: #2ecc71;
        }

        #playPauseBtn:hover:not(:disabled) {
            background-color: #27ae60;
        }

        #resetBtn {
            background-color: #e74c3c;
        }

        #resetBtn:hover:not(:disabled) {
            background-color: #c0392b;
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-top: 10px;
        }

        .speed-control label {
            font-weight: 500;
            color: #555;
        }

        #speedSlider {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            appearance: none;
            background: #ddd;
            border-radius: 4px;
            outline: none;
        }

        #speedSlider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
        }

        #speedSlider::-moz-range-thumb {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
            border: none;
        }

        .output-panel {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .output-box {
            border-radius: 8px;
            padding: 15px;
            background-color: #f8f9fa;
            border-left: 5px solid;
        }

        .output-title {
            font-weight: 700;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }

        .output-title .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            margin-right: 10px;
        }

        .preorder-output {
            border-left-color: #FF5252;
        }

        .preorder-output .output-title {
            color: #FF5252;
        }

        .preorder-output .dot {
            background-color: #FF5252;
        }

        .inorder-output {
            border-left-color: #448AFF;
        }

        .inorder-output .output-title {
            color: #448AFF;
        }

        .inorder-output .dot {
            background-color: #448AFF;
        }

        .postorder-output {
            border-left-color: #4CAF50;
        }

        .postorder-output .output-title {
            color: #4CAF50;
        }

        .postorder-output .dot {
            background-color: #4CAF50;
        }

        .sequence {
            font-size: 1.3em;
            font-weight: 600;
            letter-spacing: 2px;
            min-height: 1.5em;
            color: #2c3e50;
        }

        .current-step {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            margin-top: 10px;
            border-left: 5px solid #f1c40f;
        }

        .current-step-title {
            font-weight: 700;
            color: #f39c12;
            margin-bottom: 8px;
        }

        #stepDescription {
            font-size: 1.1em;
            min-height: 1.5em;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            color: #7f8c8d;
            font-size: 0.9em;
            padding-top: 15px;
            border-top: 1px solid #eaeaea;
        }

        .instructions {
            background-color: #e8f4fc;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 20px;
            border-left: 5px solid #3498db;
        }

        .instructions h3 {
            color: #3498db;
            margin-bottom: 10px;
        }

        .instructions ul {
            padding-left: 20px;
        }

        .instructions li {
            margin-bottom: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>二叉树三种遍历顺序对比</h1>
        <p class="subtitle">同一棵树上的先序、中序、后序遍历轨迹可视化</p>
        
        <div class="legend">
            <div class="legend-item">
                <div class="color-box preorder-color"></div>
                <span>先序遍历 (Pre-order)</span>
            </div>
            <div class="legend-item">
                <div class="color-box inorder-color"></div>
                <span>中序遍历 (In-order)</span>
            </div>
            <div class="legend-item">
                <div class="color-box postorder-color"></div>
                <span>后序遍历 (Post-order)</span>
            </div>
        </div>
    </header>

    <div class="instructions">
        <h3>使用说明</h3>
        <ul>
            <li>动画将同步展示三种遍历算法在同一棵二叉树上的执行过程。</li>
            <li>每种遍历使用不同颜色的轨迹表示，节点被访问时会高亮显示对应颜色。</li>
            <li>使用下方控制面板控制动画播放，观察三种遍历访问节点的时机差异。</li>
            <li>右侧实时显示三种遍历已访问的节点序列。</li>
        </ul>
    </div>

    <div class="container">
        <section class="visualization-section">
            <h2>遍历过程可视化</h2>
            <div class="tree-container">
                <canvas id="treeCanvas"></canvas>
            </div>
            
            <div class="current-step">
                <div class="current-step-title">当前步骤说明</div>
                <div id="stepDescription">点击"播放"按钮开始动画</div>
            </div>
        </section>
        
        <section class="control-section">
            <div class="control-panel">
                <h3 class="control-title">动画控制</h3>
                <div class="button-group">
                    <button id="playPauseBtn">播放</button>
                    <button id="nextStepBtn">下一步</button>
                    <button id="prevStepBtn">上一步</button>
                    <button id="resetBtn">重置</button>
                </div>
                
                <div class="speed-control">
                    <label for="speedSlider">播放速度:</label>
                    <input type="range" id="speedSlider" min="1" max="10" value="5">
                </div>
            </div>
            
            <div class="output-panel">
                <h3 class="control-title">遍历结果序列</h3>
                
                <div class="output-box preorder-output">
                    <div class="output-title">
                        <div class="dot"></div>
                        <span>先序遍历 (根-左-右)</span>
                    </div>
                    <div id="preorderSequence" class="sequence">-</div>
                </div>
                
                <div class="output-box inorder-output">
                    <div class="output-title">
                        <div class="dot"></div>
                        <span>中序遍历 (左-根-右)</span>
                    </div>
                    <div id="inorderSequence" class="sequence">-</div>
                </div>
                
                <div class="output-box postorder-output">
                    <div class="output-title">
                        <div class="dot"></div>
                        <span>后序遍历 (左-右-根)</span>
                    </div>
                    <div id="postorderSequence" class="sequence">-</div>
                </div>
            </div>
        </section>
    </div>
    
    <footer>
        <p>教学动画设计 | 二叉树遍历可视化 | 使用HTML5 Canvas实现</p>
    </footer>

    <script>
        // 二叉树节点定义
        class TreeNode {
            constructor(value, x, y) {
                this.value = value;
                this.x = x;
                this.y = y;
                this.left = null;
                this.right = null;
                this.radius = 25;
                
                // 访问状态标记
                this.visitedPreorder = false;
                this.visitedInorder = false;
                this.visitedPostorder = false;
                
                // 当前高亮状态
                this.highlighted = false;
                this.highlightColor = null;
            }
            
            draw(ctx) {
                // 绘制节点连接线（先画线，后画节点）
                if (this.left) {
                    ctx.beginPath();
                    ctx.moveTo(this.x, this.y);
                    ctx.lineTo(this.left.x, this.left.y);
                    ctx.strokeStyle = '#666';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
                
                if (this.right) {
                    ctx.beginPath();
                    ctx.moveTo(this.x, this.y);
                    ctx.lineTo(this.right.x, this.right.y);
                    ctx.strokeStyle = '#666';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
                
                // 绘制节点
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                
                // 节点填充色
                if (this.highlighted && this.highlightColor) {
                    ctx.fillStyle = this.highlightColor;
                } else {
                    ctx.fillStyle = 'white';
                }
                
                ctx.fill();
                
                // 节点边框
                ctx.lineWidth = 3;
                if (this.highlighted && this.highlightColor) {
                    ctx.strokeStyle = this.highlightColor;
                } else {
                    ctx.strokeStyle = '#ddd';
                }
                ctx.stroke();
                
                // 绘制访问标记点
                const markRadius = 6;
                let markCount = 0;
                
                if (this.visitedPreorder) {
                    ctx.beginPath();
                    ctx.arc(this.x - this.radius/2, this.y - this.radius/2, markRadius, 0, Math.PI * 2);
                    ctx.fillStyle = '#FF5252';
                    ctx.fill();
                    markCount++;
                }
                
                if (this.visitedInorder) {
                    ctx.beginPath();
                    ctx.arc(this.x + this.radius/2, this.y - this.radius/2, markRadius, 0, Math.PI * 2);
                    ctx.fillStyle = '#448AFF';
                    ctx.fill();
                    markCount++;
                }
                
                if (this.visitedPostorder) {
                    ctx.beginPath();
                    ctx.arc(this.x, this.y + this.radius/2, markRadius, 0, Math.PI * 2);
                    ctx.fillStyle = '#4CAF50';
                    ctx.fill();
                    markCount++;
                }
                
                // 绘制节点值
                ctx.fillStyle = this.highlighted ? 'white' : '#333';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(this.value, this.x, this.y);
            }
        }

        // 遍历动画管理器
        class TraversalAnimation {
            constructor(canvasId) {
                this.canvas = document.getElementById(canvasId);
                this.ctx = this.canvas.getContext('2d');
                this.tree = null;
                this.animationId = null;
                
                // 遍历状态
                this.preorderSteps = [];
                this.inorderSteps = [];
                this.postorderSteps = [];
                
                this.currentStepIndex = 0;
                this.isPlaying = false;
                this.speed = 5; // 1-10，值越大速度越快
                
                // 轨迹点存储
                this.preorderPath = [];
                this.inorderPath = [];
                this.postorderPath = [];
                
                // 初始化树
                this.initTree();
                
                // 生成遍历步骤
                this.generateTraversalSteps();
                
                // 调整画布大小
                this.resizeCanvas();
                window.addEventListener('resize', () => this.resizeCanvas());
                
                // 绘制初始树
                this.draw();
            }
            
            resizeCanvas() {
                const container = this.canvas.parentElement;
                this.canvas.width = container.clientWidth;
                this.canvas.height = container.clientHeight;
                this.draw();
            }
            
            initTree() {
                // 创建一棵示例二叉树 (A为根节点)
                const width = this.canvas.width;
                const height = this.canvas.height;
                
                // 节点位置计算
                const rootX = width / 2;
                const rootY = 80;
                const levelHeight = 100;
                const levelWidth = width / 4;
                
                // 创建节点
                const nodeA = new TreeNode('A', rootX, rootY);
                const nodeB = new TreeNode('B', rootX - levelWidth, rootY + levelHeight);
                const nodeC = new TreeNode('C', rootX + levelWidth, rootY + levelHeight);
                const nodeD = new TreeNode('D', rootX - levelWidth - levelWidth/2, rootY + levelHeight*2);
                const nodeE = new TreeNode('E', rootX - levelWidth + levelWidth/2, rootY + levelHeight*2);
                const nodeF = new TreeNode('F', rootX + levelWidth - levelWidth/2, rootY + levelHeight*2);
                const nodeG = new TreeNode('G', rootX + levelWidth + levelWidth/2, rootY + levelHeight*2);
                
                // 构建树结构
                nodeA.left = nodeB;
                nodeA.right = nodeC;
                nodeB.left = nodeD;
                nodeB.right = nodeE;
                nodeC.left = nodeF;
                nodeC.right = nodeG;
                
                this.tree = nodeA;
            }
            
            // 生成遍历步骤
            generateTraversalSteps() {
                // 先序遍历步骤生成
                const preorder = (node) => {
                    if (!node) return;
                    
                    this.preorderSteps.push({
                        type: 'visit',
                        traversal: 'preorder',
                        node: node,
                        description: `先序：访问节点 ${node.value}`
                    });
                    
                    this.preorderSteps.push({
                        type: 'move',
                        traversal: 'preorder',
                        from: node,
                        to: node.left,
                        description: `先序：移动到 ${node.left ? node.left.value : '空'} 的左子树`
                    });
                    
                    preorder(node.left);
                    
                    this.preorderSteps.push({
                        type: 'move',
                        traversal: 'preorder',
                        from: node,
                        to: node.right,
                        description: `先序：移动到 ${node.right ? node.right.value : '空'} 的右子树`
                    });
                    
                    preorder(node.right);
                };
                
                // 中序遍历步骤生成
                const inorder = (node) => {
                    if (!node) return;
                    
                    this.inorderSteps.push({
                        type: 'move',
                        traversal: 'inorder',
                        from: node,
                        to: node.left,
                        description: `中序：移动到 ${node.left ? node.left.value : '空'} 的左子树`
                    });
                    
                    inorder(node.left);
                    
                    this.inorderSteps.push({
                        type: 'visit',
                        traversal: 'inorder',
                        node: node,
                        description: `中序：访问节点 ${node.value}`
                    });
                    
                    this.inorderSteps.push({
                        type: 'move',
                        traversal: 'inorder',
                        from: node,
                        to: node.right,
                        description: `中序：移动到 ${node.right ? node.right.value : '空'} 的右子树`
                    });
                    
                    inorder(node.right);
                };
                
                // 后序遍历步骤生成
                const postorder = (node) => {
                    if (!node) return;
                    
                    this.postorderSteps.push({
                        type: 'move',
                        traversal: 'postorder',
                        from: node,
                        to: node.left,
                        description: `后序：移动到 ${node.left ? node.left.value : '空'} 的左子树`
                    });
                    
                    postorder(node.left);
                    
                    this.postorderSteps.push({
                        type: 'move',
                        traversal: 'postorder',
                        from: node,
                        to: node.right,
                        description: `后序：移动到 ${node.right ? node.right.value : '空'} 的右子树`
                    });
                    
                    postorder(node.right);
                    
                    this.postorderSteps.push({
                        type: 'visit',
                        traversal: 'postorder',
                        node: node,
                        description: `后序：访问节点 ${node.value}`
                    });
                };
                
                // 生成步骤
                preorder(this.tree);
                inorder(this.tree);
                postorder(this.tree);
                
                // 同步步骤：将三种遍历的步骤交错合并
                this.syncedSteps = [];
                const maxLength = Math.max(
                    this.preorderSteps.length, 
                    this.inorderSteps.length, 
                    this.postorderSteps.length
                );
                
                for (let i = 0; i < maxLength; i++) {
                    const stepGroup = [];
                    
                    if (i < this.preorderSteps.length) {
                        stepGroup.push(this.preorderSteps[i]);
                    }
                    
                    if (i < this.inorderSteps.length) {
                        stepGroup.push(this.inorderSteps[i]);
                    }
                    
                    if (i < this.postorderSteps.length) {
                        stepGroup.push(this.postorderSteps[i]);
                    }
                    
                    this.syncedSteps.push(stepGroup);
                }
            }
            
            // 执行下一步
            nextStep() {
                if (this.currentStepIndex >= this.syncedSteps.length) {
                    this.pause();
                    return;
                }
                
                const stepGroup = this.syncedSteps[this.currentStepIndex];
                let stepDescription = "";
                
                // 执行当前步骤组中的所有步骤
                stepGroup.forEach(step => {
                    if (step.type === 'visit') {
                        // 访问节点
                        step.node[`visited${step.traversal.charAt(0).toUpperCase() + step.traversal.slice(1)}`] = true;
                        step.node.highlighted = true;
                        
                        // 设置高亮颜色
                        if (step.traversal === 'preorder') {
                            step.node.highlightColor = '#FF5252';
                            this.preorderPath.push({x: step.node.x, y: step.node.y});
                        } else if (step.traversal === 'inorder') {
                            step.node.highlightColor = '#448AFF';
                            this.inorderPath.push({x: step.node.x, y: step.node.y});
                        } else if (step.traversal === 'postorder') {
                            step.node.highlightColor = '#4CAF50';
                            this.postorderPath.push({x: step.node.x, y: step.node.y});
                        }
                        
                        // 更新序列显示
                        this.updateSequenceDisplay(step.traversal, step.node.value);
                        
                        stepDescription = step.description;
                    } else if (step.type === 'move') {
                        // 移动轨迹
                        if (step.from && step.to) {
                            if (step.traversal === 'preorder') {
                                this.preorderPath.push({x: step.from.x, y: step.from.y});
                                this.preorderPath.push({x: step.to.x, y: step.to.y});
                            } else if (step.traversal === 'inorder') {
                                this.inorderPath.push({x: step.from.x, y: step.from.y});
                                this.inorderPath.push({x: step.to.x, y: step.to.y});
                            } else if (step.traversal === 'postorder') {
                                this.postorderPath.push({x: step.from.x, y: step.from.y});
                                this.postorderPath.push({x: step.to.x, y: step.to.y});
                            }
                        }
                        
                        if (stepDescription === "") {
                            stepDescription = step.description;
                        }
                    }
                });
                
                // 更新步骤说明
                document.getElementById('stepDescription').textContent = stepDescription || `步骤 ${this.currentStepIndex + 1}/${this.syncedSteps.length}`;
                
                this.currentStepIndex++;
                this.draw();
                
                // 检查是否完成
                if (this.currentStepIndex >= this.syncedSteps.length) {
                    document.getElementById('stepDescription').textContent = "遍历完成！";
                    this.disableButton('nextStepBtn');
                    this.disableButton('playPauseBtn');
                }
                
                // 更新按钮状态
                this.updateButtonStates();
            }
            
            // 执行上一步
            prevStep() {
                if (this.currentStepIndex <= 0) return;
                
                this.currentStepIndex--;
                const stepGroup = this.syncedSteps[this.currentStepIndex];
                
                // 撤销当前步骤组中的所有步骤
                stepGroup.forEach(step => {
                    if (step.type === 'visit') {
                        // 撤销访问节点
                        step.node[`visited${step.traversal.charAt(0).toUpperCase() + step.traversal.slice(1)}`] = false;
                        step.node.highlighted = false;
                        step.node.highlightColor = null;
                        
                        // 从序列中移除节点
                        this.removeFromSequenceDisplay(step.traversal, step.node.value);
                        
                        // 从路径中移除点
                        if (step.traversal === 'preorder' && this.preorderPath.length > 0) {
                            this.preorderPath.pop();
                        } else if (step.traversal === 'inorder' && this.inorderPath.length > 0) {
                            this.inorderPath.pop();
                        } else if (step.traversal === 'postorder' && this.postorderPath.length > 0) {
                            this.postorderPath.pop();
                        }
                    } else if (step.type === 'move') {
                        // 从路径中移除移动点
                        if (step.from && step.to) {
                            if (step.traversal === 'preorder' && this.preorderPath.length >= 2) {
                                this.preorderPath.pop();
                                this.preorderPath.pop();
                            } else if (step.traversal === 'inorder' && this.inorderPath.length >= 2) {
                                this.inorderPath.pop();
                                this.inorderPath.pop();
                            } else if (step.traversal === 'postorder' && this.postorderPath.length >= 2) {
                                this.postorderPath.pop();
                                this.postorderPath.pop();
                            }
                        }
                    }
                });
                
                // 更新步骤说明
                if (this.currentStepIndex > 0) {
                    const prevStepGroup = this.syncedSteps[this.currentStepIndex - 1];
                    let prevDescription = "";
                    prevStepGroup.forEach(step => {
                        if (step.type === 'visit') {
                            prevDescription = step.description;
                        }
                    });
                    document.getElementById('stepDescription').textContent = prevDescription || `步骤 ${this.currentStepIndex}/${this.syncedSteps.length}`;
                } else {
                    document.getElementById('stepDescription').textContent = "点击'播放'按钮开始动画";
                }
                
                this.draw();
                this.updateButtonStates();
            }
            
            // 更新序列显示
            updateSequenceDisplay(traversalType, value) {
                const sequenceId = traversalType + 'Sequence';
                const sequenceElement = document.getElementById(sequenceId);
                let currentSequence = sequenceElement.textContent;
                
                if (currentSequence === '-') {
                    sequenceElement.textContent = value;
                } else {
                    sequenceElement.textContent = currentSequence + ' → ' + value;
                }
            }
            
            // 从序列显示中移除节点
            removeFromSequenceDisplay(traversalType, value) {
                const sequenceId = traversalType + 'Sequence';
                const sequenceElement = document.getElementById(sequenceId);
                let currentSequence = sequenceElement.textContent;
                
                if (currentSequence.includes(' → ')) {
                    const parts = currentSequence.split(' → ');
                    parts.pop(); // 移除最后一个
                    sequenceElement.textContent = parts.length > 0 ? parts.join(' → ') : '-';
                } else {
                    sequenceElement.textContent = '-';
                }
            }
            
            // 绘制树和轨迹
            draw() {
                // 清除画布
                this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
                
                // 绘制轨迹
                this.drawPath(this.preorderPath, '#FF5252');
                this.drawPath(this.inorderPath, '#448AFF');
                this.drawPath(this.postorderPath, '#4CAF50');
                
                // 绘制树（递归绘制所有节点）
                this.drawTree(this.tree);
            }
            
            // 绘制路径
            drawPath(path, color) {
                if (path.length < 2) return;
                
                this.ctx.beginPath();
                this.ctx.moveTo(path[0].x, path[0].y);
                
                for (let i = 1; i < path.length; i++) {
                    this.ctx.lineTo(path[i].x, path[i].y);
                }
                
                this.ctx.strokeStyle = color;
                this.ctx.lineWidth = 3;
                this.ctx.lineCap = 'round';
                this.ctx.lineJoin = 'round';
                this.ctx.stroke();
                
                // 绘制路径点
                for (let i = 0; i < path.length; i++) {
                    this.ctx.beginPath();
                    this.ctx.arc(path[i].x, path[i].y, 4, 0, Math.PI * 2);
                    this.ctx.fillStyle = color;
                    this.ctx.fill();
                }
            }
            
            // 递归绘制树
            drawTree(node) {
                if (!node) return;
                
                // 先绘制子节点
                if (node.left) this.drawTree(node.left);
                if (node.right) this.drawTree(node.right);
                
                // 绘制当前节点
                node.draw(this.ctx);
            }
            
            // 播放动画
            play() {
                if (this.isPlaying) return;
                
                this.isPlaying = true;
                document.getElementById('playPauseBtn').textContent = '暂停';
                this.enableButton('nextStepBtn');
                this.enableButton('prevStepBtn');
                
                const animate = () => {
                    if (!this.isPlaying) return;
                    
                    this.nextStep();
                    
                    if (this.currentStepIndex < this.syncedSteps.length) {
                        // 根据速度计算延迟时间（速度值1-10，对应延迟1000ms-100ms）
                        const delay = 1100 - (this.speed * 100);
                        setTimeout(() => {
                            this.animationId = requestAnimationFrame(animate);
                        }, delay);
                    } else {
                        this.pause();
                    }
                };
                
                this.animationId = requestAnimationFrame(animate);
            }
            
            // 暂停动画
            pause() {
                this.isPlaying = false;
                document.getElementById('playPauseBtn').textContent = '播放';
                
                if (this.animationId) {
                    cancelAnimationFrame(this.animationId);
                    this.animationId = null;
                }
            }
            
            // 重置动画
            reset() {
                this.pause();
                this.currentStepIndex = 0;
                
                // 重置所有节点状态
                const resetNode = (node) => {
                    if (!node) return;
                    
                    node.visitedPreorder = false;
                    node.visitedInorder = false;
                    node.visitedPostorder = false;
                    node.highlighted = false;
                    node.highlightColor = null;
                    
                    resetNode(node.left);
                    resetNode(node.right);
                };
                
                resetNode(this.tree);
                
                // 清空路径
                this.preorderPath = [];
                this.inorderPath = [];
                this.postorderPath = [];
                
                // 重置序列显示
                document.getElementById('preorderSequence').textContent = '-';
                document.getElementById('inorderSequence').textContent = '-';
                document.getElementById('postorderSequence').textContent = '-';
                document.getElementById('stepDescription').textContent = "点击'播放'按钮开始动画";
                
                // 重置按钮状态
                this.enableButton('playPauseBtn');
                this.enableButton('nextStepBtn');
                this.enableButton('prevStepBtn');
                
                this.draw();
            }
            
            // 设置速度
            setSpeed(speed) {
                this.speed = speed;
            }
            
            // 更新按钮状态
            updateButtonStates() {
                if (this.currentStepIndex <= 0) {
                    this.disableButton('prevStepBtn');
                } else {
                    this.enableButton('prevStepBtn');
                }
                
                if (this.currentStepIndex >= this.syncedSteps.length) {
                    this.disableButton('nextStepBtn');
                } else {
                    this.enableButton('nextStepBtn');
                }
            }
            
            disableButton(buttonId) {
                document.getElementById(buttonId).disabled = true;
            }
            
            enableButton(buttonId) {
                document.getElementById(buttonId).disabled = false;
            }
        }

        // 页面加载完成后初始化
        document.addEventListener('DOMContentLoaded', () => {
            // 创建动画管理器
            const animation = new TraversalAnimation('treeCanvas');
            
            // 绑定按钮事件
            document.getElementById('playPauseBtn').addEventListener('click', () => {
                if (animation.isPlaying) {
                    animation.pause();
                } else {
                    animation.play();
                }
            });
            
            document.getElementById('nextStepBtn').addEventListener('click', () => {
                animation.pause();
                animation.nextStep();
            });
            
            document.getElementById('prevStepBtn').addEventListener('click', () => {
                animation.pause();
                animation.prevStep();
            });
            
            document.getElementById('resetBtn').addEventListener('click', () => {
                animation.reset();
            });
            
            // 绑定速度滑块事件
            const speedSlider = document.getElementById('speedSlider');
            speedSlider.addEventListener('input', () => {
                animation.setSpeed(parseInt(speedSlider.value));
            });
            
            // 初始按钮状态
            animation.updateButtonStates();
        });
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

### 功能说明

欢迎使用“二叉树三种遍历顺序对比”交互式教学动画！本工具旨在通过动态可视化技术，帮助您直观理解二叉树遍历的核心概念。动画将同步展示**先序遍历（Pre-order）**、**中序遍历（In-order）**和**后序遍历（Post-order）**在同一棵二叉树上的完整执行过程，通过对比鲜明的颜色轨迹和实时反馈，让抽象的递归算法变得清晰可见。

### 主要功能

1.  **同步可视化对比**
    *   三种遍历算法同时启动，以**红、蓝、绿**三种颜色轨迹在画布上同步绘制其访问路径。
    *   节点被访问时，会高亮显示对应的颜色，并在节点上留下永久性的小色点标记。

2.  **完整的交互控制**
    *   **播放/暂停**：控制动画的连续自动播放。
    *   **下一步/上一步**：手动单步执行或回退，便于仔细研究每一步的变化。
    *   **重置**：一键恢复到初始状态，重新开始观察。
    *   **速度调节**：通过滑块控制自动播放的速度（1最慢，10最快）。

3.  **实时信息反馈**
    *   **遍历序列输出区**：右侧面板实时显示三种遍历已访问的节点序列，清晰展示最终输出结果的差异。
    *   **当前步骤说明**：底部区域用文字描述当前正在执行的操作（如“先序：访问节点A”）。

4.  **精心设计的视觉编码**
    *   **颜色语义**：红色（先序-优先）、蓝色（中序-居中）、绿色（后序-最后），颜色选择符合遍历特性。
    *   **轨迹与状态**：彩色线条表示移动路径，节点高亮表示访问动作，小色点记录历史访问状态。

### 设计特色

1.  **认知负荷优化**：初始界面仅显示二叉树结构，避免信息过载。动画开始后，轨迹和状态信息才逐步呈现，引导用户注意力。
2.  **过程分解与同步**：将递归遍历分解为“移动”和“访问”两个原子操作，并让三种遍历同步执行，极大地方便了对比观察。
3.  **多模态学习支持**：结合了**视觉动态**（轨迹、高亮）、**文本输出**（序列、说明）和**交互控制**，满足不同学习风格的用户需求。
4.  **教学友好性**：“上一步”功能允许回溯，方便纠正理解错误或反复观察难点步骤，这是传统动画或视频难以实现的。

### 教学要点

通过本动画，请重点观察和理解以下核心教学要点：

1.  **访问节点的时机是根本区别**
    *   **先序**：每进入一个子树，**首先访问根节点**（红点先出现）。
    *   **中序**：先深入左子树，返回时**访问根节点**，再进入右子树（蓝点在左右移动之间出现）。
    *   **后序**：在左右子树都探索完毕后，**最后访问根节点**（绿点最后出现）。

2.  **递归过程的栈式展开**
    观察轨迹如何深入左子树到底部，然后回溯，再深入右子树。这个过程直观展示了递归调用栈的“后进先出”行为。

3.  **路径相同，时机不同**
    注意三种遍历的**移动路径是完全相同的**（都访问了所有节点），但**在路径的哪个“点”上执行访问操作**，决定了遍历的顺序和输出结果。

4.  **序列输出的构建过程**
    对照右侧的序列输出区，观察每个节点是何时被添加到序列中的，理解序列是如何一步步构建起来的。

### 使用建议

为了获得最佳学习效果，建议按以下步骤使用本动画：

1.  **初次体验（整体感知）**
    *   点击**播放**，以默认速度观看一遍完整的动画。
    *   不要纠结于细节，先感受三种颜色轨迹如何交织、节点如何被依次点亮，对整个过程形成一个整体印象。

2.  **逐步探索（深入理解）**
    *   点击**重置**，然后使用**下一步**按钮手动执行。
    *   每执行一步，仔细观察：
        *   哪个（些）节点被高亮了？是什么颜色？
        *   右侧哪个序列增加了节点？
        *   下方的步骤说明文字是什么？
        *   三种遍历的当前状态有何不同？
    *   遇到不理解的地方，使用**上一步**按钮回退，重新观察。

3.  **对比研究（发现规律）**
    *   关注一个具体的子树（例如以B为根的子树），观察三种遍历在处理这个子树时，访问节点B的时机有何不同。
    *   观察叶子节点（D、E、F、G）被访问时，三种遍历的轨迹是否汇聚于此？访问顺序是否一致？

4.  **速度调节与复习**
    *   对于复杂步骤，调慢速度反复播放。
    *   在理解整个流程后，可以调快速度进行快速复习，巩固记忆。

5.  **关联理论与代码**
    *   在观看动画的同时，回忆或查看三种遍历的递归算法代码。将动画中的每一步（“移动到左子树”、“访问节点”）与代码中的对应语句联系起来，实现从直观表象到抽象逻辑的升华。

---

希望这个交互式动画能成为您理解二叉树遍历算法的得力助手！通过主动操控、仔细观察和思考对比，您将能够牢固掌握这一数据结构与算法中的核心概念。祝您学习愉快，探索顺利！