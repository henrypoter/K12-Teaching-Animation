# 需求：快速排序的分治递归过程（左右指针交换+递归树）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：学习数据结构和算法（如计算机科学专业学生、编程初学者）的群体。
2.  **核心需求**：理解快速排序算法中“分治”与“递归”这两个抽象概念的具体执行过程，特别是左右指针交换法的动态步骤，以及递归调用如何形成一棵“递归树”。
3.  **痛点**：
    *   难以在脑海中动态模拟指针移动、元素交换和数组分割的过程。
    *   不理解递归调用栈与递归树之间的对应关系，容易混淆递归的“递”与“归”。
    *   传统静态图示或代码讲解无法提供直观、可操控的逐步演示。
4.  **期望**：通过一个可视化、可交互、可控制节奏的动画，将算法执行的“时间过程”和“空间结构”（递归树）同步展现，从而建立深刻的理解。

#### 教学设计思路
本动画设计遵循“从具体到抽象，从单步到整体”的认知规律。

1.  **核心概念分解**：
    *   **分治**：展示如何选取基准值（pivot），将原数组划分为“左（小于pivot）”、“基准”、“右（大于pivot）”三个部分。
    *   **左右指针法**：可视化左右指针（`i`, `j`）的相向移动、比较与交换过程，这是“分”的具体实现。
    *   **递归**：展示对左右两个子数组进行相同的操作，并强调这是“相同的逻辑作用于更小的问题”。
    *   **递归树**：将每一次递归调用表示为树的一个节点，直观展示递归的层次、问题规模的分裂与合并，将时间上的执行过程映射为空间上的树形结构。

2.  **认知流程设计**：
    *   **阶段一（微观操作）**：聚焦于当前待排序数组段，高亮显示pivot、左右指针。用户通过单步执行，观察指针移动、比较和交换的细节。
    *   **阶段二（宏观分治）**：在一次划分完成后，视觉上清晰地将数组分成三个区域（用不同颜色或分隔线），并展示即将对左右两个子数组发起递归调用。
    *   **阶段三（递归展开）**：当递归调用发生时，动画视角切换到“递归树”视图。新的树节点（代表新的递归调用）从父节点生长出来，同时下方对应的数组段被激活。这建立了“代码调用”与“树形结构”的直观联系。
    *   **阶段四（递归回溯）**：当某个子数组排序完成（节点变为叶子），动画显示递归返回，递归树中该节点标记为完成，视角回溯到父节点，继续未完成的操作。体现“归”的过程。

3.  **交互设计**：
    *   **双视图联动**：主视图（数组排序过程）与侧视图/下方视图（递归树生长过程）同步更新。
    *   **节奏控制**：提供“播放/暂停”、“下一步”、“上一步”、“重置”按钮，让用户能自主控制学习节奏。
    *   **关键信息提示**：在交互过程中，通过文字标签实时说明当前步骤（如“比较 `array[j]` 与 pivot”、“交换 `array[i]` 和 `array[j]`”、“递归调用左子数组”）。
    *   **可配置输入**：允许用户输入自定义的初始数组数据，观察不同情况下的排序过程。

4.  **视觉呈现**：
    *   **数组可视化**：用等宽、带标签（索引和值）的矩形条表示数组元素。不同状态用颜色区分：未处理（中性色）、pivot（突出色，如橙色）、左指针（绿色）、右指针（红色）、已交换/已就位元素（浅蓝色）。
    *   **指针与箭头**：用清晰的箭头或带标签的圆圈表示 `i` 和 `j` 指针，并随步骤移动。
    *   **递归树可视化**：采用横向或纵向树状图。每个节点显示其处理的数组区间（如 `[0, 5]`）和当前状态（进行中/已完成）。用连接线表示调用关系。当前活跃的节点和对应的数组段应高亮同步。
    *   **空间划分**：一次划分完成后，在数组中用垂直线或背景色块区分左子数组、pivot、右子数组。

#### 配色方案选择
选择对比清晰、符合认知习惯且舒适的配色，避免过多鲜艳颜色造成干扰。
*   **主色调**：深蓝灰色 (`#2c3e50`) 作为背景或边框，营造专注感。
*   **数组元素**：
    *   默认/未排序：浅灰色 (`#ecf0f1`) 填充，深灰色 (`#7f8c8d`) 边框。
    *   **Pivot元素**：醒目的橙色 (`#e67e22`)。
    *   **左指针 `i`**：绿色 (`#2ecc71`)。
    *   **右指针 `j`**：红色 (`#e74c3c`)。
    *   **已确定位置元素**：柔和的蓝色 (`#3498db`)。
*   **递归树**：
    *   节点边框：深灰色 (`#34495e`)。
    *   节点背景（默认）：白色 (`#fff`)。
    *   节点背景（活跃中）：淡黄色 (`#fcf3cf`)。
    *   节点背景（已完成）：淡绿色 (`#d5f4e6`)。
    *   连接线：灰色 (`#bdc3c7`)。
*   **界面控件**：使用蓝色 (`#3498db`) 表示主要动作（如播放、下一步），灰色 (`#95a5a6`) 表示次要/重置动作。
*   **文本与提示**：深色文本 (`#2c3e50`) 在浅色背景上，关键信息可用加粗或强调色。

#### 交互功能列表
1.  **数据输入区**：文本框或随机生成按钮，用于设置初始待排序数组。
2.  **动画控制区**：
    *   `播放 / 暂停`：连续自动执行算法。
    *   `下一步`：手动执行一个原子步骤（如一次比较、一次交换、一次递归调用）。
    *   `上一步`：回退到上一个状态，便于回顾。
    *   `重置`：恢复到初始状态。
    *   `速度调节滑块`：控制自动播放的速度。
3.  **双视图显示区**：
    *   **主视图 (排序过程视图)**：动态显示数组、指针、交换动作和分区结果。
    *   **副视图 (递归树视图)**：动态生长和更新的递归树，与主视图步骤同步。
4.  **状态信息提示区**：实时显示当前步骤的文本描述（例如：“选取最后一个元素 ‘8’ 作为基准 (pivot)”，“移动右指针 j，寻找小于 pivot 的元素”）。
5.  **代码高亮区（可选但推荐）**：显示简化的快速排序伪代码或关键代码，并高亮当前执行到的行，建立动画与代码的对应关系。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>快速排序分治递归过程可视化</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #2c3e50;
            line-height: 1.6;
            padding: 20px;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #3498db;
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
            flex-direction: column;
            gap: 30px;
        }
        
        .control-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            align-items: center;
        }
        
        .input-section {
            display: flex;
            align-items: center;
            gap: 10px;
            flex: 1;
            min-width: 300px;
        }
        
        .input-section label {
            font-weight: 600;
            color: #2c3e50;
        }
        
        #arrayInput {
            flex: 1;
            padding: 10px 15px;
            border: 2px solid #bdc3c7;
            border-radius: 6px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        #arrayInput:focus {
            outline: none;
            border-color: #3498db;
        }
        
        .button {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
            font-size: 1rem;
        }
        
        .button-primary {
            background-color: #3498db;
            color: white;
        }
        
        .button-primary:hover {
            background-color: #2980b9;
        }
        
        .button-secondary {
            background-color: #95a5a6;
            color: white;
        }
        
        .button-secondary:hover {
            background-color: #7f8c8d;
        }
        
        .button-success {
            background-color: #2ecc71;
            color: white;
        }
        
        .button-success:hover {
            background-color: #27ae60;
        }
        
        .button-warning {
            background-color: #e67e22;
            color: white;
        }
        
        .button-warning:hover {
            background-color: #d35400;
        }
        
        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-left: auto;
        }
        
        .speed-control label {
            font-weight: 600;
            color: #2c3e50;
        }
        
        #speedSlider {
            width: 150px;
        }
        
        .visualization-container {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        
        .main-view {
            background-color: white;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .view-title {
            font-size: 1.4rem;
            margin-bottom: 20px;
            color: #2c3e50;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .view-title::before {
            content: "";
            display: inline-block;
            width: 8px;
            height: 25px;
            background-color: #3498db;
            border-radius: 4px;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 300px;
            border: 1px solid #ecf0f1;
            border-radius: 8px;
            overflow: hidden;
        }
        
        #arrayCanvas {
            width: 100%;
            height: 100%;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #ecf0f1;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }
        
        .recursive-tree-view {
            background-color: white;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        #treeCanvas {
            width: 100%;
            height: 300px;
            border: 1px solid #ecf0f1;
            border-radius: 8px;
        }
        
        .status-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .status-title {
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: #2c3e50;
        }
        
        #statusText {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 6px;
            min-height: 60px;
            border-left: 4px solid #3498db;
            font-size: 1.05rem;
            line-height: 1.5;
        }
        
        .code-panel {
            background-color: white;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .code-container {
            background-color: #2c3e50;
            color: #ecf0f1;
            padding: 20px;
            border-radius: 8px;
            overflow-x: auto;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 0.95rem;
            line-height: 1.5;
        }
        
        .code-line {
            margin-bottom: 5px;
            padding: 2px 5px;
            border-radius: 3px;
            transition: background-color 0.3s;
        }
        
        .code-line.highlighted {
            background-color: #34495e;
            color: #fcf3cf;
            font-weight: 600;
        }
        
        .code-keyword {
            color: #3498db;
        }
        
        .code-function {
            color: #2ecc71;
        }
        
        .code-comment {
            color: #7f8c8d;
        }
        
        .code-variable {
            color: #e74c3c;
        }
        
        .footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            color: #7f8c8d;
            font-size: 0.9rem;
            border-top: 1px solid #ecf0f1;
        }
        
        @media (max-width: 768px) {
            .control-panel {
                flex-direction: column;
                align-items: stretch;
            }
            
            .speed-control {
                margin-left: 0;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>快速排序分治递归过程可视化</h1>
        <p class="subtitle">左右指针交换法 + 递归树动态生成</p>
    </div>
    
    <div class="container">
        <div class="control-panel">
            <div class="input-section">
                <label for="arrayInput">数组数据:</label>
                <input type="text" id="arrayInput" value="6, 3, 8, 5, 2, 7, 4, 1">
                <button id="randomBtn" class="button button-secondary">随机生成</button>
            </div>
            
            <div class="button-group">
                <button id="resetBtn" class="button button-secondary">重置</button>
                <button id="prevBtn" class="button button-secondary">上一步</button>
                <button id="nextBtn" class="button button-primary">下一步</button>
                <button id="playBtn" class="button button-success">播放</button>
                <button id="fastBtn" class="button button-warning">快速排序</button>
            </div>
            
            <div class="speed-control">
                <label for="speedSlider">速度:</label>
                <input type="range" id="speedSlider" min="1" max="10" value="5">
            </div>
        </div>
        
        <div class="visualization-container">
            <div class="main-view">
                <h2 class="view-title">数组排序过程</h2>
                <div class="canvas-container">
                    <canvas id="arrayCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e67e22;"></div>
                        <span>基准值 (Pivot)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2ecc71;"></div>
                        <span>左指针 (i)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span>右指针 (j)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #3498db;"></div>
                        <span>已确定位置</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ecf0f1; border: 1px solid #7f8c8d;"></div>
                        <span>未处理</span>
                    </div>
                </div>
            </div>
            
            <div class="recursive-tree-view">
                <h2 class="view-title">递归树生长过程</h2>
                <canvas id="treeCanvas"></canvas>
            </div>
        </div>
        
        <div class="status-panel">
            <h3 class="status-title">当前状态</h3>
            <div id="statusText">点击"下一步"开始快速排序可视化演示。首先将选取基准值(pivot)，然后使用左右指针法进行分区。</div>
        </div>
        
        <div class="code-panel">
            <h2 class="view-title">算法代码</h2>
            <div class="code-container">
                <div id="codeLine1" class="code-line"><span class="code-keyword">function</span> <span class="code-function">quickSort</span>(arr, left, right) {</div>
                <div id="codeLine2" class="code-line">  <span class="code-keyword">if</span> (left &lt; right) {</div>
                <div id="codeLine3" class="code-line">    <span class="code-keyword">let</span> <span class="code-variable">pivotIndex</span> = <span class="code-function">partition</span>(arr, left, right); <span class="code-comment">// 分区操作</span></div>
                <div id="codeLine4" class="code-line">    <span class="code-function">quickSort</span>(arr, left, <span class="code-variable">pivotIndex</span> - 1); <span class="code-comment">// 递归排序左子数组</span></div>
                <div id="codeLine5" class="code-line">    <span class="code-function">quickSort</span>(arr, <span class="code-variable">pivotIndex</span> + 1, right); <span class="code-comment">// 递归排序右子数组</span></div>
                <div id="codeLine6" class="code-line">  }</div>
                <div id="codeLine7" class="code-line">}</div>
                <div id="codeLine8" class="code-line"></div>
                <div id="codeLine9" class="code-line"><span class="code-keyword">function</span> <span class="code-function">partition</span>(arr, left, right) {</div>
                <div id="codeLine10" class="code-line">  <span class="code-keyword">let</span> <span class="code-variable">pivot</span> = arr[right]; <span class="code-comment">// 选择最右元素作为基准值</span></div>
                <div id="codeLine11" class="code-line">  <span class="code-keyword">let</span> <span class="code-variable">i</span> = left - 1; <span class="code-comment">// 左指针初始化</span></div>
                <div id="codeLine12" class="code-line">  </div>
                <div id="codeLine13" class="code-line">  <span class="code-keyword">for</span> (<span class="code-keyword">let</span> <span class="code-variable">j</span> = left; <span class="code-variable">j</span> &lt; right; <span class="code-variable">j</span>++) {</div>
                <div id="codeLine14" class="code-line">    <span class="code-keyword">if</span> (arr[<span class="code-variable">j</span>] &lt; <span class="code-variable">pivot</span>) { <span class="code-comment">// 当前元素小于基准值</span></div>
                <div id="codeLine15" class="code-line">      <span class="code-variable">i</span>++; <span class="code-comment">// 左指针右移</span></div>
                <div id="codeLine16" class="code-line">      <span class="code-function">swap</span>(arr, <span class="code-variable">i</span>, <span class="code-variable">j</span>); <span class="code-comment">// 交换元素</span></div>
                <div id="codeLine17" class="code-line">    }</div>
                <div id="codeLine18" class="code-line">  }</div>
                <div id="codeLine19" class="code-line">  </div>
                <div id="codeLine20" class="code-line">  <span class="code-function">swap</span>(arr, <span class="code-variable">i</span> + 1, right); <span class="code-comment">// 将基准值放到正确位置</span></div>
                <div id="codeLine21" class="code-line">  <span class="code-keyword">return</span> <span class="code-variable">i</span> + 1; <span class="code-comment">// 返回基准值索引</span></div>
                <div id="codeLine22" class="code-line">}</div>
            </div>
        </div>
    </div>
    
    <div class="footer">
        <p>快速排序可视化教学动画 | 设计：熊猫老师 | 使用HTML5 Canvas实现</p>
    </div>

    <script>
        // 全局变量
        let originalArray = [];
        let currentArray = [];
        let animationSteps = [];
        let currentStep = 0;
        let isPlaying = false;
        let playInterval;
        let speed = 500;
        
        // 状态历史记录，用于实现"上一步"功能
        let stateHistory = [];
        
        // 递归树节点
        class TreeNode {
            constructor(left, right, pivotIndex, depth, parent = null) {
                this.left = left;
                this.right = right;
                this.pivotIndex = pivotIndex;
                this.depth = depth;
                this.parent = parent;
                this.children = [];
                this.isActive = false;
                this.isCompleted = false;
                this.isCurrentPartition = false;
            }
        }
        
        let treeRoot = null;
        let currentNode = null;
        
        // 动画步骤类型
        const StepType = {
            INIT: 'init',
            SELECT_PIVOT: 'select_pivot',
            COMPARE: 'compare',
            SWAP: 'swap',
            MOVE_POINTER: 'move_pointer',
            PARTITION_COMPLETE: 'partition_complete',
            RECURSIVE_CALL_LEFT: 'recursive_call_left',
            RECURSIVE_CALL_RIGHT: 'recursive_call_right',
            RETURN_FROM_RECURSION: 'return_from_recursion',
            SORT_COMPLETE: 'sort_complete'
        };
        
        // DOM元素
        const arrayCanvas = document.getElementById('arrayCanvas');
        const treeCanvas = document.getElementById('treeCanvas');
        const arrayCtx = arrayCanvas.getContext('2d');
        const treeCtx = treeCanvas.getContext('2d');
        const arrayInput = document.getElementById('arrayInput');
        const randomBtn = document.getElementById('randomBtn');
        const resetBtn = document.getElementById('resetBtn');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const playBtn = document.getElementById('playBtn');
        const fastBtn = document.getElementById('fastBtn');
        const speedSlider = document.getElementById('speedSlider');
        const statusText = document.getElementById('statusText');
        
        // 初始化Canvas尺寸
        function initCanvasSize() {
            const arrayContainer = arrayCanvas.parentElement;
            arrayCanvas.width = arrayContainer.clientWidth;
            arrayCanvas.height = arrayContainer.clientHeight;
            
            treeCanvas.width = treeCanvas.parentElement.clientWidth;
            treeCanvas.height = 300;
        }
        
        // 初始化数组
        function initArray() {
            const input = arrayInput.value.trim();
            if (input === '') {
                originalArray = [6, 3, 8, 5, 2, 7, 4, 1];
            } else {
                originalArray = input.split(',').map(num => parseInt(num.trim())).filter(num => !isNaN(num));
                if (originalArray.length === 0) {
                    originalArray = [6, 3, 8, 5, 2, 7, 4, 1];
                }
            }
            
            currentArray = [...originalArray];
            animationSteps = [];
            currentStep = 0;
            stateHistory = [];
            treeRoot = null;
            currentNode = null;
            
            // 生成动画步骤
            generateAnimationSteps(0, originalArray.length - 1, null);
            
            // 保存初始状态
            saveState();
            
            // 更新UI
            updateStatus("已初始化数组。点击'下一步'开始快速排序演示。");
            updateCodeHighlight(-1);
            drawArray();
            drawTree();
        }
        
        // 生成随机数组
        function generateRandomArray() {
            const length = Math.floor(Math.random() * 8) + 5; // 5到12个元素
            const arr = [];
            for (let i = 0; i < length; i++) {
                arr.push(Math.floor(Math.random() * 20) + 1);
            }
            arrayInput.value = arr.join(', ');
            initArray();
        }
        
        // 生成动画步骤
        function generateAnimationSteps(left, right, parentNode) {
            if (left >= right) return;
            
            // 创建树节点
            const node = new TreeNode(left, right, -1, parentNode ? parentNode.depth + 1 : 0, parentNode);
            if (!treeRoot) {
                treeRoot = node;
            }
            if (parentNode) {
                parentNode.children.push(node);
            }
            currentNode = node;
            
            // 记录递归调用开始
            animationSteps.push({
                type: StepType.RECURSIVE_CALL_LEFT,
                left: left,
                right: right,
                node: node
            });
            
            // 选择基准值
            animationSteps.push({
                type: StepType.SELECT_PIVOT,
                left: left,
                right: right,
                pivotIndex: right,
                pivotValue: currentArray[right],
                node: node
            });
            
            // 初始化指针
            let i = left - 1;
            animationSteps.push({
                type: StepType.MOVE_POINTER,
                pointer: 'i',
                index: i,
                left: left,
                right: right,
                node: node
            });
            
            // 分区过程
            for (let j = left; j < right; j++) {
                animationSteps.push({
                    type: StepType.COMPARE,
                    left: left,
                    right: right,
                    i: i,
                    j: j,
                    pivotValue: currentArray[right],
                    node: node
                });
                
                if (currentArray[j] < currentArray[right]) {
                    i++;
                    animationSteps.push({
                        type: StepType.MOVE_POINTER,
                        pointer: 'i',
                        index: i,
                        left: left,
                        right: right,
                        node: node
                    });
                    
                    if (i !== j) {
                        // 交换元素
                        [currentArray[i], currentArray[j]] = [currentArray[j], currentArray[i]];
                        animationSteps.push({
                            type: StepType.SWAP,
                            left: left,
                            right: right,
                            i: i,
                            j: j,
                            node: node
                        });
                    }
                }
            }
            
            // 将基准值放到正确位置
            const pivotIndex = i + 1;
            [currentArray[pivotIndex], currentArray[right]] = [currentArray[right], currentArray[pivotIndex]];
            animationSteps.push({
                type: StepType.SWAP,
                left: left,
                right: right,
                i: pivotIndex,
                j: right,
                node: node
            });
            
            // 更新节点的pivotIndex
            node.pivotIndex = pivotIndex;
            
            // 分区完成
            animationSteps.push({
                type: StepType.PARTITION_COMPLETE,
                left: left,
                right: right,
                pivotIndex: pivotIndex,
                node: node
            });
            
            // 递归调用左子数组
            if (left < pivotIndex - 1) {
                generateAnimationSteps(left, pivotIndex - 1, node);
            }
            
            // 记录从左子数组返回
            animationSteps.push({
                type: StepType.RETURN_FROM_RECURSION,
                node: node
            });
            
            // 递归调用右子数组
            if (pivotIndex + 1 < right) {
                animationSteps.push({
                    type: StepType.RECURSIVE_CALL_RIGHT,
                    left: left,
                    right: right,
                    node: node
                });
                
                generateAnimationSteps(pivotIndex + 1, right, node);
                
                // 记录从右子数组返回
                animationSteps.push({
                    type: StepType.RETURN_FROM_RECURSION,
                    node: node
                });
            }
            
            // 当前节点排序完成
            animationSteps.push({
                type: StepType.SORT_COMPLETE,
                left: left,
                right: right,
                node: node
            });
        }
        
        // 保存当前状态到历史记录
        function saveState() {
            stateHistory.push({
                array: [...currentArray],
                step: currentStep,
                currentNode: currentNode
            });
        }
        
        // 执行下一步
        function nextStep() {
            if (currentStep >= animationSteps.length) {
                updateStatus("排序已完成！");
                if (isPlaying) {
                    togglePlay();
                }
                return;
            }
            
            saveState();
            
            const step = animationSteps[currentStep];
            executeStep(step);
            currentStep++;
            
            // 更新UI
            drawArray();
            drawTree();
            updateCodeHighlightForStep(step);
            
            if (currentStep >= animationSteps.length) {
                updateStatus("排序已完成！数组已完全排序。");
                if (isPlaying) {
                    togglePlay();
                }
            }
        }
        
        // 执行上一步
        function prevStep() {
            if (stateHistory.length <= 1) return;
            
            // 移除当前状态
            stateHistory.pop();
            
            // 恢复到上一个状态
            const prevState = stateHistory[stateHistory.length - 1];
            currentArray = [...prevState.array];
            currentStep = prevState.step;
            currentNode = prevState.currentNode;
            
            // 更新UI
            drawArray();
            drawTree();
            
            if (currentStep > 0) {
                const step = animationSteps[currentStep - 1];
                updateStatusForStep(step);
                updateCodeHighlightForStep(step);
            } else {
                updateStatus("已回到初始状态。");
                updateCodeHighlight(-1);
            }
        }
        
        // 执行步骤
        function executeStep(step) {
            // 更新当前节点状态
            if (step.node) {
                // 重置所有节点的活动状态
                resetNodeActivity(treeRoot);
                
                step.node.isActive = true;
                currentNode = step.node;
                
                if (step.type === StepType.SORT_COMPLETE) {
                    step.node.isCompleted = true;
                }
                
                if (step.type === StepType.PARTITION_COMPLETE) {
                    step.node.isCurrentPartition = true;
                } else if (step.type === StepType.RECURSIVE_CALL_LEFT || step.type === StepType.RECURSIVE_CALL_RIGHT) {
                    step.node.isCurrentPartition = false;
                }
            }
            
            // 更新状态文本
            updateStatusForStep(step);
        }
        
        // 重置节点活动状态
        function resetNodeActivity(node) {
            if (!node) return;
            
            node.isActive = false;
            for (const child of node.children) {
                resetNodeActivity(child);
            }
        }
        
        // 更新状态文本
        function updateStatusForStep(step) {
            let status = "";
            
            switch (step.type) {
                case StepType.INIT:
                    status = "初始化数组，准备开始快速排序。";
                    break;
                case StepType.SELECT_PIVOT:
                    status = `选择基准值(pivot): 选取区间[${step.left}, ${step.right}]的最右元素 ${step.pivotValue} 作为基准值。`;
                    break;
                case StepType.COMPARE:
                    status = `比较: 当前元素 arr[${step.j}] = ${currentArray[step.j]} 与基准值 ${step.pivotValue} 比较。`;
                    if (currentArray[step.j] < step.pivotValue) {
                        status += ` ${currentArray[step.j]} < ${step.pivotValue}，需要交换。`;
                    } else {
                        status += ` ${currentArray[step.j]} >= ${step.pivotValue}，继续移动右指针。`;
                    }
                    break;
                case StepType.SWAP:
                    if (step.j === step.right) {
                        status = `交换: 将基准值放到正确位置 arr[${step.i}]。现在基准值 ${currentArray[step.i]} 已位于最终排序位置。`;
                    } else {
                        status = `交换: 交换 arr[${step.i}] = ${currentArray[step.i]} 和 arr[${step.j}] = ${currentArray[step.j]}。`;
                    }
                    break;
                case StepType.MOVE_POINTER:
                    if (step.pointer === 'i') {
                        status = `移动左指针: i = ${step.index}`;
                    } else {
                        status = `移动右指针: j = ${step.index}`;
                    }
                    break;
                case StepType.PARTITION_COMPLETE:
                    status = `分区完成: 区间[${step.left}, ${step.right}]已分区。基准值位于索引 ${step.pivotIndex}。左子数组: [${step.left}, ${step.pivotIndex-1}]，右子数组: [${step.pivotIndex+1}, ${step.right}]。`;
                    break;
                case StepType.RECURSIVE_CALL_LEFT:
                    status = `递归调用: 对左子数组 [${step.left}, ${step.node.pivotIndex-1}] 进行快速排序。`;
                    break;
                case StepType.RECURSIVE_CALL_RIGHT:
                    status = `递归调用: 对右子数组 [${step.node.pivotIndex+1}, ${step.right}] 进行快速排序。`;
                    break;
                case StepType.RETURN_FROM_RECURSION:
                    status = `递归返回: 子数组排序完成，返回到上一层递归。`;
                    break;
                case StepType.SORT_COMPLETE:
                    status = `排序完成: 区间[${step.left}, ${step.right}]已完全排序。`;
                    break;
                default:
                    status = "执行快速排序步骤...";
            }
            
            updateStatus(status);
        }
        
        // 更新状态文本
        function updateStatus(text) {
            statusText.textContent = text;
        }
        
        // 更新代码高亮
        function updateCodeHighlightForStep(step) {
            // 先清除所有高亮
            for (let i = 1; i <= 22; i++) {
                document.getElementById(`codeLine${i}`).classList.remove('highlighted');
            }
            
            // 根据步骤类型高亮对应代码行
            switch (step.type) {
                case StepType.SELECT_PIVOT:
                    document.getElementById('codeLine10').classList.add('highlighted');
                    break;
                case StepType.MOVE_POINTER:
                    if (step.pointer === 'i' && step.index === step.left - 1) {
                        document.getElementById('codeLine11').classList.add('highlighted');
                    }
                    break;
                case StepType.COMPARE:
                    document.getElementById('codeLine13').classList.add('highlighted');
                    document.getElementById('codeLine14').classList.add('highlighted');
                    break;
                case StepType.SWAP:
                    if (step.j === step.right) {
                        document.getElementById('codeLine20').classList.add('highlighted');
                    } else {
                        document.getElementById('codeLine16').classList.add('highlighted');
                    }
                    break;
                case StepType.PARTITION_COMPLETE:
                    document.getElementById('codeLine21').classList.add('highlighted');
                    break;
                case StepType.RECURSIVE_CALL_LEFT:
                    document.getElementById('codeLine3').classList.add('highlighted');
                    document.getElementById('codeLine4').classList.add('highlighted');
                    break;
                case StepType.RECURSIVE_CALL_RIGHT:
                    document.getElementById('codeLine3').classList.add('highlighted');
                    document.getElementById('codeLine5').classList.add('highlighted');
                    break;
                case StepType.SORT_COMPLETE:
                    document.getElementById('codeLine2').classList.add('highlighted');
                    break;
            }
        }
        
        // 更新代码高亮（通用）
        function updateCodeHighlight(lineNumber) {
            // 先清除所有高亮
            for (let i = 1; i <= 22; i++) {
                document.getElementById(`codeLine${i}`).classList.remove('highlighted');
            }
            
            // 高亮指定行
            if (lineNumber > 0) {
                document.getElementById(`codeLine${lineNumber}`).classList.add('highlighted');
            }
        }
        
        // 绘制数组
        function drawArray() {
            const canvas = arrayCanvas;
            const ctx = arrayCtx;
            const width = canvas.width;
            const height = canvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            if (currentArray.length === 0) return;
            
            // 计算元素宽度和间距
            const elementCount = currentArray.length;
            const maxElement = Math.max(...currentArray);
            const padding = 20;
            const elementWidth = (width - 2 * padding) / elementCount;
            const elementSpacing = 5;
            const actualElementWidth = elementWidth - elementSpacing;
            
            // 绘制每个元素
            for (let i = 0; i < elementCount; i++) {
                const value = currentArray[i];
                const x = padding + i * elementWidth;
                const elementHeight = (value / maxElement) * (height - 100);
                const y = height - 40 - elementHeight;
                
                // 确定元素颜色
                let color = '#ecf0f1'; // 默认颜色
                let borderColor = '#7f8c8d';
                let textColor = '#2c3e50';
                
                // 检查当前步骤以确定高亮
                if (currentStep > 0 && currentStep <= animationSteps.length) {
                    const step = animationSteps[currentStep - 1];
                    
                    // 如果是分区步骤，检查是否在当前分区内
                    if (step.node && step.node.isCurrentPartition && i >= step.node.left && i <= step.node.right) {
                        color = '#fcf3cf'; // 当前分区背景色
                    }
                    
                    // 检查是否是基准值
                    if (step.type === StepType.SELECT_PIVOT && i === step.pivotIndex) {
                        color = '#e67e22'; // 基准值
                        borderColor = '#d35400';
                        textColor = 'white';
                    }
                    
                    // 检查是否是左指针
                    if ((step.type === StepType.COMPARE || step.type === StepType.MOVE_POINTER || step.type === StepType.SWAP) && step.i === i) {
                        color = '#2ecc71'; // 左指针
                        borderColor = '#27ae60';
                        textColor = 'white';
                    }
                    
                    // 检查是否是右指针
                    if ((step.type === StepType.COMPARE || step.type === StepType.MOVE_POINTER || step.type === StepType.SWAP) && step.j === i) {
                        color = '#e74c3c'; // 右指针
                        borderColor = '#c0392b';
                        textColor = 'white';
                    }
                    
                    // 检查是否是已交换元素
                    if (step.type === StepType.SWAP && (step.i === i || step.j === i)) {
                        color = '#3498db'; // 已交换
                        borderColor = '#2980b9';
                        textColor = 'white';
                    }
                    
                    // 检查分区完成后的基准值位置
                    if (step.type === StepType.PARTITION_COMPLETE && i === step.pivotIndex) {
                        color = '#3498db'; // 已确定位置
                        borderColor = '#2980b9';
                        textColor = 'white';
                    }
                }
                
                // 绘制元素矩形
                ctx.fillStyle = color;
                ctx.fillRect(x, y, actualElementWidth, elementHeight);
                ctx.strokeStyle = borderColor;
                ctx.lineWidth = 2;
                ctx.strokeRect(x, y, actualElementWidth, elementHeight);
                
                // 绘制元素值
                ctx.fillStyle = textColor;
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(value, x + actualElementWidth / 2, y - 10);
                
                // 绘制索引
                ctx.fillStyle = '#7f8c8d';
                ctx.font = '14px Arial';
                ctx.fillText(`[${i}]`, x + actualElementWidth / 2, height - 20);
            }
            
            // 如果有当前节点
<!--检测到代码截断，自动续写中...-->
            // 如果有当前节点，绘制分区范围
            if (currentNode && currentNode.isCurrentPartition) {
                const left = currentNode.left;
                const right = currentNode.right;
                
                // 绘制分区背景
                ctx.fillStyle = 'rgba(252, 243, 207, 0.2)';
                const leftX = padding + left * elementWidth;
                const rightX = padding + (right + 1) * elementWidth;
                ctx.fillRect(leftX, 0, rightX - leftX, height);
                
                // 绘制分区标签
                ctx.fillStyle = '#e67e22';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`当前分区: [${left}, ${right}]`, width / 2, 30);
            }
        }
        
        // 绘制递归树
        function drawTree() {
            const canvas = treeCanvas;
            const ctx = treeCtx;
            const width = canvas.width;
            const height = canvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            if (!treeRoot) return;
            
            // 计算树布局
            const nodeWidth = 80;
            const nodeHeight = 40;
            const horizontalSpacing = 40;
            const verticalSpacing = 80;
            
            // 递归绘制树节点
            function drawNode(node, x, y, levelWidth) {
                if (!node) return;
                
                // 确定节点颜色
                let bgColor = '#ffffff';
                let borderColor = '#34495e';
                let textColor = '#2c3e50';
                
                if (node.isActive) {
                    bgColor = '#fcf3cf'; // 活跃节点
                    borderColor = '#e67e22';
                } else if (node.isCompleted) {
                    bgColor = '#d5f4e6'; // 已完成节点
                    borderColor = '#27ae60';
                }
                
                // 绘制节点
                ctx.fillStyle = bgColor;
                ctx.fillRect(x - nodeWidth/2, y - nodeHeight/2, nodeWidth, nodeHeight);
                ctx.strokeStyle = borderColor;
                ctx.lineWidth = 2;
                ctx.strokeRect(x - nodeWidth/2, y - nodeHeight/2, nodeWidth, nodeHeight);
                
                // 绘制节点文本
                ctx.fillStyle = textColor;
                ctx.font = '12px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                
                // 显示节点信息
                let nodeText = `[${node.left}, ${node.right}]`;
                if (node.pivotIndex !== -1) {
                    nodeText += `\npivot: ${node.pivotIndex}`;
                }
                
                const lines = nodeText.split('\n');
                for (let i = 0; i < lines.length; i++) {
                    ctx.fillText(lines[i], x, y - (lines.length-1)*8 + i*16);
                }
                
                // 绘制到子节点的连接线
                if (node.children.length > 0) {
                    const childCount = node.children.length;
                    const childY = y + verticalSpacing;
                    
                    // 计算子节点的水平分布
                    let childXStart;
                    if (childCount === 1) {
                        childXStart = x;
                    } else {
                        const totalWidth = (childCount - 1) * (nodeWidth + horizontalSpacing);
                        childXStart = x - totalWidth / 2;
                    }
                    
                    // 绘制连接线
                    ctx.strokeStyle = '#bdc3c7';
                    ctx.lineWidth = 1;
                    ctx.beginPath();
                    
                    for (let i = 0; i < childCount; i++) {
                        const childX = childXStart + i * (nodeWidth + horizontalSpacing);
                        
                        // 从父节点底部到子节点顶部
                        ctx.moveTo(x, y + nodeHeight/2);
                        ctx.lineTo(childX, childY - nodeHeight/2);
                        
                        // 递归绘制子节点
                        drawNode(node.children[i], childX, childY, nodeWidth + horizontalSpacing);
                    }
                    
                    ctx.stroke();
                }
            }
            
            // 从根节点开始绘制
            drawNode(treeRoot, width / 2, 50, nodeWidth);
            
            // 绘制图例
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'left';
            ctx.fillText('递归树图例:', 20, height - 80);
            
            ctx.font = '12px Arial';
            ctx.fillStyle = '#fcf3cf';
            ctx.fillRect(20, height - 60, 15, 15);
            ctx.strokeStyle = '#e67e22';
            ctx.strokeRect(20, height - 60, 15, 15);
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('当前活跃节点', 40, height - 50);
            
            ctx.fillStyle = '#d5f4e6';
            ctx.fillRect(150, height - 60, 15, 15);
            ctx.strokeStyle = '#27ae60';
            ctx.strokeRect(150, height - 60, 15, 15);
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('已完成节点', 170, height - 50);
            
            ctx.fillStyle = '#ffffff';
            ctx.fillRect(280, height - 60, 15, 15);
            ctx.strokeStyle = '#34495e';
            ctx.strokeRect(280, height - 60, 15, 15);
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('待处理节点', 300, height - 50);
        }
        
        // 切换播放/暂停
        function togglePlay() {
            isPlaying = !isPlaying;
            
            if (isPlaying) {
                playBtn.textContent = '暂停';
                playBtn.classList.remove('button-success');
                playBtn.classList.add('button-secondary');
                
                playInterval = setInterval(() => {
                    nextStep();
                }, speed);
            } else {
                playBtn.textContent = '播放';
                playBtn.classList.remove('button-secondary');
                playBtn.classList.add('button-success');
                
                clearInterval(playInterval);
            }
        }
        
        // 快速完成排序
        function fastSort() {
            if (isPlaying) {
                togglePlay();
            }
            
            // 直接跳到完成
            while (currentStep < animationSteps.length) {
                nextStep();
            }
        }
        
        // 更新速度
        function updateSpeed() {
            speed = 600 - (speedSlider.value * 50);
            
            if (isPlaying) {
                clearInterval(playInterval);
                playInterval = setInterval(() => {
                    nextStep();
                }, speed);
            }
        }
        
        // 事件监听
        window.addEventListener('load', () => {
            initCanvasSize();
            initArray();
            
            // 窗口大小变化时调整Canvas
            window.addEventListener('resize', initCanvasSize);
            
            // 按钮事件
            randomBtn.addEventListener('click', generateRandomArray);
            resetBtn.addEventListener('click', initArray);
            prevBtn.addEventListener('click', prevStep);
            nextBtn.addEventListener('click', nextStep);
            playBtn.addEventListener('click', togglePlay);
            fastBtn.addEventListener('click', fastSort);
            
            // 速度滑块事件
            speedSlider.addEventListener('input', updateSpeed);
            
            // 输入框事件（按Enter键初始化）
            arrayInput.addEventListener('keypress', (e) => {
                if (e.key === 'Enter') {
                    initArray();
                }
            });
        });
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

欢迎使用《快速排序分治递归过程可视化》教学动画！本工具旨在通过直观、交互的方式，帮助您深入理解快速排序算法的核心原理——分治策略与递归过程。无论您是算法初学者还是希望巩固理解的学习者，本动画都将为您提供独特的视觉学习体验。

### 一、功能说明

本动画系统由四个核心模块组成，协同展示快速排序的全过程：

1. **控制面板**：提供数据输入、动画控制与速度调节功能
2. **数组排序视图**：实时可视化数组元素的排序过程，展示指针移动与元素交换
3. **递归树视图**：动态生成递归调用树，展示算法执行的空间结构
4. **状态与代码面板**：同步显示当前步骤说明与对应代码高亮

### 二、主要功能

#### 1. 数据配置
- **自定义数组**：在输入框中输入以逗号分隔的数字（如：`6, 3, 8, 5, 2`）
- **随机生成**：点击“随机生成”按钮，系统将自动创建5-12个元素的随机数组
- **重置功能**：随时返回初始状态，重新开始学习

#### 2. 动画控制
- **单步执行**：使用“下一步”按钮，逐帧观察算法的每个细节操作
- **上一步**：支持回退功能，便于回顾关键步骤
- **连续播放**：点击“播放”按钮，系统将以设定速度自动执行
- **快速完成**：点击“快速排序”按钮，直接观看完整排序过程
- **速度调节**：通过滑块控制动画播放速度（1-10档可调）

#### 3. 可视化特性
- **颜色编码系统**：
  - 🟠 橙色：基准值（Pivot）
  - 🟢 绿色：左指针（i）
  - 🔴 红色：右指针（j）
  - 🔵 蓝色：已确定位置的元素
  - ⬜ 浅灰色：未处理的元素
  - 🟡 淡黄色：当前活跃的递归节点
  - 🟢 淡绿色：已完成的递归节点

- **双视图联动**：
  - 数组视图中的每一步操作，都会在递归树视图中同步反映
  - 当前处理的数组区间与递归树节点实时对应

### 三、设计特色

#### 1. 认知友好的教学设计
- **从微观到宏观**：先展示指针移动、元素交换的细节，再呈现分区结果，最后展示递归调用
- **时间与空间同步**：将算法的时间执行过程（数组排序）与空间结构（递归树）同时可视化
- **抽象概念具体化**：将“分治”、“递归”等抽象概念转化为直观的视觉元素

#### 2. 专业的技术实现
- **完整的算法模拟**：严格遵循快速排序（左右指针法）的标准实现
- **状态历史记录**：支持完整的“上一步”功能，便于回溯学习
- **响应式设计**：适配不同屏幕尺寸，确保最佳观看体验

#### 3. 教学辅助功能
- **实时状态提示**：每一步都有详细的文字说明，解释当前操作的意义
- **代码高亮同步**：算法代码与动画步骤实时对应，建立理论与实践的连接
- **递归树动态生长**：直观展示递归调用的层次结构与返回过程

### 四、教学要点

#### 快速排序核心概念可视化

1. **分区过程（Partition）**
   - 观察如何选择基准值（通常是最右元素）
   - 理解左右指针如何相向移动、比较和交换
   - 掌握“小于基准值的元素在左，大于的在右”的分区原则

2. **分治策略（Divide and Conquer）**
   - 观看原数组如何被基准值分成两个子问题
   - 理解“分而治之”的思想：大问题分解为小问题，小问题独立解决

3. **递归过程（Recursion）**
   - 通过递归树观察递归调用的层次结构
   - 理解递归的“递”（向下调用）与“归”（向上返回）两个阶段
   - 观察递归基（base case）的条件：当子数组长度为0或1时停止递归

4. **算法复杂度直观理解**
   - 观察递归树的深度与平衡性，理解最好/最坏情况的时间复杂度
   - 通过交换次数直观感受算法的效率

### 五、使用建议

#### 学习路径推荐

**第一阶段：熟悉界面与基本操作**
1. 使用默认数组 `[6, 3, 8, 5, 2, 7, 4, 1]` 开始学习
2. 点击“下一步”按钮，逐帧观察每个操作
3. 注意观察颜色变化与状态提示文字

**第二阶段：深入理解分区过程**
1. 重点关注指针 `i` 和 `j` 的移动规则
2. 观察元素交换的条件与结果
3. 理解基准值最终位置的确定过程

**第三阶段：掌握递归调用**
1. 切换注意力到递归树视图
2. 观察新节点的创建时机（递归调用）
3. 注意节点的颜色变化（活跃→完成）
4. 理解递归返回的过程

**第四阶段：探索不同情况**
1. 尝试已排序数组 `[1, 2, 3, 4, 5]`，观察最坏情况
2. 尝试随机数组，观察平均情况
3. 尝试有重复元素的数组

#### 教学场景应用

**个人自学**：
- 建议先观看一遍完整动画，了解整体流程
- 然后使用单步模式，仔细研究每个步骤
- 尝试预测下一步操作，检验自己的理解

**课堂教学**：
- 教师可在大屏幕上演示，讲解关键步骤
- 学生可在个人设备上同步操作，加深理解
- 可设计思考题：如“如果选择第一个元素作为基准值，动画会有何不同？”

**复习巩固**：
- 使用“上一步”功能回顾难点步骤
- 关闭状态提示，尝试自己解释当前操作
- 对照代码面板，理解算法实现细节

#### 高级学习技巧

1. **对比学习**：观察不同输入数据下递归树的形状差异
2. **性能分析**：计数交换次数，直观感受算法效率
3. **算法变体思考**：基于可视化理解，思考如何优化（如三数取中法选择基准值）
4. **迁移应用**：尝试将分治递归的思想应用到其他算法学习中

---

**温馨提示**：算法学习如同登山，每一步都需踏实。本工具是您的视觉登山杖，帮助您看清路径、理解地形。当您能够闭上眼睛也能想象出快速排序的完整过程时，您就真正掌握了这一经典算法！

祝您学习愉快，探索成功！如有任何问题或建议，欢迎反馈。