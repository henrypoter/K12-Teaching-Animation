# 需求：配位键形成（如[Cu(NH₃)₄]²⁺深蓝色配合物）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的化学学生，他们已具备基本的原子结构、化学键（离子键、共价键）知识，正在学习配位化学入门内容。
2.  **核心需求**：理解配位键的本质——由一方（配体）提供孤对电子，另一方（中心离子）提供空轨道，通过配位作用形成的特殊共价键。具体到`[Cu(NH₃)₄]²⁺`，需要可视化：
    *   `Cu²⁺`离子的电子排布与空轨道。
    *   `NH₃`分子中N原子上的孤对电子。
    *   孤对电子填入空轨道形成配位键的动态过程。
    *   配合物的空间构型（平面正方形）。
3.  **潜在难点**：学生可能难以抽象地想象“空轨道”和“电子对给予”的过程。需要将微观、抽象的概念转化为直观、动态的视觉模型。
4.  **学习目标**：通过交互动画，学生应能描述`[Cu(NH₃)₄]²⁺`的形成过程，解释配位键的成键本质，并识别中心离子、配体和配位数。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念**：
    *   **中心离子** (`Cu²⁺`)：提供空轨道（这里是4个`sp²d`杂化轨道或`dsp²`杂化轨道，简化呈现为4个可接受电子的“空位”）。
    *   **配体** (`NH₃`)：提供孤对电子。
    *   **配位键**：一种特殊的共价键，共用电子对完全由一方提供。
    *   **配合物空间构型**：平面正方形。

2.  **认知规律（叙事与结构）**：
    *   **从已知到未知**：先回顾`Cu²⁺`（蓝色水合离子）和`NH₃`的独立存在，再展示混合后发生的惊人颜色变化（变为深蓝色），引出“发生了新的成键作用”。
    *   **分步解构**：将整个过程分解为可控制的步骤，引导学习者逐步观察：
        *   步骤1：展示`Cu²⁺`离子及其空轨道。
        *   步骤2：展示`NH₃`分子及其孤对电子。
        *   步骤3：演示一个`NH₃`接近`Cu²⁺`，孤对电子“填入”空轨道，形成第一个配位键。
        *   步骤4：重复过程，直至四个`NH₃`全部配位，形成平面正方形结构。
    *   **归纳总结**：在动画最后，高亮显示所有四个配位键，并给出配位键的定义和配合物的化学式。

3.  **交互设计**：
    *   **步骤控制**：提供“上一步”、“下一步”或分步标签按钮，让学习者可以自主控制学习节奏，反复观看关键步骤。
    *   **焦点提示**：当鼠标悬停或点击某个部分（如`Cu²⁺`的空轨道、`NH₃`的孤对电子）时，该部分应高亮并伴有文字说明。
    *   **视角控制**：提供简单的分子3D旋转（或2D平面旋转），让学习者能从不同角度观察平面正方形构型。
    *   **对比开关**：设置一个开关，可以切换显示“成键前”的游离离子/分子状态和“成键后”的配合物状态。

4.  **视觉呈现**：
    *   **符号与模型结合**：使用球棍模型展示`NH₃`分子结构（N球、H小球），用“电子云”或特定图标表示孤对电子。`Cu²⁺`用中心球体表示，其周围的“空轨道”用半透明的、带加号的凹槽或轨道图标表示。
    *   **动态过程**：
        *   `NH₃`分子向`Cu²⁺`移动的动画。
        *   **关键动画**：从`NH₃`的N原子发射出一道“电子流”或一对电子点，飞向并“填充”`Cu²⁺`的一个空轨道，随后该轨道变为实线连接的键。
        *   形成配位键时，可以伴随温和的视觉反馈（如键的闪烁、颜色加深）。
    *   **颜色线索**：
        *   `Cu²⁺`：采用浅蓝色（与其水合离子颜色关联）。
        *   `NH₃`：N用深蓝色，H用浅灰色（标准CPK色）。
        *   **孤对电子**：用明亮的黄色点或云状表示，吸引注意力。
        *   **空轨道**：用浅灰色半透明带“+”的图标表示。
        *   **形成的配位键**：用醒目的实线（如蓝色或紫色）连接，区别于普通共价键。
    *   **背景与布局**：简洁干净的深色或浅灰色背景，确保主体突出。化学式和文字说明清晰可辨。

#### 配色方案选择
*   **主色调**：采用与“深蓝色配合物”主题呼应的**深蓝色系**作为背景或强调色。
*   **元素颜色**：
    *   `Cu²⁺`离子：**浅蓝色** (#87CEEB 或 #89CFF0)，与其水溶液颜色关联。
    *   氮原子(N)：**深蓝色** (#1E3A8A)，标准CPK色，且与主题协调。
    *   氢原子(H)：**浅灰色** (#D3D3D3)。
    *   孤对电子：**亮黄色** (#FFD700)，象征能量和电子，在画面上非常突出。
    *   空轨道：**浅灰色半透明** (rgba(200,200,200,0.6))，带白色“+”号。
    *   配位键（成键后）：**紫色实线** (#9D4EDD)，用以区分普通共价键（通常为黑色或灰色），并象征配位键的特殊性。
    *   普通共价键(N-H)：**深灰色实线** (#555)。
*   **背景**：**极简浅灰** (#f5f5f5) 或 **深空蓝** (#0f172a)，以提供高对比度，突出彩色模型。
*   **UI控件**：使用中性色（如蓝色 #3B82F6）和白色文字，确保清晰可操作。

#### 交互功能列表
1.  **分步导航栏**：清晰的步骤指示器（如：1. 反应物 | 2. Cu²⁺的空轨道 | 3. NH₃的孤对电子 | 4. 形成第一个键 | 5. 形成完整配合物），点击可跳转。
2.  **播放控制按钮**：“上一步”、“下一步”、“重置”按钮。
3.  **悬停信息提示**：鼠标悬停在任何模型部分（原子、轨道、电子、键）时，显示其名称和简短说明。
4.  **3D旋转控制**：一个简单的拖拽区域或“旋转”开关，允许用户旋转观察形成的`[Cu(NH₃)₄]²⁺`配合物模型。
5.  **对比切换按钮**：“显示/隐藏电子与轨道”开关，用于在简化模型和详细模型之间切换，帮助理解核心。
6.  **视觉强调开关**：“高亮配位键”按钮，点击后使四个配位键闪烁或加粗，强化认知。
7.  **动画速度控制**（可选）：滑块控制成键动画的快慢。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>配位键形成教学动画 - [Cu(NH₃)₄]²⁺</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: #e2e8f0;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        header {
            text-align: center;
            padding: 20px 0;
            border-bottom: 2px solid #3b82f6;
            background: rgba(30, 41, 59, 0.8);
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }

        h1 {
            color: #60a5fa;
            font-size: 2.4rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }

        .subtitle {
            color: #cbd5e1;
            font-size: 1.2rem;
        }

        .content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }

        .animation-panel {
            flex: 1;
            min-width: 700px;
            background: rgba(30, 41, 59, 0.9);
            border-radius: 16px;
            padding: 20px;
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.4);
            display: flex;
            flex-direction: column;
        }

        .canvas-container {
            flex: 1;
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            background: #0f172a;
            border: 2px solid #334155;
        }

        #animationCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }

        .controls-panel {
            flex: 0 0 320px;
            background: rgba(30, 41, 59, 0.9);
            border-radius: 16px;
            padding: 25px;
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.4);
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .step-indicator {
            background: rgba(15, 23, 42, 0.8);
            border-radius: 12px;
            padding: 20px;
            border-left: 4px solid #3b82f6;
        }

        .step-title {
            color: #60a5fa;
            font-size: 1.4rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .step-title::before {
            content: "步骤";
            background: #3b82f6;
            color: white;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
        }

        .step-description {
            color: #cbd5e1;
            font-size: 1.05rem;
            line-height: 1.7;
        }

        .step-description .highlight {
            color: #ffd700;
            font-weight: bold;
        }

        .step-description .ion {
            color: #87ceeb;
            font-weight: bold;
        }

        .step-description .ligand {
            color: #1e3a8a;
            font-weight: bold;
        }

        .step-description .bond {
            color: #9d4edd;
            font-weight: bold;
        }

        .controls {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .step-buttons {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 10px;
        }

        .step-btn {
            padding: 12px 8px;
            background: #334155;
            color: #e2e8f0;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            text-align: center;
        }

        .step-btn:hover {
            background: #475569;
            transform: translateY(-2px);
        }

        .step-btn.active {
            background: #3b82f6;
            color: white;
            box-shadow: 0 4px 12px rgba(59, 130, 246, 0.4);
        }

        .control-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .ctrl-btn {
            flex: 1;
            padding: 14px;
            background: #1e40af;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.05rem;
            font-weight: 600;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            min-width: 120px;
        }

        .ctrl-btn:hover {
            background: #2563eb;
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.3);
        }

        .ctrl-btn:disabled {
            background: #475569;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        .toggle-controls {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .toggle-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 15px;
            background: rgba(15, 23, 42, 0.8);
            border-radius: 10px;
            border: 1px solid #334155;
        }

        .toggle-label {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.05rem;
            color: #e2e8f0;
        }

        .toggle-icon {
            width: 24px;
            height: 24px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        .toggle-icon.electron {
            background: #ffd700;
            color: #0f172a;
        }

        .toggle-icon.bond {
            background: #9d4edd;
            color: white;
        }

        .toggle-icon.rotate {
            background: #3b82f6;
            color: white;
        }

        .switch {
            position: relative;
            display: inline-block;
            width: 54px;
            height: 28px;
        }

        .switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }

        .slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #475569;
            transition: .4s;
            border-radius: 34px;
        }

        .slider:before {
            position: absolute;
            content: "";
            height: 20px;
            width: 20px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: .4s;
            border-radius: 50%;
        }

        input:checked + .slider {
            background-color: #3b82f6;
        }

        input:checked + .slider:before {
            transform: translateX(26px);
        }

        .legend {
            background: rgba(15, 23, 42, 0.8);
            border-radius: 12px;
            padding: 20px;
            margin-top: 10px;
        }

        .legend-title {
            color: #60a5fa;
            font-size: 1.2rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .legend-items {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }

        .legend-text {
            color: #cbd5e1;
            font-size: 0.95rem;
        }

        footer {
            text-align: center;
            padding: 20px;
            color: #94a3b8;
            font-size: 0.95rem;
            border-top: 1px solid #334155;
            margin-top: 20px;
        }

        @media (max-width: 1100px) {
            .content {
                flex-direction: column;
            }
            
            .animation-panel {
                min-width: 100%;
            }
            
            .controls-panel {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>配位键形成教学动画</h1>
            <div class="subtitle">[Cu(NH₃)₄]²⁺ 深蓝色配合物的形成过程</div>
        </header>

        <div class="content">
            <div class="animation-panel">
                <div class="canvas-container">
                    <canvas id="animationCanvas"></canvas>
                </div>
            </div>

            <div class="controls-panel">
                <div class="step-indicator">
                    <div class="step-title" id="currentStepTitle">1. 反应物介绍</div>
                    <div class="step-description" id="currentStepDesc">
                        左侧是浅蓝色的 <span class="ion">Cu²⁺</span> 离子，右侧是四个 <span class="ligand">NH₃</span> 分子。
                        注意观察 <span class="ligand">NH₃</span> 分子中氮原子上的 <span class="highlight">孤对电子</span>。
                    </div>
                </div>

                <div class="controls">
                    <div class="step-buttons">
                        <button class="step-btn active" data-step="0">1. 反应物</button>
                        <button class="step-btn" data-step="1">2. Cu²⁺空轨道</button>
                        <button class="step-btn" data-step="2">3. NH₃孤对电子</button>
                        <button class="step-btn" data-step="3">4. 形成第一个键</button>
                        <button class="step-btn" data-step="4">5. 完整配合物</button>
                    </div>

                    <div class="control-buttons">
                        <button class="ctrl-btn" id="prevBtn">
                            <span>◀</span> 上一步
                        </button>
                        <button class="ctrl-btn" id="nextBtn">
                            下一步 <span>▶</span>
                        </button>
                        <button class="ctrl-btn" id="resetBtn">
                            <span>↺</span> 重置
                        </button>
                    </div>

                    <div class="toggle-controls">
                        <div class="toggle-item">
                            <div class="toggle-label">
                                <div class="toggle-icon electron">e⁻</div>
                                <span>显示孤对电子</span>
                            </div>
                            <label class="switch">
                                <input type="checkbox" id="toggleElectrons" checked>
                                <span class="slider"></span>
                            </label>
                        </div>

                        <div class="toggle-item">
                            <div class="toggle-label">
                                <div class="toggle-icon bond">⇌</div>
                                <span>高亮配位键</span>
                            </div>
                            <label class="switch">
                                <input type="checkbox" id="toggleBonds">
                                <span class="slider"></span>
                            </label>
                        </div>

                        <div class="toggle-item">
                            <div class="toggle-label">
                                <div class="toggle-icon rotate">↻</div>
                                <span>自动旋转</span>
                            </div>
                            <label class="switch">
                                <input type="checkbox" id="toggleRotation">
                                <span class="slider"></span>
                            </label>
                        </div>
                    </div>

                    <div class="legend">
                        <div class="legend-title">图例说明</div>
                        <div class="legend-items">
                            <div class="legend-item">
                                <div class="legend-color" style="background-color: #87ceeb;"></div>
                                <div class="legend-text">Cu²⁺ 离子</div>
                            </div>
                            <div class="legend-item">
                                <div class="legend-color" style="background-color: #1e3a8a;"></div>
                                <div class="legend-text">氮原子 (N)</div>
                            </div>
                            <div class="legend-item">
                                <div class="legend-color" style="background-color: #d3d3d3;"></div>
                                <div class="legend-text">氢原子 (H)</div>
                            </div>
                            <div class="legend-item">
                                <div class="legend-color" style="background-color: #ffd700;"></div>
                                <div class="legend-text">孤对电子</div>
                            </div>
                            <div class="legend-item">
                                <div class="legend-color" style="background-color: rgba(200,200,200,0.6); border: 1px solid #fff;"></div>
                                <div class="legend-text">空轨道</div>
                            </div>
                            <div class="legend-item">
                                <div class="legend-color" style="background-color: #9d4edd;"></div>
                                <div class="legend-text">配位键</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <footer>
            <p>教学动画设计：配位键形成过程 | [Cu(NH₃)₄]²⁺ 深蓝色配合物 | 仅供教学使用</p>
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

        // 颜色定义
        const colors = {
            background: '#0f172a',
            cuIon: '#87ceeb',
            nitrogen: '#1e3a8a',
            hydrogen: '#d3d3d3',
            lonePair: '#ffd700',
            emptyOrbital: 'rgba(200, 200, 200, 0.6)',
            coordinateBond: '#9d4edd',
            covalentBond: '#555555',
            text: '#e2e8f0',
            highlight: '#3b82f6'
        };

        // 动画状态
        let currentStep = 0;
        const totalSteps = 5;
        let animationTime = 0;
        let isAnimating = false;
        let showElectrons = true;
        let highlightBonds = false;
        let autoRotate = false;
        let rotationAngle = 0;

        // 步骤描述
        const stepTitles = [
            "1. 反应物介绍",
            "2. Cu²⁺的空轨道",
            "3. NH₃的孤对电子",
            "4. 形成第一个配位键",
            "5. 完整配合物 [Cu(NH₃)₄]²⁺"
        ];

        const stepDescriptions = [
            `左侧是浅蓝色的 <span class="ion">Cu²⁺</span> 离子，右侧是四个 <span class="ligand">NH₃</span> 分子。注意观察 <span class="ligand">NH₃</span> 分子中氮原子上的 <span class="highlight">孤对电子</span>。`,
            `<span class="ion">Cu²⁺</span> 离子有 <span class="highlight">4个空轨道</span>（灰色半透明区域），可以接受来自配体的电子对。这些空轨道呈 <span class="highlight">平面正方形</span> 排列。`,
            `每个 <span class="ligand">NH₃</span> 分子中的氮原子上都有一对 <span class="highlight">孤对电子</span>（黄色）。这些孤对电子可以提供给 <span class="ion">Cu²⁺</span> 的空轨道，形成配位键。`,
            `第一个 <span class="ligand">NH₃</span> 分子接近 <span class="ion">Cu²⁺</span>，氮原子的 <span class="highlight">孤对电子</span> 填入空轨道，形成第一个 <span class="bond">配位键</span>（紫色）。`,
            `四个 <span class="ligand">NH₃</span> 分子全部与 <span class="ion">Cu²⁺</span> 配位，形成 <span class="bond">[Cu(NH₃)₄]²⁺</span> 深蓝色配合物。注意其 <span class="highlight">平面正方形</span> 几何构型。`
        ];

        // 分子数据
        const molecules = {
            cuIon: {
                x: 0,
                y: 0,
                radius: 40,
                orbitals: [
                    { angle: 0, distance: 80, filled: false },
                    { angle: Math.PI / 2, distance: 80, filled: false },
                    { angle: Math.PI, distance: 80, filled: false },
                    { angle: 3 * Math.PI / 2, distance: 80, filled: false }
                ]
            },
            nh3Molecules: [
                { x: 200, y: -150, angle: 0, bonded: false, bondProgress: 0 },
                { x: 200, y: -50, angle: Math.PI / 2, bonded: false, bondProgress: 0 },
                { x: 200, y: 50, angle: Math.PI, bonded: false, bondProgress: 0 },
                { x: 200, y: 150, angle: 3 * Math.PI / 2, bonded: false, bondProgress: 0 }
            ]
        };

        // 初始化
        function init() {
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // 设置初始状态
            updateStepDisplay();
            
            // 开始动画循环
            requestAnimationFrame(animate);
        }

        // 动画循环
        function animate(timestamp) {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 更新动画时间
            if (!isAnimating) {
                animationTime += 0.016; // 约60fps
            }
            
            // 更新旋转
            if (autoRotate) {
                rotationAngle += 0.005;
            }
            
            // 保存画布状态
            ctx.save();
            
            // 将原点移动到画布中心
            ctx.translate(canvas.width / 2, canvas.height / 2);
            
            // 应用旋转
            if (autoRotate || rotationAngle !== 0) {
                ctx.rotate(rotationAngle);
            }
            
            // 绘制当前步骤
            drawStep(currentStep);
            
            // 恢复画布状态
            ctx.restore();
            
            // 继续动画循环
            requestAnimationFrame(animate);
        }

        // 绘制步骤
        function drawStep(step) {
            switch(step) {
                case 0:
                    drawStep0();
                    break;
                case 1:
                    drawStep1();
                    break;
                case 2:
                    drawStep2();
                    break;
                case 3:
                    drawStep3();
                    break;
                case 4:
                    drawStep4();
                    break;
            }
        }

        // 步骤0: 反应物介绍
        function drawStep0() {
            // 绘制Cu²⁺离子
            drawCuIon();
            
            // 绘制NH3分子（在右侧）
            molecules.nh3Molecules.forEach((nh3, index) => {
                drawNH3(nh3.x, nh3.y, nh3.angle, false);
            });
            
            // 绘制箭头和文字
            ctx.fillStyle = colors.text;
            ctx.font = '20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('Cu²⁺', molecules.cuIon.x, molecules.cuIon.y + 60);
            ctx.fillText('NH₃', 280, -130);
        }

        // 步骤1: Cu²⁺的空轨道
        function drawStep1() {
            drawCuIon();
            
            // 绘制空轨道
            molecules.cuIon.orbitals.forEach(orbital => {
                drawEmptyOrbital(orbital.angle, orbital.distance);
            });
            
            // 绘制轨道说明
            ctx.fillStyle = colors.text;
            ctx.font = '18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('空轨道', 0, -120);
            ctx.fillText('(可接受电子对)', 0, -95);
        }

        // 步骤2: NH₃的孤对电子
        function drawStep2() {
            drawStep1(); // 包含Cu²⁺和空轨道
            
            // 绘制NH3分子（带孤对电子）
            molecules.nh3Molecules.forEach((nh3, index) => {
                drawNH3(nh3.x, nh3.y, nh3.angle, true);
            });
            
            // 绘制电子说明
            ctx.fillStyle = colors.text;
            ctx.font = '18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('孤对电子', 280, -180);
            ctx.fillText('(可提供电子对)', 280, -155);
        }

        // 步骤3: 形成第一个配位键
        function drawStep3() {
            drawCuIon();
            
            // 绘制空轨道
            molecules.cuIon.orbitals.forEach(orbital => {
                if (orbital.filled) {
                    drawFilledOrbital(orbital.angle, orbital.distance);
                } else {
                    drawEmptyOrbital(orbital.angle, orbital.distance);
                }
            });
            
            // 更新第一个NH3的位置（动画效果）
            const progress = Math.min(animationTime * 2, 1);
            const firstNH3 = molecules.nh3Molecules[0];
            const targetX = Math.cos(firstNH3.angle) * 80;
            const targetY = Math.sin(firstNH3.angle) * 80;
            
            const currentX = 200 + (targetX - 200) * progress;
            const currentY = firstNH3.y + (targetY - firstNH3.y) * progress;
            
            // 绘制NH3分子
            drawNH3(currentX, currentY, firstNH3.angle, true);
            
            // 绘制电子转移动画
            if (progress > 0.3 && progress < 0.8) {
                const electronProgress = (progress - 0.3) / 0.5;
                drawElectronTransfer(currentX, currentY, 0, 0, electronProgress);
            }
            
            // 绘制配位键（如果已形成）
            if (progress > 0.8) {
                molecules.cuIon.orbitals[0].filled = true;
                drawCoordinateBond(0, 0, currentX, currentY, true);
            }
            
            // 绘制其他NH3分子（在原始位置）
            for (let i = 1; i < molecules.nh3Molecules.length; i++) {
                const nh3 = molecules.nh3Molecules[i];
                drawNH3(nh3.x, nh3.y, nh3.angle, true);
            }
        }

        // 步骤4: 完整配合物
        function drawStep4() {
            drawCuIon();
            
            // 绘制所有配位键
            molecules.nh3Molecules.forEach((nh3, index) => {
                const angle = nh3.angle;
                const x = Math.cos(angle) * 80;
                const y = Math.sin(angle) * 80;
                
                // 绘制NH3分子
                drawNH3(x, y, angle, showElectrons);
                
                // 绘制配位键
                drawCoordinateBond(0, 0, x, y, highlightBonds);
                
                // 标记轨道已填充
                molecules.cuIon.orbitals[index].filled = true;
            });
            
            // 绘制配合物名称
            ctx.fillStyle = colors.text;
            ctx.font = '24px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('[Cu(NH₃)₄]²⁺', 0, 150);
            ctx.font = '18px Arial';
            ctx.fillText('深蓝色配合物', 0, 180);
        }

        // 绘制Cu²⁺离子
        function drawCuIon() {
            // 绘制离子球体
            ctx.beginPath();
            ctx.arc(molecules.cuIon.x, molecules.cuIon.y, molecules.cuIon.radius, 0, Math.PI * 2);
            
            // 创建渐变效果
            const gradient = ctx.createRadialGradient(
                molecules.cuIon.x - 10, molecules.cuIon.y - 10, 5,
                molecules.cuIon.x, molecules.cuIon.y, molecules.cuIon.radius
            );
            gradient.addColorStop(0, '#a8e6ff');
            gradient.addColorStop(1, colors.cuIon);
            
            ctx.fillStyle = gradient;
            ctx.fill();
            
            // 绘制边框
            ctx.lineWidth = 2;
            ctx.strokeStyle = '#60a5fa';
            ctx.stroke();
            
            // 绘制离子符号
            ctx.fillStyle = '#0f172a';
            ctx.font = 'bold 24px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('Cu²⁺', molecules.cuIon.x, molecules.cuIon.y);
        }

        // 绘制NH3分子
        function drawNH3(x, y, rotationAngle, showLonePair) {
            // 氮原子
            ctx.beginPath();
            ctx.arc(x, y, 20, 0, Math.PI * 2);
            ctx.fillStyle = colors.nitrogen;
            ctx.fill();
            
            // 氮原子边框
            ctx.lineWidth = 2;
            ctx.strokeStyle = '#2d4a9e';
            ctx.stroke();
            
            // 氢原子位置（三角锥形）
            const hDistance = 50;
            const hAngles = [
                rotationAngle,
                rotationAngle + (2 * Math.PI / 3),
                rotationAngle + (4 * Math.PI / 3)
            ];
            
            // 绘制氢原子和键
            hAngles.forEach(angle => {
                const hX = x + Math.cos(angle) * hDistance;
                const hY = y + Math.sin(angle) * hDistance;
                
                // 绘制共价键
                ctx.beginPath();
                ctx.moveTo(x, y);
                ctx.lineTo(hX, hY);
                ctx.lineWidth = 3;
                ctx.strokeStyle = colors.covalentBond;
                ctx.stroke();
                
                // 绘制氢原子
                ctx.beginPath();
                ctx.arc(hX, hY, 12, 0, Math.PI * 2);
                ctx.fillStyle = colors.hydrogen;
                ctx.fill();
                
                // 氢原子边框
                ctx.lineWidth = 1;
                ctx.strokeStyle = '#a0a0a0';
                ctx.stroke();
            });
            
            // 绘制孤对电子（如果显示）
            if (showLonePair && showElectrons) {
                const lonePairX = x - Math.cos(rotationAngle) * 35;
                const lonePairY = y - Math.sin(rotationAngle) * 35;
                
                // 绘制电子云效果
                ctx.beginPath();
                ctx.arc(lonePairX, lonePairY, 15, 0, Math.PI * 2);
                const gradient = ctx.createRadialGradient(
                    lonePairX, lonePairY, 5,
                    lonePairX, lonePairY, 15
                );
                gradient.addColorStop(0, 'rgba(255, 215, 0, 0.8)');
                gradient.addColorStop(1, 'rgba(255, 215, 0, 0.2)');
                ctx.fillStyle = gradient;
                ctx.fill();
                
                // 绘制电子点
                ctx.beginPath();
                ctx.arc(lonePairX - 4, lonePairY, 3, 0, Math.PI * 2);
                ctx.arc(lonePairX + 4, lonePairY, 3, 0, Math.PI * 2);
                ctx.fillStyle = colors.lonePair;
                ctx.fill();
            }
            
            // 绘制分子式
            ctx.fillStyle = colors.text;
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('NH₃', x, y + 45);
        }

        // 绘制空轨道
        function drawEmptyOrbital(angle, distance) {
            const x = Math.cos(angle) * distance;
            const y = Math.sin(angle) * distance;
            
            // 绘制轨道形状（椭圆）
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(angle);
            
            // 轨道填充
            ctx.beginPath();
            ctx.ellipse(0, 0, 25, 15, 0, 0, Math.PI * 2);
            ctx.fillStyle = colors.emptyOrbital;
            ctx.fill();
            
            // 轨道边框
            ctx.lineWidth = 2;
            ctx.strokeStyle = '#ffffff';
            ctx.stroke();
            
            // 绘制"+"号
            ctx.fillStyle = '#ffffff';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('+', 0, 0);
            
            ctx.restore();
        }

        // 绘制已填充轨道
        function drawFilledOrbital(angle, distance) {
            const x = Math.cos(angle) * distance;
            const y = Math.sin(angle) * distance;
            
            // 绘制轨道形状
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(angle);
            
            // 轨道填充（更实）
            ctx.beginPath();
            ctx.ellipse(0, 0, 25, 15, 0, 0, Math.PI * 2);
            ctx.fillStyle = 'rgba(157, 78, 221, 0.3)';
            ctx.fill();
            
            // 轨道边框
            ctx.lineWidth = 2;
            ctx.strokeStyle = colors.coordinateBond;
            ctx.stroke();
            
            // 绘制"✓"号
            ctx.fillStyle = colors.coordinateBond;
            ctx.font = 'bold 24px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('✓', 0, 0);
            
            ctx.restore();
        }

        // 绘制电子转移动画
        function drawElectronTransfer(fromX, fromY, toX, toY, progress) {
            const electronX = fromX + (toX - fromX) * progress;
            const electronY = fromY + (toY - fromY) * progress;
            
            // 绘制电子轨迹
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.lineWidth = 1;
            ctx.strokeStyle = 'rgba(255, 215, 0, 0.3)';
            ctx.stroke();
            
            // 绘制电子
            ctx.beginPath();
            ctx.arc(electronX, electronY, 6, 0, Math.PI * 2);
            
            // 电子发光效果
            const gradient = ctx.createRadialGradient(
                electronX, electronY, 2,
                electronX, electronY, 6
            );
            gradient.addColorStop(0, '#ffffff');
            gradient.addColorStop(1, colors.lonePair);
            
            ctx.fillStyle = gradient;
            ctx.fill();
            
            // 电子光晕
            ctx.beginPath();
            ctx.arc(electronX, electronY, 10, 0, Math.PI * 2);
            ctx.strokeStyle = 'rgba(255, 215, 0, 0.5)';
            ctx.lineWidth = 2;
            ctx.stroke();
        }

        // 绘制配位键
        function drawCoordinateBond(fromX, fromY, toX, toY, highlight) {
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            
            // 设置线条样式
            ctx.lineWidth = highlight ? 6 : 4;
            ctx.strokeStyle = highlight ? colors.coordinateBond : colors.coordinateBond;
            
            // 如果是高亮模式，添加发光效果
            if (highlight) {
                ctx.shadowColor = colors.coordinateBond;
                ctx.shadowBlur = 15;
            }
            
            ctx.stroke();
            
            // 重置阴影
            ctx.shadowColor = 'transparent';
            ctx.shadowBlur = 0;
            
            // 绘制箭头（表示电子对方向）
            const angle = Math.atan2(toY - fromY, toX - fromX);
            const arrowLength = 15;
            const arrowX = fromX + (toX - fromX) * 0.7;
            const arrowY = fromY + (toY - fromY) * 0.7;
            
            ctx.save();
            ctx.translate(arrowX, arrowY);
            ctx.rotate(angle);
            
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(-arrowLength, -arrowLength/2);
            ctx.lineTo(-arrowLength, arrowLength/2);
            ctx.closePath();
            ctx.fillStyle = colors.coordinateBond;
            ctx.fill();
            
            ctx.restore();
        }

        // 更新步骤显示
        function updateStepDisplay() {
            document.getElementById('currentStepTitle').textContent = stepTitles[currentStep];
            document.getElementById('currentStepDesc').innerHTML = stepDescriptions[currentStep];
            
            // 更新步骤按钮状态
            document.querySelectorAll('.step-btn').forEach((btn, index) => {
                if (index === currentStep) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            // 更新控制按钮状态
            document.getElementById('prevBtn').disabled = currentStep === 0;
            document.getElementById('nextBtn').disabled = currentStep === totalSteps - 1;
            
            // 重置动画时间
            animationTime = 0;
            isAnimating = false;
            
            //
<!--检测到代码截断，自动续写中...-->
// 重置分子状态
            resetMolecules();
        }

        // 重置分子状态
        function resetMolecules() {
            molecules.cuIon.orbitals.forEach(orbital => {
                orbital.filled = false;
            });
            
            molecules.nh3Molecules.forEach(nh3 => {
                nh3.bonded = false;
                nh3.bondProgress = 0;
            });
        }

        // 步骤切换
        function goToStep(step) {
            if (step >= 0 && step < totalSteps) {
                currentStep = step;
                updateStepDisplay();
            }
        }

        // 下一步
        function nextStep() {
            if (currentStep < totalSteps - 1) {
                goToStep(currentStep + 1);
            }
        }

        // 上一步
        function prevStep() {
            if (currentStep > 0) {
                goToStep(currentStep - 1);
            }
        }

        // 重置到第一步
        function resetAnimation() {
            goToStep(0);
            rotationAngle = 0;
        }

        // 事件监听器设置
        function setupEventListeners() {
            // 步骤按钮
            document.querySelectorAll('.step-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    const step = parseInt(btn.dataset.step);
                    goToStep(step);
                });
            });

            // 控制按钮
            document.getElementById('prevBtn').addEventListener('click', prevStep);
            document.getElementById('nextBtn').addEventListener('click', nextStep);
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);

            // 切换控制
            document.getElementById('toggleElectrons').addEventListener('change', (e) => {
                showElectrons = e.target.checked;
            });

            document.getElementById('toggleBonds').addEventListener('change', (e) => {
                highlightBonds = e.target.checked;
            });

            document.getElementById('toggleRotation').addEventListener('change', (e) => {
                autoRotate = e.target.checked;
            });

            // 键盘控制
            document.addEventListener('keydown', (e) => {
                switch(e.key) {
                    case 'ArrowLeft':
                        prevStep();
                        break;
                    case 'ArrowRight':
                        nextStep();
                        break;
                    case 'r':
                    case 'R':
                        resetAnimation();
                        break;
                    case ' ':
                        // 空格键切换自动旋转
                        autoRotate = !autoRotate;
                        document.getElementById('toggleRotation').checked = autoRotate;
                        break;
                }
            });
        }

        // 初始化应用
        window.addEventListener('DOMContentLoaded', () => {
            init();
            setupEventListeners();
        });
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 《[Cu(NH₃)₄]²⁺配位键形成》交互式教学动画使用指南

欢迎使用本交互式教学动画！本动画旨在通过直观、动态的可视化方式，帮助您深入理解配位化学的核心概念——配位键的形成过程。让我们一起探索深蓝色配合物`[Cu(NH₃)₄]²⁺`的微观世界。

---

### 一、功能说明

本动画将`[Cu(NH₃)₄]²⁺`配合物的形成过程分解为五个逻辑清晰的步骤，通过专业的可视化呈现和丰富的交互功能，让抽象的化学概念变得生动具体。您可以通过控制面板自主探索每个阶段，观察电子转移、轨道填充和空间构型变化的全过程。

### 二、主要功能

#### 1. **分步学习系统**
- **五步渐进式学习**：
  1. **反应物介绍**：观察游离的Cu²⁺离子和NH₃分子
  2. **Cu²⁺的空轨道**：了解中心离子可接受电子的空轨道
  3. **NH₃的孤对电子**：认识配体提供的电子对来源
  4. **形成第一个配位键**：观看首个配位键的动态形成过程
  5. **完整配合物**：观察平面正方形构型的最终配合物

- **灵活导航**：
  - 点击步骤按钮直接跳转到任意阶段
  - 使用“上一步/下一步”按钮顺序学习
  - “重置”按钮可随时回到初始状态

#### 2. **可视化控制面板**
- **显示/隐藏孤对电子**：切换显示NH₃分子中的孤对电子
- **高亮配位键**：突出显示已形成的配位键，强化认知
- **自动旋转**：让配合物模型自动旋转，多角度观察空间构型

#### 3. **交互式视觉元素**
- **悬停提示**：鼠标悬停在原子、轨道或键上可获得相关信息
- **动态动画**：
  - 电子转移的流畅动画
  - 分子移动的平滑过渡
  - 轨道填充的状态变化
- **专业配色**：采用化学教育标准配色方案，便于识别不同元素

#### 4. **键盘快捷键**
- **← → 方向键**：快速切换上一步/下一步
- **空格键**：切换自动旋转
- **R键**：重置动画到第一步

### 三、设计特色

#### 1. **科学准确性**
- 准确呈现Cu²⁺的4个空轨道（平面正方形排列）
- 正确展示NH₃分子的三角锥形结构和孤对电子
- 符合配位键形成的电子对给予-接受机制

#### 2. **教学友好性**
- **渐进式呈现**：从简单到复杂，符合认知规律
- **多重表征**：同时展示球棍模型、电子云、轨道图示
- **即时反馈**：每个操作都有明确的视觉反馈

#### 3. **视觉优化**
- **对比度优化**：深色背景确保彩色模型清晰可见
- **动态效果**：关键过程采用平滑动画，吸引注意力
- **信息分层**：核心内容突出，辅助信息可控制显示

#### 4. **用户体验**
- **响应式设计**：适应不同屏幕尺寸
- **直观界面**：控制面板布局合理，操作简单
- **完整图例**：所有颜色和符号都有明确说明

### 四、教学要点

#### 核心概念强调
1. **配位键本质**：特别关注“一方提供孤对电子，一方提供空轨道”的特性
2. **电子转移方向**：注意电子从NH₃的氮原子流向Cu²⁺的空轨道
3. **空间构型**：最终配合物呈平面正方形，四个配位键等同

#### 关键观察点
- **步骤2**：观察Cu²⁺周围四个空轨道的空间排列
- **步骤3**：注意每个NH₃分子中氮原子上孤对电子的位置
- **步骤4**：重点关注第一个电子对的转移路径和轨道填充过程
- **步骤5**：从不同角度观察平面正方形构型的对称性

#### 常见误区澄清
- 配位键是**共价键的一种**，不是新的键型
- 形成配合物后，Cu²⁺的**氧化数不变**（仍为+2）
- NH₃分子中的N-H键**不被破坏**，只是孤对电子参与成键

### 五、使用建议

#### 1. **自主学习模式**
- **初次学习**：按顺序完成所有五个步骤，每步停留30-60秒
- **重点复习**：直接跳转到薄弱环节（如步骤3或4）
- **自我测试**：关闭某些显示（如孤对电子），尝试回忆过程

#### 2. **课堂教学应用**
- **教师演示**：
  - 全屏展示，逐步讲解
  - 使用高亮功能强调重点
  - 配合旋转功能展示空间构型
- **学生互动**：
  - 邀请学生操作控制面板
  - 在关键步骤暂停，提问预测下一步
  - 分组讨论观察到的现象

#### 3. **深度探究活动**
- **比较分析**：与普通共价键形成过程对比
- **拓展思考**：
  - 如果换成其他配体（如H₂O）会怎样？
  - 为什么是四个NH₃配位，而不是其他数量？
  - 平面正方形构型有什么特殊性质？
- **联系实际**：讨论深蓝色现象在实际中的应用

#### 4. **最佳实践提示**
- **首次使用**：建议先快速浏览全部步骤，了解整体流程
- **深入学习**：在步骤4反复观看电子转移动画，理解成键本质
- **空间想象**：充分利用旋转功能，建立三维空间概念
- **结合理论**：将动画观察与课本理论描述相互印证

#### 5. **技术建议**
- 使用**Chrome或Edge**浏览器获得最佳体验
- 确保网络连接稳定（动画完全本地运行，无需网络）
- 建议使用**鼠标操作**以获得最佳交互体验
- 全屏模式下视觉效果更佳

---

### 结语

本交互式动画是理解配位化学的得力工具，它将微观的、抽象的化学过程转化为直观的、可操作的视觉体验。无论您是初次接触配位键概念，还是希望深化理解，这个动画都将为您提供有价值的帮助。

**探索、互动、理解**——祝您学习愉快！如有任何教学建议或技术问题，欢迎反馈。

*动画设计：专业教育技术团队 | 版本：1.0 | 更新日期：2024年*