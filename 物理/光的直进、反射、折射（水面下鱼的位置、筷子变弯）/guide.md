# 需求：光的直进、反射、折射（水面下鱼的位置、筷子变弯）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中或高中物理初学者，对光的基本现象有初步了解，但需要直观、动态的模型来理解抽象概念。
2.  **核心痛点**：
    *   **概念抽象**：“光路”是抽象的模型，学生难以在脑海中构建其动态变化过程。
    *   **现象与原理脱节**：知道“筷子在水里看起来弯了”、“看到的鱼比实际位置浅”，但无法与“光的折射”原理清晰关联。
    *   **缺乏探究感**：传统教学多为静态图示或口头讲解，学生被动接受，缺乏主动观察和探索的机会。
3.  **深层需求**：用户需要一个**直观、可交互、可探索**的模拟环境，能够亲手“操控”光线和观察条件，从而自主发现规律，建立从现象到原理的深刻理解。

#### 教学设计思路
1.  **核心概念**：
    *   **光的直进**：光在同种均匀介质中沿直线传播。
    *   **光的反射**：光在两种介质界面处返回原介质的现象，遵循反射定律（入射角=反射角）。
    *   **光的折射**：光从一种介质斜射入另一种介质时，传播方向发生改变的现象，遵循折射定律（定性：从光疏到光密介质，靠近法线；反之，远离法线）。
    *   **视觉错觉的形成**：人眼总是逆着进入眼睛的光线方向去寻找光源，从而对水下物体或插入水中的物体产生位置或形状的误判。

2.  **认知规律（动画结构设计）**：
    *   **从简到繁，分层呈现**：将动画分为三个循序渐进的场景，对应三个核心概念。
    *   **场景一：光的直进与反射**：作为热身和基础。展示光在空气中直进，遇到平面镜发生反射。突出显示法线、入射角、反射角，并允许用户拖拽光源改变入射角，观察反射角的实时变化。**目标**：巩固基础，引入可交互的光路概念。
    *   **场景二：光的折射**：核心教学场景。构建一个清晰的空气-水界面。允许用户拖拽水下（或水上）的光源（或物体），实时显示**实际光路**（从物体发出，经界面折射后进入人眼）和**视觉光路**（人眼逆着光线反向延长的虚线）。**目标**：清晰展示折射过程，并引出“视觉位置”与“实际位置”的差异。
    *   **场景三：经典现象解释（鱼与筷子）**：应用场景。将场景二具体化。
        *   **“看水中的鱼”**：固定一条水下真实的鱼，显示从鱼身某点发出的光线经折射进入人眼，并反向延长形成“看到的鱼”的虚像。用户可以拖动人眼（观察者）位置，观察“虚像”位置如何随之变化。
        *   **“看水中的筷子”**：展示一支筷子斜插入水中。逐点演示筷子水下部分各点发出的光经折射后进入人眼，人眼将所有反向延长线组合起来，形成一段“向上弯折”的筷子视觉图像。可以与“将筷子提出水面”的对比动画联动。
    *   **归纳与提示**：每个场景配有简洁的文字说明和引导性问题（如：“拖拽光源，你发现了什么规律？”），促进思考。

3.  **交互设计**：
    *   **直接操纵**：用户可以直接用鼠标拖拽光源、物体（鱼）、观察者（眼睛图标）、镜子角度等。
    *   **实时反馈**：任何拖拽操作都立即触发光路的重新计算和绘制，提供即时视觉反馈。
    *   **对比与切换**：提供“显示/隐藏实际光路”、“显示/隐藏视觉光路”、“显示/隐藏法线”等切换按钮。在筷子场景，提供“水中/空气中”对比按钮。
    *   **探究引导**：通过提示栏给出小任务，如“尝试让人眼移动到正上方，看看鱼的虚像在哪里？”

4.  **视觉呈现**：
    *   **介质区分**：用极浅的蓝色渐变半透明区域表示“水”，其余部分为留白或极浅灰色表示“空气”，界面清晰。
    *   **光路可视化**：
        *   **实际光路**：用带箭头的实线（如橙色）表示，箭头指示光的真实传播方向。
        *   **视觉光路**：用带箭头的虚线（如红色）表示，从人眼反向延长至虚像点。
        *   **法线**：用黑色的点划线表示。
    *   **关键元素**：
        *   **光源/物体**：用醒目的点或图标（如发光点、小鱼简笔画、筷子图形）。
        *   **人眼/观察者**：用一个简笔画眼睛图标表示。
        *   **虚像**：用半透明、轮廓与实物相同的图形（如半透明的鱼）表示。
    *   **动态效果**：光线绘制可以带有轻微的“绘制”动画效果，增强表现力。折射发生时，光线在界面处可以有一个轻微的“拐弯”动画。

#### 配色方案选择
*   **主色调**：采用**科技蓝**与**洁净白**的搭配。背景以白色或极浅灰为主，突出内容。
*   **功能色**：
    *   **空气介质**：背景白/浅灰。
    *   **水介质**：浅蓝色渐变 (`rgba(173, 216, 230, 0.2)` 到 `rgba(135, 206, 250, 0.4)`) ，确保其上的图形和线条清晰可见。
    *   **实际光路**：亮橙色 (`#FF9800`) 或明黄色 (`#FFEB3B`)，代表“光”。
    *   **视觉光路/虚像**：红色 (`#F44336`) 或品红色 (`#E91E63`)，代表“视觉错觉”，与真实光路形成鲜明对比。
    *   **法线、界面、辅助线**：深灰色 (`#607D8B`) 或黑色 (`#212121`)，保持中性。
    *   **可交互元素（光源、鱼、眼睛）**：采用饱和度较高的颜色（如蓝色 `#2196F3` 代表鱼，绿色 `#4CAF50` 代表眼睛），并添加鼠标悬停效果。
*   **文字与UI控件**：深灰色文字，控件使用主色调蓝色，保持界面清爽、专业。

#### 交互功能列表
1.  **场景选择器**：按钮或标签页，用于在“直进与反射”、“折射原理”、“鱼与筷子”三个场景间切换。
2.  **对象拖拽交互**：
    *   拖拽**点光源**改变入射光方向。
    *   拖拽**平面镜**改变镜面角度（仅限第一场景）。
    *   拖拽**水下物体（鱼）** 改变其实际位置。
    *   拖拽**观察者（眼睛图标）** 改变观察位置。
3.  **视觉元素显示控制**（复选框或按钮）：
    *   **显示/隐藏实际光路**。
    *   **显示/隐藏视觉光路（及虚像）**。
    *   **显示/隐藏法线**。
    *   **显示/隐藏角度读数**（可选，用于定量探究）。
4.  **现象对比控制**（在第三场景）：
    *   **“水中/取出”切换按钮**：用于筷子现象，一键对比筷子在水中和空气中的视觉形态。
    *   **“光线追踪”按钮**：点击后，逐步动画演示筷子水下部分多个点发出的光线如何被折射并组合成弯曲图像。
5.  **动态标注**：当用户拖拽产生关键状态（如入射角等于反射角、垂直入射时无折射）时，界面可短暂浮现文字提示（如“入射角 = 反射角”、“光沿直线进入眼睛”）。
6.  **重置按钮**：将当前场景的所有可移动元素复位到初始位置。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>光的直进、反射与折射 - 交互式教学动画</title>
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
            max-width: 900px;
        }
        
        h1 {
            color: #1a237e;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }
        
        .subtitle {
            color: #5c6bc0;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            width: 100%;
            max-width: 900px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        
        .scene-selector {
            display: flex;
            background: #f8f9fa;
            border-bottom: 1px solid #e0e0e0;
        }
        
        .scene-btn {
            flex: 1;
            padding: 15px;
            background: none;
            border: none;
            font-size: 1rem;
            font-weight: 600;
            color: #666;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
        }
        
        .scene-btn:hover {
            background-color: rgba(33, 150, 243, 0.08);
            color: #2196f3;
        }
        
        .scene-btn.active {
            color: #2196f3;
            background-color: white;
        }
        
        .scene-btn.active::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background-color: #2196f3;
        }
        
        .content-area {
            display: flex;
            flex-direction: column;
            padding: 20px;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 450px;
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid #e0e0e0;
            margin-bottom: 20px;
        }
        
        canvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 20px;
            padding: 15px;
            background-color: #f8f9fa;
            border-radius: 10px;
        }
        
        .control-group {
            display: flex;
            flex-direction: column;
            min-width: 150px;
        }
        
        .control-group h3 {
            font-size: 0.95rem;
            color: #555;
            margin-bottom: 8px;
        }
        
        .checkbox-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .checkbox-label {
            display: flex;
            align-items: center;
            cursor: pointer;
            font-size: 0.9rem;
            color: #555;
        }
        
        .checkbox-label input {
            margin-right: 6px;
            cursor: pointer;
        }
        
        .btn-group {
            display: flex;
            gap: 10px;
            align-items: flex-end;
        }
        
        button {
            padding: 8px 15px;
            background-color: #2196f3;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 0.9rem;
            transition: background-color 0.2s;
        }
        
        button:hover {
            background-color: #0d8bf2;
        }
        
        .info-panel {
            background-color: #f0f7ff;
            border-left: 4px solid #2196f3;
            padding: 15px;
            border-radius: 8px;
            margin-top: 10px;
        }
        
        .info-panel h3 {
            color: #1a237e;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }
        
        .info-panel p {
            color: #444;
            line-height: 1.5;
            font-size: 0.95rem;
        }
        
        .hint {
            color: #ff9800;
            font-weight: 600;
            margin-top: 8px;
            font-size: 0.9rem;
        }
        
        .footer {
            margin-top: 20px;
            text-align: center;
            color: #777;
            font-size: 0.9rem;
            width: 100%;
            max-width: 900px;
        }
        
        @media (max-width: 768px) {
            .container {
                border-radius: 10px;
            }
            
            .scene-btn {
                padding: 12px 8px;
                font-size: 0.9rem;
            }
            
            .canvas-container {
                height: 350px;
            }
            
            .controls {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>光的直进、反射与折射</h1>
        <p class="subtitle">交互式教学动画 - 探索光的基本性质与视觉现象</p>
    </div>
    
    <div class="container">
        <div class="scene-selector">
            <button class="scene-btn active" data-scene="1">场景一：直进与反射</button>
            <button class="scene-btn" data-scene="2">场景二：折射原理</button>
            <button class="scene-btn" data-scene="3">场景三：鱼与筷子现象</button>
        </div>
        
        <div class="content-area">
            <div class="canvas-container">
                <canvas id="mainCanvas" width="860" height="450"></canvas>
            </div>
            
            <div class="controls">
                <div class="control-group">
                    <h3>显示控制</h3>
                    <div class="checkbox-group">
                        <label class="checkbox-label">
                            <input type="checkbox" id="showActualRay" checked> 实际光路
                        </label>
                        <label class="checkbox-label">
                            <input type="checkbox" id="showVisualRay" checked> 视觉光路
                        </label>
                        <label class="checkbox-label">
                            <input type="checkbox" id="showNormal" checked> 法线
                        </label>
                        <label class="checkbox-label">
                            <input type="checkbox" id="showAngles"> 角度数值
                        </label>
                    </div>
                </div>
                
                <div class="control-group">
                    <h3>场景控制</h3>
                    <div class="btn-group">
                        <button id="resetBtn">重置场景</button>
                        <button id="traceBtn" style="display:none;">光线追踪</button>
                        <button id="compareBtn" style="display:none;">水中/空气对比</button>
                    </div>
                </div>
            </div>
            
            <div class="info-panel">
                <h3 id="sceneTitle">光的直进与反射</h3>
                <p id="sceneDescription">光在同种均匀介质中沿直线传播。当光遇到平面镜时，会发生反射，反射角等于入射角。尝试拖拽光源改变入射方向，观察反射光的变化。</p>
                <p class="hint" id="sceneHint">提示：拖拽红色光源可以改变光线方向，拖拽镜子可以改变镜面角度。</p>
            </div>
        </div>
    </div>
    
    <div class="footer">
        <p>交互式物理教学动画 | 设计原理：光的直进、反射定律、折射定律与视觉错觉</p>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('mainCanvas');
        const ctx = canvas.getContext('2d');
        
        // 场景管理
        let currentScene = 1;
        const scenes = document.querySelectorAll('.scene-btn');
        
        // 控制元素
        const showActualRay = document.getElementById('showActualRay');
        const showVisualRay = document.getElementById('showVisualRay');
        const showNormal = document.getElementById('showNormal');
        const showAngles = document.getElementById('showAngles');
        const resetBtn = document.getElementById('resetBtn');
        const traceBtn = document.getElementById('traceBtn');
        const compareBtn = document.getElementById('compareBtn');
        
        // 场景信息元素
        const sceneTitle = document.getElementById('sceneTitle');
        const sceneDescription = document.getElementById('sceneDescription');
        const sceneHint = document.getElementById('sceneHint');
        
        // 场景一：直进与反射的变量
        let lightSource1 = { x: 150, y: 225, radius: 10, isDragging: false };
        let mirror1 = { x: 430, y: 225, angle: 0, length: 120, isDragging: false };
        let reflectionPoint = { x: 430, y: 225 };
        
        // 场景二：折射原理的变量
        let waterLevel = 225;
        let lightSource2 = { x: 150, y: 150, radius: 10, isDragging: false };
        let observer2 = { x: 700, y: 150, radius: 12, isDragging: false };
        let fish2 = { x: 400, y: 350, radius: 8, isDragging: false };
        
        // 场景三：鱼与筷子现象的变量
        let fish3 = { x: 400, y: 350, radius: 12, isDragging: false };
        let observer3 = { x: 700, y: 150, radius: 12, isDragging: false };
        let chopstickAngle = 30 * Math.PI / 180;
        let showChopstickInAir = false;
        let isTracing = false;
        let traceStep = 0;
        
        // 初始化场景
        function initScene() {
            // 场景一初始化
            lightSource1 = { x: 150, y: 225, radius: 10, isDragging: false };
            mirror1 = { x: 430, y: 225, angle: 0, length: 120, isDragging: false };
            
            // 场景二初始化
            lightSource2 = { x: 150, y: 150, radius: 10, isDragging: false };
            observer2 = { x: 700, y: 150, radius: 12, isDragging: false };
            fish2 = { x: 400, y: 350, radius: 8, isDragging: false };
            
            // 场景三初始化
            fish3 = { x: 400, y: 350, radius: 12, isDragging: false };
            observer3 = { x: 700, y: 150, radius: 12, isDragging: false };
            showChopstickInAir = false;
            isTracing = false;
            traceStep = 0;
            
            updateSceneInfo();
            draw();
        }
        
        // 更新场景信息
        function updateSceneInfo() {
            switch(currentScene) {
                case 1:
                    sceneTitle.textContent = "光的直进与反射";
                    sceneDescription.textContent = "光在同种均匀介质中沿直线传播。当光遇到平面镜时，会发生反射，反射角等于入射角。尝试拖拽光源改变入射方向，观察反射光的变化。";
                    sceneHint.textContent = "提示：拖拽红色光源可以改变光线方向，拖拽镜子可以改变镜面角度。";
                    traceBtn.style.display = "none";
                    compareBtn.style.display = "none";
                    break;
                case 2:
                    sceneTitle.textContent = "光的折射原理";
                    sceneDescription.textContent = "光从一种介质斜射入另一种介质时，传播方向会发生改变，这就是折射。从空气到水（光密介质），光线会靠近法线；反之则远离法线。";
                    sceneHint.textContent = "提示：拖拽水下的小鱼或观察者（眼睛图标），观察实际光路与视觉光路的差异。";
                    traceBtn.style.display = "none";
                    compareBtn.style.display = "none";
                    break;
                case 3:
                    sceneTitle.textContent = "鱼与筷子现象";
                    sceneDescription.textContent = "人眼总是逆着进入眼睛的光线方向去寻找光源。由于光的折射，我们看到的水下物体比实际位置更浅，筷子在水面处看起来像是弯折了。";
                    sceneHint.textContent = "提示：拖拽小鱼或观察者，点击'光线追踪'查看筷子弯折的原理，点击'水中/空气对比'切换视图。";
                    traceBtn.style.display = "inline-block";
                    compareBtn.style.display = "inline-block";
                    break;
            }
        }
        
        // 绘制场景一：直进与反射
        function drawScene1() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 计算反射点
            reflectionPoint.x = mirror1.x;
            reflectionPoint.y = mirror1.y;
            
            // 计算入射角和反射角
            const mirrorNormal = { x: Math.cos(mirror1.angle + Math.PI/2), y: Math.sin(mirror1.angle + Math.PI/2) };
            const incidentVector = { x: reflectionPoint.x - lightSource1.x, y: reflectionPoint.y - lightSource1.y };
            const incidentAngle = Math.atan2(incidentVector.y, incidentVector.x) - mirror1.angle;
            const reflectionAngle = -incidentAngle;
            
            // 计算反射光线方向
            const reflectedDir = { 
                x: Math.cos(mirror1.angle + reflectionAngle), 
                y: Math.sin(mirror1.angle + reflectionAngle) 
            };
            
            // 绘制镜子
            ctx.save();
            ctx.translate(mirror1.x, mirror1.y);
            ctx.rotate(mirror1.angle);
            
            // 镜面
            ctx.fillStyle = "#e0e0e0";
            ctx.fillRect(-mirror1.length/2, -5, mirror1.length, 10);
            
            // 镜面反光效果
            ctx.fillStyle = "rgba(255, 255, 255, 0.7)";
            ctx.fillRect(-mirror1.length/2, -5, mirror1.length/2, 10);
            
            ctx.restore();
            
            // 绘制法线
            if (showNormal.checked) {
                ctx.beginPath();
                ctx.moveTo(mirror1.x, mirror1.y);
                ctx.lineTo(
                    mirror1.x + mirrorNormal.x * 60,
                    mirror1.y + mirrorNormal.y * 60
                );
                ctx.setLineDash([5, 3]);
                ctx.strokeStyle = "#607D8B";
                ctx.lineWidth = 1.5;
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 法线标签
                ctx.fillStyle = "#607D8B";
                ctx.font = "14px Arial";
                ctx.fillText("法线", mirror1.x + mirrorNormal.x * 70, mirror1.y + mirrorNormal.y * 70);
            }
            
            // 绘制入射光线（实际光路）
            if (showActualRay.checked) {
                ctx.beginPath();
                ctx.moveTo(lightSource1.x, lightSource1.y);
                ctx.lineTo(reflectionPoint.x, reflectionPoint.y);
                ctx.strokeStyle = "#FF9800";
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 入射光线箭头
                drawArrow(lightSource1.x, lightSource1.y, reflectionPoint.x, reflectionPoint.y, "#FF9800");
                
                // 入射光线标签
                ctx.fillStyle = "#FF9800";
                ctx.font = "14px Arial";
                ctx.fillText("入射光线", (lightSource1.x + reflectionPoint.x)/2 - 30, (lightSource1.y + reflectionPoint.y)/2 - 10);
            }
            
            // 绘制反射光线（实际光路）
            if (showActualRay.checked) {
                ctx.beginPath();
                ctx.moveTo(reflectionPoint.x, reflectionPoint.y);
                ctx.lineTo(
                    reflectionPoint.x + reflectedDir.x * 200,
                    reflectionPoint.y + reflectedDir.y * 200
                );
                ctx.strokeStyle = "#FF9800";
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 反射光线箭头
                drawArrow(reflectionPoint.x, reflectionPoint.y, 
                         reflectionPoint.x + reflectedDir.x * 200, 
                         reflectionPoint.y + reflectedDir.y * 200, "#FF9800");
                
                // 反射光线标签
                ctx.fillStyle = "#FF9800";
                ctx.font = "14px Arial";
                ctx.fillText("反射光线", reflectionPoint.x + reflectedDir.x * 100 - 30, 
                           reflectionPoint.y + reflectedDir.y * 100 - 10);
            }
            
            // 绘制角度
            if (showAngles.checked) {
                const angleRadius = 40;
                const incidentAngleDisplay = Math.abs(incidentAngle * 180 / Math.PI).toFixed(1);
                const reflectionAngleDisplay = Math.abs(reflectionAngle * 180 / Math.PI).toFixed(1);
                
                // 入射角弧线
                ctx.beginPath();
                ctx.arc(reflectionPoint.x, reflectionPoint.y, angleRadius, 
                       mirror1.angle + Math.PI/2, mirror1.angle + Math.PI/2 + incidentAngle, incidentAngle < 0);
                ctx.strokeStyle = "#4CAF50";
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 入射角标签
                ctx.fillStyle = "#4CAF50";
                ctx.font = "14px Arial";
                ctx.fillText(`i = ${incidentAngleDisplay}°`, 
                           reflectionPoint.x + Math.cos(mirror1.angle + Math.PI/2 + incidentAngle/2) * (angleRadius + 15),
                           reflectionPoint.y + Math.sin(mirror1.angle + Math.PI/2 + incidentAngle/2) * (angleRadius + 15));
                
                // 反射角弧线
                ctx.beginPath();
                ctx.arc(reflectionPoint.x, reflectionPoint.y, angleRadius, 
                       mirror1.angle + Math.PI/2, mirror1.angle + Math.PI/2 + reflectionAngle, reflectionAngle < 0);
                ctx.strokeStyle = "#F44336";
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 反射角标签
                ctx.fillStyle = "#F44336";
                ctx.font = "14px Arial";
                ctx.fillText(`r = ${reflectionAngleDisplay}°`, 
                           reflectionPoint.x + Math.cos(mirror1.angle + Math.PI/2 + reflectionAngle/2) * (angleRadius + 15),
                           reflectionPoint.y + Math.sin(mirror1.angle + Math.PI/2 + reflectionAngle/2) * (angleRadius + 15));
            }
            
            // 绘制光源
            drawLightSource(lightSource1.x, lightSource1.y, lightSource1.radius, "#F44336");
            
            // 绘制光源标签
            ctx.fillStyle = "#F44336";
            ctx.font = "bold 16px Arial";
            ctx.fillText("光源", lightSource1.x - 20, lightSource1.y - 15);
            
            // 绘制镜子标签
            ctx.fillStyle = "#555";
            ctx.font = "bold 16px Arial";
            ctx.fillText("平面镜", mirror1.x - 25, mirror1.y - 20);
        }
        
        // 绘制场景二：折射原理
        function drawScene2() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 绘制水面
            drawWaterSurface();
            
            // 计算折射点（光线从鱼到观察者）
            const refractionPoint = { x: fish2.x + (observer2.x - fish2.x) * (waterLevel - fish2.y) / (observer2.y - fish2.y), y: waterLevel };
            
            // 计算法线（垂直于水面）
            const normal = { x: 0, y: -1 };
            
            // 计算入射角（从水到空气）
            const incidentVector = { x: refractionPoint.x - fish2.x, y: refractionPoint.y - fish2.y };
            const incidentAngle = Math.atan2(incidentVector.y, incidentVector.x) - Math.PI/2;
            
            // 计算折射角（斯涅尔定律：n1*sinθ1 = n2*sinθ2，n_water≈1.33，n_air≈1）
            const n1 = 1.33; // 水的折射率
            const n2 = 1.0;  // 空气的折射率
            const sinRefracted = n1 * Math.sin(incidentAngle) / n2;
            const refractedAngle = Math.asin(Math.min(Math.max(sinRefracted, -1), 1));
            
            // 计算折射光线方向（从折射点到观察者）
            const refractedDir = { x: Math.sin(refractedAngle), y: -Math.cos(refractedAngle) };
            
            // 计算视觉位置（反向延长折射光线）
            const visualDistance = 100;
            const visualFish = {
                x: refractionPoint.x - refractedDir.x * visualDistance,
                y: refractionPoint.y - refractedDir.y * visualDistance
            };
            
            // 绘制实际光路（从鱼到折射点）
            if (showActualRay.checked) {
                ctx.beginPath();
                ctx.moveTo(fish2.x, fish2.y);
                ctx.lineTo(refractionPoint.x, refractionPoint.y);
                ctx.strokeStyle = "#FF9800";
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 实际光路箭头
                drawArrow(fish2.x, fish2.y, refractionPoint.x, refractionPoint.y, "#FF9800");
                
                // 水下部分标签
                ctx.fillStyle = "#FF9800";
                ctx.font = "14px Arial";
                ctx.fillText("实际光路（水下）", (fish2.x + refractionPoint.x)/2, (fish2.y + refractionPoint.y)/2 - 10);
            }
            
            // 绘制实际光路（从折射点到观察者）
            if (showActualRay.checked) {
                ctx.beginPath();
                ctx.moveTo(refractionPoint.x, refractionPoint.y);
                ctx.lineTo(observer2.x, observer2.y);
                ctx.strokeStyle = "#FF9800";
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 实际光路箭头
                drawArrow(refractionPoint.x, refractionPoint.y, observer2.x, observer2.y, "#FF9800");
                
                // 空气部分标签
                ctx.fillStyle = "#FF9800";
                ctx.font = "14px Arial";
                ctx.fillText("实际光路（空气）", (refractionPoint.x + observer2.x)/2, (refractionPoint.y + observer2.y)/2 - 10);
            }
            
            // 绘制视觉光路（从观察到视觉鱼位置）
            if (showVisualRay.checked) {
                ctx.beginPath();
                ctx.moveTo(observer2.x, observer2.y);
                ctx.lineTo(visualFish.x, visualFish.y);
                ctx.setLineDash([5, 3]);
                ctx.strokeStyle = "#F44336";
                ctx.lineWidth = 2;
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 视觉光路箭头
                drawArrow(observer2.x, observer2.y, visualFish.x, visualFish.y, "#F44336", true);
                
                // 视觉光路标签
                ctx.fillStyle = "#F44336";
                ctx.font = "14px Arial";
                ctx.fillText("视觉光路", (observer2.x + visualFish.x)/2, (observer2.y + visualFish.y)/2 - 10);
            }
            
            // 绘制法线
            if (showNormal.checked) {
                ctx.beginPath();
                ctx.moveTo(refractionPoint.x, refractionPoint.y);
                ctx.lineTo(refractionPoint.x, refractionPoint.y - 80);
                ctx.setLineDash([5, 3]);
                ctx.strokeStyle = "#607D8B";
                ctx.lineWidth = 1.5;
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 法线标签
                ctx.fillStyle = "#607D8B";
                ctx.font = "14px Arial";
                ctx.fillText("法线", refractionPoint.x + 10, refractionPoint.y - 90);
            }
            
            // 绘制角度
            if (showAngles.checked) {
                const angleRadius = 40;
                
                // 入射角弧线
                ctx.beginPath();
                ctx.arc(refractionPoint.x, refractionPoint.y, angleRadius, 
                       -Math.PI/2, -Math.PI/2 + incidentAngle, incidentAngle < 0);
                ctx.strokeStyle = "#4CAF50";
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 入射角标签
                const incidentAngleDisplay = Math.abs(incidentAngle * 180 / Math.PI).toFixed(1);
                ctx.fillStyle = "#4CAF50";
                ctx.font = "14px Arial";
                ctx.fillText(`θ₁ = ${incidentAngleDisplay}°`, 
                           refractionPoint.x + Math.cos(-Math.PI/2 + incidentAngle/2) * (angleRadius + 15),
                           refractionPoint.y + Math.sin(-Math.PI/2 + incidentAngle/2) * (angleRadius + 15));
                
                // 折射角弧线
                ctx.beginPath();
                ctx.arc(refractionPoint.x, refractionPoint.y, angleRadius, 
                       -Math.PI/2, -Math.PI/2 + refractedAngle, refractedAngle < 0);
                ctx.strokeStyle = "#2196F3";
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 折射角标签
                const refractedAngleDisplay = Math.abs(refractedAngle * 180 / Math.PI).toFixed(1);
                ctx.fillStyle = "#2196F3";
                ctx.font = "14px Arial";
                ctx.fillText(`θ₂ = ${refractedAngleDisplay}°`, 
                           refractionPoint.x + Math.cos(-Math.PI/2 + refractedAngle/2) * (angleRadius + 15),
                           refractionPoint.y + Math.sin(-Math.PI/2 + refractedAngle/2) * (angleRadius + 15));
            }
            
            // 绘制鱼（实际位置）
            drawFish(fish2.x, fish2.y, fish2.radius, "#2196F3");
            
            // 绘制视觉鱼位置（虚像）
            if (showVisualRay.checked) {
                drawFish(visualFish.x, visualFish.y, fish2.radius * 1.2, "#F44336", true);
                
                // 视觉鱼标签
                ctx.fillStyle = "#F44336";
                ctx.font = "bold 16px Arial";
                ctx.fillText("看到的鱼（虚像）", visualFish.x - 40, visualFish.y - 20);
            }
            
            // 绘制观察者
            drawObserver(observer2.x, observer2.y, observer2.radius);
            
            // 绘制实际鱼标签
            ctx.fillStyle = "#2196F3";
            ctx.font = "bold 16px Arial";
            ctx.fillText("实际的鱼", fish2.x - 30, fish2.y - 20);
            
            // 绘制观察者标签
            ctx.fillStyle = "#4CAF50";
            ctx.font = "bold 16px Arial";
            ctx.fillText("观察者", observer2.x - 25, observer2.y - 20);
        }
        
        // 绘制场景三：鱼与筷子现象
        function drawScene3() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 绘制水面
            drawWaterSurface();
            
            if (!showChopstickInAir) {
                // 绘制筷子在水中的情况
                
                // 计算折射点（光线从鱼到观察者）
                const refractionPointFish = { 
                    x: fish3.x + (observer3.x - fish3.x) * (waterLevel - fish3.y) / (observer3.y - fish3.y), 
                    y: waterLevel 
                };
                
                // 计算法线（垂直于水面）
                const normal = { x: 0, y: -1 };
                
                // 计算入射角（从水到空气）
                const incidentVectorFish = { x: refractionPointFish.x - fish3.x, y: refractionPointFish.y - fish3.y };
                const incidentAngleFish = Math.atan2(incidentVectorFish.y, incidentVectorFish.x) - Math.PI/2;
                
                // 计算折射角
                const n1 = 1.33;
                const n2 = 1.0;
                const sinRefractedFish = n1 * Math.sin(incidentAngleFish) / n2;
                const refractedAngleFish = Math.asin(Math.min(Math.max(sinRefractedFish, -1), 1));
                
                // 计算折射光线方向
                const refractedDirFish = { x: Math.sin(refractedAngleFish), y: -Math.cos(refractedAngleFish) };
                
                // 计算视觉位置
                const visualDistanceFish = 100;
                const visualFish = {
                    x: refractionPointFish.x - refractedDirFish.x * visualDistanceFish,
                    y: refractionPointFish.y - refractedDirFish.y * visualDistanceFish
                };
                
                // 绘制鱼的实际光路
                if (showActualRay.checked) {
                    ctx.beginPath();
                    ctx.moveTo(fish3.x, fish3.y);
                    ctx.lineTo(refractionPointFish.x, refractionPointFish.y);
                    ctx.lineTo(observer3.x, observer3.y);
                    ctx.strokeStyle = "#FF9800";
                    ctx.lineWidth = 3;
                    ctx.stroke();
                    
                    // 箭头
                    drawArrow(fish3.x, fish3.y, refractionPointFish.x, refractionPointFish.y, "#FF9800");
                    drawArrow(refractionPointFish.x, refractionPointFish.y, observer3.x, observer3.y, "#FF9800");
                }
                
                // 绘制鱼的视觉光路
                if (showVisualRay.checked) {
                    ctx.beginPath();
                    ctx.moveTo(observer3.x, observer3.y);
                    ctx.lineTo(visualFish.x, visualFish.y);
                    ctx.setLineDash([5, 3]);
                    ctx.strokeStyle = "#F44336";
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    ctx.setLineDash([]);
                    
                    // 箭头
                    drawArrow(observer3.x, observer3.y, visualFish.x, visualFish.y, "#F44336", true);
                }
                
                // 绘制筷子
                const chopstickTopX = 300;
                const chopstickTopY = 100;
                const chopstickBottomX = chopstickTopX + 200 * Math.sin(chopstickAngle);
                const chopstickBottomY = chopstickTopY + 200 * Math.cos(chopstickAngle);
                const chopstickWaterIntersectionX = chopstickTopX + (waterLevel - chopstickTopY) * Math.sin(chopstickAngle) / Math.cos(chopstickAngle);
                const chopstickWaterIntersectionY = waterLevel;
                
                // 绘制水上部分筷子
                ctx.beginPath();
                ctx.moveTo(chopstickTopX, chopstickTopY);
                ctx.lineTo(chopstickWaterIntersectionX, chopstickWaterIntersectionY);
                ctx.strokeStyle = "#8B4513";
                ctx.lineWidth = 8;
                ctx.stroke();
                
                // 绘制水下部分筷子（实际位置）
                ctx.beginPath();
                ctx.moveTo(chopstickWaterIntersectionX, chopstickWaterIntersectionY);
                ctx.lineTo(chopstickBottomX, chopstickBottomY);
                ctx.strokeStyle = "#8B4513";
                ctx.lineWidth = 8;
                ctx.stroke();
                
                // 绘制水下部分筷子（视觉位置 - 弯折）
                if (showVisualRay.checked) {
                    // 计算几个点的折射效果
                    const points = 5;
                    const visualPoints = [];
                    
                    for (let i = 0; i <= points; i++) {
                        const t = i / points;
                        const pointX = chopstickWaterIntersectionX + (chopstickBottomX - chopstickWaterIntersectionX) * t;
                        const pointY = chopstickWaterIntersectionY + (chopstickBottomY - chopstickWaterIntersectionY) * t;
                        
                        // 计算从该点到观察者的折射
                        const refractionPoint = { 
                            x: pointX + (observer3.x - pointX) * (waterLevel - pointY) / (observer3.y - pointY), 
                            y: waterLevel 
                        };
                        
                        const incidentVector = { x: refractionPoint.x - pointX, y: refractionPoint.y - pointY };
                        const incidentAngle = Math.atan2(incidentVector.y, incidentVector.x) - Math.PI/2;
                        const sinRefracted = n1 * Math.sin(incidentAngle) / n2;
                        const refractedAngle = Math.asin(Math.min(Math.max(sinRefracted, -1), 1));
                        const refractedDir = { x: Math.sin(refractedAngle), y: -Math.cos(refractedAngle) };
                        
                        // 计算视觉位置
                        const visualDistance = 80;
                        const visualPoint = {
                            x: refractionPoint.x - refractedDir.x * visualDistance,
                            y: refractionPoint.y - refractedDir.y * visualDistance
                        };
                        
                        visualPoints.push(visualPoint);
                        
                        // 如果正在追踪光线，绘制每个点的光路
                        if (isTracing && i <= traceStep) {
                            // 实际光路
                            ctx.beginPath();
                            ctx.moveTo(pointX, pointY);
                            ctx.lineTo(refractionPoint.x, refractionPoint.y);
                            ctx.lineTo(observer3.x, observer3.y);
                            ctx.strokeStyle = "rgba(255, 152, 0, 0.6)";
                            ctx.lineWidth = 2;
                            ctx.stroke();
                            
                            // 视觉光路
                            ctx.beginPath();
                            ctx.moveTo(observer3.x, observer3.y);
                            ctx.lineTo(visualPoint.x, visualPoint.y);
                            ctx.setLineDash([3, 2]);
                            ctx.strokeStyle = "rgba(244, 67, 54, 0.6)";
                            ctx.lineWidth = 1.5;
                            ctx.stroke();
                            ctx.setLineDash([]);
                        }
                    }
                    
                    // 绘制视觉筷子（弯折的）
                    if (!isTracing || traceStep >= points) {
                        ctx.beginPath();
                        ctx.moveTo(chopstickWaterIntersectionX, chopstickWaterIntersectionY);
                        for (let i = 0; i < visualPoints.length; i++) {
                            ctx.lineTo(visualPoints[i].x, visual
<!--检测到代码截断，自动续写中...-->
y);
                        }
                        ctx.strokeStyle = "#F44336";
                        ctx.lineWidth = 8;
                        ctx.lineCap = "round";
                        ctx.stroke();
                    }
                }
                
                // 绘制鱼（实际位置）
                drawFish(fish3.x, fish3.y, fish3.radius, "#2196F3");
                
                // 绘制视觉鱼位置（虚像）
                if (showVisualRay.checked) {
                    drawFish(visualFish.x, visualFish.y, fish3.radius * 1.2, "#F44336", true);
                }
                
                // 绘制观察者
                drawObserver(observer3.x, observer3.y, observer3.radius);
                
                // 绘制标签
                ctx.fillStyle = "#2196F3";
                ctx.font = "bold 16px Arial";
                ctx.fillText("实际的鱼", fish3.x - 30, fish3.y - 20);
                
                if (showVisualRay.checked) {
                    ctx.fillStyle = "#F44336";
                    ctx.font = "bold 16px Arial";
                    ctx.fillText("看到的鱼", visualFish.x - 30, visualFish.y - 20);
                }
                
                ctx.fillStyle = "#4CAF50";
                ctx.font = "bold 16px Arial";
                ctx.fillText("观察者", observer3.x - 25, observer3.y - 20);
                
                ctx.fillStyle = "#8B4513";
                ctx.font = "bold 16px Arial";
                ctx.fillText("筷子", chopstickTopX - 20, chopstickTopY - 10);
                
                // 绘制水面交点标记
                ctx.beginPath();
                ctx.arc(chopstickWaterIntersectionX, chopstickWaterIntersectionY, 5, 0, Math.PI * 2);
                ctx.fillStyle = "#FF5722";
                ctx.fill();
                
                ctx.fillStyle = "#FF5722";
                ctx.font = "14px Arial";
                ctx.fillText("水面交点", chopstickWaterIntersectionX + 10, chopstickWaterIntersectionY - 10);
                
            } else {
                // 绘制筷子在空气中的情况（对比）
                const chopstickTopX = 300;
                const chopstickTopY = 100;
                const chopstickBottomX = chopstickTopX + 200 * Math.sin(chopstickAngle);
                const chopstickBottomY = chopstickTopY + 200 * Math.cos(chopstickAngle);
                
                // 绘制完整的直筷子
                ctx.beginPath();
                ctx.moveTo(chopstickTopX, chopstickTopY);
                ctx.lineTo(chopstickBottomX, chopstickBottomY);
                ctx.strokeStyle = "#8B4513";
                ctx.lineWidth = 8;
                ctx.stroke();
                
                // 绘制从筷子底部到观察者的直线（空气中，无折射）
                ctx.beginPath();
                ctx.moveTo(chopstickBottomX, chopstickBottomY);
                ctx.lineTo(observer3.x, observer3.y);
                ctx.strokeStyle = "#FF9800";
                ctx.lineWidth = 3;
                ctx.stroke();
                
                drawArrow(chopstickBottomX, chopstickBottomY, observer3.x, observer3.y, "#FF9800");
                
                // 绘制标签
                ctx.fillStyle = "#8B4513";
                ctx.font = "bold 16px Arial";
                ctx.fillText("筷子（空气中）", chopstickTopX - 40, chopstickTopY - 10);
                
                ctx.fillStyle = "#4CAF50";
                ctx.font = "bold 16px Arial";
                ctx.fillText("观察者", observer3.x - 25, observer3.y - 20);
                
                // 绘制说明文字
                ctx.fillStyle = "#555";
                ctx.font = "18px Arial";
                ctx.fillText("在空气中，光沿直线传播，筷子看起来是直的", canvas.width/2 - 200, canvas.height/2);
            }
        }
        
        // 绘制背景
        function drawBackground() {
            // 绘制渐变背景
            const gradient = ctx.createLinearGradient(0, 0, 0, canvas.height);
            gradient.addColorStop(0, "#f8f9fa");
            gradient.addColorStop(1, "#e9ecef");
            ctx.fillStyle = gradient;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制网格（轻微）
            ctx.strokeStyle = "rgba(0, 0, 0, 0.05)";
            ctx.lineWidth = 0.5;
            
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
        
        // 绘制水面
        function drawWaterSurface() {
            const waterLevel = 225;
            
            // 绘制水区域
            const waterGradient = ctx.createLinearGradient(0, waterLevel, 0, canvas.height);
            waterGradient.addColorStop(0, "rgba(173, 216, 230, 0.3)");
            waterGradient.addColorStop(1, "rgba(135, 206, 250, 0.6)");
            ctx.fillStyle = waterGradient;
            ctx.fillRect(0, waterLevel, canvas.width, canvas.height - waterLevel);
            
            // 绘制水面线
            ctx.beginPath();
            ctx.moveTo(0, waterLevel);
            ctx.lineTo(canvas.width, waterLevel);
            ctx.strokeStyle = "#2196F3";
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制水面标签
            ctx.fillStyle = "#2196F3";
            ctx.font = "bold 16px Arial";
            ctx.fillText("水面", 20, waterLevel - 10);
            
            // 绘制介质标签
            ctx.fillStyle = "#555";
            ctx.font = "14px Arial";
            ctx.fillText("空气 (n≈1.0)", canvas.width - 100, waterLevel - 30);
            ctx.fillText("水 (n≈1.33)", canvas.width - 100, waterLevel + 30);
        }
        
        // 绘制光源
        function drawLightSource(x, y, radius, color) {
            // 发光效果
            const gradient = ctx.createRadialGradient(x, y, 0, x, y, radius * 2);
            gradient.addColorStop(0, color);
            gradient.addColorStop(0.7, color + "CC");
            gradient.addColorStop(1, color + "00");
            
            ctx.beginPath();
            ctx.arc(x, y, radius * 2, 0, Math.PI * 2);
            ctx.fillStyle = gradient;
            ctx.fill();
            
            // 光源核心
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.fillStyle = color;
            ctx.fill();
            
            // 光源边框
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.strokeStyle = "#333";
            ctx.lineWidth = 1.5;
            ctx.stroke();
        }
        
        // 绘制鱼
        function drawFish(x, y, radius, color, isVirtual = false) {
            ctx.save();
            ctx.translate(x, y);
            
            // 鱼身
            ctx.beginPath();
            ctx.ellipse(0, 0, radius * 1.5, radius, 0, 0, Math.PI * 2);
            
            if (isVirtual) {
                ctx.fillStyle = color + "80"; // 半透明
                ctx.setLineDash([3, 3]);
            } else {
                ctx.fillStyle = color;
            }
            
            ctx.fill();
            ctx.strokeStyle = "#333";
            ctx.lineWidth = 1;
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 鱼眼
            ctx.beginPath();
            ctx.arc(radius * 0.8, -radius * 0.3, radius * 0.3, 0, Math.PI * 2);
            ctx.fillStyle = "white";
            ctx.fill();
            
            ctx.beginPath();
            ctx.arc(radius * 0.9, -radius * 0.3, radius * 0.15, 0, Math.PI * 2);
            ctx.fillStyle = "black";
            ctx.fill();
            
            // 鱼尾
            ctx.beginPath();
            ctx.moveTo(-radius * 1.5, 0);
            ctx.lineTo(-radius * 2.5, -radius);
            ctx.lineTo(-radius * 2.5, radius);
            ctx.closePath();
            
            if (isVirtual) {
                ctx.fillStyle = color + "80";
            } else {
                ctx.fillStyle = color;
            }
            
            ctx.fill();
            ctx.strokeStyle = "#333";
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 鱼鳍
            ctx.beginPath();
            ctx.ellipse(-radius * 0.5, radius * 0.7, radius * 0.5, radius * 0.3, 0, 0, Math.PI * 2);
            
            if (isVirtual) {
                ctx.fillStyle = color + "80";
            } else {
                ctx.fillStyle = color;
            }
            
            ctx.fill();
            ctx.strokeStyle = "#333";
            ctx.lineWidth = 1;
            ctx.stroke();
            
            ctx.restore();
        }
        
        // 绘制观察者（眼睛）
        function drawObserver(x, y, radius) {
            ctx.save();
            ctx.translate(x, y);
            
            // 眼睛轮廓
            ctx.beginPath();
            ctx.arc(0, 0, radius, 0, Math.PI * 2);
            ctx.fillStyle = "#4CAF50";
            ctx.fill();
            ctx.strokeStyle = "#333";
            ctx.lineWidth = 1.5;
            ctx.stroke();
            
            // 眼球
            ctx.beginPath();
            ctx.arc(0, 0, radius * 0.7, 0, Math.PI * 2);
            ctx.fillStyle = "white";
            ctx.fill();
            
            // 瞳孔
            ctx.beginPath();
            ctx.arc(0, 0, radius * 0.4, 0, Math.PI * 2);
            ctx.fillStyle = "black";
            ctx.fill();
            
            // 高光
            ctx.beginPath();
            ctx.arc(-radius * 0.2, -radius * 0.2, radius * 0.15, 0, Math.PI * 2);
            ctx.fillStyle = "white";
            ctx.fill();
            
            // 眼睑
            ctx.beginPath();
            ctx.arc(0, -radius * 0.3, radius * 0.9, Math.PI * 0.8, Math.PI * 0.2, true);
            ctx.strokeStyle = "#333";
            ctx.lineWidth = 2;
            ctx.stroke();
            
            ctx.restore();
        }
        
        // 绘制箭头
        function drawArrow(fromX, fromY, toX, toY, color, isDashed = false) {
            const headLength = 15;
            const headAngle = Math.PI / 6;
            
            const angle = Math.atan2(toY - fromY, toX - fromX);
            
            ctx.save();
            ctx.translate(toX, toY);
            ctx.rotate(angle);
            
            if (isDashed) {
                ctx.setLineDash([5, 3]);
            }
            
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(-headLength, headLength * Math.tan(headAngle));
            ctx.moveTo(0, 0);
            ctx.lineTo(-headLength, -headLength * Math.tan(headAngle));
            
            ctx.strokeStyle = color;
            ctx.lineWidth = 3;
            ctx.lineCap = "round";
            ctx.stroke();
            
            ctx.setLineDash([]);
            ctx.restore();
        }
        
        // 主绘制函数
        function draw() {
            switch(currentScene) {
                case 1:
                    drawScene1();
                    break;
                case 2:
                    drawScene2();
                    break;
                case 3:
                    drawScene3();
                    break;
            }
        }
        
        // 检查点是否在元素内
        function isPointInCircle(x, y, circle) {
            const dx = x - circle.x;
            const dy = y - circle.y;
            return dx * dx + dy * dy <= circle.radius * circle.radius;
        }
        
        // 检查点是否在镜子附近
        function isPointNearMirror(x, y, mirror) {
            const dx = x - mirror.x;
            const dy = y - mirror.y;
            const distance = Math.sqrt(dx * dx + dy * dy);
            return distance <= 30;
        }
        
        // 获取Canvas坐标
        function getCanvasCoordinates(event) {
            const rect = canvas.getBoundingClientRect();
            const scaleX = canvas.width / rect.width;
            const scaleY = canvas.height / rect.height;
            
            return {
                x: (event.clientX - rect.left) * scaleX,
                y: (event.clientY - rect.top) * scaleY
            };
        }
        
        // 鼠标按下事件
        function handleMouseDown(event) {
            const coords = getCanvasCoordinates(event);
            
            switch(currentScene) {
                case 1:
                    if (isPointInCircle(coords.x, coords.y, lightSource1)) {
                        lightSource1.isDragging = true;
                    } else if (isPointNearMirror(coords.x, coords.y, mirror1)) {
                        mirror1.isDragging = true;
                    }
                    break;
                case 2:
                    if (isPointInCircle(coords.x, coords.y, lightSource2)) {
                        lightSource2.isDragging = true;
                    } else if (isPointInCircle(coords.x, coords.y, observer2)) {
                        observer2.isDragging = true;
                    } else if (isPointInCircle(coords.x, coords.y, fish2)) {
                        fish2.isDragging = true;
                    }
                    break;
                case 3:
                    if (isPointInCircle(coords.x, coords.y, observer3)) {
                        observer3.isDragging = true;
                    } else if (isPointInCircle(coords.x, coords.y, fish3)) {
                        fish3.isDragging = true;
                    }
                    break;
            }
            
            draw();
        }
        
        // 鼠标移动事件
        function handleMouseMove(event) {
            const coords = getCanvasCoordinates(event);
            let needsRedraw = false;
            
            switch(currentScene) {
                case 1:
                    if (lightSource1.isDragging) {
                        lightSource1.x = coords.x;
                        lightSource1.y = coords.y;
                        needsRedraw = true;
                    } else if (mirror1.isDragging) {
                        const dx = coords.x - mirror1.x;
                        const dy = coords.y - mirror1.y;
                        mirror1.angle = Math.atan2(dy, dx) - Math.PI/2;
                        needsRedraw = true;
                    }
                    break;
                case 2:
                    if (lightSource2.isDragging) {
                        lightSource2.x = Math.max(50, Math.min(coords.x, canvas.width - 50));
                        lightSource2.y = Math.max(50, Math.min(coords.y, waterLevel - 30));
                        needsRedraw = true;
                    } else if (observer2.isDragging) {
                        observer2.x = Math.max(50, Math.min(coords.x, canvas.width - 50));
                        observer2.y = Math.max(50, Math.min(coords.y, waterLevel - 30));
                        needsRedraw = true;
                    } else if (fish2.isDragging) {
                        fish2.x = Math.max(50, Math.min(coords.x, canvas.width - 50));
                        fish2.y = Math.max(waterLevel + 30, Math.min(coords.y, canvas.height - 50));
                        needsRedraw = true;
                    }
                    break;
                case 3:
                    if (observer3.isDragging) {
                        observer3.x = Math.max(50, Math.min(coords.x, canvas.width - 50));
                        observer3.y = Math.max(50, Math.min(coords.y, waterLevel - 30));
                        needsRedraw = true;
                    } else if (fish3.isDragging) {
                        fish3.x = Math.max(50, Math.min(coords.x, canvas.width - 50));
                        fish3.y = Math.max(waterLevel + 30, Math.min(coords.y, canvas.height - 50));
                        needsRedraw = true;
                    }
                    break;
            }
            
            if (needsRedraw) {
                draw();
            }
        }
        
        // 鼠标释放事件
        function handleMouseUp() {
            // 重置所有拖动状态
            lightSource1.isDragging = false;
            mirror1.isDragging = false;
            lightSource2.isDragging = false;
            observer2.isDragging = false;
            fish2.isDragging = false;
            observer3.isDragging = false;
            fish3.isDragging = false;
        }
        
        // 切换场景
        function switchScene(sceneNumber) {
            currentScene = sceneNumber;
            
            // 更新按钮状态
            scenes.forEach(btn => {
                if (parseInt(btn.dataset.scene) === sceneNumber) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            // 更新场景信息
            updateSceneInfo();
            
            // 重置追踪状态
            isTracing = false;
            traceStep = 0;
            
            // 重绘画布
            draw();
        }
        
        // 光线追踪动画
        function traceAnimation() {
            if (!isTracing) {
                isTracing = true;
                traceStep = 0;
                traceBtn.textContent = "停止追踪";
                
                const traceInterval = setInterval(() => {
                    traceStep++;
                    draw();
                    
                    if (traceStep >= 5) {
                        clearInterval(traceInterval);
                        isTracing = false;
                        traceBtn.textContent = "光线追踪";
                    }
                }, 500);
            } else {
                isTracing = false;
                traceStep = 0;
                traceBtn.textContent = "光线追踪";
                draw();
            }
        }
        
        // 事件监听器设置
        function setupEventListeners() {
            // 场景切换按钮
            scenes.forEach(btn => {
                btn.addEventListener('click', () => {
                    switchScene(parseInt(btn.dataset.scene));
                });
            });
            
            // 控制复选框
            showActualRay.addEventListener('change', draw);
            showVisualRay.addEventListener('change', draw);
            showNormal.addEventListener('change', draw);
            showAngles.addEventListener('change', draw);
            
            // 按钮
            resetBtn.addEventListener('click', initScene);
            traceBtn.addEventListener('click', traceAnimation);
            compareBtn.addEventListener('click', () => {
                showChopstickInAir = !showChopstickInAir;
                compareBtn.textContent = showChopstickInAir ? "返回水中视图" : "水中/空气对比";
                draw();
            });
            
            // 鼠标事件
            canvas.addEventListener('mousedown', handleMouseDown);
            canvas.addEventListener('mousemove', handleMouseMove);
            canvas.addEventListener('mouseup', handleMouseUp);
            canvas.addEventListener('mouseleave', handleMouseUp); // 鼠标离开画布时也释放
            
            // 触摸事件支持
            canvas.addEventListener('touchstart', (e) => {
                e.preventDefault();
                handleMouseDown(e.touches[0]);
            });
            
            canvas.addEventListener('touchmove', (e) => {
                e.preventDefault();
                handleMouseMove(e.touches[0]);
            });
            
            canvas.addEventListener('touchend', (e) => {
                e.preventDefault();
                handleMouseUp();
            });
        }
        
        // 初始化
        function init() {
            setupEventListeners();
            initScene();
            
            // 初始绘制
            draw();
            
            // 窗口大小调整时重新绘制
            window.addEventListener('resize', () => {
                // 更新Canvas尺寸
                const container = canvas.parentElement;
                canvas.width = container.clientWidth;
                canvas.height = container.clientHeight;
                draw();
            });
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 《光的直进、反射与折射》交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过直观、动态的可视化方式，帮助您深入理解光的基本性质及其产生的有趣现象。请跟随本指南，开启您的探索之旅。

---

### 一、 功能说明

本动画包含三个精心设计的教学场景，层层递进，从基本原理到实际应用：

1.  **场景一：光的直进与反射**
    *   **目标**：理解光在同种介质中的直线传播特性，掌握反射定律（入射角等于反射角）。
    *   **核心交互**：拖拽光源改变入射方向，拖拽镜子改变镜面角度，实时观察光路变化。

2.  **场景二：光的折射原理**
    *   **目标**：理解光从一种介质进入另一种介质时发生的折射现象，定性掌握折射规律（光从空气进入水，靠近法线；反之，远离法线）。
    *   **核心交互**：拖拽水下的“鱼”或空气中的“观察者”，观察实际光路与视觉光路的分离，理解“虚像”的形成原理。

3.  **场景三：鱼与筷子现象**
    *   **目标**：运用折射原理解释两个经典的生活现象——“为什么看到的鱼比实际位置浅”和“为什么筷子在水里看起来变弯了”。
    *   **核心交互**：拖拽元素观察现象，使用“光线追踪”功能分解筷子弯折过程，使用“对比”功能直观比较水中与空气中的视觉差异。

---

### 二、 主要功能与操作

*   **场景切换**：点击顶部的场景标签（场景一、场景二、场景三），可在不同教学内容间自由切换。
*   **对象拖拽**：在每个场景中，您可以用鼠标直接拖拽高亮显示的元素（如**红色光源**、**镜子**、**蓝色小鱼**、**绿色眼睛图标**），所有光路将实时更新。
*   **显示控制**：利用左侧的复选框，可以随时：
    *   **显示/隐藏实际光路**（橙色实线）：展示光的真实传播路径。
    *   **显示/隐藏视觉光路**（红色虚线）：展示人眼感知的路径，即“看到的”光线方向。
    *   **显示/隐藏法线**（灰色点划线）：辅助理解角度关系。
    *   **显示/隐藏角度数值**：定量查看入射角、反射角或折射角的大小。
*   **特殊功能按钮**：
    *   **重置场景**：将当前场景的所有可移动物体恢复至初始位置。
    *   **光线追踪**（场景三）：逐步动画演示筷子水下部分多个点发出的光线如何折射，最终组合成弯曲的视觉图像。
    *   **水中/空气对比**（场景三）：一键切换，对比筷子在水中“变弯”和在空气中“笔直”的视觉形态。
*   **信息面板**：底部面板实时显示当前场景的学习目标、原理说明和操作提示，引导您的探索。

---

### 三、 设计特色

1.  **双光路可视化**：独创性地同时显示“实际光路”与“视觉光路”，将抽象的折射原理与具体的视觉错觉直接关联，破解学习难点。
2.  **即时反馈的交互**：所有操作均得到实时图形响应，营造“动手实验”的沉浸感，让规律发现于指尖。
3.  **分层教学设计**：结构遵循认知规律，从简单反射到复杂折射，再到现象解释，循序渐进，构建完整知识体系。
4.  **专业美学设计**：采用清晰的色彩编码（橙色代表光，红色代表视觉错觉，蓝色代表水），界面简洁美观，聚焦核心内容。
5.  **探究式学习引导**：通过提示语和功能设计，鼓励用户主动提问（“如果……会怎样？”）并自行验证，培养科学探究思维。

---

### 四、 教学要点与探究问题

**场景一：**
*   **探究**：当入射光线垂直射向镜面时，反射光线会怎样？这时的入射角和反射角是多少？
*   **验证**：拖拽镜子旋转，反射定律是否始终成立？

**场景二：**
*   **核心发现**：观察“实际的鱼”与“看到的鱼”的位置差异。**虚像总是比实物更靠近水面吗？**
*   **深入探究**：拖拽观察者到鱼的正上方，此时光路有什么特点？看到的鱼在哪里？
*   **规律总结**：尝试让光线从水斜射入空气（拖拽鱼到左上角），观察折射光线是靠近还是远离法线？

**场景三：**
*   **解释现象**：启动“光线追踪”功能，仔细观察为什么筷子的水下部分看起来会向上弯折。
*   **对比思考**：使用“对比”功能，理解折射是产生这一错觉的根本原因。
*   **迁移应用**：你能用本场景学到的原理，解释“游泳池看起来比实际浅”的原因吗？

---

### 五、 使用建议

1.  **对于学生（自学者）**：
    *   **建议流程**：按场景顺序操作，每个场景先阅读说明，然后大胆拖拽、尝试，最后回答面板中的提示问题。
    *   **高效学习**：善用“显示控制”功能。例如，在场景二，可以先隐藏视觉光路，只关注实际光路如何折射；然后再打开视觉光路，理解错觉产生。
    *   **记录与反思**：将你的发现（如角度关系、位置变化）记录下来，尝试用自己的话解释每个现象。

2.  **对于教师（教学者）**：
    *   **课堂演示**：可用于导入新课或讲解重难点，用大屏幕展示动态光路，提问引导学生预测结果。
    *   **设计探究任务**：可布置具体的探究任务单，例如：“请设计一个操作，让看到的鱼位于实际鱼的左上方，并截图说明。”
    *   **突破教学难点**：重点利用场景三的“光线追踪”功能，化解“筷子变弯”这一传统教学中的抽象难点。

3.  **通用建议**：
    *   不要害怕“破坏”初始画面，拖拽是学习的一部分。
    *   结合生活中的实际观察（如碗底的硬币、水中的腿）来使用本动画，理论联系实际。
    *   如果遇到困惑，点击“重置场景”回到起点，重新开始探索。

---

**让我们开始吧！点击第一个场景，移动光源，亲自验证光的反射定律，感受交互式学习的魅力！**