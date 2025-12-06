# 需求：图的深度优先搜索（DFS递归染色）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要是计算机科学或相关专业的学生，他们正在学习数据结构和算法。用户的需求层次如下：
1.  **理解概念**：理解DFS递归遍历图的**过程**（访问顺序、递归栈的变化）和**核心思想**（“一路到底，回溯探索”）。
2.  **理解状态**：清晰地区分图中节点的三种状态：“未访问”、“访问中”（在递归栈中）、“已访问”。
3.  **建立联系**：将抽象的递归调用过程与具体的节点访问、边探索的视觉变化联系起来，化解递归的理解难点。
4.  **自主探索**：能够控制动画速度，单步执行，并可能输入不同的图结构进行验证，从而主动构建知识。

因此，动画的核心是**将递归这一不可见的控制流，通过节点的颜色变化和视觉高亮，变得清晰可见**。

#### 教学设计思路
*   **核心概念**：
    *   **节点状态**：用三种颜色明确表示。
        *   **白色**：未访问。
        *   **灰色**：正在访问/在递归栈中（即已发现但未完成其所有邻接点的探索）。
        *   **黑色**：已访问完毕（即其所有邻接点都已探索完成）。
    *   **递归过程**：从起点开始，访问一个节点（变灰），然后对其每一个未访问的邻接节点**递归调用**DFS。当一个节点的所有邻接点都处理完后，递归返回（变黑）。
    *   **遍历树/边分类**：在遍历过程中，被首次探索并用于递归深入的边形成**DFS树（或森林）**，可以高亮显示。

*   **认知规律**：
    1.  **从具体到抽象**：先展示一个具体的图，通过动画运行一次完整的DFS，让用户获得整体印象。
    2.  **分解与聚焦**：在单步模式下，每一步只发生一个核心动作（如“选择起点”、“访问节点A”、“发现边A-B”、“递归访问节点B”、“回溯至节点A”等），并配以文字说明，降低认知负荷。
    3.  **双重编码**：同时呈现视觉动画（颜色、高亮、连线）和文字/语音解说（当前步骤描述），利用视觉和听觉通道共同促进理解。
    4.  **隐喻运用**：将递归栈可视化为一个从屏幕侧边伸出或底部增长的“栈”区域，灰色节点按顺序入栈/出栈，直观展示回溯点。

*   **交互设计**：
    *   **主流程控制**：提供“播放/暂停”、“下一步”、“上一步”、“重置”按钮，让用户能按自己的节奏学习。
    *   **速度调节**：提供滑块控制动画播放速度。
    *   **视角切换**：可能提供一个开关，在“**节点染色视图**”（核心视图）和“**递归栈视图**”（辅助视图）之间切换，帮助理解递归机制。
    *   **图结构交互**：允许用户在初始化阶段点击以添加/删除节点和边，或提供一个预设图库（如简单连通图、有环图、不连通图），让用户观察不同图结构下的DFS行为。

*   **视觉呈现**：
    *   **舞台**：干净、有科技感的深色或浅色背景，突出图形元素。
    *   **节点**：三种状态颜色对比鲜明。
        *   白色 (`#ffffff` / 边框 `#cccccc`)
        *   灰色 (`#ffa726` 或 `#f9a825`， 橙色/琥珀色，代表“活跃”)
        *   黑色 (`#66bb6a`， 绿色，代表“完成”)
    *   **边**：
        *   未探索边：浅灰色 (`#eeeeee`)。
        *   **树边**：在探索时高亮为与当前活动节点（灰色）同色系的深色（如 `#ef6c00`），并在DFS结束后保持为一种中性深色（如 `#424242`），以显示DFS生成树。
        *   回边/前向边/交叉边：在高级版本中可以用其他颜色区分（例如发现指向灰色节点的边时为红色，表示回边）。
    *   **动画**：颜色变化、线条绘制采用平滑过渡。当前正在处理的节点可以有一个脉动光环或放大效果，以吸引注意力。
    *   **信息面板**：固定区域显示当前步骤的文本描述、递归栈的当前内容列表、已访问节点的顺序列表。

#### 配色方案选择
选择兼顾清晰度、美观性和色觉友好度的方案。
*   **背景**：浅色模式 `#f5f7fa`（柔和灰白）或深色模式 `#2d3748`（深灰蓝）。
*   **节点状态色**：
    *   未访问： 白色填充 (`#ffffff`)，深灰边框 (`#4a5568`)。
    *   访问中（递归中）： 暖色突出。选择 `#fbbf24`（琥珀色），醒目且不过于刺眼。
    *   已访问： 冷色表示完成。选择 `#34d399`（翡翠绿），传达“已完成”信号。
*   **边颜色**：
    *   默认/未探索： `#cbd5e0`（浅灰色）。
    *   树边（已探索）： `#4a5568`（深灰色）。
    *   当前活动边： 与“访问中”节点同色 (`#fbbf24`)。
*   **UI/文字**：
    *   主要文字：深色模式用 `#e2e8f0`，浅色模式用 `#2d3748`。
    *   高亮/强调文字：使用节点“访问中”的颜色 (`#fbbf24`)。
    *   按钮：采用与状态色协调的配色。

#### 交互功能列表
1.  **图控制区**：
    *   “预设图例”下拉菜单（可选：链状图、星形图、简单环、不连通图等）。
    *   “随机生成图”按钮。
    *   “清除/重置图”按钮。
    *   *（进阶）* “编辑模式”切换：允许拖拽节点、点击两点添加边。
2.  **动画控制区**：
    *   “开始/暂停”按钮。
    *   “下一步”按钮（单步前进）。
    *   “上一步”按钮（单步后退）。
    *   “重置动画”按钮（复位到未开始状态）。
    *   “动画速度”滑块。
3.  **视图控制区**：
    *   “显示递归栈”复选框：显示/隐藏一个可视化栈区域，动态展示灰色节点的入栈出栈。
    *   “高亮树边”复选框。
4.  **信息显示区**：
    *   **步骤日志**：实时显示文本描述，如：“访问节点 0，将其标记为‘访问中’（灰色）”。
    *   **访问顺序列表**：按访问完成（变黑）的顺序列出节点，即DFS序列。
    *   **递归栈内容**：动态列表，显示当前栈中（灰色）的节点ID。
    *   **状态图例**：固定显示白、灰、黑三色代表的含义。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>图的深度优先搜索（DFS递归染色）教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #f5f7fa;
            color: #2d3748;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        header {
            text-align: center;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        header h1 {
            font-size: 2.2rem;
            margin-bottom: 8px;
        }

        header p {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }

        .left-panel {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .right-panel {
            flex: 2;
            min-width: 500px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .card {
            background: white;
            border-radius: 12px;
            padding: 24px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            border: 1px solid #e2e8f0;
        }

        .card h2 {
            color: #4a5568;
            font-size: 1.4rem;
            margin-bottom: 16px;
            padding-bottom: 8px;
            border-bottom: 2px solid #edf2f7;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .card h2 i {
            color: #fbbf24;
        }

        /* 图控制区 */
        .graph-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 16px;
        }

        select, button {
            padding: 10px 16px;
            border-radius: 8px;
            border: 1px solid #cbd5e0;
            background-color: white;
            color: #4a5568;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        select {
            flex: 1;
            min-width: 150px;
        }

        button {
            flex: 1;
            min-width: 120px;
            background-color: #edf2f7;
        }

        button:hover {
            background-color: #e2e8f0;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        button.primary {
            background-color: #4299e1;
            color: white;
            border-color: #4299e1;
        }

        button.primary:hover {
            background-color: #3182ce;
        }

        button.warning {
            background-color: #fbbf24;
            color: #78350f;
            border-color: #fbbf24;
        }

        button.warning:hover {
            background-color: #f59e0b;
        }

        /* 动画控制区 */
        .animation-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            align-items: center;
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            flex: 1;
            min-width: 200px;
        }

        .speed-control label {
            white-space: nowrap;
        }

        input[type="range"] {
            flex: 1;
            height: 6px;
            border-radius: 3px;
            background: #e2e8f0;
            outline: none;
            -webkit-appearance: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #fbbf24;
            cursor: pointer;
        }

        /* 视图控制区 */
        .view-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 16px;
        }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        input[type="checkbox"] {
            width: 18px;
            height: 18px;
            accent-color: #fbbf24;
        }

        /* 状态图例 */
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 8px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .color-box {
            width: 24px;
            height: 24px;
            border-radius: 4px;
            border: 2px solid #4a5568;
        }

        .unvisited { background-color: #ffffff; }
        .visiting { background-color: #fbbf24; }
        .visited { background-color: #34d399; }
        .tree-edge { background-color: #4a5568; height: 4px; margin-top: 10px; }
        .default-edge { background-color: #cbd5e0; height: 4px; margin-top: 10px; }

        /* 画布容器 */
        #graphCanvas {
            width: 100%;
            height: 500px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            border: 1px solid #e2e8f0;
        }

        /* 信息显示区 */
        .info-panel {
            height: 300px;
            display: flex;
            flex-direction: column;
        }

        .info-content {
            flex: 1;
            overflow-y: auto;
            padding-right: 8px;
        }

        .step-log {
            margin-bottom: 20px;
        }

        .step-log h3 {
            color: #4a5568;
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        #currentStep {
            background-color: #f7fafc;
            padding: 12px;
            border-radius: 8px;
            border-left: 4px solid #fbbf24;
            font-weight: 500;
            margin-bottom: 16px;
        }

        .data-display {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 16px;
        }

        .data-box {
            flex: 1;
            min-width: 200px;
        }

        .data-box h3 {
            color: #4a5568;
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        .data-list {
            background-color: #f7fafc;
            padding: 12px;
            border-radius: 8px;
            min-height: 80px;
            max-height: 120px;
            overflow-y: auto;
            border: 1px solid #e2e8f0;
        }

        .stack-item {
            padding: 6px 10px;
            margin-bottom: 4px;
            background-color: #fed7aa;
            border-radius: 4px;
            font-weight: 500;
            text-align: center;
        }

        .node-sequence {
            display: inline-block;
            padding: 4px 10px;
            margin: 2px;
            background-color: #d1fae5;
            border-radius: 4px;
            font-weight: 500;
        }

        /* 响应式调整 */
        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
            
            .left-panel, .right-panel {
                min-width: 100%;
            }
        }

        /* 滚动条样式 */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb {
            background: #cbd5e0;
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: #a0aec0;
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <div class="container">
        <header>
            <h1><i class="fas fa-project-diagram"></i> 图的深度优先搜索（DFS递归染色）</h1>
            <p>通过颜色变化可视化递归遍历过程：白色(未访问) → 琥珀色(访问中) → 绿色(已访问)</p>
        </header>

        <div class="main-content">
            <!-- 左侧控制面板 -->
            <div class="left-panel">
                <!-- 图控制区 -->
                <div class="card">
                    <h2><i class="fas fa-sitemap"></i> 图控制</h2>
                    <div class="graph-controls">
                        <select id="graphPreset">
                            <option value="default">默认连通图</option>
                            <option value="chain">链状图 (0-1-2-3-4)</option>
                            <option value="star">星形图</option>
                            <option value="cycle">简单环</option>
                            <option value="disconnected">不连通图</option>
                            <option value="tree">树状图</option>
                        </select>
                        <button id="randomGraph" class="primary">
                            <i class="fas fa-random"></i> 随机生成
                        </button>
                        <button id="resetGraph" class="warning">
                            <i class="fas fa-redo"></i> 重置图
                        </button>
                    </div>
                    
                    <div class="view-controls">
                        <div class="checkbox-group">
                            <input type="checkbox" id="showStack" checked>
                            <label for="showStack">显示递归栈</label>
                        </div>
                        <div class="checkbox-group">
                            <input type="checkbox" id="highlightTreeEdges" checked>
                            <label for="highlightTreeEdges">高亮DFS树边</label>
                        </div>
                    </div>
                </div>

                <!-- 动画控制区 -->
                <div class="card">
                    <h2><i class="fas fa-play-circle"></i> 动画控制</h2>
                    <div class="animation-controls">
                        <button id="startBtn" class="primary">
                            <i class="fas fa-play"></i> 开始
                        </button>
                        <button id="nextBtn">
                            <i class="fas fa-step-forward"></i> 下一步
                        </button>
                        <button id="prevBtn">
                            <i class="fas fa-step-backward"></i> 上一步
                        </button>
                        <button id="resetAnim" class="warning">
                            <i class="fas fa-stop"></i> 重置动画
                        </button>
                    </div>
                    
                    <div class="speed-control">
                        <label for="speedSlider"><i class="fas fa-tachometer-alt"></i> 速度:</label>
                        <input type="range" id="speedSlider" min="100" max="2000" value="800" step="100">
                        <span id="speedValue">0.8s</span>
                    </div>
                </div>

                <!-- 状态图例 -->
                <div class="card">
                    <h2><i class="fas fa-palette"></i> 状态图例</h2>
                    <div class="legend">
                        <div class="legend-item">
                            <div class="color-box unvisited"></div>
                            <span>未访问</span>
                        </div>
                        <div class="legend-item">
                            <div class="color-box visiting"></div>
                            <span>访问中 (递归栈中)</span>
                        </div>
                        <div class="legend-item">
                            <div class="color-box visited"></div>
                            <span>已访问完成</span>
                        </div>
                    </div>
                    <div class="legend" style="margin-top: 16px;">
                        <div class="legend-item">
                            <div class="color-box tree-edge"></div>
                            <span>DFS树边</span>
                        </div>
                        <div class="legend-item">
                            <div class="color-box default-edge"></div>
                            <span>普通边</span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- 右侧主面板 -->
            <div class="right-panel">
                <!-- 图可视化区域 -->
                <div class="card" style="padding: 0; overflow: hidden;">
                    <canvas id="graphCanvas"></canvas>
                </div>

                <!-- 信息显示区 -->
                <div class="card info-panel">
                    <h2><i class="fas fa-info-circle"></i> 算法执行信息</h2>
                    <div class="info-content">
                        <div class="step-log">
                            <h3>当前步骤</h3>
                            <div id="currentStep">请选择图并点击"开始"按钮</div>
                        </div>
                        
                        <div class="data-display">
                            <div class="data-box">
                                <h3>递归栈内容 <span id="stackCount">(0)</span></h3>
                                <div class="data-list" id="stackContent">
                                    <div style="color: #a0aec0; text-align: center; padding: 20px;">栈为空</div>
                                </div>
                            </div>
                            
                            <div class="data-box">
                                <h3>访问顺序 (完成顺序)</h3>
                                <div class="data-list" id="visitOrder">
                                    <div style="color: #a0aec0; text-align: center; padding: 20px;">暂无节点</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // ==================== 全局变量和常量 ====================
        const canvas = document.getElementById('graphCanvas');
        const ctx = canvas.getContext('2d');
        
        // 颜色常量
        const COLORS = {
            BACKGROUND: '#ffffff',
            NODE: {
                UNVISITED: '#ffffff',
                VISITING: '#fbbf24',
                VISITED: '#34d399',
                BORDER: '#4a5568',
                TEXT: '#2d3748'
            },
            EDGE: {
                DEFAULT: '#cbd5e0',
                TREE: '#4a5568',
                ACTIVE: '#fbbf24',
                HIGHLIGHT: '#ef6c00'
            },
            STACK: {
                BACKGROUND: '#fed7aa',
                BORDER: '#fbbf24'
            }
        };
        
        // 图数据结构
        let graph = {
            nodes: [],
            edges: [],
            adjacencyList: {}
        };
        
        // 动画状态
        let animationState = {
            isRunning: false,
            isPaused: false,
            currentStepIndex: 0,
            speed: 800, // 毫秒
            visitedOrder: [],
            stack: [],
            currentNode: null,
            treeEdges: new Set()
        };
        
        // 算法步骤记录
        let algorithmSteps = [];
        
        // 视图设置
        let viewSettings = {
            showStack: true,
            highlightTreeEdges: true
        };
        
        // ==================== 初始化 ====================
        function init() {
            // 设置Canvas尺寸
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // 初始化事件监听器
            initEventListeners();
            
            // 创建默认图
            createDefaultGraph();
            
            // 绘制初始状态
            drawGraph();
            
            // 更新UI
            updateUI();
        }
        
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            drawGraph();
        }
        
        function initEventListeners() {
            // 图控制
            document.getElementById('graphPreset').addEventListener('change', function() {
                if (this.value === 'default') createDefaultGraph();
                else if (this.value === 'chain') createChainGraph();
                else if (this.value === 'star') createStarGraph();
                else if (this.value === 'cycle') createCycleGraph();
                else if (this.value === 'disconnected') createDisconnectedGraph();
                else if (this.value === 'tree') createTreeGraph();
                
                resetAnimation();
                drawGraph();
            });
            
            document.getElementById('randomGraph').addEventListener('click', createRandomGraph);
            document.getElementById('resetGraph').addEventListener('click', function() {
                createDefaultGraph();
                resetAnimation();
                drawGraph();
            });
            
            // 视图控制
            document.getElementById('showStack').addEventListener('change', function() {
                viewSettings.showStack = this.checked;
                drawGraph();
            });
            
            document.getElementById('highlightTreeEdges').addEventListener('change', function() {
                viewSettings.highlightTreeEdges = this.checked;
                drawGraph();
            });
            
            // 动画控制
            document.getElementById('startBtn').addEventListener('click', toggleAnimation);
            document.getElementById('nextBtn').addEventListener('click', nextStep);
            document.getElementById('prevBtn').addEventListener('click', prevStep);
            document.getElementById('resetAnim').addEventListener('click', resetAnimation);
            
            // 速度控制
            const speedSlider = document.getElementById('speedSlider');
            const speedValue = document.getElementById('speedValue');
            
            speedSlider.addEventListener('input', function() {
                animationState.speed = 2100 - this.value; // 反转值，使滑块向右速度更快
                speedValue.textContent = (animationState.speed / 1000).toFixed(1) + 's';
            });
            
            // 初始速度显示
            speedValue.textContent = (animationState.speed / 1000).toFixed(1) + 's';
            speedSlider.value = 2100 - animationState.speed;
        }
        
        // ==================== 图创建函数 ====================
        function createDefaultGraph() {
            // 创建一个简单的连通图
            graph.nodes = [
                {id: 0, x: 0.3, y: 0.3, state: 'unvisited'},
                {id: 1, x: 0.7, y: 0.3, state: 'unvisited'},
                {id: 2, x: 0.7, y: 0.7, state: 'unvisited'},
                {id: 3, x: 0.3, y: 0.7, state: 'unvisited'},
                {id: 4, x: 0.5, y: 0.5, state: 'unvisited'}
            ];
            
            graph.edges = [
                {from: 0, to: 1, type: 'default'},
                {from: 0, to: 3, type: 'default'},
                {from: 0, to: 4, type: 'default'},
                {from: 1, to: 2, type: 'default'},
                {from: 1, to: 4, type: 'default'},
                {from: 2, to: 3, type: 'default'},
                {from: 2, to: 4, type: 'default'},
                {from: 3, to: 4, type: 'default'}
            ];
            
            buildAdjacencyList();
            updateNodePositions();
        }
        
        function createChainGraph() {
            graph.nodes = [];
            graph.edges = [];
            
            // 创建5个节点的链
            for (let i = 0; i < 5; i++) {
                graph.nodes.push({
                    id: i,
                    x: 0.1 + i * 0.2,
                    y: 0.5,
                    state: 'unvisited'
                });
                
                if (i > 0) {
                    graph.edges.push({from: i-1, to: i, type: 'default'});
                }
            }
            
            buildAdjacencyList();
            updateNodePositions();
        }
        
        function createStarGraph() {
            graph.nodes = [];
            graph.edges = [];
            
            // 中心节点
            graph.nodes.push({id: 0, x: 0.5, y: 0.5, state: 'unvisited'});
            
            // 5个外围节点
            const angles = [0, 72, 144, 216, 288];
            for (let i = 0; i < 5; i++) {
                const angle = angles[i] * Math.PI / 180;
                graph.nodes.push({
                    id: i+1,
                    x: 0.5 + 0.3 * Math.cos(angle),
                    y: 0.5 + 0.3 * Math.sin(angle),
                    state: 'unvisited'
                });
                
                graph.edges.push({from: 0, to: i+1, type: 'default'});
            }
            
            buildAdjacencyList();
            updateNodePositions();
        }
        
        function createCycleGraph() {
            graph.nodes = [];
            graph.edges = [];
            
            // 创建6个节点的环
            for (let i = 0; i < 6; i++) {
                const angle = i * 60 * Math.PI / 180;
                graph.nodes.push({
                    id: i,
                    x: 0.5 + 0.3 * Math.cos(angle),
                    y: 0.5 + 0.3 * Math.sin(angle),
                    state: 'unvisited'
                });
                
                graph.edges.push({from: i, to: (i+1) % 6, type: 'default'});
            }
            
            buildAdjacencyList();
            updateNodePositions();
        }
        
        function createDisconnectedGraph() {
            graph.nodes = [];
            graph.edges = [];
            
            // 第一个连通分量 (3个节点)
            for (let i = 0; i < 3; i++) {
                graph.nodes.push({
                    id: i,
                    x: 0.2 + i * 0.15,
                    y: 0.3,
                    state: 'unvisited'
                });
                
                if (i > 0) {
                    graph.edges.push({from: i-1, to: i, type: 'default'});
                }
            }
            
            // 第二个连通分量 (4个节点)
            for (let i = 0; i < 4; i++) {
                graph.nodes.push({
                    id: i+3,
                    x: 0.5 + i * 0.15,
                    y: 0.7,
                    state: 'unvisited'
                });
                
                if (i > 0) {
                    graph.edges.push({from: i+2, to: i+3, type: 'default'});
                }
            }
            
            buildAdjacencyList();
            updateNodePositions();
        }
        
        function createTreeGraph() {
            graph.nodes = [];
            graph.edges = [];
            
            // 创建一棵二叉树
            const nodes = [
                {id: 0, x: 0.5, y: 0.2},  // 根节点
                {id: 1, x: 0.3, y: 0.4},  // 左子节点
                {id: 2, x: 0.7, y: 0.4},  // 右子节点
                {id: 3, x: 0.2, y: 0.6},  // 左左子节点
                {id: 4, x: 0.4, y: 0.6},  // 左右子节点
                {id: 5, x: 0.6, y: 0.6},  // 右左子节点
                {id: 6, x: 0.8, y: 0.6}   // 右右子节点
            ];
            
            graph.nodes = nodes.map(node => ({...node, state: 'unvisited'}));
            
            const edges = [
                {from: 0, to: 1}, {from: 0, to: 2},
                {from: 1, to: 3}, {from: 1, to: 4},
                {from: 2, to: 5}, {from: 2, to: 6}
            ];
            
            graph.edges = edges.map(edge => ({...edge, type: 'default'}));
            
            buildAdjacencyList();
            updateNodePositions();
        }
        
        function createRandomGraph() {
            graph.nodes = [];
            graph.edges = [];
            
            // 随机生成5-8个节点
            const nodeCount = Math.floor(Math.random() * 4) + 5;
            
            for (let i = 0; i < nodeCount; i++) {
                graph.nodes.push({
                    id: i,
                    x: 0.1 + Math.random() * 0.8,
                    y: 0.1 + Math.random() * 0.8,
                    state: 'unvisited'
                });
            }
            
            // 随机生成边，确保图是连通的
            const connected = new Set([0]);
            const unconnected = new Set(Array.from({length: nodeCount-1}, (_, i) => i+1));
            
            while (unconnected.size > 0) {
                const from = Array.from(connected)[Math.floor(Math.random() * connected.size)];
                const to = Array.from(unconnected)[Math.floor(Math.random() * unconnected.size)];
                
                graph.edges.push({from, to, type: 'default'});
                connected.add(to);
                unconnected.delete(to);
            }
            
            // 添加一些额外的随机边
            const extraEdges = Math.floor(Math.random() * 5) + 2;
            for (let i = 0; i < extraEdges; i++) {
                const from = Math.floor(Math.random() * nodeCount);
                const to = Math.floor(Math.random() * nodeCount);
                
                if (from !== to && !graph.edges.some(e => 
                    (e.from === from && e.to === to) || (e.from === to && e.to === from))) {
                    graph.edges.push({from, to, type: 'default'});
                }
            }
            
            buildAdjacencyList();
            updateNodePositions();
            resetAnimation();
            drawGraph();
        }
        
        function buildAdjacencyList() {
            graph.adjacencyList = {};
            
            for (const node of graph.nodes) {
                graph.adjacencyList[node.id] = [];
            }
            
            for (const edge of graph.edges) {
                graph.adjacencyList[edge.from].push(edge.to);
                graph.adjacencyList[edge.to].push(edge.from);
            }
        }
        
        function updateNodePositions() {
            // 将相对坐标转换为绝对坐标
            const width = canvas.width;
            const height = canvas.height;
            const margin = 60;
            
            graph.nodes.forEach(node => {
                node.actualX = margin + node.x * (width - 2 * margin);
                node.actualY = margin + node.y * (height - 2 * margin);
            });
        }
        
        // ==================== 绘图函数 ====================
        function drawGraph() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制边
            drawEdges();
            
            // 绘制节点
            drawNodes();
            
            // 绘制递归栈（如果启用）
            if (viewSettings.showStack) {
                drawStack();
            }
        }
        
        function drawEdges() {
            for (const edge of graph.edges) {
                const fromNode = graph.nodes.find(n => n.id === edge.from);
                const toNode = graph.nodes.find(n => n.id === edge.to);
                
                if (!fromNode || !toNode) continue;
                
                // 确定边的颜色
                let color = COLORS.EDGE.DEFAULT;
                let lineWidth = 2;
                
                // 检查是否是树边
                const edgeKey = `${Math.min(edge.from, edge.to)}-${Math.max(edge.from, edge.to)}`;
                const isTreeEdge = animationState.treeEdges.has(edgeKey);
                
                if (isTreeEdge && viewSettings.highlightTreeEdges) {
                    color = COLORS.EDGE.TREE;
                    lineWidth = 3;
                }
                
                // 检查是否是当前活动的边
                if (animationState.currentNode !== null) {
                    const currentNode = graph.nodes.find(n => n.id === animationState.currentNode);
                    if (currentNode && 
                        ((edge.from === currentNode.id && graph.nodes.find(n => n.id === edge.to).state === 'visiting') ||
                         (edge.to === currentNode.id && graph.nodes.find(n => n.id === edge.from).state === 'visiting'))) {
                        color = COLORS.EDGE.ACTIVE;
                        lineWidth = 4;
                    }
                }
                
                // 绘制边
                ctx.beginPath();
                ctx.moveTo(fromNode.actualX, fromNode.actualY);
                ctx.lineTo(toNode.actualX, toNode.actualY);
                ctx.strokeStyle = color;
                ctx.lineWidth = lineWidth;
                ctx.stroke();
            }
        }
        
        function drawNodes() {
            for (const node of graph.nodes) {
                // 确定节点颜色
                let fillColor;
                switch (node.state) {
                    case 'unvisited': fillColor = COLORS.NODE.UNVISITED; break;
                    case 'visiting': fillColor = COLORS.NODE.VISITING; break;
                    case 'visited': fillColor = COLORS.NODE.VISITED; break;
                    default: fillColor = COLORS.NODE.UNVISITED;
                }
                
                // 绘制节点外圈（如果正在访问，添加脉动效果）
                if (node.state === 'visiting') {
                    ctx.beginPath();
                    ctx.arc(node.actualX, node.actualY, 28, 0, Math.PI * 2);
                    ctx.fillStyle = 'rgba(251, 191, 36, 0.2)';
                    ctx.fill();
                    
                    // 脉动动画
                    const pulseSize = 24 + Math.sin(Date.now() / 300) * 4;
                    ctx.beginPath();
                    ctx.arc(node.actualX, node.actualY, pulseSize, 0, Math.PI * 2);
                    ctx.strokeStyle = 'rgba(251, 191, 36, 0.5)';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
                
                // 绘制节点
                ctx.beginPath();
                ctx.arc(node.actualX, node.actualY, 22, 0, Math.PI * 2);
                ctx.fillStyle = fillColor;
                ctx.fill();
                ctx.strokeStyle = COLORS.NODE.BORDER;
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 绘制节点ID
                ctx.fillStyle = COLORS.NODE.TEXT;
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(node.id, node.actualX, node.actualY);
                
                // 如果节点是当前活动节点，添加指示器
                if (animationState.currentNode === node.id) {
                    ctx.beginPath();
                    ctx.arc(node.actualX, node.actualY, 26, 0, Math.PI * 2);
                    ctx.strokeStyle = '#ef4444';
                    ctx.lineWidth = 3;
                    ctx.stroke();
                }
            }
        }
        
        function drawStack() {
            const stack = animationState.stack;
            if (stack.length === 0) return;
            
            const stackWidth = 80;
            const stackHeight = 40;
            const startX = canvas.width - stackWidth - 20;
            const startY = 20;
            
            // 绘制栈标题
            ctx.fillStyle = COLORS.NODE.TEXT;
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'left';
            ctx.fillText('递归栈:', startX, startY - 10);
            
            // 绘制栈容器
            ctx.strokeStyle = COLORS.STACK.BORDER;
            ctx.lineWidth = 2;
            ctx.strokeRect(startX, startY, stackWidth, stackHeight * 6);
            
            // 绘制栈中的节点
            for (let i = 0; i < stack.length; i++) {
                const nodeId = stack[i];
                const yPos = startY + stackHeight * (5 - i); // 从底部开始绘制
                
                // 栈项背景
                ctx.fillStyle = COLORS.STACK.BACKGROUND;
                ctx.fillRect(startX + 2, yPos + 2, stackWidth - 4, stackHeight - 4);
                
                // 栈项边框
                ctx.strokeStyle = COLORS.STACK.BORDER;
                ctx.lineWidth = 2;
                ctx.strokeRect(startX + 2, yPos + 2, stackWidth - 4, stackHeight - 4);
                
                // 栈项文本
                ctx.fillStyle = COLORS.NODE.TEXT;
                ctx.font = 'bold 20px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(`节点 ${nodeId}`, startX + stackWidth / 2, yPos + stackHeight / 2);
            }
        }
        
        // ==================== 算法实现 ====================
        function generateAlgorithmSteps() {
            algorithmSteps = [];
            animationState.treeEdges.clear();
            
            // 重置所有节点状态
            graph.nodes.forEach(node => node.state = 'unvisited');
            
            // 深度优先搜索递归函数
            function dfs(nodeId, parentId = null) {
                const node = graph.nodes.find(n => n.id === nodeId);
                if (!node) return;
                
                // 步骤1: 访问节点，标记为访问中
                algorithmSteps.push({
                    action: 'visit',
                    nodeId: nodeId,
                    description: `访问节点 ${nodeId}，将其标记为"访问中"（灰色）并压入递归栈`
                });
                
                node.state = 'visiting';
                if (parentId !== null) {
                    const edgeKey = `${Math.min(nodeId, parentId)}-${Math.max(nodeId, parentId)}`;
                    animationState.treeEdges.add(edgeKey);
                    
                    algorithmSteps.push({
                        action: 'tree_edge',
                        from: parentId,
                        to: nodeId,
                        description: `边 ${parentId}-${nodeId} 成为DFS树边`
                    });
                }
                
                // 获取邻居节点
                const neighbors = graph.adjacencyList[nodeId] || [];
                
                for (const neighborId of neighbors) {
                    const neighbor = graph.nodes.find(n => n.id === neighborId);
                    
                    // 步骤2: 检查邻居
                    algorithmSteps.push({
                        action: 'check_neighbor',
                        currentNode: nodeId,
                        neighborId: neighborId,
                        description: `检查节点 ${nodeId} 的邻居节点 ${neighborId}`
                    });
                    
                    if (neighbor.state === 'unvisited') {
                        // 步骤3: 递归访问邻居

<!--检测到代码截断，自动续写中...-->
algorithmSteps.push({
                            action: 'recurse',
                            from: nodeId,
                            to: neighborId,
                            description: `节点 ${neighborId} 未访问，递归调用DFS(${neighborId})`
                        });
                        
                        dfs(neighborId, nodeId);
                        
                        // 步骤4: 递归返回
                        algorithmSteps.push({
                            action: 'return',
                            nodeId: nodeId,
                            description: `从节点 ${neighborId} 递归返回到节点 ${nodeId}`
                        });
                    } else if (neighbor.state === 'visiting') {
                        // 发现回边（指向递归栈中的节点）
                        algorithmSteps.push({
                            action: 'back_edge',
                            from: nodeId,
                            to: neighborId,
                            description: `发现回边 ${nodeId}→${neighborId}（指向递归栈中的节点）`
                        });
                    } else {
                        // 邻居已访问完成
                        algorithmSteps.push({
                            action: 'skip_neighbor',
                            currentNode: nodeId,
                            neighborId: neighborId,
                            description: `节点 ${neighborId} 已访问完成，跳过`
                        });
                    }
                }
                
                // 步骤5: 完成节点访问
                algorithmSteps.push({
                    action: 'complete',
                    nodeId: nodeId,
                    description: `节点 ${nodeId} 的所有邻居已处理，标记为"已访问"（绿色）并弹出递归栈`
                });
                
                node.state = 'visited';
            }
            
            // 从节点0开始DFS（如果存在）
            if (graph.nodes.length > 0) {
                dfs(0);
            }
            
            // 检查是否有未访问的节点（不连通图）
            for (const node of graph.nodes) {
                if (node.state === 'unvisited') {
                    algorithmSteps.push({
                        action: 'new_component',
                        nodeId: node.id,
                        description: `发现新的连通分量，从节点 ${node.id} 开始DFS`
                    });
                    
                    dfs(node.id);
                }
            }
            
            // 添加完成步骤
            algorithmSteps.push({
                action: 'finish',
                description: `DFS遍历完成！总共访问了 ${graph.nodes.length} 个节点`
            });
        }
        
        // ==================== 动画控制函数 ====================
        function toggleAnimation() {
            const startBtn = document.getElementById('startBtn');
            const icon = startBtn.querySelector('i');
            
            if (!animationState.isRunning) {
                // 开始动画
                if (algorithmSteps.length === 0 || animationState.currentStepIndex >= algorithmSteps.length) {
                    generateAlgorithmSteps();
                    animationState.currentStepIndex = 0;
                    animationState.visitedOrder = [];
                    animationState.stack = [];
                    animationState.currentNode = null;
                }
                
                animationState.isRunning = true;
                animationState.isPaused = false;
                startBtn.innerHTML = '<i class="fas fa-pause"></i> 暂停';
                startBtn.classList.remove('primary');
                startBtn.classList.add('warning');
                
                playNextStep();
            } else {
                // 暂停动画
                animationState.isPaused = !animationState.isPaused;
                
                if (animationState.isPaused) {
                    startBtn.innerHTML = '<i class="fas fa-play"></i> 继续';
                    startBtn.classList.remove('warning');
                    startBtn.classList.add('primary');
                } else {
                    startBtn.innerHTML = '<i class="fas fa-pause"></i> 暂停';
                    startBtn.classList.remove('primary');
                    startBtn.classList.add('warning');
                    playNextStep();
                }
            }
            
            updateUI();
        }
        
        function playNextStep() {
            if (!animationState.isRunning || animationState.isPaused) return;
            
            if (animationState.currentStepIndex < algorithmSteps.length) {
                executeStep(animationState.currentStepIndex);
                animationState.currentStepIndex++;
                
                if (animationState.currentStepIndex < algorithmSteps.length) {
                    setTimeout(playNextStep, animationState.speed);
                } else {
                    // 动画完成
                    animationState.isRunning = false;
                    const startBtn = document.getElementById('startBtn');
                    startBtn.innerHTML = '<i class="fas fa-play"></i> 重新开始';
                    startBtn.classList.remove('warning');
                    startBtn.classList.add('primary');
                }
            }
            
            updateUI();
        }
        
        function nextStep() {
            if (algorithmSteps.length === 0 || animationState.currentStepIndex >= algorithmSteps.length) {
                generateAlgorithmSteps();
                animationState.currentStepIndex = 0;
                animationState.visitedOrder = [];
                animationState.stack = [];
                animationState.currentNode = null;
            }
            
            if (animationState.currentStepIndex < algorithmSteps.length) {
                executeStep(animationState.currentStepIndex);
                animationState.currentStepIndex++;
            }
            
            animationState.isRunning = false;
            animationState.isPaused = false;
            
            const startBtn = document.getElementById('startBtn');
            startBtn.innerHTML = '<i class="fas fa-play"></i> 继续';
            startBtn.classList.remove('warning');
            startBtn.classList.add('primary');
            
            updateUI();
        }
        
        function prevStep() {
            if (animationState.currentStepIndex > 0) {
                animationState.currentStepIndex--;
                undoStep(animationState.currentStepIndex);
            }
            
            animationState.isRunning = false;
            animationState.isPaused = false;
            
            const startBtn = document.getElementById('startBtn');
            startBtn.innerHTML = '<i class="fas fa-play"></i> 继续';
            startBtn.classList.remove('warning');
            startBtn.classList.add('primary');
            
            updateUI();
        }
        
        function executeStep(stepIndex) {
            const step = algorithmSteps[stepIndex];
            if (!step) return;
            
            // 更新当前步骤描述
            document.getElementById('currentStep').textContent = step.description;
            
            // 根据步骤类型执行相应操作
            switch (step.action) {
                case 'visit':
                    // 标记节点为访问中
                    const visitNode = graph.nodes.find(n => n.id === step.nodeId);
                    if (visitNode) visitNode.state = 'visiting';
                    
                    // 添加到递归栈
                    animationState.stack.push(step.nodeId);
                    animationState.currentNode = step.nodeId;
                    break;
                    
                case 'tree_edge':
                    // 树边已经在generateAlgorithmSteps时添加到集合中
                    break;
                    
                case 'check_neighbor':
                    animationState.currentNode = step.currentNode;
                    break;
                    
                case 'recurse':
                    animationState.currentNode = step.to;
                    break;
                    
                case 'return':
                    animationState.currentNode = step.nodeId;
                    break;
                    
                case 'complete':
                    // 标记节点为已访问
                    const completeNode = graph.nodes.find(n => n.id === step.nodeId);
                    if (completeNode) completeNode.state = 'visited';
                    
                    // 从递归栈弹出
                    if (animationState.stack.length > 0) {
                        animationState.stack.pop();
                    }
                    
                    // 添加到访问顺序列表
                    if (!animationState.visitedOrder.includes(step.nodeId)) {
                        animationState.visitedOrder.push(step.nodeId);
                    }
                    
                    // 更新当前节点
                    if (animationState.stack.length > 0) {
                        animationState.currentNode = animationState.stack[animationState.stack.length - 1];
                    } else {
                        animationState.currentNode = null;
                    }
                    break;
                    
                case 'back_edge':
                case 'skip_neighbor':
                    animationState.currentNode = step.currentNode || step.from;
                    break;
                    
                case 'new_component':
                    animationState.currentNode = step.nodeId;
                    break;
                    
                case 'finish':
                    animationState.currentNode = null;
                    break;
            }
            
            // 重绘图
            drawGraph();
        }
        
        function undoStep(stepIndex) {
            // 重置到上一步的状态需要重新生成步骤并执行到stepIndex
            // 这里简化处理：重新生成所有步骤并执行到stepIndex-1
            generateAlgorithmSteps();
            
            // 重置状态
            graph.nodes.forEach(node => node.state = 'unvisited');
            animationState.visitedOrder = [];
            animationState.stack = [];
            animationState.currentNode = null;
            animationState.treeEdges.clear();
            
            // 执行到stepIndex-1
            for (let i = 0; i < stepIndex; i++) {
                executeStep(i);
            }
            
            // 更新当前步骤描述
            if (stepIndex > 0) {
                const step = algorithmSteps[stepIndex - 1];
                document.getElementById('currentStep').textContent = step.description;
            } else {
                document.getElementById('currentStep').textContent = "已重置到初始状态";
            }
            
            drawGraph();
        }
        
        function resetAnimation() {
            animationState.isRunning = false;
            animationState.isPaused = false;
            animationState.currentStepIndex = 0;
            animationState.visitedOrder = [];
            animationState.stack = [];
            animationState.currentNode = null;
            animationState.treeEdges.clear();
            
            algorithmSteps = [];
            
            // 重置所有节点状态
            graph.nodes.forEach(node => node.state = 'unvisited');
            
            // 更新按钮状态
            const startBtn = document.getElementById('startBtn');
            startBtn.innerHTML = '<i class="fas fa-play"></i> 开始';
            startBtn.classList.remove('warning');
            startBtn.classList.add('primary');
            
            // 更新UI
            document.getElementById('currentStep').textContent = "请点击'开始'按钮运行DFS算法";
            updateUI();
            drawGraph();
        }
        
        // ==================== UI更新函数 ====================
        function updateUI() {
            // 更新递归栈显示
            const stackContent = document.getElementById('stackContent');
            const stackCount = document.getElementById('stackCount');
            
            if (animationState.stack.length === 0) {
                stackContent.innerHTML = '<div style="color: #a0aec0; text-align: center; padding: 20px;">栈为空</div>';
                stackCount.textContent = '(0)';
            } else {
                stackContent.innerHTML = '';
                animationState.stack.slice().reverse().forEach(nodeId => {
                    const stackItem = document.createElement('div');
                    stackItem.className = 'stack-item';
                    stackItem.textContent = `节点 ${nodeId}`;
                    stackContent.appendChild(stackItem);
                });
                stackCount.textContent = `(${animationState.stack.length})`;
            }
            
            // 更新访问顺序显示
            const visitOrderElement = document.getElementById('visitOrder');
            if (animationState.visitedOrder.length === 0) {
                visitOrderElement.innerHTML = '<div style="color: #a0aec0; text-align: center; padding: 20px;">暂无节点</div>';
            } else {
                visitOrderElement.innerHTML = '';
                animationState.visitedOrder.forEach(nodeId => {
                    const nodeElement = document.createElement('span');
                    nodeElement.className = 'node-sequence';
                    nodeElement.textContent = nodeId;
                    visitOrderElement.appendChild(nodeElement);
                });
            }
            
            // 更新步骤进度
            const progressElement = document.getElementById('currentStep');
            if (animationState.currentStepIndex < algorithmSteps.length) {
                // 进度信息已经在executeStep中更新
            }
        }
        
        // ==================== 初始化调用 ====================
        // 页面加载完成后初始化
        window.addEventListener('load', init);
        
        // 初始绘制
        drawGraph();
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## 图的深度优先搜索（DFS递归染色）交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过直观的视觉呈现和交互操作，帮助您深入理解图的深度优先搜索（DFS）算法的递归实现过程及其核心概念——**节点状态染色**。

---

### 一、 功能说明

本动画将抽象的DFS递归算法转化为可视化的动态过程。您将看到：
1.  **节点状态变化**：节点根据算法进程在 **白色（未访问）→ 琥珀色（访问中/递归栈中）→ 绿色（已访问完成）** 之间动态变化。
2.  **递归栈可视化**：屏幕右侧实时显示递归调用栈的内容，直观展示“深入”与“回溯”的过程。
3.  **DFS树生成**：算法探索过的边会高亮显示，最终形成一棵DFS生成树（或森林）。
4.  **完整的执行日志**：左侧面板同步显示每一步的文本描述、访问顺序和栈状态，实现视觉与逻辑的双重编码学习。

### 二、 主要功能区域与操作

#### 1. 图控制区
*   **预设图例**：下拉菜单提供6种经典图结构（如链状图、星形图、有环图、不连通图等），方便观察DFS在不同拓扑结构下的行为差异。
*   **随机生成**：点击按钮可创建一个随机连通图，用于探索不确定性。
*   **重置图**：将当前图恢复至初始状态。

#### 2. 动画控制区
*   **开始/暂停/继续**：控制动画的播放。动画将自动按设定速度执行所有步骤。
*   **下一步/上一步**：**推荐使用！** 单步前进或后退，让您有充足时间观察每一步的状态变化，是理解关键步骤的利器。
*   **重置动画**：将算法状态清零，恢复到未执行状态，但保留当前图结构。
*   **速度调节滑块**：向左拖动加快速度，向右拖动减慢速度。单步学习时建议使用较慢速度。

#### 3. 视图控制区
*   **显示递归栈**：勾选后，在画布右侧可视化显示递归栈。**强烈建议开启**，这是理解递归机制的关键。
*   **高亮DFS树边**：勾选后，被DFS首次探索并用于递归深入的边将高亮为深灰色，与普通边区分。

#### 4. 信息显示区
*   **当前步骤**：用文字详细描述算法当前执行的操作。
*   **递归栈内容**：以列表形式显示栈中节点，栈顶在最后。与右侧可视化栈同步。
*   **访问顺序**：记录节点被**标记为完成（变绿）** 的先后顺序，即DFS的完成序列。

#### 5. 可视化主画布
*   动态展示图结构、节点颜色、边的高亮效果。
*   **访问中（灰色）的节点**会有脉动光环效果，易于识别当前活动节点。
*   当前正在处理的节点会有一个红色圆圈作为额外指示。

### 三、 设计特色与教学要点

#### 核心设计隐喻：**“染色法”与“探险者”**
*   **白色区域**：代表未探索的领土。
*   **琥珀色节点**：代表“正在此地进行勘探的探险家”。每个灰色节点对应一个活跃的递归函数调用。
*   **绿色节点**：代表“已完全勘探完毕的领土”。探险家已从此地撤离，所有通路都已检查。
*   **递归栈**：代表了“探险家的足迹链”。栈顶是当前最前线的探险家，回溯时则按足迹原路返回。

#### 关键教学观察点
1.  **递归的深入**：观察当发现一个白色邻居时，算法如何“深入”——当前节点保持灰色（探险家留守），新节点变灰（派出新探险家），新节点入栈。
2.  **递归的回溯**：观察当一个节点的所有邻居都处理完毕后，该节点如何变绿（勘探完成），并从栈中弹出（探险家返回），控制权交还给栈中的上一个节点（上一个探险家）。
3.  **边的分类**：注意观察，连接灰色节点和白色节点的边被标记为**树边**（构成DFS树的骨架）。而连接灰色节点与另一个灰色节点的边，将被提示为**回边**（发现环的关键！）。
4.  **不连通图处理**：在“不连通图”预设中，观察算法如何在一个连通分量完成后，自动寻找下一个白色节点，开始新一轮DFS，形成**DFS森林**。

### 四、 使用建议与学习路径

为了达到最佳学习效果，建议按以下顺序使用本工具：

1.  **初次接触（建立直觉）**：
    *   选择“默认连通图”。
    *   点击“开始”，以正常速度观看一遍完整的动画。
    *   目标：对DFS的整体流程和颜色变化规律有一个总体的、感性的认识。

2.  **逐步深入（理解细节）**：
    *   重置动画，选择“链状图”或“树状图”这类简单结构。
    *   使用“下一步”按钮，**单步执行**。
    *   **每执行一步，完成以下观察**：
        a. 哪个节点的颜色变了？为什么？
        b. 递归栈的内容如何变化？（入栈/出栈）
        c. 当前高亮的是哪条边？它是什么类型的边？
        d. 阅读左侧的“当前步骤”描述，将文字与视觉变化对应起来。
    *   遇到“递归”步骤时，思考“控制权”的转移；遇到“返回”步骤时，思考“回溯”的发生。

3.  **对比探究（深化理解）**：
    *   使用“上一步”按钮，回退到关键步骤（如递归调用前、回溯前），重新执行，加深印象。
    *   切换到“星形图”、“简单环”等不同预设，重复单步学习过程。观察图结构如何影响访问顺序和栈的最大深度。
    *   尝试“随机生成”图，挑战在未知结构中预测算法的下一步行为。

4.  **概念整合（建立联系）**：
    *   关闭“高亮DFS树边”选项，观察图的原始状态。
    *   再次运行算法，注意观察哪些边最终被高亮。理解**DFS生成树/森林**是如何在遍历过程中自然形成的。
    *   总结节点颜色（白、灰、黑）、递归栈和DFS树边三者之间的同步关系。

---

**祝您学习愉快！** 通过这个交互式工具，我们希望将DFS算法从枯燥的代码和图示，转变为一场直观的“图领土勘探”之旅。请尽情探索、单步调试、反复观察，直到您能在脑海中清晰地复现出算法运行的每一帧画面。这正是理解算法精髓的开始。