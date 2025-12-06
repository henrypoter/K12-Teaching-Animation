# 需求：最小生成树：Kruskal（并查集+边排序加入）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：学习数据结构与算法的大学生或自学者，对图、树、排序等基础概念有一定了解，但对Kruskal算法的具体实现，尤其是并查集的应用感到抽象和困难。
2.  **核心痛点**：
    *   **算法流程抽象**：如何从一张带权无向图中，逐步选出边构成最小生成树的过程难以直观想象。
    *   **并查集理解困难**：并查集作为判断环的关键数据结构，其“合并”与“查找”操作以及集合的代表元概念较为抽象。
    *   **边排序的重要性**：为什么必须先对边按权值排序？贪心策略在此处的体现不直观。
    *   **代码与动画脱节**：静态的代码或图示无法动态展示算法每一步的状态变化和决策逻辑。
3.  **学习目标**：通过动画，用户应能：
    *   清晰复述Kruskal算法的核心步骤。
    *   理解并查集在判断环中的作用和工作原理。
    *   直观感受“贪心”选择最小权值边的过程。
    *   将动画中的每一步与伪代码或实际代码对应起来。

#### 教学设计思路
1.  **核心概念分解**：
    *   **输入**：带权连通无向图。
    *   **预处理**：将所有边按权值从小到大排序（视觉上突出排序过程）。
    *   **核心操作**：按序尝试加入每条边。
    *   **关键判断**：使用并查集判断加入此边是否会与已选边构成环（即边的两个端点是否已在同一集合中）。
    *   **结果**：当选出 `(顶点数 - 1)` 条边时，算法结束，得到最小生成树。

2.  **认知规律遵循**：
    *   **从具体到抽象**：先展示一个具体的图例，再抽象出算法步骤。
    *   **分步演示**：将算法分解为“排序边”、“取边”、“查集合”、“并集合”、“加边/跳过”等原子步骤，一步一步执行，允许用户控制节奏。
    *   **多视图联动**：同时呈现“图视图”、“并查集森林视图”、“已选边列表/高亮”和“算法伪代码高亮”，建立视觉关联，降低认知负荷。
    *   **正反例对比**：不仅展示成功加入的边，也清晰展示因构成环而被跳过的边，强化判断条件。

3.  **交互设计**：
    *   **节奏控制**：提供“上一步”、“下一步”、“自动播放/暂停”按钮，让用户能按自己的节奏学习。
    *   **探索模式**：在关键步骤（如判断是否成环时）设置提示或提问，鼓励用户先思考，再触发动画演示判断过程。
    *   **焦点引导**：通过高亮、放大、闪烁等效果，引导用户关注当前正在处理的边、正在操作的并查集节点等。
    *   **状态可视化**：实时显示当前已选边数、总权值、并查集中每个节点的父节点等信息。

4.  **视觉呈现**：
    *   **图视图**：顶点用圆形表示，边用线条连接，权值标注在线条旁。已加入生成树的边用粗体、高亮色（如绿色）显示；被检查但拒绝的边用另一种颜色（如红色）短暂高亮后恢复；未处理的边用中性色。
    *   **并查集视图**：以“森林”或“树”的形式直观展示每个集合。可以使用嵌套的圆圈、树形图或简单的“父指针”数组的可视化。当执行 `Find` 操作时，展示路径追踪；执行 `Union` 操作时，展示两棵树合并的过程。
    *   **边列表视图**：展示排序后的边列表（起点，终点，权值），当前正在处理的边高亮显示。
    *   **伪代码视图**：同步高亮当前正在执行的代码行，建立算法逻辑与视觉动画的直接映射。

#### 配色方案选择
*   **主色调**：采用科技蓝 (`#3498db`) 作为背景或主要标识色，传达理性与逻辑。
*   **状态色**：
    *   **未处理/默认**：灰色 (`#95a5a6`) 顶点和边。
    *   **当前处理中**：橙色 (`#e67e22`) 用于高亮当前选中的边和涉及的顶点。
    *   **成功加入**：绿色 (`#2ecc71`) 用于已加入最小生成树的边。
    *   **拒绝/成环**：红色 (`#e74c3c`) 用于短暂提示因构成环而被拒绝的边。
    *   **并查集高亮**：使用柔和的黄色 (`#f1c40f`) 或紫色 (`#9b59b6`) 来高亮正在操作的集合或路径。
*   **背景与文字**：浅灰色 (`#ecf0f1`) 背景，深灰色 (`#2c3e50`) 文字，确保良好的对比度和阅读舒适度。
*   **配色原则**：保持简洁、一致，使用颜色语义化（绿=通过/加入，红=拒绝/警告），避免过多颜色造成干扰。

#### 交互功能列表
1.  **基础控制**：
    *   “重置”：将动画恢复到初始状态。
    *   “上一步”：回退到上一个算法步骤。
    *   “下一步”：前进到下一个算法步骤。
    *   “播放/暂停”：自动连续执行算法步骤，可暂停。
    *   “速度调节”：滑块控制自动播放的速度。
2.  **视图控制**：
    *   “显示/隐藏权值”：切换图中边权值的显示。
    *   “并查集可视化模式切换”：在“树形图”、“父指针数组”、“压缩路径示意图”等不同可视化方式间切换。
3.  **探索性交互**：
    *   **点击边**：在手动模式下，允许用户点击“边列表”中的某条边，直接跳转到处理该边的步骤。
    *   **并查集节点查询**：鼠标悬停在并查集视图的节点上时，显示其当前父节点或集合代表元信息。
    *   **步骤解释**：每个主要步骤执行时，在信息面板显示简明的文字说明（例如：“检查边(B, D，权值4)。查找B属于集合{A,B,C}，查找D属于集合{D}。它们不在同一集合，因此可以加入。将集合{D}合并到集合{A,B,C}中。”）。
4.  **信息面板**：
    *   显示当前算法状态：已选边数/总需边数，当前生成树总权值。
    *   显示当前操作的详细日志。
    *   显示并查集的当前状态（如父节点数组）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>最小生成树：Kruskal算法教学动画</title>
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
            line-height: 1.6;
            padding: 20px;
            max-width: 1400px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #3498db;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
        }

        .main-view {
            flex: 3;
            min-width: 300px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            display: flex;
            flex-direction: column;
        }

        .side-panel {
            flex: 2;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .panel {
            background: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
        }

        .panel h2 {
            color: #3498db;
            margin-bottom: 15px;
            font-size: 1.4rem;
            border-bottom: 1px solid #eee;
            padding-bottom: 8px;
        }

        #graphCanvas {
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            background-color: #fdfdfd;
            flex-grow: 1;
            width: 100%;
            cursor: pointer;
        }

        .canvas-container {
            position: relative;
            flex-grow: 1;
            min-height: 400px;
        }

        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid #eee;
        }

        .btn {
            padding: 10px 18px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s ease;
            font-size: 0.95rem;
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
            background-color: #ecf0f1;
            color: #2c3e50;
        }

        .btn-secondary:hover {
            background-color: #d5dbdb;
        }

        .btn-success {
            background-color: #2ecc71;
            color: white;
        }

        .btn-success:hover {
            background-color: #27ae60;
        }

        .btn-warning {
            background-color: #f39c12;
            color: white;
        }

        .btn-warning:hover {
            background-color: #d68910;
        }

        .btn-danger {
            background-color: #e74c3c;
            color: white;
        }

        .btn-danger:hover {
            background-color: #c0392b;
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-left: auto;
        }

        .speed-control label {
            font-weight: 600;
            color: #7f8c8d;
        }

        #speedSlider {
            width: 120px;
        }

        .status-bar {
            display: flex;
            justify-content: space-between;
            background-color: #2c3e50;
            color: white;
            padding: 12px 20px;
            border-radius: 8px;
            margin-top: 10px;
            font-weight: 600;
        }

        .status-item {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .status-value {
            font-size: 1.4rem;
            color: #3498db;
        }

        .status-label {
            font-size: 0.9rem;
            color: #bdc3c7;
        }

        #edgeList {
            list-style-type: none;
            max-height: 200px;
            overflow-y: auto;
            border: 1px solid #eee;
            border-radius: 6px;
            padding: 10px;
        }

        .edge-item {
            padding: 8px 12px;
            margin-bottom: 5px;
            border-radius: 4px;
            display: flex;
            justify-content: space-between;
            transition: all 0.2s ease;
        }

        .edge-item.current {
            background-color: #fff9e6;
            border-left: 4px solid #f39c12;
            font-weight: 600;
        }

        .edge-item.selected {
            background-color: #e8f6f3;
            border-left: 4px solid #2ecc71;
        }

        .edge-item.rejected {
            background-color: #fdedec;
            border-left: 4px solid #e74c3c;
        }

        .edge-weight {
            font-weight: 600;
            color: #3498db;
        }

        #unionFindView {
            height: 200px;
            border: 1px solid #eee;
            border-radius: 6px;
            background-color: #fdfdfd;
            position: relative;
            overflow: auto;
        }

        .uf-node {
            position: absolute;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            transition: all 0.5s ease;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
        }

        .uf-edge {
            position: absolute;
            transition: all 0.5s ease;
        }

        #pseudocode {
            background-color: #2c3e50;
            color: #ecf0f1;
            padding: 15px;
            border-radius: 8px;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 0.95rem;
            line-height: 1.5;
            white-space: pre;
            overflow-x: auto;
            max-height: 300px;
            overflow-y: auto;
        }

        .code-line {
            padding: 2px 5px;
            border-radius: 3px;
            transition: background-color 0.3s ease;
        }

        .code-line.active {
            background-color: #3498db;
            color: white;
        }

        #logPanel {
            max-height: 200px;
            overflow-y: auto;
            border: 1px solid #eee;
            border-radius: 6px;
            padding: 10px;
            background-color: #f9f9f9;
            font-size: 0.9rem;
        }

        .log-entry {
            padding: 8px;
            margin-bottom: 5px;
            border-radius: 4px;
            border-left: 4px solid #3498db;
            background-color: white;
        }

        .log-entry.success {
            border-left-color: #2ecc71;
        }

        .log-entry.warning {
            border-left-color: #f39c12;
        }

        .log-entry.error {
            border-left-color: #e74c3c;
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
            font-size: 0.9rem;
        }

        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }

        .instructions {
            background-color: #e8f4fc;
            border-radius: 8px;
            padding: 15px;
            margin-top: 20px;
            border-left: 4px solid #3498db;
        }

        .instructions h3 {
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .instructions ul {
            padding-left: 20px;
        }

        .instructions li {
            margin-bottom: 5px;
        }

        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .controls {
                justify-content: center;
            }
            
            .speed-control {
                margin-left: 0;
                margin-top: 10px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>最小生成树：Kruskal算法教学动画</h1>
        <p class="subtitle">并查集 + 边排序加入 | 贪心算法可视化</p>
    </header>

    <div class="container">
        <div class="main-view">
            <h2>图可视化</h2>
            <div class="canvas-container">
                <canvas id="graphCanvas" width="800" height="500"></canvas>
            </div>
            
            <div class="controls">
                <button id="resetBtn" class="btn btn-secondary">重置</button>
                <button id="prevBtn" class="btn btn-secondary">上一步</button>
                <button id="nextBtn" class="btn btn-primary">下一步</button>
                <button id="playBtn" class="btn btn-success">播放</button>
                <button id="skipToEndBtn" class="btn btn-warning">跳到结束</button>
                
                <div class="speed-control">
                    <label for="speedSlider">速度:</label>
                    <input type="range" id="speedSlider" min="1" max="10" value="5">
                </div>
            </div>
            
            <div class="status-bar">
                <div class="status-item">
                    <span class="status-value" id="selectedEdgesCount">0</span>
                    <span class="status-label">已选边数</span>
                </div>
                <div class="status-item">
                    <span class="status-value" id="totalWeight">0</span>
                    <span class="status-label">总权值</span>
                </div>
                <div class="status-item">
                    <span class="status-value" id="currentStep">0</span>
                    <span class="status-label">当前步骤</span>
                </div>
                <div class="status-item">
                    <span class="status-value" id="edgesProcessed">0</span>
                    <span class="status-label">已处理边</span>
                </div>
            </div>
        </div>
        
        <div class="side-panel">
            <div class="panel">
                <h2>边列表（已排序）</h2>
                <ul id="edgeList"></ul>
            </div>
            
            <div class="panel">
                <h2>并查集可视化</h2>
                <div id="unionFindView"></div>
            </div>
            
            <div class="panel">
                <h2>算法伪代码</h2>
                <div id="pseudocode"></div>
            </div>
            
            <div class="panel">
                <h2>操作日志</h2>
                <div id="logPanel"></div>
            </div>
        </div>
    </div>
    
    <div class="legend">
        <div class="legend-item">
            <div class="legend-color" style="background-color: #95a5a6;"></div>
            <span>未处理边</span>
        </div>
        <div class="legend-item">
            <div class="legend-color" style="background-color: #e67e22;"></div>
            <span>当前处理边</span>
        </div>
        <div class="legend-item">
            <div class="legend-color" style="background-color: #2ecc71;"></div>
            <span>已选入生成树</span>
        </div>
        <div class="legend-item">
            <div class="legend-color" style="background-color: #e74c3c;"></div>
            <span>拒绝（成环）</span>
        </div>
        <div class="legend-item">
            <div class="legend-color" style="background-color: #9b59b6;"></div>
            <span>并查集集合</span>
        </div>
    </div>
    
    <div class="instructions">
        <h3>使用说明</h3>
        <ul>
            <li>点击<b>下一步</b>按钮逐步执行Kruskal算法</li>
            <li>使用<b>播放</b>按钮自动执行算法，可使用滑块调整速度</li>
            <li>观察并查集如何判断是否形成环</li>
            <li>已排序的边列表显示当前处理的边状态</li>
            <li>伪代码区域高亮显示当前执行的代码行</li>
            <li>操作日志记录算法的每一步决策</li>
        </ul>
    </div>

    <script>
        // 初始化图数据
        const graph = {
            vertices: ['A', 'B', 'C', 'D', 'E', 'F'],
            edges: [
                {from: 'A', to: 'B', weight: 4},
                {from: 'A', to: 'C', weight: 4},
                {from: 'B', to: 'C', weight: 2},
                {from: 'C', to: 'D', weight: 3},
                {from: 'C', to: 'E', weight: 2},
                {from: 'C', to: 'F', weight: 4},
                {from: 'D', to: 'F', weight: 3},
                {from: 'E', to: 'F', weight: 3}
            ]
        };

        // 算法状态
        let state = {
            currentStep: 0,
            selectedEdges: [],
            unionFind: {},
            sortedEdges: [],
            processedEdges: 0,
            totalWeight: 0,
            isPlaying: false,
            playSpeed: 500,
            history: [],
            currentEdgeIndex: 0
        };

        // 伪代码定义
        const pseudocode = [
            "function Kruskal(G):",
            "    // 初始化并查集，每个顶点单独一个集合",
            "    for each vertex v in G.vertices:",
            "        makeSet(v)",
            "    ",
            "    // 将所有边按权值从小到大排序",
            "    edges = sort(G.edges by weight)",
            "    ",
            "    // 初始化最小生成树",
            "    MST = []",
            "    ",
            "    // 遍历所有边",
            "    for each edge (u, v, weight) in edges:",
            "        // 如果u和v不在同一集合（不会形成环）",
            "        if find(u) != find(v):",
            "            // 将边加入最小生成树",
            "            MST.add(edge)",
            "            // 合并两个集合",
            "            union(u, v)",
            "    ",
            "    return MST"
        ];

        // 初始化函数
        function init() {
            // 初始化并查集
            state.unionFind = {};
            graph.vertices.forEach(v => {
                state.unionFind[v] = {parent: v, rank: 0};
            });
            
            // 边排序
            state.sortedEdges = [...graph.edges].sort((a, b) => a.weight - b.weight);
            
            // 重置状态
            state.currentStep = 0;
            state.selectedEdges = [];
            state.processedEdges = 0;
            state.totalWeight = 0;
            state.currentEdgeIndex = 0;
            state.history = [];
            
            // 更新UI
            updateEdgeList();
            updatePseudocode();
            updateUnionFindView();
            updateStatus();
            clearLog();
            addLog("初始化完成。图有 " + graph.vertices.length + " 个顶点和 " + graph.edges.length + " 条边。", "info");
            addLog("边已按权值排序完成。", "info");
            
            // 绘制初始图
            drawGraph();
        }

        // 绘制图
        function drawGraph() {
            const canvas = document.getElementById('graphCanvas');
            const ctx = canvas.getContext('2d');
            
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 计算顶点位置（圆形布局）
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const radius = Math.min(canvas.width, canvas.height) * 0.35;
            const vertexPositions = {};
            
            // 绘制边
            graph.edges.forEach(edge => {
                const fromIdx = graph.vertices.indexOf(edge.from);
                const toIdx = graph.vertices.indexOf(edge.to);
                
                const angleFrom = (fromIdx / graph.vertices.length) * 2 * Math.PI;
                const angleTo = (toIdx / graph.vertices.length) * 2 * Math.PI;
                
                const x1 = centerX + radius * Math.cos(angleFrom - Math.PI/2);
                const y1 = centerY + radius * Math.sin(angleFrom - Math.PI/2);
                const x2 = centerX + radius * Math.cos(angleTo - Math.PI/2);
                const y2 = centerY + radius * Math.sin(angleTo - Math.PI/2);
                
                // 保存顶点位置
                if (!vertexPositions[edge.from]) {
                    vertexPositions[edge.from] = {x: x1, y: y1};
                }
                if (!vertexPositions[edge.to]) {
                    vertexPositions[edge.to] = {x: x2, y: y2};
                }
                
                // 确定边的颜色和宽度
                let color = '#95a5a6'; // 默认灰色
                let width = 1;
                
                // 检查是否是当前处理的边
                if (state.currentEdgeIndex < state.sortedEdges.length) {
                    const currentEdge = state.sortedEdges[state.currentEdgeIndex];
                    if (edge.from === currentEdge.from && edge.to === currentEdge.to && 
                        edge.weight === currentEdge.weight) {
                        color = '#e67e22'; // 当前处理边 - 橙色
                        width = 3;
                    }
                }
                
                // 检查是否已选入生成树
                const isSelected = state.selectedEdges.some(e => 
                    (e.from === edge.from && e.to === edge.to) || 
                    (e.from === edge.to && e.to === edge.from));
                
                if (isSelected) {
                    color = '#2ecc71'; // 已选边 - 绿色
                    width = 4;
                }
                
                // 绘制边
                ctx.beginPath();
                ctx.moveTo(x1, y1);
                ctx.lineTo(x2, y2);
                ctx.strokeStyle = color;
                ctx.lineWidth = width;
                ctx.stroke();
                
                // 绘制权值
                const midX = (x1 + x2) / 2;
                const midY = (y1 + y2) / 2;
                ctx.fillStyle = '#2c3e50';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(edge.weight, midX, midY - 5);
            });
            
            // 绘制顶点
            graph.vertices.forEach((vertex, idx) => {
                const angle = (idx / graph.vertices.length) * 2 * Math.PI;
                const x = centerX + radius * Math.cos(angle - Math.PI/2);
                const y = centerY + radius * Math.sin(angle - Math.PI/2);
                
                // 保存位置
                vertexPositions[vertex] = {x, y};
                
                // 绘制顶点圆圈
                ctx.beginPath();
                ctx.arc(x, y, 20, 0, Math.PI * 2);
                ctx.fillStyle = '#3498db';
                ctx.fill();
                ctx.strokeStyle = '#2980b9';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 绘制顶点标签
                ctx.fillStyle = 'white';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(vertex, x, y);
                
                // 绘制并查集父节点（如果不同）
                if (state.unionFind[vertex] && state.unionFind[vertex].parent !== vertex) {
                    ctx.fillStyle = '#9b59b6';
                    ctx.font = '12px Arial';
                    ctx.fillText('→' + state.unionFind[vertex].parent, x, y + 25);
                }
            });
            
            // 保存顶点位置供其他函数使用
            window.vertexPositions = vertexPositions;
        }

        // 更新边列表
        function updateEdgeList() {
            const edgeList = document.getElementById('edgeList');
            edgeList.innerHTML = '';
            
            state.sortedEdges.forEach((edge, idx) => {
                const li = document.createElement('li');
                li.className = 'edge-item';
                
                // 设置状态类
                if (idx === state.currentEdgeIndex) {
                    li.classList.add('current');
                } else if (idx < state.currentEdgeIndex) {
                    const isSelected = state.selectedEdges.some(e => 
                        (e.from === edge.from && e.to === edge.to) || 
                        (e.from === edge.to && e.to === edge.from));
                    
                    if (isSelected) {
                        li.classList.add('selected');
                    } else {
                        li.classList.add('rejected');
                    }
                }
                
                li.innerHTML = `
                    <span>${edge.from} ↔ ${edge.to}</span>
                    <span class="edge-weight">权值: ${edge.weight}</span>
                `;
                
                edgeList.appendChild(li);
            });
        }

        // 更新并查集可视化
        function updateUnionFindView() {
            const container = document.getElementById('unionFindView');
            container.innerHTML = '';
            
            // 找出所有集合的代表元
            const sets = {};
            graph.vertices.forEach(v => {
                const root = find(v);
                if (!sets[root]) {
                    sets[root] = [];
                }
                sets[root].push(v);
            });
            
            // 计算布局
            const setKeys = Object.keys(sets);
            const containerWidth = container.clientWidth;
            const containerHeight = container.clientHeight;
            const setWidth = containerWidth / Math.max(setKeys.length, 1);
            
            // 绘制每个集合
            setKeys.forEach((root, setIndex) => {
                const vertices = sets[root];
                const setX = setIndex * setWidth + setWidth / 2;
                
                // 绘制集合标题
                const title = document.createElement('div');
                title.style.position = 'absolute';
                title.style.left = (setX - 30) + 'px';
                title.style.top = '10px';
                title.style.color = '#9b59b6';
                title.style.fontWeight = 'bold';
                title.textContent = `集合 ${root}`;
                container.appendChild(title);
                
                // 绘制集合中的顶点
                vertices.forEach((vertex, vertexIndex) => {
                    const node = document.createElement('div');
                    node.className = 'uf-node';
                    node.textContent = vertex;
                    node.style.left = (setX - 20 + (vertexIndex - vertices.length/2) * 50) + 'px';
                    node.style.top = (60 + vertexIndex * 10) + 'px';
                    
                    // 设置颜色
                    if (vertex === root) {
                        node.style.backgroundColor = '#9b59b6'; // 集合代表元
                        node.style.color = 'white';
                    } else {
                        node.style.backgroundColor = '#e8d4f4'; // 集合成员
                        node.style.color = '#2c3e50';
                    }
                    
                    // 如果当前正在处理这个顶点，添加高亮
                    if (state.currentEdgeIndex < state.sortedEdges.length) {
                        const currentEdge = state.sortedEdges[state.currentEdgeIndex];
                        if (vertex === currentEdge.from || vertex === currentEdge.to) {
                            node.style.boxShadow = '0 0 0 3px #f39c12';
                        }
                    }
                    
                    // 显示父节点（如果不是代表元）
                    if (state.unionFind[vertex].parent !== vertex) {
                        const parentLabel = document.createElement('div');
                        parentLabel.style.position = 'absolute';
                        parentLabel.style.left = '0';
                        parentLabel.style.bottom = '-20px';
                        parentLabel.style.fontSize = '10px';
                        parentLabel.style.color = '#7f8c8d';
                        parentLabel.textContent = `→${state.unionFind[vertex].parent}`;
                        node.appendChild(parentLabel);
                    }
                    
                    container.appendChild(node);
                });
            });
        }

        // 更新伪代码高亮
        function updatePseudocode() {
            const pseudocodeDiv = document.getElementById('pseudocode');
            pseudocodeDiv.innerHTML = '';
            
            // 确定当前高亮的行
            let highlightLine = -1;
            if (state.currentStep === 0) {
                highlightLine = 0; // 初始化
            } else if (state.currentStep === 1) {
                highlightLine = 1; // 初始化并查集
            } else if (state.currentStep === 2) {
                highlightLine = 4; // 排序边
            } else if (state.currentStep >= 3) {
                // 处理边的循环
                if (state.currentEdgeIndex < state.sortedEdges.length) {
                    highlightLine = 9; // for循环
                    
                    const currentEdge = state.sortedEdges[state.currentEdgeIndex];
                    const root1 = find(currentEdge.from);
                    const root2 = find(currentEdge.to);
                    
                    if (root1 === root2) {
                        highlightLine = 10; // if条件（不成立）
                    } else {
                        highlightLine = 11; // if条件（成立）
                    }
                } else {
                    highlightLine = 15; // 返回结果
                }
            }
            
            // 渲染伪代码
            pseudocode.forEach((line, index) => {
                const lineDiv = document.createElement('div');
                lineDiv.className = 'code-line';
                lineDiv.textContent = line;
                
                if (index === highlightLine) {
                    lineDiv.classList.add('active');
                }
                
                pseudocodeDiv.appendChild(lineDiv);
            });
        }

        // 更新状态栏
        function updateStatus() {
            document.getElementById('selectedEdgesCount').textContent = state.selectedEdges.length;
            document.getElementById('totalWeight').textContent = state.totalWeight;
            document.getElementById('currentStep').textContent = state.currentStep;
            document.getElementById('edgesProcessed').textContent = state.processedEdges;
        }

        // 添加日志
        function addLog(message, type = 'info') {
            const logPanel = document.getElementById('logPanel');
            const logEntry = document.createElement('div');
            logEntry.className = `log-entry ${type}`;
            
            const timestamp = new Date().toLocaleTimeString();
            logEntry.innerHTML = `<strong>[${timestamp}]</strong> ${message}`;
            
            logPanel.appendChild(logEntry);
            logPanel.scrollTop = logPanel.scrollHeight;
        }

        // 清除日志
        function clearLog() {
            document.getElementById('logPanel').innerHTML = '';
        }

        // 并查集操作：查找
        function find(vertex) {
            if (state.unionFind[vertex].parent !== vertex) {
                // 路径压缩（简化可视化，实际算法中常用）
                state.unionFind[vertex].parent = find(state.unionFind[vertex].parent);
            }
            return state.unionFind[vertex].parent;
        }

        // 并查集操作：合并
        function union(vertex1, vertex2) {
            const root1 = find(vertex1);
            const root2 = find(vertex2);
            
            if (root1 !== root2) {
                // 按秩合并
                if (state.unionFind[root1].rank < state.unionFind[root2].rank) {
                    state.unionFind[root1].parent = root2;
                } else if (state.unionFind[root1].rank > state.unionFind[root2].rank) {
                    state.unionFind[root2].parent = root1;
                } else {
                    state.unionFind[root2].parent = root1;
                    state.unionFind[root1].rank++;
                }
                return true;
            }
            return false;
        }

        // 执行下一步
        function nextStep() {
            // 保存当前状态到历史记录
            state.history.push({
                selectedEdges: [...state.selectedEdges],
                unionFind: JSON.parse(JSON.stringify(state.unionFind)),
                currentEdgeIndex: state.currentEdgeIndex,
                processedEdges: state.processedEdges,
                totalWeight: state.totalWeight
            });
            
            state.currentStep++;
            
            // 算法步骤
            if (state.currentStep === 1) {
                addLog("步骤 1: 初始化并查集，每个顶点单独一个集合", "info");
            } else if (state.currentStep === 2) {
                addLog("步骤 2: 将所有边按权值从小到大排序", "info");
            } else if (state.currentStep >= 3) {
                // 处理边
                if (state.currentEdgeIndex < state.sortedEdges.length) {
                    const edge = state.sortedEdges[state.currentEdgeIndex];
                    addLog(`步骤 ${state.currentStep}: 处理边 ${edge.from}-${edge.to} (权值: ${edge.weight})`, "warning");
                    
                    // 查找两个顶点的根节点
                    const root1 = find(edge.from);
                    const root2 = find(edge.to);
                    
                    addLog(`查找 ${edge.from} 的根节点: ${root1}, 查找 ${edge.to} 的根节点: ${root2}`, "info");
                    
                    if (root1 === root2) {
                        addLog(`${edge.from} 和 ${edge.to} 在同一集合中，加入此边会形成环，跳过此边`, "error");
                    } else {
                        // 加入边到最小生成树
                        state.selectedEdges.push(edge);
                        state.totalWeight += edge.weight;
                        union(edge.from, edge.to);
                        addLog(`将边 ${edge.from}-${edge.to} 加入最小生成树，合并集合 ${root1} 和 ${root2}`, "success");
                    }
                    
                    state.processedEdges++;
                    state.currentEdgeIndex++;
                    
                    // 检查是否完成
                    if (state.selectedEdges.length === graph.vertices.length - 1) {
                        addLog(`算法完成！找到最小生成树，包含 ${state.selectedEdges.length} 条边，总权值: ${state.totalWeight}`, "success");
                    }
                } else {
                    addLog("所有边已处理完毕", "info");
                }
            }
            
            // 更新UI
            updateEdgeList();
            updatePseudocode();
            updateUnionFindView();
            updateStatus();
            drawGraph();
            
            // 如果正在播放且未完成，继续下一步
            if (state.isPlaying && state.currentEdgeIndex < state.sortedEdges.length && 
                state.selectedEdges.length < graph.vertices.length - 1) {
                setTimeout(nextStep, 1000 - (state.playSpeed * 100));
            } else if (state.isPlaying) {
                // 算法完成，停止播放
                state.isPlaying = false;
                document.getElementById('playBtn').textContent = '播放';
                addLog("算法执行完成，自动播放停止", "info");
            }
        }

        // 执行上一步
        function prevStep() {
            if (state.history.length > 0) {
                const prevState = state.history.pop();
                state.selectedEdges = prevState.selectedEdges;
                state.unionFind = prevState.unionFind;
                state.currentEdgeIndex = prevState.currentEdgeIndex;
                state.processedEdges = prevState.processedEdges;
                state.totalWeight = prevState.totalWeight;
                state.currentStep--;
                
                // 更新UI
                updateEdgeList();
                updatePseudocode();
                updateUnionFindView();
                updateStatus();
                drawGraph();
                
                addLog("回退到上一步", "info");
            } else {
                addLog("已在第一步，无法回退", "error");
            }
        }

        // 事件监听器
        document.getElementById('resetBtn').addEventListener('click', () => {
            init();
            addLog("重置算法", "info");
        });

        document.getElementById('prevBtn').addEventListener('click', prevStep);

        document.getElementById('nextBtn').addEventListener('click', nextStep);

        document.getElementById('playBtn').addEventListener('click', () => {
            if (state.isPlaying) {
                state.isPlaying = false;
                document.getElementById('playBtn').textContent = '播放';
                addLog("暂停播放", "info");
            } else {
                state.isPlaying = true;
                document.getElementById('playBtn').textContent = '暂停';
                addLog("开始自动播放", "info");
                nextStep();
            }
        });

        document.getElementById('skipToEndBtn').addEventListener('click', () => {
            addLog("快速执行到算法结束", "warning");
            while (state.currentEdgeIndex < state.sortedEdges.length && 
                   state.selectedEdges.length < graph.vertices.length - 1) {
                // 这里简化处理，直接执行算法而不记录每一步历史
                const edge = state.sortedEdges[state.currentEdgeIndex];
                const root1 = find(edge.from);
                const root2 = find(edge.to);
                
                if (root1 !== root2) {
                    state.selectedEdges.push(edge);
                    state.totalWeight += edge.weight;
                    union(edge.from, edge.to);
                }
                
                state.processedEdges++;
                state.currentEdgeIndex++;
                state.currentStep++;
            }
            
            // 更新UI
            updateEdgeList();
            updatePseudocode();
            updateUnionFindView();
            updateStatus();
            drawGraph();
            
            addLog(`算法快速执行完成！最小生成树包含 ${state.selectedEdges.length} 条边，总权值: ${state.totalWeight}`, "success");
            
            // 如果正在播放，停止
            if (state.isPlaying) {
                state.isPlaying = false;
                document.getElementById('playBtn').textContent = '播放';
            }
        });

        document.getElementById('speedSlider').addEventListener('input', (e) => {
            state.playSpeed = parseInt(e.target.value);
        });

        // 初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 交互式教学动画使用指南

欢迎使用《最小生成树：Kruskal算法教学动画》！本指南将帮助您充分利用这个交互式学习工具，深入理解Kruskal算法的核心原理和实现细节。

---

### 一、功能说明

本动画是一个完整的HTML5交互式教学工具，通过多视图联动的方式，动态展示Kruskal算法从带权无向图中构建最小生成树的全过程。它特别强调了并查集在判断环中的关键作用，以及贪心策略（按权值排序边）的实现逻辑。

### 二、主要功能

#### 1. **核心控制面板**
   - **重置**：将动画恢复到初始状态，重新开始算法演示。
   - **上一步/下一步**：手动控制算法执行节奏，适合仔细推敲每一步的变化。
   - **播放/暂停**：自动连续执行算法步骤，适合观察整体流程。
   - **速度调节滑块**：在自动播放时，控制步骤间的间隔时间（1-10档可调）。
   - **跳到结束**：快速执行完所有算法步骤，直接查看最终的最小生成树结果。

#### 2. **多视图展示区**
   - **图可视化区**：直观展示带权无向图的结构。顶点用蓝色圆点表示，边根据其状态（未处理、当前处理、已选入、被拒绝）以不同颜色和粗细显示。
   - **边列表区**：显示所有边按权值从小到大排序后的列表。列表项会根据其处理状态（当前处理、已选入、被拒绝）高亮显示。
   - **并查集可视化区**：以集合树的形式动态展示并查集的状态变化。集合代表元（根节点）用紫色高亮显示，集合成员用浅紫色显示。当执行`Find`或`Union`操作时，可以直观看到集合的合并过程。
   - **算法伪代码区**：同步高亮当前正在执行的伪代码行，建立算法逻辑与视觉动画的直接映射。
   - **操作日志区**：记录算法的每一步决策和状态变化，包括查找根节点、判断是否成环、合并集合等关键信息。

#### 3. **状态监控面板**
   - 实时显示**已选边数**、**总权值**、**当前步骤**和**已处理边数**，帮助您把握算法进度。

### 三、设计特色

1. **认知负荷优化**：通过颜色编码（灰-未处理、橙-当前、绿-通过、红-拒绝、紫-并查集）和分步高亮，将复杂的算法过程分解为易于理解的视觉单元。
2. **多视图同步联动**：图视图、边列表、并查集视图和伪代码视图始终保持同步更新，帮助您建立不同抽象层次之间的联系。
3. **探索式学习**：支持手动控制节奏，鼓励您在关键步骤（如判断是否成环）暂停思考，再通过动画验证自己的判断。
4. **正反例对比**：不仅展示成功加入生成树的边，也清晰展示因构成环而被拒绝的边，强化对算法判断条件的理解。
5. **完整的算法轨迹**：通过“上一步”功能和操作日志，您可以回溯算法的任何一步，深入分析决策过程。

### 四、教学要点

#### 核心概念可视化
- **贪心策略**：观察边列表如何从一开始就按权值排序，理解“每次选择当前最小权值边”的贪心思想。
- **环的判断**：重点关注并查集视图的变化。当尝试加入一条边时，如果它的两个端点已经在同一集合中（有相同的根节点），则加入后会形成环，必须跳过。
- **集合的合并**：当一条边被成功加入时，观察两个端点所在集合如何合并为一个新的集合，这是并查集`Union`操作的可视化体现。
- **路径压缩示意**：在顶点旁显示的“→父节点”标签，帮助理解并查集中路径压缩的概念。

#### 推荐学习路径
1. **初次接触**：点击“播放”按钮，以中等速度观看完整的算法执行过程，建立整体印象。
2. **逐步深入**：使用“下一步”按钮，手动执行算法。在每一步暂停，尝试预测下一条边是否会被加入，并观察并查集的状态变化。
3. **重点分析**：遇到被拒绝的边时，仔细分析为什么它会形成环。观察此时两个端点在并查集中是否属于同一集合。
4. **反向验证**：算法结束后，使用“上一步”功能回溯，特别关注那些被拒绝的边，加深对环判断条件的理解。
5. **联系代码**：将伪代码高亮与动画步骤对应起来，理解每一行代码对应的实际操作。

### 五、使用建议

#### 给学习者
- **先思考，后验证**：在点击“下一步”前，先尝试判断当前边是否应该加入生成树，并思考原因。
- **关注并查集**：Kruskal算法的精髓在于并查集的应用。请将至少一半的注意力放在并查集可视化区域，理解`Find`和`Union`操作如何工作。
- **利用日志**：操作日志不仅记录结果，也解释了决策原因。当对某一步有疑问时，查看日志中的详细说明。
- **多次尝试**：重置动画，尝试用不同的速度或控制方式多次观看，每次关注不同的重点（如只看并查集变化，或只看边选择过程）。

#### 给教师/教学者
- **课堂演示**：本工具适合在讲解Kruskal算法时作为课堂演示材料。可以手动控制节奏，配合讲解逐步展开。
- **设置思考题**：在关键步骤暂停，向学生提问：“下一条边会被加入吗？为什么？”鼓励学生先根据并查集状态做出判断。
- **对比教学**：可与Prim算法的可视化工具对比使用，帮助学生理解两种最小生成树算法的异同。
- **代码关联**：将伪代码与实际编程语言（如Python、Java）的Kruskal算法实现代码对照讲解，帮助学生从可视化理解过渡到代码实现。

---

**开始探索吧！** 通过这个交互式工具，您将不仅仅“知道”Kruskal算法的步骤，更能“看见”并查集如何巧妙地避免环的形成，深入理解贪心策略在图算法中的应用。祝您学习愉快，收获满满！