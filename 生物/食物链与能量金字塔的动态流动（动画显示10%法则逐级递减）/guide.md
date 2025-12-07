# 需求：食物链与能量金字塔的动态流动（动画显示10%法则逐级递减）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向初中或高中生物学学习者。用户的核心需求是：
1.  **理解抽象概念**：将“能量流动的10%法则”这一抽象、静态的生物学规律，转化为直观、动态、可感知的视觉过程。
2.  **建立系统关联**：清晰看到“食物链”（线性关系）与“能量金字塔”（立体、量化关系）之间的内在联系，理解“递减”不仅是数量减少，更是能量的耗散。
3.  **主动探索与验证**：不满足于被动观看，希望通过交互操作来验证或探索不同情境下的能量流动情况，加深记忆和理解。
4.  **获得清晰的知识结构**：动画需逻辑清晰，重点突出，避免信息过载，最终在脑海中形成关于生态系统能量流动的完整心智模型。

#### 教学设计思路
1.  **核心概念解构**：
    *   **主线**：太阳能 → 生产者（植物）固定 → 初级消费者（食草动物）摄取 → 次级消费者（食肉动物）摄取 → 顶级消费者。
    *   **核心法则**：能量在相邻营养级之间传递的效率约为10%，其余90%通过呼吸作用、热量散失、未被利用等途径耗散。
    *   **双重表征**：用“食物链”（箭头指向捕食者）表示摄食关系；用“能量金字塔”（塔层面积/高度）表示能量逐级递减的量化关系。

2.  **认知规律遵循**：
    *   **从具体到抽象**：先展示生动的生物形象（草、兔子、狐狸、狼）和捕食关系，再抽象为能量块和金字塔图形。
    *   **从动态到静态**：通过能量流动的动画过程吸引注意力，解释原理后，静态的金字塔作为总结性知识锚点。
    *   **多感官编码**：结合视觉流动（能量粒子）、数值变化（百分比、焦耳数）、可能的轻微音效（能量传递声），强化记忆。

3.  **交互设计策略**：
    *   **引导式探索**：设计“自动演示”模式，让用户先完整观看一遍标准流程。
    *   **控制与验证**：提供交互控件，允许用户选择从哪个营养级开始观察，或手动触发能量传递，亲身体验“10%”的输入与输出。
    *   **焦点提示**：鼠标悬停在某个营养级或能量块上时，高亮显示并提示该级的能量详情（如输入值、输出值、耗散途径）。

4.  **视觉呈现规划**：
    *   **场景布局**：左侧为“动态流动区”（食物链场景），右侧为“结构总结区”（能量金字塔）。能量从左侧产生，流向右侧构建金字塔。
    *   **能量视觉化**：使用**明亮的黄色光点或粒子流**代表能量，使其在深色背景上非常醒目。能量在传递时，粒子数量会显著减少（视觉上体现90%的耗散）。
    *   **耗散表现**：被耗散的能量可以转化为逐渐 fade out 的灰色/红色粒子，或通过简单的图标（热量符号、呼吸气泡）示意。

#### 配色方案选择
*   **背景色**：深蓝灰色（`#2c3e50`）或深青色（`#1a5276`），营造沉稳、专注的科技感学习环境，并能突出前景的亮色元素。
*   **能量色**：
    *   主能量流：亮黄色（`#f1c40f`）到金黄色（`#f39c12`）的渐变，象征阳光和活性能量。
    *   耗散能量：暗红色（`#c0392b`）或灰色（`#7f8c8d`），表示以热等形式散失。
*   **生物与营养级**：
    *   生产者（草）：绿色（`#27ae60`）。
    *   各级消费者：使用和谐且区分度高的颜色，如兔子用浅褐色（`#d35400`），狐狸用橙色（`#e67e22`），狼用深灰色（`#34495e`）。
*   **金字塔与UI**：
    *   金字塔轮廓：白色或浅灰色半透明线框。
    *   各营养级填充色：采用对应生物颜色的半透明版本，形成层次。
    *   按钮/控件：使用与能量色呼应的亮色（如`#3498db`蓝色），表示可交互。

#### 交互功能列表
1.  **播放控制**：
    *   “从头播放”按钮：重置动画并开始完整演示。
    *   “暂停/继续”按钮。
    *   “单步前进”按钮：手动触发下一级能量传递。
2.  **营养级聚焦**：
    *   点击食物链中的任一生物（或金字塔的任一层），动画将聚焦展示该营养级**接收**和**传递**能量的详细过程，并弹出详细数据卡片。
3.  **能量流控制**：
    *   一个滑块，允许用户**微调能量传递效率**（例如从5%到15%），实时观察右侧能量金字塔形状的变化（塔层厚度改变），直观理解效率对生态系统结构的影响。
4.  **信息显示**：
    *   实时数值显示：在能量流动时，动态显示当前传递的能量数值（如“1000 J → 100 J”）。
    *   悬停提示：鼠标悬停时，显示该级能量的来源、去向、耗散比例与途径。
    *   图例说明：固定位置显示颜色和符号的图例（如黄色粒子=能量，红色散失=呼吸耗散等）。
5.  **视图切换**：
    *   一个开关，可在“动态流动视图”（侧重过程）和“金字塔结构视图”（侧重结果）之间平滑过渡。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>食物链与能量金字塔 - 10%法则动态演示</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #1a5276;
            color: #ecf0f1;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        header {
            text-align: center;
            padding: 15px;
            background-color: rgba(44, 62, 80, 0.8);
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }
        
        h1 {
            color: #f1c40f;
            margin-bottom: 8px;
            font-size: 2.2rem;
        }
        
        .subtitle {
            color: #bdc3c7;
            font-size: 1.1rem;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .left-panel, .right-panel {
            flex: 1;
            min-width: 300px;
            background-color: rgba(44, 62, 80, 0.8);
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }
        
        .panel-title {
            color: #3498db;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #3498db;
            font-size: 1.4rem;
        }
        
        #animationCanvas {
            width: 100%;
            height: 400px;
            background-color: rgba(26, 82, 118, 0.3);
            border-radius: 8px;
            display: block;
        }
        
        #pyramidCanvas {
            width: 100%;
            height: 400px;
            background-color: rgba(26, 82, 118, 0.3);
            border-radius: 8px;
            display: block;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 20px;
            justify-content: center;
        }
        
        .control-group {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            background-color: rgba(52, 73, 94, 0.7);
            padding: 12px;
            border-radius: 8px;
            min-width: 150px;
        }
        
        .control-label {
            font-size: 0.9rem;
            color: #bdc3c7;
        }
        
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 18px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
            min-width: 120px;
        }
        
        button:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        button#resetBtn {
            background-color: #e74c3c;
        }
        
        button#resetBtn:hover {
            background-color: #c0392b;
        }
        
        .slider-container {
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 5px;
        }
        
        input[type="range"] {
            width: 90%;
            height: 8px;
            border-radius: 4px;
            background: #34495e;
            outline: none;
            -webkit-appearance: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #f1c40f;
            cursor: pointer;
        }
        
        .slider-value {
            font-weight: bold;
            color: #f1c40f;
        }
        
        .info-panel {
            background-color: rgba(44, 62, 80, 0.9);
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }
        
        .info-title {
            color: #2ecc71;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .info-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
        }
        
        .info-item {
            background-color: rgba(52, 73, 94, 0.5);
            padding: 12px;
            border-radius: 6px;
            border-left: 4px solid #f1c40f;
        }
        
        .info-item h4 {
            color: #f1c40f;
            margin-bottom: 5px;
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
        
        .current-info {
            background-color: rgba(41, 128, 185, 0.3);
            padding: 15px;
            border-radius: 8px;
            margin-top: 15px;
            text-align: center;
            font-size: 1.1rem;
            min-height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .highlight {
            color: #f1c40f;
            font-weight: bold;
        }
        
        .energy-value {
            color: #f1c40f;
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        .dissipated {
            color: #e74c3c;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .controls {
                flex-direction: column;
                align-items: center;
            }
            
            .control-group {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>食物链与能量金字塔</h1>
            <p class="subtitle">动态演示能量流动的10%法则 - 能量在营养级间逐级递减</p>
        </header>
        
        <div class="main-content">
            <div class="left-panel">
                <h2 class="panel-title">动态能量流动 (食物链)</h2>
                <canvas id="animationCanvas"></canvas>
                
                <div class="current-info" id="currentInfo">
                    点击"开始演示"按钮观察能量流动过程
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f1c40f;"></div>
                        <span class="legend-text">能量流动</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span class="legend-text">能量耗散 (呼吸、热量)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #27ae60;"></div>
                        <span class="legend-text">生产者 (草)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #d35400;"></div>
                        <span class="legend-text">初级消费者 (兔)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e67e22;"></div>
                        <span class="legend-text">次级消费者 (狐)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #34495e;"></div>
                        <span class="legend-text">顶级消费者 (狼)</span>
                    </div>
                </div>
            </div>
            
            <div class="right-panel">
                <h2 class="panel-title">能量金字塔结构</h2>
                <canvas id="pyramidCanvas"></canvas>
                
                <div class="controls">
                    <div class="control-group">
                        <div class="control-label">动画控制</div>
                        <button id="startBtn">开始演示</button>
                        <button id="pauseBtn">暂停/继续</button>
                        <button id="stepBtn">单步前进</button>
                        <button id="resetBtn">重置</button>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">能量传递效率</div>
                        <div class="slider-container">
                            <input type="range" id="efficiencySlider" min="5" max="20" value="10" step="1">
                            <div class="slider-value" id="efficiencyValue">10%</div>
                        </div>
                        <div class="control-label">调整滑块观察金字塔变化</div>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">视图切换</div>
                        <button id="viewToggleBtn">聚焦金字塔视图</button>
                        <div class="control-label">点击生物聚焦该营养级</div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="info-panel">
            <h3 class="info-title">能量流动原理说明</h3>
            <div class="info-content">
                <div class="info-item">
                    <h4>10%能量法则</h4>
                    <p>能量在相邻营养级之间传递时，大约只有10%的能量能够传递到下一营养级，其余90%通过呼吸作用、热量散失、未被利用等途径耗散。</p>
                </div>
                <div class="info-item">
                    <h4>食物链</h4>
                    <p>表示生物之间吃与被吃的关系，箭头指向捕食者。本演示展示：草 → 兔 → 狐 → 狼。</p>
                </div>
                <div class="info-item">
                    <h4>能量金字塔</h4>
                    <p>表示生态系统中各营养级能量值的对比关系。底层最宽，代表生产者固定的太阳能；向上逐级变窄，代表能量逐级递减。</p>
                </div>
                <div class="info-item">
                    <h4>交互操作</h4>
                    <p>1. 使用控制按钮管理动画播放<br>2. 调整滑块改变能量传递效率<br>3. 点击生物聚焦该营养级能量流动<br>4. 切换视图查看不同表现形式</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const animationCanvas = document.getElementById('animationCanvas');
        const pyramidCanvas = document.getElementById('pyramidCanvas');
        const animCtx = animationCanvas.getContext('2d');
        const pyramidCtx = pyramidCanvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvases() {
            animationCanvas.width = animationCanvas.offsetWidth;
            animationCanvas.height = animationCanvas.offsetHeight;
            pyramidCanvas.width = pyramidCanvas.offsetWidth;
            pyramidCanvas.height = pyramidCanvas.offsetHeight;
        }
        
        // 初始调整尺寸
        resizeCanvases();
        window.addEventListener('resize', resizeCanvases);
        
        // 获取控制元素
        const startBtn = document.getElementById('startBtn');
        const pauseBtn = document.getElementById('pauseBtn');
        const stepBtn = document.getElementById('stepBtn');
        const resetBtn = document.getElementById('resetBtn');
        const efficiencySlider = document.getElementById('efficiencySlider');
        const efficiencyValue = document.getElementById('efficiencyValue');
        const viewToggleBtn = document.getElementById('viewToggleBtn');
        const currentInfo = document.getElementById('currentInfo');
        
        // 动画状态
        let animationState = {
            isPlaying: false,
            currentStep: 0, // 0: 初始, 1: 草到兔, 2: 兔到狐, 3: 狐到狼, 4: 完成
            efficiency: 10, // 能量传递效率百分比
            viewMode: 'both', // 'both', 'pyramid', 'foodchain'
            energyValues: [10000, 0, 0, 0, 0], // 各营养级当前能量值 [草, 兔, 狐, 狼, 耗散]
            focusLevel: -1, // 聚焦的营养级索引
            particles: [], // 能量粒子
            dissipatedParticles: [] // 耗散粒子
        };
        
        // 营养级配置
        const trophicLevels = [
            { name: '生产者 (草)', color: '#27ae60', x: 0.15, y: 0.5, energy: 10000, key: 'producer' },
            { name: '初级消费者 (兔)', color: '#d35400', x: 0.35, y: 0.5, energy: 0, key: 'primary' },
            { name: '次级消费者 (狐)', color: '#e67e22', x: 0.65, y: 0.5, energy: 0, key: 'secondary' },
            { name: '顶级消费者 (狼)', color: '#34495e', x: 0.85, y: 0.5, energy: 0, key: 'top' }
        ];
        
        // 粒子类
        class Particle {
            constructor(x, y, color, targetX, targetY, isDissipated = false) {
                this.x = x;
                this.y = y;
                this.color = color;
                this.targetX = targetX;
                this.targetY = targetY;
                this.speed = isDissipated ? 0.5 + Math.random() * 1 : 2 + Math.random() * 2;
                this.size = isDissipated ? 2 + Math.random() * 3 : 3 + Math.random() * 4;
                this.isDissipated = isDissipated;
                this.life = 1.0;
                this.decayRate = isDissipated ? 0.01 : 0.02;
                this.vx = 0;
                this.vy = 0;
                this.calculateVelocity();
            }
            
            calculateVelocity() {
                const dx = this.targetX - this.x;
                const dy = this.targetY - this.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                this.vx = (dx / distance) * this.speed;
                this.vy = (dy / distance) * this.speed;
            }
            
            update() {
                this.x += this.vx;
                this.y += this.vy;
                
                if (this.isDissipated) {
                    this.life -= this.decayRate;
                    // 耗散粒子随机飘动
                    this.x += (Math.random() - 0.5) * 1.5;
                    this.y += (Math.random() - 0.5) * 1.5;
                }
                
                // 检查是否到达目标
                const dx = this.targetX - this.x;
                const dy = this.targetY - this.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance < 5 || this.life <= 0) {
                    return false; // 粒子应被移除
                }
                
                return true; // 粒子继续存在
            }
            
            draw(ctx) {
                ctx.save();
                ctx.globalAlpha = this.isDissipated ? this.life : 0.8;
                ctx.fillStyle = this.color;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
                ctx.restore();
            }
        }
        
        // 创建能量粒子
        function createEnergyParticles(sourceIndex, targetIndex, count, isDissipated = false) {
            const source = trophicLevels[sourceIndex];
            const target = trophicLevels[targetIndex];
            
            const canvasWidth = animationCanvas.width;
            const canvasHeight = animationCanvas.height;
            
            const sourceX = source.x * canvasWidth;
            const sourceY = source.y * canvasHeight;
            let targetX, targetY;
            
            if (isDissipated) {
                // 耗散粒子随机散开
                targetX = sourceX + (Math.random() - 0.5) * 200;
                targetY = sourceY - 50 - Math.random() * 100;
            } else {
                targetX = target.x * canvasWidth;
                targetY = target.y * canvasHeight;
            }
            
            const color = isDissipated ? '#e74c3c' : '#f1c40f';
            
            for (let i = 0; i < count; i++) {
                const particle = new Particle(
                    sourceX + (Math.random() - 0.5) * 30,
                    sourceY + (Math.random() - 0.5) * 30,
                    color,
                    targetX + (Math.random() - 0.5) * 30,
                    targetY + (Math.random() - 0.5) * 30,
                    isDissipated
                );
                
                if (isDissipated) {
                    animationState.dissipatedParticles.push(particle);
                } else {
                    animationState.particles.push(particle);
                }
            }
        }
        
        // 更新能量传递
        function updateEnergyTransfer() {
            if (animationState.currentStep >= 4) return;
            
            const sourceIndex = animationState.currentStep;
            const targetIndex = animationState.currentStep + 1;
            
            // 计算传递的能量
            const transferEfficiency = animationState.efficiency / 100;
            const energyToTransfer = animationState.energyValues[sourceIndex] * transferEfficiency;
            const energyDissipated = animationState.energyValues[sourceIndex] - energyToTransfer;
            
            // 更新能量值
            animationState.energyValues[sourceIndex] = 0;
            animationState.energyValues[targetIndex] = energyToTransfer;
            animationState.energyValues[4] += energyDissipated; // 耗散能量累加
            
            // 创建粒子
            const particleCount = 50;
            createEnergyParticles(sourceIndex, targetIndex, particleCount, false);
            createEnergyParticles(sourceIndex, targetIndex, Math.floor(particleCount * 4.5), true);
            
            // 更新信息显示
            updateInfoDisplay(sourceIndex, targetIndex, energyToTransfer, energyDissipated);
            
            // 进入下一步
            animationState.currentStep++;
            
            // 如果完成所有步骤，停止动画
            if (animationState.currentStep >= 4) {
                animationState.isPlaying = false;
                currentInfo.innerHTML = `能量流动完成！最终能量值：<span class="energy-value">草: 0J</span> | <span class="energy-value">兔: ${Math.round(animationState.energyValues[1])}J</span> | <span class="energy-value">狐: ${Math.round(animationState.energyValues[2])}J</span> | <span class="energy-value">狼: ${Math.round(animationState.energyValues[3])}J</span> | <span class="dissipated">耗散: ${Math.round(animationState.energyValues[4])}J</span>`;
            }
        }
        
        // 更新信息显示
        function updateInfoDisplay(sourceIndex, targetIndex, transferred, dissipated) {
            const sourceName = trophicLevels[sourceIndex].name;
            const targetName = trophicLevels[targetIndex].name;
            
            currentInfo.innerHTML = `
                <span class="highlight">${sourceName}</span> 传递 <span class="energy-value">${Math.round(transferred)}J</span> 
                (${animationState.efficiency}%) 到 <span class="highlight">${targetName}</span> | 
                <span class="dissipated">${Math.round(dissipated)}J (${100 - animationState.efficiency}%) 耗散</span>
            `;
        }
        
        // 绘制食物链动画
        function drawFoodChain() {
            const width = animationCanvas.width;
            const height = animationCanvas.height;
            
            // 清除画布
            animCtx.clearRect(0, 0, width, height);
            
            // 绘制背景
            animCtx.fillStyle = 'rgba(26, 82, 118, 0.3)';
            animCtx.fillRect(0, 0, width, height);
            
            // 绘制连接线
            animCtx.strokeStyle = 'rgba(255, 255, 255, 0.3)';
            animCtx.lineWidth = 2;
            animCtx.setLineDash([5, 5]);
            
            for (let i = 0; i < trophicLevels.length - 1; i++) {
                const startX = trophicLevels[i].x * width;
                const startY = trophicLevels[i].y * height;
                const endX = trophicLevels[i + 1].x * width;
                const endY = trophicLevels[i + 1].y * height;
                
                animCtx.beginPath();
                animCtx.moveTo(startX, startY);
                animCtx.lineTo(endX, endY);
                animCtx.stroke();
                
                // 绘制箭头
                drawArrow(animCtx, startX, startY, endX, endY);
            }
            
            animCtx.setLineDash([]);
            
            // 绘制粒子
            animationState.particles = animationState.particles.filter(particle => particle.update());
            animationState.dissipatedParticles = animationState.dissipatedParticles.filter(particle => particle.update());
            
            animationState.particles.forEach(particle => particle.draw(animCtx));
            animationState.dissipatedParticles.forEach(particle => particle.draw(animCtx));
            
            // 绘制营养级节点
            trophicLevels.forEach((level, index) => {
                const x = level.x * width;
                const y = level.y * height;
                const radius = 40;
                
                // 绘制能量值背景
                animCtx.fillStyle = 'rgba(0, 0, 0, 0.5)';
                animCtx.fillRect(x - 50, y - 80, 100, 25);
                
                // 绘制能量值
                animCtx.fillStyle = '#f1c40f';
                animCtx.font = 'bold 14px Arial';
                animCtx.textAlign = 'center';
                animCtx.fillText(`${Math.round(animationState.energyValues[index])} J`, x, y - 65);
                
                // 绘制节点
                animCtx.fillStyle = level.color;
                animCtx.beginPath();
                animCtx.arc(x, y, radius, 0, Math.PI * 2);
                animCtx.fill();
                
                // 绘制节点边框
                animCtx.strokeStyle = animationState.focusLevel === index ? '#f1c40f' : 'white';
                animCtx.lineWidth = animationState.focusLevel === index ? 4 : 2;
                animCtx.beginPath();
                animCtx.arc(x, y, radius, 0, Math.PI * 2);
                animCtx.stroke();
                
                // 绘制生物名称
                animCtx.fillStyle = 'white';
                animCtx.font = 'bold 16px Arial';
                animCtx.textAlign = 'center';
                animCtx.fillText(level.name, x, y + radius + 25);
                
                // 绘制点击提示
                if (animationState.currentStep === 0 || animationState.focusLevel === index) {
                    animCtx.fillStyle = 'rgba(52, 152, 219, 0.8)';
                    animCtx.font = '12px Arial';
                    animCtx.fillText('点击聚焦', x, y + radius + 45);
                }
            });
            
            // 绘制总耗散能量
            if (animationState.energyValues[4] > 0) {
                animCtx.fillStyle = 'rgba(0, 0, 0, 0.7)';
                animCtx.fillRect(width - 150, 20, 130, 40);
                
                animCtx.fillStyle = '#e74c3c';
                animCtx.font = 'bold 14px Arial';
                animCtx.textAlign = 'left';
                animCtx.fillText('总耗散能量:', width - 140, 40);
                animCtx.fillText(`${Math.round(animationState.energyValues[4])} J`, width - 140, 60);
            }
        }
        
        // 绘制箭头
        function drawArrow(ctx, fromX, fromY, toX, toY) {
            const headlen = 15;
            const dx = toX - fromX;
            const dy = toY - fromY;
            const angle = Math.atan2(dy, dx);
            
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headlen * Math.cos(angle - Math.PI / 6), toY - headlen * Math.sin(angle - Math.PI / 6));
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headlen * Math.cos(angle + Math.PI / 6), toY - headlen * Math.sin(angle + Math.PI / 6));
            ctx.stroke();
        }
        
        // 绘制能量金字塔
        function drawPyramid() {
            const width = pyramidCanvas.width;
            const height = pyramidCanvas.height;
            
            // 清除画布
            pyramidCtx.clearRect(0, 0, width, height);
            
            // 绘制背景
            pyramidCtx.fillStyle = 'rgba(26, 82, 118, 0.3)';
            pyramidCtx.fillRect(0, 0, width, height);
            
            // 计算金字塔参数
            const pyramidBase = width * 0.8;
            const pyramidTop = width * 0.1;
            const pyramidHeight = height * 0.7;
            const pyramidX = (width - pyramidBase) / 2;
            const pyramidY = height * 0.15;
            
            // 绘制金字塔轮廓
            pyramidCtx.strokeStyle = 'rgba(255, 255, 255, 0.6)';
            pyramidCtx.lineWidth = 3;
            
            pyramidCtx.beginPath();
            pyramidCtx.moveTo(pyramidX, pyramidY + pyramidHeight);
            pyramidCtx.lineTo(pyramidX + pyramidBase, pyramidY + pyramidHeight);
            pyramidCtx.lineTo(pyramidX + pyramidBase / 2, pyramidY);
            pyramidCtx.closePath();
            pyramidCtx.stroke();
            
            // 计算各层高度（基于能量值）
            const totalEnergy = 10000; // 初始能量
            const levelHeights = [];
            let currentHeight = pyramidHeight;
            
            for (let i = 0; i < 4; i++) {
                const energyRatio = animationState.energyValues[i] / totalEnergy;
                const levelHeight = energyRatio * pyramidHeight;
                levelHeights.push(levelHeight);
            }
            
            // 绘制金字塔各层
            let currentY = pyramidY + pyramidHeight;
            
            for (let i = 0; i < 4; i++) {
                const levelHeight = levelHeights[i];
                const levelWidth = pyramidBase * (currentY - pyramidY) / pyramidHeight;
                const levelX = pyramidX + (pyramidBase - levelWidth) / 2;
                
                // 绘制填充层
                pyramidCtx.fillStyle = trophicLevels[i].color + 'CC'; // 添加透明度
                pyramidCtx.beginPath();
                pyramidCtx.moveTo(levelX, currentY);
                pyramidCtx.lineTo(levelX + levelWidth, currentY);
                pyramidCtx.lineTo(pyramidX + pyramidBase / 2, currentY - levelHeight);
                pyramidCtx.closePath();
                pyramidCtx.fill();
                
                // 绘制层边框
                pyramidCtx.strokeStyle = 'white';
                pyramidCtx.lineWidth = 2;
                pyramidCtx.stroke();
                
                // 绘制层标签
                pyramidCtx.fillStyle = 'white';
                pyramidCtx.font = 'bold 14px Arial';
                pyramidCtx.textAlign = 'center';
                
                const labelY = currentY - levelHeight / 2;
                pyramidCtx.fillText(trophicLevels[i].name, pyramidX + pyramidBase / 2, labelY);
                
                // 绘制能量值
                pyramidCtx.fillStyle = '#f1c40f';
                pyramidCtx.font = 'bold 16px Arial';
                pyramidCtx.fillText(`${Math.round(animationState.energyValues[i])} J`, pyramidX + pyramidBase / 2, labelY + 20);
                
                // 绘制传递效率（如果不是最后一层）
                if (i < 3) {
                    const efficiency = animationState.efficiency;
                    pyramidCtx.fillStyle = '#3498db';
                    pyramidCtx.font = 'italic 12px Arial';
                    
                    const efficiencyY = currentY - levelHeight + 15;
                    pyramidCtx.fillText(`↓ ${efficiency}%`, pyramidX + pyramidBase / 2, efficiencyY);
                }
                
                currentY -= levelHeight;
            }
            
            // 绘制标题
            pyramidCtx.fillStyle = '#f1c40f';
            pyramidCtx.font = 'bold 18px Arial';
            pyramidCtx.textAlign = 'center';
            pyramidCtx.fillText('能量金字塔', width / 2, 30);
            
            // 绘制当前效率
            pyramidCtx.fillStyle = '#3498db';
            pyramidCtx.font = '16px Arial';
            pyramidCtx.fillText(`当前能量传递效率: ${animationState.efficiency}%`, width / 2, height - 30);
            
            // 绘制耗散能量
            if (animationState.energyValues[4] > 0) {
                pyramidCtx.fillStyle = '#e74c3c';
                pyramidCtx.font = '14px Arial';
                pyramidCtx.fillText(`总耗散能量: ${Math.round(animationState.energyValues[4])} J`, width / 2, height - 10);
            }
        }
        
        // 动画循环
        function animate() {
            if (animationState.viewMode !== 'pyramid') {
                drawFoodChain();
            }
            
            if (animationState.viewMode !== 'foodchain') {
                drawPyramid();
            }
            
            // 如果正在播放且当前步骤未完成，自动进行下一步
            if (animationState.isPlaying && animationState.currentStep < 4) {
                // 检查粒子是否基本消失
                if (animationState.particles.length < 10 && animationState.dissipatedParticles.length < 10) {
                    // 延迟一段时间再进行下一步
                    setTimeout(() => {
                        updateEnergyTransfer();
                    }, 800);
                }
            }
            
            requestAnimationFrame(animate);
        }
        
        // 开始动画循环
        animate();
        
        // 事件监听器
        startBtn.addEventListener('click', () => {
            if (animationState.currentStep >= 4) {
                resetAnimation();
            }
            
            animationState.isPlaying = true;
            currentInfo.innerHTML = '能量流动开始...';
        });
        
        pauseBtn.addEventListener('click', () => {
            animationState.isPlaying = !animationState.isPlaying;
            currentInfo.innerHTML = animationState.isPlaying ? '动画继续...' : '动画已暂停';
        });
        
        stepBtn.addEventListener('click', () => {
            if (animationState.currentStep < 4) {
                updateEnergyTransfer();
                animationState.isPlaying = false;
            }
        });
        
        resetBtn.addEventListener('click', resetAnimation);
        
        efficiencySlider.addEventListener('input', () => {
            animationState.efficiency = parseInt(efficiencySlider.value);
            efficiencyValue.textContent = `${animationState.efficiency}%`;
            
            // 如果动画已完成，重新计算能量值
            if (animationState.currentStep >= 4) {
                recalculateEnergyValues();
            }
        });
        
        viewToggleBtn.addEventListener('click', () => {
            if (animationState.viewMode === 'both') {
                animationState.viewMode = 'pyramid';
                viewToggleBtn.textContent = '聚焦食物链视图';
                animationCanvas.style.opacity = '0.3';
                pyramidCanvas.style.opacity = '1';
            } else if (animationState.viewMode === 'pyramid') {
                animationState.viewMode = 'foodchain';
                viewToggleBtn.textContent = '显示双视图';
                animationCanvas.style.opacity = '1';
                pyramidCanvas.style.opacity = '0.3';
            } else {
                animationState.viewMode = 'both';
                viewToggleBtn.textContent = '聚焦金字塔视图';
                animationCanvas.style.opacity = '1';
                pyramidCanvas.style.opacity = '1';
            }
        });
        
        // 点击营养级聚焦
        animationCanvas.addEventListener('click', (e) => {
            const rect = animationCanvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            const width = animationCanvas.width;
            const height = animationCanvas.height;
            
            // 检查点击了哪个营养级
            for (let i = 0; i < trophicLevels.length; i++) {
                const level = trophicLevels[i];
                const levelX = level.x * width;
                const levelY = level.y * height;
                const radius = 40;
                
                const distance = Math.sqrt((x - levelX) ** 2 + (y - levelY) ** 2);
                
                if (distance <= radius) {
                    animationState.focusLevel = i;
                    currentInfo.innerHTML = `聚焦: <span class="highlight">${level.name}</span> | 当前能量: <span class="energy-value">${Math.round(animationState.energyValues[i])}J</span>`;
                    
                    // 3秒后取消聚焦
                    setTimeout(() => {
                        animationState.focusLevel = -1;
                    }, 3000);
                    break;
                }
            }
        });
        
        // 重置动画
        function resetAnimation() {
            animationState.isPlaying = false;
            animationState.currentStep = 0;
            animationState.energyValues = [10000, 0, 0, 0, 0];
            animationState.particles = [];
            animationState.dissipatedParticles = [];
            animationState.focusLevel = -1;
            
            currentInfo.innerHTML = '动画已重置。点击"开始演示"按钮观察能量流动过程';
        }
        
        // 根据当前效率重新计算能量值
        function recalculateEnergyValues() {
            const efficiency = animationState.efficiency / 100;
            animationState.energyValues = [10000, 0, 0, 0, 0];
            
            for (let i = 0; i < 3; i++) {
                const transferred = animationState.energyValues[i] * efficiency;
                const dissipated = animation
<!--检测到代码截断，自动续写中...-->
dissipated = animationState.energyValues[i] - transferred;
                animationState.energyValues[i] = 0;
                animationState.energyValues[i + 1] = transferred;
                animationState.energyValues[4] += dissipated;
            }
            
            // 重新分配能量值（保持总量不变）
            animationState.energyValues = [
                10000,
                10000 * efficiency,
                10000 * efficiency * efficiency,
                10000 * efficiency * efficiency * efficiency,
                10000 - (10000 * efficiency * efficiency * efficiency)
            ];
            
            currentInfo.innerHTML = `能量值已根据 ${animationState.efficiency}% 效率重新计算`;
        }
        
        // 初始绘制
        drawFoodChain();
        drawPyramid();
        
        // 添加键盘快捷键
        document.addEventListener('keydown', (e) => {
            switch(e.key) {
                case ' ':
                    // 空格键切换播放/暂停
                    animationState.isPlaying = !animationState.isPlaying;
                    e.preventDefault();
                    break;
                case 'r':
                case 'R':
                    // R键重置
                    resetAnimation();
                    break;
                case 'ArrowRight':
                    // 右箭头单步前进
                    if (animationState.currentStep < 4) {
                        updateEnergyTransfer();
                        animationState.isPlaying = false;
                    }
                    break;
                case '1':
                case '2':
                case '3':
                case '4':
                    // 数字键1-4聚焦对应营养级
                    const index = parseInt(e.key) - 1;
                    if (index >= 0 && index < 4) {
                        animationState.focusLevel = index;
                        currentInfo.innerHTML = `聚焦: <span class="highlight">${trophicLevels[index].name}</span> | 当前能量: <span class="energy-value">${Math.round(animationState.energyValues[index])}J</span>`;
                        
                        setTimeout(() => {
                            animationState.focusLevel = -1;
                        }, 3000);
                    }
                    break;
            }
        });
        
        // 初始信息
        currentInfo.innerHTML = '欢迎使用能量流动演示！点击"开始演示"按钮或使用键盘快捷键（空格:播放/暂停, R:重置, 右箭头:单步, 数字1-4:聚焦营养级）';
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

# 交互式教学动画使用指南
## 《食物链与能量金字塔：10%法则动态演示》

欢迎使用本交互式教学动画！本工具旨在通过直观、动态的可视化方式，帮助您深入理解生态系统能量流动的核心概念——**10%法则**。无论您是教师、学生还是自学者，都能通过亲身体验和探索，将抽象的生物学原理转化为生动的认知图景。

---

### 一、功能说明

本动画通过双视图联动，完整呈现了生态系统能量流动的两个关键模型：

1.  **左侧 - 动态能量流动视图**：以食物链（草 → 兔 → 狐 → 狼）为场景，通过**亮黄色粒子流**实时模拟能量从生产者向顶级消费者的传递过程，并直观展示90%能量的耗散（红色粒子）。
2.  **右侧 - 能量金字塔结构视图**：将左侧流动的能量量化为金字塔结构，塔层宽度代表能量值，清晰展示能量从底层到顶层的**逐级递减**关系。

两个视图实时同步，能量在左侧流动，右侧的金字塔随之构建，完美诠释了“过程”与“结构”的统一。

---

### 二、主要功能与交互操作

#### 1. 动画控制区
*   **开始演示**：一键启动完整的能量流动动画，按照营养级顺序自动传递能量。
*   **暂停/继续**：随时控制动画播放，便于在关键步骤进行讲解或观察。
*   **单步前进**：手动触发下一营养级的能量传递，适合精细观察每一步的输入、输出与耗散。
*   **重置**：将动画恢复到初始状态，所有能量值归零，粒子清空。

#### 2. 核心实验区
*   **能量传递效率调节滑块**：
    *   **功能**：动态调整能量传递效率（5%-20%）。
    *   **教学意义**：这是本动画最强大的探究功能！拖动滑块，您将**实时看到右侧能量金字塔形状发生显著变化**。效率提高，金字塔变得更“胖”、更稳定；效率降低，金字塔变得更“瘦”、更高层生物能量严重不足。这直观揭示了能量传递效率如何从根本上决定生态系统的结构稳定性与营养级数量上限。

#### 3. 探索与聚焦
*   **视图切换按钮**：可在“双视图”、“聚焦金字塔”、“聚焦食物链”三种模式间切换，帮助您集中注意力于特定表现形式。
*   **点击生物聚焦**：在左侧食物链视图中，**直接点击任意生物图标**（草、兔、狐、狼）。该营养级将被高亮显示，并在信息栏展示其当前能量详情。这是进行针对性讲解的理想工具。
*   **键盘快捷键**（提升操作效率）：
    *   **空格键**：播放/暂停
    *   **R键**：重置动画
    *   **右箭头键**：单步前进
    *   **数字键1-4**：快速聚焦对应营养级（1:草，2:兔，3:狐，4:狼）

---

### 三、设计特色

1.  **双重编码，符合认知规律**：将同一过程用**动态粒子流**（过程感知）和**静态几何图形**（结构归纳）同时呈现，符合从具体到抽象、从过程到结论的认知路径，有效促进深度理解。
2.  **视觉隐喻精准**：
    *   **亮黄色粒子** = 活跃的、可传递的生物化学能。
    *   **红色消散粒子** = 通过呼吸作用以热能形式耗散的能量。
    *   **金字塔层宽度** = 能量值的直观量化。
3.  **“假设-验证”式探究**：调节效率滑块并观察金字塔变化，本质上是一个完整的科学探究过程。学生可以提出假设（“如果效率改变，金字塔会怎样？”），通过操作进行验证，从而自主构建知识。
4.  **专业友好的界面**：采用深色背景衬托核心元素，配色方案严格遵循生物学可视化惯例（生产者绿、能量黄、耗散红），在保证科学性的同时提供舒适的观看体验。

---

### 四、教学要点与建议

#### 适用于以下教学环节：
*   **概念引入**：播放完整动画，首先建立对能量流动方向和逐级递减的感性认识。
*   **原理讲解**：使用“单步前进”功能，配合信息栏的精确数值，逐步剖析每一级的能量输入、传递（10%）与耗散（90%）细节。
*   **探究活动**：布置任务：“如果将能量传递效率调整为15%，生态系统可能发生什么变化？”让学生操作滑块、观察金字塔并得出结论。
*   **复习与评估**：在动画运行中途暂停，提问：“此时狼的能量来自哪里？如果狐狸种群数量减少，对金字塔的哪一层影响最大？为什么？”

#### 关键讨论问题：
1.  为什么能量金字塔总是“正金字塔形”，而生物量金字塔有时会出现倒置？
2.  观察能量耗散的过程，思考这90%的能量最终去了哪里？这与热力学定律有何联系？
3.  根据10%法则，为什么食物链的长度通常不超过4-5个营养级？尝试用调节滑块到极低值（如5%）来验证你的想法。
4.  如果人类处于顶级消费者的位置，从能量利用的角度，直接以植物为食和以食草动物为食，哪种方式能养活更多人口？为什么？

---

### 五、使用建议

1.  **首次使用**：建议先点击“开始演示”，完整观看一遍标准流程，对整体过程建立印象。
2.  **课堂教学**：
    *   **教师主导模式**：教师操作，大屏幕演示，结合提问引导学生观察。
    *   **学生探究模式**：将学生分组，每人一台设备，完成特定的探究任务单（如：记录不同效率下的各级能量值，并绘制图表）。
3.  **自主学习**：鼓励学习者大胆尝试所有按钮和滑块，特别是**效率滑块**，这是理解能量传递效率生态意义的关键。不要害怕“弄乱”，随时可以“重置”。
4.  **结合实物**：本动画是理想的数字化模型，建议与真实的食物链案例（如池塘生态系统、草原生态系统）结合讲解，帮助学生在抽象模型与真实世界之间建立桥梁。

我们希望这个精心设计的工具，能像一位耐心的导师，帮助您和您的学生揭开生态系统能量流动的神秘面纱，在交互与探索中享受发现的乐趣，真正理解“万物皆流，能量递减”这一自然界的根本法则。

祝您探索愉快！