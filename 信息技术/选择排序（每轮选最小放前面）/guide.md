# 需求：选择排序（每轮选最小放前面）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初次学习排序算法的编程初学者或中学生。他们可能对抽象的逻辑和“循环嵌套”、“索引交换”等概念感到困难。
2.  **核心需求**：
    *   **直观理解算法流程**：用户需要清晰地看到选择排序“每一轮找到最小值，并将其放到本轮最前面”这一核心思想是如何一步步执行的。
    *   **区分不同阶段**：用户需要明确区分“当前未排序序列”、“正在比较的元素”、“当前找到的最小值”以及“已排序序列”这几个关键状态。
    *   **理解关键操作**：用户需要重点理解“寻找最小值”的扫描过程，以及“交换位置”这一操作的必要性和执行方式。
    *   **控制学习节奏**：用户需要能够暂停、单步执行或重置动画，以便有足够的时间观察和思考每一步的变化。
3.  **潜在难点**：用户容易混淆“比较”和“交换”，可能不理解为什么找到最小值后需要执行一次交换，以及交换后序列状态的变化。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念解构**：
    *   **核心思想**：将排序过程分解为多轮。在每一轮中，从“未排序部分”中找到最小的元素，将其与“未排序部分”的第一个元素交换位置。该元素即加入“已排序部分”。
    *   **关键变量**：用高亮和标签明确标识 `当前轮次 (i)`、`最小值的索引 (minIndex)`、`当前比较元素的索引 (j)`。

*   **遵循认知规律**：
    *   **从具体到抽象**：使用高度不同的柱子（或数值标签）代表待排序数据，将抽象的数组索引和数值可视化。
    *   **分步演示**：将算法严格分解为单步动作（如：初始化最小值索引 -> 开始扫描 -> 比较 -> 更新最小值 -> 完成扫描 -> 执行交换），避免信息过载。
    *   **强调状态变化**：通过颜色和位置的变化，强化“未排序区”、“已排序区”的扩张，以及元素“找到归宿”的过程。

*   **交互设计**：
    *   **流程控制**：提供“上一步”、“下一步”、“播放/暂停”、“重置”按钮，让用户完全掌控学习节奏。
    *   **关键提示**：在动画区域旁设置一个“状态说明”面板，用文字动态描述当前步骤在做什么（例如：“第2轮：正在比较索引3和当前最小值索引1…”）。
    *   **代码联动（可选高阶）**：可以同步高亮当前正在执行的伪代码行，建立视觉操作与程序逻辑的直接联系。

*   **视觉呈现**：
    *   **主舞台**：一个水平排列的柱子序列，清晰展示所有元素。
    *   **颜色编码系统**：
        *   **红色**：当前轮次找到的“最小值”（在扫描过程中动态更新）。
        *   **蓝色**：正在与最小值进行比较的“当前扫描元素”。
        *   **绿色**：已经就位的“已排序部分”。
        *   **灰色/浅色**：尚未参与本轮排序的“未排序部分”。
        *   **黄色高亮**：用于标记当前准备交换的两个位置（本轮未排序部分的第一个位置，和找到的最小值位置）。
    *   **动态效果**：交换时使用平滑的位置移动动画；“比较”时可以使用轻微的脉冲或缩放效果来吸引注意力。

#### 配色方案选择
选择对比鲜明、符合认知习惯且柔和的配色，确保可读性和舒适度。
*   **背景**：浅灰色 (`#f5f5f5`) 或白色，保持干净。
*   **未排序元素**：浅灰色 (`#e0e0e0`)。
*   **已排序元素**：温和的绿色 (`#a5d6a7`)，象征“已完成”、“正确位置”。
*   **当前最小值**：醒目的红色 (`#ef5350`)，代表“关键目标”。
*   **当前扫描元素**：蓝色 (`#42a5f5`)，代表“正在活动”。
*   **交换高亮**：黄色 (`#fff176`)，代表“注意，即将发生操作”。
*   **文本与边框**：深灰色 (`#424242`)。
*   **按钮**：采用扁平化设计，主操作按钮（如下一步）用蓝色 (`#2196f3`)，重置用灰色，播放/暂停用绿色/橙色。

#### 交互功能列表
1.  **数据初始化**：
    *   预设一组随机数据（如柱子高度/数字）。
    *   提供“随机生成”按钮，重新生成一组数据。
    *   （可选）允许用户手动输入一组自定义数字。
2.  **核心流程控制**：
    *   **下一步**：执行算法的一个**最小步骤**（如一次比较，或一次交换）。
    *   **上一步**：回退到上一个步骤。
    *   **播放/暂停**：自动连续执行步骤，用户可随时暂停。
    *   **重置**：将动画恢复到初始未排序状态。
3.  **信息反馈面板**：
    *   **状态说明**：用自然语言描述当前正在进行的操作。
    *   **变量状态**：实时显示 `当前轮次 i`、`最小值索引 minIndex`、`当前比较索引 j` 的值。
    *   **伪代码展示**：同步高亮算法伪代码的当前行。
4.  **视觉标记**：
    *   所有元素上方或下方显示其索引（0, 1, 2...）。
    *   所有元素上显示其数值（柱子高度或数字标签）。
    *   通过颜色和可能的连接线，清晰标出“比较”关系和“交换”关系。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>选择排序算法动画演示</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background-color: #f5f5f5;
            color: #424242;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #e0e0e0;
        }

        h1 {
            color: #2196f3;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #757575;
            font-size: 1.1em;
        }

        .container {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        @media (min-width: 900px) {
            .container {
                flex-direction: row;
            }
            
            .left-panel {
                flex: 1;
            }
            
            .right-panel {
                flex: 1;
            }
        }

        .panel {
            background-color: white;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        h2 {
            color: #424242;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e0e0e0;
        }

        .algorithm-explanation {
            margin-bottom: 25px;
        }

        .algorithm-explanation p {
            margin-bottom: 15px;
        }

        .pseudo-code {
            background-color: #f8f9fa;
            border-left: 4px solid #2196f3;
            padding: 15px;
            font-family: 'Consolas', 'Monaco', monospace;
            line-height: 1.8;
            margin-bottom: 25px;
            border-radius: 0 5px 5px 0;
        }

        .pseudo-code .highlight {
            background-color: #fff176;
            padding: 2px 4px;
            border-radius: 3px;
            font-weight: bold;
        }

        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 25px;
        }

        button {
            padding: 12px 20px;
            border: none;
            border-radius: 6px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        button:active {
            transform: translateY(0);
        }

        .btn-primary {
            background-color: #2196f3;
            color: white;
        }

        .btn-primary:hover {
            background-color: #0d8bf2;
        }

        .btn-secondary {
            background-color: #42a5f5;
            color: white;
        }

        .btn-secondary:hover {
            background-color: #2b97f3;
        }

        .btn-success {
            background-color: #4caf50;
            color: white;
        }

        .btn-success:hover {
            background-color: #3d8b40;
        }

        .btn-warning {
            background-color: #ff9800;
            color: white;
        }

        .btn-warning:hover {
            background-color: #e68900;
        }

        .btn-reset {
            background-color: #757575;
            color: white;
        }

        .btn-reset:hover {
            background-color: #616161;
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 10px;
        }

        .speed-control label {
            font-weight: 600;
        }

        .speed-control input {
            flex-grow: 1;
        }

        .visualization-container {
            position: relative;
            height: 400px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            overflow: hidden;
            background-color: white;
        }

        #animation-canvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .status-panel {
            margin-top: 25px;
            padding: 20px;
            background-color: #f8f9fa;
            border-radius: 8px;
            border-left: 4px solid #a5d6a7;
        }

        .status-title {
            font-weight: 700;
            color: #2e7d32;
            margin-bottom: 10px;
            font-size: 1.1em;
        }

        .status-content {
            font-size: 1.05em;
            line-height: 1.8;
        }

        .variables {
            display: flex;
            gap: 20px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .variable {
            background-color: white;
            padding: 10px 15px;
            border-radius: 6px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
            min-width: 120px;
        }

        .variable-name {
            font-weight: 700;
            color: #2196f3;
            margin-bottom: 5px;
        }

        .variable-value {
            font-size: 1.3em;
            font-weight: 700;
            color: #ef5350;
            text-align: center;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 25px;
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
        }

        .legend-text {
            font-size: 0.9em;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #e0e0e0;
            color: #757575;
            font-size: 0.9em;
        }
    </style>
</head>
<body>
    <header>
        <h1>选择排序算法动画演示</h1>
        <p class="subtitle">每轮选择最小值放到前面 - 可视化理解排序过程</p>
    </header>

    <div class="container">
        <div class="left-panel">
            <div class="panel">
                <h2>算法原理</h2>
                <div class="algorithm-explanation">
                    <p><strong>选择排序</strong>是一种简单直观的排序算法。它的工作原理是：</p>
                    <p>1. 首先在未排序序列中找到最小（大）元素，存放到排序序列的起始位置。</p>
                    <p>2. 再从剩余未排序元素中继续寻找最小（大）元素，然后放到已排序序列的末尾。</p>
                    <p>3. 重复第二步，直到所有元素均排序完毕。</p>
                    <p>本动画演示的是<strong>每轮选择最小值放到前面</strong>的版本。</p>
                </div>

                <h2>伪代码</h2>
                <div class="pseudo-code" id="pseudo-code">
                    for i = 0 to n-1:<br>
                    &nbsp;&nbsp;minIndex = i<br>
                    &nbsp;&nbsp;for j = i+1 to n:<br>
                    &nbsp;&nbsp;&nbsp;&nbsp;if array[j] < array[minIndex]:<br>
                    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;minIndex = j<br>
                    &nbsp;&nbsp;swap(array[i], array[minIndex])
                </div>

                <h2>控制面板</h2>
                <div class="controls">
                    <button id="prev-btn" class="btn-secondary">
                        <span>◀</span> 上一步
                    </button>
                    <button id="next-btn" class="btn-primary">
                        下一步 <span>▶</span>
                    </button>
                    <button id="play-pause-btn" class="btn-success">
                        <span id="play-icon">▶</span> <span id="play-text">播放</span>
                    </button>
                    <button id="reset-btn" class="btn-reset">
                        <span>↺</span> 重置
                    </button>
                    <button id="randomize-btn" class="btn-warning">
                        <span>🎲</span> 随机数据
                    </button>
                </div>

                <div class="speed-control">
                    <label for="speed-slider">动画速度:</label>
                    <input type="range" id="speed-slider" min="1" max="10" value="5">
                    <span id="speed-value">中速</span>
                </div>
            </div>

            <div class="panel status-panel">
                <div class="status-title">当前状态</div>
                <div class="status-content" id="status-text">
                    点击"下一步"开始排序演示...
                </div>
                
                <div class="variables">
                    <div class="variable">
                        <div class="variable-name">当前轮次 (i)</div>
                        <div class="variable-value" id="var-i">0</div>
                    </div>
                    <div class="variable">
                        <div class="variable-name">最小值索引 (minIndex)</div>
                        <div class="variable-value" id="var-min">0</div>
                    </div>
                    <div class="variable">
                        <div class="variable-name">比较索引 (j)</div>
                        <div class="variable-value" id="var-j">0</div>
                    </div>
                </div>
            </div>
        </div>

        <div class="right-panel">
            <div class="panel">
                <h2>排序过程可视化</h2>
                <div class="visualization-container">
                    <canvas id="animation-canvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #a5d6a7;"></div>
                        <div class="legend-text">已排序</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e0e0e0;"></div>
                        <div class="legend-text">未排序</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ef5350;"></div>
                        <div class="legend-text">当前最小值</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #42a5f5;"></div>
                        <div class="legend-text">正在比较</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #fff176;"></div>
                        <div class="legend-text">交换位置</div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>选择排序算法动画演示 | 设计用于教学目的 | 时间复杂度: O(n²)</p>
    </footer>

    <script>
        // 全局变量
        let array = [];
        let arraySize = 10;
        let animationSteps = [];
        let currentStep = 0;
        let isPlaying = false;
        let playInterval;
        let animationSpeed = 300; // 毫秒
        let isAnimating = false;
        
        // 颜色定义
        const colors = {
            sorted: '#a5d6a7',      // 已排序 - 绿色
            unsorted: '#e0e0e0',    // 未排序 - 浅灰色
            currentMin: '#ef5350',  // 当前最小值 - 红色
            comparing: '#42a5f5',   // 正在比较 - 蓝色
            swapping: '#fff176',    // 交换位置 - 黄色
            default: '#757575'      // 默认 - 灰色
        };
        
        // 算法状态
        let algorithmState = {
            i: 0,           // 当前轮次
            minIndex: 0,    // 当前最小值索引
            j: 0,           // 当前比较索引
            stepDescription: '初始化',
            isComparing: false,
            isSwapping: false,
            swapFrom: -1,
            swapTo: -1,
            sortedIndices: []  // 已排序的索引
        };
        
        // 初始化
        function init() {
            generateRandomArray();
            generateAnimationSteps();
            setupCanvas();
            draw();
            updateStatus();
            updatePseudoCodeHighlight();
        }
        
        // 生成随机数组
        function generateRandomArray() {
            array = [];
            for (let i = 0; i < arraySize; i++) {
                array.push(Math.floor(Math.random() * 90) + 10); // 10-99之间的随机数
            }
            
            // 重置算法状态
            algorithmState = {
                i: 0,
                minIndex: 0,
                j: 1,
                stepDescription: '初始化数组',
                isComparing: false,
                isSwapping: false,
                swapFrom: -1,
                swapTo: -1,
                sortedIndices: []
            };
            
            currentStep = 0;
            updateVariablesDisplay();
        }
        
        // 生成动画步骤
        function generateAnimationSteps() {
            animationSteps = [];
            const arr = [...array];
            const steps = [];
            const sortedIndices = [];
            
            // 复制数组用于模拟
            const simArray = [...arr];
            const n = simArray.length;
            
            // 初始状态
            steps.push({
                type: 'init',
                i: 0,
                minIndex: 0,
                j: 1,
                description: '初始化：准备开始第一轮排序',
                sortedIndices: [...sortedIndices]
            });
            
            // 选择排序算法步骤生成
            for (let i = 0; i < n - 1; i++) {
                let minIndex = i;
                
                // 步骤：开始新的一轮，设置minIndex为i
                steps.push({
                    type: 'newRound',
                    i: i,
                    minIndex: i,
                    j: i + 1,
                    description: `第${i+1}轮：设置最小值为索引${i}（值：${simArray[i]}）`,
                    sortedIndices: [...sortedIndices]
                });
                
                // 内层循环：寻找最小值
                for (let j = i + 1; j < n; j++) {
                    // 步骤：比较arr[j]和当前最小值
                    steps.push({
                        type: 'compare',
                        i: i,
                        minIndex: minIndex,
                        j: j,
                        description: `比较：索引${j}的值${simArray[j]} < 当前最小值${simArray[minIndex]}?`,
                        sortedIndices: [...sortedIndices]
                    });
                    
                    if (simArray[j] < simArray[minIndex]) {
                        minIndex = j;
                        
                        // 步骤：找到新的最小值
                        steps.push({
                            type: 'newMin',
                            i: i,
                            minIndex: minIndex,
                            j: j,
                            description: `发现新的最小值：索引${minIndex}（值：${simArray[minIndex]}）`,
                            sortedIndices: [...sortedIndices]
                        });
                    }
                }
                
                // 如果最小值不是当前位置，需要交换
                if (minIndex !== i) {
                    // 步骤：准备交换
                    steps.push({
                        type: 'prepareSwap',
                        i: i,
                        minIndex: minIndex,
                        j: -1,
                        description: `准备交换：将最小值${simArray[minIndex]}放到位置${i}`,
                        sortedIndices: [...sortedIndices],
                        swapFrom: minIndex,
                        swapTo: i
                    });
                    
                    // 执行交换（在模拟数组中）
                    [simArray[i], simArray[minIndex]] = [simArray[minIndex], simArray[i]];
                    
                    // 步骤：完成交换
                    steps.push({
                        type: 'swap',
                        i: i,
                        minIndex: minIndex,
                        j: -1,
                        description: `完成交换：索引${i}和索引${minIndex}的值已交换`,
                        sortedIndices: [...sortedIndices],
                        swapFrom: minIndex,
                        swapTo: i
                    });
                } else {
                    // 步骤：无需交换
                    steps.push({
                        type: 'noSwap',
                        i: i,
                        minIndex: minIndex,
                        j: -1,
                        description: `最小值已在正确位置，无需交换`,
                        sortedIndices: [...sortedIndices]
                    });
                }
                
                // 本轮结束，i位置已排序
                sortedIndices.push(i);
                
                // 步骤：本轮完成
                steps.push({
                    type: 'roundComplete',
                    i: i,
                    minIndex: minIndex,
                    j: -1,
                    description: `第${i+1}轮完成：索引${i}已排序`,
                    sortedIndices: [...sortedIndices]
                });
            }
            
            // 最后一个元素自动排序
            sortedIndices.push(n - 1);
            
            // 步骤：排序完成
            steps.push({
                type: 'complete',
                i: n - 1,
                minIndex: -1,
                j: -1,
                description: '排序完成！所有元素已按升序排列',
                sortedIndices: [...sortedIndices]
            });
            
            animationSteps = steps;
        }
        
        // 设置Canvas
        function setupCanvas() {
            const canvas = document.getElementById('animation-canvas');
            const container = document.querySelector('.visualization-container');
            
            // 设置Canvas尺寸为容器尺寸
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        
        // 绘制函数
        function draw() {
            const canvas = document.getElementById('animation-canvas');
            const ctx = canvas.getContext('2d');
            const width = canvas.width;
            const height = canvas.height;
            
            // 清除画布
            ctx.clearRect(0, 0, width, height);
            
            // 计算柱状图参数
            const barCount = array.length;
            const barWidth = Math.min(60, (width - 40) / barCount);
            const spacing = (width - barWidth * barCount) / (barCount + 1);
            const maxValue = Math.max(...array);
            const scale = (height - 120) / maxValue; // 留出空间给标签
            
            // 绘制每个柱子
            for (let i = 0; i < barCount; i++) {
                const x = spacing + i * (barWidth + spacing);
                const barHeight = array[i] * scale;
                const y = height - 80 - barHeight;
                
                // 确定柱子颜色
                let color = colors.unsorted;
                
                if (algorithmState.sortedIndices.includes(i)) {
                    color = colors.sorted; // 已排序
                } else if (algorithmState.isSwapping && 
                          (i === algorithmState.swapFrom || i === algorithmState.swapTo)) {
                    color = colors.swapping; // 交换位置
                } else if (i === algorithmState.minIndex) {
                    color = colors.currentMin; // 当前最小值
                } else if (algorithmState.isComparing && i === algorithmState.j) {
                    color = colors.comparing; // 正在比较
                }
                
                // 绘制柱子
                ctx.fillStyle = color;
                ctx.fillRect(x, y, barWidth, barHeight);
                
                // 绘制柱子边框
                ctx.strokeStyle = '#424242';
                ctx.lineWidth = 1;
                ctx.strokeRect(x, y, barWidth, barHeight);
                
                // 绘制数值
                ctx.fillStyle = '#424242';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(array[i], x + barWidth / 2, y - 10);
                
                // 绘制索引
                ctx.fillStyle = '#757575';
                ctx.font = '14px Arial';
                ctx.fillText(`[${i}]`, x + barWidth / 2, height - 30);
                
                // 如果当前是i位置，添加标记
                if (i === algorithmState.i) {
                    ctx.fillStyle = '#2196f3';
                    ctx.font = 'bold 14px Arial';
                    ctx.fillText(`i=${i}`, x + barWidth / 2, height - 50);
                }
            }
            
            // 绘制当前步骤说明
            ctx.fillStyle = '#424242';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'left';
            ctx.fillText(`步骤: ${currentStep + 1}/${animationSteps.length}`, 20, 40);
            
            // 绘制算法状态
            ctx.font = '16px Arial';
            ctx.fillText(algorithmState.stepDescription, 20, 70);
        }
        
        // 更新状态显示
        function updateStatus() {
            const statusElement = document.getElementById('status-text');
            if (currentStep < animationSteps.length) {
                const step = animationSteps[currentStep];
                statusElement.textContent = step.description;
                
                // 更新算法状态
                algorithmState.i = step.i;
                algorithmState.minIndex = step.minIndex;
                algorithmState.j = step.j;
                algorithmState.stepDescription = step.description;
                algorithmState.sortedIndices = step.sortedIndices || [];
                
                // 设置比较和交换状态
                algorithmState.isComparing = step.type === 'compare';
                algorithmState.isSwapping = step.type === 'prepareSwap' || step.type === 'swap';
                
                if (step.swapFrom !== undefined && step.swapTo !== undefined) {
                    algorithmState.swapFrom = step.swapFrom;
                    algorithmState.swapTo = step.swapTo;
                } else {
                    algorithmState.swapFrom = -1;
                    algorithmState.swapTo = -1;
                }
            }
            
            updateVariablesDisplay();
            updatePseudoCodeHighlight();
            draw();
        }
        
        // 更新变量显示
        function updateVariablesDisplay() {
            document.getElementById('var-i').textContent = algorithmState.i;
            document.getElementById('var-min').textContent = algorithmState.minIndex;
            document.getElementById('var-j').textContent = algorithmState.j >= 0 ? algorithmState.j : '-';
        }
        
        // 更新伪代码高亮
        function updatePseudoCodeHighlight() {
            const pseudoElement = document.getElementById('pseudo-code');
            let pseudoCode = `for i = 0 to n-1:<br>
&nbsp;&nbsp;minIndex = i<br>
&nbsp;&nbsp;for j = i+1 to n:<br>
&nbsp;&nbsp;&nbsp;&nbsp;if array[j] < array[minIndex]:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;minIndex = j<br>
&nbsp;&nbsp;swap(array[i], array[minIndex])`;
            
            // 根据当前步骤类型高亮相应的代码行
            if (currentStep < animationSteps.length) {
                const step = animationSteps[currentStep];
                
                // 根据步骤类型高亮不同的行
                if (step.type === 'init' || step.type === 'newRound') {
                    pseudoCode = pseudoCode.replace('for i = 0 to n-1:', '<span class="highlight">for i = 0 to n-1:</span>');
                    pseudoCode = pseudoCode.replace('minIndex = i', '<span class="highlight">minIndex = i</span>');
                } else if (step.type === 'compare' || step.type === 'newMin') {
                    pseudoCode = pseudoCode.replace('for j = i+1 to n:', '<span class="highlight">for j = i+1 to n:</span>');
                    pseudoCode = pseudoCode.replace('if array[j] < array[minIndex]:', '<span class="highlight">if array[j] < array[minIndex]:</span>');
                    
                    if (step.type === 'newMin') {
                        pseudoCode = pseudoCode.replace('minIndex = j', '<span class="highlight">minIndex = j</span>');
                    }
                } else if (step.type === 'prepareSwap' || step.type === 'swap' || step.type === 'noSwap') {
                    pseudoCode = pseudoCode.replace('swap(array[i], array[minIndex])', '<span class="highlight">swap(array[i], array[minIndex])</span>');
                } else if (step.type === 'roundComplete') {
                    // 完成一轮，回到外层循环
                    pseudoCode = pseudoCode.replace('for i = 0 to n-1:', '<span class="highlight">for i = 0 to n-1:</span>');
                }
            }
            
            pseudoElement.innerHTML = pseudoCode;
        }
        
        // 执行下一步
        function nextStep() {
            if (currentStep < animationSteps.length - 1) {
                currentStep++;
                updateStatus();
                
                // 如果是最后一步，停止播放
                if (currentStep === animationSteps.length - 1 && isPlaying) {
                    togglePlayPause();
                }
            }
        }
        
        // 执行上一步
        function prevStep() {
            if (currentStep > 0) {
                currentStep--;
                updateStatus();
            }
        }
        
        // 切换播放/暂停
        function togglePlayPause() {
            const playIcon = document.getElementById('play-icon');
            const playText = document.getElementById('play-text');
            
            if (isPlaying) {
                // 停止播放
                clearInterval(playInterval);
                playIcon.textContent = '▶';
                playText.textContent = '播放';
                isPlaying = false;
            } else {
                // 开始播放
                playIcon.textContent = '⏸';
                playText.textContent = '暂停';
                isPlaying = true;
                
                // 如果已经是最后一步，重置到第一步
                if (currentStep >= animationSteps.length - 1) {
                    currentStep = 0;
                    updateStatus();
                }
                
                playInterval = setInterval(() => {
                    if (currentStep < animationSteps.length - 1) {
                        nextStep();
                    } else {
                        togglePlayPause(); // 自动停止
                    }
                }, animationSpeed);
            }
        }
        
        // 重置动画
        function resetAnimation() {
            // 如果正在播放，先停止
            if (isPlaying) {
                togglePlayPause();
            }
            
            currentStep = 0;
            updateStatus();
        }
        
        // 更新动画速度
        function updateSpeed(value) {
            // 将滑块值(1-10)转换为速度值(600ms-100ms)
            animationSpeed = 650 - (value * 55);
            
            // 更新显示
            const speedText = document.getElementById('speed-value');
            if (value <= 3) {
                speedText.textContent = '慢速';
            } else if (value <= 7) {
                speedText.textContent = '中速';
            } else {
                speedText.textContent = '快速';
            }
            
            // 如果正在播放，重新设置间隔
            if (isPlaying) {
                clearInterval(playInterval);
                playInterval = setInterval(() => {
                    if (currentStep < animationSteps.length - 1) {
                        nextStep();
                    } else {
                        togglePlayPause();
                    }
                }, animationSpeed);
            }
        }
        
        // 事件监听器设置
        function setupEventListeners() {
            // 按钮事件
            document.getElementById('prev-btn').addEventListener('click', prevStep);
            document.getElementById('next-btn').addEventListener('click', nextStep);
            document.getElementById('play-pause-btn').addEventListener('click', togglePlayPause);
            document.getElementById('reset-btn').addEventListener('click', resetAnimation);
            document.getElementById('randomize-btn').addEventListener('click', () => {
                generateRandomArray();
                generateAnimationSteps();
                resetAnimation();
            });
            
            // 速度滑块事件
            const speedSlider = document.getElementById('speed-slider');
            speedSlider.addEventListener('input', () => {
                updateSpeed(parseInt(speedSlider.value));
            });
            
            // 窗口大小变化时调整Canvas
            window.addEventListener('resize', () => {
                setupCanvas();
                draw();
            });
            
            // 键盘快捷键
            document.addEventListener('keydown', (e) => {
                // 防止在输入框内触发
                if (e.target.tagName === 'INPUT') return;
                
                switch(e.key) {
                    case 'ArrowLeft':
                        e.preventDefault();
                        prevStep();
                        break;
                    case 'ArrowRight':
                    case ' ':
                        e.preventDefault();
                        nextStep();
                        break;
                    case 'p':
                    case 'P':
                        e.preventDefault();
                        togglePlayPause();
                        break;
                    case 'r':
                    case 'R':
                        e.preventDefault();
                        resetAnimation();
                        break;
                }
            });
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', () => {
            init();
            setupEventListeners();
            
            // 初始速度设置
            const speedSlider = document.getElementById('speed-slider');
            updateSpeed(parseInt(speedSlider.value));
        });
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

欢迎使用“选择排序算法动画演示”交互式教学工具！本指南将帮助您充分利用这个精心设计的动画，深入理解选择排序算法的核心原理与执行过程。

### 一、 功能说明

本动画将抽象的选择排序算法转化为直观、动态的视觉过程。它通过**颜色编码、分步执行、状态反馈**和**代码联动**，将算法中关键的“寻找最小值”和“交换位置”操作可视化，旨在降低学习曲线，帮助您建立清晰的算法思维模型。

### 二、 主要功能

1.  **核心流程控制**
    *   **下一步 (▶)**：执行算法的一个最小逻辑步骤（如一次比较或一次交换），让您精细观察每一步的变化。
    *   **上一步 (◀)**：回退到上一个步骤，方便回顾和对比。
    *   **播放/暂停**：自动连续执行所有步骤，您可以随时暂停以观察细节。
    *   **重置 (↺)**：将动画恢复到初始的未排序状态。
    *   **随机数据 (🎲)**：生成一组全新的随机数据，用于观察算法在不同输入下的表现。

2.  **可视化呈现**
    *   **柱状图**：每个柱子的高度代表数值大小，直观展示数据。
    *   **颜色编码系统**：
        *   **绿色**：已排序部分，表示元素已在其最终正确位置。
        *   **浅灰色**：未排序部分，等待处理。
        *   **红色**：当前轮次中找到的**最小值**。
        *   **蓝色**：正在与最小值进行**比较**的元素。
        *   **黄色**：即将发生**交换**的两个位置。
    *   **动态标记**：实时显示每个元素的索引和数值，并用标签高亮当前轮次 `i`。

3.  **信息反馈面板**
    *   **状态说明**：用自然语言动态描述当前正在执行的操作（如“第2轮：正在比较索引3和当前最小值索引1…”）。
    *   **变量监视器**：实时显示算法核心变量 `i`（当前轮次）、`minIndex`（最小值索引）、`j`（比较索引）的值。
    *   **伪代码高亮**：右侧伪代码区域会同步高亮当前正在执行的代码行，建立视觉操作与程序逻辑的直接联系。
    *   **进度指示**：显示当前步骤序号和总步骤数。

4.  **自定义设置**
    *   **动画速度控制**：通过滑块调整动画播放速度（慢速/中速/快速），以适应不同的学习节奏。

### 三、 设计特色

1.  **教学驱动的交互设计**：控制逻辑严格遵循算法步骤分解，确保每一步都对应一个明确的算法动作，避免信息跳跃。
2.  **多通道信息同步**：视觉（颜色/位置）、文本（状态描述）、数据（变量值）、代码（高亮）四者同步更新，强化理解。
3.  **认知负荷管理**：通过清晰的图例和分步演示，有效降低了同时理解算法逻辑、数据变化和程序代码的认知负担。
4.  **错误容忍与探索支持**：“上一步”和“重置”功能允许您大胆尝试、反复观察，营造安全的探索式学习环境。

### 四、 教学要点

在使用本动画学习或教学时，请重点关注以下核心概念：

1.  **“轮”的概念**：观察每一轮（对应外层循环 `i`）如何将未排序部分的范围逐步缩小。绿色区域的扩张是算法进展的直观体现。
2.  **“扫描找最小”过程**：在内层循环中，注意 `j` 如何从左向右扫描，`minIndex` 如何随着更小值的发现而更新（红色标记的跳动）。这是选择排序的核心操作。
3.  **“交换”的必要性**：理解为什么找到最小值后，需要将其与未排序部分的第一个元素（位置 `i`）交换。交换后，位置 `i` 的元素即归入已排序部分（变绿）。
4.  **算法的不稳定性**：观察当存在相等值时，选择排序可能改变其相对顺序（因为交换可能将后面的相等值换到前面），理解“不稳定排序”的含义。
5.  **时间复杂度 O(n²) 的直观体现**：通过观察随着数据量增加，所需的比较和交换步骤数如何平方级增长，直观感受算法效率。

### 五、 使用建议

1.  **初学者学习路径**：
    *   **第一步**：使用“播放”功能，以较慢速度完整观看一遍排序过程，对算法流程建立整体印象。
    *   **第二步**：点击“重置”，使用“下一步”按钮**手动单步执行**。在每一步，都先观察**颜色变化**和**状态描述**，然后思考“为什么会这样”，再点击下一步验证。
    *   **第三步**：重点关注第一轮和最后一轮的完整过程，理解算法开始和结束时的状态。
    *   **第四步**：生成“随机数据”，尝试预测下一步会发生什么，再用动画验证你的预测。

2.  **教师教学建议**：
    *   **演示模式**：可连接投影，边操作边讲解，利用高亮和状态描述引导学生视线和思路。
    *   **提问引导**：在关键步骤（如发现新的最小值、准备交换前）暂停，提问学生：“接下来会发生什么？为什么？”
    *   **对比教学**：可与冒泡排序等算法的动画进行对比，突出选择排序“每轮只交换一次”的特点。

3.  **键盘快捷键**（提升操作效率）：
    *   **左箭头 (←)**：上一步
    *   **右箭头 (→) 或 空格键**：下一步
    *   **P键**：播放/暂停
    *   **R键**：重置

希望这份指南能帮助您更好地利用这个交互式工具。祝您在学习选择排序算法的旅程中，收获清晰的理解与探索的乐趣！