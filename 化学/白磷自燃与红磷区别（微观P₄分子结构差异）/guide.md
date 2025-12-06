# 需求：白磷自燃与红磷区别（微观P₄分子结构差异）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要是中学或大学低年级的化学学习者。他们需要：
1.  **理解核心差异**：直观理解白磷和红磷在宏观性质（如自燃性、稳定性）上的巨大差异，其根本原因在于微观分子结构的不同。
2.  **建立结构-性质关联**：深刻建立“分子结构 → 分子间作用力/化学键能 → 宏观性质”的化学核心思维模型。
3.  **突破抽象难点**：P₄分子结构（正四面体）和红磷的链状/网状结构较为抽象，需要通过动态、可交互的模型来降低认知负荷。
4.  **激发探究兴趣**：通过生动的动画和交互，将枯燥的结构知识转化为有趣的探索过程。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念**：
    *   **白磷**：由**离散的P₄分子**构成，分子呈**正四面体**结构，键角小（60°），存在角张力，化学活性高。
    *   **红磷**：由P₄分子**开环、聚合**形成的**链状或网状巨型分子**，键角更接近理想键角，结构稳定。
    *   **结构决定性质**：白磷分子间为**范德华力**，作用力弱，易挥发、着火点低（自燃）；红磷原子间以**共价键**连接成巨型结构，稳定，着火点高。
    *   **相互转化**：在隔绝空气加热条件下，两者可以相互转化，本质是P₄分子的聚合与解聚。

*   **认知规律**：
    1.  **从宏观到微观**：先展示白磷（自燃）和红磷（稳定）的宏观现象对比，引发疑问，再切入微观解释。
    2.  **从静态到动态**：先观察静态的分子结构，再通过动画演示“键角张力”、“聚合过程”和“自燃反应”。
    3.  **从观察到操作**：允许用户旋转、缩放分子模型，点击触发关键过程，从被动接收变为主动探索。
    4.  **归纳与联系**：最后通过对比表格或图示，系统梳理二者在多个维度上的差异，强化结构-性质观。

*   **交互设计**：
    *   **模块化导航**：设计清晰的标签页或按钮，如“宏观现象”、“白磷结构”、“红磷结构”、“转化过程”、“对比总结”。
    *   **模型操控**：提供3D（或伪3D）可旋转、缩放的白磷P₄分子和红磷结构片段模型。
    *   **过程控制**：为“聚合”、“自燃”等关键动画提供播放/暂停/重置控制条。
    *   **焦点提示**：当讲解特定部分时（如P₄的键角），模型对应部分应高亮或闪烁。
    *   **对比查看**：在总结部分，并排显示两种结构的模型，用户鼠标悬停时显示对应性质的文字说明。

*   **视觉呈现**：
    *   **分子模型**：采用“球棍模型”。磷原子用**橙色**球体（与磷单质颜色关联），共价键用灰色或浅灰色的棍棒连接。
    *   **动态效果**：
        *   用颤动的弹簧或弯曲的键来表示P₄分子中的“角张力”。
        *   用平滑的动画展示P₄分子开环、连接形成红磷长链的过程。
        *   白磷自燃时，用从P₄分子向O₂分子扩散的箭头表示反应的高活性，并结合火焰动画。
    *   **布局与动线**：界面简洁，视觉焦点明确。动画和解释文字同步出现，符合“邻近原则”。

#### 配色方案选择
*   **主色调**：采用**深蓝色（#1a237e）** 或深灰色作为背景，营造科学、专注的实验室氛围，并能突出前景的分子模型。
*   **模型色**：
    *   **磷原子**：**橙色（#FF9800）**，贴近红磷的色泽，同时与白磷的“黄白色”有联系，保持一致性。
    *   **共价键**：浅灰色（#CCCCCC）或银色，中性且不喧宾夺主。
    *   **氧原子**：红色（#F44336），用于自燃动画中，表示氧气和氧化反应。
*   **UI与强调色**：
    *   **高亮/激活色**：亮黄色（#FFEB3B）或青色（#00BCD4），用于按钮悬停、分子键角高亮等。
    *   **文字与边框**：白色或浅灰色（#E0E0E0），确保可读性。
    *   **安全提示色**：在展示白磷自燃时，使用红色背景或边框，并配以警示图标，强调其危险性。

#### 交互功能列表
1.  **场景切换器**：按钮或标签页，用于在“宏观对比”、“白磷微观”、“红磷微观”、“转化过程”、“总结”五个核心场景间切换。
2.  **3D分子查看器**：
    *   鼠标拖拽旋转白磷P₄四面体或红磷结构模型。
    *   鼠标滚轮缩放模型。
    *   点击“重置视图”按钮恢复默认视角。
3.  **动画控制器**：
    *   “展示键角张力”按钮：触发P₄分子键的颤动动画，并显示60°键角与理想键角的对比数据。
    *   “聚合为红磷”按钮：播放一个/多个P₄分子断裂键、连接成链的动画。
    *   “模拟自燃”按钮：播放白磷与氧气接触、引发燃烧的动画（伴随温和的视觉与声音效果）。
    *   通用控制：播放、暂停、重播。
4.  **焦点提示与标注**：
    *   鼠标悬停在模型特定原子或键上时，显示名称（如“磷原子”、“P-P键”）或关键数据（“键角：60°”）。
    *   在动画过程中，关键步骤配有文字标注和箭头指示。
5.  **对比悬停提示**：在总结模块，将性质（如“着火点”、“稳定性”、“毒性”）列表与分子模型并列。鼠标悬停在某个性质上时，对应的两种分子模型会进行突出显示（如高亮相关结构部分）。
6.  **知识卡片**：点击“i”图标，弹出关于历史、应用或安全注意事项的扩展阅读小卡片。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>白磷与红磷：微观结构决定宏观性质</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0a0f2b 0%, #1a237e 100%);
            color: #e0e0e0;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: rgba(25, 30, 70, 0.8);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(100, 120, 255, 0.2);
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid rgba(255, 152, 0, 0.5);
        }
        
        h1 {
            color: #FF9800;
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 5px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            color: #00BCD4;
            font-size: 1.2rem;
            font-weight: 300;
        }
        
        .scene-selector {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 30px;
        }
        
        .scene-btn {
            background-color: rgba(30, 40, 100, 0.8);
            color: #e0e0e0;
            border: 2px solid #00BCD4;
            border-radius: 50px;
            padding: 12px 25px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            min-width: 150px;
        }
        
        .scene-btn:hover {
            background-color: rgba(0, 188, 212, 0.2);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 188, 212, 0.4);
        }
        
        .scene-btn.active {
            background-color: #00BCD4;
            color: #0a0f2b;
            box-shadow: 0 0 15px rgba(0, 188, 212, 0.7);
        }
        
        .scene-container {
            display: none;
            opacity: 0;
            transition: opacity 0.5s ease;
        }
        
        .scene-container.active {
            display: block;
            opacity: 1;
        }
        
        .scene-title {
            color: #FFEB3B;
            font-size: 1.8rem;
            margin-bottom: 20px;
            text-align: center;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(255, 235, 59, 0.3);
        }
        
        .content-area {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .animation-area {
            flex: 1;
            min-width: 300px;
            background-color: rgba(10, 15, 40, 0.7);
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .canvas-container {
            width: 100%;
            height: 400px;
            position: relative;
            margin-bottom: 20px;
            border-radius: 8px;
            overflow: hidden;
            background-color: rgba(20, 25, 60, 0.9);
            border: 1px solid rgba(100, 120, 255, 0.3);
        }
        
        canvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            width: 100%;
        }
        
        .control-btn {
            background-color: rgba(255, 152, 0, 0.8);
            color: #0a0f2b;
            border: none;
            border-radius: 5px;
            padding: 10px 15px;
            font-size: 0.9rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            min-width: 120px;
        }
        
        .control-btn:hover {
            background-color: #FF9800;
            transform: translateY(-2px);
            box-shadow: 0 5px 10px rgba(255, 152, 0, 0.4);
        }
        
        .control-btn:disabled {
            background-color: rgba(100, 100, 100, 0.5);
            color: #888;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }
        
        .info-area {
            flex: 1;
            min-width: 300px;
            background-color: rgba(10, 15, 40, 0.7);
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
        }
        
        .info-title {
            color: #00BCD4;
            font-size: 1.4rem;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid rgba(0, 188, 212, 0.3);
        }
        
        .info-content {
            flex-grow: 1;
            overflow-y: auto;
            max-height: 350px;
            padding-right: 10px;
        }
        
        .info-content p {
            margin-bottom: 15px;
            text-align: justify;
        }
        
        .highlight {
            color: #FFEB3B;
            font-weight: 600;
        }
        
        .warning {
            color: #F44336;
            font-weight: 600;
            background-color: rgba(244, 67, 54, 0.1);
            padding: 10px;
            border-radius: 5px;
            border-left: 4px solid #F44336;
            margin-top: 15px;
        }
        
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        
        .comparison-table th, .comparison-table td {
            border: 1px solid rgba(100, 120, 255, 0.3);
            padding: 12px;
            text-align: center;
        }
        
        .comparison-table th {
            background-color: rgba(0, 188, 212, 0.2);
            color: #00BCD4;
        }
        
        .comparison-table td {
            background-color: rgba(30, 40, 100, 0.3);
        }
        
        .white-phosphorus {
            color: #FF9800;
            font-weight: 600;
        }
        
        .red-phosphorus {
            color: #F44336;
            font-weight: 600;
        }
        
        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            flex-wrap: wrap;
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
        
        .legend-text {
            font-size: 0.9rem;
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 152, 0, 0.3);
            color: #90a4ae;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .content-area {
                flex-direction: column;
            }
            
            .scene-btn {
                min-width: 120px;
                padding: 10px 15px;
                font-size: 0.9rem;
            }
            
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>白磷与红磷：微观结构决定宏观性质</h1>
            <p class="subtitle">探索P₄分子结构差异如何导致截然不同的化学性质</p>
        </header>
        
        <div class="scene-selector">
            <button class="scene-btn active" data-scene="macro">宏观现象对比</button>
            <button class="scene-btn" data-scene="white">白磷微观结构</button>
            <button class="scene-btn" data-scene="red">红磷微观结构</button>
            <button class="scene-btn" data-scene="transformation">相互转化过程</button>
            <button class="scene-btn" data-scene="comparison">性质对比总结</button>
        </div>
        
        <!-- 场景1: 宏观现象对比 -->
        <div id="macro-scene" class="scene-container active">
            <h2 class="scene-title">宏观现象对比</h2>
            <div class="content-area">
                <div class="animation-area">
                    <div class="canvas-container">
                        <canvas id="macro-canvas"></canvas>
                    </div>
                    <div class="controls">
                        <button class="control-btn" id="show-white">展示白磷自燃</button>
                        <button class="control-btn" id="show-red">展示红磷稳定性</button>
                        <button class="control-btn" id="reset-macro">重置</button>
                    </div>
                </div>
                <div class="info-area">
                    <h3 class="info-title">宏观现象观察</h3>
                    <div class="info-content">
                        <p>白磷和红磷是磷元素的两种常见同素异形体，它们在宏观性质上表现出<strong class="highlight">截然不同的行为</strong>。</p>
                        
                        <p><span class="white-phosphorus">白磷</span>：常温下为蜡状固体，呈淡黄色（纯品为白色）。在空气中会缓慢氧化，产生的热量积聚导致温度升高，当达到约<span class="highlight">40°C</span>时便会<strong class="warning">自燃</strong>，产生浓厚的白烟（P₄O₁₀）。</p>
                        
                        <p><span class="red-phosphorus">红磷</span>：为暗红色粉末，化学性质稳定。在空气中需加热到约<span class="highlight">260°C</span>才会燃烧，不会自燃。</p>
                        
                        <p>这种巨大的性质差异源于它们<strong class="highlight">完全不同的微观分子结构</strong>，这正是本教学动画要揭示的核心内容。</p>
                        
                        <div class="warning">
                            <strong>安全警示：</strong>白磷有剧毒且极易自燃，实验室中必须在水下保存，操作时需极其小心！
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 场景2: 白磷微观结构 -->
        <div id="white-scene" class="scene-container">
            <h2 class="scene-title">白磷微观结构：P₄分子</h2>
            <div class="content-area">
                <div class="animation-area">
                    <div class="canvas-container">
                        <canvas id="white-canvas"></canvas>
                    </div>
                    <div class="controls">
                        <button class="control-btn" id="rotate-white">旋转分子</button>
                        <button class="control-btn" id="show-angle">展示键角张力</button>
                        <button class="control-btn" id="combustion">模拟自燃反应</button>
                        <button class="control-btn" id="reset-white">重置视图</button>
                    </div>
                </div>
                <div class="info-area">
                    <h3 class="info-title">白磷结构解析</h3>
                    <div class="info-content">
                        <p>白磷由<strong class="highlight">离散的P₄分子</strong>组成，每个P₄分子呈<strong class="highlight">正四面体</strong>结构。</p>
                        
                        <p>每个磷原子通过共价键与其他三个磷原子连接，形成<strong class="highlight">P-P单键</strong>。</p>
                        
                        <p>关键特征：键角仅为<span class="highlight">60°</span>，而磷原子轨道的理想键角约为<span class="highlight">109.5°</span>。这种巨大的差异导致P₄分子中存在强烈的<strong class="highlight">角张力</strong>，使化学键变得脆弱、反应活性极高。</p>
                        
                        <p>分子间作用：P₄分子之间仅靠较弱的<strong class="highlight">范德华力</strong>结合，这使得白磷熔点低（44.1°C）、易挥发。</p>
                        
                        <p>自燃原因：角张力使P-P键易断裂，白磷挥发后与氧气接触，断键所需的活化能低，在常温下即可发生剧烈氧化反应，释放大量热导致自燃。</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 场景3: 红磷微观结构 -->
        <div id="red-scene" class="scene-container">
            <h2 class="scene-title">红磷微观结构：链状/网状巨型分子</h2>
            <div class="content-area">
                <div class="animation-area">
                    <div class="canvas-container">
                        <canvas id="red-canvas"></canvas>
                    </div>
                    <div class="controls">
                        <button class="control-btn" id="rotate-red">旋转结构</button>
                        <button class="control-btn" id="show-bond">展示理想键角</button>
                        <button class="control-btn" id="show-stability">展示稳定性</button>
                        <button class="control-btn" id="reset-red">重置视图</button>
                    </div>
                </div>
                <div class="info-area">
                    <h3 class="info-title">红磷结构解析</h3>
                    <div class="info-content">
                        <p>红磷是由P₄分子<strong class="highlight">开环、聚合</strong>形成的<strong class="highlight">链状或网状巨型分子</strong>。</p>
                        
                        <p>在红磷结构中，每个磷原子与相邻的三个磷原子形成共价键，但键角更接近理想的<span class="highlight">~100°</span>，<strong class="highlight">角张力大大减小</strong>，结构更加稳定。</p>
                        
                        <p>红磷是一个<strong class="highlight">聚合物</strong>，没有确定的分子式，通常用(P)ₙ表示。</p>
                        
                        <p>结构特点：整个红磷固体可以看作一个巨型分子，原子间全部以<strong class="highlight">强共价键</strong>连接，没有离散的小分子。</p>
                        
                        <p>稳定性来源：</p>
                        <ol>
                            <li>键角接近理想值，角张力小</li>
                            <li>巨型共价结构，破坏需要断裂大量强共价键</li>
                            <li>不易挥发，与氧气接触面积小</li>
                        </ol>
                        <p>因此红磷化学性质稳定，着火点高，无毒性。</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 场景4: 相互转化过程 -->
        <div id="transformation-scene" class="scene-container">
            <h2 class="scene-title">白磷与红磷的相互转化</h2>
            <div class="content-area">
                <div class="animation-area">
                    <div class="canvas-container">
                        <canvas id="transformation-canvas"></canvas>
                    </div>
                    <div class="controls">
                        <button class="control-btn" id="to-red">白磷→红磷</button>
                        <button class="control-btn" id="to-white">红磷→白磷</button>
                        <button class="control-btn" id="pause-trans">暂停/继续</button>
                        <button class="control-btn" id="reset-trans">重置</button>
                    </div>
                </div>
                <div class="info-area">
                    <h3 class="info-title">转化过程解析</h3>
                    <div class="info-content">
                        <p>在<strong class="highlight">隔绝空气</strong>的条件下加热，白磷和红磷可以相互转化：</p>
                        
                        <p><strong class="white-phosphorus">白磷 → 红磷</strong>：加热到<span class="highlight">260-300°C</span>，多个P₄分子中的P-P键断裂，然后重新连接形成链状或网状结构。</p>
                        
                        <p>转化本质：P₄分子的<strong class="highlight">聚合反应</strong>。多个小分子结合成巨型分子，释放能量。</p>
                        
                        <p><strong class="red-phosphorus">红磷 → 白磷</strong>：加热到<span class="highlight">416°C</span>升华后冷凝，巨型结构解聚为P₄小分子。</p>
                        
                        <p>转化本质：巨型分子的<strong class="highlight">解聚反应</strong>。需要吸收能量破坏大量共价键。</p>
                        
                        <p>重要条件：<strong class="warning">必须隔绝空气</strong>，否则磷会与氧气反应生成氧化物。</p>
                        
                        <p>这种相互转化证明了白磷和红磷具有<strong class="highlight">相同的组成元素</strong>，只是<strong class="highlight">原子排列方式不同</strong>，是典型的同素异形体关系。</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- 场景5: 性质对比总结 -->
        <div id="comparison-scene" class="scene-container">
            <h2 class="scene-title">性质对比总结</h2>
            <div class="content-area">
                <div class="animation-area">
                    <div class="canvas-container">
                        <canvas id="comparison-canvas"></canvas>
                    </div>
                    <div class="controls">
                        <button class="control-btn" id="highlight-structure">高亮结构差异</button>
                        <button class="control-btn" id="highlight-bond">高亮化学键</button>
                        <button class="control-btn" id="show-property">关联性质差异</button>
                        <button class="control-btn" id="reset-comp">重置</button>
                    </div>
                </div>
                <div class="info-area">
                    <h3 class="info-title">结构-性质关系总结</h3>
                    <div class="info-content">
                        <table class="comparison-table">
                            <thead>
                                <tr>
                                    <th>性质</th>
                                    <th>白磷</th>
                                    <th>红磷</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td>分子结构</td>
                                    <td class="white-phosphorus">P₄正四面体分子</td>
                                    <td class="red-phosphorus">(P)ₙ链状/网状结构</td>
                                </tr>
                                <tr>
                                    <td>键角</td>
                                    <td>60°（角张力大）</td>
                                    <td>~100°（接近理想）</td>
                                </tr>
                                <tr>
                                    <td>分子间作用</td>
                                    <td>范德华力（弱）</td>
                                    <td>共价键（强）</td>
                                </tr>
                                <tr>
                                    <td>着火点</td>
                                    <td>~40°C（自燃）</td>
                                    <td>~260°C</td>
                                </tr>
                                <tr>
                                    <td>毒性</td>
                                    <td>剧毒</td>
                                    <td>基本无毒</td>
                                </tr>
                                <tr>
                                    <td>稳定性</td>
                                    <td>不稳定，需水下保存</td>
                                    <td>稳定，空气中保存</td>
                                </tr>
                                <tr>
                                    <td>化学活性</td>
                                    <td>高</td>
                                    <td>低</td>
                                </tr>
                            </tbody>
                        </table>
                        
                        <p><strong class="highlight">核心结论：</strong></p>
                        <p>白磷和红磷的性质差异完全由它们的<strong class="highlight">微观结构差异</strong>决定：</p>
                        <ul>
                            <li>P₄分子的角张力 → 高反应活性 → 自燃性</li>
                            <li>离散小分子 vs 巨型分子 → 挥发性差异 → 毒性差异</li>
                            <li>范德华力 vs 共价键 → 物理性质差异</li>
                        </ul>
                        <p>这是"<strong class="highlight">结构决定性质</strong>"这一化学核心思想的完美例证。</p>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="legend">
            <div class="legend-item">
                <div class="legend-color" style="background-color: #FF9800;"></div>
                <div class="legend-text">磷原子</div>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #CCCCCC;"></div>
                <div class="legend-text">P-P共价键</div>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #F44336;"></div>
                <div class="legend-text">氧原子</div>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #00BCD4;"></div>
                <div class="legend-text">高亮/激活</div>
            </div>
        </div>
        
        <footer>
            <p>教学动画 | 化学微观结构可视化 | 结构决定性质 | 设计：教育技术专家</p>
            <p>提示：点击不同场景按钮探索白磷与红磷的微观世界</p>
        </footer>
    </div>

    <script>
        // 全局变量和配置
        const config = {
            atomColor: "#FF9800",
            bondColor: "#CCCCCC",
            oxygenColor: "#F44336",
            highlightColor: "#00BCD4",
            backgroundColor: "#14193C"
        };
        
        // 场景管理
        const sceneButtons = document.querySelectorAll('.scene-btn');
        const scenes = document.querySelectorAll('.scene-container');
        
        sceneButtons.forEach(button => {
            button.addEventListener('click', () => {
                const sceneId = button.getAttribute('data-scene');
                
                // 更新按钮状态
                sceneButtons.forEach(btn => btn.classList.remove('active'));
                button.classList.add('active');
                
                // 切换场景
                scenes.forEach(scene => {
                    scene.classList.remove('active');
                });
                
                document.getElementById(`${sceneId}-scene`).classList.add('active');
                
                // 重置所有canvas
                resetAllCanvases();
            });
        });
        
        // Canvas上下文获取
        const macroCtx = document.getElementById('macro-canvas').getContext('2d');
        const whiteCtx = document.getElementById('white-canvas').getContext('2d');
        const redCtx = document.getElementById('red-canvas').getContext('2d');
        const transCtx = document.getElementById('transformation-canvas').getContext('2d');
        const compCtx = document.getElementById('comparison-canvas').getContext('2d');
        
        // 设置所有canvas尺寸
        function resizeCanvases() {
            const canvases = document.querySelectorAll('canvas');
            canvases.forEach(canvas => {
                const container = canvas.parentElement;
                canvas.width = container.clientWidth;
                canvas.height = container.clientHeight;
            });
        }
        
        // 初始化时设置canvas尺寸
        window.addEventListener('load', resizeCanvases);
        window.addEventListener('resize', resizeCanvases);
        
        // 重置所有canvas
        function resetAllCanvases() {
            // 重置每个canvas的绘制状态
            drawMacroScene(true);
            drawWhitePhosphorus(true);
            drawRedPhosphorus(true);
            drawTransformation(true);
            drawComparison(true);
        }
        
        // ==================== 场景1: 宏观现象对比 ====================
        let macroState = {
            whiteBurning: false,
            redStable: false,
            flameFrame: 0
        };
        
        document.getElementById('show-white').addEventListener('click', () => {
            macroState.whiteBurning = true;
            macroState.redStable = false;
            animateMacroScene();
        });
        
        document.getElementById('show-red').addEventListener('click', () => {
            macroState.whiteBurning = false;
            macroState.redStable = true;
            animateMacroScene();
        });
        
        document.getElementById('reset-macro').addEventListener('click', () => {
            macroState.whiteBurning = false;
            macroState.redStable = false;
            macroState.flameFrame = 0;
            drawMacroScene(true);
        });
        
        function drawMacroScene(reset = false) {
            const canvas = macroCtx.canvas;
            const width = canvas.width;
            const height = canvas.height;
            
            if (reset) {
                macroCtx.clearRect(0, 0, width, height);
                
                // 绘制背景
                macroCtx.fillStyle = config.backgroundColor;
                macroCtx.fillRect(0, 0, width, height);
                
                // 绘制标题
                macroCtx.fillStyle = '#FFEB3B';
                macroCtx.font = 'bold 18px Arial';
                macroCtx.textAlign = 'center';
                macroCtx.fillText('宏观现象对比', width/2, 30);
                
                // 绘制白磷区域
                macroCtx.fillStyle = 'rgba(255, 152, 0, 0.1)';
                macroCtx.fillRect(width/4 - 100, height/2 - 80, 200, 160);
                macroCtx.strokeStyle = '#FF9800';
                macroCtx.lineWidth = 2;
                macroCtx.strokeRect(width/4 - 100, height/2 - 80, 200, 160);
                
                macroCtx.fillStyle = '#FF9800';
                macroCtx.font = 'bold 16px Arial';
                macroCtx.fillText('白磷', width/4, height/2 - 90);
                
                // 绘制红磷区域
                macroCtx.fillStyle = 'rgba(244, 67, 54, 0.1)';
                macroCtx.fillRect(3*width/4 - 100, height/2 - 80, 200, 160);
                macroCtx.strokeStyle = '#F44336';
                macroCtx.lineWidth = 2;
                macroCtx.strokeRect(3*width/4 - 100, height/2 - 80, 200, 160);
                
                macroCtx.fillStyle = '#F44336';
                macroCtx.font = 'bold 16px Arial';
                macroCtx.fillText('红磷', 3*width/4, height/2 - 90);
                
                // 绘制白磷分子示意
                drawP4Molecule(macroCtx, width/4, height/2, 30, false);
                
                // 绘制红磷结构示意
                drawRedStructure(macroCtx, 3*width/4, height/2, 40, false);
                
                // 绘制说明文字
                macroCtx.fillStyle = '#e0e0e0';
                macroCtx.font = '14px Arial';
                macroCtx.textAlign = 'center';
                macroCtx.fillText('点击按钮观察不同现象', width/2, height - 30);
            }
        }
        
        function animateMacroScene() {
            const canvas = macroCtx.canvas;
            const width = canvas.width;
            const height = canvas.height;
            
            macroCtx.clearRect(0, 0, width, height);
            
            // 绘制背景和静态元素
            drawMacroScene(true);
            
            // 更新火焰动画帧
            macroState.flameFrame++;
            
            // 绘制白磷自燃效果
            if (macroState.whiteBurning) {
                // 绘制火焰
                const flameHeight = 30 + 10 * Math.sin(macroState.flameFrame * 0.2);
                drawFlame(macroCtx, width/4, height/2 - 50, flameHeight);
                
                // 绘制烟雾
                for (let i = 0; i < 5; i++) {
                    const smokeX = width/4 - 30 + i * 15;
                    const smokeY = height/2 - 80 - (macroState.flameFrame % 30) - i * 5;
                    const smokeSize = 8 + i * 2;
                    drawSmoke(macroCtx, smokeX, smokeY, smokeSize);
                }
                
                // 绘制警示标志
                macroCtx.fillStyle = '#F44336';
                macroCtx.font = 'bold 20px Arial';
                macroCtx.fillText('自燃！', width/4, height/2 + 100);
            }
            
            // 绘制红磷稳定性效果
            if (macroState.redStable) {
                // 绘制稳定符号（对勾）
                macroCtx.strokeStyle = '#4CAF50';
                macroCtx.lineWidth = 3;
                macroCtx.beginPath();
                macroCtx.moveTo(3*width/4 - 20, height/2 - 20);
                macroCtx.lineTo(3*width/4 - 5, height/2);
                macroCtx.lineTo(3*width/4 + 25, height/2 - 30);
                macroCtx.stroke();
                
                // 绘制稳定文字
                macroCtx.fillStyle = '#4CAF50';
                macroCtx.font = 'bold 20px Arial';
                macroCtx.fillText('稳定', 3*width/4, height/2 + 100);
            }
            
            if (macroState.whiteBurning || macroState.redStable) {
                requestAnimationFrame(animateMacroScene);
            }
        }
        
        function drawFlame(ctx, x, y, height) {
            ctx.fillStyle = '#FF5722';
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.bezierCurveTo(x - 15, y - height/2, x - 10, y - height, x, y - height);
            ctx.bezierCurveTo(x + 10, y - height, x + 15, y - height/2, x, y);
            ctx.fill();
            
            ctx.fillStyle = '#FFEB3B';
            ctx.beginPath();
            ctx.moveTo(x, y - 10);
            ctx.bezierCurveTo(x - 10, y - height/3, x - 8, y - height*0.7, x, y - height*0.8);
            ctx.bezierCurveTo(x + 8, y - height*0.7, x + 10, y - height/3, x, y - 10);
            ctx.fill();
        }
        
        function drawSmoke(ctx, x, y, size) {
            ctx.fillStyle = 'rgba(255, 255, 255, 0.7)';
            ctx.beginPath();
            ctx.arc(x, y, size, 0, Math.PI * 2);
            ctx.fill();
        }
        
        // ==================== 场景2: 白磷微观结构 ====================
        let whiteState = {
            rotation: { x: 0, y: 0 },
            angleTension: false,
            combustion: false,
            autoRotate: false,
            combustionFrame: 0
        };
        
        document.getElementById('rotate-white').addEventListener('click', () => {
            whiteState.autoRotate = !whiteState.autoRotate;
            if (whiteState.autoRotate) {
                animateWhitePhosphorus();
            }
        });
        
        document.getElementById('show-angle').addEventListener('click', () => {
            whiteState.angleTension = true;
            whiteState.combustion = false;
            drawWhitePhosphorus();
            
            // 3秒后自动关闭高亮
            setTimeout(() => {
                whiteState.angleTension = false;
                drawWhitePhosphorus();
            }, 3000);
        });
        
        document.getElementById('combustion').addEventListener('click', () => {
            whiteState.combustion = true;
            whiteState.combustionFrame = 0;
            whiteState.angleTension = false;
            animateCombustion();
        });
        
        document.getElementById('reset-white').addEventListener('click', () => {
            whiteState.rotation = { x: 0, y: 0 };
            whiteState.angleTension = false;
            whiteState.combustion = false;
            whiteState.autoRotate = false;
            whiteState.combustionFrame = 0;
            drawWhitePhosphorus(true);
        });
        
        // 绘制P4分子函数
        function drawP4Molecule(ctx, centerX, centerY, size, showLabels = true) {
            // P4正四面体顶点坐标（3D投影到2D）
            const scale = size;
            const vertices = [
                { x: 0, y: -1, z: 0 },        // 顶部
                { x: 0.94, y: 0.33, z: 0 },   // 底部右前
                { x: -0.47, y: 0.33, z: 0.82 }, // 底部左前
                { x: -0.47, y: 0.33, z: -0.82 } // 底部左后
            ];
            
            // 应用旋转
            const rotatedVertices = vertices.map(v => {
                // 绕Y轴旋转
                let x = v.x * Math.cos(whiteState.rotation.y) - v.z * Math.sin(whiteState.rotation.y);
                let z = v.x * Math.sin(whiteState.rotation.y) + v.z * Math.cos(whiteState.rotation.y);
                let y = v.y;
                
                // 绕X轴旋转
                let y2 = y * Math.cos(whiteState.rotation.x) - z * Math.sin(whiteState.rotation.x);
                let z2 = y * Math.sin(whiteState.rotation.x) + z * Math.cos(whiteState.rotation.x);
                
                return { x: x * scale, y: y2 * scale, z: z2 };
            });
            
            // 绘制化学键
            ctx.strokeStyle = whiteState.angleTension ? config.highlightColor : config.bondColor;
            ctx.lineWidth = whiteState.angleTension ? 4 : 2;
            
            // 四面体的6条边
            const edges = [
                [0, 1], [0, 2], [0, 3],
                [1, 2], [1, 3], [2, 3]
            ];
            
            edges.forEach(edge => {
                const v1 = rotatedVertices
<!--检测到代码截断，自动续写中...-->
[edge[0]];
                const v2 = rotatedVertices[edge[1]];
                
                ctx.beginPath();
                ctx.moveTo(centerX + v1.x, centerY + v1.y);
                ctx.lineTo(centerX + v2.x, centerY + v2.y);
                ctx.stroke();
            });
            
            // 绘制磷原子
            rotatedVertices.forEach((v, i) => {
                ctx.fillStyle = config.atomColor;
                ctx.beginPath();
                ctx.arc(centerX + v.x, centerY + v.y, 8, 0, Math.PI * 2);
                ctx.fill();
                
                // 添加原子标签
                if (showLabels) {
                    ctx.fillStyle = '#FFFFFF';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText('P', centerX + v.x, centerY + v.y);
                }
            });
            
            // 如果显示键角张力，绘制角度标注
            if (whiteState.angleTension) {
                ctx.strokeStyle = config.highlightColor;
                ctx.lineWidth = 1;
                ctx.fillStyle = config.highlightColor;
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                
                // 绘制一个键角示例（顶点0到1和0到2的夹角）
                const v0 = rotatedVertices[0];
                const v1 = rotatedVertices[1];
                const v2 = rotatedVertices[2];
                
                // 计算角度标注位置
                const angleX = centerX + v0.x + (v1.x + v2.x) / 6;
                const angleY = centerY + v0.y + (v1.y + v2.y) / 6;
                
                // 绘制角度弧线
                ctx.beginPath();
                const radius = 15;
                ctx.arc(centerX + v0.x, centerY + v0.y, radius, 
                       Math.atan2(v1.y - v0.y, v1.x - v0.x),
                       Math.atan2(v2.y - v0.y, v2.x - v0.x));
                ctx.stroke();
                
                // 标注角度值
                ctx.fillText('60°', angleX, angleY);
                
                // 绘制理想键角对比
                ctx.fillStyle = '#FFEB3B';
                ctx.fillText('理想键角: ~109.5°', centerX, centerY + size + 40);
            }
        }
        
        function drawWhitePhosphorus(reset = false) {
            const canvas = whiteCtx.canvas;
            const width = canvas.width;
            const height = canvas.height;
            
            if (reset) {
                whiteCtx.clearRect(0, 0, width, height);
                
                // 绘制背景
                whiteCtx.fillStyle = config.backgroundColor;
                whiteCtx.fillRect(0, 0, width, height);
                
                // 绘制标题
                whiteCtx.fillStyle = '#FFEB3B';
                whiteCtx.font = 'bold 16px Arial';
                whiteCtx.textAlign = 'center';
                whiteCtx.fillText('白磷分子结构: P₄正四面体', width/2, 30);
            } else {
                whiteCtx.clearRect(0, 0, width, height);
                whiteCtx.fillStyle = config.backgroundColor;
                whiteCtx.fillRect(0, 0, width, height);
                
                whiteCtx.fillStyle = '#FFEB3B';
                whiteCtx.font = 'bold 16px Arial';
                whiteCtx.textAlign = 'center';
                whiteCtx.fillText('白磷分子结构: P₄正四面体', width/2, 30);
            }
            
            // 绘制P4分子
            drawP4Molecule(whiteCtx, width/2, height/2, Math.min(width, height)/4);
            
            // 绘制分子式
            whiteCtx.fillStyle = '#e0e0e0';
            whiteCtx.font = 'bold 24px Arial';
            whiteCtx.fillText('P₄', width/2, height - 40);
            
            // 如果正在自燃，绘制火焰效果
            if (whiteState.combustion) {
                drawCombustionEffect(whiteCtx, width/2, height/2 - 80);
            }
        }
        
        function animateWhitePhosphorus() {
            if (whiteState.autoRotate) {
                whiteState.rotation.y += 0.02;
                whiteState.rotation.x += 0.01;
                drawWhitePhosphorus();
                requestAnimationFrame(animateWhitePhosphorus);
            }
        }
        
        function animateCombustion() {
            whiteState.combustionFrame++;
            
            drawWhitePhosphorus();
            
            if (whiteState.combustionFrame < 100) {
                requestAnimationFrame(animateCombustion);
            } else {
                whiteState.combustion = false;
                drawWhitePhosphorus();
            }
        }
        
        function drawCombustionEffect(ctx, centerX, centerY) {
            const frame = whiteState.combustionFrame;
            
            // 绘制多个火焰
            for (let i = 0; i < 3; i++) {
                const flameX = centerX - 40 + i * 40;
                const flameY = centerY + 20 * Math.sin(frame * 0.1 + i);
                const flameHeight = 30 + 15 * Math.sin(frame * 0.15 + i * 2);
                
                drawFlame(ctx, flameX, flameY, flameHeight);
            }
            
            // 绘制氧气分子向P4移动的动画
            const oxygenCount = 6;
            for (let i = 0; i < oxygenCount; i++) {
                const angle = (i / oxygenCount) * Math.PI * 2 + frame * 0.05;
                const radius = 100 + frame * 2;
                const ox = centerX + Math.cos(angle) * radius;
                const oy = centerY + Math.sin(angle) * radius;
                
                // 绘制氧气分子（O₂）
                ctx.fillStyle = config.oxygenColor;
                ctx.beginPath();
                ctx.arc(ox - 5, oy, 5, 0, Math.PI * 2);
                ctx.arc(ox + 5, oy, 5, 0, Math.PI * 2);
                ctx.fill();
                
                // 绘制连接线
                ctx.strokeStyle = 'rgba(244, 67, 54, 0.5)';
                ctx.lineWidth = 1;
                ctx.beginPath();
                ctx.moveTo(ox, oy);
                ctx.lineTo(centerX, centerY);
                ctx.stroke();
            }
            
            // 绘制反应方程式
            ctx.fillStyle = '#FFEB3B';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('P₄ + 5O₂ → P₄O₁₀ + 热量', centerX, centerY + 150);
        }
        
        // ==================== 场景3: 红磷微观结构 ====================
        let redState = {
            rotation: { x: 0, y: 0 },
            showBondAngle: false,
            showStability: false,
            autoRotate: false
        };
        
        document.getElementById('rotate-red').addEventListener('click', () => {
            redState.autoRotate = !redState.autoRotate;
            if (redState.autoRotate) {
                animateRedPhosphorus();
            }
        });
        
        document.getElementById('show-bond').addEventListener('click', () => {
            redState.showBondAngle = true;
            redState.showStability = false;
            drawRedPhosphorus();
            
            setTimeout(() => {
                redState.showBondAngle = false;
                drawRedPhosphorus();
            }, 3000);
        });
        
        document.getElementById('show-stability').addEventListener('click', () => {
            redState.showStability = true;
            redState.showBondAngle = false;
            drawRedPhosphorus();
            
            setTimeout(() => {
                redState.showStability = false;
                drawRedPhosphorus();
            }, 3000);
        });
        
        document.getElementById('reset-red').addEventListener('click', () => {
            redState.rotation = { x: 0, y: 0 };
            redState.showBondAngle = false;
            redState.showStability = false;
            redState.autoRotate = false;
            drawRedPhosphorus(true);
        });
        
        function drawRedStructure(ctx, centerX, centerY, size, showLabels = true) {
            // 绘制红磷的链状结构片段
            const segmentCount = 5;
            const atomSpacing = size * 0.8;
            
            // 创建链状结构原子位置
            const atoms = [];
            for (let i = 0; i < segmentCount; i++) {
                // 主链原子
                atoms.push({
                    x: centerX - atomSpacing * 2 + i * atomSpacing,
                    y: centerY,
                    connections: []
                });
                
                // 侧链原子（每隔一个主链原子添加）
                if (i % 2 === 0 && i > 0 && i < segmentCount - 1) {
                    atoms.push({
                        x: centerX - atomSpacing * 2 + i * atomSpacing,
                        y: centerY - atomSpacing * 0.7,
                        connections: []
                    });
                }
            }
            
            // 定义连接关系
            for (let i = 0; i < atoms.length; i++) {
                // 连接相邻的主链原子
                if (i < segmentCount - 1) {
                    atoms[i].connections.push(i + 1);
                }
                
                // 连接侧链原子到主链
                if (i >= segmentCount && i < atoms.length) {
                    const mainChainIndex = Math.floor((i - segmentCount) * 2) + 2;
                    if (mainChainIndex < segmentCount) {
                        atoms[i].connections.push(mainChainIndex);
                        atoms[mainChainIndex].connections.push(i);
                    }
                }
            }
            
            // 应用旋转
            const rotatedAtoms = atoms.map(atom => {
                // 转换为相对于中心的坐标
                const relX = atom.x - centerX;
                const relY = atom.y - centerY;
                
                // 绕Y轴旋转（简化2D旋转）
                const cosY = Math.cos(redState.rotation.y);
                const sinY = Math.sin(redState.rotation.y);
                const x = relX * cosY - relY * sinY;
                const y = relX * sinY + relY * cosY;
                
                return {
                    x: centerX + x,
                    y: centerY + y,
                    connections: atom.connections
                };
            });
            
            // 绘制化学键
            ctx.strokeStyle = redState.showBondAngle ? config.highlightColor : config.bondColor;
            ctx.lineWidth = redState.showBondAngle ? 4 : 2;
            
            rotatedAtoms.forEach((atom, i) => {
                atom.connections.forEach(connIndex => {
                    if (connIndex > i) { // 避免重复绘制
                        const connAtom = rotatedAtoms[connIndex];
                        ctx.beginPath();
                        ctx.moveTo(atom.x, atom.y);
                        ctx.lineTo(connAtom.x, connAtom.y);
                        ctx.stroke();
                    }
                });
            });
            
            // 绘制磷原子
            rotatedAtoms.forEach((atom, i) => {
                ctx.fillStyle = config.atomColor;
                ctx.beginPath();
                ctx.arc(atom.x, atom.y, 8, 0, Math.PI * 2);
                ctx.fill();
                
                if (showLabels) {
                    ctx.fillStyle = '#FFFFFF';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText('P', atom.x, atom.y);
                }
            });
            
            // 如果显示键角，绘制角度标注
            if (redState.showBondAngle && rotatedAtoms.length >= 3) {
                // 选择三个相连的原子来展示键角
                const atom1 = rotatedAtoms[1];
                const atom2 = rotatedAtoms[2];
                const atom3 = rotatedAtoms[4];
                
                if (atom1 && atom2 && atom3) {
                    ctx.strokeStyle = config.highlightColor;
                    ctx.lineWidth = 1;
                    ctx.fillStyle = config.highlightColor;
                    ctx.font = 'bold 14px Arial';
                    ctx.textAlign = 'center';
                    
                    // 绘制角度弧线（以atom2为中心）
                    const radius = 20;
                    const angle1 = Math.atan2(atom1.y - atom2.y, atom1.x - atom2.x);
                    const angle2 = Math.atan2(atom3.y - atom2.y, atom3.x - atom2.x);
                    
                    ctx.beginPath();
                    ctx.arc(atom2.x, atom2.y, radius, angle1, angle2);
                    ctx.stroke();
                    
                    // 标注角度值
                    const angleX = atom2.x + Math.cos((angle1 + angle2) / 2) * (radius + 10);
                    const angleY = atom2.y + Math.sin((angle1 + angle2) / 2) * (radius + 10);
                    ctx.fillText('~100°', angleX, angleY);
                    
                    // 绘制理想键角对比
                    ctx.fillStyle = '#FFEB3B';
                    ctx.fillText('接近理想键角', centerX, centerY + size + 40);
                }
            }
            
            // 如果显示稳定性，绘制稳定符号
            if (redState.showStability) {
                ctx.strokeStyle = '#4CAF50';
                ctx.lineWidth = 3;
                
                // 绘制多个对勾符号
                for (let i = 0; i < 3; i++) {
                    const checkX = centerX - 50 + i * 50;
                    const checkY = centerY - 60;
                    
                    ctx.beginPath();
                    ctx.moveTo(checkX - 10, checkY);
                    ctx.lineTo(checkX, checkY + 10);
                    ctx.lineTo(checkX + 20, checkY - 10);
                    ctx.stroke();
                }
                
                ctx.fillStyle = '#4CAF50';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('结构稳定', centerX, centerY + size + 40);
            }
        }
        
        function drawRedPhosphorus(reset = false) {
            const canvas = redCtx.canvas;
            const width = canvas.width;
            const height = canvas.height;
            
            if (reset) {
                redCtx.clearRect(0, 0, width, height);
                
                // 绘制背景
                redCtx.fillStyle = config.backgroundColor;
                redCtx.fillRect(0, 0, width, height);
                
                // 绘制标题
                redCtx.fillStyle = '#FFEB3B';
                redCtx.font = 'bold 16px Arial';
                redCtx.textAlign = 'center';
                redCtx.fillText('红磷结构: 链状/网状巨型分子', width/2, 30);
            } else {
                redCtx.clearRect(0, 0, width, height);
                redCtx.fillStyle = config.backgroundColor;
                redCtx.fillRect(0, 0, width, height);
                
                redCtx.fillStyle = '#FFEB3B';
                redCtx.font = 'bold 16px Arial';
                redCtx.textAlign = 'center';
                redCtx.fillText('红磷结构: 链状/网状巨型分子', width/2, 30);
            }
            
            // 绘制红磷结构
            drawRedStructure(redCtx, width/2, height/2, Math.min(width, height)/4);
            
            // 绘制分子式
            redCtx.fillStyle = '#e0e0e0';
            redCtx.font = 'bold 24px Arial';
            redCtx.fillText('(P)ₙ', width/2, height - 40);
            
            // 绘制结构说明
            redCtx.fillStyle = '#90a4ae';
            redCtx.font = '14px Arial';
            redCtx.fillText('n值很大，为巨型分子结构', width/2, height - 70);
        }
        
        function animateRedPhosphorus() {
            if (redState.autoRotate) {
                redState.rotation.y += 0.015;
                redState.rotation.x += 0.007;
                drawRedPhosphorus();
                requestAnimationFrame(animateRedPhosphorus);
            }
        }
        
        // ==================== 场景4: 相互转化过程 ====================
        let transState = {
            toRedProgress: 0,
            toWhiteProgress: 0,
            isAnimating: false,
            animationDirection: 0, // 0: 无, 1: 白→红, 2: 红→白
            animationFrame: 0
        };
        
        document.getElementById('to-red').addEventListener('click', () => {
            if (!transState.isAnimating) {
                transState.animationDirection = 1;
                transState.isAnimating = true;
                transState.animationFrame = 0;
                transState.toRedProgress = 0;
                animateTransformation();
            }
        });
        
        document.getElementById('to-white').addEventListener('click', () => {
            if (!transState.isAnimating) {
                transState.animationDirection = 2;
                transState.isAnimating = true;
                transState.animationFrame = 0;
                transState.toWhiteProgress = 0;
                animateTransformation();
            }
        });
        
        document.getElementById('pause-trans').addEventListener('click', () => {
            transState.isAnimating = !transState.isAnimating;
            if (transState.isAnimating) {
                animateTransformation();
            }
        });
        
        document.getElementById('reset-trans').addEventListener('click', () => {
            transState.toRedProgress = 0;
            transState.toWhiteProgress = 0;
            transState.isAnimating = false;
            transState.animationDirection = 0;
            transState.animationFrame = 0;
            drawTransformation(true);
        });
        
        function drawTransformation(reset = false) {
            const canvas = transCtx.canvas;
            const width = canvas.width;
            const height = canvas.height;
            
            if (reset) {
                transCtx.clearRect(0, 0, width, height);
                
                // 绘制背景
                transCtx.fillStyle = config.backgroundColor;
                transCtx.fillRect(0, 0, width, height);
                
                // 绘制标题
                transCtx.fillStyle = '#FFEB3B';
                transCtx.font = 'bold 16px Arial';
                transCtx.textAlign = 'center';
                transCtx.fillText('白磷与红磷的相互转化', width/2, 30);
            } else {
                transCtx.clearRect(0, 0, width, height);
                transCtx.fillStyle = config.backgroundColor;
                transCtx.fillRect(0, 0, width, height);
                
                transCtx.fillStyle = '#FFEB3B';
                transCtx.font = 'bold 16px Arial';
                transCtx.textAlign = 'center';
                transCtx.fillText('白磷与红磷的相互转化', width/2, 30);
            }
            
            // 绘制左侧白磷分子
            const leftX = width / 3;
            const centerY = height / 2;
            const size = Math.min(width, height) / 6;
            
            // 绘制多个P4分子
            const p4Count = 4;
            for (let i = 0; i < p4Count; i++) {
                const offsetX = (i % 2) * 40 - 20;
                const offsetY = Math.floor(i / 2) * 40 - 20;
                
                // 根据转化进度调整透明度
                let opacity = 1;
                if (transState.animationDirection === 1) {
                    opacity = 1 - transState.toRedProgress;
                } else if (transState.animationDirection === 2 && transState.toWhiteProgress > 0) {
                    opacity = transState.toWhiteProgress;
                }
                
                transCtx.globalAlpha = opacity;
                drawP4Molecule(transCtx, leftX + offsetX, centerY + offsetY, size * 0.7, false);
                transCtx.globalAlpha = 1;
            }
            
            // 绘制右侧红磷结构
            const rightX = 2 * width / 3;
            
            // 根据转化进度调整透明度
            let redOpacity = 1;
            if (transState.animationDirection === 1) {
                redOpacity = transState.toRedProgress;
            } else if (transState.animationDirection === 2) {
                redOpacity = 1 - transState.toWhiteProgress;
            }
            
            transCtx.globalAlpha = redOpacity;
            drawRedStructure(transCtx, rightX, centerY, size * 0.9, false);
            transCtx.globalAlpha = 1;
            
            // 绘制转化箭头
            transCtx.strokeStyle = '#00BCD4';
            transCtx.lineWidth = 3;
            transCtx.fillStyle = '#00BCD4';
            
            // 左箭头（白→红）
            const arrowY = centerY - 60;
            drawArrow(transCtx, leftX + 60, arrowY, rightX - 60, arrowY);
            
            // 右箭头（红→白）
            const arrowY2 = centerY + 60;
            drawArrow(transCtx, rightX - 60, arrowY2, leftX + 60, arrowY2);
            
            // 标注转化条件
            transCtx.fillStyle = '#e0e0e0';
            transCtx.font = '14px Arial';
            transCtx.textAlign = 'center';
            
            transCtx.fillText('加热 ~260-300°C', width/2, arrowY - 15);
            transCtx.fillText('隔绝空气', width/2, arrowY);
            
            transCtx.fillText('加热 ~416°C', width/2, arrowY2 + 25);
            transCtx.fillText('升华后冷凝', width/2, arrowY2 + 40);
            
            // 绘制转化过程中的中间状态（断键/成键动画）
            if (transState.isAnimating) {
                drawTransformationAnimation(transCtx, width/2, centerY, size);
            }
            
            // 绘制分子式
            transCtx.fillStyle = '#FF9800';
            transCtx.font = 'bold 20px Arial';
            transCtx.fillText('P₄', leftX, centerY + size + 50);
            
            transCtx.fillStyle = '#F44336';
            transCtx.fillText('(P)ₙ', rightX, centerY + size + 50);
        }
        
        function drawArrow(ctx, fromX, fromY, toX, toY) {
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.stroke();
            
            // 绘制箭头头部
            const angle = Math.atan2(toY - fromY, toX - fromX);
            const headLength = 10;
            
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headLength * Math.cos(angle - Math.PI/6), 
                      toY - headLength * Math.sin(angle - Math.PI/6));
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headLength * Math.cos(angle + Math.PI/6), 
                      toY - headLength * Math.sin(angle + Math.PI/6));
            ctx.stroke();
        }
        
        function drawTransformationAnimation(ctx, centerX, centerY, size) {
            const frame = transState.animationFrame;
            
            if (transState.animationDirection === 1) { // 白→红
                // 绘制断键/成键过程
                const progress = transState.toRedProgress;
                
                // 绘制断裂的键
                ctx.strokeStyle = '#F44336';
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 5]);
                
                const breakX = centerX - 30 + progress * 60;
                const breakY = centerY - 20;
                
                ctx.beginPath();
                ctx.moveTo(breakX - 20, breakY);
                ctx.lineTo(breakX + 20, breakY);
                ctx.stroke();
                
                ctx.setLineDash([]);
                
                // 绘制新形成的键
                ctx.strokeStyle = '#4CAF50';
                ctx.lineWidth = 2 * progress;
                
                const newBondX = centerX;
                const newBondY = centerY + 20;
                
                ctx.beginPath();
                ctx.moveTo(newBondX - 30, newBondY);
                ctx.lineTo(newBondX + 30, newBondY);
                ctx.stroke();
                
                // 绘制聚合文字
                ctx.fillStyle = '#FFEB3B';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('聚合反应', centerX, centerY - 50);
                
            } else if (transState.animationDirection === 2) { // 红→白
                // 绘制解聚过程
                const progress = transState.toWhiteProgress;
                
                // 绘制断裂的键
                ctx.strokeStyle = '#F44336';
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 5]);
                
                const breakX = centerX;
                const breakY = centerY + 20 - progress * 40;
                
                ctx.beginPath();
                ctx.moveTo(breakX - 30, breakY);
                ctx.lineTo(breakX + 30, breakY);
                ctx.stroke();
                
                ctx.setLineDash([]);
                
                // 绘制解聚文字
                ctx.fillStyle = '#FFEB3B';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('解聚反应', centerX, centerY - 50);
            }
            
            // 绘制热量符号
            ctx.fillStyle = '#FF9800';
            ctx.font = 'bold 24px Arial';
            
            if (transState.animationDirection === 1) {
                // 放热反应
                ctx.fillText('+ 热量', centerX, centerY + 60);
            } else if (transState.animationDirection === 2) {
                // 吸热反应
                ctx.fillText('- 热量', centerX, centerY + 60);
            }
        }
        
        function animateTransformation() {
            if (!transState.isAnimating) return;
            
            transState.animationFrame++;
            
            // 更新转化进度
            if (transState.animationDirection === 1) { // 白→红
                transState.toRedProgress = Math.min(1, transState.toRedProgress + 0.02);
                if (transState.toRedProgress >= 1) {
                    transState.isAnimating = false;
                }
            } else if (transState.animationDirection === 2) { // 红→白
                transState.toWhiteProgress = Math.min(1, transState.toWhiteProgress + 0.02);
                if (transState.toWhiteProgress >= 1) {
                    transState.isAnimating = false;
                }
            }
            
            drawTransformation();
            
            if (transState.isAnimating) {
                requestAnimationFrame(animateTransformation);
            }
        }
        
        // ==================== 场景5: 性质对比总结 ====================
        let compState = {
            highlightStructure: false,
            highlightBond: false,
            showProperty: false,
            currentProperty: 0
        };
        
        const properties = [
            { name: "分子结构", white: "P₄正四面体", red: "(P)ₙ链状/网状" },
            { name: "键角", white: "60°（角张力大）", red: "~100°（接近理想）" },
            { name: "分子间作用", white: "范德华力（弱）", red: "共价键（强）" },
            { name: "着火点", white: "~40°C（自燃）", red: "~260°C" },
            { name: "毒性", white: "剧毒", red: "基本无毒" },
            { name: "稳定性", white: "不稳定，需水下保存", red: "稳定，空气中保存" }
        ];
        
        document.getElementById('highlight-structure').addEventListener('click', () => {
            compState.highlightStructure = !compState.highlightStructure;
            compState.highlightBond = false;
            compState.showProperty = false;
            drawComparison();
        });
        
        document.getElementById('highlight-bond').addEventListener('click', () => {
            compState.highlightBond = !compState.highlightBond;
            compState.highlightStructure = false;
            compState.showProperty = false;
            drawComparison();
        });
        
        document.getElementById('show-property').addEventListener('click', () => {
            compState.showProperty = !compState.showProperty;
            compState.highlightStructure = false;
            compState.highlightBond = false;
            if (compState.showProperty) {
                animatePropertyCycle();
            }
            drawComparison();
        });
        
        document.getElementById('reset-comp').addEventListener('click', () => {
            compState.highlightStructure = false;
            compState.highlightBond = false;
            compState.showProperty = false;
            compState.currentProperty = 0;
            drawComparison(true);
        });
        
        function drawComparison(reset = false) {
            const canvas = compCtx.canvas;
            const width = canvas.width;
            const height = canvas.height;
            
            if (reset) {
                compCtx.clearRect(0, 0, width, height);
                
                // 绘制背景
                compCtx.fillStyle = config.backgroundColor;
                compCtx.fillRect(0, 0, width, height);
                
                // 绘制标题
                compCtx.fillStyle = '#FFEB3B';
                compCtx.font = 'bold 16px Arial';
                compCtx.textAlign = 'center';
                compCtx.fillText('白磷与红磷性质对比总结', width/2, 30);
            } else {
                compCtx.clearRect(0, 0, width, height);
                compCtx.fillStyle = config.backgroundColor;
                compCtx.fillRect(0, 0, width, height);
                
                compCtx.fillStyle = '#FFEB3B';
                compCtx.font = 'bold 16px Arial';
                compCtx.textAlign = 'center';
                compCtx.fillText('白磷与红磷性质对比总结', width/2, 30);
            }
            
            // 绘制左侧白磷
            const leftX = width / 3;
            const centerY = height / 2;
            const size = Math.min(width, height) / 6;
            
            // 绘制白磷分子
            if (compState.highlightStructure) {
                compCtx.fillStyle = 'rgba(0, 188, 212, 0.2)';
                compCtx.fillRect(leftX - size - 20, centerY - size - 20, size * 2 + 40, size * 2 + 40);
            }
            
            drawP4Molecule(compCtx, leftX, centerY, size * 0.8, false);
            
            // 绘制右侧红磷
            const rightX = 2 * width / 3;
            
            if (compState.highlightStructure) {
                compCtx.fillStyle = 'rgba(0, 188, 212, 0.2)';
                compCtx.fillRect(rightX - size - 20, centerY - size - 20, size * 2 + 40, size * 2 + 40);
            }
            
            drawRedStructure(compCtx, rightX, centerY, size * 0.9, false);
            
            // 绘制标签
            compCtx.fillStyle = '#FF9800';
            compCtx.font = 'bold 20px Arial';
            compCtx.textAlign = 'center';
            compCtx.fillText('白磷', leftX, centerY + size + 40);
            
            compCtx.fillStyle = '#F44336';
            compCtx.fillText('红磷', rightX, centerY + size + 40);
            
            // 绘制对比箭头
            compCtx.strokeStyle = '#00BCD4';
            compCtx.lineWidth = 2;
            drawArrow(compCtx, leftX + 40, centerY - size - 10, rightX - 40, centerY - size - 10);
            
            // 绘制核心结论
            compCtx.fillStyle = '#FFEB3B';
            compCtx.font = 'bold 18px Arial';
            compCtx.fillText('结构决定性质', width/2, centerY + size + 80);
            
            // 如果高亮键，绘制键的对比
            if (compState.highlightBond) {
                // 白磷的弱范德华力
                compCtx.strokeStyle = '#FF9800';
                compCtx.lineWidth = 1;
                compCtx.setLineDash([2, 2]);
                
                compCtx.beginPath();
                compCtx.moveTo(leftX - 50, centerY - 30);
                compCtx.lineTo(leftX + 50, centerY - 30);
                compCtx.stroke();
                
                compCtx.setLineDash([]);
                compCtx.fillStyle = '#FF9800';
                compCtx.font = '14px Arial';
                compCtx.fillText('范德华力（弱）', leftX, centerY - 40);
                
                // 红磷的强共价键
                compCtx.strokeStyle = '#F44336';
                compCtx.lineWidth = 3;
                
                compCtx.beginPath();
                compCtx.moveTo(rightX - 50, centerY - 30);
                compCtx.lineTo(rightX + 50, centerY - 30);
                compCtx.stroke();
                
                compCtx.fillStyle = '#F44336';
                compCtx.fillText('共价键（强）', rightX, centerY - 40);
            }
            
            // 如果显示性质关联，绘制当前性质
            if (compState.showProperty) {
                const property = properties[compState.currentProperty % properties.length];
                
                compCtx.fillStyle = '#00BCD4';
                compCtx.font = 'bold 18px Arial';
                compCtx.fillText(property.name, width/2, 70);
                
                compCtx.fillStyle = '#FF9800';
                compCtx.font = '16px Arial';
                compCtx.fillText(property.white, leftX, centerY - size - 30);
                
                compCtx.fillStyle = '#F44336';
                compCtx.fillText(property.red, rightX, centerY - size - 30);
                
                // 绘制连接线
                compCtx.strokeStyle = 'rgba(0, 188, 212, 0.5)';
                compCtx.lineWidth = 2;
                compCtx.setLineDash([5, 3]);
                
                compCtx.beginPath();
                compCtx.moveTo(width/2, 80);
                compCtx.lineTo(leftX, centerY - size - 10);
                compCtx.moveTo(width/2, 80);
                compCtx.lineTo(rightX, centerY - size - 10);
                compCtx.stroke();
                
                compCtx.setLineDash([]);
            }
        }
        
        function animatePropertyCycle() {
            if (compState.showProperty) {
                // 每3秒切换一个性质
                setTimeout(() => {
                    if (compState.showProperty) {
                        compState.currentProperty++;
                        drawComparison();
                        animate
<!--检测到代码截断，自动续写中...-->
PropertyCycle();
                    }
                }, 3000);
            }
        }
        
        // 初始化所有场景
        window.addEventListener('load', () => {
            resizeCanvases();
            drawMacroScene(true);
            drawWhitePhosphorus(true);
            drawRedPhosphorus(true);
            drawTransformation(true);
            drawComparison(true);
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

# 白磷与红磷微观结构交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过直观、动态的可视化方式，帮助您深入理解白磷与红磷在微观结构上的根本差异，以及这些差异如何决定它们截然不同的宏观性质。无论您是教师、学生还是化学爱好者，本动画都将为您提供一次沉浸式的学习体验。

---

## 一、功能说明

本动画是一个基于HTML5 Canvas技术的单页Web应用，无需安装任何插件或软件，在主流浏览器中均可流畅运行。它通过五个精心设计的场景，系统性地展示了从宏观现象到微观结构，再到性质对比的完整知识链条。

## 二、主要功能

### 1. 场景导航
- **宏观现象对比**：直观展示白磷自燃与红磷稳定的宏观现象差异。
- **白磷微观结构**：深入探索P₄正四面体分子的三维结构、键角张力及其与自燃性的关系。
- **红磷微观结构**：展示红磷链状/网状巨型分子的稳定结构。
- **相互转化过程**：动态演示在隔绝空气加热条件下，白磷与红磷的聚合与解聚过程。
- **性质对比总结**：系统对比二者在结构、键角、分子间作用力、着火点、毒性等维度的差异。

### 2. 核心交互操作
- **模型操控**：在微观结构场景中，可点击“旋转”按钮让分子模型自动旋转，从各个角度观察。
- **过程触发**：点击“展示键角张力”、“模拟自燃”、“聚合/解聚”等按钮，触发关键化学过程的动画演示。
- **动画控制**：提供播放/暂停/重置功能，让您可以按自己的节奏学习。
- **焦点高亮**：使用“高亮结构差异”、“高亮化学键”等功能，将视觉焦点引导至核心知识点。

### 3. 视觉与信息同步
- 每个动画场景的左侧为可视化区域，右侧为同步的知识点解析文字。
- 关键步骤配有文字标注和动态指示箭头。
- 采用一致的配色方案（磷原子：橙色；化学键：灰色；氧原子：红色；高亮：青色），降低认知负荷。

## 三、设计特色

1. **符合认知规律**：遵循“宏观现象 → 微观解释 → 过程机制 → 总结归纳”的科学探究路径。
2. **结构-性质强关联**：始终强调并可视化“分子结构 → 化学键特性 → 宏观性质”这一化学核心思想。
3. **降低抽象难度**：将抽象的P₄四面体、角张力、聚合过程等概念转化为可操作、可观察的动态模型。
4. **专业与美观并重**：在保证科学准确性的前提下，采用深色科技感背景与高对比度色彩，营造专注的实验室氛围。
5. **响应式设计**：适配不同尺寸的屏幕，在电脑、平板等设备上均可获得良好体验。

## 四、教学要点（供教师参考）

本动画完美覆盖了以下核心教学要点，建议引导学生依次探索：

1. **引发认知冲突**：从“宏观现象对比”入手，提出“为何组成相同，性质却天差地别？”的核心问题。
2. **突破结构难点**：在“白磷微观结构”场景中，重点讲解 **60°键角** 与 **角张力** 的概念，这是理解其高反应活性的关键。
3. **建立对比模型**：在“红磷微观结构”场景中，对比其 **~100°键角** 和 **巨型共价结构**，解释稳定性来源。
4. **揭示转化本质**：通过“相互转化过程”，阐明 **聚合** 与 **解聚** 是二者转化的微观本质，并强调 **隔绝空气** 的条件。
5. **升华核心观念**：在“性质对比总结”中，引导学生利用动画中的对比表格，自主归纳“**结构决定性质**”的普遍规律。

## 五、使用建议

### 对于学生（自主学习）
- **建议路径**：按照顶部导航按钮的顺序，逐个场景进行探索。在每个场景中，先观察动画，再阅读右侧文字，最后动手操作所有按钮。
- **深度学习**：在微观结构场景，务必使用“旋转”功能从不同角度观察分子。尝试先根据结构预测性质，再与动画展示的性质进行验证。
- **思考与延伸**：动画结束后，可尝试回答：白磷的毒性与其分子结构有何关联？红磷的哪些用途得益于其稳定性？

### 对于教师（课堂教学）
- **课前引入**：播放“宏观现象对比”中的自燃动画，快速吸引学生注意力，引出探究问题。
- **课中探究**：
    - **分组任务**：将学生分为“白磷组”和“红磷组”，分别探索对应场景，然后向全班汇报其结构的特征与优缺点。
    - **互动讲解**：在教师端全屏播放动画，使用“暂停”功能在关键帧进行提问和讲解。
    - **模拟实验**：利用“模拟自燃”动画替代危险的真实实验演示，既安全又直观。
- **课后巩固**：要求学生利用“性质对比总结”场景，制作一个属于自己的对比图或思维导图。

### 技术提示
- 推荐使用 **Chrome、Edge 或 Firefox** 等现代浏览器以获得最佳体验。
- 如果动画显示不完整，请尝试刷新页面或按 **F5** 键。
- 所有交互功能均通过按钮触发，请确保点击了正确的按钮。

---

**祝您探索愉快！希望通过这次微观世界的旅程，您能真正感受到化学结构之美与“结构决定性质”这一规律的深刻力量。**