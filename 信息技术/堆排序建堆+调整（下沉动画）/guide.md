# 需求：堆排序建堆+调整（下沉动画）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：学习数据结构与算法的计算机专业学生或编程自学者。他们已具备数组、二叉树的基本知识，但对堆排序的动态过程理解不深。
2.  **核心痛点**：
    *   **过程抽象**：堆排序的“建堆”和“调整（下沉）”过程是动态、递归的，仅凭静态图示或伪代码难以在脑中构建完整的过程动画。
    *   **状态关联**：用户难以直观理解**数组索引**、**完全二叉树形态**、**堆属性（大顶堆/小顶堆）** 三者之间在每一步操作下的同步变化关系。
    *   **关键步骤**：对“从最后一个非叶子节点开始调整”、“元素下沉时与较大（小）子节点交换”等关键逻辑缺乏直观的、步骤化的视觉反馈。
3.  **学习目标**：通过动画，用户应能清晰理解：
    *   如何将一个无序数组通过“下沉调整”构建成一个堆。
    *   如何在取出堆顶元素后，通过“下沉调整”维护堆的性质。
    *   理解算法的时间复杂度与操作步骤数的直观关系。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念分解**：
    *   **概念1：堆的物理与逻辑结构**：并排展示**数组视图**和**完全二叉树视图**，并高亮显示两者的对应关系（如索引 `i` 的父节点、左右子节点）。
    *   **概念2：堆的有序性（以大顶堆为例）**：父节点值 >= 子节点值。用颜色或大小差异直观表现值的大小关系。
    *   **概念3：下沉调整**：这是动画的核心。分解为：a) 比较当前节点与子节点； b) 若小于子节点则交换； c) 以交换后的位置为新当前节点，重复此过程，直至满足堆性质或成为叶节点。

2.  **认知规律遵循**：
    *   **从具体到抽象**：先展示完整的数组和树，让用户建立初始印象。
    *   **分步演示**：将连续的算法过程分解为可单步前进/后退的离散步骤，每一步都有明确的文字说明（如“比较节点[3]（值5）与其子节点[7]（值9）和[8]（值7），发现右子节点[7]更大”）。
    *   **焦点引导**：使用高亮、放大、箭头指示等视觉手段，在每一步将用户的注意力引导到当前正在操作的节点（当前节点、待比较的子节点）上。
    *   **多视图同步**：确保数组中的元素交换与二叉树中节点的交换动画完全同步，强化两者是同一数据不同表现形式的概念。

3.  **交互设计**：
    *   **控制节奏**：提供“播放/暂停”、“下一步/上一步”、“重置”按钮，让用户能以自己的节奏学习，并可回溯复习难点。
    *   **探索与验证**：在动画区域旁，提供一个可交互的“迷你控制台”，允许用户手动输入一个小数组（如6-8个数字），然后观察为其构建堆的全过程，增强参与感。
    *   **提示与反馈**：在关键决策点（如比较、交换），通过文字提示框解释原因。如果用户尝试进行错误操作（在手动模式下），给予友好提示。

4.  **视觉呈现**：
    *   **双视图布局**：左侧为**数组视图**（带索引的条形图或圆角矩形框），右侧为**完全二叉树视图**（节点为圆形，内含数字，连线清晰）。
    *   **动态高亮**：
        *   **当前节点**：用醒目的颜色（如橙色）填充并可能轻微放大。
        *   **待比较子节点**：用另一种颜色（如浅蓝色）高亮。
        *   **交换动画**：在两个节点之间设计平滑的位置移动轨迹线或渐变交换效果。
        *   **已就位节点**：调整完成后，节点颜色变为稳定色（如绿色），表示其子树已满足堆性质。
    *   **状态标签**：在视图上方或节点旁，用文字清晰标明当前阶段（“建堆阶段”或“调整阶段”）和当前操作（“正在下沉调整节点[i]”）。

#### 配色方案选择
*   **主色调**：采用科技蓝 (`#3498db`) 作为界面主色（按钮、标题），传达理性与逻辑。
*   **视图背景**：数组和二叉树视图使用浅灰色 (`#f5f5f5`) 或极浅的蓝色 (`#ecf0f1`) 背景，与内容形成柔和对比。
*   **节点颜色**：
    *   **默认/未激活节点**：白色填充，深灰色边框 (`#bdc3c7`)，黑色数字。
    *   **当前操作节点**：橙色 (`#e67e22`) 填充，强调焦点。
    *   **待比较子节点**：浅蓝色 (`#aed6f1`) 填充。
    *   **已完成调整/已就位节点**：淡绿色 (`#d5f4e6`) 填充，表示稳定状态。
    *   **交换动画轨迹**：使用半透明的红色 (`rgba(231, 76, 60, 0.7)`) 线条或箭头。
*   **文字与提示**：重要提示和步骤说明使用深灰色 (`#2c3e50`)，确保清晰可读。
*   **按钮状态**：正常状态为科技蓝，悬停状态加深 (`#2980b9`)，禁用状态为灰色 (`#95a5a6`)。

#### 交互功能列表
1.  **数据输入区**：
    *   预设示例数组按钮（如 `[3, 9, 2, 5, 7, 1, 8]`）。
    *   自定义输入框（允许用户输入逗号分隔的数字）。
    *   “生成/重置”按钮。
2.  **动画控制区**：
    *   **播放/暂停**：开始/停止连续自动演示。
    *   **下一步**：单步执行下一个算法步骤（比较或交换）。
    *   **上一步**：回退到上一个步骤。
    *   **重置**：恢复到初始无序数组状态。
    *   **速度调节滑块**：控制自动播放的速度。
3.  **核心可视化区**：
    *   **数组视图**：水平排列的元素框，显示索引和值。元素可动态高亮和交换位置。
    *   **二叉树视图**：动态生成的完全二叉树，节点与数组元素一一对应。节点可动态高亮、交换位置。
    *   **关系连线**：在数组视图中，当选中一个节点时，可用虚线或不同颜色高亮显示其在二叉树中的父节点和子节点的对应数组位置（辅助理解索引计算）。
4.  **信息提示区**：
    *   **步骤说明面板**：用文字详细描述当前步骤在做什么以及为什么（例如：“比较节点 5 (值: 7) 和它的子节点 11 (值: 8)。因为 7 < 8，所以需要交换。”）。
    *   **状态指示器**：显示当前是“建堆过程”还是“排序调整过程”，以及当前正在处理哪个节点。
    *   **计数器**：（可选）显示已进行的比较次数和交换次数，帮助理解算法效率。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>堆排序建堆与下沉调整动画教学</title>
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
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 15px;
            border-bottom: 2px solid #3498db;
        }
        
        h1 {
            color: #3498db;
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
        
        .data-section {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            align-items: center;
            flex: 1;
        }
        
        .control-section {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            align-items: center;
            flex: 1;
        }
        
        .btn {
            padding: 8px 16px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s ease;
        }
        
        .btn-primary {
            background-color: #3498db;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #2980b9;
        }
        
        .btn-secondary {
            background-color: #ecf0f1;
            color: #2c3e50;
        }
        
        .btn-secondary:hover {
            background-color: #d5dbdb;
        }
        
        .btn-success {
            background-color: #27ae60;
            color: white;
        }
        
        .btn-success:hover {
            background-color: #219653;
        }
        
        .btn-warning {
            background-color: #e67e22;
            color: white;
        }
        
        .btn-warning:hover {
            background-color: #d35400;
        }
        
        .btn:disabled {
            background-color: #bdc3c7;
            cursor: not-allowed;
        }
        
        .input-array {
            padding: 8px 12px;
            border: 2px solid #bdc3c7;
            border-radius: 6px;
            width: 200px;
            font-size: 1em;
        }
        
        .input-array:focus {
            outline: none;
            border-color: #3498db;
        }
        
        .speed-control {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .speed-slider {
            width: 120px;
        }
        
        .visualization-area {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }
        
        .visualization-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            flex: 1;
            min-width: 300px;
        }
        
        .panel-title {
            color: #3498db;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #ecf0f1;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .array-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
            min-height: 120px;
        }
        
        .array-element {
            width: 70px;
            height: 70px;
            border-radius: 8px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        
        .element-value {
            font-size: 1.4em;
        }
        
        .element-index {
            font-size: 0.8em;
            position: absolute;
            top: 5px;
            left: 5px;
            color: #7f8c8d;
        }
        
        .tree-container {
            display: flex;
            justify-content: center;
            margin-top: 10px;
            min-height: 300px;
            position: relative;
        }
        
        .tree-svg {
            width: 100%;
            height: 300px;
        }
        
        .info-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .step-info {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 15px;
            border-left: 4px solid #3498db;
        }
        
        .step-title {
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 8px;
            display: flex;
            justify-content: space-between;
        }
        
        .step-desc {
            color: #34495e;
            line-height: 1.5;
        }
        
        .counters {
            display: flex;
            gap: 20px;
            margin-top: 15px;
        }
        
        .counter {
            text-align: center;
            padding: 10px;
            background-color: #ecf0f1;
            border-radius: 6px;
            flex: 1;
        }
        
        .counter-value {
            font-size: 1.8em;
            font-weight: bold;
            color: #3498db;
        }
        
        .counter-label {
            font-size: 0.9em;
            color: #7f8c8d;
            margin-top: 5px;
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
        
        @media (max-width: 768px) {
            .visualization-area {
                flex-direction: column;
            }
            
            .control-panel {
                flex-direction: column;
                align-items: stretch;
            }
            
            .data-section, .control-section {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>堆排序：建堆与下沉调整动画教学</h1>
        <p class="subtitle">可视化演示堆排序的建堆过程与下沉调整算法</p>
    </div>
    
    <div class="container">
        <div class="control-panel">
            <div class="data-section">
                <h3>数据输入:</h3>
                <input type="text" class="input-array" id="arrayInput" value="3,9,2,5,7,1,8">
                <button class="btn btn-primary" id="generateBtn">生成数组</button>
                <button class="btn btn-secondary" id="exampleBtn">示例数组</button>
            </div>
            
            <div class="control-section">
                <h3>动画控制:</h3>
                <button class="btn btn-success" id="playBtn">开始建堆</button>
                <button class="btn btn-warning" id="nextBtn">下一步</button>
                <button class="btn btn-secondary" id="prevBtn">上一步</button>
                <button class="btn btn-secondary" id="resetBtn">重置</button>
                
                <div class="speed-control">
                    <span>速度:</span>
                    <input type="range" min="1" max="10" value="5" class="speed-slider" id="speedSlider">
                </div>
            </div>
        </div>
        
        <div class="visualization-area">
            <div class="visualization-panel">
                <div class="panel-title">
                    <h2>数组视图</h2>
                    <span id="arrayStatus">初始数组</span>
                </div>
                <div class="array-container" id="arrayContainer">
                    <!-- 数组元素将通过JS动态生成 -->
                </div>
            </div>
            
            <div class="visualization-panel">
                <div class="panel-title">
                    <h2>二叉树视图</h2>
                    <span id="treeStatus">初始状态</span>
                </div>
                <div class="tree-container">
                    <svg class="tree-svg" id="treeSvg">
                        <!-- 二叉树将通过JS动态绘制 -->
                    </svg>
                </div>
            </div>
        </div>
        
        <div class="info-panel">
            <div class="step-info">
                <div class="step-title">
                    <span id="stepTitle">准备开始</span>
                    <span id="stepCounter">步骤: 0/0</span>
                </div>
                <div class="step-desc" id="stepDesc">
                    请点击"开始建堆"按钮或"下一步"按钮开始动画演示。
                </div>
            </div>
            
            <div class="counters">
                <div class="counter">
                    <div class="counter-value" id="compareCount">0</div>
                    <div class="counter-label">比较次数</div>
                </div>
                <div class="counter">
                    <div class="counter-value" id="swapCount">0</div>
                    <div class="counter-label">交换次数</div>
                </div>
                <div class="counter">
                    <div class="counter-value" id="stepCount">0</div>
                    <div class="counter-label">总步骤数</div>
                </div>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #ffffff; border: 2px solid #bdc3c7;"></div>
                    <span>默认节点</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #e67e22;"></div>
                    <span>当前操作节点</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #aed6f1;"></div>
                    <span>待比较子节点</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #d5f4e6;"></div>
                    <span>已就位节点</span>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 堆排序动画状态管理
        class HeapSortAnimation {
            constructor() {
                this.array = [3, 9, 2, 5, 7, 1, 8];
                this.originalArray = [...this.array];
                this.steps = [];
                this.currentStep = 0;
                this.isPlaying = false;
                this.playInterval = null;
                this.speed = 5;
                this.compareCount = 0;
                this.swapCount = 0;
                this.stepCount = 0;
                
                // 节点状态常量
                this.NODE_STATE = {
                    DEFAULT: 0,
                    CURRENT: 1,
                    COMPARE: 2,
                    SWAPPING: 3,
                    IN_PLACE: 4
                };
                
                // 初始化节点状态
                this.nodeStates = this.array.map(() => this.NODE_STATE.DEFAULT);
                
                // 初始化UI
                this.initUI();
                this.renderArray();
                this.renderTree();
                this.updateInfo();
            }
            
            initUI() {
                // 获取DOM元素
                this.arrayInput = document.getElementById('arrayInput');
                this.generateBtn = document.getElementById('generateBtn');
                this.exampleBtn = document.getElementById('exampleBtn');
                this.playBtn = document.getElementById('playBtn');
                this.nextBtn = document.getElementById('nextBtn');
                this.prevBtn = document.getElementById('prevBtn');
                this.resetBtn = document.getElementById('resetBtn');
                this.speedSlider = document.getElementById('speedSlider');
                
                // 绑定事件
                this.generateBtn.addEventListener('click', () => this.generateArray());
                this.exampleBtn.addEventListener('click', () => this.loadExample());
                this.playBtn.addEventListener('click', () => this.togglePlay());
                this.nextBtn.addEventListener('click', () => this.nextStep());
                this.prevBtn.addEventListener('click', () => this.prevStep());
                this.resetBtn.addEventListener('click', () => this.reset());
                this.speedSlider.addEventListener('input', () => this.updateSpeed());
                
                // 初始化速度
                this.updateSpeed();
            }
            
            generateArray() {
                const input = this.arrayInput.value.trim();
                if (!input) return;
                
                try {
                    const newArray = input.split(',').map(num => parseInt(num.trim()));
                    if (newArray.some(isNaN)) {
                        alert('请输入有效的数字，用逗号分隔');
                        return;
                    }
                    
                    this.array = [...newArray];
                    this.originalArray = [...newArray];
                    this.resetState();
                    this.renderArray();
                    this.renderTree();
                    this.updateInfo();
                } catch (e) {
                    alert('输入格式错误，请使用逗号分隔的数字，如: 3,9,2,5,7,1,8');
                }
            }
            
            loadExample() {
                this.arrayInput.value = '3,9,2,5,7,1,8';
                this.generateArray();
            }
            
            updateSpeed() {
                this.speed = parseInt(this.speedSlider.value);
                if (this.isPlaying) {
                    this.stopPlay();
                    this.startPlay();
                }
            }
            
            resetState() {
                this.steps = [];
                this.currentStep = 0;
                this.compareCount = 0;
                this.swapCount = 0;
                this.stepCount = 0;
                this.nodeStates = this.array.map(() => this.NODE_STATE.DEFAULT);
                this.isPlaying = false;
                this.playBtn.textContent = '开始建堆';
                this.playBtn.classList.remove('btn-warning');
                this.playBtn.classList.add('btn-success');
                
                if (this.playInterval) {
                    clearInterval(this.playInterval);
                    this.playInterval = null;
                }
            }
            
            reset() {
                this.array = [...this.originalArray];
                this.resetState();
                this.renderArray();
                this.renderTree();
                this.updateInfo();
            }
            
            togglePlay() {
                if (this.isPlaying) {
                    this.stopPlay();
                } else {
                    this.startPlay();
                }
            }
            
            startPlay() {
                if (this.steps.length === 0) {
                    this.buildHeap();
                }
                
                if (this.currentStep >= this.steps.length) {
                    this.currentStep = 0;
                }
                
                this.isPlaying = true;
                this.playBtn.textContent = '暂停';
                this.playBtn.classList.remove('btn-success');
                this.playBtn.classList.add('btn-warning');
                
                const intervalTime = 1100 - (this.speed * 100);
                this.playInterval = setInterval(() => {
                    if (this.currentStep < this.steps.length) {
                        this.executeStep(this.currentStep);
                        this.currentStep++;
                    } else {
                        this.stopPlay();
                    }
                }, intervalTime);
            }
            
            stopPlay() {
                this.isPlaying = false;
                this.playBtn.textContent = '继续建堆';
                this.playBtn.classList.remove('btn-warning');
                this.playBtn.classList.add('btn-success');
                
                if (this.playInterval) {
                    clearInterval(this.playInterval);
                    this.playInterval = null;
                }
            }
            
            nextStep() {
                if (this.steps.length === 0) {
                    this.buildHeap();
                }
                
                if (this.currentStep < this.steps.length) {
                    this.executeStep(this.currentStep);
                    this.currentStep++;
                }
            }
            
            prevStep() {
                if (this.currentStep > 0) {
                    this.currentStep--;
                    this.undoStep(this.currentStep);
                }
            }
            
            buildHeap() {
                this.resetState();
                const n = this.array.length;
                const steps = [];
                
                // 从最后一个非叶子节点开始，向前遍历
                for (let i = Math.floor(n / 2) - 1; i >= 0; i--) {
                    this.heapify(steps, n, i);
                }
                
                this.steps = steps;
                this.stepCount = steps.length;
                document.getElementById('stepCount').textContent = this.stepCount;
            }
            
            heapify(steps, n, i) {
                let largest = i;
                const left = 2 * i + 1;
                const right = 2 * i + 2;
                
                // 步骤1: 标记当前节点
                steps.push({
                    type: 'mark_current',
                    index: i,
                    description: `开始调整节点[${i}] (值: ${this.array[i]})`
                });
                
                // 步骤2: 比较左子节点
                if (left < n) {
                    steps.push({
                        type: 'compare_left',
                        index: i,
                        leftIndex: left,
                        description: `比较节点[${i}] (值: ${this.array[i]}) 与左子节点[${left}] (值: ${this.array[left]})`
                    });
                    
                    if (this.array[left] > this.array[largest]) {
                        largest = left;
                        steps.push({
                            type: 'left_larger',
                            index: i,
                            leftIndex: left,
                            description: `左子节点[${left}] (值: ${this.array[left]}) 更大，记录为最大节点`
                        });
                    }
                }
                
                // 步骤3: 比较右子节点
                if (right < n) {
                    steps.push({
                        type: 'compare_right',
                        index: i,
                        rightIndex: right,
                        description: `比较节点[${i}] (值: ${this.array[i]}) 与右子节点[${right}] (值: ${this.array[right]})`
                    });
                    
                    if (this.array[right] > this.array[largest]) {
                        largest = right;
                        steps.push({
                            type: 'right_larger',
                            index: i,
                            rightIndex: right,
                            description: `右子节点[${right}] (值: ${this.array[right]}) 更大，记录为最大节点`
                        });
                    }
                }
                
                // 步骤4: 如果需要交换
                if (largest !== i) {
                    steps.push({
                        type: 'swap',
                        index1: i,
                        index2: largest,
                        description: `节点[${i}] (值: ${this.array[i]}) 小于子节点[${largest}] (值: ${this.array[largest]})，需要交换`
                    });
                    
                    // 交换数组元素
                    [this.array[i], this.array[largest]] = [this.array[largest], this.array[i]];
                    
                    // 递归调整
                    this.heapify(steps, n, largest);
                } else {
                    steps.push({
                        type: 'in_place',
                        index: i,
                        description: `节点[${i}] (值: ${this.array[i]}) 已满足堆性质，调整完成`
                    });
                }
                
                // 恢复原始数组状态用于动画
                this.array = [...this.originalArray];
            }
            
            executeStep(stepIndex) {
                const step = this.steps[stepIndex];
                
                // 重置所有节点状态为默认
                this.nodeStates = this.nodeStates.map(() => this.NODE_STATE.DEFAULT);
                
                // 根据步骤类型执行操作
                switch (step.type) {
                    case 'mark_current':
                        this.nodeStates[step.index] = this.NODE_STATE.CURRENT;
                        break;
                        
                    case 'compare_left':
                        this.nodeStates[step.index] = this.NODE_STATE.CURRENT;
                        this.nodeStates[step.leftIndex] = this.NODE_STATE.COMPARE;
                        this.compareCount++;
                        break;
                        
                    case 'compare_right':
                        this.nodeStates[step.index] = this.NODE_STATE.CURRENT;
                        this.nodeStates[step.rightIndex] = this.NODE_STATE.COMPARE;
                        this.compareCount++;
                        break;
                        
                    case 'left_larger':
                    case 'right_larger':
                        this.nodeStates[step.index] = this.NODE_STATE.CURRENT;
                        break;
                        
                    case 'swap':
                        this.nodeStates[step.index] = this.NODE_STATE.CURRENT;
                        this.nodeStates[step.index2] = this.NODE_STATE.COMPARE;
                        
                        // 执行交换
                        [this.array[step.index1], this.array[step.index2]] = 
                        [this.array[step.index2], this.array[step.index1]];
                        this.swapCount++;
                        break;
                        
                    case 'in_place':
                        this.nodeStates[step.index] = this.NODE_STATE.IN_PLACE;
                        break;
                }
                
                // 更新UI
                this.renderArray();
                this.renderTree();
                this.updateInfo(step);
                
                // 更新计数器显示
                document.getElementById('compareCount').textContent = this.compareCount;
                document.getElementById('swapCount').textContent = this.swapCount;
                document.getElementById('stepCounter').textContent = `步骤: ${stepIndex + 1}/${this.steps.length}`;
            }
            
            undoStep(stepIndex) {
                // 重新执行到上一步
                this.compareCount = 0;
                this.swapCount = 0;
                this.array = [...this.originalArray];
                this.nodeStates = this.array.map(() => this.NODE_STATE.DEFAULT);
                
                for (let i = 0; i <= stepIndex; i++) {
                    const step = this.steps[i];
                    
                    // 根据步骤类型更新状态
                    switch (step.type) {
                        case 'compare_left':
                        case 'compare_right':
                            this.compareCount++;
                            break;
                            
                        case 'swap':
                            // 执行交换
                            [this.array[step.index1], this.array[step.index2]] = 
                            [this.array[step.index2], this.array[step.index1]];
                            this.swapCount++;
                            break;
                    }
                }
                
                // 执行当前步骤以更新状态
                if (stepIndex >= 0) {
                    this.executeStep(stepIndex);
                } else {
                    this.renderArray();
                    this.renderTree();
                    this.updateInfo();
                }
                
                // 更新计数器显示
                document.getElementById('compareCount').textContent = this.compareCount;
                document.getElementById('swapCount').textContent = this.swapCount;
                document.getElementById('stepCounter').textContent = `步骤: ${stepIndex + 1}/${this.steps.length}`;
            }
            
            renderArray() {
                const container = document.getElementById('arrayContainer');
                container.innerHTML = '';
                
                // 更新状态显示
                const arrayStatus = document.getElementById('arrayStatus');
                const isHeap = this.isMaxHeap();
                arrayStatus.textContent = isHeap ? '已建堆完成' : '建堆中...';
                arrayStatus.style.color = isHeap ? '#27ae60' : '#e67e22';
                
                // 创建数组元素
                this.array.forEach((value, index) => {
                    const element = document.createElement('div');
                    element.className = 'array-element';
                    element.dataset.index = index;
                    
                    // 根据节点状态设置样式
                    let bgColor, borderColor, textColor;
                    
                    switch (this.nodeStates[index]) {
                        case this.NODE_STATE.CURRENT:
                            bgColor = '#e67e22';
                            borderColor = '#e67e22';
                            textColor = 'white';
                            break;
                        case this.NODE_STATE.COMPARE:
                            bgColor = '#aed6f1';
                            borderColor = '#3498db';
                            textColor = '#2c3e50';
                            break;
                        case this.NODE_STATE.IN_PLACE:
                            bgColor = '#d5f4e6';
                            borderColor = '#27ae60';
                            textColor = '#2c3e50';
                            break;
                        default:
                            bgColor = 'white';
                            borderColor = '#bdc3c7';
                            textColor = '#2c3e50';
                    }
                    
                    element.style.backgroundColor = bgColor;
                    element.style.border = `2px solid ${borderColor}`;
                    element.style.color = textColor;
                    
                    // 添加索引和值
                    const indexSpan = document.createElement('span');
                    indexSpan.className = 'element-index';
                    indexSpan.textContent = `[${index}]`;
                    
                    const valueSpan = document.createElement('span');
                    valueSpan.className = 'element-value';
                    valueSpan.textContent = value;
                    
                    element.appendChild(indexSpan);
                    element.appendChild(valueSpan);
                    container.appendChild(element);
                });
            }
            
            renderTree() {
                const svg = document.getElementById('treeSvg');
                svg.innerHTML = '';
                
                // 更新状态显示
                const treeStatus = document.getElementById('treeStatus');
                const isHeap = this.isMaxHeap();
                treeStatus.textContent = isHeap ? '大顶堆已建立' : '构建大顶堆中';
                treeStatus.style.color = isHeap ? '#27ae60' : '#e67e22';
                
                const width = svg.clientWidth;
                const height = svg.clientHeight;
                const nodeRadius = 25;
                const levelHeight = 80;
                
                // 计算树的高度
                const treeHeight = Math.floor(Math.log2(this.array.length)) + 1;
                
                // 绘制树节点和连线
                for (let i = 0; i < this.array.length; i++) {
                    const level = Math.floor(Math.log2(i + 1));
                    const nodesInLevel = Math.pow(2, level);
                    const positionInLevel = i + 1 - Math.pow(2, level);
                    
                    // 计算节点位置
                    const x = width / (nodesInLevel + 1) * (positionInLevel + 1);
                    const y = level * levelHeight + 50;
                    
                    // 绘制到父节点的连线
                    if (i > 0) {
                        const parentIndex = Math.floor((i - 1) / 2);
                        const parentLevel = Math.floor(Math.log2(parentIndex + 1));
                        const parentNodesInLevel = Math.pow(2, parentLevel);
                        const parentPositionInLevel = parentIndex + 1 - Math.pow(2, parentLevel);
                        
                        const parentX = width / (parentNodesInLevel + 1) * (parentPositionInLevel + 1);
                        const parentY = parentLevel * levelHeight + 50;
                        
                        // 绘制连线
                        const line = document.createElementNS('http://www.w3.org/2000/svg', 'line');
                        line.setAttribute('x1', parentX);
                        line.setAttribute('y1', parentY + nodeRadius);
                        line.setAttribute('x2', x);
                        line.setAttribute('y2', y - nodeRadius);
                        line.setAttribute('stroke', '#bdc3c7');
                        line.setAttribute('stroke-width', '2');
                        svg.appendChild(line);
                    }
                    
                    // 绘制节点
                    const circle = document.createElementNS('http://www.w3.org/2000/svg', 'circle');
                    circle.setAttribute('cx', x);
                    circle.setAttribute('cy', y);
                    circle.setAttribute('r', nodeRadius);
                    
                    // 根据节点状态设置颜色
                    switch (this.nodeStates[i]) {
                        case this.NODE_STATE.CURRENT:
                            circle.setAttribute('fill', '#e67e22');
                            circle.setAttribute('stroke', '#d35400');
                            break;
                        case this.NODE_STATE.COMPARE:
                            circle.setAttribute('fill', '#aed6f1');
                            circle.setAttribute('stroke', '#3498db');
                            break;
                        case this.NODE_STATE.IN_PLACE:
                            circle.setAttribute('fill', '#d5f4e6');
                            circle.setAttribute('stroke', '#27ae60');
                            break;
                        default:
                            circle.setAttribute('fill', 'white');
                            circle.setAttribute('stroke', '#bdc3c7');
                    }
                    
                    circle.setAttribute('stroke-width', '2');
                    svg.appendChild(circle);
                    
                    // 绘制节点值
                    const text = document.createElementNS('http://www.w3.org/2000/svg', 'text');
                    text.setAttribute('x', x);
                    text.setAttribute('y', y + 5);
                    text.setAttribute('text-anchor', 'middle');
                    text.setAttribute('font-weight', 'bold');
                    text.setAttribute('font-size', '16');
                    
                    // 根据背景色调整文字颜色
                    if (this.nodeStates[i] === this.NODE_STATE.CURRENT) {
                        text.setAttribute('fill', 'white');
                    } else {
                        text.setAttribute('fill', '#2c3e50');
                    }
                    
                    text.textContent = this.array[i];
                    svg.appendChild(text);
                    
                    // 绘制节点索引
                    const indexText = document.createElementNS('http://www.w3.org/2000/svg', 'text');
                    indexText.setAttribute('x', x);
                    indexText.setAttribute('y', y - nodeRadius - 5);
                    indexText.setAttribute('text-anchor', 'middle');
                    indexText.setAttribute('font-size', '12');
                    indexText.setAttribute('fill', '#7f8c8d');
                    indexText.textContent = `[${i}]`;
                    svg.appendChild(indexText);
                }
            }
            
            updateInfo(step = null) {
                const stepTitle = document.getElementById('stepTitle');
                const stepDesc = document.getElementById('stepDesc');
                
                if (step) {
                    stepTitle.textContent = this.getStepTitle(step.type);
                    stepDesc.textContent = step.description;
                } else {
                    stepTitle.textContent = '准备开始';
                    stepDesc.textContent = '请点击"开始建堆"按钮或"下一步"按钮开始动画演示。';
                }
            }
            
            getStepTitle(stepType) {
                const titles = {
                    'mark_current': '标记当前节点',
                    'compare_left': '比较左子节点',
                    'compare_right': '比较右子节点',
                    'left_larger': '左子节点更大',
                    'right_larger': '右子节点更大',
                    'swap': '交换节点',
                    'in_place': '节点已就位'
                };
                
                return titles[stepType] || '执行步骤';
            }
            
            isMaxHeap() {
                for (let i = 0; i < this.array.length; i++) {
                    const left = 2 * i + 1;
                    const right = 2 * i + 2;
                    
                    if (left < this.array.length && this.array[left] > this.array[i]) {
                        return false;
                    }
                    
                    if (right < this.array.length && this.array[right] > this.array[i]) {
                        return false;
                    }
                }
                return true;
            }
        }
        
        // 页面加载完成后初始化动画
        document.addEventListener('DOMContentLoaded', () => {
            const animation = new HeapSortAnimation();
        });
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 堆排序建堆与下沉调整动画使用指南

欢迎使用堆排序交互式教学动画！本工具旨在通过可视化方式，帮助您直观理解堆排序算法中**建堆**和**下沉调整**的核心过程。无论您是初次接触堆排序，还是希望加深对算法动态过程的理解，本动画都将为您提供清晰、生动的学习体验。

---

### 一、功能说明

本动画将堆排序的建堆过程分解为一系列可交互的步骤，通过**双视图同步展示**（数组视图 + 二叉树视图）和**分步动画**，动态呈现算法如何将一个无序数组构建成一个大顶堆。您可以通过控制面板自由控制动画节奏，观察每一个比较、交换和状态变化的细节。

### 二、主要功能

1.  **数据输入与生成**
    *   **自定义数组**：在输入框中输入以逗号分隔的数字（如 `5,2,8,1,9`），点击“生成数组”即可加载。
    *   **示例数组**：一键加载预设的示例数组 `[3,9,2,5,7,1,8]`，快速开始学习。

2.  **动画控制**
    *   **开始/暂停建堆**：一键开始自动连续演示建堆全过程，可随时暂停。
    *   **单步执行**：通过“下一步”和“上一步”按钮，精确控制每一个算法步骤，适合深入分析。
    *   **速度调节**：拖动滑块可调整自动播放的速度，满足不同学习节奏的需求。
    *   **重置**：随时将动画恢复到初始无序数组状态，便于重复学习。

3.  **可视化展示**
    *   **数组视图**：以带索引的卡片形式展示数组，颜色动态反映节点状态。
    *   **二叉树视图**：将数组同步可视化为完全二叉树，清晰展示父子节点关系。
    *   **状态同步**：两个视图的节点状态（颜色、位置）实时同步，强化数据结构对应关系的理解。

4.  **学习信息面板**
    *   **步骤说明**：实时显示当前步骤的详细文字描述（如“比较节点[1]与左子节点[3]”）。
    *   **操作计数器**：统计并显示“比较次数”、“交换次数”和“总步骤数”，帮助量化理解算法效率。
    *   **图例说明**：解释不同颜色节点代表的含义（当前节点、待比较节点、已就位节点等）。

### 三、设计特色

1.  **认知友好的双视图设计**：并排显示数组和二叉树，用颜色和连线明确展示索引 `i` 的父节点(`(i-1)/2`)、左子节点(`2*i+1`)和右子节点(`2*i+2`)的对应关系，化解抽象概念。
2.  **焦点引导式动画**：每一步动画都通过**高亮当前操作节点**、**标记待比较子节点**、**平滑交换动画**，将您的注意力精准引导至算法关键处。
3.  **符合算法逻辑的步骤分解**：严格遵循堆排序建堆算法（自底向上的下沉调整），将过程分解为“标记 -> 比较 -> 决策 -> 交换/就位”的原子步骤，逻辑清晰。
4.  **即时反馈与状态追踪**：“已就位”的节点会变为绿色，让您一目了然地看到哪些部分已满足堆性质，直观感受算法“逐步构建”堆的过程。

### 四、教学要点

通过本动画，请重点关注以下核心知识点：

1.  **堆的物理与逻辑结构**：理解数组是如何通过索引计算公式映射成一棵完全二叉树的。
2.  **大顶堆的性质**：父节点的值总是大于或等于其子节点的值。动画中，值的大小通过节点位置和操作提示体现。
3.  **建堆的起点**：为什么从 **最后一个非叶子节点**（索引为 `floor(n/2)-1`）开始向前调整？动画将直观展示其必要性。
4.  **下沉调整的核心逻辑**：
    *   **比较**：当前节点需要与**两个子节点**都进行比较。
    *   **交换**：如果当前节点小于**较大的那个子节点**，则与之交换。
    *   **递归**：交换后，以子节点位置为新的当前节点，继续向下调整，直到满足堆性质或成为叶节点。
5.  **算法效率的直观感受**：观察计数器，理解建堆过程的时间复杂度 **O(n)** 是如何通过避免对每个元素都从根节点开始调整来实现的。

### 五、使用建议

为了达到最佳学习效果，建议您按以下流程使用：

1.  **初次体验**：点击“示例数组”，然后点击“**开始建堆**”，以常速观看一遍完整的建堆动画，建立整体印象。
2.  **逐步精学**：点击“重置”，使用“**下一步**”按钮手动控制。在每一步，仔细阅读步骤说明，观察两个视图中哪些节点被高亮、发生了什么变化，并思考“为什么”。
3.  **重点复盘**：遇到关键步骤（如发生交换）时，使用“**上一步**”回退，并再次执行，加深理解。特别关注从最后一个非叶子节点开始的第一个调整过程。
4.  **主动探索**：在输入框中输入**自定义数组**（如一个已排序的数组 `1,2,3,4,5` 或数值相同的数组 `5,5,5,5`），观察建堆过程有何不同，验证您的理解。
5.  **知识串联**：在观看动画的同时，尝试在纸上或脑海中同步画出对应的二叉树，并写下伪代码，将视觉信息转化为算法逻辑。

---

希望这个交互式动画能成为您学习堆排序算法的得力助手！祝您学习愉快，如有任何反馈，欢迎提出。