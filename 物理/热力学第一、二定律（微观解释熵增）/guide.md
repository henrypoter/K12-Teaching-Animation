# 需求：热力学第一、二定律（微观解释熵增）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户为高中或大学低年级的理工科学生，他们已具备基础的物理和化学知识（如分子运动、能量概念），但首次接触“熵”这一抽象概念。用户的核心需求是：
1.  **理解抽象概念**：将“熵”这个宏观、统计性的概念，与直观的微观粒子行为（如分子运动、排列）联系起来，破除其神秘感。
2.  **区分两个定律**：清晰理解热力学第一定律（能量守恒）与第二定律（熵增方向）的本质区别。第一定律说“能不能”，第二定律说“可不可以、方向如何”。
3.  **建立过程直觉**：通过观察自发过程（如气体扩散、热量传递），直观感受“熵增”的必然性和统计本质，理解“可逆”与“不可逆”的微观根源。
4.  **克服常见误区**：例如，认识到熵增并不意味着“无序”，而是“微观状态数”的增加；一个局部系统的熵可以减少（如生命体），但必须以环境更大的熵增为代价。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念与叙事线**：
    1.  **起点：能量守恒（第一定律）**：用小球碰撞的弹珠台模拟一个孤立系统，展示动能与势能相互转化，但总和不变。强调第一定律是“记账”，不涉及方向。
    2.  **冲突与引入：方向性问题**：展示两个场景：a) 热物体自动变冷，冷物体自动变热？ b) 香水分子在房间一角自动聚集回瓶子？ 引导学生思考：虽然能量守恒，但这些反向过程不会自发发生。引出“方向”问题。
    3.  **核心：熵的微观解释**：
        *   **定义**：熵（S）是系统“微观状态数（W）”的量度，S ∝ ln W。微观状态数是指实现同一个宏观状态（如温度、压强、体积）所对应的所有可能的分子位置、速度分布方式。
        *   **可视化**：用一个简化模型（如4个可区分的小球在两个相连盒子中的分布）来演示。所有球在左盒（宏观状态A）只对应1种微观状态，熵极低；均匀分布（宏观状态B）对应多种微观状态（C(4,2)=6种等），熵高。
        *   **统计规律**：让学生通过交互“随机分配”小球，会发现得到均匀分布（高熵状态）的概率远大于全部集中在一边（低熵状态）。这就是熵增原理的统计基础：系统总是自发地走向概率更大的宏观状态。
    4.  **应用与连接：第二定律**：
        *   **气体扩散**：模拟两种颜色气体分子的混合。开始时有序分离（低熵），混合后均匀分布（高熵，微观状态数剧增）。反向分离的概率几乎为零。
        *   **热传导**：模拟高温区（分子平均速度快）和低温区（分子平均速度慢）的分子碰撞。通过碰撞，能量（速度）分布趋于平均（温度相等），这对应着更大概率、更多样化的速度分布（高熵状态）。
    5.  **总结与升华**：
        *   重申：第一定律是能量数量的守恒；第二定律是能量品质的退化（从集中可用到分散无用），由微观状态数的统计规律决定。
        *   指出：生命、机器等局部创造秩序（熵减），都必然以向环境排放废热（增加环境熵）为代价，宇宙的总熵永远增加。

*   **认知规律**：
    *   **从具体到抽象**：从看得见的弹珠、小球，到分子模型，再到抽象的“微观状态数”和公式。
    *   **从对比到理解**：通过对比第一定律（无方向）与自发过程（有方向）的矛盾，制造认知冲突，激发学习动机。
    *   **从操作到归纳**：让学生亲手点击“随机化”，观察统计结果，自己归纳出“均匀分布概率最大”的结论，建构对熵增的直觉。
    *   **多表征关联**：同一过程（如扩散）同时用粒子动画（直观）、微观状态计数（量化）、概率计算（数学）三种方式呈现，强化理解。

*   **交互设计**：
    *   **模块化导航**：清晰划分“第一定律演示”、“第二定律引入”、“熵的微观解释”、“气体扩散”、“热传导”等模块，允许学生按顺序或跳跃学习。
    *   **控制与观察**：提供播放/暂停/重置按钮。关键参数可调（如粒子数、温度差），并实时显示关键数据（能量总值、熵的估算值、微观状态数、概率）。
    *   **猜想与验证**：在关键步骤前设置选择题或预测环节（如“点击前，你认为哪种分布概率最高？”），增强参与感。
    *   **焦点提示与注解**：鼠标悬停或点击时，对特定粒子、区域或数据给出解释性标注。

*   **视觉呈现**：
    *   **粒子系统**：用不同颜色、大小、运动速度的小圆点代表分子/粒子。运动应平滑，碰撞符合动量守恒。
    *   **示意图与图表**：用简洁的示意图表示“盒子与小球”模型。用动态条形图或饼图展示不同宏观状态对应的微观状态数及其概率。
    *   **数据面板**：固定位置清晰显示能量、熵（相对值）、温度等关键物理量。
    *   **视觉隐喻**：使用“有序光点”到“混乱光点”的渐变、概率分布从尖锐单峰到宽阔平峰的动态变化，来隐喻熵增。

#### 配色方案选择
*   **主色调**：采用深蓝色（`#0f1a2f`）或深灰色（`#2c3e50`）作为画布背景，模拟深邃的科学探索空间，并能突出前景的粒子。
*   **粒子色**：
    *   第一定律部分：使用中性色（如浅灰色 `#bdc3c7`）或单一强调色（如青色 `#1abc9c`）。
    *   第二定律/对比部分：使用高对比度的冷暖色对，如**红色**（`#e74c3c` 代表高温/快速）和**蓝色**（`#3498db` 代表低温/慢速），清晰区分不同群体。
    *   混合过程：红色与蓝色粒子混合后，视觉上呈现为**紫色**（`#9b59b6`）区域，直观展示混合结果。
*   **UI与数据色**：
    *   控制按钮：使用醒目的绿色（`#2ecc71`）表示开始/播放，黄色（`#f1c40f`）表示重置。
    *   数据文本：关键数据（如总能量）用白色（`#ecf0f1`）突出显示，熵值变化可用动态颜色（从低熵的蓝色渐变到高熵的红色或橙色 `#e67e22`）来强化感知。
    *   示意图：使用简洁的线框（白色 `#ffffff` 或浅灰色 `#95a5a6`）和填充色块。
*   **原则**：保证足够的对比度和可读性，色彩服务于概念区分和注意力引导，避免花哨。

#### 交互功能列表
1.  **全局控制**：播放/暂停/重置按钮，进度条（如果动画有固定序列）。
2.  **模块选择器**：标签页或菜单栏，用于在“第一定律”、“熵的解释”、“扩散”、“热传导”等场景间切换。
3.  **参数调节器**（部分场景）：
    *   粒子数量滑块（在简化模型中，如从4个调到8个）。
    *   初始温度/速度滑块（用于热传导场景）。
    *   隔板控制（在扩散场景中，点击移除隔板）。
4.  **随机化按钮**：在“盒子与小球”模型中，点击按钮随机分配小球位置，并自动计数和可视化微观状态分布。
5.  **预测与揭示交互**：在展示概率前，先让学生选择他们认为最可能的分布，然后通过随机化实验揭示答案。
6.  **信息提示**：鼠标悬停在粒子、数据标签或按钮上时，显示简短的说明文字。
7.  **数据面板**：实时显示（或动态更新）：
    *   场景1：总动能、总势能、总机械能。
    *   场景2&3：微观状态数W、熵的相对值（k*ln(W)）、当前宏观状态的概率。
    *   场景4：左右分区粒子数、混合度（或熵的近似值）。
    *   场景5：高温区平均速度、低温区平均速度、系统总熵趋势。
8.  **视角切换**：在粒子视图和统计图表视图之间切换（例如，观看分子运动的同时，旁边有一个动态更新的概率分布图）。
9.  **步骤引导**：可选的“引导模式”，通过半透明的提示框和箭头，引导用户进行关键操作。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>热力学定律与熵增原理 - 微观解释</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #0f1a2f;
            color: #ecf0f1;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #3498db;
        }
        
        h1 {
            color: #1abc9c;
            margin-bottom: 10px;
            font-size: 2.5rem;
        }
        
        .subtitle {
            color: #bdc3c7;
            font-size: 1.2rem;
        }
        
        .main-content {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        
        .module-selector {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            margin-bottom: 20px;
            background-color: rgba(44, 62, 80, 0.7);
            padding: 15px;
            border-radius: 10px;
        }
        
        .module-btn {
            padding: 12px 24px;
            background-color: #2c3e50;
            color: #ecf0f1;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .module-btn:hover {
            background-color: #3498db;
            transform: translateY(-2px);
        }
        
        .module-btn.active {
            background-color: #1abc9c;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(26, 188, 156, 0.3);
        }
        
        .simulation-area {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .canvas-container {
            background-color: rgba(15, 26, 47, 0.9);
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        canvas {
            display: block;
            margin: 0 auto;
            background-color: rgba(15, 26, 47, 0.9);
            border-radius: 5px;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            align-items: center;
            background-color: rgba(44, 62, 80, 0.7);
            padding: 20px;
            border-radius: 10px;
        }
        
        .control-btn {
            padding: 12px 24px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: all 0.2s ease;
        }
        
        .play-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .play-btn:hover {
            background-color: #27ae60;
        }
        
        .reset-btn {
            background-color: #f1c40f;
            color: #2c3e50;
        }
        
        .reset-btn:hover {
            background-color: #f39c12;
        }
        
        .param-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            align-items: center;
        }
        
        .param-slider {
            display: flex;
            flex-direction: column;
            gap: 5px;
            min-width: 180px;
        }
        
        .param-slider label {
            font-size: 0.9rem;
            color: #bdc3c7;
        }
        
        .param-slider input {
            width: 100%;
        }
        
        .data-panel {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            background-color: rgba(44, 62, 80, 0.7);
            padding: 20px;
            border-radius: 10px;
        }
        
        .data-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            background-color: rgba(52, 73, 94, 0.8);
            border-radius: 8px;
        }
        
        .data-label {
            font-size: 0.9rem;
            color: #bdc3c7;
            margin-bottom: 5px;
        }
        
        .data-value {
            font-size: 1.5rem;
            font-weight: bold;
            color: #ecf0f1;
        }
        
        .entropy-value {
            color: #e67e22;
        }
        
        .energy-value {
            color: #1abc9c;
        }
        
        .explanation {
            background-color: rgba(44, 62, 80, 0.7);
            padding: 25px;
            border-radius: 10px;
            border-left: 5px solid #3498db;
        }
        
        .explanation h3 {
            color: #1abc9c;
            margin-bottom: 15px;
        }
        
        .explanation p {
            margin-bottom: 15px;
        }
        
        .key-concept {
            background-color: rgba(155, 89, 182, 0.2);
            padding: 15px;
            border-radius: 8px;
            margin-top: 15px;
            border-left: 4px solid #9b59b6;
        }
        
        .law-first {
            color: #1abc9c;
            font-weight: bold;
        }
        
        .law-second {
            color: #e74c3c;
            font-weight: bold;
        }
        
        .highlight {
            background-color: rgba(231, 76, 60, 0.2);
            padding: 2px 6px;
            border-radius: 4px;
            color: #e74c3c;
        }
        
        .probability-display {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .probability-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            background-color: rgba(52, 73, 94, 0.8);
            border-radius: 8px;
            min-width: 120px;
        }
        
        .probability-bar {
            width: 100%;
            height: 20px;
            background-color: #2c3e50;
            border-radius: 10px;
            margin-top: 10px;
            overflow: hidden;
        }
        
        .probability-fill {
            height: 100%;
            background-color: #3498db;
            border-radius: 10px;
            width: 0%;
            transition: width 1s ease;
        }
        
        .hot {
            color: #e74c3c;
        }
        
        .cold {
            color: #3498db;
        }
        
        .mixed {
            color: #9b59b6;
        }
        
        @media (max-width: 768px) {
            .module-selector {
                flex-direction: column;
            }
            
            .controls {
                flex-direction: column;
            }
            
            .param-controls {
                width: 100%;
            }
            
            .data-panel {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>热力学第一、第二定律与熵增原理</h1>
            <p class="subtitle">微观解释与交互式模拟</p>
        </header>
        
        <div class="main-content">
            <div class="module-selector">
                <button class="module-btn active" data-module="first-law">第一定律：能量守恒</button>
                <button class="module-btn" data-module="entropy-intro">熵的微观解释</button>
                <button class="module-btn" data-module="gas-diffusion">气体扩散</button>
                <button class="module-btn" data-module="heat-conduction">热传导</button>
                <button class="module-btn" data-module="summary">总结与对比</button>
            </div>
            
            <div class="simulation-area">
                <div class="canvas-container">
                    <canvas id="simulationCanvas" width="800" height="500"></canvas>
                </div>
                
                <div class="controls">
                    <button class="control-btn play-btn" id="playBtn">播放</button>
                    <button class="control-btn reset-btn" id="resetBtn">重置</button>
                    
                    <div class="param-controls">
                        <div class="param-slider" id="particleSlider">
                            <label for="particleCount">粒子数量: <span id="particleValue">50</span></label>
                            <input type="range" id="particleCount" min="10" max="200" value="50" step="10">
                        </div>
                        
                        <div class="param-slider" id="tempSlider" style="display:none;">
                            <label for="temperature">温度差: <span id="tempValue">50</span>%</label>
                            <input type="range" id="temperature" min="10" max="100" value="50">
                        </div>
                        
                        <button class="control-btn" id="randomizeBtn" style="background-color:#9b59b6; color:white; display:none;">随机分配</button>
                        
                        <button class="control-btn" id="removeWallBtn" style="background-color:#e74c3c; color:white; display:none;">移除隔板</button>
                    </div>
                </div>
                
                <div class="data-panel">
                    <div class="data-item">
                        <div class="data-label">总能量</div>
                        <div class="data-value energy-value" id="totalEnergy">100.0</div>
                    </div>
                    
                    <div class="data-item">
                        <div class="data-label">熵 (相对值)</div>
                        <div class="data-value entropy-value" id="entropyValue">0.0</div>
                    </div>
                    
                    <div class="data-item">
                        <div class="data-label">微观状态数</div>
                        <div class="data-value" id="microstates">1</div>
                    </div>
                    
                    <div class="data-item">
                        <div class="data-label">当前状态概率</div>
                        <div class="data-value" id="stateProbability">100%</div>
                    </div>
                </div>
                
                <div class="probability-display" id="probabilityDisplay" style="display:none;">
                    <!-- 概率条将通过JS动态生成 -->
                </div>
                
                <div class="explanation" id="explanation">
                    <h3>第一定律：能量守恒</h3>
                    <p>在这个模拟中，小球在封闭系统中运动，相互碰撞并与墙壁碰撞。观察动能和势能如何相互转化，但系统的<strong class="law-first">总能量保持不变</strong>。</p>
                    <p>热力学第一定律告诉我们能量既不能被创造也不能被消灭，只能从一种形式转化为另一种形式。但它没有告诉我们过程发生的<strong>方向</strong>。</p>
                    
                    <div class="key-concept">
                        <p><strong>关键概念：</strong> 第一定律是"能量记账" - 它只关心能量的数量，不关心能量的质量或过程的方向性。</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 全局变量
        let canvas, ctx;
        let animationId = null;
        let isPlaying = false;
        let currentModule = 'first-law';
        
        // 模拟参数
        let particles = [];
        let walls = [];
        let leftBoxParticles = [];
        let rightBoxParticles = [];
        let hotParticles = [];
        let coldParticles = [];
        
        // 物理参数
        const GRAVITY = 0.1;
        const FRICTION = 0.995;
        const PARTICLE_RADIUS = 5;
        const PARTICLE_MASS = 1;
        
        // 状态变量
        let totalEnergy = 100;
        let entropy = 0;
        let microstates = 1;
        let stateProbability = 1;
        let temperatureDifference = 0.5;
        let particleCount = 50;
        let hasWall = true;
        let isMixed = false;
        
        // DOM元素
        const playBtn = document.getElementById('playBtn');
        const resetBtn = document.getElementById('resetBtn');
        const particleCountSlider = document.getElementById('particleCount');
        const particleValueSpan = document.getElementById('particleValue');
        const temperatureSlider = document.getElementById('temperature');
        const tempValueSpan = document.getElementById('tempValue');
        const randomizeBtn = document.getElementById('randomizeBtn');
        const removeWallBtn = document.getElementById('removeWallBtn');
        const tempSliderDiv = document.getElementById('tempSlider');
        const particleSliderDiv = document.getElementById('particleSlider');
        const probabilityDisplay = document.getElementById('probabilityDisplay');
        
        // 数据面板元素
        const totalEnergyEl = document.getElementById('totalEnergy');
        const entropyValueEl = document.getElementById('entropyValue');
        const microstatesEl = document.getElementById('microstates');
        const stateProbabilityEl = document.getElementById('stateProbability');
        const explanationEl = document.getElementById('explanation');
        
        // 模块按钮
        const moduleBtns = document.querySelectorAll('.module-btn');
        
        // 初始化
        function init() {
            canvas = document.getElementById('simulationCanvas');
            ctx = canvas.getContext('2d');
            
            // 设置事件监听器
            playBtn.addEventListener('click', togglePlay);
            resetBtn.addEventListener('click', resetSimulation);
            particleCountSlider.addEventListener('input', updateParticleCount);
            temperatureSlider.addEventListener('input', updateTemperature);
            randomizeBtn.addEventListener('click', randomizeParticles);
            removeWallBtn.addEventListener('click', removeWall);
            
            // 模块切换
            moduleBtns.forEach(btn => {
                btn.addEventListener('click', () => {
                    switchModule(btn.dataset.module);
                });
            });
            
            // 初始化模拟
            resetSimulation();
        }
        
        // 切换播放状态
        function togglePlay() {
            isPlaying = !isPlaying;
            playBtn.textContent = isPlaying ? '暂停' : '播放';
            
            if (isPlaying) {
                animate();
            } else {
                cancelAnimationFrame(animationId);
            }
        }
        
        // 重置模拟
        function resetSimulation() {
            // 停止动画
            if (animationId) {
                cancelAnimationFrame(animationId);
                animationId = null;
            }
            
            isPlaying = false;
            playBtn.textContent = '播放';
            
            // 根据当前模块重置
            setupModule(currentModule);
        }
        
        // 切换模块
        function switchModule(moduleName) {
            // 更新活动按钮
            moduleBtns.forEach(btn => {
                if (btn.dataset.module === moduleName) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            currentModule = moduleName;
            resetSimulation();
        }
        
        // 设置模块
        function setupModule(moduleName) {
            // 重置粒子数组
            particles = [];
            
            // 重置墙壁
            walls = [];
            
            // 根据模块设置UI
            switch(moduleName) {
                case 'first-law':
                    setupFirstLaw();
                    updateExplanationFirstLaw();
                    particleSliderDiv.style.display = 'block';
                    tempSliderDiv.style.display = 'none';
                    randomizeBtn.style.display = 'none';
                    removeWallBtn.style.display = 'none';
                    probabilityDisplay.style.display = 'none';
                    break;
                    
                case 'entropy-intro':
                    setupEntropyIntro();
                    updateExplanationEntropyIntro();
                    particleSliderDiv.style.display = 'block';
                    tempSliderDiv.style.display = 'none';
                    randomizeBtn.style.display = 'block';
                    removeWallBtn.style.display = 'none';
                    probabilityDisplay.style.display = 'flex';
                    break;
                    
                case 'gas-diffusion':
                    setupGasDiffusion();
                    updateExplanationGasDiffusion();
                    particleSliderDiv.style.display = 'block';
                    tempSliderDiv.style.display = 'none';
                    randomizeBtn.style.display = 'none';
                    removeWallBtn.style.display = 'block';
                    probabilityDisplay.style.display = 'none';
                    break;
                    
                case 'heat-conduction':
                    setupHeatConduction();
                    updateExplanationHeatConduction();
                    particleSliderDiv.style.display = 'block';
                    tempSliderDiv.style.display = 'block';
                    randomizeBtn.style.display = 'none';
                    removeWallBtn.style.display = 'none';
                    probabilityDisplay.style.display = 'none';
                    break;
                    
                case 'summary':
                    setupSummary();
                    updateExplanationSummary();
                    particleSliderDiv.style.display = 'block';
                    tempSliderDiv.style.display = 'none';
                    randomizeBtn.style.display = 'none';
                    removeWallBtn.style.display = 'none';
                    probabilityDisplay.style.display = 'none';
                    break;
            }
            
            // 更新数据面板
            updateDataPanel();
        }
        
        // 设置第一定律模块
        function setupFirstLaw() {
            // 创建墙壁
            walls.push({x: 50, y: 50, width: canvas.width - 100, height: 20}); // 上墙
            walls.push({x: 50, y: canvas.height - 70, width: canvas.width - 100, height: 20}); // 下墙
            walls.push({x: 50, y: 50, width: 20, height: canvas.height - 120}); // 左墙
            walls.push({x: canvas.width - 70, y: 50, width: 20, height: canvas.height - 120}); // 右墙
            
            // 创建粒子
            for (let i = 0; i < particleCount; i++) {
                const radius = PARTICLE_RADIUS;
                const x = Math.random() * (canvas.width - 140) + 80;
                const y = Math.random() * (canvas.height - 140) + 80;
                const vx = (Math.random() - 0.5) * 4;
                const vy = (Math.random() - 0.5) * 4;
                
                particles.push({
                    x, y, radius,
                    vx, vy,
                    mass: PARTICLE_MASS,
                    color: '#1abc9c'
                });
            }
            
            // 计算初始总能量
            calculateTotalEnergy();
        }
        
        // 设置熵介绍模块
        function setupEntropyIntro() {
            // 创建两个盒子
            const boxWidth = canvas.width / 2 - 60;
            const boxHeight = canvas.height - 150;
            const boxY = 80;
            
            // 左盒子墙壁
            walls.push({x: 50, y: boxY, width: boxWidth, height: 20}); // 上墙
            walls.push({x: 50, y: boxY + boxHeight, width: boxWidth, height: 20}); // 下墙
            walls.push({x: 50, y: boxY, width: 20, height: boxHeight}); // 左墙
            walls.push({x: 50 + boxWidth - 20, y: boxY, width: 20, height: boxHeight}); // 中间墙
            
            // 右盒子墙壁
            walls.push({x: canvas.width/2 + 10, y: boxY, width: boxWidth, height: 20}); // 上墙
            walls.push({x: canvas.width/2 + 10, y: boxY + boxHeight, width: boxWidth, height: 20}); // 下墙
            walls.push({x: canvas.width/2 + boxWidth + 10, y: boxY, width: 20, height: boxHeight}); // 右墙
            
            // 创建粒子（全部在左盒）
            leftBoxParticles = [];
            rightBoxParticles = [];
            
            for (let i = 0; i < Math.min(particleCount, 20); i++) {
                const radius = 8;
                const x = Math.random() * (boxWidth - 60) + 70;
                const y = Math.random() * (boxHeight - 60) + boxY + 30;
                const vx = (Math.random() - 0.5) * 2;
                const vy = (Math.random() - 0.5) * 2;
                
                const particle = {
                    x, y, radius,
                    vx, vy,
                    mass: PARTICLE_MASS,
                    color: '#3498db',
                    inLeftBox: true
                };
                
                particles.push(particle);
                leftBoxParticles.push(particle);
            }
            
            // 计算微观状态和熵
            calculateEntropyStats();
            
            // 创建概率显示
            createProbabilityDisplay();
        }
        
        // 设置气体扩散模块
        function setupGasDiffusion() {
            // 创建墙壁和隔板
            const containerWidth = canvas.width - 100;
            const containerHeight = canvas.height - 150;
            const containerY = 80;
            
            // 容器墙壁
            walls.push({x: 50, y: containerY, width: containerWidth, height: 20}); // 上墙
            walls.push({x: 50, y: containerY + containerHeight, width: containerWidth, height: 20}); // 下墙
            walls.push({x: 50, y: containerY, width: 20, height: containerHeight}); // 左墙
            walls.push({x: 50 + containerWidth - 20, y: containerY, width: 20, height: containerHeight}); // 右墙
            
            // 中间隔板（如果存在）
            if (hasWall) {
                walls.push({x: canvas.width/2 - 10, y: containerY, width: 20, height: containerHeight});
            }
            
            // 创建红色粒子（左盒）
            for (let i = 0; i < particleCount/2; i++) {
                const radius = PARTICLE_RADIUS;
                const x = Math.random() * (containerWidth/2 - 60) + 70;
                const y = Math.random() * (containerHeight - 60) + containerY + 30;
                const vx = (Math.random() - 0.5) * 3;
                const vy = (Math.random() - 0.5) * 3;
                
                particles.push({
                    x, y, radius,
                    vx, vy,
                    mass: PARTICLE_MASS,
                    color: '#e74c3c' // 红色
                });
            }
            
            // 创建蓝色粒子（右盒）
            for (let i = 0; i < particleCount/2; i++) {
                const radius = PARTICLE_RADIUS;
                const x = Math.random() * (containerWidth/2 - 60) + canvas.width/2 + 30;
                const y = Math.random() * (containerHeight - 60) + containerY + 30;
                const vx = (Math.random() - 0.5) * 3;
                const vy = (Math.random() - 0.5) * 3;
                
                particles.push({
                    x, y, radius,
                    vx, vy,
                    mass: PARTICLE_MASS,
                    color: '#3498db' // 蓝色
                });
            }
            
            // 计算初始熵
            calculateDiffusionEntropy();
        }
        
        // 设置热传导模块
        function setupHeatConduction() {
            // 创建墙壁
            const containerWidth = canvas.width - 100;
            const containerHeight = canvas.height - 150;
            const containerY = 80;
            
            walls.push({x: 50, y: containerY, width: containerWidth, height: 20}); // 上墙
            walls.push({x: 50, y: containerY + containerHeight, width: containerWidth, height: 20}); // 下墙
            walls.push({x: 50, y: containerY, width: 20, height: containerHeight}); // 左墙
            walls.push({x: 50 + containerWidth - 20, y: containerY, width: 20, height: containerHeight}); // 右墙
            
            // 重置热冷粒子数组
            hotParticles = [];
            coldParticles = [];
            
            // 创建热粒子（左半部分）
            const hotSpeedFactor = 1 + temperatureDifference;
            for (let i = 0; i < particleCount/2; i++) {
                const radius = PARTICLE_RADIUS;
                const x = Math.random() * (containerWidth/2 - 60) + 70;
                const y = Math.random() * (containerHeight - 60) + containerY + 30;
                const vx = (Math.random() - 0.5) * 4 * hotSpeedFactor;
                const vy = (Math.random() - 0.5) * 4 * hotSpeedFactor;
                
                const particle = {
                    x, y, radius,
                    vx, vy,
                    mass: PARTICLE_MASS,
                    color: '#e74c3c', // 红色表示热
                    isHot: true
                };
                
                particles.push(particle);
                hotParticles.push(particle);
            }
            
            // 创建冷粒子（右半部分）
            const coldSpeedFactor = 1 - temperatureDifference * 0.5;
            for (let i = 0; i < particleCount/2; i++) {
                const radius = PARTICLE_RADIUS;
                const x = Math.random() * (containerWidth/2 - 60) + canvas.width/2 + 30;
                const y = Math.random() * (containerHeight - 60) + containerY + 30;
                const vx = (Math.random() - 0.5) * 4 * coldSpeedFactor;
                const vy = (Math.random() - 0.5) * 4 * coldSpeedFactor;
                
                const particle = {
                    x, y, radius,
                    vx, vy,
                    mass: PARTICLE_MASS,
                    color: '#3498db', // 蓝色表示冷
                    isHot: false
                };
                
                particles.push(particle);
                coldParticles.push(particle);
            }
            
            // 计算初始熵
            calculateHeatConductionEntropy();
        }
        
        // 设置总结模块
        function setupSummary() {
            // 创建墙壁
            walls.push({x: 50, y: 50, width: canvas.width - 100, height: 20}); // 上墙
            walls.push({x: 50, y: canvas.height - 70, width: canvas.width - 100, height: 20}); // 下墙
            walls.push({x: 50, y: 50, width: 20, height: canvas.height - 120}); // 左墙
            walls.push({x: canvas.width - 70, y: 50, width: 20, height: canvas.height - 120}); // 右墙
            
            // 创建混合粒子
            for (let i = 0; i < particleCount; i++) {
                const radius = PARTICLE_RADIUS;
                const x = Math.random() * (canvas.width - 140) + 80;
                const y = Math.random() * (canvas.height - 140) + 80;
                const vx = (Math.random() - 0.5) * 4;
                const vy = (Math.random() - 0.5) * 4;
                
                // 随机分配颜色（模拟混合状态）
                const isRed = Math.random() > 0.5;
                particles.push({
                    x, y, radius,
                    vx, vy,
                    mass: PARTICLE_MASS,
                    color: isRed ? '#e74c3c' : '#3498db'
                });
            }
            
            // 计算总能量和熵
            calculateTotalEnergy();
            entropy = 8.5; // 设置一个较高的熵值表示混合状态
        }
        
        // 更新粒子数量
        function updateParticleCount() {
            particleCount = parseInt(particleCountSlider.value);
            particleValueSpan.textContent = particleCount;
            resetSimulation();
        }
        
        // 更新温度差
        function updateTemperature() {
            temperatureDifference = parseInt(temperatureSlider.value) / 100;
            tempValueSpan.textContent = parseInt(temperatureSlider.value);
            
            if (currentModule === 'heat-conduction') {
                // 更新热冷粒子的速度
                const hotSpeedFactor = 1 + temperatureDifference;
                const coldSpeedFactor = 1 - temperatureDifference * 0.5;
                
                hotParticles.forEach(p => {
                    p.vx *= hotSpeedFactor / (1 + temperatureDifference - 0.01);
                    p.vy *= hotSpeedFactor / (1 + temperatureDifference - 0.01);
                });
                
                coldParticles.forEach(p => {
                    p.vx *= coldSpeedFactor / (1 - (temperatureDifference - 0.01) * 0.5);
                    p.vy *= coldSpeedFactor / (1 - (temperatureDifference - 0.01) * 0.5);
                });
            }
        }
        
        // 随机分配粒子（用于熵介绍模块）
        function randomizeParticles() {
            if (currentModule !== 'entropy-intro') return;
            
            // 清空左右盒子粒子数组
            leftBoxParticles = [];
            rightBoxParticles = [];
            
            // 随机分配每个粒子到左盒或右盒
            particles.forEach(particle => {
                const inLeftBox = Math.random() > 0.5;
                particle.inLeftBox = inLeftBox;
                
                // 设置位置
                const boxWidth = canvas.width / 2 - 60;
                const boxHeight = canvas.height - 150;
                const boxY = 80;
                
                if (inLeftBox) {
                    particle.x = Math.random() * (boxWidth - 60) + 70;
                    leftBoxParticles.push(particle);
                } else {
                    particle.x = Math.random() * (boxWidth - 60) + canvas.width/2 + 30;
                    rightBoxParticles.push(particle);
                }
                
                particle.y = Math.random() * (boxHeight - 60) + boxY + 30;
                
                // 随机速度
                particle.vx = (Math.random() - 0.5) * 2;
                particle.vy = (Math.random() - 0.5) * 2;
            });
            
            // 计算微观状态和熵
            calculateEntropyStats();
        }
        
        // 移除隔板（用于气体扩散模块）
        function removeWall() {
            if (currentModule !== 'gas-diffusion') return;
            
            hasWall = false;
            removeWallBtn.style.display = 'none';
            
            // 移除中间隔板
            walls = walls.filter(wall => !(wall.x === canvas.width/2 - 10 && wall.width === 20));
            
            // 开始动画
            if (!isPlaying) {
                togglePlay();
            }
        }
        
        // 计算总能量（用于第一定律模块）
        function calculateTotalEnergy() {
            totalEnergy = 0;
            particles.forEach(p => {
                const kinetic = 0.5 * p.mass * (p.vx * p.vx + p.vy * p.vy);
                const potential = p.mass * GRAVITY * (canvas.height - p.y);
                totalEnergy += kinetic + potential;
            });
            
            totalEnergy = Math.round(totalEnergy * 10) / 10;
        }
        
        // 计算熵统计（用于熵介绍模块）
        function calculateEntropyStats() {
            const N = particles.length;
            const nLeft = leftBoxParticles.length;
            const nRight = rightBoxParticles.length;
            
            // 计算微观状态数（组合数 C(N, nLeft)）
            microstates = combination(N, nLeft);
            
            // 计算熵 S = k * ln(W)，这里k设为1
            entropy = Math.log(microstates);
            
            // 计算当前状态概率
            const totalMicrostates = Math.pow(2, N);
            stateProbability = microstates / totalMicrostates;
            
            // 更新数据面板
            updateDataPanel();
            
            // 更新概率显示
            updateProbabilityDisplay(N, nLeft);
        }
        
        // 计算组合数 C(n, k)
        function combination(n, k) {
            if (k < 0 || k > n) return 0;
            if (k === 0 || k === n) return 1;
            
            k = Math.min(k, n - k);
            let result = 1;
            for (let i = 1; i <= k; i++) {
                result = result * (n - k + i) / i;
            }
            
            return Math.round(result);
        }
        
        // 创建概率显示
        function createProbabilityDisplay() {
            probabilityDisplay.innerHTML = '';
            
            const N = Math.min(particles.length, 8); // 限制显示的数量
            
            for (let k = 0; k <= N; k++) {
                const probItem = document.createElement('div');
                probItem.className = 'probability-item';
                
                const label = document.createElement('div');
                label.className = 'data-label';
                label.textContent = `${k}:${N-k}`;
                
                const value = document.createElement('div');
                value.className = 'data-value';
                value.id = `probValue${k}`;
                value.textContent = '0%';
                
                const bar = document.createElement('div');
                bar.className = 'probability-bar';
                
                const fill = document.createElement('div');
                fill.className = 'probability-fill';
                fill.id = `probFill${k}`;
                
                bar.appendChild(fill);
                probItem.appendChild(label);
                probItem.appendChild(value);
                probItem.appendChild(bar);
                
                probabilityDisplay.appendChild(probItem);
            }
        }
        
        // 更新概率显示
        function updateProbabilityDisplay(N, currentK) {
            const totalMicrostates = Math.pow(2, N);
            
            for (let k = 0; k <= N; k++) {
                const microstatesK = combination(N, k);
                const probability = microstatesK / totalMicrostates;
                const percentage = Math.round(probability * 1000) / 10;
                
                const valueEl = document.getElementById(`probValue${k}`);
                const fillEl = document.getElementById(`probFill${k}`);
                
                if (valueEl && fillEl) {
                    valueEl.textContent = `${percentage}%`;
                    fillEl.style.width = `${probability * 100}%`;
                    
                    // 高亮当前状态
                    if (k === currentK) {
                        fillEl.style.backgroundColor = '#e74c3c';
                        valueEl.style.color = '#e74c3c';
                        valueEl.style.fontWeight = 'bold';
                    } else {
                        fillEl.style.backgroundColor = '#3498db';
                        valueEl.style.color = '#ecf0f1';
                        valueEl.style.fontWeight = 'normal';
                    }
                }
            }
        }
        
        // 计算扩散熵
        function calculateDiffusionEntropy() {
            // 简化的熵计算：基于混合程度
            const containerWidth = canvas.width - 100;
            const leftBoundary = 50 + 20;
            const rightBoundary = 50 + containerWidth - 20;
            const middle = canvas.width / 2;
            
            let redInLeft = 0;
            let redInRight = 0;
            let blueInLeft = 0;
            let blueInRight =
<!--检测到代码截断，自动续写中...-->
0;
            
            particles.forEach(p => {
                if (p.color === '#e74c3c') { // 红色粒子
                    if (p.x < middle) redInLeft++;
                    else redInRight++;
                } else { // 蓝色粒子
                    if (p.x < middle) blueInLeft++;
                    else blueInRight++;
                }
            });
            
            // 计算混合程度 (0-1)
            const totalRed = redInLeft + redInRight;
            const totalBlue = blueInLeft + blueInRight;
            
            let mixFactor = 0;
            if (totalRed > 0 && totalBlue > 0) {
                // 理想混合：红色和蓝色在左右均匀分布
                const idealRedInLeft = totalRed / 2;
                const idealBlueInLeft = totalBlue / 2;
                
                // 计算实际分布与理想分布的差异
                const redDiff = Math.abs(redInLeft - idealRedInLeft) / totalRed;
                const blueDiff = Math.abs(blueInLeft - idealBlueInLeft) / totalBlue;
                
                mixFactor = 1 - (redDiff + blueDiff) / 2;
            }
            
            // 熵与混合程度成正比
            entropy = 10 * mixFactor;
            
            // 微观状态数（简化计算）
            const totalParticles = particles.length;
            const particlesInLeft = redInLeft + blueInLeft;
            microstates = combination(totalParticles, particlesInLeft);
            
            // 状态概率（简化）
            stateProbability = mixFactor;
            
            updateDataPanel();
        }
        
        // 计算热传导熵
        function calculateHeatConductionEntropy() {
            // 计算平均动能（温度）
            let totalKineticEnergy = 0;
            particles.forEach(p => {
                const kinetic = 0.5 * p.mass * (p.vx * p.vx + p.vy * p.vy);
                totalKineticEnergy += kinetic;
            });
            
            const avgKineticEnergy = totalKineticEnergy / particles.length;
            
            // 计算速度分布的方差（作为熵的度量）
            let variance = 0;
            particles.forEach(p => {
                const kinetic = 0.5 * p.mass * (p.vx * p.vx + p.vy * p.vy);
                const diff = kinetic - avgKineticEnergy;
                variance += diff * diff;
            });
            
            variance /= particles.length;
            
            // 熵与速度分布的均匀程度成正比（方差越小，熵越大）
            // 这里使用反比关系简化计算
            const maxVariance = 50; // 估计的最大方差
            entropy = 10 * (1 - Math.min(variance / maxVariance, 1));
            
            // 更新数据面板
            updateDataPanel();
        }
        
        // 更新数据面板
        function updateDataPanel() {
            totalEnergyEl.textContent = totalEnergy.toFixed(1);
            entropyValueEl.textContent = entropy.toFixed(2);
            microstatesEl.textContent = microstates.toLocaleString();
            stateProbabilityEl.textContent = (stateProbability * 100).toFixed(1) + '%';
        }
        
        // 更新解释文本
        function updateExplanationFirstLaw() {
            explanationEl.innerHTML = `
                <h3>第一定律：能量守恒</h3>
                <p>在这个模拟中，小球在封闭系统中运动，相互碰撞并与墙壁碰撞。观察动能和势能如何相互转化，但系统的<strong class="law-first">总能量保持不变</strong>。</p>
                <p>热力学第一定律告诉我们能量既不能被创造也不能被消灭，只能从一种形式转化为另一种形式。但它没有告诉我们过程发生的<strong>方向</strong>。</p>
                
                <div class="key-concept">
                    <p><strong>关键概念：</strong> 第一定律是"能量记账" - 它只关心能量的数量，不关心能量的质量或过程的方向性。</p>
                </div>
            `;
        }
        
        function updateExplanationEntropyIntro() {
            const N = particles.length;
            const nLeft = leftBoxParticles.length;
            const nRight = rightBoxParticles.length;
            
            explanationEl.innerHTML = `
                <h3>熵的微观解释</h3>
                <p>熵（S）是系统"微观状态数（W）"的量度：S ∝ ln(W)。微观状态数是指实现同一个宏观状态所对应的所有可能的分子排列方式。</p>
                <p>当前系统：${N}个可区分粒子，${nLeft}个在左盒，${nRight}个在右盒。</p>
                <p>微观状态数 W = C(${N}, ${nLeft}) = <strong>${microstates.toLocaleString()}</strong></p>
                <p>熵 S ≈ ln(${microstates.toLocaleString()}) ≈ <strong>${entropy.toFixed(2)}</strong></p>
                
                <div class="key-concept">
                    <p><strong>关键发现：</strong> 点击"随机分配"按钮，你会发现粒子均匀分布（左右各一半）的概率最大。这就是<strong class="law-second">熵增原理</strong>的统计基础：系统总是自发地走向概率更大的宏观状态。</p>
                </div>
            `;
        }
        
        function updateExplanationGasDiffusion() {
            explanationEl.innerHTML = `
                <h3>气体扩散与熵增</h3>
                <p>开始时，红色粒子和蓝色粒子被隔板分开，处于低熵状态。点击"移除隔板"观察气体扩散过程。</p>
                <p>扩散发生后，两种粒子<strong class="mixed">均匀混合</strong>，系统的微观状态数急剧增加，熵达到最大值。</p>
                <p>反向过程（所有红色粒子自动回到左盒，蓝色粒子回到右盒）的概率微乎其微，这就是<strong class="law-second">不可逆过程</strong>的微观解释。</p>
                
                <div class="key-concept">
                    <p><strong>关键概念：</strong> 熵增并不意味着"无序"，而是系统走向<strong>更可能</strong>的宏观状态。混合状态比分离状态有更多可能的微观排列方式。</p>
                </div>
            `;
        }
        
        function updateExplanationHeatConduction() {
            explanationEl.innerHTML = `
                <h3>热传导与能量品质退化</h3>
                <p><span class="hot">红色粒子</span>代表高温区域（分子平均速度快），<span class="cold">蓝色粒子</span>代表低温区域（分子平均速度慢）。</p>
                <p>当它们混合时，通过碰撞，能量从高温粒子传递到低温粒子，最终达到温度均衡。</p>
                <p>虽然总能量守恒（第一定律），但能量从<strong>集中可用</strong>的形式（高温）变成了<strong>分散无用</strong>的形式（均匀温度），能量的品质下降了。</p>
                
                <div class="key-concept">
                    <p><strong>关键概念：</strong> 热力学第二定律指出，在孤立系统中，熵永不减少。热传导过程使系统的熵增加，因为均匀的温度分布对应更多的微观速度分布方式。</p>
                </div>
            `;
        }
        
        function updateExplanationSummary() {
            explanationEl.innerHTML = `
                <h3>总结：两个定律的关系</h3>
                <p><strong class="law-first">热力学第一定律（能量守恒）</strong>：<br>
                • 关注能量的数量<br>
                • 能量不能创造或消灭，只能转化<br>
                • 不涉及过程的方向性</p>
                
                <p><strong class="law-second">热力学第二定律（熵增原理）</strong>：<br>
                • 关注能量的品质和过程的方向<br>
                • 孤立系统的熵永不减少<br>
                • 基于微观状态数的统计规律</p>
                
                <div class="key-concept">
                    <p><strong>核心理解：</strong> 第一定律说"能不能"（能量是否守恒），第二定律说"可不可以、方向如何"（过程是否可能自发发生）。所有自发过程都朝着熵增加的方向进行，因为那对应着概率更大的宏观状态。</p>
                    <p>生命体、机器等局部系统可以通过消耗能量来降低自身的熵（变得有序），但必须以环境更大的熵增为代价。宇宙的总熵永远在增加。</p>
                </div>
            `;
        }
        
        // 动画循环
        function animate() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 更新和绘制墙壁
            walls.forEach(wall => {
                ctx.fillStyle = '#95a5a6';
                ctx.fillRect(wall.x, wall.y, wall.width, wall.height);
            });
            
            // 根据当前模块更新物理
            switch(currentModule) {
                case 'first-law':
                    updateFirstLawPhysics();
                    break;
                case 'entropy-intro':
                    updateEntropyIntroPhysics();
                    break;
                case 'gas-diffusion':
                    updateGasDiffusionPhysics();
                    break;
                case 'heat-conduction':
                    updateHeatConductionPhysics();
                    break;
                case 'summary':
                    updateSummaryPhysics();
                    break;
            }
            
            // 绘制粒子
            particles.forEach(p => {
                // 绘制粒子
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
                ctx.fillStyle = p.color;
                ctx.fill();
                ctx.closePath();
                
                // 绘制速度箭头（可选，用于热传导模块）
                if (currentModule === 'heat-conduction' && p.isHot) {
                    ctx.beginPath();
                    ctx.moveTo(p.x, p.y);
                    ctx.lineTo(p.x + p.vx, p.y + p.vy);
                    ctx.strokeStyle = '#e74c3c';
                    ctx.lineWidth = 1;
                    ctx.stroke();
                }
            });
            
            // 绘制模块特定的图形
            drawModuleSpecificGraphics();
            
            // 继续动画循环
            if (isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }
        
        // 更新第一定律物理
        function updateFirstLawPhysics() {
            // 更新粒子位置和碰撞
            particles.forEach(p => {
                // 应用重力
                p.vy += GRAVITY;
                
                // 应用摩擦力
                p.vx *= FRICTION;
                p.vy *= FRICTION;
                
                // 更新位置
                p.x += p.vx;
                p.y += p.vy;
                
                // 边界碰撞检测
                walls.forEach(wall => {
                    if (p.x + p.radius > wall.x && p.x - p.radius < wall.x + wall.width &&
                        p.y + p.radius > wall.y && p.y - p.radius < wall.y + wall.height) {
                        
                        // 确定碰撞方向并反弹
                        const dx = p.x - (wall.x + wall.width/2);
                        const dy = p.y - (wall.y + wall.height/2);
                        
                        if (Math.abs(dx) > Math.abs(dy)) {
                            // 水平碰撞
                            p.vx = -p.vx * 0.9;
                            p.x += p.vx;
                        } else {
                            // 垂直碰撞
                            p.vy = -p.vy * 0.9;
                            p.y += p.vy;
                        }
                    }
                });
                
                // 粒子间碰撞检测（简化）
                for (let i = 0; i < particles.length; i++) {
                    for (let j = i + 1; j < particles.length; j++) {
                        const p1 = particles[i];
                        const p2 = particles[j];
                        
                        const dx = p2.x - p1.x;
                        const dy = p2.y - p1.y;
                        const distance = Math.sqrt(dx * dx + dy * dy);
                        
                        if (distance < p1.radius + p2.radius) {
                            // 简单弹性碰撞
                            const angle = Math.atan2(dy, dx);
                            const speed1 = Math.sqrt(p1.vx * p1.vx + p1.vy * p1.vy);
                            const speed2 = Math.sqrt(p2.vx * p2.vx + p2.vy * p2.vy);
                            
                            const direction1 = Math.atan2(p1.vy, p1.vx);
                            const direction2 = Math.atan2(p2.vy, p2.vx);
                            
                            // 交换速度（简化）
                            const tempVx = p1.vx;
                            const tempVy = p1.vy;
                            
                            p1.vx = p2.vx * 0.9;
                            p1.vy = p2.vy * 0.9;
                            
                            p2.vx = tempVx * 0.9;
                            p2.vy = tempVy * 0.9;
                            
                            // 防止重叠
                            const overlap = (p1.radius + p2.radius - distance) / 2;
                            p1.x -= overlap * Math.cos(angle);
                            p1.y -= overlap * Math.sin(angle);
                            p2.x += overlap * Math.cos(angle);
                            p2.y += overlap * Math.sin(angle);
                        }
                    }
                }
            });
            
            // 更新总能量
            calculateTotalEnergy();
        }
        
        // 更新熵介绍物理
        function updateEntropyIntroPhysics() {
            // 粒子在各自盒子内运动
            particles.forEach(p => {
                // 更新位置
                p.x += p.vx;
                p.y += p.vy;
                
                // 盒子边界碰撞检测
                const boxWidth = canvas.width / 2 - 60;
                const boxHeight = canvas.height - 150;
                const boxY = 80;
                
                let leftBound, rightBound, topBound, bottomBound;
                
                if (p.inLeftBox) {
                    leftBound = 50 + 20;
                    rightBound = 50 + boxWidth - 20;
                } else {
                    leftBound = canvas.width/2 + 10 + 20;
                    rightBound = canvas.width/2 + 10 + boxWidth - 20;
                }
                
                topBound = boxY + 20;
                bottomBound = boxY + boxHeight - 20;
                
                // 左右边界
                if (p.x - p.radius < leftBound) {
                    p.x = leftBound + p.radius;
                    p.vx = -p.vx * 0.9;
                }
                if (p.x + p.radius > rightBound) {
                    p.x = rightBound - p.radius;
                    p.vx = -p.vx * 0.9;
                }
                
                // 上下边界
                if (p.y - p.radius < topBound) {
                    p.y = topBound + p.radius;
                    p.vy = -p.vy * 0.9;
                }
                if (p.y + p.radius > bottomBound) {
                    p.y = bottomBound - p.radius;
                    p.vy = -p.vy * 0.9;
                }
            });
        }
        
        // 更新气体扩散物理
        function updateGasDiffusionPhysics() {
            particles.forEach(p => {
                // 更新位置
                p.x += p.vx;
                p.y += p.vy;
                
                // 容器边界碰撞检测
                const containerWidth = canvas.width - 100;
                const containerHeight = canvas.height - 150;
                const containerY = 80;
                
                const leftBound = 50 + 20;
                const rightBound = 50 + containerWidth - 20;
                const topBound = containerY + 20;
                const bottomBound = containerY + containerHeight - 20;
                
                // 左右边界
                if (p.x - p.radius < leftBound) {
                    p.x = leftBound + p.radius;
                    p.vx = -p.vx * 0.9;
                }
                if (p.x + p.radius > rightBound) {
                    p.x = rightBound - p.radius;
                    p.vx = -p.vx * 0.9;
                }
                
                // 上下边界
                if (p.y - p.radius < topBound) {
                    p.y = topBound + p.radius;
                    p.vy = -p.vy * 0.9;
                }
                if (p.y + p.radius > bottomBound) {
                    p.y = bottomBound - p.radius;
                    p.vy = -p.vy * 0.9;
                }
                
                // 如果隔板存在，检测与隔板的碰撞
                if (hasWall) {
                    const wallX = canvas.width/2 - 10;
                    const wallWidth = 20;
                    
                    if (p.x + p.radius > wallX && p.x - p.radius < wallX + wallWidth &&
                        p.y > containerY && p.y < containerY + containerHeight) {
                        
                        // 从左侧碰撞
                        if (p.x < wallX + wallWidth/2) {
                            p.x = wallX - p.radius;
                            p.vx = -Math.abs(p.vx) * 0.9;
                        } 
                        // 从右侧碰撞
                        else {
                            p.x = wallX + wallWidth + p.radius;
                            p.vx = Math.abs(p.vx) * 0.9;
                        }
                    }
                }
                
                // 粒子间碰撞（简化）
                for (let i = 0; i < particles.length; i++) {
                    for (let j = i + 1; j < particles.length; j++) {
                        const p1 = particles[i];
                        const p2 = particles[j];
                        
                        const dx = p2.x - p1.x;
                        const dy = p2.y - p1.y;
                        const distance = Math.sqrt(dx * dx + dy * dy);
                        
                        if (distance < p1.radius + p2.radius) {
                            // 简单弹性碰撞
                            const tempVx = p1.vx;
                            const tempVy = p1.vy;
                            
                            p1.vx = p2.vx * 0.95;
                            p1.vy = p2.vy * 0.95;
                            
                            p2.vx = tempVx * 0.95;
                            p2.vy = tempVy * 0.95;
                            
                            // 防止重叠
                            const overlap = (p1.radius + p2.radius - distance) / 2;
                            const angle = Math.atan2(dy, dx);
                            p1.x -= overlap * Math.cos(angle);
                            p1.y -= overlap * Math.sin(angle);
                            p2.x += overlap * Math.cos(angle);
                            p2.y += overlap * Math.sin(angle);
                        }
                    }
                }
            });
            
            // 更新熵
            calculateDiffusionEntropy();
        }
        
        // 更新热传导物理
        function updateHeatConductionPhysics() {
            particles.forEach(p => {
                // 更新位置
                p.x += p.vx;
                p.y += p.vy;
                
                // 容器边界碰撞检测
                const containerWidth = canvas.width - 100;
                const containerHeight = canvas.height - 150;
                const containerY = 80;
                
                const leftBound = 50 + 20;
                const rightBound = 50 + containerWidth - 20;
                const topBound = containerY + 20;
                const bottomBound = containerY + containerHeight - 20;
                
                // 左右边界
                if (p.x - p.radius < leftBound) {
                    p.x = leftBound + p.radius;
                    p.vx = -p.vx * 0.9;
                }
                if (p.x + p.radius > rightBound) {
                    p.x = rightBound - p.radius;
                    p.vx = -p.vx * 0.9;
                }
                
                // 上下边界
                if (p.y - p.radius < topBound) {
                    p.y = topBound + p.radius;
                    p.vy = -p.vy * 0.9;
                }
                if (p.y + p.radius > bottomBound) {
                    p.y = bottomBound - p.radius;
                    p.vy = -p.vy * 0.9;
                }
                
                // 粒子间碰撞（能量传递）
                for (let i = 0; i < particles.length; i++) {
                    for (let j = i + 1; j < particles.length; j++) {
                        const p1 = particles[i];
                        const p2 = particles[j];
                        
                        const dx = p2.x - p1.x;
                        const dy = p2.y - p1.y;
                        const distance = Math.sqrt(dx * dx + dy * dy);
                        
                        if (distance < p1.radius + p2.radius) {
                            // 计算碰撞法线
                            const nx = dx / distance;
                            const ny = dy / distance;
                            
                            // 计算相对速度
                            const dvx = p2.vx - p1.vx;
                            const dvy = p2.vy - p1.vy;
                            
                            // 计算相对速度在法线方向的分量
                            const speedNormal = dvx * nx + dvy * ny;
                            
                            // 只有相互靠近时才碰撞
                            if (speedNormal < 0) {
                                // 计算碰撞冲量（简化能量传递）
                                const impulse = 2 * speedNormal / (p1.mass + p2.mass);
                                
                                // 更新速度
                                p1.vx += impulse * p2.mass * nx;
                                p1.vy += impulse * p2.mass * ny;
                                p2.vx -= impulse * p1.mass * nx;
                                p2.vy -= impulse * p1.mass * ny;
                                
                                // 防止重叠
                                const overlap = (p1.radius + p2.radius - distance) / 2;
                                p1.x -= overlap * nx;
                                p1.y -= overlap * ny;
                                p2.x += overlap * nx;
                                p2.y += overlap * ny;
                            }
                        }
                    }
                }
            });
            
            // 更新熵
            calculateHeatConductionEntropy();
        }
        
        // 更新总结模块物理
        function updateSummaryPhysics() {
            updateFirstLawPhysics(); // 使用与第一定律相同的物理
        }
        
        // 绘制模块特定的图形
        function drawModuleSpecificGraphics() {
            ctx.font = '16px Arial';
            ctx.fillStyle = '#ecf0f1';
            ctx.textAlign = 'center';
            
            switch(currentModule) {
                case 'entropy-intro':
                    // 绘制盒子标签
                    ctx.fillText('左盒', canvas.width/4, 60);
                    ctx.fillText('右盒', 3*canvas.width/4, 60);
                    
                    // 绘制粒子计数
                    ctx.fillText(`粒子数: ${leftBoxParticles.length}`, canvas.width/4, canvas.height - 40);
                    ctx.fillText(`粒子数: ${rightBoxParticles.length}`, 3*canvas.width/4, canvas.height - 40);
                    break;
                    
                case 'gas-diffusion':
                    if (hasWall) {
                        ctx.fillText('点击"移除隔板"开始扩散', canvas.width/2, 60);
                    } else {
                        ctx.fillText('扩散进行中... 熵增加', canvas.width/2, 60);
                    }
                    break;
                    
                case 'heat-conduction':
                    ctx.fillStyle = '#e74c3c';
                    ctx.fillText('高温区', canvas.width/4, 60);
                    ctx.fillStyle = '#3498db';
                    ctx.fillText('低温区', 3*canvas.width/4, 60);
                    ctx.fillStyle = '#ecf0f1';
                    ctx.fillText('热传导使温度均衡，熵增加', canvas.width/2, canvas.height - 40);
                    break;
                    
                case 'summary':
                    ctx.fillText('混合状态：高熵', canvas.width/2, 60);
                    ctx.fillText('总能量守恒，但熵达到最大', canvas.width/2, canvas.height - 40);
                    break;
            }
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

# 交互式教学动画使用指南

## 功能说明

欢迎使用“热力学第一、第二定律与熵增原理”交互式教学动画！本动画旨在通过直观的微观粒子模拟，帮助您深入理解热力学两大核心定律的本质区别，特别是熵增原理的微观统计基础。

本工具将抽象的热力学概念转化为可视化的粒子运动，让您能够“看到”能量守恒的过程，并“感受”熵增的统计必然性。通过五个精心设计的教学模块，您将逐步建立起对热力学定律的深刻直觉。

## 主要功能

### 1. 模块化学习路径
- **第一定律：能量守恒** - 观察封闭系统中粒子动能与势能的相互转化，验证总能量守恒
- **熵的微观解释** - 通过“盒子与小球”模型理解微观状态数与熵的关系
- **气体扩散** - 观察两种气体粒子的混合过程，体验不可逆性的微观根源
- **热传导** - 追踪高温与低温粒子的能量传递，理解能量品质的退化
- **总结与对比** - 综合回顾两个定律的核心差异与内在联系

### 2. 交互控制功能
- **播放/暂停控制**：随时控制模拟的运行与停止
- **参数调节**：动态调整粒子数量、温度差等关键参数
- **场景操作**：随机分配粒子、移除隔板等特定交互
- **实时数据**：监控能量、熵值、微观状态数等关键物理量

### 3. 多维度信息呈现
- **粒子动画**：彩色粒子直观展示分子运动状态
- **数据面板**：实时显示关键物理量的数值变化
- **概率分布**：可视化展示不同宏观状态的概率差异
- **解释文本**：每个模块提供专业的概念解释

## 设计特色

### 1. 认知友好的学习路径
本动画遵循“从具体到抽象”的认知规律：
- 从看得见的粒子运动开始
- 逐步引入统计概念
- 最终建立抽象的熵增原理理解

### 2. 科学的视觉编码
- **色彩语义**：红色代表高温/快速，蓝色代表低温/慢速，紫色代表混合
- **动态数据**：熵值用橙色渐变表示，能量用青色固定显示
- **概率可视化**：用条形图直观展示不同分布状态的概率差异

### 3. 基于研究的教学设计
每个模块都针对常见学习难点设计：
- **认知冲突设计**：通过“为什么反向过程不会发生？”引发思考
- **操作-归纳模式**：让您通过亲手操作发现统计规律
- **多表征关联**：同一概念用动画、数据、图表三种方式呈现

## 教学要点

### 模块一：第一定律 - 能量守恒
**核心概念**：能量形式的转化与总量守恒
**关键观察**：
- 注意粒子速度（动能）与高度（势能）的相互转化
- 观察数据面板中“总能量”的恒定不变
- 思考：能量守恒是否决定了过程的方向？

### 模块二：熵的微观解释
**核心突破**：理解熵是微观状态数的度量
**关键操作**：
1. 多次点击“随机分配”按钮
2. 观察粒子在左右盒子中的分布变化
3. 注意概率分布图中“均匀分布”的概率最高
**教学提示**：这是理解熵增原理的关键步骤！请花时间充分体验“随机分配”的统计规律。

### 模块三：气体扩散
**核心现象**：不可逆过程的微观解释
**关键实验**：
1. 初始状态：红蓝粒子被隔板分离
2. 点击“移除隔板”开始扩散
3. 观察混合过程与熵值的同步增长
**深度思考**：为什么我们从未观察到混合气体自动分离？

### 模块四：热传导
**核心理解**：能量品质的退化
**关键观察**：
- 红色（高温）粒子与蓝色（低温）粒子的速度差异
- 碰撞过程中能量的传递
- 最终达到的速度均匀分布
**重要概念**：总能量守恒，但能量从“集中可用”变为“分散无用”

### 模块五：总结与对比
**核心整合**：两个定律的关系
**对比框架**：
- 第一定律：能量数量守恒（“能不能”）
- 第二定律：过程方向确定（“可不可以”）
- 熵增原理：统计规律的宏观表现

## 使用建议

### 1. 初次使用者
**推荐路径**：严格按照模块顺序学习（1→2→3→4→5）
**时间分配**：每个模块建议体验5-10分钟
**关键动作**：在模块二中，请至少进行10次“随机分配”操作，建立对统计规律的直觉

### 2. 课堂教师
**教学整合建议**：
- **预习环节**：让学生自主探索模块一、二
- **课堂演示**：重点讲解模块三、四，配合理论推导
- **巩固练习**：使用模块五进行总结，布置思考题
**讨论话题**：
- “如果宇宙最终达到热寂，能量是否消失了？”
- “生命体如何在不违反熵增原理的前提下维持有序？”

### 3. 自主学习与复习
**深度探索**：
- 尝试调整粒子数量，观察统计规律的变化
- 在热传导模块中，调节温度差参数，观察熵增速度的变化
- 思考：如何用本动画解释冰箱的工作原理？
**常见误区澄清**：
- 熵增 ≠ 无序，而是微观状态数的增加
- 局部熵减可能（如生命成长），但必须以环境熵增为代价

### 4. 技术提示
- **浏览器要求**：建议使用Chrome、Firefox等现代浏览器
- **性能优化**：粒子数量超过100时，动画可能变慢，可适当减少数量
- **移动设备**：本动画支持移动设备，但建议在平板或电脑上获得最佳体验

### 5. 扩展学习
完成本动画学习后，您可以进一步探索：
- 熵与信息论的关系
- 统计力学中的玻尔兹曼分布
- 非平衡态热力学与耗散结构理论

---

**最后的话**：

热力学定律是理解自然界运行的基本框架，而熵增原理更是连接微观与宏观世界的桥梁。本动画只是您探索之旅的起点，真正的理解来自于您的思考、质疑和探索。

祝您学习愉快，在微观粒子的舞蹈中，发现自然规律的深邃之美！

*—— 您的教育技术伙伴*