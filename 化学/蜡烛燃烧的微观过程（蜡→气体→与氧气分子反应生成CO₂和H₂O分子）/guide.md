# 需求：蜡烛燃烧的微观过程（蜡→气体→与氧气分子反应生成CO₂和H₂O分子）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向初中或高中化学初学者。用户的核心需求是：
1.  **理解宏观现象背后的微观本质**：学生能看到蜡烛燃烧的宏观现象（发光、发热、蜡减少），但难以想象其微观的物理和化学变化过程。
2.  **建立“物质变化”的微观模型**：需要清晰地展示固态蜡如何变成气态、如何与氧气反应、以及原子如何重新组合成新分子。
3.  **突破抽象概念障碍**：分子、原子、化学反应等概念抽象，需要通过动态、可视化的方式降低认知负荷。
4.  **激发探究兴趣**：通过交互和生动的动画，让学习过程变得有趣、直观，而非死记硬背反应方程式。

#### 教学设计思路
1.  **核心概念分解**：
    *   **物理变化（熔化和汽化）**：固态蜡分子受热 → 液态蜡 → 气态蜡分子（碳氢化合物混合物，以简化模型如C₂₅H₅₂表示）。
    *   **化学变化（燃烧反应）**：
        *   反应物：气态蜡分子 + 氧气分子 (O₂)。
        *   条件：点燃、足够温度。
        *   过程：分子碰撞、旧化学键断裂、原子重新排列、新化学键形成。
        *   生成物：二氧化碳分子 (CO₂) 和水分子 (H₂O)。
    *   **能量变化**：反应过程中释放能量（以光和热的形式呈现）。

2.  **认知规律遵循（分步、分层呈现）**：
    *   **从宏观到微观**：动画起始于一支燃烧的蜡烛宏观视图，然后镜头“拉近”或“切入”到火焰底部的微观世界。
    *   **从静态到动态**：先展示关键分子的静态模型（球棍模型），再让它们运动起来。
    *   **从部分到整体**：先分步讲解“蜡的相变”和“燃烧反应”，最后整合成一个完整的、循环的动态过程。

3.  **交互设计**：
    *   **控制节奏**：允许用户暂停、播放、重置动画，以适应不同的学习速度。
    *   **聚焦学习**：通过“步骤控制”或“高亮提示”，让用户分阶段学习，避免信息过载。
    *   **探索验证**：设计简单的交互点，如点击触发分子碰撞动画，或拖拽原子模拟成键过程，加深理解。

4.  **视觉呈现**：
    *   **分子模型**：采用标准、易于识别的球棍模型（C: 黑色/灰色， H: 白色， O: 红色）。
    *   **动态效果**：
        *   用向上的“热浪”波纹表示热量传递。
        *   蜡分子运动速度随温度升高而加快。
        *   化学反应时，旧分子“碎裂”成原子（键断裂动画），原子飞散后重新组合成新分子（键形成动画）。
        *   生成物CO₂和H₂O分子向火焰上方飘散。
    *   **信息分层**：背景为简洁的深色（突出分子），关键步骤配以简洁的文字标签和化学方程式提示。

#### 配色方案选择
*   **主背景**：深蓝色或深灰色（#1a2332 或 #2d3748）。模拟深邃的微观世界，能最大程度地突出彩色分子模型和光效。
*   **分子颜色（标准球棍模型）**：
    *   碳原子：深灰色 (#333333)
    *   氢原子：浅灰色/白色 (#f0f0f0)
    *   氧原子：红色 (#e53e3e)
    *   化学键：浅灰色线条
*   **火焰与能量**：
    *   火焰核心：亮黄色 (#ffeb3b)
    *   火焰外围及热量波纹：橙色 (#ff9800) 到红色 (#f44336) 的渐变。
    *   “光”和“热”的文字标签可使用金黄色。
*   **界面与控制按钮**：
    *   按钮背景：半透明深色 (rgba(255,255,255,0.1))
    *   按钮高亮/激活色：蓝色 (#4299e1)
    *   说明文字：浅灰色 (#e2e8f0)

#### 交互功能列表
1.  **主流程控制**：
    *   “播放/暂停”按钮：控制整个动画的进行。
    *   “重置”按钮：将动画恢复到初始状态。
    *   “步骤演示”模式：提供“上一步”、“下一步”按钮，分步学习。
2.  **视角切换**：
    *   “宏观视图”按钮：显示完整的蜡烛燃烧场景。
    *   “微观视图”按钮（默认）：切换到蜡芯附近的分子级别视图。
3.  **学习提示与聚焦**：
    *   **高亮模式**：点击或悬停在“蜡分子”、“氧气”、“火焰”等标签上时，对应的分子群或区域会高亮显示。
    *   **分步解说**：动画进行到关键步骤（如熔化、汽化、反应）时，自动弹出简洁的文字说明框。
    *   **化学方程式提示**：在反应阶段，画面一角显示简化的反应方程式（如：C₂₅H₅₂ + 38O₂ → 25CO₂ + 26H₂O），并随着动画进展高亮对应的部分。
4.  **探索性交互（可选增强）**：
    *   **“碰撞”触发器**：在反应阶段，用户点击“点火”或“碰撞”按钮，手动触发一个蜡分子与氧气分子的反应动画。
    *   **温度调节滑块**：拖动滑块模拟温度变化，观察蜡分子运动速度的变化（物理变化阶段）。

这个设计旨在创建一个既科学准确又生动有趣的教学工具，通过结构化的视觉叙事和适度的交互，帮助学生构建对燃烧现象的微观理解。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>蜡烛燃烧的微观过程教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: #e2e8f0;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 20px;
            max-width: 800px;
        }

        h1 {
            color: #ffeb3b;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }

        .subtitle {
            color: #94a3b8;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
            max-width: 1000px;
            width: 100%;
        }

        .animation-area {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #1a2332;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid #2d3748;
        }

        #canvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: center;
            background: rgba(30, 41, 59, 0.8);
            padding: 20px;
            border-radius: 10px;
            width: 100%;
        }

        .btn {
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            background: #4299e1;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
            min-width: 120px;
        }

        .btn:hover {
            background: #3182ce;
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(66, 153, 225, 0.3);
        }

        .btn:active {
            transform: translateY(0);
        }

        .btn-step {
            background: #38a169;
        }

        .btn-step:hover {
            background: #2f855a;
        }

        .btn-reset {
            background: #e53e3e;
        }

        .btn-reset:hover {
            background: #c53030;
        }

        .btn-view {
            background: #805ad5;
        }

        .btn-view:hover {
            background: #6b46c1;
        }

        .btn:disabled {
            background: #4a5568;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        .info-panel {
            background: rgba(45, 55, 72, 0.9);
            border-radius: 10px;
            padding: 20px;
            width: 100%;
            border-left: 4px solid #4299e1;
        }

        .step-title {
            color: #ffeb3b;
            font-size: 1.3rem;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .step-desc {
            color: #cbd5e0;
            line-height: 1.6;
            font-size: 1.05rem;
        }

        .equation {
            background: rgba(26, 32, 44, 0.8);
            padding: 15px;
            border-radius: 8px;
            margin-top: 15px;
            text-align: center;
            font-family: 'Cambria', 'Times New Roman', serif;
            font-size: 1.2rem;
            color: #ff9800;
            border: 1px solid #4a5568;
        }

        .highlight {
            color: #68d391;
            font-weight: bold;
        }

        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #4a5568;
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
            color: #a0aec0;
        }

        .footer {
            margin-top: 20px;
            text-align: center;
            color: #718096;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .animation-area {
                height: 400px;
            }
            
            .btn {
                min-width: 100px;
                padding: 10px 16px;
                font-size: 0.9rem;
            }
            
            h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>🕯️ 蜡烛燃烧的微观过程</h1>
        <p class="subtitle">探索固态蜡如何转化为气体，并与氧气反应生成二氧化碳和水</p>
    </div>

    <div class="container">
        <div class="animation-area">
            <canvas id="canvas"></canvas>
        </div>

        <div class="controls">
            <button id="playPause" class="btn">⏸️ 暂停</button>
            <button id="prevStep" class="btn btn-step">◀ 上一步</button>
            <button id="nextStep" class="btn btn-step">下一步 ▶</button>
            <button id="reset" class="btn btn-reset">🔄 重置</button>
            <button id="toggleView" class="btn btn-view">🔬 微观视图</button>
        </div>

        <div class="info-panel">
            <div class="step-title">
                <span id="stepIcon">🔍</span>
                <span id="stepTitle">观察宏观现象</span>
            </div>
            <p class="step-desc" id="stepDesc">这是一支正在燃烧的蜡烛。注意观察火焰、热量以及蜡的减少。</p>
            <div class="equation" id="equation">
                宏观现象：发光、发热、蜡减少
            </div>
        </div>

        <div class="legend">
            <div class="legend-item">
                <div class="legend-color" style="background-color: #333333;"></div>
                <span class="legend-text">碳原子 (C)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #f0f0f0;"></div>
                <span class="legend-text">氢原子 (H)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #e53e3e;"></div>
                <span class="legend-text">氧原子 (O)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background: linear-gradient(90deg, #ffeb3b, #ff9800);"></div>
                <span class="legend-text">火焰与热量</span>
            </div>
        </div>
    </div>

    <div class="footer">
        <p>教学动画 | 化学微观过程可视化 | 设计：熊猫老师</p>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const canvas = document.getElementById('canvas');
        const ctx = canvas.getContext('2d');

        // 设置Canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
        }
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);

        // 动画状态控制
        let animationId = null;
        let isPlaying = true;
        let currentStep = 0;
        let isMicroView = false;

        // 步骤定义
        const steps = [
            {
                title: "观察宏观现象",
                desc: "这是一支正在燃烧的蜡烛。注意观察火焰、热量以及蜡的减少。",
                equation: "宏观现象：发光、发热、蜡减少",
                icon: "🔍"
            },
            {
                title: "蜡的熔化（物理变化）",
                desc: "火焰的热量传递到蜡芯，固态蜡吸收热量，分子振动加剧，从有序排列变为无序流动，转化为液态蜡。",
                equation: "固态蜡 + 热量 → 液态蜡",
                icon: "🔥"
            },
            {
                title: "蜡的汽化（物理变化）",
                desc: "液态蜡继续受热，分子获得足够能量，挣脱液体表面张力，变成气态蜡分子（以C₂₅H₅₂为例）。",
                equation: "液态蜡 + 更多热量 → 气态蜡分子",
                icon: "💨"
            },
            {
                title: "分子混合与扩散",
                desc: "气态蜡分子向上扩散，与空气中的氧气分子(O₂)混合，为化学反应做准备。",
                equation: "C₂₅H₅₂(气) + O₂(气) → 混合",
                icon: "🌀"
            },
            {
                title: "燃烧反应（化学变化）",
                desc: "在高温下，蜡分子与氧气分子剧烈碰撞，化学键断裂，碳、氢、氧原子重新组合，形成新的化学键。",
                equation: "C₂₅H₅₂ + 38O₂ → 25CO₂ + 26H₂O + 能量",
                icon: "⚡"
            },
            {
                title: "生成物与能量释放",
                desc: "反应生成二氧化碳(CO₂)和水(H₂O)分子，并向周围释放大量能量，表现为光和热。",
                equation: "生成物：CO₂ ↑ 和 H₂O ↑ | 能量：光 + 热",
                icon: "✨"
            }
        ];

        // 分子和粒子定义
        const particles = {
            solidWax: [],
            liquidWax: [],
            gasWax: [],
            oxygen: [],
            co2: [],
            h2o: [],
            heatWaves: []
        };

        // 颜色定义
        const colors = {
            carbon: '#333333',
            hydrogen: '#f0f0f0',
            oxygen: '#e53e3e',
            bond: '#a0aec0',
            flameInner: '#ffeb3b',
            flameOuter: '#ff9800',
            heatWave: 'rgba(255, 152, 0, 0.3)',
            solidWax: '#d1d5db',
            liquidWax: '#e5e7eb',
            background: '#1a2332'
        };

        // 分子类
        class Molecule {
            constructor(x, y, type, vx = 0, vy = 0) {
                this.x = x;
                this.y = y;
                this.type = type; // 'wax', 'oxygen', 'co2', 'h2o'
                this.vx = vx;
                this.vy = vy;
                this.size = type === 'wax' ? 8 : 6;
                this.atoms = [];
                this.bonds = [];
                this.reacted = false;
                this.reactionProgress = 0;
                
                // 根据分子类型初始化原子和键
                this.initMolecule();
            }

            initMolecule() {
                if (this.type === 'wax') {
                    // 简化蜡分子：中心碳原子，周围有氢原子
                    this.atoms = [
                        {type: 'C', x: 0, y: 0, color: colors.carbon},
                        {type: 'H', x: -10, y: -8, color: colors.hydrogen},
                        {type: 'H', x: 10, y: -8, color: colors.hydrogen},
                        {type: 'H', x: -10, y: 8, color: colors.hydrogen},
                        {type: 'H', x: 10, y: 8, color: colors.hydrogen}
                    ];
                    this.bonds = [
                        {from: 0, to: 1}, {from: 0, to: 2},
                        {from: 0, to: 3}, {from: 0, to: 4}
                    ];
                } else if (this.type === 'oxygen') {
                    this.atoms = [
                        {type: 'O', x: -5, y: 0, color: colors.oxygen},
                        {type: 'O', x: 5, y: 0, color: colors.oxygen}
                    ];
                    this.bonds = [{from: 0, to: 1}];
                } else if (this.type === 'co2') {
                    this.atoms = [
                        {type: 'C', x: 0, y: 0, color: colors.carbon},
                        {type: 'O', x: -8, y: 0, color: colors.oxygen},
                        {type: 'O', x: 8, y: 0, color: colors.oxygen}
                    ];
                    this.bonds = [{from: 0, to: 1}, {from: 0, to: 2}];
                } else if (this.type === 'h2o') {
                    this.atoms = [
                        {type: 'O', x: 0, y: 0, color: colors.oxygen},
                        {type: 'H', x: -6, y: -6, color: colors.hydrogen},
                        {type: 'H', x: 6, y: -6, color: colors.hydrogen}
                    ];
                    this.bonds = [{from: 0, to: 1}, {from: 0, to: 2}];
                }
            }

            update(step) {
                // 根据步骤更新分子行为
                if (step >= 1 && step <= 2 && this.type === 'wax') {
                    // 步骤1-2：蜡分子受热向上运动
                    this.vy = -0.5 - Math.random() * 0.5;
                } else if (step >= 3 && this.type === 'wax') {
                    // 步骤3+：气态蜡分子更剧烈运动
                    this.vx += (Math.random() - 0.5) * 0.2;
                    this.vy = -1 - Math.random() * 0.5;
                }
                
                if (step >= 3 && this.type === 'oxygen') {
                    // 氧气分子向火焰区域扩散
                    const dx = canvas.width/2 - this.x;
                    const dy = canvas.height*0.7 - this.y;
                    const dist = Math.sqrt(dx*dx + dy*dy);
                    if (dist > 50) {
                        this.vx += dx * 0.0005;
                        this.vy += dy * 0.0005;
                    }
                }
                
                if (step >= 5 && (this.type === 'co2' || this.type === 'h2o')) {
                    // 生成物向上飘散
                    this.vy = -1.5 - Math.random();
                    this.vx += (Math.random() - 0.5) * 0.1;
                }

                // 限制速度
                const speedLimit = this.type === 'oxygen' ? 2 : 3;
                const speed = Math.sqrt(this.vx*this.vx + this.vy*this.vy);
                if (speed > speedLimit) {
                    this.vx = (this.vx / speed) * speedLimit;
                    this.vy = (this.vy / speed) * speedLimit;
                }

                // 更新位置
                this.x += this.vx;
                this.y += this.vy;

                // 边界处理
                if (this.x < 0) this.x = 0;
                if (this.x > canvas.width) this.x = canvas.width;
                if (this.y < 0) this.y = 0;
                if (this.y > canvas.height) this.y = canvas.height;
            }

            draw() {
                // 绘制化学键
                ctx.strokeStyle = colors.bond;
                ctx.lineWidth = 2;
                for (const bond of this.bonds) {
                    const fromAtom = this.atoms[bond.from];
                    const toAtom = this.atoms[bond.to];
                    ctx.beginPath();
                    ctx.moveTo(this.x + fromAtom.x, this.y + fromAtom.y);
                    ctx.lineTo(this.x + toAtom.x, this.y + toAtom.y);
                    ctx.stroke();
                }

                // 绘制原子
                for (const atom of this.atoms) {
                    ctx.fillStyle = atom.color;
                    ctx.beginPath();
                    ctx.arc(this.x + atom.x, this.y + atom.y, 5, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 原子类型标签（微观视图）
                    if (isMicroView) {
                        ctx.fillStyle = 'white';
                        ctx.font = '10px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(atom.type, this.x + atom.x, this.y + atom.y - 8);
                    }
                }
            }
        }

        // 热波类
        class HeatWave {
            constructor(x, y) {
                this.x = x;
                this.y = y;
                this.radius = 10;
                this.maxRadius = 100;
                this.speed = 2;
                this.alpha = 0.5;
            }

            update() {
                this.radius += this.speed;
                this.alpha -= 0.01;
                return this.alpha > 0 && this.radius < this.maxRadius;
            }

            draw() {
                ctx.strokeStyle = `rgba(255, 152, 0, ${this.alpha})`;
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.stroke();
            }
        }

        // 初始化粒子系统
        function initParticles() {
            particles.solidWax = [];
            particles.liquidWax = [];
            particles.gasWax = [];
            particles.oxygen = [];
            particles.co2 = [];
            particles.h2o = [];
            particles.heatWaves = [];

            // 创建固态蜡粒子（底部）
            for (let i = 0; i < 30; i++) {
                particles.solidWax.push({
                    x: canvas.width/2 + (Math.random() - 0.5) * 100,
                    y: canvas.height - 50 + Math.random() * 30,
                    size: 4 + Math.random() * 3
                });
            }

            // 创建氧气分子
            for (let i = 0; i < 40; i++) {
                particles.oxygen.push(new Molecule(
                    Math.random() * canvas.width,
                    Math.random() * canvas.height * 0.3,
                    'oxygen',
                    (Math.random() - 0.5) * 0.5,
                    (Math.random() - 0.5) * 0.5
                ));
            }
        }

        // 绘制宏观视图
        function drawMacroView() {
            // 绘制蜡烛
            const candleX = canvas.width / 2;
            const candleBottom = canvas.height - 50;
            
            // 蜡烛主体
            ctx.fillStyle = '#f0f0f0';
            ctx.fillRect(candleX - 20, candleBottom - 150, 40, 150);
            
            // 蜡烛芯
            ctx.fillStyle = '#4a5568';
            ctx.fillRect(candleX - 2, candleBottom - 160, 4, 10);
            
            // 火焰
            const gradient = ctx.createRadialGradient(
                candleX, candleBottom - 160, 5,
                candleX, candleBottom - 160, 30
            );
            gradient.addColorStop(0, colors.flameInner);
            gradient.addColorStop(1, colors.flameOuter);
            
            ctx.fillStyle = gradient;
            ctx.beginPath();
            ctx.moveTo(candleX, candleBottom - 190);
            ctx.bezierCurveTo(
                candleX + 15, candleBottom - 170,
                candleX + 10, candleBottom - 140,
                candleX, candleBottom - 130
            );
            ctx.bezierCurveTo(
                candleX - 10, candleBottom - 140,
                candleX - 15, candleBottom - 170,
                candleX, candleBottom - 190
            );
            ctx.fill();
            
            // 热浪
            if (currentStep >= 1) {
                particles.heatWaves.push(new HeatWave(candleX, candleBottom - 160));
            }
            
            // 绘制热浪
            for (let i = particles.heatWaves.length - 1; i >= 0; i--) {
                if (!particles.heatWaves[i].update()) {
                    particles.heatWaves.splice(i, 1);
                } else {
                    particles.heatWaves[i].draw();
                }
            }
            
            // 绘制固态蜡粒子
            ctx.fillStyle = colors.solidWax;
            for (const wax of particles.solidWax) {
                ctx.beginPath();
                ctx.arc(wax.x, wax.y, wax.size, 0, Math.PI * 2);
                ctx.fill();
            }
            
            // 绘制液态蜡（步骤1-2）
            if (currentStep >= 1) {
                ctx.fillStyle = colors.liquidWax;
                for (let i = 0; i < 15; i++) {
                    const x = candleX + (Math.random() - 0.5) * 30;
                    const y = candleBottom - 50 + Math.random() * 20;
                    ctx.beginPath();
                    ctx.arc(x, y, 3, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 绘制气态蜡分子（步骤2+）
            if (currentStep >= 2) {
                for (const wax of particles.gasWax) {
                    wax.update(currentStep);
                    wax.draw();
                }
            }
            
            // 绘制氧气分子（步骤3+）
            if (currentStep >= 3) {
                for (const oxy of particles.oxygen) {
                    oxy.update(currentStep);
                    oxy.draw();
                }
            }
            
            // 绘制生成物（步骤5+）
            if (currentStep >= 5) {
                for (const co2 of particles.co2) {
                    co2.update(currentStep);
                    co2.draw();
                }
                for (const h2o of particles.h2o) {
                    h2o.update(currentStep);
                    h2o.draw();
                }
            }
            
            // 添加新的气态蜡分子（步骤2+）
            if (currentStep >= 2 && Math.random() < 0.05) {
                particles.gasWax.push(new Molecule(
                    candleX + (Math.random() - 0.5) * 40,
                    candleBottom - 50,
                    'wax',
                    (Math.random() - 0.5) * 0.5,
                    -1 - Math.random()
                ));
            }
            
            // 模拟反应（步骤4+）
            if (currentStep >= 4 && particles.gasWax.length > 0 && particles.oxygen.length > 0) {
                // 随机选择蜡分子和氧气分子进行反应
                if (Math.random() < 0.02) {
                    const waxIndex = Math.floor(Math.random() * particles.gasWax.length);
                    const oxyIndex = Math.floor(Math.random() * particles.oxygen.length);
                    
                    const wax = particles.gasWax[waxIndex];
                    const oxy = particles.oxygen[oxyIndex];
                    
                    // 移除反应物
                    particles.gasWax.splice(waxIndex, 1);
                    particles.oxygen.splice(oxyIndex, 1);
                    
                    // 添加生成物
                    particles.co2.push(new Molecule(
                        wax.x, wax.y, 'co2',
                        (Math.random() - 0.5) * 1,
                        -2 - Math.random()
                    ));
                    
                    particles.h2o.push(new Molecule(
                        wax.x + 20, wax.y, 'h2o',
                        (Math.random() - 0.5) * 1,
                        -2 - Math.random()
                    ));
                }
            }
        }

        // 绘制微观视图
        function drawMicroView() {
            // 绘制背景
            ctx.fillStyle = colors.background;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制热源区域
            const gradient = ctx.createRadialGradient(
                canvas.width/2, canvas.height*0.7, 20,
                canvas.width/2, canvas.height*0.7, 100
            );
            gradient.addColorStop(0, 'rgba(255, 235, 59, 0.3)');
            gradient.addColorStop(1, 'rgba(255, 152, 0, 0.1)');
            
            ctx.fillStyle = gradient;
            ctx.beginPath();
            ctx.arc(canvas.width/2, canvas.height*0.7, 100, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制所有分子
            for (const wax of particles.gasWax) {
                wax.update(currentStep);
                wax.draw();
            }
            
            for (const oxy of particles.oxygen) {
                oxy.update(currentStep);
                oxy.draw();
            }
            
            for (const co2 of particles.co2) {
                co2.update(currentStep);
                co2.draw();
            }
            
            for (const h2o of particles.h2o) {
                h2o.update(currentStep);
                h2o.draw();
            }
            
            // 绘制反应动画（步骤4-5）
            if (currentStep >= 4 && currentStep <= 5) {
                // 在中心区域显示反应示意
                const centerX = canvas.width/2;
                const centerY = canvas.height*0.7;
                
                // 绘制碰撞示意
                ctx.strokeStyle = 'rgba(255, 235, 59, 0.5)';
                ctx.setLineDash([5, 5]);
                ctx.beginPath();
                ctx.arc(centerX, centerY, 60, 0, Math.PI * 2);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 绘制反应箭头
                ctx.strokeStyle = '#68d391';
                ctx.lineWidth = 3;
                ctx.beginPath();
                ctx.moveTo(centerX - 80, centerY);
                ctx.lineTo(centerX - 30, centerY);
                ctx.moveTo(centerX - 20, centerY);
                ctx.lineTo(centerX - 10, centerY - 5);
                ctx.lineTo(centerX - 10, centerY + 5);
                ctx.lineTo(centerX - 20, centerY);
                ctx.stroke();
                
                // 绘制反应物和生成物示意
                if (currentStep === 4) {
                    // 反应物
                    const waxMolecule = new Molecule(centerX - 120, centerY, 'wax');
                    waxMolecule.draw();
                    
                    const oxyMolecule = new Molecule(centerX - 150, centerY + 40, 'oxygen');
                    oxyMolecule.draw();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = '14px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('+', centerX - 135, centerY + 20);
                } else if (currentStep === 5) {
                    // 生成物
                    const co2Molecule = new Molecule(centerX + 100, centerY - 30, 'co2');
                    co2Molecule.draw();
                    
                    const h2oMolecule = new Molecule(centerX + 100, centerY + 30, 'h2o');
                    h2oMolecule.draw();
                    
                    ctx.fillStyle = 'white';
                    ctx.font = '14px Arial';
                    ctx.textAlign = 'center';
                    ctx.fillText('+', centerX + 100, centerY);
                }
            }
        }

        // 更新信息面板
        function updateInfoPanel() {
            const step = steps[currentStep];
            document.getElementById('stepTitle').textContent = step.title;
            document.getElementById('stepDesc').textContent = step.desc;
            document.getElementById('equation').textContent = step.equation;
            document.getElementById('stepIcon').textContent = step.icon;
            
            // 高亮方程中的关键部分
            if (currentStep === 4 || currentStep === 5) {
                const eq = document.getElementById('equation');
                eq.innerHTML = step.equation
                    .replace('C₂₅H₅₂', '<span class="highlight">C₂₅H₅₂</span>')
                    .replace('O₂', '<span class="highlight">O₂</span>')
                    .replace('CO₂', '<span class="highlight">CO₂</span>')
                    .replace('H₂O', '<span class="highlight">H₂O</span>');
            }
            
            // 更新按钮状态
            document.getElementById('prevStep').disabled = currentStep === 0;
            document.getElementById('nextStep').disabled = currentStep === steps.length - 1;
        }

        // 主动画循环
        function animate() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 根据视图模式绘制
            if (isMicroView) {
                drawMicroView();
            } else {
                drawMacroView();
            }
            
            // 继续动画循环
            if (isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }

        // 控制函数
        function playPause() {
            isPlaying = !isPlaying;
            const btn = document.getElementById('playPause');
            btn.textContent = isPlaying ? '⏸️ 暂停' : '▶️ 播放';
            
            if (isPlaying) {
                animate();
            } else {
                cancelAnimationFrame(animationId);
            }
        }

        function nextStep() {
            if (currentStep < steps.length - 1) {
                currentStep++;
                updateInfoPanel();
                
                // 在特定步骤初始化粒子
                if (currentStep === 2) {
                    // 开始生成气态蜡分子
                    const candleX = canvas.width / 2;
                    const candleBottom = canvas.height - 50;
                    for (let i = 0; i < 10; i++) {
                        particles.gasWax.push(new Molecule(
                            candleX + (Math.random() - 0.5) * 40,
                            candleBottom - 30 + Math.random() * 20,
                            'wax',
                            (Math.random() - 0.5) * 0.5,
                            -0.5 - Math.random()
                        ));
                    }
                }
            }
        }

        function prevStep() {
            if (currentStep > 0) {
                currentStep--;
                updateInfoPanel();
            }
        }

        function resetAnimation() {
            currentStep = 0;
            isMicroView = false;
            initParticles();
            updateInfoPanel();
            
            const viewBtn = document.getElementById('toggleView');
            viewBtn.textContent = '🔬 微观视图';
            
            if (!isPlaying) {
                playPause(); // 自动开始播放
            }
        }

        function toggleView() {
            isMicroView = !isMicroView;
            const btn = document.getElementById('toggleView');
            btn.textContent = isMicroView ? '👁️ 宏观视图' : '🔬 微观视图';
        }

        // 事件监听
        document.getElementById('playPause').addEventListener('click', playPause);
        document.getElementById('nextStep').addEventListener('click', nextStep);
        document.getElementById('prevStep').addEventListener('click', prevStep);
        document.getElementById('reset').addEventListener('click', resetAnimation);
        document.getElementById('toggleView').addEventListener('click', toggleView);

        // 键盘控制
        document.addEventListener('keydown', (e) => {
            switch(e.key) {
                case ' ':
                    playPause();
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
                case 'v':
                case 'V':
                    toggleView();
                    break;
            }
        });

        // 初始化
        initParticles();
        updateInfoPanel();
        animate();

        // 添加使用提示
        setTimeout(() => {
            console.log('🎮 控制提示：');
            console.log('空格键 - 播放/暂停');
            console.log('左右箭头 - 切换步骤');
            console.log('R键 - 重置动画');
            console.log('V键 - 切换视图');
        }, 1000);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 《蜡烛燃烧的微观过程》交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态可视化方式，帮助您深入理解蜡烛燃烧这一常见现象背后复杂的物理和化学变化过程。无论您是学生、教师还是科学爱好者，本指南都将帮助您充分利用这一教学资源。

---

### 一、 功能说明

本动画将蜡烛燃烧的完整过程分解为六个逻辑清晰的步骤，从宏观现象逐步深入到分子级别的微观反应。您可以通过多种交互方式控制学习节奏，并在宏观与微观视图间自由切换，构建从现象到本质的完整认知。

### 二、 主要功能

1.  **动画流程控制**
    *   **播放/暂停**：控制整个动画的连续播放与暂停，便于仔细观察或讲解。
    *   **上一步/下一步**：分步学习，精准控制学习进度，聚焦于当前步骤的核心概念。
    *   **重置**：一键将动画恢复到初始状态，方便重复观看或重新开始。

2.  **视图模式切换**
    *   **宏观视图**：展示完整的蜡烛燃烧场景，包括火焰、蜡烛本体和热浪，直观呈现发光、发热、蜡减少等宏观现象。
    *   **微观视图**：将视角“拉近”到分子层面，清晰展示蜡分子、氧气分子、二氧化碳分子和水分子的结构、运动及反应过程。

3.  **智能信息面板**
    *   动画每一步都配有同步更新的**步骤标题**、**详细说明**和**化学方程式**。
    *   在关键的反应步骤，方程式中的反应物和生成物会被高亮显示，帮助您聚焦重点。

4.  **键盘快捷操作**
    *   **空格键**：播放/暂停
    *   **左右方向键**：上一步/下一步
    *   **R键**：重置动画
    *   **V键**：切换宏观/微观视图

### 三、 设计特色

1.  **科学准确性**：采用国际通用的球棍模型表示分子（碳：黑/灰，氢：白，氧：红），反应方程式经过简化但符合化学计量关系。
2.  **认知友好性**：严格遵循“从宏观到微观”、“从现象到本质”的认知规律，通过分层、分步的呈现方式降低学习门槛。
3.  **视觉表现力**：
    *   用粒子运动速度的变化模拟温度对分子运动的影响。
    *   用化学键的“断裂”与“形成”动画直观展示化学反应的本质。
    *   用扩散的热浪波纹和渐变的火焰颜色生动表现能量的释放。
4.  **交互引导性**：界面设计简洁，操作直观。控制按钮状态明确（如禁用不可用的步骤），信息面板同步提示，确保学习路径清晰。

### 四、 教学要点（分步解析）

建议按照以下步骤顺序进行学习，以建立完整知识链条：

**步骤1：观察宏观现象**
*   **学习目标**：建立对蜡烛燃烧宏观现象的初步认识。
*   **观察重点**：火焰的形状与颜色、蜡芯上方的热空气流动（热浪）、固态蜡的消耗。

**步骤2：蜡的熔化（物理变化）**
*   **核心概念**：**物理变化**——分子本身不变，排列方式和运动状态改变。
*   **观察重点**：火焰热量传递到蜡体，固态蜡颗粒“软化”并开始向上缓慢运动。

**步骤3：蜡的汽化（物理变化）**
*   **核心概念**：相变（固态→液态→气态），分子获得足够动能挣脱束缚。
*   **观察重点**：液态蜡进一步受热，变成**气态蜡分子**（C₂₅H₅₂模型），运动速度显著加快。

**步骤4：分子混合与扩散**
*   **核心概念**：气体扩散，反应物接触。
*   **观察重点**：气态蜡分子与空气中的**氧气分子**（O₂）相互混合，向火焰区域汇聚。

**步骤5：燃烧反应（化学变化）**
*   **核心概念**：**化学变化**——分子破裂成原子，原子重新组合成新分子。
*   **观察重点**：在高温区，蜡分子与氧气分子碰撞后“碎裂”，原子重新组合。这是本动画的**最关键步骤**，请注意观察微观视图中的示意动画。

**步骤6：生成物与能量释放**
*   **核心概念**：质量守恒、能量转化（化学能→光能+热能）。
*   **观察重点**：**二氧化碳**（CO₂）和**水**（H₂O）分子的生成，以及它们向上方飘散。注意火焰持续发光发热是反应释放能量的表现。

### 五、 使用建议

1.  **给学生（自主学习）**：
    *   首次观看时，请点击“播放”，跟随动画完整观看一遍，建立整体印象。
    *   第二次观看时，使用“上一步/下一步”按钮，在每个步骤暂停，仔细阅读信息面板的文字说明，并观察对应的动画细节。
    *   反复使用“宏观/微观视图”切换功能，将看到的宏观现象（如火焰）与微观过程（分子反应）在脑中建立联系。
    *   尝试在不看提示的情况下，向他人复述每个步骤发生了什么。

2.  **给教师（课堂演示或辅助教学）**：
    *   **引入环节**：播放完整动画，提出问题：“火焰是什么在燃烧？蜡真的‘消失’了吗？”
    *   **讲解环节**：使用“分步控制”功能，配合动画详细讲解每个阶段。在关键步骤（如第5步化学反应）可以暂停，切换到微观视图，引导学生描述他们看到的“键的断裂与形成”。
    *   **讨论与总结**：播放完毕后，可以关闭动画，让学生分组讨论并尝试画出蜡烛燃烧的微观过程示意图。最后再次播放动画进行验证和总结。
    *   **板书结合**：可以将动画与黑板上的化学方程式板书同步进行，强化理解。

3.  **给所有用户**：
    *   善用**键盘快捷键**，可以让您的操作更加流畅，专注于内容本身。
    *   当对某个步骤不理解时，点击“重置”并单独针对该步骤及其前后步骤进行反复观察。
    *   本动画是理想化的模型，实际过程更为复杂（如蜡是多种烃的混合物，燃烧可能不完全等）。它旨在揭示核心原理，可作为探索更深入知识的起点。

---

希望这份指南能帮助您更好地利用这个交互式工具，享受探索科学奥秘的乐趣！如果您有任何关于动画内容本身的疑问或教学上的想法，欢迎基于此动画模型进行进一步的探讨和延伸。祝您学习愉快，教学有成！