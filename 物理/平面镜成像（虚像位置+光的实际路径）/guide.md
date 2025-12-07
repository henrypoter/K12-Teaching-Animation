# 需求：平面镜成像（虚像位置+光的实际路径）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中物理初学者，可能对光的反射、虚像等抽象概念感到困惑。
2.  **核心痛点**：
    *   **概念抽象**：学生难以理解为什么“虚像”在镜子后面，以及为什么“光路”是理解虚像位置的关键。
    *   **路径与感知分离**：学生容易混淆“光实际走的路径”和“我们眼睛/大脑感知到的像的位置”。
    *   **静态图的局限**：传统教材中的静态光路图无法动态展示光的传播和眼睛的追踪过程。
3.  **学习目标**：通过动画，学生应能：
    *   清晰地描述平面镜成像时，光的实际反射路径。
    *   解释虚像的形成原理（反射光线的反向延长线相交）。
    *   准确指出虚像的位置（与物关于镜面对称），并理解其“虚”的本质（无实际光线到达）。
    *   建立“光路可逆”的直观感受。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念分解与串联**：
    *   **第一层：现象**。展示物体（如一支蜡烛）在平面镜中成“像”。
    *   **第二层：原理（光路）**。揭示现象背后的原因：从物体发出的光经平面镜**反射**进入人眼。
    *   **第三层：错觉（虚像）**。展示人眼和大脑如何根据**沿直线传播**的入射习惯，将反射光线反向延长，从而在镜后“看到”一个像。强调“反向延长线”是理解虚像位置的关键工具。
    *   **第四层：规律（对称）**。通过光路几何推导出“物像关于镜面对称”、“等大、等距”的规律。

2.  **遵循认知规律**：
    *   **从具体到抽象**：先看完整的成像效果，再分解展示光路。
    *   **从整体到局部**：先展示所有光线的整体效果，再允许用户控制单条光线，观察其路径与反向延长线。
    *   **多感官与交互**：用视觉动画呈现过程，用交互控制探索细节，用简洁文字和符号（如箭头、虚线）进行标注，强化理解。

3.  **交互设计**：
    *   **阶段性揭示**：动画将分步骤进行，每一步有明确的标题和简短说明。
    *   **可控元素**：用户可拖动物体，实时观察虚像位置和光路的变化。可点击按钮控制是否显示“实际光线”、“反向延长线”、“虚像”。
    *   **关键点强调**：当光线射入眼睛时，眼睛可以有一个“高亮”或“闪烁”反馈，模拟接收光信号。反向延长线相交于虚像点时，该点应明显标出。

4.  **视觉呈现**：
    *   **主场景**：一个简洁的实验室或房间背景，中央放置一个垂直的平面镜（用一条有厚度的线段表示镜面和镜背）。
    *   **核心元素**：
        *   **物体**：一个色彩鲜明、形状简单的物体（如红色箭头或蜡烛），方便区分。
        *   **光线**：
            *   **实际光线**：用**实线箭头**表示，从物体发出，经镜面反射至眼睛。
            *   **反向延长线**：用**虚线箭头**表示，从眼睛处的反射光线**反向**画出，在镜后相交。
        *   **虚像**：用与物体相同但**半透明**的图形表示，位于镜后。
        *   **眼睛/观察者**：一个简笔画风格的眼睛图标，可以移动。
    *   **动态效果**：光线以适中的速度沿路径传播，像“画”出来一样。反向延长线在光线到达眼睛后自动画出。

#### 配色方案选择
*   **背景**：浅灰色或淡蓝色，确保中性、不分散注意力。
*   **平面镜**：深灰色镜框，浅灰色（带轻微渐变）镜面，以区分正反面。
*   **物体**：**亮红色**。高饱和度，易于聚焦。
*   **实际光线**：**亮黄色**（代表光）。在较暗背景下非常醒目。
*   **反向延长线**：**蓝色虚线**。与实线光路明确区分，蓝色常与“辅助线”、“虚拟”概念关联。
*   **虚像**：**半透明的红色**（与物体同色但透明），直观体现其“虚”的特性。
*   **眼睛/观察者**：黑色简笔画。
*   **界面控件**：中性色的按钮（如浅蓝色），文字为深灰色或黑色。
*   **文本与标注**：深灰色，清晰易读。

#### 交互功能列表
1.  **步骤控制区**：
    *   “第一步：观察成像” - 只显示物体、镜子和虚像。
    *   “第二步：显示光路” - 动画展示从物体到眼睛的两条典型光线。
    *   “第三步：揭示虚像原理” - 显示反射光线的反向延长线及其在镜后的交点。
    *   “第四步：总结规律” - 显示物、像对称的辅助线。
    *   “重置”按钮：回到初始状态。

2.  **显示/隐藏开关**（复选框或按钮）：
    *   `[✓] 显示实际光线`
    *   `[✓] 显示反向延长线`
    *   `[✓] 显示虚像`
    *   `[ ] 显示辅助对称线`（连接物点与像点的虚线，垂直于镜面）

3.  **拖拽交互**：
    *   可**拖动物体**，虚像位置、所有光线和延长线实时更新。
    *   可**拖动眼睛**，观察从不同角度观看时，光路和反向延长线的变化，理解“虚像位置固定，但观察视角影响进入眼睛的光线”。

4.  **单束光模式**（可选高级功能）：
    *   一个按钮“追踪一束光”。启用后，用户点击物体上某点，只生成从该点发出并经镜面反射至眼睛的一束光及其反向延长线，帮助理解“点对应点”的成像原理。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>平面镜成像原理 - 虚像与光路</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
            color: #333;
        }
        
        .header {
            text-align: center;
            margin-bottom: 20px;
            width: 100%;
            max-width: 900px;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }
        
        .subtitle {
            color: #34495e;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            max-width: 900px;
            width: 100%;
            justify-content: center;
        }
        
        .canvas-container {
            flex: 1;
            min-width: 500px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            overflow: hidden;
            padding: 15px;
            display: flex;
            flex-direction: column;
        }
        
        #animationCanvas {
            flex: 1;
            background-color: #f8f9fa;
            border-radius: 8px;
            border: 1px solid #ddd;
            cursor: move;
        }
        
        .controls-container {
            width: 300px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            padding: 20px;
            display: flex;
            flex-direction: column;
        }
        
        .section-title {
            color: #2c3e50;
            font-size: 1.3rem;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #3498db;
        }
        
        .steps-control {
            margin-bottom: 25px;
        }
        
        .step-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .step-btn {
            flex: 1;
            min-width: 120px;
            padding: 10px 12px;
            background-color: #ecf0f1;
            border: none;
            border-radius: 6px;
            color: #2c3e50;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.2s ease;
        }
        
        .step-btn:hover {
            background-color: #d5dbdb;
            transform: translateY(-2px);
        }
        
        .step-btn.active {
            background-color: #3498db;
            color: white;
            box-shadow: 0 4px 8px rgba(52, 152, 219, 0.3);
        }
        
        .step-description {
            background-color: #f8f9fa;
            padding: 12px;
            border-radius: 6px;
            border-left: 4px solid #3498db;
            font-size: 0.95rem;
            line-height: 1.5;
            color: #34495e;
        }
        
        .display-controls {
            margin-bottom: 25px;
        }
        
        .control-group {
            margin-bottom: 15px;
        }
        
        .control-label {
            display: flex;
            align-items: center;
            margin-bottom: 8px;
            cursor: pointer;
            font-weight: 500;
            color: #2c3e50;
        }
        
        .control-label input {
            margin-right: 10px;
            width: 18px;
            height: 18px;
            cursor: pointer;
        }
        
        .slider-group {
            margin-bottom: 15px;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
            font-weight: 500;
            color: #2c3e50;
        }
        
        .slider-value {
            color: #3498db;
            font-weight: 600;
        }
        
        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: #ecf0f1;
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
        
        .drag-controls {
            margin-top: auto;
            padding-top: 15px;
            border-top: 1px solid #eee;
        }
        
        .drag-hint {
            display: flex;
            align-items: center;
            background-color: #f8f9fa;
            padding: 10px;
            border-radius: 6px;
            margin-bottom: 15px;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        .drag-hint svg {
            margin-right: 10px;
            color: #3498db;
        }
        
        .reset-btn {
            width: 100%;
            padding: 12px;
            background-color: #e74c3c;
            color: white;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.2s ease;
            margin-top: 10px;
        }
        
        .reset-btn:hover {
            background-color: #c0392b;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(231, 76, 60, 0.3);
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding: 15px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            max-width: 900px;
            width: 100%;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            margin-right: 20px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            margin-right: 8px;
            border-radius: 3px;
        }
        
        .legend-text {
            font-size: 0.9rem;
            color: #2c3e50;
        }
        
        @media (max-width: 850px) {
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
        <h1>平面镜成像原理</h1>
        <p class="subtitle">探索虚像位置与光的实际路径 - 交互式教学动画</p>
    </div>
    
    <div class="container">
        <div class="canvas-container">
            <canvas id="animationCanvas" width="800" height="500"></canvas>
        </div>
        
        <div class="controls-container">
            <div class="steps-control">
                <h3 class="section-title">学习步骤</h3>
                <div class="step-buttons">
                    <button class="step-btn active" data-step="1">1. 观察成像</button>
                    <button class="step-btn" data-step="2">2. 显示光路</button>
                    <button class="step-btn" data-step="3">3. 虚像原理</button>
                    <button class="step-btn" data-step="4">4. 总结规律</button>
                </div>
                <div class="step-description" id="stepDescription">
                    观察平面镜成像现象。注意物体与虚像的大小、形状关系。
                </div>
            </div>
            
            <div class="display-controls">
                <h3 class="section-title">显示控制</h3>
                
                <div class="control-group">
                    <label class="control-label">
                        <input type="checkbox" id="showLightRays" checked>
                        <span>显示实际光线（黄色实线）</span>
                    </label>
                </div>
                
                <div class="control-group">
                    <label class="control-label">
                        <input type="checkbox" id="showExtensions" checked>
                        <span>显示反向延长线（蓝色虚线）</span>
                    </label>
                </div>
                
                <div class="control-group">
                    <label class="control-label">
                        <input type="checkbox" id="showVirtualImage" checked>
                        <span>显示虚像（半透明红色）</span>
                    </label>
                </div>
                
                <div class="control-group">
                    <label class="control-label">
                        <input type="checkbox" id="showSymmetryLines">
                        <span>显示对称辅助线（灰色虚线）</span>
                    </label>
                </div>
                
                <div class="slider-group">
                    <div class="slider-label">
                        <span>光线速度</span>
                        <span class="slider-value" id="speedValue">中速</span>
                    </div>
                    <input type="range" id="lightSpeed" min="1" max="10" value="5">
                </div>
            </div>
            
            <div class="drag-controls">
                <h3 class="section-title">交互控制</h3>
                
                <div class="drag-hint">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M3 3v7h7V3H3zM14 3v7h7V3h-7zM3 14v7h7v-7H3zM14 14v7h7v-7h-7z"/>
                    </svg>
                    拖拽物体或眼睛改变位置，观察光路和虚像的变化
                </div>
                
                <button class="reset-btn" id="resetBtn">重置动画</button>
            </div>
        </div>
    </div>
    
    <div class="legend">
        <div class="legend-item">
            <div class="legend-color" style="background-color: #e74c3c;"></div>
            <div class="legend-text">物体（可拖拽）</div>
        </div>
        <div class="legend-item">
            <div class="legend-color" style="background-color: rgba(231, 76, 60, 0.5);"></div>
            <div class="legend-text">虚像（半透明）</div>
        </div>
        <div class="legend-item">
            <div class="legend-color" style="background-color: #f1c40f;"></div>
            <div class="legend-text">实际光线（黄色实线）</div>
        </div>
        <div class="legend-item">
            <div class="legend-color" style="background-color: #3498db; border: 1px dashed #3498db;"></div>
            <div class="legend-text">反向延长线（蓝色虚线）</div>
        </div>
        <div class="legend-item">
            <div class="legend-color" style="background-color: #95a5a6; border: 1px dashed #95a5a6;"></div>
            <div class="legend-text">对称辅助线（灰色虚线）</div>
        </div>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 调整Canvas大小以适应容器
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            draw();
        }
        
        // 初始调整大小
        window.addEventListener('load', resizeCanvas);
        window.addEventListener('resize', resizeCanvas);
        
        // 动画状态
        let currentStep = 1;
        let animationProgress = 0;
        let animationDirection = 1;
        let lastTime = 0;
        const animationSpeed = 0.02;
        
        // 显示控制
        let showLightRays = true;
        let showExtensions = true;
        let showVirtualImage = true;
        let showSymmetryLines = false;
        let lightSpeed = 5;
        
        // 元素位置
        let mirror = {
            x: canvas.width * 0.5,
            y: canvas.height * 0.5,
            width: 10,
            height: 300
        };
        
        let object = {
            x: canvas.width * 0.3,
            y: canvas.height * 0.5,
            radius: 25,
            color: '#e74c3c',
            isDragging: false
        };
        
        let eye = {
            x: canvas.width * 0.8,
            y: canvas.height * 0.3,
            radius: 20,
            isDragging: false
        };
        
        // 计算虚像位置（关于镜面对称）
        function calculateVirtualImage() {
            const mirrorCenterX = mirror.x;
            const distanceFromMirror = mirrorCenterX - object.x;
            return {
                x: mirrorCenterX + distanceFromMirror,
                y: object.y,
                radius: object.radius,
                color: 'rgba(231, 76, 60, 0.5)'
            };
        }
        
        // 计算光线路径
        function calculateLightPaths() {
            const virtualImage = calculateVirtualImage();
            
            // 物体上的两个点（用于发射光线）
            const objectTop = { x: object.x, y: object.y - object.radius * 0.7 };
            const objectBottom = { x: object.x, y: object.y + object.radius * 0.7 };
            
            // 计算光线在镜面上的反射点
            // 使用虚像法：从眼睛到虚像的连线与镜面的交点
            const mirrorTopY = mirror.y - mirror.height/2;
            const mirrorBottomY = mirror.y + mirror.height/2;
            
            // 第一条光线（从物体顶部）
            const reflectionPoint1 = {
                x: mirror.x,
                y: mirrorTopY + (mirrorBottomY - mirrorTopY) * 0.3
            };
            
            // 第二条光线（从物体底部）
            const reflectionPoint2 = {
                x: mirror.x,
                y: mirrorTopY + (mirrorBottomY - mirrorTopY) * 0.7
            };
            
            return {
                ray1: {
                    from: objectTop,
                    toMirror: reflectionPoint1,
                    toEye: eye
                },
                ray2: {
                    from: objectBottom,
                    toMirror: reflectionPoint2,
                    toEye: eye
                }
            };
        }
        
        // 绘制平面镜
        function drawMirror() {
            // 镜面
            ctx.fillStyle = '#bdc3c7';
            ctx.fillRect(mirror.x - mirror.width/2, mirror.y - mirror.height/2, mirror.width, mirror.height);
            
            // 镜框
            ctx.fillStyle = '#7f8c8d';
            ctx.fillRect(mirror.x - mirror.width/2 - 3, mirror.y - mirror.height/2 - 3, mirror.width + 6, 3);
            ctx.fillRect(mirror.x - mirror.width/2 - 3, mirror.y + mirror.height/2, mirror.width + 6, 3);
            ctx.fillRect(mirror.x - mirror.width/2 - 3, mirror.y - mirror.height/2, 3, mirror.height);
            ctx.fillRect(mirror.x + mirror.width/2, mirror.y - mirror.height/2, 3, mirror.height);
            
            // 镜面反射效果
            const gradient = ctx.createLinearGradient(mirror.x - mirror.width/2, 0, mirror.x + mirror.width/2, 0);
            gradient.addColorStop(0, 'rgba(255, 255, 255, 0.1)');
            gradient.addColorStop(0.5, 'rgba(255, 255, 255, 0.3)');
            gradient.addColorStop(1, 'rgba(255, 255, 255, 0.1)');
            ctx.fillStyle = gradient;
            ctx.fillRect(mirror.x - mirror.width/2, mirror.y - mirror.height/2, mirror.width, mirror.height);
        }
        
        // 绘制物体
        function drawObject() {
            // 物体主体
            ctx.fillStyle = object.color;
            ctx.beginPath();
            ctx.arc(object.x, object.y, object.radius, 0, Math.PI * 2);
            ctx.fill();
            
            // 物体高光
            ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
            ctx.beginPath();
            ctx.arc(object.x - object.radius * 0.3, object.y - object.radius * 0.3, object.radius * 0.4, 0, Math.PI * 2);
            ctx.fill();
            
            // 物体标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('物体', object.x, object.y);
            
            // 如果正在拖拽，显示拖拽效果
            if (object.isDragging) {
                ctx.strokeStyle = 'rgba(52, 152, 219, 0.7)';
                ctx.lineWidth = 3;
                ctx.setLineDash([5, 5]);
                ctx.beginPath();
                ctx.arc(object.x, object.y, object.radius + 5, 0, Math.PI * 2);
                ctx.stroke();
                ctx.setLineDash([]);
            }
        }
        
        // 绘制眼睛
        function drawEye() {
            // 眼睛轮廓
            ctx.fillStyle = '#2c3e50';
            ctx.beginPath();
            ctx.arc(eye.x, eye.y, eye.radius, 0, Math.PI * 2);
            ctx.fill();
            
            // 眼白
            ctx.fillStyle = 'white';
            ctx.beginPath();
            ctx.arc(eye.x, eye.y, eye.radius * 0.7, 0, Math.PI * 2);
            ctx.fill();
            
            // 瞳孔
            ctx.fillStyle = '#3498db';
            ctx.beginPath();
            ctx.arc(eye.x, eye.y, eye.radius * 0.4, 0, Math.PI * 2);
            ctx.fill();
            
            // 高光
            ctx.fillStyle = 'white';
            ctx.beginPath();
            ctx.arc(eye.x - eye.radius * 0.15, eye.y - eye.radius * 0.15, eye.radius * 0.1, 0, Math.PI * 2);
            ctx.fill();
            
            // 眼睛标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('眼睛', eye.x, eye.y + eye.radius + 20);
            
            // 如果正在拖拽，显示拖拽效果
            if (eye.isDragging) {
                ctx.strokeStyle = 'rgba(52, 152, 219, 0.7)';
                ctx.lineWidth = 3;
                ctx.setLineDash([5, 5]);
                ctx.beginPath();
                ctx.arc(eye.x, eye.y, eye.radius + 5, 0, Math.PI * 2);
                ctx.stroke();
                ctx.setLineDash([]);
            }
        }
        
        // 绘制虚像
        function drawVirtualImage() {
            if (!showVirtualImage && currentStep < 3) return;
            
            const virtualImage = calculateVirtualImage();
            
            // 虚像主体（半透明）
            ctx.fillStyle = virtualImage.color;
            ctx.beginPath();
            ctx.arc(virtualImage.x, virtualImage.y, virtualImage.radius, 0, Math.PI * 2);
            ctx.fill();
            
            // 虚像标签
            ctx.fillStyle = 'rgba(44, 62, 80, 0.7)';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('虚像', virtualImage.x, virtualImage.y);
            
            // 虚像说明文字
            if (currentStep >= 3) {
                ctx.fillStyle = '#e74c3c';
                ctx.font = 'italic 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('(无实际光线到达)', virtualImage.x, virtualImage.y + virtualImage.radius + 20);
            }
        }
        
        // 绘制光线
        function drawLightRays() {
            if (!showLightRays && currentStep < 2) return;
            
            const lightPaths = calculateLightPaths();
            const progress = currentStep >= 2 ? animationProgress : 0;
            const speedFactor = lightSpeed / 5;
            
            // 绘制第一条光线
            drawRay(
                lightPaths.ray1.from, 
                lightPaths.ray1.toMirror, 
                lightPaths.ray1.toEye, 
                progress, 
                speedFactor,
                0
            );
            
            // 绘制第二条光线
            drawRay(
                lightPaths.ray2.from, 
                lightPaths.ray2.toMirror, 
                lightPaths.ray2.toEye, 
                progress, 
                speedFactor,
                0.3
            );
        }
        
        // 绘制单条光线
        function drawRay(from, toMirror, toEye, progress, speedFactor, delay) {
            const adjustedProgress = Math.max(0, (progress - delay) / (1 - delay));
            
            if (adjustedProgress <= 0) return;
            
            // 实际光线（黄色实线）
            if (showLightRays && currentStep >= 2) {
                ctx.strokeStyle = '#f1c40f';
                ctx.lineWidth = 3;
                ctx.lineCap = 'round';
                
                // 从物体到镜面的部分
                const mirrorProgress = Math.min(1, adjustedProgress * 2);
                const mirrorX = from.x + (toMirror.x - from.x) * mirrorProgress;
                const mirrorY = from.y + (toMirror.y - from.y) * mirrorProgress;
                
                ctx.beginPath();
                ctx.moveTo(from.x, from.y);
                ctx.lineTo(mirrorX, mirrorY);
                ctx.stroke();
                
                // 绘制光线箭头（在镜面处）
                if (mirrorProgress >= 0.5 && mirrorProgress < 1) {
                    drawArrow(mirrorX, mirrorY, toMirror.x - from.x, toMirror.y - from.y, '#f1c40f');
                }
                
                // 从镜面到眼睛的部分
                if (adjustedProgress > 0.5) {
                    const eyeProgress = (adjustedProgress - 0.5) * 2;
                    const eyeX = toMirror.x + (toEye.x - toMirror.x) * eyeProgress;
                    const eyeY = toMirror.y + (toEye.y - toMirror.y) * eyeProgress;
                    
                    ctx.beginPath();
                    ctx.moveTo(toMirror.x, toMirror.y);
                    ctx.lineTo(eyeX, eyeY);
                    ctx.stroke();
                    
                    // 绘制光线箭头（在眼睛处）
                    if (eyeProgress >= 0.7) {
                        drawArrow(eyeX, eyeY, toEye.x - toMirror.x, toEye.y - toMirror.y, '#f1c40f');
                    }
                }
            }
            
            // 反向延长线（蓝色虚线）
            if (showExtensions && currentStep >= 3 && adjustedProgress > 0.5) {
                const virtualImage = calculateVirtualImage();
                const eyeProgress = (adjustedProgress - 0.5) * 2;
                
                ctx.strokeStyle = '#3498db';
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 5]);
                ctx.lineCap = 'round';
                
                // 从眼睛反向延长到虚像
                const extensionProgress = Math.min(1, eyeProgress * 1.5);
                const extensionX = toEye.x + (virtualImage.x - toEye.x) * extensionProgress;
                const extensionY = toEye.y + (virtualImage.y - toEye.y) * extensionProgress;
                
                ctx.beginPath();
                ctx.moveTo(toEye.x, toEye.y);
                ctx.lineTo(extensionX, extensionY);
                ctx.stroke();
                
                // 绘制延长线箭头
                if (extensionProgress >= 0.7) {
                    drawArrow(extensionX, extensionY, virtualImage.x - toEye.x, virtualImage.y - toEye.y, '#3498db');
                }
                
                ctx.setLineDash([]);
            }
        }
        
        // 绘制箭头
        function drawArrow(x, y, dx, dy, color) {
            const angle = Math.atan2(dy, dx);
            const arrowLength = 15;
            
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(angle);
            ctx.fillStyle = color;
            
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(-arrowLength, arrowLength/2);
            ctx.lineTo(-arrowLength, -arrowLength/2);
            ctx.closePath();
            ctx.fill();
            
            ctx.restore();
        }
        
        // 绘制对称辅助线
        function drawSymmetryLines() {
            if (!showSymmetryLines && currentStep < 4) return;
            
            const virtualImage = calculateVirtualImage();
            
            ctx.strokeStyle = '#95a5a6';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            
            // 物体到虚像的连线
            ctx.beginPath();
            ctx.moveTo(object.x, object.y);
            ctx.lineTo(virtualImage.x, virtualImage.y);
            ctx.stroke();
            
            // 镜面的垂直线（对称轴）
            ctx.beginPath();
            ctx.moveTo(mirror.x, mirror.y - mirror.height/2);
            ctx.lineTo(mirror.x, mirror.y + mirror.height/2);
            ctx.stroke();
            
            // 物体到镜面的垂线
            ctx.beginPath();
            ctx.moveTo(object.x, object.y);
            ctx.lineTo(mirror.x, object.y);
            ctx.stroke();
            
            // 虚像到镜面的垂线
            ctx.beginPath();
            ctx.moveTo(virtualImage.x, virtualImage.y);
            ctx.lineTo(mirror.x, virtualImage.y);
            ctx.stroke();
            
            ctx.setLineDash([]);
            
            // 标记距离相等
            if (currentStep >= 4) {
                const distance = Math.abs(mirror.x - object.x);
                const midY = object.y;
                
                ctx.fillStyle = '#2c3e50';
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                
                // 物体到镜面的距离
                ctx.fillText(`d = ${Math.round(distance)}px`, (object.x + mirror.x) / 2, midY - 10);
                
                // 虚像到镜面的距离
                ctx.fillText(`d = ${Math.round(distance)}px`, (virtualImage.x + mirror.x) / 2, midY - 10);
                
                // 对称标记
                ctx.fillText('对称轴', mirror.x, mirror.y - mirror.height/2 - 10);
            }
        }
        
        // 绘制步骤说明
        function drawStepInfo() {
            const stepTexts = [
                "第一步：观察成像现象。注意物体与虚像的大小、形状相同。",
                "第二步：显示实际光路。光线从物体发出，经平面镜反射后进入眼睛。",
                "第三步：揭示虚像原理。眼睛沿直线追溯光线来源，反向延长线在镜后相交形成虚像。",
                "第四步：总结规律。物像关于镜面对称，等大、等距，虚像无实际光线到达。"
            ];
            
            ctx.fillStyle = 'rgba(44, 62, 80, 0.9)';
            ctx.font = '16px Arial';
            ctx.textAlign = 'left';
            ctx.textBaseline = 'top';
            
            // 绘制背景框
            ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
            ctx.fillRect(20, 20, canvas.width - 40, 60);
            
            ctx.strokeStyle = '#3498db';
            ctx.lineWidth = 2;
            ctx.strokeRect(20, 20, canvas.width - 40, 60);
            
            // 绘制步骤文本
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 18px Arial';
            ctx.fillText(`步骤 ${currentStep}/4`, 30, 30);
            
            ctx.font = '16px Arial';
            const lines = wrapText(stepTexts[currentStep-1], canvas.width - 80);
            lines.forEach((line, index) => {
                ctx.fillText(line, 30, 55 + index * 20);
            });
        }
        
        // 文本换行函数
        function wrapText(text, maxWidth) {
            const words = text.split(' ');
            const lines = [];
            let currentLine = words[0];
            
            for (let i = 1; i < words.length; i++) {
                const word = words[i];
                const width = ctx.measureText(currentLine + " " + word).width;
                if (width < maxWidth) {
                    currentLine += " " + word;
                } else {
                    lines.push(currentLine);
                    currentLine = word;
                }
            }
            lines.push(currentLine);
            return lines;
        }
        
        // 主绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.width);
            
            // 更新镜面位置（始终在画布中央）
            mirror.x = canvas.width * 0.5;
            mirror.y = canvas.height * 0.5;
            
            // 确保物体和眼睛在合理范围内
            object.x = Math.max(object.radius + 10, Math.min(canvas.width * 0.45, object.x));
            object.y = Math.max(object.radius + 50, Math.min(canvas.height - object.radius - 50, object.y));
            
            eye.x = Math.max(mirror.x + 50, Math.min(canvas.width - eye.radius - 10, eye.x));
            eye.y = Math.max(eye.radius + 50, Math.min(canvas.height - eye.radius - 50, eye.y));
            
            // 绘制所有元素
            drawMirror();
            drawVirtualImage();
            drawSymmetryLines();
            drawLightRays();
            drawObject();
            drawEye();
            drawStepInfo();
        }
        
        // 动画循环
        function animate(timestamp) {
            if (!lastTime) lastTime = timestamp;
            const deltaTime = timestamp - lastTime;
            lastTime = timestamp;
            
            // 更新动画进度
            if (currentStep >= 2) {
                animationProgress += animationDirection * animationSpeed * (deltaTime / 16) * (lightSpeed / 5);
                
                if (animationProgress >= 1) {
                    animationProgress = 1;
                    // 在第3步和第4步，动画完成后保持状态
                    if (currentStep < 3) {
                        setTimeout(() => {
                            animationDirection = -1;
                        }, 1000);
                    }
                }
                
                if (animationProgress <= 0) {
                    animationProgress = 0;
                    animationDirection = 1;
                }
            }
            
            draw();
            requestAnimationFrame(animate);
        }
        
        // 初始化事件监听
        function initEventListeners() {
            // 步骤按钮
            document.querySelectorAll('.step-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const step = parseInt(this.dataset.step);
                    setStep(step);
                });
            });
            
            // 显示控制复选框
            document.getElementById('showLightRays').addEventListener('change', function() {
                showLightRays = this.checked;
                draw();
            });
            
            document.getElementById('showExtensions').addEventListener('change', function() {
                showExtensions = this.checked;
                draw();
            });
            
            document.getElementById('showVirtualImage').addEventListener('change', function() {
                showVirtualImage = this.checked;
                draw();
            });
            
            document.getElementById('showSymmetryLines').addEventListener('change', function() {
                showSymmetryLines = this.checked;
                draw();
            });
            
            // 光线速度滑块
            document.getElementById('lightSpeed').addEventListener('input', function() {
                lightSpeed = parseInt(this.value);
                document.getElementById('speedValue').textContent = 
                    lightSpeed <= 3 ? '慢速' : lightSpeed <= 7 ? '中速' : '快速';
            });
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', function() {
                resetAnimation();
            });
            
            // 鼠标拖拽事件
            canvas.addEventListener('mousedown', handleMouseDown);
            canvas.addEventListener('mousemove', handleMouseMove);
            canvas.addEventListener('mouseup', handleMouseUp);
            canvas.addEventListener('mouseleave', handleMouseUp);
            
            // 触摸屏支持
            canvas.addEventListener('touchstart', handleTouchStart);
            canvas.addEventListener('touchmove', handleTouchMove);
            canvas.addEventListener('touchend', handleTouchEnd);
        }
        
        // 设置当前步骤
        function setStep(step) {
            currentStep = step;
            animationProgress = 0;
            animationDirection = 1;
            
            // 更新按钮状态
            document.querySelectorAll('.step-btn').forEach(btn => {
                if (parseInt(btn.dataset.step) === step) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            // 更新步骤描述
            const stepDescriptions = [
                "观察平面镜成像现象。注意物体与虚像的大小、形状关系。",
                "显示实际光路。光线从物体发出，经平面镜反射后进入眼睛。",
                "揭示虚像原理。眼睛沿直线追溯光线来源，反向延长线在镜后相交形成虚像。",
                "总结规律。物像关于镜面对称，等大、等距，虚像无实际光线到达。"
            ];
            
            document.getElementById('stepDescription').textContent = stepDescriptions[step-1];
            
            // 根据步骤自动设置显示选项
            if (step === 1) {
                document.getElementById('showLightRays').checked = false;
                document.getElementById('showExtensions').checked = false;
                document.getElementById('showSymmetryLines').checked = false;
                showLightRays = false;
                showExtensions = false;
                showSymmetryLines = false;
            } else if (step === 2
<!--检测到代码截断，自动续写中...-->
```javascript
            } else if (step === 3) {
                document.getElementById('showLightRays').checked = true;
                document.getElementById('showExtensions').checked = true;
                document.getElementById('showSymmetryLines').checked = false;
                showLightRays = true;
                showExtensions = true;
                showSymmetryLines = false;
            } else if (step === 4) {
                document.getElementById('showLightRays').checked = true;
                document.getElementById('showExtensions').checked = true;
                document.getElementById('showSymmetryLines').checked = true;
                showLightRays = true;
                showExtensions = true;
                showSymmetryLines = true;
            }
            
            draw();
        }
        
        // 重置动画
        function resetAnimation() {
            object.x = canvas.width * 0.3;
            object.y = canvas.height * 0.5;
            eye.x = canvas.width * 0.8;
            eye.y = canvas.height * 0.3;
            currentStep = 1;
            animationProgress = 0;
            animationDirection = 1;
            
            // 重置显示选项
            document.getElementById('showLightRays').checked = false;
            document.getElementById('showExtensions').checked = false;
            document.getElementById('showSymmetryLines').checked = false;
            document.getElementById('showVirtualImage').checked = true;
            document.getElementById('lightSpeed').value = 5;
            
            showLightRays = false;
            showExtensions = false;
            showSymmetryLines = false;
            showVirtualImage = true;
            lightSpeed = 5;
            
            // 重置步骤按钮
            document.querySelectorAll('.step-btn').forEach(btn => {
                if (parseInt(btn.dataset.step) === 1) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            // 重置步骤描述
            document.getElementById('stepDescription').textContent = 
                "观察平面镜成像现象。注意物体与虚像的大小、形状关系。";
            
            document.getElementById('speedValue').textContent = '中速';
            
            draw();
        }
        
        // 鼠标事件处理
        function handleMouseDown(e) {
            const rect = canvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            // 检查是否点击了物体
            const distToObject = Math.sqrt((x - object.x) ** 2 + (y - object.y) ** 2);
            if (distToObject <= object.radius) {
                object.isDragging = true;
                return;
            }
            
            // 检查是否点击了眼睛
            const distToEye = Math.sqrt((x - eye.x) ** 2 + (y - eye.y) ** 2);
            if (distToEye <= eye.radius) {
                eye.isDragging = true;
                return;
            }
        }
        
        function handleMouseMove(e) {
            const rect = canvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            if (object.isDragging) {
                object.x = x;
                object.y = y;
                draw();
            }
            
            if (eye.isDragging) {
                eye.x = x;
                eye.y = y;
                draw();
            }
        }
        
        function handleMouseUp() {
            object.isDragging = false;
            eye.isDragging = false;
        }
        
        // 触摸事件处理
        function handleTouchStart(e) {
            e.preventDefault();
            const rect = canvas.getBoundingClientRect();
            const touch = e.touches[0];
            const x = touch.clientX - rect.left;
            const y = touch.clientY - rect.top;
            
            // 检查是否触摸了物体
            const distToObject = Math.sqrt((x - object.x) ** 2 + (y - object.y) ** 2);
            if (distToObject <= object.radius) {
                object.isDragging = true;
                return;
            }
            
            // 检查是否触摸了眼睛
            const distToEye = Math.sqrt((x - eye.x) ** 2 + (y - eye.y) ** 2);
            if (distToEye <= eye.radius) {
                eye.isDragging = true;
                return;
            }
        }
        
        function handleTouchMove(e) {
            e.preventDefault();
            const rect = canvas.getBoundingClientRect();
            const touch = e.touches[0];
            const x = touch.clientX - rect.left;
            const y = touch.clientY - rect.top;
            
            if (object.isDragging) {
                object.x = x;
                object.y = y;
                draw();
            }
            
            if (eye.isDragging) {
                eye.x = x;
                eye.y = y;
                draw();
            }
        }
        
        function handleTouchEnd(e) {
            e.preventDefault();
            object.isDragging = false;
            eye.isDragging = false;
        }
        
        // 初始化
        function init() {
            resizeCanvas();
            initEventListeners();
            animate(0);
        }
        
        // 启动应用
        window.addEventListener('load', init);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 平面镜成像原理交互式教学动画使用指南

欢迎使用“平面镜成像原理”交互式教学动画！本动画旨在通过直观、动态的可视化方式，帮助您深入理解平面镜成像的核心概念——虚像的形成原理与光的实际路径。无论您是教师、学生还是对光学感兴趣的爱好者，本工具都将为您提供一种全新的学习体验。

---

### 一、 功能说明

本动画是一个基于HTML5 Canvas技术构建的交互式教学工具。它通过分步演示、实时交互和动态光路追踪，将抽象的物理概念转化为直观的视觉过程。您不仅可以观察现象，更能通过拖拽、控制等方式主动探索成像规律。

### 二、 主要功能

1.  **分步学习模式**：
    *   **步骤1：观察成像** - 直观展示物体在平面镜中成等大、等距虚像的现象。
    *   **步骤2：显示光路** - 动态绘制从物体发出，经镜面反射后进入眼睛的**实际光线**（黄色实线）。
    *   **步骤3：揭示原理** - 展示眼睛如何沿直线反向追溯光线，其**反向延长线**（蓝色虚线）在镜后相交，从而“看到”虚像。
    *   **步骤4：总结规律** - 显示对称辅助线，总结“物像关于镜面对称”的几何规律。

2.  **交互控制面板**：
    *   **显示/隐藏开关**：可独立控制“实际光线”、“反向延长线”、“虚像”和“对称辅助线”的显示，便于聚焦核心概念。
    *   **光线速度调节**：通过滑块控制光线传播的动画速度，适应不同观察节奏。
    *   **拖拽交互**：
        *   **拖动物体**：实时观察虚像位置、光路和对称关系如何随之变化。
        *   **拖动眼睛**：改变观察视角，理解为何虚像位置固定，但不同位置看到的反射光线不同。
    *   **重置按钮**：一键将动画恢复到初始状态。

3.  **视觉图例**：
    界面底部提供完整的颜色与线型图例，帮助您快速理解各图形元素所代表的物理意义。

### 三、 设计特色

1.  **符合认知规律**：采用“现象 → 过程 → 原理 → 规律”的四步递进设计，引导学习者层层深入。
2.  **虚实对比鲜明**：
    *   **实 vs 虚**：用**实心**红色圆表示物体，用**半透明**红色圆表示虚像，直观体现“虚”的特性。
    *   **实线 vs 虚线**：用**黄色实线箭头**表示真实的光线路径，用**蓝色虚线箭头**表示人脑的视觉推理路径（反向延长线），清晰区分客观存在与主观感知。
3.  **即时反馈**：所有交互操作（拖拽、开关控制）的效果均会实时呈现在动画中，提供即时的探究反馈。
4.  **响应式布局**：适配不同尺寸的屏幕，在电脑、平板等设备上均可获得良好体验。

### 四、 教学要点（给教师的建议）

本动画可用于辅助讲解以下核心知识点：

1.  **虚像的本质**：重点强调虚像是**反射光线反向延长线的交点**，并无实际光线到达该位置。这是学生最容易产生误解的地方。
2.  **光路的可逆性**：可以通过拖拽眼睛，并观察光路，引导学生思考“如果光从眼睛发出，路径会怎样”，从而自然引出光路可逆原理。
3.  **成像规律探究**：
    *   在**步骤4**，开启“对称辅助线”，引导学生测量并总结物距与像距相等。
    *   拖动物体至不同位置，验证“物像连线与镜面垂直”这一规律始终成立。
4.  **突破思维定式**：学生常误以为“我们看到了镜子里的像”。动画明确展示：我们看到的永远是进入眼睛的**光**，大脑只是“认为”光来自镜后。这是理解所有“虚像”问题的关键。

### 五、 使用建议

1.  **初次学习**：建议按照 **1 → 2 → 3 → 4** 的步骤顺序完整体验一遍，跟随动画的引导建立完整认知框架。
2.  **重点探究**：
    *   理解“反向延长线”时，可**只打开“实际光线”和“反向延长线”**，关闭虚像，观察虚线在镜后相交后，再打开虚像，会发现交点正是虚像位置。
    *   探究对称性时，**只打开“虚像”和“对称辅助线”**，拖动物体，直观感受几何对称关系。
3.  **课堂演示**：教师可将动画用于课堂集体讲解。在关键步骤（如光线反射、延长线相交）可放慢速度，配合提问引导学生预测下一步现象。
4.  **自主复习与探究**：学生可用来自主复习。通过反复拖拽物体和眼睛，并组合不同的显示选项，自己提出并验证问题，例如：“如果物体离镜子非常近，虚像会在哪里？”、“站在侧面还能看到虚像吗？为什么？”
5.  **关联思考**：在理解本动画的基础上，可进一步思考：其他光学元件（如凸透镜、凹透镜）所成的虚像，其原理有何异同？

---

**祝您探索愉快，愿这束“光”能照亮您对物理世界的理解！**