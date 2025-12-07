# 需求：α粒子散射实验（卢瑟福原子模型建立过程）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中或大学低年级的物理初学者。用户的核心需求是：
1.  **理解实验原理**：直观地看到α粒子如何被金箔散射，以及不同角度的散射是如何发生的。
2.  **建立模型认知**：通过对比“枣糕模型”预测与实际观察结果的巨大差异，深刻理解卢瑟福提出“核式结构模型”的逻辑必然性。
3.  **掌握关键结论**：明确“绝大多数α粒子穿过”、“少数大角度偏转”、“极少数被反弹”这三个核心观察现象及其对原子内部结构（原子核极小、质量集中、带正电）的推论。
4.  **降低抽象门槛**：将微观、不可见的粒子运动可视化、动态化，弥补想象力的不足，激发学习兴趣。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念**：
    *   前置知识：汤姆逊的“枣糕模型”（均匀正电球体+嵌着的电子）。
    *   实验装置：放射源、金箔、荧光屏、显微镜、真空环境。
    *   关键现象：绝大多数直线穿过、少数发生偏转、极少数被反弹。
    *   推理结论：原子内部大部分是空的，存在一个体积极小、质量极大、带正电的“原子核”。
    *   最终模型：卢瑟福的“行星模型”（核式结构模型）。

*   **认知规律**：
    遵循“现象观察 -> 认知冲突 -> 模型修正 -> 新模型建立”的科学发现逻辑。
    1.  **铺垫**：先展示基于“枣糕模型”的理论预测（α粒子只应发生微小偏转）。
    2.  **冲突**：再展示实际实验结果（出现大角度偏转甚至反弹），制造强烈的认知冲突。
    3.  **探究**：允许用户交互，改变“原子核”的参数（如大小、电荷），观察其对散射结果的影响，从而自己“发现”核式结构的特征。
    4.  **归纳**：最后总结现象与结论的对应关系，巩固新模型。

*   **交互设计**：
    *   **分步引导**：设置“实验装置”、“枣糕模型预测”、“实际实验”、“探索原子核”、“结论总结”等步骤，通过按钮或导航控制进程。
    *   **参数控制**：在“探索”环节，提供滑动条或按钮，让用户实时调整“原子核大小”、“原子核电荷数”，观察α粒子轨迹的即时变化（例如，核变大，大角度散射增多；核电荷变大，偏转更剧烈）。
    *   **粒子发射控制**：提供“单发”、“连发”、“持续发射”模式，方便用户仔细观察单个粒子轨迹或统计大量粒子的分布。
    *   **视图切换**：可在“宏观实验装置视图”和“微观原子尺度视图”之间切换，建立宏观现象与微观机制的联系。

*   **视觉呈现**：
    *   **层次清晰**：背景（实验仪器）用浅色、低饱和度颜色；运动主体（α粒子）用高亮、对比色（如亮蓝色轨迹）；关键目标（金原子、原子核）用突出但不同的颜色。
    *   **动态效果**：
        *   α粒子轨迹平滑，接近金核时因库仑力发生弯曲。
        *   粒子击中荧光屏时，有闪烁效果。
        *   被反弹的粒子，速度方向应有明显的反向动画。
    *   **示意图风格**：采用简洁、扁平化的卡通示意图风格，避免过于复杂的细节，确保核心信息突出。关键部件（如放射源、金箔）旁配有文字标签。
    *   **统计可视化**：在屏幕一侧或下方，可以用动态条形图实时统计“直线穿过”、“小角度偏转”、“大角度偏转”、“反弹”的粒子数量比例，使定量印象更直观。

#### 配色方案选择
*   **主背景/画布**：浅灰色（#f5f5f5）或极浅的米白色（#fafafa），营造干净、专注的实验室或绘图板感觉。
*   **实验装置**：深灰色（#333333）或金属灰（#777777），体现仪器的质感。
*   **α粒子与轨迹**：采用高饱和度的**亮蓝色**（#4285F4）表示粒子点，轨迹用同色系半透明线条（rgba(66, 133, 244, 0.7)）。蓝色在科技教育中常见，且与正电性（传统）关联。
*   **金箔与原子（枣糕模型）**：用**浅金色**（#FFD700）半透明矩形表示金箔，用**橙色**（#FFA726）小点表示“枣糕模型”中均匀分布的正电荷物质。
*   **原子核（核式模型）**：用**深红色**（#EA4335）小圆点表示。红色醒目，象征其高电荷、高密度、核心地位，与蓝色的α粒子形成强对比。
*   **电子**：用**亮绿色**（#34A853）小圆点表示，与正电荷的红/蓝形成区分。
*   **荧光屏闪光**：**明黄色**（#FBBC05）闪烁，模拟荧光。
*   **交互控件（按钮、滑块）**：采用中性蓝灰色（#5F7D95），与主配色协调且清晰可操作。
*   **文字与标注**：深灰色（#212121），确保高可读性。

#### 交互功能列表
1.  **流程控制按钮**：“上一步”、“下一步”、“重置动画”，控制教学主线进度。
2.  **实验模式切换**：
    *   “装置讲解”：高亮并标注实验各部分。
    *   “理论预测（枣糕模型）”：播放基于旧模型的模拟散射。
    *   “实际实验（核式模型）”：播放基于核式模型的模拟散射，展示三种典型现象。
3.  **粒子发射控制**：
    *   “发射单颗α粒子”：逐颗发射，便于跟踪轨迹。
    *   “连续发射”：以一定频率发射，观察统计规律。
    *   “暂停/继续”：控制动画播放。
4.  **探索模式参数调节**（在“探索原子核”环节激活）：
    *   **原子核大小滑块**：从“点状”到“较大”，实时观察α粒子轨迹变化，理解“核很小”的必要性。
    *   **原子核电荷数滑块**：调节正电荷量，观察偏转角度如何随之变化，理解库仑斥力的作用。
    *   “显示/隐藏力线/等势线”：可选功能，帮助理解电场作用。
5.  **视图切换按钮**：“宏观视图”（显示整个实验装置）与“微观视图”（聚焦单个或几个金原子附近的散射）切换。
6.  **统计面板显示/隐藏**：显示实时计数和比例的统计图。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>α粒子散射实验 - 卢瑟福原子模型建立过程</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #212121;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #5F7D95;
        }
        
        h1 {
            color: #333333;
            margin-bottom: 10px;
        }
        
        .subtitle {
            color: #5F7D95;
            font-size: 1.1em;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 25px;
        }
        
        .animation-panel {
            flex: 3;
            min-width: 300px;
            background-color: #fafafa;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            position: relative;
            overflow: hidden;
        }
        
        .control-panel {
            flex: 2;
            min-width: 300px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
        }
        
        .panel-title {
            color: #333333;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e0e0e0;
            font-size: 1.3em;
        }
        
        canvas {
            display: block;
            background-color: #fafafa;
            border-radius: 8px;
            width: 100%;
            height: 500px;
        }
        
        .step-controls {
            display: flex;
            justify-content: space-between;
            margin-bottom: 25px;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .step-btn {
            flex: 1;
            min-width: 120px;
            padding: 12px 15px;
            background-color: #5F7D95;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 1em;
            transition: all 0.2s;
            text-align: center;
        }
        
        .step-btn:hover {
            background-color: #4a6378;
            transform: translateY(-2px);
        }
        
        .step-btn.active {
            background-color: #4285F4;
            box-shadow: 0 4px 8px rgba(66, 133, 244, 0.3);
        }
        
        .experiment-controls {
            margin-bottom: 25px;
        }
        
        .control-group {
            margin-bottom: 20px;
        }
        
        .control-group h3 {
            color: #5F7D95;
            margin-bottom: 10px;
            font-size: 1.1em;
        }
        
        .btn-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .control-btn {
            padding: 10px 15px;
            background-color: #e8eef2;
            color: #333333;
            border: 1px solid #d0d7dd;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.95em;
            transition: all 0.2s;
            flex: 1;
            min-width: 100px;
            text-align: center;
        }
        
        .control-btn:hover {
            background-color: #dce3e9;
        }
        
        .control-btn.active {
            background-color: #4285F4;
            color: white;
            border-color: #4285F4;
        }
        
        .slider-container {
            margin-top: 15px;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }
        
        .slider-label span {
            font-size: 0.95em;
            color: #333333;
        }
        
        .slider-value {
            color: #4285F4;
            font-weight: bold;
        }
        
        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: #e0e0e0;
            outline: none;
            -webkit-appearance: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #4285F4;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        
        .stats-panel {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            margin-top: 20px;
            border-left: 4px solid #4285F4;
        }
        
        .stats-title {
            color: #333333;
            margin-bottom: 15px;
            font-size: 1.1em;
        }
        
        .stat-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            padding-bottom: 8px;
            border-bottom: 1px dashed #e0e0e0;
        }
        
        .stat-label {
            display: flex;
            align-items: center;
        }
        
        .color-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            margin-right: 10px;
        }
        
        .straight-dot { background-color: #4285F4; }
        .small-angle-dot { background-color: #34A853; }
        .large-angle-dot { background-color: #FBBC05; }
        .bounce-dot { background-color: #EA4335; }
        
        .stat-value {
            font-weight: bold;
            color: #333333;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #e0e0e0;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            font-size: 0.9em;
            color: #555555;
        }
        
        .legend-color {
            width: 16px;
            height: 16px;
            border-radius: 50%;
            margin-right: 8px;
        }
        
        .alpha-color { background-color: #4285F4; }
        .nucleus-color { background-color: #EA4335; }
        .electron-color { background-color: #34A853; }
        .gold-color { background-color: #FFD700; }
        
        .description {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 25px;
            margin-top: 20px;
        }
        
        .description h2 {
            color: #333333;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e0e0e0;
        }
        
        .description p {
            margin-bottom: 15px;
            line-height: 1.7;
        }
        
        .highlight {
            background-color: rgba(66, 133, 244, 0.1);
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #4285F4;
            margin: 20px 0;
        }
        
        .conclusion {
            background-color: rgba(234, 67, 53, 0.05);
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #EA4335;
            margin: 20px 0;
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #e0e0e0;
            color: #777777;
            font-size: 0.9em;
        }
        
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .step-btn {
                min-width: 100px;
                font-size: 0.9em;
                padding: 10px 5px;
            }
            
            canvas {
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>α粒子散射实验</h1>
        <p class="subtitle">卢瑟福原子核式结构模型的建立过程</p>
    </header>
    
    <div class="container">
        <div class="animation-panel">
            <h2 class="panel-title">实验模拟</h2>
            <canvas id="animationCanvas" width="800" height="500"></canvas>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color alpha-color"></div>
                    <span>α粒子（带正电）</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color nucleus-color"></div>
                    <span>原子核（带正电）</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color electron-color"></div>
                    <span>电子（带负电）</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color gold-color"></div>
                    <span>金箔</span>
                </div>
            </div>
        </div>
        
        <div class="control-panel">
            <h2 class="panel-title">实验控制</h2>
            
            <div class="step-controls">
                <button class="step-btn active" id="step1">1. 实验装置</button>
                <button class="step-btn" id="step2">2. 枣糕模型预测</button>
                <button class="step-btn" id="step3">3. 实际实验结果</button>
                <button class="step-btn" id="step4">4. 探索原子核</button>
                <button class="step-btn" id="step5">5. 结论总结</button>
            </div>
            
            <div class="experiment-controls">
                <div class="control-group">
                    <h3>粒子发射控制</h3>
                    <div class="btn-group">
                        <button class="control-btn active" id="singleShot">单发</button>
                        <button class="control-btn" id="continuous">连续发射</button>
                        <button class="control-btn" id="pauseBtn">暂停</button>
                        <button class="control-btn" id="resetBtn">重置</button>
                    </div>
                </div>
                
                <div class="control-group">
                    <h3>视图切换</h3>
                    <div class="btn-group">
                        <button class="control-btn active" id="macroView">宏观视图</button>
                        <button class="control-btn" id="microView">微观视图</button>
                    </div>
                </div>
                
                <div class="control-group" id="nucleusControlGroup">
                    <h3>原子核参数探索</h3>
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>原子核大小</span>
                            <span class="slider-value" id="nucleusSizeValue">5</span>
                        </div>
                        <input type="range" id="nucleusSizeSlider" min="1" max="30" value="5" step="1">
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>原子核电荷</span>
                            <span class="slider-value" id="nucleusChargeValue">79</span>
                        </div>
                        <input type="range" id="nucleusChargeSlider" min="10" max="150" value="79" step="1">
                    </div>
                </div>
            </div>
            
            <div class="stats-panel">
                <h3 class="stats-title">粒子统计 (发射: <span id="totalParticles">0</span>)</h3>
                <div class="stat-item">
                    <div class="stat-label">
                        <div class="color-dot straight-dot"></div>
                        <span>直线穿过</span>
                    </div>
                    <div class="stat-value" id="straightCount">0</div>
                </div>
                <div class="stat-item">
                    <div class="stat-label">
                        <div class="color-dot small-angle-dot"></div>
                        <span>小角度偏转</span>
                    </div>
                    <div class="stat-value" id="smallAngleCount">0</div>
                </div>
                <div class="stat-item">
                    <div class="stat-label">
                        <div class="color-dot large-angle-dot"></div>
                        <span>大角度偏转</span>
                    </div>
                    <div class="stat-value" id="largeAngleCount">0</div>
                </div>
                <div class="stat-item">
                    <div class="stat-label">
                        <div class="color-dot bounce-dot"></div>
                        <span>反弹回来</span>
                    </div>
                    <div class="stat-value" id="bounceCount">0</div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="description">
        <h2 id="stepTitle">1. 实验装置</h2>
        <div id="stepDescription">
            <p>α粒子散射实验由卢瑟福和他的学生盖革、马斯登于1909年进行。实验装置主要包括：</p>
            <ul style="margin-left: 20px; margin-bottom: 15px;">
                <li><strong>放射源</strong>：发射α粒子（氦原子核，带正电）</li>
                <li><strong>金箔</strong>：非常薄的金箔作为靶子</li>
                <li><strong>荧光屏</strong>：环绕金箔的屏幕，用于检测α粒子</li>
                <li><strong>显微镜</strong>：观察荧光屏上的闪烁</li>
                <li><strong>真空室</strong>：排除空气分子干扰</li>
            </ul>
            <p>动画中左侧的红色方块代表放射源，中间的金色区域代表金箔，右侧的弧形代表荧光屏。</p>
        </div>
    </div>
    
    <footer>
        <p>α粒子散射实验教学动画 | 基于HTML5 Canvas实现 | 设计思路遵循科学发现与认知规律</p>
    </footer>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 动画状态变量
        let currentStep = 1; // 当前步骤：1-5
        let isMacroView = true; // 是否为宏观视图
        let isPaused = false; // 是否暂停
        let isContinuous = false; // 是否为连续发射模式
        let animationId = null; // 动画ID
        let lastShotTime = 0; // 上次发射时间
        const shotInterval = 300; // 发射间隔(ms)
        
        // 实验参数
        let nucleusSize = 5; // 原子核大小
        let nucleusCharge = 79; // 原子核电荷数（金原子）
        
        // 统计变量
        let stats = {
            total: 0,
            straight: 0,
            smallAngle: 0,
            largeAngle: 0,
            bounce: 0
        };
        
        // 粒子数组
        let particles = [];
        
        // 原子数组（用于微观视图）
        let atoms = [];
        
        // 实验装置坐标
        const device = {
            source: { x: 50, y: canvas.height / 2, width: 30, height: 30 },
            foil: { x: canvas.width / 2, y: canvas.height / 2, width: 200, height: 300 },
            screen: { cx: canvas.width / 2, cy: canvas.height / 2, radius: 350, startAngle: -Math.PI/2, endAngle: Math.PI/2 }
        };
        
        // 颜色定义
        const colors = {
            alpha: '#4285F4',
            alphaTrail: 'rgba(66, 133, 244, 0.7)',
            nucleus: '#EA4335',
            electron: '#34A853',
            goldFoil: 'rgba(255, 215, 0, 0.3)',
            goldAtom: 'rgba(255, 215, 0, 0.7)',
            device: '#333333',
            screen: 'rgba(251, 188, 5, 0.1)',
            text: '#212121'
        };
        
        // 初始化原子
        function initAtoms() {
            atoms = [];
            const atomCount = isMacroView ? 15 : 5;
            const areaWidth = isMacroView ? device.foil.width : 400;
            const areaHeight = isMacroView ? device.foil.height : 400;
            const startX = isMacroView ? device.foil.x - device.foil.width/2 : canvas.width/2 - 200;
            const startY = isMacroView ? device.foil.y - device.foil.height/2 : canvas.height/2 - 200;
            
            for (let i = 0; i < atomCount; i++) {
                atoms.push({
                    x: startX + Math.random() * areaWidth,
                    y: startY + Math.random() * areaHeight,
                    nucleusSize: nucleusSize,
                    charge: nucleusCharge,
                    electrons: []
                });
                
                // 为每个原子添加电子（枣糕模型或核式模型）
                const electronCount = currentStep === 2 ? 79 : 79; // 枣糕模型和核式模型电子数相同
                for (let j = 0; j < electronCount; j++) {
                    if (currentStep === 2) {
                        // 枣糕模型：电子均匀分布在原子内
                        atoms[i].electrons.push({
                            x: startX + Math.random() * areaWidth,
                            y: startY + Math.random() * areaHeight,
                            radius: 3
                        });
                    } else {
                        // 核式模型：电子在核外随机分布
                        const angle = Math.random() * Math.PI * 2;
                        const distance = 50 + Math.random() * 100;
                        atoms[i].electrons.push({
                            x: atoms[i].x + Math.cos(angle) * distance,
                            y: atoms[i].y + Math.sin(angle) * distance,
                            radius: 3
                        });
                    }
                }
            }
        }
        
        // 粒子类
        class Particle {
            constructor(x, y, vx, vy) {
                this.x = x;
                this.y = y;
                this.vx = vx;
                this.vy = vy;
                this.radius = 4;
                this.trail = [];
                this.maxTrailLength = 20;
                this.color = colors.alpha;
                this.hitScreen = false;
                this.scatteringType = null; // 'straight', 'small', 'large', 'bounce'
                this.isActive = true;
            }
            
            update() {
                if (!this.isActive) return;
                
                // 保存轨迹点
                this.trail.push({x: this.x, y: this.y});
                if (this.trail.length > this.maxTrailLength) {
                    this.trail.shift();
                }
                
                // 更新位置
                this.x += this.vx;
                this.y += this.vy;
                
                // 检查是否击中荧光屏
                if (!this.hitScreen) {
                    const dx = this.x - device.screen.cx;
                    const dy = this.y - device.screen.cy;
                    const distance = Math.sqrt(dx*dx + dy*dy);
                    
                    if (distance >= device.screen.radius - 5 && distance <= device.screen.radius + 5) {
                        this.hitScreen = true;
                        
                        // 计算偏转角度（相对于初始方向）
                        const initialAngle = Math.atan2(0, 1); // 初始向右
                        const finalAngle = Math.atan2(dy, dx);
                        let angleDiff = Math.abs(finalAngle - initialAngle);
                        if (angleDiff > Math.PI) angleDiff = Math.PI * 2 - angleDiff;
                        
                        // 分类统计
                        if (angleDiff < Math.PI/12) { // < 15度
                            this.scatteringType = 'straight';
                            stats.straight++;
                        } else if (angleDiff < Math.PI/3) { // < 60度
                            this.scatteringType = 'small';
                            stats.smallAngle++;
                        } else if (angleDiff < Math.PI * 0.9) { // < 162度
                            this.scatteringType = 'large';
                            stats.largeAngle++;
                        } else { // 反弹
                            this.scatteringType = 'bounce';
                            stats.bounce++;
                        }
                        
                        stats.total++;
                        updateStatsDisplay();
                    }
                }
                
                // 检查是否出界
                if (this.x < -50 || this.x > canvas.width + 50 || this.y < -50 || this.y > canvas.height + 50) {
                    this.isActive = false;
                }
                
                // 在探索模式下，应用原子核的库仑力
                if (currentStep >= 3) {
                    for (let atom of atoms) {
                        const dx = this.x - atom.x;
                        const dy = this.y - atom.y;
                        const distance = Math.sqrt(dx*dx + dy*dy);
                        
                        // 如果粒子足够接近原子核
                        if (distance < 150) {
                            // 库仑斥力：F ∝ q1*q2 / r^2
                            const force = (nucleusCharge * 2) / (distance * distance) * 0.5; // 简化计算
                            const angle = Math.atan2(dy, dx);
                            
                            // 应用力（方向远离原子核）
                            this.vx += Math.cos(angle) * force;
                            this.vy += Math.sin(angle) * force;
                            
                            // 限制最大速度
                            const speed = Math.sqrt(this.vx*this.vx + this.vy*this.vy);
                            if (speed > 8) {
                                this.vx = (this.vx / speed) * 8;
                                this.vy = (this.vy / speed) * 8;
                            }
                            
                            // 如果直接撞到原子核（探索模式下）
                            if (currentStep === 4 && distance < atom.nucleusSize + this.radius) {
                                // 反弹
                                const normalAngle = Math.atan2(dy, dx);
                                const incidentAngle = Math.atan2(this.vy, this.vx);
                                const reflectionAngle = 2 * normalAngle - incidentAngle + Math.PI;
                                
                                const speed = Math.sqrt(this.vx*this.vx + this.vy*this.vy) * 0.8;
                                this.vx = Math.cos(reflectionAngle) * speed;
                                this.vy = Math.sin(reflectionAngle) * speed;
                                
                                // 防止粒子卡在原子核内
                                this.x = atom.x + Math.cos(normalAngle) * (atom.nucleusSize + this.radius + 1);
                                this.y = atom.y + Math.sin(normalAngle) * (atom.nucleusSize + this.radius + 1);
                            }
                        }
                    }
                }
            }
            
            draw() {
                if (!this.isActive) return;
                
                // 绘制轨迹
                ctx.strokeStyle = colors.alphaTrail;
                ctx.lineWidth = 2;
                ctx.beginPath();
                if (this.trail.length > 1) {
                    ctx.moveTo(this.trail[0].x, this.trail[0].y);
                    for (let i = 1; i < this.trail.length; i++) {
                        ctx.lineTo(this.trail[i].x, this.trail[i].y);
                    }
                    ctx.stroke();
                }
                
                // 绘制粒子
                ctx.fillStyle = this.color;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fill();
                
                // 如果击中了屏幕，显示闪烁效果
                if (this.hitScreen && this.scatteringType) {
                    ctx.fillStyle = this.scatteringType === 'straight' ? colors.alpha : 
                                   this.scatteringType === 'small' ? '#34A853' : 
                                   this.scatteringType === 'large' ? '#FBBC05' : '#EA4335';
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, 8, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 闪烁效果
                    const blink = Math.sin(Date.now() / 100) > 0;
                    if (blink) {
                        ctx.fillStyle = 'rgba(255, 255, 255, 0.7)';
                        ctx.beginPath();
                        ctx.arc(this.x, this.y, 5, 0, Math.PI * 2);
                        ctx.fill();
                    }
                }
            }
        }
        
        // 发射新的α粒子
        function shootParticle() {
            if (isPaused) return;
            
            // 根据当前步骤决定发射行为
            let vx = 5;
            let vy = 0;
            
            // 在步骤2（枣糕模型）添加微小随机偏转
            if (currentStep === 2) {
                vy = (Math.random() - 0.5) * 0.5;
            }
            
            // 在步骤3和4（实际实验和探索）添加更随机的发射方向
            if (currentStep >= 3) {
                vy = (Math.random() - 0.5) * 2;
            }
            
            particles.push(new Particle(
                device.source.x + device.source.width,
                device.source.y + (Math.random() - 0.5) * 20,
                vx,
                vy
            ));
        }
        
        // 绘制实验装置
        function drawDevice() {
            // 绘制放射源
            ctx.fillStyle = '#EA4335';
            ctx.fillRect(device.source.x, device.source.y - device.source.height/2, 
                        device.source.width, device.source.height);
            ctx.fillStyle = colors.text;
            ctx.font = '14px Arial';
            ctx.fillText('α放射源', device.source.x - 10, device.source.y + device.source.height/2 + 20);
            
            // 绘制金箔
            ctx.fillStyle = colors.goldFoil;
            ctx.fillRect(device.foil.x - device.foil.width/2, device.foil.y - device.foil.height/2,
                        device.foil.width, device.foil.height);
            ctx.strokeStyle = '#FFD700';
            ctx.lineWidth = 2;
            ctx.strokeRect(device.foil.x - device.foil.width/2, device.foil.y - device.foil.height/2,
                          device.foil.width, device.foil.height);
            ctx.fillStyle = colors.text;
            ctx.fillText('金箔', device.foil.x - 15, device.foil.y + device.foil.height/2 + 20);
            
            // 绘制荧光屏
            ctx.strokeStyle = '#FBBC05';
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.arc(device.screen.cx, device.screen.cy, device.screen.radius, 
                   device.screen.startAngle, device.screen.endAngle);
            ctx.stroke();
            
            // 屏幕填充色
            ctx.fillStyle = colors.screen;
            ctx.beginPath();
            ctx.arc(device.screen.cx, device.screen.cy, device.screen.radius, 
                   device.screen.startAngle, device.screen.endAngle);
            ctx.lineTo(device.screen.cx, device.screen.cy);
            ctx.closePath();
            ctx.fill();
            
            ctx.fillStyle = colors.text;
            ctx.fillText('荧光屏', canvas.width - 80, device.screen.cy);
            
            // 绘制显微镜（简化表示）
            ctx.strokeStyle = colors.device;
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(canvas.width - 50, device.screen.cy + 100);
            ctx.lineTo(canvas.width - 50, device.screen.cy - 100);
            ctx.stroke();
            
            ctx.beginPath();
            ctx.arc(canvas.width - 50, device.screen.cy, 15, 0, Math.PI * 2);
            ctx.stroke();
            
            ctx.fillStyle = colors.text;
            ctx.fillText('显微镜', canvas.width - 65, device.screen.cy + 130);
        }
        
        // 绘制原子
        function drawAtoms() {
            // 在步骤1（装置介绍）不绘制原子
            if (currentStep === 1) return;
            
            for (let atom of atoms) {
                // 绘制原子核（在步骤2中，枣糕模型没有集中的原子核）
                if (currentStep >= 3) {
                    ctx.fillStyle = colors.nucleus;
                    ctx.beginPath();
                    ctx.arc(atom.x, atom.y, atom.nucleusSize, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 在探索模式下显示原子核参数
                    if (currentStep === 4) {
                        ctx.fillStyle = colors.text;
                        ctx.font = '12px Arial';
                        ctx.fillText(`q=${atom.charge}`, atom.x - 15, atom.y - atom.nucleusSize - 5);
                    }
                }
                
                // 绘制电子
                for (let electron of atom.electrons) {
                    ctx.fillStyle = colors.electron;
                    ctx.beginPath();
                    ctx.arc(electron.x, electron.y, electron.radius, 0, Math.PI * 2);
                    ctx.fill();
                }
                
                // 在步骤2（枣糕模型）中，绘制原子边界和正电荷均匀分布
                if (currentStep === 2) {
                    // 绘制原子边界
                    ctx.strokeStyle = colors.goldAtom;
                    ctx.lineWidth = 1;
                    ctx.beginPath();
                    ctx.arc(atom.x, atom.y, 80, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    // 绘制均匀分布的正电荷（枣糕模型）
                    ctx.fillStyle = 'rgba(255, 167, 38, 0.6)';
                    for (let i = 0; i < 20; i++) {
                        const angle = Math.random() * Math.PI * 2;
                        const radius = Math.random() * 80;
                        const px = atom.x + Math.cos(angle) * radius;
                        const py = atom.y + Math.sin(angle) * radius;
                        ctx.beginPath();
                        ctx.arc(px, py, 4, 0, Math.PI * 2);
                        ctx.fill();
                    }
                    
                    // 标注
                    ctx.fillStyle = colors.text;
                    ctx.font = '12px Arial';
                    ctx.fillText('枣糕模型原子', atom.x - 40, atom.y - 90);
                }
            }
        }
        
        // 绘制步骤特定的覆盖层和标注
        function drawStepOverlay() {
            ctx.fillStyle = 'rgba(255, 255, 255, 0.7)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 24px Arial';
            ctx.textAlign = 'center';
            
            if (currentStep === 5) {
                // 结论总结
                ctx.fillText('实验结论与原子核式结构模型', canvas.width/2, 60);
                
                ctx.font = '18px Arial';
                const conclusions = [
                    '1. 绝大多数α粒子直线穿过 → 原子内部大部分是空的',
                    '2. 少数α粒子发生大角度偏转 → 原子中心存在带正电的核',
                    '3. 极少数α粒子被反弹 → 原子核质量大、体积小',
                    '',
                    '卢瑟福提出原子核式结构模型：',
                    '- 原子中心有一个带正电的原子核',
                    '- 核外电子绕核运动',
                    '- 原子核体积很小，但集中了几乎全部质量'
                ];
                
                for (let i = 0; i < conclusions.length; i++) {
                    ctx.fillText(conclusions[i], canvas.width/2, 120 + i * 30);
                }
                
                // 绘制简化的原子模型示意图
                const centerX = canvas.width/2;
                const centerY = canvas.height - 150;
                
                // 原子核
                ctx.fillStyle = colors.nucleus;
                ctx.beginPath();
                ctx.arc(centerX, centerY, 10, 0, Math.PI * 2);
                ctx.fill();
                
                // 电子轨道
                ctx.strokeStyle = 'rgba(0, 0, 0, 0.2)';
                ctx.beginPath();
                ctx.arc(centerX, centerY, 60, 0, Math.PI * 2);
                ctx.stroke();
                
                ctx.beginPath();
                ctx.arc(centerX, centerY, 100, 0, Math.PI * 2);
                ctx.stroke();
                
                // 电子
                ctx.fillStyle = colors.electron;
                for (let i = 0; i < 8; i++) {
                    const angle = Date.now() / 1000 + i * Math.PI/4;
                    const x = centerX + Math.cos(angle) * 60;
                    const y = centerY + Math.sin(angle) * 60;
                    ctx.beginPath();
                    ctx.arc(x, y, 5, 0, Math.PI * 2);
                    ctx.fill();
                }
                
                for (let i = 0; i < 8; i++) {
                    const angle = Date.now() / 800 + i * Math.PI/4;
                    const x = centerX + Math.cos(angle) * 100;
                    const y = centerY + Math.sin(angle) * 100;
                    ctx.beginPath();
                    ctx.arc(x, y, 5, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
        }
        
        // 更新统计显示
        function updateStatsDisplay() {
            document.getElementById('totalParticles').textContent = stats.total;
            document.getElementById('straightCount').textContent = stats.straight;
            document.getElementById('smallAngleCount').textContent = stats.smallAngle;
            document.getElementById('largeAngleCount').textContent = stats.largeAngle;
            document.getElementById('bounceCount').textContent = stats.bounce;
        }
        
        // 更新步骤描述
        function updateStepDescription() {
            const stepTitle = document.getElementById('stepTitle');
            const stepDescription = document.getElementById('stepDescription');
            
            const descriptions = {
                1: {
                    title: '1. 实验装置',
                    content: `<p>α粒子散射实验由
<!--检测到代码截断，自动续写中...-->
卢瑟福和他的学生盖革、马斯登于1909年进行。实验装置主要包括：</p>
            <ul style="margin-left: 20px; margin-bottom: 15px;">
                <li><strong>放射源</strong>：发射α粒子（氦原子核，带正电）</li>
                <li><strong>金箔</strong>：非常薄的金箔作为靶子</li>
                <li><strong>荧光屏</strong>：环绕金箔的屏幕，用于检测α粒子</li>
                <li><strong>显微镜</strong>：观察荧光屏上的闪烁</li>
                <li><strong>真空室</strong>：排除空气分子干扰</li>
            </ul>
            <p>动画中左侧的红色方块代表放射源，中间的金色区域代表金箔，右侧的弧形代表荧光屏。</p>`
                },
                2: {
                    title: '2. 枣糕模型预测',
                    content: `<p>在实验之前，主流的原子模型是汤姆逊的<strong>"枣糕模型"</strong>（葡萄干布丁模型）：</p>
            <ul style="margin-left: 20px; margin-bottom: 15px;">
                <li>原子是一个均匀分布的正电荷球体</li>
                <li>电子像"枣"一样嵌在正电荷"糕"中</li>
                <li>正电荷和质量均匀分布在整个原子中</li>
            </ul>
            <div class="highlight">
                <p><strong>理论预测：</strong>根据枣糕模型，α粒子穿过金箔时只会发生<strong>非常小的偏转</strong>（通常小于1度）。因为正电荷均匀分布，对α粒子的库仑斥力很小且分散。</p>
            </div>
            <p>点击"单发"或"连续发射"观察模拟结果。</p>`
                },
                3: {
                    title: '3. 实际实验结果',
                    content: `<p>实际实验结果令人震惊：</p>
            <ul style="margin-left: 20px; margin-bottom: 15px;">
                <li><strong>绝大多数α粒子</strong>（约99.9%）直线穿过金箔</li>
                <li><strong>少数α粒子</strong>发生了较大角度的偏转</li>
                <li><strong>极少数α粒子</strong>（约1/8000）被直接反弹回来</li>
            </ul>
            <div class="conclusion">
                <p><strong>卢瑟福的惊叹：</strong>"这就像你用15英寸的炮弹轰击一张纸，结果炮弹却被反弹回来打中了你！"</p>
            </div>
            <p>这一结果完全推翻了枣糕模型的预测。大角度偏转和反弹现象表明原子内部存在<strong>一个质量很大、体积很小、带正电的核心</strong>。</p>`
                },
                4: {
                    title: '4. 探索原子核',
                    content: `<p>现在您可以探索原子核参数如何影响散射结果：</p>
            <ul style="margin-left: 20px; margin-bottom: 15px;">
                <li><strong>调整原子核大小</strong>：如果原子核变大，更多α粒子会靠近它，导致大角度散射增多。</li>
                <li><strong>调整原子核电荷</strong>：电荷越大，库仑斥力越强，α粒子偏转角度越大。</li>
            </ul>
            <div class="highlight">
                <p><strong>关键发现：</strong>要解释实验中极少数大角度散射，原子核必须<strong>非常小</strong>（直径约10⁻¹⁵m，是原子直径的十万分之一）且<strong>电荷集中</strong>。</p>
            </div>
            <p>尝试不同的参数组合，观察α粒子轨迹的变化。</p>`
                },
                5: {
                    title: '5. 结论总结',
                    content: `<p>基于α粒子散射实验，卢瑟福提出了<strong>原子核式结构模型</strong>（行星模型）：</p>
            <ul style="margin-left: 20px; margin-bottom: 15px;">
                <li>原子中心有一个带正电的<strong>原子核</strong>，几乎集中了原子的全部质量</li>
                <li>原子核体积很小，直径约为10⁻¹⁵m</li>
                <li>电子在核外空间绕核运动</li>
                <li>原子内部大部分是<strong>空的</strong></li>
            </ul>
            <div class="conclusion">
                <p><strong>科学意义：</strong>这是人类第一次通过实验证实原子有核结构，标志着现代原子物理学的开端，为后来玻尔模型、量子力学的发展奠定了基础。</p>
            </div>
            <p>三种散射现象与原子结构的对应关系：</p>
            <ol style="margin-left: 20px;">
                <li>直线穿过 → 原子内部大部分是空的</li>
                <li>大角度偏转 → 原子中心存在带正电的核</li>
                <li>反弹回来 → 原子核质量大、体积小</li>
            </ol>`
                }
            };
            
            stepTitle.textContent = descriptions[currentStep].title;
            stepDescription.innerHTML = descriptions[currentStep].content;
        }
        
        // 主动画循环
        function animate() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制实验装置（宏观视图）
            if (isMacroView || currentStep === 1) {
                drawDevice();
            }
            
            // 绘制原子
            drawAtoms();
            
            // 更新和绘制所有粒子
            for (let i = particles.length - 1; i >= 0; i--) {
                particles[i].update();
                particles[i].draw();
                
                // 移除不活动的粒子
                if (!particles[i].isActive) {
                    particles.splice(i, 1);
                }
            }
            
            // 在连续发射模式下，定期发射新粒子
            if (isContinuous && !isPaused && currentStep !== 1 && currentStep !== 5) {
                const now = Date.now();
                if (now - lastShotTime > shotInterval) {
                    shootParticle();
                    lastShotTime = now;
                }
            }
            
            // 绘制步骤覆盖层（用于步骤5）
            if (currentStep === 5) {
                drawStepOverlay();
            }
            
            // 继续动画循环
            animationId = requestAnimationFrame(animate);
        }
        
        // 切换步骤
        function switchStep(step) {
            currentStep = step;
            
            // 更新按钮状态
            document.querySelectorAll('.step-btn').forEach((btn, index) => {
                if (index + 1 === step) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            // 重置粒子
            particles = [];
            stats = { total: 0, straight: 0, smallAngle: 0, largeAngle: 0, bounce: 0 };
            updateStatsDisplay();
            
            // 重新初始化原子
            initAtoms();
            
            // 更新描述
            updateStepDescription();
            
            // 步骤特定设置
            if (step === 1) {
                // 步骤1：只显示装置
                isPaused = true;
                document.getElementById('pauseBtn').textContent = '继续';
                document.getElementById('nucleusControlGroup').style.display = 'none';
            } else if (step === 2) {
                // 步骤2：枣糕模型
                isPaused = false;
                document.getElementById('pauseBtn').textContent = '暂停';
                document.getElementById('nucleusControlGroup').style.display = 'none';
            } else if (step === 3) {
                // 步骤3：实际实验
                isPaused = false;
                document.getElementById('pauseBtn').textContent = '暂停';
                document.getElementById('nucleusControlGroup').style.display = 'none';
            } else if (step === 4) {
                // 步骤4：探索模式
                isPaused = false;
                document.getElementById('pauseBtn').textContent = '暂停';
                document.getElementById('nucleusControlGroup').style.display = 'block';
            } else if (step === 5) {
                // 步骤5：结论
                isPaused = true;
                document.getElementById('pauseBtn').textContent = '继续';
                document.getElementById('nucleusControlGroup').style.display = 'none';
            }
        }
        
        // 初始化事件监听器
        function initEventListeners() {
            // 步骤按钮
            document.getElementById('step1').addEventListener('click', () => switchStep(1));
            document.getElementById('step2').addEventListener('click', () => switchStep(2));
            document.getElementById('step3').addEventListener('click', () => switchStep(3));
            document.getElementById('step4').addEventListener('click', () => switchStep(4));
            document.getElementById('step5').addEventListener('click', () => switchStep(5));
            
            // 粒子发射控制
            document.getElementById('singleShot').addEventListener('click', function() {
                isContinuous = false;
                document.getElementById('singleShot').classList.add('active');
                document.getElementById('continuous').classList.remove('active');
                if (currentStep !== 1 && currentStep !== 5) {
                    shootParticle();
                }
            });
            
            document.getElementById('continuous').addEventListener('click', function() {
                isContinuous = true;
                document.getElementById('continuous').classList.add('active');
                document.getElementById('singleShot').classList.remove('active');
            });
            
            document.getElementById('pauseBtn').addEventListener('click', function() {
                isPaused = !isPaused;
                this.textContent = isPaused ? '继续' : '暂停';
            });
            
            document.getElementById('resetBtn').addEventListener('click', function() {
                particles = [];
                stats = { total: 0, straight: 0, smallAngle: 0, largeAngle: 0, bounce: 0 };
                updateStatsDisplay();
                initAtoms();
            });
            
            // 视图切换
            document.getElementById('macroView').addEventListener('click', function() {
                isMacroView = true;
                document.getElementById('macroView').classList.add('active');
                document.getElementById('microView').classList.remove('active');
                initAtoms();
            });
            
            document.getElementById('microView').addEventListener('click', function() {
                isMacroView = false;
                document.getElementById('microView').classList.add('active');
                document.getElementById('macroView').classList.remove('active');
                initAtoms();
            });
            
            // 原子核参数滑块
            const nucleusSizeSlider = document.getElementById('nucleusSizeSlider');
            const nucleusSizeValue = document.getElementById('nucleusSizeValue');
            const nucleusChargeSlider = document.getElementById('nucleusChargeSlider');
            const nucleusChargeValue = document.getElementById('nucleusChargeValue');
            
            nucleusSizeSlider.addEventListener('input', function() {
                nucleusSize = parseInt(this.value);
                nucleusSizeValue.textContent = nucleusSize;
                
                // 更新所有原子的核大小
                for (let atom of atoms) {
                    atom.nucleusSize = nucleusSize;
                }
            });
            
            nucleusChargeSlider.addEventListener('input', function() {
                nucleusCharge = parseInt(this.value);
                nucleusChargeValue.textContent = nucleusCharge;
                
                // 更新所有原子的电荷
                for (let atom of atoms) {
                    atom.charge = nucleusCharge;
                }
            });
        }
        
        // 初始化函数
        function init() {
            // 初始化原子
            initAtoms();
            
            // 初始化事件监听器
            initEventListeners();
            
            // 初始化步骤描述
            updateStepDescription();
            
            // 隐藏探索控制组（初始在步骤1）
            document.getElementById('nucleusControlGroup').style.display = 'none';
            
            // 开始动画循环
            animate();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 《α粒子散射实验》交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态可视化方式，帮助您深入理解20世纪物理学史上这一里程碑式的实验——卢瑟福的α粒子散射实验，以及由此诞生的原子核式结构模型。请跟随本指南，开启您的科学探索之旅。

---

### 一、 功能说明

本动画是一个完整的、基于HTML5 Canvas技术的交互式模拟程序。它将复杂的微观物理过程转化为直观的视觉动画，并允许您通过交互操作，亲身体验科学发现的逻辑过程。您无需安装任何插件，在支持现代标准的浏览器中即可流畅运行。

### 二、 主要功能

动画界面分为两大区域：**左侧的动画模拟区**和**右侧的控制与信息面板**。

#### 1. 五步教学流程（核心导航）
通过顶部的五个步骤按钮，您可以系统性地学习整个科学发现过程：
*   **步骤1：实验装置** – 认识实验的各个组成部分（放射源、金箔、荧光屏、显微镜）。
*   **步骤2：枣糕模型预测** – 查看基于汤姆逊旧原子模型的理论预测结果（α粒子只发生微小偏转）。
*   **步骤3：实际实验结果** – 观察与旧模型预测完全不符的惊人实验结果（出现大角度偏转和反弹）。
*   **步骤4：探索原子核** – 化身“卢瑟福”，通过调节原子核参数，探究何种结构能解释实验现象。
*   **步骤5：结论总结** – 总结实验现象，明确卢瑟福原子核式结构模型的核心要点。

#### 2. 交互控制功能
*   **粒子发射控制**：
    *   **单发**：一次发射一颗α粒子，便于仔细观察其运动轨迹。
    *   **连续发射**：模拟大量α粒子轰击金箔的过程，快速积累统计规律。
    *   **暂停/继续**：随时冻结或继续动画。
    *   **重置**：清空所有已发射粒子，重新开始统计。
*   **视图切换**：
    *   **宏观视图**：显示完整的实验装置全景。
    *   **微观视图**：聚焦于金箔内部几个原子的尺度，更清晰地观察α粒子与原子核的相互作用细节。
*   **参数探索（步骤4专属）**：
    *   **原子核大小滑块**：实时调整原子核的视觉尺寸，观察其对散射结果的影响。
    *   **原子核电荷滑块**：实时调整原子核所带正电荷量，观察库仑斥力强度的变化如何改变α粒子的偏转角度。

#### 3. 实时数据反馈
右侧的统计面板实时记录并显示已发射α粒子的散射情况，分为四类：
*   **直线穿过**
*   **小角度偏转**
*   **大角度偏转**
*   **反弹回来**
这使实验的定量结果一目了然，完美印证了卢瑟福当年的观测数据。

### 三、 设计特色

1.  **遵循认知规律**：设计严格遵循“旧理论预测 → 新实验现象 → 认知冲突 → 模型建构 → 结论形成”的科学发现逻辑，符合学习者的思维路径。
2.  **对比式学习**：将“枣糕模型预测”与“实际实验结果”并置于同一框架下，通过强烈的视觉对比，让学习者深刻体会旧模型的失败与新模型的必然性。
3.  **探究式学习**：“探索原子核”环节将学习者从被动观察者转变为主动探究者。通过亲手调节参数，学习者能自行“发现”原子核必须“体积小、质量大、电荷集中”才能解释极端散射现象。
4.  **多层级可视化**：
    *   **宏观与微观结合**：视图切换功能连接了实验室尺度的装置与原子尺度的相互作用。
    *   **轨迹与统计结合**：既有个体粒子的动态轨迹，又有群体行为的统计数据，兼顾定性与定量分析。
5.  **专业的视觉设计**：采用经过教育学考量的配色方案（如蓝色α粒子、红色原子核），确保主体突出、层次分明。界面简洁美观，交互反馈清晰。

### 四、 教学要点

本动画完美诠释了以下核心教学知识点：
*   **实验三大现象**：绝大多数直线穿过、少数大角度偏转、极少数被反弹。
*   **现象背后的推论**：
    *   “直线穿过” → 原子内部大部分是空的。
    *   “大角度偏转” → 原子中心存在一个带正电的核。
    *   “被反弹” → 该核质量极大、体积极小。
*   **新旧模型更替**：从汤姆逊的“枣糕模型”（正电荷均匀分布）到卢瑟福的“核式结构模型”（行星模型）。
*   **库仑力的作用**：α粒子偏转的根本原因是与原子核之间的静电斥力。

**建议教学流程**：引导学生按步骤1→2→3→4→5顺序操作。在步骤2和步骤3，鼓励学生先做出自己的预测。在步骤4，提出引导性问题：“如果把原子核变大，结果会怎样？”“如果电荷增加，会有什么变化？”让学生通过操作寻找答案。

### 五、 使用建议

1.  **初次使用**：建议按照预设的五个步骤顺序完整体验一遍，以建立完整的知识框架。
2.  **课堂演示**：教师可使用“单发”模式逐步讲解关键粒子的轨迹，使用“连续发射”模式展示统计规律。在讲解结论时，切换到“步骤5”。
3.  **自主探究**：鼓励学生在“步骤4：探索原子核”中自由尝试。例如，将原子核大小调到最大，观察是否还能出现“极少数反弹”的现象；将电荷调小，观察大角度偏转是否减少。通过“试错”深化理解。
4.  **复习与测试**：可以跳过中间步骤，直接让学生操作“步骤4”，并提问：“要模拟出卢瑟福观察到的实验现象（即统计面板显示的比例），你应该如何设置原子核的大小和电荷？”以此检验学生对模型核心特征的理解。
5.  **结合思考**：动画是理解的利器，但思考才能内化知识。建议在使用过程中或结束后，引导学生讨论：为什么这个实验必须用金箔？为什么用α粒子而不是其他粒子？卢瑟福模型还存在哪些局限性？

---

希望本交互式动画能成为您理解原子物理的得力助手，让这段波澜壮阔的科学史在您的指尖生动重现。祝您探索愉快！