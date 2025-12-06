# 需求：酸碱中和反应的微观本质（H⁺ + OH⁻ → H₂O）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中或高中化学初学者。他们已具备原子、离子、化学反应的基本概念，但需要将宏观的酸碱中和现象（如颜色变化、放热）与微观的粒子行为联系起来。
2.  **核心痛点**：学生难以在脑海中动态、可视化地想象溶液中离子如何移动、碰撞并结合。抽象的离子符号（H⁺， OH⁻）和方程式（H⁺ + OH⁻ → H₂O）缺乏直观性。
3.  **学习目标**：
    *   **知识层面**：理解酸碱中和反应的微观本质是氢离子（H⁺）与氢氧根离子（OH⁻）结合生成水分子（H₂O）。
    *   **能力层面**：能够用粒子模型描述和解释中和反应的过程。
    *   **情感层面**：通过直观有趣的动画，降低对微观世界理解的畏惧感，激发学习兴趣。

#### 教学设计思路
1.  **核心概念聚焦**：动画将紧紧围绕 `H⁺ + OH⁻ → H₂O` 这一核心展开，避免引入过多副反应或复杂离子（如Na⁺， Cl⁻）的干扰，确保信息清晰。
2.  **遵循认知规律**：
    *   **从宏观到微观**：动画起始于两个烧杯（酸和碱），点击后“放大”进入微观粒子视图。
    *   **从静态到动态**：先展示反应前离子的静态分布，再动态演示离子运动、碰撞与结合。
    *   **从现象到本质**：通过离子数量的动态减少和水分子的生成，直观对应宏观现象中“酸碱性质消失”。
3.  **交互设计**：
    *   **控制节奏**：允许用户通过“播放/暂停/重置”按钮控制动画，以适应个人学习速度。
    *   **主动探索**：设计“高亮H⁺/OH⁻”的开关，让用户可以聚焦观察特定离子的轨迹。
    *   **过程揭示**：设计“逐步演示”模式，将反应分解为“自由移动”、“相遇碰撞”、“结合成水”等步骤，并配以文字说明。
4.  **视觉呈现**：
    *   **符号化与拟人化结合**：采用国际通用的球棍模型表示水分子（H₂O）。对于H⁺和OH⁻，为了强调其带电性和反应核心，可以采用**颜色鲜艳的发光小球**（如H⁺为红色闪烁小球，OH⁻为蓝色闪烁小球），使其在众多背景离子中脱颖而出。
    *   **运动设计**：离子做无规则布朗运动，当H⁺与OH⁻进入一定“反应半径”时，设计一个吸引、碰撞的动画，然后“融合”转变为一个水分子模型。
    *   **计数可视化**：在画面一侧动态显示 `H⁺`、`OH⁻` 的数量和生成的 `H₂O` 数量，将粒子变化量化。

#### 配色方案选择
*   **主色调与科学象征**：
    *   **H⁺（氢离子）**：采用**亮红色**（#FF375B）。红色通常与“酸”的警示、活泼性关联。
    *   **OH⁻（氢氧根离子）**：采用**钴蓝色**（#2A5CFF）。蓝色常与“碱”的冷静、相反属性关联。
    *   **H₂O（水分子）**：采用**浅蓝灰色**（#88C1E3）球棍模型，表示中性、稳定的生成物。
    *   **背景离子（如Na⁺， Cl⁻）**：使用**半透明的浅灰色**（#AAAAAA80），确保它们存在但不抢镜，突出反应主体。
*   **背景与环境**：
    *   画布背景使用**深空蓝**（#0F1A2F）或**深灰**（#2C3E50），模拟微观世界的深邃感，并能强烈衬托出前方发光的离子。
    *   控制面板使用浅色卡片背景（#FFFFFF with opacity），确保清晰可读。
*   **交互状态色**：
    *   按钮悬停/激活状态使用主色的变体（如红色变橙，蓝色变亮蓝）。
    *   “高亮”模式时，被追踪的离子外围可增加**脉冲光晕**。

#### 交互功能列表
1.  **主控面板**：
    *   `播放 / 暂停`：开始或暂停动画。
    *   `重置`：将所有粒子恢复至初始状态。
    *   `步骤演示`：将连续动画分解为几个关键步骤，点击按钮逐步推进。
2.  **视角切换**：
    *   `宏观视图`：显示两个烧杯（标有“HCl溶液”和“NaOH溶液”）相混合的示意动画。
    *   `微观视图`（默认）：点击烧杯后进入，展示溶液中离子的运动。
3.  **粒子显示控制**：
    *   `高亮 H⁺` 开关：开启后，所有H⁺离子高亮显示（如加大光晕），其他粒子变暗。
    *   `高亮 OH⁻` 开关：功能同上，针对OH⁻离子。
    *   `显示/隐藏背景离子`：切换Na⁺、Cl⁻等“旁观离子”的显示，帮助聚焦核心反应。
4.  **动态信息面板**：
    *   实时显示：`剩余 H⁺：`、`剩余 OH⁻：`、`已生成 H₂O：` 的数量。
    *   在“步骤演示”模式下，显示当前步骤的文字解说（如：“步骤1：酸和碱溶液中含有大量自由的H⁺和OH⁻离子”）。
5.  **化学反应方程式面板**：
    *   在画面显眼位置悬浮显示 `H⁺ + OH⁻ → H₂O`。
    *   在反应进行时，方程式中的符号可以伴有微弱的发光效果，增强关联性。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>酸碱中和反应微观本质动画 | H⁺ + OH⁻ → H₂O</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #1a2a3a 0%, #0f1a2f 100%);
            color: #e0e0e0;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .header {
            text-align: center;
            margin-bottom: 25px;
            max-width: 900px;
            width: 100%;
        }

        h1 {
            color: #ffffff;
            margin-bottom: 10px;
            font-size: 2.5rem;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }

        .subtitle {
            font-size: 1.2rem;
            color: #88C1E3;
            margin-bottom: 15px;
        }

        .equation {
            font-size: 2.8rem;
            font-weight: bold;
            background: rgba(255, 255, 255, 0.1);
            padding: 15px 30px;
            border-radius: 12px;
            display: inline-block;
            margin: 15px 0;
            border: 2px solid rgba(136, 193, 227, 0.3);
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            max-width: 1200px;
            width: 100%;
            justify-content: center;
        }

        .canvas-container {
            flex: 1;
            min-width: 600px;
            background-color: rgba(15, 26, 47, 0.8);
            border-radius: 16px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(255, 255, 255, 0.05);
            display: flex;
            flex-direction: column;
        }

        .canvas-title {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .view-toggle {
            display: flex;
            gap: 10px;
        }

        .view-btn {
            padding: 8px 16px;
            border: none;
            border-radius: 6px;
            background: rgba(255, 255, 255, 0.1);
            color: #e0e0e0;
            cursor: pointer;
            transition: all 0.3s;
        }

        .view-btn.active {
            background: #2A5CFF;
            color: white;
            font-weight: bold;
        }

        .view-btn:hover:not(.active) {
            background: rgba(255, 255, 255, 0.2);
        }

        canvas {
            background-color: rgba(15, 26, 47, 0.9);
            border-radius: 12px;
            width: 100%;
            flex-grow: 1;
            display: block;
            cursor: pointer;
        }

        .controls-container {
            width: 350px;
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .panel {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 16px;
            padding: 22px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .panel h2 {
            color: #88C1E3;
            margin-bottom: 18px;
            font-size: 1.4rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .panel h2 i {
            font-size: 1.2rem;
        }

        .button-group {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            margin-bottom: 15px;
        }

        .btn {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            flex: 1;
            min-width: 120px;
        }

        .btn-primary {
            background: linear-gradient(135deg, #2A5CFF 0%, #1a4ae0 100%);
            color: white;
        }

        .btn-primary:hover {
            background: linear-gradient(135deg, #3a6cff 0%, #2a5af0 100%);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(42, 92, 255, 0.4);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.1);
            color: #e0e0e0;
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-2px);
        }

        .btn-danger {
            background: linear-gradient(135deg, #FF375B 0%, #e01a40 100%);
            color: white;
        }

        .btn-danger:hover {
            background: linear-gradient(135deg, #FF476B 0%, #f02a50 100%);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 55, 91, 0.4);
        }

        .toggle-group {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .toggle-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .toggle-item:last-child {
            border-bottom: none;
        }

        .toggle-label {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .ion-preview {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            display: inline-block;
        }

        .h-plus-preview {
            background: radial-gradient(circle at 30% 30%, #FF375B, #b30024);
            box-shadow: 0 0 10px #FF375B;
        }

        .oh-minus-preview {
            background: radial-gradient(circle at 30% 30%, #2A5CFF, #0a2a9e);
            box-shadow: 0 0 10px #2A5CFF;
        }

        .water-preview {
            width: 30px;
            height: 20px;
            background: #88C1E3;
            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
        }

        .toggle-switch {
            position: relative;
            display: inline-block;
            width: 54px;
            height: 28px;
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
            background-color: rgba(255, 255, 255, 0.2);
            transition: .4s;
            border-radius: 34px;
        }

        .toggle-slider:before {
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

        input:checked + .toggle-slider {
            background-color: #2A5CFF;
        }

        input:checked + .toggle-slider:before {
            transform: translateX(26px);
        }

        .stats {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .stat-item {
            background: rgba(0, 0, 0, 0.2);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .stat-value {
            font-size: 2.2rem;
            font-weight: bold;
            margin: 5px 0;
        }

        .h-plus-stat {
            color: #FF375B;
            text-shadow: 0 0 8px rgba(255, 55, 91, 0.5);
        }

        .oh-minus-stat {
            color: #2A5CFF;
            text-shadow: 0 0 8px rgba(42, 92, 255, 0.5);
        }

        .water-stat {
            color: #88C1E3;
            text-shadow: 0 0 8px rgba(136, 193, 227, 0.5);
            grid-column: span 2;
        }

        .step-info {
            background: rgba(0, 0, 0, 0.2);
            padding: 18px;
            border-radius: 10px;
            border-left: 4px solid #88C1E3;
            margin-top: 10px;
            min-height: 80px;
            display: flex;
            align-items: center;
        }

        .legend {
            display: flex;
            justify-content: space-around;
            margin-top: 15px;
            flex-wrap: wrap;
            gap: 15px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
        }

        .footer {
            margin-top: 30px;
            text-align: center;
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
            max-width: 900px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        @media (max-width: 1100px) {
            .container {
                flex-direction: column;
                align-items: center;
            }
            
            .canvas-container, .controls-container {
                width: 100%;
                min-width: unset;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>酸碱中和反应的微观本质</h1>
        <div class="subtitle">可视化探索氢离子与氢氧根离子如何结合生成水分子</div>
        <div class="equation">H⁺ + OH⁻ → H₂O</div>
    </div>

    <div class="container">
        <div class="canvas-container">
            <div class="canvas-title">
                <h2>反应可视化区域</h2>
                <div class="view-toggle">
                    <button id="macroViewBtn" class="view-btn">宏观视图</button>
                    <button id="microViewBtn" class="view-btn active">微观视图</button>
                </div>
            </div>
            <canvas id="reactionCanvas" width="800" height="600"></canvas>
        </div>

        <div class="controls-container">
            <div class="panel">
                <h2>🎬 动画控制</h2>
                <div class="button-group">
                    <button id="playBtn" class="btn btn-primary">
                        <span>▶️ 播放</span>
                    </button>
                    <button id="pauseBtn" class="btn btn-secondary">
                        <span>⏸️ 暂停</span>
                    </button>
                    <button id="resetBtn" class="btn btn-danger">
                        <span>🔄 重置</span>
                    </button>
                </div>
                <div class="button-group">
                    <button id="step1Btn" class="btn btn-secondary">步骤1: 初始状态</button>
                    <button id="step2Btn" class="btn btn-secondary">步骤2: 离子运动</button>
                    <button id="step3Btn" class="btn btn-secondary">步骤3: 碰撞结合</button>
                    <button id="step4Btn" class="btn btn-secondary">步骤4: 反应完成</button>
                </div>
                <div class="step-info" id="stepInfo">
                    点击"播放"按钮开始动画，或使用"步骤演示"分步学习。
                </div>
            </div>

            <div class="panel">
                <h2>🔍 粒子显示控制</h2>
                <div class="toggle-group">
                    <div class="toggle-item">
                        <div class="toggle-label">
                            <div class="ion-preview h-plus-preview"></div>
                            <span>高亮 H⁺ 离子</span>
                        </div>
                        <label class="toggle-switch">
                            <input type="checkbox" id="highlightHPlus">
                            <span class="toggle-slider"></span>
                        </label>
                    </div>
                    <div class="toggle-item">
                        <div class="toggle-label">
                            <div class="ion-preview oh-minus-preview"></div>
                            <span>高亮 OH⁻ 离子</span>
                        </div>
                        <label class="toggle-switch">
                            <input type="checkbox" id="highlightOHMinus">
                            <span class="toggle-slider"></span>
                        </label>
                    </div>
                    <div class="toggle-item">
                        <div class="toggle-label">
                            <div class="ion-preview" style="background: #AAAAAA;"></div>
                            <span>显示背景离子 (Na⁺, Cl⁻)</span>
                        </div>
                        <label class="toggle-switch">
                            <input type="checkbox" id="showBackgroundIons" checked>
                            <span class="toggle-slider"></span>
                        </label>
                    </div>
                </div>
            </div>

            <div class="panel">
                <h2>📊 反应实时数据</h2>
                <div class="stats">
                    <div class="stat-item">
                        <div>剩余 H⁺</div>
                        <div id="hPlusCount" class="stat-value h-plus-stat">20</div>
                        <div>氢离子</div>
                    </div>
                    <div class="stat-item">
                        <div>剩余 OH⁻</div>
                        <div id="ohMinusCount" class="stat-value oh-minus-stat">20</div>
                        <div>氢氧根离子</div>
                    </div>
                    <div class="stat-item water-stat">
                        <div>已生成 H₂O</div>
                        <div id="waterCount" class="stat-value">0</div>
                        <div>水分子</div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="legend">
        <div class="legend-item">
            <div class="ion-preview h-plus-preview"></div>
            <span>H⁺ 氢离子 (来自酸)</span>
        </div>
        <div class="legend-item">
            <div class="ion-preview oh-minus-preview"></div>
            <span>OH⁻ 氢氧根离子 (来自碱)</span>
        </div>
        <div class="legend-item">
            <div class="water-preview"></div>
            <span>H₂O 水分子 (反应产物)</span>
        </div>
        <div class="legend-item">
            <div class="ion-preview" style="background: #AAAAAA;"></div>
            <span>背景离子 (Na⁺, Cl⁻)</span>
        </div>
    </div>

    <div class="footer">
        <p>教学动画设计：酸碱中和反应微观本质 | H⁺ + OH⁻ → H₂O | 使用HTML5 Canvas实现</p>
        <p>提示：点击微观视图中的离子可以手动触发反应，尝试点击一个H⁺和一个OH⁻离子！</p>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('reactionCanvas');
        const ctx = canvas.getContext('2d');

        // 调整Canvas大小以适应容器
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight * 0.9;
            initParticles();
        }

        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();

        // 状态变量
        let animationId = null;
        let isPlaying = false;
        let currentStep = 0;
        let isMacroView = false;

        // 粒子系统
        const particles = {
            hPlus: [],    // H⁺离子
            ohMinus: [],  // OH⁻离子
            water: [],    // 水分子
            background: [] // 背景离子
        };

        // 配置
        const config = {
            totalHParticles: 20,
            totalOHParticles: 20,
            totalBackgroundParticles: 15,
            reactionRadius: 25,
            particleSpeed: 1.5,
            highlightHPlus: false,
            highlightOHMinus: false,
            showBackgroundIons: true
        };

        // 步骤说明
        const stepDescriptions = [
            "步骤1: 初始状态 - 酸溶液中含有H⁺离子，碱溶液中含有OH⁻离子，它们均匀分布在溶液中。",
            "步骤2: 离子运动 - H⁺和OH⁻离子在溶液中做无规则运动，当它们相互靠近时可能发生碰撞。",
            "步骤3: 碰撞结合 - H⁺和OH⁻离子碰撞后结合，形成水分子(H₂O)。这是一个放热反应。",
            "步骤4: 反应完成 - 当所有H⁺和OH⁻离子都结合后，反应完成，溶液中只剩下水分子和背景离子。"
        ];

        // 粒子类
        class Particle {
            constructor(x, y, type) {
                this.x = x;
                this.y = y;
                this.type = type; // 'hPlus', 'ohMinus', 'water', 'background'
                this.vx = (Math.random() - 0.5) * config.particleSpeed;
                this.vy = (Math.random() - 0.5) * config.particleSpeed;
                this.radius = type === 'water' ? 12 : 10;
                this.active = true;
                this.highlight = false;
                this.pulse = 0;
                this.pulseDirection = 1;
                
                // 设置颜色
                switch(type) {
                    case 'hPlus':
                        this.color = '#FF375B';
                        this.glowColor = 'rgba(255, 55, 91, 0.7)';
                        break;
                    case 'ohMinus':
                        this.color = '#2A5CFF';
                        this.glowColor = 'rgba(42, 92, 255, 0.7)';
                        break;
                    case 'water':
                        this.color = '#88C1E3';
                        this.glowColor = 'rgba(136, 193, 227, 0.5)';
                        break;
                    default:
                        this.color = '#AAAAAA';
                        this.glowColor = 'rgba(170, 170, 170, 0.3)';
                }
            }

            update() {
                if (!this.active) return;
                
                // 更新位置
                this.x += this.vx;
                this.y += this.vy;
                
                // 边界碰撞
                if (this.x < this.radius || this.x > canvas.width - this.radius) {
                    this.vx = -this.vx;
                    this.x = this.x < this.radius ? this.radius : canvas.width - this.radius;
                }
                if (this.y < this.radius || this.y > canvas.height - this.radius) {
                    this.vy = -this.vy;
                    this.y = this.y < this.radius ? this.radius : canvas.height - this.radius;
                }
                
                // 更新脉冲效果
                if (this.highlight) {
                    this.pulse += 0.05 * this.pulseDirection;
                    if (this.pulse > 1 || this.pulse < 0) {
                        this.pulseDirection *= -1;
                    }
                }
            }

            draw() {
                if (!this.active) return;
                
                ctx.save();
                
                // 绘制发光效果
                if ((this.type === 'hPlus' && config.highlightHPlus) || 
                    (this.type === 'ohMinus' && config.highlightOHMinus) ||
                    this.highlight) {
                    
                    const glowRadius = this.radius + 5 + (this.highlight ? this.pulse * 5 : 0);
                    const gradient = ctx.createRadialGradient(
                        this.x, this.y, 0,
                        this.x, this.y, glowRadius
                    );
                    
                    gradient.addColorStop(0, this.glowColor);
                    gradient.addColorStop(1, 'transparent');
                    
                    ctx.fillStyle = gradient;
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, glowRadius, 0, Math.PI * 2);
                    ctx.fill();
                }
                
                // 绘制粒子主体
                if (this.type === 'water') {
                    // 绘制水分子（椭圆形）
                    ctx.fillStyle = this.color;
                    ctx.beginPath();
                    ctx.ellipse(this.x, this.y, this.radius, this.radius * 0.7, 0, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 绘制水分子中的"H₂O"文字
                    ctx.fillStyle = '#0F1A2F';
                    ctx.font = 'bold 10px Arial';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText('H₂O', this.x, this.y);
                } else {
                    // 绘制离子（圆形）
                    const gradient = ctx.createRadialGradient(
                        this.x - this.radius/3, this.y - this.radius/3, 0,
                        this.x, this.y, this.radius
                    );
                    
                    if (this.type === 'hPlus') {
                        gradient.addColorStop(0, '#FF6B8B');
                        gradient.addColorStop(1, '#FF375B');
                    } else if (this.type === 'ohMinus') {
                        gradient.addColorStop(0, '#5A7CFF');
                        gradient.addColorStop(1, '#2A5CFF');
                    } else {
                        gradient.addColorStop(0, '#CCCCCC');
                        gradient.addColorStop(1, '#AAAAAA');
                    }
                    
                    ctx.fillStyle = gradient;
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 绘制离子符号
                    ctx.fillStyle = '#FFFFFF';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    
                    let symbol = '';
                    if (this.type === 'hPlus') symbol = 'H⁺';
                    else if (this.type === 'ohMinus') symbol = 'OH⁻';
                    else if (this.type === 'background') symbol = Math.random() > 0.5 ? 'Na⁺' : 'Cl⁻';
                    
                    ctx.fillText(symbol, this.x, this.y);
                }
                
                ctx.restore();
            }

            isPointInside(x, y) {
                const distance = Math.sqrt((x - this.x) ** 2 + (y - this.y) ** 2);
                return distance <= this.radius;
            }
        }

        // 初始化粒子
        function initParticles() {
            particles.hPlus = [];
            particles.ohMinus = [];
            particles.water = [];
            particles.background = [];
            
            // 创建H⁺离子（左侧区域）
            for (let i = 0; i < config.totalHParticles; i++) {
                const x = Math.random() * (canvas.width / 2 - 50) + 30;
                const y = Math.random() * (canvas.height - 60) + 30;
                particles.hPlus.push(new Particle(x, y, 'hPlus'));
            }
            
            // 创建OH⁻离子（右侧区域）
            for (let i = 0; i < config.totalOHParticles; i++) {
                const x = Math.random() * (canvas.width / 2 - 50) + canvas.width / 2 + 20;
                const y = Math.random() * (canvas.height - 60) + 30;
                particles.ohMinus.push(new Particle(x, y, 'ohMinus'));
            }
            
            // 创建背景离子
            for (let i = 0; i < config.totalBackgroundParticles; i++) {
                const x = Math.random() * (canvas.width - 60) + 30;
                const y = Math.random() * (canvas.height - 60) + 30;
                particles.background.push(new Particle(x, y, 'background'));
            }
            
            updateStats();
        }

        // 检查并处理反应
        function checkReactions() {
            for (let i = particles.hPlus.length - 1; i >= 0; i--) {
                const hPlus = particles.hPlus[i];
                if (!hPlus.active) continue;
                
                for (let j = particles.ohMinus.length - 1; j >= 0; j--) {
                    const ohMinus = particles.ohMinus[j];
                    if (!ohMinus.active) continue;
                    
                    const distance = Math.sqrt(
                        (hPlus.x - ohMinus.x) ** 2 + (hPlus.y - ohMinus.y) ** 2
                    );
                    
                    if (distance < config.reactionRadius && isPlaying) {
                        // 创建水分子
                        const waterX = (hPlus.x + ohMinus.x) / 2;
                        const waterY = (hPlus.y + ohMinus.y) / 2;
                        particles.water.push(new Particle(waterX, waterY, 'water'));
                        
                        // 移除反应离子
                        hPlus.active = false;
                        ohMinus.active = false;
                        
                        updateStats();
                        break;
                    }
                }
            }
        }

        // 更新统计信息
        function updateStats() {
            const activeHPlus = particles.hPlus.filter(p => p.active).length;
            const activeOHMinus = particles.ohMinus.filter(p => p.active).length;
            
            document.getElementById('hPlusCount').textContent = activeHPlus;
            document.getElementById('ohMinusCount').textContent = activeOHMinus;
            document.getElementById('waterCount').textContent = particles.water.length;
        }

        // 绘制宏观视图
        function drawMacroView() {
            // 清空画布
            ctx.fillStyle = '#0F1A2F';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制标题
            ctx.fillStyle = '#FFFFFF';
            ctx.font = 'bold 24px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('酸碱中和反应 - 宏观视图', canvas.width / 2, 40);
            
            // 绘制烧杯
            const beakerWidth = 150;
            const beakerHeight = 200;
            const leftBeakerX = canvas.width / 4 - beakerWidth / 2;
            const rightBeakerX = canvas.width * 3/4 - beakerWidth / 2;
            const beakerY = canvas.height / 2 - beakerHeight / 2 + 30;
            
            // 左烧杯（酸）
            ctx.fillStyle = 'rgba(255, 55, 91, 0.3)';
            ctx.fillRect(leftBeakerX, beakerY, beakerWidth, beakerHeight);
            ctx.strokeStyle = '#FFFFFF';
            ctx.lineWidth = 3;
            ctx.strokeRect(leftBeakerX, beakerY, beakerWidth, beakerHeight);
            
            // 右烧杯（碱）
            ctx.fillStyle = 'rgba(42, 92, 255, 0.3)';
            ctx.fillRect(rightBeakerX, beakerY, beakerWidth, beakerHeight);
            ctx.strokeStyle = '#FFFFFF';
            ctx.strokeRect(rightBeakerX, beakerY, beakerWidth, beakerHeight);
            
            // 烧杯标签
            ctx.fillStyle = '#FF375B';
            ctx.font = 'bold 20px Arial';
            ctx.fillText('HCl 溶液', leftBeakerX + beakerWidth / 2, beakerY - 20);
            
            ctx.fillStyle = '#2A5CFF';
            ctx.fillText('NaOH 溶液', rightBeakerX + beakerWidth / 2, beakerY - 20);
            
            // 绘制混合箭头
            const arrowY = beakerY + beakerHeight / 2;
            ctx.strokeStyle = '#88C1E3';
            ctx.lineWidth = 5;
            ctx.beginPath();
            ctx.moveTo(leftBeakerX + beakerWidth + 20, arrowY);
            ctx.lineTo(rightBeakerX - 20, arrowY);
            
            // 箭头头部
            ctx.lineTo(rightBeakerX - 40, arrowY - 10);
            ctx.moveTo(rightBeakerX - 20, arrowY);
            ctx.lineTo(rightBeakerX - 40, arrowY + 10);
            ctx.stroke();
            
            // 绘制反应方程式
            ctx.fillStyle = '#88C1E3';
            ctx.font = 'bold 32px Arial';
            ctx.fillText('H⁺ + OH⁻ → H₂O', canvas.width / 2, beakerY + beakerHeight + 60);
            
            // 绘制说明文字
            ctx.fillStyle = '#CCCCCC';
            ctx.font = '16px Arial';
            ctx.fillText('点击"微观视图"按钮观察离子级别的反应过程', canvas.width / 2, canvas.height - 30);
        }

        // 绘制微观视图
        function drawMicroView() {
            // 清空画布
            ctx.fillStyle = '#0F1A2F';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制标题和网格
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.05)';
            ctx.lineWidth = 1;
            
            // 绘制网格线
            const gridSize = 40;
            for (let x = 0; x < canvas.width; x += gridSize) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, canvas.height);
                ctx.stroke();
            }
            for (let y = 0; y < canvas.height; y += gridSize) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(canvas.width, y);
                ctx.stroke();
            }
            
            // 绘制区域分隔线
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.2)';
            ctx.lineWidth = 2;
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            ctx.moveTo(canvas.width / 2, 0);
            ctx.lineTo(canvas.width / 2, canvas.height);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制区域标签
            ctx.fillStyle = '#FF375B';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('酸溶液区域 (H⁺)', canvas.width / 4, 30);
            
            ctx.fillStyle = '#2A5CFF';
            ctx.fillText('碱溶液区域 (OH⁻)', canvas.width * 3/4, 30);
            
            // 更新和绘制粒子
            if (isPlaying) {
                checkReactions();
            }
            
            // 绘制背景离子
            if (config.showBackgroundIons) {
                particles.background.forEach(p => {
                    p.update();
                    p.draw();
                });
            }
            
            // 绘制水分子
            particles.water.forEach(p => {
                p.update();
                p.draw();
            });
            
            // 绘制H⁺离子
            particles.hPlus.forEach(p => {
                p.update();
                p.draw();
            });
            
            // 绘制OH⁻离子
            particles.ohMinus.forEach(p => {
                p.update();
                p.draw();
            });
            
            // 绘制反应方程式
            ctx.fillStyle = '#88C1E3';
            ctx.font = 'bold 28px Arial';
            ctx.fillText('H⁺ + OH⁻ → H₂O', canvas.width / 2, canvas.height - 30);
            
            // 绘制反应进度
            const totalReactions = Math.min(config.totalHParticles, config.totalOHParticles);
            const completedReactions = particles.water.length;
            const progress = completedReactions / totalReactions;
            
            if (progress > 0 && progress < 1) {
                ctx.fillStyle = 'rgba(136, 193, 227, 0.2)';
                ctx.fillRect(canvas.width / 2 - 100, canvas.height - 60, 200, 20);
                
                ctx.fillStyle = '#88C1E3';
                ctx.fillRect(canvas.width / 2 - 100, canvas.height - 60, 200 * progress, 20);
                
                ctx.fillStyle = '#FFFFFF';
                ctx.font = '14px Arial';
                ctx.fillText(
                    `反应进度: ${Math.round(progress * 100)}%`, 
                    canvas.width / 2, 
                    canvas.height - 48
                );
            }
        }

        // 动画循环
        function animate() {
            if (isMacroView) {
                drawMacroView();
            } else {
                drawMicroView();
            }
            
            if (isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }

        // 开始动画
        function startAnimation() {
            if (!isPlaying) {
                isPlaying = true;
                document.getElementById('stepInfo').textContent = "动画播放中: 观察H⁺和OH⁻离子如何运动、碰撞并生成水分子。";
                animate();
            }
        }

        // 暂停动画
        function pauseAnimation() {
            isPlaying = false;
            if (animationId) {
                cancelAnimationFrame(animationId);
            }
            document.getElementById('stepInfo').textContent = "动画已暂停。点击播放继续，或使用步骤演示。";
        }

        // 重置动画
        function resetAnimation() {
            pauseAnimation();
            currentStep = 0;
            initParticles();
            document.getElementById('stepInfo').textContent = "已重置。点击播放按钮开始动画，或使用步骤演示。";
            
            if (!isMacroView) {
                animate(); // 绘制静态视图
            }
        }

        // 步骤演示函数
        function goToStep(step) {
            currentStep = step;
            pauseAnimation();
            
            // 根据步骤设置状态
            switch(step) {
                case 1: // 初始状态
                    resetAnimation();
                    document.getElementById('stepInfo').textContent = stepDescriptions[0];
                    break;
                case 2: // 离子运动
                    resetAnimation();
                    isPlaying = true;
                    document.getElementById('stepInfo').textContent = stepDescriptions[1];
                    animate();

<!--检测到代码截断，自动续写中...-->
                    setTimeout(() => pauseAnimation(), 2000);
                    break;
                case 3: // 碰撞结合
                    resetAnimation();
                    // 让一些离子靠近以便碰撞
                    particles.hPlus.forEach((p, i) => {
                        if (i < 8) {
                            p.x = canvas.width / 2 - 50 + i * 10;
                            p.y = canvas.height / 2;
                            p.vx = 1;
                        }
                    });
                    
                    particles.ohMinus.forEach((p, i) => {
                        if (i < 8) {
                            p.x = canvas.width / 2 + 50 - i * 10;
                            p.y = canvas.height / 2;
                            p.vx = -1;
                        }
                    });
                    
                    isPlaying = true;
                    document.getElementById('stepInfo').textContent = stepDescriptions[2];
                    animate();
                    setTimeout(() => pauseAnimation(), 3000);
                    break;
                case 4: // 反应完成
                    resetAnimation();
                    // 手动触发所有反应
                    particles.hPlus.forEach(p => {
                        if (p.active) {
                            p.active = false;
                            const waterX = p.x;
                            const waterY = p.y;
                            particles.water.push(new Particle(waterX, waterY, 'water'));
                        }
                    });
                    
                    particles.ohMinus.forEach(p => {
                        if (p.active) p.active = false;
                    });
                    
                    updateStats();
                    document.getElementById('stepInfo').textContent = stepDescriptions[3];
                    animate();
                    break;
            }
        }

        // 切换视图
        function switchView(isMacro) {
            isMacroView = isMacro;
            
            if (isMacro) {
                document.getElementById('macroViewBtn').classList.add('active');
                document.getElementById('microViewBtn').classList.remove('active');
                pauseAnimation();
                drawMacroView();
            } else {
                document.getElementById('macroViewBtn').classList.remove('active');
                document.getElementById('microViewBtn').classList.add('active');
                drawMicroView();
            }
        }

        // 处理Canvas点击（手动触发反应）
        canvas.addEventListener('click', function(event) {
            if (isMacroView) {
                // 在宏观视图中点击切换到微观视图
                switchView(false);
                return;
            }
            
            const rect = canvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;
            
            // 查找点击的H⁺离子
            let clickedHPlus = null;
            for (let i = 0; i < particles.hPlus.length; i++) {
                if (particles.hPlus[i].active && particles.hPlus[i].isPointInside(x, y)) {
                    clickedHPlus = particles.hPlus[i];
                    clickedHPlus.highlight = true;
                    break;
                }
            }
            
            // 查找点击的OH⁻离子
            let clickedOHMinus = null;
            for (let i = 0; i < particles.ohMinus.length; i++) {
                if (particles.ohMinus[i].active && particles.ohMinus[i].isPointInside(x, y)) {
                    clickedOHMinus = particles.ohMinus[i];
                    clickedOHMinus.highlight = true;
                    break;
                }
            }
            
            // 如果点击了一个H⁺和一个OH⁻，让它们反应
            if (clickedHPlus && clickedOHMinus) {
                // 创建水分子
                const waterX = (clickedHPlus.x + clickedOHMinus.x) / 2;
                const waterY = (clickedHPlus.y + clickedOHMinus.y) / 2;
                particles.water.push(new Particle(waterX, waterY, 'water'));
                
                // 移除反应离子
                clickedHPlus.active = false;
                clickedOHMinus.active = false;
                
                updateStats();
                
                // 移除高亮效果
                setTimeout(() => {
                    if (clickedHPlus) clickedHPlus.highlight = false;
                    if (clickedOHMinus) clickedOHMinus.highlight = false;
                }, 1000);
            } else if (clickedHPlus || clickedOHMinus) {
                // 如果只点击了一个离子，稍后移除高亮
                setTimeout(() => {
                    if (clickedHPlus) clickedHPlus.highlight = false;
                    if (clickedOHMinus) clickedOHMinus.highlight = false;
                }, 1000);
            }
        });

        // 事件监听器设置
        document.getElementById('playBtn').addEventListener('click', startAnimation);
        document.getElementById('pauseBtn').addEventListener('click', pauseAnimation);
        document.getElementById('resetBtn').addEventListener('click', resetAnimation);
        
        document.getElementById('step1Btn').addEventListener('click', () => goToStep(1));
        document.getElementById('step2Btn').addEventListener('click', () => goToStep(2));
        document.getElementById('step3Btn').addEventListener('click', () => goToStep(3));
        document.getElementById('step4Btn').addEventListener('click', () => goToStep(4));
        
        document.getElementById('macroViewBtn').addEventListener('click', () => switchView(true));
        document.getElementById('microViewBtn').addEventListener('click', () => switchView(false));
        
        document.getElementById('highlightHPlus').addEventListener('change', function() {
            config.highlightHPlus = this.checked;
        });
        
        document.getElementById('highlightOHMinus').addEventListener('change', function() {
            config.highlightOHMinus = this.checked;
        });
        
        document.getElementById('showBackgroundIons').addEventListener('change', function() {
            config.showBackgroundIons = this.checked;
        });

        // 初始化
        initParticles();
        animate(); // 初始绘制

        // 键盘快捷键
        document.addEventListener('keydown', function(event) {
            switch(event.key) {
                case ' ':
                    // 空格键切换播放/暂停
                    if (isPlaying) {
                        pauseAnimation();
                    } else {
                        startAnimation();
                    }
                    event.preventDefault();
                    break;
                case 'r':
                case 'R':
                    // R键重置
                    resetAnimation();
                    break;
                case '1':
                    goToStep(1);
                    break;
                case '2':
                    goToStep(2);
                    break;
                case '3':
                    goToStep(3);
                    break;
                case '4':
                    goToStep(4);
                    break;
            }
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 酸碱中和反应微观本质交互式教学动画使用指南

欢迎使用“酸碱中和反应微观本质”交互式教学动画！本动画旨在通过直观、动态的可视化方式，帮助您深入理解酸碱中和反应的核心过程：**H⁺ + OH⁻ → H₂O**。无论您是教师、学生还是化学爱好者，本工具都将为您提供沉浸式的学习体验。

---

### 一、功能说明

本动画是一个基于HTML5 Canvas技术构建的交互式教学工具，包含以下核心模块：

1.  **可视化区域**：左侧主画布，动态展示反应的宏观与微观过程。
2.  **控制面板**：右侧功能区，提供动画控制、粒子显示设置和实时数据监控。
3.  **视图切换**：可在“宏观视图”（烧杯混合示意）和“微观视图”（离子运动模拟）间自由切换。
4.  **交互式学习**：支持点击粒子手动触发反应，通过控制节奏和焦点进行探索性学习。

---

### 二、主要功能

#### 1. 动画控制区
*   **播放/暂停**：控制动画的连续运行与暂停，便于仔细观察关键帧。
*   **重置**：一键恢复所有粒子至初始状态，方便重复学习。
*   **步骤演示**：将复杂的连续反应分解为四个逻辑步骤，支持分步学习：
    *   **步骤1：初始状态** - 展示反应前酸、碱溶液中离子的分布。
    *   **步骤2：离子运动** - 观察H⁺和OH⁻离子在溶液中的无规则布朗运动。
    *   **步骤3：碰撞结合** - 聚焦于离子进入反应半径后，结合生成水分子的瞬间。
    *   **步骤4：反应完成** - 展示反应终点，溶液中仅剩水分子和背景离子。

#### 2. 粒子显示控制区
*   **高亮 H⁺/OH⁻**：开启后，特定离子类型将显示脉冲光晕，使其在众多粒子中脱颖而出，便于追踪其运动轨迹和命运。
*   **显示/隐藏背景离子**：可切换钠离子（Na⁺）和氯离子（Cl⁻）等“旁观者”的显示，帮助您排除干扰，聚焦于核心反应粒子。

#### 3. 实时数据面板
动态显示反应进程中的关键量化数据：
*   **剩余 H⁺数量**
*   **剩余 OH⁻数量**
*   **已生成 H₂O数量**
这些数据与可视化过程同步更新，将微观的粒子变化与宏观的计量关系直观联系起来。

#### 4. 交互探索
*   在**微观视图**下，您可以**直接用鼠标点击画布中的H⁺和OH⁻离子**。
*   当您同时点击一个H⁺和一个OH⁻离子时，动画将立即模拟它们结合生成一个水分子。这是一个强大的探索工具，让您亲手“驱动”化学反应。

---

### 三、设计特色

1.  **科学的视觉编码**：
    *   **H⁺离子**：采用**亮红色**及发光效果，象征酸的活泼性与酸性。
    *   **OH⁻离子**：采用**钴蓝色**及发光效果，象征碱的相反属性。
    *   **H₂O分子**：采用**浅蓝灰色**的椭圆形表示，清晰展示其作为中性生成物的形态。
    *   **背景**：深邃的深空蓝背景，模拟微观世界的深邃感，完美衬托发光的粒子。

2.  **符合认知规律的教学设计**：
    *   **从宏观到微观**：通过视图切换，建立宏观现象（溶液混合）与微观本质（离子反应）的联系。
    *   **从静态到动态**：支持从观察静态分布，到观看动态运动，再到手动交互的渐进式学习。
    *   **过程可视化**：将抽象的离子符号和方程式，转化为可见的粒子运动、碰撞与转化动画。

3.  **流畅的交互体验**：
    *   界面布局清晰，控制逻辑直观。
    *   动画运行流畅，粒子运动自然模拟了溶液中的布朗运动。
    *   支持键盘快捷键（空格键播放/暂停，R键重置，数字键1-4切换步骤），提升操作效率。

---

### 四、教学要点

本动画可用于阐释以下核心教学概念：

1.  **酸碱中和的微观本质**：中和反应不是酸和碱“互相消灭”，而是酸中的**氢离子（H⁺）** 与碱中的**氢氧根离子（OH⁻）** 结合生成**水（H₂O）** 的过程。
2.  **离子反应**：反应发生在离子级别，H⁺和OH⁻必须通过运动**相互接触（碰撞）** 才能发生反应。
3.  **反应的可视化计量**：通过观察H⁺和OH⁻数量的同步减少以及H₂O数量的等量增加，直观理解化学反应中的质量守恒与定量关系。
4.  **旁观离子**：通过显示/隐藏Na⁺和Cl⁻，理解它们在反应中不参与核心过程，只是存在于溶液中，有助于深化对“离子反应实质”的理解。

---

### 五、使用建议

1.  **对于学生（自学）**：
    *   **建议学习路径**：首先进入“宏观视图”了解反应背景 → 切换到“微观视图” → 使用“步骤演示”功能，按照1→2→3→4的顺序逐步学习 → 最后点击“播放”，观看完整的连续反应过程。
    *   **主动探索**：大胆使用“点击触发反应”功能。尝试先高亮H⁺，观察它们的运动；再高亮OH⁻，最后同时高亮两者，观察它们如何找到彼此并反应。
    *   **带着问题观察**：在观看时思考：“为什么离子需要运动？”“反应速率和什么有关？”“当一种离子消耗完会发生什么？”

2.  **对于教师（课堂演示）**：
    *   **引入环节**：可先展示“宏观视图”，提出问题：“溶液混合后，里面的粒子发生了什么变化？”引发学生猜想。
    *   **讲解核心**：切换到“微观视图”，暂停动画，利用“高亮”功能分别指出H⁺和OH⁻。播放步骤2和步骤3，重点讲解碰撞与结合的过程。
    *   **互动讨论**：使用“重置”和“步骤演示”功能，分步引导学生描述每一阶段的现象。让学生预测并验证点击两个离子后的结果。
    *   **总结升华**：在反应完成后，引导学生关注实时数据面板，总结粒子数量的变化关系，并回归到化学方程式 **H⁺ + OH⁻ → H₂O**，完成从微观粒子变化到宏观符号表达的升华。

3.  **通用技巧**：
    *   利用“暂停”功能在任何时间点冻结画面，进行详细讲解或提问。
    *   通过“隐藏背景离子”来简化初始视图，降低认知负荷，待理解核心过程后再显示完整体系。
    *   鼓励记录观察：反应前后，溶液中主要存在的粒子种类发生了什么根本性变化？

希望本交互式动画能成为您探索化学微观世界的得力助手，让抽象的概念变得生动具体，激发对化学的持久兴趣与深刻理解！

**祝您探索愉快！**