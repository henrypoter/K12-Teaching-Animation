# 需求：光合作用全过程（叶绿体双层膜+光反应在类囊体薄膜、暗反应在基质）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为中学生或生物学入门者。他们需要理解光合作用这一复杂生物过程的整体框架、关键步骤和发生场所。
2.  **核心痛点**：
    *   **空间抽象**：学生难以在脑海中构建叶绿体（双层膜）、类囊体（薄膜堆叠）、基质（液态空间）的三维空间关系。
    *   **过程割裂**：容易将光反应和暗反应视为两个独立事件，不理解两者在物质（ATP、NADPH）和能量上的紧密耦合关系。
    *   **动态理解困难**：教科书上的静态图难以展示电子传递、分子合成与转运的动态过程。
3.  **学习目标**：
    *   **知识层面**：清晰掌握光反应（水的光解、ATP与NADPH的生成）和暗反应（卡尔文循环、碳的固定与还原）的关键步骤。
    *   **空间层面**：明确各步骤在叶绿体亚显微结构（类囊体膜、基质）中的具体位置。
    *   **关系层面**：理解光反应为暗反应提供能量（ATP）和还原力（NADPH），暗反应消耗它们并产生有机物，构成一个完整循环。

#### 教学设计思路
1.  **核心概念**：围绕 **“能量转换”**（光能 → 化学能）和 **“空间分工”**（类囊体膜 vs. 基质）两条主线展开。
2.  **认知规律（三步引导）**：
    *   **第一步：宏观定位**。首先展示植物细胞中的叶绿体，然后“聚焦”进入叶绿体内部，展示其双层膜结构、类囊体堆叠形成基粒、以及充满基质的空间。建立整体空间认知。
    *   **第二步：分步详解**。
        *   **光反应**：在类囊体膜上动态演示光子激发叶绿素、水的光解（释放O₂和H⁺）、电子传递链（伴随H⁺泵入类囊体内腔形成浓度梯度）、ATP合酶工作合成ATP、以及NADP⁺被还原为NADPH。
        *   **暗反应**：在基质中动态演示CO₂被固定（与RuBP结合）、形成的不稳定分子分解、在ATP和NADPH的驱动下被还原成三碳糖（如G3P）、以及RuBP的再生循环。
    *   **第三步：动态整合**。以“一个碳原子（来自CO₂）的旅程”或“一分子ATP的生成与消耗”为线索，将两个反应动态串联起来，展示物质与能量的流动闭环。
3.  **交互设计**：
    *   **层级控制**：提供“总览”、“光反应”、“暗反应”、“完整循环”四个模式按钮，允许用户按需学习。
    *   **过程控制**：每个模式内提供“播放/暂停”、“步进/步退”按钮，让用户能以自己的节奏观察。
    *   **焦点提示**：当鼠标悬停在关键分子（如H₂O, CO₂, ATP）或结构（如类囊体膜、ATP合酶）上时，高亮显示并出现简要说明标签。
    *   **示意图切换**：在暗反应部分，可提供“分子结构简图”和“循环流程图”两种视图切换，满足不同抽象层次的理解需求。
4.  **视觉呈现**：
    *   **风格**：采用扁平化、卡通化的科学插图风格，在保证科学准确性的前提下，简化细节，突出关键结构和过程。
    *   **动态表现**：
        *   用闪烁的黄色光点表示“光子”。
        *   用流动的彩色小球（如蓝色-H₂O，红色-O₂，灰色-CO₂，绿色-糖）表示分子。
        *   用沿着路径移动的“电子”图标表示电子传递。
        *   用动态的“齿轮”或“旋转”图标表示ATP合酶和酶的催化作用。
        *   用颜色深浅或粒子密度表示H⁺浓度梯度。

#### 配色方案选择
*   **背景与结构色**：
    *   **叶绿体外膜/内膜**：淡绿色（#E8F5E9）到稍深的绿色（#C8E6C9），体现生物膜质感。
    *   **类囊体膜/基粒**：鲜明的翠绿色（#4CAF50），突出其作为反应场所的核心地位。
    *   **基质**：半透明的淡黄色（#FFF9C4），模拟液态胶状环境，与膜结构形成对比。
*   **分子与元素色**（采用化学/生物学常用配色）：
    *   **水 (H₂O)**：蓝色 (#42A5F5)
    *   **氧气 (O₂)**：红色 (#EF5350)
    *   **二氧化碳 (CO₂)**：灰色 (#BDBDBD)
    *   **氢离子 (H⁺)**：粉色 (#F48FB1) 或橙色 (#FF9800)
    *   **ATP**：高亮橙色 (#FFB74D) ，代表“能量货币”。
    *   **NADPH/NADP⁺**：紫色 (#BA68C8)，代表“还原力”。
    *   **糖类 (G3P等)**：深绿色 (#388E3C)
    *   **电子 (e⁻)**：亮黄色 (#FFEB3B)
*   **动态与高亮色**：
    *   **光子/能量流**：亮黄色闪烁 (#FFFF00)
    *   **高亮/选中状态**：醒目的蓝绿色 (#00BCD4)
    *   **文字/标签**：深灰色 (#424242)

#### 交互功能列表
1.  **场景切换按钮**：`总览`、`光反应`、`暗反应`、`完整循环`。
2.  **动画控制按钮**：`播放`、`暂停`、`下一步`、`上一步`、`重置`。
3.  **图例/分子开关**：一个可折叠面板，显示各颜色小球代表的分子，并可选择隐藏/显示特定分子流，以降低视觉复杂度。
4.  **悬停信息提示**：鼠标悬停在任何关键元素上时，显示其名称和简要功能。
5.  **视角缩放与平移**：在“总览”模式下，允许用户拖拽平移和滚轮缩放，探索叶绿体结构。
6.  **步骤指示器**：在分步讲解时，屏幕一侧或底部有一个进度条或步骤列表，显示当前步骤（如“1. 水的光解”），并可点击跳转。
7.  **两种视图（仅暗反应）**：`循环图`（展示卡尔文循环的环形过程）与`简化图`（聚焦于CO₂的固定、还原和产物输出）切换按钮。
8.  **速度调节滑块**：控制动画播放速度。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>光合作用全过程教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        
        header {
            background: linear-gradient(to right, #2E7D32, #4CAF50);
            color: white;
            padding: 25px 30px;
            text-align: center;
        }
        
        h1 {
            font-size: 2.4rem;
            margin-bottom: 10px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.2);
        }
        
        .subtitle {
            font-size: 1.1rem;
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.5;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            padding: 20px;
            gap: 20px;
        }
        
        .animation-section {
            flex: 3;
            min-width: 300px;
            background-color: #f9f9f9;
            border-radius: 10px;
            padding: 15px;
            box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.05);
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #f0f8ff;
            border-radius: 8px;
            overflow: hidden;
            border: 2px solid #ddd;
        }
        
        #animationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .controls-section {
            flex: 1;
            min-width: 250px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .control-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 1px solid #e0e0e0;
        }
        
        h2 {
            color: #2E7D32;
            font-size: 1.4rem;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #E8F5E9;
        }
        
        .scene-buttons {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .scene-btn {
            padding: 12px 8px;
            background-color: #f1f8e9;
            border: 2px solid #C8E6C9;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            color: #2E7D32;
            transition: all 0.3s;
            text-align: center;
        }
        
        .scene-btn:hover {
            background-color: #E8F5E9;
            transform: translateY(-2px);
        }
        
        .scene-btn.active {
            background-color: #4CAF50;
            color: white;
            border-color: #2E7D32;
            box-shadow: 0 4px 8px rgba(76, 175, 80, 0.3);
        }
        
        .animation-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .control-btn {
            flex: 1;
            min-width: 80px;
            padding: 10px 5px;
            background-color: #2196F3;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .control-btn:hover {
            background-color: #1976D2;
            transform: translateY(-2px);
        }
        
        .control-btn:active {
            transform: translateY(0);
        }
        
        .control-btn.reset {
            background-color: #FF9800;
        }
        
        .control-btn.reset:hover {
            background-color: #F57C00;
        }
        
        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 10px;
        }
        
        .speed-slider {
            flex: 1;
        }
        
        .legend {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
            border: 1px solid rgba(0, 0, 0, 0.1);
        }
        
        .info-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 1px solid #e0e0e0;
            margin-top: 10px;
        }
        
        .step-indicator {
            font-size: 1.1rem;
            font-weight: 600;
            color: #2E7D32;
            margin-bottom: 10px;
        }
        
        .step-description {
            line-height: 1.6;
            color: #555;
            font-size: 0.95rem;
        }
        
        .hint {
            background-color: #E3F2FD;
            border-left: 4px solid #2196F3;
            padding: 12px;
            margin-top: 15px;
            border-radius: 0 8px 8px 0;
            font-size: 0.9rem;
            color: #1565C0;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: #666;
            font-size: 0.9rem;
            border-top: 1px solid #eee;
            background-color: #f9f9f9;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .canvas-container {
                height: 400px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>光合作用全过程教学动画</h1>
            <p class="subtitle">探索叶绿体中的能量转换：光反应（类囊体薄膜）与暗反应（基质）的动态过程</p>
        </header>
        
        <div class="main-content">
            <section class="animation-section">
                <div class="canvas-container">
                    <canvas id="animationCanvas"></canvas>
                </div>
            </section>
            
            <section class="controls-section">
                <div class="control-panel">
                    <h2>场景选择</h2>
                    <div class="scene-buttons">
                        <button class="scene-btn active" data-scene="overview">总览</button>
                        <button class="scene-btn" data-scene="light">光反应</button>
                        <button class="scene-btn" data-scene="dark">暗反应</button>
                        <button class="scene-btn" data-scene="full">完整循环</button>
                    </div>
                    
                    <h2>动画控制</h2>
                    <div class="animation-controls">
                        <button class="control-btn" id="playBtn">播放</button>
                        <button class="control-btn" id="pauseBtn">暂停</button>
                        <button class="control-btn" id="stepBtn">下一步</button>
                        <button class="control-btn reset" id="resetBtn">重置</button>
                    </div>
                    
                    <div class="speed-control">
                        <span>速度:</span>
                        <input type="range" min="1" max="10" value="5" class="speed-slider" id="speedSlider">
                    </div>
                </div>
                
                <div class="control-panel">
                    <h2>分子图例</h2>
                    <div class="legend">
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #42A5F5;"></div>
                            <span>水 (H₂O)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #EF5350;"></div>
                            <span>氧气 (O₂)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #BDBDBD;"></div>
                            <span>二氧化碳 (CO₂)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #FFB74D;"></div>
                            <span>ATP (能量)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #BA68C8;"></div>
                            <span>NADPH (还原力)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #388E3C;"></div>
                            <span>糖类 (G3P)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #F48FB1;"></div>
                            <span>氢离子 (H⁺)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #FFEB3B;"></div>
                            <span>电子 (e⁻)</span>
                        </div>
                    </div>
                </div>
                
                <div class="info-panel">
                    <div class="step-indicator" id="stepTitle">叶绿体结构总览</div>
                    <div class="step-description" id="stepDescription">
                        这是植物细胞中的叶绿体。外部是双层膜结构，内部有类囊体堆叠形成的基粒，以及充满基质的液态空间。光反应发生在类囊体薄膜上，暗反应发生在基质中。
                    </div>
                    <div class="hint">
                        💡 提示：将鼠标悬停在动画中的元素上，可以查看其名称和功能。
                    </div>
                </div>
            </section>
        </div>
        
        <footer>
            <p>光合作用教学动画 | 设计：教育技术专家 | 本动画用于教学演示目的</p>
        </footer>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        
        // 初始调整尺寸
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 动画状态
        let animationState = {
            currentScene: 'overview', // overview, light, dark, full
            isPlaying: false,
            animationSpeed: 5, // 1-10
            step: 0,
            time: 0,
            hoveredElement: null
        };
        
        // 场景数据
        const scenes = {
            overview: {
                steps: 1,
                title: "叶绿体结构总览",
                description: "这是植物细胞中的叶绿体。外部是双层膜结构，内部有类囊体堆叠形成的基粒，以及充满基质的液态空间。光反应发生在类囊体薄膜上，暗反应发生在基质中。"
            },
            light: {
                steps: 6,
                titles: [
                    "光子激发叶绿素",
                    "水的光解",
                    "电子传递与H⁺泵送",
                    "ATP合成",
                    "NADPH生成",
                    "光反应产物总结"
                ],
                descriptions: [
                    "光子（黄色光点）被类囊体膜上的叶绿素分子吸收，激发电子。",
                    "水分子在光系统II处被分解，释放氧气（O₂）和氢离子（H⁺），并提供电子。",
                    "电子沿着电子传递链移动，能量用于将H⁺泵入类囊体内腔，形成浓度梯度。",
                    "H⁺通过ATP合酶顺浓度梯度流出，驱动ATP的合成。",
                    "电子最终传递给NADP⁺，结合H⁺形成NADPH（还原力）。",
                    "光反应产生ATP（能量货币）和NADPH（还原力），并释放氧气。这些产物将用于暗反应。"
                ]
            },
            dark: {
                steps: 5,
                titles: [
                    "CO₂的固定",
                    "三碳化合物的形成",
                    "三碳化合物的还原",
                    "糖分子的生成",
                    "RuBP的再生"
                ],
                descriptions: [
                    "二氧化碳（CO₂）进入叶绿体基质，与RuBP（五碳化合物）结合，形成不稳定的六碳化合物。",
                    "不稳定的六碳化合物迅速分解为两个三碳化合物（3-磷酸甘油酸）。",
                    "在ATP和NADPH的驱动下，三碳化合物被还原为三碳糖（3-磷酸甘油醛，G3P）。",
                    "部分G3P输出用于合成葡萄糖等有机物，其余用于再生RuBP。",
                    "通过一系列反应，剩余的G3P在消耗ATP的情况下，重新生成RuBP，维持卡尔文循环。"
                ]
            },
            full: {
                steps: 1,
                title: "光合作用完整循环",
                description: "光反应和暗反应协同工作：光反应在类囊体膜上捕获光能，产生ATP和NADPH；暗反应在基质中利用这些产物将CO₂固定并还原为有机物。两者构成能量与物质的完整循环。"
            }
        };
        
        // 颜色定义
        const colors = {
            chloroplastOuter: '#E8F5E9',
            chloroplastInner: '#C8E6C9',
            thylakoid: '#4CAF50',
            stroma: 'rgba(255, 249, 196, 0.7)',
            water: '#42A5F5',
            oxygen: '#EF5350',
            co2: '#BDBDBD',
            atp: '#FFB74D',
            nadph: '#BA68C8',
            sugar: '#388E3C',
            proton: '#F48FB1',
            electron: '#FFEB3B',
            photon: '#FFFF00',
            highlight: '#00BCD4',
            text: '#424242'
        };
        
        // 动画元素
        let animationElements = [];
        
        // 初始化动画元素
        function initAnimationElements() {
            animationElements = [];
            
            // 根据当前场景创建不同的元素
            if (animationState.currentScene === 'overview') {
                // 叶绿体
                animationElements.push({
                    type: 'chloroplast',
                    x: canvas.width / 2,
                    y: canvas.height / 2,
                    width: Math.min(canvas.width, canvas.height) * 0.7,
                    height: Math.min(canvas.width, canvas.height) * 0.5,
                    label: '叶绿体',
                    description: '光合作用的场所，具有双层膜结构'
                });
                
                // 类囊体/基粒
                for (let i = 0; i < 5; i++) {
                    animationElements.push({
                        type: 'thylakoid',
                        x: canvas.width / 2 - 100 + i * 50,
                        y: canvas.height / 2 - 30,
                        width: 40,
                        height: 60,
                        label: '类囊体（基粒）',
                        description: '光反应的场所，含有叶绿素和电子传递链'
                    });
                }
                
                // 基质
                animationElements.push({
                    type: 'stroma',
                    x: canvas.width / 2,
                    y: canvas.height / 2,
                    width: Math.min(canvas.width, canvas.height) * 0.65,
                    height: Math.min(canvas.width, canvas.height) * 0.45,
                    label: '基质',
                    description: '暗反应（卡尔文循环）的场所，含有多种酶'
                });
                
            } else if (animationState.currentScene === 'light') {
                // 类囊体膜
                animationElements.push({
                    type: 'thylakoidMembrane',
                    x: canvas.width / 2,
                    y: canvas.height / 2,
                    width: 300,
                    height: 100,
                    label: '类囊体膜',
                    description: '光反应发生的场所'
                });
                
                // 根据步骤添加动态元素
                if (animationState.step >= 0) {
                    // 光子
                    for (let i = 0; i < 5; i++) {
                        animationElements.push({
                            type: 'photon',
                            x: canvas.width / 2 - 150 + i * 60,
                            y: canvas.height / 2 - 80,
                            radius: 8,
                            phase: i * 0.5,
                            label: '光子',
                            description: '光能的基本单位，激发叶绿素中的电子'
                        });
                    }
                }
                
                if (animationState.step >= 1) {
                    // 水分子
                    animationElements.push({
                        type: 'water',
                        x: canvas.width / 2 - 180,
                        y: canvas.height / 2,
                        radius: 12,
                        label: '水分子 (H₂O)',
                        description: '在光系统II处被光解，提供电子和质子'
                    });
                    
                    // 氧气
                    for (let i = 0; i < 3; i++) {
                        animationElements.push({
                            type: 'oxygen',
                            x: canvas.width / 2 - 180 + i * 15,
                            y: canvas.height / 2 - 50 - i * 5,
                            radius: 10,
                            phase: i * 0.3,
                            label: '氧气 (O₂)',
                            description: '光合作用的副产物，释放到大气中'
                        });
                    }
                }
                
                if (animationState.step >= 2) {
                    // 电子传递链
                    animationElements.push({
                        type: 'electronChain',
                        x: canvas.width / 2 - 100,
                        y: canvas.height / 2,
                        length: 200,
                        label: '电子传递链',
                        description: '传递电子，将能量用于泵送H⁺'
                    });
                    
                    // H+ 泵送
                    for (let i = 0; i < 8; i++) {
                        animationElements.push({
                            type: 'proton',
                            x: canvas.width / 2 - 80 + i * 20,
                            y: canvas.height / 2 + 30,
                            radius: 8,
                            phase: i * 0.4,
                            direction: 'in',
                            label: '氢离子 (H⁺)',
                            description: '被泵入类囊体内腔，形成浓度梯度'
                        });
                    }
                }
                
                if (animationState.step >= 3) {
                    // ATP合酶
                    animationElements.push({
                        type: 'atpSynthase',
                        x: canvas.width / 2 + 120,
                        y: canvas.height / 2,
                        width: 40,
                        height: 60,
                        label: 'ATP合酶',
                        description: '利用H⁺浓度梯度合成ATP'
                    });
                    
                    // ATP分子
                    for (let i = 0; i < 3; i++) {
                        animationElements.push({
                            type: 'atp',
                            x: canvas.width / 2 + 140 + i * 25,
                            y: canvas.height / 2 - 30 - i * 5,
                            radius: 12,
                            phase: i * 0.5,
                            label: 'ATP',
                            description: '能量货币，为暗反应提供能量'
                        });
                    }
                }
                
                if (animationState.step >= 4) {
                    // NADPH
                    animationElements.push({
                        type: 'nadph',
                        x: canvas.width / 2 + 180,
                        y: canvas.height / 2 + 20,
                        radius: 12,
                        label: 'NADPH',
                        description: '还原力，为暗反应提供还原能力'
                    });
                }
                
            } else if (animationState.currentScene === 'dark') {
                // 基质背景
                animationElements.push({
                    type: 'stromaBackground',
                    x: canvas.width / 2,
                    y: canvas.height / 2,
                    width: canvas.width * 0.8,
                    height: canvas.height * 0.7,
                    label: '基质',
                    description: '暗反应发生的液态环境'
                });
                
                // 卡尔文循环
                animationElements.push({
                    type: 'calvinCycle',
                    x: canvas.width / 2,
                    y: canvas.height / 2,
                    radius: 120,
                    label: '卡尔文循环',
                    description: '暗反应的核心过程，固定CO₂并合成糖类'
                });
                
                if (animationState.step >= 0) {
                    // CO2分子
                    animationElements.push({
                        type: 'co2',
                        x: canvas.width / 2 - 200,
                        y: canvas.height / 2,
                        radius: 12,
                        label: '二氧化碳 (CO₂)',
                        description: '从大气中吸收，用于碳固定'
                    });
                    
                    // RuBP
                    animationElements.push({
                        type: 'rubp',
                        x: canvas.width / 2,
                        y: canvas.height / 2 - 120,
                        radius: 15,
                        label: 'RuBP (五碳化合物)',
                        description: '二氧化碳的受体分子'
                    });
                }
                
                if (animationState.step >= 1) {
                    // 3-磷酸甘油酸
                    for (let i = 0; i < 2; i++) {
                        animationElements.push({
                            type: 'pga',
                            x: canvas.width / 2 + (i === 0 ? -60 : 60),
                            y: canvas.height / 2 + 30,
                            radius: 12,
                            label: '3-磷酸甘油酸',
                            description: 'CO₂固定后形成的三碳化合物'
                        });
                    }
                }
                
                if (animationState.step >= 2) {
                    // ATP和NADPH输入
                    animationElements.push({
                        type: 'atpInput',
                        x: canvas.width / 2 - 150,
                        y: canvas.height / 2 + 100,
                        radius: 12,
                        label: 'ATP',
                        description: '来自光反应，提供能量'
                    });
                    
                    animationElements.push({
                        type: 'nadphInput',
                        x: canvas.width / 2 + 150,
                        y: canvas.height / 2 + 100,
                        radius: 12,
                        label: 'NADPH',
                        description: '来自光反应，提供还原力'
                    });
                }
                
                if (animationState.step >= 3) {
                    // G3P输出
                    animationElements.push({
                        type: 'g3p',
                        x: canvas.width / 2,
                        y: canvas.height / 2 + 150,
                        radius: 14,
                        label: 'G3P (三碳糖)',
                        description: '卡尔文循环的产物，用于合成葡萄糖'
                    });
                }
                
                if (animationState.step >= 4) {
                    // RuBP再生
                    animationElements.push({
                        type: 'rubpRegen',
                        x: canvas.width / 2,
                        y: canvas.height / 2 - 120,
                        radius: 15,
                        label: 'RuBP再生',
                        description: '部分G3P用于重新生成RuBP，维持循环'
                    });
                }
                
            } else if (animationState.currentScene === 'full') {
                // 完整循环：结合光反应和暗反应
                // 类囊体部分
                animationElements.push({
                    type: 'thylakoidSection',
                    x: canvas.width / 2 - 150,
                    y: canvas.height / 2,
                    width: 200,
                    height: 150,
                    label: '类囊体膜（光反应）',
                    description: '捕获光能，产生ATP和NADPH'
                });
                
                // 基质部分
                animationElements.push({
                    type: 'stromaSection',
                    x: canvas.width / 2 + 150,
                    y: canvas.height / 2,
                    width: 200,
                    height: 150,
                    label: '基质（暗反应）',
                    description: '利用ATP和NADPH将CO₂转化为糖类'
                });
                
                // 物质流动
                // ATP从类囊体流向基质
                for (let i = 0; i < 3; i++) {
                    animationElements.push({
                        type: 'atpFlow',
                        x: canvas.width / 2 - 50 + i * 20,
                        y: canvas.height / 2 - 20,
                        radius: 10,
                        phase: i * 0.3,
                        label: 'ATP流动',
                        description: '光反应产生的ATP用于驱动暗反应'
                    });
                }
                
                // NADPH从类囊体流向基质
                for (let i = 0; i < 3; i++) {
                    animationElements.push({
                        type: 'nadphFlow',
                        x: canvas.width / 2 - 50 + i * 20,
                        y: canvas.height / 2 + 20,
                        radius: 10,
                        phase: i * 0.5,
                        label: 'NADPH流动',
                        description: '光反应产生的NADPH用于还原CO₂'
                    });
                }
                
                // CO2进入基质
                animationElements.push({
                    type: 'co2Flow',
                    x: canvas.width / 2 + 50,
                    y: canvas.height / 2 + 60,
                    radius: 10,
                    phase: 0,
                    label: 'CO₂输入',
                    description: '从大气进入叶绿体基质'
                });
                
                // 糖类输出
                animationElements.push({
                    type: 'sugarOutput',
                    x: canvas.width / 2 + 250,
                    y: canvas.height / 2,
                    radius: 12,
                    phase: 0,
                    label: '糖类输出',
                    description: '光合作用最终产物，用于植物生长'
                });
            }
        }
        
        // 绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制所有动画元素
            animationElements.forEach(element => {
                drawElement(element);
            });
            
            // 绘制悬停提示
            if (animationState.hoveredElement) {
                drawTooltip(animationState.hoveredElement);
            }
            
            // 更新时间
            if (animationState.isPlaying) {
                animationState.time += 0.05 * animationState.animationSpeed;
            }
        }
        
        // 绘制单个元素
        function drawElement(element) {
            ctx.save();
            
            // 根据元素类型绘制
            switch (element.type) {
                case 'chloroplast':
                    // 绘制叶绿体外膜
                    ctx.strokeStyle = colors.chloroplastOuter;
                    ctx.lineWidth = 8;
                    ctx.beginPath();
                    ctx.ellipse(element.x, element.y, element.width/2, element.height/2, 0, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    // 绘制叶绿体内膜
                    ctx.strokeStyle = colors.chloroplastInner;
                    ctx.lineWidth = 6;
                    ctx.beginPath();
                    ctx.ellipse(element.x, element.y, element.width/2 - 10, element.height/2 - 10, 0, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 16px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - element.height/2 - 20);
                    }
                    break;
                    
                case 'thylakoid':
                    // 绘制类囊体（基粒）
                    ctx.fillStyle = colors.thylakoid;
                    ctx.fillRect(element.x - element.width/2, element.y - element.height/2, element.width, element.height);
                    
                    // 绘制类囊体膜
                    ctx.strokeStyle = '#2E7D32';
                    ctx.lineWidth = 2;
                    ctx.strokeRect(element.x - element.width/2, element.y - element.height/2, element.width, element.height);
                    
                    // 绘制内部条纹（表示膜结构）
                    for (let i = 0; i < 3; i++) {
                        ctx.beginPath();
                        ctx.moveTo(element.x - element.width/2 + 5, element.y - element.height/2 + 10 + i*15);
                        ctx.lineTo(element.x + element.width/2 - 5, element.y - element.height/2 + 10 + i*15);
                        ctx.strokeStyle = '#1B5E20';
                        ctx.lineWidth = 1;
                        ctx.stroke();
                    }
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - element.height/2 - 15);
                    }
                    break;
                    
                case 'stroma':
                    // 绘制基质
                    ctx.fillStyle = colors.stroma;
                    ctx.beginPath();
                    ctx.ellipse(element.x, element.y, element.width/2 - 20, element.height/2 - 20, 0, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 16px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y + element.height/2 + 30);
                    }
                    break;
                    
                case 'thylakoidMembrane':
                    // 绘制类囊体膜（光反应场景）
                    ctx.fillStyle = colors.thylakoid;
                    ctx.fillRect(element.x - element.width/2, element.y - element.height/2, element.width, element.height);
                    
                    // 绘制膜细节
                    ctx.strokeStyle = '#1B5E20';
                    ctx.lineWidth = 2;
                    ctx.strokeRect(element.x - element.width/2, element.y - element.height/2, element.width, element.height);
                    
                    // 绘制内部膜蛋白示意
                    for (let i = 0; i < 5; i++) {
                        const proteinX = element.x - element.width/2 + 40 + i * 60;
                        ctx.fillStyle = '#8BC34A';
                        ctx.beginPath();
                        ctx.arc(proteinX, element.y, 15, 0, Math.PI * 2);
                        ctx.fill();
                        
                        ctx.fillStyle = '#1B5E20';
                        ctx.font = '12px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('PS', proteinX, element.y + 4);
                    }
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 16px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - element.height/2 - 20);
                    }
                    break;
                    
                case 'photon':
                    // 绘制光子
                    const pulse = Math.sin(animationState.time + element.phase) * 0.3 + 0.7;
                    ctx.fillStyle = colors.photon;
                    ctx.globalAlpha = pulse;
                    ctx.beginPath();
                    ctx.arc(element.x, element.y + Math.sin(animationState.time + element.phase) * 10, element.radius * pulse, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 绘制光线条
                    ctx.beginPath();
                    ctx.moveTo(element.x, element.y - 50);
                    ctx.lineTo(element.x, element.y - element.radius);
                    ctx.strokeStyle = colors.photon;
                    ctx.lineWidth = 2;
                    ctx.globalAlpha = pulse * 0.5;
                    ctx.stroke();
                    
                    ctx.globalAlpha = 1.0;
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - element.radius - 20);
                    }
                    break;
                    
                case 'water':
                    // 绘制水分子
                    ctx.fillStyle = colors.water;
                    ctx.beginPath();
                    ctx.arc(element.x, element.y, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('H₂O', element.x, element.y + 4);
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - element.radius - 20);
                    }
                    break;
                    
                case 'oxygen':
                    // 绘制氧气分子
                    const o2Y = element.y + Math.sin(animationState.time + element.phase) * 5;
                    ctx.fillStyle = colors.oxygen;
                    ctx.beginPath();
                    ctx.arc(element.x, o2Y, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('O₂', element.x, o2Y + 4);
                    
                    // 绘制上升气泡效果
                    if (animationState.step >= 1 && animationState.currentScene === 'light') {
                        ctx.beginPath();
                        ctx.arc(element.x, o2Y - element.radius - 5, 3, 0, Math.PI * 2);
                        ctx.fillStyle = colors.oxygen;
                        ctx.globalAlpha = 0.7;
                        ctx.fill();
                        ctx.globalAlpha = 1.0;
                    }
                    break;
                    
                case 'electronChain':
                    // 绘制电子传递链
                    ctx.strokeStyle = '#FFC107';
                    ctx.lineWidth = 3;
                    ctx.setLineDash([5, 5]);
                    ctx.beginPath();
                    ctx.moveTo(element.x - element.length/2, element.y);
                    ctx.lineTo(element.x + element.length/2, element.y);
                    ctx.stroke();
                    ctx.setLineDash([]);
                    
                    // 绘制电子在传递链上移动
                    const electronX = element
<!--检测到代码截断，自动续写中...-->
.x - element.length/2 + (animationState.time % 1) * element.length;
                    ctx.fillStyle = colors.electron;
                    ctx.beginPath();
                    ctx.arc(electronX, element.y, 8, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - 30);
                    }
                    break;
                    
                case 'proton':
                    // 绘制氢离子
                    const protonY = element.y + Math.sin(animationState.time + element.phase) * 10;
                    ctx.fillStyle = colors.proton;
                    ctx.beginPath();
                    ctx.arc(element.x, protonY, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('H⁺', element.x, protonY + 4);
                    
                    // 绘制移动方向
                    if (element.direction === 'in') {
                        ctx.beginPath();
                        ctx.moveTo(element.x, protonY - element.radius - 5);
                        ctx.lineTo(element.x - 5, protonY - element.radius - 10);
                        ctx.lineTo(element.x + 5, protonY - element.radius - 10);
                        ctx.closePath();
                        ctx.fillStyle = colors.proton;
                        ctx.fill();
                    }
                    break;
                    
                case 'atpSynthase':
                    // 绘制ATP合酶
                    ctx.fillStyle = '#795548';
                    ctx.fillRect(element.x - element.width/2, element.y - element.height/2, element.width, element.height);
                    
                    // 绘制旋转部分
                    ctx.save();
                    ctx.translate(element.x, element.y);
                    ctx.rotate(animationState.time * 2);
                    ctx.fillStyle = '#5D4037';
                    ctx.beginPath();
                    ctx.moveTo(0, -20);
                    ctx.lineTo(10, 10);
                    ctx.lineTo(-10, 10);
                    ctx.closePath();
                    ctx.fill();
                    ctx.restore();
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - element.height/2 - 15);
                    }
                    break;
                    
                case 'atp':
                    // 绘制ATP分子
                    const atpY = element.y + Math.sin(animationState.time + element.phase) * 5;
                    ctx.fillStyle = colors.atp;
                    ctx.beginPath();
                    ctx.arc(element.x, atpY, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('ATP', element.x, atpY + 4);
                    break;
                    
                case 'nadph':
                    // 绘制NADPH分子
                    ctx.fillStyle = colors.nadph;
                    ctx.beginPath();
                    ctx.arc(element.x, element.y, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 10px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('NADPH', element.x, element.y + 4);
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - element.radius - 20);
                    }
                    break;
                    
                case 'stromaBackground':
                    // 绘制基质背景
                    ctx.fillStyle = colors.stroma;
                    ctx.fillRect(element.x - element.width/2, element.y - element.height/2, element.width, element.height);
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 16px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - element.height/2 - 20);
                    }
                    break;
                    
                case 'calvinCycle':
                    // 绘制卡尔文循环
                    ctx.strokeStyle = '#388E3C';
                    ctx.lineWidth = 3;
                    ctx.beginPath();
                    ctx.arc(element.x, element.y, element.radius, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    // 绘制循环箭头
                    ctx.fillStyle = '#388E3C';
                    ctx.beginPath();
                    ctx.moveTo(element.x + element.radius, element.y);
                    ctx.lineTo(element.x + element.radius - 15, element.y - 10);
                    ctx.lineTo(element.x + element.radius - 15, element.y + 10);
                    ctx.closePath();
                    ctx.fill();
                    
                    ctx.fillStyle = '#388E3C';
                    ctx.font = 'bold 16px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('卡尔文循环', element.x, element.y);
                    
                    // 绘制标签
                    if (isElementHovered(element)) {
                        ctx.fillStyle = colors.highlight;
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(element.label, element.x, element.y - element.radius - 20);
                    }
                    break;
                    
                case 'co2':
                    // 绘制二氧化碳分子
                    ctx.fillStyle = colors.co2;
                    ctx.beginPath();
                    ctx.arc(element.x, element.y, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('CO₂', element.x, element.y + 4);
                    
                    // 绘制移动动画
                    if (animationState.step >= 0 && animationState.currentScene === 'dark') {
                        const moveX = element.x + Math.sin(animationState.time) * 20;
                        ctx.beginPath();
                        ctx.arc(moveX, element.y, element.radius, 0, Math.PI * 2);
                        ctx.fill();
                        
                        ctx.fillStyle = 'white';
                        ctx.font = 'bold 12px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('CO₂', moveX, element.y + 4);
                    }
                    break;
                    
                case 'rubp':
                    // 绘制RuBP分子
                    ctx.fillStyle = '#7B1FA2';
                    ctx.beginPath();
                    ctx.arc(element.x, element.y, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 10px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('RuBP', element.x, element.y + 4);
                    break;
                    
                case 'pga':
                    // 绘制3-磷酸甘油酸
                    ctx.fillStyle = '#0288D1';
                    ctx.beginPath();
                    ctx.arc(element.x, element.y, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 9px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('PGA', element.x, element.y + 4);
                    break;
                    
                case 'atpInput':
                    // 绘制ATP输入
                    const atpInputY = element.y + Math.sin(animationState.time) * 10;
                    ctx.fillStyle = colors.atp;
                    ctx.beginPath();
                    ctx.arc(element.x, atpInputY, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('ATP', element.x, atpInputY + 4);
                    
                    // 绘制箭头指向循环
                    ctx.beginPath();
                    ctx.moveTo(element.x, atpInputY - element.radius);
                    ctx.lineTo(element.x, element.y - 80);
                    ctx.strokeStyle = colors.atp;
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // 绘制箭头头
                    ctx.beginPath();
                    ctx.moveTo(element.x, element.y - 80);
                    ctx.lineTo(element.x - 5, element.y - 85);
                    ctx.lineTo(element.x + 5, element.y - 85);
                    ctx.closePath();
                    ctx.fillStyle = colors.atp;
                    ctx.fill();
                    break;
                    
                case 'nadphInput':
                    // 绘制NADPH输入
                    const nadphInputY = element.y + Math.sin(animationState.time + 1) * 10;
                    ctx.fillStyle = colors.nadph;
                    ctx.beginPath();
                    ctx.arc(element.x, nadphInputY, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 10px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('NADPH', element.x, nadphInputY + 4);
                    
                    // 绘制箭头指向循环
                    ctx.beginPath();
                    ctx.moveTo(element.x, nadphInputY - element.radius);
                    ctx.lineTo(element.x, element.y - 80);
                    ctx.strokeStyle = colors.nadph;
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // 绘制箭头头
                    ctx.beginPath();
                    ctx.moveTo(element.x, element.y - 80);
                    ctx.lineTo(element.x - 5, element.y - 85);
                    ctx.lineTo(element.x + 5, element.y - 85);
                    ctx.closePath();
                    ctx.fillStyle = colors.nadph;
                    ctx.fill();
                    break;
                    
                case 'g3p':
                    // 绘制G3P分子
                    ctx.fillStyle = colors.sugar;
                    ctx.beginPath();
                    ctx.arc(element.x, element.y, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('G3P', element.x, element.y + 4);
                    
                    // 绘制输出箭头
                    ctx.beginPath();
                    ctx.moveTo(element.x, element.y - element.radius);
                    ctx.lineTo(element.x, element.y - 50);
                    ctx.strokeStyle = colors.sugar;
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // 绘制箭头头
                    ctx.beginPath();
                    ctx.moveTo(element.x, element.y - 50);
                    ctx.lineTo(element.x - 5, element.y - 55);
                    ctx.lineTo(element.x + 5, element.y - 55);
                    ctx.closePath();
                    ctx.fillStyle = colors.sugar;
                    ctx.fill();
                    break;
                    
                case 'rubpRegen':
                    // 绘制RuBP再生动画
                    const pulseSize = Math.sin(animationState.time * 3) * 0.2 + 1;
                    ctx.fillStyle = '#7B1FA2';
                    ctx.beginPath();
                    ctx.arc(element.x, element.y, element.radius * pulseSize, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 10px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('RuBP', element.x, element.y + 4);
                    break;
                    
                case 'thylakoidSection':
                    // 绘制类囊体部分（完整循环）
                    ctx.fillStyle = colors.thylakoid;
                    ctx.fillRect(element.x - element.width/2, element.y - element.height/2, element.width, element.height);
                    
                    // 绘制光反应标签
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 14px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('光反应', element.x, element.y);
                    
                    // 绘制小太阳图标
                    ctx.fillStyle = '#FFEB3B';
                    ctx.beginPath();
                    ctx.arc(element.x, element.y - 40, 15, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 绘制光线
                    for (let i = 0; i < 8; i++) {
                        const angle = (i / 8) * Math.PI * 2;
                        ctx.beginPath();
                        ctx.moveTo(element.x + Math.cos(angle) * 15, element.y - 40 + Math.sin(angle) * 15);
                        ctx.lineTo(element.x + Math.cos(angle) * 25, element.y - 40 + Math.sin(angle) * 25);
                        ctx.strokeStyle = '#FFEB3B';
                        ctx.lineWidth = 2;
                        ctx.stroke();
                    }
                    break;
                    
                case 'stromaSection':
                    // 绘制基质部分（完整循环）
                    ctx.fillStyle = colors.stroma;
                    ctx.fillRect(element.x - element.width/2, element.y - element.height/2, element.width, element.height);
                    
                    // 绘制暗反应标签
                    ctx.fillStyle = colors.text;
                    ctx.font = 'bold 14px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('暗反应', element.x, element.y);
                    
                    // 绘制CO₂图标
                    ctx.fillStyle = colors.co2;
                    ctx.beginPath();
                    ctx.arc(element.x, element.y - 40, 12, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 10px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('CO₂', element.x, element.y - 40 + 4);
                    break;
                    
                case 'atpFlow':
                    // 绘制ATP流动
                    const atpFlowX = element.x + (animationState.time % 3) * 30;
                    ctx.fillStyle = colors.atp;
                    ctx.beginPath();
                    ctx.arc(atpFlowX, element.y, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 9px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('ATP', atpFlowX, element.y + 4);
                    break;
                    
                case 'nadphFlow':
                    // 绘制NADPH流动
                    const nadphFlowX = element.x + (animationState.time % 3) * 30;
                    ctx.fillStyle = colors.nadph;
                    ctx.beginPath();
                    ctx.arc(nadphFlowX, element.y, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 8px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('NADPH', nadphFlowX, element.y + 4);
                    break;
                    
                case 'co2Flow':
                    // 绘制CO₂流动
                    const co2FlowY = element.y - (animationState.time % 3) * 20;
                    ctx.fillStyle = colors.co2;
                    ctx.beginPath();
                    ctx.arc(element.x, co2FlowY, element.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 9px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('CO₂', element.x, co2FlowY + 4);
                    break;
                    
                case 'sugarOutput':
                    // 绘制糖类输出
                    const sugarPulse = Math.sin(animationState.time * 2) * 0.2 + 0.8;
                    ctx.fillStyle = colors.sugar;
                    ctx.globalAlpha = sugarPulse;
                    ctx.beginPath();
                    ctx.arc(element.x, element.y, element.radius * sugarPulse, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.globalAlpha = 1.0;
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 10px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('糖类', element.x, element.y + 4);
                    break;
            }
            
            ctx.restore();
        }
        
        // 绘制工具提示
        function drawTooltip(element) {
            const x = element.x;
            const y = element.y;
            const label = element.label;
            const description = element.description;
            
            // 计算文本宽度
            ctx.font = 'bold 14px Arial';
            const labelWidth = ctx.measureText(label).width;
            ctx.font = '12px Arial';
            const descWidth = ctx.measureText(description).width;
            const tooltipWidth = Math.max(labelWidth, descWidth) + 20;
            
            // 绘制工具提示背景
            ctx.fillStyle = 'rgba(255, 255, 255, 0.95)';
            ctx.strokeStyle = colors.highlight;
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.roundRect(x - tooltipWidth/2, y - 80, tooltipWidth, 60, 5);
            ctx.fill();
            ctx.stroke();
            
            // 绘制工具提示文本
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(label, x, y - 60);
            
            ctx.fillStyle = '#666';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            
            // 处理长描述文本
            const words = description.split(' ');
            let line = '';
            let lineHeight = 15;
            let lines = [];
            
            for (let i = 0; i < words.length; i++) {
                const testLine = line + words[i] + ' ';
                const testWidth = ctx.measureText(testLine).width;
                
                if (testWidth > tooltipWidth - 20 && i > 0) {
                    lines.push(line);
                    line = words[i] + ' ';
                } else {
                    line = testLine;
                }
            }
            lines.push(line);
            
            // 绘制多行文本
            for (let i = 0; i < lines.length; i++) {
                ctx.fillText(lines[i], x, y - 40 + i * lineHeight);
            }
        }
        
        // 检查元素是否被悬停
        function isElementHovered(element) {
            if (!animationState.hoveredElement) return false;
            return animationState.hoveredElement === element;
        }
        
        // 更新UI信息
        function updateUI() {
            const scene = scenes[animationState.currentScene];
            const stepTitle = document.getElementById('stepTitle');
            const stepDescription = document.getElementById('stepDescription');
            
            if (animationState.currentScene === 'overview' || animationState.currentScene === 'full') {
                stepTitle.textContent = scene.title;
                stepDescription.textContent = scene.description;
            } else {
                stepTitle.textContent = scene.titles[animationState.step];
                stepDescription.textContent = scene.descriptions[animationState.step];
            }
            
            // 更新场景按钮状态
            document.querySelectorAll('.scene-btn').forEach(btn => {
                if (btn.dataset.scene === animationState.currentScene) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
        }
        
        // 切换场景
        function switchScene(sceneName) {
            animationState.currentScene = sceneName;
            animationState.step = 0;
            animationState.time = 0;
            initAnimationElements();
            updateUI();
        }
        
        // 下一步
        function nextStep() {
            const scene = scenes[animationState.currentScene];
            if (animationState.currentScene === 'overview' || animationState.currentScene === 'full') {
                // 这些场景只有一步，循环播放动画
                animationState.time += 0.1;
            } else {
                animationState.step = (animationState.step + 1) % scene.steps;
                initAnimationElements();
            }
            updateUI();
        }
        
        // 上一步
        function prevStep() {
            const scene = scenes[animationState.currentScene];
            if (animationState.currentScene === 'overview' || animationState.currentScene === 'full') {
                // 这些场景只有一步
                animationState.time -= 0.1;
            } else {
                animationState.step = (animationState.step - 1 + scene.steps) % scene.steps;
                initAnimationElements();
            }
            updateUI();
        }
        
        // 重置动画
        function resetAnimation() {
            animationState.step = 0;
            animationState.time = 0;
            initAnimationElements();
            updateUI();
        }
        
        // 检测鼠标悬停
        function checkHover(mouseX, mouseY) {
            animationState.hoveredElement = null;
            
            for (let i = animationElements.length - 1; i >= 0; i--) {
                const element = animationElements[i];
                let isHovered = false;
                
                // 根据元素类型检测悬停
                switch (element.type) {
                    case 'chloroplast':
                    case 'stroma':
                        const dx = mouseX - element.x;
                        const dy = mouseY - element.y;
                        const rx = element.width / 2;
                        const ry = element.height / 2;
                        isHovered = (dx * dx) / (rx * rx) + (dy * dy) / (ry * ry) <= 1;
                        break;
                        
                    case 'thylakoid':
                    case 'thylakoidMembrane':
                    case 'stromaBackground':
                    case 'thylakoidSection':
                    case 'stromaSection':
                        isHovered = mouseX >= element.x - element.width/2 && 
                                   mouseX <= element.x + element.width/2 && 
                                   mouseY >= element.y - element.height/2 && 
                                   mouseY <= element.y + element.height/2;
                        break;
                        
                    case 'photon':
                    case 'water':
                    case 'oxygen':
                    case 'proton':
                    case 'atp':
                    case 'nadph':
                    case 'co2':
                    case 'rubp':
                    case 'pga':
                    case 'atpInput':
                    case 'nadphInput':
                    case 'g3p':
                    case 'rubpRegen':
                    case 'atpFlow':
                    case 'nadphFlow':
                    case 'co2Flow':
                    case 'sugarOutput':
                        const distance = Math.sqrt(
                            Math.pow(mouseX - element.x, 2) + 
                            Math.pow(mouseY - element.y, 2)
                        );
                        isHovered = distance <= element.radius * 1.5;
                        break;
                        
                    case 'electronChain':
                        isHovered = mouseY >= element.y - 15 && 
                                   mouseY <= element.y + 15 && 
                                   mouseX >= element.x - element.length/2 && 
                                   mouseX <= element.x + element.length/2;
                        break;
                        
                    case 'atpSynthase':
                        isHovered = mouseX >= element.x - element.width/2 && 
                                   mouseX <= element.x + element.width/2 && 
                                   mouseY >= element.y - element.height/2 && 
                                   mouseY <= element.y + element.height/2;
                        break;
                        
                    case 'calvinCycle':
                        const distToCenter = Math.sqrt(
                            Math.pow(mouseX - element.x, 2) + 
                            Math.pow(mouseY - element.y, 2)
                        );
                        isHovered = distToCenter <= element.radius + 10;
                        break;
                }
                
                if (isHovered) {
                    animationState.hoveredElement = element;
                    break;
                }
            }
        }
        
        // 动画循环
        function animate() {
            draw();
            requestAnimationFrame(animate);
        }
        
        // 初始化
        function init() {
            // 初始化Canvas
            resizeCanvas();
            
            // 初始化动画元素
            initAnimationElements();
            
            // 设置事件监听器
            // 场景按钮
            document.querySelectorAll('.scene-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    switchScene(btn.dataset.scene);
                });
            });
            
            // 控制按钮
            document.getElementById('playBtn').addEventListener('click', () => {
                animationState.isPlaying = true;
            });
            
            document.getElementById('pauseBtn').addEventListener('click', () => {
                animationState.isPlaying = false;
            });
            
            document.getElementById('stepBtn').addEventListener('click', nextStep);
            
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            
            // 速度滑块
            document.getElementById('speedSlider').addEventListener('input', (e) => {
                animationState.animationSpeed = parseInt(e.target.value);
            });
            
            // 鼠标移动检测
            canvas.addEventListener('mousemove', (e) => {
                const rect = canvas.getBoundingClientRect();
                const mouseX = e.clientX - rect.left;
                const mouseY = e.clientY - rect.top;
                checkHover(mouseX, mouseY);
            });
            
            canvas.addEventListener('mouseleave', () => {
                animationState.hoveredElement = null;
            });
            
            // 键盘控制
            document.addEventListener('keydown', (e) => {
                switch(e.key) {
                    case ' ':
                        animationState.isPlaying = !animationState.isPlaying;
                        break;
                    case 'ArrowRight':
                        nextStep();
                        break;
                    case 'ArrowLeft':
                        prevStep();
                        break;
                    case 'r':
                    case 'R':
                        resetAnimation();
                        break;
                    case '1':
                        switchScene('overview');
                        break;
                    case '2':
                        switchScene('light');
                        break;
                    case '3':
                        switchScene('dark');
                        break;
                    case '4':
                        switchScene('full');
                        break;
                }
            });
            
            // 开始动画循环
            animate();
            
            // 初始UI更新
            updateUI();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
        
        // 添加 roundRect 方法（如果浏览器不支持）
        if (!CanvasRenderingContext2D.prototype.roundRect) {
            CanvasRenderingContext2D.prototype.roundRect = function(x, y, width, height, radius) {
                if (width < 2 * radius) radius = width / 2;
                if (height < 2 * radius) radius = height / 2;
                this.beginPath();
                this.moveTo(x + radius, y);
                this.arcTo(x + width, y, x + width, y + height, radius);
                this.arcTo(x + width, y + height, x, y + height, radius);
                this.arcTo(x, y + height, x, y, radius);
                this.arcTo(x, y, x + width, y, radius);
                this.closePath();
                return this;
            };
        }
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 光合作用全过程交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态、直观的可视化方式，帮助您深入理解光合作用这一复杂的生物学过程。无论您是学生、教师还是生物学爱好者，本动画都将为您提供一种全新的学习体验。

---

### 一、 功能说明

本动画是一个基于HTML5 Canvas技术构建的交互式教学工具，完整模拟了光合作用在叶绿体中的全过程。它通过四个精心设计的场景，将抽象的生物化学过程转化为生动、易懂的动画，并允许您通过交互控制学习节奏和重点。

### 二、 主要功能

1.  **四场景学习模式**：
    *   **总览**：宏观展示叶绿体的双层膜结构、类囊体（基粒）和基质，建立空间认知。
    *   **光反应**：逐步演示发生在类囊体薄膜上的关键步骤：光子激发、水的光解、电子传递、H⁺泵送、ATP合成及NADPH生成。
    *   **暗反应**：详细展示发生在基质中的卡尔文循环：CO₂固定、三碳化合物还原、糖类（G3P）生成及RuBP再生。
    *   **完整循环**：动态整合光反应与暗反应，清晰展示ATP、NADPH等物质与能量在两个反应间的流动闭环。

2.  **交互式控制**：
    *   **播放/暂停**：控制动画的播放与暂停。
    *   **下一步**：在“光反应”和“暗反应”场景中，可手动步进学习每个子步骤。
    *   **重置**：将当前场景的动画恢复到初始状态。
    *   **速度调节**：通过滑块自由调整动画播放速度，适应不同学习节奏。

3.  **智能提示与探索**：
    *   **悬停提示**：将鼠标悬停在动画中的任何关键结构（如叶绿体、类囊体）或分子（如H₂O、ATP）上，会弹出信息框，显示其名称和功能简介。
    *   **步骤指示**：屏幕右侧信息面板会实时显示当前步骤的标题和详细文字说明，与动画内容同步。
    *   **分子图例**：提供标准化的分子颜色图例，帮助您快速识别不同物质。

### 三、 设计特色

1.  **科学准确性**：动画严格遵循生物学教材，准确呈现了光合作用的光反应与暗反应（卡尔文循环）的步骤、场所及物质能量转换关系。
2.  **认知友好性**：
    *   **空间分层**：从细胞器到分子层面逐级展开，符合认知规律。
    *   **视觉编码**：采用生物学中常用的配色方案（如蓝色代表水，红色代表氧气，橙色代表ATP），降低记忆负担。
    *   **动态隐喻**：用闪烁光点表示光子，流动小球表示分子，旋转齿轮表示酶促反应，使抽象过程具体化。
3.  **教学灵活性**：支持教师按需暂停、分步讲解，也支持学生自主探索和复习，是课堂演示与课后自学的理想工具。

### 四、 教学要点

使用本动画进行教学或学习时，建议重点关注以下核心概念与关系：

1.  **场所分工**：务必明确**光反应在类囊体薄膜**，**暗反应在基质**。这是理解整个过程的**空间基础**。
2.  **能量与物质流**：
    *   **能量流**：光能 → 电能（激发电子）→ 化学能（储存在ATP和NADPH中）→ 化学能（储存在糖类中）。
    *   **物质流**：关注**H₂O**的分解（提供e⁻和H⁺，释放O₂）与**CO₂**的固定还原（生成糖类）。理解**ATP和NADPH**作为“能量货币”和“还原力”从光反应到暗反应的传递作用。
3.  **反应耦合**：强调光反应与暗反应不是独立的，而是通过**ATP和NADPH**紧密耦合。光反应的产物正是暗反应的反应物。
4.  **关键步骤**：
    *   **光反应**：水的光解、H⁺浓度梯度的建立与ATP的合成。
    *   **暗反应**：CO₂的固定（与RuBP结合）、三碳化合物的还原（消耗ATP和NADPH）、RuBP的再生（消耗ATP）。

### 五、 使用建议

1.  **初次学习者**：
    *   建议按照 **“总览” → “光反应” → “暗反应” → “完整循环”** 的顺序完整观看一遍，建立整体印象。
    *   在每个场景中，先点击“播放”观看动态过程，再使用“下一步”功能暂停在关键步骤，结合右侧文字说明和悬停提示仔细理解。
    *   充分利用“完整循环”场景，巩固光反应与暗反应之间的联系。

2.  **课堂教师**：
    *   **引入**：使用“总览”场景介绍叶绿体结构。
    *   **讲解**：分别使用“光反应”和“暗反应”场景进行分步教学。利用“暂停”和“下一步”功能控制节奏，结合悬停提示进行提问和讲解。
    *   **总结**：使用“完整循环”场景进行知识串联与总结，强调物质能量流动的整体性。
    *   **复习**：可让学生操作动画，复述过程，检验学习效果。

3.  **复习与自测者**：
    *   关闭声音或文字提示，尝试仅通过观察动画来复述每个步骤发生了什么、在哪里发生、涉及哪些物质。
    *   重点关注“完整循环”场景，自己描述出从光子到糖类的完整故事线。

4.  **键盘快捷键**（提升操作效率）：
    *   **空格键**：播放/暂停
    *   **方向键右键**：下一步
    *   **方向键左键**：上一步
    *   **R键**：重置当前场景
    *   **数字键1-4**：快速切换场景（1=总览，2=光反应，3=暗反应，4=完整循环）

---

我们希望这个精心设计的交互式动画能成为您探索生命奥秘的得力助手。祝您学习愉快，收获满满！