# 需求：细胞呼吸的电子传递与氧化磷酸化（内膜褶→ATP合酶旋转合成ATP）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的生物学学生。他们已具备细胞呼吸、线粒体结构、ATP等基础知识，但难以理解电子传递链（ETC）与氧化磷酸化（ATP合成）之间抽象的能量偶联机制。
2.  **核心痛点**：
    *   **过程抽象**：电子传递、质子泵送、质子梯度、ATP合酶旋转催化等是微观、动态且不可见的。
    *   **能量转换逻辑复杂**：学生容易混淆“电子传递释放能量”与“ATP合成消耗能量”这两个步骤，不理解质子梯度如何作为中间载体和驱动力。
    *   **结构与功能脱节**：线粒体内膜（特别是嵴）的结构如何高效支持这一过程，缺乏直观感受。
3.  **学习目标**：通过动画，学生应能：
    *   清晰描述电子从NADH/FADH2到O2的传递路径。
    *   理解电子传递如何驱动质子（H+）跨膜泵出，建立电化学梯度（质子动力势）。
    *   阐明质子通过ATP合酶回流时，如何驱动其机械旋转，并催化ADP与Pi合成ATP。
    *   建立“氧化（电子传递）与磷酸化（ATP合成）通过质子梯度偶联”的核心概念。

#### 教学设计思路
1.  **核心概念聚焦**：围绕 **“质子梯度是能量转换的通用货币”** 这一核心。所有动画设计都服务于展示“化学能（还原力）→ 电能（膜电位）→ 渗透能（浓度差）→ 机械能（旋转）→ 化学能（ATP）”的转换链条。
2.  **认知规律遵循**：
    *   **从宏观到微观**：开场展示完整的线粒体，然后镜头推入，聚焦于一个内膜嵴的横截面，建立空间场景。
    *   **从静态到动态**：先展示关键分子（复合物I-IV，ATP合酶）的静态位置，再逐步激活电子流、质子流和旋转。
    *   **从分步到整合**：先分步演示“电子传递与泵质子”、“ATP合酶工作”两个半反应，最后完整演示偶联的全过程。
    *   **控制认知负荷**：简化分子细节（用形状和颜色代表），突出关键粒子的流动（电子、质子）和关键部件的运动（ATP合酶转子）。
3.  **交互设计**：
    *   **阶段控制**：提供“分步播放/暂停/重置”按钮，允许学习者控制进度。
    *   **焦点切换**：允许点击/高亮显示特定复合物或ATP合酶，显示其名称和简要功能。
    *   **参数探索**：提供简单的滑块，可以“增加底物（NADH）”或“加入解偶联剂”，观察对质子梯度和ATP产出的实时影响，深化理解。
    *   **数据可视化**：实时显示“膜电位差”、“质子浓度差”和“ATP合成计数”的模拟仪表或数字，将抽象梯度量化。
4.  **视觉呈现**：
    *   **场景**：采用横截面视角，左侧为线粒体基质（深色、富含分子），右侧为膜间隙（浅色）。内膜形成明显的嵴状凸起。
    *   **关键组件**：
        *   **电子传递链（ETC）**：用四个风格化、颜色各异的“蛋白质复合物”（I, II, III, IV）嵌于膜中，辅以移动的醌（Q）和细胞色素c（Cyt c）。
        *   **质子（H+）**：用亮粉色（或橙色）小球表示，泵出和回流时清晰醒目。
        *   **ATP合酶**：分为两部分：嵌于膜中的**F0单元**（质子通道，可旋转的“转子”和“定子”）和伸入基质的**F1单元**（催化头，三个β亚基应能显示结合ADP+Pi、合成ATP、释放ATP的不同构象）。旋转是视觉重点。
        *   **能量分子**：NADH（蓝色）、O2（红色）、ADP/Pi（黄色）、ATP（亮绿色，合成时有闪光效果）。

#### 配色方案选择
*   **背景与膜**：
    *   基质：深蓝色到蓝紫色的渐变，象征富含酶和底物的“反应池”。
    *   膜间隙：浅灰色或淡黄色，形成对比。
    *   内膜：使用中性深灰色或棕褐色，作为清晰的视觉分隔和载体。
*   **功能元素**：
    *   **电子**：亮黄色的小球或闪烁光点，代表高能粒子。
    *   **质子（H+）**：亮粉色或暖橙色小球，与背景形成强对比，强调其流动。
    *   **ATP合酶**：
        *   F0转子/柄：深红色。
        *   F1催化头：三个β亚基使用柔和的绿色、蓝色、紫色区分，但整体协调。
    *   **能量分子**：
        *   NADH/NAD+：蓝色系（深蓝/浅蓝）。
        *   O2/H2O：红色系（红/粉）。
        *   ADP/Pi：暗黄色。
        *   ATP：亮绿色（成功合成时高亮）。
*   **信息与UI**：使用干净的非衬线字体（如Arial, Helvetica），按钮和仪表盘采用扁平化设计，主色为科技蓝或中性灰，避免干扰主动画。

#### 交互功能列表
1.  **主控面板**：播放、暂停、重置、进度条。
2.  **模式切换**：
    *   “分步学习模式”：分解为“电子传递”、“建立梯度”、“ATP合成”、“完整过程”四个可单独播放的章节。
    *   “自由运行模式”：连续循环播放完整过程。
3.  **高亮与提示**：
    *   鼠标悬停在任何复合物或分子上，显示其名称和简略角色。
    *   点击关键步骤，弹出简要文字说明。
4.  **实验模拟面板**：
    *   “底物浓度”滑块：控制NADH的输入速率，观察电子流、质子泵送速度和ATP产出的变化。
    *   “解偶联剂”开关：开启后，质子不经ATP合酶直接回流，质子梯度消失，电子传递加速但ATP停止合成。直观展示“解偶联”概念。
5.  **实时数据仪表**：
    *   质子梯度指示器（一个从“低”到“高”的条形图或模拟仪表）。
    *   ATP合成计数器（数字累加）。
    *   膜电位指示器（正负电荷符号或电压值）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>细胞呼吸：电子传递与氧化磷酸化</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', 'Helvetica', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            color: #e0e0e0;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .header {
            text-align: center;
            margin-bottom: 20px;
            width: 100%;
            max-width: 1200px;
        }
        
        h1 {
            color: #4fc3f7;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            color: #b0bec5;
            font-size: 1.1rem;
            margin-bottom: 20px;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            width: 100%;
            max-width: 1200px;
            gap: 20px;
        }
        
        .animation-section {
            background: rgba(30, 30, 46, 0.8);
            border-radius: 12px;
            padding: 15px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
            border: 1px solid #2a2a3e;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            overflow: hidden;
            border-radius: 8px;
            background: linear-gradient(to bottom, #0c2461 0%, #1e3799 30%, #4a69bd 100%);
        }
        
        #mitochondriaCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 15px;
            padding: 15px;
            background: rgba(40, 40, 60, 0.7);
            border-radius: 8px;
        }
        
        .btn {
            padding: 10px 18px;
            border: none;
            border-radius: 6px;
            background: linear-gradient(to right, #3498db, #2980b9);
            color: white;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }
        
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 8px rgba(0, 0, 0, 0.3);
            background: linear-gradient(to right, #3cb0fd, #3498db);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        .btn.active {
            background: linear-gradient(to right, #2ecc71, #27ae60);
            box-shadow: 0 0 10px rgba(46, 204, 113, 0.5);
        }
        
        .mode-selector {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
        }
        
        .mode-btn {
            padding: 8px 16px;
            font-size: 0.9rem;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
            flex: 1;
            min-width: 250px;
        }
        
        .slider-label {
            min-width: 120px;
            font-size: 0.9rem;
        }
        
        .slider {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            appearance: none;
            background: linear-gradient(to right, #1a5276, #3498db);
            border-radius: 4px;
            outline: none;
        }
        
        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #f1c40f;
            cursor: pointer;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
        }
        
        .slider-value {
            min-width: 40px;
            text-align: center;
            font-weight: bold;
            color: #f1c40f;
        }
        
        .toggle-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .toggle-label {
            min-width: 100px;
            font-size: 0.9rem;
        }
        
        .toggle-switch {
            position: relative;
            display: inline-block;
            width: 50px;
            height: 24px;
        }
        
        .toggle-switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }
        
        .toggle-slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #7f8c8d;
            border-radius: 24px;
            transition: .4s;
        }
        
        .toggle-slider:before {
            position: absolute;
            content: "";
            height: 16px;
            width: 16px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            border-radius: 50%;
            transition: .4s;
        }
        
        input:checked + .toggle-slider {
            background-color: #e74c3c;
        }
        
        input:checked + .toggle-slider:before {
            transform: translateX(26px);
        }
        
        .info-panel {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 15px;
        }
        
        .data-panel {
            flex: 1;
            min-width: 200px;
            background: rgba(30, 30, 46, 0.9);
            border-radius: 8px;
            padding: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .data-title {
            color: #4fc3f7;
            font-size: 1.1rem;
            margin-bottom: 10px;
            border-bottom: 1px solid #4fc3f7;
            padding-bottom: 5px;
        }
        
        .data-value {
            font-size: 1.8rem;
            font-weight: bold;
            text-align: center;
            margin: 10px 0;
        }
        
        .gradient-bar {
            height: 20px;
            width: 100%;
            background: linear-gradient(to right, #1a5276, #3498db, #85c1e9);
            border-radius: 10px;
            margin-top: 10px;
            position: relative;
            overflow: hidden;
        }
        
        .gradient-fill {
            height: 100%;
            width: 70%;
            background: linear-gradient(to right, #e74c3c, #f1c40f);
            border-radius: 10px;
            transition: width 0.5s ease;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding: 15px;
            background: rgba(40, 40, 60, 0.7);
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
        }
        
        .instructions {
            margin-top: 20px;
            padding: 15px;
            background: rgba(30, 30, 46, 0.8);
            border-radius: 8px;
            font-size: 0.95rem;
            line-height: 1.5;
        }
        
        .highlight {
            color: #f1c40f;
            font-weight: bold;
        }
        
        @media (max-width: 768px) {
            .container {
                gap: 15px;
            }
            
            .canvas-container {
                height: 400px;
            }
            
            .controls {
                flex-direction: column;
            }
            
            .slider-container, .toggle-container {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>细胞呼吸：电子传递与氧化磷酸化</h1>
        <div class="subtitle">线粒体内膜嵴 → ATP合酶旋转合成ATP | 交互式教学动画</div>
    </div>
    
    <div class="container">
        <div class="animation-section">
            <div class="canvas-container">
                <canvas id="mitochondriaCanvas"></canvas>
            </div>
            
            <div class="controls">
                <div class="mode-selector">
                    <button id="step1Btn" class="btn mode-btn active">1. 电子传递</button>
                    <button id="step2Btn" class="btn mode-btn">2. 建立梯度</button>
                    <button id="step3Btn" class="btn mode-btn">3. ATP合成</button>
                    <button id="fullProcessBtn" class="btn mode-btn">4. 完整过程</button>
                </div>
                
                <div class="playback-controls">
                    <button id="playBtn" class="btn">播放</button>
                    <button id="pauseBtn" class="btn">暂停</button>
                    <button id="resetBtn" class="btn">重置</button>
                </div>
                
                <div class="slider-container">
                    <div class="slider-label">NADH浓度:</div>
                    <input type="range" min="1" max="10" value="5" class="slider" id="nadhSlider">
                    <div class="slider-value" id="nadhValue">5</div>
                </div>
                
                <div class="toggle-container">
                    <div class="toggle-label">解偶联剂:</div>
                    <label class="toggle-switch">
                        <input type="checkbox" id="uncouplerToggle">
                        <span class="toggle-slider"></span>
                    </label>
                    <div class="slider-value" id="uncouplerStatus">关</div>
                </div>
            </div>
            
            <div class="info-panel">
                <div class="data-panel">
                    <div class="data-title">质子梯度强度</div>
                    <div class="data-value" id="gradientValue">70%</div>
                    <div class="gradient-bar">
                        <div class="gradient-fill" id="gradientFill"></div>
                    </div>
                </div>
                
                <div class="data-panel">
                    <div class="data-title">ATP合成计数</div>
                    <div class="data-value" id="atpCount">0</div>
                    <div style="text-align: center; font-size: 0.9rem; margin-top: 10px;">每3-4个H⁺合成1个ATP</div>
                </div>
                
                <div class="data-panel">
                    <div class="data-title">膜电位</div>
                    <div class="data-value" id="membranePotential">-150 mV</div>
                    <div style="text-align: center; font-size: 0.9rem; margin-top: 10px;">内膜内侧为负</div>
                </div>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #3498db;"></div>
                    <div class="legend-text">基质 (Matrix)</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #7f8c8d;"></div>
                    <div class="legend-text">膜间隙 (Intermembrane Space)</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #f1c40f;"></div>
                    <div class="legend-text">电子 (e⁻)</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #e74c3c;"></div>
                    <div class="legend-text">质子 (H⁺)</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #2ecc71;"></div>
                    <div class="legend-text">ATP</div>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #9b59b6;"></div>
                    <div class="legend-text">ATP合酶</div>
                </div>
            </div>
        </div>
        
        <div class="instructions">
            <p><span class="highlight">使用说明：</span> 本动画展示了线粒体内膜上电子传递链与ATP合酶的工作机制。通过控制面板，您可以分步学习整个过程，调节NADH浓度观察反应速率变化，或开启解偶联剂观察质子梯度消失对ATP合成的影响。</p>
            <p><span class="highlight">核心概念：</span> 电子传递释放的能量用于将质子(H⁺)泵出基质，形成质子梯度(电化学梯度)。质子通过ATP合酶回流时驱动其旋转，将ADP和Pi合成为ATP。这一过程称为氧化磷酸化。</p>
        </div>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('mitochondriaCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
        }
        
        // 初始调整尺寸
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 动画状态变量
        let animationId = null;
        let isPlaying = false;
        let currentMode = 'step1'; // step1, step2, step3, full
        let animationTime = 0;
        
        // 模拟参数
        let nadhConcentration = 5; // 1-10
        let isUncouplerActive = false;
        let protonGradient = 70; // 0-100%
        let atpCount = 0;
        let membranePotential = -150; // mV
        
        // 动画对象
        const animation = {
            // 线粒体结构
            matrix: { x: 0, y: 0, width: 0, height: 0 },
            membrane: { x: 0, y: 0, width: 0, height: 0 },
            cristae: [],
            
            // 电子传递链复合物
            complexes: [
                { name: '复合物 I', x: 0, y: 0, width: 0, height: 0, color: '#e67e22', protons: 4 },
                { name: '复合物 II', x: 0, y: 0, width: 0, height: 0, color: '#3498db', protons: 0 },
                { name: '复合物 III', x: 0, y: 0, width: 0, height: 0, color: '#9b59b6', protons: 4 },
                { name: '复合物 IV', x: 0, y: 0, width: 0, height: 0, color: '#e74c3c', protons: 2 }
            ],
            
            // ATP合酶
            atpSynthase: {
                x: 0, y: 0, width: 0, height: 0,
                f0: { rotation: 0, color: '#c0392b' },
                f1: { rotation: 0, color: '#8e44ad' },
                stalks: []
            },
            
            // 移动粒子
            electrons: [],
            protons: [],
            atpMolecules: [],
            
            // 醌和细胞色素c
            quinones: [],
            cytochromes: [],
            
            // 初始化函数
            init() {
                this.initStructure();
                this.initParticles();
            },
            
            // 初始化结构
            initStructure() {
                const canvasWidth = canvas.width;
                const canvasHeight = canvas.height;
                
                // 基质区域 (左侧)
                this.matrix.x = 0;
                this.matrix.y = 0;
                this.matrix.width = canvasWidth * 0.4;
                this.matrix.height = canvasHeight;
                
                // 膜间隙区域 (右侧)
                this.membrane.x = this.matrix.width;
                this.membrane.y = 0;
                this.membrane.width = canvasWidth * 0.6;
                this.membrane.height = canvasHeight;
                
                // 创建内膜嵴 (多个波浪形)
                this.cristae = [];
                const cristaCount = 5;
                const cristaHeight = canvasHeight * 0.15;
                
                for (let i = 0; i < cristaCount; i++) {
                    const yPos = canvasHeight * 0.1 + (i * canvasHeight * 0.2);
                    this.cristae.push({
                        x: this.matrix.width,
                        y: yPos,
                        width: canvasWidth * 0.5,
                        height: cristaHeight,
                        amplitude: cristaHeight * 0.4,
                        frequency: 0.02
                    });
                }
                
                // 设置复合物位置 (在嵴上)
                const complexSpacing = canvasWidth * 0.08;
                for (let i = 0; i < this.complexes.length; i++) {
                    this.complexes[i].x = this.matrix.width + 30 + (i * complexSpacing);
                    this.complexes[i].y = canvasHeight * 0.5;
                    this.complexes[i].width = 30;
                    this.complexes[i].height = 60;
                }
                
                // 设置ATP合酶位置 (在最后一个嵴上)
                this.atpSynthase.x = this.matrix.width + canvasWidth * 0.4;
                this.atpSynthase.y = canvasHeight * 0.5;
                this.atpSynthase.width = 40;
                this.atpSynthase.height = 100;
                
                // 初始化ATP合酶柄
                this.atpSynthase.stalks = [];
                const stalkCount = 3;
                for (let i = 0; i < stalkCount; i++) {
                    this.atpSynthase.stalks.push({
                        angle: (i * 2 * Math.PI) / stalkCount,
                        length: 20
                    });
                }
                
                // 初始化醌和细胞色素c
                this.quinones = [];
                this.cytochromes = [];
                
                for (let i = 0; i < 8; i++) {
                    this.quinones.push({
                        x: this.complexes[0].x + 40,
                        y: canvasHeight * 0.3 + (i * 20),
                        targetX: this.complexes[2].x - 20,
                        targetY: canvasHeight * 0.3 + (i * 20),
                        progress: 0,
                        speed: 0.01 + Math.random() * 0.01
                    });
                }
                
                for (let i = 0; i < 8; i++) {
                    this.cytochromes.push({
                        x: this.complexes[2].x + 40,
                        y: canvasHeight * 0.7 + (i * 20),
                        targetX: this.complexes[3].x - 20,
                        targetY: canvasHeight * 0.7 + (i * 20),
                        progress: 0,
                        speed: 0.01 + Math.random() * 0.01
                    });
                }
            },
            
            // 初始化粒子
            initParticles() {
                this.electrons = [];
                this.protons = [];
                this.atpMolecules = [];
            },
            
            // 更新动画
            update(deltaTime) {
                // 根据模式更新
                switch(currentMode) {
                    case 'step1':
                        this.updateStep1(deltaTime);
                        break;
                    case 'step2':
                        this.updateStep2(deltaTime);
                        break;
                    case 'step3':
                        this.updateStep3(deltaTime);
                        break;
                    case 'full':
                        this.updateFullProcess(deltaTime);
                        break;
                }
                
                // 更新醌和细胞色素c
                this.updateQuinonesAndCytochromes(deltaTime);
                
                // 更新粒子
                this.updateParticles(deltaTime);
                
                // 更新ATP合酶旋转
                this.updateATPSynthase(deltaTime);
                
                // 更新模拟参数
                this.updateSimulationParams(deltaTime);
            },
            
            // 步骤1: 电子传递
            updateStep1(deltaTime) {
                // 生成电子
                if (animationTime % (40 / nadhConcentration) < 1) {
                    this.createElectron();
                }
                
                // 移动电子
                for (let i = this.electrons.length - 1; i >= 0; i--) {
                    const electron = this.electrons[i];
                    
                    // 根据电子位置决定移动方向
                    if (electron.x < this.complexes[0].x) {
                        // 向复合物I移动
                        electron.x += electron.speed * deltaTime * 0.5;
                        electron.y += (this.complexes[0].y - electron.y) * 0.02;
                    } else if (electron.x < this.complexes[1].x && electron.complex < 1) {
                        // 在复合物I
                        electron.complex = 1;
                        electron.x = this.complexes[0].x;
                        electron.y = this.complexes[0].y;
                    } else if (electron.x < this.complexes[2].x && electron.complex < 2) {
                        // 向复合物III移动 (通过醌)
                        electron.x += electron.speed * deltaTime * 0.3;
                        electron.y += (this.complexes[2].y - electron.y) * 0.02;
                    } else if (electron.x < this.complexes[3].x && electron.complex < 3) {
                        // 在复合物III
                        electron.complex = 3;
                        electron.x = this.complexes[2].x;
                        electron.y = this.complexes[2].y;
                    } else if (electron.x < canvas.width * 0.9 && electron.complex < 4) {
                        // 向复合物IV移动 (通过细胞色素c)
                        electron.x += electron.speed * deltaTime * 0.3;
                        electron.y += (this.complexes[3].y - electron.y) * 0.02;
                    } else {
                        // 到达复合物IV，与O2结合生成水，电子消失
                        this.electrons.splice(i, 1);
                    }
                }
            },
            
            // 步骤2: 建立梯度
            updateStep2(deltaTime) {
                // 生成电子和质子
                if (animationTime % (40 / nadhConcentration) < 1) {
                    this.createElectron();
                }
                
                // 移动电子并泵送质子
                for (let i = this.electrons.length - 1; i >= 0; i--) {
                    const electron = this.electrons[i];
                    
                    if (electron.x < this.complexes[0].x) {
                        electron.x += electron.speed * deltaTime * 0.5;
                    } else if (electron.x < this.complexes[1].x && electron.complex < 1) {
                        electron.complex = 1;
                        electron.x = this.complexes[0].x;
                        // 复合物I泵送质子
                        this.createProton(this.complexes[0].x, this.complexes[0].y, true);
                    } else if (electron.x < this.complexes[2].x && electron.complex < 2) {
                        electron.x += electron.speed * deltaTime * 0.3;
                    } else if (electron.x < this.complexes[3].x && electron.complex < 3) {
                        electron.complex = 3;
                        electron.x = this.complexes[2].x;
                        // 复合物III泵送质子
                        this.createProton(this.complexes[2].x, this.complexes[2].y, true);
                    } else if (electron.x < canvas.width * 0.9 && electron.complex < 4) {
                        electron.x += electron.speed * deltaTime * 0.3;
                    } else {
                        electron.complex = 4;
                        electron.x = this.complexes[3].x;
                        // 复合物IV泵送质子
                        this.createProton(this.complexes[3].x, this.complexes[3].y, true);
                        this.electrons.splice(i, 1);
                    }
                }
                
                // 移动质子到膜间隙
                for (let i = this.protons.length - 1; i >= 0; i--) {
                    const proton = this.protons[i];
                    
                    if (proton.inMatrix) {
                        // 质子被泵出到膜间隙
                        proton.x += proton.speed * deltaTime * 0.8;
                        proton.y += (this.membrane.y + this.membrane.height * 0.2 - proton.y) * 0.05;
                        
                        if (proton.x > this.matrix.width + 50) {
                            proton.inMatrix = false;
                            proton.x = this.matrix.width + 50;
                        }
                    }
                }
            },
            
            // 步骤3: ATP合成
            updateStep3(deltaTime) {
                // 质子通过ATP合酶回流
                if (animationTime % 20 < 1 && protonGradient > 10) {
                    this.createProton(this.atpSynthase.x + 30, this.membrane.y + 50, false);
                }
                
                // 移动质子通过ATP合酶
                for (let i = this.protons.length - 1; i >= 0; i--) {
                    const proton = this.protons[i];
                    
                    if (!proton.inMatrix) {
                        // 质子从膜间隙通过ATP合酶回流到基质
                        proton.x -= proton.speed * deltaTime * 0.6;
                        proton.y += (this.atpSynthase.y - proton.y) * 0.03;
                        
                        // 当质子通过ATP合酶时
                        if (proton.x < this.atpSynthase.x + 20 && proton.x > this.atpSynthase.x - 10) {
                            proton.inMatrix = true;
                            
                            // 每3-4个质子合成一个ATP
                            protonGradient = Math.max(10, protonGradient - 3);
                            if (animationTime % 4 === 0) {
                                atpCount++;
                                this.createATPMolecule();
                                document.getElementById('atpCount').textContent = atpCount;
                            }
                        }
                        
                        // 如果质子进入基质，移除它
                        if (proton.x < this.matrix.width - 30) {
                            this.protons.splice(i, 1);
                        }
                    }
                }
            },
            
            // 完整过程
            updateFullProcess(deltaTime) {
                // 结合所有步骤
                this.updateStep2(deltaTime); // 电子传递和建立梯度
                
                // 质子通过ATP合酶回流 (如果梯度足够高)
                if (protonGradient > 20 && !isUncouplerActive) {
                    if (animationTime % (30 / nadhConcentration) < 1) {
                        this.createProton(this.atpSynthase.x + 30, this.membrane.y + 50, false);
                    }
                    
                    // 移动质子通过ATP合酶
                    for (let i = this.protons.length - 1; i >= 0; i--) {
                        const proton = this.protons[i];
                        
                        if (!proton.inMatrix && proton.x > this.atpSynthase.x - 30) {
                            proton.x -= proton.speed * deltaTime * 0.6;
                            proton.y += (this.atpSynthase.y - proton.y) * 0.03;
                            
                            if (proton.x < this.atpSynthase.x + 20 && proton.x > this.atpSynthase.x - 10) {
                                proton.inMatrix = true;
                                protonGradient = Math.max(10, protonGradient - 3);
                                
                                // 每3-4个质子合成一个ATP
                                if (animationTime % 4 === 0) {
                                    atpCount++;
                                    this.createATPMolecule();
                                    document.getElementById('atpCount').textContent = atpCount;
                                }
                            }
                        }
                    }
                }
                
                // 如果解偶联剂激活，质子直接回流
                if (isUncouplerActive && protonGradient > 10) {
                    if (animationTime % 10 < 1) {
                        this.createProton(this.matrix.width + 100, canvas.height * 0.7, false);
                    }
                    
                    for (let i = this.protons.length - 1; i >= 0; i--) {
                        const proton = this.protons[i];
                        if (!proton.inMatrix && proton.x > this.matrix.width + 50) {
                            proton.x -= proton.speed * deltaTime * 2;
                            if (proton.x < this.matrix.width + 30) {
                                protonGradient = Math.max(0, protonGradient - 5);
                                this.protons.splice(i, 1);
                            }
                        }
                    }
                }
            },
            
            // 更新醌和细胞色素c
            updateQuinonesAndCytochromes(deltaTime) {
                // 更新醌
                for (let quinone of this.quinones) {
                    quinone.progress += quinone.speed * deltaTime * 0.05;
                    if (quinone.progress > 1) quinone.progress = 0;
                    
                    quinone.x = quinone.x + (quinone.targetX - quinone.x) * 0.01;
                    quinone.y = quinone.y + (quinone.targetY - quinone.y) * 0.01;
                }
                
                // 更新细胞色素c
                for (let cytochrome of this.cytochromes) {
                    cytochrome.progress += cytochrome.speed * deltaTime * 0.05;
                    if (cytochrome.progress > 1) cytochrome.progress = 0;
                    
                    cytochrome.x = cytochrome.x + (cytochrome.targetX - cytochrome.x) * 0.01;
                    cytochrome.y = cytochrome.y + (cytochrome.targetY - cytochrome.y) * 0.01;
                }
            },
            
            // 更新粒子
            updateParticles(deltaTime) {
                // 更新ATP分子
                for (let i = this.atpMolecules.length - 1; i >= 0; i--) {
                    const atp = this.atpMolecules[i];
                    atp.y -= atp.speed * deltaTime * 0.3;
                    atp.life--;
                    
                    if (atp.life <= 0 || atp.y < 0) {
                        this.atpMolecules.splice(i, 1);
                    }
                }
            },
            
            // 更新ATP合酶
            updateATPSynthase(deltaTime) {
                // 根据质子梯度决定旋转速度
                let rotationSpeed = 0;
                if (protonGradient > 20 && !isUncouplerActive) {
                    rotationSpeed = (protonGradient / 100) * 0.05;
                }
                
                // 更新F0转子旋转
                this.atpSynthase.f0.rotation += rotationSpeed * deltaTime;
                
                // 更新F1催化头旋转 (方向相反)
                this.atpSynthase.f1.rotation -= rotationSpeed * deltaTime * 3;
                
                // 更新柄的角度
                for (let stalk of this.atpSynthase.stalks) {
                    stalk.angle += rotationSpeed * deltaTime * 2;
                }
            },
            
            // 更新模拟参数
            updateSimulationParams(deltaTime) {
                // 更新质子梯度
                if (currentMode === 'step2' || currentMode === 'full') {
                    // 电子传递增加梯度
                    if (animationTime % (60 / nadhConcentration) < 1 && protonGradient < 100) {
                        protonGradient = Math.min(100, protonGradient + 2);
                    }
                }
                
                // 如果解偶联剂激活，梯度快速下降
                if (isUncouplerActive && protonGradient > 0) {
                    protonGradient = Math.max(0, protonGradient - 0.5);
                }
                
                // 更新膜电位 (与梯度相关)
                membranePotential = -120 - (protonGradient * 0.3);
                
                // 更新UI显示
                document.getElementById('gradientValue').textContent = Math.round(protonGradient) + '%';
                document.getElementById('gradientFill').style.width = protonGradient + '%';
                document.getElementById('membranePotential').textContent = Math.round(membranePotential) + ' mV';
            },
            
            // 创建电子
            createElectron() {
                this.electrons.push({
                    x: this.matrix.width * 0.5,
                    y: this.complexes[0].y + (Math.random() * 60 - 30),
                    radius: 4,
                    color: '#f1c40f',
                    speed: 1 + Math.random() * 0.5,
                    complex: 0, // 当前所在的复合物
                    life: 500
                });
            },
            
            // 创建质子
            createProton(x, y, inMatrix) {
                this.protons.push({
                    x: x,
                    y: y,
                    radius: 5,
                    color: '#e74c3c',
                    speed: 0.5 + Math.random() * 0.3,
                    inMatrix: inMatrix, // true=在基质中, false=在膜间隙中
                    life: 300
                });
            },
            
            // 创建ATP分子
            createATPMolecule() {
                this.atpMolecules.push({
                    x: this.atpSynthase.x,
                    y: this.atpSynthase.y - 40,
                    radius: 6,
                    color: '#2ecc71',
                    speed: 0.3 + Math.random() * 0.2,
                    life: 100
                });
            },
            
            // 绘制函数
            draw() {
                // 清除画布
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                
                // 绘制基质
                ctx.fillStyle = '#3498db';
                ctx.fillRect(this.matrix.x, this.matrix.y, this.matrix.width, this.matrix.height);
                
                // 绘制基质渐变
                const matrixGradient = ctx.createLinearGradient(0, 0, this.matrix.width, 0);
                matrixGradient.addColorStop(0, 'rgba(52, 152, 219, 0.9)');
                matrixGradient.addColor
<!--检测到代码截断，自动续写中...-->
Stop(1, 'rgba(26, 82, 118, 0.9)');
                ctx.fillStyle = matrixGradient;
                ctx.fillRect(this.matrix.x, this.matrix.y, this.matrix.width, this.matrix.height);
                
                // 绘制膜间隙
                ctx.fillStyle = '#7f8c8d';
                ctx.fillRect(this.membrane.x, this.membrane.y, this.membrane.width, this.membrane.height);
                
                // 绘制内膜嵴
                ctx.strokeStyle = '#34495e';
                ctx.lineWidth = 3;
                
                for (let crista of this.cristae) {
                    ctx.beginPath();
                    ctx.moveTo(crista.x, crista.y);
                    
                    // 绘制波浪形内膜
                    for (let x = crista.x; x < crista.x + crista.width; x += 5) {
                        const y = crista.y + Math.sin(x * crista.frequency) * crista.amplitude;
                        ctx.lineTo(x, y);
                    }
                    
                    ctx.lineTo(crista.x + crista.width, crista.y);
                    ctx.stroke();
                    
                    // 填充嵴内部
                    ctx.fillStyle = 'rgba(52, 73, 94, 0.1)';
                    ctx.fill();
                }
                
                // 绘制内膜线 (分隔基质和膜间隙)
                ctx.beginPath();
                ctx.moveTo(this.matrix.width, 0);
                ctx.lineTo(this.matrix.width, canvas.height);
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 绘制电子传递链复合物
                for (let complex of this.complexes) {
                    // 复合物主体
                    ctx.fillStyle = complex.color;
                    ctx.fillRect(complex.x - complex.width/2, complex.y - complex.height/2, complex.width, complex.height);
                    
                    // 复合物边框
                    ctx.strokeStyle = '#2c3e50';
                    ctx.lineWidth = 2;
                    ctx.strokeRect(complex.x - complex.width/2, complex.y - complex.height/2, complex.width, complex.height);
                    
                    // 复合物标签
                    ctx.fillStyle = 'white';
                    ctx.font = '12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText(complex.name, complex.x, complex.y + complex.height/2 + 15);
                    
                    // 显示质子泵送数量
                    if (complex.protons > 0) {
                        ctx.fillStyle = 'rgba(231, 76, 60, 0.7)';
                        ctx.font = '10px Arial';
                        ctx.fillText(`H⁺: ${complex.protons}`, complex.x, complex.y - complex.height/2 - 10);
                    }
                }
                
                // 绘制醌 (Q)
                for (let quinone of this.quinones) {
                    const qx = quinone.x + Math.cos(animationTime * 0.01) * 10;
                    const qy = quinone.y + Math.sin(animationTime * 0.01) * 5;
                    
                    ctx.fillStyle = 'rgba(241, 196, 15, 0.8)';
                    ctx.beginPath();
                    ctx.arc(qx, qy, 6, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = '10px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('Q', qx, qy + 3);
                }
                
                // 绘制细胞色素c (Cyt c)
                for (let cytochrome of this.cytochromes) {
                    const cx = cytochrome.x + Math.sin(animationTime * 0.02) * 8;
                    const cy = cytochrome.y + Math.cos(animationTime * 0.02) * 4;
                    
                    ctx.fillStyle = 'rgba(155, 89, 182, 0.8)';
                    ctx.beginPath();
                    ctx.arc(cx, cy, 5, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = '9px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('c', cx, cy + 3);
                }
                
                // 绘制ATP合酶
                this.drawATPSynthase();
                
                // 绘制电子
                for (let electron of this.electrons) {
                    ctx.fillStyle = electron.color;
                    ctx.beginPath();
                    ctx.arc(electron.x, electron.y, electron.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 电子光晕效果
                    ctx.shadowColor = '#f1c40f';
                    ctx.shadowBlur = 10;
                    ctx.fill();
                    ctx.shadowBlur = 0;
                    
                    // 电子标签
                    ctx.fillStyle = 'white';
                    ctx.font = '9px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('e⁻', electron.x, electron.y + 3);
                }
                
                // 绘制质子
                for (let proton of this.protons) {
                    ctx.fillStyle = proton.color;
                    ctx.beginPath();
                    ctx.arc(proton.x, proton.y, proton.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 质子光晕效果
                    ctx.shadowColor = '#e74c3c';
                    ctx.shadowBlur = 8;
                    ctx.fill();
                    ctx.shadowBlur = 0;
                    
                    // 质子标签
                    ctx.fillStyle = 'white';
                    ctx.font = '9px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('H⁺', proton.x, proton.y + 3);
                }
                
                // 绘制ATP分子
                for (let atp of this.atpMolecules) {
                    ctx.fillStyle = atp.color;
                    ctx.beginPath();
                    ctx.arc(atp.x, atp.y, atp.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // ATP光晕效果
                    ctx.shadowColor = '#2ecc71';
                    ctx.shadowBlur = 15;
                    ctx.fill();
                    ctx.shadowBlur = 0;
                    
                    // ATP标签
                    ctx.fillStyle = 'white';
                    ctx.font = '9px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('ATP', atp.x, atp.y + 3);
                }
                
                // 绘制氧气和水
                this.drawOxygenAndWater();
                
                // 绘制当前模式提示
                this.drawModeHint();
            },
            
            // 绘制ATP合酶
            drawATPSynthase() {
                const synth = this.atpSynthase;
                
                // F0单元 (膜内部分，质子通道)
                ctx.save();
                ctx.translate(synth.x, synth.y);
                ctx.rotate(synth.f0.rotation);
                
                // F0转子
                ctx.fillStyle = synth.f0.color;
                ctx.fillRect(-15, -30, 30, 60);
                
                // F0质子通道指示
                ctx.fillStyle = 'rgba(231, 76, 60, 0.6)';
                for (let i = 0; i < 3; i++) {
                    const angle = (i * 2 * Math.PI) / 3;
                    const x = Math.cos(angle) * 10;
                    const y = Math.sin(angle) * 10;
                    ctx.beginPath();
                    ctx.arc(x, y, 4, 0, Math.PI * 2);
                    ctx.fill();
                }
                
                ctx.restore();
                
                // F1单元 (基质部分，催化头)
                ctx.save();
                ctx.translate(synth.x, synth.y - 40);
                ctx.rotate(synth.f1.rotation);
                
                // F1催化头
                ctx.fillStyle = synth.f1.color;
                ctx.beginPath();
                ctx.arc(0, 0, 25, 0, Math.PI * 2);
                ctx.fill();
                
                // F1亚基指示
                ctx.strokeStyle = 'white';
                ctx.lineWidth = 2;
                for (let i = 0; i < 3; i++) {
                    const angle = (i * 2 * Math.PI) / 3;
                    const x1 = Math.cos(angle) * 15;
                    const y1 = Math.sin(angle) * 15;
                    const x2 = Math.cos(angle) * 25;
                    const y2 = Math.sin(angle) * 25;
                    
                    ctx.beginPath();
                    ctx.moveTo(x1, y1);
                    ctx.lineTo(x2, y2);
                    ctx.stroke();
                    
                    // 亚基状态标签
                    ctx.fillStyle = 'white';
                    ctx.font = '8px Arial';
                    ctx.textAlign = 'center';
                    const labels = ['ADP+Pi', '合成', '释放'];
                    ctx.fillText(labels[i], x2 + Math.cos(angle)*5, y2 + Math.sin(angle)*5);
                }
                
                ctx.restore();
                
                // 连接柄
                for (let stalk of synth.stalks) {
                    const startX = synth.x + Math.cos(stalk.angle) * 10;
                    const startY = synth.y + Math.sin(stalk.angle) * 10;
                    const endX = synth.x + Math.cos(stalk.angle) * stalk.length;
                    const endY = synth.y - 40 + Math.sin(stalk.angle) * stalk.length;
                    
                    ctx.strokeStyle = '#f39c12';
                    ctx.lineWidth = 3;
                    ctx.beginPath();
                    ctx.moveTo(startX, startY);
                    ctx.lineTo(endX, endY);
                    ctx.stroke();
                }
                
                // ATP合酶标签
                ctx.fillStyle = 'white';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('ATP合酶', synth.x, synth.y + 60);
                
                // 旋转方向指示
                if (protonGradient > 20 && !isUncouplerActive) {
                    ctx.strokeStyle = '#2ecc71';
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.arc(synth.x, synth.y, 35, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    // 箭头指示旋转方向
                    ctx.fillStyle = '#2ecc71';
                    ctx.beginPath();
                    ctx.moveTo(synth.x + 35, synth.y);
                    ctx.lineTo(synth.x + 25, synth.y - 5);
                    ctx.lineTo(synth.x + 25, synth.y + 5);
                    ctx.closePath();
                    ctx.fill();
                }
            },
            
            // 绘制氧气和水
            drawOxygenAndWater() {
                // 氧气 (在复合物IV处)
                const oxyX = this.complexes[3].x + 50;
                const oxyY = this.complexes[3].y;
                
                ctx.fillStyle = 'rgba(231, 76, 60, 0.8)';
                ctx.beginPath();
                ctx.arc(oxyX, oxyY, 8, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = 'white';
                ctx.font = '10px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('O₂', oxyX, oxyY + 3);
                
                // 水分子 (氧气接受电子后生成)
                const waterX = oxyX + 30;
                const waterY = oxyY;
                
                ctx.fillStyle = 'rgba(52, 152, 219, 0.8)';
                ctx.beginPath();
                ctx.arc(waterX, waterY, 8, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = 'white';
                ctx.font = '10px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('H₂O', waterX, waterY + 3);
                
                // 电子传递终点箭头
                ctx.strokeStyle = '#f1c40f';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(oxyX - 10, oxyY);
                ctx.lineTo(waterX - 10, waterY);
                ctx.stroke();
                
                // 箭头头
                ctx.fillStyle = '#f1c40f';
                ctx.beginPath();
                ctx.moveTo(waterX - 10, waterY);
                ctx.lineTo(waterX - 15, waterY - 5);
                ctx.lineTo(waterX - 15, waterY + 5);
                ctx.closePath();
                ctx.fill();
            },
            
            // 绘制当前模式提示
            drawModeHint() {
                const hints = {
                    'step1': '步骤1: 电子传递 - NADH提供电子，电子沿传递链移动',
                    'step2': '步骤2: 建立质子梯度 - 电子传递释放能量，泵送H⁺建立梯度',
                    'step3': '步骤3: ATP合成 - H⁺通过ATP合酶回流，驱动ATP合成',
                    'full': '完整过程: 氧化与磷酸化通过质子梯度偶联'
                };
                
                ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
                ctx.font = '16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(hints[currentMode], canvas.width / 2, 30);
                
                // 当前模式高亮
                ctx.strokeStyle = '#4fc3f7';
                ctx.lineWidth = 3;
                ctx.strokeRect(canvas.width / 2 - 200, 10, 400, 30);
            }
        };
        
        // 初始化动画
        animation.init();
        
        // 动画循环
        let lastTime = 0;
        function animate(currentTime) {
            const deltaTime = currentTime - lastTime || 0;
            lastTime = currentTime;
            
            if (isPlaying) {
                animationTime += deltaTime * 0.05;
                animation.update(deltaTime);
            }
            
            animation.draw();
            animationId = requestAnimationFrame(animate);
        }
        
        // 启动动画循环
        animate(0);
        
        // UI控制
        document.getElementById('playBtn').addEventListener('click', () => {
            isPlaying = true;
        });
        
        document.getElementById('pauseBtn').addEventListener('click', () => {
            isPlaying = false;
        });
        
        document.getElementById('resetBtn').addEventListener('click', () => {
            animationTime = 0;
            protonGradient = 70;
            atpCount = 0;
            membranePotential = -150;
            animation.init();
            document.getElementById('atpCount').textContent = '0';
            document.getElementById('gradientValue').textContent = '70%';
            document.getElementById('gradientFill').style.width = '70%';
            document.getElementById('membranePotential').textContent = '-150 mV';
        });
        
        // 模式切换
        function setMode(mode) {
            currentMode = mode;
            
            // 更新按钮状态
            document.getElementById('step1Btn').classList.remove('active');
            document.getElementById('step2Btn').classList.remove('active');
            document.getElementById('step3Btn').classList.remove('active');
            document.getElementById('fullProcessBtn').classList.remove('active');
            
            document.getElementById(mode + 'Btn').classList.add('active');
            
            // 重置动画时间
            animationTime = 0;
            animation.init();
        }
        
        document.getElementById('step1Btn').addEventListener('click', () => setMode('step1'));
        document.getElementById('step2Btn').addEventListener('click', () => setMode('step2'));
        document.getElementById('step3Btn').addEventListener('click', () => setMode('step3'));
        document.getElementById('fullProcessBtn').addEventListener('click', () => setMode('full'));
        
        // NADH浓度滑块
        const nadhSlider = document.getElementById('nadhSlider');
        const nadhValue = document.getElementById('nadhValue');
        
        nadhSlider.addEventListener('input', function() {
            nadhConcentration = parseInt(this.value);
            nadhValue.textContent = nadhConcentration;
        });
        
        // 解偶联剂开关
        const uncouplerToggle = document.getElementById('uncouplerToggle');
        const uncouplerStatus = document.getElementById('uncouplerStatus');
        
        uncouplerToggle.addEventListener('change', function() {
            isUncouplerActive = this.checked;
            uncouplerStatus.textContent = isUncouplerActive ? '开' : '关';
            
            if (isUncouplerActive) {
                uncouplerStatus.style.color = '#e74c3c';
            } else {
                uncouplerStatus.style.color = '#f1c40f';
            }
        });
        
        // 添加Canvas点击交互
        canvas.addEventListener('click', function(event) {
            const rect = canvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;
            
            // 检查是否点击了复合物
            for (let complex of animation.complexes) {
                if (x > complex.x - complex.width/2 && x < complex.x + complex.width/2 &&
                    y > complex.y - complex.height/2 && y < complex.y + complex.height/2) {
                    
                    alert(`${complex.name}\n功能: ${complex.protons > 0 ? 
                        `传递电子并泵送${complex.protons}个质子(H⁺)到膜间隙` : 
                        '传递电子但不泵送质子'}`);
                    return;
                }
            }
            
            // 检查是否点击了ATP合酶
            const synth = animation.atpSynthase;
            if (x > synth.x - 30 && x < synth.x + 30 &&
                y > synth.y - 50 && y < synth.y + 50) {
                
                alert('ATP合酶\n功能: 利用质子(H⁺)回流驱动力，催化ADP和Pi合成ATP\n结构: F0质子通道 + F1催化头');
                return;
            }
        });
        
        // 添加键盘控制
        document.addEventListener('keydown', function(event) {
            switch(event.key) {
                case ' ':
                    // 空格键切换播放/暂停
                    isPlaying = !isPlaying;
                    event.preventDefault();
                    break;
                case '1':
                    setMode('step1');
                    break;
                case '2':
                    setMode('step2');
                    break;
                case '3':
                    setMode('step3');
                    break;
                case '4':
                    setMode('full');
                    break;
                case 'r':
                case 'R':
                    // R键重置
                    animationTime = 0;
                    protonGradient = 70;
                    atpCount = 0;
                    membranePotential = -150;
                    animation.init();
                    document.getElementById('atpCount').textContent = '0';
                    document.getElementById('gradientValue').textContent = '70%';
                    document.getElementById('gradientFill').style.width = '70%';
                    document.getElementById('membranePotential').textContent = '-150 mV';
                    break;
            }
        });
        
        // 添加使用说明提示
        setTimeout(() => {
            alert('欢迎使用细胞呼吸教学动画！\n\n提示：\n1. 使用按钮控制动画进度\n2. 调节NADH浓度观察反应速率变化\n3. 开启解偶联剂观察质子梯度消失\n4. 点击复合物或ATP合酶查看详细信息\n5. 键盘快捷键：空格(播放/暂停) 1-4(切换模式) R(重置)');
        }, 1000);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 细胞呼吸：电子传递与氧化磷酸化 交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在将细胞呼吸中最为核心也最为抽象的“电子传递链”与“氧化磷酸化”过程，通过可视化、动态化、可交互的方式呈现，帮助您深入理解这一生命活动的能量转换枢纽。

---

### 一、 功能说明

本动画模拟了在线粒体内膜（嵴）上发生的完整氧化磷酸化过程。它不仅仅是一个播放动画，更是一个**交互式学习实验室**。您可以：
*   **分步学习**：将复杂过程分解为三个关键步骤和一个完整流程。
*   **实时调控**：通过调节参数（如底物浓度）来观察系统反应。
*   **实验模拟**：开启“解偶联剂”，直观验证理论。
*   **数据可视化**：实时查看质子梯度、膜电位和ATP产量等关键指标。

---

### 二、 主要功能与操作

#### 1. 动画控制区
*   **播放 / 暂停 / 重置**：控制动画的播放流程。重置将恢复所有参数到初始状态。
*   **分步学习模式**：
    *   **步骤1：电子传递**：聚焦于电子（黄色小球）从NADH出发，沿复合物I→III→IV传递至氧气的过程。
    *   **步骤2：建立梯度**：展示电子传递如何驱动质子（粉色小球）被泵出基质，建立跨膜质子梯度。
    *   **步骤3：ATP合成**：展示质子通过ATP合酶回流，驱动其旋转并催化ADP+Pi合成ATP（绿色小球）。
    *   **完整过程**：整合以上所有步骤，展示氧化与磷酸化的动态偶联。

#### 2. 实验模拟区
*   **NADH浓度滑块**：模拟细胞能量状态。向右滑动增加NADH（电子供体）浓度，可观察到电子传递加速、质子泵送更频繁、ATP合成速率提高。
*   **解偶联剂开关**：一个关键的教学实验工具。
    *   **关闭时**：质子只能通过ATP合酶回流，正常合成ATP。
    *   **开启时**：质子“漏回”基质，质子梯度消失。您将观察到：电子传递链“空转”加速（因无反向电化学势阻碍），但ATP合酶停止旋转，**ATP产量归零**。这生动解释了“解偶联”导致产热而非储能的现象。

#### 3. 数据监控区
实时显示三个核心参数，将抽象概念量化：
*   **质子梯度强度**：以百分比和进度条形式展示，是驱动ATP合成的直接动力源。
*   **ATP合成计数**：实时累计已合成的ATP分子数量。
*   **膜电位**：显示内膜两侧的电位差（内侧为负），是质子电化学梯度的重要组成部分。

#### 4. 交互探索
*   **鼠标悬停/点击**：将鼠标移动到**蛋白质复合物（I, II, III, IV）** 或 **ATP合酶** 上，点击即可查看其名称和核心功能简介。
*   **键盘快捷键**：
    *   **空格键**：快速切换播放/暂停。
    *   **数字键 1-4**：快速切换四个学习模式。
    *   **R键**：快速重置动画。

---

### 三、 设计特色与教学要点

#### 设计特色
1.  **科学的视觉隐喻**：
    *   **电子**（黄色）：高能粒子，流动代表能量释放。
    *   **质子**（粉色）：能量载体，其跨膜运动建立梯度。
    *   **ATP合酶旋转**：将质子回流的渗透能转化为机械能，再转化为ATP中的化学能，这是动画的视觉高潮。
    *   **颜色编码**：所有组件（基质、膜、分子）采用统一配色，便于识别和记忆。

2.  **结构与功能统一**：动画在线粒体**内膜嵴**的横截面场景中展开，直观展示了嵴的结构如何极大地增加了膜面积，从而容纳更多的电子传递链和ATP合酶，提升了能量转换效率。

3.  **“黑箱”与细节平衡**：简化了每个复合物内部的复杂化学反应，但突出了**醌（Q）** 和**细胞色素c（Cyt c）** 作为移动电子载体的作用，以及ATP合酶**F0转子**和**F1催化头**的协同旋转机制。

#### 核心教学要点
引导学习者关注以下能量转换链条，这是理解氧化磷酸化的关键：
> **还原力（NADH）的化学能** → **电子传递** → **质子电化学梯度（渗透能+电能）** → **ATP合酶机械旋转（机械能）** → **ATP高能磷酸键（化学能）**

**关键提问**：
1.  电子传递的能量去哪里了？（答：用于建立质子梯度）。
2.  质子梯度包含哪两种形式的能量？（答：浓度差产生的化学渗透势和电荷差产生的膜电位）。
3.  ATP合酶是如何工作的？（答：质子回流驱动F0单元旋转，通过柄将扭矩传递给F1单元，改变其构象催化ATP合成）。

---

### 四、 使用建议

#### 对于学习者（学生）：
1.  **首次观看**：建议按顺序（步骤1→2→3→完整）使用“分步学习模式”，每步使用“暂停”按钮仔细观察粒子的流动和结构的变化。
2.  **主动探索**：
    *   先观察“完整过程”，形成一个整体印象。
    *   然后，**调高NADH浓度**，看看整个系统的运行速率如何变化。
    *   最后，**开启解偶联剂**，与正常状态对比，深刻理解“偶联”的意义。
3.  **自我测试**：在不看动画的情况下，尝试画出过程简图并复述。然后打开动画验证和修正。

#### 对于教学者（教师）：
1.  **课堂演示**：可将本动画作为核心可视化工具，在讲解时同步操作。特别是在讲解“解偶联”作用机制时，开关的对比效果极具说服力。
2.  **提出探究性问题**：
    *   “如果复合物IV被抑制，哪些指标会首先发生变化？”
    *   “为什么说质子梯度是‘能量货币’？”
    *   “比较NADH和FADH2进入电子传递链的差异（提示：观察复合物II）。”
3.  **结合实验**：可与“探究影响细胞呼吸因素”的实际实验（如使用DNP解偶联剂）相结合，虚实对照，加深理解。

---

**总结**：本动画将教科书上静态的图表和复杂的文字描述，转化为一个动态、可操控的微观世界。我们鼓励您以“探索者”而非“观看者”的身份来使用它，通过交互和实验，亲手揭示细胞呼吸的能量奥秘。

祝您探索愉快，学有所获！