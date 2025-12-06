# 需求：堆的插入与删除（上浮、下沉动画）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为学习数据结构（如计算机科学、软件工程）的本科生或自学者。他们已具备数组、树等基本数据结构知识，正学习“堆”这一抽象数据类型。
2.  **核心痛点**：
    *   **抽象过程难以理解**：堆的插入（上浮/向上调整）和删除堆顶元素（下沉/向下调整）是动态的、基于比较和交换的过程。仅凭静态图示或文字描述，学习者难以在脑海中构建出元素位置连续变化的动态图景。
    *   **算法逻辑与数据结构的脱节**：学习者可能记住了算法步骤（如“与父节点比较”、“与较大/较小子节点交换”），但无法直观地看到这些操作如何影响堆的数组表示和逻辑上的完全二叉树形态。
    *   **缺乏主动探索与试错机会**：需要一个安全的环境，允许用户输入不同数据、触发不同操作，并即时看到结果，以验证理解或发现错误。
3.  **核心需求**：因此，用户需要一个**可视化、可交互、步骤可控**的动画，将算法步骤、数据变化（数组）和结构变化（二叉树）三者同步、直观地展现出来，降低认知负荷，促进对算法本质的理解。

#### 教学设计思路
本动画遵循“从具体到抽象，再统一关联”的认知规律进行设计。

1.  **核心概念聚焦**：
    *   **堆的定义**：强调其作为**完全二叉树**的形态，以及**堆序性质**（大顶堆：父节点值 ≥ 子节点值；小顶堆：父节点值 ≤ 子节点值）。
    *   **关键操作**：
        *   **插入（上浮）**：新元素置于末尾，破坏堆序，通过**与父节点比较并交换**，逐层“上浮”至合适位置。
        *   **删除堆顶（下沉）**：移除堆顶元素，将末尾元素移至堆顶，破坏堆序，通过**与子节点比较并交换**，逐层“下沉”至合适位置。
    *   **双重视角关联**：始终同步展示**逻辑视图（完全二叉树）** 和**物理存储视图（数组）**，并用明确的连线或对应关系强调索引计算（如父节点 `i` 的子节点为 `2*i+1` 和 `2*i+2`）。

2.  **认知规律与流程设计**：
    *   **引入与感知**：初始状态展示一个已建好的堆（二叉树+数组），让用户直观感受其结构。
    *   **分步演示与讲解**：
        *   **插入流程**：用户输入一个值 -> 动画显示该值被放入数组末尾及二叉树对应新叶节点 -> 高亮该节点及其父节点 -> 进行比较 -> 如需交换，动画展示交换过程（位置互换、颜色/连线变化）-> 重复“比较-交换”过程直至堆序满足 -> 过程结束，新堆稳定。
        *   **删除流程**：用户点击删除 -> 动画高亮并“移除”堆顶元素（根节点）-> 动画将数组末尾元素移至堆顶位置 -> 高亮该节点及其子节点 -> 进行比较 -> 如需交换，动画展示与**较大（大顶堆）/较小（小顶堆）子节点**的交换过程 -> 重复直至堆序满足。
    *   **交互探索与巩固**：允许用户连续执行插入/删除，观察堆的动态变化。提供“单步执行”控制，让用户能以自己的节奏观察每一步的细节。

3.  **交互设计**：
    *   **主动输入**：提供输入框供用户输入待插入的数字。
    *   **明确触发**：设置“插入”、“删除堆顶”两个主要按钮。
    *   **过程控制**：提供“播放/暂停”、“下一步”、“重置”等控制按钮，让学习节奏可控。
    *   **状态反馈**：在动画区域旁设置一个“状态/步骤说明”面板，用文字描述当前正在进行的操作（如：“比较新节点(15)与其父节点(10)：15>10，需要交换”）。

4.  **视觉呈现**：
    *   **双视图并列**：左侧为**完全二叉树可视化**，使用圆形节点和连线；右侧为**数组可视化**，使用矩形框按索引排列。
    *   **颜色编码**：
        *   **默认状态**：节点/数组元素为中性色（如浅灰色）。
        *   **活动/焦点元素**：当前正在参与比较或移动的元素（如新插入节点、待下沉的堆顶元素）使用**突出色（如亮蓝色）**。
        *   **比较对象**：当前比较的另一方（如父节点、子节点）使用**对比色（如橙色）**。
        *   **交换过程**：在交换时，两个元素的颜色可以短暂变为**强调色（如黄色）**，并伴有平滑的位置移动动画。
        *   **完成状态**：一次操作完成后，所有元素恢复默认色，或短暂闪烁一下表示稳定。
    *   **动画与连线**：元素移动（上浮、下沉）使用平滑的补间动画。在二叉树和数组视图中，对应的元素之间应有明确的连线或高亮对应关系，强化索引映射的概念。
    *   **提示信息**：在关键步骤，通过浮动标签或固定面板显示比较的结果、交换的原因等文本信息。

#### 配色方案选择
*   **主背景**：浅灰色或白色，确保清晰度。
*   **二叉树与数组容器**：使用细深灰色边框。
*   **节点/元素默认填充色**：`#f0f0f0` (极浅灰) 或 `#e8e8e8`。
*   **活动/焦点元素**：`#4A90E2` (明亮、友好的蓝色)，代表当前操作的核心。
*   **比较对象元素**：`#F5A623` (橙色)，与蓝色形成清晰对比，易于区分。
*   **交换过程高亮**：`#FFD700` (金黄色)，在交换瞬间短暂使用，吸引注意力。
*   **完成提示**：`#7ED321` (绿色)，可用于操作完成后的短暂闪烁或边框。
*   **文字与线条**：`#333333` (深灰色)，确保可读性。
*   **状态面板背景**：`#f9f9f9`，轻微区别于主背景。

#### 交互功能列表
1.  **数据输入区**：
    *   数字输入框（带范围提示或验证）。
    *   【插入】按钮：触发插入操作动画。
    *   【删除堆顶】按钮：触发删除堆顶元素动画。
2.  **动画控制区**：
    *   【单步播放/暂停】按钮：控制动画的进行与暂停。
    *   【下一步】按钮：在暂停或单步模式下，执行下一个原子步骤（如一次比较或一次交换）。
    *   【重置】按钮：将堆恢复到一个预设的初始状态。
3.  **可视化主区域**：
    *   **左侧：完全二叉树视图**
        *   动态绘制节点（圆形）与连接线。
        *   节点内显示数值。
        *   根据算法步骤高亮、移动对应节点。
    *   **右侧：数组存储视图**
        *   动态绘制数组单元格（矩形）。
        *   单元格内显示索引和值。
        *   与二叉树节点同步高亮和变化。
        *   可考虑用连线或同色背景直观连接二叉树节点与对应的数组单元格。
4.  **信息反馈区**：
    *   **状态/步骤说明面板**：实时用文字描述当前算法步骤、比较结果和决策。
    *   **堆属性显示**：显示当前堆类型（大顶堆/小顶堆）、大小等基本信息。
5.  **高级选项（可选或后续扩展）**：
    *   堆类型切换（大顶堆/小顶堆）。
    *   动画速度调节滑块。
    *   初始堆数据自定义输入。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>堆的插入与删除动画 - 上浮与下沉</title>
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
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #4A90E2;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .control-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            align-items: center;
        }
        
        .control-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }
        
        label {
            font-weight: 600;
            color: #2c3e50;
            font-size: 0.9rem;
        }
        
        input[type="number"] {
            padding: 10px 15px;
            border: 2px solid #e0e0e0;
            border-radius: 6px;
            font-size: 1rem;
            width: 120px;
            transition: border-color 0.3s;
        }
        
        input[type="number"]:focus {
            border-color: #4A90E2;
            outline: none;
        }
        
        .btn {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
            font-size: 0.95rem;
        }
        
        .btn-primary {
            background-color: #4A90E2;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #3a7bc8;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: #F5A623;
            color: white;
        }
        
        .btn-secondary:hover {
            background-color: #e0951a;
            transform: translateY(-2px);
        }
        
        .btn-control {
            background-color: #7ED321;
            color: white;
        }
        
        .btn-control:hover {
            background-color: #6cbb1a;
            transform: translateY(-2px);
        }
        
        .btn-reset {
            background-color: #e74c3c;
            color: white;
        }
        
        .btn-reset:hover {
            background-color: #c0392b;
            transform: translateY(-2px);
        }
        
        .btn:disabled {
            background-color: #bdc3c7;
            cursor: not-allowed;
            transform: none;
        }
        
        .visualization-area {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }
        
        .visualization-panel {
            flex: 1;
            min-width: 300px;
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-direction: column;
        }
        
        .panel-title {
            font-size: 1.2rem;
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #ecf0f1;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .heap-type {
            font-size: 0.9rem;
            background-color: #4A90E2;
            color: white;
            padding: 4px 10px;
            border-radius: 20px;
        }
        
        .tree-container, .array-container {
            flex: 1;
            position: relative;
            min-height: 350px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .info-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .info-title {
            font-size: 1.2rem;
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #ecf0f1;
        }
        
        .status-box {
            background-color: #f9f9f9;
            border-left: 4px solid #4A90E2;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 0 6px 6px 0;
            min-height: 80px;
        }
        
        .status-text {
            font-size: 1rem;
            line-height: 1.5;
        }
        
        .step-highlight {
            color: #4A90E2;
            font-weight: 600;
        }
        
        .comparison-highlight {
            color: #F5A623;
            font-weight: 600;
        }
        
        .heap-properties {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 15px;
        }
        
        .property {
            background-color: #f8f9fa;
            padding: 12px;
            border-radius: 6px;
            text-align: center;
        }
        
        .property-label {
            font-size: 0.85rem;
            color: #7f8c8d;
            margin-bottom: 5px;
        }
        
        .property-value {
            font-size: 1.2rem;
            font-weight: 600;
            color: #2c3e50;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #ecf0f1;
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
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #ecf0f1;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .visualization-area {
                flex-direction: column;
            }
            
            .control-panel {
                flex-direction: column;
                align-items: stretch;
            }
            
            .btn-group {
                display: grid;
                grid-template-columns: 1fr 1fr;
                gap: 10px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>堆的插入与删除动画</h1>
        <p class="subtitle">可视化上浮与下沉操作 · 完全二叉树与数组双视图</p>
    </header>
    
    <div class="container">
        <div class="control-panel">
            <div class="control-group">
                <label for="inputValue">插入数值</label>
                <input type="number" id="inputValue" min="1" max="99" value="15" placeholder="1-99">
            </div>
            
            <div class="btn-group">
                <button id="insertBtn" class="btn btn-primary">插入节点</button>
                <button id="deleteBtn" class="btn btn-secondary">删除堆顶</button>
            </div>
            
            <div class="control-group">
                <label>动画控制</label>
                <div style="display: flex; gap: 10px;">
                    <button id="playPauseBtn" class="btn btn-control">单步播放</button>
                    <button id="nextStepBtn" class="btn btn-control">下一步</button>
                    <button id="resetBtn" class="btn btn-reset">重置堆</button>
                </div>
            </div>
            
            <div class="control-group">
                <label>动画速度</label>
                <input type="range" id="speedSlider" min="100" max="1000" value="500" step="100">
            </div>
        </div>
        
        <div class="visualization-area">
            <div class="visualization-panel">
                <div class="panel-title">
                    <span>完全二叉树视图</span>
                    <span class="heap-type">大顶堆</span>
                </div>
                <div class="tree-container">
                    <svg id="treeSvg" width="100%" height="100%"></svg>
                </div>
            </div>
            
            <div class="visualization-panel">
                <div class="panel-title">
                    <span>数组存储视图</span>
                    <span class="heap-type">索引映射</span>
                </div>
                <div class="array-container" id="arrayContainer">
                    <!-- 数组元素将通过JS动态生成 -->
                </div>
            </div>
        </div>
        
        <div class="info-panel">
            <div class="info-title">算法状态与说明</div>
            <div class="status-box">
                <div class="status-text" id="statusText">就绪。堆已初始化，可以执行插入或删除操作。</div>
            </div>
            
            <div class="heap-properties">
                <div class="property">
                    <div class="property-label">堆大小</div>
                    <div class="property-value" id="heapSize">7</div>
                </div>
                <div class="property">
                    <div class="property-label">堆顶元素</div>
                    <div class="property-value" id="heapTop">50</div>
                </div>
                <div class="property">
                    <div class="property-label">当前操作</div>
                    <div class="property-value" id="currentOp">无</div>
                </div>
                <div class="property">
                    <div class="property-label">动画速度</div>
                    <div class="property-value" id="speedValue">中速</div>
                </div>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #4A90E2;"></div>
                    <div class="legend-text">活动节点（当前操作焦点）</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #F5A623;"></div>
                    <div class="legend-text">比较节点（父节点/子节点）</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #FFD700;"></div>
                    <div class="legend-text">交换过程</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #7ED321;"></div>
                    <div class="legend-text">操作完成</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #e8e8e8;"></div>
                    <div class="legend-text">普通节点</div>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>堆的插入与删除动画教学工具 | 设计：飞象老师 | 使用HTML5 SVG实现</p>
    </footer>

    <script>
        // 堆数据结构与动画状态
        class HeapAnimation {
            constructor() {
                // 初始堆数据（大顶堆）
                this.heap = [50, 30, 40, 10, 20, 35, 25];
                this.heapType = "max"; // "max" 或 "min"
                
                // 动画状态
                this.isAnimating = false;
                this.animationQueue = [];
                this.currentStep = 0;
                this.animationSpeed = 500; // 毫秒
                this.autoPlay = false;
                this.animationInterval = null;
                
                // 当前操作状态
                this.currentOperation = null; // "insert", "delete"
                this.activeNodeIndex = -1;
                this.comparingNodeIndex = -1;
                this.swappingNodes = [];
                this.operationSteps = [];
                this.stepIndex = 0;
                
                // DOM 元素
                this.treeSvg = document.getElementById('treeSvg');
                this.arrayContainer = document.getElementById('arrayContainer');
                this.statusText = document.getElementById('statusText');
                this.heapSizeElement = document.getElementById('heapSize');
                this.heapTopElement = document.getElementById('heapTop');
                this.currentOpElement = document.getElementById('currentOp');
                this.speedValueElement = document.getElementById('speedValue');
                
                // 初始化
                this.initEventListeners();
                this.updateHeapProperties();
                this.renderHeap();
            }
            
            initEventListeners() {
                // 插入按钮
                document.getElementById('insertBtn').addEventListener('click', () => {
                    const inputValue = parseInt(document.getElementById('inputValue').value);
                    if (!isNaN(inputValue) && inputValue >= 1 && inputValue <= 99) {
                        this.insertValue(inputValue);
                    } else {
                        this.updateStatus("请输入1-99之间的有效数字", "error");
                    }
                });
                
                // 删除按钮
                document.getElementById('deleteBtn').addEventListener('click', () => {
                    this.deleteRoot();
                });
                
                // 播放/暂停按钮
                document.getElementById('playPauseBtn').addEventListener('click', () => {
                    this.togglePlayPause();
                });
                
                // 下一步按钮
                document.getElementById('nextStepBtn').addEventListener('click', () => {
                    this.nextStep();
                });
                
                // 重置按钮
                document.getElementById('resetBtn').addEventListener('click', () => {
                    this.resetHeap();
                });
                
                // 速度滑块
                document.getElementById('speedSlider').addEventListener('input', (e) => {
                    this.animationSpeed = 1100 - e.target.value; // 反转值，使滑块向右速度更快
                    this.updateSpeedDisplay();
                    
                    // 如果正在自动播放，更新间隔
                    if (this.autoPlay) {
                        clearInterval(this.animationInterval);
                        this.startAutoPlay();
                    }
                });
                
                // 输入框回车键支持
                document.getElementById('inputValue').addEventListener('keypress', (e) => {
                    if (e.key === 'Enter') {
                        document.getElementById('insertBtn').click();
                    }
                });
            }
            
            // 插入值到堆中
            insertValue(value) {
                if (this.isAnimating) {
                    this.updateStatus("当前有动画正在执行，请等待完成", "warning");
                    return;
                }
                
                this.currentOperation = "insert";
                this.currentOpElement.textContent = "插入";
                
                // 添加新元素到堆末尾
                this.heap.push(value);
                this.activeNodeIndex = this.heap.length - 1;
                
                // 生成上浮操作的步骤
                this.generateUpwardSteps();
                
                // 开始动画
                this.startOperation();
            }
            
            // 删除堆顶元素
            deleteRoot() {
                if (this.isAnimating) {
                    this.updateStatus("当前有动画正在执行，请等待完成", "warning");
                    return;
                }
                
                if (this.heap.length === 0) {
                    this.updateStatus("堆为空，无法删除", "error");
                    return;
                }
                
                this.currentOperation = "delete";
                this.currentOpElement.textContent = "删除";
                
                // 生成删除操作的步骤
                this.generateDownwardSteps();
                
                // 开始动画
                this.startOperation();
            }
            
            // 生成上浮（插入）操作的步骤
            generateUpwardSteps() {
                this.operationSteps = [];
                let currentIndex = this.heap.length - 1;
                
                // 步骤1: 高亮新插入的节点
                this.operationSteps.push({
                    type: "highlight",
                    nodeIndex: currentIndex,
                    description: `新节点 ${this.heap[currentIndex]} 插入到堆末尾`
                });
                
                // 上浮过程
                while (currentIndex > 0) {
                    const parentIndex = Math.floor((currentIndex - 1) / 2);
                    
                    // 步骤: 高亮父节点进行比较
                    this.operationSteps.push({
                        type: "compare",
                        nodeIndex: currentIndex,
                        compareIndex: parentIndex,
                        description: `比较新节点 ${this.heap[currentIndex]} 与父节点 ${this.heap[parentIndex]}`
                    });
                    
                    // 检查是否需要交换（大顶堆：子节点 > 父节点）
                    const needSwap = this.heapType === "max" 
                        ? this.heap[currentIndex] > this.heap[parentIndex]
                        : this.heap[currentIndex] < this.heap[parentIndex];
                    
                    if (needSwap) {
                        // 步骤: 执行交换
                        this.operationSteps.push({
                            type: "swap",
                            nodeIndex: currentIndex,
                            compareIndex: parentIndex,
                            description: `${this.heap[currentIndex]} > ${this.heap[parentIndex]}，执行交换`
                        });
                        
                        // 交换堆中的值
                        [this.heap[currentIndex], this.heap[parentIndex]] = 
                        [this.heap[parentIndex], this.heap[currentIndex]];
                        
                        // 步骤: 交换完成，更新活动节点
                        this.operationSteps.push({
                            type: "move",
                            nodeIndex: parentIndex,
                            description: `节点 ${this.heap[parentIndex]} 上浮到新位置`
                        });
                        
                        currentIndex = parentIndex;
                    } else {
                        // 不需要交换，上浮结束
                        this.operationSteps.push({
                            type: "no_swap",
                            nodeIndex: currentIndex,
                            compareIndex: parentIndex,
                            description: `${this.heap[currentIndex]} ≤ ${this.heap[parentIndex]}，上浮停止`
                        });
                        break;
                    }
                }
                
                // 最后一步: 操作完成
                this.operationSteps.push({
                    type: "complete",
                    description: `插入完成，堆大小: ${this.heap.length}`
                });
            }
            
            // 生成下沉（删除）操作的步骤
            generateDownwardSteps() {
                this.operationSteps = [];
                
                if (this.heap.length === 0) return;
                
                // 步骤1: 高亮堆顶元素（将被删除）
                this.operationSteps.push({
                    type: "highlight",
                    nodeIndex: 0,
                    description: `准备删除堆顶元素 ${this.heap[0]}`
                });
                
                // 保存被删除的值
                const removedValue = this.heap[0];
                
                // 如果堆只有一个元素，直接删除
                if (this.heap.length === 1) {
                    this.heap.pop();
                    this.operationSteps.push({
                        type: "complete",
                        description: `删除完成，堆顶元素 ${removedValue} 已移除，堆现在为空`
                    });
                    return;
                }
                
                // 将最后一个元素移到堆顶
                const lastValue = this.heap[this.heap.length - 1];
                this.heap[0] = lastValue;
                this.heap.pop();
                
                // 步骤2: 将末尾元素移到堆顶
                this.operationSteps.push({
                    type: "move_to_root",
                    nodeIndex: 0,
                    description: `将末尾元素 ${lastValue} 移动到堆顶`
                });
                
                this.activeNodeIndex = 0;
                
                // 下沉过程
                let currentIndex = 0;
                const heapSize = this.heap.length;
                
                while (true) {
                    let leftChildIndex = 2 * currentIndex + 1;
                    let rightChildIndex = 2 * currentIndex + 2;
                    let targetIndex = currentIndex;
                    
                    // 如果没有子节点，停止下沉
                    if (leftChildIndex >= heapSize) {
                        this.operationSteps.push({
                            type: "no_child",
                            nodeIndex: currentIndex,
                            description: `节点 ${this.heap[currentIndex]} 没有子节点，下沉停止`
                        });
                        break;
                    }
                    
                    // 找到需要比较的子节点（大顶堆：找较大的子节点）
                    let compareIndex = leftChildIndex;
                    
                    if (rightChildIndex < heapSize) {
                        if (this.heapType === "max") {
                            compareIndex = this.heap[leftChildIndex] > this.heap[rightChildIndex] 
                                ? leftChildIndex : rightChildIndex;
                        } else {
                            compareIndex = this.heap[leftChildIndex] < this.heap[rightChildIndex] 
                                ? leftChildIndex : rightChildIndex;
                        }
                    }
                    
                    // 步骤: 高亮子节点进行比较
                    this.operationSteps.push({
                        type: "compare",
                        nodeIndex: currentIndex,
                        compareIndex: compareIndex,
                        description: `比较节点 ${this.heap[currentIndex]} 与子节点 ${this.heap[compareIndex]}`
                    });
                    
                    // 检查是否需要交换
                    const needSwap = this.heapType === "max"
                        ? this.heap[compareIndex] > this.heap[currentIndex]
                        : this.heap[compareIndex] < this.heap[currentIndex];
                    
                    if (needSwap) {
                        // 步骤: 执行交换
                        this.operationSteps.push({
                            type: "swap",
                            nodeIndex: currentIndex,
                            compareIndex: compareIndex,
                            description: `${this.heap[compareIndex]} > ${this.heap[currentIndex]}，执行交换`
                        });
                        
                        // 交换堆中的值
                        [this.heap[currentIndex], this.heap[compareIndex]] = 
                        [this.heap[compareIndex], this.heap[currentIndex]];
                        
                        // 步骤: 交换完成，更新活动节点
                        this.operationSteps.push({
                            type: "move",
                            nodeIndex: compareIndex,
                            description: `节点 ${this.heap[compareIndex]} 下沉到新位置`
                        });
                        
                        currentIndex = compareIndex;
                    } else {
                        // 不需要交换，下沉结束
                        this.operationSteps.push({
                            type: "no_swap",
                            nodeIndex: currentIndex,
                            compareIndex: compareIndex,
                            description: `${this.heap[compareIndex]} ≤ ${this.heap[currentIndex]}，下沉停止`
                        });
                        break;
                    }
                }
                
                // 最后一步: 操作完成
                this.operationSteps.push({
                    type: "complete",
                    description: `删除完成，堆顶元素 ${removedValue} 已移除，新堆顶: ${this.heap.length > 0 ? this.heap[0] : "空"}`
                });
            }
            
            // 开始操作
            startOperation() {
                this.isAnimating = true;
                this.stepIndex = 0;
                this.updateStatus("准备开始操作...", "info");
                this.updateControlButtons();
                
                // 执行第一步
                this.nextStep();
            }
            
            // 执行下一步
            nextStep() {
                if (!this.isAnimating || this.stepIndex >= this.operationSteps.length) {
                    this.completeOperation();
                    return;
                }
                
                const step = this.operationSteps[this.stepIndex];
                this.executeStep(step);
                this.stepIndex++;
                
                // 如果自动播放且还有步骤，设置定时器执行下一步
                if (this.autoPlay && this.stepIndex < this.operationSteps.length) {
                    clearInterval(this.animationInterval);
                    this.animationInterval = setTimeout(() => {
                        this.nextStep();
                    }, this.animationSpeed);
                }
            }
            
            // 执行单个步骤
            executeStep(step) {
                // 更新状态文本
                this.updateStatus(step.description, "step");
                
                // 根据步骤类型执行相应操作
                switch (step.type) {
                    case "highlight":
                        this.activeNodeIndex = step.nodeIndex;
                        this.comparingNodeIndex = -1;
                        this.swappingNodes = [];
                        break;
                        
                    case "compare":
                        this.activeNodeIndex = step.nodeIndex;
                        this.comparingNodeIndex = step.compareIndex;
                        this.swappingNodes = [];
                        break;
                        
                    case "swap":
                        this.activeNodeIndex = step.nodeIndex;
                        this.comparingNodeIndex = step.compareIndex;
                        this.swappingNodes = [step.nodeIndex, step.compareIndex];
                        break;
                        
                    case "move":
                        this.activeNodeIndex = step.nodeIndex;
                        this.comparingNodeIndex = -1;
                        this.swappingNodes = [];
                        break;
                        
                    case "move_to_root":
                        this.activeNodeIndex = step.nodeIndex;
                        this.comparingNodeIndex = -1;
                        this.swappingNodes = [];
                        break;
                        
                    case "no_swap":
                    case "no_child":
                        this.activeNodeIndex = step.nodeIndex;
                        this.comparingNodeIndex = step.compareIndex;
                        this.swappingNodes = [];
                        break;
                        
                    case "complete":
                        this.activeNodeIndex = -1;
                        this.comparingNodeIndex = -1;
                        this.swappingNodes = [];
                        break;
                }
                
                // 重新渲染堆
                this.renderHeap();
                
                // 如果是完成步骤，准备结束操作
                if (step.type === "complete") {
                    setTimeout(() => {
                        this.completeOperation();
                    }, this.animationSpeed);
                }
            }
            
            // 完成操作
            completeOperation() {
                this.isAnimating = false;
                this.currentOperation = null;
                this.activeNodeIndex = -1;
                this.comparingNodeIndex = -1;
                this.swappingNodes = [];
                this.operationSteps = [];
                this.stepIndex = 0;
                
                this.updateHeapProperties();
                this.renderHeap();
                this.updateControlButtons();
                this.currentOpElement.textContent = "无";
                
                if (this.autoPlay) {
                    this.autoPlay = false;
                    document.getElementById('playPauseBtn').textContent = "单步播放";
                }
            }
            
            // 切换播放/暂停
            togglePlayPause() {
                if (!this.isAnimating) {
                    this.updateStatus("没有正在执行的操作", "warning");
                    return;
                }
                
                this.autoPlay = !this.autoPlay;
                
                if (this.autoPlay) {
                    document.getElementById('playPauseBtn').textContent = "暂停";
                    this.startAutoPlay();
                } else {
                    document.getElementById('playPauseBtn').textContent = "单步播放";
                    clearInterval(this.animationInterval);
                }
            }
            
            // 开始自动播放
            startAutoPlay() {
                if (this.autoPlay && this.isAnimating && this.stepIndex < this.operationSteps.length) {
                    this.animationInterval = setTimeout(() => {
                        this.nextStep();
                    }, this.animationSpeed);
                }
            }
            
            // 重置堆
            resetHeap() {
                if (this.isAnimating) {
                    this.updateStatus("请先完成当前动画", "warning");
                    return;
                }
                
                this.heap = [50, 30, 40, 10, 20, 35, 25];
                this.isAnimating = false;
                this.autoPlay = false;
                this.currentOperation = null;
                this.activeNodeIndex = -1;
                this.comparingNodeIndex = -1;
                this.swappingNodes = [];
                this.operationSteps = [];
                this.stepIndex = 0;
                
                clearInterval(this.animationInterval);
                document.getElementById('playPauseBtn').textContent = "单步播放";
                
                this.updateHeapProperties();
                this.renderHeap();
                this.updateControlButtons();
                this.updateStatus("堆已重置为初始状态", "info");
                this.currentOpElement.textContent = "无";
            }
            
            // 更新堆属性显示
            updateHeapProperties() {
                this.heapSizeElement.textContent = this.heap.length;
                this.heapTopElement.textContent = this.heap.length > 0 ? this.heap[0] : "空";
            }
            
            // 更新速度显示
            updateSpeedDisplay() {
                let speedText = "中速";
                if (this.animationSpeed < 300) speedText = "快速";
                else if (this.animationSpeed > 700) speedText = "慢速";
                
                this.speedValueElement.textContent = speedText;
            }
            
            // 更新状态文本
            updateStatus(text, type = "info") {
                let styledText = text;
                
                if (type === "step") {
                    styledText = `<span class="step-highlight">${text}</span>`;
                } else if (type === "comparison") {
                    styledText = `<span class="comparison-highlight">${text}</span>`;
                }
                
                this.statusText.innerHTML = styledText;
            }
            
            // 更新控制按钮状态
            updateControlButtons() {
                const insertBtn = document.getElementById('insertBtn');
                const deleteBtn = document.getElementById('deleteBtn');
                const playPauseBtn = document.getElementById('playPauseBtn');
                const nextStepBtn = document.getElementById('nextStepBtn');
                
                if (this.isAnimating) {
                    insertBtn.disabled = true;
                    deleteBtn.disabled = true;
                    playPauseBtn.disabled = false;
                    nextStepBtn.disabled = false;
                } else {
                    insertBtn.disabled = false;
                    deleteBtn.disabled = false;
                    playPauseBtn.disabled = true;
                    nextStepBtn.disabled = true;
                }
            }
            
            // 渲染堆（二叉树和数组视图）
            renderHeap() {
                this.renderTree();
                this.renderArray();
            }
            
            // 渲染二叉树视图
            renderTree() {
                // 清空SVG
                this.treeSvg.innerHTML = '';
                
                if (this.heap.length === 0) {
                    const text = this.treeSvg.appendChild(document.createElementNS('http://www.w3.org/2000/svg', 'text'));
                    text.setAttribute('x', '50%');
                    text.setAttribute('y', '50%');
                    text.setAttribute('text-anchor', 'middle');
                    text.setAttribute('dominant-baseline', 'middle');
                    text.setAttribute('fill', '#7f8c8d');
                    text.textContent = '堆为空';
                    return;
                }
                
                const svgWidth = this.treeSvg.clientWidth;
                const svgHeight = this.treeSvg.clientHeight;
                
                // 计算树的高度
                const treeHeight = Math.floor(Math.log2(this.heap.length)) + 1;
                
                // 节点半径
                const nodeRadius = Math.min(30, svgWidth / (Math.pow(2, treeHeight) * 2));
                
                // 计算节点位置
                const positions = [];
                const levelHeight = (svgHeight - 100) / treeHeight;
                
                for (let i = 0; i < this.heap.length; i++) {
                    const level = Math.floor(Math.log2(i + 1));
                    const nodesInLevel = Math.pow(2, level);
                    const indexInLevel = i + 1 - Math.pow(2, level);
                    
                    const x = (indexInLevel + 0.5) * (svgWidth / nodesInLevel);
                    const y = 50 + level * levelHeight;
                    
                    positions.push({x, y});
                }
                
                // 绘制连接线
                for (let i = 0; i < this.heap.length; i++) {
                    const leftChildIndex = 2 * i + 1;
                    const rightChildIndex = 2 * i + 2;
                    
                    if (leftChildIndex < this.heap.length) {
                        this.drawLine(positions[i], positions[leftChildIndex]);
                    }
                    
                    if (rightChildIndex < this.heap.length) {
                        this.drawLine(positions[i], positions[rightChildIndex]);
                    }
                }
                
                // 绘制节点
                for (let i = 0; i < this.heap.length; i++) {
                    this.drawTreeNode(i, positions[i].x, positions[i].y, nodeRadius);
                }
            }
            
            // 绘制树节点
            drawTreeNode(index, x, y, radius) {
                // 确定节点颜色
                let fillColor = '#e8e8e8'; // 默认颜色
                let strokeColor = '#333';
                let strokeWidth = 2;
                
                if (index === this.activeNodeIndex) {
                    fillColor = '#4A90E2'; // 活动节点
                    strokeColor = '#2c3e50';
                } else if (index === this.comparingNodeIndex) {
                    fillColor = '#F5A623'; // 比较节点
                    strokeColor = '#d35400';
                } else if (this.swappingNodes.includes(index)) {
                    fillColor = '#FFD700'; // 交换节点
                    strokeColor = '#f39c12';
                }
                
                // 绘制圆形节点
                const circle = document.createElementNS('http://www.w3.org/2000/svg', 'circle');
                circle.setAttribute('cx', x);
                circle.setAttribute('cy', y);
                circle.setAttribute('r', radius);
                circle.setAttribute('fill', fillColor);
                circle.setAttribute('stroke', strokeColor);
                circle.setAttribute('stroke-width', strokeWidth);
                this.treeSvg.appendChild(circle);
                
                // 绘制节点文本
                const text = document.createElementNS('http://www.w3.org/2000/svg', 'text');
                text.setAttribute('x', x);
                text.setAttribute('y', y);
                text.setAttribute('text-anchor', 'middle');
                text.setAttribute('dominant-baseline', 'middle');
                text.setAttribute('fill', strokeColor);
                text.setAttribute('font-weight', '600');
                text.setAttribute('font-size', Math.min(radius * 0.6, 16));
                text.textContent = this.heap[index];
                this.treeSvg.appendChild(text);
                
                // 绘制索引文本（小字）
                const indexText = document.createElementNS('http://www.w3.org/2000/svg', 'text');
                indexText.setAttribute('x', x);
                indexText.setAttribute('y', y + radius + 15);
                indexText.setAttribute('text-anchor', 'middle');
                indexText.setAttribute('dominant-baseline', 'middle');
                indexText.setAttribute('fill', '#7f8c8d');
                indexText.setAttribute('font-size', Math.min(radius * 0.4, 12));
                indexText.textContent = `[${index}]`;
                this.treeSvg.appendChild(indexText);
            }
            
            // 绘制连接线
            drawLine(startPos, endPos) {
                const line = document.createElementNS('http://www.w3.org/2000/svg', 'line');
                line.setAttribute('x1', startPos.x);
                line.setAttribute('y1', startPos.y);
                line.setAttribute('x2', endPos.x);
                line.setAttribute('y2', endPos.y);
                line.setAttribute('stroke', '#95a5a6');
                line.setAttribute('stroke-width', 2);
                this.treeSvg.appendChild(line);
            }
            
            // 渲染数组视图
            renderArray() {
                // 清空数组容器
                this.arrayContainer.innerHTML = '';
                
                if (this.heap.length === 0) {
                    const emptyMsg =
<!--检测到代码截断，自动续写中...-->
const emptyMsg = document.createElement('div');
                    emptyMsg.style.textAlign = 'center';
                    emptyMsg.style.padding = '40px';
                    emptyMsg.style.color = '#7f8c8d';
                    emptyMsg.textContent = '数组为空';
                    this.arrayContainer.appendChild(emptyMsg);
                    return;
                }
                
                // 创建数组容器
                const arrayVisual = document.createElement('div');
                arrayVisual.style.display = 'flex';
                arrayVisual.style.flexWrap = 'wrap';
                arrayVisual.style.justifyContent = 'center';
                arrayVisual.style.gap = '10px';
                arrayVisual.style.padding = '20px';
                
                // 创建每个数组元素
                for (let i = 0; i < this.heap.length; i++) {
                    const arrayElement = document.createElement('div');
                    arrayElement.style.display = 'flex';
                    arrayElement.style.flexDirection = 'column';
                    arrayElement.style.alignItems = 'center';
                    arrayElement.style.gap = '5px';
                    
                    // 确定元素颜色
                    let bgColor = '#e8e8e8'; // 默认颜色
                    let borderColor = '#333';
                    let textColor = '#333';
                    
                    if (i === this.activeNodeIndex) {
                        bgColor = '#4A90E2'; // 活动节点
                        borderColor = '#2c3e50';
                        textColor = 'white';
                    } else if (i === this.comparingNodeIndex) {
                        bgColor = '#F5A623'; // 比较节点
                        borderColor = '#d35400';
                        textColor = 'white';
                    } else if (this.swappingNodes.includes(i)) {
                        bgColor = '#FFD700'; // 交换节点
                        borderColor = '#f39c12';
                        textColor = '#333';
                    }
                    
                    // 索引显示
                    const indexDiv = document.createElement('div');
                    indexDiv.textContent = `索引 ${i}`;
                    indexDiv.style.fontSize = '0.8rem';
                    indexDiv.style.color = '#7f8c8d';
                    arrayElement.appendChild(indexDiv);
                    
                    // 值显示框
                    const valueDiv = document.createElement('div');
                    valueDiv.textContent = this.heap[i];
                    valueDiv.style.width = '60px';
                    valueDiv.style.height = '60px';
                    valueDiv.style.display = 'flex';
                    valueDiv.style.alignItems = 'center';
                    valueDiv.style.justifyContent = 'center';
                    valueDiv.style.backgroundColor = bgColor;
                    valueDiv.style.border = `3px solid ${borderColor}`;
                    valueDiv.style.borderRadius = '8px';
                    valueDiv.style.fontSize = '1.4rem';
                    valueDiv.style.fontWeight = 'bold';
                    valueDiv.style.color = textColor;
                    valueDiv.style.transition = 'all 0.3s ease';
                    arrayElement.appendChild(valueDiv);
                    
                    // 父/子索引关系提示
                    const relationDiv = document.createElement('div');
                    relationDiv.style.fontSize = '0.7rem';
                    relationDiv.style.color = '#95a5a6';
                    relationDiv.style.textAlign = 'center';
                    relationDiv.style.minHeight = '30px';
                    
                    // 计算父节点和子节点索引
                    const parentIndex = i > 0 ? Math.floor((i - 1) / 2) : null;
                    const leftChildIndex = 2 * i + 1;
                    const rightChildIndex = 2 * i + 2;
                    
                    let relationText = '';
                    if (parentIndex !== null) {
                        relationText += `父: [${parentIndex}]`;
                    }
                    
                    if (leftChildIndex < this.heap.length) {
                        if (relationText) relationText += ' | ';
                        relationText += `左子: [${leftChildIndex}]`;
                    }
                    
                    if (rightChildIndex < this.heap.length) {
                        if (relationText) relationText += ' | ';
                        relationText += `右子: [${rightChildIndex}]`;
                    }
                    
                    relationDiv.textContent = relationText;
                    arrayElement.appendChild(relationDiv);
                    
                    arrayVisual.appendChild(arrayElement);
                }
                
                this.arrayContainer.appendChild(arrayVisual);
            }
        }
        
        // 页面加载完成后初始化动画
        document.addEventListener('DOMContentLoaded', () => {
            const heapAnimation = new HeapAnimation();
            
            // 将实例附加到window对象以便调试
            window.heapAnimation = heapAnimation;
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 堆的插入与删除动画 - 交互式教学工具使用指南

欢迎使用“堆的插入与删除动画”交互式教学工具！本工具旨在通过可视化方式帮助您深入理解堆数据结构的关键操作——插入（上浮）与删除（下沉）。无论您是数据结构初学者还是希望巩固知识的进阶学习者，本工具都将为您提供直观、互动的学习体验。

---

### 一、功能说明

本工具是一个基于HTML5 SVG技术的交互式教学动画，专门用于演示**大顶堆**的插入与删除操作。通过双视图同步展示（完全二叉树视图 + 数组存储视图），您可以清晰地观察到：

1. **插入操作（上浮）**：新元素如何从堆末尾插入，并通过与父节点比较逐层上浮至合适位置。
2. **删除操作（下沉）**：堆顶元素被移除后，末尾元素如何移至堆顶，并通过与子节点比较逐层下沉至合适位置。

所有操作均以动画形式呈现，配有详细的步骤说明，让抽象的算法过程变得具体可见。

---

### 二、主要功能

#### 1. 核心操作区
- **插入节点**：在输入框中输入1-99之间的数值，点击“插入节点”按钮，观察新元素如何被插入堆中并执行上浮操作。
- **删除堆顶**：点击“删除堆顶”按钮，观察堆顶元素如何被移除，以及堆如何通过下沉操作重新调整。

#### 2. 动画控制区
- **单步播放/暂停**：在动画执行过程中，切换自动播放与暂停模式。
- **下一步**：在暂停模式下，手动执行下一个算法步骤（一次比较或一次交换）。
- **重置堆**：将堆恢复到初始状态 [50, 30, 40, 10, 20, 35, 25]。

#### 3. 可视化区域
- **左侧：完全二叉树视图**
  - 以树形结构直观展示堆的逻辑形态
  - 节点显示数值和索引
  - 动态高亮显示当前操作涉及的元素
- **右侧：数组存储视图**
  - 展示堆在内存中的实际存储方式
  - 显示每个元素的索引和父子关系
  - 与二叉树视图同步更新

#### 4. 信息反馈区
- **算法状态与说明**：实时显示当前执行的操作步骤、比较结果和决策逻辑。
- **堆属性显示**：展示当前堆的大小、堆顶元素、当前操作类型和动画速度。
- **图例说明**：解释不同颜色代表的节点状态。

---

### 三、设计特色

#### 1. 双视图同步设计
- **逻辑与物理视图结合**：同时展示堆的完全二叉树表示（逻辑结构）和数组表示（物理存储），帮助理解两者之间的映射关系。
- **颜色编码系统**：
  - 🔵 **蓝色**：活动节点（当前操作焦点）
  - 🟠 **橙色**：比较节点（父节点或子节点）
  - 🟡 **黄色**：交换过程中的节点
  - 🟢 **绿色**：操作完成提示

#### 2. 渐进式学习支持
- **步骤可控**：支持自动播放和手动单步执行，适应不同学习节奏。
- **速度可调**：通过滑块调整动画速度（慢速/中速/快速）。
- **即时反馈**：每个步骤都有详细的文字说明，解释算法逻辑。

#### 3. 教学友好性
- **直观的父子关系显示**：在数组视图中明确标注每个元素的父节点和子节点索引。
- **完整的操作记录**：状态面板记录所有关键决策点。
- **错误预防**：输入验证和操作状态检查，防止无效操作。

---

### 四、教学要点

#### 理解堆的核心概念
1. **堆序性质**：在大顶堆中，每个节点的值都大于或等于其子节点的值。
2. **完全二叉树结构**：堆是一棵完全二叉树，可以用数组高效存储。
3. **索引计算**：
   - 父节点索引：`parent(i) = floor((i-1)/2)`
   - 左子节点索引：`left(i) = 2*i + 1`
   - 右子节点索引：`right(i) = 2*i + 2`

#### 掌握关键算法
1. **插入操作（上浮）流程**：
   - 将新元素添加到堆的末尾
   - 比较新元素与其父节点的值
   - 如果违反堆序性质，则交换两者位置
   - 重复此过程，直到堆序性质满足或到达根节点

2. **删除操作（下沉）流程**：
   - 移除堆顶元素（根节点）
   - 将最后一个元素移动到堆顶
   - 比较该元素与其子节点的值
   - 如果违反堆序性质，则与较大的子节点交换
   - 重复此过程，直到堆序性质满足或到达叶子节点

#### 观察学习重点
- **注意比较的方向**：插入时与父节点比较，删除时与子节点比较
- **理解交换的条件**：大顶堆中，子节点值 > 父节点值时需要交换（插入），父节点值 < 子节点值时需要交换（删除）
- **跟踪元素移动路径**：观察元素如何在树中“上浮”或“下沉”

---

### 五、使用建议

#### 对于初学者
1. **从观察开始**：先使用“插入节点”和“删除堆顶”按钮，完整观看几次操作流程。
2. **降低速度**：将动画速度调至“慢速”，仔细观察每一步的变化。
3. **关注对应关系**：注意二叉树节点与数组元素之间的对应关系，理解索引计算。
4. **阅读状态说明**：仔细阅读每一步的状态说明，理解算法决策逻辑。

#### 对于巩固学习者
1. **预测下一步**：在单步模式下，尝试预测下一步会发生什么，然后点击“下一步”验证。
2. **分析边界情况**：
   - 插入一个很大的数（如99），观察它如何快速上浮到堆顶
   - 插入一个很小的数（如5），观察它为什么不需要移动
   - 连续删除多次，观察堆如何逐渐变小
3. **思考时间复杂度**：通过动画理解插入和删除操作的O(log n)时间复杂度。

#### 教学场景建议
1. **课堂演示**：教师可使用本工具作为课堂辅助教学，直观展示堆操作过程。
2. **自主学习**：学生可按照自己的节奏探索堆的工作原理。
3. **实验练习**：配合编程练习，先通过可视化理解算法，再动手实现代码。

#### 最佳实践流程
1. **初始探索**：使用默认堆，执行几次插入和删除操作，熟悉界面和基本流程。
2. **深入观察**：选择一个特定值插入，使用单步模式仔细观察每一步的比较和交换。
3. **模式识别**：尝试不同数值的插入，总结上浮路径的规律。
4. **知识应用**：关闭动画，尝试在纸上模拟堆的插入删除过程，然后使用工具验证。

---

### 技术支持与反馈

本工具基于现代Web技术（HTML5、CSS3、SVG、JavaScript）开发，兼容主流现代浏览器。如果您在使用过程中遇到任何问题，或对功能有改进建议，欢迎通过以下方式反馈：

1. **操作问题**：确保使用Chrome、Firefox、Edge等现代浏览器的最新版本。
2. **学习疑问**：结合教材和在线资源，将可视化理解与理论学习相结合。
3. **功能建议**：本工具未来可扩展支持小顶堆、堆排序、堆构建等更多功能。

---

**祝您学习愉快，在数据结构的探索之旅中收获满满！**

*飞象老师 教学工具系列 · 让算法学习更直观*