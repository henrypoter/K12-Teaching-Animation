# 需求：希尔排序（插入排序的升级版，间隔缩小动画）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要是学习数据结构和算法的初学者（如大学生或自学者）。他们可能已经理解了基础的插入排序，但对希尔排序的原理、特别是“间隔序列”和“子序列插入排序”的动态过程感到抽象和困惑。他们的核心需求是：
1.  **直观理解原理**：通过动画将抽象的“间隔缩小”和“分组插入排序”过程可视化，弥补静态文字和代码的不足。
2.  **掌握算法步骤**：清晰地看到希尔排序是如何通过多轮、不同间隔的插入排序来工作的。
3.  **观察性能优势**：直观感受相比于普通插入排序，希尔排序如何通过“让元素大跨度移动”来提前减少逆序对，从而提高效率。
4.  **可控制的学习体验**：能够暂停、单步执行、重置，以便在关键步骤停下来思考和消化。

#### 教学设计思路
*   **核心概念拆解**：
    1.  **间隔序列（Gap Sequence）**：这是希尔排序的灵魂。动画将突出展示当前使用的间隔（如初始间隔为数组长度的一半，并逐次减半）。
    2.  **子序列形成与排序**：对于每个间隔，动画将用高亮颜色清晰地标出所有被该间隔“采样”出的子序列（例如，间隔为4时，索引为0,4,8...的元素构成一个子序列），并演示在这个子序列上进行的插入排序过程。
    3.  **间隔缩小**：完成一轮子序列排序后，间隔缩小（如减半），开始新一轮、更精细的排序，直至间隔为1（即标准的插入排序），此时数组已基本有序，最后一遍排序效率很高。
    4.  **与插入排序对比**：可以设置一个对比模式或旁白说明，强调普通插入排序每次只移动相邻元素，而希尔排序允许元素“跳跃”，从而更快地将元素移动到大致正确的位置。

*   **认知规律遵循**：
    *   **从已知到未知**：从回顾插入排序动画开始，引出其“每次只比较相邻元素，移动效率低”的问题。
    *   **分步演示**：将算法分解为多个“间隔轮次”，每轮再分解为多个“子序列排序步骤”。通过单步控制，让学习者跟上节奏。
    *   **突出变化**：使用强烈的视觉对比（颜色、连线、移动轨迹）来强调当前正在比较和交换的元素、当前子序列成员以及间隔的变化。
    *   **归纳总结**：动画结束后，或通过一个控制按钮，可以回放关键帧或展示文字总结，概括算法步骤和优势。

*   **交互设计**：
    *   **主动画区**：以水平排列的柱状图或带数字的圆块表示数组元素。高度或数字代表值的大小。
    *   **控制面板**：提供“播放/暂停”、“下一步”、“上一步”、“重置”按钮。以及“速度调节”滑块。
    *   **状态面板**：清晰显示当前状态，如“当前间隔 Gap = 4”、“正在排序第2个子序列（索引：1,5,9...）”、“正在比较元素[5]和[1]”等。
    *   **交互式解释**：鼠标悬停在控制按钮或状态标签上时，给出简短提示。点击某个元素，可以显示其当前索引和值。

*   **视觉呈现**：
    *   **数据结构可视化**：数组元素是视觉焦点。使用柱状图可以直观体现大小，使用带数字的圆块则更简洁，便于跟踪具体数字的移动。
    *   **颜色编码系统**：
        *   **默认状态**：元素为中性色（如浅灰色）。
        *   **当前间隔指示**：在数组上方或下方画一条标尺或一组连线，直观连接当前间隔下的子序列成员。
        *   **活动子序列**：当前正在排序的子序列，其所有成员用同一种颜色（如蓝色）高亮。
        *   **当前焦点元素**：子序列中正在被“插入”的元素（类似于插入排序中的“待插入牌”），用更醒目的颜色（如橙色）突出，并可能有一个轮廓或发光效果。
        *   **比较与交换**：当“焦点元素”与子序列中前一个元素比较时，两者用对比色（如红色）闪烁。如果发生交换，展示平滑的位置交换动画。
        *   **已排序区域**：随着间隔减小到1，逐渐用另一种颜色（如绿色）标记已最终就位的元素。

#### 配色方案选择
选择对比清晰、符合认知习惯且舒适的配色，避免过于刺眼。
*   **背景与基础元素**：
    *   画布背景：浅色调（#f8f9fa）
    *   数组元素默认填充：浅灰色（#dee2e6）
    *   元素边框/文字：深灰色（#495057）
*   **高亮与状态色**：
    *   **当前间隔/子序列高亮**：温和的蓝色（#4dabf7），用于连接线和子序列成员填充。
    *   **当前焦点元素（待插入元素）**：醒目的橙色（#ff922b），带有强调效果。
    *   **比较元素**：警示性的红色（#ff6b6b），用于比较瞬间的闪烁。
    *   **交换动画轨迹**：使用半透明的橙色或红色轨迹线。
    *   **最终有序状态**：成功的绿色（#51cf66），在间隔为1的排序完成后，或用于标记已排好的元素。
    *   **状态面板背景**：中性浅色（#e9ecef）
    *   **按钮**：主行动按钮（如播放）用蓝色（#339af0），重置用灰色，其他用中性色。

#### 交互功能列表
1.  **动画控制**：
    *   **播放/暂停**：开始或暂停连续动画。
    *   **下一步**：单步执行到下一个关键步骤（如一次比较、一次交换、或切换到下一个子序列/间隔）。
    *   **上一步**：回退到上一个关键步骤，便于回顾。
    *   **重置**：将动画恢复到初始未排序状态。
    *   **速度调节滑块**：控制连续播放的速度。
2.  **数据控制**：
    *   **随机生成数组**：生成一组新的随机数。
    *   **自定义数组输入**（可选高级功能）：允许用户输入一组自定义数字。
3.  **视觉控制**（可选）：
    *   **切换视图**：在“柱状图”和“数字圆块”两种数据表示法间切换。
    *   **高亮开关**：可开关子序列高亮连线，以减少视觉干扰。
4.  **信息显示**：
    *   **算法状态显示**：实时显示当前间隔、当前操作描述、已进行的轮次等。
    *   **元素信息提示**：鼠标悬停在数组元素上时，显示其索引和值。
    *   **计数器**（可选）：显示已进行的比较次数和交换次数。
5.  **教学模式**（可选增强功能）：
    *   **分步讲解模式**：在关键步骤弹出文字解说框。
    *   **与插入排序对比模式**：并排显示希尔排序和普通插入排序处理同一数组的动画，直观展示效率差异。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>希尔排序算法动画演示</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background-color: #f8f9fa;
            color: #495057;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #e9ecef;
        }

        h1 {
            color: #339af0;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #868e96;
            font-size: 1.1rem;
        }

        .container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .animation-section {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            padding: 25px;
        }

        .section-title {
            color: #4dabf7;
            margin-bottom: 20px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title i {
            font-size: 1.5rem;
        }

        .canvas-container {
            position: relative;
            width: 100%;
            height: 400px;
            background-color: #f8f9fa;
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid #e9ecef;
        }

        #animationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .controls-section {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            padding: 25px;
        }

        .controls-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-bottom: 25px;
        }

        .control-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .control-label {
            font-weight: 600;
            color: #495057;
            font-size: 0.95rem;
        }

        .buttons-row {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 20px;
        }

        .btn {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .btn-primary {
            background-color: #339af0;
            color: white;
        }

        .btn-primary:hover {
            background-color: #228be6;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background-color: #e9ecef;
            color: #495057;
        }

        .btn-secondary:hover {
            background-color: #dee2e6;
            transform: translateY(-2px);
        }

        .btn-success {
            background-color: #51cf66;
            color: white;
        }

        .btn-success:hover {
            background-color: #40c057;
            transform: translateY(-2px);
        }

        .btn-warning {
            background-color: #ff922b;
            color: white;
        }

        .btn-warning:hover {
            background-color: #fd7e14;
            transform: translateY(-2px);
        }

        .btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none !important;
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .slider {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            appearance: none;
            background: #e9ecef;
            border-radius: 4px;
            outline: none;
        }

        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #339af0;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        .slider-value {
            min-width: 40px;
            text-align: center;
            font-weight: 600;
            color: #339af0;
        }

        .status-section {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            padding: 25px;
        }

        .status-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .status-card {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 20px;
            border-left: 4px solid #4dabf7;
        }

        .status-title {
            font-size: 0.9rem;
            color: #868e96;
            margin-bottom: 8px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .status-value {
            font-size: 1.5rem;
            font-weight: 700;
            color: #495057;
        }

        .status-value.highlight {
            color: #ff922b;
        }

        .status-value.gap {
            color: #4dabf7;
        }

        .status-value.comparisons {
            color: #ff6b6b;
        }

        .status-value.swaps {
            color: #51cf66;
        }

        .legend-section {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            padding: 25px;
        }

        .legend-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 15px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .legend-color {
            width: 24px;
            height: 24px;
            border-radius: 4px;
            border: 2px solid rgba(0, 0, 0, 0.1);
        }

        .legend-text {
            font-size: 0.95rem;
            color: #495057;
        }

        .instructions {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 20px;
            margin-top: 10px;
            border-left: 4px solid #ff922b;
        }

        .instructions h3 {
            color: #ff922b;
            margin-bottom: 10px;
        }

        .instructions ul {
            padding-left: 20px;
        }

        .instructions li {
            margin-bottom: 8px;
        }

        @media (max-width: 768px) {
            .controls-grid {
                grid-template-columns: 1fr;
            }
            
            .buttons-row {
                justify-content: center;
            }
            
            .btn {
                flex: 1;
                min-width: 120px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <div class="header">
        <h1><i class="fas fa-sort-amount-down"></i> 希尔排序算法动画演示</h1>
        <p class="subtitle">插入排序的升级版 - 通过间隔序列实现高效排序</p>
    </div>

    <div class="container">
        <div class="animation-section">
            <h2 class="section-title"><i class="fas fa-play-circle"></i> 算法动画演示</h2>
            <div class="canvas-container">
                <canvas id="animationCanvas"></canvas>
            </div>
        </div>

        <div class="controls-section">
            <h2 class="section-title"><i class="fas fa-sliders-h"></i> 动画控制</h2>
            
            <div class="controls-grid">
                <div class="control-group">
                    <div class="control-label">数组大小</div>
                    <div class="slider-container">
                        <input type="range" min="5" max="20" value="12" class="slider" id="arraySizeSlider">
                        <span class="slider-value" id="arraySizeValue">12</span>
                    </div>
                </div>
                
                <div class="control-group">
                    <div class="control-label">动画速度</div>
                    <div class="slider-container">
                        <input type="range" min="1" max="10" value="5" class="slider" id="speedSlider">
                        <span class="slider-value" id="speedValue">5</span>
                    </div>
                </div>
            </div>

            <div class="buttons-row">
                <button class="btn btn-primary" id="playPauseBtn">
                    <i class="fas fa-play"></i> 播放
                </button>
                <button class="btn btn-secondary" id="nextStepBtn">
                    <i class="fas fa-step-forward"></i> 下一步
                </button>
                <button class="btn btn-secondary" id="prevStepBtn">
                    <i class="fas fa-step-backward"></i> 上一步
                </button>
                <button class="btn btn-warning" id="resetBtn">
                    <i class="fas fa-redo"></i> 重置
                </button>
                <button class="btn btn-success" id="newArrayBtn">
                    <i class="fas fa-random"></i> 新数组
                </button>
            </div>
        </div>

        <div class="status-section">
            <h2 class="section-title"><i class="fas fa-info-circle"></i> 算法状态</h2>
            <div class="status-grid">
                <div class="status-card">
                    <div class="status-title">当前间隔 (Gap)</div>
                    <div class="status-value gap" id="currentGap">-</div>
                </div>
                <div class="status-card">
                    <div class="status-title">当前操作</div>
                    <div class="status-value highlight" id="currentOperation">等待开始</div>
                </div>
                <div class="status-card">
                    <div class="status-title">比较次数</div>
                    <div class="status-value comparisons" id="comparisonCount">0</div>
                </div>
                <div class="status-card">
                    <div class="status-title">交换次数</div>
                    <div class="status-value swaps" id="swapCount">0</div>
                </div>
            </div>
        </div>

        <div class="legend-section">
            <h2 class="section-title"><i class="fas fa-palette"></i> 颜色图例</h2>
            <div class="legend-grid">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #dee2e6;"></div>
                    <div class="legend-text">默认元素</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #4dabf7;"></div>
                    <div class="legend-text">当前子序列</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #ff922b;"></div>
                    <div class="legend-text">焦点元素 (待插入)</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #ff6b6b;"></div>
                    <div class="legend-text">比较中元素</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #51cf66;"></div>
                    <div class="legend-text">已排序元素</div>
                </div>
            </div>
            
            <div class="instructions">
                <h3><i class="fas fa-lightbulb"></i> 希尔排序原理</h3>
                <ul>
                    <li><strong>间隔序列</strong>: 从较大间隔开始，逐渐减小间隔直到1（普通插入排序）</li>
                    <li><strong>子序列排序</strong>: 对每个间隔形成的子序列进行插入排序</li>
                    <li><strong>效率优势</strong>: 大间隔让元素大跨度移动，提前减少逆序对数量</li>
                    <li><strong>最终排序</strong>: 当间隔为1时，数组已基本有序，最后一遍插入排序效率很高</li>
                </ul>
            </div>
        </div>
    </div>

    <script>
        // 全局变量
        let canvas, ctx;
        let array = [];
        let animationId = null;
        let isPlaying = false;
        let animationSpeed = 5;
        let arraySize = 12;
        
        // 希尔排序状态变量
        let gap;
        let i, j;
        let temp;
        let currentSubArrayIndex = 0;
        let isComparing = false;
        let isSwapping = false;
        let animationStep = 0; // 0: 初始化, 1: 选择间隔, 2: 选择子序列, 3: 插入排序, 4: 完成
        let algorithmState = 'idle'; // 'idle', 'selecting_gap', 'selecting_subarray', 'insertion_sort', 'completed'
        
        // 统计变量
        let comparisonCount = 0;
        let swapCount = 0;
        
        // 颜色定义
        const colors = {
            default: '#dee2e6',
            subarray: '#4dabf7',
            focus: '#ff922b',
            comparing: '#ff6b6b',
            sorted: '#51cf66',
            background: '#f8f9fa',
            text: '#495057',
            line: '#adb5bd'
        };
        
        // 初始化
        function init() {
            canvas = document.getElementById('animationCanvas');
            ctx = canvas.getContext('2d');
            
            // 设置Canvas尺寸
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // 初始化数组
            generateRandomArray();
            
            // 初始化希尔排序
            initShellSort();
            
            // 设置事件监听器
            setupEventListeners();
            
            // 绘制初始状态
            draw();
        }
        
        // 调整Canvas大小
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            draw();
        }
        
        // 生成随机数组
        function generateRandomArray() {
            array = [];
            for (let i = 0; i < arraySize; i++) {
                array.push(Math.floor(Math.random() * 90) + 10); // 10-99之间的随机数
            }
            
            // 重置统计
            comparisonCount = 0;
            swapCount = 0;
            updateStatusDisplay();
        }
        
        // 初始化希尔排序状态
        function initShellSort() {
            // 初始间隔为数组长度的一半
            gap = Math.floor(arraySize / 2);
            i = gap;
            j = i;
            temp = null;
            currentSubArrayIndex = 0;
            isComparing = false;
            isSwapping = false;
            animationStep = 0;
            algorithmState = 'idle';
            
            // 更新状态显示
            updateStatusDisplay();
        }
        
        // 设置事件监听器
        function setupEventListeners() {
            // 播放/暂停按钮
            document.getElementById('playPauseBtn').addEventListener('click', togglePlayPause);
            
            // 下一步按钮
            document.getElementById('nextStepBtn').addEventListener('click', nextStep);
            
            // 上一步按钮（简化实现，实际需要状态历史）
            document.getElementById('prevStepBtn').addEventListener('click', prevStep);
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            
            // 新数组按钮
            document.getElementById('newArrayBtn').addEventListener('click', () => {
                generateRandomArray();
                initShellSort();
                draw();
            });
            
            // 数组大小滑块
            const arraySizeSlider = document.getElementById('arraySizeSlider');
            const arraySizeValue = document.getElementById('arraySizeValue');
            
            arraySizeSlider.addEventListener('input', () => {
                arraySize = parseInt(arraySizeSlider.value);
                arraySizeValue.textContent = arraySize;
                generateRandomArray();
                initShellSort();
                draw();
            });
            
            // 速度滑块
            const speedSlider = document.getElementById('speedSlider');
            const speedValue = document.getElementById('speedValue');
            
            speedSlider.addEventListener('input', () => {
                animationSpeed = parseInt(speedSlider.value);
                speedValue.textContent = animationSpeed;
            });
        }
        
        // 切换播放/暂停
        function togglePlayPause() {
            const playPauseBtn = document.getElementById('playPauseBtn');
            const icon = playPauseBtn.querySelector('i');
            
            if (isPlaying) {
                // 暂停动画
                if (animationId) {
                    cancelAnimationFrame(animationId);
                    animationId = null;
                }
                isPlaying = false;
                playPauseBtn.innerHTML = '<i class="fas fa-play"></i> 播放';
                algorithmState = 'idle';
            } else {
                // 开始动画
                isPlaying = true;
                playPauseBtn.innerHTML = '<i class="fas fa-pause"></i> 暂停';
                
                // 如果算法已完成，重置
                if (algorithmState === 'completed') {
                    resetAnimation();
                }
                
                // 开始动画循环
                animate();
            }
        }
        
        // 下一步
        function nextStep() {
            if (algorithmState === 'completed') return;
            
            performAlgorithmStep();
            draw();
        }
        
        // 上一步（简化版本，实际需要维护状态历史）
        function prevStep() {
            // 简化实现：重置并重新执行到上一步
            // 在实际应用中，需要维护一个状态历史栈
            alert("上一步功能需要维护状态历史，此为简化演示。请使用重置功能重新开始。");
        }
        
        // 重置动画
        function resetAnimation() {
            // 停止动画
            if (animationId) {
                cancelAnimationFrame(animationId);
                animationId = null;
            }
            
            isPlaying = false;
            document.getElementById('playPauseBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
            
            // 重新生成数组并初始化排序
            generateRandomArray();
            initShellSort();
            draw();
        }
        
        // 执行算法步骤
        function performAlgorithmStep() {
            // 根据当前状态执行相应的步骤
            switch(algorithmState) {
                case 'idle':
                    // 开始算法，选择初始间隔
                    algorithmState = 'selecting_gap';
                    updateStatusDisplay();
                    break;
                    
                case 'selecting_gap':
                    // 如果间隔为0，算法完成
                    if (gap <= 0) {
                        algorithmState = 'completed';
                        updateStatusDisplay();
                        return;
                    }
                    
                    // 开始当前间隔的排序
                    i = gap;
                    currentSubArrayIndex = 0;
                    algorithmState = 'selecting_subarray';
                    updateStatusDisplay();
                    break;
                    
                case 'selecting_subarray':
                    // 选择当前子序列
                    if (currentSubArrayIndex >= gap) {
                        // 当前间隔的所有子序列已处理完毕，减小间隔
                        gap = Math.floor(gap / 2);
                        algorithmState = 'selecting_gap';
                        updateStatusDisplay();
                        return;
                    }
                    
                    // 开始对当前子序列进行插入排序
                    i = currentSubArrayIndex + gap;
                    j = i;
                    temp = array[i];
                    isComparing = false;
                    isSwapping = false;
                    algorithmState = 'insertion_sort';
                    updateStatusDisplay();
                    break;
                    
                case 'insertion_sort':
                    // 执行插入排序的一步
                    if (j >= gap && array[j - gap] > temp) {
                        // 需要移动元素
                        isComparing = true;
                        comparisonCount++;
                        
                        // 移动元素
                        array[j] = array[j - gap];
                        swapCount++;
                        
                        j -= gap;
                        isSwapping = true;
                    } else {
                        // 插入元素到正确位置
                        array[j] = temp;
                        isComparing = false;
                        isSwapping = false;
                        
                        // 移动到下一个元素
                        i += gap;
                        
                        if (i >= arraySize) {
                            // 当前子序列排序完成，移动到下一个子序列
                            currentSubArrayIndex++;
                            algorithmState = 'selecting_subarray';
                        } else {
                            // 继续当前子序列的下一个元素
                            j = i;
                            temp = array[i];
                        }
                    }
                    updateStatusDisplay();
                    break;
                    
                case 'completed':
                    // 算法已完成
                    break;
            }
        }
        
        // 动画循环
        function animate() {
            if (!isPlaying) return;
            
            // 根据速度执行步骤
            const stepsPerFrame = Math.max(1, Math.floor(animationSpeed / 2));
            
            for (let s = 0; s < stepsPerFrame; s++) {
                performAlgorithmStep();
                
                // 如果算法完成，停止动画
                if (algorithmState === 'completed') {
                    isPlaying = false;
                    document.getElementById('playPauseBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
                    break;
                }
            }
            
            // 绘制
            draw();
            
            // 继续动画循环
            if (isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }
        
        // 更新状态显示
        function updateStatusDisplay() {
            document.getElementById('currentGap').textContent = gap > 0 ? gap : '完成';
            document.getElementById('comparisonCount').textContent = comparisonCount;
            document.getElementById('swapCount').textContent = swapCount;
            
            let operationText = '等待开始';
            
            switch(algorithmState) {
                case 'idle':
                    operationText = '等待开始';
                    break;
                case 'selecting_gap':
                    operationText = `选择间隔: ${gap}`;
                    break;
                case 'selecting_subarray':
                    operationText = `选择子序列 ${currentSubArrayIndex + 1}/${gap}`;
                    break;
                case 'insertion_sort':
                    if (isComparing) {
                        operationText = `比较: array[${j-gap}] > ${temp}`;
                    } else if (isSwapping) {
                        operationText = `移动: array[${j}] = array[${j-gap}]`;
                    } else {
                        operationText = `插入 ${temp} 到位置 ${j}`;
                    }
                    break;
                case 'completed':
                    operationText = '排序完成！';
                    break;
            }
            
            document.getElementById('currentOperation').textContent = operationText;
        }
        
        // 绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 计算元素尺寸和间距
            const elementWidth = Math.min(60, canvas.width / (arraySize * 1.5));
            const elementSpacing = elementWidth * 0.5;
            const totalWidth = arraySize * (elementWidth + elementSpacing) - elementSpacing;
            const startX = (canvas.width - totalWidth) / 2;
            const baseY = canvas.height * 0.7;
            const elementHeightMultiplier = 3;
            
            // 绘制标题
            ctx.font = 'bold 18px "Segoe UI", sans-serif';
            ctx.fillStyle = colors.text;
            ctx.textAlign = 'center';
            ctx.fillText('希尔排序算法演示', canvas.width / 2, 30);
            
            // 绘制当前间隔指示
            if (gap > 0 && algorithmState !== 'idle' && algorithmState !== 'completed') {
                ctx.font = '16px "Segoe UI", sans-serif';
                ctx.fillStyle = colors.subarray;
                ctx.textAlign = 'center';
                ctx.fillText(`当前间隔: ${gap}`, canvas.width / 2, 60);
                
                // 绘制间隔连线
                if (algorithmState === 'selecting_subarray' || algorithmState === 'insertion_sort') {
                    ctx.strokeStyle = colors.subarray;
                    ctx.lineWidth = 2;
                    ctx.setLineDash([5, 5]);
                    
                    // 绘制当前子序列的连线
                    for (let idx = currentSubArrayIndex; idx < arraySize; idx += gap) {
                        const x = startX + idx * (elementWidth + elementSpacing) + elementWidth / 2;
                        const y1 = baseY - array[idx] * elementHeightMultiplier - 20;
                        const y2 = baseY + 30;
                        
                        ctx.beginPath();
                        ctx.moveTo(x, y1);
                        ctx.lineTo(x, y2);
                        ctx.stroke();
                    }
                    
                    ctx.setLineDash([]);
                }
            }
            
            // 绘制数组元素
            for (let idx = 0; idx < arraySize; idx++) {
                const x = startX + idx * (elementWidth + elementSpacing);
                const height = array[idx] * elementHeightMultiplier;
                const y = baseY - height;
                
                // 确定元素颜色
                let color = colors.default;
                
                // 检查元素状态
                if (algorithmState === 'completed') {
                    color = colors.sorted;
                } else if (algorithmState === 'insertion_sort') {
                    // 当前子序列元素
                    if ((idx - currentSubArrayIndex) % gap === 0) {
                        color = colors.subarray;
                    }
                    
                    // 焦点元素（待插入元素）
                    if (idx === i && !isSwapping) {
                        color = colors.focus;
                    }
                    
                    // 比较中的元素
                    if (isComparing && (idx === j || idx === j - gap)) {
                        color = colors.comparing;
                    }
                    
                    // 正在交换的元素
                    if (isSwapping && idx === j) {
                        color = colors.comparing;
                    }
                } else if (algorithmState === 'selecting_subarray') {
                    // 当前子序列元素
                    if ((idx - currentSubArrayIndex) % gap === 0) {
                        color = colors.subarray;
                    }
                }
                
                // 绘制元素矩形
                ctx.fillStyle = color;
                ctx.fillRect(x, y, elementWidth, height);
                
                // 绘制元素边框
                ctx.strokeStyle = colors.text;
                ctx.lineWidth = 1;
                ctx.strokeRect(x, y, elementWidth, height);
                
                // 绘制元素值
                ctx.fillStyle = colors.text;
                ctx.font = 'bold 14px "Segoe UI", sans-serif';
                ctx.textAlign = 'center';
                ctx.fillText(array[idx], x + elementWidth / 2, y + height / 2 + 5);
                
                // 绘制元素索引
                ctx.fillStyle = colors.text;
                ctx.font = '12px "Segoe UI", sans-serif';
                ctx.fillText(`[${idx}]`, x + elementWidth / 2, baseY + 20);
            }
            
            // 绘制当前操作说明
            if (algorithmState !== 'idle') {
                ctx.font = '14px "Segoe UI", sans-serif';
                ctx.fillStyle = colors.text;
                ctx.textAlign = 'left';
                
                let explanation = '';
                
                switch(algorithmState) {
                    case 'selecting_gap':
                        explanation = `当前间隔: ${gap} (数组长度/2并逐次减半)`;
                        break;
                    case 'selecting_subarray':
                        explanation = `处理子序列 ${currentSubArrayIndex + 1}/${gap}: 索引 ${currentSubArrayIndex}, ${currentSubArrayIndex+gap}, ${currentSubArrayIndex+2*gap}...`;
                        break;
                    case 'insertion_sort':
                        if (isComparing) {
                            explanation = `比较: array[${j-gap}] (${array[j-gap]}) > ${temp} ? 是，所以移动元素`;
                        } else if (isSwapping) {
                            explanation = `移动: array[${j}] = array[${j-gap}] (${array[j]})`;
                        } else {
                            explanation = `插入 ${temp} 到位置 ${j}`;
                        }
                        break;
                    case 'completed':
                        explanation = '排序完成！希尔排序通过间隔序列提前减少逆序对，比普通插入排序更高效。';
                        break;
                }
                
                // 绘制解释文本
                ctx.fillText(explanation, 20, canvas.height - 40);
            }
            
            // 绘制算法状态
            ctx.font = 'bold 16px "Segoe UI", sans-serif';
            ctx.fillStyle = colors.text;
            ctx.textAlign = 'right';
            
            let statusText = '';
            switch(algorithmState) {
                case 'idle': statusText = '就绪'; break;
                case 'selecting_gap': statusText = '选择间隔'; break;
                case 'selecting_subarray': statusText = '选择子序列'; break;
                case 'insertion_sort': statusText = '子序列插入排序'; break;
                case 'completed': statusText = '排序完成'; break;
            }
            
            ctx.fillText(`状态: ${statusText}`, canvas.width - 20, canvas.height - 40);
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

# 希尔排序交互式教学动画使用指南

欢迎使用希尔排序算法交互式教学动画！本工具旨在通过直观的可视化方式，帮助您深入理解希尔排序这一高效排序算法的核心原理和运行过程。无论您是算法初学者还是希望巩固知识的进阶学习者，本动画都将为您提供沉浸式的学习体验。

## 一、功能说明

本动画将希尔排序算法的执行过程分解为可视化的步骤，通过颜色编码、动态高亮和实时状态反馈，清晰展示以下核心概念：
- **间隔序列（Gap Sequence）**：算法如何从大间隔开始，逐步缩小直至为1
- **子序列形成**：每个间隔如何将原数组划分为多个子序列
- **子序列插入排序**：如何在每个子序列上执行插入排序
- **元素大跨度移动**：希尔排序相比普通插入排序的效率优势来源

## 二、主要功能

### 1. 动画控制区
- **播放/暂停**：开始或暂停连续动画演示
- **下一步**：单步执行算法，适合仔细研究每个关键步骤
- **上一步**：回退到上一步（注：此为简化实现，详细版本需状态历史）
- **重置**：恢复到初始状态，重新开始算法演示
- **新数组**：生成新的随机数组，观察算法在不同数据上的表现

### 2. 参数调节区
- **数组大小**：调节待排序数组的元素数量（5-20个）
- **动画速度**：控制连续播放时的执行速度（1-10档）

### 3. 状态显示区
- **当前间隔**：实时显示算法正在使用的间隔值
- **当前操作**：描述当前正在执行的具体操作
- **比较次数**：累计比较操作计数
- **交换次数**：累计元素移动/交换计数

### 4. 视觉图例区
提供颜色编码说明，帮助理解不同颜色代表的元素状态：
- **浅灰色**：默认状态的数组元素
- **蓝色**：当前间隔下的子序列成员
- **橙色**：焦点元素（当前待插入元素）
- **红色**：正在比较中的元素
- **绿色**：已排序完成的元素

## 三、设计特色

### 1. 渐进式可视化
- **分层展示**：先展示间隔选择，再展示子序列形成，最后展示插入排序细节
- **焦点突出**：使用醒目的橙色高亮当前处理的"待插入元素"
- **关系可视化**：通过虚线连接展示同一子序列中的元素关系

### 2. 多维度反馈
- **视觉反馈**：颜色变化、位置移动、连线指示
- **文字反馈**：实时状态描述、操作解释
- **数据反馈**：比较和交换次数统计

### 3. 交互式学习
- **节奏可控**：支持连续播放和单步执行，适应不同学习节奏
- **数据可变**：可生成不同数组观察算法表现
- **状态可查**：随时查看算法当前状态和统计信息

## 四、教学要点

### 核心概念理解要点

1. **间隔序列的重要性**
   - 观察初始间隔如何设置为数组长度的一半
   - 注意间隔如何逐次减半直至为1
   - 理解大间隔如何让元素"大跨度"移动

2. **子序列的形成与排序**
   - 注意每个间隔会形成多个独立的子序列
   - 观察子序列上的插入排序过程
   - 理解为什么子序列排序能提前减少逆序对

3. **效率优势的体现**
   - 比较希尔排序与普通插入排序的移动方式
   - 观察当间隔为1时，数组已基本有序的状态
   - 理解"基本有序"对最后一遍插入排序的加速作用

### 推荐观察顺序

1. **首次观看**：使用默认设置，点击"播放"完整观看算法全过程
2. **细节研究**：使用"下一步"单步执行，在关键步骤暂停思考
3. **对比观察**：生成不同数组，观察算法在不同数据上的表现
4. **参数实验**：调整数组大小，观察算法规模变化时的行为

## 五、使用建议

### 给初学者的建议

1. **先观后思**：先完整观看一遍动画，对算法流程建立整体印象
2. **关注颜色**：密切注意元素颜色的变化，这是理解状态转换的关键
3. **结合文字**：同时关注状态区的文字描述，将视觉与概念对应
4. **控制节奏**：在复杂步骤处使用单步执行，给自己充分的思考时间

### 给教师的教学建议

1. **概念引入**：先讲解插入排序的局限性，再引出希尔排序的改进思路
2. **动画演示**：使用本工具展示希尔排序的核心过程
3. **互动提问**：在关键步骤暂停，提问学生"下一步会发生什么？"
4. **对比分析**：引导学生观察比较次数和交换次数的变化规律
5. **拓展讨论**：讨论不同间隔序列（如Hibbard、Sedgewick序列）的影响

### 最佳实践流程

1. **预习阶段**：快速播放一遍，了解算法全貌
2. **学习阶段**：单步执行，每步思考"为什么这样做？"
3. **巩固阶段**：关闭动画，尝试自己描述算法过程
4. **应用阶段**：尝试手动对小数组执行希尔排序，验证理解

### 故障排除

- **动画卡顿**：降低动画速度或减少数组大小
- **理解困难**：使用单步模式，结合状态描述仔细分析
- **显示异常**：刷新页面重新开始

---

**祝您学习愉快！** 通过这个交互式工具，您不仅能看到希尔排序的"形"，更能理解其"神"——即如何通过巧妙的间隔设计，将简单的插入排序提升为高效的高级排序算法。如果在使用过程中有任何疑问或建议，欢迎记录并分享您的学习体验。

*教育技术专家 熊猫老师 设计制作*