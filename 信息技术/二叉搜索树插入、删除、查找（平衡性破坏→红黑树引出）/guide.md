# 需求：二叉搜索树插入、删除、查找（平衡性破坏→红黑树引出）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为计算机科学或相关专业的学生，已经具备二叉树的基础知识，正在学习更高级的数据结构（二叉搜索树BST及其平衡化）。他们需要直观地理解BST的动态操作过程及其局限性。
2.  **核心痛点**：
    *   **抽象过程可视化**：BST的插入、删除、查找是动态的、分步骤的算法，仅靠静态图示或伪代码难以理解指针调整和树形结构的变化。
    *   **理解平衡性的重要性**：需要清晰地展示，在连续插入有序数据时，BST如何退化成链表，从而导致查找效率从O(log n)恶化到O(n)。这是引出平衡树（如红黑树）最直接的动机。
    *   **建立知识关联**：用户需要在“不平衡的BST”和“复杂的平衡树（红黑树）”之间建立一个平滑的认知桥梁。动画应自然地展示问题，并引出解决方案。
3.  **学习目标**：通过交互动画，用户应能：
    *   清晰地复述BST插入、查找、删除（特别是删除拥有两个子节点的节点）的步骤。
    *   直观地认识到BST可能失去平衡，并理解其对性能的影响。
    *   明确红黑树等平衡二叉搜索树被引入的目的——为了解决BST的不平衡问题。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

1.  **核心概念分解与串联**：
    *   **主线**：BST基本操作 → 操作导致不平衡（问题呈现）→ 需要保持平衡（解决方案引入）。
    *   **关键操作聚焦**：
        *   **插入**：比较、定位、挂载。
        *   **查找**：路径高亮、比较过程。
        *   **删除**：分三种情况（叶子节点、单子节点、双子节点），重点演示用“后继节点”替换并删除的经典策略。
        *   **平衡性破坏**：专门设计一个“连续插入有序序列”的演示模式，让树明显倾斜。

2.  **遵循认知规律**：
    *   **从具体到抽象**：先让用户手动操作单个节点，感受过程；再通过“自动演示”模式展示完整序列操作或退化过程。
    *   **分步与高亮**：任何操作都分解为清晰的步骤（如：1. 查找位置；2. 比较大小；3. 放置节点）。当前步骤的节点、指针、比较值用高亮和动画强调。
    *   **对比与强调**：将一棵平衡BST和一棵退化BST并排显示，并同时进行相同值的查找操作，用“步数计数器”或“路径动画速度”直观对比性能差异。

3.  **交互设计**：
    *   **双模式驱动**：
        *   **交互模式**：用户通过按钮或输入框插入/删除指定节点，完全控制流程。
        *   **演示模式**：用户输入一组数据（如`1,2,3,4,5`或随机数），动画自动按顺序执行插入，清晰展示退化过程。可暂停、继续、重置。
    *   **可控的节奏**：提供速度滑块控制动画快慢，允许用户逐步前进/后退。
    *   **即时的反馈**：在操作面板显示当前状态（如：“正在查找 35...”、“用后继节点 45 替换 40”）。对于错误操作（如插入重复值）给予提示。

4.  **视觉呈现**：
    *   **节点设计**：圆形节点，内部显示键值。用颜色和形状区分状态：
        *   普通节点：浅蓝色填充，深蓝色边框。
        *   **当前活动节点/被比较节点**：高亮黄色边框和填充。
        *   **查找路径**：已访问的节点变为浅灰色，当前路径线加粗。
        *   **待插入/被删除节点**：插入前/删除时用绿色/红色强调。
    *   **指针与动画**：指针（连线）在节点移动时具有平滑的绘制动画。节点的移动、添加、消失使用缓动动画，清晰易懂。
    *   **信息面板**：固定区域显示算法步骤说明、性能对比（平均查找长度ASL）、操作日志。
    *   **布局**：采用经典的树形拓扑布局，确保层级清晰，不交叉。当树倾斜时，布局算法能自适应，避免节点重叠。

#### 配色方案选择
*   **主色调**：采用科技蓝和中性灰，营造清晰、理性的学习氛围。
    *   背景/画布：`#f8f9fa` (浅灰白)
    *   树节点默认：`#4dabf7` (浅蓝) / 边框 `#339af0`
*   **功能色**：
    *   高亮/活动状态：`#ffd43b` (琥珀黄)
    *   插入/正确提示：`#69db7c` (柔和绿)
    *   删除/警告提示：`#ff6b6b` (柔和红)
    *   查找路径/已访问：`#dee2e6` (中灰色)
    *   文本/说明：`#495057` (深灰)
*   **对比与可访问性**：确保所有颜色组合有足够的对比度，色盲用户也能通过形状和动画区分状态。

#### 交互功能列表
1.  **数据输入与控制区**：
    *   数字输入框 + `插入` / `删除` / `查找` 按钮。
    *   `随机生成BST` 按钮（生成一棵随机键值的平衡树）。
    *   `序列演示` 输入框（可输入如“1,2,3,4,5”或“50,30,70,20,40”）+ `开始演示` 按钮。
    *   `重置` 按钮（清空整棵树）。

2.  **动画控制区**：
    *   `播放/暂停` 按钮（用于演示模式）。
    *   `上一步` / `下一步` 按钮（用于逐步查看任何操作）。
    *   `动画速度` 滑动条。

3.  **视图与模式选择区**：
    *   `对比视图` 开关：开启后，屏幕分为左右两半。左侧为当前交互的BST，右侧自动模拟一个在相同数据下**可能退化**的BST（或固定展示一个退化案例），进行并行的查找操作对比。
    *   `显示/隐藏` 开关：可切换显示节点键值、指针箭头、步数统计等。

4.  **信息显示区**：
    *   **算法步骤面板**：实时显示当前操作（插入、删除、查找）的详细文字描述。
    *   **性能指标面板**：显示当前树的节点数、高度、平均查找长度（ASL）估算。
    *   **操作历史面板**：记录用户的操作历史，并可点击回跳。

5.  **画布交互**：
    *   节点可点击（点击后，其键值自动填入输入框，方便后续对其进行删除或查找操作）。
    *   鼠标悬停在节点上时，显示该节点的子树高度信息（为理解不平衡性做铺垫）。

6.  **“引出红黑树”特别环节**：
    *   在演示模式中，当连续插入有序数据导致树高度急剧增加后，出现一个明显的`“!”`警告图标。
    *   点击该图标或一个`“如何解决？”`按钮，会在一侧或新面板中，用简化的动画展示红黑树通过旋转和变色如何保持大致平衡，并强调其`O(log n)`的稳定性能。此处仅为“引出”，不深入红黑树规则细节。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>二叉搜索树(BST)教学动画 - 插入、删除、查找与平衡性</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #f8f9fa;
            color: #495057;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1600px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #dee2e6;
        }

        h1 {
            color: #339af0;
            margin-bottom: 10px;
            font-size: 2.5rem;
        }

        .subtitle {
            color: #868e96;
            font-size: 1.1rem;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }

        .tree-section {
            flex: 1;
            min-width: 600px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.08);
            padding: 25px;
            display: flex;
            flex-direction: column;
        }

        .control-section {
            flex: 1;
            min-width: 400px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.08);
            padding: 25px;
            display: flex;
            flex-direction: column;
        }

        .section-title {
            font-size: 1.5rem;
            color: #495057;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e9ecef;
            display: flex;
            align-items: center;
        }

        .section-title i {
            margin-right: 10px;
            color: #4dabf7;
        }

        #treeCanvas {
            flex: 1;
            border: 1px solid #dee2e6;
            border-radius: 8px;
            background-color: #f8f9fa;
            cursor: pointer;
        }

        .control-panel {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 15px;
            margin-bottom: 25px;
        }

        .control-group {
            display: flex;
            flex-direction: column;
        }

        label {
            font-weight: 600;
            margin-bottom: 8px;
            color: #495057;
            font-size: 0.95rem;
        }

        input, select, button {
            padding: 12px 15px;
            border: 1px solid #ced4da;
            border-radius: 6px;
            font-size: 1rem;
            transition: all 0.2s;
        }

        input:focus, select:focus {
            outline: none;
            border-color: #4dabf7;
            box-shadow: 0 0 0 3px rgba(77, 171, 247, 0.1);
        }

        button {
            background-color: #4dabf7;
            color: white;
            border: none;
            cursor: pointer;
            font-weight: 600;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        button:hover {
            background-color: #339af0;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        button:active {
            transform: translateY(0);
        }

        .danger-btn {
            background-color: #ff6b6b;
        }

        .danger-btn:hover {
            background-color: #fa5252;
        }

        .success-btn {
            background-color: #69db7c;
        }

        .success-btn:hover {
            background-color: #51cf66;
        }

        .warning-btn {
            background-color: #ffd43b;
            color: #495057;
        }

        .warning-btn:hover {
            background-color: #fcc419;
        }

        .animation-controls {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 25px;
            padding: 15px;
            background-color: #f1f3f5;
            border-radius: 8px;
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            flex: 1;
        }

        .speed-slider {
            flex: 1;
        }

        .info-panels {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .info-panel {
            background: white;
            border-radius: 12px;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            overflow: hidden;
        }

        .info-panel h3 {
            color: #495057;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e9ecef;
            font-size: 1.2rem;
        }

        #algorithmSteps {
            height: 200px;
            overflow-y: auto;
            padding: 10px;
            background-color: #f8f9fa;
            border-radius: 6px;
            border: 1px solid #e9ecef;
            font-size: 0.95rem;
            line-height: 1.5;
        }

        .step-item {
            padding: 8px 12px;
            margin-bottom: 8px;
            border-radius: 4px;
            border-left: 4px solid #4dabf7;
            background-color: white;
            animation: fadeIn 0.3s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(5px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }

        .stat-item {
            text-align: center;
            padding: 15px;
            background-color: #f8f9fa;
            border-radius: 8px;
        }

        .stat-value {
            font-size: 1.8rem;
            font-weight: 700;
            color: #339af0;
            margin-bottom: 5px;
        }

        .stat-label {
            font-size: 0.9rem;
            color: #868e96;
        }

        .comparison-view {
            display: none;
            margin-top: 20px;
            padding: 15px;
            background-color: #fff3cd;
            border-radius: 8px;
            border-left: 4px solid #ffd43b;
        }

        .comparison-view.active {
            display: block;
            animation: slideDown 0.3s ease;
        }

        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .comparison-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .comparison-text {
            flex: 1;
        }

        .comparison-text h4 {
            color: #856404;
            margin-bottom: 5px;
        }

        .comparison-text p {
            color: #856404;
            font-size: 0.95rem;
        }

        .highlight {
            background-color: #ffd43b;
            padding: 2px 6px;
            border-radius: 4px;
            font-weight: 600;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding: 15px;
            background-color: #f8f9fa;
            border-radius: 8px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
        }

        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            border: 2px solid;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #dee2e6;
            color: #868e96;
            font-size: 0.9rem;
        }

        @media (max-width: 1200px) {
            .main-content {
                flex-direction: column;
            }
            
            .tree-section, .control-section {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>🌳 二叉搜索树(BST)教学动画</h1>
            <p class="subtitle">可视化插入、删除、查找操作 | 探索平衡性问题 | 引出红黑树解决方案</p>
        </header>

        <div class="main-content">
            <div class="tree-section">
                <h2 class="section-title"><i>📊</i> 二叉搜索树可视化</h2>
                <canvas id="treeCanvas" width="800" height="500"></canvas>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #4dabf7; border-color: #339af0;"></div>
                        <span>普通节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ffd43b; border-color: #fcc419;"></div>
                        <span>活动/比较节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #69db7c; border-color: #51cf66;"></div>
                        <span>插入节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff6b6b; border-color: #fa5252;"></div>
                        <span>删除节点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #dee2e6; border-color: #adb5bd;"></div>
                        <span>查找路径</span>
                    </div>
                </div>
            </div>

            <div class="control-section">
                <h2 class="section-title"><i>🎮</i> 交互控制面板</h2>
                
                <div class="control-panel">
                    <div class="control-group">
                        <label for="nodeValue">节点值 (1-99):</label>
                        <input type="number" id="nodeValue" min="1" max="99" value="50">
                    </div>
                    
                    <div class="control-group">
                        <label for="operation">选择操作:</label>
                        <select id="operation">
                            <option value="insert">插入节点</option>
                            <option value="delete">删除节点</option>
                            <option value="search">查找节点</option>
                        </select>
                    </div>
                    
                    <div class="control-group">
                        <label>&nbsp;</label>
                        <button id="executeBtn" class="success-btn">
                            <span>🚀 执行操作</span>
                        </button>
                    </div>
                    
                    <div class="control-group">
                        <label>&nbsp;</label>
                        <button id="randomTreeBtn" class="warning-btn">
                            <span>🎲 随机生成BST</span>
                        </button>
                    </div>
                </div>

                <div class="animation-controls">
                    <button id="prevStepBtn" title="上一步">◀</button>
                    <button id="playPauseBtn" title="播放/暂停">⏸️</button>
                    <button id="nextStepBtn" title="下一步">▶</button>
                    
                    <div class="speed-control">
                        <span>速度:</span>
                        <input type="range" id="speedSlider" class="speed-slider" min="1" max="10" value="5">
                        <span id="speedValue">中速</span>
                    </div>
                </div>

                <div class="control-panel">
                    <div class="control-group">
                        <label for="sequenceInput">序列演示 (逗号分隔):</label>
                        <input type="text" id="sequenceInput" placeholder="例如: 1,2,3,4,5 或 50,30,70,20,40" value="1,2,3,4,5">
                    </div>
                    
                    <div class="control-group">
                        <label>&nbsp;</label>
                        <button id="demoBtn" class="warning-btn">
                            <span>📽️ 开始序列演示</span>
                        </button>
                    </div>
                    
                    <div class="control-group">
                        <label>&nbsp;</label>
                        <button id="resetBtn" class="danger-btn">
                            <span>🗑️ 重置树</span>
                        </button>
                    </div>
                </div>

                <div class="comparison-view" id="comparisonView">
                    <div class="comparison-content">
                        <div class="comparison-text">
                            <h4>⚠️ 发现不平衡问题！</h4>
                            <p>当前BST已严重倾斜，查找效率从 <span class="highlight">O(log n)</span> 退化到 <span class="highlight">O(n)</span>！</p>
                            <p>红黑树等平衡二叉搜索树通过旋转和变色操作保持平衡，确保稳定的 <span class="highlight">O(log n)</span> 性能。</p>
                        </div>
                        <button id="learnMoreBtn" class="success-btn">了解更多 →</button>
                    </div>
                </div>
            </div>
        </div>

        <div class="info-panels">
            <div class="info-panel">
                <h3>📝 算法步骤</h3>
                <div id="algorithmSteps">
                    <div class="step-item">欢迎使用BST教学动画！请执行操作查看详细步骤。</div>
                </div>
            </div>
            
            <div class="info-panel">
                <h3>📊 树状统计</h3>
                <div class="stats-grid">
                    <div class="stat-item">
                        <div class="stat-value" id="nodeCount">0</div>
                        <div class="stat-label">节点总数</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value" id="treeHeight">0</div>
                        <div class="stat-label">树的高度</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value" id="avgSearchLength">0.0</div>
                        <div class="stat-label">平均查找长度</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value" id="balanceFactor">-</div>
                        <div class="stat-label">平衡状态</div>
                    </div>
                </div>
            </div>
        </div>

        <footer>
            <p>© 2023 数据结构教学动画 | 设计用于展示二叉搜索树操作与平衡性问题 | 引出红黑树解决方案</p>
        </footer>
    </div>

    <script>
        // ==================== 数据结构定义 ====================
        class TreeNode {
            constructor(value) {
                this.value = value;
                this.left = null;
                this.right = null;
                this.parent = null;
                this.x = 0;
                this.y = 0;
                this.radius = 25;
                this.state = 'normal'; // normal, active, visited, inserting, deleting
                this.highlight = false;
            }
        }

        class BST {
            constructor() {
                this.root = null;
                this.nodeCount = 0;
                this.animationQueue = [];
                this.isAnimating = false;
                this.currentStep = 0;
                this.speed = 5;
                this.operationHistory = [];
                this.lastSearchPath = [];
            }

            insert(value) {
                this.addToHistory(`开始插入节点 ${value}`);
                const newNode = new TreeNode(value);
                newNode.state = 'inserting';
                
                if (!this.root) {
                    this.root = newNode;
                    this.addToHistory(`树为空，将 ${value} 设为根节点`);
                    this.animationQueue.push({
                        type: 'insert',
                        node: newNode,
                        message: `插入 ${value} 作为根节点`
                    });
                } else {
                    this.addToHistory(`从根节点 ${this.root.value} 开始查找插入位置`);
                    this.animationQueue.push({
                        type: 'highlight',
                        node: this.root,
                        message: `比较 ${value} 与根节点 ${this.root.value}`
                    });
                    
                    let current = this.root;
                    let parent = null;
                    
                    while (current) {
                        parent = current;
                        this.animationQueue.push({
                            type: 'visit',
                            node: current,
                            message: `访问节点 ${current.value}`
                        });
                        
                        if (value < current.value) {
                            this.addToHistory(`${value} < ${current.value}，向左子树查找`);
                            if (current.left) {
                                this.animationQueue.push({
                                    type: 'highlight',
                                    node: current.left,
                                    message: `比较 ${value} 与左子节点 ${current.left.value}`
                                });
                                current = current.left;
                            } else {
                                current.left = newNode;
                                newNode.parent = current;
                                this.addToHistory(`找到空位，将 ${value} 插入为 ${current.value} 的左子节点`);
                                break;
                            }
                        } else if (value > current.value) {
                            this.addToHistory(`${value} > ${current.value}，向右子树查找`);
                            if (current.right) {
                                this.animationQueue.push({
                                    type: 'highlight',
                                    node: current.right,
                                    message: `比较 ${value} 与右子节点 ${current.right.value}`
                                });
                                current = current.right;
                            } else {
                                current.right = newNode;
                                newNode.parent = current;
                                this.addToHistory(`找到空位，将 ${value} 插入为 ${current.value} 的右子节点`);
                                break;
                            }
                        } else {
                            this.addToHistory(`节点 ${value} 已存在，插入失败`);
                            this.animationQueue.push({
                                type: 'error',
                                message: `节点 ${value} 已存在于树中`
                            });
                            return false;
                        }
                    }
                    
                    this.animationQueue.push({
                        type: 'insert',
                        node: newNode,
                        message: `成功插入节点 ${value}`
                    });
                }
                
                this.nodeCount++;
                this.updateStats();
                return true;
            }

            delete(value) {
                this.addToHistory(`开始删除节点 ${value}`);
                let nodeToDelete = this.root;
                let parent = null;
                
                // 查找要删除的节点
                while (nodeToDelete && nodeToDelete.value !== value) {
                    parent = nodeToDelete;
                    this.animationQueue.push({
                        type: 'highlight',
                        node: nodeToDelete,
                        message: `比较 ${value} 与节点 ${nodeToDelete.value}`
                    });
                    
                    if (value < nodeToDelete.value) {
                        this.addToHistory(`${value} < ${nodeToDelete.value}，向左子树查找`);
                        nodeToDelete = nodeToDelete.left;
                    } else {
                        this.addToHistory(`${value} > ${nodeToDelete.value}，向右子树查找`);
                        nodeToDelete = nodeToDelete.right;
                    }
                }
                
                if (!nodeToDelete) {
                    this.addToHistory(`节点 ${value} 不存在，删除失败`);
                    this.animationQueue.push({
                        type: 'error',
                        message: `节点 ${value} 不存在于树中`
                    });
                    return false;
                }
                
                this.animationQueue.push({
                    type: 'delete',
                    node: nodeToDelete,
                    message: `找到要删除的节点 ${value}`
                });
                
                // 情况1: 叶子节点
                if (!nodeToDelete.left && !nodeToDelete.right) {
                    this.addToHistory(`节点 ${value} 是叶子节点，直接删除`);
                    if (!parent) {
                        this.root = null;
                    } else if (parent.left === nodeToDelete) {
                        parent.left = null;
                    } else {
                        parent.right = null;
                    }
                }
                // 情况2: 只有一个子节点
                else if (!nodeToDelete.left || !nodeToDelete.right) {
                    const child = nodeToDelete.left || nodeToDelete.right;
                    this.addToHistory(`节点 ${value} 有一个子节点 ${child.value}，用子节点替换`);
                    
                    this.animationQueue.push({
                        type: 'highlight',
                        node: child,
                        message: `用子节点 ${child.value} 替换 ${value}`
                    });
                    
                    if (!parent) {
                        this.root = child;
                    } else if (parent.left === nodeToDelete) {
                        parent.left = child;
                    } else {
                        parent.right = child;
                    }
                    child.parent = parent;
                }
                // 情况3: 有两个子节点
                else {
                    this.addToHistory(`节点 ${value} 有两个子节点，查找后继节点`);
                    // 查找后继节点（右子树的最小值）
                    let successor = nodeToDelete.right;
                    let successorParent = nodeToDelete;
                    
                    this.animationQueue.push({
                        type: 'highlight',
                        node: successor,
                        message: `在右子树中查找 ${value} 的后继节点`
                    });
                    
                    while (successor.left) {
                        successorParent = successor;
                        successor = successor.left;
                        this.animationQueue.push({
                            type: 'highlight',
                            node: successor,
                            message: `继续向左查找更小的值`
                        });
                    }
                    
                    this.addToHistory(`找到后继节点 ${successor.value}`);
                    this.animationQueue.push({
                        type: 'highlight',
                        node: successor,
                        message: `后继节点是 ${successor.value}`
                    });
                    
                    // 用后继节点的值替换要删除的节点
                    const successorValue = successor.value;
                    this.addToHistory(`用后继节点 ${successorValue} 替换 ${value}`);
                    
                    // 删除后继节点（后继节点最多有一个右子节点）
                    if (successorParent.left === successor) {
                        successorParent.left = successor.right;
                    } else {
                        successorParent.right = successor.right;
                    }
                    
                    if (successor.right) {
                        successor.right.parent = successorParent;
                    }
                    
                    // 更新要删除的节点的值
                    nodeToDelete.value = successorValue;
                    this.animationQueue.push({
                        type: 'update',
                        node: nodeToDelete,
                        message: `节点值更新为 ${successorValue}`
                    });
                }
                
                this.nodeCount--;
                this.updateStats();
                return true;
            }

            search(value) {
                this.addToHistory(`开始查找节点 ${value}`);
                this.lastSearchPath = [];
                let current = this.root;
                let steps = 0;
                
                while (current) {
                    steps++;
                    this.lastSearchPath.push(current);
                    this.animationQueue.push({
                        type: 'highlight',
                        node: current,
                        message: `第${steps}步: 比较 ${value} 与节点 ${current.value}`
                    });
                    
                    if (value === current.value) {
                        this.addToHistory(`找到节点 ${value}，共查找 ${steps} 步`);
                        this.animationQueue.push({
                            type: 'found',
                            node: current,
                            message: `成功找到节点 ${value}`
                        });
                        return { found: true, steps };
                    } else if (value < current.value) {
                        this.addToHistory(`${value} < ${current.value}，向左子树查找`);
                        current = current.left;
                    } else {
                        this.addToHistory(`${value} > ${current.value}，向右子树查找`);
                        current = current.right;
                    }
                }
                
                this.addToHistory(`节点 ${value} 不存在于树中`);
                this.animationQueue.push({
                    type: 'notFound',
                    message: `节点 ${value} 不存在`
                });
                return { found: false, steps };
            }

            addToHistory(message) {
                this.operationHistory.push(message);
                if (this.operationHistory.length > 50) {
                    this.operationHistory.shift();
                }
                updateAlgorithmSteps(message);
            }

            updateStats() {
                const height = this.getHeight(this.root);
                const avgSearchLength = this.calculateASL(this.root);
                const balanceStatus = this.checkBalance(this.root);
                
                document.getElementById('nodeCount').textContent = this.nodeCount;
                document.getElementById('treeHeight').textContent = height;
                document.getElementById('avgSearchLength').textContent = avgSearchLength.toFixed(2);
                document.getElementById('balanceFactor').textContent = balanceStatus;
                
                // 检查是否需要显示不平衡警告
                if (height > Math.log2(this.nodeCount + 1) * 2 && this.nodeCount > 5) {
                    document.getElementById('comparisonView').classList.add('active');
                }
            }

            getHeight(node) {
                if (!node) return 0;
                return 1 + Math.max(this.getHeight(node.left), this.getHeight(node.right));
            }

            calculateASL(node, depth = 1) {
                if (!node) return 0;
                return depth + this.calculateASL(node.left, depth + 1) + this.calculateASL(node.right, depth + 1);
            }

            checkBalance(node) {
                if (!node) return '平衡';
                
                const leftHeight = this.getHeight(node.left);
                const rightHeight = this.getHeight(node.right);
                
                if (Math.abs(leftHeight - rightHeight) > 1) {
                    return '不平衡';
                }
                
                const leftBalance = this.checkBalance(node.left);
                const rightBalance = this.checkBalance(node.right);
                
                return leftBalance === '平衡' && rightBalance === '平衡' ? '平衡' : '不平衡';
            }

            clearAnimationQueue() {
                this.animationQueue = [];
                this.currentStep = 0;
            }

            async playAnimation() {
                if (this.isAnimating || this.animationQueue.length === 0) return;
                
                this.isAnimating = true;
                document.getElementById('playPauseBtn').textContent = '⏸️';
                
                while (this.currentStep < this.animationQueue.length && this.isAnimating) {
                    const step = this.animationQueue[this.currentStep];
                    await this.executeAnimationStep(step);
                    this.currentStep++;
                    
                    // 根据速度调整延迟
                    const delay = 1100 - (this.speed * 100);
                    await new Promise(resolve => setTimeout(resolve, delay));
                }
                
                this.isAnimating = false;
                document.getElementById('playPauseBtn').textContent = '▶️';
            }

            async executeAnimationStep(step) {
                switch (step.type) {
                    case 'highlight':
                        step.node.state = 'active';
                        step.node.highlight = true;
                        updateAlgorithmSteps(step.message);
                        await this.drawTree();
                        step.node.state = 'normal';
                        step.node.highlight = false;
                        break;
                        
                    case 'visit':
                        step.node.state = 'visited';
                        updateAlgorithmSteps(step.message);
                        await this.drawTree();
                        step.node.state = 'normal';
                        break;
                        
                    case 'insert':
                        step.node.state = 'inserting';
                        updateAlgorithmSteps(step.message);
                        await this.drawTree();
                        step.node.state = 'normal';
                        break;
                        
                    case 'delete':
                        step.node.state = 'deleting';
                        updateAlgorithmSteps(step.message);
                        await this.drawTree();
                        // 节点将在下一帧被移除
                        break;
                        
                    case 'update':
                        step.node.highlight = true;
                        updateAlgorithmSteps(step.message);
                        await this.drawTree();
                        step.node.highlight = false;
                        break;
                        
                    case 'found':
                        step.node.state = 'active';
                        updateAlgorithmSteps(step.message);
                        await this.drawTree();
                        step.node.state = 'normal';
                        break;
                        
                    case 'notFound':
                    case 'error':
                        updateAlgorithmSteps(step.message);
                        break;
                }
            }

            async drawTree() {
                const canvas = document.getElementById('treeCanvas');
                const ctx = canvas.getContext('2d');
                
                // 清除画布
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                
                // 计算布局
                this.calculatePositions(this.root, canvas.width / 2, 80, canvas.width / 4);
                
                // 绘制连接线
                this.drawConnections(ctx, this.root);
                
                // 绘制节点
                this.drawNodes(ctx, this.root);
            }

            calculatePositions(node, x, y, offsetX) {
                if (!node) return;
                
                node.x = x;
                node.y = y;
                
                if (node.left) {
                    this.calculatePositions(node.left, x - offsetX, y + 80, offsetX / 1.8);
                }
                if (node.right) {
                    this.calculatePositions(node.right, x + offsetX, y + 80, offsetX / 1.8);
                }
            }

            drawConnections(ctx, node) {
                if (!node) return;
                
                // 绘制到左子节点的连接线
                if (node.left) {
                    ctx.beginPath();
                    ctx.moveTo(node.x, node.y + node.radius);
                    ctx.lineTo(node.left.x, node.left.y - node.left.radius);
                    ctx.strokeStyle = '#adb5bd';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    this.drawConnections(ctx, node.left);
                }
                
                // 绘制到右子节点的连接线
                if (node.right) {
                    ctx.beginPath();
                    ctx.moveTo(node.x, node.y + node.radius);
                    ctx.lineTo(node.right.x, node.right.y - node.right.radius);
                    ctx.strokeStyle = '#adb5bd';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    this.drawConnections(ctx, node.right);
                }
            }

            drawNodes(ctx, node) {
                if (!node) return;
                
                // 绘制节点
                ctx.beginPath();
                ctx.arc(node.x, node.y, node.radius, 0, Math.PI * 2);
                
                // 根据节点状态设置颜色
                switch (node.state) {
                    case 'active':
                        ctx.fillStyle = '#ffd43b';
                        ctx.strokeStyle = '#fcc419';
                        break;
                    case 'visited':
                        ctx.fillStyle = '#dee2e6';
                        ctx.strokeStyle = '#adb5bd';
                        break;
                    case 'inserting':
                        ctx.fillStyle = '#69db7c';
                        ctx.strokeStyle = '#51cf66';
                        break;
                    case 'deleting':
                        ctx.fillStyle = '#ff6b6b';
                        ctx.strokeStyle = '#fa5252';
                        break;
                    default:
                        ctx.fillStyle = '#4dabf7';
                        ctx.strokeStyle = '#339af0';
                }
                
                if (node.highlight) {
                    ctx.strokeStyle = '#ff6b6b';
                    ctx.lineWidth = 3;
                } else {
                    ctx.lineWidth = 2;
                }
                
                ctx.fill();
                ctx.stroke();
                
                // 绘制节点值
                ctx.fillStyle = '#ffffff';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(node.value, node.x, node.y);
                
                // 递归绘制子节点
                this.drawNodes(ctx, node.left);
                this.drawNodes(ctx, node.right);
            }

            generateRandomTree(count = 7) {
                this.root = null;
                this.nodeCount = 0;
                this.clearAnimationQueue();
                
                const values = new Set();
                while (values.size < count) {
                    values.add(Math.floor(Math.random() * 90) + 10);
                }
                
                this.addToHistory(`生成随机BST，包含值: ${Array.from(values).join(', ')}`);
                
                Array.from(values).forEach(value => {
                    this.insert(value);
                });
                
                this.drawTree();
            }
        }

        // ==================== 全局变量 ====================
        const bst = new BST();
        let isPlaying = false;

        // ==================== DOM元素引用 ====================
        const treeCanvas = document.getElementById('treeCanvas');
        const nodeValueInput = document.getElementById('nodeValue');
        const operationSelect = document.getElementById('operation');
        const executeBtn = document.getElementById('executeBtn');
        const randomTreeBtn = document.getElementById('randomTreeBtn');
        const prevStepBtn = document.getElementById('prevStepBtn');
        const playPauseBtn = document.getElementById('playPauseBtn');
        const nextStepBtn = document.getElementById('nextStepBtn');
        const speedSlider = document.getElementById('speedSlider');
        const speedValue = document.getElementById('speedValue');
        const sequenceInput = document.getElementById('sequenceInput');
        const demoBtn = document.getElementById('demoBtn');
        const resetBtn = document.getElementById('resetBtn');
        const learnMoreBtn = document.getElementById('learnMoreBtn');
        const comparisonView = document.getElementById('comparisonView');

        // ==================== 工具函数 ====================
        function updateAlgorithmSteps(message) {
            const stepsContainer = document.getElementById('algorithmSteps');
            const stepItem = document.createElement('div');
            stepItem.className = 'step-item';
            stepItem.textContent = `• ${message}`;
            
            stepsContainer.appendChild(stepItem);
            stepsContainer.scrollTop = stepsContainer.scrollHeight;
        }

        function clearAlgorithmSteps() {
            const stepsContainer = document.getElementById('algorithmSteps');
            stepsContainer.innerHTML = '<div class="step-item">欢迎使用BST教学动画！请执行操作查看详细步骤。</div>';
        }

        // ==================== 事件监听器 ====================
        executeBtn.addEventListener('click', () => {
            const value = parseInt(nodeValueInput.value);
            const operation = operationSelect.value;
            
            if (isNaN(value) || value < 1 || value > 99) {
                updateAlgorithmSteps('错误: 请输入1-99之间的有效数字');
                return;
            }
            
            bst.clearAnimationQueue();
            clearAlgorithmSteps();
            
            switch (operation) {
                case 'insert':
                    bst.insert(value);
                    break;
                case 'delete':
                    bst.delete(value);
                    break;
                case 'search':
                    bst.search(value);
                    break;
            }
            
            bst.drawTree();
            bst.playAnimation();
        });

        randomTreeBtn.addEventListener('click', () => {
            bst.clearAnimationQueue();
            clearAlgorithmSteps();
            bst.generateRandomTree();
            updateAlgorithmSteps('已生成随机二叉搜索树');
        });

        prevStepBtn.addEventListener('click', () => {
            if (bst.currentStep > 0) {
                bst.currentStep--;
                bst.isAnimating = false;
                const step = bst.animationQueue[bst.currentStep];
                bst.executeAnimationStep(step);
            }
        });

        playPauseBtn.addEventListener('click', () => {
            if (bst.isAnimating) {
                bst.isAnimating = false;
                playPauseBtn.textContent = '▶️';
            } else {
                bst.playAnimation();
            }
        });

        nextStepBtn.addEventListener('click', () => {
            if (bst.currentStep < bst.animationQueue.length) {
                bst.isAnimating = false;
                const step = bst.animationQueue[bst.currentStep];
                bst.executeAnimationStep(step);
                bst.currentStep++;
            }
        });

        speedSlider.addEventListener('input', () => {

<!--检测到代码截断，自动续写中...-->
bst.speed = parseInt(speedSlider.value);
            const speedLabels = ['极慢', '很慢', '慢', '较慢', '中慢', '中速', '中快', '快', '很快', '极快'];
            speedValue.textContent = speedLabels[bst.speed - 1];
        });

        demoBtn.addEventListener('click', () => {
            const sequenceText = sequenceInput.value.trim();
            if (!sequenceText) {
                updateAlgorithmSteps('错误: 请输入演示序列');
                return;
            }
            
            const values = sequenceText.split(',').map(v => parseInt(v.trim())).filter(v => !isNaN(v));
            
            if (values.length === 0) {
                updateAlgorithmSteps('错误: 请输入有效的数字序列');
                return;
            }
            
            bst.clearAnimationQueue();
            clearAlgorithmSteps();
            bst.root = null;
            bst.nodeCount = 0;
            
            updateAlgorithmSteps(`开始序列演示: ${values.join(', ')}`);
            updateAlgorithmSteps('注意观察有序序列插入时BST的退化过程！');
            
            // 逐个插入值
            values.forEach((value, index) => {
                bst.insert(value);
            });
            
            bst.drawTree();
            bst.playAnimation();
            
            // 检查是否是有序序列（可能导致严重不平衡）
            const isSorted = values.every((val, i, arr) => i === 0 || val > arr[i-1]) || 
                            values.every((val, i, arr) => i === 0 || val < arr[i-1]);
            
            if (isSorted && values.length >= 5) {
                setTimeout(() => {
                    comparisonView.classList.add('active');
                    updateAlgorithmSteps('⚠️ 警告: 有序序列导致BST退化成链表！');
                    updateAlgorithmSteps('查找效率从 O(log n) 退化到 O(n)');
                }, values.length * 1000);
            }
        });

        resetBtn.addEventListener('click', () => {
            bst.root = null;
            bst.nodeCount = 0;
            bst.clearAnimationQueue();
            bst.isAnimating = false;
            clearAlgorithmSteps();
            comparisonView.classList.remove('active');
            bst.drawTree();
            bst.updateStats();
            updateAlgorithmSteps('已重置二叉搜索树');
        });

        learnMoreBtn.addEventListener('click', () => {
            updateAlgorithmSteps('📚 红黑树是一种自平衡二叉搜索树，它通过以下规则保持平衡:');
            updateAlgorithmSteps('1. 每个节点是红色或黑色');
            updateAlgorithmSteps('2. 根节点是黑色');
            updateAlgorithmSteps('3. 所有叶子节点(NIL)是黑色');
            updateAlgorithmSteps('4. 红色节点的两个子节点都是黑色');
            updateAlgorithmSteps('5. 从任一节点到其每个叶子的所有路径包含相同数目的黑色节点');
            updateAlgorithmSteps('这些规则确保树大致平衡，查找、插入、删除的时间复杂度都是 O(log n)');
            updateAlgorithmSteps('红黑树通过旋转和重新着色来维护这些性质');
        });

        treeCanvas.addEventListener('click', (event) => {
            const rect = treeCanvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;
            
            // 查找点击的节点
            const clickedNode = findNodeAtPosition(bst.root, x, y);
            if (clickedNode) {
                nodeValueInput.value = clickedNode.value;
                updateAlgorithmSteps(`选中节点 ${clickedNode.value}，已填入输入框`);
                
                // 高亮显示选中的节点
                bst.root && resetNodeStates(bst.root);
                clickedNode.highlight = true;
                bst.drawTree();
                
                setTimeout(() => {
                    clickedNode.highlight = false;
                    bst.drawTree();
                }, 1000);
            }
        });

        function findNodeAtPosition(node, x, y) {
            if (!node) return null;
            
            const distance = Math.sqrt(Math.pow(node.x - x, 2) + Math.pow(node.y - y, 2));
            if (distance <= node.radius) {
                return node;
            }
            
            return findNodeAtPosition(node.left, x, y) || findNodeAtPosition(node.right, x, y);
        }

        function resetNodeStates(node) {
            if (!node) return;
            node.state = 'normal';
            node.highlight = false;
            resetNodeStates(node.left);
            resetNodeStates(node.right);
        }

        // ==================== 初始化 ====================
        function init() {
            // 初始化速度显示
            speedValue.textContent = '中速';
            
            // 绘制初始空树
            bst.drawTree();
            bst.updateStats();
            
            // 添加一些初始节点以便演示
            setTimeout(() => {
                updateAlgorithmSteps('💡 提示: 尝试以下操作:');
                updateAlgorithmSteps('1. 插入一些节点（如: 50, 30, 70, 20, 40）');
                updateAlgorithmSteps('2. 点击"随机生成BST"创建随机树');
                updateAlgorithmSteps('3. 输入"1,2,3,4,5"并点击"开始序列演示"观察退化');
                updateAlgorithmSteps('4. 点击画布上的节点可以选中它');
            }, 1000);
        }

        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 📚 交互式教学动画使用指南

欢迎使用**二叉搜索树(BST)教学动画**！本指南将帮助您充分利用这个交互式学习工具，深入理解BST的核心操作及其平衡性问题。

---

## 🎯 功能说明

本动画是一个完整的HTML5交互式教学工具，通过可视化方式演示二叉搜索树的**插入、删除、查找**操作，并直观展示**平衡性破坏**问题，自然引出**红黑树**等平衡二叉搜索树的解决方案。

### 核心教学价值：
- **动态可视化**：将抽象的算法过程转化为直观的动画
- **即时反馈**：每一步操作都有详细的算法步骤说明
- **性能对比**：实时显示树的统计信息，理解数据结构性能
- **问题导向**：通过有序序列演示，揭示BST的局限性

---

## 🎮 主要功能

### 1. **基本操作区**
- **节点值输入**：输入1-99之间的整数值
- **操作选择**：插入、删除、查找三种基本操作
- **执行操作**：点击后开始动画演示

### 2. **动画控制区**
- **播放/暂停**：控制动画流程
- **上一步/下一步**：精细控制学习节奏
- **速度调节**：10档速度可选，从"极慢"到"极快"

### 3. **演示模式**
- **序列演示**：输入逗号分隔的数字序列（如`1,2,3,4,5`）
- **随机生成**：一键创建随机的平衡BST
- **重置功能**：清空当前树，重新开始

### 4. **信息显示区**
- **算法步骤**：实时显示当前操作的详细步骤
- **树状统计**：显示节点数、树高度、平均查找长度、平衡状态
- **不平衡警告**：当树严重倾斜时自动提示

### 5. **交互功能**
- **画布点击**：直接点击树上的节点，自动填入输入框
- **颜色编码**：不同状态的节点用不同颜色区分
- **路径追踪**：查找操作时高亮显示搜索路径

---

## ✨ 设计特色

### 🎨 **视觉设计**
- **专业配色方案**：采用科技蓝为主色调，功能色区分明确
- **清晰的视觉层次**：节点、连线、文本层次分明
- **状态反馈**：7种颜色编码区分不同节点状态
- **响应式布局**：适应不同屏幕尺寸

### 🔧 **交互设计**
- **双模式学习**：支持手动操作和自动演示两种模式
- **渐进式学习**：从简单操作到复杂概念逐步深入
- **错误预防**：输入验证和操作提示
- **历史记录**：保留最近50条操作记录

### 📊 **教学设计**
- **认知负荷管理**：分步骤演示，避免信息过载
- **对比学习**：平衡树与退化树的直观对比
- **问题引导**：通过演示引出问题，激发思考
- **知识连接**：自然过渡到红黑树解决方案

---

## 🧠 教学要点

### 第一阶段：掌握基本操作
1. **插入操作**
   - 观察比较过程：从根节点开始，逐层比较
   - 理解定位逻辑：小于向左，大于向右
   - 注意重复值处理：BST不允许重复值

2. **查找操作**
   - 追踪搜索路径：黄色高亮显示比较过程
   - 计算查找步数：理解O(log n)的理想情况
   - 分析失败情况：查找不存在的节点

3. **删除操作**
   - 三种情况区分：叶子节点、单子节点、双子节点
   - 重点理解后继节点：右子树的最小值
   - 观察替换过程：值替换而非节点移动

### 第二阶段：理解平衡性问题
1. **有序序列演示**
   - 输入`1,2,3,4,5`观察退化过程
   - 注意高度增长：从平衡树退化成链表
   - 查看统计变化：平均查找长度急剧增加

2. **性能对比**
   - 对比平衡树与退化树的高度
   - 理解O(n)与O(log n)的实际差异
   - 观察不平衡警告的触发条件

### 第三阶段：探索解决方案
1. **红黑树引出**
   - 点击"了解更多"查看红黑树基本规则
   - 理解自平衡机制的必要性
   - 建立BST与高级数据结构的知识连接

---

## 💡 使用建议

### 给学生的建议：
1. **循序渐进**：先掌握基本操作，再研究平衡性问题
2. **动手实践**：不要只看演示，自己动手操作
3. **提出问题**：在操作前预测结果，验证理解
4. **对比分析**：创建不同形状的树，对比性能差异
5. **记录发现**：记录观察到的规律和问题

### 给教师的建议：
1. **课堂演示**：使用投影展示关键操作
2. **任务驱动**：设计具体任务让学生完成
3. **分组讨论**：让学生讨论优化策略
4. **扩展研究**：以此为基础介绍AVL树、红黑树
5. **评估工具**：观察学生的操作过程，评估理解程度

### 推荐学习路径：
1. **新手入门**（15分钟）
   - 插入5-7个随机节点
   - 练习查找操作
   - 尝试删除叶子节点

2. **进阶探索**（20分钟）
   - 使用序列演示观察退化
   - 分析统计信息的变化
   - 理解不平衡警告的意义

3. **深度思考**（15分钟）
   - 思考如何避免退化
   - 探索红黑树的平衡机制
   - 设计自己的平衡策略

---

## 🚀 快速开始

1. **立即体验**：点击"随机生成BST"创建第一棵树
2. **基础练习**：尝试插入值30、50、20、40、70
3. **挑战任务**：删除值为50的节点（注意后继节点）
4. **问题探索**：演示序列`1,2,3,4,5,6,7,8,9,10`
5. **知识延伸**：点击不平衡警告中的"了解更多"

---

## 📞 技术支持

本动画为纯HTML5实现，无需安装任何插件：
- **浏览器要求**：Chrome 80+、Firefox 75+、Edge 80+
- **网络环境**：完全本地运行，无需网络连接
- **设备兼容**：支持桌面和触摸屏设备

---

## 🌟 学习目标达成

完成本动画的学习后，您将能够：
- ✅ 清晰描述BST三种基本操作的算法步骤
- ✅ 可视化理解BST可能的不平衡问题
- ✅ 解释平衡二叉搜索树的必要性
- ✅ 对比不同树结构的性能差异
- ✅ 为学习红黑树等高级数据结构奠定基础

---

**祝您学习愉快，探索数据结构的奇妙世界！** 🎓

*有任何反馈或建议，欢迎通过教育技术平台分享您的使用体验。*