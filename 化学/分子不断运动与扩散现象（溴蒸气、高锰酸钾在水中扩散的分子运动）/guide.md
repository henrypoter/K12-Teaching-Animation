# 需求：分子不断运动与扩散现象（溴蒸气、高锰酸钾在水中扩散的分子运动）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中或高中化学初学者。他们需要直观地理解抽象的微观分子运动概念，并将其与宏观的扩散现象（如溴蒸气扩散、高锰酸钾溶解）联系起来。
2.  **核心需求**：
    *   **可视化抽象概念**：学生难以直接观察分子，需要动画将微观粒子的无规则运动、速度、相互作用可视化。
    *   **建立宏-微观联系**：动画需清晰展示宏观扩散现象（颜色变化、区域混合）是由大量微观粒子运动导致的统计结果。
    *   **理解影响因素**：学生需要理解温度、分子质量（模拟为粒子大小/颜色）如何影响扩散速率。
    *   **主动探索与验证**：提供交互控制，让学生通过改变参数（如温度）观察结果，加深理解并满足探究欲。
3.  **潜在难点**：区分“分子运动”本身与“扩散”现象（分子运动导致的结果）；理解为什么粒子运动是无规则的，但扩散整体上是有方向的（从高浓度到低浓度）。

#### 教学设计思路
1.  **核心概念**：
    *   **分子不断运动**：所有物质的分子都在永不停息地做无规则运动。
    *   **扩散现象**：不同物质相互接触时彼此进入对方的现象，是分子运动的宏观表现。
    *   **影响因素**：温度（温度越高，分子运动越剧烈，扩散越快）；分子本身特性（如质量、大小）。
2.  **认知规律（动画流程设计）**：
    *   **从简到繁，从微观到宏观**：
        1.  **起点**：先展示一个隔离的微观场景（如一小块空间内的气体或液体分子），用粒子动画演示无规则的“布朗运动”，建立分子永恒、随机运动的基本图景。
        2.  **引入扩散**：将场景分为两个区域（如左红右蓝），代表两种不同物质。开始时粒子不越过边界，然后允许粒子随机运动穿过边界。引导学生观察：单个粒子的运动是随机的，但大量粒子统计下，会看到颜色（代表物质）从高浓度区向低浓度区逐渐混合，直至均匀——这就是扩散。
        3.  **连接宏观实验**：在微观动画旁或下方，同步展示对应的宏观实验动画（如溴蒸气瓶对瓶扩散、高锰酸钾晶体在水中溶解扩散）。用箭头或半透明叠加等方式，示意宏观现象背后的微观机制。
        4.  **探究对比**：提供控制面板，允许学生运行“常温 vs. 高温”下的扩散对比实验，或“轻分子（溴） vs. 重分子（假设的对比物）”的扩散速率对比，直观感受影响因素。
3.  **交互设计**：
    *   **控制与播放**：提供播放/暂停/重置按钮，让学生控制动画节奏。
    *   **视图切换**：可在“纯微观视图”、“宏微观对比视图”、“纯宏观实验视图”之间切换，适应不同教学阶段。
    *   **参数调节**：通过滑块调节“温度”（控制粒子运动速度）和“粒子大小/质量”（模拟不同物质），实时观察对扩散速率的影响。
    *   **跟踪与高亮**：可点击或框选少数几个粒子，高亮并跟踪其运动轨迹，直观展示运动的“无规则性”。
    *   **数据提示**：鼠标悬停在区域上，显示该区域的“粒子浓度（数量）”或“混合百分比”。
4.  **视觉呈现**：
    *   **粒子设计**：不同物质用不同颜色（如溴分子用红棕色，空气分子用浅灰色，高锰酸钾离子用紫红色，水分子用浅蓝色半透明小圆点）。粒子可带有轻微的光晕或尾迹（可开关），以表现运动感。
    *   **场景分层**：背景为干净的浅色；微观粒子层为主动画区；宏观实验层采用写实简笔画风格（如烧杯、玻璃片、集气瓶）；UI控制层清晰置于一侧或底部。
    *   **动态效果**：粒子碰撞时应有微妙的弹性效果；扩散过程中，区域背景色可以随着粒子混合比例渐变，强化宏观颜色变化效果。
    *   **引导与标注**：关键步骤有文字标签或简短语音提示（如“观察分子无规则运动”、“开始扩散”、“注意高温下扩散更快”）。

#### 配色方案选择
*   **主色调/背景**：采用柔和的浅灰色（#f5f7fa）或极浅的蓝灰色（#f0f8ff）作为画布背景，确保长时间观看不刺眼，并能突出前景元素。
*   **科学可视化配色**：
    *   **溴蒸气分子**：红棕色（#8B4513 或 #A0522D），贴近其宏观蒸汽颜色。
    *   **空气分子（或其他对比气体）**：浅灰色（#D3D3D3），半透明，表示背景存在。
    *   **高锰酸钾离子**：鲜明的紫红色（#8A2BE2 或 #9932CC）。
    *   **水分子**：浅蓝色（#87CEEB），透明度较高（如 alpha=0.3），表示溶剂且不喧宾夺主。
    *   **轨迹与高亮**：高亮粒子用亮黄色（#FFD700），运动轨迹用同色系半透明线条。
    *   **UI控件**：采用中性深蓝色（#2c3e50）或深灰色（#34495e），搭配白色文字，清晰专业。
    *   **文本与提示**：重要标题用深灰色（#2c3e50），说明文字用中灰色（#7f8c8d）。

#### 交互功能列表
1.  **场景选择器**：按钮组，用于在“溴蒸气扩散”、“高锰酸钾溶液扩散”两个主要实验场景间切换。
2.  **视图模式切换**：单选按钮，选择“微观视图”、“宏观视图”或“对比视图”。
3.  **动画控制**：标准的播放/暂停/重置按钮。
4.  **参数调节滑块**：
    *   **温度**：从“低温”到“高温”调节，直接影响所有粒子的平均运动速度。
    *   **粒子大小（质量）**：在特定对比场景下，调节某一类粒子的大小，模拟不同分子质量的影响。
5.  **粒子跟踪开关**：勾选框，开启后，随机或手动选择几个粒子显示其运动轨迹。
6.  **浓度显示开关**：勾选框，开启后，在场景分区上显示实时的粒子数量或浓度百分比。
7.  **速度显示开关**：勾选框，开启后，以粒子颜色深浅或微小矢量线表示其瞬时速度（辅助理解温度影响）。
8.  **教学提示面板**：一个可折叠/展开的区域，显示当前动画步骤的文字说明和关键问题。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>分子运动与扩散现象教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
            min-height: 100vh;
            padding: 20px;
            color: #2c3e50;
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
            border-bottom: 2px solid #eaeff5;
        }
        
        h1 {
            color: #2c3e50;
            font-size: 2.4rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #2c3e50, #4a6491);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 25px;
        }
        
        .animation-area {
            flex: 1;
            min-width: 300px;
            background-color: #f8fafc;
            border-radius: 12px;
            padding: 20px;
            box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.05);
            position: relative;
            overflow: hidden;
        }
        
        .canvas-container {
            width: 100%;
            height: 500px;
            position: relative;
            border-radius: 8px;
            overflow: hidden;
            background-color: #f0f8ff;
            border: 1px solid #dbe7f3;
        }
        
        #mainCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .macro-overlay {
            position: absolute;
            bottom: 20px;
            left: 20px;
            right: 20px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 8px;
            padding: 15px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            border: 1px solid #d1e3ff;
            transition: opacity 0.3s ease;
        }
        
        .controls-panel {
            flex: 0 0 320px;
            background-color: #f8fafc;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
            border: 1px solid #eaeff5;
        }
        
        .control-section {
            margin-bottom: 25px;
            padding-bottom: 20px;
            border-bottom: 1px solid #eaeff5;
        }
        
        .control-section:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        h2 {
            color: #34495e;
            font-size: 1.4rem;
            margin-bottom: 18px;
            display: flex;
            align-items: center;
        }
        
        h2 i {
            margin-right: 10px;
            color: #4a6491;
        }
        
        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        button {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            background-color: #4a6491;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            flex: 1;
            min-width: 120px;
            font-size: 1rem;
        }
        
        button:hover {
            background-color: #3a5379;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        button.primary {
            background-color: #3498db;
        }
        
        button.primary:hover {
            background-color: #2980b9;
        }
        
        button.secondary {
            background-color: #2ecc71;
        }
        
        button.secondary:hover {
            background-color: #27ae60;
        }
        
        button.warning {
            background-color: #e74c3c;
        }
        
        button.warning:hover {
            background-color: #c0392b;
        }
        
        .slider-container {
            margin-bottom: 20px;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-weight: 600;
            color: #2c3e50;
        }
        
        .slider-value {
            color: #3498db;
            font-weight: bold;
        }
        
        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: #dfe7f2;
            outline: none;
            -webkit-appearance: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        
        .checkbox-group {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        
        .checkbox-item {
            display: flex;
            align-items: center;
            cursor: pointer;
        }
        
        .checkbox-item input {
            margin-right: 10px;
            width: 18px;
            height: 18px;
            cursor: pointer;
        }
        
        .checkbox-item label {
            cursor: pointer;
            font-weight: 500;
            color: #2c3e50;
        }
        
        .info-panel {
            background-color: #f0f8ff;
            border-radius: 12px;
            padding: 25px;
            margin-top: 25px;
            border-left: 5px solid #3498db;
        }
        
        .info-panel h3 {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .info-content {
            color: #5a6c7d;
            line-height: 1.7;
            font-size: 1.05rem;
        }
        
        .highlight {
            background-color: rgba(255, 215, 0, 0.2);
            padding: 2px 6px;
            border-radius: 4px;
            font-weight: 600;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            justify-content: center;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            font-size: 0.9rem;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            margin-right: 8px;
            border: 1px solid rgba(0, 0, 0, 0.1);
        }
        
        .status-bar {
            display: flex;
            justify-content: space-between;
            background-color: #f8fafc;
            padding: 12px 20px;
            border-radius: 8px;
            margin-top: 15px;
            font-size: 0.95rem;
            color: #5a6c7d;
            border: 1px solid #eaeff5;
        }
        
        .status-item {
            display: flex;
            flex-direction: column;
        }
        
        .status-value {
            font-weight: bold;
            color: #2c3e50;
            font-size: 1.1rem;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            .controls-panel {
                flex: 1;
            }
            
            .canvas-container {
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>分子运动与扩散现象</h1>
            <p class="subtitle">通过可视化微观粒子运动，理解溴蒸气扩散和高锰酸钾在水中扩散的宏观现象。探索温度、分子大小对扩散速率的影响。</p>
        </header>
        
        <div class="main-content">
            <div class="animation-area">
                <div class="canvas-container">
                    <canvas id="mainCanvas"></canvas>
                    <div class="macro-overlay" id="macroOverlay">
                        <div id="macroDescription">宏观现象：溴蒸气（红棕色）从右侧集气瓶向左侧空气瓶中扩散，最终两瓶颜色均匀。</div>
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #8B4513;"></div>
                        <span>溴分子</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #D3D3D3;"></div>
                        <span>空气分子</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #8A2BE2;"></div>
                        <span>高锰酸钾离子</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #87CEEB; opacity: 0.3;"></div>
                        <span>水分子</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FFD700;"></div>
                        <span>被追踪粒子</span>
                    </div>
                </div>
                
                <div class="status-bar">
                    <div class="status-item">
                        <span>时间进度</span>
                        <span class="status-value" id="timeProgress">0%</span>
                    </div>
                    <div class="status-item">
                        <span>左侧浓度</span>
                        <span class="status-value" id="leftConcentration">100%</span>
                    </div>
                    <div class="status-item">
                        <span>右侧浓度</span>
                        <span class="status-value" id="rightConcentration">0%</span>
                    </div>
                    <div class="status-item">
                        <span>粒子总数</span>
                        <span class="status-value" id="particleCount">200</span>
                    </div>
                </div>
            </div>
            
            <div class="controls-panel">
                <div class="control-section">
                    <h2><i>🧪</i> 实验场景</h2>
                    <div class="button-group">
                        <button id="sceneBromine" class="primary">溴蒸气扩散</button>
                        <button id="scenePermanganate">高锰酸钾扩散</button>
                    </div>
                    
                    <div class="button-group">
                        <button id="viewMicro">微观视图</button>
                        <button id="viewMacro" class="secondary">宏观视图</button>
                        <button id="viewCompare">对比视图</button>
                    </div>
                </div>
                
                <div class="control-section">
                    <h2><i>⏯️</i> 动画控制</h2>
                    <div class="button-group">
                        <button id="playBtn" class="primary">▶ 播放</button>
                        <button id="pauseBtn">⏸ 暂停</button>
                        <button id="resetBtn" class="warning">↺ 重置</button>
                    </div>
                </div>
                
                <div class="control-section">
                    <h2><i>⚙️</i> 参数调节</h2>
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>温度</span>
                            <span class="slider-value" id="tempValue">25°C</span>
                        </div>
                        <input type="range" id="tempSlider" min="0" max="100" value="25">
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>粒子大小（质量）</span>
                            <span class="slider-value" id="sizeValue">中等</span>
                        </div>
                        <input type="range" id="sizeSlider" min="1" max="10" value="5">
                    </div>
                </div>
                
                <div class="control-section">
                    <h2><i>🔍</i> 显示选项</h2>
                    <div class="checkbox-group">
                        <div class="checkbox-item">
                            <input type="checkbox" id="showTraces" checked>
                            <label for="showTraces">显示粒子运动轨迹</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showConcentration">
                            <label for="showConcentration">显示浓度区域</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="trackParticles">
                            <label for="trackParticles">跟踪随机粒子</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showVelocity">
                            <label for="showVelocity">显示速度指示</label>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="info-panel">
            <h3>教学提示</h3>
            <div class="info-content" id="teachingTip">
                <p><span class="highlight">分子不断运动</span>：所有物质的分子都在永不停息地做无规则运动。观察画布中粒子的随机运动路径。</p>
                <p><span class="highlight">扩散现象</span>：不同物质相互接触时彼此进入对方的现象，是分子运动的宏观表现。注意观察颜色如何从高浓度区域向低浓度区域逐渐混合。</p>
                <p>尝试提高温度滑块，观察分子运动速度加快，扩散过程也随之加速。</p>
            </div>
        </div>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('mainCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        
        // 初始调整尺寸
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 动画状态
        let animationId = null;
        let isPlaying = false;
        let currentScene = 'bromine'; // 'bromine' 或 'permanganate'
        let currentView = 'compare'; // 'micro', 'macro', 'compare'
        let animationTime = 0;
        const maxAnimationTime = 300; // 动画总时间（秒模拟）
        
        // 粒子系统
        let particles = [];
        const particleCount = 200;
        let trackedParticles = [];
        
        // 颜色定义
        const colors = {
            bromine: '#8B4513',      // 溴分子 - 红棕色
            air: '#D3D3D3',          // 空气分子 - 浅灰色
            permanganate: '#8A2BE2', // 高锰酸钾离子 - 紫红色
            water: '#87CEEB',        // 水分子 - 浅蓝色
            tracked: '#FFD700',      // 被追踪粒子 - 亮黄色
            trace: 'rgba(255, 215, 0, 0.2)', // 轨迹颜色
            background: '#f0f8ff'    // 背景色
        };
        
        // 参数
        let temperature = 25; // 温度值 (0-100)
        let particleSizeFactor = 5; // 粒子大小因子 (1-10)
        let showTraces = true;
        let showConcentration = false;
        let trackParticles = false;
        let showVelocity = false;
        
        // 粒子类
        class Particle {
            constructor(type, x, y, vx, vy, radius, color) {
                this.type = type; // 'bromine', 'air', 'permanganate', 'water'
                this.x = x;
                this.y = y;
                this.vx = vx;
                this.vy = vy;
                this.radius = radius;
                this.color = color;
                this.originalColor = color;
                this.isTracked = false;
                this.trace = [];
                this.maxTraceLength = 20;
            }
            
            update(deltaTime, temperatureFactor) {
                // 根据温度调整速度
                const speedFactor = 1 + (temperatureFactor - 1) * 0.5;
                this.vx *= speedFactor;
                this.vy *= speedFactor;
                
                // 更新位置
                this.x += this.vx * deltaTime;
                this.y += this.vy * deltaTime;
                
                // 边界碰撞
                const margin = 5;
                if (this.x < margin || this.x > canvas.width - margin) {
                    this.vx = -this.vx;
                    this.x = Math.max(margin, Math.min(canvas.width - margin, this.x));
                }
                if (this.y < margin || this.y > canvas.height - margin) {
                    this.vy = -this.vy;
                    this.y = Math.max(margin, Math.min(canvas.height - margin, this.y));
                }
                
                // 添加轨迹点
                if (this.isTracked && showTraces) {
                    this.trace.push({x: this.x, y: this.y});
                    if (this.trace.length > this.maxTraceLength) {
                        this.trace.shift();
                    }
                }
            }
            
            draw(ctx) {
                // 绘制轨迹
                if (this.isTracked && showTraces && this.trace.length > 1) {
                    ctx.beginPath();
                    ctx.moveTo(this.trace[0].x, this.trace[0].y);
                    for (let i = 1; i < this.trace.length; i++) {
                        ctx.lineTo(this.trace[i].x, this.trace[i].y);
                    }
                    ctx.strokeStyle = colors.trace;
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
                
                // 绘制粒子
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                
                // 根据视图模式调整颜色透明度
                let drawColor = this.color;
                if (currentView === 'macro' && (this.type === 'air' || this.type === 'water')) {
                    // 在宏观视图中，空气和水分子几乎透明
                    drawColor = this.type === 'air' ? 'rgba(211, 211, 211, 0.1)' : 'rgba(135, 206, 235, 0.05)';
                }
                
                ctx.fillStyle = drawColor;
                ctx.fill();
                
                // 如果被追踪，添加高亮环
                if (this.isTracked) {
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius + 3, 0, Math.PI * 2);
                    ctx.strokeStyle = colors.tracked;
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
                
                // 显示速度指示
                if (showVelocity) {
                    const speed = Math.sqrt(this.vx * this.vx + this.vy * this.vy);
                    const alpha = Math.min(0.5, speed / 10);
                    ctx.beginPath();
                    ctx.moveTo(this.x, this.y);
                    ctx.lineTo(this.x + this.vx * 5, this.y + this.vy * 5);
                    ctx.strokeStyle = `rgba(255, 100, 100, ${alpha})`;
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
            }
        }
        
        // 初始化粒子系统
        function initParticles() {
            particles = [];
            trackedParticles = [];
            
            const centerX = canvas.width / 2;
            const isBromineScene = currentScene === 'bromine';
            
            // 根据场景创建粒子
            if (isBromineScene) {
                // 溴蒸气扩散场景：左侧空气，右侧溴蒸气
                for (let i = 0; i < particleCount; i++) {
                    // 空气分子 (左侧)
                    if (i < particleCount * 0.4) {
                        const x = Math.random() * centerX * 0.8;
                        const y = Math.random() * canvas.height * 0.8 + canvas.height * 0.1;
                        const speed = 0.5 + Math.random() * 1;
                        const angle = Math.random() * Math.PI * 2;
                        const vx = Math.cos(angle) * speed;
                        const vy = Math.sin(angle) * speed;
                        const radius = 3 + Math.random() * 2;
                        
                        particles.push(new Particle(
                            'air', x, y, vx, vy, radius, colors.air
                        ));
                    }
                    // 溴分子 (右侧)
                    else {
                        const x = centerX + Math.random() * centerX * 0.8;
                        const y = Math.random() * canvas.height * 0.8 + canvas.height * 0.1;
                        const speed = 0.3 + Math.random() * 0.8;
                        const angle = Math.random() * Math.PI * 2;
                        const vx = Math.cos(angle) * speed;
                        const vy = Math.sin(angle) * speed;
                        const radius = 4 + Math.random() * 3;
                        
                        particles.push(new Particle(
                            'bromine', x, y, vx, vy, radius, colors.bromine
                        ));
                    }
                }
            } else {
                // 高锰酸钾扩散场景：水中高锰酸钾扩散
                for (let i = 0; i < particleCount; i++) {
                    // 水分子 (全区域)
                    if (i < particleCount * 0.7) {
                        const x = Math.random() * canvas.width * 0.9 + canvas.width * 0.05;
                        const y = Math.random() * canvas.height * 0.9 + canvas.height * 0.05;
                        const speed = 0.2 + Math.random() * 0.5;
                        const angle = Math.random() * Math.PI * 2;
                        const vx = Math.cos(angle) * speed;
                        const vy = Math.sin(angle) * speed;
                        const radius = 2 + Math.random() * 2;
                        
                        particles.push(new Particle(
                            'water', x, y, vx, vy, radius, colors.water
                        ));
                    }
                    // 高锰酸钾离子 (初始集中在右侧)
                    else {
                        const x = centerX + Math.random() * centerX * 0.7;
                        const y = Math.random() * canvas.height * 0.8 + canvas.height * 0.1;
                        const speed = 0.4 + Math.random() * 1;
                        const angle = Math.random() * Math.PI * 2;
                        const vx = Math.cos(angle) * speed;
                        const vy = Math.sin(angle) * speed;
                        const radius = 3 + Math.random() * 2;
                        
                        particles.push(new Particle(
                            'permanganate', x, y, vx, vy, radius, colors.permanganate
                        ));
                    }
                }
            }
            
            // 随机选择几个粒子进行追踪
            for (let i = 0; i < 3; i++) {
                const randomIndex = Math.floor(Math.random() * particles.length);
                particles[randomIndex].isTracked = true;
                trackedParticles.push(particles[randomIndex]);
            }
            
            // 根据粒子大小因子调整半径
            updateParticleSizes();
        }
        
        // 更新粒子大小
        function updateParticleSizes() {
            const sizeMultiplier = particleSizeFactor / 5; // 基准值为5
            
            particles.forEach(particle => {
                let baseRadius;
                switch(particle.type) {
                    case 'bromine': baseRadius = 4; break;
                    case 'air': baseRadius = 3; break;
                    case 'permanganate': baseRadius = 3; break;
                    case 'water': baseRadius = 2; break;
                    default: baseRadius = 3;
                }
                particle.radius = baseRadius * sizeMultiplier;
            });
        }
        
        // 绘制宏观实验图示
        function drawMacroExperiment() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const isBromineScene = currentScene === 'bromine';
            
            if (isBromineScene) {
                // 绘制溴蒸气扩散实验装置
                const bottleWidth = 120;
                const bottleHeight = 180;
                const bottleY = centerY - bottleHeight / 2;
                
                // 左侧空气瓶
                ctx.beginPath();
                ctx.rect(centerX - bottleWidth - 150, bottleY, bottleWidth, bottleHeight);
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 右侧溴蒸气瓶
                ctx.beginPath();
                ctx.rect(centerX + 50, bottleY, bottleWidth, bottleHeight);
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 连接管
                ctx.beginPath();
                ctx.rect(centerX - 30, centerY - 10, 60, 20);
                ctx.fillStyle = '#bdc3c7';
                ctx.fill();
                ctx.strokeStyle = '#7f8c8d';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 溴蒸气颜色扩散效果
                const diffusionProgress = Math.min(1, animationTime / maxAnimationTime);
                
                // 左侧瓶颜色（逐渐变深）
                ctx.fillStyle = `rgba(139, 69, 19, ${0.1 + diffusionProgress * 0.4})`;
                ctx.fillRect(centerX - bottleWidth - 150, bottleY, bottleWidth, bottleHeight);
                
                // 右侧瓶颜色（逐渐变浅）
                ctx.fillStyle = `rgba(139, 69, 19, ${0.8 - diffusionProgress * 0.4})`;
                ctx.fillRect(centerX + 50, bottleY, bottleWidth, bottleHeight);
                
                // 标签
                ctx.fillStyle = '#2c3e50';
                ctx.font = '16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('空气', centerX - bottleWidth - 150 + bottleWidth/2, bottleY + bottleHeight + 25);
                ctx.fillText('溴蒸气', centerX + 50 + bottleWidth/2, bottleY + bottleHeight + 25);
                
            } else {
                // 绘制高锰酸钾在水中扩散实验
                const beakerWidth = 200;
                const beakerHeight = 220;
                const beakerX = centerX - beakerWidth / 2;
                const beakerY = centerY - beakerHeight / 2;
                
                // 烧杯轮廓
                ctx.beginPath();
                ctx.moveTo(beakerX, beakerY + beakerHeight);
                ctx.lineTo(beakerX, beakerY + 30);
                ctx.quadraticCurveTo(beakerX, beakerY, beakerX + 20, beakerY);
                ctx.lineTo(beakerX + beakerWidth - 20, beakerY);
                ctx.quadraticCurveTo(beakerX + beakerWidth, beakerY, beakerX + beakerWidth, beakerY + 30);
                ctx.lineTo(beakerX + beakerWidth, beakerY + beakerHeight);
                ctx.lineTo(beakerX, beakerY + beakerHeight);
                ctx.strokeStyle = '#2c3e50';
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 水
                const waterHeight = beakerHeight * 0.8;
                ctx.fillStyle = 'rgba(135, 206, 235, 0.3)';
                ctx.fillRect(beakerX, beakerY + beakerHeight - waterHeight, beakerWidth, waterHeight);
                
                // 高锰酸钾扩散效果
                const diffusionProgress = Math.min(1, animationTime / maxAnimationTime);
                const gradient = ctx.createLinearGradient(beakerX, 0, beakerX + beakerWidth, 0);
                
                // 创建从紫色到无色的渐变来模拟扩散
                gradient.addColorStop(0, `rgba(138, 43, 226, ${0.9 - diffusionProgress * 0.4})`);
                gradient.addColorStop(0.3, `rgba(138, 43, 226, ${0.7 - diffusionProgress * 0.35})`);
                gradient.addColorStop(0.6, `rgba(138, 43, 226, ${0.4 - diffusionProgress * 0.3})`);
                gradient.addColorStop(1, `rgba(138, 43, 226, ${0.1 - diffusionProgress * 0.05})`);
                
                ctx.fillStyle = gradient;
                ctx.fillRect(beakerX, beakerY + beakerHeight - waterHeight, beakerWidth, waterHeight);
                
                // 标签
                ctx.fillStyle = '#2c3e50';
                ctx.font = '16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('高锰酸钾溶液', centerX, beakerY + beakerHeight + 25);
            }
        }
        
        // 绘制浓度区域
        function drawConcentrationAreas() {
            if (!showConcentration) return;
            
            const centerX = canvas.width / 2;
            const isBromineScene = currentScene === 'bromine';
            
            // 计算左侧和右侧的溴/高锰酸钾粒子数量
            let leftCount = 0, rightCount = 0;
            let leftTarget = 0, rightTarget = 0;
            
            particles.forEach(p => {
                if (p.type === (isBromineScene ? 'bromine' : 'permanganate')) {
                    if (p.x < centerX) leftCount++;
                    else rightCount++;
                }
                if (p.x < centerX) leftTarget++;
                else rightTarget++;
            });
            
            const leftConcentration = leftTarget > 0 ? leftCount / leftTarget : 0;
            const rightConcentration = rightTarget > 0 ? rightCount / rightTarget : 0;
            
            // 更新状态显示
            document.getElementById('leftConcentration').textContent = `${Math.round(leftConcentration * 100)}%`;
            document.getElementById('rightConcentration').textContent = `${Math.round(rightConcentration * 100)}%`;
            
            // 绘制左侧浓度区域
            ctx.fillStyle = isBromineScene ? 
                `rgba(139, 69, 19, ${0.1 + leftConcentration * 0.4})` : 
                `rgba(138, 43, 226, ${0.1 + leftConcentration * 0.4})`;
            ctx.fillRect(0, 0, centerX, canvas.height);
            
            // 绘制右侧浓度区域
            ctx.fillStyle = isBromineScene ? 
                `rgba(139, 69, 19, ${0.1 + rightConcentration * 0.4})` : 
                `rgba(138, 43, 226, ${0.1 + rightConcentration * 0.4})`;
            ctx.fillRect(centerX, 0, centerX, canvas.height);
            
            // 绘制分界线
            ctx.beginPath();
            ctx.moveTo(centerX, 0);
            ctx.lineTo(centerX, canvas.height);
            ctx.strokeStyle = '#2c3e50';
            ctx.lineWidth = 2;
            ctx.setLineDash([5, 5]);
            ctx.stroke();
            ctx.setLineDash([]);
        }
        
        // 主动画循环
        function animate(timestamp) {
            if (!lastTimestamp) lastTimestamp = timestamp;
            const deltaTime = (timestamp - lastTimestamp) / 16; // 标准化时间增量
            lastTimestamp = timestamp;
            
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            ctx.fillStyle = colors.background;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 根据视图模式绘制
            if (currentView === 'macro') {
                // 只显示宏观实验
                drawMacroExperiment();
            } else {
                // 显示微观粒子或对比视图
                
                // 绘制浓度区域（如果启用）
                drawConcentrationAreas();
                
                // 更新和绘制所有粒子
                const temperatureFactor = 1 + (temperature - 25) / 75; // 温度影响因子
                
                particles.forEach(particle => {
                    particle.update(deltaTime, temperatureFactor);
                    particle.draw(ctx);
                });
                
                // 如果是对比视图，同时绘制宏观实验
                if (currentView === 'compare') {
                    // 在半透明层上绘制宏观实验
                    ctx.save();
                    ctx.globalAlpha = 0.7;
                    drawMacroExperiment();
                    ctx.restore();
                }
            }
            
            // 更新动画时间
            if (isPlaying) {
                animationTime += deltaTime * 0.5;
                if (animationTime > maxAnimationTime) {
                    animationTime = maxAnimationTime;
                }
                
                // 更新进度显示
                const progressPercent = Math.round((animationTime / maxAnimationTime) * 100);
                document.getElementById('timeProgress').textContent = `${progressPercent}%`;
            }
            
            // 继续动画循环
            if (isPlaying) {
                animationId = requestAnimationFrame(animate);
            }
        }
        
        let lastTimestamp = 0;
        
        // 开始动画
        function startAnimation() {
            if (!isPlaying) {
                isPlaying = true;
                lastTimestamp = 0;
                animationId = requestAnimationFrame(animate);
                updatePlayButton();
            }
        }
        
        // 暂停动画
        function pauseAnimation() {
            isPlaying = false;
            if (animationId) {
                cancelAnimationFrame(animationId);
                animationId = null;
            }
            updatePlayButton();
        }
        
        // 重置动画
        function resetAnimation() {
            pauseAnimation();
            animationTime = 0;
            initParticles();
            document.getElementById('timeProgress').textContent = '0
<!--检测到代码截断，自动续写中...-->
%';
            document.getElementById('leftConcentration').textContent = '100%';
            document.getElementById('rightConcentration').textContent = '0%';
            
            // 更新教学提示
            updateTeachingTip();
            
            // 立即绘制一帧
            lastTimestamp = 0;
            animate(performance.now());
        }
        
        // 更新播放按钮状态
        function updatePlayButton() {
            const playBtn = document.getElementById('playBtn');
            if (isPlaying) {
                playBtn.innerHTML = '⏸ 暂停';
                playBtn.classList.add('warning');
                playBtn.classList.remove('primary');
            } else {
                playBtn.innerHTML = '▶ 播放';
                playBtn.classList.remove('warning');
                playBtn.classList.add('primary');
            }
        }
        
        // 更新教学提示
        function updateTeachingTip() {
            const tipElement = document.getElementById('teachingTip');
            const macroDescription = document.getElementById('macroDescription');
            
            if (currentScene === 'bromine') {
                macroDescription.textContent = '宏观现象：溴蒸气（红棕色）从右侧集气瓶向左侧空气瓶中扩散，最终两瓶颜色均匀。';
                
                tipElement.innerHTML = `
                    <p><span class="highlight">分子不断运动</span>：所有物质的分子都在永不停息地做无规则运动。观察画布中粒子的随机运动路径。</p>
                    <p><span class="highlight">扩散现象</span>：不同物质相互接触时彼此进入对方的现象，是分子运动的宏观表现。注意观察颜色如何从高浓度区域向低浓度区域逐渐混合。</p>
                    <p><span class="highlight">影响因素</span>：尝试提高温度滑块，观察分子运动速度加快，扩散过程也随之加速。调整粒子大小模拟不同分子质量的影响。</p>
                `;
            } else {
                macroDescription.textContent = '宏观现象：高锰酸钾晶体在水中溶解，紫红色从晶体周围逐渐向整个烧杯扩散，最终溶液颜色均匀。';
                
                tipElement.innerHTML = `
                    <p><span class="highlight">溶解与扩散</span>：高锰酸钾晶体中的离子进入水中，通过水分子的间隙扩散到整个溶液。</p>
                    <p><span class="highlight">布朗运动</span>：水分子和溶质离子都在做无规则运动，相互碰撞导致扩散发生。</p>
                    <p><span class="highlight">温度的影响</span>：提高温度会使水分子运动加剧，加速高锰酸钾离子的扩散过程。</p>
                    <p>注意观察：半透明的蓝色小点代表水分子，紫红色点代表高锰酸钾离子。</p>
                `;
            }
        }
        
        // 切换场景
        function switchScene(scene) {
            currentScene = scene;
            
            // 更新按钮状态
            document.getElementById('sceneBromine').classList.toggle('primary', scene === 'bromine');
            document.getElementById('scenePermanganate').classList.toggle('primary', scene === 'permanganate');
            
            // 更新粒子数量显示
            const count = scene === 'bromine' ? 200 : 200;
            document.getElementById('particleCount').textContent = count;
            
            // 重置动画
            resetAnimation();
        }
        
        // 切换视图
        function switchView(view) {
            currentView = view;
            
            // 更新按钮状态
            document.getElementById('viewMicro').classList.toggle('secondary', view === 'micro');
            document.getElementById('viewMacro').classList.toggle('secondary', view === 'macro');
            document.getElementById('viewCompare').classList.toggle('secondary', view === 'compare');
            
            // 显示/隐藏宏观覆盖层
            const macroOverlay = document.getElementById('macroOverlay');
            macroOverlay.style.opacity = (view === 'macro' || view === 'compare') ? '1' : '0';
            
            // 立即重绘
            lastTimestamp = 0;
            animate(performance.now());
        }
        
        // 事件监听器设置
        function setupEventListeners() {
            // 场景切换按钮
            document.getElementById('sceneBromine').addEventListener('click', () => switchScene('bromine'));
            document.getElementById('scenePermanganate').addEventListener('click', () => switchScene('permanganate'));
            
            // 视图切换按钮
            document.getElementById('viewMicro').addEventListener('click', () => switchView('micro'));
            document.getElementById('viewMacro').addEventListener('click', () => switchView('macro'));
            document.getElementById('viewCompare').addEventListener('click', () => switchView('compare'));
            
            // 动画控制按钮
            document.getElementById('playBtn').addEventListener('click', () => {
                if (isPlaying) {
                    pauseAnimation();
                } else {
                    startAnimation();
                }
            });
            document.getElementById('pauseBtn').addEventListener('click', pauseAnimation);
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            
            // 温度滑块
            const tempSlider = document.getElementById('tempSlider');
            const tempValue = document.getElementById('tempValue');
            
            tempSlider.addEventListener('input', function() {
                temperature = parseInt(this.value);
                tempValue.textContent = `${temperature}°C`;
                
                // 如果动画正在播放，温度变化会立即生效
                if (isPlaying) {
                    lastTimestamp = 0;
                }
            });
            
            // 粒子大小滑块
            const sizeSlider = document.getElementById('sizeSlider');
            const sizeValue = document.getElementById('sizeValue');
            
            sizeSlider.addEventListener('input', function() {
                particleSizeFactor = parseInt(this.value);
                
                // 更新显示值
                if (particleSizeFactor <= 3) sizeValue.textContent = '小';
                else if (particleSizeFactor <= 7) sizeValue.textContent = '中等';
                else sizeValue.textContent = '大';
                
                // 更新粒子大小
                updateParticleSizes();
                
                // 立即重绘
                lastTimestamp = 0;
                animate(performance.now());
            });
            
            // 显示选项复选框
            document.getElementById('showTraces').addEventListener('change', function() {
                showTraces = this.checked;
                lastTimestamp = 0;
                animate(performance.now());
            });
            
            document.getElementById('showConcentration').addEventListener('change', function() {
                showConcentration = this.checked;
                lastTimestamp = 0;
                animate(performance.now());
            });
            
            document.getElementById('trackParticles').addEventListener('change', function() {
                trackParticles = this.checked;
                
                // 更新粒子的追踪状态
                trackedParticles.forEach(p => p.isTracked = trackParticles);
                
                lastTimestamp = 0;
                animate(performance.now());
            });
            
            document.getElementById('showVelocity').addEventListener('change', function() {
                showVelocity = this.checked;
                lastTimestamp = 0;
                animate(performance.now());
            });
            
            // 点击Canvas可以手动追踪粒子
            canvas.addEventListener('click', function(event) {
                if (currentView === 'macro') return; // 宏观视图下不追踪
                
                const rect = canvas.getBoundingClientRect();
                const x = event.clientX - rect.left;
                const y = event.clientY - rect.top;
                
                // 寻找点击位置附近的粒子
                let closestParticle = null;
                let closestDistance = 20; // 最大点击距离
                
                particles.forEach(particle => {
                    const distance = Math.sqrt(
                        Math.pow(particle.x - x, 2) + Math.pow(particle.y - y, 2)
                    );
                    
                    if (distance < closestDistance && distance < particle.radius + 10) {
                        closestDistance = distance;
                        closestParticle = particle;
                    }
                });
                
                // 如果找到粒子，切换其追踪状态
                if (closestParticle) {
                    closestParticle.isTracked = !closestParticle.isTracked;
                    
                    // 更新追踪粒子列表
                    if (closestParticle.isTracked && !trackedParticles.includes(closestParticle)) {
                        trackedParticles.push(closestParticle);
                    } else if (!closestParticle.isTracked) {
                        const index = trackedParticles.indexOf(closestParticle);
                        if (index > -1) trackedParticles.splice(index, 1);
                    }
                    
                    // 更新复选框状态
                    document.getElementById('trackParticles').checked = trackedParticles.length > 0;
                    trackParticles = trackedParticles.length > 0;
                    
                    lastTimestamp = 0;
                    animate(performance.now());
                }
            });
        }
        
        // 初始化函数
        function init() {
            // 初始化Canvas
            resizeCanvas();
            
            // 初始化粒子系统
            initParticles();
            
            // 设置事件监听器
            setupEventListeners();
            
            // 设置初始视图
            switchView('compare');
            
            // 设置初始场景
            switchScene('bromine');
            
            // 绘制初始帧
            lastTimestamp = 0;
            animate(performance.now());
            
            // 更新教学提示
            updateTeachingTip();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
        
        // 防止右键菜单
        canvas.addEventListener('contextmenu', function(e) {
            e.preventDefault();
            return false;
        });
        
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 《分子运动与扩散现象》交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过可视化手段，帮助您直观理解“分子不断运动”与“扩散现象”这两个核心的微观科学概念。无论您是教师、学生还是科学爱好者，本指南将帮助您充分利用动画的所有功能，获得最佳的学习与教学体验。

---

### 一、 功能说明

本动画模拟了两种经典的扩散实验：
1.  **溴蒸气扩散**：模拟红棕色的溴蒸气分子从高浓度区域（右侧集气瓶）向低浓度区域（左侧空气瓶）扩散的过程。
2.  **高锰酸钾溶液扩散**：模拟紫红色的高锰酸钾离子在水中溶解并从晶体周围向整个溶液扩散的过程。

动画通过**微观粒子模拟**与**宏观实验图示**相结合的方式，清晰展示了宏观现象背后的微观机制——即大量分子做无规则运动所导致的统计结果。

---

### 二、 主要功能

#### 1. 场景与视图控制
*   **实验场景切换**：在“溴蒸气扩散”和“高锰酸钾扩散”两个经典实验间一键切换。
*   **视图模式切换**：
    *   **微观视图**：专注于观察分子（粒子）的无规则运动与相互作用。
    *   **宏观视图**：展示实验装置的简化图示，观察颜色变化的宏观过程。
    *   **对比视图（推荐）**：同时显示微观粒子运动与宏观实验现象，建立宏-微观联系。

#### 2. 动画控制
*   **播放/暂停/重置**：完全控制动画的进程，便于分步讲解或重复观察关键阶段。

#### 3. 参数调节与探究
*   **温度调节滑块**：实时调整系统“温度”。观察温度升高如何加剧分子运动，从而显著**加快扩散速率**。这是探究“温度对扩散影响”的核心工具。
*   **粒子大小（质量）调节滑块**：通过改变粒子大小，模拟不同分子质量对运动速度的影响。通常，质量较小的分子扩散更快。

#### 4. 可视化增强工具
*   **显示粒子运动轨迹**：勾选后，被追踪的粒子会留下运动路径，直观展示其运动的**无规则性（布朗运动）**。
*   **显示浓度区域**：以半透明色块显示左右区域的物质浓度，量化展示扩散过程中浓度梯度的变化。
*   **跟踪随机粒子**：自动高亮并跟踪几个随机粒子，聚焦于个体行为。
*   **显示速度指示**：用短线表示粒子的瞬时速度方向和大小，帮助理解温度与速度的关系。
*   **点击追踪**：在微观或对比视图下，可直接点击画布上的任意粒子，手动将其标记为追踪对象。

---

### 三、 设计特色

1.  **双重视角，建立联系**：“对比视图”是本动画的核心教学设计，它巧妙地将不可见的微观运动与可见的宏观现象并置，有效帮助学生跨越认知鸿沟，理解“宏观现象是微观运动的统计结果”。
2.  **科学配色，直观清晰**：
    *   溴分子采用**红棕色**，贴近其实物颜色。
    *   高锰酸钾离子采用**紫红色**，与实验现象一致。
    *   空气和水分子采用**浅灰**和**浅蓝**半透明显示，既表明其存在，又不喧宾夺主。
3.  **实时交互，探究驱动**：所有参数（温度、粒子大小）的调节都能**即时反馈**在动画中，鼓励学生提出假设（“如果温度升高会怎样？”）并立即验证，培养科学探究思维。
4.  **状态反馈，量化感知**：顶部的状态栏实时显示时间进度、两侧浓度百分比和粒子总数，将过程量化，使抽象概念变得具体可测。
5.  **自适应界面**：界面布局会根据屏幕大小自动调整，确保在电脑、平板等多种设备上都能获得良好体验。

---

### 四、 教学要点与建议流程

#### 针对教师的教学建议：
**引入阶段**：
1.  使用“宏观视图”播放“溴蒸气扩散”动画，向学生展示熟悉的实验现象，提出问题：“为什么溴蒸气能进入空气瓶中？”
2.  引导学生猜想原因，引出“分子运动”的假说。

**探究核心概念阶段**：
3.  切换到“**对比视图**”，点击“重置”后“播放”。指导学生同时观察：
    *   **微观侧**：红棕色粒子（溴分子）和浅灰色粒子（空气分子）都在做无规则的、朝向各个方向的运动。
    *   **宏观侧**：右侧瓶颜色逐渐变浅，左侧瓶颜色逐渐变深。
4.  提出关键问题：“单个分子的运动方向是随机的，为什么整体上我们看到溴分子向左扩散？” 引导学生思考并理解 **“扩散的方向性（从高浓度到低浓度）是大量分子无规则运动产生的统计规律”**。
5.  开启“**跟踪随机粒子**”和“**显示轨迹**”功能，让学生观察几个代表性分子的运动路径，深刻理解“无规则运动”的含义。

**深化与拓展阶段**：
6.  **探究影响因素**：
    *   **温度**：将温度滑块从25°C逐步提高到80°C，然后重置并播放动画。让学生对比观察扩散速度的显著差异，总结结论。
    *   **粒子质量**：在“高锰酸钾”场景中，分别将粒子大小设为“小”、“中”、“大”进行对比实验，讨论分子质量对运动速度的影响。
7.  **切换场景**：切换到“高锰酸钾在水中扩散”场景，重复上述观察和探究过程。引导学生比较气体扩散与液体扩散速度的差异，并思考原因。

**总结与评估**：
8.  回到“对比视图”，暂停在扩散过程中的某一时刻。让学生根据状态栏的浓度数据，预测接下来的变化。
9.  鼓励学生利用“点击追踪”功能，自行探索他们感兴趣的粒子。

#### 针对学生的自学建议：
*   **按序探索**：建议先使用默认设置（对比视图、溴蒸气场景）完整观看一遍动画，建立整体印象。
*   **大胆尝试**：不要害怕点击各个按钮和滑块。改变参数后，点击“重置”和“播放”观察变化，这是你发现规律的过程。
*   **关注提示**：画面下方的“教学提示”面板会根据你的操作提供关键知识点的解释，请随时阅读。
*   **回答自测**：观看后，尝试向自己或他人解释：什么是分子运动？什么是扩散？为什么加热能加快扩散？

---

### 五、 使用建议

1.  **浏览器**：建议使用最新版本的 Chrome、Edge、Firefox 或 Safari 浏览器，以获得最佳性能和兼容性。
2.  **课堂演示**：教师在全班演示时，可连接投影仪，并使用“暂停”功能在关键节点进行讲解。利用“重置”功能进行对比实验。
3.  **小组学习**：学生可以2-3人一组，共同操作动画，讨论观察到的现象，并完成相关的探究任务单。
4.  **网络环境**：本动画为单HTML文件，无需网络连接即可运行，方便在各种环境下使用。

希望这个充满交互与探索的工具，能点燃您或您的学生对微观世界的好奇心，让抽象的分子理论变得生动而深刻！祝您探索愉快！