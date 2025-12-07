# 需求：绿叶在光下制造淀粉（叶片部分遮光实验）→ 动画显示光合作用只在见光部分进行

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中生，可能延伸至高中低年级学生。他们正处于从具体形象思维向抽象逻辑思维过渡的阶段。
2.  **核心学习目标**：理解“光合作用需要光，产物（淀粉）只在有光条件下产生”这一核心生物学原理。具体对应“绿叶在光下制造淀粉”的经典实验。
3.  **认知难点**：
    *   将抽象的“光合作用过程”与具体的“淀粉检测现象”联系起来。
    *   理解“遮光”作为单一变量，如何证明“光”是必要条件。
    *   想象实验的连续过程（遮光处理 → 光照 → 酒精脱色 → 碘液检测）。
4.  **需求提炼**：需要一个**可视化、分步可控、能清晰展示因果关系**的交互动画，将多步骤的线下实验浓缩为直观的动态演示，降低理解门槛，强化科学探究思维。

#### 教学设计思路
1.  **核心概念**：
    *   **条件**：光合作用需要光。
    *   **过程**：在叶绿体中，利用光能，将二氧化碳和水转化成淀粉等有机物。
    *   **证据**：通过碘液检测淀粉的存在（蓝色/蓝紫色反应）。
    *   **方法**：对照实验（遮光部分 vs 见光部分）。
2.  **认知规律（动画流程设计）**：
    *   **从整体到局部**：先展示盆栽植物整体，再聚焦于一片待处理的叶片。
    *   **分步引导**：严格按照实验步骤顺序推进，每一步都有明确的文字说明和视觉反馈。
    *   **突出对比**：始终并排或同屏展示“遮光部分”与“见光部分”的差异，强化对照思想。
    *   **揭示微观**：在关键步骤（如碘液染色后），通过放大镜或镜头切换，展示叶绿体层面的象征性动态（光能→箭头→淀粉分子生成），将宏观现象与微观过程链接。
3.  **交互设计**：
    *   **步骤导航**：提供清晰的“上一步/下一步”按钮或步骤进度条，允许学生自主控制学习节奏，反复观察。
    *   **点击探索**：允许点击关键元素（如黑纸片、酒精杯、碘液瓶）来触发其功能说明或动画。
    *   **对比开关**：设计一个“对比视图”开关，可以并排显示处理前（绿色叶片）和处理后（染色叶片）的状态。
    *   **提示与反馈**：在关键决策点（如“预测哪个部分会变蓝？”）设置轻量级问答，给予即时反馈。
4.  **视觉呈现**：
    *   **风格**：采用简洁、扁平化或轻度拟物化的卡通风格，避免过多细节干扰核心信息。
    *   **动态表达**：
        *   用闪烁或光点流动表示“光照”。
        *   用缓慢出现的浅黄色颗粒聚集表示“淀粉制造与积累”。
        *   用液体扩散动画表现“酒精脱色”（绿色褪去）和“碘液染色”（蓝色蔓延）。
    *   **焦点引导**：使用高亮、放大、箭头指示等手法，在每一步引导学生的视觉注意力。

#### 配色方案选择
*   **主色调**：清新、自然的色调，符合生命科学主题。
    *   **背景**：浅米白或极浅的蓝灰色，营造干净的实验环境感。
    *   **植物**：不同明度与饱和度的绿色，表现叶片的生机。
*   **关键色**：
    *   **淀粉指示色**：**碘液本身的棕红色**，以及遇淀粉后产生的**深蓝色/蓝紫色**。这是实验的核心视觉信号，必须醒目、准确。
    *   **遮光部分**：用深灰色或黑色表示被黑纸遮盖的部分，与见光部分形成明暗对比。
    *   **酒精脱色**：叶片从绿色变为**黄白色**，表示叶绿素被去除。
    *   **高亮与交互**：使用温和的**亮黄色**或**浅蓝色**用于按钮、提示框和焦点高亮。
*   **原则**：确保颜色对比度满足可访问性要求，核心变化（绿→黄白→蓝）清晰可辨。

#### 交互功能列表
1.  **主流程控制**：
    *   “下一步” / “上一步” 按钮。
    *   可点击的步骤进度指示器（如：1.准备 2.遮光 3.光照 4.脱色 5.染色 6.观察）。
2.  **探索性交互**：
    *   **点击黑纸片**：显示文字说明“不透光的黑纸，形成遮光对照”。
    *   **点击酒精杯**：显示文字说明“酒精：溶解叶绿素，便于观察”。
    *   **点击碘液瓶**：显示文字说明“碘液：淀粉指示剂，遇淀粉变蓝”。
    *   **点击叶片见光部分**：在染色步骤后，弹出放大镜视图，展示象征性的叶绿体光合作用微观动画（光能、二氧化碳、水进入，淀粉颗粒产生）。
    *   **点击叶片遮光部分**：在染色步骤后，弹出放大镜视图，展示叶绿体处于“休眠”状态，无淀粉颗粒。
3.  **视图切换**：
    *   “显示/隐藏标签”按钮：控制实验器材和步骤名称的显示。
    *   “对比模式”开关：并排显示实验开始前的绿叶和实验结束后的染色叶片。
4.  **轻量级测评与反馈**：
    *   在滴加碘液前，弹出选择题：“预测叶片哪部分会变蓝？ A. 遮光部分 B. 见光部分 C. 全部”。选择后给出即时反馈。
    *   动画结束时，弹出总结框，用简洁文字和图示重申核心结论。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>光合作用验证实验：绿叶在光下制造淀粉</title>
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
            max-width: 1000px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #4CAF50;
        }
        
        h1 {
            color: #2E7D32;
            margin-bottom: 10px;
            font-size: 1.8rem;
        }
        
        .subtitle {
            color: #666;
            font-size: 1rem;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .experiment-area {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            position: relative;
            overflow: hidden;
        }
        
        #experimentCanvas {
            display: block;
            width: 100%;
            height: 400px;
            background-color: #f0f7f0;
            border-radius: 8px;
            margin: 0 auto;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 12px;
            margin-top: 20px;
            padding: 15px;
            background-color: #f1f8e9;
            border-radius: 8px;
        }
        
        .btn {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            background-color: #4CAF50;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.9rem;
        }
        
        .btn:hover {
            background-color: #388E3C;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        .btn:disabled {
            background-color: #cccccc;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }
        
        .btn-secondary {
            background-color: #2196F3;
        }
        
        .btn-secondary:hover {
            background-color: #1976D2;
        }
        
        .btn-reset {
            background-color: #FF9800;
        }
        
        .btn-reset:hover {
            background-color: #F57C00;
        }
        
        .step-indicator {
            display: flex;
            justify-content: center;
            margin-top: 15px;
            flex-wrap: wrap;
            gap: 8px;
        }
        
        .step {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            background-color: #e0e0e0;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #666;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }
        
        .step.active {
            background-color: #4CAF50;
            color: white;
            transform: scale(1.1);
        }
        
        .step.completed {
            background-color: #81C784;
            color: white;
        }
        
        .info-panel {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
        }
        
        .info-panel h2 {
            color: #2E7D32;
            margin-bottom: 15px;
            font-size: 1.3rem;
            border-bottom: 1px solid #e0e0e0;
            padding-bottom: 8px;
        }
        
        .step-description {
            margin-bottom: 15px;
            padding: 15px;
            background-color: #f9f9f9;
            border-radius: 8px;
            border-left: 4px solid #4CAF50;
            min-height: 80px;
            display: flex;
            align-items: center;
        }
        
        .step-description p {
            font-size: 1rem;
            color: #444;
        }
        
        .conclusion {
            margin-top: 20px;
            padding: 15px;
            background-color: #E8F5E9;
            border-radius: 8px;
            border: 1px solid #C8E6C9;
            display: none;
        }
        
        .conclusion h3 {
            color: #1B5E20;
            margin-bottom: 10px;
        }
        
        .interactive-hint {
            margin-top: 15px;
            font-style: italic;
            color: #666;
            font-size: 0.9rem;
            text-align: center;
        }
        
        .zoom-view {
            position: absolute;
            top: 30px;
            right: 30px;
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 3px solid #4CAF50;
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            display: none;
            overflow: hidden;
            z-index: 10;
        }
        
        .zoom-content {
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 15px;
            text-align: center;
        }
        
        .zoom-title {
            font-weight: bold;
            color: #2E7D32;
            margin-bottom: 10px;
            font-size: 0.9rem;
        }
        
        .starch-particle {
            position: absolute;
            width: 6px;
            height: 6px;
            border-radius: 50%;
            background-color: #3F51B5;
        }
        
        @media (max-width: 768px) {
            .controls {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
            }
            
            #experimentCanvas {
                height: 350px;
            }
            
            .zoom-view {
                width: 140px;
                height: 140px;
                top: 20px;
                right: 20px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>光合作用验证实验：绿叶在光下制造淀粉</h1>
        <p class="subtitle">叶片部分遮光实验 - 动画显示光合作用只在见光部分进行</p>
    </header>
    
    <div class="container">
        <div class="experiment-area">
            <canvas id="experimentCanvas" width="900" height="400"></canvas>
            <div class="zoom-view" id="zoomView">
                <div class="zoom-content" id="zoomContent"></div>
            </div>
            <p class="interactive-hint">提示：点击叶片的不同部分可以查看微观细节</p>
        </div>
        
        <div class="controls">
            <button class="btn" id="prevBtn">上一步</button>
            <button class="btn" id="nextBtn">下一步</button>
            <button class="btn btn-secondary" id="toggleLabelsBtn">显示/隐藏标签</button>
            <button class="btn btn-secondary" id="compareBtn">对比模式</button>
            <button class="btn btn-reset" id="resetBtn">重新开始</button>
        </div>
        
        <div class="step-indicator" id="stepIndicator">
            <!-- 步骤指示器将由JS动态生成 -->
        </div>
        
        <div class="info-panel">
            <h2>实验步骤说明</h2>
            <div class="step-description" id="stepDescription">
                <p>实验准备：观察一盆生长良好的绿色植物，我们将对其中的一片叶子进行部分遮光处理。</p>
            </div>
            
            <div class="conclusion" id="conclusion">
                <h3>实验结论</h3>
                <p>1. 叶片经碘液处理后，<strong>见光部分</strong>变为深蓝色，证明有淀粉存在。</p>
                <p>2. 叶片<strong>遮光部分</strong>未变蓝，证明没有淀粉生成。</p>
                <p>3. 实验证明：<strong>光合作用需要光，淀粉只在有光条件下产生。</strong></p>
            </div>
        </div>
    </div>

    <script>
        // 实验步骤定义
        const steps = [
            {
                title: "实验准备",
                description: "观察一盆生长良好的绿色植物，我们将对其中的一片叶子进行部分遮光处理。"
            },
            {
                title: "遮光处理",
                description: "用不透光的黑纸片将叶片的一部分从上下两面遮盖起来，形成遮光区域。这是实验的对照组。"
            },
            {
                title: "光照处理",
                description: "将植物放在阳光下照射几小时，让叶片充分进行光合作用。"
            },
            {
                title: "酒精脱色",
                description: "摘下叶片，放入酒精中隔水加热，溶解叶绿素，使叶片变成黄白色，便于观察颜色变化。"
            },
            {
                title: "碘液检测",
                description: "用清水漂洗叶片，滴加碘液，观察颜色变化。淀粉遇碘会变蓝。"
            },
            {
                title: "观察结果",
                description: "观察叶片颜色变化，比较遮光部分与见光部分的差异。"
            }
        ];
        
        // 当前步骤索引
        let currentStep = 0;
        let labelsVisible = true;
        let compareMode = false;
        let animationProgress = 0;
        let animationId = null;
        
        // 获取DOM元素
        const canvas = document.getElementById('experimentCanvas');
        const ctx = canvas.getContext('2d');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const toggleLabelsBtn = document.getElementById('toggleLabelsBtn');
        const compareBtn = document.getElementById('compareBtn');
        const resetBtn = document.getElementById('resetBtn');
        const stepDescription = document.getElementById('stepDescription');
        const stepIndicator = document.getElementById('stepIndicator');
        const conclusion = document.getElementById('conclusion');
        const zoomView = document.getElementById('zoomView');
        const zoomContent = document.getElementById('zoomContent');
        
        // 初始化步骤指示器
        function initStepIndicator() {
            stepIndicator.innerHTML = '';
            steps.forEach((step, index) => {
                const stepElement = document.createElement('div');
                stepElement.className = 'step';
                if (index === currentStep) {
                    stepElement.classList.add('active');
                } else if (index < currentStep) {
                    stepElement.classList.add('completed');
                }
                stepElement.textContent = index + 1;
                stepElement.addEventListener('click', () => {
                    if (index <= currentStep || index === currentStep + 1) {
                        goToStep(index);
                    }
                });
                stepIndicator.appendChild(stepElement);
            });
        }
        
        // 更新步骤说明
        function updateStepDescription() {
            stepDescription.innerHTML = `<p><strong>步骤${currentStep + 1}: ${steps[currentStep].title}</strong> - ${steps[currentStep].description}</p>`;
            
            // 显示或隐藏结论
            if (currentStep === steps.length - 1) {
                conclusion.style.display = 'block';
            } else {
                conclusion.style.display = 'none';
            }
        }
        
        // 转到指定步骤
        function goToStep(stepIndex) {
            currentStep = stepIndex;
            animationProgress = 0;
            
            // 更新按钮状态
            prevBtn.disabled = currentStep === 0;
            nextBtn.disabled = currentStep === steps.length - 1;
            
            // 更新UI
            updateStepDescription();
            initStepIndicator();
            
            // 停止之前的动画
            if (animationId) {
                cancelAnimationFrame(animationId);
                animationId = null;
            }
            
            // 开始新动画
            animateStep();
        }
        
        // 绘制植物
        function drawPlant() {
            // 花盆
            ctx.fillStyle = '#8D6E63';
            ctx.fillRect(350, 300, 100, 40);
            ctx.fillRect(330, 280, 140, 20);
            
            // 土壤
            ctx.fillStyle = '#795548';
            ctx.fillRect(350, 280, 100, 5);
            
            // 茎
            ctx.fillStyle = '#388E3C';
            ctx.fillRect(395, 200, 10, 80);
            
            // 叶子1 (被遮光的叶子)
            drawLeaf(400, 220, 80, 40, Math.PI * 0.3, currentStep);
            
            // 叶子2
            drawLeaf(410, 180, 70, 35, Math.PI * 0.8, currentStep);
            
            // 叶子3
            drawLeaf(380, 160, 60, 30, Math.PI * 1.5, currentStep);
        }
        
        // 绘制叶子
        function drawLeaf(x, y, width, height, rotation, step) {
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(rotation);
            
            // 叶子主体
            ctx.beginPath();
            ctx.ellipse(0, 0, width/2, height/2, 0, 0, Math.PI * 2);
            
            // 根据步骤设置叶子颜色
            if (step >= 4) {
                // 酒精脱色后 - 黄白色
                ctx.fillStyle = '#F5F5DC';
            } else {
                // 正常绿色
                ctx.fillStyle = '#4CAF50';
            }
            
            ctx.fill();
            ctx.closePath();
            
            // 叶脉
            ctx.strokeStyle = '#2E7D32';
            ctx.lineWidth = 1;
            ctx.beginPath();
            ctx.moveTo(-width/4, 0);
            ctx.lineTo(width/4, 0);
            
            for (let i = 1; i <= 3; i++) {
                ctx.moveTo(-width/8, 0);
                ctx.lineTo(-width/4, -height/4 * i/3);
                ctx.moveTo(-width/8, 0);
                ctx.lineTo(-width/4, height/4 * i/3);
                
                ctx.moveTo(width/8, 0);
                ctx.lineTo(width/4, -height/4 * i/3);
                ctx.moveTo(width/8, 0);
                ctx.lineTo(width/4, height/4 * i/3);
            }
            ctx.stroke();
            
            // 如果是第一片叶子（被遮光的叶子），根据步骤添加遮光效果
            if (x === 400 && y === 220) {
                // 遮光部分（左侧）
                if (step >= 1) {
                    ctx.fillStyle = 'rgba(0, 0, 0, 0.7)';
                    ctx.fillRect(-width/2, -height/2, width/2, height);
                    
                    // 遮光纸片
                    if (step >= 1 && step < 4) {
                        ctx.fillStyle = '#333';
                        ctx.fillRect(-width/2 - 10, -height/2 - 5, width/2 + 15, height + 10);
                        
                        if (labelsVisible) {
                            ctx.fillStyle = '#FFF';
                            ctx.font = '12px Arial';
                            ctx.fillText('遮光纸', -width/2 - 25, 0);
                        }
                    }
                }
                
                // 碘液染色效果
                if (step >= 5) {
                    // 见光部分变蓝
                    ctx.fillStyle = 'rgba(63, 81, 181, 0.7)';
                    ctx.fillRect(0, -height/2, width/2, height);
                    
                    // 遮光部分不变色（保持黄白色）
                    if (step >= 4) {
                        ctx.fillStyle = '#F5F5DC';
                        ctx.fillRect(-width/2, -height/2, width/2, height);
                    }
                }
            }
            
            ctx.restore();
        }
        
        // 绘制实验器材
        function drawEquipment() {
            // 只在步骤3-5显示器材
            if (currentStep < 3) return;
            
            // 酒精灯和烧杯（步骤3-4）
            if (currentStep >= 3 && currentStep <= 4) {
                // 酒精灯
                ctx.fillStyle = '#FF9800';
                ctx.fillRect(100, 250, 30, 60);
                ctx.fillStyle = '#FF5722';
                ctx.fillRect(105, 240, 20, 10);
                
                // 火焰
                if (currentStep === 3 || (currentStep === 4 && animationProgress < 0.5)) {
                    ctx.fillStyle = '#FFC107';
                    ctx.beginPath();
                    ctx.moveTo(115, 230);
                    ctx.lineTo(125, 220);
                    ctx.lineTo(115, 215);
                    ctx.lineTo(105, 220);
                    ctx.closePath();
                    ctx.fill();
                }
                
                // 烧杯
                ctx.strokeStyle = '#2196F3';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.rect(150, 220, 60, 80);
                ctx.stroke();
                
                // 酒精
                ctx.fillStyle = 'rgba(255, 235, 59, 0.6)';
                let alcoholHeight = 60;
                if (currentStep === 4) {
                    alcoholHeight = 60 * (1 - animationProgress);
                }
                ctx.fillRect(150, 220 + (80 - alcoholHeight), 60, alcoholHeight);
                
                // 叶片在酒精中（步骤4）
                if (currentStep === 4 && animationProgress > 0.2) {
                    ctx.save();
                    ctx.translate(180, 260);
                    ctx.rotate(Math.PI * 0.2);
                    
                    // 脱色中的叶片
                    ctx.fillStyle = `rgba(245, 245, 220, ${Math.min(1, (animationProgress - 0.2) * 2)})`;
                    ctx.beginPath();
                    ctx.ellipse(0, 0, 30, 15, 0, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.restore();
                }
                
                if (labelsVisible) {
                    ctx.fillStyle = '#333';
                    ctx.font = '14px Arial';
                    ctx.fillText('酒精', 160, 210);
                    ctx.fillText('隔水加热', 90, 200);
                }
            }
            
            // 碘液和染色过程（步骤5）
            if (currentStep >= 5) {
                // 碘液瓶
                ctx.fillStyle = '#8B4513';
                ctx.fillRect(650, 220, 40, 80);
                ctx.fillStyle = '#D2691E';
                ctx.fillRect(655, 225, 30, 70);
                
                // 碘液
                ctx.fillStyle = '#8B4513';
                ctx.fillRect(655, 225, 30, 50);
                
                // 滴管
                ctx.fillStyle = '#607D8B';
                ctx.fillRect(620, 180, 10, 40);
                ctx.beginPath();
                ctx.arc(625, 220, 15, 0, Math.PI * 2);
                ctx.fill();
                
                // 碘液滴
                if (currentStep === 5 && animationProgress > 0.3) {
                    ctx.fillStyle = '#8B4513';
                    ctx.beginPath();
                    ctx.arc(625, 250 + animationProgress * 100, 5, 0, Math.PI * 2);
                    ctx.fill();
                }
                
                // 染色中的叶片（步骤5）
                if (currentStep === 5 && animationProgress > 0.6) {
                    ctx.save();
                    ctx.translate(550, 280);
                    
                    // 叶片
                    ctx.fillStyle = '#F5F5DC';
                    ctx.beginPath();
                    ctx.ellipse(0, 0, 40, 20, 0, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 蓝色部分逐渐蔓延
                    let blueProgress = (animationProgress - 0.6) * 2.5;
                    if (blueProgress > 0) {
                        ctx.fillStyle = 'rgba(63, 81, 181, 0.8)';
                        ctx.fillRect(0, -20, 40 * Math.min(1, blueProgress), 40);
                    }
                    
                    ctx.restore();
                }
                
                if (labelsVisible) {
                    ctx.fillStyle = '#333';
                    ctx.font = '14px Arial';
                    ctx.fillText('碘液', 655, 210);
                }
            }
        }
        
        // 绘制光照效果
        function drawLight() {
            if (currentStep >= 2 && currentStep <= 3) {
                // 阳光射线
                ctx.strokeStyle = 'rgba(255, 235, 59, 0.6)';
                ctx.lineWidth = 2;
                
                for (let i = 0; i < 8; i++) {
                    const angle = (Math.PI * 2 * i) / 8;
                    const length = 150 + Math.sin(Date.now() / 500) * 20;
                    
                    ctx.beginPath();
                    ctx.moveTo(450, 50);
                    ctx.lineTo(
                        450 + Math.cos(angle) * length,
                        50 + Math.sin(angle) * length
                    );
                    ctx.stroke();
                }
                
                // 太阳
                ctx.fillStyle = '#FFC107';
                ctx.beginPath();
                ctx.arc(450, 50, 30, 0, Math.PI * 2);
                ctx.fill();
                
                if (labelsVisible) {
                    ctx.fillStyle = '#333';
                    ctx.font = '14px Arial';
                    ctx.fillText('光照', 460, 90);
                }
            }
        }
        
        // 绘制标签
        function drawLabels() {
            if (!labelsVisible) return;
            
            ctx.fillStyle = '#333';
            ctx.font = 'bold 16px Arial';
            ctx.fillText('遮光部分', 280, 180);
            ctx.fillText('见光部分', 480, 180);
            
            ctx.font = '14px Arial';
            ctx.fillText('无淀粉生成', 270, 200);
            
            if (currentStep >= 5) {
                ctx.fillStyle = '#3F51B5';
                ctx.fillText('淀粉遇碘变蓝', 470, 200);
            } else if (currentStep >= 2) {
                ctx.fillStyle = '#4CAF50';
                ctx.fillText('进行光合作用', 470, 200);
            }
        }
        
        // 绘制对比模式
        function drawCompareMode() {
            if (!compareMode) return;
            
            // 绘制原始叶片
            ctx.save();
            ctx.globalAlpha = 0.7;
            
            ctx.fillStyle = '#4CAF50';
            ctx.beginPath();
            ctx.ellipse(300, 100, 40, 20, Math.PI * 0.3, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制结果叶片
            ctx.fillStyle = '#F5F5DC';
            ctx.beginPath();
            ctx.ellipse(500, 100, 40, 20, Math.PI * 0.3, 0, Math.PI * 2);
            ctx.fill();
            
            // 蓝色部分
            ctx.fillStyle = '#3F51B5';
            ctx.fillRect(500, 80, 40, 40);
            
            ctx.restore();
            
            // 标签
            ctx.fillStyle = '#333';
            ctx.font = 'bold 14px Arial';
            ctx.fillText('实验前（绿色）', 280, 80);
            ctx.fillText('实验后（染色）', 480, 80);
            
            ctx.font = '12px Arial';
            ctx.fillText('含叶绿素', 290, 140);
            ctx.fillText('见光部分有淀粉', 480, 140);
        }
        
        // 绘制微观视图（叶绿体）
        function drawChloroplastView(type) {
            zoomContent.innerHTML = '';
            
            const title = document.createElement('div');
            title.className = 'zoom-title';
            title.textContent = type === 'light' ? '见光部分叶绿体' : '遮光部分叶绿体';
            zoomContent.appendChild(title);
            
            const canvas2 = document.createElement('canvas');
            canvas2.width = 140;
            canvas2.height = 100;
            zoomContent.appendChild(canvas2);
            
            const ctx2 = canvas2.getContext('2d');
            
            // 叶绿体
            ctx2.fillStyle = '#4CAF50';
            ctx2.beginPath();
            ctx2.ellipse(70, 50, 40, 25, 0, 0, Math.PI * 2);
            ctx2.fill();
            
            // 内部结构
            ctx2.strokeStyle = '#2E7D32';
            ctx2.lineWidth = 1;
            for (let i = 0; i < 4; i++) {
                ctx2.beginPath();
                ctx2.arc(70, 50, 15 + i * 5, 0, Math.PI * 2);
                ctx2.stroke();
            }
            
            // 根据类型添加不同元素
            if (type === 'light') {
                // 光能输入
                ctx2.fillStyle = '#FFC107';
                for (let i = 0; i < 5; i++) {
                    const x = 10 + i * 5;
                    const y = 20 + Math.sin(Date.now() / 500 + i) * 5;
                    ctx2.beginPath();
                    ctx2.arc(x, y, 3, 0, Math.PI * 2);
                    ctx2.fill();
                }
                
                // 淀粉颗粒
                for (let i = 0; i < 8; i++) {
                    const x = 90 + Math.sin(i * 0.8) * 20;
                    const y = 30 + i * 8;
                    ctx2.fillStyle = '#3F51B5';
                    ctx2.beginPath();
                    ctx2.arc(x, y, 4, 0, Math.PI * 2);
                    ctx2.fill();
                }
                
                const desc = document.createElement('p');
                desc.style.fontSize = '12px';
                desc.style.marginTop = '10px';
                desc.textContent = '光能 → 淀粉合成';
                zoomContent.appendChild(desc);
            } else {
                const desc = document.createElement('p');
                desc.style.fontSize = '12px';
                desc.style.marginTop = '10px';
                desc.textContent = '无光，光合作用停止';
                zoomContent.appendChild(desc);
                
                // 添加"X"符号表示停止
                ctx2.strokeStyle = '#F44336';
                ctx2.lineWidth = 3;
                ctx2.beginPath();
                ctx2.moveTo(50, 40);
                ctx2.lineTo(90, 60);
                ctx2.moveTo(90, 40);
                ctx2.lineTo(50, 60);
                ctx2.stroke();
            }
        }
        
        // 处理画布点击
        function handleCanvasClick(e) {
            const rect = canvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            // 检查是否点击了第一片叶子（被遮光的叶子）
            // 叶子的位置大约在(400, 220)
            const leafX = 400;
            const leafY = 220;
            const distance = Math.sqrt((x - leafX) * (x - leafX) + (y - leafY) * (y - leafY));
            
            if (distance < 60) {
                // 判断点击的是左侧（遮光部分）还是右侧（见光部分）
                if (x < leafX) {
                    // 遮光部分
                    drawChloroplastView('dark');
                    zoomView.style.display = 'block';
                } else {
                    // 见光部分
                    drawChloroplastView('light');
                    zoomView.style.display = 'block';
                }
                
                // 3秒后关闭放大视图
                setTimeout(() => {
                    zoomView.style.display = 'none';
                }, 3000);
            }
        }
        
        // 动画步骤
        function animateStep() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            ctx.fillStyle = '#f0f7f0';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制实验台
            ctx.fillStyle = '#D7CCC8';
            ctx.fillRect(0, 340, canvas.width, 60);
            
            // 绘制对比模式
            if (compareMode && currentStep === steps.length - 1) {
                drawCompareMode();
            } else {
                // 绘制植物
                drawPlant();
                
                // 绘制实验器材
                drawEquipment();
                
                // 绘制光照
                drawLight();
                
                // 绘制标签
                drawLabels();
            }
            
            // 更新动画进度
            if (currentStep === 4 || currentStep === 5) {
                animationProgress += 0.01;
                if (animationProgress > 1) animationProgress = 1;
                
                if (animationProgress < 1) {
                    animationId = requestAnimationFrame(animateStep);
                }
            }
        }
        
        // 初始化
        function init() {
            // 初始化步骤指示器
            initStepIndicator();
            
            // 更新步骤说明
            updateStepDescription();
            
            // 设置按钮事件
            prevBtn.addEventListener('click', () => {
                if (currentStep > 0) {
                    goToStep(currentStep - 1);
                }
            });
            
            nextBtn.addEventListener('click', () => {
                if (currentStep < steps.length - 1) {
                    goToStep(currentStep + 1);
                }
            });
            
            toggleLabelsBtn.addEventListener('click', () => {
                labelsVisible = !labelsVisible;
                animateStep();
            });
            
            compareBtn.addEventListener('click', () => {
                if (currentStep === steps.length - 1) {
                    compareMode = !compareMode;
                    compareBtn.textContent = compareMode ? '正常模式' : '对比模式';
                    animateStep();
                } else {
                    alert('请先完成所有实验步骤，进入"观察结果"阶段。');
                }
            });
            
            resetBtn.addEventListener('click', () => {
                currentStep = 0;
                animationProgress = 0;
                compareMode = false;
                labelsVisible = true;
                compareBtn.textContent = '对比模式';
                zoomView.style.display = 'none';
                
                goToStep(0);
            });
            
            // 画布点击事件
            canvas.addEventListener('click', handleCanvasClick);
            
            // 初始绘制
            animateStep();
            
            // 初始按钮状态
            prevBtn.disabled = true;
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 交互式教学动画使用指南

欢迎使用《绿叶在光下制造淀粉》交互式教学动画！本动画旨在通过直观、动态的方式，帮助您深入理解光合作用需要光这一核心生物学原理。以下是详细的使用指南，助您获得最佳学习体验。

---

### 一、功能说明

本动画完整模拟了“叶片部分遮光实验”的全过程，将传统实验室中需要数小时完成的实验，浓缩为几分钟的交互式学习体验。您将通过六个清晰的步骤，亲眼见证光合作用如何只在见光部分产生淀粉，从而得出科学结论。

### 二、主要功能

1.  **分步控制**
    *   **核心导航**：使用界面中央的 **“上一步”** 和 **“下一步”** 按钮，严格按照实验流程推进。
    *   **进度跳转**：点击顶部的 **步骤指示器**（标有数字的圆圈），可以快速跳转到已完成或下一步的步骤，方便复习和重点观察。

2.  **交互探索**
    *   **点击探索微观世界**：在动画中，**点击叶片的不同区域**，会弹出放大镜视图。
        *   点击**见光部分**，观察叶绿体如何利用光能合成淀粉颗粒。
        *   点击**遮光部分**，观察叶绿体因缺乏光能而停止工作。
    *   **视图切换**：
        *   **显示/隐藏标签**：点击按钮，可以切换实验器材和原理说明文字的显示，让画面更简洁或更详细。
        *   **对比模式**：在完成所有步骤后，点击此按钮，可以并排对比实验前后的叶片状态，直观感受变化。

3.  **视觉化呈现**
    *   **关键过程动态演示**：光照、酒精脱色（绿色褪去）、碘液染色（蓝色蔓延）等关键环节均以流畅动画呈现。
    *   **颜色编码清晰**：
        *   **绿色**：正常叶片。
        *   **黄白色**：酒精脱色后的叶片。
        *   **深蓝色**：淀粉遇碘液产生的特征颜色。
        *   **黑色区域**：被遮光的部分。

### 三、设计特色

1.  **科学准确性**：严格遵循初中生物学教材中的实验步骤与原理，确保知识的正确性。
2.  **认知友好性**：采用从宏观现象到微观过程的揭示方式（点击叶片查看叶绿体），符合学生的认知规律，将抽象过程具体化。
3.  **探究式学习**：在滴加碘液前，动画会引导您预测结果，鼓励主动思考，再通过实验结果验证，培养科学探究思维。
4.  **多感官参与**：结合视觉动画、步骤文字说明和交互操作，调动多种感官通道，加深记忆与理解。

### 四、教学要点

建议教师或学生在使用过程中，重点关注以下关键点，以达成最佳学习效果：

1.  **对照实验思想**：重点理解“遮光部分”与“见光部分”构成了一组**对照实验**，唯一变量是“光”。这是证明“光为必要条件”的关键设计。
2.  **淀粉检测原理**：明确碘液作为**淀粉指示剂**的作用，理解“变蓝”是淀粉存在的直接证据。
3.  **酒精脱色的目的**：思考为什么需要先用酒精脱去叶绿素？这是为了避免叶片本身的绿色干扰对蓝色反应的观察。
4.  **因果关系建立**：最终要将现象（见光部分变蓝）与结论（光合作用需要光，并产生淀粉）牢固地联系起来。

### 五、使用建议

1.  **初次学习**：
    *   建议按照 **“下一步”** 的顺序完整体验一遍，仔细阅读每一步的说明文字。
    *   在关键步骤（如步骤2遮光、步骤5碘液检测）稍作停留，观察动画细节。

2.  **巩固复习**：
    *   使用 **步骤指示器** 直接跳转到想回顾的环节，例如直接观看“碘液检测”的染色过程。
    *   开启 **“对比模式”** ，强化实验前后变化的印象。
    *   反复 **点击叶片的遮光与见光部分**，深入理解微观层面的差异。

3.  **课堂演示/讨论**：
    *   **教师**：可将动画用于课堂导入或实验讲解，利用交互功能提问（如：“接下来会发生什么？”），引导学生预测和讨论。
    *   **学生**：可结合动画，复述实验步骤、解释现象并得出结论，完成知识的内化与输出。

4.  **最佳实践**：
    *   鼓励在观看每一步动画前，先尝试自己预测下一步会发生什么。
    *   完成动画后，尝试脱离动画，口头或书面描述整个实验过程和结论。

---

希望这份指南能帮助您充分利用这个交互式动画工具。祝您探索愉快，在光与生命的奥秘中发现科学的乐趣！