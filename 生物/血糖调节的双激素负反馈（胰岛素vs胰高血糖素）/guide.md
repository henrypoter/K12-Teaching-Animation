# 需求：血糖调节的双激素负反馈（胰岛素vs胰高血糖素）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要是高中或大学低年级的生物学、生理学或医学预科学生。他们需要：
1.  **理解核心机制**：清晰掌握胰岛素和胰高血糖素如何通过负反馈调节血糖浓度，这是内分泌系统的核心难点。
2.  **可视化动态过程**：将抽象的文字描述（如“血糖升高→胰岛素分泌→血糖降低”）转化为直观、动态的视觉流程。
3.  **区分激素功能**：明确两种激素的来源、靶器官和作用截然相反，但共同构成一个平衡系统。
4.  **建立反馈循环概念**：深刻理解“负反馈”如何维持内环境稳态，并能应用于其他类似系统（如体温调节）。
5.  **主动探索与验证**：通过交互操作，主动改变变量（如进食、运动），观察系统如何响应，从而巩固知识。

#### 教学设计思路
*   **核心概念**：聚焦于“血糖浓度”作为被调节变量，以及“胰岛素”（降糖）和“胰高血糖素”（升糖）作为一对拮抗调节因子。强调“负反馈”即“结果反过来抑制或促进原因”的逻辑。
*   **认知规律**：
    *   **从整体到局部**：先展示完整的身体轮廓和血糖变化曲线，建立宏观印象，再聚焦到胰腺和肝脏的微观作用。
    *   **从静态到动态**：先呈现初始平衡状态，再通过触发事件（如“吃糖”）打破平衡，展示系统的动态调节过程，最后回归新平衡。
    *   **从观察到操作**：用户先观看自动演示，理解流程后，再通过交互控件主动干预，进行探究式学习。
*   **交互设计**：
    *   **叙事驱动**：设计一个清晰的“故事线”：平衡 → 扰动（事件）→ 激素响应 → 效应器作用 → 恢复平衡。
    *   **分层控制**：提供“播放/暂停/重置”控制整体动画；提供“事件按钮”（如“进食”、“运动”、“注射胰岛素”）让用户施加扰动；可能提供“隐藏/显示”选项（如隐藏激素名称，用于自我测验）。
    *   **即时反馈**：所有用户操作（点击按钮）都会立即在动画和数据上得到视觉和数值反馈。
*   **视觉呈现**：
    *   **主体隐喻**：将人体简化为一个清晰的轮廓，重点突出**胰腺**、**肝脏**、**血液**（用流动的点和血管表示）和**肌肉/脂肪细胞**。
    *   **激素拟人化/符号化**：用两种鲜明、对立的图标表示胰岛素（例如，一把蓝色的“钥匙”或向下的箭头）和胰高血糖素（例如，一把橙色的“火炬”或向上的箭头）。它们从胰腺出发，沿血管移动到靶器官。
    *   **数据可视化**：在画面一侧同步绘制实时变化的“血糖浓度-时间曲线图”，将抽象概念量化。
    *   **状态高亮**：当血糖过高或过低时，背景色或警示灯会有轻微变化。靶器官被激素作用时，会高亮显示。

#### 配色方案选择
选择清晰、科学且符合认知习惯的配色，避免花哨：
*   **背景与人体**：浅灰色或极浅的米色背景。人体轮廓用柔和的深灰色细线勾勒。
*   **血糖/葡萄糖分子**：使用温暖的**亮黄色**圆点表示，高浓度时密集，低浓度时稀疏，直观易懂。
*   **胰岛素**：采用冷静、抑制性的**蓝色系**（如#3498db）。代表“降低”、“储存”、“平静”。
*   **胰高血糖素**：采用活跃、警示性的**橙色系**（如#e67e22）。代表“升高”、“释放”、“动员”。
*   **肝脏与细胞**：肝脏用**深红色**，肌肉细胞用**浅紫色**，脂肪细胞用**浅黄色**，区分不同组织。
*   **血管**：淡红色细线。
*   **曲线图**：血糖曲线用**黑色**实线。可添加淡蓝色和淡橙色区域阴影，分别表示胰岛素和胰高血糖素活跃期。
*   **交互按钮**：使用中性色（如浅灰色），在悬停和激活时有颜色变化反馈。

#### 交互功能列表
1.  **核心控制面板**：
    *   “播放/暂停”：控制预设动画的播放。
    *   “重置”：将动画恢复到初始平衡状态。
2.  **扰动事件按钮**（用户主动操作）：
    *   “吃一块糖”（或“进食”）：快速增加血液中的葡萄糖（黄点）。
    *   “剧烈运动”：模拟肌肉大量消耗葡萄糖。
    *   “跳过一餐”（或“禁食”）：缓慢减少葡萄糖来源。
    *   （进阶）“注射胰岛素”：直接外源性增加胰岛素。
    *   （进阶）“应激状态”：模拟肾上腺素等的影响。
3.  **可视化选项**（可选）：
    *   “显示/隐藏激素标签”：用于自我测验。
    *   “显示/隐藏葡萄糖流动”：简化或复杂化视图。
    *   “曲线图开关”：专注于器官动画或数据变化。
4.  **信息提示**：
    *   鼠标悬停在关键元素（胰腺、肝脏、激素、细胞）上时，显示名称和简要功能说明。
    *   在动画关键步骤（如胰岛素分泌高峰）出现简短的文字解说气泡。
5.  **状态指示器**：
    *   一个显眼的数字或仪表盘，实时显示当前“血糖浓度”（例如，单位：mmol/L）。
    *   通过颜色（绿→黄→红）或表情符号表示血糖水平是否处于正常范围。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>血糖调节的双激素负反馈 | 胰岛素 vs 胰高血糖素</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
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
            border-bottom: 2px solid #eaeaea;
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
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 25px;
        }
        
        .animation-panel {
            flex: 3;
            min-width: 300px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            position: relative;
            overflow: hidden;
        }
        
        .controls-panel {
            flex: 2;
            min-width: 300px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .panel-title {
            font-size: 1.3rem;
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #eee;
        }
        
        #animationCanvas {
            width: 100%;
            height: 500px;
            background-color: #fefefe;
            border-radius: 8px;
            display: block;
        }
        
        .control-section {
            margin-bottom: 10px;
        }
        
        .control-section h3 {
            font-size: 1.1rem;
            margin-bottom: 12px;
            color: #34495e;
        }
        
        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .btn {
            padding: 10px 16px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s ease;
            flex: 1;
            min-width: 120px;
        }
        
        .btn-primary {
            background-color: #3498db;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #2980b9;
        }
        
        .btn-event {
            background-color: #f8f9fa;
            border: 2px solid #e0e0e0;
            color: #444;
        }
        
        .btn-event:hover {
            background-color: #e9ecef;
            border-color: #3498db;
        }
        
        .btn-eat {
            border-color: #f1c40f;
        }
        
        .btn-exercise {
            border-color: #9b59b6;
        }
        
        .btn-fasting {
            border-color: #e67e22;
        }
        
        .btn-insulin {
            border-color: #3498db;
        }
        
        .btn-stress {
            border-color: #e74c3c;
        }
        
        .status-display {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            margin-top: 10px;
        }
        
        .blood-sugar-display {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        
        .blood-sugar-value {
            font-size: 1.8rem;
            font-weight: bold;
            color: #2c3e50;
        }
        
        .blood-sugar-status {
            padding: 5px 12px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 0.9rem;
        }
        
        .status-normal {
            background-color: #d5f4e6;
            color: #27ae60;
        }
        
        .status-high {
            background-color: #fdebd0;
            color: #e67e22;
        }
        
        .status-low {
            background-color: #fadbd8;
            color: #e74c3c;
        }
        
        .hormone-levels {
            display: flex;
            justify-content: space-between;
            margin-top: 15px;
        }
        
        .hormone-level {
            text-align: center;
            flex: 1;
        }
        
        .hormone-name {
            font-size: 0.9rem;
            margin-bottom: 5px;
            font-weight: 600;
        }
        
        .insulin-name {
            color: #3498db;
        }
        
        .glucagon-name {
            color: #e67e22;
        }
        
        .hormone-bar {
            height: 10px;
            border-radius: 5px;
            background-color: #ecf0f1;
            overflow: hidden;
            margin-bottom: 5px;
        }
        
        .hormone-fill {
            height: 100%;
            width: 50%;
            border-radius: 5px;
            transition: width 0.5s ease;
        }
        
        .insulin-fill {
            background-color: #3498db;
        }
        
        .glucagon-fill {
            background-color: #e67e22;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid #eee;
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
        }
        
        .legend-glucose {
            background-color: #f1c40f;
        }
        
        .legend-insulin {
            background-color: #3498db;
        }
        
        .legend-glucagon {
            background-color: #e67e22;
        }
        
        .legend-liver {
            background-color: #c0392b;
        }
        
        .legend-cell {
            background-color: #9b59b6;
        }
        
        .explanation {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            margin-top: 20px;
        }
        
        .explanation h2 {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.5rem;
        }
        
        .explanation p {
            margin-bottom: 15px;
        }
        
        .key-concept {
            background-color: #f8f9fa;
            padding: 15px;
            border-left: 4px solid #3498db;
            margin: 15px 0;
            border-radius: 0 8px 8px 0;
        }
        
        .feedback-loop {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 20px 0;
            padding: 15px;
            background-color: #f0f7ff;
            border-radius: 8px;
            flex-wrap: wrap;
        }
        
        .feedback-step {
            text-align: center;
            flex: 1;
            min-width: 150px;
            padding: 10px;
        }
        
        .step-number {
            display: inline-block;
            width: 30px;
            height: 30px;
            background-color: #3498db;
            color: white;
            border-radius: 50%;
            line-height: 30px;
            margin-bottom: 10px;
            font-weight: bold;
        }
        
        .step-arrow {
            font-size: 1.5rem;
            color: #7f8c8d;
            padding: 0 10px;
        }
        
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .feedback-loop {
                flex-direction: column;
            }
            
            .step-arrow {
                transform: rotate(90deg);
                padding: 10px 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>血糖调节的双激素负反馈</h1>
        <p class="subtitle">胰岛素 vs 胰高血糖素 | 可视化交互教学动画</p>
    </header>
    
    <div class="container">
        <div class="animation-panel">
            <h2 class="panel-title">血糖调节动画</h2>
            <canvas id="animationCanvas" width="800" height="500"></canvas>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color legend-glucose"></div>
                    <span>葡萄糖分子</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color legend-insulin"></div>
                    <span>胰岛素（降血糖）</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color legend-glucagon"></div>
                    <span>胰高血糖素（升血糖）</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color legend-liver"></div>
                    <span>肝脏</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color legend-cell"></div>
                    <span>肌肉/脂肪细胞</span>
                </div>
            </div>
        </div>
        
        <div class="controls-panel">
            <div class="control-section">
                <h3>动画控制</h3>
                <div class="button-group">
                    <button id="playBtn" class="btn btn-primary">播放</button>
                    <button id="pauseBtn" class="btn btn-primary">暂停</button>
                    <button id="resetBtn" class="btn btn-primary">重置</button>
                </div>
            </div>
            
            <div class="control-section">
                <h3>模拟事件</h3>
                <div class="button-group">
                    <button id="eatBtn" class="btn btn-event btn-eat">吃一块糖</button>
                    <button id="exerciseBtn" class="btn btn-event btn-exercise">剧烈运动</button>
                    <button id="fastingBtn" class="btn btn-event btn-fasting">跳过一餐</button>
                </div>
                <div class="button-group">
                    <button id="insulinBtn" class="btn btn-event btn-insulin">注射胰岛素</button>
                    <button id="stressBtn" class="btn btn-event btn-stress">应激状态</button>
                </div>
            </div>
            
            <div class="control-section">
                <h3>当前状态</h3>
                <div class="status-display">
                    <div class="blood-sugar-display">
                        <div>
                            <div style="font-size: 0.9rem; color: #7f8c8d;">血糖浓度</div>
                            <div id="bloodSugarValue" class="blood-sugar-value">5.0 mmol/L</div>
                        </div>
                        <div id="bloodSugarStatus" class="blood-sugar-status status-normal">正常</div>
                    </div>
                    
                    <div class="hormone-levels">
                        <div class="hormone-level">
                            <div class="hormone-name insulin-name">胰岛素水平</div>
                            <div class="hormone-bar">
                                <div id="insulinBar" class="hormone-fill insulin-fill" style="width: 50%;"></div>
                            </div>
                            <div id="insulinLevel" style="font-size: 0.9rem;">中等</div>
                        </div>
                        
                        <div class="hormone-level">
                            <div class="hormone-name glucagon-name">胰高血糖素水平</div>
                            <div class="hormone-bar">
                                <div id="glucagonBar" class="hormone-fill glucagon-fill" style="width: 50%;"></div>
                            </div>
                            <div id="glucagonLevel" style="font-size: 0.9rem;">中等</div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="control-section">
                <h3>可视化选项</h3>
                <div class="button-group">
                    <button id="toggleLabelsBtn" class="btn btn-event">显示/隐藏标签</button>
                    <button id="toggleGlucoseBtn" class="btn btn-event">显示/隐藏葡萄糖</button>
                </div>
            </div>
        </div>
    </div>
    
    <div class="explanation">
        <h2>血糖调节机制说明</h2>
        
        <p>血糖调节是人体维持内环境稳态的重要机制，主要通过胰腺分泌的两种激素——<strong>胰岛素</strong>和<strong>胰高血糖素</strong>——的拮抗作用来实现。</p>
        
        <div class="key-concept">
            <strong>核心概念：负反馈调节</strong> - 当血糖浓度偏离正常范围时，身体会通过分泌相应的激素来对抗这种变化，使血糖浓度回归正常水平。
        </div>
        
        <div class="feedback-loop">
            <div class="feedback-step">
                <div class="step-number">1</div>
                <div>血糖升高</div>
            </div>
            <div class="step-arrow">→</div>
            <div class="feedback-step">
                <div class="step-number">2</div>
                <div>胰岛素分泌增加</div>
            </div>
            <div class="step-arrow">→</div>
            <div class="feedback-step">
                <div class="step-number">3</div>
                <div>血糖降低</div>
            </div>
            <div class="step-arrow">→</div>
            <div class="feedback-step">
                <div class="step-number">4</div>
                <div>胰岛素分泌减少</div>
            </div>
        </div>
        
        <div class="feedback-loop">
            <div class="feedback-step">
                <div class="step-number">1</div>
                <div>血糖降低</div>
            </div>
            <div class="step-arrow">→</div>
            <div class="feedback-step">
                <div class="step-number">2</div>
                <div>胰高血糖素分泌增加</div>
            </div>
            <div class="step-arrow">→</div>
            <div class="feedback-step">
                <div class="step-number">3</div>
                <div>血糖升高</div>
            </div>
            <div class="step-arrow">→</div>
            <div class="feedback-step">
                <div class="step-number">4</div>
                <div>胰高血糖素分泌减少</div>
            </div>
        </div>
        
        <p><strong>胰岛素</strong>（蓝色）由胰腺β细胞分泌，主要作用是降低血糖：促进葡萄糖进入肌肉和脂肪细胞储存，抑制肝脏释放葡萄糖。</p>
        <p><strong>胰高血糖素</strong>（橙色）由胰腺α细胞分泌，主要作用是升高血糖：促进肝脏分解糖原释放葡萄糖，促进脂肪分解。</p>
        <p>这两种激素通过负反馈机制相互拮抗，共同维持血糖浓度在正常范围内（约3.9-6.1 mmol/L）。</p>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 状态变量
        let animationId = null;
        let isPlaying = false;
        let showLabels = true;
        let showGlucose = true;
        
        // 血糖系统状态
        let bloodSugar = 5.0; // 单位：mmol/L
        let insulinLevel = 50; // 百分比
        let glucagonLevel = 50; // 百分比
        
        // 动画时间
        let animationTime = 0;
        
        // 事件效果
        let activeEvent = null;
        let eventStartTime = 0;
        let eventDuration = 0;
        
        // 葡萄糖粒子
        let glucoseParticles = [];
        let insulinParticles = [];
        let glucagonParticles = [];
        
        // 身体器官位置
        const body = {
            x: canvas.width * 0.5,
            y: canvas.height * 0.5,
            width: canvas.width * 0.6,
            height: canvas.height * 0.7
        };
        
        const pancreas = {
            x: body.x - body.width * 0.15,
            y: body.y - body.height * 0.1,
            width: 40,
            height: 25
        };
        
        const liver = {
            x: body.x + body.width * 0.1,
            y: body.y - body.height * 0.05,
            width: 80,
            height: 60
        };
        
        const muscleCells = {
            x: body.x - body.width * 0.2,
            y: body.y + body.height * 0.2,
            width: 70,
            height: 50
        };
        
        const fatCells = {
            x: body.x + body.width * 0.15,
            y: body.y + body.height * 0.25,
            width: 70,
            height: 50
        };
        
        // 初始化葡萄糖粒子
        function initGlucoseParticles() {
            glucoseParticles = [];
            const particleCount = Math.floor(bloodSugar * 10); // 粒子数量与血糖浓度相关
            
            for (let i = 0; i < particleCount; i++) {
                glucoseParticles.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    size: Math.random() * 4 + 2,
                    speedX: (Math.random() - 0.5) * 1.5,
                    speedY: (Math.random() - 0.5) * 1.5,
                    alpha: Math.random() * 0.5 + 0.5
                });
            }
        }
        
        // 初始化激素粒子
        function initHormoneParticles() {
            insulinParticles = [];
            glucagonParticles = [];
            
            // 根据激素水平创建粒子
            const insulinCount = Math.floor(insulinLevel / 10);
            const glucagonCount = Math.floor(glucagonLevel / 10);
            
            for (let i = 0; i < insulinCount; i++) {
                insulinParticles.push({
                    x: pancreas.x + Math.random() * pancreas.width,
                    y: pancreas.y + Math.random() * pancreas.height,
                    targetX: muscleCells.x + Math.random() * muscleCells.width,
                    targetY: muscleCells.y + Math.random() * muscleCells.height,
                    progress: Math.random(),
                    size: 6
                });
            }
            
            for (let i = 0; i < glucagonCount; i++) {
                glucagonParticles.push({
                    x: pancreas.x + Math.random() * pancreas.width,
                    y: pancreas.y + Math.random() * pancreas.height,
                    targetX: liver.x + Math.random() * liver.width,
                    targetY: liver.y + Math.random() * liver.height,
                    progress: Math.random(),
                    size: 6
                });
            }
        }
        
        // 绘制身体轮廓
        function drawBody() {
            ctx.save();
            
            // 身体轮廓
            ctx.strokeStyle = '#bdc3c7';
            ctx.lineWidth = 2;
            ctx.setLineDash([]);
            ctx.strokeRect(
                body.x - body.width/2, 
                body.y - body.height/2, 
                body.width, 
                body.height
            );
            
            // 胰腺
            ctx.fillStyle = '#95a5a6';
            ctx.fillRect(pancreas.x - pancreas.width/2, pancreas.y - pancreas.height/2, pancreas.width, pancreas.height);
            ctx.strokeStyle = '#7f8c8d';
            ctx.strokeRect(pancreas.x - pancreas.width/2, pancreas.y - pancreas.height/2, pancreas.width, pancreas.height);
            
            if (showLabels) {
                ctx.fillStyle = '#2c3e50';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('胰腺', pancreas.x, pancreas.y + pancreas.height/2 + 20);
                
                // 标注α和β细胞
                ctx.font = '12px Arial';
                ctx.fillStyle = '#e67e22';
                ctx.fillText('α细胞', pancreas.x - 10, pancreas.y - 10);
                ctx.fillStyle = '#3498db';
                ctx.fillText('β细胞', pancreas.x + 10, pancreas.y + 5);
            }
            
            // 肝脏
            ctx.fillStyle = '#c0392b';
            ctx.beginPath();
            ctx.roundRect(liver.x - liver.width/2, liver.y - liver.height/2, liver.width, liver.height, 10);
            ctx.fill();
            ctx.strokeStyle = '#a93226';
            ctx.stroke();
            
            if (showLabels) {
                ctx.fillStyle = '#2c3e50';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('肝脏', liver.x, liver.y + liver.height/2 + 20);
            }
            
            // 肌肉细胞
            ctx.fillStyle = '#9b59b6';
            ctx.beginPath();
            ctx.ellipse(muscleCells.x, muscleCells.y, muscleCells.width/2, muscleCells.height/2, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#8e44ad';
            ctx.stroke();
            
            if (showLabels) {
                ctx.fillStyle = '#2c3e50';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('肌肉细胞', muscleCells.x, muscleCells.y + muscleCells.height/2 + 20);
            }
            
            // 脂肪细胞
            ctx.fillStyle = '#f1c40f';
            ctx.beginPath();
            ctx.ellipse(fatCells.x, fatCells.y, fatCells.width/2, fatCells.height/2, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#f39c12';
            ctx.stroke();
            
            if (showLabels) {
                ctx.fillStyle = '#2c3e50';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('脂肪细胞', fatCells.x, fatCells.y + fatCells.height/2 + 20);
            }
            
            // 血管示意
            ctx.strokeStyle = '#e74c3c';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            
            // 从胰腺到肝脏
            ctx.beginPath();
            ctx.moveTo(pancreas.x + pancreas.width/2, pancreas.y);
            ctx.lineTo(liver.x - liver.width/2, liver.y);
            ctx.stroke();
            
            // 从胰腺到肌肉细胞
            ctx.beginPath();
            ctx.moveTo(pancreas.x + pancreas.width/2, pancreas.y);
            ctx.lineTo(muscleCells.x - muscleCells.width/2, muscleCells.y);
            ctx.stroke();
            
            // 从胰腺到脂肪细胞
            ctx.beginPath();
            ctx.moveTo(pancreas.x + pancreas.width/2, pancreas.y);
            ctx.lineTo(fatCells.x - fatCells.width/2, fatCells.y);
            ctx.stroke();
            
            // 从肝脏到身体循环
            ctx.beginPath();
            ctx.moveTo(liver.x + liver.width/2, liver.y);
            ctx.lineTo(body.x + body.width/2 - 20, body.y);
            ctx.stroke();
            
            ctx.restore();
        }
        
        // 绘制葡萄糖粒子
        function drawGlucoseParticles() {
            if (!showGlucose) return;
            
            ctx.save();
            
            for (const particle of glucoseParticles) {
                // 更新位置
                particle.x += particle.speedX;
                particle.y += particle.speedY;
                
                // 边界检查
                if (particle.x < 0 || particle.x > canvas.width) particle.speedX *= -1;
                if (particle.y < 0 || particle.y > canvas.height) particle.speedY *= -1;
                
                // 确保粒子在身体内
                const inBody = (
                    particle.x > body.x - body.width/2 && 
                    particle.x < body.x + body.width/2 &&
                    particle.y > body.y - body.height/2 && 
                    particle.y < body.y + body.height/2
                );
                
                if (!inBody) {
                    // 将粒子移回身体内
                    particle.x = Math.max(body.x - body.width/2 + 10, Math.min(particle.x, body.x + body.width/2 - 10));
                    particle.y = Math.max(body.y - body.height/2 + 10, Math.min(particle.y, body.y + body.height/2 - 10));
                }
                
                // 绘制粒子
                ctx.globalAlpha = particle.alpha;
                ctx.fillStyle = '#f1c40f';
                ctx.beginPath();
                ctx.arc(particle.x, particle.y, particle.size, 0, Math.PI * 2);
                ctx.fill();
            }
            
            ctx.restore();
        }
        
        // 绘制激素粒子
        function drawHormoneParticles() {
            ctx.save();
            
            // 绘制胰岛素粒子（蓝色）
            for (const particle of insulinParticles) {
                particle.progress += 0.01;
                if (particle.progress > 1) particle.progress = 0;
                
                const x = particle.x + (particle.targetX - particle.x) * particle.progress;
                const y = particle.y + (particle.targetY - particle.y) * particle.progress;
                
                // 绘制胰岛素分子（钥匙形状）
                ctx.fillStyle = '#3498db';
                ctx.beginPath();
                ctx.arc(x, y, particle.size, 0, Math.PI * 2);
                ctx.fill();
                
                // 钥匙齿
                ctx.fillStyle = '#2980b9';
                ctx.fillRect(x - particle.size/2, y - particle.size, particle.size, particle.size/2);
            }
            
            // 绘制胰高血糖素粒子（橙色）
            for (const particle of glucagonParticles) {
                particle.progress += 0.01;
                if (particle.progress > 1) particle.progress = 0;
                
                const x = particle.x + (particle.targetX - particle.x) * particle.progress;
                const y = particle.y + (particle.targetY - particle.y) * particle.progress;
                
                // 绘制胰高血糖素分子（火焰形状）
                ctx.fillStyle = '#e67e22';
                ctx.beginPath();
                ctx.moveTo(x, y - particle.size);
                ctx.lineTo(x - particle.size, y + particle.size);
                ctx.lineTo(x + particle.size, y + particle.size);
                ctx.closePath();
                ctx.fill();
            }
            
            ctx.restore();
        }
        
        // 绘制事件效果
        function drawEventEffects() {
            if (!activeEvent) return;
            
            ctx.save();
            ctx.globalAlpha = 0.3;
            
            const elapsed = animationTime - eventStartTime;
            const progress = Math.min(elapsed / eventDuration, 1);
            
            switch(activeEvent) {
                case 'eat':
                    // 吃糖效果：黄色闪光
                    ctx.fillStyle = '#f1c40f';
                    ctx.fillRect(0, 0, canvas.width, canvas.height * progress);
                    break;
                    
                case 'exercise':
                    // 运动效果：紫色脉动
                    const pulseSize = Math.sin(animationTime * 0.1) * 10;
                    ctx.strokeStyle = '#9b59b6';
                    ctx.lineWidth = 3;
                    ctx.setLineDash([]);
                    ctx.strokeRect(
                        muscleCells.x - muscleCells.width/2 - pulseSize, 
                        muscleCells.y - muscleCells.height/2 - pulseSize, 
                        muscleCells.width + pulseSize*2, 
                        muscleCells.height + pulseSize*2
                    );
                    break;
                    
                case 'fasting':
                    // 禁食效果：暗色覆盖
                    ctx.fillStyle = '#34495e';
                    ctx.globalAlpha = 0.2;
                    ctx.fillRect(0, 0, canvas.width, canvas.height);
                    break;
                    
                case 'insulin':
                    // 注射胰岛素效果：蓝色注射器
                    ctx.fillStyle = '#3498db';
                    ctx.fillRect(canvas.width - 50, 50, 20, 40);
                    ctx.fillRect(canvas.width - 55, 45, 30, 10);
                    break;
                    
                case 'stress':
                    // 应激效果：红色警示
                    ctx.strokeStyle = '#e74c3c';
                    ctx.lineWidth = 4;
                    ctx.setLineDash([10, 5]);
                    ctx.strokeRect(20, 20, canvas.width - 40, canvas.height - 40);
                    break;
            }
            
            ctx.restore();
            
            // 如果事件结束，清除活动事件
            if (progress >= 1) {
                activeEvent = null;
            }
        }
        
        // 更新系统状态
        function updateSystem() {
            // 基础代谢：缓慢消耗葡萄糖
            bloodSugar -= 0.001;
            
            // 激素对血糖的影响
            bloodSugar -= (insulinLevel - 50) * 0.0005;
            bloodSugar += (glucagonLevel - 50) * 0.0005;
            
            // 激素调节：负反馈机制
            if (bloodSugar > 5.5) {
                // 血糖偏高，增加胰岛素，减少胰高血糖素
                insulinLevel = Math.min(100, insulinLevel + 0.2);
                glucagonLevel = Math.max(0, glucagonLevel - 0.1);
            } else if (bloodSugar < 4.5) {
                // 血糖偏低，增加胰高血糖素，减少胰岛素
                glucagonLevel = Math.min(100, glucagonLevel + 0.2);
                insulinLevel = Math.max(0, insulinLevel - 0.1);
            } else {
                // 血糖正常，激素缓慢回归中等水平
                if (insulinLevel > 50) insulinLevel -= 0.05;
                if (insulinLevel < 50) insulinLevel += 0.05;
                if (glucagonLevel > 50) glucagonLevel -= 0.05;
                if (glucagonLevel < 50) glucagonLevel += 0.05;
            }
            
            // 事件影响
            if (activeEvent) {
                const elapsed = animationTime - eventStartTime;
                const progress = Math.min(elapsed / eventDuration, 1);
                
                switch(activeEvent) {
                    case 'eat':
                        // 吃糖：快速增加血糖
                        if (progress < 0.5) {
                            bloodSugar += 0.05;
                        }
                        break;
                        
                    case 'exercise':
                        // 运动：消耗血糖
                        bloodSugar -= 0.02;
                        break;
                        
                    case 'fasting':
                        // 禁食：缓慢降低血糖
                        bloodSugar -= 0.005;
                        break;
                        
                    case 'insulin':
                        // 注射胰岛素：大幅增加胰岛素水平
                        insulinLevel = Math.min(100, insulinLevel + 0.5);
                        break;
                        
                    case 'stress':
                        // 应激：同时增加两种激素
                        insulinLevel = Math.min(100, insulinLevel + 0.1);
                        glucagonLevel = Math.min(100, glucagonLevel + 0.3);
                        break;
                }
            }
            
            // 限制血糖范围
            bloodSugar = Math.max(2.0, Math.min(bloodSugar, 15.0));
            
            // 更新葡萄糖粒子数量
            const targetParticleCount = Math.floor(bloodSugar * 10);
            if (glucoseParticles.length < targetParticleCount) {
                // 添加新粒子
                for (let i = glucoseParticles.length; i < targetParticleCount; i++) {
                    glucoseParticles.push({
                        x: body.x + (Math.random() - 0.5) * body.width * 0.8,
                        y: body.y + (Math.random() - 0.5) * body.height * 0.8,
                        size: Math.random() * 4 + 2,
                        speedX: (Math.random() - 0.5) * 1.5,
                        speedY: (Math.random() - 0.5) * 1.5,
                        alpha: Math.random() * 0.5 + 0.5
                    });
                }
            } else if (glucoseParticles.length > targetParticleCount) {
                // 移除多余粒子
                glucoseParticles = glucoseParticles.slice(0, targetParticleCount);
            }
            
            // 更新激素粒子
            initHormoneParticles();
            
            // 更新UI显示
            updateUI();
        }
        
        // 更新UI显示
        function updateUI() {
            // 更新血糖值
            document.getElementById('bloodSugarValue').textContent = bloodSugar.toFixed(1) + ' mmol/L';
            
            // 更新血糖状态
            const statusElement = document.getElementById('bloodSugarStatus');
            if (bloodSugar >= 3.9 && bloodSugar <= 6.1) {
                statusElement.textContent = '正常';
                statusElement.className = 'blood-sugar-status status-normal';
            } else if (bloodSugar > 6.1) {
                statusElement.textContent = '偏高';
                statusElement.className = 'blood-sugar-status status-high';
            } else {
                statusElement.textContent = '偏低';
                statusElement.className = 'blood-sugar-status status-low';
            }
            
            // 更新激素水平条
            document.getElementById('insulinBar').style.width = insulinLevel + '%';
            document.getElementById('glucagonBar').style.width = glucagonLevel + '%';
            
            // 更新激素水平文本
            document.getElementById('insulinLevel').textContent = 
                insulinLevel < 30 ? '低' : insulinLevel < 70 ? '中等' : '高';
            document.getElementById('glucagonLevel').textContent = 
                glucagonLevel < 30 ? '低' : glucagonLevel < 70 ? '中等' : '高';
        }
        
        // 主动画循环
        function animate() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            ctx.fillStyle = '#fefefe';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 更新时间和系统状态
            if (isPlaying) {
                animationTime += 0.016; // 假设60fps
                updateSystem();
            }
            
            // 绘制所有元素
            drawBody();
            drawGlucoseParticles();
            drawHormoneParticles();
            drawEventEffects();
            
            // 继续动画循环
            animationId = requestAnimationFrame(animate);
        }

<!--检测到代码截断，自动续写中...-->
// 事件处理函数
function triggerEvent(eventType) {
    activeEvent = eventType;
    eventStartTime = animationTime;
    
    // 设置事件持续时间
    switch(eventType) {
        case 'eat':
            eventDuration = 3.0;
            break;
        case 'exercise':
            eventDuration = 5.0;
            break;
        case 'fasting':
            eventDuration = 8.0;
            break;
        case 'insulin':
            eventDuration = 2.0;
            break;
        case 'stress':
            eventDuration = 4.0;
            break;
        default:
            eventDuration = 3.0;
    }
}

// 初始化函数
function init() {
    // 初始化粒子
    initGlucoseParticles();
    initHormoneParticles();
    
    // 设置事件监听器
    document.getElementById('playBtn').addEventListener('click', () => {
        isPlaying = true;
    });
    
    document.getElementById('pauseBtn').addEventListener('click', () => {
        isPlaying = false;
    });
    
    document.getElementById('resetBtn').addEventListener('click', () => {
        isPlaying = false;
        bloodSugar = 5.0;
        insulinLevel = 50;
        glucagonLevel = 50;
        animationTime = 0;
        activeEvent = null;
        initGlucoseParticles();
        initHormoneParticles();
        updateUI();
    });
    
    document.getElementById('eatBtn').addEventListener('click', () => {
        triggerEvent('eat');
    });
    
    document.getElementById('exerciseBtn').addEventListener('click', () => {
        triggerEvent('exercise');
    });
    
    document.getElementById('fastingBtn').addEventListener('click', () => {
        triggerEvent('fasting');
    });
    
    document.getElementById('insulinBtn').addEventListener('click', () => {
        triggerEvent('insulin');
    });
    
    document.getElementById('stressBtn').addEventListener('click', () => {
        triggerEvent('stress');
    });
    
    document.getElementById('toggleLabelsBtn').addEventListener('click', () => {
        showLabels = !showLabels;
    });
    
    document.getElementById('toggleGlucoseBtn').addEventListener('click', () => {
        showGlucose = !showGlucose;
    });
    
    // 添加Canvas圆角矩形方法（如果浏览器不支持）
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
    
    // 开始动画
    animate();
    
    // 初始UI更新
    updateUI();
}

// 页面加载完成后初始化
window.addEventListener('load', init);

// 窗口大小调整时重新调整Canvas大小
window.addEventListener('resize', () => {
    // 获取容器尺寸
    const container = document.querySelector('.animation-panel');
    const containerWidth = container.clientWidth - 40; // 减去padding
    
    // 保持宽高比
    const aspectRatio = 800 / 500;
    const newWidth = containerWidth;
    const newHeight = containerWidth / aspectRatio;
    
    // 设置Canvas尺寸
    canvas.width = newWidth;
    canvas.height = newHeight;
    
    // 重新计算器官位置
    body.x = canvas.width * 0.5;
    body.y = canvas.height * 0.5;
    body.width = canvas.width * 0.6;
    body.height = canvas.height * 0.7;
    
    pancreas.x = body.x - body.width * 0.15;
    pancreas.y = body.y - body.height * 0.1;
    
    liver.x = body.x + body.width * 0.1;
    liver.y = body.y - body.height * 0.05;
    
    muscleCells.x = body.x - body.width * 0.2;
    muscleCells.y = body.y + body.height * 0.2;
    
    fatCells.x = body.x + body.width * 0.15;
    fatCells.y = body.y + body.height * 0.25;
    
    // 重新初始化粒子
    initGlucoseParticles();
    initHormoneParticles();
});

// 初始调整Canvas大小
window.dispatchEvent(new Event('resize'));

</script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## 血糖调节双激素负反馈交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过可视化、动态交互的方式，帮助您深入理解人体血糖调节的核心机制——胰岛素与胰高血糖素的双激素负反馈系统。无论您是生物学学生、医学预科生，还是对生理学感兴趣的爱好者，本动画都将为您提供直观、生动的学习体验。

---

### 一、功能说明

本动画模拟了人体血糖调节的动态过程，通过以下核心功能实现教学目的：

1. **实时可视化系统**：将抽象的生理过程转化为直观的视觉元素
   - 葡萄糖分子（黄色圆点）在血管中流动
   - 胰岛素（蓝色钥匙状）和胰高血糖素（橙色火焰状）从胰腺分泌
   - 靶器官（肝脏、肌肉细胞、脂肪细胞）的高亮显示

2. **动态数据监控**：实时显示关键生理指标
   - 血糖浓度数值与状态指示
   - 两种激素水平的可视化进度条
   - 系统状态的即时反馈

3. **交互式实验环境**：允许用户主动干预系统，观察生理响应

---

### 二、主要功能模块

#### 1. 动画控制区
- **播放/暂停**：控制动画的自动运行
- **重置**：将系统恢复到初始平衡状态（血糖5.0 mmol/L，激素水平中等）

#### 2. 模拟事件区
通过点击以下按钮，模拟不同生理状况：

| 事件按钮 | 模拟场景 | 生理效应 |
|---------|---------|---------|
| **吃一块糖** | 进食后血糖快速升高 | 血糖↑ → 胰岛素分泌↑ → 促进葡萄糖储存 |
| **剧烈运动** | 肌肉大量消耗能量 | 血糖↓ → 胰高血糖素分泌↑ → 促进糖原分解 |
| **跳过一餐** | 长时间未进食 | 血糖缓慢↓ → 胰高血糖素持续作用 |
| **注射胰岛素** | 糖尿病治疗情景 | 外源性胰岛素↑ → 血糖快速↓ |
| **应激状态** | 紧张、压力情况 | 两种激素均↑，以胰高血糖素为主 |

#### 3. 状态显示区
- **血糖浓度**：实时数值与状态指示（正常/偏高/偏低）
- **激素水平**：胰岛素与胰高血糖素的相对水平可视化
- **颜色编码**：蓝色代表胰岛素，橙色代表胰高血糖素

#### 4. 可视化选项
- **显示/隐藏标签**：切换器官和细胞标签，可用于自我测验
- **显示/隐藏葡萄糖**：简化视图，专注于激素作用机制

---

### 三、设计特色

#### 1. 科学准确性
- 基于真实的生理学原理设计
- 负反馈机制精确模拟：血糖变化→激素分泌变化→血糖回归正常
- 激素拮抗作用清晰呈现

#### 2. 视觉隐喻设计
- **胰岛素**：蓝色钥匙形状，象征"打开细胞门锁，让葡萄糖进入"
- **胰高血糖素**：橙色火焰形状，象征"燃烧储备，释放能量"
- **葡萄糖**：黄色圆点，直观表示血糖浓度变化

#### 3. 多层次学习支持
- **观察层**：观看自动演示，理解基本流程
- **操作层**：主动干预系统，探索因果关系
- **反思层**：结合右侧说明文字，深化概念理解

#### 4. 实时反馈系统
- 所有操作立即产生可视化效果
- 数据变化与动画同步更新
- 状态指示器提供即时诊断

---

### 四、教学要点

#### 核心概念强调

1. **负反馈调节的本质**
   - 系统对偏离正常状态的反应总是**反向**的
   - 血糖升高→降糖机制启动→血糖降低
   - 血糖降低→升糖机制启动→血糖升高

2. **激素的拮抗作用**
   - 胰岛素与胰高血糖素作用**相反**但目标**一致**
   - 共同维持血糖稳态，而非相互对抗
   - 正常情况下，两者处于动态平衡

3. **靶器官特异性**
   - **胰岛素**主要作用于肌肉和脂肪细胞（促进葡萄糖摄取）
   - **胰高血糖素**主要作用于肝脏（促进糖原分解）
   - 理解不同组织的不同功能

#### 推荐学习路径

1. **第一步：观察自动运行**
   - 点击"播放"，观察系统在无干扰下的自我调节
   - 注意血糖在正常范围内的微小波动
   - 观察激素水平的相应调整

2. **第二步：单一事件实验**
   - 点击"吃一块糖"，观察完整响应链条
   - 特别注意：血糖峰值→胰岛素激增→血糖回落的时间顺序
   - 重复其他事件，比较不同刺激的响应模式

3. **第三步：组合事件探索**
   - 尝试"吃糖"后立即"运动"
   - 观察系统如何处理冲突信号
   - 理解主导机制的判断依据

4. **第四步：概念验证**
   - 隐藏标签，尝试仅通过动画判断当前状态
   - 预测特定操作的结果，然后验证
   - 将观察到的现象与理论知识对应

---

### 五、使用建议

#### 课堂教学应用

1. **导入环节**：播放完整动画，引出"血糖如何保持稳定"的问题
2. **讲解环节**：分步演示，配合右侧文字说明，讲解关键概念
3. **探究环节**：学生分组操作，设计实验验证假设
4. **总结环节**：讨论观察结果，归纳负反馈调节的普遍规律

#### 自主学习策略

1. **概念先行**：先阅读右侧说明，了解基本机制
2. **操作验证**：通过动画验证每个理论要点
3. **自我测验**：隐藏标签，尝试描述当前生理状态
4. **拓展思考**：思考其他负反馈系统（如体温调节、血压调节）的相似性

#### 常见问题引导

- **为什么吃糖后胰岛素不是立即分泌？**
  - 观察从血糖升高到胰腺响应的延迟时间
- **运动时两种激素如何变化？为什么？**
  - 注意胰高血糖素的主导作用
- **如果胰岛素持续过高会怎样？**
  - 尝试连续点击"注射胰岛素"按钮
- **负反馈与正反馈有何区别？**
  - 对比本系统与分娩、血液凝固等正反馈系统

#### 技术提示

1. **最佳观看环境**：在电脑或平板上使用，确保屏幕足够大以看清细节
2. **浏览器兼容性**：建议使用Chrome、Firefox或Edge等现代浏览器
3. **性能优化**：如果动画运行缓慢，可尝试隐藏葡萄糖粒子
4. **学习记录**：建议记录不同操作下的血糖变化曲线，绘制图表对比

---

### 六、延伸学习

本动画展示的是简化模型，真实生理过程更为复杂：
- 除胰岛素和胰高血糖素外，肾上腺素、皮质醇等也参与血糖调节
- 激素分泌受神经调节和体液调节双重控制
- 糖尿病病理与胰岛素抵抗、β细胞功能减退相关
- 进食后胰岛素分泌分为快速相和延迟相

鼓励学有余力的学习者：
1. 查阅生理学教材，了解更详细的调节机制
2. 比较1型糖尿病和2型糖尿病在本动画中的模拟差异
3. 设计实验探究不同食物（碳水化合物、蛋白质、脂肪）对血糖影响的差异

---

**最后提醒**：本工具是教学辅助材料，不能替代专业医学知识。如果您有血糖相关的健康问题，请咨询专业医疗人员。

祝您学习愉快，探索生理学的奥秘！ 🐼