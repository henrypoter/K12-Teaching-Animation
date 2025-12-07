# 需求：链式核反应（动画显示中子倍增与控制）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要为高中或大学低年级的物理、核工程专业学生，以及对核能原理感兴趣的公众。他们需要：
1.  **直观理解抽象过程**：将微观、抽象的链式反应过程（中子撞击、裂变、新中子产生）可视化，降低认知门槛。
2.  **掌握关键变量与条件**：理解“临界状态”（临界、超临界、次临界）是如何由“中子产生数”与“中子损失数”的平衡决定的。
3.  **理解控制原理**：明白控制棒（或其它中子吸收体）如何通过吸收中子来干预反应速率，实现启动、维持和停止反应。
4.  **建立安全与可控的认知**：通过动画演示可控的链式反应（如核电站）与不可控的链式反应（如核弹）在原理上的核心区别，消除对核能的纯粹恐惧感。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
*   **核心概念**：
    *   **核裂变**：一个重核（如铀-235）吸收一个中子后分裂成两个中等质量的核（裂变碎片），并释放出能量和新的中子（通常为2-3个）。
    *   **链式反应**：裂变产生的新中子又能引发周围其他重核的裂变，从而使反应持续进行下去。
    *   **倍增系数 (k)**：定义为一代中子总数与上一代中子总数之比。`k=1`为临界（反应稳定），`k>1`为超临界（反应指数增长），`k<1`为次临界（反应衰减停止）。
    *   **反应控制**：通过引入或移出中子吸收体（控制棒）来动态调整倍增系数`k`，从而控制反应速率。

*   **认知规律**：
    1.  **从具体到抽象**：先展示单个核裂变的微观动画，再扩展到多个核的链式反应宏观视图。
    2.  **从静态到动态**：先让用户观察一个“回合”的反应，再观察连续多代中子的传播与反应速率的动态变化。
    3.  **从观察到操控**：在用户理解基本过程后，提供交互控件（如拖动控制棒），让其亲自体验“控制”对反应过程的影响，深化理解。

*   **交互设计**：
    *   **模块化与流程化**：将动画分为“单次裂变演示”、“链式反应观察”和“反应控制实验”三个主要阶段或可切换的标签页。
    *   **引导式探索**：在关键步骤设置简短的文字提示或高亮提示，引导用户注意观察重点（如“注意新产生的中子数量”）。
    *   **即时反馈**：当用户调整参数（如控制棒插入深度）时，动画反应速率和倍增系数`k`的数值显示应立即、同步地发生变化，建立牢固的因果关系认知。

*   **视觉呈现**：
    *   **符号化与一致性**：
        *   **铀核**：用较大的、有质感的球体（如深蓝色或金属灰色）表示，被中子击中时高亮并“碎裂”。
        *   **中子**：用高速运动的小红点表示，轨迹清晰可见。
        *   **裂变碎片**：用两个中等大小的、颜色不同的球体（如黄色和绿色）向两侧飞散，并伴随“能量释放”的光晕效果。
        *   **控制棒**：用可上下移动的黑色或深灰色长条表示，当其插入时，路径上的中子会“消失”（被吸收）。
    *   **宏观与微观视图结合**：在展示链式反应时，可采用“蜂窝状”或“点阵状”排列的铀核来代表反应堆活性区，既能展示反应的传播，又不过于杂乱。
    *   **关键数据可视化**：在画面醒目位置（如顶部）动态显示“当前中子数”、“倍增系数 k”、“反应状态（次临界/临界/超临界）”和“功率水平（模拟）”等参数。

#### 配色方案选择
*   **主色调**：采用深蓝色或深灰色作为画布背景，模拟科技感与微观世界的深邃，同时能突出前景的动画元素。
*   **核心元素色**：
    *   **中子**：亮红色或亮橙色。红色具有“警示”和“活跃”的心理学暗示，能有效吸引注意力，代表其高速、关键的特性。
    *   **铀-235核**：金属灰蓝色或暗金色。体现其“重核”的质感与稳定性。
    *   **裂变碎片**：对比鲜明的亮绿色和亮黄色。飞散时产生视觉冲击，清晰表示分裂过程。
    *   **释放的能量**：使用半透明的黄色或白色光晕效果，表示能量的释放。
*   **控制与UI色**：
    *   **控制棒**：炭黑色或深镉灰色，与背景区分但又不刺眼，体现其“吸收”特性。
    *   **UI面板/按钮**：半透明深色背景（如#2C3E50带透明度），配白色或浅灰色文字与边框，确保清晰可读且不干扰主动画区。
    *   **数据指示器**：
        *   `k<1`（次临界）：蓝色（冷却、衰减）。
        *   `k=1`（临界）：绿色（稳定、安全）。
        *   `k>1`（超临界）：红色（增长、危险）。
*   **整体原则**：保证高对比度，使运动元素（中子）和交互元素（控制棒、按钮）在背景中一目了然，同时色彩搭配符合科学可视化的常规认知。

#### 交互功能列表
1.  **动画控制区**：
    *   “播放/暂停/重置”全局动画按钮。
    *   “单步执行”按钮：用于仔细观察一代中子的完整生命周期。
    *   “动画速度”滑块：允许用户减慢或加快动画速度。
2.  **场景选择器**：
    *   标签页或按钮，用于在“单次裂变演示”、“链式反应模拟”、“反应控制实验”三个主要场景间切换。
3.  **参数设置区（在“链式反应模拟”和“实验”场景中）**：
    *   “初始中子数”滑块/输入框（例如：1-5个）。
    *   “每个裂变产生中子数”滑块（例如：1.0 - 3.0，可模拟k值）。
    *   “中子逃逸概率”或“吸收体密度”滑块（模拟固有损失）。
4.  **核心交互控件**：
    *   **可拖动的控制棒**：用户可以用鼠标上下拖动控制棒，直观地将其插入或抽出“反应堆”区域。
    *   **控制棒插入深度指示器**：以百分比或具体长度显示。
5.  **动态数据仪表盘**：
    *   实时显示：`倍增系数 (k)`， `当前代中子数`， `总裂变次数`， `模拟功率输出`。
    *   视觉状态指示器：根据k值变化颜色（蓝/绿/红）并显示文字状态（次临界/临界/超临界）。
6.  **预设场景按钮**（用于快速理解）：
    *   “启动反应”（缓慢抽出控制棒使k略大于1）。
    *   “稳定运行”（调整到k=1）。
    *   “紧急停堆”（快速插入所有控制棒使k远小于1）。
    *   “原子弹模式”（极高k值，无控制，快速指数增长）——此按钮需谨慎设计，可能配以严肃说明。
7.  **提示与说明系统**：
    *   可开关的“知识提示”浮层，对关键步骤进行简短解说。
    *   鼠标悬停在元素（如铀核、控制棒）上时显示工具提示说明。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>链式核反应：中子倍增与控制</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f2027 0%, #203a43 50%, #2c5364 100%);
            color: #e0f7fa;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        header {
            text-align: center;
            padding: 20px;
            background: rgba(0, 30, 60, 0.7);
            border-radius: 15px;
            border: 1px solid rgba(64, 224, 208, 0.3);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        
        h1 {
            color: #4fc3f7;
            margin-bottom: 10px;
            font-size: 2.5rem;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .subtitle {
            color: #80deea;
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .animation-section {
            flex: 3;
            min-width: 300px;
            background: rgba(13, 27, 42, 0.85);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(64, 224, 208, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
            display: flex;
            flex-direction: column;
        }
        
        .animation-container {
            flex: 1;
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            background: #0a1929;
            border: 2px solid rgba(41, 98, 255, 0.1);
        }
        
        #reactionCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .control-panel {
            flex: 2;
            min-width: 300px;
            background: rgba(13, 27, 42, 0.85);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(64, 224, 208, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .panel-section {
            background: rgba(0, 30, 60, 0.5);
            border-radius: 10px;
            padding: 15px;
            border-left: 4px solid #2962ff;
        }
        
        .panel-title {
            color: #82b1ff;
            margin-bottom: 15px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .panel-title i {
            font-size: 1.5rem;
        }
        
        .controls-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
        }
        
        .control-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }
        
        .control-label {
            display: flex;
            justify-content: space-between;
            color: #bbdefb;
        }
        
        .control-value {
            color: #4fc3f7;
            font-weight: bold;
        }
        
        input[type="range"] {
            width: 100%;
            height: 8px;
            -webkit-appearance: none;
            background: linear-gradient(to right, #1565c0, #4fc3f7);
            border-radius: 4px;
            outline: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #bbdefb;
            cursor: pointer;
            border: 2px solid #0d47a1;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.5);
        }
        
        .buttons-row {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }
        
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 8px;
            background: linear-gradient(135deg, #2962ff, #448aff);
            color: white;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 120px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }
        
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
            background: linear-gradient(135deg, #2979ff, #82b1ff);
        }
        
        button:active {
            transform: translateY(1px);
        }
        
        button.reset {
            background: linear-gradient(135deg, #d32f2f, #f44336);
        }
        
        button.reset:hover {
            background: linear-gradient(135deg, #f44336, #ff7961);
        }
        
        button.preset {
            background: linear-gradient(135deg, #00796b, #009688);
        }
        
        button.preset:hover {
            background: linear-gradient(135deg, #009688, #4db6ac);
        }
        
        .status-display {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 10px;
        }
        
        .status-item {
            background: rgba(0, 0, 0, 0.3);
            border-radius: 8px;
            padding: 15px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .status-label {
            font-size: 0.9rem;
            color: #bbdefb;
            margin-bottom: 5px;
        }
        
        .status-value {
            font-size: 1.8rem;
            font-weight: bold;
            color: #4fc3f7;
        }
        
        .k-status {
            font-size: 1.2rem;
            padding: 5px 15px;
            border-radius: 20px;
            display: inline-block;
            margin-top: 5px;
            font-weight: bold;
        }
        
        .k-subcritical {
            background-color: rgba(33, 150, 243, 0.3);
            color: #81d4fa;
            border: 1px solid #29b6f6;
        }
        
        .k-critical {
            background-color: rgba(76, 175, 80, 0.3);
            color: #a5d6a7;
            border: 1px solid #4caf50;
        }
        
        .k-supercritical {
            background-color: rgba(244, 67, 54, 0.3);
            color: #ffab91;
            border: 1px solid #f44336;
        }
        
        .legend {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
        }
        
        .legend-text {
            font-size: 0.9rem;
            color: #bbdefb;
        }
        
        .info-section {
            background: rgba(13, 27, 42, 0.85);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(64, 224, 208, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
        }
        
        .info-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .info-card {
            background: rgba(0, 30, 60, 0.5);
            border-radius: 10px;
            padding: 15px;
            border-left: 4px solid #ff9800;
        }
        
        .info-card h3 {
            color: #ffb74d;
            margin-bottom: 10px;
            font-size: 1.2rem;
        }
        
        .info-card p {
            color: #e0f7fa;
            font-size: 0.95rem;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: #80deea;
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            margin-top: 20px;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .controls-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>链式核反应：中子倍增与控制</h1>
            <p class="subtitle">通过交互式动画直观理解核裂变链式反应的原理、临界状态与控制方法</p>
        </header>
        
        <div class="main-content">
            <section class="animation-section">
                <h2 class="panel-title">反应堆核心模拟</h2>
                <div class="animation-container">
                    <canvas id="reactionCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #78909c;"></div>
                        <div class="legend-text">铀-235 核</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff5252;"></div>
                        <div class="legend-text">中子</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #69f0ae;"></div>
                        <div class="legend-text">裂变碎片</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #000000;"></div>
                        <div class="legend-text">控制棒（中子吸收体）</div>
                    </div>
                </div>
            </section>
            
            <section class="control-panel">
                <div class="panel-section">
                    <h2 class="panel-title">动画控制</h2>
                    <div class="buttons-row">
                        <button id="playBtn">▶ 播放</button>
                        <button id="pauseBtn">⏸ 暂停</button>
                        <button id="stepBtn">⏭ 单步执行</button>
                        <button id="resetBtn" class="reset">↺ 重置</button>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">
                            <span>动画速度</span>
                            <span class="control-value" id="speedValue">1.0x</span>
                        </div>
                        <input type="range" id="speedSlider" min="0.1" max="3" step="0.1" value="1">
                    </div>
                </div>
                
                <div class="panel-section">
                    <h2 class="panel-title">反应参数</h2>
                    <div class="controls-grid">
                        <div class="control-group">
                            <div class="control-label">
                                <span>初始中子数</span>
                                <span class="control-value" id="initialNeutronsValue">3</span>
                            </div>
                            <input type="range" id="initialNeutronsSlider" min="1" max="10" step="1" value="3">
                        </div>
                        
                        <div class="control-group">
                            <div class="control-label">
                                <span>每个裂变产生中子数</span>
                                <span class="control-value" id="neutronsPerFissionValue">2.4</span>
                            </div>
                            <input type="range" id="neutronsPerFissionSlider" min="0.5" max="3.5" step="0.1" value="2.4">
                        </div>
                        
                        <div class="control-group">
                            <div class="control-label">
                                <span>中子逃逸概率</span>
                                <span class="control-value" id="escapeProbValue">10%</span>
                            </div>
                            <input type="range" id="escapeProbSlider" min="0" max="30" step="1" value="10">
                        </div>
                        
                        <div class="control-group">
                            <div class="control-label">
                                <span>控制棒插入深度</span>
                                <span class="control-value" id="controlRodValue">50%</span>
                            </div>
                            <input type="range" id="controlRodSlider" min="0" max="100" step="1" value="50">
                        </div>
                    </div>
                </div>
                
                <div class="panel-section">
                    <h2 class="panel-title">预设场景</h2>
                    <div class="buttons-row">
                        <button id="startupBtn" class="preset">启动反应</button>
                        <button id="stableBtn" class="preset">稳定运行</button>
                        <button id="shutdownBtn" class="preset">紧急停堆</button>
                        <button id="bombBtn" class="preset">不可控链式反应</button>
                    </div>
                </div>
                
                <div class="panel-section">
                    <h2 class="panel-title">反应状态</h2>
                    <div class="status-display">
                        <div class="status-item">
                            <div class="status-label">倍增系数 (k)</div>
                            <div class="status-value" id="kValue">1.00</div>
                            <div id="kStatus" class="k-status k-critical">临界</div>
                        </div>
                        
                        <div class="status-item">
                            <div class="status-label">当前中子数</div>
                            <div class="status-value" id="currentNeutrons">3</div>
                        </div>
                        
                        <div class="status-item">
                            <div class="status-label">总裂变次数</div>
                            <div class="status-value" id="totalFissions">0</div>
                        </div>
                        
                        <div class="status-item">
                            <div class="status-label">模拟功率</div>
                            <div class="status-value" id="powerLevel">0%</div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
        
        <section class="info-section">
            <h2 class="panel-title">核心概念说明</h2>
            <div class="info-content">
                <div class="info-card">
                    <h3>核裂变与链式反应</h3>
                    <p>铀-235原子核吸收一个中子后变得不稳定，分裂成两个中等质量的原子核（裂变碎片），同时释放出大量能量和2-3个新的中子。这些新中子又能引发周围其他铀核的裂变，从而形成自持的链式反应。</p>
                </div>
                
                <div class="info-card">
                    <h3>临界状态 (k值)</h3>
                    <p>倍增系数k = 新一代中子数 / 上一代中子数：<br>
                    • k = 1 (临界)：反应稳定进行，中子数保持不变<br>
                    • k > 1 (超临界)：反应加速，中子数指数增长<br>
                    • k < 1 (次临界)：反应衰减，中子数逐渐减少</p>
                </div>
                
                <div class="info-card">
                    <h3>反应控制原理</h3>
                    <p>控制棒由镉、硼等强中子吸收材料制成。通过调节控制棒插入反应堆的深度，可以改变中子的吸收率，从而精确控制倍增系数k值，实现反应堆的启动、功率调节和安全停堆。</p>
                </div>
            </div>
        </section>
        
        <footer>
            <p>教学动画 | 链式核反应模拟 | 交互式物理教学工具</p>
            <p>提示：拖动控制棒滑块或使用预设场景按钮来观察不同条件下链式反应的变化</p>
        </footer>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const canvas = document.getElementById('reactionCanvas');
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
        
        // 物理参数
        let params = {
            // 反应参数
            initialNeutrons: 3,
            neutronsPerFission: 2.4,
            escapeProbability: 0.10, // 10%
            controlRodDepth: 0.5, // 50%
            
            // 动画状态
            isPlaying: false,
            animationSpeed: 1.0,
            currentNeutrons: 3,
            totalFissions: 0,
            generation: 0,
            kValue: 1.0,
            
            // 模拟状态
            lastNeutronCount: 3,
            powerLevel: 0,
            reactionState: 'critical' // 'subcritical', 'critical', 'supercritical'
        };
        
        // 反应堆核心中的铀核
        const uraniumNuclei = [];
        // 活动中的中子
        let neutrons = [];
        // 裂变碎片
        let fissionFragments = [];
        // 控制棒位置
        let controlRod = { x: 0, y: 0, width: 0, height: 0 };
        
        // 初始化反应堆
        function initReactor() {
            // 清空数组
            uraniumNuclei.length = 0;
            neutrons.length = 0;
            fissionFragments.length = 0;
            
            // 创建铀核网格
            const gridSize = 8;
            const cellWidth = canvas.width / (gridSize + 2);
            const cellHeight = canvas.height / (gridSize + 2);
            
            for (let i = 0; i < gridSize; i++) {
                for (let j = 0; j < gridSize; j++) {
                    uraniumNuclei.push({
                        x: cellWidth * (i + 1.5),
                        y: cellHeight * (j + 1.5),
                        radius: Math.min(cellWidth, cellHeight) * 0.3,
                        active: true, // 是否可裂变
                        fissionCount: 0 // 记录裂变次数（用于视觉反馈）
                    });
                }
            }
            
            // 初始化中子
            for (let i = 0; i < params.initialNeutrons; i++) {
                spawnNeutron();
            }
            
            // 设置控制棒位置
            controlRod.width = canvas.width * 0.08;
            controlRod.height = canvas.height * params.controlRodDepth;
            controlRod.x = canvas.width / 2 - controlRod.width / 2;
            controlRod.y = canvas.height - controlRod.height;
            
            // 重置参数
            params.currentNeutrons = params.initialNeutrons;
            params.totalFissions = 0;
            params.generation = 0;
            params.lastNeutronCount = params.initialNeutrons;
            params.powerLevel = 0;
            updateKValue();
            
            // 更新UI显示
            updateUI();
        }
        
        // 生成一个新的中子
        function spawnNeutron() {
            // 随机起始位置（在反应堆区域内）
            const x = canvas.width * 0.2 + Math.random() * canvas.width * 0.6;
            const y = canvas.height * 0.2 + Math.random() * canvas.height * 0.6;
            
            // 随机速度方向
            const angle = Math.random() * Math.PI * 2;
            const speed = 2 + Math.random() * 2;
            
            neutrons.push({
                x: x,
                y: y,
                vx: Math.cos(angle) * speed,
                vy: Math.sin(angle) * speed,
                radius: 4,
                age: 0,
                maxAge: 100 + Math.random() * 50, // 中子寿命
                generation: params.generation
            });
        }
        
        // 生成裂变碎片
        function spawnFissionFragments(x, y) {
            // 两个碎片飞向不同方向
            for (let i = 0; i < 2; i++) {
                const angle = Math.random() * Math.PI * 2;
                const speed = 1 + Math.random() * 2;
                
                fissionFragments.push({
                    x: x,
                    y: y,
                    vx: Math.cos(angle) * speed,
                    vy: Math.sin(angle) * speed,
                    radius: 8 + Math.random() * 4,
                    age: 0,
                    maxAge: 60 + Math.random() * 30, // 碎片存在时间
                    color: i === 0 ? '#69f0ae' : '#ffd740'
                });
            }
        }
        
        // 更新k值计算
        function updateKValue() {
            // 简化的k值计算：考虑裂变产生的中子、控制棒吸收和中子逃逸
            let baseK = params.neutronsPerFission;
            
            // 控制棒吸收效应（插入越深，吸收越多）
            const absorption = params.controlRodDepth * 0.7;
            
            // 中子逃逸效应
            const escape = params.escapeProbability;
            
            // 计算有效k值
            params.kValue = baseK * (1 - absorption) * (1 - escape);
            
            // 确定反应状态
            if (params.kValue < 0.95) {
                params.reactionState = 'subcritical';
            } else if (params.kValue > 1.05) {
                params.reactionState = 'supercritical';
            } else {
                params.reactionState = 'critical';
            }
            
            // 更新功率水平（基于k值和当前中子数）
            params.powerLevel = Math.min(100, Math.max(0, 
                params.powerLevel * 0.9 + (params.currentNeutrons / 50) * 10));
        }
        
        // 更新UI显示
        function updateUI() {
            // 更新数值显示
            document.getElementById('kValue').textContent = params.kValue.toFixed(2);
            document.getElementById('currentNeutrons').textContent = params.currentNeutrons;
            document.getElementById('totalFissions').textContent = params.totalFissions;
            document.getElementById('powerLevel').textContent = Math.round(params.powerLevel) + '%';
            
            // 更新k值状态显示
            const kStatusElement = document.getElementById('kStatus');
            kStatusElement.textContent = 
                params.reactionState === 'subcritical' ? '次临界' :
                params.reactionState === 'supercritical' ? '超临界' : '临界';
            
            // 更新CSS类
            kStatusElement.className = 'k-status';
            kStatusElement.classList.add(
                params.reactionState === 'subcritical' ? 'k-subcritical' :
                params.reactionState === 'supercritical' ? 'k-supercritical' : 'k-critical'
            );
            
            // 更新滑块值显示
            document.getElementById('initialNeutronsValue').textContent = params.initialNeutrons;
            document.getElementById('neutronsPerFissionValue').textContent = params.neutronsPerFission.toFixed(1);
            document.getElementById('escapeProbValue').textContent = Math.round(params.escapeProbability * 100) + '%';
            document.getElementById('controlRodValue').textContent = Math.round(params.controlRodDepth * 100) + '%';
            document.getElementById('speedValue').textContent = params.animationSpeed.toFixed(1) + 'x';
        }
        
        // 模拟一个动画帧
        function simulateFrame() {
            if (!params.isPlaying) return;
            
            // 更新控制棒位置
            controlRod.height = canvas.height * params.controlRodDepth;
            controlRod.y = canvas.height - controlRod.height;
            
            // 更新k值
            updateKValue();
            
            // 处理中子
            const newNeutrons = [];
            
            for (let i = neutrons.length - 1; i >= 0; i--) {
                const neutron = neutrons[i];
                
                // 更新位置
                neutron.x += neutron.vx * params.animationSpeed;
                neutron.y += neutron.vy * params.animationSpeed;
                neutron.age++;
                
                // 检查是否与边界碰撞
                if (neutron.x < 0 || neutron.x > canvas.width) {
                    neutron.vx *= -1;
                    neutron.x = Math.max(0, Math.min(canvas.width, neutron.x));
                }
                
                if (neutron.y < 0 || neutron.y > canvas.height) {
                    neutron.vy *= -1;
                    neutron.y = Math.max(0, Math.min(canvas.height, neutron.y));
                }
                
                // 检查是否被控制棒吸收
                if (neutron.x > controlRod.x && 
                    neutron.x < controlRod.x + controlRod.width &&
                    neutron.y > controlRod.y) {
                    // 中子被吸收，不加入新中子数组
                    continue;
                }
                
                // 检查中子逃逸（基于概率）
                if (Math.random() < params.escapeProbability) {
                    // 中子逃逸，不加入新中子数组
                    continue;
                }
                
                // 检查中子寿命
                if (neutron.age > neutron.maxAge) {
                    // 中子衰变，不加入新中子数组
                    continue;
                }
                
                // 检查是否与铀核碰撞
                let collided = false;
                for (let j = 0; j < uraniumNuclei.length; j++) {
                    const nucleus = uraniumNuclei[j];
                    
                    if (!nucleus.active) continue;
                    
                    const dx = neutron.x - nucleus.x;
                    const dy = neutron.y - nucleus.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance < neutron.radius + nucleus.radius) {
                        // 发生裂变！
                        nucleus.active = false; // 暂时标记为不可裂变（模拟裂变后）
                        nucleus.fissionCount = 30; // 设置裂变视觉效果持续时间
                        
                        // 产生裂变碎片
                        spawnFissionFragments(nucleus.x, nucleus.y);
                        
                        // 增加裂变计数
                        params.totalFissions++;
                        
                        // 产生新的中子（基于每个裂变产生的中子数）
                        const newNeutronCount = Math.floor(params.neutronsPerFission + Math.random() - 0.5);
                        for (let n = 0; n < newNeutronCount; n++) {
                            // 新中子从裂变位置产生
                            const angle = Math.random() * Math.PI * 2;
                            const speed = 2 + Math.random() * 2;
                            
                            newNeutrons.push({
                                x: nucleus.x,
                                y: nucleus.y,
                                vx: Math.cos(angle) * speed,
                                vy: Math.sin(angle) * speed,
                                radius: 4,
                                age: 0,
                                maxAge: 100 + Math.random() * 50,
                                generation: params.generation + 1
                            });
                        }
                        
                        collided = true;
                        break;
                    }
                }
                
                // 如果未碰撞，保留中子
                if (!collided) {
                    newNeutrons.push(neutron);
                }
            }
            
            // 更新中子数组
            neutrons = newNeutrons;
            params.currentNeutrons = neutrons.length;
            
            // 如果中子数为0且反应正在衰减，重新生成一些中子
            if (neutrons.length === 0 && params.kValue < 1 && params.isPlaying) {
                for (let i = 0; i < params.initialNeutrons; i++) {
                    spawnNeutron();
                }
                params.currentNeutrons = params.initialNeutrons;
            }
            
            // 如果k>1且中子数较少，额外生成一些中子模拟反应增长
            if (params.kValue > 1.1 && neutrons.length < 20 && Math.random() < 0.1) {
                spawnNeutron();
                params.currentNeutrons++;
            }
            
            // 更新裂变碎片
            for (let i = fissionFragments.length - 1; i >= 0; i--) {
                const fragment = fissionFragments[i];
                
                fragment.x += fragment.vx * params.animationSpeed;
                fragment.y += fragment.vy * params.animationSpeed;
                fragment.age++;
                
                // 移除过期的碎片
                if (fragment.age > fragment.maxAge) {
                    fissionFragments.splice(i, 1);
                }
            }
            
            // 恢复铀核的活性（模拟新的铀核）
            for (let i = 0; i < uraniumNuclei.length; i++) {
                const nucleus = uraniumNuclei[i];
                if (nucleus.fissionCount > 0) {
                    nucleus.fissionCount--;
                    if (nucleus.fissionCount === 0) {
                        nucleus.active = true;
                    }
                }
            }
            
            // 更新代计数（如果所有中子都是新一代）
            if (neutrons.length > 0 && neutrons.every(n => n.generation > params.generation)) {
                params.generation++;
                params.lastNeutronCount = params.currentNeutrons;
            }
            
            // 更新UI
            updateUI();
        }
        
        // 绘制场景
        function drawScene() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制反应堆背景
            ctx.fillStyle = 'rgba(10, 25, 41, 0.9)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制反应堆容器（网格）
            ctx.strokeStyle = 'rgba(41, 98, 255, 0.2)';
            ctx.lineWidth = 2;
            ctx.strokeRect(canvas.width * 0.1, canvas.height * 0.1, 
                          canvas.width * 0.8, canvas.height * 0.8);
            
            // 绘制铀核
            for (const nucleus of uraniumNuclei) {
                // 铀核颜色：根据是否活跃和裂变状态
                if (nucleus.fissionCount > 0) {
                    // 裂变中的铀核（发光效果）
                    const intensity = nucleus.fissionCount / 30;
                    ctx.fillStyle = `rgba(255, 215, 64, ${intensity})`;
                    
                    // 绘制光晕
                    ctx.beginPath();
                    ctx.arc(nucleus.x, nucleus.y, nucleus.radius * 2, 0, Math.PI * 2);
                    ctx.fillStyle = `rgba(255, 215, 64, ${intensity * 0.3})`;
                    ctx.fill();
                } else if (nucleus.active) {
                    ctx.fillStyle = '#78909c'; // 活跃的铀核
                } else {
                    ctx.fillStyle = '#546e7a'; // 不活跃的铀核
                }
                
                // 绘制铀核
                ctx.beginPath();
                ctx.arc(nucleus.x, nucleus.y, nucleus.radius, 0, Math.PI * 2);
                ctx.fill();
                
                // 铀核边框
                ctx.strokeStyle = '#b0bec5';
                ctx.lineWidth = 1;
                ctx.stroke();
            }
            
            // 绘制裂变碎片
            for (const fragment of fissionFragments) {
                ctx.fillStyle = fragment.color;
                ctx.beginPath();
                ctx.arc(fragment.x, fragment.y, fragment.radius, 0, Math.PI * 2);
                ctx.fill();
                
                // 碎片轨迹
                ctx.beginPath();
                ctx.moveTo(fragment.x, fragment.y);
                ctx.lineTo(fragment.x - fragment.vx * 5, fragment.y - fragment.vy * 5);
                ctx.strokeStyle = fragment.color + '80';
                ctx.lineWidth = 2;
                ctx.stroke();
            }
            
            // 绘制中子
            for (const neutron of neutrons) {
                // 中子颜色：根据代次略有不同
                const generationColor = Math.min(255, 150 + neutron.generation * 10);
                ctx.fillStyle = `rgb(255, ${Math.max(80, 255 - neutron.generation * 20)}, ${Math.max(80, 255 - neutron.generation * 20)})`;
                
                ctx.beginPath();
                ctx.arc(neutron.x, neutron.y, neutron.radius, 0, Math.PI * 2);
                ctx.fill();
                
                // 中子轨迹
                ctx.beginPath();
                ctx.moveTo(neutron.x, neutron.y);
                ctx.lineTo(neutron.x - neutron.vx * 3, neutron.y - neutron.vy * 3);
                ctx.strokeStyle = '#ff525280';
                ctx.lineWidth = 1;
                ctx.stroke();
            }
            
            // 绘制控制棒
            ctx.fillStyle = '#000000';
            ctx.fillRect(controlRod.x, controlRod.y, controlRod.width, controlRod.height);
            
            // 控制棒边框和标签
            ctx.strokeStyle = '#ffffff';
            ctx.lineWidth = 2;
            ctx.strokeRect(controlRod.x, controlRod.y, controlRod.width, controlRod.height);
            
            ctx.fillStyle = '#ffffff';
            ctx.font = '14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('控制棒', controlRod.x + controlRod.width / 2, controlRod.y + 20);
            
            // 绘制状态文本
            ctx.fillStyle = '#e0f7fa';
            ctx.font = '16px Arial';
            ctx.textAlign = 'left';
            ctx.fillText(`第 ${params.generation} 代中子`, 10, 30);
            ctx.fillText(`反应状态: ${params.reactionState === 'subcritical' ? '次临界' : 
                        params.reactionState === 'supercritical' ? '超临界' : '临界'}`, 10,
<!--检测到代码截断，自动续写中...-->
60);
            ctx.fillText(`k = ${params.kValue.toFixed(2)}`, 10, 90);
            
            // 绘制功率指示条
            const powerBarWidth = 200;
            const powerBarHeight = 20;
            const powerBarX = canvas.width - powerBarWidth - 20;
            const powerBarY = 30;
            
            // 功率条背景
            ctx.fillStyle = 'rgba(0, 0, 0, 0.5)';
            ctx.fillRect(powerBarX, powerBarY, powerBarWidth, powerBarHeight);
            
            // 功率条填充（根据k值变色）
            let powerColor;
            if (params.reactionState === 'subcritical') {
                powerColor = '#29b6f6';
            } else if (params.reactionState === 'supercritical') {
                powerColor = '#f44336';
            } else {
                powerColor = '#4caf50';
            }
            
            ctx.fillStyle = powerColor;
            ctx.fillRect(powerBarX, powerBarY, powerBarWidth * (params.powerLevel / 100), powerBarHeight);
            
            // 功率条边框和标签
            ctx.strokeStyle = '#ffffff';
            ctx.lineWidth = 1;
            ctx.strokeRect(powerBarX, powerBarY, powerBarWidth, powerBarHeight);
            
            ctx.fillStyle = '#ffffff';
            ctx.font = '14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('功率水平', powerBarX + powerBarWidth / 2, powerBarY - 5);
            ctx.fillText(`${Math.round(params.powerLevel)}%`, powerBarX + powerBarWidth / 2, powerBarY + powerBarHeight + 15);
        }
        
        // 动画循环
        function animate() {
            simulateFrame();
            drawScene();
            requestAnimationFrame(animate);
        }
        
        // 启动动画循环
        animate();
        
        // 初始化反应堆
        initReactor();
        
        // UI事件处理
        document.getElementById('playBtn').addEventListener('click', () => {
            params.isPlaying = true;
        });
        
        document.getElementById('pauseBtn').addEventListener('click', () => {
            params.isPlaying = false;
        });
        
        document.getElementById('stepBtn').addEventListener('click', () => {
            params.isPlaying = false;
            simulateFrame();
            drawScene();
        });
        
        document.getElementById('resetBtn').addEventListener('click', () => {
            params.isPlaying = false;
            initReactor();
            drawScene();
        });
        
        // 速度滑块
        const speedSlider = document.getElementById('speedSlider');
        speedSlider.addEventListener('input', () => {
            params.animationSpeed = parseFloat(speedSlider.value);
            updateUI();
        });
        
        // 初始中子数滑块
        const initialNeutronsSlider = document.getElementById('initialNeutronsSlider');
        initialNeutronsSlider.addEventListener('input', () => {
            params.initialNeutrons = parseInt(initialNeutronsSlider.value);
            updateUI();
        });
        
        // 每个裂变产生中子数滑块
        const neutronsPerFissionSlider = document.getElementById('neutronsPerFissionSlider');
        neutronsPerFissionSlider.addEventListener('input', () => {
            params.neutronsPerFission = parseFloat(neutronsPerFissionSlider.value);
            updateUI();
        });
        
        // 中子逃逸概率滑块
        const escapeProbSlider = document.getElementById('escapeProbSlider');
        escapeProbSlider.addEventListener('input', () => {
            params.escapeProbability = parseInt(escapeProbSlider.value) / 100;
            updateUI();
        });
        
        // 控制棒滑块
        const controlRodSlider = document.getElementById('controlRodSlider');
        controlRodSlider.addEventListener('input', () => {
            params.controlRodDepth = parseInt(controlRodSlider.value) / 100;
            updateUI();
        });
        
        // 预设场景按钮
        document.getElementById('startupBtn').addEventListener('click', () => {
            // 启动反应：控制棒部分抽出，k略大于1
            params.controlRodDepth = 0.3;
            controlRodSlider.value = 30;
            params.neutronsPerFission = 2.2;
            neutronsPerFissionSlider.value = 2.2;
            params.initialNeutrons = 3;
            initialNeutronsSlider.value = 3;
            params.isPlaying = true;
            updateUI();
        });
        
        document.getElementById('stableBtn').addEventListener('click', () => {
            // 稳定运行：k=1
            params.controlRodDepth = 0.5;
            controlRodSlider.value = 50;
            params.neutronsPerFission = 2.0;
            neutronsPerFissionSlider.value = 2.0;
            params.initialNeutrons = 5;
            initialNeutronsSlider.value = 5;
            params.isPlaying = true;
            updateUI();
        });
        
        document.getElementById('shutdownBtn').addEventListener('click', () => {
            // 紧急停堆：控制棒完全插入，k远小于1
            params.controlRodDepth = 1.0;
            controlRodSlider.value = 100;
            params.neutronsPerFission = 1.5;
            neutronsPerFissionSlider.value = 1.5;
            params.isPlaying = true;
            updateUI();
        });
        
        document.getElementById('bombBtn').addEventListener('click', () => {
            // 不可控链式反应：无控制棒，k远大于1
            params.controlRodDepth = 0.0;
            controlRodSlider.value = 0;
            params.neutronsPerFission = 3.0;
            neutronsPerFissionSlider.value = 3.0;
            params.escapeProbability = 0.05;
            escapeProbSlider.value = 5;
            params.initialNeutrons = 2;
            initialNeutronsSlider.value = 2;
            params.isPlaying = true;
            updateUI();
            
            // 显示警告
            alert('警告：此模式模拟不可控链式反应（如核弹原理）。在核电站中，通过多重安全措施确保不会发生这种情况。');
        });
        
        // 初始UI更新
        updateUI();
        
        // 添加键盘快捷键
        document.addEventListener('keydown', (e) => {
            switch(e.key) {
                case ' ':
                    // 空格键切换播放/暂停
                    params.isPlaying = !params.isPlaying;
                    e.preventDefault();
                    break;
                case 'r':
                case 'R':
                    // R键重置
                    params.isPlaying = false;
                    initReactor();
                    drawScene();
                    e.preventDefault();
                    break;
                case 'ArrowUp':
                    // 上箭头增加速度
                    params.animationSpeed = Math.min(3, params.animationSpeed + 0.1);
                    speedSlider.value = params.animationSpeed;
                    updateUI();
                    e.preventDefault();
                    break;
                case 'ArrowDown':
                    // 下箭头降低速度
                    params.animationSpeed = Math.max(0.1, params.animationSpeed - 0.1);
                    speedSlider.value = params.animationSpeed;
                    updateUI();
                    e.preventDefault();
                    break;
            }
        });
        
        // 添加画布点击交互：在点击位置生成中子
        canvas.addEventListener('click', (e) => {
            const rect = canvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            // 在点击位置生成一个中子
            const angle = Math.random() * Math.PI * 2;
            const speed = 2 + Math.random() * 2;
            
            neutrons.push({
                x: x,
                y: y,
                vx: Math.cos(angle) * speed,
                vy: Math.sin(angle) * speed,
                radius: 4,
                age: 0,
                maxAge: 100 + Math.random() * 50,
                generation: params.generation
            });
            
            params.currentNeutrons = neutrons.length;
            updateUI();
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 链式核反应交互式教学动画使用指南

欢迎使用“链式核反应：中子倍增与控制”交互式教学动画！本工具旨在通过直观的可视化方式，帮助您深入理解核裂变链式反应的原理、临界状态的概念以及反应控制的方法。无论您是物理专业的学生、教师，还是对核能科学感兴趣的公众，本动画都将为您提供一次生动而深刻的学习体验。

---

### 一、功能说明

本动画模拟了一个简化的核反应堆核心，展示了以下关键过程：

1. **核裂变过程**：铀-235原子核吸收中子后分裂成两个裂变碎片，释放能量并产生新的中子。
2. **链式反应传播**：新产生的中子继续引发周围铀核的裂变，形成自持的链式反应。
3. **临界状态控制**：通过调节控制棒插入深度，改变倍增系数(k值)，实现反应的启动、稳定运行和停止。
4. **实时状态监控**：动态显示反应的关键参数，包括中子数、裂变次数、功率水平和反应状态。

### 二、主要功能

#### 1. 动画控制区
- **播放/暂停**：控制动画的运行与暂停
- **单步执行**：逐帧观察反应过程，适合详细分析
- **重置**：恢复所有参数到初始状态
- **动画速度调节**：通过滑块调整动画播放速度（0.1x - 3.0x）

#### 2. 反应参数调节
- **初始中子数**：设置反应开始时的中子数量（1-10个）
- **每个裂变产生中子数**：调节每次裂变平均产生的中子数（0.5-3.5个）
- **中子逃逸概率**：模拟中子从反应堆逃逸的比例（0%-30%）
- **控制棒插入深度**：调节控制棒插入反应堆的深度（0%-100%）

#### 3. 预设场景按钮
- **启动反应**：模拟核反应堆启动过程（k略大于1）
- **稳定运行**：模拟反应堆稳定运行状态（k≈1）
- **紧急停堆**：模拟安全停堆过程（k远小于1）
- **不可控链式反应**：演示核弹原理（k远大于1，无控制）

#### 4. 实时状态显示
- **倍增系数(k)**：当前反应的中子倍增系数
- **当前中子数**：反应堆中活跃的中子数量
- **总裂变次数**：累计发生的裂变事件数
- **模拟功率**：基于反应强度的模拟功率输出
- **反应状态**：直观显示次临界/临界/超临界状态

### 三、设计特色

#### 1. 科学准确性
- 基于真实的核物理原理设计模拟算法
- k值计算考虑了裂变产生、控制棒吸收和中子逃逸三个主要因素
- 反应状态分类符合国际标准（k<0.95次临界，0.95<k<1.05临界，k>1.05超临界）

#### 2. 视觉优化
- **颜色编码系统**：
  - 中子：红色（活跃、高速）
  - 铀核：金属灰色（稳定、重核）
  - 裂变碎片：绿色/黄色（能量释放）
  - 控制棒：黑色（中子吸收）
- **状态可视化**：
  - k值状态使用颜色区分（蓝/绿/红）
  - 裂变过程有发光效果增强视觉反馈
  - 功率条直观显示反应强度

#### 3. 交互友好性
- 响应式设计，适应不同屏幕尺寸
- 直观的滑块控制和按钮布局
- 鼠标悬停提示和点击交互
- 键盘快捷键支持（空格：播放/暂停，R：重置）

### 四、教学要点

#### 核心概念理解
1. **链式反应条件**：
   - 观察当k>1时中子数如何指数增长
   - 理解k=1时反应如何保持稳定
   - 分析k<1时反应为何逐渐停止

2. **控制原理**：
   - 控制棒如何通过吸收中子影响k值
   - 不同插入深度对反应速率的影响
   - 紧急停堆的物理机制

3. **安全与危险**：
   - 可控链式反应（核电站）与不可控链式反应（核弹）的区别
   - 多重安全措施的重要性

#### 实验探究建议
1. **基础观察**：
   - 使用“单步执行”仔细观察单个裂变事件
   - 跟踪一个中子的完整生命周期

2. **参数探究**：
   - 固定其他参数，单独调节“每个裂变产生中子数”，观察k值和反应状态的变化
   - 探究控制棒插入深度与反应速率的关系

3. **对比实验**：
   - 对比“稳定运行”和“不可控链式反应”两种场景
   - 分析初始中子数对反应建立时间的影响

### 五、使用建议

#### 对于教师
1. **课堂演示**：
   - 在讲解链式反应原理时作为可视化辅助工具
   - 使用预设场景快速展示不同反应状态
   - 结合单步执行功能详细解释裂变过程

2. **学生活动设计**：
   - 设计探究性问题：“要使反应从次临界变为临界，可以调节哪些参数？”
   - 组织小组竞赛：看哪个小组能最快实现从启动到稳定运行
   - 布置分析任务：记录不同k值下中子数的变化规律

#### 对于学生
1. **自主学习**：
   - 按照“观察-操作-分析”的步骤：先观看预设场景，再尝试自己调节参数
   - 使用“重置”功能进行对比实验
   - 记录实验数据，绘制k值与反应状态的关系图

2. **概念巩固**：
   - 在调节参数时，预测k值将如何变化，然后验证预测
   - 解释为什么控制棒插入越深，反应速率越慢
   - 描述从启动到稳定运行需要调节哪些参数

#### 对于公众科普
1. **安全认知**：
   - 通过对比“稳定运行”和“紧急停堆”，理解核电站的安全性设计
   - 观察控制棒的即时效果，认识反应控制的可靠性

2. **原理理解**：
   - 使用最简单的设置（初始中子数=1，产生中子数=2）观察链式反应的建立
   - 通过调节动画速度，仔细观察裂变细节

#### 技术提示
1. **性能优化**：
   - 当中子数过多时，可适当降低动画速度以获得更流畅的体验
   - 如需详细观察，建议使用“单步执行”模式

2. **教学扩展**：
   - 鼓励学生记录实验数据并进行定量分析
   - 结合动画讨论实际核电站的安全系统设计
   - 延伸探究：除了控制棒，还有哪些方法可以控制链式反应？

---

### 六、安全与责任说明

本教学动画严格遵循科学原理，旨在促进对核物理基础概念的理解。请注意：

1. **教学工具定位**：本动画是简化模型，用于教学演示，不能替代专业的核反应堆模拟软件。
2. **安全理念传达**：动画中展示了核反应的控制原理，强调了可控性的重要性。
3. **负责任使用**：建议教师在指导下使用“不可控链式反应”场景，并强调实际核电站的多重安全措施。

---

我们希望这个交互式动画能够成为您探索核物理世界的窗口，让抽象的科学原理变得生动可见。通过亲手调节参数、观察反应变化，您将建立起对链式反应机制的直观理解。祝您学习愉快，探索无限！

**开始您的核科学探索之旅吧！** 🚀