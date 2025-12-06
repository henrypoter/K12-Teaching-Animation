# 需求：归并排序的合并过程（两个有序数组合并）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要是学习数据结构和算法的初学者（如大学生或编程自学者）。他们的核心需求是：
1.  **理解抽象过程**：将“合并两个有序数组”这一抽象的、基于指针/索引的算法逻辑，转化为直观、可视的动画过程。
2.  **掌握关键步骤**：清晰地看到两个指针如何移动、比较，以及如何将较小的元素依次放入新数组。
3.  **突破认知难点**：理解“当一个数组元素耗尽后，如何将另一个数组的剩余部分直接复制”这一关键步骤。
4.  **可控制的学习节奏**：能够暂停、单步执行、回看，以适应不同的学习速度和进行深度思考。

#### 教学设计思路
1.  **核心概念**：
    *   **输入**：两个**已排序**的数组（例如 `[3, 8, 15]` 和 `[5, 12, 20]`）。
    *   **过程**：使用两个“指针”（或索引）`i` 和 `j`，分别指向两个数组的当前待比较元素。比较 `arr1[i]` 和 `arr2[j]`，将**较小的**元素放入结果数组，并移动对应数组的指针。重复此过程，直到一个数组的所有元素都被处理完。
    *   **收尾**：将另一个数组中剩余的所有元素直接按顺序追加到结果数组末尾。
    *   **输出**：一个合并后的有序数组。

2.  **认知规律**：
    *   **从具体到抽象**：使用颜色、标签、箭头等视觉元素具象化“指针”和“比较”操作。
    *   **分解步骤**：将合并过程分解为“初始化”、“比较与选择”、“移动指针”、“填充结果”和“处理剩余”等清晰的子步骤，并通过高亮和文字提示引导用户关注当前步骤。
    *   **即时反馈**：每次交互（如点击“下一步”）后，动画变化和状态更新（指针位置、结果数组填充）同步发生，强化因果联系。

3.  **交互设计**：
    *   **流程控制**：提供“上一步”、“下一步”、“播放/暂停”、“重置”按钮，让用户完全掌控动画进度。
    *   **状态可视化**：
        *   用不同颜色区分两个输入数组和结果数组。
        *   用带标签的箭头（`i`, `j`, `k`）明确指示当前指针位置。
        *   在比较时，高亮待比较的两个元素。
        *   在移动元素时，使用平滑的动画（如平移）将元素从原数组“移动”到结果数组的对应位置。
    *   **信息面板**：实时显示当前步骤的描述、伪代码或自然语言解释。

4.  **视觉呈现**：
    *   **布局**：将两个输入数组水平并排置于画面上方，结果数组置于画面下方中央，形成清晰的“输入-处理-输出”流。
    *   **动画**：
        *   指针移动：箭头平滑地滑动到新位置。
        *   元素移动：被选中的元素有一个“弹出”效果，然后沿弧线飞入结果数组的对应位置，并伴随颜色渐变，表示其“归属”已改变。
        *   比较高亮：待比较元素会有脉动或边框加粗的效果。
    *   **状态标识**：当某个数组的指针越界（即该数组元素已耗尽）时，对应的箭头变灰或消失，直观表示“已完成”。

#### 配色方案选择
选择对比鲜明、柔和且符合教育场景的配色，确保可读性和舒适度。
*   **数组1**：使用**蓝色系**（如 `#4A90E2` 表示元素，`#2C6FB3` 表示高亮）。
*   **数组2**：使用**绿色系**（如 `#50C878` 表示元素，`#2E8B57` 表示高亮）。
*   **结果数组**：使用**中性紫色系**（如 `#9B59B6`），表示由两者混合生成。
*   **指针/箭头**：使用醒目的**橙色**（`#FF9800`）或**红色**（`#E74C3C`），并配上 `i`, `j`, `k` 标签。
*   **背景与文本**：浅灰色背景（`#f5f5f5`），深灰色文字（`#333333`），确保清晰。
*   **高亮与完成**：比较时使用**黄色**（`#FFF176`）作为临时高亮。已完成处理的元素颜色稍作淡化（降低饱和度或透明度）。

#### 交互功能列表
1.  **核心控制面板**：
    *   `重置`：将所有数组恢复为初始状态，指针归零。
    *   `上一步`：回退到上一个操作步骤，用于复习。
    *   `播放/暂停`：自动连续执行合并步骤（可调节速度）或暂停。
    *   `下一步`：手动执行下一个合并步骤（比较、移动、指针更新）。
2.  **可视化元素**：
    *   可点击的“步骤提示”或“伪代码”区域，点击后可高亮动画中对应的部分。
    *   可选的“显示/隐藏指针标签”或“显示/隐藏数值”开关。
3.  **信息显示面板**：
    *   **当前步骤说明**：用文字描述正在发生什么（例如：“比较 arr1[i]=8 和 arr2[j]=5，5更小，将其放入结果数组”）。
    *   **状态摘要**：显示当前指针 `i`, `j` 和结果数组索引 `k` 的值。
    *   （可选）**算法伪代码**：高亮显示当前执行的代码行。
4.  **配置选项（可选，用于扩展学习）**：
    *   `随机生成数组`：生成新的随机有序数组进行练习。
    *   `自定义数组`：允许用户输入自己的两个有序数组。
    *   `动画速度调节滑块`。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>归并排序：合并两个有序数组 - 教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
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
            padding-bottom: 20px;
            border-bottom: 2px solid #e0e0e0;
        }
        
        h1 {
            color: #2C3E50;
            margin-bottom: 10px;
        }
        
        .subtitle {
            color: #7F8C8D;
            font-size: 1.1em;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .visualization-area {
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            position: relative;
            min-height: 450px;
        }
        
        .arrays-container {
            display: flex;
            justify-content: space-around;
            align-items: flex-start;
            margin-bottom: 40px;
            position: relative;
        }
        
        .array-box {
            text-align: center;
            padding: 15px;
            border-radius: 8px;
            background-color: #f9f9f9;
            min-width: 250px;
        }
        
        .array-title {
            font-weight: bold;
            margin-bottom: 15px;
            font-size: 1.2em;
        }
        
        #array1-title {
            color: #2C6FB3;
        }
        
        #array2-title {
            color: #2E8B57;
        }
        
        #result-title {
            color: #9B59B6;
        }
        
        .array-elements {
            display: flex;
            justify-content: center;
            gap: 10px;
            flex-wrap: wrap;
            min-height: 80px;
        }
        
        .array-element {
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 8px;
            font-weight: bold;
            font-size: 1.3em;
            transition: all 0.3s ease;
            position: relative;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1);
        }
        
        .array1-element {
            background-color: #4A90E2;
            color: white;
        }
        
        .array2-element {
            background-color: #50C878;
            color: white;
        }
        
        .result-element {
            background-color: #9B59B6;
            color: white;
        }
        
        .element-index {
            position: absolute;
            top: -25px;
            font-size: 0.9em;
            color: #7F8C8D;
        }
        
        .pointers-container {
            position: absolute;
            top: 120px;
            left: 0;
            width: 100%;
            display: flex;
            justify-content: space-around;
        }
        
        .pointer {
            position: relative;
            text-align: center;
            transition: all 0.5s ease;
        }
        
        .pointer-arrow {
            font-size: 2em;
            color: #FF9800;
            filter: drop-shadow(0 2px 3px rgba(0,0,0,0.2));
        }
        
        .pointer-label {
            background-color: #FF9800;
            color: white;
            padding: 3px 8px;
            border-radius: 4px;
            font-weight: bold;
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 0.9em;
        }
        
        .controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .control-btn {
            padding: 12px 24px;
            border: none;
            border-radius: 6px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.2s;
            font-size: 1em;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .control-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        .control-btn:active {
            transform: translateY(0);
        }
        
        #reset-btn {
            background-color: #95A5A6;
            color: white;
        }
        
        #prev-btn {
            background-color: #3498DB;
            color: white;
        }
        
        #play-pause-btn {
            background-color: #2ECC71;
            color: white;
        }
        
        #next-btn {
            background-color: #E74C3C;
            color: white;
        }
        
        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            background-color: #ECF0F1;
            padding: 10px 15px;
            border-radius: 6px;
        }
        
        .info-panel {
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .step-info {
            background-color: #FFF9C4;
            padding: 20px;
            border-radius: 8px;
            border-left: 5px solid #FFD54F;
            margin-bottom: 20px;
            min-height: 80px;
            display: flex;
            align-items: center;
        }
        
        .step-description {
            font-size: 1.2em;
            font-weight: 500;
        }
        
        .status-info {
            display: flex;
            justify-content: space-around;
            background-color: #F8F9FA;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
        }
        
        .status-item {
            text-align: center;
        }
        
        .status-value {
            font-size: 1.8em;
            font-weight: bold;
            color: #2C3E50;
        }
        
        .status-label {
            font-size: 0.9em;
            color: #7F8C8D;
            margin-top: 5px;
        }
        
        .pseudocode {
            background-color: #2C3E50;
            color: #ECF0F1;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Consolas', 'Monaco', monospace;
            line-height: 1.8;
        }
        
        .code-line {
            padding: 5px 10px;
            border-radius: 4px;
            transition: background-color 0.3s;
        }
        
        .code-line.active {
            background-color: #34495E;
            color: #FFF;
            font-weight: bold;
        }
        
        .code-comment {
            color: #95A5A6;
        }
        
        .highlight {
            animation: highlight-pulse 1.5s infinite;
        }
        
        @keyframes highlight-pulse {
            0% { transform: scale(1); box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1); }
            50% { transform: scale(1.05); box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2); }
            100% { transform: scale(1); box-shadow: 0 3px 6px rgba(0, 0, 0, 0.1); }
        }
        
        .move-animation {
            animation: move-element 1s ease-in-out;
        }
        
        @keyframes move-element {
            0% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(var(--tx), var(--ty)) scale(1.1); }
            100% { transform: translate(0, 0) scale(1); }
        }
        
        .completed {
            opacity: 0.6;
        }
        
        .config-panel {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }
        
        .config-group {
            display: flex;
            gap: 10px;
            align-items: center;
        }
        
        .config-btn {
            padding: 10px 20px;
            background-color: #BDC3C7;
            color: #2C3E50;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.2s;
        }
        
        .config-btn:hover {
            background-color: #A6ACAF;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            color: #7F8C8D;
            font-size: 0.9em;
            padding-top: 20px;
            border-top: 1px solid #e0e0e0;
        }
        
        @media (max-width: 768px) {
            .arrays-container {
                flex-direction: column;
                align-items: center;
                gap: 40px;
            }
            
            .pointers-container {
                position: static;
                margin-top: 20px;
                order: 3;
            }
            
            .controls {
                flex-direction: column;
                align-items: center;
            }
            
            .control-btn {
                width: 100%;
                max-width: 300px;
                justify-content: center;
            }
            
            .config-panel {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>归并排序：合并两个有序数组</h1>
        <p class="subtitle">可视化教学动画 - 理解归并排序的核心步骤</p>
    </header>
    
    <div class="container">
        <section class="visualization-area">
            <div class="arrays-container">
                <div class="array-box">
                    <div class="array-title" id="array1-title">数组 A</div>
                    <div class="array-elements" id="array1-elements">
                        <!-- 数组1元素将通过JS动态生成 -->
                    </div>
                </div>
                
                <div class="array-box">
                    <div class="array-title" id="array2-title">数组 B</div>
                    <div class="array-elements" id="array2-elements">
                        <!-- 数组2元素将通过JS动态生成 -->
                    </div>
                </div>
                
                <div class="array-box">
                    <div class="array-title" id="result-title">结果数组 C</div>
                    <div class="array-elements" id="result-elements">
                        <!-- 结果数组元素将通过JS动态生成 -->
                    </div>
                </div>
                
                <div class="pointers-container">
                    <div class="pointer" id="pointer-i">
                        <div class="pointer-arrow">↓</div>
                        <div class="pointer-label">i</div>
                    </div>
                    <div class="pointer" id="pointer-j">
                        <div class="pointer-arrow">↓</div>
                        <div class="pointer-label">j</div>
                    </div>
                    <div class="pointer" id="pointer-k">
                        <div class="pointer-arrow">↓</div>
                        <div class="pointer-label">k</div>
                    </div>
                </div>
            </div>
            
            <div class="controls">
                <button class="control-btn" id="reset-btn">
                    <span>↺</span> 重置
                </button>
                <button class="control-btn" id="prev-btn">
                    <span>←</span> 上一步
                </button>
                <button class="control-btn" id="play-pause-btn">
                    <span>▶</span> 播放
                </button>
                <button class="control-btn" id="next-btn">
                    下一步 <span>→</span>
                </button>
                
                <div class="speed-control">
                    <span>速度:</span>
                    <input type="range" id="speed-slider" min="1" max="10" value="5">
                    <span id="speed-value">中速</span>
                </div>
            </div>
            
            <div class="config-panel">
                <div class="config-group">
                    <button class="config-btn" id="random-btn">随机生成数组</button>
                    <button class="config-btn" id="custom-btn">自定义数组</button>
                </div>
                <div class="config-group">
                    <label>
                        <input type="checkbox" id="show-indexes" checked> 显示索引
                    </label>
                    <label>
                        <input type="checkbox" id="show-pseudocode" checked> 显示伪代码
                    </label>
                </div>
            </div>
        </section>
        
        <section class="info-panel">
            <div class="step-info">
                <div class="step-description" id="step-description">
                    点击"下一步"开始合并过程。初始化：i=0, j=0, k=0
                </div>
            </div>
            
            <div class="status-info">
                <div class="status-item">
                    <div class="status-value" id="i-value">0</div>
                    <div class="status-label">指针 i (数组A)</div>
                </div>
                <div class="status-item">
                    <div class="status-value" id="j-value">0</div>
                    <div class="status-label">指针 j (数组B)</div>
                </div>
                <div class="status-item">
                    <div class="status-value" id="k-value">0</div>
                    <div class="status-label">指针 k (结果C)</div>
                </div>
            </div>
            
            <div class="pseudocode" id="pseudocode">
                <div class="code-line">function merge(arr1, arr2) {</div>
                <div class="code-line">  let i = 0, j = 0, k = 0;</div>
                <div class="code-line">  let result = [];</div>
                <div class="code-line">  </div>
                <div class="code-line">  <span class="code-comment">// 步骤1: 比较并合并</span></div>
                <div class="code-line" id="code-line-1">  while (i < arr1.length && j < arr2.length) {</div>
                <div class="code-line" id="code-line-2">    if (arr1[i] <= arr2[j]) {</div>
                <div class="code-line" id="code-line-3">      result[k] = arr1[i];</div>
                <div class="code-line" id="code-line-4">      i++;</div>
                <div class="code-line">    } else {</div>
                <div class="code-line" id="code-line-5">      result[k] = arr2[j];</div>
                <div class="code-line" id="code-line-6">      j++;</div>
                <div class="code-line">    }</div>
                <div class="code-line" id="code-line-7">    k++;</div>
                <div class="code-line">  }</div>
                <div class="code-line">  </div>
                <div class="code-line">  <span class="code-comment">// 步骤2: 复制剩余元素</span></div>
                <div class="code-line" id="code-line-8">  while (i < arr1.length) {</div>
                <div class="code-line" id="code-line-9">    result[k] = arr1[i];</div>
                <div class="code-line" id="code-line-10">    i++; k++;</div>
                <div class="code-line">  }</div>
                <div class="code-line">  </div>
                <div class="code-line" id="code-line-11">  while (j < arr2.length) {</div>
                <div class="code-line" id="code-line-12">    result[k] = arr2[j];</div>
                <div class="code-line" id="code-line-13">    j++; k++;</div>
                <div class="code-line">  }</div>
                <div class="code-line">  </div>
                <div class="code-line">  return result;</div>
                <div class="code-line">}</div>
            </div>
        </section>
    </div>
    
    <footer>
        <p>归并排序合并过程教学动画 | 设计：熊猫老师 | 使用HTML5、CSS3和JavaScript实现</p>
    </footer>

    <script>
        // 初始数据
        let arr1 = [3, 8, 15, 22];
        let arr2 = [5, 12, 20, 25];
        let result = [];
        
        // 指针状态
        let i = 0; // arr1指针
        let j = 0; // arr2指针
        let k = 0; // result指针
        
        // 动画状态
        let animationSpeed = 800; // 毫秒
        let isPlaying = false;
        let playInterval = null;
        let stepHistory = [];
        let currentStep = 0;
        
        // DOM元素
        const array1Elements = document.getElementById('array1-elements');
        const array2Elements = document.getElementById('array2-elements');
        const resultElements = document.getElementById('result-elements');
        const pointerI = document.getElementById('pointer-i');
        const pointerJ = document.getElementById('pointer-j');
        const pointerK = document.getElementById('pointer-k');
        const stepDescription = document.getElementById('step-description');
        const iValue = document.getElementById('i-value');
        const jValue = document.getElementById('j-value');
        const kValue = document.getElementById('k-value');
        const speedSlider = document.getElementById('speed-slider');
        const speedValue = document.getElementById('speed-value');
        const showIndexes = document.getElementById('show-indexes');
        const showPseudocode = document.getElementById('show-pseudocode');
        const pseudocode = document.getElementById('pseudocode');
        
        // 初始化
        function init() {
            renderArrays();
            updatePointers();
            updateStepDescription("初始化：i=0, j=0, k=0。点击\"下一步\"开始合并过程。");
            updateStatus();
            resetCodeHighlight();
            highlightCodeLine(0);
            
            // 保存初始状态到历史
            stepHistory = [{
                i: 0,
                j: 0,
                k: 0,
                result: [],
                description: "初始状态",
                codeLine: 0
            }];
            currentStep = 0;
        }
        
        // 渲染数组
        function renderArrays() {
            // 清空数组元素
            array1Elements.innerHTML = '';
            array2Elements.innerHTML = '';
            resultElements.innerHTML = '';
            
            // 渲染数组1
            arr1.forEach((value, index) => {
                const element = document.createElement('div');
                element.className = 'array-element array1-element';
                element.textContent = value;
                element.id = `arr1-${index}`;
                
                if (showIndexes.checked) {
                    const indexLabel = document.createElement('div');
                    indexLabel.className = 'element-index';
                    indexLabel.textContent = `[${index}]`;
                    element.appendChild(indexLabel);
                }
                
                array1Elements.appendChild(element);
            });
            
            // 渲染数组2
            arr2.forEach((value, index) => {
                const element = document.createElement('div');
                element.className = 'array-element array2-element';
                element.textContent = value;
                element.id = `arr2-${index}`;
                
                if (showIndexes.checked) {
                    const indexLabel = document.createElement('div');
                    indexLabel.className = 'element-index';
                    indexLabel.textContent = `[${index}]`;
                    element.appendChild(indexLabel);
                }
                
                array2Elements.appendChild(element);
            });
            
            // 渲染结果数组
            // 先创建空位
            for (let idx = 0; idx < arr1.length + arr2.length; idx++) {
                const element = document.createElement('div');
                element.className = 'array-element result-element';
                element.id = `result-${idx}`;
                
                if (idx < result.length) {
                    element.textContent = result[idx];
                } else {
                    element.textContent = '?';
                    element.style.opacity = '0.5';
                }
                
                if (showIndexes.checked) {
                    const indexLabel = document.createElement('div');
                    indexLabel.className = 'element-index';
                    indexLabel.textContent = `[${idx}]`;
                    element.appendChild(indexLabel);
                }
                
                resultElements.appendChild(element);
            }
        }
        
        // 更新指针位置
        function updatePointers() {
            // 计算指针位置
            const arr1Element = document.getElementById(`arr1-${i}`);
            const arr2Element = document.getElementById(`arr2-${j}`);
            const resultElement = document.getElementById(`result-${k}`);
            
            // 更新指针i
            if (i < arr1.length && arr1Element) {
                const rect = arr1Element.getBoundingClientRect();
                const containerRect = array1Elements.getBoundingClientRect();
                pointerI.style.left = `${rect.left + rect.width/2 - containerRect.left}px`;
                pointerI.style.display = 'block';
            } else {
                pointerI.style.display = 'none';
            }
            
            // 更新指针j
            if (j < arr2.length && arr2Element) {
                const rect = arr2Element.getBoundingClientRect();
                const containerRect = array2Elements.getBoundingClientRect();
                pointerJ.style.left = `${rect.left + rect.width/2 - containerRect.left}px`;
                pointerJ.style.display = 'block';
            } else {
                pointerJ.style.display = 'none';
            }
            
            // 更新指针k
            if (k < arr1.length + arr2.length && resultElement) {
                const rect = resultElement.getBoundingClientRect();
                const containerRect = resultElements.getBoundingClientRect();
                pointerK.style.left = `${rect.left + rect.width/2 - containerRect.left}px`;
                pointerK.style.display = 'block';
            } else {
                pointerK.style.display = 'none';
            }
        }
        
        // 更新步骤描述
        function updateStepDescription(text) {
            stepDescription.textContent = text;
        }
        
        // 更新状态显示
        function updateStatus() {
            iValue.textContent = i;
            jValue.textContent = j;
            kValue.textContent = k;
        }
        
        // 重置代码高亮
        function resetCodeHighlight() {
            document.querySelectorAll('.code-line').forEach(line => {
                line.classList.remove('active');
            });
        }
        
        // 高亮代码行
        function highlightCodeLine(lineNumber) {
            resetCodeHighlight();
            const lineId = `code-line-${lineNumber}`;
            const lineElement = document.getElementById(lineId);
            if (lineElement) {
                lineElement.classList.add('active');
            }
        }
        
        // 执行下一步
        function nextStep() {
            // 保存当前状态到历史
            const currentState = {
                i: i,
                j: j,
                k: k,
                result: [...result],
                description: stepDescription.textContent,
                codeLine: getCurrentCodeLine()
            };
            
            // 如果当前不是最后一步，截断历史
            if (currentStep < stepHistory.length - 1) {
                stepHistory = stepHistory.slice(0, currentStep + 1);
            }
            
            stepHistory.push(currentState);
            currentStep++;
            
            // 执行合并逻辑
            performMergeStep();
        }
        
        // 执行合并步骤
        function performMergeStep() {
            // 高亮当前比较的元素
            highlightCurrentElements();
            
            // 判断合并阶段
            if (i < arr1.length && j < arr2.length) {
                // 阶段1：两个数组都还有元素
                compareAndMerge();
            } else if (i < arr1.length) {
                // 阶段2：只有数组1有剩余元素
                copyRemainingFromArr1();
            } else if (j < arr2.length) {
                // 阶段3：只有数组2有剩余元素
                copyRemainingFromArr2();
            } else {
                // 合并完成
                updateStepDescription("合并完成！结果数组已包含所有有序元素。");
                highlightCodeLine(14);
                updateStatus();
                updatePointers();
                if (isPlaying) togglePlayPause();
                return;
            }
            
            updateStatus();
            updatePointers();
            renderArrays();
        }
        
        // 高亮当前比较的元素
        function highlightCurrentElements() {
            // 移除之前的高亮
            document.querySelectorAll('.array-element').forEach(el => {
                el.classList.remove('highlight');
            });
            
            // 高亮当前比较的元素
            if (i < arr1.length) {
                const arr1Element = document.getElementById(`arr1-${i}`);
                if (arr1Element) arr1Element.classList.add('highlight');
            }
            
            if (j < arr2.length) {
                const arr2Element = document.getElementById(`arr2-${j}`);
                if (arr2Element) arr2Element.classList.add('highlight');
            }
        }
        
        // 比较并合并
        function compareAndMerge() {
            if (arr1[i] <= arr2[j]) {
                // 取arr1[i]
                updateStepDescription(`比较 A[${i}]=${arr1[i]} 和 B[${j}]=${arr2[j]}，${arr1[i]} ≤ ${arr2[j]}，将 ${arr1[i]} 放入结果数组 C[${k}]`);
                highlightCodeLine(3);
                
                result[k] = arr1[i];
                i++;
            } else {
                // 取arr2[j]
                updateStepDescription(`比较 A[${i}]=${arr1[i]} 和 B[${j}]=${arr2[j]}，${arr2[j]} < ${arr1[i]}，将 ${arr2[j]} 放入结果数组 C[${k}]`);
                highlightCodeLine(5);
                
                result[k] = arr2[j];
                j++;
            }
            k++;
        }
        
        // 复制数组1的剩余元素
        function copyRemainingFromArr1() {
            updateStepDescription(`数组B已耗尽，将数组A的剩余元素 A[${i}]=${arr1[i]} 复制到结果数组 C[${k}]`);
            highlightCodeLine(9);
            
            result[k] = arr1[i];
            i++;
            k++;
        }
        
        // 复制数组2的剩余元素
        function copyRemainingFromArr2() {
            updateStepDescription(`数组A已耗尽，将数组B的剩余元素 B[${j}]=${arr2[j]} 复制到结果数组 C[${k}]`);
            highlightCodeLine(12);
            
            result[k] = arr2[j];
            j++;
            k++;
        }
        
        // 获取当前代码行
        function getCurrentCodeLine() {
            if (i < arr1.length && j < arr2.length) {
                return arr1[i] <= arr2[j] ? 3 : 5;
            } else if (i < arr1.length) {
                return 9;
            } else if (j < arr2.length) {
                return 12;
            } else {
                return 14;
            }
        }
        
        // 上一步
        function prevStep() {
            if (currentStep > 0) {
                currentStep--;
                const prevState = stepHistory[currentStep];
                
                i = prevState.i;
                j = prevState.j;
                k = prevState.k;
                result = [...prevState.result];
                
                updateStepDescription(prevState.description);
                updateStatus();
                updatePointers();
                renderArrays();
                highlightCodeLine(prevState.codeLine);
                
                if (isPlaying) togglePlayPause();
            }
        }
        
        // 重置
        function reset() {
            i = 0;
            j = 0;
            k = 0;
            result = [];
            
            init();
            if (isPlaying) togglePlayPause();
        }
        
        // 切换播放/暂停
        function togglePlayPause() {
            const playPauseBtn = document.getElementById('play-pause-btn');
            
            if (isPlaying) {
                // 暂停
                clearInterval(playInterval);
                playPauseBtn.innerHTML = '<span>▶</span> 播放';
                isPlaying = false;
            } else {
                // 播放
                playPauseBtn.innerHTML = '<span>⏸</span> 暂停';
                isPlaying = true;
                
                playInterval = setInterval(() => {
                    // 检查是否已完成
                    if (i >= arr1.length && j >= arr2.length) {
                        togglePlayPause();
                        return;
                    }
                    
                    nextStep();
                }, animationSpeed);
            }
        }
        
        // 随机生成数组
        function generateRandomArrays() {
            // 生成随机长度(3-6)
            const len1 = Math.floor(Math.random() * 4) + 3;
            const len2 = Math.floor(Math.random() * 4) + 3;
            
            // 生成随机起始值
            const start1 = Math.floor(Math.random() * 10) + 1;
            const start2 = Math.floor(Math.random() * 10) + 1;
            
            // 生成递增数组
            arr1 = [];
            arr2 = [];
            
            let current = start1;
            for (let idx = 0; idx < len1; idx++) {
                arr1.push(current);
                current += Math.floor(Math.random() * 5) + 1;
            }
            
            current = start2;
            for (let idx = 0; idx < len2; idx++) {
                arr2.push(current);
                current += Math.floor(Math.random() * 5) + 1;
            }
            
            reset();
        }
        
        // 自定义数组
        function customArrays() {
            const input1 = prompt("请输入第一个有序数组，用逗号分隔（例如：3,8,15）：", arr1.join(","));
            const input2 = prompt("请输入第二个有序数组，用逗号分隔（例如：5,12,20）：", arr2.join(","));
            
            if (input1 && input2) {
                try {
                    const newArr1 = input1.split(',').map(num => parseInt(num.trim())).filter(num => !isNaN(num));
                    const newArr2 = input2.split(',').map(num => parseInt(num.trim())).filter(num => !isNaN(num));
                    
                    // 验证数组是否有序
                    let isSorted1 = true;
                    let isSorted2 = true;
                    
                    for (let idx = 1; idx < newArr1.length; idx++) {
                        if (newArr1[idx] < newArr1[idx-1]) {
                            isSorted1 = false;
                            break;
                        }
                    }
                    
                    for (let idx = 1; idx < newArr2.length; idx++) {
                        if (newArr2[idx] < newArr2[idx-1]) {
                            isSorted2 = false;
                            break;
                        }
                    }
                    
                    if (!isSorted1 || !isSorted2) {
                        alert("请注意：输入的数组必须是有序的（从小到大）。");
                    }
                    
                    if (newArr1.length > 0 && newArr2.length > 0) {
                        arr1 = newArr1;
                        arr2 = newArr2;
                        reset();
                    }
                } catch (e) {
                    alert("输入格式不正确，请使用逗号分隔数字。");
                }
            }
        }
        
        // 事件监听
        document.getElementById('reset-btn').addEventListener('click', reset);
        document.getElementById('prev-btn').addEventListener('click', prevStep);
        document.getElementById('next-btn').addEventListener('click', nextStep);
        document.getElementById('play-pause-btn').addEventListener('click', togglePlayPause);
        document.getElementById('random-btn').addEventListener('click', generateRandomArrays);
        document.getElementById('custom-btn').addEventListener('click', customArrays);
        
        // 速度控制
        speedSlider.addEventListener('input', function() {
            const speed = parseInt(this.value);
            animationSpeed = 1200 - (speed * 100); // 从1100ms到200ms
            
            // 更新速度标签
            if (speed <= 3) {
                speedValue.textContent = '慢速';
            } else if (speed <= 7) {
                speedValue.textContent = '中速';
            } else {
                speedValue.textContent = '快速';
            }
            
            // 如果正在播放，更新间隔
            if (isPlaying) {
                clearInterval(playInterval);
                playInterval = setInterval(() => {
                    if (i >= arr1.length && j >= arr2.length) {
                        togglePlayPause();
                        return;
                    }
                    nextStep();
                }, animationSpeed);
            }
        });
        
        // 显示/隐藏索引
        showIndexes.addEventListener('change', function() {
            renderArrays();
            updatePointers();
        });
        
        // 显示/隐藏伪代码
        showPseudocode.addEventListener('change', function() {
            pseudocode.style.display = this.checked ? 'block' : 'none';
        });
        
        // 窗口大小改变时更新指针位置
        window.addEventListener('resize', updatePointers);
        
        // 初始化应用
        init();
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 《归并排序合并过程》交互式教学动画使用指南

欢迎使用“归并排序：合并两个有序数组”交互式教学动画！本动画由教育技术专家“熊猫老师”精心设计，旨在通过直观的可视化方式，帮助您深入理解归并排序算法的核心步骤。无论您是算法初学者，还是希望巩固知识的编程爱好者，本工具都将为您提供沉浸式的学习体验。

### 一、功能说明

本动画完整模拟了归并排序中“合并两个有序数组”的核心过程。您将看到：
- **两个已排序的输入数组**（数组A和数组B）
- **逐步生成的合并结果数组**（数组C）
- **三个动态移动的指针**（i, j, k）
- **实时更新的算法状态和伪代码高亮**

通过交互控制，您可以完全掌控学习节奏，深入观察每个比较、选择和移动的细节。

### 二、主要功能

#### 1. 核心控制面板
- **重置（↺）**：恢复所有数组到初始状态，指针归零
- **上一步（←）**：回退到上一个操作步骤，便于复习关键环节
- **播放/暂停（▶/⏸）**：自动连续执行合并步骤（可调节速度）
- **下一步（→）**：手动执行下一个合并步骤（比较、移动、指针更新）

#### 2. 可视化区域
- **三色区分**：蓝色（数组A）、绿色（数组B）、紫色（结果数组C）
- **动态指针**：橙色箭头清晰指示当前比较位置（i, j）和结果填充位置（k）
- **元素高亮**：当前比较的元素会有脉动效果，被选中的元素有平滑移动动画
- **状态标识**：当数组元素耗尽时，对应指针会消失

#### 3. 信息面板
- **步骤说明**：用自然语言描述当前正在执行的操作
- **状态摘要**：实时显示三个指针的数值
- **伪代码高亮**：同步高亮显示当前执行的算法代码行

#### 4. 配置选项
- **速度调节滑块**：从“慢速”到“快速”五档可调
- **随机生成数组**：一键生成新的随机有序数组
- **自定义数组**：输入您自己的有序数组进行练习
- **显示/隐藏选项**：控制索引标签和伪代码面板的显示

### 三、设计特色

#### 1. 认知友好的视觉设计
- **色彩心理学应用**：蓝色和绿色的对比色区分输入数组，紫色作为混合结果色
- **空间布局优化**：符合“输入-处理-输出”的自然阅读流
- **动画平滑过渡**：所有移动和状态变化都采用缓动函数，减少认知负荷

#### 2. 多层次信息呈现
- **表层**：直观的动画和颜色变化
- **中层**：文字描述和状态数值
- **深层**：算法伪代码和理论解释
满足不同学习风格用户的需求

#### 3. 完整的教学闭环
- **预习**：通过初始状态理解问题设定
- **学习**：通过单步执行观察细节
- **练习**：通过随机数组检验理解
- **复习**：通过回退功能巩固难点

### 四、教学要点

#### 核心概念分解
1. **初始化阶段**
   - 理解三个指针的初始位置（i=0, j=0, k=0）
   - 认识两个输入数组的有序特性

2. **比较与选择阶段**
   - 观察 `arr1[i]` 和 `arr2[j]` 的比较过程
   - 理解“选择较小者”的原则
   - 注意相等时的处理逻辑（稳定排序）

3. **指针移动逻辑**
   - 被选中数组的指针前进（i++ 或 j++）
   - 结果数组指针始终前进（k++）
   - 理解指针移动与数组边界的关系

4. **剩余元素处理**
   - 识别“一个数组耗尽”的条件
   - 理解“直接复制剩余元素”的优化
   - 观察不同剩余情况的处理方式

#### 常见难点突破
- **指针越界理解**：当 i ≥ arr1.length 时意味着什么？
- **稳定性体现**：当 arr1[i] == arr2[j] 时，为什么选择 arr1[i]？
- **时间复杂度**：为什么合并操作是 O(n+m)？

### 五、使用建议

#### 初学者学习路径
1. **首次接触**：点击“播放”观看完整过程，建立整体印象
2. **逐步深入**：使用“下一步”单步执行，结合步骤说明理解每个操作
3. **难点突破**：在关键步骤使用“上一步”反复观察
4. **主动测试**：使用“随机生成数组”功能检验理解程度
5. **理论联系**：对照伪代码高亮，理解代码与动画的对应关系

#### 教学者使用建议
1. **课堂演示**：使用中速播放，配合讲解关键概念
2. **小组练习**：让学生预测“下一步”操作，然后验证
3. **错误分析**：故意输入无序数组，观察问题所在
4. **扩展讨论**：引导学生思考：
   - 如果数组无序会怎样？
   - 如何修改代码实现降序合并？
   - 这个算法在哪些实际场景中应用？

#### 高级学习技巧
1. **不看动画写代码**：先观察几次动画，然后尝试自己实现合并函数
2. **复杂度分析**：通过不同大小的数组，直观感受 O(n) 线性复杂度
3. **算法比较**：思考合并排序与插入排序、选择排序的异同
4. **实际应用联想**：数据库的合并操作、版本控制的合并冲突解决等

---

**温馨提示**：算法学习如同登山，每一步都算数。本动画设计的目标不是让您快速“看完”，而是帮助您真正“看懂”。建议您放慢节奏，在关键步骤停下来思考，甚至拿出纸笔同步推导。当您能够不看动画也能在脑海中清晰呈现整个过程时，您就真正掌握了这个重要的算法思想。

祝您学习愉快，探索顺利！如有任何问题或改进建议，欢迎反馈。

*熊猫老师 设计*
*教育技术专家 | 创意程序员*