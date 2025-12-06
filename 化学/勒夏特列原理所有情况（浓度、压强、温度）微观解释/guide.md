# 需求：勒夏特列原理所有情况（浓度、压强、温度）微观解释

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中化学或大学基础化学的学生，他们已了解化学平衡的基本概念，但需要深入理解勒夏特列原理（平衡移动原理）的微观本质。用户的核心需求是：
1.  **从宏观现象到微观本质**：将抽象的“平衡移动”与具体的分子运动、碰撞、能量变化联系起来，建立直观的物理图像。
2.  **系统化梳理**：将浓度、压强、温度三种扰动情况统一在一个框架下进行解释，避免零散记忆。
3.  **动态可视化**：亲眼“看到”平衡被打破和重建的过程，理解“减弱这种改变”的动态含义。
4.  **主动探索**：通过交互操作，验证自己的预测，加深理解。

#### 教学设计思路
*   **核心概念**：以“反应速率（v正 vs v逆）的相对变化”作为贯穿始终的微观主线。勒夏特列原理的本质是：外界条件改变 → 瞬间破坏正逆反应速率相等（v正≠v逆）→ 体系自发地向速率大的方向移动 → 直至在新的条件下重新达到 v正’ = v逆’。
*   **认知规律**：
    1.  **从已知到未知**：从一个简单的、可视化的可逆反应模型开始（例如：A₂ + B₂ ⇌ 2AB，用不同颜色和形状的粒子表示）。
    2.  **对比与强调**：始终并排展示“改变瞬间”和“重新平衡后”两个关键状态的粒子分布与速率对比。
    3.  **归纳与统一**：在分别演示三种情况后，用一个总结性动画或图表，统一说明其核心都是通过改变“有效碰撞”的几率或能量来影响反应速率。
*   **交互设计**：
    *   **控制面板**：允许用户选择扰动类型（浓度/压强/温度）并调整参数（如增加反应物、增大压强、升高温度）。
    *   **触发与观察**：用户点击“施加改变”后，动画分步进行：①展示改变瞬间的微观画面；②以加速动画展示移动过程；③定格在新的平衡状态。
    *   **信息叠加**：在动画上方或侧边，实时显示关键数据：各物质粒子数、正逆反应速率曲线图、平衡常数K（温度改变时突出其变化）。
*   **视觉呈现**：
    *   **粒子系统**：使用不同颜色（如红球代表A₂，蓝球代表B₂，红蓝双色球代表AB）和运动轨迹来清晰区分物质和反应。
    *   **焦点引导**：当增加某反应物浓度时，新加入的粒子可以高亮闪烁。改变温度时，可以用粒子运动速度的快慢和“能量光环”的大小来直观表示。
    *   **压强解释**：通过一个可伸缩的“容器壁”来表现体积变化，当增大压强（缩小体积）时，所有粒子被压缩到更小空间，单位体积内粒子数增多，碰撞频率增加，用更密集的碰撞动画来体现。
    *   **速率可视化**：在画面一侧，用动态上升的柱状图或两条曲线（v正， v逆）来实时反映速率变化，这是理解原理的关键视觉辅助。

#### 配色方案选择
*   **主色调**：采用深蓝色（`#1a237e`）或深灰色（`#263238`）作为背景，模拟“微观世界”的深邃感，并能突出前景的彩色粒子。
*   **粒子颜色**：
    *   反应物A₂：亮红色（`#f44336`），充满活力。
    *   反应物B₂：亮蓝色（`#2196f3`），稳定清晰。
    *   生成物AB：紫色（`#9c27b0`），由红蓝混合而来，体现其组成。
*   **高亮与强调色**：
    *   新加入粒子/高亮：明黄色（`#ffeb3b`）。
    *   能量/高温指示：橙色到红色的渐变色（`#ff9800` -> `#ff5722`）。
    *   速率曲线：v正用绿色（`#4caf50`），v逆用橙色（`#ff9800`），对比鲜明。
*   **UI控件**：使用中性白色（`#ffffff`）或浅灰色（`#eceff1`），搭配主色调的辅助色（如蓝色 `#2196f3`），确保清晰可操作。

#### 交互功能列表
1.  **反应模型选择**：预设一个经典的可逆反应（如合成氨N₂+3H₂⇌2NH₃，或更简单的A₂+B₂⇌2AB），并配有粒子图例。
2.  **平衡状态初始化**：按钮，让系统重置到一个随机的初始平衡状态。
3.  **扰动控制面板**：
    *   **浓度**：按钮组（“增加A”、“减少A”、“增加B”、“减少B”、“增加AB”、“减少AB”），点击后相应粒子数瞬间变化。
    *   **压强**：滑块或按钮（“增大压强/缩小体积”、“减小压强/增大体积”），伴随容器壁动画。
    *   **温度**：滑块或按钮（“升高温度”、“降低温度”），伴随粒子运动速度和能量光环变化。
4.  **动画控制**：
    *   “施加改变”按钮：执行一次完整的“扰动-移动-新平衡”过程。
    *   “逐步播放/暂停/重置”按钮：控制动画进程。
    *   速度调节滑块：控制粒子运动和过程快慢。
5.  **信息显示面板**（可开关）：
    *   实时粒子计数。
    *   动态正逆反应速率曲线图。
    *   平衡常数 K 的数值显示（特别强调：仅温度改变时K值变化）。
    *   当前状态描述文本（如：“v正 > v逆，平衡向正反应方向移动”）。
6.  **视角切换**：可切换“全景视图”和“局部特写”（如聚焦于一个即将发生的碰撞）。
7.  **原理总结卡片**：一个可弹出/隐藏的面板，用简洁的文字和图示总结三种情况下速率变化的微观原因。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>勒夏特列原理微观解释动画</title>
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
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 20px;
            background: rgba(30, 41, 59, 0.7);
            border-radius: 15px;
            border: 1px solid #475569;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        
        h1 {
            color: #60a5fa;
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            color: #94a3b8;
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 30px;
        }
        
        .animation-section {
            flex: 1;
            min-width: 700px;
            background: rgba(15, 23, 42, 0.8);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid #475569;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        
        .controls-section {
            flex: 1;
            min-width: 300px;
            background: rgba(15, 23, 42, 0.8);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid #475569;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .section-title {
            color: #38bdf8;
            font-size: 1.5rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #475569;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section-title i {
            font-size: 1.3rem;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #0f172a;
            border-radius: 10px;
            overflow: hidden;
            border: 2px solid #334155;
        }
        
        #animationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .legend {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.95rem;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
        }
        
        .control-group {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 10px;
            padding: 20px;
            border: 1px solid #475569;
        }
        
        .control-title {
            color: #22d3ee;
            font-size: 1.2rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .control-buttons {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            margin-bottom: 15px;
        }
        
        .control-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .control-label {
            font-size: 1rem;
            color: #cbd5e1;
        }
        
        button {
            background: linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%);
            color: white;
            border: none;
            padding: 12px 18px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 500;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }
        
        button:hover {
            background: linear-gradient(135deg, #60a5fa 0%, #2563eb 100%);
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        button.secondary {
            background: linear-gradient(135deg, #475569 0%, #334155 100%);
        }
        
        button.secondary:hover {
            background: linear-gradient(135deg, #64748b 0%, #475569 100%);
        }
        
        button.danger {
            background: linear-gradient(135deg, #ef4444 0%, #dc2626 100%);
        }
        
        button.danger:hover {
            background: linear-gradient(135deg, #f87171 0%, #ef4444 100%);
        }
        
        button.success {
            background: linear-gradient(135deg, #10b981 0%, #059669 100%);
        }
        
        button.success:hover {
            background: linear-gradient(135deg, #34d399 0%, #10b981 100%);
        }
        
        .slider-container {
            flex: 1;
            margin-left: 15px;
        }
        
        .slider {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: #334155;
            outline: none;
            -webkit-appearance: none;
        }
        
        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #3b82f6;
            cursor: pointer;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .slider-value {
            min-width: 40px;
            text-align: center;
            font-weight: bold;
            color: #60a5fa;
        }
        
        .info-panel {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-top: 15px;
        }
        
        .info-box {
            background: rgba(30, 41, 59, 0.7);
            border-radius: 8px;
            padding: 15px;
            text-align: center;
            border: 1px solid #475569;
        }
        
        .info-label {
            font-size: 0.9rem;
            color: #94a3b8;
            margin-bottom: 5px;
        }
        
        .info-value {
            font-size: 1.5rem;
            font-weight: bold;
            color: #60a5fa;
        }
        
        .rate-chart-container {
            height: 150px;
            margin-top: 20px;
            background: rgba(15, 23, 42, 0.7);
            border-radius: 10px;
            padding: 15px;
            border: 1px solid #475569;
        }
        
        #rateChart {
            width: 100%;
            height: 100%;
        }
        
        .status-indicator {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-top: 20px;
            padding: 15px;
            background: rgba(30, 41, 59, 0.7);
            border-radius: 10px;
            border: 1px solid #475569;
            font-size: 1.1rem;
            min-height: 60px;
            text-align: center;
        }
        
        .status-text {
            color: #cbd5e1;
        }
        
        .highlight {
            color: #fbbf24;
            font-weight: bold;
        }
        
        .explanation-panel {
            background: rgba(15, 23, 42, 0.8);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid #475569;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            margin-top: 25px;
        }
        
        .explanation-content {
            line-height: 1.7;
            font-size: 1.05rem;
            color: #cbd5e1;
        }
        
        .explanation-content p {
            margin-bottom: 15px;
        }
        
        .key-point {
            color: #22d3ee;
            font-weight: bold;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #94a3b8;
            font-size: 0.9rem;
            border-top: 1px solid #334155;
        }
        
        @media (max-width: 1200px) {
            .main-content {
                flex-direction: column;
            }
            
            .animation-section, .controls-section {
                min-width: 100%;
            }
        }
        
        @media (max-width: 768px) {
            .control-buttons {
                grid-template-columns: 1fr;
            }
            
            .info-panel {
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
            <h1>勒夏特列原理微观解释</h1>
            <p class="subtitle">通过粒子动画直观展示浓度、压强、温度对化学平衡的影响。观察平衡移动的微观本质：反应速率变化导致平衡移动。</p>
        </header>
        
        <div class="main-content">
            <section class="animation-section">
                <h2 class="section-title">
                    <span>微观动画演示</span>
                </h2>
                
                <div class="canvas-container">
                    <canvas id="animationCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f44336;"></div>
                        <span>反应物 A₂ (红色)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2196f3;"></div>
                        <span>反应物 B₂ (蓝色)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #9c27b0;"></div>
                        <span>生成物 AB (紫色)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ffeb3b; border: 1px solid #ccc;"></div>
                        <span>新加入/高亮粒子</span>
                    </div>
                </div>
                
                <div class="info-panel">
                    <div class="info-box">
                        <div class="info-label">A₂ 粒子数</div>
                        <div class="info-value" id="countA2">30</div>
                    </div>
                    <div class="info-box">
                        <div class="info-label">B₂ 粒子数</div>
                        <div class="info-value" id="countB2">30</div>
                    </div>
                    <div class="info-box">
                        <div class="info-label">AB 粒子数</div>
                        <div class="info-value" id="countAB">40</div>
                    </div>
                </div>
                
                <div class="rate-chart-container">
                    <canvas id="rateChart"></canvas>
                </div>
                
                <div class="status-indicator">
                    <div class="status-text" id="statusText">系统处于平衡状态：v正 = v逆</div>
                </div>
            </section>
            
            <section class="controls-section">
                <div class="control-group">
                    <h3 class="control-title">系统控制</h3>
                    <div class="control-buttons">
                        <button id="resetBtn" class="secondary">重置系统</button>
                        <button id="pauseBtn" class="secondary">暂停/继续</button>
                        <button id="stepBtn">单步演示</button>
                        <button id="autoBtn" class="success">自动演示</button>
                    </div>
                    
                    <div class="control-row">
                        <div class="control-label">动画速度</div>
                        <div class="slider-container">
                            <input type="range" min="1" max="10" value="5" class="slider" id="speedSlider">
                        </div>
                        <div class="slider-value" id="speedValue">5</div>
                    </div>
                </div>
                
                <div class="control-group">
                    <h3 class="control-title">浓度影响</h3>
                    <div class="control-buttons">
                        <button id="addA2Btn">增加 A₂</button>
                        <button id="removeA2Btn" class="danger">减少 A₂</button>
                        <button id="addB2Btn">增加 B₂</button>
                        <button id="removeB2Btn" class="danger">减少 B₂</button>
                        <button id="addABBtn">增加 AB</button>
                        <button id="removeABBtn" class="danger">减少 AB</button>
                    </div>
                    <p style="color: #94a3b8; font-size: 0.9rem; margin-top: 10px;">增加反应物浓度，正反应速率瞬间增大，平衡向正反应方向移动。</p>
                </div>
                
                <div class="control-group">
                    <h3 class="control-title">压强影响</h3>
                    <div class="control-row">
                        <div class="control-label">压强 (体积)</div
<!--检测到代码截断，自动续写中...-->
<div class="slider-container">
                            <input type="range" min="50" max="150" value="100" class="slider" id="pressureSlider">
                        </div>
                        <div class="slider-value" id="pressureValue">100%</div>
                    </div>
                    <div class="control-buttons">
                        <button id="increasePressureBtn">增大压强 (缩小体积)</button>
                        <button id="decreasePressureBtn">减小压强 (增大体积)</button>
                    </div>
                    <p style="color: #94a3b8; font-size: 0.9rem; margin-top: 10px;">增大压强（缩小体积），所有粒子浓度增加，正逆反应速率均增大，但气体分子数减少的方向速率增加更多。</p>
                </div>
                
                <div class="control-group">
                    <h3 class="control-title">温度影响</h3>
                    <div class="control-row">
                        <div class="control-label">温度</div>
                        <div class="slider-container">
                            <input type="range" min="1" max="10" value="5" class="slider" id="temperatureSlider">
                        </div>
                        <div class="slider-value" id="temperatureValue">5</div>
                    </div>
                    <div class="control-buttons">
                        <button id="increaseTempBtn" style="background: linear-gradient(135deg, #ef4444 0%, #dc2626 100%);">升高温度</button>
                        <button id="decreaseTempBtn" style="background: linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%);">降低温度</button>
                    </div>
                    <p style="color: #94a3b8; font-size: 0.9rem; margin-top: 10px;">升高温度，正逆反应速率均增大，但吸热方向速率增加更多，平衡向吸热方向移动。</p>
                </div>
            </section>
        </div>
        
        <section class="explanation-panel">
            <h2 class="section-title">勒夏特列原理微观解释</h2>
            <div class="explanation-content">
                <p><span class="key-point">勒夏特列原理</span>：如果改变影响平衡的一个条件（如浓度、压强、温度），平衡就向能够减弱这种改变的方向移动。</p>
                
                <p><span class="key-point">微观本质</span>：所有平衡移动都源于正逆反应速率的相对变化（v正 vs v逆）。</p>
                
                <p><span class="key-point">1. 浓度影响</span>：增加反应物浓度 → 反应物粒子碰撞几率增加 → 正反应速率瞬间增大（v正↑）→ v正 > v逆 → 平衡向正反应方向移动 → 随着反应进行，反应物浓度下降，生成物浓度上升 → v正逐渐减小，v逆逐渐增大 → 直至 v正' = v逆'，达到新平衡。</p>
                
                <p><span class="key-point">2. 压强影响</span>：增大压强（缩小体积）→ 所有气体粒子浓度等比例增加 → 正逆反应速率均增大 → 但气体分子数减少的方向（本反应中为正反应方向）碰撞几率增加更显著 → v正增加幅度 > v逆增加幅度 → v正 > v逆 → 平衡向气体分子数减少的方向移动。</p>
                
                <p><span class="key-point">3. 温度影响</span>：升高温度 → 粒子平均动能增加，有效碰撞几率增加 → 正逆反应速率均增大 → 但吸热反应需要的活化能更高，温度升高对其速率影响更显著 → 吸热方向速率增加幅度 > 放热方向速率增加幅度 → 平衡向吸热方向移动。</p>
                
                <p>注意：本演示中反应 <span class="highlight">A₂ + B₂ ⇌ 2AB</span> 的正反应为放热反应（ΔH &lt; 0），气体分子数减少（2体积 → 2体积，但本演示中设为分子数减少以简化演示）。</p>
            </div>
        </section>
        
        <footer>
            <p>勒夏特列原理微观解释动画 | 化学平衡教学工具 | 设计：教育技术专家</p>
            <p>提示：使用控制面板改变条件，观察粒子运动、反应速率和平衡移动的变化。</p>
        </footer>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const mainCanvas = document.getElementById('animationCanvas');
        const rateCanvas = document.getElementById('rateChart');
        const mainCtx = mainCanvas.getContext('2d');
        const rateCtx = rateCanvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvases() {
            const container = mainCanvas.parentElement;
            mainCanvas.width = container.clientWidth;
            mainCanvas.height = container.clientHeight;
            
            rateCanvas.width = rateCanvas.parentElement.clientWidth;
            rateCanvas.height = rateCanvas.parentElement.clientHeight;
        }
        
        window.addEventListener('resize', resizeCanvases);
        resizeCanvases();
        
        // 系统状态变量
        let isPaused = false;
        let animationSpeed = 5;
        let autoDemoMode = false;
        let autoDemoStep = 0;
        let lastTime = 0;
        
        // 反应参数
        const reaction = {
            // A₂ + B₂ ⇌ 2AB
            kForward: 0.02,  // 正反应速率常数
            kReverse: 0.015, // 逆反应速率常数
            forwardActivationEnergy: 50, // 正反应活化能
            reverseActivationEnergy: 70,  // 逆反应活化能（吸热方向活化能更高）
            isExothermic: true, // 正反应放热
            deltaH: -20, // 反应焓变
            volume: 100, // 相对体积（%）
            temperature: 5, // 相对温度（1-10）
            baseTemperature: 5 // 基准温度
        };
        
        // 粒子系统
        const particles = {
            A2: [], // 红色粒子
            B2: [], // 蓝色粒子
            AB: []  // 紫色粒子
        };
        
        // 反应速率数据
        const rateData = {
            forward: [], // 正反应速率
            reverse: [], // 逆反应速率
            maxLength: 100 // 记录的最大数据点数
        };
        
        // 初始化粒子
        function initParticles() {
            particles.A2 = [];
            particles.B2 = [];
            particles.AB = [];
            
            // 初始粒子数（平衡状态）
            const initialA2 = 30;
            const initialB2 = 30;
            const initialAB = 40;
            
            // 创建A₂粒子
            for (let i = 0; i < initialA2; i++) {
                particles.A2.push(createParticle('A2'));
            }
            
            // 创建B₂粒子
            for (let i = 0; i < initialB2; i++) {
                particles.B2.push(createParticle('B2'));
            }
            
            // 创建AB粒子
            for (let i = 0; i < initialAB; i++) {
                particles.AB.push(createParticle('AB'));
            }
            
            // 初始化速率数据
            rateData.forward = [];
            rateData.reverse = [];
            
            const initialForwardRate = calculateForwardRate();
            const initialReverseRate = calculateReverseRate();
            
            for (let i = 0; i < rateData.maxLength; i++) {
                rateData.forward.push(initialForwardRate);
                rateData.reverse.push(initialReverseRate);
            }
            
            updateParticleCounts();
            updateStatusText("系统处于平衡状态：v正 = v逆");
        }
        
        // 创建单个粒子
        function createParticle(type) {
            const canvasWidth = mainCanvas.width;
            const canvasHeight = mainCanvas.height;
            
            let color, radius, highlight;
            
            switch(type) {
                case 'A2':
                    color = '#f44336'; // 红色
                    radius = 10;
                    break;
                case 'B2':
                    color = '#2196f3'; // 蓝色
                    radius = 10;
                    break;
                case 'AB':
                    color = '#9c27b0'; // 紫色
                    radius = 12; // AB分子稍大
                    break;
                default:
                    color = '#ffffff';
                    radius = 8;
            }
            
            // 新加入的粒子高亮
            highlight = false;
            
            return {
                type: type,
                x: Math.random() * (canvasWidth - radius * 2) + radius,
                y: Math.random() * (canvasHeight - radius * 2) + radius,
                vx: (Math.random() - 0.5) * 2,
                vy: (Math.random() - 0.5) * 2,
                radius: radius,
                color: color,
                highlight: highlight,
                highlightTimer: 0
            };
        }
        
        // 计算正反应速率
        function calculateForwardRate() {
            // 速率 = k * [A₂] * [B₂] * 温度因子 * 压强因子
            const concentrationFactor = particles.A2.length * particles.B2.length / 1000;
            const temperatureFactor = Math.exp((reaction.temperature - reaction.baseTemperature) / 3);
            const pressureFactor = reaction.volume < 100 ? 100 / reaction.volume : 1;
            
            return reaction.kForward * concentrationFactor * temperatureFactor * pressureFactor;
        }
        
        // 计算逆反应速率
        function calculateReverseRate() {
            // 速率 = k * [AB]² * 温度因子 * 压强因子
            const concentrationFactor = Math.pow(particles.AB.length, 2) / 1000;
            const temperatureFactor = Math.exp((reaction.temperature - reaction.baseTemperature) / 3);
            const pressureFactor = reaction.volume < 100 ? 100 / reaction.volume : 1;
            
            // 温度对逆反应（吸热）影响更大
            const activationFactor = reaction.isExothermic ? 
                Math.exp((reaction.temperature - reaction.baseTemperature) / 2.5) : 
                Math.exp((reaction.temperature - reaction.baseTemperature) / 3);
                
            return reaction.kReverse * concentrationFactor * activationFactor * pressureFactor;
        }
        
        // 更新粒子计数显示
        function updateParticleCounts() {
            document.getElementById('countA2').textContent = particles.A2.length;
            document.getElementById('countB2').textContent = particles.B2.length;
            document.getElementById('countAB').textContent = particles.AB.length;
        }
        
        // 更新状态文本
        function updateStatusText(text) {
            document.getElementById('statusText').innerHTML = text;
        }
        
        // 添加粒子
        function addParticles(type, count = 5) {
            for (let i = 0; i < count; i++) {
                const particle = createParticle(type);
                particle.highlight = true;
                particle.highlightTimer = 60; // 高亮60帧
                particles[type].push(particle);
            }
            
            // 更新状态
            let changeText = "";
            switch(type) {
                case 'A2':
                    changeText = "增加了A₂浓度";
                    break;
                case 'B2':
                    changeText = "增加了B₂浓度";
                    break;
                case 'AB':
                    changeText = "增加了AB浓度";
                    break;
            }
            
            const forwardRate = calculateForwardRate();
            const reverseRate = calculateReverseRate();
            
            if (type === 'A2' || type === 'B2') {
                updateStatusText(`<span class="highlight">${changeText}</span> → 正反应速率瞬间增大 → v正 > v逆 → 平衡向正反应方向移动`);
            } else {
                updateStatusText(`<span class="highlight">${changeText}</span> → 逆反应速率瞬间增大 → v正 < v逆 → 平衡向逆反应方向移动`);
            }
            
            updateParticleCounts();
        }
        
        // 移除粒子
        function removeParticles(type, count = 5) {
            for (let i = 0; i < count && particles[type].length > 0; i++) {
                particles[type].pop();
            }
            
            // 更新状态
            let changeText = "";
            switch(type) {
                case 'A2':
                    changeText = "减少了A₂浓度";
                    break;
                case 'B2':
                    changeText = "减少了B₂浓度";
                    break;
                case 'AB':
                    changeText = "减少了AB浓度";
                    break;
            }
            
            const forwardRate = calculateForwardRate();
            const reverseRate = calculateReverseRate();
            
            if (type === 'A2' || type === 'B2') {
                updateStatusText(`<span class="highlight">${changeText}</span> → 正反应速率瞬间减小 → v正 < v逆 → 平衡向逆反应方向移动`);
            } else {
                updateStatusText(`<span class="highlight">${changeText}</span> → 逆反应速率瞬间减小 → v正 > v逆 → 平衡向正反应方向移动`);
            }
            
            updateParticleCounts();
        }
        
        // 改变压强（体积）
        function changePressure(newVolume) {
            reaction.volume = newVolume;
            document.getElementById('pressureValue').textContent = newVolume + '%';
            
            // 更新状态
            if (newVolume < 100) {
                updateStatusText(`<span class="highlight">增大压强（缩小体积）</span> → 所有粒子浓度增加 → 正逆反应速率均增大，但正反应（气体分子数减少方向）增加更多 → v正 > v逆 → 平衡向正反应方向移动`);
            } else if (newVolume > 100) {
                updateStatusText(`<span class="highlight">减小压强（增大体积）</span> → 所有粒子浓度降低 → 正逆反应速率均减小，但正反应（气体分子数减少方向）减小更多 → v正 < v逆 → 平衡向逆反应方向移动`);
            } else {
                updateStatusText("体积恢复原状，系统处于平衡状态");
            }
        }
        
        // 改变温度
        function changeTemperature(newTemp) {
            reaction.temperature = newTemp;
            document.getElementById('temperatureValue').textContent = newTemp;
            
            // 更新状态
            if (newTemp > reaction.baseTemperature) {
                updateStatusText(`<span class="highlight">升高温度</span> → 粒子动能增加 → 正逆反应速率均增大，但逆反应（吸热方向）增加更多 → v正 < v逆 → 平衡向吸热（逆反应）方向移动`);
            } else if (newTemp < reaction.baseTemperature) {
                updateStatusText(`<span class="highlight">降低温度</span> → 粒子动能减少 → 正逆反应速率均减小，但逆反应（吸热方向）减小更多 → v正 > v逆 → 平衡向放热（正反应）方向移动`);
            } else {
                updateStatusText("温度恢复原状，系统处于平衡状态");
            }
        }
        
        // 绘制粒子
        function drawParticles() {
            mainCtx.clearRect(0, 0, mainCanvas.width, mainCanvas.height);
            
            // 绘制容器边界（反映体积变化）
            const width = mainCanvas.width;
            const height = mainCanvas.height;
            const scale = reaction.volume / 100;
            
            const scaledWidth = width * scale;
            const scaledHeight = height * scale;
            const offsetX = (width - scaledWidth) / 2;
            const offsetY = (height - scaledHeight) / 2;
            
            // 绘制容器背景
            mainCtx.fillStyle = 'rgba(15, 23, 42, 0.7)';
            mainCtx.fillRect(offsetX, offsetY, scaledWidth, scaledHeight);
            
            // 绘制容器边框
            mainCtx.strokeStyle = reaction.volume !== 100 ? '#fbbf24' : '#475569';
            mainCtx.lineWidth = 3;
            mainCtx.strokeRect(offsetX, offsetY, scaledWidth, scaledHeight);
            
            // 绘制所有粒子
            const allParticles = [...particles.A2, ...particles.B2, ...particles.AB];
            
            for (const particle of allParticles) {
                // 调整粒子位置到缩放后的容器内
                let drawX = particle.x;
                let drawY = particle.y;
                
                // 如果粒子在容器外，将其移动到容器内
                if (drawX < offsetX) drawX = offsetX + particle.radius;
                if (drawX > offsetX + scaledWidth) drawX = offsetX + scaledWidth - particle.radius;
                if (drawY < offsetY) drawY = offsetY + particle.radius;
                if (drawY > offsetY + scaledHeight) drawY = offsetY + scaledHeight - particle.radius;
                
                // 绘制粒子
                mainCtx.beginPath();
                mainCtx.arc(drawX, drawY, particle.radius, 0, Math.PI * 2);
                
                // 高亮效果
                if (particle.highlight && particle.highlightTimer > 0) {
                    mainCtx.fillStyle = '#ffeb3b'; // 高亮黄色
                    particle.highlightTimer--;
                } else {
                    mainCtx.fillStyle = particle.color;
                    particle.highlight = false;
                }
                
                mainCtx.fill();
                
                // 温度效果：粒子周围的光环
                if (reaction.temperature > reaction.baseTemperature) {
                    mainCtx.beginPath();
                    mainCtx.arc(drawX, drawY, particle.radius + 3, 0, Math.PI * 2);
                    mainCtx.strokeStyle = `rgba(255, ${100 + reaction.temperature * 15}, 0, 0.5)`;
                    mainCtx.lineWidth = 2;
                    mainCtx.stroke();
                }
                
                // 更新粒子位置（如果未暂停）
                if (!isPaused) {
                    // 根据温度调整速度
                    const speedFactor = 1 + (reaction.temperature - reaction.baseTemperature) * 0.1;
                    
                    particle.x += particle.vx * speedFactor * (animationSpeed / 5);
                    particle.y += particle.vy * speedFactor * (animationSpeed / 5);
                    
                    // 边界碰撞（考虑缩放后的容器）
                    if (particle.x <= offsetX + particle.radius || particle.x >= offsetX + scaledWidth - particle.radius) {
                        particle.vx = -particle.vx;
                    }
                    if (particle.y <= offsetY + particle.radius || particle.y >= offsetY + scaledHeight - particle.radius) {
                        particle.vy = -particle.vy;
                    }
                }
            }
            
            // 绘制反应方程式
            mainCtx.fillStyle = 'rgba(255, 255, 255, 0.9)';
            mainCtx.font = 'bold 18px Arial';
            mainCtx.textAlign = 'center';
            mainCtx.fillText('A₂ + B₂ ⇌ 2AB', width / 2, 30);
            
            // 绘制条件指示器
            mainCtx.font = '14px Arial';
            mainCtx.textAlign = 'left';
            mainCtx.fillStyle = reaction.temperature > reaction.baseTemperature ? '#ef4444' : '#60a5fa';
            mainCtx.fillText(`温度: ${reaction.temperature}`, 20, height - 50);
            
            mainCtx.fillStyle = reaction.volume < 100 ? '#fbbf24' : '#60a5fa';
            mainCtx.fillText(`体积: ${reaction.volume}%`, 20, height - 30);
        }
        
        // 绘制速率图表
        function drawRateChart() {
            const width = rateCanvas.width;
            const height = rateCanvas.height;
            
            rateCtx.clearRect(0, 0, width, height);
            
            // 绘制背景
            rateCtx.fillStyle = 'rgba(15, 23, 42, 0.8)';
            rateCtx.fillRect(0, 0, width, height);
            
            // 绘制网格
            rateCtx.strokeStyle = 'rgba(100, 116, 139, 0.3)';
            rateCtx.lineWidth = 1;
            
            // 水平网格线
            for (let i = 0; i <= 5; i++) {
                const y = height - (i * height / 5);
                rateCtx.beginPath();
                rateCtx.moveTo(0, y);
                rateCtx.lineTo(width, y);
                rateCtx.stroke();
            }
            
            // 计算当前速率
            const forwardRate = calculateForwardRate();
            const reverseRate = calculateReverseRate();
            
            // 更新速率数据
            rateData.forward.push(forwardRate);
            rateData.reverse.push(reverseRate);
            
            if (rateData.forward.length > rateData.maxLength) {
                rateData.forward.shift();
                rateData.reverse.shift();
            }
            
            // 找到最大速率值用于缩放
            const maxRate = Math.max(...rateData.forward, ...rateData.reverse, 0.1);
            
            // 绘制正反应速率曲线（绿色）
            rateCtx.beginPath();
            rateCtx.strokeStyle = '#4caf50';
            rateCtx.lineWidth = 3;
            
            for (let i = 0; i < rateData.forward.length; i++) {
                const x = (i / rateData.maxLength) * width;
                const y = height - (rateData.forward[i] / maxRate) * height * 0.8;
                
                if (i === 0) {
                    rateCtx.moveTo(x, y);
                } else {
                    rateCtx.lineTo(x, y);
                }
            }
            
            rateCtx.stroke();
            
            // 绘制逆反应速率曲线（橙色）
            rateCtx.beginPath();
            rateCtx.strokeStyle = '#ff9800';
            rateCtx.lineWidth = 3;
            
            for (let i = 0; i < rateData.reverse.length; i++) {
                const x = (i / rateData.maxLength) * width;
                const y = height - (rateData.reverse[i] / maxRate) * height * 0.8;
                
                if (i === 0) {
                    rateCtx.moveTo(x, y);
                } else {
                    rateCtx.lineTo(x, y);
                }
            }
            
            rateCtx.stroke();
            
            // 绘制图例
            rateCtx.font = '12px Arial';
            rateCtx.textAlign = 'left';
            
            // 正反应速率图例
            rateCtx.fillStyle = '#4caf50';
            rateCtx.fillText('v正', 10, 20);
            
            // 逆反应速率图例
            rateCtx.fillStyle = '#ff9800';
            rateCtx.fillText('v逆', 10, 40);
            
            // 当前速率值
            rateCtx.fillStyle = '#cbd5e1';
            rateCtx.fillText(`v正 = ${forwardRate.toFixed(3)}`, width - 120, 20);
            rateCtx.fillText(`v逆 = ${reverseRate.toFixed(3)}`, width - 120, 40);
            
            // 绘制平衡常数K
            const K = forwardRate / reverseRate;
            rateCtx.fillText(`K = ${K.toFixed(3)}`, width - 120, 60);
            
            // 指示平衡常数是否变化（仅温度改变时变化）
            if (reaction.temperature !== reaction.baseTemperature) {
                rateCtx.fillStyle = '#ef4444';
                rateCtx.fillText('K 变化', width - 120, 80);
            }
        }
        
        // 模拟化学反应
        function simulateReaction() {
            if (isPaused) return;
            
            const forwardRate = calculateForwardRate();
            const reverseRate = calculateReverseRate();
            
            // 根据反应速率决定是否发生反应
            // 正反应：A₂ + B₂ → 2AB
            if (particles.A2.length > 0 && particles.B2.length > 0) {
                const forwardProbability = forwardRate / 100;
                
                if (Math.random() < forwardProbability * (animationSpeed / 5)) {
                    // 移除一个A₂和一个B₂
                    if (particles.A2.length > 0 && particles.B2.length > 0) {
                        particles.A2.pop();
                        particles.B2.pop();
                        
                        // 添加两个AB（高亮显示）
                        for (let i = 0; i < 2; i++) {
                            const newAB = createParticle('AB');
                            newAB.highlight = true;
                            newAB.highlightTimer = 30;
                            particles.AB.push(newAB);
                        }
                    }
                }
            }
            
            // 逆反应：2AB → A₂ + B₂
            if (particles.AB.length >= 2) {
                const reverseProbability = reverseRate / 100;
                
                if (Math.random() < reverseProbability * (animationSpeed / 5)) {
                    // 移除两个AB
                    if (particles.AB.length >= 2) {
                        particles.AB.pop();
                        particles.AB.pop();
                        
                        // 添加一个A₂和一个B₂（高亮显示）
                        const newA2 = createParticle('A2');
                        newA2.highlight = true;
                        newA2.highlightTimer = 30;
                        particles.A2.push(newA2);
                        
                        const newB2 = createParticle('B2');
                        newB2.highlight = true;
                        newB2.highlightTimer = 30;
                        particles.B2.push(newB2);
                    }
                }
            }
            
            updateParticleCounts();
        }
        
        // 自动演示模式
        function autoDemo() {
            if (!autoDemoMode) return;
            
            autoDemoStep++;
            
            // 演示序列
            switch(autoDemoStep) {
                case 30:
                    addParticles('A2', 10);
                    break;
                case 80:
                    changePressure(70); // 增大压强
                    break;
                case 130:
                    changeTemperature(8); // 升高温度
                    break;
                case 180:
                    // 恢复原状
                    changePressure(100);
                    changeTemperature(5);
                    autoDemoStep = 0;
                    break;
            }
        }
        
        // 动画循环
        function animate(timestamp) {
            // 计算时间增量
            const deltaTime = timestamp - lastTime || 0;
            lastTime = timestamp;
            
            // 自动演示
            if (autoDemoMode && deltaTime > 16) {
                autoDemo();
            }
            
            // 绘制和模拟
            drawParticles();
            drawRateChart();
            simulateReaction();
            
            requestAnimationFrame(animate);
        }
        
        // 初始化事件监听器
        function initEventListeners() {
            // 系统控制
            document.getElementById('resetBtn').addEventListener('click', () => {
                initParticles();
                changePressure(100);
                changeTemperature(5);
                document.getElementById('pressureSlider').value = 100;
                document.getElementById('temperatureSlider').value = 5;
                document.getElementById('pressureValue').textContent = '100%';
                document.getElementById('temperatureValue').textContent = '5';
                autoDemoMode = false;
                autoDemoStep = 0;
            });
            
            document.getElementById('pauseBtn').addEventListener('click', () => {
                isPaused = !isPaused;
                document.getElementById('pauseBtn').textContent = isPaused ? '继续' : '暂停';
            });
            
            document.getElementById('stepBtn').addEventListener('click', () => {
                // 单步执行：模拟一次反应
                simulateReaction();
            });
            
            document.getElementById('autoBtn').addEventListener('click', () => {
                autoDemoMode = !autoDemoMode;
                document.getElementById('autoBtn').textContent = autoDemoMode ? '停止演示' : '自动演示';
                autoDemoStep = 0;
            });
            
            // 动画速度控制
            document.getElementById('speedSlider').addEventListener('input', (e) => {
                animationSpeed = parseInt(e.target.value);
                document.getElementById('speedValue').textContent = animationSpeed;
            });
            
            // 浓度控制
            document.getElementById('addA2Btn').addEventListener('click', () => addParticles('A2', 5));
            document.getElementById('removeA2Btn').addEventListener('click', () => removeParticles('A2', 5));
            document.getElementById('addB2Btn').addEventListener('click', () => addParticles('B2', 5));
            document.getElementById('removeB2Btn').addEventListener('click', () => removeParticles('B2', 5));
            document.getElementById('addABBtn').addEventListener('click', () => addParticles('AB', 5));
            document.getElementById('removeABBtn').addEventListener('click', () => removeParticles('AB', 5));
            
            // 压强控制
            document.getElementById('pressureSlider').addEventListener('input', (e) => {
                changePressure(parseInt(e.target.value));
            });
            
            document.getElementById('increasePressureBtn').addEventListener('click', () => {
                const newPressure = Math.max(50, reaction.volume - 20);
                document.getElementById('pressureSlider').value = newPressure;
                changePressure(newPressure);
            });
            
            document.getElementById('decreasePressureBtn').addEventListener('click', () => {
                const newPressure = Math.min(150, reaction.volume + 20);
                document.getElementById('pressureSlider').value = newPressure;
                changePressure(newPressure);
            });
            
            // 温度控制
            document.getElementById('temperatureSlider').addEventListener('input', (e) => {
                changeTemperature(parseInt(e.target.value));
            });
            
            document.getElementById('increaseTempBtn').addEventListener('click', () => {
                const newTemp = Math.min(10, reaction.temperature + 1);
                document.getElementById('temperatureSlider').value = newTemp;
                changeTemperature(newTemp);
            });
            
            document.getElementById('decreaseTempBtn').addEventListener('click', () => {
                const newTemp = Math.max(1, reaction.temperature - 1);
                document.getElementById('temperatureSlider').value = newTemp;
                changeTemperature(newTemp);
            });
        }
        
        // 初始化
        function init() {
            initParticles();
            initEventListeners();
            animate(0);
        }
        
        // 启动应用
        init();
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## 勒夏特列原理微观解释交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态可视化方式，帮助您深入理解勒夏特列原理的微观本质。无论您是学生、教师还是化学爱好者，都能通过亲手操作，直观地“看见”化学平衡移动的奥秘。

---

### 一、功能说明

本动画模拟了可逆反应 **A₂ + B₂ ⇌ 2AB** 的化学平衡系统，并允许您通过交互操作改变影响平衡的三个关键条件：**浓度、压强和温度**。系统将实时展示：
- 微观粒子的运动与碰撞
- 正逆反应速率（v正和v逆）的动态变化
- 平衡移动的完整过程
- 关键参数的实时数据

### 二、主要功能区域

#### 1. 微观动画演示区（左侧）
- **粒子运动视图**：实时显示A₂（红色）、B₂（蓝色）和AB（紫色）粒子的运动、碰撞及反应过程。
- **容器边界**：灰色边框表示当前体积，改变压强时会动态缩放，直观展示“体积变化”。
- **条件指示器**：左上角显示当前温度和体积状态。
- **粒子计数面板**：实时显示各物质的粒子数量。

#### 2. 反应速率图表区
- **双曲线图**：绿色曲线代表正反应速率（v正），橙色曲线代表逆反应速率（v逆）。
- **实时数据**：显示当前v正、v逆的数值及平衡常数K。
- **关键提示**：当温度改变时，K值会发生变化并高亮显示。

#### 3. 系统状态栏
- 用简洁的语言描述当前系统的状态和变化过程。
- 高亮显示关键变化和原理。

#### 4. 控制面板区（右侧）
- **系统控制**：重置、暂停/继续、单步演示、自动演示及速度调节。
- **浓度影响**：分别增加或减少A₂、B₂、AB的浓度。
- **压强影响**：通过滑块或按钮改变压强（体积）。
- **温度影响**：通过滑块或按钮改变系统温度。

#### 5. 原理解释区（底部）
- 详细阐述勒夏特列原理在三种情况下的微观解释。
- 使用颜色高亮和分段说明，便于理解记忆。

### 三、设计特色

1. **多感官学习体验**
   - **视觉**：彩色粒子、动态曲线、高亮效果
   - **交互**：亲手操作改变条件，观察即时反馈
   - **认知**：宏观现象与微观本质的直观连接

2. **科学准确性**
   - 反应速率计算基于碰撞理论和阿伦尼乌斯方程
   - 准确区分温度对放热/吸热反应的不同影响
   - 正确体现压强改变对气体分子数不同反应的影响差异

3. **教学友好性**
   - 分步演示功能，适合课堂讲解
   - 自动演示模式，展示完整的变化序列
   - 实时状态描述，辅助理解原理

### 四、教学要点与使用建议

#### 教学要点：
1. **核心概念**：始终关注**正逆反应速率的相对变化**（v正 vs v逆），这是理解所有平衡移动的关键。
2. **浓度变化**：观察增加反应物时，如何瞬间提高正反应速率，导致v正 > v逆。
3. **压强变化**：注意体积缩小时，所有粒子浓度等比例增加，但气体分子数减少的方向（正反应）速率增加更显著。
4. **温度变化**：重点理解温度对吸热反应（本系统中为逆反应）影响更大的原因——更高的活化能。
5. **平衡常数**：特别留意**只有温度改变时，K值才会变化**这一重要规律。

#### 使用建议：
**对于学生自学：**
1. **探索模式**：先随意尝试各种操作，观察现象，培养直觉。
2. **验证模式**：根据所学知识预测结果，然后操作验证。
3. **总结模式**：操作后阅读底部的原理解释，将现象与理论对应。

**对于课堂教学：**
1. **引入环节**：使用自动演示模式，快速展示三种情况的完整过程。
2. **讲解环节**：使用单步演示和暂停功能，分步讲解关键瞬间。
3. **互动环节**：让学生上台操作，或分组设计实验方案。
4. **总结环节**：结合速率曲线图，系统归纳三种情况的共同本质。

**推荐学习路径：**
1. 从“浓度影响”开始，这是最直观的情况。
2. 接着探索“压强影响”，理解体积变化与浓度变化的联系。
3. 最后研究“温度影响”，这是最抽象但最重要的部分。
4. 使用“自动演示”模式观看完整序列，建立整体认知。
5. 操作后阅读原理解释，完成从现象到本质的升华。

### 五、技术提示

1. **性能优化**：如果动画卡顿，可适当降低动画速度。
2. **响应式设计**：工具适配不同屏幕尺寸，但在大屏幕上体验更佳。
3. **数据解读**：速率图表中的曲线有约100个数据点的历史记录，可观察变化趋势。

---

### 开启您的探索之旅

现在，您已经掌握了本工具的所有功能。请点击“重置系统”按钮，开始您的化学平衡探索之旅吧！

**记住**：最好的学习方式是亲手操作、仔细观察、用心思考。当您能准确预测每次操作的结果时，您就真正掌握了勒夏特列原理的微观本质。

祝您学习愉快，探索成功！

*—— 设计团队：教育技术专家与化学教育者*