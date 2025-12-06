# 需求：酯化反应微观机理（羧酸+醇→酯+水，显示原子重组）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：高中化学或大学基础有机化学的学生。他们已具备基本的原子、分子、化学键和官能团知识，但需要直观理解酯化反应的动态过程。
2.  **核心需求**：用户不仅需要知道酯化反应的宏观方程式（羧酸+醇→酯+水），更需要理解其微观机理，即原子如何断开、重组，特别是“酸脱羟基醇脱氢”这一核心步骤的电子转移和原子运动过程。
3.  **认知难点**：
    *   理解反应中心（羧基的羰基碳和羟基氧，醇的羟基氢和氧）的识别。
    *   可视化共价键的断裂与形成是“协同”或“分步”进行的。
    *   理解质子（H⁺）在反应中的催化作用及其转移路径。
    *   将二维结构式与三维空间中的分子接近、碰撞、重组过程联系起来。
4.  **期望成果**：通过交互式动画，用户能自主探索反应步骤，形成深刻、准确的动态心智模型，从而能预测或解释类似反应。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念聚焦**：
    1.  **亲核加成-消除机理**：明确展示羰基碳的正电性（δ+）和醇羟基氧的孤对电子，这是反应的驱动力。
    2.  **键的断裂与形成**：重点展示C-O键、O-H键的断裂和C-O键、O-H键（在水分子中）的形成过程。用颜色和动画突出“酸脱-OH”和“醇脱-H”的最终结果。
    3.  **质子转移与催化**：清晰展示质子（H⁺）从醇羟基转移到羧基氧，再转移回中间体，最后形成水分子的全过程，强调其降低反应活化能的作用。
    4.  **可逆反应**：通过“播放/倒放”功能，暗示酯化反应的可逆性（酯的水解）。

*   **遵循认知规律**：
    1.  **从整体到局部**：先展示完整的反应物分子（乙酸和乙醇）相互靠近，再高亮并聚焦于反应中心（官能团），最后放大展示电子和原子的运动。
    2.  **分步讲解**：将连续的反应分解为清晰的、可暂停的步骤（如：质子化、亲核进攻、质子转移、消除、去质子化），每一步都伴有简明的文字说明。
    3.  **减少认知负荷**：在非反应部位进行视觉降级（如半透明化、简化表示），确保注意力集中在关键原子和键上。

*   **交互设计**：
    1.  **用户控制节奏**：提供“播放/暂停/步进/重置”控件，允许学习者按自己的速度学习。
    2.  **探索式学习**：设计“高亮”交互，当鼠标悬停在特定原子或键上时，显示其角色（如“亲电中心”、“亲核试剂”、“将断裂的键”）。
    3.  **视角切换**：提供“宏观方程式视图”和“微观机理视图”的切换按钮，帮助学生在符号表征与粒子模型间建立联系。
    4.  **过程提示**：在关键步骤旁，以动态箭头和简短文本（如“亲核进攻”、“质子转移”）提示正在发生的化学事件。

*   **视觉呈现**：
    1.  **分子模型**：采用“球棍模型”，清晰展示原子和键。原子球大小适中，键的粗细能体现单键/双键区别。
    2.  **动态与路径**：使用平滑的补间动画表现分子的平移、旋转。用流动的彩色光点或虚线箭头表示电子对的移动方向。用清晰的轨迹线表示质子（H⁺）的转移路径。
    3.  **状态与变化**：
        *   **断裂的键**：闪烁后变为虚线并分开。
        *   **新形成的键**：从无到有，以生长动画呈现。
        *   **电荷变化**：用“δ+”和“δ-”符号的动态显示来体现原子电负性差异和中间体的电荷分布。
    4.  **信息分层**：背景简洁（浅色渐变），分子色彩鲜明，说明文字清晰且位置固定。

#### 配色方案选择
*   **原子颜色**：采用CPK配色方案，增强化学识别度。
    *   碳（C）：深灰色
    *   氢（H）：浅灰色或白色
    *   氧（O）：红色
    *   （可扩展）用于催化作用的**质子（H⁺）**：使用醒目的**亮黄色**或**粉色**，以区别于共价键中的氢。
*   **功能与状态色**：
    *   **高亮/强调色**：**亮蓝色**或**青色**，用于高亮反应中心、电子流箭头。
    *   **断裂键**：**红色**闪烁后变虚。
    *   **新形成键**：**绿色**生长动画。
    *   **背景**：浅蓝灰或浅米色渐变，确保对比度。
    *   **界面控件**：中性深灰色，与内容区区分。

#### 交互功能列表
1.  **主控面板**：播放、暂停、下一步、上一步、重置动画按钮。
2.  **视图切换**：“宏观方程式” / “微观机理” 切换按钮。
3.  **步骤导航**：一个进度条或分步标签（如：步骤1: 质子化 -> 步骤2: 亲核进攻...），点击可跳转到特定步骤。
4.  **信息提示**：
    *   鼠标悬停在任一原子上，显示该元素符号及在反应中的角色（如“羰基碳，亲电中心”）。
    *   鼠标悬停在键上，显示键类型（单键/双键）及状态。
5.  **机理细节开关**：一个复选框，用于“显示/隐藏电子流箭头”和“显示/隐藏电荷符号”，供进阶学习者选择。
6.  **反应方向控制**：一个“可逆反应”开关，打开后，动画可从酯+水开始向反应物方向进行（水解），直观展示可逆性。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>酯化反应微观机理教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%);
            color: #333;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            padding: 25px;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 20px;
            border-bottom: 2px solid #eaeaea;
        }
        
        h1 {
            color: #2c3e50;
            font-size: 2.4rem;
            margin-bottom: 10px;
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.2rem;
            font-weight: normal;
        }
        
        .content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 25px;
        }
        
        .animation-section {
            flex: 1;
            min-width: 300px;
            background-color: #f8f9fa;
            border-radius: 12px;
            padding: 20px;
            box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.05);
        }
        
        .controls-section {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .equation-box {
            background-color: #fff;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            text-align: center;
            border: 2px solid #e3f2fd;
        }
        
        .equation {
            font-size: 2rem;
            font-weight: bold;
            color: #2c3e50;
            margin: 10px 0;
        }
        
        .equation .reactant {
            color: #3498db;
        }
        
        .equation .product {
            color: #e74c3c;
        }
        
        .equation .arrow {
            color: #7f8c8d;
            margin: 0 15px;
        }
        
        .control-panel {
            background-color: #fff;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            border: 2px solid #e8f5e9;
        }
        
        .control-panel h3, .info-panel h3 {
            color: #2c3e50;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #eee;
        }
        
        .buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-bottom: 20px;
        }
        
        button {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            background-color: #3498db;
            color: white;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 120px;
        }
        
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(52, 152, 219, 0.3);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        button#playBtn {
            background-color: #2ecc71;
        }
        
        button#pauseBtn {
            background-color: #f39c12;
        }
        
        button#resetBtn {
            background-color: #e74c3c;
        }
        
        .step-buttons {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
        }
        
        .step-buttons button {
            flex: 1;
            margin: 0 5px;
            background-color: #9b59b6;
        }
        
        .view-toggle {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }
        
        .toggle-btn {
            padding: 10px 20px;
            background-color: #ecf0f1;
            color: #7f8c8d;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            margin: 0 5px;
        }
        
        .toggle-btn.active {
            background-color: #3498db;
            color: white;
        }
        
        .slider-container {
            margin-bottom: 20px;
        }
        
        .slider-container label {
            display: block;
            margin-bottom: 8px;
            color: #2c3e50;
            font-weight: bold;
        }
        
        .slider {
            width: 100%;
            height: 10px;
            border-radius: 5px;
            background: #ddd;
            outline: none;
            -webkit-appearance: none;
        }
        
        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
        }
        
        .info-panel {
            background-color: #fff;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            border: 2px solid #fff3e0;
        }
        
        .step-info {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            border-left: 4px solid #3498db;
        }
        
        .step-info h4 {
            color: #2c3e50;
            margin-bottom: 8px;
        }
        
        .step-info p {
            color: #555;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            margin-right: 15px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            margin-right: 8px;
        }
        
        .legend-text {
            font-size: 0.9rem;
            color: #555;
        }
        
        canvas {
            display: block;
            margin: 0 auto;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        footer {
            text-align: center;
            margin-top: 25px;
            padding-top: 20px;
            border-top: 1px solid #eee;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .content {
                flex-direction: column;
            }
            
            .buttons {
                flex-direction: column;
            }
            
            button {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>酯化反应微观机理</h1>
            <p class="subtitle">羧酸 + 醇 → 酯 + 水 · 原子重组过程可视化</p>
        </header>
        
        <div class="content">
            <section class="animation-section">
                <div class="equation-box">
                    <h3>酯化反应方程式</h3>
                    <div class="equation">
                        <span class="reactant">CH₃COOH</span> + <span class="reactant">CH₃CH₂OH</span>
                        <span class="arrow">⇌</span>
                        <span class="product">CH₃COOCH₂CH₃</span> + <span class="product">H₂O</span>
                    </div>
                    <p>乙酸 + 乙醇 ⇌ 乙酸乙酯 + 水</p>
                </div>
                
                <div style="margin-top: 20px; text-align: center;">
                    <canvas id="reactionCanvas" width="800" height="500"></canvas>
                </div>
            </section>
            
            <section class="controls-section">
                <div class="control-panel">
                    <h3>动画控制</h3>
                    <div class="buttons">
                        <button id="playBtn">▶ 播放</button>
                        <button id="pauseBtn">⏸ 暂停</button>
                        <button id="resetBtn">↺ 重置</button>
                    </div>
                    
                    <div class="step-buttons">
                        <button id="prevStepBtn">◀ 上一步</button>
                        <button id="nextStepBtn">下一步 ▶</button>
                    </div>
                    
                    <div class="slider-container">
                        <label for="speedSlider">动画速度: <span id="speedValue">1.0x</span></label>
                        <input type="range" min="0.1" max="3" step="0.1" value="1" class="slider" id="speedSlider">
                    </div>
                    
                    <div class="view-toggle">
                        <div class="toggle-btn active" id="microViewBtn">微观机理视图</div>
                        <div class="toggle-btn" id="macroViewBtn">宏观方程式视图</div>
                    </div>
                    
                    <div class="slider-container">
                        <label for="stepSlider">反应进度: <span id="stepValue">步骤 0/6</span></label>
                        <input type="range" min="0" max="6" step="1" value="0" class="slider" id="stepSlider">
                    </div>
                </div>
                
                <div class="info-panel">
                    <h3>反应步骤说明</h3>
                    <div class="step-info" id="stepInfo">
                        <h4>准备开始</h4>
                        <p>动画将展示乙酸和乙醇分子在酸催化下的酯化反应机理。请点击"播放"按钮开始。</p>
                    </div>
                    
                    <h3 style="margin-top: 20px;">图例说明</h3>
                    <div class="legend">
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #555;"></div>
                            <div class="legend-text">碳原子 (C)</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #e74c3c;"></div>
                            <div class="legend-text">氧原子 (O)</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #ecf0f1; border: 1px solid #ccc;"></div>
                            <div class="legend-text">氢原子 (H)</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #f1c40f;"></div>
                            <div class="legend-text">质子 H⁺ (催化剂)</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #3498db;"></div>
                            <div class="legend-text">亲核进攻/电子流</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #2ecc71;"></div>
                            <div class="legend-text">新形成的键</div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
        
        <footer>
            <p>酯化反应微观机理教学动画 | 设计原理：亲核加成-消除机理 | 酸脱羟基，醇脱氢</p>
            <p>提示：将鼠标悬停在原子或键上可查看详细信息</p>
        </footer>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('reactionCanvas');
        const ctx = canvas.getContext('2d');
        
        // 调整Canvas大小以适应容器
        function resizeCanvas() {
            const container = canvas.parentElement;
            const containerWidth = container.clientWidth;
            
            // 保持宽高比
            const aspectRatio = canvas.width / canvas.height;
            canvas.width = Math.min(containerWidth - 40, 800);
            canvas.height = canvas.width / aspectRatio;
            
            // 重新绘制
            draw();
        }
        
        // 初始调整大小
        window.addEventListener('load', resizeCanvas);
        window.addEventListener('resize', resizeCanvas);
        
        // 动画状态
        let animationState = {
            currentStep: 0,
            totalSteps: 6,
            isPlaying: false,
            speed: 1.0,
            microView: true,
            progress: 0, // 每个步骤内的进度 (0-1)
            hoveredAtom: null,
            hoveredBond: null
        };
        
        // 分子数据
        const molecules = {
            aceticAcid: {
                name: "乙酸",
                atoms: [
                    { id: 1, element: "C", x: 200, y: 250, color: "#555" },
                    { id: 2, element: "C", x: 250, y: 250, color: "#555" },
                    { id: 3, element: "O", x: 275, y: 225, color: "#e74c3c" },
                    { id: 4, element: "O", x: 275, y: 275, color: "#e74c3c" },
                    { id: 5, element: "H", x: 175, y: 225, color: "#ecf0f1" },
                    { id: 6, element: "H", x: 175, y: 275, color: "#ecf0f1" },
                    { id: 7, element: "H", x: 200, y: 200, color: "#ecf0f1" },
                    { id: 8, element: "H", x: 300, y: 275, color: "#ecf0f1" }
                ],
                bonds: [
                    { from: 1, to: 2, type: "single" },
                    { from: 2, to: 3, type: "double" },
                    { from: 2, to: 4, type: "single" },
                    { from: 1, to: 5, type: "single" },
                    { from: 1, to: 6, type: "single" },
                    { from: 1, to: 7, type: "single" },
                    { from: 4, to: 8, type: "single" }
                ],
                initialX: 200,
                initialY: 250
            },
            ethanol: {
                name: "乙醇",
                atoms: [
                    { id: 9, element: "C", x: 450, y: 200, color: "#555" },
                    { id: 10, element: "C", x: 500, y: 200, color: "#555" },
                    { id: 11, element: "O", x: 525, y: 225, color: "#e74c3c" },
                    { id: 12, element: "H", x: 425, y: 175, color: "#ecf0f1" },
                    { id: 13, element: "H", x: 425, y: 225, color: "#ecf0f1" },
                    { id: 14, element: "H", x: 450, y: 150, color: "#ecf0f1" },
                    { id: 15, element: "H", x: 500, y: 150, color: "#ecf0f1" },
                    { id: 16, element: "H", x: 500, y: 250, color: "#ecf0f1" },
                    { id: 17, element: "H", x: 550, y: 225, color: "#ecf0f1" }
                ],
                bonds: [
                    { from: 9, to: 10, type: "single" },
                    { from: 10, to: 11, type: "single" },
                    { from: 9, to: 12, type: "single" },
                    { from: 9, to: 13, type: "single" },
                    { from: 9, to: 14, type: "single" },
                    { from: 10, to: 15, type: "single" },
                    { from: 10, to: 16, type: "single" },
                    { from: 11, to: 17, type: "single" }
                ],
                initialX: 450,
                initialY: 200
            },
            proton: {
                name: "质子 H⁺",
                atoms: [
                    { id: 18, element: "H", x: 600, y: 300, color: "#f1c40f" }
                ],
                bonds: [],
                initialX: 600,
                initialY: 300
            }
        };
        
        // 反应中间体和产物
        const intermediates = {
            ester: {
                name: "乙酸乙酯",
                atoms: [],
                bonds: []
            },
            water: {
                name: "水",
                atoms: [],
                bonds: []
            }
        };
        
        // 步骤信息
        const stepInfo = [
            {
                title: "步骤 1: 质子化",
                description: "质子 (H⁺) 与羧酸中的羰基氧结合，使羰基碳的正电性增强，更易受到亲核进攻。"
            },
            {
                title: "步骤 2: 亲核进攻",
                description: "乙醇中的氧原子（带有孤对电子）作为亲核试剂，进攻带正电的羰基碳原子。"
            },
            {
                title: "步骤 3: 质子转移",
                description: "中间体上的一个质子从氧原子转移到另一个氧原子上，形成更稳定的四面体中间体。"
            },
            {
                title: "步骤 4: 消除水分子",
                description: "质子化的羟基以水分子的形式离去（酸脱羟基），同时羰基重新形成。"
            },
            {
                title: "步骤 5: 去质子化",
                description: "酯分子释放一个质子 (H⁺)，催化剂再生，反应完成。"
            },
            {
                title: "反应完成",
                description: "生成乙酸乙酯和水分子，质子催化剂恢复原状，可继续催化下一个反应。"
            }
        ];
        
        // 绘制原子
        function drawAtom(atom, highlight = false) {
            const radius = atom.element === "H" ? 10 : 14;
            
            // 绘制原子球
            ctx.beginPath();
            ctx.arc(atom.x, atom.y, radius, 0, Math.PI * 2);
            
            // 设置颜色
            if (highlight) {
                ctx.fillStyle = "#3498db";
            } else {
                ctx.fillStyle = atom.color;
            }
            
            ctx.fill();
            
            // 绘制边框
            ctx.strokeStyle = "#333";
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 绘制元素符号
            ctx.fillStyle = atom.element === "H" ? "#333" : "#fff";
            ctx.font = atom.element === "H" ? "bold 12px Arial" : "bold 14px Arial";
            ctx.textAlign = "center";
            ctx.textBaseline = "middle";
            
            let symbol = atom.element;
            // 如果是质子，显示H⁺
            if (atom.id === 18) symbol = "H⁺";
            
            ctx.fillText(symbol, atom.x, atom.y);
            
            // 如果是羰基氧或醇羟基氧，在特定步骤显示电荷
            if ((atom.id === 3 || atom.id === 11) && animationState.currentStep >= 1 && animationState.currentStep <= 4) {
                ctx.fillStyle = "#e74c3c";
                ctx.font = "bold 16px Arial";
                const charge = atom.id === 3 && animationState.currentStep === 1 ? "δ+" : 
                              atom.id === 11 && animationState.currentStep >= 2 && animationState.currentStep <= 3 ? "δ-" : "";
                if (charge) {
                    ctx.fillText(charge, atom.x, atom.y - 25);
                }
            }
            
            // 如果是羰基碳，在步骤1显示δ+
            if (atom.id === 2 && animationState.currentStep === 1) {
                ctx.fillStyle = "#2c3e50";
                ctx.font = "bold 16px Arial";
                ctx.fillText("δ+", atom.x, atom.y - 25);
            }
            
            return {
                x: atom.x,
                y: atom.y,
                radius: radius,
                atom: atom
            };
        }
        
        // 绘制键
        function drawBond(bond, fromAtom, toAtom, highlight = false, forming = false, breaking = false) {
            // 计算键的起点和终点
            const dx = toAtom.x - fromAtom.x;
            const dy = toAtom.y - fromAtom.y;
            const distance = Math.sqrt(dx * dx + dy * dy);
            const angle = Math.atan2(dy, dx);
            
            // 计算原子半径
            const fromRadius = fromAtom.element === "H" ? 10 : 14;
            const toRadius = toAtom.element === "H" ? 10 : 14;
            
            // 计算实际连接点（从原子表面开始）
            const startX = fromAtom.x + (fromRadius * Math.cos(angle));
            const startY = fromAtom.y + (fromRadius * Math.sin(angle));
            const endX = toAtom.x - (toRadius * Math.cos(angle));
            const endY = toAtom.y - (toRadius * Math.sin(angle));
            
            // 设置键的样式
            if (forming) {
                ctx.strokeStyle = "#2ecc71"; // 绿色表示新形成的键
                ctx.lineWidth = 4;
                ctx.setLineDash([]);
            } else if (breaking) {
                ctx.strokeStyle = "#e74c3c"; // 红色表示断裂的键
                ctx.lineWidth = 3;
                ctx.setLineDash([5, 5]);
            } else if (highlight) {
                ctx.strokeStyle = "#3498db"; // 蓝色表示高亮
                ctx.lineWidth = 4;
                ctx.setLineDash([]);
            } else {
                ctx.strokeStyle = "#333"; // 默认颜色
                ctx.lineWidth = bond.type === "double" ? 4 : 3;
                ctx.setLineDash([]);
            }
            
            // 绘制键
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            ctx.lineTo(endX, endY);
            ctx.stroke();
            
            // 如果是双键，绘制第二条线
            if (bond.type === "double" && !breaking && !forming) {
                ctx.beginPath();
                const offset = 4;
                const perpX = -dy / distance * offset;
                const perpY = dx / distance * offset;
                
                ctx.moveTo(startX + perpX, startY + perpY);
                ctx.lineTo(endX + perpX, endY + perpY);
                ctx.stroke();
            }
            
            // 返回键的信息用于悬停检测
            return {
                startX, startY, endX, endY, 
                fromAtom, toAtom, bond,
                breaking, forming, highlight
            };
        }
        
        // 绘制电子流箭头
        function drawElectronFlow(fromAtom, toAtom, progress = 1) {
            const dx = toAtom.x - fromAtom.x;
            const dy = toAtom.y - fromAtom.y;
            const distance = Math.sqrt(dx * dx + dy * dy);
            const angle = Math.atan2(dy, dx);
            
            // 计算箭头位置
            const arrowLength = 20;
            const arrowX = fromAtom.x + dx * progress;
            const arrowY = fromAtom.y + dy * progress;
            
            // 绘制箭头线
            ctx.strokeStyle = "#3498db";
            ctx.lineWidth = 2;
            ctx.setLineDash([5, 3]);
            ctx.beginPath();
            ctx.moveTo(fromAtom.x, fromAtom.y);
            ctx.lineTo(arrowX, arrowY);
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.setLineDash([]);
            ctx.beginPath();
            ctx.moveTo(arrowX, arrowY);
            ctx.lineTo(
                arrowX - arrowLength * Math.cos(angle - Math.PI / 6),
                arrowY - arrowLength * Math.sin(angle - Math.PI / 6)
            );
            ctx.moveTo(arrowX, arrowY);
            ctx.lineTo(
                arrowX - arrowLength * Math.cos(angle + Math.PI / 6),
                arrowY - arrowLength * Math.sin(angle + Math.PI / 6)
            );
            ctx.stroke();
        }
        
        // 绘制质子转移路径
        function drawProtonTransfer(fromAtom, toAtom, progress = 1) {
            const dx = toAtom.x - fromAtom.x;
            const dy = toAtom.y - fromAtom.y;
            
            // 绘制路径线
            ctx.strokeStyle = "#f1c40f";
            ctx.lineWidth = 2;
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            ctx.moveTo(fromAtom.x, fromAtom.y);
            
            // 添加一点曲线效果
            const cp1x = fromAtom.x + dx * 0.3;
            const cp1y = fromAtom.y - 30;
            const cp2x = fromAtom.x + dx * 0.7;
            const cp2y = fromAtom.y - 30;
            
            ctx.bezierCurveTo(cp1x, cp1y, cp2x, cp2y, toAtom.x, toAtom.y);
            ctx.stroke();
            
            // 绘制移动中的质子
            const t = progress;
            // 贝塞尔曲线公式
            const protonX = Math.pow(1 - t, 3) * fromAtom.x + 
                          3 * Math.pow(1 - t, 2) * t * cp1x + 
                          3 * (1 - t) * Math.pow(t, 2) * cp2x + 
                          Math.pow(t, 3) * toAtom.x;
            
            const protonY = Math.pow(1 - t, 3) * fromAtom.y + 
                          3 * Math.pow(1 - t, 2) * t * cp1y + 
                          3 * (1 - t) * Math.pow(t, 2) * cp2y + 
                          Math.pow(t, 3) * toAtom.y;
            
            // 绘制质子
            ctx.setLineDash([]);
            ctx.beginPath();
            ctx.arc(protonX, protonY, 10, 0, Math.PI * 2);
            ctx.fillStyle = "#f1c40f";
            ctx.fill();
            ctx.strokeStyle = "#333";
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 绘制质子符号
            ctx.fillStyle = "#333";
            ctx.font = "bold 12px Arial";
            ctx.textAlign = "center";
            ctx.textBaseline = "middle";
            ctx.fillText("H⁺", protonX, protonY);
            
            return { x: protonX, y: protonY };
        }
        
        // 根据当前步骤计算分子位置和状态
        function calculateStepPositions(step, progress) {
            const positions = JSON.parse(JSON.stringify(molecules));
            
            // 步骤0: 初始状态
            if (step === 0) {
                // 乙酸位置
                positions.aceticAcid.atoms.forEach(atom => {
                    atom.x = molecules.aceticAcid.initialX + (atom.x - molecules.aceticAcid.initialX);
                    atom.y = molecules.aceticAcid.initialY + (atom.y - molecules.aceticAcid.initialY);
                });
                
                // 乙醇位置
                positions.ethanol.atoms.forEach(atom => {
                    atom.x = molecules.ethanol.initialX + (atom.x - molecules.ethanol.initialX);
                    atom.y = molecules.ethanol.initialY + (atom.y - molecules.ethanol.initialY);
                });
                
                // 质子位置
                positions.proton.atoms[0].x = molecules.proton.initialX;
                positions.proton.atoms[0].y = molecules.proton.initialY;
            }
            
            // 步骤1: 质子化 - 质子移向羰基氧
            else if (step === 1) {
                const proton = positions.proton.atoms[0];
                const carbonylOxygen = positions.aceticAcid.atoms[2]; // 羰基氧
                
                // 质子移动到羰基氧
                proton.x = molecules.proton.initialX + (carbonylOxygen.x - molecules.proton.initialX) * progress;
                proton.y = molecules.proton.initialY + (carbonylOxygen.y - molecules.proton.initialY) * progress;
                
                // 乙醇向乙酸移动
                positions.ethanol.atoms.forEach(atom => {
                    const targetX = atom.x - 50 * progress;
                    const targetY = atom.y + 50 * progress;
                    atom.x = molecules.ethanol.initialX + (targetX - molecules.ethanol.initialX) * progress;
                    atom.y = molecules.ethanol.initialY + (targetY - molecules.ethanol.initialY) * progress;
                });
            }
            
            // 步骤2: 亲核进攻 - 乙醇氧进攻羰基碳
            else if (step === 2) {
                const ethanolOxygen = positions.ethanol.atoms[2]; // 乙醇的氧
                const carbonylCarbon = positions.aceticAcid.atoms[1]; // 羰基碳
                
                // 质子已连接到羰基氧
                positions.proton.atoms[0].x = positions.aceticAcid.atoms[2].x;
                positions.proton.atoms[0].y = positions.aceticAcid.atoms[2].y;
                
                // 乙醇氧向羰基碳移动
                const targetX = carbonylCarbon.x;
                const targetY = carbonylCarbon.y;
                ethanolOxygen.x = 525 + (targetX - 525) * progress;
                ethanolOxygen.y = 225 + (targetY - 225) * progress;
                
                // 乙醇的其他原子跟随移动
                positions.ethanol.atoms.forEach(atom => {
                    if (atom.id !== 11) { // 不是乙醇氧
                        const dx = ethanolOxygen.x - 525;
                        const dy = ethanolOxygen.y - 225;
                        atom.x = molecules.ethanol.atoms.find(a => a.id === atom.id).x + dx;
                        atom.y = molecules.ethanol.atoms.find(a => a.id === atom.id).y + dy;
                    }
                });
            }
            
            // 步骤3: 质子转移 - 质子从醇氧转移到酸氧
            else if (step === 3) {
                // 乙醇氧已连接到羰基碳
                positions.ethanol.atoms[2].x = positions.aceticAcid.atoms[1].x;
                positions.ethanol.atoms[2].y = positions.aceticAcid.atoms[1].y;
                
                // 乙醇的其他原子调整位置
                const ethanolOxygen = positions.ethanol.atoms[2];
                positions.ethanol.atoms.forEach(atom => {
                    if (atom.id !== 11 && atom.id !== 17) { // 不是乙醇氧和连接的氢
                        const baseAtom = molecules.ethanol.atoms.find(a => a.id === atom.id);
                        const offsetX = ethanolOxygen.x - 525;
                        const offsetY = ethanolOxygen.y - 225;
                        atom.x = baseAtom.x + offsetX;
                        atom.y = baseAtom.y + offsetY;
                    }
                });
                
                // 质子从羰基氧转移到乙醇的氢上（形成水分子）
                const proton = positions.proton.atoms[0];
                const fromAtom = positions.aceticAcid.atoms[2]; // 羰基氧
                const toAtom = positions.ethanol.atoms[7]; // 乙醇的羟基氢
                
                // 使用贝塞尔曲线计算质子位置
                const cp1x = fromAtom.x + (toAtom.x - fromAtom.x) * 0.3;
                const cp1y = fromAtom.y - 30;
                const cp2x = fromAtom.x + (toAtom.x - fromAtom.x) * 0.7;
                const cp2y = fromAtom.y - 30;
                
                const t = progress;
                proton.x = Math.pow(1 - t, 3) * fromAtom.x + 
                          3 * Math.pow(1 - t, 2) * t * cp1x + 
                          3 * (1 - t) * Math.pow(t, 2) * cp2x + 
                          Math.pow(t, 3) * toAtom.x;
                
                proton.y = Math.pow(1 - t, 3) * fromAtom.y + 
                          3 * Math.pow(1 - t, 2) * t * cp1y + 
                          3 * (1 - t) * Math.pow(t, 2) * cp2y + 
                          Math.pow(t, 3) * toAtom.y;
            }
            
            // 步骤4: 消除水分子
            else if (step === 4) {
                // 质子与乙醇的羟基氢结合，开始形成水分子
                const proton = positions.proton.atoms[0];
                const ethanolHydrogen = positions.ethanol.atoms[7]; // 乙醇的羟基氢
                
                // 水分子开始形成并离开
                const waterX = 400 + 100 * progress;
                const waterY = 350 - 50 * progress;
                
                proton.x = waterX;
                proton.y = waterY;
                ethanolHydrogen.x = waterX;
                ethanolHydrogen.y = waterY;
                
                // 乙酸上的羟基也开始离开
                const aceticHydroxylO = positions.aceticAcid.atoms[3]; // 羟基氧
                const aceticHydroxylH = positions.aceticAcid.atoms[7]; // 羟基氢
                
                aceticHydroxylO.x = waterX;
                aceticHydroxylO.y = waterY;
                aceticHydroxylH.x = waterX;
                aceticHydroxylH.y = waterY;
            }
            
            // 步骤5: 去质子化
            else if (step === 5) {
                // 水分子完全形成
                const waterX = 500;
                const waterY = 300;
                
                positions.proton.atoms[0].x = waterX;
                positions.proton.atoms[0].y = waterY;
                
                // 酯分子形成，释放质子
                const esterProton = { x: 350 + 100 * progress, y: 200 - 50 * progress
<!--检测到代码截断，自动续写中...-->
};
                
                // 酯分子形成
                positions.aceticAcid.atoms.forEach(atom => {
                    if (atom.id !== 3 && atom.id !== 7) { // 不是已离开的羟基氧和氢
                        atom.x = 300 + (atom.id - 1) * 5;
                        atom.y = 200;
                    }
                });
                
                positions.ethanol.atoms.forEach(atom => {
                    if (atom.id !== 11 && atom.id !== 17 && atom.id !== 7) { // 不是氧、羟基氢和已离开的氢
                        atom.x = 340 + (atom.id - 9) * 5;
                        atom.y = 200;
                    }
                });
                
                // 酯键形成（乙酸碳和乙醇氧连接）
                positions.ethanol.atoms[2].x = 320; // 乙醇氧移动到酯键位置
                positions.ethanol.atoms[2].y = 200;
            }
            
            // 步骤6: 反应完成
            else if (step === 6) {
                // 水分子在右侧
                positions.proton.atoms[0].x = 600; // 水中的H
                positions.proton.atoms[0].y = 350;
                
                // 酯分子在左侧
                positions.aceticAcid.atoms.forEach(atom => {
                    if (atom.id !== 3 && atom.id !== 7) { // 不是水中的原子
                        atom.x = 250 + (atom.id - 1) * 15;
                        atom.y = 200;
                    }
                });
                
                positions.ethanol.atoms.forEach(atom => {
                    if (atom.id !== 11 && atom.id !== 17 && atom.id !== 7) { // 不是水中的原子
                        atom.x = 310 + (atom.id - 9) * 15;
                        atom.y = 200;
                    }
                });
                
                // 酯键位置
                positions.ethanol.atoms[2].x = 300; // 乙醇氧
                positions.ethanol.atoms[2].y = 200;
                
                // 水分子
                positions.aceticAcid.atoms[3].x = 600; // 来自乙酸的氧
                positions.aceticAcid.atoms[3].y = 350;
                positions.aceticAcid.atoms[7].x = 580; // 来自乙酸的氢
                positions.aceticAcid.atoms[7].y = 330;
                positions.ethanol.atoms[7].x = 620; // 来自乙醇的氢
                positions.ethanol.atoms[7].y = 330;
            }
            
            return positions;
        }
        
        // 获取指定ID的原子
        function getAtomById(positions, id) {
            for (const molecule of Object.values(positions)) {
                const atom = molecule.atoms.find(a => a.id === id);
                if (atom) return atom;
            }
            return null;
        }
        
        // 主绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 计算当前步骤的分子位置
            const positions = calculateStepPositions(animationState.currentStep, animationState.progress);
            
            // 收集所有绘制的原子和键用于悬停检测
            const drawnAtoms = [];
            const drawnBonds = [];
            
            // 绘制所有键
            for (const molecule of Object.values(positions)) {
                for (const bond of molecule.bonds) {
                    const fromAtom = getAtomById(positions, bond.from);
                    const toAtom = getAtomById(positions, bond.to);
                    
                    if (fromAtom && toAtom) {
                        // 确定键的状态
                        let breaking = false;
                        let forming = false;
                        let highlight = false;
                        
                        // 步骤4: 乙酸羟基键断裂
                        if (animationState.currentStep === 4 && 
                            ((bond.from === 2 && bond.to === 4) || (bond.from === 4 && bond.to === 2))) {
                            breaking = animationState.progress > 0.3;
                        }
                        
                        // 步骤2-3: 新键形成（乙醇氧和羰基碳）
                        if ((animationState.currentStep === 2 || animationState.currentStep === 3) && 
                            ((bond.from === 2 && bond.to === 11) || (bond.from === 11 && bond.to === 2))) {
                            forming = true;
                        }
                        
                        // 步骤5-6: 酯键形成
                        if (animationState.currentStep >= 5 && 
                            ((bond.from === 2 && bond.to === 11) || (bond.from === 11 && bond.to === 2))) {
                            forming = animationState.progress > 0.5;
                        }
                        
                        // 悬停高亮
                        if (animationState.hoveredBond && 
                            ((bond.from === animationState.hoveredBond.bond.from && 
                              bond.to === animationState.hoveredBond.bond.to) ||
                             (bond.from === animationState.hoveredBond.bond.to && 
                              bond.to === animationState.hoveredBond.bond.from))) {
                            highlight = true;
                        }
                        
                        const bondInfo = drawBond(bond, fromAtom, toAtom, highlight, forming, breaking);
                        drawnBonds.push(bondInfo);
                    }
                }
            }
            
            // 绘制步骤特定的效果
            if (animationState.currentStep === 1 && animationState.progress > 0) {
                // 步骤1: 质子转移箭头
                const proton = positions.proton.atoms[0];
                const carbonylOxygen = positions.aceticAcid.atoms[2];
                drawProtonTransfer(
                    {x: molecules.proton.initialX, y: molecules.proton.initialY},
                    carbonylOxygen,
                    animationState.progress
                );
            }
            
            if (animationState.currentStep === 2 && animationState.progress > 0) {
                // 步骤2: 电子流箭头（乙醇氧的孤对电子进攻羰基碳）
                const ethanolOxygen = positions.ethanol.atoms[2];
                const carbonylCarbon = positions.aceticAcid.atoms[1];
                drawElectronFlow(ethanolOxygen, carbonylCarbon, animationState.progress);
            }
            
            if (animationState.currentStep === 3 && animationState.progress > 0) {
                // 步骤3: 质子转移
                const fromAtom = positions.aceticAcid.atoms[2]; // 质子化的羰基氧
                const toAtom = positions.ethanol.atoms[7]; // 乙醇的羟基氢
                drawProtonTransfer(fromAtom, toAtom, animationState.progress);
            }
            
            // 绘制所有原子
            for (const molecule of Object.values(positions)) {
                for (const atom of molecule.atoms) {
                    // 检查是否悬停
                    const highlight = animationState.hoveredAtom && 
                                     animationState.hoveredAtom.id === atom.id;
                    
                    const atomInfo = drawAtom(atom, highlight);
                    drawnAtoms.push(atomInfo);
                }
            }
            
            // 绘制分子名称标签
            if (animationState.currentStep <= 1) {
                ctx.fillStyle = "#2c3e50";
                ctx.font = "bold 16px Arial";
                ctx.textAlign = "center";
                ctx.fillText("乙酸", 250, 320);
                ctx.fillText("乙醇", 500, 150);
                ctx.fillText("H⁺ (催化剂)", 600, 320);
            } else if (animationState.currentStep >= 6) {
                ctx.fillStyle = "#2c3e50";
                ctx.font = "bold 16px Arial";
                ctx.textAlign = "center";
                ctx.fillText("乙酸乙酯", 300, 250);
                ctx.fillText("水", 600, 400);
            }
            
            // 存储绘制的元素用于悬停检测
            canvas.drawnAtoms = drawnAtoms;
            canvas.drawnBonds = drawnBonds;
        }
        
        // 更新步骤信息显示
        function updateStepInfo() {
            const stepInfoElement = document.getElementById('stepInfo');
            const stepValueElement = document.getElementById('stepValue');
            
            if (animationState.currentStep === 0) {
                stepInfoElement.innerHTML = `
                    <h4>准备开始</h4>
                    <p>动画将展示乙酸和乙醇分子在酸催化下的酯化反应机理。请点击"播放"按钮开始。</p>
                `;
                stepValueElement.textContent = "步骤 0/6";
            } else {
                const info = stepInfo[animationState.currentStep - 1];
                stepInfoElement.innerHTML = `
                    <h4>${info.title}</h4>
                    <p>${info.description}</p>
                `;
                stepValueElement.textContent = `步骤 ${animationState.currentStep}/6`;
            }
            
            // 更新步骤滑块
            document.getElementById('stepSlider').value = animationState.currentStep;
        }
        
        // 动画循环
        let lastTime = 0;
        function animate(timestamp) {
            if (!lastTime) lastTime = timestamp;
            const deltaTime = timestamp - lastTime;
            lastTime = timestamp;
            
            if (animationState.isPlaying) {
                // 更新进度
                animationState.progress += deltaTime * 0.001 * animationState.speed;
                
                // 如果进度超过1，进入下一步
                if (animationState.progress >= 1) {
                    animationState.progress = 0;
                    if (animationState.currentStep < animationState.totalSteps) {
                        animationState.currentStep++;
                        updateStepInfo();
                    } else {
                        animationState.isPlaying = false;
                        document.getElementById('playBtn').textContent = "▶ 播放";
                    }
                }
                
                draw();
            }
            
            requestAnimationFrame(animate);
        }
        
        // 初始化事件监听器
        function initEventListeners() {
            // 播放按钮
            document.getElementById('playBtn').addEventListener('click', function() {
                if (animationState.currentStep >= animationState.totalSteps) {
                    animationState.currentStep = 0;
                    animationState.progress = 0;
                    updateStepInfo();
                }
                
                animationState.isPlaying = !animationState.isPlaying;
                this.textContent = animationState.isPlaying ? "⏸ 暂停" : "▶ 播放";
                document.getElementById('pauseBtn').textContent = "⏸ 暂停";
            });
            
            // 暂停按钮
            document.getElementById('pauseBtn').addEventListener('click', function() {
                animationState.isPlaying = false;
                document.getElementById('playBtn').textContent = "▶ 播放";
            });
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', function() {
                animationState.currentStep = 0;
                animationState.progress = 0;
                animationState.isPlaying = false;
                document.getElementById('playBtn').textContent = "▶ 播放";
                updateStepInfo();
                draw();
            });
            
            // 上一步按钮
            document.getElementById('prevStepBtn').addEventListener('click', function() {
                if (animationState.currentStep > 0) {
                    animationState.currentStep--;
                    animationState.progress = 0;
                    animationState.isPlaying = false;
                    document.getElementById('playBtn').textContent = "▶ 播放";
                    updateStepInfo();
                    draw();
                }
            });
            
            // 下一步按钮
            document.getElementById('nextStepBtn').addEventListener('click', function() {
                if (animationState.currentStep < animationState.totalSteps) {
                    animationState.currentStep++;
                    animationState.progress = 0;
                    animationState.isPlaying = false;
                    document.getElementById('playBtn').textContent = "▶ 播放";
                    updateStepInfo();
                    draw();
                }
            });
            
            // 速度滑块
            document.getElementById('speedSlider').addEventListener('input', function() {
                animationState.speed = parseFloat(this.value);
                document.getElementById('speedValue').textContent = this.value + "x";
            });
            
            // 步骤滑块
            document.getElementById('stepSlider').addEventListener('input', function() {
                const step = parseInt(this.value);
                if (step !== animationState.currentStep) {
                    animationState.currentStep = step;
                    animationState.progress = 0;
                    animationState.isPlaying = false;
                    document.getElementById('playBtn').textContent = "▶ 播放";
                    updateStepInfo();
                    draw();
                }
            });
            
            // 视图切换
            document.getElementById('microViewBtn').addEventListener('click', function() {
                if (!animationState.microView) {
                    animationState.microView = true;
                    this.classList.add('active');
                    document.getElementById('macroViewBtn').classList.remove('active');
                    // 这里可以添加切换视图的逻辑
                }
            });
            
            document.getElementById('macroViewBtn').addEventListener('click', function() {
                if (animationState.microView) {
                    animationState.microView = false;
                    this.classList.add('active');
                    document.getElementById('microViewBtn').classList.remove('active');
                    // 这里可以添加切换视图的逻辑
                }
            });
            
            // 鼠标悬停检测
            canvas.addEventListener('mousemove', function(event) {
                const rect = canvas.getBoundingClientRect();
                const x = event.clientX - rect.left;
                const y = event.clientY - rect.top;
                
                // 检查是否悬停在原子上
                let hoveredAtom = null;
                if (canvas.drawnAtoms) {
                    for (const atomInfo of canvas.drawnAtoms) {
                        const distance = Math.sqrt(
                            Math.pow(x - atomInfo.x, 2) + 
                            Math.pow(y - atomInfo.y, 2)
                        );
                        
                        if (distance <= atomInfo.radius) {
                            hoveredAtom = atomInfo.atom;
                            break;
                        }
                    }
                }
                
                // 检查是否悬停在键上
                let hoveredBond = null;
                if (canvas.drawnBonds && !hoveredAtom) {
                    for (const bondInfo of canvas.drawnBonds) {
                        // 计算点到线段的距离
                        const A = { x: bondInfo.startX, y: bondInfo.startY };
                        const B = { x: bondInfo.endX, y: bondInfo.endY };
                        const P = { x, y };
                        
                        const AB = { x: B.x - A.x, y: B.y - A.y };
                        const AP = { x: P.x - A.x, y: P.y - A.y };
                        const BP = { x: P.x - B.x, y: P.y - B.y };
                        
                        const dot = AP.x * AB.x + AP.y * AB.y;
                        const lengthSq = AB.x * AB.x + AB.y * AB.y;
                        
                        let distance;
                        if (dot <= 0) {
                            distance = Math.sqrt(AP.x * AP.x + AP.y * AP.y);
                        } else if (dot >= lengthSq) {
                            distance = Math.sqrt(BP.x * BP.x + BP.y * BP.y);
                        } else {
                            const cross = AB.x * AP.y - AB.y * AP.x;
                            distance = Math.abs(cross) / Math.sqrt(lengthSq);
                        }
                        
                        if (distance <= 8) { // 悬停阈值
                            hoveredBond = bondInfo;
                            break;
                        }
                    }
                }
                
                // 更新悬停状态
                if (hoveredAtom !== animationState.hoveredAtom || 
                    hoveredBond !== animationState.hoveredBond) {
                    animationState.hoveredAtom = hoveredAtom;
                    animationState.hoveredBond = hoveredBond;
                    draw();
                    
                    // 更新鼠标指针
                    if (hoveredAtom || hoveredBond) {
                        canvas.style.cursor = 'pointer';
                    } else {
                        canvas.style.cursor = 'default';
                    }
                }
            });
            
            // 鼠标点击显示详细信息
            canvas.addEventListener('click', function() {
                if (animationState.hoveredAtom) {
                    const atom = animationState.hoveredAtom;
                    let role = "";
                    
                    // 根据原子ID确定角色
                    if (atom.id === 2) role = "羰基碳，亲电中心";
                    else if (atom.id === 3) role = "羰基氧";
                    else if (atom.id === 4) role = "羟基氧";
                    else if (atom.id === 11) role = "醇羟基氧，亲核试剂";
                    else if (atom.id === 18) role = "质子 H⁺，催化剂";
                    else if (atom.element === "O") role = "氧原子";
                    else if (atom.element === "C") role = "碳原子";
                    else if (atom.element === "H") role = "氢原子";
                    
                    alert(`原子信息:\n元素: ${atom.element}\n角色: ${role}`);
                } else if (animationState.hoveredBond) {
                    const bond = animationState.hoveredBond.bond;
                    const type = bond.type === "double" ? "双键" : "单键";
                    let status = "正常";
                    
                    if (animationState.hoveredBond.breaking) status = "正在断裂";
                    if (animationState.hoveredBond.forming) status = "正在形成";
                    if (animationState.hoveredBond.highlight) status = "被选中";
                    
                    alert(`化学键信息:\n类型: ${type}\n状态: ${status}`);
                }
            });
        }
        
        // 初始化
        function init() {
            // 开始动画循环
            requestAnimationFrame(animate);
            
            // 初始化事件监听器
            initEventListeners();
            
            // 初始绘制
            draw();
            updateStepInfo();
            
            // 初始调整Canvas大小
            resizeCanvas();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

欢迎使用“酯化反应微观机理”交互式教学动画！本动画旨在通过直观、动态的可视化方式，帮助您深入理解有机化学中酯化反应的微观机理。无论您是高中生、大学生还是化学爱好者，本工具都将为您提供沉浸式的学习体验。

---

### 一、 功能说明

本动画完整模拟了乙酸与乙醇在酸催化下生成乙酸乙酯和水的全过程。它不仅仅展示反应方程式，更通过**分步动画**和**交互式探索**，揭示了原子层面的键断裂、形成与重组过程，特别是“酸脱羟基，醇脱氢”这一核心机理的电子转移细节。

动画采用**球棍模型**，严格遵循CPK原子配色方案（碳：深灰，氧：红，氢：浅灰/白），并引入亮黄色突出显示作为催化剂的质子（H⁺），确保科学准确性与视觉清晰度。

---

### 二、 主要功能与操作指南

#### 1. 动画控制区
*   **播放/暂停/重置**：控制动画的整体流程。点击“播放”开始连续反应，“暂停”可随时中断，“重置”使动画回到初始状态。
*   **上一步/下一步**：**核心学习功能**。强烈建议使用此功能进行分步学习。每点击一次“下一步”，动画将前进一个反应机理的关键步骤，并伴有详细的文字说明。这允许您反复观察和思考每一步的化学变化。
*   **进度滑块**：直接拖动滑块，可快速跳转到任意反应步骤。
*   **速度调节**：通过滑块调整动画播放速度（0.1x 至 3.0x），便于您慢速观察复杂步骤或快速浏览。

#### 2. 交互探索区
*   **鼠标悬停提示**：将鼠标移动到任意**原子**或**化学键**上，该元素会高亮显示。点击后，会弹出对话框，显示该原子（如“羰基碳，亲电中心”）或化学键（如“双键”、“正在断裂”）的详细信息。
*   **视图切换**：可在“微观机理视图”（默认）和“宏观方程式视图”间切换，帮助您在分子模型与化学符号之间建立联系。

#### 3. 信息显示区
*   **步骤说明面板**：实时显示当前步骤的标题和详细化学解释（例如：“步骤2: 亲核进攻 - 乙醇中的氧原子进攻带正电的羰基碳”）。这是理解每一步化学意义的关键文本。
*   **图例**：位于界面右下角，解释了所有颜色和符号的含义，方便随时查阅。

---

### 三、 设计特色

1.  **遵循认知规律**：动画设计遵循“整体→局部→细节”的认知路径。先展示分子全貌，再聚焦反应中心，最后用动态箭头展示电子和质子的流动。
2.  **过程可视化**：
    *   **电子流**：用**蓝色箭头**表示亲核试剂（醇羟基氧）的孤对电子进攻亲电中心（羰基碳）。
    *   **质子转移**：用**黄色虚线轨迹**清晰展示质子（H⁺）在整个反应中的催化循环路径。
    *   **键的变化**：**红色闪烁虚线**表示键的断裂，**绿色生长动画**表示新键的形成。
3.  **科学准确性**：准确展示了**亲核加成-消除机理**，动态显示了中间体的电荷变化（δ+， δ-），强调了质子催化对降低反应活化能的关键作用。

---

### 四、 教学要点与学习路径建议

为了达到最佳学习效果，建议按以下顺序使用本动画：

**第一阶段：概览**
1.  点击 **“播放”**，完整观看一遍动画，对酯化反应的动态全过程建立整体印象。

**第二阶段：分步深度学习（推荐）**
2.  点击 **“重置”**，然后使用 **“下一步”** 按钮，逐步推进反应。
3.  在每一步，请结合 **“步骤说明面板”** 的文字，仔细观察：
    *   **步骤1（质子化）**：观察质子（H⁺）如何与羰基氧结合，理解为何这会增强羰基碳的正电性。
    *   **步骤2（亲核进攻）**：重点关注蓝色电子流箭头，理解“亲核进攻”的微观含义。
    *   **步骤3（质子转移）**：跟踪黄色质子的转移路径，理解分子内重排。
    *   **步骤4（消除）**：观察水分子如何作为离去基团形成并离开，理解“酸脱羟基”。
    *   **步骤5（去质子化）**：观察催化剂的再生，理解催化循环。

**第三阶段：交互探索与巩固**
4.  在任意步骤**暂停**，使用鼠标**悬停并点击**不同的原子和键，了解它们在反应中的具体角色。
5.  尝试使用**进度滑块**在已理解的步骤间来回跳转，梳理各步骤之间的因果关系。
6.  思考并回答：如果没有质子（H⁺）催化，反应为何难以进行？酯化反应为何是可逆的？

---

### 五、 使用建议

*   **最佳环境**：在电脑或平板上使用，以获得最佳的交互和视觉体验。
*   **结合理论学习**：本动画是辅助工具，建议与教材、课堂讲解结合使用，用动画验证和深化对理论的理解。
*   **主动提问**：在学习过程中，主动向自己或同伴提问：“这一步发生了什么？”“为什么这个原子带部分正电荷？”，从而变被动观看为主动探究。
*   **教学应用**：教师可在课堂演示时使用，或将其作为学生课后自主探究的作业，引导学生撰写观察报告或机理分析。

我们希望这个精心设计的交互式动画，能像一位耐心的向导，带领您穿越微观分子的世界，亲手“触摸”化学反应的奥秘，让酯化反应从一个抽象的方程式，变为一幕生动、深刻、令人难忘的科学图景。

祝您探索愉快，学有所获！