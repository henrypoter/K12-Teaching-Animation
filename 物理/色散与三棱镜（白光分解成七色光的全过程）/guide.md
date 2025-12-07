# 需求：色散与三棱镜（白光分解成七色光的全过程）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要是初中或高中物理课程的初学者，他们需要直观地理解“色散”这一光学现象。用户的核心需求包括：
1.  **现象可视化**：亲眼看到“白光不是单色光，而是由多种色光混合而成”这一抽象概念的具体过程。
2.  **原理理解**：理解色散发生的两个关键物理原因——不同色光在介质（玻璃）中的传播速度不同，从而导致折射率不同。
3.  **过程分解**：将“白光入射 -> 在三棱镜内发生两次折射 -> 出射光散开”这一连续过程分解，便于分步学习。
4.  **主动探索**：能够通过交互改变条件（如入射光颜色、入射角度、棱镜形状等），观察结果变化，从而深化理解并建立因果关系。
5.  **知识关联**：将三棱镜色散与彩虹、光盘反光等生活现象联系起来。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
*   **核心概念**：
    *   白光（复合光）由多种单色光（红、橙、黄、绿、蓝、靛、紫）组成。
    *   不同单色光在相同介质中的折射率不同（n紫 > n红）。
    *   三棱镜的几何形状导致光线发生两次折射，将微小的折射角差异累积、放大，最终形成明显的色散光谱。

*   **认知规律**：
    1.  **从整体到细节**：先展示完整的、动态的色散现象（吸引注意力，建立整体印象），再分解步骤，剖析原理。
    2.  **从具体到抽象**：用生动的光线动画展示具体过程，随后用示意图和文字标注引入“折射率”等抽象物理量。
    3.  **从观察到解释**：引导用户先“看到”光谱，再思考“为什么光会分开”，最后揭示背后的物理规律。

*   **交互设计**：
    *   **流程控制**：提供“播放/暂停/重置”按钮，让用户控制动画节奏。
    *   **分步学习模式**：将过程分解为“入射”、“第一次折射”、“棱镜内传播”、“第二次折射”、“出射形成光谱”几个步骤，可单独查看和讲解。
    *   **探索实验模式**：提供可调节控件，如：
        *   滑块调节白光入射角。
        *   选择器切换入射光类型（白光、单色红光、单色紫光）。
        *   滑块微调棱镜顶角（形状）。
    *   **提示与反馈**：鼠标悬停在关键部位（如光线、角度）时，显示相关物理量名称和值；调整参数时，光谱实时变化。

*   **视觉呈现**：
    *   **主场景**：一个深色或黑色背景，突出光线轨迹。中央放置一个透明玻璃质感的三棱镜。
    *   **光线绘制**：
        *   白光用白色或浅黄色光束表示。
        *   色散后的单色光用七种清晰、饱和度高的颜色光束表示，并明确标注名称。
        *   光线绘制平滑，带有光晕效果，增强“光”的质感。
        *   在棱镜内部，可以绘制略微分开的彩色光线，暗示折射正在发生。
    *   **辅助视觉元素**：
        *   绘制法线（虚线）。
        *   清晰标注入射角、折射角。
        *   在出射光谱旁，可绘制一个放大的、连续的彩色光谱条。
        *   关键物理量（折射率n）可以动态显示在对应光线旁。

#### 配色方案选择
*   **背景**：深空蓝或纯黑色。目的是最大化对比度，让彩色光线和白色光线清晰可见，模拟暗室环境。
*   **三棱镜**：采用浅灰色（#E0E0E0）描边，内部填充为半透明的浅蓝色或浅灰色（RGBA: 200, 220, 255, 0.2），营造透明玻璃的质感，并能隐约看到内部的光线路径。
*   **光线颜色**：
    *   白光：亮白色（#FFFFFF）或暖白色（#FFF8E7）。
    *   七色光：采用标准且易于区分的彩虹色系，确保紫色和蓝色、黄色和绿色之间有足够区分度。例如：红(#FF3333)、橙(#FF9933)、黄(#FFFF33)、绿(#33FF33)、蓝(#3333FF)、靛(#4B0082)、紫(#9933FF)。
*   **界面控件**：使用中性色（如浅灰色 #F0F0F0）背景，深灰色（#333）文字和边框，确保控件清晰但不喧宾夺主。
*   **标注与文字**：白色或浅黄色文字，搭配半透明黑色背景框，确保在任何位置都清晰可读。

#### 交互功能列表
1.  **动画控制区**：
    *   “播放/暂停”按钮：控制整个色散过程的自动播放。
    *   “重置”按钮：将所有参数恢复至初始状态。
    *   “分步演示”按钮组：包含“步骤1：入射”、“步骤2：第一次折射”…等按钮，点击后高亮并讲解该步骤。
2.  **参数调节区**：
    *   “入射角”滑块：调节白光射向棱镜的角度，实时观察入射角与出射光谱位置、宽度之间的关系。
    *   “光源类型”选择器：在“白光”、“红光”、“紫光”之间切换。选择单色光时，演示光线通过棱镜只发生偏折而不散开。
    *   “棱镜顶角”滑块（进阶）：微调棱镜的尖锐程度，观察顶角大小对色散效果（光谱宽度）的影响。
3.  **信息显示区**：
    *   实时显示当前入射角、折射角等数值。
    *   显示红、紫两种光线的折射率对比（n_红 < n_紫）。
4.  **悬停提示**：
    *   悬停在光线上：显示该光线名称（如“红光”）及其在当前介质中的折射率。
    *   悬停在棱镜边或角上：显示相关几何名称（如“折射面”、“顶角”）。
    *   悬停在角度上：高亮该角并显示角度值。
5.  **知识扩展区（可选，可折叠）**：
    *   一个链接或按钮，点击后展开一个区域，展示“生活中的色散”（如彩虹、光盘、肥皂泡）的简短图文说明，建立知识与生活的联系。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>色散现象与三棱镜 - 白光分解实验</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Microsoft YaHei', 'Segoe UI', sans-serif;
            background: linear-gradient(to bottom, #0a0a2a, #1a1a3a);
            color: #f0f0f0;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        h1 {
            color: #ffffff;
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
        }

        .subtitle {
            color: #a0c8ff;
            font-size: 1.2rem;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }

        .animation-section {
            flex: 1;
            min-width: 600px;
            background: rgba(0, 0, 0, 0.4);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .controls-section {
            flex: 1;
            min-width: 300px;
            background: rgba(0, 0, 0, 0.4);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background: #000;
            border-radius: 10px;
            overflow: hidden;
            border: 2px solid rgba(255, 255, 255, 0.1);
        }

        #animationCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }

        .info-overlay {
            position: absolute;
            top: 15px;
            left: 15px;
            background: rgba(0, 0, 0, 0.7);
            padding: 10px 15px;
            border-radius: 8px;
            font-size: 0.9rem;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .control-group {
            margin-bottom: 25px;
        }

        h2 {
            color: #7ab8ff;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid rgba(122, 184, 255, 0.3);
            font-size: 1.4rem;
        }

        h3 {
            color: #a0c8ff;
            margin: 15px 0 10px;
            font-size: 1.1rem;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 15px 0;
        }

        button {
            background: linear-gradient(to bottom, #2a4a7a, #1a3a6a);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 120px;
        }

        button:hover {
            background: linear-gradient(to bottom, #3a5a8a, #2a4a7a);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        button:active {
            transform: translateY(0);
        }

        button.active {
            background: linear-gradient(to bottom, #4a6a9a, #3a5a8a);
            box-shadow: inset 0 2px 5px rgba(0, 0, 0, 0.3);
        }

        .slider-container {
            margin: 15px 0;
        }

        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: #2a2a4a;
            outline: none;
            -webkit-appearance: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #4a8aff;
            cursor: pointer;
            box-shadow: 0 0 10px rgba(74, 138, 255, 0.5);
        }

        .value-display {
            background: rgba(0, 0, 0, 0.5);
            padding: 8px 12px;
            border-radius: 6px;
            font-family: monospace;
            font-size: 1.1rem;
            text-align: center;
            margin: 10px 0;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .color-spectrum {
            height: 30px;
            background: linear-gradient(to right, 
                #FF3333, #FF9933, #FFFF33, #33FF33, 
                #3333FF, #4B0082, #9933FF);
            border-radius: 6px;
            margin: 15px 0;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .knowledge-section {
            background: rgba(0, 0, 0, 0.4);
            border-radius: 15px;
            padding: 25px;
            margin-top: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .knowledge-content {
            display: none;
            padding-top: 15px;
        }

        .knowledge-content.active {
            display: block;
        }

        .knowledge-item {
            background: rgba(30, 40, 70, 0.5);
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
            border-left: 4px solid #4a8aff;
        }

        .knowledge-item h4 {
            color: #a0c8ff;
            margin-bottom: 8px;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #888;
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .animation-section, .controls-section {
                min-width: 100%;
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
            <h1>色散现象与三棱镜</h1>
            <p class="subtitle">白光分解成七色光的全过程演示</p>
        </header>

        <div class="main-content">
            <section class="animation-section">
                <h2>实验演示</h2>
                <div class="canvas-container">
                    <canvas id="animationCanvas"></canvas>
                    <div class="info-overlay">
                        <div>当前模式: <span id="currentMode">完整演示</span></div>
                        <div>入射角: <span id="currentAngle">45°</span></div>
                    </div>
                </div>
            </section>

            <section class="controls-section">
                <h2>实验控制</h2>
                
                <div class="control-group">
                    <h3>动画控制</h3>
                    <div class="button-group">
                        <button id="playBtn">播放</button>
                        <button id="pauseBtn">暂停</button>
                        <button id="resetBtn">重置</button>
                    </div>
                </div>

                <div class="control-group">
                    <h3>分步学习</h3>
                    <div class="button-group">
                        <button class="step-btn" data-step="0">完整演示</button>
                        <button class="step-btn" data-step="1">1. 白光入射</button>
                        <button class="step-btn" data-step="2">2. 第一次折射</button>
                        <button class="step-btn" data-step="3">3. 棱镜内传播</button>
                        <button class="step-btn" data-step="4">4. 第二次折射</button>
                        <button class="step-btn" data-step="5">5. 形成光谱</button>
                    </div>
                </div>

                <div class="control-group">
                    <h3>参数调节</h3>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>入射角度</span>
                            <span id="angleValue">45°</span>
                        </div>
                        <input type="range" id="angleSlider" min="20" max="70" value="45" step="1">
                    </div>

                    <div class="slider-container">
                        <div class="slider-label">
                            <span>棱镜顶角</span>
                            <span id="prismValue">60°</span>
                        </div>
                        <input type="range" id="prismSlider" min="40" max="80" value="60" step="1">
                    </div>

                    <div class="slider-container">
                        <div class="slider-label">
                            <span>动画速度</span>
                            <span id="speedValue">1.0x</span>
                        </div>
                        <input type="range" id="speedSlider" min="0.1" max="3" value="1" step="0.1">
                    </div>
                </div>

                <div class="control-group">
                    <h3>光源选择</h3>
                    <div class="button-group">
                        <button class="light-btn active" data-light="white">白光</button>
                        <button class="light-btn" data-light="red">红光</button>
                        <button class="light-btn" data-light="violet">紫光</button>
                    </div>
                    <div class="value-display">
                        折射率: <span id="refractionInfo">n(红)=1.51 &lt; n(紫)=1.53</span>
                    </div>
                </div>

                <div class="color-spectrum"></div>
                <p style="text-align: center; font-size: 0.9rem; color: #aaa;">
                    可见光谱: 红 → 橙 → 黄 → 绿 → 蓝 → 靛 → 紫
                </p>
            </section>
        </div>

        <section class="knowledge-section">
            <h2 style="cursor: pointer;" id="knowledgeToggle">📚 知识扩展 (点击展开)</h2>
            <div class="knowledge-content" id="knowledgeContent">
                <div class="knowledge-item">
                    <h4>色散原理</h4>
                    <p>白光是由不同波长的单色光混合而成。不同颜色的光在玻璃中的传播速度不同，导致折射率不同（n紫 > n红）。三棱镜的几何形状将这种微小的折射差异放大，形成光谱。</p>
                </div>
                <div class="knowledge-item">
                    <h4>生活中的色散现象</h4>
                    <p>• 彩虹：阳光在水滴中发生折射、反射和色散<br>
                       • 光盘表面：光栅衍射产生彩色条纹<br>
                       • 肥皂泡：薄膜干涉产生彩色图案<br>
                       • 钻石：多个切面增强色散效果，产生"火彩"</p>
                </div>
                <div class="knowledge-item">
                    <h4>科学史话</h4>
                    <p>1666年，艾萨克·牛顿通过三棱镜实验首次证明了白光是由不同颜色的光组成的，这一发现奠定了现代光学的基础。</p>
                </div>
            </div>
        </section>

        <footer>
            <p>教学动画 | 色散现象与三棱镜 | 设计用于物理光学教学</p>
            <p>提示：尝试调节参数观察色散效果的变化，使用分步学习模式理解每个物理过程</p>
        </footer>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');

        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }

        // 初始化变量
        let animationId = null;
        let isPlaying = true;
        let currentStep = 0; // 0:完整演示, 1-5:分步
        let animationTime = 0;
        let animationSpeed = 1.0;
        
        // 实验参数
        let incidentAngle = 45; // 入射角（度）
        let prismAngle = 60;    // 棱镜顶角（度）
        let lightType = 'white'; // 光源类型
        
        // 颜色定义
        const colors = {
            white: '#FFFFFF',
            red: '#FF3333',
            orange: '#FF9933',
            yellow: '#FFFF33',
            green: '#33FF33',
            blue: '#3333FF',
            indigo: '#4B0082',
            violet: '#9933FF',
            prism: 'rgba(200, 220, 255, 0.15)',
            prismBorder: 'rgba(224, 224, 224, 0.8)'
        };

        // 折射率数据
        const refractionIndices = {
            red: 1.51,
            orange: 1.512,
            yellow: 1.514,
            green: 1.516,
            blue: 1.518,
            indigo: 1.52,
            violet: 1.53
        };

        // 初始化
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);

        // 绘制三棱镜
        function drawPrism() {
            const centerX = canvas.width * 0.4;
            const centerY = canvas.height * 0.5;
            const size = Math.min(canvas.width, canvas.height) * 0.3;
            
            // 计算棱镜顶点
            const angleRad = prismAngle * Math.PI / 180;
            const height = size * Math.sin(angleRad / 2);
            const halfBase = size * Math.cos(angleRad / 2);
            
            const topX = centerX;
            const topY = centerY - height / 2;
            const leftX = centerX - halfBase;
            const leftY = centerY + height / 2;
            const rightX = centerX + halfBase;
            const rightY = centerY + height / 2;
            
            // 绘制棱镜
            ctx.save();
            ctx.beginPath();
            ctx.moveTo(topX, topY);
            ctx.lineTo(leftX, leftY);
            ctx.lineTo(rightX, rightY);
            ctx.closePath();
            
            // 棱镜填充
            ctx.fillStyle = colors.prism;
            ctx.fill();
            
            // 棱镜边框
            ctx.lineWidth = 2;
            ctx.strokeStyle = colors.prismBorder;
            ctx.stroke();
            
            // 标注顶角
            ctx.fillStyle = 'rgba(255, 255, 255, 0.7)';
            ctx.font = '14px Arial';
            ctx.fillText(`${prismAngle}°`, centerX, centerY - height/2 - 10);
            
            ctx.restore();
            
            return { topX, topY, leftX, leftY, rightX, rightY, centerX, centerY };
        }

        // 计算光线路径
        function calculateLightPath(prism, color, isSingleColor = false) {
            const { topX, topY, leftX, leftY, rightX, rightY, centerX, centerY } = prism;
            
            // 入射点（左侧面中点）
            const incidentX = leftX + (topX - leftX) * 0.5;
            const incidentY = leftY + (topY - leftY) * 0.5;
            
            // 左侧面法线（垂直于左侧面）
            const leftNormalAngle = Math.atan2(topY - leftY, topX - leftX) + Math.PI / 2;
            
            // 入射角（相对于法线）
            const incidentAngleRad = incidentAngle * Math.PI / 180;
            const actualIncidentAngle = leftNormalAngle + incidentAngleRad;
            
            // 计算折射角（斯涅尔定律）
            const n_air = 1.0;
            const n_glass = refractionIndices[color];
            const refractionAngle = Math.asin(Math.sin(incidentAngleRad) * n_air / n_glass);
            
            // 棱镜内光线方向
            const internalAngle = leftNormalAngle + refractionAngle;
            
            // 计算与右侧面的交点
            const m1 = Math.tan(internalAngle);
            const b1 = incidentY - m1 * incidentX;
            
            // 右侧面直线方程
            const m2 = (rightY - topY) / (rightX - topX);
            const b2 = topY - m2 * topX;
            
            // 求交点
            const exitX = (b2 - b1) / (m1 - m2);
            const exitY = m1 * exitX + b1;
            
            // 右侧面法线
            const rightNormalAngle = Math.atan2(topY - rightY, topX - rightX) - Math.PI / 2;
            
            // 出射角计算
            const internalIncidentAngle = internalAngle - rightNormalAngle;
            const exitAngle = Math.asin(Math.sin(internalIncidentAngle) * n_glass / n_air);
            
            // 最终出射方向
            const finalAngle = rightNormalAngle + exitAngle;
            
            return {
                incidentX, incidentY,
                exitX, exitY,
                internalAngle, finalAngle,
                refractionAngle: refractionAngle * 180 / Math.PI,
                exitAngle: exitAngle * 180 / Math.PI
            };
        }

        // 绘制光线
        function drawLightBeam(startX, startY, angle, length, color, width = 3, withGlow = true) {
            ctx.save();
            
            const endX = startX + Math.cos(angle) * length;
            const endY = startY + Math.sin(angle) * length;
            
            // 光晕效果
            if (withGlow) {
                ctx.beginPath();
                ctx.moveTo(startX, startY);
                ctx.lineTo(endX, endY);
                
                const gradient = ctx.createLinearGradient(startX, startY, endX, endY);
                gradient.addColorStop(0, color + '80');
                gradient.addColorStop(0.5, color + 'FF');
                gradient.addColorStop(1, color + '80');
                
                ctx.strokeStyle = gradient;
                ctx.lineWidth = width + 4;
                ctx.lineCap = 'round';
                ctx.stroke();
            }
            
            // 主光线
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            ctx.lineTo(endX, endY);
            ctx.strokeStyle = color;
            ctx.lineWidth = width;
            ctx.lineCap = 'round';
            ctx.stroke();
            
            ctx.restore();
            
            return { endX, endY };
        }

        // 绘制单色光
        function drawSingleColorLight(prism, colorName, progress) {
            const path = calculateLightPath(prism, colorName, true);
            const color = colors[colorName];
            
            // 入射光线
            const incidentLength = canvas.width * 0.2 * progress;
            const incidentAngle = path.internalAngle - path.refractionAngle * Math.PI / 180;
            drawLightBeam(
                path.incidentX - Math.cos(incidentAngle) * incidentLength,
                path.incidentY - Math.sin(incidentAngle) * incidentLength,
                incidentAngle,
                incidentLength,
                color
            );
            
            // 棱镜内光线
            if (progress > 0.3) {
                const internalProgress = Math.min(1, (progress - 0.3) / 0.4);
                const internalLength = Math.sqrt(
                    Math.pow(path.exitX - path.incidentX, 2) + 
                    Math.pow(path.exitY - path.incidentY, 2)
                ) * internalProgress;
                
                drawLightBeam(
                    path.incidentX,
                    path.incidentY,
                    path.internalAngle,
                    internalLength,
                    color
                );
            }
            
            // 出射光线
            if (progress > 0.7) {
                const exitProgress = (progress - 0.7) / 0.3;
                const exitLength = canvas.width * 0.3 * exitProgress;
                
                drawLightBeam(
                    path.exitX,
                    path.exitY,
                    path.finalAngle,
                    exitLength,
                    color
                );
            }
            
            // 标注折射率
            if (progress > 0.5) {
                ctx.save();
                ctx.fillStyle = color;
                ctx.font = 'bold 14px Arial';
                ctx.fillText(`n=${refractionIndices[colorName]}`, 
                    path.incidentX + 20, path.incidentY - 10);
                ctx.restore();
            }
        }

        // 绘制白光分解
        function drawWhiteLightDispersion(prism, progress) {
            const colorOrder = ['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet'];
            
            colorOrder.forEach((colorName, index) => {
                // 每个颜色稍微偏移一点角度
                const angleOffset = (index - 3) * 0.5 * Math.PI / 180;
                const originalAngle = incidentAngle;
                incidentAngle += (index - 3) * 0.1;
                
                const path = calculateLightPath(prism, colorName);
                const color = colors[colorName];
                
                // 根据步骤控制绘制
                let drawIncident = progress > 0.1;
                let drawInternal = progress > 0.3;
                let drawExit = progress > 0.7;
                
                // 分步模式控制
                if (currentStep === 1) { // 只绘制入射
                    drawInternal = false;
                    drawExit = false;
                    drawIncident = progress > 0.1;
                } else if (currentStep === 2) { // 只绘制第一次折射
                    drawIncident = progress > 0.1;
                    drawInternal = progress > 0.3 && progress < 0.5;
                    drawExit = false;
                } else if (currentStep === 3) { // 只绘制棱镜内
                    drawIncident = false;
                    drawInternal = progress > 0.3;
                    drawExit = false;
                } else if (currentStep === 4) { // 只绘制第二次折射
                    drawIncident = false;
                    drawInternal = progress > 0.3;
                    drawExit = progress > 0.7 && progress < 0.9;
                } else if (currentStep === 5) { // 只绘制出射光谱
                    drawIncident = false;
                    drawInternal = false;
                    drawExit = progress > 0.7;
                }
                
                // 入射光线
                if (drawIncident) {
                    const incidentLength = canvas.width * 0.2 * Math.min(1, progress / 0.3);
                    const incidentAngle = path.internalAngle - path.refractionAngle * Math.PI / 180 + angleOffset;
                    drawLightBeam(
                        path.incidentX - Math.cos(incidentAngle) * incidentLength,
                        path.incidentY - Math.sin(incidentAngle) * incidentLength,
                        incidentAngle,
                        incidentLength,
                        currentStep === 0 ? colors.white : color,
                        currentStep === 0 ? 5 : 2,
                        currentStep === 0
                    );
                }
                
                // 棱镜内光线
                if (drawInternal) {
                    const internalProgress = currentStep === 2 ? 
                        Math.min(1, (progress - 0.3) / 0.2) :
                        Math.min(1, (progress - 0.3) / 0.4);
                    
                    const internalLength = Math.sqrt(
                        Math.pow(path.exitX - path.incidentX, 2) + 
                        Math.pow(path.exitY - path.incidentY, 2)
                    ) * internalProgress;
                    
                    drawLightBeam(
                        path.incidentX,
                        path.incidentY,
                        path.internalAngle + angleOffset,
                        internalLength,
                        color,
                        2
                    );
                }
                
                // 出射光线
                if (drawExit) {
                    const exitProgress = currentStep === 4 ? 
                        Math.min(1, (progress - 0.7) / 0.2) :
                        Math.min(1, (progress - 0.7) / 0.3);
                    
                    const exitLength = canvas.width * 0.3 * exitProgress;
                    
                    drawLightBeam(
                        path.exitX,
                        path.exitY,
                        path.finalAngle + angleOffset * 3,
                        exitLength,
                        color,
                        2,
                        true
                    );
                }
                
                incidentAngle = originalAngle; // 恢复原始角度
            });
            
            // 绘制光谱
            if (progress > 0.8 && (currentStep === 0 || currentStep === 5)) {
                const spectrumX = prism.rightX + 50;
                const spectrumY = prism.rightY;
                const spectrumWidth = 200;
                const spectrumHeight = 150;
                
                // 光谱背景
                ctx.save();
                ctx.fillStyle = 'rgba(0, 0, 0, 0.5)';
                ctx.fillRect(spectrumX, spectrumY - spectrumHeight/2, spectrumWidth, spectrumHeight);
                
                // 渐变光谱
                const gradient = ctx.createLinearGradient(
                    spectrumX, spectrumY - spectrumHeight/2,
                    spectrumX + spectrumWidth, spectrumY - spectrumHeight/2
                );
                
                gradient.addColorStop(0, colors.red);
                gradient.addColorStop(1/6, colors.orange);
                gradient.addColorStop(2/6, colors.yellow);
                gradient.addColorStop(3/6, colors.green);
                gradient.addColorStop(4/6, colors.blue);
                gradient.addColorStop(5/6, colors.indigo);
                gradient.addColorStop(1, colors.violet);
                
                ctx.fillStyle = gradient;
                ctx.fillRect(spectrumX + 10, spectrumY - spectrumHeight/2 + 10, 
                           spectrumWidth - 20, spectrumHeight - 20);
                
                // 光谱标签
                ctx.fillStyle = 'white';
                ctx.font = '12px Arial';
                ctx.textAlign = 'center';
                const labels = ['红', '橙', '黄', '绿', '蓝', '靛', '紫'];
                for (let i = 0; i < 7; i++) {
                    ctx.fillText(labels[i], 
                        spectrumX + 10 + (i * (spectrumWidth - 20) / 6) + (spectrumWidth - 20) / 12,
                        spectrumY + spectrumHeight/2 - 5);
                }
                
                ctx.restore();
            }
        }

        // 绘制法线和角度标注
        function drawAnnotations(prism) {
            const { leftX, leftY, topX, topY, rightX, rightY } = prism;
            
            ctx.save();
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.5)';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            
            // 左侧面法线
            const leftMidX = (leftX + topX) / 2;
            const leftMidY = (leftY + topY) / 2;
            const leftNormalLength = 60;
            const leftNormalAngle = Math.atan2(topY - leftY, topX - leftX) + Math.PI / 2;
            
            ctx.beginPath();
            ctx.moveTo(leftMidX, leftMidY);
            ctx.lineTo(
                leftMidX + Math.cos(leftNormalAngle) * leftNormalLength,
                leftMidY + Math.sin(leftNormalAngle) * leftNormalLength
            );
            ctx.stroke();
            
            // 标注入射角
            ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.font = '14px Arial';
            ctx.fillText(`入射角: ${incidentAngle}°`, leftMidX + 80, leftMidY - 30);
            
            ctx.restore();
        }

        // 主绘制函数
        function draw() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制星空背景
            drawBackground();
            
            // 绘制三棱镜
            const prism = drawPrism();
            
            // 绘制法线和标注
            drawAnnotations(prism);
            
            // 计算动画进度
            let progress = 0;
            if (isPlaying) {
                animationTime += 0.016 * animationSpeed; // 约60fps
                progress = (Math.sin(animationTime) + 1) / 2; // 0到1之间循环
                
                // 分步模式下，进度只到当前步骤
                if (currentStep > 0) {
                    progress = Math.min(progress, currentStep * 0.2);
                }
            } else {
                progress = animationTime;
            }
            
            // 根据光源类型绘制光线
            if (lightType === 'white') {
                drawWhiteLightDispersion(prism, progress);
            } else {
                drawSingleColorLight(prism, lightType, progress);
            }
            
            // 更新显示信息
            updateDisplayInfo();
        }

        // 绘制星空背景
        function drawBackground() {
            // 深色渐变背景
            const gradient = ctx.createLinearGradient(0, 0, 0, canvas.height);
            gradient.addColorStop(0, '#0a0a2a');
            gradient.addColorStop(1, '#1a1a3a');
            ctx.fillStyle = gradient;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制星星
            ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            for (let i = 0; i < 50; i++) {
                const x = (i * 1234567) % canvas.width;
                const y = (i * 7654321) % canvas.height;
                const size = (i % 3) * 0.5 + 0.5;
                
                ctx.beginPath();
                ctx.arc(x, y, size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        // 更新显示信息
        function updateDisplayInfo() {
            document.getElementById('currentAngle').textContent = `${incidentAngle}°`;
            document.getElementById('angleValue').textContent = `${incidentAngle}°`;
            document.getElementById('prismValue').textContent = `${prismAngle}°`;
            document.getElementById('speedValue').textContent = `${animationSpeed.toFixed(1)}x`;
            
            // 更新模式显示
            const modeNames = ['完整演示', '白光入射', '第一次折射', '棱镜内传播', '第二次折射', '形成光谱'];
            document.getElementById('currentMode').textContent = modeNames[currentStep];
            
            // 更新折射率信息
            if (lightType === 'white') {
                document.getElementById('refractionInfo').innerHTML = 
                    `n(红)=${refractionIndices.red} &lt; n(紫)=${refractionIndices.violet}`;
            } else if (lightType === 'red') {
                document.getElementById('refractionInfo').textContent = 
                    `n(红)=${refractionIndices.red}`;
            } else {
                document.getElementById('refractionInfo').textContent = 
                    `n(紫)=${refractionIndices.violet}`;
            }
        }

        // 动画循环
        function animate() {
            draw();
            animationId = requestAnimationFrame(animate);
        }

        // 初始化事件监听
        function initEventListeners() {
            // 动画控制按钮
            document.getElementById('playBtn').addEventListener('click', () => {
                isPlaying = true;
            });
            
            document.getElementById('pauseBtn').addEventListener('click', () => {
                isPlaying = false;
            });
            
            document.getElementById('resetBtn').addEventListener('click', () => {
                animationTime = 0;
                incidentAngle = 45;
                prismAngle = 60;
                animationSpeed = 1.0;
                lightType = 'white';
                currentStep = 0;
                
                // 更新UI
                document.getElementById('angleSlider').value = incidentAngle;
                document.getElementById('prismSlider').value = prismAngle;
                document.getElementById('speedSlider').value = animationSpeed;
                
                // 更新按钮状态
                document.querySelectorAll('.light-btn').forEach(btn => {
                    btn.classList.remove('active');
                });
                document.querySelector('.light-btn[data-light="white"]').classList.add('active');
                
                document.querySelectorAll('.step-btn').forEach(btn => {
                    btn.classList.remove('active');
                });
                document.querySelector('.step-btn[data-step="0"]').classList.add('active');
            });
            
            // 分步学习按钮
            document.querySelectorAll('.step-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const step = parseInt(this.dataset.step);
                    currentStep = step;
                    
                    // 更新按钮状态
                    document.querySelectorAll('.step-btn').forEach(b => {
                        b.classList.remove('active');
                    });
                    this.classList.add('active');
                    
                    // 重置动画时间
                    animationTime = 0;
                });
            });
            
            // 光源选择按钮
            document.querySelectorAll('.light-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    lightType = this.dataset.light;
                    
                    // 更新按钮状态
                    document.querySelectorAll('.light-btn').forEach(b => {
                        b.classList.remove('active');
                    });
                    this.classList.add('active');
                    
                    // 重置动画时间
                    animationTime = 0;
                });
            });
            
            // 滑块控制
            document.getElementById('angleSlider').addEventListener('input', function() {
                incidentAngle = parseInt(this.value);
                animationTime = 0;
            });
            
            document.getElementById('prismSlider').addEventListener('input', function() {
                prismAngle = parseInt(this.value);
                animationTime = 0;
            });
            
            document.getElementById('speedSlider').addEventListener('input', function() {
                animationSpeed = parseFloat(this.value);
            });
            
            // 知识扩展切换
            document.getElementById('knowledgeToggle').add
<!--检测到代码截断，自动续写中...-->
            // 知识扩展切换
            document.getElementById('knowledgeToggle').addEventListener('click', function() {
                const content = document.getElementById('knowledgeContent');
                content.classList.toggle('active');
                this.textContent = content.classList.contains('active') ? 
                    '📚 知识扩展 (点击收起)' : '📚 知识扩展 (点击展开)';
            });
            
            // 悬停提示效果
            canvas.addEventListener('mousemove', function(event) {
                const rect = canvas.getBoundingClientRect();
                const x = event.clientX - rect.left;
                const y = event.clientY - rect.top;
                
                // 简单的区域检测（实际应用中可以根据坐标计算具体位置）
                const prism = drawPrism();
                const prismCenterX = (prism.leftX + prism.topX + prism.rightX) / 3;
                const prismCenterY = (prism.leftY + prism.topY + prism.rightY) / 3;
                
                const distance = Math.sqrt(Math.pow(x - prismCenterX, 2) + Math.pow(y - prismCenterY, 2));
                
                if (distance < 150) {
                    canvas.style.cursor = 'pointer';
                    // 可以在这里添加更详细的悬停提示
                } else {
                    canvas.style.cursor = 'default';
                }
            });
            
            // 点击画布重置动画
            canvas.addEventListener('click', function() {
                if (!isPlaying) {
                    animationTime = 0;
                }
            });
        }

        // 页面加载完成后初始化
        window.addEventListener('load', function() {
            resizeCanvas();
            initEventListeners();
            animate();
            
            // 初始激活完整演示按钮
            document.querySelector('.step-btn[data-step="0"]').classList.add('active');
            
            // 初始激活白光按钮
            document.querySelector('.light-btn[data-light="white"]').classList.add('active');
            
            console.log('色散现象教学动画已加载完成！');
            console.log('提示：尝试调节参数观察色散效果的变化');
        });

        // 页面卸载时清理动画
        window.addEventListener('beforeunload', function() {
            if (animationId) {
                cancelAnimationFrame(animationId);
            }
        });
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 《色散现象与三棱镜》交互式教学动画使用指南

欢迎使用本交互式教学动画！本动画旨在通过直观、互动的方式，帮助您深入理解白光通过三棱镜分解成七色光（色散）的物理过程。无论您是学生、教师还是科学爱好者，这份指南都将帮助您充分利用本动画的所有功能。

---

### 一、功能说明

本动画是一个基于HTML5 Canvas技术的交互式教学工具，模拟了经典的三棱镜色散实验。它不仅能动态展示白光分解的全过程，还允许您通过调节各种参数来探索物理规律，将抽象的物理概念转化为直观的视觉体验。

### 二、主要功能

1.  **动态演示**
    *   **完整动画**：一键播放白光从入射、折射到最终形成彩色光谱的完整过程。
    *   **分步学习**：将复杂的色散过程分解为五个关键步骤，便于逐一理解和掌握：
        *   **步骤1：白光入射** - 观察白光以特定角度射向三棱镜。
        *   **步骤2：第一次折射** - 观察光在棱镜第一个界面发生的折射，理解折射角的变化。
        *   **步骤3：棱镜内传播** - 观察不同色光在棱镜内因速度不同而开始分离。
        *   **步骤4：第二次折射** - 观察光在棱镜第二个界面再次折射，分离被放大。
        *   **步骤5：形成光谱** - 观察七色光完全分开，在屏幕上形成清晰的可见光谱。

2.  **实验探索**
    *   **调节入射角**：使用滑块改变白光射向棱镜的角度，观察光谱位置和宽度的变化。
    *   **改变棱镜形状**：调节棱镜顶角大小，探索几何形状对色散效果的影响。
    *   **切换光源**：在“白光”、“红光”、“紫光”之间切换，直观对比复合光与单色光通过棱镜时的不同行为（白光散开，单色光仅偏折）。
    *   **控制动画速度**：加快或减慢动画播放速度，便于仔细观察细节。

3.  **信息呈现**
    *   **实时数据显示**：屏幕左上角实时显示当前入射角和实验模式。
    *   **物理量标注**：动画中标注了关键角度，单色光模式下会显示其折射率。
    *   **知识扩展面板**：提供色散原理、生活应用和科学史背景等扩展阅读材料。

### 三、设计特色

*   **符合认知规律**：采用“整体→分解→探索”的设计逻辑，符合学习者的认知路径。
*   **科学的视觉编码**：
    *   **背景**：采用深空暗色背景，最大化突出光线轨迹，模拟暗室环境。
    *   **光线**：白光与七色光使用高区分度的颜色，并带有光晕效果，增强质感。
    *   **棱镜**：采用半透明填充和描边，呈现玻璃的透明质感，内部光路隐约可见。
*   **即时反馈的交互**：所有参数调节均能实时反映在动画中，帮助建立直观的因果关系。
*   **响应式布局**：适配不同尺寸的屏幕，在电脑、平板等设备上均可获得良好体验。

### 四、教学要点（给教师的建议）

本动画可用于辅助讲解以下核心知识点：

1.  **白光的复合性**：通过分解动画，直观证明白光是由多种单色光混合而成。
2.  **折射定律与折射率**：
    *   展示光从空气进入玻璃（第一次折射）和从玻璃进入空气（第二次折射）的偏折。
    *   **关键对比**：切换到单色光（红/紫）模式，强调所有光都遵循折射定律，都会偏折。
3.  **色散的根本原因**：
    *   **核心原理**：强调不同色光在**同种介质**中折射率不同（n紫 > n红）。
    *   **动画体现**：在棱镜内部，七色光已开始轻微分离，这正是折射率差异的体现。
4.  **三棱镜的作用**：
    *   解释棱镜的**几何形状**（两面不平行）如何将微小的折射角差异累积、放大，最终形成明显的光谱。
    *   引导学生使用“棱镜顶角”滑块，验证顶角越大，色散效果通常越显著。
5.  **联系生活实际**：
    *   结合“知识扩展”中的内容，引导学生思考彩虹、光盘、钻石火彩等现象背后的色散原理。

### 五、使用建议

1.  **初次学习**：
    *   点击“播放”按钮，观看完整的色散动画，建立整体印象。
    *   点击“分步学习”中的各个步骤按钮，跟随讲解逐步理解每个子过程。
    *   阅读“知识扩展”面板，了解原理与应用。

2.  **深入探究**：
    *   切换到“红光”或“紫光”，观察单色光**只偏折不散开**，理解色散的必要条件是“复合光”+“折射率差异”。
    *   调节“入射角”滑块，观察并总结入射角变化对出射光谱位置的影响。
    *   调节“棱镜顶角”滑块，理解仪器形状对实验现象的影响。

3.  **课堂教学**：
    *   **教师演示**：可连接投影仪，作为课堂引入或原理讲解的动态教具。
    *   **学生活动**：布置探索任务，例如：“如何让光谱变得更宽？”“为什么紫光比红光偏折得更厉害？”让学生通过操作动画寻找答案。
    *   **讨论基点**：利用动画呈现的现象，引导学生进行讨论和推理，构建物理模型。

我们希望这个交互式动画能成为您探索光学世界的有力工具，让抽象的物理概念变得生动有趣，激发对科学的好奇与热爱！

**开始您的色散探索之旅吧！**