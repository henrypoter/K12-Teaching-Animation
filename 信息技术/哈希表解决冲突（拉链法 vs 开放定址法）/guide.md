# 需求：哈希表解决冲突（拉链法 vs 开放定址法）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要是计算机科学或相关专业的学生，他们正在学习数据结构与算法课程。用户的核心需求是：
1.  **理解概念**：清晰理解哈希表的基本原理、哈希冲突的必然性，以及两种主流解决策略（拉链法与开放定址法）的核心思想和工作流程。
2.  **对比差异**：直观地看到两种方法在数据结构、插入、查找、删除操作上的根本区别，理解各自的优缺点和适用场景。
3.  **动态观察**：希望通过动态、可视化的方式，观察数据项如何被插入哈希表，冲突如何发生以及如何被解决，而不是静态地阅读文字描述。
4.  **主动探索**：能够通过交互（如输入数据、选择方法、触发步骤）来控制动画，加深对算法流程的理解和记忆。

#### 教学设计思路
1.  **核心概念分解**：
    *   **基石**：哈希函数（将输入映射到固定范围的索引）。
    *   **问题**：哈希冲突（不同输入映射到同一索引）。
    *   **解决方案A（拉链法）**：每个索引位置是一个“桶”（链表或其他容器），冲突元素被放入同一个桶中。
    *   **解决方案B（开放定址法）**：所有元素都存放在数组本身中。发生冲突时，按照某种探测序列（如线性探测、平方探测）寻找下一个空闲位置。
    *   **关键对比**：数据结构（链表数组 vs 对象数组）、空间开销、查找性能、对删除操作的处理。

2.  **遵循认知规律**：
    *   **从已知到未知**：先回顾数组和链表，再引入哈希表。
    *   **从简单到复杂**：先展示无冲突的理想插入，再引入冲突，最后展示解决方案。
    *   **对比学习**：将两种方法并置，同步演示相同数据集的操作，突出差异。
    *   **及时反馈**：在用户交互后（如点击插入），动画应清晰展示当前步骤的计算过程（计算哈希值、检查位置、处理冲突）和结果。

3.  **交互设计**：
    *   **双视图对比**：界面主要分为左右两个并排的动画区域，分别代表拉链法和开放定址法（以线性探测为例）的哈希表。
    *   **流程控制**：提供“单步执行”、“连续播放”、“重置”按钮，允许用户控制动画节奏。
    *   **数据输入**：允许用户输入一组自定义的键值对，或从预设数据集中选择，以观察不同数据下的表现。
    *   **操作选择**：可以单独执行“插入”、“查找”或“删除”操作，并指定要操作的键。
    *   **高亮与提示**：动画过程中，高亮当前正在处理的元素、计算出的哈希值、当前检查的数组位置/链表节点，并用文字提示说明当前状态（如“发生冲突！”、“沿链表查找”、“探测下一个位置”）。

4.  **视觉呈现**：
    *   **哈希表结构**：
        *   拉链法：用一个水平数组表示，每个单元格下方垂直延伸出一个链表（用节点和箭头表示）。
        *   开放定址法：用一个水平数组表示，每个单元格直接存放键值对或标记（空/已删除）。
    *   **数据元素**：设计成色彩鲜明、带有键（Key）和值（Value）标识的卡片或圆球。
    *   **动态效果**：
        *   元素移动：从“输入区”移动到计算出的哈希索引位置。
        *   冲突处理：拉链法中，新元素“挂”到链表末端；开放定址法中，元素按探测序列“跳跃”到下一个空闲位置。
        *   查找路径：查找时，高亮遍历过的链表节点或探测过的数组位置。
    *   **信息面板**：显示当前操作说明、哈希函数公式、探测序列、统计数据（冲突次数、平均查找长度等）。

#### 配色方案选择
*   **主色调**：采用科技蓝（`#3498db`）作为主色，代表逻辑与计算。
*   **辅助色**：
    *   拉链法视图使用蓝绿色系（如 `#1abc9c`），体现链式结构。
    *   开放定址法视图使用紫色系（如 `#9b59b6`），体现数组内寻址。
*   **元素色**：
    *   数据元素：使用温和的暖色（如 `#e74c3c` 红色代表键，`#f39c12` 橙色代表值），与背景形成对比。
    *   高亮色：使用醒目的亮黄色（`#f1c40f`）或亮绿色（`#2ecc71`）表示当前活动元素、哈希命中位置或查找路径。
    *   状态色：灰色（`#bdc3c7`）表示空位置，浅红色（`#eaa4a4`）表示“已删除”标记（针对开放定址法）。
*   **背景与文字**：浅灰色（`#ecf0f1`）背景，深灰色（`#2c3e50`）文字，确保可读性和舒适度。

#### 交互功能列表
1.  **数据管理**：
    *   预设数据集选择（如一组易冲突的键）。
    *   自定义数据输入框（输入键值对，格式如 `key:value`）。
    *   “加载数据”按钮。
2.  **方法选择**：默认双视图同时展示，也可提供单选按钮只查看一种方法。
3.  **操作控制**：
    *   `插入(Insert)` 按钮：将当前输入数据插入两个哈希表。
    *   `查找(Search)` 按钮：输入一个键，在两个表中演示查找过程。
    *   `删除(Delete)` 按钮：输入一个键，演示删除过程（重点展示开放定址法的“已删除”标记）。
    *   `单步(Step)` 按钮：将插入/查找/删除操作分解为更细的步骤（计算哈希、访问索引、解决冲突等）逐步执行。
    *   `播放(Play)` / `暂停(Pause)` 按钮：连续自动执行一系列操作。
    *   `重置(Reset)` 按钮：清空两个哈希表，回到初始状态。
4.  **动画视图**：
    *   实时高亮当前操作的键、计算出的哈希值。
    *   动态显示元素移动和链接过程。
    *   冲突发生时，显示视觉提示（如闪烁）和文字说明。
    *   在开放定址法中，可视化探测序列的路径。
5.  **信息显示**：
    *   当前操作状态提示。
    *   哈希函数表达式显示。
    *   实时统计信息（表大小、元素数量、总冲突次数、当前冲突次数）。
    *   简要的优缺点文字总结，根据操作结果动态更新。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>哈希表冲突解决教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #ecf0f1;
            color: #2c3e50;
            line-height: 1.6;
            padding: 20px;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
        }

        .main-content {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .control-panel {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }

        .control-section {
            margin-bottom: 20px;
        }

        h2 {
            color: #3498db;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #ecf0f1;
        }

        h3 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .data-input {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            align-items: center;
        }

        input[type="text"] {
            padding: 10px 15px;
            border: 2px solid #bdc3c7;
            border-radius: 5px;
            font-size: 1rem;
            flex: 1;
            min-width: 200px;
        }

        input[type="text"]:focus {
            outline: none;
            border-color: #3498db;
        }

        .btn {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
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

        .btn-group {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .preset-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .preset-btn {
            background-color: #9b59b6;
            color: white;
        }

        .preset-btn:hover {
            background-color: #8e44ad;
        }

        .animation-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }

        .animation-view {
            flex: 1;
            min-width: 600px;
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            display: flex;
            flex-direction: column;
        }

        .view-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #ecf0f1;
        }

        .method-title {
            font-size: 1.5rem;
            font-weight: bold;
        }

        .chaining-title {
            color: #1abc9c;
        }

        .open-addressing-title {
            color: #9b59b6;
        }

        .canvas-container {
            flex: 1;
            border: 2px solid #ecf0f1;
            border-radius: 5px;
            overflow: auto;
            position: relative;
        }

        canvas {
            display: block;
        }

        .info-panel {
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
        }

        .stats-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 15px;
        }

        .stats-box {
            flex: 1;
            min-width: 200px;
            padding: 15px;
            border-radius: 5px;
        }

        .chaining-stats {
            background-color: rgba(26, 188, 156, 0.1);
            border-left: 4px solid #1abc9c;
        }

        .addressing-stats {
            background-color: rgba(155, 89, 182, 0.1);
            border-left: 4px solid #9b59b6;
        }

        .stat-item {
            margin-bottom: 10px;
            display: flex;
            justify-content: space-between;
        }

        .status-bar {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
            border-left: 4px solid #f1c40f;
            font-weight: 500;
        }

        .explanation {
            margin-top: 20px;
            padding: 15px;
            background-color: #f8f9fa;
            border-radius: 5px;
            border-left: 4px solid #3498db;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
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

        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #7f8c8d;
            font-size: 0.9rem;
        }

        @media (max-width: 1200px) {
            .animation-container {
                flex-direction: column;
            }
            
            .animation-view {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>哈希表冲突解决教学动画</h1>
            <p class="subtitle">拉链法 vs 开放定址法（线性探测）</p>
        </header>

        <div class="main-content">
            <div class="control-panel">
                <div class="control-section">
                    <h2>数据控制</h2>
                    <div class="data-input">
                        <input type="text" id="keyInput" placeholder="输入键 (如: apple)">
                        <input type="text" id="valueInput" placeholder="输入值 (如: 10)">
                        <button class="btn btn-primary" id="insertBtn">插入</button>
                        <button class="btn btn-secondary" id="searchBtn">查找</button>
                        <button class="btn btn-warning" id="deleteBtn">删除</button>
                    </div>
                    
                    <div style="margin-top: 15px;">
                        <h3>预设数据集</h3>
                        <div class="preset-buttons">
                            <button class="btn preset-btn" data-preset="simple">简单数据</button>
                            <button class="btn preset-btn" data-preset="conflict">易冲突数据</button>
                            <button class="btn preset-btn" data-preset="numbers">数字数据</button>
                            <button class="btn btn-warning" id="clearBtn">清空哈希表</button>
                        </div>
                    </div>
                </div>

                <div class="control-section">
                    <h2>动画控制</h2>
                    <div class="btn-group">
                        <button class="btn btn-primary" id="stepBtn">单步执行</button>
                        <button class="btn btn-secondary" id="playBtn">连续播放</button>
                        <button class="btn" id="pauseBtn" disabled>暂停</button>
                        <button class="btn" id="resetBtn">重置动画</button>
                    </div>
                </div>

                <div class="control-section">
                    <h2>哈希函数设置</h2>
                    <div style="display: flex; align-items: center; gap: 15px;">
                        <div>h(key) = (sum(key.charCodeAt(i))) % <input type="number" id="tableSize" value="7" min="5" max="15" style="width: 60px; padding: 5px;"> </div>
                        <button class="btn" id="applySizeBtn">应用新大小</button>
                    </div>
                </div>
            </div>

            <div class="animation-container">
                <div class="animation-view">
                    <div class="view-header">
                        <div class="method-title chaining-title">拉链法 (Separate Chaining)</div>
                        <div>表大小: <span id="chainingSize">7</span></div>
                    </div>
                    <div class="canvas-container">
                        <canvas id="chainingCanvas" width="800" height="400"></canvas>
                    </div>
                </div>

                <div class="animation-view">
                    <div class="view-header">
                        <div class="method-title open-addressing-title">开放定址法 (Open Addressing)</div>
                        <div>表大小: <span id="addressingSize">7</span></div>
                    </div>
                    <div class="canvas-container">
                        <canvas id="addressingCanvas" width="800" height="400"></canvas>
                    </div>
                </div>
            </div>

            <div class="info-panel">
                <h2>信息与统计</h2>
                <div class="status-bar" id="statusBar">就绪。请插入数据或选择预设数据集开始。</div>
                
                <div class="stats-container">
                    <div class="stats-box chaining-stats">
                        <h3 class="chaining-title">拉链法统计</h3>
                        <div class="stat-item">
                            <span>元素数量:</span>
                            <span id="chainingCount">0</span>
                        </div>
                        <div class="stat-item">
                            <span>冲突次数:</span>
                            <span id="chainingConflicts">0</span>
                        </div>
                        <div class="stat-item">
                            <span>最长链表:</span>
                            <span id="chainingMaxChain">0</span>
                        </div>
                        <div class="stat-item">
                            <span>平均查找长度:</span>
                            <span id="chainingASL">0.00</span>
                        </div>
                    </div>
                    
                    <div class="stats-box addressing-stats">
                        <h3 class="open-addressing-title">开放定址法统计</h3>
                        <div class="stat-item">
                            <span>元素数量:</span>
                            <span id="addressingCount">0</span>
                        </div>
                        <div class="stat-item">
                            <span>冲突次数:</span>
                            <span id="addressingConflicts">0</span>
                        </div>
                        <div class="stat-item">
                            <span>探测次数:</span>
                            <span id="addressingProbes">0</span>
                        </div>
                        <div class="stat-item">
                            <span>平均查找长度:</span>
                            <span id="addressingASL">0.00</span>
                        </div>
                    </div>
                </div>
                
                <div class="explanation">
                    <h3>当前操作说明</h3>
                    <p id="explanationText">哈希表是一种通过哈希函数将键映射到表中位置来访问数据的数据结构。当不同的键映射到同一位置时，发生哈希冲突。本动画演示两种解决冲突的方法。</p>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span>键 (Key)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f39c12;"></div>
                        <span>值 (Value)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2ecc71;"></div>
                        <span>当前活动元素</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f1c40f;"></div>
                        <span>哈希计算位置</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #bdc3c7;"></div>
                        <span>空位置</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #eaa4a4;"></div>
                        <span>已删除标记</span>
                    </div>
                </div>
            </div>
        </div>

        <footer>
            <p>哈希表冲突解决教学动画 | 使用HTML5 Canvas实现 | 设计用于数据结构与算法教学</p>
        </footer>
    </div>

    <script>
        // 哈希表类定义
        class HashTableAnimation {
            constructor(canvasId, method) {
                this.canvas = document.getElementById(canvasId);
                this.ctx = this.canvas.getContext('2d');
                this.method = method; // 'chaining' 或 'addressing'
                this.tableSize = 7;
                this.data = method === 'chaining' ? [] : new Array(this.tableSize).fill(null);
                this.conflictCount = 0;
                this.elementCount = 0;
                this.totalProbes = 0;
                this.totalSearchLength = 0;
                this.searchCount = 0;
                
                // 动画状态
                this.animationState = 'idle';
                this.currentStep = 0;
                this.steps = [];
                this.animationSpeed = 500; // ms
                this.animationInterval = null;
                
                // 高亮元素
                this.highlightedIndex = -1;
                this.highlightedElement = null;
                this.highlightedChain = [];
                this.highlightedProbes = [];
                
                this.initTable();
            }
            
            initTable() {
                if (this.method === 'chaining') {
                    this.data = [];
                    for (let i = 0; i < this.tableSize; i++) {
                        this.data.push([]);
                    }
                } else {
                    this.data = new Array(this.tableSize).fill(null);
                }
                this.conflictCount = 0;
                this.elementCount = 0;
                this.totalProbes = 0;
                this.totalSearchLength = 0;
                this.searchCount = 0;
            }
            
            hashFunction(key) {
                let hash = 0;
                for (let i = 0; i < key.length; i++) {
                    hash += key.charCodeAt(i);
                }
                return hash % this.tableSize;
            }
            
            // 线性探测函数
            linearProbe(index, step) {
                return (index + step) % this.tableSize;
            }
            
            insert(key, value, animate = true) {
                const hashIndex = this.hashFunction(key);
                const element = { key, value, hashIndex };
                
                if (animate) {
                    this.steps = [];
                    this.steps.push({
                        action: 'calculate_hash',
                        element,
                        index: hashIndex,
                        message: `计算哈希值: h("${key}") = ${hashIndex}`
                    });
                }
                
                if (this.method === 'chaining') {
                    return this.insertChaining(key, value, hashIndex, element, animate);
                } else {
                    return this.insertAddressing(key, value, hashIndex, element, animate);
                }
            }
            
            insertChaining(key, value, hashIndex, element, animate) {
                const chain = this.data[hashIndex];
                let conflict = false;
                
                // 检查键是否已存在
                for (let i = 0; i < chain.length; i++) {
                    if (chain[i].key === key) {
                        if (animate) {
                            this.steps.push({
                                action: 'key_exists',
                                element,
                                index: hashIndex,
                                chainIndex: i,
                                message: `键 "${key}" 已存在，更新值`
                            });
                        }
                        chain[i].value = value;
                        return { success: true, conflict: false };
                    }
                }
                
                // 检查是否有冲突（链表不为空）
                if (chain.length > 0) {
                    conflict = true;
                    this.conflictCount++;
                    
                    if (animate) {
                        this.steps.push({
                            action: 'conflict_detected',
                            element,
                            index: hashIndex,
                            message: `冲突！位置 ${hashIndex} 已有元素`
                        });
                        
                        this.steps.push({
                            action: 'add_to_chain',
                            element,
                            index: hashIndex,
                            chainIndex: chain.length,
                            message: `将元素添加到链表末尾`
                        });
                    }
                } else if (animate) {
                    this.steps.push({
                        action: 'insert_direct',
                        element,
                        index: hashIndex,
                        message: `位置 ${hashIndex} 为空，直接插入`
                    });
                }
                
                chain.push(element);
                this.elementCount++;
                
                return { success: true, conflict };
            }
            
            insertAddressing(key, value, hashIndex, element, animate) {
                let currentIndex = hashIndex;
                let probeStep = 0;
                let conflict = false;
                
                while (probeStep < this.tableSize) {
                    if (animate && probeStep > 0) {
                        this.steps.push({
                            action: 'probe_next',
                            element,
                            index: currentIndex,
                            probeStep,
                            message: `探测下一个位置: ${currentIndex}`
                        });
                    }
                    
                    if (this.data[currentIndex] === null) {
                        // 找到空位置
                        if (probeStep > 0) {
                            conflict = true;
                            this.conflictCount++;
                            
                            if (animate) {
                                this.steps.push({
                                    action: 'conflict_resolved',
                                    element,
                                    index: currentIndex,
                                    probeStep,
                                    message: `冲突解决！在位置 ${currentIndex} 插入`
                                });
                            }
                        } else if (animate) {
                            this.steps.push({
                                action: 'insert_direct',
                                element,
                                index: currentIndex,
                                message: `位置 ${currentIndex} 为空，直接插入`
                            });
                        }
                        
                        this.data[currentIndex] = element;
                        this.elementCount++;
                        this.totalProbes += probeStep;
                        return { success: true, conflict };
                    } else if (this.data[currentIndex].key === key) {
                        // 键已存在
                        if (animate) {
                            this.steps.push({
                                action: 'key_exists',
                                element,
                                index: currentIndex,
                                message: `键 "${key}" 已存在，更新值`
                            });
                        }
                        this.data[currentIndex].value = value;
                        return { success: true, conflict: false };
                    }
                    
                    // 继续探测
                    probeStep++;
                    currentIndex = this.linearProbe(hashIndex, probeStep);
                }
                
                // 表已满
                if (animate) {
                    this.steps.push({
                        action: 'table_full',
                        element,
                        message: `哈希表已满，无法插入 "${key}"`
                    });
                }
                return { success: false, conflict: false };
            }
            
            search(key, animate = true) {
                const hashIndex = this.hashFunction(key);
                
                if (animate) {
                    this.steps = [];
                    this.steps.push({
                        action: 'calculate_hash',
                        key,
                        index: hashIndex,
                        message: `计算哈希值: h("${key}") = ${hashIndex}`
                    });
                }
                
                if (this.method === 'chaining') {
                    return this.searchChaining(key, hashIndex, animate);
                } else {
                    return this.searchAddressing(key, hashIndex, animate);
                }
            }
            
            searchChaining(key, hashIndex, animate) {
                const chain = this.data[hashIndex];
                let searchLength = 1;
                
                if (chain.length === 0) {
                    if (animate) {
                        this.steps.push({
                            action: 'not_found',
                            key,
                            index: hashIndex,
                            message: `位置 ${hashIndex} 的链表为空，键 "${key}" 不存在`
                        });
                    }
                    this.searchCount++;
                    this.totalSearchLength += searchLength;
                    return { found: false, index: hashIndex, searchLength };
                }
                
                if (animate) {
                    this.steps.push({
                        action: 'check_chain',
                        key,
                        index: hashIndex,
                        message: `检查位置 ${hashIndex} 的链表`
                    });
                }
                
                for (let i = 0; i < chain.length; i++) {
                    if (animate && i > 0) {
                        this.steps.push({
                            action: 'traverse_chain',
                            key,
                            index: hashIndex,
                            chainIndex: i,
                            message: `遍历链表，检查第 ${i+1} 个节点`
                        });
                    }
                    
                    if (chain[i].key === key) {
                        if (animate) {
                            this.steps.push({
                                action: 'found',
                                key,
                                index: hashIndex,
                                chainIndex: i,
                                message: `在链表第 ${i+1} 个节点找到键 "${key}"`
                            });
                        }
                        searchLength = i + 1;
                        this.searchCount++;
                        this.totalSearchLength += searchLength;
                        return { found: true, index: hashIndex, chainIndex: i, searchLength };
                    }
                    
                    searchLength++;
                }
                
                if (animate) {
                    this.steps.push({
                        action: 'not_found',
                        key,
                        index: hashIndex,
                        message: `链表中未找到键 "${key}"`
                    });
                }
                this.searchCount++;
                this.totalSearchLength += searchLength;
                return { found: false, index: hashIndex, searchLength };
            }
            
            searchAddressing(key, hashIndex, animate) {
                let currentIndex = hashIndex;
                let probeStep = 0;
                let searchLength = 1;
                
                while (probeStep < this.tableSize) {
                    if (animate && probeStep > 0) {
                        this.steps.push({
                            action: 'probe_next',
                            key,
                            index: currentIndex,
                            probeStep,
                            message: `探测下一个位置: ${currentIndex}`
                        });
                    }
                    
                    if (this.data[currentIndex] === null) {
                        // 空位置，键不存在
                        if (animate) {
                            this.steps.push({
                                action: 'not_found',
                                key,
                                index: currentIndex,
                                message: `位置 ${currentIndex} 为空，键 "${key}" 不存在`
                            });
                        }
                        this.searchCount++;
                        this.totalSearchLength += searchLength;
                        return { found: false, index: currentIndex, searchLength };
                    } else if (this.data[currentIndex].key === key) {
                        // 找到键
                        if (animate) {
                            this.steps.push({
                                action: 'found',
                                key,
                                index: currentIndex,
                                probeStep,
                                message: `在位置 ${currentIndex} 找到键 "${key}"`
                            });
                        }
                        this.searchCount++;
                        this.totalSearchLength += searchLength;
                        return { found: true, index: currentIndex, searchLength };
                    }
                    
                    // 继续探测
                    probeStep++;
                    searchLength++;
                    currentIndex = this.linearProbe(hashIndex, probeStep);
                }
                
                if (animate) {
                    this.steps.push({
                        action: 'not_found',
                        key,
                        message: `遍历整个表未找到键 "${key}"`
                    });
                }
                this.searchCount++;
                this.totalSearchLength += searchLength;
                return { found: false, searchLength };
            }
            
            delete(key, animate = true) {
                const hashIndex = this.hashFunction(key);
                
                if (animate) {
                    this.steps = [];
                    this.steps.push({
                        action: 'calculate_hash',
                        key,
                        index: hashIndex,
                        message: `计算哈希值: h("${key}") = ${hashIndex}`
                    });
                }
                
                if (this.method === 'chaining') {
                    return this.deleteChaining(key, hashIndex, animate);
                } else {
                    return this.deleteAddressing(key, hashIndex, animate);
                }
            }
            
            deleteChaining(key, hashIndex, animate) {
                const chain = this.data[hashIndex];
                
                for (let i = 0; i < chain.length; i++) {
                    if (chain[i].key === key) {
                        if (animate) {
                            this.steps.push({
                                action: 'found',
                                key,
                                index: hashIndex,
                                chainIndex: i,
                                message: `在链表第 ${i+1} 个节点找到键 "${key}"`
                            });
                            
                            this.steps.push({
                                action: 'delete_from_chain',
                                key,
                                index: hashIndex,
                                chainIndex: i,
                                message: `从链表中删除键 "${key}"`
                            });
                        }
                        
                        chain.splice(i, 1);
                        this.elementCount--;
                        return { success: true, index: hashIndex };
                    }
                }
                
                if (animate) {
                    this.steps.push({
                        action: 'not_found',
                        key,
                        index: hashIndex,
                        message: `链表中未找到键 "${key}"`
                    });
                }
                return { success: false };
            }
            
            deleteAddressing(key, hashIndex, animate) {
                let currentIndex = hashIndex;
                let probeStep = 0;
                
                while (probeStep < this.tableSize) {
                    if (this.data[currentIndex] === null) {
                        // 空位置，键不存在
                        if (animate) {
                            this.steps.push({
                                action: 'not_found',
                                key,
                                index: currentIndex,
                                message: `位置 ${currentIndex} 为空，键 "${key}" 不存在`
                            });
                        }
                        return { success: false };
                    } else if (this.data[currentIndex].key === key) {
                        // 找到键，标记为已删除
                        if (animate) {
                            this.steps.push({
                                action: 'found',
                                key,
                                index: currentIndex,
                                probeStep,
                                message: `在位置 ${currentIndex} 找到键 "${key}"`
                            });
                            
                            this.steps.push({
                                action: 'mark_deleted',
                                key,
                                index: currentIndex,
                                message: `标记位置 ${currentIndex} 为已删除`
                            });
                        }
                        
                        this.data[currentIndex] = 'DELETED';
                        this.elementCount--;
                        return { success: true, index: currentIndex };
                    }
                    
                    probeStep++;
                    currentIndex = this.linearProbe(hashIndex, probeStep);
                }
                
                if (animate) {
                    this.steps.push({
                        action: 'not_found',
                        key,
                        message: `遍历整个表未找到键 "${key}"`
                    });
                }
                return { success: false };
            }
            
            resize(newSize) {
                const oldData = this.data;
                const oldSize = this.tableSize;
                
                this.tableSize = newSize;
                this.initTable();
                
                if (this.method === 'chaining') {
                    for (let i = 0; i < oldSize; i++) {
                        for (const element of oldData[i]) {
                            this.insert(element.key, element.value, false);
                        }
                    }
                } else {
                    for (let i = 0; i < oldSize; i++) {
                        if (oldData[i] && oldData[i] !== 'DELETED') {
                            this.insert(oldData[i].key, oldData[i].value, false);
                        }
                    }
                }
            }
            
            getStats() {
                let maxChainLength = 0;
                let asl = 0;
                
                if (this.method === 'chaining') {
                    for (const chain of this.data) {
                        if (chain.length > maxChainLength) {
                            maxChainLength = chain.length;
                        }
                    }
                    asl = this.searchCount > 0 ? (this.totalSearchLength / this.searchCount).toFixed(2) : '0.00';
                    
                    return {
                        elementCount: this.elementCount,
                        conflictCount: this.conflictCount,
                        maxChainLength,
                        asl
                    };
                } else {
                    asl = this.searchCount > 0 ? (this.totalSearchLength / this.searchCount).toFixed(2) : '0.00';
                    
                    return {
                        elementCount: this.elementCount,
                        conflictCount: this.conflictCount,
                        totalProbes: this.totalProbes,
                        asl
                    };
                }
            }
            
            // 动画控制
            startAnimation() {
                if (this.steps.length === 0) return;
                
                this.animationState = 'running';
                this.currentStep = 0;
                
                this.animationInterval = setInterval(() => {
                    if (this.currentStep < this.steps.length) {
                        this.executeStep(this.currentStep);
                        this.currentStep++;
                    } else {
                        this.stopAnimation();
                    }
                }, this.animationSpeed);
            }
            
            stopAnimation() {
                if (this.animationInterval) {
                    clearInterval(this.animationInterval);
                    this.animationInterval = null;
                }
                this.animationState = 'idle';
            }
            
            executeStep(stepIndex) {
                if (stepIndex >= this.steps.length) return;
                
                const step = this.steps[stepIndex];
                
                // 根据步骤类型更新高亮状态
                switch (step.action) {
                    case 'calculate_hash':
                        this.highlightedIndex = step.index;
                        this.highlightedElement = step.element || null;
                        this.highlightedChain = [];
                        this.highlightedProbes = [step.index];
                        break;
                        
                    case 'conflict_detected':
                    case 'insert_direct':
                    case 'conflict_resolved':
                        this.highlightedIndex = step.index;
                        this.highlightedElement = step.element || null;
                        break;
                        
                    case 'add_to_chain':
                        this.highlightedIndex = step.index;
                        this.highlightedElement = step.element || null;
                        this.highlightedChain = [step.chainIndex];
                        break;
                        
                    case 'check_chain':
                    case 'traverse_chain':
                        this.highlightedIndex = step.index;
                        this.highlightedChain = step.chainIndex !== undefined ? [step.chainIndex] : [];
                        break;
                        
                    case 'probe_next':
                        this.highlightedIndex = step.index;
                        this.highlightedProbes.push(step.index);
                        break;
                        
                    case 'found':
                        this.highlightedIndex = step.index;
                        if (step.chainIndex !== undefined) {
                            this.highlightedChain = [step.chainIndex];
                        }
                        break;
                        
                    case 'not_found':
                    case 'table_full':
                    case 'key_exists':
                    case 'delete_from_chain':
                    case 'mark_deleted':
                        // 保持当前高亮状态
                        break;
                }
                
                // 更新状态信息
                if (step.message && this.method === 'chaining') {
                    updateStatus(step.message, 'chaining');
                } else if (step.message && this.method === 'addressing') {
                    updateStatus(step.message, 'addressing');
                }
                
                this.draw();
            }
            
            stepForward() {
                if (this.currentStep < this.steps.length) {
                    this.executeStep(this.currentStep);
                    this.currentStep++;
                }
            }
            
            // 绘制函数
            draw() {
                this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
                
                if (this.method === 'chaining') {
                    this.drawChainingTable();
                } else {
                    this.drawAddressingTable();
                }
            }
            
            drawChainingTable() {
                const ctx = this.ctx;
                const tableWidth = this.canvas.width;
                const tableHeight = this.canvas.height;
                const cellWidth = 80;
                const cellHeight = 60;
                const startX = (tableWidth - this.tableSize * cellWidth) / 2;
                const startY = 80;
                
                // 绘制标题
                ctx.fillStyle = '#2c3e50';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('拉链法哈希表', tableWidth / 2, 30);
                
                // 绘制表头
                ctx.fillStyle = '#3498db';
                ctx.font = '14px Arial';
                for (let i = 0; i < this.tableSize; i++) {
                    const x = startX + i * cellWidth + cellWidth / 2;
                    const y = startY - 30;
                    
                    ctx.fillText(`索引 ${i}`, x, y);
                }
                
                // 绘制哈希表单元格
                for (let i = 0; i < this.tableSize; i++) {
                    const x = startX + i * cellWidth;
                    const y = startY;
                    
                    // 绘制单元格背景
                    ctx.fillStyle = i === this.highlightedIndex ? 'rgba(241, 196, 15, 0.3)' : '#f8f9fa';
                    ctx.fillRect(x, y, cellWidth, cellHeight);
                    
                    // 绘制单元格边框
                    ctx.strokeStyle = i === this.highlightedIndex ? '#f1c40f' : '#bdc3c7';
                    ctx.lineWidth = i === this.highlightedIndex ? 3 : 1;
                    ctx.strokeRect(x, y, cellWidth, cellHeight);
                    
                    // 绘制链表
                    const chain = this.data[i];
                    let chainY = y + cellHeight + 20;
                    
                    if (chain.length > 0) {
                        // 绘制链表节点
                        for (let j = 0; j < chain.length; j++) {
                            const nodeX = x + cellWidth / 2 - 35;
                            const nodeY = chainY;
                            
                            // 高亮当前节点
                            const isHighlighted = i === this.highlightedIndex && 
                                                this.highlightedChain.includes(j);
                            
                            // 绘制节点
                            ctx.fillStyle = isHighlighted ? '#2ecc71' : '#f8f9fa';
                            ctx.fillRect(nodeX, nodeY, 70, 40);
                            
                            ctx.strokeStyle = isHighlighted ? '#27ae60' : '#1abc9c';
                            ctx.lineWidth = isHighlighted ? 3 : 1;
                            ctx.strokeRect(nodeX, nodeY, 70, 40);
                            
                            // 绘制键值对
                            ctx.fillStyle = '#e74c3c';
                            ctx.font = '12px Arial';
                            ctx.textAlign = '
<!--检测到代码截断，自动续写中...-->
'left';
                            ctx.fillText(`${chain[j].key}:`, nodeX + 5, nodeY + 15);
                            
                            ctx.fillStyle = '#f39c12';
                            ctx.fillText(chain[j].value, nodeX + 5, nodeY + 30);
                            
                            // 绘制链表连接线（如果不是最后一个节点）
                            if (j < chain.length - 1) {
                                ctx.beginPath();
                                ctx.moveTo(nodeX + 35, nodeY + 40);
                                ctx.lineTo(nodeX + 35, nodeY + 60);
                                ctx.strokeStyle = '#1abc9c';
                                ctx.lineWidth = 2;
                                ctx.stroke();
                                
                                // 绘制箭头
                                ctx.beginPath();
                                ctx.moveTo(nodeX + 35, nodeY + 60);
                                ctx.lineTo(nodeX + 30, nodeY + 55);
                                ctx.lineTo(nodeX + 40, nodeY + 55);
                                ctx.closePath();
                                ctx.fillStyle = '#1abc9c';
                                ctx.fill();
                            }
                            
                            chainY += 60;
                        }
                    } else {
                        // 绘制空链表指示
                        ctx.fillStyle = '#bdc3c7';
                        ctx.font = '12px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('空', x + cellWidth / 2, y + cellHeight / 2 + 5);
                    }
                }
                
                // 绘制当前高亮元素（如果有）
                if (this.highlightedElement && this.animationState !== 'idle') {
                    ctx.fillStyle = 'rgba(46, 204, 113, 0.8)';
                    ctx.font = 'bold 14px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText(
                        `当前: ${this.highlightedElement.key}:${this.highlightedElement.value}`,
                        tableWidth / 2,
                        tableHeight - 20
                    );
                }
            }
            
            drawAddressingTable() {
                const ctx = this.ctx;
                const tableWidth = this.canvas.width;
                const tableHeight = this.canvas.height;
                const cellWidth = 100;
                const cellHeight = 80;
                const startX = (tableWidth - this.tableSize * cellWidth) / 2;
                const startY = 80;
                
                // 绘制标题
                ctx.fillStyle = '#2c3e50';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('开放定址法哈希表（线性探测）', tableWidth / 2, 30);
                
                // 绘制表头
                ctx.fillStyle = '#3498db';
                ctx.font = '14px Arial';
                for (let i = 0; i < this.tableSize; i++) {
                    const x = startX + i * cellWidth + cellWidth / 2;
                    const y = startY - 30;
                    
                    ctx.fillText(`索引 ${i}`, x, y);
                }
                
                // 绘制探测路径（如果有）
                if (this.highlightedProbes && this.highlightedProbes.length > 0) {
                    ctx.strokeStyle = 'rgba(155, 89, 182, 0.5)';
                    ctx.lineWidth = 3;
                    ctx.setLineDash([5, 5]);
                    
                    for (let i = 0; i < this.highlightedProbes.length - 1; i++) {
                        const fromIndex = this.highlightedProbes[i];
                        const toIndex = this.highlightedProbes[i + 1];
                        
                        const fromX = startX + fromIndex * cellWidth + cellWidth / 2;
                        const fromY = startY + cellHeight / 2;
                        const toX = startX + toIndex * cellWidth + cellWidth / 2;
                        const toY = startY + cellHeight / 2;
                        
                        ctx.beginPath();
                        ctx.moveTo(fromX, fromY);
                        
                        // 绘制曲线路径
                        const midY = fromY - 40;
                        ctx.quadraticCurveTo((fromX + toX) / 2, midY, toX, toY);
                        ctx.stroke();
                        
                        // 绘制箭头
                        const angle = Math.atan2(toY - midY, toX - (fromX + toX) / 2);
                        ctx.setLineDash([]);
                        ctx.beginPath();
                        ctx.moveTo(toX, toY);
                        ctx.lineTo(
                            toX - 10 * Math.cos(angle - Math.PI / 6),
                            toY - 10 * Math.sin(angle - Math.PI / 6)
                        );
                        ctx.lineTo(
                            toX - 10 * Math.cos(angle + Math.PI / 6),
                            toY - 10 * Math.sin(angle + Math.PI / 6)
                        );
                        ctx.closePath();
                        ctx.fillStyle = '#9b59b6';
                        ctx.fill();
                        ctx.setLineDash([5, 5]);
                    }
                    
                    ctx.setLineDash([]);
                }
                
                // 绘制哈希表单元格
                for (let i = 0; i < this.tableSize; i++) {
                    const x = startX + i * cellWidth;
                    const y = startY;
                    
                    // 确定单元格颜色
                    let cellColor = '#f8f9fa';
                    let borderColor = '#bdc3c7';
                    let lineWidth = 1;
                    
                    if (i === this.highlightedIndex) {
                        cellColor = 'rgba(241, 196, 15, 0.3)';
                        borderColor = '#f1c40f';
                        lineWidth = 3;
                    } else if (this.highlightedProbes && this.highlightedProbes.includes(i)) {
                        cellColor = 'rgba(155, 89, 182, 0.2)';
                        borderColor = '#9b59b6';
                        lineWidth = 2;
                    }
                    
                    // 绘制单元格背景
                    ctx.fillStyle = cellColor;
                    ctx.fillRect(x, y, cellWidth, cellHeight);
                    
                    // 绘制单元格边框
                    ctx.strokeStyle = borderColor;
                    ctx.lineWidth = lineWidth;
                    ctx.strokeRect(x, y, cellWidth, cellHeight);
                    
                    // 绘制单元格内容
                    const cellData = this.data[i];
                    
                    if (cellData === null) {
                        // 空单元格
                        ctx.fillStyle = '#bdc3c7';
                        ctx.font = '14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('空', x + cellWidth / 2, y + cellHeight / 2 + 5);
                    } else if (cellData === 'DELETED') {
                        // 已删除标记
                        ctx.fillStyle = '#eaa4a4';
                        ctx.font = '14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('已删除', x + cellWidth / 2, y + cellHeight / 2 + 5);
                    } else {
                        // 有数据的单元格
                        // 绘制键
                        ctx.fillStyle = '#e74c3c';
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(cellData.key, x + cellWidth / 2, y + cellHeight / 2 - 10);
                        
                        // 绘制值
                        ctx.fillStyle = '#f39c12';
                        ctx.font = '14px Arial';
                        ctx.fillText(cellData.value, x + cellWidth / 2, y + cellHeight / 2 + 15);
                        
                        // 绘制哈希值（小字）
                        ctx.fillStyle = '#7f8c8d';
                        ctx.font = '10px Arial';
                        ctx.fillText(`h=${cellData.hashIndex}`, x + cellWidth / 2, y + cellHeight - 10);
                    }
                }
                
                // 绘制当前高亮元素（如果有）
                if (this.highlightedElement && this.animationState !== 'idle') {
                    ctx.fillStyle = 'rgba(46, 204, 113, 0.8)';
                    ctx.font = 'bold 14px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText(
                        `当前: ${this.highlightedElement.key}:${this.highlightedElement.value}`,
                        tableWidth / 2,
                        tableHeight - 20
                    );
                }
            }
        }

        // 全局变量
        let chainingTable, addressingTable;
        let currentOperation = null;
        let currentKey = '';
        let currentValue = '';
        let isPlaying = false;

        // DOM 元素
        const keyInput = document.getElementById('keyInput');
        const valueInput = document.getElementById('valueInput');
        const insertBtn = document.getElementById('insertBtn');
        const searchBtn = document.getElementById('searchBtn');
        const deleteBtn = document.getElementById('deleteBtn');
        const clearBtn = document.getElementById('clearBtn');
        const stepBtn = document.getElementById('stepBtn');
        const playBtn = document.getElementById('playBtn');
        const pauseBtn = document.getElementById('pauseBtn');
        const resetBtn = document.getElementById('resetBtn');
        const tableSizeInput = document.getElementById('tableSize');
        const applySizeBtn = document.getElementById('applySizeBtn');
        const presetButtons = document.querySelectorAll('.preset-btn');
        const statusBar = document.getElementById('statusBar');
        const explanationText = document.getElementById('explanationText');

        // 统计元素
        const chainingCount = document.getElementById('chainingCount');
        const chainingConflicts = document.getElementById('chainingConflicts');
        const chainingMaxChain = document.getElementById('chainingMaxChain');
        const chainingASL = document.getElementById('chainingASL');
        const addressingCount = document.getElementById('addressingCount');
        const addressingConflicts = document.getElementById('addressingConflicts');
        const addressingProbes = document.getElementById('addressingProbes');
        const addressingASL = document.getElementById('addressingASL');
        const chainingSize = document.getElementById('chainingSize');
        const addressingSize = document.getElementById('addressingSize');

        // 初始化函数
        function init() {
            const tableSize = parseInt(tableSizeInput.value);
            
            chainingTable = new HashTableAnimation('chainingCanvas', 'chaining');
            addressingTable = new HashTableAnimation('addressingCanvas', 'addressing');
            
            chainingTable.tableSize = tableSize;
            addressingTable.tableSize = tableSize;
            chainingTable.initTable();
            addressingTable.initTable();
            
            chainingSize.textContent = tableSize;
            addressingSize.textContent = tableSize;
            
            updateStats();
            drawTables();
            
            // 设置初始说明
            explanationText.innerHTML = `
                <strong>拉链法</strong>：每个哈希桶是一个链表，冲突元素被添加到链表中。<br>
                <strong>开放定址法</strong>：所有元素都存储在数组中，冲突时通过探测序列寻找下一个空闲位置。<br>
                <strong>线性探测</strong>：探测序列为 h(key), h(key)+1, h(key)+2, ... 模表大小。
            `;
        }

        // 绘制两个表格
        function drawTables() {
            chainingTable.draw();
            addressingTable.draw();
        }

        // 更新统计信息
        function updateStats() {
            const chainingStats = chainingTable.getStats();
            const addressingStats = addressingTable.getStats();
            
            chainingCount.textContent = chainingStats.elementCount;
            chainingConflicts.textContent = chainingStats.conflictCount;
            chainingMaxChain.textContent = chainingStats.maxChainLength;
            chainingASL.textContent = chainingStats.asl;
            
            addressingCount.textContent = addressingStats.elementCount;
            addressingConflicts.textContent = addressingStats.conflictCount;
            addressingProbes.textContent = addressingStats.totalProbes;
            addressingASL.textContent = addressingStats.asl;
        }

        // 更新状态栏
        function updateStatus(message, method) {
            let methodText = method === 'chaining' ? '拉链法' : '开放定址法';
            statusBar.textContent = `${methodText}: ${message}`;
            statusBar.style.borderLeftColor = method === 'chaining' ? '#1abc9c' : '#9b59b6';
        }

        // 执行操作
        function performOperation(operation) {
            currentKey = keyInput.value.trim();
            currentValue = valueInput.value.trim();
            
            if (operation === 'insert' && (!currentKey || !currentValue)) {
                statusBar.textContent = '请输入键和值进行插入操作';
                statusBar.style.borderLeftColor = '#e74c3c';
                return;
            }
            
            if ((operation === 'search' || operation === 'delete') && !currentKey) {
                statusBar.textContent = '请输入键进行查找或删除操作';
                statusBar.style.borderLeftColor = '#e74c3c';
                return;
            }
            
            currentOperation = operation;
            
            if (operation === 'insert') {
                // 同时执行插入，但分别动画
                const chainingResult = chainingTable.insert(currentKey, currentValue, true);
                const addressingResult = addressingTable.insert(currentKey, currentValue, true);
                
                if (!addressingResult.success) {
                    updateStatus(`开放定址法: 哈希表已满，无法插入 "${currentKey}"`, 'addressing');
                } else {
                    updateStatus(`插入 "${currentKey}:${currentValue}"`, 'chaining');
                }
                
                // 更新说明
                explanationText.innerHTML = `
                    <strong>插入操作完成</strong><br>
                    • 拉链法: ${chainingResult.conflict ? '发生冲突，元素添加到链表' : '直接插入'}。<br>
                    • 开放定址法: ${addressingResult.conflict ? '发生冲突，使用线性探测找到空闲位置' : '直接插入'}。
                `;
            } else if (operation === 'search') {
                chainingTable.search(currentKey, true);
                addressingTable.search(currentKey, true);
                updateStatus(`查找键 "${currentKey}"`, 'chaining');
                
                explanationText.innerHTML = `
                    <strong>查找操作</strong><br>
                    • 拉链法: 计算哈希值，在对应链表中线性查找。<br>
                    • 开放定址法: 计算哈希值，沿探测序列查找直到找到键或遇到空位置。
                `;
            } else if (operation === 'delete') {
                chainingTable.delete(currentKey, true);
                addressingTable.delete(currentKey, true);
                updateStatus(`删除键 "${currentKey}"`, 'chaining');
                
                explanationText.innerHTML = `
                    <strong>删除操作</strong><br>
                    • 拉链法: 从链表中直接删除节点。<br>
                    • 开放定址法: 标记为"已删除"，避免破坏探测序列。
                `;
            }
            
            updateStats();
            drawTables();
        }

        // 事件监听器
        insertBtn.addEventListener('click', () => {
            if (isPlaying) return;
            performOperation('insert');
        });

        searchBtn.addEventListener('click', () => {
            if (isPlaying) return;
            performOperation('search');
        });

        deleteBtn.addEventListener('click', () => {
            if (isPlaying) return;
            performOperation('delete');
        });

        clearBtn.addEventListener('click', () => {
            if (isPlaying) return;
            chainingTable.initTable();
            addressingTable.initTable();
            updateStats();
            drawTables();
            statusBar.textContent = '哈希表已清空';
            statusBar.style.borderLeftColor = '#3498db';
            explanationText.innerHTML = `
                <strong>哈希表已重置</strong><br>
                两个哈希表都已清空，可以重新开始插入数据。
            `;
        });

        stepBtn.addEventListener('click', () => {
            if (isPlaying) return;
            
            if (chainingTable.steps.length > 0 && chainingTable.currentStep < chainingTable.steps.length) {
                chainingTable.stepForward();
            }
            
            if (addressingTable.steps.length > 0 && addressingTable.currentStep < addressingTable.steps.length) {
                addressingTable.stepForward();
            }
            
            drawTables();
            
            // 如果两个动画都结束了
            if (chainingTable.currentStep >= chainingTable.steps.length && 
                addressingTable.currentStep >= addressingTable.steps.length) {
                statusBar.textContent = '单步执行完成';
                statusBar.style.borderLeftColor = '#3498db';
            }
        });

        playBtn.addEventListener('click', () => {
            if (isPlaying) return;
            
            isPlaying = true;
            playBtn.disabled = true;
            pauseBtn.disabled = false;
            stepBtn.disabled = true;
            
            chainingTable.startAnimation();
            addressingTable.startAnimation();
            
            statusBar.textContent = '动画播放中...';
            statusBar.style.borderLeftColor = '#f1c40f';
        });

        pauseBtn.addEventListener('click', () => {
            if (!isPlaying) return;
            
            isPlaying = false;
            playBtn.disabled = false;
            pauseBtn.disabled = true;
            stepBtn.disabled = false;
            
            chainingTable.stopAnimation();
            addressingTable.stopAnimation();
            
            statusBar.textContent = '动画已暂停';
            statusBar.style.borderLeftColor = '#f39c12';
        });

        resetBtn.addEventListener('click', () => {
            chainingTable.stopAnimation();
            addressingTable.stopAnimation();
            
            chainingTable.currentStep = 0;
            addressingTable.currentStep = 0;
            chainingTable.steps = [];
            addressingTable.steps = [];
            chainingTable.highlightedIndex = -1;
            addressingTable.highlightedIndex = -1;
            chainingTable.highlightedElement = null;
            addressingTable.highlightedElement = null;
            chainingTable.highlightedChain = [];
            addressingTable.highlightedProbes = [];
            
            isPlaying = false;
            playBtn.disabled = false;
            pauseBtn.disabled = true;
            stepBtn.disabled = false;
            
            drawTables();
            statusBar.textContent = '动画已重置';
            statusBar.style.borderLeftColor = '#3498db';
        });

        applySizeBtn.addEventListener('click', () => {
            if (isPlaying) return;
            
            const newSize = parseInt(tableSizeInput.value);
            if (newSize < 5 || newSize > 15) {
                alert('表大小必须在5到15之间');
                return;
            }
            
            chainingTable.resize(newSize);
            addressingTable.resize(newSize);
            
            chainingSize.textContent = newSize;
            addressingSize.textContent = newSize;
            
            updateStats();
            drawTables();
            
            statusBar.textContent = `哈希表大小已更改为 ${newSize}`;
            statusBar.style.borderLeftColor = '#3498db';
        });

        // 预设数据集
        const presetData = {
            simple: [
                {key: 'apple', value: 10},
                {key: 'banana', value: 20},
                {key: 'cherry', value: 30},
                {key: 'date', value: 40}
            ],
            conflict: [
                {key: 'abc', value: 1},  // 哈希值可能相同
                {key: 'acb', value: 2},
                {key: 'bac', value: 3},
                {key: 'bca', value: 4},
                {key: 'cab', value: 5},
                {key: 'cba', value: 6}
            ],
            numbers: [
                {key: 'one', value: 1},
                {key: 'two', value: 2},
                {key: 'three', value: 3},
                {key: 'four', value: 4},
                {key: 'five', value: 5},
                {key: 'six', value: 6},
                {key: 'seven', value: 7}
            ]
        };

        presetButtons.forEach(btn => {
            btn.addEventListener('click', () => {
                if (isPlaying) return;
                
                const preset = btn.dataset.preset;
                const data = presetData[preset];
                
                // 清空当前表
                chainingTable.initTable();
                addressingTable.initTable();
                
                // 插入预设数据
                data.forEach(item => {
                    chainingTable.insert(item.key, item.value, false);
                    addressingTable.insert(item.key, item.value, false);
                });
                
                updateStats();
                drawTables();
                
                statusBar.textContent = `已加载"${preset}"预设数据集，包含 ${data.length} 个元素`;
                statusBar.style.borderLeftColor = '#3498db';
                
                explanationText.innerHTML = `
                    <strong>预设数据集 "${preset}" 已加载</strong><br>
                    • 包含 ${data.length} 个键值对。<br>
                    • 观察两种方法如何处理这些数据。<br>
                    • 尝试执行查找和删除操作。
                `;
            });
        });

        // 键盘快捷键
        document.addEventListener('keydown', (e) => {
            if (e.target.tagName === 'INPUT') return;
            
            if (e.key === 'Enter' && keyInput.value && valueInput.value) {
                performOperation('insert');
            } else if (e.key === 's' || e.key === 'S') {
                stepBtn.click();
            } else if (e.key === 'p' || e.key === 'P') {
                if (isPlaying) {
                    pauseBtn.click();
                } else {
                    playBtn.click();
                }
            } else if (e.key === 'r' || e.key === 'R') {
                resetBtn.click();
            }
        });

        // 初始化应用
        window.addEventListener('load', init);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

欢迎使用“哈希表冲突解决教学动画”！本工具旨在通过直观、动态的可视化方式，帮助您深入理解哈希表的核心概念以及两种主流冲突解决方法——拉链法和开放定址法。请跟随本指南，开启您的探索学习之旅。

### 一、 功能说明

本动画是一个基于HTML5 Canvas构建的交互式教学工具。它将抽象的哈希表算法转化为可视化的图形操作，允许您通过插入、查找、删除数据，并实时观察拉链法（Separate Chaining）与开放定址法（Open Addressing，采用线性探测）两种策略在处理相同数据时的不同表现。所有操作均伴有分步动画和文字说明，旨在降低学习门槛，提升理解深度。

### 二、 主要功能

1.  **核心操作模拟**
    *   **插入**：输入键值对，观察元素如何根据哈希函数定位，以及发生冲突时两种方法的处理流程。
    *   **查找**：输入键，高亮显示在两种哈希表中的查找路径，直观对比查找效率。
    *   **删除**：演示两种方法删除元素的差异，特别是开放定址法中“已删除”标记的作用。

2.  **动画与流程控制**
    *   **单步执行**：将算法分解为计算哈希、检查位置、解决冲突等步骤，逐步执行，适合精细学习。
    *   **连续播放**：自动播放完整的操作动画，适合观察整体流程。
    *   **暂停/重置**：随时控制动画节奏，或清空状态重新开始。

3.  **数据与参数管理**
    *   **自定义数据**：自由输入任意键值对进行测试。
    *   **预设数据集**：提供“简单数据”、“易冲突数据”、“数字数据”三组预设，一键加载，快速体验不同场景。
    *   **动态调整哈希表大小**：可实时修改哈希表数组的大小（5-15），观察负载因子变化对性能的影响。

4.  **信息与统计面板**
    *   **实时状态提示**：顶部状态栏实时显示当前操作步骤的详细说明。
    *   **对比统计**：左右两侧独立显示两种方法的统计数据，包括元素数量、冲突次数、最长链表（拉链法）、总探测次数（开放定址法）和平均查找长度（ASL）。
    *   **视觉图例**：提供颜色编码说明，确保您理解每种颜色代表的元素或状态。

### 三、 设计特色

1.  **双视图对比学习**：界面采用并排设计，左侧展示拉链法，右侧展示开放定址法。相同的操作会同时在两个视图中执行，让差异一目了然。
2.  **丰富的视觉编码**：
    *   **颜色**：键（红）、值（橙）、当前活动元素（绿）、哈希计算位置（黄）、空位（灰）、已删除标记（浅红）。
    *   **动态效果**：元素移动、链表延伸、探测路径（虚线箭头）等，使算法过程生动形象。
3.  **遵循认知规律**：从简单操作到复杂冲突，从单步分解到连续播放，设计符合“从易到难、从分解到综合”的学习路径。
4.  **即时反馈与说明**：每一步操作都有对应的文字解释出现在状态栏和说明区域，将视觉动画与概念描述紧密结合，巩固学习效果。

### 四、 教学要点

通过本动画，您可以重点观察和理解以下核心知识点：

1.  **哈希冲突的必然性**：使用“易冲突数据”预设，直观感受不同键映射到同一哈希值的过程。
2.  **拉链法的本质**：观察哈希表每个桶如何成为一个链表（或其它容器），冲突元素如何被“链”在一起。注意查找时需要遍历链表。
3.  **开放定址法（线性探测）的寻址逻辑**：观察元素如何像“停车找位”一样，在发生冲突时顺序寻找下一个空闲位置。特别关注“聚集”现象的形成。
4.  **删除操作的关键差异**：
    *   拉链法：直接从链表中移除节点，简单直接。
    *   开放定址法：不能简单置空，而需标记为“已删除”，以保障后续查找操作的正确性。这是学习中的一个难点，动画提供了清晰演示。
5.  **性能影响因素**：通过调整哈希表大小，插入大量数据，观察统计信息（特别是冲突次数和平均查找长度ASL）的变化，理解**负载因子**对哈希表性能的核心影响。

### 五、 使用建议

1.  **新手入门路径**：
    *   第一步：选择“简单数据”预设，点击“插入”或“连续播放”，先观察无冲突情况下的理想插入过程。
    *   第二步：选择“易冲突数据”预设，使用“单步执行”模式，仔细跟随每一步，理解冲突如何产生与解决。
    *   第三步：尝试“查找”和“删除”操作，对比两种方法在路径上的差异。

2.  **深度探究建议**：
    *   **设计实验**：自定义一组有大量冲突的键（如“abc”，“acb”，“bac”等），比较两种方法在插入所有这些键后，哈希表的形态和统计数据的差异。
    *   **参数调优**：固定一组数据，分别用小（如5）和大（如15）的哈希表大小插入，对比冲突次数和平均查找长度的变化，直观理解空间换时间的权衡。
    *   **预测与验证**：在操作前，先根据哈希函数心算键的哈希值，预测它会被插入哪个位置，然后用动画验证你的预测。

3.  **教学辅助提示**：
    *   **教师**：可在讲解概念时，同步演示此动画。利用“单步执行”分解复杂步骤，利用“预设数据”快速切换场景。引导学生根据统计数据分析算法优劣。
    *   **学生**：将动画作为预习和复习工具。在编写代码实现哈希表之前，先用动画彻底理解数据结构和算法流程。遇到疑惑时，通过动画反复观察相关操作。

我们相信，通过亲手操作和直观观察，哈希表及其冲突解决机制将不再抽象。祝您学习愉快，探索顺利！