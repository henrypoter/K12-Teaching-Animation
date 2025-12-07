# 需求：神经元动作电位与突触传递（钠钾泵、电压门控通道、神经递质释放）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
目标用户主要是高中或大学低年级的生物学、神经科学或医学预科学生。他们需要理解神经元如何产生和传导电信号（动作电位），以及信号如何通过突触传递给下一个细胞。这是一个微观、动态且涉及多个分子机制的过程，传统静态图表难以清晰展示其时间顺序和因果关系。因此，用户的核心需求是：
1.  **可视化动态过程**：将离子流动、通道开闭、电位变化等抽象概念转化为直观的动画。
2.  **理解因果链条**：清晰地展示静息电位 -> 去极化 -> 动作电位 -> 复极化 -> 超极化 -> 突触传递这一连串事件的触发关系。
3.  **模块化解构复杂系统**：将整个过程分解为可独立观察和学习的核心模块（如钠钾泵、电压门控通道、突触小泡释放）。
4.  **交互探索与验证**：通过交互控制（如改变离子浓度、阻断通道）来加深理解，并即时看到结果。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
*   **核心概念**：
    *   **基础**：静息电位（膜内外电位差）、浓度梯度、电化学梯度。
    *   **动作电位**：阈值、去极化（钠离子内流）、峰值、复极化（钾离子外流）、超极化、不应期。
    *   **关键蛋白**：钠钾泵（建立并维持梯度）、电压门控钠/钾通道（动作电位的执行者）。
    *   **突触传递**：动作电位到达末梢、钙离子内流、突触小泡与突触前膜融合、神经递质释放、与突触后膜受体结合、产生突触后电位。
*   **认知规律**：
    *   **从宏观到微观**：先展示一个完整的神经元产生并传导动作电位，再聚焦到一小段轴突膜和单个突触进行详细拆解。
    *   **从结构到功能**：先介绍关键“零件”（泵、通道、小泡），再演示它们如何协同“工作”。
    *   **分步讲解与连续演示结合**：每个关键步骤有分步讲解动画，最后提供完整的、连续的自动演示。
*   **交互设计**：
    *   **阶段控制**：提供“静息电位”、“去极化”、“复极化”、“突触传递”等阶段按钮，允许用户跳转到特定阶段观察。
    *   **播放控制**：播放、暂停、重置、慢速播放按钮，让用户掌控学习节奏。
    *   **“实验”模式**：提供开关，允许用户“关闭”电压门控钠通道或“阻断”钙通道，然后重新播放动画，观察动作电位无法产生或突触传递失败，以验证理解。
    *   **信息提示**：鼠标悬停在关键元素（如泵、通道、离子）上时，显示其名称和当前状态。
    *   **同步视图**：动画主视图旁，同步显示膜电位随时间变化的曲线图，并将当前时刻用竖线标出，建立微观事件与宏观电信号的联系。
*   **视觉呈现**：
    *   **主场景**：一个简化的神经元示意图，包含细胞体、轴突和末端突触。重点区域（一段轴突膜和突触）会高亮并放大显示。
    *   **符号化与拟人化**：
        *   **离子**：用不同颜色的小球（Na⁺：橙色， K⁺：蓝色， Ca²⁺：绿色， Cl⁻：灰色）表示，带“+”或“-”号。
        *   **蛋白质**：
            *   钠钾泵：用两个旋转的“齿轮”或“泵”的卡通形象表示，显示其将3个Na⁺泵出、2个K⁺泵入的循环动作。
            *   电压门控通道：用嵌在膜上的“门”表示。静息时关闭，去极化时钠通道门快速打开（红色闪烁），随后关闭；钾通道门缓慢打开（蓝色闪烁）。
            *   突触小泡：用圆形囊泡表示，内部充满小点（神经递质）。与膜融合时有一个“破裂”释放的动画。
        *   **膜电位**：用膜内侧的“-”号和外侧的“+”号密度来粗略表示，并用数值（如-70mV）和同步的曲线图精确展示。
    *   **动画重点**：离子流动的路径、通道门的开闭动作、小泡的移动与融合，这些是关键，动作要清晰、夸张但不失科学准确性。

#### 配色方案选择
选择清晰、对比度高、符合常见科学图示惯例的配色，以利于区分不同元素：
*   **神经元细胞膜/背景**：浅灰色或米白色，保持中性，突出前景元素。
*   **细胞外液**：非常浅的蓝色。
*   **细胞内液**：非常浅的黄色。
*   **钠离子 (Na⁺)**：**亮橙色**。醒目，代表其快速内流是去极化的主要原因。
*   **钾离子 (K⁺)**：**深蓝色**。与橙色形成强对比，代表其外流导致复极化。
*   **钙离子 (Ca²⁺)**：**绿色**。在突触传递部分突出显示，区别于Na⁺/K⁺。
*   **氯离子 (Cl⁻) / 其他**：浅灰色，作为背景离子。
*   **钠钾泵**：深紫色或金属色，显得稳固、机械。
*   **电压门控钠通道**：**红色**（强调其激活快、是关键触发器）。
*   **电压门控钾通道**：**蓝色**（与钾离子颜色呼应，激活较慢）。
*   **突触小泡**：淡黄色半透明，内部神经递质可用紫色小点表示。
*   **膜电位曲线图**：背景白色，坐标轴黑色，电位曲线用**黑色粗线**绘制，关键点（阈值、峰值）可标红。

#### 交互功能列表
1.  **全局控制面板**：
    *   “播放/暂停”按钮。
    *   “重置”按钮。
    *   “慢速/常速”切换。
    *   “完整演示”模式开关。
2.  **学习阶段选择器**（标签式或按钮式）：
    *   阶段1：静息电位与钠钾泵
    *   阶段2：去极化与动作电位上升支
    *   阶段3：复极化与动作电位下降支
    *   阶段4：突触传递（钙内流与递质释放）
    *   阶段5：完整过程（从刺激到突触后电位）
3.  **“实验”模式开关及选项**：
    *   勾选框：“阻断电压门控钠通道”
    *   勾选框：“阻断电压门控钙通道”
    *   （勾选后，动画中相应通道将显示为灰色且无法激活）
4.  **信息提示系统**：
    *   鼠标悬停在任何离子、泵、通道、小泡上时，弹出文本框显示其名称和简要功能。
    *   在动画关键步骤，屏幕一侧或下方自动出现文字解说。
5.  **同步视图**：
    *   一个始终显示的膜电位-时间曲线图，动画播放时，一条垂直的标记线随动画时间在曲线上移动，高亮显示当前电位对应曲线上的哪一点。
6.  **图例**：
    *   一个固定的角落，用图标和文字说明每种颜色和符号代表什么（Na⁺, K⁺, 钠通道等）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>神经元动作电位与突触传递教学动画</title>
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
            padding: 20px;
            color: #333;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            padding: 25px;
        }

        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 20px;
            border-bottom: 2px solid #eaeaea;
        }

        h1 {
            color: #2c3e50;
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.2rem;
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

        .animation-section {
            flex: 3;
            min-width: 300px;
            background: #fff;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
            border: 1px solid #e0e0e0;
        }

        .controls-section {
            flex: 1;
            min-width: 300px;
            background: #fff;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
            border: 1px solid #e0e0e0;
        }

        .section-title {
            color: #3498db;
            font-size: 1.5rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #f0f0f0;
            display: flex;
            align-items: center;
        }

        .section-title i {
            margin-right: 10px;
            font-size: 1.3rem;
        }

        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background-color: #f8f9fa;
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid #ddd;
        }

        #mainCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .control-group {
            margin-bottom: 25px;
        }

        .control-group h3 {
            color: #2c3e50;
            font-size: 1.2rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }

        .control-group h3 i {
            margin-right: 8px;
            color: #3498db;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }

        .btn {
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            flex: 1;
            min-width: 120px;
        }

        .btn-primary {
            background: linear-gradient(to right, #3498db, #2980b9);
            color: white;
        }

        .btn-primary:hover {
            background: linear-gradient(to right, #2980b9, #2573a7);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(52, 152, 219, 0.3);
        }

        .btn-secondary {
            background: linear-gradient(to right, #2ecc71, #27ae60);
            color: white;
        }

        .btn-secondary:hover {
            background: linear-gradient(to right, #27ae60, #219653);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(46, 204, 113, 0.3);
        }

        .btn-warning {
            background: linear-gradient(to right, #e74c3c, #c0392b);
            color: white;
        }

        .btn-warning:hover {
            background: linear-gradient(to right, #c0392b, #a93226);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(231, 76, 60, 0.3);
        }

        .btn-info {
            background: linear-gradient(to right, #9b59b6, #8e44ad);
            color: white;
        }

        .btn-info:hover {
            background: linear-gradient(to right, #8e44ad, #7d3c98);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(155, 89, 182, 0.3);
        }

        .btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none !important;
            box-shadow: none !important;
        }

        .stage-buttons {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
        }

        .stage-btn {
            padding: 14px 10px;
            background-color: #ecf0f1;
            border: 2px solid #bdc3c7;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            color: #34495e;
            transition: all 0.3s ease;
            text-align: center;
        }

        .stage-btn:hover {
            background-color: #d5dbdb;
            transform: translateY(-2px);
        }

        .stage-btn.active {
            background-color: #3498db;
            color: white;
            border-color: #2980b9;
            box-shadow: 0 4px 10px rgba(52, 152, 219, 0.3);
        }

        .checkbox-group {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 12px;
            background-color: #f8f9fa;
            border-radius: 8px;
            border: 1px solid #e0e0e0;
            transition: all 0.3s ease;
        }

        .checkbox-item:hover {
            background-color: #edf2f7;
            border-color: #3498db;
        }

        .checkbox-item input[type="checkbox"] {
            width: 20px;
            height: 20px;
            cursor: pointer;
            accent-color: #3498db;
        }

        .checkbox-item label {
            font-weight: 600;
            color: #2c3e50;
            cursor: pointer;
            flex: 1;
        }

        .legend {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-top: 20px;
            padding: 20px;
            background-color: #f8f9fa;
            border-radius: 10px;
            border: 1px solid #e0e0e0;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .legend-color {
            width: 25px;
            height: 25px;
            border-radius: 50%;
            border: 2px solid rgba(0,0,0,0.1);
        }

        .legend-text {
            font-size: 0.9rem;
            color: #2c3e50;
            font-weight: 500;
        }

        .info-panel {
            position: absolute;
            bottom: 20px;
            left: 20px;
            right: 20px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border-left: 5px solid #3498db;
            max-height: 120px;
            overflow-y: auto;
        }

        .info-title {
            color: #3498db;
            font-weight: 700;
            margin-bottom: 8px;
            font-size: 1.1rem;
        }

        .info-text {
            color: #555;
            line-height: 1.5;
            font-size: 0.95rem;
        }

        .graph-container {
            width: 100%;
            height: 200px;
            background-color: #fff;
            border-radius: 10px;
            margin-top: 20px;
            padding: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border: 1px solid #e0e0e0;
        }

        #graphCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #eaeaea;
            color: #7f8c8d;
            font-size: 0.9rem;
        }

        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
            
            .legend {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 600px) {
            .stage-buttons {
                grid-template-columns: 1fr;
            }
            
            .legend {
                grid-template-columns: 1fr;
            }
            
            .button-group {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <div class="container">
        <header>
            <h1><i class="fas fa-brain"></i> 神经元动作电位与突触传递</h1>
            <p class="subtitle">本动画演示了神经元如何通过离子通道和神经递质产生和传递电信号。交互式控制允许您探索每个关键步骤。</p>
        </header>
        
        <div class="main-content">
            <section class="animation-section">
                <h2 class="section-title"><i class="fas fa-play-circle"></i> 动画演示</h2>
                <div class="canvas-container">
                    <canvas id="mainCanvas"></canvas>
                    <div class="info-panel">
                        <div class="info-title" id="infoTitle">静息电位</div>
                        <div class="info-text" id="infoText">神经元膜处于静息状态。钠钾泵持续工作，维持膜内外离子浓度梯度。膜电位约为-70mV。</div>
                    </div>
                </div>
                <div class="graph-container">
                    <canvas id="graphCanvas"></canvas>
                </div>
            </section>
            
            <section class="controls-section">
                <h2 class="section-title"><i class="fas fa-sliders-h"></i> 控制面板</h2>
                
                <div class="control-group">
                    <h3><i class="fas fa-gamepad"></i> 动画控制</h3>
                    <div class="button-group">
                        <button id="playBtn" class="btn btn-primary">
                            <i class="fas fa-play"></i> 播放
                        </button>
                        <button id="pauseBtn" class="btn btn-secondary">
                            <i class="fas fa-pause"></i> 暂停
                        </button>
                        <button id="resetBtn" class="btn btn-warning">
                            <i class="fas fa-redo"></i> 重置
                        </button>
                    </div>
                    <div class="button-group">
                        <button id="slowBtn" class="btn btn-info">
                            <i class="fas fa-tachometer-alt"></i> 慢速模式
                        </button>
                        <button id="fullDemoBtn" class="btn btn-primary">
                            <i class="fas fa-film"></i> 完整演示
                        </button>
                    </div>
                </div>
                
                <div class="control-group">
                    <h3><i class="fas fa-map-signs"></i> 学习阶段</h3>
                    <div class="stage-buttons">
                        <button class="stage-btn active" data-stage="resting">1. 静息电位</button>
                        <button class="stage-btn" data-stage="depolarization">2. 去极化</button>
                        <button class="stage-btn" data-stage="repolarization">3. 复极化</button>
                        <button class="stage-btn" data-stage="synapse">4. 突触传递</button>
                        <button class="stage-btn" data-stage="complete">5. 完整过程</button>
                        <button class="stage-btn" data-stage="refractory">6. 不应期</button>
                    </div>
                </div>
                
                <div class="control-group">
                    <h3><i class="fas fa-flask"></i> 实验模式</h3>
                    <div class="checkbox-group">
                        <div class="checkbox-item">
                            <input type="checkbox" id="blockNaChannel">
                            <label for="blockNaChannel">阻断电压门控钠通道</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="blockCaChannel">
                            <label for="blockCaChannel">阻断电压门控钙通道</label>
                        </div>
                    </div>
                </div>
                
                <div class="control-group">
                    <h3><i class="fas fa-palette"></i> 图例</h3>
                    <div class="legend">
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #FF8C00;"></div>
                            <div class="legend-text">钠离子 (Na⁺)</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #1E90FF;"></div>
                            <div class="legend-text">钾离子 (K⁺)</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #32CD32;"></div>
                            <div class="legend-text">钙离子 (Ca²⁺)</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #8A2BE2;"></div>
                            <div class="legend-text">钠钾泵</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #FF4500;"></div>
                            <div class="legend-text">钠通道</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #4169E1;"></div>
                            <div class="legend-text">钾通道</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #FFD700;"></div>
                            <div class="legend-text">突触小泡</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #9370DB;"></div>
                            <div class="legend-text">神经递质</div>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #A9A9A9;"></div>
                            <div class="legend-text">氯离子 (Cl⁻)</div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
        
        <footer>
            <p>教学动画设计：熊猫老师 | 神经元动作电位与突触传递 | 使用HTML5 Canvas实现</p>
            <p>提示：将鼠标悬停在动画中的元素上可以查看详细信息</p>
        </footer>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const mainCanvas = document.getElementById('mainCanvas');
        const graphCanvas = document.getElementById('graphCanvas');
        const mainCtx = mainCanvas.getContext('2d');
        const graphCtx = graphCanvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvases() {
            const container = document.querySelector('.canvas-container');
            mainCanvas.width = container.clientWidth;
            mainCanvas.height = container.clientHeight;
            
            const graphContainer = document.querySelector('.graph-container');
            graphCanvas.width = graphContainer.clientWidth;
            graphCanvas.height = graphContainer.clientHeight;
            
            drawGraph();
        }
        
        window.addEventListener('resize', resizeCanvases);
        resizeCanvases();
        
        // 动画状态变量
        let animationId = null;
        let isPlaying = false;
        let isSlowMode = false;
        let isFullDemo = false;
        let currentStage = 'resting';
        let animationTime = 0;
        let blockNaChannel = false;
        let blockCaChannel = false;
        
        // 膜电位数据
        let membranePotential = -70;
        const potentialData = [];
        const maxDataPoints = 500;
        
        // 颜色定义
        const colors = {
            naIon: '#FF8C00',      // 钠离子 - 橙色
            kIon: '#1E90FF',       // 钾离子 - 蓝色
            caIon: '#32CD32',      // 钙离子 - 绿色
            clIon: '#A9A9A9',      // 氯离子 - 灰色
            naKpump: '#8A2BE2',    // 钠钾泵 - 紫色
            naChannel: '#FF4500',  // 钠通道 - 红色
            kChannel: '#4169E1',   // 钾通道 - 蓝色
            vesicle: '#FFD700',    // 突触小泡 - 金色
            neurotransmitter: '#9370DB', // 神经递质 - 紫色
            membrane: '#D3D3D3',   // 细胞膜 - 浅灰色
            extracellular: '#E6F2FF', // 细胞外液 - 淡蓝色
            intracellular: '#FFF8DC', // 细胞内液 - 淡黄色
            text: '#2C3E50',       // 文本颜色
            graphLine: '#2C3E50',  // 曲线颜色
            graphGrid: '#E0E0E0'   // 网格颜色
        };
        
        // 动画元素定义
        const elements = {
            // 钠钾泵
            naKPump: {
                x: 0, y: 0, width: 60, height: 40,
                rotation: 0, active: true,
                naOut: 0, kIn: 0,
                description: "钠钾泵：每消耗1个ATP，泵出3个Na⁺，泵入2个K⁺，维持静息电位。"
            },
            
            // 电压门控钠通道
            naChannels: [
                {x: 0, y: 0, open: false, openingProgress: 0, active: true, description: "电压门控钠通道：去极化时快速打开，允许Na⁺内流。"},
                {x: 0, y: 0, open: false, openingProgress: 0, active: true, description: "电压门控钠通道：去极化时快速打开，允许Na⁺内流。"},
                {x: 0, y: 0, open: false, openingProgress: 0, active: true, description: "电压门控钠通道：去极化时快速打开，允许Na⁺内流。"}
            ],
            
            // 电压门控钾通道
            kChannels: [
                {x: 0, y: 0, open: false, openingProgress: 0, active: true, description: "电压门控钾通道：去极化时缓慢打开，允许K⁺外流。"},
                {x: 0, y: 0, open: false, openingProgress: 0, active: true, description: "电压门控钾通道：去极化时缓慢打开，允许K⁺外流。"},
                {x: 0, y: 0, open: false, openingProgress: 0, active: true, description: "电压门控钾通道：去极化时缓慢打开，允许K⁺外流。"}
            ],
            
            // 钠离子
            naIons: [],
            
            // 钾离子
            kIons: [],
            
            // 钙离子
            caIons: [],
            
            // 突触小泡
            vesicles: [
                {x: 0, y: 0, radius: 15, attached: false, fusing: false, releaseProgress: 0, description: "突触小泡：内含神经递质，与突触前膜融合后释放。"},
                {x: 0, y: 0, radius: 15, attached: false, fusing: false, releaseProgress: 0, description: "突触小泡：内含神经递质，与突触前膜融合后释放。"},
                {x: 0, y: 0, radius: 15, attached: false, fusing: false, releaseProgress: 0, description: "突触小泡：内含神经递质，与突触前膜融合后释放。"}
            ],
            
            // 神经递质
            neurotransmitters: [],
            
            // 钙通道
            caChannels: [
                {x: 0, y: 0, open: false, openingProgress: 0, active: true, description: "电压门控钙通道：动作电位到达时打开，允许Ca²⁺内流触发递质释放。"}
            ]
        };
        
        // 初始化元素位置
        function initializeElements() {
            const centerX = mainCanvas.width / 2;
            const centerY = mainCanvas.height / 2;
            const membraneWidth = 600;
            const membraneHeight = 150;
            
            // 设置钠钾泵位置
            elements.naKPump.x = centerX - membraneWidth/2 + 100;
            elements.naKPump.y = centerY;
            
            // 设置钠通道位置
            elements.naChannels.forEach((channel, i) => {
                channel.x = centerX - membraneWidth/2 + 250 + i * 100;
                channel.y = centerY;
            });
            
            // 设置钾通道位置
            elements.kChannels.forEach((channel, i) => {
                channel.x = centerX - membraneWidth/2 + 280 + i * 100;
                channel.y = centerY;
            });
            
            // 设置钙通道位置（在突触前膜）
            elements.caChannels[0].x = centerX + membraneWidth/2 - 50;
            elements.caChannels[0].y = centerY - 100;
            
            // 设置突触小泡位置
            elements.vesicles.forEach((vesicle, i) => {
                vesicle.x = centerX + membraneWidth/2 - 30;
                vesicle.y = centerY - 150 - i * 40;
            });
            
            // 初始化离子
            elements.naIons = [];
            elements.kIons = [];
            elements.caIons = [];
            elements.neurotransmitters = [];
            
            // 创建初始离子
            for (let i = 0; i < 30; i++) {
                // 细胞外钠离子
                elements.naIons.push({
                    x: centerX - membraneWidth/2 + 50 + Math.random() * (membraneWidth/2 - 100),
                    y: centerY - 80 - Math.random() * 60,
                    vx: 0, vy: 0,
                    inside: false,
                    description: "钠离子 (Na⁺)：带正电荷，细胞外浓度高于细胞内。"
                });
                
                // 细胞内钠离子
                elements.naIons.push({
                    x: centerX - membraneWidth/2 + 50 + Math.random() * (membraneWidth/2 - 100),
                    y: centerY + 20 + Math.random() * 60,
                    vx: 0, vy: 0,
                    inside: true,
                    description: "钠离子 (Na⁺)：带正电荷，细胞外浓度高于细胞内。"
                });
                
                // 细胞外钾离子
                elements.kIons.push({
                    x: centerX + 50 + Math.random() * (membraneWidth/2 - 100),
                    y: centerY - 80 - Math.random() * 60,
                    vx: 0, vy: 0,
                    inside: false,
                    description: "钾离子 (K⁺)：带正电荷，细胞内浓度高于细胞外。"
                });
                
                // 细胞内钾离子
                elements.kIons.push({
                    x: centerX + 50 + Math.random() * (membraneWidth/2 - 100),
                    y: centerY + 20 + Math.random() * 60,
                    vx: 0, vy: 0,
                    inside: true,
                    description: "钾离子 (K⁺)：带正电荷，细胞内浓度高于细胞外。"
                });
            }
            
            // 创建钙离子
            for (let i = 0; i < 10; i++) {
                elements.caIons.push({
                    x: centerX + membraneWidth/2 - 100 + Math.random() * 80,
                    y: centerY - 180 - Math.random() * 40,
                    vx: 0, vy: 0,
                    inside: false,
                    description: "钙离子 (Ca²⁺)：带两个正电荷，动作电位触发其内流。"
                });
            }
        }
        
        // 绘制主动画
        function drawMainCanvas() {
            // 清除画布
            mainCtx.clearRect(0, 0, mainCanvas.width, mainCanvas.height);
            
            const centerX = mainCanvas.width / 2;
            const centerY = mainCanvas.height / 2;
            const membraneWidth = 600;
            const membraneHeight = 150;
            const membraneY = centerY;
            
            // 绘制细胞外区域
            mainCtx.fillStyle = colors.extracellular;
            mainCtx.fillRect(centerX - membraneWidth/2, 0, membraneWidth, membraneY - membraneHeight/2);
            
            // 绘制细胞内区域
            mainCtx.fillStyle = colors.intracellular;
            mainCtx.fillRect(centerX - membraneWidth/2, membraneY + membraneHeight/2, membraneWidth, mainCanvas.height - (membraneY + membraneHeight/2));
            
            // 绘制细胞膜
            mainCtx.fillStyle = colors.membrane;
            mainCtx.fillRect(centerX - membraneWidth/2, membraneY - membraneHeight/2, membraneWidth, membraneHeight);
            
            // 绘制膜上的文本标签
            mainCtx.fillStyle = colors.text;
            mainCtx.font = "bold 16px Arial";
            mainCtx.textAlign = "center";
            mainCtx.fillText("细胞外", centerX, membraneY - membraneHeight/2 - 20);
            mainCtx.fillText("细胞内", centerX, membraneY + membraneHeight/2 + 30);
            
            // 绘制膜电位数值
            mainCtx.fillStyle = membranePotential >= 0 ? '#FF4500' : '#1E90FF';
            mainCtx.font = "bold 20px Arial";
            mainCtx.fillText(`膜电位: ${membranePotential.toFixed(1)} mV`, centerX, membraneY + membraneHeight/2 + 70);
            
            // 绘制钠钾泵
            drawNaKPump();
            
            // 绘制离子通道
            drawIonChannels();
            
            // 绘制突触区域
            drawSynapse();
            
            // 绘制离子
            drawIons();
            
            // 绘制神经递质
            drawNeurotransmitters();
            
            // 绘制突触小泡
            drawVesicles();
            
            // 绘制突触后膜受体
            drawPostsynapticReceptors();
            
            // 绘制标题
            mainCtx.fillStyle = colors.text;
            mainCtx.font = "bold 24px Arial";
            mainCtx.textAlign = "left";
            mainCtx.fillText("神经元轴突膜与突触", 20, 40);
            
            // 绘制阶段指示器
            mainCtx.font = "16px Arial";
            const stageNames = {
                resting: "静息电位",
                depolarization: "去极化",
                repolarization: "复极化",
                synapse: "突触传递",
                complete: "完整过程",
                refractory: "不应期"
            };
            mainCtx.fillText(`当前阶段: ${stageNames[currentStage]}`, 20, 70);
        }
        
        // 绘制钠钾泵
        function drawNaKPump() {
            const pump = elements.naKPump;
            
            // 绘制泵体
            mainCtx.save();
            mainCtx.translate(pump.x, pump.y);
            mainCtx.rotate(pump.rotation);
            
            mainCtx.fillStyle = colors.naKpump;
            mainCtx.fillRect(-pump.width/2, -pump.height/2, pump.width, pump.height);
            
            // 绘制泵上的符号
            mainCtx.fillStyle = 'white';
            mainCtx.font = "bold 14px Arial";
            mainCtx.textAlign = "center";
            mainCtx.textBaseline = "middle";
            mainCtx.fillText("Na⁺/K⁺", 0, 0);
            mainCtx.fillText("泵", 0, 15);
            
            // 绘制泵出的钠离子
            if (pump.naOut > 0) {
                const naX = -pump.width/2 - 20 - pump.naOut * 5;
                const naY = -10;
                drawIon(naX, naY, colors.naIon, "Na⁺", true);
            }
            
            // 绘制泵入的钾离子
            if (pump.kIn > 0) {
                const kX = -pump.width/2 - 20 - pump.kIn * 5;
                const kY = 10;
                drawIon(kX, kY, colors.kIon, "K⁺", true);
            }
            
            mainCtx.restore();
            
            // 绘制泵的描述（如果鼠标悬停）
            if (isMouseOver(pump.x, pump.y, pump.width, pump.height)) {
                showTooltip(pump.x, pump.y + 50, pump.description);
            }
        }
        
        // 绘制离子通道
        function drawIonChannels() {
            // 绘制钠通道
            elements.naChannels.forEach(channel => {
                drawIonChannel(channel, colors.naChannel, "Na⁺", blockNaChannel ? "#888" : colors.naChannel);
                
                // 绘制通道描述（如果鼠标悬停）
                if (isMouseOver(channel.x, channel.y, 40, 60)) {
                    const status = blockNaChannel ? "（已阻断）" : (channel.open ? "（开放）" : "（关闭）");
                    showTooltip(channel.x, channel.y + 40, channel.description + status);
                }
            });
            
            // 绘制钾通道
            elements.kChannels.forEach(channel => {
                drawIonChannel(channel, colors.kChannel, "K⁺", colors.kChannel);
                
                // 绘制通道描述（如果鼠标悬停）
                if (isMouseOver(channel.x, channel.y, 40, 60)) {
                    const status = channel.open ? "（开放）" : "（关闭）";
                    showTooltip(channel.x, channel.y + 40, channel.description + status);
                }
            });
            
            // 绘制钙通道
            elements.caChannels.forEach(channel => {
                drawIonChannel(channel, colors.caIon, "Ca²⁺", blockCaChannel ? "#888" : colors.caIon);
                
                // 绘制通道描述（如果鼠标悬停）
                if (isMouseOver(channel.x, channel.y, 40, 60)) {
                    const status = blockCaChannel ? "（已阻断）" : (channel.open ? "（开放）" : "（关闭）");
                    showTooltip(channel.x, channel.y + 40, channel.description + status);
                }
            });
        }
        
        // 绘制单个离子通道
        function drawIonChannel(channel, color, label, fillColor) {
            mainCtx.save();
            mainCtx.translate(channel.x, channel.y);
            
            // 绘制通道主体
            mainCtx.fillStyle = fillColor;
            mainCtx.fillRect(-20, -30, 40, 60);
            
            // 绘制通道门
            if (channel.open) {
                // 开放状态
                mainCtx.fillStyle = '#90EE90';
                mainCtx.fillRect(-15, -25 * (1 - channel.openingProgress), 30, 50 * (1 - channel.openingProgress));
            } else {
                // 关闭状态
                mainCtx.fillStyle = '#FFB6C1';
                mainCtx.fillRect(-15, -25, 30, 50);
            }
            
            // 绘制标签
            mainCtx.fillStyle = 'white';
            mainCtx.font = "bold 14px Arial";
            mainCtx.textAlign = "center";
            mainCtx.textBaseline = "middle";
            mainCtx.fillText(label, 0, 0);
            
            mainCtx.restore();
        }
        
        // 绘制离子
        function drawIons() {
            // 绘制钠离子
            elements.naIons.forEach(ion => {
                drawIon(ion.x, ion.y, colors.naIon, "Na⁺");
                
                // 绘制离子描述（如果鼠标悬停）
                if (isMouseOver(ion.x, ion.y, 20, 20)) {
                    const location = ion.inside ? "细胞内" : "细胞外";
                    showTooltip(ion.x, ion.y + 20, ion.description + ` 位置: ${location}`);
                }
            });
            
            // 绘制钾离子
            elements.kIons.forEach(ion => {
                drawIon(ion.x, ion.y, colors.kIon, "K⁺");
                
                // 绘制离子描述（如果鼠标悬停）
                if (isMouseOver(ion.x, ion.y, 20, 20)) {
                    const location = ion.inside ? "细胞内" : "细胞外";
                    showTooltip(ion.x, ion.y + 20, ion.description + ` 位置: ${location}`);
                }
            });
            
            // 绘制钙离子
            elements.caIons.forEach(ion => {
                drawIon(ion.x, ion.y, colors.caIon, "Ca²⁺");
                
                // 绘制离子描述
<!--检测到代码截断，自动续写中...-->
（如果鼠标悬停）
                if (isMouseOver(ion.x, ion.y, 20, 20)) {
                    const location = ion.inside ? "细胞内" : "细胞外";
                    showTooltip(ion.x, ion.y + 20, ion.description + ` 位置: ${location}`);
                }
            });
        }
        
        // 绘制单个离子
        function drawIon(x, y, color, label, isPumpIon = false) {
            const radius = isPumpIon ? 10 : 12;
            
            // 绘制离子外圈
            mainCtx.beginPath();
            mainCtx.arc(x, y, radius, 0, Math.PI * 2);
            mainCtx.fillStyle = color;
            mainCtx.fill();
            
            // 绘制离子边框
            mainCtx.strokeStyle = 'rgba(0, 0, 0, 0.2)';
            mainCtx.lineWidth = 1;
            mainCtx.stroke();
            
            // 绘制离子标签
            mainCtx.fillStyle = 'white';
            mainCtx.font = isPumpIon ? "bold 10px Arial" : "bold 12px Arial";
            mainCtx.textAlign = "center";
            mainCtx.textBaseline = "middle";
            mainCtx.fillText(label, x, y);
        }
        
        // 绘制突触区域
        function drawSynapse() {
            const centerX = mainCanvas.width / 2;
            const centerY = mainCanvas.height / 2;
            const membraneWidth = 600;
            
            // 绘制突触间隙
            const synapseX = centerX + membraneWidth/2;
            const synapseWidth = 100;
            
            mainCtx.fillStyle = '#F0F8FF';
            mainCtx.fillRect(synapseX, centerY - 150, synapseWidth, 120);
            
            // 绘制突触前膜
            mainCtx.fillStyle = colors.membrane;
            mainCtx.fillRect(synapseX - 10, centerY - 150, 10, 120);
            
            // 绘制突触后膜
            mainCtx.fillStyle = colors.membrane;
            mainCtx.fillRect(synapseX + synapseWidth, centerY - 150, 10, 120);
            
            // 绘制标签
            mainCtx.fillStyle = colors.text;
            mainCtx.font = "bold 16px Arial";
            mainCtx.textAlign = "center";
            mainCtx.fillText("突触前膜", synapseX - 5, centerY - 170);
            mainCtx.fillText("突触间隙", synapseX + synapseWidth/2, centerY - 170);
            mainCtx.fillText("突触后膜", synapseX + synapseWidth + 5, centerY - 170);
        }
        
        // 绘制突触小泡
        function drawVesicles() {
            elements.vesicles.forEach(vesicle => {
                // 绘制小泡
                mainCtx.beginPath();
                mainCtx.arc(vesicle.x, vesicle.y, vesicle.radius, 0, Math.PI * 2);
                
                if (vesicle.fusing) {
                    // 融合状态
                    const gradient = mainCtx.createRadialGradient(
                        vesicle.x, vesicle.y, 0,
                        vesicle.x, vesicle.y, vesicle.radius
                    );
                    gradient.addColorStop(0, '#FFEC8B');
                    gradient.addColorStop(1, colors.vesicle);
                    mainCtx.fillStyle = gradient;
                } else {
                    // 正常状态
                    mainCtx.fillStyle = colors.vesicle;
                }
                
                mainCtx.fill();
                
                // 绘制小泡边框
                mainCtx.strokeStyle = 'rgba(0, 0, 0, 0.3)';
                mainCtx.lineWidth = 2;
                mainCtx.stroke();
                
                // 绘制小泡内的神经递质点
                for (let i = 0; i < 8; i++) {
                    const angle = (i / 8) * Math.PI * 2;
                    const distance = vesicle.radius * 0.6;
                    const dotX = vesicle.x + Math.cos(angle) * distance;
                    const dotY = vesicle.y + Math.sin(angle) * distance;
                    
                    mainCtx.beginPath();
                    mainCtx.arc(dotX, dotY, 3, 0, Math.PI * 2);
                    mainCtx.fillStyle = colors.neurotransmitter;
                    mainCtx.fill();
                }
                
                // 绘制小泡描述（如果鼠标悬停）
                if (isMouseOver(vesicle.x, vesicle.y, vesicle.radius*2, vesicle.radius*2)) {
                    const status = vesicle.fusing ? "（正在融合释放）" : (vesicle.attached ? "（附着于膜）" : "（游离状态）");
                    showTooltip(vesicle.x, vesicle.y + vesicle.radius + 10, vesicle.description + status);
                }
            });
        }
        
        // 绘制神经递质
        function drawNeurotransmitters() {
            elements.neurotransmitters.forEach(nt => {
                // 绘制递质分子
                mainCtx.beginPath();
                mainCtx.arc(nt.x, nt.y, 6, 0, Math.PI * 2);
                
                // 根据状态设置颜色
                if (nt.bound) {
                    mainCtx.fillStyle = '#8B008B'; // 结合状态颜色更深
                } else {
                    mainCtx.fillStyle = colors.neurotransmitter;
                }
                
                mainCtx.fill();
                
                // 绘制递质边框
                mainCtx.strokeStyle = 'rgba(0, 0, 0, 0.2)';
                mainCtx.lineWidth = 1;
                mainCtx.stroke();
                
                // 绘制递质描述（如果鼠标悬停）
                if (isMouseOver(nt.x, nt.y, 12, 12)) {
                    const status = nt.bound ? "（已与受体结合）" : "（在突触间隙扩散）";
                    showTooltip(nt.x, nt.y + 15, `神经递质${status}`);
                }
            });
        }
        
        // 绘制突触后膜受体
        function drawPostsynapticReceptors() {
            const centerX = mainCanvas.width / 2;
            const membraneWidth = 600;
            const synapseX = centerX + membraneWidth/2;
            
            // 绘制受体
            for (let i = 0; i < 5; i++) {
                const receptorX = synapseX + 110;
                const receptorY = centerY - 130 + i * 25;
                
                // 绘制受体蛋白
                mainCtx.fillStyle = '#48D1CC';
                mainCtx.fillRect(receptorX, receptorY, 25, 15);
                
                // 绘制结合位点
                mainCtx.fillStyle = '#FF69B4';
                mainCtx.beginPath();
                mainCtx.arc(receptorX + 12.5, receptorY + 7.5, 4, 0, Math.PI * 2);
                mainCtx.fill();
                
                // 检查是否有递质结合
                const hasBoundNT = elements.neurotransmitters.some(nt => 
                    nt.bound && Math.abs(nt.x - (receptorX + 12.5)) < 10 && Math.abs(nt.y - (receptorY + 7.5)) < 10
                );
                
                if (hasBoundNT) {
                    // 绘制激活效果
                    mainCtx.strokeStyle = '#32CD32';
                    mainCtx.lineWidth = 2;
                    mainCtx.beginPath();
                    mainCtx.arc(receptorX + 12.5, receptorY + 7.5, 8, 0, Math.PI * 2);
                    mainCtx.stroke();
                }
                
                // 绘制受体描述（如果鼠标悬停）
                if (isMouseOver(receptorX, receptorY, 25, 15)) {
                    showTooltip(receptorX + 12.5, receptorY + 20, "突触后膜受体：与神经递质结合后激活，产生突触后电位。");
                }
            }
        }
        
        // 绘制电位曲线图
        function drawGraph() {
            const width = graphCanvas.width;
            const height = graphCanvas.height;
            const padding = 30;
            const graphWidth = width - 2 * padding;
            const graphHeight = height - 2 * padding;
            
            // 清除画布
            graphCtx.clearRect(0, 0, width, height);
            
            // 绘制网格
            graphCtx.strokeStyle = colors.graphGrid;
            graphCtx.lineWidth = 0.5;
            
            // 水平网格线
            for (let i = 0; i <= 10; i++) {
                const y = padding + (i / 10) * graphHeight;
                graphCtx.beginPath();
                graphCtx.moveTo(padding, y);
                graphCtx.lineTo(width - padding, y);
                graphCtx.stroke();
                
                // 绘制Y轴标签
                const potential = -80 + i * 20; // -80mV 到 +40mV
                graphCtx.fillStyle = colors.text;
                graphCtx.font = "12px Arial";
                graphCtx.textAlign = "right";
                graphCtx.textBaseline = "middle";
                graphCtx.fillText(`${potential} mV`, padding - 5, y);
            }
            
            // 垂直网格线
            for (let i = 0; i <= 10; i++) {
                const x = padding + (i / 10) * graphWidth;
                graphCtx.beginPath();
                graphCtx.moveTo(x, padding);
                graphCtx.lineTo(x, height - padding);
                graphCtx.stroke();
                
                // 绘制X轴标签
                graphCtx.fillStyle = colors.text;
                graphCtx.font = "12px Arial";
                graphCtx.textAlign = "center";
                graphCtx.textBaseline = "top";
                graphCtx.fillText(`${i * 100} ms`, x, height - padding + 5);
            }
            
            // 绘制坐标轴
            graphCtx.strokeStyle = colors.text;
            graphCtx.lineWidth = 2;
            
            // X轴
            graphCtx.beginPath();
            graphCtx.moveTo(padding, height - padding);
            graphCtx.lineTo(width - padding, height - padding);
            graphCtx.stroke();
            
            // Y轴
            graphCtx.beginPath();
            graphCtx.moveTo(padding, padding);
            graphCtx.lineTo(padding, height - padding);
            graphCtx.stroke();
            
            // 绘制坐标轴标签
            graphCtx.fillStyle = colors.text;
            graphCtx.font = "bold 14px Arial";
            graphCtx.textAlign = "center";
            graphCtx.fillText("时间 (ms)", width / 2, height - 5);
            
            graphCtx.save();
            graphCtx.translate(10, height / 2);
            graphCtx.rotate(-Math.PI / 2);
            graphCtx.fillText("膜电位 (mV)", 0, 0);
            graphCtx.restore();
            
            // 绘制零电位线
            graphCtx.strokeStyle = '#888';
            graphCtx.lineWidth = 1;
            graphCtx.setLineDash([5, 5]);
            const zeroY = padding + (80 / 120) * graphHeight; // -80到+40，0在80/120处
            graphCtx.beginPath();
            graphCtx.moveTo(padding, zeroY);
            graphCtx.lineTo(width - padding, zeroY);
            graphCtx.stroke();
            graphCtx.setLineDash([]);
            
            // 绘制阈值线
            graphCtx.strokeStyle = '#FFA500';
            graphCtx.lineWidth = 1;
            graphCtx.setLineDash([3, 3]);
            const thresholdY = padding + (55 / 120) * graphHeight; // -55mV
            graphCtx.beginPath();
            graphCtx.moveTo(padding, thresholdY);
            graphCtx.lineTo(width - padding, thresholdY);
            graphCtx.stroke();
            graphCtx.setLineDash([]);
            
            // 绘制阈值标签
            graphCtx.fillStyle = '#FFA500';
            graphCtx.font = "12px Arial";
            graphCtx.textAlign = "right";
            graphCtx.fillText("阈值 (-55mV)", width - padding, thresholdY - 5);
            
            // 绘制电位曲线
            if (potentialData.length > 1) {
                graphCtx.strokeStyle = colors.graphLine;
                graphCtx.lineWidth = 3;
                graphCtx.beginPath();
                
                potentialData.forEach((point, index) => {
                    const x = padding + (index / (maxDataPoints - 1)) * graphWidth;
                    const y = padding + ((80 - point) / 120) * graphHeight; // 转换电位值到Y坐标
                    
                    if (index === 0) {
                        graphCtx.moveTo(x, y);
                    } else {
                        graphCtx.lineTo(x, y);
                    }
                });
                
                graphCtx.stroke();
                
                // 绘制当前时间点标记
                if (potentialData.length > 0) {
                    const currentIndex = Math.min(potentialData.length - 1, Math.floor(animationTime / 2));
                    const currentX = padding + (currentIndex / (maxDataPoints - 1)) * graphWidth;
                    const currentY = padding + ((80 - membranePotential) / 120) * graphHeight;
                    
                    // 绘制垂直线
                    graphCtx.strokeStyle = '#FF4500';
                    graphCtx.lineWidth = 2;
                    graphCtx.beginPath();
                    graphCtx.moveTo(currentX, padding);
                    graphCtx.lineTo(currentX, height - padding);
                    graphCtx.stroke();
                    
                    // 绘制当前点
                    graphCtx.fillStyle = '#FF4500';
                    graphCtx.beginPath();
                    graphCtx.arc(currentX, currentY, 6, 0, Math.PI * 2);
                    graphCtx.fill();
                    
                    // 绘制当前电位值
                    graphCtx.fillStyle = '#FF4500';
                    graphCtx.font = "bold 14px Arial";
                    graphCtx.textAlign = "center";
                    graphCtx.fillText(`${membranePotential.toFixed(1)} mV`, currentX, currentY - 15);
                }
            }
        }
        
        // 显示工具提示
        function showTooltip(x, y, text) {
            mainCtx.fillStyle = 'rgba(0, 0, 0, 0.85)';
            mainCtx.strokeStyle = '#3498db';
            mainCtx.lineWidth = 2;
            
            // 计算文本宽度
            mainCtx.font = "14px Arial";
            const textWidth = mainCtx.measureText(text).width;
            const tooltipWidth = textWidth + 20;
            const tooltipHeight = 40;
            
            // 确保工具提示在画布内
            let tooltipX = x - tooltipWidth / 2;
            if (tooltipX < 10) tooltipX = 10;
            if (tooltipX + tooltipWidth > mainCanvas.width - 10) {
                tooltipX = mainCanvas.width - tooltipWidth - 10;
            }
            
            let tooltipY = y;
            if (tooltipY + tooltipHeight > mainCanvas.height - 10) {
                tooltipY = y - tooltipHeight - 20;
            }
            
            // 绘制工具提示框
            mainCtx.beginPath();
            mainCtx.roundRect(tooltipX, tooltipY, tooltipWidth, tooltipHeight, 5);
            mainCtx.fill();
            mainCtx.stroke();
            
            // 绘制工具提示文本
            mainCtx.fillStyle = 'white';
            mainCtx.font = "14px Arial";
            mainCtx.textAlign = "center";
            mainCtx.textBaseline = "middle";
            mainCtx.fillText(text, tooltipX + tooltipWidth / 2, tooltipY + tooltipHeight / 2);
        }
        
        // 检查鼠标是否在元素上
        function isMouseOver(x, y, width, height) {
            if (!mouseX || !mouseY) return false;
            
            return mouseX >= x - width/2 && mouseX <= x + width/2 &&
                   mouseY >= y - height/2 && mouseY <= y + height/2;
        }
        
        // 鼠标位置跟踪
        let mouseX = 0;
        let mouseY = 0;
        
        mainCanvas.addEventListener('mousemove', (e) => {
            const rect = mainCanvas.getBoundingClientRect();
            mouseX = e.clientX - rect.left;
            mouseY = e.clientY - rect.top;
        });
        
        // 更新动画
        function updateAnimation() {
            // 更新动画时间
            if (isPlaying) {
                const timeStep = isSlowMode ? 0.01 : 0.02;
                animationTime += timeStep;
                
                // 根据当前阶段更新动画
                switch(currentStage) {
                    case 'resting':
                        updateRestingStage();
                        break;
                    case 'depolarization':
                        updateDepolarizationStage();
                        break;
                    case 'repolarization':
                        updateRepolarizationStage();
                        break;
                    case 'synapse':
                        updateSynapseStage();
                        break;
                    case 'complete':
                        updateCompleteStage();
                        break;
                    case 'refractory':
                        updateRefractoryStage();
                        break;
                }
                
                // 更新电位数据
                potentialData.push(membranePotential);
                if (potentialData.length > maxDataPoints) {
                    potentialData.shift();
                }
            }
            
            // 绘制所有内容
            drawMainCanvas();
            drawGraph();
            
            // 继续动画循环
            if (isPlaying || isFullDemo) {
                animationId = requestAnimationFrame(updateAnimation);
            }
        }
        
        // 更新静息电位阶段
        function updateRestingStage() {
            // 更新钠钾泵
            elements.naKPump.rotation += 0.02;
            elements.naKPump.naOut = (elements.naKPump.naOut + 0.05) % 10;
            elements.naKPump.kIn = (elements.naKPump.kIn + 0.03) % 10;
            
            // 静息电位维持在-70mV左右
            membranePotential = -70 + Math.sin(animationTime * 0.5) * 2;
            
            // 更新信息面板
            document.getElementById('infoTitle').textContent = '静息电位';
            document.getElementById('infoText').textContent = '神经元膜处于静息状态。钠钾泵持续工作，维持膜内外离子浓度梯度。膜电位约为-70mV。';
            
            // 自动切换到下一阶段（仅在全演示模式下）
            if (isFullDemo && animationTime > 5) {
                switchToStage('depolarization');
                animationTime = 0;
            }
        }
        
        // 更新去极化阶段
        function updateDepolarizationStage() {
            // 钠钾泵继续工作
            elements.naKPump.rotation += 0.02;
            
            // 打开钠通道（如果没有被阻断）
            if (!blockNaChannel) {
                elements.naChannels.forEach(channel => {
                    if (animationTime > 0.5 && channel.openingProgress < 1) {
                        channel.openingProgress += 0.05;
                        channel.open = channel.openingProgress > 0.5;
                    }
                });
            }
            
            // 钠离子内流（如果通道打开）
            if (!blockNaChannel && animationTime > 0.8) {
                elements.naIons.forEach(ion => {
                    if (!ion.inside && ion.x > mainCanvas.width/2 - 200 && ion.x < mainCanvas.width/2 + 200) {
                        // 细胞外钠离子向细胞内移动
                        ion.vy += 0.1;
                        if (ion.y < mainCanvas.height/2 && Math.random() < 0.1) {
                            ion.inside = true;
                        }
                    }
                });
                
                // 膜电位上升（去极化）
                membranePotential += 1.5;
                if (membranePotential > 40) membranePotential = 40;
            } else if (blockNaChannel) {
                // 如果钠通道被阻断，去极化不会发生
                membranePotential = -55;
            }
            
            // 更新信息面板
            document.getElementById('infoTitle').textContent = '去极化';
            document.getElementById('infoText').textContent = blockNaChannel ? 
                '钠通道被阻断！刺激无法引起足够的去极化达到阈值，动作电位不能产生。' :
                '刺激使膜电位去极化达到阈值(-55mV)，电压门控钠通道快速打开，Na⁺大量内流，膜电位迅速上升。';
            
            // 自动切换到下一阶段（仅在全演示模式下）
            if (isFullDemo && animationTime > 3) {
                switchToStage('repolarization');
                animationTime = 0;
            }
        }
        
        // 更新复极化阶段
        function updateRepolarizationStage() {
            // 钠钾泵继续工作
            elements.naKPump.rotation += 0.02;
            
            // 关闭钠通道（失活）
            elements.naChannels.forEach(channel => {
                if (animationTime > 0.5) {
                    channel.openingProgress = Math.max(0, channel.openingProgress - 0.03);
                    channel.open = channel.openingProgress > 0.5;
                }
            });
            
            // 打开钾通道
            elements.kChannels.forEach(channel => {
                if (animationTime > 0.8 && channel.openingProgress < 1) {
                    channel.openingProgress += 0.03;
                    channel.open = channel.openingProgress > 0.3;
                }
            });
            
            // 钾离子外流
            if (animationTime > 1.2) {
                elements.kIons.forEach(ion => {
                    if (ion.inside && ion.x > mainCanvas.width/2 - 200 && ion.x < mainCanvas.width/2 + 200) {
                        // 细胞内钾离子向细胞外移动
                        ion.vy -= 0.08;
                        if (ion.y < mainCanvas.height/2 && Math.random() < 0.05) {
                            ion.inside = false;
                        }
                    }
                });
                
                // 膜电位下降（复极化）
                membranePotential -= 1.2;
                if (membranePotential < -80) membranePotential = -80; // 超极化
            }
            
            // 更新信息面板
            document.getElementById('infoTitle').textContent = '复极化与超极化';
            document.getElementById('infoText').textContent = '钠通道失活关闭，钾通道缓慢打开，K⁺外流使膜电位恢复并暂时超极化（低于静息电位）。';
            
            // 自动切换到下一阶段（仅在全演示模式下）
            if (isFullDemo && animationTime > 4) {
                switchToStage('synapse');
                animationTime = 0;
            }
        }
        
        // 更新突触传递阶段
        function updateSynapseStage() {
            // 动作电位到达突触末梢
            if (animationTime > 0.5) {
                // 打开钙通道（如果没有被阻断）
                if (!blockCaChannel) {
                    elements.caChannels[0].openingProgress = Math.min(1, elements.caChannels[0].openingProgress + 0.04);
                    elements.caChannels[0].open = elements.caChannels[0].openingProgress > 0.5;
                }
                
                // 钙离子内流
                if (!blockCaChannel && animationTime > 1.0) {
                    elements.caIons.forEach(ion => {
                        if (!ion.inside) {
                            // 钙离子向突触前膜移动
                            const dx = elements.caChannels[0].x - ion.x;
                            const dy = elements.caChannels[0].y - ion.y;
                            const dist = Math.sqrt(dx*dx + dy*dy);
                            
                            if (dist < 100) {
                                ion.vx += dx * 0.001;
                                ion.vy += dy * 0.001;
                                
                                // 限制速度
                                const speed = Math.sqrt(ion.vx*ion.vx + ion.vy*ion.vy);
                                if (speed > 2) {
                                    ion.vx = (ion.vx / speed) * 2;
                                    ion.vy = (ion.vy / speed) * 2;
                                }
                                
                                // 如果钙离子接近通道，标记为进入细胞内
                                if (dist < 15) {
                                    ion.inside = true;
                                }
                            }
                        }
                    });
                }
                
                // 突触小泡与突触前膜融合
                if (!blockCaChannel && animationTime > 2.0) {
                    elements.vesicles.forEach((vesicle, index) => {
                        if (!vesicle.fusing && animationTime > 2.0 + index * 0.5) {
                            // 小泡向突触前膜移动
                            const targetX = elements.caChannels[0].x;
                            const targetY = elements.caChannels[0].y + 30;
                            
                            const dx = targetX - vesicle.x;
                            const dy = targetY - vesicle.y;
                            
                            vesicle.x += dx * 0.05;
                            vesicle.y += dy * 0.05;
                            
                            // 如果接近膜，开始融合
                            if (Math.abs(dx) < 10 && Math.abs(dy) < 10) {
                                vesicle.attached = true;
                                vesicle.fusing = true;
                            }
                        }
                        
                        // 释放神经递质
                        if (vesicle.fusing && vesicle.releaseProgress < 1) {
                            vesicle.releaseProgress += 0.02;
                            vesicle.radius = Math.max(5, 15 * (1 - vesicle.releaseProgress));
                            
                            // 创建新的神经递质分子
                            if (Math.random() < 0.1 && elements.neurotransmitters.length < 50) {
                                elements.neurotransmitters.push({
                                    x: vesicle.x,
                                    y: vesicle.y,
                                    vx: (Math.random() - 0.5) * 0.5,
                                    vy: Math.random() * 0.3,
                                    bound: false,
                                    bindProgress: 0
                                });
                            }
                        }
                    });
                }
                
                // 更新神经递质
                elements.neurotransmitters.forEach(nt => {
                    // 移动递质
                    nt.x += nt.vx;
                    nt.y += nt.vy;
                    
                    // 递质在突触间隙中扩散
                    nt.vx *= 0.99;
                    nt.vy *= 0.99;
                    
                    // 添加随机运动
                    nt.vx += (Math.random() - 0.5) * 0.05;
                    nt.vy += (Math.random() - 0.5) * 0.05;
                    
                    // 检查是否与突触后膜受体结合
                    const centerX = mainCanvas.width / 2;
                    const membraneWidth = 600;
                    const synapseX = centerX + membraneWidth/2;
                    
                    if (nt.x > synapseX + 100 && nt.x < synapseX + 140 && !nt.bound) {
                        // 接近突触后膜
                        if (Math.random() < 0.02) {
                            nt.bound = true;
                            nt.vx = 0;
                            nt.vy = 0;
                        }
                    }
                    
                    // 如果递质超出范围，移除它
                    if (nt.y < 0 || nt.y > mainCanvas.height || nt.x > mainCanvas.width) {
                        const index = elements.neurotransmitters.indexOf(nt);
                        if (index > -1) {
                            elements.neurotransmitters.splice(index, 1);
                        }
                    }
                });
            }
            
            // 更新信息面板
            document.getElementById('infoTitle').textContent = '突触传递';
            document.getElementById('infoText').textContent = blockCaChannel ? 
                '钙通道被阻断！动作电位无法触发钙内流，突触小泡不能融合，神经递质无法释放。' :
                '动作电位到达突触末梢，电压门控钙通道打开，Ca²⁺内流触发突触小泡与突触前膜融合，释放神经递质。';
            
            // 自动切换到下一阶段（仅在全演示模式下）
            if (isFullDemo && animationTime > 6) {
                switchToStage('refractory');
                animationTime = 0;
            }
        }
        
        // 更新完整过程阶段
        function updateCompleteStage() {
            // 组合所有阶段的动画
            const stageTime = animationTime % 15; // 完整循环15秒
            
            if (stageTime < 3) {
                // 静息电位
                updateRestingStage();
                membranePotential = -70 + Math.sin(stageTime * 0.5) * 2;
            } else if (stageTime < 6) {
                // 去极化
                updateDepolarizationStage();
                if (!blockNaChannel) {
                    membranePotential = Math.min(40, -70 + (stageTime - 3) * 40);
                }
            } else if (stageTime < 10) {
                // 复极化
                updateRepolarizationStage();
                membranePotential = Math.max(-85, 40 - (stageTime - 6) * 30);
            } else {
                // 突触传递
                updateSynapseStage();
                membranePotential = -70 + Math.sin(stageTime * 0.5) * 2;
            }
            
            // 更新信息面板
            document.getElementById('infoTitle').textContent = '完整过程';
            document.getElementById('infoText').textContent = '展示从静息电位到动作电位产生，再到突触传递的完整过程。注意观察离子流动与电位变化的同步关系。';
        }
        
        // 更新不应期阶段
        function updateRefractoryStage() {
            // 膜电位处于超极化状态
            membranePotential = -80 + Math.sin(animationTime * 0.3) * 5;
            
            // 钠通道处于失活状态
            elements.naChannels.forEach(channel => {
                channel.open = false;
                channel.openingProgress = 0;
            });
            
            // 钾通道部分开放
            elements.kChannels.forEach(channel => {
                channel.open = true;
                channel.openingProgress = 0.7;
            });
            
            // 尝试刺激（但不会引起动作电位）
            if (animationTime > 2 && animationTime < 4) {
                membranePotential = -60; // 小的去极化，但达不到阈值
            }
            
            // 更新信息面板
            document.getElementById('infoTitle').textContent = '不应期';
            document.getElementById('infoText').textContent = '动作电位之后的一段时间内，钠通道处于失活状态，无论多强的刺激都不能引发新的动作电位。这是神经信号单向传导的基础。';
            
            // 自动切换到下一阶段（仅在全演示模式下）
            if (isFullDemo && animationTime > 5) {
                switchToStage('resting');
                animationTime = 0;
            }
        }
        
        // 切换到指定阶段
        function switchToStage(stage) {
            currentStage = stage;
            
            // 更新阶段按钮状态
            document.querySelectorAll('.stage-btn').forEach(btn => {
                if (btn.dataset.stage === stage) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            // 重置动画时间
            animationTime = 0;
            
            // 重置电位数据
            potentialData.length = 0;
            
            // 重置一些元素状态
            if (stage === 'resting' || stage === 'complete') {
                membranePotential = -70;
                
                // 重置通道
                elements.naChannels.forEach(channel => {
                    channel.open = false;
                    channel.openingProgress = 0;
                });
                
                elements.kChannels.forEach(channel => {
                    channel.open = false;
                    channel.openingProgress = 0;
                });
                
                elements.caChannels.forEach(channel => {
                    channel.open = false;
                    channel.openingProgress = 0;
                });
                
                // 重置小泡
                elements.vesicles.forEach(vesicle => {
                    vesicle.attached = false;
                    vesicle.fusing = false;
                    vesicle.releaseProgress = 0;
                    vesicle.radius = 15;
                });
                
                // 清空神经递质
                elements.neurotransmitters.length = 0;
                
                // 重新初始化离子位置
                initializeElements();
            }
            
            // 开始动画（如果当前正在播放）
            if (isPlaying) {
                if (animationId) {
                    cancelAnimationFrame(animationId);
                }
                animationId = requestAnimationFrame(updateAnimation);
            }
        }
        
        // 初始化
        function init() {
            // 初始化元素位置
            initializeElements();
            
            // 绘制初始状态
            drawMainCanvas();
            drawGraph();
            
            // 设置事件监听器
            
            // 播放按钮
            document.getElementById('playBtn').addEventListener('click', () => {
                isPlaying = true;
                isFullDemo = false;
                if (!animationId) {
                    animationId = requestAnimationFrame(updateAnimation);
                }
            });
            
            // 暂停按钮
            document.getElementById('pauseBtn').addEventListener('click', () => {
                isPlaying = false;
                isFullDemo = false;
            });
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', () => {
                isPlaying = false;
                isFullDemo = false;
                animationTime = 0;
                membranePotential = -70;
                potentialData.length = 0;
                switchToStage('resting');
                drawMainCanvas();
                drawGraph();
            });
            
            // 慢速模式按钮
            document.getElementById('slowBtn').addEventListener('click', function() {
                isSlowMode = !isSlowMode;
                this.innerHTML = isSlowMode ? 
                    '<i class="fas fa-tachometer-alt"></i> 常速模式' : 
                    '<i class="fas fa-tachometer-alt"></i> 慢速模式';
                this.classList.toggle('btn-secondary');
                this.classList.toggle('btn-info');
            });
            
            // 完整演示按钮
            document.getElementById('fullDemoBtn').addEventListener('click', function() {
                isFullDemo = !isFullDemo;
                isPlaying = isFullDemo;
                this.innerHTML = isFullDemo ? 
                    '<i class="fas fa-stop-circle"></i> 停止演示' : 
                    '<i class="fas fa-film"></i> 完整演示';
                this.classList.toggle('btn-primary');
                this.classList.toggle('btn-warning');
                
                if (isFullDemo) {
                    switchToStage('complete');
                    if (!animationId) {
                        animationId = requestAnimationFrame(updateAnimation);
                    }
                }
            });
            
            // 阶段按钮
            document.querySelectorAll('.stage-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const stage = this.dataset.stage;
                    isFullDemo = false;
                    document.getElementById('fullDemoBtn').innerHTML = '<i class="fas fa-film"></i> 完整演示';
                    document.getElementById('fullDemoBtn').classList.remove('btn-warning');
                    document.getElementById('fullDemoBtn').classList.add('btn-primary');
                    switchToStage(stage);
                });
            });
            
            // 实验模式复选框
            document.getElementById('blockNaChannel').addEventListener('change', function() {
                blockNaChannel = this.checked;
            });
            
            document.getElementById('blockCaChannel').addEventListener('change', function() {
                blockCaChannel = this.checked;
            });
            
            // 初始绘制
            updateAnimation();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## 《神经元动作电位与突触传递》交互式教学动画使用指南

欢迎使用本交互式教学动画！本指南将帮助您充分利用这一工具，深入理解神经元电信号产生与传递的复杂过程。

---

### 一、 功能总览

本动画旨在将抽象的神经生理学概念（如离子流动、膜电位变化、突触传递）转化为直观、动态的视觉模型。它通过**可视化、交互式**的方式，让您能够：
*   **观察** 动作电位从产生到传导，再到跨突触传递的完整动态过程。
*   **控制** 学习节奏，分步探索每个关键阶段。
*   **实验** 通过“阻断”关键离子通道，验证其对信号传递的影响。
*   **关联** 微观的分子事件（如离子通道开闭）与宏观的电信号变化（膜电位曲线）。

### 二、 主要功能区说明

#### 1. 动画演示区（主视图）
*   **核心场景**：展示了一段神经元轴突膜及一个化学突触的放大视图。
*   **视觉元素**：
    *   **彩色离子**：钠离子（橙色）、钾离子（蓝色）、钙离子（绿色），其流动方向代表浓度梯度和电化学驱动力。
    *   **动态蛋白质**：旋转的钠钾泵（紫色）、可开闭的电压门控通道（钠通道-红色，钾通道-蓝色，钙通道-绿色）。
    *   **突触结构**：包含突触小泡（金色）、神经递质（紫色）和突触后膜受体（青色）。
*   **信息提示**：将鼠标悬停在**任何元素**（离子、泵、通道、小泡）上，会弹出其名称、功能和当前状态的详细说明。

#### 2. 膜电位曲线图（同步视图）
*   位于主动画下方，实时绘制膜电位随时间变化的曲线。
*   **关键标识**：
    *   **黑色粗线**：实时电位曲线。
    *   **红色竖线与圆点**：指示当前动画时刻对应的电位值。
    *   **橙色虚线**：动作电位阈值（约-55mV）。
    *   **灰色虚线**：0mV参考线。
*   **教学意义**：将微观的离子流动事件与宏观的、可测量的电信号（动作电位波形）直接关联，是理解本课题的核心。

#### 3. 控制面板（右侧功能区）

##### **动画控制**
*   **播放/暂停**：控制动画的进行与停止，让您能仔细审视每一帧。
*   **重置**：将动画恢复到初始的静息状态。
*   **慢速模式**：切换为慢速播放，便于观察快速过程（如钠通道的快速激活）。
*   **完整演示**：自动循环播放从静息电位到突触传递的完整过程。

##### **学习阶段**
*   提供六个模块化学习阶段按钮，允许您**直接跳转**到特定环节进行重点学习：
    1.  **静息电位**：观察钠钾泵如何建立并维持离子梯度。
    2.  **去极化**：观看刺激如何引发钠通道开放和钠离子内流。
    3.  **复极化**：观察钠通道失活、钾通道开放和钾离子外流。
    4.  **突触传递**：聚焦突触，看动作电位如何触发钙内流和神经递质释放。
    5.  **完整过程**：连续观看上述所有阶段。
    6.  **不应期**：理解动作电位后钠通道失活带来的暂时性兴奋缺失。

##### **实验模式**
*   这是本动画的**核心交互功能**，允许您进行“虚拟实验”：
    *   **阻断电压门控钠通道**：勾选后，去极化阶段将无法发生，动作电位**不能产生**。这直观地证明了钠通道是动作电位上升支的“触发器”。
    *   **阻断电压门控钙通道**：勾选后，动作电位虽能到达突触末梢，但无法引起钙内流，导致**突触传递失败**。这验证了钙离子在递质释放中的关键作用。

##### **图例**
*   清晰列出了所有视觉元素的颜色和符号对应关系，方便随时查阅。

### 三、 设计特色与教学要点

1.  **分步与连续相结合**：既可通过“学习阶段”按钮进行分解学习，又可通过“完整演示”观看流畅的连续过程，符合“分析-综合”的认知规律。
2.  **因果关系的可视化**：
    *   去极化 → 钠通道开放 → 钠离子内流 → 电位上升。
    *   动作电位到达 → 钙通道开放 → 钙离子内流 → 小泡融合 → 递质释放。
    *   **实验模式**能直接打断这些链条，让您观察“因”被移除后“果”的消失，深刻理解其必要性。
3.  **分子机制与电信号的同步**：主视图的离子流动、通道开闭与下方电位曲线的变化严格同步，帮助您建立“微观分子事件决定宏观电信号”的思维模型。
4.  **强调关键概念**：
    *   **阈值**：只有去极化达到阈值，才能引爆动作电位（观察去极化阶段与阈值线的关联）。
    *   **不应期**：解释了神经冲动为什么是**全或无**的，以及为什么传导是**单向**的。
    *   **化学突触的转换**：电信号（动作电位）→ 化学信号（神经递质）→ 电信号（突触后电位）的转换过程一目了然。

### 四、 使用建议

1.  **初次学习者**：
    *   建议顺序：先使用“完整演示”按钮观看1-2遍，获得整体印象。
    *   然后，按照“学习阶段”的顺序（1→2→3→4→6），逐个阶段点击，结合**信息提示**仔细阅读每个元素的说明，并观察其动态。
    *   最后，再次观看“完整过程”，尝试在心中默念每个步骤。

2.  **巩固与探究者**：
    *   打开“实验模式”，分别勾选两个阻断选项，然后播放“完整过程”或相应阶段。**预测并观察**会发生什么，然后用学过的原理解释现象。
    *   尝试在动画播放时，**同步描述**：“现在膜电位正在去极化，因为钠通道打开了，钠离子正在快速内流……”
    *   关注“不应期”阶段，思考其在防止信号回传和限制神经元最大发放频率方面的生理意义。

3.  **教学者**：
    *   可将此动画作为课堂演示工具，分步讲解。
    *   提出引导性问题，如：“如果我们用河豚毒素（TTX）阻断钠通道，动画中的哪一部分会发生变化？请大家用实验模式验证一下。”
    *   鼓励学生利用“实验模式”自主设计探究性问题并验证。

---

我们希望这个精心设计的交互式动画能成为您探索神经科学奥秘的得力助手。请尽情点击、悬停、实验和观察，让复杂的过程在您眼前变得清晰而生动！

**祝您学习愉快，探索无限！**

—— 熊猫老师 教育技术团队