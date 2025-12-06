# 需求：二分查找（左右指针夹逼动画，旋转版也超清晰）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为学习算法与数据结构的学生（大学或高中阶段），以及需要重温该算法的程序员。
2.  **核心需求**：
    *   **理解算法流程**：直观地看到二分查找如何通过不断缩小搜索范围来定位目标值。
    *   **掌握关键概念**：清晰理解“有序数组”、“左指针（L）”、“右指针（R）”、“中间指针（M）”、“比较与决策”以及“循环不变式”或“夹逼”思想。
    *   **观察边界条件**：看到当目标值不存在、位于数组两端或中间时，指针的移动和循环终止条件。
    *   **动态与多角度**：希望动画不是静态的步骤图，而是有连贯的视觉引导。特别提到“旋转版”，表明用户希望从不同视角（如将数组视为环形或从时间维度展开）加深理解，避免视觉疲劳和思维定式。
3.  **潜在痛点**：
    *   传统左右指针动画在一条直线上，步骤多了容易眼花。
    *   对“夹逼”过程的动态感和空间感体会不深。
    *   难以在脑中构建算法每一步的状态变化。

#### 教学设计思路
*   **核心概念**：
    1.  **前提**：数组必须**有序**（升序）。
    2.  **核心操作**：取中间索引 `mid`，比较 `arr[mid]` 与目标值 `target`。
    3.  **决策与移动**：
        *   `arr[mid] == target`：查找成功。
        *   `arr[mid] < target`：目标在右侧，`left = mid + 1`。
        *   `arr[mid] > target`：目标在左侧，`right = mid - 1`。
    4.  **终止条件**：`left > right`，查找失败。
    5.  **“夹逼”隐喻**：左、右指针像两堵墙向中间移动，逐步挤压掉不可能的区域，直到找到目标或区域消失。

*   **认知规律**：
    1.  **从具体到抽象**：先展示一个完整的、有数值的例子动画，再提炼出通用的伪代码或步骤。
    2.  **聚焦与引导**：每一步高亮当前关注的三个元素（`left`, `mid`, `right` 指针及其对应值），其他元素视觉弱化。
    3.  **多模态呈现**：将数值比较（文本）、指针移动（动画）、范围排除（颜色填充/渐隐）和代码执行（高亮）同步进行，强化记忆。
    4.  **提供变式**：“旋转版”设计正是为了提供一种新的空间表征，帮助用户打破线性思维，从“范围收敛”的本质来理解算法，符合深度学习和迁移应用的要求。

*   **交互设计**：
    1.  **用户控制**：允许用户输入自定义数组和目标值，或从预设例子中选择。
    2.  **节奏控制**：提供“播放/暂停”、“下一步/上一步”、“重置”按钮，让学习者能以自己的节奏学习。
    3.  **模式切换**：在“标准线性视图”和“旋转环形视图”之间切换，从不同视觉角度理解同一过程。
    4.  **提示与反馈**：每一步都有文字说明当前比较情况和决策理由。查找成功或失败时有明确提示。

*   **视觉呈现**：
    1.  **标准线性视图**：
        *   数组元素水平排列在一条基线上。
        *   左指针（L）和右指针（R）用垂直的、颜色鲜明的箭头或标尺表示，分别位于当前搜索范围的两端。
        *   中间指针（M）用另一种颜色的箭头或标记表示，每次计算后出现在 `(L+R)/2` 位置。
        *   比较后，被排除的半个范围（如 `[L, M-1]` 或 `[M+1, R]`）视觉上“变灰”或“下沉”，表示不再考虑。当前活跃的搜索范围保持高亮。
        *   动画重点表现指针的“跳跃”和范围的“收缩”。
    2.  **旋转环形视图（创新点）**：
        *   将数组元素排列在一个**圆环**上。
        *   **左指针（L）固定**在圆环顶部（12点钟方向）。
        *   **右指针（R）** 和 **中间指针（M）** 在圆环上动态移动。
        *   **核心隐喻**：将“搜索范围”可视化为从 L 点**顺时针**到 R 点的一段**圆弧**。每次比较后，根据决策，动画表现为 R 或 L 沿着圆环“旋转”到新的位置（M+1 或 M-1），从而**缩短这段圆弧的长度**，直观体现“夹逼”和“范围缩小”。
        *   此视图能清晰展示：无论指针如何移动，算法始终在审视一段连续的弧段，并且这段弧段越来越短，直到长度为零（未找到）或弧段内某个点被命中（找到）。

#### 配色方案选择
*   **主色调**：采用科技蓝 (`#3498db`) 作为背景或主标题色，传达理性和清晰感。
*   **指针颜色**：
    *   左指针（L）：**绿色** (`#2ecc71`)，象征起点/安全范围。
    *   右指针（R）：**红色** (`#e74c3c`)，象征终点/边界。
    *   中间指针（M）：**醒目的黄色** (`#f1c40f`)，象征当前焦点和决策点。
*   **数组元素**：
    *   默认状态：浅灰色 (`#ecf0f1`) 背景，深灰色 (`#2c3e50`) 文字。
    *   活跃范围：元素背景为柔和的蓝色 (`#d6eaf8`)。
    *   已排除范围：元素背景变为更浅的灰色 (`#bdc3c7`)，文字颜色变淡，或增加透明度。
*   **成功/失败提示**：
    *   成功：元素背景变为金色 (`#f7dc6f`)，带有庆祝性动画（如轻微弹跳）。
    *   失败：整个区域柔和闪烁红色 (`#fadbd8`) 边框。
*   **交互控件**：使用中性但明确的颜色，如蓝色 (`#5dade2`) 表示主要动作，灰色 (`#95a5a6`) 表示次要/禁用状态。
*   **整体背景**：使用浅色背景 (`#f8f9fa`)，
    确保高对比度和可读性。

#### 交互功能列表
1.  **数据输入区**：
    *   预设示例选择下拉框（如：在有序数组中查找存在/不存在的值）。
    *   自定义数组输入框（逗号分隔的整数）。
    *   自定义目标值输入框。
    *   “应用数据”按钮。
2.  **视图控制区**：
    *   “标准视图” / “旋转视图” 切换按钮。
3.  **动画控制区**：
    *   “播放/暂停” 按钮。
    *   “下一步” 按钮（步进）。
    *   “上一步” 按钮（回溯）。
    *   “重置” 按钮（回到初始状态）。
    *   动画速度调节滑块。
4.  **信息展示区**：
    *   **算法状态面板**：实时显示当前 `left`, `mid`, `right` 的索引和值，以及 `arr[mid]` 与 `target` 的比较结果。
    *   **步骤说明面板**：用自然语言描述当前步骤在做什么（例如：“比较中间值 15 和目标值 20，15 < 20，因此目标在右侧，将左指针移动到 mid+1。”）。
    *   **伪代码面板**：高亮显示当前正在执行的伪代码行。
5.  **可视化主画布**：
    *   根据所选视图（标准/旋转），动态渲染数组、指针及动画效果。
    *   响应用户的播放控制指令。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>二分查找教学动画 - 左右指针夹逼（标准视图与旋转视图）</title>
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
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #3498db;
        }

        h1 {
            color: #3498db;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.1em;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }

        .control-panel {
            flex: 1;
            min-width: 300px;
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }

        .visualization-panel {
            flex: 2;
            min-width: 500px;
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-direction: column;
        }

        .panel-title {
            color: #2c3e50;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #ecf0f1;
            font-size: 1.3em;
        }

        .input-group {
            margin-bottom: 25px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #34495e;
        }

        input, select {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #ecf0f1;
            border-radius: 8px;
            font-size: 16px;
            transition: border-color 0.3s;
        }

        input:focus, select:focus {
            outline: none;
            border-color: #3498db;
        }

        .preset-examples {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
            margin-top: 10px;
        }

        .example-btn {
            padding: 10px;
            background-color: #ecf0f1;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.2s;
            font-size: 14px;
        }

        .example-btn:hover {
            background-color: #d5dbdb;
        }

        .example-btn.active {
            background-color: #3498db;
            color: white;
        }

        .view-toggle {
            display: flex;
            margin-bottom: 25px;
            background-color: #ecf0f1;
            border-radius: 8px;
            overflow: hidden;
        }

        .view-btn {
            flex: 1;
            padding: 12px;
            text-align: center;
            background: none;
            border: none;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
        }

        .view-btn.active {
            background-color: #3498db;
            color: white;
        }

        .animation-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 25px;
        }

        .control-btn {
            flex: 1;
            min-width: 120px;
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            font-size: 16px;
            transition: all 0.2s;
        }

        .primary-btn {
            background-color: #5dade2;
            color: white;
        }

        .primary-btn:hover {
            background-color: #3498db;
        }

        .secondary-btn {
            background-color: #ecf0f1;
            color: #2c3e50;
        }

        .secondary-btn:hover {
            background-color: #d5dbdb;
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 25px;
        }

        .speed-slider {
            flex: 1;
        }

        .info-panel {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 20px;
            margin-top: 20px;
        }

        .info-title {
            font-weight: 600;
            margin-bottom: 10px;
            color: #2c3e50;
        }

        .status-display {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 20px;
        }

        .status-item {
            text-align: center;
            padding: 15px;
            border-radius: 8px;
            background-color: white;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.05);
        }

        .status-label {
            font-size: 14px;
            color: #7f8c8d;
            margin-bottom: 5px;
        }

        .status-value {
            font-size: 24px;
            font-weight: 700;
        }

        .L-value { color: #2ecc71; }
        .M-value { color: #f1c40f; }
        .R-value { color: #e74c3c; }

        .step-description {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 15px;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.05);
            min-height: 80px;
        }

        .code-panel {
            background-color: #2c3e50;
            color: #ecf0f1;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 15px;
            line-height: 1.5;
            overflow-x: auto;
            white-space: nowrap;
        }

        .code-line {
            margin-bottom: 8px;
        }

        .code-line.highlight {
            background-color: #34495e;
            padding: 5px 10px;
            border-radius: 4px;
            border-left: 3px solid #f1c40f;
        }

        .canvas-container {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 400px;
            position: relative;
        }

        canvas {
            display: block;
            max-width: 100%;
            max-height: 100%;
        }

        .result-message {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            padding: 20px 40px;
            border-radius: 12px;
            font-size: 24px;
            font-weight: 700;
            text-align: center;
            opacity: 0;
            transition: opacity 0.5s;
            z-index: 10;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .success {
            background-color: #f7dc6f;
            color: #2c3e50;
        }

        .failure {
            background-color: #fadbd8;
            color: #c0392b;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #ecf0f1;
            color: #7f8c8d;
            font-size: 14px;
        }

        @media (max-width: 900px) {
            .main-content {
                flex-direction: column;
            }
            
            .control-panel, .visualization-panel {
                min-width: 100%;
            }
            
            .status-display {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>二分查找教学动画</h1>
            <p class="subtitle">左右指针夹逼算法可视化 - 标准视图与旋转视图</p>
        </header>
        
        <div class="main-content">
            <!-- 左侧控制面板 -->
            <div class="control-panel">
                <h2 class="panel-title">控制面板</h2>
                
                <div class="input-group">
                    <label for="arrayInput">有序数组（逗号分隔的整数）</label>
                    <input type="text" id="arrayInput" value="2, 5, 8, 12, 16, 23, 38, 45, 56, 67, 78, 89, 90">
                </div>
                
                <div class="input-group">
                    <label for="targetInput">查找目标值</label>
                    <input type="number" id="targetInput" value="45">
                </div>
                
                <div class="input-group">
                    <label>预设示例</label>
                    <div class="preset-examples">
                        <button class="example-btn" data-array="2,5,8,12,16,23,38,45,56,67,78,89,90" data-target="45">示例1：查找中间值</button>
                        <button class="example-btn" data-array="1,3,5,7,9,11,13,15,17,19" data-target="7">示例2：查找存在值</button>
                        <button class="example-btn" data-array="10,20,30,40,50,60,70,80,90,100" data-target="55">示例3：查找不存在值</button>
                        <button class="example-btn" data-array="1,2,3,4,5,6,7,8,9,10" data-target="1">示例4：查找第一个元素</button>
                    </div>
                </div>
                
                <button id="applyData" class="control-btn primary-btn" style="width: 100%; margin-bottom: 25px;">
                    应用数据并重置
                </button>
                
                <div class="view-toggle">
                    <button id="standardViewBtn" class="view-btn active">标准视图</button>
                    <button id="rotatedViewBtn" class="view-btn">旋转视图</button>
                </div>
                
                <div class="animation-controls">
                    <button id="playPauseBtn" class="control-btn primary-btn">播放</button>
                    <button id="nextStepBtn" class="control-btn secondary-btn">下一步</button>
                    <button id="prevStepBtn" class="control-btn secondary-btn">上一步</button>
                    <button id="resetBtn" class="control-btn secondary-btn">重置</button>
                </div>
                
                <div class="speed-control">
                    <span>动画速度:</span>
                    <input type="range" id="speedSlider" class="speed-slider" min="1" max="10" value="5">
                    <span id="speedValue">中速</span>
                </div>
                
                <div class="info-panel">
                    <div class="info-title">算法状态</div>
                    <div class="status-display">
                        <div class="status-item">
                            <div class="status-label">左指针 (L)</div>
                            <div id="LValue" class="status-value L-value">0</div>
                        </div>
                        <div class="status-item">
                            <div class="status-label">中间指针 (M)</div>
                            <div id="MValue" class="status-value M-value">6</div>
                        </div>
                        <div class="status-item">
                            <div class="status-label">右指针 (R)</div>
                            <div id="RValue" class="status-value R-value">12</div>
                        </div>
                    </div>
                    
                    <div class="step-description" id="stepDescription">
                        点击"播放"按钮开始二分查找动画演示。算法将比较中间值与目标值，并根据结果移动左指针或右指针。
                    </div>
                </div>
            </div>
            
            <!-- 右侧可视化面板 -->
            <div class="visualization-panel">
                <h2 class="panel-title">算法可视化</h2>
                
                <div class="canvas-container">
                    <canvas id="animationCanvas" width="800" height="500"></canvas>
                    <div id="resultMessage" class="result-message"></div>
                </div>
                
                <div class="info-panel">
                    <div class="info-title">伪代码</div>
                    <div class="code-panel">
                        <div class="code-line">function binarySearch(arr, target) {</div>
                        <div class="code-line" id="codeLine1">    let left = 0;</div>
                        <div class="code-line" id="codeLine2">    let right = arr.length - 1;</div>
                        <div class="code-line" id="codeLine3">    while (left <= right) {</div>
                        <div class="code-line" id="codeLine4">        let mid = Math.floor((left + right) / 2);</div>
                        <div class="code-line" id="codeLine5">        if (arr[mid] === target) {</div>
                        <div class="codeLine6">            return mid; // 找到目标</div>
                        <div class="code-line" id="codeLine7">        } else if (arr[mid] < target) {</div>
                        <div class="code-line" id="codeLine8">            left = mid + 1; // 目标在右侧</div>
                        <div class="code-line" id="codeLine9">        } else {</div>
                        <div class="code-line" id="codeLine10">            right = mid - 1; // 目标在左侧</div>
                        <div class="code-line">        }</div>
                        <div class="code-line">    }</div>
                        <div class="code-line">    return -1; // 未找到目标</div>
                        <div class="code-line">}</div>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>二分查找教学动画 | 设计思路：标准视图展示线性搜索过程，旋转视图展示范围夹逼的环形隐喻</p>
            <p>绿色(L) = 左指针 | 黄色(M) = 中间指针 | 红色(R) = 右指针</p>
        </footer>
    </div>

    <script>
        // 全局变量
        let arr = [2, 5, 8, 12, 16, 23, 38, 45, 56, 67, 78, 89, 90];
        let target = 45;
        let left = 0;
        let right = arr.length - 1;
        let mid = Math.floor((left + right) / 2);
        let steps = [];
        let currentStep = 0;
        let isPlaying = false;
        let animationSpeed = 5; // 1-10
        let currentView = 'standard'; // 'standard' 或 'rotated'
        let animationFrameId = null;
        let lastTimestamp = 0;
        let animationProgress = 0;
        let isAnimating = false;
        
        // 获取DOM元素
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        const arrayInput = document.getElementById('arrayInput');
        const targetInput = document.getElementById('targetInput');
        const applyDataBtn = document.getElementById('applyData');
        const standardViewBtn = document.getElementById('standardViewBtn');
        const rotatedViewBtn = document.getElementById('rotatedViewBtn');
        const playPauseBtn = document.getElementById('playPauseBtn');
        const nextStepBtn = document.getElementById('nextStepBtn');
        const prevStepBtn = document.getElementById('prevStepBtn');
        const resetBtn = document.getElementById('resetBtn');
        const speedSlider = document.getElementById('speedSlider');
        const speedValue = document.getElementById('speedValue');
        const LValue = document.getElementById('LValue');
        const MValue = document.getElementById('MValue');
        const RValue = document.getElementById('RValue');
        const stepDescription = document.getElementById('stepDescription');
        const resultMessage = document.getElementById('resultMessage');
        const codeLines = {};
        for (let i = 1; i <= 10; i++) {
            codeLines[i] = document.getElementById(`codeLine${i}`);
        }
        
        // 预设示例按钮
        document.querySelectorAll('.example-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                document.querySelectorAll('.example-btn').forEach(b => b.classList.remove('active'));
                this.classList.add('active');
                
                const arrayStr = this.getAttribute('data-array');
                const targetVal = this.getAttribute('data-target');
                
                arrayInput.value = arrayStr;
                targetInput.value = targetVal;
                
                applyData();
            });
        });
        
        // 应用数据按钮
        applyDataBtn.addEventListener('click', applyData);
        
        // 视图切换
        standardViewBtn.addEventListener('click', () => switchView('standard'));
        rotatedViewBtn.addEventListener('click', () => switchView('rotated'));
        
        // 动画控制
        playPauseBtn.addEventListener('click', togglePlayPause);
        nextStepBtn.addEventListener('click', nextStep);
        prevStepBtn.addEventListener('click', prevStep);
        resetBtn.addEventListener('click', resetAnimation);
        
        // 速度控制
        speedSlider.addEventListener('input', function() {
            animationSpeed = parseInt(this.value);
            updateSpeedDisplay();
        });
        
        // 初始化
        function init() {
            // 解析数组输入
            try {
                arr = arrayInput.value.split(',').map(num => parseInt(num.trim())).filter(num => !isNaN(num));
                if (arr.length === 0) throw new Error("数组不能为空");
                
                // 检查数组是否有序
                for (let i = 1; i < arr.length; i++) {
                    if (arr[i] < arr[i-1]) {
                        alert("警告：输入数组不是升序排列，二分查找需要有序数组！");
                        break;
                    }
                }
            } catch (e) {
                alert("数组输入格式错误，请使用逗号分隔的整数，例如：1, 3, 5, 7, 9");
                arr = [2, 5, 8, 12, 16, 23, 38, 45, 56, 67, 78, 89, 90];
                arrayInput.value = arr.join(', ');
            }
            
            // 解析目标值
            target = parseInt(targetInput.value);
            if (isNaN(target)) {
                target = 45;
                targetInput.value = target;
            }
            
            // 重置算法状态
            left = 0;
            right = arr.length - 1;
            mid = Math.floor((left + right) / 2);
            steps = [];
            currentStep = 0;
            isPlaying = false;
            isAnimating = false;
            animationProgress = 0;
            
            // 生成步骤记录
            generateSteps();
            
            // 更新UI
            updateStatusDisplay();
            updateCodeHighlight();
            updateStepDescription();
            clearResultMessage();
            
            // 停止任何正在进行的动画
            if (animationFrameId) {
                cancelAnimationFrame(animationFrameId);
                animationFrameId = null;
            }
            
            // 重新绘制
            draw();
            
            // 更新播放按钮文本
            playPauseBtn.textContent = '播放';
        }
        
        // 应用数据
        function applyData() {
            init();
        }
        
        // 切换视图
        function switchView(view) {
            currentView = view;
            
            if (view === 'standard') {
                standardViewBtn.classList.add('active');
                rotatedViewBtn.classList.remove('active');
            } else {
                standardViewBtn.classList.remove('active');
                rotatedViewBtn.classList.add('active');
            }
            
            draw();
        }
        
        // 生成步骤记录
        function generateSteps() {
            steps = [];
            let l = 0;
            let r = arr.length - 1;
            let stepCount = 0;
            
            // 记录初始状态
            steps.push({
                left: l,
                right: r,
                mid: Math.floor((l + r) / 2),
                action: '初始化',
                description: `初始化：左指针 L=0，右指针 R=${r}，搜索范围为整个数组`
            });
            
            // 模拟二分查找过程
            while (l <= r) {
                stepCount++;
                if (stepCount > 50) break; // 防止无限循环
                
                const m = Math.floor((l + r) / 2);
                
                if (arr[m] === target) {
                    steps.push({
                        left: l,
                        right: r,
                        mid: m,
                        action: '比较',
                        description: `比较 arr[${m}]=${arr[m]} 与 target=${target}，相等！找到目标值`
                    });
                    steps.push({
                        left: l,
                        right: r,
                        mid: m,
                        action: '找到',
                        description: `查找成功！目标值 ${target} 在索引 ${m} 处`
                    });
                    break;
                } else if (arr[m] < target) {
                    steps.push({
                        left: l,
                        right: r,
                        mid: m,
                        action: '比较',
                        description: `比较 arr[${m}]=${arr[m]} 与 target=${target}，${arr[m]} < ${target}，目标在右侧`
                    });
                    l = m + 1;
                    steps.push({
                        left: l,
                        right: r,
                        mid: Math.floor((l + r) / 2),
                        action: '移动左指针',
                        description: `移动左指针 L 到 ${m+1}，搜索范围缩小为右半部分`
                    });
                } else {
                    steps.push({
                        left: l,
                        right: r,
                        mid: m,
                        action: '比较',
                        description: `比较 arr[${m}]=${arr[m]} 与 target=${target}，${arr[m]} > ${target}，目标在左侧`
                    });
                    r = m - 1;
                    steps.push({
                        left: l,
                        right: r,
                        mid: Math.floor((l + r) / 2),
                        action: '移动右指针',
                        description: `移动右指针 R 到 ${m-1}，搜索范围缩小为左半部分`
                    });
                }
            }
            
            if (l > r) {
                steps.push({
                    left: l,
                    right: r,
                    mid: -1,
                    action: '未找到',
                    description: `左指针 L=${l} > 右指针 R=${r}，搜索范围为空，目标值 ${target} 不在数组中`
                });
            }
        }
        
        // 切换播放/暂停
        function togglePlayPause() {
            isPlaying = !isPlaying;
            
            if (isPlaying) {
                playPauseBtn.textContent = '暂停';
                if (currentStep >= steps.length - 1) {
                    resetAnimation();
                }
                animate();
            } else {
                playPauseBtn.textContent = '播放';
                if (animationFrameId) {
                    cancelAnimationFrame(animationFrameId);
                    animationFrameId = null;
                }
            }
        }
        
        // 动画循环
        function animate(timestamp) {
            if (!lastTimestamp) lastTimestamp = timestamp;
            const deltaTime = timestamp - lastTimestamp;
            lastTimestamp = timestamp;
            
            if (isPlaying && !isAnimating) {
                // 计算动画进度
                const animationDuration = 1000 / animationSpeed;
                animationProgress += deltaTime / animationDuration;
                
                if (animationProgress >= 1) {
                    animationProgress = 0;
                    nextStep();
                }
            }
            
            // 绘制当前状态（带动画效果）
            draw();
            
            if (isPlaying) {
                animationFrameId = requestAnimationFrame(animate);
            }
        }
        
        // 下一步
        function nextStep() {
            if (currentStep < steps.length - 1) {
                currentStep++;
                updateFromStep();
                
                // 如果到达最后一步，停止播放
                if (currentStep === steps.length - 1) {
                    isPlaying = false;
                    playPauseBtn.textContent = '播放';
                }
            }
        }
        
        // 上一步
        function prevStep() {
            if (currentStep > 0) {
                currentStep--;
                updateFromStep();
            }
        }
        
        // 重置动画
        function resetAnimation() {
            currentStep = 0;
            isPlaying = false;
            playPauseBtn.textContent = '播放';
            updateFromStep();
            
            if (animationFrameId) {
                cancelAnimationFrame(animationFrameId);
                animationFrameId = null;
            }
        }
        
        // 从当前步骤更新状态
        function updateFromStep() {
            const step = steps[currentStep];
            left = step.left;
            right = step.right;
            mid = step.mid;
            
            updateStatusDisplay();
            updateCodeHighlight();
            updateStepDescription();
            
            // 检查是否找到或未找到
            if (step.action === '找到') {
                showResultMessage('success', `找到目标值 ${target} 在索引 ${mid} 处`);
            } else if (step.action === '未找到') {
                showResultMessage('failure', `未找到目标值 ${target}`);
            } else {
                clearResultMessage();
            }
            
            // 开始动画循环（如果正在播放）
            if (isPlaying) {
                if (animationFrameId) {
                    cancelAnimationFrame(animationFrameId);
                }
                lastTimestamp = 0;
                animationFrameId = requestAnimationFrame(animate);
            } else {
                draw();
            }
        }
        
        // 更新速度显示
        function updateSpeedDisplay() {
            const speedLabels = ['极慢', '很慢', '慢', '较慢', '中慢', '中速', '中快', '快', '很快', '极快'];
            speedValue.textContent = speedLabels[animationSpeed - 1];
        }
        
        // 更新状态显示
        function updateStatusDisplay() {
            LValue.textContent = left;
            RValue.textContent = right;
            MValue.textContent = mid >= 0 ? mid : '-';
        }
        
        // 更新代码高亮
        function updateCodeHighlight() {
            // 重置所有代码行
            Object.values(codeLines).forEach(line => {
                line.classList.remove('highlight');
            });
            
            const step = steps[currentStep];
            
            // 根据当前步骤高亮相应的代码行
            if (step.action === '初始化') {
                codeLines[1].classList.add('highlight');
                codeLines[2].classList.add('highlight');
            } else if (step.action === '比较') {
                codeLines[4].classList.add('highlight');
                codeLines[5].classList.add('highlight');
            } else if (step.action === '移动左指针') {
                codeLines[7].classList.add('highlight');
                codeLines[8].classList.add('highlight');
            } else if (step.action === '移动右指针') {
                codeLines[9].classList.add('highlight');
                codeLines[10].classList.add('highlight');
            } else if (step.action === '找到') {
                codeLines[5].classList.add('highlight');
                codeLines[6].classList.add('highlight');
            } else if (step.action === '未找到') {
                // 不特别高亮，因为已经退出循环
            }
        }
        
        // 更新步骤描述
        function updateStepDescription() {
            if (currentStep < steps.length) {
                stepDescription.textContent = `步骤 ${currentStep + 1}/${steps.length}: ${steps[currentStep].description}`;
            }
        }
        
        // 显示结果消息
        function showResultMessage(type, message) {
            resultMessage.textContent = message;
            resultMessage.className = `result-message ${type}`;
            resultMessage.style.opacity = '1';
            
            // 5秒后淡出
            setTimeout(() => {
                resultMessage.style.opacity = '0';
            }, 5000);
        }
        
        // 清除结果消息
        function clearResultMessage() {
            resultMessage.style.opacity = '0';
        }
        
        // 绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            if (currentView === 'standard') {
                drawStandardView();
            } else {
                drawRotatedView();
            }
        }
        
        // 绘制标准视图
        function drawStandardView() {
            const canvasWidth = canvas.width;
            const canvasHeight = canvas.height;
            const arrayLength = arr.length;
            
            // 计算元素宽度和间距
            const elementWidth = Math.min(60, (canvasWidth - 100) / arrayLength);
            const spacing = 10;
            const totalWidth = arrayLength * (elementWidth + spacing) - spacing;
            const startX = (canvasWidth - totalWidth) / 2;
            const baseY = canvasHeight * 0.6;
            
            // 绘制标题
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('二分查找 - 标准视图（线性搜索）', canvasWidth / 2, 40);
            
            // 绘制数组元素
            for (let i = 0; i < arrayLength; i++) {
                const x = startX + i * (elementWidth + spacing);
                const y = baseY;
                
                // 判断元素状态
                let bgColor, textColor;
                
                if (i < left || i > right) {
                    // 已排除的范围
                    bgColor = '#bdc3c7';
                    textColor = '#7f8c8d';
                } else if (i === mid && mid >= 0 && mid < arrayLength) {
                    // 中间指针
                    bgColor = '#f1c40f';
                    textColor = '#2c3e50';
                } else {
                    // 当前搜索范围
                    bgColor = '#d6eaf8';
                    textColor = '#2c3e50';
                }
                
                // 绘制元素背景
                ctx.fillStyle = bgColor;
                ctx.fillRect(x, y, elementWidth, 60);
                
                // 绘制元素边框
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 2;
                ctx.strokeRect(x, y, elementWidth, 60);
                
                // 绘制索引
                ctx.fillStyle = '#7f8c8d';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`[${i}]`, x + elementWidth / 2, y + 20);
                
                // 绘制值
                ctx.fillStyle = textColor;
                ctx.font = 'bold 18px Arial';
                ctx.fillText(arr[i].toString(), x + elementWidth / 2, y + 45);
                
                // 如果是目标值且已找到，添加特殊标记
                if (arr[i] === target && steps[currentStep].action === '找到' && i === mid) {
                    ctx.fillStyle = 'rgba(247, 220, 111, 0.3)';
                    ctx.fillRect(x - 5, y - 5, elementWidth + 10, 70);
                    
                    // 绘制找到的动画效果
                    const pulseSize = 5 + Math.sin(Date.now() / 200) * 3;
                    ctx.strokeStyle = '#f7dc6f';
                    ctx.lineWidth = 3;
                    ctx.strokeRect(x - pulseSize, y - pulseSize, elementWidth + 2 * pulseSize, 60 + 2 * pulseSize);
                }
            }
            
            // 绘制指针
            drawStandardPointers(startX, baseY, elementWidth, spacing);
            
            // 绘制目标值指示
            ctx.fillStyle = '#e74c3c';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'left';
            ctx.fillText(`目标值: ${target}`, 30, 80);
            
            // 绘制当前搜索范围
            if (left <= right) {
                ctx.fillStyle = '#2ecc71';
                ctx.font = '16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`当前搜索范围: [${left}, ${right}]`, canvasWidth / 2, 100);
            }
        }
        
        // 绘制标准视图的指针
        function drawStandardPointers(startX, baseY, elementWidth, spacing) {
            const pointerLength = 80;
            
            // 左指针 (L) - 绿色
            if (left >= 0 && left < arr.length) {
                const lx = startX + left * (elementWidth + spacing) + elementWidth / 2;
                const ly = baseY - 30;
                
                ctx.fillStyle = '#2ecc71';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('L', lx, ly - 10);
                
                // 绘制指针箭头
                ctx.beginPath();
                ctx.moveTo(lx, ly);
                ctx.lineTo(lx - 10, ly - 20);
                ctx.lineTo(lx + 10, ly - 20);
                ctx.closePath();
                ctx.fill();
                
                // 绘制指针线
                ctx.beginPath();
                ctx.moveTo(lx, ly);
                ctx.lineTo(lx, baseY);
                ctx.strokeStyle = '#2ecc71';
                ctx.lineWidth = 3;
                ctx.stroke();
            }
            
            // 右指针 (R) - 红色
            if (right >= 0 && right < arr.length) {
                const rx = startX + right * (elementWidth + spacing) + elementWidth / 2;
                const ry = baseY - 30;
                
                ctx.fillStyle = '#e74c3c';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('R', rx, ry - 10);
                
                // 绘制指针箭头
                ctx.beginPath();
                ctx.moveTo(rx, ry);
                ctx.lineTo(rx - 10, ry - 20);
                ctx.lineTo(rx + 10, ry - 20);
                ctx.closePath();
                ctx.fill();
                
                // 绘制指针线
                ctx.beginPath();
                ctx.moveTo(rx, ry);
                ctx.lineTo(rx, baseY);
                ctx.strokeStyle = '#e74c3c';
                ctx.lineWidth = 3;
                ctx.stroke();
            }
            
            // 中间指针 (M) - 黄色
            if (mid >= 0 && mid < arr.length && mid >= left && mid <= right) {
                const mx = startX + mid * (elementWidth + spacing) + elementWidth / 2;
                const my = baseY - 60;
                
                ctx.fillStyle = '#f1c40f';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('M', mx, my - 10);
                
                // 绘制指针箭头
                ctx.beginPath();
                ctx.moveTo(mx, my);
                ctx.lineTo(mx - 10, my
<!--检测到代码截断，自动续写中...-->
- 20);
                ctx.lineTo(mx + 10, my - 20);
                ctx.closePath();
                ctx.fill();
                
                // 绘制指针线
                ctx.beginPath();
                ctx.moveTo(mx, my);
                ctx.lineTo(mx, baseY);
                ctx.strokeStyle = '#f1c40f';
                ctx.lineWidth = 3;
                ctx.stroke();
            }
        }
        
        // 绘制旋转视图
        function drawRotatedView() {
            const canvasWidth = canvas.width;
            const canvasHeight = canvas.height;
            const arrayLength = arr.length;
            
            // 计算圆环参数
            const centerX = canvasWidth / 2;
            const centerY = canvasHeight / 2;
            const radius = Math.min(canvasWidth, canvasHeight) * 0.35;
            
            // 绘制标题
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('二分查找 - 旋转视图（环形搜索范围）', canvasWidth / 2, 40);
            
            // 绘制圆环
            ctx.strokeStyle = '#ecf0f1';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.arc(centerX, centerY, radius, 0, Math.PI * 2);
            ctx.stroke();
            
            // 绘制数组元素（在圆环上）
            const angleStep = (Math.PI * 2) / arrayLength;
            
            for (let i = 0; i < arrayLength; i++) {
                const angle = i * angleStep - Math.PI / 2; // 从顶部开始
                const x = centerX + radius * Math.cos(angle);
                const y = centerY + radius * Math.sin(angle);
                
                // 判断元素状态
                let bgColor, textColor;
                
                // 在旋转视图中，判断元素是否在当前搜索范围内
                // 搜索范围是从L到R的顺时针弧段
                let isInRange = false;
                if (left <= right) {
                    isInRange = (i >= left && i <= right);
                } else {
                    // 正常情况下二分查找不会出现left>right还在搜索的情况
                    isInRange = false;
                }
                
                if (!isInRange) {
                    // 已排除的范围
                    bgColor = '#bdc3c7';
                    textColor = '#7f8c8d';
                } else if (i === mid && mid >= 0 && mid < arrayLength) {
                    // 中间指针
                    bgColor = '#f1c40f';
                    textColor = '#2c3e50';
                } else {
                    // 当前搜索范围
                    bgColor = '#d6eaf8';
                    textColor = '#2c3e50';
                }
                
                // 绘制元素背景（圆形）
                ctx.fillStyle = bgColor;
                ctx.beginPath();
                ctx.arc(x, y, 25, 0, Math.PI * 2);
                ctx.fill();
                
                // 绘制元素边框
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.arc(x, y, 25, 0, Math.PI * 2);
                ctx.stroke();
                
                // 绘制索引
                ctx.fillStyle = '#7f8c8d';
                ctx.font = '12px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`[${i}]`, x, y - 10);
                
                // 绘制值
                ctx.fillStyle = textColor;
                ctx.font = 'bold 16px Arial';
                ctx.fillText(arr[i].toString(), x, y + 5);
            }
            
            // 绘制指针和搜索范围弧段
            drawRotatedPointersAndArc(centerX, centerY, radius, angleStep);
            
            // 绘制目标值指示
            ctx.fillStyle = '#e74c3c';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'left';
            ctx.fillText(`目标值: ${target}`, 30, 80);
            
            // 绘制当前搜索范围
            if (left <= right) {
                ctx.fillStyle = '#2ecc71';
                ctx.font = '16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`当前搜索范围: [${left}, ${right}]`, canvasWidth / 2, 100);
                
                // 绘制范围长度指示
                ctx.fillText(`范围长度: ${right - left + 1} 个元素`, canvasWidth / 2, 120);
            }
            
            // 绘制图例
            drawLegend(centerX, centerY, radius);
        }
        
        // 绘制旋转视图的指针和弧段
        function drawRotatedPointersAndArc(centerX, centerY, radius, angleStep) {
            // 绘制搜索范围弧段（从L到R的顺时针弧段）
            if (left <= right && left >= 0 && right < arr.length) {
                const startAngle = left * angleStep - Math.PI / 2;
                const endAngle = (right + 1) * angleStep - Math.PI / 2; // +1 使弧段包含右端点
                
                ctx.strokeStyle = 'rgba(46, 204, 113, 0.6)';
                ctx.lineWidth = 8;
                ctx.beginPath();
                ctx.arc(centerX, centerY, radius + 15, startAngle, endAngle);
                ctx.stroke();
            }
            
            // 左指针 (L) - 绿色，固定在顶部
            if (left >= 0 && left < arr.length) {
                const lAngle = left * angleStep - Math.PI / 2;
                const lx = centerX + (radius + 40) * Math.cos(lAngle);
                const ly = centerY + (radius + 40) * Math.sin(lAngle);
                
                // 绘制指针线
                ctx.beginPath();
                ctx.moveTo(centerX, centerY);
                ctx.lineTo(lx, ly);
                ctx.strokeStyle = '#2ecc71';
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 绘制指针标记
                ctx.fillStyle = '#2ecc71';
                ctx.beginPath();
                ctx.arc(lx, ly, 12, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = 'white';
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText('L', lx, ly);
            }
            
            // 右指针 (R) - 红色
            if (right >= 0 && right < arr.length) {
                const rAngle = right * angleStep - Math.PI / 2;
                const rx = centerX + (radius + 40) * Math.cos(rAngle);
                const ry = centerY + (radius + 40) * Math.sin(rAngle);
                
                // 绘制指针线
                ctx.beginPath();
                ctx.moveTo(centerX, centerY);
                ctx.lineTo(rx, ry);
                ctx.strokeStyle = '#e74c3c';
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 绘制指针标记
                ctx.fillStyle = '#e74c3c';
                ctx.beginPath();
                ctx.arc(rx, ry, 12, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = 'white';
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText('R', rx, ry);
            }
            
            // 中间指针 (M) - 黄色
            if (mid >= 0 && mid < arr.length && mid >= left && mid <= right) {
                const mAngle = mid * angleStep - Math.PI / 2;
                const mx = centerX + (radius + 60) * Math.cos(mAngle);
                const my = centerY + (radius + 60) * Math.sin(mAngle);
                
                // 绘制指针线
                ctx.beginPath();
                ctx.moveTo(centerX, centerY);
                ctx.lineTo(mx, my);
                ctx.strokeStyle = '#f1c40f';
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 绘制指针标记
                ctx.fillStyle = '#f1c40f';
                ctx.beginPath();
                ctx.arc(mx, my, 15, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = '#2c3e50';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText('M', mx, my);
                
                // 如果是比较步骤，添加比较动画
                if (steps[currentStep] && steps[currentStep].action === '比较') {
                    ctx.strokeStyle = '#f1c40f';
                    ctx.lineWidth = 2;
                    const pulseSize = 5 + Math.sin(Date.now() / 200) * 3;
                    ctx.beginPath();
                    ctx.arc(mx, my, 15 + pulseSize, 0, Math.PI * 2);
                    ctx.stroke();
                }
            }
            
            // 绘制中心点
            ctx.fillStyle = '#3498db';
            ctx.beginPath();
            ctx.arc(centerX, centerY, 10, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制中心标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = '14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('搜索中心', centerX, centerY - 25);
        }
        
        // 绘制图例
        function drawLegend(centerX, centerY, radius) {
            const legendX = centerX + radius + 100;
            const legendY = centerY - radius + 50;
            
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'left';
            ctx.fillText('图例', legendX, legendY);
            
            // 左指针图例
            ctx.fillStyle = '#2ecc71';
            ctx.beginPath();
            ctx.arc(legendX + 10, legendY + 30, 8, 0, Math.PI * 2);
            ctx.fill();
            ctx.fillStyle = '#2c3e50';
            ctx.font = '14px Arial';
            ctx.fillText('左指针 (L)', legendX + 30, legendY + 34);
            
            // 右指针图例
            ctx.fillStyle = '#e74c3c';
            ctx.beginPath();
            ctx.arc(legendX + 10, legendY + 60, 8, 0, Math.PI * 2);
            ctx.fill();
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('右指针 (R)', legendX + 30, legendY + 64);
            
            // 中间指针图例
            ctx.fillStyle = '#f1c40f';
            ctx.beginPath();
            ctx.arc(legendX + 10, legendY + 90, 8, 0, Math.PI * 2);
            ctx.fill();
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('中间指针 (M)', legendX + 30, legendY + 94);
            
            // 搜索范围图例
            ctx.strokeStyle = 'rgba(46, 204, 113, 0.6)';
            ctx.lineWidth = 6;
            ctx.beginPath();
            ctx.moveTo(legendX + 5, legendY + 120);
            ctx.lineTo(legendX + 25, legendY + 120);
            ctx.stroke();
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('当前搜索范围', legendX + 30, legendY + 124);
            
            // 已排除范围图例
            ctx.fillStyle = '#bdc3c7';
            ctx.fillRect(legendX + 5, legendY + 140, 20, 10);
            ctx.fillStyle = '#2c3e50';
            ctx.fillText('已排除范围', legendX + 30, legendY + 148);
        }
        
        // 初始化应用
        window.addEventListener('load', function() {
            init();
            updateSpeedDisplay();
            
            // 设置初始示例按钮为激活状态
            document.querySelector('.example-btn').classList.add('active');
        });
        
        // 窗口大小变化时调整画布
        window.addEventListener('resize', function() {
            // 简单处理：重新绘制
            draw();
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

# 二分查找交互式教学动画使用指南

欢迎使用“二分查找教学动画”！本工具旨在通过动态、直观的可视化方式，帮助您深入理解二分查找算法的核心原理与执行过程。无论您是初次接触算法的学生，还是希望巩固知识的开发者，本动画都将为您提供独特的学习体验。

## 一、功能说明

本动画提供了两种独特的可视化视角来演示二分查找算法：
1. **标准视图**：传统的线性数组展示方式，直观呈现指针在数组上的移动和搜索范围的收缩。
2. **旋转视图**：创新的环形展示方式，将搜索范围可视化为一段圆弧，生动体现“夹逼”过程的本质。

通过两种视图的对比，您可以从不同角度理解同一算法，加深对“分治”和“范围收敛”思想的认识。

## 二、主要功能

### 1. 数据输入与预设
- **自定义数组**：输入任意升序整数数组（逗号分隔）
- **自定义目标值**：指定要查找的目标数字
- **预设示例**：提供4个典型场景的预设，一键加载：
  - 查找中间值
  - 查找存在值
  - 查找不存在值
  - 查找第一个元素

### 2. 动画控制
- **播放/暂停**：控制动画的连续播放
- **步进控制**：通过“下一步/上一步”按钮精确控制算法每一步
- **速度调节**：10档速度调节（极慢到极快）
- **重置功能**：随时回到初始状态

### 3. 信息同步展示
- **实时状态面板**：显示当前左(L)、中(M)、右(R)指针的位置
- **步骤描述**：用自然语言解释当前步骤的逻辑
- **伪代码高亮**：同步高亮当前执行的代码行
- **结果反馈**：查找成功或失败时有明确的视觉和文字提示

## 三、设计特色

### 1. 双重视角设计
- **标准视图**：采用经典的水平数组布局，适合初学者建立直观认知
  - 绿色(L)、黄色(M)、红色(R)指针清晰标识
  - 已排除区域视觉弱化（变灰）
  - 当前搜索范围高亮显示

- **旋转视图**：创新的环形隐喻，揭示算法本质
  - 将数组排列在圆环上
  - 搜索范围可视化为从L到R的**顺时针弧段**
  - 每次比较后，弧段长度缩短，直观体现“夹逼”
  - 固定L在顶部，R和M动态旋转，强化空间认知

### 2. 精心设计的视觉编码
- **色彩语义**：
  - 绿色(#2ecc71)：左指针(L) - 起点/安全
  - 黄色(#f1c40f)：中间指针(M) - 焦点/决策点
  - 红色(#e74c3c)：右指针(R) - 终点/边界
  - 蓝色(#d6eaf8)：当前搜索范围
  - 灰色(#bdc3c7)：已排除范围

- **动画效果**：
  - 指针移动平滑过渡
  - 范围排除时的渐隐效果
  - 找到目标时的脉冲高亮
  - 比较步骤的焦点强调

### 3. 认知友好的交互设计
- **节奏可控**：支持暂停、步进，适应不同学习节奏
- **状态可逆**：支持回溯到上一步，便于反复观察
- **多模态同步**：视觉动画、文字描述、代码高亮三同步
- **错误预防**：自动检测数组是否有序，给出友好提示

## 四、教学要点

### 核心概念可视化
1. **有序前提**：强调二分查找仅适用于有序数组
2. **指针含义**：
   - L：当前搜索范围的左边界
   - R：当前搜索范围的右边界
   - M：当前比较的中间位置
3. **比较决策**：
   - arr[M] = target → 查找成功
   - arr[M] < target → 目标在右侧，L = M + 1
   - arr[M] > target → 目标在左侧，R = M - 1
4. **终止条件**：L > R 时搜索范围为空，查找失败

### 算法思维培养
1. **分治思想**：每次比较排除一半不可能的区域
2. **循环不变式**：始终维护“目标值（如果存在）一定在[L, R]范围内”的不变性
3. **边界处理**：注意指针移动时的+1/-1操作，避免死循环
4. **效率理解**：直观感受O(log n)的时间复杂度

### 旋转视图的独特价值
1. **空间转换**：将线性思维转换为环形思维
2. **范围本质**：强调算法操作的是“一段连续范围”而非离散点
3. **收敛过程**：弧段长度从整个圆周逐渐缩短到零或一个点
4. **抽象提升**：帮助从具体实现抽象到算法思想

## 五、使用建议

### 学习路径推荐
1. **初学者**：
   - 从“标准视图”开始，使用预设示例1
   - 先用“播放”模式观看完整过程
   - 再用“步进”模式仔细分析每一步
   - 重点理解指针移动逻辑和比较决策

2. **进阶学习**：
   - 尝试自定义数组和目标值
   - 观察边界情况（查找首尾元素、查找不存在值）
   - 切换到“旋转视图”，体会范围收敛的本质
   - 对比两种视图，思考其内在一致性

3. **教学演示**：
   - 先用标准视图讲解基本流程
   - 再用旋转视图揭示算法本质
   - 通过改变动画速度适应课堂节奏
   - 鼓励学生预测下一步操作

### 探究性问题
在观看动画时，可以思考以下问题：
1. 如果数组不是升序排列，二分查找还能正常工作吗？为什么？
2. 当查找一个不存在的值时，算法最终会停在哪里？
3. 为什么中间位置要取 floor((L+R)/2) 而不是 ceil？
4. 在旋转视图中，为什么L固定在顶部而R可以移动？
5. 二分查找的时间复杂度为什么是O(log n)？从动画中能看出什么线索？

### 扩展思考
1. **变体算法**：了解二分查找的变体（查找第一个/最后一个出现的位置）
2. **实际应用**：思考二分查找在现实场景中的应用（字典查找、版本控制中的二分定位bug）
3. **错误调试**：故意输入错误数据，观察系统的反馈和处理

---

**温馨提示**：本工具支持响应式设计，在电脑和平板上都能获得良好体验。建议在Chrome、Firefox或Edge等现代浏览器中使用。

祝您学习愉快，在算法的世界里探索无限可能！如有任何反馈或建议，欢迎与我们分享。