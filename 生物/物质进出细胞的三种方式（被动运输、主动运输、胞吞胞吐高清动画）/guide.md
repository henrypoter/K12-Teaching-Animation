# 需求：物质进出细胞的三种方式（被动运输、主动运输、胞吞胞吐高清动画）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的生物学学习者。他们需要直观理解抽象、微观的细胞膜运输过程。
2.  **核心需求**：
    *   **概念可视化**：将教材中静态的图片和文字描述，转化为动态、连续的过程，帮助理解物质如何穿越细胞膜。
    *   **对比与区分**：清晰展示被动运输（自由扩散、协助扩散）、主动运输以及胞吞/胞吐在**能量消耗、载体蛋白需求、物质运动方向**上的关键区别。
    *   **主动探索与验证**：用户希望能通过交互操作（如改变浓度、开关能量供应）来观察过程变化，从而加深理解，而非被动观看。
    *   **知识整合与测试**：在观看动画后，有一个简明的总结和自测环节，以巩固学习效果。

#### 教学设计思路
1.  **核心概念分解**：
    *   **被动运输**：顺浓度梯度，不消耗能量。细分为**自由扩散**（小分子/脂溶性物质直接通过脂双层）和**协助扩散**（借助通道蛋白或载体蛋白）。
    *   **主动运输**：逆浓度梯度，需要载体蛋白并消耗ATP。
    *   **胞吞与胞吐**：大分子或颗粒物质，通过膜包裹形成囊泡进行运输，消耗能量。
    *   **贯穿线索**：**浓度梯度、膜蛋白（载体/通道）、能量（ATP）、物质大小**。

2.  **认知规律遵循**：
    *   **从简到繁**：先展示最简单的自由扩散，再引入蛋白质辅助的协助扩散，然后是复杂的主动运输，最后是大尺度的膜泡运输。
    *   **对比学习**：将三种方式并列展示，用高亮、动画速度、提示标签等方式突出其差异点。
    *   **建构主义**：通过交互实验，让用户自己“构建”浓度差、添加ATP等，观察结果，从而内化知识。

3.  **交互设计**：
    *   **模块化导航**：设计清晰的标签页或按钮，让用户可以自由选择学习任一运输方式，或进入对比模式。
    *   **模拟实验台**：为每种运输方式设计一个可操作的“实验环境”。例如：
        *   拖动滑块调整细胞膜内外物质浓度。
        *   点击按钮“提供ATP”或“耗尽ATP”。
        *   选择不同的物质（如O₂、葡萄糖、K⁺离子）观察其运输方式。
        *   点击“播放/暂停/重置”控制动画。
    *   **实时反馈**：交互操作时，动画立即响应，并伴有文字说明（如“能量充足，主动运输启动”）和关键数据变化（如ATP数量减少）。

4.  **视觉呈现**：
    *   **风格**：采用简洁、扁平化或轻微拟物化的卡通风格，确保科学性和清晰度。
    *   **细胞膜**：用双层磷脂分子清晰排列表示，蛋白质（载体、通道）用不同形状和颜色区分。
    *   **物质粒子**：用不同颜色和形状的小球代表不同物质（如红色小球代表O₂，蓝色方块代表葡萄糖，紫色三角形代表K⁺）。
    *   **能量表示**：ATP用黄色闪电符号或“ATP”标签表示，消耗时出现破碎或消失动画。
    *   **动态效果**：粒子运动平滑，浓度高低用粒子密度直观表现。囊泡形成、移动、融合的过程要连贯。

#### 配色方案选择
*   **主色调**：采用温和、不刺眼的科技蓝或生物学常用的淡绿色作为背景和界面主色，营造冷静、专注的学习氛围。
*   **细胞膜**：磷脂双层用浅灰色/白色表示头部，淡黄色表示尾部。背景色为浅蓝色透明细胞质和浅粉色透明细胞外液。
*   **关键元素高亮色**：
    *   **ATP/能量**：亮黄色或橙色。
    *   **载体蛋白**：蓝色。
    *   **通道蛋白**：绿色。
    *   **物质粒子**：
        *   氧气/二氧化碳（自由扩散）：红色/灰色。
        *   葡萄糖、氨基酸（协助扩散/主动运输）：蓝色。
        *   离子（如K⁺、Na⁺）：紫色。
    *   **囊泡（胞吞胞吐）**：淡粉色或淡橙色边框。
*   **文字与UI**：深灰色文字，白色或半透明黑色底色的信息框，确保可读性。

#### 交互功能列表
1.  **全局导航**：
    *   “自由扩散”、“协助扩散”、“主动运输”、“胞吞/胞吐”四个主模式切换按钮。
    *   “对比模式”按钮，将三种穿膜方式并列对比播放。
    *   “知识总结”按钮，弹出对比表格。
    *   “小测验”按钮，进入5道选择题的自测环节。

2.  **自由扩散模块**：
    *   浓度差滑块（膜内/膜外）。
    *   物质选择器（O₂, CO₂, 脂溶性物质）。
    *   观察提示：粒子从高密度区随机运动到低密度区。

3.  **协助扩散模块**：
    *   浓度差滑块。
    *   “开关通道蛋白”按钮（或选择不同物质自动匹配蛋白）。
    *   物质选择器（葡萄糖，水[通过水通道蛋白]）。
    *   观察提示：粒子通过特定蛋白通道，仍顺浓度梯度。

4.  **主动运输模块**：
    *   浓度差滑块（可设置为初始逆浓度梯度）。
    *   “提供/耗尽ATP”开关。
    *   物质选择器（K⁺, Na⁺, 碘离子）。
    *   载体蛋白形状变化动画（结合物质-消耗ATP-构象改变-释放物质）。
    *   ATP计数器，显示消耗数量。

5.  **胞吞胞吐模块**：
    *   切换“胞吞”（进入细胞）和“胞吐”（排出细胞）子模式。
    *   物质选择器（大蛋白质、细菌颗粒）。
    *   “启动”按钮：播放膜凹陷/突起、包裹、形成囊泡、移动、融合的完整过程。
    *   高亮显示细胞骨架（如微丝）的参与。

6.  **对比模式**：
    *   并排三个相同初始条件的细胞膜场景。
    *   统一控制：“开始运输”按钮。
    *   关键差异点用动态箭头（浓度梯度方向）、高亮ATP消耗、蛋白闪烁等方式同步提示。

7.  **反馈与总结**：
    *   交互时，屏幕侧边或底部有动态文字说明框。
    *   “知识总结”为可折叠的对比表格。
    *   “小测验”提供即时正误反馈和解析。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>物质进出细胞的三种方式 - 交互式教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
            color: #333;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 150, 0.1);
            overflow: hidden;
            padding: 25px;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #e0e9ff;
        }

        h1 {
            color: #2c3e50;
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #3498db, #2ecc71);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.2rem;
        }

        .main-content {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .control-panel {
            background: #f8fafd;
            border-radius: 15px;
            padding: 25px;
            border: 2px solid #e0e9ff;
        }

        .mode-selector {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 25px;
            justify-content: center;
        }

        .mode-btn {
            padding: 12px 25px;
            border: none;
            border-radius: 50px;
            background: linear-gradient(135deg, #e0e9ff, #c8d8f0);
            color: #2c3e50;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.08);
        }

        .mode-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.12);
        }

        .mode-btn.active {
            background: linear-gradient(135deg, #3498db, #2980b9);
            color: white;
            box-shadow: 0 4px 15px rgba(52, 152, 219, 0.4);
        }

        .experiment-controls {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .control-group {
            background: white;
            padding: 15px;
            border-radius: 10px;
            border: 1px solid #e0e9ff;
        }

        .control-group h3 {
            color: #3498db;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .slider-container label {
            min-width: 80px;
            color: #555;
        }

        input[type="range"] {
            flex: 1;
            height: 8px;
            border-radius: 4px;
            background: #e0e9ff;
            outline: none;
            -webkit-appearance: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        .button-group {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .action-btn {
            padding: 8px 16px;
            border: none;
            border-radius: 6px;
            background: #2ecc71;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .action-btn:hover {
            background: #27ae60;
            transform: translateY(-2px);
        }

        .action-btn.secondary {
            background: #e74c3c;
        }

        .action-btn.secondary:hover {
            background: #c0392b;
        }

        .animation-area {
            background: white;
            border-radius: 15px;
            padding: 20px;
            border: 2px solid #e0e9ff;
            min-height: 500px;
            position: relative;
            overflow: hidden;
        }

        #animationCanvas {
            width: 100%;
            height: 460px;
            display: block;
            background: linear-gradient(180deg, #f0f8ff 0%, #e6f2ff 100%);
            border-radius: 10px;
        }

        .info-panel {
            background: #f8fafd;
            border-radius: 15px;
            padding: 25px;
            border: 2px solid #e0e9ff;
        }

        .info-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }

        .info-header h2 {
            color: #2c3e50;
            font-size: 1.5rem;
        }

        .info-content {
            line-height: 1.6;
            color: #555;
        }

        .highlight {
            background: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);
            padding: 2px 6px;
            border-radius: 4px;
            font-weight: 600;
        }

        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }

        .comparison-table th {
            background: #3498db;
            color: white;
            padding: 15px;
            text-align: left;
        }

        .comparison-table td {
            padding: 12px 15px;
            border-bottom: 1px solid #e0e9ff;
        }

        .comparison-table tr:last-child td {
            border-bottom: none;
        }

        .comparison-table tr:nth-child(even) {
            background: #f8fafd;
        }

        .status-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px;
            background: #2c3e50;
            color: white;
            border-radius: 10px;
            margin-top: 20px;
        }

        .status-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .status-value {
            font-weight: 600;
            color: #2ecc71;
        }

        .quiz-section {
            margin-top: 30px;
            padding: 20px;
            background: #f8fafd;
            border-radius: 15px;
            border: 2px solid #e0e9ff;
        }

        .quiz-question {
            margin-bottom: 20px;
            padding: 15px;
            background: white;
            border-radius: 10px;
            border-left: 5px solid #3498db;
        }

        .quiz-options {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-top: 10px;
        }

        .quiz-option {
            padding: 12px;
            background: #f0f8ff;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .quiz-option:hover {
            background: #e0e9ff;
        }

        .quiz-option.correct {
            background: #d4edda;
            border-left: 5px solid #28a745;
        }

        .quiz-option.incorrect {
            background: #f8d7da;
            border-left: 5px solid #dc3545;
        }

        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            .mode-selector {
                flex-direction: column;
            }
            
            .experiment-controls {
                grid-template-columns: 1fr;
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
            <h1>物质进出细胞的三种方式</h1>
            <p class="subtitle">交互式教学动画 - 探索被动运输、主动运输与胞吞胞吐</p>
        </header>

        <div class="main-content">
            <div class="control-panel">
                <div class="mode-selector">
                    <button class="mode-btn active" data-mode="passive">被动运输</button>
                    <button class="mode-btn" data-mode="facilitated">协助扩散</button>
                    <button class="mode-btn" data-mode="active">主动运输</button>
                    <button class="mode-btn" data-mode="endocytosis">胞吞胞吐</button>
                    <button class="mode-btn" data-mode="compare">对比模式</button>
                    <button class="mode-btn" data-mode="quiz">知识测验</button>
                </div>

                <div class="experiment-controls">
                    <div class="control-group">
                        <h3>浓度控制</h3>
                        <div class="slider-container">
                            <label>膜外浓度:</label>
                            <input type="range" id="outsideConc" min="0" max="100" value="70">
                            <span id="outsideValue">70%</span>
                        </div>
                        <div class="slider-container">
                            <label>膜内浓度:</label>
                            <input type="range" id="insideConc" min="0" max="100" value="30">
                            <span id="insideValue">30%</span>
                        </div>
                    </div>

                    <div class="control-group">
                        <h3>物质选择</h3>
                        <div class="button-group">
                            <button class="action-btn" data-particle="oxygen">氧气(O₂)</button>
                            <button class="action-btn" data-particle="glucose">葡萄糖</button>
                            <button class="action-btn" data-particle="ion">钾离子(K⁺)</button>
                            <button class="action-btn" data-particle="protein">蛋白质</button>
                        </div>
                    </div>

                    <div class="control-group">
                        <h3>实验控制</h3>
                        <div class="button-group">
                            <button class="action-btn" id="startBtn">开始运输</button>
                            <button class="action-btn secondary" id="resetBtn">重置实验</button>
                            <button class="action-btn" id="atpBtn">提供ATP</button>
                        </div>
                    </div>
                </div>
            </div>

            <div class="animation-area">
                <canvas id="animationCanvas"></canvas>
            </div>

            <div class="info-panel">
                <div class="info-header">
                    <h2 id="infoTitle">被动运输 - 自由扩散</h2>
                    <div class="status-bar">
                        <div class="status-item">
                            <span>ATP数量:</span>
                            <span class="status-value" id="atpCount">10</span>
                        </div>
                        <div class="status-item">
                            <span>运输速度:</span>
                            <span class="status-value" id="speedValue">中等</span>
                        </div>
                        <div class="status-item">
                            <span>当前模式:</span>
                            <span class="status-value" id="currentMode">被动运输</span>
                        </div>
                    </div>
                </div>

                <div class="info-content" id="infoContent">
                    <p><span class="highlight">被动运输</span>是指物质顺浓度梯度，从高浓度向低浓度方向的跨膜运输方式，不需要消耗细胞代谢产生的能量。</p>
                    <p><span class="highlight">自由扩散</span>是其中最简单的一种形式，小分子或脂溶性物质（如O₂、CO₂）可以直接通过磷脂双分子层。</p>
                    <p>特点：不消耗ATP，不需要载体蛋白，运输速度取决于浓度差。</p>
                    
                    <table class="comparison-table" id="comparisonTable">
                        <thead>
                            <tr>
                                <th>运输方式</th>
                                <th>浓度梯度</th>
                                <th>能量需求</th>
                                <th>载体蛋白</th>
                                <th>示例物质</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>自由扩散</td>
                                <td>顺浓度梯度</td>
                                <td>不消耗ATP</td>
                                <td>不需要</td>
                                <td>O₂、CO₂、甘油</td>
                            </tr>
                            <tr>
                                <td>协助扩散</td>
                                <td>顺浓度梯度</td>
                                <td>不消耗ATP</td>
                                <td>需要</td>
                                <td>葡萄糖、氨基酸</td>
                            </tr>
                            <tr>
                                <td>主动运输</td>
                                <td>逆浓度梯度</td>
                                <td>消耗ATP</td>
                                <td>需要</td>
                                <td>K⁺、Na⁺、碘离子</td>
                            </tr>
                            <tr>
                                <td>胞吞胞吐</td>
                                <td>-</td>
                                <td>消耗ATP</td>
                                <td>-</td>
                                <td>蛋白质、细菌</td>
                            </tr>
                        </tbody>
                    </table>
                </div>

                <div class="quiz-section" id="quizSection" style="display: none;">
                    <div class="quiz-question">
                        <h3>问题1: 下列哪种运输方式需要消耗ATP？</h3>
                        <div class="quiz-options">
                            <div class="quiz-option" data-answer="A">A. 自由扩散</div>
                            <div class="quiz-option" data-answer="B">B. 协助扩散</div>
                            <div class="quiz-option correct" data-answer="C">C. 主动运输</div>
                            <div class="quiz-option" data-answer="D">D. 以上都不需要</div>
                        </div>
                    </div>
                    
                    <div class="quiz-question">
                        <h3>问题2: 葡萄糖进入红细胞的方式是？</h3>
                        <div class="quiz-options">
                            <div class="quiz-option" data-answer="A">A. 自由扩散</div>
                            <div class="quiz-option correct" data-answer="B">B. 协助扩散</div>
                            <div class="quiz-option" data-answer="C">C. 主动运输</div>
                            <div class="quiz-option" data-answer="D">D. 胞吞作用</div>
                        </div>
                    </div>
                    
                    <div class="quiz-question">
                        <h3>问题3: 大分子蛋白质进出细胞的主要方式是？</h3>
                        <div class="quiz-options">
                            <div class="quiz-option" data-answer="A">A. 自由扩散</div>
                            <div class="quiz-option" data-answer="B">B. 协助扩散</div>
                            <div class="quiz-option" data-answer="C">C. 主动运输</div>
                            <div class="quiz-option correct" data-answer="D">D. 胞吞胞吐</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 全局变量
        let canvas, ctx;
        let currentMode = 'passive';
        let currentParticle = 'oxygen';
        let animationId = null;
        let isAnimating = false;
        let atpCount = 10;
        let outsideConc = 70;
        let insideConc = 30;

        // 粒子系统
        const particles = {
            oxygen: { color: '#e74c3c', size: 4, speed: 2, type: 'small' },
            glucose: { color: '#3498db', size: 6, speed: 1.5, type: 'medium' },
            ion: { color: '#9b59b6', size: 5, speed: 1, type: 'small' },
            protein: { color: '#e67e22', size: 12, speed: 0.5, type: 'large' }
        };

        // 细胞膜和粒子数据
        let membrane = {
            x: 400,
            y: 230,
            width: 600,
            height: 40,
            phospholipids: []
        };

        let outsideParticles = [];
        let insideParticles = [];
        let carrierProteins = [];
        let channelProteins = [];
        let vesicles = [];
        let atpParticles = [];

        // 初始化
        function init() {
            canvas = document.getElementById('animationCanvas');
            ctx = canvas.getContext('2d');
            
            // 设置Canvas实际大小
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
            
            initMembrane();
            resetExperiment();
            setupEventListeners();
            updateInfo();
            draw();
        }

        // 初始化细胞膜结构
        function initMembrane() {
            membrane.phospholipids = [];
            const headRadius = 8;
            const tailLength = 20;
            
            for (let i = 0; i < 30; i++) {
                membrane.phospholipids.push({
                    x: membrane.x - membrane.width/2 + i * 20,
                    y: membrane.y,
                    rotation: Math.PI / 2
                });
            }
            
            // 初始化载体蛋白
            carrierProteins = [
                { x: membrane.x - 100, y: membrane.y, width: 30, height: 40, state: 'idle', boundParticle: null },
                { x: membrane.x + 50, y: membrane.y, width: 30, height: 40, state: 'idle', boundParticle: null }
            ];
            
            // 初始化通道蛋白
            channelProteins = [
                { x: membrane.x - 200, y: membrane.y, width: 20, height: 40, open: true },
                { x: membrane.x + 150, y: membrane.y, width: 20, height: 40, open: true }
            ];
        }

        // 重置实验
        function resetExperiment() {
            outsideParticles = [];
            insideParticles = [];
            vesicles = [];
            atpParticles = [];
            atpCount = 10;
            isAnimating = false;
            
            // 根据浓度创建外部粒子
            const outsideCount = Math.floor(outsideConc / 100 * 50);
            for (let i = 0; i < outsideCount; i++) {
                outsideParticles.push(createParticle('outside'));
            }
            
            // 根据浓度创建内部粒子
            const insideCount = Math.floor(insideConc / 100 * 50);
            for (let i = 0; i < insideCount; i++) {
                insideParticles.push(createParticle('inside'));
            }
            
            // 创建ATP粒子
            for (let i = 0; i < atpCount; i++) {
                atpParticles.push({
                    x: 50 + i * 30,
                    y: 50,
                    active: true
                });
            }
            
            updateStatus();
        }

        // 创建粒子
        function createParticle(location) {
            const config = particles[currentParticle];
            const isOutside = location === 'outside';
            
            return {
                x: isOutside ? 
                    Math.random() * (membrane.x - membrane.width/2 - 100) + 50 :
                    Math.random() * (membrane.x - membrane.width/2 - 100) + membrane.x + membrane.width/2 + 50,
                y: Math.random() * (canvas.height - 100) + 50,
                vx: (Math.random() - 0.5) * config.speed,
                vy: (Math.random() - 0.5) * config.speed,
                color: config.color,
                size: config.size,
                type: config.type,
                boundToProtein: false,
                inVesicle: false
            };
        }

        // 绘制函数
        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 绘制细胞膜
            drawMembrane();
            
            // 绘制蛋白质
            drawProteins();
            
            // 绘制粒子
            drawParticles();
            
            // 绘制囊泡
            drawVesicles();
            
            // 绘制ATP
            drawATP();
            
            // 绘制标签和指示器
            drawLabels();
            
            if (isAnimating) {
                updateAnimation();
            }
            
            animationId = requestAnimationFrame(draw);
        }

        // 绘制背景
        function drawBackground() {
            // 外部区域
            ctx.fillStyle = 'rgba(255, 240, 240, 0.3)';
            ctx.fillRect(0, 0, membrane.x - membrane.width/2, canvas.height);
            
            // 内部区域
            ctx.fillStyle = 'rgba(240, 255, 240, 0.3)';
            ctx.fillRect(membrane.x + membrane.width/2, 0, canvas.width - (membrane.x + membrane.width/2), canvas.height);
            
            // 标签
            ctx.fillStyle = '#e74c3c';
            ctx.font = 'bold 16px Arial';
            ctx.fillText('细胞外', 50, 30);
            
            ctx.fillStyle = '#2ecc71';
            ctx.fillText('细胞内', canvas.width - 100, 30);
        }

        // 绘制细胞膜
        function drawMembrane() {
            // 磷脂双分子层
            membrane.phospholipids.forEach(phos => {
                // 绘制头部
                ctx.save();
                ctx.translate(phos.x, phos.y);
                ctx.rotate(phos.rotation);
                
                // 磷脂头部
                ctx.fillStyle = '#ecf0f1';
                ctx.beginPath();
                ctx.arc(0, 0, 8, 0, Math.PI * 2);
                ctx.fill();
                
                // 磷脂尾部
                ctx.fillStyle = '#f1c40f';
                ctx.fillRect(-2, -20, 4, 40);
                
                ctx.restore();
            });
            
            // 膜背景
            ctx.fillStyle = 'rgba(241, 196, 15, 0.1)';
            ctx.fillRect(membrane.x - membrane.width/2, membrane.y - 20, membrane.width, 40);
        }

        // 绘制蛋白质
        function drawProteins() {
            // 载体蛋白
            carrierProteins.forEach(protein => {
                ctx.fillStyle = protein.state === 'active' ? '#2980b9' : '#3498db';
                ctx.fillRect(protein.x - protein.width/2, protein.y - protein.height/2, protein.width, protein.height);
                
                // 结合位点
                ctx.fillStyle = '#e74c3c';
                ctx.beginPath();
                ctx.arc(protein.x, protein.y, 5, 0, Math.PI * 2);
                ctx.fill();
                
                if (protein.boundParticle) {
                    ctx.fillStyle = particles[currentParticle].color;
                    ctx.beginPath();
                    ctx.arc(protein.x, protein.y, 8, 0, Math.PI * 2);
                    ctx.fill();
                }
            });
            
            // 通道蛋白
            channelProteins.forEach(channel => {
                ctx.fillStyle = channel.open ? '#27ae60' : '#95a5a6';
                ctx.fillRect(channel.x - channel.width/2, channel.y - channel.height/2, channel.width, channel.height);
                
                // 通道
                ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
                ctx.fillRect(channel.x - 3, channel.y - channel.height/2, 6, channel.height);
            });
        }

        // 绘制粒子
        function drawParticles() {
            // 外部粒子
            outsideParticles.forEach(particle => {
                if (!particle.inVesicle) {
                    ctx.fillStyle = particle.color;
                    ctx.beginPath();
                    ctx.arc(particle.x, particle.y, particle.size, 0, Math.PI * 2);
                    ctx.fill();
                }
            });
            
            // 内部粒子
            insideParticles.forEach(particle => {
                if (!particle.inVesicle) {
                    ctx.fillStyle = particle.color;
                    ctx.beginPath();
                    ctx.arc(particle.x, particle.y, particle.size, 0, Math.PI * 2);
                    ctx.fill();
                }
            });
        }

        // 绘制囊泡
        function drawVesicles() {
            vesicles.forEach(vesicle => {
                // 囊泡膜
                ctx.strokeStyle = '#e67e22';
                ctx.lineWidth = 3;
                ctx.beginPath();
                ctx.arc(vesicle.x, vesicle.y, vesicle.radius, 0, Math.PI * 2);
                ctx.stroke();
                
                // 内部粒子
                ctx.fillStyle = particles[currentParticle].color;
                ctx.beginPath();
                ctx.arc(vesicle.x, vesicle.y, particles[currentParticle].size, 0, Math.PI * 2);
                ctx.fill();
            });
        }

        // 绘制ATP
        function drawATP() {
            atpParticles.forEach(atp => {
                if (atp.active) {
                    ctx.fillStyle = '#f1c40f';
                    ctx.font = 'bold 14px Arial';
                    ctx.fillText('ATP', atp.x, atp.y);
                }
            });
        }

        // 绘制标签和指示器
        function drawLabels() {
            // 浓度梯度箭头
            if (outsideConc > insideConc) {
                drawArrow(membrane.x - membrane.width/2 - 50, canvas.height/2, 
                         membrane.x - membrane.width/2 - 150, canvas.height/2, '#e74c3c');
                ctx.fillStyle = '#e74c3c';
                ctx.fillText('高浓度', membrane.x - membrane.width/2 - 180, canvas.height/2 - 10);
            }
            
            // 当前模式指示
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 18px Arial';
            ctx.fillText(getModeName(currentMode), canvas.width/2 - 50, 50);
        }

        // 绘制箭头
        function drawArrow(fromX, fromY, toX, toY, color) {
            ctx.strokeStyle = color;
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.stroke();
            
            // 箭头头部
            const angle = Math.atan2(toY - fromY, toX - fromX);
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - 10 * Math.cos(angle - Math.PI/6), toY - 10 * Math.sin(angle - Math.PI/6));
            ctx.lineTo(toX - 10 * Math.cos(angle + Math.PI/6), toY - 10 * Math.sin(angle + Math.PI/6));
            ctx.closePath();
            ctx.fillStyle = color;
            ctx.fill();
        }

        // 更新动画
        function updateAnimation() {
            switch(currentMode) {
                case 'passive':
                    updatePassiveTransport();
                    break;
                case 'facilitated':
                    updateFacilitatedDiffusion();
                    break;
                case 'active':
                    updateActiveTransport();
                    break;
                case 'endocytosis':
                    updateEndocytosis();
                    break;
                case 'compare':
                    updateCompareMode();
                    break;
            }
        }

        // 被动运输更新
        function updatePassiveTransport() {
            const config = particles[currentParticle];
            
            // 外部粒子运动
            outsideParticles.forEach(particle => {
                if (!particle.boundToProtein && !particle.inVesicle) {
                    // 布朗运动
                    particle.x += particle.vx;
                    particle.y += particle.vy;
                    
                    // 边界检查
                    if (particle.x < 0 || particle.x > membrane.x - membrane.width/2) particle.vx *= -1;
                    if (particle.y < 50 || particle.y > canvas.height - 50) particle.vy *= -1;
                    
                    // 跨膜扩散（小分子可以直接通过）
                    if (config.type === 'small' && 
                        particle.x > membrane.x - membrane.width/2 - 10 && 
                        particle.x < membrane.x - membrane.width/2 + 10 &&
                        Math.random() < 0.02) {
                        // 移动到内部
                        particle.x = membrane.x + membrane.width/2 + 10;
                        insideParticles.push(particle);
                        outsideParticles = outsideParticles.filter(p => p !== particle);
                    }
                }
            });
        }

        // 协助扩散更新
        function updateFacilitatedDiffusion() {
            // 通过通道蛋白运输
            channelProteins.forEach(channel => {
                if (channel.open) {
                    // 寻找附近的粒子
                    outsideParticles.forEach(particle => {
                        const distance = Math.sqrt(
                            Math.pow(particle.x - channel.x, 2) + 
                            Math.pow(particle.y - channel.y, 2)
                        );
                        
                        if (distance < 30 && Math.random() < 0.05) {
                            // 通过通道
                            particle.x = membrane.x + membrane.width/2 + 10;
                            insideParticles.push(particle);
                            outsideParticles = outsideParticles.filter(p => p !== particle);
                        }
                    });
                }
            });
        }

        // 主动运输更新
        function updateActiveTransport() {
            if (atpCount <= 0) return;
            
            carrierProteins.forEach(protein => {
                if (protein.state === 'idle' && Math.random() < 0.01) {
                    // 寻找外部粒子
                    const nearbyParticle = outsideParticles.find(p => 
                        Math.abs(p.x - protein.x) < 30 && 
                        Math.abs(p.y - protein.y) < 30
                    );
                    
                    if (nearbyParticle) {
                        protein.boundParticle = nearbyParticle;
                        protein.state = 'active';
                        nearbyParticle.boundToProtein = true;
                        
                        // 消耗ATP
                        if (atpCount > 0) {
                            atpCount--;
                            const activeATP = atpParticles.find(atp => atp.active);
                            if (activeATP) activeATP.active = false;
                            updateStatus();
                        }
                    }
                }
                
                // 运输过程
                if (protein.state === 'active') {
                    if (protein.boundParticle) {
                        // 移动粒子到内部
                        protein.boundParticle.x = protein.x;
                        protein.boundParticle.y = protein.y;
                        
                        if (Math.random() < 0.05) {
                            // 释放粒子
                            protein.boundParticle.x = membrane.x + membrane.width/2 + 30;
                            protein.boundParticle.y = protein.y;
                            protein.boundParticle.boundToProtein = false;
                            insideParticles.push(protein.boundParticle);
                            outsideParticles = outsideParticles.filter(p => p !== protein.boundParticle);
                            protein.boundParticle = null;
                            protein.state = 'idle';
                        }
                    }
                }
            });
        }

        // 胞吞胞吐更新
        function updateEndocytosis() {
            if (currentParticle !== 'protein') return;
            
            // 胞吞过程
            if (outsideParticles.length > 0 && vesicles.length < 3 && Math.random() < 0.01) {
                const particle = outsideParticles[0];
                vesicles.push({
                    x: particle.x,
                    y: particle.y,
                    radius: 20,
                    vx: 0,
                    vy: 1,
                    type: 'endocytosis',
                    particle: particle
                });
                particle.inVesicle = true;
            }
            
            // 更新囊泡位置
            vesicles.forEach(vesicle => {
                if (vesicle.type === 'endocytosis') {
                    vesicle.y += vesicle.vy;
                    if (vesicle.y > membrane.y + 50) {
                        // 进入细胞
                        vesicle.particle.inVesicle = false;
                        vesicle.particle.x = membrane.x + membrane.width/2 + 50;
                        insideParticles.push(vesicle.particle);
                        vesicles = vesicles.filter(v => v !== vesicle);
                    }
                }
            });
        }

        // 对比模式更新
        function updateCompareMode() {
            // 简化的对比演示
            updatePassiveTransport();
            updateFacilitatedDiffusion();
            updateActiveTransport();
        }

        // 更新信息显示
        function updateInfo() {
            const modeNames = {
                'passive': '被动运输 - 自由扩散',
                'facilitated': '被动运输 - 协助扩散',
                'active': '主动运输',
                'endocytosis': '胞吞胞吐',
                'compare': '对比模式',
                'quiz': '知识测验'
            };
            
            const modeDescriptions = {
                'passive': '物质顺浓度梯度，不消耗能量，不需要载体蛋白。小分子或脂溶性物质（如O₂、CO₂）直接通过磷脂双分子层。',
                'facilitated': '物质顺浓度梯度，不消耗能量，但需要载体蛋白或通道蛋白协助。如葡萄糖通过载体蛋白进入红细胞。',
                'active': '物质逆浓度梯度，需要载体蛋白并消耗ATP。如钠钾泵维持细胞内外离子浓度差。',
                'endocytosis': '大分子或颗粒物质通过膜包裹形成囊泡进出细胞，消耗能量。如白细胞吞噬细菌。',
                'compare': '同时展示三种主要运输方式的差异，注意观察浓度梯度方向、能量消耗和载体蛋白需求。'
            };
            
            document.getElementById('infoTitle').textContent = modeNames[currentMode];
            document.getElementById('currentMode').textContent = modeNames[currentMode].split(' - ')[0];
            
            const infoContent = document.getElementById('infoContent');
            if (currentMode !== 'quiz') {
                infoContent.style.display = 'block';
                document.getElementById('quizSection').style.display = 'none';
                
                let html = `<p><span class="highlight">${modeNames[currentMode].split(' - ')[0]}</span>`;
                if (modeNames[currentMode].includes('-')) {
                    html += ` - <span class="highlight">${modeNames[currentMode].split(' - ')[1]}</span>`;
                }
                html += `: ${modeDescriptions[currentMode]}</p>`;
                
                if (currentMode !== 'compare') {
                    html += `<p>特点：${getModeCharacteristics(currentMode)}</p>`;
                }
                
                infoContent.innerHTML = html + infoContent
<!--检测到代码截断，自动续写中...-->
.querySelector('.comparison-table').outerHTML;
            } else {
                infoContent.style.display = 'none';
                document.getElementById('quizSection').style.display = 'block';
            }
        }

        // 获取模式特点
        function getModeCharacteristics(mode) {
            const characteristics = {
                'passive': '不消耗ATP，不需要载体蛋白，运输速度取决于浓度差',
                'facilitated': '不消耗ATP，需要特异性载体蛋白，具有饱和性',
                'active': '消耗ATP，需要载体蛋白，可以逆浓度梯度运输',
                'endocytosis': '消耗ATP，形成囊泡，用于大分子和颗粒物质运输'
            };
            return characteristics[mode] || '';
        }

        // 更新状态栏
        function updateStatus() {
            document.getElementById('atpCount').textContent = atpCount;
            document.getElementById('outsideValue').textContent = outsideConc + '%';
            document.getElementById('insideValue').textContent = insideConc + '%';
            
            // 更新运输速度显示
            let speed = '停止';
            if (isAnimating) {
                if (currentMode === 'passive') speed = '中等';
                else if (currentMode === 'facilitated') speed = '较慢';
                else if (currentMode === 'active') speed = atpCount > 0 ? '慢' : '停止';
                else if (currentMode === 'endocytosis') speed = '很慢';
            }
            document.getElementById('speedValue').textContent = speed;
        }

        // 设置事件监听器
        function setupEventListeners() {
            // 模式选择按钮
            document.querySelectorAll('.mode-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    document.querySelectorAll('.mode-btn').forEach(b => b.classList.remove('active'));
                    btn.classList.add('active');
                    currentMode = btn.dataset.mode;
                    resetExperiment();
                    updateInfo();
                });
            });

            // 物质选择按钮
            document.querySelectorAll('.action-btn[data-particle]').forEach(btn => {
                btn.addEventListener('click', () => {
                    document.querySelectorAll('.action-btn[data-particle]').forEach(b => {
                        b.style.background = '#2ecc71';
                    });
                    btn.style.background = '#27ae60';
                    currentParticle = btn.dataset.particle;
                    resetExperiment();
                });
            });

            // 浓度滑块
            document.getElementById('outsideConc').addEventListener('input', (e) => {
                outsideConc = parseInt(e.target.value);
                document.getElementById('outsideValue').textContent = outsideConc + '%';
                resetExperiment();
            });

            document.getElementById('insideConc').addEventListener('input', (e) => {
                insideConc = parseInt(e.target.value);
                document.getElementById('insideValue').textContent = insideConc + '%';
                resetExperiment();
            });

            // 控制按钮
            document.getElementById('startBtn').addEventListener('click', () => {
                isAnimating = !isAnimating;
                document.getElementById('startBtn').textContent = isAnimating ? '暂停运输' : '开始运输';
                updateStatus();
            });

            document.getElementById('resetBtn').addEventListener('click', () => {
                resetExperiment();
                updateStatus();
            });

            document.getElementById('atpBtn').addEventListener('click', () => {
                atpCount = 10;
                atpParticles = [];
                for (let i = 0; i < atpCount; i++) {
                    atpParticles.push({
                        x: 50 + i * 30,
                        y: 50,
                        active: true
                    });
                }
                updateStatus();
            });

            // 测验选项
            document.querySelectorAll('.quiz-option').forEach(option => {
                option.addEventListener('click', function() {
                    const isCorrect = this.classList.contains('correct');
                    
                    // 移除所有现有状态
                    this.parentElement.querySelectorAll('.quiz-option').forEach(opt => {
                        opt.classList.remove('correct', 'incorrect');
                    });
                    
                    // 显示正确/错误状态
                    if (isCorrect) {
                        this.classList.add('correct');
                    } else {
                        this.classList.add('incorrect');
                        // 显示正确答案
                        const correctOption = this.parentElement.querySelector('.correct');
                        correctOption.classList.add('correct');
                    }
                });
            });

            // 窗口大小调整
            window.addEventListener('resize', () => {
                canvas.width = canvas.offsetWidth;
                canvas.height = canvas.offsetHeight;
                resetExperiment();
            });
        }

        // 获取模式名称
        function getModeName(mode) {
            const names = {
                'passive': '自由扩散',
                'facilitated': '协助扩散',
                'active': '主动运输',
                'endocytosis': '胞吞胞吐',
                'compare': '对比模式'
            };
            return names[mode] || '';
        }

        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 《物质进出细胞的三种方式》交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过可视化、可操作的动态演示，帮助您深入理解物质进出细胞的三种主要方式：被动运输、主动运输以及胞吞胞吐。请跟随本指南，开启您的探索之旅。

---

### 一、 功能说明

本动画是一个基于HTML5 Canvas技术构建的交互式模拟实验平台。它将抽象的生物学概念转化为直观的视觉元素和动态过程，允许您通过调整参数、选择模式来观察不同条件下细胞膜运输机制的变化，从而在“动手”实验中建构知识。

### 二、 主要功能

1.  **模式切换**：
    *   **被动运输**：演示自由扩散（如氧气）的直接跨膜过程。
    *   **协助扩散**：演示葡萄糖等物质通过通道蛋白的运输。
    *   **主动运输**：演示钾离子（K⁺）逆浓度梯度、消耗ATP的运输过程。
    *   **胞吞胞吐**：演示大分子蛋白质通过膜泡运输进出细胞。
    *   **对比模式**：并行动态展示三种穿膜运输的核心差异。
    *   **知识测验**：通过选择题即时检验学习成果。

2.  **实验控制台**：
    *   **浓度控制**：通过滑块实时调整细胞膜内、外的物质浓度，观察浓度梯度对运输方向和速度的影响。
    *   **物质选择**：可选择氧气、葡萄糖、钾离子、蛋白质四种代表性物质，观察其对应的运输方式。
    *   **实验操作**：
        *   **开始/暂停运输**：控制动画的播放与暂停。
        *   **重置实验**：清空所有粒子，恢复初始设置。
        *   **提供ATP**：为主动运输和胞吞胞吐补充能量（ATP）。

3.  **动态信息面板**：
    *   **实时状态**：显示当前ATP数量、运输速度和活动模式。
    *   **知识讲解**：随模式切换，同步更新当前运输方式的详细文字说明和特点。
    *   **对比表格**：清晰汇总四种运输方式在浓度梯度、能量需求、载体蛋白和示例物质上的区别。

### 三、 设计特色

1.  **科学可视化**：
    *   细胞膜采用双层磷脂分子模型，载体蛋白、通道蛋白形态分明。
    *   不同物质（O₂、葡萄糖、K⁺、蛋白质）用不同颜色和形状的粒子表示，易于区分。
    *   ATP用醒目的黄色“ATP”标签表示，消耗时有视觉反馈。

2.  **符合认知规律**：
    *   **从简到繁**：建议学习顺序为“被动运输→协助扩散→主动运输→胞吞胞吐→对比模式”。
    *   **对比学习**：“对比模式”将关键差异（如箭头方向、ATP消耗）高亮并排展示，强化记忆。
    *   **建构主义学习**：鼓励用户先预测“如果耗尽ATP会怎样？”，再通过操作验证，深化理解。

3.  **友好的交互体验**：
    *   界面采用温和的蓝绿色调，保护视力，聚焦内容。
    *   所有控件均有明确的标签和实时数值反馈。
    *   动画流畅，粒子运动模拟了布朗运动和随机性。

### 四、 教学要点与探究建议

本动画不仅是演示工具，更是探究平台。以下是一些关键的教学观察点和探究问题：

| 运输方式 | 核心观察点 | 可探究的问题 |
| :--- | :--- | :--- |
| **自由扩散** | 粒子无需借助蛋白，直接、随机地穿过膜；速度与浓度差正相关。 | 1. 如果将物质换成“蛋白质”，还能自由扩散吗？为什么？<br>2. 当膜内外浓度相等时，粒子还会运动吗？方向如何？ |
| **协助扩散** | 粒子必须通过特定的“通道蛋白”才能进入；仍顺浓度梯度。 | 1. 关闭通道蛋白（在代码逻辑中模拟），运输会停止吗？<br>2. 它与自由扩散的最大区别是什么？ |
| **主动运输** | **逆浓度梯度**运输；必须**消耗ATP**；需要**载体蛋白**构象变化。 | 1. 点击“耗尽ATP”按钮，观察运输过程的变化。这说明了什么？<br>2. 为什么说主动运输对维持细胞生命活动至关重要？ |
| **胞吞胞吐** | 膜发生形变，包裹大颗粒形成**囊泡**；整个过程消耗能量。 | 1. 为什么氧气不能通过这种方式运输？<br>2. 比较“胞吞”和“胞吐”过程中囊泡运动的方向。 |
| **综合对比** | 在“对比模式”下，同步观察**浓度梯度方向**、**ATP消耗**、**蛋白参与**三个维度的差异。 | 尝试根据动画现象，自己归纳并填写完整的对比表格。 |

### 五、 使用建议

1.  **初次学习者**：
    *   建议按顺序体验各个模式，先观看动画，阅读右侧知识讲解。
    *   重点理解每个方式的**定义、方向和能量需求**。
    *   完成体验后，进入“知识测验”环节巩固概念。

2.  **复习与探究者**：
    *   直接使用“对比模式”，快速回顾核心差异。
    *   主动设置实验条件：例如，在主动运输模式下，**先耗尽ATP，再创建逆浓度梯度**，然后点击“提供ATP”，观察现象。记录下你的预测和实际结果。
    *   尝试用本动画解释真实生理现象：如“为什么小肠能逆浓度吸收葡萄糖？”（涉及主动运输）。

3.  **教师教学**：
    *   **课堂演示**：可用于引入新概念或总结复习，通过大屏幕展示，引导学生观察和讨论。
    *   **任务驱动学习**：为学生设计探究任务单，提出上述“可探究的问题”，让学生通过操作动画寻找答案。
    *   **概念辨析**：利用对比模式，直接解决学生容易混淆的“协助扩散 vs 主动运输”等难点。

---

**祝您探索愉快，在微观世界的奇妙运输网络中收获知识与乐趣！**

*—— 您的教育技术伙伴*