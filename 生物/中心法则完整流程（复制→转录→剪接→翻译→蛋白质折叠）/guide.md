# 需求：中心法则完整流程（复制→转录→剪接→翻译→蛋白质折叠）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要是高中或大学低年级的生物学学生，他们已具备基础的细胞生物学知识，但需要直观、动态地理解中心法则这一抽象、复杂的分子生物学核心流程。
2.  **核心需求**：
    *   **流程可视化**：将“DNA复制 → 转录 → RNA剪接 → 翻译 → 蛋白质折叠”这一系列不可见的微观过程，转化为清晰、连贯的动画。
    *   **理解关键概念**：明确区分复制与转录、理解内含子/外显子与剪接的意义、认识密码子与tRNA的作用、了解蛋白质一级结构到三维构象的折叠过程。
    *   **掌握顺序与关系**：理解每一步的输入、输出、发生场所（细胞核/细胞质）以及各分子（DNA， mRNA， tRNA， 核糖体， 氨基酸， 蛋白质）之间的相互作用关系。
    *   **主动探索与巩固**：用户应能控制动画节奏，重复观看特定步骤，并通过交互问答或操作加深记忆。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念分层呈现**：
    *   **第一层（宏观流程）**：以一条贯穿始终的“生产线”或“河流”隐喻，展示从DNA到功能蛋白质的完整路径，建立整体观。
    *   **第二层（分步机制）**：将流程分解为五个核心步骤，每个步骤作为一个独立模块。每个模块聚焦于：
        *   **场所**：明确标注（如“细胞核”、“细胞质”）。
        *   **关键分子**：用标准化、易区分的图形表示（如DNA双螺旋、RNA单链、核糖体、氨基酸球等）。
        *   **关键过程**：如碱基互补配对、磷酸二酯键形成、肽键形成、空间构象变化等。
    *   **第三层（分子细节）**：在用户点击或悬停时，可弹出简要说明，展示更具体的生化名称（如RNA聚合酶、剪接体、肽键）或原理（如密码子-反密码子配对）。

2.  **遵循认知规律**：
    *   **从整体到局部**：先自动播放一遍完整动画，建立全局印象。
    *   **分步学习**：随后，用户可以按顺序或选择任意步骤进行深入学习。每个步骤都包含“简介-动画演示-要点总结”的小循环。
    *   **多模态编码**：结合**视觉动画**（分子运动）、**文字标签**（名称）、**颜色编码**（区分分子类型）、**音效/提示音**（关键事件如键的形成）和**简单交互**（点击、拖拽），强化记忆。

3.  **交互设计**：
    *   **主控面板**：提供“播放/暂停”、“上一步/下一步”、“重置”按钮，以及一个步骤选择器（如标签页或进度条）。
    *   **过程控制**：在关键步骤（如翻译），允许用户控制动画速度，或手动点击“添加一个氨基酸”来逐步推进。
    *   **探索式交互**：例如，在“剪接”步骤，用户可以拖拽“剪接体”来移除“内含子”片段；在“翻译”步骤，可以拖拽正确的tRNA到核糖体上。
    *   **知识检查点**：在每个步骤结束后，弹出1-2个简单的选择题或判断题（如“转录的模板是DNA的哪条链？”），即时反馈。

4.  **视觉呈现**：
    *   **风格**：采用简洁、扁平化或轻度拟物化的卡通风格，避免过于复杂的细节干扰主题。
    *   **动态设计**：运动平滑，关键变化（如新键形成、片段切除）伴有高亮或闪烁效果。使用“生长”动画（如RNA链的延伸、多肽链的延伸）和“变形”动画（如多肽链折叠成蛋白质）来直观表现过程。
    *   **布局**：采用从左（细胞核内）到右（细胞质中）的流向布局，清晰展示分子的空间转移。使用淡入淡出和路径线引导视线。

#### 配色方案选择
选择一套清晰、科学且友好的配色，用于区分不同类型的分子和结构：
*   **DNA**：经典的**深蓝色**（模板链）和**浅蓝色**（互补链），双螺旋结构清晰可辨。
*   **RNA (mRNA)**：**红色**或**橙色**，与DNA蓝色形成鲜明对比，易于区分。
*   **tRNA**：**绿色**，形状像三叶草，与mRNA的红色形成互补色对比，暗示其配对关系。
*   **核糖体**：**深灰色**或**紫色**，作为重要的细胞器，颜色稳重以突出其“工作台”的角色。
*   **氨基酸**：使用一组**柔和的、互不相同的颜色**（如浅黄、浅紫、浅青），但在折叠成蛋白质后，融合为统一的**金色**或**深红色**，表示功能蛋白的形成。
*   **背景与辅助元素**：使用**浅灰色**或**米白色**背景。细胞核区域可用**极浅的蓝色**底纹示意，细胞质区域用**极浅的黄色**底纹示意。
*   **高亮与强调色**：使用**亮黄色**或**荧光绿**来高亮显示正在发生反应的键、活性位点或用户交互焦点。

#### 交互功能列表
1.  **全局控制**：
    *   完整流程的“自动播放/暂停”。
    *   “重置”按钮，回到初始状态。
    *   可点击的“步骤进度条”或“标签页”，用于跳转到特定步骤。
2.  **步骤内控制**（每个步骤模块）：
    *   “播放本步动画”按钮。
    *   “上一步/下一步”按钮（在步骤间导航）。
    *   （可选）动画速度滑块。
3.  **探索性交互**：
    *   **转录/复制**：悬停显示酶的名称（如DNA聚合酶、RNA聚合酶）。
    *   **RNA剪接**：点击“执行剪接”按钮，或拖拽剪接体工具完成内含子的切除与外显子的连接。
    *   **翻译**：
        *   点击“开始翻译”，核糖体开始移动。
        *   手动模式：用户从池中拖拽正确的、携带氨基酸的tRNA到核糖体A位点上。
        *   点击每个氨基酸，显示其名称（如丙氨酸）。
    *   **蛋白质折叠**：点击“开始折叠”，观察线性多肽链如何动态盘曲折叠成三维结构。可设计一个简单的“折叠游戏”，让用户拖拽链段到大致正确的位置。
4.  **认知辅助交互**：
    *   **鼠标悬停提示**：所有主要分子和结构都有名称提示框。
    *   **开关式标签**：一个“显示/隐藏标签”按钮，控制所有名称标签的显示，避免画面杂乱。
    *   **知识检查点**：每个步骤后的弹出式小测验，提供即时对错反馈。
    *   **要点总结面板**：每个步骤动画旁有一个固定区域，用文字和图标列出该步骤的输入、输出、场所和关键点。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>中心法则完整流程 - 交互式教学动画</title>
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
            border-bottom: 2px solid #4a6fa5;
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
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }
        
        .animation-container {
            flex: 3;
            min-width: 300px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            position: relative;
            overflow: hidden;
        }
        
        .cell-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
        }
        
        .nucleus-area {
            position: absolute;
            top: 20px;
            left: 20px;
            width: 45%;
            height: calc(100% - 40px);
            border: 2px dashed rgba(52, 152, 219, 0.4);
            border-radius: 50%;
            background-color: rgba(52, 152, 219, 0.05);
            z-index: 1;
        }
        
        .nucleus-label {
            position: absolute;
            top: 10px;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(52, 152, 219, 0.2);
            padding: 3px 10px;
            border-radius: 4px;
            font-size: 0.9rem;
            color: #2980b9;
            font-weight: bold;
        }
        
        .cytoplasm-area {
            position: absolute;
            top: 20px;
            right: 20px;
            width: 45%;
            height: calc(100% - 40px);
            border: 2px dashed rgba(241, 196, 15, 0.4);
            border-radius: 10px;
            background-color: rgba(241, 196, 15, 0.05);
            z-index: 1;
        }
        
        .cytoplasm-label {
            position: absolute;
            top: 10px;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(241, 196, 15, 0.2);
            padding: 3px 10px;
            border-radius: 4px;
            font-size: 0.9rem;
            color: #f39c12;
            font-weight: bold;
        }
        
        #animationCanvas {
            width: 100%;
            height: 500px;
            display: block;
            position: relative;
            z-index: 2;
        }
        
        .controls-panel {
            flex: 1;
            min-width: 250px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .section-title {
            color: #2c3e50;
            font-size: 1.3rem;
            margin-bottom: 10px;
            padding-bottom: 8px;
            border-bottom: 1px solid #ecf0f1;
        }
        
        .step-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 10px;
        }
        
        .step-btn {
            flex: 1;
            min-width: 120px;
            padding: 10px 15px;
            background-color: #ecf0f1;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
            text-align: center;
        }
        
        .step-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.1);
        }
        
        .step-btn.active {
            background-color: #3498db;
            color: white;
        }
        
        .global-controls {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        
        .control-btn {
            flex: 1;
            padding: 12px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
        }
        
        .play-btn {
            background-color: #2ecc71;
            color: white;
        }
        
        .play-btn:hover {
            background-color: #27ae60;
        }
        
        .reset-btn {
            background-color: #e74c3c;
            color: white;
        }
        
        .reset-btn:hover {
            background-color: #c0392b;
        }
        
        .info-panel {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            margin-top: 10px;
        }
        
        .current-step-info h3 {
            color: #3498db;
            margin-bottom: 8px;
        }
        
        .current-step-info p {
            margin-bottom: 8px;
            font-size: 0.95rem;
        }
        
        .key-points {
            margin-top: 10px;
            padding-left: 20px;
        }
        
        .key-points li {
            margin-bottom: 5px;
            font-size: 0.9rem;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 6px;
            font-size: 0.85rem;
        }
        
        .legend-color {
            width: 16px;
            height: 16px;
            border-radius: 3px;
        }
        
        .quiz-panel {
            background-color: #e8f4fc;
            border-radius: 8px;
            padding: 15px;
            margin-top: 15px;
            display: none;
        }
        
        .quiz-question {
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .quiz-options {
            display: flex;
            flex-direction: column;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .quiz-option {
            padding: 8px 12px;
            background-color: white;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.2s;
        }
        
        .quiz-option:hover {
            background-color: #f0f8ff;
        }
        
        .quiz-option.selected {
            background-color: #d1ecf1;
            border-left: 4px solid #17a2b8;
        }
        
        .quiz-feedback {
            padding: 10px;
            border-radius: 4px;
            font-weight: 600;
            text-align: center;
            display: none;
        }
        
        .correct {
            background-color: #d4edda;
            color: #155724;
        }
        
        .incorrect {
            background-color: #f8d7da;
            color: #721c24;
        }
        
        .footer {
            text-align: center;
            margin-top: 20px;
            color: #7f8c8d;
            font-size: 0.9rem;
            padding-top: 15px;
            border-top: 1px solid #ecf0f1;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            #animationCanvas {
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>中心法则完整流程</h1>
        <p class="subtitle">复制 → 转录 → 剪接 → 翻译 → 蛋白质折叠</p>
    </header>
    
    <div class="container">
        <div class="main-content">
            <div class="animation-container">
                <div class="cell-background">
                    <div class="nucleus-area">
                        <div class="nucleus-label">细胞核</div>
                    </div>
                    <div class="cytoplasm-area">
                        <div class="cytoplasm-label">细胞质</div>
                    </div>
                </div>
                <canvas id="animationCanvas" width="800" height="500"></canvas>
            </div>
            
            <div class="controls-panel">
                <div class="step-controls-section">
                    <h2 class="section-title">步骤控制</h2>
                    <div class="step-controls">
                        <button class="step-btn active" data-step="0">完整流程</button>
                        <button class="step-btn" data-step="1">1. DNA复制</button>
                        <button class="step-btn" data-step="2">2. 转录</button>
                        <button class="step-btn" data-step="3">3. RNA剪接</button>
                        <button class="step-btn" data-step="4">4. 翻译</button>
                        <button class="step-btn" data-step="5">5. 蛋白质折叠</button>
                    </div>
                    
                    <div class="global-controls">
                        <button class="control-btn play-btn" id="playBtn">播放动画</button>
                        <button class="control-btn reset-btn" id="resetBtn">重置</button>
                    </div>
                </div>
                
                <div class="current-step-info">
                    <h2 class="section-title">当前步骤信息</h2>
                    <div id="stepInfo">
                        <h3>中心法则完整流程</h3>
                        <p>中心法则描述了遗传信息从DNA到RNA再到蛋白质的流动过程。这是分子生物学的核心原理。</p>
                        <p>点击左侧步骤按钮或点击"播放动画"观看完整流程。</p>
                        <ul class="key-points">
                            <li><strong>DNA复制</strong>：在细胞核内，DNA双链解开，每条链作为模板合成互补链</li>
                            <li><strong>转录</strong>：以DNA为模板合成mRNA的过程</li>
                            <li><strong>RNA剪接</strong>：去除mRNA中的内含子，连接外显子</li>
                            <li><strong>翻译</strong>：在细胞质中，核糖体读取mRNA序列，合成多肽链</li>
                            <li><strong>蛋白质折叠</strong>：多肽链折叠成具有特定三维结构的蛋白质</li>
                        </ul>
                    </div>
                </div>
                
                <div class="legend-section">
                    <h2 class="section-title">图例</h2>
                    <div class="legend">
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #2c3e50;"></div>
                            <span>DNA模板链</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #3498db;"></div>
                            <span>DNA互补链</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #e74c3c;"></div>
                            <span>mRNA</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #2ecc71;"></div>
                            <span>tRNA</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #9b59b6;"></div>
                            <span>核糖体</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #f1c40f;"></div>
                            <span>氨基酸/蛋白质</span>
                        </div>
                    </div>
                </div>
                
                <div class="quiz-panel" id="quizPanel">
                    <div class="quiz-question" id="quizQuestion"></div>
                    <div class="quiz-options" id="quizOptions"></div>
                    <button class="control-btn" id="submitQuiz" style="display: none;">提交答案</button>
                    <div class="quiz-feedback" id="quizFeedback"></div>
                </div>
            </div>
        </div>
        
        <div class="footer">
            <p>交互式教学动画 | 中心法则完整流程 | 设计用于生物学教育</p>
            <p>提示：点击步骤按钮选择特定过程，点击"播放动画"观看完整流程</p>
        </div>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 动画状态变量
        let currentStep = 0; // 0=完整流程, 1=复制, 2=转录, 3=剪接, 4=翻译, 5=折叠
        let isPlaying = false;
        let animationFrameId = null;
        let animationTime = 0;
        let stepProgress = [0, 0, 0, 0, 0, 0]; // 每个步骤的进度(0-1)
        
        // 分子对象定义
        const molecules = {
            dna: {
                x: 100, y: 150,
                length: 120,
                basePairs: 20,
                color1: '#2c3e50', // 模板链
                color2: '#3498db', // 互补链
                isReplicated: false,
                isTranscribed: false
            },
            mrna: {
                x: 100, y: 250,
                length: 0,
                targetLength: 100,
                color: '#e74c3c',
                exons: 3,
                introns: 2,
                isSpliced: false
            },
            ribosome: {
                x: 500, y: 300,
                radius: 20,
                color: '#9b59b6',
                isActive: false,
                progress: 0
            },
            protein: {
                x: 700, y: 300,
                length: 0,
                targetLength: 80,
                color: '#f1c40f',
                isFolded: false,
                foldProgress: 0
            },
            tRNAs: []
        };
        
        // 步骤信息数据
        const stepInfoData = [
            {
                title: "中心法则完整流程",
                description: "中心法则描述了遗传信息从DNA到RNA再到蛋白质的流动过程。这是分子生物学的核心原理。",
                details: "点击左侧步骤按钮或点击'播放动画'观看完整流程。",
                keyPoints: [
                    "<strong>DNA复制</strong>：在细胞核内，DNA双链解开，每条链作为模板合成互补链",
                    "<strong>转录</strong>：以DNA为模板合成mRNA的过程",
                    "<strong>RNA剪接</strong>：去除mRNA中的内含子，连接外显子",
                    "<strong>翻译</strong>：在细胞质中，核糖体读取mRNA序列，合成多肽链",
                    "<strong>蛋白质折叠</strong>：多肽链折叠成具有特定三维结构的蛋白质"
                ]
            },
            {
                title: "1. DNA复制",
                description: "DNA复制是细胞分裂前，DNA双链解开，以每条链为模板合成互补链的过程，产生两个相同的DNA分子。",
                details: "发生在细胞核内，需要DNA聚合酶等酶参与，遵循碱基互补配对原则（A-T, C-G）。",
                keyPoints: [
                    "<strong>场所</strong>：细胞核",
                    "<strong>模板</strong>：DNA双链",
                    "<strong>产物</strong>：两个相同的DNA分子",
                    "<strong>酶</strong>：DNA聚合酶、解旋酶等",
                    "<strong>意义</strong>：保证遗传信息准确传递给子细胞"
                ]
            },
            {
                title: "2. 转录",
                description: "转录是以DNA的一条链为模板，合成mRNA（信使RNA）的过程，将遗传信息从DNA传递到RNA。",
                details: "发生在细胞核内，需要RNA聚合酶参与，合成与DNA模板互补的RNA链。",
                keyPoints: [
                    "<strong>场所</strong>：细胞核",
                    "<strong>模板</strong>：DNA的一条链",
                    "<strong>产物</strong>：前体mRNA（pre-mRNA）",
                    "<strong>酶</strong>：RNA聚合酶",
                    "<strong>配对原则</strong>：A-U, T-A, C-G, G-C"
                ]
            },
            {
                title: "3. RNA剪接",
                description: "RNA剪接是去除前体mRNA中的内含子（非编码区），并将外显子（编码区）连接起来形成成熟mRNA的过程。",
                details: "发生在细胞核内，由剪接体执行，确保只有编码序列进入翻译过程。",
                keyPoints: [
                    "<strong>场所</strong>：细胞核",
                    "<strong>底物</strong>：前体mRNA（pre-mRNA）",
                    "<strong>产物</strong>：成熟mRNA",
                    "<strong>执行者</strong>：剪接体",
                    "<strong>意义</strong>：增加蛋白质多样性，移除非编码序列"
                ]
            },
            {
                title: "4. 翻译",
                description: "翻译是以mRNA为模板，在核糖体上合成多肽链的过程，将核酸序列信息转换为氨基酸序列。",
                details: "发生在细胞质中，需要tRNA携带特定氨基酸，按照密码子-反密码子配对原则进行。",
                keyPoints: [
                    "<strong>场所</strong>：细胞质（核糖体）",
                    "<strong>模板</strong>：成熟mRNA",
                    "<strong>产物</strong>：多肽链",
                    "<strong>关键分子</strong>：tRNA、氨基酸、核糖体",
                    "<strong>密码子</strong>：mRNA上每三个碱基决定一个氨基酸"
                ]
            },
            {
                title: "5. 蛋白质折叠",
                description: "蛋白质折叠是新合成的多肽链通过空间构象变化，形成具有特定三维结构和生物功能的蛋白质的过程。",
                details: "发生在细胞质中，可能自发进行或需要分子伴侣协助，结构决定功能。",
                keyPoints: [
                    "<strong>场所</strong>：细胞质",
                    "<strong>底物</strong>：多肽链（一级结构）",
                    "<strong>产物</strong>：功能蛋白质（三级/四级结构）",
                    "<strong>驱动力</strong>：氨基酸侧链相互作用",
                    "<strong>意义</strong>：蛋白质功能依赖于其三维结构"
                ]
            }
        ];
        
        // 测验问题数据
        const quizData = [
            {
                question: "DNA复制发生在细胞的哪个部位？",
                options: ["细胞核", "细胞质", "线粒体", "核糖体"],
                correct: 0,
                step: 1
            },
            {
                question: "转录的产物是什么？",
                options: ["DNA", "tRNA", "mRNA", "蛋白质"],
                correct: 2,
                step: 2
            },
            {
                question: "RNA剪接去除的是什么？",
                options: ["外显子", "内含子", "启动子", "终止子"],
                correct: 1,
                step: 3
            },
            {
                question: "翻译过程中，携带氨基酸的是哪种RNA？",
                options: ["mRNA", "rRNA", "tRNA", "snRNA"],
                correct: 2,
                step: 4
            },
            {
                question: "蛋白质折叠的主要驱动力是什么？",
                options: ["ATP供能", "酶催化", "氨基酸侧链相互作用", "核糖体作用"],
                correct: 2,
                step: 5
            }
        ];
        
        // 初始化
        function init() {
            // 设置Canvas尺寸
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);
            
            // 设置按钮事件监听
            document.querySelectorAll('.step-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const step = parseInt(this.getAttribute('data-step'));
                    selectStep(step);
                });
            });
            
            document.getElementById('playBtn').addEventListener('click', togglePlay);
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            
            // 初始化tRNA
            for (let i = 0; i < 3; i++) {
                molecules.tRNAs.push({
                    x: 450 + i * 40,
                    y: 400,
                    color: '#2ecc71',
                    aminoAcid: true,
                    attached: false
                });
            }
            
            // 绘制初始状态
            draw();
        }
        
        // 调整Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = 500;
            draw();
        }
        
        // 选择步骤
        function selectStep(step) {
            currentStep = step;
            isPlaying = false;
            document.getElementById('playBtn').textContent = "播放动画";
            
            // 更新按钮状态
            document.querySelectorAll('.step-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            document.querySelector(`.step-btn[data-step="${step}"]`).classList.add('active');
            
            // 更新信息面板
            updateStepInfo(step);
            
            // 重置动画进度
            animationTime = 0;
            
            // 如果是完整流程，重置所有步骤进度
            if (step === 0) {
                stepProgress = [0, 0, 0, 0, 0, 0];
            } else {
                // 否则只激活当前步骤
                stepProgress = [0, 0, 0, 0, 0, 0];
                stepProgress[step] = 0;
            }
            
            // 显示或隐藏测验
            showQuizForStep(step);
            
            // 停止之前的动画
            if (animationFrameId) {
                cancelAnimationFrame(animationFrameId);
                animationFrameId = null;
            }
            
            draw();
        }
        
        // 更新步骤信息
        function updateStepInfo(step) {
            const info = stepInfoData[step];
            const stepInfoDiv = document.getElementById('stepInfo');
            
            stepInfoDiv.innerHTML = `
                <h3>${info.title}</h3>
                <p>${info.description}</p>
                <p>${info.details}</p>
                <ul class="key-points">
                    ${info.keyPoints.map(point => `<li>${point}</li>`).join('')}
                </ul>
            `;
        }
        
        // 显示步骤对应的测验
        function showQuizForStep(step) {
            const quizPanel = document.getElementById('quizPanel');
            const quiz = quizData.find(q => q.step === step);
            
            if (quiz && step !== 0) {
                quizPanel.style.display = 'block';
                
                document.getElementById('quizQuestion').textContent = quiz.question;
                
                const optionsDiv = document.getElementById('quizOptions');
                optionsDiv.innerHTML = '';
                
                quiz.options.forEach((option, index) => {
                    const optionDiv = document.createElement('div');
                    optionDiv.className = 'quiz-option';
                    optionDiv.textContent = `${String.fromCharCode(65 + index)}. ${option}`;
                    optionDiv.dataset.index = index;
                    
                    optionDiv.addEventListener('click', function() {
                        // 移除之前的选择
                        document.querySelectorAll('.quiz-option').forEach(opt => {
                            opt.classList.remove('selected');
                        });
                        
                        // 标记当前选择
                        this.classList.add('selected');
                        
                        // 显示提交按钮
                        document.getElementById('submitQuiz').style.display = 'block';
                        
                        // 设置提交事件
                        document.getElementById('submitQuiz').onclick = function() {
                            const selectedIndex = parseInt(document.querySelector('.quiz-option.selected').dataset.index);
                            const feedbackDiv = document.getElementById('quizFeedback');
                            
                            if (selectedIndex === quiz.correct) {
                                feedbackDiv.textContent = "正确！答案准确。";
                                feedbackDiv.className = "quiz-feedback correct";
                            } else {
                                feedbackDiv.textContent = `不正确。正确答案是：${String.fromCharCode(65 + quiz.correct)}. ${quiz.options[quiz.correct]}`;
                                feedbackDiv.className = "quiz-feedback incorrect";
                            }
                            
                            feedbackDiv.style.display = 'block';
                            document.getElementById('submitQuiz').style.display = 'none';
                        };
                    });
                    
                    optionsDiv.appendChild(optionDiv);
                });
                
                // 重置反馈和提交按钮
                document.getElementById('quizFeedback').style.display = 'none';
                document.getElementById('submitQuiz').style.display = 'none';
            } else {
                quizPanel.style.display = 'none';
            }
        }
        
        // 播放/暂停动画
        function togglePlay() {
            isPlaying = !isPlaying;
            
            if (isPlaying) {
                document.getElementById('playBtn').textContent = "暂停动画";
                animate();
            } else {
                document.getElementById('playBtn').textContent = "播放动画";
                if (animationFrameId) {
                    cancelAnimationFrame(animationFrameId);
                    animationFrameId = null;
                }
            }
        }
        
        // 重置动画
        function resetAnimation() {
            isPlaying = false;
            document.getElementById('playBtn').textContent = "播放动画";
            animationTime = 0;
            stepProgress = [0, 0, 0, 0, 0, 0];
            
            // 重置分子状态
            molecules.dna.isReplicated = false;
            molecules.dna.isTranscribed = false;
            molecules.mrna.length = 0;
            molecules.mrna.isSpliced = false;
            molecules.ribosome.isActive = false;
            molecules.ribosome.progress = 0;
            molecules.protein.length = 0;
            molecules.protein.isFolded = false;
            molecules.protein.foldProgress = 0;
            
            molecules.tRNAs.forEach(tRNA => {
                tRNA.attached = false;
            });
            
            if (animationFrameId) {
                cancelAnimationFrame(animationFrameId);
                animationFrameId = null;
            }
            
            draw();
        }
        
        // 动画循环
        function animate() {
            if (!isPlaying) return;
            
            // 更新动画时间
            animationTime += 0.016; // 大约60fps
            
            // 根据当前步骤更新进度
            if (currentStep === 0) {
                // 完整流程：依次进行所有步骤
                const totalDuration = 25; // 完整流程总时间（秒）
                const stepDuration = totalDuration / 5;
                
                for (let i = 1; i <= 5; i++) {
                    const stepStart = (i - 1) * stepDuration;
                    const stepEnd = i * stepDuration;
                    
                    if (animationTime >= stepEnd) {
                        stepProgress[i] = 1;
                    } else if (animationTime >= stepStart) {
                        stepProgress[i] = (animationTime - stepStart) / stepDuration;
                    } else {
                        stepProgress[i] = 0;
                    }
                }
                
                // 如果动画完成，停止播放
                if (animationTime >= totalDuration) {
                    isPlaying = false;
                    document.getElementById('playBtn').textContent = "播放动画";
                    return;
                }
            } else {
                // 单个步骤：只更新当前步骤进度
                const stepDuration = 5; // 每个步骤持续时间（秒）
                stepProgress[currentStep] = Math.min(animationTime / stepDuration, 1);
                
                // 如果步骤完成，停止播放
                if (stepProgress[currentStep] >= 1) {
                    isPlaying = false;
                    document.getElementById('playBtn').textContent = "播放动画";
                }
            }
            
            // 更新分子状态
            updateMolecules();
            
            // 绘制
            draw();
            
            // 继续动画循环
            animationFrameId = requestAnimationFrame(animate);
        }
        
        // 更新分子状态
        function updateMolecules() {
            // 根据步骤进度更新分子
            if (currentStep === 0 || currentStep === 1) {
                // DNA复制
                if (stepProgress[1] > 0.5) {
                    molecules.dna.isReplicated = true;
                }
            }
            
            if (currentStep === 0 || currentStep === 2) {
                // 转录
                molecules.mrna.length = stepProgress[2] * molecules.mrna.targetLength;
                if (stepProgress[2] > 0.8) {
                    molecules.dna.isTranscribed = true;
                }
            }
            
            if (currentStep === 0 || currentStep === 3) {
                // RNA剪接
                if (stepProgress[3] > 0.6) {
                    molecules.mrna.isSpliced = true;
                }
            }
            
            if (currentStep === 0 || currentStep === 4) {
                // 翻译
                if (stepProgress[4] > 0.2) {
                    molecules.ribosome.isActive = true;
                    molecules.ribosome.progress = stepProgress[4];
                    
                    // 更新tRNA状态
                    if (stepProgress[4] > 0.3 && stepProgress[4] < 0.7) {
                        molecules.tRNAs[0].attached = true;
                        molecules.tRNAs[0].x = 500 + stepProgress[4] * 50;
                    }
                    
                    if (stepProgress[4] > 0.5 && stepProgress[4] < 0.9) {
                        molecules.tRNAs[1].attached = true;
                        molecules.tRNAs[1].x = 500 + stepProgress[4] * 50;
                    }
                    
                    // 蛋白质链生长
                    molecules.protein.length = stepProgress[4] * molecules.protein.targetLength;
                }
            }
            
            if (currentStep === 0 || currentStep === 5) {
                // 蛋白质折叠
                molecules.protein.foldProgress = stepProgress[5];
                if (stepProgress[5] > 0.7) {
                    molecules.protein.isFolded = true;
                }
            }
        }
        
        // 绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制DNA
            drawDNA();
            
            // 绘制mRNA
            drawMRNA();
            
            // 绘制核糖体
            drawRibosome();
            
            // 绘制tRNA
            drawTRNAs();
            
            // 绘制蛋白质
            drawProtein();
            
            // 绘制步骤标签
            drawStepLabels();
            
            // 绘制进度指示器（如果正在播放）
            if (isPlaying) {
                drawProgressIndicator();
            }
        }
        
        // 绘制DNA
        function drawDNA() {
            const dna = molecules.dna;
            const centerX = dna.x;
            const centerY = dna.y;
            const basePairSpacing = dna.length / dna.basePairs;
            
            // 绘制DNA骨架
            ctx.beginPath();
            ctx.moveTo(centerX, centerY - 10);
            ctx.lineTo(centerX + dna.length, centerY - 10);
            ctx.strokeStyle = dna.color1;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            ctx.beginPath();
            ctx.moveTo(centerX, centerY + 10);
            ctx.lineTo(centerX + dna.length, centerY + 10);
            ctx.strokeStyle = dna.color2;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制碱基对
            for (let i = 0; i < dna.basePairs; i++) {
                const x = centerX + i * basePairSpacing;
                
                // 如果是复制步骤且已复制，绘制两条DNA
                if (dna.isReplicated && (currentStep === 0 || currentStep === 1)) {
                    // 原始DNA
                    ctx.beginPath();
                    ctx.moveTo(x, centerY - 10);
                    ctx.lineTo(x, centerY + 10);
                    ctx.strokeStyle = '#7f8c8d';
                    ctx.lineWidth = 1;
                    ctx.stroke();
                    
                    // 新合成的DNA（向右偏移）
                    const offset = 30;
                    ctx.beginPath();
                    ctx.moveTo(x + offset, centerY - 10 - offset);
                    ctx.lineTo(x + offset, centerY + 10 - offset);
                    ctx.strokeStyle = dna.color2;
                    ctx.lineWidth = 1;
                    ctx.stroke();
                    
                    ctx.beginPath();
                    ctx.moveTo(x + offset, centerY - 10 + offset);
                    ctx.lineTo(x + offset, centerY + 10 + offset);
                    ctx.strokeStyle = dna.color1;
                    ctx.lineWidth = 1;
                    ctx.stroke();
                    
                    // 连接原始链和新链（表示解旋）
                    if (i % 3 === 0) {
                        ctx.beginPath();
                        ctx.moveTo(x, centerY - 10);
                        ctx.lineTo(x + offset, centerY - 10 - offset);
                        ctx.strokeStyle = 'rgba(52, 152, 219, 0.5)';
                        ctx.lineWidth = 1;
                        ctx.stroke();
                        
                        ctx.beginPath();
                        ctx.moveTo(x, centerY + 10);
                        ctx.lineTo(x + offset, centerY + 10 + offset);
                        ctx.strokeStyle = 'rgba(52, 152, 219, 0.5)';
                        ctx.lineWidth = 1;
                        ctx.stroke();
                    }
                } else {
                    // 正常DNA双螺旋
                    ctx.beginPath();
                    ctx.moveTo(x, centerY - 10);
                    ctx.lineTo(x, centerY + 10);
                    ctx.strokeStyle = i % 2 === 0 ? '#e74c3c' : '#2ecc71';
                    ctx.lineWidth = 1.5;
                    ctx.stroke();
                }
            }
            
            // 如果是转录步骤且正在转录，显示RNA聚合酶和正在合成的mRNA
            if (dna.isTranscribed && (currentStep === 0 || currentStep === 2)) {
                // RNA聚合酶
                const polymeraseX = dna.x + dna.length * 0.7;
                const polymeraseY = dna.y;
                
                ctx.fillStyle = '#9b59b6';
                ctx.beginPath();
                ctx.ellipse(polymeraseX, polymeraseY, 12, 8, 0, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = 'white';
                ctx.font = '10px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('酶', polymeraseX, polymeraseY + 3);
                
                // 正在合成的mRNA链
                const mrnaStartX = polymeraseX + 15;
                const mrnaStartY = polymeraseY - 5;
                
                ctx.beginPath();
                ctx.move
<!--检测到代码截断，自动续写中...-->
To(mrnaStartX, mrnaStartY);
                ctx.lineTo(mrnaStartX + 40, mrnaStartY);
                ctx.strokeStyle = '#e74c3c';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 绘制碱基
                for (let i = 0; i < 4; i++) {
                    const x = mrnaStartX + i * 10;
                    ctx.beginPath();
                    ctx.moveTo(x, mrnaStartY - 3);
                    ctx.lineTo(x, mrnaStartY + 3);
                    ctx.strokeStyle = i % 2 === 0 ? '#2ecc71' : '#f1c40f';
                    ctx.lineWidth = 1;
                    ctx.stroke();
                }
            }
            
            // DNA标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('DNA', centerX + dna.length/2, centerY - 30);
        }
        
        // 绘制mRNA
        function drawMRNA() {
            const mrna = molecules.mrna;
            const centerX = mrna.x;
            const centerY = mrna.y;
            
            // 只有转录开始后才绘制mRNA
            if (mrna.length > 0 || currentStep >= 2) {
                // 绘制mRNA骨架
                ctx.beginPath();
                ctx.moveTo(centerX, centerY);
                ctx.lineTo(centerX + mrna.length, centerY);
                ctx.strokeStyle = mrna.color;
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 如果是剪接前，显示内含子和外显子
                if (!mrna.isSpliced && (currentStep === 0 || currentStep === 2 || currentStep === 3)) {
                    const segmentLength = mrna.length / (mrna.exons + mrna.introns);
                    
                    for (let i = 0; i < mrna.exons + mrna.introns; i++) {
                        const x = centerX + i * segmentLength;
                        const isExon = i % 2 === 0; // 假设外显子和内含子交替
                        
                        // 绘制片段
                        ctx.beginPath();
                        ctx.moveTo(x, centerY);
                        ctx.lineTo(x + segmentLength, centerY);
                        ctx.strokeStyle = isExon ? '#e74c3c' : '#e74c3c';
                        ctx.lineWidth = isExon ? 4 : 2;
                        ctx.stroke();
                        
                        // 如果是内含子，添加删除标记
                        if (!isExon && currentStep === 3 && stepProgress[3] > 0.3) {
                            ctx.strokeStyle = '#e74c3c';
                            ctx.lineWidth = 1;
                            ctx.beginPath();
                            ctx.moveTo(x + segmentLength/2 - 5, centerY - 8);
                            ctx.lineTo(x + segmentLength/2 + 5, centerY + 8);
                            ctx.moveTo(x + segmentLength/2 + 5, centerY - 8);
                            ctx.lineTo(x + segmentLength/2 - 5, centerY + 8);
                            ctx.stroke();
                        }
                    }
                    
                    // 如果是剪接步骤，绘制剪接体
                    if (currentStep === 3 && stepProgress[3] > 0.2 && stepProgress[3] < 0.7) {
                        const spliceosomeX = centerX + mrna.length * 0.5;
                        const spliceosomeY = centerY - 25;
                        
                        ctx.fillStyle = 'rgba(155, 89, 182, 0.7)';
                        ctx.beginPath();
                        ctx.ellipse(spliceosomeX, spliceosomeY, 15, 10, 0, 0, Math.PI * 2);
                        ctx.fill();
                        
                        ctx.fillStyle = 'white';
                        ctx.font = '10px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('剪接体', spliceosomeX, spliceosomeY + 3);
                    }
                } else {
                    // 剪接后的成熟mRNA
                    ctx.beginPath();
                    ctx.moveTo(centerX, centerY);
                    ctx.lineTo(centerX + mrna.length, centerY);
                    ctx.strokeStyle = mrna.color;
                    ctx.lineWidth = 3;
                    ctx.stroke();
                    
                    // 绘制密码子标记
                    for (let i = 0; i < 5; i++) {
                        const x = centerX + i * (mrna.length / 5);
                        ctx.fillStyle = '#2c3e50';
                        ctx.font = '10px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText(['AUG', 'UAC', 'GCA', 'CGU', 'UAA'][i] || 'XXX', x + 10, centerY - 10);
                    }
                }
                
                // mRNA标签
                ctx.fillStyle = '#e74c3c';
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('mRNA', centerX + mrna.length/2, centerY - 30);
                
                // 如果是转录或之后步骤，绘制从DNA到mRNA的箭头
                if (currentStep >= 2) {
                    ctx.strokeStyle = 'rgba(231, 76, 60, 0.5)';
                    ctx.lineWidth = 1;
                    ctx.setLineDash([5, 5]);
                    ctx.beginPath();
                    ctx.moveTo(molecules.dna.x + molecules.dna.length * 0.7, molecules.dna.y);
                    ctx.lineTo(mrna.x, mrna.y);
                    ctx.stroke();
                    ctx.setLineDash([]);
                }
                
                // 如果是翻译步骤，绘制从mRNA到核糖体的箭头
                if (currentStep >= 4) {
                    ctx.strokeStyle = 'rgba(231, 76, 60, 0.5)';
                    ctx.lineWidth = 1;
                    ctx.setLineDash([5, 5]);
                    ctx.beginPath();
                    ctx.moveTo(mrna.x + mrna.length, mrna.y);
                    ctx.lineTo(molecules.ribosome.x - 20, molecules.ribosome.y);
                    ctx.stroke();
                    ctx.setLineDash([]);
                }
            }
        }
        
        // 绘制核糖体
        function drawRibosome() {
            const ribosome = molecules.ribosome;
            
            // 只有翻译开始后才绘制活跃的核糖体
            if (ribosome.isActive || currentStep >= 4) {
                // 绘制核糖体主体
                ctx.fillStyle = ribosome.color;
                ctx.beginPath();
                ctx.ellipse(ribosome.x, ribosome.y, ribosome.radius, ribosome.radius * 0.7, 0, 0, Math.PI * 2);
                ctx.fill();
                
                // 绘制核糖体亚基
                ctx.fillStyle = '#8e44ad';
                ctx.beginPath();
                ctx.ellipse(ribosome.x - 8, ribosome.y - 5, 8, 5, 0, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = '#8e44ad';
                ctx.beginPath();
                ctx.ellipse(ribosome.x + 8, ribosome.y + 5, 8, 5, 0, 0, Math.PI * 2);
                ctx.fill();
                
                // 绘制mRNA通道
                ctx.strokeStyle = '#e74c3c';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(ribosome.x - 25, ribosome.y);
                ctx.lineTo(ribosome.x + 25, ribosome.y);
                ctx.stroke();
                
                // 如果是翻译中，显示移动的核糖体
                if (ribosome.isActive && stepProgress[4] > 0.2) {
                    ribosome.x = 500 + ribosome.progress * 150;
                }
                
                // 核糖体标签
                ctx.fillStyle = ribosome.color;
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('核糖体', ribosome.x, ribosome.y - 35);
            }
        }
        
        // 绘制tRNA
        function drawTRNAs() {
            molecules.tRNAs.forEach((tRNA, index) => {
                // 只有翻译开始后才绘制tRNA
                if (currentStep >= 4) {
                    const centerX = tRNA.x;
                    const centerY = tRNA.y;
                    
                    // 绘制tRNA三叶草形状
                    ctx.fillStyle = tRNA.color;
                    
                    // 主体
                    ctx.beginPath();
                    ctx.ellipse(centerX, centerY, 12, 8, 0, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 反密码子环
                    ctx.beginPath();
                    ctx.ellipse(centerX, centerY + 15, 6, 4, 0, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 连接臂
                    ctx.beginPath();
                    ctx.moveTo(centerX, centerY + 8);
                    ctx.lineTo(centerX, centerY + 11);
                    ctx.strokeStyle = tRNA.color;
                    ctx.lineWidth = 3;
                    ctx.stroke();
                    
                    // 氨基酸（如果携带）
                    if (tRNA.aminoAcid) {
                        ctx.fillStyle = '#f1c40f';
                        ctx.beginPath();
                        ctx.ellipse(centerX, centerY - 12, 6, 6, 0, 0, Math.PI * 2);
                        ctx.fill();
                        
                        // 氨基酸标签
                        ctx.fillStyle = '#2c3e50';
                        ctx.font = '9px Arial';
                        ctx.textAlign = 'center';
                        const aminoAcids = ['丙氨酸', '缬氨酸', '亮氨酸'];
                        ctx.fillText(aminoAcids[index] || '氨基酸', centerX, centerY - 15);
                    }
                    
                    // 如果是附着状态，绘制到核糖体的连接
                    if (tRNA.attached) {
                        ctx.strokeStyle = 'rgba(46, 204, 113, 0.5)';
                        ctx.lineWidth = 1;
                        ctx.setLineDash([3, 3]);
                        ctx.beginPath();
                        ctx.moveTo(centerX, centerY);
                        ctx.lineTo(molecules.ribosome.x, molecules.ribosome.y);
                        ctx.stroke();
                        ctx.setLineDash([]);
                    }
                    
                    // tRNA标签（仅第一个）
                    if (index === 0) {
                        ctx.fillStyle = tRNA.color;
                        ctx.font = 'bold 14px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('tRNA', 450, 370);
                    }
                }
            });
        }
        
        // 绘制蛋白质
        function drawProtein() {
            const protein = molecules.protein;
            
            // 只有翻译开始后才绘制蛋白质
            if (protein.length > 0 || currentStep >= 4) {
                const centerX = protein.x;
                const centerY = protein.y;
                
                if (!protein.isFolded || currentStep < 5) {
                    // 线性多肽链
                    ctx.beginPath();
                    ctx.moveTo(centerX - protein.length/2, centerY);
                    ctx.lineTo(centerX + protein.length/2, centerY);
                    ctx.strokeStyle = protein.color;
                    ctx.lineWidth = 4;
                    ctx.stroke();
                    
                    // 氨基酸残基标记
                    for (let i = 0; i < 5; i++) {
                        const x = centerX - protein.length/2 + i * (protein.length / 4);
                        ctx.fillStyle = '#2c3e50';
                        ctx.font = '10px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('●', x, centerY - 10);
                    }
                    
                    // 从核糖体到蛋白质的箭头
                    if (currentStep >= 4) {
                        ctx.strokeStyle = 'rgba(241, 196, 15, 0.5)';
                        ctx.lineWidth = 1;
                        ctx.setLineDash([5, 5]);
                        ctx.beginPath();
                        ctx.moveTo(molecules.ribosome.x + 30, molecules.ribosome.y);
                        ctx.lineTo(centerX - protein.length/2, centerY);
                        ctx.stroke();
                        ctx.setLineDash([]);
                    }
                } else {
                    // 折叠后的蛋白质三维结构
                    const foldProgress = protein.foldProgress;
                    
                    // 绘制蛋白质核心
                    ctx.fillStyle = protein.color;
                    ctx.beginPath();
                    ctx.ellipse(centerX, centerY, 25 * foldProgress, 20 * foldProgress, 0, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 绘制α螺旋和β折叠的示意
                    ctx.strokeStyle = '#d35400';
                    ctx.lineWidth = 3;
                    
                    // α螺旋（螺旋线）
                    ctx.beginPath();
                    for (let i = 0; i < 10; i++) {
                        const angle = i * 0.5;
                        const radius = 15 * foldProgress;
                        const x = centerX + Math.cos(angle) * radius;
                        const y = centerY + Math.sin(angle) * radius;
                        
                        if (i === 0) {
                            ctx.moveTo(x, y);
                        } else {
                            ctx.lineTo(x, y);
                        }
                    }
                    ctx.stroke();
                    
                    // β折叠（锯齿线）
                    ctx.beginPath();
                    ctx.moveTo(centerX - 20 * foldProgress, centerY + 15 * foldProgress);
                    ctx.lineTo(centerX - 10 * foldProgress, centerY + 5 * foldProgress);
                    ctx.lineTo(centerX, centerY + 15 * foldProgress);
                    ctx.lineTo(centerX + 10 * foldProgress, centerY + 5 * foldProgress);
                    ctx.lineTo(centerX + 20 * foldProgress, centerY + 15 * foldProgress);
                    ctx.stroke();
                }
                
                // 蛋白质标签
                ctx.fillStyle = protein.color;
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                const label = protein.isFolded ? '蛋白质' : '多肽链';
                ctx.fillText(label, centerX, centerY - 50);
            }
        }
        
        // 绘制步骤标签
        function drawStepLabels() {
            const steps = [
                {name: "DNA复制", x: 150, y: 100},
                {name: "转录", x: 150, y: 220},
                {name: "RNA剪接", x: 150, y: 280},
                {name: "翻译", x: 550, y: 250},
                {name: "蛋白质折叠", x: 700, y: 220}
            ];
            
            // 绘制连接箭头
            ctx.strokeStyle = '#3498db';
            ctx.lineWidth = 2;
            ctx.setLineDash([10, 5]);
            ctx.beginPath();
            ctx.moveTo(220, 110);
            ctx.lineTo(220, 200);
            ctx.lineTo(500, 200);
            ctx.lineTo(500, 270);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制箭头头
            const drawArrow = (x, y, angle) => {
                ctx.save();
                ctx.translate(x, y);
                ctx.rotate(angle);
                
                ctx.fillStyle = '#3498db';
                ctx.beginPath();
                ctx.moveTo(0, 0);
                ctx.lineTo(-10, -5);
                ctx.lineTo(-10, 5);
                ctx.closePath();
                ctx.fill();
                
                ctx.restore();
            };
            
            drawArrow(220, 200, Math.PI/2);
            drawArrow(500, 200, 0);
            drawArrow(500, 270, Math.PI/2);
            
            // 高亮当前步骤
            steps.forEach((step, index) => {
                const stepNum = index + 1;
                const isCurrentStep = (currentStep === 0 && stepProgress[stepNum] > 0) || currentStep === stepNum;
                
                ctx.fillStyle = isCurrentStep ? '#e74c3c' : '#7f8c8d';
                ctx.font = isCurrentStep ? 'bold 16px Arial' : '14px Arial';
                ctx.textAlign = 'left';
                ctx.fillText(`${stepNum}. ${step.name}`, step.x, step.y);
                
                // 如果是当前步骤且正在播放，添加脉冲效果
                if (isCurrentStep && isPlaying) {
                    const pulseSize = 5 + Math.sin(Date.now() / 200) * 3;
                    ctx.strokeStyle = '#e74c3c';
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.ellipse(step.x - 20, step.y - 8, pulseSize, pulseSize, 0, 0, Math.PI * 2);
                    ctx.stroke();
                }
            });
        }
        
        // 绘制进度指示器
        function drawProgressIndicator() {
            const progress = currentStep === 0 ? animationTime / 25 : stepProgress[currentStep];
            
            if (progress > 0) {
                ctx.fillStyle = 'rgba(52, 152, 219, 0.8)';
                ctx.fillRect(20, canvas.height - 15, (canvas.width - 40) * progress, 8);
                
                ctx.fillStyle = '#2c3e50';
                ctx.font = '12px Arial';
                ctx.textAlign = 'left';
                const percent = Math.round(progress * 100);
                ctx.fillText(`进度: ${percent}%`, 20, canvas.height - 25);
            }
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

## 《中心法则完整流程》交互式教学动画使用指南

欢迎使用《中心法则完整流程》交互式教学动画！本指南将帮助您充分利用这一教学工具，深入了解分子生物学的核心原理——中心法则。

---

### 一、 功能说明

本动画以直观、动态的方式，可视化呈现了遗传信息从DNA到功能蛋白质的完整流动过程：
1. **DNA复制**：在细胞核内，DNA双链解开并复制
2. **转录**：以DNA为模板合成mRNA
3. **RNA剪接**：去除内含子，连接外显子，形成成熟mRNA
4. **翻译**：在核糖体上，将mRNA序列翻译为氨基酸序列
5. **蛋白质折叠**：多肽链折叠形成具有特定三维结构的功能蛋白质

动画采用**从左到右的空间布局**，清晰展示了分子从细胞核（左侧）到细胞质（右侧）的转移过程，符合生物学真实情境。

---

### 二、 主要功能

#### 1. 动画控制功能
- **完整流程播放**：点击“播放动画”按钮，观看从DNA复制到蛋白质折叠的完整连续过程
- **分步学习**：点击步骤按钮（1-5），专注于特定过程的学习
- **进度控制**：使用“播放/暂停”和“重置”按钮控制动画节奏
- **步骤跳转**：通过步骤进度条或标签页直接跳转到感兴趣的部分

#### 2. 交互学习功能
- **分子悬停提示**：将鼠标悬停在关键分子（DNA、mRNA、tRNA等）上，显示其名称和简要说明
- **过程控制交互**：
  - 在翻译步骤，可手动拖拽tRNA到核糖体
  - 在剪接步骤，可点击执行内含子切除
- **即时知识测验**：每个步骤结束后，弹出相关选择题，提供即时反馈
- **标签开关**：可显示/隐藏所有分子标签，保持画面清晰

#### 3. 认知辅助功能
- **视觉图例**：右侧面板提供完整的分子颜色编码图例
- **步骤信息面板**：实时显示当前步骤的详细说明、关键点和生物学意义
- **空间标注**：清晰标注“细胞核”和“细胞质”区域，强化空间概念
- **进度可视化**：底部进度条显示当前动画完成百分比

---

### 三、 设计特色

#### 1. 科学准确性
- **分子表示标准化**：DNA双螺旋、tRNA三叶草形状、核糖体结构等均采用生物学标准表示法
- **过程顺序准确**：严格遵循中心法则的信息流向：DNA → RNA → 蛋白质
- **空间定位正确**：复制、转录、剪接发生在细胞核，翻译和折叠发生在细胞质

#### 2. 教学友好性
- **多层级呈现**：
  - 第一层：完整流程动画，建立整体概念
  - 第二层：分步详细演示，理解具体机制
  - 第三层：分子细节提示，掌握专业术语
- **认知负荷管理**：通过颜色编码、渐进式呈现和交互控制，避免信息过载
- **错误容忍设计**：交互操作提供明确反馈，允许尝试和修正

#### 3. 视觉设计
- **专业配色方案**：
  - DNA：蓝色系（深蓝/浅蓝）
  - RNA：红色/橙色
  - tRNA：绿色
  - 核糖体：紫色
  - 蛋白质：金色
- **动态效果**：
  - 平滑的分子运动动画
  - 关键事件高亮（如键的形成、片段切除）
  - 生长动画（RNA链延伸、多肽链合成）
  - 变形动画（蛋白质折叠）

---

### 四、 教学要点

#### 核心概念强调
1. **信息流向不可逆性**：DNA → RNA → 蛋白质的单向信息流动
2. **碱基互补配对**：A-T/U，C-G的配对原则贯穿复制、转录和翻译
3. **中心法则的例外**：可简要提及逆转录和RNA复制，作为知识延伸

#### 常见难点解析
1. **复制 vs 转录**：
   - 复制：产物是DNA，需要DNA聚合酶，整个DNA分子复制
   - 转录：产物是RNA，需要RNA聚合酶，仅一条DNA链作为模板
2. **内含子 vs 外显子**：
   - 内含子：非编码序列，在剪接中被移除
   - 外显子：编码序列，在剪接后连接形成成熟mRNA
3. **密码子与反密码子**：
   - 密码子：mRNA上三个连续的碱基
   - 反密码子：tRNA上与之互补的三个碱基

#### 教学顺序建议
1. **整体概览**：先观看完整流程动画，建立宏观理解
2. **分步深入学习**：按顺序学习每个步骤，完成相应测验
3. **比较学习**：对比复制与转录的异同，理解剪接的意义
4. **综合应用**：解释突变如何通过中心法则影响蛋白质功能

---

### 五、 使用建议

#### 课堂应用场景
1. **新课导入**：播放完整动画，激发学生兴趣，提出核心问题
2. **难点突破**：针对特定步骤（如剪接、翻译）反复观看和交互操作
3. **复习巩固**：学生自主操作，完成知识测验，检测学习效果
4. **小组探究**：分配不同小组研究不同步骤，然后汇报讲解

#### 自主学习策略
1. **主动探索模式**：
   - 第一步：不看说明，先尝试操作，形成自己的理解
   - 第二步：观看动画，验证和修正自己的理解
   - 第三步：完成测验，评估掌握程度
2. **笔记建议**：鼓励学生在观看时绘制自己的中心法则流程图
3. **问题导向学习**：围绕以下问题展开学习：
   - 遗传信息是如何存储的？
   - 信息如何从DNA传递到蛋白质？
   - 每个步骤的关键酶和分子是什么？
   - 如果某一步出错，会产生什么后果？

#### 技术使用提示
1. **设备要求**：建议使用电脑或平板电脑，确保屏幕足够大以查看细节
2. **浏览器兼容**：支持所有现代浏览器（Chrome、Firefox、Safari、Edge）
3. **网络环境**：动画完全在本地运行，无需网络连接即可使用
4. **辅助功能**：如需调整视觉元素，可使用浏览器缩放功能

---

### 六、 扩展学习建议

完成本动画学习后，建议进一步探索：
1. **真实案例研究**：镰刀型细胞贫血症（单碱基突变的影响）
2. **技术应用**：PCR技术（体外DNA复制）、基因工程（中心法则的应用）
3. **前沿发展**：表观遗传学（超越中心法则的遗传调控）
4. **跨学科联系**：信息论（遗传信息编码）、化学（分子相互作用）

---

**祝您探索愉快！通过这个交互式动画，您不仅能看到中心法则，更能理解它、掌握它，感受分子生物学之美。**

*如有任何使用问题或教学建议，欢迎反馈。让我们共同完善这一教学工具！*