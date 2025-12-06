# 需求：拓扑排序（入度减0→队列弹出）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为学习数据结构与算法（如计算机科学、软件工程专业）的大学生或自学者。他们已具备图的基本概念（节点、边、有向图），但对拓扑排序的原理和过程感到抽象，难以在脑海中动态构建其执行流程。
2.  **核心痛点**：
    *   **过程动态性**：拓扑排序是一个逐步“移除”入度为0的节点的过程，静态的图示或文字描述难以清晰展示这一动态的、状态连续变化的过程。
    *   **数据结构联动**：算法涉及图（节点和边）的状态变化与队列（或栈）的联动，用户需要同时理解两个数据结构的协同工作。
    *   **“入度”概念可视化**：入度的实时计算和变化是理解算法的关键，需要直观地呈现。
3.  **学习目标**：通过动画，用户应能：
    *   清晰理解拓扑排序的定义和适用条件（有向无环图）。
    *   逐步跟踪并描述“基于入度的Kahn算法”的每一步操作。
    *   将屏幕上图的变化与队列的操作（入队、出队）在逻辑上关联起来。
    *   最终在脑海中形成“入度减0→入队→出队输出”的清晰算法图景。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念分解与串联**：
    *   **基石**：有向边（A->B）表示A必须先于B。**入度**是进入一个节点的边的数量。
    *   **算法核心循环**：
        1.  **初始**：找到所有入度为0的节点，放入队列。
        2.  **循环**：从队列中弹出一个节点，将其输出到结果序列。
        3.  **关键操作**：“删除”该节点及其所有出边（在算法中体现为将其所有邻居节点的入度减1）。
        4.  **状态检查**：若某个邻居节点入度因此变为0，则将其加入队列。
        5.  **终止**：重复2-4步，直到队列为空。若输出的节点数等于总节点数，则排序成功；否则，图中存在环。

2.  **遵循认知规律**：
    *   **从具体到抽象**：从一个具体的课程安排或任务依赖实例图开始，引出问题，再过渡到一般性的算法。
    *   **分步与聚焦**：动画必须严格一步步执行，每一步高亮当前操作的节点和边，并伴有清晰的文字说明。避免一次性展示过多变化。
    *   **双重编码**：同时利用视觉元素（图形、颜色、移动）和语言解释（步骤说明、状态提示）来强化记忆和理解。

3.  **交互设计**：
    *   **控制节奏**：提供“上一步”、“下一步”、“播放/暂停”按钮，让用户能以自己的速度学习，并可回溯观察。
    *   **探索与验证**：允许用户在预设的几个经典示例图（如简单线性、多分支、复杂依赖图）之间切换，甚至提供一个极简的“沙盒模式”，让用户手动添加节点和边，然后运行算法，以验证理解。
    *   **提示与反馈**：在关键步骤（如入度变为0时）有明确的视觉反馈（如颜色闪烁、音效）和文字提示。

4.  **视觉呈现**：
    *   **三区域布局**：
        *   **主视觉区**：展示有向图。节点内显示节点标识（如A，B）和实时**入度值**。边为有向箭头。
        *   **数据结构区**：清晰展示**队列（Queue）** 的状态变化（入队、出队动画）和**结果序列（Sorted Order）** 的逐步形成。
        *   **控制与日志区**：放置控制按钮，并实时输出当前步骤的文本描述（如：“将入度为0的节点A加入队列”）。
    *   **状态颜色编码**：
        *   **待处理节点**：中性色（如浅灰色）。
        *   **当前活动节点**：高亮色（如亮蓝色）。
        *   **已处理/已输出节点**：完成色（如绿色），并可能移至结果区或在主图中变灰。
        *   **队列中的节点**：特殊标识（如节点外框为橙色）。
        *   **正在被“删除”的边**：高亮后消失或变为虚线。

#### 配色方案选择
*   **主色调**：采用专业、清晰、对视力友好的配色。
    *   **背景**：浅灰色或白色，避免刺眼。
    *   **节点默认**：浅蓝色填充，深蓝色边框。
    *   **节点高亮（当前操作）**：亮黄色填充，橙色边框。
    *   **节点完成**：浅绿色填充，深绿色边框。
    *   **队列中节点**：橙色边框（内部填充色可能仍为默认色，以示区分状态）。
    *   **边**：深灰色箭头。
    *   **队列容器**：半透明浅橙色背景。
    *   **结果序列容器**：半透明浅绿色背景。
    *   **文本与日志**：深灰色或黑色，确保高可读性。
*   **原则**：保证足够的对比度，颜色含义一致，避免使用过多鲜艳色彩造成干扰。

#### 交互功能列表
1.  **核心流程控制**：
    *   `上一步`：回退到动画的上一个状态。
    *   `下一步`：前进到动画的下一个状态。
    *   `播放/暂停`：自动连续执行动画。
    *   `重置`：将动画恢复到初始状态。
2.  **示例选择**：一个下拉菜单或按钮组，用于切换不同的预设有向图示例（例如：“课程安排”、“简单DAG”、“带复杂依赖的图”）。
3.  **步骤说明面板**：实时显示当前步骤的详细文字描述。
4.  **高亮与动画**：
    *   自动高亮当前正在处理的节点和边。
    *   节点入度值变化时，有数字变化动画。
    *   节点被加入队列时，有平滑移动动画。
    *   节点从队列弹出并加入结果序列时，有移动动画。
5.  **（进阶）沙盒模式**：
    *   `添加节点`按钮：在画布上点击添加节点。
    *   `添加边`模式：选择两个节点创建有向边。
    *   `运行拓扑排序`按钮：在用户自定义的图上执行算法。
    *   `清除`按钮：清空画布。
6.  **（可选）速度调节**：一个滑块，用于控制自动播放时的速度。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>拓扑排序算法动画演示</title>
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

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #e1e5eb;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.1em;
        }

        .container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }

        .graph-section {
            flex: 3;
            min-width: 300px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            display: flex;
            flex-direction: column;
        }

        .data-structures {
            flex: 2;
            min-width: 250px;
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .queue-container, .result-container {
            background: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            display: flex;
            flex-direction: column;
        }

        .section-title {
            font-size: 1.3em;
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #e1e5eb;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .section-title i {
            font-size: 1.2em;
        }

        #graph-canvas {
            border: 1px solid #e1e5eb;
            border-radius: 8px;
            background-color: #f9fafc;
            flex-grow: 1;
            width: 100%;
            height: 400px;
        }

        .queue-display, .result-display {
            min-height: 120px;
            border: 2px dashed #e1e5eb;
            border-radius: 8px;
            padding: 15px;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 12px;
            background-color: #f9fafc;
            flex-grow: 1;
        }

        .node {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
            position: relative;
        }

        .node-label {
            font-size: 1.2em;
        }

        .node-indegree {
            font-size: 0.9em;
            position: absolute;
            bottom: -5px;
            right: -5px;
            background: white;
            border-radius: 50%;
            width: 24px;
            height: 24px;
            display: flex;
            justify-content: center;
            align-items: center;
            border: 1px solid #ddd;
        }

        .queue-node {
            background-color: #fff8e1;
            border: 2px solid #ffb74d;
            color: #e65100;
        }

        .result-node {
            background-color: #e8f5e9;
            border: 2px solid #66bb6a;
            color: #2e7d32;
        }

        .normal-node {
            background-color: #e3f2fd;
            border: 2px solid #42a5f5;
            color: #1565c0;
        }

        .active-node {
            background-color: #fff9c4;
            border: 3px solid #ffd600;
            color: #f57f17;
            transform: scale(1.1);
            box-shadow: 0 5px 15px rgba(255, 214, 0, 0.4);
            z-index: 10;
        }

        .control-panel {
            background: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            margin-top: 10px;
        }

        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 20px;
        }

        button {
            padding: 10px 18px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .primary-btn {
            background-color: #42a5f5;
            color: white;
        }

        .primary-btn:hover {
            background-color: #1e88e5;
            transform: translateY(-2px);
        }

        .secondary-btn {
            background-color: #e0e0e0;
            color: #424242;
        }

        .secondary-btn:hover {
            background-color: #bdbdbd;
        }

        .example-selector {
            margin-bottom: 20px;
        }

        select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-size: 1em;
            background-color: white;
        }

        .log-panel {
            background-color: #f5f5f5;
            border-radius: 8px;
            padding: 15px;
            height: 150px;
            overflow-y: auto;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 0.95em;
            border: 1px solid #e0e0e0;
        }

        .log-entry {
            margin-bottom: 8px;
            padding-bottom: 8px;
            border-bottom: 1px dashed #ddd;
        }

        .log-time {
            color: #7f8c8d;
            font-size: 0.85em;
            margin-right: 10px;
        }

        .log-message {
            color: #2c3e50;
        }

        .highlight {
            font-weight: bold;
            color: #e65100;
        }

        .algorithm-steps {
            margin-top: 25px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
        }

        .step-list {
            list-style-type: none;
            counter-reset: step-counter;
        }

        .step-list li {
            counter-increment: step-counter;
            margin-bottom: 15px;
            padding-left: 40px;
            position: relative;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .step-list li:before {
            content: counter(step-counter);
            background-color: #42a5f5;
            color: white;
            width: 28px;
            height: 28px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            position: absolute;
            left: 0;
            top: 0;
            font-weight: bold;
        }

        .current-step {
            background-color: #f0f7ff;
            border-radius: 6px;
            padding: 10px;
            margin-left: -10px;
            border-left: 4px solid #42a5f5;
        }

        .current-step:before {
            background-color: #ff9800 !important;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #e1e5eb;
            color: #7f8c8d;
            font-size: 0.9em;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .controls {
                justify-content: center;
            }
            
            button {
                flex-grow: 1;
                justify-content: center;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <header>
        <h1><i class="fas fa-sort-amount-down"></i> 拓扑排序算法动画演示</h1>
        <p class="subtitle">基于入度的Kahn算法：入度减0 → 队列弹出 → 输出结果</p>
    </header>

    <div class="container">
        <div class="main-content">
            <section class="graph-section">
                <h2 class="section-title"><i class="fas fa-project-diagram"></i> 有向图</h2>
                <canvas id="graph-canvas" width="800" height="400"></canvas>
                <div class="example-selector">
                    <label for="example-select">选择示例图：</label>
                    <select id="example-select">
                        <option value="course">示例1：课程安排依赖</option>
                        <option value="simple">示例2：简单依赖图</option>
                        <option value="complex">示例3：复杂依赖图</option>
                    </select>
                </div>
            </section>

            <div class="data-structures">
                <section class="queue-container">
                    <h2 class="section-title"><i class="fas fa-stream"></i> 队列 (Queue)</h2>
                    <div class="queue-display" id="queue-display">
                        <div class="empty-queue-msg">队列为空</div>
                    </div>
                    <div class="queue-info">
                        <p>入度为0的节点会加入队列，按先进先出(FIFO)顺序处理。</p>
                    </div>
                </section>

                <section class="result-container">
                    <h2 class="section-title"><i class="fas fa-list-ol"></i> 拓扑排序结果</h2>
                    <div class="result-display" id="result-display">
                        <div class="empty-result-msg">结果将在此显示</div>
                    </div>
                    <div class="result-info">
                        <p>从队列弹出的节点会按顺序加入结果序列。</p>
                    </div>
                </section>
            </div>
        </div>

        <section class="control-panel">
            <h2 class="section-title"><i class="fas fa-sliders-h"></i> 控制面板</h2>
            <div class="controls">
                <button id="prev-btn" class="secondary-btn"><i class="fas fa-step-backward"></i> 上一步</button>
                <button id="next-btn" class="primary-btn"><i class="fas fa-step-forward"></i> 下一步</button>
                <button id="play-btn" class="primary-btn"><i class="fas fa-play"></i> 播放</button>
                <button id="reset-btn" class="secondary-btn"><i class="fas fa-redo"></i> 重置</button>
                <button id="speed-slow" class="secondary-btn"><i class="fas fa-tachometer-alt"></i> 慢速</button>
                <button id="speed-normal" class="primary-btn"><i class="fas fa-tachometer-alt"></i> 中速</button>
                <button id="speed-fast" class="secondary-btn"><i class="fas fa-tachometer-alt"></i> 快速</button>
            </div>
            
            <div class="log-panel" id="log-panel">
                <div class="log-entry">
                    <span class="log-time">[就绪]</span>
                    <span class="log-message">请选择一个示例图，然后点击"下一步"开始拓扑排序。</span>
                </div>
            </div>
        </section>

        <section class="algorithm-steps">
            <h2 class="section-title"><i class="fas fa-list-ol"></i> 算法步骤</h2>
            <ol class="step-list" id="step-list">
                <li>初始化：计算所有节点的入度</li>
                <li>将所有入度为0的节点加入队列</li>
                <li>当队列不为空时，执行以下操作：</li>
                <li>从队列中取出一个节点（队首）</li>
                <li>将该节点加入拓扑排序结果</li>
                <li>遍历该节点的所有邻居节点</li>
                <li>将每个邻居节点的入度减1</li>
                <li>如果邻居节点的入度变为0，将其加入队列</li>
                <li>重复步骤3-8，直到队列为空</li>
                <li>如果结果中的节点数等于总节点数，排序成功；否则图中存在环</li>
            </ol>
        </section>
    </div>

    <footer>
        <p>拓扑排序算法动画演示 | 基于入度的Kahn算法 | 使用HTML5 Canvas实现</p>
        <p>交互式教学动画 - 理解"入度减0→队列弹出"的核心过程</p>
    </footer>

    <script>
        // 拓扑排序算法状态机
        class TopologicalSortAnimation {
            constructor() {
                this.canvas = document.getElementById('graph-canvas');
                this.ctx = this.canvas.getContext('2d');
                this.queueDisplay = document.getElementById('queue-display');
                this.resultDisplay = document.getElementById('result-display');
                this.logPanel = document.getElementById('log-panel');
                this.stepList = document.getElementById('step-list').children;
                this.exampleSelect = document.getElementById('example-select');
                
                // 控制按钮
                this.prevBtn = document.getElementById('prev-btn');
                this.nextBtn = document.getElementById('next-btn');
                this.playBtn = document.getElementById('play-btn');
                this.resetBtn = document.getElementById('reset-btn');
                this.speedSlowBtn = document.getElementById('speed-slow');
                this.speedNormalBtn = document.getElementById('speed-normal');
                this.speedFastBtn = document.getElementById('speed-fast');
                
                // 状态变量
                this.currentStep = 0;
                this.isPlaying = false;
                this.playSpeed = 1000; // 毫秒
                this.playInterval = null;
                this.history = [];
                this.currentHistoryIndex = -1;
                
                // 图数据
                this.graph = {
                    nodes: [],
                    edges: [],
                    adjacencyList: {}
                };
                
                // 算法状态
                this.indegree = {};
                this.queue = [];
                this.result = [];
                this.currentNode = null;
                this.currentNeighbors = [];
                this.visitedEdges = new Set();
                
                // 示例图定义
                this.examples = {
                    course: {
                        name: "课程安排依赖",
                        nodes: [
                            {id: 'A', x: 150, y: 200, label: '数学基础'},
                            {id: 'B', x: 300, y: 100, label: '数据结构'},
                            {id: 'C', x: 300, y: 300, label: '算法设计'},
                            {id: 'D', x: 450, y: 200, label: '数据库'},
                            {id: 'E', x: 600, y: 200, label: '毕业设计'}
                        ],
                        edges: [
                            {from: 'A', to: 'B'},
                            {from: 'A', to: 'C'},
                            {from: 'B', to: 'D'},
                            {from: 'C', to: 'D'},
                            {from: 'D', to: 'E'}
                        ]
                    },
                    simple: {
                        name: "简单依赖图",
                        nodes: [
                            {id: 'A', x: 200, y: 150},
                            {id: 'B', x: 200, y: 250},
                            {id: 'C', x: 350, y: 150},
                            {id: 'D', x: 350, y: 250},
                            {id: 'E', x: 500, y: 200}
                        ],
                        edges: [
                            {from: 'A', to: 'C'},
                            {from: 'B', to: 'D'},
                            {from: 'C', to: 'E'},
                            {from: 'D', to: 'E'}
                        ]
                    },
                    complex: {
                        name: "复杂依赖图",
                        nodes: [
                            {id: 'A', x: 150, y: 100},
                            {id: 'B', x: 150, y: 200},
                            {id: 'C', x: 150, y: 300},
                            {id: 'D', x: 300, y: 150},
                            {id: 'E', x: 300, y: 250},
                            {id: 'F', x: 450, y: 200},
                            {id: 'G', x: 600, y: 200}
                        ],
                        edges: [
                            {from: 'A', to: 'D'},
                            {from: 'B', to: 'D'},
                            {from: 'B', to: 'E'},
                            {from: 'C', to: 'E'},
                            {from: 'D', to: 'F'},
                            {from: 'E', to: 'F'},
                            {from: 'F', to: 'G'}
                        ]
                    }
                };
                
                // 初始化
                this.init();
            }
            
            init() {
                // 加载默认示例
                this.loadExample('course');
                
                // 绑定事件
                this.bindEvents();
                
                // 初始渲染
                this.render();
                this.updateStepHighlight();
                this.addLog("系统初始化完成，请选择一个示例图开始。");
            }
            
            bindEvents() {
                // 示例选择
                this.exampleSelect.addEventListener('change', (e) => {
                    this.loadExample(e.target.value);
                    this.resetAnimation();
                });
                
                // 控制按钮
                this.prevBtn.addEventListener('click', () => this.prevStep());
                this.nextBtn.addEventListener('click', () => this.nextStep());
                this.playBtn.addEventListener('click', () => this.togglePlay());
                this.resetBtn.addEventListener('click', () => this.resetAnimation());
                
                // 速度控制
                this.speedSlowBtn.addEventListener('click', () => this.setSpeed(1500));
                this.speedNormalBtn.addEventListener('click', () => this.setSpeed(1000));
                this.speedFastBtn.addEventListener('click', () => this.setSpeed(500));
            }
            
            loadExample(exampleKey) {
                const example = this.examples[exampleKey];
                if (!example) return;
                
                this.graph.nodes = JSON.parse(JSON.stringify(example.nodes));
                this.graph.edges = JSON.parse(JSON.stringify(example.edges));
                
                // 构建邻接表
                this.graph.adjacencyList = {};
                this.graph.nodes.forEach(node => {
                    this.graph.adjacencyList[node.id] = [];
                });
                
                this.graph.edges.forEach(edge => {
                    if (this.graph.adjacencyList[edge.from]) {
                        this.graph.adjacencyList[edge.from].push(edge.to);
                    }
                });
                
                // 重置算法状态
                this.resetAlgorithmState();
                
                this.addLog(`已加载示例: ${example.name}`);
            }
            
            resetAlgorithmState() {
                // 计算初始入度
                this.indegree = {};
                this.graph.nodes.forEach(node => {
                    this.indegree[node.id] = 0;
                });
                
                this.graph.edges.forEach(edge => {
                    this.indegree[edge.to]++;
                });
                
                // 清空队列和结果
                this.queue = [];
                this.result = [];
                this.currentNode = null;
                this.currentNeighbors = [];
                this.visitedEdges = new Set();
                
                // 清空历史
                this.history = [];
                this.currentHistoryIndex = -1;
                this.saveStateToHistory();
                
                // 重置步骤
                this.currentStep = 0;
                
                // 初始：将所有入度为0的节点加入队列
                this.graph.nodes.forEach(node => {
                    if (this.indegree[node.id] === 0) {
                        this.queue.push(node.id);
                    }
                });
                
                // 更新显示
                this.updateQueueDisplay();
                this.updateResultDisplay();
                this.updateStepHighlight();
            }
            
            resetAnimation() {
                this.stopPlay();
                this.resetAlgorithmState();
                this.render();
                this.addLog("动画已重置。");
            }
            
            saveStateToHistory() {
                const state = {
                    indegree: {...this.indegree},
                    queue: [...this.queue],
                    result: [...this.result],
                    currentNode: this.currentNode,
                    currentNeighbors: [...this.currentNeighbors],
                    visitedEdges: new Set(this.visitedEdges),
                    step: this.currentStep
                };
                
                this.history = this.history.slice(0, this.currentHistoryIndex + 1);
                this.history.push(state);
                this.currentHistoryIndex = this.history.length - 1;
            }
            
            restoreStateFromHistory(index) {
                if (index < 0 || index >= this.history.length) return;
                
                const state = this.history[index];
                this.indegree = {...state.indegree};
                this.queue = [...state.queue];
                this.result = [...state.result];
                this.currentNode = state.currentNode;
                this.currentNeighbors = [...state.currentNeighbors];
                this.visitedEdges = new Set(state.visitedEdges);
                this.currentStep = state.step;
                
                this.currentHistoryIndex = index;
                
                this.updateQueueDisplay();
                this.updateResultDisplay();
                this.updateStepHighlight();
                this.render();
            }
            
            prevStep() {
                if (this.currentHistoryIndex > 0) {
                    this.restoreStateFromHistory(this.currentHistoryIndex - 1);
                    this.addLog("回退到上一步。");
                }
            }
            
            nextStep() {
                this.stopPlay();
                
                // 保存当前状态到历史
                this.saveStateToHistory();
                
                // 执行下一步
                this.executeNextStep();
                
                // 更新显示
                this.updateQueueDisplay();
                this.updateResultDisplay();
                this.updateStepHighlight();
                this.render();
            }
            
            executeNextStep() {
                // 根据当前步骤执行相应操作
                switch (this.currentStep) {
                    case 0: // 初始化：计算所有节点的入度
                        this.addLog("步骤1: 初始化完成，已计算所有节点的入度。");
                        this.currentStep = 1;
                        break;
                        
                    case 1: // 将所有入度为0的节点加入队列
                        if (this.queue.length === 0) {
                            this.addLog("没有入度为0的节点，图中可能存在环。");
                            this.currentStep = 9; // 跳到最后一步
                        } else {
                            this.addLog(`步骤2: 将入度为0的节点 ${this.queue.join(', ')} 加入队列。`);
                            this.currentStep = 2;
                        }
                        break;
                        
                    case 2: // 检查队列是否为空
                        if (this.queue.length === 0) {
                            this.addLog("队列已空，算法结束。");
                            this.currentStep = 9; // 跳到最后一步
                        } else {
                            this.addLog("步骤3: 队列不为空，继续处理。");
                            this.currentStep = 3;
                        }
                        break;
                        
                    case 3: // 从队列中取出一个节点
                        this.currentNode = this.queue.shift();
                        this.addLog(`步骤4: 从队列中取出节点 ${this.currentNode}。`);
                        this.currentNeighbors = this.graph.adjacencyList[this.currentNode] || [];
                        this.currentStep = 4;
                        break;
                        
                    case 4: // 将该节点加入拓扑排序结果
                        this.result.push(this.currentNode);
                        this.addLog(`步骤5: 将节点 ${this.currentNode} 加入拓扑排序结果。`);
                        this.currentStep = 5;
                        break;
                        
                    case 5: // 遍历该节点的所有邻居节点
                        if (this.currentNeighbors.length === 0) {
                            this.addLog(`节点 ${this.currentNode} 没有邻居节点。`);
                            this.currentStep = 2; // 回到检查队列
                        } else {
                            const neighbor = this.currentNeighbors[0];
                            this.addLog(`步骤6: 处理邻居节点 ${neighbor}。`);
                            this.currentStep = 6;
                        }
                        break;
                        
                    case 6: // 将邻居节点的入度减1
                        const currentNeighbor = this.currentNeighbors[0];
                        this.indegree[currentNeighbor]--;
                        
                        // 标记边为已访问
                        const edgeKey = `${this.currentNode}->${currentNeighbor}`;
                        this.visitedEdges.add(edgeKey);
                        
                        this.addLog(`步骤7: 将节点 ${currentNeighbor} 的入度减1，新入度为 ${this.indegree[currentNeighbor]}。`);
                        this.currentStep = 7;
                        break;
                        
                    case 7: // 检查邻居节点入度是否变为0
                        const neighbor = this.currentNeighbors.shift();
                        if (this.indegree[neighbor] === 0) {
                            this.queue.push(neighbor);
                            this.addLog(`步骤8: 节点 ${neighbor} 的入度变为0，将其加入队列。`);
                        } else {
                            this.addLog(`节点 ${neighbor} 的入度不为0，不入队。`);
                        }
                        
                        // 如果还有邻居需要处理，回到步骤6
                        if (this.currentNeighbors.length > 0) {
                            this.currentStep = 6;
                        } else {
                            this.currentStep = 2; // 回到检查队列
                        }
                        break;
                        
                    case 9: // 算法结束，检查结果
                        if (this.result.length === this.graph.nodes.length) {
                            this.addLog(`步骤10: 拓扑排序成功！结果: ${this.result.join(' → ')}`);
                        } else {
                            this.addLog(`步骤10: 拓扑排序失败！图中存在环。只排序了部分节点: ${this.result.join(' → ')}`);
                        }
                        this.currentStep = 10;
                        break;
                        
                    case 10: // 最终状态
                        this.addLog("算法已结束。点击重置重新开始。");
                        break;
                }
            }
            
            togglePlay() {
                if (this.isPlaying) {
                    this.stopPlay();
                } else {
                    this.startPlay();
                }
            }
            
            startPlay() {
                this.isPlaying = true;
                this.playBtn.innerHTML = '<i class="fas fa-pause"></i> 暂停';
                this.playBtn.classList.remove('primary-btn');
                this.playBtn.classList.add('secondary-btn');
                
                this.playInterval = setInterval(() => {
                    // 如果算法已结束，停止播放
                    if (this.currentStep >= 10) {
                        this.stopPlay();
                        return;
                    }
                    
                    this.nextStep();
                }, this.playSpeed);
            }
            
            stopPlay() {
                this.isPlaying = false;
                this.playBtn.innerHTML = '<i class="fas fa-play"></i> 播放';
                this.playBtn.classList.remove('secondary-btn');
                this.playBtn.classList.add('primary-btn');
                
                if (this.playInterval) {
                    clearInterval(this.playInterval);
                    this.playInterval = null;
                }
            }
            
            setSpeed(speed) {
                this.playSpeed = speed;
                
                // 更新按钮状态
                [this.speedSlowBtn, this.speedNormalBtn, this.speedFastBtn].forEach(btn => {
                    btn.classList.remove('primary-btn');
                    btn.classList.add('secondary-btn');
                });
                
                if (speed === 1500) {
                    this.speedSlowBtn.classList.remove('secondary-btn');
                    this.speedSlowBtn.classList.add('primary-btn');
                } else if (speed === 1000) {
                    this.speedNormalBtn.classList.remove('secondary-btn');
                    this.speedNormalBtn.classList.add('primary-btn');
                } else if (speed === 500) {
                    this.speedFastBtn.classList.remove('secondary-btn');
                    this.speedFastBtn.classList.add('primary-btn');
                }
                
                // 如果正在播放，重新设置间隔
                if (this.isPlaying) {
                    this.stopPlay();
                    this.startPlay();
                }
                
                this.addLog(`播放速度设置为: ${speed === 1500 ? '慢速' : speed === 1000 ? '中速' : '快速'}`);
            }
            
            updateQueueDisplay() {
                this.queueDisplay.innerHTML = '';
                
                if (this.queue.length === 0) {
                    this.queueDisplay.innerHTML = '<div class="empty-queue-msg">队列为空</div>';
                    return;
                }
                
                this.queue.forEach(nodeId => {
                    const nodeElement = document.createElement('div');
                    nodeElement.className = 'node queue-node';
                    nodeElement.innerHTML = `
                        <div class="node-label">${nodeId}</div>
                        <div class="node-indegree">${this.indegree[nodeId]}</div>
                    `;
                    this.queueDisplay.appendChild(nodeElement);
                });
            }
            
            updateResultDisplay() {
                this.resultDisplay.innerHTML = '';
                
                if (this.result.length === 0) {
                    this.resultDisplay.innerHTML = '<div class="empty-result-msg">结果将在此显示</div>';
                    return;
                }
                
                this.result.forEach(nodeId => {
                    const nodeElement = document.createElement('div');
                    nodeElement.className = 'node result-node';
                    nodeElement.innerHTML = `
                        <div class="node-label">${nodeId}</div>
                        <div class="node-indegree">${this.indegree[nodeId]}</div>
                    `;
                    this.resultDisplay.appendChild(nodeElement);
                });
            }
            
            updateStepHighlight() {
                // 移除所有当前步骤高亮
                Array.from(this.stepList).forEach(li => {
                    li.classList.remove('current-step');
                });
                
                // 高亮当前步骤
                if (this.currentStep < this.stepList.length) {
                    this.stepList[this.currentStep].classList.add('current-step');
                }
            }
            
            addLog(message) {
                const now = new Date();
                const timeString = `${now.getHours().toString().padStart(2, '0')}:${now.getMinutes().toString().padStart(2, '0')}:${now.getSeconds().toString().padStart(2, '0')}`;
                
                const logEntry = document.createElement('div');
                logEntry.className = 'log-entry';
                logEntry.innerHTML = `
                    <span class="log-time">[${timeString}]</span>
                    <span class="log-message">${message}</span>
                `;
                
                this.logPanel.appendChild(logEntry);
                this.logPanel.scrollTop = this.logPanel.scrollHeight;
            }
            
            render() {
                // 清空画布
                this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
                
                // 绘制边
                this.graph.edges.forEach(edge => {
                    const fromNode = this.graph.nodes.find(n => n.id === edge.from);
                    const toNode = this.graph.nodes.find(n => n.id === edge.to);
                    
                    if (!fromNode || !toNode) return;
                    
                    // 检查边是否已被访问
                    const edgeKey = `${edge.from}->${edge.to}`;
                    const isVisited = this.visitedEdges.has(edgeKey);
                    
                    // 绘制箭头线
                    this.drawArrow(
                        fromNode.x, fromNode.y,
                        toNode.x, toNode.y,
                        isVisited ? '#81c784' : '#90a4ae',
                        isVisited ? 3 : 2,
                        isVisited
                    );
                });
                
                // 绘制节点
                this.graph.nodes.forEach(node => {
                    // 确定节点状态
                    let nodeClass = 'normal-node';
                    if (this.result.includes(node.id)) {
                        nodeClass = 'result-node';
                    } else if (this.queue.includes(node.id)) {
                        nodeClass = 'queue-node';
                    }
                    
                    if (node.id === this.currentNode) {
                        nodeClass = 'active-node';
                    }
                    
                    // 绘制节点
                    this.drawNode(node, nodeClass);
                });
            }
            
            drawNode(node, nodeClass) {
                // 根据节点类确定颜色
                let fillColor, borderColor, textColor;
                
                switch(nodeClass) {
                    case 'normal-node':
                        fillColor = '#e3f2fd';
                        borderColor = '#42a5f5';
                        textColor = '#1565c0';
                        break;
                    case 'queue-node':
                        fillColor = '#fff8e1';
                        borderColor = '#ffb74d';
                        textColor = '#e65100';
                        break;
                    case 'result-node':
                        fillColor = '#e8f5e9';
                        borderColor = '#66bb6a';
                        textColor = '#2e7d32';
                        break;
                    case 'active-node':
                        fillColor = '#fff9c4';
                        borderColor = '#ffd600';
                        textColor = '#f57f17';
                        break;
                }
                
                // 绘制节点圆
                this.ctx.beginPath();
                this.ctx.arc(node.x, node.y, 25, 0, Math.PI * 2);
                this.ctx.fillStyle = fillColor;
                this.ctx.fill();
                this.ctx.lineWidth = nodeClass === 'active-node' ? 3 : 2;
                this.ctx.strokeStyle = borderColor;
                this.ctx.stroke();
                
                // 绘制节点标签
                this.ctx.font = 'bold 16px Arial';
                this.ctx.fillStyle = textColor;
                this.ctx.textAlign = 'center';
                this.ctx.textBaseline = 'middle';
                this.ctx.fillText(node.id, node.x, node.y);
                
                // 绘制入度值
                this.ctx.beginPath();
                this.ctx.arc(node.x + 20, node.y - 20, 12, 0, Math.PI * 2);
                this.ctx.fillStyle = 'white';
                this.ctx.fill();
                this.ctx.lineWidth = 1;
                this.ctx.strokeStyle = '#ddd';
                this.ctx.stroke();
                
                this.ctx.font = '12px Arial';
                this.ctx.fillStyle = '#333';
                this.ctx.textAlign = 'center';
                this.ctx.textBaseline = 'middle';
                this.ctx.fillText(this.indegree[node.id] || 0, node.x + 20, node.y - 20);
                
                // 如果有额外标签（如课程名），显示在节点下方
                if (node.label) {
                    this.ctx.font = '12px Arial';
                    this.ctx.fillStyle = '#666';
                    this.ctx.fillText(node.label, node.x, node.y + 40);
                }
            }
            
            drawArrow(fromX, fromY, toX, toY, color, width, isVisited) {
                // 计算箭头方向
                const dx = toX - fromX;
                const dy = toY - fromY;
                const angle = Math.atan2(dy, dx);
                const length = Math.sqrt(dx * dx + dy * dy);
                
                // 考虑节点半径，调整起点和终点
                const startRadius = 25;
                const endRadius = 25;
                const adjustedFromX = fromX + Math.cos(angle) * startRadius;
                const adjustedFromY = fromY + Math.sin(angle) * startRadius;
                const adjustedTo
<!--检测到代码截断，自动续写中...-->
X = toX - Math.cos(angle) * endRadius;
                const adjustedToY = toY - Math.sin(angle) * endRadius;
                
                // 绘制线
                this.ctx.beginPath();
                this.ctx.moveTo(adjustedFromX, adjustedFromY);
                this.ctx.lineTo(adjustedToX, adjustedToY);
                this.ctx.strokeStyle = color;
                this.ctx.lineWidth = width;
                this.ctx.stroke();
                
                // 绘制箭头
                const arrowLength = 10;
                const arrowWidth = 8;
                
                this.ctx.beginPath();
                this.ctx.moveTo(adjustedToX, adjustedToY);
                this.ctx.lineTo(
                    adjustedToX - arrowLength * Math.cos(angle - Math.PI / 6),
                    adjustedToY - arrowLength * Math.sin(angle - Math.PI / 6)
                );
                this.ctx.lineTo(
                    adjustedToX - arrowLength * Math.cos(angle + Math.PI / 6),
                    adjustedToY - arrowLength * Math.sin(angle + Math.PI / 6)
                );
                this.ctx.closePath();
                this.ctx.fillStyle = color;
                this.ctx.fill();
                
                // 如果边已被访问，添加动画效果
                if (isVisited) {
                    this.ctx.beginPath();
                    this.ctx.arc(adjustedToX, adjustedToY, 5, 0, Math.PI * 2);
                    this.ctx.fillStyle = '#4caf50';
                    this.ctx.fill();
                }
            }
        }
        
        // 页面加载完成后初始化动画
        document.addEventListener('DOMContentLoaded', () => {
            const animation = new TopologicalSortAnimation();
            
            // 将动画实例暴露给全局，方便调试
            window.topologicalSortAnimation = animation;
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

# 拓扑排序算法交互式教学动画使用指南

欢迎使用拓扑排序算法交互式教学动画！本指南将帮助您充分利用这个教学工具，深入理解基于入度的Kahn算法核心原理。

## 🎯 功能说明

本动画通过可视化方式演示拓扑排序算法的完整执行过程，特别聚焦于"入度减0→队列弹出"这一核心机制。它将抽象的算法转化为直观的视觉体验，帮助您：

- 直观理解有向无环图(DAG)中节点的依赖关系
- 跟踪算法每一步的状态变化
- 观察队列和结果序列的实时更新
- 掌握算法的时间复杂度和应用场景

## 🚀 主要功能

### 1. 示例图选择
- **课程安排依赖**：以课程先修关系为例，展示实际应用场景
- **简单依赖图**：基础示例，适合初学者理解核心概念
- **复杂依赖图**：多分支结构，展示算法的完整处理流程

### 2. 动画控制
- **单步执行**：通过"上一步"/"下一步"按钮精确控制算法进度
- **自动播放**：点击"播放"按钮自动执行完整算法流程
- **速度调节**：提供慢速、中速、快速三种播放速度
- **一键重置**：随时回到初始状态重新开始

### 3. 可视化区域
- **主图区域**：显示有向图结构，节点包含标识和实时入度值
- **队列区域**：展示当前等待处理的节点（入度为0）
- **结果区域**：显示已完成的拓扑排序序列
- **日志面板**：记录每一步的详细操作说明

### 4. 算法步骤跟踪
- 实时高亮显示当前执行的算法步骤
- 10个关键步骤的详细说明和状态跟踪

## ✨ 设计特色

### 视觉编码系统
- **颜色语义**：
  - 🔵 蓝色：待处理节点
  - 🟠 橙色：队列中的节点
  - 🟢 绿色：已完成的节点
  - 🟡 黄色：当前活动节点（高亮显示）
- **状态指示**：
  - 节点内显示标识（如A、B）
  - 右上角小圆显示实时入度值
  - 边颜色变化表示是否已被处理

### 教学友好设计
- **渐进式学习**：从简单示例开始，逐步过渡到复杂场景
- **即时反馈**：每一步操作都有对应的日志记录和视觉反馈
- **错误处理**：当图中存在环时，会明确提示拓扑排序失败
- **上下文保持**：历史状态可回溯，便于对比分析

## 📚 教学要点

### 核心概念可视化
1. **入度(Indegree)**：指向节点的边数，在动画中以数字实时显示
2. **队列操作**：入度为0的节点加入队列，按FIFO顺序处理
3. **边删除**：算法中"删除节点"体现为将其邻居节点的入度减1
4. **终止条件**：队列为空时算法结束

### 算法步骤详解
建议按照以下顺序理解算法：
1. **初始化阶段**：计算所有节点的初始入度
2. **入队阶段**：将所有入度为0的节点加入队列
3. **循环处理**：
   - 弹出队首节点
   - 加入结果序列
   - 更新邻居节点入度
   - 将新入度为0的节点入队
4. **结果验证**：检查结果节点数是否等于总节点数

### 常见问题理解
- **为什么需要队列？**：管理待处理节点，确保按正确顺序处理
- **如何处理多个入度为0的节点？**：任意顺序均可，本动画使用队列的FIFO特性
- **如何检测环？**：算法结束后，如果结果节点数少于总节点数，说明存在环

## 💡 使用建议

### 学习路径推荐
1. **初学者**：
   - 选择"课程安排依赖"示例
   - 使用"慢速"自动播放观看完整流程
   - 重点关注入度值的变化规律

2. **进阶学习**：
   - 选择"复杂依赖图"示例
   - 使用单步执行模式，预测下一步操作
   - 观察队列和结果的同步变化

3. **巩固理解**：
   - 在不同示例间切换，比较算法处理差异
   - 尝试在脑海中模拟算法，然后与动画对比
   - 关注算法的时间复杂度表现

### 教学应用建议
**教师使用**：
- 课堂演示时，可先讲解理论，再用动画验证
- 使用单步模式引导学生思考下一步操作
- 通过不同示例展示算法的通用性

**学生自学**：
- 遇到困惑时，使用"上一步"功能回溯观察
- 结合日志记录理解每个操作的意图
- 尝试解释每个颜色变化的含义

### 最佳实践
1. **先观察后操作**：首次接触时，先观看完整动画了解整体流程
2. **主动预测**：在点击"下一步"前，尝试预测会发生什么
3. **多角度验证**：从节点、队列、结果三个视角同时观察算法状态
4. **联系实际**：思考拓扑排序在课程安排、任务调度、编译顺序等场景的应用

### 故障排除
- **动画卡顿**：尝试切换到更简单的示例图
- **理解困难**：从"简单依赖图"开始，逐步增加复杂度
- **浏览器兼容**：建议使用Chrome、Firefox或Edge的最新版本

## 🎓 学习目标达成

完成本动画的学习后，您应该能够：
- ✅ 清晰描述拓扑排序算法的每一步操作
- ✅ 根据有向图手动计算拓扑排序结果
- ✅ 解释队列在算法中的作用
- ✅ 判断一个图是否可以进行拓扑排序
- ✅ 将算法应用于实际问题场景

---

**祝您学习愉快！** 拓扑排序是理解图算法的重要基础，掌握它将为您学习更复杂的算法奠定坚实基础。如有任何问题或建议，欢迎反馈。

*教育技术专家 熊猫老师 设计制作*