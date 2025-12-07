# 需求：生态系统的物质循环与能量流动（碳循环、氮循环全局动态图）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向的是中学生或大学低年级生物学、生态学入门学习者。用户的核心需求是：
1.  **理解抽象过程**：将碳、氮循环这两个复杂的、不可见的全球性生物地球化学过程，转化为直观、动态、可感知的视觉模型。
2.  **区分核心概念**：清晰区分“物质循环”（元素如C、N在不同库/储库间往复流动）与“能量流动”（太阳能输入，沿食物链单向递减耗散）的本质差异。
3.  **建立系统思维**：理解生态系统各组分（生物：生产者、消费者、分解者；非生物：大气、水体、土壤）如何相互连接，构成一个动态整体。
4.  **掌握关键环节**：识别每个循环中的关键生物过程（如光合作用、呼吸作用、固氮作用、硝化作用、反硝化作用）和物理过程（如溶解、沉积、化石燃料燃烧）。
5.  **激发学习兴趣**：通过美观、互动、游戏化的设计，降低认知负荷，让学习过程变得生动有趣。

#### 教学设计思路
*   **核心概念**：
    *   **碳循环**：强调大气CO₂库与生物圈、水圈、岩石圈的交换。核心驱动是光合作用（固碳）与呼吸作用/燃烧（释碳）。突出人类活动（化石燃料燃烧、毁林）对循环的干扰。
    *   **氮循环**：强调大气N₂库的惰性与生物固氮的关键“解锁”作用。核心是氮的形态转化（N₂ → NH₃/NO₃⁻ → 有机氮 → NH₄⁺ → NO₃⁻ → N₂），以及硝化、反硝化等微生物过程。
    *   **能量流动**：以太阳为起点，沿食物链（营养级）单向流动，并以热能形式散失。与物质循环的“循环性”形成鲜明对比。
*   **认知规律**：
    *   **从宏观到微观**：先展示全球尺度的循环全景图，再允许用户点击聚焦到特定过程（如一个土壤微环境中的分解作用）进行详细观察。
    *   **从静态到动态**：初始为静态示意图，启动后元素（碳原子、氮原子、能量包）开始沿路径运动，过程标签高亮显示。
    *   **从观察到操作**：用户先观看自动演示，然后可以通过滑块调节参数（如“化石燃料消耗率”、“化肥使用量”），观察循环平衡如何被打破，从而理解人类影响。
*   **交互设计**：
    *   **模式切换**：提供“碳循环”、“氮循环”、“能量流动”三个主模式，以及一个“对比模式”同时展示物质循环与能量流动。
    *   **过程控制**：播放/暂停/重置按钮。速度调节滑块。
    *   **探索式点击**：点击任何储库（如“大气”、“森林”、“土壤”）、生物角色或过程箭头，弹出详细说明卡片（文字+示意图）。
    *   **参数模拟**：在“人类影响”子模式中，提供交互控件，让用户扮演“决策者”，直观看到其选择带来的后果。
*   **视觉呈现**：
    *   **全局视图**：采用“地球剖面”或“景观俯视图”作为画布背景，将大气、海洋、陆地、地下等空间整合在一个连贯的场景中。
    *   **元素符号化**：
        *   **碳原子**：用小的黑色或深灰色球体表示。
        *   **氮原子**：用小的蓝色球体表示。
        *   **能量**：用发光的黄色粒子或波浪线表示。
        *   **物质流**：用带有方向箭头的半透明色带表示，碳循环用灰色/绿色系，氮循环用蓝色/紫色系。
        *   **能量流**：用明亮的、逐渐变细变暗的黄色/橙色箭头表示。
    *   **动态可视化**：粒子沿路径运动；储库大小随含量变化轻微脉动；过程发生时，相关区域有简洁的动画（如树叶生长表示光合作用，火焰表示燃烧）。

#### 配色方案选择
*   **主背景**：深蓝到浅蓝的渐变（代表天空与大气），底部过渡为绿色/棕色（代表陆地与土壤）。
*   **碳循环主题色**：
    *   大气/海洋中的碳：浅灰色、蓝灰色。
    *   生物体中的碳：生命绿色（植物）、动物色系（消费者）。
    *   化石燃料/岩石中的碳：深棕色、黑色。
    *   碳流动路径：半透明的灰绿色。
*   **氮循环主题色**：
    *   大气氮气（N₂）：天蓝色。
    *   生物可利用氮（NH₄⁺， NO₃⁻）：紫色、品红色。
    *   有机氮：与生物体颜色一致。
    *   氮流动路径：半透明的蓝紫色。
*   **能量流动主题色**：
    *   太阳能：亮黄色、白色。
    *   化学能（在食物链中）：橙色、红色，随着营养级升高逐渐变暗。
    *   热能散失：暗红色，逐渐消散。
*   **交互元素**：按钮、高亮色使用醒目的暖色（如橙色、亮蓝），与背景形成对比。说明卡片使用浅色半透明底衬，确保文字清晰。

#### 交互功能列表
1.  **主控制面板**：
    *   模式选择按钮（碳循环/氮循环/能量流动/对比视图）。
    *   动画控制：播放、暂停、重置。
    *   速度调节滑块。
2.  **探索性交互**：
    *   **点击储库**：如点击“大气CO₂”，显示其当前含量、变化趋势、主要输入输出过程。
    *   **点击生物角色**：如点击“豆科植物”，显示其固氮作用；点击“分解者”，显示其分解过程。
    *   **点击过程箭头**：如点击“光合作用”箭头，播放放大动画并显示化学方程式与文字解释。
3.  **模拟实验交互**（“人类影响”模式）：
    *   **碳循环**：滑块控制“化石燃料燃烧速率”、“森林砍伐面积”。实时观察大气CO₂储库大小变化和全球温度指示计上升。
    *   **氮循环**：滑块控制“化肥施用量”、“汽车尾气排放量”。实时观察水体富营养化指示（水体颜色变绿）和N₂O（温室气体）排放量。
4.  **辅助功能**：
    *   图例开关：显示/隐藏所有元素符号的图例。
    *   过程列表：侧边栏列出所有关键过程，点击可快速定位并高亮该过程。
    *   数据摘要：实时显示关键数据，如“当前碳循环速率”、“氮固定总量”等。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>生态系统物质循环与能量流动教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(to bottom, #0a1a2d, #1a3a5f);
            color: #e0f7ff;
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
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid rgba(255, 213, 79, 0.3);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(to right, #4fc3f7, #a5d6a7);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.5;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 30px;
        }
        
        .animation-container {
            flex: 1;
            min-width: 800px;
            background: rgba(10, 30, 50, 0.7);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(100, 180, 255, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .controls-panel {
            width: 350px;
            background: rgba(15, 40, 70, 0.8);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(120, 200, 255, 0.2);
        }
        
        .panel-section {
            margin-bottom: 30px;
        }
        
        .panel-title {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: #81d4fa;
            padding-bottom: 8px;
            border-bottom: 1px solid rgba(129, 212, 250, 0.3);
        }
        
        .mode-buttons {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
            margin-bottom: 20px;
        }
        
        .mode-btn {
            padding: 14px 10px;
            background: rgba(30, 70, 120, 0.8);
            border: 2px solid rgba(100, 180, 255, 0.3);
            border-radius: 10px;
            color: #e0f7ff;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .mode-btn:hover {
            background: rgba(40, 90, 150, 0.9);
            transform: translateY(-2px);
        }
        
        .mode-btn.active {
            background: rgba(79, 195, 247, 0.25);
            border-color: #4fc3f7;
            box-shadow: 0 0 15px rgba(79, 195, 247, 0.4);
        }
        
        .control-buttons {
            display: flex;
            gap: 15px;
            margin-bottom: 25px;
        }
        
        .control-btn {
            flex: 1;
            padding: 14px;
            border: none;
            border-radius: 10px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .play-btn {
            background: linear-gradient(to right, #2e7d32, #4caf50);
            color: white;
        }
        
        .reset-btn {
            background: linear-gradient(to right, #1565c0, #2196f3);
            color: white;
        }
        
        .control-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .slider-container {
            margin-bottom: 20px;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }
        
        .slider-value {
            color: #ffcc80;
            font-weight: 600;
        }
        
        .slider {
            width: 100%;
            height: 10px;
            -webkit-appearance: none;
            appearance: none;
            background: rgba(50, 100, 150, 0.7);
            border-radius: 5px;
            outline: none;
        }
        
        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #4fc3f7;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
        }
        
        .info-panel {
            background: rgba(20, 50, 90, 0.8);
            border-radius: 15px;
            padding: 25px;
            margin-top: 25px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(120, 200, 255, 0.2);
        }
        
        .info-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: #a5d6a7;
        }
        
        .info-content {
            line-height: 1.6;
            font-size: 1.05rem;
        }
        
        .highlight {
            color: #ffcc80;
            font-weight: 600;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            padding-top: 15px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }
        
        canvas {
            display: block;
            border-radius: 10px;
            background: rgba(5, 20, 40, 0.9);
        }
        
        .data-display {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-top: 20px;
        }
        
        .data-item {
            background: rgba(30, 70, 120, 0.5);
            padding: 12px;
            border-radius: 8px;
            text-align: center;
            border-left: 4px solid #4fc3f7;
        }
        
        .data-value {
            font-size: 1.4rem;
            font-weight: 700;
            color: #ffcc80;
            margin-top: 5px;
        }
        
        .data-label {
            font-size: 0.9rem;
            opacity: 0.9;
        }
        
        .human-impact-controls {
            background: rgba(120, 40, 40, 0.2);
            padding: 15px;
            border-radius: 10px;
            margin-top: 15px;
            border: 1px solid rgba(255, 100, 100, 0.3);
        }
        
        .impact-title {
            color: #ffab91;
            font-size: 1.1rem;
            margin-bottom: 10px;
        }
        
        @media (max-width: 1200px) {
            .main-content {
                flex-direction: column;
            }
            
            .animation-container, .controls-panel {
                min-width: 100%;
            }
        }
        
        .click-hint {
            position: absolute;
            bottom: 15px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0, 0, 0, 0.7);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            color: #b3e5fc;
            border: 1px solid rgba(179, 229, 252, 0.3);
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>生态系统物质循环与能量流动</h1>
            <p class="subtitle">探索碳循环、氮循环与能量流动的全球动态过程。点击画布中的元素查看详细信息，调整参数观察人类活动的影响。</p>
        </header>
        
        <div class="main-content">
            <div class="animation-container">
                <canvas id="ecosystemCanvas" width="1100" height="700"></canvas>
                <div class="click-hint">💡 提示：点击画布中的元素（储库、生物、箭头）查看详细信息</div>
            </div>
            
            <div class="controls-panel">
                <div class="panel-section">
                    <h3 class="panel-title">模式选择</h3>
                    <div class="mode-buttons">
                        <button class="mode-btn active" data-mode="carbon">碳循环</button>
                        <button class="mode-btn" data-mode="nitrogen">氮循环</button>
                        <button class="mode-btn" data-mode="energy">能量流动</button>
                        <button class="mode-btn" data-mode="compare">对比视图</button>
                    </div>
                    
                    <div class="control-buttons">
                        <button class="control-btn play-btn" id="playBtn">▶ 播放</button>
                        <button class="control-btn reset-btn" id="resetBtn">↺ 重置</button>
                    </div>
                    
                    <div class="slider-container">
                        <div class="slider-label">
                            <span>动画速度</span>
                            <span class="slider-value" id="speedValue">1.0x</span>
                        </div>
                        <input type="range" min="0.1" max="3" step="0.1" value="1" class="slider" id="speedSlider">
                    </div>
                </div>
                
                <div class="panel-section">
                    <h3 class="panel-title">人类活动影响模拟</h3>
                    <div class="human-impact-controls">
                        <div class="impact-title">碳循环影响</div>
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>化石燃料燃烧</span>
                                <span class="slider-value" id="fuelValue">50%</span>
                            </div>
                            <input type="range" min="0" max="100" step="1" value="50" class="slider" id="fuelSlider">
                        </div>
                        
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>森林砍伐</span>
                                <span class="slider-value" id="deforestValue">30%</span>
                            </div>
                            <input type="range" min="0" max="100" step="1" value="30" class="slider" id="deforestSlider">
                        </div>
                        
                        <div class="impact-title" style="margin-top: 15px;">氮循环影响</div>
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>化肥使用</span>
                                <span class="slider-value" id="fertilizerValue">40%</span>
                            </div>
                            <input type="range" min="0" max="100" step="1" value="40" class="slider" id="fertilizerSlider">
                        </div>
                    </div>
                </div>
                
                <div class="data-display">
                    <div class="data-item">
                        <div class="data-label">大气CO₂浓度</div>
                        <div class="data-value" id="co2Value">415 ppm</div>
                    </div>
                    <div class="data-item">
                        <div class="data-label">全球温度变化</div>
                        <div class="data-value" id="tempValue">+1.2°C</div>
                    </div>
                    <div class="data-item">
                        <div class="data-label">氮固定总量</div>
                        <div class="data-value" id="nitrogenValue">140 Tg/年</div>
                    </div>
                    <div class="data-item">
                        <div class="data-label">能量传递效率</div>
                        <div class="data-value" id="energyValue">10%</div>
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #4db6ac;"></div>
                        <span>碳原子</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #7986cb;"></div>
                        <span>氮原子</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ffb74d;"></div>
                        <span>能量粒子</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #81c784;"></div>
                        <span>生产者</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="info-panel">
            <h3 class="info-title" id="infoTitle">生态系统物质循环与能量流动</h3>
            <div class="info-content" id="infoContent">
                欢迎使用生态系统教学动画！请选择一种模式开始探索：
                <br><br>
                <span class="highlight">碳循环</span>：碳元素在大气、生物、海洋和地壳之间的循环过程。
                <br>
                <span class="highlight">氮循环</span>：氮元素在大气、生物和土壤之间的转化与循环过程。
                <br>
                <span class="highlight">能量流动</span>：太阳能如何通过食物链传递，并以热能形式散失。
                <br>
                <span class="highlight">对比视图</span>：同时展示物质循环与能量流动，理解两者的本质差异。
                <br><br>
                点击画布中的任何元素（储库、生物角色、过程箭头）查看详细信息。
            </div>
        </div>
    </div>

    <script>
        // 全局变量
        const canvas = document.getElementById('ecosystemCanvas');
        const ctx = canvas.getContext('2d');
        let animationId = null;
        let isPlaying = true;
        let currentMode = 'carbon';
        let animationSpeed = 1.0;
        let time = 0;
        
        // 人类活动影响参数
        let humanImpact = {
            fuelBurning: 0.5,    // 化石燃料燃烧强度 (0-1)
            deforestation: 0.3,  // 森林砍伐程度 (0-1)
            fertilizerUse: 0.4   // 化肥使用强度 (0-1)
        };
        
        // 数据状态
        let dataState = {
            co2Concentration: 415,  // ppm
            temperatureChange: 1.2, // °C
            nitrogenFixed: 140,     // Tg/年
            energyEfficiency: 10    // %
        };
        
        // 生态系统元素定义
        const elements = {
            reservoirs: [
                { id: 'atmosphere', name: '大气', x: 550, y: 100, radius: 80, color: '#81d4fa', type: 'carbon', content: 'CO₂, N₂' },
                { id: 'forest', name: '森林', x: 300, y: 400, radius: 70, color: '#66bb6a', type: 'carbon', content: '有机碳' },
                { id: 'ocean', name: '海洋', x: 800, y: 500, radius: 90, color: '#29b6f6', type: 'carbon', content: '溶解碳' },
                { id: 'soil', name: '土壤', x: 550, y: 550, radius: 60, color: '#8d6e63', type: 'both', content: '有机质, 硝酸盐' },
                { id: 'fossil', name: '化石燃料', x: 850, y: 300, radius: 50, color: '#5d4037', type: 'carbon', content: '煤, 石油, 天然气' }
            ],
            
            organisms: [
                { id: 'producers', name: '生产者', x: 300, y: 300, radius: 40, color: '#81c784', type: 'both' },
                { id: 'consumers', name: '消费者', x: 400, y: 350, radius: 35, color: '#ffb74d', type: 'both' },
                { id: 'decomposers', name: '分解者', x: 550, y: 600, radius: 30, color: '#ba68c8', type: 'both' },
                { id: 'nitrogenFixers', name: '固氮生物', x: 700, y: 400, radius: 35, color: '#64b5f6', type: 'nitrogen' }
            ],
            
            processes: [
                { id: 'photosynthesis', name: '光合作用', from: 'atmosphere', to: 'producers', color: '#4caf50', width: 4, type: 'carbon' },
                { id: 'respiration', name: '呼吸作用', from: 'producers', to: 'atmosphere', color: '#ff9800', width: 3, type: 'carbon' },
                { id: 'consumption', name: '摄食', from: 'producers', to: 'consumers', color: '#ffb74d', width: 3, type: 'both' },
                { id: 'decomposition', name: '分解作用', from: 'consumers', to: 'soil', color: '#8d6e63', width: 3, type: 'both' },
                { id: 'fossilBurning', name: '化石燃料燃烧', from: 'fossil', to: 'atmosphere', color: '#f44336', width: 4, type: 'carbon' },
                { id: 'oceanUptake', name: '海洋吸收', from: 'atmosphere', to: 'ocean', color: '#29b6f6', width: 3, type: 'carbon' },
                { id: 'nitrogenFixation', name: '固氮作用', from: 'atmosphere', to: 'nitrogenFixers', color: '#7986cb', width: 4, type: 'nitrogen' },
                { id: 'nitrogenToSoil', name: '氮进入土壤', from: 'nitrogenFixers', to: 'soil', color: '#9575cd', width: 3, type: 'nitrogen' },
                { id: 'plantUptake', name: '植物吸收', from: 'soil', to: 'producers', color: '#4db6ac', width: 3, type: 'both' }
            ],
            
            energyFlow: [
                { id: 'sunToProducers', name: '太阳能输入', from: {x: 100, y: 150}, to: 'producers', color: '#ffeb3b', width: 5, type: 'energy' },
                { id: 'producersToConsumers', name: '初级消费者', from: 'producers', to: 'consumers', color: '#ffb74d', width: 4, type: 'energy' },
                { id: 'consumersToDecomposers', name: '次级消费者/分解', from: 'consumers', to: 'decomposers', color: '#ff9800', width: 3, type: 'energy' },
                { id: 'energyLoss', name: '热能散失', from: 'decomposers', to: {x: 1000, y: 100}, color: '#f44336', width: 2, type: 'energy' }
            ]
        };
        
        // 粒子系统
        const particles = {
            carbon: [],
            nitrogen: [],
            energy: []
        };
        
        // 初始化粒子
        function initParticles() {
            particles.carbon = [];
            particles.nitrogen = [];
            particles.energy = [];
            
            // 创建碳粒子
            for (let i = 0; i < 50; i++) {
                particles.carbon.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    size: 4 + Math.random() * 3,
                    speed: 0.5 + Math.random() * 1,
                    path: null,
                    progress: Math.random(),
                    color: '#4db6ac'
                });
            }
            
            // 创建氮粒子
            for (let i = 0; i < 40; i++) {
                particles.nitrogen.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    size: 4 + Math.random() * 3,
                    speed: 0.5 + Math.random() * 1,
                    path: null,
                    progress: Math.random(),
                    color: '#7986cb'
                });
            }
            
            // 创建能量粒子
            for (let i = 0; i < 30; i++) {
                particles.energy.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    size: 5 + Math.random() * 4,
                    speed: 1 + Math.random() * 1.5,
                    path: null,
                    progress: Math.random(),
                    color: '#ffb74d',
                    glow: true
                });
            }
        }
        
        // 获取元素位置
        function getElementPosition(id) {
            // 检查是否是储库
            const reservoir = elements.reservoirs.find(r => r.id === id);
            if (reservoir) return {x: reservoir.x, y: reservoir.y};
            
            // 检查是否是生物
            const organism = elements.organisms.find(o => o.id === id);
            if (organism) return {x: organism.x, y: organism.y};
            
            return null;
        }
        
        // 绘制背景
        function drawBackground() {
            // 天空渐变
            const skyGradient = ctx.createLinearGradient(0, 0, 0, canvas.height);
            skyGradient.addColorStop(0, '#0a1a2d');
            skyGradient.addColorStop(1, '#1a3a5f');
            ctx.fillStyle = skyGradient;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 陆地
            ctx.fillStyle = '#2e7d32';
            ctx.beginPath();
            ctx.moveTo(0, canvas.height);
            ctx.bezierCurveTo(200, 500, 400, 550, canvas.width, canvas.height);
            ctx.lineTo(canvas.width, canvas.height);
            ctx.lineTo(0, canvas.height);
            ctx.closePath();
            ctx.fill();
            
            // 海洋
            ctx.fillStyle = '#1565c0';
            ctx.beginPath();
            ctx.moveTo(0, canvas.height);
            ctx.bezierCurveTo(300, 600, 700, 550, canvas.width, canvas.height);
            ctx.lineTo(canvas.width, canvas.height);
            ctx.lineTo(0, canvas.height);
            ctx.closePath();
            ctx.fill();
            
            // 太阳（能量模式）
            if (currentMode === 'energy' || currentMode === 'compare') {
                ctx.beginPath();
                const sunX = 100, sunY = 150, sunRadius = 40;
                const sunGradient = ctx.createRadialGradient(sunX, sunY, 5, sunX, sunY, sunRadius);
                sunGradient.addColorStop(0, '#ffff00');
                sunGradient.addColorStop(1, '#ff9800');
                ctx.fillStyle = sunGradient;
                ctx.arc(sunX, sunY, sunRadius, 0, Math.PI * 2);
                ctx.fill();
                
                // 太阳光芒
                ctx.strokeStyle = 'rgba(255, 235, 59, 0.7)';
                ctx.lineWidth = 3;
                for (let i = 0; i < 12; i++) {
                    const angle = (i * Math.PI) / 6;
                    const startX = sunX + Math.cos(angle) * sunRadius;
                    const startY = sunY + Math.sin(angle) * sunRadius;
                    const endX = sunX + Math.cos(angle) * (sunRadius + 25);
                    const endY = sunY + Math.sin(angle) * (sunRadius + 25);
                    
                    ctx.beginPath();
                    ctx.moveTo(startX, startY);
                    ctx.lineTo(endX, endY);
                    ctx.stroke();
                }
                
                ctx.fillStyle = '#fff';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('太阳', sunX, sunY + sunRadius + 25);
            }
        }
        
        // 绘制储库
        function drawReservoirs() {
            elements.reservoirs.forEach(reservoir => {
                // 根据当前模式决定是否绘制
                if (currentMode === 'carbon' && !reservoir.type.includes('carbon')) return;
                if (currentMode === 'nitrogen' && !reservoir.type.includes('both')) return;
                if (currentMode === 'energy') return;
                
                // 绘制储库圆圈
                ctx.beginPath();
                ctx.arc(reservoir.x, reservoir.y, reservoir.radius, 0, Math.PI * 2);
                
                // 根据人类影响调整颜色
                let color = reservoir.color;
                if (reservoir.id === 'atmosphere' && humanImpact.fuelBurning > 0.5) {
                    color = '#ff8a65'; // 大气受污染变橙色
                }
                if (reservoir.id === 'forest' && humanImpact.deforestation > 0.5) {
                    color = '#a1887f'; // 森林砍伐变棕色
                }
                
                ctx.fillStyle = color + '80'; // 80表示50%透明度
                ctx.fill();
                
                ctx.strokeStyle = color;
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 绘制储库标签
                ctx.fillStyle = '#fff';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(reservoir.name, reservoir.x, reservoir.y - reservoir.radius - 10);
                
                // 绘制储库内容
                ctx.font = '14px Arial';
                ctx.fillText(reservoir.content, reservoir.x, reservoir.y + 5);
            });
        }
        
        // 绘制生物
        function drawOrganisms() {
            elements.organisms.forEach(organism => {
                // 根据当前模式决定是否绘制
                if (currentMode === 'carbon' && organism.type === 'nitrogen') return;
                if (currentMode === 'nitrogen' && organism.type === 'carbon') return;
                if (currentMode === 'energy' && organism.id !== 'producers' && 
                    organism.id !== 'consumers' && organism.id !== 'decomposers') return;
                
                // 绘制生物圆圈
                ctx.beginPath();
                ctx.arc(organism.x, organism.y, organism.radius, 0, Math.PI * 2);
                ctx.fillStyle = organism.color + '80';
                ctx.fill();
                
                ctx.strokeStyle = organism.color;
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 绘制生物标签
                ctx.fillStyle = '#fff';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                
                // 根据生物类型调整标签位置
                let labelY = organism.y - organism.radius - 10;
                if (organism.id === 'decomposers') labelY = organism.y + organism.radius + 20;
                
                ctx.fillText(organism.name, organism.x, labelY);
            });
        }
        
        // 绘制过程箭头
        function drawProcesses() {
            // 绘制物质循环过程
            if (currentMode !== 'energy') {
                elements.processes.forEach(process => {
                    // 根据当前模式过滤
                    if (currentMode === 'carbon' && process.type !== 'carbon') return;
                    if (currentMode === 'nitrogen' && process.type !== 'nitrogen') return;
                    
                    const fromPos = getElementPosition(process.from);
                    const toPos = getElementPosition(process.to);
                    
                    if (!fromPos || !toPos) return;
                    
                    drawArrow(fromPos.x, fromPos.y, toPos.x, toPos.y, process.color, process.width, process.name);
                });
            }
            
            // 绘制能量流动过程
            if (currentMode === 'energy' || currentMode === 'compare') {
                elements.energyFlow.forEach(flow => {
                    let fromPos, toPos;
                    
                    // 处理起始点
                    if (typeof flow.from === 'object') {
                        fromPos = flow.from;
                    } else {
                        fromPos = getElementPosition(flow.from);
                    }
                    
                    // 处理终点
                    if (typeof flow.to === 'object') {
                        toPos = flow.to;
                    } else {
                        toPos = getElementPosition(flow.to);
                    }
                    
                    if (!fromPos || !toPos) return;
                    
                    // 能量流动使用不同的箭头样式
                    drawEnergyArrow(fromPos.x, fromPos.y, toPos.x, toPos.y, flow.color, flow.width, flow.name);
                });
            }
        }
        
        // 绘制普通箭头
        function drawArrow(fromX, fromY, toX, toY, color, width, label) {
            // 计算角度
            const angle = Math.atan2(toY - fromY, toX - fromX);
            const headLength = 15;
            const distance = Math.sqrt(Math.pow(toX - fromX, 2) + Math.pow(toY - fromY, 2));
            
            // 调整起点和终点，避免与圆圈重叠
            const fromElement = [...elements.reservoirs, ...elements.organisms].find(e => 
                Math.abs(e.x - fromX) < 5 && Math.abs(e.y - fromY) < 5);
            const toElement = [...elements.reservoirs, ...elements.organisms].find(e => 
                Math.abs(e.x - toX) < 5 && Math.abs(e.y - toY) < 5);
            
            let startX = fromX, startY = fromY;
            let endX = toX, endY = toY;
            
            if (fromElement) {
                const radius = fromElement.radius + 5;
                startX = fromX + Math.cos(angle) * radius;
                startY = fromY + Math.sin(angle) * radius;
            }
            
            if (toElement) {
                const radius = toElement.radius + 5;
                endX = toX - Math.cos(angle) * radius;
                endY = toY - Math.sin(angle) * radius;
            }
            
            // 绘制箭头线
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            ctx.lineTo(endX, endY);
            ctx.strokeStyle = color;
            ctx.lineWidth = width;
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(endX, endY);
            ctx.lineTo(
                endX - headLength * Math.cos(angle - Math.PI / 7),
                endY - headLength * Math.sin(angle - Math.PI / 7)
            );
            ctx.lineTo(
                endX - headLength * Math.cos(angle + Math.PI / 7),
                endY - headLength * Math.sin(angle + Math.PI / 7)
            );
            ctx.closePath();
            ctx.fillStyle = color;
            ctx.fill();
            
            // 绘制过程标签
            if (label && distance > 80) {
                const midX = (startX + endX) / 2;
                const midY = (startY + endY) / 2;
                
                ctx.save();
                ctx.translate(midX, midY);
                ctx.rotate(angle);
                
                ctx.fillStyle = '#fff';
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(label, 0, -10);
                
                ctx.restore();
            }
        }
        
        // 绘制能量箭头（渐变、发光效果）
        function drawEnergyArrow(fromX, fromY, toX, toY, color, width, label) {
            const angle = Math.atan2(toY - fromY, toX - fromX);
            const headLength = 20;
            const distance = Math.sqrt(Math.pow(toX - fromX, 2) + Math.pow(toY - fromY, 2));
            
            // 调整起点和终点
            const fromElement = [...elements.reservoirs, ...elements.organisms].find(e => 
                Math.abs(e.x - fromX) < 5 && Math.abs(e.y - fromY) < 5);
            const toElement = [...elements.reservoirs, ...elements.organisms].find(e => 
                Math.abs(e.x - toX) < 5 && Math.abs(e.y - toY) < 5);
            
            let startX = fromX, startY = fromY;
            let endX = toX, endY = toY;
            
            if (fromElement) {
                const radius = fromElement.radius + 5;
                startX = fromX + Math.cos(angle) * radius;
                startY = fromY + Math.sin(angle) * radius;
            }
            
            if (toElement) {
                const radius = toElement.radius + 5;
                endX = toX - Math.cos(angle) * radius;
                endY = toY - Math.sin(angle) * radius;
            }
            
            // 创建能量流动的渐变
            const gradient = ctx.createLinearGradient(startX, startY, endX, endY);
            gradient.addColorStop(0, color);
            gradient.addColorStop(1, '#f44336'); // 能量逐渐耗散为热能
            
            // 绘制能量流线
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            ctx.lineTo(endX, endY);
            ctx.strokeStyle = gradient;
            ctx.lineWidth = width;
            ctx.lineCap = 'round';
            ctx.stroke();
            
            // 添加发光效果
            ctx.shadowColor = color;
            ctx.shadowBlur =
<!--检测到代码截断，自动续写中...-->
15;
            ctx.beginPath();
            ctx.moveTo(startX, startY);
            ctx.lineTo(endX, endY);
            ctx.stroke();
            ctx.shadowBlur = 0;
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(endX, endY);
            ctx.lineTo(
                endX - headLength * Math.cos(angle - Math.PI / 7),
                endY - headLength * Math.sin(angle - Math.PI / 7)
            );
            ctx.lineTo(
                endX - headLength * Math.cos(angle + Math.PI / 7),
                endY - headLength * Math.sin(angle + Math.PI / 7)
            );
            ctx.closePath();
            ctx.fillStyle = gradient;
            ctx.fill();
            
            // 绘制能量标签
            if (label && distance > 80) {
                const midX = (startX + endX) / 2;
                const midY = (startY + endY) / 2;
                
                ctx.save();
                ctx.translate(midX, midY);
                ctx.rotate(angle);
                
                ctx.fillStyle = '#ffeb3b';
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(label, 0, -15);
                
                // 绘制能量损失百分比（仅对能量流动）
                if (label.includes('消费者') || label.includes('分解')) {
                    const efficiency = label.includes('初级') ? '10%' : '1%';
                    ctx.font = '12px Arial';
                    ctx.fillText(`效率: ${efficiency}`, 0, 5);
                }
                
                ctx.restore();
            }
        }
        
        // 绘制粒子
        function drawParticles() {
            // 更新并绘制碳粒子
            if (currentMode === 'carbon' || currentMode === 'compare') {
                particles.carbon.forEach(particle => {
                    // 更新粒子位置
                    particle.progress += 0.005 * animationSpeed;
                    if (particle.progress > 1) particle.progress = 0;
                    
                    // 让粒子沿简单路径移动
                    particle.x = 550 + Math.cos(time * 0.5 + particle.progress * Math.PI * 2) * 400;
                    particle.y = 350 + Math.sin(time * 0.3 + particle.progress * Math.PI * 2) * 250;
                    
                    // 绘制粒子
                    ctx.beginPath();
                    ctx.arc(particle.x, particle.y, particle.size, 0, Math.PI * 2);
                    ctx.fillStyle = particle.color;
                    ctx.fill();
                    
                    // 添加轻微发光效果
                    ctx.shadowColor = particle.color;
                    ctx.shadowBlur = 8;
                    ctx.fill();
                    ctx.shadowBlur = 0;
                });
            }
            
            // 更新并绘制氮粒子
            if (currentMode === 'nitrogen' || currentMode === 'compare') {
                particles.nitrogen.forEach(particle => {
                    particle.progress += 0.004 * animationSpeed;
                    if (particle.progress > 1) particle.progress = 0;
                    
                    particle.x = 550 + Math.cos(time * 0.4 + particle.progress * Math.PI * 2) * 350;
                    particle.y = 400 + Math.sin(time * 0.5 + particle.progress * Math.PI * 2) * 200;
                    
                    ctx.beginPath();
                    ctx.arc(particle.x, particle.y, particle.size, 0, Math.PI * 2);
                    ctx.fillStyle = particle.color;
                    ctx.fill();
                    
                    ctx.shadowColor = particle.color;
                    ctx.shadowBlur = 8;
                    ctx.fill();
                    ctx.shadowBlur = 0;
                });
            }
            
            // 更新并绘制能量粒子
            if (currentMode === 'energy' || currentMode === 'compare') {
                particles.energy.forEach(particle => {
                    particle.progress += 0.008 * animationSpeed;
                    if (particle.progress > 1) particle.progress = 0;
                    
                    // 能量粒子沿能量流动路径移动
                    const pathProgress = particle.progress;
                    let x, y;
                    
                    if (pathProgress < 0.25) {
                        // 从太阳到生产者
                        x = 100 + (300 - 100) * (pathProgress * 4);
                        y = 150 + (300 - 150) * (pathProgress * 4);
                    } else if (pathProgress < 0.5) {
                        // 从生产者到消费者
                        x = 300 + (400 - 300) * ((pathProgress - 0.25) * 4);
                        y = 300 + (350 - 300) * ((pathProgress - 0.25) * 4);
                    } else if (pathProgress < 0.75) {
                        // 从消费者到分解者
                        x = 400 + (550 - 400) * ((pathProgress - 0.5) * 4);
                        y = 350 + (600 - 350) * ((pathProgress - 0.5) * 4);
                    } else {
                        // 从分解者散失到大气
                        x = 550 + (1000 - 550) * ((pathProgress - 0.75) * 4);
                        y = 600 + (100 - 600) * ((pathProgress - 0.75) * 4);
                    }
                    
                    particle.x = x;
                    particle.y = y;
                    
                    // 随着能量传递，粒子变小变暗
                    const sizeFactor = 1 - (pathProgress * 0.7);
                    const alpha = 1 - (pathProgress * 0.8);
                    
                    ctx.beginPath();
                    ctx.arc(particle.x, particle.y, particle.size * sizeFactor, 0, Math.PI * 2);
                    ctx.fillStyle = `rgba(255, 183, 77, ${alpha})`;
                    ctx.fill();
                    
                    if (particle.glow) {
                        ctx.shadowColor = '#ffeb3b';
                        ctx.shadowBlur = 15;
                        ctx.fill();
                        ctx.shadowBlur = 0;
                    }
                });
            }
        }
        
        // 绘制人类活动影响
        function drawHumanImpact() {
            // 绘制化石燃料燃烧效果
            if (humanImpact.fuelBurning > 0.3 && (currentMode === 'carbon' || currentMode === 'compare')) {
                const intensity = humanImpact.fuelBurning;
                const fossil = elements.reservoirs.find(r => r.id === 'fossil');
                
                // 绘制烟雾
                for (let i = 0; i < 5 * intensity; i++) {
                    const smokeX = fossil.x + Math.cos(time * 2 + i) * 30;
                    const smokeY = fossil.y - 50 - (time * 20 + i * 10) % 100;
                    const smokeSize = 10 + Math.sin(time + i) * 5;
                    
                    ctx.beginPath();
                    ctx.arc(smokeX, smokeY, smokeSize, 0, Math.PI * 2);
                    ctx.fillStyle = `rgba(100, 100, 100, ${0.3 * intensity})`;
                    ctx.fill();
                }
                
                // 绘制火焰
                if (intensity > 0.5) {
                    ctx.fillStyle = `rgba(255, 69, 0, ${0.6 * intensity})`;
                    ctx.beginPath();
                    ctx.moveTo(fossil.x - 20, fossil.y);
                    ctx.bezierCurveTo(
                        fossil.x - 15, fossil.y - 40,
                        fossil.x + 15, fossil.y - 40,
                        fossil.x + 20, fossil.y
                    );
                    ctx.bezierCurveTo(
                        fossil.x + 10, fossil.y - 20,
                        fossil.x - 10, fossil.y - 20,
                        fossil.x - 20, fossil.y
                    );
                    ctx.closePath();
                    ctx.fill();
                }
            }
            
            // 绘制森林砍伐效果
            if (humanImpact.deforestation > 0.3 && (currentMode === 'carbon' || currentMode === 'compare')) {
                const forest = elements.reservoirs.find(r => r.id === 'forest');
                const stumpsCount = Math.floor(humanImpact.deforestation * 5);
                
                // 绘制树桩
                for (let i = 0; i < stumpsCount; i++) {
                    const stumpX = forest.x - 40 + (i % 3) * 40;
                    const stumpY = forest.y - 20 + Math.floor(i / 3) * 30;
                    
                    ctx.fillStyle = '#8d6e63';
                    ctx.fillRect(stumpX - 5, stumpY - 5, 10, 10);
                    
                    // 年轮
                    ctx.strokeStyle = '#5d4037';
                    ctx.beginPath();
                    ctx.arc(stumpX, stumpY, 3, 0, Math.PI * 2);
                    ctx.stroke();
                }
            }
            
            // 绘制化肥使用效果（氮污染）
            if (humanImpact.fertilizerUse > 0.3 && (currentMode === 'nitrogen' || currentMode === 'compare')) {
                const soil = elements.reservoirs.find(r => r.id === 'soil');
                
                // 绘制化肥颗粒
                for (let i = 0; i < 10 * humanImpact.fertilizerUse; i++) {
                    const grainX = soil.x - 30 + Math.random() * 60;
                    const grainY = soil.y - 20 + Math.random() * 40;
                    const grainSize = 2 + Math.random() * 3;
                    
                    ctx.beginPath();
                    ctx.arc(grainX, grainY, grainSize, 0, Math.PI * 2);
                    ctx.fillStyle = `rgba(255, 235, 59, ${0.7 * humanImpact.fertilizerUse})`;
                    ctx.fill();
                }
                
                // 绘制水体富营养化（如果海洋可见）
                if (currentMode !== 'carbon') {
                    const ocean = elements.reservoirs.find(r => r.id === 'ocean');
                    ctx.fillStyle = `rgba(76, 175, 80, ${0.3 * humanImpact.fertilizerUse})`;
                    ctx.beginPath();
                    ctx.arc(ocean.x, ocean.y, ocean.radius * 0.9, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
        }
        
        // 更新数据展示
        function updateDataDisplay() {
            // 根据人类活动影响更新数据
            dataState.co2Concentration = 415 + humanImpact.fuelBurning * 100 + humanImpact.deforestation * 50;
            dataState.temperatureChange = 1.2 + (humanImpact.fuelBurning * 0.8) + (humanImpact.deforestation * 0.4);
            dataState.nitrogenFixed = 140 + humanImpact.fertilizerUse * 60;
            
            // 能量效率随着污染略微降低
            dataState.energyEfficiency = 10 - (humanImpact.fuelBurning * 2) - (humanImpact.fertilizerUse * 1);
            if (dataState.energyEfficiency < 5) dataState.energyEfficiency = 5;
            
            // 更新DOM元素
            document.getElementById('co2Value').textContent = Math.round(dataState.co2Concentration) + ' ppm';
            document.getElementById('tempValue').textContent = '+' + dataState.temperatureChange.toFixed(1) + '°C';
            document.getElementById('nitrogenValue').textContent = Math.round(dataState.nitrogenFixed) + ' Tg/年';
            document.getElementById('energyValue').textContent = dataState.energyEfficiency.toFixed(1) + '%';
            
            // 更新滑块值显示
            document.getElementById('fuelValue').textContent = Math.round(humanImpact.fuelBurning * 100) + '%';
            document.getElementById('deforestValue').textContent = Math.round(humanImpact.deforestation * 100) + '%';
            document.getElementById('fertilizerValue').textContent = Math.round(humanImpact.fertilizerUse * 100) + '%';
        }
        
        // 主绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 绘制生态系统元素
            drawReservoirs();
            drawOrganisms();
            drawProcesses();
            
            // 绘制人类活动影响
            drawHumanImpact();
            
            // 绘制粒子
            drawParticles();
            
            // 更新时间
            time += 0.05 * animationSpeed;
            
            // 更新数据展示
            updateDataDisplay();
            
            // 继续动画循环
            if (isPlaying) {
                animationId = requestAnimationFrame(draw);
            }
        }
        
        // 处理画布点击事件
        function handleCanvasClick(event) {
            const rect = canvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;
            
            // 检查是否点击了储库
            for (const reservoir of elements.reservoirs) {
                const distance = Math.sqrt(Math.pow(x - reservoir.x, 2) + Math.pow(y - reservoir.y, 2));
                if (distance <= reservoir.radius) {
                    showInfo(reservoir.name, getReservoirInfo(reservoir.id));
                    return;
                }
            }
            
            // 检查是否点击了生物
            for (const organism of elements.organisms) {
                const distance = Math.sqrt(Math.pow(x - organism.x, 2) + Math.pow(y - organism.y, 2));
                if (distance <= organism.radius) {
                    showInfo(organism.name, getOrganismInfo(organism.id));
                    return;
                }
            }
            
            // 如果没有点击任何元素，显示默认信息
            showDefaultInfo();
        }
        
        // 获取储库信息
        function getReservoirInfo(id) {
            const info = {
                atmosphere: `大气是碳循环和氮循环的关键储库。<br><br>
                           <span class="highlight">碳循环</span>: 大气中含有二氧化碳(CO₂)，是光合作用的原料，也是呼吸作用和燃烧的产物。<br>
                           <span class="highlight">氮循环</span>: 大气中78%是氮气(N₂)，但大多数生物无法直接利用。<br><br>
                           当前CO₂浓度: <span class="highlight">${dataState.co2Concentration.toFixed(0)} ppm</span><br>
                           人类活动使大气CO₂浓度比工业革命前增加了约50%。`,
                
                forest: `森林是重要的碳汇和生物多样性宝库。<br><br>
                        <span class="highlight">碳储存</span>: 森林通过光合作用吸收大气中的CO₂，将碳固定在生物质中。<br>
                        <span class="highlight">氮循环</span>: 森林参与氮的吸收和转化，维持土壤肥力。<br><br>
                        当前森林砍伐程度: <span class="highlight">${Math.round(humanImpact.deforestation * 100)}%</span><br>
                        森林砍伐会释放储存的碳，加剧气候变化。`,
                
                ocean: `海洋是地球上最大的碳汇，吸收了约30%人类排放的CO₂。<br><br>
                       <span class="highlight">碳循环</span>: 海洋通过物理溶解和生物泵吸收大气CO₂。<br>
                       <span class="highlight">氮循环</span>: 海洋中的蓝藻等生物可以进行固氮作用。<br><br>
                       海洋酸化: 吸收过多CO₂导致海水pH值下降，影响海洋生物。`,
                
                soil: `土壤是物质循环的重要枢纽。<br><br>
                      <span class="highlight">碳循环</span>: 土壤有机质是巨大的碳库，分解者将有机物分解为CO₂。<br>
                      <span class="highlight">氮循环</span>: 土壤中进行着硝化、反硝化等关键氮转化过程。<br><br>
                      土壤健康直接影响生态系统的生产力和稳定性。`,
                
                fossil: `化石燃料是古代生物经过数百万年形成的碳储存库。<br><br>
                        <span class="highlight">碳循环</span>: 燃烧化石燃料会快速释放大量CO₂到大气中，打破自然碳平衡。<br><br>
                        当前化石燃料燃烧强度: <span class="highlight">${Math.round(humanImpact.fuelBurning * 100)}%</span><br>
                        这是当前全球变暖的主要原因之一。`
            };
            
            return info[id] || "信息未找到。";
        }
        
        // 获取生物信息
        function getOrganismInfo(id) {
            const info = {
                producers: `生产者（主要是植物和藻类）是生态系统的能量基础。<br><br>
                          <span class="highlight">碳循环</span>: 通过光合作用将大气CO₂转化为有机物。<br>
                          <span class="highlight">氮循环</span>: 吸收土壤中的氮化合物合成蛋白质等有机物。<br>
                          <span class="highlight">能量流动</span>: 将太阳能转化为化学能，供其他生物利用。<br><br>
                          生产者固定的能量只有约1%能被后续营养级利用。`,
                
                consumers: `消费者通过摄食其他生物获取能量和物质。<br><br>
                          <span class="highlight">碳循环</span>: 通过呼吸作用将有机物分解为CO₂释放回大气。<br>
                          <span class="highlight">氮循环</span>: 通过排泄和死亡将氮返回环境。<br>
                          <span class="highlight">能量流动</span>: 能量传递效率通常只有10%，其余以热能散失。<br><br>
                          消费者在物质循环和能量流动中起关键传递作用。`,
                
                decomposers: `分解者（细菌、真菌等）是物质循环的"清道夫"。<br><br>
                            <span class="highlight">碳循环</span>: 将动植物残体分解为CO₂和无机物。<br>
                            <span class="highlight">氮循环</span>: 将有机氮转化为无机氮，供植物重新利用。<br><br>
                            没有分解者，生态系统中的物质循环将很快停止。`,
                
                nitrogenFixers: `固氮生物（如根瘤菌、蓝藻）是氮循环的关键。<br><br>
                               <span class="highlight">氮循环</span>: 将大气中惰性的N₂转化为生物可利用的氨(NH₃)。<br><br>
                               自然固氮量: <span class="highlight">约140 Tg/年</span><br>
                               工业固氮（化肥）已接近甚至超过自然固氮量，造成氮污染。`
            };
            
            return info[id] || "信息未找到。";
        }
        
        // 显示信息
        function showInfo(title, content) {
            document.getElementById('infoTitle').textContent = title;
            document.getElementById('infoContent').innerHTML = content;
        }
        
        // 显示默认信息
        function showDefaultInfo() {
            const modeInfo = {
                carbon: `当前模式: <span class="highlight">碳循环</span><br><br>
                        碳元素在大气、生物、海洋和地壳之间循环。<br>
                        关键过程: 光合作用、呼吸作用、分解作用、化石燃料燃烧。<br><br>
                        人类活动（燃烧化石燃料、毁林）正加速碳循环，导致大气CO₂浓度升高和全球变暖。`,
                
                nitrogen: `当前模式: <span class="highlight">氮循环</span><br><br>
                          氮元素在大气、生物和土壤之间转化循环。<br>
                          关键过程: 固氮作用、硝化作用、反硝化作用、植物吸收。<br><br>
                          人类活动（化肥使用、化石燃料燃烧）增加了活性氮含量，导致水体富营养化和温室气体排放。`,
                
                energy: `当前模式: <span class="highlight">能量流动</span><br><br>
                        能量从太阳流向生产者，然后通过食物链传递，最终以热能形式散失。<br>
                        关键特征: 单向流动、逐级递减（通常只有10%传递到下一营养级）。<br><br>
                        与物质循环不同，能量不能循环利用，需要太阳持续输入。`,
                
                compare: `当前模式: <span class="highlight">对比视图</span><br><br>
                         同时展示物质循环与能量流动，理解两者的本质差异:<br>
                         <span class="highlight">物质循环</span>: 元素（C, N）在不同储库间往复循环。<br>
                         <span class="highlight">能量流动</span>: 能量从太阳单向流动，最终以热能散失。<br><br>
                         生态系统依靠这两大过程维持功能和稳定。`
            };
            
            document.getElementById('infoTitle').textContent = '生态系统动态';
            document.getElementById('infoContent').innerHTML = modeInfo[currentMode] || "请选择一种模式开始探索。";
        }
        
        // 切换模式
        function switchMode(mode) {
            currentMode = mode;
            
            // 更新按钮状态
            document.querySelectorAll('.mode-btn').forEach(btn => {
                btn.classList.remove('active');
                if (btn.dataset.mode === mode) {
                    btn.classList.add('active');
                }
            });
            
            // 重新初始化粒子
            initParticles();
            
            // 显示模式信息
            showDefaultInfo();
            
            // 如果动画暂停，重绘一帧
            if (!isPlaying) {
                draw();
            }
        }
        
        // 播放/暂停动画
        function togglePlay() {
            isPlaying = !isPlaying;
            const playBtn = document.getElementById('playBtn');
            
            if (isPlaying) {
                playBtn.textContent = '⏸ 暂停';
                draw(); // 重新开始动画循环
            } else {
                playBtn.textContent = '▶ 播放';
                if (animationId) {
                    cancelAnimationFrame(animationId);
                }
            }
        }
        
        // 重置动画
        function resetAnimation() {
            time = 0;
            humanImpact.fuelBurning = 0.5;
            humanImpact.deforestation = 0.3;
            humanImpact.fertilizerUse = 0.4;
            
            // 重置滑块
            document.getElementById('fuelSlider').value = 50;
            document.getElementById('deforestSlider').value = 30;
            document.getElementById('fertilizerSlider').value = 40;
            
            // 更新滑块显示
            document.getElementById('fuelValue').textContent = '50%';
            document.getElementById('deforestValue').textContent = '30%';
            document.getElementById('fertilizerValue').textContent = '40%';
            
            // 重新初始化粒子
            initParticles();
            
            // 显示默认信息
            showDefaultInfo();
            
            // 如果动画暂停，重绘一帧
            if (!isPlaying) {
                draw();
            }
        }
        
        // 初始化事件监听器
        function initEventListeners() {
            // 模式切换按钮
            document.querySelectorAll('.mode-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    switchMode(btn.dataset.mode);
                });
            });
            
            // 播放/暂停按钮
            document.getElementById('playBtn').addEventListener('click', togglePlay);
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            
            // 速度滑块
            document.getElementById('speedSlider').addEventListener('input', function() {
                animationSpeed = parseFloat(this.value);
                document.getElementById('speedValue').textContent = animationSpeed.toFixed(1) + 'x';
            });
            
            // 人类影响滑块
            document.getElementById('fuelSlider').addEventListener('input', function() {
                humanImpact.fuelBurning = this.value / 100;
                document.getElementById('fuelValue').textContent = this.value + '%';
            });
            
            document.getElementById('deforestSlider').addEventListener('input', function() {
                humanImpact.deforestation = this.value / 100;
                document.getElementById('deforestValue').textContent = this.value + '%';
            });
            
            document.getElementById('fertilizerSlider').addEventListener('input', function() {
                humanImpact.fertilizerUse = this.value / 100;
                document.getElementById('fertilizerValue').textContent = this.value + '%';
            });
            
            // 画布点击事件
            canvas.addEventListener('click', handleCanvasClick);
            
            // 窗口大小调整
            window.addEventListener('resize', function() {
                // 如果动画暂停，重绘一帧以适应新尺寸
                if (!isPlaying) {
                    draw();
                }
            });
        }
        
        // 初始化函数
        function init() {
            // 初始化粒子系统
            initParticles();
            
            // 初始化事件监听器
            initEventListeners();
            
            // 显示默认信息
            showDefaultInfo();
            
            // 开始动画循环
            draw();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

# 交互式教学动画使用指南

## 欢迎使用生态系统教学动画！

亲爱的老师和同学们，欢迎使用这款关于“生态系统物质循环与能量流动”的交互式教学动画。本工具旨在将复杂的生态学概念转化为直观、动态、可操作的视觉体验，帮助您深入理解碳循环、氮循环和能量流动的全球动态过程。

---

## 一、功能说明

### 核心功能模块
1. **动态可视化系统**：实时展示碳、氮元素和能量在生态系统各组分间的流动路径
2. **多模式切换**：提供四种观察视角，满足不同学习需求
3. **参数模拟实验**：通过调整人类活动参数，观察生态系统响应
4. **交互式探索**：点击任何元素获取详细科学解释
5. **实时数据反馈**：显示关键生态指标的变化情况

### 技术特点
- 基于HTML5 Canvas技术，无需额外插件
- 响应式设计，适配不同屏幕尺寸
- 单文件部署，使用便捷
- 粒子系统模拟物质流动过程

---

## 二、主要功能详解

### 1. 模式选择系统
- **碳循环模式**：聚焦碳元素在大气、生物、海洋和地壳间的循环
  - 观察光合作用、呼吸作用、分解作用等关键过程
  - 理解化石燃料燃烧对碳平衡的影响

- **氮循环模式**：展示氮元素在大气、生物和土壤间的转化
  - 探索固氮作用、硝化作用、反硝化作用等微生物过程
  - 了解化肥使用对氮循环的干扰

- **能量流动模式**：追踪太阳能从输入到散失的全过程
  - 观察能量沿食物链单向递减的规律
  - 理解能量传递效率（通常约10%）的概念

- **对比视图模式**：同时展示物质循环与能量流动
  - 直观比较两者的本质差异
  - 理解生态系统如何协调这两大过程

### 2. 动画控制系统
- **播放/暂停**：控制动画运行状态
- **速度调节**：通过滑块调整动画速度（0.1x-3.0x）
- **重置功能**：恢复所有参数到初始状态

### 3. 人类影响模拟实验
通过调整以下参数，观察生态系统的响应：

| 参数 | 影响范围 | 可观察现象 |
|------|----------|------------|
| 化石燃料燃烧 | 碳循环 | 大气CO₂浓度升高、全球温度上升 |
| 森林砍伐 | 碳循环 | 碳汇减少、大气CO₂积累 |
| 化肥使用 | 氮循环 | 水体富营养化、氮氧化物排放 |

### 4. 交互式探索功能
- **点击储库**（大气、森林、海洋、土壤、化石燃料）
  - 获取该储库的详细科学描述
  - 查看当前状态数据

- **点击生物角色**（生产者、消费者、分解者、固氮生物）
  - 了解其在物质循环和能量流动中的作用
  - 学习相关生态学概念

- **点击过程箭头**（光合作用、呼吸作用等）
  - 查看过程的具体机制
  - 了解化学方程式和生态意义

### 5. 实时数据面板
显示四个关键生态指标：
- 大气CO₂浓度（ppm）
- 全球温度变化（°C）
- 氮固定总量（Tg/年）
- 能量传递效率（%）

---

## 三、设计特色

### 1. 视觉设计理念
- **色彩编码系统**：
  - 碳元素：绿色系（生命、植物）
  - 氮元素：蓝色系（大气、水体）
  - 能量：黄色/橙色系（太阳、热能）
  - 人类影响：红色系（警示）

- **动态效果**：
  - 粒子流动模拟物质迁移
  - 储库大小脉动表示含量变化
  - 渐变箭头表示能量耗散
  - 烟雾、火焰等效果增强视觉提示

### 2. 认知设计原则
- **从宏观到微观**：先展示全局视图，再聚焦具体过程
- **从静态到动态**：由示意图逐步过渡到动态模拟
- **从观察到操作**：先观看演示，再通过参数调整进行探索
- **多感官学习**：结合视觉、交互和实时反馈

### 3. 教学适应性
- **分层学习**：适合不同知识水平的学习者
- **自主探索**：支持个性化学习路径
- **课堂演示**：适合教师课堂讲解
- **课后复习**：学生可自主操作加深理解

---

## 四、教学要点

### 核心概念对比

| 特征 | 物质循环 | 能量流动 |
|------|----------|----------|
| 本质 | 元素（C、N）的循环利用 | 能量的单向传递 |
| 路径 | 闭合循环 | 开放流动 |
| 终点 | 无终点，持续循环 | 最终以热能形式散失 |
| 驱动 | 生物地球化学过程 | 太阳辐射 |
| 效率 | 物质基本不损失 | 逐级递减（约90%损失） |

### 关键教学节点

#### 碳循环教学要点
1. **碳的存在形式**：CO₂（大气）、有机物（生物）、碳酸盐（岩石/海洋）
2. **关键生物过程**：
   - 光合作用：CO₂ → 有机物（固碳）
   - 呼吸作用：有机物 → CO₂（释碳）
   - 分解作用：有机物 → 无机物
3. **人类影响**：
   - 化石燃料燃烧：快速释放地质碳
   - 毁林：减少碳汇，释放生物碳
4. **时间尺度差异**：
   - 生物循环：快速（年-十年）
   - 地质循环：缓慢（百万年）

#### 氮循环教学要点
1. **氮的存在形式**：
   - N₂（大气，惰性）
   - NH₄⁺、NO₃⁻（生物可利用）
   - 有机氮（生物体内）
2. **关键转化过程**：
   - 固氮作用：N₂ → NH₃（生物/工业）
   - 硝化作用：NH₄⁺ → NO₃⁻（需氧）
   - 反硝化作用：NO₃⁻ → N₂（厌氧）
3. **微生物的核心作用**：
   - 固氮菌、硝化菌、反硝化菌
4. **人类影响**：
   - 哈伯-博世法：工业固氮
   - 化肥过量使用：氮污染、富营养化

#### 能量流动教学要点
1. **能量金字塔**：
   - 生产者（基础）
   - 初级消费者
   - 次级消费者
   - 分解者
2. **10%定律**：
   - 能量传递效率通常为10%
   - 90%以热能形式散失
3. **营养级限制**：
   - 通常不超过4-5个营养级
   - 能量限制决定食物链长度

---

## 五、使用建议

### 课堂教学应用

#### 1. 引入新课（5分钟）
- 展示“对比视图”模式，让学生直观感受物质循环与能量流动的差异
- 提出问题：“为什么能量不能像物质一样循环利用？”

#### 2. 概念讲解（15分钟）
- 切换到“碳循环”模式，讲解关键过程
- 使用暂停功能，重点讲解光合作用、呼吸作用
- 点击相关元素，展示详细解释

#### 3. 互动探究（10分钟）
- 学生操作“人类影响”滑块
- 观察数据变化，讨论生态影响
- 记录观察结果，形成实验报告

#### 4. 小组讨论（10分钟）
- 对比自然循环与人类干扰的差异
- 讨论可持续发展策略
- 提出减少生态足迹的建议

#### 5. 总结巩固（5分钟）
- 切回“对比视图”模式
- 总结物质循环与能量流动的关系
- 布置思考题或拓展任务

### 自主学习建议

#### 初级学习者（初中水平）
1. 从“碳循环”模式开始，跟随动画了解基本过程
2. 使用较慢的动画速度（0.5x-1.0x）
3. 重点理解：光合作用、呼吸作用、分解作用
4. 完成基础观察记录表

#### 中级学习者（高中水平）
1. 比较三种模式的异同
2. 设计模拟实验：如果森林砍伐达到80%，会发生什么？
3. 分析数据变化，绘制趋势图
4. 撰写简短的研究报告

#### 高级学习者（大学水平）
1. 探索各过程的化学方程式
2. 研究人类活动对全球生物地球化学循环的影响
3. 提出基于系统思维的生态管理方案
4. 设计自己的生态系统模型

### 评估与反馈

#### 形成性评估活动
1. **概念图绘制**：基于动画内容，绘制碳循环概念图
2. **模拟实验报告**：记录参数调整后的观察结果
3. **问题解决**：给定生态问题，提出基于循环原理的解决方案
4. **同伴教学**：向同学解释某个生态过程

#### 学习成果检查
- 能够区分物质循环与能量流动的本质差异
- 能够解释碳循环和氮循环的关键过程
- 能够分析人类活动对生态循环的影响
- 能够提出减少生态足迹的具体措施

---

## 六、技术提示与故障排除

### 系统要求
- 现代浏览器（Chrome 80+、Firefox 75+、Safari 13+、Edge 80+）
- 建议屏幕分辨率：1920×1080或更高
- 启用JavaScript

### 常见问题
1. **动画卡顿**：
   - 降低动画速度
   - 关闭其他占用资源的程序
   - 使用硬件加速的浏览器

2. **交互无响应**：
   - 确保点击的是可交互元素（储库、生物、箭头）
   - 刷新页面重新加载
   - 检查浏览器控制台是否有错误信息

3. **显示异常**：
   - 清除浏览器缓存
   - 尝试不同浏览器
   - 检查屏幕缩放设置

### 扩展使用建议
- **结合实地考察**：在观察本地生态系统后使用本动画
- **跨学科连接**：联系化学（化学反应）、地理（全球分布）、物理（能量转化）
- **项目式学习**：以本动画为基础，开展生态保护项目
- **翻转课堂**：学生课前自主学习，课堂深入讨论

---

## 结语

本交互式教学动画是理解生态系统复杂过程的强大工具。通过动态可视化、交互探索和参数模拟，它将抽象的生态学概念转化为直观的学习体验。我们鼓励您充分探索所有功能，尝试不同的学习路径，并在教学实践中创造性地使用这一资源。

记住，生态系统的美丽在于其相互连接的复杂性，而理解这种复杂性是我们保护地球家园的第一步。祝您学习愉快，探索无限！

**熊猫老师 教育技术团队**  
*让复杂变得简单，让学习变得生动*