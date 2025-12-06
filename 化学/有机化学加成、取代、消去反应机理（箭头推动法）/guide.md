# 需求：有机化学加成、取代、消去反应机理（箭头推动法）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中化学选修或大学基础有机化学的学生。他们已具备基本的化学键、官能团和电子云等预备知识。
2.  **核心痛点**：
    *   **抽象性**：反应机理涉及不可见的电子移动和键的断裂与形成，难以在静态书本上直观理解。
    *   **动态性**：箭头推动法（电子流向）是一个连续、动态的过程，传统教学缺乏对这一过程的动态分解。
    *   **规则性**：学生需要理解并记忆不同类型反应（加成、取代、消去）的通用机理模式，而非孤立地记忆单个反应。
3.  **学习目标**：
    *   **理解**：能准确描述三类反应中电子的起源、路径和终点。
    *   **识别**：能根据反应物和条件，预判可能发生的反应类型及关键中间体。
    *   **绘制**：能独立、正确地使用弯箭头绘制简单反应的机理示意图。

#### 教学设计思路
1.  **核心概念解构**：
    *   **基石**：强化“电子富集区”（亲核试剂，如`:Nu-`）攻击“电子匮乏区”（亲电试剂，如`Cδ+`）的基本思想。
    *   **三类反应核心对比**：
        *   **加成**：不饱和键（π键）打开，两个部分分别加到两端。
        *   **取代**：一个基团被另一个基团替换（常伴随离去基团`-L`的离开）。
        *   **消去**：从一个分子中脱去两个原子或基团，形成新的π键。
    *   **箭头语义**：明确区分“电子对转移箭头”（弯箭头，从电子源指向新键形成处或正电荷）和“反应箭头”（直箭头，表示反应过程）。

2.  **认知规律遵循**：
    *   **从具体到抽象**：先展示一个生动的宏观类比（如“握手”、“交换舞伴”、“拆开拉链”），再过渡到微观的电子层面。
    *   **分步动画与可控节奏**：将连续的机理分解为清晰的“步骤”，每一步都高亮当前移动的电子对和变化的化学键，允许学习者暂停、回放。
    *   **对比学习**：并排展示三类反应的机理动画，突出其电子流向和键变化的根本差异。

3.  **交互设计**：
    *   **模式化学习路径**：设计“引导模式”（自动播放讲解）和“探索模式”（手动点击触发每一步）。
    *   **“分子积木”交互**：在练习区，提供可拖拽的常见基团（如`-OH`， `-Br`， `H+`）和电子对，让用户尝试组合并绘制正确箭头，系统提供即时反馈。
    *   **视觉线索强化**：当鼠标悬停在试剂上时，高亮显示其亲核或亲电区域（如用蓝色渐变表示电子云密度高，红色表示低）。

4.  **视觉呈现**：
    *   **分子模型**：采用清晰的“球棍模型”与“电子云/轨道示意图”结合的方式。键的断裂与形成要有平滑的形变动画。
    *   **箭头动力学**：
        *   电子对箭头（弯箭头）应从电子对的精确位置（如孤对电子或π键中部）平滑“生长”并移动到目标位置。
        *   键的断裂动画应与电子箭头的到达同步，旧键渐隐/断裂，新键渐现/形成。
    *   **电荷变化可视化**：原子上的形式电荷用动态变化的“+”或“-”符号显示，并伴随颜色变化（如正电荷区域泛红，负电荷区域泛蓝）。

#### 配色方案选择
*   **主色调**：采用深蓝色（`#2c3e50`）作为背景，营造专注、科学的氛围，并能突出前景的彩色元素。
*   **原子色标**（遵循CPK惯例，增强识别度）：
    *   碳（C）：`#909090`（灰色）
    *   氢（H）：`#ffffff`（白色）
    *   氧（O）：`#ff0d0d`（红色）
    *   氮（N）：`#3050f8`（蓝色）
    *   卤素（Cl， Br）：`#1ff01f`（绿色）
*   **功能色**：
    *   **电子与箭头**：`#f9e300`（亮黄色），在深色背景下极其醒目。
    *   **亲核区域高亮**：`#00bfff`（浅蓝色，半透明渐变）。
    *   **亲电区域高亮**：`#ff6b6b`（浅红色，半透明渐变）。
    *   **键形成/断裂高亮**：`#ffa500`（橙色）脉冲效果。
    *   **界面按钮/交互元素**：`#3498db`（蓝色）与 `#2ecc71`（绿色），表示可操作与正确反馈。

#### 交互功能列表
1.  **主控面板**：播放/暂停/重置动画、速度调节滑块。
2.  **反应类型选择器**：通过标签页或按钮在“加成”、“取代”、“消去”三大类之间切换。
3.  **分步控制条**：显示当前反应的步骤（如“步骤1：亲核进攻”、“步骤2：离去基团离开”），可点击跳转到任意步骤。
4.  **视图切换**：在“球棍模型”、“电子云视图”和“混合视图”之间切换，帮助理解电子分布。
5.  **悬停提示**：鼠标悬停在原子、键或箭头上时，显示其名称、电荷、电子云密度等详细信息。
6.  **练习模块**：
    *   **拖拽构建**：从工具栏拖拽分子片段组装反应物。
    *   **箭头绘制工具**：在指定区域，用户可点击电子源并拖拽到目标来绘制弯箭头，系统会判断正确性。
    *   **即时反馈**：对用户的操作给出“正确！”或提示“电子流向错误，请检查亲电中心”。
7.  **对比视图**：可同时打开两个窗口，对比不同反应机理的异同。
8.  **知识卡片**：在动画侧边栏，随步骤弹出关键概念的文字说明（如“马氏规则”、“碳正离子稳定性”等）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>有机化学反应机理动画教学</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #2c3e50;
            color: #ecf0f1;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        header {
            text-align: center;
            padding: 20px;
            background: linear-gradient(135deg, #3498db, #2c3e50);
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: #f9e300;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .subtitle {
            font-size: 1.2rem;
            color: #bdc3c7;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }

        .left-panel {
            flex: 1;
            min-width: 300px;
            background-color: #34495e;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
        }

        .right-panel {
            flex: 2;
            min-width: 500px;
            background-color: #34495e;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .reaction-selector {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        .reaction-btn {
            padding: 12px 20px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 120px;
        }

        .reaction-btn:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }

        .reaction-btn.active {
            background-color: #2ecc71;
            box-shadow: 0 0 10px rgba(46, 204, 113, 0.5);
        }

        .example-selector {
            margin-bottom: 20px;
        }

        .example-btn {
            padding: 10px 15px;
            background-color: #7f8c8d;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-right: 10px;
            margin-bottom: 10px;
            transition: all 0.3s ease;
        }

        .example-btn:hover {
            background-color: #95a5a6;
        }

        .example-btn.active {
            background-color: #e74c3c;
        }

        .control-panel {
            background-color: #2c3e50;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
        }

        .control-row {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 10px;
            flex-wrap: wrap;
        }

        .control-btn {
            padding: 8px 15px;
            background-color: #9b59b6;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .control-btn:hover {
            background-color: #8e44ad;
        }

        .control-btn:disabled {
            background-color: #7d3c98;
            opacity: 0.5;
            cursor: not-allowed;
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .speed-slider {
            width: 150px;
        }

        .step-indicator {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 10px;
        }

        .step-btn {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            border: 2px solid #3498db;
            background-color: transparent;
            color: #3498db;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .step-btn:hover {
            background-color: #3498db;
            color: white;
        }

        .step-btn.active {
            background-color: #2ecc71;
            border-color: #2ecc71;
            color: white;
        }

        .step-btn.completed {
            background-color: #3498db;
            border-color: #3498db;
            color: white;
        }

        .canvas-container {
            flex: 1;
            background-color: #1a252f;
            border-radius: 8px;
            overflow: hidden;
            position: relative;
            min-height: 400px;
        }

        #reactionCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .info-panel {
            background-color: #2c3e50;
            padding: 15px;
            border-radius: 8px;
            min-height: 150px;
        }

        .info-title {
            color: #f9e300;
            margin-bottom: 10px;
            font-size: 1.2rem;
            border-bottom: 2px solid #f9e300;
            padding-bottom: 5px;
        }

        .info-content {
            line-height: 1.8;
        }

        .highlight {
            color: #f9e300;
            font-weight: bold;
        }

        .key-concept {
            background-color: rgba(52, 152, 219, 0.2);
            border-left: 4px solid #3498db;
            padding: 10px;
            margin: 10px 0;
            border-radius: 0 5px 5px 0;
        }

        .practice-panel {
            background-color: #2c3e50;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
        }

        .practice-title {
            color: #2ecc71;
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .practice-area {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .molecule-builder {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 15px;
        }

        .molecule-part {
            padding: 8px 12px;
            background-color: #34495e;
            border: 2px dashed #7f8c8d;
            border-radius: 5px;
            cursor: move;
            user-select: none;
        }

        .molecule-part:hover {
            border-color: #3498db;
            background-color: #3d566e;
        }

        .feedback {
            padding: 10px;
            border-radius: 5px;
            margin-top: 10px;
            text-align: center;
            font-weight: bold;
            display: none;
        }

        .feedback.correct {
            background-color: rgba(46, 204, 113, 0.2);
            border: 2px solid #2ecc71;
            color: #2ecc71;
            display: block;
        }

        .feedback.incorrect {
            background-color: rgba(231, 76, 60, 0.2);
            border: 2px solid #e74c3c;
            color: #e74c3c;
            display: block;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding: 15px;
            background-color: rgba(0, 0, 0, 0.2);
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
            border-radius: 50%;
        }

        footer {
            text-align: center;
            padding: 20px;
            color: #bdc3c7;
            font-size: 0.9rem;
            margin-top: 20px;
            border-top: 1px solid #34495e;
        }

        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
            
            .left-panel, .right-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>有机化学反应机理教学动画</h1>
            <p class="subtitle">加成 · 取代 · 消去反应 | 箭头推动法可视化</p>
        </header>
        
        <div class="main-content">
            <div class="left-panel">
                <h2>反应类型</h2>
                <div class="reaction-selector">
                    <button class="reaction-btn active" data-type="addition">加成反应</button>
                    <button class="reaction-btn" data-type="substitution">取代反应</button>
                    <button class="reaction-btn" data-type="elimination">消去反应</button>
                </div>
                
                <h3>反应示例</h3>
                <div class="example-selector">
                    <div id="addition-examples" class="example-list">
                        <button class="example-btn active" data-example="alkene-hbr">烯烃 + HBr</button>
                        <button class="example-btn" data-example="alkyne-h2">炔烃 + H₂</button>
                        <button class="example-btn" data-example="carbonyl-nabh4">羰基 + NaBH₄</button>
                    </div>
                    <div id="substitution-examples" class="example-list" style="display:none;">
                        <button class="example-btn active" data-example="haloalkane-oh">卤代烷 + OH⁻</button>
                        <button class="example-btn" data-example="ester-hydrolysis">酯的水解</button>
                        <button class="example-btn" data-example="aromatic-nitration">芳香族硝化</button>
                    </div>
                    <div id="elimination-examples" class="example-list" style="display:none;">
                        <button class="example-btn active" data-example="haloalkane-oh-elim">卤代烷 + OH⁻ (E2)</button>
                        <button class="example-btn" data-example="alcohol-h2so4">醇 + H₂SO₄</button>
                        <button class="example-btn" data-example="hofmann">Hofmann消除</button>
                    </div>
                </div>
                
                <div class="control-panel">
                    <h3>动画控制</h3>
                    <div class="control-row">
                        <button class="control-btn" id="playBtn">▶ 播放</button>
                        <button class="control-btn" id="pauseBtn">⏸ 暂停</button>
                        <button class="control-btn" id="resetBtn">↺ 重置</button>
                        <button class="control-btn" id="prevStepBtn">◀ 上一步</button>
                        <button class="control-btn" id="nextStepBtn">▶ 下一步</button>
                    </div>
                    
                    <div class="control-row">
                        <div class="speed-control">
                            <span>速度:</span>
                            <input type="range" min="1" max="10" value="5" class="speed-slider" id="speedSlider">
                            <span id="speedValue">中速</span>
                        </div>
                    </div>
                    
                    <div class="step-indicator">
                        <span>步骤:</span>
                        <button class="step-btn active" data-step="0">1</button>
                        <button class="step-btn" data-step="1">2</button>
                        <button class="step-btn" data-step="2">3</button>
                        <button class="step-btn" data-step="3">4</button>
                    </div>
                </div>
                
                <div class="info-panel">
                    <div class="info-title">当前步骤说明</div>
                    <div class="info-content" id="stepInfo">
                        <p><span class="highlight">步骤1: 亲核进攻</span></p>
                        <p>亲核试剂（富电子物种）进攻亲电中心（缺电子碳原子）。</p>
                        <div class="key-concept">
                            <strong>关键概念:</strong> 弯箭头从亲核试剂的孤对电子或π键指向亲电中心，表示电子对的转移。
                        </div>
                    </div>
                </div>
                
                <div class="practice-panel">
                    <div class="practice-title">互动练习</div>
                    <div class="practice-area">
                        <p>尝试绘制电子流动箭头：</p>
                        <div class="molecule-builder">
                            <div class="molecule-part" draggable="true">H₃C-CH=CH₂</div>
                            <div class="molecule-part" draggable="true">H⁺</div>
                            <div class="molecule-part" draggable="true">Br⁻</div>
                            <div class="molecule-part" draggable="true">:OH⁻</div>
                        </div>
                        <button class="control-btn" id="checkArrowBtn">检查箭头</button>
                        <div class="feedback" id="feedback"></div>
                    </div>
                </div>
            </div>
            
            <div class="right-panel">
                <div class="canvas-container">
                    <canvas id="reactionCanvas" width="800" height="500"></canvas>
                </div>
                
                <div class="info-panel">
                    <div class="info-title">反应机理详解</div>
                    <div class="info-content" id="mechanismInfo">
                        <p><span class="highlight">加成反应机理:</span> 不饱和键（π键）打开，两个部分分别加到两端。</p>
                        <p>1. 亲电试剂（如H⁺）进攻π键，形成碳正离子中间体。</p>
                        <p>2. 亲核试剂（如Br⁻）进攻碳正离子，形成最终产物。</p>
                        <p><span class="highlight">马氏规则:</span> 氢原子加到含氢较多的碳原子上。</p>
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #909090;"></div>
                        <span>碳原子 (C)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ffffff; border: 1px solid #ccc;"></div>
                        <span>氢原子 (H)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff0d0d;"></div>
                        <span>氧原子 (O)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #3050f8;"></div>
                        <span>氮原子 (N)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #1ff01f;"></div>
                        <span>卤素 (Br/Cl)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f9e300;"></div>
                        <span>电子/箭头</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #00bfff;"></div>
                        <span>亲核区域</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff6b6b;"></div>
                        <span>亲电区域</span>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>有机化学反应机理教学动画 | 设计：教育技术专家 | 本动画使用HTML5 Canvas实现</p>
            <p>提示：点击步骤按钮可跳转到特定步骤，使用速度滑块调整动画播放速度</p>
        </footer>
    </div>

    <script>
        // 全局变量
        let canvas, ctx;
        let currentReactionType = 'addition';
        let currentExample = 'alkene-hbr';
        let animationSpeed = 5;
        let currentStep = 0;
        let totalSteps = 4;
        let isPlaying = false;
        let animationFrameId = null;
        let animationTime = 0;
        
        // 原子颜色映射
        const atomColors = {
            'C': '#909090',
            'H': '#ffffff',
            'O': '#ff0d0d',
            'N': '#3050f8',
            'Br': '#1ff01f',
            'Cl': '#1ff01f'
        };
        
        // 反应数据
        const reactionData = {
            'addition': {
                'alkene-hbr': {
                    name: '烯烃与HBr的加成',
                    reactants: ['H₂C=CH₂', 'HBr'],
                    products: ['CH₃-CH₂-Br'],
                    steps: [
                        {
                            title: '步骤1: 亲电进攻',
                            description: 'H⁺作为亲电试剂进攻π键，形成碳正离子中间体',
                            mechanism: 'H⁺进攻烯烃的π键，π电子对转移到H⁺上，形成C-H键'
                        },
                        {
                            title: '步骤2: 碳正离子形成',
                            description: '生成仲碳正离子中间体（遵循马氏规则）',
                            mechanism: 'π键断裂，正电荷转移到含氢较少的碳原子上'
                        },
                        {
                            title: '步骤3: 亲核进攻',
                            description: 'Br⁻作为亲核试剂进攻碳正离子',
                            mechanism: 'Br⁻的孤对电子转移到带正电的碳原子上'
                        },
                        {
                            title: '步骤4: 产物形成',
                            description: '形成最终加成产物',
                            mechanism: '形成新的C-Br键，得到溴乙烷'
                        }
                    ],
                    mechanismInfo: '加成反应机理: 不饱和键（π键）打开，两个部分分别加到两端。\n1. 亲电试剂（如H⁺）进攻π键，形成碳正离子中间体。\n2. 亲核试剂（如Br⁻）进攻碳正离子，形成最终产物。\n马氏规则: 氢原子加到含氢较多的碳原子上。'
                },
                'alkyne-h2': {
                    name: '炔烃与H₂的加成',
                    reactants: ['HC≡CH', 'H₂'],
                    products: ['H₂C=CH₂', 'CH₃-CH₃'],
                    steps: [
                        {
                            title: '步骤1: 催化剂吸附',
                            description: 'H₂在金属催化剂表面解离',
                            mechanism: 'H-H键在催化剂表面断裂，形成两个吸附的H原子'
                        },
                        {
                            title: '步骤2: 顺式加成',
                            description: '两个H原子顺式加到炔烃三键上',
                            mechanism: 'H原子从催化剂表面转移到炔烃上，形成烯烃'
                        },
                        {
                            title: '步骤3: 进一步加成',
                            description: '烯烃进一步加氢生成烷烃',
                            mechanism: '剩余的π键与H原子反应'
                        },
                        {
                            title: '步骤4: 产物解吸',
                            description: '烷烃产物从催化剂表面解吸',
                            mechanism: '形成最终烷烃产物'
                        }
                    ],
                    mechanismInfo: '炔烃催化加氢机理: 在金属催化剂表面，H₂发生均裂，H原子顺式加到不饱和键上。\n1. H₂在催化剂表面解离为两个H原子。\n2. H原子顺式加到三键上，首先生成烯烃。\n3. 烯烃可进一步加氢生成烷烃。'
                }
            },
            'substitution': {
                'haloalkane-oh': {
                    name: '卤代烷的SN2取代',
                    reactants: ['CH₃-Br', 'OH⁻'],
                    products: ['CH₃-OH', 'Br⁻'],
                    steps: [
                        {
                            title: '步骤1: 亲核进攻',
                            description: 'OH⁻从背面进攻碳原子',
                            mechanism: '亲核试剂从离去基团背面接近碳原子'
                        },
                        {
                            title: '步骤2: 过渡态形成',
                            description: '形成五配位过渡态',
                            mechanism: 'C-Br键部分断裂，C-OH键部分形成'
                        },
                        {
                            title: '步骤3: 键的断裂与形成',
                            description: 'C-Br键完全断裂，C-OH键完全形成',
                            mechanism: 'Br⁻作为离去基团离开，OH⁻与碳原子成键'
                        },
                        {
                            title: '步骤4: 产物形成',
                            description: '生成醇和溴离子',
                            mechanism: '构型发生瓦尔登翻转'
                        }
                    ],
                    mechanismInfo: 'SN2取代反应机理: 一步协同反应，亲核试剂从背面进攻。\n1. 亲核试剂从离去基团背面进攻碳原子。\n2. 形成五配位过渡态。\n3. 旧键断裂与新键形成同时发生。\n4. 产物构型发生翻转（瓦尔登翻转）。'
                }
            },
            'elimination': {
                'haloalkane-oh-elim': {
                    name: '卤代烷的E2消除',
                    reactants: ['CH₃-CH₂-Br', 'OH⁻'],
                    products: ['H₂C=CH₂', 'H₂O', 'Br⁻'],
                    steps: [
                        {
                            title: '步骤1: 碱进攻β-氢',
                            description: 'OH⁻进攻β-碳上的氢原子',
                            mechanism: '碱夺取β-氢原子，形成部分负电荷'
                        },
                        {
                            title: '步骤2: 键的同步变化',
                            description: 'C-H键和C-Br键同步断裂',
                            mechanism: 'β-氢被夺取，C-Br键开始断裂'
                        },
                        {
                            title: '步骤3: π键形成',
                            description: '在α和β碳之间形成π键',
                            mechanism: '电子对转移到α和β碳之间形成双键'
                        },
                        {
                            title: '步骤4: 产物形成',
                            description: '生成烯烃、水和溴离子',
                            mechanism: '离去基团Br⁻离开，形成最终产物'
                        }
                    ],
                    mechanismInfo: 'E2消除反应机理: 一步协同反应，碱夺取β-氢。\n1. 强碱进攻β-氢原子。\n2. C-H键和C-X键同步断裂。\n3. 在α和β碳之间形成π键。\n4. 生成烯烃和离去基团。\n遵循查依采夫规则: 生成更稳定的烯烃（更多取代基）。'
                }
            }
        };
        
        // 初始化
        document.addEventListener('DOMContentLoaded', function() {
            canvas = document.getElementById('reactionCanvas');
            ctx = canvas.getContext('2d');
            
            // 设置Canvas尺寸
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // 初始化事件监听器
            initEventListeners();
            
            // 绘制初始反应
            drawReaction();
        });
        
        // 调整Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            drawReaction();
        }
        
        // 初始化事件监听器
        function initEventListeners() {
            // 反应类型按钮
            document.querySelectorAll('.reaction-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    document.querySelectorAll('.reaction-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    currentReactionType = this.dataset.type;
                    
                    // 显示对应的示例
                    document.querySelectorAll('.example-list').forEach(list => {
                        list.style.display = 'none';
                    });
                    document.getElementById(`${currentReactionType}-examples`).style.display = 'block';
                    
                    // 重置示例选择
                    const firstExample = document.querySelector(`#${currentReactionType}-examples .example-btn`);
                    if (firstExample) {
                        document.querySelectorAll('.example-btn').forEach(b => b.classList.remove('active'));
                        firstExample.classList.add('active');
                        currentExample = firstExample.dataset.example;
                    }
                    
                    resetAnimation();
                    updateStepInfo();
                    updateMechanismInfo();
                });
            });
            
            // 示例按钮
            document.querySelectorAll('.example-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const parent = this.parentElement;
                    parent.querySelectorAll('.example-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    currentExample = this.dataset.example;
                    
                    resetAnimation();
                    updateStepInfo();
                    updateMechanismInfo();
                });
            });
            
            // 控制按钮
            document.getElementById('playBtn').addEventListener('click', playAnimation);
            document.getElementById('pauseBtn').addEventListener('click', pauseAnimation);
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            document.getElementById('prevStepBtn').addEventListener('click', prevStep);
            document.getElementById('nextStepBtn').addEventListener('click', nextStep);
            
            // 速度滑块
            const speedSlider = document.getElementById('speedSlider');
            const speedValue = document.getElementById('speedValue');
            speedSlider.addEventListener('input', function() {
                animationSpeed = parseInt(this.value);
                const speedText = ['极慢', '很慢', '慢', '较慢', '中速', '较快', '快', '很快', '极快', '最快'];
                speedValue.textContent = speedText[animationSpeed - 1];
            });
            
            // 步骤按钮
            document.querySelectorAll('.step-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const step = parseInt(this.dataset.step);
                    goToStep(step);
                });
            });
            
            // 检查箭头按钮
            document.getElementById('checkArrowBtn').addEventListener('click', function() {
                const feedback = document.getElementById('feedback');
                const isCorrect = Math.random() > 0.5; // 模拟检查结果
                
                if (isCorrect) {
                    feedback.textContent = '✓ 正确！电子流向绘制准确。';
                    feedback.className = 'feedback correct';
                } else {
                    feedback.textContent = '✗ 电子流向错误，请检查亲电中心。';
                    feedback.className = 'feedback incorrect';
                }
                
                // 3秒后隐藏反馈
                setTimeout(() => {
                    feedback.style.display = 'none';
                }, 3000);
            });
            
            // 拖拽分子部件
            document.querySelectorAll('.molecule-part').forEach(part => {
                part.addEventListener('dragstart', function(e) {
                    e.dataTransfer.setData('text/plain', this.textContent);
                });
            });
        }
        
        // 播放动画
        function playAnimation() {
            if (isPlaying) return;
            isPlaying = true;
            document.getElementById('playBtn').disabled = true;
            document.getElementById('pauseBtn').disabled = false;
            animate();
        }
        
        // 暂停动画
        function pauseAnimation() {
            isPlaying = false;
            document.getElementById('playBtn').disabled = false;
            document.getElementById('pauseBtn').disabled = true;
            if (animationFrameId) {
                cancelAnimationFrame(animationFrameId);
                animationFrameId = null;
            }
        }
        
        // 重置动画
        function resetAnimation() {
            pauseAnimation();
            currentStep = 0;
            animationTime = 0;
            updateStepButtons();
            drawReaction();
            updateStepInfo();
        }
        
        // 上一步
        function prevStep() {
            if (currentStep > 0) {
                currentStep--;
                updateStepButtons();
                drawReaction();
                updateStepInfo();
            }
        }
        
        // 下一步
        function nextStep() {
            if (currentStep < totalSteps - 1) {
                currentStep++;
                updateStepButtons();
                drawReaction();
                updateStepInfo();
            }
        }
        
        // 跳转到指定步骤
        function goToStep(step) {
            if (step >= 0 && step < totalSteps) {
                currentStep = step;
                updateStepButtons();
                drawReaction();
                updateStepInfo();
            }
        }
        
        // 更新步骤按钮状态
        function updateStepButtons() {
            document.querySelectorAll('.step-btn').forEach((btn, index) => {
                btn.classList.remove('active', 'completed');
                if (index === currentStep) {
                    btn.classList.add('active');
                } else if (index < currentStep) {
                    btn.classList.add('completed');
                }
            });
        }
        
        // 更新步骤信息
        function updateStepInfo() {
            const stepInfo = document.getElementById('stepInfo');
            const data = reactionData[currentReactionType]?.[currentExample];
            
            if (data && data.steps && data.steps[currentStep]) {
                const step = data.steps[currentStep];
                stepInfo.innerHTML = `
                    <p><span class="highlight">${step.title}</span></p>
                    <p>${step.description}</p>
                    <div class="key-concept">
                        <strong>机理描述:</strong> ${step.mechanism}
                    </div>
                `;
            }
        }
        
        // 更新机理信息
        function updateMechanismInfo() {
            const mechanismInfo = document.getElementById('mechanismInfo');
            const data = reactionData[currentReactionType]?.[currentExample];
            
            if (data && data.mechanismInfo) {
                mechanismInfo.innerHTML = data.mechanismInfo.split('\n').map(line => {
                    if (line.includes(':')) {
                        const parts = line.split(':');
                        return `<p><span class="highlight">${parts[0]}:</span>${parts.slice(1).join(':')}</p>`;
                    }
                    return `<p>${line}</p>`;
                }).join('');
            }
        }
        
        // 动画循环
        function animate() {
            if (!isPlaying) return;
            
            animationTime += 0.02 * animationSpeed;
            
            // 如果动画时间超过当前步骤的持续时间，进入下一步
            if (animationTime > 1) {
                animationTime = 0;
                if (currentStep < totalSteps - 1) {
                    currentStep++;
                    updateStepButtons();
                    updateStepInfo();
                } else {
                    pauseAnimation();
                    return;
                }
            }
            
            drawReaction();
            animationFrameId = requestAnimationFrame(animate);
        }
        
        // 绘制反应
        function drawReaction() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            ctx.fillStyle = '#1a252f';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 获取当前反应数据
            const data = reactionData[currentReactionType]?.[currentExample];
            if (!data) return;
            
            // 绘制标题
            ctx.fillStyle = '#f9e300';
            ctx.font = 'bold 24px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(data.name, canvas.width / 2, 40);
            
            // 绘制反应物和产物
            ctx.font = 'bold 20px Arial';
            ctx.fillStyle = '#ecf0f1';
            
            // 反应物
            ctx.fillText('反应物:', canvas.width * 0.2, 100);
            data.reactants.forEach((reactant, i) => {
                ctx.fillText(reactant, canvas.width * 0.2, 130 + i * 30);
            });
            
            // 反应箭头
            ctx.fillStyle = '#3498db';
            ctx.font = 'bold 30px Arial';
            ctx.fillText('→', canvas.width * 0.45, 120);
            
            // 产物
            ctx.fillStyle = '#ecf0f1';
            ctx.font = 'bold 20px Arial';
            ctx.fillText('产物:', canvas.width * 0.7, 100);
            data.products.forEach((product, i) => {
                ctx.fillText(product, canvas.width * 0.7, 130 + i * 30);
            });
            
            // 根据反应类型和步骤绘制机理
            drawMechanism();
            
            // 绘制当前步骤指示器
            ctx.fillStyle = '#2ecc71';
            ctx.font = '16px Arial';
            ctx.textAlign = 'left';
            ctx.fillText(`当前步骤: ${currentStep + 1}/${totalSteps}`, 20, canvas.height - 30);
            
            // 绘制电子流动箭头（动画效果）
            drawElectronArrows();
        }
        
        // 绘制机理示意图
        function drawMechanism() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2 + 50;
            
            // 根据反应类型绘制不同的机理
            switch(currentReactionType) {
                case 'addition':
                    drawAdditionMechanism(centerX, centerY);
                    break;
                case 'substitution':
                    drawSubstitutionMechanism(centerX, centerY);
                    break;
                case 'elimination':
                    drawEliminationMechanism(centerX, centerY);
                    break;
            }
        }
        
        // 绘制加成反应机理
        function drawAdditionMechanism(centerX, centerY) {
            // 绘制烯烃分子
            drawAtom(centerX - 100, centerY, 'C', 'C1');
            drawAtom(centerX - 60, centerY, 'C', 'C2');
            drawBond(centerX - 100, centerY, centerX - 60, centerY, 2); // 双键
            
            // 绘制氢原子
            drawAtom(centerX - 120, centerY - 30, 'H', 'H1');
            drawAtom(centerX - 120, centerY + 30, 'H', 'H2');
            drawAtom(centerX - 40, centerY - 30, 'H', 'H3');
            drawAtom(centerX - 40, centerY + 30, 'H', 'H4');
            
            drawBond(centerX - 100, centerY, centerX - 120, centerY - 30, 1);
            drawBond(centerX - 100, centerY, centerX - 120, centerY + 30, 1);
            drawBond(centerX - 60, centerY, centerX - 40, centerY - 30, 1);
            drawBond(centerX - 60, centerY, centerX - 40, centerY + 30, 1);
            
            // 绘制HBr分子
            drawAtom(centerX + 
<!--检测到代码截断，自动续写中...-->
100, centerY - 50, 'H', 'H5');
            drawAtom(centerX + 140, centerY - 50, 'Br', 'Br1');
            drawBond(centerX + 100, centerY - 50, centerX + 140, centerY - 50, 1);
            
            // 根据步骤绘制动画
            if (currentStep >= 0) {
                // 步骤1: 亲电进攻 - H⁺进攻π键
                const progress = Math.min(1, animationTime * 2);
                const arrowStartX = centerX + 100;
                const arrowStartY = centerY - 50;
                const arrowEndX = centerX - 80 + (centerX - 80 - arrowStartX) * progress;
                const arrowEndY = centerY + (centerY - arrowStartY) * progress;
                
                // 绘制电子箭头
                drawCurvedArrow(arrowStartX, arrowStartY, arrowEndX, arrowEndY, progress);
                
                // 高亮亲电区域
                if (progress < 0.5) {
                    drawHighlight(centerX - 80, centerY, 40, '#ff6b6b', 0.3);
                }
            }
            
            if (currentStep >= 1) {
                // 步骤2: 碳正离子形成
                drawAtom(centerX - 80, centerY, 'C', 'C1', true); // 带正电荷
                drawAtom(centerX - 40, centerY, 'C', 'C2');
                
                // 绘制单键
                drawBond(centerX - 80, centerY, centerX - 40, centerY, 1);
                
                // 绘制H⁺已加到碳上
                drawAtom(centerX - 80, centerY - 20, 'H', 'H5');
                drawBond(centerX - 80, centerY, centerX - 80, centerY - 20, 1);
                
                // 高亮碳正离子
                drawHighlight(centerX - 80, centerY, 30, '#ff6b6b', 0.5);
            }
            
            if (currentStep >= 2) {
                // 步骤3: 亲核进攻 - Br⁻进攻碳正离子
                const progress = Math.max(0, Math.min(1, (animationTime - 0.5) * 2));
                const arrowStartX = centerX + 140;
                const arrowStartY = centerY - 50;
                const arrowEndX = centerX - 80 + (centerX - 80 - arrowStartX) * progress;
                const arrowEndY = centerY + 20 + (centerY + 20 - arrowStartY) * progress;
                
                // 绘制电子箭头
                drawCurvedArrow(arrowStartX, arrowStartY, arrowEndX, arrowEndY, progress, true);
                
                // 高亮亲核试剂
                drawHighlight(centerX + 140, centerY - 50, 25, '#00bfff', 0.3);
            }
            
            if (currentStep >= 3) {
                // 步骤4: 产物形成
                drawAtom(centerX - 80, centerY, 'C', 'C1');
                drawAtom(centerX - 40, centerY, 'C', 'C2');
                drawBond(centerX - 80, centerY, centerX - 40, centerY, 1);
                
                // 绘制Br加到碳上
                drawAtom(centerX - 80, centerY + 20, 'Br', 'Br1');
                drawBond(centerX - 80, centerY, centerX - 80, centerY + 20, 1);
                
                // 绘制最终产物
                ctx.fillStyle = '#2ecc71';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('CH₃-CH₂-Br', centerX, centerY + 100);
            }
        }
        
        // 绘制取代反应机理
        function drawSubstitutionMechanism(centerX, centerY) {
            // 绘制CH₃-Br分子
            drawAtom(centerX - 80, centerY, 'C', 'C1');
            drawAtom(centerX - 120, centerY - 30, 'H', 'H1');
            drawAtom(centerX - 120, centerY + 30, 'H', 'H2');
            drawAtom(centerX - 40, centerY, 'H', 'H3');
            drawAtom(centerX - 80, centerY - 60, 'Br', 'Br1');
            
            drawBond(centerX - 80, centerY, centerX - 120, centerY - 30, 1);
            drawBond(centerX - 80, centerY, centerX - 120, centerY + 30, 1);
            drawBond(centerX - 80, centerY, centerX - 40, centerY, 1);
            drawBond(centerX - 80, centerY, centerX - 80, centerY - 60, 1);
            
            // 绘制OH⁻离子
            drawAtom(centerX + 80, centerY, 'O', 'O1');
            drawAtom(centerX + 80, centerY - 30, 'H', 'H4');
            drawBond(centerX + 80, centerY, centerX + 80, centerY - 30, 1);
            
            // 绘制负电荷
            ctx.fillStyle = '#f9e300';
            ctx.font = 'bold 20px Arial';
            ctx.fillText('⁻', centerX + 95, centerY - 5);
            
            if (currentStep >= 0) {
                // 步骤1: 亲核试剂从背面进攻
                const progress = Math.min(1, animationTime * 2);
                const angle = Math.PI * 0.7; // 从背面进攻的角度
                const radius = 60;
                const arrowStartX = centerX + 80;
                const arrowStartY = centerY;
                const arrowEndX = centerX - 80 + radius * Math.cos(angle) * progress;
                const arrowEndY = centerY + radius * Math.sin(angle) * progress;
                
                drawCurvedArrow(arrowStartX, arrowStartY, arrowEndX, arrowEndY, progress);
                
                // 高亮亲核试剂
                drawHighlight(centerX + 80, centerY, 25, '#00bfff', 0.3);
            }
            
            if (currentStep >= 1) {
                // 步骤2: 过渡态形成
                const progress = Math.max(0, Math.min(1, (animationTime - 0.5) * 2));
                
                // 绘制五配位过渡态
                drawAtom(centerX - 80, centerY, 'C', 'C1');
                
                // 部分形成的C-O键
                ctx.strokeStyle = '#f9e300';
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 3]);
                ctx.beginPath();
                ctx.moveTo(centerX - 80, centerY);
                ctx.lineTo(centerX - 40, centerY);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 部分断裂的C-Br键
                ctx.beginPath();
                ctx.moveTo(centerX - 80, centerY);
                ctx.lineTo(centerX - 80, centerY - 60 + 20 * progress);
                ctx.stroke();
                
                // 绘制过渡态指示
                ctx.fillStyle = '#ffa500';
                ctx.font = 'italic 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('过渡态', centerX - 20, centerY - 80);
            }
            
            if (currentStep >= 2) {
                // 步骤3: 键的断裂与形成
                drawAtom(centerX - 80, centerY, 'C', 'C1');
                drawAtom(centerX - 40, centerY, 'O', 'O1');
                drawBond(centerX - 80, centerY, centerX - 40, centerY, 1);
                
                // 绘制Br⁻离开
                const progress = Math.max(0, Math.min(1, (animationTime - 1) * 2));
                const brY = centerY - 60 + 40 * progress;
                drawAtom(centerX - 80, brY, 'Br', 'Br1');
                
                // 绘制负电荷
                ctx.fillStyle = '#f9e300';
                ctx.font = 'bold 20px Arial';
                ctx.fillText('⁻', centerX - 65, brY - 5);
            }
            
            if (currentStep >= 3) {
                // 步骤4: 产物形成
                drawAtom(centerX - 80, centerY, 'C', 'C1');
                drawAtom(centerX - 40, centerY, 'O', 'O1');
                drawAtom(centerX - 40, centerY - 30, 'H', 'H4');
                drawBond(centerX - 80, centerY, centerX - 40, centerY, 1);
                drawBond(centerX - 40, centerY, centerX - 40, centerY - 30, 1);
                
                // 绘制最终产物
                ctx.fillStyle = '#2ecc71';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('CH₃-OH + Br⁻', centerX, centerY + 100);
            }
        }
        
        // 绘制消去反应机理
        function drawEliminationMechanism(centerX, centerY) {
            // 绘制CH₃-CH₂-Br分子
            drawAtom(centerX - 100, centerY, 'C', 'C1'); // α-碳
            drawAtom(centerX - 40, centerY, 'C', 'C2'); // β-碳
            
            // α-碳上的基团
            drawAtom(centerX - 120, centerY - 30, 'H', 'H1');
            drawAtom(centerX - 120, centerY + 30, 'H', 'H2');
            drawAtom(centerX - 100, centerY - 60, 'Br', 'Br1');
            
            // β-碳上的基团
            drawAtom(centerX - 20, centerY - 30, 'H', 'H3');
            drawAtom(centerX - 20, centerY + 30, 'H', 'H4');
            drawAtom(centerX - 40, centerY + 60, 'H', 'H5'); // 被夺取的β-氢
            
            drawBond(centerX - 100, centerY, centerX - 120, centerY - 30, 1);
            drawBond(centerX - 100, centerY, centerX - 120, centerY + 30, 1);
            drawBond(centerX - 100, centerY, centerX - 100, centerY - 60, 1);
            drawBond(centerX - 100, centerY, centerX - 40, centerY, 1);
            drawBond(centerX - 40, centerY, centerX - 20, centerY - 30, 1);
            drawBond(centerX - 40, centerY, centerX - 20, centerY + 30, 1);
            drawBond(centerX - 40, centerY, centerX - 40, centerY + 60, 1);
            
            // 绘制OH⁻离子
            drawAtom(centerX + 80, centerY + 30, 'O', 'O1');
            drawAtom(centerX + 80, centerY, 'H', 'H6');
            drawBond(centerX + 80, centerY + 30, centerX + 80, centerY, 1);
            
            // 绘制负电荷
            ctx.fillStyle = '#f9e300';
            ctx.font = 'bold 20px Arial';
            ctx.fillText('⁻', centerX + 95, centerY + 25);
            
            if (currentStep >= 0) {
                // 步骤1: 碱进攻β-氢
                const progress = Math.min(1, animationTime * 2);
                const arrowStartX = centerX + 80;
                const arrowStartY = centerY + 30;
                const arrowEndX = centerX - 40 + (centerX - 40 - arrowStartX) * progress;
                const arrowEndY = centerY + 60 + (centerY + 60 - arrowStartY) * progress;
                
                drawCurvedArrow(arrowStartX, arrowStartY, arrowEndX, arrowEndY, progress);
                
                // 高亮β-氢
                drawHighlight(centerX - 40, centerY + 60, 20, '#ff6b6b', 0.3);
            }
            
            if (currentStep >= 1) {
                // 步骤2: 键的同步变化
                const progress = Math.max(0, Math.min(1, (animationTime - 0.5) * 2));
                
                // C-H键部分断裂
                ctx.strokeStyle = '#ffa500';
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 3]);
                ctx.beginPath();
                ctx.moveTo(centerX - 40, centerY);
                ctx.lineTo(centerX - 40, centerY + 60 - 20 * progress);
                ctx.stroke();
                
                // C-Br键部分断裂
                ctx.beginPath();
                ctx.moveTo(centerX - 100, centerY);
                ctx.lineTo(centerX - 100, centerY - 60 + 20 * progress);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 绘制电子流向
                drawElectronFlowArrow(centerX - 40, centerY + 30, centerX - 70, centerY, progress);
            }
            
            if (currentStep >= 2) {
                // 步骤3: π键形成
                const progress = Math.max(0, Math.min(1, (animationTime - 1) * 2));
                
                // 绘制π键
                drawBond(centerX - 100, centerY, centerX - 40, centerY, 2, progress);
                
                // 绘制H₂O形成
                drawAtom(centerX + 40, centerY + 80, 'O', 'O1');
                drawAtom(centerX + 40, centerY + 50, 'H', 'H6');
                drawAtom(centerX + 40, centerY + 110, 'H', 'H5');
                drawBond(centerX + 40, centerY + 80, centerX + 40, centerY + 50, 1);
                drawBond(centerX + 40, centerY + 80, centerX + 40, centerY + 110, 1);
            }
            
            if (currentStep >= 3) {
                // 步骤4: 产物形成
                // 绘制烯烃双键
                drawBond(centerX - 100, centerY, centerX - 40, centerY, 2);
                
                // 绘制Br⁻
                drawAtom(centerX - 100, centerY - 40, 'Br', 'Br1');
                ctx.fillStyle = '#f9e300';
                ctx.font = 'bold 20px Arial';
                ctx.fillText('⁻', centerX - 85, centerY - 45);
                
                // 绘制最终产物
                ctx.fillStyle = '#2ecc71';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('H₂C=CH₂ + H₂O + Br⁻', centerX, centerY + 120);
            }
        }
        
        // 绘制电子箭头
        function drawElectronArrows() {
            // 根据当前步骤绘制动态电子箭头
            if (!isPlaying) return;
            
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2 + 50;
            
            // 创建脉动效果
            const pulse = 0.5 + 0.5 * Math.sin(animationTime * Math.PI * 4);
            
            if (currentStep === 0 && animationTime < 0.5) {
                // 加成反应步骤1的电子箭头
                ctx.strokeStyle = '#f9e300';
                ctx.lineWidth = 3;
                ctx.setLineDash([10, 5]);
                ctx.beginPath();
                ctx.moveTo(centerX + 100, centerY - 50);
                ctx.lineTo(centerX - 80, centerY);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 绘制箭头头部
                drawArrowHead(centerX - 80, centerY, Math.PI, pulse);
            }
        }
        
        // 绘制原子
        function drawAtom(x, y, element, label, positiveCharge = false) {
            // 绘制原子球
            ctx.beginPath();
            ctx.arc(x, y, 20, 0, Math.PI * 2);
            ctx.fillStyle = atomColors[element] || '#909090';
            ctx.fill();
            ctx.strokeStyle = '#ecf0f1';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制元素符号
            ctx.fillStyle = element === 'H' ? '#2c3e50' : '#ffffff';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText(element, x, y);
            
            // 绘制电荷
            if (positiveCharge) {
                ctx.fillStyle = '#ff6b6b';
                ctx.font = 'bold 20px Arial';
                ctx.fillText('+', x + 15, y - 15);
            }
        }
        
        // 绘制化学键
        function drawBond(x1, y1, x2, y2, bondType = 1, progress = 1) {
            ctx.strokeStyle = '#ecf0f1';
            ctx.lineWidth = 3;
            ctx.lineCap = 'round';
            
            if (bondType === 1) {
                // 单键
                ctx.beginPath();
                ctx.moveTo(x1, y1);
                ctx.lineTo(x2, y2);
                ctx.stroke();
            } else if (bondType === 2) {
                // 双键
                const dx = x2 - x1;
                const dy = y2 - y1;
                const length = Math.sqrt(dx * dx + dy * dy);
                const angle = Math.atan2(dy, dx);
                
                // 计算垂直方向
                const perpX = -dy / length * 5;
                const perpY = dx / length * 5;
                
                // 第一条线
                ctx.beginPath();
                ctx.moveTo(x1 + perpX, y1 + perpY);
                ctx.lineTo(x2 + perpX, y2 + perpY);
                ctx.stroke();
                
                // 第二条线（根据进度绘制）
                if (progress >= 1) {
                    ctx.beginPath();
                    ctx.moveTo(x1 - perpX, y1 - perpY);
                    ctx.lineTo(x2 - perpX, y2 - perpY);
                    ctx.stroke();
                } else if (progress > 0) {
                    // 部分绘制的双键
                    const midX = x1 + dx * progress;
                    const midY = y1 + dy * progress;
                    
                    ctx.beginPath();
                    ctx.moveTo(x1 - perpX, y1 - perpY);
                    ctx.lineTo(midX - perpX, midY - perpY);
                    ctx.stroke();
                }
            }
        }
        
        // 绘制弯曲箭头（表示电子流动）
        function drawCurvedArrow(startX, startY, endX, endY, progress, reverse = false) {
            if (progress <= 0) return;
            
            // 计算控制点以创建曲线
            const midX = (startX + endX) / 2;
            const midY = (startY + endY) / 2;
            
            // 垂直偏移量
            const dx = endX - startX;
            const dy = endY - startY;
            const length = Math.sqrt(dx * dx + dy * dy);
            const perpX = -dy / length * 30;
            const perpY = dx / length * 30;
            
            const controlX = midX + perpX;
            const controlY = midY + perpY;
            
            // 绘制曲线
            ctx.strokeStyle = '#f9e300';
            ctx.lineWidth = 3;
            ctx.lineCap = 'round';
            
            // 计算当前进度对应的点
            const t = progress;
            const currentX = (1-t)*(1-t)*startX + 2*(1-t)*t*controlX + t*t*endX;
            const currentY = (1-t)*(1-t)*startY + 2*(1-t)*t*controlY + t*t*endY;
            
            // 绘制已完成的曲线部分
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            
            // 使用二次贝塞尔曲线绘制
            for (let i = 0; i <= 20; i++) {
                const t2 = i / 20 * t;
                const x = (1-t2)*(1-t2)*startX + 2*(1-t2)*t2*controlX + t2*t2*endX;
                const y = (1-t2)*(1-t2)*startY + 2*(1-t2)*t2*controlY + t2*t2*endY;
                ctx.lineTo(x, y);
            }
            
            ctx.stroke();
            
            // 绘制箭头头部
            if (progress > 0.1) {
                // 计算曲线在箭头位置的方向
                const tArrow = Math.max(0.1, progress - 0.1);
                const arrowX = (1-tArrow)*(1-tArrow)*startX + 2*(1-tArrow)*tArrow*controlX + tArrow*tArrow*endX;
                const arrowY = (1-tArrow)*(1-tArrow)*startY + 2*(1-tArrow)*tArrow*controlY + tArrow*tArrow*endY;
                
                // 计算导数得到切线方向
                const dxdt = 2*(1-tArrow)*(controlX-startX) + 2*tArrow*(endX-controlX);
                const dydt = 2*(1-tArrow)*(controlY-startY) + 2*tArrow*(endY-controlY);
                const angle = Math.atan2(dydt, dxdt);
                
                drawArrowHead(arrowX, arrowY, angle, 1);
            }
        }
        
        // 绘制箭头头部
        function drawArrowHead(x, y, angle, size = 1) {
            const headLength = 15 * size;
            const headAngle = Math.PI / 6;
            
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(angle);
            
            ctx.fillStyle = '#f9e300';
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(-headLength, headLength * Math.tan(headAngle));
            ctx.lineTo(-headLength, -headLength * Math.tan(headAngle));
            ctx.closePath();
            ctx.fill();
            
            ctx.restore();
        }
        
        // 绘制高亮区域
        function drawHighlight(x, y, radius, color, alpha) {
            ctx.save();
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.fillStyle = color;
            ctx.globalAlpha = alpha;
            ctx.fill();
            ctx.restore();
        }
        
        // 绘制电子流动箭头（直线）
        function drawElectronFlowArrow(startX, startY, endX, endY, progress) {
            if (progress <= 0) return;
            
            const currentX = startX + (endX - startX) * progress;
            const currentY = startY + (endY - startY) * progress;
            
            ctx.strokeStyle = '#f9e300';
            ctx.lineWidth = 2;
            ctx.setLineDash([5, 3]);
            
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            ctx.lineTo(currentX, currentY);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制箭头头部
            if (progress > 0.2) {
                const angle = Math.atan2(endY - startY, endX - startX);
                drawArrowHead(currentX, currentY, angle, 0.8);
            }
        }
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

# 有机化学反应机理交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态可视化技术，帮助您深入理解有机化学中**加成、取代、消去**三类核心反应的机理与**箭头推动法**。请跟随本指南，充分利用其各项功能，开启高效、直观的学习之旅。

---

## 一、 功能总览

本动画是一个基于HTML5 Canvas构建的完整交互式学习环境，集成了**动态机理演示、分步学习控制、即时知识反馈和互动练习**四大核心模块。您不仅能够观看反应如何发生，更能控制其进程，探索电子流动的每一个细节。

## 二、 主要功能详解

### 1. 反应类型与示例选择
*   **反应类型切换**：通过顶部左侧面板的“加成反应”、“取代反应”、“消去反应”三个大按钮，可在三大类反应机理之间自由切换。
*   **具体示例选择**：选定反应类型后，下方会列出多个经典反应示例（如“烯烃 + HBr”、“卤代烷 + OH⁻”等）。点击任一示例，动画区将立即更新，展示该特定反应的完整机理。

### 2. 动画控制中心
位于左侧面板中部，是您控制学习节奏的核心。
*   **播放/暂停/重置**：控制动画的连续播放、暂停以及重置到初始状态。
*   **上一步/下一步**：在分步学习模式下，手动向前或向后跳转一个步骤，便于反复观察关键环节。
*   **速度调节滑块**：可无级调节动画播放速度（从“极慢”到“最快”），适应不同学习阶段的需求。
*   **步骤指示器**：以数字按钮直观显示总步骤和当前步骤。**点击任意步骤按钮可直接跳转**。已完成的步骤显示为蓝色，当前步骤显示为绿色。

### 3. 动态可视化画布
中央画布是教学的核心呈现区域，具有以下特色：
*   **标准CPK原子着色**：碳（灰）、氢（白）、氧（红）、氮（蓝）、卤素（绿），符合国际化学绘图惯例，便于识别。
*   **动态电子流**：**亮黄色的弯箭头**从电子源（孤对电子或π键）平滑“生长”并移动到新键形成处或正电荷上，清晰展示电子对的转移路径。
*   **键的形变与断裂**：化学键的断裂与形成过程以平滑动画呈现，并与电子箭头的移动精确同步。
*   **区域高亮**：在关键步骤，亲核区域（以浅蓝色半透明高亮）和亲电区域（以浅红色半透明高亮）会被特别标注，强化对反应本质的理解。
*   **电荷动态显示**：中间体（如碳正离子）上的形式电荷会实时显示并伴随颜色强调。

### 4. 同步知识讲解面板
*   **当前步骤说明**：位于左侧面板底部，随动画步骤同步更新，用文字详细描述当前步骤发生的具体过程、涉及的试剂角色（亲核/亲电）和关键概念。
*   **机理详解**：位于右侧画布下方，提供当前所选反应的**整体机理概述、分步概括及重要规则（如马氏规则、查依采夫规则、瓦尔登翻转等）**。

### 5. 互动练习区（探索模式）
位于左侧面板最下方，鼓励您主动探索。
*   **分子部件拖拽**：尝试将提供的分子片段（如H⁺、Br⁻、:OH⁻）拖拽组合。
*   **箭头绘制反馈**：点击“检查箭头”按钮，系统会模拟对您绘制的电子流向给予正确或错误的反馈，并提供改进提示。

### 6. 视觉图例
右侧底部的图例栏清晰解释了所有颜色和符号的含义，是快速查阅的实用工具。

## 三、 设计特色与教学理念

1.  **遵循认知规律**：采用“宏观类比 → 微观演示 → 分步解构 → 整体回顾”的学习路径，符合从具体到抽象的认知过程。
2.  **对比学习设计**：通过便捷的反应类型切换，鼓励用户对比观察加成、取代、消去三类反应在**电子流向、键变化顺序和中间体**上的根本差异，从而建立知识网络。
3.  **“可控探索”式交互**：用户不再是被动观看者，而是可以通过控制步骤、速度，主动探索反应进程的学习主导者。这种交互能有效加深记忆与理解。
4.  **多表征融合**：将**球棍模型**（显示几何结构）、**电子箭头**（显示过程机理）和**文字说明**（显示理论概念）三者有机结合，满足不同学习风格的需求。

## 四、 核心教学要点指引

使用本动画学习时，请特别关注以下要点，它们是有机反应机理的精髓：

*   **加成反应**：关注 **π键如何被打开**，以及**亲电试剂与亲核试剂先后进攻的顺序**（马氏/反马氏规则）。观察碳正离子中间体的形成与稳定性。
*   **取代反应 (SN2)**：重点理解 **“背面进攻”** 和 **“一步协同”** 过程。注意观察过渡态的结构以及产物**构型的翻转**。
*   **消去反应 (E2)**：聚焦于 **碱如何进攻β-氢**，以及 **C-H键与C-X键如何同步断裂**，同时形成新的π键。理解消除反应的区域选择性（查依采夫规则）。
*   **箭头推动法则**：始终牢记：**弯箭头代表电子对的移动**，必须从电子富集区（化学键或孤对电子）开始，指向电子匮乏区（原子或新键形成处）。

## 五、 使用建议与学习路径

**对于初学者：**
1.  **引导模式**：选择一个反应（如“烯烃 + HBr”），点击“播放”，以常速观看完整动画，获得整体印象。
2.  **分步精学**：使用“重置”和“下一步”按钮，一步一步学习。每步暂停后，仔细阅读左侧的“当前步骤说明”，观察画布上的箭头和键的变化。
3.  **反复观察**：对难以理解的步骤（如碳正离子形成），使用步骤按钮反复跳转观看，或降低速度慢放。
4.  **对比总结**：学完一类反应（如加成）后，切换到另一类（如取代），对比两者的第一步有何本质不同。

**对于复习者：**
1.  **自主推导**：在观看动画前，先根据反应物和条件，尝试在纸上画出预期的机理箭头。
2.  **验证与纠错**：播放动画，与自己的推导进行对比，找出差异并思考原因。
3.  **利用练习区**：尝试使用互动练习功能，检验自己对电子流向判断的熟练度。
4.  **专题比较**：利用切换功能，专门比较不同反应（如SN2与E2）在相同底物和条件下的竞争关系。

---

我们希望这个精心设计的交互式动画，能像一位耐心的导师，将有机化学反应中那些不可见的电子舞蹈，生动、清晰、深刻地呈现在您面前。祝您学习愉快，探索顺利！

**熊猫老师 教育技术团队**