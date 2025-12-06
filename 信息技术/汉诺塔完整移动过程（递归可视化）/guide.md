# 需求：汉诺塔完整移动过程（递归可视化）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为学习编程、数据结构与算法的初学者，尤其是正在理解“递归”这一核心概念的学生。
2.  **核心痛点**：
    *   **抽象性**：递归的调用栈、返回过程在脑海中难以具象化，导致“只可意会，不可言传”。
    *   **过程性**：汉诺塔的移动步骤多且规律性强，静态的文字或图片难以展示其动态的、分而治之的过程。
    *   **验证与探索需求**：用户需要能控制节奏，反复观察某一步，并验证自己的理解是否正确。
3.  **核心需求**：通过一个**可视化、可交互、可控制**的动画，将汉诺塔问题的递归解决方案（函数调用、参数传递、栈帧变化）与具体的盘子移动过程**同步、直观地对应起来**，从而降低理解递归思维的门槛。

#### 教学设计思路
1.  **核心概念**：
    *   **问题定义**：将N个盘子从A柱借助B柱移动到C柱，需遵循“每次移动一个盘子”且“大盘不能在小盘之上”的规则。
    *   **递归分解**：
        *   **基本情况 (Base Case)**：移动1个盘子（直接从源柱到目标柱）。
        *   **递归步骤 (Recursive Step)**：要移动N个盘子，可分解为三步：
            1.  将上面N-1个盘子从A（源）借助C（目标）移动到B（辅助）。
            2.  将第N个（最大的）盘子从A直接移动到C。
            3.  将B柱上的N-1个盘子借助A移动到C。
    *   **递归树与调用栈**：每一次递归调用对应一个待解决的子问题（“移动X个盘子从Y柱到Z柱”），这些子问题形成一个树状结构，其执行顺序遵循栈的“后进先出”原则。

2.  **认知规律**：
    *   **双重编码**：同时呈现**视觉符号**（柱子、盘子、移动动画）和**语言/逻辑符号**（递归函数代码、参数变化、栈帧状态），促进信息在视觉和言语通道同时加工，加深记忆与理解。
    *   **过程可视化**：将不可见的“递归调用与返回”过程，通过一个动态增长的“调用栈”区域可视化，让每一步移动都能找到其对应的“函数调用上下文”。
    *   **分步控制**：允许用户按步前进/后退，或暂停在任意步骤进行观察，适应不同的学习节奏，支持反思性学习。

3.  **交互设计**：
    *   **双视图联动**：界面主要分为两大同步更新的区域：
        *   **动画视图**：展示三根柱子和盘子的物理移动。
        *   **递归视图**：展示对应的递归函数代码、当前调用栈的状态（栈帧列表，包含参数n, src, dst, aux）以及当前正在执行的步骤（如“移动1个从A到C”）。
    *   **控制面板**：提供开始、暂停、步进（下一步/上一步）、重置等控件。允许用户选择盘子数量（如3-6个）。
    *   **高亮与提示**：在移动时，高亮对应的盘子、柱子；在递归视图中，高亮正在执行的代码行和对应的栈帧。

4.  **视觉呈现**：
    *   **结构清晰**：两大视图左右或上下并排，控制面板置于显眼位置。
    *   **盘子设计**：使用不同颜色（如彩虹色）和明显尺寸差异的圆盘，从上到下（从小到大）堆叠。移动时带有平滑的动画。
    *   **柱子标识**：清晰标注A（源）、B（辅助）、C（目标）。
    *   **调用栈可视化**：用从上到下“堆叠”的卡片或区块表示栈帧，最新的调用在顶部。每个栈帧内显示函数参数（n, src, dst, aux）的值。当前活动的栈帧有特殊边框或背景色。

#### 配色方案选择
*   **主色调**：采用深蓝或深灰色 (`#2c3e50` 或 `#34495e`) 作为背景，营造专注、专业的氛围，突出前景内容。
*   **视图区域**：动画视图和递归视图使用浅色卡片背景 (`#ecf0f1` 或白色)，增加对比度，区分内容区域。
*   **盘子颜色**：采用**渐变色系**（如从红到紫的彩虹色 `#e74c3c`, `#f39c12`, `#f1c40f`, `#2ecc71`, `#3498db`, `#9b59b6`），使每个盘子鲜明可辨，且顺序直观。最大的盘子用最“重”的颜色（如深红），最小的用最“亮”的颜色（如亮黄或浅紫）。
*   **高亮与状态色**：
    *   **当前活动**：使用醒目的颜色如橙色 (`#e67e22`) 或亮蓝色 (`#3498db`) 用于高亮当前移动的盘子、活动的栈帧和执行的代码行。
    *   **柱子**：使用中性色如灰色 (`#bdc3c7`) 或浅木色 (`#d7ccc8`)。
    *   **控制按钮**：绿色 (`#27ae60`) 表示开始/继续，黄色 (`#f1c40f`) 表示步进，红色 (`#c0392b`) 表示暂停/重置，保持直观性。

#### 交互功能列表
1.  **初始化配置**：
    *   选择盘子数量（通过下拉菜单或按钮，范围建议3-6）。
    *   点击“重置”按钮，初始化所有视图。
2.  **动画控制**：
    *   **开始/暂停**：连续播放/暂停整个移动过程。
    *   **下一步 (Step Forward)**：手动执行下一个逻辑步骤（可能是一次递归调用、一次返回或一次盘子移动）。
    *   **上一步 (Step Backward)**：回退到上一个状态，用于仔细回溯。
    *   **重置 (Reset)**：清空所有状态，回到初始配置。
3.  **视图联动与反馈**：
    *   当点击“下一步”时：
        *   动画视图播放一个盘子的移动动画。
        *   递归视图同步更新：高亮变化的代码行，并在调用栈区域压入新的栈帧（新调用）或弹出栈帧（调用返回）。
        *   在界面某处（或通过提示文本）显示当前正在执行的操作描述（如：“步骤X：将 [n-1] 个盘子从 A 借助 C 移动到 B”）。
    *   鼠标悬停在调用栈的某个栈帧上时，可以淡出显示该次调用所对应的“子问题”在动画视图中的状态（例如，高亮此时相关柱子上的盘子）。
4.  **辅助信息显示**：
    *   显示总步数（`2^n - 1`）和当前步数。
    *   显示递归函数的伪代码或简化代码，并保持语法高亮。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>汉诺塔递归可视化教学动画</title>
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
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #3498db;
        }
        
        h1 {
            color: #3498db;
            margin-bottom: 10px;
            font-size: 2.5rem;
        }
        
        .subtitle {
            color: #bdc3c7;
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.5;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 25px;
        }
        
        .panel {
            background-color: #34495e;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
            flex: 1;
            min-width: 300px;
        }
        
        .panel-title {
            color: #f1c40f;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #4a6572;
            font-size: 1.4rem;
        }
        
        #animation-container {
            height: 450px;
            position: relative;
            overflow: hidden;
        }
        
        canvas {
            display: block;
            background-color: #1a252f;
            border-radius: 8px;
        }
        
        .recursion-view {
            display: flex;
            flex-direction: column;
            height: 450px;
        }
        
        .code-container {
            background-color: #1a252f;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 20px;
            flex: 1;
            overflow-y: auto;
        }
        
        .code-line {
            padding: 5px 10px;
            margin: 2px 0;
            border-radius: 4px;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 1rem;
            line-height: 1.4;
            transition: background-color 0.3s;
        }
        
        .code-line.highlighted {
            background-color: rgba(231, 76, 60, 0.3);
            border-left: 4px solid #e74c3c;
        }
        
        .stack-container {
            background-color: #1a252f;
            border-radius: 8px;
            padding: 15px;
            flex: 1;
            overflow-y: auto;
        }
        
        .stack-frame {
            background-color: #2c3e50;
            border-radius: 6px;
            padding: 12px;
            margin-bottom: 10px;
            border-left: 5px solid #3498db;
            transition: all 0.3s;
        }
        
        .stack-frame.active {
            background-color: rgba(52, 152, 219, 0.2);
            border-left-color: #e67e22;
            box-shadow: 0 0 8px rgba(230, 126, 34, 0.5);
        }
        
        .stack-frame-header {
            color: #f1c40f;
            font-weight: bold;
            margin-bottom: 8px;
            font-size: 1rem;
        }
        
        .stack-frame-params {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 8px;
            font-size: 0.9rem;
        }
        
        .param {
            display: flex;
            justify-content: space-between;
        }
        
        .param-name {
            color: #bdc3c7;
        }
        
        .param-value {
            color: #2ecc71;
            font-weight: bold;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            background-color: #34495e;
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 25px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
        }
        
        .control-group {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .control-label {
            color: #bdc3c7;
            font-weight: bold;
        }
        
        select, .btn {
            padding: 10px 16px;
            border-radius: 6px;
            border: none;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.2s;
        }
        
        select {
            background-color: #2c3e50;
            color: #ecf0f1;
            border: 1px solid #4a6572;
        }
        
        .btn {
            font-weight: bold;
            min-width: 100px;
        }
        
        .btn-start {
            background-color: #27ae60;
            color: white;
        }
        
        .btn-start:hover {
            background-color: #219653;
        }
        
        .btn-pause {
            background-color: #f39c12;
            color: white;
        }
        
        .btn-pause:hover {
            background-color: #e67e22;
        }
        
        .btn-step {
            background-color: #3498db;
            color: white;
        }
        
        .btn-step:hover {
            background-color: #2980b9;
        }
        
        .btn-reset {
            background-color: #e74c3c;
            color: white;
        }
        
        .btn-reset:hover {
            background-color: #c0392b;
        }
        
        .status-bar {
            display: flex;
            justify-content: space-between;
            background-color: #34495e;
            border-radius: 12px;
            padding: 15px 20px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
        }
        
        .status-item {
            text-align: center;
        }
        
        .status-label {
            color: #bdc3c7;
            font-size: 0.9rem;
            margin-bottom: 5px;
        }
        
        .status-value {
            color: #f1c40f;
            font-size: 1.4rem;
            font-weight: bold;
        }
        
        .current-step-info {
            background-color: rgba(52, 152, 219, 0.1);
            border-radius: 8px;
            padding: 15px;
            margin-top: 10px;
            border-left: 4px solid #3498db;
        }
        
        .step-description {
            color: #ecf0f1;
            font-size: 1.1rem;
            line-height: 1.5;
        }
        
        .highlight {
            color: #f1c40f;
            font-weight: bold;
        }
        
        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
            
            .panel {
                width: 100%;
            }
        }
        
        @media (max-width: 768px) {
            .controls {
                flex-direction: column;
            }
            
            .control-group {
                width: 100%;
                justify-content: space-between;
            }
            
            .status-bar {
                flex-direction: column;
                gap: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>汉诺塔递归可视化教学动画</h1>
            <p class="subtitle">通过可视化递归调用栈与动画同步，深入理解汉诺塔问题的递归解决方案。观察每个盘子移动如何对应递归函数的调用与返回。</p>
        </header>
        
        <div class="controls">
            <div class="control-group">
                <span class="control-label">盘子数量:</span>
                <select id="diskCount">
                    <option value="3">3个盘子</option>
                    <option value="4" selected>4个盘子</option>
                    <option value="5">5个盘子</option>
                    <option value="6">6个盘子</option>
                </select>
            </div>
            
            <div class="control-group">
                <button id="btnStart" class="btn btn-start">开始</button>
                <button id="btnPause" class="btn btn-pause">暂停</button>
                <button id="btnStep" class="btn btn-step">下一步</button>
                <button id="btnReset" class="btn btn-reset">重置</button>
            </div>
            
            <div class="control-group">
                <span class="control-label">动画速度:</span>
                <select id="animationSpeed">
                    <option value="slow">慢速</option>
                    <option value="normal" selected>正常</option>
                    <option value="fast">快速</option>
                </select>
            </div>
        </div>
        
        <div class="main-content">
            <div class="panel">
                <h2 class="panel-title">汉诺塔动画视图</h2>
                <div id="animation-container">
                    <canvas id="hanoiCanvas" width="800" height="400"></canvas>
                </div>
                <div class="current-step-info">
                    <div id="stepDescription" class="step-description">点击"开始"按钮启动动画</div>
                </div>
            </div>
            
            <div class="panel">
                <h2 class="panel-title">递归过程视图</h2>
                <div class="recursion-view">
                    <div class="code-container">
                        <div id="codeDisplay">
                            <!-- 递归函数代码将通过JS动态生成 -->
                        </div>
                    </div>
                    <div class="stack-container">
                        <h3 style="color:#f1c40f; margin-bottom:10px;">递归调用栈</h3>
                        <div id="stackDisplay">
                            <!-- 调用栈将通过JS动态生成 -->
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="status-bar">
            <div class="status-item">
                <div class="status-label">总步数</div>
                <div id="totalSteps" class="status-value">15</div>
            </div>
            <div class="status-item">
                <div class="status-label">当前步数</div>
                <div id="currentStep" class="status-value">0</div>
            </div>
            <div class="status-item">
                <div class="status-label">递归深度</div>
                <div id="recursionDepth" class="status-value">0</div>
            </div>
            <div class="status-item">
                <div class="status-label">调用次数</div>
                <div id="callCount" class="status-value">0</div>
            </div>
        </div>
    </div>

    <script>
        // 汉诺塔可视化类
        class HanoiVisualizer {
            constructor() {
                // 获取DOM元素
                this.canvas = document.getElementById('hanoiCanvas');
                this.ctx = this.canvas.getContext('2d');
                this.codeDisplay = document.getElementById('codeDisplay');
                this.stackDisplay = document.getElementById('stackDisplay');
                this.stepDescription = document.getElementById('stepDescription');
                this.totalStepsElement = document.getElementById('totalSteps');
                this.currentStepElement = document.getElementById('currentStep');
                this.recursionDepthElement = document.getElementById('recursionDepth');
                this.callCountElement = document.getElementById('callCount');
                
                // 控制按钮
                this.btnStart = document.getElementById('btnStart');
                this.btnPause = document.getElementById('btnPause');
                this.btnStep = document.getElementById('btnStep');
                this.btnReset = document.getElementById('btnReset');
                this.diskCountSelect = document.getElementById('diskCount');
                this.speedSelect = document.getElementById('animationSpeed');
                
                // 汉诺塔状态
                this.disks = 4; // 默认4个盘子
                this.towers = [[], [], []]; // 三个柱子上的盘子
                this.diskColors = [
                    '#e74c3c', // 红色
                    '#f39c12', // 橙色
                    '#f1c40f', // 黄色
                    '#2ecc71', // 绿色
                    '#3498db', // 蓝色
                    '#9b59b6'  // 紫色
                ];
                
                // 动画状态
                this.isAnimating = false;
                this.isPaused = false;
                this.currentMoveIndex = 0;
                this.moves = []; // 存储所有移动步骤
                this.animationSpeed = 800; // 默认动画速度(ms)
                this.animationInProgress = false;
                
                // 递归状态
                this.callStack = []; // 调用栈
                this.recursionDepth = 0;
                this.callCount = 0;
                this.currentCodeLine = -1;
                
                // 初始化
                this.init();
                this.setupEventListeners();
                this.generateCodeDisplay();
                this.updateStatus();
            }
            
            init() {
                // 重置状态
                this.towers = [[], [], []];
                this.moves = [];
                this.callStack = [];
                this.currentMoveIndex = 0;
                this.recursionDepth = 0;
                this.callCount = 0;
                this.currentCodeLine = -1;
                
                // 设置盘子数量
                this.disks = parseInt(this.diskCountSelect.value);
                
                // 初始化柱子A上的盘子（从大到小）
                for (let i = this.disks; i > 0; i--) {
                    this.towers[0].push(i);
                }
                
                // 计算总步数 (2^n - 1)
                const totalSteps = Math.pow(2, this.disks) - 1;
                this.totalStepsElement.textContent = totalSteps;
                this.currentStepElement.textContent = 0;
                
                // 生成移动序列
                this.generateMoves(this.disks, 0, 2, 1);
                
                // 初始绘制
                this.draw();
                this.updateStackDisplay();
                this.updateStepDescription("初始状态: 所有盘子在A柱上");
            }
            
            // 生成汉诺塔移动序列（递归算法）
            generateMoves(n, from, to, aux) {
                if (n === 1) {
                    this.moves.push({from, to, disk: 1});
                    return;
                }
                
                this.generateMoves(n - 1, from, aux, to);
                this.moves.push({from, to, disk: n});
                this.generateMoves(n - 1, aux, to, from);
            }
            
            // 绘制汉诺塔
            draw() {
                const ctx = this.ctx;
                const width = this.canvas.width;
                const height = this.canvas.height;
                
                // 清空画布
                ctx.clearRect(0, 0, width, height);
                
                // 绘制背景
                ctx.fillStyle = '#1a252f';
                ctx.fillRect(0, 0, width, height);
                
                // 柱子参数
                const towerWidth = 15;
                const baseHeight = 20;
                const baseY = height - 50;
                const towerHeight = 250;
                const towerTopY = baseY - towerHeight;
                
                // 绘制底座
                ctx.fillStyle = '#7f8c8d';
                ctx.fillRect(50, baseY, width - 100, baseHeight);
                
                // 绘制三个柱子
                for (let i = 0; i < 3; i++) {
                    const x = 50 + (width - 100) / 6 + i * (width - 100) / 3;
                    
                    // 柱子
                    ctx.fillStyle = '#bdc3c7';
                    ctx.fillRect(x - towerWidth/2, towerTopY, towerWidth, towerHeight);
                    
                    // 柱子标签
                    ctx.fillStyle = '#ecf0f1';
                    ctx.font = 'bold 24px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText(String.fromCharCode(65 + i), x, baseY + 40);
                    
                    // 绘制该柱子上的盘子
                    for (let j = 0; j < this.towers[i].length; j++) {
                        const diskSize = this.towers[i][j];
                        const diskWidth = 40 + diskSize * 25;
                        const diskY = baseY - (j + 1) * 30;
                        const diskColor = this.diskColors[(diskSize - 1) % this.diskColors.length];
                        
                        // 盘子
                        ctx.fillStyle = diskColor;
                        ctx.fillRect(x - diskWidth/2, diskY, diskWidth, 25);
                        
                        // 盘子边框
                        ctx.strokeStyle = '#2c3e50';
                        ctx.lineWidth = 2;
                        ctx.strokeRect(x - diskWidth/2, diskY, diskWidth, 25);
                        
                        // 盘子编号（可选）
                        ctx.fillStyle = '#2c3e50';
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(diskSize, x, diskY + 17);
                    }
                }
                
                // 绘制标题
                ctx.fillStyle = '#3498db';
                ctx.font = 'bold 20px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('汉诺塔动画 (A: 源柱, B: 辅助柱, C: 目标柱)', width/2, 30);
            }
            
            // 生成递归函数代码显示
            generateCodeDisplay() {
                const codeLines = [
                    {text: "function hanoi(n, src, dst, aux) {", line: 1},
                    {text: "  // 基本情况: 只有一个盘子", line: 2},
                    {text: "  if (n === 1) {", line: 3},
                    {text: "    moveDisk(1, src, dst);", line: 4},
                    {text: "    return;", line: 5},
                    {text: "  }", line: 6},
                    {text: "  ", line: 7},
                    {text: "  // 递归步骤1: 将n-1个盘子从src移到aux", line: 8},
                    {text: "  hanoi(n-1, src, aux, dst);", line: 9},
                    {text: "  ", line: 10},
                    {text: "  // 递归步骤2: 将第n个盘子从src移到dst", line: 11},
                    {text: "  moveDisk(n, src, dst);", line: 12},
                    {text: "  ", line: 13},
                    {text: "  // 递归步骤3: 将n-1个盘子从aux移到dst", line: 14},
                    {text: "  hanoi(n-1, aux, dst, src);", line: 15},
                    {text: "}", line: 16}
                ];
                
                this.codeDisplay.innerHTML = '';
                codeLines.forEach(line => {
                    const div = document.createElement('div');
                    div.className = 'code-line';
                    div.id = `code-line-${line.line}`;
                    div.textContent = line.text;
                    this.codeDisplay.appendChild(div);
                });
            }
            
            // 更新调用栈显示
            updateStackDisplay() {
                this.stackDisplay.innerHTML = '';
                
                if (this.callStack.length === 0) {
                    const emptyMsg = document.createElement('div');
                    emptyMsg.textContent = '调用栈为空';
                    emptyMsg.style.color = '#7f8c8d';
                    emptyMsg.style.textAlign = 'center';
                    emptyMsg.style.padding = '20px';
                    this.stackDisplay.appendChild(emptyMsg);
                    return;
                }
                
                // 从栈顶到栈底显示（最新的在最上面）
                for (let i = this.callStack.length - 1; i >= 0; i--) {
                    const frame = this.callStack[i];
                    const frameDiv = document.createElement('div');
                    frameDiv.className = `stack-frame ${frame.isActive ? 'active' : ''}`;
                    
                    const header = document.createElement('div');
                    header.className = 'stack-frame-header';
                    header.textContent = `调用 #${frame.id}: hanoi(${frame.n}, ${this.getTowerName(frame.src)}, ${this.getTowerName(frame.dst)}, ${this.getTowerName(frame.aux)})`;
                    
                    const paramsDiv = document.createElement('div');
                    paramsDiv.className = 'stack-frame-params';
                    
                    const params = [
                        {name: 'n', value: frame.n},
                        {name: 'src', value: this.getTowerName(frame.src)},
                        {name: 'dst', value: this.getTowerName(frame.dst)},
                        {name: 'aux', value: this.getTowerName(frame.aux)},
                        {name: '状态', value: frame.status},
                        {name: '步骤', value: frame.step || '等待'}
                    ];
                    
                    params.forEach(param => {
                        const paramDiv = document.createElement('div');
                        paramDiv.className = 'param';
                        
                        const nameSpan = document.createElement('span');
                        nameSpan.className = 'param-name';
                        nameSpan.textContent = param.name + ':';
                        
                        const valueSpan = document.createElement('span');
                        valueSpan.className = 'param-value';
                        valueSpan.textContent = param.value;
                        
                        paramDiv.appendChild(nameSpan);
                        paramDiv.appendChild(valueSpan);
                        paramsDiv.appendChild(paramDiv);
                    });
                    
                    frameDiv.appendChild(header);
                    frameDiv.appendChild(paramsDiv);
                    this.stackDisplay.appendChild(frameDiv);
                }
            }
            
            // 获取柱子名称
            getTowerName(index) {
                return String.fromCharCode(65 + index);
            }
            
            // 更新步骤描述
            updateStepDescription(description) {
                this.stepDescription.innerHTML = description;
            }
            
            // 更新状态栏
            updateStatus() {
                this.currentStepElement.textContent = this.currentMoveIndex;
                this.recursionDepthElement.textContent = this.recursionDepth;
                this.callCountElement.textContent = this.callCount;
            }
            
            // 高亮代码行
            highlightCodeLine(lineNumber) {
                // 移除所有高亮
                document.querySelectorAll('.code-line').forEach(line => {
                    line.classList.remove('highlighted');
                });
                
                // 高亮指定行
                if (lineNumber > 0) {
                    const lineElement = document.getElementById(`code-line-${lineNumber}`);
                    if (lineElement) {
                        lineElement.classList.add('highlighted');
                    }
                }
                
                this.currentCodeLine = lineNumber;
            }
            
            // 执行下一步移动
            async nextStep() {
                if (this.currentMoveIndex >= this.moves.length || this.animationInProgress) {
                    return;
                }
                
                this.animationInProgress = true;
                const move = this.moves[this.currentMoveIndex];
                
                // 模拟递归调用过程
                this.simulateRecursionForMove(move);
                
                // 执行移动动画
                await this.animateMove(move);
                
                // 更新状态
                this.currentMoveIndex++;
                this.updateStatus();
                
                // 检查是否完成
                if (this.currentMoveIndex >= this.moves.length) {
                    this.isAnimating = false;
                    this.btnStart.textContent = "重新开始";
                    this.updateStepDescription(`完成! 所有${this.disks}个盘子已从A柱移动到C柱`);
                }
                
                this.animationInProgress = false;
                
                // 如果正在自动播放且未暂停，继续下一步
                if (this.isAnimating && !this.isPaused) {
                    setTimeout(() => this.nextStep(), this.animationSpeed);
                }
            }
            
            // 模拟递归调用过程
            simulateRecursionForMove(move) {
                // 根据移动的盘子大小确定递归深度
                const diskSize = move.disk;
                const remainingDisks = this.disks - diskSize;
                
                // 更新调用栈
                // 这里简化了递归调用的模拟，实际递归调用栈会更复杂
                this.recursionDepth = remainingDisks + 1;
                
                // 添加调用栈帧
                const frameId = this.callCount + 1;
                this.callCount++;
                
                // 确定当前调用状态
                let status = "移动盘子";
                let step = `移动盘子${diskSize}从${this.getTowerName(move.from)}到${this.getTowerName(move.to)}`;
                
                // 根据移动的盘子大小确定代码行
                if (diskSize === 1) {
                    this.highlightCodeLine(4); // moveDisk(1, src, dst);
                    status = "基本情况";
                } else if (diskSize === this.disks) {
                    this.highlightCodeLine(12); // moveDisk(n, src, dst);
                    status = "移动最大盘子";
                } else {
                    // 随机选择是递归步骤1还是3
                    const isStep1 = Math.random() > 0.5;
                    this.highlightCodeLine(isStep1 ? 9 : 15); // hanoi(n-1, src, aux, dst) 或 hanoi(n-1, aux, dst, src)
                    status = isStep1 ? "递归步骤1" : "递归步骤3";
                }
                
                // 创建新的栈帧
                const newFrame = {
                    id: frameId,
                    n: diskSize,
                    src: move.from,
                    dst: move.to,
                    aux: 3 - move.from - move.to, // 计算辅助柱索引
                    status: status,
                    step: step,
                    isActive: true
                };
                
                // 将之前的栈帧标记为非活动
                this.callStack.forEach(frame => frame.isActive = false);
                
                // 添加新栈帧
                this.callStack.push(newFrame);
                
                // 更新步骤描述
                this.updateStepDescription(`步骤 ${this.currentMoveIndex + 1}/${this.moves.length}: <span class="highlight">${step}</span> (递归深度: ${this.recursionDepth})`);
                
                // 更新调用栈显示
                this.updateStackDisplay();
            }
            
            // 执行移动动画
            animateMove(move) {
                return new Promise(resolve => {
                    const {from, to, disk} = move;
                    const animationDuration = this.animationSpeed;
                    const startTime = Date.now();
                    
                    // 从源柱子移除盘子
                    const diskIndex = this.towers[from].indexOf(disk);
                    this.towers[from].splice(diskIndex, 1);
                    
                    // 获取动画参数
                    const width = this.canvas.width;
                    const fromX = 50 + (width - 100) / 6 + from * (width - 100) / 3;
                    const toX = 50 + (width - 100) / 6 + to * (width - 100) / 3;
                    const baseY = this.canvas.height - 50;
                    const liftHeight = 100; // 抬起高度
                    
                    // 动画函数
                    const animate = () => {
                        const elapsed = Date.now() - startTime;
                        const progress = Math.min(elapsed / animationDuration, 1);
                        
                        // 计算当前位置
                        let x, y;
                        
                        if (progress < 0.3) {
                            // 第一阶段：向上抬起
                            const phaseProgress = progress / 0.3;
                            x = fromX;
                            y = baseY - (this.towers[to].length + 1) * 30 - liftHeight * phaseProgress;
                        } else if (progress < 0.7) {
                            // 第二阶段：水平移动
                            const phaseProgress = (progress - 0.3) / 0.4;
                            x = fromX + (toX - fromX) * phaseProgress;
                            y = baseY - (this.towers[to].length + 1) * 30 - liftHeight;
                        } else {
                            // 第三阶段：向下放置
                            const phaseProgress = (progress - 0.7) / 0.3;
                            x = toX;
                            y = baseY - (this.towers[to].length + 1) * 30 - liftHeight * (1 - phaseProgress);
                        }
                        
                        // 绘制
                        this.draw();
                        
                        // 绘制移动中的盘子
                        const diskWidth = 40 + disk * 25;
                        const diskColor = this.diskColors[(disk - 1) % this.diskColors.length];
                        
                        this.ctx.fillStyle = diskColor;
                        this.ctx.fillRect(x - diskWidth/2, y, diskWidth, 25);
                        
                        // 盘子边框
                        this.ctx.strokeStyle = '#2c3e50';
                        this.ctx.lineWidth = 2;
                        this.ctx.strokeRect(x - diskWidth/2, y, diskWidth, 25);
                        
                        // 盘子编号
                        this.ctx.fillStyle = '#2c3e50';
                        this.ctx.font = 'bold 14px Arial';
                        this.ctx.textAlign = 'center';
                        this.ctx.fillText(disk, x, y + 17);
                        
                        // 继续动画或完成
                        if (progress < 1) {
                            requestAnimationFrame(animate);
                        } else {
                            // 动画完成，将盘子添加到目标柱子
                            this.towers[to].push(disk);
                            this.draw();
                            resolve();
                        }
                    };
                    
                    // 开始动画
                    animate();
                });
            }
            
            // 设置事件监听器
            setupEventListeners() {
                // 开始/暂停按钮
                this.btnStart.addEventListener('click', () => {
                    if (this.currentMoveIndex >= this.moves.length) {
                        // 重新开始
                        this.init();
                        this.btnStart.textContent = "开始";
                        return;
                    }
                    
                    if (!this.isAnimating) {
                        this.isAnimating = true;
                        this.isPaused = false;
                        this.btnStart.textContent = "继续";
                        this.nextStep();
                    } else if (this.isPaused) {
                        this.isPaused = false;
                        this.btnStart.textContent = "继续";
                        this.nextStep();
                    }
                });
                
                // 暂停按钮
                this.btnPause.addEventListener('click', () => {
                    if (this.isAnimating && !this.isPaused) {
                        this.isPaused = true;
                        this.btnStart.textContent = "继续";
                    }
                });
                
                // 下一步按钮
                this.btnStep.addEventListener('click', () => {
                    if (this.isAnimating) {
                        this.isPaused = true;
                        this.btnStart.textContent = "继续";
                    }
                    this.nextStep();
                });
                
                // 重置按钮
                this.btnReset.addEventListener('click', () => {
                    this.init();
                    this.isAnimating = false;
                    this.isPaused = false;
                    this.btnStart.textContent = "开始";
                });
                
                // 盘子数量选择
                this.diskCountSelect.addEventListener('change', () => {
                    this.init();
                    this.isAnimating = false;
                    this.isPaused = false;
                    this.btnStart.textContent = "开始";
                });
                
                // 动画速度选择
                this.speedSelect.addEventListener('change', () => {
                    const speed = this.speedSelect.value;
                    switch(speed) {
                        case 'slow': this.animationSpeed = 1200; break;
                        case 'normal': this.animationSpeed = 800; break;
                        case 'fast': this.animationSpeed = 400; break;
                    }
                });
            }
        }
        
        // 页面加载完成后初始化
        document.addEventListener('DOMContentLoaded', () => {
            const visualizer = new HanoiVisualizer();
        });
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 《汉诺塔递归可视化教学动画》使用指南

欢迎使用本交互式教学动画！本工具旨在通过**可视化、可交互、可控制**的方式，帮助您深入理解汉诺塔问题的递归解决方案。无论您是初次接触递归概念，还是希望巩固对分治思想的理解，本动画都将为您提供一个直观、高效的学习平台。

---

### 一、 功能说明

本动画将经典的汉诺塔问题分解为两个同步联动的视图：
1.  **动画视图**：直观展示三个柱子上盘子的物理移动过程。
2.  **递归过程视图**：实时展示与每一步移动相对应的**递归函数代码执行状态**和**递归调用栈**的变化。

通过将抽象的递归调用、返回过程与具体的盘子移动一一对应，本工具旨在揭示递归算法“分而治之”的本质，让您“看见”递归的思维过程。

### 二、 主要功能

1.  **动画控制**：
    *   **开始/继续**：启动或继续连续播放整个移动过程。
    *   **暂停**：暂停当前动画，便于仔细观察。
    *   **下一步**：手动执行下一个逻辑步骤（一次完整的盘子移动及对应的递归状态更新）。
    *   **重置**：清空所有状态，恢复到初始设置。

2.  **参数配置**：
    *   **盘子数量**：可选择3至6个盘子进行演示。盘子越多，递归深度和总步数随之增加，有助于观察更复杂的递归树。
    *   **动画速度**：提供慢速、正常、快速三档，适应不同的观察节奏。

3.  **状态监控**：
    *   **总步数**：显示解决当前盘子数量所需的总移动步数（公式：2^n - 1）。
    *   **当前步数**：显示已执行的移动步数。
    *   **递归深度**：显示当前递归调用的深度（即调用栈的高度）。
    *   **调用次数**：记录递归函数被调用的总次数。

4.  **过程描述**：
    *   在动画视图下方，实时用文字描述当前正在执行的操作（例如：“移动盘子3从A到C”），并提示当前的递归深度。

### 三、 设计特色

1.  **双视图联动教学**：这是本工具的核心特色。当盘子移动时，右侧的递归视图会同步高亮对应的代码行，并更新调用栈。这种设计强制建立了“具体操作”与“抽象逻辑”之间的映射，是理解递归的关键。
2.  **调用栈可视化**：将内存中不可见的“调用栈”用堆叠的卡片直观呈现。您可以清晰地看到：
    *   每次新的递归调用如何“压入”一个新的栈帧。
    *   每个栈帧保存的参数（n, src, dst, aux）如何定义了当前要解决的子问题。
    *   函数返回时，对应的栈帧如何“弹出”。
3.  **分步探索与回溯**：通过“下一步”和“暂停”功能，您可以完全控制学习节奏。遇到不理解的地方，可以暂停、反复观察当前状态，甚至使用“重置”后以更慢的速度重新开始。
4.  **精心设计的视觉编码**：
    *   **盘子**：采用彩虹色系，大小分明，易于追踪单个盘子的移动轨迹。
    *   **代码高亮**：当前正在执行的代码行会以醒目的背景色突出显示。
    *   **活动栈帧**：调用栈中正在处理的栈帧有特殊边框和阴影，一目了然。

### 四、 教学要点（建议学习路径）

为了达到最佳学习效果，建议您按以下步骤使用本工具：

1.  **观察整体（快速播放）**：首先选择3个盘子，以正常或快速速度点击“开始”，完整观看一遍动画。目的是对汉诺塔的移动规律和递归解决方案的“整体形状”有一个感性认识。
2.  **关联理解（单步执行）**：重置后，选择4个盘子，使用“下一步”功能手动操作。**核心任务是：在每一步，都要在脑中或口头上解释清楚**：
    *   **动画视图**：哪个盘子从哪移到哪？
    *   **递归视图**：这对应代码的哪一行？（是高亮的那一行吗？）
    *   **调用栈**：栈顶的栈帧（活动的）代表什么子问题？它的参数`(n, src, dst, aux)`是什么意思？
3.  **深入分析（聚焦递归分解）**：当移动一个较大的盘子（比如4个盘子中的第3号盘）时，暂停并思考：
    *   在移动它之前，发生了什么？（递归步骤1：将上面所有小盘子移到辅助柱）
    *   在移动它之后，将要发生什么？（递归步骤3：将辅助柱上的小盘子移回目标柱）
    *   观察调用栈在此过程中的变化，理解“递归调用”和“返回”如何对应着子问题的“分解”与“解决”。
4.  **挑战与验证（改变参数）**：尝试5个或6个盘子。预测下一步的移动，然后用“下一步”功能验证您的预测。这能极大地锻炼您的递归思维。

### 五、 使用建议

*   **给初学者**：不要急于求成。从3个盘子开始，确保完全理解了每一步与递归代码的对应关系后，再增加盘子数量。反复使用“重置”和“下一步”是学习的关键。
*   **给教师**：本工具非常适合课堂演示或作为学生课后探索的辅助材料。您可以引导学生关注“递归三要素”在本动画中的体现：**定义子问题（栈帧参数）、基本结束条件（移动1个盘子）、递归调用（分解问题）**。
*   **给编程爱好者**：尝试在观看动画的同时，在纸上或脑海中模拟程序的执行。本动画可视化了递归的“纵向”深度，有助于您理解递归函数的空间复杂度（调用栈深度）。

我们希望这个精心设计的交互式动画，能像一位耐心的向导，带领您穿越递归思维的迷雾，最终领略到算法设计中“分而治之”这一强大思想的清晰与优美。

**祝您学习愉快，探索成功！**