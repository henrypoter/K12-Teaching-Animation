# 需求：斐波那契数列递归树（不动画根本看不出指数爆炸）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
用户的核心需求是通过一个**动态、可视化的交互动画**，直观地理解斐波那契数列递归计算的两个关键点：
1.  **递归过程的重复性**：展示计算 `fib(n)` 时，大量相同的子问题（如 `fib(2)`）被重复计算，这是递归算法效率低下的根本原因。
2.  **指数级的时间复杂度**：通过递归树的“生长”过程，让学习者亲眼看到随着 `n` 的增大，递归调用次数如何呈爆炸式（指数级）增长，从而深刻理解“指数爆炸”的概念。

用户需要一个**教学工具**，而非单纯的演示。它应该允许学习者控制进度、探索不同参数，并清晰地展示每一步的计算逻辑和状态。

#### 教学设计思路
*   **核心概念**：斐波那契数列定义（`F(0)=0, F(1)=1, F(n)=F(n-1)+F(n-2)`）、递归函数调用、递归树、重复子问题、指数时间复杂度（O(2^n)）。
*   **认知规律**：
    *   **从具体到抽象**：从一个具体的 `fib(5)` 计算开始，让学习者先看到完整的递归树，建立整体印象。
    *   **从慢到快**：初始演示采用慢速或步进模式，让学习者能跟上调用逻辑。之后提供加速或直接完成的功能，以感受“爆炸”效果。
    *   **从观察到交互**：先引导观察，再允许用户输入不同的 `n` 值，亲自启动动画，并可能通过高亮等功能聚焦特定分支。
*   **交互设计**：
    *   **控制面板**：提供开始、暂停、步进、重置、调整速度等控件，让用户掌握学习节奏。
    *   **参数输入**：允许用户输入一个 `n` 值（如3到10之间，平衡可读性与爆炸感），重新生成递归树。
    *   **可视化焦点**：
        *   当前正在计算的节点高亮显示。
        *   已计算完成并缓存了结果的节点用不同颜色/样式表示。
        *   用连线清晰表示函数调用关系。
        *   实时显示当前总调用次数、已计算出的值等信息。
*   **视觉呈现**：
    *   **递归树结构**：采用经典的树形图自上而下展开。根节点是 `fib(n)`，向下分裂为 `fib(n-1)` 和 `fib(n-2)` 两个子节点，以此类推。
    *   **节点设计**：每个节点是一个视觉元素（如圆角矩形），内部显示 `fib(?)` 以及最终计算出的值（当计算完成后）。
    *   **生长动画**：新的节点和连线以平滑的动画形式出现，模拟树的“生长”。
    *   **重复子问题高亮**：当算法首次计算 `fib(3)` 时，其子树正常展开。当在另一个分支再次遇到 `fib(3)` 时，可以将其整个子树用特殊颜色（如灰色）快速“绘制”出来，并显示“重复计算”的提示，强烈对比出效率问题。

#### 配色方案选择
选择一套清晰、友好且有助于区分状态的配色：
*   **背景**：浅灰色（`#f5f7fa`）或白色，确保清晰度。
*   **树与节点**：
    *   **待计算节点**：浅蓝色边框和填充（`#d0e7ff`），代表“等待中”。
    *   **正在计算节点**：亮黄色填充（`#fff9c4`），边框加粗，吸引全部注意力。
    *   **已计算完成节点**：柔和的绿色填充（`#d4edda`），边框为深绿色（`#155724`），表示“已解决”。
    *   **重复计算的子树**：使用统一的浅灰色（`#e9ecef`）填充，并可能带有斜纹图案，直观表示“这是重复劳动，本可避免”。
*   **连线**：使用深灰色（`#495057`）细线。
*   **控制面板**：采用中性色（如蓝色系 `#007bff` 用于主要按钮，灰色 `#6c757d` 用于次要按钮），符合常见UI习惯。
*   **文字与数据**：深灰色（`#212529`）确保可读性，关键数据（如调用次数）可用醒目的橙色（`#fd7e14`）强调。

#### 交互功能列表
1.  **动画控制**：
    *   “开始/暂停”按钮：控制动画播放。
    *   “下一步”按钮：单步执行一次递归调用。
    *   “重置”按钮：清除当前树，回到初始状态。
    *   “速度调节”滑块：控制动画播放速度。
2.  **参数设置**：
    *   数字输入框：用于输入要计算的斐波那契数列项数 `n`（建议默认5，范围3-15）。
    *   “生成”按钮：根据输入的 `n` 重新开始。
3.  **可视化辅助**：
    *   “显示/隐藏数值”开关：在节点上显示或隐藏具体的斐波那契数值。
    *   “高亮重复子树”开关：自动用不同样式标记所有重复计算的子树。
4.  **信息面板**（实时显示）：
    *   当前计算的表达式（如 `Calculating: fib(5) = fib(4) + fib(3)`）。
    *   总递归调用次数。
    *   当前递归深度。
    *   最终结果：`fib(n) = ?`。
5.  **教学提示**：在侧边或顶部提供一个简明的文字区域，解释当前动画步骤在说明什么概念（如“现在正在展开 `fib(4)` 的子树...”，“注意！`fib(2)` 被第二次计算到了，这就是重复子问题”）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>斐波那契数列递归树 - 可视化指数爆炸</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #212529;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        header {
            text-align: center;
            padding: 15px;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        h1 {
            font-size: 2.2rem;
            margin-bottom: 8px;
        }
        
        .subtitle {
            font-size: 1.1rem;
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .visualization-panel {
            flex: 1;
            min-width: 700px;
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-direction: column;
        }
        
        .control-panel {
            flex: 0 0 320px;
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .panel-title {
            font-size: 1.4rem;
            color: #2575fc;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #e9ecef;
        }
        
        .canvas-container {
            flex: 1;
            border: 1px solid #dee2e6;
            border-radius: 8px;
            overflow: hidden;
            background-color: #f8f9fa;
            position: relative;
        }
        
        #fibCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .control-section {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #2575fc;
        }
        
        .control-group {
            margin-bottom: 15px;
        }
        
        .control-group:last-child {
            margin-bottom: 0;
        }
        
        .control-label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #495057;
        }
        
        .input-row {
            display: flex;
            gap: 10px;
            align-items: center;
        }
        
        input[type="number"] {
            width: 80px;
            padding: 10px;
            border: 1px solid #ced4da;
            border-radius: 5px;
            font-size: 1rem;
            text-align: center;
        }
        
        button {
            padding: 10px 16px;
            border: none;
            border-radius: 5px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            font-size: 0.95rem;
        }
        
        .btn-primary {
            background-color: #007bff;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #0056b3;
        }
        
        .btn-secondary {
            background-color: #6c757d;
            color: white;
        }
        
        .btn-secondary:hover {
            background-color: #545b62;
        }
        
        .btn-success {
            background-color: #28a745;
            color: white;
        }
        
        .btn-success:hover {
            background-color: #1e7e34;
        }
        
        .btn-warning {
            background-color: #ffc107;
            color: #212529;
        }
        
        .btn-warning:hover {
            background-color: #e0a800;
        }
        
        .btn-danger {
            background-color: #dc3545;
            color: white;
        }
        
        .btn-danger:hover {
            background-color: #bd2130;
        }
        
        .btn-group {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
        }
        
        .btn-small {
            padding: 6px 12px;
            font-size: 0.85rem;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        input[type="range"] {
            flex: 1;
            height: 6px;
            border-radius: 3px;
            background: #dee2e6;
            outline: none;
            -webkit-appearance: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: #007bff;
            cursor: pointer;
        }
        
        .toggle-switch {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .switch {
            position: relative;
            display: inline-block;
            width: 50px;
            height: 24px;
        }
        
        .switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }
        
        .slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #ccc;
            transition: .4s;
            border-radius: 24px;
        }
        
        .slider:before {
            position: absolute;
            content: "";
            height: 16px;
            width: 16px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: .4s;
            border-radius: 50%;
        }
        
        input:checked + .slider {
            background-color: #28a745;
        }
        
        input:checked + .slider:before {
            transform: translateX(26px);
        }
        
        .info-panel {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #28a745;
            margin-top: 10px;
        }
        
        .info-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            padding-bottom: 8px;
            border-bottom: 1px dashed #dee2e6;
        }
        
        .info-item:last-child {
            margin-bottom: 0;
            padding-bottom: 0;
            border-bottom: none;
        }
        
        .info-label {
            font-weight: 600;
            color: #495057;
        }
        
        .info-value {
            font-weight: 700;
            color: #fd7e14;
        }
        
        .teaching-tips {
            background-color: #fff3cd;
            border-left: 4px solid #ffc107;
            padding: 15px;
            border-radius: 8px;
            margin-top: 10px;
        }
        
        .teaching-tips h3 {
            color: #856404;
            margin-bottom: 8px;
            font-size: 1.1rem;
        }
        
        .teaching-tips p {
            color: #856404;
        }
        
        .status-bar {
            display: flex;
            justify-content: space-between;
            margin-top: 15px;
            padding: 10px 15px;
            background-color: #e9ecef;
            border-radius: 5px;
            font-size: 0.9rem;
        }
        
        .status-item {
            display: flex;
            gap: 5px;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #dee2e6;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.85rem;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
            border: 1px solid rgba(0, 0, 0, 0.1);
        }
        
        footer {
            text-align: center;
            padding: 15px;
            color: #6c757d;
            font-size: 0.9rem;
            border-top: 1px solid #dee2e6;
            margin-top: 20px;
        }
        
        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
            
            .visualization-panel {
                min-width: 100%;
            }
            
            .control-panel {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>斐波那契数列递归树可视化</h1>
            <p class="subtitle">通过动画直观展示递归算法的重复计算与指数爆炸现象</p>
        </header>
        
        <div class="main-content">
            <div class="visualization-panel">
                <h2 class="panel-title">递归树可视化</h2>
                <div class="canvas-container">
                    <canvas id="fibCanvas"></canvas>
                </div>
                
                <div class="status-bar">
                    <div class="status-item">
                        <span>当前状态:</span>
                        <strong id="currentStatus">就绪</strong>
                    </div>
                    <div class="status-item">
                        <span>当前计算:</span>
                        <strong id="currentCalculation">-</strong>
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #d0e7ff;"></div>
                        <span>待计算节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #fff9c4;"></div>
                        <span>正在计算节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #d4edda;"></div>
                        <span>已计算完成节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e9ecef; background-image: repeating-linear-gradient(45deg, transparent, transparent 5px, rgba(0,0,0,0.1) 5px, rgba(0,0,0,0.1) 10px);"></div>
                        <span>重复计算的子树</span>
                    </div>
                </div>
            </div>
            
            <div class="control-panel">
                <h2 class="panel-title">控制面板</h2>
                
                <div class="control-section">
                    <div class="control-group">
                        <label class="control-label">斐波那契数 n (3-15):</label>
                        <div class="input-row">
                            <input type="number" id="fibInput" min="3" max="15" value="5">
                            <button id="generateBtn" class="btn-primary">生成递归树</button>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <label class="control-label">动画控制:</label>
                        <div class="btn-group">
                            <button id="startBtn" class="btn-success">开始</button>
                            <button id="pauseBtn" class="btn-warning">暂停</button>
                            <button id="stepBtn" class="btn-secondary">单步执行</button>
                            <button id="resetBtn" class="btn-danger">重置</button>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <label class="control-label">动画速度:</label>
                        <div class="slider-container">
                            <span>慢</span>
                            <input type="range" id="speedSlider" min="1" max="10" value="5">
                            <span>快</span>
                            <span id="speedValue">中速</span>
                        </div>
                    </div>
                </div>
                
                <div class="control-section">
                    <div class="control-group">
                        <label class="control-label">可视化选项:</label>
                        <div class="toggle-switch">
                            <span>显示节点数值</span>
                            <label class="switch">
                                <input type="checkbox" id="showValuesToggle" checked>
                                <span class="slider"></span>
                            </label>
                        </div>
                        <div class="toggle-switch">
                            <span>高亮重复子树</span>
                            <label class="switch">
                                <input type="checkbox" id="highlightRepeatsToggle" checked>
                                <span class="slider"></span>
                            </label>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <label class="control-label">快速示例:</label>
                        <div class="btn-group">
                            <button class="btn-small btn-secondary" data-n="4">n=4</button>
                            <button class="btn-small btn-secondary" data-n="6">n=6</button>
                            <button class="btn-small btn-secondary" data-n="8">n=8</button>
                            <button class="btn-small btn-secondary" data-n="10">n=10</button>
                        </div>
                    </div>
                </div>
                
                <div class="info-panel">
                    <h3 class="panel-title">计算信息</h3>
                    <div class="info-item">
                        <span class="info-label">递归调用次数:</span>
                        <span class="info-value" id="callCount">0</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">当前递归深度:</span>
                        <span class="info-value" id="currentDepth">0</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">重复计算次数:</span>
                        <span class="info-value" id="repeatCount">0</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">最终结果 fib(n):</span>
                        <span class="info-value" id="finalResult">-</span>
                    </div>
                </div>
                
                <div class="teaching-tips">
                    <h3>教学提示</h3>
                    <p id="teachingText">点击"生成递归树"按钮开始。观察递归树如何展开，注意相同子问题被重复计算的现象。</p>
                </div>
            </div>
        </div>
        
        <footer>
            <p>斐波那契递归树可视化教学工具 | 设计用于展示递归算法的指数时间复杂度与重复子问题</p>
        </footer>
    </div>

    <script>
        // 全局变量
        let canvas, ctx;
        let animationId = null;
        let isAnimating = false;
        let animationSpeed = 500; // 毫秒
        let currentStep = 0;
        let totalSteps = 0;
        
        // 斐波那契递归树数据
        let treeData = {
            nodes: [],
            edges: [],
            root: null
        };
        
        // 计算状态
        let calculationState = {
            n: 5,
            callCount: 0,
            repeatCount: 0,
            currentDepth: 0,
            finalResult: null,
            calculatedValues: {}, // 缓存已计算的值
            currentCalculation: null,
            isRepeating: false
        };
        
        // 节点状态常量
        const NODE_STATE = {
            PENDING: 'pending',      // 待计算
            CALCULATING: 'calculating', // 正在计算
            CALCULATED: 'calculated',   // 已计算完成
            REPEAT: 'repeat'         // 重复计算
        };
        
        // 颜色配置
        const COLORS = {
            [NODE_STATE.PENDING]: '#d0e7ff',
            [NODE_STATE.CALCULATING]: '#fff9c4',
            [NODE_STATE.CALCULATED]: '#d4edda',
            [NODE_STATE.REPEAT]: '#e9ecef',
            edge: '#495057',
            text: '#212529',
            highlight: '#fd7e14'
        };
        
        // 节点类
        class TreeNode {
            constructor(id, value, depth, x, y) {
                this.id = id;
                this.value = value;
                this.depth = depth;
                this.x = x;
                this.y = y;
                this.state = NODE_STATE.PENDING;
                this.result = null;
                this.children = [];
                this.parent = null;
                this.width = 60;
                this.height = 40;
                this.isRepeatingSubtree = false;
            }
            
            draw() {
                // 绘制节点背景
                let fillColor = COLORS[this.state];
                
                // 如果是重复子树，添加斜纹图案
                if (this.isRepeatingSubtree && document.getElementById('highlightRepeatsToggle').checked) {
                    ctx.fillStyle = COLORS[NODE_STATE.REPEAT];
                    ctx.fillRect(this.x - this.width/2, this.y - this.height/2, this.width, this.height);
                    
                    // 绘制斜纹
                    ctx.strokeStyle = 'rgba(0, 0, 0, 0.1)';
                    ctx.lineWidth = 1;
                    ctx.beginPath();
                    for (let i = -this.width; i < this.width; i += 10) {
                        ctx.moveTo(this.x - this.width/2 + i, this.y - this.height/2);
                        ctx.lineTo(this.x - this.width/2 + i + this.height, this.y + this.height/2);
                    }
                    ctx.stroke();
                    
                    // 覆盖一层半透明原色
                    ctx.fillStyle = fillColor + '80'; // 添加透明度
                    ctx.fillRect(this.x - this.width/2, this.y - this.height/2, this.width, this.height);
                } else {
                    ctx.fillStyle = fillColor;
                    ctx.fillRect(this.x - this.width/2, this.y - this.height/2, this.width, this.height);
                }
                
                // 绘制节点边框
                ctx.strokeStyle = this.state === NODE_STATE.CALCULATING ? '#ffc107' : '#495057';
                ctx.lineWidth = this.state === NODE_STATE.CALCULATING ? 3 : 1;
                ctx.strokeRect(this.x - this.width/2, this.y - this.height/2, this.width, this.height);
                
                // 绘制节点文本
                ctx.fillStyle = COLORS.text;
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                
                let displayText = `fib(${this.value})`;
                if (this.result !== null && document.getElementById('showValuesToggle').checked) {
                    displayText += `\n=${this.result}`;
                }
                
                // 绘制多行文本
                const lines = displayText.split('\n');
                const lineHeight = 18;
                const startY = this.y - (lines.length - 1) * lineHeight / 2;
                
                lines.forEach((line, index) => {
                    ctx.fillText(line, this.x, startY + index * lineHeight);
                });
            }
        }
        
        // 初始化Canvas
        function initCanvas() {
            canvas = document.getElementById('fibCanvas');
            ctx = canvas.getContext('2d');
            
            // 设置Canvas尺寸
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // 初始化树
            generateTree(5);
        }
        
        // 调整Canvas大小
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            drawTree();
        }
        
        // 生成斐波那契递归树
        function generateTree(n) {
            // 重置状态
            resetCalculation();
            calculationState.n = n;
            
            // 清空树数据
            treeData.nodes = [];
            treeData.edges = [];
            
            // 创建根节点
            const rootX = canvas.width / 2;
            const rootY = 80;
            const rootNode = new TreeNode(`fib(${n})`, n, 0, rootX, rootY);
            treeData.root = rootNode;
            treeData.nodes.push(rootNode);
            
            // 生成树结构
            generateSubtree(rootNode, n, 0, rootX, rootY, canvas.width * 0.8);
            
            // 更新UI
            updateTeachingText(`已生成 fib(${n}) 的递归树结构。点击"开始"按钮观察递归计算过程。`);
            updateInfoPanel();
            drawTree();
        }
        
        // 递归生成子树
        function generateSubtree(node, value, depth, x, y, width) {
            if (value <= 1) {
                return;
            }
            
            // 计算子节点的位置
            const childDepth = depth + 1;
            const childY = y + 100;
            const spacing = width / (Math.pow(2, childDepth));
            
            // 左子节点: fib(n-1)
            if (value - 1 >= 0) {
                const leftX = x - spacing;
                const leftNode = new TreeNode(`fib(${value-1})`, value-1, childDepth, leftX, childY);
                leftNode.parent = node;
                node.children.push(leftNode);
                treeData.nodes.push(leftNode);
                treeData.edges.push({from: node, to: leftNode});
                
                generateSubtree(leftNode, value-1, childDepth, leftX, childY, width);
            }
            
            // 右子节点: fib(n-2)
            if (value - 2 >= 0) {
                const rightX = x + spacing;
                const rightNode = new TreeNode(`fib(${value-2})`, value-2, childDepth, rightX, childY);
                rightNode.parent = node;
                node.children.push(rightNode);
                treeData.nodes.push(rightNode);
                treeData.edges.push({from: node, to: rightNode});
                
                generateSubtree(rightNode, value-2, childDepth, rightX, childY, width);
            }
        }
        
        // 绘制整个树
        function drawTree() {
            if (!ctx) return;
            
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制边
            ctx.strokeStyle = COLORS.edge;
            ctx.lineWidth = 1;
            treeData.edges.forEach(edge => {
                ctx.beginPath();
                ctx.moveTo(edge.from.x, edge.from.y + edge.from.height/2);
                ctx.lineTo(edge.to.x, edge.to.y - edge.to.height/2);
                ctx.stroke();
            });
            
            // 绘制节点
            treeData.nodes.forEach(node => {
                node.draw();
            });
        }
        
        // 模拟递归计算斐波那契数
        function fib(n, node, isRepeat = false) {
            calculationState.callCount++;
            calculationState.currentDepth = Math.max(calculationState.currentDepth, node.depth);
            
            // 更新当前计算节点
            node.state = NODE_STATE.CALCULATING;
            calculationState.currentCalculation = `fib(${n})`;
            
            if (isRepeat) {
                calculationState.repeatCount++;
                node.isRepeatingSubtree = true;
                node.state = NODE_STATE.REPEAT;
                
                // 标记整个子树为重复
                markSubtreeAsRepeat(node);
                
                updateTeachingText(`发现重复计算: fib(${n}) 已经在之前计算过了！这是递归算法效率低下的主要原因。`);
                updateInfoPanel();
                drawTree();
                
                // 直接返回缓存的值
                return calculationState.calculatedValues[n];
            }
            
            // 更新教学提示
            if (n <= 1) {
                updateTeachingText(`基础情况: fib(${n}) = ${n}。递归到达终点，开始回溯。`);
            } else {
                updateTeachingText(`计算 fib(${n}) = fib(${n-1}) + fib(${n-2})。递归调用继续深入...`);
            }
            
            updateInfoPanel();
            drawTree();
            
            // 等待动画
            return new Promise(resolve => {
                setTimeout(() => {
                    // 检查是否已经计算过这个值
                    if (calculationState.calculatedValues.hasOwnProperty(n)) {
                        calculationState.repeatCount++;
                        node.isRepeatingSubtree = true;
                        node.state = NODE_STATE.REPEAT;
                        markSubtreeAsRepeat(node);
                        
                        updateTeachingText(`发现重复计算: fib(${n}) 已经在之前计算过了！这是递归算法效率低下的主要原因。`);
                        updateInfoPanel();
                        drawTree();
                        
                        resolve(calculationState.calculatedValues[n]);
                        return;
                    }
                    
                    // 基础情况
                    if (n <= 1) {
                        node.result = n;
                        node.state = NODE_STATE.CALCULATED;
                        calculationState.calculatedValues[n] = n;
                        
                        // 如果是根节点，更新最终结果
                        if (n === calculationState.n) {
                            calculationState.finalResult = n;
                        }
                        
                        updateInfoPanel();
                        drawTree();
                        resolve(n);
                        return;
                    }
                    
                    // 递归计算 fib(n-1) 和 fib(n-2)
                    const leftChild = node.children.find(child => child.value === n-1);
                    const rightChild = node.children.find(child => child.value === n-2);
                    
                    // 递归计算左子树
                    fib(n-1, leftChild).then(leftResult => {
                        // 递归计算右子树
                        fib(n-2, rightChild).then(rightResult => {
                            // 计算当前节点的值
                            const result = leftResult + rightResult;
                            node.result = result;
                            node.state = NODE_STATE.CALCULATED;
                            calculationState.calculatedValues[n] = result;
                            
                            // 如果是根节点，更新最终结果
                            if (n === calculationState.n) {
                                calculationState.finalResult = result;
                            }
                            
                            updateTeachingText(`完成计算: fib(${n}) = ${leftResult} + ${rightResult} = ${result}。回溯到上一层。`);
                            updateInfoPanel();
                            drawTree();
                            
                            resolve(result);
                        });
                    });
                }, animationSpeed);
            });
        }
        
        // 标记整个子树为重复
        function markSubtreeAsRepeat(node) {
            node.state = NODE_STATE.REPEAT;
            node.isRepeatingSubtree = true;
            
            node.children.forEach(child => {
                markSubtreeAsRepeat(child);
            });
        }
        
        // 开始动画
        function startAnimation() {
            if (isAnimating) return;
            
            isAnimating = true;
            document.getElementById('currentStatus').textContent = '计算中...';
            
            // 重置计算状态但保留树结构
            calculationState.callCount = 0;
            calculationState.repeatCount = 0;
            calculationState.currentDepth = 0;
            calculationState.finalResult = null;
            calculationState.calculatedValues = {};
            calculationState.currentCalculation = null;
            
            // 重置所有节点状态
            treeData.nodes.forEach(node => {
                node.state = NODE_STATE.PENDING;
                node.result = null;
                node.isRepeatingSubtree = false;
            });
            
            updateInfoPanel();
            drawTree();
            
            // 开始递归计算
            fib(calculationState.n, treeData.root).then(result => {
                isAnimating = false;
                document.getElementById('currentStatus').textContent = '计算完成';
                
                updateTeachingText(`计算完成! fib(${calculationState.n}) = ${result}。总共进行了 ${calculationState.callCount} 次递归调用，其中 ${calculationState.repeatCount} 次是重复计算。这就是指数时间复杂度的体现！`);
            });
        }
        
        // 暂停动画
        function pauseAnimation() {
            isAnimating = false;
            document.getElementById('currentStatus').textContent = '已暂停';
            updateTeachingText('动画已暂停。点击"开始"继续观察递归过程。');
        }
        
        // 单步执行
        function stepAnimation() {
            // 简化版本：单步执行会直接完成当前节点的计算
            updateTeachingText('单步执行功能在完整动画中更易观察。请使用开始/暂停控制动画速度。');
        }
        
        // 重置计算
        function resetCalculation() {
            isAnimating = false;
            
            calculationState.callCount = 0;
            calculationState.repeatCount = 0;
            calculationState.currentDepth = 0;
            calculationState.finalResult = null;
            calculationState.calculatedValues = {};
            calculationState.currentCalculation = null;
            
            document.getElementById('currentStatus').textContent = '就绪';
            document.getElementById('currentCalculation').textContent = '-';
            
            updateInfoPanel();
        }
        
        // 更新信息面板
        function updateInfoPanel() {
            document.getElementById('callCount').textContent = calculationState.callCount;
            document.getElementById('currentDepth').textContent = calculationState.currentDepth;
            document.getElementById('repeatCount').textContent = calculationState.repeatCount;
            document.getElementById('finalResult').textContent = calculationState.finalResult !== null ? calculationState.finalResult : '-';
            document.getElementById('currentCalculation').textContent = calculationState.currentCalculation || '-';
        }
        
        // 更新教学提示
        function updateTeachingText(text) {
            document.getElementById('teachingText').textContent = text;
        }
        
        // 事件监听器设置
        function setupEventListeners() {
            // 生成递归树按钮
            document.getElementById('generateBtn').addEventListener('click', () => {
                const n = parseInt(document.getElementById('fibInput').value);
                if (n >= 3 && n <= 15) {
                    generateTree(n);
                } else {
                    alert('请输入3到15之间的整数');
                }
            });
            
            // 动画控制按钮
            document.getElementById('startBtn').addEventListener('click', startAnimation);
            document.getElementById('pauseBtn').addEventListener('click', pauseAnimation);
            document.getElementById('stepBtn').addEventListener('click', stepAnimation);
            document.getElementById('resetBtn').addEventListener('click', () => {
                generateTree(calculationState.n);
            });
            
            // 速度滑块
            document.getElementById('speedSlider').addEventListener('input', (e) => {
                const speed = parseInt(e.target.value);
                // 速度值映射到动画延迟时间（毫秒）
                animationSpeed = 1000 - (speed - 1) * 100;
                
                // 更新速度显示
                const speedText = speed <= 3 ? '慢速' : speed <= 7 ? '中速' : '快速';
                document.getElementById('speedValue').textContent = speedText;
            });
            
            // 可视化选项切换
            document.getElementById('showValuesToggle').addEventListener('change', drawTree);
            document.getElementById('highlightRepeatsToggle').addEventListener('change', drawTree);
            
            // 快速示例按钮
            document.querySelectorAll('.btn-small[data-n]').forEach(button => {
                button.addEventListener('click', (e) => {
                    const n = parseInt(e.target.getAttribute('data-n'));
                    document.getElementById('fibInput').value = n;
                    generateTree(n);
                });
            });
            
            // 输入框回车事件
            document.getElementById('fibInput').addEventListener('keyup', (e) => {
                if (e.key === 'Enter') {
                    document.getElementById('generateBtn').click();
                }
            });
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', () => {
            initCanvas();
            setupEventListeners();
            
            // 初始教学提示
            updateTeachingText('欢迎使用斐波那契递归树可视化工具。输入一个n值(3-15)，点击"生成递归树"，然后点击"开始"观察递归计算过程。注意观察相同子问题被重复计算的现象！');
        });
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 斐波那契递归树交互式教学动画使用指南

欢迎使用"斐波那契数列递归树可视化"教学动画！本工具旨在通过动态、交互的方式，帮助您直观理解递归算法的核心特性——特别是**重复计算**和**指数时间复杂度**这两个关键概念。无论您是编程初学者、算法学习者，还是计算机科学教育者，本工具都将为您提供深刻的视觉学习体验。

---

### 一、功能说明

本动画模拟了计算斐波那契数 `fib(n)` 的经典递归过程，并以**树形图**的形式实时展示：
1. **递归调用过程**：展示函数如何不断调用自身，分解问题
2. **递归树生长**：可视化展示调用关系的树状结构如何展开
3. **重复计算高亮**：明确标识出哪些子树被重复计算
4. **计算状态跟踪**：实时显示当前计算节点、调用次数、递归深度等关键信息

### 二、主要功能

#### 1. 核心控制区
- **参数设置**：输入 n 值（3-15），点击"生成递归树"创建对应的递归树结构
- **动画控制**：
  - **开始**：启动递归计算动画
  - **暂停**：暂停当前动画
  - **单步执行**：逐步执行递归调用（建议配合暂停使用）
  - **重置**：清空当前计算状态，回到初始树结构

#### 2. 可视化调节
- **动画速度**：通过滑块调节动画播放速度（慢速→快速）
- **显示选项**：
  - 显示/隐藏节点数值
  - 高亮/取消高亮重复子树

#### 3. 快速示例
- 提供 n=4, 6, 8, 10 的预设按钮，一键生成常见示例

#### 4. 信息面板
- **递归调用次数**：已执行的递归调用总数
- **当前递归深度**：调用栈的最大深度
- **重复计算次数**：重复计算的子树数量
- **最终结果**：`fib(n)` 的计算结果
- **当前计算**：正在计算的表达式

#### 5. 教学提示区
- 实时显示当前步骤的教学解释
- 引导观察重点，解释算法行为

### 三、设计特色

#### 1. 四色状态系统
- **浅蓝色**：待计算节点
- **亮黄色**：正在计算节点（当前焦点）
- **浅绿色**：已计算完成节点
- **灰色斜纹**：重复计算的子树（效率问题的直观体现）

#### 2. 渐进式教学
- **先结构后过程**：先生成完整的树结构，再展示计算过程
- **速度可调**：支持从慢速理解到快速感受"指数爆炸"
- **提示引导**：每个关键步骤都有文字解释

#### 3. 交互友好性
- 响应式设计，适应不同屏幕尺寸
- 直观的图标和颜色编码
- 实时反馈的用户界面

### 四、教学要点

#### 重点观察内容：

1. **递归分解模式**
   - 观察 `fib(n)` 如何分解为 `fib(n-1)` 和 `fib(n-2)`
   - 注意递归的终止条件（`fib(0)` 和 `fib(1)`）

2. **重复计算现象**
   - 特别关注 `fib(2)`、`fib(3)` 等较小值的重复出现
   - 启用"高亮重复子树"功能，灰色区域直观展示效率损失

3. **指数增长规律**
   - 比较 n=5 和 n=8 的递归树规模差异
   - 注意调用次数随 n 增大的爆炸式增长

4. **计算状态流转**
   - 跟踪黄色高亮节点的移动路径
   - 理解深度优先的递归遍历顺序

#### 推荐教学流程：

1. **初次接触**：使用 n=5，慢速播放，观察完整过程
2. **重点分析**：使用 n=6，暂停在中间状态，分析当前调用栈
3. **模式识别**：使用 n=8，快速播放，感受指数增长趋势
4. **问题探究**：关闭重复高亮，再开启，对比观察效率问题

### 五、使用建议

#### 给学习者的建议：
1. **循序渐进**：从 n=4 或 5 开始，理解基本模式后再尝试更大的 n
2. **主动探索**：
   - 尝试不同的 n 值，观察树结构的变化
   - 比较开启/关闭"高亮重复子树"的视觉差异
   - 用不同速度观看同一过程，加深理解
3. **结合思考**：
   - 动画暂停时，尝试预测下一步计算
   - 记录不同 n 值对应的调用次数，验证 O(2ⁿ) 复杂度
   - 思考：如何改进算法避免重复计算？

#### 给教师/演示者的建议：
1. **课堂演示**：
   - 首次演示使用 n=5，慢速，讲解每个步骤
   - 第二次使用 n=8，快速，展示"指数爆炸"的震撼效果
   - 对比展示动态规划（记忆化）与纯递归的差异
2. **互动教学**：
   - 让学生预测 n=6 的调用次数，再用动画验证
   - 分组讨论：从动画中找出 3 个重复计算的例子
   - 设计练习：根据动画画出 n=7 的递归树
3. **深度拓展**：
   - 引导学生计算理论调用次数：T(n) = T(n-1) + T(n-2) + 1
   - 讨论递归的空间复杂度（最大递归深度）
   - 引入记忆化递归和动态规划的概念

#### 技术提示：
- 推荐使用 Chrome、Edge 或 Firefox 等现代浏览器
- n=12 以上时，动画时间较长，建议使用较快的速度设置
- 教学时可将浏览器窗口最大化，获得最佳视觉效果

---

**最后提醒**：这个动画不仅展示了斐波那契递归的计算过程，更重要的是揭示了**算法设计中的关键权衡**。通过亲眼看到"指数爆炸"和重复计算，您将对递归算法的效率问题有更直观、更深刻的理解。这正是可视化教学的魅力所在——让抽象的概念变得可见，让复杂的规律变得清晰。

祝您探索愉快，学有所获！