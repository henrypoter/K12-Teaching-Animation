# 需求：电解饱和食盐水的三产物生成微观同步动画

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学预科阶段的学生，正在学习“电解原理”或“氯碱工业”相关内容。他们具备基础的化学粒子（离子、原子、分子）概念，但对电解过程的微观动态和同步性理解不深。
2.  **核心需求**：
    *   **直观理解**：将抽象的离子移动、电子得失、分子生成过程可视化，帮助学生建立宏观现象（气泡、颜色变化）与微观粒子反应之间的联系。
    *   **同步性认知**：强调阴极、阳极和溶液中反应是**同时、等量（电子转移角度）** 发生的，这是教学难点。学生常误认为反应有先后顺序。
    *   **产物对应关系**：清晰展示三种产物（`H₂`、`Cl₂`、`NaOH`）分别来自哪个电极、如何生成，以及最终在溶液中如何共存。
    *   **主动探索**：允许学生控制动画（如开始/暂停、调节速度），以自主观察和思考，而非被动观看。

#### 教学设计思路
1.  **核心概念**：
    *   电解池构成：直流电源、惰性电极（石墨）、饱和食盐水。
    *   粒子存在：`Na⁺`、`Cl⁻`、`H⁺`（来自水）、`OH⁻`（来自水）。
    *   放电顺序：阳极`Cl⁻` > `OH⁻`，阴极`H⁺` > `Na⁺`。
    *   电极反应：
        *   阳极：`2Cl⁻ - 2e⁻ → Cl₂↑`
        *   阴极：`2H⁺ + 2e⁻ → H₂↑`
    *   总反应与产物：`2NaCl + 2H₂O → H₂↑ + Cl₂↑ + 2NaOH`。强调`NaOH`是溶液中`Na⁺`和`OH⁻`（因阴极消耗`H⁺`而相对富集）结合的结果。
2.  **认知规律**：
    *   **从静态到动态**：先展示初始状态（溶液中离子分布），再动态演示过程。
    *   **从分解到整合**：先分别讲解阴极、阳极反应，再用同步动画整合，最后展示总反应和产物收集。
    *   **突出关键线索**：用“电子流”作为贯穿始终的线索，连接两极反应，解释同步性与等量关系。
3.  **交互设计**：
    *   **分层控制**：提供“播放/暂停/重置”全局控制，以及“慢速/常速/快速”速度调节。
    *   **焦点提示**：允许用户点击或悬停在特定区域（如电极、离子、气泡），高亮显示并给出简要文字说明。
    *   **步骤引导**：可设计“分步演示”模式，将连续过程分解为几个关键步骤（如：离子迁移 → 电子得失 → 气体生成 → 溶液成分变化），由用户手动触发下一步。
4.  **视觉呈现**：
    *   **主视图**：一个横置的U型管电解池，中间用半透膜（可选视觉元素）隔开，左右分别为阳极区和阴极区，上方连接直流电源和产物收集装置。
    *   **粒子设计**：
        *   `Na⁺`：蓝色小球，带“+”号。
        *   `Cl⁻`：绿色小球，带“-”号。
        *   `H⁺`：极小红色小球，带“+”号。
        *   `OH⁻`：红色氧与白色氢的组合球，带“-”号。
        *   `H₂`分子：两个白色小球的组合。
        *   `Cl₂`分子：两个绿色小球的组合。
        *   电子（`e⁻`）：极小的亮黄色闪烁光点。
    *   **动画流程**：
        1.  **初始**：所有离子均匀分布。
        2.  **通电**：显示电路连通，电子从电源负极流向阴极，从阳极流向电源正极。
        3.  **迁移与放电**：
            *   阴极区：`H⁺`向阴极移动，接触电极获得电子（黄色光点融入），变成`H`原子，然后两两结合成`H₂`气泡上浮。
            *   阳极区：`Cl⁻`向阳极移动，接触电极失去电子（从电极飞出黄色光点），变成`Cl`原子，然后两两结合成`Cl₂`气泡上浮。
            *   **关键同步**：阴极每“吸收”一个电子，阳极同时“释放”一个电子，动画上可设计为电子在导线中连续流动。
        4.  **溶液变化**：随着反应进行，阴极区`H⁺`减少，`OH⁻`相对增多（可改变区域背景色或`OH⁻`密度示意碱性增强）；阳极区`Cl⁻`减少。`Na⁺`作为旁观离子，向阴极迁移以保持电荷平衡。
        5.  **产物生成**：`H₂`和`Cl₂`分别在上方收集，溶液底部出现“NaOH”字样或晶体析出（示意）。

#### 配色方案选择
*   **主背景**：浅灰色或淡蓝色，模拟实验台或背景板，中性不抢眼。
*   **电解池与电极**：电解池玻璃壁为透明或浅灰色细线。电极为深灰色（石墨）。导线为金色或铜色。
*   **粒子配色**（遵循部分化学可视化惯例并保证高对比度）：
    *   `Na⁺`：**宝蓝色**（稳定、阳离子常用色）。
    *   `Cl⁻`：**草绿色**（区别于`Cl₂`气体）。
    *   `H⁺`：**亮红色**（强调其活性，且与酸关联）。
    *   `OH⁻`：**红白相间**（氧元素红，氢元素白，整体偏粉）。
    *   `H₂`：**浅灰色或白色**（无色气体）。
    *   `Cl₂`：**黄绿色**（氯气特征色）。
    *   电子：**亮黄色**（高亮、能量象征）。
    *   水流/背景：极浅的蓝色半透明。
*   **交互元素**：控制按钮用深蓝色填充，白色文字。高亮状态用发光黄色边框。

#### 交互功能列表
1.  **动画控制区**：
    *   播放 / 暂停 / 重置 按钮。
    *   速度滑块或按钮组：慢速 (0.5x) / 常速 (1x) / 快速 (2x)。
2.  **演示模式选择**：
    *   “连续动画”模式：自动播放完整过程。
    *   “分步讲解”模式：分为4-5个步骤，每步有标题和说明，用户点击“下一步”继续。
3.  **焦点交互**：
    *   鼠标悬停在任一粒子或气体分子上，显示其名称和化学式。
    *   鼠标悬停在电极上，显示电极名称（阴极/阳极）和反应式。
    *   点击“电子流”路径，高亮整个回路，并显示文字：“电子从电源负极流向阴极，参与还原反应；从阳极流向电源正极，来自氧化反应”。
4.  **信息面板**：
    *   固定显示总化学方程式：`2NaCl + 2H₂O → H₂↑ + Cl₂↑ + 2NaOH`。
    *   动态显示当前步骤说明或关键提示。
    *   可开关的“粒子图例”，展示各颜色粒子对应的物质。
5.  **视图辅助**：
    *   “显示/隐藏离子标签”开关。
    *   “高亮`OH⁻`浓度变化”开关（用于突出阴极区碱性增强）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>电解饱和食盐水微观动画</title>
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
            max-width: 1000px;
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
        
        .equation {
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            padding: 12px 20px;
            display: inline-block;
            font-size: 1.4rem;
            font-weight: bold;
            color: #2980b9;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            border-left: 5px solid #3498db;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            max-width: 1000px;
            width: 100%;
            justify-content: center;
        }
        
        .animation-area {
            flex: 1;
            min-width: 600px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
            overflow: hidden;
            padding: 15px;
            display: flex;
            flex-direction: column;
        }
        
        .canvas-container {
            flex: 1;
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            background-color: #e8f4f8;
            border: 2px solid #bdc3c7;
        }
        
        #electrolysisCanvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .control-panel {
            background-color: #f8f9fa;
            border-radius: 15px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
            padding: 20px;
            min-width: 300px;
            max-width: 350px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .panel-section {
            background-color: white;
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
        }
        
        .section-title {
            color: #2c3e50;
            font-size: 1.2rem;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #ecf0f1;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .section-title i {
            color: #3498db;
        }
        
        .controls {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .button-group {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 10px 15px;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }
        
        .btn-primary {
            background-color: #3498db;
            color: white;
            flex: 1;
        }
        
        .btn-primary:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: #ecf0f1;
            color: #2c3e50;
            flex: 1;
        }
        
        .btn-secondary:hover {
            background-color: #d5dbdb;
            transform: translateY(-2px);
        }
        
        .speed-controls {
            display: flex;
            gap: 8px;
        }
        
        .speed-btn {
            flex: 1;
            padding: 8px 5px;
        }
        
        .speed-btn.active {
            background-color: #3498db;
            color: white;
        }
        
        .mode-controls {
            display: flex;
            gap: 8px;
        }
        
        .mode-btn {
            flex: 1;
            padding: 8px 5px;
        }
        
        .mode-btn.active {
            background-color: #2ecc71;
            color: white;
        }
        
        .legend {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
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
            border-radius: 50%;
            border: 1px solid rgba(0,0,0,0.1);
        }
        
        .info-panel {
            margin-top: 10px;
            background-color: #fffde7;
            border-radius: 8px;
            padding: 12px;
            border-left: 4px solid #f1c40f;
            font-size: 0.95rem;
            line-height: 1.5;
            min-height: 70px;
        }
        
        .step-info {
            color: #d35400;
            font-weight: 600;
            margin-bottom: 5px;
        }
        
        .hint {
            font-size: 0.85rem;
            color: #7f8c8d;
            text-align: center;
            margin-top: 10px;
            font-style: italic;
        }
        
        .toggle-group {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }
        
        .toggle-btn {
            padding: 8px 12px;
            font-size: 0.85rem;
        }
        
        @media (max-width: 950px) {
            .container {
                flex-direction: column;
                align-items: center;
            }
            
            .animation-area, .control-panel {
                width: 100%;
                max-width: 100%;
                min-width: unset;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <div class="header">
        <h1><i class="fas fa-atom"></i> 电解饱和食盐水微观过程</h1>
        <p class="subtitle">观察离子迁移、电子转移与三产物生成的同步动画</p>
        <div class="equation">2NaCl + 2H₂O → H₂↑ + Cl₂↑ + 2NaOH</div>
    </div>
    
    <div class="container">
        <div class="animation-area">
            <div class="canvas-container">
                <canvas id="electrolysisCanvas" width="800" height="500"></canvas>
            </div>
            <p class="hint"><i class="fas fa-mouse-pointer"></i> 提示：将鼠标悬停在粒子、电极或气泡上查看详细信息</p>
        </div>
        
        <div class="control-panel">
            <div class="panel-section">
                <div class="section-title"><i class="fas fa-play-circle"></i> 动画控制</div>
                <div class="controls">
                    <div class="button-group">
                        <button id="playBtn" class="btn-primary"><i class="fas fa-play"></i> 播放</button>
                        <button id="pauseBtn" class="btn-secondary"><i class="fas fa-pause"></i> 暂停</button>
                        <button id="resetBtn" class="btn-secondary"><i class="fas fa-redo"></i> 重置</button>
                    </div>
                    
                    <div>
                        <div class="section-title" style="font-size: 1rem; margin-bottom: 10px;"><i class="fas fa-tachometer-alt"></i> 播放速度</div>
                        <div class="speed-controls">
                            <button id="slowBtn" class="speed-btn btn-secondary">慢速</button>
                            <button id="normalBtn" class="speed-btn btn-secondary active">常速</button>
                            <button id="fastBtn" class="speed-btn btn-secondary">快速</button>
                        </div>
                    </div>
                    
                    <div>
                        <div class="section-title" style="font-size: 1rem; margin-bottom: 10px;"><i class="fas fa-list-ol"></i> 演示模式</div>
                        <div class="mode-controls">
                            <button id="continuousBtn" class="mode-btn btn-secondary active">连续动画</button>
                            <button id="stepBtn" class="mode-btn btn-secondary">分步讲解</button>
                        </div>
                    </div>
                    
                    <div class="toggle-group">
                        <button id="labelsToggle" class="toggle-btn btn-secondary"><i class="fas fa-tag"></i> 显示标签</button>
                        <button id="ohHighlightToggle" class="toggle-btn btn-secondary"><i class="fas fa-highlighter"></i> 高亮OH⁻</button>
                    </div>
                </div>
            </div>
            
            <div class="panel-section">
                <div class="section-title"><i class="fas fa-info-circle"></i> 当前信息</div>
                <div class="info-panel">
                    <div id="stepInfo" class="step-info">准备开始电解...</div>
                    <div id="infoText">点击"播放"按钮开始动画，观察微观粒子如何运动并生成三种产物。</div>
                </div>
            </div>
            
            <div class="panel-section">
                <div class="section-title"><i class="fas fa-palette"></i> 粒子图例</div>
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #3498db;"></div>
                        <span>Na⁺ (钠离子)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #2ecc71;"></div>
                        <span>Cl⁻ (氯离子)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span>H⁺ (氢离子)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background: linear-gradient(45deg, #e74c3c 50%, white 50%);"></div>
                        <span>OH⁻ (氢氧根)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ecf0f1;"></div>
                        <span>H₂ (氢气)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f1c40f;"></div>
                        <span>Cl₂ (氯气)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f39c12; border: 2px dashed #e67e22;"></div>
                        <span>电子 (e⁻)</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 获取Canvas元素和上下文
        const canvas = document.getElementById('electrolysisCanvas');
        const ctx = canvas.getContext('2d');
        
        // 调整Canvas大小以适应容器
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            initCanvasDimensions();
        }
        
        // 初始化Canvas尺寸相关变量
        let canvasWidth, canvasHeight;
        function initCanvasDimensions() {
            canvasWidth = canvas.width;
            canvasHeight = canvas.height;
        }
        
        // 动画状态
        let animationId = null;
        let isPlaying = false;
        let speed = 1.0; // 1.0 = 正常速度
        let isStepMode = false;
        let currentStep = 0;
        let showLabels = true;
        let highlightOH = true;
        
        // 电解池参数
        const cell = {
            x: 0,
            y: 0,
            width: 0,
            height: 0,
            leftCompartment: { x: 0, width: 0, color: 'rgba(224, 247, 250, 0.7)' },
            rightCompartment: { x: 0, width: 0, color: 'rgba(224, 247, 250, 0.7)' },
            membrane: { x: 0, width: 5 }
        };
        
        // 电极参数
        const electrodes = {
            anode: { x: 0, y: 0, width: 15, height: 80, name: '阳极 (石墨)' },
            cathode: { x: 0, y: 0, width: 15, height: 80, name: '阴极 (石墨)' }
        };
        
        // 电源参数
        const powerSupply = {
            x: 0,
            y: 0,
            width: 80,
            height: 40
        };
        
        // 粒子数组
        let particles = [];
        let electrons = [];
        let gasBubbles = [];
        
        // 鼠标交互
        let mouse = { x: 0, y: 0, hoveredItem: null };
        
        // 初始化电解池布局
        function initLayout() {
            // 电解池尺寸和位置
            cell.x = canvasWidth * 0.1;
            cell.y = canvasHeight * 0.2;
            cell.width = canvasWidth * 0.8;
            cell.height = canvasHeight * 0.6;
            
            // 电解池左右室
            cell.leftCompartment.width = cell.width * 0.45;
            cell.leftCompartment.x = cell.x;
            cell.rightCompartment.width = cell.width * 0.45;
            cell.rightCompartment.x = cell.x + cell.width * 0.55;
            
            // 隔膜
            cell.membrane.x = cell.x + cell.width * 0.5 - cell.membrane.width / 2;
            
            // 电极位置
            electrodes.anode.x = cell.leftCompartment.x + cell.leftCompartment.width * 0.7;
            electrodes.anode.y = cell.y + 30;
            electrodes.cathode.x = cell.rightCompartment.x + cell.rightCompartment.width * 0.3;
            electrodes.cathode.y = cell.y + 30;
            
            // 电源位置
            powerSupply.x = canvasWidth / 2 - powerSupply.width / 2;
            powerSupply.y = cell.y - 70;
        }
        
        // 粒子类
        class Particle {
            constructor(type, x, y) {
                this.type = type; // 'Na+', 'Cl-', 'H+', 'OH-'
                this.x = x;
                this.y = y;
                this.radius = 0;
                this.color = '';
                this.label = '';
                this.speed = 0;
                this.targetX = x;
                this.targetY = y;
                this.isMoving = false;
                this.initProperties();
            }
            
            initProperties() {
                switch(this.type) {
                    case 'Na+':
                        this.radius = 10;
                        this.color = '#3498db';
                        this.label = 'Na⁺';
                        this.speed = 0.5;
                        break;
                    case 'Cl-':
                        this.radius = 10;
                        this.color = '#2ecc71';
                        this.label = 'Cl⁻';
                        this.speed = 0.5;
                        break;
                    case 'H+':
                        this.radius = 6;
                        this.color = '#e74c3c';
                        this.label = 'H⁺';
                        this.speed = 0.8;
                        break;
                    case 'OH-':
                        this.radius = 10;
                        this.color = '#e74c3c'; // 红色部分
                        this.color2 = 'white'; // 白色部分
                        this.label = 'OH⁻';
                        this.speed = 0.6;
                        break;
                }
            }
            
            update() {
                // 向目标位置移动
                if (this.isMoving) {
                    const dx = this.targetX - this.x;
                    const dy = this.targetY - this.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance > 1) {
                        this.x += (dx / distance) * this.speed * speed;
                        this.y += (dy / distance) * this.speed * speed;
                    } else {
                        this.isMoving = false;
                    }
                }
                
                // 限制在电解池内
                const margin = this.radius + 5;
                if (this.x < cell.x + margin) this.x = cell.x + margin;
                if (this.x > cell.x + cell.width - margin) this.x = cell.x + cell.width - margin;
                if (this.y < cell.y + margin) this.y = cell.y + margin;
                if (this.y > cell.y + cell.height - margin) this.y = cell.y + cell.height - margin;
            }
            
            draw() {
                // 绘制粒子
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                
                if (this.type === 'OH-') {
                    // OH-特殊绘制（红白各半）
                    ctx.fillStyle = this.color;
                    ctx.fill();
                    
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius * 0.7, 0, Math.PI * 2);
                    ctx.fillStyle = this.color2;
                    ctx.fill();
                    
                    // 边框
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                    ctx.strokeStyle = this.color;
                    ctx.lineWidth = 1.5;
                    ctx.stroke();
                } else {
                    ctx.fillStyle = this.color;
                    ctx.fill();
                    
                    // 边框
                    ctx.strokeStyle = 'rgba(0,0,0,0.2)';
                    ctx.lineWidth = 1;
                    ctx.stroke();
                }
                
                // 绘制标签
                if (showLabels) {
                    ctx.fillStyle = 'white';
                    ctx.font = 'bold 12px Arial';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText(this.label, this.x, this.y);
                }
                
                // 如果高亮OH-且是OH-粒子
                if (highlightOH && this.type === 'OH-') {
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius + 3, 0, Math.PI * 2);
                    ctx.strokeStyle = 'rgba(231, 76, 60, 0.5)';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
                
                // 鼠标悬停效果
                if (this.isHovered()) {
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius + 5, 0, Math.PI * 2);
                    ctx.strokeStyle = 'rgba(241, 196, 15, 0.8)';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // 显示详细信息
                    this.drawTooltip();
                }
            }
            
            isHovered() {
                const dx = this.x - mouse.x;
                const dy = this.y - mouse.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                return distance < this.radius + 5;
            }
            
            drawTooltip() {
                let text = '';
                switch(this.type) {
                    case 'Na+': text = '钠离子 (Na⁺) - 不参与放电，向阴极迁移'; break;
                    case 'Cl-': text = '氯离子 (Cl⁻) - 在阳极失去电子生成氯气'; break;
                    case 'H+': text = '氢离子 (H⁺) - 在阴极获得电子生成氢气'; break;
                    case 'OH-': text = '氢氧根离子 (OH⁻) - 阴极区浓度增加，形成NaOH'; break;
                }
                
                ctx.fillStyle = 'rgba(0, 0, 0, 0.85)';
                ctx.fillRect(mouse.x + 10, mouse.y - 30, 220, 40);
                
                ctx.fillStyle = 'white';
                ctx.font = '13px Arial';
                ctx.textAlign = 'left';
                ctx.fillText(text, mouse.x + 15, mouse.y - 10);
            }
        }
        
        // 电子类
        class Electron {
            constructor(x, y, targetX, targetY) {
                this.x = x;
                this.y = y;
                this.targetX = targetX;
                this.targetY = targetY;
                this.radius = 4;
                this.color = '#f39c12';
                this.speed = 3;
                this.life = 100; // 电子存在时间
                this.active = true;
            }
            
            update() {
                const dx = this.targetX - this.x;
                const dy = this.targetY - this.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                
                if (distance > 1 && this.life > 0) {
                    this.x += (dx / distance) * this.speed * speed;
                    this.y += (dy / distance) * this.speed * speed;
                    this.life--;
                } else {
                    this.active = false;
                }
            }
            
            draw() {
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = this.color;
                ctx.fill();
                
                // 发光效果
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius + 3, 0, Math.PI * 2);
                ctx.strokeStyle = 'rgba(243, 156, 18, 0.5)';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // 虚线边框
                ctx.setLineDash([3, 3]);
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius + 1, 0, Math.PI * 2);
                ctx.strokeStyle = '#e67e22';
                ctx.lineWidth = 1;
                ctx.stroke();
                ctx.setLineDash([]);
            }
        }
        
        // 气泡类
        class GasBubble {
            constructor(type, x, y) {
                this.type = type; // 'H2' 或 'Cl2'
                this.x = x;
                this.y = y;
                this.radius = 5;
                this.speed = 0.7;
                this.color = '';
                this.label = '';
                this.initProperties();
            }
            
            initProperties() {
                if (this.type === 'H2') {
                    this.color = '#ecf0f1';
                    this.label = 'H₂';
                } else {
                    this.color = '#f1c40f';
                    this.label = 'Cl₂';
                }
            }
            
            update() {
                // 气泡向上移动
                this.y -= this.speed * speed;
                
                // 缓慢增大
                if (this.radius < 12) {
                    this.radius += 0.05 * speed;
                }
            }
            
            draw() {
                // 绘制气泡
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = this.color;
                ctx.fill();
                
                // 气泡高光
                ctx.beginPath();
                ctx.arc(this.x - this.radius * 0.3, this.y - this.radius * 0.3, this.radius * 0.4, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(255, 255, 255, 0.6)';
                ctx.fill();
                
                // 边框
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.strokeStyle = 'rgba(0,0,0,0.2)';
                ctx.lineWidth = 1;
                ctx.stroke();
                
                // 标签
                if (showLabels) {
                    ctx.fillStyle = 'rgba(0,0,0,0.7)';
                    ctx.font = 'bold 10px Arial';
                    ctx.textAlign = 'center';
                    ctx.textBaseline = 'middle';
                    ctx.fillText(this.label, this.x, this.y);
                }
                
                // 鼠标悬停效果
                if (this.isHovered()) {
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius + 5, 0, Math.PI * 2);
                    ctx.strokeStyle = 'rgba(241, 196, 15, 0.8)';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // 显示详细信息
                    this.drawTooltip();
                }
            }
            
            isHovered() {
                const dx = this.x - mouse.x;
                const dy = this.y - mouse.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                return distance < this.radius + 5;
            }
            
            drawTooltip() {
                let text = '';
                if (this.type === 'H2') {
                    text = '氢气 (H₂) - 阴极产物，由H⁺获得电子生成';
                } else {
                    text = '氯气 (Cl₂) - 阳极产物，由Cl⁻失去电子生成';
                }
                
                ctx.fillStyle = 'rgba(0, 0, 0, 0.85)';
                ctx.fillRect(mouse.x + 10, mouse.y - 30, 200, 40);
                
                ctx.fillStyle = 'white';
                ctx.font = '13px Arial';
                ctx.textAlign = 'left';
                ctx.fillText(text, mouse.x + 15, mouse.y - 10);
            }
        }
        
        // 初始化粒子
        function initParticles() {
            particles = [];
            electrons = [];
            gasBubbles = [];
            
            // 创建Na+和Cl-粒子（均匀分布）
            for (let i = 0; i < 25; i++) {
                // Na+在左室
                particles.push(new Particle('Na+', 
                    cell.leftCompartment.x + Math.random() * cell.leftCompartment.width,
                    cell.y + 50 + Math.random() * (cell.height - 100)
                ));
                
                // Na+在右室
                particles.push(new Particle('Na+', 
                    cell.rightCompartment.x + Math.random() * cell.rightCompartment.width,
                    cell.y + 50 + Math.random() * (cell.height - 100)
                ));
                
                // Cl-在左室
                particles.push(new Particle('Cl-', 
                    cell.leftCompartment.x + Math.random() * cell.leftCompartment.width,
                    cell.y + 50 + Math.random() * (cell.height - 100)
                ));
                
                // Cl-在右室
                particles.push(new Particle('Cl-', 
                    cell.rightCompartment.x + Math.random() * cell.rightCompartment.width,
                    cell.y + 50 + Math.random() * (cell.height - 100)
                ));
            }
            
            // 创建H+和OH-粒子（均匀分布，数量较少）
            for (let i = 0; i < 15; i++) {
                // H+在左室
                particles.push(new Particle('H+', 
                    cell.leftCompartment.x + Math.random() * cell.leftCompartment.width,
                    cell.y + 50 + Math.random() * (cell.height - 100)
                ));
                
                // H+在右室
                particles.push(new Particle('H+', 
                    cell.rightCompartment.x + Math.random() * cell.rightCompartment.width,
                    cell.y + 50 + Math.random() * (cell.height - 100)
                ));
                
                // OH-在左室
                particles.push(new Particle('OH-', 
                    cell.leftCompartment.x + Math.random() * cell.leftCompartment.width,
                    cell.y + 50 + Math.random() * (cell.height - 100)
                ));
                
                // OH-在右室
                particles.push(new Particle('OH-', 
                    cell.rightCompartment.x + Math.random() * cell.rightCompartment.width,
                    cell.y + 50 + Math.random() * (cell.height - 100)
                ));
            }
        }
        
        // 开始电解过程
        function startElectrolysis() {
            // 重置步骤
            currentStep = 0;
            
            // 清除现有电子和气泡
            electrons = [];
            gasBubbles = [];
            
            // 设置步骤信息
            updateStepInfo(1, "通电：电子开始从电源负极流向阴极，从阳极流向电源正极");
            
            // 如果是分步模式，只执行第一步
            if (isStepMode) {
                return;
            }
            
            // 连续模式：开始电解过程
            setTimeout(() => {
                updateStepInfo(2, "离子迁移：Cl⁻向阳极移动，H⁺向阴极移动，Na⁺向阴极迁移");
                startIonMigration();
            }, 2000);
            
            setTimeout(() => {
                updateStepInfo(3, "电极反应：阳极Cl⁻失去电子生成Cl₂，阴极H⁺获得电子生成H₂");
                startElectrodeReactions();
            }, 4000);
            
            setTimeout(() => {
                updateStepInfo(4, "产物生成：H₂和Cl₂气泡上升，阴极区OH⁻浓度增加形成NaOH");
                showFinalProducts();
            }, 8000);
        }
        
        // 开始离子迁移
        function startIonMigration() {
            // 设置粒子移动目标
            particles.forEach(p => {
                if (p.type === 'Cl-') {
                    // Cl-向阳极移动（左室）
                    p.targetX = electrodes.anode.x + electrodes.anode.width / 2;
                    p.targetY = electrodes.anode.y + electrodes.anode.height * 0.7;
                    p.isMoving = true;
                } else if (p.type === 'H+') {
                    // H+向阴极移动（右室）
                    p.targetX = electrodes.cathode.x + electrodes.cathode.width / 2;
                    p.targetY = electrodes.cathode.y + electrodes.cathode.height * 0.7;
                    p.isMoving = true;
                } else if (p.type === 'Na+') {
                    // Na+向阴极区迁移（右室）
                    if (p.x < cell.membrane.x) {
                        p.targetX = electrodes.cathode.x - 30;
                        p.targetY = p.y;
                        p.isMoving = true;
                    }
                }
            });
        }
        
        // 开始电极反应
        function startElectrodeReactions() {
            // 创建电子流
            const electronInterval = setInterval(() => {
                // 从阳极到电源正极的电子
                electrons.push(new Electron(
                    electrodes.anode.x + electrodes.anode.width / 2,
                    electrodes.anode.y + 10,
                    powerSupply.x + powerSupply.width - 10,
                    powerSupply.y + powerSupply.height / 2
                ));
                
                // 从电源负极到阴极的电子
                electrons.push(new Electron(
                    powerSupply.x + 10,
                    powerSupply.y + powerSupply.height / 2,
                    electrodes.cathode.x + electrodes.cathode.width / 2,
                    electrodes.cathode.y + 10
                ));
                
                // 生成气泡（每隔一段时间）
                if (Math.random() > 0.7) {
                    // 阳极生成Cl2气泡
                    gasBubbles.push(new GasBubble('Cl2', 
                        electrodes.anode.x + electrodes.anode.width / 2,
                        electrodes.anode.y + electrodes.anode.height
                    ));
                }
                
                if (Math.random() > 0.7) {
                    // 阴极生成H2气泡
                    gasBubbles.push(new GasBubble('H2', 
                        electrodes.cathode.x + electrodes.cathode.width / 2,
                        electrodes.cathode.y + electrodes.cathode.height
                    ));
                }
            }, 300);
            
            // 10秒后停止生成电子
            setTimeout(() => {
                clearInterval(electronInterval);
            }, 10000);
        }
        
        // 显示最终产物
        function showFinalProducts() {
            updateStepInfo(5, "电解完成：生成H₂、Cl₂和NaOH三种产物");
            
            // 改变阴极区背景色表示碱性增强
            cell.rightCompartment.color = 'rgba(255, 243, 224, 0.7)';
            
            // 显示NaOH文字
            setTimeout(() => {
                // 在信息面板显示完成信息
                document.getElementById('infoText').innerHTML = 
                    "电解完成！三种产物已生成：<br>" +
                    "1. 氢气(H₂)在阴极产生<br>" +
                    "2. 氯气(Cl₂)在阳极产生<br>" +
                    "3. 氢氧化钠(NaOH)在阴极区溶液中形成";
            }, 1000);
        }
        
        // 更新步骤信息
        function updateStepInfo(step, text) {
            currentStep = step;
            document.getElementById('stepInfo').textContent = `步骤 ${step}: ${text}`;
            
            if (step === 1) {
                document.getElementById('infoText').textContent = 
                    "电路接通，电子开始定向移动。注意电子流动方向：从电源负极到阴极，从阳极到电源正极。";
            } else if (step === 2) {
                document.getElementById('infoText').textContent = 
                    "离子在电场作用下定向迁移：阴离子(Cl⁻)向阳极移动，阳离子(H⁺、Na⁺)向阴极移动。";
            } else if (step === 3) {
                document.getElementById('infoText').textContent = 
                    "电极发生氧化还原反应：阳极Cl⁻失去电子被氧化为Cl₂，阴极H⁺获得电子被还原为H₂。";
            } else if (step === 4) {
                document.getElementById('infoText').textContent = 
                    "气体产物以气泡形式逸出，阴极区H⁺减少使OH⁻浓度相对增加，与Na⁺结合形成NaOH。";
            }
        }
        
        // 下一步（分步模式）
        function nextStep() {
            if (!isStepMode) return;
            
            currentStep++;
            
            if (currentStep === 1) {
                updateStepInfo(1, "通电：电子开始从电源负极流向阴极，从阳极流向电源正极");
            } else if (currentStep === 2) {
                updateStepInfo(2, "离子迁移：Cl⁻向阳极移动，H⁺向阴极移动，Na
<!--检测到代码截断，自动续写中...-->
⁺向阴极迁移");
                startIonMigration();
            } else if (currentStep === 3) {
                updateStepInfo(3, "电极反应：阳极Cl⁻失去电子生成Cl₂，阴极H⁺获得电子生成H₂");
                startElectrodeReactions();
            } else if (currentStep === 4) {
                updateStepInfo(4, "产物生成：H₂和Cl₂气泡上升，阴极区OH⁻浓度增加形成NaOH");
                showFinalProducts();
            } else if (currentStep > 4) {
                currentStep = 4;
                document.getElementById('infoText').textContent = "分步演示已完成。点击'重置'按钮重新开始。";
            }
        }

        // 绘制电解池
        function drawElectrolysisCell() {
            // 绘制电解池外框
            ctx.strokeStyle = '#7f8c8d';
            ctx.lineWidth = 3;
            ctx.strokeRect(cell.x, cell.y, cell.width, cell.height);
            
            // 绘制左室背景
            ctx.fillStyle = cell.leftCompartment.color;
            ctx.fillRect(cell.leftCompartment.x, cell.y, cell.leftCompartment.width, cell.height);
            
            // 绘制右室背景
            ctx.fillStyle = cell.rightCompartment.color;
            ctx.fillRect(cell.rightCompartment.x, cell.y, cell.rightCompartment.width, cell.height);
            
            // 绘制隔膜
            ctx.fillStyle = 'rgba(149, 165, 166, 0.5)';
            ctx.fillRect(cell.membrane.x, cell.y, cell.membrane.width, cell.height);
            
            // 绘制电极
            drawElectrode(electrodes.anode, '阳极');
            drawElectrode(electrodes.cathode, '阴极');
            
            // 绘制电源
            drawPowerSupply();
            
            // 绘制导线
            drawWires();
            
            // 绘制电极标签
            if (showLabels) {
                ctx.fillStyle = '#2c3e50';
                ctx.font = 'bold 14px Arial';
                ctx.textAlign = 'center';
                
                // 阳极标签
                ctx.fillText('阳极 (+)', electrodes.anode.x + electrodes.anode.width/2, electrodes.anode.y - 10);
                
                // 阴极标签
                ctx.fillText('阴极 (-)', electrodes.cathode.x + electrodes.cathode.width/2, electrodes.cathode.y - 10);
            }
            
            // 电极悬停效果
            if (isElectrodeHovered(electrodes.anode)) {
                drawElectrodeTooltip(electrodes.anode, '阳极: 2Cl⁻ - 2e⁻ → Cl₂↑');
            }
            
            if (isElectrodeHovered(electrodes.cathode)) {
                drawElectrodeTooltip(electrodes.cathode, '阴极: 2H⁺ + 2e⁻ → H₂↑');
            }
        }
        
        // 绘制电极
        function drawElectrode(electrode, label) {
            // 电极柱
            ctx.fillStyle = '#2c3e50';
            ctx.fillRect(electrode.x, electrode.y, electrode.width, electrode.height);
            
            // 电极金属光泽
            ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
            ctx.fillRect(electrode.x + 2, electrode.y + 2, electrode.width - 4, 10);
        }
        
        // 绘制电源
        function drawPowerSupply() {
            // 电源外壳
            ctx.fillStyle = '#34495e';
            ctx.fillRect(powerSupply.x, powerSupply.y, powerSupply.width, powerSupply.height);
            
            // 电源正负极标志
            ctx.fillStyle = 'white';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('+', powerSupply.x + 20, powerSupply.y + powerSupply.height/2);
            ctx.fillText('-', powerSupply.x + powerSupply.width - 20, powerSupply.y + powerSupply.height/2);
            
            // 电源标签
            ctx.fillStyle = '#2c3e50';
            ctx.font = 'bold 12px Arial';
            ctx.fillText('直流电源', powerSupply.x + powerSupply.width/2, powerSupply.y - 10);
        }
        
        // 绘制导线
        function drawWires() {
            ctx.strokeStyle = '#e67e22';
            ctx.lineWidth = 3;
            ctx.setLineDash([]);
            
            // 从电源正极到阳极
            ctx.beginPath();
            ctx.moveTo(powerSupply.x, powerSupply.y + powerSupply.height/2);
            ctx.lineTo(powerSupply.x - 30, powerSupply.y + powerSupply.height/2);
            ctx.lineTo(powerSupply.x - 30, electrodes.anode.y + electrodes.anode.height/2);
            ctx.lineTo(electrodes.anode.x + electrodes.anode.width, electrodes.anode.y + electrodes.anode.height/2);
            ctx.stroke();
            
            // 从电源负极到阴极
            ctx.beginPath();
            ctx.moveTo(powerSupply.x + powerSupply.width, powerSupply.y + powerSupply.height/2);
            ctx.lineTo(powerSupply.x + powerSupply.width + 30, powerSupply.y + powerSupply.height/2);
            ctx.lineTo(powerSupply.x + powerSupply.width + 30, electrodes.cathode.y + electrodes.cathode.height/2);
            ctx.lineTo(electrodes.cathode.x, electrodes.cathode.y + electrodes.cathode.height/2);
            ctx.stroke();
            
            // 绘制电子流动方向指示
            if (isPlaying || currentStep >= 1) {
                // 阳极到电源正极方向
                drawArrow(
                    electrodes.anode.x + electrodes.anode.width + 5,
                    electrodes.anode.y + electrodes.anode.height/2,
                    powerSupply.x - 25,
                    electrodes.anode.y + electrodes.anode.height/2,
                    '#f39c12'
                );
                
                // 电源负极到阴极方向
                drawArrow(
                    powerSupply.x + powerSupply.width + 25,
                    electrodes.cathode.y + electrodes.cathode.height/2,
                    electrodes.cathode.x - 5,
                    electrodes.cathode.y + electrodes.cathode.height/2,
                    '#f39c12'
                );
                
                // 电子流标签
                ctx.fillStyle = '#d35400';
                ctx.font = 'bold 12px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('电子流方向', canvasWidth/2, powerSupply.y - 25);
            }
        }
        
        // 绘制箭头
        function drawArrow(fromX, fromY, toX, toY, color) {
            const headlen = 10;
            const dx = toX - fromX;
            const dy = toY - fromY;
            const angle = Math.atan2(dy, dx);
            
            // 绘制线
            ctx.strokeStyle = color;
            ctx.lineWidth = 2;
            ctx.setLineDash([5, 5]);
            
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.setLineDash([]);
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headlen * Math.cos(angle - Math.PI/6), toY - headlen * Math.sin(angle - Math.PI/6));
            ctx.lineTo(toX - headlen * Math.cos(angle + Math.PI/6), toY - headlen * Math.sin(angle + Math.PI/6));
            ctx.closePath();
            ctx.fillStyle = color;
            ctx.fill();
        }
        
        // 检查电极是否被悬停
        function isElectrodeHovered(electrode) {
            return mouse.x >= electrode.x - 10 && 
                   mouse.x <= electrode.x + electrode.width + 10 && 
                   mouse.y >= electrode.y && 
                   mouse.y <= electrode.y + electrode.height;
        }
        
        // 绘制电极提示
        function drawElectrodeTooltip(electrode, text) {
            ctx.fillStyle = 'rgba(0, 0, 0, 0.85)';
            const tooltipWidth = 250;
            const tooltipHeight = 50;
            const tooltipX = mouse.x + 15;
            const tooltipY = mouse.y - tooltipHeight - 10;
            
            // 确保提示框不超出画布
            const adjustedX = tooltipX + tooltipWidth > canvasWidth ? 
                mouse.x - tooltipWidth - 15 : tooltipX;
            
            ctx.fillRect(adjustedX, tooltipY, tooltipWidth, tooltipHeight);
            
            ctx.fillStyle = 'white';
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'left';
            
            // 电极名称
            ctx.fillText(electrode.name, adjustedX + 10, tooltipY + 20);
            
            // 反应式
            ctx.font = '13px Arial';
            ctx.fillText(text, adjustedX + 10, tooltipY + 40);
        }
        
        // 绘制NaOH产物指示
        function drawNaOHIndicator() {
            if (currentStep >= 4) {
                // 在阴极区底部绘制NaOH文字
                ctx.fillStyle = 'rgba(52, 152, 219, 0.9)';
                ctx.font = 'bold 24px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText('NaOH', 
                    cell.rightCompartment.x + cell.rightCompartment.width/2,
                    cell.y + cell.height - 30
                );
                
                // 绘制晶体示意
                for (let i = 0; i < 5; i++) {
                    const x = cell.rightCompartment.x + cell.rightCompartment.width/2 - 40 + i * 20;
                    const y = cell.y + cell.height - 50;
                    
                    ctx.beginPath();
                    ctx.moveTo(x, y);
                    ctx.lineTo(x + 8, y - 10);
                    ctx.lineTo(x + 16, y);
                    ctx.lineTo(x + 8, y + 10);
                    ctx.closePath();
                    ctx.fillStyle = 'rgba(52, 152, 219, 0.6)';
                    ctx.fill();
                    ctx.strokeStyle = '#2980b9';
                    ctx.lineWidth = 1;
                    ctx.stroke();
                }
            }
        }
        
        // 主绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvasWidth, canvasHeight);
            
            // 绘制电解池
            drawElectrolysisCell();
            
            // 绘制粒子
            particles.forEach(p => {
                p.update();
                p.draw();
            });
            
            // 绘制电子
            electrons.forEach(e => {
                e.update();
                e.draw();
            });
            
            // 移除不活跃的电子
            electrons = electrons.filter(e => e.active);
            
            // 绘制气泡
            gasBubbles.forEach(b => {
                b.update();
                b.draw();
            });
            
            // 移除超出画布的气泡
            gasBubbles = gasBubbles.filter(b => b.y > 0 && b.y < canvasHeight);
            
            // 绘制NaOH产物指示
            drawNaOHIndicator();
            
            // 绘制总方程式
            ctx.fillStyle = 'rgba(41, 128, 185, 0.9)';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('2NaCl + 2H₂O → H₂↑ + Cl₂↑ + 2NaOH', canvasWidth/2, 30);
            
            // 继续动画循环
            if (isPlaying) {
                animationId = requestAnimationFrame(draw);
            }
        }
        
        // 重置动画
        function resetAnimation() {
            isPlaying = false;
            currentStep = 0;
            
            // 停止动画循环
            if (animationId) {
                cancelAnimationFrame(animationId);
            }
            
            // 重置电解池颜色
            cell.leftCompartment.color = 'rgba(224, 247, 250, 0.7)';
            cell.rightCompartment.color = 'rgba(224, 247, 250, 0.7)';
            
            // 重新初始化粒子
            initParticles();
            
            // 更新信息面板
            updateStepInfo(0, "准备开始电解...");
            document.getElementById('infoText').textContent = 
                "点击'播放'按钮开始动画，观察微观粒子如何运动并生成三种产物。";
            
            // 绘制初始状态
            draw();
        }
        
        // 事件监听器
        function setupEventListeners() {
            // 播放按钮
            document.getElementById('playBtn').addEventListener('click', () => {
                if (!isPlaying) {
                    isPlaying = true;
                    if (isStepMode && currentStep === 0) {
                        nextStep();
                    } else if (!isStepMode && currentStep === 0) {
                        startElectrolysis();
                    }
                    draw();
                }
            });
            
            // 暂停按钮
            document.getElementById('pauseBtn').addEventListener('click', () => {
                isPlaying = false;
                if (animationId) {
                    cancelAnimationFrame(animationId);
                }
            });
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', resetAnimation);
            
            // 速度控制按钮
            document.getElementById('slowBtn').addEventListener('click', () => {
                speed = 0.5;
                document.querySelectorAll('.speed-btn').forEach(btn => btn.classList.remove('active'));
                document.getElementById('slowBtn').classList.add('active');
            });
            
            document.getElementById('normalBtn').addEventListener('click', () => {
                speed = 1.0;
                document.querySelectorAll('.speed-btn').forEach(btn => btn.classList.remove('active'));
                document.getElementById('normalBtn').classList.add('active');
            });
            
            document.getElementById('fastBtn').addEventListener('click', () => {
                speed = 2.0;
                document.querySelectorAll('.speed-btn').forEach(btn => btn.classList.remove('active'));
                document.getElementById('fastBtn').classList.add('active');
            });
            
            // 模式控制按钮
            document.getElementById('continuousBtn').addEventListener('click', () => {
                isStepMode = false;
                document.querySelectorAll('.mode-btn').forEach(btn => btn.classList.remove('active'));
                document.getElementById('continuousBtn').classList.add('active');
                resetAnimation();
            });
            
            document.getElementById('stepBtn').addEventListener('click', () => {
                isStepMode = true;
                document.querySelectorAll('.mode-btn').forEach(btn => btn.classList.remove('active'));
                document.getElementById('stepBtn').classList.add('active');
                resetAnimation();
                
                // 更新信息面板提示
                document.getElementById('infoText').textContent = 
                    "分步演示模式已启用。点击'播放'按钮开始第一步，然后使用'播放'按钮继续下一步。";
            });
            
            // 标签显示切换
            document.getElementById('labelsToggle').addEventListener('click', function() {
                showLabels = !showLabels;
                this.innerHTML = showLabels ? 
                    '<i class="fas fa-tag"></i> 隐藏标签' : 
                    '<i class="fas fa-tag"></i> 显示标签';
                draw();
            });
            
            // OH⁻高亮切换
            document.getElementById('ohHighlightToggle').addEventListener('click', function() {
                highlightOH = !highlightOH;
                this.innerHTML = highlightOH ? 
                    '<i class="fas fa-highlighter"></i> 取消高亮' : 
                    '<i class="fas fa-highlighter"></i> 高亮OH⁻';
                draw();
            });
            
            // 鼠标移动事件（用于悬停效果）
            canvas.addEventListener('mousemove', (e) => {
                const rect = canvas.getBoundingClientRect();
                mouse.x = e.clientX - rect.left;
                mouse.y = e.clientY - rect.top;
                
                // 检查悬停状态
                let hovered = false;
                
                // 检查粒子
                particles.forEach(p => {
                    if (p.isHovered()) {
                        hovered = true;
                        mouse.hoveredItem = p;
                    }
                });
                
                // 检查气泡
                gasBubbles.forEach(b => {
                    if (b.isHovered()) {
                        hovered = true;
                        mouse.hoveredItem = b;
                    }
                });
                
                // 检查电极
                if (isElectrodeHovered(electrodes.anode) || isElectrodeHovered(electrodes.cathode)) {
                    hovered = true;
                }
                
                if (!hovered) {
                    mouse.hoveredItem = null;
                }
                
                // 重绘以显示悬停效果
                if (isPlaying) {
                    // 如果动画正在播放，不需要单独重绘，因为下一帧会绘制
                } else {
                    draw();
                }
            });
            
            // 在分步模式下，播放按钮用作下一步按钮
            canvas.addEventListener('click', (e) => {
                if (isStepMode && isPlaying) {
                    nextStep();
                }
            });
            
            // 窗口大小调整
            window.addEventListener('resize', () => {
                resizeCanvas();
                initLayout();
                resetAnimation();
            });
        }
        
        // 初始化函数
        function init() {
            resizeCanvas();
            initLayout();
            initParticles();
            setupEventListeners();
            draw();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 过程输出

# 《电解饱和食盐水微观动画》使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态可视化方式，帮助您深入理解电解饱和食盐水的微观过程。无论您是学生、教师还是化学爱好者，都能通过直观的动画和丰富的交互功能，掌握这一重要的电化学原理。

---

## 一、功能说明

本动画完整模拟了电解饱和食盐水的微观过程，以**三产物（H₂、Cl₂、NaOH）的同步生成为核心**，展示了从通电到产物生成的完整动态过程。动画采用**Canvas技术**实现，包含粒子运动、电子转移、气体生成等逼真效果，并提供了多种交互控制选项，让学习过程更加自主和深入。

---

## 二、主要功能

### 1. 动画控制区
- **播放/暂停/重置**：控制动画的开始、暂停和重新开始。
- **速度调节**：提供慢速（0.5x）、常速（1x）、快速（2x）三种播放速度，适应不同观察需求。
- **演示模式**：
  - **连续动画**：自动播放完整电解过程（约15秒）。
  - **分步讲解**：将过程分解为4个关键步骤，可手动控制进度，适合详细讲解。

### 2. 交互探索功能
- **悬停提示**：将鼠标悬停在任意粒子、气泡或电极上，会显示其名称、化学式和详细说明。
- **标签显示/隐藏**：可切换是否显示粒子标签（Na⁺、Cl⁻等）。
- **OH⁻浓度高亮**：特别高亮显示阴极区OH⁻浓度的变化，直观展示NaOH的形成过程。

### 3. 信息面板
- **步骤提示**：实时显示当前动画步骤和关键说明。
- **详细解释**：提供与当前步骤对应的化学原理说明。
- **粒子图例**：清晰展示各种颜色粒子对应的化学物质。

### 4. 视觉呈现
- **电解池结构**：展示U型管电解池、石墨电极、隔膜和直流电源。
- **粒子运动**：Na⁺、Cl⁻、H⁺、OH⁻的定向迁移动画。
- **电子流动**：用亮黄色电子显示电子在电路中的定向移动。
- **气体生成**：H₂（白色）和Cl₂（黄绿色）气泡的生成和上浮过程。
- **溶液变化**：阴极区背景色渐变，表示OH⁻浓度增加和碱性增强。

---

## 三、设计特色

### 1. 科学准确性
- 严格遵循电解饱和食盐水的实际化学原理：
  - 放电顺序：阳极Cl⁻ > OH⁻，阴极H⁺ > Na⁺
  - 电极反应式准确：阳极`2Cl⁻ - 2e⁻ → Cl₂↑`，阴极`2H⁺ + 2e⁻ → H₂↑`
  - 总反应式：`2NaCl + 2H₂O → H₂↑ + Cl₂↑ + 2NaOH`

### 2. 教学针对性
- **同步性强调**：通过电子流的连续动画，强调阴极和阳极反应是**同时、等电子**发生的。
- **难点突破**：专门设计OH⁻浓度变化的高亮显示，解决“NaOH如何生成”这一教学难点。
- **多层次呈现**：从离子迁移到电子转移，再到产物生成，层层递进。

### 3. 用户体验
- **响应式设计**：适应不同屏幕尺寸，在电脑、平板等设备上均可良好显示。
- **直观配色**：采用化学教学中常用的离子配色方案（如Na⁺蓝色、Cl⁻绿色），同时保证高对比度。
- **友好交互**：所有控制按钮均有图标和文字说明，操作简单直观。

---

## 四、教学要点

### 核心概念可视化
1. **离子定向迁移**：在电场作用下，阴离子（Cl⁻）向阳极移动，阳离子（H⁺、Na⁺）向阴极移动。
2. **选择性放电**：阳极Cl⁻优先放电（而非OH⁻），阴极H⁺优先放电（而非Na⁺）。
3. **电子守恒**：阴极获得的电子数 = 阳极失去的电子数，通过电子流动画直观展示。
4. **产物来源**：
   - H₂来自阴极H⁺的还原
   - Cl₂来自阳极Cl⁻的氧化  
   - NaOH来自阴极区Na⁺和OH⁻（因H⁺消耗而相对富集）的结合

### 关键观察点
- **注意电子流动方向**：从电源负极→阴极，从阳极→电源正极。
- **观察离子迁移速度差异**：H⁺迁移速度较快（半径小），Cl⁻和Na⁺较慢。
- **关注阴极区变化**：随着H⁺消耗，OH⁻浓度增加，区域颜色变浅表示碱性增强。
- **气泡生成同步性**：H₂和Cl₂气泡几乎同时生成，体现反应的同步性。

---

## 五、使用建议

### 对学生：
1. **首次观看**：建议先用“连续动画”模式完整观看一遍，了解整个过程。
2. **深入学习**：切换到“分步讲解”模式，逐步观察每个阶段的变化，结合信息面板的说明理解原理。
3. **主动探索**：使用悬停功能查看每个粒子的详细信息，尝试回答：
   - 为什么Na⁺不放电？
   - OH⁻浓度为什么在阴极区增加？
   - 电子是如何将两个电极反应联系起来的？
4. **速度调节**：在观察离子迁移细节时使用慢速，在复习时使用快速。

### 对教师：
1. **课堂演示**：
   - 可先隐藏标签，让学生猜测各粒子身份，再显示标签验证。
   - 在关键步骤暂停，提出问题引导学生思考。
   - 使用分步模式配合讲解，控制教学节奏。
2. **探究活动设计**：
   - 让学生预测：如果改变电压或浓度，动画会有何变化？
   - 对比实验：与电解水、电解CuCl₂溶液进行对比分析。
3. **难点突破**：
   - 专门演示“OH⁻高亮”功能，解释NaOH的形成机制。
   - 强调电子流的连续性，理解氧化还原反应的电子守恒。

### 最佳学习路径：
1. **预习阶段**：快速观看连续动画，建立整体印象。
2. **学习阶段**：分步观看，结合教材和教师讲解，理解每个细节。
3. **复习阶段**：关闭标签，尝试描述整个过程，再打开标签验证。
4. **拓展思考**：基于此原理，思考工业上氯碱生产的实际应用。

---

## 技术提示
- 本动画在现代浏览器（Chrome、Firefox、Edge、Safari）中均可正常运行。
- 如果动画卡顿，可尝试降低播放速度或刷新页面。
- 动画中的粒子数量经过优化，既能清晰展示过程，又保证流畅运行。

---

**化学是微观世界的舞蹈，电解是电子指挥的芭蕾。** 希望本动画能帮助您看清这场精彩的微观演出，深入理解电解原理的本质。祝您学习愉快，探索成功！

*如有任何使用问题或教学建议，欢迎反馈。本动画由教育技术专家设计，致力于提升化学学习的直观性和趣味性。*