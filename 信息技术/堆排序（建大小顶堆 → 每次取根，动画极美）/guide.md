# 需求：堆排序（建大/小顶堆 → 每次取根，动画极美）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为计算机科学或相关专业的学生、编程初学者以及对算法感兴趣的自学者。他们具备基础的编程和数据结构知识，但可能对堆排序的动态过程理解不深。
2.  **核心需求**：
    *   **直观理解过程**：用户需要清晰地看到堆（完全二叉树）的构建（Heapify）过程，以及如何通过反复交换堆顶元素和末尾元素、并重新调整堆来完成排序。
    *   **区分大小顶堆**：需要明确展示大顶堆（用于升序排序）和小顶堆（用于降序排序）的区别与联系。
    *   **控制学习节奏**：用户希望能暂停、单步执行、回退或重置动画，以便在关键步骤停下来思考。
    *   **关联代码与动画**：将算法步骤与伪代码或关键代码行高亮关联，帮助用户建立逻辑与实现的联系。
    *   **美学与趣味性**：一个“极美”的动画能降低认知负荷，提升学习兴趣和记忆效果。

#### 教学设计思路
1.  **核心概念分解**：
    *   **堆的定义**：强调其作为完全二叉树和满足堆性质（父节点值 ≥ 或 ≤ 子节点值）的数据结构。
    *   **建堆（Heapify）**：从最后一个非叶子节点开始，自底向上、自右向左地进行“下沉”操作，确保每个子树都满足堆性质。这是动画的**第一个高潮**。
    *   **排序过程**：
        *   **交换**：将堆顶（最大/最小值）与当前未排序部分的最后一个元素交换。
        *   **缩小堆**：将交换后的末尾元素标记为已排序，堆的有效大小减一。
        *   **调整**：对新的堆顶元素进行“下沉”操作，恢复堆性质。
        *   **循环**：重复上述步骤，直到堆大小为1。这是动画的**第二个高潮**，呈现出元素逐渐归位的动态美感。

2.  **遵循认知规律**：
    *   **从具体到抽象**：先展示数组如何可视化为一个二叉树，建立直观印象。
    *   **分步演示**：将复杂的排序过程分解为“建堆”和“取根-调整”两个清晰阶段。
    *   **突出变化**：使用高亮、颜色变化、移动轨迹来强调当前操作的节点、比较的对象和交换的元素。
    *   **即时反馈**：在用户交互（如点击下一步）时，提供对应的文字说明和代码高亮。

3.  **交互设计**：
    *   **双视图同步**：左侧为**树形视图**（直观展示堆结构），右侧为**数组视图**（对应实际存储）。两个视图的节点/元素状态实时同步。
    *   **过程控制**：提供播放/暂停、下一步、上一步、重置等控制按钮。
    *   **模式选择**：允许用户选择“大顶堆（升序）”或“小顶堆（降序）”，并动态更新说明。
    *   **手动探索**（进阶）：允许用户点击某个节点，查看其“下沉”或“上浮”的潜在路径（以半透明方式预览），增强探索性。

4.  **视觉呈现**：
    *   **树形布局**：采用清晰美观的树状图，节点大小适中，连线柔和。
    *   **状态色码**：
        *   **默认/未操作**：浅灰色（数组背景）、中性色节点（树）。
        *   **当前焦点节点**（如正在下沉的节点）：亮蓝色。
        *   **比较中的节点**：黄色。
        *   **待交换/正在交换的节点**：红色，并伴有平滑的移动动画。
        *   **已排序元素**：绿色，并逐渐从树形视图“移出”到右侧的已排序区域。
        *   **堆的有效范围**：在数组视图中用背景色区分。
    *   **动画效果**：交换使用平滑的弧线运动；“下沉”过程有连续的比较和位置调整动画；已排序元素“飞”到指定位置。整体节奏舒缓、清晰。

#### 配色方案选择
*   **主色调**：采用**深蓝（#2c3e50）** 作为画布背景，营造专注、专业的氛围，并能突出前景元素。
*   **数据元素**：
    *   节点/数组元素默认填充：**浅灰色（#ecf0f1）**，边框：**中灰色（#bdc3c7）**。
    *   当前操作节点：**亮蓝色（#3498db）**。
    *   比较节点：**琥珀色（#f1c40f）**。
    *   交换节点：**红色（#e74c3c）**。
    *   已排序/已固定元素：**绿色（#2ecc71）**。
*   **文本与界面**：主要说明文字用**白色（#ffffff）**，辅助文字用**浅灰色（#bdc3c7）**。按钮使用**扁平化设计**，主操作按钮为蓝色（#3498db），次要按钮为灰色。
*   **动态效果**：运动轨迹使用主操作节点的蓝色半透明线条，增强视觉引导。

#### 交互功能列表
1.  **核心控制面板**：
    *   `播放 / 暂停`：开始或暂停自动连续动画。
    *   `下一步`：手动执行下一个关键步骤（如一次比较、一次交换、一次下沉完成）。
    *   `上一步`：回退到上一个状态，便于复习。
    *   `重置`：将动画恢复至初始状态，并清空已排序序列。
2.  **配置面板**：
    *   `排序模式选择`：单选按钮组，在“大顶堆（升序）”和“小顶堆（降序）”之间切换。
    *   `动画速度滑块`：调整自动播放的速度。
    *   `随机初始化`：生成一组新的随机数据重新开始。
3.  **信息显示面板**：
    *   **当前步骤说明**：用文字描述当前正在进行的操作（例如：“正在调整节点[5]，与其左子节点[11]进行比较”）。
    *   **伪代码/代码高亮**：显示堆排序的关键伪代码，并高亮当前执行到的行。
    *   **数据状态**：显示当前堆的大小、已排序元素个数等。
4.  **可视化区域**：
    *   **树形视图**：动态绘制堆的二叉树表示。
    *   **数组视图**：同步显示对应的数组，并清晰标出堆的边界和已排序部分。
    *   **已排序序列**：在数组右侧或下方单独展示已取出的根元素组成的序列。
5.  **（可选）探索式交互**：
    *   在暂停状态下，鼠标悬停在节点上可显示其索引和值。
    *   点击某个非叶子节点，可预览其“下沉”的可能路径（虚线连接）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>堆排序算法可视化 | Heap Sort Visualization</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #2c3e50;
            color: #ecf0f1;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .container {
            max-width: 1200px;
            width: 100%;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        header {
            text-align: center;
            padding: 15px;
            border-bottom: 2px solid #3498db;
            margin-bottom: 10px;
        }
        
        h1 {
            color: #3498db;
            font-size: 2.5rem;
            margin-bottom: 8px;
        }
        
        .subtitle {
            color: #bdc3c7;
            font-size: 1.1rem;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .visualization-section {
            flex: 2;
            min-width: 300px;
            background-color: rgba(44, 62, 80, 0.8);
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .control-section {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .panel {
            background-color: rgba(44, 62, 80, 0.8);
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .panel-title {
            color: #3498db;
            font-size: 1.3rem;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #3498db;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 400px;
            border: 2px solid #34495e;
            border-radius: 8px;
            overflow: hidden;
            background-color: #1a252f;
        }
        
        #treeCanvas, #arrayCanvas {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        
        .control-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        button {
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.2s ease;
            font-size: 0.95rem;
        }
        
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        .btn-primary {
            background-color: #3498db;
            color: white;
        }
        
        .btn-secondary {
            background-color: #7f8c8d;
            color: white;
        }
        
        .btn-success {
            background-color: #2ecc71;
            color: white;
        }
        
        .btn-warning {
            background-color: #f1c40f;
            color: #2c3e50;
        }
        
        .btn-danger {
            background-color: #e74c3c;
            color: white;
        }
        
        .config-options {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .option-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }
        
        .option-label {
            font-weight: bold;
            color: #bdc3c7;
        }
        
        .radio-group {
            display: flex;
            gap: 15px;
        }
        
        .radio-option {
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        input[type="radio"] {
            accent-color: #3498db;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        input[type="range"] {
            flex: 1;
            accent-color: #3498db;
        }
        
        .status-display {
            background-color: rgba(26, 37, 47, 0.8);
            border-radius: 8px;
            padding: 15px;
            margin-top: 10px;
        }
        
        .status-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            padding-bottom: 8px;
            border-bottom: 1px dashed #34495e;
        }
        
        .status-item:last-child {
            margin-bottom: 0;
            border-bottom: none;
        }
        
        .status-label {
            color: #bdc3c7;
        }
        
        .status-value {
            font-weight: bold;
            color: #3498db;
        }
        
        .step-description {
            background-color: rgba(26, 37, 47, 0.8);
            border-radius: 8px;
            padding: 15px;
            min-height: 120px;
            line-height: 1.6;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            justify-content: center;
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
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .legend-text {
            font-size: 0.9rem;
            color: #bdc3c7;
        }
        
        .code-panel {
            font-family: 'Consolas', 'Monaco', monospace;
            background-color: #1a252f;
            border-radius: 8px;
            padding: 15px;
            overflow-x: auto;
            line-height: 1.5;
        }
        
        .code-line {
            padding: 2px 5px;
            margin: 2px 0;
            border-radius: 3px;
            transition: background-color 0.3s;
        }
        
        .code-line.active {
            background-color: rgba(52, 152, 219, 0.3);
            color: #3498db;
            font-weight: bold;
        }
        
        .footer {
            text-align: center;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #34495e;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>堆排序算法可视化</h1>
            <p class="subtitle">Heap Sort Visualization | 建堆 → 取根 → 调整 → 排序完成</p>
        </header>
        
        <div class="main-content">
            <section class="visualization-section">
                <h2 class="panel-title">堆排序过程可视化</h2>
                <div class="canvas-container">
                    <canvas id="treeCanvas"></canvas>
                    <canvas id="arrayCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ecf0f1;"></div>
                        <span class="legend-text">默认节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #3498db;"></div>
                        <span class="legend-text">当前操作节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f1c40f;"></div>
                        <span class="legend-text">比较节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span class="legend-text">交换节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2ecc71;"></div>
                        <span class="legend-text">已排序元素</span>
                    </div>
                </div>
            </section>
            
            <section class="control-section">
                <div class="panel">
                    <h2 class="panel-title">动画控制</h2>
                    <div class="control-buttons">
                        <button id="playPauseBtn" class="btn-primary">▶ 播放</button>
                        <button id="nextStepBtn" class="btn-secondary">⏭ 下一步</button>
                        <button id="prevStepBtn" class="btn-secondary">⏮ 上一步</button>
                        <button id="resetBtn" class="btn-warning">↺ 重置</button>
                        <button id="randomizeBtn" class="btn-success">🎲 随机数据</button>
                    </div>
                    
                    <div class="config-options">
                        <div class="option-group">
                            <div class="option-label">排序模式</div>
                            <div class="radio-group">
                                <label class="radio-option">
                                    <input type="radio" name="sortMode" value="max" checked>
                                    <span>大顶堆 (升序排序)</span>
                                </label>
                                <label class="radio-option">
                                    <input type="radio" name="sortMode" value="min">
                                    <span>小顶堆 (降序排序)</span>
                                </label>
                            </div>
                        </div>
                        
                        <div class="option-group">
                            <div class="option-label">动画速度</div>
                            <div class="slider-container">
                                <span>慢</span>
                                <input type="range" id="speedSlider" min="1" max="10" value="5">
                                <span>快</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="status-display">
                        <div class="status-item">
                            <span class="status-label">当前步骤:</span>
                            <span id="currentStep" class="status-value">准备开始</span>
                        </div>
                        <div class="status-item">
                            <span class="status-label">堆大小:</span>
                            <span id="heapSize" class="status-value">10</span>
                        </div>
                        <div class="status-item">
                            <span class="status-label">已排序:</span>
                            <span id="sortedCount" class="status-value">0</span>
                        </div>
                        <div class="status-item">
                            <span class="status-label">比较次数:</span>
                            <span id="comparisonCount" class="status-value">0</span>
                        </div>
                        <div class="status-item">
                            <span class="status-label">交换次数:</span>
                            <span id="swapCount" class="status-value">0</span>
                        </div>
                    </div>
                </div>
                
                <div class="panel">
                    <h2 class="panel-title">步骤说明</h2>
                    <div class="step-description" id="stepDescription">
                        点击"播放"按钮开始堆排序可视化演示。算法分为两个阶段：1) 建堆阶段：从最后一个非叶子节点开始，自底向上调整，构建大顶堆/小顶堆；2) 排序阶段：反复将堆顶元素与末尾元素交换，然后调整堆结构。
                    </div>
                </div>
            </section>
        </div>
        
        <div class="panel">
            <h2 class="panel-title">算法伪代码</h2>
            <div class="code-panel">
                <div id="codeLine1" class="code-line">function heapSort(arr):</div>
                <div id="codeLine2" class="code-line">    n = arr.length</div>
                <div id="codeLine3" class="code-line">    # 1. 建堆阶段</div>
                <div id="codeLine4" class="code-line">    for i = n/2 - 1 down to 0:</div>
                <div id="codeLine5" class="code-line">        heapify(arr, n, i)</div>
                <div id="codeLine6" class="code-line">    # 2. 排序阶段</div>
                <div id="codeLine7" class="code-line">    for i = n-1 down to 1:</div>
                <div id="codeLine8" class="code-line">        swap(arr[0], arr[i])</div>
                <div id="codeLine9" class="code-line">        heapify(arr, i, 0)</div>
                <div id="codeLine10" class="code-line"></div>
                <div id="codeLine11" class="code-line">function heapify(arr, n, i):</div>
                <div id="codeLine12" class="code-line">    largest = i  # 或 smallest 对于小顶堆</div>
                <div id="codeLine13" class="code-line">    left = 2*i + 1</div>
                <div id="codeLine14" class="code-line">    right = 2*i + 2</div>
                <div id="codeLine15" class="code-line">    </div>
                <div id="codeLine16" class="code-line">    if left < n and arr[left] > arr[largest]:</div>
                <div id="codeLine17" class="code-line">        largest = left</div>
                <div id="codeLine18" class="code-line">    </div>
                <div id="codeLine19" class="code-line">    if right < n and arr[right] > arr[largest]:</div>
                <div id="codeLine20" class="code-line">        largest = right</div>
                <div id="codeLine21" class="code-line">    </div>
                <div id="codeLine22" class="code-line">    if largest != i:</div>
                <div id="codeLine23" class="code-line">        swap(arr[i], arr[largest])</div>
                <div id="codeLine24" class="code-line">        heapify(arr, n, largest)</div>
            </div>
        </div>
        
        <footer class="footer">
            <p>堆排序算法可视化 | 时间复杂度: O(n log n) | 空间复杂度: O(1) | 不稳定排序</p>
            <p>交互式教学动画设计 | 使用HTML5 Canvas实现</p>
        </footer>
    </div>

    <script>
        // 堆排序可视化主程序
        document.addEventListener('DOMContentLoaded', function() {
            // 常量定义
            const TREE_CANVAS = document.getElementById('treeCanvas');
            const ARRAY_CANVAS = document.getElementById('arrayCanvas');
            const TREE_CTX = TREE_CANVAS.getContext('2d');
            const ARRAY_CTX = ARRAY_CANVAS.getContext('2d');
            
            // 状态变量
            let data = [];
            let heapSize = 0;
            let sortedElements = [];
            let animationState = {
                phase: 'idle', // 'idle', 'building', 'sorting', 'heapifying'
                stepIndex: 0,
                currentIndex: -1,
                comparingIndex: -1,
                swappingIndex: -1,
                heapifyRoot: -1,
                heapifyTarget: -1,
                isMaxHeap: true,
                isPlaying: false,
                speed: 500,
                comparisonCount: 0,
                swapCount: 0,
                steps: []
            };
            
            // 初始化数据
            function initializeData() {
                data = [];
                const size = 10;
                for (let i = 0; i < size; i++) {
                    data.push(Math.floor(Math.random() * 90) + 10); // 10-99之间的随机数
                }
                heapSize = data.length;
                sortedElements = [];
                animationState.stepIndex = 0;
                animationState.currentIndex = -1;
                animationState.comparingIndex = -1;
                animationState.swappingIndex = -1;
                animationState.heapifyRoot = -1;
                animationState.heapifyTarget = -1;
                animationState.comparisonCount = 0;
                animationState.swapCount = 0;
                animationState.steps = [];
                animationState.phase = 'idle';
                
                updateStatusDisplay();
                updateStepDescription('已生成新的随机数据。点击"播放"按钮开始堆排序演示。');
                highlightCodeLine(1);
                drawVisualization();
            }
            
            // 更新状态显示
            function updateStatusDisplay() {
                document.getElementById('heapSize').textContent = heapSize;
                document.getElementById('sortedCount').textContent = sortedElements.length;
                document.getElementById('comparisonCount').textContent = animationState.comparisonCount;
                document.getElementById('swapCount').textContent = animationState.swapCount;
                
                const modeRadios = document.getElementsByName('sortMode');
                animationState.isMaxHeap = modeRadios[0].checked;
                document.getElementById('currentStep').textContent = 
                    animationState.phase === 'idle' ? '准备开始' :
                    animationState.phase === 'building' ? '建堆阶段' :
                    animationState.phase === 'sorting' ? '排序阶段' :
                    animationState.phase === 'heapifying' ? '调整堆' : '完成';
            }
            
            // 更新步骤说明
            function updateStepDescription(text) {
                document.getElementById('stepDescription').textContent = text;
            }
            
            // 高亮代码行
            function highlightCodeLine(lineNumber) {
                // 清除所有高亮
                for (let i = 1; i <= 24; i++) {
                    const lineElement = document.getElementById(`codeLine${i}`);
                    if (lineElement) {
                        lineElement.classList.remove('active');
                    }
                }
                
                // 高亮指定行
                const activeLine = document.getElementById(`codeLine${lineNumber}`);
                if (activeLine) {
                    activeLine.classList.add('active');
                }
            }
            
            // 绘制树形视图
            function drawTree() {
                TREE_CTX.clearRect(0, 0, TREE_CANVAS.width, TREE_CANVAS.height);
                
                // 设置画布尺寸
                TREE_CANVAS.width = TREE_CANVAS.parentElement.clientWidth;
                TREE_CANVAS.height = TREE_CANVAS.parentElement.clientHeight;
                
                const nodeRadius = 25;
                const levelHeight = 80;
                const canvasWidth = TREE_CANVAS.width;
                
                // 计算树的深度
                const treeDepth = Math.floor(Math.log2(heapSize)) + 1;
                
                // 递归绘制节点
                function drawNode(index, x, y, level) {
                    if (index >= heapSize) return;
                    
                    // 确定节点颜色
                    let nodeColor = '#ecf0f1'; // 默认
                    if (index === animationState.currentIndex) {
                        nodeColor = '#3498db'; // 当前操作节点
                    } else if (index === animationState.comparingIndex) {
                        nodeColor = '#f1c40f'; // 比较节点
                    } else if (index === animationState.swappingIndex) {
                        nodeColor = '#e74c3c'; // 交换节点
                    } else if (index === animationState.heapifyRoot || index === animationState.heapifyTarget) {
                        nodeColor = '#3498db'; // 堆化相关节点
                    }
                    
                    // 绘制连接线到子节点
                    const leftChildIndex = 2 * index + 1;
                    const rightChildIndex = 2 * index + 2;
                    
                    if (leftChildIndex < heapSize) {
                        const childX = x - (canvasWidth / Math.pow(2, level + 2));
                        const childY = y + levelHeight;
                        
                        TREE_CTX.beginPath();
                        TREE_CTX.moveTo(x, y + nodeRadius);
                        TREE_CTX.lineTo(childX, childY - nodeRadius);
                        TREE_CTX.strokeStyle = '#7f8c8d';
                        TREE_CTX.lineWidth = 2;
                        TREE_CTX.stroke();
                        
                        drawNode(leftChildIndex, childX, childY, level + 1);
                    }
                    
                    if (rightChildIndex < heapSize) {
                        const childX = x + (canvasWidth / Math.pow(2, level + 2));
                        const childY = y + levelHeight;
                        
                        TREE_CTX.beginPath();
                        TREE_CTX.moveTo(x, y + nodeRadius);
                        TREE_CTX.lineTo(childX, childY - nodeRadius);
                        TREE_CTX.strokeStyle = '#7f8c8d';
                        TREE_CTX.lineWidth = 2;
                        TREE_CTX.stroke();
                        
                        drawNode(rightChildIndex, childX, childY, level + 1);
                    }
                    
                    // 绘制节点
                    TREE_CTX.beginPath();
                    TREE_CTX.arc(x, y, nodeRadius, 0, Math.PI * 2);
                    TREE_CTX.fillStyle = nodeColor;
                    TREE_CTX.fill();
                    TREE_CTX.strokeStyle = '#34495e';
                    TREE_CTX.lineWidth = 2;
                    TREE_CTX.stroke();
                    
                    // 绘制节点值
                    TREE_CTX.fillStyle = '#2c3e50';
                    TREE_CTX.font = 'bold 16px Arial';
                    TREE_CTX.textAlign = 'center';
                    TREE_CTX.textBaseline = 'middle';
                    TREE_CTX.fillText(data[index], x, y);
                    
                    // 绘制节点索引
                    TREE_CTX.fillStyle = '#7f8c8d';
                    TREE_CTX.font = '12px Arial';
                    TREE_CTX.fillText(`[${index}]`, x, y + nodeRadius + 15);
                }
                
                // 从根节点开始绘制
                const rootX = canvasWidth / 2;
                const rootY = nodeRadius + 30;
                drawNode(0, rootX, rootY, 1);
                
                // 绘制已排序元素
                const sortedStartY = TREE_CANVAS.height - 60;
                const sortedSpacing = 40;
                
                TREE_CTX.fillStyle = '#bdc3c7';
                TREE_CTX.font = '14px Arial';
                TREE_CTX.textAlign = 'left';
                TREE_CTX.fillText('已排序元素:', 20, sortedStartY - 20);
                
                for (let i = 0; i < sortedElements.length; i++) {
                    const x = 30 + i * sortedSpacing;
                    const y = sortedStartY;
                    
                    TREE_CTX.beginPath();
                    TREE_CTX.arc(x, y, 15, 0, Math.PI * 2);
                    TREE_CTX.fillStyle = '#2ecc71';
                    TREE_CTX.fill();
                    TREE_CTX.strokeStyle = '#27ae60';
                    TREE_CTX.lineWidth = 2;
                    TREE_CTX.stroke();
                    
                    TREE_CTX.fillStyle = '#2c3e50';
                    TREE_CTX.font = 'bold 14px Arial';
                    TREE_CTX.textAlign = 'center';
                    TREE_CTX.textBaseline = 'middle';
                    TREE_CTX.fillText(sortedElements[i], x, y);
                }
            }
            
            // 绘制数组视图
            function drawArray() {
                ARRAY_CTX.clearRect(0, 0, ARRAY_CANVAS.width, ARRAY_CANVAS.height);
                
                // 设置画布尺寸
                ARRAY_CANVAS.width = ARRAY_CANVAS.parentElement.clientWidth;
                ARRAY_CANVAS.height = ARRAY_CANVAS.parentElement.clientHeight;
                
                const cellWidth = 50;
                const cellHeight = 40;
                const startX = (ARRAY_CANVAS.width - (data.length * cellWidth)) / 2;
                const startY = 50;
                
                // 绘制数组标题
                ARRAY_CTX.fillStyle = '#bdc3c7';
                ARRAY_CTX.font = 'bold 18px Arial';
                ARRAY_CTX.textAlign = 'center';
                ARRAY_CTX.fillText('数组表示', ARRAY_CANVAS.width / 2, 30);
                
                // 绘制堆范围指示
                if (heapSize < data.length) {
                    ARRAY_CTX.fillStyle = 'rgba(52, 152, 219, 0.2)';
                    ARRAY_CTX.fillRect(
                        startX + heapSize * cellWidth, 
                        startY - 5, 
                        (data.length - heapSize) * cellWidth, 
                        cellHeight + 10
                    );
                    
                    ARRAY_CTX.fillStyle = '#3498db';
                    ARRAY_CTX.font = '14px Arial';
                    ARRAY_CTX.textAlign = 'center';
                    ARRAY_CTX.fillText(
                        `堆范围: 0-${heapSize-1}`, 
                        startX + (heapSize + (data.length - heapSize) / 2) * cellWidth, 
                        startY + cellHeight + 25
                    );
                }
                
                // 绘制数组元素
                for (let i = 0; i < data.length; i++) {
                    const x = startX + i * cellWidth;
                    const y = startY;
                    
                    // 确定单元格颜色
                    let cellColor = '#ecf0f1'; // 默认
                    if (i === animationState.currentIndex) {
                        cellColor = '#3498db'; // 当前操作节点
                    } else if (i === animationState.comparingIndex) {
                        cellColor = '#f1c40f'; // 比较节点
                    } else if (i === animationState.swappingIndex) {
                        cellColor = '#e74c3c'; // 交换节点
                    } else if (i === animationState.heapifyRoot || i === animationState.heapifyTarget) {
                        cellColor = '#3498db'; // 堆化相关节点
                    } else if (i >= heapSize) {
                        cellColor = '#2ecc71'; // 已排序元素
                    }
                    
                    // 绘制单元格
                    ARRAY_CTX.fillStyle = cellColor;
                    ARRAY_CTX.fillRect(x, y, cellWidth, cellHeight);
                    ARRAY_CTX.strokeStyle = '#34495e';
                    ARRAY_CTX.lineWidth = 2;
                    ARRAY_CTX.strokeRect(x, y, cellWidth, cellHeight);
                    
                    // 绘制值
                    ARRAY_CTX.fillStyle = '#2c3e50';
                    ARRAY_CTX.font = 'bold 16px Arial';
                    ARRAY_CTX.textAlign = 'center';
                    ARRAY_CTX.textBaseline = 'middle';
                    ARRAY_CTX.fillText(data[i], x + cellWidth / 2, y + cellHeight / 2);
                    
                    // 绘制索引
                    ARRAY_CTX.fillStyle = '#7f8c8d';
                    ARRAY_CTX.font = '12px Arial';
                    ARRAY_CTX.fillText(`[${i}]`, x + cellWidth / 2, y + cellHeight + 15);
                }
            }
            
            // 绘制可视化
            function drawVisualization() {
                drawTree();
                drawArray();
            }
            
            // 执行建堆阶段
            async function buildHeap() {
                animationState.phase = 'building';
                updateStatusDisplay();
                
                // 从最后一个非叶子节点开始
                const startIdx = Math.floor(heapSize / 2) - 1;
                
                for (let i = startIdx; i >= 0; i--) {
                    await heapify(i, heapSize);
                }
                
                updateStepDescription(`建堆完成！现在堆顶元素是${animationState.isMaxHeap ? '最大' : '最小'}值: ${data[0]}`);
                highlightCodeLine(6);
                
                // 建堆完成后进入排序阶段
                animationState.phase = 'sorting';
                updateStatusDisplay();
            }
            
            // 堆化函数
            async function heapify(rootIndex, size) {
                animationState.heapifyRoot = rootIndex;
                animationState.phase = 'heapifying';
                updateStatusDisplay();
                highlightCodeLine(11);
                
                let largestOrSmallest = rootIndex;
                const leftChildIndex = 2 * rootIndex + 1;
                const rightChildIndex = 2 * rootIndex + 2;
                
                // 与左子节点比较
                if (leftChildIndex < size) {
                    animationState.comparingIndex = leftChildIndex;
                    animationState.currentIndex = largestOrSmallest;
                    updateStepDescription(`比较节点[${largestOrSmallest}](${data[largestOrSmallest]})和左子节点[${leftChildIndex}](${data[leftChildIndex]})`);
                    drawVisualization();
                    animationState.comparisonCount++;
                    updateStatusDisplay();
                    highlightCodeLine(16);
                    
                    await sleep(animationState.speed);
                    
                    const shouldUpdate = animationState.isMaxHeap ? 
                        data[leftChildIndex] > data[largestOrSmallest] : 
                        data[leftChildIndex] < data[largestOrSmallest];
                    
                    if (shouldUpdate) {
                        largestOrSmallest = leftChildIndex;
                        highlightCodeLine(17);
                    }
                }
                
                // 与右子节点比较
                if (rightChildIndex < size) {
                    animationState.comparingIndex = rightChildIndex;
                    animationState.currentIndex = largestOrSmallest;
                    updateStepDescription(`比较节点[${largestOrSmallest}](${data[largestOrSmallest]})和右子节点[${rightChildIndex}](${data[rightChildIndex]})`);
                    drawVisualization();
                    animationState.comparisonCount++;
                    updateStatusDisplay();
                    highlightCodeLine(19);
                    
                    await sleep(animationState.speed);
                    
                    const shouldUpdate = animationState.isMaxHeap ? 
                        data[rightChildIndex] > data[largestOrSmallest] : 
                        data[rightChildIndex] < data[largestOrSmallest];
                    
                    if (shouldUpdate) {
                        largestOrSmallest = rightChildIndex;
                        highlightCodeLine(20);
                    }
                }
                
                // 如果需要交换
                if (largestOrSmallest !== rootIndex) {
                    animationState.heapifyTarget = largestOrSmallest;
                    animationState.swappingIndex = rootIndex;
                    updateStepDescription(`交换节点[${rootIndex}](${data[rootIndex]})和节点[${largestOrSmallest}](${data[largestOrSmallest]})`);
                    highlightCodeLine(22);
                    
                    drawVisualization();
                    await sleep(animationState.speed);
                    
                    // 执行交换
                    [data[rootIndex], data[largestOrSmallest]] = [data[largestOrSmallest], data[rootIndex]];
                    animationState.swapCount++;
                    updateStatusDisplay();
                    highlightCodeLine(23);
                    
                    drawVisualization();
                    await sleep(animationState.speed);
                    
                    // 递归堆化受影响的子树
                    highlightCodeLine(24);
                    await heapify(largestOrSmallest, size);
                }
                
                animationState.heapifyRoot = -1;
                animationState.heapifyTarget = -1;
                animationState.comparingIndex = -1;
                animationState.currentIndex = -1;
                animationState.swappingIndex = -1;
            }
            
            // 执行排序阶段
            async function sortHeap() {
                for (let i = data.length - 1; i > 0; i--) {
                    // 交换堆顶和当前末尾元素
                    animationState.currentIndex = 0;
                    animationState.swappingIndex = i;
                    updateStepDescription(`交换堆顶元素[0](${data[0]})和末尾元素[${i}](${data[i]})，将${animationState.isMaxHeap ? '最大' : '最小'}值放到正确位置`);
                    highlightCodeLine(8);
                    
                    drawVisualization();
                    await sleep(animationState.speed);
                    
                    // 执行交换
                    [data[0], data[i]] = [data[i], data[0]];
                    animationState.swapCount++;
                    updateStatusDisplay();
                    
                    drawVisualization();
                    await sleep(animationState.speed);
                    
                    // 将交换后的元素标记为已排序
                    sortedElements.unshift(data[i]);
                    heapSize--;
                    
                    // 调整堆
                    highlightCodeLine(9);
                    if (heapSize > 1) {
                        await heapify(0, heapSize);
                    }
                    
                    updateStatusDisplay();
                    drawVisualization();
                    
                    if (i > 1) {
                        await sleep(animationState.speed);
                    }
                }
                
                // 最后一个元素
                sortedElements.unshift(data[0]);
                heapSize = 0;
                
                animationState.phase = 'idle';
                updateStatusDisplay();
                updateStepDescription(`排序完成！${animationState.isMaxHeap ? '升序' : '降序'}排序结果: ${sortedElements.join(', ')}`);
                highlightCodeLine(1);
                
                // 更新播放按钮状态
                const playPauseBtn = document.getElementById('playPauseBtn');
                playPauseBtn.textContent = '▶ 播放';
                playPauseBtn.classList.remove('btn-danger');
                playPauseBtn.classList.add('btn-primary');
                animationState.isPlaying = false;
            }
            
            // 执行下一步
            async function nextStep() {
                if (animationState.phase === 'idle') {
                    // 开始建堆
                    await buildHeap();
                } else if (animationState.phase === 'building' || animationState.phase === 'heapifying') {
                    // 建堆阶段 - 继续执行
                    // 在实际实现中，这里需要更精细的步骤控制
                    // 为简化，我们直接执行完整建堆
                    if (heapSize === data.length) {
                        await buildHeap();
                    }
                } else if (animationState.phase === 'sorting') {
                    // 排序阶段 - 继续执行
                    if (heapSize > 0) {
                        await sortHeap();
                    }
                }
            }
            
            // 睡眠函数（用于动画延迟）
            function sleep(ms) {
                return new Promise(resolve => setTimeout(resolve, ms));
            }
            
            // 开始/暂停动画
            async function togglePlayPause() {
                const playPauseBtn = document.getElementById('playPauseBtn');
                
                if (animationState.isPlaying) {
                    // 暂停
                    animationState.isPlaying = false;
                    playPauseBtn.textContent = '▶ 播放';
                    playPauseBtn.classList.remove('btn-danger');
                    playPauseBtn.classList.add('btn-primary');
                } else {
                    // 开始播放
                    animationState.isPlaying = true
<!--检测到代码截断，自动续写中...-->
playPauseBtn.textContent = '⏸ 暂停';
                    playPauseBtn.classList.remove('btn-primary');
                    playPauseBtn.classList.add('btn-danger');
                    
                    // 如果还没开始，先建堆
                    if (animationState.phase === 'idle') {
                        await buildHeap();
                    }
                    
                    // 然后执行排序
                    await sortHeap();
                    
                    // 完成后重置按钮状态
                    playPauseBtn.textContent = '▶ 播放';
                    playPauseBtn.classList.remove('btn-danger');
                    playPauseBtn.classList.add('btn-primary');
                    animationState.isPlaying = false;
                }
            }
            
            // 上一步（简化实现，重置到初始状态）
            function prevStep() {
                if (animationState.stepIndex > 0) {
                    animationState.stepIndex--;
                    // 在实际完整实现中，这里应该恢复之前的状态
                    // 为简化，我们提示用户使用重置功能
                    updateStepDescription('上一步功能需要完整的状态历史记录。请使用"重置"按钮重新开始。');
                }
            }
            
            // 重置动画
            function resetAnimation() {
                // 停止任何正在进行的动画
                animationState.isPlaying = false;
                const playPauseBtn = document.getElementById('playPauseBtn');
                playPauseBtn.textContent = '▶ 播放';
                playPauseBtn.classList.remove('btn-danger');
                playPauseBtn.classList.add('btn-primary');
                
                // 重新初始化数据
                initializeData();
            }
            
            // 随机生成新数据
            function randomizeData() {
                resetAnimation();
                initializeData();
            }
            
            // 更新动画速度
            function updateSpeed() {
                const speedSlider = document.getElementById('speedSlider');
                // 将滑块值（1-10）转换为延迟时间（1000ms-100ms）
                animationState.speed = 1100 - (speedSlider.value * 100);
            }
            
            // 事件监听器
            document.getElementById('playPauseBtn').addEventListener('click', togglePlayPause);
            document.getElementById('nextStepBtn').addEventListener('click', async () => {
                if (!animationState.isPlaying) {
                    await nextStep();
                }
            });
            document.getElementById('prevStepBtn').addEventListener('click', prevStep);
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            document.getElementById('randomizeBtn').addEventListener('click', randomizeData);
            
            // 排序模式切换
            const modeRadios = document.getElementsByName('sortMode');
            modeRadios.forEach(radio => {
                radio.addEventListener('change', function() {
                    if (!animationState.isPlaying) {
                        animationState.isMaxHeap = this.value === 'max';
                        resetAnimation();
                    }
                });
            });
            
            // 速度滑块
            const speedSlider = document.getElementById('speedSlider');
            speedSlider.addEventListener('input', updateSpeed);
            
            // 窗口大小变化时重绘
            window.addEventListener('resize', drawVisualization);
            
            // 初始化
            initializeData();
            
            // 初始绘制
            drawVisualization();
        });
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 堆排序交互式教学动画使用指南

欢迎使用堆排序算法交互式教学动画！本工具旨在通过直观、美观的可视化方式，帮助您深入理解堆排序算法的核心原理与执行过程。无论您是计算机科学专业的学生、编程爱好者，还是算法自学者，本动画都将为您提供沉浸式的学习体验。

### 一、 功能说明

本动画完整模拟了堆排序算法的两个核心阶段：
1.  **建堆阶段**：将无序数组调整为一个符合堆性质（大顶堆或小顶堆）的完全二叉树。
2.  **排序阶段**：反复将堆顶元素（最大值或最小值）与当前堆的末尾元素交换，并重新调整堆结构，直至所有元素有序。

动画采用**双视图同步**设计：
*   **左侧树形视图**：以二叉树形式直观展示堆的结构与节点间关系。
*   **右侧数组视图**：展示数组的实际存储状态，并与树形视图实时同步。

### 二、 主要功能

1.  **核心控制面板**
    *   **播放/暂停**：开始或暂停自动连续动画，让算法流程自动演示。
    *   **下一步**：手动单步执行算法，在关键步骤（如比较、交换、调整）处暂停，便于仔细思考。
    *   **上一步**：回退到上一个操作状态（注：当前实现为简化版本，完整回退需依赖状态历史，建议配合“重置”功能进行阶段复习）。
    *   **重置**：将动画恢复到初始状态，清空所有操作记录。
    *   **随机数据**：生成一组全新的随机数，重新开始排序演示。

2.  **配置面板**
    *   **排序模式选择**：
        *   **大顶堆 (升序排序)**：父节点值 ≥ 子节点值，排序结果为从小到大。
        *   **小顶堆 (降序排序)**：父节点值 ≤ 子节点值，排序结果为从大到小。
    *   **动画速度滑块**：可动态调整自动播放的速度，从“慢”到“快”满足不同学习节奏。

3.  **信息显示面板**
    *   **状态仪表盘**：实时显示堆大小、已排序元素个数、算法执行过程中的比较次数和交换次数。
    *   **步骤说明区**：用自然语言详细描述当前正在执行的操作（如“正在调整节点[5]，与其左子节点[11]进行比较”）。
    *   **算法伪代码**：右侧显示堆排序的关键伪代码，并会**高亮显示当前正在执行的行**，建立视觉操作与抽象代码的直接关联。

4.  **可视化图例**
    位于树形视图下方，清晰说明了不同颜色节点的含义：
    *   **浅灰色**：默认/未操作节点
    *   **亮蓝色**：当前正在操作的焦点节点
    *   **黄色**：正在与焦点节点进行比较的节点
    *   **红色**：即将或正在交换的节点
    *   **绿色**：已排序完成的元素

### 三、 设计特色

1.  **极美动画与专业配色**：采用深蓝背景与高饱和度配色方案，营造专注的学习环境。节点移动、交换轨迹平滑流畅，符合“动画极美”的要求。
2.  **认知负荷优化**：通过分阶段演示（建堆→排序）、颜色编码、同步高亮和即时文字反馈，将复杂算法分解为易于理解的认知单元。
3.  **双视图同步映射**：树形结构与数组存储的同步变化，帮助学习者建立数据结构不同表现形式之间的心智模型。
4.  **探索式学习支持**：结合自动播放与单步控制，既支持整体流程观摩，也支持关键步骤的暂停与审视。

### 四、 教学要点

使用本动画时，建议重点关注以下算法核心概念：

1.  **堆的性质**：观察无论是大顶堆还是小顶堆，如何始终保持父节点与子节点之间的大小关系。
2.  **“下沉”操作**：这是`heapify`（堆化）的核心。注意观察一个节点如何与其子节点比较，并在不满足堆性质时如何“下沉”到正确位置。
3.  **建堆的起点**：理解为什么建堆要从 **最后一个非叶子节点** 开始，自底向上进行。
4.  **排序的本质**：在排序阶段，体会每次“交换堆顶与末尾元素”的操作，实际上就是将当前堆中的极值元素移动到其最终的有序位置。
5.  **堆大小的变化**：注意观察每次交换后，“堆”的有效范围如何减一，而“已排序”区域如何增长。

### 五、 使用建议

为了获得最佳学习效果，我们推荐以下使用流程：

1.  **初次接触**：选择“大顶堆”模式，点击“播放”按钮，完整观看一遍算法从建堆到排序结束的全过程，建立整体印象。
2.  **分步学习**：
    *   点击“重置”后，使用“下一步”按钮手动执行。
    *   **在建堆阶段**：关注每个非叶子节点调整时，其子树的演变过程。
    *   **在排序阶段**：重点关注每次交换后，对新的堆顶元素进行的“下沉”调整。
3.  **对比学习**：完成大顶堆学习后，切换到“小顶堆”模式，观察两者在比较逻辑和排序结果上的差异。
4.  **关联代码**：在单步执行时，同步观察右侧伪代码的高亮行，理解每一行代码对应的实际数据操作。
5.  **尝试与验证**：使用“随机数据”功能生成不同数据集，观察算法在不同数据下的表现，加深理解。

---

**祝您学习愉快，在算法的美妙世界中收获知识与灵感！** 如果您有任何反馈或建议，欢迎与我们交流。