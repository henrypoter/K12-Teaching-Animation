# 需求：Kruskal算法并查集路径压缩+按秩合并

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户是学习数据结构与算法（如计算机科学、软件工程专业）的大学生或自学者。他们已了解图的基本概念和最小生成树问题，但对Kruskal算法中高效判断连通性的并查集（Union-Find）数据结构，特别是其优化技巧（路径压缩和按秩合并）感到抽象和困惑。
*   **核心痛点**：理解并查集如何工作，以及两种优化策略如何将操作效率提升至近乎常数时间。
*   **学习目标**：
    1.  **理解**：掌握并查集在Kruskal算法中“判断是否形成环”的核心作用。
    2.  **掌握**：理解并查集“查找”与“合并”的基本操作。
    3.  **深入**：可视化理解“路径压缩”如何扁平化树结构，以及“按秩合并”如何控制树高，从而理解优化的原理。
    4.  **应用**：能够将优化后的并查集与Kruskal算法流程结合起来，解决一个完整的最小生成树问题。
*   **形式需求**：需要一个**分步骤、可控制、可视化**的动画，允许学习者暂停、单步前进/后退、观察数据结构（数组、树形）的同步变化，以建立直观认知。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

1.  **核心概念解构**：
    *   **第一层：Kruskal算法流程**。按边权排序，依次尝试添加边，避免环。
    *   **第二层：并查集的核心作用**。用“代表元”（根节点）判断两个顶点是否已连通（属于同一集合）。`Find` 操作找根，`Union` 操作合并集合。
    *   **第三层：朴素并查集的问题**。可能退化成链，导致 `Find` 操作变慢。
    *   **第四层：优化策略**：
        *   **路径压缩**：在 `Find` 过程中，将查找路径上的所有节点直接指向根。
        *   **按秩合并**：在 `Union` 过程中，总是将较矮的树合并到较高的树下，以控制整体树高。

2.  **认知规律遵循**：
    *   **从具体到抽象**：先展示一个完整的、使用朴素并查集的Kruskal算法示例，让学习者看到效率问题。再引入优化，对比效果。
    *   **分而治之**：将动画分为几个模式或阶段：① 只看Kruskal流程与并查集基础操作；② 聚焦于 `Find` 与路径压缩；③ 聚焦于 `Union` 与按秩合并；④ 完整优化流程。
    *   **对比学习**：在关键步骤（如执行 `Find` ），可以并排展示“优化前”和“优化后”的树结构变化，突出差异。
    *   **及时反馈**：在用户交互（如点击“下一步”）后，动画变化需清晰，并伴有简短的文字说明当前步骤做了什么（例如：“查找节点5的根：5 -> 3 -> 1，找到根为1。应用路径压缩：将5和3直接指向根1。”）。

3.  **交互设计**：
    *   **主控面板**：提供“播放/暂停”、“下一步”、“上一步”、“重置”按钮，让用户完全控制节奏。
    *   **模式切换**：提供“学习模式”选择器，如“完整流程”、“仅看查找与压缩”、“仅看合并与按秩”。
    *   **步骤高亮与说明**：当前正在执行的算法步骤（如“尝试连接边(E, F)”）和并查集操作（如“执行 Find(F)”）应在界面显著位置用文字和颜色高亮显示。
    *   **交互式探索**：允许用户点击图中的某个节点，手动触发一次 `Find` 操作，观察路径压缩的过程；或选择两个节点，触发 `Union` 操作，观察按秩合并的决策过程。

4.  **视觉呈现**：
    *   **双视图布局**：
        *   **左侧：图与Kruskal过程视图**。展示带权无向图，已加入最小生成树的边用醒目颜色（如绿色）加粗显示，正在考虑的边用黄色闪烁，被拒绝的边（会成环）用灰色或红色显示。
        *   **右侧：并查集数据结构视图**。这是重点，采用**两种同步的表示法**：
            *   **树形表示**：直观展示节点间的父子关系（指向）。根节点特殊标记。路径压缩时，箭头会动态重绘。
            *   **数组表示**：显示 `parent[]` 和 `rank[]`（或 `size[]`）数组。数值变化与树形图同步，建立抽象数据结构与具体实现的联系。
    *   **动画与颜色编码**：
        *   **查找路径**：当执行 `Find(x)` 时，从节点 `x` 到根节点的路径用高亮颜色（如蓝色）依次点亮。
        *   **路径压缩**：路径点亮后，这些节点会“跳”向根节点，其父指针箭头动态改变指向根。
        *   **合并决策**：进行 `Union` 时，比较高亮两棵树的“秩”（或大小），并用文字提示合并决策（“树A的秩较小，将其根合并到树B的根下”）。
        *   **颜色统一**：属于同一个并查集集合的节点，在图视图和树视图中使用相同的浅色背景色，增强关联性。

#### 配色方案选择
*   **主色调**：选择一种专业、清晰、对色盲友好的配色。例如，使用 **“深蓝色 (#2c3e50)”** 作为界面背景或标题色，营造专注感。
*   **数据高亮色**：
    *   **当前操作/路径**：使用醒目的 **“亮蓝色 (#3498db)”** 或 **“青色 (#1abc9c)”**。
    *   **最小生成树边/有效集合**：使用 **“绿色 (#2ecc71)”** 表示成功、已确定的部分。
    *   **冲突/拒绝边**：使用 **“柔和的红色 (#e74c3c)”**。
    *   **待处理/中性状态**：使用 **“浅灰色 (#bdc3c7)”**。
*   **视图背景**：
    *   图视图和并查集视图背景使用 **“白色”** 或 **“极浅的灰色 (#ecf0f1)”**，确保对比度。
    *   文本和线条使用 **“深灰色 (#34495e)”**，保证可读性。
*   **按钮与交互元素**：使用 **“主色调的变体”**，如深蓝色按钮搭配白色文字，悬停时变为亮蓝色。

#### 交互功能列表
1.  **核心控制**：
    *   播放/暂停 动画
    *   下一步 (Step Forward)
    *   上一步 (Step Backward)
    *   重置 (Reset) 到初始状态
    *   调节动画速度的滑块
2.  **学习模式选择**：
    *   **模式一：完整Kruskal算法**（默认）
    *   **模式二：聚焦Find与路径压缩**（自动或手动触发Find）
    *   **模式三：聚焦Union与按秩合并**（自动或手动触发Union）
3.  **视图控制**：
    *   显示/隐藏 并查集的树形图
    *   显示/隐藏 并查集的数组表示 (`parent[]`, `rank[]`)
    *   切换是否自动应用优化（可对比关闭/开启优化的效果）
4.  **交互式探索**：
    *   **点击节点**：在“聚焦Find”模式下，触发对该节点的 `Find` 操作，并展示过程。
    *   **选择两个节点**：在“聚焦Union”模式下，触发对这两个节点所在集合的 `Union` 操作，并展示决策与合并过程。
5.  **信息显示**：
    *   **步骤说明面板**：用文字描述当前Kruskal算法步骤及并查集操作。
    *   **数据面板**：实时显示边的排序列表、当前处理的边、并查集数组的当前值。
    *   **统计面板**：显示已进行的 `Find` 和 `Union` 操作次数，直观感受优化带来的效率提升（访问节点数减少）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kruskal算法与并查集优化教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #2c3e50;
            color: #34495e;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1600px;
            margin: 0 auto;
            background-color: #ecf0f1;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            overflow: hidden;
        }

        header {
            background-color: #3498db;
            color: white;
            padding: 25px 30px;
            text-align: center;
        }

        h1 {
            font-size: 2.2rem;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .subtitle {
            font-size: 1.1rem;
            opacity: 0.9;
            font-weight: 300;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            padding: 20px;
            gap: 20px;
        }

        .panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .graph-panel {
            flex: 1;
            min-width: 500px;
            min-height: 500px;
        }

        .data-structure-panel {
            flex: 1;
            min-width: 500px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .panel-title {
            color: #2c3e50;
            font-size: 1.4rem;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid #3498db;
            font-weight: 600;
        }

        .canvas-container {
            width: 100%;
            height: 450px;
            border: 2px solid #bdc3c7;
            border-radius: 8px;
            overflow: hidden;
            position: relative;
        }

        canvas {
            display: block;
            background-color: white;
        }

        .tree-view, .array-view {
            flex: 1;
        }

        .array-container {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-top: 10px;
        }

        .array-row {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .array-label {
            font-weight: bold;
            width: 80px;
            color: #2c3e50;
        }

        .array-cells {
            display: flex;
            gap: 5px;
            flex-wrap: wrap;
        }

        .cell {
            width: 50px;
            height: 50px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            border: 2px solid #bdc3c7;
            border-radius: 6px;
            background-color: white;
            transition: all 0.3s ease;
            position: relative;
        }

        .cell.index {
            background-color: #f8f9fa;
            font-weight: bold;
            color: #7f8c8d;
        }

        .cell.highlight {
            border-color: #3498db;
            background-color: #ebf5fb;
            box-shadow: 0 0 10px rgba(52, 152, 219, 0.3);
        }

        .cell-value {
            font-size: 1.2rem;
            font-weight: bold;
        }

        .cell-label {
            font-size: 0.8rem;
            color: #7f8c8d;
            margin-top: 2px;
        }

        .controls-panel {
            width: 100%;
            margin-top: 10px;
        }

        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            align-items: center;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .control-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .control-label {
            font-weight: 600;
            color: #2c3e50;
            font-size: 0.9rem;
        }

        .buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        button {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            background-color: #3498db;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            font-size: 0.95rem;
        }

        button:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }

        button:active {
            transform: translateY(0);
        }

        button:disabled {
            background-color: #bdc3c7;
            cursor: not-allowed;
            transform: none;
        }

        button.reset {
            background-color: #e74c3c;
        }

        button.reset:hover {
            background-color: #c0392b;
        }

        select {
            padding: 10px;
            border: 2px solid #bdc3c7;
            border-radius: 6px;
            background-color: white;
            color: #2c3e50;
            font-weight: 500;
            cursor: pointer;
            min-width: 200px;
        }

        select:focus {
            outline: none;
            border-color: #3498db;
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        input[type="range"] {
            width: 150px;
            height: 6px;
            -webkit-appearance: none;
            background: #bdc3c7;
            border-radius: 3px;
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
        }

        .info-panel {
            width: 100%;
            margin-top: 10px;
        }

        .info-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .step-info, .stats-info {
            flex: 1;
            min-width: 300px;
        }

        .info-title {
            color: #2c3e50;
            font-size: 1.2rem;
            margin-bottom: 10px;
            padding-bottom: 8px;
            border-bottom: 1px solid #3498db;
            font-weight: 600;
        }

        .step-description {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #3498db;
            font-size: 1.05rem;
            line-height: 1.5;
            min-height: 80px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }

        .stat-item {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            text-align: center;
        }

        .stat-label {
            font-size: 0.9rem;
            color: #7f8c8d;
            margin-bottom: 5px;
        }

        .stat-value {
            font-size: 1.8rem;
            font-weight: bold;
            color: #2c3e50;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding: 15px;
            background-color: #f8f9fa;
            border-radius: 8px;
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
            font-size: 0.9rem;
            color: #2c3e50;
        }

        .mst-edge { background-color: #2ecc71; }
        .candidate-edge { background-color: #f1c40f; }
        .rejected-edge { background-color: #e74c3c; }
        .normal-edge { background-color: #bdc3c7; }
        .find-path { background-color: #3498db; }
        .union-highlight { background-color: #9b59b6; }

        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
            
            .graph-panel, .data-structure-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Kruskal算法与并查集优化</h1>
            <div class="subtitle">路径压缩 + 按秩合并 - 交互式教学动画</div>
        </header>
        
        <div class="main-content">
            <div class="panel graph-panel">
                <h2 class="panel-title">图与Kruskal算法过程</h2>
                <div class="canvas-container">
                    <canvas id="graphCanvas" width="800" height="450"></canvas>
                </div>
            </div>
            
            <div class="data-structure-panel">
                <div class="panel tree-view">
                    <h2 class="panel-title">并查集 - 树形表示</h2>
                    <div class="canvas-container">
                        <canvas id="treeCanvas" width="800" height="200"></canvas>
                    </div>
                </div>
                
                <div class="panel array-view">
                    <h2 class="panel-title">并查集 - 数组表示</h2>
                    <div class="array-container">
                        <div class="array-row">
                            <div class="array-label">parent[]:</div>
                            <div class="array-cells" id="parentArray">
                                <!-- 动态生成 -->
                            </div>
                        </div>
                        <div class="array-row">
                            <div class="array-label">rank[]:</div>
                            <div class="array-cells" id="rankArray">
                                <!-- 动态生成 -->
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="controls-panel">
            <div class="controls">
                <div class="control-group">
                    <div class="control-label">核心控制</div>
                    <div class="buttons">
                        <button id="playPauseBtn">▶ 播放</button>
                        <button id="stepBtn">⏭ 下一步</button>
                        <button id="backBtn">⏮ 上一步</button>
                        <button id="resetBtn" class="reset">↺ 重置</button>
                    </div>
                </div>
                
                <div class="control-group">
                    <div class="control-label">学习模式</div>
                    <select id="modeSelect">
                        <option value="full">完整Kruskal算法</option>
                        <option value="find">聚焦Find与路径压缩</option>
                        <option value="union">聚焦Union与按秩合并</option>
                    </select>
                </div>
                
                <div class="control-group">
                    <div class="control-label">优化开关</div>
                    <div class="buttons">
                        <button id="togglePathCompression">路径压缩: 开启</button>
                        <button id="toggleUnionByRank">按秩合并: 开启</button>
                    </div>
                </div>
                
                <div class="control-group">
                    <div class="control-label">动画速度</div>
                    <div class="slider-container">
                        <span>慢</span>
                        <input type="range" id="speedSlider" min="1" max="10" value="5">
                        <span>快</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="info-panel">
            <div class="info-container">
                <div class="step-info">
                    <h3 class="info-title">当前步骤说明</h3>
                    <div class="step-description" id="stepDescription">
                        点击"播放"或"下一步"开始动画演示。初始状态：图中所有节点都是独立的集合。
                    </div>
                </div>
                
                <div class="stats-info">
                    <h3 class="info-title">统计信息</h3>
                    <div class="stats-grid">
                        <div class="stat-item">
                            <div class="stat-label">Find操作次数</div>
                            <div class="stat-value" id="findCount">0</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-label">Union操作次数</div>
                            <div class="stat-value" id="unionCount">0</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-label">已选MST边数</div>
                            <div class="stat-value" id="mstEdgeCount">0</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-label">总权重</div>
                            <div class="stat-value" id="totalWeight">0</div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color mst-edge"></div>
                    <div class="legend-text">最小生成树边</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color candidate-edge"></div>
                    <div class="legend-text">候选边</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color rejected-edge"></div>
                    <div class="legend-text">拒绝边（会成环）</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color find-path"></div>
                    <div class="legend-text">Find查找路径</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color union-highlight"></div>
                    <div class="legend-text">Union合并操作</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // ==================== 全局变量与配置 ====================
        const config = {
            nodeRadius: 25,
            nodeSpacing: 100,
            treeNodeRadius: 20,
            animationSpeed: 500, // 初始速度
            colors: {
                mstEdge: '#2ecc71',
                candidateEdge: '#f1c40f',
                rejectedEdge: '#e74c3c',
                normalEdge: '#bdc3c7',
                findPath: '#3498db',
                unionHighlight: '#9b59b6',
                nodeDefault: '#ecf0f1',
                nodeHighlight: '#3498db',
                nodeRoot: '#2ecc71',
                text: '#2c3e50'
            }
        };

        // 图数据结构
        const graph = {
            nodes: [
                {id: 0, x: 150, y: 150, label: 'A'},
                {id: 1, x: 350, y: 100, label: 'B'},
                {id: 2, x: 550, y: 150, label: 'C'},
                {id: 3, x: 150, y: 300, label: 'D'},
                {id: 4, x: 350, y: 250, label: 'E'},
                {id: 5, x: 550, y: 300, label: 'F'}
            ],
            edges: [
                {u: 0, v: 1, weight: 4},
                {u: 0, v: 3, weight: 2},
                {u: 1, v: 2, weight: 5},
                {u: 1, v: 3, weight: 10},
                {u: 1, v: 4, weight: 3},
                {u: 2, v: 4, weight: 6},
                {u: 2, v: 5, weight: 1},
                {u: 3, v: 4, weight: 7},
                {u: 4, v: 5, weight: 8}
            ]
        };

        // 并查集数据结构
        class UnionFind {
            constructor(size) {
                this.parent = Array.from({length: size}, (_, i) => i);
                this.rank = Array(size).fill(0);
                this.size = size;
            }
            
            // 查找根节点（带路径压缩）
            find(x, animate = false) {
                if (animate) {
                    this.highlightFindPath(x);
                }
                
                if (this.parent[x] !== x) {
                    // 路径压缩：将x的父节点直接设为根
                    this.parent[x] = this.find(this.parent[x]);
                }
                return this.parent[x];
            }
            
            // 合并两个集合（按秩合并）
            union(x, y, animate = false) {
                let rootX = this.find(x);
                let rootY = this.find(y);
                
                if (rootX === rootY) return false; // 已经在同一集合
                
                if (animate) {
                    this.highlightUnion(rootX, rootY);
                }
                
                // 按秩合并
                if (this.rank[rootX] < this.rank[rootY]) {
                    this.parent[rootX] = rootY;
                } else if (this.rank[rootX] > this.rank[rootY]) {
                    this.parent[rootY] = rootX;
                } else {
                    this.parent[rootY] = rootX;
                    this.rank[rootX]++;
                }
                
                return true;
            }
            
            highlightFindPath(x) {
                // 记录查找路径用于动画
                animationState.findPath = [];
                let current = x;
                while (this.parent[current] !== current) {
                    animationState.findPath.push(current);
                    current = this.parent[current];
                }
                animationState.findPath.push(current); // 加入根节点
            }
            
            highlightUnion(rootX, rootY) {
                animationState.unionNodes = [rootX, rootY];
            }
        }

        // 动画状态
        const animationState = {
            isPlaying: false,
            currentStep: 0,
            sortedEdges: [],
            mstEdges: [],
            rejectedEdges: [],
            currentEdgeIndex: -1,
            findPath: [],
            unionNodes: [],
            description: "",
            findCount: 0,
            unionCount: 0,
            mstEdgeCount: 0,
            totalWeight: 0,
            pathCompressionEnabled: true,
            unionByRankEnabled: true
        };

        // 初始化并查集
        let uf = new UnionFind(graph.nodes.length);

        // ==================== DOM元素引用 ====================
        const graphCanvas = document.getElementById('graphCanvas');
        const treeCanvas = document.getElementById('treeCanvas');
        const graphCtx = graphCanvas.getContext('2d');
        const treeCtx = treeCanvas.getContext('2d');
        const parentArrayEl = document.getElementById('parentArray');
        const rankArrayEl = document.getElementById('rankArray');
        const stepDescriptionEl = document.getElementById('stepDescription');
        const findCountEl = document.getElementById('findCount');
        const unionCountEl = document.getElementById('unionCount');
        const mstEdgeCountEl = document.getElementById('mstEdgeCount');
        const totalWeightEl = document.getElementById('totalWeight');
        
        // 控制按钮
        const playPauseBtn = document.getElementById('playPauseBtn');
        const stepBtn = document.getElementById('stepBtn');
        const backBtn = document.getElementById('backBtn');
        const resetBtn = document.getElementById('resetBtn');
        const modeSelect = document.getElementById('modeSelect');
        const togglePathCompressionBtn = document.getElementById('togglePathCompression');
        const toggleUnionByRankBtn = document.getElementById('toggleUnionByRank');
        const speedSlider = document.getElementById('speedSlider');

        // ==================== 初始化函数 ====================
        function init() {
            // 初始化边排序
            animationState.sortedEdges = [...graph.edges].sort((a, b) => a.weight - b.weight);
            
            // 初始化数组显示
            updateArrayDisplay();
            
            // 绘制初始状态
            drawGraph();
            drawTree();
            
            // 更新步骤说明
            updateStepDescription("初始化完成。图中包含6个节点和9条带权边。所有节点都是独立的集合。");
            
            // 设置事件监听器
            setupEventListeners();
        }

        function setupEventListeners() {
            playPauseBtn.addEventListener('click', togglePlayPause);
            stepBtn.addEventListener('click', nextStep);
            backBtn.addEventListener('click', previousStep);
            resetBtn.addEventListener('click', resetAnimation);
            
            modeSelect.addEventListener('change', changeMode);
            
            togglePathCompressionBtn.addEventListener('click', () => {
                animationState.pathCompressionEnabled = !animationState.pathCompressionEnabled;
                togglePathCompressionBtn.textContent = 
                    `路径压缩: ${animationState.pathCompressionEnabled ? '开启' : '关闭'}`;
            });
            
            toggleUnionByRankBtn.addEventListener('click', () => {
                animationState.unionByRankEnabled = !animationState.unionByRankEnabled;
                toggleUnionByRankBtn.textContent = 
                    `按秩合并: ${animationState.unionByRankEnabled ? '开启' : '关闭'}`;
            });
            
            speedSlider.addEventListener('input', (e) => {
                config.animationSpeed = 1000 - (e.target.value * 90); // 100ms 到 1000ms
            });
            
            // 画布点击交互
            graphCanvas.addEventListener('click', handleCanvasClick);
        }

        // ==================== 动画控制函数 ====================
        function togglePlayPause() {
            animationState.isPlaying = !animationState.isPlaying;
            playPauseBtn.textContent = animationState.isPlaying ? '⏸ 暂停' : '▶ 播放';
            
            if (animationState.isPlaying) {
                playAnimation();
            }
        }

        function playAnimation() {
            if (!animationState.isPlaying) return;
            
            if (animationState.currentStep < animationState.sortedEdges.length * 2) {
                nextStep();
                setTimeout(playAnimation, config.animationSpeed);
            } else {
                animationState.isPlaying = false;
                playPauseBtn.textContent = '▶ 播放';
            }
        }

        function nextStep() {
            const mode = modeSelect.value;
            
            if (mode === 'full') {
                performKruskalStep();
            } else if (mode === 'find') {
                performFindStep();
            } else if (mode === 'union') {
                performUnionStep();
            }
            
            updateArrayDisplay();
            drawGraph();
            drawTree();
            updateStats();
        }

        function previousStep() {
            // 简化实现：重置到初始状态然后重放直到上一步
            // 在实际应用中，这里应该实现一个历史栈
            alert("上一步功能需要更复杂的历史记录实现。请使用重置功能重新开始。");
        }

        function resetAnimation() {
            // 重置并查集
            uf = new UnionFind(graph.nodes.length);
            
            // 重置动画状态
            animationState.isPlaying = false;
            animationState.currentStep = 0;
            animationState.mstEdges = [];
            animationState.rejectedEdges = [];
            animationState.currentEdgeIndex = -1;
            animationState.findPath = [];
            animationState.unionNodes = [];
            animationState.findCount = 0;
            animationState.unionCount = 0;
            animationState.mstEdgeCount = 0;
            animationState.totalWeight = 0;
            
            // 重置按钮状态
            playPauseBtn.textContent = '▶ 播放';
            
            // 重新绘制
            updateArrayDisplay();
            drawGraph();
            drawTree();
            updateStepDescription("已重置到初始状态。所有节点都是独立的集合。");
            updateStats();
        }

        function changeMode() {
            resetAnimation();
        }

        // ==================== 算法步骤函数 ====================
        function performKruskalStep() {
            if (animationState.currentEdgeIndex >= animationState.sortedEdges.length - 1) {
                updateStepDescription("算法完成！已找到最小生成树。");
                animationState.isPlaying = false;
                playPauseBtn.textContent = '▶ 播放';
                return;
            }
            
            // 获取当前边
            animationState.currentEdgeIndex++;
            const edge = animationState.sortedEdges[animationState.currentEdgeIndex];
            
            // 清空高亮
            animationState.findPath = [];
            animationState.unionNodes = [];
            
            // 查找两个端点的根
            const rootU = uf.find(edge.u, true);
            animationState.findCount++;
            
            const rootV = uf.find(edge.v, true);
            animationState.findCount++;
            
            // 更新步骤说明
            updateStepDescription(`处理边 ${graph.nodes[edge.u].label}-${graph.nodes[edge.v].label} (权重: ${edge.weight})。查找根节点: ${graph.nodes[edge.u].label}→${graph.nodes[rootU].label}, ${graph.nodes[edge.v].label}→${graph.nodes[rootV].label}。`);
            
            // 检查是否形成环
            if (rootU === rootV) {
                animationState.rejectedEdges.push(edge);
                updateStepDescription(`根节点相同 (${graph.nodes[rootU].label})，添加此边会形成环，因此拒绝该边。`);
            } else {
                // 合并两个集合
                const merged = uf.union(edge.u, edge.v, true);
                if (merged) {
                    animationState.unionCount++;
                    animationState.mstEdges.push(edge);
                    animationState.mstEdgeCount++;
                    animationState.totalWeight += edge.weight;
                    updateStepDescription(`根节点不同，合并集合 ${graph.nodes[rootU].label} 和 ${graph.nodes[rootV].label}。将边加入最小生成树。`);
                }
            }
            
            animationState.currentStep++;
        }

        function performFindStep() {
            // 随机选择一个节点进行Find操作
            const randomNode = Math.floor(Math.random() * graph.nodes.length);
            const root = uf.find(randomNode, true);
            animationState.findCount++;
            
            updateStepDescription(`执行 Find(${graph.nodes[randomNode].label})。查找路径: ${animationState.findPath.map(id => graph.nodes[id].label).join(' → ')}。根节点: ${graph.nodes[root].label}。${animationState.pathCompressionEnabled ? '应用路径压缩优化。' : ''}`);
            
            animationState.currentStep++;
        }

        function performUnionStep() {
            // 随机选择两个不同节点进行Union操作
            let node1 = Math.floor(Math.random() * graph.nodes.length);
            let node2 = Math.floor(Math.random() * graph.nodes.length);
            while (node1 === node2) {
                node2 = Math.floor(Math.random() * graph.nodes.length);
            }
            
            const root1 = uf.find(node1);
            const root2 = uf.find(node2);
            
            if (root1 !== root2) {
                uf.union(node1, node2, true);
                animationState.unionCount++;
                
                const rank1 = uf.rank[root1];
                const rank2 = uf.rank[root2];
                
                let mergeDecision = "";
                if (rank1 < rank2) {
                    mergeDecision = `rank[${graph.nodes[root1].label}](${rank1}) < rank[${graph.nodes[root2].label}](${rank2})，将 ${graph.nodes[root1].label} 合并到 ${graph.nodes[root2].label}`;
                } else if (rank1 > rank2) {
                    mergeDecision = `rank[${graph.nodes[root1].label}](${rank1}) > rank[${graph.nodes[root2].label}](${rank2})，将 ${graph.nodes[root2].label} 合并到 ${graph.nodes[root1].label}`;
                } else {
                    mergeDecision = `rank[${graph.nodes[root1].label}](${rank1}) = rank[${graph.nodes[root2].label}](${rank2})，将 ${graph.nodes[root2].label} 合并到 ${graph.nodes[root1].label}，rank[${graph.nodes[root1].label}]++`;
                }
                
                updateStepDescription(`执行 Union(${graph.nodes[node1].label}, ${graph.nodes[node2].label})。根节点: ${graph.nodes[root1].label} 和 ${graph.nodes[root2].label}。${animationState.unionByRankEnabled ? `按秩合并决策: ${mergeDecision}` : '随机合并。'}`);
            } else {
                updateStepDescription(`执行 Union(${graph.nodes[node1].label}, ${graph.nodes[node2].label})。根节点相同 (${graph.nodes[root1].label})，已在同一集合，无需合并。`);
            }
            
            animationState.currentStep++;
        }

        // ==================== 绘图函数 ====================
        function drawGraph() {
            // 清空画布
            graphCtx.clearRect(0, 0, graphCanvas.width, graphCanvas.height);
            
            // 绘制边
            graph.edges.forEach(edge => {
                const nodeU = graph.nodes[edge.u];
                const nodeV = graph.nodes[edge.v];
                
                // 确定边的颜色
                let edgeColor = config.colors.normalEdge;
                let lineWidth = 2;
                
                // 检查边的状态
                const isMST = animationState.mstEdges.some(e => 
                    (e.u === edge.u && e.v === edge.v) || (e.u === edge.v && e.v === edge.u));
                const isRejected = animationState.rejectedEdges.some(e => 
                    (e.u === edge.u && e.v === edge.v) || (e.u === edge.v && e.v === edge.u));
                const isCurrent = animationState.currentEdgeIndex >= 0 && 
                    animationState.sortedEdges[animationState.currentEdgeIndex] === edge;
                
                if (isMST) {
                    edgeColor = config.colors.mstEdge;
                    lineWidth = 4;
                } else if (isRejected) {
                    edgeColor = config.colors.rejectedEdge;
                    lineWidth = 3;
                } else if (isCurrent) {
                    edgeColor = config.colors.candidateEdge;
                    lineWidth = 3;
                }
                
                // 绘制边
                graphCtx.beginPath();
                graphCtx.moveTo(nodeU.x, nodeU.y);
                graphCtx.lineTo(nodeV.x, nodeV.y);
                graphCtx.strokeStyle = edgeColor;
                graphCtx.lineWidth = lineWidth;
                graphCtx.stroke();
                
                // 绘制权重
                const midX = (nodeU.x + nodeV.x) / 2;
                const midY = (nodeU.y + nodeV.y) / 2;
                graphCtx.fillStyle = config.colors.text;
                graphCtx.font = 'bold 14px Arial';
                graphCtx.textAlign = 'center';
                graphCtx.textBaseline = 'middle';
                graphCtx.fillText(edge.weight.toString(), midX, midY - 5);
            });
            
            // 绘制节点
            graph.nodes.forEach((node, index) => {
                // 确定节点颜色
                let nodeColor = config.colors.nodeDefault;
                const isInFindPath = animationState.findPath.includes(index);
                const isInUnion = animationState.unionNodes.includes(index);
                const isRoot = uf.find(index) === index;
                
                if (isInFindPath) {
                    nodeColor = config.colors.findPath;
                } else if (isInUnion) {
                    nodeColor = config.colors.unionHighlight;
                } else if (isRoot) {
                    nodeColor = config.colors.nodeRoot;
                }
                
                // 绘制节点圆
                graphCtx.beginPath();
                graphCtx.arc(node.x, node.y, config.nodeRadius, 0, Math.PI * 2);
                graphCtx.fillStyle = nodeColor;
                graphCtx.fill();
                graphCtx.strokeStyle = config.colors.text;
                graphCtx.lineWidth = 2;
                graphCtx.stroke();
                
                // 绘制节点标签
                graphCtx.fillStyle = config.colors.text;
                graphCtx.font = 'bold 18px Arial';
                graphCtx.textAlign = 'center';
                graphCtx.textBaseline = 'middle';
                graphCtx.fillText(node.label, node.x, node.y);
                
                // 绘制节点ID（小字）
                graphCtx.font = '12px Arial';
                graphCtx.fillText(`id:${index}`, node.x, node.y + config.nodeRadius + 15);
            });
        }

        function drawTree() {
            // 清空画布
            treeCtx.clearRect(0, 0, treeCanvas.width, treeCanvas.height);
            
            // 计算树布局
            const treeLayout = calculateTreeLayout();
            
            // 绘制边（父指针）
            graph.nodes.forEach((node, i) => {
                const parent = uf.parent[i];
                if (parent !== i) { // 不是根节点
                    const childPos = treeLayout[i];
                    const parentPos = treeLayout[parent];
                    
                    // 绘制箭头线
                    treeCtx.beginPath();
                    treeCtx.moveTo(childPos.x, childPos.y + config.treeNodeRadius);
                    treeCtx.lineTo(parentPos.x, parentPos.y - config.treeNodeRadius);
                    
                    // 检查是否在查找路径中
                    const isInFindPath = animationState.findPath.includes(i) || 
                                       animationState.findPath.includes(parent);
                    
                    treeCtx.strokeStyle = isInFindPath ? config.colors.findPath : config.colors.text;
                    treeCtx.lineWidth = isInFindPath ? 3 : 2;
                    treeCtx.stroke();
                    
                    // 绘制箭头
                    drawArrow(treeCtx, childPos.x, childPos.y + config.treeNodeRadius, 
                             parentPos.x, parentPos.y - config.treeNodeRadius, 
                             isInFindPath ? config.colors.findPath : config.colors.text);
                }
            });
            
            // 绘制节点
            graph.nodes.forEach((node, i) => {
                const pos = treeLayout[i];
                const isRoot = uf.find(i) === i;
                const isInFindPath = animationState.findPath.includes(i);
                const isInUnion = animationState.unionNodes.includes(i);
                
                // 确定节点颜色
                let nodeColor = config.colors.nodeDefault;
                if (isInFindPath) {
                    nodeColor = config.colors.findPath;
                } else if (isInUnion) {
                    nodeColor = config.colors.unionHighlight;
                } else if (isRoot) {
                    nodeColor = config.colors.nodeRoot;
                }
                
                // 绘制节点圆
                treeCtx.beginPath();
                treeCtx.arc(pos.x, pos.y, config.treeNodeRadius, 0, Math.PI * 2);
                treeCtx.fillStyle = nodeColor;
                treeCtx.fill();
                treeCtx.strokeStyle = config.colors
<!--检测到代码截断，自动续写中...-->
.text;
                treeCtx.lineWidth = 2;
                treeCtx.stroke();
                
                // 绘制节点标签
                treeCtx.fillStyle = config.colors.text;
                treeCtx.font = 'bold 16px Arial';
                treeCtx.textAlign = 'center';
                treeCtx.textBaseline = 'middle';
                treeCtx.fillText(graph.nodes[i].label, pos.x, pos.y);
                
                // 绘制父指针信息
                treeCtx.font = '12px Arial';
                treeCtx.fillText(`→${graph.nodes[uf.parent[i]].label}`, pos.x, pos.y + config.treeNodeRadius + 15);
                
                // 如果是根节点，显示秩
                if (isRoot && uf.rank[i] > 0) {
                    treeCtx.fillStyle = '#e74c3c';
                    treeCtx.fillText(`rank=${uf.rank[i]}`, pos.x, pos.y - config.treeNodeRadius - 10);
                }
            });
        }

        function calculateTreeLayout() {
            // 简单的树布局算法
            const layout = [];
            const level = {};
            const nodesByLevel = {};
            
            // 计算每个节点的深度（到根的距离）
            for (let i = 0; i < graph.nodes.length; i++) {
                let depth = 0;
                let current = i;
                while (uf.parent[current] !== current) {
                    depth++;
                    current = uf.parent[current];
                }
                level[i] = depth;
                
                if (!nodesByLevel[depth]) nodesByLevel[depth] = [];
                nodesByLevel[depth].push(i);
            }
            
            // 计算位置
            const maxDepth = Math.max(...Object.values(level));
            const levelHeight = treeCanvas.height / (maxDepth + 2);
            
            for (let d = 0; d <= maxDepth; d++) {
                const nodes = nodesByLevel[d] || [];
                const nodeWidth = treeCanvas.width / (nodes.length + 1);
                
                nodes.forEach((nodeId, index) => {
                    layout[nodeId] = {
                        x: nodeWidth * (index + 1),
                        y: levelHeight * (d + 1)
                    };
                });
            }
            
            return layout;
        }

        function drawArrow(ctx, fromX, fromY, toX, toY, color) {
            const headlen = 10;
            const dx = toX - fromX;
            const dy = toY - fromY;
            const angle = Math.atan2(dy, dx);
            
            ctx.save();
            ctx.strokeStyle = color;
            ctx.fillStyle = color;
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headlen * Math.cos(angle - Math.PI / 6), 
                      toY - headlen * Math.sin(angle - Math.PI / 6));
            ctx.lineTo(toX - headlen * Math.cos(angle + Math.PI / 6), 
                      toY - headlen * Math.sin(angle + Math.PI / 6));
            ctx.closePath();
            ctx.fill();
            
            ctx.restore();
        }

        // ==================== 辅助函数 ====================
        function updateArrayDisplay() {
            // 更新parent数组显示
            parentArrayEl.innerHTML = '';
            
            // 索引行
            const indexRow = document.createElement('div');
            indexRow.className = 'array-row';
            const indexLabel = document.createElement('div');
            indexLabel.className = 'array-label';
            indexLabel.textContent = '索引:';
            indexRow.appendChild(indexLabel);
            
            const indexCells = document.createElement('div');
            indexCells.className = 'array-cells';
            
            for (let i = 0; i < graph.nodes.length; i++) {
                const cell = document.createElement('div');
                cell.className = 'cell index';
                cell.innerHTML = `<div class="cell-value">${i}</div><div class="cell-label">${graph.nodes[i].label}</div>`;
                indexCells.appendChild(cell);
            }
            
            indexRow.appendChild(indexCells);
            parentArrayEl.appendChild(indexRow);
            
            // 父指针行
            const parentRow = document.createElement('div');
            parentRow.className = 'array-row';
            
            const parentCells = document.createElement('div');
            parentCells.className = 'array-cells';
            
            for (let i = 0; i < uf.parent.length; i++) {
                const cell = document.createElement('div');
                cell.className = 'cell';
                if (animationState.findPath.includes(i) || animationState.unionNodes.includes(i)) {
                    cell.classList.add('highlight');
                }
                cell.innerHTML = `<div class="cell-value">${uf.parent[i]}</div><div class="cell-label">${graph.nodes[uf.parent[i]].label}</div>`;
                parentCells.appendChild(cell);
            }
            
            parentRow.appendChild(parentCells);
            parentArrayEl.appendChild(parentRow);
            
            // 更新rank数组显示
            rankArrayEl.innerHTML = '';
            
            const rankRow = document.createElement('div');
            rankRow.className = 'array-row';
            
            const rankCells = document.createElement('div');
            rankCells.className = 'array-cells';
            
            for (let i = 0; i < uf.rank.length; i++) {
                const cell = document.createElement('div');
                cell.className = 'cell';
                if (animationState.unionNodes.includes(i)) {
                    cell.classList.add('highlight');
                }
                cell.innerHTML = `<div class="cell-value">${uf.rank[i]}</div><div class="cell-label">${graph.nodes[i].label}</div>`;
                rankCells.appendChild(cell);
            }
            
            rankRow.appendChild(rankCells);
            rankArrayEl.appendChild(rankRow);
        }

        function updateStepDescription(text) {
            animationState.description = text;
            stepDescriptionEl.textContent = text;
        }

        function updateStats() {
            findCountEl.textContent = animationState.findCount;
            unionCountEl.textContent = animationState.unionCount;
            mstEdgeCountEl.textContent = animationState.mstEdgeCount;
            totalWeightEl.textContent = animationState.totalWeight;
        }

        function handleCanvasClick(event) {
            const rect = graphCanvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;
            
            // 检查点击了哪个节点
            for (let i = 0; i < graph.nodes.length; i++) {
                const node = graph.nodes[i];
                const distance = Math.sqrt((x - node.x) ** 2 + (y - node.y) ** 2);
                
                if (distance <= config.nodeRadius) {
                    // 根据模式执行不同操作
                    const mode = modeSelect.value;
                    
                    if (mode === 'find') {
                        // 执行Find操作
                        const root = uf.find(i, true);
                        animationState.findCount++;
                        
                        updateStepDescription(`手动触发 Find(${graph.nodes[i].label})。查找路径: ${animationState.findPath.map(id => graph.nodes[id].label).join(' → ')}。根节点: ${graph.nodes[root].label}。${animationState.pathCompressionEnabled ? '应用路径压缩优化。' : ''}`);
                        
                        updateArrayDisplay();
                        drawGraph();
                        drawTree();
                        updateStats();
                    }
                    break;
                }
            }
        }

        // ==================== 启动应用 ====================
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## Kruskal算法与并查集优化交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过可视化方式，帮助您深入理解Kruskal算法及其核心数据结构——并查集（Union-Find）的优化原理。无论您是初次接触此概念，还是希望巩固理解，本动画都将为您提供直观、互动的学习体验。

### 一、功能说明

本动画系统包含以下核心模块：

1. **双视图同步展示**
   - **左侧视图**：展示带权无向图及Kruskal算法的执行过程
   - **右侧视图**：同步展示并查集的两种表示形式（树形结构+数组表示）

2. **三种学习模式**
   - **完整Kruskal算法**：完整展示从排序边到构建最小生成树的全过程
   - **聚焦Find与路径压缩**：专注于并查集的查找操作及路径压缩优化
   - **聚焦Union与按秩合并**：专注于集合合并操作及按秩合并策略

3. **实时数据反馈**
   - 动态显示parent[]和rank[]数组的变化
   - 统计Find/Union操作次数、MST边数、总权重
   - 详细的步骤说明文字

### 二、主要功能

#### 控制面板功能
- **播放/暂停**：控制动画的自动播放
- **下一步/上一步**：手动控制算法步骤（上一步功能为简化实现）
- **重置**：恢复到初始状态重新开始
- **速度调节**：通过滑块控制动画播放速度（1-10档）

#### 学习模式切换
- **模式选择下拉框**：可在三种学习模式间自由切换
- **优化开关**：可独立开启/关闭“路径压缩”和“按秩合并”优化
  - 绿色按钮表示“开启”，灰色按钮表示“关闭”
  - 通过对比开启/关闭优化的效果，直观理解优化的重要性

#### 交互式探索
- **在“聚焦Find”模式下**：点击图中任意节点，手动触发对该节点的Find操作
- **可视化反馈**：查找路径、合并操作等关键步骤均有颜色高亮和动画效果

### 三、设计特色

#### 1. 认知友好的视觉设计
- **颜色编码系统**：
  - 绿色：最小生成树边、根节点（成功/确定状态）
  - 蓝色：Find查找路径（当前操作）
  - 紫色：Union合并操作
  - 黄色：当前候选边
  - 红色：被拒绝的边（会形成环）
  - 灰色：普通边/中性状态

- **同步更新机制**：
  - 图视图中的节点颜色与树视图中的节点颜色同步
  - 数组表示与树形表示实时对应更新
  - 所有视图中的同一集合使用相同背景色

#### 2. 渐进式学习路径
- **从整体到局部**：先看完整算法流程，再聚焦具体操作
- **从朴素到优化**：可对比开启/关闭优化时的性能差异
- **从观察到交互**：先观看自动演示，再通过点击进行探索

#### 3. 专业的数据结构展示
- **树形表示**：直观展示父子指针关系，动态显示路径压缩过程
- **数组表示**：展示parent[]和rank[]的实际存储，连接抽象概念与具体实现
- **统计面板**：量化展示操作次数，帮助理解算法复杂度

### 四、教学要点

#### 核心概念可视化
1. **并查集的基本操作**
   - **Find**：查找节点的根代表元，动画显示从节点到根的完整路径
   - **Union**：合并两个集合，动画显示秩的比较和合并决策过程

2. **优化策略原理**
   - **路径压缩**：在Find操作中，将路径上所有节点直接指向根，动画显示节点的“跳跃”过程
   - **按秩合并**：在Union操作中，总是将较矮的树合并到较高的树下，动画显示秩的比较逻辑

3. **Kruskal算法流程**
   - 边按权重排序
   - 依次尝试添加边，避免环的形成
   - 使用并查集高效判断连通性

#### 关键观察点
- 注意观察**路径压缩**时树结构如何从“链状”变为“星状”
- 关注**按秩合并**时如何根据rank值决定合并方向
- 比较开启/关闭优化时，Find操作的路径长度差异
- 观察MST构建过程中，并查集集合数量的变化规律

### 五、使用建议

#### 学习路径推荐
1. **初学者**：
   - 从“完整Kruskal算法”模式开始，观看1-2遍完整流程
   - 关注步骤说明文字，理解每个操作的目的
   - 使用“播放”功能观看自动演示

2. **进阶学习**：
   - 切换到“聚焦Find”模式，手动点击节点观察查找过程
   - 尝试关闭路径压缩，对比查找路径的变化
   - 切换到“聚焦Union”模式，观察按秩合并的决策逻辑

3. **深入理解**：
   - 同时关闭两种优化，观察最坏情况下的树退化
   - 统计不同配置下的Find操作次数，理解优化效果
   - 尝试预测下一步操作，然后通过“下一步”验证

#### 教学应用建议
- **课堂演示**：教师可使用本工具进行课堂实时演示
- **自主学习**：学生可按自己的节奏探索不同模式
- **实验对比**：可设计实验对比不同优化策略的效果

#### 最佳实践
1. **先看后做**：先观看完整演示，再尝试交互操作
2. **多问为什么**：在每个步骤暂停，思考“为什么这样操作？”
3. **对比学习**：主动对比不同配置下的算法行为
4. **联系实际**：思考并查集在其他场景（如社交网络连通性）的应用

#### 技术提示
- 本工具使用纯HTML5/CSS3/JavaScript实现，无需安装任何插件
- 建议使用Chrome、Firefox或Edge等现代浏览器
- 在移动设备上也可使用，但建议在桌面端获得最佳体验

---

**开始您的探索之旅吧！** 通过这个交互式动画，您将不仅理解Kruskal算法和并查集的工作原理，更能直观感受算法优化带来的巨大效率提升。祝您学习愉快，收获满满！

如有任何问题或建议，欢迎通过适当渠道反馈。本工具将持续改进，为算法学习者提供更好的可视化学习体验。