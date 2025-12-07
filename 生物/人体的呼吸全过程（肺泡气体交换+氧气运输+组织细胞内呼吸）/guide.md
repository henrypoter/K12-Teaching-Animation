# 需求：人体的呼吸全过程（肺泡气体交换+氧气运输+组织细胞内呼吸）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要为中学生或生物学初学者。他们需要：
1.  **理解一个动态、连续的过程**：呼吸不是单一动作，而是涉及多个系统和环节的复杂生理过程。用户需要看到气体如何从外界进入，最终被细胞利用的全貌。
2.  **建立空间与层级概念**：需要清晰地理解从宏观的“呼吸系统”（鼻、气管、肺）到微观的“肺泡”、“毛细血管网”，再到细胞内部的“线粒体”之间的空间关系和层级递进。
3.  **区分两个关键的气体交换环节**：肺泡处的气体交换（外部呼吸）与组织细胞处的气体交换（内部呼吸），并理解其原理（分压差/浓度差）和方向性。
4.  **可视化抽象的运输过程**：理解氧气和二氧化碳在血液中是如何被运输的（氧合血红蛋白、碳酸氢盐等形式）。
5.  **克服认知难点**：例如，理解气体交换的动力是扩散作用而非主动运输；区分呼吸运动（通气）与细胞呼吸（产能）；理解血红蛋白的可逆结合特性。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念**：
    *   **主线流程**：外界空气 → 呼吸道 → 肺泡 → 肺泡毛细血管（氧气进入血液/二氧化碳离开血液）→ 血液循环运输 → 组织毛细血管（氧气离开血液/二氧化碳进入血液） → 组织细胞 → 线粒体（细胞呼吸）。
    *   **关键原理**：气体扩散（顺浓度梯度）、血红蛋白的可逆氧合、细胞有氧呼吸（葡萄糖+氧气→二氧化碳+水+能量）。

*   **认知规律**：
    *   **从宏观到微观，层层递进**：动画将采用“镜头缩放”的叙事方式。从整体人体轮廓开始，聚焦胸部，放大进入肺部，再放大到肺泡-毛细血管网单元，最后进入红细胞和细胞内部。这符合人类认识复杂系统的自然顺序。
    *   **分模块讲解，再整合**：将全过程分解为三个清晰模块：
        1.  **肺泡气体交换**（肺呼吸）：重点展示肺泡和毛细血管壁的结构（单层上皮），以及O₂和CO₂的交换方向。
        2.  **氧气运输**：重点展示红细胞中的血红蛋白如何结合氧气形成氧合血红蛋白，并随血液循环流动。
        3.  **组织细胞内呼吸**：重点展示氧气在组织毛细血管释放，进入细胞，最终在线粒体中被利用，同时产生CO₂。
    *   **强调对比与联系**：并排展示肺泡交换和组织交换，突出气体方向相反但原理相同（扩散）。用相同的颜色和符号（如O₂分子、CO₂分子）贯穿始终，保持一致性。

*   **交互设计**：
    *   **进度条控制**：允许用户播放、暂停、快进、快退整个动画流程，自主控制学习节奏。
    *   **模块选择器**：提供三个按钮（“肺泡交换”、“氧气运输”、“细胞呼吸”），用户可以点击直接跳转到特定模块进行深入学习。
    *   **“探索模式”**：在关键结构（如肺泡、红细胞、线粒体）上设置热点，鼠标悬停或点击时，弹出简要说明框并高亮该结构。
    *   **原理开关**：提供“显示浓度梯度”的复选框。勾选后，在气体交换场景用颜色深浅（如红色由深到浅代表氧浓度由高到低）直观展示扩散的动力来源。
    *   **分步提示**：在动画关键步骤出现文字标签和箭头指示，引导用户注意力。

*   **视觉呈现**：
    *   **风格**：采用简洁、扁平化或轻度拟物化的卡通风格，避免过于复杂的细节干扰对过程的理解。线条清晰，色块明确。
    *   **动态效果**：
        *   气体分子（O₂、CO₂）以粒子流或小圆点形式运动。
        *   红细胞在血管中流动，结合氧气时颜色变化（暗红→鲜红）。
        *   毛细血管网和肺泡囊有轻微的舒张收缩，体现生命感。
        *   线粒体内有简单的“能量”（如小星星或光点）产生动画。
    *   **视觉隐喻**：将血红蛋白比喻为“运输车”，将线粒体比喻为“发电厂”，帮助初学者建立直观印象。

#### 配色方案选择
*   **主色调**：采用柔和、专业的蓝色系，象征氧气、呼吸和科学感。
*   **关键元素配色**：
    *   **氧气（O₂）**：使用**鲜亮、有活力的红色**（传统上代表动脉血和富氧）。这是整个动画的视觉焦点。
    *   **二氧化碳（CO₂）**：使用**暗蓝色或灰紫色**，与氧气形成鲜明对比，代表代谢废物。
    *   **血液**：
        *   缺氧血（静脉血）：**暗红色**。
        *   富氧血（动脉血）：**鲜红色**。
    *   **生物结构**：
        *   呼吸道、肺泡囊：**浅粉色或淡灰色**，体现组织质感。
        *   毛细血管：**非常细的红色/暗红色线条网**。
        *   细胞和线粒体：**浅黄色或米色**，温暖且有生机感。
    *   **背景**：**浅灰色或极淡的蓝灰色**，确保前景所有元素突出。
    *   **交互元素（按钮、标签）**：使用与主色调协调的**中性色（如深蓝、白色）**，清晰可辨。

#### 交互功能列表
1.  **主控面板**：播放/暂停、进度条、重置按钮。
2.  **章节跳转**：三个主要模块的快速导航按钮。
3.  **知识提示点**：鼠标悬停在关键结构（肺泡壁、红细胞、血红蛋白、线粒体）上时显示名称和功能简介。
4.  **可视化开关**：“显示浓度梯度”复选框，用颜色渐变覆盖层展示气体分压差。
5.  **动画速度调节**：简易的慢速/常速/快速切换选项。
6.  **过程标签**：动画播放时，关键步骤自动出现非侵入性的文字说明（如“氧气扩散进入血液”、“血红蛋白结合氧”）。
7.  **呼吸节律提示**：可选的、轻微的背景膨胀收缩动画，提示呼吸动作与气体交换的同步关系。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>人体的呼吸全过程 - 交互式教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #4a90e2;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .animation-container {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            overflow: hidden;
            position: relative;
        }
        
        #animationCanvas {
            display: block;
            width: 100%;
            height: 500px;
            background-color: #f0f4f8;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            padding: 20px;
            background-color: #f9fbfd;
            border-top: 1px solid #e1e8ed;
        }
        
        .control-group {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        button {
            padding: 10px 18px;
            background-color: #4a90e2;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        button:hover {
            background-color: #3a7bc8;
            transform: translateY(-2px);
        }
        
        button.active {
            background-color: #2c3e50;
            box-shadow: 0 3px 8px rgba(44, 62, 80, 0.2);
        }
        
        .module-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        .module-btn {
            background-color: #5d9cec;
        }
        
        .module-btn.active {
            background-color: #2c3e50;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
            flex-grow: 1;
        }
        
        input[type="range"] {
            flex-grow: 1;
            height: 8px;
            border-radius: 4px;
            background: #dfe6e9;
            outline: none;
            -webkit-appearance: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #4a90e2;
            cursor: pointer;
        }
        
        .checkbox-container {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-left: auto;
        }
        
        .info-panel {
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .info-panel h3 {
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #ecf0f1;
        }
        
        .info-content {
            display: none;
        }
        
        .info-content.active {
            display: block;
        }
        
        .info-content p {
            margin-bottom: 15px;
            color: #555;
        }
        
        .key-points {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .point {
            background-color: #f8fafc;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #4a90e2;
        }
        
        .point h4 {
            color: #2c3e50;
            margin-bottom: 8px;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #ecf0f1;
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
        
        .tooltip {
            position: absolute;
            background-color: rgba(44, 62, 80, 0.95);
            color: white;
            padding: 10px 15px;
            border-radius: 6px;
            font-size: 0.9rem;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.2s;
            z-index: 100;
            max-width: 250px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #e1e8ed;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .controls {
                flex-direction: column;
            }
            
            .checkbox-container {
                margin-left: 0;
            }
            
            .key-points {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>人体的呼吸全过程</h1>
        <p class="subtitle">肺泡气体交换 + 氧气运输 + 组织细胞内呼吸 - 交互式教学动画</p>
    </header>
    
    <div class="container">
        <div class="animation-container">
            <canvas id="animationCanvas"></canvas>
            <div class="tooltip" id="tooltip"></div>
        </div>
        
        <div class="controls">
            <div class="control-group">
                <button id="playPauseBtn">▶ 播放</button>
                <button id="resetBtn">↺ 重置</button>
            </div>
            
            <div class="slider-container">
                <span>进度:</span>
                <input type="range" id="progressSlider" min="0" max="100" value="0">
                <span id="progressLabel">0%</span>
            </div>
            
            <div class="control-group">
                <span>速度:</span>
                <button id="speedSlow">慢速</button>
                <button id="speedNormal" class="active">常速</button>
                <button id="speedFast">快速</button>
            </div>
            
            <div class="module-buttons">
                <button class="module-btn" data-module="alveolar">肺泡交换</button>
                <button class="module-btn" data-module="transport">氧气运输</button>
                <button class="module-btn" data-module="cellular">细胞呼吸</button>
            </div>
            
            <div class="checkbox-container">
                <input type="checkbox" id="showGradient" checked>
                <label for="showGradient">显示浓度梯度</label>
            </div>
        </div>
        
        <div class="info-panel">
            <h3 id="infoTitle">呼吸过程概述</h3>
            <div class="info-content active" id="overviewInfo">
                <p>人体的呼吸全过程包括三个主要环节：</p>
                <ol>
                    <li><strong>肺泡气体交换（外部呼吸）</strong>：氧气从肺泡扩散进入肺毛细血管血液，二氧化碳从血液扩散进入肺泡。</li>
                    <li><strong>氧气运输</strong>：氧气与红细胞中的血红蛋白结合，通过血液循环运输到全身各组织。</li>
                    <li><strong>组织细胞内呼吸（内部呼吸）</strong>：氧气从组织毛细血管扩散进入细胞，在线粒体中参与有氧呼吸，产生能量。</li>
                </ol>
                <p>点击上方模块按钮或使用进度条探索每个环节的详细过程。</p>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff6b6b;"></div>
                        <span>氧气 (O₂)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #5d6de2;"></div>
                        <span>二氧化碳 (CO₂)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff3838;"></div>
                        <span>富氧血 (动脉血)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #8b0000;"></div>
                        <span>缺氧血 (静脉血)</span>
                    </div>
                </div>
            </div>
            
            <div class="info-content" id="alveolarInfo">
                <p><strong>肺泡气体交换</strong>发生在肺泡和肺毛细血管之间。</p>
                <p>肺泡壁和毛细血管壁都非常薄（仅一层上皮细胞），这有利于气体通过扩散作用进行交换。</p>
                <p>由于肺泡内氧气浓度高，二氧化碳浓度低，而毛细血管血液中氧气浓度低，二氧化碳浓度高，因此：</p>
                <ul>
                    <li>氧气从肺泡扩散进入血液</li>
                    <li>二氧化碳从血液扩散进入肺泡</li>
                </ul>
                
                <div class="key-points">
                    <div class="point">
                        <h4>扩散作用</h4>
                        <p>气体分子从高浓度区域向低浓度区域移动的过程，不需要能量。</p>
                    </div>
                    <div class="point">
                        <h4>肺泡结构</h4>
                        <p>人体约有3-4亿个肺泡，总表面积约70-100平方米，为气体交换提供了巨大面积。</p>
                    </div>
                </div>
            </div>
            
            <div class="info-content" id="transportInfo">
                <p><strong>氧气运输</strong>主要通过红细胞中的血红蛋白完成。</p>
                <p>血红蛋白由四个亚基组成，每个亚基含有一个血红素分子，可以结合一个氧分子。</p>
                <p>在肺部，氧气分压高，血红蛋白与氧气结合形成氧合血红蛋白；在组织，氧气分压低，氧合血红蛋白解离释放氧气。</p>
                
                <div class="key-points">
                    <div class="point">
                        <h4>血红蛋白</h4>
                        <p>每个血红蛋白分子最多可结合4个氧分子，使血液的携氧能力提高约70倍。</p>
                    </div>
                    <div class="point">
                        <h4>血液循环</h4>
                        <p>富氧血从左心室泵出，通过动脉系统输送到全身各组织。</p>
                    </div>
                </div>
            </div>
            
            <div class="info-content" id="cellularInfo">
                <p><strong>组织细胞内呼吸</strong>是氧气被细胞利用产生能量的过程。</p>
                <p>在组织毛细血管中，氧气从血液扩散进入组织细胞，最终到达线粒体。</p>
                <p>在线粒体中，氧气参与有氧呼吸的电子传递链，帮助产生大量ATP（细胞能量货币）。</p>
                <p>同时，细胞代谢产生的二氧化碳扩散进入血液，被运输到肺部排出。</p>
                
                <div class="key-points">
                    <div class="point">
                        <h4>线粒体</h4>
                        <p>细胞的"动力工厂"，通过有氧呼吸将葡萄糖和氧气转化为ATP、二氧化碳和水。</p>
                    </div>
                    <div class="point">
                        <h4>ATP产生</h4>
                        <p>1分子葡萄糖通过有氧呼吸可产生约36-38分子ATP，远高于无氧呼吸的2分子。</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>交互式教学动画 | 人体的呼吸全过程 | 设计：熊猫老师</p>
    </footer>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        const tooltip = document.getElementById('tooltip');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
        }
        
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();
        
        // 动画状态
        const state = {
            isPlaying: false,
            progress: 0, // 0-100
            speed: 1, // 1=正常, 0.5=慢速, 2=快速
            currentModule: 'overview', // overview, alveolar, transport, cellular
            showGradient: true,
            lastTime: 0,
            animationFrameId: null
        };
        
        // 颜色定义
        const colors = {
            oxygen: '#ff6b6b',      // 氧气 - 鲜红色
            co2: '#5d6de2',         // 二氧化碳 - 蓝色
            oxygenatedBlood: '#ff3838', // 富氧血 - 亮红色
            deoxygenatedBlood: '#8b0000', // 缺氧血 - 暗红色
            alveoli: '#ffd8d8',     // 肺泡 - 浅粉色
            capillary: '#ff9999',   // 毛细血管 - 粉色
            cell: '#fff9c4',        // 细胞 - 浅黄色
            mitochondria: '#ffcc80', // 线粒体 - 橙色
            text: '#2c3e50',        // 文字颜色
            background: '#f0f4f8',  // 背景色
            gradientHigh: 'rgba(255, 107, 107, 0.3)',   // 高浓度氧气
            gradientLow: 'rgba(255, 107, 107, 0.05)',   // 低浓度氧气
            gradientHighCO2: 'rgba(93, 109, 226, 0.3)', // 高浓度二氧化碳
            gradientLowCO2: 'rgba(93, 109, 226, 0.05)'  // 低浓度二氧化碳
        };
        
        // 动画元素定义
        const elements = {
            // 肺泡交换模块
            alveoli: {
                x: canvas.width * 0.3,
                y: canvas.height * 0.5,
                radius: 80,
                oxygenCount: 30,
                co2Count: 10
            },
            capillary: {
                x: canvas.width * 0.7,
                y: canvas.height * 0.5,
                width: 120,
                height: 60,
                bloodCells: []
            },
            // 运输模块
            artery: {
                x: canvas.width * 0.2,
                y: canvas.height * 0.3,
                width: canvas.width * 0.6,
                height: 40,
                bloodCells: []
            },
            // 细胞呼吸模块
            tissueCell: {
                x: canvas.width * 0.3,
                y: canvas.height * 0.6,
                radius: 70,
                mitochondria: []
            },
            tissueCapillary: {
                x: canvas.width * 0.7,
                y: canvas.height * 0.6,
                width: 100,
                height: 50,
                bloodCells: []
            }
        };
        
        // 初始化动画元素
        function initElements() {
            // 初始化肺泡氧气和二氧化碳分子
            elements.alveoli.oxygenMolecules = [];
            elements.alveoli.co2Molecules = [];
            
            for (let i = 0; i < elements.alveoli.oxygenCount; i++) {
                elements.alveoli.oxygenMolecules.push({
                    x: elements.alveoli.x + (Math.random() - 0.5) * elements.alveoli.radius * 1.5,
                    y: elements.alveoli.y + (Math.random() - 0.5) * elements.alveoli.radius * 1.5,
                    vx: (Math.random() - 0.5) * 0.5,
                    vy: (Math.random() - 0.5) * 0.5,
                    radius: 4
                });
            }
            
            for (let i = 0; i < elements.alveoli.co2Count; i++) {
                elements.alveoli.co2Molecules.push({
                    x: elements.capillary.x + (Math.random() - 0.5) * elements.capillary.width * 0.8,
                    y: elements.capillary.y + (Math.random() - 0.5) * elements.capillary.height * 0.8,
                    vx: (Math.random() - 0.5) * 0.3,
                    vy: (Math.random() - 0.5) * 0.3,
                    radius: 5
                });
            }
            
            // 初始化毛细血管血细胞
            elements.capillary.bloodCells = [];
            for (let i = 0; i < 8; i++) {
                elements.capillary.bloodCells.push({
                    x: elements.capillary.x - elements.capillary.width/2 + i * 15,
                    y: elements.capillary.y + (Math.random() - 0.5) * 10,
                    radius: 8,
                    oxygenated: i < 4, // 前4个是富氧的
                    oxygenMolecules: i < 4 ? 4 : 0 // 富氧血细胞有4个氧分子
                });
            }
            
            // 初始化动脉血细胞
            elements.artery.bloodCells = [];
            for (let i = 0; i < 12; i++) {
                elements.artery.bloodCells.push({
                    x: elements.artery.x + i * 25,
                    y: elements.artery.y + (Math.random() - 0.5) * 10,
                    radius: 10,
                    oxygenated: true,
                    oxygenMolecules: 4
                });
            }
            
            // 初始化组织毛细血管血细胞
            elements.tissueCapillary.bloodCells = [];
            for (let i = 0; i < 6; i++) {
                elements.tissueCapillary.bloodCells.push({
                    x: elements.tissueCapillary.x - elements.tissueCapillary.width/2 + i * 15,
                    y: elements.tissueCapillary.y + (Math.random() - 0.5) * 10,
                    radius: 8,
                    oxygenated: i > 2, // 后3个是富氧的
                    oxygenMolecules: i > 2 ? 4 : 0
                });
            }
            
            // 初始化线粒体
            elements.tissueCell.mitochondria = [];
            for (let i = 0; i < 5; i++) {
                const angle = (i / 5) * Math.PI * 2;
                elements.tissueCell.mitochondria.push({
                    x: elements.tissueCell.x + Math.cos(angle) * elements.tissueCell.radius * 0.6,
                    y: elements.tissueCell.y + Math.sin(angle) * elements.tissueCell.radius * 0.6,
                    radius: 12,
                    energyLevel: Math.random()
                });
            }
        }
        
        // 绘制肺泡交换模块
        function drawAlveolarModule() {
            const { alveoli, capillary } = elements;
            
            // 绘制肺泡
            ctx.beginPath();
            ctx.arc(alveoli.x, alveoli.y, alveoli.radius, 0, Math.PI * 2);
            ctx.fillStyle = colors.alveoli;
            ctx.fill();
            ctx.strokeStyle = '#ff9999';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制肺泡标签
            ctx.fillStyle = colors.text;
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('肺泡', alveoli.x, alveoli.y - alveoli.radius - 10);
            
            // 绘制氧气分子（肺泡内）
            alveoli.oxygenMolecules.forEach(molecule => {
                ctx.beginPath();
                ctx.arc(molecule.x, molecule.y, molecule.radius, 0, Math.PI * 2);
                ctx.fillStyle = colors.oxygen;
                ctx.fill();
                
                // 氧气分子标签
                ctx.fillStyle = colors.oxygen;
                ctx.font = '10px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('O₂', molecule.x, molecule.y + 1);
            });
            
            // 绘制毛细血管
            ctx.beginPath();
            ctx.roundRect(
                capillary.x - capillary.width/2, 
                capillary.y - capillary.height/2, 
                capillary.width, 
                capillary.height, 
                10
            );
            ctx.fillStyle = colors.capillary;
            ctx.fill();
            ctx.strokeStyle = '#ff6666';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制毛细血管标签
            ctx.fillStyle = colors.text;
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('肺毛细血管', capillary.x, capillary.y - capillary.height/2 - 15);
            
            // 绘制血细胞
            capillary.bloodCells.forEach(cell => {
                ctx.beginPath();
                ctx.arc(cell.x, cell.y, cell.radius, 0, Math.PI * 2);
                ctx.fillStyle = cell.oxygenated ? colors.oxygenatedBlood : colors.deoxygenatedBlood;
                ctx.fill();
                
                // 绘制血细胞中的氧分子
                if (cell.oxygenMolecules > 0) {
                    for (let i = 0; i < cell.oxygenMolecules; i++) {
                        const angle = (i / cell.oxygenMolecules) * Math.PI * 2;
                        const ox = cell.x + Math.cos(angle) * cell.radius * 0.6;
                        const oy = cell.y + Math.sin(angle) * cell.radius * 0.6;
                        
                        ctx.beginPath();
                        ctx.arc(ox, oy, 3, 0, Math.PI * 2);
                        ctx.fillStyle = colors.oxygen;
                        ctx.fill();
                    }
                }
            });
            
            // 绘制二氧化碳分子（毛细血管内）
            alveoli.co2Molecules.forEach(molecule => {
                ctx.beginPath();
                ctx.arc(molecule.x, molecule.y, molecule.radius, 0, Math.PI * 2);
                ctx.fillStyle = colors.co2;
                ctx.fill();
                
                // 二氧化碳分子标签
                ctx.fillStyle = colors.co2;
                ctx.font = '10px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('CO₂', molecule.x, molecule.y + 1);
            });
            
            // 绘制气体交换箭头
            if (state.progress > 15 && state.progress < 40) {
                // 氧气从肺泡到毛细血管
                drawArrow(
                    alveoli.x + alveoli.radius * 0.7, 
                    alveoli.y, 
                    capillary.x - capillary.width/2, 
                    capillary.y, 
                    colors.oxygen, 
                    'O₂'
                );
                
                // 二氧化碳从毛细血管到肺泡
                drawArrow(
                    capillary.x - capillary.width/2 + 20, 
                    capillary.y, 
                    alveoli.x + alveoli.radius * 0.5, 
                    alveoli.y, 
                    colors.co2, 
                    'CO₂'
                );
            }
            
            // 显示浓度梯度
            if (state.showGradient) {
                // 肺泡氧气梯度
                const alveolarGradient = ctx.createRadialGradient(
                    alveoli.x, alveoli.y, 0,
                    alveoli.x, alveoli.y, alveoli.radius * 1.5
                );
                alveolarGradient.addColorStop(0, colors.gradientHigh);
                alveolarGradient.addColorStop(1, colors.gradientLow);
                
                ctx.beginPath();
                ctx.arc(alveoli.x, alveoli.y, alveoli.radius * 1.5, 0, Math.PI * 2);
                ctx.fillStyle = alveolarGradient;
                ctx.fill();
                
                // 毛细血管二氧化碳梯度
                const capillaryGradient = ctx.createLinearGradient(
                    capillary.x - capillary.width/2, 
                    capillary.y,
                    capillary.x + capillary.width/2, 
                    capillary.y
                );
                capillaryGradient.addColorStop(0, colors.gradientHighCO2);
                capillaryGradient.addColorStop(1, colors.gradientLowCO2);
                
                ctx.beginPath();
                ctx.roundRect(
                    capillary.x - capillary.width/2, 
                    capillary.y - capillary.height/2, 
                    capillary.width, 
                    capillary.height, 
                    10
                );
                ctx.fillStyle = capillaryGradient;
                ctx.fill();
            }
            
            // 模块标题
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('肺泡气体交换（外部呼吸）', canvas.width/2, 40);
            
            // 说明文字
            ctx.font = '14px Arial';
            ctx.fillText('氧气从肺泡扩散进入血液，二氧化碳从血液扩散进入肺泡', canvas.width/2, 70);
        }
        
        // 绘制氧气运输模块
        function drawTransportModule() {
            const { artery } = elements;
            
            // 绘制动脉
            ctx.beginPath();
            ctx.roundRect(
                artery.x, 
                artery.y - artery.height/2, 
                artery.width, 
                artery.height, 
                20
            );
            ctx.fillStyle = colors.oxygenatedBlood;
            ctx.fill();
            ctx.strokeStyle = '#ff1a1a';
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制动脉标签
            ctx.fillStyle = colors.text;
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('动脉（富氧血）', artery.x + artery.width/2, artery.y - artery.height/2 - 15);
            
            // 绘制血细胞
            artery.bloodCells.forEach(cell => {
                ctx.beginPath();
                ctx.arc(cell.x, cell.y, cell.radius, 0, Math.PI * 2);
                ctx.fillStyle = colors.oxygenatedBlood;
                ctx.fill();
                
                // 绘制血红蛋白分子（简化表示）
                ctx.beginPath();
                ctx.arc(cell.x, cell.y, cell.radius * 0.7, 0, Math.PI * 2);
                ctx.strokeStyle = '#ff6b6b';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 绘制氧分子
                for (let i = 0; i < cell.oxygenMolecules; i++) {
                    const angle = (i / cell.oxygenMolecules) * Math.PI * 2 + Date.now() / 1000;
                    const ox = cell.x + Math.cos(angle) * cell.radius * 0.8;
                    const oy = cell.y + Math.sin(angle) * cell.radius * 0.8;
                    
                    ctx.beginPath();
                    ctx.arc(ox, oy, 4, 0, Math.PI * 2);
                    ctx.fillStyle = colors.oxygen;
                    ctx.fill();
                    
                    ctx.fillStyle = colors.oxygen;
                    ctx.font = '9px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('O₂', ox, oy + 1);
                }
            });
            
            // 绘制心脏简图
            const heartX = canvas.width * 0.1;
            const heartY = canvas.height * 0.3;
            
            ctx.beginPath();
            ctx.moveTo(heartX, heartY - 15);
            ctx.bezierCurveTo(heartX - 20, heartY - 30, heartX - 20, heartY + 20, heartX, heartY + 15);
            ctx.bezierCurveTo(heartX + 20, heartY + 20, heartX + 20, heartY - 30, heartX, heartY - 15);
            ctx.fillStyle = '#ff6b6b';
            ctx.fill();
            
            ctx.fillStyle = colors.text;
            ctx.font = '14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('心脏', heartX, heartY + 40);
            
            // 绘制运输箭头
            if (state.progress > 45 && state.progress < 70) {
                drawArrow(
                    artery.x + 50, 
                    artery.y, 
                    artery.x + artery.width - 50, 
                    artery.y, 
                    colors.oxygenatedBlood, 
                    '氧气运输'
                );
            }
            
            // 模块标题
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('氧气运输', canvas.width/2, 40);
            
            // 说明文字
            ctx.font = '14px Arial';
            ctx.fillText('氧气与血红蛋白结合，通过血液循环运输到全身组织', canvas.width/2, 70);
        }
        
        // 绘制细胞呼吸模块
        function drawCellularModule() {
            const { tissueCell, tissueCapillary } = elements;
            
            // 绘制组织细胞
            ctx.beginPath();
            ctx.arc(tissueCell.x, tissueCell.y, tissueCell.radius, 0, Math.PI * 2);
            ctx.fillStyle = colors.cell;
            ctx.fill();
            ctx.strokeStyle = '#e6c200';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制细胞标签
            ctx.fillStyle = colors.text;
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('组织细胞', tissueCell.x, tissueCell.y - tissueCell.radius - 10);
            
            // 绘制线粒体
            tissueCell.mitochondria.forEach(mito => {
                ctx.beginPath();
                ctx.arc(mito.x, mito.y, mito.radius, 0, Math.PI * 2);
                ctx.fillStyle = colors.mitochondria;
                ctx.fill();
                
                // 线粒体内膜（简化表示）
                ctx.beginPath();
                ctx.arc(mito.x, mito.y, mito.radius * 0.6, 0, Math.PI * 2);
                ctx.strokeStyle = '#e65100';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 能量产生动画
                if (state.progress > 75) {
                    for (let i = 0; i < 3; i++) {
                        const angle = Math.PI * 2 * Math.random();
                        const distance = mito.radius * 0.8;
                        const ex = mito.x + Math.cos(angle) * distance;
                        const ey = mito.y + Math.sin(angle) * distance;
                        
                        ctx.beginPath();
                        ctx.arc(ex, ey, 3, 0, Math.PI * 2);
                        ctx.fillStyle = `rgba(255, 204, 0, ${0.5 + 0.5 * Math.sin(Date.now()/200 + i)})`;
                        ctx.fill();
                    }
                }
            });
            
            // 绘制组织毛细血管
            ctx.beginPath();
            ctx.roundRect(
                tissueCapillary.x - tissueCapillary.width/2, 
                tissueCapillary.y - tissueCapillary.height/2, 
                tissueCapillary.width, 
                tissueCapillary.height, 
                8
            );
            ctx.fillStyle = colors.deoxygenatedBlood;
            ctx.fill();
            ctx.strokeStyle = '#990000';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制毛细血管标签
            ctx.fillStyle = colors.text;
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('组织毛细血管', tissueCapillary.x, tissueCapillary.y - tissueCapillary.height/2 - 15);
            
            // 绘制血细胞
            tissueCapillary.bloodCells.forEach(cell => {
                ctx.beginPath();
                ctx.arc(cell.x, cell.y, cell.radius, 0, Math.PI * 2);
                ctx.fillStyle = cell.oxygenated ? colors.oxygenatedBlood : colors.deoxygenatedBlood;
                ctx.fill();
                
                // 绘制血细胞中的氧分子
                if (cell.oxygenMolecules > 0) {
                    for (let i = 0; i < cell.oxygenMolecules; i++) {
                        const angle = (i / cell.oxygenMolecules) * Math.PI * 2;
                        const ox = cell.x + Math.cos(angle) * cell.radius * 0.6;
                        const oy = cell.y + Math.sin(angle) * cell.radius * 0.6;
                        
                        ctx.beginPath();
                        ctx.arc(ox, oy, 3, 0, Math.PI * 2);
                        ctx.fillStyle = colors.oxygen;
                        ctx.fill();
                    }
                }
            });
            
            // 绘制气体交换箭头
            if (state.progress > 75 && state.progress < 95) {
                // 氧气从毛细血管到细胞
                drawArrow(
                    tissueCapillary.x - tissueCapillary.width/2 + 20, 
                    tissueCapillary.y, 
                    tissueCell.x + tissueCell.radius * 0.7, 
                    tissueCell.y, 
                    colors.oxygen, 
                    'O₂'
                );
                
                // 二氧化碳从细胞到毛细血管
                drawArrow(
                    tissueCell.x + tissueCell.radius * 0.5, 
                    tissueCell.y, 
                    tissueCapillary.x - tissueCapillary.width/2 + 40, 
                    tissueCapillary.y, 
                    colors.co2, 
                    'CO₂'
                );
            }
            
            // 显示浓度梯度
            if (state.showGradient) {
                // 组织毛细血管氧气梯度
                const capillaryGradient = ctx.createLinearGradient(
                    tissueCapillary.x - tissueCapillary.width/2, 
                    tissueCapillary.y,
                    tissueCapillary.x + tissueCapillary.width/2, 
                    tissueCapillary.y
                );
                capillaryGradient.addColorStop(0, colors.gradientLow);
                capillaryGradient.addColorStop(1, colors.gradientHigh);
                
                ctx.beginPath();
                ctx.roundRect(
                    tissueCapillary.x - tissueCapillary.width/2, 
                    tissueCapillary.y - tissueCapillary.height/2, 
                    tissueCapillary.width, 
                    tissueCapillary.height, 
                    8
                );
                ctx.fillStyle = capillaryGradient;
                ctx.fill();
                
                // 细胞二氧化碳梯度
                const cellGradient = ctx.createRadialGradient(
                    tissueCell.x, tissueCell.y, 0,
                    tissueCell.x, tissueCell.y, tissueCell.radius * 1.2
                );
                cellGradient.addColorStop(0, colors.gradientHighCO2);
                cellGradient
<!--检测到代码截断，自动续写中...-->
.addColorStop(1, colors.gradientLowCO2);
                
                ctx.beginPath();
                ctx.arc(tissueCell.x, tissueCell.y, tissueCell.radius * 1.2, 0, Math.PI * 2);
                ctx.fillStyle = cellGradient;
                ctx.fill();
            }
            
            // 模块标题
            ctx.fillStyle = colors.text;
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('组织细胞内呼吸（内部呼吸）', canvas.width/2, 40);
            
            // 说明文字
            ctx.font = '14px Arial';
            ctx.fillText('氧气进入细胞，在线粒体中产生能量；二氧化碳从细胞进入血液', canvas.width/2, 70);
        }
        
        // 绘制箭头
        function drawArrow(fromX, fromY, toX, toY, color, label) {
            const headlen = 15;
            const angle = Math.atan2(toY - fromY, toX - fromX);
            
            // 绘制箭头线
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.strokeStyle = color;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(
                toX - headlen * Math.cos(angle - Math.PI / 7),
                toY - headlen * Math.sin(angle - Math.PI / 7)
            );
            ctx.lineTo(
                toX - headlen * Math.cos(angle + Math.PI / 7),
                toY - headlen * Math.sin(angle + Math.PI / 7)
            );
            ctx.closePath();
            ctx.fillStyle = color;
            ctx.fill();
            
            // 绘制标签
            if (label) {
                const midX = (fromX + toX) / 2;
                const midY = (fromY + toY) / 2;
                
                ctx.fillStyle = color;
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(label, midX, midY - 10);
            }
        }
        
        // 更新动画元素
        function updateElements(deltaTime) {
            const speedFactor = deltaTime * 0.06 * state.speed;
            
            // 更新肺泡模块
            if (state.currentModule === 'alveolar' || state.currentModule === 'overview') {
                // 更新氧气分子运动
                elements.alveoli.oxygenMolecules.forEach(molecule => {
                    molecule.x += molecule.vx * speedFactor;
                    molecule.y += molecule.vy * speedFactor;
                    
                    // 边界检查
                    const dx = molecule.x - elements.alveoli.x;
                    const dy = molecule.y - elements.alveoli.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance > elements.alveoli.radius * 0.8) {
                        molecule.vx = -molecule.vx * 0.8;
                        molecule.vy = -molecule.vy * 0.8;
                    }
                    
                    // 随机运动
                    molecule.vx += (Math.random() - 0.5) * 0.05;
                    molecule.vy += (Math.random() - 0.5) * 0.05;
                    
                    // 限制速度
                    const speed = Math.sqrt(molecule.vx * molecule.vx + molecule.vy * molecule.vy);
                    if (speed > 2) {
                        molecule.vx = (molecule.vx / speed) * 2;
                        molecule.vy = (molecule.vy / speed) * 2;
                    }
                });
                
                // 更新二氧化碳分子运动
                elements.alveoli.co2Molecules.forEach(molecule => {
                    molecule.x += molecule.vx * speedFactor;
                    molecule.y += molecule.vy * speedFactor;
                    
                    // 边界检查（毛细血管内）
                    if (molecule.x < elements.capillary.x - elements.capillary.width/2 + 10 || 
                        molecule.x > elements.capillary.x + elements.capillary.width/2 - 10 ||
                        molecule.y < elements.capillary.y - elements.capillary.height/2 + 10 || 
                        molecule.y > elements.capillary.y + elements.capillary.height/2 - 10) {
                        molecule.vx = -molecule.vx * 0.8;
                        molecule.vy = -molecule.vy * 0.8;
                    }
                    
                    // 随机运动
                    molecule.vx += (Math.random() - 0.5) * 0.03;
                    molecule.vy += (Math.random() - 0.5) * 0.03;
                });
                
                // 更新毛细血管血细胞
                elements.capillary.bloodCells.forEach(cell => {
                    cell.x += 0.5 * speedFactor;
                    
                    // 循环血细胞位置
                    if (cell.x > elements.capillary.x + elements.capillary.width/2 + 10) {
                        cell.x = elements.capillary.x - elements.capillary.width/2 - 10;
                        
                        // 当血细胞循环时，改变其氧合状态
                        if (state.progress > 20 && state.progress < 35) {
                            cell.oxygenated = true;
                            cell.oxygenMolecules = 4;
                        }
                    }
                });
            }
            
            // 更新运输模块
            if (state.currentModule === 'transport' || state.currentModule === 'overview') {
                // 更新动脉血细胞
                elements.artery.bloodCells.forEach(cell => {
                    cell.x += 1 * speedFactor;
                    
                    // 循环血细胞位置
                    if (cell.x > elements.artery.x + elements.artery.width + 20) {
                        cell.x = elements.artery.x - 20;
                    }
                    
                    // 氧分子动画
                    cell.oxygenMolecules = 4; // 始终保持富氧
                });
            }
            
            // 更新细胞呼吸模块
            if (state.currentModule === 'cellular' || state.currentModule === 'overview') {
                // 更新组织毛细血管血细胞
                elements.tissueCapillary.bloodCells.forEach(cell => {
                    cell.x += 0.4 * speedFactor;
                    
                    // 循环血细胞位置
                    if (cell.x > elements.tissueCapillary.x + elements.tissueCapillary.width/2 + 10) {
                        cell.x = elements.tissueCapillary.x - elements.tissueCapillary.width/2 - 10;
                        
                        // 当血细胞循环时，改变其氧合状态
                        if (state.progress > 80 && state.progress < 90) {
                            cell.oxygenated = false;
                            cell.oxygenMolecules = 0;
                        }
                    }
                });
                
                // 更新线粒体能量水平
                elements.tissueCell.mitochondria.forEach(mito => {
                    mito.energyLevel = 0.5 + 0.5 * Math.sin(Date.now() / 1000 + mito.x);
                });
            }
            
            // 根据进度更新状态
            if (state.isPlaying) {
                state.progress += 0.05 * state.speed;
                
                if (state.progress > 100) {
                    state.progress = 0;
                }
                
                // 更新进度条和标签
                updateProgressDisplay();
                
                // 根据进度自动切换模块
                if (state.progress < 33) {
                    state.currentModule = 'alveolar';
                } else if (state.progress < 66) {
                    state.currentModule = 'transport';
                } else {
                    state.currentModule = 'cellular';
                }
                
                // 更新模块按钮状态
                updateModuleButtons();
            }
        }
        
        // 绘制整个动画
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            ctx.fillStyle = colors.background;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 根据当前模块绘制
            switch(state.currentModule) {
                case 'alveolar':
                    drawAlveolarModule();
                    break;
                case 'transport':
                    drawTransportModule();
                    break;
                case 'cellular':
                    drawCellularModule();
                    break;
                case 'overview':
                    // 绘制所有模块的简化版
                    drawAlveolarModule();
                    drawTransportModule();
                    drawCellularModule();
                    
                    // 绘制连接箭头
                    if (state.progress > 5) {
                        // 从肺泡到动脉
                        drawArrow(
                            canvas.width * 0.5, 
                            canvas.height * 0.3, 
                            canvas.width * 0.2, 
                            canvas.height * 0.3, 
                            colors.oxygenatedBlood, 
                            '富氧血'
                        );
                        
                        // 从动脉到组织
                        drawArrow(
                            canvas.width * 0.5, 
                            canvas.height * 0.4, 
                            canvas.width * 0.5, 
                            canvas.height * 0.55, 
                            colors.oxygenatedBlood, 
                            '血液循环'
                        );
                    }
                    
                    // 绘制总标题
                    ctx.fillStyle = colors.text;
                    ctx.font = 'bold 24px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('人体的呼吸全过程', canvas.width/2, 30);
                    break;
            }
            
            // 绘制进度指示器
            drawProgressIndicator();
        }
        
        // 绘制进度指示器
        function drawProgressIndicator() {
            const indicatorWidth = canvas.width * 0.8;
            const indicatorHeight = 8;
            const indicatorX = canvas.width * 0.1;
            const indicatorY = canvas.height - 30;
            
            // 绘制进度条背景
            ctx.beginPath();
            ctx.roundRect(indicatorX, indicatorY, indicatorWidth, indicatorHeight, 4);
            ctx.fillStyle = '#dfe6e9';
            ctx.fill();
            
            // 绘制进度条填充
            const progressWidth = (state.progress / 100) * indicatorWidth;
            ctx.beginPath();
            ctx.roundRect(indicatorX, indicatorY, progressWidth, indicatorHeight, 4);
            
            // 根据模块设置不同颜色
            let progressColor;
            if (state.progress < 33) {
                progressColor = colors.oxygen; // 肺泡交换 - 氧气色
            } else if (state.progress < 66) {
                progressColor = colors.oxygenatedBlood; // 运输 - 动脉血色
            } else {
                progressColor = colors.mitochondria; // 细胞呼吸 - 线粒体色
            }
            
            ctx.fillStyle = progressColor;
            ctx.fill();
            
            // 绘制模块标记
            const moduleMarkers = [
                { x: indicatorX, label: '肺泡交换' },
                { x: indicatorX + indicatorWidth * 0.33, label: '氧气运输' },
                { x: indicatorX + indicatorWidth * 0.66, label: '细胞呼吸' },
                { x: indicatorX + indicatorWidth, label: '完成' }
            ];
            
            moduleMarkers.forEach(marker => {
                ctx.beginPath();
                ctx.arc(marker.x, indicatorY + indicatorHeight/2, 6, 0, Math.PI * 2);
                ctx.fillStyle = '#2c3e50';
                ctx.fill();
                
                ctx.fillStyle = colors.text;
                ctx.font = '12px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(marker.label, marker.x, indicatorY - 10);
            });
            
            // 绘制当前模块指示器
            const currentX = indicatorX + (state.progress / 100) * indicatorWidth;
            ctx.beginPath();
            ctx.moveTo(currentX, indicatorY - 10);
            ctx.lineTo(currentX - 8, indicatorY - 20);
            ctx.lineTo(currentX + 8, indicatorY - 20);
            ctx.closePath();
            ctx.fillStyle = '#2c3e50';
            ctx.fill();
        }
        
        // 动画循环
        function animate(timestamp) {
            if (!state.lastTime) state.lastTime = timestamp;
            const deltaTime = timestamp - state.lastTime;
            state.lastTime = timestamp;
            
            updateElements(deltaTime);
            draw();
            
            state.animationFrameId = requestAnimationFrame(animate);
        }
        
        // 更新进度显示
        function updateProgressDisplay() {
            document.getElementById('progressSlider').value = state.progress;
            document.getElementById('progressLabel').textContent = Math.round(state.progress) + '%';
        }
        
        // 更新模块按钮状态
        function updateModuleButtons() {
            document.querySelectorAll('.module-btn').forEach(btn => {
                btn.classList.remove('active');
                if (btn.dataset.module === state.currentModule) {
                    btn.classList.add('active');
                }
            });
            
            // 更新信息面板
            document.querySelectorAll('.info-content').forEach(content => {
                content.classList.remove('active');
            });
            
            let infoTitle = '呼吸过程概述';
            let infoContentId = 'overviewInfo';
            
            switch(state.currentModule) {
                case 'alveolar':
                    infoTitle = '肺泡气体交换';
                    infoContentId = 'alveolarInfo';
                    break;
                case 'transport':
                    infoTitle = '氧气运输';
                    infoContentId = 'transportInfo';
                    break;
                case 'cellular':
                    infoTitle = '组织细胞内呼吸';
                    infoContentId = 'cellularInfo';
                    break;
            }
            
            document.getElementById('infoTitle').textContent = infoTitle;
            document.getElementById(infoContentId).classList.add('active');
        }
        
        // 初始化事件监听器
        function initEventListeners() {
            // 播放/暂停按钮
            document.getElementById('playPauseBtn').addEventListener('click', () => {
                state.isPlaying = !state.isPlaying;
                document.getElementById('playPauseBtn').textContent = 
                    state.isPlaying ? '❚❚ 暂停' : '▶ 播放';
                
                if (state.isPlaying && !state.animationFrameId) {
                    state.lastTime = 0;
                    state.animationFrameId = requestAnimationFrame(animate);
                }
            });
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', () => {
                state.progress = 0;
                state.isPlaying = false;
                document.getElementById('playPauseBtn').textContent = '▶ 播放';
                updateProgressDisplay();
                initElements();
            });
            
            // 进度条
            document.getElementById('progressSlider').addEventListener('input', (e) => {
                state.progress = parseFloat(e.target.value);
                updateProgressDisplay();
                
                // 根据进度设置当前模块
                if (state.progress < 33) {
                    state.currentModule = 'alveolar';
                } else if (state.progress < 66) {
                    state.currentModule = 'transport';
                } else {
                    state.currentModule = 'cellular';
                }
                
                updateModuleButtons();
            });
            
            // 速度控制按钮
            document.getElementById('speedSlow').addEventListener('click', () => {
                state.speed = 0.5;
                document.getElementById('speedSlow').classList.add('active');
                document.getElementById('speedNormal').classList.remove('active');
                document.getElementById('speedFast').classList.remove('active');
            });
            
            document.getElementById('speedNormal').addEventListener('click', () => {
                state.speed = 1;
                document.getElementById('speedSlow').classList.remove('active');
                document.getElementById('speedNormal').classList.add('active');
                document.getElementById('speedFast').classList.remove('active');
            });
            
            document.getElementById('speedFast').addEventListener('click', () => {
                state.speed = 2;
                document.getElementById('speedSlow').classList.remove('active');
                document.getElementById('speedNormal').classList.remove('active');
                document.getElementById('speedFast').classList.add('active');
            });
            
            // 模块按钮
            document.querySelectorAll('.module-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    state.currentModule = btn.dataset.module;
                    state.isPlaying = false;
                    document.getElementById('playPauseBtn').textContent = '▶ 播放';
                    
                    // 设置对应进度
                    switch(state.currentModule) {
                        case 'alveolar':
                            state.progress = 10;
                            break;
                        case 'transport':
                            state.progress = 45;
                            break;
                        case 'cellular':
                            state.progress = 75;
                            break;
                    }
                    
                    updateProgressDisplay();
                    updateModuleButtons();
                });
            });
            
            // 浓度梯度开关
            document.getElementById('showGradient').addEventListener('change', (e) => {
                state.showGradient = e.target.checked;
            });
            
            // Canvas点击交互
            canvas.addEventListener('mousemove', (e) => {
                const rect = canvas.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                let tooltipText = '';
                
                // 检查鼠标是否在关键元素上
                if (state.currentModule === 'alveolar' || state.currentModule === 'overview') {
                    // 检查肺泡
                    const dxAlveoli = x - elements.alveoli.x;
                    const dyAlveoli = y - elements.alveoli.y;
                    const distAlveoli = Math.sqrt(dxAlveoli * dxAlveoli + dyAlveoli * dyAlveoli);
                    
                    if (distAlveoli < elements.alveoli.radius) {
                        tooltipText = '肺泡：气体交换的场所，壁薄，表面积大';
                    }
                    
                    // 检查毛细血管
                    if (x > elements.capillary.x - elements.capillary.width/2 && 
                        x < elements.capillary.x + elements.capillary.width/2 &&
                        y > elements.capillary.y - elements.capillary.height/2 && 
                        y < elements.capillary.y + elements.capillary.height/2) {
                        tooltipText = '肺毛细血管：包围肺泡，血液在此进行气体交换';
                    }
                    
                    // 检查血细胞
                    elements.capillary.bloodCells.forEach(cell => {
                        const dx = x - cell.x;
                        const dy = y - cell.y;
                        const dist = Math.sqrt(dx * dx + dy * dy);
                        
                        if (dist < cell.radius) {
                            tooltipText = cell.oxygenated ? 
                                '红细胞（富氧）：含有氧合血红蛋白，颜色鲜红' : 
                                '红细胞（缺氧）：等待结合氧气，颜色暗红';
                        }
                    });
                }
                
                if (state.currentModule === 'transport' || state.currentModule === 'overview') {
                    // 检查动脉血细胞
                    elements.artery.bloodCells.forEach(cell => {
                        const dx = x - cell.x;
                        const dy = y - cell.y;
                        const dist = Math.sqrt(dx * dx + dy * dy);
                        
                        if (dist < cell.radius) {
                            tooltipText = '红细胞：通过血红蛋白运输氧气，每个血红蛋白可结合4个氧分子';
                        }
                    });
                }
                
                if (state.currentModule === 'cellular' || state.currentModule === 'overview') {
                    // 检查线粒体
                    elements.tissueCell.mitochondria.forEach(mito => {
                        const dx = x - mito.x;
                        const dy = y - mito.y;
                        const dist = Math.sqrt(dx * dx + dy * dy);
                        
                        if (dist < mito.radius) {
                            tooltipText = '线粒体：细胞的"动力工厂"，进行有氧呼吸产生ATP';
                        }
                    });
                    
                    // 检查组织细胞
                    const dxCell = x - elements.tissueCell.x;
                    const dyCell = y - elements.tissueCell.y;
                    const distCell = Math.sqrt(dxCell * dxCell + dyCell * dyCell);
                    
                    if (distCell < elements.tissueCell.radius) {
                        tooltipText = '组织细胞：消耗氧气产生能量，释放二氧化碳';
                    }
                }
                
                // 显示或隐藏工具提示
                if (tooltipText) {
                    tooltip.textContent = tooltipText;
                    tooltip.style.left = (e.clientX + 15) + 'px';
                    tooltip.style.top = (e.clientY - 15) + 'px';
                    tooltip.style.opacity = '1';
                } else {
                    tooltip.style.opacity = '0';
                }
            });
            
            canvas.addEventListener('mouseleave', () => {
                tooltip.style.opacity = '0';
            });
        }
        
        // 初始化
        function init() {
            // 添加Canvas圆角矩形方法（如果不存在）
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
            
            initElements();
            initEventListeners();
            updateModuleButtons();
            
            // 开始动画循环
            state.animationFrameId = requestAnimationFrame(animate);
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## 《人体的呼吸全过程》交互式教学动画使用指南

欢迎使用“人体的呼吸全过程”交互式教学动画！本动画由熊猫老师精心设计，旨在通过直观、动态的可视化方式，帮助您深入理解人体呼吸这一复杂而精妙的生理过程。无论您是学生、教师还是生物学爱好者，本工具都将为您提供沉浸式的学习体验。

---

### 一、 功能说明

本动画将人体的呼吸全过程分解为三个核心环节，并允许您以多种方式进行探索：

1.  **肺泡气体交换**：展示氧气和二氧化碳在肺泡与肺毛细血管之间的扩散过程。
2.  **氧气运输**：展示氧气如何与血红蛋白结合，并通过血液循环系统输送到全身。
3.  **组织细胞内呼吸**：展示氧气在组织细胞中被利用产生能量，以及二氧化碳被排出的过程。

您可以选择**连续观看**全过程，也可以**分模块深入研究**每个环节。

---

### 二、 主要功能与操作

#### 1. 动画控制面板
位于画布下方，是您控制学习节奏的核心工具。
*   **播放/暂停**：控制动画的播放与暂停。
*   **重置**：将动画进度归零，所有元素恢复初始状态。
*   **进度条**：拖动滑块可以快速跳转到动画的任何时间点。上方的进度指示器会显示当前所处的阶段（肺泡交换、运输、细胞呼吸）。
*   **速度控制**：提供“慢速”、“常速”、“快速”三档，适应不同的学习需求。建议初次学习时使用“慢速”。

#### 2. 模块快速导航
位于控制面板中部的三个彩色按钮：
*   **肺泡交换**：点击直接跳转至肺泡气体交换环节。
*   **氧气运输**：点击直接跳转至血液循环运输环节。
*   **细胞呼吸**：点击直接跳转至组织细胞利用氧气环节。
*   **提示**：在“总览”模式下，三个模块会同时简化呈现，展示完整的流程衔接。

#### 3. 核心可视化工具
*   **浓度梯度显示**：勾选“显示浓度梯度”复选框，动画中将用颜色渐变直观展示氧气和二氧化碳的浓度差。**这是理解气体扩散原理的关键**！红色渐变代表氧气浓度（深红为高，浅红为低），蓝色渐变代表二氧化碳浓度（深蓝为高，浅蓝为低）。
*   **交互式探索**：将鼠标悬停在动画中的关键结构上（如**肺泡、红细胞、线粒体**），会弹出详细的说明框，解释其结构和功能。

#### 4. 同步知识面板
画布下方的信息面板会**随动画进度或模块切换自动更新**，提供与当前画面相对应的详细文字解释和知识要点，实现“图文声像”同步学习。

---

### 三、 设计特色

1.  **符合认知规律的叙事**：采用“从宏观到微观”的镜头语言，从人体轮廓逐步聚焦到细胞内的线粒体，引导思维层层深入。
2.  **一致的视觉编码**：
    *   **氧气**：始终用鲜红色表示。
    *   **二氧化碳**：始终用蓝色表示。
    *   **富氧血**：鲜红色。
    *   **缺氧血**：暗红色。
    这种一致性避免了概念混淆，让您能轻松追踪气体分子的“旅程”。
3.  **动态原理演示**：不仅展示“发生了什么”，更通过粒子运动、箭头方向和浓度梯度可视化，清晰揭示了“为什么会发生”（扩散作用）。
4.  **隐喻化设计**：将血红蛋白比喻为“运输车”，将线粒体比喻为“发电厂”，帮助初学者建立生动而准确的心智模型。

---

### 四、 教学要点与学习路径建议

#### 最佳学习路径（推荐给初次学习者）：
1.  **第一步：总览**：保持所有模块按钮为非激活状态，点击“播放”，以“常速”观看一遍完整动画，建立整体印象。
2.  **第二步：分步精学**：使用“模块快速导航”按钮，分别进入三个环节。在每个环节内：
    *   开启“显示浓度梯度”，观察扩散的动力来源。
    *   使用“慢速”播放，仔细观察每一个步骤。
    *   将鼠标悬停在各个结构上，阅读提示信息。
    *   结合下方信息面板的详细说明进行学习。
3.  **第三步：对比与整合**：再次播放完整动画，思考并回答：
    *   肺泡交换和组织交换中，氧气和二氧化碳的扩散方向有何不同？为什么？
    *   血液的颜色在流程中如何变化？原因是什么？
    *   呼吸全过程最终的能量归宿在哪里？

#### 核心概念突破点：
*   **气体交换的动力**：重点利用“浓度梯度”可视化工具，理解**扩散作用**（顺浓度梯度，不消耗能量）是气体交换的唯一动力。
*   **运输的关键分子**：在“氧气运输”模块，关注红细胞中的**血红蛋白**，理解其可逆结合氧的特性。
*   **呼吸的终极目的**：在“细胞呼吸”模块，聚焦**线粒体**，理解呼吸全过程是为了细胞进行有氧呼吸、产生生命活动所需的**ATP**。

---

### 五、 使用建议

*   **给学生的建议**：不要被动观看，要主动探索。多使用暂停、悬停查看、切换速度等功能。尝试在观看后，用自己的话复述整个过程。
*   **给教师的建议**：可将此动画用于课堂导入、难点讲解或课后复习。在讲解时，可以操作“浓度梯度”开关，通过对比强调扩散原理。可以让学生分组操作，并围绕“教学要点”中的问题进行讨论。
*   **技术提示**：本动画基于HTML5标准，请在Chrome、Firefox、Edge等现代浏览器的最新版本中使用，以获得最佳体验。

我们希望这个交互式动画能像一位耐心的向导，带领您揭开人体呼吸奥秘的面纱。祝您探索愉快，学有所获！

**设计制作：熊猫老师**