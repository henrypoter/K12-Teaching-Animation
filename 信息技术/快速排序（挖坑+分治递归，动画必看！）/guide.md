# 需求：快速排序（挖坑+分治递归，动画必看！）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为计算机科学或相关专业的初学者，以及对算法感兴趣的编程爱好者。他们具备基础的编程概念，但对快速排序算法的具体执行流程、尤其是“挖坑法”这一形象化的实现方式理解不深。
2.  **核心需求**：
    *   **直观理解算法流程**：用户需要清晰地看到数组如何被选取的基准值（pivot）分割成两部分，以及递归过程如何展开。
    *   **掌握“挖坑法”细节**：这是本动画的重点。用户需要看到“坑”的位置如何移动，左右指针如何交替“填坑”和“挖新坑”，这是理解该实现方式的关键。
    *   **观察元素比较与交换**：需要高亮显示当前正在比较的元素和基准值，以及发生交换的时刻。
    *   **控制学习节奏**：用户需要能够暂停、步进、重置动画，以便在关键步骤停下来思考。
    *   **关联代码与动画**：将动画的每一步与伪代码或关键代码行同步高亮，建立视觉操作与程序逻辑的直接联系。

#### 教学设计思路
1.  **核心概念**：
    *   **分治递归**：强调“选取基准 -> 分区 -> 递归处理左右子序列”这一核心思想。
    *   **挖坑法**：将基准值视为一个“坑”，通过左右指针的交替移动和元素赋值，完成分区过程。这是降低理解难度的关键隐喻。
    *   **递归栈**：可视化递归调用栈，帮助理解算法的深度和当前正在处理的子问题。
2.  **认知规律**：
    *   **从整体到局部**：先展示一次完整的分区操作，再逐步分解“挖坑”和“填坑”的每一步。
    *   **多通道编码**：结合视觉动画（元素移动、颜色变化）、文本说明（步骤提示）、代码高亮和可能的音效，强化记忆。
    *   **交互式探索**：允许用户手动输入或随机生成不同的初始数组，观察算法在不同数据（如已排序、逆序、随机）下的表现。
3.  **交互设计**：
    *   **主控面板**：提供播放、暂停、下一步、上一步、重置、速度调节等控件。
    *   **数据输入区**：允许用户输入自定义数组或一键生成随机数组。
    *   **双视图同步**：
        *   **动画视图**：以条形图或圆球形式展示数组，动态显示坑位、左右指针、比较和交换。
        *   **代码/逻辑视图**：同步显示对应的算法伪代码或关键步骤描述，并高亮当前执行行。
    *   **递归栈可视化**：在画面一侧展示一个“栈”的图形，动态压入和弹出当前处理的子数组区间 `[left, right]`。
4.  **视觉呈现**：
    *   **数组可视化**：使用不同高度的彩色条形或编号圆球代表数组元素。
    *   **状态色标**：
        *   **基准/坑**：用醒目的颜色（如红色）标记，并可能显示一个“坑”的图标或凹陷效果。
        *   **左指针**：蓝色。
        *   **右指针**：绿色。
        *   **当前比较元素**：高亮（如黄色）。
        *   **已排序元素**：分区完成后，基准值最终落位的位置元素用特殊颜色（如金色）标记，表示其位置已确定。
        *   **待处理区间**：灰色或半透明。
        *   **已处理区间**：分区完成后，左右子数组用不同的浅色调区分。
    *   **动画流畅性**：元素的移动、颜色变化采用平滑过渡，使过程清晰不突兀。

#### 配色方案选择
*   **主色调**：采用科技蓝 (`#3498db`) 作为背景或主界面色调，传达理性与逻辑。
*   **数据元素色**：
    *   默认元素：浅灰色 (`#ecf0f1`) 或温和的渐变色。
    *   基准/坑：亮红色 (`#e74c3c`)，强调其核心和“空洞”状态。
    *   左指针：蓝色 (`#3498db`)。
    *   右指针：绿色 (`#2ecc71`)。
    *   当前活动/比较：亮黄色 (`#f1c40f`)。
    *   已确定位置：金色 (`#f39c12`)。
*   **UI控件**：使用深灰色 (`#2c3e50`) 和白色文字，按钮采用主色调蓝的变体，悬停有效果变化。
*   **代码高亮**：当前行背景用浅黄色 (`#fffacd`)，关键字用不同颜色区分。
*   **整体风格**：干净、明亮、对比度适中，确保视觉焦点始终在动态变化的算法过程上。

#### 交互功能列表
1.  **动画控制**：
    *   播放 / 暂停
    *   下一步 (Step Forward) / 上一步 (Step Backward)
    *   重置 (Reset) 到初始状态
    *   动画速度滑动条调节
2.  **数据管理**：
    *   自定义数组输入框（支持逗号或空格分隔的数字）
    *   “随机生成数组”按钮
    *   “使用示例数组”按钮（提供典型用例，如已排序、逆序、重复值）
3.  **视图与信息**：
    *   **分区过程动画**：核心视图，展示元素移动和“挖坑填坑”。
    *   **递归栈监视器**：可视化展示当前递归调用的层级和待处理的区间。
    *   **代码执行视图**：同步高亮当前执行的伪代码或逻辑步骤。
    *   **步骤说明面板**：用文字描述当前步骤在做什么（例如：“选取左端元素6为基准，挖坑...”）。
    *   **关键信息显示**：当前基准值、左右指针索引、比较次数、交换次数等。
4.  **辅助功能**：
    *   显示/隐藏递归栈视图或代码视图的开关。
    *   工具提示：鼠标悬停在元素或控件上时有简要说明。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>快速排序算法动画 - 挖坑法+分治递归</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #1a2980, #26d0ce);
            color: #333;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            padding: 25px;
            margin-top: 20px;
        }

        h1 {
            text-align: center;
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }

        .subtitle {
            text-align: center;
            color: #3498db;
            margin-bottom: 25px;
            font-size: 1.1rem;
        }

        .panel {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 25px;
        }

        .control-panel {
            flex: 1;
            min-width: 300px;
            background: #f8f9fa;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }

        .info-panel {
            flex: 1;
            min-width: 300px;
            background: #f8f9fa;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }

        h2 {
            color: #2c3e50;
            border-bottom: 2px solid #3498db;
            padding-bottom: 8px;
            margin-bottom: 15px;
            font-size: 1.4rem;
        }

        .input-group {
            margin-bottom: 15px;
        }

        label {
            display: block;
            margin-bottom: 5px;
            color: #555;
            font-weight: 500;
        }

        input[type="text"] {
            width: 100%;
            padding: 10px;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        input[type="text"]:focus {
            border-color: #3498db;
            outline: none;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }

        button {
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
            flex: 1;
            min-width: 120px;
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
            background-color: #2ecc71;
            color: white;
        }

        .btn-secondary:hover {
            background-color: #27ae60;
            transform: translateY(-2px);
        }

        .btn-warning {
            background-color: #e74c3c;
            color: white;
        }

        .btn-warning:hover {
            background-color: #c0392b;
            transform: translateY(-2px);
        }

        .btn-info {
            background-color: #9b59b6;
            color: white;
        }

        .btn-info:hover {
            background-color: #8e44ad;
            transform: translateY(-2px);
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 15px;
        }

        .speed-control label {
            margin-bottom: 0;
            min-width: 80px;
        }

        input[type="range"] {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            background: #ddd;
            border-radius: 4px;
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            background: #3498db;
            border-radius: 50%;
            cursor: pointer;
        }

        .info-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 12px;
            padding-bottom: 8px;
            border-bottom: 1px dashed #ddd;
        }

        .info-label {
            font-weight: 600;
            color: #555;
        }

        .info-value {
            font-weight: 700;
            color: #2c3e50;
        }

        .pivot-value {
            color: #e74c3c;
        }

        .left-pointer {
            color: #3498db;
        }

        .right-pointer {
            color: #2ecc71;
        }

        .comparisons {
            color: #f39c12;
        }

        .swaps {
            color: #9b59b6;
        }

        .step-description {
            background-color: #fffacd;
            border-left: 4px solid #f1c40f;
            padding: 15px;
            border-radius: 5px;
            margin-top: 15px;
            font-size: 1rem;
            line-height: 1.5;
            min-height: 70px;
        }

        .visualization-container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .array-container {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }

        .canvas-container {
            width: 100%;
            height: 300px;
            position: relative;
            margin-top: 10px;
        }

        #arrayCanvas {
            width: 100%;
            height: 100%;
            border-radius: 5px;
            background-color: #f8f9fa;
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
            gap: 5px;
        }

        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 3px;
        }

        .legend-text {
            font-size: 0.9rem;
            color: #555;
        }

        .code-container {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }

        .code-wrapper {
            background-color: #2c3e50;
            border-radius: 5px;
            padding: 15px;
            overflow-x: auto;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 0.95rem;
            line-height: 1.4;
        }

        .code-line {
            padding: 3px 5px;
            margin: 2px 0;
            border-radius: 3px;
            transition: background-color 0.3s;
            color: #ecf0f1;
        }

        .code-line.highlighted {
            background-color: rgba(241, 196, 15, 0.3);
            color: #f1c40f;
            font-weight: 600;
        }

        .recursion-container {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }

        .recursion-stack {
            display: flex;
            flex-direction: column-reverse;
            gap: 10px;
            margin-top: 15px;
            min-height: 120px;
        }

        .stack-frame {
            background-color: #3498db;
            color: white;
            padding: 10px 15px;
            border-radius: 5px;
            font-family: 'Consolas', 'Monaco', monospace;
            font-weight: 600;
            text-align: center;
            transition: all 0.3s;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .stack-frame.active {
            background-color: #e74c3c;
            transform: scale(1.05);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .footer {
            text-align: center;
            margin-top: 25px;
            color: rgba(255, 255, 255, 0.8);
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .panel {
                flex-direction: column;
            }
            
            .button-group {
                flex-direction: column;
            }
            
            button {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <h1>快速排序算法动画</h1>
    <div class="subtitle">挖坑法 + 分治递归 - 交互式教学演示</div>
    
    <div class="container">
        <div class="panel">
            <div class="control-panel">
                <h2>控制面板</h2>
                
                <div class="input-group">
                    <label for="arrayInput">数组输入 (逗号或空格分隔):</label>
                    <input type="text" id="arrayInput" value="6, 1, 8, 4, 9, 3, 7, 2, 5">
                </div>
                
                <div class="button-group">
                    <button id="startBtn" class="btn-primary">开始排序</button>
                    <button id="pauseBtn" class="btn-warning">暂停</button>
                    <button id="stepBtn" class="btn-info">单步执行</button>
                    <button id="resetBtn" class="btn-warning">重置</button>
                </div>
                
                <div class="button-group">
                    <button id="randomBtn" class="btn-secondary">随机数组</button>
                    <button id="sortedBtn" class="btn-secondary">已排序数组</button>
                    <button id="reverseBtn" class="btn-secondary">逆序数组</button>
                </div>
                
                <div class="speed-control">
                    <label for="speedSlider">动画速度:</label>
                    <input type="range" id="speedSlider" min="1" max="10" value="5">
                    <span id="speedValue">中速</span>
                </div>
            </div>
            
            <div class="info-panel">
                <h2>算法状态</h2>
                
                <div class="info-item">
                    <span class="info-label">基准值 (坑):</span>
                    <span id="pivotValue" class="info-value pivot-value">-</span>
                </div>
                
                <div class="info-item">
                    <span class="info-label">左指针 (i):</span>
                    <span id="leftPointer" class="info-value left-pointer">-</span>
                </div>
                
                <div class="info-item">
                    <span class="info-label">右指针 (j):</span>
                    <span id="rightPointer" class="info-value right-pointer">-</span>
                </div>
                
                <div class="info-item">
                    <span class="info-label">比较次数:</span>
                    <span id="comparisonCount" class="info-value comparisons">0</span>
                </div>
                
                <div class="info-item">
                    <span class="info-label">交换次数:</span>
                    <span id="swapCount" class="info-value swaps">0</span>
                </div>
                
                <div class="info-item">
                    <span class="info-label">递归深度:</span>
                    <span id="recursionDepth" class="info-value">0</span>
                </div>
                
                <div class="step-description" id="stepDescription">
                    点击"开始排序"按钮启动算法动画演示...
                </div>
            </div>
        </div>
        
        <div class="visualization-container">
            <div class="array-container">
                <h2>数组可视化</h2>
                <div class="canvas-container">
                    <canvas id="arrayCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span class="legend-text">基准/坑</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #3498db;"></div>
                        <span class="legend-text">左指针</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2ecc71;"></div>
                        <span class="legend-text">右指针</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f1c40f;"></div>
                        <span class="legend-text">当前比较</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f39c12;"></div>
                        <span class="legend-text">已确定位置</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #9b59b6;"></div>
                        <span class="legend-text">已处理区间</span>
                    </div>
                </div>
            </div>
            
            <div class="code-container">
                <h2>算法代码 (挖坑法)</h2>
                <div class="code-wrapper">
                    <div id="codeLine1" class="code-line">function quickSort(arr, left, right) {</div>
                    <div id="codeLine2" class="code-line">  if (left >= right) return;</div>
                    <div id="codeLine3" class="code-line">  let pivot = partition(arr, left, right);</div>
                    <div id="codeLine4" class="code-line">  quickSort(arr, left, pivot - 1);</div>
                    <div id="codeLine5" class="code-line">  quickSort(arr, pivot + 1, right);</div>
                    <div id="codeLine6" class="code-line">}</div>
                    <div id="codeLine7" class="code-line"></div>
                    <div id="codeLine8" class="code-line">function partition(arr, left, right) {</div>
                    <div id="codeLine9" class="code-line">  let pivot = arr[left]; // 挖坑：取最左元素为基准</div>
                    <div id="codeLine10" class="code-line">  let i = left, j = right;</div>
                    <div id="codeLine11" class="code-line">  while (i < j) {</div>
                    <div id="codeLine12" class="code-line">    while (i < j && arr[j] >= pivot) {</div>
                    <div id="codeLine13" class="code-line">      j--; // 从右向左找小于基准的元素</div>
                    <div id="codeLine14" class="code-line">    }</div>
                    <div id="codeLine15" class="code-line">    if (i < j) {</div>
                    <div id="codeLine16" class="code-line">      arr[i] = arr[j]; // 填左坑，挖右坑</div>
                    <div id="codeLine17" class="code-line">      i++;</div>
                    <div id="codeLine18" class="code-line">    }</div>
                    <div id="codeLine19" class="code-line">    while (i < j && arr[i] <= pivot) {</div>
                    <div id="codeLine20" class="code-line">      i++; // 从左向右找大于基准的元素</div>
                    <div id="codeLine21" class="code-line">    }</div>
                    <div id="codeLine22" class="code-line">    if (i < j) {</div>
                    <div id="codeLine23" class="code-line">      arr[j] = arr[i]; // 填右坑，挖左坑</div>
                    <div id="codeLine24" class="code-line">      j--;</div>
                    <div id="codeLine25" class="code-line">    }</div>
                    <div id="codeLine26" class="code-line">  }</div>
                    <div id="codeLine27" class="code-line">  arr[i] = pivot; // 基准归位</div>
                    <div id="codeLine28" class="code-line">  return i;</div>
                    <div id="codeLine29" class="code-line">}</div>
                </div>
            </div>
            
            <div class="recursion-container">
                <h2>递归调用栈</h2>
                <div class="recursion-stack" id="recursionStack">
                    <div class="stack-frame">栈空</div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="footer">
        快速排序算法动画演示 | 挖坑法实现 | 分治递归可视化
    </div>

    <script>
        // 全局变量
        let array = [6, 1, 8, 4, 9, 3, 7, 2, 5];
        let originalArray = [...array];
        let animationQueue = [];
        let isAnimating = false;
        let isPaused = false;
        let animationSpeed = 300; // 毫秒
        let currentStep = 0;
        let comparisonCount = 0;
        let swapCount = 0;
        let recursionStack = [];
        let currentCodeLine = 0;
        
        // 颜色定义
        const colors = {
            default: '#3498db',
            pivot: '#e74c3c',
            leftPointer: '#3498db',
            rightPointer: '#2ecc71',
            comparing: '#f1c40f',
            sorted: '#f39c12',
            processed: '#9b59b6',
            text: '#2c3e50',
            background: '#f8f9fa'
        };
        
        // DOM元素
        const arrayCanvas = document.getElementById('arrayCanvas');
        const ctx = arrayCanvas.getContext('2d');
        const arrayInput = document.getElementById('arrayInput');
        const startBtn = document.getElementById('startBtn');
        const pauseBtn = document.getElementById('pauseBtn');
        const stepBtn = document.getElementById('stepBtn');
        const resetBtn = document.getElementById('resetBtn');
        const randomBtn = document.getElementById('randomBtn');
        const sortedBtn = document.getElementById('sortedBtn');
        const reverseBtn = document.getElementById('reverseBtn');
        const speedSlider = document.getElementById('speedSlider');
        const speedValue = document.getElementById('speedValue');
        const pivotValue = document.getElementById('pivotValue');
        const leftPointer = document.getElementById('leftPointer');
        const rightPointer = document.getElementById('rightPointer');
        const comparisonCountElem = document.getElementById('comparisonCount');
        const swapCountElem = document.getElementById('swapCount');
        const recursionDepth = document.getElementById('recursionDepth');
        const stepDescription = document.getElementById('stepDescription');
        const recursionStackElem = document.getElementById('recursionStack');
        
        // 初始化Canvas
        function initCanvas() {
            const dpr = window.devicePixelRatio || 1;
            const rect = arrayCanvas.getBoundingClientRect();
            
            arrayCanvas.width = rect.width * dpr;
            arrayCanvas.height = rect.height * dpr;
            
            ctx.scale(dpr, dpr);
            arrayCanvas.style.width = `${rect.width}px`;
            arrayCanvas.style.height = `${rect.height}px`;
            
            drawArray();
        }
        
        // 绘制数组
        function drawArray(highlight = {}) {
            const width = arrayCanvas.width / (window.devicePixelRatio || 1);
            const height = arrayCanvas.height / (window.devicePixelRatio || 1);
            
            ctx.clearRect(0, 0, width, height);
            
            const barWidth = Math.min(60, (width - 20) / array.length);
            const maxValue = Math.max(...array);
            const barSpacing = 5;
            const startX = (width - (barWidth + barSpacing) * array.length) / 2;
            
            // 绘制背景
            ctx.fillStyle = colors.background;
            ctx.fillRect(0, 0, width, height);
            
            // 绘制每个元素
            for (let i = 0; i < array.length; i++) {
                const x = startX + i * (barWidth + barSpacing);
                const barHeight = (array[i] / maxValue) * (height - 80);
                const y = height - barHeight - 30;
                
                // 确定颜色
                let color = colors.default;
                
                if (highlight.pivotIndex === i) {
                    color = colors.pivot;
                } else if (highlight.leftPointer === i) {
                    color = colors.leftPointer;
                } else if (highlight.rightPointer === i) {
                    color = colors.rightPointer;
                } else if (highlight.comparing && 
                          (highlight.comparing.left === i || highlight.comparing.right === i)) {
                    color = colors.comparing;
                } else if (highlight.sorted && highlight.sorted.includes(i)) {
                    color = colors.sorted;
                } else if (highlight.processed && 
                          i >= highlight.processed.start && i <= highlight.processed.end) {
                    color = colors.processed;
                }
                
                // 绘制条形
                ctx.fillStyle = color;
                ctx.fillRect(x, y, barWidth, barHeight);
                
                // 绘制圆角
                ctx.beginPath();
                ctx.moveTo(x, y);
                ctx.lineTo(x + barWidth, y);
                ctx.lineTo(x + barWidth, y + barHeight);
                ctx.lineTo(x, y + barHeight);
                ctx.closePath();
                ctx.fill();
                
                // 绘制边框
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 1;
                ctx.strokeRect(x, y, barWidth, barHeight);
                
                // 绘制数值
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(array[i], x + barWidth/2, height - 10);
                
                // 绘制索引
                ctx.fillStyle = '#7f8c8d';
                ctx.font = '14px Arial';
                ctx.fillText(`[${i}]`, x + barWidth/2, height - 30);
                
                // 如果是坑，绘制特殊标记
                if (highlight.pivotIndex === i && highlight.isHole) {
                    ctx.fillStyle = 'rgba(0, 0, 0, 0.1)';
                    ctx.beginPath();
                    ctx.arc(x + barWidth/2, y + barHeight/2, barWidth/3, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = colors.pivot;
                    ctx.font = 'bold 12px Arial';
                    ctx.fillText('坑', x + barWidth/2, y + barHeight/2 + 4);
                }
            }
            
            // 绘制指针标签
            if (highlight.leftPointer !== undefined) {
                const x = startX + highlight.leftPointer * (barWidth + barSpacing) + barWidth/2;
                ctx.fillStyle = colors.leftPointer;
                ctx.font = 'bold 18px Arial';
                ctx.fillText('i', x, 25);
            }
            
            if (highlight.rightPointer !== undefined) {
                const x = startX + highlight.rightPointer * (barWidth + barSpacing) + barWidth/2;
                ctx.fillStyle = colors.rightPointer;
                ctx.font = 'bold 18px Arial';
                ctx.fillText('j', x, 25);
            }
        }
        
        // 更新代码高亮
        function highlightCodeLine(lineNumber) {
            // 移除所有高亮
            for (let i = 1; i <= 29; i++) {
                const lineElem = document.getElementById(`codeLine${i}`);
                if (lineElem) {
                    lineElem.classList.remove('highlighted');
                }
            }
            
            // 高亮当前行
            if (lineNumber >= 1 && lineNumber <= 29) {
                const lineElem = document.getElementById(`codeLine${lineNumber}`);
                if (lineElem) {
                    lineElem.classList.add('highlighted');
                    lineElem.scrollIntoView({ behavior: 'smooth', block: 'center' });
                }
            }
            
            currentCodeLine = lineNumber;
        }
        
        // 更新递归栈显示
        function updateRecursionStack() {
            recursionStackElem.innerHTML = '';
            
            if (recursionStack.length === 0) {
                const emptyFrame = document.createElement('div');
                emptyFrame.className = 'stack-frame';
                emptyFrame.textContent = '栈空';
                recursionStackElem.appendChild(emptyFrame);
                return;
            }
            
            // 显示栈（从栈底到栈顶）
            for (let i = recursionStack.length - 1; i >= 0; i--) {
                const frame = recursionStack[i];
                const frameElem = document.createElement('div');
                frameElem.className = `stack-frame ${frame.active ? 'active' : ''}`;
                frameElem.textContent = `quickSort(${frame.left}, ${frame.right})`;
                recursionStackElem.appendChild(frameElem);
            }
            
            recursionDepth.textContent = recursionStack.length;
        }
        
        // 生成快速排序动画步骤
        function generateQuickSortAnimation(arr, left, right, depth = 0) {
            if (left >= right) {
                animationQueue.push({
                    type: 'baseCase',
                    left, right,
                    description: `递归基线条件：left(${left}) >= right(${right})，直接返回`,
                    codeLine: 2
                });
                return;
            }
            
            // 记录递归调用
            recursionStack.push({left, right, active: true});
            animationQueue.push({
                type: 'recursionEnter',
                left, right, depth,
                description: `进入递归：处理子数组 [${left}, ${right}]`,
                codeLine: 1
            });
            
            // 分区过程
            let pivotValue = arr[left];
            let i = left, j = right;
            
            animationQueue.push({
                type: 'selectPivot',
                pivotIndex: left,
                pivotValue,
                description: `选取基准：arr[${left}] = ${pivotValue}，挖第一个坑`,
                codeLine: 9
            });
            
            animationQueue.push({
                type: 'initPointers',
                left: i,
                right: j,
                description: `初始化指针：i = ${left}, j = ${right}`,
                codeLine: 10
            });
            
            while (i < j) {
                // 从右向左找小于基准的元素
                animationQueue.push({
                    type: 'startRightScan',
                    left: i,
                    right: j,
                    pivotValue,
                    description: `开始从右向左扫描：寻找小于基准值 ${pivotValue} 的元素`,
                    codeLine: 11
                });
                
                while (i < j && arr[j] >= pivotValue) {
                    comparisonCount++;
                    animationQueue.push({
                        type: 'compareRight',
                        left: i,
                        right: j,
                        pivotValue,
                        arrValue: arr[j],
                        description: `比较：arr[j]=arr[${j}]=${arr[j]} >= 基准值 ${pivotValue}，继续左移 j`,
                        codeLine: 12
                    });
                    j--;
                    
                    animationQueue.push({
                        type: 'moveRightPointer',
                        left: i,
                        right: j,
                        description: `右指针左移：j = ${j}`,
                        codeLine: 13
                    });
                }
                
                if (i < j) {
                    comparisonCount++;
                    animationQueue.push({
                        type: 'foundRight',
                        left: i,
                        right: j,
                        pivotValue,
                        arrValue: arr[j],
                        description: `找到小于基准的元素：arr[${j}]=${arr[j]} < ${pivotValue}`,
                        codeLine: 15
                    });
                    
                    // 填左坑，挖右坑
                    animationQueue.push({
                        type: 'fillLeftHole',
                        fromIndex: j,
                        toIndex: i,
                        value: arr[j],
                        description: `填左坑：将 arr[${j}]=${arr[j]} 填入 arr[${i}]（左坑），现在 arr[${j}] 成为新坑`,
                        codeLine: 16
                    });
                    
                    arr[i] = arr[j];
                    swapCount++;
                    i++;
                    
                    animationQueue.push({
                        type: 'moveLeftPointer',
                        left: i,
                        right: j,
                        description: `左指针右移：i = ${i}`,
                        codeLine: 17
                    });
                }
                
                // 从左向右找大于基准的元素
                animationQueue.push({
                    type: 'startLeftScan',
                    left: i,
                    right: j,
                    pivotValue,
                    description: `开始从左向右扫描：寻找大于基准值 ${pivotValue} 的元素`,
                    codeLine: 19
                });
                
                while (i < j && arr[i] <= pivotValue) {
                    comparisonCount++;
                    animationQueue.push({
                        type: 'compareLeft',
                        left: i,
                        right: j,
                        pivotValue,
                        arrValue: arr[i],
                        description: `比较：arr[i]=arr[${i}]=${arr[i]} <= 基准值 ${pivotValue}，继续右移 i`,
                        codeLine: 20
                    });
                    i++;
                    
                    animationQueue.push({
                        type: 'moveLeftPointer',
                        left: i,
                        right: j,
                        description: `左指针右移：i = ${i}`,
                        codeLine: 21
                    });
                }
                
                if (i < j) {
                    comparisonCount++;
                    animationQueue.push({
                        type: 'foundLeft',
                        left: i,
                        right: j,
                        pivotValue,
                        arrValue: arr[i],
                        description: `找到大于基准的元素：arr[${i}]=${arr[i]} > ${pivotValue}`,
                        codeLine: 22
                    });
                    
                    // 填右坑，挖左坑
                    animationQueue.push({
                        type: 'fillRightHole',
                        fromIndex: i,
                        toIndex: j,
                        value: arr[i],
                        description: `填右坑：将 arr[${i}]=${arr[i]} 填入 arr[${j}]（右坑），现在 arr[${i}] 成为新坑`,
                        codeLine: 23
                    });
                    
                    arr[j] = arr[i];
                    swapCount++;
                    j--;
                    
                    animationQueue.push({
                        type: 'moveRightPointer',
                        left: i,
                        right: j,
                        description: `右指针左移：j = ${j}`,
                        codeLine: 24
                    });
                }
            }
            
            // 基准归位
            animationQueue.push({
                type: 'pivotPosition',
                pivotIndex: i,
                pivotValue,
                description: `指针相遇：i = j = ${i}，将基准值 ${pivotValue} 放入此位置`,
                codeLine: 26
            });
            
            arr[i] = pivotValue;
            
            animationQueue.push({
                type: 'pivotFinal',
                pivotIndex: i,
                pivotValue,
                description: `基准归位：arr[${i}] = ${pivotValue}，分区完成，基准位置 = ${i}`,
                codeLine: 27
            });
            
            let pivot = i;
            
            // 递归处理左子数组
            recursionStack[recursionStack.length-1].active = false;
            generateQuickSortAnimation(arr, left, pivot - 1, depth + 1);
            
            // 递归处理右子数组
            recursionStack.push({left: pivot + 1, right: right, active: true});
            generateQuickSortAnimation(arr, pivot + 1, right, depth + 1);
            
            // 递归返回
            recursionStack.pop();
            animationQueue.push({
                type: 'recursionExit',
                left, right,
                description: `递归返回：子数组 [${left}, ${right}] 排序完成`,
                codeLine: 6
            });
        }
        
        // 执行动画队列
        function executeAnimation() {
            if (!isAnimating || isPaused || currentStep >= animationQueue.length) {
                if (currentStep >= animationQueue.length) {
                    isAnimating = false;
                    stepDescription.textContent = '排序完成！数组已完全有序。';
                    highlightCodeLine(0);
                    
                    // 绘制最终状态
                    drawArray({
                        sorted: Array.from({length: array.length}, (_, i) => i)
                    });
                }
                return;
            }
            
            const step = animationQueue[currentStep];
            
            // 更新状态显示
            stepDescription.textContent = step.description;
            highlightCodeLine(step.codeLine);
            
            // 更新指针显示
            if (step.left !== undefined) {
                leftPointer.textContent = step.left;
            }
            if (step.right !== undefined) {
                rightPointer.textContent = step.right;
            }
            
            // 更新计数显示
            comparisonCountElem.textContent = comparisonCount;
            swapCountElem.textContent = swapCount;
            
            // 根据步骤类型更新显示
            switch (step.type) {
                case 'selectPivot':
                    pivotValue.textContent = `${step.pivotValue} [索引:${step.pivotIndex}]`;
                    drawArray({
                        pivotIndex: step.pivotIndex,
                        isHole: true
                    });
                    break;
                    
                case 'initPointers':
                    drawArray({
                        pivotIndex: step.left, // 基准在左端
                        isHole: true,
                        leftPointer: step.left,
                        rightPointer: step.right
                    });
                    break;
                    
                case 'compareRight':
                    drawArray({
                        pivotIndex: step.left,
                        isHole: true,
                        leftPointer: step.left,
                        rightPointer: step.right,
                        comparing: {right: step.right}
                    });
                    break;
                    
                case 'foundRight':
                    drawArray({
                        pivotIndex: step.left,
                        isHole: true,
                        leftPointer: step.left,
                        rightPointer: step.right,
                        comparing: {right: step.right}
                    });
                    break;
                    
                case 'fillLeftHole':
                    // 更新数组
                    array[step.toIndex] = step.value;
                    drawArray({
                        pivotIndex: step.fromIndex, // 新坑在右边
                        isHole: true,
                        leftPointer: step.toIndex + 1, // i已经增加了
                        rightPointer: step.fromIndex
                    });
                    break;
                    
                case 'compareLeft':
                    drawArray({
                        pivotIndex: step.right, // 坑在右边
                        isHole: true,
                        leftPointer: step.left,
                        rightPointer: step.right,
                        comparing: {left: step.left}
                    });
                    break;
                    
                case 'foundLeft':
                    drawArray({

<!--检测到代码截断，自动续写中...-->
                        pivotIndex: step.right, // 坑在右边
                        isHole: true,
                        leftPointer: step.left,
                        rightPointer: step.right,
                        comparing: {left: step.left}
                    });
                    break;
                    
                case 'fillRightHole':
                    // 更新数组
                    array[step.toIndex] = step.value;
                    drawArray({
                        pivotIndex: step.fromIndex, // 新坑在左边
                        isHole: true,
                        leftPointer: step.fromIndex,
                        rightPointer: step.toIndex - 1 // j已经减少了
                    });
                    break;
                    
                case 'pivotPosition':
                    drawArray({
                        pivotIndex: step.pivotIndex,
                        leftPointer: step.pivotIndex,
                        rightPointer: step.pivotIndex
                    });
                    break;
                    
                case 'pivotFinal':
                    // 更新数组
                    array[step.pivotIndex] = step.pivotValue;
                    drawArray({
                        sorted: [step.pivotIndex],
                        processed: {start: step.pivotIndex + 1, end: step.right}
                    });
                    break;
                    
                case 'recursionEnter':
                    recursionStack[recursionStack.length-1].active = true;
                    updateRecursionStack();
                    drawArray({
                        processed: {start: step.left, end: step.right}
                    });
                    break;
                    
                case 'recursionExit':
                    recursionStack.pop();
                    updateRecursionStack();
                    drawArray({
                        sorted: Array.from({length: step.right - step.left + 1}, (_, i) => step.left + i)
                    });
                    break;
                    
                case 'baseCase':
                    drawArray();
                    break;
                    
                default:
                    drawArray({
                        leftPointer: step.left,
                        rightPointer: step.right
                    });
            }
            
            currentStep++;
            
            // 继续执行下一个动画步骤
            setTimeout(executeAnimation, animationSpeed);
        }
        
        // 开始排序
        function startSorting() {
            if (isAnimating) return;
            
            // 重置状态
            resetState();
            
            // 解析输入数组
            const input = arrayInput.value.trim();
            if (input) {
                array = input.split(/[, ]+/).map(Number).filter(n => !isNaN(n));
                originalArray = [...array];
            }
            
            if (array.length === 0) {
                array = [6, 1, 8, 4, 9, 3, 7, 2, 5];
                originalArray = [...array];
                arrayInput.value = array.join(', ');
            }
            
            // 生成动画队列
            animationQueue = [];
            comparisonCount = 0;
            swapCount = 0;
            recursionStack = [];
            
            generateQuickSortAnimation([...array], 0, array.length - 1);
            
            // 开始动画
            isAnimating = true;
            isPaused = false;
            currentStep = 0;
            
            pauseBtn.textContent = '暂停';
            stepDescription.textContent = '开始快速排序算法演示...';
            
            executeAnimation();
        }
        
        // 暂停/继续动画
        function togglePause() {
            if (!isAnimating) return;
            
            isPaused = !isPaused;
            pauseBtn.textContent = isPaused ? '继续' : '暂停';
            
            if (!isPaused) {
                executeAnimation();
            }
        }
        
        // 单步执行
        function stepForward() {
            if (!isAnimating) {
                // 如果还没开始，先开始
                startSorting();
                isPaused = true;
                pauseBtn.textContent = '继续';
                return;
            }
            
            if (!isPaused) {
                isPaused = true;
                pauseBtn.textContent = '继续';
            }
            
            if (currentStep < animationQueue.length) {
                const step = animationQueue[currentStep];
                stepDescription.textContent = step.description;
                highlightCodeLine(step.codeLine);
                
                // 执行单步（复制executeAnimation中的相关代码）
                switch (step.type) {
                    case 'selectPivot':
                        pivotValue.textContent = `${step.pivotValue} [索引:${step.pivotIndex}]`;
                        drawArray({
                            pivotIndex: step.pivotIndex,
                            isHole: true
                        });
                        break;
                        
                    case 'initPointers':
                        drawArray({
                            pivotIndex: step.left,
                            isHole: true,
                            leftPointer: step.left,
                            rightPointer: step.right
                        });
                        break;
                        
                    case 'compareRight':
                        drawArray({
                            pivotIndex: step.left,
                            isHole: true,
                            leftPointer: step.left,
                            rightPointer: step.right,
                            comparing: {right: step.right}
                        });
                        break;
                        
                    case 'foundRight':
                        drawArray({
                            pivotIndex: step.left,
                            isHole: true,
                            leftPointer: step.left,
                            rightPointer: step.right,
                            comparing: {right: step.right}
                        });
                        break;
                        
                    case 'fillLeftHole':
                        array[step.toIndex] = step.value;
                        drawArray({
                            pivotIndex: step.fromIndex,
                            isHole: true,
                            leftPointer: step.toIndex + 1,
                            rightPointer: step.fromIndex
                        });
                        break;
                        
                    case 'compareLeft':
                        drawArray({
                            pivotIndex: step.right,
                            isHole: true,
                            leftPointer: step.left,
                            rightPointer: step.right,
                            comparing: {left: step.left}
                        });
                        break;
                        
                    case 'foundLeft':
                        drawArray({
                            pivotIndex: step.right,
                            isHole: true,
                            leftPointer: step.left,
                            rightPointer: step.right,
                            comparing: {left: step.left}
                        });
                        break;
                        
                    case 'fillRightHole':
                        array[step.toIndex] = step.value;
                        drawArray({
                            pivotIndex: step.fromIndex,
                            isHole: true,
                            leftPointer: step.fromIndex,
                            rightPointer: step.toIndex - 1
                        });
                        break;
                        
                    case 'pivotPosition':
                        drawArray({
                            pivotIndex: step.pivotIndex,
                            leftPointer: step.pivotIndex,
                            rightPointer: step.pivotIndex
                        });
                        break;
                        
                    case 'pivotFinal':
                        array[step.pivotIndex] = step.pivotValue;
                        drawArray({
                            sorted: [step.pivotIndex],
                            processed: {start: step.pivotIndex + 1, end: step.right}
                        });
                        break;
                        
                    case 'recursionEnter':
                        recursionStack[recursionStack.length-1].active = true;
                        updateRecursionStack();
                        drawArray({
                            processed: {start: step.left, end: step.right}
                        });
                        break;
                        
                    case 'recursionExit':
                        recursionStack.pop();
                        updateRecursionStack();
                        drawArray({
                            sorted: Array.from({length: step.right - step.left + 1}, (_, i) => step.left + i)
                        });
                        break;
                        
                    default:
                        drawArray({
                            leftPointer: step.left,
                            rightPointer: step.right
                        });
                }
                
                // 更新指针显示
                if (step.left !== undefined) {
                    leftPointer.textContent = step.left;
                }
                if (step.right !== undefined) {
                    rightPointer.textContent = step.right;
                }
                
                // 更新计数
                comparisonCountElem.textContent = comparisonCount;
                swapCountElem.textContent = swapCount;
                
                currentStep++;
                
                if (currentStep >= animationQueue.length) {
                    isAnimating = false;
                    stepDescription.textContent = '排序完成！数组已完全有序。';
                    highlightCodeLine(0);
                    drawArray({
                        sorted: Array.from({length: array.length}, (_, i) => i)
                    });
                }
            }
        }
        
        // 重置状态
        function resetState() {
            isAnimating = false;
            isPaused = false;
            currentStep = 0;
            comparisonCount = 0;
            swapCount = 0;
            recursionStack = [];
            
            array = [...originalArray];
            
            pivotValue.textContent = '-';
            leftPointer.textContent = '-';
            rightPointer.textContent = '-';
            comparisonCountElem.textContent = '0';
            swapCountElem.textContent = '0';
            recursionDepth.textContent = '0';
            
            pauseBtn.textContent = '暂停';
            stepDescription.textContent = '点击"开始排序"按钮启动算法动画演示...';
            
            highlightCodeLine(0);
            updateRecursionStack();
            drawArray();
        }
        
        // 生成随机数组
        function generateRandomArray() {
            const length = Math.floor(Math.random() * 8) + 5; // 5-12个元素
            array = [];
            for (let i = 0; i < length; i++) {
                array.push(Math.floor(Math.random() * 20) + 1);
            }
            originalArray = [...array];
            arrayInput.value = array.join(', ');
            resetState();
        }
        
        // 生成已排序数组
        function generateSortedArray() {
            array = [1, 3, 5, 7, 9, 11, 13, 15, 17];
            originalArray = [...array];
            arrayInput.value = array.join(', ');
            resetState();
        }
        
        // 生成逆序数组
        function generateReverseArray() {
            array = [20, 18, 16, 14, 12, 10, 8, 6, 4, 2];
            originalArray = [...array];
            arrayInput.value = array.join(', ');
            resetState();
        }
        
        // 更新动画速度
        function updateSpeed() {
            const speed = parseInt(speedSlider.value);
            animationSpeed = 600 - (speed * 50); // 从550ms到100ms
            
            const speedLabels = ['极慢', '很慢', '慢', '较慢', '中速', '较快', '快', '很快', '极快', '最快'];
            speedValue.textContent = speedLabels[speed - 1] || '中速';
        }
        
        // 事件监听器
        startBtn.addEventListener('click', startSorting);
        pauseBtn.addEventListener('click', togglePause);
        stepBtn.addEventListener('click', stepForward);
        resetBtn.addEventListener('click', resetState);
        randomBtn.addEventListener('click', generateRandomArray);
        sortedBtn.addEventListener('click', generateSortedArray);
        reverseBtn.addEventListener('click', generateReverseArray);
        speedSlider.addEventListener('input', updateSpeed);
        arrayInput.addEventListener('change', function() {
            const input = this.value.trim();
            if (input) {
                const newArray = input.split(/[, ]+/).map(Number).filter(n => !isNaN(n));
                if (newArray.length > 0) {
                    array = newArray;
                    originalArray = [...array];
                    resetState();
                }
            }
        });
        
        // 窗口大小变化时重新初始化Canvas
        window.addEventListener('resize', initCanvas);
        
        // 初始化
        initCanvas();
        updateSpeed();
        resetState();
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 快速排序算法交互式教学动画使用指南

欢迎使用“快速排序算法动画——挖坑法+分治递归”交互式教学工具！本指南将帮助您充分利用这个精心设计的教学动画，深入理解快速排序算法的核心原理。

### 🎯 功能说明

本动画采用“挖坑法”这一形象化方式，生动展示了快速排序算法的完整执行过程。通过视觉化呈现、代码同步高亮和递归栈可视化，将抽象算法转化为直观、易于理解的动态演示。

### 🚀 主要功能

#### 1. **核心动画演示**
- **挖坑法可视化**：清晰展示基准值如何作为“坑”，左右指针如何交替“填坑”和“挖新坑”
- **实时状态显示**：高亮显示当前基准值、左右指针、比较元素和已排序元素
- **平滑过渡动画**：所有元素移动和状态变化都采用流畅的动画效果

#### 2. **交互控制面板**
- **播放控制**：开始、暂停、单步执行、重置
- **速度调节**：10档速度调节（从“极慢”到“最快”）
- **数据管理**：支持自定义数组输入和多种预设数组

#### 3. **多视图同步**
- **算法代码视图**：伪代码与动画步骤同步高亮
- **递归栈可视化**：动态显示递归调用层次和待处理区间
- **状态信息面板**：实时显示比较次数、交换次数、指针位置等关键信息

#### 4. **数据输入选项**
- **自定义数组**：输入任意数字序列（逗号或空格分隔）
- **预设数组**：
  - 随机数组：每次生成不同的测试数据
  - 已排序数组：观察算法在最优情况下的表现
  - 逆序数组：观察算法在最坏情况下的表现

### ✨ 设计特色

#### 1. **认知友好的视觉设计**
- **颜色编码系统**：
  - 🔴 红色：基准值/坑位
  - 🔵 蓝色：左指针 (i)
  - 🟢 绿色：右指针 (j)
  - 🟡 黄色：当前比较元素
  - 🟠 橙色：已确定位置的元素
  - 🟣 紫色：已处理区间

- **分层信息展示**：从宏观流程到微观操作，层层递进

#### 2. **教学导向的交互设计**
- **渐进式学习**：支持从完整播放到单步调试的学习模式
- **错误预防**：输入验证和合理的默认值设置
- **上下文提示**：每一步都有详细的中文说明

#### 3. **技术实现亮点**
- 响应式Canvas渲染，适配不同屏幕尺寸
- 状态机管理，确保动画逻辑清晰
- 模块化代码结构，便于理解和扩展

### 📚 教学要点

#### 核心概念理解路径

1. **第一阶段：整体认知**
   ```
   建议：先用默认数组完整播放一遍
   目标：了解快速排序“分治-递归”的整体流程
   ```

2. **第二阶段：分区过程详解**
   ```
   建议：使用“单步执行”模式，重点关注：
   1. 基准值选取和“挖坑”操作
   2. 右指针向左扫描，寻找小于基准的元素
   3. “填左坑，挖右坑”操作
   4. 左指针向右扫描，寻找大于基准的元素
   5. “填右坑，挖左坑”操作
   6. 基准值最终归位
   ```

3. **第三阶段：递归过程分析**
   ```
   建议：观察递归栈的变化
   目标：理解递归如何分解问题，以及递归调用的顺序
   ```

4. **第四阶段：不同数据测试**
   ```
   建议：分别测试已排序、逆序、随机数组
   目标：理解算法的时间复杂度特性
   ```

#### 关键教学时刻

- **“坑”的移动**：这是挖坑法的核心，注意观察“坑”如何在左右指针间传递
- **指针相遇**：当i=j时，分区完成，基准值归位
- **递归深度**：观察递归栈的深度变化，理解分治策略
- **比较与交换**：关注计数器的变化，理解算法效率

### 💡 使用建议

#### 给教师的建议

1. **课堂演示**
   - 先完整演示一遍，建立整体印象
   - 分步骤讲解时，使用“单步执行”和“暂停”功能
   - 关键步骤可重复演示，加深学生理解

2. **互动教学**
   - 让学生预测下一步操作
   - 比较不同输入数据的执行差异
   - 引导学生观察递归栈的变化规律

3. **课后练习**
   - 提供不同数组让学生分析执行过程
   - 要求学生描述特定步骤的“挖坑填坑”过程
   - 挑战：让学生手动模拟算法执行

#### 给学习者的建议

1. **学习路径**
   ```
   初学者：观看完整动画 → 单步学习分区过程 → 理解递归
   进阶者：分析不同数据表现 → 思考算法优化 → 尝试实现代码
   ```

2. **学习技巧**
   - 善用“单步执行”功能，在关键步骤停下来思考
   - 关注颜色变化，建立视觉记忆
   - 将动画步骤与代码行对应起来
   - 尝试自己预测下一步，再验证

3. **调试思维培养**
   - 如果某一步不理解，重置后重新单步执行
   - 观察递归栈，理解函数调用关系
   - 记录比较和交换次数，分析算法效率

#### 最佳实践组合

1. **完整学习流程**：
   ```
   1. 观看默认数组的完整动画
   2. 单步执行理解分区细节
   3. 观察递归栈理解递归过程
   4. 测试不同输入数据
   5. 关闭动画，尝试手动模拟
   ```

2. **重点突破策略**：
   - 对“挖坑法”不理解？重点关注步骤3-6
   - 对递归困惑？专注观察递归栈变化
   - 对算法效率好奇？比较不同数据的执行统计

### 🎓 教学价值

本工具不仅展示了算法执行过程，更重要的是：

1. **建立直观理解**：将抽象算法转化为具体视觉形象
2. **培养计算思维**：通过交互探索，理解分治递归思想
3. **连接理论与实现**：架起算法思想与代码实现之间的桥梁
4. **激发学习兴趣**：动态、交互式的学习体验比静态文字更有吸引力

### 🔧 技术说明

- 支持现代浏览器（Chrome、Firefox、Edge、Safari）
- 完全本地运行，无需网络连接
- 响应式设计，适配桌面和移动设备
- 开源代码结构，可供教学和二次开发使用

---

**开始您的快速排序探索之旅吧！** 无论您是算法初学者还是希望深化理解的进阶者，这个交互式工具都将为您提供独特而深入的学习体验。通过亲手操作、观察思考，您将真正掌握快速排序这一经典算法的精髓。

祝您学习愉快，收获满满！ 🚀