# 需求：最长公共子序列LCS（动态规划表格斜线找路径）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：学习算法与数据结构、动态规划的中高年级本科生或自学者。他们已了解动态规划的基本思想，但对LCS的填表过程和路径回溯（特别是“斜线”代表的“相等”情况）理解不深。
2.  **核心痛点**：
    *   难以将抽象的“状态转移方程”与动态变化的表格建立直观联系。
    *   不理解表格中每个单元格数值的来源（来自上方、左方还是左上方）。
    *   对如何从完成的表格中“找路径”以构造出最长公共子序列感到困惑，尤其是当存在多条等长路径时。
    *   传统静态图表或分步幻灯片无法提供自主探索和即时反馈。
3.  **学习目标**：
    *   **理解**：深入理解LCS动态规划表中每个单元格 `dp[i][j]` 的计算逻辑（三种情况：`str1[i-1] == str2[j-1]` 和 `!=`）。
    *   **掌握**：掌握从完成表格的右下角回溯到左上角，寻找一条（或多条）最长公共子序列路径的方法。
    *   **应用**：能够独立对给定的两个字符串，手动或通过动画验证其LCS的求解过程。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念**：
    1.  **状态定义**：`dp[i][j]` 表示 `str1[0..i-1]` 和 `str2[0..j-1]` 的LCS长度。
    2.  **状态转移**：
        *   若 `str1[i-1] == str2[j-1]`，则 `dp[i][j] = dp[i-1][j-1] + 1` （**斜线方向**）。
        *   否则，`dp[i][j] = max(dp[i-1][j], dp[i][j-1])` （**上方或左方**）。
    3.  **路径回溯**：从 `dp[m][n]` 出发，根据数值来源反向追踪。优先寻找来自“斜线”的路径（代表匹配字符），以构造出子序列。

*   **认知规律**：
    1.  **从具体到抽象**：使用一组预设的经典示例字符串（如“ABCBDAB”和“BDCABA”），让学习者先观察整体过程，再允许自定义输入。
    2.  **分步分解**：将完整的求解过程分解为“初始化表格”、“逐行/逐列填充”、“路径回溯”三个阶段，允许用户分步控制。
    3.  **突出焦点与对比**：在每一步操作中，通过高亮、动画和颜色，将用户的注意力集中在当前正在计算的单元格、参与比较的字符以及候选的来源单元格上。
    4.  **即时反馈与探索**：允许用户点击任意单元格，查看其值是如何由其他单元格计算得出的。在路径回溯阶段，允许用户尝试选择不同的来源路径，观察如何得到不同的LCS（如果存在）。

*   **交互设计**：
    1.  **阶段控制**：提供清晰的“上一步”、“下一步”、“播放/暂停”按钮，控制动画流程。
    2.  **模式切换**：在“自动演示”和“手动探索”模式间切换。自动演示用于教学引导，手动探索允许用户自由点击和观察。
    3.  **数据输入**：提供预设案例下拉菜单和一个允许用户输入自定义两个字符串的区域。
    4.  **单元格交互**：
        *   **填充阶段**：点击一个已填充的单元格，用箭头和说明文字显示其值的来源（上方、左方、左上方）。
        *   **回溯阶段**：在完成的表格上，用户可以从终点开始，通过点击可能的来源单元格（高亮显示）来“选择”路径，系统实时显示当前构造出的子序列。

*   **视觉呈现**：
    1.  **三区域布局**：
        *   **控制与输入区**（顶部）：包含按钮、字符串输入框、说明文字。
        *   **核心动画区**（中央左侧）：动态规划表格，字符序列分别作为表头和侧栏。
        *   **信息输出与解释区**（中央右侧/底部）：动态显示当前步骤的详细文字解释、状态转移方程、以及最终找出的LCS。
    2.  **表格视觉编码**：
        *   **单元格**：显示 `dp[i][j]` 的值。
        *   **边界**：用不同粗细或颜色的线区分 `i=0` 或 `j=0` 的初始化行/列。
        *   **字符匹配**：当比较 `str1[i-1]` 和 `str2[j-1]` 时，高亮对应的表头单元格。
        *   **数值来源**：用**彩色箭头**明确指示：
            *   **红色箭头（左上）**：表示来自 `dp[i-1][j-1]`（字符相等）。
            *   **蓝色箭头（上）**：表示来自 `dp[i-1][j]`。
            *   **绿色箭头（左）**：表示来自 `dp[i][j-1]`。
        *   **路径高亮**：在回溯时，将构成LCS的路径上的单元格用醒目的背景色（如浅金色）填充，连接的箭头加粗。

#### 配色方案选择
*   **主色调**：采用深蓝色（`#2c3e50`）作为背景或标题色，体现专业、清晰。
*   **表格背景**：白色或浅灰色（`#f8f9fa`），确保数字清晰可读。
*   **高亮色**：
    *   **当前焦点单元格**：浅蓝色背景（`#e3f2fd`）。
    *   **字符匹配高亮**：浅绿色背景（`#d4edda`）。
    *   **路径单元格**：浅金色背景（`#fff3cd`）。
*   **箭头与指示色**：
    *   红色（`#dc3545`）：用于“斜线/相等”转移。
    *   蓝色（`#007bff`）：用于“来自上方”转移。
    *   绿色（`#28a745`）：用于“来自左方”转移。
*   **按钮与交互元素**：使用与箭头色系呼应的蓝色，悬停时加深。

#### 交互功能列表
1.  **流程控制**：
    *   重置 / 初始化
    *   上一步
    *   下一步 / 单步执行
    *   播放 / 暂停自动演示
    *   直接跳转到“填充完成”或“开始回溯”阶段
2.  **数据输入与选择**：
    *   预设示例下拉选择框（如：“ABCBDAB” & “BDCABA”）
    *   自定义字符串1和字符串2的输入框
    *   “应用”或“生成表格”按钮
3.  **可视化与探索**：
    *   **自动填充模式**：以可控速度自动演示表格填充过程。
    *   **单元格详情查看**：在任意阶段，点击表格中的单元格，显示其值计算过程的详细解释和箭头指示。
    *   **交互式路径回溯**：
        *   进入回溯模式后，当前合法来源单元格高亮。
        *   用户点击选择一个来源，路径延伸一步，右侧信息区更新当前已构建的子序列。
        *   提供“自动回溯”按钮，让系统快速展示一条标准路径。
        *   当存在多条路径时，允许用户“重置回溯”并尝试选择另一条路径。
4.  **信息显示**：
    *   当前阶段提示（如：“正在计算 dp[3][4]...”）
    *   当前字符比较结果显示（如：“A” != “B”，取 max(上，左)”）
    *   状态转移方程动态显示（根据当前情况高亮对应部分）
    *   最长公共子序列长度显示
    *   找到的一条或多条最长公共子序列结果显示

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>最长公共子序列(LCS)动态规划教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .header {
            background-color: #2c3e50;
            color: white;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        h1 {
            font-size: 28px;
            margin-bottom: 10px;
        }
        
        .subtitle {
            font-size: 16px;
            opacity: 0.9;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .control-panel {
            flex: 1;
            min-width: 300px;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }
        
        .visualization-area {
            flex: 2;
            min-width: 600px;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            display: flex;
            flex-direction: column;
        }
        
        .info-panel {
            flex: 1;
            min-width: 300px;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }
        
        .section-title {
            font-size: 18px;
            font-weight: 600;
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #eaeaea;
        }
        
        .input-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        input[type="text"] {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        
        select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            background-color: white;
        }
        
        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        button {
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.2s ease;
        }
        
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        .btn-primary {
            background-color: #3498db;
            color: white;
        }
        
        .btn-secondary {
            background-color: #95a5a6;
            color: white;
        }
        
        .btn-success {
            background-color: #2ecc71;
            color: white;
        }
        
        .btn-warning {
            background-color: #f39c12;
            color: white;
        }
        
        .btn-danger {
            background-color: #e74c3c;
            color: white;
        }
        
        .btn-info {
            background-color: #17a2b8;
            color: white;
        }
        
        .btn-small {
            padding: 6px 10px;
            font-size: 14px;
        }
        
        .mode-selector {
            display: flex;
            margin-bottom: 20px;
            border-radius: 5px;
            overflow: hidden;
            border: 1px solid #ddd;
        }
        
        .mode-btn {
            flex: 1;
            padding: 10px;
            text-align: center;
            background-color: #f8f9fa;
            border: none;
            border-radius: 0;
        }
        
        .mode-btn.active {
            background-color: #3498db;
            color: white;
        }
        
        #canvas-container {
            flex: 1;
            border: 1px solid #eee;
            border-radius: 5px;
            overflow: auto;
            position: relative;
            min-height: 500px;
            background-color: #f8f9fa;
        }
        
        #lcs-canvas {
            display: block;
            margin: 0 auto;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #eee;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 3px;
        }
        
        .current-step {
            background-color: #e3f2fd;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 15px;
            border-left: 4px solid #3498db;
        }
        
        .step-title {
            font-weight: 600;
            margin-bottom: 8px;
            color: #2c3e50;
        }
        
        .equation {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 15px;
            font-family: 'Courier New', monospace;
            font-size: 16px;
            border-left: 4px solid #2ecc71;
        }
        
        .lcs-result {
            background-color: #fff3cd;
            padding: 15px;
            border-radius: 5px;
            margin-top: 15px;
            border-left: 4px solid #f39c12;
        }
        
        .result-title {
            font-weight: 600;
            margin-bottom: 8px;
            color: #856404;
        }
        
        .lcs-string {
            font-family: 'Courier New', monospace;
            font-size: 20px;
            font-weight: bold;
            color: #d35400;
            letter-spacing: 2px;
        }
        
        .status-bar {
            background-color: #2c3e50;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            margin-top: 20px;
            font-size: 14px;
        }
        
        .arrow-example {
            display: inline-block;
            margin: 0 5px;
            font-weight: bold;
        }
        
        .red-arrow {
            color: #dc3545;
        }
        
        .blue-arrow {
            color: #007bff;
        }
        
        .green-arrow {
            color: #28a745;
        }
        
        @media (max-width: 1200px) {
            .container {
                flex-direction: column;
            }
            
            .control-panel, .visualization-area, .info-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>最长公共子序列(LCS)动态规划教学动画</h1>
        <p class="subtitle">通过交互式动画理解动态规划表格的填充与路径回溯过程</p>
    </div>
    
    <div class="container">
        <div class="control-panel">
            <div class="section-title">输入与控制</div>
            
            <div class="input-group">
                <label for="example-select">选择预设示例：</label>
                <select id="example-select">
                    <option value="custom">自定义输入</option>
                    <option value="example1" selected>示例1: ABCBDAB & BDCABA</option>
                    <option value="example2">示例2: AGGTAB & GXTXAYB</option>
                    <option value="example3">示例3: ABCD & ACBD</option>
                    <option value="example4">示例4: 算法 & 动态规划</option>
                </select>
            </div>
            
            <div class="input-group">
                <label for="str1-input">字符串1：</label>
                <input type="text" id="str1-input" value="ABCBDAB" maxlength="15">
            </div>
            
            <div class="input-group">
                <label for="str2-input">字符串2：</label>
                <input type="text" id="str2-input" value="BDCABA" maxlength="15">
            </div>
            
            <div class="button-group">
                <button id="generate-btn" class="btn-primary">生成表格</button>
                <button id="reset-btn" class="btn-secondary">重置</button>
            </div>
            
            <div class="section-title">操作模式</div>
            <div class="mode-selector">
                <button id="mode-auto" class="mode-btn active">自动演示</button>
                <button id="mode-manual" class="mode-btn">手动探索</button>
            </div>
            
            <div class="section-title">流程控制</div>
            <div class="button-group">
                <button id="prev-btn" class="btn-secondary" disabled>上一步</button>
                <button id="next-btn" class="btn-primary">下一步</button>
                <button id="play-btn" class="btn-success">播放</button>
                <button id="fill-all-btn" class="btn-warning">填充全部</button>
                <button id="backtrack-btn" class="btn-info" disabled>开始回溯</button>
            </div>
            
            <div class="section-title">速度控制</div>
            <div class="input-group">
                <label for="speed-slider">动画速度：<span id="speed-value">中速</span></label>
                <input type="range" id="speed-slider" min="1" max="5" value="3">
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #e3f2fd;"></div>
                    <span>当前单元格</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #d4edda;"></div>
                    <span>字符匹配</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #fff3cd;"></div>
                    <span>LCS路径</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #f8d7da;"></div>
                    <span>回溯选项</span>
                </div>
            </div>
        </div>
        
        <div class="visualization-area">
            <div class="section-title">动态规划表格</div>
            <div id="canvas-container">
                <canvas id="lcs-canvas" width="800" height="500"></canvas>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <span class="arrow-example red-arrow">↖</span>
                    <span>字符相等（来自左上）</span>
                </div>
                <div class="legend-item">
                    <span class="arrow-example blue-arrow">↑</span>
                    <span>来自上方</span>
                </div>
                <div class="legend-item">
                    <span class="arrow-example green-arrow">←</span>
                    <span>来自左方</span>
                </div>
            </div>
        </div>
        
        <div class="info-panel">
            <div class="section-title">当前步骤</div>
            <div id="step-info" class="current-step">
                <div class="step-title">初始化</div>
                <p>已创建动态规划表格，第一行和第一列已初始化为0。</p>
            </div>
            
            <div class="section-title">状态转移方程</div>
            <div id="equation-info" class="equation">
                dp[i][j] = 
                <span id="eq-case1" style="color: #dc3545; font-weight: bold;">dp[i-1][j-1] + 1</span> 
                <span>如果 str1[i-1] == str2[j-1]</span><br>
                <span>否则取 </span>
                <span id="eq-case2" style="color: #007bff; font-weight: bold;">max(dp[i-1][j], dp[i][j-1])</span>
            </div>
            
            <div class="section-title">最长公共子序列</div>
            <div id="result-info" class="lcs-result">
                <div class="result-title">LCS长度：<span id="lcs-length">0</span></div>
                <div class="result-title">LCS序列：</div>
                <div id="lcs-sequence" class="lcs-string">-</div>
                <div id="multiple-paths" style="margin-top: 10px; font-size: 14px; display: none;">
                    <span>存在多条LCS路径，尝试不同的回溯选择！</span>
                </div>
            </div>
        </div>
    </div>
    
    <div class="status-bar">
        <span id="status-text">就绪。请点击"生成表格"开始。</span>
    </div>

    <script>
        // 全局变量
        let str1 = "ABCBDAB";
        let str2 = "BDCABA";
        let dp = [];
        let m, n;
        let canvas, ctx;
        let cellSize = 50;
        let startX = 100, startY = 80;
        let currentStep = 0;
        let totalSteps = 0;
        let isPlaying = false;
        let playInterval;
        let speed = 500; // 毫秒
        let isAutoMode = true;
        let isBacktracking = false;
        let backtrackPath = [];
        let backtrackChoices = [];
        let lcsSequence = "";
        let animationQueue = [];
        let currentI = 0, currentJ = 0;
        let isTableGenerated = false;
        
        // 预设示例
        const examples = {
            example1: { str1: "ABCBDAB", str2: "BDCABA" },
            example2: { str1: "AGGTAB", str2: "GXTXAYB" },
            example3: { str1: "ABCD", str2: "ACBD" },
            example4: { str1: "算法", str2: "动态规划" }
        };
        
        // DOM元素
        const str1Input = document.getElementById('str1-input');
        const str2Input = document.getElementById('str2-input');
        const exampleSelect = document.getElementById('example-select');
        const generateBtn = document.getElementById('generate-btn');
        const resetBtn = document.getElementById('reset-btn');
        const prevBtn = document.getElementById('prev-btn');
        const nextBtn = document.getElementById('next-btn');
        const playBtn = document.getElementById('play-btn');
        const fillAllBtn = document.getElementById('fill-all-btn');
        const backtrackBtn = document.getElementById('backtrack-btn');
        const modeAutoBtn = document.getElementById('mode-auto');
        const modeManualBtn = document.getElementById('mode-manual');
        const speedSlider = document.getElementById('speed-slider');
        const speedValue = document.getElementById('speed-value');
        const stepInfo = document.getElementById('step-info');
        const equationInfo = document.getElementById('equation-info');
        const resultInfo = document.getElementById('result-info');
        const lcsLength = document.getElementById('lcs-length');
        const lcsSequenceEl = document.getElementById('lcs-sequence');
        const multiplePaths = document.getElementById('multiple-paths');
        const statusText = document.getElementById('status-text');
        
        // 初始化
        function init() {
            canvas = document.getElementById('lcs-canvas');
            ctx = canvas.getContext('2d');
            
            // 设置事件监听器
            generateBtn.addEventListener('click', generateTable);
            resetBtn.addEventListener('click', resetAll);
            prevBtn.addEventListener('click', prevStep);
            nextBtn.addEventListener('click', nextStep);
            playBtn.addEventListener('click', togglePlay);
            fillAllBtn.addEventListener('click', fillAll);
            backtrackBtn.addEventListener('click', startBacktracking);
            
            modeAutoBtn.addEventListener('click', () => setMode(true));
            modeManualBtn.addEventListener('click', () => setMode(false));
            
            exampleSelect.addEventListener('change', handleExampleChange);
            speedSlider.addEventListener('input', updateSpeed);
            
            canvas.addEventListener('click', handleCanvasClick);
            
            // 初始绘制
            drawEmptyTable();
            updateUI();
        }
        
        // 生成表格
        function generateTable() {
            str1 = str1Input.value.trim();
            str2 = str2Input.value.trim();
            
            if (str1 === "" || str2 === "") {
                alert("请输入两个字符串");
                return;
            }
            
            m = str1.length;
            n = str2.length;
            
            // 初始化dp数组
            dp = Array(m + 1).fill().map(() => Array(n + 1).fill(0));
            
            // 计算总步骤数
            totalSteps = m * n;
            currentStep = 0;
            currentI = 1;
            currentJ = 1;
            isBacktracking = false;
            backtrackPath = [];
            backtrackChoices = [];
            lcsSequence = "";
            animationQueue = [];
            isTableGenerated = true;
            
            // 重置按钮状态
            prevBtn.disabled = true;
            nextBtn.disabled = false;
            backtrackBtn.disabled = true;
            
            // 绘制初始表格
            drawTable();
            
            // 更新UI
            updateStepInfo("初始化", "已创建动态规划表格，第一行和第一列已初始化为0。");
            updateEquation("初始化");
            updateResult();
            updateStatus(`已生成表格：字符串1="${str1}" (长度=${m}), 字符串2="${str2}" (长度=${n})`);
            
            // 如果手动模式，允许点击单元格
            if (!isAutoMode) {
                updateStatus("手动模式：点击表格单元格查看计算过程");
            }
        }
        
        // 重置所有
        function resetAll() {
            str1 = "ABCBDAB";
            str2 = "BDCABA";
            str1Input.value = str1;
            str2Input.value = str2;
            exampleSelect.value = "example1";
            
            dp = [];
            currentStep = 0;
            totalSteps = 0;
            isPlaying = false;
            isBacktracking = false;
            backtrackPath = [];
            backtrackChoices = [];
            lcsSequence = "";
            animationQueue = [];
            isTableGenerated = false;
            
            if (playInterval) {
                clearInterval(playInterval);
                playInterval = null;
            }
            
            playBtn.textContent = "播放";
            prevBtn.disabled = true;
            nextBtn.disabled = false;
            backtrackBtn.disabled = true;
            
            drawEmptyTable();
            updateStepInfo("初始化", "已重置。请点击\"生成表格\"开始。");
            updateEquation("初始化");
            updateResult();
            updateStatus("已重置。请点击\"生成表格\"开始。");
        }
        
        // 上一步
        function prevStep() {
            if (isBacktracking) {
                // 回溯模式的上一步
                if (backtrackPath.length > 0) {
                    backtrackPath.pop();
                    lcsSequence = lcsSequence.slice(0, -1);
                    drawTable();
                    updateResult();
                    updateStatus(`回溯上一步，当前LCS: ${lcsSequence || "空"}`);
                }
            } else {
                // 填充模式的上一步
                if (currentStep > 0) {
                    currentStep--;
                    
                    // 计算当前单元格位置
                    currentI = Math.floor((currentStep) / n) + 1;
                    currentJ = (currentStep % n) + 1;
                    
                    // 如果回到第一步之前，重置为初始状态
                    if (currentStep === 0) {
                        dp = Array(m + 1).fill().map(() => Array(n + 1).fill(0));
                        currentI = 1;
                        currentJ = 1;
                    } else {
                        // 清除当前单元格的值
                        dp[currentI][currentJ] = 0;
                    }
                    
                    drawTable();
                    updateStepInfoForCell(currentI, currentJ, false);
                    updateStatus(`上一步：准备计算 dp[${currentI}][${currentJ}]`);
                    
                    // 更新按钮状态
                    nextBtn.disabled = false;
                    if (currentStep === 0) {
                        prevBtn.disabled = true;
                    }
                }
            }
        }
        
        // 下一步
        function nextStep() {
            if (!isTableGenerated) {
                alert("请先生成表格");
                return;
            }
            
            if (isBacktracking) {
                // 回溯模式的下一步
                performBacktrackStep();
            } else {
                // 填充模式的下一步
                if (currentStep < totalSteps) {
                    performFillStep();
                    
                    // 如果填充完成，启用回溯按钮
                    if (currentStep === totalSteps) {
                        backtrackBtn.disabled = false;
                        updateStatus("表格填充完成！点击\"开始回溯\"查找LCS路径。");
                    }
                }
            }
        }
        
        // 执行填充步骤
        function performFillStep() {
            currentStep++;
            currentI = Math.floor((currentStep - 1) / n) + 1;
            currentJ = ((currentStep - 1) % n) + 1;
            
            // 计算dp[i][j]
            const char1 = str1[currentI - 1];
            const char2 = str2[currentJ - 1];
            
            if (char1 === char2) {
                // 字符相等，来自左上角+1
                dp[currentI][currentJ] = dp[currentI - 1][currentJ - 1] + 1;
            } else {
                // 字符不等，取上方和左方的最大值
                dp[currentI][currentJ] = Math.max(dp[currentI - 1][currentJ], dp[currentI][currentJ - 1]);
            }
            
            drawTable();
            updateStepInfoForCell(currentI, currentJ, true);
            
            // 更新按钮状态
            prevBtn.disabled = false;
            if (currentStep === totalSteps) {
                nextBtn.disabled = true;
            }
        }
        
        // 开始回溯
        function startBacktracking() {
            if (!isTableGenerated || currentStep < totalSteps) {
                alert("请先完成表格填充");
                return;
            }
            
            isBacktracking = true;
            backtrackPath = [];
            backtrackChoices = [];
            lcsSequence = "";
            
            // 从右下角开始
            let i = m, j = n;
            backtrackPath.push({i, j});
            
            drawTable();
            updateStepInfo("开始回溯", `从右下角 dp[${i}][${j}] = ${dp[i][j]} 开始回溯查找LCS路径。`);
            updateStatus("开始回溯：从右下角开始，查找LCS路径");
            
            // 更新按钮文本
            backtrackBtn.textContent = "重置回溯";
            backtrackBtn.classList.remove("btn-info");
            backtrackBtn.classList.add("btn-warning");
            
            // 如果是自动模式，自动执行回溯
            if (isAutoMode) {
                autoBacktrack();
            }
        }
        
        // 执行回溯步骤
        function performBacktrackStep() {
            if (backtrackPath.length === 0) return;
            
            const current = backtrackPath[backtrackPath.length - 1];
            const i = current.i, j = current.j;
            
            // 如果到达左上角，回溯完成
            if (i === 0 || j === 0) {
                updateStepInfo("回溯完成", `已找到最长公共子序列: "${lcsSequence}"，长度 = ${lcsSequence.length}`);
                updateStatus(`回溯完成！LCS: "${lcsSequence}"，长度 = ${lcsSequence.length}`);
                return;
            }
            
            // 查找可能的回溯路径
            const choices = [];
            const char1 = str1[i - 1];
            const char2 = str2[j - 1];
            
            if (char1 === char2 && dp[i][j] === dp[i - 1][j - 1] + 1) {
                choices.push({i: i - 1, j: j - 1, direction: "diagonal", char: char1});
            }
            
            if (dp[i][j] === dp[i - 1][j]) {
                choices.push({i: i - 1, j: j, direction: "up"});
            }
            
            if (dp[i][j] === dp[i][j - 1]) {
                choices.push({i: i, j: j - 1, direction: "left"});
            }
            
            // 如果有多个选择，记录并让用户选择（手动模式）
            if (choices.length > 1 && !isAutoMode) {
                backtrackChoices = choices;
                updateStepInfo("多个回溯选项", `dp[${i}][${j}] 有 ${choices.length} 个可能的来源。点击一个高亮单元格选择路径。`);
                updateStatus(`多个回溯选项：请点击选择一个来源单元格`);
                drawTable();
                return;
            }
            
            // 自动模式或只有一个选择
            let nextCell;
            if (choices.length === 1) {
                nextCell = choices[0];
            } else if (choices.length > 1) {
                // 优先选择斜线方向（字符匹配）
                const diagonalChoice = choices.find(c => c.direction === "diagonal");
                nextCell = diagonalChoice || choices[0];
            } else {
                // 没有选择，回溯完成
                updateStepInfo("回溯完成", `已找到最长公共子序列: "${lcsSequence}"，长度 = ${lcsSequence.length}`);
                updateStatus(`回溯完成！LCS: "${lcsSequence}"，长度 = ${lcsSequence.length}`);
                return;
            }
            
            // 添加到路径
            backtrackPath.push(nextCell);
            
            // 如果是从斜线方向来的，添加到LCS序列
            if (nextCell.direction === "diagonal") {
                lcsSequence = nextCell.char + lcsSequence;
            }
            
            drawTable();
            updateStepInfoForBacktrack(i, j, nextCell);
            updateResult();
            
            // 检查是否有多条路径
            if (choices.length > 1) {
                multiplePaths.style.display = "block";
            }
        }
        
        // 自动回溯
        function autoBacktrack() {
            if (!isBacktracking) return;
            
            const interval = setInterval(() => {
                const current = backtrackPath[backtrackPath.length - 1];
                if (current.i === 0 || current.j === 0) {
                    clearInterval(interval);
                    updateStepInfo("回溯完成", `已找到最长公共子序列: "${lcsSequence}"，长度 = ${lcsSequence.length}`);
                    updateStatus(`回溯完成！LCS: "${lcsSequence}"，长度 = ${lcsSequence.length}`);
                    return;
                }
                
                performBacktrackStep();
            }, speed);
        }
        
        // 填充所有
        function fillAll() {
            if (!isTableGenerated) {
                alert("请先生成表格");
                return;
            }
            
            // 填充整个表格
            for (let i = 1; i <= m; i++) {
                for (let j = 1; j <= n; j++) {
                    const char1 = str1[i - 1];
                    const char2 = str2[j - 1];
                    
                    if (char1 === char2) {
                        dp[i][j] = dp[i - 1][j - 1] + 1;
                    } else {
                        dp[i][j] = Math.max(dp[i - 1][j], dp[i][j - 1]);
                    }
                }
            }
            
            currentStep = totalSteps;
            currentI = m;
            currentJ = n;
            
            drawTable();
            updateStepInfo("填充完成", `表格已全部填充。LCS长度 = ${dp[m][n]}。`);
            updateStatus("表格填充完成！点击\"开始回溯\"查找LCS路径。");
            
            // 更新按钮状态
            prevBtn.disabled = false;
            nextBtn.disabled = true;
            backtrackBtn.disabled = false;
        }
        
        // 切换播放/暂停
        function togglePlay() {
            if (!isTableGenerated) {
                alert("请先生成表格");
                return;
            }
            
            if (isPlaying) {
                // 暂停
                if (playInterval) {
                    clearInterval(playInterval);
                    playInterval = null;
                }
                isPlaying = false;
                playBtn.textContent = "播放";
                updateStatus("已暂停");
            } else {
                // 播放
                isPlaying = true;
                playBtn.textContent = "暂停";
                
                if (isBacktracking) {
                    // 回溯模式的播放
                    autoBacktrack();
                } else {
                    // 填充模式的播放
                    playInterval = setInterval(() => {
                        if (currentStep >= totalSteps) {
                            clearInterval(playInterval);
                            isPlaying = false;
                            playBtn.textContent = "播放";
                            updateStatus("表格填充完成！");
                            backtrackBtn.disabled = false;
                            return;
                        }
                        
                        nextStep();
                    }, speed);
                }
            }
        }
        
        // 设置模式
        function setMode(auto) {
            isAutoMode = auto;
            
            if (auto) {
                modeAutoBtn.classList.add("active");
                modeManualBtn.classList.remove("active");
                updateStatus("自动演示模式：点击播放按钮观看完整过程");
            } else {
                modeAutoBtn.classList.remove("active");
                modeManualBtn.classList.add("active");
                updateStatus("手动探索模式：点击表格单元格查看计算过程");
            }
            
            drawTable();
        }
        
        // 更新速度
        function updateSpeed() {
            const speedLevel = parseInt(speedSlider.value);
            const speedTexts = ["很慢", "慢速", "中速", "快速", "很快"];
            speedValue.textContent = speedTexts[speedLevel - 1];
            
            // 速度级别对应的时间（毫秒）
            const speeds = [1000, 700, 500, 300, 150];
            speed = speeds[speedLevel - 1];
            
            // 如果正在播放，更新间隔
            if (isPlaying && playInterval) {
                clearInterval(playInterval);
                playInterval = setInterval(() => {
                    if (isBacktracking) {
                        // 回溯模式
                        const current = backtrackPath[backtrackPath.length - 1];
                        if (current.i === 0 || current.j === 0) {
                            clearInterval(playInterval);
                            isPlaying = false;
                            playBtn.textContent = "播放";
                            return;
                        }
                        performBacktrackStep();
                    } else {
                        // 填充模式
                        if (currentStep >= totalSteps) {
                            clearInterval(playInterval);
                            isPlaying = false;
                            playBtn.textContent = "播放";
                            backtrackBtn.disabled = false;
                            return;
                        }
                        nextStep();
                    }
                }, speed);
            }
        }
        
        // 处理示例选择
        function handleExampleChange() {
            const example = exampleSelect.value;
            
            if (example === "custom") {
                str1Input.value = "";
                str2Input.value = "";
                str1Input.focus();
            } else {
                const ex = examples[example];
                str1Input.value = ex.str1;
                str2Input.value = ex.str2;
            }
        }
        
        // 处理画布点击
        function handleCanvasClick(event) {
            if (!isTableGenerated) return;
            
            const rect = canvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;
            
            // 计算点击的单元格
            const i = Math.floor((y - startY) / cellSize);
            const j = Math.floor((x - startX) / cellSize);
            
            // 检查是否在有效范围内
            if (i >= 0 && i <= m && j >= 0 && j <= n) {
                if (isBacktracking) {
                    // 回溯模式：选择回溯路径
                    handleBacktrackClick(i, j);
                } else if (!isAutoMode) {
                    // 手动模式：查看单元格计算过程
                    handleCellClick(i, j);
                }
            }
        }
        
        // 处理单元格点击（手动模式）
        function handleCellClick(i, j) {
            if (i === 0 || j === 0) {
                updateStepInfo("边界单元格", `dp[${i}][${j}] = 0 (边界初始化)`);
                updateStatus(`点击了边界单元格 dp[${i}][${j}]`);
                return;
            }
            
            if (dp[i][j] === 0 && (i > currentI || (i === currentI && j > currentJ))) {
                updateStepInfo("未计算单元格", `dp[${i}][${j}] 尚未计算`);
                updateStatus(`dp[${i}][${j}] 尚未计算`);
                return;
            }
            
            updateStepInfoForCell(i, j, true);
            updateStatus(`查看 dp[${i}][${j}] 的计算过程`);
            
            // 临时高亮显示
            drawTable();
            highlightCell(i, j, "#e3f2fd");
        }
        
        // 处理回溯点击
        function handleBacktrackClick(i, j) {
            if (backtrackChoices.length === 0) return;
            
            // 检查点击的单元格是否是可选路径之一
            const choice = backtrackChoices.find(c => c.i === i && c.j === j);
            if (!choice) return;
            
            // 添加到路径
            backtrackPath.push(choice);
            
            // 如果是从斜线方向来的，添加到LCS序列
            if (choice.direction === "diagonal") {
                lcsSequence = choice.char + lcsSequence;
            }
            
            // 清空选择
            backtrackChoices = [];
            
            drawTable();
            updateStepInfoForBacktrack(backtrackPath[backtrackPath.length-2].i, 
                                      backtrackPath[backtrackPath.length-2].j, 
                                      choice);
            updateResult();
            updateStatus(`选择了回溯路径到 dp[${i}][${j}]，当前LCS: ${lcsSequence || "空"}`);
        }
        
        // 绘制空表格
        function drawEmptyTable() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制标题
            ctx.font = "18px Arial";
            ctx.fillStyle = "#2c3e50";
            ctx.textAlign = "center";
            ctx.fillText("请点击\"生成表格\"开始", canvas.width/2, canvas.height/2);
            
            ctx.textAlign = "left";
        }
        
        // 绘制表格
        function drawTable() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            if (!isTableGenerated) {
                drawEmptyTable();
                return;
            }
            
            // 绘制字符串1（纵向）
            ctx.font = "bold 18px Arial";
            ctx.fillStyle = "#2c3e50";
            ctx.textAlign = "center";
            ctx.textBas
<!--检测到代码截断，自动续写中...-->
eline = "middle";
            
            for (let i = 0; i < m; i++) {
                const x = startX - cellSize;
                const y = startY + (i + 1) * cellSize;
                ctx.fillText(str1[i], x, y);
            }
            
            // 绘制字符串2（横向）
            for (let j = 0; j < n; j++) {
                const x = startX + (j + 1) * cellSize;
                const y = startY - cellSize;
                ctx.fillText(str2[j], x, y);
            }
            
            // 绘制表格单元格
            ctx.font = "bold 20px Arial";
            ctx.textAlign = "center";
            ctx.textBaseline = "middle";
            
            for (let i = 0; i <= m; i++) {
                for (let j = 0; j <= n; j++) {
                    const x = startX + j * cellSize;
                    const y = startY + i * cellSize;
                    
                    // 单元格背景色
                    let fillColor = "#ffffff";
                    
                    // 检查是否在回溯路径中
                    if (isBacktracking) {
                        const inPath = backtrackPath.some(cell => cell.i === i && cell.j === j);
                        if (inPath) {
                            fillColor = "#fff3cd"; // 路径单元格
                        }
                        
                        // 检查是否是当前回溯选项
                        const isChoice = backtrackChoices.some(cell => cell.i === i && cell.j === j);
                        if (isChoice) {
                            fillColor = "#f8d7da"; // 回溯选项
                        }
                    } 
                    // 检查是否是当前正在计算的单元格（填充模式）
                    else if (i === currentI && j === currentJ && currentStep > 0 && currentStep <= totalSteps) {
                        fillColor = "#e3f2fd"; // 当前单元格
                    }
                    
                    // 绘制单元格背景
                    ctx.fillStyle = fillColor;
                    ctx.fillRect(x - cellSize/2, y - cellSize/2, cellSize, cellSize);
                    
                    // 绘制单元格边框
                    ctx.strokeStyle = "#ddd";
                    ctx.lineWidth = 1;
                    ctx.strokeRect(x - cellSize/2, y - cellSize/2, cellSize, cellSize);
                    
                    // 绘制单元格值
                    ctx.fillStyle = "#333";
                    if (i === 0 && j === 0) {
                        ctx.fillText("", x, y); // 左上角空白
                    } else {
                        ctx.fillText(dp[i][j], x, y);
                    }
                    
                    // 如果是第一行或第一列，显示0
                    if ((i === 0 || j === 0) && !(i === 0 && j === 0)) {
                        ctx.fillStyle = "#95a5a6";
                        ctx.fillText("0", x, y);
                    }
                }
            }
            
            // 绘制当前字符比较高亮
            if (!isBacktracking && currentI > 0 && currentJ > 0 && currentStep > 0 && currentStep <= totalSteps) {
                const char1 = str1[currentI - 1];
                const char2 = str2[currentJ - 1];
                
                // 高亮字符串1的字符
                const x1 = startX - cellSize;
                const y1 = startY + currentI * cellSize;
                ctx.fillStyle = char1 === char2 ? "#d4edda" : "#f8d7da";
                ctx.fillRect(x1 - cellSize/2, y1 - cellSize/2, cellSize, cellSize);
                ctx.fillStyle = "#333";
                ctx.fillText(char1, x1, y1);
                
                // 高亮字符串2的字符
                const x2 = startX + currentJ * cellSize;
                const y2 = startY - cellSize;
                ctx.fillStyle = char1 === char2 ? "#d4edda" : "#f8d7da";
                ctx.fillRect(x2 - cellSize/2, y2 - cellSize/2, cellSize, cellSize);
                ctx.fillStyle = "#333";
                ctx.fillText(char2, x2, y2);
                
                // 绘制箭头指示
                drawArrows(currentI, currentJ);
            }
            
            // 绘制回溯路径箭头
            if (isBacktracking && backtrackPath.length > 1) {
                for (let k = 1; k < backtrackPath.length; k++) {
                    const prev = backtrackPath[k-1];
                    const curr = backtrackPath[k];
                    
                    const x1 = startX + prev.j * cellSize;
                    const y1 = startY + prev.i * cellSize;
                    const x2 = startX + curr.j * cellSize;
                    const y2 = startY + curr.i * cellSize;
                    
                    // 绘制箭头
                    ctx.strokeStyle = "#d35400";
                    ctx.lineWidth = 3;
                    ctx.beginPath();
                    ctx.moveTo(x1, y1);
                    ctx.lineTo(x2, y2);
                    ctx.stroke();
                    
                    // 绘制箭头头部
                    drawArrowHead(x1, y1, x2, y2, "#d35400");
                }
            }
            
            // 绘制网格标签
            ctx.font = "14px Arial";
            ctx.fillStyle = "#7f8c8d";
            ctx.textAlign = "center";
            
            // 行标签
            for (let i = 0; i <= m; i++) {
                const x = startX - cellSize * 1.5;
                const y = startY + i * cellSize;
                ctx.fillText(i.toString(), x, y);
            }
            
            // 列标签
            for (let j = 0; j <= n; j++) {
                const x = startX + j * cellSize;
                const y = startY - cellSize * 1.5;
                ctx.fillText(j.toString(), x, y);
            }
            
            // 绘制标签说明
            ctx.font = "12px Arial";
            ctx.fillStyle = "#7f8c8d";
            ctx.textAlign = "right";
            ctx.fillText("i", startX - cellSize * 1.5, startY - cellSize * 1.5);
            ctx.textAlign = "center";
            ctx.fillText("j", startX - cellSize * 1.5, startY - cellSize * 1.5);
        }
        
        // 绘制箭头
        function drawArrows(i, j) {
            const x = startX + j * cellSize;
            const y = startY + i * cellSize;
            
            const char1 = str1[i - 1];
            const char2 = str2[j - 1];
            
            if (char1 === char2) {
                // 来自左上角
                const prevX = startX + (j - 1) * cellSize;
                const prevY = startY + (i - 1) * cellSize;
                
                ctx.strokeStyle = "#dc3545";
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(prevX, prevY);
                ctx.lineTo(x, y);
                ctx.stroke();
                
                drawArrowHead(prevX, prevY, x, y, "#dc3545");
            } else {
                // 可能来自上方或左方
                const fromTop = dp[i][j] === dp[i-1][j];
                const fromLeft = dp[i][j] === dp[i][j-1];
                
                if (fromTop) {
                    // 来自上方
                    const prevX = startX + j * cellSize;
                    const prevY = startY + (i - 1) * cellSize;
                    
                    ctx.strokeStyle = "#007bff";
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.moveTo(prevX, prevY);
                    ctx.lineTo(x, y);
                    ctx.stroke();
                    
                    drawArrowHead(prevX, prevY, x, y, "#007bff");
                }
                
                if (fromLeft) {
                    // 来自左方
                    const prevX = startX + (j - 1) * cellSize;
                    const prevY = startY + i * cellSize;
                    
                    ctx.strokeStyle = "#28a745";
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.moveTo(prevX, prevY);
                    ctx.lineTo(x, y);
                    ctx.stroke();
                    
                    drawArrowHead(prevX, prevY, x, y, "#28a745");
                }
            }
        }
        
        // 绘制箭头头部
        function drawArrowHead(fromX, fromY, toX, toY, color) {
            const headlen = 10;
            const angle = Math.atan2(toY - fromY, toX - fromX);
            
            ctx.fillStyle = color;
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(
                toX - headlen * Math.cos(angle - Math.PI / 6),
                toY - headlen * Math.sin(angle - Math.PI / 6)
            );
            ctx.lineTo(
                toX - headlen * Math.cos(angle + Math.PI / 6),
                toY - headlen * Math.sin(angle + Math.PI / 6)
            );
            ctx.closePath();
            ctx.fill();
        }
        
        // 高亮单元格
        function highlightCell(i, j, color) {
            const x = startX + j * cellSize;
            const y = startY + i * cellSize;
            
            ctx.fillStyle = color;
            ctx.fillRect(x - cellSize/2, y - cellSize/2, cellSize, cellSize);
            
            // 重新绘制边框和文本
            ctx.strokeStyle = "#ddd";
            ctx.lineWidth = 1;
            ctx.strokeRect(x - cellSize/2, y - cellSize/2, cellSize, cellSize);
            
            ctx.fillStyle = "#333";
            ctx.font = "bold 20px Arial";
            ctx.textAlign = "center";
            ctx.textBaseline = "middle";
            
            if (i === 0 && j === 0) {
                ctx.fillText("", x, y);
            } else if (i === 0 || j === 0) {
                ctx.fillStyle = "#95a5a6";
                ctx.fillText("0", x, y);
            } else {
                ctx.fillStyle = "#333";
                ctx.fillText(dp[i][j], x, y);
            }
        }
        
        // 更新步骤信息
        function updateStepInfo(title, description) {
            stepInfo.innerHTML = `
                <div class="step-title">${title}</div>
                <p>${description}</p>
            `;
        }
        
        // 更新单元格步骤信息
        function updateStepInfoForCell(i, j, isCalculated) {
            if (i === 0 || j === 0) {
                updateStepInfo("边界单元格", `dp[${i}][${j}] = 0 (边界初始化)`);
                return;
            }
            
            const char1 = str1[i - 1];
            const char2 = str2[j - 1];
            
            if (!isCalculated) {
                updateStepInfo(
                    `准备计算 dp[${i}][${j}]`,
                    `即将计算 dp[${i}][${j}]，比较字符 str1[${i-1}]='${char1}' 和 str2[${j-1}]='${char2}'`
                );
                return;
            }
            
            let description = "";
            let equationHighlight = "case1";
            
            if (char1 === char2) {
                description = `字符相等：str1[${i-1}]='${char1}' == str2[${j-1}]='${char2}'，因此 dp[${i}][${j}] = dp[${i-1}][${j-1}] + 1 = ${dp[i-1][j-1]} + 1 = ${dp[i][j]}`;
                equationHighlight = "case1";
            } else {
                const fromTop = dp[i][j] === dp[i-1][j];
                const fromLeft = dp[i][j] === dp[i][j-1];
                
                if (fromTop && fromLeft) {
                    description = `字符不等：str1[${i-1}]='${char1}' != str2[${j-1}]='${char2}'，dp[${i-1}][${j}] = ${dp[i-1][j]}，dp[${i}][${j-1}] = ${dp[i][j-1]}，两者相等，取 max = ${dp[i][j]}`;
                } else if (fromTop) {
                    description = `字符不等：str1[${i-1}]='${char1}' != str2[${j-1}]='${char2}'，dp[${i-1}][${j}] = ${dp[i-1][j]}，dp[${i}][${j-1}] = ${dp[i][j-1]}，取 max = ${dp[i-1][j]} = ${dp[i][j]}`;
                } else {
                    description = `字符不等：str1[${i-1}]='${char1}' != str2[${j-1}]='${char2}'，dp[${i-1}][${j}] = ${dp[i-1][j]}，dp[${i}][${j-1}] = ${dp[i][j-1]}，取 max = ${dp[i][j-1]} = ${dp[i][j]}`;
                }
                equationHighlight = "case2";
            }
            
            updateStepInfo(`计算 dp[${i}][${j}]`, description);
            updateEquation(equationHighlight);
        }
        
        // 更新回溯步骤信息
        function updateStepInfoForBacktrack(i, j, nextCell) {
            let description = "";
            
            if (nextCell.direction === "diagonal") {
                description = `dp[${i}][${j}] = ${dp[i][j]}，来自 dp[${i-1}][${j-1}] = ${dp[i-1][j-1]}，字符匹配 '${nextCell.char}'，添加到LCS`;
            } else if (nextCell.direction === "up") {
                description = `dp[${i}][${j}] = ${dp[i][j]}，来自 dp[${i-1}][${j}] = ${dp[i-1][j]}，字符不匹配，继续回溯`;
            } else {
                description = `dp[${i}][${j}] = ${dp[i][j]}，来自 dp[${i}][${j-1}] = ${dp[i][j-1]}，字符不匹配，继续回溯`;
            }
            
            updateStepInfo(`回溯 dp[${i}][${j}]`, description);
        }
        
        // 更新方程显示
        function updateEquation(highlight) {
            if (highlight === "初始化") {
                equationInfo.innerHTML = `
                    dp[i][j] = <br>
                    <span style="color: #dc3545; font-weight: bold;">dp[i-1][j-1] + 1</span> 
                    <span>如果 str1[i-1] == str2[j-1]</span><br>
                    <span>否则取 </span>
                    <span style="color: #007bff; font-weight: bold;">max(dp[i-1][j], dp[i][j-1])</span>
                `;
            } else if (highlight === "case1") {
                equationInfo.innerHTML = `
                    dp[i][j] = <br>
                    <span style="color: #dc3545; font-weight: bold; background-color: #ffe6e6; padding: 2px 5px; border-radius: 3px;">dp[i-1][j-1] + 1</span> 
                    <span>如果 str1[i-1] == str2[j-1]</span><br>
                    <span>否则取 </span>
                    <span style="color: #007bff; font-weight: bold;">max(dp[i-1][j], dp[i][j-1])</span>
                `;
            } else {
                equationInfo.innerHTML = `
                    dp[i][j] = <br>
                    <span style="color: #dc3545; font-weight: bold;">dp[i-1][j-1] + 1</span> 
                    <span>如果 str1[i-1] == str2[j-1]</span><br>
                    <span>否则取 </span>
                    <span style="color: #007bff; font-weight: bold; background-color: #e6f2ff; padding: 2px 5px; border-radius: 3px;">max(dp[i-1][j], dp[i][j-1])</span>
                `;
            }
        }
        
        // 更新结果
        function updateResult() {
            if (!isTableGenerated) {
                lcsLength.textContent = "0";
                lcsSequenceEl.textContent = "-";
                multiplePaths.style.display = "none";
                return;
            }
            
            if (isBacktracking) {
                lcsLength.textContent = lcsSequence.length;
                lcsSequenceEl.textContent = lcsSequence || "(空)";
            } else {
                lcsLength.textContent = dp[m] ? dp[m][n] : "0";
                lcsSequenceEl.textContent = "-";
                multiplePaths.style.display = "none";
            }
        }
        
        // 更新状态
        function updateStatus(text) {
            statusText.textContent = text;
        }
        
        // 更新UI
        function updateUI() {
            // 更新播放按钮文本
            playBtn.textContent = isPlaying ? "暂停" : "播放";
            
            // 更新回溯按钮
            if (isBacktracking) {
                backtrackBtn.textContent = "重置回溯";
                backtrackBtn.classList.remove("btn-info");
                backtrackBtn.classList.add("btn-warning");
            } else {
                backtrackBtn.textContent = "开始回溯";
                backtrackBtn.classList.remove("btn-warning");
                backtrackBtn.classList.add("btn-info");
            }
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 交互式教学动画使用指南

欢迎使用“最长公共子序列(LCS)动态规划教学动画”！本工具旨在通过直观、交互式的可视化方式，帮助您深入理解动态规划求解LCS的核心思想——表格填充与路径回溯。无论您是算法初学者，还是希望巩固动态规划概念的学习者，本动画都将为您提供沉浸式的学习体验。

---

#### 一、 功能说明

本动画将LCS的动态规划求解过程分解为两个核心阶段：
1.  **表格填充阶段**：动态展示如何根据状态转移方程，从左上到右下逐步填充整个二维DP表格。
2.  **路径回溯阶段**：在填充完成的表格上，演示如何从右下角回溯到左上角，寻找并构造出最长公共子序列。

通过分步控制、高亮提示和交互探索，您将清晰地看到每个单元格数值的来源，并理解“斜线”在匹配字符和构造解中的关键作用。

#### 二、 主要功能

1.  **输入与初始化**
    *   **预设示例**：提供多个经典案例（如“ABCBDAB”与“BDCABA”），一键加载。
    *   **自定义输入**：支持输入任意两个字符串（建议长度不超过15个字符），探索不同情况。
    *   **生成表格**：根据输入的字符串，初始化并绘制动态规划表格框架。

2.  **流程控制与演示**
    *   **分步执行**：使用“上一步”、“下一步”按钮，精确控制动画的每一步，仔细观察计算逻辑。
    *   **自动播放**：点击“播放”按钮，以设定的速度自动演示整个求解过程。
    *   **快速填充**：使用“填充全部”按钮，瞬间完成表格计算，快速查看最终结果。
    *   **速度调节**：通过滑块控制动画播放速度（从“很慢”到“很快”），适应不同学习节奏。

3.  **交互式探索**
    *   **两种模式**：
        *   **自动演示模式**：系统引导您完成标准求解流程，适合首次学习。
        *   **手动探索模式**：您可以自由点击表格中的任意单元格，系统会即时显示该单元格值的详细计算过程和来源箭头，适合深度探究。
    *   **回溯路径选择**：当存在多条等长的LCS路径时，在回溯阶段，系统会高亮所有可能的来源单元格，允许您手动选择不同的路径，观察如何得到不同的最长公共子序列。

4.  **可视化与信息反馈**
    *   **彩色编码**：
        *   **红色箭头(↖)**：表示字符相等，值来自左上方单元格 `dp[i-1][j-1] + 1`。
        *   **蓝色箭头(↑)**：表示值来自上方单元格 `dp[i-1][j]`。
        *   **绿色箭头(←)**：表示值来自左方单元格 `dp[i][j-1]`。
        *   **高亮色块**：清晰标识当前计算单元格、匹配的字符、LCS路径及可选回溯路径。
    *   **实时信息面板**：
        *   **当前步骤**：详细描述每一步发生了什么。
        *   **状态转移方程**：动态高亮当前步骤对应的公式部分。
        *   **结果展示**：实时显示已找到的LCS长度和序列内容。
    *   **状态栏**：始终显示当前系统状态和操作提示。

#### 三、 设计特色

1.  **认知负荷优化**：通过分阶段、焦点高亮和渐进式信息呈现，避免信息过载，符合学习者的认知规律。
2.  **从具象到抽象**：使用具体字符串案例建立直观印象，再通过交互引导理解抽象的状态转移方程。
3.  **错误驱动学习**：在手动探索模式下，鼓励点击和尝试，即时反馈机制让您从“错误”或“意外”的路径中发现算法的本质。
4.  **多路径支持**：专门处理存在多个LCS的情况，让您理解动态规划表格如何蕴含全部最优解，而回溯是选择其中一个解的过程。
5.  **响应式设计**：界面适配不同屏幕尺寸，确保在各种设备上都能获得良好的学习体验。

#### 四、 教学要点

在使用本动画学习或教学时，请重点关注以下核心概念：

1.  **状态与子问题**：理解 `dp[i][j]` 定义的子问题是什么（`str1` 前 `i` 个字符与 `str2` 前 `j` 个字符的LCS长度）。
2.  **状态转移的逻辑**：
    *   **字符相等时（走斜线）**：当前字符可以加入LCS，因此子问题规模缩小，LCS长度+1。
    *   **字符不等时（走上或左）**：当前字符不能同时加入LCS，因此继承 `str1` 或 `str2` 缩小一个字符时的最优解。
3.  **填表顺序的意义**：为什么必须从左到右、从上到下填充？因为这保证了计算 `dp[i][j]` 时，它所依赖的 `dp[i-1][j-1]`、`dp[i-1][j]` 和 `dp[i][j-1]` 都已被计算出来。
4.  **回溯构造解**：理解表格中数值的“来源”就是解的构造线索。**优先选择斜线方向**，意味着将匹配的字符加入解中；选择上方或左方，意味着跳过当前不匹配的字符。
5.  **空间与时间的权衡**：通过动画直观感受O(m*n)的时间与空间复杂度。可以思考如何优化空间（滚动数组）。

#### 五、 使用建议

**给学习者：**
1.  **首次学习**：选择预设示例，切换到“自动演示模式”，点击“播放”，跟随动画完整观看一遍。然后使用“上一步/下一步”分步复盘，结合右侧信息面板理解每一步。
2.  **巩固理解**：切换到“手动探索模式”，尝试自定义字符串。在填充阶段，随机点击单元格查看其计算逻辑；在回溯阶段，尝试选择不同的路径。
3.  **挑战自我**：输入一些有特点的字符串，如：
    *   完全相同的字符串（观察表格特点）。
    *   完全不同的字符串（观察表格特点）。
    *   存在多个LCS的字符串（如“ABC”、“ACB”），体验多路径回溯。

**给教师/教学者：**
1.  **课堂演示**：可将本动画作为课件的一部分，在讲解LCS时进行动态演示。利用“分步执行”功能，与讲解节奏同步。
2.  **布置探索任务**：可以要求学生使用本工具验证特定字符串的LCS，或回答诸如“为什么这里可以走蓝色箭头也可以走绿色箭头？”、“如果改变字符串顺序，LCS会变吗？”等问题。
3.  **引导讨论**：在演示后，可以引导学生讨论设计背后的思想：颜色编码是否有效？交互设计如何帮助理解？如何将动画中的过程转化为伪代码？

---

我们希望这个精心设计的交互式动画，能像一位耐心的向导，帮助您穿越动态规划求解LCS的思维迷宫，不仅“看到”结果，更能“理解”过程。祝您学习愉快，探索顺利！