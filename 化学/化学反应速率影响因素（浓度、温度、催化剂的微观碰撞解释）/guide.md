# 需求：化学反应速率影响因素（浓度、温度、催化剂的微观碰撞解释）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的化学初学者。他们已具备基本的分子、原子概念，但对抽象的微观反应机理和统计规律理解存在困难。
2.  **核心痛点**：
    *   **抽象性**：学生难以将宏观的“反应快慢”与微观的“分子碰撞”建立直观联系。
    *   **动态性**：传统静态图表无法展示分子随机运动、有效碰撞的动态过程。
    *   **多因素干扰**：浓度、温度、催化剂三个因素同时影响，学生容易混淆其各自的作用机理。
3.  **学习目标**：
    *   **理解核心**：建立“化学反应速率取决于单位时间内有效碰撞频率”的微观模型。
    *   **区分因素**：能清晰解释浓度、温度、催化剂分别如何影响有效碰撞频率。
    *   **形成直觉**：通过观察动画，对“哪个条件反应更快”产生直观的预测能力。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念解构**：
    *   **基线模型**：所有反应均源于分子（用小球代表）的随机热运动和无规则碰撞。
    *   **有效碰撞**：引入“能量阈值”（活化能）概念，只有动能足够大（速度足够快）的碰撞才能导致反应。这是动画需要重点凸显的关键。
    *   **三因素机理**：
        *   **浓度**：增加单位体积内反应物分子数 → 碰撞频率增加 → 有效碰撞频率增加。
        *   **温度**：提高分子平均动能 → 更多分子达到或超过活化能 → 有效碰撞比例和频率均增加。
        *   **催化剂**：提供一条“低矮的山路”（降低活化能）→ 使更多碰撞成为有效碰撞 → 有效碰撞比例大幅增加。

2.  **认知规律遵循**：
    *   **从简到繁**：先展示单一因素（如浓度）对基线模型的影响，再引入更复杂的因素（如温度、催化剂）。
    *   **对比学习**：设计并排或可切换的动画场景，让用户能直观对比不同条件下分子运动的差异。
    *   **主动建构**：通过交互控制变量，让用户自己“做实验”观察结果，而非被动观看。

3.  **交互设计**：
    *   **控制面板**：提供清晰的滑块或按钮，分别控制“浓度”（分子数量）、“温度”（分子运动速度/动能）、“催化剂”（开关，用于改变活化能阈值线）。
    *   **模拟与重置**：提供“开始/暂停/重置”模拟的控件。
    *   **数据可视化**：实时显示关键数据，如“总碰撞次数”、“有效碰撞次数”、“当前温度/浓度值”、“活化能阈值线”。
    *   **焦点提示**：当用户调整某个因素时，动画应有视觉反馈（如高亮相关分子、改变阈值线颜色），引导注意力。

4.  **视觉呈现**：
    *   **分子表征**：用不同颜色（如红、蓝）的圆球代表不同反应物分子。分子大小适中，确保在合理数量下清晰可见。
    *   **运动与碰撞**：分子做布朗运动。碰撞时应有轻微形变或光效提示。**有效碰撞**必须与普通碰撞有显著区别（例如，碰撞时分子变色、结合成新物质、或迸发出特殊光效/火花）。
    *   **能量可视化**：
        *   **动能**：用分子运动速度直观表现。高温时分子运动轨迹更“躁动”。
        *   **活化能**：在场景一侧设置一个垂直的“能量标尺”，并有一条清晰的“阈值线”。可以设计分子在碰撞瞬间，其动能（可用一个临时上升的色条或高度表示）与阈值线进行比较。
    *   **催化剂**：可以用一个固定的、特殊形状的物体（如一个凹槽或平台）表示催化剂表面。当分子与其接触时，阈值线临时降低，或分子被“激活”发出光芒，再进行更容易成功的碰撞。

#### 配色方案选择
*   **主色调**：采用深蓝色或深灰色作为画布背景，模拟微观世界的深邃感，并能突出彩色的分子。
*   **分子颜色**：
    *   反应物A：采用明快的**红色**。
    *   反应物B：采用清爽的**蓝色**。
    *   生成物：当有效碰撞发生后，红蓝分子结合，可以变为**紫色**，或保持连接状态。
*   **功能与数据色**：
    *   **有效碰撞高亮色**：使用**亮黄色**或**白色**闪光，表示成功反应瞬间，吸引所有注意力。
    *   **活化能阈值线**：使用**醒目的橙色**或**红色**实线。
    *   **催化剂降低的阈值线**：当催化剂启用时，在原阈值线下方显示一条**绿色**虚线，形成对比。
    *   **UI控件与数据文本**：使用**浅灰色**或**白色**，确保清晰可读。
*   **整体原则**：保证高对比度，色彩有明确的语义指向（如红/蓝对立，黄/白高亮，绿表促进），避免过多杂乱色彩干扰对核心过程的观察。

#### 交互功能列表
1.  **模拟控制**：
    *   开始 / 暂停 / 重置 按钮。
2.  **变量控制面板**：
    *   **浓度滑块**：控制反应物分子的数量（如10-100个）。
    *   **温度滑块**：控制分子的平均运动速度（如“低温”、“室温”、“高温”三档或连续调节）。
    *   **催化剂开关**：一个复选框或Toggle按钮，用于开启或关闭催化剂效应。
3.  **可视化显示面板**：
    *   **实时计数器**：显示“总碰撞次数”和“有效碰撞（反应）次数”。
    *   **反应速率指示器**：一个简单的柱状图或数字，根据有效碰撞频率动态变化。
    *   **能量分布图**（可选）：一个简单的动态条形图，显示当前速度（动能）分布，以及活化能阈值线的位置。
4.  **教学提示与高亮**：
    *   **因素说明标签**：当鼠标悬停在某个控制滑块上时，显示简短的文字说明（如“增加浓度 = 增加碰撞机会”）。
    *   **有效碰撞追踪**：可勾选“高亮有效碰撞”选项，使每一次有效碰撞的视觉效果更持久、更突出。
    *   **分子动能显示**（可选）：勾选后，每个分子上方显示一个代表其瞬时动能的小色条。

此设计旨在创建一个直观、可探索的微观世界模拟器，将抽象的化学原理转化为可见、可操作的动态过程。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>化学反应速率影响因素 - 微观碰撞解释</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #e0f7fa;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .container {
            max-width: 1200px;
            width: 100%;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        header {
            text-align: center;
            padding: 20px;
            background: rgba(0, 30, 60, 0.7);
            border-radius: 15px;
            border: 2px solid #4fc3f7;
            box-shadow: 0 5px 15px rgba(0, 150, 255, 0.2);
        }

        h1 {
            color: #4fc3f7;
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }

        .subtitle {
            color: #b3e5fc;
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }

        .simulation-area {
            flex: 1;
            min-width: 300px;
            background: rgba(10, 25, 47, 0.85);
            border-radius: 15px;
            padding: 15px;
            border: 2px solid #00bcd4;
            box-shadow: 0 5px 15px rgba(0, 188, 212, 0.3);
            display: flex;
            flex-direction: column;
        }

        .canvas-container {
            position: relative;
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            background: #0a1929;
            border: 1px solid #1a3a5f;
        }

        #reactionCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }

        .energy-scale {
            position: absolute;
            right: 10px;
            top: 10px;
            width: 30px;
            height: 80%;
            background: rgba(0, 0, 0, 0.6);
            border-radius: 5px;
            border: 1px solid #555;
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 5px 0;
        }

        .threshold-line {
            position: absolute;
            left: 0;
            width: 100%;
            height: 3px;
            background-color: #ff9800;
            box-shadow: 0 0 5px #ff9800;
        }

        .catalyst-threshold {
            background-color: #4caf50;
            box-shadow: 0 0 5px #4caf50;
        }

        .controls-panel {
            flex: 1;
            min-width: 300px;
            background: rgba(10, 25, 47, 0.85);
            border-radius: 15px;
            padding: 20px;
            border: 2px solid #00bcd4;
            box-shadow: 0 5px 15px rgba(0, 188, 212, 0.3);
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .panel-section {
            background: rgba(20, 40, 80, 0.5);
            border-radius: 10px;
            padding: 15px;
            border-left: 4px solid #2196f3;
        }

        .section-title {
            color: #29b6f6;
            font-size: 1.3rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .section-title i {
            font-size: 1.2rem;
        }

        .control-group {
            margin-bottom: 15px;
        }

        .control-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            color: #bbdefb;
        }

        .value-display {
            color: #4fc3f7;
            font-weight: bold;
        }

        .slider {
            width: 100%;
            height: 10px;
            -webkit-appearance: none;
            appearance: none;
            background: linear-gradient(to right, #1565c0, #42a5f5);
            border-radius: 5px;
            outline: none;
        }

        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #00e5ff;
            cursor: pointer;
            border: 2px solid #ffffff;
            box-shadow: 0 0 5px rgba(0, 229, 255, 0.8);
        }

        .toggle-switch {
            position: relative;
            display: inline-block;
            width: 60px;
            height: 30px;
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
            background-color: #555;
            border-radius: 34px;
            transition: .4s;
        }

        .toggle-slider:before {
            position: absolute;
            content: "";
            height: 22px;
            width: 22px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            border-radius: 50%;
            transition: .4s;
        }

        input:checked + .toggle-slider {
            background-color: #4caf50;
        }

        input:checked + .toggle-slider:before {
            transform: translateX(30px);
        }

        .button-group {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        .btn {
            flex: 1;
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .btn-primary {
            background: linear-gradient(to right, #00bcd4, #00838f);
            color: white;
        }

        .btn-primary:hover {
            background: linear-gradient(to right, #00acc1, #006064);
            box-shadow: 0 0 10px rgba(0, 188, 212, 0.5);
        }

        .btn-secondary {
            background: linear-gradient(to right, #757575, #424242);
            color: white;
        }

        .btn-secondary:hover {
            background: linear-gradient(to right, #616161, #212121);
            box-shadow: 0 0 10px rgba(117, 117, 117, 0.5);
        }

        .stats-panel {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 10px;
        }

        .stat-box {
            background: rgba(30, 60, 114, 0.6);
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            border: 1px solid #2962ff;
        }

        .stat-value {
            font-size: 2rem;
            font-weight: bold;
            color: #00e5ff;
            margin: 5px 0;
            text-shadow: 0 0 5px rgba(0, 229, 255, 0.7);
        }

        .stat-label {
            color: #bbdefb;
            font-size: 0.9rem;
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
            border-radius: 50%;
        }

        .legend-text {
            color: #e0f7fa;
            font-size: 0.9rem;
        }

        footer {
            text-align: center;
            padding: 15px;
            color: #80d8ff;
            font-size: 0.9rem;
            margin-top: 10px;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .stats-panel {
                grid-template-columns: 1fr 1fr;
            }
        }

        .highlight {
            animation: pulse 0.5s ease;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>化学反应速率影响因素</h1>
            <p class="subtitle">通过微观分子碰撞模型，直观理解浓度、温度、催化剂如何影响化学反应速率。调整参数，观察分子运动、碰撞和反应的变化。</p>
        </header>

        <div class="main-content">
            <div class="simulation-area">
                <div class="canvas-container">
                    <canvas id="reactionCanvas"></canvas>
                    <div class="energy-scale">
                        <div class="threshold-line" id="thresholdLine"></div>
                        <div class="threshold-line catalyst-threshold" id="catalystThreshold" style="display: none;"></div>
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff5252;"></div>
                        <span class="legend-text">反应物 A (红色分子)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #448aff;"></div>
                        <span class="legend-text">反应物 B (蓝色分子)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #7c4dff;"></div>
                        <span class="legend-text">生成物 (紫色分子)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff9800;"></div>
                        <span class="legend-text">活化能阈值</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #4caf50;"></div>
                        <span class="legend-text">催化剂降低的阈值</span>
                    </div>
                </div>
            </div>

            <div class="controls-panel">
                <div class="panel-section">
                    <h2 class="section-title">模拟控制</h2>
                    <div class="button-group">
                        <button id="startBtn" class="btn btn-primary">▶ 开始模拟</button>
                        <button id="pauseBtn" class="btn btn-secondary">⏸ 暂停</button>
                        <button id="resetBtn" class="btn btn-secondary">↺ 重置</button>
                    </div>
                </div>

                <div class="panel-section">
                    <h2 class="section-title">影响因素调节</h2>
                    
                    <div class="control-group">
                        <div class="control-label">
                            <span>浓度 (分子数量)</span>
                            <span id="concentrationValue" class="value-display">50</span>
                        </div>
                        <input type="range" min="10" max="100" value="50" class="slider" id="concentrationSlider">
                        <div style="display: flex; justify-content: space-between; font-size: 0.8rem; color: #90a4ae; margin-top: 5px;">
                            <span>稀</span>
                            <span>浓</span>
                        </div>
                    </div>

                    <div class="control-group">
                        <div class="control-label">
                            <span>温度 (分子动能)</span>
                            <span id="temperatureValue" class="value-display">中</span>
                        </div>
                        <input type="range" min="1" max="3" value="2" class="slider" id="temperatureSlider">
                        <div style="display: flex; justify-content: space-between; font-size: 0.8rem; color: #90a4ae; margin-top: 5px;">
                            <span>低</span>
                            <span>中</span>
                            <span>高</span>
                        </div>
                    </div>

                    <div class="control-group">
                        <div class="control-label">
                            <span>催化剂</span>
                            <div>
                                <span id="catalystStatus" class="value-display">关闭</span>
                                <label class="toggle-switch" style="margin-left: 10px;">
                                    <input type="checkbox" id="catalystToggle">
                                    <span class="toggle-slider"></span>
                                </label>
                            </div>
                        </div>
                        <p style="color: #b3e5fc; font-size: 0.9rem; margin-top: 8px;">催化剂通过降低反应活化能，使更多碰撞成为有效碰撞。</p>
                    </div>
                </div>

                <div class="panel-section">
                    <h2 class="section-title">实时数据</h2>
                    <div class="stats-panel">
                        <div class="stat-box">
                            <div class="stat-value" id="totalCollisions">0</div>
                            <div class="stat-label">总碰撞次数</div>
                        </div>
                        <div class="stat-box">
                            <div class="stat-value" id="effectiveCollisions">0</div>
                            <div class="stat-label">有效碰撞次数</div>
                        </div>
                        <div class="stat-box">
                            <div class="stat-value" id="reactionRate">0</div>
                            <div class="stat-label">反应速率 (次/秒)</div>
                        </div>
                        <div class="stat-box">
                            <div class="stat-value" id="productCount">0</div>
                            <div class="stat-label">生成物数量</div>
                        </div>
                    </div>
                </div>

                <div class="panel-section">
                    <h2 class="section-title">微观解释</h2>
                    <div id="explanationText" style="color: #e1f5fe; line-height: 1.6; font-size: 0.95rem;">
                        <p><strong>浓度</strong>: 增加单位体积内分子数 → 碰撞频率增加 → 有效碰撞增加。</p>
                        <p><strong>温度</strong>: 提高分子平均动能 → 更多分子达到活化能 → 有效碰撞比例增加。</p>
                        <p><strong>催化剂</strong>: 提供低能量路径 → 降低活化能 → 更多碰撞成为有效碰撞。</p>
                        <p style="margin-top: 10px; color: #4fc3f7;">调整上方参数，观察微观变化如何影响宏观反应速率！</p>
                    </div>
                </div>
            </div>
        </div>

        <footer>
            <p>化学反应速率微观解释模拟器 | 设计原理：碰撞理论 | 有效碰撞需要满足能量要求（活化能）和合适取向</p>
        </footer>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('reactionCanvas');
        const ctx = canvas.getContext('2d');

        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }

        // 初始化变量
        let animationId = null;
        let isRunning = false;
        let lastTime = 0;
        let statsInterval;

        // 模拟参数
        let params = {
            concentration: 50,      // 分子数量
            temperature: 2,         // 1=低, 2=中, 3=高
            catalyst: false,        // 催化剂是否启用
            baseActivationEnergy: 0.7,  // 基础活化能阈值 (0-1)
            catalystActivationEnergy: 0.4 // 催化剂下的活化能阈值
        };

        // 统计数据
        let stats = {
            totalCollisions: 0,
            effectiveCollisions: 0,
            productCount: 0,
            collisionsPerSecond: 0,
            lastSecondCollisions: 0,
            lastSecondTime: 0
        };

        // 分子数组
        let molecules = [];
        let products = [];

        // 分子类
        class Molecule {
            constructor(type, x, y) {
                this.type = type; // 'A' 或 'B'
                this.x = x;
                this.y = y;
                this.radius = type === 'A' ? 12 : 10; // A分子稍大
                this.color = type === 'A' ? '#ff5252' : '#448aff';
                this.vx = (Math.random() - 0.5) * 2;
                this.vy = (Math.random() - 0.5) * 2;
                this.collisionCooldown = 0;
                this.isProduct = false;
            }

            // 更新位置
            update(deltaTime, speedFactor) {
                // 应用温度影响速度
                const tempFactor = params.temperature === 1 ? 0.5 : params.temperature === 2 ? 1 : 1.8;
                
                this.x += this.vx * speedFactor * tempFactor * deltaTime;
                this.y += this.vy * speedFactor * tempFactor * deltaTime;

                // 边界碰撞
                if (this.x < this.radius || this.x > canvas.width - this.radius) {
                    this.vx *= -0.95; // 轻微能量损失
                    this.x = this.x < this.radius ? this.radius : canvas.width - this.radius;
                }
                if (this.y < this.radius || this.y > canvas.height - this.radius) {
                    this.vy *= -0.95;
                    this.y = this.y < this.radius ? this.radius : canvas.height - this.radius;
                }

                // 冷却时间减少
                if (this.collisionCooldown > 0) {
                    this.collisionCooldown -= deltaTime;
                }
            }

            // 绘制分子
            draw() {
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = this.color;
                ctx.fill();
                
                // 添加高光效果
                ctx.beginPath();
                ctx.arc(this.x - this.radius/3, this.y - this.radius/3, this.radius/3, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
                ctx.fill();
                
                // 如果是生成物，添加连接线
                if (this.isProduct) {
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius + 2, 0, Math.PI * 2);
                    ctx.strokeStyle = '#7c4dff';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
            }

            // 计算动能 (用于判断是否达到活化能)
            getKineticEnergy() {
                const speed = Math.sqrt(this.vx * this.vx + this.vy * this.vy);
                return speed * speed * (this.type === 'A' ? 1.2 : 1.0); // A分子质量稍大
            }
        }

        // 生成物类
        class Product {
            constructor(x, y) {
                this.x = x;
                this.y = y;
                this.radius = 14;
                this.color = '#7c4dff';
                this.life = 5; // 生成物存在时间（秒）
            }

            update(deltaTime) {
                this.life -= deltaTime;
                return this.life > 0;
            }

            draw() {
                const alpha = Math.min(1, this.life);
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = `rgba(124, 77, 255, ${alpha})`;
                ctx.fill();
                
                // 发光效果
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius + 5, 0, Math.PI * 2);
                ctx.strokeStyle = `rgba(124, 77, 255, ${alpha * 0.3})`;
                ctx.lineWidth = 2;
                ctx.stroke();
            }
        }

        // 初始化分子
        function initMolecules() {
            molecules = [];
            products = [];
            
            const countA = Math.floor(params.concentration / 2);
            const countB = params.concentration - countA;
            
            // 创建A分子
            for (let i = 0; i < countA; i++) {
                const x = Math.random() * (canvas.width - 40) + 20;
                const y = Math.random() * (canvas.height - 40) + 20;
                molecules.push(new Molecule('A', x, y));
            }
            
            // 创建B分子
            for (let i = 0; i < countB; i++) {
                const x = Math.random() * (canvas.width - 40) + 20;
                const y = Math.random() * (canvas.height - 40) + 20;
                molecules.push(new Molecule('B', x, y));
            }
        }

        // 检测碰撞并处理
        function handleCollisions() {
            for (let i = 0; i < molecules.length; i++) {
                for (let j = i + 1; j < molecules.length; j++) {
                    const mol1 = molecules[i];
                    const mol2 = molecules[j];
                    
                    // 跳过冷却中的分子
                    if (mol1.collisionCooldown > 0 || mol2.collisionCooldown > 0) continue;
                    
                    // 计算距离
                    const dx = mol2.x - mol1.x;
                    const dy = mol2.y - mol1.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    // 检测碰撞
                    if (distance < mol1.radius + mol2.radius) {
                        stats.totalCollisions++;
                        
                        // 计算相对动能
                        const relativeSpeed = Math.sqrt(
                            Math.pow(mol2.vx - mol1.vx, 2) + 
                            Math.pow(mol2.vy - mol1.vy, 2)
                        );
                        const kineticEnergy = relativeSpeed * relativeSpeed;
                        
                        // 确定活化能阈值
                        const activationEnergy = params.catalyst ? 
                            params.catalystActivationEnergy : params.baseActivationEnergy;
                        
                        // 判断是否为有效碰撞（不同类型分子且动能足够）
                        const isEffective = mol1.type !== mol2.type && kineticEnergy > activationEnergy;
                        
                        if (isEffective) {
                            stats.effectiveCollisions++;
                            stats.productCount++;
                            
                            // 创建生成物
                            const px = (mol1.x + mol2.x) / 2;
                            const py = (mol1.y + mol2.y) / 2;
                            products.push(new Product(px, py));
                            
                            // 标记分子为生成物（视觉上）
                            mol1.isProduct = true;
                            mol2.isProduct = true;
                            
                            // 有效碰撞特效
                            drawCollisionEffect(px, py, '#00e5ff');
                        } else {
                            // 普通碰撞特效
                            drawCollisionEffect((mol1.x + mol2.x) / 2, (mol1.y + mol2.y) / 2, '#ffffff');
                        }
                        
                        // 碰撞响应（弹性碰撞简化版）
                        const angle = Math.atan2(dy, dx);
                        const sin = Math.sin(angle);
                        const cos = Math.cos(angle);
                        
                        // 旋转速度
                        const vx1 = mol1.vx * cos + mol1.vy * sin;
                        const vy1 = mol1.vy * cos - mol1.vx * sin;
                        const vx2 = mol2.vx * cos + mol2.vy * sin;
                        const vy2 = mol2.vy * cos - mol2.vx * sin;
                        
                        // 交换x方向速度（一维弹性碰撞）
                        const finalVx1 = vx2;
                        const finalVx2 = vx1;
                        
                        // 旋转回原坐标系
                        mol1.vx = finalVx1 * cos - vy1 * sin;
                        mol1.vy = vy1 * cos + finalVx1 * sin;
                        mol2.vx = finalVx2 * cos - vy2 * sin;
                        mol2.vy = vy2 * cos + finalVx2 * sin;
                        
                        // 防止粘连
                        const overlap = mol1.radius + mol2.radius - distance;
                        mol1.x -= overlap * dx / distance / 2;
                        mol1.y -= overlap * dy / distance / 2;
                        mol2.x += overlap * dx / distance / 2;
                        mol2.y += overlap * dy / distance / 2;
                        
                        // 设置冷却时间
                        mol1.collisionCooldown = 0.1;
                        mol2.collisionCooldown = 0.1;
                    }
                }
            }
        }

        // 绘制碰撞特效
        function drawCollisionEffect(x, y, color) {
            ctx.beginPath();
            ctx.arc(x, y, 15, 0, Math.PI * 2);
            ctx.fillStyle = color + '40';
            ctx.fill();
            
            ctx.beginPath();
            ctx.arc(x, y, 8, 0, Math.PI * 2);
            ctx.fillStyle = color + '80';
            ctx.fill();
        }

        // 更新能量标尺
        function updateEnergyScale() {
            const thresholdLine = document.getElementById('thresholdLine');
            const catalystLine = document.getElementById('catalystThreshold');
            const scaleHeight = document.querySelector('.energy-scale').clientHeight;
            
            // 基础活化能阈值位置
            const baseY = scaleHeight * (1 - params.baseActivationEnergy);
            thresholdLine.style.bottom = `${baseY}px`;
            
            // 催化剂阈值位置
            if (params.catalyst) {
                const catalystY = scaleHeight * (1 - params.catalystActivationEnergy);
                catalystLine.style.bottom = `${catalystY}px`;
                catalystLine.style.display = 'block';
            } else {
                catalystLine.style.display = 'none';
            }
        }

        // 更新统计数据
        function updateStats(deltaTime) {
            // 更新每秒碰撞数
            const currentTime = performance.now() / 1000;
            if (currentTime - stats.lastSecondTime >= 1) {
                stats.collisionsPerSecond = stats.effectiveCollisions - stats.lastSecondCollisions;
                stats.lastSecondCollisions = stats.effectiveCollisions;
                stats.lastSecondTime = currentTime;
            }
            
            // 更新显示
            document.getElementById('totalCollisions').textContent = stats.totalCollisions;
            document.getElementById('effectiveCollisions').textContent = stats.effectiveCollisions;
            document.getElementById('reactionRate').textContent = stats.collisionsPerSecond;
            document.getElementById('productCount').textContent = stats.productCount;
            
            // 高亮变化
            document.getElementById('totalCollisions').classList.add('highlight');
            document.getElementById('effectiveCollisions').classList.add('highlight');
            setTimeout(() => {
                document.getElementById('totalCollisions').classList.remove('highlight');
                document.getElementById('effectiveCollisions').classList.remove('highlight');
            }, 300);
        }

        // 主动画循环
        function animate(currentTime) {
            if (!lastTime) lastTime = currentTime;
            const deltaTime = (currentTime - lastTime) / 1000; // 转换为秒
            lastTime = currentTime;
            
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景网格
            drawGrid();
            
            // 更新和绘制分子
            molecules.forEach(mol => {
                mol.update(deltaTime, 60);
                mol.draw();
            });
            
            // 处理碰撞
            handleCollisions();
            
            // 更新和绘制生成物
            products = products.filter(product => product.update(deltaTime));
            products.forEach(product => product.draw());
            
            // 更新能量标尺
            updateEnergyScale();
            
            // 更新统计数据
            updateStats(deltaTime);
            
            if (isRunning) {
                animationId = requestAnimationFrame(animate);
            }
        }

        // 绘制背景网格
        function drawGrid() {
            ctx.strokeStyle = 'rgba(100, 150, 255, 0.05)';
            ctx.lineWidth = 1;
            
            // 垂直线
            for (let x = 0; x < canvas.width; x += 50) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, canvas.height);
                ctx.stroke();
            }
            
            // 水平线
            for (let y = 0; y < canvas.height; y += 50) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(canvas.width, y);
                ctx.stroke();
            }
        }

        // 重置模拟
        function resetSimulation() {
            stats = {
                totalCollisions: 0,
                effectiveCollisions: 0,
                productCount: 0,
                collisionsPerSecond: 0,
                lastSecondCollisions: 0,
                lastSecondTime: 0
            };
            
            initMolecules();
            updateStats(0);
        }

        // 开始模拟
        function startSimulation() {
            if (!isRunning) {
                isRunning = true;
                lastTime = 0;
                animationId = requestAnimationFrame(animate);
                document.getElementById('startBtn').textContent = '▶ 模拟中...';
            }
        }

        // 暂停模拟
        function pauseSimulation() {
            isRunning = false;
            if (animationId) {
                cancelAnimationFrame(animationId);
                animationId = null;
            }
            document.getElementById('startBtn').textContent = '▶ 继续模拟';
        }

        // 事件监听器
        document.getElementById('startBtn').addEventListener('click', startSimulation);
        document.getElementById('pauseBtn').addEventListener('click', pauseSimulation);
        document.getElementById('resetBtn').addEventListener('click', resetSimulation);

        // 浓度滑块
        const concentrationSlider = document.getElementById('concentrationSlider');
        const concentrationValue = document.getElementById('concentrationValue');
        
        concentrationSlider.addEventListener('input', function() {
            params.concentration = parseInt(this.value);
            concentrationValue.textContent = params.concentration;
            initMolecules();
        });

        // 温度滑块
        const temperatureSlider = document.getElementById('temperatureSlider');
        const temperatureValue = document.getElementById('temperatureValue');
        
        temperatureSlider.addEventListener('input', function() {
            params.temperature = parseInt(this.value);
            const labels = ['低', '中', '高'];
            temperatureValue.textContent = labels[params.temperature - 1];
        });

        // 催化剂开关
        const catalystToggle = document.getElementById('catalystToggle');
        const catalystStatus = document.getElementById('catalystStatus');
        
        catalystToggle.addEventListener('change', function() {
            params.catalyst = this.checked;
            catalystStatus.textContent = params.catalyst ? '开启' : '关闭';
            catalystStatus.style.color = params.catalyst ? '#4caf50' : '#4fc3f7';
        });

        // 窗口大小变化时调整Canvas
        window.addEventListener('resize', function() {
            resizeCanvas();
            initMolecules();
        });

        // 初始化
        resizeCanvas();
        initMolecules();
        updateEnergyScale();
        
        // 初始绘制
        drawGrid();
        molecules.forEach(mol => mol.draw());
        updateStats(0);
        
        // 自动开始模拟
        setTimeout(startSimulation, 1000);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 《化学反应速率影响因素》交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过直观的微观分子碰撞模型，帮助您深入理解浓度、温度、催化剂如何影响化学反应速率。请跟随本指南，开启您的化学探索之旅。

---

### 一、 功能说明

本动画基于化学**碰撞理论**，将抽象的化学反应速率概念转化为可视化的动态模拟。您将看到一个由红、蓝分子构成的微观世界，通过调整实验参数，实时观察分子运动、碰撞及反应过程，并获取关键数据，从而直观理解宏观反应速率背后的微观机理。

---

### 二、 主要功能与操作

#### 1. **模拟控制区**
*   **开始模拟**：启动分子运动与碰撞模拟。
*   **暂停**：暂停当前模拟，便于仔细观察某一瞬间的微观状态。
*   **重置**：清空所有数据，并根据当前参数重新生成分子，开始新一轮实验。

#### 2. **影响因素调节区**
这是本动画的核心交互部分，您可以像在实验室中一样控制三个关键变量：
*   **浓度滑块**：控制反应容器中分子的总数量。向右滑动增加浓度，向左滑动降低浓度。
*   **温度滑块**：控制分子的平均动能。分为“低”、“中”、“高”三档，温度越高，分子运动越剧烈。
*   **催化剂开关**：开启或关闭催化剂。开启后，将显著降低反应所需的活化能。

#### 3. **实时数据面板**
模拟过程中，以下数据将动态更新：
*   **总碰撞次数**：所有分子间发生的碰撞总数。
*   **有效碰撞次数**：满足能量要求（达到活化能）并成功引发反应的碰撞次数。
*   **反应速率**：单位时间内（每秒）发生的有效碰撞次数，是宏观反应速率的直接体现。
*   **生成物数量**：当前已通过反应生成的紫色分子数量。

#### 4. **微观可视化区域**
*   **分子运动**：红色和蓝色小球分别代表两种不同的反应物分子，它们进行无规则热运动。
*   **碰撞与反应**：
    *   普通碰撞：分子接触时会出现白色闪光。
    *   **有效碰撞**：当碰撞动能足够大时，会触发亮青色闪光，并在碰撞中心生成一个**紫色生成物分子**，这是本动画最重要的视觉反馈。
*   **能量标尺**：右侧的竖条是能量标尺。
    *   **橙色实线**：代表常规条件下的**活化能阈值**。
    *   **绿色虚线**（催化剂开启时显示）：代表催化剂作用下的**降低后的活化能阈值**。分子碰撞时的动能需要超过阈值线，才能成为有效碰撞。

---

### 三、 设计特色

1.  **科学性与直观性并重**：严格依据碰撞理论设计算法，同时通过色彩、闪光、动态数据等元素，将“有效碰撞频率”这一核心概念变得清晰可见。
2.  **对比探究式学习**：鼓励您采用“控制变量法”进行探究。例如，固定温度和催化剂，只改变浓度，观察数据变化，自主归纳结论。
3.  **多感官信息整合**：结合视觉动画（分子运动、颜色变化）、动态数据流和交互操作，形成立体化的学习体验，加深记忆与理解。
4.  **即时反馈机制**：任何参数调整都会立即在模拟画面和数据上得到反馈，帮助您快速建立“因-果”联系。

---

### 四、 教学要点与探究建议

通过操作本动画，您可以验证并深入理解以下核心知识点：

#### **探究活动一：浓度的影响**
*   **操作**：将温度和催化剂设为固定值（如“中温”、催化剂“关闭”），逐步增大浓度滑块。
*   **观察与思考**：
    *   分子数量如何变化？空间是否变得更“拥挤”？
    *   “总碰撞次数”和“有效碰撞次数”如何变化？**反应速率**如何变化？
*   **结论归纳**：增加浓度 → 单位体积内分子数增多 → **碰撞频率**增加 → 有效碰撞频率增加 → 反应速率加快。

#### **探究活动二：温度的影响**
*   **操作**：固定浓度和催化剂状态，将温度从“低”逐步调至“高”。
*   **观察与思考**：
    *   分子的平均运动速度如何变化？
    *   观察能量标尺，思考为什么更多分子能越过活化能阈值（橙色线）？
    *   “有效碰撞次数”的增长幅度是否比“总碰撞次数”更大？这说明了什么？
*   **结论归纳**：升高温度 → 分子平均动能增大 → **更多分子达到或超过活化能** → **有效碰撞的比例和频率**都显著增加 → 反应速率急剧加快。

#### **探究活动三：催化剂的影响**
*   **操作**：固定浓度和温度，点击打开“催化剂开关”。
*   **观察与思考**：
    *   能量标尺上出现了什么新的线（绿色虚线）？它意味着什么？
    *   在分子动能分布不变的情况下，为什么“有效碰撞次数”会突然增加？
    *   催化剂本身（在动画中表现为一条更低的能量门槛）是否被消耗？
*   **结论归纳**：使用催化剂 → **降低反应的活化能** → 使更多碰撞成为有效碰撞 → **有效碰撞比例大幅提高** → 反应速率显著加快，而催化剂本身的性质和质量在反应前后不变。

---

### 五、 使用建议

1.  **分步探究**：建议初次使用时，按照上述“探究活动”顺序，逐一研究三个因素，避免同时改变多个变量导致混淆。
2.  **提出假设**：在调整每个滑块前，先根据所学知识预测一下画面和数据会如何变化，然后再验证。
3.  **关注对比**：充分利用“重置”和“暂停”功能，对比不同参数下的模拟结果，差异是理解的钥匙。
4.  **关联宏观与微观**：时刻将屏幕上微观分子的“有效碰撞频率”与右侧数据面板中的宏观“反应速率”联系起来，这是本动画教学的核心目标。
5.  **教学应用**：
    *   **学生自学**：可作为课前预习或课后巩固的探究工具。
    *   **课堂演示**：教师可在大屏幕上进行操作和讲解，引导全班同学观察与讨论。
    *   **小组探究**：布置探究任务，让学生以小组形式完成实验报告（记录了不同条件下的数据并得出结论）。

希望本交互式动画能成为您理解化学反应动力学的得力助手，祝您探索愉快，收获满满！