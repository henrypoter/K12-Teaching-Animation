# 需求：插入排序（抓牌整理）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为计算机科学或数据结构的初学者，可能包括高中生、大学生或自学者。他们具备基础的编程概念，但对算法细节和动态过程理解不深。
2.  **核心需求**：
    *   **直观理解过程**：用户需要清晰地看到插入排序如何像整理扑克牌一样，将未排序的元素逐个“插入”到已排序部分的正确位置。
    *   **掌握关键步骤**：理解“比较”、“移动（腾出空间）”、“插入”这三个核心操作。
    *   **观察数据变化**：实时观察数组（或列表）中元素位置和值的变化，以及“当前待插入元素”、“已排序区域”、“未排序区域”等状态的划分。
    *   **控制学习节奏**：能够暂停、单步执行、重置，以便在关键步骤进行思考和消化。
    *   **获得即时反馈**：在操作或观察过程中，通过视觉提示（如高亮、箭头、文字说明）了解当前正在进行的操作及其结果。

#### 教学设计思路
1.  **核心概念**：
    *   **核心比喻**：使用“抓牌整理”作为核心比喻。将算法过程类比为打扑克牌时，将新抓到的牌插入手中已排序牌堆的正确位置。
    *   **关键操作**：分解为 **“选取”** (Pick)、**“比较与移动”** (Compare & Shift)、**“插入”** (Insert) 三个原子操作。
    *   **区域划分**：明确区分“已排序区域”（通常用不同颜色或边框表示）和“未排序区域”。
2.  **认知规律**：
    *   **从具体到抽象**：先通过生动的“抓牌”动画建立直观印象，再逐步关联到抽象的数组索引和值操作。
    *   **分步演示**：将完整的排序过程分解为多个“插入”循环，每个循环再分解为上述三个原子操作，逐步推进。
    *   **强调不变性**：在每一步中，都突出显示“已排序区域始终是有序的”这一循环不变式。
3.  **交互设计**：
    *   **流程控制**：提供“播放/暂停”、“下一步”、“上一步”、“重置”按钮，让用户完全掌控动画进度。
    *   **直接操作**：在“分步模式”下，用户可以点击“待插入元素”，手动将其与已排序部分的元素进行比较，增强参与感。
    *   **变量与状态可视化**：在动画旁同步显示当前循环的 `i` (待插入元素索引)、`key` (待插入元素的值)、`j` (比较位置索引) 等关键变量，并高亮显示代码中对应的行。
4.  **视觉呈现**：
    *   **主场景**：一个水平排列的数组可视化区域，每个元素用一个矩形（“牌”）表示，矩形内显示数字（“牌面”）。
    *   **视觉编码**：
        *   **颜色**：已排序区域用温和的绿色系，未排序区域用中性灰色，当前待插入元素用醒目的黄色（或橙色），正在比较的元素用蓝色，移动路径用箭头或半透明轨迹表示。
        *   **空间分离**：用背景色块或分隔线明确划分“已排序区”和“未排序区”。
        *   **动态效果**：使用平滑的位移动画模拟“移动”操作，使用缩放或脉动效果强调“选取”和“插入”时刻。
    *   **多视图联动**：将“扑克牌比喻视图”、“数组操作视图”和“伪代码高亮视图”并列或关联显示，帮助用户建立多角度理解。

#### 配色方案选择
选择对比清晰、符合认知习惯且舒适的配色方案：
*   **背景与框架**：浅灰色 (`#f5f5f5`) 或白色背景，深灰色 (`#333`) 文字。
*   **已排序区域**：柔和的渐变色绿色，如从 `#d4edda` (浅绿) 到 `#c3e6cb` (稍深绿)，表示“已完成、有序、稳定”。
*   **未排序区域**：浅灰色 (`#e9ecef`)，表示“待处理”。
*   **当前待插入元素 (`key`)**：醒目的暖色，如橙色 (`#fd7e14`)，吸引全部注意力。
*   **正在比较的元素**：蓝色 (`#007bff`)，与黄色形成清晰对比，表示“正在活动”。
*   **移动轨迹/箭头**：半透明的蓝色 (`rgba(0, 123, 255, 0.3)`) 或灰色。
*   **代码高亮**：当前执行行用浅黄色背景 (`#fff3cd`) 高亮。
*   **按钮与交互元素**：采用 Bootstrap 风格的蓝色 (`#007bff`) 表示主要操作，绿色 (`#28a745`) 表示播放，灰色 (`#6c757d`) 表示重置。

#### 交互功能列表
1.  **核心控制面板**：
    *   `播放 / 暂停`：开始或暂停连续动画。
    *   `下一步`：手动前进到下一个关键步骤（如：开始新循环、进行一次比较、完成一次插入）。
    *   `上一步`：回退到上一个关键步骤，便于回顾。
    *   `重置`：将数据恢复为初始的随机乱序状态，并回到第一步。
2.  **动画速度调节**：一个滑动条，允许用户调整连续播放时的速度（慢速-常速-快速）。
3.  **数据控制**：
    *   `随机生成`：生成一组新的随机数。
    *   `自定义输入`：允许用户输入一组自定义数字（如用逗号分隔）进行排序。
    *   `数据规模`：选择数组大小（例如 5, 8, 10个元素），以适应不同复杂度。
4.  **视图切换/显示**：
    *   `显示/隐藏代码`：切换伪代码区域的显示。
    *   `显示/隐藏变量值`：切换显示当前 `i`, `key`, `j` 等变量值的面板。
    *   `高亮区域`：始终用背景色高亮显示“已排序区”和“未排序区”。
5.  **分步学习模式（可选增强）**：
    *   在“下一步”模式下，提示用户“点击待插入元素，将其与左侧已排序元素进行比较”，增加互动性。
    *   在每个步骤提供简短的文字说明，如：“现在，我们将数字 7 插入到已排序部分 [3, 5, 8] 中。”
6.  **完成状态反馈**：当所有元素排序完成后，整个数组元素变为统一的“完成色”（如深绿色 `#155724`），并显示“排序完成！”的提示信息。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>插入排序（抓牌整理）教学动画</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 15px;
            border-bottom: 2px solid #007bff;
        }
        
        h1 {
            color: #007bff;
            margin-bottom: 10px;
        }
        
        .subtitle {
            color: #6c757d;
            font-size: 1.1rem;
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
        
        .visualization-section {
            flex: 1;
            min-width: 300px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
        }
        
        .code-section {
            flex: 1;
            min-width: 300px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
        }
        
        .section-title {
            color: #495057;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #e9ecef;
            font-size: 1.3rem;
        }
        
        #animation-container {
            width: 100%;
            height: 300px;
            position: relative;
            margin-bottom: 20px;
            border: 1px solid #dee2e6;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .array-element {
            position: absolute;
            width: 60px;
            height: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 8px;
            font-weight: bold;
            font-size: 1.5rem;
            transition: all 0.5s ease;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
            border: 2px solid transparent;
        }
        
        .sorted-region {
            position: absolute;
            height: 90px;
            background-color: rgba(195, 230, 203, 0.3);
            border-radius: 8px;
            border: 2px dashed #c3e6cb;
            transition: all 0.5s ease;
        }
        
        .unsorted-region {
            position: absolute;
            height: 90px;
            background-color: rgba(233, 236, 239, 0.3);
            border-radius: 8px;
            border: 2px dashed #e9ecef;
            transition: all 0.5s ease;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #e9ecef;
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
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }
        
        button {
            padding: 10px 16px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        
        .btn-play {
            background-color: #28a745;
            color: white;
        }
        
        .btn-play:hover {
            background-color: #218838;
        }
        
        .btn-pause {
            background-color: #ffc107;
            color: #333;
        }
        
        .btn-pause:hover {
            background-color: #e0a800;
        }
        
        .btn-next, .btn-prev {
            background-color: #007bff;
            color: white;
        }
        
        .btn-next:hover, .btn-prev:hover {
            background-color: #0069d9;
        }
        
        .btn-reset {
            background-color: #6c757d;
            color: white;
        }
        
        .btn-reset:hover {
            background-color: #5a6268;
        }
        
        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-left: auto;
        }
        
        #speedSlider {
            width: 120px;
        }
        
        .code-container {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 0.95rem;
            line-height: 1.5;
            overflow-x: auto;
            margin-bottom: 20px;
            border: 1px solid #e9ecef;
        }
        
        .code-line {
            padding: 2px 5px;
            margin: 2px 0;
            border-radius: 3px;
            transition: background-color 0.3s;
        }
        
        .highlight {
            background-color: #fff3cd;
        }
        
        .variables-panel {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            margin-top: 20px;
            border: 1px solid #e9ecef;
        }
        
        .variables-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 15px;
        }
        
        .variable-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 10px;
            background-color: white;
            border-radius: 6px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
        }
        
        .variable-name {
            font-weight: bold;
            color: #007bff;
            margin-bottom: 5px;
        }
        
        .variable-value {
            font-size: 1.2rem;
            font-weight: bold;
            color: #333;
            min-height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .status-panel {
            background-color: #e7f3ff;
            border-radius: 8px;
            padding: 15px;
            margin-top: 20px;
            border-left: 4px solid #007bff;
        }
        
        .status-title {
            font-weight: bold;
            color: #007bff;
            margin-bottom: 8px;
        }
        
        .status-text {
            color: #333;
        }
        
        .explanation {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            margin-top: 20px;
        }
        
        .explanation h3 {
            color: #495057;
            margin-bottom: 15px;
        }
        
        .explanation p {
            margin-bottom: 10px;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .controls {
                justify-content: center;
            }
            
            .speed-control {
                margin-left: 0;
                margin-top: 10px;
                width: 100%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>插入排序（抓牌整理）教学动画</h1>
        <p class="subtitle">像整理扑克牌一样理解插入排序算法</p>
    </header>
    
    <div class="container">
        <div class="main-content">
            <section class="visualization-section">
                <h2 class="section-title">排序过程可视化</h2>
                <div id="animation-container">
                    <!-- 数组元素将通过JS动态生成 -->
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #fd7e14;"></div>
                        <span>当前待插入元素 (key)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #007bff;"></div>
                        <span>正在比较的元素</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #c3e6cb;"></div>
                        <span>已排序区域</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e9ecef;"></div>
                        <span>未排序区域</span>
                    </div>
                </div>
                
                <div class="controls">
                    <button id="playBtn" class="btn-play">
                        <span>▶ 播放</span>
                    </button>
                    <button id="pauseBtn" class="btn-pause">
                        <span>⏸ 暂停</span>
                    </button>
                    <button id="prevBtn" class="btn-prev">
                        <span>◀ 上一步</span>
                    </button>
                    <button id="nextBtn" class="btn-next">
                        <span>▶ 下一步</span>
                    </button>
                    <button id="resetBtn" class="btn-reset">
                        <span>↺ 重置</span>
                    </button>
                    
                    <div class="speed-control">
                        <span>速度:</span>
                        <input type="range" id="speedSlider" min="1" max="10" value="5">
                        <span id="speedValue">中速</span>
                    </div>
                </div>
                
                <div class="status-panel">
                    <div class="status-title">当前状态</div>
                    <div id="statusText" class="status-text">点击"播放"开始排序动画</div>
                </div>
            </section>
            
            <section class="code-section">
                <h2 class="section-title">算法代码</h2>
                <div class="code-container">
                    <div id="codeLine1" class="code-line">for (i = 1; i < n; i++) {</div>
                    <div id="codeLine2" class="code-line">  key = arr[i];</div>
                    <div id="codeLine3" class="code-line">  j = i - 1;</div>
                    <div id="codeLine4" class="code-line">  </div>
                    <div id="codeLine5" class="code-line">  while (j >= 0 && arr[j] > key) {</div>
                    <div id="codeLine6" class="code-line">    arr[j + 1] = arr[j];</div>
                    <div id="codeLine7" class="code-line">    j = j - 1;</div>
                    <div id="codeLine8" class="code-line">  }</div>
                    <div id="codeLine9" class="code-line">  </div>
                    <div id="codeLine10" class="code-line">  arr[j + 1] = key;</div>
                    <div id="codeLine11" class="code-line">}</div>
                </div>
                
                <div class="variables-panel">
                    <h3 class="section-title">当前变量值</h3>
                    <div class="variables-grid">
                        <div class="variable-item">
                            <div class="variable-name">i (当前索引)</div>
                            <div id="varI" class="variable-value">-</div>
                        </div>
                        <div class="variable-item">
                            <div class="variable-name">key (待插入值)</div>
                            <div id="varKey" class="variable-value">-</div>
                        </div>
                        <div class="variable-item">
                            <div class="variable-name">j (比较索引)</div>
                            <div id="varJ" class="variable-value">-</div>
                        </div>
                        <div class="variable-item">
                            <div class="variable-name">循环次数</div>
                            <div id="varLoop" class="variable-value">0</div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
        
        <section class="explanation">
            <h3>插入排序算法解析</h3>
            <p><strong>核心思想：</strong>插入排序的工作方式像整理手中的扑克牌。每次从未排序部分取出一张牌（元素），将其插入到已排序部分的正确位置。</p>
            <p><strong>算法步骤：</strong></p>
            <ol>
                <li>从第二个元素开始（索引 i=1），将其作为待插入元素（key）。</li>
                <li>将 key 与已排序部分的元素从右向左依次比较。</li>
                <li>如果已排序部分的元素大于 key，则将该元素向右移动一位，为 key 腾出空间。</li>
                <li>重复步骤3，直到找到 key 的正确插入位置。</li>
                <li>将 key 插入到正确位置。</li>
                <li>对未排序部分的所有元素重复上述过程。</li>
            </ol>
            <p><strong>时间复杂度：</strong>最坏情况 O(n²)，最好情况 O(n)（当数组已排序时）。</p>
            <p><strong>空间复杂度：</strong>O(1)（原地排序）。</p>
        </section>
    </div>

    <script>
        // 插入排序算法状态机
        class InsertionSortAnimation {
            constructor() {
                // 初始数据
                this.originalArray = [5, 2, 9, 1, 7, 4, 8, 3, 6];
                this.array = [...this.originalArray];
                this.n = this.array.length;
                
                // 算法状态变量
                this.i = 1;      // 外层循环索引
                this.j = 0;      // 内层循环索引
                this.key = 0;    // 当前待插入值
                this.loopCount = 0; // 循环计数
                
                // 动画状态
                this.isPlaying = false;
                this.speed = 5;  // 1-10，值越大速度越快
                this.animationInterval = null;
                this.currentStep = 0; // 当前步骤
                this.stepHistory = []; // 步骤历史，用于回退
                
                // 算法阶段
                this.phase = 'init'; // init, pick, compare, shift, insert, done
                this.comparing = false;
                this.shifting = false;
                
                // DOM 元素引用
                this.animationContainer = document.getElementById('animation-container');
                this.statusText = document.getElementById('statusText');
                this.varI = document.getElementById('varI');
                this.varKey = document.getElementById('varKey');
                this.varJ = document.getElementById('varJ');
                this.varLoop = document.getElementById('varLoop');
                this.speedSlider = document.getElementById('speedSlider');
                this.speedValue = document.getElementById('speedValue');
                
                // 代码高亮元素
                this.codeLines = [];
                for (let i = 1; i <= 11; i++) {
                    this.codeLines.push(document.getElementById(`codeLine${i}`));
                }
                
                // 初始化
                this.init();
                this.renderArray();
                this.updateVariables();
                this.updateStatus();
                this.setupEventListeners();
            }
            
            init() {
                // 重置状态
                this.array = [...this.originalArray];
                this.i = 1;
                this.j = 0;
                this.key = 0;
                this.loopCount = 0;
                this.phase = 'init';
                this.comparing = false;
                this.shifting = false;
                this.currentStep = 0;
                this.stepHistory = [];
                
                // 清除高亮
                this.clearCodeHighlight();
                
                // 保存初始状态
                this.saveStep();
            }
            
            saveStep() {
                this.stepHistory.push({
                    array: [...this.array],
                    i: this.i,
                    j: this.j,
                    key: this.key,
                    loopCount: this.loopCount,
                    phase: this.phase,
                    comparing: this.comparing,
                    shifting: this.shifting
                });
            }
            
            restorePreviousStep() {
                if (this.stepHistory.length > 1) {
                    this.stepHistory.pop(); // 移除当前状态
                    const prevState = this.stepHistory[this.stepHistory.length - 1];
                    
                    this.array = [...prevState.array];
                    this.i = prevState.i;
                    this.j = prevState.j;
                    this.key = prevState.key;
                    this.loopCount = prevState.loopCount;
                    this.phase = prevState.phase;
                    this.comparing = prevState.comparing;
                    this.shifting = prevState.shifting;
                    
                    this.renderArray();
                    this.updateVariables();
                    this.updateStatus();
                    this.updateCodeHighlight();
                    
                    return true;
                }
                return false;
            }
            
            renderArray() {
                // 清空容器
                this.animationContainer.innerHTML = '';
                
                const containerWidth = this.animationContainer.clientWidth;
                const containerHeight = this.animationContainer.clientHeight;
                const elementWidth = 60;
                const elementHeight = 80;
                const spacing = 20;
                const totalWidth = this.n * elementWidth + (this.n - 1) * spacing;
                const startX = (containerWidth - totalWidth) / 2;
                const y = (containerHeight - elementHeight) / 2;
                
                // 绘制已排序区域
                if (this.i > 0) {
                    const sortedRegion = document.createElement('div');
                    sortedRegion.className = 'sorted-region';
                    sortedRegion.style.width = `${this.i * elementWidth + (this.i - 1) * spacing}px`;
                    sortedRegion.style.left = `${startX}px`;
                    sortedRegion.style.top = `${y - 5}px`;
                    this.animationContainer.appendChild(sortedRegion);
                }
                
                // 绘制未排序区域
                if (this.i < this.n) {
                    const unsortedRegion = document.createElement('div');
                    unsortedRegion.className = 'unsorted-region';
                    unsortedRegion.style.width = `${(this.n - this.i) * elementWidth + (this.n - this.i - 1) * spacing}px`;
                    unsortedRegion.style.left = `${startX + this.i * elementWidth + this.i * spacing}px`;
                    unsortedRegion.style.top = `${y - 5}px`;
                    this.animationContainer.appendChild(unsortedRegion);
                }
                
                // 绘制数组元素
                for (let index = 0; index < this.n; index++) {
                    const element = document.createElement('div');
                    element.className = 'array-element';
                    element.textContent = this.array[index];
                    element.style.left = `${startX + index * (elementWidth + spacing)}px`;
                    element.style.top = `${y}px`;
                    
                    // 设置元素颜色
                    if (index === this.i && this.phase !== 'done') {
                        // 当前待插入元素
                        element.style.backgroundColor = '#fd7e14';
                        element.style.color = 'white';
                        element.style.borderColor = '#e8590c';
                        element.style.zIndex = '10';
                    } else if (this.comparing && index === this.j) {
                        // 正在比较的元素
                        element.style.backgroundColor = '#007bff';
                        element.style.color = 'white';
                        element.style.borderColor = '#0056b3';
                        element.style.zIndex = '5';
                    } else if (index < this.i) {
                        // 已排序区域
                        element.style.backgroundColor = '#c3e6cb';
                        element.style.color = '#155724';
                        element.style.borderColor = '#b1dfbb';
                    } else {
                        // 未排序区域
                        element.style.backgroundColor = '#e9ecef';
                        element.style.color = '#495057';
                        element.style.borderColor = '#dee2e6';
                    }
                    
                    // 如果排序完成，所有元素变为完成色
                    if (this.phase === 'done') {
                        element.style.backgroundColor = '#155724';
                        element.style.color = 'white';
                        element.style.borderColor = '#0c4128';
                    }
                    
                    this.animationContainer.appendChild(element);
                }
            }
            
            updateVariables() {
                this.varI.textContent = this.i < this.n ? this.i : '完成';
                this.varKey.textContent = this.key > 0 ? this.key : '-';
                this.varJ.textContent = this.j >= 0 ? this.j : '-';
                this.varLoop.textContent = this.loopCount;
            }
            
            updateStatus() {
                let status = '';
                
                switch (this.phase) {
                    case 'init':
                        status = '准备开始排序。点击"播放"按钮开始动画。';
                        break;
                    case 'pick':
                        status = `选取第 ${this.i+1} 个元素 (值=${this.array[this.i]}) 作为待插入元素。`;
                        break;
                    case 'compare':
                        status = `比较待插入元素 (${this.key}) 与已排序元素 arr[${this.j}] = ${this.array[this.j]}。`;
                        if (this.j >= 0 && this.array[this.j] > this.key) {
                            status += ` 因为 ${this.array[this.j]} > ${this.key}，需要向右移动。`;
                        } else if (this.j >= 0) {
                            status += ` 因为 ${this.array[this.j]} ≤ ${this.key}，找到插入位置。`;
                        }
                        break;
                    case 'shift':
                        status = `将 arr[${this.j}] = ${this.array[this.j]} 向右移动一位。`;
                        break;
                    case 'insert':
                        status = `将待插入元素 (${this.key}) 插入到 arr[${this.j+1}] 的位置。`;
                        break;
                    case 'done':
                        status = '排序完成！所有元素已按升序排列。';
                        break;
                }
                
                this.statusText.textContent = status;
            }
            
            updateCodeHighlight() {
                // 清除所有高亮
                this.clearCodeHighlight();
                
                // 根据当前阶段高亮对应代码行
                switch (this.phase) {
                    case 'pick':
                        this.codeLines[0].classList.add('highlight'); // for循环
                        this.codeLines[1].classList.add('highlight'); // key = arr[i]
                        break;
                    case 'compare':
                        this.codeLines[2].classList.add('highlight'); // j = i-1
                        this.codeLines[4].classList.add('highlight'); // while循环条件
                        break;
                    case 'shift':
                        this.codeLines[5].classList.add('highlight'); // arr[j+1] = arr[j]
                        this.codeLines[6].classList.add('highlight'); // j = j-1
                        break;
                    case 'insert':
                        this.codeLines[9].classList.add('highlight'); // arr[j+1] = key
                        break;
                    case 'done':
                        this.codeLines[10].classList.add('highlight'); // 循环结束
                        break;
                }
            }
            
            clearCodeHighlight() {
                this.codeLines.forEach(line => line.classList.remove('highlight'));
            }
            
            nextStep() {
                // 保存当前步骤
                this.saveStep();
                
                // 执行算法下一步
                switch (this.phase) {
                    case 'init':
                        this.phase = 'pick';
                        this.key = this.array[this.i];
                        this.updateCodeHighlight();
                        break;
                        
                    case 'pick':
                        this.phase = 'compare';
                        this.j = this.i - 1;
                        this.comparing = true;
                        this.updateCodeHighlight();
                        break;
                        
                    case 'compare':
                        if (this.j >= 0 && this.array[this.j] > this.key) {
                            this.phase = 'shift';
                            this.shifting = true;
                        } else {
                            this.phase = 'insert';
                            this.comparing = false;
                        }
                        this.updateCodeHighlight();
                        break;
                        
                    case 'shift':
                        // 执行移动操作
                        this.array[this.j + 1] = this.array[this.j];
                        this.j = this.j - 1;
                        
                        // 渲染移动效果
                        this.renderArray();
                        
                        // 判断下一步
                        if (this.j >= 0 && this.array[this.j] > this.key) {
                            this.phase = 'compare';
                            this.shifting = false;
                            this.comparing = true;
                        } else {
                            this.phase = 'insert';
                            this.shifting = false;
                            this.comparing = false;
                        }
                        this.updateCodeHighlight();
                        break;
                        
                    case 'insert':
                        // 执行插入操作
                        this.array[this.j + 1] = this.key;
                        
                        // 准备下一轮循环
                        this.i++;
                        this.loopCount++;
                        
                        if (this.i < this.n) {
                            this.phase = 'pick';
                            this.key = this.array[this.i];
                        } else {
                            this.phase = 'done';
                        }
                        
                        this.comparing = false;
                        this.shifting = false;
                        this.updateCodeHighlight();
                        break;
                        
                    case 'done':
                        // 排序已完成，不再前进
                        return;
                }
                
                this.renderArray();
                this.updateVariables();
                this.updateStatus();
                this.currentStep++;
            }
            
            prevStep() {
                if (this.restorePreviousStep()) {
                    this.currentStep--;
                }
            }
            
            play() {
                if (this.phase === 'done') {
                    this.reset();
                }
                
                this.isPlaying = true;
                const speedMap = {
                    1: 1500, 2: 1200, 3: 1000, 4: 800, 5: 600,
                    6: 500, 7: 400, 8: 300, 9: 200, 10: 100
                };
                
                const intervalTime = speedMap[this.speed] || 600;
                
                if (this.animationInterval) {
                    clearInterval(this.animationInterval);
                }
                
                this.animationInterval = setInterval(() => {
                    if (this.phase === 'done') {
                        this.pause();
                        return;
                    }
                    
                    this.nextStep();
                }, intervalTime);
            }
            
            pause() {
                this.isPlaying = false;
                if (this.animationInterval) {
                    clearInterval(this.animationInterval);
                    this.animationInterval = null;
                }
            }
            
            reset() {
                this.pause();
                this.init();
                this.renderArray();
                this.updateVariables();
                this.updateStatus();
            }
            
            setSpeed(value) {
                this.speed = parseInt(value);
                const speedLabels = {
                    1: '极慢', 2: '很慢', 3: '慢速', 4: '较慢', 5: '中速',
                    6: '较快', 7: '快速', 8: '很快', 9: '极快', 10: '最快'
                };
                this.speedValue.textContent = speedLabels[this.speed] || '中速';
                
                // 如果正在播放，更新播放速度
                if (this.isPlaying) {
                    this.pause();
                    this.play();
                }
            }
            
            setupEventListeners() {
                document.getElementById('playBtn').addEventListener('click', () => {
                    this.play();
                });
                
                document.getElementById('pauseBtn').addEventListener('click', () => {
                    this.pause();
                });
                
                document.getElementById('nextBtn').addEventListener('click', () => {
                    this.pause();
                    this.nextStep();
                });
                
                document.getElementById('prevBtn').addEventListener('click', () => {
                    this.pause();
                    this.prevStep();
                });
                
                document.getElementById('resetBtn').addEventListener('click', () => {
                    this.reset();
                });
                
                this.speedSlider.addEventListener('input', (e) => {
                    this.setSpeed(e.target.value);
                });
                
                // 初始速度设置
                this.speedSlider.value = this.speed;
                this.setSpeed(this.speed);
                
                // 窗口大小变化时重新渲染
                window.addEventListener('resize', () => {
                    this.renderArray();
                });
            }
        }
        
        // 页面加载完成后初始化动画
        document.addEventListener('DOMContentLoaded', () => {
            const insertionSort = new InsertionSortAnimation();
        });
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 交互式教学动画使用指南

欢迎使用“插入排序（抓牌整理）”交互式教学动画！本动画旨在通过直观的视觉呈现和交互式操作，帮助您深入理解插入排序算法的核心原理。无论您是计算机科学初学者，还是希望巩固算法知识的进阶学习者，本工具都将为您提供沉浸式的学习体验。

---

### 一、功能说明

本动画将插入排序算法的抽象过程转化为生动的视觉演示，通过以下核心功能帮助您掌握算法：

1. **算法过程可视化**：将数组元素以“扑克牌”形式呈现，动态展示排序全过程
2. **分步执行控制**：支持播放、暂停、单步前进/后退，完全掌控学习节奏
3. **多视图联动**：动画视图、代码视图、变量视图同步更新，建立完整认知
4. **即时状态反馈**：实时显示算法状态、变量值和当前操作说明

### 二、主要功能

#### 1. 动画控制区
- **▶ 播放**：开始连续动画演示，自动执行排序全过程
- **⏸ 暂停**：暂停当前动画，便于仔细观察
- **◀ 上一步**：回退到前一个算法步骤，支持回溯学习
- **▶ 下一步**：手动前进到下一个算法步骤
- **↺ 重置**：恢复初始状态，重新开始

#### 2. 速度调节
- 使用滑块调节动画速度（极慢 → 最快）
- 建议初学者使用“慢速”或“中速”，逐步理解每个步骤
- 熟悉后可加快速度，观察算法整体流程

#### 3. 视觉区域
- **已排序区域**（绿色背景）：表示已完成排序的部分
- **未排序区域**（灰色背景）：表示待处理的部分
- **当前待插入元素**（橙色高亮）：正在处理的“扑克牌”
- **正在比较的元素**（蓝色高亮）：与待插入元素比较的元素

#### 4. 信息面板
- **算法代码区**：显示插入排序伪代码，当前执行行高亮显示
- **变量值面板**：实时显示 i、key、j 等关键变量的当前值
- **状态说明区**：用自然语言描述当前正在执行的操作

### 三、设计特色

#### 1. 双重认知模型
- **扑克牌比喻**：将算法过程类比为整理手中的扑克牌，降低理解门槛
- **数组操作视图**：同步显示实际的数组操作，连接比喻与抽象实现

#### 2. 渐进式学习支持
- **分步分解**：将算法分解为“选取→比较→移动→插入”四个原子操作
- **循环不变式可视化**：始终突出显示“已排序区域保持有序”这一关键性质

#### 3. 多感官学习体验
- **视觉编码**：使用颜色、位置、动画等多种视觉线索
- **交互反馈**：通过按钮操作和状态反馈增强学习参与感
- **同步更新**：动画、代码、变量三视图实时同步

### 四、教学要点

#### 核心概念理解
1. **关键变量角色**：
   - `i`：指向当前待插入元素的索引
   - `key`：当前待插入元素的值（手中的“新牌”）
   - `j`：在已排序部分进行比较的索引

2. **算法三阶段**：
   - **选取阶段**：从未排序部分取出一个元素作为 `key`
   - **比较与移动阶段**：将 `key` 与已排序部分从右向左比较，将大于 `key` 的元素右移
   - **插入阶段**：找到正确位置后插入 `key`

3. **循环不变式**：
   - 在算法的每个循环中，`arr[0..i-1]` 始终保持有序
   - 这是理解算法正确性的关键

#### 学习路径建议
1. **初次接触**：
   - 使用“播放”功能观看完整排序过程
   - 观察“扑克牌”如何逐个插入到正确位置
   - 注意已排序区域如何逐渐扩大

2. **深入理解**：
   - 使用“暂停”和“下一步”功能，单步执行算法
   - 在每个步骤暂停，观察变量值的变化
   - 对照代码高亮行，理解当前执行的操作

3. **巩固掌握**：
   - 尝试预测下一步操作，然后点击“下一步”验证
   - 使用“上一步”功能回溯，重新观察关键步骤
   - 调整不同数据规模，观察算法行为变化

### 五、使用建议

#### 针对不同学习阶段
- **初学者**：建议从“中速”播放开始，建立整体印象后，切换到“慢速”单步学习
- **中级学习者**：重点关注代码与动画的对应关系，理解每个操作的具体实现
- **教师/助教**：可在关键步骤暂停，引导学生预测下一步，培养算法思维

#### 最佳实践
1. **观察→思考→验证**循环：
   - 观察当前状态
   - 思考下一步应该发生什么
   - 点击“下一步”验证你的预测

2. **多角度关联学习**：
   - 同时关注动画变化、代码高亮和变量更新
   - 思考“为什么这个元素要移动到这里？”
   - 理解“比较条件”何时满足，何时不满足

3. **主动探索**：
   - 尝试在算法执行到一半时点击“重置”
   - 观察不同初始数组的排序过程
   - 思考：如果数组已经部分有序，算法效率如何？

#### 教学场景应用
- **课堂演示**：教师可使用本动画作为课堂辅助工具，直观展示算法过程
- **自主学习**：学生可按照自己的节奏反复观看、单步执行
- **小组讨论**：小组成员可共同操作动画，讨论算法细节和优化可能

---

### 开始您的学习之旅吧！

插入排序是理解更复杂算法的基础。通过本交互式动画，您不仅能够掌握插入排序的具体实现，更能培养“分治思维”和“循环不变式”等重要的算法思想。

**温馨提示**：学习算法就像学习一门新语言——需要耐心和实践。不要急于求成，享受每一个“啊哈！”时刻的喜悦！

祝您学习愉快，算法精进！ 🚀