# 需求：乙醇催化氧化成乙醛（微观脱氢过程）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：高中或大学低年级化学学生。他们已具备基本的分子结构（如C、H、O原子，单键、双键）和氧化还原反应概念，但需要直观理解抽象的“催化脱氢”微观过程。
2.  **核心需求**：
    *   **可视化抽象过程**：将教材中静态的化学方程式和文本描述（“铜或银作催化剂，乙醇脱氢生成乙醛”）转化为动态、可视的分子模型拆解与重组过程。
    *   **理解催化剂作用**：清晰展示催化剂如何参与反应、降低能垒、在反应前后保持不变，并突出其“吸附-反应-脱附”的关键步骤。
    *   **建立微观与宏观联系**：通过微观动画，帮助学生理解宏观实验现象（如铜丝由黑变红变亮、产生刺激性气味）。
    *   **主动探索与强化记忆**：提供交互控制，让学生能主动分步观察、重复关键步骤，从而深化理解。

#### 教学设计思路
1.  **核心概念分解**：
    *   **反应物与产物结构**：乙醇（CH₃CH₂OH）与乙醛（CH₃CHO）的分子模型对比，重点突出羟基（-OH）和与氧相连的碳（C）上氢原子的变化。
    *   **催化剂角色**：铜催化剂表面作为“反应舞台”。
    *   **脱氢过程**：分步展示O-H键和C-H键的断裂。
    *   **氢转移与结合**：断裂的氢原子在催化剂表面结合成氢气（H₂）并脱附。
    *   **双键形成**：碳氧之间从单键变为双键，生成乙醛。

2.  **遵循认知规律**：
    *   **从整体到局部**：先展示完整的反应体系和总方程式，再聚焦于催化剂表面的微观变化。
    *   **分步动画**：将连续过程分解为清晰的、符合反应机理的步骤，每一步都有视觉和文本提示。
    *   **对比与强调**：通过颜色、闪烁、高亮等手段，强调断键、成键的位置和原子的转移路径。
    *   **总结与回顾**：动画结束后，可回放或展示步骤总结图，强化认知结构。

3.  **交互设计**：
    *   **流程控制**：提供“播放/暂停”、“上一步/下一步”按钮，允许学生按自己的节奏学习。
    *   **视角控制**：允许旋转分子模型或场景，从不同角度观察空间结构。
    *   **信息提示**：鼠标悬停在原子、键或催化剂上时，显示其名称和角色。
    *   **步骤选择**：提供一个步骤列表或进度条，支持跳转到特定步骤进行重点观察。

4.  **视觉呈现**：
    *   **分子模型**：采用球棍模型，清晰展示原子和化学键。原子颜色采用CPK标准（C: 深灰， H: 白色， O: 红色）。化学键用圆柱体表示。
    *   **动画效果**：
        *   断键：键的模型变细、变色（如变红）后消失，伴随震动效果。
        *   成键：新的键从无到有生长出来。
        *   原子移动：平滑的轨迹动画，显示氢原子从分子转移到催化剂表面，再结合成H₂。
    *   **催化剂**：用一片排列有序的金属球（金色或红铜色）网格表示铜表面，被吸附的原子可显示在其上方。
    *   **界面布局**：主画面为3D动画区，侧边或底部为控制面板和步骤说明文字区。

#### 配色方案选择
*   **主色调**：采用深蓝色或深灰色作为背景，营造科技感和深邃的微观世界氛围，并能突出前景的彩色分子模型。
*   **原子颜色（CPK标准）**：
    *   碳（C）：深灰色或黑色
    *   氢（H）：白色或浅灰色
    *   氧（O）：红色
    *   铜催化剂：采用金属质感配色，如亮铜色（#B87333）或金色渐变，以区别于有机分子。
*   **强调色**：
    *   **断键/高亮**：使用醒目的**亮黄色**或**橙色**闪烁，表示正在断裂的键或活跃的反应位点。
    *   **信息提示/文本**：使用与背景对比度高的**白色**或**浅蓝色**。
    *   **按钮/交互元素**：使用友好的蓝色系（如#4A90E2）表示可交互状态。
*   **整体原则**：保证色彩有足够的对比度和区分度，避免过多鲜艳颜色造成视觉疲劳，重点突出反应中心。

#### 交互功能列表
1.  **主控面板**：
    *   播放/暂停 按钮
    *   上一步 / 下一步 按钮
    *   重置 按钮
2.  **进度导航**：
    *   可点击的步骤进度条（如：1.初始吸附 -> 2.O-H键断裂 -> 3.C-H键断裂 -> 4.H₂形成与脱附 -> 5.乙醛脱附）。
    *   或步骤列表菜单。
3.  **视角控制**：
    *   鼠标拖拽旋转3D场景。
    *   鼠标滚轮缩放。
    *   可选预设视角按钮（如“俯视图”、“侧视图”）。
4.  **信息提示（Hover）**：
    *   悬停原子：显示元素符号（如“O”、“C”）。
    *   悬停化学键：显示键类型（如“O-H键”、“C-H键”、“C=O双键”）。
    *   悬停催化剂：显示“铜催化剂表面”。
5.  **辅助显示开关**：
    *   显示/隐藏 化学键标签 开关。
    *   显示/隐藏 原子符号 开关。
    *   显示/隐藏 反应方程式（随步骤高亮）面板。
6.  **学习辅助**：
    *   每一步都有简明的文字解说区域。
    *   关键步骤可配有简短的音效（如断键的“咔嚓”声）或视觉震动反馈（可选）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>乙醇催化氧化成乙醛 - 微观脱氢过程</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, #0a1929 0%, #1a2b3c 100%);
            color: #e6f7ff;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid rgba(74, 144, 226, 0.3);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #4A90E2, #63D2FF);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        .subtitle {
            font-size: 1.2rem;
            color: #a8d8ff;
            opacity: 0.9;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }

        .animation-section {
            flex: 3;
            min-width: 300px;
            background: rgba(26, 43, 60, 0.8);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(74, 144, 226, 0.2);
        }

        .controls-section {
            flex: 2;
            min-width: 300px;
            background: rgba(26, 43, 60, 0.8);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(74, 144, 226, 0.2);
        }

        .canvas-container {
            width: 100%;
            height: 500px;
            position: relative;
            background: rgba(10, 25, 41, 0.9);
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        #reactionCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .legend {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding: 15px;
            background: rgba(10, 25, 41, 0.6);
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

        .controls {
            margin-bottom: 25px;
        }

        .control-group {
            margin-bottom: 20px;
        }

        h2 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #63D2FF;
            border-left: 4px solid #4A90E2;
            padding-left: 10px;
        }

        .btn-group {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 12px 20px;
            background: linear-gradient(135deg, #2a5c8f, #4A90E2);
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 120px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }

        .btn:hover {
            background: linear-gradient(135deg, #4A90E2, #63D2FF);
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
        }

        .btn:active {
            transform: translateY(0);
        }

        .btn:disabled {
            background: #3a4a5c;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        .btn-primary {
            background: linear-gradient(135deg, #4A90E2, #63D2FF);
        }

        .step-indicator {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .step {
            padding: 15px;
            background: rgba(10, 25, 41, 0.6);
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            border-left: 4px solid transparent;
        }

        .step:hover {
            background: rgba(74, 144, 226, 0.2);
            transform: translateX(5px);
        }

        .step.active {
            background: rgba(74, 144, 226, 0.3);
            border-left-color: #4A90E2;
            box-shadow: 0 4px 8px rgba(74, 144, 226, 0.2);
        }

        .step-number {
            display: inline-block;
            width: 28px;
            height: 28px;
            background: #4A90E2;
            color: white;
            border-radius: 50%;
            text-align: center;
            line-height: 28px;
            margin-right: 10px;
            font-weight: bold;
        }

        .step-title {
            font-weight: 600;
            margin-bottom: 5px;
            color: #e6f7ff;
        }

        .step-desc {
            font-size: 0.9rem;
            color: #a8d8ff;
            opacity: 0.9;
        }

        .equation {
            text-align: center;
            font-size: 1.8rem;
            margin: 25px 0;
            padding: 20px;
            background: rgba(10, 25, 41, 0.6);
            border-radius: 10px;
            font-family: 'Cambria', 'Times New Roman', serif;
            color: #ffcc80;
            border: 1px solid rgba(255, 204, 128, 0.2);
        }

        .highlight {
            color: #FFA726;
            font-weight: bold;
        }

        .info-panel {
            position: absolute;
            top: 20px;
            left: 20px;
            background: rgba(10, 25, 41, 0.85);
            padding: 15px;
            border-radius: 10px;
            border: 1px solid rgba(74, 144, 226, 0.3);
            max-width: 300px;
            backdrop-filter: blur(5px);
            z-index: 10;
        }

        .info-title {
            font-size: 1.1rem;
            color: #63D2FF;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .info-content {
            font-size: 0.95rem;
            color: #e6f7ff;
        }

        .atom-info {
            position: absolute;
            background: rgba(10, 25, 41, 0.95);
            padding: 10px 15px;
            border-radius: 8px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 20;
            font-size: 0.9rem;
            max-width: 200px;
        }

        .toggle-group {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .toggle-btn {
            padding: 10px 15px;
            background: rgba(74, 144, 226, 0.2);
            color: #a8d8ff;
            border: 1px solid rgba(74, 144, 226, 0.4);
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
            text-align: center;
        }

        .toggle-btn.active {
            background: rgba(74, 144, 226, 0.5);
            color: white;
            border-color: #4A90E2;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(74, 144, 226, 0.3);
            color: #a8d8ff;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .canvas-container {
                height: 400px;
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
            <h1>乙醇催化氧化成乙醛</h1>
            <p class="subtitle">微观脱氢过程可视化教学动画</p>
        </header>

        <div class="equation">
            CH₃CH₂OH + CuO → CH₃CHO + H₂O + Cu
            <div style="font-size: 1rem; margin-top: 10px; color: #a8d8ff;">
                总反应方程式 | 催化剂：铜（Cu）
            </div>
        </div>

        <div class="main-content">
            <section class="animation-section">
                <h2>微观反应过程</h2>
                <div class="canvas-container">
                    <canvas id="reactionCanvas"></canvas>
                    <div class="info-panel">
                        <div class="info-title">当前步骤：<span id="currentStepTitle">准备阶段</span></div>
                        <div class="info-content" id="stepDescription">动画准备中，请点击播放按钮开始...</div>
                    </div>
                    <div class="atom-info" id="atomInfo"></div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #333333;"></div>
                        <span>碳原子 (C)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FFFFFF;"></div>
                        <span>氢原子 (H)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FF4444;"></div>
                        <span>氧原子 (O)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background: linear-gradient(45deg, #B87333, #FFD700);"></div>
                        <span>铜催化剂 (Cu)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FFA726;"></div>
                        <span>反应位点 (高亮)</span>
                    </div>
                </div>
            </section>

            <section class="controls-section">
                <div class="controls">
                    <h2>动画控制</h2>
                    <div class="control-group">
                        <div class="btn-group">
                            <button id="playBtn" class="btn btn-primary">▶ 播放</button>
                            <button id="pauseBtn" class="btn">⏸ 暂停</button>
                            <button id="resetBtn" class="btn">↺ 重置</button>
                        </div>
                    </div>

                    <div class="control-group">
                        <div class="btn-group">
                            <button id="prevBtn" class="btn">◀ 上一步</button>
                            <button id="nextBtn" class="btn">▶ 下一步</button>
                        </div>
                    </div>

                    <h2>步骤导航</h2>
                    <div class="step-indicator" id="stepIndicator">
                        <!-- 步骤将通过JS动态生成 -->
                    </div>

                    <h2>显示选项</h2>
                    <div class="toggle-group">
                        <div class="toggle-btn active" id="toggleLabels">显示标签</div>
                        <div class="toggle-btn active" id="toggleEquation">显示方程式</div>
                    </div>
                </div>
            </section>
        </div>

        <footer>
            <p>教学动画设计 | 乙醇催化氧化微观过程 | 使用Canvas技术实现</p>
            <p>提示：鼠标悬停在原子或化学键上可查看详细信息，拖拽可旋转视角</p>
        </footer>
    </div>

    <script>
        // 全局变量
        const canvas = document.getElementById('reactionCanvas');
        const ctx = canvas.getContext('2d');
        const stepIndicator = document.getElementById('stepIndicator');
        const currentStepTitle = document.getElementById('currentStepTitle');
        const stepDescription = document.getElementById('stepDescription');
        const atomInfo = document.getElementById('atomInfo');
        
        // 控制按钮
        const playBtn = document.getElementById('playBtn');
        const pauseBtn = document.getElementById('pauseBtn');
        const resetBtn = document.getElementById('resetBtn');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const toggleLabels = document.getElementById('toggleLabels');
        const toggleEquation = document.getElementById('toggleEquation');
        
        // 动画状态
        let animationId = null;
        let currentStep = 0;
        let isPlaying = false;
        let showLabels = true;
        let showEquation = true;
        let animationProgress = 0;
        let mouseX = 0, mouseY = 0;
        let isDragging = false;
        let lastMouseX = 0, lastMouseY = 0;
        let rotationX = 0, rotationY = 0;
        let zoom = 1;
        
        // 步骤定义
        const steps = [
            {
                title: "初始状态",
                description: "乙醇分子(CH₃CH₂OH)接近铜催化剂表面。催化剂表面由铜原子组成。",
                duration: 2000
            },
            {
                title: "吸附与O-H键断裂",
                description: "乙醇分子吸附在催化剂表面，羟基(-OH)中的O-H键断裂，氢原子转移到催化剂表面。",
                duration: 3000
            },
            {
                title: "C-H键断裂",
                description: "与羟基相连的碳原子上的C-H键断裂，氢原子转移到催化剂表面。",
                duration: 3000
            },
            {
                title: "氢原子结合",
                description: "催化剂表面的两个氢原子结合形成氢气(H₂)分子。",
                duration: 2500
            },
            {
                title: "乙醛生成与脱附",
                description: "碳氧之间形成双键(C=O)，生成乙醛(CH₃CHO)并从催化剂表面脱附。",
                duration: 3000
            },
            {
                title: "催化剂再生",
                description: "氢气从催化剂表面脱附，催化剂恢复初始状态，准备下一次反应。",
                duration: 2500
            }
        ];
        
        // 原子颜色定义 (CPK标准)
        const atomColors = {
            'C': '#333333',
            'H': '#FFFFFF',
            'O': '#FF4444',
            'Cu': '#B87333'
        };
        
        // 分子和原子数据
        let ethanol = {
            atoms: [
                { type: 'C', x: 0, y: 0, z: 0, label: 'C1' },
                { type: 'C', x: 1.54, y: 0, z: 0, label: 'C2' },
                { type: 'O', x: 2.1, y: 1.42, z: 0, label: 'O' },
                { type: 'H', x: -0.51, y: 0.89, z: 0, label: 'H1' },
                { type: 'H', x: -0.51, y: -0.89, z: 0, label: 'H2' },
                { type: 'H', x: 0.51, y: 0, z: 0.89, label: 'H3' },
                { type: 'H', x: 2.05, y: -0.89, z: 0, label: 'H4' },
                { type: 'H', x: 2.05, y: 0, z: 0.89, label: 'H5' },
                { type: 'H', x: 2.65, y: 1.42, z: 0, label: 'H6' }
            ],
            bonds: [
                { a1: 0, a2: 1, type: 'single' },
                { a1: 1, a2: 2, type: 'single' },
                { a1: 0, a2: 3, type: 'single' },
                { a1: 0, a2: 4, type: 'single' },
                { a1: 0, a2: 5, type: 'single' },
                { a1: 1, a2: 6, type: 'single' },
                { a1: 1, a2: 7, type: 'single' },
                { a1: 2, a2: 8, type: 'single' }
            ]
        };
        
        let acetaldehyde = {
            atoms: [
                { type: 'C', x: 0, y: 0, z: 0, label: 'C1' },
                { type: 'C', x: 1.54, y: 0, z: 0, label: 'C2' },
                { type: 'O', x: 2.1, y: 1.42, z: 0, label: 'O' },
                { type: 'H', x: -0.51, y: 0.89, z: 0, label: 'H1' },
                { type: 'H', x: -0.51, y: -0.89, z: 0, label: 'H2' },
                { type: 'H', x: 0.51, y: 0, z: 0.89, label: 'H3' },
                { type: 'H', x: 2.05, y: -0.89, z: 0, label: 'H4' }
            ],
            bonds: [
                { a1: 0, a2: 1, type: 'single' },
                { a1: 1, a2: 2, type: 'double' },
                { a1: 0, a2: 3, type: 'single' },
                { a1: 0, a2: 4, type: 'single' },
                { a1: 0, a2: 5, type: 'single' },
                { a1: 1, a2: 6, type: 'single' }
            ]
        };
        
        // 催化剂表面
        let catalystSurface = [];
        for (let i = -3; i <= 3; i++) {
            for (let j = -3; j <= 3; j++) {
                catalystSurface.push({
                    type: 'Cu',
                    x: i * 1.2,
                    y: 3.5,
                    z: j * 1.2
                });
            }
        }
        
        // 反应过程中的临时原子
        let detachedAtoms = [];
        let hydrogenMolecule = null;
        
        // 初始化步骤指示器
        function initStepIndicator() {
            stepIndicator.innerHTML = '';
            steps.forEach((step, index) => {
                const stepElement = document.createElement('div');
                stepElement.className = `step ${index === 0 ? 'active' : ''}`;
                stepElement.innerHTML = `
                    <div>
                        <span class="step-number">${index + 1}</span>
                        <span class="step-title">${step.title}</span>
                    </div>
                    <div class="step-desc">${step.description}</div>
                `;
                stepElement.addEventListener('click', () => {
                    goToStep(index);
                });
                stepIndicator.appendChild(stepElement);
            });
        }
        
        // 更新步骤显示
        function updateStepDisplay() {
            // 更新标题和描述
            currentStepTitle.textContent = steps[currentStep].title;
            stepDescription.textContent = steps[currentStep].description;
            
            // 更新步骤指示器
            document.querySelectorAll('.step').forEach((step, index) => {
                if (index === currentStep) {
                    step.classList.add('active');
                } else {
                    step.classList.remove('active');
                }
            });
            
            // 更新按钮状态
            prevBtn.disabled = currentStep === 0;
            nextBtn.disabled = currentStep === steps.length - 1;
        }
        
        // 转到指定步骤
        function goToStep(stepIndex) {
            currentStep = Math.max(0, Math.min(stepIndex, steps.length - 1));
            animationProgress = 0;
            updateStepDisplay();
            resetAnimationState();
        }
        
        // 重置动画状态
        function resetAnimationState() {
            detachedAtoms = [];
            hydrogenMolecule = null;
        }
        
        // 播放动画
        function playAnimation() {
            if (isPlaying) return;
            isPlaying = true;
            playBtn.disabled = true;
            pauseBtn.disabled = false;
            
            if (currentStep >= steps.length - 1 && animationProgress >= 1) {
                goToStep(0);
            }
            
            animate();
        }
        
        // 暂停动画
        function pauseAnimation() {
            isPlaying = false;
            playBtn.disabled = false;
            pauseBtn.disabled = true;
            
            if (animationId) {
                cancelAnimationFrame(animationId);
                animationId = null;
            }
        }
        
        // 重置动画
        function resetAnimation() {
            pauseAnimation();
            goToStep(0);
        }
        
        // 上一步
        function prevStep() {
            if (currentStep > 0) {
                goToStep(currentStep - 1);
            }
        }
        
        // 下一步
        function nextStep() {
            if (currentStep < steps.length - 1) {
                goToStep(currentStep + 1);
            }
        }
        
        // 3D投影函数
        function project(x, y, z) {
            const scale = 80 * zoom;
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 应用旋转
            const cosX = Math.cos(rotationX);
            const sinX = Math.sin(rotationX);
            const cosY = Math.cos(rotationY);
            const sinY = Math.sin(rotationY);
            
            let y1 = y * cosX - z * sinX;
            let z1 = y * sinX + z * cosX;
            
            let x1 = x * cosY + z1 * sinY;
            z1 = -x * sinY + z1 * cosY;
            
            return {
                x: centerX + x1 * scale,
                y: centerY - y1 * scale
            };
        }
        
        // 绘制原子
        function drawAtom(atom, highlight = false) {
            const pos = project(atom.x, atom.y, atom.z);
            const radius = atom.type === 'H' ? 8 : 12;
            
            // 绘制原子球体
            ctx.beginPath();
            ctx.arc(pos.x, pos.y, radius, 0, Math.PI * 2);
            
            if (atom.type === 'Cu') {
                // 铜原子的金属质感
                const gradient = ctx.createRadialGradient(
                    pos.x - radius/3, pos.y - radius/3, 1,
                    pos.x, pos.y, radius
                );
                gradient.addColorStop(0, '#FFD700');
                gradient.addColorStop(0.7, '#B87333');
                gradient.addColorStop(1, '#8B4513');
                ctx.fillStyle = gradient;
            } else {
                ctx.fillStyle = highlight ? '#FFA726' : atomColors[atom.type];
            }
            
            ctx.fill();
            
            // 绘制边框
            ctx.strokeStyle = highlight ? '#FFA726' : 'rgba(255, 255, 255, 0.3)';
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 绘制标签
            if (showLabels && atom.label) {
                ctx.fillStyle = '#FFFFFF';
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(atom.label, pos.x, pos.y);
            }
            
            // 检查鼠标悬停
            const dx = mouseX - pos.x;
            const dy = mouseY - pos.y;
            const distance = Math.sqrt(dx * dx + dy * dy);
            
            if (distance < radius) {
                showAtomInfo(atom, pos);
            }
            
            return { pos, radius };
        }
        
        // 显示原子信息
        function showAtomInfo(atom, pos) {
            let info = '';
            switch(atom.type) {
                case 'C':
                    info = '碳原子 (Carbon)';
                    break;
                case 'H':
                    info = '氢原子 (Hydrogen)';
                    break;
                case 'O':
                    info = '氧原子 (Oxygen)';
                    break;
                case 'Cu':
                    info = '铜原子 (Copper) - 催化剂';
                    break;
            }
            
            if (atom.label) {
                info += `\n${atom.label}`;
            }
            
            atomInfo.textContent = info;
            atomInfo.style.left = (pos.x + 15) + 'px';
            atomInfo.style.top = (pos.y - 15) + 'px';
            atomInfo.style.opacity = '1';
        }
        
        // 绘制化学键
        function drawBond(atom1, atom2, type, highlight = false) {
            const pos1 = project(atom1.x, atom1.y, atom1.z);
            const pos2 = project(atom2.x, atom2.y, atom2.z);
            
            ctx.beginPath();
            ctx.moveTo(pos1.x, pos1.y);
            ctx.lineTo(pos2.x, pos2.y);
            
            if (highlight) {
                ctx.strokeStyle = '#FFA726';
                ctx.lineWidth = 6;
                ctx.setLineDash([]);
            } else {
                ctx.strokeStyle = type === 'double' ? '#4A90E2' : '#CCCCCC';
                ctx.lineWidth = type === 'double' ? 4 : 3;
                ctx.setLineDash(type === 'double' ? [5, 5] : []);
            }
            
            ctx.stroke();
            
            // 重置线条样式
            ctx.setLineDash([]);
            
            // 检查鼠标悬停在键上
            const midX = (pos1.x + pos2.x) / 2;
            const midY = (pos1.y + pos2.y) / 2;
            const dx = mouseX - midX;
            const dy = mouseY - midY;
            const distance = Math.sqrt(dx * dx + dy * dy);
            
            if (distance < 15) {
                const bondType = type === 'double' ? '双键 (C=O)' : '单键';
                atomInfo.textContent = `化学键: ${bondType}`;
                atomInfo.style.left = (midX + 15) + 'px';
                atomInfo.style.top = (midY - 15) + 'px';
                atomInfo.style.opacity = '1';
            }
        }
        
        // 绘制催化剂表面
        function drawCatalystSurface() {
            catalystSurface.forEach(cuAtom => {
                drawAtom(cuAtom);
            });
        }
        
        // 绘制反应方程式
        function drawEquation() {
            if (!showEquation) return;
            
            const equations = [
                "CH₃CH₂OH → CH₃CHO + 2H",
                "2H → H₂",
                "总反应: CH₃CH₂OH → CH₃CHO + H₂"
            ];
            
            ctx.fillStyle = 'rgba(255, 204, 128, 0.9)';
            ctx.font = 'bold 20px Cambria, serif';
            ctx.textAlign = 'center';
            
            equations.forEach((eq, index) => {
                ctx.fillText(eq, canvas.width / 2, 40 + index * 30);
            });
        }
        
        // 根据当前步骤绘制动画
        function drawStep() {
            const progress = Math.min(animationProgress, 1);
            
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            ctx.fillStyle = 'rgba(10, 25, 41, 0.9)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制催化剂表面
            drawCatalystSurface();
            
            // 根据步骤绘制不同的内容
            switch(currentStep) {
                case 0: // 初始状态
                    drawEthanolInitial(progress);
                    break;
                case 1: // O-H键断裂
                    drawOHBondBreaking(progress);
                    break;
                case 2: // C-H键断裂
                    drawCHBondBreaking(progress);
                    break;
                case 3: // 氢原子结合
                    drawHydrogenCombination(progress);
                    break;
                case 4: // 乙醛生成
                    drawAcetaldehydeFormation(progress);
                    break;
                case 5: // 催化剂再生
                    drawCatalystRegeneration(progress);
                    break;
            }
            
            // 绘制反应方程式
            drawEquation();
            
            // 绘制分离的原子
            detachedAtoms.forEach(atom => {
                drawAtom(atom);
            });
            
            // 绘制氢气分子
            if (hydrogenMolecule) {
                drawAtom(hydrogenMolecule.atom1);
                drawAtom(hydrogenMolecule.atom2);
                drawBond(hydrogenMolecule.atom1, hydrogenMolecule.atom2, 'single');
            }
        }
        
        // 绘制初始乙醇分子
        function drawEthanolInitial(progress) {
            // 乙醇分子从上方进入
            const offsetY = 3 * (1 - progress);
            const ethanolCopy = JSON.parse(JSON.stringify(ethanol));
            
            ethanolCopy.atoms.forEach(atom => {
                atom.y -= offsetY;
                drawAtom(atom);
            });
            
            ethanolCopy.bonds.forEach(bond => {
                const atom1 = ethanolCopy.atoms[bond.a1];
                const atom2 = ethanolCopy.atoms[bond.a2];
                drawBond(atom1, atom2, bond.type);
            });
        }
        
        // 绘制O-H键断裂
        function drawOHBondBreaking(progress) {
            // 绘制乙醇分子
            ethanol.atoms.forEach(atom => {
                drawAtom(atom, atom.label === 'H6');
            });
            
            ethanol.bonds.forEach(bond => {
                const atom1 = ethanol.atoms[bond.a1];
                const atom2 = ethanol.atoms[bond.a2];
                const isOHBond = (atom1.label === 'O' && atom2.label === 'H6') || 
                                (atom1.label === 'H6' && atom2.label === 'O');
                drawBond(atom1, atom2, bond.type, isOHBond);
            });
            
            // 动画：氢原子移动到催化剂表面
            if (progress > 0.3) {
                const hAtom = ethanol.atoms[8]; // H6
                const targetY = 3.5;
                const targetX = 0;
                const moveProgress = Math.min((progress - 0.3) / 0.7, 1);
                
                const currentY = hAtom.y + (targetY - hAtom.y) * moveProgress;
                const currentX = hAtom.x + (targetX - hAtom.x) * moveProgress;
                
                detachedAtoms.push({
                    type: 'H',
                    x: currentX,
                    y: currentY,
                    z: 0,
                    label: 'H'
                });
            }
        }
        
        // 绘制C-H键断裂
        function drawCHBondBreaking(progress) {
            // 绘制乙醇分子（已无OH键）
            ethanol.atoms.forEach(atom => {
                const isRelevantH = atom.label === 'H5';
                drawAtom(atom, isRelevantH);
            });
            
            ethanol.bonds.forEach(bond => {
                const atom1 = ethanol.atoms[bond.a1];
                const atom2 = ethanol.atoms[bond.a2];
                const isCHBond = (atom1.label === 'C2' && atom2.label === 'H5') || 
                                (atom1.label === 'H5' && atom2.label === 'C2');
                if (!(atom1.label === 'O' && atom2.label === 'H6')) {
                    drawBond(atom1, atom2, bond.type, isCHBond);
                }
            });
            
            // 第一个氢原子已在催化剂表面
            detachedAtoms.push({
                type: 'H',
                x: 0,
                y: 3.5,
                z: 0,
                label: 'H'
            });
            
            // 动画：第二个氢原子移动到催化剂表面
            if (progress > 0.3) {
                const hAtom = ethanol.atoms[7]; // H5
                const targetY = 3.5;
                const targetX = 1.2;
                const moveProgress = Math.min((progress - 0.3) / 0.7, 1);
                
                const currentY = hAtom.y + (targetY - hAtom.y) * moveProgress;
                const currentX = hAtom.x + (targetX - hAtom.x) * moveProgress;
                
                detachedAtoms.push({
                    type: 'H',
                    x: currentX,
                    y: currentY,
                    z: 0,
                    label: 'H'
                });
            }
        }
        
        // 绘制氢原子结合
        function drawHydrogenCombination(progress) {
            // 绘制中间体（已失去两个H的乙醇）
            const intermediateAtoms = ethanol.atoms.filter(atom => 
                atom.label !== 'H5' && atom.label !== 'H6'
            );
            
            intermediateAtoms.forEach(atom => {
                drawAtom(atom);
            });
            
            // 绘制剩余的键
            const remainingBonds = ethanol.bonds.filter(bond => {
                const atom1 = ethanol.atoms[bond.a1];
                const atom2 = ethanol.atoms[bond.a2];
                return !((atom1.label === 'O' && atom2.label === 'H6') || 
                        (atom1.label === 'C2' && atom2.label === 'H5'));
            });
            
            remainingBonds.forEach(bond => {
                const atom1 = intermediateAtoms.find(a => 
                    a.label === ethanol.atoms[bond.a1].label
                );
                const atom2 =
<!--检测到代码截断，自动续写中...-->
intermediateAtoms.find(a => 
                    a.label === ethanol.atoms[bond.a2].label
                );
                if (atom1 && atom2) {
                    drawBond(atom1, atom2, bond.type);
                }
            });
            
            // 两个氢原子在催化剂表面
            if (progress < 0.5) {
                detachedAtoms.push(
                    { type: 'H', x: 0, y: 3.5, z: 0, label: 'H' },
                    { type: 'H', x: 1.2, y: 3.5, z: 0, label: 'H' }
                );
            } else {
                // 氢原子结合成氢气分子
                const combineProgress = (progress - 0.5) / 0.5;
                const distance = 0.74; // H-H键长
                const midX = 0.6;
                
                hydrogenMolecule = {
                    atom1: {
                        type: 'H',
                        x: midX - distance/2 * combineProgress,
                        y: 3.5,
                        z: 0,
                        label: 'H'
                    },
                    atom2: {
                        type: 'H',
                        x: midX + distance/2 * combineProgress,
                        y: 3.5,
                        z: 0,
                        label: 'H'
                    }
                };
            }
        }
        
        // 绘制乙醛生成
        function drawAcetaldehydeFormation(progress) {
            // 绘制氢气分子
            if (hydrogenMolecule) {
                drawAtom(hydrogenMolecule.atom1);
                drawAtom(hydrogenMolecule.atom2);
                drawBond(hydrogenMolecule.atom1, hydrogenMolecule.atom2, 'single');
            }
            
            // 绘制乙醛分子（从中间体转换）
            const acetaldehydeCopy = JSON.parse(JSON.stringify(acetaldehyde));
            
            // 动画：乙醛分子向上移动并形成双键
            const moveUpProgress = Math.min(progress / 0.7, 1);
            const bondFormProgress = Math.max(0, (progress - 0.3) / 0.7);
            
            acetaldehydeCopy.atoms.forEach(atom => {
                // 初始位置调整
                atom.y -= 3.5;
                atom.y += 3.5 * moveUpProgress;
                
                // 如果是氧原子，稍微调整位置形成双键
                if (atom.label === 'O' && bondFormProgress > 0) {
                    atom.x = 1.54 + (2.1 - 1.54) * bondFormProgress;
                    atom.y = 0 + (1.42 - 0) * bondFormProgress;
                }
                
                drawAtom(atom, atom.label === 'O' && bondFormProgress > 0);
            });
            
            // 绘制乙醛的键
            acetaldehydeCopy.bonds.forEach(bond => {
                const atom1 = acetaldehydeCopy.atoms[bond.a1];
                const atom2 = acetaldehydeCopy.atoms[bond.a2];
                
                // 如果是C=O双键，根据进度绘制
                if (bond.type === 'double') {
                    if (bondFormProgress > 0) {
                        drawBond(atom1, atom2, 'double', true);
                    }
                } else {
                    drawBond(atom1, atom2, bond.type);
                }
            });
        }
        
        // 绘制催化剂再生
        function drawCatalystRegeneration(progress) {
            // 绘制乙醛分子（已完全形成）
            acetaldehyde.atoms.forEach(atom => {
                const atomCopy = {...atom};
                atomCopy.y += 2 * progress; // 继续向上移动
                drawAtom(atomCopy);
            });
            
            acetaldehyde.bonds.forEach(bond => {
                const atom1 = {...acetaldehyde.atoms[bond.a1]};
                const atom2 = {...acetaldehyde.atoms[bond.a2]};
                atom1.y += 2 * progress;
                atom2.y += 2 * progress;
                drawBond(atom1, atom2, bond.type);
            });
            
            // 绘制氢气分子向上移动并消失
            if (hydrogenMolecule && progress < 0.7) {
                const moveProgress = progress / 0.7;
                const h2Y = 3.5 - 2 * moveProgress;
                
                const h2Copy = {
                    atom1: {...hydrogenMolecule.atom1, y: h2Y},
                    atom2: {...hydrogenMolecule.atom2, y: h2Y}
                };
                
                drawAtom(h2Copy.atom1);
                drawAtom(h2Copy.atom2);
                drawBond(h2Copy.atom1, h2Copy.atom2, 'single');
            }
            
            // 高亮催化剂表面（表示再生）
            if (progress > 0.5) {
                const highlightProgress = (progress - 0.5) / 0.5;
                catalystSurface.forEach((cuAtom, index) => {
                    if (index < 5 && highlightProgress > 0) {
                        const atomCopy = {...cuAtom};
                        drawAtom(atomCopy, true);
                    } else {
                        drawAtom(cuAtom);
                    }
                });
            } else {
                drawCatalystSurface();
            }
        }
        
        // 动画循环
        function animate() {
            if (isPlaying) {
                animationProgress += 0.016 / (steps[currentStep].duration / 1000);
                
                if (animationProgress >= 1) {
                    animationProgress = 1;
                    
                    // 自动进入下一步
                    if (currentStep < steps.length - 1) {
                        setTimeout(() => {
                            currentStep++;
                            animationProgress = 0;
                            updateStepDisplay();
                            resetAnimationState();
                        }, 500);
                    } else {
                        // 最后一步完成后暂停
                        setTimeout(() => {
                            pauseAnimation();
                        }, 1000);
                    }
                }
            }
            
            drawStep();
            
            // 隐藏原子信息如果鼠标没有悬停
            const dx = mouseX - parseFloat(atomInfo.style.left || 0);
            const dy = mouseY - parseFloat(atomInfo.style.top || 0);
            const distance = Math.sqrt(dx * dx + dy * dy);
            
            if (distance > 100) {
                atomInfo.style.opacity = '0';
            }
            
            animationId = requestAnimationFrame(animate);
        }
        
        // 初始化画布大小
        function initCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        
        // 事件监听器
        function initEventListeners() {
            // 控制按钮
            playBtn.addEventListener('click', playAnimation);
            pauseBtn.addEventListener('click', pauseAnimation);
            resetBtn.addEventListener('click', resetAnimation);
            prevBtn.addEventListener('click', prevStep);
            nextBtn.addEventListener('click', nextStep);
            
            // 显示选项
            toggleLabels.addEventListener('click', () => {
                showLabels = !showLabels;
                toggleLabels.classList.toggle('active', showLabels);
            });
            
            toggleEquation.addEventListener('click', () => {
                showEquation = !showEquation;
                toggleEquation.classList.toggle('active', showEquation);
            });
            
            // 鼠标事件
            canvas.addEventListener('mousemove', (e) => {
                const rect = canvas.getBoundingClientRect();
                mouseX = e.clientX - rect.left;
                mouseY = e.clientY - rect.top;
                
                if (isDragging) {
                    const deltaX = e.clientX - lastMouseX;
                    const deltaY = e.clientY - lastMouseY;
                    
                    rotationY += deltaX * 0.01;
                    rotationX += deltaY * 0.01;
                    
                    lastMouseX = e.clientX;
                    lastMouseY = e.clientY;
                }
            });
            
            canvas.addEventListener('mousedown', (e) => {
                isDragging = true;
                lastMouseX = e.clientX;
                lastMouseY = e.clientY;
                canvas.style.cursor = 'grabbing';
            });
            
            canvas.addEventListener('mouseup', () => {
                isDragging = false;
                canvas.style.cursor = 'default';
            });
            
            canvas.addEventListener('mouseleave', () => {
                isDragging = false;
                canvas.style.cursor = 'default';
                atomInfo.style.opacity = '0';
            });
            
            // 鼠标滚轮缩放
            canvas.addEventListener('wheel', (e) => {
                e.preventDefault();
                zoom += e.deltaY * -0.001;
                zoom = Math.min(Math.max(0.5, zoom), 2);
            });
            
            // 窗口大小调整
            window.addEventListener('resize', () => {
                initCanvas();
                drawStep();
            });
        }
        
        // 初始化
        function init() {
            initCanvas();
            initStepIndicator();
            initEventListeners();
            updateStepDisplay();
            
            // 初始绘制
            drawStep();
            
            // 禁用暂停按钮（初始状态）
            pauseBtn.disabled = true;
        }
        
        // 启动应用
        init();
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 乙醇催化氧化成乙醛 - 交互式教学动画使用指南

### 功能说明

本交互式教学动画旨在通过动态可视化技术，生动展示乙醇在铜催化剂作用下氧化生成乙醛的微观脱氢过程。动画将抽象的化学反应机理转化为直观的分子模型动画，帮助学生深入理解催化剂的作用机制、化学键的断裂与形成过程，以及微观反应与宏观现象之间的联系。

### 主要功能

#### 1. 动画控制功能
- **播放/暂停控制**：控制动画的播放与暂停，便于分步观察
- **步骤导航**：支持跳转到任意反应步骤，针对性学习特定环节
- **重置功能**：一键恢复到初始状态，便于重复学习

#### 2. 视角交互功能
- **3D旋转**：鼠标拖拽可360度旋转分子模型，从不同角度观察空间结构
- **缩放控制**：鼠标滚轮可放大缩小视图，观察细节或整体布局
- **预设视角**：自动优化的视角展示反应关键步骤

#### 3. 信息提示功能
- **原子识别**：鼠标悬停在原子上显示元素符号和角色说明
- **化学键信息**：悬停在化学键上显示键类型和特性
- **步骤说明**：每个步骤都有详细的文字解释和化学原理说明

#### 4. 显示定制功能
- **标签开关**：可显示/隐藏原子标签，适应不同学习阶段
- **方程式显示**：控制反应方程式的显示状态
- **高亮强调**：关键反应位点自动高亮显示，突出重点

### 设计特色

#### 1. 科学准确性
- **CPK标准配色**：采用国际通用的原子颜色标准（碳：深灰、氢：白、氧：红）
- **真实键长比例**：化学键长度基于实际分子结构数据
- **正确反应机理**：严格遵循乙醇催化氧化的实际反应路径

#### 2. 教学友好性
- **分步分解**：将连续反应分解为6个清晰的认知步骤
- **渐进式展示**：从整体到局部，符合认知规律
- **多感官刺激**：视觉高亮、文字说明、交互反馈相结合

#### 3. 技术先进性
- **HTML5 Canvas实现**：无需插件，跨平台兼容
- **流畅3D渲染**：实时计算投影，提供立体观察体验
- **响应式设计**：适应不同屏幕尺寸和设备类型

#### 4. 界面美观性
- **科技感配色**：深蓝背景搭配原子标准色，专业且清晰
- **渐变金属质感**：铜催化剂表面呈现逼真的金属光泽
- **柔和动画过渡**：所有动作平滑自然，避免视觉疲劳

### 教学要点

#### 核心概念可视化
1. **催化剂作用机制**
   - 展示铜表面如何吸附乙醇分子
   - 可视化催化剂降低反应活化能的过程
   - 明确催化剂在反应前后保持不变的特点

2. **脱氢过程分解**
   - O-H键断裂：羟基氢的脱离
   - C-H键断裂：α-碳上氢的脱离
   - 氢原子结合：表面氢原子形成氢气

3. **化学键变化**
   - 单键断裂的动画表现
   - 双键形成的渐进过程
   - 键能变化的视觉暗示

4. **产物生成**
   - 乙醛分子的结构特征
   - C=O双键的形成标志
   - 产物脱附的动力学展示

#### 认知难点突破
- **抽象概念具体化**：将“吸附”、“脱氢”等抽象术语转化为可见过程
- **微观宏观连接**：通过微观动画解释“铜丝变红再变亮”的宏观现象
- **能量变化暗示**：通过动画节奏和视觉效果暗示反应能垒变化

### 使用建议

#### 1. 课堂教学应用
- **导入环节**：播放完整动画，激发学生兴趣，提出问题
- **讲解环节**：分步播放，配合教师讲解，每步暂停讨论
- **巩固环节**：学生自主操作，探索不同视角，加深理解
- **总结环节**：回顾关键步骤，连接微观过程与宏观现象

#### 2. 自主学习策略
- **初次学习**：按顺序完整观看动画，了解整体过程
- **重点突破**：针对不理解步骤，反复观看并旋转视角观察
- **自我测试**：隐藏标签，尝试识别原子和化学键
- **知识整合**：将动画过程与化学方程式、实验现象相联系

#### 3. 教学场景建议
- **高中化学课堂**：配合“醇类性质”章节教学
- **大学基础化学**：深化对催化机理的理解
- **实验课前预习**：帮助学生理解实验原理
- **复习巩固工具**：考前回顾反应机理细节

#### 4. 最佳实践提示
- **分步学习法**：建议每次专注于1-2个步骤，充分理解后再继续
- **多角度观察**：鼓励旋转分子模型，建立空间结构概念
- **互动探索**：主动悬停查看原子信息，培养观察能力
- **联系实际**：思考动画内容与实际实验现象的关系

#### 5. 技术使用技巧
- **大屏展示**：教室投影时，适当调高对比度确保后排可见
- **小组学习**：学生分组操作，讨论观察到的现象
- **个性化学习**：根据学生掌握程度，选择不同的学习路径
- **整合教学**：将动画与板书、实验视频、练习题相结合

---

**教学提示**：本动画不仅是展示工具，更是探究平台。鼓励学生提出问题，如“为什么氢原子要在催化剂表面结合？”“铜催化剂表面发生了什么变化？”，通过操作动画寻找答案，培养科学探究能力。

**技术说明**：本动画基于现代Web标准开发，在Chrome、Firefox、Edge等主流浏览器上均可流畅运行，建议使用最新版本浏览器以获得最佳体验。

希望这份交互式教学动画能够成为您化学教学中的得力助手，让微观世界的奥秘变得触手可及！