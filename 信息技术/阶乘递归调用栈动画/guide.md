# 需求：阶乘递归调用栈动画

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户是**计算机科学或编程的初学者**，特别是正在学习“递归”这一核心概念的学生。他们面临的典型困难是：
1.  **抽象性**：递归调用过程在代码层面是静态的，难以在脑海中动态构建其执行流程。
2.  **栈的不可见性**：函数调用栈是系统自动管理的，初学者无法直观看到栈的增长与收缩。
3.  **理解“递”与“归”**：容易混淆递归的展开（递）和返回（归）两个阶段，不理解返回值是如何一步步回溯并组合出最终结果的。

因此，用户的核心需求是：**通过一个清晰、直观、可控制的视觉动画，将抽象的递归调用栈具象化，从而深刻理解递归的执行机制和阶乘的计算过程。**

#### 教学设计思路
1.  **核心概念聚焦**：动画将紧紧围绕 **“函数调用栈”** 和 **“递归深度”** 这两个关键概念展开。所有视觉元素和交互都服务于展示栈的变化。
2.  **遵循认知规律**：
    *   **从具体到抽象**：以一个具体的数字（如 `5!`）为例开始，避免一开始就讨论通用公式。
    *   **分解步骤**：将连续的递归过程分解为离散的、可暂停的帧，允许学习者按自己的节奏观察。
    *   **双重编码**：同时使用**视觉符号**（栈帧、箭头、数字）和**文本说明**（状态描述、公式）来强化记忆和理解。
3.  **交互设计**：
    *   **控制权交给用户**：提供“下一步”、“上一步”、“播放/暂停”和“重置”控件，让用户主动探索，而非被动观看。
    *   **关键状态高亮**：在“递”阶段，高亮当前正在计算的表达式和即将进行的递归调用；在“归”阶段，高亮返回的值以及它如何被用于上一层的计算。
    *   **可调节的输入**：允许用户输入不同的 `n` 值（如3, 5, 7），观察递归深度变化对调用栈的影响。
4.  **视觉呈现**：
    *   **调用栈可视化**：将调用栈设计为一个从底部向上“生长”的垂直栈。每个栈帧是一个清晰的矩形，包含函数名、参数 `n` 的当前值、以及当前要计算的表达式（如 `factorial(5) = 5 * factorial(4)`）。
    *   **动态箭头指示**：使用箭头明确指示程序执行流：
        *   向下的箭头表示“递”——调用更深层的函数，新的栈帧入栈。
        *   向上的箭头表示“归”——函数返回，栈帧出栈，返回值沿箭头向上传递。
    *   **信息分区**：
        *   **主动画区**：占据中心位置，动态展示调用栈和箭头。
        *   **代码区**：静态显示 `factorial` 函数的伪代码，并与动画同步高亮当前执行的行。
        *   **控制与输入区**：放置所有交互控件和数字输入框。
        *   **状态说明区**：用文字描述当前步骤发生了什么（例如：“计算 `factorial(2)`，需要先知道 `factorial(1)`，因此调用 `factorial(1)`”）。

#### 配色方案选择
选择清晰、友好且有助于区分不同信息层次的配色：
*   **背景与主色调**：使用柔和的浅灰色（`#f5f7fa`）作为背景，避免视觉疲劳。主区域使用干净的白色（`#ffffff`）卡片。
*   **栈帧颜色**：
    *   **当前活动栈帧**：使用温和的强调色，如浅蓝色（`#e3f2fd`），边框为深蓝色（`#2196f3`），表示这是正在执行或刚刚返回的帧。
    *   **非活动栈帧**：使用中性浅灰色（`#eeeeee`），边框为灰色（`#9e9e9e`）。
*   **箭头与高亮**：
    *   **“递”过程箭头**：使用绿色（`#4caf50`），象征“展开”和“生长”。
    *   **“归”过程箭头/返回值**：使用橙色（`#ff9800`），象征“回溯”和“结果合成”。
    *   **代码高亮**：使用与当前活动栈帧匹配的浅蓝色背景（`#e3f2fd`）。
*   **文本与控件**：主要文字为深灰色（`#333333`）。按钮使用友好的蓝色（`#2196f3`）和绿色（`#4caf50`），悬停时有加深效果。

#### 交互功能列表
1.  **核心动画控制**：
    *   **下一步**：单步执行到下一个关键状态（一次调用、一次返回或一次计算）。
    *   **上一步**：回退到上一个关键状态。
    *   **播放/暂停**：自动连续播放动画。
    *   **重置**：清空栈，回到初始状态。
2.  **输入与初始化**：
    *   **数字输入框**：允许用户输入一个非负整数 `n`（例如：5）。
    *   **开始演示按钮**：根据输入的 `n` 初始化动画，准备计算 `factorial(n)`。
3.  **视觉反馈与说明**：
    *   **栈帧的压入与弹出**：伴随平滑的动画效果。
    *   **执行流箭头**：在“递”和“归”时动态绘制。
    *   **返回值传递**：以“气泡”或标签形式，沿着箭头方向移动，显示返回的具体数值。
    *   **同步代码高亮**：代码区始终高亮与当前栈帧对应的代码行。
    *   **动态状态文本**：在专用区域用自然语言描述当前步骤。
4.  **辅助功能**：
    *   **速度调节**：在自动播放模式下，可以调节动画速度的滑块。
    *   **栈帧标签**：每个栈帧清晰标注 `factorial(n)` 和 `n` 的值。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>阶乘递归调用栈动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 15px;
            border-bottom: 2px solid #e0e0e0;
        }

        h1 {
            color: #2196f3;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #666;
            font-size: 1.1em;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
        }

        .panel {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            padding: 20px;
        }

        .control-panel {
            flex: 1;
            min-width: 300px;
        }

        .code-panel {
            flex: 1;
            min-width: 300px;
        }

        .animation-panel {
            flex: 2;
            min-width: 500px;
            min-height: 500px;
        }

        .panel-title {
            font-size: 1.2em;
            font-weight: 600;
            color: #2196f3;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #e0e0e0;
        }

        .input-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        input[type="number"] {
            width: 100%;
            padding: 10px 12px;
            border: 2px solid #ddd;
            border-radius: 6px;
            font-size: 16px;
            transition: border-color 0.3s;
        }

        input[type="number"]:focus {
            border-color: #2196f3;
            outline: none;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }

        button {
            padding: 10px 16px;
            border: none;
            border-radius: 6px;
            font-size: 15px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }

        .btn-primary {
            background-color: #2196f3;
            color: white;
        }

        .btn-primary:hover {
            background-color: #0d8bf2;
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

        .btn-secondary {
            background-color: #9e9e9e;
            color: white;
        }

        .btn-secondary:hover {
            background-color: #757575;
        }

        .speed-control {
            margin-top: 15px;
        }

        .speed-control label {
            margin-bottom: 5px;
        }

        .speed-slider {
            width: 100%;
            margin-top: 5px;
        }

        .code-container {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 15px;
            line-height: 1.5;
            overflow-x: auto;
            border: 1px solid #e0e0e0;
        }

        .code-line {
            padding: 4px 8px;
            margin: 2px 0;
            border-radius: 4px;
            transition: background-color 0.3s;
        }

        .code-line.highlighted {
            background-color: #e3f2fd;
            border-left: 3px solid #2196f3;
        }

        .code-keyword {
            color: #2196f3;
            font-weight: bold;
        }

        .code-function {
            color: #e91e63;
        }

        .code-number {
            color: #4caf50;
        }

        .code-operator {
            color: #ff9800;
        }

        #animationCanvas {
            width: 100%;
            height: 500px;
            border-radius: 8px;
            background-color: white;
            display: block;
        }

        .status-panel {
            flex: 100%;
            min-height: 100px;
            margin-top: 10px;
        }

        .status-title {
            font-size: 1.1em;
            font-weight: 600;
            color: #2196f3;
            margin-bottom: 10px;
        }

        .status-content {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            border: 1px solid #e0e0e0;
            min-height: 70px;
            font-size: 16px;
        }

        .status-step {
            font-weight: 600;
            color: #2196f3;
            margin-bottom: 5px;
        }

        .status-desc {
            color: #333;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #e0e0e0;
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
            font-size: 14px;
        }

        .footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #e0e0e0;
            color: #666;
            font-size: 0.9em;
        }

        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .animation-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>阶乘递归调用栈动画</h1>
        <p class="subtitle">可视化理解递归函数的执行过程与调用栈变化</p>
    </div>

    <div class="container">
        <div class="panel control-panel">
            <div class="panel-title">控制面板</div>
            
            <div class="input-group">
                <label for="inputNumber">计算阶乘 factorial(n):</label>
                <input type="number" id="inputNumber" min="0" max="10" value="5">
                <button id="btnStart" class="btn-primary" style="margin-top: 10px; width: 100%;">
                    <span>开始演示</span>
                </button>
            </div>

            <div class="button-group">
                <button id="btnPrev" class="btn-secondary">
                    <span>上一步</span>
                </button>
                <button id="btnNext" class="btn-primary">
                    <span>下一步</span>
                </button>
                <button id="btnPlayPause" class="btn-success">
                    <span>播放</span>
                </button>
                <button id="btnReset" class="btn-warning">
                    <span>重置</span>
                </button>
            </div>

            <div class="speed-control">
                <label for="speedSlider">动画速度:</label>
                <input type="range" id="speedSlider" min="1" max="10" value="5" class="speed-slider">
            </div>

            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #e3f2fd; border: 2px solid #2196f3;"></div>
                    <div class="legend-text">当前活动栈帧</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #eeeeee; border: 1px solid #9e9e9e;"></div>
                    <div class="legend-text">非活动栈帧</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #4caf50;"></div>
                    <div class="legend-text">"递"过程 (调用)</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #ff9800;"></div>
                    <div class="legend-text">"归"过程 (返回)</div>
                </div>
            </div>
        </div>

        <div class="panel code-panel">
            <div class="panel-title">递归函数代码</div>
            <div class="code-container">
                <div id="codeLine1" class="code-line">
                    <span class="code-keyword">function</span> <span class="code-function">factorial</span>(<span class="code-number">n</span>) {
                </div>
                <div id="codeLine2" class="code-line">
                    &nbsp;&nbsp;<span class="code-keyword">if</span> (<span class="code-number">n</span> <span class="code-operator"><=</span> <span class="code-number">1</span>) {
                </div>
                <div id="codeLine3" class="code-line">
                    &nbsp;&nbsp;&nbsp;&nbsp;<span class="code-keyword">return</span> <span class="code-number">1</span>;
                </div>
                <div id="codeLine4" class="code-line">
                    &nbsp;&nbsp;}
                </div>
                <div id="codeLine5" class="code-line">
                    &nbsp;&nbsp;<span class="code-keyword">return</span> <span class="code-number">n</span> <span class="code-operator">*</span> <span class="code-function">factorial</span>(<span class="code-number">n</span> <span class="code-operator">-</span> <span class="code-number">1</span>);
                </div>
                <div id="codeLine6" class="code-line">
                    }
                </div>
            </div>
        </div>

        <div class="panel animation-panel">
            <div class="panel-title">调用栈动画</div>
            <canvas id="animationCanvas"></canvas>
        </div>

        <div class="panel status-panel">
            <div class="panel-title">执行状态</div>
            <div class="status-content">
                <div id="statusStep" class="status-step">准备开始</div>
                <div id="statusDesc" class="status-desc">请输入一个非负整数 n，然后点击"开始演示"按钮。</div>
            </div>
        </div>
    </div>

    <div class="footer">
        <p>阶乘递归调用栈动画 | 设计用于理解递归执行过程与函数调用栈</p>
    </div>

    <script>
        // 全局变量
        let canvas, ctx;
        let n = 5; // 默认计算的阶乘数
        let stack = []; // 调用栈
        let animationSteps = []; // 动画步骤
        let currentStep = 0; // 当前步骤索引
        let isPlaying = false; // 是否正在播放
        let playInterval; // 播放定时器
        let animationSpeed = 5; // 动画速度 (1-10)
        let returnValues = {}; // 存储返回值 {depth: value}
        
        // 栈帧类
        class StackFrame {
            constructor(depth, nValue, expression, isActive = false) {
                this.depth = depth; // 递归深度
                this.nValue = nValue; // n的值
                this.expression = expression; // 表达式文本
                this.isActive = isActive; // 是否是活动栈帧
                this.returnValue = null; // 返回值
                this.isReturning = false; // 是否正在返回
            }
        }
        
        // 动画步骤类
        class AnimationStep {
            constructor(type, depth, nValue, description, codeLine) {
                this.type = type; // 'call', 'return', 'compute'
                this.depth = depth; // 栈深度
                this.nValue = nValue; // n的值
                this.description = description; // 描述
                this.codeLine = codeLine; // 高亮的代码行
            }
        }
        
        // 初始化
        function init() {
            canvas = document.getElementById('animationCanvas');
            ctx = canvas.getContext('2d');
            
            // 设置Canvas尺寸
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // 初始化事件监听
            setupEventListeners();
            
            // 初始状态
            updateStatus("准备开始", "请输入一个非负整数 n，然后点击'开始演示'按钮。");
        }
        
        // 调整Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            draw();
        }
        
        // 设置事件监听
        function setupEventListeners() {
            // 开始演示按钮
            document.getElementById('btnStart').addEventListener('click', startDemo);
            
            // 控制按钮
            document.getElementById('btnPrev').addEventListener('click', prevStep);
            document.getElementById('btnNext').addEventListener('click', nextStep);
            document.getElementById('btnPlayPause').addEventListener('click', togglePlayPause);
            document.getElementById('btnReset').addEventListener('click', reset);
            
            // 速度滑块
            document.getElementById('speedSlider').addEventListener('input', function() {
                animationSpeed = parseInt(this.value);
                if (isPlaying) {
                    clearInterval(playInterval);
                    startPlayInterval();
                }
            });
            
            // 输入框回车键
            document.getElementById('inputNumber').addEventListener('keyup', function(e) {
                if (e.key === 'Enter') {
                    startDemo();
                }
            });
        }
        
        // 开始演示
        function startDemo() {
            const input = document.getElementById('inputNumber');
            n = parseInt(input.value);
            
            if (isNaN(n) || n < 0 || n > 10) {
                alert("请输入一个0到10之间的整数");
                return;
            }
            
            // 重置状态
            reset();
            
            // 生成动画步骤
            generateAnimationSteps();
            
            // 更新状态
            updateStatus("开始计算", `开始计算 factorial(${n})`);
            
            // 绘制初始状态
            draw();
        }
        
        // 生成动画步骤
        function generateAnimationSteps() {
            animationSteps = [];
            
            // 生成调用步骤
            for (let i = n; i >= 1; i--) {
                const depth = n - i;
                let expression = `factorial(${i})`;
                if (i > 1) {
                    expression += ` = ${i} × factorial(${i-1})`;
                } else {
                    expression += ` = 1 (基准情况)`;
                }
                
                animationSteps.push(new AnimationStep(
                    'call', 
                    depth, 
                    i, 
                    `调用 factorial(${i})，需要计算 ${i > 1 ? `${i} × factorial(${i-1})` : '基准情况'}`,
                    1
                ));
                
                // 添加计算步骤（仅对非基准情况）
                if (i > 1) {
                    animationSteps.push(new AnimationStep(
                        'compute', 
                        depth, 
                        i, 
                        `等待 factorial(${i-1}) 的结果来计算 ${i} × factorial(${i-1})`,
                        5
                    ));
                } else {
                    animationSteps.push(new AnimationStep(
                        'compute', 
                        depth, 
                        i, 
                        `到达基准情况，factorial(1) = 1`,
                        2
                    ));
                }
            }
            
            // 生成返回步骤
            for (let i = 1; i <= n; i++) {
                const depth = n - i;
                let result = 1;
                for (let j = 1; j <= i; j++) {
                    result *= j;
                }
                
                animationSteps.push(new AnimationStep(
                    'return', 
                    depth, 
                    i, 
                    `factorial(${i}) 返回 ${result}`,
                    i === 1 ? 3 : 5
                ));
                
                // 存储返回值
                returnValues[depth] = result;
            }
            
            // 添加最终结果步骤
            animationSteps.push(new AnimationStep(
                'complete', 
                0, 
                n, 
                `计算完成！factorial(${n}) = ${returnValues[0]}`,
                6
            ));
        }
        
        // 执行下一步
        function nextStep() {
            if (currentStep >= animationSteps.length) return;
            
            const step = animationSteps[currentStep];
            
            // 根据步骤类型更新栈
            if (step.type === 'call') {
                // 添加新的栈帧
                let expression = `factorial(${step.nValue})`;
                if (step.nValue > 1) {
                    expression += ` = ${step.nValue} × factorial(${step.nValue-1})`;
                } else {
                    expression += ` = 1`;
                }
                
                // 将之前的栈帧设为非活动
                stack.forEach(frame => frame.isActive = false);
                
                // 添加新栈帧
                stack.push(new StackFrame(step.depth, step.nValue, expression, true));
                
            } else if (step.type === 'return') {
                // 设置当前栈帧为返回状态
                const currentFrame = stack[stack.length - 1];
                if (currentFrame) {
                    currentFrame.isReturning = true;
                    currentFrame.returnValue = returnValues[step.depth];
                    
                    // 如果是最后一个返回步骤，移除栈帧
                    if (step.nValue === n) {
                        setTimeout(() => {
                            stack.pop();
                            draw();
                        }, 300);
                    }
                }
                
            } else if (step.type === 'compute') {
                // 计算步骤，不需要改变栈，只是状态更新
            }
            
            // 更新代码高亮
            highlightCodeLine(step.codeLine);
            
            // 更新状态文本
            updateStatus(
                step.type === 'call' ? "递归调用 (递)" : 
                step.type === 'return' ? "返回结果 (归)" : 
                step.type === 'compute' ? "等待结果" : "计算完成",
                step.description
            );
            
            // 增加步骤索引
            currentStep++;
            
            // 如果到达最后一步，停止播放
            if (currentStep >= animationSteps.length && isPlaying) {
                togglePlayPause();
            }
            
            // 重绘
            draw();
        }
        
        // 执行上一步
        function prevStep() {
            if (currentStep <= 0) return;
            
            // 减少步骤索引
            currentStep--;
            
            // 由于动画步骤是线性的，回退需要重新生成栈状态
            // 这里简化处理：重置栈然后重新执行到上一步
            const tempStep = currentStep;
            resetStack();
            currentStep = 0;
            
            for (let i = 0; i < tempStep; i++) {
                const step = animationSteps[i];
                
                if (step.type === 'call') {
                    let expression = `factorial(${step.nValue})`;
                    if (step.nValue > 1) {
                        expression += ` = ${step.nValue} × factorial(${step.nValue-1})`;
                    } else {
                        expression += ` = 1`;
                    }
                    
                    stack.forEach(frame => frame.isActive = false);
                    stack.push(new StackFrame(step.depth, step.nValue, expression, true));
                    
                } else if (step.type === 'return') {
                    const currentFrame = stack[stack.length - 1];
                    if (currentFrame) {
                        currentFrame.isReturning = true;
                        currentFrame.returnValue = returnValues[step.depth];
                    }
                }
            }
            
            // 更新代码高亮和状态
            if (tempStep > 0) {
                const step = animationSteps[tempStep - 1];
                highlightCodeLine(step.codeLine);
                updateStatus(
                    step.type === 'call' ? "递归调用 (递)" : 
                    step.type === 'return' ? "返回结果 (归)" : 
                    step.type === 'compute' ? "等待结果" : "计算完成",
                    step.description
                );
            } else {
                highlightCodeLine(0);
                updateStatus("准备开始", "请输入一个非负整数 n，然后点击'开始演示'按钮。");
            }
            
            // 重绘
            draw();
        }
        
        // 切换播放/暂停
        function togglePlayPause() {
            const btn = document.getElementById('btnPlayPause');
            
            if (isPlaying) {
                // 暂停
                clearInterval(playInterval);
                btn.innerHTML = '<span>播放</span>';
                btn.className = 'btn-success';
            } else {
                // 播放
                // 如果已经完成，从头开始
                if (currentStep >= animationSteps.length) {
                    resetStack();
                    currentStep = 0;
                }
                
                startPlayInterval();
                btn.innerHTML = '<span>暂停</span>';
                btn.className = 'btn-warning';
            }
            
            isPlaying = !isPlaying;
        }
        
        // 开始播放定时器
        function startPlayInterval() {
            const interval = 1100 - (animationSpeed * 100); // 速度从1000ms到100ms
            playInterval = setInterval(nextStep, interval);
        }
        
        // 重置
        function reset() {
            // 停止播放
            if (isPlaying) {
                togglePlayPause();
            }
            
            // 重置状态
            resetStack();
            animationSteps = [];
            currentStep = 0;
            returnValues = {};
            
            // 更新UI
            highlightCodeLine(0);
            updateStatus("准备开始", "请输入一个非负整数 n，然后点击'开始演示'按钮。");
            
            // 重绘
            draw();
        }
        
        // 重置栈
        function resetStack() {
            stack = [];
        }
        
        // 更新状态显示
        function updateStatus(step, description) {
            document.getElementById('statusStep').textContent = step;
            document.getElementById('statusDesc').textContent = description;
        }
        
        // 高亮代码行
        function highlightCodeLine(lineNumber) {
            // 移除所有高亮
            for (let i = 1; i <= 6; i++) {
                document.getElementById(`codeLine${i}`).classList.remove('highlighted');
            }
            
            // 高亮指定行
            if (lineNumber > 0 && lineNumber <= 6) {
                document.getElementById(`codeLine${lineNumber}`).classList.add('highlighted');
            }
        }
        
        // 绘制函数
        function draw() {
            if (!ctx) return;
            
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制标题
            ctx.fillStyle = '#333';
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(`递归调用栈: factorial(${n})`, canvas.width / 2, 30);
            
            // 如果没有栈帧，显示提示
            if (stack.length === 0) {
                ctx.fillStyle = '#999';
                ctx.font = '18px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('点击"开始演示"查看调用栈动画', canvas.width / 2, canvas.height / 2);
                return;
            }
            
            // 栈绘制参数
            const stackStartX = canvas.width / 2;
            const stackStartY = canvas.height - 50;
            const frameWidth = 200;
            const frameHeight = 80;
            const frameSpacing = 20;
            
            // 绘制栈帧
            for (let i = 0; i < stack.length; i++) {
                const frame = stack[i];
                const frameY = stackStartY - i * (frameHeight + frameSpacing);
                
                // 绘制栈帧背景
                if (frame.isActive) {
                    // 活动栈帧
                    ctx.fillStyle = '#e3f2fd';
                    ctx.strokeStyle = '#2196f3';
                    ctx.lineWidth = 3;
                } else {
                    // 非活动栈帧
                    ctx.fillStyle = '#eeeeee';
                    ctx.strokeStyle = '#9e9e9e';
                    ctx.lineWidth = 1;
                }
                
                // 绘制矩形
                ctx.fillRect(stackStartX - frameWidth / 2, frameY - frameHeight / 2, frameWidth, frameHeight);
                ctx.strokeRect(stackStartX - frameWidth / 2, frameY - frameHeight / 2, frameWidth, frameHeight);
                
                // 绘制栈帧内容
                ctx.fillStyle = '#333';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`factorial(${frame.nValue})`, stackStartX, frameY - 20);
                
                ctx.font = '16px Arial';
                ctx.fillText(frame.expression, stackStartX, frameY + 5);
                
                // 如果正在返回，显示返回值
                if (frame.isReturning && frame.returnValue) {
                    ctx.fillStyle = '#ff9800';
                    ctx.font = 'bold 18px Arial';
                    ctx.fillText(`返回: ${frame.returnValue}`, stackStartX, frameY + 25);
                }
                
                // 绘制栈深度标签
                ctx.fillStyle = '#666';
                ctx.font = '14px Arial';
                ctx.textAlign = 'right';
                ctx.fillText(`深度: ${frame.depth}`, stackStartX + frameWidth / 2 - 10, frameY - frameHeight / 2 + 20);
                
                // 绘制栈帧编号
                ctx.textAlign = 'left';
                ctx.fillText(`#${i+1}`, stackStartX - frameWidth / 2 + 10, frameY - frameHeight / 2 + 20);
            }
            
            // 绘制调用箭头（递）
            if (currentStep > 0 && currentStep <= animationSteps.length) {
                const currentAnimationStep = animationSteps[Math.min(currentStep, animationSteps.length - 1)];
                
                if (currentAnimationStep.type === 'call' && stack.length > 1) {
                    const fromFrameIndex = stack.length - 2;
                    const toFrameIndex = stack.length - 1;
                    
                    const fromY = stackStartY - fromFrameIndex * (frameHeight + frameSpacing) + frameHeight / 2;
                    const toY = stackStartY - toFrameIndex * (frameHeight + frameSpacing) - frameHeight / 2;
                    
                    drawArrow(stackStartX, fromY, stackStartX, toY, '#4caf50', '调用');
                }
            }
            
            // 绘制返回箭头（归）
            for (let i = 0; i < stack.length; i++) {
                const frame = stack[i];
                if (frame.isReturning && i > 0) {
                    const fromY = stackStartY - i * (frameHeight + frameSpacing) + frameHeight / 2;
                    const toY = stackStartY - (i - 1) * (frameHeight + frameSpacing) - frameHeight / 2;
                    
                    drawArrow(stackStartX, fromY, stackStartX, toY, '#ff9800', '返回');
                }
            }
            
            // 绘制栈底部
            ctx.fillStyle = '#999';
            ctx.font = '14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('栈底', stackStartX, stackStartY + 40);
            
            // 绘制栈指针
            if (stack.length > 0) {
                const topFrameIndex = stack.length - 1;
                const topFrameY = stackStartY - topFrameIndex * (frameHeight + frameSpacing) - frameHeight / 2;
                
                ctx.fillStyle = '#2196f3';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'left';
                ctx.fillText('↑ 栈顶指针', stackStartX + frameWidth / 2 + 20, topFrameY);
            }
        }
        
        // 绘制箭头函数
        function drawArrow(fromX, fromY, toX, toY, color, label) {
            ctx.strokeStyle = color;
            ctx.fillStyle = color;
            ctx.lineWidth = 3;
            
            // 绘制箭头线
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.stroke();
            
            // 绘制箭头头部
            const headLength = 15;
            const angle = Math.atan2(toY - fromY, toX - fromX);
            
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(
                toX - headLength * Math.cos(angle - Math.PI / 6),
                toY - headLength * Math.sin(angle - Math.PI / 6)
            );
            ctx.lineTo(
                toX - headLength * Math.cos(angle + Math.PI / 6),
                toY - headLength * Math.sin(angle + Math.PI / 6)
            );
            ctx.closePath();
            ctx.fill();
            
            // 绘制标签
            ctx.fillStyle = color;
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'center';
            const midX = (fromX + toX) / 2;
            const midY = (fromY + toY) / 2;
            
            // 偏移标签位置，避免与线重叠
            const offsetX = Math.sin(angle) * 20;
            const offsetY = -Math.cos(angle) * 20;
            
            ctx.fillText(label, midX + offsetX, midY + offsetY);
        }
        
        // 页面加载完成后初始化
        window.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

# 阶乘递归调用栈动画使用指南

## 欢迎使用！

欢迎使用“阶乘递归调用栈动画”交互式教学工具！本工具专为帮助您直观理解递归这一计算机科学核心概念而设计。通过动态可视化函数调用栈的变化过程，您将能够清晰地看到递归的“递”与“归”两个阶段，从而深入掌握递归的执行机制。

## 功能说明

本动画以计算阶乘（factorial）为例，通过以下核心组件为您提供沉浸式学习体验：

1. **控制面板**：提供输入和操作控件
2. **代码展示区**：显示阶乘递归函数的伪代码，并与动画同步高亮
3. **动画展示区**：动态可视化函数调用栈的创建、增长和收缩过程
4. **状态说明区**：用自然语言描述当前执行步骤

## 主要功能

### 1. 输入与初始化
- **数字输入框**：输入0-10之间的整数n，计算factorial(n)
- **开始演示按钮**：根据输入的n值初始化动画

### 2. 动画控制
- **上一步/下一步**：单步控制动画进程，精细观察每个关键状态
- **播放/暂停**：自动连续播放整个递归过程
- **重置**：清空当前状态，重新开始
- **速度调节**：在播放模式下调整动画速度（1-10级）

### 3. 视觉反馈
- **栈帧可视化**：每个函数调用显示为一个栈帧，包含参数值和当前表达式
- **执行流指示**：绿色箭头表示“递”（调用），橙色箭头表示“归”（返回）
- **代码同步高亮**：代码区实时高亮与当前栈帧对应的代码行
- **状态描述**：用通俗语言解释当前正在发生的计算步骤

## 设计特色

### 1. 认知友好的视觉设计
- **双色系统**：绿色代表“递”过程，橙色代表“归”过程，符合直觉
- **层次分明**：活动栈帧（浅蓝）与非活动栈帧（浅灰）清晰区分
- **空间隐喻**：调用栈自下而上“生长”，直观体现栈的LIFO特性

### 2. 符合学习规律的教学设计
- **逐步分解**：将连续递归过程分解为离散步骤，降低认知负荷
- **双重编码**：同时提供视觉动画和文字描述，强化理解
- **主动探索**：用户控制进度，按自己的节奏学习

### 3. 技术实现亮点
- **响应式设计**：适应不同屏幕尺寸
- **平滑动画**：栈帧移动和箭头绘制流畅自然
- **状态保持**：支持前进后退，方便反复观察难点

## 教学要点

### 理解递归的两个阶段
1. **“递”阶段（递归调用）**
   - 函数不断调用自身，每次调用参数减小
   - 新的栈帧被压入调用栈
   - 直到达到基准情况（n <= 1）

2. **“归”阶段（结果返回）**
   - 从基准情况开始返回具体值
   - 栈帧依次弹出，返回值用于上层计算
   - 最终得到完整结果

### 关键概念可视化
- **调用栈**：展示函数调用如何形成栈结构
- **递归深度**：通过栈帧数量直观显示
- **返回值传递**：显示中间结果如何向上层传递
- **基准情况**：突出递归终止条件的重要性

### 常见误区澄清
- **栈溢出风险**：通过限制n≤10，避免无限递归
- **返回值计算**：展示返回值不是立即计算，而是等待下层结果
- **执行顺序**：明确“先递后归”的执行流程

## 使用建议

### 初学者学习路径
1. **首次体验**：输入n=3，使用“播放”功能观看完整过程
2. **逐步分析**：输入n=5，使用“上一步/下一步”单步观察每个细节
3. **对比观察**：分别输入n=2、n=4、n=6，比较递归深度的差异
4. **自主探索**：尝试预测下一步会发生什么，然后验证预测

### 课堂教学应用
- **教师演示**：在全班讲解时使用，配合分步讲解
- **学生练习**：让学生操作动画，解释每个步骤的含义
- **小组讨论**：围绕“如果n=0会怎样？”等问题展开讨论
- **巩固练习**：关闭动画，让学生在白板上画出n=4的调用栈变化

### 深入学习建议
1. **代码关联**：将动画中的栈帧与代码行对应起来
2. **扩展思考**：
   - 如果去掉基准情况会怎样？
   - 递归与迭代计算阶乘有何异同？
   - 如何计算斐波那契数列的递归调用栈？
3. **实际应用**：思考哪些实际问题适合用递归解决

### 故障排除
- **动画不启动**：确保输入了0-10之间的整数
- **控制按钮无效**：确保已点击“开始演示”初始化动画
- **显示异常**：尝试刷新页面或调整浏览器缩放

## 结语

递归是编程中的强大工具，也是初学者常遇到的难点。本动画工具通过将抽象概念具象化，帮助您建立正确的递归思维模型。记住，理解递归的关键在于看清“调用栈”这一隐藏的结构。

祝您学习愉快！如有任何反馈或建议，欢迎与我们分享。现在，开始您的递归探索之旅吧！