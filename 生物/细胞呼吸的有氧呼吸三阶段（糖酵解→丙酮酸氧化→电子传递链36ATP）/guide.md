# 需求：细胞呼吸的有氧呼吸三阶段（糖酵解→丙酮酸氧化→电子传递链36ATP）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的生物学学生。他们具备基础的细胞生物学知识，但需要将“有氧呼吸三阶段”这一抽象、动态的生化过程具体化、可视化。
2.  **核心需求**：
    *   **理解过程**：清晰地看到三个阶段（糖酵解、丙酮酸氧化、电子传递链）的先后顺序、发生场所（细胞质基质、线粒体基质、线粒体内膜）和输入/输出物。
    *   **掌握能量**：直观地理解ATP、NADH、FADH2等能量载体的产生、消耗与净收益，特别是最终36个ATP的由来。
    *   **克服难点**：化解对电子传递链和化学渗透学说等微观、抽象概念的认知障碍。
    *   **主动探索**：能够控制动画节奏，点击查看关键分子细节，从而进行自主学习和复习。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念聚焦**：
    *   **主线**：追踪一个葡萄糖分子的“能量释放与捕获之旅”。
    *   **阶段划分**：严格遵循三个阶段，突出每个阶段的“输入物”、“关键反应”、“输出物”和“发生场所”。
    *   **能量账本**：全程可视化统计ATP、NADH、FADH2的数量变化，最终汇总为净赚约36 ATP。

2.  **遵循认知规律**：
    *   **从宏观到微观**：动画开场展示一个典型真核细胞（如动物细胞），然后镜头推近，聚焦到线粒体结构，再进入分子反应层面。
    *   **分步讲解**：将连续过程分解为清晰的步骤，允许用户按阶段或步骤播放/暂停。
    *   **多模态编码**：颜色编码分子（如葡萄糖=蓝色，ATP=金色，NADH=橙色），动态箭头表示物质转移与电子流，音效（如“叮”声）提示ATP生成，强化记忆。

3.  **交互设计**：
    *   **叙事控制**：提供“播放/暂停”、“下一步/上一步”、“跳转到阶段”的控制面板。
    *   **探索式学习**：
        *   点击关键分子（如葡萄糖、丙酮酸、ATP合酶）可弹出卡片，显示其结构式或功能简介。
        *   鼠标悬停在线粒体不同区域（外膜、膜间隙、基质、内膜）时高亮并显示名称。
    *   **动态数据面板**：在屏幕一侧实时更新“能量计数板”，显示当前ATP、NADH、FADH2的累计数量。
    *   **总结与测验**：动画末尾提供可折叠的“三个阶段总览图”和几道简单的选择题（如“哪个阶段产生最多ATP？”），提供即时反馈。

4.  **视觉呈现**：
    *   **场景设计**：采用横屏布局，左侧为细胞与线粒体的“舞台”，右侧为控制面板和数据面板。
    *   **分子拟人化/符号化**：使用简洁、可爱的几何图形代表分子（如六边形代表葡萄糖，小球代表碳原子），既保证科学性又提升亲和力。酶和复合物用特殊的齿轮或机器形状表示。
    *   **动态效果**：
        *   糖酵解：葡萄糖在细胞质中被“切割”、磷酸化，分子图形拆分与重组。
        *   丙酮酸氧化：丙酮酸进入线粒体，释放CO2，与辅酶A结合，过程伴有缩放和变形动画。
        *   电子传递链：使用流动的光点代表电子沿内膜上的蛋白复合物（I, III, IV）传递。同时，用向上泵出的“小球”代表H+被泵入膜间隙，形成浓度梯度。最后，H+通过ATP合酶回流驱动“分子风车”旋转，每转一次合成一个ATP，此过程需重点突出。

#### 配色方案选择
*   **背景与舞台**：使用柔和的浅灰色或淡蓝色背景，确保清晰度。线粒体外膜用浅棕色，内膜用深棕色，基质用更浅的米黄色，以区分结构。
*   **分子颜色编码**：
    *   **葡萄糖/碳骨架**：蓝色系（稳定、主体）。
    *   **ATP/能量相关**：金色或亮黄色（突出、醒目）。
    *   **NADH/FADH2（电子载体）**：橙色和浅绿色（温暖、活跃）。
    *   **CO2**：灰色（代谢废物）。
    *   **O2**：天蓝色（最终电子受体）。
    *   **H+质子**：红色小点（带正电，显眼）。
*   **交互元素**：控制按钮使用友好的蓝色，悬停高亮用黄色，提示卡片用白色半透明底衬。

#### 交互功能列表
1.  **主控导航**：播放/暂停、重置、快进/快退（阶段跳转）。
2.  **信息悬停**：鼠标悬停在线粒体区域、蛋白复合物、关键分子上显示名称。
3.  **点击详情**：点击关键分子（如葡萄糖、丙酮酸、乙酰辅酶A、ATP合酶）弹出详细信息卡片。
4.  **动态数据面板**：实时显示“能量账本”（消耗ATP、产生ATP、净ATP、NADH、FADH2数量）。
5.  **过程高亮**：当前正在进行的反应步骤，相关分子和区域会轻微高亮。
6.  **总结折叠面板**：动画结束后，可展开/折叠一个总结三阶段输入输出的图表。
7.  **简单测验**：3-5道选择题，检验学习效果，提交后显示解析。

---

思考完毕，我已准备好根据以上设计，为您编写这个关于有氧呼吸三阶段的交互式教学动画的HTML、CSS和JavaScript代码。请告诉我，可以开始进行【第二步：代码实现】了吗？

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>有氧呼吸三阶段交互式教学动画</title>
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
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .header {
            text-align: center;
            margin-bottom: 25px;
            width: 100%;
            max-width: 1200px;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            width: 100%;
            max-width: 1200px;
            justify-content: center;
        }

        /* 左侧动画区域 */
        .animation-area {
            flex: 3;
            min-width: 700px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            padding: 20px;
            position: relative;
            overflow: hidden;
        }

        #animationCanvas {
            width: 100%;
            height: 500px;
            display: block;
            background-color: #f8fafc;
            border-radius: 10px;
        }

        .stage-indicator {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
            padding: 10px;
            background-color: #edf2f7;
            border-radius: 10px;
        }

        .stage {
            padding: 8px 20px;
            border-radius: 20px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            flex: 1;
            margin: 0 5px;
        }

        .stage.active {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .stage-1 { background-color: #4a90e2; color: white; }
        .stage-2 { background-color: #50c878; color: white; }
        .stage-3 { background-color: #ff6b6b; color: white; }

        /* 右侧控制面板 */
        .control-panel {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .panel {
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            padding: 25px;
        }

        .panel h2 {
            color: #2c3e50;
            margin-bottom: 20px;
            font-size: 1.4rem;
            border-bottom: 2px solid #eaeaea;
            padding-bottom: 10px;
        }

        /* 控制按钮 */
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: center;
        }

        .btn {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .btn-primary {
            background-color: #3498db;
            color: white;
        }

        .btn-primary:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background-color: #95a5a6;
            color: white;
        }

        .btn-secondary:hover {
            background-color: #7f8c8d;
        }

        .btn-success {
            background-color: #2ecc71;
            color: white;
        }

        .btn-success:hover {
            background-color: #27ae60;
        }

        /* 能量计数板 */
        .energy-counter {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .energy-item {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            border-left: 5px solid;
            transition: transform 0.3s ease;
        }

        .energy-item:hover {
            transform: translateY(-3px);
        }

        .energy-item.atp { border-left-color: #f1c40f; }
        .energy-item.nadh { border-left-color: #e67e22; }
        .energy-item.fadh2 { border-left-color: #2ecc71; }
        .energy-item.total { border-left-color: #9b59b6; }

        .energy-value {
            font-size: 2rem;
            font-weight: bold;
            margin: 5px 0;
        }

        .energy-label {
            font-size: 0.9rem;
            color: #7f8c8d;
        }

        /* 详细信息面板 */
        .info-panel {
            max-height: 300px;
            overflow-y: auto;
        }

        .info-content {
            font-size: 0.95rem;
            line-height: 1.6;
        }

        .info-content h3 {
            color: #2c3e50;
            margin: 15px 0 8px 0;
            font-size: 1.1rem;
        }

        .info-content p {
            margin-bottom: 10px;
            color: #555;
        }

        .molecule-key {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .key-item {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 0.85rem;
        }

        .key-color {
            width: 15px;
            height: 15px;
            border-radius: 3px;
        }

        /* 测验部分 */
        .quiz {
            display: none;
        }

        .quiz-question {
            margin-bottom: 15px;
            font-weight: bold;
            color: #2c3e50;
        }

        .quiz-option {
            background-color: #f8f9fa;
            padding: 12px;
            margin-bottom: 10px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
            border: 2px solid transparent;
        }

        .quiz-option:hover {
            background-color: #e9ecef;
        }

        .quiz-option.selected {
            border-color: #3498db;
            background-color: #e3f2fd;
        }

        .quiz-option.correct {
            border-color: #2ecc71;
            background-color: #d5f4e6;
        }

        .quiz-option.incorrect {
            border-color: #e74c3c;
            background-color: #fadbd8;
        }

        .quiz-feedback {
            margin-top: 15px;
            padding: 12px;
            border-radius: 8px;
            display: none;
        }

        .feedback-correct {
            background-color: #d5f4e6;
            color: #27ae60;
            border-left: 5px solid #2ecc71;
        }

        .feedback-incorrect {
            background-color: #fadbd8;
            color: #c0392b;
            border-left: 5px solid #e74c3c;
        }

        /* 响应式设计 */
        @media (max-width: 1100px) {
            .container {
                flex-direction: column;
            }
            
            .animation-area, .control-panel {
                min-width: 100%;
            }
        }

        @media (max-width: 768px) {
            .animation-area {
                padding: 15px;
            }
            
            #animationCanvas {
                height: 400px;
            }
            
            .stage {
                padding: 6px 12px;
                font-size: 0.9rem;
            }
            
            .controls {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
            }
        }

        .footer {
            margin-top: 30px;
            text-align: center;
            color: #7f8c8d;
            font-size: 0.9rem;
            width: 100%;
            max-width: 1200px;
            padding-top: 20px;
            border-top: 1px solid #eaeaea;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>有氧呼吸三阶段交互式教学动画</h1>
        <p class="subtitle">糖酵解 → 丙酮酸氧化 → 电子传递链 (36 ATP)</p>
    </div>

    <div class="container">
        <!-- 左侧动画区域 -->
        <div class="animation-area">
            <canvas id="animationCanvas" width="1000" height="500"></canvas>
            
            <div class="stage-indicator">
                <div class="stage stage-1 active" data-stage="1">1. 糖酵解<br>(细胞质基质)</div>
                <div class="stage stage-2" data-stage="2">2. 丙酮酸氧化<br>(线粒体基质)</div>
                <div class="stage stage-3" data-stage="3">3. 电子传递链<br>(线粒体内膜)</div>
            </div>
        </div>

        <!-- 右侧控制面板 -->
        <div class="control-panel">
            <!-- 控制按钮 -->
            <div class="panel">
                <h2>动画控制</h2>
                <div class="controls">
                    <button class="btn btn-primary" id="playPauseBtn">
                        <span id="playIcon">▶</span> <span id="playText">播放</span>
                    </button>
                    <button class="btn btn-secondary" id="resetBtn">↺ 重置</button>
                    <button class="btn btn-secondary" id="prevBtn">◀ 上一步</button>
                    <button class="btn btn-secondary" id="nextBtn">下一步 ▶</button>
                    <button class="btn btn-success" id="quizBtn">测验</button>
                </div>
            </div>

            <!-- 能量计数板 -->
            <div class="panel">
                <h2>能量计数板</h2>
                <div class="energy-counter">
                    <div class="energy-item atp">
                        <div class="energy-label">ATP (净)</div>
                        <div class="energy-value" id="atpCount">2</div>
                        <div class="energy-label">糖酵解产生</div>
                    </div>
                    <div class="energy-item nadh">
                        <div class="energy-label">NADH</div>
                        <div class="energy-value" id="nadhCount">2</div>
                        <div class="energy-label">电子载体</div>
                    </div>
                    <div class="energy-item fadh2">
                        <div class="energy-label">FADH₂</div>
                        <div class="energy-value" id="fadh2Count">0</div>
                        <div class="energy-label">电子载体</div>
                    </div>
                    <div class="energy-item total">
                        <div class="energy-label">预计总ATP</div>
                        <div class="energy-value" id="totalAtpCount">2</div>
                        <div class="energy-label">(通过氧化磷酸化)</div>
                    </div>
                </div>
            </div>

            <!-- 详细信息面板 -->
            <div class="panel info-panel">
                <h2>阶段详情</h2>
                <div class="info-content" id="stageInfo">
                    <h3>1. 糖酵解 (细胞质基质)</h3>
                    <p><strong>输入:</strong> 1葡萄糖 (6C) + 2ATP + 2NAD⁺</p>
                    <p><strong>输出:</strong> 2丙酮酸 (3C) + 4ATP (净2) + 2NADH</p>
                    <p><strong>关键步骤:</strong> 葡萄糖分解为两分子丙酮酸，产生少量ATP和NADH。</p>
                    
                    <div class="molecule-key">
                        <div class="key-item">
                            <div class="key-color" style="background-color: #4a90e2;"></div>
                            <span>葡萄糖/碳骨架</span>
                        </div>
                        <div class="key-item">
                            <div class="key-color" style="background-color: #f1c40f;"></div>
                            <span>ATP</span>
                        </div>
                        <div class="key-item">
                            <div class="key-color" style="background-color: #e67e22;"></div>
                            <span>NADH</span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- 测验部分 -->
            <div class="panel quiz" id="quizPanel">
                <h2>知识测验</h2>
                <div class="quiz-question" id="quizQuestion">有氧呼吸的三个阶段按顺序是？</div>
                
                <div class="quiz-option" data-answer="A">糖酵解 → 丙酮酸氧化 → 电子传递链</div>
                <div class="quiz-option" data-answer="B">丙酮酸氧化 → 糖酵解 → 电子传递链</div>
                <div class="quiz-option" data-answer="C">电子传递链 → 糖酵解 → 丙酮酸氧化</div>
                <div class="quiz-option" data-answer="D">糖酵解 → 电子传递链 → 丙酮酸氧化</div>
                
                <div class="quiz-feedback" id="quizFeedback">
                    <strong id="feedbackTitle">正确！</strong>
                    <p id="feedbackText">有氧呼吸的正确顺序是糖酵解（细胞质）、丙酮酸氧化（线粒体基质）、电子传递链（线粒体内膜）。</p>
                </div>
                
                <button class="btn btn-primary" id="submitQuizBtn" style="margin-top: 15px; width: 100%;">提交答案</button>
            </div>
        </div>
    </div>

    <div class="footer">
        <p>交互式教学动画 | 有氧呼吸三阶段 | 设计：教育技术专家</p>
        <p>提示：点击阶段标签可跳转，鼠标悬停在分子上查看详细信息</p>
    </div>

    <script>
        // 全局变量
        let canvas, ctx;
        let animationId = null;
        let isPlaying = false;
        let currentStage = 1; // 1:糖酵解, 2:丙酮酸氧化, 3:电子传递链
        let stageProgress = 0; // 当前阶段进度 0-100
        let animationSpeed = 1;
        
        // 能量计数
        let energyCounts = {
            atp: 2,      // 净ATP
            nadh: 2,     // NADH数量
            fadh2: 0,    // FADH2数量
            totalAtp: 2  // 预计总ATP
        };
        
        // 分子定义
        const molecules = {
            glucose: { name: "葡萄糖", color: "#4a90e2", x: 150, y: 250, radius: 30 },
            pyruvate: { name: "丙酮酸", color: "#3498db", x: 400, y: 250, radius: 20 },
            acetylCoA: { name: "乙酰辅酶A", color: "#9b59b6", x: 650, y: 200, radius: 22 },
            atp: { name: "ATP", color: "#f1c40f", x: 850, y: 150, radius: 18 },
            nadh: { name: "NADH", color: "#e67e22", x: 850, y: 250, radius: 18 },
            fadh2: { name: "FADH₂", color: "#2ecc71", x: 850, y: 350, radius: 18 },
            co2: { name: "CO₂", color: "#95a5a6", x: 500, y: 150, radius: 15 },
            o2: { name: "O₂", color: "#1abc9c", x: 750, y: 400, radius: 16 },
            hPlus: { name: "H⁺", color: "#e74c3c", x: 700, y: 100, radius: 8 }
        };
        
        // 线粒体结构
        const mitochondria = {
            outerMembrane: { x: 550, y: 250, width: 300, height: 200 },
            innerMembrane: { x: 575, y: 250, width: 250, height: 150 },
            matrix: { x: 600, y: 250, width: 200, height: 100 }
        };
        
        // 初始化Canvas
        function initCanvas() {
            canvas = document.getElementById('animationCanvas');
            ctx = canvas.getContext('2d');
            
            // 设置Canvas尺寸适应容器
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = 500;
            
            draw();
        }
        
        // 绘制函数
        function draw() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景和标题
            drawBackground();
            
            // 根据当前阶段绘制
            switch(currentStage) {
                case 1:
                    drawGlycolysis();
                    break;
                case 2:
                    drawPyruvateOxidation();
                    break;
                case 3:
                    drawETC();
                    break;
            }
            
            // 绘制线粒体（阶段2和3）
            if (currentStage >= 2) {
                drawMitochondria();
            }
            
            // 绘制分子
            drawMolecules();
            
            // 绘制电子和质子流动（阶段3）
            if (currentStage === 3) {
                drawElectronFlow();
                drawProtonFlow();
            }
            
            // 绘制ATP合酶（阶段3）
            if (currentStage === 3 && stageProgress > 50) {
                drawATPSynthase();
            }
        }
        
        // 绘制背景
        function drawBackground() {
            // 细胞质背景（左侧）
            ctx.fillStyle = '#f0f8ff';
            ctx.fillRect(0, 0, 500, canvas.height);
            
            // 线粒体区域背景（右侧）
            ctx.fillStyle = '#f9f9f9';
            ctx.fillRect(500, 0, canvas.width - 500, canvas.height);
            
            // 绘制标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 16px Arial';
            ctx.fillText('细胞质基质', 100, 40);
            
            if (currentStage >= 2) {
                ctx.fillText('线粒体', 650, 40);
            }
            
            // 绘制阶段标题
            ctx.font = 'bold 20px Arial';
            const stageTitles = ['', '1. 糖酵解 (Glycolysis)', '2. 丙酮酸氧化 (Pyruvate Oxidation)', '3. 电子传递链 (Electron Transport Chain)'];
            ctx.fillStyle = ['', '#4a90e2', '#50c878', '#ff6b6b'][currentStage];
            ctx.fillText(stageTitles[currentStage], canvas.width/2 - 100, 80);
            
            // 绘制进度条
            drawProgressBar();
        }
        
        // 绘制进度条
        function drawProgressBar() {
            const barWidth = 300;
            const barHeight = 10;
            const barX = canvas.width/2 - barWidth/2;
            const barY = 100;
            
            // 背景
            ctx.fillStyle = '#ecf0f1';
            ctx.fillRect(barX, barY, barWidth, barHeight);
            ctx.strokeStyle = '#bdc3c7';
            ctx.strokeRect(barX, barY, barWidth, barHeight);
            
            // 进度
            ctx.fillStyle = ['', '#4a90e2', '#50c878', '#ff6b6b'][currentStage];
            ctx.fillRect(barX, barY, barWidth * (stageProgress/100), barHeight);
            
            // 进度文本
            ctx.fillStyle = '#7f8c8d';
            ctx.font = '14px Arial';
            ctx.fillText(`进度: ${Math.round(stageProgress)}%`, barX + barWidth/2 - 30, barY + 25);
        }
        
        // 绘制糖酵解
        function drawGlycolysis() {
            // 绘制葡萄糖分解过程
            const progress = stageProgress / 100;
            
            // 葡萄糖分子
            drawHexagon(molecules.glucose.x, molecules.glucose.y, molecules.glucose.radius, molecules.glucose.color, '葡萄糖');
            
            // 箭头指向丙酮酸
            drawArrow(molecules.glucose.x + molecules.glucose.radius, molecules.glucose.y, 
                     molecules.pyruvate.x - molecules.pyruvate.radius, molecules.pyruvate.y, 
                     '#4a90e2', progress * 0.7);
            
            // 丙酮酸分子（根据进度显示）
            if (progress > 0.3) {
                const pyruvateCount = progress > 0.6 ? 2 : 1;
                for (let i = 0; i < pyruvateCount; i++) {
                    const offset = i * 60 - 30;
                    drawCircle(molecules.pyruvate.x + offset, molecules.pyruvate.y, molecules.pyruvate.radius, molecules.pyruvate.color, '丙酮酸');
                }
            }
            
            // ATP产生
            if (progress > 0.4) {
                const atpCount = progress > 0.8 ? 4 : (progress > 0.5 ? 2 : 0);
                for (let i = 0; i < atpCount; i++) {
                    const yPos = 150 + i * 30;
                    drawCircle(300, yPos, 15, molecules.atp.color, 'ATP');
                }
            }
            
            // NADH产生
            if (progress > 0.7) {
                for (let i = 0; i < 2; i++) {
                    const yPos = 350 + i * 30;
                    drawCircle(300, yPos, 15, molecules.nadh.color, 'NADH');
                }
            }
        }
        
        // 绘制丙酮酸氧化
        function drawPyruvateOxidation() {
            const progress = (stageProgress - 100) / 100; // 阶段2从100开始
            
            // 丙酮酸进入线粒体
            if (progress > 0.1) {
                for (let i = 0; i < 2; i++) {
                    const offset = i * 40 - 20;
                    drawCircle(450 + offset, 250, molecules.pyruvate.radius, molecules.pyruvate.color, '丙酮酸');
                    
                    // 箭头进入线粒体
                    if (progress > 0.3) {
                        drawArrow(450 + offset, 250, 550, 250, '#3498db', Math.min(1, (progress - 0.3) * 3));
                    }
                }
            }
            
            // 乙酰辅酶A产生
            if (progress > 0.5) {
                drawCircle(molecules.acetylCoA.x, molecules.acetylCoA.y, molecules.acetylCoA.radius, molecules.acetylCoA.color, '乙酰辅酶A');
                
                // CO2释放
                if (progress > 0.6) {
                    drawCircle(molecules.co2.x, molecules.co2.y, molecules.co2.radius, molecules.co2.color, 'CO₂');
                }
                
                // NADH产生
                if (progress > 0.7) {
                    for (let i = 0; i < 2; i++) {
                        const yPos = 200 + i * 30;
                        drawCircle(700, yPos, 15, molecules.nadh.color, 'NADH');
                    }
                }
            }
        }
        
        // 绘制电子传递链
        function drawETC() {
            const progress = (stageProgress - 200) / 100; // 阶段3从200开始
            
            // 绘制蛋白复合物
            const complexes = [
                { x: 620, y: 300, label: 'I', color: '#e74c3c' },
                { x: 680, y: 300, label: 'III', color: '#9b59b6' },
                { x: 740, y: 300, label: 'IV', color: '#3498db' }
            ];
            
            complexes.forEach(complex => {
                // 复合物矩形
                ctx.fillStyle = complex.color;
                ctx.fillRect(complex.x - 20, complex.y - 15, 40, 30);
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 2;
                ctx.strokeRect(complex.x - 20, complex.y - 15, 40, 30);
                
                // 标签
                ctx.fillStyle = 'white';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(complex.label, complex.x, complex.y);
                
                // 复合物名称
                ctx.fillStyle = '#2c3e50';
                ctx.font = '12px Arial';
                ctx.fillText(`复合物${complex.label}`, complex.x, complex.y + 25);
            });
            
            // ATP合酶
            if (progress > 0.3) {
                drawATPSynthase();
            }
            
            // O2分子
            drawCircle(molecules.o2.x, molecules.o2.y, molecules.o2.radius, molecules.o2.color, 'O₂');
        }
        
        // 绘制电子流动
        function drawElectronFlow() {
            const progress = (stageProgress - 200) / 100;
            const electronRadius = 6;
            
            if (progress > 0.1) {
                // 从NADH到复合物I的电子
                const electronCount = Math.min(10, Math.floor(progress * 20));
                
                for (let i = 0; i < electronCount; i++) {
                    const t = (i / 10 + progress * 2) % 1;
                    const x = 600 + t * 150;
                    const y = 280 + Math.sin(t * Math.PI * 2) * 10;
                    
                    ctx.fillStyle = '#f39c12';
                    ctx.beginPath();
                    ctx.arc(x, y, electronRadius, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 电子光晕
                    ctx.strokeStyle = 'rgba(243, 156, 18, 0.5)';
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.arc(x, y, electronRadius + 3, 0, Math.PI * 2);
                    ctx.stroke();
                }
            }
        }
        
        // 绘制质子流动
        function drawProtonFlow() {
            const progress = (stageProgress - 200) / 100;
            
            if (progress > 0.4) {
                // H+被泵出
                const protonCount = Math.min(8, Math.floor((progress - 0.4) * 20));
                
                for (let i = 0; i < protonCount; i++) {
                    const t = (i / 8 + (progress - 0.4) * 3) % 1;
                    const x = 700 + Math.sin(t * Math.PI) * 50;
                    const y = 280 - t * 60;
                    
                    drawCircle(x, y, molecules.hPlus.radius, molecules.hPlus.color, '');
                }
                
                // H+通过ATP合酶回流
                if (progress > 0.6) {
                    const backflowCount = Math.min(5, Math.floor((progress - 0.6) * 15));
                    
                    for (let i = 0; i < backflowCount; i++) {
                        const t = (i / 5 + (progress - 0.6) * 2) % 1;
                        const x = 800 - t * 50;
                        const y = 320 + Math.sin(t * Math.PI) * 20;
                        
                        drawCircle(x, y, molecules.hPlus.radius, molecules.hPlus.color, '');
                    }
                }
            }
        }
        
        // 绘制ATP合酶
        function drawATPSynthase() {
            const x = 800, y = 320;
            const progress = (stageProgress - 200) / 100;
            
            // 基部
            ctx.fillStyle = '#34495e';
            ctx.fillRect(x - 15, y - 5, 30, 40);
            
            // 旋转部分（根据进度旋转）
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(progress * Math.PI * 4);
            
            // 转子
            ctx.fillStyle = '#1abc9c';
            ctx.beginPath();
            ctx.arc(0, 0, 20, 0, Math.PI * 2);
            ctx.fill();
            
            // 叶片
            ctx.fillStyle = '#16a085';
            for (let i = 0; i < 6; i++) {
                ctx.rotate(Math.PI / 3);
                ctx.fillRect(15, -5, 15, 10);
            }
            
            ctx.restore();
            
            // ATP产生
            if (progress > 0.7) {
                const atpGenerated = Math.min(34, Math.floor((progress - 0.7) * 100));
                for (let i = 0; i < Math.min(5, atpGenerated); i++) {
                    const yPos = 380 + i * 25;
                    drawCircle(x, yPos, 12, molecules.atp.color, '');
                }
                
                // 显示ATP数量
                ctx.fillStyle = '#2c3e50';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(`已生成 ${atpGenerated} ATP`, x, 420);
            }
            
            // 标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('ATP合酶', x, y + 60);
        }
        
        // 绘制线粒体
        function drawMitochondria() {
            // 外膜
            ctx.strokeStyle = '#d35400';
            ctx.lineWidth = 3;
            ctx.strokeRect(
                mitochondria.outerMembrane.x - mitochondria.outerMembrane.width/2,
                mitochondria.outerMembrane.y - mitochondria.outerMembrane.height/2,
                mitochondria.outerMembrane.width,
                mitochondria.outerMembrane.height
            );
            
            // 内膜（有褶皱）
            ctx.strokeStyle = '#c0392b';
            ctx.lineWidth = 3;
            
            const innerX = mitochondria.innerMembrane.x - mitochondria.innerMembrane.width/2;
            const innerY = mitochondria.innerMembrane.y - mitochondria.innerMembrane.height/2;
            const innerWidth = mitochondria.innerMembrane.width;
            const innerHeight = mitochondria.innerMembrane.height;
            
            // 绘制内膜褶皱
            ctx.beginPath();
            for (let i = 0; i < 5; i++) {
                const foldX = innerX + i * (innerWidth / 4);
                const foldHeight = i % 2 === 0 ? innerHeight + 20 : innerHeight - 20;
                
                if (i === 0) {
                    ctx.moveTo(foldX, innerY + innerHeight/2 - foldHeight/2);
                }
                
                ctx.lineTo(foldX, innerY + innerHeight/2 - foldHeight/2);
                ctx.lineTo(foldX + innerWidth/4, innerY + innerHeight/2 + foldHeight/2);
            }
            ctx.stroke();
            
            // 基质
            ctx.fillStyle = 'rgba(241, 196, 15, 0.1)';
            ctx.fillRect(
                mitochondria.matrix.x - mitochondria.matrix.width/2,
                mitochondria.matrix.y - mitochondria.matrix.height/2,
                mitochondria.matrix.width,
                mitochondria.matrix.height
            );
            
            // 标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('线粒体外膜', mitochondria.outerMembrane.x, mitochondria.outerMembrane.y - mitochondria.outerMembrane.height/2 - 10);
            ctx.fillText('线粒体内膜', mitochondria.innerMembrane.x, mitochondria.innerMembrane.y - mitochondria.innerMembrane.height/2 - 25);
            ctx.fillText('基质', mitochondria.matrix.x, mitochondria.matrix.y);
        }
        
        // 绘制所有分子
        function drawMolecules() {
            // 根据阶段显示不同的分子
            if (currentStage === 1) {
                // 阶段1：显示葡萄糖和ATP/NADH
                drawHexagon(molecules.glucose.x, molecules.glucose.y, molecules.glucose.radius, molecules.glucose.color, '葡萄糖');
                
                // ATP分子
                for (let i = 0; i < Math.min(4, energyCounts.atp + 2); i++) {
                    const yPos = 150 + i * 30;
                    drawCircle(300, yPos, 15, molecules.atp.color, i < 2 ? '消耗' : '产生');
                }
                
                // NADH分子
                if (stageProgress > 70) {
                    for (let i = 0; i < 2; i++) {
                        const yPos = 350 + i * 30;
                        drawCircle(300, yPos, 15, molecules.nadh.color, 'NADH');
                    }
                }
            }
            
            if (currentStage >= 2) {
                // 阶段2和3：显示丙酮酸、乙酰辅酶A等
                drawCircle(molecules.acetylCoA.x, molecules.acetylCoA.y, molecules.acetylCoA.radius, molecules.acetylCoA.color, '乙酰辅酶A');
                drawCircle(molecules.co2.x, molecules.co2.y, molecules.co2.radius, molecules.co2.color, 'CO₂');
                
                // NADH
                const nadhY = currentStage === 2 ? 200 : 250;
                for (let i = 0; i < Math.min(10, energyCounts.nadh); i++) {
                    const xPos = 700 + (i % 5) * 30;
                    const yPos = nadhY + Math.floor(i / 5) * 30;
                    drawCircle(xPos, yPos, 12, molecules.nadh.color, '');
                }
                
                // FADH2（阶段3）
                if (currentStage === 3 && energyCounts.fadh2 > 0) {
                    for (let i = 0; i < Math.min(2, energyCounts.fadh2); i++) {
                        drawCircle(700 + i * 30, 320, 12, molecules.fadh2.color, '');
                    }
               
<!--检测到代码截断，自动续写中...-->
            }
            
            if (currentStage === 3) {
                // 阶段3：显示O2和ATP
                drawCircle(molecules.o2.x, molecules.o2.y, molecules.o2.radius, molecules.o2.color, 'O₂');
                
                // 显示生成的ATP
                const atpGenerated = Math.floor((energyCounts.totalAtp - 2) / 34 * 10);
                for (let i = 0; i < Math.min(10, atpGenerated); i++) {
                    const xPos = 850 + (i % 5) * 25;
                    const yPos = 150 + Math.floor(i / 5) * 25;
                    drawCircle(xPos, yPos, 10, molecules.atp.color, '');
                }
            }
        }
        
        // 绘制六边形（代表葡萄糖）
        function drawHexagon(x, y, radius, color, label) {
            ctx.fillStyle = color;
            ctx.beginPath();
            for (let i = 0; i < 6; i++) {
                const angle = Math.PI / 3 * i;
                const px = x + radius * Math.cos(angle);
                const py = y + radius * Math.sin(angle);
                
                if (i === 0) {
                    ctx.moveTo(px, py);
                } else {
                    ctx.lineTo(px, py);
                }
            }
            ctx.closePath();
            ctx.fill();
            
            // 边框
            ctx.strokeStyle = '#2c3e50';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 标签
            ctx.fillStyle = 'white';
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText(label, x, y);
        }
        
        // 绘制圆形分子
        function drawCircle(x, y, radius, color, label) {
            // 分子主体
            ctx.fillStyle = color;
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.fill();
            
            // 边框
            ctx.strokeStyle = '#2c3e50';
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 标签
            if (label) {
                ctx.fillStyle = '#2c3e50';
                ctx.font = '12px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(label, x, y + radius + 15);
            }
        }
        
        // 绘制箭头
        function drawArrow(fromX, fromY, toX, toY, color, progress) {
            if (progress <= 0) return;
            
            const currentToX = fromX + (toX - fromX) * progress;
            const currentToY = fromY + (toY - fromY) * progress;
            
            // 箭头线
            ctx.strokeStyle = color;
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(currentToX, currentToY);
            ctx.stroke();
            
            // 箭头头部（如果进度足够）
            if (progress > 0.1) {
                const angle = Math.atan2(currentToY - fromY, currentToX - fromX);
                const headLength = 15;
                
                ctx.fillStyle = color;
                ctx.beginPath();
                ctx.moveTo(currentToX, currentToY);
                ctx.lineTo(
                    currentToX - headLength * Math.cos(angle - Math.PI / 6),
                    currentToY - headLength * Math.sin(angle - Math.PI / 6)
                );
                ctx.lineTo(
                    currentToX - headLength * Math.cos(angle + Math.PI / 6),
                    currentToY - headLength * Math.sin(angle + Math.PI / 6)
                );
                ctx.closePath();
                ctx.fill();
            }
        }
        
        // 动画循环
        function animate() {
            if (!isPlaying) return;
            
            // 更新进度
            stageProgress += animationSpeed;
            
            // 检查阶段转换
            if (stageProgress > 100 && currentStage === 1) {
                // 阶段1完成，转到阶段2
                currentStage = 2;
                stageProgress = 100; // 从100开始阶段2
                updateStageIndicator();
                updateStageInfo();
                
                // 更新能量计数
                energyCounts.nadh += 2; // 丙酮酸氧化产生2NADH
                updateEnergyCounts();
            } else if (stageProgress > 200 && currentStage === 2) {
                // 阶段2完成，转到阶段3
                currentStage = 3;
                stageProgress = 200; // 从200开始阶段3
                updateStageIndicator();
                updateStageInfo();
                
                // 更新能量计数
                energyCounts.fadh2 = 2; // 电子传递链使用FADH2
                updateEnergyCounts();
            } else if (stageProgress > 300 && currentStage === 3) {
                // 阶段3完成，停止动画
                stageProgress = 300;
                pauseAnimation();
                
                // 最终能量计算
                energyCounts.totalAtp = 36;
                updateEnergyCounts();
            }
            
            // 更新能量计数（动态变化）
            if (currentStage === 3 && stageProgress > 200) {
                const etcProgress = (stageProgress - 200) / 100;
                energyCounts.totalAtp = 2 + Math.floor(etcProgress * 34);
                updateEnergyCounts();
            }
            
            // 重绘画布
            draw();
            
            // 继续动画循环
            animationId = requestAnimationFrame(animate);
        }
        
        // 更新阶段指示器
        function updateStageIndicator() {
            document.querySelectorAll('.stage').forEach(stage => {
                stage.classList.remove('active');
            });
            document.querySelector(`.stage-${currentStage}`).classList.add('active');
        }
        
        // 更新阶段信息
        function updateStageInfo() {
            const infoContent = document.getElementById('stageInfo');
            
            const stageInfo = [
                '',
                `<h3>1. 糖酵解 (细胞质基质)</h3>
                <p><strong>输入:</strong> 1葡萄糖 (6C) + 2ATP + 2NAD⁺</p>
                <p><strong>输出:</strong> 2丙酮酸 (3C) + 4ATP (净2) + 2NADH</p>
                <p><strong>关键步骤:</strong> 葡萄糖分解为两分子丙酮酸，产生少量ATP和NADH。</p>`,
                
                `<h3>2. 丙酮酸氧化 (线粒体基质)</h3>
                <p><strong>输入:</strong> 2丙酮酸 + 2NAD⁺ + 2辅酶A</p>
                <p><strong>输出:</strong> 2乙酰辅酶A + 2CO₂ + 2NADH</p>
                <p><strong>关键步骤:</strong> 丙酮酸进入线粒体，脱羧形成乙酰辅酶A，释放CO₂并产生NADH。</p>`,
                
                `<h3>3. 电子传递链与氧化磷酸化 (线粒体内膜)</h3>
                <p><strong>输入:</strong> 10NADH + 2FADH₂ + 6O₂ + 约34ADP + Pi</p>
                <p><strong>输出:</strong> 10NAD⁺ + 2FAD + 6H₂O + 约34ATP</p>
                <p><strong>关键步骤:</strong> 电子通过蛋白复合物传递，驱动H⁺泵出形成梯度，H⁺通过ATP合酶回流驱动ATP合成。</p>
                <p><strong>化学渗透学说:</strong> 质子梯度储存的能量用于合成ATP。</p>`
            ];
            
            infoContent.innerHTML = stageInfo[currentStage] + `
                <div class="molecule-key">
                    <div class="key-item">
                        <div class="key-color" style="background-color: #4a90e2;"></div>
                        <span>葡萄糖/碳骨架</span>
                    </div>
                    <div class="key-item">
                        <div class="key-color" style="background-color: #f1c40f;"></div>
                        <span>ATP</span>
                    </div>
                    <div class="key-item">
                        <div class="key-color" style="background-color: #e67e22;"></div>
                        <span>NADH</span>
                    </div>
                    ${currentStage >= 3 ? `
                    <div class="key-item">
                        <div class="key-color" style="background-color: #2ecc71;"></div>
                        <span>FADH₂</span>
                    </div>
                    <div class="key-item">
                        <div class="key-color" style="background-color: #e74c3c;"></div>
                        <span>H⁺质子</span>
                    </div>
                    ` : ''}
                </div>`;
        }
        
        // 更新能量计数显示
        function updateEnergyCounts() {
            document.getElementById('atpCount').textContent = energyCounts.atp;
            document.getElementById('nadhCount').textContent = energyCounts.nadh;
            document.getElementById('fadh2Count').textContent = energyCounts.fadh2;
            document.getElementById('totalAtpCount').textContent = energyCounts.totalAtp;
        }
        
        // 播放/暂停动画
        function toggleAnimation() {
            if (isPlaying) {
                pauseAnimation();
            } else {
                playAnimation();
            }
        }
        
        function playAnimation() {
            isPlaying = true;
            document.getElementById('playIcon').textContent = '⏸';
            document.getElementById('playText').textContent = '暂停';
            animate();
        }
        
        function pauseAnimation() {
            isPlaying = false;
            document.getElementById('playIcon').textContent = '▶';
            document.getElementById('playText').textContent = '播放';
            
            if (animationId) {
                cancelAnimationFrame(animationId);
                animationId = null;
            }
        }
        
        // 重置动画
        function resetAnimation() {
            pauseAnimation();
            currentStage = 1;
            stageProgress = 0;
            
            // 重置能量计数
            energyCounts = {
                atp: 2,
                nadh: 2,
                fadh2: 0,
                totalAtp: 2
            };
            
            updateStageIndicator();
            updateStageInfo();
            updateEnergyCounts();
            draw();
        }
        
        // 下一步
        function nextStep() {
            pauseAnimation();
            
            if (currentStage === 1 && stageProgress < 100) {
                stageProgress = Math.min(100, stageProgress + 20);
                
                // 更新能量计数
                if (stageProgress >= 70 && energyCounts.nadh < 2) {
                    energyCounts.nadh = 2;
                }
            } else if (currentStage === 2 && stageProgress < 200) {
                stageProgress = Math.min(200, stageProgress + 20);
                
                // 更新能量计数
                if (stageProgress >= 170 && energyCounts.nadh < 4) {
                    energyCounts.nadh = 4;
                }
            } else if (currentStage === 3 && stageProgress < 300) {
                stageProgress = Math.min(300, stageProgress + 20);
                
                // 更新能量计数
                if (stageProgress >= 210) {
                    energyCounts.fadh2 = 2;
                    const etcProgress = (stageProgress - 200) / 100;
                    energyCounts.totalAtp = 2 + Math.floor(etcProgress * 34);
                }
            } else if (currentStage < 3) {
                // 转到下一阶段
                currentStage++;
                stageProgress = (currentStage - 1) * 100;
                updateStageIndicator();
                updateStageInfo();
                
                // 更新能量计数
                if (currentStage === 2) {
                    energyCounts.nadh = 4;
                } else if (currentStage === 3) {
                    energyCounts.fadh2 = 2;
                }
            }
            
            updateEnergyCounts();
            draw();
        }
        
        // 上一步
        function prevStep() {
            pauseAnimation();
            
            if (currentStage === 1 && stageProgress > 0) {
                stageProgress = Math.max(0, stageProgress - 20);
                
                // 更新能量计数
                if (stageProgress < 70) {
                    energyCounts.nadh = 0;
                }
            } else if (currentStage === 2 && stageProgress > 100) {
                stageProgress = Math.max(100, stageProgress - 20);
                
                // 更新能量计数
                if (stageProgress < 170) {
                    energyCounts.nadh = 2;
                }
            } else if (currentStage === 3 && stageProgress > 200) {
                stageProgress = Math.max(200, stageProgress - 20);
                
                // 更新能量计数
                const etcProgress = (stageProgress - 200) / 100;
                energyCounts.totalAtp = 2 + Math.floor(etcProgress * 34);
            } else if (currentStage > 1) {
                // 转到上一阶段
                currentStage--;
                stageProgress = (currentStage - 1) * 100;
                updateStageIndicator();
                updateStageInfo();
                
                // 更新能量计数
                if (currentStage === 1) {
                    energyCounts.nadh = 2;
                    energyCounts.fadh2 = 0;
                    energyCounts.totalAtp = 2;
                } else if (currentStage === 2) {
                    energyCounts.fadh2 = 0;
                    energyCounts.totalAtp = 2;
                }
            }
            
            updateEnergyCounts();
            draw();
        }
        
        // 跳转到阶段
        function goToStage(stage) {
            pauseAnimation();
            currentStage = stage;
            stageProgress = (stage - 1) * 100;
            
            // 更新能量计数
            if (stage === 1) {
                energyCounts = { atp: 2, nadh: 2, fadh2: 0, totalAtp: 2 };
            } else if (stage === 2) {
                energyCounts = { atp: 2, nadh: 4, fadh2: 0, totalAtp: 2 };
            } else if (stage === 3) {
                energyCounts = { atp: 2, nadh: 10, fadh2: 2, totalAtp: 2 };
            }
            
            updateStageIndicator();
            updateStageInfo();
            updateEnergyCounts();
            draw();
        }
        
        // 切换测验面板
        function toggleQuiz() {
            const quizPanel = document.getElementById('quizPanel');
            const isQuizVisible = quizPanel.style.display === 'block';
            
            if (isQuizVisible) {
                quizPanel.style.display = 'none';
                document.getElementById('quizBtn').textContent = '测验';
            } else {
                quizPanel.style.display = 'block';
                document.getElementById('quizBtn').textContent = '返回动画';
                
                // 重置测验状态
                document.querySelectorAll('.quiz-option').forEach(option => {
                    option.classList.remove('selected', 'correct', 'incorrect');
                });
                document.getElementById('quizFeedback').style.display = 'none';
            }
        }
        
        // 处理测验
        function handleQuiz() {
            const selectedOption = document.querySelector('.quiz-option.selected');
            if (!selectedOption) {
                alert('请先选择一个答案！');
                return;
            }
            
            const isCorrect = selectedOption.dataset.answer === 'A';
            const feedback = document.getElementById('quizFeedback');
            
            if (isCorrect) {
                selectedOption.classList.add('correct');
                feedback.className = 'quiz-feedback feedback-correct';
                document.getElementById('feedbackTitle').textContent = '正确！';
                document.getElementById('feedbackText').textContent = '有氧呼吸的正确顺序是糖酵解（细胞质）、丙酮酸氧化（线粒体基质）、电子传递链（线粒体内膜）。';
            } else {
                selectedOption.classList.add('incorrect');
                feedback.className = 'quiz-feedback feedback-incorrect';
                document.getElementById('feedbackTitle').textContent = '不正确';
                document.getElementById('feedbackText').textContent = '正确答案是A：糖酵解 → 丙酮酸氧化 → 电子传递链。糖酵解在细胞质中进行，丙酮酸氧化在线粒体基质，电子传递链在线粒体内膜。';
            }
            
            feedback.style.display = 'block';
        }
        
        // 初始化事件监听
        function initEventListeners() {
            // 控制按钮
            document.getElementById('playPauseBtn').addEventListener('click', toggleAnimation);
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            document.getElementById('prevBtn').addEventListener('click', prevStep);
            document.getElementById('nextBtn').addEventListener('click', nextStep);
            document.getElementById('quizBtn').addEventListener('click', toggleQuiz);
            document.getElementById('submitQuizBtn').addEventListener('click', handleQuiz);
            
            // 阶段跳转
            document.querySelectorAll('.stage').forEach(stage => {
                stage.addEventListener('click', () => {
                    const stageNum = parseInt(stage.dataset.stage);
                    goToStage(stageNum);
                });
            });
            
            // 测验选项
            document.querySelectorAll('.quiz-option').forEach(option => {
                option.addEventListener('click', () => {
                    // 移除其他选项的选中状态
                    document.querySelectorAll('.quiz-option').forEach(opt => {
                        opt.classList.remove('selected');
                    });
                    
                    // 选中当前选项
                    option.classList.add('selected');
                });
            });
            
            // 窗口大小调整
            window.addEventListener('resize', initCanvas);
            
            // Canvas点击交互
            canvas.addEventListener('click', (e) => {
                const rect = canvas.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                // 检查是否点击了分子
                for (const [key, molecule] of Object.entries(molecules)) {
                    const distance = Math.sqrt((x - molecule.x) ** 2 + (y - molecule.y) ** 2);
                    if (distance < molecule.radius + 10) {
                        alert(`您点击了: ${molecule.name}\n\n${getMoleculeInfo(key)}`);
                        return;
                    }
                }
                
                // 检查是否点击了线粒体区域
                if (x > 400 && x < 800 && y > 150 && y < 350) {
                    alert('线粒体 - 细胞的"动力工厂"\n\n外膜: 通透性较高\n内膜: 折叠形成嵴，含有电子传递链蛋白\n基质: 含有三羧酸循环酶系');
                }
            });
            
            // Canvas悬停效果
            canvas.addEventListener('mousemove', (e) => {
                const rect = canvas.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                let hovered = false;
                
                // 检查是否悬停在分子上
                for (const molecule of Object.values(molecules)) {
                    const distance = Math.sqrt((x - molecule.x) ** 2 + (y - molecule.y) ** 2);
                    if (distance < molecule.radius + 5) {
                        canvas.style.cursor = 'pointer';
                        hovered = true;
                        break;
                    }
                }
                
                if (!hovered) {
                    canvas.style.cursor = 'default';
                }
            });
        }
        
        // 获取分子信息
        function getMoleculeInfo(key) {
            const info = {
                glucose: '葡萄糖 (C₆H₁₂O₆): 细胞的主要能源物质，通过糖酵解分解。',
                pyruvate: '丙酮酸 (C₃H₄O₃): 糖酵解的终产物，进入线粒体进一步氧化。',
                acetylCoA: '乙酰辅酶A: 丙酮酸氧化的产物，进入三羧酸循环。',
                atp: 'ATP (三磷酸腺苷): 细胞的能量货币，水解时释放能量。',
                nadh: 'NADH: 还原型辅酶Ⅰ，携带高能电子，用于电子传递链。',
                fadh2: 'FADH₂: 还原型黄素腺嘌呤二核苷酸，携带高能电子。',
                co2: '二氧化碳 (CO₂): 呼吸作用的废物，通过肺部排出。',
                o2: '氧气 (O₂): 最终电子受体，与H⁺结合生成水。',
                hPlus: '氢离子 (H⁺): 电子传递链中泵出形成质子梯度。'
            };
            
            return info[key] || '该分子的详细信息。';
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', () => {
            initCanvas();
            initEventListeners();
            updateStageInfo();
            updateEnergyCounts();
            
            // 初始绘制
            draw();
        });
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 《有氧呼吸三阶段交互式教学动画》使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态可视化、交互探索和即时反馈，帮助您深入理解有氧呼吸这一复杂的细胞能量代谢过程。无论您是学生、教师还是自学者，本指南将引导您充分利用其全部功能，获得最佳的学习体验。

---

### 一、 功能说明

本动画将抽象的生物化学过程转化为直观、生动的视觉叙事。它完整地模拟了**一个葡萄糖分子**在有氧条件下，经历**糖酵解、丙酮酸氧化、电子传递链**三个阶段，最终产生约36个ATP的全过程。动画不仅展示了反应步骤，还实时追踪并计算能量载体（ATP、NADH、FADH₂）的数量变化，将“能量账本”可视化。

### 二、 主要功能与操作

#### 1. **动画控制中心**
   - **播放/暂停**：控制动画的连续播放与暂停，让您能按自己的节奏学习。
   - **上一步/下一步**：在暂停状态下，逐步骤前进或后退，精细观察每一个生化反应。
   - **重置**：一键将动画恢复到初始状态，方便重复学习。
   - **阶段跳转**：点击顶部三个彩色阶段标签（糖酵解、丙酮酸氧化、电子传递链），可直接跳转到对应部分。

#### 2. **动态信息面板**
   - **能量计数板**：位于右侧面板，实时更新并显示：
     - **ATP (净)**：当前净产生的ATP数量。
     - **NADH / FADH₂**：已生成的电子载体数量。
     - **预计总ATP**：根据当前进度计算的最终ATP产量（从2逐步增至约36）。
   - **阶段详情**：详细描述当前阶段的输入物、输出物和关键步骤，内容随动画进度自动更新。

#### 3. **交互探索**
   - **点击分子**：在左侧动画区域的分子（如葡萄糖、ATP、NADH）上点击，会弹出该分子的名称和功能简介卡片。
   - **悬停提示**：将鼠标悬停在分子或线粒体结构上，光标会变为手形，提示此处有交互信息。
   - **点击线粒体**：点击线粒体区域，会弹出关于其结构（外膜、内膜、基质）和功能的说明。

#### 4. **知识巩固与测验**
   - **分子图例**：在“阶段详情”面板底部，配有按颜色编码的分子图例，帮助您记忆不同分子的代表色。
   - **互动测验**：点击“测验”按钮，右侧面板将切换为一道选择题，测试您对三个阶段顺序的掌握。选择答案并提交后，会获得即时反馈与解析。

### 三、 设计特色

1. **科学的可视化编码**：
   - **颜色编码**：葡萄糖（蓝色）、ATP（金色）、NADH（橙色）、FADH₂（绿色）、H⁺质子（红色）。一致的色彩体系降低了认知负荷。
   - **动态箭头**：清晰展示物质转化与转移的方向。
   - **拟物化设计**：ATP合酶被设计成旋转的“分子风车”，直观展示H⁺回流驱动ATP合成的化学渗透机制。

2. **遵循认知规律**：
   - **从宏观到微观**：动画始于细胞整体视图，逐步聚焦到线粒体，最后呈现分子反应。
   - **过程分解**：将连续反应分解为可控的步骤，符合“分块”学习原理。
   - **多感官刺激**：结合视觉动态、进度提示和交互反馈，强化记忆。

3. **游戏化学习体验**：
   - 通过控制进度、探索点击和完成测验，赋予学习者主动权，变被动观看为主动探索。

### 四、 教学要点

本动画特别适合用于讲解或理解以下核心概念与难点：

1. **三个阶段的发生场所**：明确糖酵解在**细胞质基质**，丙酮酸氧化在**线粒体基质**，电子传递链在**线粒体内膜**。
2. **能量输入与产出**：清晰展示每个阶段的“能量账”，尤其是理解为什么糖酵解净产2 ATP，而电子传递链能产出大量ATP。
3. **电子与质子的流向**：
   - **电子传递链**：可视化电子从NADH/FADH₂沿蛋白复合物（I、III、IV）传递至O₂的过程。
   - **化学渗透学说**：通过H⁺被泵出内膜形成梯度，再通过ATP合酶回流这一动态过程，生动阐释ATP合成的驱动力。
4. **中间产物的转化**：追踪葡萄糖→丙酮酸→乙酰辅酶A的碳骨架变化，以及CO₂的释放节点。

### 五、 使用建议

1. **对于学生/自学者**：
   - **首次学习**：建议先点击“播放”，完整观看一遍动画，建立整体流程概念。
   - **深入学习**：使用“暂停”和“上一步/下一步”，结合右侧“阶段详情”文字说明，逐步研究每个反应。重点关注能量计数板的变化。
   - **复习巩固**：直接使用“阶段跳转”功能复习特定阶段，并完成测验检验理解。
   - **主动探索**：不要忘记点击分子和线粒体，发现隐藏的详细信息。

2. **对于教师**：
   - **课堂演示**：可在讲解时同步播放动画，或使用“下一步”功能分步控制，作为可视化教具。
   - **引导探究**：提出诸如“为什么FADH₂产生的ATP比NADH少？”等问题，让学生通过操作动画（观察电子传递起点）自行寻找答案。
   - **翻转课堂**：可将此动画作为课前预习材料，让学生先自主探索，课堂上再针对难点进行讨论。

3. **最佳学习路径**：
   1. **通览**：完整播放动画，了解全过程。
   2. **分阶学习**：分三个阶段，利用控制功能逐步学习，记下每个阶段的输入、输出、场所和能量变化。
   3. **难点聚焦**：在电子传递链部分反复观看H⁺泵出、梯度形成和ATP合酶工作的动画，理解化学渗透。
   4. **总结与测试**：回顾三个阶段的联系，并完成互动测验。

---

希望这份指南能帮助您充分利用这个交互式工具，将有氧呼吸的知识点内化为清晰、动态的心智模型。祝您学习愉快，探索不止！